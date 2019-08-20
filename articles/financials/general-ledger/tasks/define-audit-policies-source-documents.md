---
title: Überwachungsrichtlinien für Quelldokumente definieren
description: Diese Prozedur zeigt, wie und Überwachungsrichtlinienregeln eingerichtet und ausgeführt werden.
author: ryansandness
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: 17b712f07a0ffe6874eb6d98b47ced96f5a54483
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846486"
---
# <a name="define-audit-policies-for-source-documents"></a><span data-ttu-id="67752-103">Überwachungsrichtlinien für Quelldokumente definieren</span><span class="sxs-lookup"><span data-stu-id="67752-103">Define audit policies for source documents</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="67752-104">Diese Prozedur zeigt, wie und Überwachungsrichtlinienregeln eingerichtet und ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="67752-104">This procedure shows how to set up and run audit policy rules.</span></span> <span data-ttu-id="67752-105">Das Beispiel verwendet Spesenabrechnungen mit dem Hotelausgabentyp.</span><span class="sxs-lookup"><span data-stu-id="67752-105">The example uses expense reports with the hotel expense type.</span></span> <span data-ttu-id="67752-106">Für diese Prozedur wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="67752-106">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="67752-107">Die Wirtschaftsprüferrolle umfasst die richtigen Berechtigungen, um diese Aufgaben auszuführen.</span><span class="sxs-lookup"><span data-stu-id="67752-107">The auditor role contains the correct permissions in order to perform these tasks.</span></span>

1. <span data-ttu-id="67752-108">Wechseln Sie zu "Überwachungsworkbench" > "Einstellung" > "Richtlinienregeltyp".</span><span class="sxs-lookup"><span data-stu-id="67752-108">Go to Audit workbench > Setup > Policy rule type.</span></span>
2. <span data-ttu-id="67752-109">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="67752-109">Click New.</span></span>
3. <span data-ttu-id="67752-110">Geben Sie im Feld "Regelname" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="67752-110">In the Rule name field, type a value.</span></span>
4. <span data-ttu-id="67752-111">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="67752-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="67752-112">Wählen Sie im Feld "Abfragename" die Position "Spesenabrechnung" aus</span><span class="sxs-lookup"><span data-stu-id="67752-112">In the Query name field, select Expense report line</span></span>
6. <span data-ttu-id="67752-113">Wählen Sie im Abfragetypfeld "Zusammenführen" aus</span><span class="sxs-lookup"><span data-stu-id="67752-113">In the query type field, select Aggregate</span></span>
7. <span data-ttu-id="67752-114">Wählen Sie im Feld "Juristische Person" die Option "Juristische Person" aus</span><span class="sxs-lookup"><span data-stu-id="67752-114">In the Legal entity field, select Legal entity</span></span>
8. <span data-ttu-id="67752-115">Wählen Sie im Feld "Dokumentdatumsreferenz" die Option "Änderungsdatum und -uhrzeit" aus</span><span class="sxs-lookup"><span data-stu-id="67752-115">In the Document date reference field, select Modified date and time</span></span>
9. <span data-ttu-id="67752-116">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="67752-116">Click Save.</span></span>
10. <span data-ttu-id="67752-117">Wechseln Sie zu "Überwachungsworkbench" > "Einstellung" > "Überwachungsrichtlinien".</span><span class="sxs-lookup"><span data-stu-id="67752-117">Go to Audit workbench > Setup > Audit policies.</span></span>
11. <span data-ttu-id="67752-118">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="67752-118">Click New.</span></span>
12. <span data-ttu-id="67752-119">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="67752-119">In the Name field, type a value.</span></span>
13. <span data-ttu-id="67752-120">Erweitern Sie den Abschnitt "Richtlinienorganisationen".</span><span class="sxs-lookup"><span data-stu-id="67752-120">Expand the Policy organizations section.</span></span>
14. <span data-ttu-id="67752-121">Wählen Sie in der Struktur "Contoso Unterhaltungsanlagen USA" aus.</span><span class="sxs-lookup"><span data-stu-id="67752-121">In the tree, select 'Contoso Entertainment System USA'.</span></span>
15. <span data-ttu-id="67752-122">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="67752-122">Click Add.</span></span>
16. <span data-ttu-id="67752-123">Wählen Sie in der Struktur "Contoso Beratung USA" aus.</span><span class="sxs-lookup"><span data-stu-id="67752-123">In the tree, select 'Contoso Consulting USA'.</span></span>
17. <span data-ttu-id="67752-124">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="67752-124">Click Add.</span></span>
18. <span data-ttu-id="67752-125">Wählen Sie in der Struktur "Contoso Einzelhandel USA" aus.</span><span class="sxs-lookup"><span data-stu-id="67752-125">In the tree, select 'Contoso Retail USA'.</span></span>
19. <span data-ttu-id="67752-126">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="67752-126">Click Add.</span></span>
20. <span data-ttu-id="67752-127">Reduzieren Sie den Abschnitt "Richtlinienorganisationen".</span><span class="sxs-lookup"><span data-stu-id="67752-127">Collapse the Policy organizations section.</span></span>
21. <span data-ttu-id="67752-128">Erweitern Sie den Abschnitt "Richtlinienregeln".</span><span class="sxs-lookup"><span data-stu-id="67752-128">Expand the Policy rules section.</span></span>
22. <span data-ttu-id="67752-129">Suchen Sie in der Liste die zuvor erstellte "Richtlinienregel" und wählen Sie diese aus.</span><span class="sxs-lookup"><span data-stu-id="67752-129">In the list, find and select the Policy Rule that was created previously.</span></span>
23. <span data-ttu-id="67752-130">Klicken Sie auf "Richtlinienregel erstellen".</span><span class="sxs-lookup"><span data-stu-id="67752-130">Click Create policy rule.</span></span>
24. <span data-ttu-id="67752-131">Geben Sie im Feld "Gültigkeitsdatum" ein Datum und eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="67752-131">In the Effective date field, enter a date and time.</span></span>
25. <span data-ttu-id="67752-132">Klicken Sie auf "Filter".</span><span class="sxs-lookup"><span data-stu-id="67752-132">Click Filter.</span></span>
26. <span data-ttu-id="67752-133">Wählen Sie in der Liste die Zeile für "Ausgabenkategorie" aus, und legen Sie die Details zum "Hotel" fest</span><span class="sxs-lookup"><span data-stu-id="67752-133">In the list, select the row for Expense category, and set the details to Hotel</span></span>
27. <span data-ttu-id="67752-134">Geben Sie im Feld "Kriterien" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="67752-134">In the Criteria field, enter or select a value.</span></span>
28. <span data-ttu-id="67752-135">Klicken Sie auf die Registerkarte "Zusammenführen".</span><span class="sxs-lookup"><span data-stu-id="67752-135">Click the Aggregate tab.</span></span>
29. <span data-ttu-id="67752-136">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="67752-136">Click Add.</span></span>
30. <span data-ttu-id="67752-137">Wählen Sie in der Liste einen Feldwert von "Transaktionsbetrag" aus</span><span class="sxs-lookup"><span data-stu-id="67752-137">In the list, select a field value of Transaction amount</span></span>
31. <span data-ttu-id="67752-138">Geben Sie im Feld "Feld" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="67752-138">In the Field field, enter or select a value.</span></span>
32. <span data-ttu-id="67752-139">Wählen Sie im Feld "Funktion zusammenführen" die Option "Summe" aus.</span><span class="sxs-lookup"><span data-stu-id="67752-139">In the AggregateFunction field, select 'Sum'.</span></span>
33. <span data-ttu-id="67752-140">Klicken Sie auf die Registerkarte "Gruppieren nach".</span><span class="sxs-lookup"><span data-stu-id="67752-140">Click the Group by tab.</span></span>
34. <span data-ttu-id="67752-141">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="67752-141">Click Add.</span></span>
35. <span data-ttu-id="67752-142">Wählen Sie in der Liste einen Wert von "Mitarbeiter" aus </span><span class="sxs-lookup"><span data-stu-id="67752-142">In the list, select a value of Employee</span></span> 
36. <span data-ttu-id="67752-143">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="67752-143">Click Add.</span></span>
37. <span data-ttu-id="67752-144">Wählen Sie in der Liste einen Wert von "Ausgabenkategorie" aus</span><span class="sxs-lookup"><span data-stu-id="67752-144">In the list, select a value of Expense category</span></span>
38. <span data-ttu-id="67752-145">Geben Sie im Feld "Feld" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="67752-145">In the Field field, enter or select a value.</span></span>
39. <span data-ttu-id="67752-146">Klicken Sie auf die Registerkarte "Haben".</span><span class="sxs-lookup"><span data-stu-id="67752-146">Click the Having tab.</span></span>
40. <span data-ttu-id="67752-147">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="67752-147">Click Add.</span></span>
41. <span data-ttu-id="67752-148">Wählen Sie den "Transaktionsbetrag" aus</span><span class="sxs-lookup"><span data-stu-id="67752-148">Select Transaction amount</span></span>
42. <span data-ttu-id="67752-149">Geben Sie im Feld "Feld" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="67752-149">In the Field field, enter or select a value.</span></span>
43. <span data-ttu-id="67752-150">Wählen Sie im Feld "Funktion zusammenführen" die Option "Summe" aus.</span><span class="sxs-lookup"><span data-stu-id="67752-150">In the AggregateFunction field, select 'Sum'.</span></span>
44. <span data-ttu-id="67752-151">Geben Sie im Feld "Kriterien" den Wert ">2000" ein.</span><span class="sxs-lookup"><span data-stu-id="67752-151">In the Criteria field, type '>2000'.</span></span>
45. <span data-ttu-id="67752-152">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="67752-152">Click OK.</span></span>
46. <span data-ttu-id="67752-153">Klicken Sie auf Test.</span><span class="sxs-lookup"><span data-stu-id="67752-153">Click Test.</span></span>
47. <span data-ttu-id="67752-154">Geben Sie im Feld "Startdatum für Dokumentauswahl" ein Datum und eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="67752-154">In the Document selection starting date field, enter a date and time.</span></span>
48. <span data-ttu-id="67752-155">Geben Sie im Feld "Enddatum für Dokumentauswahl" ein Datum und eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="67752-155">In the Document selection ending date field, enter a date and time.</span></span>
49. <span data-ttu-id="67752-156">Klicken Sie auf "Test ausführen".</span><span class="sxs-lookup"><span data-stu-id="67752-156">Click Run test.</span></span>
50. <span data-ttu-id="67752-157">Klicken Sie im Aktivitätsbereich auf "Überwachungsrichtlinie".</span><span class="sxs-lookup"><span data-stu-id="67752-157">On the Action Pane, click Audit policy.</span></span>
51. <span data-ttu-id="67752-158">Klicken Sie auf "Zusätzliche Optionen".</span><span class="sxs-lookup"><span data-stu-id="67752-158">Click Additional options.</span></span>
52. <span data-ttu-id="67752-159">Geben Sie im Feld "Startdatum" ein Datum und eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="67752-159">In the Starting date field, enter a date and time.</span></span>
53. <span data-ttu-id="67752-160">Geben Sie im Feld "Enddatum" ein Datum und eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="67752-160">In the Ending date field, enter a date and time.</span></span>
54. <span data-ttu-id="67752-161">Klicken Sie auf "Charge".</span><span class="sxs-lookup"><span data-stu-id="67752-161">Click Batch.</span></span>
55. <span data-ttu-id="67752-162">Erweitern Sie den Abschnitt "Ausführen im Hintergrund".</span><span class="sxs-lookup"><span data-stu-id="67752-162">Expand the Run in the background section.</span></span>
56. <span data-ttu-id="67752-163">Wählen Sie "Ja" im Feld "Stapelverarbeitung" aus.</span><span class="sxs-lookup"><span data-stu-id="67752-163">Select Yes in the Batch processing field.</span></span>
57. <span data-ttu-id="67752-164">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="67752-164">Click OK.</span></span>
58. <span data-ttu-id="67752-165">Wechseln Sie zu "Überwachungsworkbench" > "Überwachungsanfragen".</span><span class="sxs-lookup"><span data-stu-id="67752-165">Go to Audit workbench > Audit cases.</span></span>
59. <span data-ttu-id="67752-166">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="67752-166">In the list, find and select the desired record.</span></span>
60. <span data-ttu-id="67752-167">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="67752-167">In the list, click the link in the selected row.</span></span>
61. <span data-ttu-id="67752-168">Erweitern Sie den Abschnitt "Zuordnungen".</span><span class="sxs-lookup"><span data-stu-id="67752-168">Expand the Associations section.</span></span>
62. <span data-ttu-id="67752-169">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="67752-169">In the list, find and select the desired record.</span></span>
63. <span data-ttu-id="67752-170">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="67752-170">In the list, click the link in the selected row.</span></span>

