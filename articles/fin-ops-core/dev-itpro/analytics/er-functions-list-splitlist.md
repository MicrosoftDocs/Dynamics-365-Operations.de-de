---
title: SPLITLIST EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der SPLITLIST-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: af8c413726ca8d9f92eff18807e7fa9002fc9d37
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559137"
---
# <a name="splitlist-er-function"></a><span data-ttu-id="911da-103">SPLITLIST EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="911da-103">SPLITLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="911da-104">Die Funktion `SPLITLIST` teilt die angegebene Liste in Unterlisten (oder Batches), die jeweils die angegebene Anzahl von Datensätzen enthalten.</span><span class="sxs-lookup"><span data-stu-id="911da-104">The `SPLITLIST` function splits the specified list into sublists (or batches), each of which contains the specified number of records.</span></span> <span data-ttu-id="911da-105">Sie gibt dann das Ergebnis als neuen Wert *Datensatzliste* zurück, der aus den Batches besteht.</span><span class="sxs-lookup"><span data-stu-id="911da-105">It then returns the result as a new *Record list* value that consists of the batches.</span></span>

## <a name="syntax"></a><span data-ttu-id="911da-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="911da-106">Syntax</span></span>

```vb
SPLITLIST (list, number)
```

## <a name="arguments"></a><span data-ttu-id="911da-107">Argumente</span><span class="sxs-lookup"><span data-stu-id="911da-107">Arguments</span></span>

<span data-ttu-id="911da-108">`list`: *Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="911da-108">`list`: *Record list*</span></span>

<span data-ttu-id="911da-109">Der gültige Pfad einer Datenquelle des Datentyps *Datensatzliste*.</span><span class="sxs-lookup"><span data-stu-id="911da-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="911da-110">`number`: *Integer*</span><span class="sxs-lookup"><span data-stu-id="911da-110">`number`: *Integer*</span></span>

<span data-ttu-id="911da-111">Die maximale Anzahl angezeigter Datensätze pro Batch.</span><span class="sxs-lookup"><span data-stu-id="911da-111">The maximum number of records per batch.</span></span>

## <a name="return-values"></a><span data-ttu-id="911da-112">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="911da-112">Return values</span></span>

<span data-ttu-id="911da-113">*Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="911da-113">*Record list*</span></span>

<span data-ttu-id="911da-114">Die resultierende Liste der Datensätze.</span><span class="sxs-lookup"><span data-stu-id="911da-114">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="911da-115">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="911da-115">Usage notes</span></span>

<span data-ttu-id="911da-116">Die Liste der Batches, die zurückgegeben wird, enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="911da-116">The list of batches that is returned contains the following elements:</span></span>

 - <span data-ttu-id="911da-117">**Wert:** *Liste*</span><span class="sxs-lookup"><span data-stu-id="911da-117">**Value:** *List*</span></span>

    <span data-ttu-id="911da-118">Die Liste der Datensätze, die zum aktuellen Batch gehören.</span><span class="sxs-lookup"><span data-stu-id="911da-118">The list of records that belong to the current batch.</span></span>

- <span data-ttu-id="911da-119">**BatchNumber:** *Integer*</span><span class="sxs-lookup"><span data-stu-id="911da-119">**BatchNumber:** *Integer*</span></span>

    <span data-ttu-id="911da-120">Die Nummer des aktuellen Batches in der zurückgegebenen Liste.</span><span class="sxs-lookup"><span data-stu-id="911da-120">The number of the current batch in the returned list.</span></span>

## <a name="example"></a><span data-ttu-id="911da-121">Beispiel</span><span class="sxs-lookup"><span data-stu-id="911da-121">Example</span></span>

<span data-ttu-id="911da-122">In der folgenden Abbildung wird eine Datenquelle **Positionen** als eine Datensatzliste von drei Datensätzen erstellt.</span><span class="sxs-lookup"><span data-stu-id="911da-122">In the following illustration, a **Lines** data source is created as a record list that has three records.</span></span> <span data-ttu-id="911da-123">Diese Liste wird in Chargen aufgeteilt, die jeweils bis zu zwei Datensätze enthalten.</span><span class="sxs-lookup"><span data-stu-id="911da-123">This list is divided into batches, each of which contains up to two records.</span></span>

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

<span data-ttu-id="911da-124">Die folgende Abbildung zeigt das entworfene Formatlayout.</span><span class="sxs-lookup"><span data-stu-id="911da-124">The following illustration shows the designed format layout.</span></span> <span data-ttu-id="911da-125">In diesem Formatlayout werden die Bindungen an die Datenquelle **Positionen** erstellt, mit Ausgabe im XML-Format zu generieren.</span><span class="sxs-lookup"><span data-stu-id="911da-125">In this format layout, bindings to the **Lines** data source are created to generate output in XML format.</span></span> <span data-ttu-id="911da-126">Dies Ausgabe präsentiert einzelne Knoten für jede Charge und die darin befindlichen Datensätze.</span><span class="sxs-lookup"><span data-stu-id="911da-126">This output presents individual nodes for each batch and the records in it.</span></span>

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

<span data-ttu-id="911da-127">Die folgende Abbildung zeigt das Ergebnis, wenn das entworfene Format ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="911da-127">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a><span data-ttu-id="911da-128">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="911da-128">Additional resources</span></span>

[<span data-ttu-id="911da-129">Listenfunktionen</span><span class="sxs-lookup"><span data-stu-id="911da-129">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]