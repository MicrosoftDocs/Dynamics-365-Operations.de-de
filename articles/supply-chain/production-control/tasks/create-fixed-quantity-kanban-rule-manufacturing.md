---
title: Kanban-Regel für feste Mengen für die Fertigung erstellen
description: Ziel dieser Prozedur ist es, eine notwendige Einstellung für eine feste Fertigungs-Kanban-Regel zum Starten von Umwandlungsaktivitäten in einer Arbeitsgruppe einer kleinen Umgebung zu erstellen.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, UnitOfMeasureLookup, KanbanCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: af912ecfb07a7af2f299e354243ba0d80c063a9e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981305"
---
# <a name="create-a-fixed-quantity-kanban-rule-for-manufacturing"></a><span data-ttu-id="7b3f1-103">Kanban-Regel für feste Mengen für die Fertigung erstellen</span><span class="sxs-lookup"><span data-stu-id="7b3f1-103">Create a fixed quantity kanban rule for manufacturing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7b3f1-104">Ziel dieser Prozedur ist es, eine notwendige Einstellung für eine feste Fertigungs-Kanban-Regel zum Starten von Umwandlungsaktivitäten in einer Arbeitsgruppe einer kleinen Umgebung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7b3f1-104">This procedure focuses on the setup needed to create a fixed manufacturing kanban rule for triggering transforming activities, at a work cell, in a lean environment.</span></span> <span data-ttu-id="7b3f1-105">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="7b3f1-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="7b3f1-106">Diese Vorgehensweise ist für den Verfahrenstechniker oder den Wertstrom-Manager vorgesehen, da dieser die Produktion eines neuen oder geänderten Produkts vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="7b3f1-106">This procedure is intended for the Process Engineer or the Value Stream Manager, as they prepare production of a new or modified product.</span></span>


## <a name="create-new-kanban-rule"></a><span data-ttu-id="7b3f1-107">Neue Kanban-Regel erstellen</span><span class="sxs-lookup"><span data-stu-id="7b3f1-107">Create new kanban rule</span></span>
1. <span data-ttu-id="7b3f1-108">Wechseln Sie zu Kanban-Regeln.</span><span class="sxs-lookup"><span data-stu-id="7b3f1-108">Go to Kanban rules.</span></span>
2. <span data-ttu-id="7b3f1-109">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="7b3f1-109">Click New.</span></span>
    * <span data-ttu-id="7b3f1-110">Beachten Sie, dass der Standardtyp "Manufacturing und Auffüllungsstrategie sind festgelegt" ist.</span><span class="sxs-lookup"><span data-stu-id="7b3f1-110">Notice that the default Type is Manufacturing and Replenishment strategy is Fixed.</span></span> <span data-ttu-id="7b3f1-111">Sie müssen diese Parameter nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="7b3f1-111">You do not have to change these parameters.</span></span>  
3. <span data-ttu-id="7b3f1-112">Geben Sie im Feld "Erste Planaktivität" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="7b3f1-112">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="7b3f1-113">Dies ist die Aktivität, die für die Kanbans ausgeführt wird, die auf dieser Kanban-Regel erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="7b3f1-113">This is the activity that will be performed for kanbans created based on this kanban rule.</span></span>  <span data-ttu-id="7b3f1-114">Wählen Sie "SpeakerTestAndPackaging" aus.</span><span class="sxs-lookup"><span data-stu-id="7b3f1-114">Select 'SpeakerTestAndPackaging'.</span></span>  
4. <span data-ttu-id="7b3f1-115">Erweitern Sie den Abschnitt "Details".</span><span class="sxs-lookup"><span data-stu-id="7b3f1-115">Expand the Details section.</span></span>
5. <span data-ttu-id="7b3f1-116">Geben Sie im Feld "Produkt" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="7b3f1-116">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="7b3f1-117">Wählen Sie L0050 aus.</span><span class="sxs-lookup"><span data-stu-id="7b3f1-117">Select L0050.</span></span>  
6. <span data-ttu-id="7b3f1-118">Geben Sie im Feld "Maßeinheit" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="7b3f1-118">In the Unit of measure field, enter or select a value.</span></span>
    * <span data-ttu-id="7b3f1-119">Wählen Sie Minuten aus.</span><span class="sxs-lookup"><span data-stu-id="7b3f1-119">Select minutes.</span></span>  
7. <span data-ttu-id="7b3f1-120">Geben Sie im Feld "Lieferzeit" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="7b3f1-120">In the Lead time field, enter a number.</span></span>
    * <span data-ttu-id="7b3f1-121">Geben Sie "5" ein.</span><span class="sxs-lookup"><span data-stu-id="7b3f1-121">Enter 5.</span></span>  

## <a name="set-quantities"></a><span data-ttu-id="7b3f1-122">Mengen festlegen</span><span class="sxs-lookup"><span data-stu-id="7b3f1-122">Set quantities</span></span>
1. <span data-ttu-id="7b3f1-123">Erweitern Sie den Abschnitt "Mengen".</span><span class="sxs-lookup"><span data-stu-id="7b3f1-123">Expand the Quantities section.</span></span>
2. <span data-ttu-id="7b3f1-124">Legen Sie "Standardmenge" auf "10" fest.</span><span class="sxs-lookup"><span data-stu-id="7b3f1-124">Set Default quantity to '10'.</span></span>
    * <span data-ttu-id="7b3f1-125">Dies ist die Menge, die für jeden Kanban übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="7b3f1-125">This is the quantity that will be transferred for each kanban.</span></span>  
3. <span data-ttu-id="7b3f1-126">Aktivieren Sie das Kontrollkästchen "Abweichung der Produktmenge".</span><span class="sxs-lookup"><span data-stu-id="7b3f1-126">Select the Product quantity variance check box.</span></span>
    * <span data-ttu-id="7b3f1-127">Hiermit können ausgewählte Kanbans mit einer Abweichung von der Standardmenge abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="7b3f1-127">With this, selected kanbans can be completed with a variance from the default quantity.</span></span>  <span data-ttu-id="7b3f1-128">Um Kanbans einen Abschluss mit einer Menge von 8 bis 12 zu ermöglichen, legen Sie beide Abweichungen auf 2 fest.</span><span class="sxs-lookup"><span data-stu-id="7b3f1-128">To allow kanbans to be completed with a quantity from 8 to 12, set both variances to 2.</span></span>  
4. <span data-ttu-id="7b3f1-129">Legen Sie "Abweichung unter" auf '2' fest.</span><span class="sxs-lookup"><span data-stu-id="7b3f1-129">Set Variance below to '2'.</span></span>
    * <span data-ttu-id="7b3f1-130">Dies ermöglicht einen Abschluss nach unten bis 10 - 2 = 8</span><span class="sxs-lookup"><span data-stu-id="7b3f1-130">This will allow completing down to 10 - 2 = 8</span></span>  
5. <span data-ttu-id="7b3f1-131">Legen Sie "Abweichung über" auf '2' fest.</span><span class="sxs-lookup"><span data-stu-id="7b3f1-131">Set Variance above to '2'.</span></span>
    * <span data-ttu-id="7b3f1-132">Dies ermöglicht einen Abschluss nach oben bis 10 + 2 = 12</span><span class="sxs-lookup"><span data-stu-id="7b3f1-132">This will allow completing up to 10 + 2 = 12</span></span>  
6. <span data-ttu-id="7b3f1-133">Geben Sie im Feld "Feste Kanban-Menge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="7b3f1-133">In the Fixed kanban quantity field, enter a number.</span></span>
    * <span data-ttu-id="7b3f1-134">Dies ist der Betrag von Kanbans, die aktiv sein sollen.</span><span class="sxs-lookup"><span data-stu-id="7b3f1-134">This is the amount of kanbans that should be active.</span></span> <span data-ttu-id="7b3f1-135">In diesem Fall 5 Kanbans, die je 10 verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="7b3f1-135">In this case, 5 kanbans processing 10 each.</span></span>  
7. <span data-ttu-id="7b3f1-136">Geben Sie im Feld "Min. Warnungsgrenzwert" "2 "ein.</span><span class="sxs-lookup"><span data-stu-id="7b3f1-136">In the Alert boundary minimum field, enter '2'.</span></span>
    * <span data-ttu-id="7b3f1-137">Dies wird verwendet, um die Mindestmenge vollständiger Kanbans zu verfolgen, die am Ziel sein sollen.</span><span class="sxs-lookup"><span data-stu-id="7b3f1-137">Used to keep track of the minimum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="7b3f1-138">Beispielsweise wird dieses in der Kanban-Mengenübersicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="7b3f1-138">For example, this is used on the kanban quantity overview.</span></span>  
8. <span data-ttu-id="7b3f1-139">Geben Sie im Feld "Max. Warnungsgrenzwert" "4 "ein.</span><span class="sxs-lookup"><span data-stu-id="7b3f1-139">In the Alert boundary maximum field, enter '4'.</span></span>
    * <span data-ttu-id="7b3f1-140">Wird verwendet, um die maximale Menge vollständiger Kanbans zu verfolgen, die am Ziel sein sollen.</span><span class="sxs-lookup"><span data-stu-id="7b3f1-140">Used to keep track of the maximum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="7b3f1-141">Beispielsweise wird dieses in der Kanban-Mengenübersicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="7b3f1-141">For example, this is used on the kanban quantity overview.</span></span>  
9. <span data-ttu-id="7b3f1-142">Geben Sie im Feld "Automatische Planungsmenge" "1"ein.</span><span class="sxs-lookup"><span data-stu-id="7b3f1-142">In the Automatic planning quantity field, enter '1'.</span></span>
    * <span data-ttu-id="7b3f1-143">Wenn hier bis 1 festgelegt wird, bedeutet es, dass jeder Kanban automatisch geplant wird.</span><span class="sxs-lookup"><span data-stu-id="7b3f1-143">Setting this to 1 means that every kanban will be automatically planned.</span></span>   <span data-ttu-id="7b3f1-144">Wenn wir 3 eingegeben haben, werden die Kanbans nicht terminiert, bis 3 leere Kanbans für die Planung bereit sind.</span><span class="sxs-lookup"><span data-stu-id="7b3f1-144">If we entered 3, the kanbans would not be planned until 3 empty kanbans are ready for planning.</span></span> <span data-ttu-id="7b3f1-145">Dies ist zum Gruppieren der Arbeit und der Vermeidung zu vieler Einstellungen hilfreich.</span><span class="sxs-lookup"><span data-stu-id="7b3f1-145">This is useful for grouping work and avoiding too much setup.</span></span>  

## <a name="create-kanbans"></a><span data-ttu-id="7b3f1-146">Kanbans erstellen</span><span class="sxs-lookup"><span data-stu-id="7b3f1-146">Create Kanbans</span></span>
1. <span data-ttu-id="7b3f1-147">Erweitern Sie den Abschnitt "Kanbans".</span><span class="sxs-lookup"><span data-stu-id="7b3f1-147">Expand the Kanbans section.</span></span>
2. <span data-ttu-id="7b3f1-148">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="7b3f1-148">Click Save.</span></span>
    * <span data-ttu-id="7b3f1-149">Die Kanban-Regel muss gespeichert werden, bevor Kanbans erstellt werden können.</span><span class="sxs-lookup"><span data-stu-id="7b3f1-149">The kanban rule needs to be saved before kanbans can be created.</span></span>  
3. <span data-ttu-id="7b3f1-150">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="7b3f1-150">Click Add.</span></span>
    * <span data-ttu-id="7b3f1-151">Beachten Sie, dass keine aktiven Kanbans vorhanden, deshalb ist die vorgeschlagenen "Anzahl der neuen Kanbans. 5.</span><span class="sxs-lookup"><span data-stu-id="7b3f1-151">Note that there are no active kanbans, due to this the suggested 'Number of new kanbans' are 5.</span></span> <span data-ttu-id="7b3f1-152">Dies entspricht der "festen Kanban-Menge".</span><span class="sxs-lookup"><span data-stu-id="7b3f1-152">This is equal to the 'Fixed kanban quantity'.</span></span>  
4. <span data-ttu-id="7b3f1-153">Klicken Sie auf "Erstellen".</span><span class="sxs-lookup"><span data-stu-id="7b3f1-153">Click Create.</span></span>
    * <span data-ttu-id="7b3f1-154">Dieses erstellt 5 Kanbans.</span><span class="sxs-lookup"><span data-stu-id="7b3f1-154">This will create 5 kanbans.</span></span>  
    * <span data-ttu-id="7b3f1-155">Beachten Sie, dass 5 Kanbans mit jeweils 10 für diese Kanban-Produktionsregel erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="7b3f1-155">Note that 5 kanbans, for 10 each, was created for this manufacturing kanban rule.</span></span> <span data-ttu-id="7b3f1-156">Dies ist der letzte Schritt in diesem Verfahren.</span><span class="sxs-lookup"><span data-stu-id="7b3f1-156">This is the last step in this procedure.</span></span>  

