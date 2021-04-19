---
title: LISTOFFIRSTITEM EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der LISTOFFIRSTITEM-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
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
ms.openlocfilehash: 6dd6c84b43bea36bf922ae9348f95b450e882832
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750179"
---
# <a name="listoffirstitem-er-function"></a><span data-ttu-id="ebfda-103">LISTOFFIRSTITEM EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="ebfda-103">LISTOFFIRSTITEM ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ebfda-104">Die Funktion `LISTOFFIRSTITEM` gibt den Wert *Datensatzliste* zurück, der nur aus dem ersten Datensatz der angegebenen Liste besteht.</span><span class="sxs-lookup"><span data-stu-id="ebfda-104">The `LISTOFFIRSTITEM` function returns a *Record list* value that consists of only the first record of the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebfda-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ebfda-105">Syntax</span></span>

```vb
LISTOFFIRSTITEM (list)
```

## <a name="arguments"></a><span data-ttu-id="ebfda-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="ebfda-106">Arguments</span></span>

<span data-ttu-id="ebfda-107">`list`: *Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="ebfda-107">`list`: *Record list*</span></span>

<span data-ttu-id="ebfda-108">Der gültige Pfad einer Datenquelle des Datentyps *Datensatzliste*.</span><span class="sxs-lookup"><span data-stu-id="ebfda-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="ebfda-109">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="ebfda-109">Return values</span></span>

<span data-ttu-id="ebfda-110">*Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="ebfda-110">*Record list*</span></span>

<span data-ttu-id="ebfda-111">Die resultierende Liste der Datensätze.</span><span class="sxs-lookup"><span data-stu-id="ebfda-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="ebfda-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ebfda-112">Example</span></span>

<span data-ttu-id="ebfda-113">Der Ausdruck `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` gibt den Textwert **"A"** zurück.</span><span class="sxs-lookup"><span data-stu-id="ebfda-113">The expression `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` returns the text value **"A"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ebfda-114">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ebfda-114">Additional resources</span></span>

[<span data-ttu-id="ebfda-115">Listenfunktionen</span><span class="sxs-lookup"><span data-stu-id="ebfda-115">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]