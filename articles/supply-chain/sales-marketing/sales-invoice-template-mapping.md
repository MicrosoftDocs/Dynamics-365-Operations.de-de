---
title: Verkaufsrechnungszeilen und -positionen von Finance and Operations mit Sales synchronisieren
description: "Das Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Verkaufsangebotskopfzeilen und -positionen von Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, mit Microsoft Dynamics 365 for Sales zu synchronisieren."
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: fb5ba099911deda5308daf92d82cd6b3489995bf
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-sales-invoice-headers-and-lines-from-finance-and-operations-to-sales"></a>Verkaufsrechnungszeilen und -positionen von Finance and Operations mit Sales synchronisieren

[!include[banner](../includes/banner.md)]

Das Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Verkaufsangebotskopfzeilen und -positionen von Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, mit Microsoft Dynamics 365 for Sales zu synchronisieren. 

## <a name="templates-and-tasks"></a>Vorlagen und Aufgaben

Die folgenden Vorlagen und zugrunde liegenden Aufgaben werden verwendet, um Rechnungskopfzeilen und -positionen von Finance and Operations mit Sales zu synchronisieren:

- **Name der Vorlage in der Datenintegration** 

     - Verkaufsrechnungen (Finance and Operations nach Sales)

- **Namen der Aufgaben im Datenintegrationsprojekt**

    - SalesInvoiceHeader
    - SalesInvoiceLine

Synchronisiert die Aufgaben, die vor der Verkaufsrechnungskopf- und -Positionssynchronisierung erforderlich sind:
-   Produkte (Finance and Operations nach Sales)
-   Konten (Sales nach Finance and Operations) (wenn verwendet)
-   Kontakte (Sales nach Finance and Operations) (wenn verwendet)
-   Auftragskopf und -positionen (Finance and Operations nach Sales)

## <a name="entity-set"></a>Entitätssatz

| Finance and Operations                               | Common Data Service (CDS)              | Vertrieb          |
|------------------------------------------------------|------------------|----------------|
| Extern gepflegte Debitorenverkaufsrechnungs-Kopfzeilen | SalesInvoice     | Rechnungen       |
| Extern gepflegte Debitorenverkaufsrechnungs-Positionen   | SalesInvoiceLine | InvoiceDetails |

## <a name="entity-flow"></a>Entitätsfluss

Verkaufsrechnungen werden in Finance and Operations erstellt und mit Sales synchronisiert.

> [!NOTE]
> Die Steuer für Belastungen auf dem **Verkaufsrechnungskopf** ist derzeit nicht in der Synchronisierung von Finance and Operations mit Sales enthalten. Der Grund dafür ist, dass Sales keine Steuerinformationen auf Kopfebene unterstützt. Die Steuer, die sich auf Belastungen auf Positionsebene bezieht, ist enthalten.

## <a name="prospect-to-cash-solution-for-sales"></a>Prospect to Cash-Lösung für Sales

-  Ein **Rechnungsnummernfeld** wird zur Entität **Rechnung** hinzugefügt und auf der Seite angezeigt.
 
-  Die Schaltfläche **Rechnung erstellen** auf der Seite **Auftrag** ist ausgeblendet, da Rechnungen in Finance and Operations erstellt und mit Sales synchronisiert werden. Die Seite **Rechnung** kann nicht geändert werden, da Rechnungen über Finance and Operations synchronisiert werden.
 
-  Der **Auftragsstatus** wird automatisch in **Fakturiert** geändert, wenn die zugehörige Rechnung aus Finance and Operations mit Sales synchronisiert wurde. Darüber hinaus wird der Eigentümer des Auftrags, aufgrund dessen die Rechnung erstellt wurde, als Eigentümer der Rechnung zugewiesen. Dadurch kann der Eigentümer des Auftrags die Rechnung anzeigen.
 
## <a name="preconditions-and-mapping-setup"></a>Voraussetzungen und Einrichtung der Zuordnung

Vor dem Synchronisieren von Verkaufsrechnungen müssen die Systeme mit den folgenden Einstellungen synchronisiert werden:

### <a name="setup-in-sales"></a>Einrichtung in Sales

- Stellen Sie unter **Einstellungen** > **Verwaltung** > **Systemeinstellungen** > **Verkäufe** sicher, dass das **Systempreisberechnungssystem** auf **Ja** festgelegt ist. 

- Stellen Sie unter **Einstellungen** > **Verwaltung** > **Systemeinstellungen** > **Verkäufe** sicher, dass **Rabattberechnungsmethode** auf **Positionsartikel** festgelegt ist. 

### <a name="setup-in-the-data-integration-project"></a>Einrichtung im Datenenintegrationsprojekt

#### <a name="salesinvoiceheader-task"></a>SalesInvoiceHeader-Aufgabe

- Aktualisieren Sie die Zuordnung für **CDS-Organisations-ID** in **Quelle** > **CDS**. 

    -  Der Standardvorlagenwert für **SalesOrder_Organization_OrganizationId** ist ORG001.
    -  Der Standardvorlagenwert für **Account_Organization_OrganizationId** ist ORG001.
    -  Der Standardvorlagenwert für **Organization_OrganizationId** ist ORG001.

- Vergewissern Sie sich, dass die erforderliche Zuordnung in **Quelle** > **CDS für InvoiceCountryRegionId** in **BillingAddress_Country** vorhanden ist.

    -  Der Vorlagenwert ist **ValueMap** mit einer Reihe zugeordneter Länder.

- **Preisliste** ist erforderlich, um Rechnungen in Sales zu erstellen. Aktualisieren Sie die **ValueMap** in **CDS** > **Ziel für pricelevelid.name [Preislistenname]** auf die **Preisliste**, die in Sales pro Währung verwendet wird. Sie können entweder die standardmäßige **Preisliste** bei einer einheitlichen Währung verwenden oder **ValueMap** nutzen, wenn Sie **Preislisten** in mehreren Währungen haben.

    -  Der Vorlagenwert für **pricelevelid.name [Preislistenanme]** ist **ValueMap** basierend auf **Währung**.
    -  usd: CRM-Service USA (Beispiel). 

#### <a name="salesinvoiceline-task"></a>SalesInvoiceLine-Aufgabe

- Vergewissern Sie sich, dass die erforderliche Zuordnung in **Quelle** > **CDS für Maßeinheit** vorhanden ist.

- Stellen Sie sicher, dass die erforderliche **ValueMap** für **SalesUnitSymbol** in Finance and Operations unter **Quelle** > **CDS-Zuordnung** vorhanden ist. 
    
    - Der Vorlagenwert für **ValueMap** ist für **SalesUnitSymbol zu Quantity_UOM** definiert.
    
-  Aktualisieren Sie die Zuordnung für **CDS-Organisations-ID in Quelle** > **CDS**. 

    -  Der Standardvorlagenwert für **SalesInvoicer_Organization_OrganizationId** ist ORG001.
    -  Der Standardvorlagenwert für **Product_Organization_OrganizationId** ist ORG001.
 
## <a name="template-mapping-in-data-integrator"></a>Vorlagenzuordnung im Datenintegrator

> [!NOTE]
> Die Felder **Zahlungsbedingungen**, **Frachtkonditionen**, **Lieferbedingungen**, **Liefermethode** und **Liefermodus** sind nicht Teil der Standardzuordnungen. Um diese Feldern zuzuordnen, müssen Sie eine Wertzuordnung einrichten, die spezifisch für die Daten in den Organisationen ist, zwischen denen die Entität synchronisiert wird.

Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenzuordnung im Datenintegrator.

![Vorlagenzuordnung im Datenintegrator](./media/sales-invoice-template-mapping-data-integrator-1.png)

![Vorlagenzuordnung im Datenintegrator](./media/sales-invoice-template-mapping-data-integrator-2.png)

![Vorlagenzuordnung im Datenintegrator](./media/sales-invoice-template-mapping-data-integrator-3.png)

![Vorlagenzuordnung im Datenintegrator](./media/sales-invoice-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a>Verwandte Themen

[Synchronisierung von Produkten aus Finance and Operations für Produkte in Sales](products-template-mapping.md)

[Konten von Sales mit Debitoren in Finance and Operations synchronisieren](accounts-template-mapping.md)

[Kontakte von Sales mit Kontakten oder Debitoren in Finance and Operations synchronisieren](contacts-template-mapping.md)

[Verkaufsangebotskopfzeilen und -positionen von Sales mit Finance and Operations synchronisieren](sales-quotation-template-mapping.md)

[Auftragskopfzeilen und -positionen von Finance and Operations mit Sales synchronisieren](sales-order-template-mapping.md)


