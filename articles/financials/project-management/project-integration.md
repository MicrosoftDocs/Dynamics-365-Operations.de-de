---
title: Microsoft Project Client-Integration
description: "Die Planung und Verwaltung eines Projektzeitplans kann komplex sein. Deshalb müssen Projektmanager Tools verwenden, mit denen sie diese Aufgabe bewältigen können. Die Integration mit Microsoft Project Client bietet Unterstützung, um einen Projektstrukturplan zu öffnen und zu verwalten."
author: KimANelson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: a72963f755f8eddb19b8526d2938eff039ab7df2
ms.contentlocale: de-de
ms.lasthandoff: 01/17/2018

---

# <a name="microsoft-project-client-integration"></a><span data-ttu-id="ae853-104">Microsoft Project Client-Integration</span><span class="sxs-lookup"><span data-stu-id="ae853-104">Microsoft Project client integration</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ae853-105">Die Planung und Verwaltung eines Projektzeitplans kann komplex sein. Deshalb müssen Projektmanager Tools verwenden, mit denen sie diese Aufgabe bewältigen können.</span><span class="sxs-lookup"><span data-stu-id="ae853-105">Planning and maintaining a project schedule can be complex, so project managers need to use tools that help them manage this task.</span></span> <span data-ttu-id="ae853-106">Die Integration mit Microsoft Project Client bietet Unterstützung, um einen Projektstrukturplan zu öffnen und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="ae853-106">Integration with Microsoft Project Client provides support to open and manage a project work breakdown structure.</span></span> <span data-ttu-id="ae853-107">Der Projektmanager kann beliebige Änderungen zurück zum Finance and Operations-Projektstrukturplan veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="ae853-107">The project manager can publish any changes back to the Finance and Operations project work breakdown structure.</span></span>

> [!NOTE]
> <span data-ttu-id="ae853-108">Wenn Sie das Update vom Juli für Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, verwenden, müssen Sie auch KB 4054797 und 4055884 installieren.</span><span class="sxs-lookup"><span data-stu-id="ae853-108">If you are using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, July update, you must install KB 4054797 and 4055884.</span></span>

## <a name="configure-the-microsoft-project-client-add-in"></a><span data-ttu-id="ae853-109">Konfigurieren des Microsoft Project Client-Add-Ins</span><span class="sxs-lookup"><span data-stu-id="ae853-109">Configure the Microsoft Project Client add-in</span></span>
<span data-ttu-id="ae853-110">Um die Integration mit Microsoft Project Client zu ermöglichen, muss ein Microsoft Dynamics 365-Add-In der Microsoft Project-Anwendung des Clients des Benutzers installiert werden.</span><span class="sxs-lookup"><span data-stu-id="ae853-110">To enable the integration with Microsoft Project Client, a Microsoft Dynamics 365 add-in is required to be installed in the user’s client Microsoft Project application.</span></span> <span data-ttu-id="ae853-111">Dies erfolgt, indem der **Projektverwaltungsarbeitsbereich** geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="ae853-111">This is done by opening the **Project management workspace**.</span></span>

<span data-ttu-id="ae853-112">•   Klicken Sie auf **Project Client-Add-In konfigurieren** aus dem Abschnitt **Links** > **Setup** des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="ae853-112">•   Click **Configure project client add-in** from the **Links** > **Setup** section of the workspace.</span></span>

<span data-ttu-id="ae853-113">•   Klicken Sie auf **Öffnen**, und klicken Sie dann auf **Ausführen**, wenn Sie dazu aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="ae853-113">•   Click **Open**, then click **Run** when prompted.</span></span>

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a><span data-ttu-id="ae853-114">Öffnen und Bearbeiten eines vorhandenen Entwurfs-Projektstrukturplans in Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="ae853-114">Open and edit an existing draft work breakdown structure in Microsoft Project Client</span></span>
<span data-ttu-id="ae853-115">Wenn für ein Projekt in Finance and Operations bereits ein Projektstrukturplan erstellt wird, kann der Projektstrukturplan in der Microsoft Project Client-Anwendung geöffnet werden, wenn der Projektstrukturplan sich im Entwurfsstatus befindet.</span><span class="sxs-lookup"><span data-stu-id="ae853-115">If a project in Finance and Operations already has a work breakdown structure created, the work breakdown structure can be opened in the Microsoft Project Client application if the work breakdown structure is in a draft status.</span></span> <span data-ttu-id="ae853-116">Um von der Seite **Project** aus zu öffnen, klicken Sie auf den Link **In Microsoft Project öffnen** von der Registerkarte **Plan**. Diese Seite kann auch von innerhalb der Microsoft Project Client-Anwendung aus geöffnet werden, indem Sie auf **Öffnen** in der Registerkarte **Microsoft Dynamics 365** klicken. Wählen Sie die **Juristische Person** und **Projekt** aus der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="ae853-116">To open from the **Project** page, click **Open in Microsoft Project** link from the **Plan** tab. This page can also be opened from within the Microsoft Project Client application by clicking **Open** in the **Microsoft Dynamics 365** tab. Select the **Legal entity** and **Project** from the list.</span></span>

> [!NOTE]
> <span data-ttu-id="ae853-117">Wenn Sie Internet Explorer als Browser verwenden, müssen Sie auf **Speichern** klicken, um manuell vom Speicherplatz aus zu öffnen, zu dem die Datei heruntergeladen wird.</span><span class="sxs-lookup"><span data-stu-id="ae853-117">If you're using Internet Explorer as your browser, you will need to click **Save** to manually open from the location that the file is downloaded to.</span></span> <span data-ttu-id="ae853-118">Oder klicken Sie auf **Speichern und öffnen**, um die Datei in Microsoft Project Client zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ae853-118">Or, click **Save and open** to open the file in Microsoft Project Client.</span></span> <span data-ttu-id="ae853-119">Benennen Sie den Dateinamen beim Speichern nicht um.</span><span class="sxs-lookup"><span data-stu-id="ae853-119">Do not rename the file name when saving.</span></span>

<span data-ttu-id="ae853-120">Bevor Sie irgendwelche Bearbeitungen an der Datei mithilfe von Microsoft Project Client vornehmen, müssen Sie sie zuerst auschecken. Klicken Sie auf **Auschecken** in der Registerkarte **Microsoft Dynamics 365**. Dadurch wird verhindert, dass andere Benutzer den Projektstrukturplan zur gleichen Zeit von innerhalb Finance and Operations aus bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="ae853-120">Before making any edits to the file using Microsoft Project Client, you need to check it out. Click **Check out** in the **Microsoft Dynamics 365** tab. This will prevent other users from editing the work breakdown structure from within Finance and Operations at the same time.</span></span> <span data-ttu-id="ae853-121">Um den Projektstrukturplan zu veröffentlichen, nachdem Sie irgendwelche Bearbeitungen abgeschlossen haben, klicken Sie auf **Einchecken** auf der Registerkarte **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="ae853-121">To publish the work breakdown structure after completing any edits, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

<span data-ttu-id="ae853-122">Wenn ein Projektteam bereits dem Projekt in Finance and Operations hinzugefügt wurde, wird die Ressourcenliste mit den Teammitgliedern aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="ae853-122">If a project team has already been added to the project in Finance and Operations, the resource list will be populated with the team members.</span></span> <span data-ttu-id="ae853-123">Wenn ein Projektteam noch nicht dem Projekt hinzugefügt wurde, können Sie Ressourcen auswählen und das Team innerhalb von Microsoft Project Client erstellen, indem Sie auf die Schaltfläche **Ressourcen** auf der Registerkarte **Microsoft Dynamics 365** klicken.</span><span class="sxs-lookup"><span data-stu-id="ae853-123">If a project team has not yet been added to the project, you can select resources and build the team within Microsoft Project Client by clicking the **Resources** button on the **Microsoft Dynamics 365** tab.</span></span> 

<span data-ttu-id="ae853-124">Die folgenden Daten werden zurück zu Finance and Operations als Teil des Eincheckprozesses synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="ae853-124">The following data will be synced back to Finance and Operations as part of the check in process:</span></span>

<span data-ttu-id="ae853-125">•   Aufgabenname</span><span class="sxs-lookup"><span data-stu-id="ae853-125">•   Task name</span></span>

<span data-ttu-id="ae853-126">•   Anfangsdatum</span><span class="sxs-lookup"><span data-stu-id="ae853-126">•   Start date</span></span>

<span data-ttu-id="ae853-127">•   Abschlussdatum</span><span class="sxs-lookup"><span data-stu-id="ae853-127">•   Finish date</span></span>

<span data-ttu-id="ae853-128">•   Vorherige Aktivitäten</span><span class="sxs-lookup"><span data-stu-id="ae853-128">•   Predecessors</span></span>

<span data-ttu-id="ae853-129">•   Ressourcennamen</span><span class="sxs-lookup"><span data-stu-id="ae853-129">•   Resource names</span></span>

<span data-ttu-id="ae853-130">•   Kategorie:</span><span class="sxs-lookup"><span data-stu-id="ae853-130">•   Category</span></span>

<span data-ttu-id="ae853-131">•   Ressourcenkategorie</span><span class="sxs-lookup"><span data-stu-id="ae853-131">•   Resource category</span></span>

<span data-ttu-id="ae853-132">•   Arbeitsstunden</span><span class="sxs-lookup"><span data-stu-id="ae853-132">•   Work hours</span></span>

<span data-ttu-id="ae853-133">•   Notizen</span><span class="sxs-lookup"><span data-stu-id="ae853-133">•   Notes</span></span>

<span data-ttu-id="ae853-134">•   Priorität</span><span class="sxs-lookup"><span data-stu-id="ae853-134">•   Priority</span></span>

> [!NOTE]
> <span data-ttu-id="ae853-135">Wenn Sie irgendwelche weitere Spalten zu Ihrer Microsoft Project Client-Datei hinzufügen, werden sie nicht in der Datei gespeichert und werden nicht angezeigt, wenn die Datei wieder geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="ae853-135">If you add any other columns to your Microsoft Project Client file, they will not be saved to the file and will not be displayed when the file is opened again.</span></span>

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="ae853-136">Erstellen des Projektstrukturplans für ein vorhandenes Projekt mithilfe von Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="ae853-136">Create the work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="ae853-137">Um einen neuen Projektstrukturplan mithilfe von Microsoft Project Client zu erstellen, folgen Sie diesen Schritten:</span><span class="sxs-lookup"><span data-stu-id="ae853-137">To create a new work breakdown structure using Microsoft Project Client, follow these steps:</span></span>


1.  <span data-ttu-id="ae853-138">Öffnen Sie Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="ae853-138">Open Microsoft Project Client.</span></span>

2.  <span data-ttu-id="ae853-139">Klicken Sie auf der Registerkarte **Microsoft Dynamics 365** auf **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="ae853-139">On the **Microsoft Dynamics 365** tab, click **Open**.</span></span>

3.  <span data-ttu-id="ae853-140">Wählen Sie die **Juristische Person** für das Projekt aus.</span><span class="sxs-lookup"><span data-stu-id="ae853-140">Select the **Legal entity** for the project.</span></span>

4.  <span data-ttu-id="ae853-141">Wählen Sie das **Projekt** aus.</span><span class="sxs-lookup"><span data-stu-id="ae853-141">Select the **Project**.</span></span>

5.  <span data-ttu-id="ae853-142">Klicken Sie auf **Auschecken** auf der Registerkarte **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="ae853-142">Click **Check out** on the **Microsoft Dynamics 365** tab.</span></span>

6.  <span data-ttu-id="ae853-143">Wenn Sie bereit sind, nach Finance and Operations zu veröffentlichen, klicken Sie auf **Einchecken** auf der Registerkarte **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="ae853-143">When ready to publish to Finance and Operations, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="ae853-144">Ersetzen des vorhandenen Projektstrukturplans für ein vorhandenes Projekt mithilfe von Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="ae853-144">Replace the existing work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="ae853-145">Um einen neuen Projektstrukturplan mithilfe von Microsoft Project Client zu erstellen und einen vorhandenen Projektstrukturplan für ein vorhandenes Projekt zu ersetzen, folgen Sie diesen Schritten:</span><span class="sxs-lookup"><span data-stu-id="ae853-145">To create a new work breakdown structure using Microsoft Project Client and replace an existing work breakdown structure for an existing project, follow these steps:</span></span>

1.  <span data-ttu-id="ae853-146">Öffnen Sie den Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="ae853-146">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="ae853-147">Erstellen Sie den Zeitplan in Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="ae853-147">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="ae853-148">Klicken Sie auf der Registerkarte **Microsoft Dynamics 365** auf **Änderungen speichern** > **Vorhandenes Projekt ersetzen**.</span><span class="sxs-lookup"><span data-stu-id="ae853-148">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Replace existing project**.</span></span>

4.  <span data-ttu-id="ae853-149">Wählen Sie die **Juristische Person** für das Projekt aus.</span><span class="sxs-lookup"><span data-stu-id="ae853-149">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="ae853-150">Wählen Sie das **Projekt** aus.</span><span class="sxs-lookup"><span data-stu-id="ae853-150">Select the **Project**.</span></span>

6.  <span data-ttu-id="ae853-151">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="ae853-151">Click **OK**.</span></span>

## <a name="create-a-new-project-from-within-microsoft-project-client"></a><span data-ttu-id="ae853-152">Erstellen eines neuen Projekts von Microsoft Project Client aus</span><span class="sxs-lookup"><span data-stu-id="ae853-152">Create a new project from within Microsoft Project Client</span></span>


1.  <span data-ttu-id="ae853-153">Öffnen Sie den Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="ae853-153">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="ae853-154">Erstellen Sie den Zeitplan in Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="ae853-154">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="ae853-155">Klicken Sie auf der Registerkarte **Microsoft Dynamics 365** auf **Änderungen speichern** > **In neuem Projekt speichern**.</span><span class="sxs-lookup"><span data-stu-id="ae853-155">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Save to new Project**.</span></span>

4.  <span data-ttu-id="ae853-156">Wählen Sie die **Juristische Person** für das Projekt aus.</span><span class="sxs-lookup"><span data-stu-id="ae853-156">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="ae853-157">Geben Sie die **Projektkennung** ein, falls erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ae853-157">Enter the **Project ID**, if necessary.</span></span>

6.  <span data-ttu-id="ae853-158">Geben Sie den **Projektnamen** ein.</span><span class="sxs-lookup"><span data-stu-id="ae853-158">Enter the **Project name**.</span></span>

7.  <span data-ttu-id="ae853-159">Wählen Sie den **Projekttyp**, die **Projektgruppe** und die **Projektvertragskennung** aus.</span><span class="sxs-lookup"><span data-stu-id="ae853-159">Select the **Project type**, **Project group** and the **Project contract ID**.</span></span> <span data-ttu-id="ae853-160">Alternativ können Sie einen neuen Projektvertrag erstellen, indem Sie auf **Neu** klicken.</span><span class="sxs-lookup"><span data-stu-id="ae853-160">Alternatively, you can create a new project contract by clicking **New**.</span></span>

8.  <span data-ttu-id="ae853-161">Wählen Sie den **Kalender** aus, der für die Ressourcenzuordnung zu verwenden ist.</span><span class="sxs-lookup"><span data-stu-id="ae853-161">Select the **Calendar** to be used for resourcing.</span></span>

11. <span data-ttu-id="ae853-162">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="ae853-162">Click **OK**.</span></span>

