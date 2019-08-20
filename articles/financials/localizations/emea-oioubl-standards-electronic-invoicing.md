---
title: Unterstützte Standards für die elektronische Rechnungsstellung in Europa
description: Dieses Thema beschreibt die Abdeckung für eine elektronische Rechnungsstellung in Microsoft Dynamics 365 for Finance and Operations in der europäischen Region.
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
ms.openlocfilehash: 869deceb825ce6a823d5a39052e64e5b7ab61447
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/02/2019
ms.locfileid: "1852455"
---
# <a name="supported-standards-for-electronic-invoicing-in-europe"></a><span data-ttu-id="4a57b-103">Unterstützte Standards für die elektronische Rechnungsstellung in Europa</span><span class="sxs-lookup"><span data-stu-id="4a57b-103">Supported standards for electronic invoicing in Europe</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4a57b-104">Dieses Thema beschreibt die Abdeckung für eine elektronische Rechnungsstellung für Europa.</span><span class="sxs-lookup"><span data-stu-id="4a57b-104">This topic explains the level of coverage that exists for electronic invoicing for Europe.</span></span> 

<span data-ttu-id="4a57b-105">Die Implementierung und Übernahme der EU-weiten elektronischen Rechnungsstellung ist in der [Ratsrichtlinie 2010/45/EU](https://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2010:189:0001:0008:EN:PDF) geregelt, die für alle EU-Mitgliedstaaten gilt.</span><span class="sxs-lookup"><span data-stu-id="4a57b-105">Implementation and adoption of European Union-wide electronic invoicing is regulated [Council Directive 2010/45/EU](https://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2010:189:0001:0008:EN:PDF), which affects all EU member states.</span></span> <span data-ttu-id="4a57b-106">Unternehmen, die von der elektronischen Rechnungsstellung profitieren wollen, müssen Vertriebsrechnungen, Freitextrechnungen, Projektrechnungen, Vertriebsgutschriften und Projektrechnungsgutschriften als .xml-Dateien an die Regierung oder andere Handelspartner schicken, die die Verwendung der elektronischen Rechnungsstellung unterstützen.</span><span class="sxs-lookup"><span data-stu-id="4a57b-106">Companies that want to benefit from electronic invoicing must submit sales order invoices, free text invoices, project invoices, sales order credit notes, and project invoice credit notes as .xml files to the government or other trading parties that mandate use of electronic invoicing.</span></span> <span data-ttu-id="4a57b-107">Diese .xml-Dateien müssen bestimmten Standards entsprechen.</span><span class="sxs-lookup"><span data-stu-id="4a57b-107">These .xml files must comply with certain standards.</span></span> <span data-ttu-id="4a57b-108">Die länderspezifischen Anforderungen und ihre Implementierung kann sich zwischen EU-Mitgliedstaaten unterscheiden, aber in der Regel verwenden Sie [UBL](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=ubl) (Universal Business Language) in unterschiedlichen Versionen mit Anpassungen, ebenso wie [PEPPOL](https://www.peppol.eu)-Spezifikationen und -Zugriffspunkte für die Überprüfung und den Transport.</span><span class="sxs-lookup"><span data-stu-id="4a57b-108">The country-specific requirements and their implementation may differ across EU member states but commonly they are using Universal Business Language ([UBL](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=ubl)) in different versions with customizations as well as [PEPPOL](https://www.peppol.eu) specifications and access points for validation and transportation.</span></span> <span data-ttu-id="4a57b-109">Der Hauptvorteil von UBL ist, dass Geschäftsunterlagen für unterschiedliche Zwecke standardisiert werden können.</span><span class="sxs-lookup"><span data-stu-id="4a57b-109">The primary advantage of UBL is that business documents can be standardized for different purposes.</span></span> <span data-ttu-id="4a57b-110">UBL ist ein flexibler, internationaler Standard, der viele Geschäftsanforderungen unterstützt, deshalb können diese Geschäftsunterlagen über Landesgrenzen hinweg ausgetauscht werden.</span><span class="sxs-lookup"><span data-stu-id="4a57b-110">Because UBL is a flexible, international standard that supports many business requirements, these business documents can be exchanged across national borders.</span></span>

## <a name="what-electronic-invoice-formats-are-currently-available-in-finance-and-operations"></a><span data-ttu-id="4a57b-111">Welche elektronischen Rechnungsformate stehen derzeit in Finance and Operations zur Verfügung?</span><span class="sxs-lookup"><span data-stu-id="4a57b-111">What electronic invoice formats are currently available in Finance and Operations?</span></span>

<span data-ttu-id="4a57b-112">Die folgenden länderspezifischen Formate elektronischer Rechnungen stehen zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="4a57b-112">The following country-specific formats of electronic invoices are available:</span></span>

-   <span data-ttu-id="4a57b-113">OIOUBL v.2.02 für Dänemark</span><span class="sxs-lookup"><span data-stu-id="4a57b-113">OIOUBL v.2.02 for Denmark</span></span>
-   <span data-ttu-id="4a57b-114">EHF v.2.0.8 für Norwegen</span><span class="sxs-lookup"><span data-stu-id="4a57b-114">EHF v.2.0.8 for Norway</span></span>
-   <span data-ttu-id="4a57b-115">PEPPOL BIS v.2 für Österreich, Frankreich und Belgien</span><span class="sxs-lookup"><span data-stu-id="4a57b-115">PEPPOL BIS v.2 for Austria, France, and Belgium</span></span>
-   <span data-ttu-id="4a57b-116">UBL-OHNL 1.9 für die Niederlande</span><span class="sxs-lookup"><span data-stu-id="4a57b-116">UBL-OHNL 1.9 for the Netherlands</span></span>
-   <span data-ttu-id="4a57b-117">FacturaE v.3.2.1 für Spanien</span><span class="sxs-lookup"><span data-stu-id="4a57b-117">FacturaE v.3.2.1 for Spain</span></span>
-   <span data-ttu-id="4a57b-118">FatturaPA v.1.2 für Italien</span><span class="sxs-lookup"><span data-stu-id="4a57b-118">FatturaPA v.1.2 for Italy</span></span>

<span data-ttu-id="4a57b-119">Die elektronische Rechnungsstellung basiert auf der [elektronischen Berichtserstellung](../../dev-itpro/analytics/general-electronic-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="4a57b-119">Electronic invoicing is based on [electronic reporting](../../dev-itpro/analytics/general-electronic-reporting.md).</span></span> <span data-ttu-id="4a57b-120">Es gibt ein **Kundenrechnungsmodell**-Datenmodell sowie mehrere länderspezifische elektronische Berichtsformatkonfigurationen für Österreich (AT), Dänemark (DK), Italien (IT), Norwegen (NO), Spanien (ES), Frankreich (FR), Belgien (BE) und die Niederlande (NL).</span><span class="sxs-lookup"><span data-stu-id="4a57b-120">There is a **Customer invoice model** data model and a number of country-specific electronic reporting format configurations created for Austria (AT), Denmark (DK), Italy (IT), Norway (NO), Spain (ES), France (FR), Belgium (BE), and the Netherlands (NL).</span></span>

-   <span data-ttu-id="4a57b-121">OIOUBL Vertriebsrechnung – für AT, DK und NO</span><span class="sxs-lookup"><span data-stu-id="4a57b-121">OIOUBL Sales invoice - for AT, DK, and NO</span></span>
-   <span data-ttu-id="4a57b-122">OIOUBL Vertriebsgutschrift – für AT, DK und NO</span><span class="sxs-lookup"><span data-stu-id="4a57b-122">OIOUBL Sales credit note - for AT, DK, and NO</span></span>
-   <span data-ttu-id="4a57b-123">OIOUBL Projektrechnung – für AT, DK und NO</span><span class="sxs-lookup"><span data-stu-id="4a57b-123">OIOUBL Project invoice - for AT, DK, and NO</span></span>
-   <span data-ttu-id="4a57b-124">OIOUBL Projektgutschrift – für AT, DK und NO</span><span class="sxs-lookup"><span data-stu-id="4a57b-124">OIOUBL Project credit note - for AT, DK, and NO</span></span>
-   <span data-ttu-id="4a57b-125">UBL Vertriebsrechnung FR</span><span class="sxs-lookup"><span data-stu-id="4a57b-125">UBL Sales Invoice FR</span></span>
-   <span data-ttu-id="4a57b-126">UBL Vertriebsgutschrift FR</span><span class="sxs-lookup"><span data-stu-id="4a57b-126">UBL Sales Credit Note FR</span></span>
-   <span data-ttu-id="4a57b-127">UBL Projektrechnung FR</span><span class="sxs-lookup"><span data-stu-id="4a57b-127">UBL Project Invoice FR</span></span>
-   <span data-ttu-id="4a57b-128">UBL Projektgutschrift FR</span><span class="sxs-lookup"><span data-stu-id="4a57b-128">UBL Project Credit Note FR</span></span>
-   <span data-ttu-id="4a57b-129">UBL Vertriebsrechnung BE</span><span class="sxs-lookup"><span data-stu-id="4a57b-129">UBL Sales Invoice BE</span></span>
-   <span data-ttu-id="4a57b-130">UBL Vertriebsgutschrift BE</span><span class="sxs-lookup"><span data-stu-id="4a57b-130">UBL Sales Credit Note BE</span></span>
-   <span data-ttu-id="4a57b-131">UBL Projektrechnung BE</span><span class="sxs-lookup"><span data-stu-id="4a57b-131">UBL Project Invoice BE</span></span>
-   <span data-ttu-id="4a57b-132">UBL Projektgutschrift BE</span><span class="sxs-lookup"><span data-stu-id="4a57b-132">UBL Project Credit Note BE</span></span>
-   <span data-ttu-id="4a57b-133">UBL Vertriebsrechnung NL</span><span class="sxs-lookup"><span data-stu-id="4a57b-133">UBL Sales Invoice NL</span></span>
-   <span data-ttu-id="4a57b-134">UBL Vertriebsgutschrift NL</span><span class="sxs-lookup"><span data-stu-id="4a57b-134">UBL Sales Credit Note NL</span></span>
-   <span data-ttu-id="4a57b-135">UBL Projektrechnung NL</span><span class="sxs-lookup"><span data-stu-id="4a57b-135">UBL Project Invoice NL</span></span>
-   <span data-ttu-id="4a57b-136">UBL Projektgutschrift NL</span><span class="sxs-lookup"><span data-stu-id="4a57b-136">UBL Project Credit Note NL</span></span> 
-   <span data-ttu-id="4a57b-137">Vertriebsrechnung (ES)</span><span class="sxs-lookup"><span data-stu-id="4a57b-137">Sales invoice (ES)</span></span>
-   <span data-ttu-id="4a57b-138">Vertriebsrechnung (IT)</span><span class="sxs-lookup"><span data-stu-id="4a57b-138">Sales invoice (IT)</span></span>
-   <span data-ttu-id="4a57b-139">Projektrechnung (ES)</span><span class="sxs-lookup"><span data-stu-id="4a57b-139">Project invoice (ES)</span></span>
-   <span data-ttu-id="4a57b-140">Projektrechnung (IT)</span><span class="sxs-lookup"><span data-stu-id="4a57b-140">Project invoice (IT)</span></span>

<span data-ttu-id="4a57b-141">Die von Ihnen erstellten elektronischen Rechnungen und Gutschriften enthalten die erforderlichen Informationen, wie beispielsweise die EAN-Nummer (European Article Numbering), den Ansprechpartner, die Kontonummer sowie Adressinformationen für den Kunden.</span><span class="sxs-lookup"><span data-stu-id="4a57b-141">The electronic invoices and credit notes that you generate include required information, such as a European Article Numbering (EAN) number, contact person, dimension account number, and address information for the customer.</span></span> <span data-ttu-id="4a57b-142">Bei der Erstellung von Rechnungen werden Auswertungsregeln angewendet, Sie können also überprüfen, ob die richtigen Informationen eingetragen wurden.</span><span class="sxs-lookup"><span data-stu-id="4a57b-142">Validation rules are applied when invoices are generated so you can verify that the correct information has been entered.</span></span> <span data-ttu-id="4a57b-143">Welche Informationen gefordert werden, unterscheidet sich für die einzelnen Länder.</span><span class="sxs-lookup"><span data-stu-id="4a57b-143">The set of required information may differ from country to country.</span></span> <span data-ttu-id="4a57b-144">Die Anforderungen und die unterstützten Länder und Formate verändern sich in unregelmäßigen Abständen, Sie sollten also immer die Bibliothek der freigegebenen Anlagen in Microsoft Dynamics Lifecycle Services (LCS) besuchen und die aktuellste Liste der verfügbaren Dateien mit dem Anlagentyp der **GER-Konfiguration** abfragen.</span><span class="sxs-lookup"><span data-stu-id="4a57b-144">Because the requirements, as well as supported countries and formats, is subject to change, you should always go to the Shared asset library on Microsoft Dynamics Lifecycle services (LCS) and view the most up-to-date list of available files that have an asset type of **GER configuration**.</span></span>

## <a name="additional-information"></a><span data-ttu-id="4a57b-145">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4a57b-145">Additional information</span></span>
<span data-ttu-id="4a57b-146">Weitere Informationen über die Einrichtung elektronischer Rechnungen finden Sie in den folgenden [Aufgabenleitfäden](../../fin-and-ops/get-started/help-overview.md#task-guides) im Feld Hilfe:</span><span class="sxs-lookup"><span data-stu-id="4a57b-146">For more details about how to set up electronic invoices, you can play the following [Task guides](../../fin-and-ops/get-started/help-overview.md#task-guides) in the Help pane:</span></span>

 - <span data-ttu-id="4a57b-147">Einrichten der elektronischen OIOUBL-Rechnungsstellung</span><span class="sxs-lookup"><span data-stu-id="4a57b-147">Set up OIOUBL electronic invoicing</span></span>
 - <span data-ttu-id="4a57b-148">Konfigurationen der elektronischen Fakturierung des Imports OIOUBL</span><span class="sxs-lookup"><span data-stu-id="4a57b-148">Import OIOUBL electronic invoicing configurations</span></span>
 - <span data-ttu-id="4a57b-149">Einrichten von Debitorenkonten für die elektronische Fakturierung per OIOXML</span><span class="sxs-lookup"><span data-stu-id="4a57b-149">Set up customer accounts for OIOUBL electronic invoicing</span></span>

> [!NOTE] 
> <span data-ttu-id="4a57b-150">Diese Aufgabenleitfäden wurden für das für Dänemark spezifische Format elektronischer Rechnungen erstellt, *OIOUBL*, sie gelten jedoch mit geringen Abweichungen auch für andere unterstütze Länder.</span><span class="sxs-lookup"><span data-stu-id="4a57b-150">Although these Task guides were created for Danish-specific e-invoice format *OIOUBL*, they are applicable for other supported countries with minor deviations.</span></span>
