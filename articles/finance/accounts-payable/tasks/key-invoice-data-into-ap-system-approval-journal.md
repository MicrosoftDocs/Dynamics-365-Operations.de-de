---
title: Rechnungsdaten mit einer Genehmigungserfassung in Kreditorenkonten eingeben
description: In diesem Thema wird erläutert, wie das Rechnungsregister verwendet wird, um Rechnungen zu erstellen und anschließend die Genehmigungserfassung verwendet wird, um die Ausgabenkonten zu aktualisieren.
author: abruer
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransInvoiceRegister, HcmWorkerLookUp, LedgerJournalTransApprove, LedgerJournalTransApproveFetchVouchers, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 788397b5c9a3f42e373f7cdad256c1ee3d058e57
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4443411"
---
# <a name="key-invoice-data-into-accounts-payable-using-an-approval-journal"></a><span data-ttu-id="ffd9b-103">Rechnungsdaten mit einer Genehmigungserfassung in Kreditorenkonten eingeben</span><span class="sxs-lookup"><span data-stu-id="ffd9b-103">Key invoice data into accounts payable using an approval journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ffd9b-104">In diesem Thema wird erläutert, wie das Rechnungsregister verwendet wird, um Rechnungen zu erstellen und anschließend die Genehmigungserfassung verwendet wird, um die Ausgabenkonten zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="ffd9b-104">This topic explains how to use the invoice register to create invoices and then use the approval journal to update the expense accounts.</span></span>

## <a name="create-and-post-and-invoice"></a><span data-ttu-id="ffd9b-105">Erstellen und buchen und fakturieren</span><span class="sxs-lookup"><span data-stu-id="ffd9b-105">Create and post and invoice</span></span>
1. <span data-ttu-id="ffd9b-106">Wechseln Sie im Navigationsbereich zu **Module > Kreditoren > Rechnungen > Rechnungserfassung**.</span><span class="sxs-lookup"><span data-stu-id="ffd9b-106">In the navigation pan, go to **Modules > Accounts payable > Invoices > Invoice register**.</span></span>
2. <span data-ttu-id="ffd9b-107">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="ffd9b-107">Select **New**.</span></span>
3. <span data-ttu-id="ffd9b-108">Wählen Sie den Namen des Rechnungsregisters aus, den Sie benutzen möchten.</span><span class="sxs-lookup"><span data-stu-id="ffd9b-108">Select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="ffd9b-109">Klicken Sie auf **Positionen**, um das Register zu öffnen und Ausgabenpositionen einzugeben.</span><span class="sxs-lookup"><span data-stu-id="ffd9b-109">Select **Lines** to open the register and enter expense lines.</span></span>
5. <span data-ttu-id="ffd9b-110">Wählen Sie einen Kreditor aus.</span><span class="sxs-lookup"><span data-stu-id="ffd9b-110">Select a vendor.</span></span> <span data-ttu-id="ffd9b-111">Geben Sie beispielsweise `US-104` ein oder wählen Sie es aus.</span><span class="sxs-lookup"><span data-stu-id="ffd9b-111">For example, enter or select `US-104`.</span></span>
6. <span data-ttu-id="ffd9b-112">Geben Sie im Feld **Rechnung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="ffd9b-112">In the **Invoice** field, type a value.</span></span>
7. <span data-ttu-id="ffd9b-113">Geben Sie im Feld **Beschreibung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="ffd9b-113">In the **Description** field, type a value.</span></span>
8. <span data-ttu-id="ffd9b-114">Geben Sie im Feld **Kredit** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="ffd9b-114">In the **Credit** field, enter a number.</span></span>
9. <span data-ttu-id="ffd9b-115">Wählen Sie im Feld **Genehmigt von** einen Genehmiger in der Dropdownliste aus.</span><span class="sxs-lookup"><span data-stu-id="ffd9b-115">In the **Approved by** field, select an approver from the drop-down menu.</span></span>
10. <span data-ttu-id="ffd9b-116">Wählen Sie **Buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="ffd9b-116">Select **Post**.</span></span>

## <a name="approve-an-invoice"></a><span data-ttu-id="ffd9b-117">Genehmigen einer Rechnung</span><span class="sxs-lookup"><span data-stu-id="ffd9b-117">Approve an invoice</span></span>
1. <span data-ttu-id="ffd9b-118">Wechseln Sie im Navigationsbereich zu **Module > Kreditoren > Rechnungen > Rechnungsgenehmigung**.</span><span class="sxs-lookup"><span data-stu-id="ffd9b-118">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice approval**.</span></span>
2. <span data-ttu-id="ffd9b-119">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="ffd9b-119">Select **New**.</span></span>
3. <span data-ttu-id="ffd9b-120">Wählen Sie den Namen der Rechnungsgenehmigungserfassung aus, den Sie benutzen möchten.</span><span class="sxs-lookup"><span data-stu-id="ffd9b-120">Select the name of the invoice approval journal that you want to use.</span></span>
4. <span data-ttu-id="ffd9b-121">Klicken Sie auf **Positionen**, um eine Seite anzuzeigen, auf der Sie die Rechnungen auswählen können, die Sie genehmigen möchten.</span><span class="sxs-lookup"><span data-stu-id="ffd9b-121">Select **Lines** to display a page where you will be able to select the invoices that you want to approve.</span></span>
5. <span data-ttu-id="ffd9b-122">Wählen Sie **Belege suchen** aus, um alle Rechnungen anzuzeigen, die zur Genehmigung bereit sind.</span><span class="sxs-lookup"><span data-stu-id="ffd9b-122">Select **Find Vouchers** to display all of the invoices that are ready for approval.</span></span>
6. <span data-ttu-id="ffd9b-123">Markieren Sie die Rechnung, die Sie erstellt haben, klicken Sie **Auswählen**.</span><span class="sxs-lookup"><span data-stu-id="ffd9b-123">Mark the invoice that you created, then click **Select**.</span></span> <span data-ttu-id="ffd9b-124">Die Belege, die Sie oben ausgewählt haben, werden auf diese Liste verschoben, nachdem Sie sie auswählen.</span><span class="sxs-lookup"><span data-stu-id="ffd9b-124">The vouchers that you selected above are moved to this list after you select them.</span></span>  
7. <span data-ttu-id="ffd9b-125">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="ffd9b-125">Select **OK**.</span></span>
8. <span data-ttu-id="ffd9b-126">Wählen Sie das Feld **Kontonummern**, um ein Ausgabenkonto der Rechnung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="ffd9b-126">Select the **account number** field to add an expense account to the invoice.</span></span>
9. <span data-ttu-id="ffd9b-127">Geben Sie eine Kontonummer ein und bewegen Sie die Tabulatortaste vom Feld weg.</span><span class="sxs-lookup"><span data-stu-id="ffd9b-127">Enter an account number and tab off of the field.</span></span> <span data-ttu-id="ffd9b-128">Geben Sie beispielsweise `600120` ein.</span><span class="sxs-lookup"><span data-stu-id="ffd9b-128">For example, enter `600120`.</span></span>
10. <span data-ttu-id="ffd9b-129">Wählen Sie **Buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="ffd9b-129">Select **Post**.</span></span>
11. <span data-ttu-id="ffd9b-130">Wählen Sie **Beleg** aus, um die Einträge anzuzeigen, die gebucht wurden.</span><span class="sxs-lookup"><span data-stu-id="ffd9b-130">Select **Voucher** to view the entries that were posted.</span></span> <span data-ttu-id="ffd9b-131">Das Konto "Rechnung mit ausstehender Genehmigung" wird zurückgesetzt und durch das tatsächliche Ausgabenkonto ersetzt.</span><span class="sxs-lookup"><span data-stu-id="ffd9b-131">The Invoice Pending Approval account is reversed and replaced with the actual expense account.</span></span>  

