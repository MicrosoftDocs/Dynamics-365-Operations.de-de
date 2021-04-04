---
title: EB-Funktion ENDSWITH
description: In diesem Thema werden Informationen zur Verwendung der ENDSWITH-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: 2470bd8c75cf690d701957c4c79009659d61f7a5
ms.sourcegitcommit: 08ac570bece3e4ee4a0f632f51623e328536dfcf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/08/2021
ms.locfileid: "5557520"
---
# <a name="endswith-er-function"></a><span data-ttu-id="019cd-103">EB-Funktion ENDSWITH</span><span class="sxs-lookup"><span data-stu-id="019cd-103">ENDSWITH ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="019cd-104">Die `ENDSWITH`-Funktion untersucht, ob die angegebene Eingabe mit dem angegebenen Text endet.</span><span class="sxs-lookup"><span data-stu-id="019cd-104">The `ENDSWITH` function determines whether the specified input ends with the specified text.</span></span> <span data-ttu-id="019cd-105">Sie gibt einen *booleschen* Wert von **TRUE** zurück, wenn die angegebene Eingabe mit dem angegebenen Text endet.</span><span class="sxs-lookup"><span data-stu-id="019cd-105">It returns a *Boolean* value of **TRUE** if the specified input ends with the specified text.</span></span> <span data-ttu-id="019cd-106">Andernfalls gibt sie den *booleschen* Wert **FALSE** zurück.</span><span class="sxs-lookup"><span data-stu-id="019cd-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="019cd-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="019cd-107">Syntax</span></span>

```vb
ENDSWITH (input, end text)
```

## <a name="arguments"></a><span data-ttu-id="019cd-108">Argumente</span><span class="sxs-lookup"><span data-stu-id="019cd-108">Arguments</span></span>

<span data-ttu-id="019cd-109">`input`: *String*</span><span class="sxs-lookup"><span data-stu-id="019cd-109">`input`: *String*</span></span>

<span data-ttu-id="019cd-110">Der gültige Pfad eines Elements einer Datenquelle des *Zeichenfolge*-Typs oder eine Zeichenfolgenkonstante, deren Wert möglicherweise mit dem zweiten Argument endet.</span><span class="sxs-lookup"><span data-stu-id="019cd-110">The valid path of an item of a data source of the *String* type or a string constant, the value of which might end with the second argument.</span></span>

<span data-ttu-id="019cd-111">`start text`: *String*</span><span class="sxs-lookup"><span data-stu-id="019cd-111">`start text`: *String*</span></span>

<span data-ttu-id="019cd-112">Der gültige Pfad einer Datenquelle des *Zeichenfolge*-Datentyps oder eine Zeichenfolgenkonstante, deren Wert möglicherweise am Ende des ersten Arguments steht.</span><span class="sxs-lookup"><span data-stu-id="019cd-112">The valid path of a data source of the *String* data type or a string constant, the value of which might be at the end of the first argument.</span></span>

## <a name="return-values"></a><span data-ttu-id="019cd-113">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="019cd-113">Return values</span></span>

<span data-ttu-id="019cd-114">*Aktiv*</span><span class="sxs-lookup"><span data-stu-id="019cd-114">*Boolean*</span></span>

<span data-ttu-id="019cd-115">Der resultierende *boolesche* Wert.</span><span class="sxs-lookup"><span data-stu-id="019cd-115">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="019cd-116">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="019cd-116">Usage notes</span></span>

<span data-ttu-id="019cd-117">Diese Funktion kann nur dann zur Angabe eines Bedingungsausdrucks der [FILTER](er-functions-list-filter.md)-Funktion verwendet werden, wenn die entsprechende Zuordnung in [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) für den Zugriff auf [Microsoft Dataverse](../data-entities/data-integration-cds.md) konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="019cd-117">This function can be used to specify a condition expression of the [FILTER](er-functions-list-filter.md) function only when the relevant mapping is configured in [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) to access [Microsoft Dataverse](../data-entities/data-integration-cds.md).</span></span> <span data-ttu-id="019cd-118">Andernfalls wird während der Entwurfszeit eine Ausnahme ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="019cd-118">Otherwise, an exception is thrown at design time.</span></span> <span data-ttu-id="019cd-119">Die Nachricht, die Sie erhalten, empfiehlt, die [WHERE](er-functions-list-where.md)-Funktion anstelle der `FILTER`-Funktion zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="019cd-119">The message that you receive recommends that you use the [WHERE](er-functions-list-where.md) function instead of the `FILTER` function.</span></span>

## <a name="example-1"></a><span data-ttu-id="019cd-120">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="019cd-120">Example 1</span></span>

<span data-ttu-id="019cd-121">Der Ausdruck `ENDSWITH ("abc", "d")` gibt **FALSE** zurück, während der Ausdruck `ENDSWITH ("abc", "C")` **TRUE** zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="019cd-121">The expression `ENDSWITH ("abc", "d")` returns **FALSE**, whereas the expression `ENDSWITH ("abc", "C")` returns **TRUE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="019cd-122">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="019cd-122">Example 2</span></span>

<span data-ttu-id="019cd-123">Der Ausdruck `ENDSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "USA")` gibt **TRUE** zurück, wenn der Wert des Feldes **Adresse** der Datenquelle **Modell** mit der Zeichenfolge **USA** endet.</span><span class="sxs-lookup"><span data-stu-id="019cd-123">The expression `ENDSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "USA")` returns **TRUE** if the value of the **Address** field of the **model** data source ends with the string **USA**.</span></span> <span data-ttu-id="019cd-124">Andernfalls wird **FALSE** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="019cd-124">Otherwise, it returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="019cd-125">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="019cd-125">Additional resources</span></span>

[<span data-ttu-id="019cd-126">Logische Funktionen</span><span class="sxs-lookup"><span data-stu-id="019cd-126">Logical functions</span></span>](er-functions-category-logical.md)
