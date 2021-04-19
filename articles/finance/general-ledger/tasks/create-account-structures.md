---
title: Kontostrukturen erstellen
description: Dieser Aufgabenleitfaden führt Sie durch die Erstellung einer Kontostruktur.
author: aprilolson
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, DimensionCreateAccountStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: aece2b79633802d28ba3b4fd8b51788e26c17a67
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815163"
---
# <a name="create-account-structures"></a><span data-ttu-id="44096-103">Kontostrukturen erstellen</span><span class="sxs-lookup"><span data-stu-id="44096-103">Create account structures</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="44096-104">Dieser Aufgabenleitfaden führt Sie durch die Erstellung einer Kontostruktur.</span><span class="sxs-lookup"><span data-stu-id="44096-104">This task guide steps through creating an account structure.</span></span> <span data-ttu-id="44096-105">Bei den Schritten wird das Demodatunternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="44096-105">The steps use demo data company USMF.</span></span>

1. <span data-ttu-id="44096-106">Gehen Sie zu **Navigationsbereich > Module > Hauptbuch > Kontenplan > Strukturen > Kontostrukturen konfigurieren**.</span><span class="sxs-lookup"><span data-stu-id="44096-106">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Structures > Configure account structures**.</span></span>
2. <span data-ttu-id="44096-107">Klicken Sie im **Aktivitätsbereich** auf **Neu**, um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="44096-107">On the **Action pane**, click **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="44096-108">Im Feld **Kontostruktur** geben Sie einen Namen ein, um den Zweck der Kontostruktur zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="44096-108">In the **Account structure** field, type a name to describe the purpose of the account structure.</span></span>
4. <span data-ttu-id="44096-109">Geben Sie im Feld **Beschreibung** eine Beschreibung ein, um den Zweck der Kontostruktur zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="44096-109">In the **Description** field, type a description to specify the purpose of the account structure.</span></span>
5. <span data-ttu-id="44096-110">Klicken Sie auf **Erstellen**.</span><span class="sxs-lookup"><span data-stu-id="44096-110">Click **Create**.</span></span>
6. <span data-ttu-id="44096-111">Klicken Sie in **Segmente und zulässige Werte** auf **Segment hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="44096-111">In the **Segments and allowed values**, click **Add segment**.</span></span>
7. <span data-ttu-id="44096-112">Wählen Sie in er Liste „Dimensionen“ die Dimension aus, um sie der Kontostruktur hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="44096-112">In the dimensions list, select the dimension to add to the account structure.</span></span>
8. <span data-ttu-id="44096-113">Am Ende der Liste klicken Sie auf **Segment hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="44096-113">At the end of the list, click **Add segment**.</span></span>
9. <span data-ttu-id="44096-114">Wiederholen Sie die Schritte 6 bis 9 nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="44096-114">Repeat step 6 to 9 as needed.</span></span>
10. <span data-ttu-id="44096-115">Wählen Sie im Abschnitt **Details zu zulässigem Wert** das Segment aus, um die zulässigen Werte zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="44096-115">In the **Allowed value details** section, select the segment to edit the allowed values.</span></span>
    <span data-ttu-id="44096-116">Beispielsweise klicken Sie auf das Feld **Hauptkonto**.</span><span class="sxs-lookup"><span data-stu-id="44096-116">For example, click the **Main Account** field.</span></span>  
11. <span data-ttu-id="44096-117">Wählen Sie im Feld **Operator** eine Option aus (z. B. „liegt zwischen“ und „schließt ein“).</span><span class="sxs-lookup"><span data-stu-id="44096-117">In the **Operator** field, select an option, such as is between and includes.</span></span>
12. <span data-ttu-id="44096-118">Geben Sie im Feld **Wert** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="44096-118">In the **Value** field, type a value.</span></span> <span data-ttu-id="44096-119">Beispiel: 600000.</span><span class="sxs-lookup"><span data-stu-id="44096-119">For example, 600000.</span></span>  
13. <span data-ttu-id="44096-120">Geben Sie im Feld **Bis** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="44096-120">In the **through** field, type a value.</span></span> <span data-ttu-id="44096-121">Beispiel: 699999.</span><span class="sxs-lookup"><span data-stu-id="44096-121">For example, 699999.</span></span>  
14. <span data-ttu-id="44096-122">Im Abschnitt **Details zu zulässigem Wert** klicken Sie auf **Übernehmen**.</span><span class="sxs-lookup"><span data-stu-id="44096-122">In the **Allowed value details** section, click **Apply**.</span></span>
15. <span data-ttu-id="44096-123">Wiederholen Sie die Schritte 10 bis 15 nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="44096-123">Repeat step 10 to 15 as needed.</span></span>  
16. <span data-ttu-id="44096-124">Im Abschnitt **Details zu zulässigem Wert** klicken Sie auf **Neue Kriterien hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="44096-124">In the **Allowed value details** section, click **Add new criteria**.</span></span>
17. <span data-ttu-id="44096-125">Wählen Sie im Feld "Operator" eine Option aus (z. B., "liegt zwischen" und "schließt ein").</span><span class="sxs-lookup"><span data-stu-id="44096-125">In the Operator field, select an option, such as is between and includes.</span></span>
18. <span data-ttu-id="44096-126">Geben Sie im Feld **Wert** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="44096-126">In the **Value** field, type a value.</span></span> <span data-ttu-id="44096-127">Beispiel: 033.</span><span class="sxs-lookup"><span data-stu-id="44096-127">For example, 033.</span></span>  
19. <span data-ttu-id="44096-128">Geben Sie im Feld **Bis** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="44096-128">In the **through** field, type a value.</span></span> <span data-ttu-id="44096-129">Beispiel: 034.</span><span class="sxs-lookup"><span data-stu-id="44096-129">For example, 034.</span></span>  
20. <span data-ttu-id="44096-130">Klicken Sie auf **Übernehmen**.</span><span class="sxs-lookup"><span data-stu-id="44096-130">Click **Apply**.</span></span>
21. <span data-ttu-id="44096-131">Wählen Sie im Raster das Segment aus, um die zulässigen Werte zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="44096-131">In the grid, select the segment to edit the allowed values.</span></span> <span data-ttu-id="44096-132">Beispiel: "Kostenstelle".</span><span class="sxs-lookup"><span data-stu-id="44096-132">For example, Cost Center.</span></span>  
22. <span data-ttu-id="44096-133">Geben Sie im **CostCenter-Feld** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="44096-133">In the **CostCenter field**, type a value.</span></span> <span data-ttu-id="44096-134">Beispiel: 007..021.</span><span class="sxs-lookup"><span data-stu-id="44096-134">For example, 007..021.</span></span>  
23. <span data-ttu-id="44096-135">Klicken Sie in **Segmente und zulässige Werte** auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="44096-135">In the **Segments and allowed values**, click **Add**.</span></span>
24. <span data-ttu-id="44096-136">Geben Sie im Feld **MainAccount** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="44096-136">In the **MainAccount** field, type a value.</span></span> <span data-ttu-id="44096-137">Beispiel: 600000..699999</span><span class="sxs-lookup"><span data-stu-id="44096-137">For example, 600000..699999</span></span>  
25. <span data-ttu-id="44096-138">Wählen Sie im Raster das Segment aus, um die zulässigen Werte zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="44096-138">In the grid, select the segment to edit the allowed values.</span></span> <span data-ttu-id="44096-139">Beispiel: "Abteilung".</span><span class="sxs-lookup"><span data-stu-id="44096-139">For example, Department.</span></span>  
26. <span data-ttu-id="44096-140">Geben Sie im Feld "Abteilung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="44096-140">In the Department field, type a value.</span></span> <span data-ttu-id="44096-141">Beispiel: 032.</span><span class="sxs-lookup"><span data-stu-id="44096-141">For example, 032.</span></span>  
27. <span data-ttu-id="44096-142">Geben Sie im Feld "CostCenter" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="44096-142">In the CostCenter field, type a value.</span></span> <span data-ttu-id="44096-143">Beispiel: 086.</span><span class="sxs-lookup"><span data-stu-id="44096-143">For example, 086.</span></span>  
28. <span data-ttu-id="44096-144">Klicken Sie im **Aktivitätsbereich** auf **Überprüfen**.</span><span class="sxs-lookup"><span data-stu-id="44096-144">On the **Action pane**, click **Validate**.</span></span>
29. <span data-ttu-id="44096-145">Klicken Sie im **Aktivitätsbereich** auf **Aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="44096-145">On the **Action pane**, click **Activate**.</span></span>
30. <span data-ttu-id="44096-146">Klicken Sie auf **Aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="44096-146">Click **Activate**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]