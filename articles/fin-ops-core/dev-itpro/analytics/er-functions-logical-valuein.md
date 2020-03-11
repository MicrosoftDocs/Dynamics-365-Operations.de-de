---
title: VALUEIN EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der VALUEIN-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: d0df97234df41d11897473dea4e85354e82d36ec
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041698"
---
# <span data-ttu-id="24be2-103"><a name="VALUEIN">VALUEIN EB-Funktion</a></span><span class="sxs-lookup"><span data-stu-id="24be2-103"><a name="VALUEIN">VALUEIN ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="24be2-104">Die Funktion `VALUEIN` bestimmt, ob die Eingabe mit einem angegebenen Wert eines angegebenen Artikels in der angegebenen Liste übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="24be2-104">The `VALUEIN` function determines whether the specified input matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="24be2-105">Sie gibt den *booleschen* Wert **TRUE** zurück, wenn die angegebene Eingabe mit dem Ergebnis der Ausführung des angegebenen Ausdrucks für mindestens einen Datensatz der entsprechenden Liste übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="24be2-105">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="24be2-106">Andernfalls gibt sie den *booleschen* Wert **FALSE** zurück.</span><span class="sxs-lookup"><span data-stu-id="24be2-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="24be2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="24be2-107">Syntax</span></span>

```vb
VALUEIN (input, list, list item expression)
```

## <a name="arguments"></a><span data-ttu-id="24be2-108">Argumente</span><span class="sxs-lookup"><span data-stu-id="24be2-108">Arguments</span></span>

<span data-ttu-id="24be2-109">`input`: *Feld*</span><span class="sxs-lookup"><span data-stu-id="24be2-109">`input`: *Field*</span></span>

<span data-ttu-id="24be2-110">Der gültige Pfad des Elementes einer Datenquelle des Typs *Datensatzliste*.</span><span class="sxs-lookup"><span data-stu-id="24be2-110">The valid path of an item of a data source of the *Record list* type.</span></span> <span data-ttu-id="24be2-111">Der Wert dieses Elements, der abgeglichen wird.</span><span class="sxs-lookup"><span data-stu-id="24be2-111">The value of this item will be matched.</span></span>

<span data-ttu-id="24be2-112">`list`: *Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="24be2-112">`list`: *Record list*</span></span>

<span data-ttu-id="24be2-113">Der gültige Pfad einer Datenquelle des Datentyps *Datensatzliste*.</span><span class="sxs-lookup"><span data-stu-id="24be2-113">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="24be2-114">`list item expression`: *Boolesch*</span><span class="sxs-lookup"><span data-stu-id="24be2-114">`list item expression`: *Boolean*</span></span>

<span data-ttu-id="24be2-115">Ein gültiger Bedingungsausdruck , der entweder zu einem Feld zeigt oder ein einzelnes Feld der Liste enthält, die zum Abgleich verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="24be2-115">A valid conditional expression that either points to or contains a single field of the specified list that should be used for the matching.</span></span>

## <a name="return-values"></a><span data-ttu-id="24be2-116">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="24be2-116">Return values</span></span>

<span data-ttu-id="24be2-117">*Aktiv*</span><span class="sxs-lookup"><span data-stu-id="24be2-117">*Boolean*</span></span>

<span data-ttu-id="24be2-118">Der resultierende *boolesche* Wert.</span><span class="sxs-lookup"><span data-stu-id="24be2-118">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="24be2-119">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="24be2-119">Usage notes</span></span>

<span data-ttu-id="24be2-120">Im Allgemeinen wird die Funktion `VALUEIN` zu einem Satz **OR**-Bedingungen umgerechnet.</span><span class="sxs-lookup"><span data-stu-id="24be2-120">In general, the `VALUEIN` function is translated to a set of **OR** conditions.</span></span>

```vb
(input = list.item1.value) OR (input = list.item2.value) OR …
```

<span data-ttu-id="24be2-121">In einigen Fällen kann es in eine SQL-Datenbankanweisung durch Verwendung des Operators `EXISTS JOIN` übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="24be2-121">In some cases, it can be translated to a database SQL statement by using the `EXISTS JOIN` operator.</span></span>

## <a name="example-1"></a><span data-ttu-id="24be2-122">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="24be2-122">Example 1</span></span>

<span data-ttu-id="24be2-123">In Ihrer Modellzuweisung definieren Sie die Datenquelle **Liste** des Typs *Berechnetes Feld*.</span><span class="sxs-lookup"><span data-stu-id="24be2-123">In your model mapping, you define the **List** data source of the *Calculated field* type.</span></span> <span data-ttu-id="24be2-124">Diese Datenquelle enthält den Ausdruck `SPLIT ("a,b,c", ",")`.</span><span class="sxs-lookup"><span data-stu-id="24be2-124">This data source contains the expression `SPLIT ("a,b,c", ",")`.</span></span>

<span data-ttu-id="24be2-125">Beim Aufruf einer Datenquelle, wenn diese als `VALUEIN ("B", List, List.Value)`-Ausdruck konfiguriert wurde, wird **TRUE** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="24be2-125">When a data source is called, if it has been configured as the `VALUEIN ("B", List, List.Value)` expression, it returns **TRUE**.</span></span> <span data-ttu-id="24be2-126">In diesem Fall wird die Funktion `VALUEIN` in den folgenden Satz an Bedingungen umgerechnet: `(("B" = "a") or ("B" = "b") or ("B" = "c"))`, wobei `("B" = "b")` **TRUE** entspricht.</span><span class="sxs-lookup"><span data-stu-id="24be2-126">In this case, the `VALUEIN` function is translated to the following set of conditions: `(("B" = "a") or ("B" = "b") or ("B" = "c"))`, where `("B" = "b")` equals **TRUE**.</span></span>

<span data-ttu-id="24be2-127">Beim Aufruf einer Datenquelle, wenn diese als `VALUEIN ("B", List, LEFT(List.Value, 0))`-Ausdruck konfiguriert wurde, wird **FALSE** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="24be2-127">When a data source is called, if it has been configured as the `VALUEIN ("B", List, LEFT(List.Value, 0))` expression, it returns **FALSE**.</span></span> <span data-ttu-id="24be2-128">In diesem Fall wird die Funktion `VALUEIN` in die folgende Bedingung umgerechnet: `("B" = "")`, was nicht **TRUE** entspricht.</span><span class="sxs-lookup"><span data-stu-id="24be2-128">In this case, the `VALUEIN` function is translated to the following condition: `("B" = "")`, which doesn't equal **TRUE**.</span></span>

<span data-ttu-id="24be2-129">Der obere Grenzwert für die Anzahl der Zeichen im Text einer derartigen Bedingung entspricht 32.768 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="24be2-129">The upper limit for the number of characters in the text of such a condition is 32,768 characters.</span></span> <span data-ttu-id="24be2-130">Daher sollten Sie keine Datenquellen erstellen, die möglicherweise zur Laufzeit diesen Grenzwert überschreiten.</span><span class="sxs-lookup"><span data-stu-id="24be2-130">Therefore, you should not create data sources that might exceed this limit at runtime.</span></span> <span data-ttu-id="24be2-131">Wenn das Limit überschritten wird, wird die Anwendung nicht mehr ausgeführt und eine Ausnahme ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="24be2-131">If the limit is exceeded, the application stops running, and an exception is thrown.</span></span> <span data-ttu-id="24be2-132">Beispielsweise kann diese Situation erfolgen, wenn die Datenquelle als `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)` konfiguriert wird, und die Listen **List1** und **List2** eine große Anzahl von Datensätzen enthalten.</span><span class="sxs-lookup"><span data-stu-id="24be2-132">For example, this situation can occur if the data source is configured as `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)`, and the **List1** and **List2** lists contain a large volume of records.</span></span>

<span data-ttu-id="24be2-133">In einigen Fällen wird die Funktion `VALUEIN` in eine Datenbankaussage durch Verwendung des Operators `EXISTS JOIN` umgerechnet.</span><span class="sxs-lookup"><span data-stu-id="24be2-133">In some cases, the `VALUEIN` function is translated to a database statement by using the `EXISTS JOIN` operator.</span></span> <span data-ttu-id="24be2-134">Dieses Verhalten ist der Fall, wenn die Funktion [FILTER](er-functions-list-filter.md) verwendet wird und die folgenden Bedingungen erfüllt sind:</span><span class="sxs-lookup"><span data-stu-id="24be2-134">This behavior occurs when the [FILTER](er-functions-list-filter.md) function is used and the following conditions are met:</span></span>

- <span data-ttu-id="24be2-135">Die Option **BITTEN SIE UM ABFRAGE** wird für die Datenquelle der Funktion `VALUEIN` deaktiviert, die die Liste von Datenträgen bezieht.</span><span class="sxs-lookup"><span data-stu-id="24be2-135">The **ASK FOR QUERY** option is turned off for the data source of the `VALUEIN` function that refers to the list of records.</span></span> <span data-ttu-id="24be2-136">Es werden keine zusätzliche Bedingungen auf diese Datenquelle zur Bearbeitungszeit angewendet.</span><span class="sxs-lookup"><span data-stu-id="24be2-136">No additional conditions will be applied to this data source at runtime.</span></span>
- <span data-ttu-id="24be2-137">Es werden keine eingebetteten Ausdrücke für die Datenquelle der Funktion `VALUEIN` konfiguriert, die sich auf die Liste von Datenträgen bezieht.</span><span class="sxs-lookup"><span data-stu-id="24be2-137">No nested expressions are configured for the data source of the `VALUEIN` function that refers to the list of records.</span></span>
- <span data-ttu-id="24be2-138">Ein Listenelement der Funktion `VALUEIN` bezieht sich auf ein Feld der angegebenen Datenquelle, nicht auf einen Ausdruck oder eine Methode dieser Datenquelle.</span><span class="sxs-lookup"><span data-stu-id="24be2-138">A list item of the `VALUEIN` function refers to a field of the specified data source, not to an expression or method of that data source.</span></span>

<span data-ttu-id="24be2-139">Berücksichtigen Sie diese Option anstelle der Funktion [WHERE](er-functions-list-where.md), die weiter oben in diesem Beispiel beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="24be2-139">Consider using this option instead of the [WHERE](er-functions-list-where.md) function that is described earlier in this example.</span></span>

## <a name="example-2"></a><span data-ttu-id="24be2-140">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="24be2-140">Example 2</span></span>

<span data-ttu-id="24be2-141">Die folgenden Datenquellen definieren Sie in Ihrer Modellzuordnung:</span><span class="sxs-lookup"><span data-stu-id="24be2-141">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="24be2-142">Die Datenquelle **In** des Typs *Tabellendatensätze*.</span><span class="sxs-lookup"><span data-stu-id="24be2-142">The **In** data source of the *Table records* type.</span></span> <span data-ttu-id="24be2-143">Diese Datenquelle bezieht sich auf die Intrastat-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="24be2-143">This data source refers to the Intrastat table.</span></span>
- <span data-ttu-id="24be2-144">Die Datenquelle **Port** des Typs *Tabellendatensätze*.</span><span class="sxs-lookup"><span data-stu-id="24be2-144">The **Port** data source of the *Table records* type.</span></span> <span data-ttu-id="24be2-145">Diese Datenquelle bezieht sich auf die IntrastatPort-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="24be2-145">This data source refers to the IntrastatPort table.</span></span>

<span data-ttu-id="24be2-146">Wenn eine Datenquelle angerufen wird, die als Ausdruck `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)` konfiguriert, wird die nächste SQL-Anweisung generiert, um gefilterte Datensätze der Intrastat-Tabelle zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="24be2-146">When a data source is called that has been configured as the `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)` expression, the following SQL statement is generated to return filtered records of the Intrastat table.</span></span>

```vb
select … from Intrastat
exists join TableId from IntrastatPort
where IntrastatPort.PortId = Intrastat.Port
```

<span data-ttu-id="24be2-147">Für **dataAreaId**-Felder wird die endgültige SQL-Anweisung durch die Verwendung des Operators `IN` generiert.</span><span class="sxs-lookup"><span data-stu-id="24be2-147">For **dataAreaId** fields, the final SQL statement is generated by the using `IN` operator.</span></span>

## <a name="example-3"></a><span data-ttu-id="24be2-148">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="24be2-148">Example 3</span></span>

<span data-ttu-id="24be2-149">Die folgenden Datenquellen definieren Sie in Ihrer Modellzuordnung:</span><span class="sxs-lookup"><span data-stu-id="24be2-149">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="24be2-150">Die Datenquelle **Le** des Typs *Berechnetes Feld*.</span><span class="sxs-lookup"><span data-stu-id="24be2-150">The **Le** data source of the *Calculated field* type.</span></span> <span data-ttu-id="24be2-151">Diese Datenquelle enthält den Ausdruck `SPLIT ("DEMF,GBSI,USMF", ",")`.</span><span class="sxs-lookup"><span data-stu-id="24be2-151">This data source contains the expression `SPLIT ("DEMF,GBSI,USMF", ",")`.</span></span>
- <span data-ttu-id="24be2-152">Die Datenquelle **In** des Typs *Tabellendatensätze*.</span><span class="sxs-lookup"><span data-stu-id="24be2-152">The **In** data source of the *Table records* type.</span></span> <span data-ttu-id="24be2-153">Diese Datenquelle bezieht sich auf die Intrastat-Tabelle und die Option **Unternehmensübergreifend** ist dafür aktiviert.</span><span class="sxs-lookup"><span data-stu-id="24be2-153">This data source refers to the Intrastat table, and the **Cross-company** option is turned on for it.</span></span>

<span data-ttu-id="24be2-154">Wenn eine Datenquelle angerufen wird, die als Ausdruck `FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)` konfiguriert wird, enthält die abschließende SQL-Anweisung die folgende Bedingung.</span><span class="sxs-lookup"><span data-stu-id="24be2-154">When a data source is called that has been configured as the `FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)` expression, the final SQL statement contains the following condition.</span></span>

```vb
Intrastat.dataAreaId IN ('DEMF', 'GBSI', 'USMF')
```

## <a name="additional-resources"></a><span data-ttu-id="24be2-155">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="24be2-155">Additional resources</span></span>

[<span data-ttu-id="24be2-156">Logische Funktionen</span><span class="sxs-lookup"><span data-stu-id="24be2-156">Logical functions</span></span>](er-functions-category-logical.md)
