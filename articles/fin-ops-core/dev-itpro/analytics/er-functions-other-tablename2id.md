---
title: TABLENAME2ID EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der TABLENAME2ID-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a68a8e1f4afa378ab446eae12bc90cdb3aba8b19
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681157"
---
# <a name="tablename2id-er-function"></a><span data-ttu-id="e7aba-103">TABLENAME2ID EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="e7aba-103">TABLENAME2ID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e7aba-104">Die Funktion `TABLENAME2ID` gibt eine numerische Darstellung der Tabellen-ID für den angegebenen Tabellennamen mit dem Wert *Integer* zurück.</span><span class="sxs-lookup"><span data-stu-id="e7aba-104">The `TABLENAME2ID` function returns a numeric representation of the table ID for the specified table name as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7aba-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7aba-105">Syntax</span></span>

```vb
TABLENAME2ID (text)
```

## <a name="arguments"></a><span data-ttu-id="e7aba-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="e7aba-106">Arguments</span></span>

<span data-ttu-id="e7aba-107">`text`: *String*</span><span class="sxs-lookup"><span data-stu-id="e7aba-107">`text`: *String*</span></span>

<span data-ttu-id="e7aba-108">Ein Textwert, der einen gültigen Tabellennamen darstellt.</span><span class="sxs-lookup"><span data-stu-id="e7aba-108">A text value that represents a valid table name.</span></span>

## <a name="return-values"></a><span data-ttu-id="e7aba-109">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="e7aba-109">Return values</span></span>

<span data-ttu-id="e7aba-110">*Ganze Zahl*</span><span class="sxs-lookup"><span data-stu-id="e7aba-110">*Integer*</span></span>

<span data-ttu-id="e7aba-111">Der resultierende numerische Wert.</span><span class="sxs-lookup"><span data-stu-id="e7aba-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="e7aba-112">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="e7aba-112">Usage notes</span></span>

<span data-ttu-id="e7aba-113">Die Ausführung dieser Funktion kann in verschiedenen Instanzen von Microsoft Dynamics 365 Finance zu unterschiedlichen Ergebnissen führen, auch wenn derselbe Firmenname verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e7aba-113">Execution of this function can have different results in different instances of Microsoft Dynamics 365 Finance, even if the same company name is used.</span></span>

## <a name="example"></a><span data-ttu-id="e7aba-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e7aba-114">Example</span></span>

<span data-ttu-id="e7aba-115">`TABLENAME2ID ("Intrastat")` gibt **1510** zurück.</span><span class="sxs-lookup"><span data-stu-id="e7aba-115">`TABLENAME2ID ("Intrastat")` returns **1510**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e7aba-116">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e7aba-116">Additional resources</span></span>

[<span data-ttu-id="e7aba-117">Andere (geschäftsdomänenspezifische) Funktionen</span><span class="sxs-lookup"><span data-stu-id="e7aba-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
