---
title: ORDERBY EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der ORDERBY-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: a6aed53dcad6d402fc2ca61ae0687016cdb3af5b
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916199"
---
# <span data-ttu-id="9cf56-103"><a name="ORDERBY">ORDERBY EB-Funktion</a></span><span class="sxs-lookup"><span data-stu-id="9cf56-103"><a name="ORDERBY">ORDERBY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9cf56-104">Die Funktion `ORDERBY` gibt die angegebene Liste mit dem Wert *Datensatzliste* zurück, nachdem sie nach den angegebenen Argumenten sortiert wurde.</span><span class="sxs-lookup"><span data-stu-id="9cf56-104">The `ORDERBY` function returns the specified list as a *Record list* value after it has been sorted according to the specified arguments.</span></span> <span data-ttu-id="9cf56-105">Diese Argumente können als Ausdrücke definiert werden.</span><span class="sxs-lookup"><span data-stu-id="9cf56-105">These arguments can be defined as expressions.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cf56-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9cf56-106">Syntax</span></span>

```
ORDERBY (list , expression 1[, expression 2, …, expression N])
```

## <a name="arguments"></a><span data-ttu-id="9cf56-107">Argumente</span><span class="sxs-lookup"><span data-stu-id="9cf56-107">Arguments</span></span>

<span data-ttu-id="9cf56-108">`list`: *Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="9cf56-108">`list`: *Record list*</span></span>

<span data-ttu-id="9cf56-109">Der gültige Pfad einer Datenquelle des Datentyps *Datensatzliste*.</span><span class="sxs-lookup"><span data-stu-id="9cf56-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="9cf56-110">`expression 1`: *Feld*</span><span class="sxs-lookup"><span data-stu-id="9cf56-110">`expression 1`: *Field*</span></span>

<span data-ttu-id="9cf56-111">Der gültige Pfad eines Feldes der Datenquelle, die durch das Argument `list` der aufgerufenen Funktion referenziert wird.</span><span class="sxs-lookup"><span data-stu-id="9cf56-111">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="9cf56-112">Das referenzierte Feld muss ein Feld des primitiven Datentyps sein.</span><span class="sxs-lookup"><span data-stu-id="9cf56-112">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="9cf56-113">Dieses Argument ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9cf56-113">This argument is required.</span></span>

<span data-ttu-id="9cf56-114">`expression N`: *Feld*</span><span class="sxs-lookup"><span data-stu-id="9cf56-114">`expression N`: *Field*</span></span>

<span data-ttu-id="9cf56-115">Der gültige Pfad eines Feldes der Datenquelle, die durch das Argument `list` der aufgerufenen Funktion referenziert wird.</span><span class="sxs-lookup"><span data-stu-id="9cf56-115">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="9cf56-116">Das referenzierte Feld muss ein Feld des primitiven Datentyps sein.</span><span class="sxs-lookup"><span data-stu-id="9cf56-116">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="9cf56-117">Diese zusätzlichen Argumente sind optional.</span><span class="sxs-lookup"><span data-stu-id="9cf56-117">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="9cf56-118">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="9cf56-118">Return values</span></span>

<span data-ttu-id="9cf56-119">*Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="9cf56-119">*Record list*</span></span>

<span data-ttu-id="9cf56-120">Die resultierende Liste der Datensätze.</span><span class="sxs-lookup"><span data-stu-id="9cf56-120">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="9cf56-121">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9cf56-121">Example 1</span></span>

<span data-ttu-id="9cf56-122">Wenn Sie die Datenquelle **DS** des Typs *Berechnetes Feld* eingeben, und sie den Ausdruck `SPLIT ("C|B|A", "|")` enthält, gibt der Ausdruck `FIRST( ORDERBY( DS, DS. Value)).Value` den Textwert **"A"** zurück.</span><span class="sxs-lookup"><span data-stu-id="9cf56-122">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( ORDERBY( DS, DS. Value)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="9cf56-123">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="9cf56-123">Example 2</span></span>

<span data-ttu-id="9cf56-124">Wenn **Kreditor** als Datenquelle der elektronischen Berichterstellung (EB) konfiguriert ist, die sich auf die Tabelle „VendTable” bezieht, gibt der Ausdruck `ORDERBY (Vendors, Vendors.'name()')` eine Liste von Kreditoren zurück, die nach Namen in aufsteigender Reihenfolge sortiert ist.</span><span class="sxs-lookup"><span data-stu-id="9cf56-124">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `ORDERBY (Vendors, Vendors.'name()')` returns a list of vendors that is sorted by name in ascending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9cf56-125">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9cf56-125">Additional resources</span></span>

[<span data-ttu-id="9cf56-126">Listenfunktionen</span><span class="sxs-lookup"><span data-stu-id="9cf56-126">List functions</span></span>](er-functions-category-list.md)
