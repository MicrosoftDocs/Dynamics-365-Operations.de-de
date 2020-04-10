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
ms.openlocfilehash: 67e09e3187ac49e12727116f55066b64a386e2de
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142385"
---
# <a name="er-import-a-configuration-from-lifecycle-services"></a><span data-ttu-id="d6159-103">ER Import einer Konfiguration von Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="d6159-103">ER Import a configuration from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d6159-104">In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Systemadministratorrolle oder der Rolle "Entwickler für elektronische Berichterstellung" eine neue Konfiguration für "Elektronische Berichterstellung (ER)" erstellen kann und sie nach Microsoft Lifecycle Services (LCS) hochladen kann.</span><span class="sxs-lookup"><span data-stu-id="d6159-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can import a new version of an Electronic reporting (ER) configuration from Microsoft Lifecycle Services (LCS).</span></span>

<span data-ttu-id="d6159-105">In diesem Beispiel wählen Sie die gewünschte Version der ER-Konfiguration und importieren das Beispielunternehmen, Litware, Inc. Diese Schritte können in einem beliebigen Unternehmen ausgeführt werden, da ER-Konfigurationsanbieter unter allen Unternehmen geteilt werden.</span><span class="sxs-lookup"><span data-stu-id="d6159-105">In this example, you will select the desired version of the ER configuration and import it for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="d6159-106">Um diese Schritte abzuschließen, müssen Sie zunächst die Schritte in der Prozedur „Eine ER-Konfiguration nach Lifecycle Services hochladen“ abschließen.</span><span class="sxs-lookup"><span data-stu-id="d6159-106">To complete these steps, you must first complete the steps in the "Upload an ER configuration into Lifecycle Services" procedure.</span></span> <span data-ttu-id="d6159-107">Zugriff auf LCS ist auch für den Abschluss dieser Schritte erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d6159-107">Access to LCS is also required for completion of these steps.</span></span>

1. <span data-ttu-id="d6159-108">Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="d6159-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="d6159-109">Klicken Sie auf "Konfigurationen".</span><span class="sxs-lookup"><span data-stu-id="d6159-109">Click Configurations.</span></span>

## <a name="delete-a-shared-version-of-data-model-configuration"></a><span data-ttu-id="d6159-110">Löschen Sie eine freigegebene Version der Datenmodellkonfiguration</span><span class="sxs-lookup"><span data-stu-id="d6159-110">Delete a shared version of data model configuration</span></span>
1. <span data-ttu-id="d6159-111">Wählen Sie "Beispielmodellkonfiguration" in der Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="d6159-111">In the tree, select 'Sample model configuration'.</span></span>
    * <span data-ttu-id="d6159-112">Die erste Version einer Beispieldaten-Modellkonfiguration wurde erstellt und nach LCS veröffentlicht während der Prozedur „Hochladen einer ER-Konfiguration nach Lifecycle Services“.</span><span class="sxs-lookup"><span data-stu-id="d6159-112">The first version of a sample data model configuration has been created and published to LCS during the "Upload an ER configuration into Lifecycle Services" procedure.</span></span> <span data-ttu-id="d6159-113">In dieser Prozedur löschen Sie diese Version der ER-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="d6159-113">In this procedure, you will delete this version of the ER configuration.</span></span> <span data-ttu-id="d6159-114">Diese Version einer Beispieldatmodellkonfiguration wird später von LCS importiert.</span><span class="sxs-lookup"><span data-stu-id="d6159-114">This version of a sample data model configuration will be imported later from LCS.</span></span>  
2. <span data-ttu-id="d6159-115">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="d6159-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d6159-116">Wählen Sie die Version dieser Konfiguration aus, die sich im Status „Freigegeben“ befindet.</span><span class="sxs-lookup"><span data-stu-id="d6159-116">Select the version of this configuration that is in the 'Shared' status.</span></span> <span data-ttu-id="d6159-117">Dieser Status gibt an, dass die Konfiguration nach LCS veröffentlicht wurde.</span><span class="sxs-lookup"><span data-stu-id="d6159-117">This status indicates that the configuration has been published to LCS.</span></span>  
3. <span data-ttu-id="d6159-118">Klicken Sie auf "Status ändern".</span><span class="sxs-lookup"><span data-stu-id="d6159-118">Click Change status.</span></span>
4. <span data-ttu-id="d6159-119">Klicken Sie auf "Nicht fortsetzen".</span><span class="sxs-lookup"><span data-stu-id="d6159-119">Click Discontinue.</span></span>
    * <span data-ttu-id="d6159-120">Ändern Sie den Status der ausgewählten Version von „Freigegeben“ zu „Nicht mehr verfügbar“, um sie zur Löschung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="d6159-120">Change the status of the selected version from 'Shared' to 'Discontinued' to make it available for deletion.</span></span>  
5. <span data-ttu-id="d6159-121">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="d6159-121">Click OK.</span></span>
6. <span data-ttu-id="d6159-122">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="d6159-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d6159-123">Wählen Sie die Version dieser Konfiguration aus, die den Status „Nicht mehr verfügbar“ hat.</span><span class="sxs-lookup"><span data-stu-id="d6159-123">Select the version of this configuration that has a status of 'Discontinued'.</span></span>  
7. <span data-ttu-id="d6159-124">Klicken Sie auf Löschen.</span><span class="sxs-lookup"><span data-stu-id="d6159-124">Click Delete.</span></span>
8. <span data-ttu-id="d6159-125">Klicken Sie auf „Ja“.</span><span class="sxs-lookup"><span data-stu-id="d6159-125">Click Yes.</span></span>
    * <span data-ttu-id="d6159-126">Beachten Sie, dass die einzige Entwurfsversion 2 der ausgewählten Datenmodellkonfiguration verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="d6159-126">Note that the only draft version 2 of the selected data model configuration is available.</span></span>  
9. <span data-ttu-id="d6159-127">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="d6159-127">Close the page.</span></span>

## <a name="import-a-shared-version-of-data-model-configuration-from-lcs"></a><span data-ttu-id="d6159-128">Importieren Sie eine freigegebene Version der Datenmodellkonfiguration von LCS</span><span class="sxs-lookup"><span data-stu-id="d6159-128">Import a shared version of data model configuration from LCS</span></span>
1. <span data-ttu-id="d6159-129">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="d6159-129">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="d6159-130">Öffnen Sie die Liste von Repositorys für den Konfigurationsanbieter „Litware, Inc.“</span><span class="sxs-lookup"><span data-stu-id="d6159-130">Open the list of repositories for the 'Litware, Inc.'</span></span> <span data-ttu-id="d6159-131">zu öffnen Konfigurationsanbieter.</span><span class="sxs-lookup"><span data-stu-id="d6159-131">configuration provider.</span></span>  
2. <span data-ttu-id="d6159-132">Klicken Sie auf Repositorys.</span><span class="sxs-lookup"><span data-stu-id="d6159-132">Click Repositories.</span></span>
3. <span data-ttu-id="d6159-133">Klicken Sie auf "Öffnen".</span><span class="sxs-lookup"><span data-stu-id="d6159-133">Click Open.</span></span>
    * <span data-ttu-id="d6159-134">Wählen Sie das LCS-Repository aus und öffnen Sie es.</span><span class="sxs-lookup"><span data-stu-id="d6159-134">Select the LCS repository and open it.</span></span>  
4. <span data-ttu-id="d6159-135">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="d6159-135">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="d6159-136">Wählen Sie die erste Version der "Beispielmodellkonfiguration" in der Versionsliste aus.</span><span class="sxs-lookup"><span data-stu-id="d6159-136">Select the first version of the 'Sample model configuration' in the versions list.</span></span>  
5. <span data-ttu-id="d6159-137">Klicken Sie auf Import.</span><span class="sxs-lookup"><span data-stu-id="d6159-137">Click Import.</span></span>
6. <span data-ttu-id="d6159-138">Klicken Sie auf "Ja".</span><span class="sxs-lookup"><span data-stu-id="d6159-138">Click Yes.</span></span>
    * <span data-ttu-id="d6159-139">Bestätigen Sie den Import der ausgewählten Version von LCS.</span><span class="sxs-lookup"><span data-stu-id="d6159-139">Confirm the import of the selected version from LCS .</span></span>  
    * <span data-ttu-id="d6159-140">Beachten Sie, dass die Informationsmeldung (über dem Formular) den erfolgreichen Abschluss des Importvorgangs der ausgewählten Version bestätigt.</span><span class="sxs-lookup"><span data-stu-id="d6159-140">Note that the information message (above the form) confirms the successful completion of the import of the selected version.</span></span>  
7. <span data-ttu-id="d6159-141">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="d6159-141">Close the page.</span></span>
8. <span data-ttu-id="d6159-142">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="d6159-142">Close the page.</span></span>
9. <span data-ttu-id="d6159-143">Klicken Sie auf "Konfigurationen".</span><span class="sxs-lookup"><span data-stu-id="d6159-143">Click Configurations.</span></span>
10. <span data-ttu-id="d6159-144">Wählen Sie "Beispielmodellkonfiguration" in der Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="d6159-144">In the tree, select 'Sample model configuration'.</span></span>
11. <span data-ttu-id="d6159-145">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="d6159-145">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d6159-146">Wählen Sie die Version dieser Konfiguration aus, die den Status „Freigegeben“ hat.</span><span class="sxs-lookup"><span data-stu-id="d6159-146">Select the version of this configuration that has a status of 'Shared'.</span></span>  
    * <span data-ttu-id="d6159-147">Beachten Sie, dass die freigegebene Version 1 der ausgewählten Datenmodellkonfiguration jetzt verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="d6159-147">Note that the shared version 1 of the selected data model configuration is available now as well.</span></span>  

