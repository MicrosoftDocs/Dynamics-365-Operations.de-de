--- 
title: Mahnschreiben verarbeiten
description: Dieses Verfahren zeigt , wie Mahnschreiben erstellt, gedruckt und gebucht werden.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 12/04/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.translationtype: HT
ms.sourcegitcommit: 18eaadf417ce6d0aacf0b13b3e4f857e06031e66
ms.openlocfilehash: 8a3f74d2891c050294e089eae14ba2386449d7c9
ms.contentlocale: de-de
ms.lasthandoff: 01/22/2019

---
# <a name="process-collection-letters"></a><span data-ttu-id="d9ed6-103">Mahnschreiben verarbeiten</span><span class="sxs-lookup"><span data-stu-id="d9ed6-103">Process collection letters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d9ed6-104">Dieses Verfahren zeigt , wie Mahnschreiben erstellt, gedruckt und gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="d9ed6-104">This procedure shows how to create, print, and post collection letters.</span></span> <span data-ttu-id="d9ed6-105">Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="d9ed6-105">This task uses the USMF demo company.</span></span>

## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a><span data-ttu-id="d9ed6-106">Richten Sie eine Mahnschreibensequenz zum Buchungsprofil ein.</span><span class="sxs-lookup"><span data-stu-id="d9ed6-106">Set up a collection letter sequence on the posting profile</span></span>
1. <span data-ttu-id="d9ed6-107">**Wechseln Sie zu "Kredit und Inkasso > Einstellungen > Debitorenbuchungsprofile**.</span><span class="sxs-lookup"><span data-stu-id="d9ed6-107">Go to **Credit and collections > Setup > Customer posting profiles**.</span></span>
2. <span data-ttu-id="d9ed6-108">Klicken Sie auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="d9ed6-108">Click **Edit**.</span></span>
3. <span data-ttu-id="d9ed6-109">Wählen Sie eine Mahnschreibensequenz aus der Dropdownliste aus.</span><span class="sxs-lookup"><span data-stu-id="d9ed6-109">Select a collection letter sequence from the drop-down list.</span></span> <span data-ttu-id="d9ed6-110">Wenn Sie kein Mahnschreiben für Buchungen dieses Buchungsprofils erstellen wollen, lassen Sie das Feld leer.</span><span class="sxs-lookup"><span data-stu-id="d9ed6-110">If you do not want to generate collection letters for transactions using this posting profile, leave the field blank.</span></span>  
4. <span data-ttu-id="d9ed6-111">Das Erweitern der Tabelleneinschränkungsregisterkarte ermöglicht Ihnen das Verfahren, mit dem Mahnschreiben verarbeitet werden, zu ändern.</span><span class="sxs-lookup"><span data-stu-id="d9ed6-111">Expand the table restriction tab to change the way that collection letters are processed.</span></span> <span data-ttu-id="d9ed6-112">Wenn dieses Feld auf **Ja** festgelegt ist, werden Mahnschreiben für dieses Buchungsprofil erstellt.</span><span class="sxs-lookup"><span data-stu-id="d9ed6-112">If this field is set to **Yes**, then collection letters will be created for this posting profile.</span></span>  

## <a name="create-collection-letters"></a><span data-ttu-id="d9ed6-113">Mahnschreiben erstellen</span><span class="sxs-lookup"><span data-stu-id="d9ed6-113">Create collection letters</span></span>
1. <span data-ttu-id="d9ed6-114">Wechseln Sie zu **Kredit und Inkasso > Mahnschreiben > Erstellen von Mahnschreiben**.</span><span class="sxs-lookup"><span data-stu-id="d9ed6-114">Go to **Credit and collections > Collection letter > Create collection letters**.</span></span>
2. <span data-ttu-id="d9ed6-115">Sie müssen die Buchungsarten auswählen, die Sie anmahnen wollen.</span><span class="sxs-lookup"><span data-stu-id="d9ed6-115">Select the transaction types for which you will collect letters.</span></span> <span data-ttu-id="d9ed6-116">Alle offenen Transaktionen für diese Typen werden in die Berechnung einbezogen.</span><span class="sxs-lookup"><span data-stu-id="d9ed6-116">All of the open transactions for these types will be included in the calculation.</span></span>  
2. <span data-ttu-id="d9ed6-117">Wählen Sie im Feld **Mahnschreiben** eine Mahnschreibenoption aus.</span><span class="sxs-lookup"><span data-stu-id="d9ed6-117">In the **Collection letter** field, select an option.</span></span>
3. <span data-ttu-id="d9ed6-118">Geben Sie das Datum des letzten Mahnschreibens an.</span><span class="sxs-lookup"><span data-stu-id="d9ed6-118">Enter the date of the collection letter.</span></span>
4. <span data-ttu-id="d9ed6-119">Wählen Sie ein Buchungsprofil aus, wenn Sie **Verwenden des Buchungsprofils aus** in **Auswählen** geändert haben.</span><span class="sxs-lookup"><span data-stu-id="d9ed6-119">Select a posting profile if you changed **Use posting profile from** to **Select**.</span></span> <span data-ttu-id="d9ed6-120">Es gibt zwei Arten von Buchungsoptionen:</span><span class="sxs-lookup"><span data-stu-id="d9ed6-120">There are two posting profile options:</span></span>   
   - <span data-ttu-id="d9ed6-121">**Konto** – Dient zum Verwenden des Buchungsprofils, das dem Debitorenkonto für die einzelnen Zinsrechnungen zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="d9ed6-121">**Account** – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   
   - <span data-ttu-id="d9ed6-122">**Auswählen** – Dient zum Verwenden des im Feld **Buchungsprofil** ausgewählten Buchungsprofils.</span><span class="sxs-lookup"><span data-stu-id="d9ed6-122">**Select** – Use the posting profile that you select in the **Posting profile** field.</span></span>  
5. <span data-ttu-id="d9ed6-123">Erweitern Sie den Abschnitt **Einzuschließende Datensätze**.</span><span class="sxs-lookup"><span data-stu-id="d9ed6-123">Expand the **Records to include** section.</span></span>
6. <span data-ttu-id="d9ed6-124">Klicken Sie auf **Filter**.</span><span class="sxs-lookup"><span data-stu-id="d9ed6-124">Click **Filter**.</span></span>
7. <span data-ttu-id="d9ed6-125">Geben Sie im Feld **Kriterien** eine "Debitorenkennung" ein.</span><span class="sxs-lookup"><span data-stu-id="d9ed6-125">In the **Criteria** field, enter a Customer ID.</span></span> <span data-ttu-id="d9ed6-126">Geben Sie beispielsweise "US-001" ein.</span><span class="sxs-lookup"><span data-stu-id="d9ed6-126">For example, enter 'US-001'.</span></span>
8. <span data-ttu-id="d9ed6-127">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="d9ed6-127">Click **OK**.</span></span>
9. <span data-ttu-id="d9ed6-128">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="d9ed6-128">Click **OK**.</span></span>

## <a name="print-collection-letters"></a><span data-ttu-id="d9ed6-129">Mahnschreiben drucken</span><span class="sxs-lookup"><span data-stu-id="d9ed6-129">Print collection letters</span></span>
1. <span data-ttu-id="d9ed6-130">Wechseln Sie zu **Kredit und Inkasso > "Mahnschreiben" > "Mahnschreiben prüfen und verarbeiten**.</span><span class="sxs-lookup"><span data-stu-id="d9ed6-130">Go to **Credit and collections > Collection letter > Review and process collection letters**.</span></span>
2. <span data-ttu-id="d9ed6-131">Wählen Sie im Feld **Status** die Option **Erstellt** aus.</span><span class="sxs-lookup"><span data-stu-id="d9ed6-131">In the **Status** field, select **Created**.</span></span>
3. <span data-ttu-id="d9ed6-132">Wählen Sie im Feld **Gedruckt** die Option **Nicht gedruckt** aus.</span><span class="sxs-lookup"><span data-stu-id="d9ed6-132">In the **Printed** field, select **Not printed**.</span></span>
4. <span data-ttu-id="d9ed6-133">Klicken Sie auf **Drucken**.</span><span class="sxs-lookup"><span data-stu-id="d9ed6-133">Click **Print**.</span></span>
5. <span data-ttu-id="d9ed6-134">Klicken Sie **Mahnung**.</span><span class="sxs-lookup"><span data-stu-id="d9ed6-134">Click **Collection letter note**.</span></span>
6. <span data-ttu-id="d9ed6-135">Erweitern Sie den Abschnitt **Einzuschließende Datensätze**.</span><span class="sxs-lookup"><span data-stu-id="d9ed6-135">Expand the **Records to include** section.</span></span>
7. <span data-ttu-id="d9ed6-136">Geben Sie das Abschnittsdatum für Buchungen ein.</span><span class="sxs-lookup"><span data-stu-id="d9ed6-136">Enter the cutoff date for postings.</span></span>
8. <span data-ttu-id="d9ed6-137">Klicken Sie **OK**, um das Mahnschreiben zu drucken.</span><span class="sxs-lookup"><span data-stu-id="d9ed6-137">Click **OK** to print the collection letter.</span></span>
9. <span data-ttu-id="d9ed6-138">Mahnschreiben buchen.</span><span class="sxs-lookup"><span data-stu-id="d9ed6-138">Post the collection letter.</span></span>
   1. <span data-ttu-id="d9ed6-139">Klicken Sie auf **Buchen**.</span><span class="sxs-lookup"><span data-stu-id="d9ed6-139">Click **Post**.</span></span>
   2. <span data-ttu-id="d9ed6-140">Geben Sie ein Buchungsdatum für die Mahnung ein.</span><span class="sxs-lookup"><span data-stu-id="d9ed6-140">Enter the posting date for the collection letter.</span></span>
   3. <span data-ttu-id="d9ed6-141">Erweitern Sie den Abschnitt **Einzuschließende Datensätze**.</span><span class="sxs-lookup"><span data-stu-id="d9ed6-141">Expand the **Records to include** section.</span></span>
   4. <span data-ttu-id="d9ed6-142">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="d9ed6-142">Click **OK**.</span></span>
   5. <span data-ttu-id="d9ed6-143">Wählen Sie im Feld **Status** die Option **Gebucht** aus.</span><span class="sxs-lookup"><span data-stu-id="d9ed6-143">In the **Status** field, select **Posted**.</span></span>
   6. <span data-ttu-id="d9ed6-144">Wählen Sie im Feld **Gedruckt** eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="d9ed6-144">In the **Printed** field, select an option.</span></span>

## <a name="control-collection-letters-at-the-customer-level"></a><span data-ttu-id="d9ed6-145">Steuermahnschreiben auf Debitorenebene</span><span class="sxs-lookup"><span data-stu-id="d9ed6-145">Control collection letters at the customer level</span></span>
<span data-ttu-id="d9ed6-146">Sie können Mahnschreiben auf Debitorenebene auch einrichten, sodass der Mahnschreibencode für jede Buchung erfasst ist, aber das Mahnschreibenverarbeiten basiert auf einer einzelne Mahnschreibenebene, die für den Debitor gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="d9ed6-146">You can also set up collection letters at the customer level so that the collection letter code for each transaction is tracked, but the collection letter processing will be based on a single collection letter level that is stored for the customer.</span></span> <span data-ttu-id="d9ed6-147">Das jeweilige Mahnschreiben enthält alle Buchungen, die für den Debitor überfällig sind.</span><span class="sxs-lookup"><span data-stu-id="d9ed6-147">The single collection letter will contain all transactions that are overdue for the customer.</span></span> <span data-ttu-id="d9ed6-148">Da die Schontage nun auf Debitorenebene nachverfolgt werden, wird das nächste Mahnschreiben nicht übermittelt, bis die Anzahl der Schontagen für das nächste Mahnschreiben im Nummernkreis abgelaufen ist, obwohl Buchungen überfällig werden, nachdem das letzte Mahnschreiben gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="d9ed6-148">Because the grace days are now tracked on the customer level, the next collection letter will not be sent until the number of grace days has passed for the next collection letter in the sequence, even though transactions become overdue after the last collection letter was sent.</span></span> <span data-ttu-id="d9ed6-149">Diese Option verringert die Nummer des Mahnschreibens, die Sie pro Debitor übermitteln.</span><span class="sxs-lookup"><span data-stu-id="d9ed6-149">This option reduces the number of collection letters you will send per customer.</span></span> 

### <a name="set-up-the-customer-to-control-collection-letters-at-the-customer-level"></a><span data-ttu-id="d9ed6-150">Kunden einrichten, um Steuermahnschreiben auf Debitorenebene zu steuern</span><span class="sxs-lookup"><span data-stu-id="d9ed6-150">Set up the customer to control collection letters at the customer level</span></span>
1.  <span data-ttu-id="d9ed6-151">Gehen Sie zu **Kredit und Inkasso > einrichten > Debitorenparameter** und klicken Sie auf die Registerkarte **Inkassi**.</span><span class="sxs-lookup"><span data-stu-id="d9ed6-151">Go to **Credit and collections > Setup > Accounts receivable parameters** and click the **Collections** tab.</span></span> 
2.  <span data-ttu-id="d9ed6-152">Ändern Sie den Wert von **Erstellen Sie Mahnschreiben pro** zu **Debitor**.</span><span class="sxs-lookup"><span data-stu-id="d9ed6-152">Change the value of **Create collection letter per** to **Customer**.</span></span> 
3.  <span data-ttu-id="d9ed6-153">Wechseln Sie zu **Kredit und Inkasso > "Mahnschreiben" > "Mahnschreiben prüfen und verarbeiten**.</span><span class="sxs-lookup"><span data-stu-id="d9ed6-153">Go to **Credit and collections > Collection letter > Review and process collection letters**.</span></span> <span data-ttu-id="d9ed6-154">Es wird ein Mahnschreiben für einen Debitor mit allen überfälligen Buchungen generiert.</span><span class="sxs-lookup"><span data-stu-id="d9ed6-154">Only one collection letter will be generated for a customer with all the overdue transactions.</span></span>

## <a name="ignore-payments-and-credit-memos-when-calculating-the-collection-letter-code"></a><span data-ttu-id="d9ed6-155">Zahlungen und Habenbuchungen für Berechnung des Mahnschreibencodes ignorieren</span><span class="sxs-lookup"><span data-stu-id="d9ed6-155">Ignore payments and credit memos when calculating the collection letter code</span></span>
<span data-ttu-id="d9ed6-156">Wenn Sie Zahlungen und Gutschriften in den Buchungen erfassen, die im Mahnschreiben integriert werden, haben Sie möglicherweise Zahlungen oder Gutschriften, für die ein Mahnschreiben gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="d9ed6-156">If you include payments and credit memos in the transactions that will be included in the collection letters, you may have payments or credit memos that will trigger a collection letter.</span></span> <span data-ttu-id="d9ed6-157">Sie können auch steuern, wie Zahlungen und Gutschriften den Mahnschreibencode steuern, indem Sie den Wert des Parameters **Ignorieren Sie Zahlungen und Gutschriften, wenn Sie den Mahnschreibencode berechnen** ändern.</span><span class="sxs-lookup"><span data-stu-id="d9ed6-157">You can control how payments and credit memos control the collection letter code by changing the value of the **Ignore payments and credit memos when calculating the collection letter code** parameter.</span></span> 

<span data-ttu-id="d9ed6-158">Um Zahlungen und Habenbuchungen für Berechnung des Mahnschreibencodes zu ignorieren, gehen Sie wie folgt vor.</span><span class="sxs-lookup"><span data-stu-id="d9ed6-158">To ignore payments and credit memos when calculating the collection letter code, do the following.</span></span>
1. <span data-ttu-id="d9ed6-159">Gehen Sie zu **Kredit und Inkasso > einrichten > Debitorenparameter** und klicken Sie auf die Registerkarte **Inkassi**.</span><span class="sxs-lookup"><span data-stu-id="d9ed6-159">Go to **Credit and collections > Setup > Accounts receivable parameters** and click the **Collections** tab.</span></span> 
2. <span data-ttu-id="d9ed6-160">Ändern Sie den Wert von **Zahlungen und Habenbuchungen für Berechnung des Mahnschreibencodes ignorieren** auf **Ja** ab.</span><span class="sxs-lookup"><span data-stu-id="d9ed6-160">Change the value of **Ignore payments and credit memos when calculating the collection letter code** to **Yes**.</span></span>

