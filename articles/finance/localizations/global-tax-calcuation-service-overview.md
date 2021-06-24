---
title: Steuerberechnung (Vorschau)
description: In diesem Thema werden der Gesamtumfang und die Funktionen der Steuerberechnung erläutert.
author: wangchen
ms.date: 06/03/2021
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
ms.openlocfilehash: 9daa6e001200d03a2639974fb6de618d77ddf09d
ms.sourcegitcommit: cb282e8d2306ab71adf80a84346a6863d2d019e8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2021
ms.locfileid: "6184100"
---
# <a name="tax-calculation-preview"></a><span data-ttu-id="ede1e-103">Steuerberechnung (Vorschau)</span><span class="sxs-lookup"><span data-stu-id="ede1e-103">Tax Calculation (Preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="ede1e-104">Die Steuerberechnung ist ein hyperskalierbarer mandantenfähiger Dienst, mit dem die Global Tax Engine den Steuerermittlungs- und -berechnungsprozess automatisieren und vereinfachen kann.</span><span class="sxs-lookup"><span data-stu-id="ede1e-104">Tax Calculation is a hyper-scalable multitenant service that enables the global tax engine to automate and simplify the tax determination and calculation process.</span></span> <span data-ttu-id="ede1e-105">Das Steuermodul ist vollständig konfigurierbar.</span><span class="sxs-lookup"><span data-stu-id="ede1e-105">The tax engine is fully configurable.</span></span> <span data-ttu-id="ede1e-106">Zu den Elementen, die konfiguriert werden können, gehören unter anderem das steuerpflichtige Datenmodell, der Steuercode, die Steueranwendbarkeitsmatrix und die Steuerberechnungsformel.</span><span class="sxs-lookup"><span data-stu-id="ede1e-106">The elements that can be configured include, but aren't limited to, the taxable data model, tax code, tax applicability matrix, and tax calculation formula.</span></span> <span data-ttu-id="ede1e-107">Das Steuermodul läuft auf der Microsoft Azure-Hauptserviceplattform und bietet moderne Technologie und exponenzielle Skalierbarkeit.</span><span class="sxs-lookup"><span data-stu-id="ede1e-107">The tax engine runs on the Microsoft Azure core services platform, and offers modern technology and exponential scalability.</span></span>

<span data-ttu-id="ede1e-108">Die Steuerberechnung ist in Dynamics 365 Finance und Dynamics 365 Supply Chain Management integriert.</span><span class="sxs-lookup"><span data-stu-id="ede1e-108">Tax Calculation integrates with Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="ede1e-109">Schließlich wird er auch in Dynamics 365 Project Operations, Dynamics 365 Commerce und andere Anwendungen von Erstanbietern und Drittanbietern integriert.</span><span class="sxs-lookup"><span data-stu-id="ede1e-109">Eventually, it will also integrate with Dynamics 365 Project Operations, Dynamics 365 Commerce, and other first-party and third-party applications.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ede1e-110">Wenn Sie den Steuerberechnungsdienst aktivieren, werden einige Vorgänge an verwandten Daten möglicherweise in einem anderen Rechenzentrum als dem Rechenzentrum ausgeführt, das Ihre Dienstdaten verwaltet.</span><span class="sxs-lookup"><span data-stu-id="ede1e-110">When you enable the Tax Calculation service, some operations on related data might be performed in a data center other than the data center that maintains your service data.</span></span> <span data-ttu-id="ede1e-111">Überprüfen Sie die [Geschäftsbedingungen](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md), bevor Sie den Steuerberechnungsdienst aktivieren.</span><span class="sxs-lookup"><span data-stu-id="ede1e-111">Review the [Terms and Conditions](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md) before you enable the Tax Calculation service.</span></span> <span data-ttu-id="ede1e-112">Datenschutz ist uns sehr wichtig.</span><span class="sxs-lookup"><span data-stu-id="ede1e-112">Your privacy is important to us.</span></span> <span data-ttu-id="ede1e-113">Weiteres erfahren Sie in unserer [Datenschutzerklärung](https://go.microsoft.com/fwlink/?LinkId=521839).</span><span class="sxs-lookup"><span data-stu-id="ede1e-113">To learn more, read our [Privacy Statement](https://go.microsoft.com/fwlink/?LinkId=521839).</span></span>

<span data-ttu-id="ede1e-114">Die Steuerberechnung ist ein Microsoft-basiertes Steuermodul, das exponenzielle Skalierbarkeit bietet.</span><span class="sxs-lookup"><span data-stu-id="ede1e-114">Tax Calculation is a microservice-based tax engine that offers exponential scalability.</span></span> <span data-ttu-id="ede1e-115">Er kann bei der Ausführung folgender Aufgaben helfen:</span><span class="sxs-lookup"><span data-stu-id="ede1e-115">It can help you perform the following tasks:</span></span>

- <span data-ttu-id="ede1e-116">Konfigurieren Sie die Steuerberechnung über den Regulatory Configuration Service (RCS).</span><span class="sxs-lookup"><span data-stu-id="ede1e-116">Configure Tax Calculation through Regulatory Configuration Service (RCS).</span></span> <span data-ttu-id="ede1e-117">RCS ist eine erweiterte Version des Designers für elektronische Berichterstellung (ER) und als eigenständiger Dienst verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ede1e-117">RCS is an enhanced version of the Electronic reporting (ER) designer and is available as a standalone service.</span></span>
- <span data-ttu-id="ede1e-118">Konfigurieren Sie die Steuermatrix so, dass Steuercodes und Steuersätze automatisch ermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="ede1e-118">Configure the tax matrix to automatically determine tax codes and rates.</span></span>
- <span data-ttu-id="ede1e-119">Konfigurieren Sie die Steuermatrix so, dass die Steuerregistrierungsnummer automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="ede1e-119">Configure the tax matrix to automatically determine the tax registration number.</span></span>
- <span data-ttu-id="ede1e-120">Konfigurieren Sie den Steuerberechnungsdesigner so, dass Formeln und Bedingungen definiert werden.</span><span class="sxs-lookup"><span data-stu-id="ede1e-120">Configure the tax calculation designer to define formulas and conditions.</span></span>
- <span data-ttu-id="ede1e-121">Teilen Sie die Steuerermittlungs- und -berechnungslösung für verschiedene juristische Personen.</span><span class="sxs-lookup"><span data-stu-id="ede1e-121">Share the tax determination and calculation solution across legal entities.</span></span>

<span data-ttu-id="ede1e-122">Um den Steuerberechnungsdienst zu verwenden, installieren Sie das Steuerberechnungsdienst-Add-In aus Ihrem Projekt in Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="ede1e-122">To use the tax calculation service, install the tax calculation service add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="ede1e-123">Schließen Sie dann die Einrichtung in RCS ab und aktivieren Sie den Steuerberechnungsdienst in Finance und Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ede1e-123">Then complete the setup in RCS, and enable the tax calculation service in Finance and Supply Chain Management.</span></span> <span data-ttu-id="ede1e-124">Weitere Informationen finden Sie unter [Erste Schritte mit dem Steuerdienst](./global-get-started-with-tax-calculation-service.md).</span><span class="sxs-lookup"><span data-stu-id="ede1e-124">For more information, see [Get started with tax service](./global-get-started-with-tax-calculation-service.md).</span></span>

## <a name="availability"></a><span data-ttu-id="ede1e-125">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="ede1e-125">Availability</span></span>

<span data-ttu-id="ede1e-126">Die Steuerberechnung ist nur in Sandbox-Umgebungen und für ausgewählte Kunden über ein öffentliches Vorschauprogramm verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ede1e-126">Tax Calculation is available only in sandbox environments and to selected customers, through a public preview program.</span></span> <span data-ttu-id="ede1e-127">Schließlich wird es für alle Kunden und in Produktionsumgebungen allgemein verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="ede1e-127">Eventually, it will become generally available to all customers and in production environments.</span></span>

<span data-ttu-id="ede1e-128">Da laufend neue Funktionen bereitgestellt werden, lesen Sie regelmäßig die aktuellste Dokumentation, um mehr über die Abdeckung und den Umfang der unterstützten Funktionen zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="ede1e-128">New features will continue to be delivered, so be sure to check the most up-to-date documentation often to learn about the coverage and scope of supported features.</span></span>

<span data-ttu-id="ede1e-129">Die Steuerberechnung wird in den folgenden Azure-Regionen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="ede1e-129">Tax Calculation is deployed in the following Azure geographies.</span></span> <span data-ttu-id="ede1e-130">Er wird auch in weiteren Azure-Regionen bereitgestellt, je nach Kundenanforderungen:</span><span class="sxs-lookup"><span data-stu-id="ede1e-130">It will also be deployed to more Azure geographies, based on customer needs:</span></span>

- <span data-ttu-id="ede1e-131">Vereinigte Staaten</span><span class="sxs-lookup"><span data-stu-id="ede1e-131">United States</span></span>
- <span data-ttu-id="ede1e-132">Europa</span><span class="sxs-lookup"><span data-stu-id="ede1e-132">Europe</span></span>

> [!NOTE]
> <span data-ttu-id="ede1e-133">Die Steuerberechnung unterstützt keine lokalen Bereitstellungen von Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="ede1e-133">Tax Calculation doesn't support on-premises deployments of Dynamics 365.</span></span> <span data-ttu-id="ede1e-134">Frühere Versionen wie Dynamics AX 2012 werden ebenfalls nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ede1e-134">It also doesn't support earlier versions, such as Dynamics AX 2012.</span></span>

## <a name="feature-highlights"></a><span data-ttu-id="ede1e-135">Besondere Funktionen</span><span class="sxs-lookup"><span data-stu-id="ede1e-135">Feature highlights</span></span>

- <span data-ttu-id="ede1e-136">Eine konfigurierbare Steuermatrix für die automatische Ermittlung und Berechnung der Steuer</span><span class="sxs-lookup"><span data-stu-id="ede1e-136">A configurable tax matrix to automatically determine and calculate tax</span></span>
- <span data-ttu-id="ede1e-137">Unterstützung für mehrere Steuernummern</span><span class="sxs-lookup"><span data-stu-id="ede1e-137">Support for multiple tax registration numbers</span></span>
- <span data-ttu-id="ede1e-138">Umlagerungsauftragsunterstützung für Steuerermittlung und -berechnung</span><span class="sxs-lookup"><span data-stu-id="ede1e-138">Transfer order support for tax determination and calculation</span></span>
- <span data-ttu-id="ede1e-139">Umlagerungsauftragsunterstützung zur Ermittlung mehrerer Steuernummern</span><span class="sxs-lookup"><span data-stu-id="ede1e-139">Transfer order support for determination of multiple tax registration numbers</span></span>

## <a name="supported-transactions"></a><span data-ttu-id="ede1e-140">Unterstützte Transaktionen</span><span class="sxs-lookup"><span data-stu-id="ede1e-140">Supported transactions</span></span>

<span data-ttu-id="ede1e-141">Die Steuerberechnung kann nach juristischer Person und Transaktion aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="ede1e-141">Tax Calculation can be enabled by legal entity and transaction.</span></span> <span data-ttu-id="ede1e-142">Folgende Transaktionen werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="ede1e-142">The following transactions are supported:</span></span>

- <span data-ttu-id="ede1e-143">Verkaufsprozess</span><span class="sxs-lookup"><span data-stu-id="ede1e-143">Sales process</span></span>

    - <span data-ttu-id="ede1e-144">Verkaufsangebot</span><span class="sxs-lookup"><span data-stu-id="ede1e-144">Sales quotation</span></span>
    - <span data-ttu-id="ede1e-145">Auftrag</span><span class="sxs-lookup"><span data-stu-id="ede1e-145">Sales order</span></span>
    - <span data-ttu-id="ede1e-146">Bestätigung</span><span class="sxs-lookup"><span data-stu-id="ede1e-146">Confirmation</span></span>
    - <span data-ttu-id="ede1e-147">Kommissionierliste</span><span class="sxs-lookup"><span data-stu-id="ede1e-147">Picking list</span></span>
    - <span data-ttu-id="ede1e-148">Lieferschein</span><span class="sxs-lookup"><span data-stu-id="ede1e-148">Packing slip</span></span>
    - <span data-ttu-id="ede1e-149">Verkaufsrechnung</span><span class="sxs-lookup"><span data-stu-id="ede1e-149">Sales invoice</span></span>
    - <span data-ttu-id="ede1e-150">Gutschrift</span><span class="sxs-lookup"><span data-stu-id="ede1e-150">Credit note</span></span>
    - <span data-ttu-id="ede1e-151">Rücklieferung</span><span class="sxs-lookup"><span data-stu-id="ede1e-151">Return order</span></span>
    - <span data-ttu-id="ede1e-152">Sonstige Kopfgebühren</span><span class="sxs-lookup"><span data-stu-id="ede1e-152">Header miscellaneous charge</span></span>
    - <span data-ttu-id="ede1e-153">Sonstige Positionsbelastungen</span><span class="sxs-lookup"><span data-stu-id="ede1e-153">Line miscellaneous charge</span></span>

- <span data-ttu-id="ede1e-154">Kaufprozess</span><span class="sxs-lookup"><span data-stu-id="ede1e-154">Purchase process</span></span>

    - <span data-ttu-id="ede1e-155">Bestellung</span><span class="sxs-lookup"><span data-stu-id="ede1e-155">Purchase order</span></span>
    - <span data-ttu-id="ede1e-156">Bestätigung</span><span class="sxs-lookup"><span data-stu-id="ede1e-156">Confirmation</span></span>
    - <span data-ttu-id="ede1e-157">Zugangsliste</span><span class="sxs-lookup"><span data-stu-id="ede1e-157">Receipts list</span></span>
    - <span data-ttu-id="ede1e-158">Produktzugang</span><span class="sxs-lookup"><span data-stu-id="ede1e-158">Product receipt</span></span>
    - <span data-ttu-id="ede1e-159">Einkaufsrechnung</span><span class="sxs-lookup"><span data-stu-id="ede1e-159">Purchase invoice</span></span>
    - <span data-ttu-id="ede1e-160">Sonstige Kopfgebühren</span><span class="sxs-lookup"><span data-stu-id="ede1e-160">Header miscellaneous charge</span></span>
    - <span data-ttu-id="ede1e-161">Sonstige Positionsbelastungen</span><span class="sxs-lookup"><span data-stu-id="ede1e-161">Line miscellaneous charge</span></span>
    - <span data-ttu-id="ede1e-162">Gutschrift</span><span class="sxs-lookup"><span data-stu-id="ede1e-162">Credit note</span></span>
    - <span data-ttu-id="ede1e-163">Rücklieferung</span><span class="sxs-lookup"><span data-stu-id="ede1e-163">Return order</span></span>
    - <span data-ttu-id="ede1e-164">Bestellanforderung</span><span class="sxs-lookup"><span data-stu-id="ede1e-164">Purchase requisition</span></span>
    - <span data-ttu-id="ede1e-165">Sonstige Belastung pro Bestellanforderungsposition</span><span class="sxs-lookup"><span data-stu-id="ede1e-165">Purchase requisition line miscellaneous charge</span></span>
    - <span data-ttu-id="ede1e-166">Angebotsanforderung</span><span class="sxs-lookup"><span data-stu-id="ede1e-166">Request for quotation</span></span>
    - <span data-ttu-id="ede1e-167">Sonstige Kopfgebühr für Angebotsanforderung</span><span class="sxs-lookup"><span data-stu-id="ede1e-167">Request for quotation header miscellaneous charge</span></span>
    - <span data-ttu-id="ede1e-168">Sonstige Belastung pro Angebotsanforderungsposition</span><span class="sxs-lookup"><span data-stu-id="ede1e-168">Request for quotation line miscellaneous charge</span></span>

- <span data-ttu-id="ede1e-169">Bestandsprozess</span><span class="sxs-lookup"><span data-stu-id="ede1e-169">Inventory process</span></span>

    - <span data-ttu-id="ede1e-170">Umlagerungsauftrag – versenden</span><span class="sxs-lookup"><span data-stu-id="ede1e-170">Transfer order – ship</span></span>
    - <span data-ttu-id="ede1e-171">Umlagerungsauftrag – empfangen</span><span class="sxs-lookup"><span data-stu-id="ede1e-171">Transfer order – receive</span></span>

## <a name="related-resources"></a><span data-ttu-id="ede1e-172">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ede1e-172">Related resources</span></span>

[<span data-ttu-id="ede1e-173">Erste Schritte mit dem Steuerdienst</span><span class="sxs-lookup"><span data-stu-id="ede1e-173">Get started with tax service</span></span>](./global-get-started-with-tax-calculation-service.md)

[<span data-ttu-id="ede1e-174">Mehrere Mehrwertsteuererfassungsnummern</span><span class="sxs-lookup"><span data-stu-id="ede1e-174">Multiple VAT registration number</span></span>](./emea-multiple-vat-registration-numbers.md)

[<span data-ttu-id="ede1e-175">Unterstützung für Steuerfunktionen für Umlagerungsaufträge</span><span class="sxs-lookup"><span data-stu-id="ede1e-175">Tax feature support for transfer order</span></span>](./tasks/tax-feature-support-for-transfer-order.md)

[<span data-ttu-id="ede1e-176">So erstellen Sie eine Erweiterung im Steuerdienst</span><span class="sxs-lookup"><span data-stu-id="ede1e-176">How to build extension in tax service</span></span>](./tax-service-add-data-fields-tax-integration-by-extension.md)
