---
title: CN_GBT_ADDITIONALDIMENSIONID EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der CN_GBT_ADDITIONALDIMENSIONID-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 7fdc4527bc6115bdb3fca9d6a92d3d77a7c264c2
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744430"
---
# <a name="cn_gbt_additionaldimensionid-er-function"></a><span data-ttu-id="83f11-103">CN_GBT_ADDITIONALDIMENSIONID EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="83f11-103">CN_GBT_ADDITIONALDIMENSIONID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="83f11-104">Die Funktion `CN_GBT_ADDITIONALDIMENSIONID` gibt den Wert *String* zurück, der eine einzelne Finanzdimensions-ID darstellt, die der angegebenen Zeichenfolge entnommen wird.</span><span class="sxs-lookup"><span data-stu-id="83f11-104">The `CN_GBT_ADDITIONALDIMENSIONID` function returns a *String* value that represents a single financial dimension ID that is taken from the specified string.</span></span> <span data-ttu-id="83f11-105">Die angegebene Zeichenfolge zeigt alle Dimensionen als durch Kommata getrennte ID-Listen an.</span><span class="sxs-lookup"><span data-stu-id="83f11-105">The specified string presents all dimensions as a comma-separated list of IDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="83f11-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="83f11-106">Syntax</span></span>

```vb
CN_GBT_ADDITIONALDIMENSIONID (text, number)
```

## <a name="arguments"></a><span data-ttu-id="83f11-107">Argumente</span><span class="sxs-lookup"><span data-stu-id="83f11-107">Arguments</span></span>

<span data-ttu-id="83f11-108">`text`: *String*</span><span class="sxs-lookup"><span data-stu-id="83f11-108">`text`: *String*</span></span>

<span data-ttu-id="83f11-109">Der Wert *String* zeigt alle Dimensionen als durch Kommata getrennte ID-Listen an.</span><span class="sxs-lookup"><span data-stu-id="83f11-109">A *String* value that presents all dimensions as a comma-separated list of IDs.</span></span>

<span data-ttu-id="83f11-110">`number`: Integer</span><span class="sxs-lookup"><span data-stu-id="83f11-110">`number`: Integer</span></span>

<span data-ttu-id="83f11-111">Der Wert *Integer*, der den Sequenzcode der gewünschten Dimension in der angegebenen Zeichenfolge definiert.</span><span class="sxs-lookup"><span data-stu-id="83f11-111">An *Integer* value that defines the sequence code of the requested dimension in the specified string.</span></span>

## <a name="return-values"></a><span data-ttu-id="83f11-112">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="83f11-112">Return values</span></span>

<span data-ttu-id="83f11-113">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="83f11-113">*String*</span></span>

<span data-ttu-id="83f11-114">Der resultierende Textwert.</span><span class="sxs-lookup"><span data-stu-id="83f11-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="83f11-115">Beispiel</span><span class="sxs-lookup"><span data-stu-id="83f11-115">Example</span></span>

<span data-ttu-id="83f11-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` gibt **"CC"** zurück.</span><span class="sxs-lookup"><span data-stu-id="83f11-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` returns **"CC"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="83f11-117">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="83f11-117">Additional resources</span></span>

[<span data-ttu-id="83f11-118">Andere (geschäftsdomänenspezifische) Funktionen</span><span class="sxs-lookup"><span data-stu-id="83f11-118">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
