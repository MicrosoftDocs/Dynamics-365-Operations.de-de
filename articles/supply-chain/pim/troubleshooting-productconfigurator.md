---
title: Behebung von Problemen mit dem Produktkonfigurator
description: In diesem Thema wird beschrieben, wie Sie Probleme beheben, die bei der Arbeit mit dem Produktkonfigurator auftreten können.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: e6cfeb6a2b4166dfa9a5a5cc1b7d3d913b865ce2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999605"
---
# <a name="troubleshoot-the-product-configurator"></a><span data-ttu-id="a8730-103">Behebung von Problemen mit dem Produktkonfigurator</span><span class="sxs-lookup"><span data-stu-id="a8730-103">Troubleshoot the product configurator</span></span>

<span data-ttu-id="a8730-104">In diesem Thema wird beschrieben, wie Sie Probleme beheben, die bei der Arbeit mit dem Produktkonfigurator auftreten können.</span><span class="sxs-lookup"><span data-stu-id="a8730-104">This topic describes how to fix issues that you might encounter while you work with the product configurator.</span></span>

## <a name="item-text-is-overwritten-when-i-configure-a-product-on-a-sales-order-line"></a><span data-ttu-id="a8730-105">Element-Text wird überschrieben, wenn ich ein Produkt in einer Zeile eines Verkaufsauftrags konfiguriere.</span><span class="sxs-lookup"><span data-stu-id="a8730-105">Item text is overwritten when I configure a product on a sales order line.</span></span>

### <a name="issue-description"></a><span data-ttu-id="a8730-106">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="a8730-106">Issue description</span></span>

<span data-ttu-id="a8730-107">Dieses Problem tritt auf, wenn Sie eine Verkaufsauftragszeile für einen konfigurierbaren Artikel erstellen und dann den Artikeltext ändern.</span><span class="sxs-lookup"><span data-stu-id="a8730-107">This issue occurs when you create a sales order line for a configurable item and then modify the item text.</span></span> <span data-ttu-id="a8730-108">Wenn Sie den Artikel konfigurieren und dann **OK** wählen, wird der Text mit dem Standardtext überschrieben.</span><span class="sxs-lookup"><span data-stu-id="a8730-108">When you configure the item and then select **OK**, the text is overwritten with the standard text.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="a8730-109">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="a8730-109">Issue resolution</span></span>

<span data-ttu-id="a8730-110">Dieses Verhalten wird erwartet.</span><span class="sxs-lookup"><span data-stu-id="a8730-110">This behavior is expected.</span></span> <span data-ttu-id="a8730-111">Das Textfeld enthält den Variantennamen, der erst ausgefüllt wird, nachdem Sie die Zeile konfiguriert haben.</span><span class="sxs-lookup"><span data-stu-id="a8730-111">The text field includes the variant name, which is filled in only after you configure the line.</span></span> <span data-ttu-id="a8730-112">Daher müssen Sie den Text ändern, nachdem Sie die Zeile konfiguriert haben, nicht vorher.</span><span class="sxs-lookup"><span data-stu-id="a8730-112">Therefore, you must change the text after you've configured the line, not before.</span></span>

## <a name="integer-attributes-are-incorrectly-rounded-when-product-configuration-models-are-calculated"></a><span data-ttu-id="a8730-113">Ganzzahlige Attribute werden bei der Berechnung von Produktkonfigurationsmodellen falsch gerundet.</span><span class="sxs-lookup"><span data-stu-id="a8730-113">Integer attributes are incorrectly rounded when product configuration models are calculated.</span></span>

### <a name="issue-description"></a><span data-ttu-id="a8730-114">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="a8730-114">Issue description</span></span>

<span data-ttu-id="a8730-115">Dieses Problem kann auftreten, wenn Sie die folgende Reihe von Aktionen durchführen:</span><span class="sxs-lookup"><span data-stu-id="a8730-115">This issue can occur when you perform the following series of actions:</span></span>

1. <span data-ttu-id="a8730-116">Legen Sie die folgenden Attribute in einem Produktkonfigurationsmodell fest:</span><span class="sxs-lookup"><span data-stu-id="a8730-116">Set up the following attributes on a production configuration model:</span></span>

    - <span data-ttu-id="a8730-117">Eingabe (ganzzahlig)</span><span class="sxs-lookup"><span data-stu-id="a8730-117">Input (integer)</span></span>
    - <span data-ttu-id="a8730-118">Prozentsatz (dezimal)</span><span class="sxs-lookup"><span data-stu-id="a8730-118">Percent (decimal)</span></span>
    - <span data-ttu-id="a8730-119">Ergebnis (ganzzahlig)</span><span class="sxs-lookup"><span data-stu-id="a8730-119">Result (integer)</span></span>

2. <span data-ttu-id="a8730-120">Erstellen Sie eine Formel, die den folgenden Ausdruck hat:</span><span class="sxs-lookup"><span data-stu-id="a8730-120">Create a calculation that has the following expression:</span></span>

    <span data-ttu-id="a8730-121">*Ergebnis* = *Eingabe* × *Prozent* ÷ 100</span><span class="sxs-lookup"><span data-stu-id="a8730-121">*Result* = *Input* × *Percent* ÷ 100</span></span>

<span data-ttu-id="a8730-122">In diesem Fall wird das ganzzahlige Ergebnis nicht immer korrekt gerundet.</span><span class="sxs-lookup"><span data-stu-id="a8730-122">In this case, the integer result isn't always correctly rounded.</span></span> <span data-ttu-id="a8730-123">Zum Beispiel ist die Eingabe 1.000, und der Prozentsatz ist 2,40.</span><span class="sxs-lookup"><span data-stu-id="a8730-123">For example, the input is 1,000, and the percentage is 2.40.</span></span> <span data-ttu-id="a8730-124">Daher erwarten Sie, dass das ganzzahlige Ergebnis 24 ist, denn 2,40 Prozent von 1.000 ist 24 (oder 24,00 in dezimaler Form).</span><span class="sxs-lookup"><span data-stu-id="a8730-124">Therefore, you expect the integer result to be 24, because 2.40 percent of 1,000 is 24 (or 24.00 in decimal form).</span></span> <span data-ttu-id="a8730-125">Stattdessen wird das Ergebnis als 23 angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a8730-125">Instead, the result is shown as 23.</span></span> <span data-ttu-id="a8730-126">Wenn der Prozentsatz jedoch 2,39 beträgt, wird die Berechnung auf 24 anstelle von 23 gerundet.</span><span class="sxs-lookup"><span data-stu-id="a8730-126">However, when the percentage is 2.39, the calculation is rounded to 24 instead of 23.</span></span> <span data-ttu-id="a8730-127">Wenn der Prozentsatz 2,50 beträgt, wird die Berechnung wie erwartet auf 25 gerundet.</span><span class="sxs-lookup"><span data-stu-id="a8730-127">When the percentage is 2.50, the calculation is rounded to 25, as expected.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="a8730-128">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="a8730-128">Issue resolution</span></span>

<span data-ttu-id="a8730-129">Dieses Problem tritt aufgrund der Art und Weise auf, wie Microsoft Solver Foundation intern Zahlen unter Verwendung von Brüchen darstellt.</span><span class="sxs-lookup"><span data-stu-id="a8730-129">This issue occurs because of the way that Microsoft Solver Foundation internally represents numbers by using fractions.</span></span> <span data-ttu-id="a8730-130">Im vorangegangenen Beispiel wird das Ergebnis der Berechnung, bei der der Prozentsatz 2,40 beträgt, als 27021597764222975 ÷ 1125899906842624 = 23,99999999999999911182158029987476766109466552734375 dargestellt.</span><span class="sxs-lookup"><span data-stu-id="a8730-130">For the preceding example, the result of the calculation where the percentage is 2.40 is represented as 27021597764222975 ÷ 1125899906842624 = 23.99999999999999911182158029987476766109466552734375.</span></span> <span data-ttu-id="a8730-131">Wenn .NET diesen Wert in eine Ganzzahl umwandelt, wird 23 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a8730-131">When .NET casts this value as an integer, it will return 23.</span></span>

<span data-ttu-id="a8730-132">Dieses Verhalten wird nicht geändert, da andere Szenarien davon abhängen.</span><span class="sxs-lookup"><span data-stu-id="a8730-132">This behavior won't be changed, because other scenarios depend on it.</span></span> <span data-ttu-id="a8730-133">Für das vorangegangene Beispiel können Sie das Problem beheben, indem Sie ein zusätzliches Dezimalattribut und eine Berechnung einführen.</span><span class="sxs-lookup"><span data-stu-id="a8730-133">For the preceding example, you can fix the issue by introducing an additional decimal attribute and a calculation.</span></span>

<span data-ttu-id="a8730-134">Sie können zum Beispiel die folgenden Attribute in einem Produktionskonfigurationsmodell festlegen:</span><span class="sxs-lookup"><span data-stu-id="a8730-134">For example, you can set up the following attributes on a production configuration model:</span></span>

- <span data-ttu-id="a8730-135">Eingabe (ganzzahlig)</span><span class="sxs-lookup"><span data-stu-id="a8730-135">Input (integer)</span></span>
- <span data-ttu-id="a8730-136">Prozentsatz (dezimal)</span><span class="sxs-lookup"><span data-stu-id="a8730-136">Percent (decimal)</span></span>
- <span data-ttu-id="a8730-137">ResultDecimal (dezimal)</span><span class="sxs-lookup"><span data-stu-id="a8730-137">ResultDecimal (decimal)</span></span>
- <span data-ttu-id="a8730-138">ResultInteger (ganzzahlig)</span><span class="sxs-lookup"><span data-stu-id="a8730-138">ResultInteger (integer)</span></span>

<span data-ttu-id="a8730-139">Sie können dann die folgenden Berechnungen hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="a8730-139">You can then add the following calculations:</span></span>

- <span data-ttu-id="a8730-140">*ResultDecimal* = *Eingabe* × *Prozent* ÷ 100</span><span class="sxs-lookup"><span data-stu-id="a8730-140">*ResultDecimal* = *Input* × *Percent* ÷ 100</span></span>
- <span data-ttu-id="a8730-141">*ResultInteger* = *ResultDecimal*</span><span class="sxs-lookup"><span data-stu-id="a8730-141">*ResultInteger* = *ResultDecimal*</span></span>
