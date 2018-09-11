--- 
title: "Richtlinien für Beschaffungskategoriehierarchien einrichten"
description: Verwenden Sie dieses Verfahren, um Regeln zum Bestellen von Produkten in einer Kategorie einzurichten.
author: mkirknel
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysPolicyListPage, SysPolicy, ProcCategoryAccessPolicyRule, ProcCategoryPolicyRule, EcoResCategorySingleLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 1c5e4b70897af5e45350d1b3766fc1d303a36ea1
ms.contentlocale: de-de
ms.lasthandoff: 09/11/2018

---
# <a name="set-up-policies-for-procurement-category-hierarchies"></a><span data-ttu-id="d9c96-103">Richtlinien für Beschaffungskategoriehierarchien einrichten</span><span class="sxs-lookup"><span data-stu-id="d9c96-103">Set up policies for procurement category hierarchies</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d9c96-104">Verwenden Sie dieses Verfahren, um Regeln zum Bestellen von Produkten in einer Kategorie einzurichten.</span><span class="sxs-lookup"><span data-stu-id="d9c96-104">Use this procedure to set up rules for ordering products in a category.</span></span> <span data-ttu-id="d9c96-105">Die Regeln werden für eine bestimmte Einkaufsrichtlinie definiert.</span><span class="sxs-lookup"><span data-stu-id="d9c96-105">The rules are defined for a specific purchasing policy.</span></span> <span data-ttu-id="d9c96-106">Die Kategoriezugriffsregel steuert, auf welche Beschaffungskategorien Mitarbeiter Zugriff haben, wenn sie eine Anforderung erstellen.</span><span class="sxs-lookup"><span data-stu-id="d9c96-106">The category access rule controls which procurement categories employees have access to when they create a requisition.</span></span> <span data-ttu-id="d9c96-107">Wenn eine Anforderung erstellt wird, werden die Einkaufsrichtlinie und Kategoriezugriffsregel, die angewendet werden sollten, durch die juristische Person und die Organisationseinheit bestimmt, der der Mitarbeiter angehört.</span><span class="sxs-lookup"><span data-stu-id="d9c96-107">When a requisition is being created, the purchasing policy and category access rule that should be applied are determined by the legal entity and the operational unit that the employee belongs to.</span></span> <span data-ttu-id="d9c96-108">Sie können diese Prozedur im Demodatunternehmen USMF verwenden.</span><span class="sxs-lookup"><span data-stu-id="d9c96-108">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="d9c96-109">In der Regel wird diese Aufgabe von einem Einkaufsleiter ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d9c96-109">This task would typically be carried out by a purchasing manager.</span></span>


## <a name="find-the-procurement-policy"></a><span data-ttu-id="d9c96-110">Die Beschaffungsrichtlinie suchen</span><span class="sxs-lookup"><span data-stu-id="d9c96-110">Find the procurement policy</span></span>
1. <span data-ttu-id="d9c96-111">Wechseln Sie zu Beschaffung > Einstellungen > Richtlinien > Beschaffungsrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="d9c96-111">Go to Procurement and sourcing > Setup > Policies > Purchasing policies.</span></span>
2. <span data-ttu-id="d9c96-112">Klicken Sie auf den Link auf der USMF-Richtlinie "Beschaffungsrichtlinie".</span><span class="sxs-lookup"><span data-stu-id="d9c96-112">Click the link on the Procurement Policy USMF policy.</span></span>
    * <span data-ttu-id="d9c96-113">Dies ist die Richtlinie, zu der Sie eine Regel hinzufügen werden.</span><span class="sxs-lookup"><span data-stu-id="d9c96-113">This is the policy that you’ll add a rule to.</span></span> <span data-ttu-id="d9c96-114">Es muss eine aktive Richtlinie sein.</span><span class="sxs-lookup"><span data-stu-id="d9c96-114">It must be an Active policy.</span></span>  

## <a name="create-a-category-access-rule"></a><span data-ttu-id="d9c96-115">Erstellen einer Kategoriezugriffsregel</span><span class="sxs-lookup"><span data-stu-id="d9c96-115">Create a category access rule</span></span>
1. <span data-ttu-id="d9c96-116">Wählen Sie die Kategoriezugriffs-Richtlinienregel aus.</span><span class="sxs-lookup"><span data-stu-id="d9c96-116">Select the Category access policy rule.</span></span>
    * <span data-ttu-id="d9c96-117">Wenn die Schaltfläche "Richtlinienregel erstellen" ausgegraut ist, liegt das daran, dass bereits eine aktive Richtlinienregel für den Kategoriezugriff vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="d9c96-117">If the Create policy rule button is dimmed, it’s because there’s already an active policy rule for Category access.</span></span> <span data-ttu-id="d9c96-118">Überprüfen Sie die Felder "Gültigkeit" und "Ablaufdatum", um zu bestimmen, welches es ist und wählen Sie es dann aus und klicken Sie auf "Richtlinienregel außer Kraft setzen".</span><span class="sxs-lookup"><span data-stu-id="d9c96-118">Check the Effective and Expiration date fields to determine which it is, then select it, and click Retire policy rule.</span></span> <span data-ttu-id="d9c96-119">Wenn die Schaltfläche "Richtlinienregel erstellen" verfügbar ist, müssen Sie nichts unternehmen.</span><span class="sxs-lookup"><span data-stu-id="d9c96-119">If the Create policy rule button is available, you don’t need to do anything.</span></span>  
2. <span data-ttu-id="d9c96-120">Klicken Sie auf "Richtlinienregel erstellen".</span><span class="sxs-lookup"><span data-stu-id="d9c96-120">Click Create policy rule.</span></span>
3. <span data-ttu-id="d9c96-121">Geben Sie im Feld "Gültigkeitsdatum" ein Datum und eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="d9c96-121">In the Effective date field, enter a date and time.</span></span>
    * <span data-ttu-id="d9c96-122">Die Zeit darf sich nicht mit einer anderen Regel überschneiden, die bereits aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="d9c96-122">The time must not overlap with another rule that’s already active.</span></span>  
    * <span data-ttu-id="d9c96-123">Wählen Sie eine Kategorie aus, für die die Regel gilt.</span><span class="sxs-lookup"><span data-stu-id="d9c96-123">Select a category that the rule will apply to.</span></span> <span data-ttu-id="d9c96-124">Notieren Sie sich, welche Kategorie das ist – Sie benötigen sie später.</span><span class="sxs-lookup"><span data-stu-id="d9c96-124">Make a note of which category this is – you’ll need it later.</span></span> <span data-ttu-id="d9c96-125">Wenn Sie eine Kategorie auswählen, werden ihre übergeordnete(n) Kategorie(n) ebenfalls der Liste "Ausgewählte Kategorien" hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d9c96-125">When you select a category, its parent category or categories will also be added to the Selected categories list.</span></span>  
    * <span data-ttu-id="d9c96-126">Wenn Sie möchten, dass die Regel für alle Unterkategorien der ausgewählten Kategorie gilt, aktivieren Sie das Kontrollkästchen "Unterkategorien einschließen".</span><span class="sxs-lookup"><span data-stu-id="d9c96-126">If you want the rule to apply to all subcategories of the selected category, select the Include subcategories check box.</span></span>  
4. <span data-ttu-id="d9c96-127">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d9c96-127">Click Add.</span></span>
    * <span data-ttu-id="d9c96-128">Wenn Sie die Option "Übergeordnete Regel einschließen" auf "Ja" festlegen, wird die Richtlinienregel, die Sie für eine übergeordnete Kategorie definieren, ebenfalls deren untergeordneten Kategorien zugewiesen, wenn für die untergeordneten Kategorien keine Richtlinienregel definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="d9c96-128">If you set the Include parent rule option to Yes, the policy rule that you define for a parent category is also assigned to its child categories, if no policy rule has been defined for the child categories.</span></span>  
5. <span data-ttu-id="d9c96-129">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="d9c96-129">Click OK.</span></span>

## <a name="create-a-category-policy-rule"></a><span data-ttu-id="d9c96-130">Erstellen einer Kategorierichtlinienregel</span><span class="sxs-lookup"><span data-stu-id="d9c96-130">Create a category policy rule</span></span>
1. <span data-ttu-id="d9c96-131">Die Kategorierichtlinienregel auswählen</span><span class="sxs-lookup"><span data-stu-id="d9c96-131">Select the Category policy rule</span></span>
    * <span data-ttu-id="d9c96-132">Wenn die Schaltfläche "Richtlinienregel erstellen" ausgegraut ist, wählen Sie die aktive Richtlinienregel aus und klicken Sie dann auf "Richtlinienregel außer Kraft setzen".</span><span class="sxs-lookup"><span data-stu-id="d9c96-132">If the Create policy rule button is dimmed, select the active policy rule, and then click Retire policy rule.</span></span>  
2. <span data-ttu-id="d9c96-133">Klicken Sie auf "Richtlinienregel erstellen".</span><span class="sxs-lookup"><span data-stu-id="d9c96-133">Click Create policy rule.</span></span>
3. <span data-ttu-id="d9c96-134">Geben Sie im Feld "Gültigkeitsdatum" ein Datum und eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="d9c96-134">In the Effective date field, enter a date and time.</span></span>
4. <span data-ttu-id="d9c96-135">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d9c96-135">Click Add.</span></span>
5. <span data-ttu-id="d9c96-136">Wählen Sie dieselbe Kategorie aus, die Sie für die "Kategoriezugriffsregel" verwendeten.</span><span class="sxs-lookup"><span data-stu-id="d9c96-136">Select the same category that you used for the Category access rule.</span></span>
6. <span data-ttu-id="d9c96-137">Wählen Sie im Feld "Kreditorenauswahl" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="d9c96-137">In the Vendor selection field, select an option.</span></span>
    * <span data-ttu-id="d9c96-138">Wählen Sie eine Regel aus, um zu steuern, welche Art von Kreditoren für die Kategorie ausgewählt werden können, wenn Anforderungen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d9c96-138">Select a rule to control which kind of vendors can be selected for the category when requisitions are created.</span></span>  
7. <span data-ttu-id="d9c96-139">Klicken Sie auf "Schließen".</span><span class="sxs-lookup"><span data-stu-id="d9c96-139">Click Close.</span></span>
    * <span data-ttu-id="d9c96-140">Die Richtlinienregeln, die Sie definiert haben, sind für die Anforderungen des Typs "Verbrauch" gewesen.</span><span class="sxs-lookup"><span data-stu-id="d9c96-140">The policy rules that you have defined have been for requisitions of type Consumption.</span></span> <span data-ttu-id="d9c96-141">Sollten Sie Richtlinien für Anforderungen des Typs "Wiederbeschaffung" definieren wollen, würden Sie eine Regel für den Richtlinienregeltyp mit der Bezeichnung "Wiederbeschaffungskategorie-Zugriffsrichtlinienregel" erstellen.</span><span class="sxs-lookup"><span data-stu-id="d9c96-141">If you wanted to define policies for requisitions of type Replenishment, you would create a rule for the Policy rule type called “Replenishment category access policy rule”.</span></span>  


