---
title: Fragebögen verteilen und planen
description: In diesem Artikel wird beschrieben, wie Sie die Fragebögen verteilen die Sie entworfen haben, sodass sie für die Person oder Gruppe von Personen verfügbar sind, die sie beantworten sollen.
author: andreabichsel
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: KMConnectionType, KMKnowledgeCollectorPlanningTabel, SysEmailParameters
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 17424
ms.assetid: fd8d867a-2446-400a-b91f-ad4085427470
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 37c9392263e8c113c541b64e8e79853520a13d11
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/19/2019
ms.locfileid: "857960"
---
# <a name="distribute-and-schedule-questionnaires"></a><span data-ttu-id="edb4f-103">Fragebögen verteilen und planen</span><span class="sxs-lookup"><span data-stu-id="edb4f-103">Distribute and schedule questionnaires</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="edb4f-104">In diesem Artikel wird beschrieben, wie Sie die Fragebögen verteilen die Sie entworfen haben, sodass sie für die Person oder Gruppe von Personen verfügbar sind, die sie beantworten sollen.</span><span class="sxs-lookup"><span data-stu-id="edb4f-104">This topic explains how distribute the questionnaires that you design, so that they are available to the person or group of people who will complete them.</span></span> 

<span data-ttu-id="edb4f-105">Es gibt mehrere Möglichkeiten, einen Fragebogen zu verteilen:</span><span class="sxs-lookup"><span data-stu-id="edb4f-105">There are multiple ways to distribute a questionnaire:</span></span>

-   <span data-ttu-id="edb4f-106">Markieren Sie den Fragebogen als aktiv.</span><span class="sxs-lookup"><span data-stu-id="edb4f-106">Mark the questionnaire as active.</span></span> <span data-ttu-id="edb4f-107">Der Fragebogen ist für alle Mitarbeiter verfügbar, sofern keine Fragebogengruppe eingerichtet wird, um den Zugriff auf den Fragebogen zu beschränken.</span><span class="sxs-lookup"><span data-stu-id="edb4f-107">The questionnaire is then available to all employees, unless a questionnaire group is set up to restrict access to it.</span></span>
-   <span data-ttu-id="edb4f-108">Zuweisen von Rechten zu einer Fragebogengruppe.</span><span class="sxs-lookup"><span data-stu-id="edb4f-108">Assign rights to a questionnaire group.</span></span> <span data-ttu-id="edb4f-109">Der Fragebogen ist dann für alle Mitglieder der ausgewählten Gruppe verfügbar.</span><span class="sxs-lookup"><span data-stu-id="edb4f-109">The questionnaire is then available to all members of the selected group.</span></span>
-   <span data-ttu-id="edb4f-110">Erstellen von geplanten Antwortsitzungen.</span><span class="sxs-lookup"><span data-stu-id="edb4f-110">Create planned answer sessions.</span></span> <span data-ttu-id="edb4f-111">Der Fragebogen steht dann für eine bestimmte Person zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="edb4f-111">The questionnaire is then available only to a particular person.</span></span>
-   <span data-ttu-id="edb4f-112">Zeitplan erstellen.</span><span class="sxs-lookup"><span data-stu-id="edb4f-112">Create a schedule.</span></span> <span data-ttu-id="edb4f-113">Der Fragebogen kann dann für mehrere Personen verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="edb4f-113">The questionnaire can then be available to multiple people.</span></span>

## <a name="marking-a-questionnaire-as-active"></a><span data-ttu-id="edb4f-114">Markieren eines Fragebogens als aktiv</span><span class="sxs-lookup"><span data-stu-id="edb4f-114">Marking a questionnaire as active</span></span>
<span data-ttu-id="edb4f-115">Setzen Sie das Feld **Aktiv** auf **Ja** auf der Seite **Fragebögen**. Sie geben den Fragebogen für alle Mitarbeiter zur Beantwortung frei.</span><span class="sxs-lookup"><span data-stu-id="edb4f-115">By setting the **Active** field to **Yes** on the **Questionnaires** page, you make the questionnaire available for all employees to complete.</span></span> <span data-ttu-id="edb4f-116">Die Befragungsteilnehmer können den Fragebogen mehrmals ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="edb4f-116">Respondents can complete the questionnaire multiple times.</span></span> <span data-ttu-id="edb4f-117">Diese Funktionalität ist hilfreich, wenn ständige Rückmeldung für das ganze Jahr gesammelt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="edb4f-117">This functionality is useful if you want to gather continual feedback throughout the year.</span></span> <span data-ttu-id="edb4f-118">So können Sie beispielsweise einen Fragebogen erstellten, über den die Mitarbeiter ein Feedback zum Mittagessen in der Cafeteria abgeben können.</span><span class="sxs-lookup"><span data-stu-id="edb4f-118">For example, you can make a questionnaire that employees use to give feedback about the lunch service in the cafeteria.</span></span>

## <a name="questionnaire-groups"></a><span data-ttu-id="edb4f-119">Fragebogengruppen</span><span class="sxs-lookup"><span data-stu-id="edb4f-119">Questionnaire groups</span></span>
<span data-ttu-id="edb4f-120">Sie können Fragebogengruppen einrichten und die Befragten einbeziehen, für die ein Fragebogen verteilt werden soll.</span><span class="sxs-lookup"><span data-stu-id="edb4f-120">You can set up questionnaire groups and then include the respondents that a questionnaire should be distributed to.</span></span> 

<span data-ttu-id="edb4f-121">Sie können Fragebogengruppen von den folgenden Seiten erstellen:</span><span class="sxs-lookup"><span data-stu-id="edb4f-121">You can create questionnaire groups from the following pages:</span></span>

-   <span data-ttu-id="edb4f-122">**Fragebogengruppen** – Nur Personen innerhalb einer Fragebogengruppe können einen ausgewählten Fragebogen ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="edb4f-122">**Questionnaire groups** – Only individuals in a questionnaire group can complete a selected questionnaire.</span></span> <span data-ttu-id="edb4f-123">Wenn beispielsweise die gewünschte Zielgruppe "Auftragnehmer" ist, können Sie eine Fragebogengruppe erstellen, die für diese Teilnehmer spezifisch ist.</span><span class="sxs-lookup"><span data-stu-id="edb4f-123">For example, your intended audience is contractors, so you create a questionnaire group that is specific to those respondents.</span></span>
-   <span data-ttu-id="edb4f-124">**Fragebogengruppenmitglieder** – Mithilfe dieses Formulars können Sie Personen zu Fragebogengruppen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="edb4f-124">**Questionnaire group members** – You can add people to the questionnaire groups.</span></span>

<span data-ttu-id="edb4f-125">Um eine Fragebogengruppe einem Fragebogen zuzuweisen, klicken Sie auf der Seite **Fragebögen** auf **Benutzerrechte**.</span><span class="sxs-lookup"><span data-stu-id="edb4f-125">To assign a questionnaire group to a questionnaire, on the **Questionnaires** page, click **User rights**.</span></span> <span data-ttu-id="edb4f-126">Nachdem der Fragebogen als aktiv gespeichert ist, können die Mitglieder der Fragebogengruppe den Fragebogen ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="edb4f-126">After the questionnaire is saved as active, the members of the questionnaire group can complete the questionnaire.</span></span> <span data-ttu-id="edb4f-127">Diese Funktion ist hilfreich, wenn Sie einen Fragebogen mit einer Auswählensgruppe von Personen testen möchten, bevor Sie diese in einer größeren Gruppe verteilen, oder wenn Sie den Fragebogen einer Zielgruppe zukommen lassen wollen.</span><span class="sxs-lookup"><span data-stu-id="edb4f-127">This functionality is helpful if you want to test a questionnaire on a select group of people before you roll it out to a larger group, or if you want to target a questionnaire to a very specific audience.</span></span>

## <a name="planned-answer-sessions-in-a-questionnaire"></a><span data-ttu-id="edb4f-128">Geplante Beantwortungssitzung in einem Fragebogen</span><span class="sxs-lookup"><span data-stu-id="edb4f-128">Planned answer sessions in a questionnaire</span></span>
<span data-ttu-id="edb4f-129">Geplante Antwortsitzungen sind Fragebogen, die Sie entwickelt und für die Sie die Befragten ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="edb4f-129">Planned answer sessions are questionnaires that you've designed and selected the respondents for.</span></span> 

> <span data-ttu-id="edb4f-130">**Hinweis** Bevor Sie geplante Antwortsitzungen einrichten können, müssen Sie einen Fragebogen entwerfen.</span><span class="sxs-lookup"><span data-stu-id="edb4f-130">**Note** Before you can set up planned answer sessions, you must design a questionnaire.</span></span> 

<span data-ttu-id="edb4f-131">Auf der Seite **Geplante Antwortsitzung** können Sie eine geplante Antwortsitzung für einen einzelnen Mitarbeiter erstellen.</span><span class="sxs-lookup"><span data-stu-id="edb4f-131">On the **Planned answer session** page, you can create a planned answer session for an individual employee.</span></span> <span data-ttu-id="edb4f-132">In der Liste auf der Seite werden alle geplanten Fragebögen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="edb4f-132">The list on the page displays all planned questionnaires.</span></span> 

<span data-ttu-id="edb4f-133">Geplante Antwortsitzungen werden auch auf der Seite **Zeitpläne für Fragebögen** verwendet, in dem Sie Fragebögen für mehrere Personen planen können:</span><span class="sxs-lookup"><span data-stu-id="edb4f-133">Planned answer sessions are also used on the **Questionnaire schedules** page, where you can plan questionnaires for multiple people:</span></span>

-   <span data-ttu-id="edb4f-134">Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="edb4f-134">Employees</span></span>
-   <span data-ttu-id="edb4f-135">Kursteilnehmer</span><span class="sxs-lookup"><span data-stu-id="edb4f-135">Course participants</span></span>
-   <span data-ttu-id="edb4f-136">Organisationseinheiten</span><span class="sxs-lookup"><span data-stu-id="edb4f-136">Organizational units</span></span>

<span data-ttu-id="edb4f-137">Jede Person kann den Fragebogen nur einmal beantworten.</span><span class="sxs-lookup"><span data-stu-id="edb4f-137">Each person can answer the questionnaire only one time.</span></span>

## <a name="scheduling-a-questionnaire"></a><span data-ttu-id="edb4f-138">Planung eines Fragebogens</span><span class="sxs-lookup"><span data-stu-id="edb4f-138">Scheduling a questionnaire</span></span>
<span data-ttu-id="edb4f-139">Sie können einen Fragebogen optional für mehrere Befragungsteilnehmer planen.</span><span class="sxs-lookup"><span data-stu-id="edb4f-139">You can optionally schedule a questionnaire for multiple respondents.</span></span>

### <a name="planning-types"></a><span data-ttu-id="edb4f-140">Planungstypen</span><span class="sxs-lookup"><span data-stu-id="edb4f-140">Planning types</span></span>

<span data-ttu-id="edb4f-141">Planungstypen werden benötigt, wenn Sie geplante Antwortsitzungen für mehrere Befragungsteilnehmer planen möchten.</span><span class="sxs-lookup"><span data-stu-id="edb4f-141">Planning types are required if you want to schedule planned answer sessions for multiple respondents.</span></span> <span data-ttu-id="edb4f-142">Planungstypen werden verwendet, um Fragebogenzeitpläne zu klassifizieren.</span><span class="sxs-lookup"><span data-stu-id="edb4f-142">Planning types are used to classify questionnaire schedules.</span></span> <span data-ttu-id="edb4f-143">Beispielsweise können Sie Fragebögen für folgende Zwecke planen:</span><span class="sxs-lookup"><span data-stu-id="edb4f-143">For example, you can schedule questionnaires for the following purposes:</span></span>

-   <span data-ttu-id="edb4f-144">Beurteilung</span><span class="sxs-lookup"><span data-stu-id="edb4f-144">Evaluation</span></span>
-   <span data-ttu-id="edb4f-145">Umfrage</span><span class="sxs-lookup"><span data-stu-id="edb4f-145">Survey</span></span>
-   <span data-ttu-id="edb4f-146">Testen</span><span class="sxs-lookup"><span data-stu-id="edb4f-146">Testing</span></span>

<span data-ttu-id="edb4f-147">Sie können Planungstypen für einen Fragebogenzeitplan auf der Seite **Zeitpläne für Fragebögen** angeben.</span><span class="sxs-lookup"><span data-stu-id="edb4f-147">You can specify planning types for a questionnaire schedule on the **Questionnaire schedules** page.</span></span>

### <a name="reference-types-for-questionnaire"></a><span data-ttu-id="edb4f-148">Referenztypen für Fragebögen</span><span class="sxs-lookup"><span data-stu-id="edb4f-148">Reference types for questionnaire</span></span>

<span data-ttu-id="edb4f-149">Sie können Referenztypen verwenden, um Kriterien für die Auswahl von Befragungsteilnehmern einzugeben, wenn Sie einen Fragebogen terminieren.</span><span class="sxs-lookup"><span data-stu-id="edb4f-149">You can use reference types to enter criteria for the respondents that you might select when you schedule a questionnaire.</span></span> 

<span data-ttu-id="edb4f-150">Verwenden Sie die **Referenztypen**-Seite, um Referenztypen für einen Fragebogen einzurichten.</span><span class="sxs-lookup"><span data-stu-id="edb4f-150">Use the **Reference types** page to set up reference types for a questionnaire.</span></span> <span data-ttu-id="edb4f-151">Jeder Referenztyp entspricht einer Tabelle in Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="edb4f-151">Each reference type corresponds to a table in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="edb4f-152">Wenn Sie Zeitpläne für Fragebögen erstellen, können Sie einzelne Datensätze in der Tabelle oder einen Datensatzbereich angeben, denen bzw. dem der Fragebogen zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="edb4f-152">When you create questionnaire schedules, you can specify individual records in the table or a range of records that the questionnaire will be associated with.</span></span> 

<span data-ttu-id="edb4f-153">Wenn Sie beispielsweise die Tabelle Kurse auswählen, können Sie entscheiden, für welchen Kurs der Fragebogen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="edb4f-153">For example, if you select the Courses table, you can decide which specific course the questionnaire will be for.</span></span> <span data-ttu-id="edb4f-154">Wenn Sie einen Referenztyp für die Kurstabelle einrichten, sind einige Felder und Schaltflächen auf der Seite **Kurse** verfügbar.</span><span class="sxs-lookup"><span data-stu-id="edb4f-154">When you set up a reference for the Courses table, some fields and buttons on the **Courses** page become available.</span></span>

### <a name="questionnaire-schedules"></a><span data-ttu-id="edb4f-155">Zeitpläne für Fragebögen</span><span class="sxs-lookup"><span data-stu-id="edb4f-155">Questionnaire schedules</span></span>

<span data-ttu-id="edb4f-156">Sie können Fragebogenzeitpläne verwenden, um mehrere geplante Antwortsitzungen für eine Benutzergruppe auf Grundlage eines Referenztyps zu generieren.</span><span class="sxs-lookup"><span data-stu-id="edb4f-156">You can use questionnaire schedules to generate multiple planned answer sessions for a group of users, based on a reference type.</span></span> <span data-ttu-id="edb4f-157">Dient zum Erstellen eines Zeitplans für die Seite **Fragebogenzeitpläne**.</span><span class="sxs-lookup"><span data-stu-id="edb4f-157">Create a schedule on the **Questionnaire schedules** page.</span></span> <span data-ttu-id="edb4f-158">Wählen Sie den Planungstyp aus, um den Zeitplan zu Kategorisieren, und wählen Sie auch den Referenztyp aus, der verwendet werden soll, um das System für bestimmte Benutzer abzufragen.</span><span class="sxs-lookup"><span data-stu-id="edb4f-158">Select the planning type to categorize the schedule, and also select the reference type that should be used to query the system for specific users.</span></span> <span data-ttu-id="edb4f-159">Wenn Sie zum Beispiel den Referenztyp auf die Kursetabelle festlegen, können Sie einen bestimmten Kurs im Feld **Referenz** auswählen.</span><span class="sxs-lookup"><span data-stu-id="edb4f-159">For example, if you set the reference type to the Courses table, you can select a specific course in the **Reference** field.</span></span> 

<span data-ttu-id="edb4f-160">Klicken Sie auf **Einstellungsdetails**, um den Fragebogen und andere Kriterien auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="edb4f-160">Click **Setup details** to select the questionnaire and other criteria.</span></span> <span data-ttu-id="edb4f-161">Geben Sie beispielsweise den Namen des Kursleiters als Kriterium an, nachdem der Fragebogen eine Bewertung des Kursleiters ist.</span><span class="sxs-lookup"><span data-stu-id="edb4f-161">For example, specify the instructor's name as a criterion if the questionnaire is an evaluation of the instructor.</span></span> <span data-ttu-id="edb4f-162">Nachdem Sie abgeschlossen und die Einrichtungsdetails eingeben haben, generiert das System geplante Antwortsitzungen für die Benutzer, die in der Abfrage enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="edb4f-162">After you've finished entering the setup details, the system generates planned answer sessions for the users that are included in the query.</span></span> 

<span data-ttu-id="edb4f-163">Klicken Sie auf **Geplante Antwortsitzungen**, um die Antwortsitzungen für den Zeitplan anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="edb4f-163">Click **Planned answer sessions** to view the answer sessions for the schedule.</span></span> <span data-ttu-id="edb4f-164">Sie können dann manuell zusätzliche geplante Antwortsitzungen erstellen oder geplante Antwortsitzungen die nicht beantwortet wurden löschen.</span><span class="sxs-lookup"><span data-stu-id="edb4f-164">You can then manually create additional planned answer sessions or delete planned answer sessions that haven't been answered.</span></span> 

<span data-ttu-id="edb4f-165">Klicken Sie auf **Funktionen** &gt; **Starten**, um den Fragebogen für die Benutzer in den zugehörigen geplanten Antwortsitzungen verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="edb4f-165">Click **Functions** &gt; **Start** to make the questionnaire available to the users in related planned answer sessions.</span></span> <span data-ttu-id="edb4f-166">Klicken Sie auf **Antworten**, um die abgeschlossenen Antworten für den Fragebogen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="edb4f-166">Click **Answers** to view the completed responses to the questionnaire.</span></span> <span data-ttu-id="edb4f-167">Sie können die Fragebogenzeitplaneinstellungen, geplante Antwortsitzungen und Antworten in einen neuen Fragebogenzeitplan kopieren.</span><span class="sxs-lookup"><span data-stu-id="edb4f-167">You can optionally copy the questionnaire schedule settings, planned answer sessions, and answers to a new questionnaire schedule.</span></span>

## <a name="notifying-respondents-about-questionnaires-that-are-available-to-them"></a><span data-ttu-id="edb4f-168">Benachrichtigen von Befragungsteilnehmern zu den verfügbaren Fragebögen</span><span class="sxs-lookup"><span data-stu-id="edb4f-168">Notifying respondents about questionnaires that are available to them</span></span>
<span data-ttu-id="edb4f-169">Wenn Sie einen Fragebogen verteilen, müssen Sie die Teilnehmer informieren, dass Fragebögen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="edb4f-169">When you distribute a questionnaire, you must notify respondents that questionnaires are available to them.</span></span> 

### <a name="notifying-respondents-about-a-planned-answer-session"></a><span data-ttu-id="edb4f-170">Benachrichtigen von Befragungsteilnehmern zu einer geplanten Beantwortungssitzung</span><span class="sxs-lookup"><span data-stu-id="edb4f-170">Notifying respondents about a planned answer session</span></span>

<span data-ttu-id="edb4f-171">Wenn Sie eine geplante Antwortsitzung verwenden, müssen Sie die Person z. B. telefonisch oder per E-Mail-Nachricht direkt informieren.</span><span class="sxs-lookup"><span data-stu-id="edb4f-171">If you use a planned answer session, you must notify the person directly, such as by telephone or email.</span></span>

### <a name="notifying-respondents-about-a-scheduling"></a><span data-ttu-id="edb4f-172">Benachrichtigen von Befragungsteilnehmern zu einer Planung</span><span class="sxs-lookup"><span data-stu-id="edb4f-172">Notifying respondents about a scheduling</span></span>

<span data-ttu-id="edb4f-173">Verwenden Sie die Seite **Zeitpläne für Fragebögen**, um eine E-Mail-Nachricht an alle Teilnehmer, die dem Fragebogen zugeordnet sind, zu erstellen und zu senden.</span><span class="sxs-lookup"><span data-stu-id="edb4f-173">Use the **Questionnaire schedules** page to prepare and send email to all respondents who are assigned to the questionnaire.</span></span> <span data-ttu-id="edb4f-174">Geben Sie den Text der E-Mail auf der Registerkarte **E-Mail für Mitarbeiter-Self-Service** ein. Nachdem der Plan gestartet wurde, klicken Sie **Funktionen** &gt; **E-Mail senden**, um die E-Mail den Befragungsteilnehmern zu generieren und zu senden.</span><span class="sxs-lookup"><span data-stu-id="edb4f-174">Enter the email text on the **E-mail for employee self service** tab. After the schedule has been started, click **Functions** &gt; **Send e-mail** to generate and send the email to the respondents.</span></span> <span data-ttu-id="edb4f-175">Die Befragungsteilnehmer können sich nun auf der Website anmelden und den Fragebogen ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="edb4f-175">Respondents can then sign in to the website and complete the questionnaire.</span></span> 

> <span data-ttu-id="edb4f-176">**Hinweis** Bevor Sie die E-Mail-Funktion verwenden können, muss Ihr IT-Administrator auf der Seite **E-Mail-Parameter** die E-Mail-Einstellungen eintragen.</span><span class="sxs-lookup"><span data-stu-id="edb4f-176">**Note** Before you can use the email functionality, your IT administrator must enter the email settings on the **E-mail parameters** page.</span></span>

## <a name="ending-a-scheduled-questionnaire"></a><span data-ttu-id="edb4f-177">Beenden eines geplanten Fragebogens</span><span class="sxs-lookup"><span data-stu-id="edb4f-177">Ending a scheduled questionnaire</span></span>
<span data-ttu-id="edb4f-178">Sie können einen geplanten Fragebogen beenden, nachdem alle Befragungsteilnehmer ihre zugewiesenen Antwortsitzungen abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="edb4f-178">You can end a scheduled questionnaire after all respondents have completed their assigned answer sessions.</span></span> <span data-ttu-id="edb4f-179">Nachdem ein geplanter Fragebogen beendet ist, können Sie seine Einstellungen nicht in eine neue Planung kopieren.</span><span class="sxs-lookup"><span data-stu-id="edb4f-179">After a scheduled questionnaire is ended, you can't copy its settings to a new schedule.</span></span> 

> <span data-ttu-id="edb4f-180">**Hinweis** Wenn ein oder mehrere Befragungsteilnehmer den Fragebogen nicht ausgefüllt haben, Sie aber die Planung beenden wollen, müssen Sie zuerst diese Befragungsteilnehmer aus der Liste auf der Seite **Geplante Antwortsitzung** löschen.</span><span class="sxs-lookup"><span data-stu-id="edb4f-180">**Note** If one or more respondents haven't completed the questionnaire, but you still want to end the scheduling, you must first delete those respondents from the list on the **Planned answer session** page.</span></span> <span data-ttu-id="edb4f-181">Dann können Sie die Planung beenden.</span><span class="sxs-lookup"><span data-stu-id="edb4f-181">You can then end the schedule.</span></span>

## <a name="completing-questionnaires"></a><span data-ttu-id="edb4f-182">Ausfüllen von Fragebögen</span><span class="sxs-lookup"><span data-stu-id="edb4f-182">Completing questionnaires</span></span>
<span data-ttu-id="edb4f-183">Nachdem Sie einen Fragebogen entworfen und verteilt haben, kann der Fragebogen von ausgewählten Befragten ausgefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="edb4f-183">After you've designed and distributed a questionnaire, the questionnaire can be completed by selected respondents.</span></span> <span data-ttu-id="edb4f-184">Die verfügbaren Fragebögen können von zwei Orten aus aufgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="edb4f-184">You can complete the questionnaires that are available to you from two locations:</span></span>

-   <span data-ttu-id="edb4f-185">Im Navigationsbereich Klicken Sie auf **Fragebögen** &gt; **Verteilen** &gt; **Fragebogen ausfüllen**.</span><span class="sxs-lookup"><span data-stu-id="edb4f-185">In the navigation pane, click **Questionnaires** &gt; **Distribute** &gt; **Complete a questionnaire**.</span></span>
-   <span data-ttu-id="edb4f-186">Im "Mitarbeiter-Self-Service" klicken Sie auf **Auszufüllende Fragebögen**.</span><span class="sxs-lookup"><span data-stu-id="edb4f-186">In Employee self-service, click **Questionnaires to complete**.</span></span>

<span data-ttu-id="edb4f-187">Fragebögen können entweder allen Personen im Netzwerk oder lediglich bestimmten Benutzern oder Benutzergruppen zur Verfügung gestellt werden.</span><span class="sxs-lookup"><span data-stu-id="edb4f-187">Questionnaires can made be available to specific users or groups of users, or to all users in a network.</span></span>

<a name="additional-resources"></a><span data-ttu-id="edb4f-188">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="edb4f-188">Additional resources</span></span>
--------

[<span data-ttu-id="edb4f-189">Entwurf von Fragebögen</span><span class="sxs-lookup"><span data-stu-id="edb4f-189">Designing questionnaires</span></span>](design-questionnaires.md)

[<span data-ttu-id="edb4f-190">Verwenden von Fragebögen</span><span class="sxs-lookup"><span data-stu-id="edb4f-190">Using questionnaires</span></span>](questionnaires.md)

[<span data-ttu-id="edb4f-191">Anzeigen und Auswerten der Ergebnisse eines Fragebogens</span><span class="sxs-lookup"><span data-stu-id="edb4f-191">Viewing and evaluating the results of questionnaires</span></span>](evaluate-questionnaire-results.md)


