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
ms.openlocfilehash: 0a6b5cddc325625dc5b3d677ffcc1da1f8b829cd
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041951"
---
# <span data-ttu-id="ba088-103"><a name="ORDERBY">ORDERBY EB-Funktion</a></span><span class="sxs-lookup"><span data-stu-id="ba088-103"><a name="ORDERBY">ORDERBY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ba088-104">Die Funktion `ORDERBY` gibt die angegebene Liste mit dem Wert *Datensatzliste* zurück, nachdem sie nach den angegebenen Argumenten sortiert wurde.</span><span class="sxs-lookup"><span data-stu-id="ba088-104">The `ORDERBY` function returns the specified list as a *Record list* value after it has been sorted according to the specified arguments.</span></span> <span data-ttu-id="ba088-105">Diese Argumente können als Ausdrücke definiert werden.</span><span class="sxs-lookup"><span data-stu-id="ba088-105">These arguments can be defined as expressions.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba088-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba088-106">Syntax</span></span>

```vb
ORDERBY (list , expression 1[, expression 2, …, expression N])
```

## <a name="arguments"></a><span data-ttu-id="ba088-107">Argumente</span><span class="sxs-lookup"><span data-stu-id="ba088-107">Arguments</span></span>

<span data-ttu-id="ba088-108">`list`: *Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="ba088-108">`list`: *Record list*</span></span>

<span data-ttu-id="ba088-109">Der gültige Pfad einer Datenquelle des Datentyps *Datensatzliste*.</span><span class="sxs-lookup"><span data-stu-id="ba088-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="ba088-110">`expression 1`: *Feld*</span><span class="sxs-lookup"><span data-stu-id="ba088-110">`expression 1`: *Field*</span></span>

<span data-ttu-id="ba088-111">Der gültige Pfad eines Feldes der Datenquelle, die durch das Argument `list` der aufgerufenen Funktion referenziert wird.</span><span class="sxs-lookup"><span data-stu-id="ba088-111">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="ba088-112">Das referenzierte Feld muss ein Feld des primitiven Datentyps sein.</span><span class="sxs-lookup"><span data-stu-id="ba088-112">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="ba088-113">Dieses Argument ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ba088-113">This argument is required.</span></span>

<span data-ttu-id="ba088-114">`expression N`: *Feld*</span><span class="sxs-lookup"><span data-stu-id="ba088-114">`expression N`: *Field*</span></span>

<span data-ttu-id="ba088-115">Der gültige Pfad eines Feldes der Datenquelle, die durch das Argument `list` der aufgerufenen Funktion referenziert wird.</span><span class="sxs-lookup"><span data-stu-id="ba088-115">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="ba088-116">Das referenzierte Feld muss ein Feld des primitiven Datentyps sein.</span><span class="sxs-lookup"><span data-stu-id="ba088-116">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="ba088-117">Diese zusätzlichen Argumente sind optional.</span><span class="sxs-lookup"><span data-stu-id="ba088-117">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="ba088-118">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="ba088-118">Return values</span></span>

<span data-ttu-id="ba088-119">*Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="ba088-119">*Record list*</span></span>

<span data-ttu-id="ba088-120">Die resultierende Liste der Datensätze.</span><span class="sxs-lookup"><span data-stu-id="ba088-120">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="ba088-121">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ba088-121">Example 1</span></span>

<span data-ttu-id="ba088-122">Wenn Sie die Datenquelle **DS** des Typs *Berechnetes Feld* eingeben, und sie den Ausdruck `SPLIT ("C|B|A", "|")` enthält, gibt der Ausdruck `FIRST( ORDERBY( DS, DS. Value)).Value` den Textwert **"A"** zurück.</span><span class="sxs-lookup"><span data-stu-id="ba088-122">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( ORDERBY( DS, DS. Value)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="ba088-123">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ba088-123">Example 2</span></span>

<span data-ttu-id="ba088-124">Wenn **Kreditor** als Datenquelle der elektronischen Berichterstellung (EB) konfiguriert ist, die sich auf die Tabelle „VendTable” bezieht, gibt der Ausdruck `ORDERBY (Vendors, Vendors.'name()')` eine Liste von Kreditoren zurück, die nach Namen in aufsteigender Reihenfolge sortiert ist.</span><span class="sxs-lookup"><span data-stu-id="ba088-124">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `ORDERBY (Vendors, Vendors.'name()')` returns a list of vendors that is sorted by name in ascending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ba088-125">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ba088-125">Additional resources</span></span>

[<span data-ttu-id="ba088-126">Listenfunktionen</span><span class="sxs-lookup"><span data-stu-id="ba088-126">List functions</span></span>](er-functions-category-list.md)
