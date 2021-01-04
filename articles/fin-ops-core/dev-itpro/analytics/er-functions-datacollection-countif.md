---
title: COUNTIF EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung von COUNTIF bei der elektronischen Berichterstellungsfunktion (EB) bereitgestellt.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3f1429ad98f9d4fdab992c2011c6518734484a84
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681183"
---
# <a name="countif-er-function"></a><span data-ttu-id="41550-103">COUNTIF EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="41550-103">COUNTIF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="41550-104">Die Funktion `COUNTIF` gibt den Wert *Integer* zurück, der die Anzahl der Formatelemente darstellt, die erfasst wurden, als die Formatelemente zum Generieren eines ausgehenden Dokuments während der Formatausführung verwendet wurden, und der die angegebene Bedingung erfüllt.</span><span class="sxs-lookup"><span data-stu-id="41550-104">The `COUNTIF` function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="41550-105">Die Bedingung besteht aus einem Schlüsselbereich und einem Schlüsselwert.</span><span class="sxs-lookup"><span data-stu-id="41550-105">The condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="41550-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="41550-106">Syntax</span></span>

```vb
COUNTIF (condition range, condition value)
```

## <a name="arguments"></a><span data-ttu-id="41550-107">Argumente</span><span class="sxs-lookup"><span data-stu-id="41550-107">Arguments</span></span>

<span data-ttu-id="41550-108">`condition range`: *String*</span><span class="sxs-lookup"><span data-stu-id="41550-108">`condition range`: *String*</span></span>

<span data-ttu-id="41550-109">Ein Wert, der von dem Ausdruck zurückgegeben wird, der in der Eigenschaft **Gesammelter Datenschlüsselname** einer Komponente im elektronischen Berichterstellungsformat konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="41550-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of an Electronic reporting (ER) format component.</span></span>

<span data-ttu-id="41550-110">`condition value`: *String*</span><span class="sxs-lookup"><span data-stu-id="41550-110">`condition value`: *String*</span></span>

<span data-ttu-id="41550-111">Ein Wert, der von dem Ausdruck zurückgegeben wird, der in der Eigenschaft **Gesammelter Datenschlüsselwert** einer Komponente im elektronischen Berichterstellungsformat konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="41550-111">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span>

## <a name="return-values"></a><span data-ttu-id="41550-112">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="41550-112">Return values</span></span>

<span data-ttu-id="41550-113">*Ganze Zahl*</span><span class="sxs-lookup"><span data-stu-id="41550-113">*Integer*</span></span>

<span data-ttu-id="41550-114">Der resultierende numerische Wert.</span><span class="sxs-lookup"><span data-stu-id="41550-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="41550-115">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="41550-115">Usage notes</span></span>

<span data-ttu-id="41550-116">Die Eigenschaften **Gesammelter Datenschlüsselname** und **Gesammelter Datenschlüsselwert** können entweder für die Komponente **Reihenfolge** oder die Komponente **XML-Element** eines EB-Formats konfiguriert werden, das sich unter der Komponente **Allgemeine\\Datei** befindet, in der die Option **Ausgabendetails sammeln** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="41550-116">The **Collected data key name** and **Collected data key value** properties can be configured for either the **Sequence** component or the **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="41550-117">Diese Funktion gibt den Wert **0** (null) zurück, wenn die Option **Ausgabedetails sammeln** der aktiven Komponente **Allgemeine\\Datei** deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="41550-117">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="41550-118">Im `condition range`-Argument können Platzhalterzeichen **"\*"** verwendet werden, um mehrere beliebige Zeichen darzustellen.</span><span class="sxs-lookup"><span data-stu-id="41550-118">In the `condition range` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="41550-119">Im `condition value`-Argument können Platzhalterzeichen **"\*"** verwendet werden, um mehrere beliebige Zeichen darzustellen.</span><span class="sxs-lookup"><span data-stu-id="41550-119">In the `condition value` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="41550-120">Beispiel</span><span class="sxs-lookup"><span data-stu-id="41550-120">Example</span></span>

<span data-ttu-id="41550-121">Um mehr darüber zu erfahren, wie diese Funktion verwendet wird, finden Sie Informationen im Aufgabenleitfaden [EB – Verwendung von Daten der Formatausgabe für Inventur und Summierungen](tasks/er-format-counting-summing-1.md), der Teil des Geschäftsprozesses **IT-Dienstleistungs-/-Lösungskomponenten anschaffen/entwickeln** ist.</span><span class="sxs-lookup"><span data-stu-id="41550-121">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="41550-122">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="41550-122">Additional resources</span></span>

[<span data-ttu-id="41550-123">Datensammlungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="41550-123">Data collection functions</span></span>](er-functions-category-data-collection.md)
