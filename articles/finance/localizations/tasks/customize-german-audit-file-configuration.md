---
title: Anpassen der deutschen Protokolldateikonfiguration
description: Im folgenden Verfahren sehen Sie, wie Sie die deutsche Protokolldateikonfiguration durch Hinzufügen einer neuen Tabellengruppe und Auswählen einer Tabelle mit Feldern für die Datenexportdefinition anpassen.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, ERTableNameLookup, ERModelGDPdUFunctionEditor,  ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Germany
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fbc371fabb85dd60004831fcef68111851050f9f
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141549"
---
# <a name="customize-german-audit-file-configuration"></a><span data-ttu-id="68f72-103">Anpassen der deutschen Protokolldateikonfiguration</span><span class="sxs-lookup"><span data-stu-id="68f72-103">Customize German audit file configuration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="68f72-104">Im folgenden Verfahren sehen Sie, wie Sie die deutsche Protokolldateikonfiguration durch Hinzufügen einer neuen Tabellengruppe und Auswählen einer Tabelle mit Feldern für die Datenexportdefinition anpassen.</span><span class="sxs-lookup"><span data-stu-id="68f72-104">This procedure shows how to customize the German audit file configuration by adding a new table group and selecting a table with fields for data export definition.</span></span> 

<span data-ttu-id="68f72-105">Diese Aufgabe wurde mithilfe des Demodatenunternehmens DEMF erstellt, mit "Deutschland" als Land/Region für die primäre Adresse für die juristischen Person.</span><span class="sxs-lookup"><span data-stu-id="68f72-105">This procedure was created using the demo data company DEMF with Germany as the country of legal entity primary address.</span></span>

1. <span data-ttu-id="68f72-106">Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="68f72-106">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="68f72-107">Klicken Sie auf "Konfigurationen".</span><span class="sxs-lookup"><span data-stu-id="68f72-107">Click Configurations.</span></span>
3. <span data-ttu-id="68f72-108">Klicken Sie auf "Filter anzeigen".</span><span class="sxs-lookup"><span data-stu-id="68f72-108">Click Show filters.</span></span>
4. <span data-ttu-id="68f72-109">Filter hinzufügen</span><span class="sxs-lookup"><span data-stu-id="68f72-109">Add filter</span></span>
5. <span data-ttu-id="68f72-110">Klicken Sie auf Übernehmen.</span><span class="sxs-lookup"><span data-stu-id="68f72-110">Click Apply.</span></span>
6. <span data-ttu-id="68f72-111">Klicken Sie auf "Modelldesigner".</span><span class="sxs-lookup"><span data-stu-id="68f72-111">Click Model designer.</span></span>
7. <span data-ttu-id="68f72-112">Wählen Sie in der Struktur 'enumTableGroup' aus.</span><span class="sxs-lookup"><span data-stu-id="68f72-112">In the tree, select 'enumTableGroup'.</span></span>
8. <span data-ttu-id="68f72-113">Klicken Sie auf Neu.</span><span class="sxs-lookup"><span data-stu-id="68f72-113">Click New.</span></span>
9. <span data-ttu-id="68f72-114">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="68f72-114">In the Name field, type a value.</span></span>
10. <span data-ttu-id="68f72-115">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="68f72-115">In the Description field, type a value.</span></span>
11. <span data-ttu-id="68f72-116">Klicken Sie auf "Modell der Datenquelle zuordnen".</span><span class="sxs-lookup"><span data-stu-id="68f72-116">Click Map model to datasource.</span></span>
12. <span data-ttu-id="68f72-117">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="68f72-117">Click Designer.</span></span>
13. <span data-ttu-id="68f72-118">Wählen Sie in der Strukturdarstellung "Dynamics Ax\Tabellendatensätze" aus.</span><span class="sxs-lookup"><span data-stu-id="68f72-118">In the tree, select 'Dynamics Ax\Table records'.</span></span>
14. <span data-ttu-id="68f72-119">Klicken Sie auf "Stamm hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="68f72-119">Click Add root.</span></span>
15. <span data-ttu-id="68f72-120">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="68f72-120">In the Name field, type a value.</span></span>
16. <span data-ttu-id="68f72-121">Geben Sie im Feld 'Tabelle' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="68f72-121">In the Table field, enter or select a value.</span></span>
17. <span data-ttu-id="68f72-122">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="68f72-122">Click OK.</span></span>
18. <span data-ttu-id="68f72-123">Wählen Sie in der Struktur "Functions\Table metadata" aus.</span><span class="sxs-lookup"><span data-stu-id="68f72-123">In the tree, select 'Functions\Table metadata'.</span></span>
19. <span data-ttu-id="68f72-124">Klicken Sie auf "Stamm hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="68f72-124">Click Add root.</span></span>
20. <span data-ttu-id="68f72-125">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="68f72-125">In the Name field, type a value.</span></span>
21. <span data-ttu-id="68f72-126">Geben Sie im Feld Beschreibung einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="68f72-126">In the Label field, type a value.</span></span>
22. <span data-ttu-id="68f72-127">Klicken Sie auf "Editor".</span><span class="sxs-lookup"><span data-stu-id="68f72-127">Click Editor.</span></span>
23. <span data-ttu-id="68f72-128">Wählen Sie in der -Struktur "AssetTable" aus.</span><span class="sxs-lookup"><span data-stu-id="68f72-128">In the tree, select 'AssetTable'.</span></span>
24. <span data-ttu-id="68f72-129">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="68f72-129">Click Add.</span></span>
25. <span data-ttu-id="68f72-130">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="68f72-130">In the Name field, type a value.</span></span>
26. <span data-ttu-id="68f72-131">Erweitern Sie in der Struktur den Knoten 'AssetTable'.</span><span class="sxs-lookup"><span data-stu-id="68f72-131">In the tree, expand 'AssetTable'.</span></span>
27. <span data-ttu-id="68f72-132">Wählen Sie in der Struktur "AssetTable\Fixed asset number(AssetId)" aus.</span><span class="sxs-lookup"><span data-stu-id="68f72-132">In the tree, select 'AssetTable\Fixed asset number(AssetId)'.</span></span>
28. <span data-ttu-id="68f72-133">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="68f72-133">Click Add.</span></span>
29. <span data-ttu-id="68f72-134">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="68f72-134">In the list, mark the selected row.</span></span>
30. <span data-ttu-id="68f72-135">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="68f72-135">In the Name field, type a value.</span></span>
31. <span data-ttu-id="68f72-136">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="68f72-136">Close the page.</span></span>
32. <span data-ttu-id="68f72-137">Klicken Sie auf "Ja".</span><span class="sxs-lookup"><span data-stu-id="68f72-137">Click Yes.</span></span>
33. <span data-ttu-id="68f72-138">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="68f72-138">Click OK.</span></span>
34. <span data-ttu-id="68f72-139">Wählen Sie in der Struktur "TblGroup" aus.</span><span class="sxs-lookup"><span data-stu-id="68f72-139">In the tree, select 'TblGroup'.</span></span>
35. <span data-ttu-id="68f72-140">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="68f72-140">Click Edit.</span></span>
36. <span data-ttu-id="68f72-141">Klicken Sie auf Formel bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="68f72-141">Click Edit formula.</span></span>
37. <span data-ttu-id="68f72-142">Geben Sie im Feld "expressionAsStringText" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="68f72-142">In the expressionAsStringText field, type a value.</span></span>
38. <span data-ttu-id="68f72-143">Erweitern oder reduzieren Sie 'enumTableGroup' in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="68f72-143">In the tree, expand 'enumTableGroup'.</span></span>
39. <span data-ttu-id="68f72-144">Wählen Sie in der Struktur 'enumTableGroup\Anlagen' aus.</span><span class="sxs-lookup"><span data-stu-id="68f72-144">In the tree, select 'enumTableGroup\Anlagen'.</span></span>
40. <span data-ttu-id="68f72-145">Klicken Sie auf Datenquelle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="68f72-145">Click Add data source.</span></span>
41. <span data-ttu-id="68f72-146">Geben Sie im Feld "expressionAsStringText" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="68f72-146">In the expressionAsStringText field, type a value.</span></span>
42. <span data-ttu-id="68f72-147">Wählen Sie in der Struktur '_05Anlagen(TblGroup5)' aus.</span><span class="sxs-lookup"><span data-stu-id="68f72-147">In the tree, select '_05Anlagen(TblGroup5)'.</span></span>
43. <span data-ttu-id="68f72-148">Klicken Sie auf Datenquelle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="68f72-148">Click Add data source.</span></span>
44. <span data-ttu-id="68f72-149">Geben Sie im Feld "expressionAsStringText" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="68f72-149">In the expressionAsStringText field, type a value.</span></span>
45. <span data-ttu-id="68f72-150">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="68f72-150">Click Save.</span></span>
46. <span data-ttu-id="68f72-151">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="68f72-151">Close the page.</span></span>
47. <span data-ttu-id="68f72-152">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="68f72-152">Click OK.</span></span>
48. <span data-ttu-id="68f72-153">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="68f72-153">Close the page.</span></span>
49. <span data-ttu-id="68f72-154">Klicken Sie auf "Ja".</span><span class="sxs-lookup"><span data-stu-id="68f72-154">Click Yes.</span></span>
50. <span data-ttu-id="68f72-155">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="68f72-155">Close the page.</span></span>
51. <span data-ttu-id="68f72-156">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="68f72-156">Close the page.</span></span>
52. <span data-ttu-id="68f72-157">Klicken Sie auf "Status ändern".</span><span class="sxs-lookup"><span data-stu-id="68f72-157">Click Change status.</span></span>
53. <span data-ttu-id="68f72-158">Klicken Sie auf "Abgeschlossen".</span><span class="sxs-lookup"><span data-stu-id="68f72-158">Click Complete.</span></span>
54. <span data-ttu-id="68f72-159">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="68f72-159">In the Description field, type a value.</span></span>
55. <span data-ttu-id="68f72-160">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="68f72-160">Click OK.</span></span>

