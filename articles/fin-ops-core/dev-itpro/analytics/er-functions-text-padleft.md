---
title: PADLEFT EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der PADLEFT-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 268941d8bc0bd4dc6de6d2597c05a11c1f530f15
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680145"
---
# <a name="padleft-er-function"></a><span data-ttu-id="9a294-103">PADLEFT EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="9a294-103">PADLEFT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9a294-104">Die Funktion `PADLEFT` gibt den Wert *String* mit der angegebenen Länge zurück, bei der der Anfang der angegebenen Zeichenfolge mit den angegebenen Zeichen aufgefüllt ist.</span><span class="sxs-lookup"><span data-stu-id="9a294-104">The `PADLEFT` function returns a *String* value of the specified length, where the start of the specified string is padded with the specified characters.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a294-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a294-105">Syntax</span></span>

```vb
PADLEFT (text, length, padding chars)
```

## <a name="arguments"></a><span data-ttu-id="9a294-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="9a294-106">Arguments</span></span>

<span data-ttu-id="9a294-107">`text`: *String*</span><span class="sxs-lookup"><span data-stu-id="9a294-107">`text`: *String*</span></span>

<span data-ttu-id="9a294-108">Der Wert *String*, der den Originaltext darstellt.</span><span class="sxs-lookup"><span data-stu-id="9a294-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="9a294-109">`length`: *Integer*</span><span class="sxs-lookup"><span data-stu-id="9a294-109">`length`: *Integer*</span></span>

<span data-ttu-id="9a294-110">Der Wert *Integer*, der die endgültige Anzahl von Zeichen in der aufgefüllten Zeichenfolge darstellt.</span><span class="sxs-lookup"><span data-stu-id="9a294-110">An *Integer* value that represents the final number of characters in the padded string.</span></span>

<span data-ttu-id="9a294-111">`padding chars`: *String*</span><span class="sxs-lookup"><span data-stu-id="9a294-111">`padding chars`: *String*</span></span>

<span data-ttu-id="9a294-112">Die Zeichen, die zum Auffüllen verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9a294-112">The characters to use for padding.</span></span>

## <a name="return-values"></a><span data-ttu-id="9a294-113">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="9a294-113">Return values</span></span>

<span data-ttu-id="9a294-114">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="9a294-114">*String*</span></span>

<span data-ttu-id="9a294-115">Der resultierende Textwert.</span><span class="sxs-lookup"><span data-stu-id="9a294-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="9a294-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="9a294-116">Example</span></span>

<span data-ttu-id="9a294-117">`PADLEFT ("1234", 10, "`&nbsp;`")` gibt die Textzeichenfolge **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"** zurück.</span><span class="sxs-lookup"><span data-stu-id="9a294-117">`PADLEFT ("1234", 10, "`&nbsp;`")` returns the text string **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9a294-118">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9a294-118">Additional resources</span></span>

[<span data-ttu-id="9a294-119">Textfunktionen</span><span class="sxs-lookup"><span data-stu-id="9a294-119">Text functions</span></span>](er-functions-category-text.md)
