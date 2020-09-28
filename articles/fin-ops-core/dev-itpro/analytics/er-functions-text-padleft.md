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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3f8a8e2006fe279b25bbf154c6e1802babf51117
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744358"
---
# <a name="padleft-er-function"></a><span data-ttu-id="df9b6-103">PADLEFT EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="df9b6-103">PADLEFT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="df9b6-104">Die Funktion `PADLEFT` gibt den Wert *String* mit der angegebenen Länge zurück, bei der der Anfang der angegebenen Zeichenfolge mit den angegebenen Zeichen aufgefüllt ist.</span><span class="sxs-lookup"><span data-stu-id="df9b6-104">The `PADLEFT` function returns a *String* value of the specified length, where the start of the specified string is padded with the specified characters.</span></span>

## <a name="syntax"></a><span data-ttu-id="df9b6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="df9b6-105">Syntax</span></span>

```vb
PADLEFT (text, length, padding chars)
```

## <a name="arguments"></a><span data-ttu-id="df9b6-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="df9b6-106">Arguments</span></span>

<span data-ttu-id="df9b6-107">`text`: *String*</span><span class="sxs-lookup"><span data-stu-id="df9b6-107">`text`: *String*</span></span>

<span data-ttu-id="df9b6-108">Der Wert *String*, der den Originaltext darstellt.</span><span class="sxs-lookup"><span data-stu-id="df9b6-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="df9b6-109">`length`: *Integer*</span><span class="sxs-lookup"><span data-stu-id="df9b6-109">`length`: *Integer*</span></span>

<span data-ttu-id="df9b6-110">Der Wert *Integer*, der die endgültige Anzahl von Zeichen in der aufgefüllten Zeichenfolge darstellt.</span><span class="sxs-lookup"><span data-stu-id="df9b6-110">An *Integer* value that represents the final number of characters in the padded string.</span></span>

<span data-ttu-id="df9b6-111">`padding chars`: *String*</span><span class="sxs-lookup"><span data-stu-id="df9b6-111">`padding chars`: *String*</span></span>

<span data-ttu-id="df9b6-112">Die Zeichen, die zum Auffüllen verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="df9b6-112">The characters to use for padding.</span></span>

## <a name="return-values"></a><span data-ttu-id="df9b6-113">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="df9b6-113">Return values</span></span>

<span data-ttu-id="df9b6-114">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="df9b6-114">*String*</span></span>

<span data-ttu-id="df9b6-115">Der resultierende Textwert.</span><span class="sxs-lookup"><span data-stu-id="df9b6-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="df9b6-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="df9b6-116">Example</span></span>

<span data-ttu-id="df9b6-117">`PADLEFT ("1234", 10, "`&nbsp;`")` gibt die Textzeichenfolge **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"** zurück.</span><span class="sxs-lookup"><span data-stu-id="df9b6-117">`PADLEFT ("1234", 10, "`&nbsp;`")` returns the text string **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="df9b6-118">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="df9b6-118">Additional resources</span></span>

[<span data-ttu-id="df9b6-119">Textfunktionen</span><span class="sxs-lookup"><span data-stu-id="df9b6-119">Text functions</span></span>](er-functions-category-text.md)
