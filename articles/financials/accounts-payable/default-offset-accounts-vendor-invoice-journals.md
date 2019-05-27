---
title: Standardgegenkonten für Kreditorenrechnungserfassungen und Rechnungsgenehmigungserfassungen
description: Dieses Thema hilft Ihnen, zu entscheiden, wohin Standardkonten für Rechnungserfassungen zugewiesen werden sollten.
author: abruer
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 62093
ms.assetid: 553933ca-928d-4031-bb8c-f9cff458320b
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5cf772a0f0f9f99519322be1f37f961dc0ab2500
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1509105"
---
# <a name="default-offset-accounts-for-vendor-invoice-journals-and-invoice-approval-journals"></a><span data-ttu-id="3b1e9-103">Standardgegenkonten für Kreditorenrechnungserfassungen und Rechnungsgenehmigungserfassungen</span><span class="sxs-lookup"><span data-stu-id="3b1e9-103">Default offset accounts for vendor invoice journals and invoice approval journals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3b1e9-104">Standardgegenkonten werden auf den folgenden Kreditorenrechnungserfassungs-Seiten verwendet:</span><span class="sxs-lookup"><span data-stu-id="3b1e9-104">Default offset accounts are used on the following vendor invoice journal pages:</span></span>

-   <span data-ttu-id="3b1e9-105">Rechnungserfassung</span><span class="sxs-lookup"><span data-stu-id="3b1e9-105">Invoice journal</span></span>
-   <span data-ttu-id="3b1e9-106">Rechnungsgenehmigungs-Erfassung</span><span class="sxs-lookup"><span data-stu-id="3b1e9-106">Invoice approval journal</span></span>

<span data-ttu-id="3b1e9-107">Verwenden Sie die folgende Tabelle, um zu entscheiden, wohin Standardkonten für Rechnungserfassungen zugewiesen werden sollten.</span><span class="sxs-lookup"><span data-stu-id="3b1e9-107">Use the following table to help decide where you should assign default accounts for invoice journals.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3b1e9-108">Standardgegenkonten hier einrichten</span><span class="sxs-lookup"><span data-stu-id="3b1e9-108">Set up default accounts here</span></span></th>
<th><span data-ttu-id="3b1e9-109">Wo Standardkonten bereitgestellt werden</span><span class="sxs-lookup"><span data-stu-id="3b1e9-109">Where default accounts are provided</span></span></th>
<th><span data-ttu-id="3b1e9-110">Wie sich diese Option auf die Verarbeitung auswirkt</span><span class="sxs-lookup"><span data-stu-id="3b1e9-110">How this option affects processing</span></span></th>
<th><span data-ttu-id="3b1e9-111">Wann Sie diese Option verwenden sollten</span><span class="sxs-lookup"><span data-stu-id="3b1e9-111">When you should use this option</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3b1e9-112"><strong>Kreditorengruppe</strong> – Richten Sie Standardgegenkonten für Kreditorengruppen auf der Seite <strong>Standardkontoeinstellungen</strong> ein, die Sie von der Seite <strong>Kreditorengruppen</strong> aus öffnen können.</span><span class="sxs-lookup"><span data-stu-id="3b1e9-112"><strong>Vendor group</strong> – Set up default offset accounts for vendor groups on the <strong>Default account setup</strong> page, which you can open from the <strong>Vendor groups</strong> page.</span></span></td>
<td><ul>
<li><span data-ttu-id="3b1e9-113">Kreditorenkonto</span><span class="sxs-lookup"><span data-stu-id="3b1e9-113">Vendor account</span></span></li>
<li><span data-ttu-id="3b1e9-114">Erfassungseinträge für Kreditorenkonten in der Kreditorengruppe, wenn keine Standardkonten für Kreditorenkonten angegeben werden</span><span class="sxs-lookup"><span data-stu-id="3b1e9-114">Journal entries for vendor accounts in the vendor group, if default accounts aren’t specified for vendor accounts</span></span></li>
</ul></td>
<td><span data-ttu-id="3b1e9-115">Die Standardgegenkonten für Kreditorengruppen werden auf der Seite <strong>Standardkontoeinstellungen</strong> als Standardgegenkonten für Kreditoren angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3b1e9-115">The default offset accounts for vendor groups are shown as default offset accounts for vendors on the <strong>Default account setup</strong> page.</span></span> <span data-ttu-id="3b1e9-116">Sie können diese Seite über die Listenseite <strong>Alle Kreditoren</strong> öffnen.</span><span class="sxs-lookup"><span data-stu-id="3b1e9-116">You can open this page from the <strong>All vendors</strong> list page.</span></span></td>
<td><span data-ttu-id="3b1e9-117">Verwenden Sie diese Option, wenn Sie im Laufe der Zeit in der Regel für dieselben Arten von Produkten oder Dienstleistungen von denselben Kreditorengruppen bezahlen.</span><span class="sxs-lookup"><span data-stu-id="3b1e9-117">Use this option if you typically pay for the same types of things from the same vendor groups over time.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3b1e9-118"><strong>Kreditorenkonto</strong> – Richten Sie Standardkonten für Kreditorenkonten auf der Seite <strong>Standardkontoeinstellungen</strong> ein, die Sie von der Seite <strong>Kreditoren</strong> aus öffnen können.</span><span class="sxs-lookup"><span data-stu-id="3b1e9-118"><strong>Vendor account</strong> – Set up default accounts for vendor accounts on the <strong>Default account setup</strong> page, which you can open from the <strong>Vendors</strong> page.</span></span></td>
<td><span data-ttu-id="3b1e9-119">Erfassungseinträge für das Kreditorenkonto</span><span class="sxs-lookup"><span data-stu-id="3b1e9-119">Journal entries for the vendor account</span></span></td>
<td><span data-ttu-id="3b1e9-120">Die Standardgegenkonten für Kreditorenkonten werden als Standardgegenkonten für Erfassungseinträge für das Kreditorenkonto anzeigt.</span><span class="sxs-lookup"><span data-stu-id="3b1e9-120">The default offset accounts for vendor accounts are shown as default offset accounts for journal entries for the vendor account.</span></span></td>
<td><span data-ttu-id="3b1e9-121">Verwenden Sie diese Option, wenn Sie im Laufe der Zeit in der Regel für dieselben Arten von Produkten oder Dienstleistungen von denselben Kreditoren bezahlen.</span><span class="sxs-lookup"><span data-stu-id="3b1e9-121">Use this option if you typically pay for the same types of things from the same vendors over time.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3b1e9-122"><strong>Erfassungsnamen</strong> – Richten Sie Standardgegenkonten für Erfassungen auf der Seite <strong>Erfassungsnamen</strong> ein.</span><span class="sxs-lookup"><span data-stu-id="3b1e9-122"><strong>Journal names</strong> – Set up default offset accounts for journals on the <strong>Journal names</strong> page.</span></span> <span data-ttu-id="3b1e9-123">Wählen Sie die Option <strong>Festes Gegenkonto</strong> aus.</span><span class="sxs-lookup"><span data-stu-id="3b1e9-123">Select the <strong>Fixed offset account</strong> option.</span></span> <span data-ttu-id="3b1e9-124">Beachten Sie, dass Sie keine Standardgegenkonten zu Erfassungsnamen angeben können, wenn der Erfassungstyp der Erfassungsnamen <strong>Rechnungsbuch</strong> oder <strong>Genehmigung</strong> ist.</span><span class="sxs-lookup"><span data-stu-id="3b1e9-124">Note that you can&#39;t specify default offset accounts on journal names if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><ul>
<li><span data-ttu-id="3b1e9-125">Erfassungskopf, der den gleichen Erfassungsnamen verwendet</span><span class="sxs-lookup"><span data-stu-id="3b1e9-125">Journal header that uses the journal name</span></span></li>
<li><span data-ttu-id="3b1e9-126">Erfassungseinträge in Erfassungen, die den Erfassungsnamen verwenden</span><span class="sxs-lookup"><span data-stu-id="3b1e9-126">Journal entries in journals that use the journal name</span></span></li>
</ul></td>
<td><span data-ttu-id="3b1e9-127">Wenn die Option <strong>Festes Gegenkonto</strong> auf der Seite <strong>Erfassungsnamen</strong> ausgewählt ist, setzt das Gegenkonto für den Erfassungsnamen das Standardgegenkonto für den Kreditor oder die Kreditorengruppe außer Kraft.</span><span class="sxs-lookup"><span data-stu-id="3b1e9-127">If the <strong>Fixed offset account</strong> option on the <strong>Journal names</strong> page is selected, the offset account for the journal name overrides the default offset account for the vendor or vendor group.</span></span></td>
<td><span data-ttu-id="3b1e9-128">Verwenden Sie diese Option, um Erfassungen für bestimmte Kosten und Ausgaben einzurichten, die für bestimmte Konten berechnet werden, unabhängig davon, wer der Kreditor ist, oder zu welcher Kreditorengruppe er gehört.</span><span class="sxs-lookup"><span data-stu-id="3b1e9-128">Use this option to set up journals for specific costs and expenses that are charged to specific accounts, regardless of the vendor or the vendor group that the vendor belongs to.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3b1e9-129"><strong>Erfassungsnamen</strong> – Richten Sie Standardgegenkonten für Erfassungen auf der Seite <strong>Erfassungsnamen</strong> ein.</span><span class="sxs-lookup"><span data-stu-id="3b1e9-129"><strong>Journal names</strong> – Set up default offset accounts for journals on the <strong>Journal names</strong> page.</span></span> <span data-ttu-id="3b1e9-130">Deaktivieren Sie die Option <strong>Festes Gegenkonto</strong>.</span><span class="sxs-lookup"><span data-stu-id="3b1e9-130">Clear the <strong>Fixed offset account</strong> option.</span></span> <span data-ttu-id="3b1e9-131">Beachten Sie, dass Sie keine Standardgegenkonten zu Erfassungsnamen angeben können, wenn der Erfassungstyp der Erfassungsnamen <strong>Rechnungsbuch</strong> oder <strong>Genehmigung</strong> ist.</span><span class="sxs-lookup"><span data-stu-id="3b1e9-131">Note that you can&#39;t specify default offset accounts on journal names if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><ul>
<li><span data-ttu-id="3b1e9-132">Erfassungskopf</span><span class="sxs-lookup"><span data-stu-id="3b1e9-132">Journal header</span></span></li>
<li><span data-ttu-id="3b1e9-133">Erfassungseinträge in Erfassungen, die den Erfassungsnamen verwenden</span><span class="sxs-lookup"><span data-stu-id="3b1e9-133">Journal entries in journals that use the journal name</span></span></li>
</ul></td>
<td><span data-ttu-id="3b1e9-134">Diese Standardeinträge werden auf Erfassungskopfseiten verwendet, und das Gegenkonto auf der Erfassungskopfseite wird als Standardeintrag auf den Erfassungsbelegseiten verwendet.</span><span class="sxs-lookup"><span data-stu-id="3b1e9-134">These default entries are used on journal header pages, and the offset account on the journal header page is used as a default entry on the journal voucher pages.</span></span> <span data-ttu-id="3b1e9-135">Standardkonten von der Seite <strong>Erfassungsnamen </strong>werden nur verwendet, wenn für das Kreditorenkonto keine Standardkonten eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="3b1e9-135">Default accounts from the <strong>Journal names </strong>page are used only if default accounts aren’t set up for the vendor account.</span></span></td>
<td><span data-ttu-id="3b1e9-136">Verwenden Sie diese Option, um Standardkonten einzurichten, die verwendet werden, wenn kein standardmäßiges Kreditorengegenkonto zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="3b1e9-136">Use this option to set up default accounts that are used when a default vendor offset account isn&#39;t assigned.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3b1e9-137"><strong>Erfassungskopf</strong> – Richten Sie ein Standardgegenkonto für eine Erfassung als ein Standardeintrag auf den Erfassungsbelegseiten ein.</span><span class="sxs-lookup"><span data-stu-id="3b1e9-137"><strong>Journal header</strong> – Set up a default offset account for a journal as a default entry on the journal voucher pages.</span></span> <span data-ttu-id="3b1e9-138">Beachten Sie, dass Sie keine Standardgegenkonten auf dem Erfassungskopf angeben können, wenn der Erfassungstyp der Erfassungsnamen <strong>Rechnungsbuch</strong> oder <strong>Genehmigung</strong> ist.</span><span class="sxs-lookup"><span data-stu-id="3b1e9-138">Note that you can&#39;t specify default offset accounts on the journal header if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><span data-ttu-id="3b1e9-139">Erfassungseinträge in der Erfassung</span><span class="sxs-lookup"><span data-stu-id="3b1e9-139">Journal entries in the journal</span></span></td>
<td><span data-ttu-id="3b1e9-140">Das Standardgegenkonto für eine Erfassung wird als Standardeintrag auf den Erfassungsbelegseiten verwendet.</span><span class="sxs-lookup"><span data-stu-id="3b1e9-140">The default offset account for a journal is used as the default entry on the journal voucher pages.</span></span></td>
<td><span data-ttu-id="3b1e9-141">Verwenden Sie diese Option, um die Dateneingabe zu beschleunigen, wenn die meisten Einträge in einer Erfassung das gleiche Gegenkonto haben.</span><span class="sxs-lookup"><span data-stu-id="3b1e9-141">Use this option to help speed up data entry if most entries in a journal have the same offset account.</span></span></td>
</tr>
</tbody>
</table>





