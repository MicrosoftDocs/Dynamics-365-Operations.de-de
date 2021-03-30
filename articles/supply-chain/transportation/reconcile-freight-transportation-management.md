---
title: Fracht in der Transportverwaltung abstimmen
description: Dieser Artikel beschreibt den Frachtabstimmungsprozess.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSFBDetailReconcile, TMSInvoiceTable,TMSInvoiceLineReconcile,TMSReconcileInvoice, TMSFreightBillDetail, TMSFreightBillTypeAssignment, TMSRejectInvoiceLine, TMSMiscellaneousCharge
audience: Application User
ms.reviewer: kamaybac
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7af7bbb500de25e0a796147fae42cd7d943be9df
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5205225"
---
# <a name="reconcile-freight-in-transportation-management"></a><span data-ttu-id="c2e19-103">Fracht in der Transportverwaltung abstimmen</span><span class="sxs-lookup"><span data-stu-id="c2e19-103">Reconcile freight in transportation management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c2e19-104">Dieser Artikel beschreibt den Frachtabstimmungsprozess.</span><span class="sxs-lookup"><span data-stu-id="c2e19-104">This topic describes the freight reconciliation process.</span></span>

<span data-ttu-id="c2e19-105">Die Frachtabstimmung kann manuell oder automatischen durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c2e19-105">Freight reconciliation can be done manually, or it can be set up to occur automatically.</span></span> <span data-ttu-id="c2e19-106">Um die automatische Frachtabstimmung zu verwenden, müssen Sie einen Überwachungsmaster einrichten. In ihm können Sie die Kriterien definieren, die festlegen, welche Fracht automatisch abgestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="c2e19-106">To use automatic freight reconciliation, you must set up an audit master where you can define criteria that determine which freight bills are matched automatically.</span></span>

## <a name="the-freight-reconciliation-process"></a><span data-ttu-id="c2e19-107">Der Frachtabstimmungsprozess</span><span class="sxs-lookup"><span data-stu-id="c2e19-107">The freight reconciliation process</span></span>

<span data-ttu-id="c2e19-108">Frachtkosten werden vom den Tarifmodul berechnet, das dem relevanten Spediteur zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c2e19-108">Freight rates are calculated by the rate engine that is associated with the relevant shipping carrier.</span></span> <span data-ttu-id="c2e19-109">Wenn ein Ladung bestätigt ist, wird ein Frachtbrief erstellt und die Frachtkosten werden an diesen übertragen.</span><span class="sxs-lookup"><span data-stu-id="c2e19-109">When a load is confirmed, a freight bill is generated, and the freight rates are transferred to it.</span></span> <span data-ttu-id="c2e19-110">Die Frachtkosten werden je nach Konfiguration für den regulären Abrechnungsprozess als sonstige Zuschläge auf das entsprechende Quelldokument umgelegt (Bestellung, Auftrag und/oder Umlagerungsauftrag).</span><span class="sxs-lookup"><span data-stu-id="c2e19-110">The freight rates are apportioned as miscellaneous charges to the relevant source document (purchase order, sales order, and/or transfer order), depending on the setup that is used for the regular billing process.</span></span> <span data-ttu-id="c2e19-111">Der Frachtabstimmungsprozesse (auch Abgleichsprozess genannt) kann starten sobald die Frachtrechnung vom Spediteur eingeht.</span><span class="sxs-lookup"><span data-stu-id="c2e19-111">The freight reconciliation process (which is also known as the matching process) can start as soon as the freight invoice arrives from the shipping carrier.</span></span> <span data-ttu-id="c2e19-112">Die Rechnung elektronisch oder auf Papier erhalten werden.</span><span class="sxs-lookup"><span data-stu-id="c2e19-112">The invoice can be received electronically or on paper.</span></span> <span data-ttu-id="c2e19-113">Wenn die Rechnung auf Papier erhalten wird, können Sie mit dem Frachtbrief als Vorlage eine elektronische Rechnung generieren.</span><span class="sxs-lookup"><span data-stu-id="c2e19-113">If the invoice is received on paper, you can generate an electronic invoice by using the freight bill as a template.</span></span>

<span data-ttu-id="c2e19-114">[![Frachtabstimmungsprozess](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span><span class="sxs-lookup"><span data-stu-id="c2e19-114">[![Freight reconciliation process](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span></span>

## <a name="manual-reconciliation"></a><span data-ttu-id="c2e19-115">Manuelle Abstimmung</span><span class="sxs-lookup"><span data-stu-id="c2e19-115">Manual reconciliation</span></span>

<span data-ttu-id="c2e19-116">Wenn Sie die Fracht manuell abstimmen, müssen Sie jede Rechnungsposition mit der Frachtbriefposition oder den-positionen für die zu fakturierende Ladung abgleichen.</span><span class="sxs-lookup"><span data-stu-id="c2e19-116">If you're reconciling freight manually, you must match each invoice line with the freight bill line or lines for the load that is being invoiced.</span></span> <span data-ttu-id="c2e19-117">Diesen Abgleich führen Sie auf der Seite **Frachtbrief- und Rechnungsabgleich** durch.</span><span class="sxs-lookup"><span data-stu-id="c2e19-117">You do this matching on the **Freight bill and invoice matching** page.</span></span> <span data-ttu-id="c2e19-118">Wenn der Betrag der Rechnungsposition nicht mit dem Frachtbriefbetrag übereinstimmt, müssen Sie einen Abstimmungsgrund für die Abweichung auswählen.</span><span class="sxs-lookup"><span data-stu-id="c2e19-118">If the amount on the invoice line doesn’t match the freight bill amount, you must select a reconciliation reason for the difference.</span></span> <span data-ttu-id="c2e19-119">Sind mehrere Gründe für die Abstimmung zutreffen, können Sie die nicht abgeglichenen Mengen auf diese Gründe verteilen.</span><span class="sxs-lookup"><span data-stu-id="c2e19-119">If there are multiple reasons for reconciliation, you can split the unmatched amount across them.</span></span> <span data-ttu-id="c2e19-120">Der Abstimmungsgrund bestimmt, wie die Differenzbeträge im Hauptbuch gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="c2e19-120">The reconciliation reason determines how the difference amounts are posted in the general ledger.</span></span> <span data-ttu-id="c2e19-121">Bei die Abstimmung des gesamten Rechnungsbetrags gebucht wird, wird dieser zur Genehmigung gesendet. Dann wird die Erfassung gebucht.</span><span class="sxs-lookup"><span data-stu-id="c2e19-121">When the reconciliation of the whole invoice amount is accounted for, it's submitted for approval, and then the journal is posted.</span></span> <span data-ttu-id="c2e19-122">Die folgende Abbildung zeigt, wie eine Frachtrechnung generiert und eine Frachtabstimmung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c2e19-122">The following illustration shows how to generate a freight invoice and do freight reconciliation.</span></span>

<span data-ttu-id="c2e19-123">[![Frachtabstimmungsaufgaben](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span><span class="sxs-lookup"><span data-stu-id="c2e19-123">[![Freight reconciliation tasks](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span></span>

## <a name="automatic-reconciliation"></a><span data-ttu-id="c2e19-124">Automatische Abstimmung</span><span class="sxs-lookup"><span data-stu-id="c2e19-124">Automatic reconciliation</span></span>

<span data-ttu-id="c2e19-125">Um die automatische Abstimmung zu verwenden, müssen Sie den Zeitplan für die Abstimmung und die zu verwendenden Rechnungen und Spediteure angeben.</span><span class="sxs-lookup"><span data-stu-id="c2e19-125">To use automatic reconciliation, you must specify the schedule for reconciliation, and the invoices and shipping carriers to use.</span></span> <span data-ttu-id="c2e19-126">Der Abgleich der Rechnungspositionen und Frachtbriefe wird entsprechend der Einrichtung des Überwachungsmasters und der Frachtbriefart ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c2e19-126">The matching of the invoice lines and freight bills is done according to the setup of the audit master and freight bill type.</span></span> <span data-ttu-id="c2e19-127">Nach dem Ausführen der automatischen Abstimmung müssen Sie alle Rechnungen bearbeiten, die das System nicht zuordnen kann.</span><span class="sxs-lookup"><span data-stu-id="c2e19-127">After you run the automatic reconciliation, you must handle any invoices that the system can't match.</span></span> <span data-ttu-id="c2e19-128">Sie müssen diese Rechnungen dann manuell verarbeiten, bevor Sie alle Rechnung für die Zahlung buchen können.</span><span class="sxs-lookup"><span data-stu-id="c2e19-128">You must then process these invoices manually before you can post all the invoices for payment.</span></span>

## <a name="match-freight-bills-with-freight-invoices-using-automatic-or-manual-reconciliation"></a><span data-ttu-id="c2e19-129">Abgleichen von Frachtbriefen mit Frachtrechnungen mithilfe einer automatischen oder manuellen Abstimmung</span><span class="sxs-lookup"><span data-stu-id="c2e19-129">Match freight bills with freight invoices using automatic or manual reconciliation</span></span>

<span data-ttu-id="c2e19-130">*Abgleichen* ist der Prozess des Findens der Frachbriefe, die jeder Frachtrechnung entsprechen.</span><span class="sxs-lookup"><span data-stu-id="c2e19-130">*Matching* is the process of finding the freight bills that correspond to each freight invoice.</span></span> <span data-ttu-id="c2e19-131">Dies kann durch Abgleichen der einzelnen Rechnungspositionen (manuelles Abgleichen) oder durch gleichzeitiges Abgleichen aller verfügbaren Rechnungen (automatisches Abgleichen) erfolgen.</span><span class="sxs-lookup"><span data-stu-id="c2e19-131">This can be done by matching the invoice lines one-by-one (manual matching), or by matching all available invoices at once (auto matching).</span></span>

### <a name="auto-matching"></a><span data-ttu-id="c2e19-132">Automatisches Abgleichen</span><span class="sxs-lookup"><span data-stu-id="c2e19-132">Auto matching</span></span>

<span data-ttu-id="c2e19-133">Wenn mehrere Frachtrechnungen mit demselben Frachtbrief abgeglichen werden, funktioniert der automatische Abgleich wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c2e19-133">When matching multiple freight invoices to the same freight bill, the process for auto matching works as follows:</span></span>

1. <span data-ttu-id="c2e19-134">Alle nicht abgeglichenen Frachtrechnungen werden nach Betrag sortiert, wobei der größte Betrag zuerst angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c2e19-134">All freight invoices not matched are sorted by amount, with largest amount first.</span></span>
1. <span data-ttu-id="c2e19-135">Die Frachtrechnungen werden nacheinander abgeglichen, bis auf dem Frachtbrief kein positiver Betrag mehr vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c2e19-135">The freight invoices are matched one-by-one, until the freight bill has no positive amount remaining.</span></span>
1. <span data-ttu-id="c2e19-136">Abhängig von der Einrichtung des Überwachungsmasters und dem Restbetrag auf den Frachtrechnungen wird der Restbetrag festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c2e19-136">Depending on the setup of the audit master and the remaining amount on the freight invoices, the remaining amount is set.</span></span>

### <a name="manual-matching"></a><span data-ttu-id="c2e19-137">Manuelle Zuordnung</span><span class="sxs-lookup"><span data-stu-id="c2e19-137">Manual matching</span></span>

<span data-ttu-id="c2e19-138">Alle Frachtbriefe mit positiven Beträgen stehen zum Abgleich zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="c2e19-138">All freight bills with positive amounts will be available for matching.</span></span> <span data-ttu-id="c2e19-139">Ähnlich wie beim automatischen Abgleich kann der Benutzer nur Frachtrechnungen mit negativen Beträgen mit Frachtbriefen abgleichen, die nicht vollständig abgeglichen wurden.</span><span class="sxs-lookup"><span data-stu-id="c2e19-139">Similar to auto matching, the user will only be able to match freight invoices with negative amounts to freight bills not fully matched.</span></span>

### <a name="example"></a><span data-ttu-id="c2e19-140">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c2e19-140">Example</span></span>

<span data-ttu-id="c2e19-141">Angenommen, Ihnen liegt ein Frachtbrief (FB) über einen Betrag von 1.500 vor und Sie haben für den Frachtbrief drei Frachtrechnungen erstellt mit einer Rechnungsposition für jede Rechnung und mit folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="c2e19-141">Suppose that you have a freight bill (FB) for an amount of 1500 and you have created three freight invoices for the freight bill with one invoice line for each invoice with following settings:</span></span>

- <span data-ttu-id="c2e19-142">Ursprünglicher Frachtbrief (FB): Betrag 1.500</span><span class="sxs-lookup"><span data-stu-id="c2e19-142">Original freight bill (FB): Amount 1500</span></span>
- <span data-ttu-id="c2e19-143">Rechnung 1 (Inv1): Betrag 1.000</span><span class="sxs-lookup"><span data-stu-id="c2e19-143">Invoice 1 (Inv1): Amount 1000</span></span>
- <span data-ttu-id="c2e19-144">Rechnung 2 (Inv2): Betrag 600</span><span class="sxs-lookup"><span data-stu-id="c2e19-144">Invoice 2 (Inv2): Amount 600</span></span>
- <span data-ttu-id="c2e19-145">Rechnung 3 (Inv3): Betrag –100</span><span class="sxs-lookup"><span data-stu-id="c2e19-145">Invoice 3 (Inv3): Amount -100</span></span>

#### <a name="automatic-matching-result"></a><span data-ttu-id="c2e19-146">Ergebnis des automatischen Abgleichs</span><span class="sxs-lookup"><span data-stu-id="c2e19-146">Automatic matching result</span></span>

<span data-ttu-id="c2e19-147">Der automatische Abgleich wird in der folgenden Reihenfolge ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="c2e19-147">Auto matching will execute in following order:</span></span>

1. <span data-ttu-id="c2e19-148">Alle Frachtrechnungen absteigend nach Betrag sortieren: Inv1 -> Inv2 -> Inv3.</span><span class="sxs-lookup"><span data-stu-id="c2e19-148">Sort all freight invoices descending by amount: Inv1 -> Inv2 -> Inv3.</span></span>
1. <span data-ttu-id="c2e19-149">Gleichen Sie Inv1 mit FB ab.</span><span class="sxs-lookup"><span data-stu-id="c2e19-149">Match Inv1 with FB.</span></span> <span data-ttu-id="c2e19-150">Für Inv1 wird ein Betrag von 1.000 abgeglichen und auf dem FB verbleibt ein Betrag von 500. Der Status wird daher auf *Teilweise abgeglichen* gesetzt.</span><span class="sxs-lookup"><span data-stu-id="c2e19-150">Inv1 has 1000 matched and FB has 500 amount remaining, so the status is set to *Partially matched*.</span></span>
1. <span data-ttu-id="c2e19-151">Gleichen Sie Inv2 mit FB ab.</span><span class="sxs-lookup"><span data-stu-id="c2e19-151">Match Inv2 with FB.</span></span> <span data-ttu-id="c2e19-152">Für Inv2 wird ein Betrag von 500 abgeglichen und auf dem FB verbleibt ein Betrag von 0. Der Status wird daher auf *Vollständig abgeglichen* gesetzt.</span><span class="sxs-lookup"><span data-stu-id="c2e19-152">Inv2 has 500 matched and FB has 0 remaining, so the status is set to *Fully matched*.</span></span>
1. <span data-ttu-id="c2e19-153">Da der FB jetzt vollständig abgeglichen wurde, wird Inv3 nicht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="c2e19-153">Because FB is now fully matched, Inv3 won't be processed.</span></span>

#### <a name="manual-matching-result"></a><span data-ttu-id="c2e19-154">Ergebnis des manuellen Abgleichs</span><span class="sxs-lookup"><span data-stu-id="c2e19-154">Manual matching result</span></span>

<span data-ttu-id="c2e19-155">Beim manuellen Abgleich variieren die Ergebnisse in Abhängigkeit von der Reihenfolge des Abgleichs, wie in den folgenden Beispielfällen dargestellt.</span><span class="sxs-lookup"><span data-stu-id="c2e19-155">For manual matching, the results vary depending on the order of the matching, as illustrated in the following example cases.</span></span>

##### <a name="manual-matching-case-1"></a><span data-ttu-id="c2e19-156">Manueller Abgleich Fall 1</span><span class="sxs-lookup"><span data-stu-id="c2e19-156">Manual matching case 1</span></span>

<span data-ttu-id="c2e19-157">Eine Möglichkeit zum manuellen Abgleich für dieses Beispiel besteht darin, wie folgt vorzugehen:</span><span class="sxs-lookup"><span data-stu-id="c2e19-157">One way to do manual matching for this example is to proceed as follows:</span></span>

1. <span data-ttu-id="c2e19-158">Gleichen Sie den FB mit Inv1 ab.</span><span class="sxs-lookup"><span data-stu-id="c2e19-158">Match FB with Inv1.</span></span> <span data-ttu-id="c2e19-159">Auf dem FB verbleibt ein Betrag von 500, sodass der Status auf *Teilweise abgeglichen* gesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="c2e19-159">FB has 500 amount remaining, so the status set to *Partially matched*.</span></span>
1. <span data-ttu-id="c2e19-160">Gleichen Sie Inv2 mit FB ab.</span><span class="sxs-lookup"><span data-stu-id="c2e19-160">Match Inv2 with FB.</span></span> <span data-ttu-id="c2e19-161">Für Inv2 wird ein Betrag von 500 abgeglichen und auf dem FB verbleibt ein Betrag von 0. Der Status wird daher auf *Vollständig abgeglichen* gesetzt.</span><span class="sxs-lookup"><span data-stu-id="c2e19-161">Inv2 has 500 matched and FB has 0 remaining, so the status is set to *Fully matched*.</span></span>
1. <span data-ttu-id="c2e19-162">Wenn Sie Inv3 manuell abgleichen, werden Sie keine nicht nicht abgeglichenen Frachtbriefe finden.</span><span class="sxs-lookup"><span data-stu-id="c2e19-162">When manually matching Inv3, you won't find any unmatched freight bills.</span></span>

<span data-ttu-id="c2e19-163">Dieser Fall entspricht im Wesentlichen dem automatischen Abgleich.</span><span class="sxs-lookup"><span data-stu-id="c2e19-163">This case is essentially the same as auto matching</span></span>

##### <a name="manual-matching-case-2"></a><span data-ttu-id="c2e19-164">Manueller Abgleich Fall 2</span><span class="sxs-lookup"><span data-stu-id="c2e19-164">Manual matching case 2</span></span>

<span data-ttu-id="c2e19-165">Eine weitere Möglichkeit zum manuellen Abgleich für dieses Beispiel besteht darin, wie folgt vorzugehen:</span><span class="sxs-lookup"><span data-stu-id="c2e19-165">Another way to do manual matching for this example is to proceed as follows:</span></span>

1. <span data-ttu-id="c2e19-166">Gleichen Sie Inv3 mit dem FB ab.</span><span class="sxs-lookup"><span data-stu-id="c2e19-166">Match Inv3 with FB.</span></span> <span data-ttu-id="c2e19-167">Jetzt verbleibt auf dem FB ein Betrag von 1.600, was der Subtraktion von –100 von 1.500 entspricht.</span><span class="sxs-lookup"><span data-stu-id="c2e19-167">Now FB has amount remaining 1600, which is the same as subtracting negative 100 on top of 1500.</span></span> <span data-ttu-id="c2e19-168">Sowohl der FB als auch Inv3 haben eine abgeglichene Menge von –100.</span><span class="sxs-lookup"><span data-stu-id="c2e19-168">Both FB and Inv3 have a matched quantity of -100.</span></span>
1. <span data-ttu-id="c2e19-169">Gleichen Sie Inv1 und Inv 2 nacheinander mit FB ab.</span><span class="sxs-lookup"><span data-stu-id="c2e19-169">Match Inv1 and Inv 2 with FB one after another.</span></span> <span data-ttu-id="c2e19-170">Der FB ist vollständig abgeglichen.</span><span class="sxs-lookup"><span data-stu-id="c2e19-170">FB is fully matched.</span></span>

<span data-ttu-id="c2e19-171">Wie dieses Beispiel zeigt, sollte der Abgleich von Frachtrechnungen mit negativen Beträgen nur manuell erfolgen.</span><span class="sxs-lookup"><span data-stu-id="c2e19-171">As this example shows, matching freight invoices with negative amounts should only be done manually.</span></span> <span data-ttu-id="c2e19-172">Dadurch wird sichergestellt, dass es immer möglich ist, die Frachtrechnungen mit negativen Beträgen mit einem nicht vollständig abgeglichenen Frachtbrief abzugleichen, da Sie so die Reihenfolge des Abgleichs steuern können.</span><span class="sxs-lookup"><span data-stu-id="c2e19-172">This will ensure that it is always possible to match the freight invoices with negative amounts to a freight bill not fully matched because that enables you to control the matching sequence.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]