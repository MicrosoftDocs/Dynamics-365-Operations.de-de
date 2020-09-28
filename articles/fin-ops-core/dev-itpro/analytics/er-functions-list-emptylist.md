---
title: EMPTYLIST EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der EMPTYLIST-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: 747b661d0dee4e9c27741e167c89f9ef7eefa470
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745320"
---
# <a name="emptylist-er-function"></a><span data-ttu-id="17568-103">EMPTYLIST EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="17568-103">EMPTYLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="17568-104">Die Funktion `EMPTYLIST` gibt den Wert *Datensatzliste* zurück, indem eine angegebene Liste als Quelle für die Listenstruktur verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="17568-104">The `EMPTYLIST` function returns an empty *Record list* value by using the specified list as a source for the list structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="17568-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="17568-105">Syntax</span></span>

```vb
EMPTYLIST (list)
```

## <a name="arguments"></a><span data-ttu-id="17568-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="17568-106">Arguments</span></span>

<span data-ttu-id="17568-107">`list`: *Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="17568-107">`list`: *Record list*</span></span>

<span data-ttu-id="17568-108">Der gültige Pfad einer Datenquelle des Datentyps *Datensatzliste*.</span><span class="sxs-lookup"><span data-stu-id="17568-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="17568-109">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="17568-109">Return values</span></span>

<span data-ttu-id="17568-110">*Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="17568-110">*Record list*</span></span>

<span data-ttu-id="17568-111">Die resultierende Liste der Datensätze.</span><span class="sxs-lookup"><span data-stu-id="17568-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="17568-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="17568-112">Example</span></span>

<span data-ttu-id="17568-113">`EMPTYLIST (SPLIT ("abc", 1))` gibt eine neue leere Liste zurück, die dieselbe Struktur wie die Liste hat, die durch die verwendete Funktion `SPLIT` zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="17568-113">`EMPTYLIST (SPLIT ("abc", 1))` returns a new empty list that has the same structure as the list that is returned by the `SPLIT` function that is used.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="17568-114">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="17568-114">Additional resources</span></span>

[<span data-ttu-id="17568-115">Listenfunktionen</span><span class="sxs-lookup"><span data-stu-id="17568-115">List functions</span></span>](er-functions-category-list.md)
