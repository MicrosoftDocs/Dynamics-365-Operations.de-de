---
title: ER Import einer Konfiguration von Lifecycle Services
description: In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Systemadministratorrolle oder der Rolle "Entwickler für elektronische Berichterstellung" eine neue Konfiguration für "Elektronische Berichterstellung (ER)" erstellen kann und sie nach Microsoft Lifecycle Services (LCS) hochladen kann.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable,  ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 036d7e7e3f79e0945d6fef866a30edd41e688c07
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551321"
---
# <a name="er-import-a-configuration-from-lifecycle-services"></a><span data-ttu-id="add1a-103">ER Import einer Konfiguration von Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="add1a-103">ER Import a configuration from Lifecycle Services</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="add1a-104">In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Systemadministratorrolle oder der Rolle "Entwickler für elektronische Berichterstellung" eine neue Konfiguration für "Elektronische Berichterstellung (ER)" erstellen kann und sie nach Microsoft Lifecycle Services (LCS) hochladen kann.</span><span class="sxs-lookup"><span data-stu-id="add1a-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can import a new version of an Electronic reporting (ER) configuration from Microsoft Lifecycle Services (LCS).</span></span>

<span data-ttu-id="add1a-105">In diesem Beispiel wählen Sie die gewünschte Version der ER-Konfiguration und importieren das Beispielunternehmen, Litware, Inc. Diese Schritte können in einem beliebigen Unternehmen ausgeführt werden, da ER-Konfigurationsanbieter unter allen Unternehmen geteilt werden.</span><span class="sxs-lookup"><span data-stu-id="add1a-105">In this example, you will select the desired version of the ER configuration and import it for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="add1a-106">Um diese Schritte abzuschließen, müssen Sie zunächst die Schritte in der Prozedur "Eine ER-Konfiguration nach Lifecycle Services hochladen" abschließen.</span><span class="sxs-lookup"><span data-stu-id="add1a-106">To complete these steps, you must first complete the steps in the “Upload an ER configuration into Lifecycle Services” procedure.</span></span> <span data-ttu-id="add1a-107">Zugriff auf LCS ist auch für den Abschluss dieser Schritte erforderlich.</span><span class="sxs-lookup"><span data-stu-id="add1a-107">Access to LCS is also required for completion of these steps.</span></span>

1. <span data-ttu-id="add1a-108">Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="add1a-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="add1a-109">Klicken Sie auf "Konfigurationen".</span><span class="sxs-lookup"><span data-stu-id="add1a-109">Click Configurations.</span></span>

## <a name="delete-a-shared-version-of-data-model-configuration"></a><span data-ttu-id="add1a-110">Löschen Sie eine freigegebene Version der Datenmodellkonfiguration</span><span class="sxs-lookup"><span data-stu-id="add1a-110">Delete a shared version of data model configuration</span></span>
1. <span data-ttu-id="add1a-111">Wählen Sie "Beispielmodellkonfiguration" in der Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="add1a-111">In the tree, select 'Sample model configuration'.</span></span>
    * <span data-ttu-id="add1a-112">Die erste Version einer Beispieldaten-Modellkonfiguration wurde erstellt und nach LCS veröffentlicht während der Prozedur "Hochladen einer ER-Konfiguration nach Lifecycle Services".</span><span class="sxs-lookup"><span data-stu-id="add1a-112">The first version of a sample data model configuration has been created and published to LCS during the “Upload an ER configuration into Lifecycle Services” procedure.</span></span> <span data-ttu-id="add1a-113">In dieser Prozedur löschen Sie diese Version der ER-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="add1a-113">In this procedure, you will delete this version of the ER configuration.</span></span> <span data-ttu-id="add1a-114">Diese Version einer Beispieldatmodellkonfiguration wird später von LCS importiert.</span><span class="sxs-lookup"><span data-stu-id="add1a-114">This version of a sample data model configuration will be imported later from LCS.</span></span>  
2. <span data-ttu-id="add1a-115">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="add1a-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="add1a-116">Wählen Sie die Version dieser Konfiguration aus, die sich im Status "Freigegeben" befindet.</span><span class="sxs-lookup"><span data-stu-id="add1a-116">Select the version of this configuration that is in the ‘Shared’ status.</span></span> <span data-ttu-id="add1a-117">Dieser Status gibt an, dass die Konfiguration nach LCS veröffentlicht wurde.</span><span class="sxs-lookup"><span data-stu-id="add1a-117">This status indicates that the configuration has been published to LCS.</span></span>  
3. <span data-ttu-id="add1a-118">Klicken Sie auf "Status ändern".</span><span class="sxs-lookup"><span data-stu-id="add1a-118">Click Change status.</span></span>
4. <span data-ttu-id="add1a-119">Klicken Sie auf "Nicht fortsetzen".</span><span class="sxs-lookup"><span data-stu-id="add1a-119">Click Discontinue.</span></span>
    * <span data-ttu-id="add1a-120">Ändern Sie den Status der ausgewählten Version von "Freigegeben" zu "Nicht mehr verfügbar", um sie zur Löschung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="add1a-120">Change the status of the selected version from ‘Shared’ to ‘Discontinued’ to make it available for deletion.</span></span>  
5. <span data-ttu-id="add1a-121">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="add1a-121">Click OK.</span></span>
6. <span data-ttu-id="add1a-122">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="add1a-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="add1a-123">Wählen Sie die Version dieser Konfiguration aus, die den Status "Nicht mehr verfügbar" hat.</span><span class="sxs-lookup"><span data-stu-id="add1a-123">Select the version of this configuration that has a status of ‘Discontinued’.</span></span>  
7. <span data-ttu-id="add1a-124">Klicken Sie auf Löschen.</span><span class="sxs-lookup"><span data-stu-id="add1a-124">Click Delete.</span></span>
8. <span data-ttu-id="add1a-125">Klicken Sie auf "Ja".</span><span class="sxs-lookup"><span data-stu-id="add1a-125">Click Yes.</span></span>
    * <span data-ttu-id="add1a-126">Beachten Sie, dass die einzige Entwurfsversion 2 der ausgewählten Datenmodellkonfiguration verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="add1a-126">Note that the only draft version 2 of the selected data model configuration is available.</span></span>  
9. <span data-ttu-id="add1a-127">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="add1a-127">Close the page.</span></span>

## <a name="import-a-shared-version-of-data-model-configuration-from-lcs"></a><span data-ttu-id="add1a-128">Importieren Sie eine freigegebene Version der Datenmodellkonfiguration von LCS</span><span class="sxs-lookup"><span data-stu-id="add1a-128">Import a shared version of data model configuration from LCS</span></span>
1. <span data-ttu-id="add1a-129">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="add1a-129">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="add1a-130">Öffnen Sie die Liste von Repositorys für den Konfigurationsanbieter "Litware, Inc."</span><span class="sxs-lookup"><span data-stu-id="add1a-130">Open the list of repositories for the ‘Litware, Inc.’</span></span> <span data-ttu-id="add1a-131">zu öffnen Konfigurationsanbieter.</span><span class="sxs-lookup"><span data-stu-id="add1a-131">configuration provider.</span></span>  
2. <span data-ttu-id="add1a-132">Klicken Sie auf Repositorys.</span><span class="sxs-lookup"><span data-stu-id="add1a-132">Click Repositories.</span></span>
3. <span data-ttu-id="add1a-133">Klicken Sie auf "Öffnen".</span><span class="sxs-lookup"><span data-stu-id="add1a-133">Click Open.</span></span>
    * <span data-ttu-id="add1a-134">Wählen Sie das LCS-Repository aus und öffnen Sie es.</span><span class="sxs-lookup"><span data-stu-id="add1a-134">Select the LCS repository and open it.</span></span>  
4. <span data-ttu-id="add1a-135">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="add1a-135">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="add1a-136">Wählen Sie die erste Version der "Beispielmodellkonfiguration" in der Versionsliste aus.</span><span class="sxs-lookup"><span data-stu-id="add1a-136">Select the first version of the 'Sample model configuration' in the versions list.</span></span>  
5. <span data-ttu-id="add1a-137">Klicken Sie auf Import.</span><span class="sxs-lookup"><span data-stu-id="add1a-137">Click Import.</span></span>
6. <span data-ttu-id="add1a-138">Klicken Sie auf "Ja".</span><span class="sxs-lookup"><span data-stu-id="add1a-138">Click Yes.</span></span>
    * <span data-ttu-id="add1a-139">Bestätigen Sie den Import der ausgewählten Version von LCS.</span><span class="sxs-lookup"><span data-stu-id="add1a-139">Confirm the import of the selected version from LCS .</span></span>  
    * <span data-ttu-id="add1a-140">Beachten Sie, dass die Informationsmeldung (über dem Formular) den erfolgreichen Abschluss des Importvorgangs der ausgewählten Version bestätigt.</span><span class="sxs-lookup"><span data-stu-id="add1a-140">Note that the information message (above the form) confirms the successful completion of the import of the selected version.</span></span>  
7. <span data-ttu-id="add1a-141">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="add1a-141">Close the page.</span></span>
8. <span data-ttu-id="add1a-142">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="add1a-142">Close the page.</span></span>
9. <span data-ttu-id="add1a-143">Klicken Sie auf "Konfigurationen".</span><span class="sxs-lookup"><span data-stu-id="add1a-143">Click Configurations.</span></span>
10. <span data-ttu-id="add1a-144">Wählen Sie "Beispielmodellkonfiguration" in der Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="add1a-144">In the tree, select 'Sample model configuration'.</span></span>
11. <span data-ttu-id="add1a-145">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="add1a-145">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="add1a-146">Wählen Sie die Version dieser Konfiguration aus, die den Status "Freigegeben" hat.</span><span class="sxs-lookup"><span data-stu-id="add1a-146">Select the version of this configuration that has a status of ‘Shared’.</span></span>  
    * <span data-ttu-id="add1a-147">Beachten Sie, dass die freigegebene Version 1 der ausgewählten Datenmodellkonfiguration jetzt verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="add1a-147">Note that the shared version 1 of the selected data model configuration is available now as well.</span></span>  

