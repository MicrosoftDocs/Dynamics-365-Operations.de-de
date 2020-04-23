---
title: Eine Kanban-Regel mithilfe eines Kanban-Positionsereignisses erstellen
description: Diese Prozedur erstellt eine Kanban-Regel mithilfe der Kanban-Positionsereigniseinstellung, um das Ausführen von Pull aus einer Prozessaktivität auszulösen.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5a6c4b7103874a6d955b21e99b8e219a039d4b55
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3212273"
---
# <a name="create-a-kanban-rule-using-a-kanban-line-event"></a><span data-ttu-id="64c94-103">Eine Kanban-Regel mithilfe eines Kanban-Positionsereignisses erstellen</span><span class="sxs-lookup"><span data-stu-id="64c94-103">Create a kanban rule using a kanban line event</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="64c94-104">Diese Prozedur erstellt eine Kanban-Regel mithilfe der Kanban-Positionsereigniseinstellung, um das Ausführen von Pull aus einer Prozessaktivität auszulösen.</span><span class="sxs-lookup"><span data-stu-id="64c94-104">This procedure creates a kanban rule by using the kanban line event setting to trigger pull from a process activity.</span></span> <span data-ttu-id="64c94-105">Die Kanban-Regel wird durch eine Kanban-Prozessaktivität jeweils mit einer Menge gleich oder größer als 25 ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="64c94-105">The kanban rule is triggered by a kanban process activity, with a quantity equal to or greater than 25 each.</span></span> <span data-ttu-id="64c94-106">Das Demodatenunternehmen, das verwendet wird, um diese Aufgabe zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="64c94-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="64c94-107">Diese Aufgabe ist für den Fertigungsplaner oder den Wertstrom-Manager vorgesehen, da diese die Produktion eines neuen oder geänderten Produkts in einer schlanken Umgebung vorbereiten.</span><span class="sxs-lookup"><span data-stu-id="64c94-107">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-kanban-rule"></a><span data-ttu-id="64c94-108">Erstellen einer Kanban-Regel</span><span class="sxs-lookup"><span data-stu-id="64c94-108">Create a kanban rule</span></span>
1. <span data-ttu-id="64c94-109">Wechseln Sie zu "Produktinformationsverwaltung" > "Lean Manufacturing" > "Kanban-Regeln".</span><span class="sxs-lookup"><span data-stu-id="64c94-109">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="64c94-110">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="64c94-110">Click New.</span></span>
3. <span data-ttu-id="64c94-111">Wählen Sie im Feld "Auffüllungsstrategie" "Ereignis" aus.</span><span class="sxs-lookup"><span data-stu-id="64c94-111">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="64c94-112">Dadurch werden Kanbans direkt auf Grundlage des Bedarfs generiert.</span><span class="sxs-lookup"><span data-stu-id="64c94-112">This generates kanbans directly from demand.</span></span> <span data-ttu-id="64c94-113">Dies wird verwendet, um Regeln einzurichten, die ein Auftragsfertigungszenario definieren.</span><span class="sxs-lookup"><span data-stu-id="64c94-113">It is used to set up rules that define a make-to-order scenario.</span></span>  
4. <span data-ttu-id="64c94-114">Geben Sie im Feld "Erste Planaktivität" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="64c94-114">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="64c94-115">Geben Sie "SpeakerAssemblyAndPolish" ein oder wählen Sie es aus.</span><span class="sxs-lookup"><span data-stu-id="64c94-115">Enter or select SpeakerAssemblyAndPolish.</span></span> <span data-ttu-id="64c94-116">Die erste Aktivität einer Kanban-Regel für die Fertigung ist eine Prozessaktivität im Produktionsfluss.</span><span class="sxs-lookup"><span data-stu-id="64c94-116">The first activity of a manufacturing kanban rule is a process activity in the production flow.</span></span> <span data-ttu-id="64c94-117">Wenn Sie die Aktivität auswählen, werden die Gültigkeitsdaten der Aktivität in die Gültigkeitsdaten der Kanban-Regel kopiert.</span><span class="sxs-lookup"><span data-stu-id="64c94-117">When you select the activity, the validity dates of the activity are copied to the validity dates of the kanban rule.</span></span>  
5. <span data-ttu-id="64c94-118">Erweitern Sie den Abschnitt "Details".</span><span class="sxs-lookup"><span data-stu-id="64c94-118">Expand the Details section.</span></span>
6. <span data-ttu-id="64c94-119">Geben Sie im Feld "Produkt" den Wert "L0001" ein.</span><span class="sxs-lookup"><span data-stu-id="64c94-119">In the Product field, type 'L0001'.</span></span>
7. <span data-ttu-id="64c94-120">Erweitern Sie den Abschnitt "Ereignis".</span><span class="sxs-lookup"><span data-stu-id="64c94-120">Expand the Events section.</span></span>
8. <span data-ttu-id="64c94-121">Wählen Sie im Feld "Kanban-Positionsereignis" die Option "Automatisch" aus.</span><span class="sxs-lookup"><span data-stu-id="64c94-121">In the Kanban line event field, select 'Automatic'.</span></span>
    * <span data-ttu-id="64c94-122">Dadurch werden Ereignis-Kanbans bei Bedarf generiert.</span><span class="sxs-lookup"><span data-stu-id="64c94-122">This generates event kanbans on demand.</span></span>  <span data-ttu-id="64c94-123">Dieses Feld wird verwendet, um Kanban-Regeln zu konfigurieren, durch die für eine Downstream-Prozessaktivität erforderliches Material aufgefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="64c94-123">The field is used to configure kanban rules that replenish material that is required for a downstream process activity.</span></span> <span data-ttu-id="64c94-124">Wenn Sie "Automatisch" auswählen, werden die Ereignis-Kanbans mit dem Bedarf erstellt.</span><span class="sxs-lookup"><span data-stu-id="64c94-124">When you select Automatic, the event kanbans are created with the demand.</span></span> <span data-ttu-id="64c94-125">Diese Einstellung wird empfohlen, wenn Sie erwarten, Produktion am gleichen Tag auszuführen.</span><span class="sxs-lookup"><span data-stu-id="64c94-125">This setting is recommended if you expect to execute production on the same day.</span></span>  
9. <span data-ttu-id="64c94-126">Legen Sie die "Mindestmenge für Ereignis" auf '25' fest.</span><span class="sxs-lookup"><span data-stu-id="64c94-126">Set Minimum event quantity to '25'.</span></span>
    * <span data-ttu-id="64c94-127">Ereignis-Kanbans werden generiert, wenn die Bedarfsmenge gleich oder größer als dieses Feld ist.</span><span class="sxs-lookup"><span data-stu-id="64c94-127">Event kanbans are generated when the demand quantity is equal to or more than this field.</span></span> <span data-ttu-id="64c94-128">Dies ist nützlich, wenn Sie eine Auftragsmenge produzieren möchten, die geringer als dieses Feld auf einer Maschine und größer als dieses Feld auf einer anderen Maschine ist.</span><span class="sxs-lookup"><span data-stu-id="64c94-128">This is useful if you want to produce an order quantity less than this field on one machine and more than this field on another machine.</span></span>  
10. <span data-ttu-id="64c94-129">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="64c94-129">Click Save.</span></span>

## <a name="create-sales-order-and-trigger-kanban-chain"></a><span data-ttu-id="64c94-130">Aufträge erstellen und Kanban-Kette auslösen</span><span class="sxs-lookup"><span data-stu-id="64c94-130">Create sales order and trigger kanban chain</span></span>
1. <span data-ttu-id="64c94-131">Wechseln Sie zu "Vertrieb und Marketing" > "Aufträge" > "Alle Aufträge".</span><span class="sxs-lookup"><span data-stu-id="64c94-131">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="64c94-132">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="64c94-132">Click New.</span></span>
3. <span data-ttu-id="64c94-133">Geben Sie im Feld "Debitorenkonto" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="64c94-133">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="64c94-134">Wählen Sie Kundenkonto "US-003, Forest Wholesales" aus.</span><span class="sxs-lookup"><span data-stu-id="64c94-134">Select Customer account US-003, Forest Wholesales.</span></span>  
4. <span data-ttu-id="64c94-135">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="64c94-135">Click OK.</span></span>
5. <span data-ttu-id="64c94-136">Geben Sie im Feld "Artikelnummer" die Zeichenfolge "L0001" ein.</span><span class="sxs-lookup"><span data-stu-id="64c94-136">In the Item number field, type 'L0001'.</span></span>
    * <span data-ttu-id="64c94-137">L0001 ist ein Artikel, für den Sie die Kanban-Regel erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="64c94-137">L0001 is the item for which you created the kanban rule.</span></span>  
6. <span data-ttu-id="64c94-138">Legen Sie die Menge auf "27" fest.</span><span class="sxs-lookup"><span data-stu-id="64c94-138">Set Quantity to '27'.</span></span>
    * <span data-ttu-id="64c94-139">Weil 27 höher als die Mindestmenge von 25 auf der Kanban-Regel ist, löst dies ein Ereignis-Kanban aus.</span><span class="sxs-lookup"><span data-stu-id="64c94-139">Because 27 is higher than the minimum quantity of 25 on the kanban rule, this will trigger an event kanban.</span></span>  
7. <span data-ttu-id="64c94-140">Geben Sie im Feld 'Standort' den Wert '1' ein.</span><span class="sxs-lookup"><span data-stu-id="64c94-140">In the Site field, type '1'.</span></span>
8. <span data-ttu-id="64c94-141">Geben Sie im Feld 'Lagerort' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="64c94-141">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="64c94-142">Wählen Sie Lagerort 13.</span><span class="sxs-lookup"><span data-stu-id="64c94-142">Select warehouse 13.</span></span>  
9. <span data-ttu-id="64c94-143">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="64c94-143">Click Save.</span></span>

## <a name="view-the-kanban-generated-by-the-kanban-rule"></a><span data-ttu-id="64c94-144">Die durch die Kanban-Regel generierte Kanban anzeigen</span><span class="sxs-lookup"><span data-stu-id="64c94-144">View the kanban generated by the kanban rule</span></span>
1. <span data-ttu-id="64c94-145">Wechseln Sie zu "Produktinformationsverwaltung" > "Lean Manufacturing" > "Kanban-Regeln".</span><span class="sxs-lookup"><span data-stu-id="64c94-145">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="64c94-146">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="64c94-146">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="64c94-147">Erweitern Sie den Abschnitt "Kanbans".</span><span class="sxs-lookup"><span data-stu-id="64c94-147">Expand the Kanbans section.</span></span>
    * <span data-ttu-id="64c94-148">Beachten Sie, dass ein Kanban für 27 erstellt wurde, um die Aktivität auf Grundlage der erstellten Kanban-Regel zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="64c94-148">Notice that a kanban for 27 was created to process the  activity based on the created kanban rule.</span></span>  
    * <span data-ttu-id="64c94-149">Dies ist der letzte Schritt.</span><span class="sxs-lookup"><span data-stu-id="64c94-149">This is the last step.</span></span>  

