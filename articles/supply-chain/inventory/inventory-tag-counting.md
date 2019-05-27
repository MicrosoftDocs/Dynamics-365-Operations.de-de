---
title: Markierungsinventur
description: Dieser Artikel enthält Informationen zu Umlagerungen, die Sie verwenden, um die tatsächlichen Inhalt eines Lagerorts mit dem verfügbaren Lagerbestand zu vergleichen.
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCountTag
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 11594
ms.assetid: 03772d0e-5c37-454c-ab85-82bc8b60a76d
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dff899d0e6d94287c0f1924fe1787189d79c09f4
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570833"
---
# <a name="inventory-tag-counting"></a><span data-ttu-id="420b1-103">Markierungsinventur</span><span class="sxs-lookup"><span data-stu-id="420b1-103">Inventory tag counting</span></span>

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

<span data-ttu-id="420b1-104">Dieser Artikel enthält Informationen zu Umlagerungen, die Sie verwenden, um die tatsächlichen Inhalt eines Lagerorts mit dem verfügbaren Lagerbestand zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="420b1-104">This article provides information about tag counting, which you use to compare the actual contents of a warehouse with the on-hand inventory.</span></span>

<span data-ttu-id="420b1-105">Wenn Sie Positionen in der markierungsbasierte **Zählvorgang** Seite erstellen, platzieren Sie eine Markierungsnummer Nummer auf jedem Lagerartikel, wie einer Zahl zwischen 1 und 500.</span><span class="sxs-lookup"><span data-stu-id="420b1-105">By creating lines on the **Tag counting** page, you place a tag number on each inventory item, such as a number from 1 to 500.</span></span> <span data-ttu-id="420b1-106">Während der Zählung die Artikelnummer und die Anzahl auf einer entsprechenden Markierung ein.</span><span class="sxs-lookup"><span data-stu-id="420b1-106">During the count, you enter the item number and the quantity on a corresponding tag.</span></span> <span data-ttu-id="420b1-107">Diese Markierung kann als Grundlage für die Eingabe in der Markierungsinventurerfassung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="420b1-107">This tag can then be used as the basis for input in the tag counting journal.</span></span> <span data-ttu-id="420b1-108">Nach dem Buchen der Markierungs-Inventurerfassung wird eine neue Inventurerfassung auf der Seite **Inventur**erstellt.</span><span class="sxs-lookup"><span data-stu-id="420b1-108">After you post the tag counting journal, a new counting journal is created on the **Counting** page.</span></span> <span data-ttu-id="420b1-109">Die neue Erfassung basiert auf den Positionen der Markierungs-Inventurerfassung, die Sie selbst erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="420b1-109">The new journal is based on the tag counting journal lines that you created.</span></span> <span data-ttu-id="420b1-110">Um Inventurartikel für eine bestimmte Lagerdimension zu markieren, wählen Sie die Dimension auf der Seite **Dimension anzeigen**aus, die angezeigt wird, wenn Sie die Markierungs-Inventurerfassung erstellen.</span><span class="sxs-lookup"><span data-stu-id="420b1-110">To tag-count items by a specific inventory dimension, select the dimension on the **Display dimension** page that is displayed when you create the tag counting journal.</span></span> <span data-ttu-id="420b1-111">Um beispielsweise Artikel an einem bestimmten Lagerort zu inventarisieren, aktivieren Sie das **Lagerort**-Kontrollkästchen.</span><span class="sxs-lookup"><span data-stu-id="420b1-111">For example, to count items in a specific warehouse, select the **Warehouse** check box.</span></span> <span data-ttu-id="420b1-112">Wenn der **Artikel während der Inventur sperren**-Schieberegler auf der **Parameter für Lager- und Lagerortverwaltung**-Seite aktiviert ist, können Artikel nicht innerhalb der Inventur physisch aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="420b1-112">If the **Lock items during count** slider on the **Inventory and warehouse management parameters** page is selected, items can't be physically updated during counting.</span></span> <span data-ttu-id="420b1-113">Allerdings werden Artikel in den Markierungs-Inventurerfassungen nicht während der Inventur gesperrt.</span><span class="sxs-lookup"><span data-stu-id="420b1-113">However, items in tag counting journals aren't locked during counting.</span></span> <span data-ttu-id="420b1-114">Lagerbuchungen werden nicht erstellt, bis die Positionen der Markungsinventur an eine Inventurerfassung übermittelt und gebucht sind.</span><span class="sxs-lookup"><span data-stu-id="420b1-114">Inventory transactions aren't created until the tag counting lines are posted and transferred to a counting journal.</span></span> <span data-ttu-id="420b1-115">Wenn Markierungen nach dem Zufallsprinzip eingegeben werden und Sie fehlende Markierungen ermitteln möchten, klicken Sie auf den Spaltenkopf **Markierung**, damit die Positionen sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="420b1-115">If tags are entered randomly, and you want to identify missing tags, click the **Tag** column header to sort the lines by tag.</span></span>

<a name="additional-resources"></a><span data-ttu-id="420b1-116">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="420b1-116">Additional resources</span></span>
--------

[<span data-ttu-id="420b1-117">Zykluszählung</span><span class="sxs-lookup"><span data-stu-id="420b1-117">Cycle counting</span></span>](../warehousing/cycle-counting.md)
