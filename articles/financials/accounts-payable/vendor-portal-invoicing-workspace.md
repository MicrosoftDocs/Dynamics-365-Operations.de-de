---
title: "Arbeitsbereich für Kreditor-Kooperationsrechungen"
description: "In diesem Thema wird erläutert, wie Sie Kreditorenrechnungen anzeigen und Rechnungen vom Arbeitsberiech\"Kreditorenzusammenarbeit-Rechnungsstellung\" senden können."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendInvoiceWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 221534
ms.assetid: c4ed62f3-d351-41d7-a2ad-790576cde4ab
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 57fc1c21394d91f6a8bd4726c9d948c8ae2cf4d0
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---

# <a name="vendor-collaboration-invoicing-workspace"></a><span data-ttu-id="21ffb-103">Arbeitsbereich für Kreditor-Kooperationsrechungen</span><span class="sxs-lookup"><span data-stu-id="21ffb-103">Vendor collaboration invoicing workspace</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="21ffb-104">In diesem Thema wird erläutert, wie Sie Kreditorenrechnungen anzeigen und Rechnungen vom Arbeitsberiech"Kreditorenzusammenarbeit-Rechnungsstellung" senden können.</span><span class="sxs-lookup"><span data-stu-id="21ffb-104">This topic explains how you can view vendor invoices and submit invoices from the vendor collaboration invoicing workspace.</span></span>

<span data-ttu-id="21ffb-105">Der Arbeitsbereich **Kreditorenzusammenarbeitsrechnungsstellung** kann verwendet werden, um Kreditorenrechnungsinformationen anzuzeigen und Rechnungen an Microsoft Dynamics 365 for Finance and Operations mithilfe der Workflowfähigkeiten zu senden.</span><span class="sxs-lookup"><span data-stu-id="21ffb-105">The **Vendor collaboration invoicing** workspace can be used to view vendor invoice information and to submit invoices to Microsoft Dynamics 365 for Finance and Operations using workflow capabilities.</span></span>


<a name="vendor-collaboration-invoicing-workspace"></a><span data-ttu-id="21ffb-106">Arbeitsbereich für Kreditorkooperationsrechnungen</span><span class="sxs-lookup"><span data-stu-id="21ffb-106">Vendor collaboration invoicing workspace</span></span>
----------------------------------------

### <a name="summary-tiles"></a><span data-ttu-id="21ffb-107">Zusammenfassungskacheln</span><span class="sxs-lookup"><span data-stu-id="21ffb-107">Summary tiles</span></span>

<span data-ttu-id="21ffb-108">Die Kacheln **Zusammenfassung** bieten einen Überblick über die Rechnungen für den ausgewählten Kreditor.</span><span class="sxs-lookup"><span data-stu-id="21ffb-108">The **Summary** tiles give an overview of the invoices for the selected vendor.</span></span> <span data-ttu-id="21ffb-109">Sie können Rechnungen nach Status anzeigen.</span><span class="sxs-lookup"><span data-stu-id="21ffb-109">You can view invoices by their state.</span></span>
-   <span data-ttu-id="21ffb-110">Entwurfsrechnungen wurden nicht an den Workflow übermittelt.</span><span class="sxs-lookup"><span data-stu-id="21ffb-110">Draft invoices have not been submitted to workflow.</span></span>
-   <span data-ttu-id="21ffb-111">Gesendete, nicht genehmigte Rechnungen sind jene Rechnungen, die vom Lieferanten übermittelt wurden, aber noch nicht in Finance and Operations gebucht sind.</span><span class="sxs-lookup"><span data-stu-id="21ffb-111">Submitted, not approved invoices are those invoices that the vendor has submitted, but they have not been posted in Finance and Operations.</span></span>
-   <span data-ttu-id="21ffb-112">Genehmigte, nicht bezahlte Rechnungen sind jene Rechnungen, die in Finance and Operations gebucht aber noch nicht vollständig bezahlt sind.</span><span class="sxs-lookup"><span data-stu-id="21ffb-112">Approved, not paid invoices are those that have been posted in Finance and Operations, but they have not yet been fully paid.</span></span>
-   <span data-ttu-id="21ffb-113">Bezahlte Rechnungen sind jene, die in Finance and Operations vollständig bezahlt wurden.</span><span class="sxs-lookup"><span data-stu-id="21ffb-113">Paid invoices are those that have been fully paid in Finance and Operations.</span></span>

<span data-ttu-id="21ffb-114">Durch Klicken auf eine Kachel öffnet sich eine gefilterte Ansicht der Seite **Rechnungsliste**.</span><span class="sxs-lookup"><span data-stu-id="21ffb-114">Clicking on a tile will open a filtered view of the **Invoices list** page.</span></span>

### <a name="tabular-lists"></a><span data-ttu-id="21ffb-115">Tabellarische Listen</span><span class="sxs-lookup"><span data-stu-id="21ffb-115">Tabular lists</span></span>

<span data-ttu-id="21ffb-116">Im Abschnitt **Tabellarische Listen** wird der Status der Rechnungsstellung auf ähnliche Weise aufgeteilt, wie die Zusammenfassung der Kacheln: Entwurfs- und übermittelte nicht genehmigte Listen.</span><span class="sxs-lookup"><span data-stu-id="21ffb-116">In the **Tabular lists** section, the status of the invoicing is broken down in similar ways as the summary tiles: Draft and Submitted, not approved lists.</span></span> <span data-ttu-id="21ffb-117">Im Entwurfstatus kann eine Rechnung an einen Workflow gesendet oder gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="21ffb-117">While in the Draft state, an invoice can be submitted to workflow or deleted.</span></span> <span data-ttu-id="21ffb-118">Die letzte tabellarische Liste ist eine Möglichkeit, Rechnungen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="21ffb-118">The last tabular list is an option to find invoices.</span></span> <span data-ttu-id="21ffb-119">Sie können Ihre Suche filtern, um schnellere Suchen zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="21ffb-119">You can filter as you search, to allow for faster searches.</span></span>

<a name="all-vendor-invoices-list-page"></a><span data-ttu-id="21ffb-120">Listenseite "Alle Kreditorenrechnungen"</span><span class="sxs-lookup"><span data-stu-id="21ffb-120">All vendor invoices list page</span></span>
-----------------------------

<span data-ttu-id="21ffb-121">Sie können alle gebuchten und nicht gebuchten Kreditorenrechnungen auf der Listenseite **Kreditor-Kooperationsrechnungen** anzeigen.</span><span class="sxs-lookup"><span data-stu-id="21ffb-121">You can view all posted and unposted vendor invoices on the **Vendor collaboration invoices** list page.</span></span> <span data-ttu-id="21ffb-122">Sie können mit dieser Listenseite den Zahlungsstatus der Rechnungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="21ffb-122">You can use this list page to view the payment status of the invoices.</span></span> <span data-ttu-id="21ffb-123">Der Zahlungsstatus enthält " Nicht gebuicht, unbezahlt, teilweise bezahlt und vollständig bezahlt.</span><span class="sxs-lookup"><span data-stu-id="21ffb-123">The payment statuses include Unposted, Unpaid, Partially paid, and Fully paid.</span></span>
<span data-ttu-id="21ffb-124">Eine neue Rechnung aus einer Bestellung erstellen</span><span class="sxs-lookup"><span data-stu-id="21ffb-124">Creating a new invoice from a purchase order</span></span>
--------------------------------------------

<span data-ttu-id="21ffb-125">Sie können eine neue Kreditorenrechnung erstellen, indem Sie die Aktivität **Neu** für den Arbeitsbereich **Kreditorenzusammenarbeitrechnungsstellung** auswählen.</span><span class="sxs-lookup"><span data-stu-id="21ffb-125">You can create a new vendor invoice by selecting the **New** action on the **Vendor collaboration invoicing** workspace.</span></span> <span data-ttu-id="21ffb-126">Die Bestellnummer und die Rechnungsnummer müssen vom Kreditor angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="21ffb-126">The purchase order number and invoice number must be provided by the vendor.</span></span> <span data-ttu-id="21ffb-127">Standardmäßig werden alle Positionen aus der Bestellung des neuen Kreditors auf der Rechnung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="21ffb-127">By default, all of the lines from the vendor's purchase order will appear on the new invoice.</span></span> <span data-ttu-id="21ffb-128">Die Menge und die Kostendaten können vor dem Versenden der Kreditorenrechnung an den Workflow verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="21ffb-128">The quantity and cost information can be edited prior to submitting the vendor invoice to workflow.</span></span> <span data-ttu-id="21ffb-129">Sie können Dateien, Hinweise, Bilder und URLs einer Rechnung zuordnen, bevor Sie diese senden.</span><span class="sxs-lookup"><span data-stu-id="21ffb-129">You can attach files, notes, images, and URLs to an invoice before submitting it.</span></span>



<span data-ttu-id="21ffb-130">Weitere Informationen finden Sie unter [Lieferantenzusammenarbeiten mit externen Kreditoren](../../supply-chain/procurement/vendor-collaboration-work-external-vendors.md)</span><span class="sxs-lookup"><span data-stu-id="21ffb-130">For more information, see [Vendor collaboration with external vendors](../../supply-chain/procurement/vendor-collaboration-work-external-vendors.md)</span></span>




