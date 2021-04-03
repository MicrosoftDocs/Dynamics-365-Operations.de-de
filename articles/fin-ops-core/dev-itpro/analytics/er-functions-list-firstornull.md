---
title: FIRSTORNULL EB-Funktion
description: In diesem Thema wir die Verwendung der FIRSTORNULL-Funktion bei der elektronischen Berichterstellung (EB) erklärt
author: NickSelin
manager: kfend
ms.date: 11/29/2019
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
ms.openlocfilehash: 53284333507ef1264d3eb66b0c7141eb69f32392
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564624"
---
# <a name="firstornull-er-function"></a><span data-ttu-id="f15ff-103">FIRSTORNULL EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="f15ff-103">FIRSTORNULL ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f15ff-104">Die Funktion `FIRSTORNULL` gibt den ersten Datensatz der angegebenen Liste mit dem Wert *Container (Datensatz)* zurück, wenn dieser Datensatz nicht leer ist.</span><span class="sxs-lookup"><span data-stu-id="f15ff-104">The `FIRSTORNULL` function returns the first record of the specified list as a *Container (record)* value, if that record isn't empty.</span></span> <span data-ttu-id="f15ff-105">Wenn der Datensatz leer ist, gibt diese Funktion den Wert null für *Container (Datensatz)* zurück.</span><span class="sxs-lookup"><span data-stu-id="f15ff-105">If the record is empty, this function returns a null *Container (record)* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="f15ff-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f15ff-106">Syntax</span></span>

```vb
FIRSTORNULL (list)
```

## <a name="arguments"></a><span data-ttu-id="f15ff-107">Argumente</span><span class="sxs-lookup"><span data-stu-id="f15ff-107">Arguments</span></span>

<span data-ttu-id="f15ff-108">`list`: *Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="f15ff-108">`list`: *Record list*</span></span>

<span data-ttu-id="f15ff-109">Der gültige Pfad einer Datenquelle des Datentyps *Datensatzliste*.</span><span class="sxs-lookup"><span data-stu-id="f15ff-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="f15ff-110">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="f15ff-110">Return values</span></span>

<span data-ttu-id="f15ff-111">*Container (Datensatz)*</span><span class="sxs-lookup"><span data-stu-id="f15ff-111">*Container (record)*</span></span>

<span data-ttu-id="f15ff-112">Der resultierende Datensatzwert.</span><span class="sxs-lookup"><span data-stu-id="f15ff-112">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="f15ff-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f15ff-113">Example</span></span>

<span data-ttu-id="f15ff-114">Der Ausdruck `FIRSTORNULL(SPLIT("",1)).Value` gibt eine leere Zeichenkette zurück (**""**).</span><span class="sxs-lookup"><span data-stu-id="f15ff-114">The expression `FIRSTORNULL(SPLIT("",1)).Value` returns an empty string (**""**).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f15ff-115">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f15ff-115">Additional resources</span></span>

[<span data-ttu-id="f15ff-116">Listenfunktionen</span><span class="sxs-lookup"><span data-stu-id="f15ff-116">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]