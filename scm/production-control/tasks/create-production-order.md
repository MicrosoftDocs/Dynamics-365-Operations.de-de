--- 
title: Produktionsauftrag erstellen
description: Diese Prozedur zeigt, wie ein Produktionsauftrag erstellt wird.
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: ac2ee418082aa6579424fc9480478587b7c22c6d
ms.contentlocale: de-de
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-production-order"></a><span data-ttu-id="8b8bd-103">Produktionsauftrag erstellen</span><span class="sxs-lookup"><span data-stu-id="8b8bd-103">Create a production order</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8b8bd-104">Diese Prozedur zeigt, wie ein Produktionsauftrag erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="8b8bd-104">This procedure shows how to create a production order.</span></span> <span data-ttu-id="8b8bd-105">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="8b8bd-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="8b8bd-106">Dies ist die erste Prozedur von sieben, die den Produktionsauftrags-Lebenszyklus erklärt.</span><span class="sxs-lookup"><span data-stu-id="8b8bd-106">This is the first procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="8b8bd-107">Produktionsauftrag erstellen</span><span class="sxs-lookup"><span data-stu-id="8b8bd-107">Create a production order</span></span>
1. <span data-ttu-id="8b8bd-108">Wechseln Sie zu "Produktionssteuerung" > "Produktionsaufträge" > "Alle Produktionsaufträge".</span><span class="sxs-lookup"><span data-stu-id="8b8bd-108">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="8b8bd-109">Klicken Sie auf "Neuer Produktionsauftrag".</span><span class="sxs-lookup"><span data-stu-id="8b8bd-109">Click New production order.</span></span>
3. <span data-ttu-id="8b8bd-110">Geben Sie im Feld "Artikelnummer" die Zeichenfolge "D0001" ein.</span><span class="sxs-lookup"><span data-stu-id="8b8bd-110">In the Item number field, type 'D0001'.</span></span>
4. <span data-ttu-id="8b8bd-111">Geben Sie im Feld "Lieferung" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="8b8bd-111">In the Delivery field, enter a date.</span></span>
    * <span data-ttu-id="8b8bd-112">Das Lieferdatum zeigt an, wann der Produktionsauftrag enden soll, um pünktlich zu liefern.</span><span class="sxs-lookup"><span data-stu-id="8b8bd-112">The delivery date indicates when the production order should end in order to deliver on time.</span></span> <span data-ttu-id="8b8bd-113">Dieses Datum kann im Planungsprozess verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8b8bd-113">This date can be used in the scheduling process.</span></span> <span data-ttu-id="8b8bd-114">Sie können beispielsweise den Auftrag rückwärts ab dem Lieferdatum planen.</span><span class="sxs-lookup"><span data-stu-id="8b8bd-114">For example, you can schedule the order backward from the delivery date.</span></span>  
5. <span data-ttu-id="8b8bd-115">Legen Sie die Menge auf "20" fest.</span><span class="sxs-lookup"><span data-stu-id="8b8bd-115">Set Quantity to '20'.</span></span>
    * <span data-ttu-id="8b8bd-116">Hinweis: Das Feld "Stücklistennummer" zeigt automatisch die Nummer von jeder aktiven Stücklisten für den aktuellen Artikel an, aber Sie können die Stückliste für den Produktionsauftrag ändern, indem Sie eine aktive Stückliste aus der Liste der genehmigten Stücklistenversionen auswählen.</span><span class="sxs-lookup"><span data-stu-id="8b8bd-116">Note: The BOM number field automatically displays the number of any active BOM for the current item, but you can change the BOM for the production order by selecting an active BOM from the list of approved BOM versions.</span></span>    <span data-ttu-id="8b8bd-117">Das Feld "Arbeitsplannummer" zeigt automatisch die Nummer von jeder aktiven Stücklisten für den aktuellen Artikel an, aber Sie können den Arbeitsplan für den Produktionsauftrag ändern, indem Sie einen aktiven Arbeitsplan aus der Liste der genehmigten Arbeitsplanversionen auswählen.</span><span class="sxs-lookup"><span data-stu-id="8b8bd-117">The Route number field automatically displays the number of any active Route for the current item, but you can change the Route for the production order by selecting an active Route from the list of approved Route versions.</span></span>  
6. <span data-ttu-id="8b8bd-118">Klicken Sie auf "Erstellen".</span><span class="sxs-lookup"><span data-stu-id="8b8bd-118">Click Create.</span></span>

## <a name="validate-the-production-order"></a><span data-ttu-id="8b8bd-119">Den Produktionsauftrag überprüfen</span><span class="sxs-lookup"><span data-stu-id="8b8bd-119">Validate the production order</span></span>
1. <span data-ttu-id="8b8bd-120">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="8b8bd-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="8b8bd-121">Klicken Sie auf den Link für die Produktionsauftragsnummer, die Sie soeben erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="8b8bd-121">Click the link for the production order number that you have just created.</span></span> <span data-ttu-id="8b8bd-122">Dadurch wird die Detailseite für den Auftrag geöffnet.</span><span class="sxs-lookup"><span data-stu-id="8b8bd-122">This will open the details page for the order.</span></span>  
2. <span data-ttu-id="8b8bd-123">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="8b8bd-123">Click Edit.</span></span>
3. <span data-ttu-id="8b8bd-124">Geben Sie im Feld "Lieferung" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="8b8bd-124">In the Delivery field, enter a date.</span></span>
    * <span data-ttu-id="8b8bd-125">Sie können beispielsweise das Lieferdatum für den Produktionsauftrag ändern.</span><span class="sxs-lookup"><span data-stu-id="8b8bd-125">For example, you can change the delivery date for the production order.</span></span>  
4. <span data-ttu-id="8b8bd-126">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="8b8bd-126">Click Save.</span></span>
5. <span data-ttu-id="8b8bd-127">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8b8bd-127">Close the page.</span></span>

## <a name="update-the-bom"></a><span data-ttu-id="8b8bd-128">Die Stückliste aktualisieren</span><span class="sxs-lookup"><span data-stu-id="8b8bd-128">Update the BOM</span></span>
1. <span data-ttu-id="8b8bd-129">Klicken Sie im Aktivitätsbereich auf "Produktionsauftrag".</span><span class="sxs-lookup"><span data-stu-id="8b8bd-129">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="8b8bd-130">Klicken Sie auf "Stückliste".</span><span class="sxs-lookup"><span data-stu-id="8b8bd-130">Click BOM.</span></span>
    * <span data-ttu-id="8b8bd-131">Öffnen Sie die Stücklistenseite, um die Stücklistendaten zu prüfen, die von den Standarddaten kopiert wurden, als der Produktionsauftrag erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="8b8bd-131">Open the BOM page to validate the BOM data that was copied from the default data when the production order was created.</span></span> <span data-ttu-id="8b8bd-132">In dieser Prozedur müssen Sie die Menge für eine Stückliste aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="8b8bd-132">In this procedure, you need to update the quantity for a BOM.</span></span>  
3. <span data-ttu-id="8b8bd-133">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="8b8bd-133">Click Edit.</span></span>
4. <span data-ttu-id="8b8bd-134">Geben Sie im Feld "Menge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="8b8bd-134">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="8b8bd-135">Das Ändern der Menge in der Stücklistenposition wirkt sich auf die Vorkalkulation des Materialverbrauchs für den Produktionsauftrag aus.</span><span class="sxs-lookup"><span data-stu-id="8b8bd-135">Changing the quantity on the BOM line affects the cost estimate of material consumption for the production order.</span></span>  
5. <span data-ttu-id="8b8bd-136">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="8b8bd-136">Click Save.</span></span>
6. <span data-ttu-id="8b8bd-137">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8b8bd-137">Close the page.</span></span>

## <a name="update-the-production-route"></a><span data-ttu-id="8b8bd-138">Den Produktionsarbeitsplan aktualisieren</span><span class="sxs-lookup"><span data-stu-id="8b8bd-138">Update the production route</span></span>
1. <span data-ttu-id="8b8bd-139">Klicken Sie im Aktivitätsbereich auf "Produktionsauftrag".</span><span class="sxs-lookup"><span data-stu-id="8b8bd-139">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="8b8bd-140">Klicken Sie auf "Arbeitsplan".</span><span class="sxs-lookup"><span data-stu-id="8b8bd-140">Click Route.</span></span>
    * <span data-ttu-id="8b8bd-141">Öffnen Sie die Arbeitsplanseite, um die Daten des Produktionsarbeitsplans zu prüfen, die von den Standarddaten kopiert wurden, als der Auftrag erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="8b8bd-141">Open the Route page to validate the data of the production route that was copied from the default data when the order was created.</span></span> <span data-ttu-id="8b8bd-142">In dieser Prozedur müssen Sie die Menge für einen der Arbeitsgänge im Produktionsarbeitsplan aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="8b8bd-142">In this procedure, you need to update the quantity for one of the operations in the production route.</span></span>  
3. <span data-ttu-id="8b8bd-143">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="8b8bd-143">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="8b8bd-144">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="8b8bd-144">Click Edit.</span></span>
5. <span data-ttu-id="8b8bd-145">Geben Sie im Feld "Bearb. Menge"</span><span class="sxs-lookup"><span data-stu-id="8b8bd-145">In the Process qty.</span></span> <span data-ttu-id="8b8bd-146">eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="8b8bd-146">field, enter a number.</span></span>
    * <span data-ttu-id="8b8bd-147">Das Ändern der Bearbeitungszeit wirkt sich auf die geschätzte Arbeitsplanrückmeldung und die Kosten des Produktionsauftrags aus.</span><span class="sxs-lookup"><span data-stu-id="8b8bd-147">Changing the process time affects the estimated route consumption and the cost of the production order.</span></span>  
6. <span data-ttu-id="8b8bd-148">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="8b8bd-148">Click Save.</span></span>
7. <span data-ttu-id="8b8bd-149">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8b8bd-149">Close the page.</span></span>


