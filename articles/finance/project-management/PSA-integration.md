---
title: Project Service Automation – Übersicht
description: Dieses Thema bietet Informationen über die Integrationslösung Dynamics 365 Project Service Automation zu Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 31d72591041f8d8cc327aa7c6578c15731ba13c5
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250552"
---
# <a name="project-service-automation-overview"></a><span data-ttu-id="c6876-103">Project Service Automation – Übersicht</span><span class="sxs-lookup"><span data-stu-id="c6876-103">Project Service Automation overview</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c6876-104">Die Integrationslösung Project Service Automation to Finance nutzt die Datenintegrationsfunktion, um Daten über Instanzen von Dynamics 365 Finance und Dynamics 365 Project Service Automation über Common Data Service zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="c6876-104">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Dynamics 365 Finance and Dynamics 365 Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="c6876-105">Die Integrationsvorlagen, die mit der Datenintegrationsfunktion verfügbar sind, ermöglichen den Fluss von Projekten, Projektverträgen, Projektvertragspositionen, Projektvertragspositions-Meilensteinen, Projektaufgaben, Ausgabenbuchungskategorien, Stundenvorkalkulationen und Ausgabenvorkalkulationen von Project Service Automation zu Finance.</span><span class="sxs-lookup"><span data-stu-id="c6876-105">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="c6876-106">Wenn Sie Version7.3.0 verwenden, müssen Sie KB 4074835 installieren.</span><span class="sxs-lookup"><span data-stu-id="c6876-106">If you're using version 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="c6876-107">Dadurch wird es Ihnen dann ermöglicht, Festpreisprojekte zu integrieren.</span><span class="sxs-lookup"><span data-stu-id="c6876-107">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="c6876-108">Wenn Sie Version 7.3.0 verwenden und Gebührenbuchungen aus Project Service Automation übernehmen, müssen Sie KB 4345320 installieren, um diese Gebühren in der Projektrechnung einzuschließen.</span><span class="sxs-lookup"><span data-stu-id="c6876-108">If you're using version 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="c6876-109">Wenn Sie Version 8.0 verwenden, sind Sie in der Lage, Projektaufgaben-Integration, Ausgabenbuchungskategorien, Stundenschätzungen, Ausgabenenschätzungen und Funktionenssperre zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="c6876-109">If you're using version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="c6876-110">Wenn Sie Version 8.0.1 oder höher verwenden, sind Sie in der Lage, Ist-Werte zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="c6876-110">If you're using version 8.0.1 or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="c6876-111">Bevor Sie Project Service Automation Finance integrieren können, müssen Sie auch die Project Service Automation mit Finance and Operations integrieren.</span><span class="sxs-lookup"><span data-stu-id="c6876-111">Before you can integrate Project Service Automation Finance, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="c6876-112">Weitere Informationen finden Sie unter [Project Service Automation-Integrationsparameter](PSA-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c6876-112">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="c6876-113">Diese Integrationslösung bietet direkte Synchronisation in den folgenden Szenarien:</span><span class="sxs-lookup"><span data-stu-id="c6876-113">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="c6876-114">Verwalten Sie Projektverträge in der Project Service Automation und synchronisieren Sie direkt von der Project Service Automation zu Finance.</span><span class="sxs-lookup"><span data-stu-id="c6876-114">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="c6876-115">Erstellen Sie Projektverträge in der Project Service Automation und synchronisieren Sie direkt von der Project Service Automation zu Finance</span><span class="sxs-lookup"><span data-stu-id="c6876-115">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="c6876-116">Verwalten Sie Projektvertragspositionen in der Project Service Automation und synchronisieren Sie direkt von der Project Service Automation zu Finance.</span><span class="sxs-lookup"><span data-stu-id="c6876-116">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="c6876-117">Verwalten Sie Projektvertragspositionsmeilensteine in der Project Service Automation und synchronisieren Sie direkt von der Project Service Automation zu Finance.</span><span class="sxs-lookup"><span data-stu-id="c6876-117">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="c6876-118">Verwalten Sie Projektaufträge in der Project Service Automation und synchronisieren Sie direkt von der Project Service Automation zu Finance.</span><span class="sxs-lookup"><span data-stu-id="c6876-118">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="c6876-119">Verwalten Sie Ausgabentransaktionskategorien in Finance und synchronisieren Sie direkt von Finance zu Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="c6876-119">Maintain expense transaction categories in Finance, and synchronize them directly from Finance to Project Service Automation.</span></span>
- <span data-ttu-id="c6876-120">Erstellen Sie Projektstundenschätzungen in der Project Service Automation und synchronisieren Sie direkt von der Project Service Automation zu Finance.</span><span class="sxs-lookup"><span data-stu-id="c6876-120">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="c6876-121">Erstellen Sie Projektausgabenschätzungen in der Project Service Automation und synchronisieren Sie direkt von der Project Service Automation zu Finance.</span><span class="sxs-lookup"><span data-stu-id="c6876-121">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="c6876-122">Erstellen Sie Projektzeit, Ausgaben und Gebühren-Ist-Werte in Project Service Automation und erstellen Sie Projekttransaktionen in der Project Service Automation-Integrationserfassung, damit sie in Finance gebucht werden können.</span><span class="sxs-lookup"><span data-stu-id="c6876-122">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="c6876-123">Datensynchronisierung</span><span class="sxs-lookup"><span data-stu-id="c6876-123">Data synchronization</span></span>

<span data-ttu-id="c6876-124">Die folgende Abbildung zeigt, wie Daten als Teil der Integration zwischen Project Service Automation und Finance synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="c6876-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance.</span></span>

> [!NOTE]
> <span data-ttu-id="c6876-125">Nicht alle Vorlagen sind derzeit verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c6876-125">Not all templates are currently available.</span></span> <span data-ttu-id="c6876-126">Vorlagen werden freigegeben, wenn diese abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="c6876-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="c6876-127">[![Project Service Automation-Integration in Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="c6876-127">[![Project Service Automation integration with Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance"></a><span data-ttu-id="c6876-128">Systemanforderungen für Finance</span><span class="sxs-lookup"><span data-stu-id="c6876-128">System requirements for Finance</span></span>

<span data-ttu-id="c6876-129">Um die Project Service Automation zu Finance Integrationslösung zu verwenden, müssen Sie , Enterprise Edition 7.3 mit Plattformaktualisierung 12 oder höher einrichten.</span><span class="sxs-lookup"><span data-stu-id="c6876-129">To use the Project Service Automation to Finance integration solution, you must install Enterprise edition 7.3 with Platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="c6876-130">Systemanforderungen für Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="c6876-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="c6876-131">Um die Project Service Automation zu Finance-Integrationslösung zu verwenden, müssen Sie die folgenden Komponenten installieren:</span><span class="sxs-lookup"><span data-stu-id="c6876-131">To use the Project Service Automation to Finance integration solution, you must install the following components:</span></span>

- <span data-ttu-id="c6876-132">Dynamics 365 Project Service Automation Version 9.0.0.0 oder höher</span><span class="sxs-lookup"><span data-stu-id="c6876-132">Dynamics 365 Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="c6876-133">Interessent zu Bargeld-Lösung für Dynamics 365 Sales, Version 1.14.0.0 (v14) oder höher.</span><span class="sxs-lookup"><span data-stu-id="c6876-133">Prospect to cash solution for Dynamics 365 Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="c6876-134">Project Service Automation zu Finance-Integrationslösung für Dynamics 365 Project Service Automation Version1.0.0.0 oder höher</span><span class="sxs-lookup"><span data-stu-id="c6876-134">Project Service Automation to Finance solution for Dynamics 365 Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="c6876-135">Installieren Sie die Project Service Automation zu Finance Integrationslösung in Project Service Automation Instanz</span><span class="sxs-lookup"><span data-stu-id="c6876-135">Install the Project Service Automation to Finance integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="c6876-136">Laden Sie die Project Service Automation-zu-Finance-Integrationslösung von [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016) herunter, und befolgen Sie die Anweisungen, die in der Lösung enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="c6876-136">Download the Project Service Automation to Finance integration solution from [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>
