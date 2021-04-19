---
title: Dienst für Steuerberechnungen (Vorschau)
description: In diesem Thema werden der Gesamtumfang und die Funktionen des Steuerberechnungsdienstes erläutert.
author: wangchen
ms.date: 03/02/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 518d3fda7b97e55d23beea6a1ba0e50b44a7aa0e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818223"
---
# <a name="tax-calculation-service-preview"></a><span data-ttu-id="3d06f-103">Dienst für Steuerberechnungen (Vorschau)</span><span class="sxs-lookup"><span data-stu-id="3d06f-103">Tax calculation service (Preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="3d06f-104">Der Steuerberechnungsdienst ist ein hyperskalierbarer mandantenfähiger Dienst, mit dem die Global Tax Engine den Steuerermittlungs- und -berechnungsprozess automatisieren und vereinfachen kann.</span><span class="sxs-lookup"><span data-stu-id="3d06f-104">The tax calculation service is a hyper-scalable multitenant service that enables the global tax engine to automate and simplify the tax determination and calculation process.</span></span> <span data-ttu-id="3d06f-105">Das Steuermodul ist vollständig konfigurierbar.</span><span class="sxs-lookup"><span data-stu-id="3d06f-105">The tax engine is fully configurable.</span></span> <span data-ttu-id="3d06f-106">Zu den Elementen, die konfiguriert werden können, gehören unter anderem das steuerpflichtige Datenmodell, der Steuercode, die Steueranwendbarkeitsmatrix und die Steuerberechnungsformel.</span><span class="sxs-lookup"><span data-stu-id="3d06f-106">The elements that can be configured include, but aren't limited to, the taxable data model, tax code, tax applicability matrix, and tax calculation formula.</span></span> <span data-ttu-id="3d06f-107">Das Steuermodul läuft auf der Microsoft Azure-Hauptserviceplattform und bietet moderne Technologie und exponenzielle Skalierbarkeit.</span><span class="sxs-lookup"><span data-stu-id="3d06f-107">The tax engine runs on the Microsoft Azure core services platform, and offers modern technology and exponential scalability.</span></span>

<span data-ttu-id="3d06f-108">Der Steuerberechnungsdienst ist in Dynamics 365 Finance und Dynamics 365 Supply Chain Management integriert.</span><span class="sxs-lookup"><span data-stu-id="3d06f-108">The tax calculation service integrates with Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="3d06f-109">Schließlich wird er auch in Dynamics 365 Project Operations, Dynamics 365 Commerce und andere Anwendungen von Erstanbietern und Drittanbietern integriert.</span><span class="sxs-lookup"><span data-stu-id="3d06f-109">Eventually, it will also integrate with Dynamics 365 Project Operations, Dynamics 365 Commerce, and other first-party and third-party applications.</span></span>

<span data-ttu-id="3d06f-110">Der Steuerberechnungsdienst ist ein Microsoft-basiertes Steuermodul, das exponenzielle Skalierbarkeit bietet.</span><span class="sxs-lookup"><span data-stu-id="3d06f-110">The tax calculation service is a Microsoft-based tax engine that offers exponential scalability.</span></span> <span data-ttu-id="3d06f-111">Er kann bei der Ausführung folgender Aufgaben helfen:</span><span class="sxs-lookup"><span data-stu-id="3d06f-111">It can help you perform the following tasks:</span></span>

- <span data-ttu-id="3d06f-112">Konfigurieren Sie den Steuerberechnungsdienst über den Regulatory Configuration Service (RCS).</span><span class="sxs-lookup"><span data-stu-id="3d06f-112">Configure the tax calculation service through Regulatory Configuration Service (RCS).</span></span> <span data-ttu-id="3d06f-113">RCS ist eine erweiterte Version des Designers für elektronische Berichterstellung (ER) und als eigenständiger Dienst verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3d06f-113">RCS is an enhanced version of the Electronic reporting (ER) designer and is available as a standalone service.</span></span>
- <span data-ttu-id="3d06f-114">Konfigurieren Sie die Steuermatrix so, dass Steuercodes und Steuersätze automatisch ermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="3d06f-114">Configure the tax matrix to automatically determine tax codes and rates.</span></span>
- <span data-ttu-id="3d06f-115">Konfigurieren Sie die Steuermatrix so, dass die Steuerregistrierungsnummer automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="3d06f-115">Configure the tax matrix to automatically determine the tax registration number.</span></span>
- <span data-ttu-id="3d06f-116">Konfigurieren Sie den Steuerberechnungsdesigner so, dass Formeln und Bedingungen definiert werden.</span><span class="sxs-lookup"><span data-stu-id="3d06f-116">Configure the tax calculation designer to define formulas and conditions.</span></span>
- <span data-ttu-id="3d06f-117">Teilen Sie die Steuerermittlungs- und -berechnungslösung für verschiedene juristische Personen.</span><span class="sxs-lookup"><span data-stu-id="3d06f-117">Share the tax determination and calculation solution across legal entities.</span></span>

<span data-ttu-id="3d06f-118">Um den Steuerberechnungsdienst zu verwenden, installieren Sie das Steuerberechnungsdienst-Add-In aus Ihrem Projekt in Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="3d06f-118">To use the tax calculation service, install the tax calculation service add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="3d06f-119">Schließen Sie dann die Einrichtung in RCS ab und aktivieren Sie den Steuerberechnungsdienst in Finance und Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="3d06f-119">Then complete the setup in RCS, and enable the tax calculation service in Finance and Supply Chain Management.</span></span> <span data-ttu-id="3d06f-120">Weitere Informationen finden Sie unter [Erste Schritte mit dem Steuerdienst](https://go.microsoft.com/fwlink/?linkid=2138482).</span><span class="sxs-lookup"><span data-stu-id="3d06f-120">For more information, see [Get started with tax service](https://go.microsoft.com/fwlink/?linkid=2138482).</span></span>

## <a name="availability"></a><span data-ttu-id="3d06f-121">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="3d06f-121">Availability</span></span>

<span data-ttu-id="3d06f-122">Der Steuerberechnungsdienst ist nur in Sandbox-Umgebungen und für ausgewählte Kunden über ein öffentliches Vorschauprogramm verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3d06f-122">The tax calculation service is available only in sandbox environments and to selected customers, through a public preview program.</span></span> <span data-ttu-id="3d06f-123">Schließlich wird es für alle Kunden und in Produktionsumgebungen allgemein verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="3d06f-123">Eventually, it will become generally available to all customers and in production environments.</span></span>

<span data-ttu-id="3d06f-124">Neue Funktionen werden weiterhin im Steuerberechnungsdienst bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="3d06f-124">New features will continue to be delivered in the tax calculation service.</span></span> <span data-ttu-id="3d06f-125">Lesen Sie daher regelmäßig die aktuellste Dokumentation, um mehr über die Abdeckung und den Umfang der unterstützten Funktionen zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="3d06f-125">Therefore, be sure to check the most up-to-date documentation often to learn about the coverage and scope of supported features.</span></span>

<span data-ttu-id="3d06f-126">Der Steuerberechnungsdienst wird in den folgenden Azure-Regionen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="3d06f-126">The tax calculation service is deployed in the following Azure geographies.</span></span> <span data-ttu-id="3d06f-127">Er wird auch in weiteren Azure-Regionen bereitgestellt, je nach Kundenanforderungen:</span><span class="sxs-lookup"><span data-stu-id="3d06f-127">It will also be deployed to more Azure geographies, based on customer needs:</span></span>

- <span data-ttu-id="3d06f-128">Vereinigte Staaten</span><span class="sxs-lookup"><span data-stu-id="3d06f-128">United States</span></span>
- <span data-ttu-id="3d06f-129">Europa</span><span class="sxs-lookup"><span data-stu-id="3d06f-129">Europe</span></span>
- <span data-ttu-id="3d06f-130">Frankreich</span><span class="sxs-lookup"><span data-stu-id="3d06f-130">France</span></span>
- <span data-ttu-id="3d06f-131">Vereinigtes Königreich</span><span class="sxs-lookup"><span data-stu-id="3d06f-131">United Kingdom</span></span>

> [!NOTE]
> <span data-ttu-id="3d06f-132">Der Steuerberechnungsdienst unterstützt keine lokalen Bereitstellungen von Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="3d06f-132">The tax calculation service doesn't support on-premises deployments of Dynamics 365.</span></span> <span data-ttu-id="3d06f-133">Frühere Versionen wie Dynamics AX 2012 werden ebenfalls nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3d06f-133">It also doesn't support earlier versions, such as Dynamics AX 2012.</span></span>

## <a name="feature-highlights"></a><span data-ttu-id="3d06f-134">Besondere Funktionen</span><span class="sxs-lookup"><span data-stu-id="3d06f-134">Feature highlights</span></span>

- <span data-ttu-id="3d06f-135">Eine konfigurierbare Steuermatrix für die automatische Ermittlung und Berechnung der Steuer</span><span class="sxs-lookup"><span data-stu-id="3d06f-135">A configurable tax matrix to automatically determine and calculate tax</span></span>
- <span data-ttu-id="3d06f-136">Unterstützung für mehrere Mehrwertsteuer (MwSt.)-Erfassungsnummern</span><span class="sxs-lookup"><span data-stu-id="3d06f-136">Support for multiple value-added tax (VAT) registration numbers</span></span>
- <span data-ttu-id="3d06f-137">Umlagerungsauftragsunterstützung für Steuerermittlung und -berechnung</span><span class="sxs-lookup"><span data-stu-id="3d06f-137">Transfer order support for tax determination and calculation</span></span>
- <span data-ttu-id="3d06f-138">Umlagerungsauftragsunterstützung zur Ermittlung mehrerer Mehrwertsteuererfassungsnummern</span><span class="sxs-lookup"><span data-stu-id="3d06f-138">Transfer order support for determination of multiple VAT registration numbers</span></span>

## <a name="supported-transactions"></a><span data-ttu-id="3d06f-139">Unterstützte Transaktionen</span><span class="sxs-lookup"><span data-stu-id="3d06f-139">Supported transactions</span></span>

<span data-ttu-id="3d06f-140">Der Steuerberechnungsdienst kann nach juristischer Person und Transaktion aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="3d06f-140">The tax calculation service can be enabled by legal entity and transaction.</span></span> <span data-ttu-id="3d06f-141">Folgende Transaktionen werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="3d06f-141">The following transactions are supported:</span></span>

- <span data-ttu-id="3d06f-142">Verkaufsprozess</span><span class="sxs-lookup"><span data-stu-id="3d06f-142">Sales process</span></span>

    - <span data-ttu-id="3d06f-143">Verkaufsangebot</span><span class="sxs-lookup"><span data-stu-id="3d06f-143">Sales quotation</span></span>
    - <span data-ttu-id="3d06f-144">Auftrag</span><span class="sxs-lookup"><span data-stu-id="3d06f-144">Sales order</span></span>
    - <span data-ttu-id="3d06f-145">Bestätigung</span><span class="sxs-lookup"><span data-stu-id="3d06f-145">Confirmation</span></span>
    - <span data-ttu-id="3d06f-146">Kommissionierliste</span><span class="sxs-lookup"><span data-stu-id="3d06f-146">Picking list</span></span>
    - <span data-ttu-id="3d06f-147">Lieferschein</span><span class="sxs-lookup"><span data-stu-id="3d06f-147">Packing slip</span></span>
    - <span data-ttu-id="3d06f-148">Verkaufsrechnung</span><span class="sxs-lookup"><span data-stu-id="3d06f-148">Sales invoice</span></span>
    - <span data-ttu-id="3d06f-149">Gutschrift</span><span class="sxs-lookup"><span data-stu-id="3d06f-149">Credit note</span></span>
    - <span data-ttu-id="3d06f-150">Rücklieferung</span><span class="sxs-lookup"><span data-stu-id="3d06f-150">Return order</span></span>
    - <span data-ttu-id="3d06f-151">Sonstige Kopfgebühren</span><span class="sxs-lookup"><span data-stu-id="3d06f-151">Header miscellaneous charge</span></span>
    - <span data-ttu-id="3d06f-152">Sonstige Positionsbelastungen</span><span class="sxs-lookup"><span data-stu-id="3d06f-152">Line miscellaneous charge</span></span>

- <span data-ttu-id="3d06f-153">Kaufprozess</span><span class="sxs-lookup"><span data-stu-id="3d06f-153">Purchase process</span></span>

    - <span data-ttu-id="3d06f-154">Bestellung</span><span class="sxs-lookup"><span data-stu-id="3d06f-154">Purchase order</span></span>
    - <span data-ttu-id="3d06f-155">Bestätigung</span><span class="sxs-lookup"><span data-stu-id="3d06f-155">Confirmation</span></span>
    - <span data-ttu-id="3d06f-156">Zugangsliste</span><span class="sxs-lookup"><span data-stu-id="3d06f-156">Receipts list</span></span>
    - <span data-ttu-id="3d06f-157">Produktzugang</span><span class="sxs-lookup"><span data-stu-id="3d06f-157">Product receipt</span></span>
    - <span data-ttu-id="3d06f-158">Einkaufsrechnung</span><span class="sxs-lookup"><span data-stu-id="3d06f-158">Purchase invoice</span></span>
    - <span data-ttu-id="3d06f-159">Sonstige Kopfgebühren</span><span class="sxs-lookup"><span data-stu-id="3d06f-159">Header miscellaneous charge</span></span>
    - <span data-ttu-id="3d06f-160">Sonstige Positionsbelastungen</span><span class="sxs-lookup"><span data-stu-id="3d06f-160">Line miscellaneous charge</span></span>
    - <span data-ttu-id="3d06f-161">Gutschrift</span><span class="sxs-lookup"><span data-stu-id="3d06f-161">Credit note</span></span>
    - <span data-ttu-id="3d06f-162">Rücklieferung</span><span class="sxs-lookup"><span data-stu-id="3d06f-162">Return order</span></span>
    - <span data-ttu-id="3d06f-163">Bestellanforderung</span><span class="sxs-lookup"><span data-stu-id="3d06f-163">Purchase requisition</span></span>
    - <span data-ttu-id="3d06f-164">Sonstige Belastung pro Bestellanforderungsposition</span><span class="sxs-lookup"><span data-stu-id="3d06f-164">Purchase requisition line miscellaneous charge</span></span>
    - <span data-ttu-id="3d06f-165">Angebotsanforderung</span><span class="sxs-lookup"><span data-stu-id="3d06f-165">Request for quotation</span></span>
    - <span data-ttu-id="3d06f-166">Sonstige Kopfgebühr für Angebotsanforderung</span><span class="sxs-lookup"><span data-stu-id="3d06f-166">Request for quotation header miscellaneous charge</span></span>
    - <span data-ttu-id="3d06f-167">Sonstige Belastung pro Angebotsanforderungsposition</span><span class="sxs-lookup"><span data-stu-id="3d06f-167">Request for quotation line miscellaneous charge</span></span>

- <span data-ttu-id="3d06f-168">Bestandsprozess</span><span class="sxs-lookup"><span data-stu-id="3d06f-168">Inventory process</span></span>

    - <span data-ttu-id="3d06f-169">Umlagerungsauftrag – versenden</span><span class="sxs-lookup"><span data-stu-id="3d06f-169">Transfer order – ship</span></span>
    - <span data-ttu-id="3d06f-170">Umlagerungsauftrag – empfangen</span><span class="sxs-lookup"><span data-stu-id="3d06f-170">Transfer order – receive</span></span>

## <a name="related-resources"></a><span data-ttu-id="3d06f-171">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="3d06f-171">Related resources</span></span>

[<span data-ttu-id="3d06f-172">Erste Schritte mit dem Steuerdienst</span><span class="sxs-lookup"><span data-stu-id="3d06f-172">Get started with tax service</span></span>](https://go.microsoft.com/fwlink/?linkid=2138482)

[<span data-ttu-id="3d06f-173">Mehrere Mehrwertsteuererfassungsnummern</span><span class="sxs-lookup"><span data-stu-id="3d06f-173">Multiple VAT registration number</span></span>](https://go.microsoft.com/fwlink/?linkid=2153387)

[<span data-ttu-id="3d06f-174">Unterstützung für Steuerfunktionen für Umlagerungsaufträge</span><span class="sxs-lookup"><span data-stu-id="3d06f-174">Tax feature support for transfer order</span></span>](https://go.microsoft.com/fwlink/?linkid=2153388)

[<span data-ttu-id="3d06f-175">So erstellen Sie eine Erweiterung im Steuerdienst</span><span class="sxs-lookup"><span data-stu-id="3d06f-175">How to build extension in tax service</span></span>](https://go.microsoft.com/fwlink/?linkid=2138483)
