---
title: NOT EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der NOT-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: a518f255a4488c5ed6e007b1787e678fd88aff36
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041721"
---
# <span data-ttu-id="56fe6-103"><a name="NOT">NOT EB-Funktion</a></span><span class="sxs-lookup"><span data-stu-id="56fe6-103"><a name="NOT">NOT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="56fe6-104">Die Funktion `NOT` gibt den umgekehrten logischen Wert der angegebenen Bedingung als *booleschen* Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="56fe6-104">The `NOT` function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="56fe6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="56fe6-105">Syntax</span></span>

```vb
NOT (condition)
```

## <a name="arguments"></a><span data-ttu-id="56fe6-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="56fe6-106">Arguments</span></span>

<span data-ttu-id="56fe6-107">`condition`: *Boolesch*</span><span class="sxs-lookup"><span data-stu-id="56fe6-107">`condition`: *Boolean*</span></span>

<span data-ttu-id="56fe6-108">Ein gültiger Bedingungsausdruck, der aufgehoben werden muss.</span><span class="sxs-lookup"><span data-stu-id="56fe6-108">A valid conditional expression that must be reversed.</span></span>

## <a name="return-values"></a><span data-ttu-id="56fe6-109">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="56fe6-109">Return values</span></span>

<span data-ttu-id="56fe6-110">*Aktiv*</span><span class="sxs-lookup"><span data-stu-id="56fe6-110">*Boolean*</span></span>

<span data-ttu-id="56fe6-111">Der resultierende *boolesche* Wert.</span><span class="sxs-lookup"><span data-stu-id="56fe6-111">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="56fe6-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="56fe6-112">Example</span></span>

<span data-ttu-id="56fe6-113">`NOT (TRUE)` gibt **FALSE** zurück.</span><span class="sxs-lookup"><span data-stu-id="56fe6-113">`NOT (TRUE)` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="56fe6-114">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="56fe6-114">Additional resources</span></span>

[<span data-ttu-id="56fe6-115">Logische Funktionen</span><span class="sxs-lookup"><span data-stu-id="56fe6-115">Logical functions</span></span>](er-functions-category-logical.md)
