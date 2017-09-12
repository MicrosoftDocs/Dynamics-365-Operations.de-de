---
title: Intrastat
description: "Dieser Artikel enthält Informationen zur Intrastat-Berichterstattung für den Warenhandel und in einigen Fällen Dienstleistungen unter Ländern/Regionen der Europäischen Union (EU). Er gibt einen Überblick über Berichterstellungsprozesses und beschreibt die erforderlichen Einstellungen und die Voraussetzungen."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: Intrastat
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 28581
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: f54bf30a5f7666818757e6f89e8c01b7d54a266b
ms.contentlocale: de-de
ms.lasthandoff: 06/29/2017


---

# <a name="intrastat"></a><span data-ttu-id="c2dac-104">Intrastat</span><span class="sxs-lookup"><span data-stu-id="c2dac-104">Intrastat</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="c2dac-105">Dieser Artikel enthält Informationen zur Intrastat-Berichterstattung für den Warenhandel und in einigen Fällen Dienstleistungen unter Ländern/Regionen der Europäischen Union (EU).</span><span class="sxs-lookup"><span data-stu-id="c2dac-105">This article provides information about Intrastat reporting for the trade of goods and, in some cases, services among countries/regions of the European Union (EU).</span></span> <span data-ttu-id="c2dac-106">Er gibt einen Überblick über Berichterstellungsprozesses und beschreibt die erforderlichen Einstellungen und die Voraussetzungen.</span><span class="sxs-lookup"><span data-stu-id="c2dac-106">It provides an overview of the reporting process, and describes the required settings and prerequisites.</span></span>

<span data-ttu-id="c2dac-107">Intrastat ist das System für die Sammlung von Informationen und Generierung von statistischen Daten über den Warenhandel zwischen Ländern/Regionen der Europäischen Union (EU).</span><span class="sxs-lookup"><span data-stu-id="c2dac-107">Intrastat is the system for collecting information and generating statistics about the trade of goods among countries/regions of the European Union (EU).</span></span> <span data-ttu-id="c2dac-108">Intrastat-Berichte werden benötigt, wenn ein Produkt die Grenze eines anderen EU-Landes/einer anderen Region überschreitet.</span><span class="sxs-lookup"><span data-stu-id="c2dac-108">Intrastat reporting is required whenever a product crosses the border of another EU country/region.</span></span> <span data-ttu-id="c2dac-109">In einigen Ländern/Regionen sind Intrastat-Berichte außerdem für Dienstleistungen nötig.</span><span class="sxs-lookup"><span data-stu-id="c2dac-109">In several countries/regions, Intrastat reporting also applies to services.</span></span> <span data-ttu-id="c2dac-110">Erforderliche und optionale Elemente können im Intrastat-Bericht erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="c2dac-110">Mandatory and optional elements can be collected in Intrastat reporting.</span></span> <span data-ttu-id="c2dac-111">Die folgenden Elemente sind erforderlich: Die Umsatzsteuernummer (VAT ID) der Partei, die für die Bereitstellung der Informationen verantwortlich ist, der Referenzzeitraum, der Flow (Eingang oder Ausgang), der Warencode mit acht Ziffern, der Mitgliedsstaat des Partners (Mitgliedsstaat der Lieferung bei Eingang und Mitgliedsstaat des Ziels bei Ausgang), der Warenwert, die Warenmenge (Nettogewicht und zugehörige Einheit) sowie die Art der Transaktion.</span><span class="sxs-lookup"><span data-stu-id="c2dac-111">The following elements are mandatory: the value-added tax (VAT) number of the party that is responsible for providing information, the reference period, the flow (arrival or dispatch), the eight-digit commodity code, the partner member state (member state of consignment on arrivals and member state of destination on dispatches), the value of the goods, the quantity of the goods (net mass and supplementary unit), and the nature of the transaction.</span></span> <span data-ttu-id="c2dac-112">Länder/Regionen können auch optionale Elemente gemäß verschiedenen Bedingungen erfassen.</span><span class="sxs-lookup"><span data-stu-id="c2dac-112">Countries/regions can also collect optional elements under various conditions.</span></span> <span data-ttu-id="c2dac-113">Einige optionale Elemente sind Ursprungsland/-region, Lieferbedingungen, die Art des Transports, ein ausführlicherer Warencode als CN8, die Region des Ursprungs auf Dispositionen und die Region des Ziels auf Eingängen, das Statistikverfahren, der statistische Wert, einer Beschreibung der Waren und der Anschluss/der Flughafen des Ladens/Entladens.</span><span class="sxs-lookup"><span data-stu-id="c2dac-113">Some optional elements are the country/region of origin, the delivery terms, the mode of transport, a more detailed commodity code than CN8, the region of origin on dispatches and the region of destination on arrivals, the statistical procedure, the statistical value, a description of the goods, and the port/airport of loading/unloading.</span></span>

## <a name="overview-of-the-intrastat-reporting-process"></a><span data-ttu-id="c2dac-114">Überblick des Intrastat-Berichterstellungsprozesses</span><span class="sxs-lookup"><span data-stu-id="c2dac-114">Overview of the Intrastat reporting process</span></span>
<span data-ttu-id="c2dac-115">Die folgenden Abschnitte beschreiben den allgemeinen Informationsfluss, der für Intrastat-Berichte verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c2dac-115">The following sections describe the overall flow of information that is used for Intrastat reporting.</span></span>

### <a name="1-enter-a-transaction-that-crosses-the-border-of-another-eu-countryregion"></a><span data-ttu-id="c2dac-116">1. Geben Sie eine Buchung ein, welche die Grenze eines anderen EU-Landes/einer anderen Region überschreitet</span><span class="sxs-lookup"><span data-stu-id="c2dac-116">1. Enter a transaction that crosses the border of another EU country/region</span></span>

<span data-ttu-id="c2dac-117">Eine Debitorenrechnung, eine Freitextrechnung, eine Einkaufsrechnung, Projektrechnung, ein Debitorenlieferschein, ein Kreditorenproduktzugang oder Umlagerungsauftrag wird in die Intrastat-Erfassung übertragen, wenn die Länder-/Regionsart des Ziels (auf Dispositionen) oder Lieferung (auf Eingängen) ist **EU**.</span><span class="sxs-lookup"><span data-stu-id="c2dac-117">A customer invoice, free text invoice, purchase invoice, project invoice, customer packing slip, vendor product receipt, or transfer order is transferred to the Intrastat journal only if the country/region type of the destination (on dispatches) or consignment (on arrivals) is **EU**.</span></span> <span data-ttu-id="c2dac-118">Diese Funktion wurde für Microsoft Dynamics 365 for Operations (1611) erweitert und gestattet, Ladungsadressen für eine Intragemeinschaftsbuchung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="c2dac-118">This feature was extended for Microsoft Dynamics 365 for Operations (1611) and allows you to specify lading addresses for an intra-community transaction.</span></span> <span data-ttu-id="c2dac-119">Wenn eine Ladungsadresse sich von einer Kreditoren-Geschäftsadresse unterscheidet (oder Debitoren-Geschäftsadresse für Rücklieferung) funktioniert der Intrastat-Bericht mit diesen Informationen.</span><span class="sxs-lookup"><span data-stu-id="c2dac-119">If a lading address differs with a vendor business address (or customer business address for return order) the Intrastat reporting will operate with this information.</span></span> <span data-ttu-id="c2dac-120">Wenn Sie einen Auftrag, eine Freitextrechnung, eine Bestellung, eine Kreditorenrechnung, Projektrechnung oder einen Umlagerungsauftrag erstellen, besitzen einige Felder, die für Außenhandel zugeordnet sind, Standardwerte im Dokumentkopf oder in der Position.</span><span class="sxs-lookup"><span data-stu-id="c2dac-120">When you create a sales order, free text invoice, purchase order, vendor invoice, project invoice, or transfer order, some fields that are related to foreign trade have default values in the document header or on the line.</span></span> <span data-ttu-id="c2dac-121">Der standardmäßige Buchungscode wird aus dem entsprechenden Feld auf der Seite **Außenhandelsparameter** entnommen.</span><span class="sxs-lookup"><span data-stu-id="c2dac-121">The default transaction code is taken from the corresponding field on the **Foreign trade parameters** page.</span></span> <span data-ttu-id="c2dac-122">Der standardmäßige Warencode, Ursprungsland/-region und Bundesland/Kanton des Ursprungs werden dem Artikel selbst übernommen.</span><span class="sxs-lookup"><span data-stu-id="c2dac-122">The default commodity code, country/region of origin, and state/province of origin are taken from the item.</span></span> <span data-ttu-id="c2dac-123">Sie können die Standardwerte ändern und können auch andere außenhandelsbezogene Informationen ausfüllen: Statistiken-Verfahren, Transportmethode und Port.</span><span class="sxs-lookup"><span data-stu-id="c2dac-123">You can change the default values and can also fill in other foreign trade–related information: the statistics procedure, transport method, and port.</span></span>

### <a name="2-use-the-intrastat-journal-to-generate-information-about-trade-among-eu-countriesregions"></a><span data-ttu-id="c2dac-124">2. Mithilfe der Intrastat-Erfassung können Sie Informationen zum Handel zwischen EU-Ländern/Regionen generieren und melden</span><span class="sxs-lookup"><span data-stu-id="c2dac-124">2. Use the Intrastat journal to generate information about trade among EU countries/regions</span></span>

<span data-ttu-id="c2dac-125">Zu statistischen Zwecken generieren Sie Informationen zum Handel zwischen EU-Ländern/Regionen jeden Monat.</span><span class="sxs-lookup"><span data-stu-id="c2dac-125">For statistical purposes, you generate information about trade among EU countries/regions every month.</span></span> <span data-ttu-id="c2dac-126">Sie können Buchungen übertragen aus einer Freitextrechnung, einer Debitorenrechnung, einem Debitorenlieferschein, einer Kreditorenrechnung, einem Lieferschein des Kreditors, einer Projektrechnung oder aus einem Umlagerungsauftrag, entsprechend den Übertragungskriterien, die auf der Seite **Außenhandelsparameter** eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="c2dac-126">You can transfer transactions from a free text invoice, customer invoice, customer packing slip, vendor invoice, vendor packing slip, project invoice, or transfer order, according to the transfer criteria that are set up on the **Foreign trade parameters** page.</span></span> <span data-ttu-id="c2dac-127">Ersatzweise können Sie Transaktionen manuell eingeben.</span><span class="sxs-lookup"><span data-stu-id="c2dac-127">Alternatively, you can enter transactions manually.</span></span> <span data-ttu-id="c2dac-128">Sie können übertragene Buchungen in der Intrastat-Erfassung manuell aktualisieren, wenn derzeit Aktualisierungen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="c2dac-128">You can manually update transferred transactions in the Intrastat journal, if any updates are required.</span></span> <span data-ttu-id="c2dac-129">Unter bestimmten Bedingungen, die auf der Seite **Komprimierung von Intrastat** eingerichtet werden, können Sie die Buchungen in der Intrastat-Erfassung komprimieren.</span><span class="sxs-lookup"><span data-stu-id="c2dac-129">Under specific conditions that are set up on the **Compression of Intrastat** page, you can compress the transactions in the Intrastat journal.</span></span> <span data-ttu-id="c2dac-130">In einigen Ländern/Regionen können Sie einen kleinen Buchungsschwellenwert übernehmen.</span><span class="sxs-lookup"><span data-stu-id="c2dac-130">Some countries/regions let you apply a small transaction threshold.</span></span> <span data-ttu-id="c2dac-131">Sie können dann Buchungen melden, die unter dem Schwellenwert unter dem angegebenen Warencode sind.</span><span class="sxs-lookup"><span data-stu-id="c2dac-131">You can then report transactions that are below that threshold under the specified commodity code.</span></span> <span data-ttu-id="c2dac-132">Sie können den Warencode in den entsprechenden Intrastat-Erfassungspositionen aktualisieren, basierend auf der Einstellung **Untergrenze** auf der Seite **Außenhandelsparameter**.</span><span class="sxs-lookup"><span data-stu-id="c2dac-132">You can update the commodity code on the corresponding Intrastat journal lines, based on the **Minimum limit** setting on the **Foreign trade parameters** page.</span></span> <span data-ttu-id="c2dac-133">Sie können diese Buchungen auch komprimieren, basierend auf den Einstellungen auch **Komprimierung von Intrastat**.</span><span class="sxs-lookup"><span data-stu-id="c2dac-133">You can also compress those transactions, based on the **Compression of Intrastat** setting.</span></span> <span data-ttu-id="c2dac-134">Sie können die Vollständigkeit der Buchungen in der Intrastat-Erfassung überprüfen, basierend auf der Einstellung **Einstellungen prüfen** auf der Seite **Außenhandelsparameter**.</span><span class="sxs-lookup"><span data-stu-id="c2dac-134">You can validate the completeness of the transactions in the Intrastat journal, based on the **Check setup** setting on the **Foreign trade parameters** page.</span></span> <span data-ttu-id="c2dac-135">Die Daten in den entsprechenden Feldern werden auf Vollständigkeit geprüft möglicherweise: Land/Region, Bundesland oder Kanton., Gewicht, Warencode, Buchungscode, zusätzliche Einheit, Port, Buchungsgrundlage, Lieferbedingungen, Transportmethode und Steuernummer.</span><span class="sxs-lookup"><span data-stu-id="c2dac-135">The data in corresponding fields might be validated for completeness: country/region, state or province, weight, commodity code, transaction code, additional unit, port, origin, terms of delivery, transport method, and tax exempt number.</span></span> <span data-ttu-id="c2dac-136">Buchungen, die nicht abgeschlossen sind, werden markiert als ungültig.</span><span class="sxs-lookup"><span data-stu-id="c2dac-136">Transactions that aren't completed will be marked as not valid.</span></span>

### <a name="3-use-the-intrastat-journal-to-report-information-about-trade-among-eu-countriesregions"></a><span data-ttu-id="c2dac-137">3. Mithilfe der Intrastat-Erfassung können Sie Informationen zum Handel zwischen EU-Ländern/Regionen melden</span><span class="sxs-lookup"><span data-stu-id="c2dac-137">3. Use the Intrastat journal to report information about trade among EU countries/regions</span></span>

<span data-ttu-id="c2dac-138">Zu statistischen Zwecken melden Sie Informationen zum Handel zwischen EU-Ländern/Regionen jeden Monat.</span><span class="sxs-lookup"><span data-stu-id="c2dac-138">For statistical purposes, you report information about trade among EU countries/regions every month.</span></span> <span data-ttu-id="c2dac-139">Sie können den Intrastat-Bericht, basierend auf den Einstellungen **Berichtsformatzuordnung** drucken auf der **Außenhandelsparameter** Seite.</span><span class="sxs-lookup"><span data-stu-id="c2dac-139">You can print the Intrastat report, based on the **Report format mapping** settings on the **Foreign trade parameters** page.</span></span> <span data-ttu-id="c2dac-140">Sie können auch eine elektronische Datei generieren, basierend auf den Einstellungen **Dateiformatzuordnung** auf der **Außenhandelsparameter** Seite.</span><span class="sxs-lookup"><span data-stu-id="c2dac-140">You can also generate an electronic file, based on the **File format mapping** settings on the **Foreign trade parameters** page.</span></span> <span data-ttu-id="c2dac-141">Siehe auch die zusammenfassende Meldungs-Berichterstellungs-Wiki-Seite für weitere Informationen zu zusammenfassenden Meldungen, einschließlich der erforderlichen Komponenten.</span><span class="sxs-lookup"><span data-stu-id="c2dac-141">For more information about Intrastat reporting, including required prerequisites, see the Intrastat reporting task recordings:</span></span>

-   <span data-ttu-id="c2dac-142">Generieren Sie eine EU-Intrastat-Meldung</span><span class="sxs-lookup"><span data-stu-id="c2dac-142">Generate an EU Intrastat declaration,</span></span>
-   <span data-ttu-id="c2dac-143">Übertragen Sie Transaktionen an den Intrastat</span><span class="sxs-lookup"><span data-stu-id="c2dac-143">Transfer transactions to the Intrastat,</span></span>
-   <span data-ttu-id="c2dac-144">Angeben der Ladungsadresse für eine Innergemeinschaftliche Buchung.</span><span class="sxs-lookup"><span data-stu-id="c2dac-144">Specifying lading address for an intra-community transaction.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c2dac-145">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="c2dac-145">Prerequisites</span></span>
<span data-ttu-id="c2dac-146">In der folgenden Tabelle werden die Komponenten für Intrastat-Berichte angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c2dac-146">The following table lists the prerequisites for Intrastat reporting.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c2dac-147">Voraussetzung</span><span class="sxs-lookup"><span data-stu-id="c2dac-147">Prerequisite</span></span></th>
<th><span data-ttu-id="c2dac-148">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c2dac-148">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c2dac-149">Adresseinstellungen</span><span class="sxs-lookup"><span data-stu-id="c2dac-149">Address setup</span></span></td>
<td><span data-ttu-id="c2dac-150">Codes der Internationalen Organisation für Normung (ISO) für Länder/Regionen.</span><span class="sxs-lookup"><span data-stu-id="c2dac-150">Set up International Organization for Standardization (ISO) codes for countries/regions.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c2dac-151">Juristische Person</span><span class="sxs-lookup"><span data-stu-id="c2dac-151">Legal entity</span></span></td>
<td><span data-ttu-id="c2dac-152">Einrichten von Umsatzsteuer-ID-Nummern für den Import/Exportieren, die Fillialnummer-Erweiterung für den Import/Export und den Intrastat-Code, der der juristischen Person zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="c2dac-152">Set up tax exempt numbers for import/export, the branch number extension for import/export, and the Intrastat code that is assigned to the legal entity.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c2dac-153">Hierarchie der Produktkategorie (Vertriebshierarchie, Beschaffungshierarchie)</span><span class="sxs-lookup"><span data-stu-id="c2dac-153">Product category hierarchy (sales hierarchy, procurement hierarchy)</span></span></td>
<td><span data-ttu-id="c2dac-154">Weisen Sie die Intrastat-Warencodes den Kategorieknoten auf der Registerkarte <strong>Warencodes</strong> der Seite <strong>Kategoriehierarchie</strong> zu.</span><span class="sxs-lookup"><span data-stu-id="c2dac-154">Assign the Intrastat commodity codes to the category nodes on the <strong>Commodity codes</strong> tab of the <strong>Category hierarchy</strong> page.</span></span> <span data-ttu-id="c2dac-155">Wenn Sie einen Warencode einem Knoten der übergeordneten Kategorie zuweisen, ist dieser Code auf alle Knoten der untergeordneten Kategorie anwendbar.</span><span class="sxs-lookup"><span data-stu-id="c2dac-155">When you assign a commodity code to a parent category node, that code is applicable to all child category nodes.</span></span> <span data-ttu-id="c2dac-156">Die ausgewählten Warencodes sind in der Ansicht <strong>Ausgewählt</strong> verfügbar, wenn Sie einen Warencode in den Details für freigegebene Produkte und in Aufträgen, Bestellungen und Umlagerungsauftragspositionen auswählen.</span><span class="sxs-lookup"><span data-stu-id="c2dac-156">The selected commodity codes will be available in the <strong>Selected</strong> view when you select a commodity code in the released product details, and on sales order, purchase order, and transfer order lines.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c2dac-157">Details für freigegebene Produkte</span><span class="sxs-lookup"><span data-stu-id="c2dac-157">Released product details</span></span></td>
<td><span data-ttu-id="c2dac-158">Richten Sie die folgenden Außenhandelsdaten für freigegebene Produkte ein:</span><span class="sxs-lookup"><span data-stu-id="c2dac-158">Set up the following foreign trade data for released products:</span></span>
<ul>
<li><span data-ttu-id="c2dac-159"><strong>Warencode</strong> - Wählen Sie entweder aus der Liste der ausgewählten Waren aus, die von zugewiesenen Produktkategorien oder von der vollständigen Liste von Intrastat-Warencodes abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c2dac-159"><strong>Commodity code</strong> – Select from either the list of selected commodities that is retrieved from assigned product categories or the full list of Intrastat commodity codes.</span></span></li>
<li><span data-ttu-id="c2dac-160"><strong>Statistischer Prozentsatz der Belastungen</strong></span><span class="sxs-lookup"><span data-stu-id="c2dac-160"><strong>Statistical charges percentage</strong></span></span></li>
<li><span data-ttu-id="c2dac-161"><strong>Herkunftsland/-region</strong> - Wählen Sie das Standardland /-region aus, in dem die Waren vollständig erhalten oder produziert wurden.</span><span class="sxs-lookup"><span data-stu-id="c2dac-161"><strong>Country/region of origin</strong> – Select the default country/region where the goods were completely obtained or produced.</span></span></li>
<li><span data-ttu-id="c2dac-162"><strong>Bundesland/Kanton für Ursprung/Ziel</strong> - Wählen Sie das Standardbundesland/den Kanton des Ziels für Eingänge sowie das Ursprungsbundesland/den Kanton für den Versand aus.</span><span class="sxs-lookup"><span data-stu-id="c2dac-162"><strong>State/province of origin/destination</strong> – Select the default state/province of destination for arrivals and the state/province of origin for dispatches.</span></span></li>
<li><span data-ttu-id="c2dac-163"><strong>Nettogewicht in kg</strong></span><span class="sxs-lookup"><span data-stu-id="c2dac-163"><strong>Net weight in kg</strong></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c2dac-164">Kunden</span><span class="sxs-lookup"><span data-stu-id="c2dac-164">Customers</span></span></td>
<td><span data-ttu-id="c2dac-165">Richten Sie die Lieferadresse des Debitors im EU-Land/der EU-Region ein.</span><span class="sxs-lookup"><span data-stu-id="c2dac-165">Set up the customer delivery address in the EU country/region.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c2dac-166">Lieferanten</span><span class="sxs-lookup"><span data-stu-id="c2dac-166">Vendors</span></span></td>
<td><span data-ttu-id="c2dac-167">Richten Sie die Händleradresse im EU-Land/der EU-Region ein.</span><span class="sxs-lookup"><span data-stu-id="c2dac-167">Set up the vendor address in the EU country/region.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c2dac-168">Sonstige Zuschläge</span><span class="sxs-lookup"><span data-stu-id="c2dac-168">Miscellaneous charges</span></span></td>
<td><span data-ttu-id="c2dac-169">Richten Sie den Code für sonstige Zuschläge ein, der in den Rechnungsbetrag, im statistischen Betrag oder in beide einbezogen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c2dac-169">Set up the miscellaneous charges code to include in the invoice amount, the statistical amount, or both.</span></span> <span data-ttu-id="c2dac-170">Aktivieren Sie auf der Seite <strong>Codes für Belastungen</strong> auf der Registerkarte <strong>Außenhandel</strong> die Option <strong>Intrastat-Rechnungswert</strong>, um den Betrag der Zuschläge im Rechnungswert einzubeziehen, und aktivieren Sie <strong>Intrastat-Statistikwert</strong>, um den Betrag der Zuschläge im statistischen Wert einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="c2dac-170">On the <strong>Charges codes</strong> page, on the <strong>Foreign trade</strong> tab, enable <strong>Intrastat invoice value</strong> to include the charges amount in the invoice value, and enable <strong>Intrastat statistical value</strong> to include the charges amount in the statistical value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c2dac-171">Elektronische Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="c2dac-171">Electronic reporting</span></span></td>
<td><span data-ttu-id="c2dac-172">Einrichten der elektronischen Berichterstellungskonfigurationen, um Intrastat-Daten in einer elektronischen Datei zu exportieren, die das Format hat, das von den zuständigen Behörden angefordert wird, und Intrastat-Daten in einem benutzerfreundlichen, lesbaren Format in der Vorschau anzuzeigen (beispielsweise in Microsoft Excel).</span><span class="sxs-lookup"><span data-stu-id="c2dac-172">Set up electronic reporting configurations to export Intrastat data in an electronic file that has the format that is requested by the relevant authorities, and to preview Intrastat data in a user-friendly, readable format (for example, in Microsoft Excel).</span></span></td>
</tr>
</tbody>
</table>

## <a name="setup"></a><span data-ttu-id="c2dac-173">Einstellung</span><span class="sxs-lookup"><span data-stu-id="c2dac-173">Setup</span></span>
<span data-ttu-id="c2dac-174">In den folgenden Abschnitten werden die Einstellungen beschrieben, die für Intrastat-Berichte erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="c2dac-174">The following sections describe the settings that are required for Intrastat reporting.</span></span>

### <a name="set-up-all-required-intrastat-related-lists"></a><span data-ttu-id="c2dac-175">Einrichten aller erforderlichen Intrastat-zugeordneten Listen</span><span class="sxs-lookup"><span data-stu-id="c2dac-175">Set up all required Intrastat-related lists</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c2dac-176">Liste</span><span class="sxs-lookup"><span data-stu-id="c2dac-176">List</span></span></th>
<th><span data-ttu-id="c2dac-177">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c2dac-177">Additional information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c2dac-178">Warencodes</span><span class="sxs-lookup"><span data-stu-id="c2dac-178">Commodity codes</span></span></td>
<td><span data-ttu-id="c2dac-179">Richten Sie eine Kategoriehierarchie vom Typ <strong>Warencode</strong> ein, und geben Sie alle Warencodes gemäß der Liste der kombinierten Nomenklatur ein.</span><span class="sxs-lookup"><span data-stu-id="c2dac-179">Set up a category hierarchy of type <strong>Commodity code</strong>, and enter all commodity codes according to the combined nomenclature list.</span></span> <span data-ttu-id="c2dac-180">Für jede Ware richten Sie die folgenden Informationen ein:</span><span class="sxs-lookup"><span data-stu-id="c2dac-180">For each commodity, you set up the following information:</span></span>
<ul>
<li><span data-ttu-id="c2dac-181">Der Name der Ware und der Warencode</span><span class="sxs-lookup"><span data-stu-id="c2dac-181">The name of the commodity and the commodity code</span></span></li>
<li><span data-ttu-id="c2dac-182">Der Anzeigename und/oder übersetzte Name</span><span class="sxs-lookup"><span data-stu-id="c2dac-182">The friendly name and/or translated name</span></span></li>
<li><span data-ttu-id="c2dac-183">Einstellungen für die Meldung von zusätzlichen Einheiten auf der <strong>Außenhandel</strong> Registerkarte.</span><span class="sxs-lookup"><span data-stu-id="c2dac-183">Settings for reporting additional (supplementary) units on the <strong>Foreign trade</strong> tab.</span></span> <span data-ttu-id="c2dac-184">Sie können die zusätzliche Einheit in der Einheitsliste auswählen.</span><span class="sxs-lookup"><span data-stu-id="c2dac-184">You can select the additional unit in the unit list.</span></span> <span data-ttu-id="c2dac-185">Sie können auch angeben, ob das Gewicht von Waren zusätzlich zur ausgewählten zusätzlichen Einheit angegeben werden muss.</span><span class="sxs-lookup"><span data-stu-id="c2dac-185">You can also specify whether the weight of commodities must be reported in addition to the selected additional unit.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c2dac-186">Art des Geschäftes</span><span class="sxs-lookup"><span data-stu-id="c2dac-186">Transaction codes</span></span></td>
<td><span data-ttu-id="c2dac-187">Richten Sie die Art der Buchung gemäß den Anforderungen Ihres Landes/Ihrer Region ein.</span><span class="sxs-lookup"><span data-stu-id="c2dac-187">Set up the nature of the transaction according to your country's/region's requirements.</span></span> <span data-ttu-id="c2dac-188">Für jeden Buchungscode, den Sie einrichten, müssen Sie die Regeln für die Berechnung der Rechnungsbeträge und von statistischen Beträgen für Umlagerungsaufträge und Verkauf/Bestellungen einrichten.</span><span class="sxs-lookup"><span data-stu-id="c2dac-188">For each transaction code that you set up, you must set up the rules for calculating invoice amounts and statistical amounts for transfer orders and sales/purchase orders.</span></span>
<ul>
<li><span data-ttu-id="c2dac-189">Für Umlagerungsaufträge richten Sie eine der folgenden Regeln für die Berechnung der Rechnungsbeträge und statistischen Beträgen ein:</span><span class="sxs-lookup"><span data-stu-id="c2dac-189">For transfer orders, you set up one of the following rules for calculating invoice amounts and statistical amounts:</span></span>
<ul>
<li><span data-ttu-id="c2dac-190"><strong>Leer</strong> – Der Betrag ist 0 (Null).</span><span class="sxs-lookup"><span data-stu-id="c2dac-190"><strong>Empty</strong> – The amount will be 0 (zero).</span></span></li>
<li><span data-ttu-id="c2dac-191"><strong>Wertmäßiger Einstandsbetrag</strong> – Der Betrag entspricht dem wertmäßigen Einstandsbetrag.</span><span class="sxs-lookup"><span data-stu-id="c2dac-191"><strong>Financial cost amount</strong> – The amount will be equal to the financial cost.</span></span></li>
<li><span data-ttu-id="c2dac-192"><strong>Gesamtkosten</strong> – Der Betrag entspricht die Gesamtkosten der Buchung.</span><span class="sxs-lookup"><span data-stu-id="c2dac-192"><strong>Total cost</strong> – The amount will be equal to the total cost of the transaction.</span></span></li>
<li><span data-ttu-id="c2dac-193"><strong>Manuell</strong> – Der Betrag entspricht dem Betrag, der manuell auf der Umlagerungsauftragsposition angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="c2dac-193"><strong>Manual</strong> – The amount will be equal to the amount that is manually specified on the transfer order line.</span></span></li>
</ul></li>
<li><span data-ttu-id="c2dac-194">Für Aufträge und Bestellungen richten Sie eine der folgenden Regeln für die Berechnung der Rechnungsbeträge und statistischen Beträgen ein:</span><span class="sxs-lookup"><span data-stu-id="c2dac-194">For sales orders and purchase orders, you set up one of the following rules for calculating invoice amounts and statistical amounts:</span></span>
<ul>
<li><span data-ttu-id="c2dac-195"><strong>Leer</strong> – Der Betrag ist 0 (Null).</span><span class="sxs-lookup"><span data-stu-id="c2dac-195"><strong>Empty</strong> – The amount will be 0 (zero).</span></span></li>
<li><span data-ttu-id="c2dac-196"><strong>Rechnungsbetrag</strong> - Der Betrag entspricht dem Betrag, der für die Ware in Rechnung gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="c2dac-196"><strong>Invoice amount</strong> – The amount will be equal to the amount that is invoiced for the commodity.</span></span></li>
<li><span data-ttu-id="c2dac-197"><strong>Grundbetrag</strong> - Der Betrag entspricht dem Betrag, der gestellt werden, bevor einer beliebigen Rabatt angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="c2dac-197"><strong>Base amount</strong> – The amount will be equal to the amount that would be invoiced before any discount is applied.</span></span></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c2dac-198">Transportmethoden</span><span class="sxs-lookup"><span data-stu-id="c2dac-198">Transport methods</span></span></td>
<td><span data-ttu-id="c2dac-199">Richten Sie den Transportmodus gemäß den Anforderungen Ihres Landes/Ihrer Region ein.</span><span class="sxs-lookup"><span data-stu-id="c2dac-199">Set up the transport mode according to your country's/region's requirements.</span></span> <span data-ttu-id="c2dac-200">Für jede Lieferart können Sie eine standardmäßige Transportmethode auf der Registerkarte <strong>Außenhandel</strong> einrichten.</span><span class="sxs-lookup"><span data-stu-id="c2dac-200">For each delivery mode, you can set up a default transport method on the <strong>Foreign trade</strong> tab.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c2dac-201">Ports</span><span class="sxs-lookup"><span data-stu-id="c2dac-201">Ports</span></span></td>
<td><span data-ttu-id="c2dac-202">Richten Sie den Hafen/Flughafen des Ladens/Entladens ein, wenn diese Informationen von Ihrem Land/Ihrer Region erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="c2dac-202">Set up the port/airport of loading/unloading if this information is collected by your country/region.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c2dac-203">Statistikverfahren</span><span class="sxs-lookup"><span data-stu-id="c2dac-203">Statistics procedures</span></span></td>
<td><span data-ttu-id="c2dac-204">Richten Sie die Statistikverfahren ein, wenn diese Informationen von Ihrem Land/Ihrer Region erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="c2dac-204">Set up the statistical procedure if this information is collected by your country/region.</span></span></td>
</tr>
</tbody>
</table>

### <a name="set-up-rules-for-compressing-intrastat-transactions"></a><span data-ttu-id="c2dac-205">Einrichten von Regeln zur Komprimierung von Intrastat-Transaktionen</span><span class="sxs-lookup"><span data-stu-id="c2dac-205">Set up rules for compressing Intrastat transactions</span></span>

<span data-ttu-id="c2dac-206">Auf der **Komprimierung von Intrastat** Seite können Sie die Felder festlegen, die für die Komprimierung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="c2dac-206">On the **Compression of Intrastat** page, you can select the fields to use for compression.</span></span> <span data-ttu-id="c2dac-207">Alle Buchungen, die eine identische Kombination von Werten für die ausgewählten Felder in der Intrastat-Erfassung haben, werden in eine einzige Buchung komprimiert, wenn Sie die Komprimierungsfunktion in der Intrastat-Erfassung ausführen.</span><span class="sxs-lookup"><span data-stu-id="c2dac-207">All transactions that have the same combination of values for the selected fields in the Intrastat journal will be compressed into a single transaction when you run the Compress function in the Intrastat journal.</span></span>

### <a name="set-up-foreign-trade-parameters"></a><span data-ttu-id="c2dac-208">Außenhandelsparameter einrichten</span><span class="sxs-lookup"><span data-stu-id="c2dac-208">Set up foreign trade parameters</span></span>

<span data-ttu-id="c2dac-209">Verwenden Sie die **Außenhandelsparameter** Seite, um die Parameter in der folgenden Tabelle einzurichten.</span><span class="sxs-lookup"><span data-stu-id="c2dac-209">Use the **Foreign trade parameters** page to set up the parameters in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c2dac-210">Registerkarte</span><span class="sxs-lookup"><span data-stu-id="c2dac-210">Tab</span></span></th>
<th><span data-ttu-id="c2dac-211">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2dac-211">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c2dac-212">Allgemeines</span><span class="sxs-lookup"><span data-stu-id="c2dac-212">General</span></span></td>
<td><ul>
<li><span data-ttu-id="c2dac-213"><strong>Allgemein</strong> – Geben Sie die folgenden Informationen ein:</span><span class="sxs-lookup"><span data-stu-id="c2dac-213"><strong>General</strong> – Specify the following information:</span></span>
<ul>
<li><span data-ttu-id="c2dac-214">Die Standardtransaktionscodes für Aufträge, Bestellungen, Gutschriften und Umlagerungsaufträge.</span><span class="sxs-lookup"><span data-stu-id="c2dac-214">The default transaction codes for sales orders, purchase orders, credit notes, and transfer orders.</span></span> <span data-ttu-id="c2dac-215">Der Buchungscode, der für Gutschriften eingerichtet wurde, wird auch als Code für die Rückgabe physischer Waren und zur Ermittlung der Abweichung von physischer Rückgaben gegenüber Korrekturgutschriften verwendet.</span><span class="sxs-lookup"><span data-stu-id="c2dac-215">The transaction code that is set up for credit notes is also used as the code for physical goods return and is used for deviating physical returns versus correction credit notes.</span></span></li>
<li><span data-ttu-id="c2dac-216">Der Mitarbeiter, der für die Vorbereitung von Intrastat-Berichten zuständig ist.</span><span class="sxs-lookup"><span data-stu-id="c2dac-216">The employee who is responsible for preparing Intrastat reports.</span></span></li>
</ul></li>
<li><span data-ttu-id="c2dac-217"><strong>Untergrenze</strong> - Geben Sie die Einstellungen für die Aktualisierung von Buchungen an, die unter dem Schwellenwert sind:</span><span class="sxs-lookup"><span data-stu-id="c2dac-217"><strong>Minimum limit</strong> – Specify the settings for updating transactions that are below the threshold:</span></span>
<ul>
<li><span data-ttu-id="c2dac-218">Der Schwellenbetrag und das Gewicht</span><span class="sxs-lookup"><span data-stu-id="c2dac-218">The threshold amount and weight</span></span></li>
<li><span data-ttu-id="c2dac-219">Der Warencode, der auf Buchungen angewendet werden soll, die unter dem Schwellenwert sind</span><span class="sxs-lookup"><span data-stu-id="c2dac-219">The commodity code to apply to transactions that are under the threshold</span></span></li>
</ul></li>
<li><span data-ttu-id="c2dac-220"><strong>Übertragen</strong> - Geben Sie die Kriterien für die Übertragung von Buchungen zur Intrastat-Erfassung an.</span><span class="sxs-lookup"><span data-stu-id="c2dac-220"><strong>Transfer</strong> – Specify the criteria for transferring transactions to the Intrastat journal.</span></span> <span data-ttu-id="c2dac-221">Sie können angeben, dass Posten gebucht werden, wenn die Artikel eine oder alle der folgenden Kriterien erfüllen:</span><span class="sxs-lookup"><span data-stu-id="c2dac-221">You can specify that transactions are transferred only when the items meet one or all of the following criteria:</span></span>
<ul>
<li><span data-ttu-id="c2dac-222">Die Artikel sind keine Dienstleistungsartikel.</span><span class="sxs-lookup"><span data-stu-id="c2dac-222">The items aren't service items.</span></span></li>
<li><span data-ttu-id="c2dac-223">Die Artikel haben einen Warencode.</span><span class="sxs-lookup"><span data-stu-id="c2dac-223">The items have a commodity code.</span></span></li>
<li><span data-ttu-id="c2dac-224">Die Artikel werden ein Gewicht.</span><span class="sxs-lookup"><span data-stu-id="c2dac-224">The items have a weight.</span></span></li>
<li><span data-ttu-id="c2dac-225">Die Artikel haben besonderer Maßeinheiten.</span><span class="sxs-lookup"><span data-stu-id="c2dac-225">The items have additional units.</span></span></li>
</ul></li>
<li><span data-ttu-id="c2dac-226"><strong>Einstellungen prüfen</strong> - Geben Sie die Regeln für die Überprüfung der Vollständigkeit von Intrastat-Daten an.</span><span class="sxs-lookup"><span data-stu-id="c2dac-226"><strong>Check setup</strong> – Specify the rules for validating the completeness of Intrastat data.</span></span> <span data-ttu-id="c2dac-227">Sie können auswählen, welche Daten geprüft werden.</span><span class="sxs-lookup"><span data-stu-id="c2dac-227">You can select which data is validated.</span></span></li>
<li><span data-ttu-id="c2dac-228"><strong>Rundungsregeln</strong> - Geben Sie die folgenden Einstellungen für Rundungsbeträge und Gewichten im Intrastat-Bericht an:</span><span class="sxs-lookup"><span data-stu-id="c2dac-228"><strong>Rounding rules</strong> – Specify the following settings for rounding amounts and weights in Intrastat reporting:</span></span>
<ul>
<li><span data-ttu-id="c2dac-229">Die Rundungsregel (Genauigkeit)</span><span class="sxs-lookup"><span data-stu-id="c2dac-229">The rounding rule (precision)</span></span></li>
<li><span data-ttu-id="c2dac-230">Die Rundungsmethode: aufrunden, abrunden oder normal</span><span class="sxs-lookup"><span data-stu-id="c2dac-230">The rounding method: up, down, or normal</span></span></li>
<li><span data-ttu-id="c2dac-231">Die Anzahl von Dezimalstellen für Beträge und Gewichten</span><span class="sxs-lookup"><span data-stu-id="c2dac-231">The number of decimal places for amounts and weights</span></span></li>
<li><span data-ttu-id="c2dac-232">Anweisungen für das Runden von Gewichtungen, die kleiner als 1 Kilogramm (kg) sind: bis 1 kg, normal oder keine Rundung</span><span class="sxs-lookup"><span data-stu-id="c2dac-232">Instructions for rounding weights that are less than 1 kilogram (kg): up to 1 kg, normal, or no rounding</span></span></li>
</ul></li>
<li><span data-ttu-id="c2dac-233"><strong>Elektronische Berichterstellung</strong> - Geben Sie Referenzen auf elektronische Berichterstellungskonfigurationen an, mit denen Sie eine Datei und einen Bericht generieren können.</span><span class="sxs-lookup"><span data-stu-id="c2dac-233"><strong>Electronic reporting</strong> – Specify references to electronic reporting configurations, so that you can generate an electronic file and report.</span></span></li>
<li><span data-ttu-id="c2dac-234"><strong>Warencodehierarchie</strong> - Geben Sie die Kategoriehierarchie vom <strong>Warencode</strong>-Typ an, der den Intrastat-Warencode CN8 darstellt.</span><span class="sxs-lookup"><span data-stu-id="c2dac-234"><strong>Commodity code hierarchy</strong> – Specify the category hierarchy of the <strong>Commodity code</strong> type that represents Intrastat commodity code CN8.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c2dac-235">Kontaktinformationen des Beauftragten</span><span class="sxs-lookup"><span data-stu-id="c2dac-235">Agent contact information</span></span></td>
<td><span data-ttu-id="c2dac-236">Geben Sie Name, Adresse, die Umsatzsteuernummer, Telefonnummer und die Faxnummer des Agenten an.</span><span class="sxs-lookup"><span data-stu-id="c2dac-236">Specify the agent's name, address, tax exempt number, telephone number, and fax number.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c2dac-237">Länder-/Regionseigenschaften</span><span class="sxs-lookup"><span data-stu-id="c2dac-237">Country/region properties</span></span></td>
<td><span data-ttu-id="c2dac-238">Legen Sie das Land/die Region der aktuellen juristischen Person auf <strong>Inland</strong> fest.</span><span class="sxs-lookup"><span data-stu-id="c2dac-238">Set the country/region of the current legal entity to <strong>Domestic</strong>.</span></span> <span data-ttu-id="c2dac-239">Festlegen des Lands oder einer Region aus EU-Ländern/Regionen, die am EU-Handel mit der aktuellen juristischen Person mit <strong>EU</strong> teilnehmen.</span><span class="sxs-lookup"><span data-stu-id="c2dac-239">Set the country/region of EU countries/regions that participate in EU trade with the current legal entity to <strong>EU</strong>.</span></span> <span data-ttu-id="c2dac-240">Für jedes Land/Region kennzeichnen Sie auch Länder-/Regionscode zu den Außenhandelzwecken.</span><span class="sxs-lookup"><span data-stu-id="c2dac-240">For each country/region, you also identify country/region code for foreign trade purposes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c2dac-241">Nummernkreis</span><span class="sxs-lookup"><span data-stu-id="c2dac-241">Number sequence</span></span></td>
<td><span data-ttu-id="c2dac-242">Geben Sie hier den Kennungscode für die Intrastat-Erfassung an.</span><span class="sxs-lookup"><span data-stu-id="c2dac-242">Specify the number sequence for the Intrastat journal.</span></span></td>
</tr>
</tbody>
</table>

 




