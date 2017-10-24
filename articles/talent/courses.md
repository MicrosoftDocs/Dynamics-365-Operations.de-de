---
title: Kursschulungen einrichten
description: "Personalverwaltungsadministratoren und ein Manager können die Kursfunktionen verwenden, um Informationen zur Schulung zu verwalten, welche für Arbeitskräfte angeboten wird."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 7532
ms.assetid: a6950c29-8b3e-45b2-9084-ddfb1317ffaa
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0ab79e85872c19e30f24e182ea483687ecc0bc09
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-training-courses"></a><span data-ttu-id="ee00c-103">Kursschulungen einrichten</span><span class="sxs-lookup"><span data-stu-id="ee00c-103">Set up training courses</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="ee00c-104">Personalverwaltungsadministratoren und ein Manager können die Kursfunktionen verwenden, um Informationen zur Schulung zu verwalten, welche für Arbeitskräfte angeboten wird.</span><span class="sxs-lookup"><span data-stu-id="ee00c-104">Human resources administrators and managers can use the courses features to maintain information about the training that's offered to workers.</span></span>

 <a name="set-up-prerequisites"></a><span data-ttu-id="ee00c-105">Einrichten von Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="ee00c-105">Set up prerequisites</span></span>
---------------------

<span data-ttu-id="ee00c-106">Die folgenden Informationen werden benötigt und müssen eingerichtet werden, bevor Sie Kurse erstellen.</span><span class="sxs-lookup"><span data-stu-id="ee00c-106">The following information is required and must be set up before you create courses.</span></span>
-   <span data-ttu-id="ee00c-107">**Kurstypen**</span><span class="sxs-lookup"><span data-stu-id="ee00c-107">**Course types**</span></span>

<span data-ttu-id="ee00c-108">Die folgenden Informationen sind optionale Informationen, die Sie für Kurse angeben können.</span><span class="sxs-lookup"><span data-stu-id="ee00c-108">The following information is optional information that you can specify for courses.</span></span> <span data-ttu-id="ee00c-109">Wenn Sie wissen, dass Sie diese Informationen für Kurse eingeben werden, sollten Sie dies tun, bevor Sie Kursdatensätze erstellen.</span><span class="sxs-lookup"><span data-stu-id="ee00c-109">If you know that you will be entering this information for courses, you should set up this information before you create course records.</span></span>
-   <span data-ttu-id="ee00c-110">**Kursraumgruppen**</span><span class="sxs-lookup"><span data-stu-id="ee00c-110">**Classroom groups**</span></span>
-   <span data-ttu-id="ee00c-111">**Kursgruppen**</span><span class="sxs-lookup"><span data-stu-id="ee00c-111">**Course groups**</span></span>
-   <span data-ttu-id="ee00c-112">**Kursorte**</span><span class="sxs-lookup"><span data-stu-id="ee00c-112">**Course locations**</span></span>
-   <span data-ttu-id="ee00c-113">**Kursräume**</span><span class="sxs-lookup"><span data-stu-id="ee00c-113">**Classrooms**</span></span>
-   <span data-ttu-id="ee00c-114">**Kursleiter**</span><span class="sxs-lookup"><span data-stu-id="ee00c-114">**Instructors**</span></span>

## <a name="course-types"></a><span data-ttu-id="ee00c-115">Kurstypen</span><span class="sxs-lookup"><span data-stu-id="ee00c-115">Course types</span></span>
<span data-ttu-id="ee00c-116">Kurstypen können verwendet werden, um Kurse entsprechend ihrer Struktur oder ihrem Inhalt zu kategorisieren.</span><span class="sxs-lookup"><span data-stu-id="ee00c-116">You can use course types to categorize courses according to the structure or content of the course.</span></span> <span data-ttu-id="ee00c-117">Sie können Kurstypen auf der Seite **Kurstypen** erstellen.</span><span class="sxs-lookup"><span data-stu-id="ee00c-117">You can create course types on the **Course types** page.</span></span> <span data-ttu-id="ee00c-118">Sie müssen einen Kurstyp auswählen, wenn einen Kursdatensatz erstellen.</span><span class="sxs-lookup"><span data-stu-id="ee00c-118">You must select a course type when you create a course record.</span></span>

## <a name="course-setup-type"></a><span data-ttu-id="ee00c-119">Kurseinstellungstyp</span><span class="sxs-lookup"><span data-stu-id="ee00c-119">Course setup type</span></span>
<span data-ttu-id="ee00c-120">In der folgenden Tabelle werden die drei Einstellungstypen für Kurse aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="ee00c-120">The following table lists the three setup types for courses.</span></span> <span data-ttu-id="ee00c-121">Einstellungstypen bestimmen die Struktur des Kurses.</span><span class="sxs-lookup"><span data-stu-id="ee00c-121">Setup types determine the structure of the course.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="ee00c-122">Einstellungstyp</span><span class="sxs-lookup"><span data-stu-id="ee00c-122">Setup type</span></span></th>
<th><span data-ttu-id="ee00c-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ee00c-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ee00c-124"><strong>Standard</strong></span><span class="sxs-lookup"><span data-stu-id="ee00c-124"><strong>Standard</strong></span></span></td>
<td><span data-ttu-id="ee00c-125">Wählen Sie diesen Typ für Kurse aus, die keinen täglichen Kursplan haben.</span><span class="sxs-lookup"><span data-stu-id="ee00c-125">Select this type for courses that will not have a daily agenda.</span></span> <span data-ttu-id="ee00c-126">Dies ist der Standardeinstellungstyp, wenn Sie einen neuen Kurs erstellen.</span><span class="sxs-lookup"><span data-stu-id="ee00c-126">This is the default setup type when you create a new course.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee00c-127"><strong>Agenda</strong></span><span class="sxs-lookup"><span data-stu-id="ee00c-127"><strong>Agenda</strong></span></span></td>
<td><span data-ttu-id="ee00c-128">Wählen Sie diese Typ aus, um die Details für jeden Tag eines Kurses zu planen, der an mehreren Tagen stattfindet.</span><span class="sxs-lookup"><span data-stu-id="ee00c-128">Select this type to plan the details of each day of a course that takes place over multiple days.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ee00c-129"><strong>Agenda und Sitzung</strong></span><span class="sxs-lookup"><span data-stu-id="ee00c-129"><strong>Agenda + session</strong></span></span></td>
<td><span data-ttu-id="ee00c-130">Wählen Sie diesen Typ für komplexere Kurse aus.</span><span class="sxs-lookup"><span data-stu-id="ee00c-130">Select this type for the more complex courses.</span></span> <span data-ttu-id="ee00c-131">Sie können etwa den Kursplan in Verläufe und Sitzungen unterteilen.</span><span class="sxs-lookup"><span data-stu-id="ee00c-131">For example, you can divide the agenda for the course into tracks and sessions.</span></span>
<ul>
<li><span data-ttu-id="ee00c-132"><strong>Verlauf</strong> - Verläufe sind bestimmte Fachgebiete für einen Kurs.</span><span class="sxs-lookup"><span data-stu-id="ee00c-132"><strong>Track</strong> – Tracks are specific subject areas for a course.</span></span></li>
<li><span data-ttu-id="ee00c-133"><strong>Sitzungen</strong> – Sitzungen unterteilen Verläufe und können bestimmte Prozesse oder Techniken abdecken, die für jeden Verlauf relevant sind.</span><span class="sxs-lookup"><span data-stu-id="ee00c-133"><strong>Sessions</strong> – Sessions divide up tracks and help identify specific processes or techniques that are relevant to the track.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="course-tasks"></a><span data-ttu-id="ee00c-134">Kursaufgaben</span><span class="sxs-lookup"><span data-stu-id="ee00c-134">Course tasks</span></span>
<span data-ttu-id="ee00c-135">Für jeden Kurs können die folgenden Aufgaben ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ee00c-135">For each course, you can complete the following tasks.</span></span>
-   <span data-ttu-id="ee00c-136">Registrieren von Teilnehmern</span><span class="sxs-lookup"><span data-stu-id="ee00c-136">Register participants</span></span>
-   <span data-ttu-id="ee00c-137">Angeben einer Registrierungsfrist</span><span class="sxs-lookup"><span data-stu-id="ee00c-137">Specify a registration deadline</span></span>
-   <span data-ttu-id="ee00c-138">Festlegen der minimalen und maximalen Teilnehmerzahl.</span><span class="sxs-lookup"><span data-stu-id="ee00c-138">Define the minimum and maximum number of participants</span></span>
-   <span data-ttu-id="ee00c-139">Zuweisen eines Kursorts und Kursraums</span><span class="sxs-lookup"><span data-stu-id="ee00c-139">Assign a course location and classroom</span></span>
-   <span data-ttu-id="ee00c-140">Empfehlen von Hotels für Kursteilnehmer</span><span class="sxs-lookup"><span data-stu-id="ee00c-140">Recommend hotels to course participants</span></span>
-   <span data-ttu-id="ee00c-141">Erstellen einer Kursbeschreibung, mit der Sie im Mitarbeiter-Self-Service-Portal werben können.</span><span class="sxs-lookup"><span data-stu-id="ee00c-141">Create a course description, which you can then advertise on Employee self service</span></span>

  ><span data-ttu-id="ee00c-142">**Hinweis** Sie können einen Kurs nur löschen, wenn niemand für ihn registriert ist.</span><span class="sxs-lookup"><span data-stu-id="ee00c-142">**Note** You can delete a course only if no one has registered for it.</span></span> 
    
## <a name="course-statuses"></a><span data-ttu-id="ee00c-143">Kursstatus</span><span class="sxs-lookup"><span data-stu-id="ee00c-143">Course statuses</span></span>
<span data-ttu-id="ee00c-144">In der folgenden Tabelle werden die möglichen Kursstatus und Aktivitäten aufgelistet, die ausgeführt werden können, wenn der Kurs einen bestimmten Status hat.</span><span class="sxs-lookup"><span data-stu-id="ee00c-144">The following table lists the possible course statuses and the actions that you can complete when the course has a specific status.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="ee00c-145">Status</span><span class="sxs-lookup"><span data-stu-id="ee00c-145">Status</span></span></th>
<th><span data-ttu-id="ee00c-146">Aktionen</span><span class="sxs-lookup"><span data-stu-id="ee00c-146">Actions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ee00c-147"><strong>Erstellt</strong></span><span class="sxs-lookup"><span data-stu-id="ee00c-147"><strong>Created</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="ee00c-148">Geben Sie Kursinformationen ein, und bearbeiten Sie sie.</span><span class="sxs-lookup"><span data-stu-id="ee00c-148">Enter and modify course information.</span></span></li>
<li><span data-ttu-id="ee00c-149">Ändern Sie den Kursstatus in <strong>Offen</strong>, so dass Arbeitskräfte sich für den Kurs registrieren können.</span><span class="sxs-lookup"><span data-stu-id="ee00c-149">Change the course status to <strong>Open</strong> so that workers can register for the course.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee00c-150"><strong>Offen</strong></span><span class="sxs-lookup"><span data-stu-id="ee00c-150"><strong>Open</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="ee00c-151">Registrieren Sie Teilnehmer für den Kurs.</span><span class="sxs-lookup"><span data-stu-id="ee00c-151">Register participants for the course.</span></span></li>
<li><span data-ttu-id="ee00c-152">Entfernen Sie Teilnehmer aus dem Kurs.</span><span class="sxs-lookup"><span data-stu-id="ee00c-152">Remove participants from the course.</span></span></li>
<li><span data-ttu-id="ee00c-153">Bestätigen Sie die Teilnehmer für den Kurs.</span><span class="sxs-lookup"><span data-stu-id="ee00c-153">Confirm participants for the course.</span></span></li>
<li><span data-ttu-id="ee00c-154">Ändern Sie den Kursstatus in <strong>Geschlossen</strong> oder <strong>Storniert</strong>.</span><span class="sxs-lookup"><span data-stu-id="ee00c-154">Change the course status to <strong>Closed</strong> or <strong>Canceled</strong>.</span></span></li>
<li><span data-ttu-id="ee00c-155">Planen von Fragebögen für Teilnehmer mit dem Status <strong>Bestätigt</strong>.</span><span class="sxs-lookup"><span data-stu-id="ee00c-155">Plan questionnaires for participants whose status is <strong>Confirmed</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ee00c-156"><strong>Geschlossen</strong></span><span class="sxs-lookup"><span data-stu-id="ee00c-156"><strong>Closed</strong></span></span></td>
<td><span data-ttu-id="ee00c-157">Sie können den Kurs erneut öffnen.</span><span class="sxs-lookup"><span data-stu-id="ee00c-157">You can reopen the course.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee00c-158"><strong>Abgebrochen</strong></span><span class="sxs-lookup"><span data-stu-id="ee00c-158"><strong>Canceled</strong></span></span></td>
<td><span data-ttu-id="ee00c-159">Sie können den Kurs erneut öffnen.</span><span class="sxs-lookup"><span data-stu-id="ee00c-159">You can reopen the course.</span></span></td>
</tr>
</tbody>
</table>

## <a name="course-participants"></a><span data-ttu-id="ee00c-160">Kursteilnehmer</span><span class="sxs-lookup"><span data-stu-id="ee00c-160">Course participants</span></span>
<span data-ttu-id="ee00c-161">Kursteilnehmer sind Arbeitskräfte, Bewerber oder Kontaktpersonen, die an einem Schulungskurs oder Ereignis teilnehmen.</span><span class="sxs-lookup"><span data-stu-id="ee00c-161">Course participants are workers, applicants, or contact persons who participate in a training course or event.</span></span> <span data-ttu-id="ee00c-162">Sie können nur Teilnehmer für offene Kurse registrieren.</span><span class="sxs-lookup"><span data-stu-id="ee00c-162">You can only register participants for open courses.</span></span> <span data-ttu-id="ee00c-163">Die Höchst- und Mindestzahl der Teilnehmer, die für einen Kurs registriert werden können, wird im Inforegister **Allgemein** auf der Seite **Kurse** definiert.</span><span class="sxs-lookup"><span data-stu-id="ee00c-163">The minimum and maximum number of participants that you can register for a course is defined on the **General** FastTab on the **Courses** page.</span></span>

<a name="workflow"></a><span data-ttu-id="ee00c-164">Workflow</span><span class="sxs-lookup"><span data-stu-id="ee00c-164">Workflow</span></span>
--------

<span data-ttu-id="ee00c-165">Mitarbeiter, die sich über die Seite **Mitarbeiter-Self-Service** erfassen, können ihre Erfassung per Workflow zur Genehmigung weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="ee00c-165">Employees who register for a course through the **Employee self service** page can have their registration routed through workflow for approval.</span></span>  <span data-ttu-id="ee00c-166">Ein Workflow kann für einen Kurs im Inforegister **Allgemein** auf der Seite**Kurse** zugewiesen werden. </span><span class="sxs-lookup"><span data-stu-id="ee00c-166">A workflow can be assigned to a course on the **General** FastTab on the **Courses** page.</span></span>






