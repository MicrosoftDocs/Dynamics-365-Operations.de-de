---
title: Sicherheitsbestandserfassung verwenden, um die Mindestdeckung zu aktualisieren
description: Diese Prozedur zeigt, wie man die Vorschläge zur Mindestdeckung berechnet, basierend auf früheren Transaktionen, und dann die Artikeldeckung mit dem Vorschlag aktualisiert.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7a6e217d476cedc0318c382e12b7dc2036e557c3
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571426"
---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage"></a><span data-ttu-id="43400-103">Sicherheitsbestandserfassung verwenden, um die Mindestdeckung zu aktualisieren</span><span class="sxs-lookup"><span data-stu-id="43400-103">Use the safety stock journal to update minimum coverage</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="43400-104">Diese Prozedur zeigt, wie man die Vorschläge zur Mindestdeckung berechnet, basierend auf früheren Transaktionen, und dann die Artikeldeckung mit dem Vorschlag aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="43400-104">This procedure shows how to calculate minimum coverage proposals based on historical transactions and then update the item coverage with the proposals.</span></span> <span data-ttu-id="43400-105">Dieses wird unter Verwendung der Sicherheitsbestandserfassung getan.</span><span class="sxs-lookup"><span data-stu-id="43400-105">This is done using the safety stock journal.</span></span> <span data-ttu-id="43400-106">Das Demodatenunternehmen, das verwendet wird, um diese Aufgabe zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="43400-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="43400-107">Diese Aufgabe ist für den Produktionsplaner bestimmt, um mithilfe davon die Mindestdeckung beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="43400-107">This task is intended for the production planner, to help maintain minimum coverage.</span></span>


## <a name="create-a-new-safety-stock-journal-name"></a><span data-ttu-id="43400-108">Einen neuen Sicherheitsbestands-Erfassungsname erstellen</span><span class="sxs-lookup"><span data-stu-id="43400-108">Create a new safety stock journal name</span></span>
1. <span data-ttu-id="43400-109">Wechseln Sie zu Sicherheitsbestands-Erfassungsnamen.</span><span class="sxs-lookup"><span data-stu-id="43400-109">Go to Safety stock journal names.</span></span>
2. <span data-ttu-id="43400-110">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="43400-110">Click New.</span></span>
3. <span data-ttu-id="43400-111">Geben Sie im Feld "Name" die Bezeichnung "Material" ein.</span><span class="sxs-lookup"><span data-stu-id="43400-111">In the Name field, type 'Material'.</span></span>
4. <span data-ttu-id="43400-112">Geben Sie im Feld "Beschreibung" die Bezeichnung "Material" ein.</span><span class="sxs-lookup"><span data-stu-id="43400-112">In the Description field, type 'Material'.</span></span>
5. <span data-ttu-id="43400-113">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="43400-113">Close the page.</span></span>

## <a name="create-a-safety-stock-journal"></a><span data-ttu-id="43400-114">Eine Sicherheitsbestandserfassung erstellen</span><span class="sxs-lookup"><span data-stu-id="43400-114">Create a safety stock journal</span></span>
1. <span data-ttu-id="43400-115">Wechseln Sie zu Sicherheitsbestandsberechnung.</span><span class="sxs-lookup"><span data-stu-id="43400-115">Go to Safety stock calculation.</span></span>
2. <span data-ttu-id="43400-116">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="43400-116">Click New.</span></span>
3. <span data-ttu-id="43400-117">Geben Sie im Feld "Name" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="43400-117">In the Name field, enter or select a value.</span></span>
    * <span data-ttu-id="43400-118">Wählen Sie den Sicherheitsbestands-Erfassungsname aus, den Sie erstellt haben, zum Beispiel "Material".</span><span class="sxs-lookup"><span data-stu-id="43400-118">Select the safety stock journal name that you created, for example, Material.</span></span>  
4. <span data-ttu-id="43400-119">Klicken Sie auf "Positionen erstellen".</span><span class="sxs-lookup"><span data-stu-id="43400-119">Click Create lines.</span></span>
5. <span data-ttu-id="43400-120">Geben Sie in das Feld "Von Datum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="43400-120">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="43400-121">Legen Sie das Datum auf "02.01.2015" fest.</span><span class="sxs-lookup"><span data-stu-id="43400-121">Set the date to '2015-01-02'.</span></span>  
6. <span data-ttu-id="43400-122">Geben Sie in das Feld "Bis Datum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="43400-122">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="43400-123">Legen Sie das Datum auf "30.12.2015" fest.</span><span class="sxs-lookup"><span data-stu-id="43400-123">Set the date to '2015-12-30'.</span></span>  
7. <span data-ttu-id="43400-124">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="43400-124">Click OK.</span></span>
    * <span data-ttu-id="43400-125">Dadurch werden Positionen für Dimensionen erstellt, die Bestandstransaktionen haben.</span><span class="sxs-lookup"><span data-stu-id="43400-125">This will create lines for the dimensions that have inventory transactions.</span></span>  

## <a name="calculate-proposal"></a><span data-ttu-id="43400-126">Vorschlag ermitteln</span><span class="sxs-lookup"><span data-stu-id="43400-126">Calculate proposal</span></span>
1. <span data-ttu-id="43400-127">Klicken Sie auf "Vorschlag berechnen".</span><span class="sxs-lookup"><span data-stu-id="43400-127">Click Calculate proposal.</span></span>
2. <span data-ttu-id="43400-128">Wählen Sie die Option "Durchschnittliche Abgänge während Lieferzeit verwenden".</span><span class="sxs-lookup"><span data-stu-id="43400-128">Select the Use average issue during lead time option.</span></span>
3. <span data-ttu-id="43400-129">Legen Sie den Multiplikationsfaktor auf "10" fest.</span><span class="sxs-lookup"><span data-stu-id="43400-129">Set Multiplication factor to '10'.</span></span>
    * <span data-ttu-id="43400-130">Der Faktor "Multiplizieren" wird verwendet, um den Vorschlag anzupassen.</span><span class="sxs-lookup"><span data-stu-id="43400-130">The Multiply factor is used to adjust the proposal.</span></span> <span data-ttu-id="43400-131">Weil Demodaten nur einige, wenige Transaktionen haben, müssen Sie den Faktor festlegen, um einen realistischen Vorschlag zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="43400-131">Because demo data only has a few transactions, you will need to set the factor to get a realistic proposal.</span></span>  
4. <span data-ttu-id="43400-132">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="43400-132">Click OK.</span></span>
    * <span data-ttu-id="43400-133">Führen Sie einen Bildlauf nach unten durch, um M0002 und M0003 zu suchen.</span><span class="sxs-lookup"><span data-stu-id="43400-133">Scroll down to find M0002 and M0003.</span></span> <span data-ttu-id="43400-134">Zeigen Sie die Spalte "Berechnete Mindestmenge" an.</span><span class="sxs-lookup"><span data-stu-id="43400-134">View the Calculated minimum quantity column.</span></span>   

## <a name="update-minimum-quantity"></a><span data-ttu-id="43400-135">Mindestmenge aktualisieren</span><span class="sxs-lookup"><span data-stu-id="43400-135">Update minimum quantity</span></span>
1. <span data-ttu-id="43400-136">Geben Sie im Feld "Neue Mindestmenge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="43400-136">In the New minimum quantity field, enter a number.</span></span>
    * <span data-ttu-id="43400-137">Aktualisieren Sie die "Neue Mindestmenge", damit sie dem Wert in der "Berechneten Mindestmenge" entspricht.</span><span class="sxs-lookup"><span data-stu-id="43400-137">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="43400-138">Wenn das "Berechnete Minimum" null ist, können Sie den gewünschten zukünftigen Wert eingeben.</span><span class="sxs-lookup"><span data-stu-id="43400-138">If the Calculated minimum is zero,  you can enter the desired future value.</span></span> <span data-ttu-id="43400-139">Zum Beispiel können Sie die "Berechnete Mindestmenge" in diesem Feld für M0002 eingeben, die den Lagerort 12 hat.</span><span class="sxs-lookup"><span data-stu-id="43400-139">For example, you can enter the Calculated minimum quantity in this field for M0002 that has warehouse 12.</span></span>  
2. <span data-ttu-id="43400-140">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="43400-140">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="43400-141">Zum Beispiel können Sie M0002 auswählen, der Lagerort 12 hat.</span><span class="sxs-lookup"><span data-stu-id="43400-141">For example, you can select M0002 that has warehouse 12.</span></span>  
3. <span data-ttu-id="43400-142">Geben Sie im Feld "Neue Mindestmenge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="43400-142">In the New minimum quantity field, enter a number.</span></span>
    * <span data-ttu-id="43400-143">Aktualisieren Sie die "Neue Mindestmenge", damit sie dem Wert in der "Berechneten Mindestmenge" entspricht.</span><span class="sxs-lookup"><span data-stu-id="43400-143">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="43400-144">Wenn das "Berechnete Minimum" null ist, können Sie den gewünschten zukünftigen Wert eingeben.</span><span class="sxs-lookup"><span data-stu-id="43400-144">If the Calculated minimum is zero you can enter the desired future value.</span></span>  

## <a name="post-the-new-minimum-quantity-and-validate-the-result"></a><span data-ttu-id="43400-145">Buchen Sie die neue Mindestmenge und überprüfen Sie das Ergebnis</span><span class="sxs-lookup"><span data-stu-id="43400-145">Post the new minimum quantity and validate the result</span></span>
1. <span data-ttu-id="43400-146">Klicken Sie auf "Buchen".</span><span class="sxs-lookup"><span data-stu-id="43400-146">Click Post.</span></span>
2. <span data-ttu-id="43400-147">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="43400-147">Click OK.</span></span>
3. <span data-ttu-id="43400-148">Klicken Sie, um dem Link im Feld "Artikelnummer" zu folgen.</span><span class="sxs-lookup"><span data-stu-id="43400-148">Click to follow the link in the Item number field.</span></span>
4. <span data-ttu-id="43400-149">Klicken Sie, um dem Link im Feld "Artikelnummer" zu folgen.</span><span class="sxs-lookup"><span data-stu-id="43400-149">Click to follow the link in the Item number field.</span></span>
5. <span data-ttu-id="43400-150">Klicken Sie im Aktivitätsbereich auf "Plan".</span><span class="sxs-lookup"><span data-stu-id="43400-150">On the Action Pane, click Plan.</span></span>
6. <span data-ttu-id="43400-151">Klicken Sie auf "Artikeldeckung".</span><span class="sxs-lookup"><span data-stu-id="43400-151">Click Item coverage.</span></span>
    * <span data-ttu-id="43400-152">Beachten Sie, dass die "Mindestmenge" mit der neuen Mindestmenge aus der Sicherheitsbestandserfassung aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="43400-152">Notice that the Minimum quantity has been updated with the new minimum quantity from the safety stock journal.</span></span>  

