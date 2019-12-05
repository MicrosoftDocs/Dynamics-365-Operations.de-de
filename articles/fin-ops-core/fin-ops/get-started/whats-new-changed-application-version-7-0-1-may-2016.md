---
title: Neuheiten und Änderungen in Dynamics AX 7.0.1 (Mai 2016)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics AX 7.0.1 entweder neu oder geändert sind. Diese Version wurde im Mai 2016 veröffentlicht und hat die Build-Nummer 7.0.1265.23014.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.custom: 91213
ms.assetid: f0bbc78f-87fc-40e9-b46a-6655893f69be
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 715e0f8d08c6abbde35eb917cddc4ecf4b7b67ed
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811455"
---
# <a name="whats-new-or-changed-in-dynamics-ax-application-version-701-may-2016"></a><span data-ttu-id="0f5da-104">Neuheiten und Änderungen in Dynamics AX 7.0.1 (Mai 2016)</span><span class="sxs-lookup"><span data-stu-id="0f5da-104">What's new or changed in Dynamics AX application version 7.0.1 (May 2016)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0f5da-105">In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics AX 7.0.1 entweder neu oder geändert sind.</span><span class="sxs-lookup"><span data-stu-id="0f5da-105">This article describes features that are either new or changed in Microsoft Dynamics AX application version 7.0.1.</span></span> <span data-ttu-id="0f5da-106">Diese Version wurde im Mai 2016 veröffentlicht und hat die Build-Nummer 7.0.1265.23014.</span><span class="sxs-lookup"><span data-stu-id="0f5da-106">This version was released in May 2016 and has a build number of 7.0.1265.23014.</span></span>

## <a name="electronic-reporting-er"></a><span data-ttu-id="0f5da-107">Elektronische Berichterstellung (ER, Elektronic Reporting)</span><span class="sxs-lookup"><span data-stu-id="0f5da-107">Electronic reporting (ER)</span></span>

| <span data-ttu-id="0f5da-108">Wie können Sie vorgehen?</span><span class="sxs-lookup"><span data-stu-id="0f5da-108">What can you do?</span></span> | <span data-ttu-id="0f5da-109">Warum ist dieses wichtig?</span><span class="sxs-lookup"><span data-stu-id="0f5da-109">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="0f5da-110">Konfigurieren Sie ein Laufzeit-Dialogfeld für die elektronische Berichterstellung, über das der Benutzer die gewünschten Finanzdimensionen auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="0f5da-110">Configure a run-time dialog box for designing Electronic reporting (ER) reports, so that users can select the financial dimensions that they want.</span></span> | <span data-ttu-id="0f5da-111">Zur Laufzeit können die Benutzer im Dialogfeld für die Ausführung eines ER-Berichts mehrere Finanzdimensionen auswählen.</span><span class="sxs-lookup"><span data-stu-id="0f5da-111">At run time, in the dialog box for running an ER report, users can select multiple financial dimensions.</span></span> <span data-ttu-id="0f5da-112">Die Details der ausgewählten Finanzdimensionen werden im generierten elektronischen Dokument angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0f5da-112">The details of the selected financial dimensions will be displayed in the electronic document that is generated.</span></span> |
| <span data-ttu-id="0f5da-113">Konfigurieren des Zugriffs auf mehrere Finanzdimensionen beim Entwurf eines ER-Berichts über eine einzelne Zuordnung zur gewünschte Datenquelle.</span><span class="sxs-lookup"><span data-stu-id="0f5da-113">Configure access to multiple financial dimensions during the design of an ER report, via a single mapping to the desired data source.</span></span> | <span data-ttu-id="0f5da-114">Die selbe ER Berichtskonfiguration kann verwendet werden, um elektronische Dokumente zu generieren, die Buchungsdaten mit Details zu Finanzdimensionen anzeigen – und zwar unabhängig von der Anzahl der Finanzdimensionen die vom Benutzer ausgewählt oder für die aktuelle juristische Person oder Instanz konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="0f5da-114">The same ER report configuration can be used to generate electronic documents that present transactional data together with details of financial dimensions, regardless of the number of financial dimensions that are either selected by the user or configured for the current legal entity or instance.</span></span> |
| <span data-ttu-id="0f5da-115">Konfigurieren eines Er-Berichts zur Eingabe von Daten in dynamisch generierten Spalten eines elektronischen Dokuments, dass im OPENXML-Arbeitsblattformat erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="0f5da-115">Configure an ER report to enter data in dynamically generated columns of an electronic document that is created in OPENXML worksheet format.</span></span> | <span data-ttu-id="0f5da-116">Ein ER-Bericht kann über horizontal replizierte spalten Daten in einem generierten OPENXML-Arbeitsblatt eingeben.</span><span class="sxs-lookup"><span data-stu-id="0f5da-116">An ER report can enter data in an OPENXML worksheet that is generated, via horizontally replicating columns.</span></span> <span data-ttu-id="0f5da-117">Daher kann eine ER Berichtskonfiguration zur Generierung von elektronischen Dokumenten genutzt werden, die unterschiedlich viele dynamisch generierte Spalten haben.</span><span class="sxs-lookup"><span data-stu-id="0f5da-117">Therefore, the same ER report configuration can be reused to generate electronic documents that have a different number of dynamically generated columns.</span></span> |
| <span data-ttu-id="0f5da-118">Konfigurieren von ER-Zielen für die Umleitung des Ausgabeergebnisses eines Formats an ein bestimmtes Ziel: Datei, E-Mail und Archivierung (Microsoft SharePoint-Ordner oder Microsoft Azure Storage).</span><span class="sxs-lookup"><span data-stu-id="0f5da-118">Configure ER destinations so that the output result of a format is directed to specific destination: file, email, or archive (Microsoft SharePoint folder or Microsoft Azure Storage).</span></span> | <span data-ttu-id="0f5da-119">Zuvor wurde bei der Ausführung einer ER-Konfiguration ein Meldungsfeld angezeigt, bei dem eine Benutzeraktion zum Speichern oder Öffnen einer Datei erforderlich war.</span><span class="sxs-lookup"><span data-stu-id="0f5da-119">Previously, when you ran an ER configuration, a message box appeared that required user action to save or open a file.</span></span> <span data-ttu-id="0f5da-120">Sie können nun ein separates Ziel für jede Formatkonfiguration und für jede Ausgabenkomponente (einen Ordner oder eine Datei) vorkonfigurieren.</span><span class="sxs-lookup"><span data-stu-id="0f5da-120">You can now pre-configure a destination for each format configuration and for each output component (a folder or a file) separately.</span></span> <span data-ttu-id="0f5da-121">Benutzer, die entsprechende Zugriffsrechte haben, können auch Zieleinstellungen zur Laufzeit ändern.</span><span class="sxs-lookup"><span data-stu-id="0f5da-121">Users who have appropriate access rights can also modify destination settings at run time.</span></span> |

## <a name="pos--microsoft-dynamics-ax-retail"></a><span data-ttu-id="0f5da-122">POS – Microsoft Dynamics AX Retail</span><span class="sxs-lookup"><span data-stu-id="0f5da-122">POS – Microsoft Dynamics AX Retail</span></span>

| <span data-ttu-id="0f5da-123">Wie können Sie vorgehen?</span><span class="sxs-lookup"><span data-stu-id="0f5da-123">What can you do?</span></span> | <span data-ttu-id="0f5da-124">Warum ist dieses wichtig?</span><span class="sxs-lookup"><span data-stu-id="0f5da-124">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="0f5da-125">Verwenden des Google Chrome-Browsers.</span><span class="sxs-lookup"><span data-stu-id="0f5da-125">Use the Google Chrome browser.</span></span> | <span data-ttu-id="0f5da-126">Einzelhändler können nun Cloud POS über den Chrome-Browser nutzen und alle Funktionen verwenden, die in der Microsoft Edge und Internet Explorer über Cloud POS verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="0f5da-126">Retailers can now start Cloud POS from the Chrome browser, and can experience all the functionality that is available in the Microsoft Edge and Internet Explorer version of Cloud POS.</span></span> |

## <a name="financial-reporting"></a><span data-ttu-id="0f5da-127">Finanzberichterstellung</span><span class="sxs-lookup"><span data-stu-id="0f5da-127">Financial reporting</span></span>

| <span data-ttu-id="0f5da-128">Wie können Sie vorgehen?</span><span class="sxs-lookup"><span data-stu-id="0f5da-128">What can you do?</span></span> | <span data-ttu-id="0f5da-129">Warum ist dieses wichtig?</span><span class="sxs-lookup"><span data-stu-id="0f5da-129">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="0f5da-130">Neu Erstellen der Finanzberichterstellungs-Data Mart-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="0f5da-130">Rebuild the Financial reporting data mart.</span></span> | <span data-ttu-id="0f5da-131">Wenn Sie Dynamics AX-Datenbanken zwischen Umgebungen verschieben oder andere invasive Änderungen an der Umgebung vornehmen, muss möglicherweise die Finanzberichterstellungsdatenbank neu erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="0f5da-131">When you move Dynamics AX databases between environments or make other invasive changes to the environment, the Financial reporting database might have to be rebuilt.</span></span> <span data-ttu-id="0f5da-132">Ein Windows PowerShell-Skript wird nun bereitgestellt, mit dem die Datenbank für Sie neu erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="0f5da-132">A Windows PowerShell script is now provided to rebuild the database for you.</span></span> |
| <span data-ttu-id="0f5da-133">Sie können nicht mehr ungültige Designer Berichtsoptionen auswählen.</span><span class="sxs-lookup"><span data-stu-id="0f5da-133">You can no longer select report designer options that aren't valid.</span></span> | <span data-ttu-id="0f5da-134">Mehrere Designer-Optionen, die in den veröffentlichten Versionen von Management Reporter verwendeten wurden, gelten nicht für diese Version von Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="0f5da-134">Several report designer options that were used in the in-market versions of Management reporter don't apply to this version of Dynamics AX.</span></span> <span data-ttu-id="0f5da-135">Diese Optionen betrafen das Finanzberichtsdesign, die Ausgabe und das Verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="0f5da-135">These options were related to financial report design, output, and linking.</span></span> <span data-ttu-id="0f5da-136">Diese Optionen wurden aus dem Finanzberichtsdesigner entfernt, um Benutzerfehler zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="0f5da-136">These options have been removed from the financial report designer to prevent user errors.</span></span> |

## <a name="financial-management"></a><span data-ttu-id="0f5da-137">Finanzverwaltung</span><span class="sxs-lookup"><span data-stu-id="0f5da-137">Financial management</span></span>

| <span data-ttu-id="0f5da-138">Wie können Sie vorgehen?</span><span class="sxs-lookup"><span data-stu-id="0f5da-138">What can you do?</span></span> | <span data-ttu-id="0f5da-139">Warum ist dieses wichtig?</span><span class="sxs-lookup"><span data-stu-id="0f5da-139">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="0f5da-140">Generieren positiver Lohndateien für Kreditorenkontozahlungen.</span><span class="sxs-lookup"><span data-stu-id="0f5da-140">Generate positive pay files for accounts payable payments.</span></span> | <span data-ttu-id="0f5da-141">Um Scheckbetrug zu verhindern können positive Lohndateien generiert werden.</span><span class="sxs-lookup"><span data-stu-id="0f5da-141">Positive pay files can be generated to help prevent check fraud.</span></span> |

## <a name="warehouse-and-production"></a><span data-ttu-id="0f5da-142">Lagerort und Produktion</span><span class="sxs-lookup"><span data-stu-id="0f5da-142">Warehouse and production</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0f5da-143">Wie können Sie vorgehen?</span><span class="sxs-lookup"><span data-stu-id="0f5da-143">What can you do?</span></span></th>
<th><span data-ttu-id="0f5da-144">Warum ist dieses wichtig?</span><span class="sxs-lookup"><span data-stu-id="0f5da-144">Why is this important?</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0f5da-145">Definieren Sie eine Lagerortrichtlinie, die die Erstellung der Arbeit für eine Reihe von Produkten an bestimmten Lagerorten steuert.</span><span class="sxs-lookup"><span data-stu-id="0f5da-145">Define a warehouse work policy that controls the creation of work for a set of products at specific locations.</span></span></td>
<td><span data-ttu-id="0f5da-146">Lagerortprozesse enthalten nicht immer Arbeit.</span><span class="sxs-lookup"><span data-stu-id="0f5da-146">Warehouse processes don't always include work.</span></span> <span data-ttu-id="0f5da-147">Wenn Sie die neue Lagerortarbeitsrichtlinie verwenden, können Sie die Erstellung von Arbeit für Rohmaterialentnahme sowie die Einlagerung fertiger Waren für einen Satz von Produkten an bestimmten Lagerplätzen verhindern.</span><span class="sxs-lookup"><span data-stu-id="0f5da-147">By using the new warehouse work policy, you can prevent work from being created for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f5da-148">Geben Sie an, dass ein Warenausgangslagerplatz nicht über Ladungsträger gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="0f5da-148">Specify that a production output location isn't license plate–controlled.</span></span></td>
<td><span data-ttu-id="0f5da-149">Sie können nun festlegen, dass ein Produktausgangslagerplatz nicht über Ladungsträger gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="0f5da-149">You can now specify that a product output location isn't license plate–controlled.</span></span> <span data-ttu-id="0f5da-150">Diese Funktion eignet sich beispielsweise, wenn Upstream-Fertigungsauftrag Artikel direkt an einen Lagerort als fertiggestellt meldet der als Produktionseingangslagerort für einen Downstream-Produktionsauftrag agiert.</span><span class="sxs-lookup"><span data-stu-id="0f5da-150">For example, this feature is useful when an upstream production order reports items as finished directly to a location that acts as production input location for a downstream production order.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f5da-151">Unterstützung für Stücklisten, die Artikel mit unterschiedlichen Produktdimensionen desselben Artikels umfassen.</span><span class="sxs-lookup"><span data-stu-id="0f5da-151">Support BOMs that include items with different product dimensions of the same item.</span></span></td>
<td><span data-ttu-id="0f5da-152">Wenn Sie eine oder mehrere der Produktdimensionen in der Produktion verwenden, treten Situationen auf, in denen Sie einen Artikel auf Basis einer Variante des gleichen Artikels produzieren möchten.</span><span class="sxs-lookup"><span data-stu-id="0f5da-152">When using one or multiple of the product dimensions in production, you can have situations where you would like to produce an item, based on a different variant of the same item.</span></span> <span data-ttu-id="0f5da-153">Weitere Informationen finden Sie <a href="https://blogs.msdn.microsoft.com/axmfg/2015/12/22/support-for-boms-that-includes-items-with-different-product-dimensions-of-the-same-item/">in diesem Blog</a>.</span><span class="sxs-lookup"><span data-stu-id="0f5da-153">For more information, see <a href="https://blogs.msdn.microsoft.com/axmfg/2015/12/22/support-for-boms-that-includes-items-with-different-product-dimensions-of-the-same-item/">this blog</a>.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f5da-154">Fertigungsaufträge mit Zirkularitätsstrukturen auf der ersten Ebene ihrer Stücklisten sind von der Kalkulation der Materialressourcenplanung auf Stücklistenebene ausgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="0f5da-154">Production orders with circular structures at the first level of their BOMs are excluded from BOM level calculation for material resource planning.</span></span></td>
<td><span data-ttu-id="0f5da-155">Es ist nicht möglich, korrekte Stücklistenebenen zu Produktvarianten für Fertigungsaufträge zuzuweisen die einen in der Stücklistenhierarchie einen Verweis auf sich selbst darstellen.</span><span class="sxs-lookup"><span data-stu-id="0f5da-155">It is not possible to assign correct BOM levels to product variants for production orders that cause circularity in the BOM hierarchy.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f5da-156">Berechnen separater Stücklistenebenen für die Materialressourcenplanung und Kostenkalkulation:</span><span class="sxs-lookup"><span data-stu-id="0f5da-156">Calculate separate BOM levels for material resource planning and cost calculation:</span></span>
<ul>
<li><span data-ttu-id="0f5da-157">Für die Materialressourcenplanung werden Stücklistenebenen in der neuen Tabelle <strong>ReqItemLevel</strong> kalkuliert.</span><span class="sxs-lookup"><span data-stu-id="0f5da-157">For material resource planning, BOM levels are calculated in the new <strong>ReqItemLevel</strong> table.</span></span> <span data-ttu-id="0f5da-158">Beendete Fertigungsaufträge werden bei der Berechnung ignoriert.</span><span class="sxs-lookup"><span data-stu-id="0f5da-158">Ended production orders are ignored in the calculation.</span></span></li>
<li><span data-ttu-id="0f5da-159">Für die Berechnung der Produktionskosten werden Stücklistenebenen in der Tabelle <strong>InventTable</strong> berechnet.</span><span class="sxs-lookup"><span data-stu-id="0f5da-159">For production cost calculation, BOM levels are calculated in the <strong>InventTable</strong>.</span></span> <span data-ttu-id="0f5da-160">Beendete Fertigungsaufträge werden bei der Berechnung einbezogen.</span><span class="sxs-lookup"><span data-stu-id="0f5da-160">Ended production orders are included in the calculation.</span></span></li>
</ul>
</td>
<td>
<ul>
<li><span data-ttu-id="0f5da-161">Bei der Ausführung der Materialressourcenplanung (beispielsweise die Produktprogrammplanplanung und -auflösung) müssen nur Stücklistenebenen neu berechnet werden, die zur Materialressourcenplanung genutzt werden.</span><span class="sxs-lookup"><span data-stu-id="0f5da-161">When running material resource planning, for example, master planning plan scheduling and explosion, only BOM levels used for material resource planning need to be recalculated.</span></span> <span data-ttu-id="0f5da-162">Es ist also nicht erforderlich die zur Produktionskostenberechnung verwendeten Stücklistenebenen neu zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="0f5da-162">In other words, there is no need to calculate BOM levels used for production costing calculation.</span></span></li>
<li><span data-ttu-id="0f5da-163">Bei der Ausführung von Nachkalkulationsvorgängen (beispielsweise der Lagerabschluss) müssen nur zur Produktionskostenkalkulation verwendete Stücklistenebenen neu berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="0f5da-163">When running costing operations, for example, inventory closing, only BOM levels used for production costing calculation need to be recalculated.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="0f5da-164">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0f5da-164">Additional resources</span></span>

[<span data-ttu-id="0f5da-165">Neuerungen oder Änderungen in Finance and Operations – Startseite</span><span class="sxs-lookup"><span data-stu-id="0f5da-165">What's new or changed in Finance and Operations home page</span></span>](whats-new-changed.md)

[<span data-ttu-id="0f5da-166">Neue oder aktualisierte Aufgabenleitfäden (Mai 2016)</span><span class="sxs-lookup"><span data-stu-id="0f5da-166">New or updated task guides (May 2016)</span></span>](new-updated-task-guides-available-may-2016.md)
