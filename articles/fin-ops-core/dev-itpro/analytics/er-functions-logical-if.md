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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 198210f15e75de761dbb03e5087ba7c77a95721a
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041744"
---
# <span data-ttu-id="be978-103"><a name="IF">IF EB-Funktion</a></span><span class="sxs-lookup"><span data-stu-id="be978-103"><a name="IF">IF ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="be978-104">Die Funktion `IF` gibt den ersten angegebenen Wert zurück, wenn die angegebene Bedingung zutrifft.</span><span class="sxs-lookup"><span data-stu-id="be978-104">The `IF` function returns the first specified value if the specified condition is met.</span></span> <span data-ttu-id="be978-105">Sie gibt andernfalls den zweiten angegebenen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="be978-105">Otherwise, it returns the second specified value.</span></span> <span data-ttu-id="be978-106">Der zurückgegebene Wert kann ein Wert eines beliebigen unterstützten Datentyps sein.</span><span class="sxs-lookup"><span data-stu-id="be978-106">The value that is returned can be a value of any of the supported data types.</span></span>

## <a name="syntax"></a><span data-ttu-id="be978-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="be978-107">Syntax</span></span>

```vb
IF (condition, first value, second value) as any of the supported data types
```

## <a name="arguments"></a><span data-ttu-id="be978-108">Argumente</span><span class="sxs-lookup"><span data-stu-id="be978-108">Arguments</span></span>

<span data-ttu-id="be978-109">`condition`: *Boolesch*</span><span class="sxs-lookup"><span data-stu-id="be978-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="be978-110">Ein gültiger Bedingungsausdruck, der getestet werden muss.</span><span class="sxs-lookup"><span data-stu-id="be978-110">A valid conditional expression that must be tested.</span></span>

<span data-ttu-id="be978-111">`first value`: *Beliebige der unterstützten Datentypen*</span><span class="sxs-lookup"><span data-stu-id="be978-111">`first value`: *Any of the supported data types*</span></span>

<span data-ttu-id="be978-112">Das Ergebnis, das zurückgegeben wird, wenn die Bedingung erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="be978-112">The result that is returned if the condition is met.</span></span>

<span data-ttu-id="be978-113">`second value`: *Beliebige der unterstützten Datentypen*</span><span class="sxs-lookup"><span data-stu-id="be978-113">`second value`: *Any of the supported data types*</span></span>

<span data-ttu-id="be978-114">Das Ergebnis, das zurückgegeben wird, wenn die Bedingung nicht erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="be978-114">The result that is returned if the condition isn't met.</span></span>

## <a name="return-values"></a><span data-ttu-id="be978-115">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="be978-115">Return values</span></span>

<span data-ttu-id="be978-116">*Beliebige der unterstützten Datentypen*</span><span class="sxs-lookup"><span data-stu-id="be978-116">*Any of the supported data types*</span></span>

<span data-ttu-id="be978-117">Der resultierende Wert eines der unterstützten Datentypen.</span><span class="sxs-lookup"><span data-stu-id="be978-117">The resulting value of any of the supported data types.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="be978-118">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="be978-118">Usage notes</span></span>

<span data-ttu-id="be978-119">Die Argumente `first value` und `second value` müssen anhand desselben Datentyps angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="be978-119">The `first value` and `second value` arguments must be specified by using the same data type.</span></span> <span data-ttu-id="be978-120">Eine Ausnahme wird zur Entwurfszeit ausgelöst, wenn die Datentypen der konfigurierten Werte nicht übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="be978-120">An exception is thrown at design time if the data types of the configured values don't match.</span></span>

<span data-ttu-id="be978-121">Wenn der erste Wert und der zweite Wert Werte des Datentyps *Container (Datensatz)* oder *Datensatzliste* sind, enthält das Ergebnis nur die Felder, die in beiden Werten vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="be978-121">If the first value and the second value are values of the *Container (record)* or *Record list* data type, the result has only the fields that exist in both values.</span></span>

## <a name="example"></a><span data-ttu-id="be978-122">Beispiel</span><span class="sxs-lookup"><span data-stu-id="be978-122">Example</span></span>

<span data-ttu-id="be978-123">`IF (1=2, "condition is met", "condition is not met")` gibt die Zeichenfolge **"Bedingung nicht erfüllt"** zurück.</span><span class="sxs-lookup"><span data-stu-id="be978-123">`IF (1=2, "condition is met", "condition is not met")` returns the string **"condition is not met"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="be978-124">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="be978-124">Additional resources</span></span>

[<span data-ttu-id="be978-125">Logische Funktionen</span><span class="sxs-lookup"><span data-stu-id="be978-125">Logical functions</span></span>](er-functions-category-logical.md)
