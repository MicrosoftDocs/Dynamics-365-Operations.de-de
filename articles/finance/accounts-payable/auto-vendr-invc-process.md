---
title: Überblick über automatisierte Kreditorenabrechnungsprozesse
description: In diesem Thema werden die Funktionen zur Automatisierung der Verarbeitung Ihrer Kreditorenrechnungen und die Vorteile der Verwendung eines automatisierten Prozesses beschrieben.
author: abruer
manager: AnnBe
ms.date: 08/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-30
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 187b3c4f1a8b2c9ec6df95c19b261756ec4562dc
ms.sourcegitcommit: 6ffbae02de2eee1f3be9bab2da37a3771aae8bec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/30/2020
ms.locfileid: "3905013"
---
# <a name="automated-vendor-invoicing-processes-overview"></a><span data-ttu-id="61606-103">Überblick über automatisierte Kreditorenabrechnungsprozesse</span><span class="sxs-lookup"><span data-stu-id="61606-103">Automated vendor invoicing processes overview</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="61606-104">In diesem Thema werden die Funktionen zur Automatisierung der Verarbeitung Ihrer Kreditorenrechnungen und die Vorteile der Verwendung eines automatisierten Prozesses beschrieben.</span><span class="sxs-lookup"><span data-stu-id="61606-104">This topic describes the capability for automating your vendor invoice processing and the benefits of using an automated process.</span></span> <span data-ttu-id="61606-105">Die Funktionen hierfür werden in der Funktionsverwaltung aktiviert.</span><span class="sxs-lookup"><span data-stu-id="61606-105">This capability consists of features that are turned on in Feature management.</span></span> <span data-ttu-id="61606-106">Diese Funktionen gelten nur für Kreditorenrechnungen, nicht für Rechnungen, die über die **Rechnungserfassung** oder die Seite **Rechnungsbucherfassung** verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="61606-106">These features apply only to vendor invoices, not to invoices that are processed through the **Invoice journal** or **Invoice register journal** page.</span></span>

<span data-ttu-id="61606-107">Organisationen arbeiten häufig mit Dritten zusammen, um Papierrechnungen mithilfe einer optischen Zeichenerkennung (OCR) von einem Dienstanbieter zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="61606-107">Organizations often work with third parties to process paper invoices by using an optical character recognition (OCR) service provider.</span></span> <span data-ttu-id="61606-108">Vom Dienstanbieter erhalten sie dann maschinenlesbare Rechnungsmetadaten.</span><span class="sxs-lookup"><span data-stu-id="61606-108">The service provider returns machine-readable invoice metadata.</span></span> <span data-ttu-id="61606-109">Um die Automatisierung zu unterstützen, können Sie mit den Automatisierungsfunktionen für die Kreditorenkonten diese Artefakte aus den Kreditorenkonten verwenden.</span><span class="sxs-lookup"><span data-stu-id="61606-109">To help with automation, the Accounts payable automation features let you consume these artifacts from Accounts payable.</span></span>

<span data-ttu-id="61606-110">Sie können einige Kreditorenabrechnungsprozesse für Kreditorenkonten automatisieren.</span><span class="sxs-lookup"><span data-stu-id="61606-110">You can automate some Accounts payable vendor invoicing processes.</span></span> <span data-ttu-id="61606-111">Diese Prozesse umfassen das Übermitteln importierter Kreditorenrechnungen an das Workflowsystem und das Abgleichen der gebuchten Produktzugangspositionen mit ausstehenden Kreditorenrechnungspositionen.</span><span class="sxs-lookup"><span data-stu-id="61606-111">These processes include submitting imported vendor invoices to the workflow system and matching posted product receipt lines to pending vendor invoice lines.</span></span> <span data-ttu-id="61606-112">Der automatisierte Prozess zeigt Informationen über den Fortschritt einer Kreditorenrechnung an, während diese die einzelnen Prozesse durchläuft.</span><span class="sxs-lookup"><span data-stu-id="61606-112">The automated process shows information about the progress of a vendor invoice as it moves through each of the processes.</span></span> <span data-ttu-id="61606-113">Diese Funktion kann Sachbearbeitern und Mangern von Kreditorenkonten helfen, Kreditorenrechnungen effizienter zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="61606-113">This capability can help Accounts payable clerks and managers process vendor invoices more efficiently.</span></span> <span data-ttu-id="61606-114">Sie trägt auch dazu bei, die Fehler und Ineffizienzen zu reduzieren, die bei der manuellen Eingabe und Verarbeitung von Informationen auftreten können.</span><span class="sxs-lookup"><span data-stu-id="61606-114">It also helps reduce the errors and inefficiencies that can occur when information is manually entered and processed.</span></span>

<span data-ttu-id="61606-115">Die Automatisierungsprozesse können verwendet werden, um folgende Aufgaben auszuführen:</span><span class="sxs-lookup"><span data-stu-id="61606-115">The automation processes can be used to perform these tasks:</span></span>

- <span data-ttu-id="61606-116">Senden Sie importierte Rechnungen automatisch an das Workflowsystem.</span><span class="sxs-lookup"><span data-stu-id="61606-116">Automatically submit imported invoices to the workflow system.</span></span>
- <span data-ttu-id="61606-117">Gleichen Sie Produktzugänge mit ausstehenden Kreditorenrechnungspositionen ab.</span><span class="sxs-lookup"><span data-stu-id="61606-117">Match product receipts to pending vendor invoice lines.</span></span>
- <span data-ttu-id="61606-118">Simulieren Sie die Buchung, bevor eine Kreditorenrechnung gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="61606-118">Simulate posting before a vendor invoice is posted.</span></span>
- <span data-ttu-id="61606-119">Zeigen Sie schnell und effizient die Workflowhistorie an.</span><span class="sxs-lookup"><span data-stu-id="61606-119">Quickly and efficiently view workflow history.</span></span>
- <span data-ttu-id="61606-120">Zeigen Sie die Ergebnisse der Automatisierung der Verarbeitung von Kreditorenrechnungen an und analysieren Sie sie.</span><span class="sxs-lookup"><span data-stu-id="61606-120">View and analyze the results of automating vendor invoice processing.</span></span>

## <a name="vendor-invoice-automation--submit-imported-vendor-invoices-to-the-workflow-system"></a><span data-ttu-id="61606-121">Automatisierung von Kreditorenrechnungen – Senden von importierten Kreditorenrechnungen an das Workflowsystem</span><span class="sxs-lookup"><span data-stu-id="61606-121">Vendor invoice automation – Submit imported vendor invoices to the workflow system</span></span>

<span data-ttu-id="61606-122">Im Rahmen eines berührungslosen Rechnungsstellungsprozesses für Kreditorenkonten können Sie das System automatisch eine importierte Rechnung an das Workflowsystem senden lassen.</span><span class="sxs-lookup"><span data-stu-id="61606-122">As part of a touchless Accounts payable invoicing process, you can have the system automatically submit an imported invoice to the workflow system.</span></span> <span data-ttu-id="61606-123">Der Prozess wird im Hintergrund mit einer von Ihnen angegebenen Häufigkeit (entweder stündlich oder täglich) ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="61606-123">The process will run in the background, at a frequency that you specify (either hourly or daily).</span></span> <span data-ttu-id="61606-124">Um importierte Rechnungen automatisch an das Workflowsystem senden zu können, muss Ihr Prozess mit einer importierten Rechnung beginnen.</span><span class="sxs-lookup"><span data-stu-id="61606-124">The capability to automatically submit imported invoices to the workflow system requires that your process begin with an imported invoice.</span></span> <span data-ttu-id="61606-125">Um sicherzustellen, dass die Rechnung ohne manuellen Eingriff von Anfang bis Ende verarbeitet werden kann, muss eine automatisierte Buchungsaufgabe in der Workflowkonfiguration enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="61606-125">To ensure that the invoice can be processed from start to finish without manual intervention, an automated posting task must be included in the workflow configuration.</span></span>

<span data-ttu-id="61606-126">Rechnungen, die sich auf Bestellungen beziehen, sowie Rechnungen, die eine Beschaffungskategorie ohne Bestellung und nicht vorrätige Positionen enthalten, können automatisch an das Workflow-System gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="61606-126">'Invoices that are related to purchase orders (POs), and invoices that contain a non-PO procurement category and non-stocked lines, can automatically be submitted to the workflow system.</span></span> <span data-ttu-id="61606-127">Rechnungen, die manuell eingegeben werden, und Rechnungen, die über den Arbeitsbereich **Kreditorkooperationsrechnungen** erstellt werden, müssen manuell an das Workflowsystem gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="61606-127">Invoices that are manually entered and invoices that are created via the **Vendor collaboration invoicing** workspace must be manually submitted to the workflow system.</span></span>

<span data-ttu-id="61606-128">Die Automatisierungsfunktion stellt ein flexibles Framework bereit, mit dem Sie unternehmensspezifische Regeln für das Senden importierter Kreditorenrechnungen an das Workflowsystem und das Abgleichen gebuchter Produktzugangspositionen mit ausstehenden Kreditorenrechnungspositionen definieren können.</span><span class="sxs-lookup"><span data-stu-id="61606-128">The automation feature provides a flexible framework that lets you define company-specific rules for submitting imported vendor invoices to the workflow system and matching posted product receipt lines to pending vendor invoice lines.</span></span>

## <a name="vendor-invoice-automation--match-product-receipts-to-invoice-lines-that-have-a-three-way-matching-policy"></a><span data-ttu-id="61606-129">Kreditorenrechnungsautomatisierung – Abgleichen von gebuchten Produktzugängen mit Rechnungspositionen, für die eine dreiseitige Abgleichsrichtlinie gilt</span><span class="sxs-lookup"><span data-stu-id="61606-129">Vendor invoice automation – Match product receipts to invoice lines that have a three-way matching policy</span></span>

<span data-ttu-id="61606-130">Das System kann gebuchte Produktzugänge automatisch mit Rechnungspositionen abgleichen, für die eine dreiseitige Abgleichsrichtlinie definiert ist.</span><span class="sxs-lookup"><span data-stu-id="61606-130">The system can automatically match posted product receipts to invoice lines that a three-way matching policy is defined for.</span></span> <span data-ttu-id="61606-131">Der Prozess wird ausgeführt, bis die abgeglichene Produktzugangsmenge der Rechnungsmenge entspricht.</span><span class="sxs-lookup"><span data-stu-id="61606-131">The process will run until the matched product receipt quantity equals the invoice quantity.</span></span> <span data-ttu-id="61606-132">Im Rahmen dieses Prozesses können Sie für das System die maximale Anzahl der versuchten Abgleiche der Produktzugänge mit einer Rechnungsposition festlegen, bevor das System zu dem Schluss kommt, dass der Prozess fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="61606-132">As part of this process, you can specify the maximum number of times that the system should try to match product receipts to an invoice line before it concludes that the process failed.</span></span> <span data-ttu-id="61606-133">Der Prozess wird entweder stündlich oder täglich im Hintergrund ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="61606-133">The process will run in the background, either hourly or daily.</span></span> <span data-ttu-id="61606-134">Sie können den automatisierten Abgleichprozess im Rahmen des Prozesses zum Senden von Rechnungen an das Workflowsystem ausführen.</span><span class="sxs-lookup"><span data-stu-id="61606-134">You can run the automated matching process as part of the process for submitting invoices to the workflow system.</span></span> <span data-ttu-id="61606-135">Alternativ können Sie den Prozess auch als eigenständigen Prozess ausführen.</span><span class="sxs-lookup"><span data-stu-id="61606-135">Alternatively, you can run it as a standalone process.</span></span>

## <a name="vendor-invoice-automation--pre-validate-vendor-invoice-posting"></a><span data-ttu-id="61606-136">Kreditorenrechnungsautomatisierung – Überprüfen von Kreditorenrechnungen vor der Buchung</span><span class="sxs-lookup"><span data-stu-id="61606-136">Vendor invoice automation – Pre-validate vendor invoice posting</span></span>

<span data-ttu-id="61606-137">Die Buchungssimulation schließt die Prüfungsschritte ab, die während des Buchungsprozesses für Kreditorenrechnungen ausgeführt werden. Dabei werden jedoch keine Konten aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="61606-137">Posting simulation completes the validation steps that are done during the posting process for vendor invoices, but no accounts are updated.</span></span> <span data-ttu-id="61606-138">Um den Prozess auszuführen, können Sie auf der Seite **Ausstehende Kreditorenrechnungen** entweder eine einzelne Rechnung oder mehrere Rechnungen auswählen.</span><span class="sxs-lookup"><span data-stu-id="61606-138">To run the process, you can select either a single invoice or multiple invoices on the **Pending vendor invoices** page.</span></span>

## <a name="vendor-invoice-automation--enhanced-experience-for-viewing-workflow-historical-information-for-vendor-invoices"></a><span data-ttu-id="61606-139">Kreditorenrechnungsautomatisierung – verbesserte Erfahrung beim Anzeigen von Informationen aus der Workflowhistorie für Kreditorenrechnungen</span><span class="sxs-lookup"><span data-stu-id="61606-139">Vendor invoice automation – Enhanced experience for viewing workflow historical information for vendor invoices</span></span>

<span data-ttu-id="61606-140">Es wird eine übersichtliche Ansicht der Workflowhistorie der Kreditorenrechnung bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="61606-140">An easy-to-read view of vendor invoice workflow history is provided.</span></span> <span data-ttu-id="61606-141">Auf die Ansicht der Workflowhistorie kann direkt über die Kreditorenrechnung zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="61606-141">Vendor invoice workflow history can be accessed directly from the vendor invoice.</span></span> <span data-ttu-id="61606-142">Daher sind weniger Mausklicks erforderlich, um diese Informationen zu finden.</span><span class="sxs-lookup"><span data-stu-id="61606-142">Therefore, fewer clicks are required to find that information.</span></span>

## <a name="vendor-invoice-automation--analytics-and-metrics"></a><span data-ttu-id="61606-143">Kreditorenrechnungsautomatisierung – Analysen und Metriken</span><span class="sxs-lookup"><span data-stu-id="61606-143">Vendor invoice automation – Analytics and metrics</span></span>

<span data-ttu-id="61606-144">Der Arbeitsbereich **Kreditorenrechnungseintrag** ermöglicht die Fokussierung auf Kreditorenrechnungen, die den automatisierten Prozess nicht durchlaufen haben.</span><span class="sxs-lookup"><span data-stu-id="61606-144">The **Vendor invoice entry** workspace lets you focus on vendor invoices that didn't make it through the automated process.</span></span> <span data-ttu-id="61606-145">Kacheln im Arbeitsbereich enthalten Informationen zu Kreditorenrechnungen, die nicht erfolgreich an das Workflowsystem gesendet, importiert oder mit Produktzugängen abgeglichen wurden.</span><span class="sxs-lookup"><span data-stu-id="61606-145">Tiles on the workspace list information about vendor invoices that weren't successfully submitted to the workflow system, imported, or matched to product receipts.</span></span> <span data-ttu-id="61606-146">Darüber hinaus werden Microsoft Power BI-Metriken bereitgestellt, um den Mangern von Kreditorenkonten einen Einblick in die Effizienz der Automatisierung von Kreditorenrechnungen zu geben.</span><span class="sxs-lookup"><span data-stu-id="61606-146">Microsoft Power BI metrics are also provided to give Accounts payable managers insight into the efficiencies of vendor invoice automation.</span></span>