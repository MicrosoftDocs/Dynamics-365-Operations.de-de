---
title: RIGHT EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der RIGHT-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: 01718f9b153c1d6c46d50a9b17e899ccfba16915
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916728"
---
# <span data-ttu-id="34ba5-103"><a name="RIGHT">RIGHT EB-Funktion</a></span><span class="sxs-lookup"><span data-stu-id="34ba5-103"><a name="RIGHT">RIGHT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="34ba5-104">Die Funktion `RIGHT` gibt den Wert *String* zurück, der die angegebene Anzahl von Zeichen ab dem Ende der angegebenen Zeichenfolge angibt.</span><span class="sxs-lookup"><span data-stu-id="34ba5-104">The `RIGHT` function returns a *String* value that presents the specified number of characters from the end of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="34ba5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="34ba5-105">Syntax</span></span>

```
RIGHT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="34ba5-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="34ba5-106">Arguments</span></span>

<span data-ttu-id="34ba5-107">`text`: *String*</span><span class="sxs-lookup"><span data-stu-id="34ba5-107">`text`: *String*</span></span>

<span data-ttu-id="34ba5-108">Der Wert *String*, der den Originaltext darstellt.</span><span class="sxs-lookup"><span data-stu-id="34ba5-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="34ba5-109">`number`: *Integer*</span><span class="sxs-lookup"><span data-stu-id="34ba5-109">`number`: *Integer*</span></span>

<span data-ttu-id="34ba5-110">Die Anzahl der Zeichen, die vom Ende des Originaltexts zurückgegeben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="34ba5-110">The number of characters that must be returned from the end of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="34ba5-111">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="34ba5-111">Return values</span></span>

<span data-ttu-id="34ba5-112">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="34ba5-112">*String*</span></span>

<span data-ttu-id="34ba5-113">Der resultierende Textwert.</span><span class="sxs-lookup"><span data-stu-id="34ba5-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="34ba5-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="34ba5-114">Example</span></span>

<span data-ttu-id="34ba5-115">`RIGHT ("Sample", 3)` gibt **"ple"** zurück.</span><span class="sxs-lookup"><span data-stu-id="34ba5-115">`RIGHT ("Sample", 3)` returns **"ple"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="34ba5-116">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="34ba5-116">Additional resources</span></span>

[<span data-ttu-id="34ba5-117">Textfunktionen</span><span class="sxs-lookup"><span data-stu-id="34ba5-117">Text functions</span></span>](er-functions-category-text.md)
