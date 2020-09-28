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
ms.openlocfilehash: af588c3714069040fa339d3121e6eb404b9be979
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744646"
---
# <a name="not-er-function"></a><span data-ttu-id="5e7dc-103">NOT EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="5e7dc-103">NOT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5e7dc-104">Die Funktion `NOT` gibt den umgekehrten logischen Wert der angegebenen Bedingung als *booleschen* Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="5e7dc-104">The `NOT` function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e7dc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e7dc-105">Syntax</span></span>

```vb
NOT (condition)
```

## <a name="arguments"></a><span data-ttu-id="5e7dc-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="5e7dc-106">Arguments</span></span>

<span data-ttu-id="5e7dc-107">`condition`: *Boolesch*</span><span class="sxs-lookup"><span data-stu-id="5e7dc-107">`condition`: *Boolean*</span></span>

<span data-ttu-id="5e7dc-108">Ein gültiger Bedingungsausdruck, der aufgehoben werden muss.</span><span class="sxs-lookup"><span data-stu-id="5e7dc-108">A valid conditional expression that must be reversed.</span></span>

## <a name="return-values"></a><span data-ttu-id="5e7dc-109">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="5e7dc-109">Return values</span></span>

<span data-ttu-id="5e7dc-110">*Aktiv*</span><span class="sxs-lookup"><span data-stu-id="5e7dc-110">*Boolean*</span></span>

<span data-ttu-id="5e7dc-111">Der resultierende *boolesche* Wert.</span><span class="sxs-lookup"><span data-stu-id="5e7dc-111">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="5e7dc-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5e7dc-112">Example</span></span>

<span data-ttu-id="5e7dc-113">`NOT (TRUE)` gibt **FALSE** zurück.</span><span class="sxs-lookup"><span data-stu-id="5e7dc-113">`NOT (TRUE)` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5e7dc-114">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5e7dc-114">Additional resources</span></span>

[<span data-ttu-id="5e7dc-115">Logische Funktionen</span><span class="sxs-lookup"><span data-stu-id="5e7dc-115">Logical functions</span></span>](er-functions-category-logical.md)
