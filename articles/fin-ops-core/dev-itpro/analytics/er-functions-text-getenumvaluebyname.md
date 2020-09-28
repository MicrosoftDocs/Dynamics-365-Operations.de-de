---
title: GETENUMVALUEBYNAME EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der GETENUMVALUEBYNAME-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: 33ccf358dc5355cd00d5ff41ebd8148a334cba38
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743854"
---
# <a name="getenumvaluebyname-er-function"></a><span data-ttu-id="0c84c-103">GETENUMVALUEBYNAME EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="0c84c-103">GETENUMVALUEBYNAME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0c84c-104">Die Funktion `GETENUMVALUEBYNAME` sucht nach dem bestimmten Wert *Enum* in der angegebenen Aufzählungsdatenquelle unter Verwendung des Aufzählungsnamens, der mit dem Wert *String* angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="0c84c-104">The `GETENUMVALUEBYNAME` function searches for a specific *Enum* value in the specified enumeration data source by using the enumeration name that is specified as a *String* value.</span></span> <span data-ttu-id="0c84c-105">Wenn der Wert *Enum* gefunden wird, gibt die Funktion ihn zurück.</span><span class="sxs-lookup"><span data-stu-id="0c84c-105">If the *Enum* value is found, the function returns it.</span></span> <span data-ttu-id="0c84c-106">Andernfalls gibt die Funktion den Aufzählungswert **Null** zurück.</span><span class="sxs-lookup"><span data-stu-id="0c84c-106">Otherwise, the function returns the **null** enumeration value.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c84c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c84c-107">Syntax</span></span>

```vb
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a><span data-ttu-id="0c84c-108">Argumente</span><span class="sxs-lookup"><span data-stu-id="0c84c-108">Arguments</span></span>

<span data-ttu-id="0c84c-109">`enumeration data source path`: *Aufzählung*</span><span class="sxs-lookup"><span data-stu-id="0c84c-109">`enumeration data source path`: *Enumeration*</span></span>

<span data-ttu-id="0c84c-110">Der gültige Pfad einer Datenquelle eines der folgenden Aufzählungstypen:</span><span class="sxs-lookup"><span data-stu-id="0c84c-110">The valid path of a data source of one of the following enumeration types:</span></span>

- <span data-ttu-id="0c84c-111">Modellenumeration für die elektronische Berichterstellung (EB)</span><span class="sxs-lookup"><span data-stu-id="0c84c-111">Electronic reporting (ER) model enumeration</span></span>
- <span data-ttu-id="0c84c-112">EB-Formatenumeration</span><span class="sxs-lookup"><span data-stu-id="0c84c-112">ER format enumeration</span></span>
- <span data-ttu-id="0c84c-113">Microsoft Dynamics 365 Finance-Enumeration</span><span class="sxs-lookup"><span data-stu-id="0c84c-113">Microsoft Dynamics 365 Finance enumeration</span></span>

<span data-ttu-id="0c84c-114">`enumeration value text`: *String*</span><span class="sxs-lookup"><span data-stu-id="0c84c-114">`enumeration value text`: *String*</span></span>

<span data-ttu-id="0c84c-115">Ein Zeichenfolgewert, der den Namen eines einzelnen Aufzählungswerts darstellt.</span><span class="sxs-lookup"><span data-stu-id="0c84c-115">A string value that represents the name of a single enumeration value.</span></span>

## <a name="return-values"></a><span data-ttu-id="0c84c-116">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="0c84c-116">Return values</span></span>

<span data-ttu-id="0c84c-117">Nullbar *Enum*</span><span class="sxs-lookup"><span data-stu-id="0c84c-117">Nullable *Enum*</span></span>

<span data-ttu-id="0c84c-118">Der resultierende Aufzählungswert.</span><span class="sxs-lookup"><span data-stu-id="0c84c-118">The resulting enumeration value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="0c84c-119">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="0c84c-119">Usage notes</span></span>

<span data-ttu-id="0c84c-120">Es wird keine Ausnahme ausgelöst, wenn ein Wert *Enum* nicht unter Verwendung des Namens des Aufzählungswerts gefunden wird, der mit dem Wert *String* angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="0c84c-120">No exception is thrown if an *Enum* value isn't found by using the name of the enumeration value that is specified as a *String* value.</span></span>

## <a name="example"></a><span data-ttu-id="0c84c-121">Beispiel</span><span class="sxs-lookup"><span data-stu-id="0c84c-121">Example</span></span>

<span data-ttu-id="0c84c-122">In der folgenden Abbildung wird die Aufzählung **ReportDirection** in einem Datenmodell eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0c84c-122">In the following illustration, the **ReportDirection** enumeration is introduced in a data model.</span></span> <span data-ttu-id="0c84c-123">Beachten Sie, dass Beschriftungen für Enumerationswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="0c84c-123">Notice that labels are defined for the enumeration values.</span></span>

<p><a href="./media/ER-data-model-enumeration-values.PNG"><img src="./media/ER-data-model-enumeration-values.PNG" alt="Available values for a data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

<span data-ttu-id="0c84c-124">Die folgende Abbildung zeigt diese Details an:</span><span class="sxs-lookup"><span data-stu-id="0c84c-124">The following illustration shows these details:</span></span>

- <span data-ttu-id="0c84c-125">Die Datenquelle **$Direction** wird in einem EB-Bericht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="0c84c-125">The **$Direction** data source is configured in an ER report.</span></span> <span data-ttu-id="0c84c-126">Diese Datenquelle wird basierend auf der Modellenumeration **ReportDirection** konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="0c84c-126">This data source is configured based on the **ReportDirection** model enumeration.</span></span>
- <span data-ttu-id="0c84c-127">Der Ausdruck `$IsArrivals` ist dazu konzipiert, die auf der Modellenumeration basierende Datenquelle **$Direction** als Parameter dieser Funktion zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="0c84c-127">The `$IsArrivals` expression is designed to use the model enumeration–based **$Direction** data source as a parameter of this function.</span></span>
- <span data-ttu-id="0c84c-128">Der Wert dieses Vergleichswerts lautet **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="0c84c-128">The value of this comparison expression is **TRUE**.</span></span>

<a href="./media/ER-data-model-enumeration-usage.PNG"><img src="./media/ER-data-model-enumeration-usage.PNG" alt="Example of data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

## <a name="additional-resources"></a><span data-ttu-id="0c84c-129">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0c84c-129">Additional resources</span></span>

[<span data-ttu-id="0c84c-130">Textfunktionen</span><span class="sxs-lookup"><span data-stu-id="0c84c-130">Text functions</span></span>](er-functions-category-text.md)
