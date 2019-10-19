---
title: ER Upload einer Konfiguration nach Lifecycle Services
description: In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Systemadministratorrolle oder der Rolle "Entwickler für elektronische Berichterstellung" eine neue Konfiguration für "Elektronische Berichterstellung (ER)" erstellen kann und sie nach Microsoft Lifecycle Services (LCS) hochladen kann.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 980ce00ae702ea0a3394efa15419e0f7b7dc2530
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182208"
---
# <a name="er-upload-a-configuration-into-lifecycle-services"></a><span data-ttu-id="9691f-103">ER Upload einer Konfiguration nach Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="9691f-103">ER Upload a configuration into Lifecycle Services</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9691f-104">In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Systemadministratorrolle oder der Rolle "Entwickler für elektronische Berichterstellung" eine neue Konfiguration für "Elektronische Berichterstellung (ER)" erstellen kann und sie nach Microsoft Lifecycle Services (LCS) hochladen kann.</span><span class="sxs-lookup"><span data-stu-id="9691f-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration and upload it into Microsoft Lifecycle Services (LCS).</span></span>

<span data-ttu-id="9691f-105">In diesem Beispiel erstellen Sie eine Konfiguration für das Beispielunternehmen, Litware, Inc. und laden Sie in LCS hoch. Diese Schritte können in einem beliebigen Unternehmen ausgeführt werden, da ER-Konfigurationen unter Unternehmen geteilt werden.</span><span class="sxs-lookup"><span data-stu-id="9691f-105">In this example, you will create a configuration and upload it to LCS for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="9691f-106">Um diese Schritte auszuführen, müssen Sie zunächst die Schritte unter "Konfigurationsanbieter erstellen und als aktiv markieren" abschließen.</span><span class="sxs-lookup"><span data-stu-id="9691f-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="9691f-107">Zugriff auf LCS ist auch für den Abschluss dieser Schritte erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9691f-107">Access to LCS is also required for completion of these steps.</span></span>

1. <span data-ttu-id="9691f-108">Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="9691f-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="9691f-109">Wählen Sie „Litware, inc.” aus</span><span class="sxs-lookup"><span data-stu-id="9691f-109">Select ‘Litware, Inc.’</span></span> <span data-ttu-id="9691f-110">un lege es als aktiv fest.</span><span class="sxs-lookup"><span data-stu-id="9691f-110">and set it as active.</span></span>
3. <span data-ttu-id="9691f-111">Klicken Sie auf "Konfigurationen".</span><span class="sxs-lookup"><span data-stu-id="9691f-111">Click Configurations.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="9691f-112">Neue Datenmodellkonfiguration erstellen</span><span class="sxs-lookup"><span data-stu-id="9691f-112">Create a new data model configuration</span></span>
1. <span data-ttu-id="9691f-113">Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="9691f-113">Click Create configuration to open the drop dialog.</span></span>
    * <span data-ttu-id="9691f-114">Sie erstellen eine Konfiguration, die ein Beispieldatenmodell für elektronische Dokumente enthält.</span><span class="sxs-lookup"><span data-stu-id="9691f-114">You will create a configuration that contains a sample data model for electronic documents.</span></span> <span data-ttu-id="9691f-115">Diese Datenmodellkonfiguration wird später in LCS hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="9691f-115">This data model configuration will be uploaded into LCS later.</span></span>  
2. <span data-ttu-id="9691f-116">Geben Sie im Feld "Name" die Bezeichnung "Beispielmodellkonfiguration" ein.</span><span class="sxs-lookup"><span data-stu-id="9691f-116">In the Name field, type 'Sample model configuration'.</span></span>
    * <span data-ttu-id="9691f-117">Beispielmodellkonfiguration</span><span class="sxs-lookup"><span data-stu-id="9691f-117">Sample model configuration</span></span>  
3. <span data-ttu-id="9691f-118">Geben Sie im Feld "Beschreibung" die Bezeichnung "Beispielmodellkonfiguration" ein.</span><span class="sxs-lookup"><span data-stu-id="9691f-118">In the Description field, type 'Sample model configuration'.</span></span>
    * <span data-ttu-id="9691f-119">Beispielmodellkonfiguration</span><span class="sxs-lookup"><span data-stu-id="9691f-119">Sample model configuration</span></span>  
4. <span data-ttu-id="9691f-120">Klicken Sie auf Konfiguration erstellen.</span><span class="sxs-lookup"><span data-stu-id="9691f-120">Click Create configuration.</span></span>
5. <span data-ttu-id="9691f-121">Klicken Sie auf "Modelldesigner".</span><span class="sxs-lookup"><span data-stu-id="9691f-121">Click Model designer.</span></span>
6. <span data-ttu-id="9691f-122">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="9691f-122">Click New.</span></span>
7. <span data-ttu-id="9691f-123">Geben Sie im Feld "Name" die Bezeichnung "Eingangspunkt" ein.</span><span class="sxs-lookup"><span data-stu-id="9691f-123">In the Name field, type 'Entry point'.</span></span>
    * <span data-ttu-id="9691f-124">Einstiegspunkt</span><span class="sxs-lookup"><span data-stu-id="9691f-124">Entry point</span></span>  
8. <span data-ttu-id="9691f-125">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="9691f-125">Click Add.</span></span>
9. <span data-ttu-id="9691f-126">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="9691f-126">Click Save.</span></span>
10. <span data-ttu-id="9691f-127">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9691f-127">Close the page.</span></span>
11. <span data-ttu-id="9691f-128">Klicken Sie auf "Status ändern".</span><span class="sxs-lookup"><span data-stu-id="9691f-128">Click Change status.</span></span>
12. <span data-ttu-id="9691f-129">Klicken Sie auf "Abgeschlossen".</span><span class="sxs-lookup"><span data-stu-id="9691f-129">Click Complete.</span></span>
13. <span data-ttu-id="9691f-130">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="9691f-130">Click OK.</span></span>

## <a name="register-a-new--repository"></a><span data-ttu-id="9691f-131">Registrieren Sie ein neues Repository</span><span class="sxs-lookup"><span data-stu-id="9691f-131">Register a new  repository</span></span>
1. <span data-ttu-id="9691f-132">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9691f-132">Close the page.</span></span>
2. <span data-ttu-id="9691f-133">Klicken Sie auf Repositorys.</span><span class="sxs-lookup"><span data-stu-id="9691f-133">Click Repositories.</span></span>
    * <span data-ttu-id="9691f-134">Dies ermöglicht Ihnen, die Liste der Repositorys für Litware, Inc. als Konfigurationsanbieter zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="9691f-134">This enables you to open the list of repositories for the Litware, Inc. configuration provider.</span></span>  
3. <span data-ttu-id="9691f-135">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="9691f-135">Click Add to open the drop dialog.</span></span>
    * <span data-ttu-id="9691f-136">Dies ermöglicht Ihnen, ein neues Repository hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="9691f-136">This allows you to add a new repository.</span></span>  
4. <span data-ttu-id="9691f-137">Wählen Sie im Feld "Konfigurationsrepository-Typ" die Option "LCS" aus.</span><span class="sxs-lookup"><span data-stu-id="9691f-137">In the Configuration repository type field, select LCS.</span></span>
5. <span data-ttu-id="9691f-138">Klicken Sie auf "Repository erstellen".</span><span class="sxs-lookup"><span data-stu-id="9691f-138">Click Create repository.</span></span>
6. <span data-ttu-id="9691f-139">Geben Sie im Feld "Projekt" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="9691f-139">In the Project field, enter or select a value.</span></span>
    * <span data-ttu-id="9691f-140">Wählen Sie das gewünschte LCS-Projekt aus.</span><span class="sxs-lookup"><span data-stu-id="9691f-140">Select the desired LCS project.</span></span> <span data-ttu-id="9691f-141">Sie müssen Zugriff auf das Projekt besitzen.</span><span class="sxs-lookup"><span data-stu-id="9691f-141">You must have access to the project.</span></span>  
7. <span data-ttu-id="9691f-142">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="9691f-142">Click OK.</span></span>
    * <span data-ttu-id="9691f-143">Schließen Sie einen neuen Repositoryeintrag ab.</span><span class="sxs-lookup"><span data-stu-id="9691f-143">Complete a new repository entry.</span></span>  
8. <span data-ttu-id="9691f-144">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="9691f-144">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="9691f-145">Wählen Sie den LCS-Repository-Datensatz aus.</span><span class="sxs-lookup"><span data-stu-id="9691f-145">Select the LCS repository record.</span></span>  
    * <span data-ttu-id="9691f-146">Beachten Sie, dass ein registriertes Repository durch den aktuellen Anbieter markiert ist. Das bedeutet, dass nur Varianten, die diesem Anbieter gehören, zu diesem Repository platziert und folglich in das ausgewählte LCS-Projekt hochgeladen werden können.</span><span class="sxs-lookup"><span data-stu-id="9691f-146">Note that a registered repository is marked by the current provider meaning that the only configurations owned by that provider can be placed to this repository and, consequently, uploaded into the selected LCS project.</span></span>  
9. <span data-ttu-id="9691f-147">Klicken Sie auf "Öffnen".</span><span class="sxs-lookup"><span data-stu-id="9691f-147">Click Open.</span></span>
    * <span data-ttu-id="9691f-148">Öffnen Sie das Repository, um die Liste der ER-Konfigurationen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9691f-148">Open the repository to view the list of ER configurations.</span></span> <span data-ttu-id="9691f-149">Es ist leer, wenn dieses Projekt noch nicht zum Freigeben von ER-Konfigurationen verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="9691f-149">It will be empty if this project has not yet been used for ER configurations sharing.</span></span>  
10. <span data-ttu-id="9691f-150">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9691f-150">Close the page.</span></span>
11. <span data-ttu-id="9691f-151">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9691f-151">Close the page.</span></span>

## <a name="upload-configuration-into-lcs"></a><span data-ttu-id="9691f-152">Laden Sie Konfiguration in LCS hoch</span><span class="sxs-lookup"><span data-stu-id="9691f-152">Upload configuration into LCS</span></span>
1. <span data-ttu-id="9691f-153">Klicken Sie auf "Konfigurationen".</span><span class="sxs-lookup"><span data-stu-id="9691f-153">Click Configurations.</span></span>
2. <span data-ttu-id="9691f-154">Wählen Sie "Beispielmodellkonfiguration" in der Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="9691f-154">In the tree, select 'Sample model configuration'.</span></span>
    * <span data-ttu-id="9691f-155">Wählen Sie eine erstellte Konfiguration aus, die bereits abgeschlossen wurden.</span><span class="sxs-lookup"><span data-stu-id="9691f-155">Select a created configuration that has been already completed.</span></span>  
3. <span data-ttu-id="9691f-156">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="9691f-156">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="9691f-157">Wählen Sie die Version der ausgewählten Konfiguration mit dem Status "Abgeschlossen" aus.</span><span class="sxs-lookup"><span data-stu-id="9691f-157">Select the version of the selected configuration with the status of ‘Completed’.</span></span>  
4. <span data-ttu-id="9691f-158">Klicken Sie auf "Status ändern".</span><span class="sxs-lookup"><span data-stu-id="9691f-158">Click Change status.</span></span>
5. <span data-ttu-id="9691f-159">Klicken Sie auf "Freigeben".</span><span class="sxs-lookup"><span data-stu-id="9691f-159">Click Share.</span></span>
    * <span data-ttu-id="9691f-160">Der Konfigurationsstatus ändert sich von "Abgeschlossen" zu "Freigegeben", wenn er in LCS veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="9691f-160">The configuration status will change from ‘Completed’ to ‘Shared’ when it is published in LCS.</span></span>  
6. <span data-ttu-id="9691f-161">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="9691f-161">Click OK.</span></span>
7. <span data-ttu-id="9691f-162">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="9691f-162">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="9691f-163">Wählen Sie die Konfigurationsversion mit dem Status "Freigegeben" aus.</span><span class="sxs-lookup"><span data-stu-id="9691f-163">Select the configuration version with the status of 'Shared'.</span></span>  
    * <span data-ttu-id="9691f-164">Beachten Sie, dass sich der Status der ausgewählten Version von "Abgeschlossen" zu "Freigegeben" geändert hat.</span><span class="sxs-lookup"><span data-stu-id="9691f-164">Note that the status of the selected version has changed from ‘Completed’ to ‘Shared’.</span></span>  
8. <span data-ttu-id="9691f-165">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9691f-165">Close the page.</span></span>
9. <span data-ttu-id="9691f-166">Klicken Sie auf Repositorys.</span><span class="sxs-lookup"><span data-stu-id="9691f-166">Click Repositories.</span></span>
    * <span data-ttu-id="9691f-167">Dies ermöglicht Ihnen, die Liste der Repositorys für Litware, Inc. als Konfigurationsanbieter zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="9691f-167">This enables you to open the list of repositories for the Litware, Inc. configuration provider.</span></span>  
10. <span data-ttu-id="9691f-168">Klicken Sie auf "Öffnen".</span><span class="sxs-lookup"><span data-stu-id="9691f-168">Click Open.</span></span>
    * <span data-ttu-id="9691f-169">Wählen Sie das LCS-Repository aus und öffnen Sie es.</span><span class="sxs-lookup"><span data-stu-id="9691f-169">Select the LCS repository and open it.</span></span>  
    * <span data-ttu-id="9691f-170">Beachten Sie, dass die ausgewählte Variante als Anlage des ausgewählten LCS-Projekts angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="9691f-170">Note that the selected configuration is shown as an asset of the selected LCS project.</span></span>  
    * <span data-ttu-id="9691f-171">Öffnen Sie LCS mithilfe von https://lcs.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="9691f-171">Open LCS using https://lcs.dynamics.com.</span></span> <span data-ttu-id="9691f-172">Öffnen Sie ein Projekt, das zuvor für Repositoryregistrierung verwendet wurde, öffnen zu die "Anlagenbibliothek" dieses Projekts und erweitern Sie den Inhalt des Anlagentyps "GER-Konfiguration" – die hochgeladene ER-Konfiguration wird verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="9691f-172">Open a project that was used earlier for repository registration, open the ‘Asset library’ of this project, and expand the content of the ‘GER configuration’ asset type – the uploaded ER configuration will be available.</span></span> <span data-ttu-id="9691f-173">Beachten Sie, dass die hochgeladene LCS-Konfiguration zu einer anderen Instance werden kann, wenn Anbieter Zugriff auf dieses LCS-Projekt haben.</span><span class="sxs-lookup"><span data-stu-id="9691f-173">Note that the uploaded LCS configuration can be imported to another instance if providers have access to this LCS project.</span></span>  

