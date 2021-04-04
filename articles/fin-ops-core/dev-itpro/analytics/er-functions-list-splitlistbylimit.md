---
title: SPLITLISTBYLIMIT EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der SPLITLISTBYLIMIT-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: 119ad3c363913ddaf3d6b890e36989d03e91b3c0
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565103"
---
# <a name="splitlistbylimit-er-function"></a><span data-ttu-id="d4f04-103">SPLITLISTBYLIMIT EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="d4f04-103">SPLITLISTBYLIMIT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d4f04-104">Die Funktion `SPLITLISTBYLIMIT` teilt die angegebene Liste in eine neue Liste von Unterlisten (Batches) auf.</span><span class="sxs-lookup"><span data-stu-id="d4f04-104">The `SPLITLISTBYLIMIT` function splits the specified list into a new list of sublists (batches).</span></span> <span data-ttu-id="d4f04-105">Die Anzahl der Datensätze in jedem Batch wird dynamisch berechnet.</span><span class="sxs-lookup"><span data-stu-id="d4f04-105">The number of records in each batch is dynamically calculated.</span></span> <span data-ttu-id="d4f04-106">Die Funktion gibt dann das Ergebnis als neuen Wert *Datensatzliste* zurück, der aus den Batches besteht.</span><span class="sxs-lookup"><span data-stu-id="d4f04-106">The function then returns the result as a new *Record list* value that consists of the batches.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4f04-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4f04-107">Syntax</span></span>

```vb
SPLITLISTBYLIMIT (list, limit value, limit source)
```

## <a name="arguments"></a><span data-ttu-id="d4f04-108">Argumente</span><span class="sxs-lookup"><span data-stu-id="d4f04-108">Arguments</span></span>

<span data-ttu-id="d4f04-109">`list`: *Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="d4f04-109">`list`: *Record list*</span></span>

<span data-ttu-id="d4f04-110">Der gültige Pfad einer Datenquelle des Datentyps *Datensatzliste*.</span><span class="sxs-lookup"><span data-stu-id="d4f04-110">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="d4f04-111">`limit value`: *Integer* oder *Real*</span><span class="sxs-lookup"><span data-stu-id="d4f04-111">`limit value`: *Integer* or *Real*</span></span>

<span data-ttu-id="d4f04-112">Der maximale Wert des Grenzwerts, der zum Aufteilen der ursprünglichen Liste in Batches verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d4f04-112">The maximum value of the limit that is used to split the original list into batches.</span></span>

<span data-ttu-id="d4f04-113">`limit source`: *Feld*</span><span class="sxs-lookup"><span data-stu-id="d4f04-113">`limit source`: *Field*</span></span>

<span data-ttu-id="d4f04-114">Der gültige Pfad eines Feldes des Typs *Integer* oder *Real* in der angegebenen Liste.</span><span class="sxs-lookup"><span data-stu-id="d4f04-114">The valid path of a field of the *Integer* or *Real* type in the specified list.</span></span> <span data-ttu-id="d4f04-115">Der Wert dieses Feldes definiert den Schritt, bei dem die Gesamtsumme erhöht wird.</span><span class="sxs-lookup"><span data-stu-id="d4f04-115">The value of this field defines the step that the total sum is increased on.</span></span>

## <a name="return-values"></a><span data-ttu-id="d4f04-116">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="d4f04-116">Return values</span></span>

<span data-ttu-id="d4f04-117">*Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="d4f04-117">*Record list*</span></span>

<span data-ttu-id="d4f04-118">Die resultierende Liste der Datensätze.</span><span class="sxs-lookup"><span data-stu-id="d4f04-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="d4f04-119">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="d4f04-119">Usage notes</span></span>

<span data-ttu-id="d4f04-120">Die Liste der Batches, die zurückgegeben wird, enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="d4f04-120">The list of batches that is returned contains the following elements:</span></span>

- <span data-ttu-id="d4f04-121">**Wert**: *Liste*</span><span class="sxs-lookup"><span data-stu-id="d4f04-121">**Value**: *List*</span></span>

    <span data-ttu-id="d4f04-122">Die Liste der Datensätze, die zum aktuellen Batch gehören.</span><span class="sxs-lookup"><span data-stu-id="d4f04-122">The list of records that belong to the current batch.</span></span>

- <span data-ttu-id="d4f04-123">**BatchNumber**: *Integer*</span><span class="sxs-lookup"><span data-stu-id="d4f04-123">**BatchNumber**: *Integer*</span></span>

    <span data-ttu-id="d4f04-124">Die Nummer des aktuellen Batches in der zurückgegebenen Liste.</span><span class="sxs-lookup"><span data-stu-id="d4f04-124">The number of the current batch in the returned list.</span></span>

<span data-ttu-id="d4f04-125">Die Begrenzung wird auf keinen einzelnen Artikel der ursprünglichen Liste angewendet, wenn die Begrenzungsquelle die definierte Begrenzung überschreitet.</span><span class="sxs-lookup"><span data-stu-id="d4f04-125">The limit isn't applied to a single item of the original list if the limit source exceeds the defined limit.</span></span>

## <a name="example"></a><span data-ttu-id="d4f04-126">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d4f04-126">Example</span></span>

<span data-ttu-id="d4f04-127">Die folgende Abbildung zeigt das Format der elektronischen Berichterstattung (EB).</span><span class="sxs-lookup"><span data-stu-id="d4f04-127">The following illustration shows an Electronic reporting (ER) format.</span></span>

<a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="Format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a>

<span data-ttu-id="d4f04-128">Die folgende Abbildung zeigt die Datenquellen an, die für das Format verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d4f04-128">The following illustration shows the data sources that are used for the format.</span></span>

<a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="Data sources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a>

<span data-ttu-id="d4f04-129">Die folgende Abbildung zeigt das Ergebnis an, wenn Format ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d4f04-129">The following illustration shows the result when the format is run.</span></span> <span data-ttu-id="d4f04-130">In diesem Fall ist die Ausgabeliste eine flache Liste von Warenartikeln.</span><span class="sxs-lookup"><span data-stu-id="d4f04-130">In this case, the output is a flat list of commodity items.</span></span>

<a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="Output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a>

<span data-ttu-id="d4f04-131">In den folgenden Abbildungen ist dasselbe Format so angepasst worden, dass es die Liste der Warenpositionen in Chargen präsentiert, wenn eine einzelne Charge Waren enthalten muss und das Gesamtgewicht nicht die Begrenzung von 9 überschreiten sollte.</span><span class="sxs-lookup"><span data-stu-id="d4f04-131">In the following illustrations, the same format has been adjusted so that it presents the list of commodity items in batches if a single batch must include commodities and the total weight should not exceed a limit of 9.</span></span>

<a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="Adjusted format" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a>

<a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="Data sources for the adjusted format" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a>

<span data-ttu-id="d4f04-132">Die folgende Abbildung zeigt das Ergebnis, wenn das angepasste Format ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d4f04-132">The following illustration shows the result when the adjusted format is run.</span></span>

<a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="Output of the adjusted format" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a>

> [!NOTE] 
> <span data-ttu-id="d4f04-133">Die Begrenzung wird nicht auf den letzten Artikel der ursprünglichen Liste angewendet, weil der Wert (**11**) der Begrenzungsquelle (**Gewicht**) die definierte Begrenzung (**9**) überschreitet.</span><span class="sxs-lookup"><span data-stu-id="d4f04-133">The limit isn't applied to the last item of the original list, because the value (**11**) of the limit source (**weight**) exceeds the defined limit (**9**).</span></span> <span data-ttu-id="d4f04-134">Um Unterlisten beim Erstellen von Berichten zu ignorieren, verwenden Sie entweder die Funktion `WHERE` oder den Ausdruck **Aktiviert** des entsprechenden Formatelements.</span><span class="sxs-lookup"><span data-stu-id="d4f04-134">To ignore sublists during report generation, use either the `WHERE` function or the **Enabled** expression of the corresponding format element, as you require.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d4f04-135">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d4f04-135">Additional resources</span></span>

[<span data-ttu-id="d4f04-136">Listenfunktionen</span><span class="sxs-lookup"><span data-stu-id="d4f04-136">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]