---
title: Berechnungen für Produktkonfigurationsmodelle
description: In diesem Thema wird beschrieben, wie Sie Berechnungen für Attribute in einem Produktkonfigurationsmodell erstellen
author: t-benebo
ms.date: 03/18/2021
ms.topic: article
ms.search.form: PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-03-18
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: eaf6264f060d33575740ad38e7a65158baba296b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829617"
---
# <a name="product-configuration-model-calculations"></a><span data-ttu-id="d0d0b-103">Berechnungen für Produktkonfigurationsmodelle</span><span class="sxs-lookup"><span data-stu-id="d0d0b-103">Product configuration model calculations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d0d0b-104">In diesem Thema wird beschrieben, wie Sie Berechnungen für Attribute in einem Produktkonfigurationsmodell erstellen.</span><span class="sxs-lookup"><span data-stu-id="d0d0b-104">This topic describes how to create calculations for attributes in a product configuration model.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d0d0b-105">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="d0d0b-105">Prerequisites</span></span>

<span data-ttu-id="d0d0b-106">Berechnungen werden in einem Produktkonfigurationsmodell verwendet, um die Konfigurationswerte für ein Produkt zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="d0d0b-106">Calculations are used in a product configuration model to calculate the configuration values for a product.</span></span> <span data-ttu-id="d0d0b-107">Bevor Sie mit dem Einrichten von Berechnungen beginnen können, muss das zugehörige Produktkonfigurationsmodell vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="d0d0b-107">Before you can start to set up calculations, the related product configuration model must exist.</span></span> <span data-ttu-id="d0d0b-108">Eine Übersicht über den Einrichtungsprozess für Konfigurationsmodelle und die damit verbundenen Aufgaben finden Sie unter [Produktkonfigurationsmodell einrichten](set-up-maintain-product-configuration-model.md).</span><span class="sxs-lookup"><span data-stu-id="d0d0b-108">For an overview of the setup process for configuration models and the related tasks, see [Set up a product configuration model](set-up-maintain-product-configuration-model.md).</span></span>

## <a name="create-a-calculation"></a><span data-ttu-id="d0d0b-109">Eine Berechnung erstellen</span><span class="sxs-lookup"><span data-stu-id="d0d0b-109">Create a calculation</span></span>

<span data-ttu-id="d0d0b-110">Eine Berechnung besteht aus einem Ausdruck und einem Zielattribut.</span><span class="sxs-lookup"><span data-stu-id="d0d0b-110">A calculation consists of an expression and a target attribute.</span></span> <span data-ttu-id="d0d0b-111">Weitere Informationen finden Sie unter [Berechnungen für Produktkonfigurationsmodelle, FAQ](calculate-product-configuration-models.md).</span><span class="sxs-lookup"><span data-stu-id="d0d0b-111">For more information, see [Calculations for product configuration models FAQ](calculate-product-configuration-models.md).</span></span>

<span data-ttu-id="d0d0b-112">Gehen Sie wie folgt vor, um eine Berechnung für ein vorhandenes Produktmodell zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d0d0b-112">To create a calculation for an existing product model, follow these steps.</span></span>

1. <span data-ttu-id="d0d0b-113">Gehen Sie zu **Produktinformationsverwaltung \> Allgemein \> Produktkonfigurationsmodelle**.</span><span class="sxs-lookup"><span data-stu-id="d0d0b-113">Go to **Product information management \> Common \> Product configuration models**.</span></span>
1. <span data-ttu-id="d0d0b-114">Öffnen Sie ein Konfigurationsmodell und wählen Sie anschließend **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="d0d0b-114">Open a product configuration model, and then select **Edit**.</span></span>
1. <span data-ttu-id="d0d0b-115">Wählen Sie auf dem Inforegister **Berechnungen** **Hinzufügen**, um eine Berechnung hinzuzufügen, und legen Sie dann die folgenden Felder fest:</span><span class="sxs-lookup"><span data-stu-id="d0d0b-115">On the **Calculations** FastTab, select **Add** to add a calculation, and then set the following fields:</span></span>

    - <span data-ttu-id="d0d0b-116">**Name** – Geben Sie einen Namen für die Berechnung ein.</span><span class="sxs-lookup"><span data-stu-id="d0d0b-116">**Name** – Enter a name for the calculation.</span></span>
    - <span data-ttu-id="d0d0b-117">**Beschreibung** – Geben Sie eine Beschreibung für die Berechnung ein.</span><span class="sxs-lookup"><span data-stu-id="d0d0b-117">**Description** – Enter a description of the calculation.</span></span>
    - <span data-ttu-id="d0d0b-118">**Zielattribut** – Wählen Sie das Attribut aus, für das Sie die Berechnung erstellen.</span><span class="sxs-lookup"><span data-stu-id="d0d0b-118">**Target attribute** – Select the attribute that you're making the calculation for.</span></span>

1. <span data-ttu-id="d0d0b-119">Wählen Sie **Ausdruck bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="d0d0b-119">Select **Edit expression**.</span></span>
1. <span data-ttu-id="d0d0b-120">Fügen Sie im Dialogfeld **Eine Berechnung eingeben** dem Ausdruck die erforderlichen Attribute, Operatoren und Werte hinzu.</span><span class="sxs-lookup"><span data-stu-id="d0d0b-120">In the **Enter a calculation** dialog box, add the required attributes, operators, and values to the expression.</span></span> <span data-ttu-id="d0d0b-121">Weitere Informationen zum Arbeiten mit diesen Elementen finden Sie unter [Ausdruckseinschränkungen und Tabelleneinschränkungen in Produktkonfigurationsmodellen](expression-constraints-table-constraints-product-configuration-models.md).</span><span class="sxs-lookup"><span data-stu-id="d0d0b-121">For more information about how to work with these elements, see [Expression constraints and table constraints in product configuration models](expression-constraints-table-constraints-product-configuration-models.md).</span></span>
1. <span data-ttu-id="d0d0b-122">Wenn Ihr Ausdruck fertig ist, wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0d0b-122">When your expression is ready, select **OK**.</span></span>

## <a name="calculation-examples"></a><span data-ttu-id="d0d0b-123">Berechnungsbeispiele</span><span class="sxs-lookup"><span data-stu-id="d0d0b-123">Calculation examples</span></span>

<span data-ttu-id="d0d0b-124">Dieser Abschnitt enthält einige Beispiele, die zeigen, wie Berechnungen funktionieren.</span><span class="sxs-lookup"><span data-stu-id="d0d0b-124">This section provides a few examples that show how calculations work.</span></span>

### <a name="example-1"></a><span data-ttu-id="d0d0b-125">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d0d0b-125">Example 1</span></span>

<span data-ttu-id="d0d0b-126">Das Zielattribut ist vom booleschen Typ und die Berechnung verwendet den folgenden Bedingungsausdruck:</span><span class="sxs-lookup"><span data-stu-id="d0d0b-126">The target attribute is Boolean, and the calculation uses the following conditional expression:</span></span>

`If[(decimalAttribute1 / decimalAttribute2) < 1, True, False]`

<span data-ttu-id="d0d0b-127">Dieser Ausdruck gibt dem Zielattribut den Wert *Wahr* zurück, wenn `decimalAttribute2` größer oder gleich `decimalAttribute1` ist.</span><span class="sxs-lookup"><span data-stu-id="d0d0b-127">This expression returns a value of *True* to the target attribute if `decimalAttribute2` is greater than or equal to `decimalAttribute1`.</span></span> <span data-ttu-id="d0d0b-128">Andernfalls gibt sie den Wert *falsch* zurück.</span><span class="sxs-lookup"><span data-stu-id="d0d0b-128">Otherwise, it returns a value of *False*.</span></span>

### <a name="example-2"></a><span data-ttu-id="d0d0b-129">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d0d0b-129">Example 2</span></span>

<span data-ttu-id="d0d0b-130">In diesem Beispiel wird das Textattribut `textFixedList` als Zielattribut verwendet.</span><span class="sxs-lookup"><span data-stu-id="d0d0b-130">This example uses the text attribute `textFixedList` as the target attribute.</span></span> <span data-ttu-id="d0d0b-131">Dieses Attribut enthält die folgende feste Liste.</span><span class="sxs-lookup"><span data-stu-id="d0d0b-131">This attribute contains the following fixed list.</span></span>

| <span data-ttu-id="d0d0b-132">Wert</span><span class="sxs-lookup"><span data-stu-id="d0d0b-132">Value</span></span> | <span data-ttu-id="d0d0b-133">Solver-Wert</span><span class="sxs-lookup"><span data-stu-id="d0d0b-133">Solver value</span></span> |
|---|---|
| <span data-ttu-id="d0d0b-134">K</span><span class="sxs-lookup"><span data-stu-id="d0d0b-134">A</span></span> | <span data-ttu-id="d0d0b-135">1a</span><span class="sxs-lookup"><span data-stu-id="d0d0b-135">1a</span></span> |
| <span data-ttu-id="d0d0b-136">Mrd</span><span class="sxs-lookup"><span data-stu-id="d0d0b-136">B</span></span> | <span data-ttu-id="d0d0b-137">2b</span><span class="sxs-lookup"><span data-stu-id="d0d0b-137">2b</span></span> |
| <span data-ttu-id="d0d0b-138">C</span><span class="sxs-lookup"><span data-stu-id="d0d0b-138">C</span></span> | <span data-ttu-id="d0d0b-139">2c</span><span class="sxs-lookup"><span data-stu-id="d0d0b-139">2c</span></span> |

<span data-ttu-id="d0d0b-140">Der folgende Screenshot zeigt, wie die Einstellungen für dieses Attribut in Ihrem System aussehen könnten.</span><span class="sxs-lookup"><span data-stu-id="d0d0b-140">The following screenshot shows how the settings for this attribute might look in your system.</span></span>

<span data-ttu-id="d0d0b-141">![Attributtypeinstellungen für Beispiel 2](media/model-calculations-example2.png "Attributtypeinstellungen für Beispiel 2")</span><span class="sxs-lookup"><span data-stu-id="d0d0b-141">![Attribute type settings for example 2](media/model-calculations-example2.png "Attribute type settings for example 2")</span></span>

<span data-ttu-id="d0d0b-142">Das Attribut wird in der folgenden Bedingungsanweisung verwendet:</span><span class="sxs-lookup"><span data-stu-id="d0d0b-142">The attribute is used in the following conditional statement:</span></span>

`If[integerAttribute < 150, 0, 2]`

<span data-ttu-id="d0d0b-143">Wenn `integerAttribute` kleiner ist als 150, gibt diese Anweisung den Textwert des ersten Datensatzes in der festen Liste zurück – *A*. Andernfalls wird der Textwert des dritten Datensatzes in der festen Liste zurückgegeben – *C*.</span><span class="sxs-lookup"><span data-stu-id="d0d0b-143">If `integerAttribute` is less than 150, this statement returns the text value of the first record in the fixed list, *A*. Otherwise, it returns the text value of the third record in the fixed list, *C*.</span></span>

> [!NOTE]
> <span data-ttu-id="d0d0b-144">Die feste Liste entspricht einer auf Null basierenden Aufzählung (enum). Auf ihre Werte wird über den entsprechenden Ganzzahlwert zugegriffen.</span><span class="sxs-lookup"><span data-stu-id="d0d0b-144">The fixed list is equivalent to a zero-based enumeration (enum), and its values are accessed by the appropriate integer value.</span></span> <span data-ttu-id="d0d0b-145">Daher wird der erste Wert der festen Liste (*A*) *0* zugeordnet, der zweite Wert (*B*) *1* und der dritte Wert (*C*) *2*.</span><span class="sxs-lookup"><span data-stu-id="d0d0b-145">Therefore, the first fixed list value (*A*) is matched to *0*, the second value (*B*) is matched to *1*, and the third value (*C*) is matched to *2*.</span></span>

### <a name="example-3"></a><span data-ttu-id="d0d0b-146">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="d0d0b-146">Example 3</span></span>

<span data-ttu-id="d0d0b-147">In diesem Beispiel wird das Zielattribut `textFixedList` aus dem letzten Beispiel verwendet.</span><span class="sxs-lookup"><span data-stu-id="d0d0b-147">This example uses the `textFixedList` target attribute from the previous example.</span></span> <span data-ttu-id="d0d0b-148">Es wird auch ein anderes Textattribut verwendet, `textAttribute`, das die folgende feste Liste enthält.</span><span class="sxs-lookup"><span data-stu-id="d0d0b-148">It also uses another text attribute, `textAttribute`, that contains the following fixed list.</span></span>

| <span data-ttu-id="d0d0b-149">Wert</span><span class="sxs-lookup"><span data-stu-id="d0d0b-149">Value</span></span> | <span data-ttu-id="d0d0b-150">Solver-Wert</span><span class="sxs-lookup"><span data-stu-id="d0d0b-150">Solver value</span></span> |
|---|---|
| <span data-ttu-id="d0d0b-151">AA</span><span class="sxs-lookup"><span data-stu-id="d0d0b-151">AA</span></span> | <span data-ttu-id="d0d0b-152">1aa</span><span class="sxs-lookup"><span data-stu-id="d0d0b-152">1aa</span></span> |
| <span data-ttu-id="d0d0b-153">BB</span><span class="sxs-lookup"><span data-stu-id="d0d0b-153">BB</span></span> | <span data-ttu-id="d0d0b-154">2bb</span><span class="sxs-lookup"><span data-stu-id="d0d0b-154">2bb</span></span> |

<span data-ttu-id="d0d0b-155">Der folgende Screenshot zeigt, wie die Einstellungen für dieses Attribut in Ihrem System aussehen könnten.</span><span class="sxs-lookup"><span data-stu-id="d0d0b-155">The following screenshot shows how the settings for this attribute might look in your system.</span></span>

<span data-ttu-id="d0d0b-156">![Attributtypeinstellungen für Beispiel 3](media/model-calculations-example3.png "Attributtypeinstellungen für Beispiel 3")</span><span class="sxs-lookup"><span data-stu-id="d0d0b-156">![Attribute type settings for example 3](media/model-calculations-example3.png "Attribute type settings for example 3")</span></span>

<span data-ttu-id="d0d0b-157">Der Wert für das Attribut `textFixedList` wird unter Verwendung der folgenden Bedingungsanweisung berechnet:</span><span class="sxs-lookup"><span data-stu-id="d0d0b-157">The value for the `textFixedList` attribute is calculated by using the following conditional statement:</span></span>

`If[textAttribute == "1aa", 0, 2]`

<span data-ttu-id="d0d0b-158">Wenn der Wert `textAttribute` einen Solver-Wert hat, der *1aa* entspricht, gibt dieser Ausdruck den Textwert des ersten Datensatzes in der festen Liste `textFixedList` zurück – *A*. Andernfalls wird der Textwert des dritten Datensatzes in der festen Liste `textFixedList` zurückgegeben – *C*.</span><span class="sxs-lookup"><span data-stu-id="d0d0b-158">If the `textAttribute` value has a solver value that equals *1aa*, this expression returns the text value of the first record in the `textFixedList` fixed list, *A*. Otherwise, it returns the text value of the third record in the `textFixedList` fixed list, *C*.</span></span>

> [!NOTE]
> - <span data-ttu-id="d0d0b-159">Die Bedingungsanweisung muss den Solver-Wert des Attributs verwenden.</span><span class="sxs-lookup"><span data-stu-id="d0d0b-159">The conditional statement must use the solver value of the attribute.</span></span>
> - <span data-ttu-id="d0d0b-160">Bei Berechnungen können nur Textattribute mit fester Liste verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d0d0b-160">Only fixed-list text attributes can be used in calculations.</span></span>

## <a name="see-also"></a><span data-ttu-id="d0d0b-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d0d0b-161">See also</span></span>

- [<span data-ttu-id="d0d0b-162">Berechnungen für Produktkonfigurationsmodelle, FAQ</span><span class="sxs-lookup"><span data-stu-id="d0d0b-162">Calculations for product configuration models FAQ</span></span>](calculate-product-configuration-models.md)
- [<span data-ttu-id="d0d0b-163">Einem Produktkonfigurationsmodell eine Ausdruckseinschränkung hinzufügen</span><span class="sxs-lookup"><span data-stu-id="d0d0b-163">Add an expression constraint to a product configuration model</span></span>](tasks/add-expression-constraint-product-configuration-model.md)
- [<span data-ttu-id="d0d0b-164">Produktkonfigurationsmodelle – Überblick</span><span class="sxs-lookup"><span data-stu-id="d0d0b-164">Product configuration models overview</span></span>](product-configuration-models.md)
