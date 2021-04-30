---
title: Steuerberechnung (Vorschau)
description: In diesem Thema werden der Gesamtumfang und die Funktionen der Steuerberechnung erläutert.
author: wangchen
ms.date: 04/12/2021
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
ms.openlocfilehash: 3df952e0632807e55f176e63dc2047be5e622ec2
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892348"
---
# <a name="tax-calculation-preview"></a><span data-ttu-id="ad057-103">Steuerberechnung (Vorschau)</span><span class="sxs-lookup"><span data-stu-id="ad057-103">Tax Calculation (Preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="ad057-104">Die Steuerberechnung ist ein hyperskalierbarer mandantenfähiger Dienst, mit dem die Global Tax Engine den Steuerermittlungs- und -berechnungsprozess automatisieren und vereinfachen kann.</span><span class="sxs-lookup"><span data-stu-id="ad057-104">Tax Calculation is a hyper-scalable multitenant service that enables the global tax engine to automate and simplify the tax determination and calculation process.</span></span> <span data-ttu-id="ad057-105">Das Steuermodul ist vollständig konfigurierbar.</span><span class="sxs-lookup"><span data-stu-id="ad057-105">The tax engine is fully configurable.</span></span> <span data-ttu-id="ad057-106">Zu den Elementen, die konfiguriert werden können, gehören unter anderem das steuerpflichtige Datenmodell, der Steuercode, die Steueranwendbarkeitsmatrix und die Steuerberechnungsformel.</span><span class="sxs-lookup"><span data-stu-id="ad057-106">The elements that can be configured include, but aren't limited to, the taxable data model, tax code, tax applicability matrix, and tax calculation formula.</span></span> <span data-ttu-id="ad057-107">Das Steuermodul läuft auf der Microsoft Azure-Hauptserviceplattform und bietet moderne Technologie und exponenzielle Skalierbarkeit.</span><span class="sxs-lookup"><span data-stu-id="ad057-107">The tax engine runs on the Microsoft Azure core services platform, and offers modern technology and exponential scalability.</span></span>

<span data-ttu-id="ad057-108">Die Steuerberechnung ist in Dynamics 365 Finance und Dynamics 365 Supply Chain Management integriert.</span><span class="sxs-lookup"><span data-stu-id="ad057-108">Tax Calculation integrates with Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="ad057-109">Schließlich wird er auch in Dynamics 365 Project Operations, Dynamics 365 Commerce und andere Anwendungen von Erstanbietern und Drittanbietern integriert.</span><span class="sxs-lookup"><span data-stu-id="ad057-109">Eventually, it will also integrate with Dynamics 365 Project Operations, Dynamics 365 Commerce, and other first-party and third-party applications.</span></span>

<span data-ttu-id="ad057-110">Die Steuerberechnung ist ein Microsoft-basiertes Steuermodul, das exponenzielle Skalierbarkeit bietet.</span><span class="sxs-lookup"><span data-stu-id="ad057-110">Tax Calculation is a microservice-based tax engine that offers exponential scalability.</span></span> <span data-ttu-id="ad057-111">Er kann bei der Ausführung folgender Aufgaben helfen:</span><span class="sxs-lookup"><span data-stu-id="ad057-111">It can help you perform the following tasks:</span></span>

- <span data-ttu-id="ad057-112">Konfigurieren Sie die Steuerberechnung über den Regulatory Configuration Service (RCS).</span><span class="sxs-lookup"><span data-stu-id="ad057-112">Configure Tax Calculation through Regulatory Configuration Service (RCS).</span></span> <span data-ttu-id="ad057-113">RCS ist eine erweiterte Version des Designers für elektronische Berichterstellung (ER) und als eigenständiger Dienst verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ad057-113">RCS is an enhanced version of the Electronic reporting (ER) designer and is available as a standalone service.</span></span>
- <span data-ttu-id="ad057-114">Konfigurieren Sie die Steuermatrix so, dass Steuercodes und Steuersätze automatisch ermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="ad057-114">Configure the tax matrix to automatically determine tax codes and rates.</span></span>
- <span data-ttu-id="ad057-115">Konfigurieren Sie die Steuermatrix so, dass die Steuerregistrierungsnummer automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="ad057-115">Configure the tax matrix to automatically determine the tax registration number.</span></span>
- <span data-ttu-id="ad057-116">Konfigurieren Sie den Steuerberechnungsdesigner so, dass Formeln und Bedingungen definiert werden.</span><span class="sxs-lookup"><span data-stu-id="ad057-116">Configure the tax calculation designer to define formulas and conditions.</span></span>
- <span data-ttu-id="ad057-117">Teilen Sie die Steuerermittlungs- und -berechnungslösung für verschiedene juristische Personen.</span><span class="sxs-lookup"><span data-stu-id="ad057-117">Share the tax determination and calculation solution across legal entities.</span></span>

<span data-ttu-id="ad057-118">Um den Steuerberechnungsdienst zu verwenden, installieren Sie das Steuerberechnungsdienst-Add-In aus Ihrem Projekt in Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="ad057-118">To use the tax calculation service, install the tax calculation service add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="ad057-119">Schließen Sie dann die Einrichtung in RCS ab und aktivieren Sie den Steuerberechnungsdienst in Finance und Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ad057-119">Then complete the setup in RCS, and enable the tax calculation service in Finance and Supply Chain Management.</span></span> <span data-ttu-id="ad057-120">Weitere Informationen finden Sie unter [Erste Schritte mit dem Steuerdienst](./global-get-started-with-tax-calculation-service.md).</span><span class="sxs-lookup"><span data-stu-id="ad057-120">For more information, see [Get started with tax service](./global-get-started-with-tax-calculation-service.md).</span></span>

## <a name="availability"></a><span data-ttu-id="ad057-121">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="ad057-121">Availability</span></span>

<span data-ttu-id="ad057-122">Die Steuerberechnung ist nur in Sandbox-Umgebungen und für ausgewählte Kunden über ein öffentliches Vorschauprogramm verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ad057-122">Tax Calculation is available only in sandbox environments and to selected customers, through a public preview program.</span></span> <span data-ttu-id="ad057-123">Schließlich wird es für alle Kunden und in Produktionsumgebungen allgemein verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="ad057-123">Eventually, it will become generally available to all customers and in production environments.</span></span>

<span data-ttu-id="ad057-124">Da laufend neue Funktionen bereitgestellt werden, lesen Sie regelmäßig die aktuellste Dokumentation, um mehr über die Abdeckung und den Umfang der unterstützten Funktionen zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="ad057-124">New features will continue to be delivered, so be sure to check the most up-to-date documentation often to learn about the coverage and scope of supported features.</span></span>

<span data-ttu-id="ad057-125">Die Steuerberechnung wird in den folgenden Azure-Regionen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="ad057-125">Tax Calculation is deployed in the following Azure geographies.</span></span> <span data-ttu-id="ad057-126">Er wird auch in weiteren Azure-Regionen bereitgestellt, je nach Kundenanforderungen:</span><span class="sxs-lookup"><span data-stu-id="ad057-126">It will also be deployed to more Azure geographies, based on customer needs:</span></span>

- <span data-ttu-id="ad057-127">Vereinigte Staaten</span><span class="sxs-lookup"><span data-stu-id="ad057-127">United States</span></span>
- <span data-ttu-id="ad057-128">Europa</span><span class="sxs-lookup"><span data-stu-id="ad057-128">Europe</span></span>

> [!NOTE]
> <span data-ttu-id="ad057-129">Die Steuerberechnung unterstützt keine lokalen Bereitstellungen von Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="ad057-129">Tax Calculation doesn't support on-premises deployments of Dynamics 365.</span></span> <span data-ttu-id="ad057-130">Frühere Versionen wie Dynamics AX 2012 werden ebenfalls nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ad057-130">It also doesn't support earlier versions, such as Dynamics AX 2012.</span></span>

## <a name="feature-highlights"></a><span data-ttu-id="ad057-131">Besondere Funktionen</span><span class="sxs-lookup"><span data-stu-id="ad057-131">Feature highlights</span></span>

- <span data-ttu-id="ad057-132">Eine konfigurierbare Steuermatrix für die automatische Ermittlung und Berechnung der Steuer</span><span class="sxs-lookup"><span data-stu-id="ad057-132">A configurable tax matrix to automatically determine and calculate tax</span></span>
- <span data-ttu-id="ad057-133">Unterstützung für mehrere Steuernummern</span><span class="sxs-lookup"><span data-stu-id="ad057-133">Support for multiple tax registration numbers</span></span>
- <span data-ttu-id="ad057-134">Umlagerungsauftragsunterstützung für Steuerermittlung und -berechnung</span><span class="sxs-lookup"><span data-stu-id="ad057-134">Transfer order support for tax determination and calculation</span></span>
- <span data-ttu-id="ad057-135">Umlagerungsauftragsunterstützung zur Ermittlung mehrerer Steuernummern</span><span class="sxs-lookup"><span data-stu-id="ad057-135">Transfer order support for determination of multiple tax registration numbers</span></span>

## <a name="supported-transactions"></a><span data-ttu-id="ad057-136">Unterstützte Transaktionen</span><span class="sxs-lookup"><span data-stu-id="ad057-136">Supported transactions</span></span>

<span data-ttu-id="ad057-137">Die Steuerberechnung kann nach juristischer Person und Transaktion aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="ad057-137">Tax Calculation can be enabled by legal entity and transaction.</span></span> <span data-ttu-id="ad057-138">Folgende Transaktionen werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="ad057-138">The following transactions are supported:</span></span>

- <span data-ttu-id="ad057-139">Verkaufsprozess</span><span class="sxs-lookup"><span data-stu-id="ad057-139">Sales process</span></span>

    - <span data-ttu-id="ad057-140">Verkaufsangebot</span><span class="sxs-lookup"><span data-stu-id="ad057-140">Sales quotation</span></span>
    - <span data-ttu-id="ad057-141">Auftrag</span><span class="sxs-lookup"><span data-stu-id="ad057-141">Sales order</span></span>
    - <span data-ttu-id="ad057-142">Bestätigung</span><span class="sxs-lookup"><span data-stu-id="ad057-142">Confirmation</span></span>
    - <span data-ttu-id="ad057-143">Kommissionierliste</span><span class="sxs-lookup"><span data-stu-id="ad057-143">Picking list</span></span>
    - <span data-ttu-id="ad057-144">Lieferschein</span><span class="sxs-lookup"><span data-stu-id="ad057-144">Packing slip</span></span>
    - <span data-ttu-id="ad057-145">Verkaufsrechnung</span><span class="sxs-lookup"><span data-stu-id="ad057-145">Sales invoice</span></span>
    - <span data-ttu-id="ad057-146">Gutschrift</span><span class="sxs-lookup"><span data-stu-id="ad057-146">Credit note</span></span>
    - <span data-ttu-id="ad057-147">Rücklieferung</span><span class="sxs-lookup"><span data-stu-id="ad057-147">Return order</span></span>
    - <span data-ttu-id="ad057-148">Sonstige Kopfgebühren</span><span class="sxs-lookup"><span data-stu-id="ad057-148">Header miscellaneous charge</span></span>
    - <span data-ttu-id="ad057-149">Sonstige Positionsbelastungen</span><span class="sxs-lookup"><span data-stu-id="ad057-149">Line miscellaneous charge</span></span>

- <span data-ttu-id="ad057-150">Kaufprozess</span><span class="sxs-lookup"><span data-stu-id="ad057-150">Purchase process</span></span>

    - <span data-ttu-id="ad057-151">Bestellung</span><span class="sxs-lookup"><span data-stu-id="ad057-151">Purchase order</span></span>
    - <span data-ttu-id="ad057-152">Bestätigung</span><span class="sxs-lookup"><span data-stu-id="ad057-152">Confirmation</span></span>
    - <span data-ttu-id="ad057-153">Zugangsliste</span><span class="sxs-lookup"><span data-stu-id="ad057-153">Receipts list</span></span>
    - <span data-ttu-id="ad057-154">Produktzugang</span><span class="sxs-lookup"><span data-stu-id="ad057-154">Product receipt</span></span>
    - <span data-ttu-id="ad057-155">Einkaufsrechnung</span><span class="sxs-lookup"><span data-stu-id="ad057-155">Purchase invoice</span></span>
    - <span data-ttu-id="ad057-156">Sonstige Kopfgebühren</span><span class="sxs-lookup"><span data-stu-id="ad057-156">Header miscellaneous charge</span></span>
    - <span data-ttu-id="ad057-157">Sonstige Positionsbelastungen</span><span class="sxs-lookup"><span data-stu-id="ad057-157">Line miscellaneous charge</span></span>
    - <span data-ttu-id="ad057-158">Gutschrift</span><span class="sxs-lookup"><span data-stu-id="ad057-158">Credit note</span></span>
    - <span data-ttu-id="ad057-159">Rücklieferung</span><span class="sxs-lookup"><span data-stu-id="ad057-159">Return order</span></span>
    - <span data-ttu-id="ad057-160">Bestellanforderung</span><span class="sxs-lookup"><span data-stu-id="ad057-160">Purchase requisition</span></span>
    - <span data-ttu-id="ad057-161">Sonstige Belastung pro Bestellanforderungsposition</span><span class="sxs-lookup"><span data-stu-id="ad057-161">Purchase requisition line miscellaneous charge</span></span>
    - <span data-ttu-id="ad057-162">Angebotsanforderung</span><span class="sxs-lookup"><span data-stu-id="ad057-162">Request for quotation</span></span>
    - <span data-ttu-id="ad057-163">Sonstige Kopfgebühr für Angebotsanforderung</span><span class="sxs-lookup"><span data-stu-id="ad057-163">Request for quotation header miscellaneous charge</span></span>
    - <span data-ttu-id="ad057-164">Sonstige Belastung pro Angebotsanforderungsposition</span><span class="sxs-lookup"><span data-stu-id="ad057-164">Request for quotation line miscellaneous charge</span></span>

- <span data-ttu-id="ad057-165">Bestandsprozess</span><span class="sxs-lookup"><span data-stu-id="ad057-165">Inventory process</span></span>

    - <span data-ttu-id="ad057-166">Umlagerungsauftrag – versenden</span><span class="sxs-lookup"><span data-stu-id="ad057-166">Transfer order – ship</span></span>
    - <span data-ttu-id="ad057-167">Umlagerungsauftrag – empfangen</span><span class="sxs-lookup"><span data-stu-id="ad057-167">Transfer order – receive</span></span>

## <a name="related-resources"></a><span data-ttu-id="ad057-168">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ad057-168">Related resources</span></span>

[<span data-ttu-id="ad057-169">Erste Schritte mit dem Steuerdienst</span><span class="sxs-lookup"><span data-stu-id="ad057-169">Get started with tax service</span></span>](./global-get-started-with-tax-calculation-service.md)

[<span data-ttu-id="ad057-170">Mehrere Mehrwertsteuererfassungsnummern</span><span class="sxs-lookup"><span data-stu-id="ad057-170">Multiple VAT registration number</span></span>](./emea-multiple-vat-registration-numbers.md)

[<span data-ttu-id="ad057-171">Unterstützung für Steuerfunktionen für Umlagerungsaufträge</span><span class="sxs-lookup"><span data-stu-id="ad057-171">Tax feature support for transfer order</span></span>](./tasks/tax-feature-support-for-transfer-order.md)

[<span data-ttu-id="ad057-172">So erstellen Sie eine Erweiterung im Steuerdienst</span><span class="sxs-lookup"><span data-stu-id="ad057-172">How to build extension in tax service</span></span>](./tax-service-add-data-fields-tax-integration-by-extension.md)