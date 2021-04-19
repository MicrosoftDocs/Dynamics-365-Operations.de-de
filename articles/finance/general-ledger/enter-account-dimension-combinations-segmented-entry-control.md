---
title: Eingeben von Konto- und Dimensionskombinationen (segmentierte Eintragssteuerung)
description: In diesem Artikel wird beschrieben, wie Konto- und Dimensions-Kombinationen oder Sachkonten eingegeben werden. Die Eintragserfahrung wird häufig als segmentiertes Eintragssteuerelement bezeichnet.
author: aprilolson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure
audience: Application User
ms.reviewer: roschlom
ms.custom: 14071
ms.assetid: e6fce826-c403-4d91-a78b-e9a58c44ac03
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 21a67e4760e870b4d0a576523cbece0db5fa1923
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837985"
---
# <a name="enter-account-and-dimension-combinations-segmented-entry-control"></a><span data-ttu-id="a31f1-104">Eingeben von Konto- und Dimensionskombinationen (segmentierte Eintragssteuerung)</span><span class="sxs-lookup"><span data-stu-id="a31f1-104">Enter account and dimension combinations (segmented entry control)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a31f1-105">In diesem Artikel wird beschrieben, wie Konto- und Dimensions-Kombinationen oder Sachkonten eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a31f1-105">This article describes how to enter account and dimension combinations or ledger accounts.</span></span> <span data-ttu-id="a31f1-106">Die Eintragserfahrung wird häufig als segmentiertes Eintragssteuerelement bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="a31f1-106">The entry experience is often referred to as segmented entry control.</span></span>

<span data-ttu-id="a31f1-107">Benutzer geben Konto- und Dimensionskombinationen auf verschiedenen Seiten ein, z. B. auf Seiten für die allgemeine Erfassung, Budgetierung und Buchungsdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="a31f1-107">Users enter account and dimension combinations on various pages, such as pages for general journals, budgeting, and posting definitions.</span></span> <span data-ttu-id="a31f1-108">Die gültigen Konto- und Dimensionskombinationen hängen von den dem Sachkonto zugewiesenen Kontostrukturen und den erweiterten Regeln ab, die den Kontostrukturen zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="a31f1-108">The valid account and dimension combinations depend on the account structures that are assigned to the ledger and the advanced rules that are assigned to the account structures.</span></span> <span data-ttu-id="a31f1-109">Wenn Benutzer eine Kombination eingeben, können sie entweder die Werttypen manuell eingeben oder die vielfältigen Suchfunktionen nutzen.</span><span class="sxs-lookup"><span data-stu-id="a31f1-109">When users enter a combination, they can either manually type the values or take advantage of a rich, lookup experience.</span></span> <span data-ttu-id="a31f1-110">Wenn Sie das Feld eingeben, können Sie mit der Eingabe beginnen und es wird nach dem Wert und der Beschreibung gesucht.</span><span class="sxs-lookup"><span data-stu-id="a31f1-110">When you enter the field, you can start to type and it will search the value and the description.</span></span> <span data-ttu-id="a31f1-111">Wenn Sie z. B. Typ 180 eingeben wird ein Wert gesucht, der mit dieser Kontokombination beginnt.</span><span class="sxs-lookup"><span data-stu-id="a31f1-111">For example, if you type 180 it will search any value that begins with that number combination.</span></span> <span data-ttu-id="a31f1-112">Oder Sie können Bargeld eingeben und es wird jeder beliebige Wert gesucht, der eine Beschreibung hat, die mit "Bar" beginnt.</span><span class="sxs-lookup"><span data-stu-id="a31f1-112">Or you may type Cash and it will search any value that has a description that begins with Cash.</span></span> <span data-ttu-id="a31f1-113">Sie können einen Platzhalter, wie \*Bargeld oder \*180 eingeben, um den Wert oder die Beschreibung zu suchen, die das Kriterium enthalten.</span><span class="sxs-lookup"><span data-stu-id="a31f1-113">You can also use a wildcard, such as \*Cash or \*180 to search if the value or description contain the search criteria.</span></span> 

<span data-ttu-id="a31f1-114">In der folgenden Tabelle werden die Tastenkombinationen beschrieben, die verwendet werden können, wenn die Suche geschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="a31f1-114">The following table describes the keyboard shortcuts that can be used when the lookup is closed.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a31f1-115">Tastenkombination</span><span class="sxs-lookup"><span data-stu-id="a31f1-115">Keyboard shortcut</span></span></th>
<th><span data-ttu-id="a31f1-116">Aktion</span><span class="sxs-lookup"><span data-stu-id="a31f1-116">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a31f1-117">ALT+NACH-UNTEN-TASTE</span><span class="sxs-lookup"><span data-stu-id="a31f1-117">Alt+Down Arrow</span></span></td>
<td><span data-ttu-id="a31f1-118">Öffnet die Suche.</span><span class="sxs-lookup"><span data-stu-id="a31f1-118">Open the lookup.</span></span> <span data-ttu-id="a31f1-119">Wenn Sie ein zweites Mal die Kombination ALT+NACH-UNTEN-TASTE drücken, wechselt der Fokus zu den Segmenten im Flyout.</span><span class="sxs-lookup"><span data-stu-id="a31f1-119">If you press Alt+Down Arrow a second time, the focus moves to the segments in the flyout.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="a31f1-120">EINGABETASTE und UMSCHALT+EINGABETASTE</span><span class="sxs-lookup"><span data-stu-id="a31f1-120">Enter and Shift+Enter</span></span></li>
<li><span data-ttu-id="a31f1-121">Trennzeichen für Kontenplan</span><span class="sxs-lookup"><span data-stu-id="a31f1-121">Chart of accounts delimiter</span></span></li>
<li><span data-ttu-id="a31f1-122">NACH-RECHTS-TASTE und NACH-LINKS-TASTE</span><span class="sxs-lookup"><span data-stu-id="a31f1-122">Right Arrow and Left Arrow</span></span></li>
</ul></td>
<td><span data-ttu-id="a31f1-123">Wechselt zum nächsten bzw. vorhergehenden Segment.</span><span class="sxs-lookup"><span data-stu-id="a31f1-123">Move to the next or previous segment.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a31f1-124">Registerkarte</span><span class="sxs-lookup"><span data-stu-id="a31f1-124">Tab</span></span></td>
<td><span data-ttu-id="a31f1-125">Wechselt zum nächsten Feld im Raster.</span><span class="sxs-lookup"><span data-stu-id="a31f1-125">Move to the next field in the grid.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a31f1-126">In der folgenden Tabelle werden die Tastenkombinationen beschrieben, die verwendet werden können, wenn die Suche geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="a31f1-126">The following table describes the keyboard shortcuts that can be used when the lookup is open.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a31f1-127">Tastenkombination</span><span class="sxs-lookup"><span data-stu-id="a31f1-127">Keyboard shortcut</span></span></th>
<th><span data-ttu-id="a31f1-128">Aktion</span><span class="sxs-lookup"><span data-stu-id="a31f1-128">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a31f1-129">ESC</span><span class="sxs-lookup"><span data-stu-id="a31f1-129">Esc</span></span></td>
<td><span data-ttu-id="a31f1-130">Schließt die Suche.</span><span class="sxs-lookup"><span data-stu-id="a31f1-130">Close the lookup.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="a31f1-131">NACH-OBEN-TASTE und NACH-UNTEN-TASTE</span><span class="sxs-lookup"><span data-stu-id="a31f1-131">Up Arrow and Down Arrow</span></span></li>
<li><span data-ttu-id="a31f1-132">BILD-AUF und BILD-AB</span><span class="sxs-lookup"><span data-stu-id="a31f1-132">Page Up and Page Down</span></span></li>
<li><span data-ttu-id="a31f1-133">POS1 und ENDE-TASTE</span><span class="sxs-lookup"><span data-stu-id="a31f1-133">Home and End</span></span></li>
</ul></td>
<td><span data-ttu-id="a31f1-134">Wechselt zum vorherigen bzw. nächsten Wert in den Listen, zur vorherigen bzw. nächsten Gruppe von Werten oder zum ersten bzw. letzten Element in der Suche.</span><span class="sxs-lookup"><span data-stu-id="a31f1-134">Move to the previous or next value in the lists, to the previous or next group of values, or to the first or last element in the lookup.</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="a31f1-135">Trennzeichen für Kontenplan</span><span class="sxs-lookup"><span data-stu-id="a31f1-135">Chart of accounts delimiter</span></span></li>
<li><span data-ttu-id="a31f1-136">NACH-RECHTS-TASTE und NACH-LINKS-TASTE</span><span class="sxs-lookup"><span data-stu-id="a31f1-136">Right Arrow and Left Arrow</span></span></li>
</ul></td>
<td><span data-ttu-id="a31f1-137">Wechselt zum nächsten bzw. vorhergehenden Segment.</span><span class="sxs-lookup"><span data-stu-id="a31f1-137">Move to the next or previous segment.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a31f1-138">Registerkarte</span><span class="sxs-lookup"><span data-stu-id="a31f1-138">Tab</span></span></td>
<td><span data-ttu-id="a31f1-139">Wechselt zum nächsten Feld im Raster.</span><span class="sxs-lookup"><span data-stu-id="a31f1-139">Move to the next field in the grid.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a31f1-140">Alt+W</span><span class="sxs-lookup"><span data-stu-id="a31f1-140">Alt+W</span></span></td>
<td><span data-ttu-id="a31f1-141">Wechselt zwischen <strong>Alle anzeigen</strong> und <strong>Gültige anzeigen</strong>.</span><span class="sxs-lookup"><span data-stu-id="a31f1-141">Switch between <strong>Show all</strong> and <strong>Show valid</strong>.</span></span></td>
</tr>
</tbody>
</table>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]