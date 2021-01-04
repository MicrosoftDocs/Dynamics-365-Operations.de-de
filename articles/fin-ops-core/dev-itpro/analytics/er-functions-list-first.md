---
title: FIRST EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der FIRST-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: a5c52d3f999b4c6fbdea0685977ab13fca1e8ffb
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679413"
---
# <a name="first-er-function"></a><span data-ttu-id="f9000-103">FIRST EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="f9000-103">FIRST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f9000-104">Die Funktion `FIRST` gibt den ersten Datensatz der angegebenen Liste mit dem Wert *Container (Datensatz)* zurück, wenn diese Liste nicht leer ist.</span><span class="sxs-lookup"><span data-stu-id="f9000-104">The `FIRST` function returns the first record of the specified list as a *Container (record)* value, if that list isn't empty.</span></span> <span data-ttu-id="f9000-105">Wenn die Liste leer ist, löst diese Funktion eine Ausnahme aus.</span><span class="sxs-lookup"><span data-stu-id="f9000-105">If the list is empty, this function throws an exception.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9000-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9000-106">Syntax</span></span>

```vb
FIRST (list)
```

## <a name="arguments"></a><span data-ttu-id="f9000-107">Argumente</span><span class="sxs-lookup"><span data-stu-id="f9000-107">Arguments</span></span>

<span data-ttu-id="f9000-108">`list`: *Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="f9000-108">`list`: *Record list*</span></span>

<span data-ttu-id="f9000-109">Der gültige Pfad einer Datenquelle des Datentyps *Datensatzliste*.</span><span class="sxs-lookup"><span data-stu-id="f9000-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="f9000-110">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="f9000-110">Return values</span></span>

<span data-ttu-id="f9000-111">*Container (Datensatz)*</span><span class="sxs-lookup"><span data-stu-id="f9000-111">*Container (record)*</span></span>

<span data-ttu-id="f9000-112">Der resultierende Datensatzwert.</span><span class="sxs-lookup"><span data-stu-id="f9000-112">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="f9000-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f9000-113">Example 1</span></span>

<span data-ttu-id="f9000-114">Der Ausdruck `FIRST(SPLIT("ABC",1)).Value` gibt den Textwert **"A"** zurück.</span><span class="sxs-lookup"><span data-stu-id="f9000-114">The expression `FIRST(SPLIT("ABC",1)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="f9000-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f9000-115">Example 2</span></span>

<span data-ttu-id="f9000-116">Der Ausdruck `FIRST(SPLIT("",1)).Value` löst zur Laufzeit eine Ausnahme aus.</span><span class="sxs-lookup"><span data-stu-id="f9000-116">The expression `FIRST(SPLIT("",1)).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f9000-117">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f9000-117">Additional resources</span></span>

[<span data-ttu-id="f9000-118">Listenfunktionen</span><span class="sxs-lookup"><span data-stu-id="f9000-118">List functions</span></span>](er-functions-category-list.md)
