---
title: LOWER EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der LOWER-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: ad971bd78fa1da17be916efcc6857aa32575f7ac
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680313"
---
# <a name="lower-er-function"></a><span data-ttu-id="772ce-103">LOWER EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="772ce-103">LOWER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="772ce-104">Die Funktion `LOWER` gibt die angegebene Textzeichenfolge mit dem Wert *String* zurück, nachdem er in Kleinbuchstaben umgewandelt wurde.</span><span class="sxs-lookup"><span data-stu-id="772ce-104">The `LOWER` function returns the specified text string as a *String* value after it has been converted to lowercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="772ce-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="772ce-105">Syntax</span></span>

```vb
LOWER (text)
```

## <a name="arguments"></a><span data-ttu-id="772ce-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="772ce-106">Arguments</span></span>

<span data-ttu-id="772ce-107">`text`: *String*</span><span class="sxs-lookup"><span data-stu-id="772ce-107">`text`: *String*</span></span>

<span data-ttu-id="772ce-108">Der Wert *String*, der den Text angibt.</span><span class="sxs-lookup"><span data-stu-id="772ce-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="772ce-109">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="772ce-109">Return values</span></span>

<span data-ttu-id="772ce-110">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="772ce-110">*String*</span></span>

<span data-ttu-id="772ce-111">Der resultierende Textwert.</span><span class="sxs-lookup"><span data-stu-id="772ce-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="772ce-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="772ce-112">Example</span></span>

<span data-ttu-id="772ce-113">`LOWER ("Sample")` gibt **"sample"** zurück.</span><span class="sxs-lookup"><span data-stu-id="772ce-113">`LOWER ("Sample")` returns **"sample"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="772ce-114">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="772ce-114">Additional resources</span></span>

[<span data-ttu-id="772ce-115">Textfunktionen</span><span class="sxs-lookup"><span data-stu-id="772ce-115">Text functions</span></span>](er-functions-category-text.md)
