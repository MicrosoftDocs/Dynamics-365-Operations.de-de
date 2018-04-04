---
title: Verkaufsrechnungskopfzeilen und -positionen direkt von Finance and Operations mit Sales synchronisieren
description: "Dieses Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Verkaufsrechnungskopfzeilen und -positionen direkt von Microsoft Dynamics 365 for Finance and Operations mit Microsoft Dynamics 365 for Sales zu synchronisieren."
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
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: afbf4a24b737cf7221bac4b688b8801b1bcd839c
ms.contentlocale: de-de
ms.lasthandoff: 03/26/2018

---

# <a name="synchronize-sales-invoice-headers-and-lines-directly-from-finance-and-operations-to-sales"></a>Verkaufsrechnungskopfzeilen und -positionen direkt von Finance and Operations mit Sales synchronisieren

[!include[banner](../includes/banner.md)]

Dieses Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Verkaufsrechnungskopfzeilen und -positionen direkt von Microsoft Dynamics 365 for Finance and Operations mit Microsoft Dynamics 365 for Sales zu synchronisieren.

## <a name="data-flow-in-prospect-to-cash"></a>Datenfluss in Interessent nach Bargeld

Die Lösung Interessent nach Bargeld verwendet die Datenenintegrationsfunktion, um Daten über Instanzen von Finance and Operations und Sales hinweg zu synchronisieren. Die „Interessent zu Bargeld”-Vorlagen, die über die Datenintegrationsfunktion verfügbar sind, ermöglichen den Fluss von Konten, Kontakten, Produkten, Verkaufsangeboten, Aufträgen und Verkaufsrechnungen zwischen Finance and Operations und Sales. Die folgende Abbildung zeigt, wie Daten zwischen Finance and Operations und Sales synchronisiert werden.

[![Datenfluss in Interessent nach Bargeld](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Vorlagen und Aufgaben

Um auf die verfügbaren Vorlagen zuzugreifen, öffnen Sie [PowerApps-Administrator-Center](https://preview.admin.powerapps.com/dataintegration). Wählen Sie **Projekte**, und dann auf, in der oberen rechten Ecke, wählen Sie **Neues Projekt**, um öffentliche Vorlagen auszuwählen.

Die folgenden Vorlagen und zugrunde liegenden Aufgaben werden verwendet, um Rechnungskopfzeilen und -positionen von Finance and Operations mit Sales zu synchronisieren:

- **Name der Vorlage in der Datenintegration:** Verkaufsrechnungen (Finance and Operations zu Sales) - direkt
- **Namen der Aufgaben im Datenintegrationsprojekt:**

    - SalesInvoiceHeader
    - SalesInvoiceLine

Die folgenden Synchronisierungsaufgaben sind erforderlich, bevor die Synchronisierung von Rechnungskopfzeilen und -positionen erfolgen kann:

- Produkte (Finance and Operations nach Sales) - Direkt
- Konten (Sales nach Finance and Operations) - Direkt (wenn verwendet)
- Kontakte (Sales nach Finance and Operations) - Direkt (wenn verwendet)
- Auftragskopf und -positionen (Finance and Operations nach Sales) - Direkt

## <a name="entity-set"></a>Entitätssatz

| Finance and Operations                               | Vertrieb          |
|------------------------------------------------------|----------------|
| Extern gepflegte Debitorenverkaufsrechnungs-Kopfzeilen | Rechnungen       |
| Extern gepflegte Debitorenverkaufsrechnungs-Positionen   | InvoiceDetails |

## <a name="entity-flow"></a>Entitätsfluss

Verkaufsrechnungen werden in Finance and Operations erstellt und mit Sales synchronisiert.

> [!NOTE]
> Die Steuer für Belastungen auf dem Verkaufsrechnungskopf ist derzeit nicht in der Synchronisierung von Finance and Operations mit Sales enthalten. Sales unterstützt keine Steuerinformationen auf Kopfebene. Allerdings sind Steuern, die den Belastungen auf Positionsebene zugeordnet sind, in die Synchronisierung einbezogen.

## <a name="prospect-to-cash-solution-for-sales"></a>Prospect to Cash-Lösung für Sales

- Ein Feld **Rechnungsnummer** wurde zur Entität **Rechnung** hinzugefügt und wird auf der Seite angezeigt.
- Die Schaltfläche **Rechnung erstellen** auf der Seite **Auftrag** ist ausgeblendet, da Rechnungen in Finance and Operations erstellt und mit Sales synchronisiert werden. Die Seite **Rechnung** kann nicht geändert werden, da Rechnungen über Finance and Operations synchronisiert werden.
- Der **Auftragsstatus**-Wert wird automatisch in **Fakturiert** geändert, wenn die zugehörige Rechnung aus Finance and Operations mit Sales synchronisiert wurde. Darüber hinaus wird der Eigentümer des Auftrags, aufgrund dessen die Rechnung erstellt wurde, als Eigentümer der Rechnung zugewiesen. Daher kann der Besitzer des Auftrags die Rechnung anzeigen.

## <a name="preconditions-and-mapping-setup"></a>Voraussetzungen und Einrichtung der Zuordnung

Vor dem Synchronisieren von Rechnungen müssen die Systeme mit den folgenden Einstellungen synchronisiert werden:

### <a name="setup-in-sales"></a>Einrichtung in Sales

Gehen Sie zu **Einstellungen** > **Verwaltung** > **Systemeinstellungen** > **Sales**, und überprüfen Sie, ob die folgenden Einstellungen verwendet werden:

- Die Option **Systempreisberechnungssystem verwenden** wird auf **Ja** festgelegt.
- Das Feld **Rabattberechnungsmethode** wird auf **Positionsartikel** festgelegt.

### <a name="setup-in-the-data-integration-project"></a>Einrichtung im Datenenintegrationsprojekt

#### <a name="salesinvoiceheader-task"></a>SalesInvoiceHeader-Aufgabe

- Vergewissern Sie sich, dass die erforderliche Zuordnung für **InvoiceCountryRegionId** zu **BillingAddress\_Country** vorhanden ist.

    Der Vorlagenwert ist eine Wertzuordnung, in der verschiedene Länder/Regionen zugeordnet sind.

- Preisliste ist erforderlich, um Rechnungen in Sales zu erstellen. Aktualisieren Sie die Wertzuordnung für **pricelevelid.name \[Price list name\]** auf die Preisliste, die in Sales pro Währung verwendet wird. Sie können die Standardpreisliste für eine einzelne Währung verwenden. Alternativ können Sie, wenn Sie Preislisten in mehreren Währungen haben, eine Zuordnung verwenden.

    Der Vorlagenwert für **pricelevelid.name \[Price list name\]** ist ein Wertzuordnung, die auf Währung mit USD = CRM Service USA (Beispiel) basiert.  
    
#### <a name="salesinvoiceline-task"></a>SalesInvoiceLine-Aufgabe

- Vergewissern Sie sich, dass die erforderliche Zuordnung für **Maßeinheit** vorhanden ist.
- tellen Sie sicher, dass die erforderliche Wertzuordnung für **SalesUnitSymbol** in Finance and Operations vorhanden ist.

    Ein Vorlagenwert, der eine Wertzuordnung hat, wird für **SalesUnitSymbol** als **Quantity\_UOM** definiert.

## <a name="template-mapping-in-data-integration"></a>Vorlagenzuordnung in Datenintegration

> [!NOTE]
> Die Felder **Zahlungsbedingungen**, **Frachtbedingungen**, **Lieferbedingungen**, **Liefermethode** und **Bereitstellungsmodus** sind nicht in den Standardzuordnungen enthalten. Um diese Feldern zuzuordnen, müssen Sie eine Wertzuordnung einrichten, die spezifisch für die Daten in den Organisationen ist, zwischen denen die Entität synchronisiert wird.

Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenzuordnung in Datenintegration. 

> [!NOTE]
> Die Zuordnung zeigt, welche Feldinformationen von Sales zu Finance and Operations synchronisiert werden.

### <a name="salesinvoiceheader"></a>SalesInvoiceHeader

![Vorlagenzuordnung in Datenintegration](./media/sales-invoice-direct-template-mapping-data-integrator-1.png)

### <a name="salesinvoiceline"></a>SalesInvoiceLine

![Vorlagenzuordnung in Datenintegration](./media/sales-invoice-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a>Verwandte Themen

[Interessent zu Bargeld](prospect-to-cash.md)

[Konten von Sales direkt mit Debitoren in Finance and Operations synchronisieren](accounts-template-mapping-direct.md)

[Produkte direkt von Finance and Operations mit Produkten in Sales synchronisieren](products-template-mapping-direct.md)

[Kontakte direkt von Sales mit Kontakten oder Debitoren in Finance and Operations synchronisieren](contacts-template-mapping-direct.md)

[Auftragskopfzeilen und -positionen direkt von Finance and Operations mit Sales synchronisieren](sales-order-template-mapping-direct-two-ways.md)







