---
title: Kreditorenkonten konfigurieren – Übersicht
description: In diesem Artikel werden die Seiten beschrieben, die Sie verwenden, um die grundlegenden und optionalen Funktionen für Kreditorenkonten einzurichten. Er beschreibt zudem die Einrichtungsschritte, die Sie durchführen müssen, bevor Sie damit beginnen, die Kreditoren einzurichten.
author: abruer
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankAccountTable, DeliveryMode, PaymTerm, VendGroup, VendParameters, VendPaymMode, VendTable, DeliveryReason, DeliveryTerms, DestinationCode
audience: Application User
ms.reviewer: roschlom
ms.custom: 24671
ms.assetid: 82561fe7-b2d6-464c-9347-79d0ce0f9743
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9ff2da881bb77bf7db2c443f3556b4255cd81e3d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972179"
---
# <a name="configure-accounts-payable-overview"></a><span data-ttu-id="7765f-104">Kreditorenkonten konfigurieren – Übersicht</span><span class="sxs-lookup"><span data-stu-id="7765f-104">Configure Accounts payable overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7765f-105">In diesem Artikel werden die Seiten beschrieben, die Sie verwenden, um die grundlegenden und optionalen Funktionen für Kreditorenkonten einzurichten.</span><span class="sxs-lookup"><span data-stu-id="7765f-105">This article describes the pages that you use to set up basic and optional functionality for Accounts payable.</span></span> <span data-ttu-id="7765f-106">Er beschreibt zudem die Einrichtungsschritte, die Sie durchführen müssen, bevor Sie damit beginnen, die Kreditoren einzurichten.</span><span class="sxs-lookup"><span data-stu-id="7765f-106">It also describes setup steps that you must complete before you start to set up Accounts payable.</span></span>

<a name="prerequisites-for-accounts-payable-setup"></a><span data-ttu-id="7765f-107">Voraussetzungen für die Einstellungen von Kreditoren</span><span class="sxs-lookup"><span data-stu-id="7765f-107">Prerequisites for Accounts payable setup</span></span>
----------------------------------------

<span data-ttu-id="7765f-108">Die folgenden Einstellungen müssen abgeschlossen werden, bevor Sie Kreditoren einrichten können:</span><span class="sxs-lookup"><span data-stu-id="7765f-108">Before you can set up Accounts payable, you must complete the following setup:</span></span>

-   <span data-ttu-id="7765f-109">Im Hauptbuch:</span><span class="sxs-lookup"><span data-stu-id="7765f-109">In General ledger:</span></span>
    -   <span data-ttu-id="7765f-110">Wenn Sie Zahlungserfassungen verwenden möchten, müssen Sie Zahlungserfassungen einrichten.</span><span class="sxs-lookup"><span data-stu-id="7765f-110">If you plan to use payment journals, set up payment journals.</span></span>
    -   <span data-ttu-id="7765f-111">Wenn Sie Wechselkursregulierungen ausführen möchten, müssen Sie die Währungscodes auf der Seite "Fremdwährungen", die Wechselkurstypen auf der Seite "Wechselkurstyp" und die Währungswechselkurse auf der Seite "Währungswechselkurse" einrichten.</span><span class="sxs-lookup"><span data-stu-id="7765f-111">If you plan to run exchange rate adjustments, set up currency codes on the Currencies page, set up exchange rate types on the Exchange rate types page, and set up currency exchange rates on the Currency exchange rates page.</span></span>
-   <span data-ttu-id="7765f-112">Richten Sie Bankkonten zur Verwendung mit Zahlungsmethoden unter "Bargeld- und Bankverwaltung" ein.</span><span class="sxs-lookup"><span data-stu-id="7765f-112">In Cash and bank management, set up bank accounts to use with methods of payment.</span></span>

## <a name="setup-pages-for-accounts-payable"></a><span data-ttu-id="7765f-113">Seiten für Kreditorenkonten einrichten</span><span class="sxs-lookup"><span data-stu-id="7765f-113">Setup pages for Accounts payable</span></span>

<span data-ttu-id="7765f-114">Verwenden Sie die folgenden Seiten, um die grundlegenden Funktionen von Kreditoren für jede juristische Person einzurichten.</span><span class="sxs-lookup"><span data-stu-id="7765f-114">Use the following pages to set up the basic functionality of Accounts payable for each legal entity.</span></span> <span data-ttu-id="7765f-115">Die Seiten sind in der empfohlenen Einrichtungsreihenfolge aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="7765f-115">The pages are listed in the recommended order of setup.</span></span> <span data-ttu-id="7765f-116">Erstellen Sie aus den ersten erstellten Datensätzen Vorlagen, um das Verfahren zu erleichtern.</span><span class="sxs-lookup"><span data-stu-id="7765f-116">To make the setup process easier, you can create templates from the first records that you create.</span></span> <span data-ttu-id="7765f-117">Eine Vorlage umfasst normalerweise Werte in einer Vielzahl von Feldern, die die Funktionen widerspiegeln, die die Organisation für einen bestimmten Kreditorentyp implementieren möchte.</span><span class="sxs-lookup"><span data-stu-id="7765f-117">In a template, values are typically entered in many fields to reflect the features that the organization wants to implement for a particular type of vendor.</span></span>
1.  <span data-ttu-id="7765f-118">Legen Sie auf der Seite "Zahlungsbedingungen", die Zahlungsbedingungen fest, die Sie Aufträgen, Bestellungen, Debitoren und Kreditoren zuweisen wollen und die die Fälligkeitsdaten bestimmen.</span><span class="sxs-lookup"><span data-stu-id="7765f-118">On the Terms of payment page, define the terms of payment that you assign to sales orders, purchase orders, customers, and vendors, and that determine invoice due dates.</span></span> <span data-ttu-id="7765f-119">Weitere Informationen finden Sie unter [Kreditorenzahlungsübersicht definieren](tasks/define-vendor-payment-fees.md).</span><span class="sxs-lookup"><span data-stu-id="7765f-119">For more information, see [Define vendor payment fees](tasks/define-vendor-payment-fees.md).</span></span>
2.  <span data-ttu-id="7765f-120">Erstellen und pflegen Sie im Formular "Zahlungsmethoden" Informationen zu der Art, wie die Organisation ihre Kreditoren bezahlt.</span><span class="sxs-lookup"><span data-stu-id="7765f-120">On the Methods of payment - vendors page, create and maintain information about how the organization pays its vendors.</span></span>
3.  <span data-ttu-id="7765f-121">Erstellen und pflegen Sie im Formular "Kreditorengruppen", Kreditorengruppen, die wichtige Parameter für Buchung, Zahlung und Ausgleich, die Berichterstellung und Planung gemeinsam haben.</span><span class="sxs-lookup"><span data-stu-id="7765f-121">On the Vendor groups page, create and maintain groups of vendors that share important parameters for posting, settlement and payment, reporting, and forecasting.</span></span>
4.  <span data-ttu-id="7765f-122">Definieren Sie auf der Seite "Debitorenbuchungsprofile", wie Kreditorenbuchungen im Hauptbuch gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="7765f-122">On the Vendor posting profiles page, define how vendor transactions are posted to the general ledger.</span></span>
5.  <span data-ttu-id="7765f-123">Richten Sie Standardeinstellungen auf der Seite "Kreditorenkontenparameter"ein, die angewendet werden, wenn keine spezifischere Einstellung angegeben wurde, sowie Parameter für verschiedene Arten von Funktionalität und die verschiedenen Nummernkreise für Kreditoren.</span><span class="sxs-lookup"><span data-stu-id="7765f-123">On the Accounts payable parameters page, set up default settings that are applied if a more specific setting isn't specified, parameters for various kinds of functionality, and the various number sequences for Accounts payable.</span></span>
6.  <span data-ttu-id="7765f-124">Legen Sie auf der Seite "Formular" das Format für verschiedene Dokumente fest, die sich auf Händler beziehen und in der Organisation verwendet werden, um Zugänge von Händlern zu verfolgen und Gründe für den Zahlungsfluss an Händler einzugeben.</span><span class="sxs-lookup"><span data-stu-id="7765f-124">On the Form setup page, define the format of various documents that are related to vendors, and that the organization uses to keep track of receipts from vendors and enter reasons for the flow of payments to vendors.</span></span>
7.  <span data-ttu-id="7765f-125">Erstellen und pflegen Sie auf der Seite "Händler" die Kreditorenkonten, einschließlich der Steuerbehörden, bei denen Ihre Organisation die Mehrwertsteuer meldet.</span><span class="sxs-lookup"><span data-stu-id="7765f-125">On the Vendors page, create and maintain vendor accounts, and also the tax authorities that your organization reports sales taxes to.</span></span>

## <a name="optional-setup-pages-for-accounts-payable"></a><span data-ttu-id="7765f-126">Optionale Einrichtungsseiten für Kreditorenkonten</span><span class="sxs-lookup"><span data-stu-id="7765f-126">Optional setup pages for Accounts payable</span></span>
<span data-ttu-id="7765f-127">Neben den grundlegenden Funktionen, können Sie weitere Funktionen für Kreditoren einrichten.</span><span class="sxs-lookup"><span data-stu-id="7765f-127">In addition to the basic functionality, Accounts payable has other functionality that you can set up.</span></span>

<span data-ttu-id="7765f-128">Die Seiten für zusätzliche Einstellungen sind nach Funktionen geordnet.</span><span class="sxs-lookup"><span data-stu-id="7765f-128">The additional setup pages are organized by functionality.</span></span>

<span data-ttu-id="7765f-129">**Richtlinien**</span><span class="sxs-lookup"><span data-stu-id="7765f-129">**Policies**</span></span>
-   <span data-ttu-id="7765f-130">Richten Sie auf der Seite "Kreditorenrechnungsrichtlinie" Kreditorenrechnungsrichtlinien ein.</span><span class="sxs-lookup"><span data-stu-id="7765f-130">On the Vendor invoice policy page, set up vendor invoice policies.</span></span>

<span data-ttu-id="7765f-131">**Rechnungsabgleich**</span><span class="sxs-lookup"><span data-stu-id="7765f-131">**Invoice matching**</span></span>

-   <span data-ttu-id="7765f-132">Richten Sie auf der Seite "Rechnungssummentoleranzen" Toleranzen für Rechnungssummen ein.</span><span class="sxs-lookup"><span data-stu-id="7765f-132">On the Invoice totals tolerances page, set up tolerances for invoice totals.</span></span>
-   <span data-ttu-id="7765f-133">Richten Sie auf der Seite "Abgleichsrichtlinie" zweiseitige und dreiseitige Abgleichsrichtlinien ein.</span><span class="sxs-lookup"><span data-stu-id="7765f-133">On the Matching policy page, set up two-way and three-way matching policies.</span></span>
-   <span data-ttu-id="7765f-134">Richten Sie auf der Seite "Preistoleranz" Toleranzen für Preise je Einheit ein.</span><span class="sxs-lookup"><span data-stu-id="7765f-134">On the Price tolerances page, set up tolerances for unit prices.</span></span>
-   <span data-ttu-id="7765f-135">Richten Sie auf der Seite "Preistoleranzgruppen für Artikel" Toleranzgruppen für Artikelpreise ein.</span><span class="sxs-lookup"><span data-stu-id="7765f-135">On the Item price tolerance groups page, set up tolerance groups for item prices.</span></span>
-   <span data-ttu-id="7765f-136">Richten Sie auf der Seite "Preistoleranzgruppen für Kreditoren" Toleranzgruppen für Kreditorenpreise ein.</span><span class="sxs-lookup"><span data-stu-id="7765f-136">On the Vendor price tolerance groups page, set up  tolerance groups for vendor prices.</span></span>
-   <span data-ttu-id="7765f-137">Richten Sie auf der Seite "Toleranzen für Belastungen" Toleranzen für Belastungen ein.</span><span class="sxs-lookup"><span data-stu-id="7765f-137">On the Charges tolerances page, set up tolerances for charges.</span></span>

<span data-ttu-id="7765f-138">**Workflow**</span><span class="sxs-lookup"><span data-stu-id="7765f-138">**Workflow**</span></span>

-   <span data-ttu-id="7765f-139">Richten Sie auf der Seite "Kreditorenkontenworkflows" die Workflowkonfigurationen für Erfassungsgenehmigungen und Bestellanforderung ein</span><span class="sxs-lookup"><span data-stu-id="7765f-139">On the Accounts payable workflows page, set up workflow configurations for journal approvals and purchase requisitions.</span></span>

<span data-ttu-id="7765f-140">**Ursachen**</span><span class="sxs-lookup"><span data-stu-id="7765f-140">**Reasons**</span></span>

-   <span data-ttu-id="7765f-141">Richten Sie auf der Seite "Ursachen für Kreditorenbuchungen" Ursachencodes ein.</span><span class="sxs-lookup"><span data-stu-id="7765f-141">On the Vendor reasons page, set up reason codes.</span></span>

<span data-ttu-id="7765f-142">**Belastungen**</span><span class="sxs-lookup"><span data-stu-id="7765f-142">**Charges**</span></span>

-   <span data-ttu-id="7765f-143">Richten Sie auf der Seite "Belastungscodes" Codes für die Belastungen ein, die in Bestellungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7765f-143">On the Charges code page, set up codes for the charges that are used in purchase orders.</span></span>
-   <span data-ttu-id="7765f-144">Auf der Seite "Gruppe für Kreditorenbelastungen" können Sie Belastungsgruppen für Kreditoren erstellen und verwalten.</span><span class="sxs-lookup"><span data-stu-id="7765f-144">On the Vendor charges group page, create and maintain charges groups for vendors.</span></span>
-   <span data-ttu-id="7765f-145">Auf der Seite "Gruppen für Artikelbelastungen" können Sie Belastungsgruppen für Artikel erstellen und verwalten.</span><span class="sxs-lookup"><span data-stu-id="7765f-145">On the Item charge groups page, create and maintain charges groups for items.</span></span>
-   <span data-ttu-id="7765f-146">Definieren Sie auf der Seite "Auto-Belastungen" Belastungen, die Aufträgen automatisch zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="7765f-146">On the Auto charges page, define the charges that are automatically assigned to orders.</span></span>

<span data-ttu-id="7765f-147">**Zusätzliche Artikel**</span><span class="sxs-lookup"><span data-stu-id="7765f-147">**Supplementary items**</span></span>

-   <span data-ttu-id="7765f-148">Auf der Seite "Zusätzliche Artikelgruppen - Kreditor", erstellen und verwalten Sie zusätzliche Artikelgruppen für Kreditoren.</span><span class="sxs-lookup"><span data-stu-id="7765f-148">On the Supplementary item groups - Vendor page, create and maintain supplementary item groups for vendors.</span></span>
-   <span data-ttu-id="7765f-149">Auf der Seite "Zusätzliche Artikelgruppen - Bestand", erstellen und verwalten Sie zusätzliche Artikelgruppen für Artikel.</span><span class="sxs-lookup"><span data-stu-id="7765f-149">On the Supplementary item groups - Inventory page, create and maintain supplementary item groups for items.</span></span>

<span data-ttu-id="7765f-150">**Verteilung**</span><span class="sxs-lookup"><span data-stu-id="7765f-150">**Distribution**</span></span>

-   <span data-ttu-id="7765f-151">Auf der Seite "Lieferbedingungen" erstellen und pflegen Sie die Bedingungen für den Transport eines Artikels vom Verkäufer zum Einkäufer.</span><span class="sxs-lookup"><span data-stu-id="7765f-151">On the Terms of delivery page, create and maintain the conditions for an item's transfer from seller to buyer.</span></span>
-   <span data-ttu-id="7765f-152">Auf der Seite "Lieferarten" erstellen und pflegen Sie die Transportmethoden, die beim Liefern eines Auftrags vom Verkäufer an den Käufer verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7765f-152">On the Modes of delivery page, create and maintain the methods of transport that are used when an order is delivered from the seller to the buyer.</span></span>
-   <span data-ttu-id="7765f-153">Auf der Seite "Bestimmungsortcodes" erstellen und pflegen Sie Kennungungen und Beschreibungen für Lieferziele.</span><span class="sxs-lookup"><span data-stu-id="7765f-153">On the Destination codes page, create and maintain identifiers and descriptions for delivery destinations.</span></span>

<span data-ttu-id="7765f-154">**Formulare**</span><span class="sxs-lookup"><span data-stu-id="7765f-154">**Forms**</span></span>

-   <span data-ttu-id="7765f-155">Erstellen Sie auf der Seite "Formularhinweise" den Standardtext, der auf verschiedenen Seiten angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="7765f-155">On the Form notes page, create the standard text that appears on various pages.</span></span>
-   <span data-ttu-id="7765f-156">Richten Sie auf der Seite "Sortierparameter für Formulare" die Sortierreihenfolgen für Anforderungen, Eingangslisten, Lieferscheine und Rechnungen ein.</span><span class="sxs-lookup"><span data-stu-id="7765f-156">On the Form sorting parameters page, set up the sorting order for requisitions, receipt lists, packing slips, and invoices.</span></span>
-   <span data-ttu-id="7765f-157">Richten Sie auf der Seite "Druckverwaltungseinstellungen" Druckverwaltungsinformationen für Originale und Kopien von Seiten ein.</span><span class="sxs-lookup"><span data-stu-id="7765f-157">On the Print management setup page, set up print management information for originals and copies of pages.</span></span>

<span data-ttu-id="7765f-158">**Zahlungen**</span><span class="sxs-lookup"><span data-stu-id="7765f-158">**Payments**</span></span>

-   <span data-ttu-id="7765f-159">Richten Sie auf der Seite "Skonto" die Bedingungen für den Erhalt von Skonti ein, und verwalten Sie diese.</span><span class="sxs-lookup"><span data-stu-id="7765f-159">On the Cash discounts page, set up and manage the terms for obtaining cash discounts.</span></span> <span data-ttu-id="7765f-160">Die Skontocodes sind mit Kreditoren verknüpft und werden auf Bestellungen angewendet.</span><span class="sxs-lookup"><span data-stu-id="7765f-160">The cash discount codes are linked to vendors and are applied to purchase orders.</span></span>
-   <span data-ttu-id="7765f-161">Auf der Seite "Zahlungspläne" richten Sie die Zahlungspläne ein, die verwendet werden, um Teilzahlungszahlungen an Kreditoren zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="7765f-161">On the Payment schedules page, set up the payment schedules that are used to manage installment payments to vendors.</span></span>
-   <span data-ttu-id="7765f-162">Legen Sie auf der Seite "Zahlungstage" die Zahlungstage fest, die zur Berechnung von Fälligkeitsdaten verwendet werden, und geben Sie Zahlungstage für einen bestimmten Wochentag oder bestimmten Tag im Monat an.</span><span class="sxs-lookup"><span data-stu-id="7765f-162">On the Payment days page, define the payment days that are used to calculate due dates, and specify payment days for a specific day of the week or month.</span></span>
-   <span data-ttu-id="7765f-163">Erstellen und pflegen Sie auf der Seite "Zahlungsgebühr" Zahlungsgebühren, die den Kreditoren zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="7765f-163">On the Payment fee page, create and maintain the payment fees that are associated with vendors.</span></span>
-   <span data-ttu-id="7765f-164">Erstellen und verwalten Sie auf der Seite "Zahlungsanweisungen" Zahlungsanweisungen.</span><span class="sxs-lookup"><span data-stu-id="7765f-164">On the Payment instruction page, create and maintain payment instructions.</span></span>

<span data-ttu-id="7765f-165">**Statistik**</span><span class="sxs-lookup"><span data-stu-id="7765f-165">**Statistics**</span></span>

-   <span data-ttu-id="7765f-166">Richten Sie auf der Seite "Zahlungsfristdefinitionen" benutzerdefinierte Intervalle zum Analysieren der Fälligkeitsverteilung von Kreditorenkonten ein.</span><span class="sxs-lookup"><span data-stu-id="7765f-166">On the Aging period definitions page, set up user-defined intervals that are used to analyze the maturity distribution of vendor accounts.</span></span>
-   <span data-ttu-id="7765f-167">Erstellen Sie auf der Seite "Sparte" die Spartencodes, die den Kreditoren zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="7765f-167">On the Line of business page, create the line of business (LOB) codes that are assigned to vendors.</span></span>

<span data-ttu-id="7765f-168">**Steuererklärung (US 1099)**</span><span class="sxs-lookup"><span data-stu-id="7765f-168">**Tax 1099**</span></span>

-   <span data-ttu-id="7765f-169">Überprüfen und aktualisieren Sie auf der Seite **1099 Felder** die Mindestbeträge, die dem Internal Revenue Service (IRS) auf Grundlage der neuesten IRS-Anforderungen gemeldet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="7765f-169">On the **1099 fields** page, verify and update the minimum amounts that must be reported to the Internal Revenue Service (IRS), based on the latest IRS requirements.</span></span>

## <a name="optional-setup-for-other-modules"></a><span data-ttu-id="7765f-170">**Optionaler Setup für andere Module**</span><span class="sxs-lookup"><span data-stu-id="7765f-170">**Optional setup for other modules**</span></span>
<span data-ttu-id="7765f-171">**Organisationsverwaltung**</span><span class="sxs-lookup"><span data-stu-id="7765f-171">**Organization administration**</span></span>

-   <span data-ttu-id="7765f-172">Richten Sie auf der Seite "Nummernkreise" die Nummernkreisgruppen für Rechnungsnummern ein.</span><span class="sxs-lookup"><span data-stu-id="7765f-172">On the Number sequences page, set up number sequence groups for invoice numbers.</span></span>
-   <span data-ttu-id="7765f-173">Richten Sie auf den folgenden Seiten Adressdaten ein:</span><span class="sxs-lookup"><span data-stu-id="7765f-173">On the following pages, set up address information:</span></span>
    -   <span data-ttu-id="7765f-174">Adresseinstellungen</span><span class="sxs-lookup"><span data-stu-id="7765f-174">Address setup</span></span>
    -   <span data-ttu-id="7765f-175">NAF-Codes</span><span class="sxs-lookup"><span data-stu-id="7765f-175">NAF codes</span></span>
    -   <span data-ttu-id="7765f-176">Postleitzahlen importieren</span><span class="sxs-lookup"><span data-stu-id="7765f-176">Import ZIP/postal codes</span></span>

<span data-ttu-id="7765f-177">**Hauptbuch**</span><span class="sxs-lookup"><span data-stu-id="7765f-177">**General ledger**</span></span>

-   <span data-ttu-id="7765f-178">Richten Sie auf der Seite "Finanzdimensionen" Finanzdimensionen ein.</span><span class="sxs-lookup"><span data-stu-id="7765f-178">On the Financial dimensions page, set up financial dimensions.</span></span>
-   <span data-ttu-id="7765f-179">Richten Sie auf den folgenden Seiten Steuerinformationen ein:</span><span class="sxs-lookup"><span data-stu-id="7765f-179">On the following pages, set up tax information:</span></span>
    -   <span data-ttu-id="7765f-180">Mehrwertsteuercodes</span><span class="sxs-lookup"><span data-stu-id="7765f-180">Sales tax codes</span></span>
    -   <span data-ttu-id="7765f-181">Mehrwertsteuergruppen</span><span class="sxs-lookup"><span data-stu-id="7765f-181">Sales tax groups</span></span>
    -   <span data-ttu-id="7765f-182">Artikel-Mehrwertsteuergruppen</span><span class="sxs-lookup"><span data-stu-id="7765f-182">Item sales tax groups</span></span>
    -   <span data-ttu-id="7765f-183">Kontengruppe</span><span class="sxs-lookup"><span data-stu-id="7765f-183">Account group</span></span>
    -   <span data-ttu-id="7765f-184">Mehrwertsteuer-Befreiungscodes</span><span class="sxs-lookup"><span data-stu-id="7765f-184">Sales tax exempt codes</span></span>
    -   <span data-ttu-id="7765f-185">Umsatzsteuerzuständigkeiten</span><span class="sxs-lookup"><span data-stu-id="7765f-185">Sales tax jurisdictions</span></span>
    -   <span data-ttu-id="7765f-186">Mehrwertsteuer-Behörden</span><span class="sxs-lookup"><span data-stu-id="7765f-186">Sales tax authorities</span></span>
    -   <span data-ttu-id="7765f-187">Mehrwertsteuer-Abrechnungszeiträume</span><span class="sxs-lookup"><span data-stu-id="7765f-187">Sales tax settlement periods</span></span>

<span data-ttu-id="7765f-188">**Bargeld- und Bankverwaltung**</span><span class="sxs-lookup"><span data-stu-id="7765f-188">**Cash and bank management**</span></span>

-   <span data-ttu-id="7765f-189">Richten Sie auf der Seite "Zahlungszweckcodes" den Code für die Zentralbank ein.</span><span class="sxs-lookup"><span data-stu-id="7765f-189">On the Payment purpose codes page, set up the Central Bank purpose code.</span></span>





