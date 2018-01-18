---
title: Auftragskopfzeilen und -positionen von Finance and Operations mit Sales synchronisieren
description: "Das Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Auftragskopfzeilen und -positionen von Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, mit Microsoft Dynamics 365 for Sales zu synchronisieren."
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c7b2ff6430e99661ee284f65089086df9fa5a1ad
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-order-headers-and-lines-from-finance-and-operations-to-sales"></a>Auftragskopfzeilen und -positionen von Finance and Operations mit Sales synchronisieren

[!include[banner](../includes/banner.md)]

Das Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Auftragskopfzeilen und -positionen von Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, mit Microsoft Dynamics 365 for Sales zu synchronisieren. 

## <a name="template-and-tasks"></a>Vorlage und Aufgaben

Die folgenden Vorlagen und zugrunde liegenden Aufgaben werden verwendet, um Auftragskopfzeilen und -positionen von Finance and Operations mit Sales zu synchronisieren:

- **Name der Vorlage in der Datenintegration** 

    - Aufträge (Finance and Operations nach Sales)
    
- **Namen der Aufgaben im Datenintegrationsprojekt**

    - OrderHeader
    - OrderLine

Synchronisiert die Aufgaben, die vor der Verkaufsrechnungskopf- und -Positionssynchronisierung erforderlich sind:

- Produkte (Finance and Operations nach Sales)
- Konten (Sales nach Finance and Operations) (wenn verwendet)
- Kontakte nach Debitoren (Sales nach Finance and Operations) (wenn verwendet)

## <a name="entity-set"></a>Entitätssatz

| Finance and Operations |    Common Data Service (CDS)         |     Vertrieb      |
|------------------------|----------------|----------------|
| CDS-Auftragskopfzeilen| SalesOrder     | SalesOrders |
| CDS-Auftragspositionen  | SalesOrderLine | SalesOrderDetails|

## <a name="entity-flow"></a>Entitätsfluss

Aufträge werden in Finance and Operations erstellt und mit Sales synchronisiert.

Filter in der Vorlage stellen sicher, dass nur relevante Aufträge in die Synchronisierung einfließen:

- Sowohl der Bestellungs- als auch der Rechnungsdebitor auf dem Auftrag, der aus Sales stammt, werden in die Synchronisierung einbezogen. In Finance and Operations werden die Felder **OrderingCustomerIsExternallyMaintained** und **InvoiceCustomerIsExternallyMaintained** verwendet, um die Synchronisierung in den Datenentitäten zu verfolgen.

- Der **Auftrag** in Finance and Operations muss bestätigt werden. Nur bestätigte Aufträge oder Aufträge mit fortgeschrittenem Verarbeitungsstatus (beispielsweise "Versendet" oder "Fakturiert") werden mit Sales synchronisiert.

- Nach dem Erstellen oder Ändern eines Auftrags, muss der Stapelverarbeitungsauftrag **Verkaufssummen berechnen** aus Finance and Operations ausgeführt werden. Nur die Aufträge mit den berechneten Gesamtumsätzen werden mit CDS und Sales synchronisiert.

> [!NOTE]
> Die Steuer für Belastungen auf dem **Auftragskopf** ist derzeit nicht in der Synchronisierung von Finance and Operations mit Sales enthalten. Der Grund dafür ist, dass Sales keine Steuerinformationen auf Kopfebene unterstützt. Die Steuer, die sich auf Belastungen auf Positionsebene bezieht, ist enthalten.

## <a name="prospect-to-cash-solution-for-sales"></a>Prospect to Cash-Lösung für Sales

Neue Felder werden der Entität **Auftrag** hinzugefügt und auf der Seite angezeigt:

- **Wird extern verwaltet** – Auf **Ja** gesetzt, wenn der Auftrag aus Finance and Operations stammt.

- **Verarbeitungsstatus** – Wird verwendet, um den Verarbeitungsstatus des Auftrags in Finance and Operations anzuzeigen. Werte sind:

    - Aktiv
    - Bestätigt
    - Lieferschein
    - Fakturiert
    - Entnommen
    - Teilweise kommissioniert
    - Teilweise verpackt
    - Versendet
    - Teilweise geliefert
    - Teilweise fakturiert
    - Storniert

Die Einstellung für **Verfügt nur über extern verwaltete Produkte** wird in anderen Auftragsszenarien (Synchronisierung von Sales mit Finance and Operation) verwendet, um permanent darüber auf dem Laufenden zu sein, ob der Auftrag vollständig aus **Extern verwalteten Produkten** besteht. In diesem Fall werden Produkte in Finance and Operations verwaltet. Dadurch wird sichergestellt, dass Sie nicht versuchen, Auftragspositionen mit Produkten zu synchronisieren, die in Finance and Operations unbekannt sind.
 
Die Schaltflächen **Rechnung erstellen**, **Auftrag stornieren**, **Neu berechnen** und die für **Produkte abrufen** und **Adresse suchen** auf der Seite **Auftrag** sind bei extern verwalteten Aufträgen ausgeblendet, da Rechnungen in Finance and Operations erstellt und mit Sales synchronisiert werden. Die Seite "Auftrag" kann nicht geändert werden, da Auftragsinformationen über Finance and Operations synchronisiert werden.
 
Der **Auftragsstatus** bleibt aktiv, um sicherstellen, dass Änderungen aus Finance and Operations in Sales in den **Auftrag** einfließen. Dies wird gesteuert, indem Sie den standardmäßigen **Statecode [Status]** im Datenintegrationsprojekt auf **Aktiv** setzen.

## <a name="preconditions-and-mapping-setup"></a>Voraussetzungen und Einrichtung der Zuordnung 

Vor dem Synchronisieren von Aufträgen müssen die Systeme mit den folgenden Einstellungen synchronisiert werden:

### <a name="setup-in-sales"></a>Einrichtung in Sales

- Stellen Sie sicher, dass Berechtigungen für das Team, zu dem der Benutzer (aus Ihren **Verbindungseinstellungen** in Sales) zugewiesen ist, vorhanden sind. Werden Demodaten verwendet, hat in der Regel der Benutzer einen Administratorzugriff aber nicht das Team. Ohne erhalten Sie eine Fehlermeldung, die besagt, dass das Prinzipal-Team fehlt, wenn Sie das Projekt über den Datenintegrator ausführen. 

    - Wählen Sie unter **Einstellungen** > **Sicherheit** > **Teams** das relevante Team aus, klicken Sie auf die Option für **Rollen verwalten**, und wählen Sie eine Rolle mit den benötigten Berechtigungen aus, beispielsweise Systemadministrator.

- Stellen Sie unter **Einstellungen** > **Verwaltung** > **Systemeinstellungen** > **Verkäufe** sicher, dass das **Systempreisberechnungssystem** auf **Ja** festgelegt ist. 

- Stellen Sie unter **Einstellungen** > **Verwaltung** > **Systemeinstellungen** > **Verkäufe** sicher, dass **Rabattberechnungsmethode** auf **Positionsartikel** festgelegt ist. 

### <a name="setup-in-finance-and-operations"></a>Einrichtung in Finance and Operations

Legen Sie **Vertrieb und Marketing** > **Periodische Aufgaben** > **Verkaufssummen berechnen** für eine Ausführung als Stapelverarbeitungsauftrag fest und setzen Sie **Summen für Aufträge berechnen** auf **Ja**. Dies ist wichtig, da nur Aufträge mit berechneten Gesamtumsätzen mit CDS und Sales synchronisiert werden. Die Häufigkeit des Stapelverarbeitungsauftrags sollte sich an der Häufigkeit der Auftragssynchronisierung orientieren.

### <a name="setup-in-the-data-integration-project"></a>Einrichtung im Datenenintegrationsprojekt

#### <a name="salesheader-task"></a>SalesHeader-Aufgabe

- Aktualisieren Sie die Zuordnung für **CDS-Organisations-ID in Quelle** > **CDS**.

    - Der Standardvorlagenwert für **Account_Organization_OrganizationId** ist ORG001.
    - Der Standardvorlagenwert für **InvoiceAccount_Organization_OrganizationId** ist ORG001.
    - Der Standardvorlagenwert für **Organization_OrganizationId** ist ORG001.

- Vergewissern Sie sich, dass die erforderliche Zuordnung in **Quelle** > **CDS für InvoiceCountryRegionId zu BillingAddress_Country** und für **DeliveryCountryRegionId zu DeliveryAddress_Country** vorhanden ist.

    - Der Vorlagenwert ist **ValueMap** mit einer Reihe zugeordneter Länder.

- **Preisliste** ist erforderlich, um Aufträge in Sales zu erstellen. Aktualisieren Sie die **ValueMap** in **CDS** > **Ziel** für **pricelevelid.name [Preislistenname]** auf die **Preisliste**, die in Sales pro Währung verwendet wird. Sie können entweder die standardmäßige **Preisliste** bei einer einheitlichen Währung verwenden oder **ValueMap** nutzen, wenn Sie **Preislisten** in mehreren Währungen haben.
    
    - Der Standardvorlagewert für **pricelevelid.name [Preislistenname]** ist CRM-Service USA (Beispiel). 

#### <a name="salesline-task"></a>SalesLine-Aufgabe

- Aktualisieren Sie die Zuordnung für **CDS-Organisations-ID in Quelle** > **CDS**. 
    
    - Der Standardvorlagenwert für **SalesOrder_Organization_OrganizationId** ist ORG001.
    - Der Standardvorlagenwert für **Product_Organization_OrganizationId** ist ORG001.

- Vergewissern Sie sich, dass die erforderliche Zuordnung in **Quelle** > **CDS** für **DeliveryCountryRegionId** zu **DeliveryAddress_Country** vorhanden ist.

    - Der Vorlagenwert ist **ValueMap** mit einer Reihe zugeordneter Länder.
    
- Stellen Sie sicher, dass die erforderliche **ValueMap** für **SalesUnitSymbol** in Finance and Operations unter **Quelle** > **CDS-Zuordnung** vorhanden ist.

    - Der Vorlagenwert für **ValueMap** ist für **SalesUnitSymbol zu Quantity_UOM** definiert.

## <a name="template-mapping-in-data-integrator"></a>Vorlagenzuordnung im Datenintegrator

> [!NOTE]
> Die Felder **Zahlungsbedingungen**, **Frachtkonditionen**, **Lieferbedingungen**, **Liefermethode** und **Liefermodus** sind nicht Teil der Standardzuordnungen. Um diese Feldern zuzuordnen, müssen Sie eine Wertzuordnung einrichten, die spezifisch für die Daten in den Organisationen ist, zwischen denen die Entität synchronisiert wird.

Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenzuordnung im Datenintegrator.

### <a name="orderheader"></a>OrderHeader

![Vorlagenzuordnung im Datenintegrator](./media/sales-order-template-mapping-data-integrator-1.png)

![Vorlagenzuordnung im Datenintegrator](./media/sales-order-template-mapping-data-integrator-2.png)

### <a name="orderline"></a>OrderLine

![Vorlagenzuordnung im Datenintegrator](./media/sales-order-template-mapping-data-integrator-3.png)

![Vorlagenzuordnung im Datenintegrator](./media/sales-order-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a>Verwandte Themen

[Synchronisierung von Produkten aus Finance and Operations für Produkte in Sales](products-template-mapping.md)

[Konten von Sales mit Debitoren in Finance and Operations synchronisieren](accounts-template-mapping.md)

[Kontakte von Sales mit Kontakten oder Debitoren in Finance and Operations synchronisieren](contacts-template-mapping.md)

[Verkaufsangebotskopfzeilen und -positionen von Sales mit Finance and Operations synchronisieren](sales-quotation-template-mapping.md)

[Verkaufsrechnungszeilen und -positionen von Finance and Operations mit Sales synchronisieren](sales-invoice-template-mapping.md)


