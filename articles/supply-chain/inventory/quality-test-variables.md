---
title: Qualitätsmanagement-Testvariablen
description: Dieses Thema beschreibt, wie Sie Testvariablen erstellen, die für qualitative Tests zu Qualitätsprüfungsaufträgen in Microsoft Dynamics 365 Supply Chain Management verwendet werden können.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b5102d09f5762a390d6fd3aadafcb2ed23820982
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021707"
---
# <a name="quality-management-test-variables"></a><span data-ttu-id="e5ef2-103">Qualitätsmanagement-Testvariablen</span><span class="sxs-lookup"><span data-stu-id="e5ef2-103">Quality management test variables</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e5ef2-104">Dieses Thema beschreibt, wie Sie Testvariablen erstellen, die für qualitative Tests zu Qualitätsprüfungsaufträgen in Microsoft Dynamics 365 Supply Chain Management verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-104">This topic describes how to create test variables that can be used for qualitative tests on quality orders in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="e5ef2-105">Für jeden qualitativen Test, der auf der Seite **Tests** definiert wird, müssen Sie eine Testvariable und ihre möglichen Ergebnisse (Resultate) definieren.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-105">For every qualitative test that is defined on the **Tests** page, you must define a test variable and its possible outcomes (results).</span></span> <span data-ttu-id="e5ef2-106">(Für qualitative Tests wird das Feld **Typ** auf der Seite **Tests** auf *Option* festgelegt.)</span><span class="sxs-lookup"><span data-stu-id="e5ef2-106">(For qualitative tests, the **Type** field on the **Tests** page is set to *Option*.)</span></span>

<span data-ttu-id="e5ef2-107">Sie verwenden die Seite **Testvariablen**, um die möglichen Ergebnisse für eine Testvariable, die mit einem qualitativen Test verbunden ist, festzulegen, zu bearbeiten und anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-107">You use the **Test variables** page to set up, edit, and view the possible outcomes for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="e5ef2-108">Für jedes Ergebnis weisen Sie einen Ergebnisstatus von entweder *Bestanden* oder *Nicht bestanden* zu, um anzugeben, ob der Test bestanden oder nicht bestanden ist, wenn dieses Ergebnis als Testergebnis ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-108">For each outcome, you assign an outcome status of either *Pass* or *Fail* to indicate whether the test is passed or failed when that outcome is selected as a test result.</span></span> <span data-ttu-id="e5ef2-109">Sie verwenden die Seite **Testgruppen**, um einem einzelnen qualitativen Test eine Testvariable und ein Standard-Ergebnis dafür zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-109">You use the **Test groups** page to assign a test variable and a default outcome for it to an individual qualitative test.</span></span>

<span data-ttu-id="e5ef2-110">Wir empfehlen, für jede Testvariable mindestens zwei Ergebnisse zu definieren: eines, das den Ergebnisstatus *Bestanden* hat, und eines, das den Ergebnisstatus *Nicht bestanden* hat.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-110">For every test variable, we recommend that you define at least two outcomes: one that has an outcome status of *Pass* and one that has an outcome status of *Fail*.</span></span> <span data-ttu-id="e5ef2-111">Es gibt keine Begrenzung für die Gesamtzahl der Variablen oder Ergebnisse, die definiert werden können.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-111">There is no limit on the total number of variables or outcomes that can be defined.</span></span> <span data-ttu-id="e5ef2-112">Außerdem können mehrere Tests dieselben Testvariablen verwenden, um die Ergebnisse zu daten.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-112">Additionally, multiple tests can use the same test variables to record results.</span></span>

## <a name="examples-of-test-variables"></a><span data-ttu-id="e5ef2-113">Beispiele für Prüfvariablen</span><span class="sxs-lookup"><span data-stu-id="e5ef2-113">Examples of test variables</span></span>

### <a name="example-1"></a><span data-ttu-id="e5ef2-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e5ef2-114">Example 1</span></span>

<span data-ttu-id="e5ef2-115">Eine produzierende Firma führt zwei Tests an hergestellten Materialien durch.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-115">A manufacturing company performs two tests on manufactured materials.</span></span> <span data-ttu-id="e5ef2-116">In einem Test ist der pH-Wert mit einem Farbstreifen verbunden.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-116">In one test, the pH level is associated with a color strip.</span></span> <span data-ttu-id="e5ef2-117">Akzeptable pH-Werte sind in helleren Farben dargestellt, inakzeptable pH-Werte in dunkleren Farben.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-117">Acceptable pH levels are in lighter colors, and unacceptable pH levels are in darker colors.</span></span> <span data-ttu-id="e5ef2-118">In einem anderen Test werden mehrere visuelle Inspektionen durchgeführt, und die Arbeitskräfte der Qualitätsabteilung entscheiden anhand ihres Urteils, ob das Element die visuelle Inspektion besteht oder nicht.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-118">In another test, multiple visual inspections are performed, and quality workers use their judgement to determine whether the item passes or fails the visual inspection.</span></span>

### <a name="example-2"></a><span data-ttu-id="e5ef2-119">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e5ef2-119">Example 2</span></span>

<span data-ttu-id="e5ef2-120">Ein Unternehmen, das Kekse herstellt, führt einen Prüftest bezüglich des fertigen Produkts aus.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-120">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="e5ef2-121">Diese Abnahmeprüfung besitzt mehrere Variablen.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-121">This inspection test has several variables.</span></span> <span data-ttu-id="e5ef2-122">Eine Variable ist der Geschmack, und die möglichen Ergebnisse für ihn sind gut und schlecht.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-122">One variable is taste, and the possible outcomes for it are good and bad.</span></span> <span data-ttu-id="e5ef2-123">Eine zweite Variable ist die Farbe, und die möglichen Ergebnisse für sie sind zu dunkel, zu hell und korrekt.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-123">A second variable is color, and the possible outcomes for it are too dark, too light, and correct.</span></span>

## <a name="create-a-test-variable"></a><span data-ttu-id="e5ef2-124">Eine Testvariable erstellen</span><span class="sxs-lookup"><span data-stu-id="e5ef2-124">Create a test variable</span></span>

<span data-ttu-id="e5ef2-125">Führen Sie diese Schritte aus, um eine Testvariable zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-125">Follow these steps to create a test variable.</span></span>

1. <span data-ttu-id="e5ef2-126">Gehen Sie zu **Bestandsverwaltung \> Einrichten \> Qualitätskontrolle \> Testvariablen**.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-126">Go to **Inventory management \> Setup \> Quality control \> Test variables**.</span></span>
1. <span data-ttu-id="e5ef2-127">Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Zeile zum Raster hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-127">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="e5ef2-128">Legen Sie für die neue Zeile die folgenden Felder fest:</span><span class="sxs-lookup"><span data-stu-id="e5ef2-128">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="e5ef2-129">**Variable** – Geben Sie eine eindeutige ID oder einen Namen für die Variable ein.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-129">**Variable** – Enter a unique ID or name for the variable.</span></span>
    - <span data-ttu-id="e5ef2-130">**Beschreibung** – Geben Sie eine detaillierte Beschreibung der Variablen ein.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-130">**Description** – Enter a detailed description of the variable.</span></span>

1. <span data-ttu-id="e5ef2-131">Während die neue Zeile noch markiert ist, wählen Sie **Ergebnisse** im Aktivitätsbereich.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-131">While the new row is still selected, select **Outcomes** on the Action Pane.</span></span>
1. <span data-ttu-id="e5ef2-132">Wählen Sie auf der Seite **Test variable Ergebnisse** im Aktivitätsbereich **Neu**, um dem Raster eine Zeile hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-132">On the **Test variable outcomes** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="e5ef2-133">Legen Sie für die neue Zeile die folgenden Felder fest:</span><span class="sxs-lookup"><span data-stu-id="e5ef2-133">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="e5ef2-134">**Ergebnis** – Geben Sie eine eindeutige ID oder einen Namen für das Ergebnis ein.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-134">**Outcome** – Enter a unique ID or name for the outcome.</span></span>
    - <span data-ttu-id="e5ef2-135">**Beschreibung** – Geben Sie eine detaillierte Beschreibung des Ergebnisses ein.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-135">**Description** – Enter a detailed description of the outcome.</span></span>
    - <span data-ttu-id="e5ef2-136">**Ergebnisstatus** – Wählen Sie entweder *Bestanden* oder *Nicht bestanden*, um anzugeben, ob der Test bestanden oder nicht bestanden ist, wenn das Ergebnis als Testergebnis ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-136">**Outcome status** – Select either *Pass* or *Fail* to indicate whether the test is passed or failed when the outcome is selected as a test result.</span></span>

1. <span data-ttu-id="e5ef2-137">Wiederholen Sie den vorherigen Schritt für jedes zusätzliche Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-137">Repeat the previous step for each additional outcome.</span></span> <span data-ttu-id="e5ef2-138">Stellen Sie sicher, dass mindestens ein Ergebnis den Status *Pass* und mindestens ein Ergebnis den Status *Fail* hat.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-138">Make sure that at least one outcome has an outcome status of *Pass* and at least one has an outcome status of *Fail*.</span></span>
1. <span data-ttu-id="e5ef2-139">Schließen Sie die Seiten.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-139">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e5ef2-140">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e5ef2-140">Additional resources</span></span>

- [<span data-ttu-id="e5ef2-141">Qualitätsmanagement Testinstrumente</span><span class="sxs-lookup"><span data-stu-id="e5ef2-141">Quality management test instruments</span></span>](quality-test-instruments.md)
- [<span data-ttu-id="e5ef2-142">Qualitätsmanagement-Tests</span><span class="sxs-lookup"><span data-stu-id="e5ef2-142">Quality management tests</span></span>](quality-tests.md)
- [<span data-ttu-id="e5ef2-143">Qualitätsmanagement Testgruppen</span><span class="sxs-lookup"><span data-stu-id="e5ef2-143">Quality management test groups</span></span>](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
