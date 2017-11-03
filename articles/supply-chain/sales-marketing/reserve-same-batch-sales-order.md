---
title: "Reservieren derselben Charge für einen Auftrag"
description: "In diesem Artikel wird beschrieben, wie ein Produkt eingerichtet wird, um Bestandreservationen für eine einzelne Bestandcharge zu ermöglichen."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetailsExtended, EcoResStorageDimensionGroup, EcoResTrackingDimensionGroup, InventBatch, InventModelGroup, PdsAskSameLotForm, PdsCustSellableDays
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 28911
ms.assetid: 5823d75e-f839-46dd-beb3-e09b79fc8aa4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: aef3a52f4cb2d5af47a8c25a67e6c2076fa1ff03
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="reserve-the-same-batch-for-a-sales-order"></a><span data-ttu-id="89b78-103">Reservieren derselben Charge für einen Auftrag</span><span class="sxs-lookup"><span data-stu-id="89b78-103">Reserve the same batch for a sales order</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="89b78-104">In diesem Artikel wird beschrieben, wie ein Produkt eingerichtet wird, um Bestandreservationen für eine einzelne Bestandcharge zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="89b78-104">This article explains how to set up a product to allow reservation of inventory against a single batch of inventory.</span></span>

<span data-ttu-id="89b78-105">Mit der Reservierung derselben Charge können Sie Bestand für eine Auftragsposition aus einer einzelnen Lagercharge reservieren.</span><span class="sxs-lookup"><span data-stu-id="89b78-105">Same batch reservation lets you reserve inventory for a sales order line against a single batch of inventory.</span></span> <span data-ttu-id="89b78-106">Zum Beispiel kann ein Debitor, der Tapete bestellt, fordern, dass der gesamte Auftrag aus derselben Charge oder demselben Los stammt, damit Unterschiede zwischen den Rollen vermieden werden.</span><span class="sxs-lookup"><span data-stu-id="89b78-106">For example, a customer who orders wallpaper can request that the whole order be filled from the same batch or lot, to avoid inconsistencies among the rolls.</span></span> <span data-ttu-id="89b78-107">Damit ein Produkt die Reservierung derselben Charge verwendet, müssen die folgenden Einstellungen in den Artikelmodellgruppen, der Rückverfolgungsangabengruppe und der Lagerdimensionsgruppe, die alle dem Produkt zugewiesen werden, aktiviert sein:</span><span class="sxs-lookup"><span data-stu-id="89b78-107">To set up a product to use same batch reservation, the following settings must be active in the item model group, tracking dimension group, and storage dimension group that you assign to the product:</span></span>

-   <span data-ttu-id="89b78-108">**Artikelmodellgruppen** – Für die Artikelmodellgruppe müssen die Felder **Auswahl derselben Charge** und **Bedarf konsolidieren** in der Feldgruppe **Reservierung** für Bestandsrichtlinien aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="89b78-108">**Item model groups** – The item model group must have the **Same batch selection** and **Consolidate requirement** fields selected in the **Reservation** field group for inventory policies.</span></span>
-   <span data-ttu-id="89b78-109">**Rückverfolgungsangabengruppen** – Für die Rückverfolgungsangabengruppe muss das Feld **Disposition nach Dimensionen** für die Chargennummer aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="89b78-109">**Tracking dimensions groups** – The tracking dimension group must have the **Coverage plan by dimension** field selected for the batch number.</span></span>
-   <span data-ttu-id="89b78-110">**Lagerdimensionsgruppen** – Für die Lagerdimensionsgruppe muss das Feld **Disposition nach Dimensionen** für **Standort** und **Lagerort** aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="89b78-110">**Storage dimensions groups** – The storage dimension group must have the **Coverage plan by dimension** field selected for **Site** and **Warehouse**.</span></span>

<span data-ttu-id="89b78-111">Beim Reservieren von Bestand für ein Produkt in einer Auftragsposition, die für die Auswahl derselben Charge eingerichtet ist, versucht Microsoft Dynamics 365 for Finance and Operations, die aus einer einzelnen Lagercharge bestellte Menge zu reservieren.</span><span class="sxs-lookup"><span data-stu-id="89b78-111">When you reserve inventory for a product on a sales order line that is set up for same batch selection, Microsoft Dynamics 365 for Finance and Operations tries to reserve the ordered quantity from a single inventory batch.</span></span> <span data-ttu-id="89b78-112">Dabei werden auch bestimmte Chargenattributanforderungen berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="89b78-112">Any specific batch attribute requirements are also considered.</span></span> <span data-ttu-id="89b78-113">Kann die Menge nicht durch eine Charge abgedeckt werden kann, wird die Seite **Reservierungskonflikt aufgrund identischer Charge** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="89b78-113">If the quantity can't be filled from a single batch, the **Same batch reservation conflict** page appears.</span></span> <span data-ttu-id="89b78-114">Diese Seite beschreibt die Probleme und auch die Aktivitäten, die Sie ausführen können, um mit der Reservierung fortzufahren.</span><span class="sxs-lookup"><span data-stu-id="89b78-114">This page describes the issues and also the actions that you can take to continue with the reservation.</span></span> <span data-ttu-id="89b78-115">Die folgenden Umstände könnten verhindern, dass die Charge reserviert werden kann:</span><span class="sxs-lookup"><span data-stu-id="89b78-115">The following conditions might prevent the batch from being reserved:</span></span>

-   <span data-ttu-id="89b78-116">Im Chargendispositionscode ist die Einstellung **Reservierung sperren** für Verkäufe mit dem Status **Gesperrt** gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="89b78-116">The batch disposition code has **Block reservation** for sales flagged as **Blocked**.</span></span>
-   <span data-ttu-id="89b78-117">Die Charge ist abgelaufen (unter Berücksichtigung des Ablaufdatums und aller zutreffenden Verkaufstage für Debitoren).</span><span class="sxs-lookup"><span data-stu-id="89b78-117">The batch has expired, based on the expiration date and any applicable customer sellable days.</span></span> <span data-ttu-id="89b78-118">Der Artikel kann nach wie vor für die Reservierung berücksichtigt werden, wenn die Lagermodellgruppe für den Artikel First Expiry First Out (FEFO)-datumsgesteuert ist und Mindesthaltbarkeitsdatum als Kommissionierungskriterium ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="89b78-118">The item can still be considered for reservation if the item model group for the item is First Expiry First Out (FEFO) date–controlled, and if the best-before date is selected as the pick criterion.</span></span>
-   <span data-ttu-id="89b78-119">Die verbleibende Haltbarkeitsdauer der Charge ist unzureichend (dabei werden das Ablauf- bzw. Mindesthaltbarkeitsdatum sowie alle Verkaufstage für Debitoren berücksichtigt).</span><span class="sxs-lookup"><span data-stu-id="89b78-119">The batch doesn't have enough shelf-life days remaining, based on the expiration date and best-before date, plus any customer sellable days.</span></span>





