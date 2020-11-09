---
title: Unterlieferungs-Wiederbeschaffungsauftrag erstellen
description: Dieses Thema erklärt, wie ein Unterlieferungs-Wiederbeschaffungsauftrag erstellt wird, in dem Sie die erwartete Lieferung von einem Kreditor in den Lieferungsbestand verfolgen können.
author: mkirknel
manager: tfehr
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ConsignmentReplenishmentOrder, ConsignmentReplenishmentOrderCreate, InventTrans, ConsignmentDraftReplenishmentOrderJournal, InventOnhandMovement, InventOnhandItem, InventItemIdLookupSimple, ConsignmentProductReceiptJournal, ConsignmentReplenishmentOrderLineQuantity
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e993190150e2d82088390d8db4b7c5ada2b0161
ms.sourcegitcommit: e3f4dd2257a3255c2982f4fc7b72a1121275b88a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4018352"
---
# <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="8f26d-103">Unterlieferungs-Wiederbeschaffungsauftrag erstellen</span><span class="sxs-lookup"><span data-stu-id="8f26d-103">Create a consignment replenishment order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8f26d-104">Dieses Thema erklärt, wie ein Unterlieferungs-Wiederbeschaffungsauftrag erstellt wird, in dem Sie die erwartete Lieferung von einem Kreditor in den Lieferungsbestand verfolgen können.</span><span class="sxs-lookup"><span data-stu-id="8f26d-104">This topic explains how to create a consignment replenishment order where you can track the expected delivery from a vendor into your consignment inventory.</span></span> <span data-ttu-id="8f26d-105">Es zeigt auch, wie einen Produktempfang erfassen, damit der Lieferungsbestand als verfügbarer Lagerbestand im Besitz des Kreditors erfasst wird.</span><span class="sxs-lookup"><span data-stu-id="8f26d-105">It also shows how to record a receipt of products so that the consignment inventory is registered as on-hand inventory owned by the vendor.</span></span> <span data-ttu-id="8f26d-106">Diese Prozedur würde normalerweise durch einen Beschaffungsspezialist durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="8f26d-106">This procedure would typically be done by a procurement professional.</span></span> <span data-ttu-id="8f26d-107">Sie können diese Anleitung im Demodatenunternehmen USMF ausführen.</span><span class="sxs-lookup"><span data-stu-id="8f26d-107">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="8f26d-108">Diese Prozedur ist eine Funktion, für die in Dynamics 365 for Operations Version 1611 hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="8f26d-108">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>

## <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="8f26d-109">Unterlieferungs-Wiederbeschaffungsauftrag erstellen</span><span class="sxs-lookup"><span data-stu-id="8f26d-109">Create a consignment replenishment order</span></span>
1. <span data-ttu-id="8f26d-110">Wechseln Sie im Navigationsbereich zu **Module > Beschaffung > Lieferung > Unterlieferungs-Wiederbeschaffungsaufträge**.</span><span class="sxs-lookup"><span data-stu-id="8f26d-110">In the navigation pane, go to **Modules > Procurement and sourcing > Consignment > Consignment replenishment orders**.</span></span>
2. <span data-ttu-id="8f26d-111">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="8f26d-111">Select **New**.</span></span>
3. <span data-ttu-id="8f26d-112">Wählen Sie im Feld **Kreditorenkonto** **US-104** aus (Sie müssen einen Kreditor auswählen, der als Besitzer auf der Seite **Bestandseigentümer** erfasst ist).</span><span class="sxs-lookup"><span data-stu-id="8f26d-112">In the **Vendor account** field, select vendor **US-104** (you must select a vendor that's registered as an owner in the **inventory owners** page).</span></span> 
4. <span data-ttu-id="8f26d-113">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="8f26d-113">Select **OK**.</span></span>
5. <span data-ttu-id="8f26d-114">Wählen Sie **Position hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="8f26d-114">Select **Add line**.</span></span>
6. <span data-ttu-id="8f26d-115">Wählen Sie im Feld **Artikelnummer** `M9211CI` aus (Sie müssen einen Artikel auswählen, der für Lieferbestand eingerichtet wurde).</span><span class="sxs-lookup"><span data-stu-id="8f26d-115">In the **Item number** field, type `M9211CI` (you must select an item that is set up for consignment inventory).</span></span>
7. <span data-ttu-id="8f26d-116">Geben Sie im Feld **Menge** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="8f26d-116">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="8f26d-117">Geben Sie im Feld **Angefordertes Lieferdatum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="8f26d-117">In the **Requested delivery date** field, enter a date.</span></span> <span data-ttu-id="8f26d-118">Die Angefordert und Bestätigt-Daten werden im MRP-Modul für den Wareneingang der erwarteten Waren verwendet.</span><span class="sxs-lookup"><span data-stu-id="8f26d-118">The requested and confirmed dates are used by the MRP engine for the expected arrival of the goods.</span></span>  
9. <span data-ttu-id="8f26d-119">Geben Sie im Feld **Bestätigtes Lieferdatum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="8f26d-119">In the **Confirmed delivery date** field, enter a date.</span></span>
10. <span data-ttu-id="8f26d-120">Erweitern Sie den Abschnitt **Positionsdetails**.</span><span class="sxs-lookup"><span data-stu-id="8f26d-120">Expand the **Line details** section.</span></span>
11. <span data-ttu-id="8f26d-121">Wählen Sie die Registerkarte **Lagerungsdimensionen** aus.</span><span class="sxs-lookup"><span data-stu-id="8f26d-121">Select the **Inventory dimensions** tab.</span></span>
12. <span data-ttu-id="8f26d-122">Um den Eigentümer im Feld **Lagerungsdimensionseigentümer** anzuzeigen, aktualisieren Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8f26d-122">To show the owner in the **Inventory dimensions owner** field, refresh the page.</span></span> <span data-ttu-id="8f26d-123">Kreditor US-104 wird jetzt als Besitzer aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="8f26d-123">Vendor US-104 is now listed as the owner.</span></span>  

## <a name="check-the-inventory-transaction-status"></a><span data-ttu-id="8f26d-124">Prüfen des Lagerbuchungstatus</span><span class="sxs-lookup"><span data-stu-id="8f26d-124">Check the inventory transaction status</span></span>
1. <span data-ttu-id="8f26d-125">Wählen Sie **Bestand** aus.</span><span class="sxs-lookup"><span data-stu-id="8f26d-125">Select **Inventory**.</span></span>
2. <span data-ttu-id="8f26d-126">Wählen Sie **Buchungen** aus.</span><span class="sxs-lookup"><span data-stu-id="8f26d-126">Select **Transactions**.</span></span>
3. <span data-ttu-id="8f26d-127">Beachten Sie in der gewünschten Zeile, dass das Feld **Zugang** auf **Bestellt** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="8f26d-127">In the desired row, notice that the **Receipt** field is set to **Ordered**.</span></span>  
4. <span data-ttu-id="8f26d-128">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8f26d-128">Close the page.</span></span>

## <a name="receive-items"></a><span data-ttu-id="8f26d-129">Artikel empfangen</span><span class="sxs-lookup"><span data-stu-id="8f26d-129">Receive items</span></span>
1. <span data-ttu-id="8f26d-130">Wählen Sie **Produktzugang** aus.</span><span class="sxs-lookup"><span data-stu-id="8f26d-130">Select **Product receipt**.</span></span>
2. <span data-ttu-id="8f26d-131">Geben Sie im Feld **Externer Produktzugang** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="8f26d-131">In the **External product receipt** field, type a value.</span></span>
3. <span data-ttu-id="8f26d-132">Geben Sie im Feld **Menge** eine Zahl ein, die geringer ist als jene Zahl, die dort angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="8f26d-132">In the **Quantity** field, enter a number that's lower than the number that's shown there.</span></span> 
4. <span data-ttu-id="8f26d-133">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="8f26d-133">Select **OK**.</span></span>

## <a name="check-the-on-hand-inventory"></a><span data-ttu-id="8f26d-134">Prüfen des verfügbaren Lagerbestands</span><span class="sxs-lookup"><span data-stu-id="8f26d-134">Check the on-hand inventory</span></span>
1. <span data-ttu-id="8f26d-135">Wählen Sie **Bestand** aus.</span><span class="sxs-lookup"><span data-stu-id="8f26d-135">Select **Inventory**.</span></span>
2. <span data-ttu-id="8f26d-136">Wählen Sie **Verfügbar** aus.</span><span class="sxs-lookup"><span data-stu-id="8f26d-136">Select **On-hand**.</span></span>
3. <span data-ttu-id="8f26d-137">Wählen Sie **Überblick** aus.</span><span class="sxs-lookup"><span data-stu-id="8f26d-137">Select **Overview**.</span></span> <span data-ttu-id="8f26d-138">Die Artikel, die als verfügbarer Lieferungsbestand eingegangen sind, der dem Kreditor gehört, sind der verfügbare Bestand.</span><span class="sxs-lookup"><span data-stu-id="8f26d-138">The items that have been received as consignment inventory owned by the vendor are available on-hand.</span></span> <span data-ttu-id="8f26d-139">Die Restmenge für den Unterlieferungs-Wiederbeschaffungsauftrag wird im Feld **Insgesamt bestellt** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8f26d-139">The remaining quantity on the consignment replenishment order is shown in the **Ordered in total** field.</span></span>  
4. <span data-ttu-id="8f26d-140">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8f26d-140">Close the page.</span></span>

