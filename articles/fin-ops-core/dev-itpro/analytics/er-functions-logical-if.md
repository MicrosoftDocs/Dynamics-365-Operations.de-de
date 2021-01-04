---
title: IF EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der IF-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: b8733022b44f3460e34a610140fd6d584ab990c2
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687001"
---
# <a name="if-er-function"></a><span data-ttu-id="ec96d-103">IF EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="ec96d-103">IF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ec96d-104">Die Funktion `IF` gibt den ersten angegebenen Wert zurück, wenn die angegebene Bedingung zutrifft.</span><span class="sxs-lookup"><span data-stu-id="ec96d-104">The `IF` function returns the first specified value if the specified condition is met.</span></span> <span data-ttu-id="ec96d-105">Sie gibt andernfalls den zweiten angegebenen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ec96d-105">Otherwise, it returns the second specified value.</span></span> <span data-ttu-id="ec96d-106">Der zurückgegebene Wert kann ein Wert eines beliebigen unterstützten Datentyps sein.</span><span class="sxs-lookup"><span data-stu-id="ec96d-106">The value that is returned can be a value of any of the supported data types.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec96d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec96d-107">Syntax</span></span>

```vb
IF (condition, first value, second value) as any of the supported data types
```

## <a name="arguments"></a><span data-ttu-id="ec96d-108">Argumente</span><span class="sxs-lookup"><span data-stu-id="ec96d-108">Arguments</span></span>

<span data-ttu-id="ec96d-109">`condition`: *Boolesch*</span><span class="sxs-lookup"><span data-stu-id="ec96d-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="ec96d-110">Ein gültiger Bedingungsausdruck, der getestet werden muss.</span><span class="sxs-lookup"><span data-stu-id="ec96d-110">A valid conditional expression that must be tested.</span></span>

<span data-ttu-id="ec96d-111">`first value`: *Beliebige der unterstützten Datentypen*</span><span class="sxs-lookup"><span data-stu-id="ec96d-111">`first value`: *Any of the supported data types*</span></span>

<span data-ttu-id="ec96d-112">Das Ergebnis, das zurückgegeben wird, wenn die Bedingung erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="ec96d-112">The result that is returned if the condition is met.</span></span>

<span data-ttu-id="ec96d-113">`second value`: *Beliebige der unterstützten Datentypen*</span><span class="sxs-lookup"><span data-stu-id="ec96d-113">`second value`: *Any of the supported data types*</span></span>

<span data-ttu-id="ec96d-114">Das Ergebnis, das zurückgegeben wird, wenn die Bedingung nicht erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="ec96d-114">The result that is returned if the condition isn't met.</span></span>

## <a name="return-values"></a><span data-ttu-id="ec96d-115">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="ec96d-115">Return values</span></span>

<span data-ttu-id="ec96d-116">*Beliebige der unterstützten Datentypen*</span><span class="sxs-lookup"><span data-stu-id="ec96d-116">*Any of the supported data types*</span></span>

<span data-ttu-id="ec96d-117">Der resultierende Wert eines der unterstützten Datentypen.</span><span class="sxs-lookup"><span data-stu-id="ec96d-117">The resulting value of any of the supported data types.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ec96d-118">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="ec96d-118">Usage notes</span></span>

<span data-ttu-id="ec96d-119">Die Argumente `first value` und `second value` müssen anhand desselben Datentyps angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ec96d-119">The `first value` and `second value` arguments must be specified by using the same data type.</span></span> <span data-ttu-id="ec96d-120">Eine Ausnahme wird zur Entwurfszeit ausgelöst, wenn die Datentypen der konfigurierten Werte nicht übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="ec96d-120">An exception is thrown at design time if the data types of the configured values don't match.</span></span>

<span data-ttu-id="ec96d-121">Wenn der erste Wert und der zweite Wert Werte des Datentyps *Container (Datensatz)* oder *Datensatzliste* sind, enthält das Ergebnis nur die Felder, die in beiden Werten vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="ec96d-121">If the first value and the second value are values of the *Container (record)* or *Record list* data type, the result has only the fields that exist in both values.</span></span>

## <a name="example"></a><span data-ttu-id="ec96d-122">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ec96d-122">Example</span></span>

<span data-ttu-id="ec96d-123">`IF (1=2, "condition is met", "condition is not met")` gibt die Zeichenfolge **"Bedingung nicht erfüllt"** zurück.</span><span class="sxs-lookup"><span data-stu-id="ec96d-123">`IF (1=2, "condition is met", "condition is not met")` returns the string **"condition is not met"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ec96d-124">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ec96d-124">Additional resources</span></span>

[<span data-ttu-id="ec96d-125">Logische Funktionen</span><span class="sxs-lookup"><span data-stu-id="ec96d-125">Logical functions</span></span>](er-functions-category-logical.md)
