---
title: SUMIFS EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung von SUMIFS bei der elektronischen Berichterstellungsfunktion (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9d9ef51f3c8cb090f940670c4c3afae104268ed
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687961"
---
# <a name="sumifs-er-function"></a><span data-ttu-id="cde62-103">SUMIFS EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="cde62-103">SUMIFS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cde62-104">Die Funktion `SUMIFS` gibt den Wert *Real* zurück, der die Summe der Werte darstellt, die bei Bindungen der Formatelemente zurückgegeben und erfasst wurden, als die Formatelemente zum Generieren eines ausgehenden Dokuments während der Formatausführung verwendet wurden, und der die angegebenen Bedingungen erfüllt.</span><span class="sxs-lookup"><span data-stu-id="cde62-104">The `SUMIFS` function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="cde62-105">Jede Bedingung besteht aus einem Schlüsselbereich und einem Schlüsselwert.</span><span class="sxs-lookup"><span data-stu-id="cde62-105">Each condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="cde62-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="cde62-106">Syntax</span></span>

```vb
SUMIFS (key name for summing, condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a><span data-ttu-id="cde62-107">Argumente</span><span class="sxs-lookup"><span data-stu-id="cde62-107">Arguments</span></span>

<span data-ttu-id="cde62-108">`key name for summing`: *String*</span><span class="sxs-lookup"><span data-stu-id="cde62-108">`key name for summing`: *String*</span></span>

<span data-ttu-id="cde62-109">Ein Wert, der von dem Ausdruck zurückgegeben wird, der in der Eigenschaft **Gesammelter Datenschlüsselname** der Formatkomponente der elektronischen Berichterstattung (EB) konfiguriert wurde, für die der Wert der Bindung zu Summierungszwecken verwendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="cde62-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of the Electronic reporting (ER) format component for which the value of the binding must be used for summing purposes.</span></span>

<span data-ttu-id="cde62-110">Die Eigenschaft **Gesammelter Datenschlüsselname** kann entweder für die Komponente **Numerisch** oder die Komponente **String** eines EB-Formats konfiguriert werden, das sich unter der Komponente **Allgemeine\\Datei** befindet, in der die Option **Ausgabendetails sammeln** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="cde62-110">The **Collected data key name** property can be configured for either a **Numeric** component or a **String** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="cde62-111">`condition 1 range`: *String*</span><span class="sxs-lookup"><span data-stu-id="cde62-111">`condition 1 range`: *String*</span></span>

<span data-ttu-id="cde62-112">Ein Wert, der von dem Ausdruck zurückgegeben wird, der in der Eigenschaft **Gesammelter Datenschlüsselname** einer Komponente im elektronischen Berichterstellungsformat konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="cde62-112">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="cde62-113">Dieses Argument ist obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="cde62-113">This argument is mandatory.</span></span>

<span data-ttu-id="cde62-114">Die Eigenschaft **Gesammelter Datenschlüsselname** kann entweder für die Komponente **Reichenfolge** oder die Komponente **XML-Element** eines EB-Formats konfiguriert werden, das sich unter der Komponente **Allgemeine\\Datei** befindet, in der die Option **Ausgabendetails sammeln** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="cde62-114">The **Collected data key name** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="cde62-115">`condition 1 value`: *String*</span><span class="sxs-lookup"><span data-stu-id="cde62-115">`condition 1 value`: *String*</span></span>

<span data-ttu-id="cde62-116">Ein Wert, der von dem Ausdruck zurückgegeben wird, der in der Eigenschaft **Gesammelter Datenschlüsselwert** einer Komponente im elektronischen Berichterstellungsformat konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="cde62-116">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="cde62-117">Dieses Argument ist obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="cde62-117">This argument is mandatory.</span></span>

<span data-ttu-id="cde62-118">Die Eigenschaft **Gesammelter Datenschlüsselwert** kann entweder für die Komponente **Reichenfolge** oder die Komponente **XML-Element** eines EB-Formats konfiguriert werden, das sich unter der Komponente **Allgemeine\\Datei** befindet, in der die Option **Ausgabendetails sammeln** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="cde62-118">The **Collected data key value** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="cde62-119">`condition N range`: *String*</span><span class="sxs-lookup"><span data-stu-id="cde62-119">`condition N range`: *String*</span></span>

<span data-ttu-id="cde62-120">Ein Wert, der von dem Ausdruck zurückgegeben wird, der in der Eigenschaft **Gesammelter Datenschlüsselname** einer Komponente im elektronischen Berichterstellungsformat konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="cde62-120">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="cde62-121">Diese zusätzlichen Argumente sind optional.</span><span class="sxs-lookup"><span data-stu-id="cde62-121">These additional arguments are optional.</span></span>

<span data-ttu-id="cde62-122">Die Eigenschaft **Gesammelter Datenschlüsselname** kann entweder für die Komponente **Reichenfolge** oder die Komponente **XML-Element** eines EB-Formats konfiguriert werden, das sich unter der Komponente **Allgemeine\\Datei** befindet, in der die Option **Ausgabendetails sammeln** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="cde62-122">The **Collected data key name** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="cde62-123">`condition N value`: *String*</span><span class="sxs-lookup"><span data-stu-id="cde62-123">`condition N value`: *String*</span></span>

<span data-ttu-id="cde62-124">Ein Wert, der von dem Ausdruck zurückgegeben wird, der in der Eigenschaft **Gesammelter Datenschlüsselwert** einer Komponente im elektronischen Berichterstellungsformat konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="cde62-124">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="cde62-125">Diese zusätzlichen Argumente sind optional.</span><span class="sxs-lookup"><span data-stu-id="cde62-125">These additional arguments are optional.</span></span>

<span data-ttu-id="cde62-126">Die Eigenschaft **Gesammelter Datenschlüsselwert** kann entweder für die Komponente **Reichenfolge** oder die Komponente **XML-Element** eines EB-Formats konfiguriert werden, das sich unter der Komponente **Allgemeine\\Datei** befindet, in der die Option **Ausgabendetails sammeln** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="cde62-126">The **Collected data key value** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="return-values"></a><span data-ttu-id="cde62-127">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="cde62-127">Return values</span></span>

<span data-ttu-id="cde62-128">*Gleitkommazahl*</span><span class="sxs-lookup"><span data-stu-id="cde62-128">*Real*</span></span>

<span data-ttu-id="cde62-129">Der resultierende numerische Wert.</span><span class="sxs-lookup"><span data-stu-id="cde62-129">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="cde62-130">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="cde62-130">Usage notes</span></span>

<span data-ttu-id="cde62-131">Diese Funktion gibt den Wert **0** (null) zurück, wenn die Option **Ausgabedetails sammeln** der aktiven Komponente **Allgemeine\\Datei** deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="cde62-131">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="cde62-132">In `condition range`-Argumenten können Platzhalterzeichen **"\*"** verwendet werden, um mehrere beliebige Zeichen darzustellen.</span><span class="sxs-lookup"><span data-stu-id="cde62-132">In the `condition range` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="cde62-133">In `condition value`-Argumenten können Platzhalterzeichen **"\*"** verwendet werden, um mehrere beliebige Zeichen darzustellen.</span><span class="sxs-lookup"><span data-stu-id="cde62-133">In the `condition value` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="cde62-134">Beispiel</span><span class="sxs-lookup"><span data-stu-id="cde62-134">Example</span></span>

<span data-ttu-id="cde62-135">Um mehr darüber zu erfahren, wie diese Funktion verwendet wird, finden Sie Informationen im Aufgabenleitfaden [EB – Verwendung von Daten der Formatausgabe für Inventur und Summierungen](tasks/er-format-counting-summing-1.md), der Teil des Geschäftsprozesses **IT-Dienstleistungs-/-Lösungskomponenten anschaffen/entwickeln** ist.</span><span class="sxs-lookup"><span data-stu-id="cde62-135">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cde62-136">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="cde62-136">Additional resources</span></span>

[<span data-ttu-id="cde62-137">Datensammlungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="cde62-137">Data collection functions</span></span>](er-functions-category-data-collection.md)
