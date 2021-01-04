---
title: STRINGJOIN EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der STRINGJOIN-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 586dbcb98d237325188f4b0384580613ab7a9347
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683733"
---
# <a name="stringjoin-er-function"></a><span data-ttu-id="e26a2-103">STRINGJOIN EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="e26a2-103">STRINGJOIN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e26a2-104">Die Funktion `STRINGJOIN` gibt den Wert *String* zurück, der aus verketteten Werten des angegebenen Feldes aus der angegebenen Liste besteht.</span><span class="sxs-lookup"><span data-stu-id="e26a2-104">The `STRINGJOIN` function returns a *String* value that consists of concatenated values of the specified field from the specified list.</span></span> <span data-ttu-id="e26a2-105">Die Werte können durch das angegebene Trennzeichen getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="e26a2-105">The values can be separated by the specified delimiter.</span></span>

## <a name="syntax"></a><span data-ttu-id="e26a2-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e26a2-106">Syntax</span></span>

```vb
STRINGJOIN (list, field, delimiter)
```

## <a name="arguments"></a><span data-ttu-id="e26a2-107">Argumente</span><span class="sxs-lookup"><span data-stu-id="e26a2-107">Arguments</span></span>

<span data-ttu-id="e26a2-108">`list`: *Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="e26a2-108">`list`: *Record list*</span></span>

<span data-ttu-id="e26a2-109">Der gültige Pfad einer Datenquelle des Datentyps *Datensatzliste*.</span><span class="sxs-lookup"><span data-stu-id="e26a2-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="e26a2-110">`field`: *Feld*</span><span class="sxs-lookup"><span data-stu-id="e26a2-110">`field`: *Field*</span></span>

<span data-ttu-id="e26a2-111">Der gültige Pfad eines Feldes des Datentyps *String* in der angegebenen Liste.</span><span class="sxs-lookup"><span data-stu-id="e26a2-111">The valid path of a field of the *String* data type in the specified list.</span></span>

<span data-ttu-id="e26a2-112">`delimiter`: *String*</span><span class="sxs-lookup"><span data-stu-id="e26a2-112">`delimiter`: *String*</span></span>

<span data-ttu-id="e26a2-113">Ein Trennzeichen, das zum Trennen von Teilzeichenfolgen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e26a2-113">A delimiter that is used to separate substrings.</span></span>

## <a name="return-values"></a><span data-ttu-id="e26a2-114">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="e26a2-114">Return values</span></span>

<span data-ttu-id="e26a2-115">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="e26a2-115">*String*</span></span>

<span data-ttu-id="e26a2-116">Der resultierende Textwert.</span><span class="sxs-lookup"><span data-stu-id="e26a2-116">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="e26a2-117">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e26a2-117">Example</span></span>

<span data-ttu-id="e26a2-118">Wenn Sie `SPLIT("abc" , 1)` als Datenquelle **DS** eingeben, gibt der Ausdruck `STRINGJOIN (DS, DS.Value, "-")` **"a-b-c"** zurück.</span><span class="sxs-lookup"><span data-stu-id="e26a2-118">If you enter `SPLIT("abc" , 1)` as data source **DS**, the expression `STRINGJOIN (DS, DS.Value, "-")` returns **"a-b-c"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e26a2-119">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e26a2-119">Additional resources</span></span>

[<span data-ttu-id="e26a2-120">Listenfunktionen</span><span class="sxs-lookup"><span data-stu-id="e26a2-120">List functions</span></span>](er-functions-category-list.md)
