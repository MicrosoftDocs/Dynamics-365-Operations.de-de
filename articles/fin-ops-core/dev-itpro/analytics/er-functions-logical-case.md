---
title: CASE EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der CASE-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 38b51a4d8bf8dc997bae2ae9206d8e71ca48dec6
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916061"
---
# <span data-ttu-id="4f176-103"><a name="CASE">CASE ER Funktion</a></span><span class="sxs-lookup"><span data-stu-id="4f176-103"><a name="CASE">CASE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4f176-104">Die Funktion `CASE` bewertet den Wert des angegebenen Ausdrucks anhand der angegebenen alternativen Optionen und gibt das Ergebnis der ersten Option zurück, die dem Wert des angegebenen Ausdrucks entspricht.</span><span class="sxs-lookup"><span data-stu-id="4f176-104">The `CASE` function evaluates the value of the specified expression against the specified alternative options and returns the result of the first option that equals the value of the specified expression.</span></span> <span data-ttu-id="4f176-105">Andernfalls wird ein optionales Standardergebnis zurückgegeben, wenn als letztes Argument der aufgerufenen Funktion ein Standardergebnis angegeben wird, dem keine Option vorangestellt ist.</span><span class="sxs-lookup"><span data-stu-id="4f176-105">Otherwise, it returns the optional default result, if a default result is specified as the last argument of the called function that isn't preceded by an option.</span></span> <span data-ttu-id="4f176-106">Der zurückgegebene Wert kann ein Wert eines beliebigen unterstützten Datentyps sein.</span><span class="sxs-lookup"><span data-stu-id="4f176-106">The value that is returned can be a value of any of the supported data types.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f176-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f176-107">Syntax</span></span>

```
CASE (expression, option 1, result 1[, option 2, result 2, …, option N, result N, default result])
```

## <a name="arguments"></a><span data-ttu-id="4f176-108">Argumente</span><span class="sxs-lookup"><span data-stu-id="4f176-108">Arguments</span></span>

<span data-ttu-id="4f176-109">`expression`: *Primitiver Datentyp* (Boolesch, numerisch oder Text)</span><span class="sxs-lookup"><span data-stu-id="4f176-109">`expression`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="4f176-110">Ein gültiger Ausdruck, der einen Wert des primitiven Datentyps zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="4f176-110">A valid expression that returns a value of the primitive data type.</span></span>

<span data-ttu-id="4f176-111">`option 1`: *Primitiver Datentyp* (Boolesch, numerisch oder Text)</span><span class="sxs-lookup"><span data-stu-id="4f176-111">`option 1`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="4f176-112">Ein gültiger Ausdruck, der einen Wert desselben primitiven Datentyps als Argument `expression` der aufgerufenen Funktion zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="4f176-112">A valid expression that returns a value of the same primitive data type as the `expression` argument of the called function.</span></span> <span data-ttu-id="4f176-113">Dieses Argument ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4f176-113">This argument is required.</span></span>

<span data-ttu-id="4f176-114">`result 1`: *Beliebige der unterstützten Datentypen*</span><span class="sxs-lookup"><span data-stu-id="4f176-114">`result 1`: *Any of the supported data types*</span></span>

<span data-ttu-id="4f176-115">Das zurückgegebene Ergebnis, das der vorherigen Option entspricht.</span><span class="sxs-lookup"><span data-stu-id="4f176-115">The returned result that corresponds to the preceding option.</span></span> <span data-ttu-id="4f176-116">Dieses Argument ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4f176-116">This argument is required.</span></span>

<span data-ttu-id="4f176-117">`option N`: *Primitiver Datentyp* (Boolesch, numerisch oder Text)</span><span class="sxs-lookup"><span data-stu-id="4f176-117">`option N`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="4f176-118">Ein gültiger Ausdruck, der einen Wert desselben primitiven Datentyps als Argument `expression` der aufgerufenen Funktion zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="4f176-118">A valid expression that returns a value of the same primitive data type as the `expression` argument of the called function.</span></span> <span data-ttu-id="4f176-119">Dieses Argument ist optional.</span><span class="sxs-lookup"><span data-stu-id="4f176-119">This argument is optional.</span></span>

<span data-ttu-id="4f176-120">`result N`: *Beliebige der unterstützten Datentypen*</span><span class="sxs-lookup"><span data-stu-id="4f176-120">`result N`: *Any of the supported data types*</span></span>

<span data-ttu-id="4f176-121">Das zurückgegebene Ergebnis, das der vorherigen Option entspricht.</span><span class="sxs-lookup"><span data-stu-id="4f176-121">The returned result that corresponds to the preceding option.</span></span> <span data-ttu-id="4f176-122">Dieses Argument ist optional.</span><span class="sxs-lookup"><span data-stu-id="4f176-122">This argument is optional.</span></span>

<span data-ttu-id="4f176-123">`default result`: *Beliebige der unterstützten Datentypen*</span><span class="sxs-lookup"><span data-stu-id="4f176-123">`default result`: *Any of the supported data types*</span></span>

<span data-ttu-id="4f176-124">Das Ergebnis, das zurückgegeben werden soll, wenn keine Übereinstimmung vorliegt.</span><span class="sxs-lookup"><span data-stu-id="4f176-124">The result that should be returned if there is no match.</span></span> <span data-ttu-id="4f176-125">Dieses Argument ist optional.</span><span class="sxs-lookup"><span data-stu-id="4f176-125">This argument is optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="4f176-126">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="4f176-126">Return values</span></span>

<span data-ttu-id="4f176-127">*Beliebige der unterstützten Datentypen*</span><span class="sxs-lookup"><span data-stu-id="4f176-127">*Any of the supported data types*</span></span>

<span data-ttu-id="4f176-128">Der resultierende Wert eines der unterstützten Datentypen.</span><span class="sxs-lookup"><span data-stu-id="4f176-128">The resulting value of any of the supported data types.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="4f176-129">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="4f176-129">Usage notes</span></span>

<span data-ttu-id="4f176-130">Eine Ausnahme wird zur Laufzeit ausgelöst, wenn keine Übereinstimmung vorliegt und kein optionales Standardergebnis definiert ist.</span><span class="sxs-lookup"><span data-stu-id="4f176-130">An exception is thrown at runtime if there is no match and an optional default result isn't defined.</span></span>

<span data-ttu-id="4f176-131">Alle Ergebnisse müssen anhand desselben Datentyps angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4f176-131">All results must be specified by using the same data type.</span></span> <span data-ttu-id="4f176-132">Eine Ausnahme wird zur Entwurfszeit ausgelöst, wenn die Datentypen der konfigurierten Ergebnisse nicht übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="4f176-132">An exception is thrown at design time if the data types of the configured results don't match.</span></span>

<span data-ttu-id="4f176-133">Wenn der erste Ergebniswert und der zweite Ergebniswert *N*. des Datentyps *Container (Datensatz)* oder des Datentyps *Datensatzliste* sind, enthält das Ergebnis nur die Felder, die in beiden Werten vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="4f176-133">If the first result value and the *N*th result value are values of the *Container (record)* or *Record list* data type, the result has only the fields that exist in both values.</span></span>

## <a name="example"></a><span data-ttu-id="4f176-134">Beispiel</span><span class="sxs-lookup"><span data-stu-id="4f176-134">Example</span></span>

<span data-ttu-id="4f176-135">`CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")` gibt die Zeichenfolge **"WINTER"** zurück, wenn die aktuelle Anwendungssitzung zwischen Oktober und Dezember liegt.</span><span class="sxs-lookup"><span data-stu-id="4f176-135">`CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")` returns the string **"WINTER"** if the current application session date is between October and December.</span></span> <span data-ttu-id="4f176-136">Andernfalls wird eine leere Zeichenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4f176-136">Otherwise, it returns a blank string.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4f176-137">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4f176-137">Additional resources</span></span>

[<span data-ttu-id="4f176-138">Logische Funktionen</span><span class="sxs-lookup"><span data-stu-id="4f176-138">Logical functions</span></span>](er-functions-category-logical.md)
