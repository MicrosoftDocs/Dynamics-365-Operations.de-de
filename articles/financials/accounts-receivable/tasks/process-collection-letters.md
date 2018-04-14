--- 
title: Mahnschreiben verarbeiten
description: Dieses Verfahren zeigt , wie Mahnschreiben erstellt, gedruckt und gebucht werden.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 5c146d6ef34137eb8eef3a5a5123ce0174df3033
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---
# <a name="process-collection-letters"></a><span data-ttu-id="51f1f-103">Mahnschreiben verarbeiten</span><span class="sxs-lookup"><span data-stu-id="51f1f-103">Process collection letters</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="51f1f-104">Dieses Verfahren zeigt , wie Mahnschreiben erstellt, gedruckt und gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="51f1f-104">This procedure shows how to create, print, and post collection letters.</span></span> <span data-ttu-id="51f1f-105">Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="51f1f-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a><span data-ttu-id="51f1f-106">Richten Sie eine Mahnschreibensequenz zum Buchungsprofil ein.</span><span class="sxs-lookup"><span data-stu-id="51f1f-106">Set up a collection letter sequence on the posting profile</span></span>
1. <span data-ttu-id="51f1f-107">Wechseln Sie zu "Kredit und Inkasso" > "Einstellungen" > "Debitorenbuchungsprofile".</span><span class="sxs-lookup"><span data-stu-id="51f1f-107">Go to Credit and collections > Setup > Customer posting profiles.</span></span>
2. <span data-ttu-id="51f1f-108">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="51f1f-108">Click Edit.</span></span>
    * <span data-ttu-id="51f1f-109">Wählen Sie eine Mahnschreibensequenz aus der Dropdownliste aus.</span><span class="sxs-lookup"><span data-stu-id="51f1f-109">Select a collection letter sequence from the drop-down list.</span></span> <span data-ttu-id="51f1f-110">Wenn Sie kein Mahnschreiben für Buchungen dieses Buchungsprofils erstellen wollen, lassen Sie das Feld leer.</span><span class="sxs-lookup"><span data-stu-id="51f1f-110">If you do not want generate collection letters for transactions using this posting profile, leave the field blank.</span></span>  
    * <span data-ttu-id="51f1f-111">Die Tabelleneinschränkungsregisterkarte ermöglicht Ihnen das Verfahren, mit dem Mahnschreiben verarbeitet werden, zu ändern.</span><span class="sxs-lookup"><span data-stu-id="51f1f-111">The table restriction tab allows you to change the way that collection letters are processed.</span></span> <span data-ttu-id="51f1f-112">Wenn dieses Feld auf "Ja" festgelegt ist, werden Mahnschreiben für dieses Buchungsprofil erstellt.</span><span class="sxs-lookup"><span data-stu-id="51f1f-112">If this field is set to Yes, then collection letters will be created for this posting profile.</span></span>  
3. <span data-ttu-id="51f1f-113">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="51f1f-113">Close the page.</span></span>

## <a name="create-collection-letters"></a><span data-ttu-id="51f1f-114">Mahnschreiben erstellen</span><span class="sxs-lookup"><span data-stu-id="51f1f-114">Create collection letters</span></span>
1. <span data-ttu-id="51f1f-115">Wechseln Sie zu "Kredit und Inkasso" > "Mahnschreiben" > "Erstellen von Mahnschreiben".</span><span class="sxs-lookup"><span data-stu-id="51f1f-115">Go to Credit and collections > Collection letter > Create collection letters.</span></span>
    * <span data-ttu-id="51f1f-116">Sie müssen die Buchungsarten auswählen, die Sie anmahnen wollen.</span><span class="sxs-lookup"><span data-stu-id="51f1f-116">You must select the transaction types for which you will collect letters.</span></span> <span data-ttu-id="51f1f-117">Alle offenen Transaktionen für diese Typen werden in die Berechnung einbezogen.</span><span class="sxs-lookup"><span data-stu-id="51f1f-117">All of the open transactions for these types will be included in the calculation.</span></span>  
2. <span data-ttu-id="51f1f-118">Wählen Sie im Feld "Mahnschreiben" eine Mahnschreibenoption aus.</span><span class="sxs-lookup"><span data-stu-id="51f1f-118">In the Collection letter field, select an option.</span></span>
3. <span data-ttu-id="51f1f-119">Geben Sie das Datum des letzten Mahnschreibens an.</span><span class="sxs-lookup"><span data-stu-id="51f1f-119">Enter the date of the collection letter.</span></span>
    * <span data-ttu-id="51f1f-120">Es gibt zwei Buchungsprofiloptionen: Konto - Verwenden Sie das Buchungsprofil, das dem Debitorenkonto für die einzelnen Zinsrechnungen zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="51f1f-120">There are two posting profile options:   Account – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   <span data-ttu-id="51f1f-121">Auswählen – Dient zum Verwenden des im Feld "Buchungsprofil" ausgewählten Buchungsprofils.</span><span class="sxs-lookup"><span data-stu-id="51f1f-121">Select – Use the posting profile that you select in the Posting profile field.</span></span>  
    * <span data-ttu-id="51f1f-122">Wählen Sie ein Buchungsprofil aus, wenn Sie "Verwenden des Buchungsprofils aus" in" Auswählen " geändert haben.</span><span class="sxs-lookup"><span data-stu-id="51f1f-122">Select a posting profile if you changed "Use posting profile from" to "Select".</span></span>  
4. <span data-ttu-id="51f1f-123">Erweitern Sie den Abschnitt "Einzuschließende Datensätze".</span><span class="sxs-lookup"><span data-stu-id="51f1f-123">Expand the Records to include section.</span></span>
5. <span data-ttu-id="51f1f-124">Klicken Sie auf "Filter".</span><span class="sxs-lookup"><span data-stu-id="51f1f-124">Click Filter.</span></span>
6. <span data-ttu-id="51f1f-125">Im Feld "Kriterien" geben Sie eine Debitorenkennung ein.</span><span class="sxs-lookup"><span data-stu-id="51f1f-125">In the Criteria field, In the Criteria field, enter a Customer ID.</span></span> <span data-ttu-id="51f1f-126">Geben Sie beispielsweise "US-001" ein.</span><span class="sxs-lookup"><span data-stu-id="51f1f-126">For example, enter 'US-001'..</span></span>
7. <span data-ttu-id="51f1f-127">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="51f1f-127">Click OK.</span></span>
8. <span data-ttu-id="51f1f-128">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="51f1f-128">Click OK.</span></span>

## <a name="print-collection-letters"></a><span data-ttu-id="51f1f-129">Mahnschreiben drucken</span><span class="sxs-lookup"><span data-stu-id="51f1f-129">Print collection letters</span></span>
1. <span data-ttu-id="51f1f-130">Wechseln Sie zu "Kredit und Inkasso" > "Mahnschreiben" > "Mahnschreiben prüfen und verarbeiten".</span><span class="sxs-lookup"><span data-stu-id="51f1f-130">Go to Credit and collections > Collection letter > Review and process collection letters.</span></span>
2. <span data-ttu-id="51f1f-131">Wählen Sie im Feld "Status" die Option "Erstellt" aus.</span><span class="sxs-lookup"><span data-stu-id="51f1f-131">In the Status field, select 'Created'.</span></span>
3. <span data-ttu-id="51f1f-132">Wählen Sie im Feld "Gedruckt" die Option "Nicht gedruckt" aus.</span><span class="sxs-lookup"><span data-stu-id="51f1f-132">In the Printed field, select 'Not printed'.</span></span>
4. <span data-ttu-id="51f1f-133">Klicken Sie auf Drucken.</span><span class="sxs-lookup"><span data-stu-id="51f1f-133">Click Print.</span></span>
5. <span data-ttu-id="51f1f-134">Klicken Sie Mahnung</span><span class="sxs-lookup"><span data-stu-id="51f1f-134">Click Collection letter note.</span></span>
6. <span data-ttu-id="51f1f-135">Erweitern Sie den Abschnitt "Einzuschließende Datensätze".</span><span class="sxs-lookup"><span data-stu-id="51f1f-135">Expand the Records to include section.</span></span>
7. <span data-ttu-id="51f1f-136">Geben Sie das Abschnittsdatum für Buchungen ein.</span><span class="sxs-lookup"><span data-stu-id="51f1f-136">Enter the cutoff date for postings</span></span>
8. <span data-ttu-id="51f1f-137">Klicken Sie "OK", um das Mahnschreiben zu drucken.</span><span class="sxs-lookup"><span data-stu-id="51f1f-137">Click OK to print the collection letter.</span></span>

## <a name="post-the-collection-letter"></a><span data-ttu-id="51f1f-138">Mahnschreiben buchen</span><span class="sxs-lookup"><span data-stu-id="51f1f-138">Post the collection letter</span></span>
1. <span data-ttu-id="51f1f-139">Klicken Sie auf "Buchen".</span><span class="sxs-lookup"><span data-stu-id="51f1f-139">Click Post.</span></span>
2. <span data-ttu-id="51f1f-140">Geben Sie ein Buchungsdatum für die Mahnung ein.</span><span class="sxs-lookup"><span data-stu-id="51f1f-140">Enter the posting date for the collection letter.</span></span>
3. <span data-ttu-id="51f1f-141">Erweitern Sie den Abschnitt "Einzuschließende Datensätze".</span><span class="sxs-lookup"><span data-stu-id="51f1f-141">Expand the Records to include section.</span></span>
4. <span data-ttu-id="51f1f-142">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="51f1f-142">Click OK.</span></span>
5. <span data-ttu-id="51f1f-143">Wählen Sie im Feld "Status" die Option "Gebucht" aus.</span><span class="sxs-lookup"><span data-stu-id="51f1f-143">In the Status field, select 'Posted'.</span></span>
6. <span data-ttu-id="51f1f-144">Wählen Sie im Feld "Gedruckt" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="51f1f-144">In the Printed field, select an option.</span></span>


