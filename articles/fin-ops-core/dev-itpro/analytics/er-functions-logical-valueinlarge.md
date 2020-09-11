---
title: VALUEINLARGE-EB-Funktion
description: Dieses Thema bietet Informationen zur Verwendung der VALUEINLARGE-Funktion der elektronischen Berichterstellung (EB).
author: NickSelin
manager: kfend
ms.date: 08/17/2020
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
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 4630ec20e7cbca97c5e43093e6a888a5e09f41a3
ms.sourcegitcommit: 38ad6f791c3d5688a5dc201a234ba89f155f7f03
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "3705142"
---
# <a name="valueinlarge-er-function"></a><span data-ttu-id="bff6f-103">VALUEINLARGE-EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="bff6f-103">VALUEINLARGE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bff6f-104">Die `VALUEINLARGE`-Funktion bestimmt, ob die angegebene Eingabe des Typs *Int64* oder *Integer* mit irgendeinem Wert eines angegebenen Artikels in der angegebenen Liste übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="bff6f-104">The `VALUEINLARGE` function determines whether the specified input of the *Int64* or *Integer* type matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="bff6f-105">Die Funktion gibt den *booleschen* Wert **TRUE** zurück, wenn die angegebene Eingabe mit dem Ergebnis der Ausführung des angegebenen Ausdrucks für mindestens einen Datensatz der entsprechenden Liste übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="bff6f-105">The function returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="bff6f-106">Andernfalls gibt sie den *booleschen* Wert **FALSE** zurück.</span><span class="sxs-lookup"><span data-stu-id="bff6f-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> <span data-ttu-id="bff6f-107">Um den Unterschied zur `VALUEIN`-Funktion zu verstehen, sehen Sie den Abschnitt [Verwendungshinweis](#usage_note) später in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="bff6f-107">To understand the difference with the `VALUEIN` function, see the [Usage note](#usage_note) section later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="bff6f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="bff6f-108">Syntax</span></span>

```vb
VALUEINLARGE (input, list, list item expression)
```

## <a name="arguments"></a><span data-ttu-id="bff6f-109">Argumente</span><span class="sxs-lookup"><span data-stu-id="bff6f-109">Arguments</span></span>

<span data-ttu-id="bff6f-110">`input`: *Feld*</span><span class="sxs-lookup"><span data-stu-id="bff6f-110">`input`: *Field*</span></span>

<span data-ttu-id="bff6f-111">Der gültige Pfad eines Datenquellenelements des Typs *Datensatzliste*.</span><span class="sxs-lookup"><span data-stu-id="bff6f-111">The valid path of a data source item of the *Record list* type.</span></span> <span data-ttu-id="bff6f-112">Der Wert dieses Elements, der abgeglichen wird.</span><span class="sxs-lookup"><span data-stu-id="bff6f-112">The value of this item will be matched.</span></span>

<span data-ttu-id="bff6f-113">`list`: *Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="bff6f-113">`list`: *Record list*</span></span>

<span data-ttu-id="bff6f-114">Der gültige Pfad einer Datenquelle des Datentyps *Datensatzliste*.</span><span class="sxs-lookup"><span data-stu-id="bff6f-114">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="bff6f-115">`list item expression`: *Ausdruck*</span><span class="sxs-lookup"><span data-stu-id="bff6f-115">`list item expression`: *Expression*</span></span>

<span data-ttu-id="bff6f-116">Ein gültiger Bedingungsausdruck , der entweder zu einem Feld zeigt oder ein einzelnes Feld der Liste enthält, die zum Abgleich verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="bff6f-116">A valid conditional expression that either points to or contains a single field of the specified list that should be used for the matching.</span></span>

## <a name="return-values"></a><span data-ttu-id="bff6f-117">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="bff6f-117">Return values</span></span>

<span data-ttu-id="bff6f-118">*Aktiv*</span><span class="sxs-lookup"><span data-stu-id="bff6f-118">*Boolean*</span></span>

<span data-ttu-id="bff6f-119">Der resultierende *boolesche* Wert.</span><span class="sxs-lookup"><span data-stu-id="bff6f-119">The resulting *Boolean* value.</span></span>

## <a name=""></a><span data-ttu-id="bff6f-120"><a name="usage_note">Anwendungshinweise</a></span><span class="sxs-lookup"><span data-stu-id="bff6f-120"><a name="usage_note">Usage notes</a></span></span>

<span data-ttu-id="bff6f-121">Wenn die angegebene Eingabe einen Typ *Int64* oder *Integer* eines Datenquellenelements darstellt, deren Aufruf in eine direkte SQL-Anweisung übersetzt werden kann, wird die angegebene Liste in eine temporäre SQL-Tabelle konvertiert und der Abgleich erfolgt in der Datenbank, indem eine einzelne `EXISTS JOIN`-Abfrage ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bff6f-121">When the specified input represents an *Int64* or *Integer* type of a data source item, the call to which is translatable to a direct SQL statement, the specified list is converted to a temporary SQL table and matching is performed in the database by executing a single `EXISTS JOIN` query.</span></span> <span data-ttu-id="bff6f-122">Andernfalls funktioniert diese Funktion als [`VALUEIN`](er-functions-logical-valuein.md)-Funktion.</span><span class="sxs-lookup"><span data-stu-id="bff6f-122">Otherwise, this function works as the [`VALUEIN`](er-functions-logical-valuein.md) function.</span></span>

<span data-ttu-id="bff6f-123">Wenn die angegebene Eingabe ein Datenquellenelement darstellt, das als ein anderes Element als der Typ *Int64* und *Integer* konzipiert ist, tritt zur Entwurfszeit ein Fehler auf, der Sie darüber informiert, dass die `VALUEINLARGE`-Funktion für den konfigurierten EB-Ausdruck nicht anwendbar ist.</span><span class="sxs-lookup"><span data-stu-id="bff6f-123">When the specified input represents a data source item that is designed as an item other than *Int64* and *Integer* type, an error occurs at design time informing you that the `VALUEINLARGE` function is not applicable for the configured ER expression.</span></span>

<span data-ttu-id="bff6f-124">Wenn der `VALUEINLARGE`-Funktionsausdruck ausgeführt wird und mehr als eine temporäre Tabelle im Rahmen dieser Ausführung verwendet, tritt ein Laufzeitfehler auf.</span><span class="sxs-lookup"><span data-stu-id="bff6f-124">When the `VALUEINLARGE` function expression is executed and more than one temporary table is used in scope of this execution, a runtime error occurs.</span></span>

## <a name="example"></a><span data-ttu-id="bff6f-125">Beispiel</span><span class="sxs-lookup"><span data-stu-id="bff6f-125">Example</span></span>

<span data-ttu-id="bff6f-126">Die folgenden Datenquellen definieren Sie in Ihrer Modellzuordnung:</span><span class="sxs-lookup"><span data-stu-id="bff6f-126">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="bff6f-127">Die Datenquelle **In** des Typs *Tabellendatensätze*.</span><span class="sxs-lookup"><span data-stu-id="bff6f-127">The **In** data source of the *Table records* type.</span></span>
    - <span data-ttu-id="bff6f-128">Diese Datenquelle bezieht sich auf die **Intrastat**-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="bff6f-128">This data source refers to the **Intrastat** table.</span></span>
    - <span data-ttu-id="bff6f-129">Die Option **Unternehmensübergreifend** ist auf **Nein** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="bff6f-129">The **Cross-company** option is set to **No**.</span></span>
- <span data-ttu-id="bff6f-130">Die Datenquelle **InMemory** des Typs *Berechnetes Feld*.</span><span class="sxs-lookup"><span data-stu-id="bff6f-130">The **InMemory** data source of the *Calculated field* type.</span></span>
    - <span data-ttu-id="bff6f-131">Diese Datenquelle enthält den Ausdruck `WHERE (In, In.Port <> "")`.</span><span class="sxs-lookup"><span data-stu-id="bff6f-131">This data source contains the expression `WHERE (In, In.Port <> "")`.</span></span>
- <span data-ttu-id="bff6f-132">Die Datenquelle **InFiltered** des Typs *Berechnetes Feld*.</span><span class="sxs-lookup"><span data-stu-id="bff6f-132">The **InFiltered** data source of the *Calculated field* type.</span></span>
    - <span data-ttu-id="bff6f-133">Diese Datenquelle enthält den Ausdruck `FILTER (In, VALUEINLARGE(In.RecId, InMemory, InMemory.RecId)`.</span><span class="sxs-lookup"><span data-stu-id="bff6f-133">This data source contains the expression `FILTER (In, VALUEINLARGE(In.RecId, InMemory, InMemory.RecId)`.</span></span>

<span data-ttu-id="bff6f-134">Wenn die Datenquelle **InFiltered** im Rahmen des Unternehmens **DEMF** aufgerufen wird, wird eine neue temporäre Tabelle in der Anwendungsdatenbank erstellt, die gesammelte In-Memory-Liste von Datensatzkennungscodes werden in diese Tabelle eingefügt und die folgende SQL-Anweisung wird generiert, um gefilterte Datensätze der **Intrastat**-Tabelle zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="bff6f-134">When the data source **InFiltered** is called under the context of the company **DEMF**, a new temporary table is created in the application database, the collected in memory list of record identification codes are inserted to this table, and the following SQL statement is generated to return filtered records of the **Intrastat** table.</span></span>

```xpp
SELECT … from Intrastat T1
WHERE ((T1.PARTITION=?) AND (T1.DATAAREAID IN (N'DEMF'))) AND
EXISTS (SELECT 'x' FROM tempdb."DBO".? T2 WHERE ((T2.PARTITION=?) AND (T1.RecId=T2.RecId)))
```

## <a name="additional-resources"></a><span data-ttu-id="bff6f-135">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="bff6f-135">Additional resources</span></span>

[<span data-ttu-id="bff6f-136">Logische Funktionen</span><span class="sxs-lookup"><span data-stu-id="bff6f-136">Logical functions</span></span>](er-functions-category-logical.md)

[<span data-ttu-id="bff6f-137">VALUEIN-Funktionen</span><span class="sxs-lookup"><span data-stu-id="bff6f-137">VALUEIN functions</span></span>](er-functions-logical-valuein.md)
