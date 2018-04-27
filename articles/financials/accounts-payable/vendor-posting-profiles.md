---
title: Kreditoren-Buchungsprofile
description: "Händlerbuchungsprofile steuern die Buchung von Händlertransaktionen im Hauptbuch."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 24691
ms.assetid: 18def866-7655-4f0b-b299-eec83098d23a
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 3571726fd3603371b8e1daec7d6ebe85d72d280d
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---

# <a name="vendor-posting-profiles"></a><span data-ttu-id="7737f-103">Kreditoren-Buchungsprofile</span><span class="sxs-lookup"><span data-stu-id="7737f-103">Vendor posting profiles</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="7737f-104">Händlerbuchungsprofile steuern die Buchung von Händlertransaktionen im Hauptbuch.</span><span class="sxs-lookup"><span data-stu-id="7737f-104">Vendor posting profiles control the posting of vendor transactions to the general ledger.</span></span>

<a name="vendor-posting-profiles"></a><span data-ttu-id="7737f-105">Kreditoren-Buchungsprofile</span><span class="sxs-lookup"><span data-stu-id="7737f-105">Vendor posting profiles</span></span>
-----------------------

<span data-ttu-id="7737f-106">Kreditoren-Buchungsprofile ermöglichen das Zuweisen von Hauptbuchkonten und Dokumenteinstellungen zu allen Kreditoren, einer Kreditorengruppe oder einem bestimmten Kreditor.</span><span class="sxs-lookup"><span data-stu-id="7737f-106">Vendor posting profiles enable you to assign general ledger accounts and document settings to all vendors, a group of vendors or a single vendor.</span></span> <span data-ttu-id="7737f-107">Diese Einstellungen werden verwendet, wenn Sie Bestellungen, Kreditorenrechnungen und Barzahlungen erstellen.</span><span class="sxs-lookup"><span data-stu-id="7737f-107">These settings will be used when you create purchase orders, vendor invoices and cash payments.</span></span> <span data-ttu-id="7737f-108">Bei einigen Buchungen können Sie ein Buchungsprofil auswählen, das sich von den in diesem Formular für Buchungen eingerichteten Buchungsprofilen unterscheidet und Vorrang vor diesen hat.</span><span class="sxs-lookup"><span data-stu-id="7737f-108">For some transactions, you can select a posting profile that differs from and takes precedence over the posting profiles that are set up for transactions in this page.</span></span> <span data-ttu-id="7737f-109">Das Buchungsprofil wird im Sachkonto- und Mehrwertsteuer-Inforegister auf der Kreditorenparameterseite definiert.</span><span class="sxs-lookup"><span data-stu-id="7737f-109">The default posting profile is defined in the Ledger and Sales Tax fasttab on the Accounts payable parameters page.</span></span> <span data-ttu-id="7737f-110">Das Buchungsprofil wird dann automatisch in den Kopf neuer Dokumente einbezogen. Dort können es bei Bedarf zu einem anderen Buchungsprofil ändern.</span><span class="sxs-lookup"><span data-stu-id="7737f-110">The default posting profile is then included automatically on the header of new documents where you can change it to a different posting profile if needed.</span></span>

<span data-ttu-id="7737f-111">Sie können auch Buchungsdefinitionen zu Buchungsarten auf der Seite "Transaktionsbuchungsdefinitionen" zuordnen.</span><span class="sxs-lookup"><span data-stu-id="7737f-111">You can also associate posting definitions with transaction posting types in the Transaction posting definitions page.</span></span> <span data-ttu-id="7737f-112">Buchungsdefinitionen dienen zum Steuern von Kreditorenbuchungen auf das Hauptbuch anstelle von Buchungsprofilen.</span><span class="sxs-lookup"><span data-stu-id="7737f-112">Posting definitions control the posting of vendor transactions to the general ledger instead of posting profiles.</span></span>

## <a name="creating-a-posting-profile"></a><span data-ttu-id="7737f-113">Buchungsprofil erstellen</span><span class="sxs-lookup"><span data-stu-id="7737f-113">Creating a posting profile</span></span>
### <a name="setup"></a><span data-ttu-id="7737f-114">**Einstellungen**</span><span class="sxs-lookup"><span data-stu-id="7737f-114">**Setup**</span></span>

<span data-ttu-id="7737f-115">Hier können Sie die Sachkonten angeben, die bei Buchungen mit dem ausgewählten Buchungsprofil verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7737f-115">Specify the ledger accounts that are used in the posting of transactions that use the selected posting profile.</span></span> <span data-ttu-id="7737f-116">Wählen Sie einen Kontocode und ggf. eine Konto- oder Gruppennummer für das ausgewählte Buchungsprofil aus.</span><span class="sxs-lookup"><span data-stu-id="7737f-116">Select an account code and, whenever possible, an account or group number for the selected posting profile.</span></span> <span data-ttu-id="7737f-117">Während des Buchungsprozesses wird für jede Buchung das am besten geeignete Buchungsprofil gesucht. Hierzu wird nach einem möglichst spezifischen Kontocode, einer möglichst spezifischen Kontonummer oder nach einer möglichst spezifischen Kombination aus Gruppe und Nummer gesucht. Dabei gilt folgende Priorität:</span><span class="sxs-lookup"><span data-stu-id="7737f-117">In the posting process, the most appropriate posting profile for each transaction is located by searching for the most specific account code, account number, or group and number combination in the following priority:</span></span>

| <span data-ttu-id="7737f-118">**Kontocode**-Feldwert</span><span class="sxs-lookup"><span data-stu-id="7737f-118">**Account code** field value</span></span> | <span data-ttu-id="7737f-119">**Konto-/Gruppennummer**-Feldwert</span><span class="sxs-lookup"><span data-stu-id="7737f-119">**Account/Group number** field value</span></span>        | <span data-ttu-id="7737f-120">Suchpriorität</span><span class="sxs-lookup"><span data-stu-id="7737f-120">Search priority</span></span> |
|------------------------------|---------------------------------------------|-----------------|
| <span data-ttu-id="7737f-121">**Tabelle**</span><span class="sxs-lookup"><span data-stu-id="7737f-121">**Table**</span></span>                    | <span data-ttu-id="7737f-122">Bestimmtes Kreditorenkonto</span><span class="sxs-lookup"><span data-stu-id="7737f-122">Specific vendor account</span></span>                     | <span data-ttu-id="7737f-123">1</span><span class="sxs-lookup"><span data-stu-id="7737f-123">1</span></span>               |
| <span data-ttu-id="7737f-124">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="7737f-124">**Group**</span></span>                    | <span data-ttu-id="7737f-125">Die Kreditorengruppe, die dem Kreditor zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="7737f-125">vendor group that is assigned to the vendor</span></span> | <span data-ttu-id="7737f-126">2</span><span class="sxs-lookup"><span data-stu-id="7737f-126">2</span></span>               |
| <span data-ttu-id="7737f-127">**Alle**</span><span class="sxs-lookup"><span data-stu-id="7737f-127">**All**</span></span>                      | <span data-ttu-id="7737f-128">Leer</span><span class="sxs-lookup"><span data-stu-id="7737f-128">Blank</span></span>                                       | <span data-ttu-id="7737f-129">3</span><span class="sxs-lookup"><span data-stu-id="7737f-129">3</span></span>               |

<span data-ttu-id="7737f-130">Wenn alle Kreditorenbuchungen das gleiche Buchungsprofil besitzen sollen, richten Sie nur ein Buchungsprofil mit der Angabe "Alle" im Feld "Kontocode" ein.</span><span class="sxs-lookup"><span data-stu-id="7737f-130">If you want all vendor transactions to have the same posting profile, set up only one posting profile with All in the Account code field.</span></span> <span data-ttu-id="7737f-131">Geben Sie die folgenden Werte an, um das Buchungsprofil einzurichten:</span><span class="sxs-lookup"><span data-stu-id="7737f-131">Specify the following values to set up your posting profile:</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="7737f-132">Feld</span><span class="sxs-lookup"><span data-stu-id="7737f-132">Field</span></span></th>
<th><span data-ttu-id="7737f-133">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7737f-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7737f-134"><strong>Buchungsprofil</strong></span><span class="sxs-lookup"><span data-stu-id="7737f-134"><strong>Posting profile</strong></span></span></td>
<td><span data-ttu-id="7737f-135">Hier können Sie einen Code für das Buchungsprofil eingeben.</span><span class="sxs-lookup"><span data-stu-id="7737f-135">Enter a code for the posting profile.</span></span> <span data-ttu-id="7737f-136">Sie können z. B. zwei Buchungsprofile erstellen, um ein Konto für Kreditorensalden in der Landeswährung und ein weiteres Konto für Kreditorensalden in einer Fremdwährung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="7737f-136">For example, you could create two posting profiles to obtain one account for vendor balances in the national currency and another for vendor balances in a foreign currency.</span></span> <span data-ttu-id="7737f-137">Das erste Konto können Sie dann mit "Landeswährung", das zweite mit "Fremdwährung" benennen.</span><span class="sxs-lookup"><span data-stu-id="7737f-137">You could call one account National and the other Foreign.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7737f-138"><strong>Beschreibung</strong></span><span class="sxs-lookup"><span data-stu-id="7737f-138"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="7737f-139">Geben Sie eine Beschreibung des Buchungsprofils ein.</span><span class="sxs-lookup"><span data-stu-id="7737f-139">Enter a description of the posting profile.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7737f-140"><strong>Kontocode</strong></span><span class="sxs-lookup"><span data-stu-id="7737f-140"><strong>Account code</strong></span></span></td>
<td><span data-ttu-id="7737f-141">Geben Sie an, ob sich das Buchungsprofil auf einen bestimmten Kreditor, eine Kreditorengruppe oder alle Kreditoren bezieht:</span><span class="sxs-lookup"><span data-stu-id="7737f-141">Specify whether the posting profile applies to a specific vendor, a group of vendors, or all vendors:</span></span>
<ul>
<li><span data-ttu-id="7737f-142"><strong>Tabelle</strong> – Das Buchungsprofil gilt für einen einzelnen Kreditor.</span><span class="sxs-lookup"><span data-stu-id="7737f-142"><strong>Table</strong> – The posting profile applies to a single vendor.</span></span> <span data-ttu-id="7737f-143">Wählen Sie das Kreditorenkonto im Feld 'Konto-/Gruppennummer' aus.</span><span class="sxs-lookup"><span data-stu-id="7737f-143">Select the vendor account in the Account/Group number field.</span></span></li>
<li><span data-ttu-id="7737f-144"><strong>Gruppe</strong> – Das Buchungsprofil gilt für eine Kreditorengruppe.</span><span class="sxs-lookup"><span data-stu-id="7737f-144"><strong>Group</strong> – The posting profile applies to a vendor group.</span></span> <span data-ttu-id="7737f-145">Wählen Sie das Kreditorengruppe im Feld 'Konto-/Gruppennummer' aus.</span><span class="sxs-lookup"><span data-stu-id="7737f-145">Select the vendor group in the Account/Group number field.</span></span></li>
<li><span data-ttu-id="7737f-146"><strong>Alle</strong> – Das Buchungsprofil gilt für alle Kreditoren.</span><span class="sxs-lookup"><span data-stu-id="7737f-146"><strong>All</strong> – The posting profile applies to all vendors.</span></span> <span data-ttu-id="7737f-147">Lassen Sie die "Konto-/Gruppennummer"-Feld leer.</span><span class="sxs-lookup"><span data-stu-id="7737f-147">Leave the Account/Group number field blank.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7737f-148"><strong>Konto-/Gruppennummer</strong></span><span class="sxs-lookup"><span data-stu-id="7737f-148"><strong>Account/Group number</strong></span></span></td>
<td><span data-ttu-id="7737f-149">Wurde im Feld "Kontocode" die Option "Tabelle" ausgewählt, wählen Sie die Kontonummer des Kreditors aus, der dem Buchungsprofil zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="7737f-149">If Table is selected in the Account code field, select the account number of the vendor that is associated with the posting profile.</span></span> <span data-ttu-id="7737f-150">Wenn Sie "Gruppe" ausgewählt haben, wählen Sie eine Kreditorengruppe aus.</span><span class="sxs-lookup"><span data-stu-id="7737f-150">If Group is selected, select a vendor group.</span></span> <span data-ttu-id="7737f-151">Wurde "Alle" ausgewählt, lassen Sie das Feld leer.</span><span class="sxs-lookup"><span data-stu-id="7737f-151">If All is selected, leave this field blank.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7737f-152"><strong>Sammelkonto</strong></span><span class="sxs-lookup"><span data-stu-id="7737f-152"><strong>Summary account</strong></span></span></td>
<td><span data-ttu-id="7737f-153">Wählen Sie das Sachkonto aus, das als Sammelkonto für die Kreditoren verwendet werden soll, auf die sich das Buchungsprofil bezieht.</span><span class="sxs-lookup"><span data-stu-id="7737f-153">Select the ledger account that will be used as the summary account for the vendors that the posting profile relates to.</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Notiz" alt="Note" id="alert_note" class="cl_IC101471" /><span data-ttu-id="7737f-155"><strong>Hinweis</strong></span><span class="sxs-lookup"><span data-stu-id="7737f-155"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7737f-156">Wenn die Option "Buchungsdefinitionen verwenden" auf der Seite "Hauptbuchparameter" aktiviert ist, wird die Buchungsdefinition für Kreditorenrechnungen anstatt des Sammelkontos verwendet.</span><span class="sxs-lookup"><span data-stu-id="7737f-156">If the Use posting definitions toggle is selected in the General ledger parameters page, the transaction posting definition for vendor invoices is used instead of the summary account.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7737f-157"><strong>Konto ausgleichen</strong></span><span class="sxs-lookup"><span data-stu-id="7737f-157"><strong>Settle account</strong></span></span></td>
<td><span data-ttu-id="7737f-158">Wählen Sie das Liquiditätssachkonto aus, das für Cashflowplanungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7737f-158">Select the liquidity ledger account that is used for cash flow forecasts.</span></span> <span data-ttu-id="7737f-159">Dieses Feld ist nur verfügbar wenn Cashflowplanungen aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="7737f-159">This fields is only available when cash flow forecasting is enabled.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7737f-160"><strong>Mehrwertsteuervorauszahlungen</strong></span><span class="sxs-lookup"><span data-stu-id="7737f-160"><strong>Sales tax prepayments</strong></span></span></td>
<td><span data-ttu-id="7737f-161">Wählen Sie das Konto für die Mehrwertsteuerzahlungen aus, die vorab eingehen.</span><span class="sxs-lookup"><span data-stu-id="7737f-161">Select the account for sales tax payments that are received in advance.</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Notiz" alt="Note" id="alert_note" class="cl_IC101471" /><span data-ttu-id="7737f-163"><strong>Hinweis</strong></span><span class="sxs-lookup"><span data-stu-id="7737f-163"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7737f-164">Das Buchungsprofil, das verwendet wird, wenn die Zahlung im Feld "Buchungsprofil mit Erfassungsbeleg für Vorauszahlung" im Bereich "Sachkonto und Mehrwertsteuer" der Kreditorenparameterseite als Vorauszahlung gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="7737f-164">The posting profile that is used when the payment is marked as a prepayment is selected in the Posting profile with prepayment journal voucher field in the Ledger and sales tax area of the Accounts payable parameters page.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7737f-165"><strong>Wareneingang</strong></span><span class="sxs-lookup"><span data-stu-id="7737f-165"><strong>Arrival</strong></span></span></td>
<td><span data-ttu-id="7737f-166">Wählen Sie das Sachkonto aus, auf das Informationen zu nicht genehmigten Kreditorenrechnungen gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="7737f-166">Select the ledger account that information about unapproved vendor invoices is posted to.</span></span> <span data-ttu-id="7737f-167">Die Informationen werden in der Rechnungsbucherfassung erfasst.</span><span class="sxs-lookup"><span data-stu-id="7737f-167">The information is entered in the Invoice register journal.</span></span> <span data-ttu-id="7737f-168">Ein Benutzer gibt z. B. grundlegende Informationen zu Kreditorenrechnungen ein, wenn diese im Rechnungsbuch eingehen.</span><span class="sxs-lookup"><span data-stu-id="7737f-168">For example, a user enters very basic information about vendor invoices when they are received in the invoice register.</span></span> <span data-ttu-id="7737f-169">Beim Buchen des Rechnungsbuchs erfolgen die Buchungen auf dem Konto, das hier und im Feld "Gegenkonto" eingegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7737f-169">When the invoice register is posted, the transactions are posted to the account that is entered here and in the Offset account field.</span></span> <span data-ttu-id="7737f-170">Wenn die Rechnungen genehmigt werden, wird die Verbindlichkeit aus dem Eingangskonto in das Sammelkonto des Kreditors übertragen.</span><span class="sxs-lookup"><span data-stu-id="7737f-170">When the invoices are approved, the debt is transferred from the Arrival account to the vendor summary account.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7737f-171"><strong>Gegenkonto</strong></span><span class="sxs-lookup"><span data-stu-id="7737f-171"><strong>Offset account</strong></span></span></td>
<td><span data-ttu-id="7737f-172">Wählen Sie das Sachkonto aus, das zum Aufrechnen nicht genehmigter Kreditorenrechnungen verwendet wird, die über das Rechnungsbuch aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="7737f-172">Select the ledger account that is used for offsetting unapproved vendor invoices that are updated by using the invoice register.</span></span> <span data-ttu-id="7737f-173">Das Gegenkonto dient als Gegenkonto für Buchungen, die auf Eingangskonten gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="7737f-173">The offset account acts as the offset account for transactions that are posted to arrival accounts.</span></span> <span data-ttu-id="7737f-174">Daher enthält das Konto Kreditoreneinkäufe, die noch nicht genehmigt wurden.</span><span class="sxs-lookup"><span data-stu-id="7737f-174">Therefore, the account contains vendor purchases that have not yet been approved.</span></span></td>
</tr>
</tbody>
</table>


### <a name="table-restrictions"></a><span data-ttu-id="7737f-175">**Tabelleneinschränkungen**</span><span class="sxs-lookup"><span data-stu-id="7737f-175">**Table restrictions**</span></span>

<span data-ttu-id="7737f-176">Hier können Sie für Buchungen mit dem ausgewählten Buchungsprofil angeben, ob die Buchungen automatisch ausgeglichen werden, ob eine Zinsberechnung erfolgt und ob Mahnschreiben erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="7737f-176">For transactions that have the selected posting profile, specify whether transactions will be settled automatically, interest will be calculated, and collection letters will be issued.</span></span> <span data-ttu-id="7737f-177">Darüber hinaus können Sie das Konto auswählen, das beim Abschließen von Buchungen mit dem ausgewählten Buchungsprofil verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7737f-177">You can also select the account that is used when transactions that have the selected posting profile are closed.</span></span>

<span data-ttu-id="7737f-178">Geben Sie die folgenden Werte an, um das Buchungsprofil einzurichten:</span><span class="sxs-lookup"><span data-stu-id="7737f-178">Specify the following values to set up your posting profile:</span></span>

| <span data-ttu-id="7737f-179">Feld</span><span class="sxs-lookup"><span data-stu-id="7737f-179">Field</span></span>          | <span data-ttu-id="7737f-180">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7737f-180">Description</span></span>                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7737f-181">**Ausgleich**</span><span class="sxs-lookup"><span data-stu-id="7737f-181">**Settlement**</span></span> | <span data-ttu-id="7737f-182">Aktivieren Sie diese Option, um den automatischen Ausgleich von Buchungen mit diesem Buchungsprofil zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="7737f-182">Select this option to enable automatic settlement of transactions that have this posting profile.</span></span> <span data-ttu-id="7737f-183">Ist diese Option deaktiviert, müssen die Buchungen manuell mithilfe der Seite "Offene Buchungen ausgleichen" ausgeglichen werden.</span><span class="sxs-lookup"><span data-stu-id="7737f-183">If this option is cleared, you must manually settle transactions by using the Settle open transactions page.</span></span> |
| <span data-ttu-id="7737f-184">**Stornieren**</span><span class="sxs-lookup"><span data-stu-id="7737f-184">**Cancel**</span></span>     | <span data-ttu-id="7737f-185">Aktivieren Sie diese Option, wenn Sie in der Lage sein möchten, Buchungen mit diesem Buchungsprofil zu stornieren.</span><span class="sxs-lookup"><span data-stu-id="7737f-185">Select this option if you want to be able to cancel transactions that have this posting profile.</span></span>                                                                                                               |
| <span data-ttu-id="7737f-186">**Schließen**</span><span class="sxs-lookup"><span data-stu-id="7737f-186">**Close**</span></span>      | <span data-ttu-id="7737f-187">Wählen Sie ein Buchungsprofil aus, das geändert werden soll, wenn Buchungen mit diesem Buchungsprofil abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="7737f-187">Select a posting profile to change to when transactions that have this posting profile are closed.</span></span> <span data-ttu-id="7737f-188">Eine Buchung gilt als abgeschlossen, wenn sie vollständig ausgeglichen wurde.</span><span class="sxs-lookup"><span data-stu-id="7737f-188">A transaction is regarded as closed when it has been settled in full.</span></span>                                       |






