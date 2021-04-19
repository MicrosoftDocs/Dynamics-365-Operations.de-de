---
title: CONCATENATE EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der CONCATENATE-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: f1a47a05127412588f4628cb425eab0379493c3c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746481"
---
# <a name="concatenate-er-function"></a><span data-ttu-id="85675-103">CONCATENATE EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="85675-103">CONCATENATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="85675-104">Die Funktion `CONCATENATE` gibt alle angegebenen Textzeichenfolgen mit dem Wert *String* zurück, nachdem sie zu einer Zeichenfolge zusammengefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="85675-104">The `CONCATENATE` function returns all the specified text strings as a *String* value after they have been joined into one string.</span></span>

## <a name="syntax"></a><span data-ttu-id="85675-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="85675-105">Syntax</span></span>

```vb
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a><span data-ttu-id="85675-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="85675-106">Arguments</span></span>

<span data-ttu-id="85675-107">`text 1`: *String*</span><span class="sxs-lookup"><span data-stu-id="85675-107">`text 1`: *String*</span></span>

<span data-ttu-id="85675-108">Ein Verweis auf eine Datenquelle des Datensatztyps *String*.</span><span class="sxs-lookup"><span data-stu-id="85675-108">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="85675-109">Dieses Argument ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="85675-109">This argument is required.</span></span>

<span data-ttu-id="85675-110">`text N`: *String*</span><span class="sxs-lookup"><span data-stu-id="85675-110">`text N`: *String*</span></span>

<span data-ttu-id="85675-111">Ein Verweis auf eine Datenquelle des Datensatztyps *String*.</span><span class="sxs-lookup"><span data-stu-id="85675-111">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="85675-112">Diese zusätzlichen Argumente sind optional.</span><span class="sxs-lookup"><span data-stu-id="85675-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="85675-113">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="85675-113">Return values</span></span>

<span data-ttu-id="85675-114">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="85675-114">*String*</span></span>

<span data-ttu-id="85675-115">Der resultierende Textwert.</span><span class="sxs-lookup"><span data-stu-id="85675-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="85675-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="85675-116">Example</span></span>

<span data-ttu-id="85675-117">`CONCATENATE ("abc", "def")` gibt **"abcdef"** zurück.</span><span class="sxs-lookup"><span data-stu-id="85675-117">`CONCATENATE ("abc", "def")` returns **"abcdef"**.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="85675-118">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="85675-118">Usage notes</span></span>

<span data-ttu-id="85675-119">Der Ausdruck `"abc" & "def"` gibt auch **"abcdef"** zurück.</span><span class="sxs-lookup"><span data-stu-id="85675-119">The expression `"abc" & "def"` also returns **"abcdef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="85675-120">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="85675-120">Additional resources</span></span>

[<span data-ttu-id="85675-121">Textfunktionen</span><span class="sxs-lookup"><span data-stu-id="85675-121">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]