---
title: Project Service Automation
description: "Diese Lösung verwendet Datenintegration, um Daten über Instanzen von Microsoft Dynamics 365 for Finance and Operations und Microsoft Dynamics 365 for Project Service Automation über Common Data Service (CDC) zu synchronisieren."
author: KimANelson
manager: AnnBe
ms.date: 11/27/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 0ad9e6ba7fe8dd915681da8e671ff210de887b1e
ms.contentlocale: de-de
ms.lasthandoff: 05/29/2018

---

# <a name="project-service-automation"></a><span data-ttu-id="0562b-103">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="0562b-103">Project Service Automation</span></span>

<span data-ttu-id="0562b-104">Die Project Service Automation zur Finance and Operations Integrationslösung nutzt die Datenintegrationsfunktion, um Daten über Instanzen von Microsoft Dynamics 365 for Finance and Operations und Microsoft Dynamics 365 for Project Service Automation über Common Data Service (CDC) zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="0562b-104">The Project Service Automation to Finance and Operations integration solution uses the Data Integration feature to synchronize data across instances of Microsoft Dynamics 365 for Finance and Operations and Microsoft Dynamics 365 for Project Service Automation via the Common Data Service (CDS).</span></span> <span data-ttu-id="0562b-105">Die Integrationsvorlagen, die in der Daten-Integrationsfunktion verfügbar sind, aktivieren den Fluss von Projekten, von Projektverträgen, Projektvertragspositionen, Projektvertragszeilen-Meilensteinen,  Projektaufgaben, Ausgabenbuchungskategorien, Stundenschätzungen und von Ausgabenschätzungen von Project Service Automation zu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0562b-105">The integration templates that are available with the Data Integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance and Operations.</span></span>

> [!NOTE] 
> <span data-ttu-id="0562b-106">Wenn Sie Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.0 verwenden, müssen Sie auch KB 4074835 installieren.</span><span class="sxs-lookup"><span data-stu-id="0562b-106">If you are using Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="0562b-107">Dadurch wird es Ihnen ermöglicht, Festpreisprojekte zu integrieren.</span><span class="sxs-lookup"><span data-stu-id="0562b-107">This will allow you to integrate fixed price projects.</span></span>
>
> <span data-ttu-id="0562b-108">Wenn Sie Dynamics 365 for Finance and Operations 8,0 verwenden, sind Sie in der Lage, Projektaufgaben-Integration, Ausgabenbuchungskategorien, Stundenschätzungen, Ausgabenenschätzungen und Funktionenssperre zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="0562b-108">If you are using Dynamics 365 for Finance and Operations version 8.0, you will be able to use project tasks integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
>
> <span data-ttu-id="0562b-109">Wenn Sie Dynamics 365 for Finance and Operations 8.0.1 verwenden, sind Sie in der Lage, aktuelle Verhältnisse zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="0562b-109">If you are using Dynamics 365 for Finance and Operations version 8.0.1, you will be able to synchronize actuals.</span></span>
>
> <span data-ttu-id="0562b-110">Wenn Sie Dynamics 365  for Finance and Operations, Enterprise edition 7.3.0,verwenden und KB 4132657 und 4132660 KB einrichten, sind Sie in der Lage, die Vorlagen zu verwenden, um Projektaufgaben,  Ausgabentransaktionskategorien, geschätzte Stunden, geschätzte Ausgaben und aktuelle Kosten zu integrieren und die Funktionalitätssperre zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="0562b-110">If you are using Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="0562b-111">Wenn Sie die Buchhaltungsverteilungen zurücksetzen müssen, wird empfohlen, dass Sie auch 4131710 KB einrichten.</span><span class="sxs-lookup"><span data-stu-id="0562b-111">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

<span data-ttu-id="0562b-112">Bevor Sie Project Service Automation mit Finance and Operations integrieren können, müssen Sie auch die Project Service Automation mit Finance and Operations integrieren.</span><span class="sxs-lookup"><span data-stu-id="0562b-112">Before you can integrate Project Service Automation with Finance and Operations, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="0562b-113">Weitere Informationen finden Sie unter Project Service Automation Integrationsparameter.</span><span class="sxs-lookup"><span data-stu-id="0562b-113">For more information, see Project Service Automation integration parameters.</span></span>

<span data-ttu-id="0562b-114">Diese Integrationslösung bietet direkte Synchronisation in den folgenden Szenarien:</span><span class="sxs-lookup"><span data-stu-id="0562b-114">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="0562b-115">Verwalten Sie Projektverträge in der Project Service Automation und synchronisieren Sie direkt von der Project Service Automation zu Finance Finanzen und Arbeitsgänge.</span><span class="sxs-lookup"><span data-stu-id="0562b-115">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="0562b-116">Erstellen Sie Projektverträge in der Project Service Automation und synchronisieren Sie direkt von der Project Service Automation zu Finance</span><span class="sxs-lookup"><span data-stu-id="0562b-116">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="0562b-117">Verwalten Sie Projektvertragszeilen in der Project Service Automation und synchronisieren Sie direkt von der Project Service Automation zu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0562b-117">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="0562b-118">Verwalten Sie Projektvertragszeiln-Meilensteine in der Project Service Automation und synchronisieren Sie direkt von der Project Service Automation zu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0562b-118">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="0562b-119">Verwalten Sie Projektaufgaben in der Project Service Automation und synchronisieren Sie direkt von der Project Service Automation zu Finance Finanzen und Arbeitsgänge.</span><span class="sxs-lookup"><span data-stu-id="0562b-119">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="0562b-120">Verwalten Sie Ausgabentransaktionskategorien in Finance and Operations und synchronisieren Sie direkt von Finance and Operations zu Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="0562b-120">Maintain expense transaction categories in Finance and Operations, and synchronize them directly from Finance and Operations to Project Service Automation.</span></span>
- <span data-ttu-id="0562b-121">Erstellen Sie Projektstundenschätzungen in der Project Service Automation und synchronisieren Sie direkt von der Project Service Automation zu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0562b-121">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="0562b-122">Erstellen Sie Projektausgabenschätzungen in der Project Service Automation und synchronisieren Sie direkt von der Project Service Automation zu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0562b-122">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="0562b-123">Datensynchronisierung</span><span class="sxs-lookup"><span data-stu-id="0562b-123">Data synchronization</span></span>
<span data-ttu-id="0562b-124">Die folgende Abbildung zeigt, wie Daten als Teil der Integration zwischen Project Service Automation und Finance and Operations synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="0562b-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="0562b-125">Nicht alle Vorlagen sind derzeit verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0562b-125">Not all templates are currently available.</span></span> <span data-ttu-id="0562b-126">Vorlagen werden freigegeben, wenn diese abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="0562b-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="0562b-127">[![Project Service Automation Integration mit Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="0562b-127">[![Project Service Automation integration with Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="0562b-128">Systemanforderungen für Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="0562b-128">System requirements for Finance and Operations</span></span>

<span data-ttu-id="0562b-129">Um die Project Service Automation zu Finance and Operations Integrationslösung zu verwenden, müssen Sie Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition mit 7.3 Plattformaktualisierung 12 oder später einrichten.</span><span class="sxs-lookup"><span data-stu-id="0562b-129">To use the Project Service Automation to Finance and Operations integration solution, you must install Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 with platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="0562b-130">Systemanforderungen für Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="0562b-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="0562b-131">Um die Project Service Automation zu Finance and Operations-Integrationslösung zu verwenden, müssen Sie die folgenden Komponenten installieren:</span><span class="sxs-lookup"><span data-stu-id="0562b-131">To use the Project Service Automation to Finance and Operations integration solution, you must install the following components:</span></span>

- <span data-ttu-id="0562b-132">Microsoft Dynamics 365 for Project Service Automation Version 9.0.0.0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="0562b-132">Microsoft Dynamics 365 for Project Service Automation version 9.0.0.0 or later.</span></span>
- <span data-ttu-id="0562b-133">Interessent zu Bargeld-Lösung für Dynamics 365 for Sales, Version 1.14.0.0 (v14) oder höher.</span><span class="sxs-lookup"><span data-stu-id="0562b-133">Prospect to cash solution for Dynamics 365 for Sales, version 1.14.0.0 (v14) or later.</span></span>
- <span data-ttu-id="0562b-134">roject Service Automation to Operations-Lösung für Dynamics 365 for Project Service Automation Version 1.0.0.0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="0562b-134">Project Service Automation to Operations solution for Dynamics 365 for Project Service Automation version 1.0.0.0 or later.</span></span>

## <a name="install-the-project-service-automation-to-finance-and-operations-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="0562b-135">Installieren Sie die Project Service Automation to Finance and Operations Integrationslösung in Project Service Automation Instanz</span><span class="sxs-lookup"><span data-stu-id="0562b-135">Install the Project Service Automation to Finance and Operations integration solution in your Project Service Automation instance</span></span>



