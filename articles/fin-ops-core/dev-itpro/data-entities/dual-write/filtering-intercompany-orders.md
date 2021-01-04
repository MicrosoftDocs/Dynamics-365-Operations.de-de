---
title: Intercompany-Aufträge filtern, um die Synchronisierung von Aufträgen und Auftragspositionen zu vermeiden
description: In diesem Thema wird beschrieben, wie Intercompany-Aufträge gefiltert werden, um die Synchronisierung von Aufträgen und Auftragspositionen zu vermeiden.
author: negudava
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: negudava
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 6c5e1e2467673badd20366d3bd8e1b93b8078b26
ms.sourcegitcommit: 0eb33909a419d526eb84b4e4b64d3595d01731ef
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "4701032"
---
# <a name="filter-intercompany-orders-to-avoid-synchronizing-orders-and-orderlines"></a><span data-ttu-id="59768-103">Intercompany-Aufträge filtern, um die Synchronisierung von Aufträgen und Auftragspositionen zu vermeiden</span><span class="sxs-lookup"><span data-stu-id="59768-103">Filter intercompany orders to avoid synchronizing Orders and OrderLines</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="59768-104">Sie können Intercompany-Aufträge filtern, um die Synchronisierung der Entitäten **Orders** und **OrderLines** zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="59768-104">You can filter intercompany orders to avoid synchronizing the **Orders** and **OrderLines** entities.</span></span> <span data-ttu-id="59768-105">In einigen Szenarien sind die Intercompany-Auftragsdetails in der Kundenbindungs-App nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="59768-105">In some scenarios, the intercompany order details are not necessary in customer engagement app.</span></span>

<span data-ttu-id="59768-106">Jede der Common Data Service-Standardentitäten wird mit Verweisen auf das Feld **IntercompanyOrder** erweitert und die Zuordnungen für duales Schreiben werden geändert, um auf die zusätzlichen Felder in den Filtern zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="59768-106">Each of the standard Common Data Service entities is extended with references to the **IntercompanyOrder** field, and the dual-write maps are modified to refer to the additional fields in the filters.</span></span> <span data-ttu-id="59768-107">Das Ergebnis ist, dass die Intercompany-Aufträge nicht mehr synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="59768-107">The result is that the intercompany orders are no longer synchronized.</span></span> <span data-ttu-id="59768-108">Dieser Prozess vermeidet unnötige Daten in der Kundenbindungs-App.</span><span class="sxs-lookup"><span data-stu-id="59768-108">This process avoids unnecessary data in the customer engagement app.</span></span>

1. <span data-ttu-id="59768-109">Fügen Sie einen Verweis auf **IntercompanyOrder** zu **CDS-Auftragskopfzeilen** hinzu.</span><span class="sxs-lookup"><span data-stu-id="59768-109">Add a reference to **IntercompanyOrder** to **CDS Sales Order Headers**.</span></span> <span data-ttu-id="59768-110">Eine Auffüllung erfolgt nur bei Intercompany-Aufträgen.</span><span class="sxs-lookup"><span data-stu-id="59768-110">It is populated on only intercompany orders.</span></span> <span data-ttu-id="59768-111">Das Feld **IntercompanyOrder** ist in **SalesTable** verfügbar.</span><span class="sxs-lookup"><span data-stu-id="59768-111">The field **IntercompanyOrder** is available in **SalesTable**.</span></span>

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="Staging dem Ziel zuordnen, SalesOrderHeader":::
    
2. <span data-ttu-id="59768-113">Nachdem **CDS-Auftragskopfzeilen** erweitert wurde, ist das Feld **IntercompanyOrder** im Mapping verfügbar.</span><span class="sxs-lookup"><span data-stu-id="59768-113">After **CDS Sales Order Headers** is extended, the **IntercompanyOrder** field is available in the mapping.</span></span> <span data-ttu-id="59768-114">Wenden Sie einen Filter mit `INTERCOMPANYORDER == ""` als Abfragezeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="59768-114">Apply a filter with `INTERCOMPANYORDER == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="Kundenauftragskopfzeilen, Abfrage bearbeiten":::

3. <span data-ttu-id="59768-116">Fügen Sie einen Verweis auf **IntercompanyInventTransId** zu **CDS-Auftragspositionen** hinzu.</span><span class="sxs-lookup"><span data-stu-id="59768-116">Add a reference to **IntercompanyInventTransId** to **CDS Sales Order Lines**.</span></span>  <span data-ttu-id="59768-117">Eine Auffüllung erfolgt nur bei Intercompany-Aufträgen.</span><span class="sxs-lookup"><span data-stu-id="59768-117">It is populated on only intercompany orders.</span></span> <span data-ttu-id="59768-118">Das Feld **InterCompanyInventTransID** ist in **SalesLine** verfügbar.</span><span class="sxs-lookup"><span data-stu-id="59768-118">The field **InterCompanyInventTransID** is available in **SalesLine**.</span></span>

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="Staging dem Ziel zuordnen, SalesOrderLine":::

4. <span data-ttu-id="59768-120">Nachdem **CDS-Auftragspositionen** erweitert wurde, ist das Feld **IntercompanyInventTransId** im Mapping verfügbar.</span><span class="sxs-lookup"><span data-stu-id="59768-120">After **CDS Sales Order Lines** is extended, the **IntercompanyInventTransId** field is available in the mapping.</span></span> <span data-ttu-id="59768-121">Wenden Sie einen Filter mit `INTERCOMPANYINVENTTRANSID == ""` als Abfragezeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="59768-121">Apply a filter with `INTERCOMPANYINVENTTRANSID == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="Auftragspositionen, Abfrage bearbeiten":::

5. <span data-ttu-id="59768-123">Erweitern Sie **Verkaufsrechnungskopfzeile V2** und **Verkaufsrechnungspositionen V2** auf die gleiche Weise, auf die Sie die Common Data Service-Entitäten in den Schritten 1 und 2 erweitert haben.</span><span class="sxs-lookup"><span data-stu-id="59768-123">Extend **Sales Invoice Header V2** and **Sales Invoice Lines V2** in the same way you extended the Common Data Service entities in steps 1 and 2.</span></span> <span data-ttu-id="59768-124">Fügen Sie dann die Filterabfragen hinzu.</span><span class="sxs-lookup"><span data-stu-id="59768-124">Then add the filter queries.</span></span> <span data-ttu-id="59768-125">Die Filterzeichenfolge für **Verkaufsrechnungskopfzeile V2** ist `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")`.</span><span class="sxs-lookup"><span data-stu-id="59768-125">The filter string for **Sales Invoice Header V2** is `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")`.</span></span> <span data-ttu-id="59768-126">Die Filterzeichenfolge für **Verkaufsrechnungspositionen V2** ist `INTERCOMPANYINVENTTRANSID == ""`.</span><span class="sxs-lookup"><span data-stu-id="59768-126">The filter string for **Sales Invoice Lines V2** is `INTERCOMPANYINVENTTRANSID == ""`.</span></span>

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="Staging dem Ziel zuordnen, Verkaufsrechnungskopfzeilen":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="Verkaufsrechnungskopfzeilen, Abfrage bearbeiten":::

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="Verkaufsrechnungspositionen, Abfrage bearbeiten":::

6. <span data-ttu-id="59768-130">Die Entität **Angebote** hat keine Intercompany-Beziehung.</span><span class="sxs-lookup"><span data-stu-id="59768-130">The **Quotations** entity doesn't have an intercompany relationship.</span></span> <span data-ttu-id="59768-131">Wenn jemand ein Angebot für einen Ihrer Intercompany-Kunden erstellt, können Sie alle diese Kunden über das Feld **Kundengruppe** in eine Kundengruppe einordnen.</span><span class="sxs-lookup"><span data-stu-id="59768-131">If someone creates a quote for one of your intercompany customers, you can put all of these customers in one customer group by using the **CustGroup** field.</span></span>  <span data-ttu-id="59768-132">Kopfzeilen und Positionen können erweitert werden, um das Feld **CustGroup** hinzuzufügen und anschließend zu filtern, um diese Gruppe nicht einzuschließen.</span><span class="sxs-lookup"><span data-stu-id="59768-132">Header and lines can be extended to add the **CustGroup** field and then filter to not include this group.</span></span>

    :::image type="content" source="media/filter-cust-group.png" alt-text="Staging dem Ziel zuordnen, Verkaufsangebotskopfzeile":::

7. <span data-ttu-id="59768-134">Nachdem Sie die Entität **Zitate** erweitert haben, wenden Sie einen Filter mit `CUSTGROUP !=  "<company>"` als Abfragezeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="59768-134">After you extent the **Quotations** entity, apply a filter with `CUSTGROUP !=  "<company>"` as the query string.</span></span>

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="Verkaufsangebotskopfzeile, Abfrage bearbeiten":::
