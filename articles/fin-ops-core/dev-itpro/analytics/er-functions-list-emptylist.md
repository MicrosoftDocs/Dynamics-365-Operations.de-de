---
title: EMPTYLIST EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der EMPTYLIST-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: 1e2a92d9951c3ad27503cf82f1b45026f16c3835
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746674"
---
# <a name="emptylist-er-function"></a><span data-ttu-id="53dd4-103">EMPTYLIST EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="53dd4-103">EMPTYLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="53dd4-104">Die Funktion `EMPTYLIST` gibt den Wert *Datensatzliste* zurück, indem eine angegebene Liste als Quelle für die Listenstruktur verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="53dd4-104">The `EMPTYLIST` function returns an empty *Record list* value by using the specified list as a source for the list structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="53dd4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="53dd4-105">Syntax</span></span>

```vb
EMPTYLIST (list)
```

## <a name="arguments"></a><span data-ttu-id="53dd4-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="53dd4-106">Arguments</span></span>

<span data-ttu-id="53dd4-107">`list`: *Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="53dd4-107">`list`: *Record list*</span></span>

<span data-ttu-id="53dd4-108">Der gültige Pfad einer Datenquelle des Datentyps *Datensatzliste*.</span><span class="sxs-lookup"><span data-stu-id="53dd4-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="53dd4-109">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="53dd4-109">Return values</span></span>

<span data-ttu-id="53dd4-110">*Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="53dd4-110">*Record list*</span></span>

<span data-ttu-id="53dd4-111">Die resultierende Liste der Datensätze.</span><span class="sxs-lookup"><span data-stu-id="53dd4-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="53dd4-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="53dd4-112">Example</span></span>

<span data-ttu-id="53dd4-113">`EMPTYLIST (SPLIT ("abc", 1))` gibt eine neue leere Liste zurück, die dieselbe Struktur wie die Liste hat, die durch die verwendete Funktion `SPLIT` zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="53dd4-113">`EMPTYLIST (SPLIT ("abc", 1))` returns a new empty list that has the same structure as the list that is returned by the `SPLIT` function that is used.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="53dd4-114">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="53dd4-114">Additional resources</span></span>

[<span data-ttu-id="53dd4-115">Listenfunktionen</span><span class="sxs-lookup"><span data-stu-id="53dd4-115">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]