---
title: ISEMPTY EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der ISEMPTY-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 9c33e8b613bf5bf5bc17a42a7668d4cc4ee58e53
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750435"
---
# <a name="isempty-er-function"></a><span data-ttu-id="bb80c-103">ISEMPTY EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="bb80c-103">ISEMPTY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bb80c-104">Die Funktion `ISEMPTY` gibt den *booleschen* Wert **TRUE** zurück, wenn die angegebene Liste keine Datensätze enthält.</span><span class="sxs-lookup"><span data-stu-id="bb80c-104">The `ISEMPTY` function returns a *Boolean* value of **TRUE** if the specified list contains no records.</span></span> <span data-ttu-id="bb80c-105">Andernfalls gibt sie den *booleschen* Wert **FALSE** zurück.</span><span class="sxs-lookup"><span data-stu-id="bb80c-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb80c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb80c-106">Syntax</span></span>

```vb
ISEMPTY (list)
```

## <a name="arguments"></a><span data-ttu-id="bb80c-107">Argumente</span><span class="sxs-lookup"><span data-stu-id="bb80c-107">Arguments</span></span>

<span data-ttu-id="bb80c-108">`list`: *Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="bb80c-108">`list`: *Record list*</span></span>

<span data-ttu-id="bb80c-109">Der gültige Pfad einer Datenquelle des Datentyps *Datensatzliste*.</span><span class="sxs-lookup"><span data-stu-id="bb80c-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="bb80c-110">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="bb80c-110">Return values</span></span>

<span data-ttu-id="bb80c-111">*Aktiv*</span><span class="sxs-lookup"><span data-stu-id="bb80c-111">*Boolean*</span></span>

<span data-ttu-id="bb80c-112">Der resultierende *boolesche* Wert.</span><span class="sxs-lookup"><span data-stu-id="bb80c-112">The resulting *Boolean* value.</span></span>

## <a name="example-1"></a><span data-ttu-id="bb80c-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bb80c-113">Example 1</span></span>

<span data-ttu-id="bb80c-114">Wenn Sie die Datenquelle **DS** des Typs *Berechnetes Feld* eingeben, und sie den Ausdruck `SPLIT ("A|B|C", "|")` enthält, gibt der Ausdruck `ISEMPTY(DS)` **FALSE** zurück.</span><span class="sxs-lookup"><span data-stu-id="bb80c-114">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `ISEMPTY(DS)` returns **FALSE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="bb80c-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="bb80c-115">Example 2</span></span>

<span data-ttu-id="bb80c-116">Der Ausdruck `ISEMPTY (SPLIT ("",1))` gibt **TRUE** zurück.</span><span class="sxs-lookup"><span data-stu-id="bb80c-116">The expression `ISEMPTY (SPLIT ("",1))` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bb80c-117">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="bb80c-117">Additional resources</span></span>

[<span data-ttu-id="bb80c-118">Listenfunktionen</span><span class="sxs-lookup"><span data-stu-id="bb80c-118">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]