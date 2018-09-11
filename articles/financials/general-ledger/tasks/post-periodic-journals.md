--- 
title: "Periodische Erfassungen veröffentlichen"
description: Periodische Erfassungen werden mitunter als wiederkehrende Erfassungen bezeichnet, da der Betrag, der Text und andere Informationen jedes Mal wiederholt werden, wenn die periodische Erfassung abgerufen wird.
author: aprilolson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTable, LedgerJournalTransPeriodic, LedgerJournalTransDaily
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: c84e9297b2a672600e71fcb614d80d9729a000d6
ms.contentlocale: de-de
ms.lasthandoff: 09/11/2018

---
# <a name="post-periodic-journals"></a><span data-ttu-id="a9f21-103">Periodische Erfassungen veröffentlichen</span><span class="sxs-lookup"><span data-stu-id="a9f21-103">Post periodic journals</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a9f21-104">Periodische Erfassungen werden mitunter als wiederkehrende Erfassungen bezeichnet, da der Betrag, der Text und andere Informationen jedes Mal wiederholt werden, wenn die periodische Erfassung abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="a9f21-104">Periodic journals are sometimes called recurring journals because the amount, text, and other information are repeated each time that the periodic journal is retrieved.</span></span> <span data-ttu-id="a9f21-105">Wenn Sie die periodische Erfassung erstellen, geben Sie das Periodenintervall für die Wiederholung an, wie Tage oder Monate.</span><span class="sxs-lookup"><span data-stu-id="a9f21-105">When you create the periodic journal, you specify the period interval for the recurrence, such as days or months.</span></span> <span data-ttu-id="a9f21-106">Dieses Aufgabenhandbuch erstellt eine periodische Erfassung mit einer monatlichen Wiederholung.</span><span class="sxs-lookup"><span data-stu-id="a9f21-106">This task guide will create a periodic journal with a monthly recurrence.</span></span>



1. <span data-ttu-id="a9f21-107">Wechseln Sie zu "Hauptbuch" > "Periodische Aufgaben" > "Periodische Erfassungen".</span><span class="sxs-lookup"><span data-stu-id="a9f21-107">Go to General ledger > Periodic tasks > Periodic journals.</span></span>
2. <span data-ttu-id="a9f21-108">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="a9f21-108">Click New.</span></span>
3. <span data-ttu-id="a9f21-109">Geben Sie im Feld "Name" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="a9f21-109">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="a9f21-110">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="a9f21-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="a9f21-111">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="a9f21-111">In the Description field, type a value.</span></span>
    * <span data-ttu-id="a9f21-112">Die Beschreibung ist der Name der "Periodischen Erfassung", wenn sie später abgerufen wird. Stellen Sie deshalb sicher, ihr einen entsprechenden Namen zu geben.</span><span class="sxs-lookup"><span data-stu-id="a9f21-112">The description will be the name of the Periodic journal when retrieved later so make sure to give it a relevant name.</span></span>  
6. <span data-ttu-id="a9f21-113">Klicken Sie auf "Positionen".</span><span class="sxs-lookup"><span data-stu-id="a9f21-113">Click Lines.</span></span>
    * <span data-ttu-id="a9f21-114">Eine periodische Erfassung enthält normalerweise mehrere Erfassungspositionen.</span><span class="sxs-lookup"><span data-stu-id="a9f21-114">A periodic journal will typically include several journal lines.</span></span> <span data-ttu-id="a9f21-115">In diesem Aufgabenhandbuch wird jedoch nur eine Position hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a9f21-115">this task guide will however only add one line.</span></span>  
7. <span data-ttu-id="a9f21-116">Geben Sie ein Datum in das Feld "Datum" ein.</span><span class="sxs-lookup"><span data-stu-id="a9f21-116">In the Date field, enter a date.</span></span>
    * <span data-ttu-id="a9f21-117">Das Feld "Datum" enthält das Buchungsdatum für die nächste Übertragung in die Tageserfassung.</span><span class="sxs-lookup"><span data-stu-id="a9f21-117">The Date field contains the posting date for the next transfer to the daily journal.</span></span> <span data-ttu-id="a9f21-118">Für Erfassungen, die jeden Monat abgerufen werden, wird empfohlen, das Datum im Monat zu verwenden, in dem sie gebucht wird, normalerweise das erste oder letzte Datum der Periode.</span><span class="sxs-lookup"><span data-stu-id="a9f21-118">For journals that will be retrieved each month it is recommended to use the date in the month when it will be posted, typically the first or last date in the period.</span></span> <span data-ttu-id="a9f21-119">Es ist möglich, das Feld "Datum" leer zu lassen und ein Datum einzugeben, wenn die Erfassung abgerufen wird, und zwar mithilfe des Felds "Leerdatum".</span><span class="sxs-lookup"><span data-stu-id="a9f21-119">It is possible to leave the Date field blank and to give a date when the journal is retrieved, using the Empty date field.</span></span>    <span data-ttu-id="a9f21-120">Das Feld wird automatisch auf das nächste wiederkehrende Datum aktualisiert, an dem Buchungen abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="a9f21-120">The field is automatically updated to the next recurring date when transactions are retrieved.</span></span>  
8. <span data-ttu-id="a9f21-121">Geben Sie im Feld "Konto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="a9f21-121">In the Account field, specify the desired values.</span></span>
9. <span data-ttu-id="a9f21-122">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="a9f21-122">In the Description field, type a value.</span></span>
10. <span data-ttu-id="a9f21-123">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="a9f21-123">Close the page.</span></span>
11. <span data-ttu-id="a9f21-124">Geben Sie im Feld "Soll" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="a9f21-124">In the Debit field, enter a number.</span></span>
12. <span data-ttu-id="a9f21-125">Geben Sie im Feld "Gegenkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="a9f21-125">In the Offset account field, specify the desired values.</span></span>
13. <span data-ttu-id="a9f21-126">Wählen Sie im Feld "Einheit" die Option "Monate" aus.</span><span class="sxs-lookup"><span data-stu-id="a9f21-126">In the Unit field, select 'Months'.</span></span>
14. <span data-ttu-id="a9f21-127">Geben Sie im Feld "Anzahl der Einheiten" den Wert "1" ein.</span><span class="sxs-lookup"><span data-stu-id="a9f21-127">In the Number of units field, enter '1'.</span></span>
15. <span data-ttu-id="a9f21-128">Geben Sie in das Feld "Letztes Datum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="a9f21-128">In the Last date field, enter a date.</span></span>
    * <span data-ttu-id="a9f21-129">Wenn Sie das letzte Datum in der vorhergehenden Periode eingeben, wird verhindert, dass die wiederkehrende Erfassung irrtümlicherweise im falschen Startzeitraum erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="a9f21-129">Entering last date in the preceding period will prevent that the recurring journal by mistake is created in the wrong starting period.</span></span> <span data-ttu-id="a9f21-130">Das letztes Datum wird später jedes Mal aktualisiert, wenn die periodische Erfassung abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="a9f21-130">Last date will later on be updated each time the periodic journal is retrieved.</span></span>  
16. <span data-ttu-id="a9f21-131">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="a9f21-131">Click Save.</span></span>
17. <span data-ttu-id="a9f21-132">Wechseln Sie zu "Standard-Dashboard".</span><span class="sxs-lookup"><span data-stu-id="a9f21-132">Go to Default dashboard.</span></span>
18. <span data-ttu-id="a9f21-133">Wechseln Sie zu "Hauptbuch" > "Journaleinträge" > "Allgemeine Erfassungen".</span><span class="sxs-lookup"><span data-stu-id="a9f21-133">Go to General ledger > Journal entries > General journals.</span></span>
19. <span data-ttu-id="a9f21-134">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="a9f21-134">Click New.</span></span>
20. <span data-ttu-id="a9f21-135">Geben Sie im Feld "Name" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="a9f21-135">In the Name field, enter or select a value.</span></span>
21. <span data-ttu-id="a9f21-136">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="a9f21-136">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="a9f21-137">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="a9f21-137">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="a9f21-138">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="a9f21-138">In the Description field, type a value.</span></span>
24. <span data-ttu-id="a9f21-139">Klicken Sie auf "Positionen".</span><span class="sxs-lookup"><span data-stu-id="a9f21-139">Click Lines.</span></span>
25. <span data-ttu-id="a9f21-140">Klicken Sie auf "Periodische Erfassung".</span><span class="sxs-lookup"><span data-stu-id="a9f21-140">Click Period journal.</span></span>
26. <span data-ttu-id="a9f21-141">Klicken Sie auf "Erfassung abrufen".</span><span class="sxs-lookup"><span data-stu-id="a9f21-141">Click Retrieve journal.</span></span>
27. <span data-ttu-id="a9f21-142">Geben Sie in das Feld "Bis Datum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="a9f21-142">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="a9f21-143">Das "Bis Datum" dient als Abschnittsdatum für die periodischen Belegpositionen.</span><span class="sxs-lookup"><span data-stu-id="a9f21-143">The To date serves as the cutoff date for the periodic voucher lines.</span></span> <span data-ttu-id="a9f21-144">Auf Grundlage der Wiederholungseinstellung werden das "Letzte Datum" und das "Bis Datum" in derselben Position möglicherweise mehr als einmal in die sich ergebende Erfassung einbezogen.</span><span class="sxs-lookup"><span data-stu-id="a9f21-144">Based on the recurrence setting, the Last date and To date the same line might be included more than once in the resulting journal.</span></span> <span data-ttu-id="a9f21-145">Das "Bis Datum" wird automatisch auf Grundlage des Sitzungsdatums aktualisiert, an dem zum letzten Mal die periodische Position an eine Erfassung übertragen wurde.</span><span class="sxs-lookup"><span data-stu-id="a9f21-145">To date is automatically updated based on  session date of the last time the periodic line was transferred to a journal.</span></span>  
28. <span data-ttu-id="a9f21-146">Geben Sie im Feld "Periodische Erfassungsnummer" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="a9f21-146">In the Periodic journal number field, enter or select a value.</span></span>
29. <span data-ttu-id="a9f21-147">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="a9f21-147">In the list, click the link in the selected row.</span></span>
30. <span data-ttu-id="a9f21-148">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="a9f21-148">Click OK.</span></span>
    * <span data-ttu-id="a9f21-149">Die periodischen Erfassung kann je nach Bedarf und Einstellung jetzt überprüft, genehmigt oder gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="a9f21-149">The period journal can now be reviewed, approved or posted depending on requirement and setup.</span></span>  


