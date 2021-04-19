---
title: FIRST EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der FIRST-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: d30c8481866ccf3f7080197b37586a0460a4ad2c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746578"
---
# <a name="first-er-function"></a><span data-ttu-id="94f66-103">FIRST EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="94f66-103">FIRST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="94f66-104">Die Funktion `FIRST` gibt den ersten Datensatz der angegebenen Liste mit dem Wert *Container (Datensatz)* zurück, wenn diese Liste nicht leer ist.</span><span class="sxs-lookup"><span data-stu-id="94f66-104">The `FIRST` function returns the first record of the specified list as a *Container (record)* value, if that list isn't empty.</span></span> <span data-ttu-id="94f66-105">Wenn die Liste leer ist, löst diese Funktion eine Ausnahme aus.</span><span class="sxs-lookup"><span data-stu-id="94f66-105">If the list is empty, this function throws an exception.</span></span>

## <a name="syntax"></a><span data-ttu-id="94f66-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="94f66-106">Syntax</span></span>

```vb
FIRST (list)
```

## <a name="arguments"></a><span data-ttu-id="94f66-107">Argumente</span><span class="sxs-lookup"><span data-stu-id="94f66-107">Arguments</span></span>

<span data-ttu-id="94f66-108">`list`: *Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="94f66-108">`list`: *Record list*</span></span>

<span data-ttu-id="94f66-109">Der gültige Pfad einer Datenquelle des Datentyps *Datensatzliste*.</span><span class="sxs-lookup"><span data-stu-id="94f66-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="94f66-110">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="94f66-110">Return values</span></span>

<span data-ttu-id="94f66-111">*Container (Datensatz)*</span><span class="sxs-lookup"><span data-stu-id="94f66-111">*Container (record)*</span></span>

<span data-ttu-id="94f66-112">Der resultierende Datensatzwert.</span><span class="sxs-lookup"><span data-stu-id="94f66-112">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="94f66-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="94f66-113">Example 1</span></span>

<span data-ttu-id="94f66-114">Der Ausdruck `FIRST(SPLIT("ABC",1)).Value` gibt den Textwert **"A"** zurück.</span><span class="sxs-lookup"><span data-stu-id="94f66-114">The expression `FIRST(SPLIT("ABC",1)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="94f66-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="94f66-115">Example 2</span></span>

<span data-ttu-id="94f66-116">Der Ausdruck `FIRST(SPLIT("",1)).Value` löst zur Laufzeit eine Ausnahme aus.</span><span class="sxs-lookup"><span data-stu-id="94f66-116">The expression `FIRST(SPLIT("",1)).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="94f66-117">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="94f66-117">Additional resources</span></span>

[<span data-ttu-id="94f66-118">Listenfunktionen</span><span class="sxs-lookup"><span data-stu-id="94f66-118">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]