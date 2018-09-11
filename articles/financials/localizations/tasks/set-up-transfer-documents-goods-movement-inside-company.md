--- 
title: "Umlagerungsdokument für Warenbewegung innerhalb eines Unternehmens einrichten"
description: "Dieses Verfahren zeigt, wie Umlagerungsdokumente für Warenbewegung innerhalb eines Unternehmens erstellt werden."
author: v-oloski
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventTransferOrders, InventLocationIdLookup, TransportationDocument, HcmWorkerLookUp, SrsReportViewerForm, InventTransferParmShip
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 0bb78219a5fb02a95d1b9d8cda592293406ce844
ms.contentlocale: de-de
ms.lasthandoff: 09/11/2018

---
# <a name="set-up-the-transfer-documents-for-goods-movement-inside-a-company"></a><span data-ttu-id="c8e52-103">Umlagerungsdokument für Warenbewegung innerhalb eines Unternehmens einrichten</span><span class="sxs-lookup"><span data-stu-id="c8e52-103">Set up the transfer documents for goods movement inside a company</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c8e52-104">Dieses Verfahren zeigt, wie Umlagerungsdokumente für Warenbewegung innerhalb eines Unternehmens erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="c8e52-104">This procedure shows how to create transfer documents for goods movement inside a company.</span></span> <span data-ttu-id="c8e52-105">Diese Prozedur ist nur für juristische Personen mit einer primären Adresse in Litauen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c8e52-105">This procedure is only available for legal entities with a primary address in Lithuania.</span></span> <span data-ttu-id="c8e52-106">Diese Prozedur wurde mithilfe des Demodatenunternehmens DEMF mit der primären Adresse einer juristischen Person in Litauen erstellt.</span><span class="sxs-lookup"><span data-stu-id="c8e52-106">The procedure was created using the demo data company DEMF with a primary address in Lithuania.</span></span> <span data-ttu-id="c8e52-107">Bevor Sie dieses Verfahren ausführen können, müssen Sie das Verfahren "Umlagerungsdokumente für Warenbewegung innerhalb eines Unternehmens erstellen" ausführen.</span><span class="sxs-lookup"><span data-stu-id="c8e52-107">Before you can complete this procedure, you must complete the “Set up transfer documents for goods movement inside a company” procedure.</span></span> <span data-ttu-id="c8e52-108">Diese Prozedur ist für Bestandsbuchhalter vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="c8e52-108">This procedure is intended for inventory accountants.</span></span> <span data-ttu-id="c8e52-109">Diese Prozedur ist eine Funktion, die in Dynamics 365 for Operations, Version 1611 hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="c8e52-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-transfer-order"></a><span data-ttu-id="c8e52-110">Erstellen eines Umlagerungsauftrags</span><span class="sxs-lookup"><span data-stu-id="c8e52-110">Create a transfer order</span></span>
1. <span data-ttu-id="c8e52-111">Navigieren zur Lagerverwaltung > Eingehende Aufträge > Umlagerungsauftrag.</span><span class="sxs-lookup"><span data-stu-id="c8e52-111">Go to Inventory management > Inbound orders > Transfer order.</span></span>
2. <span data-ttu-id="c8e52-112">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="c8e52-112">Click New.</span></span>
3. <span data-ttu-id="c8e52-113">Geben Sie im Feld "Von Lagerort" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="c8e52-113">In the From warehouse field, enter or select a value.</span></span>
4. <span data-ttu-id="c8e52-114">Geben Sie im Feld "Nach Lagerort" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="c8e52-114">In the To warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="c8e52-115">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c8e52-115">Click Add.</span></span>
6. <span data-ttu-id="c8e52-116">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="c8e52-116">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="c8e52-117">Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="c8e52-117">In the Item number field, enter or select a value.</span></span>

## <a name="enter-transportation-details-for-the-transfer-order"></a><span data-ttu-id="c8e52-118">Transportdetails für Umlagerungsauftrag ausfüllen</span><span class="sxs-lookup"><span data-stu-id="c8e52-118">Enter transportation details for the transfer order</span></span>
1. <span data-ttu-id="c8e52-119">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="c8e52-119">Click Save.</span></span>
2. <span data-ttu-id="c8e52-120">Klicken Sie im Aktivitätsbereich auf Versenden.</span><span class="sxs-lookup"><span data-stu-id="c8e52-120">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="c8e52-121">Klicken Sie auf Transportdetails.</span><span class="sxs-lookup"><span data-stu-id="c8e52-121">Click Transportation details.</span></span>
4. <span data-ttu-id="c8e52-122">Wählen Sie die Option Ja im Feld "Transportdetails drucken" aus.</span><span class="sxs-lookup"><span data-stu-id="c8e52-122">Select Yes in the Print transportation details field.</span></span>
5. <span data-ttu-id="c8e52-123">Geben Sie im Feld 'Wahren genehmigt von' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="c8e52-123">In the Goods issued by field, enter or select a value.</span></span>
6. <span data-ttu-id="c8e52-124">Geben Sie im Feld 'Verpackung' einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="c8e52-124">In the Package field, type a value.</span></span>
7. <span data-ttu-id="c8e52-125">Geben Sie im Feld "Risikoebene der Auslastung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="c8e52-125">In the Risk level of the load field, type a value.</span></span>
8. <span data-ttu-id="c8e52-126">Geben Sie im Feld 'Spediteur' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="c8e52-126">In the Carrier field, enter or select a value.</span></span>
9. <span data-ttu-id="c8e52-127">Geben Sie im Feld 'Modell' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="c8e52-127">In the Model field, enter or select a value.</span></span>
10. <span data-ttu-id="c8e52-128">Geben Sie im Feld "Registrierungsnummer" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="c8e52-128">In the Registration number field, type a value.</span></span>
11. <span data-ttu-id="c8e52-129">Geben Sie im Feld "Anhängererfassungsnummer" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="c8e52-129">In the Trailer registration number field, type a value.</span></span>
12. <span data-ttu-id="c8e52-130">Geben Sie im Feld 'Fahrer' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="c8e52-130">In the Driver field, enter or select a value.</span></span>
13. <span data-ttu-id="c8e52-131">Geben Sie im Feld "Fahrername" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="c8e52-131">In the Driver name field, type a value.</span></span>
14. <span data-ttu-id="c8e52-132">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="c8e52-132">Click Save.</span></span>
15. <span data-ttu-id="c8e52-133">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="c8e52-133">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-unposted-transfer-order"></a><span data-ttu-id="c8e52-134">Anzeigen des Lieferscheins für nicht gebuchten Umlagerungsauftrag</span><span class="sxs-lookup"><span data-stu-id="c8e52-134">View the packing slip for the unposted transfer order</span></span>
1. <span data-ttu-id="c8e52-135">Klicken Sie auf "Lieferschein".</span><span class="sxs-lookup"><span data-stu-id="c8e52-135">Click Packing slip.</span></span>
2. <span data-ttu-id="c8e52-136">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="c8e52-136">Click OK.</span></span>
3. <span data-ttu-id="c8e52-137">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="c8e52-137">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-posted-transfer-order"></a><span data-ttu-id="c8e52-138">Anzeigen des Lieferscheins für gebuchten Umlagerungsauftrag</span><span class="sxs-lookup"><span data-stu-id="c8e52-138">View the packing slip for the posted transfer order</span></span>
1. <span data-ttu-id="c8e52-139">Klicken Sie im Aktivitätsbereich auf Umlagerungsauftrag.</span><span class="sxs-lookup"><span data-stu-id="c8e52-139">On the Action Pane, click Transfer order.</span></span>
2. <span data-ttu-id="c8e52-140">Klicken Sie im Aktivitätsbereich auf Versenden.</span><span class="sxs-lookup"><span data-stu-id="c8e52-140">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="c8e52-141">Klicken Sie auf "Umlagerungsauftrag versenden".</span><span class="sxs-lookup"><span data-stu-id="c8e52-141">Click Ship transfer order.</span></span>
4. <span data-ttu-id="c8e52-142">Klicken Sie auf die Registerkarte "Allgemein".</span><span class="sxs-lookup"><span data-stu-id="c8e52-142">Click the General tab.</span></span>
5. <span data-ttu-id="c8e52-143">Wählen Sie im Feld 'Aktualisieren' eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="c8e52-143">In the Update field, select an option.</span></span>
6. <span data-ttu-id="c8e52-144">Klicken Sie auf die Registerkarte "Überblick".</span><span class="sxs-lookup"><span data-stu-id="c8e52-144">Click the Overview tab.</span></span>
7. <span data-ttu-id="c8e52-145">Geben Sie im Feld "Lieferschein" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="c8e52-145">In the Packing slip field, type a value.</span></span>
8. <span data-ttu-id="c8e52-146">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="c8e52-146">Click OK.</span></span>
9. <span data-ttu-id="c8e52-147">Klicken Sie im Aktivitätsbereich auf Versenden.</span><span class="sxs-lookup"><span data-stu-id="c8e52-147">On the Action Pane, click Ship.</span></span>
10. <span data-ttu-id="c8e52-148">Klicken Sie auf "Lieferschein".</span><span class="sxs-lookup"><span data-stu-id="c8e52-148">Click Packing slip.</span></span>
11. <span data-ttu-id="c8e52-149">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="c8e52-149">Click OK.</span></span>


