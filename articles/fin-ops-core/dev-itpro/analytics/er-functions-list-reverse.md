---
title: REVERSE EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der REVERSE-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: 3343ad788cef29a79f9b110bf29809cd5f0e5c63
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917234"
---
# <span data-ttu-id="198e5-103"><a name="REVERSE">REVERSE EB-Funktion</a></span><span class="sxs-lookup"><span data-stu-id="198e5-103"><a name="REVERSE">REVERSE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="198e5-104">Die Funktion `REVERSE` gibt die angegebene Liste mit dem Wert *Datensatzliste* in umgekehrter Sortierreihenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="198e5-104">The `REVERSE` function returns the specified list as a *Record list* value in reversed sort order.</span></span>

## <a name="syntax"></a><span data-ttu-id="198e5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="198e5-105">Syntax</span></span>

```
REVERSE (list)
```

## <a name="arguments"></a><span data-ttu-id="198e5-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="198e5-106">Arguments</span></span>

<span data-ttu-id="198e5-107">`list`: *Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="198e5-107">`list`: *Record list*</span></span>

<span data-ttu-id="198e5-108">Der gültige Pfad einer Datenquelle des Datentyps *Datensatzliste*.</span><span class="sxs-lookup"><span data-stu-id="198e5-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="198e5-109">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="198e5-109">Return values</span></span>

<span data-ttu-id="198e5-110">*Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="198e5-110">*Record list*</span></span>

<span data-ttu-id="198e5-111">Die resultierende Liste der Datensätze.</span><span class="sxs-lookup"><span data-stu-id="198e5-111">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="198e5-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="198e5-112">Example 1</span></span>

<span data-ttu-id="198e5-113">Wenn Sie die Datenquelle **DS** des Typs *Berechnetes Feld* eingeben, und sie den Ausdruck `SPLIT ("C|B|A", "|")` enthält, gibt der Ausdruck `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` den Textwert **"C"** zurück.</span><span class="sxs-lookup"><span data-stu-id="198e5-113">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` returns the text value **"C"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="198e5-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="198e5-114">Example 2</span></span>

<span data-ttu-id="198e5-115">Wenn **Kreditor** als Datenquelle der elektronischen Berichtserstellung (EB) konfiguriert ist, die sich auf die Tabelle „VendTable“ bezieht, gibt der Ausdruck `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` eine Liste von Kreditoren zurück, die nach Namen in absteigender Reihenfolge sortiert ist.</span><span class="sxs-lookup"><span data-stu-id="198e5-115">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` returns a list of vendors that is sorted by name in descending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="198e5-116">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="198e5-116">Additional resources</span></span>

[<span data-ttu-id="198e5-117">Listenfunktionen</span><span class="sxs-lookup"><span data-stu-id="198e5-117">List functions</span></span>](er-functions-category-list.md)