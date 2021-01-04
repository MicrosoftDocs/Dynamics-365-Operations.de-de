---
title: FIRSTORNULL EB-Funktion
description: In diesem Thema wir die Verwendung der FIRSTORNULL-Funktion bei der elektronischen Berichterstellung (EB) erklärt
author: NickSelin
manager: kfend
ms.date: 11/29/2019
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
ms.openlocfilehash: 3547eeea3c6fef5cca0699002cc0c35cffd940b3
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688042"
---
# <a name="firstornull-er-function"></a><span data-ttu-id="a0dc7-103">FIRSTORNULL EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="a0dc7-103">FIRSTORNULL ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a0dc7-104">Die Funktion `FIRSTORNULL` gibt den ersten Datensatz der angegebenen Liste mit dem Wert *Container (Datensatz)* zurück, wenn dieser Datensatz nicht leer ist.</span><span class="sxs-lookup"><span data-stu-id="a0dc7-104">The `FIRSTORNULL` function returns the first record of the specified list as a *Container (record)* value, if that record isn't empty.</span></span> <span data-ttu-id="a0dc7-105">Wenn der Datensatz leer ist, gibt diese Funktion den Wert null für *Container (Datensatz)* zurück.</span><span class="sxs-lookup"><span data-stu-id="a0dc7-105">If the record is empty, this function returns a null *Container (record)* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0dc7-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0dc7-106">Syntax</span></span>

```vb
FIRSTORNULL (list)
```

## <a name="arguments"></a><span data-ttu-id="a0dc7-107">Argumente</span><span class="sxs-lookup"><span data-stu-id="a0dc7-107">Arguments</span></span>

<span data-ttu-id="a0dc7-108">`list`: *Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="a0dc7-108">`list`: *Record list*</span></span>

<span data-ttu-id="a0dc7-109">Der gültige Pfad einer Datenquelle des Datentyps *Datensatzliste*.</span><span class="sxs-lookup"><span data-stu-id="a0dc7-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="a0dc7-110">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="a0dc7-110">Return values</span></span>

<span data-ttu-id="a0dc7-111">*Container (Datensatz)*</span><span class="sxs-lookup"><span data-stu-id="a0dc7-111">*Container (record)*</span></span>

<span data-ttu-id="a0dc7-112">Der resultierende Datensatzwert.</span><span class="sxs-lookup"><span data-stu-id="a0dc7-112">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="a0dc7-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a0dc7-113">Example</span></span>

<span data-ttu-id="a0dc7-114">Der Ausdruck `FIRSTORNULL(SPLIT("",1)).Value` gibt eine leere Zeichenkette zurück (**""**).</span><span class="sxs-lookup"><span data-stu-id="a0dc7-114">The expression `FIRSTORNULL(SPLIT("",1)).Value` returns an empty string (**""**).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a0dc7-115">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a0dc7-115">Additional resources</span></span>

[<span data-ttu-id="a0dc7-116">Listenfunktionen</span><span class="sxs-lookup"><span data-stu-id="a0dc7-116">List functions</span></span>](er-functions-category-list.md)
