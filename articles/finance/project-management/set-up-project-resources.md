---
title: Einrichten von Projektressourcen
description: Dieser Thema enthält Informationen über die Einrichtung oder Anforderung von Projektressourcen.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c882e23794e3937f85b3e73774b36deaf28ac3ed
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760558"
---
# <a name="set-up-project-resources"></a><span data-ttu-id="5a715-103">Einrichten von Projektressourcen</span><span class="sxs-lookup"><span data-stu-id="5a715-103">Set up project resources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5a715-104">Sie müssen einen Kalender einrichten und diesen einem Mitarbeiter oder einer Arbeitskraft zuordnen.</span><span class="sxs-lookup"><span data-stu-id="5a715-104">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="5a715-105">Der Kalender wird verwendet, um das Projekt und die Arbeitszeit der Ressourcen planen, die dem Projekt reserviert werden.</span><span class="sxs-lookup"><span data-stu-id="5a715-105">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="5a715-106">Während der Kalendereinstellung können Projektmanager einen Ressourcenausgleich als Teil der Ressourcenoptimierung ausführen.</span><span class="sxs-lookup"><span data-stu-id="5a715-106">During calendar setup, project managers can do resource leveling as part of resource optimization.</span></span> <span data-ttu-id="5a715-107">Basierend auf dem Kalenderzeitplan können Einschränkungen für Ressourcen festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="5a715-107">Based on the calendar schedule, restrictions can be put on resources.</span></span> <span data-ttu-id="5a715-108">Sie können einen Kalender auf der **Seite** Kalender einrichten.</span><span class="sxs-lookup"><span data-stu-id="5a715-108">You can set up a calendar on the **Calendars** page.</span></span>

<span data-ttu-id="5a715-109">Wenn Sie eine Arbeitskraft als Projektressource einrichten, können Sie aus Arbeitskräften auswählen, die in dem Unternehmen arbeiten, für das Sie Ressourcen einrichten.</span><span class="sxs-lookup"><span data-stu-id="5a715-109">When you set up a worker as a project resource, you can select from workers who work in the company that you're setting up resources for.</span></span> <span data-ttu-id="5a715-110">Alternativ können Sie Arbeitskräfte von anderen Unternehmen in Ihrer Organisation auswählen.</span><span class="sxs-lookup"><span data-stu-id="5a715-110">Alternatively, you can select workers from other companies in your organization.</span></span> <span data-ttu-id="5a715-111">Diese Arbeitskräfte werden als Intercompany-Ressourcen bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="5a715-111">These workers are known as intercompany resources.</span></span>

<span data-ttu-id="5a715-112">Nachfolgend wird erläutert, wie eine Arbeitskraft als Projektressource in Ihrem Unternehmen eingerichtet wird und wie eine Intercompany-Ressource eingerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="5a715-112">The following procedures explain how to set up a worker as a project resource in your company and how to set up an intercompany project resource.</span></span>

## <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="5a715-113">Arbeitskräfte als Projektressourcen einrichten</span><span class="sxs-lookup"><span data-stu-id="5a715-113">Set up a worker as a project resource</span></span>

1. <span data-ttu-id="5a715-114">Wählen Sie auf der Seite **Arbeitskräfte** in der Liste **Arbeitskräfte** die Arbeitskraft, die Sie als Projektressource hinzufügen und öffnen Sie den Arbeitskraftdatensatz.</span><span class="sxs-lookup"><span data-stu-id="5a715-114">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2. <span data-ttu-id="5a715-115">Klicken Sie im Aktivitätsbereich auf **Projekt** &gt; **Einstellungen** &gt; **Projekteinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="5a715-115">On the Action Pane, select **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3. <span data-ttu-id="5a715-116">Wählen Sie einen Kalender aus, und schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="5a715-116">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="5a715-117">Sie können außerdem standardmäßige Projekte für eine Ressource als Typ einer Vorabzuweisung angeben.</span><span class="sxs-lookup"><span data-stu-id="5a715-117">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="5a715-118">Vorabzuweisungen können verwendet werden, wenn der Ressourcen-Manager oder der Projektmanager weiß, welche Projekte für die Ressource gelten oder im Voraus.</span><span class="sxs-lookup"><span data-stu-id="5a715-118">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="5a715-119">Vorabzuweisungen können außerdem auf der Anforderung eines Projektträgers oder des Debitors basieren.</span><span class="sxs-lookup"><span data-stu-id="5a715-119">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="5a715-120">Damit ein Projekt auf der Seite **Projekte zuweisen** vorab zugewiesen werden kann, wählen Sie auf der Registerkarte **Projekte** in der Liste **Verbleibende Projekte** das gewünschte Projekt aus.</span><span class="sxs-lookup"><span data-stu-id="5a715-120">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

## <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="5a715-121">Einrichten einer Intercompany-Ressource</span><span class="sxs-lookup"><span data-stu-id="5a715-121">Set up an intercompany resource</span></span>

<span data-ttu-id="5a715-122">Wenn Sie eine Arbeitskraft als Intercompany-Ressource einrichten, müssen Sie die Einstellungen im Ausleiheunternehmen und im leihenden Unternehmen ausführen.</span><span class="sxs-lookup"><span data-stu-id="5a715-122">When you set up a worker as an intercompany resource, you must complete the setup in both the lending company and the borrowing company.</span></span>

### <a name="in-the-lending-company"></a><span data-ttu-id="5a715-123">Im Ausleiheunternehmen</span><span class="sxs-lookup"><span data-stu-id="5a715-123">In the lending company</span></span>

1. <span data-ttu-id="5a715-124">Überprüfen Sie in Finance, dass das Ausleiheunternehmen aktiviert ist, und schließen Sie dann das Verfahren wie im vorherigen Abschnitt „Arbeitkraft als Projektressource einrichten“ beschrieben ab.</span><span class="sxs-lookup"><span data-stu-id="5a715-124">In Finance, verify that the lending company is selected, and then complete the procedure in the previous section, "Set up a worker as a project resource."</span></span>
2. <span data-ttu-id="5a715-125">Wählen Sie auf der Seite **Verrechnung** **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="5a715-125">On the **Intercompany accounting** page, select **New**.</span></span>
3. <span data-ttu-id="5a715-126">Wählen Sie im Feld **Kennung der juristischen Person** das Ausleiheunternehmen aus.</span><span class="sxs-lookup"><span data-stu-id="5a715-126">In the **Legal entity ID** field, select the lending company.</span></span> <span data-ttu-id="5a715-127">Füllen Sie die restlichen Felder entsprechend aus, und wählen Sie dann **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="5a715-127">Fill in the remaining fields as appropriate, and then select **Save**.</span></span>
4. <span data-ttu-id="5a715-128">Wählen Sie auf der Seite **Interner Verrechnungspreis** **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="5a715-128">On the **Transfer price** page, select **New**.</span></span>
5. <span data-ttu-id="5a715-129">Wählen Sie im Feld **Ausleihende juristische Person** das entsprechende Unternehmen aus.</span><span class="sxs-lookup"><span data-stu-id="5a715-129">In the **Borrowing legal entity** field, select the appropriate company.</span></span>
6. <span data-ttu-id="5a715-130">Wenn Sie dem borgenden Unternehmen nur die Ressource ausleihen möchten, die Sie am Anfang dieses Abschnitts im Feld **Ressource** erstellt haben, wählen Sie den Namen der Ressource aus, die Sie erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="5a715-130">To lend the borrowing company only the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="5a715-131">Wenn alle Ressourcen im Ausleiheunternehmen für das borgende Unternehmen verfügbar gemacht werden sollen, lassen Sie das Feld **Ressource** leer.</span><span class="sxs-lookup"><span data-stu-id="5a715-131">To make all resources in the lending company available to the borrowing company, leave the **Resource** field blank.</span></span>
7. <span data-ttu-id="5a715-132">Setzen Sie auf der Seite **Projektverwaltungs- und -verrechnungsparameter** auf der Registerkarte **Intercompany** die Option **Intercompany-Ressourcenplanung und -Arbeitszeitnachweise** auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="5a715-132">On the **Project management and accounting parameters** page, on the **Intercompany** tab, set the **Enable intercompany resource scheduling and timesheets** option to **Yes**.</span></span>

### <a name="in-the-borrowing-company"></a><span data-ttu-id="5a715-133">Im leihenden Unternehmen</span><span class="sxs-lookup"><span data-stu-id="5a715-133">In the borrowing company</span></span>

- <span data-ttu-id="5a715-134">Geben Sie auf der Seite **Ressourcenliste** im Suchfilter den Namen der Ressource ein, die Sie für das Ausleiheunternehmen erstellt haben, um zu prüfen, ob der Name in der Ressourcenliste für das borgende Unternehmen enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="5a715-134">On the **Resources list** page, in the search filter, enter the name of the resource that you created for the lending company, to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="request-project-resources"></a><span data-ttu-id="5a715-135">Projektressourcen anfordern</span><span class="sxs-lookup"><span data-stu-id="5a715-135">Request project resources</span></span>
<span data-ttu-id="5a715-136">Die Projekteinsatzplanungsfunktionen unterstützen Ressourcen-Manager nur bei der Verteilung von Ressourcen mit Personal auf Aufträge oder Projekte.</span><span class="sxs-lookup"><span data-stu-id="5a715-136">The functionality for project resource scheduling only lets resource managers distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="5a715-137">Um diese Funktion zu aktivieren, führen Sie die folgenden Aufgaben aus, oder stellen Sie sicher, dass diese abgeschlossen wurden:</span><span class="sxs-lookup"><span data-stu-id="5a715-137">To enable this functionality, complete the following tasks, or verify that they have been completed:</span></span>

- <span data-ttu-id="5a715-138">Hier können Sie Nummernkreise einrichten.</span><span class="sxs-lookup"><span data-stu-id="5a715-138">Set up number sequences.</span></span>
- <span data-ttu-id="5a715-139">Einrichten von Projektverwaltungs- und Buchhaltungsworkflows</span><span class="sxs-lookup"><span data-stu-id="5a715-139">Set up project management and accounting workflows.</span></span>
- <span data-ttu-id="5a715-140">Aktivieren der Ressourcenanforderungsworkflows.</span><span class="sxs-lookup"><span data-stu-id="5a715-140">Enable resource request workflows.</span></span>

<span data-ttu-id="5a715-141">Nachdem Sie die vorherigen Aufgaben abgeschlossen haben, können Sie die folgenden Aufgaben bei Bedarf abschließen:</span><span class="sxs-lookup"><span data-stu-id="5a715-141">After the preceding tasks have been completed, you can complete the following tasks as you require:</span></span>

- <span data-ttu-id="5a715-142">Erstellen Sie eine Ressourcenanforderung von nicht fest gebuchten Personal Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="5a715-142">Create a resource request from a soft-booked staffed resource.</span></span>
- <span data-ttu-id="5a715-143">Ressourcenanforderungen überwachen</span><span class="sxs-lookup"><span data-stu-id="5a715-143">Monitor resource requests.</span></span>
- <span data-ttu-id="5a715-144">Ressourcenanforderungen erfüllen</span><span class="sxs-lookup"><span data-stu-id="5a715-144">Fulfill resource requests.</span></span>
- <span data-ttu-id="5a715-145">Anfordern von Ressourcen mit Personal aus PSP.</span><span class="sxs-lookup"><span data-stu-id="5a715-145">Request a staffed resource from a WBS.</span></span>
- <span data-ttu-id="5a715-146">Buchen von Ressourcen für ein Projekt ohne Anforderung einer Ressource mit Personal.</span><span class="sxs-lookup"><span data-stu-id="5a715-146">Book resources to a project without having a request for a staffed resource.</span></span>
