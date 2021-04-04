---
title: LEN EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der LEN-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: fce4b5311d84364310b76545a775f1cc8db2fd70
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569967"
---
# <a name="len-er-function"></a><span data-ttu-id="687e2-103">LEN EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="687e2-103">LEN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="687e2-104">Die Funktion `LEN` gibt die angegebene Anzahl von Zeichen in der angegebenen Zeichenfolge mit dem Wert *Integer* zurück.</span><span class="sxs-lookup"><span data-stu-id="687e2-104">The `LEN` function returns the number of characters in the specified string as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="687e2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="687e2-105">Syntax</span></span>

```vb
LEN (text)
```

## <a name="arguments"></a><span data-ttu-id="687e2-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="687e2-106">Arguments</span></span>

<span data-ttu-id="687e2-107">`text`: *String*</span><span class="sxs-lookup"><span data-stu-id="687e2-107">`text`: *String*</span></span>

<span data-ttu-id="687e2-108">Der Wert *String*, der den Text angibt.</span><span class="sxs-lookup"><span data-stu-id="687e2-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="687e2-109">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="687e2-109">Return values</span></span>

<span data-ttu-id="687e2-110">*Ganze Zahl*</span><span class="sxs-lookup"><span data-stu-id="687e2-110">*Integer*</span></span>

<span data-ttu-id="687e2-111">Der resultierende numerische Wert.</span><span class="sxs-lookup"><span data-stu-id="687e2-111">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="687e2-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="687e2-112">Example</span></span>

<span data-ttu-id="687e2-113">`LEN ("Sample")` gibt **6** zurück.</span><span class="sxs-lookup"><span data-stu-id="687e2-113">`LEN ("Sample")` returns **6**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="687e2-114">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="687e2-114">Additional resources</span></span>

[<span data-ttu-id="687e2-115">Textfunktionen</span><span class="sxs-lookup"><span data-stu-id="687e2-115">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]