---
title: SUMIF EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung von SUMIF bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
ms.date: 04/27/2020
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
ms.openlocfilehash: 60cf85ac0ffcdb163c12670efa3dcc7e9f05cb16
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747106"
---
# <a name="sumif-er-function"></a><span data-ttu-id="81017-103">SUMIF EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="81017-103">SUMIF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="81017-104">Die Funktion `SUMIF` gibt den Wert *Real* zurück, der die Summe der Werte darstellt, die bei Bindungen der Formatelemente zurückgegeben und erfasst wurden, als die Formatelemente zum Generieren eines ausgehenden Dokuments während der Formatausführung verwendet wurden, und der die angegebene Bedingung erfüllt.</span><span class="sxs-lookup"><span data-stu-id="81017-104">The `SUMIF` function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="81017-105">Die Bedingung besteht aus einem Schlüsselbereich und einem Schlüsselwert.</span><span class="sxs-lookup"><span data-stu-id="81017-105">The condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="81017-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="81017-106">Syntax</span></span>

```vb
SUMIF (key name for summing, condition range, condition value)
```

## <a name="arguments"></a><span data-ttu-id="81017-107">Argumente</span><span class="sxs-lookup"><span data-stu-id="81017-107">Arguments</span></span>

<span data-ttu-id="81017-108">`key name for summing`: *String*</span><span class="sxs-lookup"><span data-stu-id="81017-108">`key name for summing`: *String*</span></span>

<span data-ttu-id="81017-109">Ein Wert, der von dem Ausdruck zurückgegeben wird, der in der Eigenschaft **Gesammelter Datenschlüsselname** der Formatkomponente der elektronischen Berichterstattung (EB) konfiguriert wurde, für die der Wert der Bindung zu Summierungszwecken verwendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="81017-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of the Electronic reporting (ER) format component for which the value of the binding must be used for summing purposes.</span></span>

<span data-ttu-id="81017-110">Die Eigenschaft **Gesammelter Datenschlüsselwert** kann entweder für die Komponente **Reichenfolge** oder die Komponente **XML-Element** eines EB-Formats konfiguriert werden, das sich unter der Komponente **Allgemeine\\Datei** befindet, in der die Option **Ausgabendetails sammeln** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="81017-110">The **Collected data key value** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="return-values"></a><span data-ttu-id="81017-111">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="81017-111">Return values</span></span>

<span data-ttu-id="81017-112">*Gleitkommazahl*</span><span class="sxs-lookup"><span data-stu-id="81017-112">*Real*</span></span>

<span data-ttu-id="81017-113">Der resultierende numerische Wert.</span><span class="sxs-lookup"><span data-stu-id="81017-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="81017-114">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="81017-114">Usage notes</span></span>

<span data-ttu-id="81017-115">Diese Funktion gibt den Wert **0** (null) zurück, wenn die Option **Ausgabedetails sammeln** der aktiven Komponente **Allgemeine\\Datei** deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="81017-115">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="81017-116">Im `condition range`-Argument können Platzhalterzeichen **"\*"** verwendet werden, um mehrere beliebige Zeichen darzustellen.</span><span class="sxs-lookup"><span data-stu-id="81017-116">In the `condition range` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="81017-117">Im `condition value`-Argument können Platzhalterzeichen **"\*"** verwendet werden, um mehrere beliebige Zeichen darzustellen.</span><span class="sxs-lookup"><span data-stu-id="81017-117">In the `condition value` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="81017-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="81017-118">Example</span></span>

<span data-ttu-id="81017-119">Um mehr darüber zu erfahren, wie diese Funktion verwendet wird, finden Sie Informationen im Aufgabenleitfaden [EB – Verwendung von Daten der Formatausgabe für Inventur und Summierungen](tasks/er-format-counting-summing-1.md), der Teil des Geschäftsprozesses **IT-Dienstleistungs-/-Lösungskomponenten anschaffen/entwickeln** ist.</span><span class="sxs-lookup"><span data-stu-id="81017-119">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

<span data-ttu-id="81017-120">Weitere Informationen und Beispiele zur Verwendung dieser Funktion finden Sie unter [Verschieben Sie die Ausführung von Sequenzelementen in EB-Formaten](er-defer-sequence-element.md#Example) und [Verschieben Sie die Ausführung von XML-Elementen in EB-Formaten](er-defer-xml-element.md#Example).</span><span class="sxs-lookup"><span data-stu-id="81017-120">For more information and examples about using this function, see [Defer the execution of sequence elements in ER formats](er-defer-sequence-element.md#Example) and [Defer the execution of XML elements in ER formats](er-defer-xml-element.md#Example).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="81017-121">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="81017-121">Additional resources</span></span>

[<span data-ttu-id="81017-122">Datensammlungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="81017-122">Data collection functions</span></span>](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]