---
title: CONTAINS ER-Funktion
description: In diesem Thema werden Informationen zur Verwendung von CONTAINS Electronic reporting (ER)-Funktion bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: 81964681688cebf870bc9b6c59aff0b7fdd82449
ms.sourcegitcommit: 08ac570bece3e4ee4a0f632f51623e328536dfcf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/08/2021
ms.locfileid: "5557521"
---
# <a name="contains-er-function"></a><span data-ttu-id="7f68b-103">CONTAINS ER-Funktion</span><span class="sxs-lookup"><span data-stu-id="7f68b-103">CONTAINS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7f68b-104">Die `CONTAINS`-Funktion untersucht, ob die angegebene Eingabe den angegebenen Text enthält.</span><span class="sxs-lookup"><span data-stu-id="7f68b-104">The `CONTAINS` function determines whether the specified input contains the specified text.</span></span> <span data-ttu-id="7f68b-105">Sie gibt einen *booleschen* Wert von **TRUE** zurück, wenn die angegebene Eingabe den angegebenen Text enthält.</span><span class="sxs-lookup"><span data-stu-id="7f68b-105">It returns a *Boolean* value of **TRUE** if the specified input contains the specified text.</span></span> <span data-ttu-id="7f68b-106">Andernfalls gibt sie den *booleschen* Wert **FALSE** zurück.</span><span class="sxs-lookup"><span data-stu-id="7f68b-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f68b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f68b-107">Syntax</span></span>

```vb
CONTAINS (input, search text)
```

## <a name="arguments"></a><span data-ttu-id="7f68b-108">Argumente</span><span class="sxs-lookup"><span data-stu-id="7f68b-108">Arguments</span></span>

<span data-ttu-id="7f68b-109">`input`: *String*</span><span class="sxs-lookup"><span data-stu-id="7f68b-109">`input`: *String*</span></span>

<span data-ttu-id="7f68b-110">Der gültige Pfad eines Elements einer Datenquelle des *Zeichenfolge*-Typs oder eine Zeichenfolgenkonstante, deren Wert möglicherweise das zweite Argument enthält.</span><span class="sxs-lookup"><span data-stu-id="7f68b-110">The valid path of an item of a data source of the *String* type or a string constant, the value of which might contain the second argument.</span></span>

<span data-ttu-id="7f68b-111">`search text`: *String*</span><span class="sxs-lookup"><span data-stu-id="7f68b-111">`search text`: *String*</span></span>

<span data-ttu-id="7f68b-112">Der gültige Pfad einer Datenquelle des *Zeichenfolge*-Datentyps oder eine Zeichenfolgenkonstante, deren Wert möglicherweise im ersten Argument enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="7f68b-112">The valid path of a data source of the *String* data type or a string constant, the value of which might be contained in the first argument.</span></span>

## <a name="return-values"></a><span data-ttu-id="7f68b-113">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="7f68b-113">Return values</span></span>

<span data-ttu-id="7f68b-114">*Aktiv*</span><span class="sxs-lookup"><span data-stu-id="7f68b-114">*Boolean*</span></span>

<span data-ttu-id="7f68b-115">Der resultierende *boolesche* Wert.</span><span class="sxs-lookup"><span data-stu-id="7f68b-115">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="7f68b-116">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="7f68b-116">Usage notes</span></span>

<span data-ttu-id="7f68b-117">Diese Funktion kann nur dann zur Angabe eines Bedingungsausdrucks der [FILTER](er-functions-list-filter.md)-Funktion verwendet werden, wenn die entsprechende Zuordnung in [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) für den Zugriff auf [Microsoft Dataverse](../data-entities/data-integration-cds.md) konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="7f68b-117">This function can be used to specify a condition expression of the [FILTER](er-functions-list-filter.md) function only when the relevant mapping is configured in [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) to access [Microsoft Dataverse](../data-entities/data-integration-cds.md).</span></span> <span data-ttu-id="7f68b-118">Andernfalls wird während der Entwurfszeit eine Ausnahme ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="7f68b-118">Otherwise, an exception is thrown at design time.</span></span> <span data-ttu-id="7f68b-119">Die Nachricht, die Sie erhalten, empfiehlt, die [WHERE](er-functions-list-where.md)-Funktion anstelle der `FILTER`-Funktion zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="7f68b-119">The message that you receive recommends that you use the [WHERE](er-functions-list-where.md) function instead of the `FILTER` function.</span></span>

## <a name="example-1"></a><span data-ttu-id="7f68b-120">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7f68b-120">Example 1</span></span>

<span data-ttu-id="7f68b-121">Der Ausdruck `CONTAINS ("abc", "d")` gibt **FALSE** zurück, während der Ausdruck `CONTAINS ("abc", "C")` **TRUE** zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="7f68b-121">The expression `CONTAINS ("abc", "d")` returns **FALSE**, whereas the expression `CONTAINS ("abc", "C")` returns **TRUE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="7f68b-122">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="7f68b-122">Example 2</span></span>

<span data-ttu-id="7f68b-123">Der Ausdruck `CONTAINS (model.InvoiceBase.Customer.PostalAddress.Address, "DEU")` gibt **TRUE** zurück, wenn der Wert des Feldes **Adresse** der Datenquelle **Modell** die Zeichenfolge **DEU** enthält.</span><span class="sxs-lookup"><span data-stu-id="7f68b-123">The expression `CONTAINS (model.InvoiceBase.Customer.PostalAddress.Address, "DEU")` returns **TRUE** if the value of the **Address** field of the **model** data source contains the string **DEU**.</span></span> <span data-ttu-id="7f68b-124">Andernfalls wird **FALSE** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7f68b-124">Otherwise, it returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7f68b-125">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7f68b-125">Additional resources</span></span>

[<span data-ttu-id="7f68b-126">Logische Funktionen</span><span class="sxs-lookup"><span data-stu-id="7f68b-126">Logical functions</span></span>](er-functions-category-logical.md)
