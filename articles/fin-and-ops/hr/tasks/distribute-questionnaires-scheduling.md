--- 
title: Einen Fragebogen mithilfe des Zeitplans verteilen
description: "Die Fragebogenplanung ermöglicht es Ihnen, Fragebögen für mehrere Befragungsteilnehmer zu planen und zu verteilen."
author: kherr75
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KMKnowledgeCollectorPlanningTable, KMKnowledgeCollectorPlanningMulti, SysQueryForm, HcmPersonLookup, KMKnowledgeCollectorPlanning
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: b66389a7d63c51f059a39495b8c7fbd325ef41e8
ms.contentlocale: de-de
ms.lasthandoff: 09/14/2018

---
# <a name="distribute-questionnaires-using-scheduling"></a><span data-ttu-id="99cfe-103">Einen Fragebogen mithilfe des Zeitplans verteilen</span><span class="sxs-lookup"><span data-stu-id="99cfe-103">Distribute questionnaires using scheduling</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="99cfe-104">Die Fragebogenplanung ermöglicht es Ihnen, Fragebögen für mehrere Befragungsteilnehmer zu planen und zu verteilen.</span><span class="sxs-lookup"><span data-stu-id="99cfe-104">Questionnaire scheduling allows you to plan and distribute questionnaires to multiple respondents.</span></span> <span data-ttu-id="99cfe-105">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="99cfe-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-questionnaire-schedule"></a><span data-ttu-id="99cfe-106">Erstellen eines Fragebogenzeitplans</span><span class="sxs-lookup"><span data-stu-id="99cfe-106">Create a questionnaire schedule</span></span>
1. <span data-ttu-id="99cfe-107">Gehen Sie zu "Fragebogen" > "Verteilen" > "Fragebogenzeitpläne".</span><span class="sxs-lookup"><span data-stu-id="99cfe-107">Go to Questionnaire > Distribute > Questionnaire schedules.</span></span>
2. <span data-ttu-id="99cfe-108">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="99cfe-108">Click New.</span></span>
3. <span data-ttu-id="99cfe-109">Geben Sie im Feld Zeitplan einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="99cfe-109">In the Scheduling field, type a value.</span></span>
4. <span data-ttu-id="99cfe-110">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="99cfe-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="99cfe-111">Legen Sie den Zeitplan auf anonymem fest, wenn die Antworten ohne die Namen erfasst werden sollen, die den Antworten zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="99cfe-111">Set the schedule to Anonymous if the responses should be recorded without names associated to the response.</span></span>  
    * <span data-ttu-id="99cfe-112">Das Zulassen von anonymen Ergebnissen muss zuerst über die Personalverwaltungsparameter eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="99cfe-112">Allowing anonymous results must be set up in the HR parameters first.</span></span>  
5. <span data-ttu-id="99cfe-113">Wählen Sie im Feld Typ den Zeitplantyp aus.</span><span class="sxs-lookup"><span data-stu-id="99cfe-113">In the Type field, select the planning type.</span></span>  <span data-ttu-id="99cfe-114">In diesem Beispiel nutzen wir den Zufriedenheits-Typ.</span><span class="sxs-lookup"><span data-stu-id="99cfe-114">In this example we will use the Satisfaction type.</span></span>
6. <span data-ttu-id="99cfe-115">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="99cfe-115">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="99cfe-116">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="99cfe-116">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="99cfe-117">Geben Sie ein Datum in das Feld "Datum" ein.</span><span class="sxs-lookup"><span data-stu-id="99cfe-117">In the Date field, enter a date.</span></span>
9. <span data-ttu-id="99cfe-118">Erweitern oder reduzieren Sie den Abschnitt "E-Mail für Mitarbeiter-Self-Service".</span><span class="sxs-lookup"><span data-stu-id="99cfe-118">Expand the Email for employee self service section.</span></span>
10. <span data-ttu-id="99cfe-119">Geben Sie im Feld "Betreff" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="99cfe-119">In the Subject field, type a value.</span></span>
    * <span data-ttu-id="99cfe-120">Beispiel: Fragebogen verfügbar</span><span class="sxs-lookup"><span data-stu-id="99cfe-120">Example: Questionnaire available</span></span>  
11. <span data-ttu-id="99cfe-121">Geben Sie im Textfeld den Textkörper der E-Mail ein.</span><span class="sxs-lookup"><span data-stu-id="99cfe-121">In the Text field, type the body of your email message.</span></span> <span data-ttu-id="99cfe-122">Beachten Sie, das die Variable nur zum Ersetzen von Werten im System verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="99cfe-122">Note, the variable can be used to substitue values in the system.</span></span>
    * <span data-ttu-id="99cfe-123">Beispiel:    Lieber %P%, melden Sie sich in Dynamics AX, Employee Self Service an, um den Belegschafts-Statusfragebogen auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="99cfe-123">Example:   Dear %P%,  Please log in to Employee Self Service to complete the Workforce Health questionnaire.</span></span>  <span data-ttu-id="99cfe-124">Contoso</span><span class="sxs-lookup"><span data-stu-id="99cfe-124">Contoso</span></span>  
12. <span data-ttu-id="99cfe-125">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="99cfe-125">Click Save.</span></span>

## <a name="use-the-setup-details-to-select-the-questionnaires-to-be-answered-as-well-as-any-queries-to-use-to-select-respondents"></a><span data-ttu-id="99cfe-126">Verwenden Sie die Einrichtungsdetails, um die zu beantwortenden Fragebögen sowie alle Abfragen für Auswahl der Antwortenden auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="99cfe-126">Use the Setup details to select the questionnaire(s) to be answered as well as any queries to use to select respondents.</span></span>
1. <span data-ttu-id="99cfe-127">Auf Einstellungsdetails klicken.</span><span class="sxs-lookup"><span data-stu-id="99cfe-127">Click Setup details.</span></span>
2. <span data-ttu-id="99cfe-128">Wählen Sie in der Liste eine Abfrage zur Suche im System für die Antwortenden für den Fragebogen aus.</span><span class="sxs-lookup"><span data-stu-id="99cfe-128">In the list, select a query to use to search the system for respondents for the questionnaire.</span></span>
    * <span data-ttu-id="99cfe-129">Beispiel: Arbeitskräfte</span><span class="sxs-lookup"><span data-stu-id="99cfe-129">Example: Workers</span></span>  
3. <span data-ttu-id="99cfe-130">Klicken Sie auf Anzeigen oder Ändern, um bestimmte Personen auszuwählen oder die Abfrage anzupassen, um Personen zu finden, die den Kriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="99cfe-130">Click View or modify query to select specific people or adjust the query to find people who match specific criteria.</span></span>
    * <span data-ttu-id="99cfe-131">Beachten Sie, dass alle Befragten auch Benutzer im System sein müssen.</span><span class="sxs-lookup"><span data-stu-id="99cfe-131">Note that all respondents must also be users in the system.</span></span>  
4. <span data-ttu-id="99cfe-132">Markieren Sie in der Liste die Zeile für "Person".</span><span class="sxs-lookup"><span data-stu-id="99cfe-132">In the list, mark the row for Person</span></span>
5. <span data-ttu-id="99cfe-133">Geben Sie im Feld "Kriterien" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="99cfe-133">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="99cfe-134">Wählen Sie "Julia Funderburk" aus.</span><span class="sxs-lookup"><span data-stu-id="99cfe-134">Select Julia Funderburk</span></span>  
6. <span data-ttu-id="99cfe-135">Wählen Sie in der Liste "Julia Funderburk".</span><span class="sxs-lookup"><span data-stu-id="99cfe-135">In the list, select Julia Funderburk</span></span>
7. <span data-ttu-id="99cfe-136">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="99cfe-136">Click OK.</span></span>
8. <span data-ttu-id="99cfe-137">Klicken Sie auf die Registerkarte "Fragebogen".</span><span class="sxs-lookup"><span data-stu-id="99cfe-137">Click the Questionnaires tab.</span></span>
9. <span data-ttu-id="99cfe-138">In der Struktur erweitern Sie den Knoten für den Fragebogentyp "Zufriedenheitsumfrage".</span><span class="sxs-lookup"><span data-stu-id="99cfe-138">In the tree, expand 'the node for the questionnaire type Satisfaction Survey'.</span></span>
10. <span data-ttu-id="99cfe-139">In der Struktur markieren Sie "Mitarbeiterstatusbewertung".</span><span class="sxs-lookup"><span data-stu-id="99cfe-139">In the tree, check 'Workforce Health Assessment'.</span></span>
11. <span data-ttu-id="99cfe-140">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="99cfe-140">Click OK.</span></span>
12. <span data-ttu-id="99cfe-141">Klicken Sie auf "Geplante Antwortsitzung".</span><span class="sxs-lookup"><span data-stu-id="99cfe-141">Click Planned answer session.</span></span>
    * <span data-ttu-id="99cfe-142">Beachten Sie, dass geplante Antwortsitzungen für jeden ausgewählten/abgefragten Benutzer erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="99cfe-142">Note that Planned answer sessions have been created for each selected/queried user.</span></span>  
13. <span data-ttu-id="99cfe-143">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="99cfe-143">Close the page.</span></span>

## <a name="start-the-questionnaire-schedule-in-order-to-make-the-questionnaire-available-for-respondents-to-complete"></a><span data-ttu-id="99cfe-144">Starten Sie den Fragebogenzeitplan, um den Fragebogen bereitzustellen, damit ihn die Befragten abschließen können.</span><span class="sxs-lookup"><span data-stu-id="99cfe-144">Start the questionnaire schedule in order to make the questionnaire available for respondents to complete.</span></span>
1. <span data-ttu-id="99cfe-145">Klicken Sie auf Funktionen.</span><span class="sxs-lookup"><span data-stu-id="99cfe-145">Click Functions.</span></span>
2. <span data-ttu-id="99cfe-146">Klicken Sie auf "Start".</span><span class="sxs-lookup"><span data-stu-id="99cfe-146">Click Start.</span></span>
3. <span data-ttu-id="99cfe-147">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="99cfe-147">Click OK.</span></span>

## <a name="send-the-email-to-inform-respondents-of-the-available-questionnaire"></a><span data-ttu-id="99cfe-148">Senden Sie die E-Mail, um Befragungsteilnehmer über den verfügbaren Fragebogen zu informieren.</span><span class="sxs-lookup"><span data-stu-id="99cfe-148">Send the email to inform respondents of the available questionnaire.</span></span>
1. <span data-ttu-id="99cfe-149">Klicken Sie auf Funktionen.</span><span class="sxs-lookup"><span data-stu-id="99cfe-149">Click Functions.</span></span>
2. <span data-ttu-id="99cfe-150">Klicken Sie auf "E-Mail senden".</span><span class="sxs-lookup"><span data-stu-id="99cfe-150">Click Send email.</span></span>
3. <span data-ttu-id="99cfe-151">Klicken Sie auf "Abbrechen".</span><span class="sxs-lookup"><span data-stu-id="99cfe-151">Click Cancel.</span></span>

## <a name="use-planned-answer-sessions-to-monitor-who-needs-to-complete-the-questionnaire"></a><span data-ttu-id="99cfe-152">Verwenden Sie geplante Antwortsitzungen, um zu überwachen, wer den Fragebogen ausfüllen muss.</span><span class="sxs-lookup"><span data-stu-id="99cfe-152">Use Planned answer sessions to monitor who needs to complete the questionnaire.</span></span>
1. <span data-ttu-id="99cfe-153">Klicken Sie auf "Geplante Antwortsitzung".</span><span class="sxs-lookup"><span data-stu-id="99cfe-153">Click Planned answer session.</span></span>
    * <span data-ttu-id="99cfe-154">Löschen Sie alle verbleibenden geplante Antwortsitzung, wenn Sie bereit sind, die geplante Sitzung zu beenden.</span><span class="sxs-lookup"><span data-stu-id="99cfe-154">Delete any remaining planned answer session when you're ready to end the scheduled session.</span></span>  
2. <span data-ttu-id="99cfe-155">Klicken Sie auf Löschen.</span><span class="sxs-lookup"><span data-stu-id="99cfe-155">Click Delete.</span></span>
3. <span data-ttu-id="99cfe-156">Klicken Sie auf "Ja".</span><span class="sxs-lookup"><span data-stu-id="99cfe-156">Click Yes.</span></span>
4. <span data-ttu-id="99cfe-157">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="99cfe-157">Close the page.</span></span>

## <a name="end-the-schedule-when-all-respondents-have-completed-the-questionnaire-andor-all-remaining-planned-answer-sessions-have-been-deleted"></a><span data-ttu-id="99cfe-158">Beenden Sie den Zeitplan, wenn alle Befragten den Fragebogen abgeschlossen haben und/oder alle restlichen geplanten Antwortsitzungen gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="99cfe-158">End the schedule when all respondents have completed the questionnaire and/or all remaining Planned answer sessions have been deleted.</span></span>
1. <span data-ttu-id="99cfe-159">Klicken Sie auf Funktionen.</span><span class="sxs-lookup"><span data-stu-id="99cfe-159">Click Functions.</span></span>
2. <span data-ttu-id="99cfe-160">Klicken Sie auf "Beenden".</span><span class="sxs-lookup"><span data-stu-id="99cfe-160">Click End.</span></span>
3. <span data-ttu-id="99cfe-161">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="99cfe-161">Click OK.</span></span>


