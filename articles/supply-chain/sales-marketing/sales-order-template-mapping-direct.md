---
title: Auftragskopfzeilen und -positionen direkt von Finance and Operations mit Sales synchronisieren
description: "Das Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Auftragskopfzeilen und -positionen von Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, mit Microsoft Dynamics 365 for Sales zu synchronisieren."
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2017
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
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: cc0be50552ae680ba5291e72b7c482ee67e1e70e
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-order-headers-and-lines-directly-from-finance-and-operations-to-sales"></a>Auftragskopfzeilen und -positionen direkt von Finance and Operations mit Sales synchronisieren

[!include[banner](../includes/banner.md)]

Das Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Auftragskopfzeilen und -positionen von Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, mit Microsoft Dynamics 365 for Sales zu synchronisieren.

## <a name="data-flow-in-prospect-to-cash"></a>Datenfluss in Interessent nach Bargeld

Die Lösung Interessent nach Bargeld verwendet die Datenenintegrationsfunktion, um Daten über Instanzen von Finance and Operations und Sales hinweg zu synchronisieren. Die „Interessent zu Bargeld”-Vorlagen, die über die Datenintegrationsfunktion verfügbar sind, ermöglichen den Fluss von Konten, Kontakten, Produkten, Verkaufsangeboten, Aufträgen und Verkaufsrechnungen zwischen Finance and Operations und Sales. Die folgende Abbildung zeigt, wie Daten zwischen Finance and Operations und Sales synchronisiert werden.

[![Datenfluss in Interessent nach Bargeld](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Vorlagen und Aufgaben

Um auf die verfügbaren Vorlagen zuzugreifen, öffnen Sie [PowerApps-Administrator-Center](https://preview.admin.powerapps.com/dataintegration). Wählen Sie **Projekte**, und dann auf, in der oberen rechten Ecke, wählen Sie **Neues Projekt**, um öffentliche Vorlagen auszuwählen.

Die folgende Vorlage und zugrunde liegenden Aufgaben werden verwendet, um Auftragskopfzeilen und -positionen von Finance and Operations mit Sales zu synchronisieren:

- **Name der Vorlage in der Datenintegration:** Verkaufsaufträge (Finance and Operations zu Sales) - direkt
- **Namen der Aufgaben im Datenintegrationsprojekt:**

    - OrderHeader
    - OrderLine

Die folgenden Synchronisierungsaufgaben sind erforderlich, bevor die Synchronisierung von Rechnungskopfzeilen und -positionen erfolgen kann:

- Produkte (Finance and Operations nach Sales) - Direkt
- Konten (Sales nach Finance and Operations) - Direkt (wenn verwendet)
- Kontakte nach Debitoren (Sales nach Finance and Operations) - Direkt (wenn verwendet)

## <a name="entity-set"></a>Entitätssatz

| Finance and Operations  | Vertrieb             |
|-------------------------|-------------------|
| CDS-Auftragskopfzeilen | SalesOrders       |
| CDS-Auftragspositionen   | SalesOrderDetails |

## <a name="entity-flow"></a>Entitätsfluss

Aufträge werden in Finance and Operations erstellt und mit Sales synchronisiert.

Filter in der Vorlage helfen, sicherzustellen, dass nur relevante Aufträge in die Synchronisierung einfließen:

- Sowohl der Bestellungskunde als auch der Rechnungsdebitor auf dem Auftrag, der aus Sales stammt, werden in die Synchronisierung einbezogen. In Finance and Operations werden die Felder **OrderingCustomerIsExternallyMaintained** und **InvoiceCustomerIsExternallyMaintained** verwendet, um die Synchronisierung in den Datenentitäten zu verfolgen.
- Der Auftrag in Finance and Operations muss bestätigt werden. Nur bestätigte Aufträge oder Aufträge mit fortgeschrittenem Verarbeitungsstatus (beispielsweise **Versendet** oder **Fakturiert**) werden mit Sales synchronisiert.
- Nach dem Erstellen oder Ändern eines Auftrags, muss der Stapelverarbeitungsauftrag **Verkaufssummen berechnen** aus Finance and Operations ausgeführt werden. Nur Aufträge, bei denen Auftragssummen berechnet wurden, werden mit Sales synchronisiert.

> [!NOTE]
> Die Steuer für Belastungen auf dem Verkaufsauftragskopf ist derzeit nicht in der Synchronisierung von Finance and Operations mit Sales enthalten. Sales unterstützt keine Steuerinformationen auf Kopfebene. Allerdings sind Steuern, die den Belastungen auf Positionsebene zugeordnet sind, in die Synchronisierung einbezogen.

## <a name="prospect-to-cash-solution-for-sales"></a>Prospect to Cash-Lösung für Sales

Neue Felder wurden der Entität **Auftrag** hinzugefügt und auf der Seite angezeigt:

- **Wird extern verwaltet** – Auf **Ja** setzen, wenn der Auftrag aus Finance and Operations stammt.
- **Verarbeitungsstatus** – Wird verwendet, um den Verarbeitungsstatus des Auftrags in Finance and Operations anzuzeigen. Folgende Werte sind verfügbar:

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

Die Einstellung für **Verfügt nur über extern verwaltete Produkte** wird in anderen Auftragsszenarien (z. B. Synchronisierung von Sales mit Finance and Operation) verwendet, um permanent darüber auf dem Laufenden zu sein, ob der Auftrag vollständig aus extern verwalteten Produkten besteht. Wenn ein Verkaufsauftrag nur aus extern verwalteten Produkten besteht, werden die Produkte in Finance and Operations verwaltet. Mit diesem Verhalten wird sichergestellt, dass Sie nicht versuchen, Verkaufsangebotspositionen mit Produkten zu synchronisieren, die in Finance and Operations unbekannt sind.

Bei extern verwalteten Aufträgen, werden die Schaltflächen **Rechnung erstellen**, **Auftrag stornieren**, **Neu berechnen** und die für **Produkte abrufen** und **Adresse suchen** auf der Seite **Auftrag** ausgeblendet, da Rechnungen in Finance and Operations erstellt und mit Sales synchronisiert werden. Die Seite "Auftrag" kann nicht geändert werden, da Auftragsinformationen über Finance and Operations synchronisiert werden.

Der Auftragsstatus bleibt **Aktiv**, um sicherstellen, dass Änderungen aus Finance and Operations in Sales in den Auftrag einfließen. Dies wird gesteuert, indem Sie den standardmäßigen **Statecode \[Status\]** Wert auf **Aktiv** setzen.

## <a name="preconditions-and-mapping-setup"></a>Voraussetzungen und Einrichtung der Zuordnung

Vor dem Synchronisieren von Aufträgen müssen die Systeme mit den folgenden Einstellungen synchronisiert werden:

### <a name="setup-in-sales"></a>Einrichtung in Sales

- Stellen Sie sicher, dass Berechtigungen für das Team, zu dem der Benutzer (aus Ihren Verbindungseinstellungen in Sales) zugewiesen ist, vorhanden sind. Werden Demodaten verwendet, hat in der Regel der Benutzer einen Administratorzugriff aber nicht das Team. Wenn dieses Team nicht auch Administratorzugriff hat, wenn Sie das Projekt vom Datenintegrator ausführen, erhalten Sie eine Fehlermeldung, die angibt, dass das Hauptteam fehlt.

    Wählen Sie unter **Settings** > **Security** > **Teams** das relevante Team aus, klicken Sie auf die Option für **Rollen verwalten**, und wählen Sie eine Rolle mit den benötigten Berechtigungen aus, beispielsweise **Systemadministrator**.

- Gehen Sie zu **Einstellungen** > **Verwaltung** > **Systemeinstellungen** > **Sales**, und überprüfen Sie, ob die folgenden Einstellungen verwendet werden:

    - Die Option **Systempreisberechnungssystem verwenden** wird auf **Ja** festgelegt.
    - Das Feld **Rabattberechnungsmethode** wird auf **Positionsartikel** festgelegt.

### <a name="setup-in-finance-and-operations"></a>Einrichtung in Finance and Operations

Gehen Sie zu **Vertrieb und Marketing** > **Periodische Aufgaben** > **Vertriebssummen berechnen**, und richten Sie den Einzelvorgang so ein, dass er als Stapelverarbeitungslauf ausgeführt wird. Legen sie Option **Berechnen Sie Summen für Aufträge** auf **Ja** fest. Diese Einstellung ist wichtig, da nur Aufträge, bei denen Auftragssummen berechnet wurden, werden mit Sales synchronisiert. Die Häufigkeit des Stapelverarbeitungsauftrags sollte sich an der Häufigkeit der Auftragssynchronisierung orientieren.

### <a name="setup-in-the-data-integration-project"></a>Einrichtung im Datenenintegrationsprojekt

#### <a name="salesheader-task"></a>SalesHeader-Aufgabe

- Vergewissern Sie sich, dass die erforderliche Zuordnung für **InvoiceCountryRegionId** zu **BillingAddress\_Country** und für **DeliveryCountryRegionId** zu **DeliveryAddress\_Country** vorhanden ist.

    Der Vorlagenwert ist eine Wertzuordnung, in der verschiedene Länder/Regionen zugeordnet sind.

- Preisliste ist erforderlich, um Aufträge in Sales zu erstellen. Aktualisieren Sie die Wertzuordnung für **pricelevelid.name \[Price list name\]** auf die Preisliste, die in Sales pro Währung verwendet wird. Sie können die Standardpreisliste für eine einzelne Währung verwenden. Alternativ können Sie, wenn Sie Preislisten in mehreren Währungen haben, eine Zuordnung verwenden.

    Der Standardvorlagewert für **pricelevelid.name \[Price list name\]** ist **CRM Service USA (Beispiel)**.

#### <a name="salesline-task"></a>SalesLine-Aufgabe

- Vergewissern Sie sich, dass die erforderliche Zuordnung für **DeliveryCountryRegionId** zu **DeliveryAddress\_Country** vorhanden ist.

    Der Vorlagenwert ist eine Wertzuordnung, in der verschiedene Länder/Regionen zugeordnet sind.

- tellen Sie sicher, dass die erforderliche Wertzuordnung für **SalesUnitSymbol** in Finance and Operations vorhanden ist.

    Ein Vorlagenwert, der eine Wertzuordnung hat, wird für **SalesUnitSymbol** als **Quantity\_UOM** definiert.

## <a name="template-mapping-in-data-integration"></a>Vorlagenzuordnung in Datenintegration

> [!NOTE]
> Die Felder **Zahlungsbedingungen**, **Frachtbedingungen**, **Lieferbedingungen**, **Liefermethode** und **Bereitstellungsmodus** sind nicht in den Standardzuordnungen enthalten. Um diese Feldern zuzuordnen, müssen Sie eine Wertzuordnung einrichten, die spezifisch für die Daten in den Organisationen ist, zwischen denen die Entität synchronisiert wird.

Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenzuordnung in Datenintegration. 

> [!NOTE]
> Die Zuordnung zeigt, welche Feldinformationen von Sales zu Finance and Operations synchronisiert werden.

### <a name="orderheader"></a>OrderHeader

![Vorlagenzuordnung im Datenintegrator](./media/sales-order-direct-template-mapping-data-integrator-1.png)

### <a name="orderline"></a>OrderLine

![Vorlagenzuordnung im Datenintegrator](./media/sales-order-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a>Verwandte Themen

[Interessent zu Bargeld](prospect-to-cash.md)

[Konten von Sales direkt mit Debitoren in Finance and Operations synchronisieren](accounts-template-mapping-direct.md)

[Produkte direkt von Finance and Operations mit Produkten in Sales synchronisieren](products-template-mapping-direct.md)

[Kontakte direkt von Sales mit Kontakten oder Debitoren in Finance and Operations synchronisieren](contacts-template-mapping-direct.md)

[Verkaufsrechnungskopfzeilen und -positionen direkt von Finance and Operations mit Sales synchronisieren](sales-invoice-template-mapping-direct.md)




