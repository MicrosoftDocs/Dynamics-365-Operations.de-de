---
title: LEFT EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der LEFT-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 6f1ec7a21a16c3a34bed9779b05f20f21815ab9d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569991"
---
# <a name="left-er-function"></a><span data-ttu-id="111d1-103">LEFT EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="111d1-103">LEFT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="111d1-104">Die Funktion `LEFT` gibt den Wert *String* zurück, der die angegebene Anzahl von Zeichen ab dem Anfang der angegebenen Zeichenfolge angibt.</span><span class="sxs-lookup"><span data-stu-id="111d1-104">The `LEFT` function returns a *String* value that presents the specified number of characters from the start of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="111d1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="111d1-105">Syntax</span></span>

```vb
LEFT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="111d1-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="111d1-106">Arguments</span></span>

<span data-ttu-id="111d1-107">`text`: *String*</span><span class="sxs-lookup"><span data-stu-id="111d1-107">`text`: *String*</span></span>

<span data-ttu-id="111d1-108">Der Wert *String*, der den Originaltext darstellt.</span><span class="sxs-lookup"><span data-stu-id="111d1-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="111d1-109">`number`: *Integer*</span><span class="sxs-lookup"><span data-stu-id="111d1-109">`number`: *Integer*</span></span>

<span data-ttu-id="111d1-110">Die Anzahl der Zeichen, die vom Start des Originaltexts zurückgegeben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="111d1-110">The number of characters that must be returned from the start of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="111d1-111">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="111d1-111">Return values</span></span>

<span data-ttu-id="111d1-112">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="111d1-112">*String*</span></span>

<span data-ttu-id="111d1-113">Der resultierende Textwert.</span><span class="sxs-lookup"><span data-stu-id="111d1-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="111d1-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="111d1-114">Example</span></span>

<span data-ttu-id="111d1-115">`LEFT ("Sample", 3)` gibt **"Sam"** zurück.</span><span class="sxs-lookup"><span data-stu-id="111d1-115">`LEFT ("Sample", 3)` returns **"Sam"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="111d1-116">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="111d1-116">Additional resources</span></span>

[<span data-ttu-id="111d1-117">Textfunktionen</span><span class="sxs-lookup"><span data-stu-id="111d1-117">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]