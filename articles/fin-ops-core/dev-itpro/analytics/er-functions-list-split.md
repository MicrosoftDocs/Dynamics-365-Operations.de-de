---
title: SPLIT EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der SPLIT-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
ms.date: 04/01/2021
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
ms.openlocfilehash: 26b6ddeb2880fc220283b6389327a497549a4511
ms.sourcegitcommit: 74f5b04b482b2ae023c728e0df0eb78305493c6a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2021
ms.locfileid: "5853442"
---
# <a name="split-er-function"></a><span data-ttu-id="91097-103">SPLIT EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="91097-103">SPLIT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="91097-104">Die Funktion `SPLIT` teilt die angegebene Eingabezeichenfolge in Teilzeichenfolgen auf und gibt das Ergebnis als neuen Wert *Datensatzliste* zurück.</span><span class="sxs-lookup"><span data-stu-id="91097-104">The `SPLIT` function splits the specified input string into substrings and returns the result as a new *Record list* value.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="91097-105">Syntax 1</span><span class="sxs-lookup"><span data-stu-id="91097-105">Syntax 1</span></span>

```vb
SPLIT (input, length)
```

<span data-ttu-id="91097-106">Diese Syntax wird verwendet, um die angegebene Eingabezeichenfolge in Teilzeichenfolgen aufzuteilen, von denen jede die angegebene Länge hat.</span><span class="sxs-lookup"><span data-stu-id="91097-106">This syntax is used to split the specified input string into substrings, each of which has the specified length.</span></span>

## <a name="syntax-2"></a><span data-ttu-id="91097-107">Syntax 2</span><span class="sxs-lookup"><span data-stu-id="91097-107">Syntax 2</span></span>

```vb
SPLIT (input, delimiter)
```

<span data-ttu-id="91097-108">Diese Syntax wird verwendet, um die angegebene Eingabezeichenfolge in Teilzeichenfolgen zu teilen, von denen jede die angegebene Länge hat.</span><span class="sxs-lookup"><span data-stu-id="91097-108">This syntax is used to split the specified input string into substrings, based on the specified delimiter.</span></span>

## <a name="arguments"></a><span data-ttu-id="91097-109">Argumente</span><span class="sxs-lookup"><span data-stu-id="91097-109">Arguments</span></span>

<span data-ttu-id="91097-110">`input`: *String*</span><span class="sxs-lookup"><span data-stu-id="91097-110">`input`: *String*</span></span>

<span data-ttu-id="91097-111">Zu trennender Text.</span><span class="sxs-lookup"><span data-stu-id="91097-111">The text to split.</span></span>

<span data-ttu-id="91097-112">`length`: *Integer*</span><span class="sxs-lookup"><span data-stu-id="91097-112">`length`: *Integer*</span></span>

<span data-ttu-id="91097-113">Die maximale Länge einer einzelnen Teilzeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="91097-113">The maximum length of a single substring.</span></span>

<span data-ttu-id="91097-114">`delimiter`: *String*</span><span class="sxs-lookup"><span data-stu-id="91097-114">`delimiter`: *String*</span></span>

<span data-ttu-id="91097-115">Ein Trennzeichen, das zum Trennen von Teilzeichenfolgen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="91097-115">A delimiter that is used to separate substrings.</span></span>

## <a name="return-values"></a><span data-ttu-id="91097-116">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="91097-116">Return values</span></span>

<span data-ttu-id="91097-117">*Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="91097-117">*Record list*</span></span>

<span data-ttu-id="91097-118">Die resultierende Liste der Datensätze.</span><span class="sxs-lookup"><span data-stu-id="91097-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="91097-119">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="91097-119">Usage notes</span></span>

<span data-ttu-id="91097-120">Die Datensatzstruktur der zurückgegebenen Liste besteht aus dem Feld **Wert** des Typs *String*.</span><span class="sxs-lookup"><span data-stu-id="91097-120">The record structure of the list that is returned consists of the **Value** field of the *String* type.</span></span> <span data-ttu-id="91097-121">Jeder Datensatz der zurückgegebenen Liste enthält generierte Teilzeichenfolgen in diesem Feld.</span><span class="sxs-lookup"><span data-stu-id="91097-121">Every record of the list that is returned contains generated substrings in this field.</span></span>

<span data-ttu-id="91097-122">Wenn das Argument `delimiter` leer ist, besteht die neue Liste, die zurückgegeben wir, aus einem Datensatz, der das Feld **Wert** des Typs *String* enthält.</span><span class="sxs-lookup"><span data-stu-id="91097-122">If the `delimiter` argument is empty, the new list that is returned consists of one record that has the **Value** field of the *String* type.</span></span> <span data-ttu-id="91097-123">Dieses Feld enthält den Eingabetext.</span><span class="sxs-lookup"><span data-stu-id="91097-123">This field contains the input text.</span></span>

<span data-ttu-id="91097-124">Falls das Argument `input` leer ist, wird eine neue leere Liste zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="91097-124">If the `input` argument is empty, a new empty list is returned.</span></span> <span data-ttu-id="91097-125">Wenn entweder das Argument `input` oder `delimiter` nicht definiert (null) ist, wird eine Anwendungsausnahme ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="91097-125">If either the `input` or `delimiter` argument is unspecified (null), an application exception is thrown.</span></span>

## <a name="example-1"></a><span data-ttu-id="91097-126">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="91097-126">Example 1</span></span>

<span data-ttu-id="91097-127">`SPLIT ("abcd", 3)` gibt eine neue Liste zurück, die aus zwei Datensätzen besteht, die das Feld **Wert** des Typs *String* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="91097-127">`SPLIT ("abcd", 3)` returns a new list that consists of two records that have the **Value** field of the *String* type.</span></span> <span data-ttu-id="91097-128">Das Feld **Wert** im ersten Datensatz enthält den Text **"abc"**, und das Feld **Wert** im zweiten Datensatz enthält den Text **"d"**.</span><span class="sxs-lookup"><span data-stu-id="91097-128">The **Value** field in the first record contains the text **"abc"**, and the **Value** field in the second record contains the text **"d"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="91097-129">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="91097-129">Example 2</span></span>

<span data-ttu-id="91097-130">`SPLIT ("XAb aBy", "aB")` gibt eine neue Liste zurück, die aus drei Datensätzen besteht, die das Feld **Wert** des Typs *String* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="91097-130">`SPLIT ("XAb aBy", "aB")` returns a new list that consists of three records that have the **Value** field of the *String* type.</span></span> <span data-ttu-id="91097-131">Das Feld **Wert** im ersten Datensatz enthält den Text **"X"**, das Feld **Wert** im zweiten Datensatz enthält den Text **"&nbsp;"**, und das Feld **Wert** im dritten Datensatz enthält den Text **"y"**.</span><span class="sxs-lookup"><span data-stu-id="91097-131">The **Value** field in the first record contains the text **"X"**, the **Value** field in the second record contains the text **"&nbsp;"**, and the **Value** field in the third record contains the text **"y"**.</span></span> 

## <a name="example-3"></a><span data-ttu-id="91097-132">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="91097-132">Example 3</span></span>

<span data-ttu-id="91097-133">Sie können die Funktion [INDEX](er-functions-list-index.md) zum Zugriff auf einzelne Elemente der angegebenen Eingabezeichenfolge verwenden.</span><span class="sxs-lookup"><span data-stu-id="91097-133">Yo can use the [INDEX](er-functions-list-index.md) function to access individual elements of the specified input string.</span></span> <span data-ttu-id="91097-134">Wenn Sie die Datenquelle **MyList** des Typs **Berechnetes Feld** eingeben, und auf den Ausdruck `SPLIT("abc", 1)` konfigurieren, gibt der Ausdruck `INDEX(MyList,2).Value` den Text **„A“** zurück.</span><span class="sxs-lookup"><span data-stu-id="91097-134">If you enter the **MyList** data source of the **Calculated field** type and configure for it the `SPLIT("abc", 1)` expression, the expression `INDEX(MyList,2).Value` returns the text **"b"**.</span></span>

## <a name="example-4"></a><span data-ttu-id="91097-135">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="91097-135">Example 4</span></span>

<span data-ttu-id="91097-136">Die Funktion [AUFZÄHLEN](er-functions-list-enumerate.md) auch zum Zugriff auf einzelne Elemente der angegebenen Eingabezeichenfolge verwenden.</span><span class="sxs-lookup"><span data-stu-id="91097-136">The [ENUMERATE](er-functions-list-enumerate.md) function can also help you access individual elements of the specified input string.</span></span> <span data-ttu-id="91097-137">Wenn Sie zuerst die Datenquelle **MyList** des Typs **Berechnetes Feld** eingeben und sie auf den Ausdruck `SPLIT("abc", 1)` konfigurieren und dann die Datenquelle **EnumeratedList** des Typs **Berechnetes Feld** eingeben und dafür den Ausdruck `ENUMERATE(MyList)` konfigurieren, gibt der Ausdruck `FIRSTORNULL(WHERE(EnumeratedList, EnumeratedList.Number=2)).Value` den Text **„B“** zurück.</span><span class="sxs-lookup"><span data-stu-id="91097-137">If you first enter the **MyList** data source of the **Calculated field** type and configure for it the `SPLIT("abc", 1)` expression, and then enter the **EnumeratedList** data source of the **Calculated field** type and configure for it the `ENUMERATE(MyList)` expression, the expression `FIRSTORNULL(WHERE(EnumeratedList, EnumeratedList.Number=2)).Value` returns the text **"b"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="91097-138">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="91097-138">Additional resources</span></span>

[<span data-ttu-id="91097-139">Listenfunktionen</span><span class="sxs-lookup"><span data-stu-id="91097-139">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
