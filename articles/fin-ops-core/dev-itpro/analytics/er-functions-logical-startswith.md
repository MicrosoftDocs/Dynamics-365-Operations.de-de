---
title: EB-Funktion STARTSWITH
description: In diesem Thema werden Informationen zur Verwendung der STARTSWITH-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
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
ms.openlocfilehash: ef7e9c88abff2b4b58ecb8abf1e69f7853f9b3fa
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751679"
---
# <a name="startswith-er-function"></a><span data-ttu-id="0a6f2-103">EB-Funktion STARTSWITH</span><span class="sxs-lookup"><span data-stu-id="0a6f2-103">STARTSWITH ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0a6f2-104">Die `STARTSWITH`-Funktion untersucht, ob die angegebene Eingabe mit dem angegebenen Text beginnt.</span><span class="sxs-lookup"><span data-stu-id="0a6f2-104">The `STARTSWITH` function determines whether the specified input starts with the specified text.</span></span> <span data-ttu-id="0a6f2-105">Sie gibt einen *booleschen* Wert von **TRUE** zurück, wenn die angegebene Eingabe mit dem angegebenen Text beginnt.</span><span class="sxs-lookup"><span data-stu-id="0a6f2-105">It returns a *Boolean* value of **TRUE** if the specified input starts with the specified text.</span></span> <span data-ttu-id="0a6f2-106">Andernfalls gibt sie den *booleschen* Wert **FALSE** zurück.</span><span class="sxs-lookup"><span data-stu-id="0a6f2-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a6f2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a6f2-107">Syntax</span></span>

```vb
STARTSWITH (input, start text)
```

## <a name="arguments"></a><span data-ttu-id="0a6f2-108">Argumente</span><span class="sxs-lookup"><span data-stu-id="0a6f2-108">Arguments</span></span>

<span data-ttu-id="0a6f2-109">`input`: *String*</span><span class="sxs-lookup"><span data-stu-id="0a6f2-109">`input`: *String*</span></span>

<span data-ttu-id="0a6f2-110">Der gültige Pfad eines Elements einer Datenquelle des *Zeichenfolge*-Typs oder eine Zeichenfolgenkonstante, deren Wert möglicherweise mit dem zweiten Argument beginnt.</span><span class="sxs-lookup"><span data-stu-id="0a6f2-110">The valid path of an item of a data source of the *String* type or a string constant, the value of which might start with the second argument.</span></span>

<span data-ttu-id="0a6f2-111">`start text`: *String*</span><span class="sxs-lookup"><span data-stu-id="0a6f2-111">`start text`: *String*</span></span>

<span data-ttu-id="0a6f2-112">Der gültige Pfad einer Datenquelle des *Zeichenfolge*-Datentyps oder eine Zeichenfolgenkonstante, deren Wert möglicherweise am Anfang des ersten Arguments steht.</span><span class="sxs-lookup"><span data-stu-id="0a6f2-112">The valid path of a data source of the *String* data type or a string constant, the value of which might be at the beginning of the first argument.</span></span>

## <a name="return-values"></a><span data-ttu-id="0a6f2-113">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="0a6f2-113">Return values</span></span>

<span data-ttu-id="0a6f2-114">*Aktiv*</span><span class="sxs-lookup"><span data-stu-id="0a6f2-114">*Boolean*</span></span>

<span data-ttu-id="0a6f2-115">Der resultierende *boolesche* Wert.</span><span class="sxs-lookup"><span data-stu-id="0a6f2-115">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="0a6f2-116">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="0a6f2-116">Usage notes</span></span>

<span data-ttu-id="0a6f2-117">Diese Funktion kann nur dann zur Angabe eines Bedingungsausdrucks der [FILTER](er-functions-list-filter.md)-Funktion verwendet werden, wenn die entsprechende Zuordnung in [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) für den Zugriff auf [Microsoft Dataverse](../data-entities/data-integration-cds.md) konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="0a6f2-117">This function can be used to specify a condition expression of the [FILTER](er-functions-list-filter.md) function only when the relevant mapping is configured in [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) to access [Microsoft Dataverse](../data-entities/data-integration-cds.md).</span></span> <span data-ttu-id="0a6f2-118">Andernfalls wird während der Entwurfszeit eine Ausnahme ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="0a6f2-118">Otherwise, an exception is thrown at design time.</span></span> <span data-ttu-id="0a6f2-119">Die Nachricht, die Sie erhalten, empfiehlt, die [WHERE](er-functions-list-where.md)-Funktion anstelle der `FILTER`-Funktion zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="0a6f2-119">The message that you receive recommends that you use the [WHERE](er-functions-list-where.md) function instead of the `FILTER` function.</span></span>

## <a name="example-1"></a><span data-ttu-id="0a6f2-120">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0a6f2-120">Example 1</span></span>

<span data-ttu-id="0a6f2-121">Der Ausdruck `STARTSWITH ("abc", "d")` gibt **FALSE** zurück, während der Ausdruck `STARTSWITH ("abc", "A")` **TRUE** zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="0a6f2-121">The expression `STARTSWITH ("abc", "d")` returns **FALSE**, whereas the expression `STARTSWITH ("abc", "A")` returns **TRUE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="0a6f2-122">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="0a6f2-122">Example 2</span></span>

<span data-ttu-id="0a6f2-123">Der Ausdruck `STARTSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "123 Coffee Street")` gibt **TRUE** zurück, wenn der Wert des Feldes **Adresse** der Datenquelle **Modell** mit der Zeichenfolge **123 Coffee Street** endet.</span><span class="sxs-lookup"><span data-stu-id="0a6f2-123">The expression `STARTSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "123 Coffee Street")` returns **TRUE** if the value of the **Address** field of the **model** data source starts with the string **123 Coffee Street**.</span></span> <span data-ttu-id="0a6f2-124">Andernfalls wird **FALSE** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0a6f2-124">Otherwise, it returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0a6f2-125">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0a6f2-125">Additional resources</span></span>

[<span data-ttu-id="0a6f2-126">Logische Funktionen</span><span class="sxs-lookup"><span data-stu-id="0a6f2-126">Logical functions</span></span>](er-functions-category-logical.md)
