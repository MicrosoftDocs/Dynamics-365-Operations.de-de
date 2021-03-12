---
title: Unterstützte Standards für die elektronische Rechnungsstellung in Europa
description: Dieses Thema beschreibt die Abdeckung für eine elektronische Rechnungsstellung für Europa.
author: mrolecki
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 10274
ms.search.region: Austria, Denmark, Italy, Norway, Spain, France, Belgium, Netherlands
ms.search.industry: ''
ms.author: mrolecki
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 5e0bf6af3f255d277d4363b4d6c8c499c7a173f5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5002829"
---
# <a name="supported-standards-for-electronic-invoicing-in-europe"></a><span data-ttu-id="a69e8-103">Unterstützte Standards für die elektronische Rechnungsstellung in Europa</span><span class="sxs-lookup"><span data-stu-id="a69e8-103">Supported standards for electronic invoicing in Europe</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a69e8-104">Dieses Thema beschreibt die Abdeckung für eine elektronische Rechnungsstellung für Europa.</span><span class="sxs-lookup"><span data-stu-id="a69e8-104">This topic explains the level of coverage that exists for electronic invoicing for Europe.</span></span> 

<span data-ttu-id="a69e8-105">Die Implementierung und Übernahme der EU-weiten elektronischen Rechnungsstellung ist in der [Ratsrichtlinie 2010/45/EU](https://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2010:189:0001:0008:EN:PDF) geregelt, die für alle EU-Mitgliedstaaten gilt.</span><span class="sxs-lookup"><span data-stu-id="a69e8-105">Implementation and adoption of European Union-wide electronic invoicing is regulated [Council Directive 2010/45/EU](https://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2010:189:0001:0008:EN:PDF), which affects all EU member states.</span></span> <span data-ttu-id="a69e8-106">Unternehmen, die von der elektronischen Rechnungsstellung profitieren wollen, müssen Vertriebsrechnungen, Freitextrechnungen, Projektrechnungen, Vertriebsgutschriften und Projektrechnungsgutschriften als .xml-Dateien an die Regierung oder andere Handelspartner schicken, die die Verwendung der elektronischen Rechnungsstellung unterstützen.</span><span class="sxs-lookup"><span data-stu-id="a69e8-106">Companies that want to benefit from electronic invoicing must submit sales order invoices, free text invoices, project invoices, sales order credit notes, and project invoice credit notes as .xml files to the government or other trading parties that mandate use of electronic invoicing.</span></span> <span data-ttu-id="a69e8-107">Diese .xml-Dateien müssen bestimmten Standards entsprechen.</span><span class="sxs-lookup"><span data-stu-id="a69e8-107">These .xml files must comply with certain standards.</span></span> <span data-ttu-id="a69e8-108">Die länderspezifischen Anforderungen und ihre Implementierung kann sich zwischen EU-Mitgliedstaaten unterscheiden, aber in der Regel verwenden Sie [UBL](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=ubl) (Universal Business Language) in unterschiedlichen Versionen mit Anpassungen, ebenso wie [PEPPOL](https://www.peppol.eu)-Spezifikationen und -Zugriffspunkte für die Überprüfung und den Transport.</span><span class="sxs-lookup"><span data-stu-id="a69e8-108">The country-specific requirements and their implementation may differ across EU member states but commonly they are using Universal Business Language ([UBL](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=ubl)) in different versions with customizations as well as [PEPPOL](https://www.peppol.eu) specifications and access points for validation and transportation.</span></span> <span data-ttu-id="a69e8-109">Der Hauptvorteil von UBL ist, dass Geschäftsunterlagen für unterschiedliche Zwecke standardisiert werden können.</span><span class="sxs-lookup"><span data-stu-id="a69e8-109">The primary advantage of UBL is that business documents can be standardized for different purposes.</span></span> <span data-ttu-id="a69e8-110">UBL ist ein flexibler, internationaler Standard, der viele Geschäftsanforderungen unterstützt, deshalb können diese Geschäftsunterlagen über Landesgrenzen hinweg ausgetauscht werden.</span><span class="sxs-lookup"><span data-stu-id="a69e8-110">Because UBL is a flexible, international standard that supports many business requirements, these business documents can be exchanged across national borders.</span></span>

## <a name="electronic-invoice-formats-currently-available-in-dynamics-365-finance"></a><span data-ttu-id="a69e8-111">Derzeit in Dynamics 365 Finance verfügbare Formate der elektronischen Rechnung</span><span class="sxs-lookup"><span data-stu-id="a69e8-111">Electronic invoice formats currently available in Dynamics 365 Finance</span></span>

<span data-ttu-id="a69e8-112">Die folgenden länderspezifischen Formate elektronischer Rechnungen stehen zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="a69e8-112">The following country-specific formats of electronic invoices are available:</span></span>

-   <span data-ttu-id="a69e8-113">OIOUBL v.2.02 für Dänemark</span><span class="sxs-lookup"><span data-stu-id="a69e8-113">OIOUBL v.2.02 for Denmark</span></span>
-   <span data-ttu-id="a69e8-114">EHF v.3.0 für Norwegen</span><span class="sxs-lookup"><span data-stu-id="a69e8-114">EHF v.3.0 for Norway</span></span>
-   <span data-ttu-id="a69e8-115">PEPPOL BIS v.2 für Österreich, Frankreich und Belgien</span><span class="sxs-lookup"><span data-stu-id="a69e8-115">PEPPOL BIS v.2 for Austria, France, and Belgium</span></span>
-   <span data-ttu-id="a69e8-116">UBL-OHNL 1.9 für die Niederlande</span><span class="sxs-lookup"><span data-stu-id="a69e8-116">UBL-OHNL 1.9 for the Netherlands</span></span>
-   <span data-ttu-id="a69e8-117">FacturaE v.3.2.1 für Spanien</span><span class="sxs-lookup"><span data-stu-id="a69e8-117">FacturaE v.3.2.1 for Spain</span></span>
-   <span data-ttu-id="a69e8-118">FatturaPA v.1.2 für Italien</span><span class="sxs-lookup"><span data-stu-id="a69e8-118">FatturaPA v.1.2 for Italy</span></span>
-   <span data-ttu-id="a69e8-119">xRechnung v.1.2 für Deutschland</span><span class="sxs-lookup"><span data-stu-id="a69e8-119">xRechnung v.1.2 for Germany</span></span>
-   <span data-ttu-id="a69e8-120">PEPPOL BIS Billing v.3.0 für die Europäische Union öffnen</span><span class="sxs-lookup"><span data-stu-id="a69e8-120">Open PEPPOL BIS Billing v.3.0 for European Union</span></span>
-   <span data-ttu-id="a69e8-121">Estnisches spezifisches Format, Version 1.2</span><span class="sxs-lookup"><span data-stu-id="a69e8-121">Estonian specific format version 1.2</span></span>
-   <span data-ttu-id="a69e8-122">Finvoice 3.0 für Finnland</span><span class="sxs-lookup"><span data-stu-id="a69e8-122">Finvoice 3.0 for Finland</span></span>

<span data-ttu-id="a69e8-123">Die elektronische Rechnungsstellung basiert auf der [elektronischen Berichtserstellung (EB)](../../dev-itpro/analytics/general-electronic-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="a69e8-123">Electronic invoicing is based on [Electronic reporting (ER)](../../dev-itpro/analytics/general-electronic-reporting.md).</span></span> <span data-ttu-id="a69e8-124">Für die folgenden Länder/Regionen wurde ein **Rechnungsmodell**, Datenmodell, Rechnungsmodell-Mapping und verschiedene länder-/regionenspezifische EB-Formatkonfigurationen erstellt:</span><span class="sxs-lookup"><span data-stu-id="a69e8-124">An **Invoice model** data model, invoice model mapping, and several country/region-specific ER format configurations have been created for the following countries/regions:</span></span> 

- <span data-ttu-id="a69e8-125">Österreich (AT)</span><span class="sxs-lookup"><span data-stu-id="a69e8-125">Austria (AT)</span></span>
- <span data-ttu-id="a69e8-126">Dänemark (DK)</span><span class="sxs-lookup"><span data-stu-id="a69e8-126">Denmark (DK)</span></span>
- <span data-ttu-id="a69e8-127">Italien (IT)</span><span class="sxs-lookup"><span data-stu-id="a69e8-127">Italy (IT)</span></span>
- <span data-ttu-id="a69e8-128">Norwegen (NO)</span><span class="sxs-lookup"><span data-stu-id="a69e8-128">Norway (NO)</span></span>
- <span data-ttu-id="a69e8-129">Spanien (ES)</span><span class="sxs-lookup"><span data-stu-id="a69e8-129">Spain (ES)</span></span>
- <span data-ttu-id="a69e8-130">Frankreich (FR)</span><span class="sxs-lookup"><span data-stu-id="a69e8-130">France (FR)</span></span>
- <span data-ttu-id="a69e8-131">Belgien (BE)</span><span class="sxs-lookup"><span data-stu-id="a69e8-131">Belgium (BE)</span></span>
- <span data-ttu-id="a69e8-132">Niederlande (NL)</span><span class="sxs-lookup"><span data-stu-id="a69e8-132">The Netherlands (NL)</span></span>
- <span data-ttu-id="a69e8-133">Deutschland (DE)</span><span class="sxs-lookup"><span data-stu-id="a69e8-133">Germany (DE)</span></span>
- <span data-ttu-id="a69e8-134">Estland (EE)</span><span class="sxs-lookup"><span data-stu-id="a69e8-134">Estonia (EE)</span></span>
- <span data-ttu-id="a69e8-135">Finnland (FI)</span><span class="sxs-lookup"><span data-stu-id="a69e8-135">Finland (FI)</span></span>
- <span data-ttu-id="a69e8-136">Europäische Union (EU)</span><span class="sxs-lookup"><span data-stu-id="a69e8-136">The European Union (EU)</span></span>

<span data-ttu-id="a69e8-137">Das **Rechnungsmodell**, Datenmodell, Rechnungsmodell-Mapping und die länder-/regionenspezifische EB-Formatkonfigurationen umfassen:</span><span class="sxs-lookup"><span data-stu-id="a69e8-137">The **Invoice model** data model, invoice model mapping, and country/region-specific ER format configurations include:</span></span>

-   <span data-ttu-id="a69e8-138">OIOUBL Vertriebsrechnung – für AT, DK und NO</span><span class="sxs-lookup"><span data-stu-id="a69e8-138">OIOUBL Sales invoice - for AT, DK, and NO</span></span>
-   <span data-ttu-id="a69e8-139">OIOUBL Vertriebsgutschrift – für AT, DK und NO</span><span class="sxs-lookup"><span data-stu-id="a69e8-139">OIOUBL Sales credit note - for AT, DK, and NO</span></span>
-   <span data-ttu-id="a69e8-140">OIOUBL Projektrechnung – für AT, DK und NO</span><span class="sxs-lookup"><span data-stu-id="a69e8-140">OIOUBL Project invoice - for AT, DK, and NO</span></span>
-   <span data-ttu-id="a69e8-141">OIOUBL Projektgutschrift – für AT, DK und NO</span><span class="sxs-lookup"><span data-stu-id="a69e8-141">OIOUBL Project credit note - for AT, DK, and NO</span></span>
-   <span data-ttu-id="a69e8-142">UBL Vertriebsrechnung FR</span><span class="sxs-lookup"><span data-stu-id="a69e8-142">UBL Sales Invoice FR</span></span>
-   <span data-ttu-id="a69e8-143">UBL Vertriebsgutschrift FR</span><span class="sxs-lookup"><span data-stu-id="a69e8-143">UBL Sales Credit Note FR</span></span>
-   <span data-ttu-id="a69e8-144">UBL Projektrechnung FR</span><span class="sxs-lookup"><span data-stu-id="a69e8-144">UBL Project Invoice FR</span></span>
-   <span data-ttu-id="a69e8-145">UBL Projektgutschrift FR</span><span class="sxs-lookup"><span data-stu-id="a69e8-145">UBL Project Credit Note FR</span></span>
-   <span data-ttu-id="a69e8-146">UBL Vertriebsrechnung BE</span><span class="sxs-lookup"><span data-stu-id="a69e8-146">UBL Sales Invoice BE</span></span>
-   <span data-ttu-id="a69e8-147">UBL Vertriebsgutschrift BE</span><span class="sxs-lookup"><span data-stu-id="a69e8-147">UBL Sales Credit Note BE</span></span>
-   <span data-ttu-id="a69e8-148">UBL Projektrechnung BE</span><span class="sxs-lookup"><span data-stu-id="a69e8-148">UBL Project Invoice BE</span></span>
-   <span data-ttu-id="a69e8-149">UBL Projektgutschrift BE</span><span class="sxs-lookup"><span data-stu-id="a69e8-149">UBL Project Credit Note BE</span></span>
-   <span data-ttu-id="a69e8-150">UBL Vertriebsrechnung NL</span><span class="sxs-lookup"><span data-stu-id="a69e8-150">UBL Sales Invoice NL</span></span>
-   <span data-ttu-id="a69e8-151">UBL Vertriebsgutschrift NL</span><span class="sxs-lookup"><span data-stu-id="a69e8-151">UBL Sales Credit Note NL</span></span>
-   <span data-ttu-id="a69e8-152">UBL Projektrechnung NL</span><span class="sxs-lookup"><span data-stu-id="a69e8-152">UBL Project Invoice NL</span></span>
-   <span data-ttu-id="a69e8-153">UBL Projektgutschrift NL</span><span class="sxs-lookup"><span data-stu-id="a69e8-153">UBL Project Credit Note NL</span></span> 
-   <span data-ttu-id="a69e8-154">Vertriebsrechnung (ES)</span><span class="sxs-lookup"><span data-stu-id="a69e8-154">Sales invoice (ES)</span></span>
-   <span data-ttu-id="a69e8-155">Vertriebsrechnung (IT)</span><span class="sxs-lookup"><span data-stu-id="a69e8-155">Sales invoice (IT)</span></span>
-   <span data-ttu-id="a69e8-156">Projektrechnung (ES)</span><span class="sxs-lookup"><span data-stu-id="a69e8-156">Project invoice (ES)</span></span>
-   <span data-ttu-id="a69e8-157">Projektrechnung (IT)</span><span class="sxs-lookup"><span data-stu-id="a69e8-157">Project invoice (IT)</span></span>
-   <span data-ttu-id="a69e8-158">Verkaufsrechnung DE</span><span class="sxs-lookup"><span data-stu-id="a69e8-158">Sales Invoice DE</span></span>
-   <span data-ttu-id="a69e8-159">Projektrechnung DE</span><span class="sxs-lookup"><span data-stu-id="a69e8-159">Project Invoice DE</span></span>
-   <span data-ttu-id="a69e8-160">Peppol Verkaufsrechnung – für die EU</span><span class="sxs-lookup"><span data-stu-id="a69e8-160">Peppol Sales Invoice - for EU</span></span>
-   <span data-ttu-id="a69e8-161">Peppol Vertriebsgutschrift – für die EU</span><span class="sxs-lookup"><span data-stu-id="a69e8-161">Peppol Sales Credit Note - for EU</span></span>
-   <span data-ttu-id="a69e8-162">Peppol Projektrechnung – für die EU</span><span class="sxs-lookup"><span data-stu-id="a69e8-162">Peppol Project Invoice - for EU</span></span>
-   <span data-ttu-id="a69e8-163">Peppol Projekt-Vertriebsgutschrift – für die EU</span><span class="sxs-lookup"><span data-stu-id="a69e8-163">Peppol Project Credit Note - for EU</span></span>
-   <span data-ttu-id="a69e8-164">Vertriebsrechnung (EE)</span><span class="sxs-lookup"><span data-stu-id="a69e8-164">Sales invoice (EE)</span></span>
-   <span data-ttu-id="a69e8-165">Projektrechnung (EE)</span><span class="sxs-lookup"><span data-stu-id="a69e8-165">Project invoice (EE)</span></span>
-   <span data-ttu-id="a69e8-166">Vertriebsrechnung (FI)</span><span class="sxs-lookup"><span data-stu-id="a69e8-166">Sales invoice (FI)</span></span>
-   <span data-ttu-id="a69e8-167">Projektrechnung (FI)</span><span class="sxs-lookup"><span data-stu-id="a69e8-167">Project invoice (FI)</span></span>

<span data-ttu-id="a69e8-168">Die von Ihnen erstellten elektronischen Rechnungen und Gutschriften enthalten die erforderlichen Informationen, wie beispielsweise die EAN-Nummer (European Article Numbering), den Ansprechpartner, die Kontonummer sowie Adressinformationen für den Kunden.</span><span class="sxs-lookup"><span data-stu-id="a69e8-168">The electronic invoices and credit notes that you generate include required information, such as a European Article Numbering (EAN) number, contact person, dimension account number, and address information for the customer.</span></span> <span data-ttu-id="a69e8-169">Bei der Erstellung von Rechnungen werden Auswertungsregeln angewendet, Sie können also überprüfen, ob die richtigen Informationen eingetragen wurden.</span><span class="sxs-lookup"><span data-stu-id="a69e8-169">Validation rules are applied when invoices are generated so you can verify that the correct information has been entered.</span></span> <span data-ttu-id="a69e8-170">Welche Informationen gefordert werden, unterscheidet sich für die einzelnen Länder.</span><span class="sxs-lookup"><span data-stu-id="a69e8-170">The set of required information may differ from country to country.</span></span> <span data-ttu-id="a69e8-171">Die Anforderungen und die unterstützten Länder und Formate verändern sich in unregelmäßigen Abständen, Sie sollten also immer zur Bibliothek der freigegebenen Anlagen in Microsoft Dynamics Lifecycle Services (LCS) gehen und die aktuellste Liste der verfügbaren Dateien mit dem Anlagentyp der **GER-Konfiguration** abfragen.</span><span class="sxs-lookup"><span data-stu-id="a69e8-171">Because the requirements, as well as supported countries and formats, is subject to change, you should always go to the Shared asset library on Microsoft Dynamics Lifecycle Services (LCS) and view the most up-to-date list of available files that have an asset type of **GER configuration**.</span></span>

## <a name="electronic-invoice-configuration"></a><span data-ttu-id="a69e8-172">Elektronische Rechnungskonfiguration</span><span class="sxs-lookup"><span data-stu-id="a69e8-172">Electronic invoice configuration</span></span>
<span data-ttu-id="a69e8-173">Die Einrichtung und Besonderheiten elektronischer Rechnungen hängen von dem Land/der Region ab, für das/die sie implementiert sind.</span><span class="sxs-lookup"><span data-stu-id="a69e8-173">The setup and specifics of electronic invoices depend on the country/region that it's implemented for.</span></span> <span data-ttu-id="a69e8-174">Weitere Informationen zum Einrichten und Verwenden elektronischer Kundenrechnungen finden Sie in den entsprechenden länderspezifischen Themen:</span><span class="sxs-lookup"><span data-stu-id="a69e8-174">For more information about how to set up and use customer electronic invoices, see the related country-specific topics:</span></span>

- [<span data-ttu-id="a69e8-175">Italien</span><span class="sxs-lookup"><span data-stu-id="a69e8-175">Italy</span></span>](emea-ita-e-invoices.md)
- [<span data-ttu-id="a69e8-176">Norwegen</span><span class="sxs-lookup"><span data-stu-id="a69e8-176">Norway</span></span>](emea-nor-e-invoices.md)
- [<span data-ttu-id="a69e8-177">Deutschland</span><span class="sxs-lookup"><span data-stu-id="a69e8-177">Germany</span></span>](emea-deu-e-invoices.md)
- [<span data-ttu-id="a69e8-178">Finnland</span><span class="sxs-lookup"><span data-stu-id="a69e8-178">Finland</span></span>](https://support.microsoft.com/help/4559937)
- [<span data-ttu-id="a69e8-179">Estland</span><span class="sxs-lookup"><span data-stu-id="a69e8-179">Estonia</span></span>](https://support.microsoft.com/help/4552679)
- [<span data-ttu-id="a69e8-180">PEPPOL</span><span class="sxs-lookup"><span data-stu-id="a69e8-180">PEPPOL</span></span>](https://support.microsoft.com/help/4490320)

## <a name="additional-resources"></a><span data-ttu-id="a69e8-181">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a69e8-181">Additional resources</span></span>
<span data-ttu-id="a69e8-182">Weitere Informationen über die Einrichtung elektronischer Rechnungen finden Sie in den folgenden [Aufgabenleitfäden](../../fin-and-ops/get-started/help-overview.md#task-guides) im Feld Hilfe:</span><span class="sxs-lookup"><span data-stu-id="a69e8-182">For more details about how to set up electronic invoices, you can play the following [Task guides](../../fin-and-ops/get-started/help-overview.md#task-guides) in the Help pane:</span></span>

 - <span data-ttu-id="a69e8-183">Einrichten der elektronischen OIOUBL-Rechnungsstellung</span><span class="sxs-lookup"><span data-stu-id="a69e8-183">Set up OIOUBL electronic invoicing</span></span>
 - <span data-ttu-id="a69e8-184">Konfigurationen der elektronischen Fakturierung des Imports OIOUBL</span><span class="sxs-lookup"><span data-stu-id="a69e8-184">Import OIOUBL electronic invoicing configurations</span></span>
 - <span data-ttu-id="a69e8-185">Einrichten von Debitorenkonten für die elektronische Fakturierung per OIOXML</span><span class="sxs-lookup"><span data-stu-id="a69e8-185">Set up customer accounts for OIOUBL electronic invoicing</span></span>

> [!NOTE] 
> <span data-ttu-id="a69e8-186">Diese Aufgabenleitfäden wurden für das für Dänemark spezifische Format elektronischer Rechnungen erstellt, *OIOUBL*, sie gelten jedoch mit geringen Abweichungen auch für andere unterstütze Länder/Regionen.</span><span class="sxs-lookup"><span data-stu-id="a69e8-186">Although these Task guides were created for Danish-specific e-invoice format *OIOUBL*, they are applicable for other supported countries/regions with minor deviations.</span></span>
