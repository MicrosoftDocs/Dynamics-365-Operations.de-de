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
ms.openlocfilehash: 211891a0ad5dc6152ce8d980bcd40a9a6bc7e3e6
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917349"
---
# <span data-ttu-id="3b134-103"><a name="FIRST">FIRST EB-Funktion</a></span><span class="sxs-lookup"><span data-stu-id="3b134-103"><a name="FIRST">FIRST ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3b134-104">Die Funktion `FIRST` gibt den ersten Datensatz der angegebenen Liste mit dem Wert *Container (Datensatz)* zurück, wenn diese Liste nicht leer ist.</span><span class="sxs-lookup"><span data-stu-id="3b134-104">The `FIRST` function returns the first record of the specified list as a *Container (record)* value, if that list isn't empty.</span></span> <span data-ttu-id="3b134-105">Wenn die Liste leer ist, löst diese Funktion eine Ausnahme aus.</span><span class="sxs-lookup"><span data-stu-id="3b134-105">If the list is empty, this function throws an exception.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b134-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b134-106">Syntax</span></span>

```
FIRST (list)
```

## <a name="arguments"></a><span data-ttu-id="3b134-107">Argumente</span><span class="sxs-lookup"><span data-stu-id="3b134-107">Arguments</span></span>

<span data-ttu-id="3b134-108">`list`: *Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="3b134-108">`list`: *Record list*</span></span>

<span data-ttu-id="3b134-109">Der gültige Pfad einer Datenquelle des Datentyps *Datensatzliste*.</span><span class="sxs-lookup"><span data-stu-id="3b134-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="3b134-110">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="3b134-110">Return values</span></span>

<span data-ttu-id="3b134-111">*Container (Datensatz)*</span><span class="sxs-lookup"><span data-stu-id="3b134-111">*Container (record)*</span></span>

<span data-ttu-id="3b134-112">Der resultierende Datensatzwert.</span><span class="sxs-lookup"><span data-stu-id="3b134-112">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="3b134-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3b134-113">Example 1</span></span>

<span data-ttu-id="3b134-114">Der Ausdruck `FIRST(SPLIT("ABC",1)).Value` gibt den Textwert **"A"** zurück.</span><span class="sxs-lookup"><span data-stu-id="3b134-114">The expression `FIRST(SPLIT("ABC",1)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="3b134-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="3b134-115">Example 2</span></span>

<span data-ttu-id="3b134-116">Der Ausdruck `FIRST(SPLIT("",1)).Value` löst zur Laufzeit eine Ausnahme aus.</span><span class="sxs-lookup"><span data-stu-id="3b134-116">The expression `FIRST(SPLIT("",1)).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3b134-117">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="3b134-117">Additional resources</span></span>

[<span data-ttu-id="3b134-118">Listenfunktionen</span><span class="sxs-lookup"><span data-stu-id="3b134-118">List functions</span></span>](er-functions-category-list.md)
