---
title: Steuerberechnung (Vorschau)
description: In diesem Thema werden der Gesamtumfang und die Funktionen der Steuerberechnung erläutert.
author: wangchen
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: b26472e195d9bdbba340a118c106de1a4dc79b34
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021931"
---
# <a name="tax-calculation-preview"></a><span data-ttu-id="9da69-103">Steuerberechnung (Vorschau)</span><span class="sxs-lookup"><span data-stu-id="9da69-103">Tax Calculation (Preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="9da69-104">Die Steuerberechnung ist ein hyperskalierbarer mandantenfähiger Dienst, mit dem die Global Tax Engine den Steuerermittlungs- und -berechnungsprozess automatisieren und vereinfachen kann.</span><span class="sxs-lookup"><span data-stu-id="9da69-104">Tax Calculation is a hyper-scalable multitenant service that enables the global tax engine to automate and simplify the tax determination and calculation process.</span></span> <span data-ttu-id="9da69-105">Das Steuermodul ist vollständig konfigurierbar.</span><span class="sxs-lookup"><span data-stu-id="9da69-105">The tax engine is fully configurable.</span></span> <span data-ttu-id="9da69-106">Zu den Elementen, die konfiguriert werden können, gehören unter anderem das steuerpflichtige Datenmodell, der Steuercode, die Steueranwendbarkeitsmatrix und die Steuerberechnungsformel.</span><span class="sxs-lookup"><span data-stu-id="9da69-106">The elements that can be configured include, but aren't limited to, the taxable data model, tax code, tax applicability matrix, and tax calculation formula.</span></span> <span data-ttu-id="9da69-107">Das Steuermodul läuft auf der Microsoft Azure-Hauptserviceplattform und bietet moderne Technologie und exponenzielle Skalierbarkeit.</span><span class="sxs-lookup"><span data-stu-id="9da69-107">The tax engine runs on the Microsoft Azure core services platform, and offers modern technology and exponential scalability.</span></span>

<span data-ttu-id="9da69-108">Die Steuerberechnung ist in Dynamics 365 Finance und Dynamics 365 Supply Chain Management integriert.</span><span class="sxs-lookup"><span data-stu-id="9da69-108">Tax Calculation integrates with Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="9da69-109">Schließlich wird er auch in Dynamics 365 Project Operations, Dynamics 365 Commerce und andere Anwendungen von Erstanbietern und Drittanbietern integriert.</span><span class="sxs-lookup"><span data-stu-id="9da69-109">Eventually, it will also integrate with Dynamics 365 Project Operations, Dynamics 365 Commerce, and other first-party and third-party applications.</span></span>

<span data-ttu-id="9da69-110">Die Steuerberechnung ist ein Microsoft-basiertes Steuermodul, das exponenzielle Skalierbarkeit bietet.</span><span class="sxs-lookup"><span data-stu-id="9da69-110">Tax Calculation is a microservice-based tax engine that offers exponential scalability.</span></span> <span data-ttu-id="9da69-111">Er kann bei der Ausführung folgender Aufgaben helfen:</span><span class="sxs-lookup"><span data-stu-id="9da69-111">It can help you perform the following tasks:</span></span>

- <span data-ttu-id="9da69-112">Konfigurieren Sie die Steuerberechnung über den Regulatory Configuration Service (RCS).</span><span class="sxs-lookup"><span data-stu-id="9da69-112">Configure Tax Calculation through Regulatory Configuration Service (RCS).</span></span> <span data-ttu-id="9da69-113">RCS ist eine erweiterte Version des Designers für elektronische Berichterstellung (ER) und als eigenständiger Dienst verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9da69-113">RCS is an enhanced version of the Electronic reporting (ER) designer and is available as a standalone service.</span></span>
- <span data-ttu-id="9da69-114">Konfigurieren Sie die Steuermatrix so, dass Steuercodes und Steuersätze automatisch ermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="9da69-114">Configure the tax matrix to automatically determine tax codes and rates.</span></span>
- <span data-ttu-id="9da69-115">Konfigurieren Sie die Steuermatrix so, dass die Steuerregistrierungsnummer automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="9da69-115">Configure the tax matrix to automatically determine the tax registration number.</span></span>
- <span data-ttu-id="9da69-116">Konfigurieren Sie den Steuerberechnungsdesigner so, dass Formeln und Bedingungen definiert werden.</span><span class="sxs-lookup"><span data-stu-id="9da69-116">Configure the tax calculation designer to define formulas and conditions.</span></span>
- <span data-ttu-id="9da69-117">Teilen Sie die Steuerermittlungs- und -berechnungslösung für verschiedene juristische Personen.</span><span class="sxs-lookup"><span data-stu-id="9da69-117">Share the tax determination and calculation solution across legal entities.</span></span>

<span data-ttu-id="9da69-118">Um den Steuerberechnungsdienst zu verwenden, installieren Sie das Steuerberechnungsdienst-Add-In aus Ihrem Projekt in Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="9da69-118">To use the tax calculation service, install the tax calculation service add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="9da69-119">Schließen Sie dann die Einrichtung in RCS ab und aktivieren Sie den Steuerberechnungsdienst in Finance und Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="9da69-119">Then complete the setup in RCS, and enable the tax calculation service in Finance and Supply Chain Management.</span></span> <span data-ttu-id="9da69-120">Weitere Informationen finden Sie unter [Erste Schritte mit dem Steuerdienst](./global-get-started-with-tax-calculation-service.md).</span><span class="sxs-lookup"><span data-stu-id="9da69-120">For more information, see [Get started with tax service](./global-get-started-with-tax-calculation-service.md).</span></span>

## <a name="availability"></a><span data-ttu-id="9da69-121">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="9da69-121">Availability</span></span>

<span data-ttu-id="9da69-122">Die Steuerberechnung ist nur in Sandbox-Umgebungen und für ausgewählte Kunden über ein öffentliches Vorschauprogramm verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9da69-122">Tax Calculation is available only in sandbox environments and to selected customers, through a public preview program.</span></span> <span data-ttu-id="9da69-123">Schließlich wird es für alle Kunden und in Produktionsumgebungen allgemein verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="9da69-123">Eventually, it will become generally available to all customers and in production environments.</span></span>

<span data-ttu-id="9da69-124">Da laufend neue Funktionen bereitgestellt werden, lesen Sie regelmäßig die aktuellste Dokumentation, um mehr über die Abdeckung und den Umfang der unterstützten Funktionen zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="9da69-124">New features will continue to be delivered, so be sure to check the most up-to-date documentation often to learn about the coverage and scope of supported features.</span></span>

<span data-ttu-id="9da69-125">Die Steuerberechnung wird in den folgenden Azure-Regionen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="9da69-125">Tax Calculation is deployed in the following Azure geographies.</span></span> <span data-ttu-id="9da69-126">Er wird auch in weiteren Azure-Regionen bereitgestellt, je nach Kundenanforderungen:</span><span class="sxs-lookup"><span data-stu-id="9da69-126">It will also be deployed to more Azure geographies, based on customer needs:</span></span>

- <span data-ttu-id="9da69-127">Vereinigte Staaten</span><span class="sxs-lookup"><span data-stu-id="9da69-127">United States</span></span>
- <span data-ttu-id="9da69-128">Europa</span><span class="sxs-lookup"><span data-stu-id="9da69-128">Europe</span></span>

> [!NOTE]
> <span data-ttu-id="9da69-129">Die Steuerberechnung unterstützt keine lokalen Bereitstellungen von Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="9da69-129">Tax Calculation doesn't support on-premises deployments of Dynamics 365.</span></span> <span data-ttu-id="9da69-130">Frühere Versionen wie Dynamics AX 2012 werden ebenfalls nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9da69-130">It also doesn't support earlier versions, such as Dynamics AX 2012.</span></span>

## <a name="feature-highlights"></a><span data-ttu-id="9da69-131">Besondere Funktionen</span><span class="sxs-lookup"><span data-stu-id="9da69-131">Feature highlights</span></span>

- <span data-ttu-id="9da69-132">Eine konfigurierbare Steuermatrix für die automatische Ermittlung und Berechnung der Steuer</span><span class="sxs-lookup"><span data-stu-id="9da69-132">A configurable tax matrix to automatically determine and calculate tax</span></span>
- <span data-ttu-id="9da69-133">Unterstützung für mehrere Steuernummern</span><span class="sxs-lookup"><span data-stu-id="9da69-133">Support for multiple tax registration numbers</span></span>
- <span data-ttu-id="9da69-134">Umlagerungsauftragsunterstützung für Steuerermittlung und -berechnung</span><span class="sxs-lookup"><span data-stu-id="9da69-134">Transfer order support for tax determination and calculation</span></span>
- <span data-ttu-id="9da69-135">Umlagerungsauftragsunterstützung zur Ermittlung mehrerer Steuernummern</span><span class="sxs-lookup"><span data-stu-id="9da69-135">Transfer order support for determination of multiple tax registration numbers</span></span>

## <a name="supported-transactions"></a><span data-ttu-id="9da69-136">Unterstützte Transaktionen</span><span class="sxs-lookup"><span data-stu-id="9da69-136">Supported transactions</span></span>

<span data-ttu-id="9da69-137">Die Steuerberechnung kann nach juristischer Person und Transaktion aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="9da69-137">Tax Calculation can be enabled by legal entity and transaction.</span></span> <span data-ttu-id="9da69-138">Folgende Transaktionen werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="9da69-138">The following transactions are supported:</span></span>

- <span data-ttu-id="9da69-139">Verkaufsprozess</span><span class="sxs-lookup"><span data-stu-id="9da69-139">Sales process</span></span>

    - <span data-ttu-id="9da69-140">Verkaufsangebot</span><span class="sxs-lookup"><span data-stu-id="9da69-140">Sales quotation</span></span>
    - <span data-ttu-id="9da69-141">Auftrag</span><span class="sxs-lookup"><span data-stu-id="9da69-141">Sales order</span></span>
    - <span data-ttu-id="9da69-142">Bestätigung</span><span class="sxs-lookup"><span data-stu-id="9da69-142">Confirmation</span></span>
    - <span data-ttu-id="9da69-143">Kommissionierliste</span><span class="sxs-lookup"><span data-stu-id="9da69-143">Picking list</span></span>
    - <span data-ttu-id="9da69-144">Lieferschein</span><span class="sxs-lookup"><span data-stu-id="9da69-144">Packing slip</span></span>
    - <span data-ttu-id="9da69-145">Verkaufsrechnung</span><span class="sxs-lookup"><span data-stu-id="9da69-145">Sales invoice</span></span>
    - <span data-ttu-id="9da69-146">Gutschrift</span><span class="sxs-lookup"><span data-stu-id="9da69-146">Credit note</span></span>
    - <span data-ttu-id="9da69-147">Rücklieferung</span><span class="sxs-lookup"><span data-stu-id="9da69-147">Return order</span></span>
    - <span data-ttu-id="9da69-148">Sonstige Kopfgebühren</span><span class="sxs-lookup"><span data-stu-id="9da69-148">Header miscellaneous charge</span></span>
    - <span data-ttu-id="9da69-149">Sonstige Positionsbelastungen</span><span class="sxs-lookup"><span data-stu-id="9da69-149">Line miscellaneous charge</span></span>

- <span data-ttu-id="9da69-150">Kaufprozess</span><span class="sxs-lookup"><span data-stu-id="9da69-150">Purchase process</span></span>

    - <span data-ttu-id="9da69-151">Bestellung</span><span class="sxs-lookup"><span data-stu-id="9da69-151">Purchase order</span></span>
    - <span data-ttu-id="9da69-152">Bestätigung</span><span class="sxs-lookup"><span data-stu-id="9da69-152">Confirmation</span></span>
    - <span data-ttu-id="9da69-153">Zugangsliste</span><span class="sxs-lookup"><span data-stu-id="9da69-153">Receipts list</span></span>
    - <span data-ttu-id="9da69-154">Produktzugang</span><span class="sxs-lookup"><span data-stu-id="9da69-154">Product receipt</span></span>
    - <span data-ttu-id="9da69-155">Einkaufsrechnung</span><span class="sxs-lookup"><span data-stu-id="9da69-155">Purchase invoice</span></span>
    - <span data-ttu-id="9da69-156">Sonstige Kopfgebühren</span><span class="sxs-lookup"><span data-stu-id="9da69-156">Header miscellaneous charge</span></span>
    - <span data-ttu-id="9da69-157">Sonstige Positionsbelastungen</span><span class="sxs-lookup"><span data-stu-id="9da69-157">Line miscellaneous charge</span></span>
    - <span data-ttu-id="9da69-158">Gutschrift</span><span class="sxs-lookup"><span data-stu-id="9da69-158">Credit note</span></span>
    - <span data-ttu-id="9da69-159">Rücklieferung</span><span class="sxs-lookup"><span data-stu-id="9da69-159">Return order</span></span>
    - <span data-ttu-id="9da69-160">Bestellanforderung</span><span class="sxs-lookup"><span data-stu-id="9da69-160">Purchase requisition</span></span>
    - <span data-ttu-id="9da69-161">Sonstige Belastung pro Bestellanforderungsposition</span><span class="sxs-lookup"><span data-stu-id="9da69-161">Purchase requisition line miscellaneous charge</span></span>
    - <span data-ttu-id="9da69-162">Angebotsanforderung</span><span class="sxs-lookup"><span data-stu-id="9da69-162">Request for quotation</span></span>
    - <span data-ttu-id="9da69-163">Sonstige Kopfgebühr für Angebotsanforderung</span><span class="sxs-lookup"><span data-stu-id="9da69-163">Request for quotation header miscellaneous charge</span></span>
    - <span data-ttu-id="9da69-164">Sonstige Belastung pro Angebotsanforderungsposition</span><span class="sxs-lookup"><span data-stu-id="9da69-164">Request for quotation line miscellaneous charge</span></span>

- <span data-ttu-id="9da69-165">Bestandsprozess</span><span class="sxs-lookup"><span data-stu-id="9da69-165">Inventory process</span></span>

    - <span data-ttu-id="9da69-166">Umlagerungsauftrag – versenden</span><span class="sxs-lookup"><span data-stu-id="9da69-166">Transfer order – ship</span></span>
    - <span data-ttu-id="9da69-167">Umlagerungsauftrag – empfangen</span><span class="sxs-lookup"><span data-stu-id="9da69-167">Transfer order – receive</span></span>

## <a name="related-resources"></a><span data-ttu-id="9da69-168">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9da69-168">Related resources</span></span>

[<span data-ttu-id="9da69-169">Erste Schritte mit dem Steuerdienst</span><span class="sxs-lookup"><span data-stu-id="9da69-169">Get started with tax service</span></span>](./global-get-started-with-tax-calculation-service.md)

[<span data-ttu-id="9da69-170">Mehrere Mehrwertsteuererfassungsnummern</span><span class="sxs-lookup"><span data-stu-id="9da69-170">Multiple VAT registration number</span></span>](./emea-multiple-vat-registration-numbers.md)

[<span data-ttu-id="9da69-171">Unterstützung für Steuerfunktionen für Umlagerungsaufträge</span><span class="sxs-lookup"><span data-stu-id="9da69-171">Tax feature support for transfer order</span></span>](./tasks/tax-feature-support-for-transfer-order.md)

[<span data-ttu-id="9da69-172">So erstellen Sie eine Erweiterung im Steuerdienst</span><span class="sxs-lookup"><span data-stu-id="9da69-172">How to build extension in tax service</span></span>](./tax-service-add-data-fields-tax-integration-by-extension.md)