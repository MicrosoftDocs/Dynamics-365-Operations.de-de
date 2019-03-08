---
title: Materialentnahme berechnen
description: Dieser Artikel enthält Informationen zu unterschiedlichen Optionen, die in Zusammenhang mit der Berechnung des Materialverbrauchs stehen.
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMDesignerEditBOM, BOMTable, ProdBOM
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 53401
ms.assetid: 9cff88e4-0425-4707-9178-3c2cb10df7c2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3e4010b5abb6b5a871d098422f1489cb2db3a071
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "316187"
---
# <a name="calculate-material-consumption"></a><span data-ttu-id="6e6d5-103">Materialentnahme berechnen</span><span class="sxs-lookup"><span data-stu-id="6e6d5-103">Calculate material consumption</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6e6d5-104">Dieser Artikel enthält Informationen zu unterschiedlichen Optionen, die in Zusammenhang mit der Berechnung des Materialverbrauchs stehen.</span><span class="sxs-lookup"><span data-stu-id="6e6d5-104">This article provides information about various options that are related to the calculation of material consumption.</span></span> 

<span data-ttu-id="6e6d5-105">Die folgenden Optionen, die mit der Berechnung des Materialverbrauchs zusammenhängen, sind auf den Registerkarten **Einstellungen** und **Verbrauch pro Schritt** auf dem Inforegister **Positionsdetails** der Seite **Stücklisten** verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6e6d5-105">The following options that are related to the calculation of material consumption are available on the **Setup** and **Step consumption** tabs on the **Line details** FastTab of the **Bill of materials** page.</span></span>

## <a name="variable-and-constant-consumption"></a><span data-ttu-id="6e6d5-106">Variabler und konstanter Verbrauch</span><span class="sxs-lookup"><span data-stu-id="6e6d5-106">Variable and constant consumption</span></span>
<span data-ttu-id="6e6d5-107">Im Feld **Verbrauch** können Sie auswählen, ob der Verbrauch auf konstanten Mengen oder auf variablen Mengen berechnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6e6d5-107">In the **Consumption is** field, you can select whether consumption should be calculated as a constant quantity or a variable quantity.</span></span> <span data-ttu-id="6e6d5-108">Wählen Sie **Konstant**  wenn eine feste Menge oder ein festes Volumen benötigt wird, und zwar unabhängig von der produzierten Menge.</span><span class="sxs-lookup"><span data-stu-id="6e6d5-108">Select **Constant** if a fixed quantity or volume is required for the production, regardless of the quantity that is produced.</span></span> <span data-ttu-id="6e6d5-109">Wählen Sie **Variable** aus, was die Standardeinstellung ist, wenn die erforderliche Menge des Materials in den fertigen Waren im Verhältnis zur Anzahl der fertigen Waren steht, die produziert werden.</span><span class="sxs-lookup"><span data-stu-id="6e6d5-109">Select **Variable**, which is the default setting, if the required amount of material in the finished goods is proportional to the number of finished goods that are produced.</span></span>

## <a name="calculating-consumption-from-a-formula"></a><span data-ttu-id="6e6d5-110">Verbrauch nach einer Formel berechnen</span><span class="sxs-lookup"><span data-stu-id="6e6d5-110">Calculating consumption from a formula</span></span>
<span data-ttu-id="6e6d5-111">Im Feld **Formel** können Sie verschiedene Formeln für die Berechnung des Materialverbrauchs einrichten.</span><span class="sxs-lookup"><span data-stu-id="6e6d5-111">In the **Formula** field, you can set up various formulas for calculating material consumption.</span></span> <span data-ttu-id="6e6d5-112">Wenn Sie den Standardwert **Standard** verwenden, wird der Verbrauch nicht nach einer Formel berechnet.</span><span class="sxs-lookup"><span data-stu-id="6e6d5-112">If you use the default value, **Standard**, the consumption isn't calculated from a formula.</span></span> <span data-ttu-id="6e6d5-113">Die folgenden Formeln funktionieren zusammen mit den Feldern **Höhe**, **Breite**, **Tiefe**, **Dichte** und **Konstante**:</span><span class="sxs-lookup"><span data-stu-id="6e6d5-113">The following formulas work together with the **Height**, **Width**, **Depth**, **Density**, and **Constant** fields:</span></span>

-   <span data-ttu-id="6e6d5-114">Höhe \* Konstante</span><span class="sxs-lookup"><span data-stu-id="6e6d5-114">Height \* Constant</span></span>
-   <span data-ttu-id="6e6d5-115">Höhe \* Breite \* Konstante</span><span class="sxs-lookup"><span data-stu-id="6e6d5-115">Height \* Width \* Constant</span></span>
-   <span data-ttu-id="6e6d5-116">Höhe \* Breite \* Tiefe \* Konstante</span><span class="sxs-lookup"><span data-stu-id="6e6d5-116">Height \* Width \* Depth \* Constant</span></span>
-   <span data-ttu-id="6e6d5-117">(Höhe \* Breite \* Tiefe/Dichte) \* Konstante</span><span class="sxs-lookup"><span data-stu-id="6e6d5-117">(Height \* Width \* Depth / Density) \* Constant</span></span>

## <a name="rounding-up-and-multiples"></a><span data-ttu-id="6e6d5-118">Aufrunden und Vielfache</span><span class="sxs-lookup"><span data-stu-id="6e6d5-118">Rounding up and multiples</span></span>
<span data-ttu-id="6e6d5-119">Zusammen ermöglichen Ihnen die Felder **Aufrunden** und **Vielfache**, den Materialverbrauchswert aufzurunden.</span><span class="sxs-lookup"><span data-stu-id="6e6d5-119">Together, the **Rounding up** and **Multiples** fields let you round up the material consumption value.</span></span> <span data-ttu-id="6e6d5-120">So können Sie beispielsweise den Wert entsprechend der Handhabungseinheit aufrunden, in der das Rohmaterial für die Produktion entnommen wird.</span><span class="sxs-lookup"><span data-stu-id="6e6d5-120">For example, you can round up the value according to the handling unit in which the raw material is picked for production.</span></span> <span data-ttu-id="6e6d5-121">Die folgenden Optionen stehen im Feld **Aufrunden** zur Verfügung: **Menge**, **Messung** und **Verbrauch**.</span><span class="sxs-lookup"><span data-stu-id="6e6d5-121">The following options are available in the **Rounding up** field: **Quantity**, **Measurement**, and **Consumption**.</span></span>

### <a name="quantity"></a><span data-ttu-id="6e6d5-122">Menge</span><span class="sxs-lookup"><span data-stu-id="6e6d5-122">Quantity</span></span>

<span data-ttu-id="6e6d5-123">Wenn Sie **Menge** als Aufrundungsmechanismus auswählen, muss die Menge ein Mehrfaches der angegebenen Menge sein.</span><span class="sxs-lookup"><span data-stu-id="6e6d5-123">If you select **Quantity** as the rounding-up mechanism, the quantity must be a multiple of the specified quantity.</span></span> <span data-ttu-id="6e6d5-124">Wenn z. B. ganze Zahlen erforderlich sind, wählen Sie den Wert **1** im Feld **Vielfaches** aus.</span><span class="sxs-lookup"><span data-stu-id="6e6d5-124">For example, if whole numbers are required, select **1** in the **Multiples** field.</span></span> <span data-ttu-id="6e6d5-125">Zahlen werden dann zu einer Menge aufgerundet, die durch 1 teilbar ist.</span><span class="sxs-lookup"><span data-stu-id="6e6d5-125">Numbers are then rounded up to a quantity that is divisible by 1.</span></span>

### <a name="measurement"></a><span data-ttu-id="6e6d5-126">Verbrauchsberechnung</span><span class="sxs-lookup"><span data-stu-id="6e6d5-126">Measurement</span></span>

<span data-ttu-id="6e6d5-127">In der Regel wählen Sie **Messung** als Aufrundungsmechanismus aus, wenn das Rohmaterial in bestimmten Abmessungen geliefert wird.</span><span class="sxs-lookup"><span data-stu-id="6e6d5-127">Typically, you select **Measurement** as the rounding-up mechanism when the raw material comes in specific dimensions.</span></span> <span data-ttu-id="6e6d5-128">Beispielsweise ist ein Stück eines 2-Meter-Metallrohrs für eine fertige Ware erforderlich, und das Metallrohr wird in Längen von 4,5 Metern gelagert.</span><span class="sxs-lookup"><span data-stu-id="6e6d5-128">For example, a piece of 2-meter metal tube is required for a finished good, and the metal tube is stored in 4.5-meter lengths.</span></span> <span data-ttu-id="6e6d5-129">In diesem Fall kann der Aufrundungsmechanismus **Messung** verwendet werden, um zu berechnen, wie viele Metallrohre erforderlich sind, um eine bestimmte Stückanzahl fertige Ware zu erzeugen.</span><span class="sxs-lookup"><span data-stu-id="6e6d5-129">In this case, the **Measurement** rounding-up mechanism can be used to calculate how many metal tubes are required to produce a specific number of pieces of the finished good.</span></span> <span data-ttu-id="6e6d5-130">Bei diesem Beispiel wird das Feld **Formel** auf festgelegt **Höhen\*Konstante** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6e6d5-130">For this example, the **Formula** field is set to **Height \* Constant**.</span></span> <span data-ttu-id="6e6d5-131">Das Feld **Höhe** wird auf **2** festgelegt, um die Länge des Rohrs anzugeben, das für das Endprodukt erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="6e6d5-131">The **Height** field is set to **2** to indicate the length of the tube that is required for the finished good.</span></span> <span data-ttu-id="6e6d5-132">Das Feld **Mehrfach** wird auf **4,5** festgelegt, um anzugeben, dass das Rohr in Längen von 4,5 Metern entnommen wird.</span><span class="sxs-lookup"><span data-stu-id="6e6d5-132">The **Multiple** field is set to **4.5** to indicate that the tube is picked in lengths of 4.5 meters.</span></span> <span data-ttu-id="6e6d5-133">Hier ist die Berechnung:</span><span class="sxs-lookup"><span data-stu-id="6e6d5-133">Here is the calculation:</span></span>

1.  <span data-ttu-id="6e6d5-134">Anzahl der Vielfachen, die für 10 Stück der fertigen Ware erforderlich sind: 10 ÷ 2 = 5 Stück</span><span class="sxs-lookup"><span data-stu-id="6e6d5-134">Number of multiples that are required for 10 pieces of the finished good: 10 ÷ 2 = 5 pieces</span></span>
2.  <span data-ttu-id="6e6d5-135">Gesamtverbrauch: 4,5 × 5 = 22,5 Meter des Metallrohrs</span><span class="sxs-lookup"><span data-stu-id="6e6d5-135">Total consumption:  4.5 × 5 = 22.5 meters of metal tube</span></span>

<span data-ttu-id="6e6d5-136">Es wird angenommen, dass 0,5 Meter des Rohrs für alle fünf Stücke des Rohrs verschrottet werden, die verbraucht werden.</span><span class="sxs-lookup"><span data-stu-id="6e6d5-136">It's assumed that 0.5 meter of tube is scrapped for every five pieces of tube that are consumed.</span></span>

### <a name="consumption"></a><span data-ttu-id="6e6d5-137">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="6e6d5-137">Consumption</span></span>

<span data-ttu-id="6e6d5-138">In der Regel wählen Sie**Verbrauch** als Aufrundungsmechanismus aus, wenn Rohmaterial in gesamten Mengen einer bestimmten Handhabungseinheit des Produkts entnommen werden muss.</span><span class="sxs-lookup"><span data-stu-id="6e6d5-138">Typically, you select **Consumption** as the rounding-up mechanism when raw material must be picked in whole quantities of a specific handling unit of the product.</span></span> <span data-ttu-id="6e6d5-139">Beispielsweise werden 2 Liter Farbe verwendet, die zur Produktion einer fertigen Ware verwendet werden, und die Farbe wird in 25-Liter-Eimern entnommen.</span><span class="sxs-lookup"><span data-stu-id="6e6d5-139">For example, 2 quarts of paint are used to produce one piece of a finished good, and the paint is picked in 25-quart cans.</span></span> <span data-ttu-id="6e6d5-140">In diesem Fall kann der Aufrundungsmechanismus **Verbrauch** verwendet werden, um den Verbrauch auf ganze Anzahlen von 25-Liter-Eimern aufzurunden.</span><span class="sxs-lookup"><span data-stu-id="6e6d5-140">In this case, the **Consumption** rounding-up mechanism can be used to round up consumption to whole numbers of 25-quart cans.</span></span> <span data-ttu-id="6e6d5-141">Ist hier die Berechnung für die benötigte Farbmenge, wenn 180 Stück fertige Ware produziert werden müssen:</span><span class="sxs-lookup"><span data-stu-id="6e6d5-141">Here is the calculation for the amount of paint that is required if 180 pieces of the finished good must be produced:</span></span>

1.  <span data-ttu-id="6e6d5-142">Farbe, die erforderlich ist, abzüglich des Ausschusses: 180 × 2 = 360 Liter</span><span class="sxs-lookup"><span data-stu-id="6e6d5-142">Paint that is required, excluding scrap: 180 × 2 = 360 quarts</span></span>
2.  <span data-ttu-id="6e6d5-143">Anzahl der Farbeimer: 360 ÷ 25 = 14,4, das auf 15 aufgerundet wird</span><span class="sxs-lookup"><span data-stu-id="6e6d5-143">Number of cans: 360 ÷ 25 = 14.4, which is rounded up to 15</span></span>
3.  <span data-ttu-id="6e6d5-144">Farbe, die erforderlich ist, einschließlich des Ausschusses: 15 × 25 = 375 Liter</span><span class="sxs-lookup"><span data-stu-id="6e6d5-144">Paint that is required, including scrap: 15 × 25 = 375 quarts</span></span>

## <a name="step-consumption"></a><span data-ttu-id="6e6d5-145">Verbrauch pro Serie</span><span class="sxs-lookup"><span data-stu-id="6e6d5-145">Step consumption</span></span>
<span data-ttu-id="6e6d5-146">"Verbrauch pro Schritt" wird verwendet, um den konstanten Verbrauch in Mengenintervallen zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="6e6d5-146">Step consumption is used to calculate constant consumption in quantity intervals.</span></span> <span data-ttu-id="6e6d5-147">Wenn Sie **Verbrauch pro Schritt** im Feld **Berechnungsgrundlage** auf der Registerkarte **Einstellungen** auswählen, können Sie Informationen über die Schritte auf der Registerkarte **Verbrauch pro Schritt** hinzugefügt. Die feste verbrauchten Menge kann in die Intervalle der hergestellten Menge eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="6e6d5-147">If you select **Step consumption** in the **Formula** field on the **Setup** tab, you can add information about the steps on the **Step consumption** tab. The fixed consumed quantity can be set up in intervals of the produced quantity.</span></span> <span data-ttu-id="6e6d5-148">Beispielsweise wird der Verbrauch pro Schritt, wie in der folgenden Tabelle angezeigt, eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="6e6d5-148">For example, step consumption is set up as shown in the following table.</span></span>

| <span data-ttu-id="6e6d5-149">Von Serie</span><span class="sxs-lookup"><span data-stu-id="6e6d5-149">From series</span></span> | <span data-ttu-id="6e6d5-150">Menge</span><span class="sxs-lookup"><span data-stu-id="6e6d5-150">Quantity</span></span> |
|-------------|----------|
| <span data-ttu-id="6e6d5-151">0,00</span><span class="sxs-lookup"><span data-stu-id="6e6d5-151">0.00</span></span>        | <span data-ttu-id="6e6d5-152">10.0000</span><span class="sxs-lookup"><span data-stu-id="6e6d5-152">10.0000</span></span>  |
| <span data-ttu-id="6e6d5-153">100,00</span><span class="sxs-lookup"><span data-stu-id="6e6d5-153">100.00</span></span>      | <span data-ttu-id="6e6d5-154">20.0000</span><span class="sxs-lookup"><span data-stu-id="6e6d5-154">20.0000</span></span>  |
| <span data-ttu-id="6e6d5-155">200,00</span><span class="sxs-lookup"><span data-stu-id="6e6d5-155">200.00</span></span>      | <span data-ttu-id="6e6d5-156">40.0000</span><span class="sxs-lookup"><span data-stu-id="6e6d5-156">40.0000</span></span>  |

<span data-ttu-id="6e6d5-157">Die Stücklistenmenge (BOM) ist 1 und die Produktionsmenge ist 110.</span><span class="sxs-lookup"><span data-stu-id="6e6d5-157">The bill of materials (BOM) quantity is 1, and the production quantity is 110.</span></span> <span data-ttu-id="6e6d5-158">Die Formel für den Verbrauch ist "Von Serien (Menge) = Verbrauch.</span><span class="sxs-lookup"><span data-stu-id="6e6d5-158">The formula for the consumption is From series (Quantity) = Consumption.</span></span> <span data-ttu-id="6e6d5-159">Da die Produktionsmenge 110 ist, fällt sie in die "Von-100-Serie".</span><span class="sxs-lookup"><span data-stu-id="6e6d5-159">Because the production quantity is 110, it falls into the "From 100 series."</span></span> <span data-ttu-id="6e6d5-160">Die Menge ist daher 20.</span><span class="sxs-lookup"><span data-stu-id="6e6d5-160">Therefore, the quantity is 20.</span></span>



