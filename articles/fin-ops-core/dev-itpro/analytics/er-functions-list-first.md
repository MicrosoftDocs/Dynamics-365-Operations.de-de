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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4d10abcf15b93961bd2ba4aec22914825d9ac38c
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042089"
---
# <span data-ttu-id="152d2-103"><a name="FIRST">FIRST EB-Funktion</a></span><span class="sxs-lookup"><span data-stu-id="152d2-103"><a name="FIRST">FIRST ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="152d2-104">Die Funktion `FIRST` gibt den ersten Datensatz der angegebenen Liste mit dem Wert *Container (Datensatz)* zurück, wenn diese Liste nicht leer ist.</span><span class="sxs-lookup"><span data-stu-id="152d2-104">The `FIRST` function returns the first record of the specified list as a *Container (record)* value, if that list isn't empty.</span></span> <span data-ttu-id="152d2-105">Wenn die Liste leer ist, löst diese Funktion eine Ausnahme aus.</span><span class="sxs-lookup"><span data-stu-id="152d2-105">If the list is empty, this function throws an exception.</span></span>

## <a name="syntax"></a><span data-ttu-id="152d2-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="152d2-106">Syntax</span></span>

```vb
FIRST (list)
```

## <a name="arguments"></a><span data-ttu-id="152d2-107">Argumente</span><span class="sxs-lookup"><span data-stu-id="152d2-107">Arguments</span></span>

<span data-ttu-id="152d2-108">`list`: *Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="152d2-108">`list`: *Record list*</span></span>

<span data-ttu-id="152d2-109">Der gültige Pfad einer Datenquelle des Datentyps *Datensatzliste*.</span><span class="sxs-lookup"><span data-stu-id="152d2-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="152d2-110">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="152d2-110">Return values</span></span>

<span data-ttu-id="152d2-111">*Container (Datensatz)*</span><span class="sxs-lookup"><span data-stu-id="152d2-111">*Container (record)*</span></span>

<span data-ttu-id="152d2-112">Der resultierende Datensatzwert.</span><span class="sxs-lookup"><span data-stu-id="152d2-112">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="152d2-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="152d2-113">Example 1</span></span>

<span data-ttu-id="152d2-114">Der Ausdruck `FIRST(SPLIT("ABC",1)).Value` gibt den Textwert **"A"** zurück.</span><span class="sxs-lookup"><span data-stu-id="152d2-114">The expression `FIRST(SPLIT("ABC",1)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="152d2-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="152d2-115">Example 2</span></span>

<span data-ttu-id="152d2-116">Der Ausdruck `FIRST(SPLIT("",1)).Value` löst zur Laufzeit eine Ausnahme aus.</span><span class="sxs-lookup"><span data-stu-id="152d2-116">The expression `FIRST(SPLIT("",1)).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="152d2-117">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="152d2-117">Additional resources</span></span>

[<span data-ttu-id="152d2-118">Listenfunktionen</span><span class="sxs-lookup"><span data-stu-id="152d2-118">List functions</span></span>](er-functions-category-list.md)
