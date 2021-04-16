---
title: Nachverfolgen der laufenden Durchschnittskosten pro Lagerungsdimension
description: Jedem Lagerartikel ist eine Lagerdimensionsgruppe zugewiesen. Der laufende Durchschnittseinstandspreis für einen Artikel wird deshalb auf Basis der Auswahl von Lagerungsdimensionen berechnet, die wertmäßig verfolgt werden.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 75053
ms.assetid: 68cc00f4-0f7a-4a7d-be90-8f2e0d0563d3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8da13a01b28ca09ce9c29ecd3a9342dfb9eaa4bd
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834312"
---
# <a name="track-running-average-cost-per-inventory-dimension"></a><span data-ttu-id="f4b2d-104">Nachverfolgen der laufenden Durchschnittskosten pro Lagerungsdimension</span><span class="sxs-lookup"><span data-stu-id="f4b2d-104">Track running average cost per inventory dimension</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f4b2d-105">Jedem Lagerartikel ist eine Lagerdimensionsgruppe zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="f4b2d-105">An inventory dimension group is attached to every inventory item.</span></span> <span data-ttu-id="f4b2d-106">Der laufende Durchschnittseinstandspreis für einen Artikel wird deshalb auf Basis der Auswahl von Lagerungsdimensionen berechnet, die wertmäßig verfolgt werden.</span><span class="sxs-lookup"><span data-stu-id="f4b2d-106">Therefore, the running average cost price of an item is calculated based on the selected inventory dimensions that are being tracked financially.</span></span>

<span data-ttu-id="f4b2d-107">Drei Arten von Lagerungsdimensionen sind verfügbar: Produkt, Lagerung und Nachverfolgung.</span><span class="sxs-lookup"><span data-stu-id="f4b2d-107">There are three types of inventory dimensions: product, storage, and tracking.</span></span> <span data-ttu-id="f4b2d-108">Zu den Produktdimensionen zählen "Variante", "Größe" und "Farbe".</span><span class="sxs-lookup"><span data-stu-id="f4b2d-108">Product dimensions include configuration, size, and color.</span></span> <span data-ttu-id="f4b2d-109">Produktdimensionen werden immer wertmäßig verfolgt.</span><span class="sxs-lookup"><span data-stu-id="f4b2d-109">Product dimensions are always tracked financially.</span></span> <span data-ttu-id="f4b2d-110">Zu den Lager- und Überwachungsdimensionen zählen "Standort", "Lagerort", ""Lagerplatz", "Bestandsstatus", "Ladungsträger", "Chargennummer" und "Seriennummer".</span><span class="sxs-lookup"><span data-stu-id="f4b2d-110">Storage and tracking dimensions include site, warehouse, location, inventory status, license plate, batch number, and serial number.</span></span> <span data-ttu-id="f4b2d-111">Bei Lager- und Überwachungsdimensionen können Sie entscheiden, welche Dimensionen wertmäßig verfolgt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f4b2d-111">You can decide which storage and tracking dimensions are tracked financially.</span></span> 

<span data-ttu-id="f4b2d-112">**Beispiel 1**</span><span class="sxs-lookup"><span data-stu-id="f4b2d-112">**Example 1**</span></span> 

<span data-ttu-id="f4b2d-113">Wenn die Lagerdimensionsgruppe, die dem zugeordnete ist, wertmäßig nach Lagerort verfolgt wird, werden die laufenden Durchschnittseinstandspreis für jeden Lagerort berechnet.</span><span class="sxs-lookup"><span data-stu-id="f4b2d-113">If the storage dimension group that is attached to the item is financially tracked by warehouse, the running average cost price is calculated per warehouse.</span></span> <span data-ttu-id="f4b2d-114">Folgende Bestellungen wurden fakturiert:</span><span class="sxs-lookup"><span data-stu-id="f4b2d-114">The following purchase orders have been invoiced:</span></span>

-   <span data-ttu-id="f4b2d-115">Eine Bestellung der Menge "2" zu einem Einstandspreis von EUR 10,00, fakturiert für den Lagerort "GW".</span><span class="sxs-lookup"><span data-stu-id="f4b2d-115">A purchase order for a quantity of 2 at a cost price of USD 10.00 has been invoiced for warehouse GW.</span></span>
-   <span data-ttu-id="f4b2d-116">Eine Bestellung der Menge "3" zu einem Einstandspreis von EUR 12,00, fakturiert für den Lagerort "GW".</span><span class="sxs-lookup"><span data-stu-id="f4b2d-116">A purchase order for a quantity of 3 at a cost price of USD 12.00 has been invoiced for warehouse GW.</span></span>
-   <span data-ttu-id="f4b2d-117">Eine Bestellung der Menge "5" zu einem Einstandspreis von EUR 15,00, fakturiert für den Lagerort "MW".</span><span class="sxs-lookup"><span data-stu-id="f4b2d-117">A purchase order for a quantity of 5 at a cost price of USD 15.00 has been invoiced for warehouse MW.</span></span>

<span data-ttu-id="f4b2d-118">Der laufende Durchschnittseinstandspreis für den Lagerort "GW" beträgt EUR 11,20, und der laufende Durchschnittseinstandspreis für den Lagerort "MW" beträgt EUR 15,00.</span><span class="sxs-lookup"><span data-stu-id="f4b2d-118">The running average cost price for warehouse GW is USD 11.20, and the running average cost price for warehouse MW is USD 15.00.</span></span> <span data-ttu-id="f4b2d-119">Für den Lagerort "GW" wird eine Auftragsrechnung gebucht.</span><span class="sxs-lookup"><span data-stu-id="f4b2d-119">A sales order invoice is posted for warehouse GW.</span></span> <span data-ttu-id="f4b2d-120">Der Wert für das Lager und für den Wareneinsatz (vor dem Ausführen des Lagerabschlusses und ohne Markierung) beträgt EUR 11,20.</span><span class="sxs-lookup"><span data-stu-id="f4b2d-120">The value of the inventory and the cost of goods sold (before inventory close is run and without marking) is USD 11.20.</span></span> <span data-ttu-id="f4b2d-121">Für den Lagerort "MW" wird ein weiterer Auftrag gebucht.</span><span class="sxs-lookup"><span data-stu-id="f4b2d-121">Another sales order is posted for warehouse MW.</span></span> <span data-ttu-id="f4b2d-122">Der Wert für das Lager und für den Wareneinsatz (vor dem Ausführen des Lagerabschlusses und ohne Markierung) beträgt EUR 15,00.</span><span class="sxs-lookup"><span data-stu-id="f4b2d-122">The value of the inventory and the cost of goods sold (before inventory close is run and without marking) is USD 15.00.</span></span> 

<span data-ttu-id="f4b2d-123">**Beispiel 2** Wenn die Lagerdimensionsgruppe, die dem Artikel zugeordnet ist, wertmäßig nach Lagerort und die Rückverfolgungsangabengruppe wertmäßig nach Chargennummer verfolgt wird, wird der laufende Durchschnittseinstandspreis für jede Charge berechnet.</span><span class="sxs-lookup"><span data-stu-id="f4b2d-123">**Example 2** If the storage dimension group that is attached to the item is financially tracked by warehouse, and the tracking dimension group is financially tracked by batch number, the running average cost price is calculated for each batch.</span></span> 

<span data-ttu-id="f4b2d-124">**Hinweis:** Es empfiehlt sich, den Einstandspreis immer zusammen mit allen wertmäßig nachverfolgten Dimensionen zu betrachten.</span><span class="sxs-lookup"><span data-stu-id="f4b2d-124">**Note:** We recommend that you always view the cost price for all financial dimensions that are being tracked.</span></span> <span data-ttu-id="f4b2d-125">Folgende Bestellungen wurden fakturiert:</span><span class="sxs-lookup"><span data-stu-id="f4b2d-125">The following purchase orders have been invoiced:</span></span>

-   <span data-ttu-id="f4b2d-126">Eine Bestellung der Menge "2" zu einem Einstandspreis von EUR 10,00 wurde für den Lagerort "GW" und die Charge "AAA" fakturiert.</span><span class="sxs-lookup"><span data-stu-id="f4b2d-126">A purchase order for a quantity of 2 at a cost price of USD 10.00 has been invoiced for warehouse GW and batch AAA.</span></span>
-   <span data-ttu-id="f4b2d-127">Eine Bestellung der Menge "3" zu einem Einstandspreis von EUR 12,00 wurde für den Lagerort "GW" und die Charge "AAA" fakturiert.</span><span class="sxs-lookup"><span data-stu-id="f4b2d-127">A purchase order for a quantity of 3 at a cost price of USD 12.00 has been invoiced for warehouse GW and batch AAA.</span></span>
-   <span data-ttu-id="f4b2d-128">Eine Bestellung der Menge "2" zu einem Einstandspreis von EUR 15,00 wurde für den Lagerort "GW" und die Charge "BBB" fakturiert.</span><span class="sxs-lookup"><span data-stu-id="f4b2d-128">A purchase order for a quantity of 2 at a cost price of USD 15.00 has been invoiced for warehouse GW and batch BBB.</span></span>

<span data-ttu-id="f4b2d-129">Der laufende Durchschnittseinstandspreis für den Lagerort "GW" und Charge "AAA" beträgt EUR 11,20, und der laufende Durchschnittseinstandspreis für den Lagerort "GW" und Charge "BBB" beträgt EUR 15,00.</span><span class="sxs-lookup"><span data-stu-id="f4b2d-129">The running average cost price for warehouse GW and batch AAA is USD 11.20, and the running average cost price for warehouse GW and batch BBB is USD 15.00.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]