---
title: "Standardgegenkonten für Kreditorenrechnungserfassungen und Rechnungsgenehmigungserfassungen"
description: 
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 62093
ms.assetid: 553933ca-928d-4031-bb8c-f9cff458320b
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: c2b62eafc71b5d1ad4eaaf252efd1dcbb97b86f3
ms.contentlocale: de-de
ms.lasthandoff: 08/29/2017

---

# <a name="default-offset-accounts-for-vendor-invoice-journals-and-invoice-approval-journals"></a><span data-ttu-id="83ce3-102">Standardgegenkonten für Kreditorenrechnungserfassungen und Rechnungsgenehmigungserfassungen</span><span class="sxs-lookup"><span data-stu-id="83ce3-102">Default offset accounts for vendor invoice journals and invoice approval journals</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="83ce3-103">Standardgegenkonten werden auf den folgenden Kreditorenrechnungserfassungs-Seiten verwendet:</span><span class="sxs-lookup"><span data-stu-id="83ce3-103">Default offset accounts are used on the following vendor invoice journal pages:</span></span>

-   <span data-ttu-id="83ce3-104">Rechnungserfassung</span><span class="sxs-lookup"><span data-stu-id="83ce3-104">Invoice journal</span></span>
-   <span data-ttu-id="83ce3-105">Rechnungsgenehmigungs-Erfassung</span><span class="sxs-lookup"><span data-stu-id="83ce3-105">Invoice approval journal</span></span>

<span data-ttu-id="83ce3-106">Verwenden Sie die folgende Tabelle, um zu entscheiden, wohin Standardkonten für Rechnungserfassungen zugewiesen werden sollten.</span><span class="sxs-lookup"><span data-stu-id="83ce3-106">Use the following table to help decide where you should assign default accounts for invoice journals.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="83ce3-107">Standardgegenkonten hier einrichten</span><span class="sxs-lookup"><span data-stu-id="83ce3-107">Set up default accounts here</span></span></th>
<th><span data-ttu-id="83ce3-108">Wo Standardkonten bereitgestellt werden</span><span class="sxs-lookup"><span data-stu-id="83ce3-108">Where default accounts are provided</span></span></th>
<th><span data-ttu-id="83ce3-109">Wie sich diese Option auf die Verarbeitung auswirkt</span><span class="sxs-lookup"><span data-stu-id="83ce3-109">How this option affects processing</span></span></th>
<th><span data-ttu-id="83ce3-110">Wann Sie diese Option verwenden sollten</span><span class="sxs-lookup"><span data-stu-id="83ce3-110">When you should use this option</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="83ce3-111"><strong>Kreditorengruppe</strong> – Richten Sie Standardgegenkonten für Kreditorengruppen auf der Seite <strong>Standardkontoeinstellungen</strong> ein, die Sie von der Seite <strong>Kreditorengruppen</strong> aus öffnen können.</span><span class="sxs-lookup"><span data-stu-id="83ce3-111"><strong>Vendor group</strong> – Set up default offset accounts for vendor groups on the <strong>Default account setup</strong> page, which you can open from the <strong>Vendor groups</strong> page.</span></span></td>
<td><ul>
<li><span data-ttu-id="83ce3-112">Kreditorenkonto</span><span class="sxs-lookup"><span data-stu-id="83ce3-112">Vendor account</span></span></li>
<li><span data-ttu-id="83ce3-113">Erfassungseinträge für Kreditorenkonten in der Kreditorengruppe, wenn keine Standardkonten für Kreditorenkonten angegeben werden</span><span class="sxs-lookup"><span data-stu-id="83ce3-113">Journal entries for vendor accounts in the vendor group, if default accounts aren’t specified for vendor accounts</span></span></li>
</ul></td>
<td><span data-ttu-id="83ce3-114">Die Standardgegenkonten für Kreditorengruppen werden auf der Seite <strong>Standardkontoeinstellungen</strong> als Standardgegenkonten für Kreditoren angezeigt.</span><span class="sxs-lookup"><span data-stu-id="83ce3-114">The default offset accounts for vendor groups are shown as default offset accounts for vendors on the <strong>Default account setup</strong> page.</span></span> <span data-ttu-id="83ce3-115">Sie können diese Seite über die Listenseite <strong>Alle Kreditoren</strong> öffnen.</span><span class="sxs-lookup"><span data-stu-id="83ce3-115">You can open this page from the <strong>All vendors</strong> list page.</span></span></td>
<td><span data-ttu-id="83ce3-116">Verwenden Sie diese Option, wenn Sie im Laufe der Zeit in der Regel für dieselben Arten von Produkten oder Dienstleistungen von denselben Kreditorengruppen bezahlen.</span><span class="sxs-lookup"><span data-stu-id="83ce3-116">Use this option if you typically pay for the same types of things from the same vendor groups over time.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="83ce3-117"><strong>Kreditorenkonto</strong> – Richten Sie Standardkonten für Kreditorenkonten auf der Seite <strong>Standardkontoeinstellungen</strong> ein, die Sie von der Seite <strong>Kreditoren</strong> aus öffnen können.</span><span class="sxs-lookup"><span data-stu-id="83ce3-117"><strong>Vendor account</strong> – Set up default accounts for vendor accounts on the <strong>Default account setup</strong> page, which you can open from the <strong>Vendors</strong> page.</span></span></td>
<td><span data-ttu-id="83ce3-118">Erfassungseinträge für das Kreditorenkonto</span><span class="sxs-lookup"><span data-stu-id="83ce3-118">Journal entries for the vendor account</span></span></td>
<td><span data-ttu-id="83ce3-119">Die Standardgegenkonten für Kreditorenkonten werden als Standardgegenkonten für Erfassungseinträge für das Kreditorenkonto anzeigt.</span><span class="sxs-lookup"><span data-stu-id="83ce3-119">The default offset accounts for vendor accounts are shown as default offset accounts for journal entries for the vendor account.</span></span></td>
<td><span data-ttu-id="83ce3-120">Verwenden Sie diese Option, wenn Sie im Laufe der Zeit in der Regel für dieselben Arten von Produkten oder Dienstleistungen von denselben Kreditoren bezahlen.</span><span class="sxs-lookup"><span data-stu-id="83ce3-120">Use this option if you typically pay for the same types of things from the same vendors over time.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="83ce3-121"><strong>Erfassungsnamen</strong> – Richten Sie Standardgegenkonten für Erfassungen auf der Seite <strong>Erfassungsnamen</strong> ein.</span><span class="sxs-lookup"><span data-stu-id="83ce3-121"><strong>Journal names</strong> – Set up default offset accounts for journals on the <strong>Journal names</strong> page.</span></span> <span data-ttu-id="83ce3-122">Wählen Sie die Option <strong>Festes Gegenkonto</strong> aus.</span><span class="sxs-lookup"><span data-stu-id="83ce3-122">Select the <strong>Fixed offset account</strong> option.</span></span> <span data-ttu-id="83ce3-123">Beachten Sie, dass Sie keine Standardgegenkonten zu Erfassungsnamen angeben können, wenn der Erfassungstyp der Erfassungsnamen <strong>Rechnungsbuch</strong> oder <strong>Genehmigung</strong> ist.</span><span class="sxs-lookup"><span data-stu-id="83ce3-123">Note that you can't specify default offset accounts on journal names if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><ul>
<li><span data-ttu-id="83ce3-124">Erfassungskopf, der den gleichen Erfassungsnamen verwendet</span><span class="sxs-lookup"><span data-stu-id="83ce3-124">Journal header that uses the journal name</span></span></li>
<li><span data-ttu-id="83ce3-125">Erfassungseinträge in Erfassungen, die den Erfassungsnamen verwenden</span><span class="sxs-lookup"><span data-stu-id="83ce3-125">Journal entries in journals that use the journal name</span></span></li>
</ul></td>
<td><span data-ttu-id="83ce3-126">Wenn die Option <strong>Festes Gegenkonto</strong> auf der Seite <strong>Erfassungsnamen</strong> ausgewählt ist, setzt das Gegenkonto für den Erfassungsnamen das Standardgegenkonto für den Kreditor oder die Kreditorengruppe außer Kraft.</span><span class="sxs-lookup"><span data-stu-id="83ce3-126">If the <strong>Fixed offset account</strong> option on the <strong>Journal names</strong> page is selected, the offset account for the journal name overrides the default offset account for the vendor or vendor group.</span></span></td>
<td><span data-ttu-id="83ce3-127">Verwenden Sie diese Option, um Erfassungen für bestimmte Kosten und Ausgaben einzurichten, die für bestimmte Konten berechnet werden, unabhängig davon, wer der Kreditor ist, oder zu welcher Kreditorengruppe er gehört.</span><span class="sxs-lookup"><span data-stu-id="83ce3-127">Use this option to set up journals for specific costs and expenses that are charged to specific accounts, regardless of the vendor or the vendor group that the vendor belongs to.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="83ce3-128"><strong>Erfassungsnamen</strong> – Richten Sie Standardgegenkonten für Erfassungen auf der Seite <strong>Erfassungsnamen</strong> ein.</span><span class="sxs-lookup"><span data-stu-id="83ce3-128"><strong>Journal names</strong> – Set up default offset accounts for journals on the <strong>Journal names</strong> page.</span></span> <span data-ttu-id="83ce3-129">Deaktivieren Sie die Option <strong>Festes Gegenkonto</strong>.</span><span class="sxs-lookup"><span data-stu-id="83ce3-129">Clear the <strong>Fixed offset account</strong> option.</span></span> <span data-ttu-id="83ce3-130">Beachten Sie, dass Sie keine Standardgegenkonten zu Erfassungsnamen angeben können, wenn der Erfassungstyp der Erfassungsnamen <strong>Rechnungsbuch</strong> oder <strong>Genehmigung</strong> ist.</span><span class="sxs-lookup"><span data-stu-id="83ce3-130">Note that you can't specify default offset accounts on journal names if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><ul>
<li><span data-ttu-id="83ce3-131">Erfassungskopf</span><span class="sxs-lookup"><span data-stu-id="83ce3-131">Journal header</span></span></li>
<li><span data-ttu-id="83ce3-132">Erfassungseinträge in Erfassungen, die den Erfassungsnamen verwenden</span><span class="sxs-lookup"><span data-stu-id="83ce3-132">Journal entries in journals that use the journal name</span></span></li>
</ul></td>
<td><span data-ttu-id="83ce3-133">Diese Standardeinträge werden auf Erfassungskopfseiten verwendet, und das Gegenkonto auf der Erfassungskopfseite wird als Standardeintrag auf den Erfassungsbelegseiten verwendet.</span><span class="sxs-lookup"><span data-stu-id="83ce3-133">These default entries are used on journal header pages, and the offset account on the journal header page is used as a default entry on the journal voucher pages.</span></span> <span data-ttu-id="83ce3-134">Standardkonten von der Seite <strong>Erfassungsnamen </strong>werden nur verwendet, wenn für das Kreditorenkonto keine Standardkonten eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="83ce3-134">Default accounts from the <strong>Journal names </strong>page are used only if default accounts aren’t set up for the vendor account.</span></span></td>
<td><span data-ttu-id="83ce3-135">Verwenden Sie diese Option, um Standardkonten einzurichten, die verwendet werden, wenn kein standardmäßiges Kreditorengegenkonto zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="83ce3-135">Use this option to set up default accounts that are used when a default vendor offset account isn't assigned.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="83ce3-136"><strong>Erfassungskopf</strong> – Richten Sie ein Standardgegenkonto für eine Erfassung als ein Standardeintrag auf den Erfassungsbelegseiten ein.</span><span class="sxs-lookup"><span data-stu-id="83ce3-136"><strong>Journal header</strong> – Set up a default offset account for a journal as a default entry on the journal voucher pages.</span></span> <span data-ttu-id="83ce3-137">Beachten Sie, dass Sie keine Standardgegenkonten auf dem Erfassungskopf angeben können, wenn der Erfassungstyp der Erfassungsnamen <strong>Rechnungsbuch</strong> oder <strong>Genehmigung</strong> ist.</span><span class="sxs-lookup"><span data-stu-id="83ce3-137">Note that you can't specify default offset accounts on the journal header if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><span data-ttu-id="83ce3-138">Erfassungseinträge in der Erfassung</span><span class="sxs-lookup"><span data-stu-id="83ce3-138">Journal entries in the journal</span></span></td>
<td><span data-ttu-id="83ce3-139">Das Standardgegenkonto für eine Erfassung wird als Standardeintrag auf den Erfassungsbelegseiten verwendet.</span><span class="sxs-lookup"><span data-stu-id="83ce3-139">The default offset account for a journal is used as the default entry on the journal voucher pages.</span></span></td>
<td><span data-ttu-id="83ce3-140">Verwenden Sie diese Option, um die Dateneingabe zu beschleunigen, wenn die meisten Einträge in einer Erfassung das gleiche Gegenkonto haben.</span><span class="sxs-lookup"><span data-stu-id="83ce3-140">Use this option to help speed up data entry if most entries in a journal have the same offset account.</span></span></td>
</tr>
</tbody>
</table>






