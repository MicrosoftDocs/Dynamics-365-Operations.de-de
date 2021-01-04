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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 38908c63c35465747505479bc983ada891f9e2bf
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686809"
---
# <a name="cn_gbt_additionaldimensionid-er-function"></a><span data-ttu-id="a7c0e-103">CN_GBT_ADDITIONALDIMENSIONID EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="a7c0e-103">CN_GBT_ADDITIONALDIMENSIONID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a7c0e-104">Die Funktion `CN_GBT_ADDITIONALDIMENSIONID` gibt den Wert *String* zurück, der eine einzelne Finanzdimensions-ID darstellt, die der angegebenen Zeichenfolge entnommen wird.</span><span class="sxs-lookup"><span data-stu-id="a7c0e-104">The `CN_GBT_ADDITIONALDIMENSIONID` function returns a *String* value that represents a single financial dimension ID that is taken from the specified string.</span></span> <span data-ttu-id="a7c0e-105">Die angegebene Zeichenfolge zeigt alle Dimensionen als durch Kommata getrennte ID-Listen an.</span><span class="sxs-lookup"><span data-stu-id="a7c0e-105">The specified string presents all dimensions as a comma-separated list of IDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7c0e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7c0e-106">Syntax</span></span>

```vb
CN_GBT_ADDITIONALDIMENSIONID (text, number)
```

## <a name="arguments"></a><span data-ttu-id="a7c0e-107">Argumente</span><span class="sxs-lookup"><span data-stu-id="a7c0e-107">Arguments</span></span>

<span data-ttu-id="a7c0e-108">`text`: *String*</span><span class="sxs-lookup"><span data-stu-id="a7c0e-108">`text`: *String*</span></span>

<span data-ttu-id="a7c0e-109">Der Wert *String* zeigt alle Dimensionen als durch Kommata getrennte ID-Listen an.</span><span class="sxs-lookup"><span data-stu-id="a7c0e-109">A *String* value that presents all dimensions as a comma-separated list of IDs.</span></span>

<span data-ttu-id="a7c0e-110">`number`: Integer</span><span class="sxs-lookup"><span data-stu-id="a7c0e-110">`number`: Integer</span></span>

<span data-ttu-id="a7c0e-111">Der Wert *Integer*, der den Sequenzcode der gewünschten Dimension in der angegebenen Zeichenfolge definiert.</span><span class="sxs-lookup"><span data-stu-id="a7c0e-111">An *Integer* value that defines the sequence code of the requested dimension in the specified string.</span></span>

## <a name="return-values"></a><span data-ttu-id="a7c0e-112">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="a7c0e-112">Return values</span></span>

<span data-ttu-id="a7c0e-113">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="a7c0e-113">*String*</span></span>

<span data-ttu-id="a7c0e-114">Der resultierende Textwert.</span><span class="sxs-lookup"><span data-stu-id="a7c0e-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="a7c0e-115">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a7c0e-115">Example</span></span>

<span data-ttu-id="a7c0e-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` gibt **"CC"** zurück.</span><span class="sxs-lookup"><span data-stu-id="a7c0e-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` returns **"CC"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a7c0e-117">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a7c0e-117">Additional resources</span></span>

[<span data-ttu-id="a7c0e-118">Andere (geschäftsdomänenspezifische) Funktionen</span><span class="sxs-lookup"><span data-stu-id="a7c0e-118">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
