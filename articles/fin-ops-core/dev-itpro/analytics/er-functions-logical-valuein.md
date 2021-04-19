---
title: VALUEIN EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der VALUEIN-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
ms.date: 08/18/2020
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
ms.openlocfilehash: 909aef5e52817a67e400f3132cb5d6ecc8a18906
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751745"
---
# <a name="valuein-er-function"></a><span data-ttu-id="644c6-103">VALUEIN EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="644c6-103">VALUEIN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="644c6-104">Die Funktion `VALUEIN` bestimmt, ob die Eingabe mit einem angegebenen Wert eines angegebenen Artikels in der angegebenen Liste übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="644c6-104">The `VALUEIN` function determines whether the specified input matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="644c6-105">Sie gibt den *booleschen* Wert **TRUE** zurück, wenn die angegebene Eingabe mit dem Ergebnis der Ausführung des angegebenen Ausdrucks für mindestens einen Datensatz der entsprechenden Liste übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="644c6-105">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="644c6-106">Andernfalls gibt sie den *booleschen* Wert **FALSE** zurück.</span><span class="sxs-lookup"><span data-stu-id="644c6-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="644c6-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="644c6-107">Syntax</span></span>

```vb
VALUEIN (input, list, list item expression)
```

## <a name="arguments"></a><span data-ttu-id="644c6-108">Argumente</span><span class="sxs-lookup"><span data-stu-id="644c6-108">Arguments</span></span>

<span data-ttu-id="644c6-109">`input`: *Feld*</span><span class="sxs-lookup"><span data-stu-id="644c6-109">`input`: *Field*</span></span>

<span data-ttu-id="644c6-110">Der gültige Pfad des Elementes einer Datenquelle des Typs *Datensatzliste*.</span><span class="sxs-lookup"><span data-stu-id="644c6-110">The valid path of an item of a data source of the *Record list* type.</span></span> <span data-ttu-id="644c6-111">Der Wert dieses Elements, der abgeglichen wird.</span><span class="sxs-lookup"><span data-stu-id="644c6-111">The value of this item will be matched.</span></span>

<span data-ttu-id="644c6-112">`list`: *Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="644c6-112">`list`: *Record list*</span></span>

<span data-ttu-id="644c6-113">Der gültige Pfad einer Datenquelle des Datentyps *Datensatzliste*.</span><span class="sxs-lookup"><span data-stu-id="644c6-113">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="644c6-114">`list item expression`: *Boolesch*</span><span class="sxs-lookup"><span data-stu-id="644c6-114">`list item expression`: *Boolean*</span></span>

<span data-ttu-id="644c6-115">Ein gültiger Bedingungsausdruck , der entweder zu einem Feld zeigt oder ein einzelnes Feld der Liste enthält, die zum Abgleich verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="644c6-115">A valid conditional expression that either points to or contains a single field of the specified list that should be used for the matching.</span></span>

## <a name="return-values"></a><span data-ttu-id="644c6-116">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="644c6-116">Return values</span></span>

<span data-ttu-id="644c6-117">*Aktiv*</span><span class="sxs-lookup"><span data-stu-id="644c6-117">*Boolean*</span></span>

<span data-ttu-id="644c6-118">Der resultierende *boolesche* Wert.</span><span class="sxs-lookup"><span data-stu-id="644c6-118">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="644c6-119">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="644c6-119">Usage notes</span></span>

<span data-ttu-id="644c6-120">Im Allgemeinen wird die Funktion `VALUEIN` zu einem Satz **OR**-Bedingungen umgerechnet.</span><span class="sxs-lookup"><span data-stu-id="644c6-120">In general, the `VALUEIN` function is translated to a set of **OR** conditions.</span></span> <span data-ttu-id="644c6-121">Wenn die Liste von **ODER**-Bedingungen groß ist und die maximale Gesamtlänge einer SQL-Anweisung überschritten werden kann, erwägen Sie die Verwendung der [`VALUEINLARGE`](er-functions-logical-valueinlarge.md)-Funktion.</span><span class="sxs-lookup"><span data-stu-id="644c6-121">If the list of **OR** conditions is large and the maximum total length of an SQL statement might be exceeded, consider using the [`VALUEINLARGE`](er-functions-logical-valueinlarge.md) function.</span></span>

```vb
(input = list.item1.value) OR (input = list.item2.value) OR …
```

<span data-ttu-id="644c6-122">In einigen Fällen kann es in eine SQL-Datenbankanweisung durch Verwendung des Operators `EXISTS JOIN` übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="644c6-122">In some cases, it can be translated to a database SQL statement by using the `EXISTS JOIN` operator.</span></span>

## <a name="example-1"></a><span data-ttu-id="644c6-123">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="644c6-123">Example 1</span></span>

<span data-ttu-id="644c6-124">In Ihrer Modellzuweisung definieren Sie die Datenquelle **Liste** des Typs *Berechnetes Feld*.</span><span class="sxs-lookup"><span data-stu-id="644c6-124">In your model mapping, you define the **List** data source of the *Calculated field* type.</span></span> <span data-ttu-id="644c6-125">Diese Datenquelle enthält den Ausdruck `SPLIT ("a,b,c", ",")`.</span><span class="sxs-lookup"><span data-stu-id="644c6-125">This data source contains the expression `SPLIT ("a,b,c", ",")`.</span></span>

<span data-ttu-id="644c6-126">Beim Aufruf einer Datenquelle, wenn diese als `VALUEIN ("B", List, List.Value)`-Ausdruck konfiguriert wurde, wird **TRUE** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="644c6-126">When a data source is called, if it has been configured as the `VALUEIN ("B", List, List.Value)` expression, it returns **TRUE**.</span></span> <span data-ttu-id="644c6-127">In diesem Fall wird die Funktion `VALUEIN` in den folgenden Satz an Bedingungen umgerechnet: `(("B" = "a") or ("B" = "b") or ("B" = "c"))`, wobei `("B" = "b")` **TRUE** entspricht.</span><span class="sxs-lookup"><span data-stu-id="644c6-127">In this case, the `VALUEIN` function is translated to the following set of conditions: `(("B" = "a") or ("B" = "b") or ("B" = "c"))`, where `("B" = "b")` equals **TRUE**.</span></span>

<span data-ttu-id="644c6-128">Beim Aufruf einer Datenquelle, wenn diese als `VALUEIN ("B", List, LEFT(List.Value, 0))`-Ausdruck konfiguriert wurde, wird **FALSE** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="644c6-128">When a data source is called, if it has been configured as the `VALUEIN ("B", List, LEFT(List.Value, 0))` expression, it returns **FALSE**.</span></span> <span data-ttu-id="644c6-129">In diesem Fall wird die Funktion `VALUEIN` in die folgende Bedingung umgerechnet: `("B" = "")`, was nicht **TRUE** entspricht.</span><span class="sxs-lookup"><span data-stu-id="644c6-129">In this case, the `VALUEIN` function is translated to the following condition: `("B" = "")`, which doesn't equal **TRUE**.</span></span>

<span data-ttu-id="644c6-130">Der obere Grenzwert für die Anzahl der Zeichen im Text einer derartigen Bedingung entspricht 32.768 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="644c6-130">The upper limit for the number of characters in the text of such a condition is 32,768 characters.</span></span> <span data-ttu-id="644c6-131">Daher sollten Sie keine Datenquellen erstellen, die möglicherweise zur Laufzeit diesen Grenzwert überschreiten.</span><span class="sxs-lookup"><span data-stu-id="644c6-131">Therefore, you should not create data sources that might exceed this limit at runtime.</span></span> <span data-ttu-id="644c6-132">Wenn das Limit überschritten wird, wird die Anwendung nicht mehr ausgeführt und eine Ausnahme ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="644c6-132">If the limit is exceeded, the application stops running, and an exception is thrown.</span></span> <span data-ttu-id="644c6-133">Beispielsweise kann diese Situation erfolgen, wenn die Datenquelle als `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)` konfiguriert wird, und die Listen **List1** und **List2** eine große Anzahl von Datensätzen enthalten.</span><span class="sxs-lookup"><span data-stu-id="644c6-133">For example, this situation can occur if the data source is configured as `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)`, and the **List1** and **List2** lists contain a large volume of records.</span></span>

<span data-ttu-id="644c6-134">In einigen Fällen wird die Funktion `VALUEIN` in eine Datenbankaussage durch Verwendung des Operators `EXISTS JOIN` umgerechnet.</span><span class="sxs-lookup"><span data-stu-id="644c6-134">In some cases, the `VALUEIN` function is translated to a database statement by using the `EXISTS JOIN` operator.</span></span> <span data-ttu-id="644c6-135">Dieses Verhalten tritt auf, wenn die Funktion [`FILTER`](er-functions-list-filter.md) verwendet wird und die folgenden Bedingungen erfüllt sind:</span><span class="sxs-lookup"><span data-stu-id="644c6-135">This behavior occurs when the [`FILTER`](er-functions-list-filter.md) function is used and the following conditions are met:</span></span>

- <span data-ttu-id="644c6-136">Die Option **BITTEN SIE UM ABFRAGE** wird für die Datenquelle der Funktion `VALUEIN` deaktiviert, die die Liste von Datenträgen bezieht.</span><span class="sxs-lookup"><span data-stu-id="644c6-136">The **ASK FOR QUERY** option is turned off for the data source of the `VALUEIN` function that refers to the list of records.</span></span> <span data-ttu-id="644c6-137">Es werden keine zusätzliche Bedingungen auf diese Datenquelle zur Bearbeitungszeit angewendet.</span><span class="sxs-lookup"><span data-stu-id="644c6-137">No additional conditions will be applied to this data source at runtime.</span></span>
- <span data-ttu-id="644c6-138">Es werden keine eingebetteten Ausdrücke für die Datenquelle der Funktion `VALUEIN` konfiguriert, die sich auf die Liste von Datenträgen bezieht.</span><span class="sxs-lookup"><span data-stu-id="644c6-138">No nested expressions are configured for the data source of the `VALUEIN` function that refers to the list of records.</span></span>
- <span data-ttu-id="644c6-139">Ein Listenelement der Funktion `VALUEIN` bezieht sich auf ein Feld der angegebenen Datenquelle, nicht auf einen Ausdruck oder eine Methode dieser Datenquelle.</span><span class="sxs-lookup"><span data-stu-id="644c6-139">A list item of the `VALUEIN` function refers to a field of the specified data source, not to an expression or method of that data source.</span></span>

<span data-ttu-id="644c6-140">Erwägen Sie die Nutzung dieser Option anstelle der Funktion [`WHERE`](er-functions-list-where.md), die weiter oben in diesem Beispiel beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="644c6-140">Consider using this option instead of the [`WHERE`](er-functions-list-where.md) function that is described earlier in this example.</span></span>

## <a name="example-2"></a><span data-ttu-id="644c6-141">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="644c6-141">Example 2</span></span>

<span data-ttu-id="644c6-142">Die folgenden Datenquellen definieren Sie in Ihrer Modellzuordnung:</span><span class="sxs-lookup"><span data-stu-id="644c6-142">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="644c6-143">Die Datenquelle **In** des Typs *Tabellendatensätze*.</span><span class="sxs-lookup"><span data-stu-id="644c6-143">The **In** data source of the *Table records* type.</span></span> <span data-ttu-id="644c6-144">Diese Datenquelle bezieht sich auf die Intrastat-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="644c6-144">This data source refers to the Intrastat table.</span></span>
- <span data-ttu-id="644c6-145">Die Datenquelle **Port** des Typs *Tabellendatensätze*.</span><span class="sxs-lookup"><span data-stu-id="644c6-145">The **Port** data source of the *Table records* type.</span></span> <span data-ttu-id="644c6-146">Diese Datenquelle bezieht sich auf die IntrastatPort-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="644c6-146">This data source refers to the IntrastatPort table.</span></span>

<span data-ttu-id="644c6-147">Wenn eine Datenquelle angerufen wird, die als Ausdruck `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)` konfiguriert, wird die nächste SQL-Anweisung generiert, um gefilterte Datensätze der Intrastat-Tabelle zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="644c6-147">When a data source is called that has been configured as the `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)` expression, the following SQL statement is generated to return filtered records of the Intrastat table.</span></span>

```vb
select … from Intrastat
exists join TableId from IntrastatPort
where IntrastatPort.PortId = Intrastat.Port
```

<span data-ttu-id="644c6-148">Für **dataAreaId**-Felder wird die endgültige SQL-Anweisung durch die Verwendung des Operators `IN` generiert.</span><span class="sxs-lookup"><span data-stu-id="644c6-148">For **dataAreaId** fields, the final SQL statement is generated by the using `IN` operator.</span></span>

## <a name="example-3"></a><span data-ttu-id="644c6-149">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="644c6-149">Example 3</span></span>

<span data-ttu-id="644c6-150">Die folgenden Datenquellen definieren Sie in Ihrer Modellzuordnung:</span><span class="sxs-lookup"><span data-stu-id="644c6-150">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="644c6-151">Die Datenquelle **Le** des Typs *Berechnetes Feld*.</span><span class="sxs-lookup"><span data-stu-id="644c6-151">The **Le** data source of the *Calculated field* type.</span></span> <span data-ttu-id="644c6-152">Diese Datenquelle enthält den Ausdruck `SPLIT ("DEMF,GBSI,USMF", ",")`.</span><span class="sxs-lookup"><span data-stu-id="644c6-152">This data source contains the expression `SPLIT ("DEMF,GBSI,USMF", ",")`.</span></span>
- <span data-ttu-id="644c6-153">Die Datenquelle **In** des Typs *Tabellendatensätze*.</span><span class="sxs-lookup"><span data-stu-id="644c6-153">The **In** data source of the *Table records* type.</span></span> <span data-ttu-id="644c6-154">Diese Datenquelle bezieht sich auf die Intrastat-Tabelle und die Option **Unternehmensübergreifend** ist dafür aktiviert.</span><span class="sxs-lookup"><span data-stu-id="644c6-154">This data source refers to the Intrastat table, and the **Cross-company** option is turned on for it.</span></span>

<span data-ttu-id="644c6-155">Wenn eine Datenquelle angerufen wird, die als Ausdruck `FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)` konfiguriert wird, enthält die abschließende SQL-Anweisung die folgende Bedingung.</span><span class="sxs-lookup"><span data-stu-id="644c6-155">When a data source is called that has been configured as the `FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)` expression, the final SQL statement contains the following condition.</span></span>

```vb
Intrastat.dataAreaId IN ('DEMF', 'GBSI', 'USMF')
```

## <a name="additional-resources"></a><span data-ttu-id="644c6-156">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="644c6-156">Additional resources</span></span>

[<span data-ttu-id="644c6-157">Logische Funktionen</span><span class="sxs-lookup"><span data-stu-id="644c6-157">Logical functions</span></span>](er-functions-category-logical.md)

[<span data-ttu-id="644c6-158">VALUEINLARGE-Funktionen</span><span class="sxs-lookup"><span data-stu-id="644c6-158">VALUEINLARGE functions</span></span>](er-functions-logical-valueinlarge.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]