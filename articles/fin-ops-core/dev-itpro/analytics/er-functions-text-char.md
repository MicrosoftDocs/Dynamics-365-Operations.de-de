---
title: CHAR EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der CHAR-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: d42afcf97690351763138fd9e16265aa104a6bc4
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915739"
---
# <span data-ttu-id="6fa1e-103"><a name="CHAR">CHAR EB-Funktion</a></span><span class="sxs-lookup"><span data-stu-id="6fa1e-103"><a name="CHAR">CHAR ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6fa1e-104">Die Funktion `CHAR` gibt den Wert *String* zurück, der ein einzelnes Zeichen darstellt, auf das durch die angegebene Unicode-Nummer verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="6fa1e-104">The `CHAR` function returns a *String* value that presents a single character that is referenced by the specified Unicode number.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fa1e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6fa1e-105">Syntax</span></span>

```
CHAR (number)
```

## <a name="arguments"></a><span data-ttu-id="6fa1e-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="6fa1e-106">Arguments</span></span>

<span data-ttu-id="6fa1e-107">`number`: *Integer*</span><span class="sxs-lookup"><span data-stu-id="6fa1e-107">`number`: *Integer*</span></span>

<span data-ttu-id="6fa1e-108">Eine Zahl, die einem erwarteten einzelnen Zeichen entspricht.</span><span class="sxs-lookup"><span data-stu-id="6fa1e-108">A number that corresponds to an expected single character.</span></span>

## <a name="return-values"></a><span data-ttu-id="6fa1e-109">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="6fa1e-109">Return values</span></span>

<span data-ttu-id="6fa1e-110">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="6fa1e-110">*String*</span></span>

<span data-ttu-id="6fa1e-111">Der resultierende Textwert.</span><span class="sxs-lookup"><span data-stu-id="6fa1e-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="6fa1e-112">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="6fa1e-112">Usage notes</span></span>

<span data-ttu-id="6fa1e-113">Die Zeichenfolge, die diese Funktion zurückgibt, hängt von der Codierung ab, die im übergeordneten **DATEI**-Formatelement ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="6fa1e-113">The string that this function returns depends on the encoding that is selected in the parent **FILE** format element.</span></span> <span data-ttu-id="6fa1e-114">Eine Liste der unterstützten Codierungen erhalten Sie unter [Codierungsklasse](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="6fa1e-114">For a list of the supported encodings, see [Encoding class](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).</span></span>

## <a name="example"></a><span data-ttu-id="6fa1e-115">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6fa1e-115">Example</span></span>

<span data-ttu-id="6fa1e-116">`CHAR (255)` gibt **"ÿ"** zurück.</span><span class="sxs-lookup"><span data-stu-id="6fa1e-116">`CHAR (255)` returns **"ÿ"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6fa1e-117">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6fa1e-117">Additional resources</span></span>

[<span data-ttu-id="6fa1e-118">Textfunktionen</span><span class="sxs-lookup"><span data-stu-id="6fa1e-118">Text functions</span></span>](er-functions-category-text.md)
