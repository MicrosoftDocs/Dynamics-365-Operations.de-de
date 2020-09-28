---
title: CONCATENATE EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der CONCATENATE-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: 1a21140e5636ebd96eca4be90308c915e77510e1
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743902"
---
# <a name="concatenate-er-function"></a><span data-ttu-id="23fc7-103">CONCATENATE EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="23fc7-103">CONCATENATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="23fc7-104">Die Funktion `CONCATENATE` gibt alle angegebenen Textzeichenfolgen mit dem Wert *String* zurück, nachdem sie zu einer Zeichenfolge zusammengefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="23fc7-104">The `CONCATENATE` function returns all the specified text strings as a *String* value after they have been joined into one string.</span></span>

## <a name="syntax"></a><span data-ttu-id="23fc7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="23fc7-105">Syntax</span></span>

```vb
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a><span data-ttu-id="23fc7-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="23fc7-106">Arguments</span></span>

<span data-ttu-id="23fc7-107">`text 1`: *String*</span><span class="sxs-lookup"><span data-stu-id="23fc7-107">`text 1`: *String*</span></span>

<span data-ttu-id="23fc7-108">Ein Verweis auf eine Datenquelle des Datensatztyps *String*.</span><span class="sxs-lookup"><span data-stu-id="23fc7-108">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="23fc7-109">Dieses Argument ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="23fc7-109">This argument is required.</span></span>

<span data-ttu-id="23fc7-110">`text N`: *String*</span><span class="sxs-lookup"><span data-stu-id="23fc7-110">`text N`: *String*</span></span>

<span data-ttu-id="23fc7-111">Ein Verweis auf eine Datenquelle des Datensatztyps *String*.</span><span class="sxs-lookup"><span data-stu-id="23fc7-111">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="23fc7-112">Diese zusätzlichen Argumente sind optional.</span><span class="sxs-lookup"><span data-stu-id="23fc7-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="23fc7-113">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="23fc7-113">Return values</span></span>

<span data-ttu-id="23fc7-114">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="23fc7-114">*String*</span></span>

<span data-ttu-id="23fc7-115">Der resultierende Textwert.</span><span class="sxs-lookup"><span data-stu-id="23fc7-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="23fc7-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="23fc7-116">Example</span></span>

<span data-ttu-id="23fc7-117">`CONCATENATE ("abc", "def")` gibt **"abcdef"** zurück.</span><span class="sxs-lookup"><span data-stu-id="23fc7-117">`CONCATENATE ("abc", "def")` returns **"abcdef"**.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="23fc7-118">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="23fc7-118">Usage notes</span></span>

<span data-ttu-id="23fc7-119">Der Ausdruck `"abc" & "def"` gibt auch **"abcdef"** zurück.</span><span class="sxs-lookup"><span data-stu-id="23fc7-119">The expression `"abc" & "def"` also returns **"abcdef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="23fc7-120">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="23fc7-120">Additional resources</span></span>

[<span data-ttu-id="23fc7-121">Textfunktionen</span><span class="sxs-lookup"><span data-stu-id="23fc7-121">Text functions</span></span>](er-functions-category-text.md)
