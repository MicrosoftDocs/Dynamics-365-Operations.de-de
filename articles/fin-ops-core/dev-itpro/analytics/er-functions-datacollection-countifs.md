---
title: COUNTIFS EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung von COUNTIFS bei der elektronischen Berichterstellungsfunktion (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a28e2dd263c3f2cabd1c07c4aba8dfb22db01cc4
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745656"
---
# <a name="countifs-er-function"></a><span data-ttu-id="2489b-103">COUNTIFS EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="2489b-103">COUNTIFS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2489b-104">Die Funktion `COUNTIFS` gibt den Wert *Integer* zurück, der die Anzahl der Formatelemente darstellt, die erfasst wurden, als die Formatelemente zum Generieren eines ausgehenden Dokuments während der Formatausführung verwendet wurden, und der die angegebenen Bedingungen erfüllt.</span><span class="sxs-lookup"><span data-stu-id="2489b-104">The `COUNTIFS` function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="2489b-105">Jede Bedingung besteht aus einem Schlüsselbereich und einem Schlüsselwert.</span><span class="sxs-lookup"><span data-stu-id="2489b-105">Each condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="2489b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="2489b-106">Syntax</span></span>

```vb
COUNTIFS (condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a><span data-ttu-id="2489b-107">Argumente</span><span class="sxs-lookup"><span data-stu-id="2489b-107">Arguments</span></span>

<span data-ttu-id="2489b-108">`condition 1 range`: *String*</span><span class="sxs-lookup"><span data-stu-id="2489b-108">`condition 1 range`: *String*</span></span>

<span data-ttu-id="2489b-109">Ein Wert, der von dem Ausdruck zurückgegeben wird, der in der Eigenschaft **Gesammelter Datenschlüsselname** einer Komponente im elektronischen Berichterstellungsformat konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="2489b-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of an Electronic reporting (ER) format component.</span></span> <span data-ttu-id="2489b-110">Dieses Argument ist obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="2489b-110">This argument is mandatory.</span></span>

<span data-ttu-id="2489b-111">`condition 1 value`: *String*</span><span class="sxs-lookup"><span data-stu-id="2489b-111">`condition 1 value`: *String*</span></span>

<span data-ttu-id="2489b-112">Ein Wert, der von dem Ausdruck zurückgegeben wird, der in der Eigenschaft **Gesammelter Datenschlüsselwert** einer Komponente im elektronischen Berichterstellungsformat konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="2489b-112">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="2489b-113">Dieses Argument ist obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="2489b-113">This argument is mandatory.</span></span>

<span data-ttu-id="2489b-114">`condition N range`: *String*</span><span class="sxs-lookup"><span data-stu-id="2489b-114">`condition N range`: *String*</span></span>

<span data-ttu-id="2489b-115">Ein Wert, der von dem Ausdruck zurückgegeben wird, der in der Eigenschaft **Gesammelter Datenschlüsselname** einer Komponente im elektronischen Berichterstellungsformat konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="2489b-115">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="2489b-116">Diese zusätzlichen Argumente sind optional.</span><span class="sxs-lookup"><span data-stu-id="2489b-116">These additional arguments are optional.</span></span>

<span data-ttu-id="2489b-117">`condition N value`: *String*</span><span class="sxs-lookup"><span data-stu-id="2489b-117">`condition N value`: *String*</span></span>

<span data-ttu-id="2489b-118">Ein Wert, der von dem Ausdruck zurückgegeben wird, der in der Eigenschaft **Gesammelter Datenschlüsselwert** einer Komponente im elektronischen Berichterstellungsformat konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="2489b-118">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="2489b-119">Diese zusätzlichen Argumente sind optional.</span><span class="sxs-lookup"><span data-stu-id="2489b-119">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="2489b-120">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="2489b-120">Return values</span></span>

<span data-ttu-id="2489b-121">*Ganze Zahl*</span><span class="sxs-lookup"><span data-stu-id="2489b-121">*Integer*</span></span>

<span data-ttu-id="2489b-122">Der resultierende numerische Wert.</span><span class="sxs-lookup"><span data-stu-id="2489b-122">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="2489b-123">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="2489b-123">Usage notes</span></span>

<span data-ttu-id="2489b-124">Die Eigenschaften **Gesammelter Datenschlüsselname** und **Gesammelter Datenschlüsselwert** können entweder für die Komponente **Reihenfolge** oder die Komponente **XML-Element** eines EB-Formats konfiguriert werden, das sich unter der Komponente **Allgemeine\\Datei** befindet, in der die Option **Ausgabendetails sammeln** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="2489b-124">The **Collected data key name** and **Collected data key value** properties can be configured for either the **Sequence** component or the **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="2489b-125">Diese Funktion gibt den Wert **0** (null) zurück, wenn die Option **Ausgabedetails sammeln** der aktiven Komponente **Allgemeine\\Datei** deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="2489b-125">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="2489b-126">In `condition range`-Argumenten können Platzhalterzeichen **"\*"** verwendet werden, um mehrere beliebige Zeichen darzustellen.</span><span class="sxs-lookup"><span data-stu-id="2489b-126">In `condition range` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="2489b-127">In `condition value`-Argumenten können Platzhalterzeichen **"\*"** verwendet werden, um mehrere beliebige Zeichen darzustellen.</span><span class="sxs-lookup"><span data-stu-id="2489b-127">In `condition value` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="2489b-128">Beispiel</span><span class="sxs-lookup"><span data-stu-id="2489b-128">Example</span></span>

<span data-ttu-id="2489b-129">Um mehr darüber zu erfahren, wie diese Funktion verwendet wird, finden Sie Informationen im Aufgabenleitfaden [EB – Verwendung von Daten der Formatausgabe für Inventur und Summierungen](tasks/er-format-counting-summing-1.md), der Teil des Geschäftsprozesses **IT-Dienstleistungs-/-Lösungskomponenten anschaffen/entwickeln** ist.</span><span class="sxs-lookup"><span data-stu-id="2489b-129">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2489b-130">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="2489b-130">Additional resources</span></span>

[<span data-ttu-id="2489b-131">Datensammlungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="2489b-131">Data collection functions</span></span>](er-functions-category-data-collection.md)
