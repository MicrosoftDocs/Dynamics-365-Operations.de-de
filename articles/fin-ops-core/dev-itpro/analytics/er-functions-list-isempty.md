---
title: ISEMPTY EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der ISEMPTY-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: b689e6d4bb849f07db5d00cf8a9dc5c16646a927
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563871"
---
# <a name="isempty-er-function"></a><span data-ttu-id="dd669-103">ISEMPTY EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="dd669-103">ISEMPTY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dd669-104">Die Funktion `ISEMPTY` gibt den *booleschen* Wert **TRUE** zurück, wenn die angegebene Liste keine Datensätze enthält.</span><span class="sxs-lookup"><span data-stu-id="dd669-104">The `ISEMPTY` function returns a *Boolean* value of **TRUE** if the specified list contains no records.</span></span> <span data-ttu-id="dd669-105">Andernfalls gibt sie den *booleschen* Wert **FALSE** zurück.</span><span class="sxs-lookup"><span data-stu-id="dd669-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd669-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd669-106">Syntax</span></span>

```vb
ISEMPTY (list)
```

## <a name="arguments"></a><span data-ttu-id="dd669-107">Argumente</span><span class="sxs-lookup"><span data-stu-id="dd669-107">Arguments</span></span>

<span data-ttu-id="dd669-108">`list`: *Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="dd669-108">`list`: *Record list*</span></span>

<span data-ttu-id="dd669-109">Der gültige Pfad einer Datenquelle des Datentyps *Datensatzliste*.</span><span class="sxs-lookup"><span data-stu-id="dd669-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="dd669-110">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="dd669-110">Return values</span></span>

<span data-ttu-id="dd669-111">*Aktiv*</span><span class="sxs-lookup"><span data-stu-id="dd669-111">*Boolean*</span></span>

<span data-ttu-id="dd669-112">Der resultierende *boolesche* Wert.</span><span class="sxs-lookup"><span data-stu-id="dd669-112">The resulting *Boolean* value.</span></span>

## <a name="example-1"></a><span data-ttu-id="dd669-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="dd669-113">Example 1</span></span>

<span data-ttu-id="dd669-114">Wenn Sie die Datenquelle **DS** des Typs *Berechnetes Feld* eingeben, und sie den Ausdruck `SPLIT ("A|B|C", "|")` enthält, gibt der Ausdruck `ISEMPTY(DS)` **FALSE** zurück.</span><span class="sxs-lookup"><span data-stu-id="dd669-114">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `ISEMPTY(DS)` returns **FALSE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="dd669-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="dd669-115">Example 2</span></span>

<span data-ttu-id="dd669-116">Der Ausdruck `ISEMPTY (SPLIT ("",1))` gibt **TRUE** zurück.</span><span class="sxs-lookup"><span data-stu-id="dd669-116">The expression `ISEMPTY (SPLIT ("",1))` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dd669-117">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="dd669-117">Additional resources</span></span>

[<span data-ttu-id="dd669-118">Listenfunktionen</span><span class="sxs-lookup"><span data-stu-id="dd669-118">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]