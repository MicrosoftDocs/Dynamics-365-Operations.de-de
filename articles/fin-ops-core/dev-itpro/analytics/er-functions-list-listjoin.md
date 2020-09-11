---
title: LISTJOIN EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der LISTJOIN-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c7f78b687865e63e658c1c1c4f148b50595bf063
ms.sourcegitcommit: 54bdcf8e9b6d1b1aae2a244f7a82754879d12053
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2020
ms.locfileid: "3740662"
---
# <a name=""></a><span data-ttu-id="4f5c0-103"><a name="LISTJOIN">LISTJOIN EB-Funktion</a></span><span class="sxs-lookup"><span data-stu-id="4f5c0-103"><a name="LISTJOIN">LISTJOIN ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4f5c0-104">Die `LISTJOIN` Funktion gibt den Wert *Datensatzliste* zurück, der eine neue Liste von Datensätzen darstellt, die anhand der angegebenen Argumente erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="4f5c0-104">The `LISTJOIN` function returns a *Record list* value that represents a new joined list of records that is created from the specified arguments.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f5c0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f5c0-105">Syntax</span></span>

```vb
LIST (list 1 [, list 2, …, list N])
```

## <a name="arguments"></a><span data-ttu-id="4f5c0-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="4f5c0-106">Arguments</span></span>

<span data-ttu-id="4f5c0-107">`list 1`: *Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="4f5c0-107">`list 1`: *Record list*</span></span>

<span data-ttu-id="4f5c0-108">Ein Verweis auf eine Datenquelle des Datensatztyps *Datensatzliste*.</span><span class="sxs-lookup"><span data-stu-id="4f5c0-108">A reference to a data source of the *Record list* data type.</span></span> <span data-ttu-id="4f5c0-109">Dieses Argument ist obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="4f5c0-109">This argument is mandatory.</span></span>

<span data-ttu-id="4f5c0-110">`list N`: *Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="4f5c0-110">`list N`: *Record list*</span></span>

<span data-ttu-id="4f5c0-111">Ein Verweis auf eine Datenquelle des Datensatztyps *Datensatzliste*.</span><span class="sxs-lookup"><span data-stu-id="4f5c0-111">A reference to a data source of the *Record list* data type.</span></span> <span data-ttu-id="4f5c0-112">Diese zusätzlichen Argumente sind optional.</span><span class="sxs-lookup"><span data-stu-id="4f5c0-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="4f5c0-113">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="4f5c0-113">Return values</span></span>

<span data-ttu-id="4f5c0-114">*Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="4f5c0-114">*Record list*</span></span>

<span data-ttu-id="4f5c0-115">Die resultierende Liste der Datensätze.</span><span class="sxs-lookup"><span data-stu-id="4f5c0-115">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="4f5c0-116">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="4f5c0-116">Usage notes</span></span>

<span data-ttu-id="4f5c0-117">Die Struktur der Liste, die erstellt wird, zeigt nur die Felder, die in der Struktur jedes Datensatzes dargestellt werden, der in den Argumenten erwähnt wird.</span><span class="sxs-lookup"><span data-stu-id="4f5c0-117">The structure of the list that is created contains only the fields that are present in the structure of every record list that is referenced in the arguments.</span></span>

## <a name="example"></a><span data-ttu-id="4f5c0-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="4f5c0-118">Example</span></span>

<span data-ttu-id="4f5c0-119">Sie geben die Datenquelle **Record 1** des Typs `Container` ein.</span><span class="sxs-lookup"><span data-stu-id="4f5c0-119">You enter data source **Record 1** of the `Container` type.</span></span> <span data-ttu-id="4f5c0-120">Diese Datenquelle enthält die folgenden verschachtelten Felder des Typs `Calculated field` Feld:</span><span class="sxs-lookup"><span data-stu-id="4f5c0-120">This data source contains the following nested fields of the `Calculated field` type:</span></span>

- <span data-ttu-id="4f5c0-121">**Code**: Dieses Feld enthält einen Ausdruck, der einen Wert vom Typ `String` zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="4f5c0-121">**Code**: This field contains an expression that returns a value of the `String` type.</span></span>
- <span data-ttu-id="4f5c0-122">**Betrag**: Dieses Feld enthält einen Ausdruck, der einen Wert vom Typ `Real` zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="4f5c0-122">**Amount**: This field contains an expression that returns a value of the `Real` type.</span></span>

<span data-ttu-id="4f5c0-123">Sie geben dann die Datenquelle **Record 2** des Typs `Container` ein.</span><span class="sxs-lookup"><span data-stu-id="4f5c0-123">You then enter data source **Record 2** of the `Container` type.</span></span> <span data-ttu-id="4f5c0-124">Diese Datenquelle enthält die folgenden verschachtelten Felder des Typs `Calculated field` Feld:</span><span class="sxs-lookup"><span data-stu-id="4f5c0-124">This data source contains the following nested fields of the `Calculated field` type:</span></span>

- <span data-ttu-id="4f5c0-125">**Betrag**: Dieses Feld enthält einen Ausdruck, der einen Wert vom Typ `Real` zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="4f5c0-125">**Amount**: This field contains an expression that returns a value of the `Real` type.</span></span>
- <span data-ttu-id="4f5c0-126">**IsValid**: Dieses Feld enthält einen Ausdruck, der einen Wert vom Typ `Boolean` zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="4f5c0-126">**IsValid**: This field contains an expression that returns a value of the `Boolean` type.</span></span>

![ER-Modellzuordnungsdesigner – Seite](./media/er-functions-list-listjoin-image1.gif)

<span data-ttu-id="4f5c0-128">In diesem Fall gibt der Ausdruck `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` eine neue Liste zurück, die zwei Datensätze enthält.</span><span class="sxs-lookup"><span data-stu-id="4f5c0-128">In this case, the expression `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` returns a new list that contains two records.</span></span>

![ER-Modellzuordnungsdesigner – Seite](./media/er-functions-list-listjoin-image2.gif)

<span data-ttu-id="4f5c0-130">Die Struktur dieser Liste besteht aus einem einzelnen Feld **Betrag** des Typs `Real`, da dieses Feld das einzige Feld ist, das in jedem Argument der aufgerufenen Funktion vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="4f5c0-130">The structure of this list consists of a single **Amount** field of the `Real` type, because this field is the only field that is presented in every argument of the called function.</span></span>

![ER-Modellzuordnungsdesigner – Seite](./media/er-functions-list-listjoin-image3.gif)

## <a name="additional-resources"></a><span data-ttu-id="4f5c0-132">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4f5c0-132">Additional resources</span></span>

[<span data-ttu-id="4f5c0-133">Listenfunktionen</span><span class="sxs-lookup"><span data-stu-id="4f5c0-133">List functions</span></span>](er-functions-category-list.md)

[<span data-ttu-id="4f5c0-134">Debuggen Sie Datenquellen eines ausgeführten EB-Formats, um den Datenfluss und die Transformation zu analysieren</span><span class="sxs-lookup"><span data-stu-id="4f5c0-134">Debug data sources of an executed ER format to analyze data flow and transformation</span></span>](er-debug-data-sources.md)
