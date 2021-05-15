---
title: Qualitätsmanagement-Tests
description: Dieses Thema beschreibt, wie Sie Tests erstellen, die für Qualitätsprüfungsaufträge in Microsoft Dynamics 365 Supply Chain Management verwendet werden können.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: b88011f486b6582db4727b85d021868899c6abe1
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956668"
---
# <a name="quality-management-tests"></a><span data-ttu-id="82c0b-103">Qualitätsmanagement-Tests</span><span class="sxs-lookup"><span data-stu-id="82c0b-103">Quality management tests</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="82c0b-104">Dieses Thema beschreibt, wie Sie Tests erstellen, die für Qualitätsprüfungsaufträge in Microsoft Dynamics 365 Supply Chain Management verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="82c0b-104">This topic describes how to create tests that can be used for quality orders in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="82c0b-105">Sie verwenden die Seite **Tests**, um die einzelnen Tests zu definieren und anzuzeigen, die bestimmen, ob Ihre Produkte die Qualitätsspezifikationen erfüllen.</span><span class="sxs-lookup"><span data-stu-id="82c0b-105">You use the **Tests** page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="82c0b-106">Einzelne Tests können einer Testgruppe zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="82c0b-106">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="82c0b-107">In diesem Fall werden auch testspezifische Informationen (beispielsweise die zulässigen Messwerte) angegeben.</span><span class="sxs-lookup"><span data-stu-id="82c0b-107">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="82c0b-108">Messwerte werden für quantitative Tests verwendet.</span><span class="sxs-lookup"><span data-stu-id="82c0b-108">Measurement values are used for quantitative tests.</span></span> <span data-ttu-id="82c0b-109">Für qualitative Tests werden Testvariablen verwendet.</span><span class="sxs-lookup"><span data-stu-id="82c0b-109">For qualitative tests, test variables are used.</span></span>

- <span data-ttu-id="82c0b-110">Für quantitative Tests wird das Feld **Typ** auf *Ganzzahl* oder *Bruch* festgelegt.</span><span class="sxs-lookup"><span data-stu-id="82c0b-110">For quantitative tests, the **Type** field is set to *Integer* or *Fraction*.</span></span> <span data-ttu-id="82c0b-111">Außerdem wird eine Maßeinheit angegeben.</span><span class="sxs-lookup"><span data-stu-id="82c0b-111">A unit of measure is also specified.</span></span> <span data-ttu-id="82c0b-112">Qualitätsangaben und Testergebnisse werden in Zahlen ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="82c0b-112">Quality specifications and test results are expressed as numbers.</span></span>
- <span data-ttu-id="82c0b-113">Für qualitative Tests wird das Feld **Typ** auf *Option* festgelegt.</span><span class="sxs-lookup"><span data-stu-id="82c0b-113">For qualitative tests, the **Type** field is set to *Option*.</span></span> <span data-ttu-id="82c0b-114">Qualitative Tests erfordern zusätzliche Informationen über die zu messende Variable und die zugehörigen Optionen.</span><span class="sxs-lookup"><span data-stu-id="82c0b-114">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="82c0b-115">Qualitätsangaben und Testergebnisse werden gemäß einem Ergebnis ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="82c0b-115">Quality specifications and test results are expressed according to an outcome.</span></span>

<span data-ttu-id="82c0b-116">Sie können einem Test optional ein Testinstrument zuweisen.</span><span class="sxs-lookup"><span data-stu-id="82c0b-116">You can optionally assign a test instrument to a test.</span></span> <span data-ttu-id="82c0b-117">Für das Erstellen und Verwenden von Tests mit Qualitätsprüfungsaufträgen sind jedoch keine Testinstrumente erforderlich.</span><span class="sxs-lookup"><span data-stu-id="82c0b-117">However, test instruments aren't required to create and use tests with quality orders.</span></span> <span data-ttu-id="82c0b-118">Weitere Informationen finden Sie unter [Qualitätsmanagement Prüfmittel](quality-test-instruments.md).</span><span class="sxs-lookup"><span data-stu-id="82c0b-118">For more information, see [Quality management test instruments](quality-test-instruments.md).</span></span>

<span data-ttu-id="82c0b-119">Sie können auch optional eine Einheit für einen Test angeben, um die Maßeinheit anzugeben, in der die Testergebnisse gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="82c0b-119">You can also optionally specify a unit for a test, to indicate the unit of measure that test results are recorded in.</span></span> <span data-ttu-id="82c0b-120">Zum Beispiel könnte ein Test für Temperatur eine Einheit von entweder Grad Fahrenheit oder Grad Celsius enthalten.</span><span class="sxs-lookup"><span data-stu-id="82c0b-120">For example, a test for temperature might include a unit of either degrees Fahrenheit or degrees Celsius.</span></span>

## <a name="example-of-a-test"></a><span data-ttu-id="82c0b-121">Beispiel für einen Test</span><span class="sxs-lookup"><span data-stu-id="82c0b-121">Example of a test</span></span>

<span data-ttu-id="82c0b-122">Eine produzierende Firma führt zwei Tests an gekauftem Material durch: einen quantitativen Test auf Materialqualität und einen qualitativen Test auf Verpackungsschäden.</span><span class="sxs-lookup"><span data-stu-id="82c0b-122">A manufacturing company performs two tests on purchased material: a quantitative test for material quality and a qualitative test for packaging damage.</span></span> <span data-ttu-id="82c0b-123">Die Firma gibt zusätzliche Informationen über den qualitativen Test an, um die Testvariable (z. B. beschädigte Verpackung) und ihre Ergebnisse zu definieren.</span><span class="sxs-lookup"><span data-stu-id="82c0b-123">The company specifies additional information about the qualitative test to define the test variable (for example, damaged packaging) and its outcomes.</span></span> <span data-ttu-id="82c0b-124">Auf der Seite **Testgruppen** werden die beiden Tests einer Testgruppe zugeordnet und die testspezifischen Informationen angegeben.</span><span class="sxs-lookup"><span data-stu-id="82c0b-124">The company uses the **Test groups** page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="82c0b-125">Die Testgruppe wird einem Qualitätsprüfungsauftrag zugeordnet, damit die Firma Testergebnisse für die beiden Tests melden kann.</span><span class="sxs-lookup"><span data-stu-id="82c0b-125">The test group is assigned to a quality order so that the company can report test results for the two tests.</span></span>

## <a name="create-a-test"></a><span data-ttu-id="82c0b-126">Einen Test erstellen</span><span class="sxs-lookup"><span data-stu-id="82c0b-126">Create a test</span></span>

<span data-ttu-id="82c0b-127">Folgen Sie diesen Schritten, um einen Test zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="82c0b-127">Follow these steps to create a test.</span></span>

1. <span data-ttu-id="82c0b-128">Gehen Sie zu **Bestandsverwaltung \> Einrichten \> Qualitätskontrolle \> Tests**.</span><span class="sxs-lookup"><span data-stu-id="82c0b-128">Go to **Inventory management \> Setup \> Quality control \> Tests**.</span></span>
1. <span data-ttu-id="82c0b-129">Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Zeile zum Raster hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="82c0b-129">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="82c0b-130">Legen Sie für die neue Zeile die folgenden Felder fest:</span><span class="sxs-lookup"><span data-stu-id="82c0b-130">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="82c0b-131">**Test** – Geben Sie eine eindeutige ID oder einen Namen für den Test ein.</span><span class="sxs-lookup"><span data-stu-id="82c0b-131">**Test** – Enter a unique ID or name for the test.</span></span>
    - <span data-ttu-id="82c0b-132">**Beschreibung** – Geben Sie eine detaillierte Beschreibung des Tests ein.</span><span class="sxs-lookup"><span data-stu-id="82c0b-132">**Description** – Enter a detailed description of the test.</span></span>
    - <span data-ttu-id="82c0b-133">**Typ** – Wählen Sie die Art der Ergebnisse, die der Test erzeugt.</span><span class="sxs-lookup"><span data-stu-id="82c0b-133">**Type** – Select the type of results that the test produces.</span></span> <span data-ttu-id="82c0b-134">Für quantitative Tests wählen Sie *Bruch* oder *Ganzzahl*.</span><span class="sxs-lookup"><span data-stu-id="82c0b-134">For quantitative tests, select *Fraction* or *Integer*.</span></span> <span data-ttu-id="82c0b-135">Wählen Sie für qualitative Tests *Option*.</span><span class="sxs-lookup"><span data-stu-id="82c0b-135">For qualitative tests, select *Option*.</span></span>
    - <span data-ttu-id="82c0b-136">**Testgerät** – Wählen Sie ein [Testgerät](quality-test-instruments.md), das für den Test verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="82c0b-136">**Test instrument** – Select a [test instrument](quality-test-instruments.md) that should be used for the test.</span></span>
    - <span data-ttu-id="82c0b-137">**Einheit** – Wenn Sie *Bruch* oder *Ganzzahl* im Feld **Typ** gewählt haben (d.h. wenn es sich um einen quantitativen Test handelt), wählen Sie die Maßeinheit, in der die Testergebnisse gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="82c0b-137">**Unit** – If you selected *Fraction* or *Integer* in the **Type** field (that is, if the test is a quantitative test), select the unit of measure that test results should be recorded in.</span></span>

1. <span data-ttu-id="82c0b-138">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="82c0b-138">Close the page.</span></span>

> [!NOTE]
> <span data-ttu-id="82c0b-139">Nachdem Sie einen Test gespeichert haben, können Sie das Feld **Typ** im Raster nicht mehr bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="82c0b-139">After you save a test, you can no longer edit the **Type** field in the grid.</span></span> <span data-ttu-id="82c0b-140">Wenn Sie die Art der Testergebnisse, die für einen Test aufgezeichnet werden sollen, ändern müssen, wählen Sie **Qualitätstesttyp ändern** im Aktivitätsbereich.</span><span class="sxs-lookup"><span data-stu-id="82c0b-140">If you must change the type of test results that will be recorded for a test, select **Change quality test type** on the Action Pane.</span></span> <span data-ttu-id="82c0b-141">Legen Sie im Dialogfeld **Qualitätstesttyp ändern** das Feld **Neuer Typ** auf den gewünschten Typ fest und wählen Sie dann **OK**, um das Dialogfeld zu schließen.</span><span class="sxs-lookup"><span data-stu-id="82c0b-141">In the **Change quality test type** dialog box, set the **New type** field to the desired type, and then select **OK** to close the dialog box.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="82c0b-142">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="82c0b-142">Additional resources</span></span>

- [<span data-ttu-id="82c0b-143">Qualitätsmanagement Testinstrumente</span><span class="sxs-lookup"><span data-stu-id="82c0b-143">Quality management test instruments</span></span>](quality-test-instruments.md)
- [<span data-ttu-id="82c0b-144">Qualitätsmanagement Testgruppen</span><span class="sxs-lookup"><span data-stu-id="82c0b-144">Quality management test groups</span></span>](quality-test-groups.md)
- [<span data-ttu-id="82c0b-145">Qualitätsmanagement-Testvariablen</span><span class="sxs-lookup"><span data-stu-id="82c0b-145">Quality management test variables</span></span>](quality-test-variables.md)
- [<span data-ttu-id="82c0b-146">Qualitätszuordnungen</span><span class="sxs-lookup"><span data-stu-id="82c0b-146">Quality associations</span></span>](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
