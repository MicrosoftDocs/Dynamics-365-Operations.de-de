---
title: Die Steuer wird nicht berechnet oder der Steuerbetrag ist Null
description: Dieses Thema enthält Informationen zur Fehlerbehebung, die helfen können, wenn der Steuerbetrag 0 (Null) ist oder die Steuer nicht berechnet wird.
author: shtao
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: c398579a0a408e7f5625a3e801a967955c4b1e5b
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020114"
---
# <a name="tax-isnt-calculated-or-the-tax-amount-is-zero"></a><span data-ttu-id="20a7d-103">Die Steuer wird nicht berechnet oder der Steuerbetrag ist Null</span><span class="sxs-lookup"><span data-stu-id="20a7d-103">Tax isn't calculated or the tax amount is zero</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="20a7d-104">Eine Transaktion kann einen Zeilenbetrag haben, der nicht 0 (Null) ist, aber entweder wird die Steuer nicht berechnet oder der berechnete Steuerbetrag ist 0.</span><span class="sxs-lookup"><span data-stu-id="20a7d-104">A transaction might have a line amount that isn't 0 (zero), but either tax isn't calculated or the calculated tax amount is 0.</span></span> <span data-ttu-id="20a7d-105">Um dieses Problem zu beheben, führen Sie die Schritte in den folgenden Abschnitten wie erforderlich aus.</span><span class="sxs-lookup"><span data-stu-id="20a7d-105">To troubleshoot this issue, follow the steps in the following sections as required.</span></span>

## <a name="verify-that-tax-codes-are-correctly-selected-by-the-transaction"></a><span data-ttu-id="20a7d-106">Überprüfen Sie, ob die Steuerkennzeichen in der Transaktion korrekt ausgewählt sind</span><span class="sxs-lookup"><span data-stu-id="20a7d-106">Verify that tax codes are correctly selected by the transaction</span></span>

<span data-ttu-id="20a7d-107">Wenn die Transaktion nicht die richtigen Steuerkennzeichen auswählt oder wenn sie keine Steuerkennzeichen auswählt, werden keine Steuern für sie berechnet.</span><span class="sxs-lookup"><span data-stu-id="20a7d-107">If the transaction doesn't select the correct tax codes, or if it doesn't select any tax codes, taxes won't be calculated on it.</span></span> <span data-ttu-id="20a7d-108">Führen Sie diese Schritte aus, um zu überprüfen, ob die Steuerkennzeichen von der Transaktion korrekt ausgewählt wurden.</span><span class="sxs-lookup"><span data-stu-id="20a7d-108">Follow these steps to verify that tax codes are correctly selected by the transaction.</span></span> 

1. <span data-ttu-id="20a7d-109">Stellen Sie in der Zeile der Transaktion auf dem Inforegister **Zeilendetails**, auf der Registerkarte **Einrichten**, im Abschnitt **Mehrwertsteuer** sicher, dass die richtigen Mehrwertsteuergruppen in den Feldern **Element Mehrwertsteuergruppe** und **Mehrwertsteuergruppe** ausgewählt sind.</span><span class="sxs-lookup"><span data-stu-id="20a7d-109">On the transaction line, on the **Line details** FastTab, on the **Setup** tab, in the **Sales tax** section, verify that the correct tax groups are selected in the **Item sales tax group** and **Sales tax group** fields.</span></span> <span data-ttu-id="20a7d-110">Wenn die richtigen Steuergruppen nicht ausgewählt sind, wählen Sie sie aus.</span><span class="sxs-lookup"><span data-stu-id="20a7d-110">If the correct tax groups aren't selected, select them.</span></span>

    <span data-ttu-id="20a7d-111">[![Felder „Element Mehrwertsteuergruppe und Mehrwertsteuergruppe“](./media/tax-not-calculated-tax-amount-zero-Picture1.png)](./media/tax-not-calculated-tax-amount-zero-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="20a7d-111">[![Item sales tax group and Sales tax group fields](./media/tax-not-calculated-tax-amount-zero-Picture1.png)](./media/tax-not-calculated-tax-amount-zero-Picture1.png)</span></span>

2. <span data-ttu-id="20a7d-112">Gehen Sie zu **Steuern** \> **Direkte Steuern** \> **Mehrwertsteuer** \> **Mehrwertsteuergruppen**.</span><span class="sxs-lookup"><span data-stu-id="20a7d-112">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax groups**.</span></span>
3. <span data-ttu-id="20a7d-113">Wählen Sie die entsprechende Mehrwertsteuergruppe und notieren Sie sich dann auf dem Inforegister **Einrichten** das Steuerkennzeichen im Feld **Umsatzsteuerkennzeichen**.</span><span class="sxs-lookup"><span data-stu-id="20a7d-113">Select the appropriate sales tax group, and then, on the **Setup** FastTab, make a note of the tax code in the **Sales tax code** field.</span></span>

    <span data-ttu-id="20a7d-114">[![Mehrwertsteuergruppen Seite](./media/tax-not-calculated-tax-amount-zero-Picture2.png)](./media/tax-not-calculated-tax-amount-zero-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="20a7d-114">[![Sales tax groups page](./media/tax-not-calculated-tax-amount-zero-Picture2.png)](./media/tax-not-calculated-tax-amount-zero-Picture2.png)</span></span>

4. <span data-ttu-id="20a7d-115">Gehen Sie zu **Steuern** \> **Indirekte Steuern** \> **Mehrwertsteuer** \> **Element Mehrwertsteuergruppen**.</span><span class="sxs-lookup"><span data-stu-id="20a7d-115">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Item sales tax groups**.</span></span>
5. <span data-ttu-id="20a7d-116">Wählen Sie das entsprechende Element Mehrwertsteuer-Gruppe und stellen Sie dann im Inforegister **Einrichten** sicher, dass das Steuerkennzeichen im Feld **Steuerkennzeichen** mit dem Steuerkennzeichen der Mehrwertsteuergruppe übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="20a7d-116">Select the appropriate item sales tax group, and then, on the **Setup** FastTab, verify that the tax code in the **Sales tax code** field matches the tax code of the sales tax group.</span></span>

    <span data-ttu-id="20a7d-117">[![Element Mehrwertsteuergruppen Seite](./media/tax-not-calculated-tax-amount-zero-Picture3.png)](./media/tax-not-calculated-tax-amount-zero-Picture3.png)</span><span class="sxs-lookup"><span data-stu-id="20a7d-117">[![Item sales tax groups page](./media/tax-not-calculated-tax-amount-zero-Picture3.png)](./media/tax-not-calculated-tax-amount-zero-Picture3.png)</span></span>

6. <span data-ttu-id="20a7d-118">Wenn die Steuerkennzeichen nicht übereinstimmen, aktualisieren Sie das Mehrwertsteuerkennzeichen für eine der Gruppen.</span><span class="sxs-lookup"><span data-stu-id="20a7d-118">If the tax codes don't match, update the sales tax code for one of the groups.</span></span>

## <a name="verify-that-the-selected-tax-codes-arent-exempt-and-that-they-have-the-correct-tax-rate-value"></a><span data-ttu-id="20a7d-119">Überprüfen Sie, dass die ausgewählten Steuerkennzeichen nicht befreit sind und dass sie den richtigen Wert für den Steuersatz haben</span><span class="sxs-lookup"><span data-stu-id="20a7d-119">Verify that the selected tax codes aren't exempt and that they have the correct tax rate value</span></span>

<span data-ttu-id="20a7d-120">Wenn die Steuerkennzeichen befreit sind oder der Steuersatz 0 (Null) ist, ist das Ergebnis der Steuerberechnung 0.</span><span class="sxs-lookup"><span data-stu-id="20a7d-120">If the tax codes are exempt, or if the tax rate is 0 (zero), the tax calculation result will be 0.</span></span> <span data-ttu-id="20a7d-121">Führen Sie diese Schritte aus, um festzustellen, ob die ausgewählten Steuerkennzeichen befreit sind und um zu überprüfen, ob der richtige Steuersatz auf sie angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="20a7d-121">Follow these steps to determine whether the selected tax codes are exempt and to verify that the correct tax rate is applied to them.</span></span>

1. <span data-ttu-id="20a7d-122">Gehen Sie zu **Steuern** \> **Direkte Steuern** \> **Mehrwertsteuer** \> **Mehrwertsteuergruppen**.</span><span class="sxs-lookup"><span data-stu-id="20a7d-122">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax groups**.</span></span>
2. <span data-ttu-id="20a7d-123">Wählen Sie die entsprechende Mehrwertsteuergruppe aus und stellen Sie dann im Inforegister **Einrichtung** sicher, dass das Kontrollkästchen **Befreit** deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="20a7d-123">Select the appropriate sales tax group, and then, on the **Setup** FastTab, verify that the **Exempt** check box is cleared.</span></span> <span data-ttu-id="20a7d-124">Wenn er ausgewählt ist, löschen Sie ihn.</span><span class="sxs-lookup"><span data-stu-id="20a7d-124">If it's selected, clear it.</span></span>

    <span data-ttu-id="20a7d-125">[![Kontrollkästchen Befreit auf der Seite Mehrwertsteuergruppen](./media/tax-not-calculated-tax-amount-zero-Picture4.png)](./media/tax-not-calculated-tax-amount-zero-Picture4.png)</span><span class="sxs-lookup"><span data-stu-id="20a7d-125">[![Exempt check box on the Sales tax groups page](./media/tax-not-calculated-tax-amount-zero-Picture4.png)](./media/tax-not-calculated-tax-amount-zero-Picture4.png)</span></span>

3. <span data-ttu-id="20a7d-126">Wechseln Sie zu **Steuern** \> **Direkte Steuern** \> **Umsatzsteuer** \> **Umsatzsteuercodes**.</span><span class="sxs-lookup"><span data-stu-id="20a7d-126">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax codes**.</span></span>
4. <span data-ttu-id="20a7d-127">Wählen Sie das entsprechende Mehrwertsteuerkennzeichen und überprüfen Sie, ob der Wert des Steuersatzes im Feld **Wert** nicht 0 (Null) ist.</span><span class="sxs-lookup"><span data-stu-id="20a7d-127">Select the appropriate sales tax code, and then verify that the tax rate value in the **Value** field isn't 0 (zero).</span></span> <span data-ttu-id="20a7d-128">Wenn es 0 ist, aktualisieren Sie das Feld, so dass es auf den richtigen Steuersatz festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="20a7d-128">If it's 0, update the field so that it's set to the correct tax rate.</span></span>

    <span data-ttu-id="20a7d-129">[![Feld „Wert“ auf der Seite „Werte für Mehrwertsteuer-Code“](./media/tax-not-calculated-tax-amount-zero-Picture5.png)](./media/tax-not-calculated-tax-amount-zero-Picture5.png)</span><span class="sxs-lookup"><span data-stu-id="20a7d-129">[![Value field on the Sales tax code values page](./media/tax-not-calculated-tax-amount-zero-Picture5.png)](./media/tax-not-calculated-tax-amount-zero-Picture5.png)</span></span>

## <a name="determine-whether-zero-is-the-correct-tax-amount"></a><span data-ttu-id="20a7d-130">Bestimmen Sie, ob Null der korrekte Steuerbetrag ist</span><span class="sxs-lookup"><span data-stu-id="20a7d-130">Determine whether zero is the correct tax amount</span></span>

<span data-ttu-id="20a7d-131">In einigen Szenarien ist ein Steuerwert von 0 (Null) korrekt.</span><span class="sxs-lookup"><span data-stu-id="20a7d-131">In some scenarios, a tax amount of 0 (zero) is correct.</span></span> <span data-ttu-id="20a7d-132">Führen Sie diese Schritte aus, um festzustellen, ob 0 der richtige Steuerbetrag für Ihre Transaktion ist.</span><span class="sxs-lookup"><span data-stu-id="20a7d-132">Follow these steps to determine whether 0 is the correct tax amount for your transaction.</span></span>

1. <span data-ttu-id="20a7d-133">Gehen Sie zu **Hauptbuch** \> **Hauptbuch einrichten** \> **Hauptbuch-Parameter**.</span><span class="sxs-lookup"><span data-stu-id="20a7d-133">Go to **General ledger** \> **Ledger setup** \> **General ledger parameters**.</span></span>
2. <span data-ttu-id="20a7d-134">Stellen Sie auf der Registerkarte **Mehrwertsteuer** im Feld **Berechnungsmethode** sicher, dass **Gesamt** ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="20a7d-134">On the **Sales tax** tab, in the **Calculation method** field, verify that **Total** is selected.</span></span>

    <span data-ttu-id="20a7d-135">[![Feld „Berechnungsmethode“ auf der Seite „Parameter Hauptbuch“](./media/tax-not-calculated-tax-amount-zero-Picture6.png)](./media/tax-not-calculated-tax-amount-zero-Picture6.png)</span><span class="sxs-lookup"><span data-stu-id="20a7d-135">[![Calculation method field on the General ledger parameters page](./media/tax-not-calculated-tax-amount-zero-Picture6.png)](./media/tax-not-calculated-tax-amount-zero-Picture6.png)</span></span>

3. <span data-ttu-id="20a7d-136">Wechseln Sie zu **Steuern** \> **Direkte Steuern** \> **Umsatzsteuer** \> **Umsatzsteuercodes**.</span><span class="sxs-lookup"><span data-stu-id="20a7d-136">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax codes**.</span></span>
4. <span data-ttu-id="20a7d-137">Wählen Sie das entsprechende Umsatzsteuerkennzeichen, wählen Sie **Berechnung** \> **Margenbasis**, und überprüfen Sie, ob die Margenbasis auf **Nettobetrag des Rechnungssaldos** oder **Rechnungssumme inkl. sonstiger Umsatzsteuerbeträge** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="20a7d-137">Select the appropriate sales tax code, select **Calculation** \> **Marginal base**, and verify that the marginal base is set to **Net amount of invoice balance** or **Invoice total incl. other sales tax amounts**.</span></span> <span data-ttu-id="20a7d-138">Für weitere Informationen, siehe [Rechnungssumme inkl. sonstiger Mehrwertsteuerbeträge](marginal-base-field.md#invoice-total-incl-other-sales-tax-amounts).</span><span class="sxs-lookup"><span data-stu-id="20a7d-138">For more information, see the [Invoice total incl. other sales tax amounts](marginal-base-field.md#invoice-total-incl-other-sales-tax-amounts).</span></span>
5. <span data-ttu-id="20a7d-139">Wenn in den Schritten 2 und 4 die richtigen Werte festgelegt wurden, stellen Sie fest, ob der Gesamtbetrag der Transaktion 0 (Null) ist.</span><span class="sxs-lookup"><span data-stu-id="20a7d-139">If the correct values are set in steps 2 and 4, determine whether the total amount of the transaction is 0 (zero).</span></span> <span data-ttu-id="20a7d-140">Wenn der Gesamtbetrag 0 ist, ist ein Steuerbetrag von 0 das erwartete Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="20a7d-140">If the total amount is 0, a tax amount of 0 is the expected result.</span></span> <span data-ttu-id="20a7d-141">Da die Steuerberechnung auf dem Gesamtbetrag des Rechnungssaldos basiert und dieser Betrag nicht zeilenweise ist, wird jeder Zeile nach der Steuerberechnung der Steuerbetrag von 0 zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="20a7d-141">Because the tax calculation is based on the total amount of the invoice balance, and that amount isn't line by line, the tax amount of 0 will be allocated to each line after the tax calculation.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="20a7d-142">Ermitteln Sie, ob eine Anpassung vorliegt</span><span class="sxs-lookup"><span data-stu-id="20a7d-142">Determine whether customization exists</span></span>

<span data-ttu-id="20a7d-143">Wenn Sie die Schritte in den vorherigen Abschnitten ausgeführt haben, aber kein Problem gefunden haben, stellen Sie fest, ob eine Anpassung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="20a7d-143">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="20a7d-144">Wenn keine Anpassung vorhanden ist, erstellen Sie eine Microsoft Service-Anfrage für weiteren Support.</span><span class="sxs-lookup"><span data-stu-id="20a7d-144">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
