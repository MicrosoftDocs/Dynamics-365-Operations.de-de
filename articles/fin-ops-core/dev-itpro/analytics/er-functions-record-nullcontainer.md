---
title: NULLCONTAINER EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der NULLCONTAINER-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d08a4a12d2b142744d3f35c6f1088ec25158c97c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563221"
---
# <a name="nullcontainer-er-function"></a><span data-ttu-id="6e130-103">NULLCONTAINER EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="6e130-103">NULLCONTAINER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6e130-104">Die Funktion `NULLCONTAINER` gibt für *Container (Datensatz)* den Wert null zurück, der dieselbe Struktur wie die angegebene Datensatzliste oder der angegebene Datensatz besitzt.</span><span class="sxs-lookup"><span data-stu-id="6e130-104">The `NULLCONTAINER` function returns a null *Container (record)* value that has the same structure as the specified record list or record.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e130-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e130-105">Syntax</span></span>

```vb
NULLCONTAINER (list)
```

## <a name="arguments"></a><span data-ttu-id="6e130-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="6e130-106">Arguments</span></span>

<span data-ttu-id="6e130-107">`list`: *Datensatzliste* oder *Container (Datensatz)*</span><span class="sxs-lookup"><span data-stu-id="6e130-107">`list`: *Record list* or *Container (record)*</span></span>

<span data-ttu-id="6e130-108">Der gültige Pfad einer Datenquelle des Typs *Datensatzliste* oder *Container (Datensatz)*.</span><span class="sxs-lookup"><span data-stu-id="6e130-108">The valid path of a data source of either the *Record list* or *Container (record)* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="6e130-109">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="6e130-109">Return values</span></span>

<span data-ttu-id="6e130-110">*Container (Datensatz)*</span><span class="sxs-lookup"><span data-stu-id="6e130-110">*Container (record)*</span></span>

<span data-ttu-id="6e130-111">Der resultierende Datensatzwert.</span><span class="sxs-lookup"><span data-stu-id="6e130-111">The resulting record value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="6e130-112">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="6e130-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="6e130-113">Diese Funktion ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="6e130-113">This function is obsolete.</span></span> <span data-ttu-id="6e130-114">Verwenden Sie stattdessen die Funktion `EMPTYRECORD`.</span><span class="sxs-lookup"><span data-stu-id="6e130-114">Use the `EMPTYRECORD` function instead.</span></span> <span data-ttu-id="6e130-115">Weitere Informationen finden Sie in [EMPTYRECORD](er-functions-record-emptyrecord.md).</span><span class="sxs-lookup"><span data-stu-id="6e130-115">For more information, see [EMPTYRECORD](er-functions-record-emptyrecord.md).</span></span>

## <a name="example"></a><span data-ttu-id="6e130-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6e130-116">Example</span></span>

<span data-ttu-id="6e130-117">`NULLCONTAINER (SPLIT ("abc", 1))` gibt einen neuen leeren Datensatz zurück, der dieselbe Struktur wie die Liste hat, die durch die Funktion `SPLIT` zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6e130-117">`NULLCONTAINER (SPLIT ("abc", 1))` returns a new empty record that has the same structure as the list that is returned by the `SPLIT` function.</span></span> <span data-ttu-id="6e130-118">Weitere Informationen finden Sie unter [SPLIT](er-functions-list-split.md).</span><span class="sxs-lookup"><span data-stu-id="6e130-118">For more information, see [SPLIT](er-functions-list-split.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6e130-119">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6e130-119">Additional resources</span></span>

[<span data-ttu-id="6e130-120">Datensatzfunktionen</span><span class="sxs-lookup"><span data-stu-id="6e130-120">Record functions</span></span>](er-functions-category-record.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]