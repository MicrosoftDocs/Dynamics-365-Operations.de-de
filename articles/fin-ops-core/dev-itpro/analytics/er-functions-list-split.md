---
title: SPLIT EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der SPLIT-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e1f11d68b697fdd363f429e60a79f1e1f97bab5b
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686391"
---
# <a name="split-er-function"></a><span data-ttu-id="d7e51-103">SPLIT EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="d7e51-103">SPLIT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d7e51-104">Die Funktion `SPLIT` teilt die angegebene Eingabezeichenfolge in Teilzeichenfolgen auf und gibt das Ergebnis als neuen Wert *Datensatzliste* zurück.</span><span class="sxs-lookup"><span data-stu-id="d7e51-104">The `SPLIT` function splits the specified input string into substrings and returns the result as a new *Record list* value.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="d7e51-105">Syntax 1</span><span class="sxs-lookup"><span data-stu-id="d7e51-105">Syntax 1</span></span>

```vb
SPLIT (input, length)
```

<span data-ttu-id="d7e51-106">Diese Syntax wird verwendet, um die angegebene Eingabezeichenfolge in Teilzeichenfolgen aufzuteilen, von denen jede die angegebene Länge hat.</span><span class="sxs-lookup"><span data-stu-id="d7e51-106">This syntax is used to split the specified input string into substrings, each of which has the specified length.</span></span>

## <a name="syntax-2"></a><span data-ttu-id="d7e51-107">Syntax 2</span><span class="sxs-lookup"><span data-stu-id="d7e51-107">Syntax 2</span></span>

```vb
SPLIT (input, delimiter)
```

<span data-ttu-id="d7e51-108">Diese Syntax wird verwendet, um die angegebene Eingabezeichenfolge in Teilzeichenfolgen zu teilen, von denen jede die angegebene Länge hat.</span><span class="sxs-lookup"><span data-stu-id="d7e51-108">This syntax is used to split the specified input string into substrings, based on the specified delimiter.</span></span>

## <a name="arguments"></a><span data-ttu-id="d7e51-109">Argumente</span><span class="sxs-lookup"><span data-stu-id="d7e51-109">Arguments</span></span>

<span data-ttu-id="d7e51-110">`input`: *String*</span><span class="sxs-lookup"><span data-stu-id="d7e51-110">`input`: *String*</span></span>

<span data-ttu-id="d7e51-111">Zu trennender Text.</span><span class="sxs-lookup"><span data-stu-id="d7e51-111">The text to split.</span></span>

<span data-ttu-id="d7e51-112">`length`: *Integer*</span><span class="sxs-lookup"><span data-stu-id="d7e51-112">`length`: *Integer*</span></span>

<span data-ttu-id="d7e51-113">Die maximale Länge einer einzelnen Teilzeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="d7e51-113">The maximum length of a single substring.</span></span>

<span data-ttu-id="d7e51-114">`delimiter`: *String*</span><span class="sxs-lookup"><span data-stu-id="d7e51-114">`delimiter`: *String*</span></span>

<span data-ttu-id="d7e51-115">Ein Trennzeichen, das zum Trennen von Teilzeichenfolgen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d7e51-115">A delimiter that is used to separate substrings.</span></span>

## <a name="return-values"></a><span data-ttu-id="d7e51-116">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="d7e51-116">Return values</span></span>

<span data-ttu-id="d7e51-117">*Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="d7e51-117">*Record list*</span></span>

<span data-ttu-id="d7e51-118">Die resultierende Liste der Datensätze.</span><span class="sxs-lookup"><span data-stu-id="d7e51-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="d7e51-119">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="d7e51-119">Usage notes</span></span>

<span data-ttu-id="d7e51-120">Die Datensatzstruktur der zurückgegebenen Liste besteht aus dem Feld **Wert** des Typs *String*.</span><span class="sxs-lookup"><span data-stu-id="d7e51-120">The record structure of the list that is returned consists of the **Value** field of the *String* type.</span></span> <span data-ttu-id="d7e51-121">Jeder Datensatz der zurückgegebenen Liste enthält generierte Teilzeichenfolgen in diesem Feld.</span><span class="sxs-lookup"><span data-stu-id="d7e51-121">Every record of the list that is returned contains generated substrings in this field.</span></span>

<span data-ttu-id="d7e51-122">Wenn das Argument `delimiter` leer ist, besteht die neue Liste, die zurückgegeben wir, aus einem Datensatz, der das Feld **Wert** des Typs *String* enthält.</span><span class="sxs-lookup"><span data-stu-id="d7e51-122">If the `delimiter` argument is empty, the new list that is returned consists of one record that has the **Value** field of the *String* type.</span></span> <span data-ttu-id="d7e51-123">Dieses Feld enthält den Eingabetext.</span><span class="sxs-lookup"><span data-stu-id="d7e51-123">This field contains the input text.</span></span>

<span data-ttu-id="d7e51-124">Falls das Argument `input` leer ist, wird eine neue leere Liste zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d7e51-124">If the `input` argument is empty, a new empty list is returned.</span></span> <span data-ttu-id="d7e51-125">Wenn entweder das Argument `input` oder `delimiter` nicht definiert (null) ist, wird eine Anwendungsausnahme ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="d7e51-125">If either the `input` or `delimiter` argument is unspecified (null), an application exception is thrown.</span></span>

## <a name="example-1"></a><span data-ttu-id="d7e51-126">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d7e51-126">Example 1</span></span>

<span data-ttu-id="d7e51-127">`SPLIT ("abcd", 3)` gibt eine neue Liste zurück, die aus zwei Datensätzen besteht, die das Feld **Wert** des Typs *String* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="d7e51-127">`SPLIT ("abcd", 3)` returns a new list that consists of two records that have the **Value** field of the *String* type.</span></span> <span data-ttu-id="d7e51-128">Das Feld **Wert** im ersten Datensatz enthält den Text **"abc"**, und das Feld **Wert** im zweiten Datensatz enthält den Text **"d"**.</span><span class="sxs-lookup"><span data-stu-id="d7e51-128">The **Value** field in the first record contains the text **"abc"**, and the **Value** field in the second record contains the text **"d"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="d7e51-129">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d7e51-129">Example 2</span></span>

<span data-ttu-id="d7e51-130">`SPLIT ("XAb aBy", "aB")` gibt eine neue Liste zurück, die aus drei Datensätzen besteht, die das Feld **Wert** des Typs *String* aufweisen.</span><span class="sxs-lookup"><span data-stu-id="d7e51-130">`SPLIT ("XAb aBy", "aB")` returns a new list that consists of three records that have the **Value** field of the *String* type.</span></span> <span data-ttu-id="d7e51-131">Das Feld **Wert** im ersten Datensatz enthält den Text **"X"**, das Feld **Wert** im zweiten Datensatz enthält den Text **"&nbsp;"**, und das Feld **Wert** im dritten Datensatz enthält den Text **"y"**.</span><span class="sxs-lookup"><span data-stu-id="d7e51-131">The **Value** field in the first record contains the text **"X"**, the **Value** field in the second record contains the text **"&nbsp;"**, and the **Value** field in the third record contains the text **"y"**.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="d7e51-132">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d7e51-132">Additional resources</span></span>

[<span data-ttu-id="d7e51-133">Listenfunktionen</span><span class="sxs-lookup"><span data-stu-id="d7e51-133">List functions</span></span>](er-functions-category-list.md)
