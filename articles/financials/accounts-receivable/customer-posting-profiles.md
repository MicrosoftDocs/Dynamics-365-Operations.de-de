---
title: Debitoren-Buchungsprofile
description: Kundenbuchungsprofile steuern die Buchungen von Kundentransaktionen im Hauptbuch.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 956dca24c2cfa7e22d718ff84b338bc4ba030394
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "322351"
---
# <a name="customer-posting-profiles"></a><span data-ttu-id="5fdae-103">Debitoren-Buchungsprofile</span><span class="sxs-lookup"><span data-stu-id="5fdae-103">Customer posting profiles</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5fdae-104">Kundenbuchungsprofile steuern die Buchungen von Kundentransaktionen im Hauptbuch.</span><span class="sxs-lookup"><span data-stu-id="5fdae-104">Customer posting profiles control the posting of customer transactions to the general ledger.</span></span>

<a name="customer-posting-profiles"></a><span data-ttu-id="5fdae-105">Debitoren-Buchungsprofile</span><span class="sxs-lookup"><span data-stu-id="5fdae-105">Customer posting profiles</span></span>
-------------------------

<span data-ttu-id="5fdae-106">Debitoren-Buchungsprofile ermöglichen das Zuweisen von Hauptbuchkonten und Dokumenteinstellungen zu allen Debitoren, einer Debitorengruppe oder einem bestimmten Debitor.</span><span class="sxs-lookup"><span data-stu-id="5fdae-106">Customer posting profiles enable you to assign general ledger accounts and document settings to all customers, a group of customers or a single customer.</span></span> <span data-ttu-id="5fdae-107">Diese Einstellungen werden verwendet, wenn Aufträge, Freitextrechnungen, Barzahlungen, Mahnschreiben und Zinsrechnungen erstellen werden.</span><span class="sxs-lookup"><span data-stu-id="5fdae-107">These settings will be used when you create sales orders, free text invoices, cash payments, collection letters, and interest notes.</span></span> <span data-ttu-id="5fdae-108">Bei einigen Buchungen können Sie ein Buchungsprofil auswählen, das sich von den in diesem Formular für Buchungen eingerichteten Buchungsprofilen unterscheidet und Vorrang vor diesen hat.</span><span class="sxs-lookup"><span data-stu-id="5fdae-108">For some transactions, you can select a posting profile that differs from and takes precedence over the posting profiles that are set up for transactions in this page.</span></span> 

<span data-ttu-id="5fdae-109">Das Buchungsprofil wird im Sachkonto- und Mehrwertsteuer-Inforegister auf der Debitorenparameterseite definiert.</span><span class="sxs-lookup"><span data-stu-id="5fdae-109">The default posting profile is defined in the Ledger and Sales Tax fasttab on the Accounts receivable parameters page.</span></span> <span data-ttu-id="5fdae-110">Das Buchungsprofil wird dann automatisch in den Kopf neuer Dokumente einbezogen. Dort können es bei Bedarf zu einem anderen Buchungsprofil ändern.</span><span class="sxs-lookup"><span data-stu-id="5fdae-110">The default posting profile is then included automatically on the header of new documents where you can change it to a different posting profile if needed.</span></span>

<span data-ttu-id="5fdae-111">Sie können auch Buchungsdefinitionen zu Buchungsarten auf der Seite "Transaktionsbuchungsdefinitionen" zuordnen.</span><span class="sxs-lookup"><span data-stu-id="5fdae-111">You can also associate posting definitions with transaction posting types in the Transaction posting definitions page.</span></span> <span data-ttu-id="5fdae-112">Buchungsdefinitionen dienen zum Steuern von Debitorenbuchungen auf das Hauptbuch anstelle von Buchungsprofilen.</span><span class="sxs-lookup"><span data-stu-id="5fdae-112">Posting definitions control the posting of customer transactions to the general ledger instead of posting profiles.</span></span>

## <a name="creating-a-posting-profile"></a><span data-ttu-id="5fdae-113">Buchungsprofil erstellen</span><span class="sxs-lookup"><span data-stu-id="5fdae-113">Creating a posting profile</span></span>
<span data-ttu-id="5fdae-114">Hier können Sie die Sachkonten angeben, die bei Buchungen mit dem ausgewählten Buchungsprofil verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5fdae-114">Specify the ledger accounts that are used in the posting of transactions that use the selected posting profile.</span></span> <span data-ttu-id="5fdae-115">Wählen Sie einen Kontocode und ggf. eine Konto- oder Gruppennummer für das ausgewählte Buchungsprofil aus.</span><span class="sxs-lookup"><span data-stu-id="5fdae-115">Select an account code and, whenever possible, an account or group number for the selected posting profile.</span></span> <span data-ttu-id="5fdae-116">Während des Buchungsprozesses wird für jede Buchung das am besten geeignete Buchungsprofil gesucht. Hierzu wird nach einem möglichst spezifischen Kontocode, einer möglichst spezifischen Kontonummer oder nach einer möglichst spezifischen Kombination aus Gruppe und Nummer gesucht. Dabei gilt folgende Priorität:</span><span class="sxs-lookup"><span data-stu-id="5fdae-116">In the posting process, the most appropriate posting profile for each transaction is located by searching for the most specific account code, account number, or group and number combination in the following priority:</span></span>

| <span data-ttu-id="5fdae-117">**Kontocode**-Feldwert</span><span class="sxs-lookup"><span data-stu-id="5fdae-117">**Account code** field value</span></span> | <span data-ttu-id="5fdae-118">**Konto-/Gruppennummer**-Feldwert</span><span class="sxs-lookup"><span data-stu-id="5fdae-118">**Account/Group number** field value</span></span>            | <span data-ttu-id="5fdae-119">Suchpriorität</span><span class="sxs-lookup"><span data-stu-id="5fdae-119">Search priority</span></span> |
|------------------------------|-------------------------------------------------|-----------------|
| <span data-ttu-id="5fdae-120">**Tabelle**</span><span class="sxs-lookup"><span data-stu-id="5fdae-120">**Table**</span></span>                    | <span data-ttu-id="5fdae-121">Bestimmtes Debitorenkonto</span><span class="sxs-lookup"><span data-stu-id="5fdae-121">Specific customer account</span></span>                       | <span data-ttu-id="5fdae-122">1</span><span class="sxs-lookup"><span data-stu-id="5fdae-122">1</span></span>               |
| <span data-ttu-id="5fdae-123">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="5fdae-123">**Group**</span></span>                    | <span data-ttu-id="5fdae-124">Dem Debitor zugeordnete Debitorengruppe</span><span class="sxs-lookup"><span data-stu-id="5fdae-124">Customer group that is assigned to the customer</span></span> | <span data-ttu-id="5fdae-125">2</span><span class="sxs-lookup"><span data-stu-id="5fdae-125">2</span></span>               |
| <span data-ttu-id="5fdae-126">**Alle**</span><span class="sxs-lookup"><span data-stu-id="5fdae-126">**All**</span></span>                      | <span data-ttu-id="5fdae-127">Leer</span><span class="sxs-lookup"><span data-stu-id="5fdae-127">Blank</span></span>                                           | <span data-ttu-id="5fdae-128">3</span><span class="sxs-lookup"><span data-stu-id="5fdae-128">3</span></span>               |

<span data-ttu-id="5fdae-129">Wenn alle Debitorenbuchungen das gleiche Buchungsprofil besitzen sollen, richten Sie nur ein Buchungsprofil mit der Angabe "Alle" im Feld "Kontocode" ein.</span><span class="sxs-lookup"><span data-stu-id="5fdae-129">If you want all customer transactions to have the same posting profile, set up only one posting profile with All in the Account code field.</span></span> <span data-ttu-id="5fdae-130">Geben Sie die folgenden Werte an, um das Buchungsprofil einzurichten:</span><span class="sxs-lookup"><span data-stu-id="5fdae-130">Specify the following values to set up your posting profile:</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="5fdae-131">Feld</span><span class="sxs-lookup"><span data-stu-id="5fdae-131">Field</span></span></th>
<th><span data-ttu-id="5fdae-132">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5fdae-132">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5fdae-133"><strong>Buchungsprofil</strong></span><span class="sxs-lookup"><span data-stu-id="5fdae-133"><strong>Posting profile</strong></span></span></td>
<td><span data-ttu-id="5fdae-134">Hier können Sie einen Code für das Buchungsprofil eingeben.</span><span class="sxs-lookup"><span data-stu-id="5fdae-134">Enter a code for the posting profile.</span></span> <span data-ttu-id="5fdae-135">Sie können beispielsweise zwei Buchungsprofile erstellen, um ein Konto für Debitorensaldos in der Landeswährung und ein weiteres Konto für Debitorensaldos in einer Fremdwährung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5fdae-135">For example, you could create two posting profiles to obtain one account for customer balances in the national currency and another for customer balances in a foreign currency.</span></span> <span data-ttu-id="5fdae-136">Das erste Konto können Sie dann mit "Landeswährung", das zweite mit "Fremdwährung" benennen.</span><span class="sxs-lookup"><span data-stu-id="5fdae-136">You could call one account National and the other Foreign.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5fdae-137"><strong>Beschreibung</strong></span><span class="sxs-lookup"><span data-stu-id="5fdae-137"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="5fdae-138">Geben Sie eine Beschreibung des Buchungsprofils ein.</span><span class="sxs-lookup"><span data-stu-id="5fdae-138">Enter a description of the posting profile.</span></span> <span data-ttu-id="5fdae-139">Es wird nur verwendet, um das Buchungsprofil besser zu identifizieren, wenn Sie es auf dieser Seite anzeigen.</span><span class="sxs-lookup"><span data-stu-id="5fdae-139">This is only used to better identify the posting profile when you view it in this page.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5fdae-140"><strong>Kontocode</strong></span><span class="sxs-lookup"><span data-stu-id="5fdae-140"><strong>Account code</strong></span></span></td>
<td><span data-ttu-id="5fdae-141">Geben Sie an, ob sich das Buchungsprofil für einen einzelnen Debitor, für eine Debitorengruppe oder für alle Debitoren gelten soll:</span><span class="sxs-lookup"><span data-stu-id="5fdae-141">Specify whether the posting profile applies to a single customer, a group of customers, or all customers:</span></span>
<ul>
<li><span data-ttu-id="5fdae-142"><strong>Tabelle</strong> – Das Buchungsprofil gilt für einen einzelnen Debitor.</span><span class="sxs-lookup"><span data-stu-id="5fdae-142"><strong>Table</strong> – The posting profile applies to a single customer.</span></span> <span data-ttu-id="5fdae-143">Wählen Sie das Debitorenkonto im Feld 'Konto-/Gruppennummer' aus.</span><span class="sxs-lookup"><span data-stu-id="5fdae-143">Select the customer account in the Account/Group number field.</span></span></li>
<li><span data-ttu-id="5fdae-144"><strong>Gruppe</strong> – Das Buchungsprofil gilt für eine Debitorengruppe.</span><span class="sxs-lookup"><span data-stu-id="5fdae-144"><strong>Group</strong> – The posting profile applies to a customer group.</span></span> <span data-ttu-id="5fdae-145">Wählen Sie das Debitorengruppe im Feld 'Konto-/Gruppennummer' aus.</span><span class="sxs-lookup"><span data-stu-id="5fdae-145">Select the customer group in the Account/Group number field.</span></span></li>
<li><span data-ttu-id="5fdae-146"><strong>Alle</strong> – Das Buchungsprofil gilt für alle Debitoren.</span><span class="sxs-lookup"><span data-stu-id="5fdae-146"><strong>All</strong> – The posting profile applies to all customers.</span></span> <span data-ttu-id="5fdae-147">Lassen Sie die "Konto-/Gruppennummer"-Feld leer.</span><span class="sxs-lookup"><span data-stu-id="5fdae-147">Leave the Account/Group number field blank.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5fdae-148"><strong>Konto-/Gruppennummer</strong></span><span class="sxs-lookup"><span data-stu-id="5fdae-148"><strong>Account/Group number</strong></span></span></td>
<td><span data-ttu-id="5fdae-149">Wurde im Feld "Kontocode" die Option "Tabelle" ausgewählt, wählen Sie die Kontonummer des Debitors aus, der dem Buchungsprofil zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="5fdae-149">If Table is selected in the Account code field, select the account number of the customer who is associated with the posting profile.</span></span> <span data-ttu-id="5fdae-150">Wurde "Grupe" ausgewählt, wählen Sie die Debitorengruppe aus.</span><span class="sxs-lookup"><span data-stu-id="5fdae-150">If Group is selected, select the customer group.</span></span> <span data-ttu-id="5fdae-151">Wurde "Alle" ausgewählt, lassen Sie das Feld leer.</span><span class="sxs-lookup"><span data-stu-id="5fdae-151">If All is selected, leave this field blank.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5fdae-152"><strong>Sammelkonto</strong></span><span class="sxs-lookup"><span data-stu-id="5fdae-152"><strong>Summary account</strong></span></span></td>
<td><span data-ttu-id="5fdae-153">Wählen Sie das Sachkonto aus, das als Debitorensammelkonto für die Debitoren verwendet werden soll, die dem Buchungsprofil zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="5fdae-153">Select the ledger account that will be used as the customer summary account for the customers who are associated with the posting profile.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5fdae-154"><strong>Konto ausgleichen</strong></span><span class="sxs-lookup"><span data-stu-id="5fdae-154"><strong>Settle account</strong></span></span></td>
<td><span data-ttu-id="5fdae-155">Wählen Sie das Liquiditätssachkonto aus, das für Cashflowplanungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5fdae-155">Select the liquidity ledger account that is used for cash flow forecasts.</span></span> <span data-ttu-id="5fdae-156">Dieses Feld wird nur angezeigt, wenn Cashflow-Planungen aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="5fdae-156">This field will only appear if cash flow forecasts are enabled.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5fdae-157"><strong>Mehrwertsteuervorauszahlungen</strong></span><span class="sxs-lookup"><span data-stu-id="5fdae-157"><strong>Sales tax prepayments</strong></span></span></td>
<td><span data-ttu-id="5fdae-158">Wählen Sie das Konto für die Mehrwertsteuer auf eingegangene Vorauszahlungen aus.</span><span class="sxs-lookup"><span data-stu-id="5fdae-158">Select the account for sales tax for payments that are received in advance.</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Notiz" alt="Note" id="alert_note" class="cl_IC101471" /><span data-ttu-id="5fdae-160"><strong>Hinweis</strong></span><span class="sxs-lookup"><span data-stu-id="5fdae-160"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5fdae-161">Geben Sie auf der Seite "Debitorenkontenparameter" das Buchungsprofil an, das verwendet werden soll, wenn eine Zahlung als Vorauszahlung markiert ist.</span><span class="sxs-lookup"><span data-stu-id="5fdae-161">Use the Accounts receivable parameters page to specify the posting profile to use when a payment is marked as a prepayment.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5fdae-162"><strong>Konto für Diskontverbindlichkeiten</strong></span><span class="sxs-lookup"><span data-stu-id="5fdae-162"><strong>Liabilities for discount account</strong></span></span></td>
<td><span data-ttu-id="5fdae-163">Wählen Sie das Sachkonto für Diskontverbindlichkeiten aus.</span><span class="sxs-lookup"><span data-stu-id="5fdae-163">Select the ledger account for liabilities of discount.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5fdae-164"><strong>Mahnschreibensequenz</strong></span><span class="sxs-lookup"><span data-stu-id="5fdae-164"><strong>Collection letter sequence</strong></span></span></td>
<td><span data-ttu-id="5fdae-165">Wählen Sie die Kennung der Mahnschreibensequenz aus, die für Debitoren mit dem Buchungsprofil verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5fdae-165">Select the identifier of the collection letter sequence to use for customers to whom the posting profile is assigned.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5fdae-166"><strong>Zinscode</strong></span><span class="sxs-lookup"><span data-stu-id="5fdae-166"><strong>Interest code</strong></span></span></td>
<td><span data-ttu-id="5fdae-167">Wählen Sie den Zinscode aus, der bei der Zinsberechnung für Debitoren mit dem Buchungsprofil verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5fdae-167">Select the interest code to use for the calculation of interest for customers to whom the posting profile is assigned.</span></span></td>
</tr>
</tbody>
</table>

### 

### <a name="table-restrictions"></a><span data-ttu-id="5fdae-168">**Tabelleneinschränkungen**</span><span class="sxs-lookup"><span data-stu-id="5fdae-168">**Table restrictions**</span></span>

<span data-ttu-id="5fdae-169">Hier können Sie für Buchungen mit dem ausgewählten Buchungsprofil angeben, ob die Buchungen automatisch ausgeglichen werden, ob eine Zinsberechnung erfolgt und ob Mahnschreiben erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="5fdae-169">For transactions that have the selected posting profile, specify whether transactions will be settled automatically, interest will be calculated, and collection letters will be issued.</span></span> <span data-ttu-id="5fdae-170">Darüber hinaus können Sie das Konto auswählen, das beim Abschließen von Buchungen mit dem ausgewählten Buchungsprofil verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5fdae-170">You can also select the account that is used when transactions that have the selected posting profile are closed.</span></span>

<span data-ttu-id="5fdae-171">Geben Sie die folgenden Werte an, um das Buchungsprofil einzurichten:</span><span class="sxs-lookup"><span data-stu-id="5fdae-171">Specify the following values to set up your posting profile:</span></span>

| <span data-ttu-id="5fdae-172">Feld</span><span class="sxs-lookup"><span data-stu-id="5fdae-172">Field</span></span>                 | <span data-ttu-id="5fdae-173">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5fdae-173">Description</span></span>                                                                                                                                                                                                                                        |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fdae-174">**Ausgleich**</span><span class="sxs-lookup"><span data-stu-id="5fdae-174">**Settlement**</span></span>        | <span data-ttu-id="5fdae-175">Aktivieren Sie diese Option, um den automatischen Ausgleich von Buchungen mit diesem Buchungsprofil zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="5fdae-175">Select this toggle to enable automatic settlement of transactions that have this posting profile.</span></span> <span data-ttu-id="5fdae-176">Wenn die Option deaktiviert ist, müssen Sie die Buchungen manuell ausgleichen, indem Sie die Seite "Offene Buchungen ausgleichen" oder "Debitorenzahlungen eingeben" verwenden.</span><span class="sxs-lookup"><span data-stu-id="5fdae-176">If this toggle is cleared, you must manually settle transactions by using the Settle open transactions page or the Enter customer payments page.</span></span> |
| <span data-ttu-id="5fdae-177">**Interesse**</span><span class="sxs-lookup"><span data-stu-id="5fdae-177">**Interest**</span></span>          | <span data-ttu-id="5fdae-178">Aktivieren Sie diese Option, wenn für Debitorenkonten mit diesem Profil Zinsen auf Außenstände berechnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5fdae-178">Select this toggle if interest should be calculated on outstanding balances for customer accounts that use this profile.</span></span> <span data-ttu-id="5fdae-179">Ist diese Option deaktiviert, werden für diese Debitoren keine Zinsen berechnet.</span><span class="sxs-lookup"><span data-stu-id="5fdae-179">If this toggle is cleared, interest will not be calculated for these customers.</span></span>                                           |
| <span data-ttu-id="5fdae-180">**Mahnschreiben**</span><span class="sxs-lookup"><span data-stu-id="5fdae-180">**Collection letter**</span></span> | <span data-ttu-id="5fdae-181">Aktivieren Sie diese Option, wenn für Debitorenkonten mit diesem Profil Mahnschreiben generiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5fdae-181">Select this toggle if collection letters should be generated for customer accounts that use this profile.</span></span> <span data-ttu-id="5fdae-182">Ist diese Option deaktiviert, werden für diese Debitoren keine Mahnschreiben generiert.</span><span class="sxs-lookup"><span data-stu-id="5fdae-182">If this toggle is cleared, collection letters will not be generated for these customers.</span></span>                                                 |
| <span data-ttu-id="5fdae-183">**Schließen**</span><span class="sxs-lookup"><span data-stu-id="5fdae-183">**Close**</span></span>             | <span data-ttu-id="5fdae-184">Wählen Sie ein Buchungsprofil aus, das geändert werden soll, wenn Buchungen mit diesem Buchungsprofil abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="5fdae-184">Select a posting profile to change to when transactions that have this posting profile are closed.</span></span> <span data-ttu-id="5fdae-185">Eine Buchung gilt als abgeschlossen, wenn sie vollständig ausgeglichen wurde.</span><span class="sxs-lookup"><span data-stu-id="5fdae-185">A transaction is regarded as closed when it has been settled in full.</span></span>                                                                           |



<span data-ttu-id="5fdae-186">Weitere Informationen finden Sie unter [Überfällige Debitorenzahlungen](../cash-bank-management/tasks/customer-payment-overview.md).</span><span class="sxs-lookup"><span data-stu-id="5fdae-186">For more information, see [Customer payment overview](../cash-bank-management/tasks/customer-payment-overview.md).</span></span>

