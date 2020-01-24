---
title: Unterstützte Standards für die elektronische Rechnungsstellung in Europa
description: Dieses Thema beschreibt die Abdeckung für eine elektronische Rechnungsstellung für Europa.
author: mrolecki
manager: AnnBe
ms.date: 07/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 10274
ms.search.region: Austria, Denmark, Italy, Norway, Spain, France, Belgium, Netherlands
ms.search.industry: ''
ms.author: mrolecki
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 2fb188498705dcbad841645ced43e6a1715cbbd0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915163"
---
# <a name="supported-standards-for-electronic-invoicing-in-europe"></a><span data-ttu-id="0f69d-103">Unterstützte Standards für die elektronische Rechnungsstellung in Europa</span><span class="sxs-lookup"><span data-stu-id="0f69d-103">Supported standards for electronic invoicing in Europe</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0f69d-104">Dieses Thema beschreibt die Abdeckung für eine elektronische Rechnungsstellung für Europa.</span><span class="sxs-lookup"><span data-stu-id="0f69d-104">This topic explains the level of coverage that exists for electronic invoicing for Europe.</span></span> 

<span data-ttu-id="0f69d-105">Die Implementierung und Übernahme der EU-weiten elektronischen Rechnungsstellung ist in der [Ratsrichtlinie 2010/45/EU](https://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2010:189:0001:0008:EN:PDF) geregelt, die für alle EU-Mitgliedstaaten gilt.</span><span class="sxs-lookup"><span data-stu-id="0f69d-105">Implementation and adoption of European Union-wide electronic invoicing is regulated [Council Directive 2010/45/EU](https://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2010:189:0001:0008:EN:PDF), which affects all EU member states.</span></span> <span data-ttu-id="0f69d-106">Unternehmen, die von der elektronischen Rechnungsstellung profitieren wollen, müssen Vertriebsrechnungen, Freitextrechnungen, Projektrechnungen, Vertriebsgutschriften und Projektrechnungsgutschriften als .xml-Dateien an die Regierung oder andere Handelspartner schicken, die die Verwendung der elektronischen Rechnungsstellung unterstützen.</span><span class="sxs-lookup"><span data-stu-id="0f69d-106">Companies that want to benefit from electronic invoicing must submit sales order invoices, free text invoices, project invoices, sales order credit notes, and project invoice credit notes as .xml files to the government or other trading parties that mandate use of electronic invoicing.</span></span> <span data-ttu-id="0f69d-107">Diese .xml-Dateien müssen bestimmten Standards entsprechen.</span><span class="sxs-lookup"><span data-stu-id="0f69d-107">These .xml files must comply with certain standards.</span></span> <span data-ttu-id="0f69d-108">Die länderspezifischen Anforderungen und ihre Implementierung kann sich zwischen EU-Mitgliedstaaten unterscheiden, aber in der Regel verwenden Sie [UBL](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=ubl) (Universal Business Language) in unterschiedlichen Versionen mit Anpassungen, ebenso wie [PEPPOL](https://www.peppol.eu)-Spezifikationen und -Zugriffspunkte für die Überprüfung und den Transport.</span><span class="sxs-lookup"><span data-stu-id="0f69d-108">The country-specific requirements and their implementation may differ across EU member states but commonly they are using Universal Business Language ([UBL](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=ubl)) in different versions with customizations as well as [PEPPOL](https://www.peppol.eu) specifications and access points for validation and transportation.</span></span> <span data-ttu-id="0f69d-109">Der Hauptvorteil von UBL ist, dass Geschäftsunterlagen für unterschiedliche Zwecke standardisiert werden können.</span><span class="sxs-lookup"><span data-stu-id="0f69d-109">The primary advantage of UBL is that business documents can be standardized for different purposes.</span></span> <span data-ttu-id="0f69d-110">UBL ist ein flexibler, internationaler Standard, der viele Geschäftsanforderungen unterstützt, deshalb können diese Geschäftsunterlagen über Landesgrenzen hinweg ausgetauscht werden.</span><span class="sxs-lookup"><span data-stu-id="0f69d-110">Because UBL is a flexible, international standard that supports many business requirements, these business documents can be exchanged across national borders.</span></span>

## <a name="what-electronic-invoice-formats-are-currently-available-in-dynamics-365-finance"></a><span data-ttu-id="0f69d-111">Welche Formate der elektronischen Rechnung sind in Dynamics 365 Finance derzeit verfügbar?</span><span class="sxs-lookup"><span data-stu-id="0f69d-111">What electronic invoice formats are currently available in Dynamics 365 Finance?</span></span>

<span data-ttu-id="0f69d-112">Die folgenden länderspezifischen Formate elektronischer Rechnungen stehen zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="0f69d-112">The following country-specific formats of electronic invoices are available:</span></span>

-   <span data-ttu-id="0f69d-113">OIOUBL v.2.02 für Dänemark</span><span class="sxs-lookup"><span data-stu-id="0f69d-113">OIOUBL v.2.02 for Denmark</span></span>
-   <span data-ttu-id="0f69d-114">EHF v.3.0 für Norwegen</span><span class="sxs-lookup"><span data-stu-id="0f69d-114">EHF v.3.0 for Norway</span></span>
-   <span data-ttu-id="0f69d-115">PEPPOL BIS v.2 für Österreich, Frankreich und Belgien</span><span class="sxs-lookup"><span data-stu-id="0f69d-115">PEPPOL BIS v.2 for Austria, France, and Belgium</span></span>
-   <span data-ttu-id="0f69d-116">UBL-OHNL 1.9 für die Niederlande</span><span class="sxs-lookup"><span data-stu-id="0f69d-116">UBL-OHNL 1.9 for the Netherlands</span></span>
-   <span data-ttu-id="0f69d-117">FacturaE v.3.2.1 für Spanien</span><span class="sxs-lookup"><span data-stu-id="0f69d-117">FacturaE v.3.2.1 for Spain</span></span>
-   <span data-ttu-id="0f69d-118">FatturaPA v.1.2 für Italien</span><span class="sxs-lookup"><span data-stu-id="0f69d-118">FatturaPA v.1.2 for Italy</span></span>
-   <span data-ttu-id="0f69d-119">xRechnung v.1.2 für Deutschland</span><span class="sxs-lookup"><span data-stu-id="0f69d-119">xRechnung v.1.2 for Germany</span></span>
-   <span data-ttu-id="0f69d-120">PEPPOL BIS Billing v.3.0 für die Europäische Union öffnen</span><span class="sxs-lookup"><span data-stu-id="0f69d-120">Open PEPPOL BIS Billing v.3.0 for European Union</span></span>

<span data-ttu-id="0f69d-121">Die elektronische Rechnungsstellung basiert auf der [elektronischen Berichtserstellung (EB)](../../dev-itpro/analytics/general-electronic-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="0f69d-121">Electronic invoicing is based on [Electronic reporting (ER)](../../dev-itpro/analytics/general-electronic-reporting.md).</span></span> <span data-ttu-id="0f69d-122">Es gibt ein **Debitorenrechnungsmodell**-Datenmodell sowie verschiedene länder-/regionsspezifische EB-Formatkonfigurationen für Österreich (AT), Dänemark (DK), Italien (IT), Norwegen (NO), Spanien (ES), Frankreich (FR), Belgien (BE), die Niederlande (NL), Deutschland (DE) und die Europäische Union (EU).</span><span class="sxs-lookup"><span data-stu-id="0f69d-122">A **Customer invoice model** data model and several country/region-specific ER format configurations have been created for Austria (AT), Denmark (DK), Italy (IT), Norway (NO), Spain (ES), France (FR), Belgium (BE), the Netherlands (NL), Germany (DE), and the European Union (EU).</span></span>

-   <span data-ttu-id="0f69d-123">OIOUBL Vertriebsrechnung – für AT, DK und NO</span><span class="sxs-lookup"><span data-stu-id="0f69d-123">OIOUBL Sales invoice - for AT, DK, and NO</span></span>
-   <span data-ttu-id="0f69d-124">OIOUBL Vertriebsgutschrift – für AT, DK und NO</span><span class="sxs-lookup"><span data-stu-id="0f69d-124">OIOUBL Sales credit note - for AT, DK, and NO</span></span>
-   <span data-ttu-id="0f69d-125">OIOUBL Projektrechnung – für AT, DK und NO</span><span class="sxs-lookup"><span data-stu-id="0f69d-125">OIOUBL Project invoice - for AT, DK, and NO</span></span>
-   <span data-ttu-id="0f69d-126">OIOUBL Projektgutschrift – für AT, DK und NO</span><span class="sxs-lookup"><span data-stu-id="0f69d-126">OIOUBL Project credit note - for AT, DK, and NO</span></span>
-   <span data-ttu-id="0f69d-127">UBL Vertriebsrechnung FR</span><span class="sxs-lookup"><span data-stu-id="0f69d-127">UBL Sales Invoice FR</span></span>
-   <span data-ttu-id="0f69d-128">UBL Vertriebsgutschrift FR</span><span class="sxs-lookup"><span data-stu-id="0f69d-128">UBL Sales Credit Note FR</span></span>
-   <span data-ttu-id="0f69d-129">UBL Projektrechnung FR</span><span class="sxs-lookup"><span data-stu-id="0f69d-129">UBL Project Invoice FR</span></span>
-   <span data-ttu-id="0f69d-130">UBL Projektgutschrift FR</span><span class="sxs-lookup"><span data-stu-id="0f69d-130">UBL Project Credit Note FR</span></span>
-   <span data-ttu-id="0f69d-131">UBL Vertriebsrechnung BE</span><span class="sxs-lookup"><span data-stu-id="0f69d-131">UBL Sales Invoice BE</span></span>
-   <span data-ttu-id="0f69d-132">UBL Vertriebsgutschrift BE</span><span class="sxs-lookup"><span data-stu-id="0f69d-132">UBL Sales Credit Note BE</span></span>
-   <span data-ttu-id="0f69d-133">UBL Projektrechnung BE</span><span class="sxs-lookup"><span data-stu-id="0f69d-133">UBL Project Invoice BE</span></span>
-   <span data-ttu-id="0f69d-134">UBL Projektgutschrift BE</span><span class="sxs-lookup"><span data-stu-id="0f69d-134">UBL Project Credit Note BE</span></span>
-   <span data-ttu-id="0f69d-135">UBL Vertriebsrechnung NL</span><span class="sxs-lookup"><span data-stu-id="0f69d-135">UBL Sales Invoice NL</span></span>
-   <span data-ttu-id="0f69d-136">UBL Vertriebsgutschrift NL</span><span class="sxs-lookup"><span data-stu-id="0f69d-136">UBL Sales Credit Note NL</span></span>
-   <span data-ttu-id="0f69d-137">UBL Projektrechnung NL</span><span class="sxs-lookup"><span data-stu-id="0f69d-137">UBL Project Invoice NL</span></span>
-   <span data-ttu-id="0f69d-138">UBL Projektgutschrift NL</span><span class="sxs-lookup"><span data-stu-id="0f69d-138">UBL Project Credit Note NL</span></span> 
-   <span data-ttu-id="0f69d-139">Vertriebsrechnung (ES)</span><span class="sxs-lookup"><span data-stu-id="0f69d-139">Sales invoice (ES)</span></span>
-   <span data-ttu-id="0f69d-140">Vertriebsrechnung (IT)</span><span class="sxs-lookup"><span data-stu-id="0f69d-140">Sales invoice (IT)</span></span>
-   <span data-ttu-id="0f69d-141">Projektrechnung (ES)</span><span class="sxs-lookup"><span data-stu-id="0f69d-141">Project invoice (ES)</span></span>
-   <span data-ttu-id="0f69d-142">Projektrechnung (IT)</span><span class="sxs-lookup"><span data-stu-id="0f69d-142">Project invoice (IT)</span></span>
-   <span data-ttu-id="0f69d-143">Verkaufsrechnung DE</span><span class="sxs-lookup"><span data-stu-id="0f69d-143">Sales Invoice DE</span></span>
-   <span data-ttu-id="0f69d-144">Projektrechnung DE</span><span class="sxs-lookup"><span data-stu-id="0f69d-144">Project Invoice DE</span></span>
-   <span data-ttu-id="0f69d-145">Peppol Verkaufsrechnung – für die EU</span><span class="sxs-lookup"><span data-stu-id="0f69d-145">Peppol Sales Invoice - for EU</span></span>
-   <span data-ttu-id="0f69d-146">Peppol Vertriebsgutschrift – für die EU</span><span class="sxs-lookup"><span data-stu-id="0f69d-146">Peppol Sales Credit Note - for EU</span></span>
-   <span data-ttu-id="0f69d-147">Peppol Projektrechnung – für die EU</span><span class="sxs-lookup"><span data-stu-id="0f69d-147">Peppol Project Invoice - for EU</span></span>
-   <span data-ttu-id="0f69d-148">Peppol Projekt-Vertriebsgutschrift – für die EU</span><span class="sxs-lookup"><span data-stu-id="0f69d-148">Peppol Project Credit Note - for EU</span></span>

<span data-ttu-id="0f69d-149">Die von Ihnen erstellten elektronischen Rechnungen und Gutschriften enthalten die erforderlichen Informationen, wie beispielsweise die EAN-Nummer (European Article Numbering), den Ansprechpartner, die Kontonummer sowie Adressinformationen für den Kunden.</span><span class="sxs-lookup"><span data-stu-id="0f69d-149">The electronic invoices and credit notes that you generate include required information, such as a European Article Numbering (EAN) number, contact person, dimension account number, and address information for the customer.</span></span> <span data-ttu-id="0f69d-150">Bei der Erstellung von Rechnungen werden Auswertungsregeln angewendet, Sie können also überprüfen, ob die richtigen Informationen eingetragen wurden.</span><span class="sxs-lookup"><span data-stu-id="0f69d-150">Validation rules are applied when invoices are generated so you can verify that the correct information has been entered.</span></span> <span data-ttu-id="0f69d-151">Welche Informationen gefordert werden, unterscheidet sich für die einzelnen Länder.</span><span class="sxs-lookup"><span data-stu-id="0f69d-151">The set of required information may differ from country to country.</span></span> <span data-ttu-id="0f69d-152">Die Anforderungen und die unterstützten Länder und Formate verändern sich in unregelmäßigen Abständen, Sie sollten also immer die Bibliothek der freigegebenen Anlagen in Microsoft Dynamics Lifecycle Services (LCS) besuchen und die aktuellste Liste der verfügbaren Dateien mit dem Anlagentyp der **GER-Konfiguration** abfragen.</span><span class="sxs-lookup"><span data-stu-id="0f69d-152">Because the requirements, as well as supported countries and formats, is subject to change, you should always go to the Shared asset library on Microsoft Dynamics Lifecycle services (LCS) and view the most up-to-date list of available files that have an asset type of **GER configuration**.</span></span>

## <a name="additional-information"></a><span data-ttu-id="0f69d-153">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0f69d-153">Additional information</span></span>
<span data-ttu-id="0f69d-154">Weitere Informationen über die Einrichtung elektronischer Rechnungen finden Sie in den folgenden [Aufgabenleitfäden](../../fin-and-ops/get-started/help-overview.md#task-guides) im Feld Hilfe:</span><span class="sxs-lookup"><span data-stu-id="0f69d-154">For more details about how to set up electronic invoices, you can play the following [Task guides](../../fin-and-ops/get-started/help-overview.md#task-guides) in the Help pane:</span></span>

 - <span data-ttu-id="0f69d-155">Einrichten der elektronischen OIOUBL-Rechnungsstellung</span><span class="sxs-lookup"><span data-stu-id="0f69d-155">Set up OIOUBL electronic invoicing</span></span>
 - <span data-ttu-id="0f69d-156">Konfigurationen der elektronischen Fakturierung des Imports OIOUBL</span><span class="sxs-lookup"><span data-stu-id="0f69d-156">Import OIOUBL electronic invoicing configurations</span></span>
 - <span data-ttu-id="0f69d-157">Einrichten von Debitorenkonten für die elektronische Fakturierung per OIOXML</span><span class="sxs-lookup"><span data-stu-id="0f69d-157">Set up customer accounts for OIOUBL electronic invoicing</span></span>

> [!NOTE] 
> <span data-ttu-id="0f69d-158">Diese Aufgabenleitfäden wurden für das für Dänemark spezifische Format elektronischer Rechnungen erstellt, *OIOUBL*, sie gelten jedoch mit geringen Abweichungen auch für andere unterstütze Länder.</span><span class="sxs-lookup"><span data-stu-id="0f69d-158">Although these Task guides were created for Danish-specific e-invoice format *OIOUBL*, they are applicable for other supported countries with minor deviations.</span></span>
