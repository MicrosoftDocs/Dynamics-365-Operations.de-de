---
title: Übersicht über die indische Quellenbesteuerung (TDS)
description: Dieses Thema enthält detaillierte Informationen zur indischen Quellenbesteuerung (TDS). Die TDS-Dokumentation behandelt die Funktionalität dieser Funktion.
author: kailiang
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 28ee843036e11bd37b97a065ce53d2eb860c79d9
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023281"
---
# <a name="indian-tax-deducted-at-source-tds-overview"></a><span data-ttu-id="4e16f-104">Übersicht über die indische Quellenbesteuerung (TDS)</span><span class="sxs-lookup"><span data-stu-id="4e16f-104">Indian Tax Deducted at Source (TDS) overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4e16f-105">Dieses Thema enthält detaillierte Informationen zur indischen Quellenbesteuerung (TDS).</span><span class="sxs-lookup"><span data-stu-id="4e16f-105">This topic provides detailed information about Indian Tax Deducted at Source (TDS).</span></span>

<span data-ttu-id="4e16f-106">Die TDS-Dokumentation behandelt die Funktionalität dieser Funktion.</span><span class="sxs-lookup"><span data-stu-id="4e16f-106">The TDS documentation covers the functionality of this capability.</span></span> <span data-ttu-id="4e16f-107">Außerdem wird erläutert, wie Sie die Grundeinstellungen für TDS festlegen, TDS für Buchungen berechnen, den TDS-Ausgleichsprozess durchführen, TDS-Zertifikatsnummern aufzeichnen und TDS-Anfragen, TDS-Erklärungen und TDS-Zertifikate generieren.</span><span class="sxs-lookup"><span data-stu-id="4e16f-107">It also explains how to do the basic setup for TDS, calculate TDS on transactions, complete the TDS settlement process, record TDS certificate numbers, and generate TDS inquiries, TDS statements, and TDS certificates.</span></span> <span data-ttu-id="4e16f-108">Die Dokumentation enthält die folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="4e16f-108">The documentation includes the following topics:</span></span>

- [<span data-ttu-id="4e16f-109">Grundeinstellungen für TDS</span><span class="sxs-lookup"><span data-stu-id="4e16f-109">Basic setup for TDS</span></span>](apac-ind-TDS-TDS-ledger-accounts-setup.md)
- [<span data-ttu-id="4e16f-110">Formeldesigner und Schwellenwertfunktionalität für die TDS-Berechnung</span><span class="sxs-lookup"><span data-stu-id="4e16f-110">Formula designer and threshold limit functionality used for TDS calculation</span></span>](apac-ind-TDS-Formula-designer.md)
- [<span data-ttu-id="4e16f-111">TDS-Berechnung für Rechnungen, Zahlungen, Solawechsel und Intercompany-Buchungen</span><span class="sxs-lookup"><span data-stu-id="4e16f-111">Calculation of TDS on invoices, payments, promissory notes, and intercompany transactions</span></span>](apac-ind-TDS-Calculate-TDS-on-invoices-using-journals.md)
- [<span data-ttu-id="4e16f-112">Der periodische TDS-Ausgleichsprozess und der Ausgleich von TDS-Beträgen gegenüber Behördenkreditoren</span><span class="sxs-lookup"><span data-stu-id="4e16f-112">Periodic TDS settlement process and settlement of TDS amounts to TDS authority vendors</span></span>](apac-ind-TDS-Run-the-periodic-TDS-settlement-process.md)
- [<span data-ttu-id="4e16f-113">TDS-Zertifikatsnummern und -daten aufzeichnen und aktualisieren</span><span class="sxs-lookup"><span data-stu-id="4e16f-113">Recording and updating TDS certificate numbers and dates</span></span>](apac-ind-TDS-Record-TDS-concession-certificate-numbers.md)

## <a name="introduction-to-tds"></a><span data-ttu-id="4e16f-114">Einführung in TDS</span><span class="sxs-lookup"><span data-stu-id="4e16f-114">Introduction to TDS</span></span>

<span data-ttu-id="4e16f-115">Gemäß dem Einkommensteuergesetz von 1961 wird die Einkommensteuer vom Empfänger der Dienstleistung zum Zeitpunkt der Vorauszahlung oder der Verbuchung der Gutschrift an der Quelle abgezogen, je nachdem, was zuerst eintritt.</span><span class="sxs-lookup"><span data-stu-id="4e16f-115">Per the Income tax Act, 1961, income tax is deducted at the source by the receiver of the service at the time of advance payment or accounting of credit, whichever occurs first.</span></span> <span data-ttu-id="4e16f-116">Wer die Zahlung leistet, muss den Steuerbetrag abziehen und nur den Nettosaldo an den Dienstleister zahlen.</span><span class="sxs-lookup"><span data-stu-id="4e16f-116">The person who makes the payment must deduct the tax amount and pay only the net balance to the provider of the service.</span></span> <span data-ttu-id="4e16f-117">TDS wird auf staatlich festgelegte Dienstleistungen angewendet, und die Steuer wird unter Verwendung der vom Staat für einen bestimmten Zeitraum festgelegten Sätze abgezogen.</span><span class="sxs-lookup"><span data-stu-id="4e16f-117">TDS is applied on services that the government specifies, and the tax is deducted by using the rates that the government specifies for a period.</span></span> <span data-ttu-id="4e16f-118">Der Abzugssatz basiert auf dem Status der Entität, die die Zahlung erhält oder die Dienstleistung erbringt.</span><span class="sxs-lookup"><span data-stu-id="4e16f-118">The rate of deduction is based on the status of the entity that receives the payment or provides the service.</span></span> <span data-ttu-id="4e16f-119">Mögliche Status sind unter anderem **Einzelperson**, **Ungeteilte Hindufamilie** (**HUF**), **Unternehmen**, **Firma**, **Personenverband** (**AOP**), **Personenzusammenschluss** (**BOI**) und **Gemeinde**.</span><span class="sxs-lookup"><span data-stu-id="4e16f-119">Statuses include **Individual**, **Hindu Undivided Family** (**HUF**), **Company**, **Firm**, **Association of Persons** (**AOP**), **Body of Individuals** (**BOI**), and **Local authority**.</span></span>

<span data-ttu-id="4e16f-120">In den folgenden Abschnitten werden die Dienste aufgeführt, auf die TDS, wie vom indischen Staat festgelegt, angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="4e16f-120">The following sections list the services that TDS is applied on, as specified by the Government of India.</span></span>

<span data-ttu-id="4e16f-121">**Einwohner**</span><span class="sxs-lookup"><span data-stu-id="4e16f-121">**Residents**</span></span>

- <span data-ttu-id="4e16f-122">Einkommen aus Gehältern (gemäß § 192)</span><span class="sxs-lookup"><span data-stu-id="4e16f-122">Income from salaries (Under section 192)</span></span>
- <span data-ttu-id="4e16f-123">Zinserträge aus Wertpapieren (gemäß § 193)</span><span class="sxs-lookup"><span data-stu-id="4e16f-123">Income from interest on securities (Under section 193)</span></span>
- <span data-ttu-id="4e16f-124">Dividendenerträge (gemäß § 194)</span><span class="sxs-lookup"><span data-stu-id="4e16f-124">Income from dividend (Under section 194)</span></span>
- <span data-ttu-id="4e16f-125">Zinserträge (gemäß § 194A)</span><span class="sxs-lookup"><span data-stu-id="4e16f-125">Income from interest (Under section 194A)</span></span>
- <span data-ttu-id="4e16f-126">Einkünfte aus Lotterien oder Gewinnspielen (gemäß § 194B)</span><span class="sxs-lookup"><span data-stu-id="4e16f-126">Income from lotteries or puzzles (Under section 194B)</span></span>
- <span data-ttu-id="4e16f-127">Gewinne von Pferderennen usw. (gemäß § 194BB)</span><span class="sxs-lookup"><span data-stu-id="4e16f-127">Winning from horse races etc. (Under section 194BB)</span></span>
- <span data-ttu-id="4e16f-128">Auftragnehmer und Unterauftragnehmer (gemäß § 194C)</span><span class="sxs-lookup"><span data-stu-id="4e16f-128">Contractors and sub-contractors (Under section 194C)</span></span>
- <span data-ttu-id="4e16f-129">Versicherungsprovisionen (gemäß § 194D)</span><span class="sxs-lookup"><span data-stu-id="4e16f-129">Insurance commission (Under section 194D)</span></span>
- <span data-ttu-id="4e16f-130">Einkünfte aus Einlagen in den nationalen Sparplan (gemäß § 194EE)</span><span class="sxs-lookup"><span data-stu-id="4e16f-130">Income from deposit under national saving scheme (Under section 194EE)</span></span>
- <span data-ttu-id="4e16f-131">Erträge aus Investmentfonds oder UTI (gemäß § 194F)</span><span class="sxs-lookup"><span data-stu-id="4e16f-131">Income from mutual fund or UTI (Under section 194F)</span></span>
- <span data-ttu-id="4e16f-132">Provisionen, Honorare, Preise usw. aus einem Verkauf oder einer Lotterie (gemäß § 194G)</span><span class="sxs-lookup"><span data-stu-id="4e16f-132">Commission, Remuneration, Prize etc., on sale or lottery (Under section 194G)</span></span>
- <span data-ttu-id="4e16f-133">Zahlung von Provisionen oder Maklergebühren (gemäß § 194H)</span><span class="sxs-lookup"><span data-stu-id="4e16f-133">Payment of Commission or brokerage (Under section 194H)</span></span>
- <span data-ttu-id="4e16f-134">Miete (gemäß § 194I)</span><span class="sxs-lookup"><span data-stu-id="4e16f-134">Rent (Under section 194I)</span></span>
- <span data-ttu-id="4e16f-135">Fachliche Dienstleistungen (gemäß § 194J)</span><span class="sxs-lookup"><span data-stu-id="4e16f-135">Professional service (Under section 194J)</span></span>
- <span data-ttu-id="4e16f-136">Einkommen aus Anteilen (gemäß § 194K)</span><span class="sxs-lookup"><span data-stu-id="4e16f-136">Income from Units (Under section 194K)</span></span>
- <span data-ttu-id="4e16f-137">Zahlung einer Entschädigung beim Erwerb bestimmter Immobilien (gemäß § 194LA)</span><span class="sxs-lookup"><span data-stu-id="4e16f-137">Payment of compensation on acquisition of certain immovable property (Under section 194LA)</span></span>

<span data-ttu-id="4e16f-138">**Nicht ansässige Personen**</span><span class="sxs-lookup"><span data-stu-id="4e16f-138">**Non-residents**</span></span>

- <span data-ttu-id="4e16f-139">Zahlungen an nicht ansässige Sportler oder Sportverbände (gemäß § 194E)</span><span class="sxs-lookup"><span data-stu-id="4e16f-139">Payments to Non-resident sportsmen or sports association (Under section 194E)</span></span>
- <span data-ttu-id="4e16f-140">Andere Beträge (unter § 195)</span><span class="sxs-lookup"><span data-stu-id="4e16f-140">Other sums (Under section 195)</span></span>
- <span data-ttu-id="4e16f-141">Einkommen in Bezug auf Anteilen von nicht ansässigen Personen (gemäß § 196A)</span><span class="sxs-lookup"><span data-stu-id="4e16f-141">Income in respect of units of non-residents (Under section 196A)</span></span>

    - <span data-ttu-id="4e16f-142">Erträge aus Anleihen oder Aktien eines indischen Unternehmens in einer Fremdwährung (gemäß § 196C)</span><span class="sxs-lookup"><span data-stu-id="4e16f-142">Income from foreign currency bonds or shares of Indian Company (Under section 196C)</span></span>
    - <span data-ttu-id="4e16f-143">Erträge ausländischer institutioneller Anleger aus Wertpapieren (gemäß § 196D)</span><span class="sxs-lookup"><span data-stu-id="4e16f-143">Incomes of foreign institutional investors from securities (Under section 196D)</span></span>
    - <span data-ttu-id="4e16f-144">Gehälter und alle anderen positiven Einkommen unter einer Einkommensüberschrift (§ 192)</span><span class="sxs-lookup"><span data-stu-id="4e16f-144">Salary and all other positive incomes under any head on income (Section 192)</span></span>
    - <span data-ttu-id="4e16f-145">Zinsen auf Wertpapiere (§ 193)</span><span class="sxs-lookup"><span data-stu-id="4e16f-145">Interest on securities (Section 193)</span></span>
    - <span data-ttu-id="4e16f-146">Andere Zinsen als Zinsen auf Wertpapiere (§ 194A)</span><span class="sxs-lookup"><span data-stu-id="4e16f-146">Interest other than interest on securities (Section 194A)</span></span>
    - <span data-ttu-id="4e16f-147">Zahlungen an Auftragnehmer und Unterauftragnehmer (§ 194C)</span><span class="sxs-lookup"><span data-stu-id="4e16f-147">Payments to contractors and sub-contractors (Section 194C)</span></span>
    - <span data-ttu-id="4e16f-148">Gewinne aus Lotterien oder Kreuzworträtseln (§ 194B)</span><span class="sxs-lookup"><span data-stu-id="4e16f-148">Winnings from Lottery or crossword puzzles (Section 194B)</span></span>
    - <span data-ttu-id="4e16f-149">Gewinne aus Pferderennen (§ 194BB)</span><span class="sxs-lookup"><span data-stu-id="4e16f-149">Winnings from horse races (Section 194BB)</span></span>
    - <span data-ttu-id="4e16f-150">Versicherungsprovisionen für alle Zahlungen für den Erwerb eines Versicherungsabschlusses (§ 194D)</span><span class="sxs-lookup"><span data-stu-id="4e16f-150">Insurance Commission covering all payments for procuring Insurance business (Section 194D)</span></span>
    - <span data-ttu-id="4e16f-151">Alle anderen Zinsen als Zinsen auf Wertpapiere, die an nicht ansässige Personen, die kein Unternehmen sind, oder ausländische Unternehmen zu zahlen sind (§ 195)</span><span class="sxs-lookup"><span data-stu-id="4e16f-151">Any interest other than interest on securities payable to non-residents not being a company or to a foreign company (Section 195)</span></span>
    - <span data-ttu-id="4e16f-152">Zahlung an einen nicht ansässigen Sportler, einschließlich Sportler, Sportverbände oder -einrichtungen.</span><span class="sxs-lookup"><span data-stu-id="4e16f-152">Payment to non-resident sportsman including athlete or sports association or institution.</span></span> <span data-ttu-id="4e16f-153">Im Falle eines nicht ansässigen Sportlers sind Zahlungen in Bezug auf Werbung sowie Artikel zu Spielen/Sportarten in Indien in Zeitungen, Zeitschriften usw.</span><span class="sxs-lookup"><span data-stu-id="4e16f-153">In case of non-resident sportsman, payments in respect of advertisements as well as articles on any game/sports in India in newspapers, magazines, and so.</span></span> <span data-ttu-id="4e16f-154">enthalten (§ 194E).</span><span class="sxs-lookup"><span data-stu-id="4e16f-154">is included (Section 194E)</span></span>
    - <span data-ttu-id="4e16f-155">Zahlung für Einlagen im Rahmen des NSS \[nationaler Sparplan\] (§ 194EE)</span><span class="sxs-lookup"><span data-stu-id="4e16f-155">Payment in respect of deposits under NSS \[National Savings Scheme\] (Section 194EE)</span></span>
    - <span data-ttu-id="4e16f-156">Zahlungen aufgrund des Rückkaufs von Anteilen durch Investmentfonds oder UTI (§ 194F)</span><span class="sxs-lookup"><span data-stu-id="4e16f-156">Payment on account of repurchase of Units by Mutual Fund or UTI (Section 194F)</span></span>
    - <span data-ttu-id="4e16f-157">Zahlungen für Provisionen oder Maklergebühren (§ 194H)</span><span class="sxs-lookup"><span data-stu-id="4e16f-157">Payment for Commission or brokerage (Section 194H)</span></span>
    - <span data-ttu-id="4e16f-158">Mietzahlungen (§ 194I)</span><span class="sxs-lookup"><span data-stu-id="4e16f-158">Payment of rent (Section 194I)</span></span>
    - <span data-ttu-id="4e16f-159">Zahlung von Gebühren für fachliche oder technische Dienstleistungen (§ 194J)</span><span class="sxs-lookup"><span data-stu-id="4e16f-159">Payment of fees for professional or technical services (Section 194J)</span></span>
    - <span data-ttu-id="4e16f-160">Provision an Fachhändler, Händler, Käufer und Verkäufer von Lottoscheinen einschließlich Vergütungen oder Preise für solche Scheine (§ 194G)</span><span class="sxs-lookup"><span data-stu-id="4e16f-160">Commission to Stockiest, distributors, buyers and sellers of Lottery tickets including remuneration or prize on such tickets (Section 194G)</span></span>
    - <span data-ttu-id="4e16f-161">Erträge aus in Fremdwährung gekauften Anteilen oder langfristige Kapitalgewinn aus der Übertragung solcher in Fremdwährung erworbenen Anteile (§ 196B)</span><span class="sxs-lookup"><span data-stu-id="4e16f-161">Income from Units purchased in foreign currency or long-term capital gain arising from the transfer of such Units purchased in foreign currency (Section 196B)</span></span>
    - <span data-ttu-id="4e16f-162">Zahlung von Erträgen an nicht ansässige Personen in Bezug auf Zinsen oder Dividenden auf Anleihen und Aktien (§ 196C)</span><span class="sxs-lookup"><span data-stu-id="4e16f-162">Payment of any income to non-residents in respect of interest or dividend on bonds and shares (Section 196C)</span></span>

<span data-ttu-id="4e16f-163">Die TDS wird für Käufe, Verkäufe, Rücksendungen, Gutschriften, Anschaffungen von Anlagen, Vorauszahlungen, Anzahlungen, Solawechsel, Einkommen und Intercompany-Buchungen berechnet.</span><span class="sxs-lookup"><span data-stu-id="4e16f-163">TDS is calculated on purchases, sales, sales returns, credit notes, fixed asset acquisitions, prepayments, advance payments, promissory notes, works tax, and intercompany transactions.</span></span>

> [!NOTE]
> <span data-ttu-id="4e16f-164">Im indischen Steuerszenario wird TDS derzeit für Verkaufstransaktionen nicht berechnet.</span><span class="sxs-lookup"><span data-stu-id="4e16f-164">In the current Indian tax scenario, TDS isn't calculated on sales transactions.</span></span> <span data-ttu-id="4e16f-165">Das System enthält jedoch eine Bestimmung zur Berechnung der TDS, die bei Verkaufstransaktionen, insbesondere bei Intercompany-Buchungen, erstattungsfähig ist.</span><span class="sxs-lookup"><span data-stu-id="4e16f-165">However, the system includes a provision to calculate TDS recoverable on sales transactions, especially for intercompany transactions.</span></span>

<span data-ttu-id="4e16f-166">Bei der Berechnung der TDS werden immer der Schwellenwert und der Ausnahmeschwellenwert berücksichtigt, die für die TDS-Komponente festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="4e16f-166">The calculation of TDS always considers the threshold and the exception threshold that are defined for the TDS component.</span></span>

<span data-ttu-id="4e16f-167">Der periodische TDS-Ausgleichsprozess muss ausgeführt werden, und die TDS-Zahlungen müssen gegenüber TDS-Behördenkreditoren ausgeglichen werden.</span><span class="sxs-lookup"><span data-stu-id="4e16f-167">The periodic TDS settlement process must be run, and the TDS payments must be settled to TDS authority vendors.</span></span>

<span data-ttu-id="4e16f-168">Die Zertifikatsnummern und -daten für TDS-Zertifikate, die von Kreditoren oder Debitoren empfangen werden, können aufgezeichnet und aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="4e16f-168">The certificate numbers and dates for TDS certificates that are received from vendors or customers can be recorded and updated.</span></span> <span data-ttu-id="4e16f-169">Darüber hinaus können in Finance die Formulare 26Q und 27Q für die vierteljährlichen Erklärungen sowie das Zertifikat Formular 16A erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="4e16f-169">Additionally, Form 26Q and Form 27Q quarterly statements, and the Form 16A certificate for TDS, can be generated in Finance.</span></span>

## <a name="setting-up-and-working-with-tds"></a><span data-ttu-id="4e16f-170">TDS einrichten und damit arbeiten</span><span class="sxs-lookup"><span data-stu-id="4e16f-170">Setting up and working with TDS</span></span>

<span data-ttu-id="4e16f-171">Hier finden Sie eine Übersicht, wie Sie TDS einrichten und damit arbeiten:</span><span class="sxs-lookup"><span data-stu-id="4e16f-171">Here is an overview of the process for setting up and working with TDS:</span></span>

1. <span data-ttu-id="4e16f-172">**TDS-Setup:**</span><span class="sxs-lookup"><span data-stu-id="4e16f-172">**TDS setup:**</span></span>

    - <span data-ttu-id="4e16f-173">Parametereinstellungen:</span><span class="sxs-lookup"><span data-stu-id="4e16f-173">Parameter setup:</span></span>

        - <span data-ttu-id="4e16f-174">Aktivieren Sie unter Hauptbuchparameter Parameter, die mit TDS zusammenhängen.</span><span class="sxs-lookup"><span data-stu-id="4e16f-174">In General ledger parameters, activate parameters that are related to TDS.</span></span>
        - <span data-ttu-id="4e16f-175">Richten Sie unter Hauptbuchparameter die Nummernkreise für Quellensteuerzahlungen ein.</span><span class="sxs-lookup"><span data-stu-id="4e16f-175">In General ledger parameters, set up the number sequence for withholding tax payments.</span></span>
        - <span data-ttu-id="4e16f-176">Richten Sie Parameter für Kreditoren und Debitoren ein.</span><span class="sxs-lookup"><span data-stu-id="4e16f-176">Set up parameters in Accounts payable and Accounts receivable.</span></span>

    - <span data-ttu-id="4e16f-177">Grundeinstellungen:</span><span class="sxs-lookup"><span data-stu-id="4e16f-177">Basic setup:</span></span>

        - <span data-ttu-id="4e16f-178">Richten Sie TDS-Registrierungsnummern für Unternehmen, Debitoren und Kreditoren ein.</span><span class="sxs-lookup"><span data-stu-id="4e16f-178">Set up TDS registration numbers for a company, customers, and vendors.</span></span>
        - <span data-ttu-id="4e16f-179">Richten Sie TDS-Komponentengruppen ein.</span><span class="sxs-lookup"><span data-stu-id="4e16f-179">Set up TDS component groups.</span></span>
        - <span data-ttu-id="4e16f-180">Richten Sie TDS-Komponenten ein, verknüpfen Sie TDS-Komponentengruppen damit und definieren Sie den Schwellenwert sowie den Ausnahmeschwellenwert dafür.</span><span class="sxs-lookup"><span data-stu-id="4e16f-180">Set up TDS components, attach TDS component groups to them, and define the threshold and exception threshold for them.</span></span>
        - <span data-ttu-id="4e16f-181">Richten Sie TDS-Behörden ein.</span><span class="sxs-lookup"><span data-stu-id="4e16f-181">Set up TDS authorities.</span></span>
        - <span data-ttu-id="4e16f-182">Richten Sie TDS-Ausgleichsperioden ein.</span><span class="sxs-lookup"><span data-stu-id="4e16f-182">Set up TDS settlement periods.</span></span>
        - <span data-ttu-id="4e16f-183">Richten Sie TDS-Steuercodes ein und fügen Sie ihnen TDS-Komponenten hinzu.</span><span class="sxs-lookup"><span data-stu-id="4e16f-183">Set up TDS tax codes, and attach TDS components to them.</span></span>
        - <span data-ttu-id="4e16f-184">Richten Sie TDS-Steuergruppen ein und fügen Sie ihnen TDS-Steuercodes hinzu.</span><span class="sxs-lookup"><span data-stu-id="4e16f-184">Set up TDS tax groups, and attach TDS tax codes to them.</span></span>
        - <span data-ttu-id="4e16f-185">Legen Sie im Formeldesigner eine Formel zur Berechnung der TDS für eine TDS-Gruppe fest.</span><span class="sxs-lookup"><span data-stu-id="4e16f-185">In the formula designer, define a formula to calculate TDS for a TDS group.</span></span>
        - <span data-ttu-id="4e16f-186">Erfassen Sie die Nummern der TDS-Konzessionszertifikate.</span><span class="sxs-lookup"><span data-stu-id="4e16f-186">Record TDS concession certificate numbers.</span></span>

    - <span data-ttu-id="4e16f-187">Sachkonten und Unternehmen einrichten:</span><span class="sxs-lookup"><span data-stu-id="4e16f-187">Ledger accounts and company setup:</span></span>

        - <span data-ttu-id="4e16f-188">Richten sie Sachkonten für Debitoren und Kreditoren ein.</span><span class="sxs-lookup"><span data-stu-id="4e16f-188">Set up TDS payable and receivable ledger accounts.</span></span>
        - <span data-ttu-id="4e16f-189">Legen Sie eine Steuerabzugs- und Inkassokontonummer (TAN) und eine Kategorie des Abzugstyps für das Unternehmen fest.</span><span class="sxs-lookup"><span data-stu-id="4e16f-189">Set up a Tax Deduction and Collection Account Number (TAN) and a deductor type category for the company.</span></span>

    - <span data-ttu-id="4e16f-190">Andere Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="4e16f-190">Other setup:</span></span>

        - <span data-ttu-id="4e16f-191">Legen Sie einen Zahlungsplan fest, der die TDS-Zuteilung enthält.</span><span class="sxs-lookup"><span data-stu-id="4e16f-191">Set up a payment schedule that includes TDS allocation.</span></span>
        - <span data-ttu-id="4e16f-192">Legen Sie einen Zahlungsgebührentyp für Zahlungen an die TDS-Behörden fest.</span><span class="sxs-lookup"><span data-stu-id="4e16f-192">Set up a payment fee type for payments to the TDS authority.</span></span>
        - <span data-ttu-id="4e16f-193">Legen Sie Angaben zu TDS-Gruppen, Permanente Kontonummern (PANs) und TANs für Kreditoren und Debitoren fest.</span><span class="sxs-lookup"><span data-stu-id="4e16f-193">Set up information about TDS groups, permanent account numbers (PANs), and TANs for vendors and customers.</span></span>

2. <span data-ttu-id="4e16f-194">**Berechnung der TDS in Transaktionen:**</span><span class="sxs-lookup"><span data-stu-id="4e16f-194">**Calculation of TDS in transactions:**</span></span>

    - <span data-ttu-id="4e16f-195">Rechnungen und Zahlungen</span><span class="sxs-lookup"><span data-stu-id="4e16f-195">Invoices and payments</span></span>
    - <span data-ttu-id="4e16f-196">Solawechsel</span><span class="sxs-lookup"><span data-stu-id="4e16f-196">Promissory notes</span></span>
    - <span data-ttu-id="4e16f-197">Anzahlungen</span><span class="sxs-lookup"><span data-stu-id="4e16f-197">Advance payments</span></span>
    - <span data-ttu-id="4e16f-198">Vorauszahlungen</span><span class="sxs-lookup"><span data-stu-id="4e16f-198">Prepayments</span></span>

3. <span data-ttu-id="4e16f-199">**TDS-Ausgleich:**</span><span class="sxs-lookup"><span data-stu-id="4e16f-199">**TDS settlement:**</span></span>

    - <span data-ttu-id="4e16f-200">Periodischer TDS-Ausgleichsprozess</span><span class="sxs-lookup"><span data-stu-id="4e16f-200">Periodic TDS settlement process</span></span>
    - <span data-ttu-id="4e16f-201">Ausgleich von TDS-Zahlungen an TDS-Behördenkreditoren und Generierung von TDS-Challan</span><span class="sxs-lookup"><span data-stu-id="4e16f-201">Settlement of TDS payments to TDS authority vendors and generation of TDS challan</span></span>

4. <span data-ttu-id="4e16f-202">**TDS-Anfragen, -abrechnungen und -zertifikate:**</span><span class="sxs-lookup"><span data-stu-id="4e16f-202">**TDS inquiries, statements, and certificate:**</span></span>

    - <span data-ttu-id="4e16f-203">Zeichen Sie TDS-Zertifikatsnummern und -daten auf und aktualisieren Sie sie.</span><span class="sxs-lookup"><span data-stu-id="4e16f-203">Record and update TDS certificate numbers and dates.</span></span>
    - <span data-ttu-id="4e16f-204">Generieren Sie eine TDS-Anfrage und eine gebuchte TDS-Anfrage.</span><span class="sxs-lookup"><span data-stu-id="4e16f-204">Generate a TDS inquiry and a posted TDS inquiry.</span></span>
    - <span data-ttu-id="4e16f-205">Generieren Sie die Formulare 27A, 26Q und 27Q für die vierteljährliche TDS- und E-TDS-Erklärung.</span><span class="sxs-lookup"><span data-stu-id="4e16f-205">Generate Form 27A, Form 26Q, and Form 27Q TDS and e-TDS quarterly statements.</span></span>
    - <span data-ttu-id="4e16f-206">Generieren Sie ein TDS-Zertifikat des Formulars 16A.</span><span class="sxs-lookup"><span data-stu-id="4e16f-206">Generate a Form 16A TDS certificate.</span></span>
