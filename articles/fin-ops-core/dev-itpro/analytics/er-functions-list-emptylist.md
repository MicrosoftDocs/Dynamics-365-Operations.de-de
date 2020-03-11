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
ms.openlocfilehash: 5fb991eb9ee08aeb418313eb782dbde7fa22b763
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042181"
---
# <span data-ttu-id="df605-103"><a name="EMPTYLIST">EMPTYLIST EB-Funktion</a></span><span class="sxs-lookup"><span data-stu-id="df605-103"><a name="EMPTYLIST">EMPTYLIST ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="df605-104">Die Funktion `EMPTYLIST` gibt den Wert *Datensatzliste* zurück, indem eine angegebene Liste als Quelle für die Listenstruktur verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="df605-104">The `EMPTYLIST` function returns an empty *Record list* value by using the specified list as a source for the list structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="df605-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="df605-105">Syntax</span></span>

```vb
EMPTYLIST (list)
```

## <a name="arguments"></a><span data-ttu-id="df605-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="df605-106">Arguments</span></span>

<span data-ttu-id="df605-107">`list`: *Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="df605-107">`list`: *Record list*</span></span>

<span data-ttu-id="df605-108">Der gültige Pfad einer Datenquelle des Datentyps *Datensatzliste*.</span><span class="sxs-lookup"><span data-stu-id="df605-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="df605-109">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="df605-109">Return values</span></span>

<span data-ttu-id="df605-110">*Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="df605-110">*Record list*</span></span>

<span data-ttu-id="df605-111">Die resultierende Liste der Datensätze.</span><span class="sxs-lookup"><span data-stu-id="df605-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="df605-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="df605-112">Example</span></span>

<span data-ttu-id="df605-113">`EMPTYLIST (SPLIT ("abc", 1))` gibt eine neue leere Liste zurück, die dieselbe Struktur wie die Liste hat, die durch die verwendete Funktion `SPLIT` zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="df605-113">`EMPTYLIST (SPLIT ("abc", 1))` returns a new empty list that has the same structure as the list that is returned by the `SPLIT` function that is used.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="df605-114">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="df605-114">Additional resources</span></span>

[<span data-ttu-id="df605-115">Listenfunktionen</span><span class="sxs-lookup"><span data-stu-id="df605-115">List functions</span></span>](er-functions-category-list.md)
