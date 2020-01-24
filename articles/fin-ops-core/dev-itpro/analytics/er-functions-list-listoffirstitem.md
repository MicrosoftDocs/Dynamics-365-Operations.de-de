---
title: LISTOFFIRSTITEM EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der LISTOFFIRSTITEM-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: 4d985ef5015bc104a83260b64418821cc715e8cb
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917257"
---
# <span data-ttu-id="98a2e-103"><a name="LISTOFFIRSTITEM">LISTOFFIRSTITEM EB-Funktion</a></span><span class="sxs-lookup"><span data-stu-id="98a2e-103"><a name="LISTOFFIRSTITEM">LISTOFFIRSTITEM ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="98a2e-104">Die Funktion `LISTOFFIRSTITEM` gibt den Wert *Datensatzliste* zurück, der nur aus dem ersten Datensatz der angegebenen Liste besteht.</span><span class="sxs-lookup"><span data-stu-id="98a2e-104">The `LISTOFFIRSTITEM` function returns a *Record list* value that consists of only the first record of the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="98a2e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="98a2e-105">Syntax</span></span>

```
LISTOFFIRSTITEM (list)
```

## <a name="arguments"></a><span data-ttu-id="98a2e-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="98a2e-106">Arguments</span></span>

<span data-ttu-id="98a2e-107">`list`: *Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="98a2e-107">`list`: *Record list*</span></span>

<span data-ttu-id="98a2e-108">Der gültige Pfad einer Datenquelle des Datentyps *Datensatzliste*.</span><span class="sxs-lookup"><span data-stu-id="98a2e-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="98a2e-109">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="98a2e-109">Return values</span></span>

<span data-ttu-id="98a2e-110">*Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="98a2e-110">*Record list*</span></span>

<span data-ttu-id="98a2e-111">Die resultierende Liste der Datensätze.</span><span class="sxs-lookup"><span data-stu-id="98a2e-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="98a2e-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="98a2e-112">Example</span></span>

<span data-ttu-id="98a2e-113">Der Ausdruck `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` gibt den Textwert **"A"** zurück.</span><span class="sxs-lookup"><span data-stu-id="98a2e-113">The expression `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` returns the text value **"A"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="98a2e-114">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="98a2e-114">Additional resources</span></span>

[<span data-ttu-id="98a2e-115">Listenfunktionen</span><span class="sxs-lookup"><span data-stu-id="98a2e-115">List functions</span></span>](er-functions-category-list.md)
