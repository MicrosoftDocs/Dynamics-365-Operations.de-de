---
title: Masseneinstellungsprojekte
description: Masseneinstellungsprojekte ermöglichen dem Personalverwaltungsspezialisten mehrere Positionen zu erstellen und effektiv mehrere Arbeitskräfte für diese Positionen einzustellen.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMMassHireProject
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.custom: 7481
ms.assetid: 5f5eb271-76eb-4305-bd1c-5d171dafccc9
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f7dacc8b0ca8659d3ae69c81385918ef6fa39c04
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1510748"
---
# <a name="mass-hire-projects"></a><span data-ttu-id="a4b2d-103">Masseneinstellungsprojekte</span><span class="sxs-lookup"><span data-stu-id="a4b2d-103">Mass hire projects</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a4b2d-104">Masseneinstellungsprojekte ermöglichen dem Personalverwaltungsspezialisten mehrere Positionen zu erstellen und effektiv mehrere Arbeitskräfte für diese Positionen einzustellen.</span><span class="sxs-lookup"><span data-stu-id="a4b2d-104">Mass hire projects allow human resources specialists to create multiple positions and efficiently hire workers into those positions.</span></span>

## <a name="overview"></a><span data-ttu-id="a4b2d-105">Überblick</span><span class="sxs-lookup"><span data-stu-id="a4b2d-105">Overview</span></span>

<span data-ttu-id="a4b2d-106">Verwenden Sie Masseneinstellungsprojekte, wenn Sie mehrere Arbeitskräfte gleichzeitig einstellen, beispielsweise bei Einstellungen zur Deckung eines saisonalen Bedarfs.</span><span class="sxs-lookup"><span data-stu-id="a4b2d-106">Use mass hire projects when you hire multiple workers at one time, such as when you hire to meet a seasonal demand.</span></span> <span data-ttu-id="a4b2d-107">Die Erstellung eines Masseneinstellungsprojekts ist sinnvoll, da Sie Positionsdatensätze, Arbeitskraftdatensätze und Arbeitskraftzuweisungen für Positionen gleichzeitig erstellen können.</span><span class="sxs-lookup"><span data-stu-id="a4b2d-107">Creating a mass hire project is useful because you can create position records, worker records, and worker assignments for positions at the same time.</span></span> <span data-ttu-id="a4b2d-108">Wenn Sie Positionen für ein Masseneinstellungsprojekt erstellen, können Sie die folgenden Informationen angeben:</span><span class="sxs-lookup"><span data-stu-id="a4b2d-108">When you create positions for a mass hire project, you can specify the following information:</span></span>

- <span data-ttu-id="a4b2d-109">die Anzahl der zu erstellenden Positionen</span><span class="sxs-lookup"><span data-stu-id="a4b2d-109">The number of positions to create</span></span>
- <span data-ttu-id="a4b2d-110">den Arbeitskrafttyp der Personen, die Sie für die Positionen einstellen</span><span class="sxs-lookup"><span data-stu-id="a4b2d-110">The worker type of the people that you will hire for the positions</span></span>
- <span data-ttu-id="a4b2d-111">die Abteilung und den Einzelvorgang, die den Positionen zugeordnet sind</span><span class="sxs-lookup"><span data-stu-id="a4b2d-111">The department and the job that are associated with the positions</span></span>
- <span data-ttu-id="a4b2d-112">das Vollzeitäquivalent der Position</span><span class="sxs-lookup"><span data-stu-id="a4b2d-112">The full-time equivalent value of the position</span></span>

## <a name="example"></a><span data-ttu-id="a4b2d-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a4b2d-113">Example</span></span>

<span data-ttu-id="a4b2d-114">Im Sommer stellen Sie normalerweise 15-20 Teilzeitstudenten ein, die verfügbare Praktikantenstellen in Ihrem Unternehmen ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="a4b2d-114">In the summer, you usually hire 15-20 part-time college students to fill available internships in your company.</span></span> <span data-ttu-id="a4b2d-115">In diesem Jahr möchten Sie fünf Buchhalter, fünf Auftragsbearbeiter und fünf Kassierer einstellen.</span><span class="sxs-lookup"><span data-stu-id="a4b2d-115">This year, you want to hire five accountants, five order processors, and five cashiers.</span></span> <span data-ttu-id="a4b2d-116">Anstatt jeden Positionsdatensatz und Arbeitskraftdatensatz separat zu erstellen, erstellen Sie ein Masseneinstellungsprojekt mit der Bezeichnung "SummerInterns".</span><span class="sxs-lookup"><span data-stu-id="a4b2d-116">Instead of creating each position record and worker record separately, you create one mass hire project called "SummerInterns".</span></span> <span data-ttu-id="a4b2d-117">Anfangs- und Enddatum des Projekts entsprechen dem Anfangs- und Enddatum der Dauer der Positionen, die Sie für das Masseneinstellungsprojekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="a4b2d-117">The project start and end dates correlate with the start and end dates of the position durations for the positions you create for the mass hire project.</span></span>

<span data-ttu-id="a4b2d-118">Wählen Sie auf der Seite **Masseneinstellungsprojekte** das Projekt “SummerInterns” aus und klicken Sie auf **Projekt öffnen**.</span><span class="sxs-lookup"><span data-stu-id="a4b2d-118">In the **Mass hire projects** page, select the "SummerInterns" project and then click **Open project**.</span></span> <span data-ttu-id="a4b2d-119">Klicken Sie im geöffneten Masseneinstellungsprojekt auf **Positionen erstellen**, und geben Sie Informationen zur Buchhalterposition ein.</span><span class="sxs-lookup"><span data-stu-id="a4b2d-119">In the open mass hire project, click **Create positions** and enter information about the accountant position.</span></span> <span data-ttu-id="a4b2d-120">Sie können angeben, dass fünf Buchhalterpositionen mithilfe derselben Informationen erstellt werden sollten. Klicken Sie anschließend auf "OK".</span><span class="sxs-lookup"><span data-stu-id="a4b2d-120">You can indicate that five accountant positions should be created using the same information for each one, and then click OK.</span></span> <span data-ttu-id="a4b2d-121">Wiederholen Sie diesen Vorgang für die Auftragssachbearbeiter- und Kassiererpositionen.</span><span class="sxs-lookup"><span data-stu-id="a4b2d-121">Repeat this process for the order processor and cashier positions.</span></span>

<span data-ttu-id="a4b2d-122">«»Nachdem Sie Studenten für die Praktikumspositionen ausgewählt haben, geben Sie die Informationen jedes Studenten unter **Positionsdetails** für die Position ein, für die sie eingestellt werden.</span><span class="sxs-lookup"><span data-stu-id="a4b2d-122">After selecting students to hire for the internship positions, you'll enter each student's information in the **Position details** for the position that you're hiring them for.</span></span> <span data-ttu-id="a4b2d-123">Wenn Sie alle Positionsdetails eingegeben haben, wählen Sie die Position auf der Seite "Masseneinstellungsprojekte" aus, und dann klicken Sie auf **Einstellen**.</span><span class="sxs-lookup"><span data-stu-id="a4b2d-123">When you have entered all of the position details, select the position in the Mass hire projects page, and then click **Hire**.</span></span> <span data-ttu-id="a4b2d-124">Für jede Position wird ein Positionsdatensatz erstellt, und für jede Person, die Sie einstellen, wird ein Arbeitskraftdatensatz erstellt und der richtigen Position zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="a4b2d-124">A position record will be created for each position and a worker record will be created and assigned to the correct position for each person who you hire.</span></span>

## <a name="mass-hire-project-statuses"></a><span data-ttu-id="a4b2d-125">Status eines Masseneinstellungsprojekts</span><span class="sxs-lookup"><span data-stu-id="a4b2d-125">Mass hire project statuses</span></span>

<span data-ttu-id="a4b2d-126">Ein Masseneinstellungsprojekt kann folgende Status besitzen.</span><span class="sxs-lookup"><span data-stu-id="a4b2d-126">A mass hire project can have the following statuses.</span></span>

- <span data-ttu-id="a4b2d-127">Erstellt</span><span class="sxs-lookup"><span data-stu-id="a4b2d-127">Created</span></span>
- <span data-ttu-id="a4b2d-128">Geöffnet</span><span class="sxs-lookup"><span data-stu-id="a4b2d-128">Open</span></span>
- <span data-ttu-id="a4b2d-129">Geschlossen</span><span class="sxs-lookup"><span data-stu-id="a4b2d-129">Closed</span></span>

<span data-ttu-id="a4b2d-130">Klicken Sie auf der Seite **Masseneinstellungsprojekt** auf **Projekt öffnen** oder **Projekt schließen**, um den Status eines Masseneinstellungsprojekts zu ändern.</span><span class="sxs-lookup"><span data-stu-id="a4b2d-130">On the **Mass hire project** page, click **Open project** or **Close project** to change the status of a mass hire project.</span></span> <span data-ttu-id="a4b2d-131">In der folgenden Tabelle wird erläutert, welche Möglichkeiten Sie im Hinblick auf den Projektstatus haben:</span><span class="sxs-lookup"><span data-stu-id="a4b2d-131">The following table describes what you can do with a project according to its status.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a4b2d-132">Status</span><span class="sxs-lookup"><span data-stu-id="a4b2d-132">Status</span></span></th>
<th><span data-ttu-id="a4b2d-133">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a4b2d-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a4b2d-134">Erstellt</span><span class="sxs-lookup"><span data-stu-id="a4b2d-134">Created</span></span></td>
<td><span data-ttu-id="a4b2d-135">Sie können Informationen erstellen und ändern, können jedoch keine Positionen für das Projekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="a4b2d-135">You can create and modify information, but cannot create positions for the project.</span></span> <span data-ttu-id="a4b2d-136">Dies ist der standardmäßige Status von neuen Projekten.</span><span class="sxs-lookup"><span data-stu-id="a4b2d-136">This is the default status for new projects.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4b2d-137">Geöffnet</span><span class="sxs-lookup"><span data-stu-id="a4b2d-137">Open</span></span></td>
<td><span data-ttu-id="a4b2d-138">Sie können die Projektdetails ändern, Positionen für das Masseneinstellungsprojekt erstellen und Personen für die Positionen einstellen.</span><span class="sxs-lookup"><span data-stu-id="a4b2d-138">You can modify the project details, create positions for the mass hire project, and hire people for the positions.</span></span> <span data-ttu-id="a4b2d-139">Dies ist der Status für aktive Projekte.</span><span class="sxs-lookup"><span data-stu-id="a4b2d-139">This is the status for active projects.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4b2d-140">Geschlossen</span><span class="sxs-lookup"><span data-stu-id="a4b2d-140">Closed</span></span></td>
<td><span data-ttu-id="a4b2d-141">Sie können dem Projekt keine Positionen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a4b2d-141">You cannot add positions to the project.</span></span> <span data-ttu-id="a4b2d-142">Wenn Sie dem Masseneinstellungsprojekt Positionen hinzufügen möchten, öffnen Sie das Projekt erneut.</span><span class="sxs-lookup"><span data-stu-id="a4b2d-142">To add positions to the mass hire project, open the project again.</span></span> <span data-ttu-id="a4b2d-143">Dies ist der Status für abgeschlossene Projekte.</span><span class="sxs-lookup"><span data-stu-id="a4b2d-143">This is the status for completed projects.</span></span>
<blockquote>[!NOTE] <span data-ttu-id="a4b2d-144">Ein Masseneinstellungsprojekt kann erst geschlossen werden, wenn alle Positionen im Projekt entweder den Status "Erstellt" oder den Status "Geschlossen" haben.</span><span class="sxs-lookup"><span data-stu-id="a4b2d-144">Before you can close a mass hire project, all positions in the project must have a status of either Created or Closed.</span></span></blockquote>
</td>
</tr>
</tbody>
</table>
