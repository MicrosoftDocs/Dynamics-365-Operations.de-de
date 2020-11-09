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
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSInvoiceTable, TMSFreightBillDetail, TMSFreightBillTypeAssignment, TMSFBDetailReconcile, TMSRejectInvoiceLine, TMSMiscellaneousCharge
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8472094ba532d531b15dc4e9f120646b2c3bbe96
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017298"
---
# <a name="reconcile-freight-in-transportation-management"></a><span data-ttu-id="7d17c-103">Fracht in der Transportverwaltung abstimmen</span><span class="sxs-lookup"><span data-stu-id="7d17c-103">Reconcile freight in transportation management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7d17c-104">Dieser Artikel beschreibt den Frachtabstimmungsprozess.</span><span class="sxs-lookup"><span data-stu-id="7d17c-104">This topic describes the freight reconciliation process.</span></span>

<span data-ttu-id="7d17c-105">Die Frachtabstimmung kann manuell oder automatischen durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="7d17c-105">Freight reconciliation can be done manually, or it can be set up to occur automatically.</span></span> <span data-ttu-id="7d17c-106">Um die automatische Frachtabstimmung zu verwenden, müssen Sie einen Überwachungsmaster einrichten. In ihm können Sie die Kriterien definieren, die festlegen, welche Fracht automatisch abgestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="7d17c-106">To use automatic freight reconciliation, you must set up an audit master where you can define criteria that determine which freight bills are matched automatically.</span></span>

## <a name="the-freight-reconciliation-process"></a><span data-ttu-id="7d17c-107">Der Frachtabstimmungsprozess</span><span class="sxs-lookup"><span data-stu-id="7d17c-107">The freight reconciliation process</span></span>
<span data-ttu-id="7d17c-108">Frachtkosten werden vom den Tarifmodul berechnet, das dem relevanten Spediteur zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="7d17c-108">Freight rates are calculated by the rate engine that is associated with the relevant shipping carrier.</span></span> <span data-ttu-id="7d17c-109">Wenn ein Ladung bestätigt ist, wird ein Frachtbrief erstellt und die Frachtkosten werden an diesen übertragen.</span><span class="sxs-lookup"><span data-stu-id="7d17c-109">When a load is confirmed, a freight bill is generated, and the freight rates are transferred to it.</span></span> <span data-ttu-id="7d17c-110">Die Frachtkosten werden je nach Konfiguration für den regulären Abrechnungsprozess als sonstige Zuschläge auf das entsprechende Quelldokument umgelegt (Bestellung, Auftrag und/oder Umlagerungsauftrag).</span><span class="sxs-lookup"><span data-stu-id="7d17c-110">The freight rates are apportioned as miscellaneous charges to the relevant source document (purchase order, sales order, and/or transfer order), depending on the setup that is used for the regular billing process.</span></span> <span data-ttu-id="7d17c-111">Der Frachtabstimmungsprozesse (auch Abgleichsprozess genannt) kann starten sobald die Frachtrechnung vom Spediteur eingeht.</span><span class="sxs-lookup"><span data-stu-id="7d17c-111">The freight reconciliation process (which is also known as the matching process) can start as soon as the freight invoice arrives from the shipping carrier.</span></span> <span data-ttu-id="7d17c-112">Die Rechnung elektronisch oder auf Papier erhalten werden.</span><span class="sxs-lookup"><span data-stu-id="7d17c-112">The invoice can be received electronically or on paper.</span></span> <span data-ttu-id="7d17c-113">Wenn die Rechnung auf Papier erhalten wird, können Sie mit dem Frachtbrief als Vorlage eine elektronische Rechnung generieren.</span><span class="sxs-lookup"><span data-stu-id="7d17c-113">If the invoice is received on paper, you can generate an electronic invoice by using the freight bill as a template.</span></span> 

<span data-ttu-id="7d17c-114">[![Frachtabstimmungsprozess](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span><span class="sxs-lookup"><span data-stu-id="7d17c-114">[![Freight reconcilation process](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span></span>

## <a name="manual-reconciliation"></a><span data-ttu-id="7d17c-115">Manuelle Abstimmung</span><span class="sxs-lookup"><span data-stu-id="7d17c-115">Manual reconciliation</span></span>
<span data-ttu-id="7d17c-116">Wenn Sie die Fracht manuell abstimmen, müssen Sie jede Rechnungsposition mit der Frachtbriefposition oder den-positionen für die zu fakturierende Ladung abgleichen.</span><span class="sxs-lookup"><span data-stu-id="7d17c-116">If you're reconciling freight manually, you must match each invoice line with the freight bill line or lines for the load that is being invoiced.</span></span> <span data-ttu-id="7d17c-117">Diesen Abgleich führen Sie auf der Seite **Frachtbrief- und Rechnungsabgleich** durch.</span><span class="sxs-lookup"><span data-stu-id="7d17c-117">You do this matching on the **Freight bill and invoice matching** page.</span></span> <span data-ttu-id="7d17c-118">Wenn der Betrag der Rechnungsposition nicht mit dem Frachtbriefbetrag übereinstimmt, müssen Sie einen Abstimmungsgrund für die Abweichung auswählen.</span><span class="sxs-lookup"><span data-stu-id="7d17c-118">If the amount on the invoice line doesn’t match the freight bill amount, you must select a reconciliation reason for the difference.</span></span> <span data-ttu-id="7d17c-119">Sind mehrere Gründe für die Abstimmung zutreffen, können Sie die nicht abgeglichenen Mengen auf diese Gründe verteilen.</span><span class="sxs-lookup"><span data-stu-id="7d17c-119">If there are multiple reasons for reconciliation, you can split the unmatched amount across them.</span></span> <span data-ttu-id="7d17c-120">Der Abstimmungsgrund bestimmt, wie die Differenzbeträge im Hauptbuch gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="7d17c-120">The reconciliation reason determines how the difference amounts are posted in the general ledger.</span></span> <span data-ttu-id="7d17c-121">Bei die Abstimmung des gesamten Rechnungsbetrags gebucht wird, wird dieser zur Genehmigung gesendet. Dann wird die Erfassung gebucht.</span><span class="sxs-lookup"><span data-stu-id="7d17c-121">When the reconciliation of the whole invoice amount is accounted for, it's submitted for approval, and then the journal is posted.</span></span> <span data-ttu-id="7d17c-122">Die folgende Abbildung zeigt, wie eine Frachtrechnung generiert und eine Frachtabstimmung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7d17c-122">The following illustration shows how to generate a freight invoice and do freight reconciliation.</span></span> 
<span data-ttu-id="7d17c-123">[![Frachtabstimmungsaufgaben](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span><span class="sxs-lookup"><span data-stu-id="7d17c-123">[![Freight reconcilation tasks](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span></span>
## <a name="automatic-reconciliation"></a><span data-ttu-id="7d17c-124">Automatische Abstimmung</span><span class="sxs-lookup"><span data-stu-id="7d17c-124">Automatic reconciliation</span></span>
<span data-ttu-id="7d17c-125">Um die automatische Abstimmung zu verwenden, müssen Sie den Zeitplan für die Abstimmung und die zu verwendenden Rechnungen und Spediteure angeben.</span><span class="sxs-lookup"><span data-stu-id="7d17c-125">To use automatic reconciliation, you must specify the schedule for reconciliation, and the invoices and shipping carriers to use.</span></span> <span data-ttu-id="7d17c-126">Der Abgleich der Rechnungspositionen und Frachtbriefe wird entsprechend der Einrichtung des Überwachungsmasters und der Frachtbriefart ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7d17c-126">The matching of the invoice lines and freight bills is done according to the setup of the audit master and freight bill type.</span></span> <span data-ttu-id="7d17c-127">Nach dem Ausführen der automatischen Abstimmung müssen Sie alle Rechnungen bearbeiten, die das System nicht zuordnen kann.</span><span class="sxs-lookup"><span data-stu-id="7d17c-127">After you run the automatic reconciliation, you must handle any invoices that the system can't match.</span></span> <span data-ttu-id="7d17c-128">Sie müssen diese Rechnungen dann manuell verarbeiten, bevor Sie alle Rechnung für die Zahlung buchen können.</span><span class="sxs-lookup"><span data-stu-id="7d17c-128">You must then process these invoices manually before you can post all the invoices for payment.</span></span>



