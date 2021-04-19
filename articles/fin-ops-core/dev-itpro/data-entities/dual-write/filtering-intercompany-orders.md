---
title: Intercompany-Aufträge filtern, um die Synchronisierung von Aufträgen und Auftragspositionen zu vermeiden
description: In diesem Thema wird erläutert, wie Sie Intercompany-Aufträge filtern, damit die Entitäten „Orders“ und „OrderLines“ nicht synchronisiert werden.
author: negudava
ms.date: 11/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: negudava
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 123427db61782490d348489c23e0eaf5f8b513c9
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748640"
---
# <a name="filter-intercompany-orders-to-avoid-syncing-orders-and-orderlines"></a><span data-ttu-id="28c1a-103">Intercompany-Aufträge filtern, um die Synchronisierung von Aufträgen und Auftragspositionen zu vermeiden</span><span class="sxs-lookup"><span data-stu-id="28c1a-103">Filter intercompany orders to avoid syncing Orders and OrderLines</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="28c1a-104">Sie können Intercompany-Aufträge filtern, sodass die Tabellen **Orders** und **OrderLines** nicht synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="28c1a-104">You can filter intercompany orders so that the **Orders** and **OrderLines** tables aren't synced.</span></span> <span data-ttu-id="28c1a-105">In einigen Szenarien sind die Intercompany-Auftragsdetails in der Kundenbindungs-App nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="28c1a-105">In some scenarios, the intercompany order details aren't required in a customer engagement app.</span></span>

<span data-ttu-id="28c1a-106">Jede der Dataverse-Standardentitäten wird mit Verweisen auf die Spalte **IntercompanyOrder** erweitert und die Zuordnungen für duales Schreiben werden geändert, sodass auf die zusätzlichen Spalten in den Filtern verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="28c1a-106">Each standard Dataverse table is extended through references to the **IntercompanyOrder** column, and the dual-write maps are modified so that they refer to the additional columns in the filters.</span></span> <span data-ttu-id="28c1a-107">Daher werden die Intercompany-Aufträge nicht mehr synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="28c1a-107">Therefore, the intercompany orders are no longer synced.</span></span> <span data-ttu-id="28c1a-108">Dieser Prozess vermeidet unnötige Daten in der Kundenbindungs-App.</span><span class="sxs-lookup"><span data-stu-id="28c1a-108">This process helps prevent unnecessary data in the customer engagement app.</span></span>

1. <span data-ttu-id="28c1a-109">Erweitern Sie die Tabelle **CDS-Auftragskopfzeilen** durch Hinzufügen eines Verweises auf die Spalte **IntercompanyOrder**.</span><span class="sxs-lookup"><span data-stu-id="28c1a-109">Extend the **CDS Sales Order Headers** table by adding a reference to the **IntercompanyOrder** column.</span></span> <span data-ttu-id="28c1a-110">Diese Spalte wird nur für Intercompany-Aufträge ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="28c1a-110">This column is filled in only on intercompany orders.</span></span> <span data-ttu-id="28c1a-111">Die Spalte **IntercompanyOrder** ist in der Tabelle **SalesTable** verfügbar.</span><span class="sxs-lookup"><span data-stu-id="28c1a-111">The **IntercompanyOrder** column is available in the **SalesTable** table.</span></span>

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="Staging der Zielseite für CDS-Auftragskopfzeilen zuordnen":::

2. <span data-ttu-id="28c1a-113">Nachdem **CDS-Auftragskopfzeilen** erweitert wurde, ist die Spalte **IntercompanyOrder** in der Zuordnung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="28c1a-113">After **CDS Sales Order Headers** is extended, the **IntercompanyOrder** column is available in the mapping.</span></span> <span data-ttu-id="28c1a-114">Wenden Sie einen Filter mit `INTERCOMPANYORDER == ""` als Abfragezeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="28c1a-114">Apply a filter that has `INTERCOMPANYORDER == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="Dialogfeld „Abfrage bearbeiten“ für CDS-Auftragskopfzeilen":::

3. <span data-ttu-id="28c1a-116">Erweitern Sie die Tabelle **CDS-Auftragspositionen** durch Hinzufügen eines Verweises auf die Spalte **IntercompanyInventTransId**.</span><span class="sxs-lookup"><span data-stu-id="28c1a-116">Extend the **CDS Sales Order Lines** table by adding a reference to the **IntercompanyInventTransId** column.</span></span> <span data-ttu-id="28c1a-117">Diese Spalte wird nur für Intercompany-Aufträge ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="28c1a-117">This column is filled in only on intercompany orders.</span></span> <span data-ttu-id="28c1a-118">Die Spalte **IntercompanyInventTransId** ist in der Tabelle **SalesLine** verfügbar.</span><span class="sxs-lookup"><span data-stu-id="28c1a-118">The **InterCompanyInventTransId** column is available in the **SalesLine** table.</span></span>

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="Staging der Zielseite für CDS-Auftragspositionen":::

4. <span data-ttu-id="28c1a-120">Nachdem **CDS-Auftragspositionen** erweitert wurde, ist die Spalte **IntercompanyInventTransId** in der Zuordnung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="28c1a-120">After **CDS Sales Order Lines** is extended, the **IntercompanyInventTransId** column is available in the mapping.</span></span> <span data-ttu-id="28c1a-121">Wenden Sie einen Filter mit `INTERCOMPANYINVENTTRANSID == ""` als Abfragezeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="28c1a-121">Apply a filter that has `INTERCOMPANYINVENTTRANSID == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="Dialogfeld „Abfrage bearbeiten“ für CDS-Auftragspositionen":::

5. <span data-ttu-id="28c1a-123">Wiederholen Sie die Schritte 1 und 2, um die Tabelle **Verkaufsrechnungskopfzeile V2** zu erweitern und eine Filterabfrage hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="28c1a-123">Repeat steps 1 and 2 to extend the **Sales Invoice Header V2** table and add a filter query.</span></span> <span data-ttu-id="28c1a-124">In diesem Fall verwenden Sie `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")` als Abfragezeichenfolge für den Filter.</span><span class="sxs-lookup"><span data-stu-id="28c1a-124">In this case, use `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")` as the query string for the filter.</span></span>

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="Staging der Zielseite für Verkaufsrechnungskopfzeile V2":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="Dialogfeld „Abfrage bearbeiten“ für Verkaufsrechnungskopfzeile V2":::

6. <span data-ttu-id="28c1a-127">Wiederholen Sie die Schritte 3 und 4, um die Tabelle **Verkaufsrechnungspositionen V2** zu erweitern und eine Filterabfrage hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="28c1a-127">Repeat steps 3 and 4 to extend the **Sales Invoice Lines V2** table and add a filter query.</span></span> <span data-ttu-id="28c1a-128">In diesem Fall verwenden Sie `INTERCOMPANYINVENTTRANSID == ""` als Abfragezeichenfolge für den Filter.</span><span class="sxs-lookup"><span data-stu-id="28c1a-128">In this case, use `INTERCOMPANYINVENTTRANSID == ""` as the query string for the filter.</span></span>

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="Dialogfeld „Abfrage bearbeiten“ für Verkaufsrechnungspositionen V2":::

7. <span data-ttu-id="28c1a-130">Die Tabelle **Angebote** hat keine Intercompany-Beziehung.</span><span class="sxs-lookup"><span data-stu-id="28c1a-130">The **Quotations** table doesn't have an intercompany relationship.</span></span> <span data-ttu-id="28c1a-131">Wenn jemand ein Angebot für einen Ihrer Intercompany-Kunden erstellt, können Sie alle diese Kunden über die Spalte **CustGroup** in eine Kundengruppe einordnen.</span><span class="sxs-lookup"><span data-stu-id="28c1a-131">If someone creates a quotation for one of your intercompany customers, you can use the **CustGroup** column to put all those customers into one customer group.</span></span> <span data-ttu-id="28c1a-132">Sie können die Kopfzeile und die Positionen erweitern, indem Sie die Spalte **CustGroup** hinzufügen, und filtern Sie dann so, dass die Gruppe nicht enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="28c1a-132">You can extend the header and lines by adding the **CustGroup** column, and then filter so that the group isn't included.</span></span>

    :::image type="content" source="media/filter-cust-group.png" alt-text="Staging der Zielseite für CDS-Verkaufsangebotskopf":::

8. <span data-ttu-id="28c1a-134">Nachdem Sie die **Angebote** erweitert haben, wenden Sie einen Filter mit `CUSTGROUP != "<company>"` als Abfragezeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="28c1a-134">After **Quotations** is extended, apply a filter that has `CUSTGROUP != "<company>"` as the query string.</span></span>

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="Dialogfeld „Abfrage bearbeiten“ für CDS-Verkaufsangebotskopf":::


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]