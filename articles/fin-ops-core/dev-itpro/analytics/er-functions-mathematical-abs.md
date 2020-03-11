---
title: ABS EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der ABS-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: 214fb2808f024487795f27de45de1d4de8cead2d
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041652"
---
# <span data-ttu-id="4ef7f-103"><a name="ABS">ABS EB-Funktion</a></span><span class="sxs-lookup"><span data-stu-id="4ef7f-103"><a name="ABS">ABS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4ef7f-104">Die Funktion `ABS` gibt den absoluten Wert (Modulus) der angegebenen Zahl mit dem Wert *Real* zurück.</span><span class="sxs-lookup"><span data-stu-id="4ef7f-104">The `ABS` function returns the absolute value (modulus) of the specified number as a *Real* value.</span></span> <span data-ttu-id="4ef7f-105">In anderen Worten gibt sie die Zahl ohne das Vorzeichen zurück.</span><span class="sxs-lookup"><span data-stu-id="4ef7f-105">In other words, it returns the number without its sign.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ef7f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ef7f-106">Syntax</span></span>

```vb
ABS (number)
```

## <a name="arguments"></a><span data-ttu-id="4ef7f-107">Argumente</span><span class="sxs-lookup"><span data-stu-id="4ef7f-107">Arguments</span></span>

<span data-ttu-id="4ef7f-108">`number`: *Real*</span><span class="sxs-lookup"><span data-stu-id="4ef7f-108">`number`: *Real*</span></span>

<span data-ttu-id="4ef7f-109">Ein numerischer Wert, dessen Modul Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="4ef7f-109">A numeric value that you want the modulus of.</span></span>

## <a name="return-values"></a><span data-ttu-id="4ef7f-110">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="4ef7f-110">Return values</span></span>

<span data-ttu-id="4ef7f-111">*Gleitkommazahl*</span><span class="sxs-lookup"><span data-stu-id="4ef7f-111">*Real*</span></span>

<span data-ttu-id="4ef7f-112">Der resultierende numerische Wert.</span><span class="sxs-lookup"><span data-stu-id="4ef7f-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="4ef7f-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="4ef7f-113">Example</span></span>

<span data-ttu-id="4ef7f-114">`ABS (-1)` gibt **1** zurück.</span><span class="sxs-lookup"><span data-stu-id="4ef7f-114">`ABS (-1)` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4ef7f-115">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4ef7f-115">Additional resources</span></span>

[<span data-ttu-id="4ef7f-116">Rechenoperationen</span><span class="sxs-lookup"><span data-stu-id="4ef7f-116">Mathematical functions</span></span>](er-functions-category-mathematical.md)
