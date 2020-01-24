---
title: ISEMPTY EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der ISEMPTY-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c8450c17fe2de964016951197b0d4e231c550a99
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916130"
---
# <span data-ttu-id="096ba-103"><a name="ISEMPTY">ISEMPTY EB-Funktion</a></span><span class="sxs-lookup"><span data-stu-id="096ba-103"><a name="ISEMPTY">ISEMPTY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="096ba-104">Die Funktion `ISEMPTY` gibt den *booleschen* Wert **TRUE** zurück, wenn die angegebene Liste keine Datensätze enthält.</span><span class="sxs-lookup"><span data-stu-id="096ba-104">The `ISEMPTY` function returns a *Boolean* value of **TRUE** if the specified list contains no records.</span></span> <span data-ttu-id="096ba-105">Andernfalls gibt sie den *booleschen* Wert **FALSE** zurück.</span><span class="sxs-lookup"><span data-stu-id="096ba-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="096ba-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="096ba-106">Syntax</span></span>

```
ISEMPTY (list)
```

## <a name="arguments"></a><span data-ttu-id="096ba-107">Argumente</span><span class="sxs-lookup"><span data-stu-id="096ba-107">Arguments</span></span>

<span data-ttu-id="096ba-108">`list`: *Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="096ba-108">`list`: *Record list*</span></span>

<span data-ttu-id="096ba-109">Der gültige Pfad einer Datenquelle des Datentyps *Datensatzliste*.</span><span class="sxs-lookup"><span data-stu-id="096ba-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="096ba-110">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="096ba-110">Return values</span></span>

<span data-ttu-id="096ba-111">*Aktiv*</span><span class="sxs-lookup"><span data-stu-id="096ba-111">*Boolean*</span></span>

<span data-ttu-id="096ba-112">Der resultierende *boolesche* Wert.</span><span class="sxs-lookup"><span data-stu-id="096ba-112">The resulting *Boolean* value.</span></span>

## <a name="example-1"></a><span data-ttu-id="096ba-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="096ba-113">Example 1</span></span>

<span data-ttu-id="096ba-114">Wenn Sie die Datenquelle **DS** des Typs *Berechnetes Feld* eingeben, und sie den Ausdruck `SPLIT ("A|B|C", "|")` enthält, gibt der Ausdruck `ISEMPTY(DS)` **FALSE** zurück.</span><span class="sxs-lookup"><span data-stu-id="096ba-114">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `ISEMPTY(DS)` returns **FALSE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="096ba-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="096ba-115">Example 2</span></span>

<span data-ttu-id="096ba-116">Der Ausdruck `ISEMPTY (SPLIT ("",1))` gibt **TRUE** zurück.</span><span class="sxs-lookup"><span data-stu-id="096ba-116">The expression `ISEMPTY (SPLIT ("",1))` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="096ba-117">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="096ba-117">Additional resources</span></span>

[<span data-ttu-id="096ba-118">Listenfunktionen</span><span class="sxs-lookup"><span data-stu-id="096ba-118">List functions</span></span>](er-functions-category-list.md)
