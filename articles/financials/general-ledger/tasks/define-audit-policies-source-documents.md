---
title: Überwachungsrichtlinien für Quelldokumente definieren
description: Dieses Thema erklärt, wie und Überwachungsrichtlinienregeln eingerichtet und ausgeführt werden.
author: ryansandness
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysFieldLookUp, SysPolicyListPage, SysPolicy, AuditPolicyRule, SysQueryForm, SysQueryFieldLookUp, AuditPolicyDateSelection, AuditPolicyAdditionalOption, BatchJob, CaseDetail
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a6b0fa28d778a4d9fa1f718b1d50bf1dce00be00
ms.sourcegitcommit: e10491a2ff04f65d9f306ef6e068ee123213b23b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2019
ms.locfileid: "1914826"
---
# <a name="define-audit-policies-for-source-documents"></a><span data-ttu-id="c1175-103">Überwachungsrichtlinien für Quelldokumente definieren</span><span class="sxs-lookup"><span data-stu-id="c1175-103">Define audit policies for source documents</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c1175-104">Dieses Thema erklärt, wie und Überwachungsrichtlinienregeln eingerichtet und ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c1175-104">This topic explains how to set up and run audit policy rules.</span></span> <span data-ttu-id="c1175-105">Das Beispiel verwendet Spesenabrechnungen mit dem Hotelausgabentyp.</span><span class="sxs-lookup"><span data-stu-id="c1175-105">The example uses expense reports with the hotel expense type.</span></span> <span data-ttu-id="c1175-106">Für diese Prozedur wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="c1175-106">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="c1175-107">Die Wirtschaftsprüferrolle umfasst die richtigen Berechtigungen, um diese Aufgaben auszuführen.</span><span class="sxs-lookup"><span data-stu-id="c1175-107">The auditor role contains the correct permissions in order to perform these tasks.</span></span>

1. <span data-ttu-id="c1175-108">Gehen Sie im Navigationsbereich zu **Module > Überwachungs-Workbench > Einstellungen > Richtlinienregeltyp**.</span><span class="sxs-lookup"><span data-stu-id="c1175-108">In the navigation pane, go to **Modules > Audit workbench > Setup > Policy rule type**.</span></span>
2. <span data-ttu-id="c1175-109">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="c1175-109">Select **New**.</span></span>
3. <span data-ttu-id="c1175-110">Geben Sie im Feld **Regelname** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="c1175-110">In the **Rule name** field, type a value.</span></span>
4. <span data-ttu-id="c1175-111">Geben Sie im Feld **Beschreibung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="c1175-111">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="c1175-112">Wählen Sie im Feld **Abfragename** **Spesenabrechnungsposition** aus</span><span class="sxs-lookup"><span data-stu-id="c1175-112">In the **Query name** field, select **Expense report line**</span></span>
6. <span data-ttu-id="c1175-113">Wählen Sie im Feld **Abfragetyp** **Zusammenführen** aus</span><span class="sxs-lookup"><span data-stu-id="c1175-113">In the **query type** field, select **Aggregate**</span></span>
7. <span data-ttu-id="c1175-114">Wählen Sie im Feld **Juristische Person** die Option **Juristische Person** aus.</span><span class="sxs-lookup"><span data-stu-id="c1175-114">In the **Legal entity** field, select **Legal entity**</span></span>
8. <span data-ttu-id="c1175-115">Wählen Sie im Feld **Dokumentdatumsreferenz** die Option **Änderungsdatum und -uhrzeit** aus</span><span class="sxs-lookup"><span data-stu-id="c1175-115">In the **Document date reference** field, select **Modified date and time**</span></span>
9. <span data-ttu-id="c1175-116">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="c1175-116">Select **Save**.</span></span>
10. <span data-ttu-id="c1175-117">Gehen Sie im Navigationsbereich zu **Module > Überwachungs-Workbench > Einstellungen > Überwachungsrichtlinien**.</span><span class="sxs-lookup"><span data-stu-id="c1175-117">In the navigation pane, go to **Modules > Audit workbench > Setup > Audit policies**.</span></span>
11. <span data-ttu-id="c1175-118">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="c1175-118">Select **New**.</span></span>
12. <span data-ttu-id="c1175-119">Geben Sie im Feld **Name** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="c1175-119">In the **Name** field, type a value.</span></span>
13. <span data-ttu-id="c1175-120">Erweitern Sie den Abschnitt **Richtlinienorganisationen**.</span><span class="sxs-lookup"><span data-stu-id="c1175-120">Expand the **Policy organizations** section.</span></span>
14. <span data-ttu-id="c1175-121">Wählen Sie in der Struktur **Contoso Unterhaltungsanlagen USA** aus, und wählen Sie dann **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="c1175-121">In the tree, select **Contoso Entertainment System USA**, then select **Add**.</span></span>
15. <span data-ttu-id="c1175-122">Wählen Sie in der Struktur **Contoso Beratung USA** aus, und wählen Sie dann **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="c1175-122">In the tree, select **Contoso Consulting USA**, then select **Add**.</span></span>
16. <span data-ttu-id="c1175-123">Wählen Sie in der Struktur **Contoso Einzelhandel USA** aus, und wählen Sie dann **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="c1175-123">In the tree, select **Contoso Retail USA**, then select **Add**.</span></span>
17. <span data-ttu-id="c1175-124">Reduzieren Sie den Abschnitt **Richtlinienorganisationen**.</span><span class="sxs-lookup"><span data-stu-id="c1175-124">Collapse the **Policy organizations** section.</span></span>
18. <span data-ttu-id="c1175-125">Erweitern Sie den Abschnitt **Richtlinienregeln**.</span><span class="sxs-lookup"><span data-stu-id="c1175-125">Expand the **Policy rules** section.</span></span>
19. <span data-ttu-id="c1175-126">Suchen Sie in der Liste die zuvor erstellte "Richtlinienregel" und wählen Sie diese aus.</span><span class="sxs-lookup"><span data-stu-id="c1175-126">In the list, find and select the Policy Rule that was created previously.</span></span>
20. <span data-ttu-id="c1175-127">Wählen Sie **Richtlinienregel erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="c1175-127">Select **Create policy rule**.</span></span>
21. <span data-ttu-id="c1175-128">Geben Sie im Feld **Gültigkeitsdatum** ein Datum und eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="c1175-128">In the **Effective date** field, enter a date and time.</span></span>
22. <span data-ttu-id="c1175-129">Wählen Sie **Filter** aus.</span><span class="sxs-lookup"><span data-stu-id="c1175-129">Select **Filter**.</span></span>
23. <span data-ttu-id="c1175-130">Wählen Sie in der Liste die Zeile für **Spesenkategorie** aus, und legen Sie die Details zum **Hotel** fest.</span><span class="sxs-lookup"><span data-stu-id="c1175-130">In the list, select the row for **Expense category**, and set the details to **Hotel**.</span></span>
24. <span data-ttu-id="c1175-131">Geben Sie im Feld **Kriterien** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="c1175-131">In the **Criteria** field, enter or select a value.</span></span>
25. <span data-ttu-id="c1175-132">Wählen Sie die Registerkarte **Zusammenführen** aus.</span><span class="sxs-lookup"><span data-stu-id="c1175-132">Select the **Aggregate** tab.</span></span>
26. <span data-ttu-id="c1175-133">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="c1175-133">Select **Add**.</span></span>
27. <span data-ttu-id="c1175-134">Wählen Sie in der Liste einen Feldwert von **Buchungsbetrag** aus.</span><span class="sxs-lookup"><span data-stu-id="c1175-134">In the list, select a field value of **Transaction amount**.</span></span>
28. <span data-ttu-id="c1175-135">Geben Sie im Feld **Feld** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="c1175-135">In the **Field** field, enter or select a value.</span></span>
29. <span data-ttu-id="c1175-136">Wählen Sie im Feld **Funktion zusammenführen** die Option **Summe** aus.</span><span class="sxs-lookup"><span data-stu-id="c1175-136">In the **AggregateFunction** field, select **Sum**.</span></span>
30. <span data-ttu-id="c1175-137">Wählen Sie die Registerkarte **Gruppieren nach** aus.</span><span class="sxs-lookup"><span data-stu-id="c1175-137">Select the **Group by** tab.</span></span>
31. <span data-ttu-id="c1175-138">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="c1175-138">Select **Add**.</span></span>
32. <span data-ttu-id="c1175-139">Wählen Sie in der Liste einen Wert von **Mitarbeiter** aus.</span><span class="sxs-lookup"><span data-stu-id="c1175-139">In the list, select a value of **Employee** .</span></span>
33. <span data-ttu-id="c1175-140">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="c1175-140">Select **Add**.</span></span>
34. <span data-ttu-id="c1175-141">Wählen Sie in der Liste einen Wert von **Ausgabenkategorie** aus.</span><span class="sxs-lookup"><span data-stu-id="c1175-141">In the list, select a value of **Expense category**.</span></span>
35. <span data-ttu-id="c1175-142">Geben Sie im Feld **Feld** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="c1175-142">In the **Field** field, enter or select a value.</span></span>
36. <span data-ttu-id="c1175-143">Wählen Sie die Registerkarte **Haben** aus.</span><span class="sxs-lookup"><span data-stu-id="c1175-143">Select the **Having** tab.</span></span>
37. <span data-ttu-id="c1175-144">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="c1175-144">Select **Add**.</span></span>
38. <span data-ttu-id="c1175-145">Wählen Sie **Transaktionsbetrag** aus.</span><span class="sxs-lookup"><span data-stu-id="c1175-145">Select **Transaction amount**.</span></span>
39. <span data-ttu-id="c1175-146">Geben Sie im Feld **Feld** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="c1175-146">In the **Field** field, enter or select a value.</span></span>
40. <span data-ttu-id="c1175-147">Wählen Sie im Feld **Funktion zusammenführen** die Option **Summe** aus.</span><span class="sxs-lookup"><span data-stu-id="c1175-147">In the **AggregateFunction** field, select **Sum**.</span></span>
41. <span data-ttu-id="c1175-148">Geben Sie im Feld **Kriterien** `>2000` ein.</span><span class="sxs-lookup"><span data-stu-id="c1175-148">In the **Criteria** field, type `>2000`.</span></span>
42. <span data-ttu-id="c1175-149">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="c1175-149">Select **OK**.</span></span>
43. <span data-ttu-id="c1175-150">Wählen Sie **Testen** aus.</span><span class="sxs-lookup"><span data-stu-id="c1175-150">Select **Test**.</span></span>
44. <span data-ttu-id="c1175-151">Geben Sie im Feld **Startdatum für Dokumentauswahl** ein Datum und eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="c1175-151">In the **Document selection starting date** field, enter a date and time.</span></span>
45. <span data-ttu-id="c1175-152">Geben Sie im Feld **Enddatum für Dokumentauswahl** ein Datum und eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="c1175-152">In the **Document selection ending date** field, enter a date and time.</span></span>
46. <span data-ttu-id="c1175-153">Wählen Sie **Test ausführen** aus.</span><span class="sxs-lookup"><span data-stu-id="c1175-153">Select **Run test**.</span></span>
47. <span data-ttu-id="c1175-154">Wählen Sie im Aktivitätsbereich **Überwachungsrichtlinie** aus.</span><span class="sxs-lookup"><span data-stu-id="c1175-154">On the Action Pane, select **Audit policy**.</span></span>
48. <span data-ttu-id="c1175-155">Wählen Sie **Weitere Optionen** aus.</span><span class="sxs-lookup"><span data-stu-id="c1175-155">Select **Additional options**.</span></span>
49. <span data-ttu-id="c1175-156">Geben Sie im Feld **Startdatum** ein Datum und eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="c1175-156">In the **Starting date** field, enter a date and time.</span></span>
50. <span data-ttu-id="c1175-157">Geben Sie im Feld **Enddatum** ein Datum und eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="c1175-157">In the **Ending date** field, enter a date and time.</span></span>
51. <span data-ttu-id="c1175-158">Wählen Sie **Charge** aus.</span><span class="sxs-lookup"><span data-stu-id="c1175-158">Select **Batch**.</span></span>
52. <span data-ttu-id="c1175-159">Erweitern Sie den Abschnitt **Im Hintergrund ausführen**.</span><span class="sxs-lookup"><span data-stu-id="c1175-159">Expand the **Run in the background** section.</span></span>
53. <span data-ttu-id="c1175-160">Wählen Sie **Ja** im Feld **Stapelverarbeitung** aus.</span><span class="sxs-lookup"><span data-stu-id="c1175-160">Select **Yes** in the **Batch processing** field.</span></span>
54. <span data-ttu-id="c1175-161">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="c1175-161">Select **OK**.</span></span>
55. <span data-ttu-id="c1175-162">Gehen Sie im Navigationsbereich zu **Module > Überwachungs-Workbench > Überwachungsanfragen**.</span><span class="sxs-lookup"><span data-stu-id="c1175-162">In the navigation pane, go to **Modules > Audit workbench > Audit cases**.</span></span>
56. <span data-ttu-id="c1175-163">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="c1175-163">In the list, find and select the desired record.</span></span>
57. <span data-ttu-id="c1175-164">Erweitern Sie den Abschnitt **Zuordnungen**.</span><span class="sxs-lookup"><span data-stu-id="c1175-164">Expand the **Associations** section.</span></span>
58. <span data-ttu-id="c1175-165">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="c1175-165">In the list, find and select the desired record.</span></span>

