---
title: NULLCONTAINER EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der NULLCONTAINER-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: ea71bfc4b30164fd32e804bf83a46c49cd18d155
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041468"
---
# <span data-ttu-id="7753f-103"><a name="NULLCONTAINER">NULLCONTAINER EB-Funktion</a></span><span class="sxs-lookup"><span data-stu-id="7753f-103"><a name="NULLCONTAINER">NULLCONTAINER ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7753f-104">Die Funktion `NULLCONTAINER` gibt für *Container (Datensatz)* den Wert null zurück, der dieselbe Struktur wie die angegebene Datensatzliste oder der angegebene Datensatz besitzt.</span><span class="sxs-lookup"><span data-stu-id="7753f-104">The `NULLCONTAINER` function returns a null *Container (record)* value that has the same structure as the specified record list or record.</span></span>

## <a name="syntax"></a><span data-ttu-id="7753f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7753f-105">Syntax</span></span>

```vb
NULLCONTAINER (list)
```

## <a name="arguments"></a><span data-ttu-id="7753f-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="7753f-106">Arguments</span></span>

<span data-ttu-id="7753f-107">`list`: *Datensatzliste* oder *Container (Datensatz)*</span><span class="sxs-lookup"><span data-stu-id="7753f-107">`list`: *Record list* or *Container (record)*</span></span>

<span data-ttu-id="7753f-108">Der gültige Pfad einer Datenquelle des Typs *Datensatzliste* oder *Container (Datensatz)*.</span><span class="sxs-lookup"><span data-stu-id="7753f-108">The valid path of a data source of either the *Record list* or *Container (record)* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="7753f-109">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="7753f-109">Return values</span></span>

<span data-ttu-id="7753f-110">*Container (Datensatz)*</span><span class="sxs-lookup"><span data-stu-id="7753f-110">*Container (record)*</span></span>

<span data-ttu-id="7753f-111">Der resultierende Datensatzwert.</span><span class="sxs-lookup"><span data-stu-id="7753f-111">The resulting record value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="7753f-112">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="7753f-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="7753f-113">Diese Funktion ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="7753f-113">This function is obsolete.</span></span> <span data-ttu-id="7753f-114">Verwenden Sie stattdessen die Funktion `EMPTYRECORD`.</span><span class="sxs-lookup"><span data-stu-id="7753f-114">Use the `EMPTYRECORD` function instead.</span></span> <span data-ttu-id="7753f-115">Weitere Informationen finden Sie in [EMPTYRECORD](er-functions-record-emptyrecord.md).</span><span class="sxs-lookup"><span data-stu-id="7753f-115">For more information, see [EMPTYRECORD](er-functions-record-emptyrecord.md).</span></span>

## <a name="example"></a><span data-ttu-id="7753f-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7753f-116">Example</span></span>

<span data-ttu-id="7753f-117">`NULLCONTAINER (SPLIT ("abc", 1))` gibt einen neuen leeren Datensatz zurück, der dieselbe Struktur wie die Liste hat, die durch die Funktion `SPLIT` zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7753f-117">`NULLCONTAINER (SPLIT ("abc", 1))` returns a new empty record that has the same structure as the list that is returned by the `SPLIT` function.</span></span> <span data-ttu-id="7753f-118">Weitere Informationen finden Sie unter [SPLIT](er-functions-list-split.md).</span><span class="sxs-lookup"><span data-stu-id="7753f-118">For more information, see [SPLIT](er-functions-list-split.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7753f-119">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7753f-119">Additional resources</span></span>

[<span data-ttu-id="7753f-120">Datensatzfunktionen</span><span class="sxs-lookup"><span data-stu-id="7753f-120">Record functions</span></span>](er-functions-category-record.md)
