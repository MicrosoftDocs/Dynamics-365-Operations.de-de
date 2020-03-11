---
title: LISTOFFIRSTITEM EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der LISTOFFIRSTITEM-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: 8cd48732280c9af0b89129a32b42285207f97fb7
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041974"
---
# <span data-ttu-id="f6202-103"><a name="LISTOFFIRSTITEM">LISTOFFIRSTITEM EB-Funktion</a></span><span class="sxs-lookup"><span data-stu-id="f6202-103"><a name="LISTOFFIRSTITEM">LISTOFFIRSTITEM ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f6202-104">Die Funktion `LISTOFFIRSTITEM` gibt den Wert *Datensatzliste* zurück, der nur aus dem ersten Datensatz der angegebenen Liste besteht.</span><span class="sxs-lookup"><span data-stu-id="f6202-104">The `LISTOFFIRSTITEM` function returns a *Record list* value that consists of only the first record of the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6202-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f6202-105">Syntax</span></span>

```vb
LISTOFFIRSTITEM (list)
```

## <a name="arguments"></a><span data-ttu-id="f6202-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="f6202-106">Arguments</span></span>

<span data-ttu-id="f6202-107">`list`: *Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="f6202-107">`list`: *Record list*</span></span>

<span data-ttu-id="f6202-108">Der gültige Pfad einer Datenquelle des Datentyps *Datensatzliste*.</span><span class="sxs-lookup"><span data-stu-id="f6202-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="f6202-109">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="f6202-109">Return values</span></span>

<span data-ttu-id="f6202-110">*Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="f6202-110">*Record list*</span></span>

<span data-ttu-id="f6202-111">Die resultierende Liste der Datensätze.</span><span class="sxs-lookup"><span data-stu-id="f6202-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="f6202-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f6202-112">Example</span></span>

<span data-ttu-id="f6202-113">Der Ausdruck `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` gibt den Textwert **"A"** zurück.</span><span class="sxs-lookup"><span data-stu-id="f6202-113">The expression `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` returns the text value **"A"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f6202-114">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f6202-114">Additional resources</span></span>

[<span data-ttu-id="f6202-115">Listenfunktionen</span><span class="sxs-lookup"><span data-stu-id="f6202-115">List functions</span></span>](er-functions-category-list.md)
