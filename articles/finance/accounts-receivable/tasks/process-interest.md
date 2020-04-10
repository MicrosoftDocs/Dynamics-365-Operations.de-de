---
title: Prozesszinsen
description: Dieses Verfahren zeigt an, wie Zinsrechnungen erstellt, gedruckt und gebucht werden.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, SysQueryForm, CustInterestNote, SrsReportViewerForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 093fbd23f9fcaf62db9988a98a94b8cebf582768
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140144"
---
# <a name="process-interest"></a><span data-ttu-id="22eeb-103">Prozesszinsen</span><span class="sxs-lookup"><span data-stu-id="22eeb-103">Process interest</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="22eeb-104">Dieses Verfahren zeigt an, wie Zinsrechnungen erstellt, gedruckt und gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="22eeb-104">This procedure shows how to create, print, and post interest notes.</span></span> <span data-ttu-id="22eeb-105">Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="22eeb-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-interest-on-the-posting-profile"></a><span data-ttu-id="22eeb-106">Zinsen für das Buchungsprofil einrichten</span><span class="sxs-lookup"><span data-stu-id="22eeb-106">Set up interest on the posting profile</span></span>
1. <span data-ttu-id="22eeb-107">Gehen Sie im Navigationsbereich **Navigationsbereich** zu **Module > Guthaben und Einzüge > Einrichtung > Kundenbuchungsprofile**.</span><span class="sxs-lookup"><span data-stu-id="22eeb-107">In the **Navigation pane**, go to **Modules > Credit and collections > Setup > Customer posting profiles**.</span></span>
2. <span data-ttu-id="22eeb-108">Klicken Sie auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="22eeb-108">Click **Edit**.</span></span>
3. <span data-ttu-id="22eeb-109">Wählen Sie im Feld **Einrichtung-FastTab**, im Feld **Zinscode**, einen Zinscode aus der Dropdown-Liste aus.</span><span class="sxs-lookup"><span data-stu-id="22eeb-109">In the **Setup fastTab**, in the **Interest code** field, select an interest code from the drop-down list.</span></span> <span data-ttu-id="22eeb-110">Wenn Sie nicht möchten, dass Zinsen für Transaktionen mithilfe dieses Buchungsprofils berechnet werden, lassen Sie das Feld leer.</span><span class="sxs-lookup"><span data-stu-id="22eeb-110">If you do not want interest calculated for transactions using this posting profile, leave the field blank.</span></span> <span data-ttu-id="22eeb-111">Die **Tabellenbeschränkung** fastTab ermöglicht es Ihnen, die Art und Weise, wie Zinsen verarbeitet werden, zu ändern.</span><span class="sxs-lookup"><span data-stu-id="22eeb-111">The **Table restriction** fastTab allows you to change the way that interest is processed.</span></span> <span data-ttu-id="22eeb-112">Wenn dieses Feld auf "Ja" festgelegt ist, werden Zinsen für dieses Buchungsprofil berechnet.</span><span class="sxs-lookup"><span data-stu-id="22eeb-112">If this field is set to Yes, then interest will be calculated for this posting profile.</span></span>  

## <a name="calculate-interest"></a><span data-ttu-id="22eeb-113">Zinsen berechnen</span><span class="sxs-lookup"><span data-stu-id="22eeb-113">Calculate interest</span></span>
1. <span data-ttu-id="22eeb-114">Gehen Sie im Navigationsbereich **Navigationsbereich** zu **Module > Guthaben und Einzüge > Zinsen > Zinsen > Zinsnoten erstellen**.</span><span class="sxs-lookup"><span data-stu-id="22eeb-114">In the **Navigation pane**, go to **Modules > Credit and collections > Interest > Create interest notes**.</span></span>
2. <span data-ttu-id="22eeb-115">Sie müssen die Transaktionstypen auswählen, für die Sie Zinsen berechnen.</span><span class="sxs-lookup"><span data-stu-id="22eeb-115">You must select the transaction types for which you will calculate interest.</span></span> <span data-ttu-id="22eeb-116">Alle offenen Transaktionen für diese Typen werden in die Berechnung einbezogen.</span><span class="sxs-lookup"><span data-stu-id="22eeb-116">All of the open transactions for these types will be included in the calculation.</span></span>  
3. <span data-ttu-id="22eeb-117">Wenn Sie **Zinsen** auf'Ja' setzen, berechnen Sie die Zinsen.</span><span class="sxs-lookup"><span data-stu-id="22eeb-117">If you set **Interest** to 'Yes', you will calculate interest on interest.</span></span> <span data-ttu-id="22eeb-118">Sie sollten die Gesetze prüfen, die für die Berechnung von Zinsen auf Zinsen gelten, bevor Sie diese Transaktionen einbeziehen.</span><span class="sxs-lookup"><span data-stu-id="22eeb-118">You may want to check the laws governing the calculation of interest on interest before including these transactions.</span></span>  
4. <span data-ttu-id="22eeb-119">Geben Sie im Feld **Ab Datum** ein Datum ein, ab dem die Zinsen berechnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="22eeb-119">In the **From date** field, enter a date from which the interest will be calculated.</span></span> <span data-ttu-id="22eeb-120">Wenn Sie kein **Ab-Datum** angeben, werden alle nicht gebuchten Zinsnoten storniert und die Zinsen ab dem Transaktionsdatum neu berechnet.</span><span class="sxs-lookup"><span data-stu-id="22eeb-120">If you do not specific a **From date**, then all unposted interest notes will be canceled and interest will be recalculated from the transaction date.</span></span>
5. <span data-ttu-id="22eeb-121">Geben Sie im Feld **Bis Datum** ein Datum ein, bis zu dem die Zinsen berechnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="22eeb-121">In the **To date** field, enter a date to which the interest would be calculated.</span></span>
6. <span data-ttu-id="22eeb-122">Wählen Sie im Feld **Buchungsprofil verwenden aus** eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="22eeb-122">In the **Use posting profile from** field, select an option.</span></span> <span data-ttu-id="22eeb-123">Es gibt drei Möglichkeiten des Buchungsprofils:</span><span class="sxs-lookup"><span data-stu-id="22eeb-123">There are three posting profile options:</span></span>
    - <span data-ttu-id="22eeb-124">Konto – Dient zum Verwenden des Buchungsprofils, das dem Debitorenkonto für die einzelnen Zinsrechnungen zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="22eeb-124">Account – Use the posting profile that is assigned to the customer account for each interest note.</span></span> 
    - <span data-ttu-id="22eeb-125">Auswählen – Dient zum Verwenden des im Feld "Buchungsprofil" ausgewählten Buchungsprofils.</span><span class="sxs-lookup"><span data-stu-id="22eeb-125">Select – Use the posting profile that you select in the Posting profile field.</span></span>
    - <span data-ttu-id="22eeb-126">Transaktion – Dient zum Verwenden des jeweiligen Buchungsprofils von Transaktionen, für die Zinsen für die einzelnen Zinsrechnungen berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="22eeb-126">Transaction – Use the individual posting profile from transactions on which interest is calculated for each interest note.</span></span> <span data-ttu-id="22eeb-127">Für Transaktionen ohne zugewiesenes Buchungsprofil wird das Buchungsprofil verwendet, das im Bereich "Sachkonto und Mehrwertsteuer" des Formulars "Debitorenparameter" angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="22eeb-127">Transactions that do not have an assigned posting profile will use the posting profile that is specified in the Ledger and sales tax area of the Accounts receivable parameters form.</span></span>  
7. <span data-ttu-id="22eeb-128">Erweitern Sie die **Datensätze um** fastTab.</span><span class="sxs-lookup"><span data-stu-id="22eeb-128">Expand the **Records to include** fastTab.</span></span>
8. <span data-ttu-id="22eeb-129">Klicken Sie auf **Filter**.</span><span class="sxs-lookup"><span data-stu-id="22eeb-129">Click **Filter**.</span></span>
9. <span data-ttu-id="22eeb-130">Geben Sie im Feld **Kriterien** eine "Debitorenkennung" ein.</span><span class="sxs-lookup"><span data-stu-id="22eeb-130">In the **Criteria** field, enter a Customer ID.</span></span> <span data-ttu-id="22eeb-131">Geben Sie beispielsweise "US-001" ein.</span><span class="sxs-lookup"><span data-stu-id="22eeb-131">For example, enter 'US-001'.</span></span>
6. <span data-ttu-id="22eeb-132">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="22eeb-132">Click **OK**.</span></span>
7. <span data-ttu-id="22eeb-133">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="22eeb-133">Click **OK**.</span></span>

## <a name="print-interest-notes"></a><span data-ttu-id="22eeb-134">Zinsrechnungen drucken</span><span class="sxs-lookup"><span data-stu-id="22eeb-134">Print interest notes</span></span>
1. <span data-ttu-id="22eeb-135">Gehen Sie im Navigationsbereich **Navigationsbereich** zu **Module > Guthaben und Sammlungen > Zinsen > Zinsen > Zinsnotizen überprüfen und bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="22eeb-135">In the **Navigation pane**, go to **Modules > Credit and collections > Interest > Review and process interest notes**.</span></span>
2. <span data-ttu-id="22eeb-136">Wählen Sie im Feld **Status** die Option 'Erstellt'.</span><span class="sxs-lookup"><span data-stu-id="22eeb-136">In the **Status** field, select 'Created'.</span></span>
3. <span data-ttu-id="22eeb-137">Wählen Sie im Feld **Drucken** die Option 'Nicht gedruckt'.</span><span class="sxs-lookup"><span data-stu-id="22eeb-137">In the **Printed** field, select 'Not printed'.</span></span>
4. <span data-ttu-id="22eeb-138">Klicken Sie auf **Drucken**.</span><span class="sxs-lookup"><span data-stu-id="22eeb-138">Click **Print**.</span></span>
5. <span data-ttu-id="22eeb-139">Erweitern Sie die **Datensätze um** fastTab.</span><span class="sxs-lookup"><span data-stu-id="22eeb-139">Expand the **Records to include** fastTab.</span></span>
6. <span data-ttu-id="22eeb-140">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="22eeb-140">Click **OK**.</span></span>
7. <span data-ttu-id="22eeb-141">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="22eeb-141">Close the page.</span></span>

## <a name="post-the-interest-note"></a><span data-ttu-id="22eeb-142">Die Zinsrechnung buchen</span><span class="sxs-lookup"><span data-stu-id="22eeb-142">Post the interest note</span></span>
1. <span data-ttu-id="22eeb-143">Wählen Sie eine Zinsrechnung aus, die zum Buchen bereit ist (Status wird erstellt).</span><span class="sxs-lookup"><span data-stu-id="22eeb-143">Select an interest note that is ready to post (status is created).</span></span>
2. <span data-ttu-id="22eeb-144">Klicken Sie auf **Buchen**.</span><span class="sxs-lookup"><span data-stu-id="22eeb-144">Click **Post**.</span></span>
3. <span data-ttu-id="22eeb-145">Geben Sie das Buchungsdatum für die Zinsrechnung ein.</span><span class="sxs-lookup"><span data-stu-id="22eeb-145">Enter the posting date for the interest note.</span></span> <span data-ttu-id="22eeb-146">Wählen Sie "Ja" aus, um eine Hauptbuchtransaktion für jede Zinsrechnung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="22eeb-146">Select Yes to create a general ledger transaction for each interest note.</span></span> <span data-ttu-id="22eeb-147">Wenn Sie nicht "Ja" auswählen, werden die Zinsen für alle Zinsrechnungen für den Debitor kumuliert und in einer einzigen Transaktion im Hauptbuch gebucht.</span><span class="sxs-lookup"><span data-stu-id="22eeb-147">If you do not select Yes, the interest on all interest notes to the customer is accumulated and posted to the general ledger in one transaction.</span></span>  
4. <span data-ttu-id="22eeb-148">Erweitern Sie die **Datensätze um** fastTab.</span><span class="sxs-lookup"><span data-stu-id="22eeb-148">Expand the **Records to include** fastTab.</span></span>
5. <span data-ttu-id="22eeb-149">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="22eeb-149">Click **OK**.</span></span>
6. <span data-ttu-id="22eeb-150">Wählen Sie im Feld **Status** die Option 'Gebucht'.</span><span class="sxs-lookup"><span data-stu-id="22eeb-150">In the **Status** field, select 'Posted'.</span></span>

