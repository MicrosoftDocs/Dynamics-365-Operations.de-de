---
title: WHERE EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der WHERE-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: 50d90697f522f3c4d7b62190928008b6d923ffc6
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916084"
---
# <span data-ttu-id="58919-103"><a name="WHERE">WHERE EB-Funktion</a></span><span class="sxs-lookup"><span data-stu-id="58919-103"><a name="WHERE">WHERE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="58919-104">Die Funktion `WHERE` gibt die angegebene Liste mit dem Wert *Datensatzliste* zurück, nachdem sie gemäß der angegebenen Bedingung gefiltert wurde.</span><span class="sxs-lookup"><span data-stu-id="58919-104">The `WHERE` function returns the specified list as a *Record list* value after it has been filtered according to the specified condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="58919-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="58919-105">Syntax</span></span>

```
WHERE (list, condition)
```

## <a name="arguments"></a><span data-ttu-id="58919-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="58919-106">Arguments</span></span>

<span data-ttu-id="58919-107">`list`: *Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="58919-107">`list`: *Record list*</span></span>

<span data-ttu-id="58919-108">Der gültige Pfad einer Datenquelle des Datentyps *Datensatzliste*.</span><span class="sxs-lookup"><span data-stu-id="58919-108">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="58919-109">`condition`: *Boolesch*</span><span class="sxs-lookup"><span data-stu-id="58919-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="58919-110">Ein gültiger Bedingungsausdruck, mit dem Datensätze der angegebenen Liste gefiltert werden.</span><span class="sxs-lookup"><span data-stu-id="58919-110">A valid conditional expression that is used to filter records of the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="58919-111">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="58919-111">Return values</span></span>

<span data-ttu-id="58919-112">*Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="58919-112">*Record list*</span></span>

<span data-ttu-id="58919-113">Die resultierende Liste der Datensätze.</span><span class="sxs-lookup"><span data-stu-id="58919-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="58919-114">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="58919-114">Usage notes</span></span>

<span data-ttu-id="58919-115">Diese Funktion unterscheidet sich von der Funktion [FILTER](er-functions-list-filter.md), da die angegebene Bedingung auf jede beliebige Datenquelle der elektronischen Berichterstellung (EB) des Typs *Datensatzliste* angewendet wird, die sich im Speicher befindet.</span><span class="sxs-lookup"><span data-stu-id="58919-115">This function differs from the [FILTER](er-functions-list-filter.md) function, because the specified condition is applied to any Electronic reporting (ER) data source of the *Record list* type that is present in memory.</span></span>

<span data-ttu-id="58919-116">Wenn die Argumente, die für diese Funktion konfiguriert sind (`list` und `condition`), die Übersetzung dieser Anforderung für den direkten SQL-Aufruf zulassen, wird zur Entwurfszeit eine Warnmeldung ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="58919-116">If the arguments that are configured for this function (`list` and `condition`) allow this request to be translated to the direct SQL call, a warning message is thrown at design time.</span></span> <span data-ttu-id="58919-117">Diese Nachricht informiert den Benutzer darüber, dass die Leistung verbessert werden könnte, wenn die Funktion [FILTER ](er-functions-list-filter.md) anstelle von `WHERE` verwendet werden würde.</span><span class="sxs-lookup"><span data-stu-id="58919-117">This message informs the user that performance might be improved if the [FILTER](er-functions-list-filter.md) function is used instead of `WHERE`.</span></span>

## <a name="example-1"></a><span data-ttu-id="58919-118">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="58919-118">Example 1</span></span>

<span data-ttu-id="58919-119">Wenn **Kreditor** als EB-Datenquelle konfiguriert wurde, die sich auf die Tabelle „VendTable“ bezieht, gibt der Ausdruck `WHERE (Vendors, Vendors.VendGroup = "40")` eine Liste von ausschließlich den Kreditoren zurück, die zur Kreditorengruppe 40 gehören.</span><span class="sxs-lookup"><span data-stu-id="58919-119">If **Vendor** is configured as an ER data source that refers to the VendTable table, the expression `WHERE (Vendors, Vendors.VendGroup = "40")` returns a list of only vendors that belong to vendor group 40.</span></span>

## <a name="example-2"></a><span data-ttu-id="58919-120">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="58919-120">Example 2</span></span>

<span data-ttu-id="58919-121">Wenn Sie die Datenquelle **DS** des Typs *Berechnetes Feld* eingeben und sie den Ausdruck `SPLIT ("A|B|C", "|")` enthält, gibt der Ausdruck `WHERE( DS, DS.Value = "B")` eine Liste mit nur einem Datensatz zurück, der den Text **"B"** im Feld **Wert** enthält.</span><span class="sxs-lookup"><span data-stu-id="58919-121">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `WHERE( DS, DS.Value = "B")` returns a list of only one record that contains the text **"B"** in the **Value** field.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="58919-122">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="58919-122">Additional resources</span></span>

[<span data-ttu-id="58919-123">Listenfunktionen</span><span class="sxs-lookup"><span data-stu-id="58919-123">List functions</span></span>](er-functions-category-list.md)
