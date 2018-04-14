--- 
title: Mahnschreibensequenzen einrichten
description: Erstellen Sie mithilfe dieser Aufgabenanleitung eine Mahnschreibensequenz.
author: mikefalkner
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 5905a630addfd850d22d34bdbecf116e83b4933f
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-collection-letter-sequence"></a><span data-ttu-id="569d1-103">Mahnschreibensequenzen einrichten</span><span class="sxs-lookup"><span data-stu-id="569d1-103">Create a collection letter sequence</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="569d1-104">Erstellen Sie mithilfe dieser Aufgabenanleitung eine Mahnschreibensequenz.</span><span class="sxs-lookup"><span data-stu-id="569d1-104">Use this task guide to create a collection letter sequence.</span></span> <span data-ttu-id="569d1-105">Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="569d1-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="569d1-106">Wechseln Sie zu "Kredit und Inkasso" > "Einstellungen > "Mahnschreibensequenz einrichten".</span><span class="sxs-lookup"><span data-stu-id="569d1-106">Go to Credit and collections > Setup > Set up collection letter sequence.</span></span>
2. <span data-ttu-id="569d1-107">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="569d1-107">Click New.</span></span>
3. <span data-ttu-id="569d1-108">Geben Sie im Feld "Mahnschreibensequenz" eine Sequenzkennung ein, die die Reihenfolge darstellt.</span><span class="sxs-lookup"><span data-stu-id="569d1-108">In the Collection letter sequence field, enter a sequence ID that will represent the sequence.</span></span> <span data-ttu-id="569d1-109">Sie wird verwendet, wenn Sie ein Buchungsprofil einrichten.</span><span class="sxs-lookup"><span data-stu-id="569d1-109">It will be used when you set up a posting profile.</span></span>
4. <span data-ttu-id="569d1-110">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="569d1-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="569d1-111">Die Zahlungsbedingungen sind optional.</span><span class="sxs-lookup"><span data-stu-id="569d1-111">The terms of payment is optional.</span></span> <span data-ttu-id="569d1-112">Wenn Sie einen Wert hier eingeben, verwendet die Mahngebührenrechnung diese Zahlungsbedingungen anstelle der Zahlungsbedingungen, die beim Debitor gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="569d1-112">If you enter a value here, the collection letter fee invoice will use these terms of payment instead of the terms of payment stored with the customer.</span></span>  
5. <span data-ttu-id="569d1-113">Wählen Sie im Mahnschreibencode-Feld den Code für das erste Mahnschreiben aus, das Sie senden möchten.</span><span class="sxs-lookup"><span data-stu-id="569d1-113">In the collection letter code field, select the code for the first collection letter that you want to send.</span></span>
    * <span data-ttu-id="569d1-114">Das erste Mahnschreiben wird gemäß dem Fälligkeitsdatum auf der Rechnung, der Toleranzperiode, die Sie im Feld "Tage" auf dieser Position eingegeben haben und anderen Informationen, die Sie auf dieser Position eingeben, erstellt.</span><span class="sxs-lookup"><span data-stu-id="569d1-114">The first collection letter is created according to the due date on the invoice, the value that you enter for the grace period in the Days field on this line, and other information that you enter on this line.</span></span>  
6. <span data-ttu-id="569d1-115">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="569d1-115">In the Description field, type a value.</span></span>
    * <span data-ttu-id="569d1-116">Die Währung für die Gebühr ist standardmäßig die Währung des Debitors.</span><span class="sxs-lookup"><span data-stu-id="569d1-116">The currency for the fee defaults to the customer currency.</span></span> <span data-ttu-id="569d1-117">Dieser Währungscode kann sich von der Rechnungswährung unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="569d1-117">This currency code can be different than the invoice currency.</span></span>  
7. <span data-ttu-id="569d1-118">Klicken Sie auf "Hinzufügen", um das nächste Mahnschreiben hinzuzufügen, das in der Reihenfolge gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="569d1-118">Click Add to add the next collection letter that will be sent in the sequence</span></span>
    * <span data-ttu-id="569d1-119">In vielen Fällen ist das erste Mahnschreiben nur eine Warnung.</span><span class="sxs-lookup"><span data-stu-id="569d1-119">In many cases, the first collection letter is just a warning.</span></span> <span data-ttu-id="569d1-120">Sie können Gebühren nach Bedarf hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="569d1-120">You can add fees if needed.</span></span>  
8. <span data-ttu-id="569d1-121">Wählen Sie im Mahnschreibencode-Feld das nächste Mahnschreiben aus, das in der Reihenfolge gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="569d1-121">In the collection letter code field, select the next collection letter that will be sent in the sequence.</span></span>
9. <span data-ttu-id="569d1-122">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="569d1-122">In the Description field, type a value.</span></span>
10. <span data-ttu-id="569d1-123">Wählen Sie im Hauptkontofeld das Umsatzerlöskonto aus, das für Gebühren verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="569d1-123">In the main account field, select the revenue account that will be used for fees.</span></span>
11. <span data-ttu-id="569d1-124">Geben Sie die Gebühr ein, die berechnet wird, wenn dieses Mahnschreiben gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="569d1-124">Enter the fee that will be charged when this collection letter is posted.</span></span>
12. <span data-ttu-id="569d1-125">Klicken Sie im Feld "Artikel-Mehrwertsteuergruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="569d1-125">In the Item sales tax group field, click the drop down button to open the lookup.</span></span>
    * <span data-ttu-id="569d1-126">Wählen Sie eine Artikel-Mehrwertsteuergruppe aus, wenn Mehrwertsteuern auf die Gebühr berechnet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="569d1-126">Select an item sales tax group if sales taxes must be calculated on the fee.</span></span>  
13. <span data-ttu-id="569d1-127">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="569d1-127">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="569d1-128">Geben Sie den überfälligen Mindestsaldo ein, der erforderlich ist, bevor ein Mahnschreiben gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="569d1-128">Enter the minimum overdue balance required before a collection letter is sent.</span></span>
15. <span data-ttu-id="569d1-129">Geben Sie die Anzahl der Toleranztage ein, die Sie gestatten werden.</span><span class="sxs-lookup"><span data-stu-id="569d1-129">Enter the number of grace days that you will allow.</span></span>
    * <span data-ttu-id="569d1-130">Dies ist die Anzahl von Tagen nach dem Fälligkeitsdatum, damit ein Mahnschreiben generiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="569d1-130">This is the number of days after the due date that a collection letter can be generated.</span></span> <span data-ttu-id="569d1-131">Das Fälligkeitsdatum, das für die Berechnung verwendet wird, hängt von der Position des Mahnschreibens in der Mahnschreibensequenz ab: ⦁ Die Toleranzperiode für Mahnschreiben 1 ist relativ zum Fälligkeitsdatum auf der Rechnung.</span><span class="sxs-lookup"><span data-stu-id="569d1-131">The due date that is used for the calculation depends on the position of the collection letter in the collection letter sequence:   ⦁    The grace period for collection letter 1 is relative to the due date on the invoice.</span></span>  <span data-ttu-id="569d1-132">⦁ Die Toleranzperiode für Mahnschreiben 2 und höhere ist relativ zum Datum, an dem das vorherige Mahnschreiben gebucht oder gedruckt wird, abhängig von der Auswahl im Feld "Mahnschreibencode aktualisieren" auf der Seite "Debitorenparameter".</span><span class="sxs-lookup"><span data-stu-id="569d1-132">⦁ The grace period for collection letters 2 and higher is relative to the date that the previous collection letter is posted or printed, depending on the selection in the Update collection letter code field in the Accounts receivable parameters page.</span></span>  
16. <span data-ttu-id="569d1-133">Klicken Sie auf "Hinzufügen", um das letzte Mahnschreiben in der Reihenfolge hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="569d1-133">Click Add to add the last collection letter in the sequence.</span></span>
    * <span data-ttu-id="569d1-134">Sie können für eine Mahnschreibensequenz bis zu fünf Mahnschreibencodes hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="569d1-134">You can add up to five collection letter codes for a collection letter sequence.</span></span>  
17. <span data-ttu-id="569d1-135">Wählen Sie im Mahnschreibencode-Feld das nächste Mahnschreiben aus, das in der Reihenfolge gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="569d1-135">In the collection letter code field, select the next collection letter that will be sent in the sequence.</span></span>
18. <span data-ttu-id="569d1-136">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="569d1-136">In the Description field, type a value.</span></span>
19. <span data-ttu-id="569d1-137">Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="569d1-137">In the Main account field, specify the desired values.</span></span>
20. <span data-ttu-id="569d1-138">Geben Sie eine Zahl in das Feld "Gebühr in Währung" ein.</span><span class="sxs-lookup"><span data-stu-id="569d1-138">In the Fee in currency field, enter a number.</span></span>
21. <span data-ttu-id="569d1-139">Klicken Sie im Feld "Mehrwertsteuergruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="569d1-139">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="569d1-140">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="569d1-140">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="569d1-141">Geben Sie im Feld "Überfälliger Mindestsaldo" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="569d1-141">In the Minimum overdue balance field, enter a number.</span></span>
24. <span data-ttu-id="569d1-142">Geben Sie im Feld "Tage" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="569d1-142">In the Days field, enter a number.</span></span>
25. <span data-ttu-id="569d1-143">Aktivieren Sie dieses Kontrollkästchen, um den Debitor von zusätzlichen Lieferungen und der Rechnungsstellung auszuschließen.</span><span class="sxs-lookup"><span data-stu-id="569d1-143">Select this check box to stop the customer from additional deliveries and invoicing.</span></span>
    * <span data-ttu-id="569d1-144">Damit das Konto entsperrt wird, wählen Sie im Feld "Rechnungsstellung und Lieferung gesperrt" der Seite "Debitoren" "Nein" aus.</span><span class="sxs-lookup"><span data-stu-id="569d1-144">To unblock the account, select No in the Invoicing and delivery on hold field in the Customers page.</span></span>  
26. <span data-ttu-id="569d1-145">Erweitern Sie das Inforegister "Hinweis".</span><span class="sxs-lookup"><span data-stu-id="569d1-145">Expand the Note fasttab.</span></span>
27. <span data-ttu-id="569d1-146">Geben Sie den Text ein, der im Mahnschreiben für den ausgewählten Mahnschreibencode angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="569d1-146">Enter the text to appear on the collection letter for the selected collection letter code.</span></span>
    * <span data-ttu-id="569d1-147">Sie können diesen Text in mehrere Sprachen mithilfe des Menüs "Übersetzungen" über dem Hinweisfeld übersetzen.</span><span class="sxs-lookup"><span data-stu-id="569d1-147">You can translate this text in to multiple languages using the Translations menu above the note box.</span></span>  


