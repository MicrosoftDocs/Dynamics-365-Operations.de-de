---
title: TABLENAME2ID EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der TABLENAME2ID-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 49370af4ebb7552dd3aff4512890fd93fa67c72d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563269"
---
# <a name="tablename2id-er-function"></a><span data-ttu-id="8bb4f-103">TABLENAME2ID EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="8bb4f-103">TABLENAME2ID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8bb4f-104">Die Funktion `TABLENAME2ID` gibt eine numerische Darstellung der Tabellen-ID für den angegebenen Tabellennamen mit dem Wert *Integer* zurück.</span><span class="sxs-lookup"><span data-stu-id="8bb4f-104">The `TABLENAME2ID` function returns a numeric representation of the table ID for the specified table name as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bb4f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8bb4f-105">Syntax</span></span>

```vb
TABLENAME2ID (text)
```

## <a name="arguments"></a><span data-ttu-id="8bb4f-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="8bb4f-106">Arguments</span></span>

<span data-ttu-id="8bb4f-107">`text`: *String*</span><span class="sxs-lookup"><span data-stu-id="8bb4f-107">`text`: *String*</span></span>

<span data-ttu-id="8bb4f-108">Ein Textwert, der einen gültigen Tabellennamen darstellt.</span><span class="sxs-lookup"><span data-stu-id="8bb4f-108">A text value that represents a valid table name.</span></span>

## <a name="return-values"></a><span data-ttu-id="8bb4f-109">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="8bb4f-109">Return values</span></span>

<span data-ttu-id="8bb4f-110">*Ganze Zahl*</span><span class="sxs-lookup"><span data-stu-id="8bb4f-110">*Integer*</span></span>

<span data-ttu-id="8bb4f-111">Der resultierende numerische Wert.</span><span class="sxs-lookup"><span data-stu-id="8bb4f-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="8bb4f-112">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="8bb4f-112">Usage notes</span></span>

<span data-ttu-id="8bb4f-113">Die Ausführung dieser Funktion kann in verschiedenen Instanzen von Microsoft Dynamics 365 Finance zu unterschiedlichen Ergebnissen führen, auch wenn derselbe Firmenname verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8bb4f-113">Execution of this function can have different results in different instances of Microsoft Dynamics 365 Finance, even if the same company name is used.</span></span>

## <a name="example"></a><span data-ttu-id="8bb4f-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="8bb4f-114">Example</span></span>

<span data-ttu-id="8bb4f-115">`TABLENAME2ID ("Intrastat")` gibt **1510** zurück.</span><span class="sxs-lookup"><span data-stu-id="8bb4f-115">`TABLENAME2ID ("Intrastat")` returns **1510**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8bb4f-116">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8bb4f-116">Additional resources</span></span>

[<span data-ttu-id="8bb4f-117">Andere (geschäftsdomänenspezifische) Funktionen</span><span class="sxs-lookup"><span data-stu-id="8bb4f-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]