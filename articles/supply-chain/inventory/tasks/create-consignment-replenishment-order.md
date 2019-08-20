---
title: Unterlieferungs-Wiederbeschaffungsauftrag erstellen
description: Dieses Verfahren zeigt, wie ein Unterlieferungs-Wiederbeschaffungsauftrag erstellt wird, in dem Sie die erwartete Lieferung von einem Kreditor in den Lieferungsbestand verfolgen können.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ConsignmentReplenishmentOrder, ConsignmentReplenishmentOrderCreate, InventTrans, ConsignmentDraftReplenishmentOrderJournal, InventOnhandMovement, InventOnhandItem, InventItemIdLookupSimple
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2cf2e8f742fee2dedaac72902d207af0081700ca
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845545"
---
# <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="f1a07-103">Unterlieferungs-Wiederbeschaffungsauftrag erstellen</span><span class="sxs-lookup"><span data-stu-id="f1a07-103">Create a consignment replenishment order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f1a07-104">Dieses Verfahren zeigt, wie ein Unterlieferungs-Wiederbeschaffungsauftrag erstellt wird, in dem Sie die erwartete Lieferung von einem Kreditor in den Lieferungsbestand verfolgen können.</span><span class="sxs-lookup"><span data-stu-id="f1a07-104">This procedure shows how to create a consignment replenishment order where you can track the expected delivery from a vendor into your consignment inventory.</span></span> <span data-ttu-id="f1a07-105">Es zeigt auch, wie einen Produktempfang erfassen, damit der Lieferungsbestand als verfügbarer Lagerbestand im Besitz des Kreditors erfasst wird.</span><span class="sxs-lookup"><span data-stu-id="f1a07-105">It also shows how to record a receipt of products so that the consignment inventory is registered as on-hand inventory owned by the vendor.</span></span> <span data-ttu-id="f1a07-106">Diese Prozedur würde normalerweise durch einen Beschaffungsspezialist durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="f1a07-106">This procedure would typically be done by a procurement professional.</span></span> <span data-ttu-id="f1a07-107">Sie können diese Anleitung im Demodatenunternehmen USMF ausführen.</span><span class="sxs-lookup"><span data-stu-id="f1a07-107">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="f1a07-108">Diese Prozedur ist eine Funktion, für die in Dynamics 365 for Operations Version 1611 hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="f1a07-108">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>




## <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="f1a07-109">Unterlieferungs-Wiederbeschaffungsauftrag erstellen</span><span class="sxs-lookup"><span data-stu-id="f1a07-109">Create a consignment replenishment order</span></span>
1. <span data-ttu-id="f1a07-110">Wechseln Sie zu "Beschaffung" > "Lieferung" > "Unterlieferungs-Wiederbeschaffungsaufträge".</span><span class="sxs-lookup"><span data-stu-id="f1a07-110">Go to Procurement and sourcing > Consignment > Consignment replenishment orders.</span></span>
2. <span data-ttu-id="f1a07-111">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="f1a07-111">Click New.</span></span>
3. <span data-ttu-id="f1a07-112">Wählen Sie im Feld "Kreditorenkonto" "US-104" aus.</span><span class="sxs-lookup"><span data-stu-id="f1a07-112">In the Vendor account field, select vendor US-104.</span></span>
    * <span data-ttu-id="f1a07-113">Sie müssen einen Kreditor auswählen, der als Besitzer in der Bestandseigentümerseite erfasst wird.</span><span class="sxs-lookup"><span data-stu-id="f1a07-113">You must select a vendor that’s registered as an owner in the Inventory owners page.</span></span>  
4. <span data-ttu-id="f1a07-114">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f1a07-114">Click OK.</span></span>
5. <span data-ttu-id="f1a07-115">Klicken Sie auf "Position hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="f1a07-115">Click Add line.</span></span>
6. <span data-ttu-id="f1a07-116">Geben Sie im Feld "Artikelnummer" die Zeichenfolge "M9211CI." ein.</span><span class="sxs-lookup"><span data-stu-id="f1a07-116">In the Item number field, type M9211CI.</span></span>
    * <span data-ttu-id="f1a07-117">Sie müssen ein Artikel ausgewählt, der für Lieferungsbestand eingerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="f1a07-117">You must select an item that is set up for consignment inventory.</span></span>  
7. <span data-ttu-id="f1a07-118">Geben Sie im Feld "Menge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="f1a07-118">In the Quantity field, enter a number.</span></span>
8. <span data-ttu-id="f1a07-119">Geben Sie im Feld "Angefordertes Lieferdatum:" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="f1a07-119">In the Requested delivery date field, enter a date.</span></span>
    * <span data-ttu-id="f1a07-120">Die Angefordert und Bestätigt-Daten werden im MRP-Modul für den Wareneingang der erwarteten Waren verwendet.</span><span class="sxs-lookup"><span data-stu-id="f1a07-120">The requested and confirmed dates are used by the MRP engine for the expected arrival of the goods.</span></span>  
9. <span data-ttu-id="f1a07-121">Geben Sie im Feld "Bestätigtes Lieferdatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="f1a07-121">In the Confirmed delivery date field, enter a date.</span></span>
10. <span data-ttu-id="f1a07-122">Erweitern Sie den Abschnitt "Positionsdetails".</span><span class="sxs-lookup"><span data-stu-id="f1a07-122">Expand the Line details section.</span></span>
11. <span data-ttu-id="f1a07-123">Klicken Sie auf die Registerkarte "Lagerungsdimension".</span><span class="sxs-lookup"><span data-stu-id="f1a07-123">Click the Inventory dimensions tab.</span></span>
12. <span data-ttu-id="f1a07-124">Um den Eigentümer im Feld Lagerungsdimensionseigentümer anzuzeigen, aktualisieren der Seite.</span><span class="sxs-lookup"><span data-stu-id="f1a07-124">To show the owner in the Inventory dimensions owner field, refresh the page.</span></span>
    * <span data-ttu-id="f1a07-125">Kreditor US-104 wird jetzt als Besitzer aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="f1a07-125">Vendor US-104 is now listed as the owner.</span></span>  

## <a name="check-the-inventory-transaction-status"></a><span data-ttu-id="f1a07-126">Prüfen des Lagerbuchungstatus</span><span class="sxs-lookup"><span data-stu-id="f1a07-126">Check the inventory transaction status</span></span>
1. <span data-ttu-id="f1a07-127">Klicken Sie auf Lager.</span><span class="sxs-lookup"><span data-stu-id="f1a07-127">Click Inventory.</span></span>
2. <span data-ttu-id="f1a07-128">Klicken Sie auf "Transaktionen".</span><span class="sxs-lookup"><span data-stu-id="f1a07-128">Click Transactions.</span></span>
3. <span data-ttu-id="f1a07-129">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="f1a07-129">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="f1a07-130">Beachten Sie, dass das Zugangsfeld auf "Bestellt" festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="f1a07-130">Notice that the Receipt field is set to Ordered.</span></span>  
4. <span data-ttu-id="f1a07-131">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="f1a07-131">Close the page.</span></span>

## <a name="receive-items"></a><span data-ttu-id="f1a07-132">Artikel empfangen</span><span class="sxs-lookup"><span data-stu-id="f1a07-132">Receive items</span></span>
1. <span data-ttu-id="f1a07-133">Klicken Sie auf "Produktzugang".</span><span class="sxs-lookup"><span data-stu-id="f1a07-133">Click Product receipt.</span></span>
2. <span data-ttu-id="f1a07-134">Geben Sie im Feld "Externer Produktzugang" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="f1a07-134">In the External product receipt field, type a value.</span></span>
3. <span data-ttu-id="f1a07-135">Geben Sie im Feld "Menge" Sie eine Zahl ein, die geringer ist als die Zahl, die dort angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="f1a07-135">In the Quantity field, enter a number that’s lower than the number that’s shown there.</span></span> 
4. <span data-ttu-id="f1a07-136">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f1a07-136">Click OK.</span></span>

## <a name="check-the-on-hand-inventory"></a><span data-ttu-id="f1a07-137">Prüfen des verfügbaren Lagerbestands</span><span class="sxs-lookup"><span data-stu-id="f1a07-137">Check the on-hand inventory</span></span>
1. <span data-ttu-id="f1a07-138">Klicken Sie auf Lager.</span><span class="sxs-lookup"><span data-stu-id="f1a07-138">Click Inventory.</span></span>
2. <span data-ttu-id="f1a07-139">Klicken Sie auf "Verfügbar".</span><span class="sxs-lookup"><span data-stu-id="f1a07-139">Click On-hand.</span></span>
3. <span data-ttu-id="f1a07-140">Klicken Sie auf "Überblick".</span><span class="sxs-lookup"><span data-stu-id="f1a07-140">Click Overview.</span></span>
    * <span data-ttu-id="f1a07-141">Die Artikel, die als verfügbarer Lieferungsbestand eingegangen sind, der dem Kreditor gehört, sind der verfügbare Bestand.</span><span class="sxs-lookup"><span data-stu-id="f1a07-141">The items that have been received as consignment inventory owned by the vendor are available on-hand.</span></span> <span data-ttu-id="f1a07-142">Die Restmenge wird im auf dem Unterlieferungs-Wiederbeschaffungsauftrag wird im Feld "Insgesamt bestellt" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f1a07-142">The remaining quantity on the consignment replenishment order is shown in the Ordered in total field.</span></span>  
4. <span data-ttu-id="f1a07-143">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="f1a07-143">Close the page.</span></span>
5. <span data-ttu-id="f1a07-144">Klicken Sie auf "Schließen".</span><span class="sxs-lookup"><span data-stu-id="f1a07-144">Click Close.</span></span>

