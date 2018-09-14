--- 
title: Unterlieferungs-Wiederbeschaffungsauftrag erstellen
description: "Dieses Verfahren zeigt, wie ein Unterlieferungs-Wiederbeschaffungsauftrag erstellt wird, in dem Sie die erwartete Lieferung von einem Kreditor in den Lieferungsbestand verfolgen können."
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ConsignmentReplenishmentOrder, ConsignmentReplenishmentOrderCreate, InventTrans, ConsignmentDraftReplenishmentOrderJournal, InventOnhandMovement, InventOnhandItem, InventItemIdLookupSimple
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 9d3e33008d04ea8bb7d145c7b63cec23a4a45dd2
ms.contentlocale: de-de
ms.lasthandoff: 09/14/2018

---
# <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="db832-103">Unterlieferungs-Wiederbeschaffungsauftrag erstellen</span><span class="sxs-lookup"><span data-stu-id="db832-103">Create a consignment replenishment order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="db832-104">Dieses Verfahren zeigt, wie ein Unterlieferungs-Wiederbeschaffungsauftrag erstellt wird, in dem Sie die erwartete Lieferung von einem Kreditor in den Lieferungsbestand verfolgen können.</span><span class="sxs-lookup"><span data-stu-id="db832-104">This procedure shows how to create a consignment replenishment order where you can track the expected delivery from a vendor into your consignment inventory.</span></span> <span data-ttu-id="db832-105">Es zeigt auch, wie einen Produktempfang erfassen, damit der Lieferungsbestand als verfügbarer Lagerbestand im Besitz des Kreditors erfasst wird.</span><span class="sxs-lookup"><span data-stu-id="db832-105">It also shows how to record a receipt of products so that the consignment inventory is registered as on-hand inventory owned by the vendor.</span></span> <span data-ttu-id="db832-106">Diese Prozedur würde normalerweise durch einen Beschaffungsspezialist durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="db832-106">This procedure would typically be done by a procurement professional.</span></span> <span data-ttu-id="db832-107">Sie können diese Anleitung im Demodatenunternehmen USMF ausführen.</span><span class="sxs-lookup"><span data-stu-id="db832-107">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="db832-108">Diese Prozedur ist für eine Funktion gedacht, die in Dynamics 365 for Operations Version 1611 hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="db832-108">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>




## <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="db832-109">Unterlieferungs-Wiederbeschaffungsauftrag erstellen</span><span class="sxs-lookup"><span data-stu-id="db832-109">Create a consignment replenishment order</span></span>
1. <span data-ttu-id="db832-110">Wechseln Sie zu "Beschaffung" > "Lieferung" > "Unterlieferungs-Wiederbeschaffungsaufträge".</span><span class="sxs-lookup"><span data-stu-id="db832-110">Go to Procurement and sourcing > Consignment > Consignment replenishment orders.</span></span>
2. <span data-ttu-id="db832-111">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="db832-111">Click New.</span></span>
3. <span data-ttu-id="db832-112">Wählen Sie im Feld "Kreditorenkonto" "US-104" aus.</span><span class="sxs-lookup"><span data-stu-id="db832-112">In the Vendor account field, select vendor US-104.</span></span>
    * <span data-ttu-id="db832-113">Sie müssen einen Kreditor auswählen, der als Besitzer in der Bestandseigentümerseite erfasst wird.</span><span class="sxs-lookup"><span data-stu-id="db832-113">You must select a vendor that’s registered as an owner in the Inventory owners page.</span></span>  
4. <span data-ttu-id="db832-114">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="db832-114">Click OK.</span></span>
5. <span data-ttu-id="db832-115">Klicken Sie auf "Position hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="db832-115">Click Add line.</span></span>
6. <span data-ttu-id="db832-116">Geben Sie im Feld "Artikelnummer" die Zeichenfolge "M9211CI." ein.</span><span class="sxs-lookup"><span data-stu-id="db832-116">In the Item number field, type M9211CI.</span></span>
    * <span data-ttu-id="db832-117">Sie müssen ein Artikel ausgewählt, der für Lieferungsbestand eingerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="db832-117">You must select an item that is set up for consignment inventory.</span></span>  
7. <span data-ttu-id="db832-118">Geben Sie im Feld "Menge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="db832-118">In the Quantity field, enter a number.</span></span>
8. <span data-ttu-id="db832-119">Geben Sie im Feld "Angefordertes Lieferdatum:" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="db832-119">In the Requested delivery date field, enter a date.</span></span>
    * <span data-ttu-id="db832-120">Die Angefordert und Bestätigt-Daten werden im MRP-Modul für den Wareneingang der erwarteten Waren verwendet.</span><span class="sxs-lookup"><span data-stu-id="db832-120">The requested and confirmed dates are used by the MRP engine for the expected arrival of the goods.</span></span>  
9. <span data-ttu-id="db832-121">Geben Sie im Feld "Bestätigtes Lieferdatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="db832-121">In the Confirmed delivery date field, enter a date.</span></span>
10. <span data-ttu-id="db832-122">Erweitern Sie den Abschnitt "Positionsdetails".</span><span class="sxs-lookup"><span data-stu-id="db832-122">Expand the Line details section.</span></span>
11. <span data-ttu-id="db832-123">Klicken Sie auf die Registerkarte "Lagerungsdimension".</span><span class="sxs-lookup"><span data-stu-id="db832-123">Click the Inventory dimensions tab.</span></span>
12. <span data-ttu-id="db832-124">Um den Eigentümer im Feld Lagerungsdimensionseigentümer anzuzeigen, aktualisieren der Seite.</span><span class="sxs-lookup"><span data-stu-id="db832-124">To show the owner in the Inventory dimensions owner field, refresh the page.</span></span>
    * <span data-ttu-id="db832-125">Kreditor US-104 wird jetzt als Besitzer aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="db832-125">Vendor US-104 is now listed as the owner.</span></span>  

## <a name="check-the-inventory-transaction-status"></a><span data-ttu-id="db832-126">Prüfen des Lagerbuchungstatus</span><span class="sxs-lookup"><span data-stu-id="db832-126">Check the inventory transaction status</span></span>
1. <span data-ttu-id="db832-127">Klicken Sie auf Lager.</span><span class="sxs-lookup"><span data-stu-id="db832-127">Click Inventory.</span></span>
2. <span data-ttu-id="db832-128">Klicken Sie auf "Transaktionen".</span><span class="sxs-lookup"><span data-stu-id="db832-128">Click Transactions.</span></span>
3. <span data-ttu-id="db832-129">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="db832-129">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="db832-130">Beachten Sie, dass das Zugangsfeld auf "Bestellt" festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="db832-130">Notice that the Receipt field is set to Ordered.</span></span>  
4. <span data-ttu-id="db832-131">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="db832-131">Close the page.</span></span>

## <a name="receive-items"></a><span data-ttu-id="db832-132">Artikel empfangen</span><span class="sxs-lookup"><span data-stu-id="db832-132">Receive items</span></span>
1. <span data-ttu-id="db832-133">Klicken Sie auf "Produktzugang".</span><span class="sxs-lookup"><span data-stu-id="db832-133">Click Product receipt.</span></span>
2. <span data-ttu-id="db832-134">Geben Sie im Feld "Externer Produktzugang" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="db832-134">In the External product receipt field, type a value.</span></span>
3. <span data-ttu-id="db832-135">Geben Sie im Feld "Menge" Sie eine Zahl ein, die geringer ist als die Zahl, die dort angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="db832-135">In the Quantity field, enter a number that’s lower than the number that’s shown there.</span></span> 
4. <span data-ttu-id="db832-136">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="db832-136">Click OK.</span></span>

## <a name="check-the-on-hand-inventory"></a><span data-ttu-id="db832-137">Prüfen des verfügbaren Lagerbestands</span><span class="sxs-lookup"><span data-stu-id="db832-137">Check the on-hand inventory</span></span>
1. <span data-ttu-id="db832-138">Klicken Sie auf Lager.</span><span class="sxs-lookup"><span data-stu-id="db832-138">Click Inventory.</span></span>
2. <span data-ttu-id="db832-139">Klicken Sie auf "Verfügbar".</span><span class="sxs-lookup"><span data-stu-id="db832-139">Click On-hand.</span></span>
3. <span data-ttu-id="db832-140">Klicken Sie auf "Überblick".</span><span class="sxs-lookup"><span data-stu-id="db832-140">Click Overview.</span></span>
    * <span data-ttu-id="db832-141">Die Artikel, die als verfügbarer Lieferungsbestand eingegangen sind, der dem Kreditor gehört, sind der verfügbare Bestand.</span><span class="sxs-lookup"><span data-stu-id="db832-141">The items that have been received as consignment inventory owned by the vendor are available on-hand.</span></span> <span data-ttu-id="db832-142">Die Restmenge wird im auf dem Unterlieferungs-Wiederbeschaffungsauftrag wird im Feld "Insgesamt bestellt" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="db832-142">The remaining quantity on the consignment replenishment order is shown in the Ordered in total field.</span></span>  
4. <span data-ttu-id="db832-143">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="db832-143">Close the page.</span></span>
5. <span data-ttu-id="db832-144">Klicken Sie auf "Schließen".</span><span class="sxs-lookup"><span data-stu-id="db832-144">Click Close.</span></span>


