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
ms.openlocfilehash: 3bba9cd190db61fda3636cc3c8093030f886b9bd
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041767"
---
# <span data-ttu-id="b161a-103"><a name="CASE">CASE ER Funktion</a></span><span class="sxs-lookup"><span data-stu-id="b161a-103"><a name="CASE">CASE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b161a-104">Die Funktion `CASE` bewertet den Wert des angegebenen Ausdrucks anhand der angegebenen alternativen Optionen und gibt das Ergebnis der ersten Option zurück, die dem Wert des angegebenen Ausdrucks entspricht.</span><span class="sxs-lookup"><span data-stu-id="b161a-104">The `CASE` function evaluates the value of the specified expression against the specified alternative options and returns the result of the first option that equals the value of the specified expression.</span></span> <span data-ttu-id="b161a-105">Andernfalls wird ein optionales Standardergebnis zurückgegeben, wenn als letztes Argument der aufgerufenen Funktion ein Standardergebnis angegeben wird, dem keine Option vorangestellt ist.</span><span class="sxs-lookup"><span data-stu-id="b161a-105">Otherwise, it returns the optional default result, if a default result is specified as the last argument of the called function that isn't preceded by an option.</span></span> <span data-ttu-id="b161a-106">Der zurückgegebene Wert kann ein Wert eines beliebigen unterstützten Datentyps sein.</span><span class="sxs-lookup"><span data-stu-id="b161a-106">The value that is returned can be a value of any of the supported data types.</span></span>

## <a name="syntax"></a><span data-ttu-id="b161a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b161a-107">Syntax</span></span>

```vb
CASE (expression, option 1, result 1[, option 2, result 2, …, option N, result N, default result])
```

## <a name="arguments"></a><span data-ttu-id="b161a-108">Argumente</span><span class="sxs-lookup"><span data-stu-id="b161a-108">Arguments</span></span>

<span data-ttu-id="b161a-109">`expression`: *Primitiver Datentyp* (Boolesch, numerisch oder Text)</span><span class="sxs-lookup"><span data-stu-id="b161a-109">`expression`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="b161a-110">Ein gültiger Ausdruck, der einen Wert des primitiven Datentyps zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="b161a-110">A valid expression that returns a value of the primitive data type.</span></span>

<span data-ttu-id="b161a-111">`option 1`: *Primitiver Datentyp* (Boolesch, numerisch oder Text)</span><span class="sxs-lookup"><span data-stu-id="b161a-111">`option 1`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="b161a-112">Ein gültiger Ausdruck, der einen Wert desselben primitiven Datentyps als Argument `expression` der aufgerufenen Funktion zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="b161a-112">A valid expression that returns a value of the same primitive data type as the `expression` argument of the called function.</span></span> <span data-ttu-id="b161a-113">Dieses Argument ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b161a-113">This argument is required.</span></span>

<span data-ttu-id="b161a-114">`result 1`: *Beliebige der unterstützten Datentypen*</span><span class="sxs-lookup"><span data-stu-id="b161a-114">`result 1`: *Any of the supported data types*</span></span>

<span data-ttu-id="b161a-115">Das zurückgegebene Ergebnis, das der vorherigen Option entspricht.</span><span class="sxs-lookup"><span data-stu-id="b161a-115">The returned result that corresponds to the preceding option.</span></span> <span data-ttu-id="b161a-116">Dieses Argument ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b161a-116">This argument is required.</span></span>

<span data-ttu-id="b161a-117">`option N`: *Primitiver Datentyp* (Boolesch, numerisch oder Text)</span><span class="sxs-lookup"><span data-stu-id="b161a-117">`option N`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="b161a-118">Ein gültiger Ausdruck, der einen Wert desselben primitiven Datentyps als Argument `expression` der aufgerufenen Funktion zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="b161a-118">A valid expression that returns a value of the same primitive data type as the `expression` argument of the called function.</span></span> <span data-ttu-id="b161a-119">Dieses Argument ist optional.</span><span class="sxs-lookup"><span data-stu-id="b161a-119">This argument is optional.</span></span>

<span data-ttu-id="b161a-120">`result N`: *Beliebige der unterstützten Datentypen*</span><span class="sxs-lookup"><span data-stu-id="b161a-120">`result N`: *Any of the supported data types*</span></span>

<span data-ttu-id="b161a-121">Das zurückgegebene Ergebnis, das der vorherigen Option entspricht.</span><span class="sxs-lookup"><span data-stu-id="b161a-121">The returned result that corresponds to the preceding option.</span></span> <span data-ttu-id="b161a-122">Dieses Argument ist optional.</span><span class="sxs-lookup"><span data-stu-id="b161a-122">This argument is optional.</span></span>

<span data-ttu-id="b161a-123">`default result`: *Beliebige der unterstützten Datentypen*</span><span class="sxs-lookup"><span data-stu-id="b161a-123">`default result`: *Any of the supported data types*</span></span>

<span data-ttu-id="b161a-124">Das Ergebnis, das zurückgegeben werden soll, wenn keine Übereinstimmung vorliegt.</span><span class="sxs-lookup"><span data-stu-id="b161a-124">The result that should be returned if there is no match.</span></span> <span data-ttu-id="b161a-125">Dieses Argument ist optional.</span><span class="sxs-lookup"><span data-stu-id="b161a-125">This argument is optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="b161a-126">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="b161a-126">Return values</span></span>

<span data-ttu-id="b161a-127">*Beliebige der unterstützten Datentypen*</span><span class="sxs-lookup"><span data-stu-id="b161a-127">*Any of the supported data types*</span></span>

<span data-ttu-id="b161a-128">Der resultierende Wert eines der unterstützten Datentypen.</span><span class="sxs-lookup"><span data-stu-id="b161a-128">The resulting value of any of the supported data types.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="b161a-129">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="b161a-129">Usage notes</span></span>

<span data-ttu-id="b161a-130">Eine Ausnahme wird zur Laufzeit ausgelöst, wenn keine Übereinstimmung vorliegt und kein optionales Standardergebnis definiert ist.</span><span class="sxs-lookup"><span data-stu-id="b161a-130">An exception is thrown at runtime if there is no match and an optional default result isn't defined.</span></span>

<span data-ttu-id="b161a-131">Alle Ergebnisse müssen anhand desselben Datentyps angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b161a-131">All results must be specified by using the same data type.</span></span> <span data-ttu-id="b161a-132">Eine Ausnahme wird zur Entwurfszeit ausgelöst, wenn die Datentypen der konfigurierten Ergebnisse nicht übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="b161a-132">An exception is thrown at design time if the data types of the configured results don't match.</span></span>

<span data-ttu-id="b161a-133">Wenn der erste Ergebniswert und der zweite Ergebniswert *N*. des Datentyps *Container (Datensatz)* oder des Datentyps *Datensatzliste* sind, enthält das Ergebnis nur die Felder, die in beiden Werten vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="b161a-133">If the first result value and the *N*th result value are values of the *Container (record)* or *Record list* data type, the result has only the fields that exist in both values.</span></span>

## <a name="example"></a><span data-ttu-id="b161a-134">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b161a-134">Example</span></span>

<span data-ttu-id="b161a-135">`CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")` gibt die Zeichenfolge **"WINTER"** zurück, wenn die aktuelle Anwendungssitzung zwischen Oktober und Dezember liegt.</span><span class="sxs-lookup"><span data-stu-id="b161a-135">`CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")` returns the string **"WINTER"** if the current application session date is between October and December.</span></span> <span data-ttu-id="b161a-136">Andernfalls wird eine leere Zeichenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b161a-136">Otherwise, it returns a blank string.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b161a-137">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b161a-137">Additional resources</span></span>

[<span data-ttu-id="b161a-138">Logische Funktionen</span><span class="sxs-lookup"><span data-stu-id="b161a-138">Logical functions</span></span>](er-functions-category-logical.md)
