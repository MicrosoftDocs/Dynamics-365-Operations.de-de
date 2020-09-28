---
title: COUNT EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der COUNT-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: c48483a6677aaeb36eac57a57cec71bf54c7991d
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745344"
---
# <a name="count-er-function"></a><span data-ttu-id="9ffbd-103">COUNT EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="9ffbd-103">COUNT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9ffbd-104">Die Funktion `COUNT` gibt den Wert *Integer* zurück, der die Anzahl der Datensätze in der angegebenen Liste darstellt, wenn die Liste nicht leer ist.</span><span class="sxs-lookup"><span data-stu-id="9ffbd-104">The `COUNT` function returns an *Integer* value that represents the number of records in the specified list, if the list isn't empty.</span></span> <span data-ttu-id="9ffbd-105">Wenn die Liste leer ist, gibt diese Funktion **0** (Null) zurück.</span><span class="sxs-lookup"><span data-stu-id="9ffbd-105">If the list is empty, this function returns **0** (zero).</span></span>

## <a name="syntax"></a><span data-ttu-id="9ffbd-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ffbd-106">Syntax</span></span>

```vb
COUNT (list)
```

## <a name="arguments"></a><span data-ttu-id="9ffbd-107">Argumente</span><span class="sxs-lookup"><span data-stu-id="9ffbd-107">Arguments</span></span>

<span data-ttu-id="9ffbd-108">`list`: *Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="9ffbd-108">`list`: *Record list*</span></span>

<span data-ttu-id="9ffbd-109">Der gültige Pfad einer Datenquelle des Datentyps *Datensatzliste*.</span><span class="sxs-lookup"><span data-stu-id="9ffbd-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="9ffbd-110">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="9ffbd-110">Return values</span></span>

<span data-ttu-id="9ffbd-111">*Ganze Zahl*</span><span class="sxs-lookup"><span data-stu-id="9ffbd-111">*Integer*</span></span>

<span data-ttu-id="9ffbd-112">Der resultierende numerische Wert.</span><span class="sxs-lookup"><span data-stu-id="9ffbd-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="9ffbd-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="9ffbd-113">Example</span></span>

<span data-ttu-id="9ffbd-114">`COUNT (SPLIT("abcd" , 3))` gibt **2** zurück, da die Funktion `SPLIT`, die in diesem Beispiel verwendet wird, eine Liste erstellt, die aus zwei Datensätzen besteht.</span><span class="sxs-lookup"><span data-stu-id="9ffbd-114">`COUNT (SPLIT("abcd" , 3))` returns **2**, because the `SPLIT` function that is used in this example creates a list that consists of two records.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9ffbd-115">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9ffbd-115">Additional resources</span></span>

[<span data-ttu-id="9ffbd-116">Listenfunktionen</span><span class="sxs-lookup"><span data-stu-id="9ffbd-116">List functions</span></span>](er-functions-category-list.md)
