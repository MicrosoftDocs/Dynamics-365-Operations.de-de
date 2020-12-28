---
title: Sicherheitsbestandserfassung verwenden, um die Mindestdeckung zu aktualisieren
description: Diese Prozedur zeigt, wie man die Vorschläge zur Mindestdeckung berechnet, basierend auf früheren Transaktionen, und dann die Artikeldeckung mit dem Vorschlag aktualisiert.
author: ChristianRytt
manager: tfehr
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0d69daf3d307ba72ff6017d91849e3d22bd0bd85
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428933"
---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage"></a><span data-ttu-id="cf97b-103">Sicherheitsbestandserfassung verwenden, um die Mindestdeckung zu aktualisieren</span><span class="sxs-lookup"><span data-stu-id="cf97b-103">Use the safety stock journal to update minimum coverage</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cf97b-104">Diese Prozedur zeigt, wie man die Vorschläge zur Mindestdeckung berechnet, basierend auf früheren Transaktionen, und dann die Artikeldeckung mit dem Vorschlag aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="cf97b-104">This procedure shows how to calculate minimum coverage proposals based on historical transactions and then update the item coverage with the proposals.</span></span> <span data-ttu-id="cf97b-105">Dieses wird unter Verwendung der Sicherheitsbestandserfassung getan.</span><span class="sxs-lookup"><span data-stu-id="cf97b-105">This is done using the safety stock journal.</span></span> <span data-ttu-id="cf97b-106">Das Demodatenunternehmen, das verwendet wird, um diese Aufgabe zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="cf97b-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="cf97b-107">Diese Aufgabe ist für den Produktionsplaner bestimmt, um mithilfe davon die Mindestdeckung beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="cf97b-107">This task is intended for the production planner, to help maintain minimum coverage.</span></span>


## <a name="create-a-new-safety-stock-journal-name"></a><span data-ttu-id="cf97b-108">Einen neuen Sicherheitsbestands-Erfassungsname erstellen</span><span class="sxs-lookup"><span data-stu-id="cf97b-108">Create a new safety stock journal name</span></span>
1. <span data-ttu-id="cf97b-109">Gehen Sie im Navigationsbereich **Navigationsbereich** zu **Masterplanung > Einrichten > Sicherheitsbestand Journalnamen**.</span><span class="sxs-lookup"><span data-stu-id="cf97b-109">In the **Navigation pane**, go to **Master planning > Setup > Safety stock journal names**.</span></span>
2. <span data-ttu-id="cf97b-110">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="cf97b-110">Click **New**.</span></span>
3. <span data-ttu-id="cf97b-111">Geben Sie im Feld **Name** den Text'Material' ein.</span><span class="sxs-lookup"><span data-stu-id="cf97b-111">In the **Name** field, type 'Material'.</span></span>
4. <span data-ttu-id="cf97b-112">Geben Sie im Feld **Beschreibung** den Text'Material' ein.</span><span class="sxs-lookup"><span data-stu-id="cf97b-112">In the **Description** field, type 'Material'.</span></span>
5. <span data-ttu-id="cf97b-113">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="cf97b-113">Close the page.</span></span>

## <a name="create-a-safety-stock-journal"></a><span data-ttu-id="cf97b-114">Eine Sicherheitsbestandserfassung erstellen</span><span class="sxs-lookup"><span data-stu-id="cf97b-114">Create a safety stock journal</span></span>
1. <span data-ttu-id="cf97b-115">Gehen Sie im Navigationsbereich **Navigationsbereich** zu **Masterplanung > Masterplanung > Ausführen > Sicherheitsbestandsberechnung**.</span><span class="sxs-lookup"><span data-stu-id="cf97b-115">In the **Navigation pane**, go to **Master planning > Master planning > Run > Safety stock calculation**.</span></span>
2. <span data-ttu-id="cf97b-116">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="cf97b-116">Click **New**.</span></span>
3. <span data-ttu-id="cf97b-117">Geben Sie im Feld **Name** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="cf97b-117">In the **Name** field, enter or select a value.</span></span> <span data-ttu-id="cf97b-118">Wählen Sie den Sicherheitsbestands-Erfassungsname aus, den Sie erstellt haben, zum Beispiel "Material".</span><span class="sxs-lookup"><span data-stu-id="cf97b-118">Select the safety stock journal name that you created, for example, Material.</span></span>  
4. <span data-ttu-id="cf97b-119">Klicken Sie auf **Zeilen erstellen**.</span><span class="sxs-lookup"><span data-stu-id="cf97b-119">Click **Create lines**.</span></span>
5. <span data-ttu-id="cf97b-120">Geben Sie im Feld **Von Datum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="cf97b-120">In the **From date** field, enter a date.</span></span>  
6. <span data-ttu-id="cf97b-121">Geben Sie im Feld **Bis Datum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="cf97b-121">In the **To date** field, enter a date.</span></span>
7. <span data-ttu-id="cf97b-122">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="cf97b-122">Click **OK**.</span></span> <span data-ttu-id="cf97b-123">Dadurch werden Positionen für Dimensionen erstellt, die Bestandstransaktionen haben.</span><span class="sxs-lookup"><span data-stu-id="cf97b-123">This will create lines for the dimensions that have inventory transactions.</span></span>  

## <a name="calculate-proposal"></a><span data-ttu-id="cf97b-124">Vorschlag ermitteln</span><span class="sxs-lookup"><span data-stu-id="cf97b-124">Calculate proposal</span></span>
1. <span data-ttu-id="cf97b-125">Klicken Sie auf **Angebotsberechnung**.</span><span class="sxs-lookup"><span data-stu-id="cf97b-125">Click **Calculate proposal**.</span></span>
2. <span data-ttu-id="cf97b-126">Wählen Sie die Option **Durchschnittliches Problem während der Vorlaufzeit** verwenden.</span><span class="sxs-lookup"><span data-stu-id="cf97b-126">Select the **Use average issue during lead time** option.</span></span>
3. <span data-ttu-id="cf97b-127">Setzen Sie **Multiplikationsfaktor** auf '10'.</span><span class="sxs-lookup"><span data-stu-id="cf97b-127">Set **Multiplication factor** to '10'.</span></span> <span data-ttu-id="cf97b-128">Der Faktor "Multiplizieren" wird verwendet, um den Vorschlag anzupassen.</span><span class="sxs-lookup"><span data-stu-id="cf97b-128">The Multiply factor is used to adjust the proposal.</span></span> <span data-ttu-id="cf97b-129">Weil Demodaten nur einige, wenige Transaktionen haben, müssen Sie den Faktor festlegen, um einen realistischen Vorschlag zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="cf97b-129">Because demo data only has a few transactions, you will need to set the factor to get a realistic proposal.</span></span>  
4. <span data-ttu-id="cf97b-130">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="cf97b-130">Click **OK**.</span></span> <span data-ttu-id="cf97b-131">Führen Sie einen Bildlauf nach unten durch, um M0002 und M0003 zu suchen.</span><span class="sxs-lookup"><span data-stu-id="cf97b-131">Scroll down to find M0002 and M0003.</span></span> <span data-ttu-id="cf97b-132">Betrachten Sie die Spalte **Berechnetes Minimum** Menge.</span><span class="sxs-lookup"><span data-stu-id="cf97b-132">View the **Calculated minimum** quantity column.</span></span>   

## <a name="update-minimum-quantity"></a><span data-ttu-id="cf97b-133">Mindestmenge aktualisieren</span><span class="sxs-lookup"><span data-stu-id="cf97b-133">Update minimum quantity</span></span>
1. <span data-ttu-id="cf97b-134">Geben Sie im Feld **Neue Mindestmenge** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="cf97b-134">In the **New minimum quantity** field, enter a number.</span></span> <span data-ttu-id="cf97b-135">Aktualisieren Sie die "Neue Mindestmenge", damit sie dem Wert in der "Berechneten Mindestmenge" entspricht.</span><span class="sxs-lookup"><span data-stu-id="cf97b-135">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="cf97b-136">Wenn das "Berechnete Minimum" null ist, können Sie den gewünschten zukünftigen Wert eingeben.</span><span class="sxs-lookup"><span data-stu-id="cf97b-136">If the Calculated minimum is zero,  you can enter the desired future value.</span></span> <span data-ttu-id="cf97b-137">Zum Beispiel können Sie die "Berechnete Mindestmenge" in diesem Feld für M0002 eingeben, die den Lagerort 12 hat.</span><span class="sxs-lookup"><span data-stu-id="cf97b-137">For example, you can enter the Calculated minimum quantity in this field for M0002 that has warehouse 12.</span></span>  
2. <span data-ttu-id="cf97b-138">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="cf97b-138">In the list, find and select the desired record.</span></span> <span data-ttu-id="cf97b-139">Zum Beispiel können Sie M0002 auswählen, der Lagerort 12 hat.</span><span class="sxs-lookup"><span data-stu-id="cf97b-139">For example, you can select M0002 that has warehouse 12.</span></span>  
3. <span data-ttu-id="cf97b-140">Geben Sie im Feld **Neue Mindestmenge** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="cf97b-140">In the **New minimum quantity** field, enter a number.</span></span> <span data-ttu-id="cf97b-141">Aktualisieren Sie die "Neue Mindestmenge", damit sie dem Wert in der "Berechneten Mindestmenge" entspricht.</span><span class="sxs-lookup"><span data-stu-id="cf97b-141">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="cf97b-142">Wenn das "Berechnete Minimum" null ist, können Sie den gewünschten zukünftigen Wert eingeben.</span><span class="sxs-lookup"><span data-stu-id="cf97b-142">If the Calculated minimum is zero you can enter the desired future value.</span></span>  

## <a name="post-the-new-minimum-quantity-and-validate-the-result"></a><span data-ttu-id="cf97b-143">Buchen Sie die neue Mindestmenge und überprüfen Sie das Ergebnis</span><span class="sxs-lookup"><span data-stu-id="cf97b-143">Post the new minimum quantity and validate the result</span></span>
1. <span data-ttu-id="cf97b-144">Klicken Sie auf **Buchen**.</span><span class="sxs-lookup"><span data-stu-id="cf97b-144">Click **Post**.</span></span>
2. <span data-ttu-id="cf97b-145">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="cf97b-145">Click **OK**.</span></span>
3. <span data-ttu-id="cf97b-146">Klicken Sie hier, um dem Link im Feld **Artikelnummer** zu folgen.</span><span class="sxs-lookup"><span data-stu-id="cf97b-146">Click to follow the link in the **Item number** field.</span></span>
4. <span data-ttu-id="cf97b-147">Klicken Sie hier, um dem Link im Feld **Artikelnummer** zu folgen.</span><span class="sxs-lookup"><span data-stu-id="cf97b-147">Click to follow the link in the **Item number** field.</span></span>
5. <span data-ttu-id="cf97b-148">Klicken Sie im Aktionsbereich **Action Pane** auf Plan.</span><span class="sxs-lookup"><span data-stu-id="cf97b-148">On the **Action Pane**, click Plan.</span></span>
6. <span data-ttu-id="cf97b-149">Klicken Sie auf **Einzelteilabdeckung**.</span><span class="sxs-lookup"><span data-stu-id="cf97b-149">Click **Item coverage**.</span></span> <span data-ttu-id="cf97b-150">Beachten Sie, dass die **Mindestmenge** mit der neuen Mindestmenge aus dem Sicherheitsbestandsjournal aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="cf97b-150">Notice that the **Minimum quantity** has been updated with the new minimum quantity from the safety stock journal.</span></span>  

