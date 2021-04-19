---
title: PADLEFT EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der PADLEFT-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
ms.date: 12/10/2019
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
ms.openlocfilehash: 806b1d318f18b0ade01f7b03909c90b1e4fd29b1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746242"
---
# <a name="padleft-er-function"></a><span data-ttu-id="d41c8-103">PADLEFT EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="d41c8-103">PADLEFT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d41c8-104">Die Funktion `PADLEFT` gibt den Wert *String* mit der angegebenen Länge zurück, bei der der Anfang der angegebenen Zeichenfolge mit den angegebenen Zeichen aufgefüllt ist.</span><span class="sxs-lookup"><span data-stu-id="d41c8-104">The `PADLEFT` function returns a *String* value of the specified length, where the start of the specified string is padded with the specified characters.</span></span>

## <a name="syntax"></a><span data-ttu-id="d41c8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d41c8-105">Syntax</span></span>

```vb
PADLEFT (text, length, padding chars)
```

## <a name="arguments"></a><span data-ttu-id="d41c8-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="d41c8-106">Arguments</span></span>

<span data-ttu-id="d41c8-107">`text`: *String*</span><span class="sxs-lookup"><span data-stu-id="d41c8-107">`text`: *String*</span></span>

<span data-ttu-id="d41c8-108">Der Wert *String*, der den Originaltext darstellt.</span><span class="sxs-lookup"><span data-stu-id="d41c8-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="d41c8-109">`length`: *Integer*</span><span class="sxs-lookup"><span data-stu-id="d41c8-109">`length`: *Integer*</span></span>

<span data-ttu-id="d41c8-110">Der Wert *Integer*, der die endgültige Anzahl von Zeichen in der aufgefüllten Zeichenfolge darstellt.</span><span class="sxs-lookup"><span data-stu-id="d41c8-110">An *Integer* value that represents the final number of characters in the padded string.</span></span>

<span data-ttu-id="d41c8-111">`padding chars`: *String*</span><span class="sxs-lookup"><span data-stu-id="d41c8-111">`padding chars`: *String*</span></span>

<span data-ttu-id="d41c8-112">Die Zeichen, die zum Auffüllen verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d41c8-112">The characters to use for padding.</span></span>

## <a name="return-values"></a><span data-ttu-id="d41c8-113">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="d41c8-113">Return values</span></span>

<span data-ttu-id="d41c8-114">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="d41c8-114">*String*</span></span>

<span data-ttu-id="d41c8-115">Der resultierende Textwert.</span><span class="sxs-lookup"><span data-stu-id="d41c8-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="d41c8-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d41c8-116">Example</span></span>

<span data-ttu-id="d41c8-117">`PADLEFT ("1234", 10, "`&nbsp;`")` gibt die Textzeichenfolge **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"** zurück.</span><span class="sxs-lookup"><span data-stu-id="d41c8-117">`PADLEFT ("1234", 10, "`&nbsp;`")` returns the text string **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d41c8-118">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d41c8-118">Additional resources</span></span>

[<span data-ttu-id="d41c8-119">Textfunktionen</span><span class="sxs-lookup"><span data-stu-id="d41c8-119">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]