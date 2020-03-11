---
title: JSONVALUE EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der JSONVALUE-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 75f20632074cb4dead98991fd6522ab9b20b9965
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041215"
---
# <span data-ttu-id="e4274-103"><a name="JSONVALUE">JSONVALUE EB-Funktion</a></span><span class="sxs-lookup"><span data-stu-id="e4274-103"><a name="JSONVALUE">JSONVALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e4274-104">Die Funktion `JSONVALUE` analysiert Daten im JavaScript Object Notation (JSON)-Format, auf die über den angegebenen Pfad zugegriffen wird, und sie extrahiert einen Skalarwert, der auf der angegebenen ID basiert.</span><span class="sxs-lookup"><span data-stu-id="e4274-104">The `JSONVALUE` function parses data in JavaScript Object Notation (JSON) format that is accessed at the specified path, and it extracts a scalar value that has the specified ID.</span></span> <span data-ttu-id="e4274-105">Anschließend wird der extrahierte Skalarwert als Wert *String* zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e4274-105">It then returns the extracted scalar value as a *String* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4274-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4274-106">Syntax</span></span>

```vb
JSONVALUE (input, path)
```

## <a name="arguments"></a><span data-ttu-id="e4274-107">Argumente</span><span class="sxs-lookup"><span data-stu-id="e4274-107">Arguments</span></span>

<span data-ttu-id="e4274-108">`input`: *String*</span><span class="sxs-lookup"><span data-stu-id="e4274-108">`input`: *String*</span></span>

<span data-ttu-id="e4274-109">Der gültige Pfad einer Datenquelle des Typs *String*, die JSON-Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="e4274-109">The valid path of a data source of the *String* type that contains JSON data.</span></span>

<span data-ttu-id="e4274-110">`path`: *String*</span><span class="sxs-lookup"><span data-stu-id="e4274-110">`path`: *String*</span></span>

<span data-ttu-id="e4274-111">Der Bezeichner eines Skalarwerts der JSON-Daten.</span><span class="sxs-lookup"><span data-stu-id="e4274-111">The identifier of a scalar value of JSON data.</span></span>

## <a name="return-values"></a><span data-ttu-id="e4274-112">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="e4274-112">Return values</span></span>

<span data-ttu-id="e4274-113">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="e4274-113">*String*</span></span>

<span data-ttu-id="e4274-114">Der resultierende Textwert.</span><span class="sxs-lookup"><span data-stu-id="e4274-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="e4274-115">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e4274-115">Example</span></span>

<span data-ttu-id="e4274-116">Die Datenquelle **JsonField** enthält die folgenden Daten im JSON-Format: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**.</span><span class="sxs-lookup"><span data-stu-id="e4274-116">The **JsonField** data source contains the following data in JSON format: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**.</span></span> <span data-ttu-id="e4274-117">In diesem Fall gibt der Ausdruck `JSONVALUE (JsonField, "BuildNumber")` den folgenden Wert des Datentyps *String* zurück: **"7.3.1234.1"**.</span><span class="sxs-lookup"><span data-stu-id="e4274-117">In this case, the expression `JSONVALUE (JsonField, "BuildNumber")` returns the following value of the *String* data type: **"7.3.1234.1"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e4274-118">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e4274-118">Additional resources</span></span>

[<span data-ttu-id="e4274-119">Textfunktionen</span><span class="sxs-lookup"><span data-stu-id="e4274-119">Text functions</span></span>](er-functions-category-text.md)
