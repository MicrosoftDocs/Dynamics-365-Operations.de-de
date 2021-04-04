---
title: Mahnschreiben verarbeiten – Beispiel
description: In diesem Thema wird ein Beispiel vorgestellt, das den Prozess des Erstellens, Druckens und Versendens von Mahnschreiben zeigt.
author: JodiChristiansen
manager: AnnBe
ms.date: 02/03/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: df4252513f9e3a02632561b4e465c98edc888ea7
ms.sourcegitcommit: 4ecc1bf82fbb04882d7ef5e1994ef3c07ef953dc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/08/2021
ms.locfileid: "5558310"
---
# <a name="process-collection-letters-example"></a><span data-ttu-id="37b42-103">Mahnschreiben verarbeiten – Beispiel</span><span class="sxs-lookup"><span data-stu-id="37b42-103">Process collection letters example</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="37b42-104">In diesem Thema wird ein Beispiel vorgestellt, das den Prozess des Erstellens, Druckens und Versendens von Mahnschreiben zeigt.</span><span class="sxs-lookup"><span data-stu-id="37b42-104">This topic goes through an example that shows the process of creating, printing, and posting collection letters.</span></span> <span data-ttu-id="37b42-105">Das Beispiel basiert auf der Option **Zahlungen und Habenbuchungen für Berechnung des Mahnschreibencodes ignorieren** in Kredit und Inkasso.</span><span class="sxs-lookup"><span data-stu-id="37b42-105">The example is based on the **Ignore payments and credit memos when calculating collection letter code** option in Credit and collections.</span></span> <span data-ttu-id="37b42-106">Es werden Daten des USMF-Demounternehmens und eines neuen Kunden, US-045, verwendet.</span><span class="sxs-lookup"><span data-stu-id="37b42-106">It uses data in the USMF demo company and a new customer, US-045.</span></span>

<span data-ttu-id="37b42-107">Rufen Sie zu Beginn **Debitorenkonten \> Debitoren \> Alle Debitoren** auf. Wählen Sie die Option **Neu** aus, und geben Sie dann die erforderlichen Informationen ein, um den Debitoren US-045 zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="37b42-107">To begin, go to **Accounts receivable \> Customers \> All customers**, select **New**, and then enter the required information to create customer US-045.</span></span>

<span data-ttu-id="37b42-108">Wenn Sie fertig sind, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="37b42-108">When you've finished, follow these steps.</span></span>

1. <span data-ttu-id="37b42-109">Rufen Sie **Kredit und Inkasso \> Mahnschreiben \> Mahnschreibensequenz einrichten** auf, und richten Sie die Mahnschfreibensequenz wie in der folgenden Tabelle gezeigt ein, die dem Debitorenbuchungsprofil zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="37b42-109">Go to **Credit and collections \> Collection letter \> Setup collection letter sequence**, and set up the collection letter sequence as shown in the following table that is assigned to the customer posting profile.</span></span>

|     <span data-ttu-id="37b42-110">Mahnschreibencode</span><span class="sxs-lookup"><span data-stu-id="37b42-110">Collection   letter code</span></span>      |     <span data-ttu-id="37b42-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="37b42-111">Description</span></span>                           |     <span data-ttu-id="37b42-112">Währung</span><span class="sxs-lookup"><span data-stu-id="37b42-112">Currency</span></span>      |     <span data-ttu-id="37b42-113">Hauptkonto</span><span class="sxs-lookup"><span data-stu-id="37b42-113">Main   account</span></span>        |     <span data-ttu-id="37b42-114">Gebühren in Währung</span><span class="sxs-lookup"><span data-stu-id="37b42-114">Fee   in currency</span></span>     |     <span data-ttu-id="37b42-115">Minimum über</span><span class="sxs-lookup"><span data-stu-id="37b42-115">Minimum   over</span></span>        |     <span data-ttu-id="37b42-116">Zu sperrende Tage</span><span class="sxs-lookup"><span data-stu-id="37b42-116">Days   Block</span></span>      |
|---------------------------------  |---------------------------------------    |-----------------  |-----------------------    |-------------------------- |-----------------------    |---------------------  |
|     <span data-ttu-id="37b42-117">Mahnschreiben 1</span><span class="sxs-lookup"><span data-stu-id="37b42-117">Collection   letter 1</span></span>         |     <span data-ttu-id="37b42-118">Zweite Benachrichtigung mit Gebühr</span><span class="sxs-lookup"><span data-stu-id="37b42-118">Second   notification with fee</span></span>        |     <span data-ttu-id="37b42-119">USD</span><span class="sxs-lookup"><span data-stu-id="37b42-119">USD</span></span>           |                           |     <span data-ttu-id="37b42-120">0,00</span><span class="sxs-lookup"><span data-stu-id="37b42-120">0.00</span></span>                  |     <span data-ttu-id="37b42-121">0,00</span><span class="sxs-lookup"><span data-stu-id="37b42-121">0.00</span></span>                  |     <span data-ttu-id="37b42-122">2</span><span class="sxs-lookup"><span data-stu-id="37b42-122">2</span></span>                 |
|     <span data-ttu-id="37b42-123">Mahnschreiben 2</span><span class="sxs-lookup"><span data-stu-id="37b42-123">Collection   letter 2</span></span>         |     <span data-ttu-id="37b42-124">Zweite Benachrichtigung mit Gebühr</span><span class="sxs-lookup"><span data-stu-id="37b42-124">Second   notification with fee</span></span>        |     <span data-ttu-id="37b42-125">USC</span><span class="sxs-lookup"><span data-stu-id="37b42-125">USC</span></span>           |     <span data-ttu-id="37b42-126">403150</span><span class="sxs-lookup"><span data-stu-id="37b42-126">403150</span></span>                |     <span data-ttu-id="37b42-127">20.00</span><span class="sxs-lookup"><span data-stu-id="37b42-127">20.00</span></span>                 |     <span data-ttu-id="37b42-128">10.00</span><span class="sxs-lookup"><span data-stu-id="37b42-128">10.00</span></span>                 |     <span data-ttu-id="37b42-129">3</span><span class="sxs-lookup"><span data-stu-id="37b42-129">3</span></span>                 |
|     <span data-ttu-id="37b42-130">Inkasso</span><span class="sxs-lookup"><span data-stu-id="37b42-130">Collection</span></span>                    |     <span data-ttu-id="37b42-131">Letzte Benachrichtigung mit Gebühr</span><span class="sxs-lookup"><span data-stu-id="37b42-131">Final   notification with fee</span></span>         |     <span data-ttu-id="37b42-132">USD</span><span class="sxs-lookup"><span data-stu-id="37b42-132">USD</span></span>           |     <span data-ttu-id="37b42-133">403150</span><span class="sxs-lookup"><span data-stu-id="37b42-133">403150</span></span>                |     <span data-ttu-id="37b42-134">50.00</span><span class="sxs-lookup"><span data-stu-id="37b42-134">50.00</span></span>                 |     <span data-ttu-id="37b42-135">100.00</span><span class="sxs-lookup"><span data-stu-id="37b42-135">100.00</span></span>                |     <span data-ttu-id="37b42-136">15</span><span class="sxs-lookup"><span data-stu-id="37b42-136">15</span></span>                |

<span data-ttu-id="37b42-137">Die folgende Abbildung zeigt die Informationen in der Tabelle so, wie sie auf der Seite **Mahnschreiben** dargestellt würden.</span><span class="sxs-lookup"><span data-stu-id="37b42-137">The following illustration shows the information that's in the table as it would appear on the **Collection letters** page.</span></span> 

<span data-ttu-id="37b42-138">[![Einrichten von Mahnschreibensequenzen](./media/Ignore-payments-creditmemos-1.PNG)](./media/Ignore-payments-creditmemos-1.PNG)</span><span class="sxs-lookup"><span data-stu-id="37b42-138">[![Setting up a collection letter sequence](./media/Ignore-payments-creditmemos-1.PNG)](./media/Ignore-payments-creditmemos-1.PNG)</span></span>

 <span data-ttu-id="37b42-139">Sie müssen jetzt die beiden Parameter einstellen, die für dieses Beispiel erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="37b42-139">You must now set the two parameters that are required for this example.</span></span>

2. <span data-ttu-id="37b42-140">Rufen Sie **Kredit und Inkasso \> Einrichtung \> Debitorenparameter** auf, und befolgen Sie diese Schritte:</span><span class="sxs-lookup"><span data-stu-id="37b42-140">Go to **Credit and collections \> Setup \> Accounts receivable parameters**, and follow these steps:</span></span>

    1. <span data-ttu-id="37b42-141">Stellen Sie auf der Registerkarte **Inkasso** die Option **Zahlungen und Habenbuchungen für Berechnung des Mahnschreibencodes ignorieren** auf **Ja** ein.</span><span class="sxs-lookup"><span data-stu-id="37b42-141">On the **Collections** tab, set the **Ignore payments and credit memos when calculating collection letter code** option to **Yes**.</span></span>
    2. <span data-ttu-id="37b42-142">Vergewissern Sie sich, dass das Feld **Erstellen eines Mahnschreibens pro** auf **Debitor** eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="37b42-142">Make sure that the **Create collection letter per** field is set to **Customer**.</span></span>

    <span data-ttu-id="37b42-143">[![Einstellen von Debitorenparametern für Kredite und Inkassos](./media/Ignore-payments-creditmemos-2.PNG)](./media/Ignore-payments-creditmemos-2.PNG)</span><span class="sxs-lookup"><span data-stu-id="37b42-143">[![Setting Accounts receivable parameters for Credit collections](./media/Ignore-payments-creditmemos-2.PNG)](./media/Ignore-payments-creditmemos-2.PNG)</span></span>

3. <span data-ttu-id="37b42-144">Rufen Sie **Debitoren \> Rechnungen \> Alle Freitextrechnungen** auf, wählen Sie **Neu** aus, und befolgen Sie dann diese Schritte:</span><span class="sxs-lookup"><span data-stu-id="37b42-144">Go to **Accounts receivable \> Invoices \> All free text invoices**, select **New**, and then follow these steps:</span></span>

    1. <span data-ttu-id="37b42-145">Wählen Sie im Feld **Debitorenkonto** die Option **US-045** aus.</span><span class="sxs-lookup"><span data-stu-id="37b42-145">In the **Customer account** field select **US-045**.</span></span>
    2. <span data-ttu-id="37b42-146">Geben Sie im Feld **Rechnungsdatum** **1/15/2021** ein.</span><span class="sxs-lookup"><span data-stu-id="37b42-146">In the **Invoice date** field, enter **1/15/2021**.</span></span>
    3. <span data-ttu-id="37b42-147">Geben Sie im Feld **Fälligkeitsdatum** den Wert **1/16/2021** ein.</span><span class="sxs-lookup"><span data-stu-id="37b42-147">In the **Due date** field, enter **1/16/2021**.</span></span>
    4. <span data-ttu-id="37b42-148">Geben Sie auf der Registerkarte **Rechnungspositionen** im Feld **Hauptkonto** den Wert **401100** ein.</span><span class="sxs-lookup"><span data-stu-id="37b42-148">On the **Invoice lines** FastTab, in the **Main account** field, enter **401100**.</span></span>
    5. <span data-ttu-id="37b42-149">Geben Sie im Feld **Einzelpreis** die Zahl **500.00** ein.</span><span class="sxs-lookup"><span data-stu-id="37b42-149">In the **Unit price** field, enter **500.00**.</span></span>
    6. <span data-ttu-id="37b42-150">Wählen Sie **Buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="37b42-150">Select **Post**.</span></span>

    <span data-ttu-id="37b42-151">Sie müssen jetzt zwei Gutschriften für den Debitoren eingeben.</span><span class="sxs-lookup"><span data-stu-id="37b42-151">You must now enter two credit notes for the customer.</span></span>

4. <span data-ttu-id="37b42-152">Wählen Sie **Hinzufügen** aus, und befolgen Sie die folgenden Schritte:</span><span class="sxs-lookup"><span data-stu-id="37b42-152">Select **New**, and then follow these steps:</span></span>

    1. <span data-ttu-id="37b42-153">Wählen Sie im Feld **Kundenkonto** die Option **US-045** aus.</span><span class="sxs-lookup"><span data-stu-id="37b42-153">In the **Customer account** field, select **US-045**.</span></span>
    2. <span data-ttu-id="37b42-154">Geben Sie im Feld **Rechnungsdatum** **1/15/2021** ein.</span><span class="sxs-lookup"><span data-stu-id="37b42-154">In the **Invoice date** field, enter **1/15/2021**.</span></span>
    3. <span data-ttu-id="37b42-155">Geben Sie im Feld **Fälligkeitsdatum** den Wert **1/16/2021** ein.</span><span class="sxs-lookup"><span data-stu-id="37b42-155">In the **Due date** field, enter **1/16/2021**.</span></span>
    4. <span data-ttu-id="37b42-156">Geben Sie auf der Registerkarte **Rechnungspositionen** im Feld **Hauptkonto** den Wert **401100** ein.</span><span class="sxs-lookup"><span data-stu-id="37b42-156">On the **Invoice lines** FastTab, in the **Main account** field, enter **401100**.</span></span>
    5. <span data-ttu-id="37b42-157">Geben Sie im Feld **Preis je Einheit** die Zahl **-100,00** ein.</span><span class="sxs-lookup"><span data-stu-id="37b42-157">In the **Unit price** field, enter **-100.00**.</span></span>
    6. <span data-ttu-id="37b42-158">Wählen Sie **Buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="37b42-158">Select **Post**.</span></span>

5. <span data-ttu-id="37b42-159">Wiederholen Sie Schritt 4, aber geben Sie **-200,00** im Feld **Preis je Einheit** ein.</span><span class="sxs-lookup"><span data-stu-id="37b42-159">Repeat step 4, but enter **-200.00** in the **Unit price** field.</span></span>
6. <span data-ttu-id="37b42-160">Rufen Sie **Debitorenkonten \> Debitoren \> Alle Debitoren** auf, und wählen Sie Debitor **US-045** aus.</span><span class="sxs-lookup"><span data-stu-id="37b42-160">Go to **Accounts receivable \> Customers \> All customers**, and select customer **US-045**.</span></span> <span data-ttu-id="37b42-161">Wählen Sie dann im Aktionsbereich die Option **Transaktionen \> Transaktionen** aus, um die Debitortransaktionen zu überprüfen, die Sie zuvor gebucht haben.</span><span class="sxs-lookup"><span data-stu-id="37b42-161">Then, on the Action Pane, select **Transactions \> Transactions** to review the customer transactions that you posted earlier.</span></span>

    <span data-ttu-id="37b42-162">[![Überprüfen der gebuchten Debitortransaktionen](./media/Ignore-payments-creditmemos-3.PNG)](./media/Ignore-payments-creditmemos-3.PNG)</span><span class="sxs-lookup"><span data-stu-id="37b42-162">[![Reviewing the posted customer transactions](./media/Ignore-payments-creditmemos-3.PNG)](./media/Ignore-payments-creditmemos-3.PNG)</span></span>

    <span data-ttu-id="37b42-163">Nun müssen Sie Mahnschreiben für Debitor US-045 erstellen.</span><span class="sxs-lookup"><span data-stu-id="37b42-163">You must now create collection letters for customer US-045.</span></span>

7. <span data-ttu-id="37b42-164">Rufen Sie **Kredit und Inkasso \> Mahnschreiben \> Mahnschreiben erstellen** auf, und befolgen Sie diese Schritte:</span><span class="sxs-lookup"><span data-stu-id="37b42-164">Go to **Credit and collections \> Collection letter \> Create collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="37b42-165">Stellen Sie die Optionen **Rechnung** und **Gutschrift** auf **Ja** ein.</span><span class="sxs-lookup"><span data-stu-id="37b42-165">Set the **Invoice** and **Credit note** options to **Yes**.</span></span>

        <span data-ttu-id="37b42-166">Standardmäßig sollte das Feld **Mahnschreiben** auf **Mahnung pro Debitor** eingestellt sein.</span><span class="sxs-lookup"><span data-stu-id="37b42-166">By default, the **Collection letter** field should be set to **Collection per customer**.</span></span>

    2. <span data-ttu-id="37b42-167">Geben Sie im Feld **Datum des Mahnschreibens** den Wert **1/19/2021** ein.</span><span class="sxs-lookup"><span data-stu-id="37b42-167">In the **Collection letter date** field, enter **1/19/2021**.</span></span>
    3. <span data-ttu-id="37b42-168">Wählen Sie auf der Registerkarte **Einzuschließende Datensätze** die Option **Filter** aus, und fügen Sie dann im Feld **Debitorenkonto** den Debitor **US-045** hinzu.</span><span class="sxs-lookup"><span data-stu-id="37b42-168">On the **Records to include** FastTab, select **Filter**, and then, in the **Customer account** field, add customer **US-045**.</span></span>
    4. <span data-ttu-id="37b42-169">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="37b42-169">Select **OK**.</span></span>
    5. <span data-ttu-id="37b42-170">Wählen Sie **OK** aus, um Mahnschreiben zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="37b42-170">Select **OK** to create collection letters.</span></span>

8. <span data-ttu-id="37b42-171">Rufen Sie **Kredit und Inkasso \> Mahnschreiben \> Mahnschreiben prüfen und verarbeiten** auf, und befolgen Sie diese Schritte:</span><span class="sxs-lookup"><span data-stu-id="37b42-171">Go to **Credit and collections \> Collection letter \> Review and process collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="37b42-172">Beachten Sie, dass der Mahnschreibencode sowohl in der Kopfzeile als auch in den Transaktionspositionen **Mahnschreiben 1** lautet, da es sich bei diesem Mahnschreiben um das erste Mahnschreiben in der Sequenz handelt.</span><span class="sxs-lookup"><span data-stu-id="37b42-172">Notice that the collection letter code on both the header and the transaction lines is **Collection letter 1**, because this collection letter is the first collection letter in the sequence.</span></span> <span data-ttu-id="37b42-173">(Um sich die Transaktionspositionen anzeigen zu lassen, müssen Sie möglicherweise das Inforegister **Transaktionen** auswählen.)</span><span class="sxs-lookup"><span data-stu-id="37b42-173">(To view the transaction lines, you might have to select the **Transactions** FastTab.)</span></span>

   <span data-ttu-id="37b42-174">[![Sicherstellen, dass in der Kopfzeile und den Positionen derselbe Mahnschreibencode angezeigt wird](./media/Ignore-payments-creditmemos-4.PNG)](./media/Ignore-payments-creditmemos-4.PNG)</span><span class="sxs-lookup"><span data-stu-id="37b42-174">[![Verifying that the same collection letter code appears on the header and the lines](./media/Ignore-payments-creditmemos-4.PNG)](./media/Ignore-payments-creditmemos-4.PNG)</span></span>

    2. <span data-ttu-id="37b42-175">Wählen Sie im Aktionsbereich **Buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="37b42-175">On the Action Pane, select **Post**.</span></span>
    3. <span data-ttu-id="37b42-176">Geben Sie im Feld **Buchungsdatum** den Wert **1/19/2021** ein.</span><span class="sxs-lookup"><span data-stu-id="37b42-176">In the **Posting date** field, enter **1/19/2021**.</span></span>

    <span data-ttu-id="37b42-177">Nun müssen Sie erneut Mahnschreiben für Debitor US-045 erstellen.</span><span class="sxs-lookup"><span data-stu-id="37b42-177">You must now create collection letters again for customer US-045.</span></span>

9. <span data-ttu-id="37b42-178">Rufen Sie **Kredit und Inkasso \> Mahnschreiben \> Mahnschreiben erstellen** auf, und befolgen Sie diese Schritte:</span><span class="sxs-lookup"><span data-stu-id="37b42-178">Go to **Credit and collections \> Collection letter \> Create collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="37b42-179">Stellen Sie die Optionen **Rechnung** und **Gutschrift** auf **Ja** ein.</span><span class="sxs-lookup"><span data-stu-id="37b42-179">Set the **Invoice** and **Credit note** options to **Yes**.</span></span>

        <span data-ttu-id="37b42-180">Standardmäßig sollte das Feld **Mahnschreiben** auf **Mahnung pro Debitor** eingestellt sein.</span><span class="sxs-lookup"><span data-stu-id="37b42-180">By default, the **Collection letter** field should be set to **Collection per customer**.</span></span>

    2. <span data-ttu-id="37b42-181">Geben Sie im Feld **Datum des Mahnschreibens** den Wert **1/23/2021** ein.</span><span class="sxs-lookup"><span data-stu-id="37b42-181">In the **Collection letter date** field, enter **1/23/2021**.</span></span>
    3. <span data-ttu-id="37b42-182">Wählen Sie auf der Registerkarte **Einzuschließende Datensätze** die Option **Filter** aus, und fügen Sie dann im Feld **Debitorenkonto** den Debitor **US-045** hinzu.</span><span class="sxs-lookup"><span data-stu-id="37b42-182">On the **Records to include** FastTab, select **Filter**, and then, in the **Customer account** field, add customer **US-045**.</span></span>
    4. <span data-ttu-id="37b42-183">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="37b42-183">Select **OK**.</span></span>
    5. <span data-ttu-id="37b42-184">Wählen Sie **OK** aus, um Mahnschreiben zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="37b42-184">Select **OK** to create collection letters.</span></span>

10. <span data-ttu-id="37b42-185">Rufen Sie **Kredit und Inkasso \> Mahnschreiben \> Mahnschreiben prüfen und verarbeiten** auf, und befolgen Sie diese Schritte:</span><span class="sxs-lookup"><span data-stu-id="37b42-185">Go to **Credit and collections \> Collection letter \> Review and process collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="37b42-186">Beachten Sie, dass der Mahnschreibencode in der Kopfzeile **Mahnschreiben 1** lautet.</span><span class="sxs-lookup"><span data-stu-id="37b42-186">Notice that the collection letter code on the header is **Collection letter 1**.</span></span> <span data-ttu-id="37b42-187">Der Code in den Transaktionspositionen lautet jedoch **Mahnschreiben 2**.</span><span class="sxs-lookup"><span data-stu-id="37b42-187">However, the code on the transaction lines is **Collection letter 2**.</span></span>

   <span data-ttu-id="37b42-188">[![Sicherstellen, dass in der Kopfzeile und den Positionen verschiedene Mahnschreibencodes angezeigt werden](./media/Ignore-payments-creditmemos-5.PNG)](./media/Ignore-payments-creditmemos-5.PNG)</span><span class="sxs-lookup"><span data-stu-id="37b42-188">[![Verifies that different collection letter codes appear on the header and the lines](./media/Ignore-payments-creditmemos-5.PNG)](./media/Ignore-payments-creditmemos-5.PNG)</span></span>

  <span data-ttu-id="37b42-189">Die Codes sind unterschiedlich, da die Option **Zahlungen und Habenbuchungen für Berechnung des Mahnschreibencodes ignorieren** auf **Ja** eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="37b42-189">The codes differ because the **Ignore payments and credit memos when calculating collection letter code** option is to **Yes**.</span></span>

  2. <span data-ttu-id="37b42-190">Buchen Sie nicht dieses Mahnschreiben.</span><span class="sxs-lookup"><span data-stu-id="37b42-190">Don't post this collection letter.</span></span>

11. <span data-ttu-id="37b42-191">Rufen Sie **Kredit und Inkasso \> Einrichtung \> Debitorenparameter** auf, und stellen Sie dann auf der Registerkarte **Inkasso** die Option **Zahlungen und Habenbuchungen für Berechnung des Mahnschreibencodes ignorieren** auf **Nein** ein.</span><span class="sxs-lookup"><span data-stu-id="37b42-191">Go to **Credit and collections \> Setup \> Accounts receivable parameters**, and then, on the **Collections** tab, set the **Ignore payments and credit memos when calculating collection letter code** option to **No**.</span></span>

    <span data-ttu-id="37b42-192">[![Einstellen der Option „Zahlungen und Habenbuchungen für Berechnung des Mahnschreibencodes ignorieren“ auf „Nein“](./media/Ignore-payments-creditmemos-6.PNG)](./media/Ignore-payments-creditmemos-6.PNG)</span><span class="sxs-lookup"><span data-stu-id="37b42-192">[![Setting the Ignore payments and credit memos when calculating collection letter code option to No](./media/Ignore-payments-creditmemos-6.PNG)](./media/Ignore-payments-creditmemos-6.PNG)</span></span>

    <span data-ttu-id="37b42-193">Nun müssen Sie erneut Mahnschreiben für Debitor US-045 erstellen.</span><span class="sxs-lookup"><span data-stu-id="37b42-193">You must now create collection letters again for customer US-045.</span></span>

12. <span data-ttu-id="37b42-194">Rufen Sie **Kredit und Inkasso \> Mahnschreiben \> Mahnschreiben erstellen** auf, und befolgen Sie diese Schritte:</span><span class="sxs-lookup"><span data-stu-id="37b42-194">Go to **Credit and collections \> Collection letter \> Create collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="37b42-195">Stellen Sie die Optionen **Rechnung** und **Gutschrift** auf **Ja** ein.</span><span class="sxs-lookup"><span data-stu-id="37b42-195">Set the **Invoice** and **Credit note** options to **Yes**.</span></span>

        <span data-ttu-id="37b42-196">Standardmäßig sollte das Feld **Mahnschreiben** auf **Mahnung pro Debitor** eingestellt sein.</span><span class="sxs-lookup"><span data-stu-id="37b42-196">By default, the **Collection letter** field should be set to **Collection per customer**.</span></span>

    2. <span data-ttu-id="37b42-197">Geben Sie im Feld **Datum des Mahnschreibens** den Wert **1/23/2021** ein.</span><span class="sxs-lookup"><span data-stu-id="37b42-197">In the **Collection letter date** field, enter **1/23/2021**.</span></span>
    3. <span data-ttu-id="37b42-198">Wählen Sie auf der Registerkarte **Einzuschließende Datensätze** die Option **Filter** aus, und fügen Sie dann im Feld **Debitorenkonto** den Debitor **US-045** hinzu.</span><span class="sxs-lookup"><span data-stu-id="37b42-198">On the **Records to include** FastTab, select **Filter**, and then, in the **Customer account** field, add customer **US-045**.</span></span>
    4. <span data-ttu-id="37b42-199">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="37b42-199">Select **OK**.</span></span>
    5. <span data-ttu-id="37b42-200">Wählen Sie **OK** aus, um Mahnschreiben zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="37b42-200">Select **OK** to create collection letters.</span></span>

13. <span data-ttu-id="37b42-201">Rufen Sie **Kredit und Inkasso \> Mahnschreiben \> Mahnschreiben prüfen und verarbeiten** auf, und beachten Sie, dass der Mahnschreibencode sowohl in der Kopfzeile als auch in den Transaktionspositionen **Mahnschreiben 2** lautet.</span><span class="sxs-lookup"><span data-stu-id="37b42-201">Go to **Credit and collections \> Collection letter \> Review and process collection letters**, and notice that the collection letter code on both the header and the transaction lines is **Collection letter 2**.</span></span>

    <span data-ttu-id="37b42-202">[![Erneutes Anzeigen, dass in der Kopfzeile und den Positionen derselbe Mahnschreibencode angegeben ist](./media/Ignore-payments-creditmemos-7.PNG)](./media/Ignore-payments-creditmemos-7.PNG)</span><span class="sxs-lookup"><span data-stu-id="37b42-202">[![Showing again that the same collection letter code appears on the header and the lines](./media/Ignore-payments-creditmemos-7.PNG)](./media/Ignore-payments-creditmemos-7.PNG)</span></span>

    <span data-ttu-id="37b42-203">Derselbe Code erscheint an beiden Stellen, da die Option **Zahlungen und Habenbuchungen für Berechnung des Mahnschreibencodes ignorieren** jetzt auf **Nein** eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="37b42-203">The same code appears in both places because the **Ignore payments and credit memos when calculating collection letter code** option is now set to **No**.</span></span>
