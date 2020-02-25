---
title: Ergebnisse des Fragebogens analysieren
description: Die Fragebogenstatistiken können verwendet werden, um Durchschnitte, Summen und Prozentsätze basierend auf einer Gruppe von demografischen Daten zu berechnen.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMQuestionnaireStatistics, KMQuestionnaireStatisticsLine
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9d3b13ef7eda9943af35bbb37e3059dd81aa6365
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009192"
---
# <a name="analyzing-questionnaire-results"></a><span data-ttu-id="30ae5-103">Ergebnisse des Fragebogens analysieren</span><span class="sxs-lookup"><span data-stu-id="30ae5-103">Analyzing questionnaire results</span></span>



<span data-ttu-id="30ae5-104">Die Fragebogenstatistiken können verwendet werden, um Durchschnitte, Summen und Prozentsätze basierend auf einer Gruppe von demografischen Daten zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="30ae5-104">Questionnaire statistics can be used to calculate averages, totals, and percentages based on a set of demographic data.</span></span> <span data-ttu-id="30ae5-105">Um diese Prozedur zu starten, gehen Sie zu "Fragebogen" > "Ergebnisse anzeigen und analysieren" > "Fragebogenstatistik".</span><span class="sxs-lookup"><span data-stu-id="30ae5-105">To begin this procedure, go to Questionnaire > View and analyze results > Questionnaire statistics.</span></span> <span data-ttu-id="30ae5-106">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="30ae5-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-questionnaire-statistics-record"></a><span data-ttu-id="30ae5-107">Fragebogenstatistik-Datensatz erstellen</span><span class="sxs-lookup"><span data-stu-id="30ae5-107">Create a Questionnaire statistics record</span></span>
1. <span data-ttu-id="30ae5-108">Wechseln Sie zu "Fragebogenstatistik".</span><span class="sxs-lookup"><span data-stu-id="30ae5-108">Go to Questionnaire statistics.</span></span>
2. <span data-ttu-id="30ae5-109">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="30ae5-109">Click New.</span></span>
3. <span data-ttu-id="30ae5-110">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="30ae5-110">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="30ae5-111">Geben Sie im Feld "Statistik" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="30ae5-111">In the Statistics field, type a value.</span></span>
5. <span data-ttu-id="30ae5-112">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="30ae5-112">In the Description field, type a value.</span></span>
6. <span data-ttu-id="30ae5-113">Klicken Sie im Feld "Fragebogen" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="30ae5-113">In the Questionnaire field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="30ae5-114">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="30ae5-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="30ae5-115">Klicken Sie auf die Registerkarte "Allgemein".</span><span class="sxs-lookup"><span data-stu-id="30ae5-115">Click the General tab.</span></span>
    * <span data-ttu-id="30ae5-116">Wählen Sie, ob anonyme Ergebnisse oder Ergebnisse von Arbeitskräften, von Kontakten und Bewerbern einbezogen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="30ae5-116">Select if you want to include anonymous results or results from workers, contacts, and applicants.</span></span>  
9. <span data-ttu-id="30ae5-117">Aktivieren bzw. deaktivieren Sie das Kontrollkästchen "Arbeitskraft".</span><span class="sxs-lookup"><span data-stu-id="30ae5-117">Select or clear the Worker check box.</span></span>
    * <span data-ttu-id="30ae5-118">Wenn Sie die Ergebnisse nach Dienstalter oder Alter anzeigen, geben Sie die Intervalle an, die Sie zum Gruppieren der Ergebnisse verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="30ae5-118">If you will be viewing the results by seniority or age, specify the intervals that you would like to use for grouping the results.</span></span>  
    * <span data-ttu-id="30ae5-119">Der Wert 5 für das Altersintervall gruppiert die Ergebnisse auf Grundlage von Fünfjahresintervallen.</span><span class="sxs-lookup"><span data-stu-id="30ae5-119">Entering a 5 for the age interval will group the results based on five-year age intervals.</span></span>  
10. <span data-ttu-id="30ae5-120">Geben Sie im Feld "Alter" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="30ae5-120">In the Age field, enter a number.</span></span>
    * <span data-ttu-id="30ae5-121">Aktivieren Sie diese Option, wenn die Berechnung gegen den gesamten Fragebogen, für jede Ergebnisgruppe, für jede Frage oder für jede Fragenzeile ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="30ae5-121">Select if you want to run the calculation against the entire questionnaire, for each result group, for each question, or for each question row.</span></span>  
    * <span data-ttu-id="30ae5-122">Wählen Sie, wie die Ergebnisse gruppiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="30ae5-122">Select how you would like to group the results.</span></span>  
    * <span data-ttu-id="30ae5-123">Wenn Sie beispielsweise die durchschnittlichen Punkte pro Frage berechnen, möchten Sie, dass die Fragen nach Ergebnisgruppe gruppiert werden.</span><span class="sxs-lookup"><span data-stu-id="30ae5-123">For example, if you calculate the average points per question, you may want to see the questions grouped by Result group.</span></span>  
    * <span data-ttu-id="30ae5-124">Wählen Sie die Daten aus, auf denen die Berechnung basieren soll.</span><span class="sxs-lookup"><span data-stu-id="30ae5-124">Select the data to base the calculation on.</span></span>  
    * <span data-ttu-id="30ae5-125">Wenn Sie beispielsweise den durchschnittlichen Prozentsatz anzeigen möchten, der auf dem Fragebogen zu den Arbeitskräften für die durchschnittliche Anzahl der Punkte empfangen wird, die über den Arbeitskräften erreicht werden.</span><span class="sxs-lookup"><span data-stu-id="30ae5-125">For example, if you want to see the average percent received on the questionnaire across your workers versus the average number of points achieved across your workers.</span></span>  
11. <span data-ttu-id="30ae5-126">Klicken Sie auf die Registerkarte "Bereich".</span><span class="sxs-lookup"><span data-stu-id="30ae5-126">Click the Range tab.</span></span>
    * <span data-ttu-id="30ae5-127">Verwenden Sie Bereiche, um die Ergebnismenge auf die Bereichskriterien einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="30ae5-127">Use ranges to limit your result set to only those meeting the Range criteria.</span></span>  
12. <span data-ttu-id="30ae5-128">Klicken Sie auf die Registerkarte "Gruppieren nach".</span><span class="sxs-lookup"><span data-stu-id="30ae5-128">Click the Grouping by tab.</span></span>
    * <span data-ttu-id="30ae5-129">Verwenden Sie Gruppierungen, um zu bestimmen, wie die Ergebnisse angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="30ae5-129">Use Groupings to determine how the results should be displayed.</span></span>  
    * <span data-ttu-id="30ae5-130">Gruppieren Sie z. B. die Ergebnisse zunächst nach Geschlecht und dann nach Alter.</span><span class="sxs-lookup"><span data-stu-id="30ae5-130">For example, group the results first by gender, then by age.</span></span>  
13. <span data-ttu-id="30ae5-131">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="30ae5-131">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="30ae5-132">Verschieben Sie die Gruppierungen auf die Seite "Ausgewählt" und platzieren Sie sie im gewünschten Auftrag.</span><span class="sxs-lookup"><span data-stu-id="30ae5-132">Move the groupings into the Selected side and place them in the desired order.</span></span>  

## <a name="execute-the-statistics-calculation"></a><span data-ttu-id="30ae5-133">Statistikberechnung ausführen</span><span class="sxs-lookup"><span data-stu-id="30ae5-133">Execute the statistics calculation</span></span>
1. <span data-ttu-id="30ae5-134">Klicken Sie auf "Ausführen".</span><span class="sxs-lookup"><span data-stu-id="30ae5-134">Click Execute.</span></span>
    * <span data-ttu-id="30ae5-135">Wählen Sie aus, welche Berechnungsfunktion Sie für die Ergebnisse ausführen möchten.</span><span class="sxs-lookup"><span data-stu-id="30ae5-135">Select which calculation function you would like to perform on the results.</span></span>  
    * <span data-ttu-id="30ae5-136">Berechnen Sie z. B. die durchschnittlichen Prozentsätze zu dem Fragebogen für die ausgewählten Gruppierungen oder summieren Sie die Gesamtpunkte anhand der Ergebnisgruppen für die ausgewählten Gruppierungen.</span><span class="sxs-lookup"><span data-stu-id="30ae5-136">For example, calculate the average percentages across the questionnaire for the selected groupings or total the points across the result groups for the selected groupings.</span></span>  
2. <span data-ttu-id="30ae5-137">Aktivieren oder deaktivieren Sie das Kontrollkästchen "Frühere Suchen löschen".</span><span class="sxs-lookup"><span data-stu-id="30ae5-137">Select or clear the Delete previous searches check box.</span></span>
3. <span data-ttu-id="30ae5-138">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="30ae5-138">Click OK.</span></span>

## <a name="view-the-results-of-the-questionnaire-statistics-run"></a><span data-ttu-id="30ae5-139">Ergebnisse der Fragebogenstatistikausführung anzeigen</span><span class="sxs-lookup"><span data-stu-id="30ae5-139">View the results of the questionnaire statistics run.</span></span>
1. <span data-ttu-id="30ae5-140">Klicken Sie auf "Ergebnis".</span><span class="sxs-lookup"><span data-stu-id="30ae5-140">Click Result.</span></span>
2. <span data-ttu-id="30ae5-141">Klicken Sie auf "Ergebnis".</span><span class="sxs-lookup"><span data-stu-id="30ae5-141">Click Result.</span></span>
3. <span data-ttu-id="30ae5-142">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="30ae5-142">Close the page.</span></span>

