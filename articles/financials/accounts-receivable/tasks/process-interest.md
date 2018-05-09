--- 
title: Prozesszinsen
description: Dieses Verfahren zeigt an, wie Zinsrechnungen erstellt, gedruckt und gebucht werden.
author: ShivamPandey-msft
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
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: cb4a3e9420c8749213ac17274575bae79b6e14a8
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---
# <a name="process-interest"></a><span data-ttu-id="8e87b-103">Prozesszinsen</span><span class="sxs-lookup"><span data-stu-id="8e87b-103">Process interest</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8e87b-104">Dieses Verfahren zeigt an, wie Zinsrechnungen erstellt, gedruckt und gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="8e87b-104">This procedure shows how to create, print, and post interest notes.</span></span> <span data-ttu-id="8e87b-105">Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="8e87b-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-interest-on-the-posting-profile"></a><span data-ttu-id="8e87b-106">Zinsen für das Buchungsprofil einrichten</span><span class="sxs-lookup"><span data-stu-id="8e87b-106">Set up interest on the posting profile</span></span>
1. <span data-ttu-id="8e87b-107">Wechseln Sie zu "Kredit und Inkasso" > "Einstellungen" > "Debitorenbuchungsprofile".</span><span class="sxs-lookup"><span data-stu-id="8e87b-107">Go to Credit and collections > Setup > Customer posting profiles.</span></span>
2. <span data-ttu-id="8e87b-108">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="8e87b-108">Click Edit.</span></span>
    * <span data-ttu-id="8e87b-109">Wählen Sie einen Zinscode aus der Dropdownliste aus.</span><span class="sxs-lookup"><span data-stu-id="8e87b-109">Select an interest code from the drop-down list.</span></span> <span data-ttu-id="8e87b-110">Wenn Sie nicht möchten, dass Zinsen für Transaktionen mithilfe dieses Buchungsprofils berechnet werden, lassen Sie das Feld leer.</span><span class="sxs-lookup"><span data-stu-id="8e87b-110">If you do not want interest calculated for transactions using this posting profile, leave the field blank.</span></span>  
    * <span data-ttu-id="8e87b-111">Die Registerkarte "Tabelleneinschränkung" ermöglicht Ihnen, das Verfahren zu ändern, mit dem Zinsen verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="8e87b-111">The Table restriction tab allows you to change the way that interest is processed.</span></span> <span data-ttu-id="8e87b-112">Wenn dieses Feld auf "Ja" festgelegt ist, werden Zinsen für dieses Buchungsprofil berechnet.</span><span class="sxs-lookup"><span data-stu-id="8e87b-112">If this field is set to Yes, then interest will be calculated for this posting profile.</span></span>  

## <a name="calculate-interest"></a><span data-ttu-id="8e87b-113">Zinsen berechnen</span><span class="sxs-lookup"><span data-stu-id="8e87b-113">Calculate interest</span></span>
1. <span data-ttu-id="8e87b-114">Wechseln Sie zu "Kredit und Inkasso" > "Zinsen" > "Zinsrechnungen erstellen".</span><span class="sxs-lookup"><span data-stu-id="8e87b-114">Go to Credit and collections > Interest > Create interest notes.</span></span>
    * <span data-ttu-id="8e87b-115">Sie müssen die Transaktionstypen auswählen, für die Sie Zinsen berechnen.</span><span class="sxs-lookup"><span data-stu-id="8e87b-115">You must select the transaction types for which you will calculate interest.</span></span> <span data-ttu-id="8e87b-116">Alle offenen Transaktionen für diese Typen werden in die Berechnung einbezogen.</span><span class="sxs-lookup"><span data-stu-id="8e87b-116">All of the open transactions for these types will be included in the calculation.</span></span>  
    * <span data-ttu-id="8e87b-117">Wenn Sie Zinsen auswählen, berechnen Sie die Zinsen auf die Zinsen.</span><span class="sxs-lookup"><span data-stu-id="8e87b-117">If you select Interest, you will calculate interest on interest.</span></span> <span data-ttu-id="8e87b-118">Sie sollten die Gesetze prüfen, die für die Berechnung von Zinsen auf Zinsen gelten, bevor Sie diese Transaktionen einbeziehen.</span><span class="sxs-lookup"><span data-stu-id="8e87b-118">You may want to check the laws governing the calculation of interest on interest before including these transactions.</span></span>  
    * <span data-ttu-id="8e87b-119">Zinsen werden ab diesem Datum bis zu "Bis Datum" berechnet.</span><span class="sxs-lookup"><span data-stu-id="8e87b-119">Interest will be calculated from this date to the "To date".</span></span> <span data-ttu-id="8e87b-120">Wenn Sie kein "Von Datum" angeben, dann werden alle nicht gebuchten Zinsrechnungen storniert und Zinsen werden ab dem Transaktionsdatum neu berechnet.</span><span class="sxs-lookup"><span data-stu-id="8e87b-120">If you do not specific a "From date", then all unposted interest notes will be canceled and interest will be recalculated from the transaction date.</span></span>  
2. <span data-ttu-id="8e87b-121">Geben Sie das Datum der Zinsrechnung ein.</span><span class="sxs-lookup"><span data-stu-id="8e87b-121">Enter the date of the interest note.</span></span>
    * <span data-ttu-id="8e87b-122">Es gibt drei Buchungsprofiloptionen: Konto - Verwenden Sie das Buchungsprofil, das dem Debitorenkonto für die einzelnen Zinsrechnungen zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="8e87b-122">There are three posting profile options:   Account – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   <span data-ttu-id="8e87b-123">Auswählen – Dient zum Verwenden des im Feld "Buchungsprofil" ausgewählten Buchungsprofils.</span><span class="sxs-lookup"><span data-stu-id="8e87b-123">Select – Use the posting profile that you select in the Posting profile field.</span></span>   <span data-ttu-id="8e87b-124">Transaktion – Dient zum Verwenden des jeweiligen Buchungsprofils von Transaktionen, für die Zinsen für die einzelnen Zinsrechnungen berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="8e87b-124">Transaction – Use the individual posting profile from transactions on which interest is calculated for each interest note.</span></span> <span data-ttu-id="8e87b-125">Für Transaktionen ohne zugewiesenes Buchungsprofil wird das Buchungsprofil verwendet, das im Bereich "Sachkonto und Mehrwertsteuer" des Formulars "Debitorenparameter" angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="8e87b-125">Transactions that do not have an assigned posting profile will use the posting profile that is specified in the Ledger and sales tax area of the Accounts receivable parameters form.</span></span>  
    * <span data-ttu-id="8e87b-126">Wählen Sie hier ein Buchungsprofil aus, wenn Sie "Verwenden des Buchungsprofils aus" in" Auswählen" geändert haben.</span><span class="sxs-lookup"><span data-stu-id="8e87b-126">Select a posting profile here if you changed "Use posting profile from" to "Select".</span></span>  
3. <span data-ttu-id="8e87b-127">Erweitern oder reduzieren Sie "Datensätze", um den Abschnitt einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="8e87b-127">Expand or collapse the Records to include section.</span></span>
4. <span data-ttu-id="8e87b-128">Klicken Sie auf "Filter".</span><span class="sxs-lookup"><span data-stu-id="8e87b-128">Click Filter.</span></span>
5. <span data-ttu-id="8e87b-129">Geben Sie im Feld "Kriterien" eine "Debitorenkennung" ein.</span><span class="sxs-lookup"><span data-stu-id="8e87b-129">In the Criteria field, enter a Customer ID.</span></span> <span data-ttu-id="8e87b-130">Geben Sie beispielsweise "US-001" ein.</span><span class="sxs-lookup"><span data-stu-id="8e87b-130">For example, enter 'US-001'..</span></span>
6. <span data-ttu-id="8e87b-131">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8e87b-131">Click OK.</span></span>
7. <span data-ttu-id="8e87b-132">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8e87b-132">Click OK.</span></span>

## <a name="print-interest-notes"></a><span data-ttu-id="8e87b-133">Zinsrechnungen drucken</span><span class="sxs-lookup"><span data-stu-id="8e87b-133">Print interest notes</span></span>
1. <span data-ttu-id="8e87b-134">Wechseln Sie zu "Kredit und Inkasso" > "Zinsen" > "Zinsrechnungen prüfen und verarbeiten".</span><span class="sxs-lookup"><span data-stu-id="8e87b-134">Go to Credit and collections > Interest > Review and process interest notes.</span></span>
2. <span data-ttu-id="8e87b-135">Wählen Sie im Feld "Status" die Option "Erstellt" aus.</span><span class="sxs-lookup"><span data-stu-id="8e87b-135">In the Status field, select 'Created'.</span></span>
3. <span data-ttu-id="8e87b-136">Wählen Sie im Feld "Gedruckt" die Option "Nicht gedruckt" aus.</span><span class="sxs-lookup"><span data-stu-id="8e87b-136">In the Printed field, select 'Not printed'.</span></span>
4. <span data-ttu-id="8e87b-137">Klicken Sie auf Drucken.</span><span class="sxs-lookup"><span data-stu-id="8e87b-137">Click Print.</span></span>
5. <span data-ttu-id="8e87b-138">Erweitern oder reduzieren Sie "Datensätze", um den Abschnitt einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="8e87b-138">Expand or collapse the Records to include section.</span></span>
6. <span data-ttu-id="8e87b-139">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8e87b-139">Click OK.</span></span>
7. <span data-ttu-id="8e87b-140">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8e87b-140">Close the page.</span></span>

## <a name="post-the-interest-note"></a><span data-ttu-id="8e87b-141">Die Zinsrechnung buchen</span><span class="sxs-lookup"><span data-stu-id="8e87b-141">Post the interest note</span></span>
1. <span data-ttu-id="8e87b-142">Wählen Sie eine Zinsrechnung aus, die zum Buchen bereit ist (Status wird erstellt).</span><span class="sxs-lookup"><span data-stu-id="8e87b-142">Select an interest note that is ready to post (status is created).</span></span>
2. <span data-ttu-id="8e87b-143">Klicken Sie auf "Buchen".</span><span class="sxs-lookup"><span data-stu-id="8e87b-143">Click Post.</span></span>
3. <span data-ttu-id="8e87b-144">Geben Sie das Buchungsdatum für die Zinsrechnung ein.</span><span class="sxs-lookup"><span data-stu-id="8e87b-144">Enter the posting date for the interest note.</span></span>
    * <span data-ttu-id="8e87b-145">Wählen Sie "Ja" aus, um eine Hauptbuchtransaktion für jede Zinsrechnung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8e87b-145">Select Yes to create a general ledger transaction for each interest note.</span></span>     <span data-ttu-id="8e87b-146">Wenn Sie nicht "Ja" auswählen, werden die Zinsen für alle Zinsrechnungen für den Debitor kumuliert und in einer einzigen Transaktion im Hauptbuch gebucht.</span><span class="sxs-lookup"><span data-stu-id="8e87b-146">If you do not select Yes, the interest on all interest notes to the customer is accumulated and posted to the general ledger in one transaction.</span></span>  
4. <span data-ttu-id="8e87b-147">Erweitern oder reduzieren Sie "Datensätze", um den Abschnitt einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="8e87b-147">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="8e87b-148">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8e87b-148">Click OK.</span></span>
6. <span data-ttu-id="8e87b-149">Wählen Sie im Feld "Status" die Option "Gebucht" aus.</span><span class="sxs-lookup"><span data-stu-id="8e87b-149">In the Status field, select 'Posted'.</span></span>


