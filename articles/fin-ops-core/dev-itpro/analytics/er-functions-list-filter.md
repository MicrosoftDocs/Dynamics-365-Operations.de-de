---
title: FILTER EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der FILTER-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: 2783fbfa0ba45c8d3772cf9ca16d110549d227b4
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917372"
---
# <span data-ttu-id="a9ae4-103"><a name="FILTER">FILTER EB-Funktion</a></span><span class="sxs-lookup"><span data-stu-id="a9ae4-103"><a name="FILTER">FILTER ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a9ae4-104">Die Funktion `FILTER` gibt die angegebene Liste als Wert *Datensatzliste* zurück, nachdem die Abfrage so geändert wurde, dass sie nach der angegebenen Bedingung filtert.</span><span class="sxs-lookup"><span data-stu-id="a9ae4-104">The `FILTER` function returns the specified list as a *Record list* value after the query has been changed so that it filters for the specified condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9ae4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9ae4-105">Syntax</span></span>

```
FILTER (list, condition)
```

## <a name="arguments"></a><span data-ttu-id="a9ae4-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="a9ae4-106">Arguments</span></span>

<span data-ttu-id="a9ae4-107">`list`: *Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="a9ae4-107">`list`: *Record list*</span></span>

<span data-ttu-id="a9ae4-108">Der gültige Pfad einer Datenquelle des Datentyps *Datensatzliste*.</span><span class="sxs-lookup"><span data-stu-id="a9ae4-108">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="a9ae4-109">`condition`: *Boolesch*</span><span class="sxs-lookup"><span data-stu-id="a9ae4-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="a9ae4-110">Ein gültiger Bedingungsausdruck, mit dem Datensätze der angegebenen Liste gefiltert werden.</span><span class="sxs-lookup"><span data-stu-id="a9ae4-110">A valid conditional expression that is used to filter records of the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="a9ae4-111">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="a9ae4-111">Return values</span></span>

<span data-ttu-id="a9ae4-112">*Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="a9ae4-112">*Record list*</span></span>

<span data-ttu-id="a9ae4-113">Die resultierende Liste der Datensätze.</span><span class="sxs-lookup"><span data-stu-id="a9ae4-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="a9ae4-114">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="a9ae4-114">Usage notes</span></span>

<span data-ttu-id="a9ae4-115">Diese Funktion unterscheidet sich von der Funktion [WO](er-functions-list-where.md), da die angegebene Bedingung auf jede beliebige Datenquelle der elektronischen Berichtserstellung (EB) des Typs *Tabellendatensätze* auf Datenbankebene angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="a9ae4-115">This function differs from the [WHERE](er-functions-list-where.md) function, because the specified condition is applied to any Electronic reporting (ER) data source of the *Table records* type at the database level.</span></span> <span data-ttu-id="a9ae4-116">Die Liste und die Bedingung können definiert werden, indem Tabellen und Relationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a9ae4-116">The list and condition can be defined by using tables and relations.</span></span>

<span data-ttu-id="a9ae4-117">Wenn eines oder beide Argumente, die für diese Funktion konfiguriert sind (`list` und `condition`), nicht die Übersetzung dieser Anforderung für den direkten SQL-Aufruf zulassen, wird zur Entwurfszeit eine Ausnahme ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="a9ae4-117">If one or both arguments that are configured for this function (`list` and `condition`) don't allow this request to be translated to the direct SQL call, an exception is thrown at design time.</span></span> <span data-ttu-id="a9ae4-118">Diese Ausnahme informiert den Benutzer darüber, dass entweder `list` oder `condition` nicht zum Abfragen der Datenbank verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a9ae4-118">This exception informs the user that either `list` or `condition` can't be used to query the database.</span></span>

## <a name="example-1"></a><span data-ttu-id="a9ae4-119">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a9ae4-119">Example 1</span></span>

<span data-ttu-id="a9ae4-120">Wenn **Kreditor** als EB-Datenquelle konfiguriert wurde, die sich auf die Tabelle „VendTable“ bezieht, gibt der Ausdruck `FILTER (Vendors, Vendors.VendGroup = "40")` eine Liste von ausschließlich den Kreditoren zurück, die zur Kreditorengruppe 40 gehören.</span><span class="sxs-lookup"><span data-stu-id="a9ae4-120">If **Vendor** is configured as an ER data source that refers to the VendTable table, the expression `FILTER (Vendors, Vendors.VendGroup = "40")` returns a list of only vendors that belong to vendor group 40.</span></span>

## <a name="example-2"></a><span data-ttu-id="a9ae4-121">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a9ae4-121">Example 2</span></span>

<span data-ttu-id="a9ae4-122">Wenn **Kreditor** als EB-Datenquelle konfiguriert ist, die auf die Tabelle „VendTable“ verweist, und wenn **parmVendorBankGroup** als EB-Datenquelle konfiguriert ist, die einen Wert des Datentyps *String* zurückgibt, gibt der Ausdruck `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` eine Liste nur der Kreditorenkonten zurück, die zu einer bestimmten Bankengruppe gehören.</span><span class="sxs-lookup"><span data-stu-id="a9ae4-122">If **Vendor** is configured as an ER data source that refers to the VendTable table, and if **parmVendorBankGroup** is configured as an ER data source that returns a value of the *String* data type, the expression `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` returns a list of only vendor accounts that belong to a specific bank group.</span></span>

## <a name="example-3"></a><span data-ttu-id="a9ae4-123">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="a9ae4-123">Example 3</span></span>

<span data-ttu-id="a9ae4-124">Sie geben die Datenquelle **DS** des Typs *Berechnetes Feld* ein, und sie enthält den Ausdruck `SPLIT ("A,B,C", ",")`.</span><span class="sxs-lookup"><span data-stu-id="a9ae4-124">You enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A,B,C", ",")`.</span></span> <span data-ttu-id="a9ae4-125">Sie geben dann einen anderen Ausdruck ein, `FILTER( DS, DS.Value = "B")`.</span><span class="sxs-lookup"><span data-stu-id="a9ae4-125">You then enter another expression, `FILTER( DS, DS.Value = "B")`.</span></span> <span data-ttu-id="a9ae4-126">Wenn Sie versuchen, diesen Ausdruck im EB-Formel-Designer zu speichern, wird die folgende Ausnahme ausgelöst: „Validierungsfehler: Der Listenausdruck der FILTER-Funktion kann nicht abgefragt werden.“</span><span class="sxs-lookup"><span data-stu-id="a9ae4-126">When you try to save this expression in the ER formula designer, the following exception is thrown: "Validation error: The list expression of FILTER function is not queryable."</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a9ae4-127">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a9ae4-127">Additional resources</span></span>

[<span data-ttu-id="a9ae4-128">Listenfunktionen</span><span class="sxs-lookup"><span data-stu-id="a9ae4-128">List functions</span></span>](er-functions-category-list.md)