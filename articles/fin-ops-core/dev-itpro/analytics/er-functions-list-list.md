---
title: LIST EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung von LIST bei der elektronischen Berichterstellungsfunktion (EB) bereitgestellt.
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
ms.openlocfilehash: a31288885abda69873ae23b28a36e2a54852f593
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745152"
---
# <a name="list-er-function"></a><span data-ttu-id="1cd46-103">LIST EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="1cd46-103">LIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1cd46-104">Die Funktion `LIST` gibt den Wert *Datensatzliste* zurück, der aus einer neuen Liste an Datensätzen besteht, die anhand der angegebenen Argumente erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="1cd46-104">The `LIST` function returns a *Record list* value that consists of a new list of records that is created from the specified arguments.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cd46-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1cd46-105">Syntax</span></span>

```vb
LIST (record 1 [, record 2, …, record N])
```

## <a name="arguments"></a><span data-ttu-id="1cd46-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="1cd46-106">Arguments</span></span>

<span data-ttu-id="1cd46-107">`record 1`: *Container (Datensatz)*</span><span class="sxs-lookup"><span data-stu-id="1cd46-107">`record 1`: *Container (record)*</span></span>

<span data-ttu-id="1cd46-108">Ein Verweis auf eine Datenquelle des Datensatztyps *Datensatz*.</span><span class="sxs-lookup"><span data-stu-id="1cd46-108">A reference to a data source of the *Record* data type.</span></span> <span data-ttu-id="1cd46-109">Dieses Argument ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1cd46-109">This argument is required.</span></span>

<span data-ttu-id="1cd46-110">`record N`: *Container (Datensatz)*</span><span class="sxs-lookup"><span data-stu-id="1cd46-110">`record N`: *Container (record)*</span></span>

<span data-ttu-id="1cd46-111">Ein Verweis auf eine Datenquelle des Datensatztyps *Datensatz*.</span><span class="sxs-lookup"><span data-stu-id="1cd46-111">A reference to a data source of the *Record* data type.</span></span> <span data-ttu-id="1cd46-112">Diese zusätzlichen Argumente sind optional.</span><span class="sxs-lookup"><span data-stu-id="1cd46-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="1cd46-113">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="1cd46-113">Return values</span></span>

<span data-ttu-id="1cd46-114">*Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="1cd46-114">*Record list*</span></span>

<span data-ttu-id="1cd46-115">Die resultierende Liste der Datensätze.</span><span class="sxs-lookup"><span data-stu-id="1cd46-115">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="1cd46-116">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="1cd46-116">Usage notes</span></span>

<span data-ttu-id="1cd46-117">Die Struktur der Liste, die erstellt wird, enthält nur die Felder, die in der Struktur jedes Datensatzes dargestellt werden, der in den Argumenten erwähnt wird.</span><span class="sxs-lookup"><span data-stu-id="1cd46-117">The structure of the list that is created contains only the fields that are presented in the structure of every record that is mentioned in the arguments.</span></span>

## <a name="example"></a><span data-ttu-id="1cd46-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="1cd46-118">Example</span></span>

<span data-ttu-id="1cd46-119">Sie geben die Datenquelle **Record 1** des Typs *Container* ein.</span><span class="sxs-lookup"><span data-stu-id="1cd46-119">You enter data source **Record 1** of the *Container* type.</span></span> <span data-ttu-id="1cd46-120">Diese Datenquelle enthält die folgenden verschachtelten Felder des Typs *Berechnetes Feld*:</span><span class="sxs-lookup"><span data-stu-id="1cd46-120">This data source contains the following nested fields of the *Calculated field* type:</span></span>

- <span data-ttu-id="1cd46-121">**Code:** Dieses Feld enthält einen Ausdruck, der einen Wert vom Typ *String* zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="1cd46-121">**Code:** This field contains an expression that returns a value of the *String* type.</span></span>
- <span data-ttu-id="1cd46-122">**Betrag:** Dieses Feld enthält einen Ausdruck, der einen Wert vom Typ *Real* zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="1cd46-122">**Amount:** This field contains an expression that returns a value of the *Real* type.</span></span>

<span data-ttu-id="1cd46-123">Sie geben dann die Datenquelle **Record 2** des Typs *Container* ein.</span><span class="sxs-lookup"><span data-stu-id="1cd46-123">You then enter data source **Record 2** of the *Container* type.</span></span> <span data-ttu-id="1cd46-124">Diese Datenquelle enthält die folgenden verschachtelten Felder des Typs *Berechnetes Feld*:</span><span class="sxs-lookup"><span data-stu-id="1cd46-124">This data source contains the following nested fields of the *Calculated field* type:</span></span>

- <span data-ttu-id="1cd46-125">**Betrag:** Dieses Feld enthält einen Ausdruck, der einen Wert vom Typ *Real* zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="1cd46-125">**Amount:** This field contains an expression that returns a value of the *Real* type.</span></span>
- <span data-ttu-id="1cd46-126">**IsValid:** Dieses Feld enthält einen Ausdruck, der einen Wert vom Typ *Boolesch* zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="1cd46-126">**IsValid:** This field contains an expression that returns a value of the *Boolean* type.</span></span>

<span data-ttu-id="1cd46-127">In diesem Fall gibt der Ausdruck `LIST('Record 1', 'Record 2')` eine neue Liste zurück, die zwei Datensätze enthält.</span><span class="sxs-lookup"><span data-stu-id="1cd46-127">In this case, the expression `LIST('Record 1', 'Record 2')` returns a new list that contains two records.</span></span> <span data-ttu-id="1cd46-128">Die Struktur dieser Liste besteht aus einem einzelnen Feld **Betrag** des Typs *Real*, da dieses Feld das einzige Feld ist, das in jedem Argument der aufgerufenen Funktion vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="1cd46-128">The structure of this list consists of a single **Amount** field of the *Real* type, because this field is the only field that is presented in every argument of the called function.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1cd46-129">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1cd46-129">Additional resources</span></span>

[<span data-ttu-id="1cd46-130">Listenfunktionen</span><span class="sxs-lookup"><span data-stu-id="1cd46-130">List functions</span></span>](er-functions-category-list.md)
