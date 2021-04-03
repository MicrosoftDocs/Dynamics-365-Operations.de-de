---
title: SUMIFS EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung von SUMIFS bei der elektronischen Berichterstellungsfunktion (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: ff5ad3371a6e18ca1a3ee855e3b35f51f7513ef0
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564758"
---
# <a name="sumifs-er-function"></a><span data-ttu-id="cff6b-103">SUMIFS EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="cff6b-103">SUMIFS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cff6b-104">Die Funktion `SUMIFS` gibt den Wert *Real* zurück, der die Summe der Werte darstellt, die bei Bindungen der Formatelemente zurückgegeben und erfasst wurden, als die Formatelemente zum Generieren eines ausgehenden Dokuments während der Formatausführung verwendet wurden, und der die angegebenen Bedingungen erfüllt.</span><span class="sxs-lookup"><span data-stu-id="cff6b-104">The `SUMIFS` function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="cff6b-105">Jede Bedingung besteht aus einem Schlüsselbereich und einem Schlüsselwert.</span><span class="sxs-lookup"><span data-stu-id="cff6b-105">Each condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="cff6b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="cff6b-106">Syntax</span></span>

```vb
SUMIFS (key name for summing, condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a><span data-ttu-id="cff6b-107">Argumente</span><span class="sxs-lookup"><span data-stu-id="cff6b-107">Arguments</span></span>

<span data-ttu-id="cff6b-108">`key name for summing`: *String*</span><span class="sxs-lookup"><span data-stu-id="cff6b-108">`key name for summing`: *String*</span></span>

<span data-ttu-id="cff6b-109">Ein Wert, der von dem Ausdruck zurückgegeben wird, der in der Eigenschaft **Gesammelter Datenschlüsselname** der Formatkomponente der elektronischen Berichterstattung (EB) konfiguriert wurde, für die der Wert der Bindung zu Summierungszwecken verwendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="cff6b-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of the Electronic reporting (ER) format component for which the value of the binding must be used for summing purposes.</span></span>

<span data-ttu-id="cff6b-110">Die Eigenschaft **Gesammelter Datenschlüsselname** kann entweder für die Komponente **Numerisch** oder die Komponente **String** eines EB-Formats konfiguriert werden, das sich unter der Komponente **Allgemeine\\Datei** befindet, in der die Option **Ausgabendetails sammeln** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="cff6b-110">The **Collected data key name** property can be configured for either a **Numeric** component or a **String** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="cff6b-111">`condition 1 range`: *String*</span><span class="sxs-lookup"><span data-stu-id="cff6b-111">`condition 1 range`: *String*</span></span>

<span data-ttu-id="cff6b-112">Ein Wert, der von dem Ausdruck zurückgegeben wird, der in der Eigenschaft **Gesammelter Datenschlüsselname** einer Komponente im elektronischen Berichterstellungsformat konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="cff6b-112">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="cff6b-113">Dieses Argument ist obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="cff6b-113">This argument is mandatory.</span></span>

<span data-ttu-id="cff6b-114">Die Eigenschaft **Gesammelter Datenschlüsselname** kann entweder für die Komponente **Reichenfolge** oder die Komponente **XML-Element** eines EB-Formats konfiguriert werden, das sich unter der Komponente **Allgemeine\\Datei** befindet, in der die Option **Ausgabendetails sammeln** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="cff6b-114">The **Collected data key name** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="cff6b-115">`condition 1 value`: *String*</span><span class="sxs-lookup"><span data-stu-id="cff6b-115">`condition 1 value`: *String*</span></span>

<span data-ttu-id="cff6b-116">Ein Wert, der von dem Ausdruck zurückgegeben wird, der in der Eigenschaft **Gesammelter Datenschlüsselwert** einer Komponente im elektronischen Berichterstellungsformat konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="cff6b-116">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="cff6b-117">Dieses Argument ist obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="cff6b-117">This argument is mandatory.</span></span>

<span data-ttu-id="cff6b-118">Die Eigenschaft **Gesammelter Datenschlüsselwert** kann entweder für die Komponente **Reichenfolge** oder die Komponente **XML-Element** eines EB-Formats konfiguriert werden, das sich unter der Komponente **Allgemeine\\Datei** befindet, in der die Option **Ausgabendetails sammeln** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="cff6b-118">The **Collected data key value** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="cff6b-119">`condition N range`: *String*</span><span class="sxs-lookup"><span data-stu-id="cff6b-119">`condition N range`: *String*</span></span>

<span data-ttu-id="cff6b-120">Ein Wert, der von dem Ausdruck zurückgegeben wird, der in der Eigenschaft **Gesammelter Datenschlüsselname** einer Komponente im elektronischen Berichterstellungsformat konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="cff6b-120">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="cff6b-121">Diese zusätzlichen Argumente sind optional.</span><span class="sxs-lookup"><span data-stu-id="cff6b-121">These additional arguments are optional.</span></span>

<span data-ttu-id="cff6b-122">Die Eigenschaft **Gesammelter Datenschlüsselname** kann entweder für die Komponente **Reichenfolge** oder die Komponente **XML-Element** eines EB-Formats konfiguriert werden, das sich unter der Komponente **Allgemeine\\Datei** befindet, in der die Option **Ausgabendetails sammeln** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="cff6b-122">The **Collected data key name** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="cff6b-123">`condition N value`: *String*</span><span class="sxs-lookup"><span data-stu-id="cff6b-123">`condition N value`: *String*</span></span>

<span data-ttu-id="cff6b-124">Ein Wert, der von dem Ausdruck zurückgegeben wird, der in der Eigenschaft **Gesammelter Datenschlüsselwert** einer Komponente im elektronischen Berichterstellungsformat konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="cff6b-124">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="cff6b-125">Diese zusätzlichen Argumente sind optional.</span><span class="sxs-lookup"><span data-stu-id="cff6b-125">These additional arguments are optional.</span></span>

<span data-ttu-id="cff6b-126">Die Eigenschaft **Gesammelter Datenschlüsselwert** kann entweder für die Komponente **Reichenfolge** oder die Komponente **XML-Element** eines EB-Formats konfiguriert werden, das sich unter der Komponente **Allgemeine\\Datei** befindet, in der die Option **Ausgabendetails sammeln** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="cff6b-126">The **Collected data key value** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="return-values"></a><span data-ttu-id="cff6b-127">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="cff6b-127">Return values</span></span>

<span data-ttu-id="cff6b-128">*Gleitkommazahl*</span><span class="sxs-lookup"><span data-stu-id="cff6b-128">*Real*</span></span>

<span data-ttu-id="cff6b-129">Der resultierende numerische Wert.</span><span class="sxs-lookup"><span data-stu-id="cff6b-129">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="cff6b-130">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="cff6b-130">Usage notes</span></span>

<span data-ttu-id="cff6b-131">Diese Funktion gibt den Wert **0** (null) zurück, wenn die Option **Ausgabedetails sammeln** der aktiven Komponente **Allgemeine\\Datei** deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="cff6b-131">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="cff6b-132">In `condition range`-Argumenten können Platzhalterzeichen **"\*"** verwendet werden, um mehrere beliebige Zeichen darzustellen.</span><span class="sxs-lookup"><span data-stu-id="cff6b-132">In the `condition range` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="cff6b-133">In `condition value`-Argumenten können Platzhalterzeichen **"\*"** verwendet werden, um mehrere beliebige Zeichen darzustellen.</span><span class="sxs-lookup"><span data-stu-id="cff6b-133">In the `condition value` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="cff6b-134">Beispiel</span><span class="sxs-lookup"><span data-stu-id="cff6b-134">Example</span></span>

<span data-ttu-id="cff6b-135">Um mehr darüber zu erfahren, wie diese Funktion verwendet wird, finden Sie Informationen im Aufgabenleitfaden [EB – Verwendung von Daten der Formatausgabe für Inventur und Summierungen](tasks/er-format-counting-summing-1.md), der Teil des Geschäftsprozesses **IT-Dienstleistungs-/-Lösungskomponenten anschaffen/entwickeln** ist.</span><span class="sxs-lookup"><span data-stu-id="cff6b-135">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cff6b-136">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="cff6b-136">Additional resources</span></span>

[<span data-ttu-id="cff6b-137">Datensammlungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="cff6b-137">Data collection functions</span></span>](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]