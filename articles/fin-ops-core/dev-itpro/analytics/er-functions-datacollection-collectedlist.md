---
title: COLLECTEDLIST EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung von COLLECTEDLIST bei der elektronischen Berichterstellungsfunktion (EB) bereitgestellt.
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
ms.openlocfilehash: 8a66ba364a7d06cd5ac03b57f07e2c5d4eb7a46d
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042595"
---
# <span data-ttu-id="18912-103"><a name="COLLECTEDLIST">COLLECTEDLIST EB-Funktion</a></span><span class="sxs-lookup"><span data-stu-id="18912-103"><a name="COLLECTEDLIST">COLLECTEDLIST ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="18912-104">Dies Funktion `COLLECTEDLIST` gibt den Wert *Datensatzliste* zurück, der die Liste der Werte enthält, die von der Eigenschaft **Gesammelter Datenschlüsselwert** des Formatelements zurückgegeben und erfasst wurden, als die Formatelemente zum Generieren ausgehender Dokumente während der Formatausführung verwendet wurden, und der die angegebenen Bedingungen erfüllt.</span><span class="sxs-lookup"><span data-stu-id="18912-104">The `COLLECTEDLIST` function a *Record list* value that contains the list of values that were returned by the **Collected data key value** property of format elements and collected when the format elements were used to generate outbound documents during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="18912-105">Jede Bedingung besteht aus einem Schlüsselbereich und einem Schlüsselwert.</span><span class="sxs-lookup"><span data-stu-id="18912-105">Each condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="18912-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="18912-106">Syntax</span></span>

```vb
COLLECTEDLIST (condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a><span data-ttu-id="18912-107">Argumente</span><span class="sxs-lookup"><span data-stu-id="18912-107">Arguments</span></span>

<span data-ttu-id="18912-108">`condition 1 range`: *String*</span><span class="sxs-lookup"><span data-stu-id="18912-108">`condition 1 range`: *String*</span></span>

<span data-ttu-id="18912-109">Ein Wert, der von dem Ausdruck zurückgegeben wird, der in der Eigenschaft **Gesammelter Datenschlüsselname** einer Komponente im elektronischen Berichterstellungsformat konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="18912-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of an Electronic reporting (ER) format component.</span></span> <span data-ttu-id="18912-110">Dieses Argument ist obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="18912-110">This argument is mandatory.</span></span>

<span data-ttu-id="18912-111">`condition 1 value`: *String*</span><span class="sxs-lookup"><span data-stu-id="18912-111">`condition 1 value`: *String*</span></span>

<span data-ttu-id="18912-112">Ein Wert, der von dem Ausdruck zurückgegeben wird, der in der Eigenschaft **Gesammelter Datenschlüsselwert** einer Komponente im elektronischen Berichterstellungsformat konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="18912-112">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="18912-113">Dieses Argument ist obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="18912-113">This argument is mandatory.</span></span>

<span data-ttu-id="18912-114">`condition N range`: *String*</span><span class="sxs-lookup"><span data-stu-id="18912-114">`condition N range`: *String*</span></span>

<span data-ttu-id="18912-115">Ein Wert, der von dem Ausdruck zurückgegeben wird, der in der Eigenschaft **Gesammelter Datenschlüsselname** einer Komponente im elektronischen Berichterstellungsformat konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="18912-115">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="18912-116">Diese zusätzlichen Argumente sind optional.</span><span class="sxs-lookup"><span data-stu-id="18912-116">These additional arguments are optional.</span></span>

<span data-ttu-id="18912-117">`condition N value`: *String*</span><span class="sxs-lookup"><span data-stu-id="18912-117">`condition N value`: *String*</span></span>

<span data-ttu-id="18912-118">Ein Wert, der von dem Ausdruck zurückgegeben wird, der in der Eigenschaft **Gesammelter Datenschlüsselwert** einer Komponente im elektronischen Berichterstellungsformat konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="18912-118">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="18912-119">Diese zusätzlichen Argumente sind optional.</span><span class="sxs-lookup"><span data-stu-id="18912-119">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="18912-120">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="18912-120">Return values</span></span>

<span data-ttu-id="18912-121">*Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="18912-121">*Record list*</span></span>

<span data-ttu-id="18912-122">Die resultierende Liste der Datensätze.</span><span class="sxs-lookup"><span data-stu-id="18912-122">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="18912-123">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="18912-123">Usage notes</span></span>

<span data-ttu-id="18912-124">Die Eigenschaften **Gesammelter Datenschlüsselname** und **Gesammelter Datenschlüsselwert** können entweder für die Komponente **Reihenfolge** oder die Komponente **XML-Element** eines EB-Formats konfiguriert werden, das sich unter der Komponente **Allgemeine\\Datei** befindet, in der die Option **Ausgabendetails sammeln** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="18912-124">The **Collected data key name** and **Collected data key value** properties can be configured for either the **Sequence** component or the **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="18912-125">Diese Funktion gibt eine leere Liste zurück, wenn die Option **Ausgabedetails sammeln** der aktiven Komponente **Common\\File** deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="18912-125">This function returns an empty list when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="18912-126">In `condition range`-Argumenten können Platzhalterzeichen **"\*"** verwendet werden, um mehrere beliebige Zeichen darzustellen.</span><span class="sxs-lookup"><span data-stu-id="18912-126">In `condition range` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="18912-127">In `condition value`-Argumenten können Platzhalterzeichen **"\*"** verwendet werden, um mehrere beliebige Zeichen darzustellen.</span><span class="sxs-lookup"><span data-stu-id="18912-127">In `condition value` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="18912-128">Beispiel</span><span class="sxs-lookup"><span data-stu-id="18912-128">Example</span></span>

<span data-ttu-id="18912-129">Um mehr darüber zu erfahren, wie diese Funktion verwendet wird, finden Sie Informationen im Aufgabenleitfaden [EB – Verwendung von Daten der Formatausgabe für Inventur und Summierungen](tasks/er-format-counting-summing-1.md), der Teil des Geschäftsprozesses **IT-Dienstleistungs-/-Lösungskomponenten anschaffen/entwickeln** ist.</span><span class="sxs-lookup"><span data-stu-id="18912-129">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="18912-130">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="18912-130">Additional resources</span></span>

[<span data-ttu-id="18912-131">Datensammlungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="18912-131">Data collection functions</span></span>](er-functions-category-data-collection.md)
