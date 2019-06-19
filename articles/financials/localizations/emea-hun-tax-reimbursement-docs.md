---
title: Steuerrückerstattungsdokumente für Ungarn
description: In diesem Thema wird erläutert, wie Steuerrückerstattungsdokumente für Ungarn eingerichtet und erstellt werden.
author: ShylaThompson
manager: AnnBe
ms.date: 03/27/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Austria
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7f7ae1baf4c79b7938fcf666e43e8e71087a4f64
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545475"
---
# <a name="tax-reimbursement-documents-for-hungary"></a><span data-ttu-id="cfd7a-103">Steuerrückerstattungsdokumente für Ungarn</span><span class="sxs-lookup"><span data-stu-id="cfd7a-103">Tax reimbursement documents for Hungary</span></span>

[!include [banner](../includes/banner.md)]

## <a name="set-up-parameters-for-tax-reimbursement-documents"></a><span data-ttu-id="cfd7a-104">Parameter für Steuerrückerstattungsdokumente einrichten</span><span class="sxs-lookup"><span data-stu-id="cfd7a-104">Set up parameters for tax reimbursement documents</span></span>

<span data-ttu-id="cfd7a-105">Ein Debitor ist ggf. eine Person, die in einem Land oder in einer Region wohnt, die kein Mitglied der Europäischen Union (EU) ist.</span><span class="sxs-lookup"><span data-stu-id="cfd7a-105">A customer might be a person who resides in a country or region that isn't a member of the European Union (EU).</span></span> <span data-ttu-id="cfd7a-106">Debitoren dieses Typs beantragen möglicherweise die Rückerstattung von Mehrwertsteuer (MwSt.), die sie bei Einkäufen bezahlt, die sie in Ungarn vorgenommen haben.</span><span class="sxs-lookup"><span data-stu-id="cfd7a-106">Customers of this type might request reimbursement of value-added tax (VAT) that they paid on purchases that they made in Hungary.</span></span> <span data-ttu-id="cfd7a-107">Diese Debitoren bitten Sie möglicherweise auch darum, den Betrag der MwSt. zu dokumentieren, den sie Ihnen gezahlt haben.</span><span class="sxs-lookup"><span data-stu-id="cfd7a-107">These customers might also ask that you provide documentation of the amount of VAT that they paid to you.</span></span> <span data-ttu-id="cfd7a-108">In diesem Fall können Sie ein Steuerrückerstattungsdokument aus der Debitorenrechnung erstellen.</span><span class="sxs-lookup"><span data-stu-id="cfd7a-108">In this case, you can create a tax reimbursement document from the customer invoice.</span></span>

### <a name="set-up-a-default-exchange-rate"></a><span data-ttu-id="cfd7a-109">Standardwechselkurs einrichten</span><span class="sxs-lookup"><span data-stu-id="cfd7a-109">Set up a default exchange rate</span></span>

<span data-ttu-id="cfd7a-110">Verwenden Sie diese Prozedur, um einen Wechselkurs einzurichten, der automatisch in Steuerrückerstattungsdokumenten aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="cfd7a-110">Use this procedure to set up an exchange rate that is automatically selected in tax reimbursement documents.</span></span>

1. <span data-ttu-id="cfd7a-111">Wählen Sie **Debitoren** &gt; **Einstellungen** &gt; **Debitorenparameter** aus.</span><span class="sxs-lookup"><span data-stu-id="cfd7a-111">Select **Accounts receivable** &gt; **Setup** &gt; **Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="cfd7a-112">Auf der Seite **Debitorenparameter** auf der Registerkarte **Updates** im Inforegister **Sonstiges** im Feld **Steuerrückerstattungsbeleg** wählen Sie den Wechselkurstyp aus, der für Steuerrückerstattungsdokumente standardmäßig verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cfd7a-112">On the **Accounts receivable parameters** page, on the **Updates** tab, on the **Other** FastTab, in the **Tax reimbursement slip** field, select the type of exchange rate that should be used by default for tax reimbursement documents.</span></span>

### <a name="set-up-a-number-sequence"></a><span data-ttu-id="cfd7a-113">Einrichten eines Nummernkreises</span><span class="sxs-lookup"><span data-stu-id="cfd7a-113">Set up a number sequence</span></span>

<span data-ttu-id="cfd7a-114">Verwenden Sie diese Prozedur, um einen Nummernkreis einzurichten, der automatisch den Steuerrückerstattungsdokumenten zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="cfd7a-114">Use this procedure to set up a number sequence that is automatically assigned to tax reimbursement documents.</span></span>

1. <span data-ttu-id="cfd7a-115">Wählen Sie **Debitoren** &gt; **Einstellungen** &gt; **Debitorenparameter** aus.</span><span class="sxs-lookup"><span data-stu-id="cfd7a-115">Select **Accounts receivable** &gt; **Setup** &gt; **Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="cfd7a-116">Auf der Seite **Debitorenparameter** auf der Registerkarte **Nummernkreise**, im Feld **Referenz**, wählen Sie **Steuerrückerstattungsdokument** aus.</span><span class="sxs-lookup"><span data-stu-id="cfd7a-116">On the **Accounts receivable parameters** page, on the **Number sequences** tab, in the **Reference** field, select **Tax reimbursement document**.</span></span>
3. <span data-ttu-id="cfd7a-117">Wählen Sie im Feld **Nummernkreiscode** einen Nummernkreis für Steuerrückerstattungsdokumente aus.</span><span class="sxs-lookup"><span data-stu-id="cfd7a-117">In the **Number sequence code** field, select a number sequence for tax reimbursement documents.</span></span>
4. <span data-ttu-id="cfd7a-118">Füllen Sie die verbleibenden optionalen Felder aus.</span><span class="sxs-lookup"><span data-stu-id="cfd7a-118">Complete the remaining optional fields.</span></span>

## <a name="create-and-print-a-tax-reimbursement-document"></a><span data-ttu-id="cfd7a-119">Erstellen und Drucken eines Steuerrückerstattungsdokuments</span><span class="sxs-lookup"><span data-stu-id="cfd7a-119">Create and print a tax reimbursement document</span></span>

<span data-ttu-id="cfd7a-120">Sie können ein Steuerrückerstattungsdokument für Debitoren bereitstellen, die Ihnen MwSt. gezahlt haben.</span><span class="sxs-lookup"><span data-stu-id="cfd7a-120">You can provide a tax reimbursement document to customers who have paid VAT to you.</span></span> <span data-ttu-id="cfd7a-121">Debitoren können das Steuerrückerstattungsdokument verwenden, um eine Mehrwertsteuererrückerstattung von der Steuerbehörde zu beanspruchen.</span><span class="sxs-lookup"><span data-stu-id="cfd7a-121">Customers can use the tax reimbursement document to claim a VAT reimbursement from the authorities.</span></span>

<span data-ttu-id="cfd7a-122">Das Steuerrückerstattungsdokument ist nur verfügbar, wenn der Debitor als Person auf der Seite **Debitoren** eingerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="cfd7a-122">The tax reimbursement document is available only if the customer is set up as a person on the **Customers** page.</span></span> <span data-ttu-id="cfd7a-123">Auf der Seite **Debitoren** auf dem Inforegister **Allgemein** bestätigen Sie, dass das Feld **Datensatztyp** auf **Person** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="cfd7a-123">On the **Customers** page, on the **General** FastTab, confirm that the **Record type** field is set to **Person**.</span></span>

### <a name="set-up-print-management-for-a-tax-reimbursement-document"></a><span data-ttu-id="cfd7a-124">Einrichten der Druckverwaltung für ein Steuerrückerstattungsdokument</span><span class="sxs-lookup"><span data-stu-id="cfd7a-124">Set up print management for a tax reimbursement document</span></span>

1. <span data-ttu-id="cfd7a-125">Wählen Sie **Debitoren** &gt; **Einstellungen** &gt; **Formulare** &gt; **Formulareinstellungen** aus.</span><span class="sxs-lookup"><span data-stu-id="cfd7a-125">Select **Accounts receivable** &gt; **Setup** &gt; **Forms** &gt; **Form setup**.</span></span>
2. <span data-ttu-id="cfd7a-126">Auf der Seite **Formulareinstellungen** auf der Registerkarte **Allgemein** wählen Sie **Druckverwaltung** aus.</span><span class="sxs-lookup"><span data-stu-id="cfd7a-126">On the **Form setup** page, on the **General** tab, select **Print management**.</span></span>
3. <span data-ttu-id="cfd7a-127">Auf der Seite **Druckverwaltungseinstellungen** unter **Modul – Debitoren** wählen Sie **Steuerrückerstattungsbeleg** aus.</span><span class="sxs-lookup"><span data-stu-id="cfd7a-127">On the **Print management setup** page, under **Module - accounts receivable**, select **Tax reimbursement slip**.</span></span>
4. <span data-ttu-id="cfd7a-128">Unter **Modul – Lagerverwaltung** &gt; **Kommissionierliste** wählen Sie entweder **Original** oder **Kopie** aus.</span><span class="sxs-lookup"><span data-stu-id="cfd7a-128">Under **Module - inventory management** &gt; **Picking list**, select either **Original** or **Copy**.</span></span>
5. <span data-ttu-id="cfd7a-129">Geben Sie im rechten Fensterbereich Informationen darüber ein, was gedruckt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cfd7a-129">In the right pane, enter information about what should be printed.</span></span>
6. <span data-ttu-id="cfd7a-130">Optional: Geben Sie im Feld **Fußzeilentext** den Text ein, der unten im Steuerrückerstattungsdokument gedruckt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cfd7a-130">Optional: In the **Footer text** field, enter text that should be printed at the bottom of the tax reimbursement document.</span></span>

### <a name="select-invoice-lines-for-a-tax-reimbursement-document"></a><span data-ttu-id="cfd7a-131">Rechnungspositionen für ein Steuerrückerstattungsdokument auswählen</span><span class="sxs-lookup"><span data-stu-id="cfd7a-131">Select invoice lines for a tax reimbursement document</span></span>

1. <span data-ttu-id="cfd7a-132">Wählen Sie **Debitoren** &gt; **Abfragen und Berichte** &gt; **Erfassungen** &gt; **Rechnungserfassung** aus.</span><span class="sxs-lookup"><span data-stu-id="cfd7a-132">Select **Accounts receivable** &gt; **Inquiries and reports** &gt; **Journals** &gt; **Invoice journal**.</span></span>
2. <span data-ttu-id="cfd7a-133">Auf der Seite **Rechnungserfassung** auf der Registerkarte **Übersicht** wählen Sie die Debitorenrechnung aus, für die der Debitor eine Steuerrückerstattung anfordert.</span><span class="sxs-lookup"><span data-stu-id="cfd7a-133">On the **Invoice journal** page, on the **Overview** tab, select the customer invoice that the customer is requesting tax reimbursement for.</span></span>
3. <span data-ttu-id="cfd7a-134">Aktivieren Sie das Kontrollkästchen **Steuerrückerstattung** für die ausgewählte Rechnung.</span><span class="sxs-lookup"><span data-stu-id="cfd7a-134">Select the **Tax reimbursement** check box for the selected invoice.</span></span>
4. <span data-ttu-id="cfd7a-135">Standardmäßig sind auf der Registerkarte **Positionen**, im Feld **Steuerrückerstattungspositionen** alle Rechnungspositionen ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="cfd7a-135">By default, on the **Lines** tab, in the **Tax reimbursement lines** field, all invoice lines are selected.</span></span> <span data-ttu-id="cfd7a-136">Deaktivieren Sie das Kontrollkästchen für jede Rechnungsposition, die vom Steuerrückerstattungsdokument ausgeschlossen werden soll.</span><span class="sxs-lookup"><span data-stu-id="cfd7a-136">Clear the check box for any invoice line that should be excluded from the tax reimbursement document.</span></span>
5. <span data-ttu-id="cfd7a-137">Auf der Registerkarte **Übersicht** wählen Sie **Steuerrückerstattung** &gt; **Vorschau des Originals** aus, um das Dokument anzuzeigen, bevor Sie es drucken.</span><span class="sxs-lookup"><span data-stu-id="cfd7a-137">On the **Overview** tab, select **Tax reimbursement** &gt; **Original preview** to view the document before you print it.</span></span>
6. <span data-ttu-id="cfd7a-138">Optional: Wählen Sie **Steuerrückerstattung** &gt; **Druckverwaltung verwenden** aus, um die Druckeinstellungen zu ändern, beispielsweise die Anzahl der zu druckenden Kopien.</span><span class="sxs-lookup"><span data-stu-id="cfd7a-138">Optional: Select **Tax reimbursement** &gt; **Use print management** to modify the print settings, such as the number of copies to print.</span></span>
7. <span data-ttu-id="cfd7a-139">Überprüfen Sie auf der Seite **Original anzeigen** die Informationen, und drucken Sie dann das Steuerrückerstattungsdokument.</span><span class="sxs-lookup"><span data-stu-id="cfd7a-139">On the **View original** page, review the information, and then print the tax reimbursement document.</span></span>

<span data-ttu-id="cfd7a-140">Wenn Sie ein Steuerrückerstattungsdokument drucken, wird die Dokumentnummer, die dem Dokument zugewiesen ist, im Feld **Steuerrückerstattungsdokument** auf der Seite **Rechnungserfassung** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cfd7a-140">When you print a tax reimbursement document, the document number that is assigned to the document appears in the **Tax reimbursement document** field on the **Invoice journal** page.</span></span> <span data-ttu-id="cfd7a-141">Das Kontrollkästchen **Steuerrückerstattung** ist für die Positionen, die Sie in das Steuerrückerstattungsdokument einbezogen haben, nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cfd7a-141">The **Tax reimbursement** check box is unavailable for the lines that you included in the tax reimbursement document.</span></span>

### <a name="settle-a-tax-reimbursement"></a><span data-ttu-id="cfd7a-142">Eine Steuerrückerstattung ausgleichen</span><span class="sxs-lookup"><span data-stu-id="cfd7a-142">Settle a tax reimbursement</span></span>

<span data-ttu-id="cfd7a-143">Wenn Ihre Organisation einem Debitor für Mehrwertsteuer Erstattung bietet, müssen Sie die Rückerstattung in der Rechnungserfassung angeben.</span><span class="sxs-lookup"><span data-stu-id="cfd7a-143">When your organization reimburses a customer for VAT, you must indicate the reimbursement in the invoice journal.</span></span> <span data-ttu-id="cfd7a-144">Andernfalls könnte der Debitor dieselbe Rückerstattung doppelt erhalten.</span><span class="sxs-lookup"><span data-stu-id="cfd7a-144">Otherwise, the customer could receive a duplicate reimbursement.</span></span> <span data-ttu-id="cfd7a-145">Gehen Sie folgendermaßen vor, um Rechnungspositionen auszugleichen, für die ein Debitor eine MwSt.-Rückerstattung empfangen hat.</span><span class="sxs-lookup"><span data-stu-id="cfd7a-145">Use the following procedure to settle invoice lines that a customer received a VAT reimbursement for.</span></span>

1. <span data-ttu-id="cfd7a-146">Wählen Sie **Debitoren** &gt; **Abfragen und Berichte** &gt; **Erfassungen** &gt; **Rechnungserfassung** aus.</span><span class="sxs-lookup"><span data-stu-id="cfd7a-146">Select **Accounts receivable** &gt; **Inquiries and reports** &gt; **Journals** &gt; **Invoice journal**.</span></span>
2. <span data-ttu-id="cfd7a-147">Auf der Seite **Rechnungserfassung** auf der Registerkarte **Übersicht** wählen Sie die Debitorenrechnung aus, für die der Debitor eine Mehrwertsteuerrückerstattung empfangen hat.</span><span class="sxs-lookup"><span data-stu-id="cfd7a-147">On the **Invoice journal** page, on the **Overview** tab, select the customer invoice that the customer received a VAT reimbursement for.</span></span>
3. <span data-ttu-id="cfd7a-148">Wählen Sie **Steuerrückerstattung** &gt; **MwSt. ausgeglichen.** aus.</span><span class="sxs-lookup"><span data-stu-id="cfd7a-148">Select **Tax reimbursement** &gt; **VAT settled**.</span></span>

<span data-ttu-id="cfd7a-149">Das Kontrollkästchen **MwSt. ausgeglichen.** ist für die Rechnung und die Rechnungspositionen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="cfd7a-149">The **VAT settled** check box is selected for the invoice and the invoice lines.</span></span>
