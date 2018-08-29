---
title: Synchronisieren von Projektaufgaben direkt aus Project Service Automation mit Finance and Operations
description: "Dieses Thema erläutert die Vorlage und die zugrunde liegende Aufgabe, die verwendet werden, um Projektaufgaben direkt aus Microsoft Dynamics 365 for Project Service Automation mit Microsoft Dynamics 365 for Finance and Operations zu synchronisieren."
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 53e4eab0d455af4ac1e17754f31d46458db742c3
ms.contentlocale: de-de
ms.lasthandoff: 08/08/2018

---

# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="cc96c-103">Synchronisieren von Projektaufgaben direkt aus Project Service Automation mit Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cc96c-103">Synchronize project tasks directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="cc96c-104">Dieses Thema erläutert die Vorlage und die zugrunde liegende Aufgabe, die verwendet werden, um Projektaufgaben direkt aus Microsoft Dynamics 365 for Project Service Automation mit Microsoft Dynamics 365 for Finance and Operations zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="cc96c-104">This topic describes the template and underlying task that are used to synchronize project tasks directly from Microsoft Dynamics 365 for Project Service Automation to Microsoft Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE]
> - <span data-ttu-id="cc96c-105">Projektaufgabenintegration, Ausgabentransaktionskategorien, Stundenvorkalkulationen, Ausgabenvorkalkulationen und Funktionalitätssperren sind in Microsoft Dynamics 365 for Finance and Operations, Version 8.0, verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cc96c-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in Microsoft Dynamics 365 for Finance and Operations version 8.0.</span></span>
> - <span data-ttu-id="cc96c-106">Wenn Sie Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.0 verwenden, nachdem Sie KB 4132657 und 4132660 KB installiert haben, sind Sie in der Lage, die Vorlagen zu verwenden, um Projektaufgaben, Ausgabentransaktionskategorien, geschätzte Stunden, geschätzte Ausgaben und Ist-Werte zu integrieren und die Funktionalitätssperre zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="cc96c-106">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="cc96c-107">Wenn Sie die Buchhaltungsverteilungen zurücksetzen müssen, wird empfohlen, dass Sie auch KB 4131710 installieren.</span><span class="sxs-lookup"><span data-stu-id="cc96c-107">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>
> - <span data-ttu-id="cc96c-108">Integration von Ist-Werten ist in Microsoft Dynamics 365 for Finance and Operations, Version 8.0.1 oder höher, verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cc96c-108">Actuals integration is available in Microsoft Dynamics 365 for Finance and Operations version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="cc96c-109">Datenfluss für Project Service Automation zu Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cc96c-109">Data flow for Project Service Automation to Finance and Operations</span></span>

<span data-ttu-id="cc96c-110">Die Project Service Automation zu Finance and Operations Integrationslösung nutzt die Datenenintegrationsfunktion, um Daten in Instanzen von Project Service Automation und Finance and Operations zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="cc96c-110">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="cc96c-111">Die Integrationsvorlage, die der Datenenintegrationsfunktion verfügbar ist, ermöglicht den Datenfluss zu Projektaufgaben von Project Service Automation zu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="cc96c-111">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="cc96c-112">Die folgende Abbildung zeigt, wie Daten als Teil der Integration zwischen Project Service Automation und Finance and Operations synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="cc96c-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="cc96c-113">[![Datenfluss für Project Service Automation Integration mit Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="cc96c-113">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="cc96c-114">Vorlage und Aufgabe</span><span class="sxs-lookup"><span data-stu-id="cc96c-114">Template and task</span></span>

<span data-ttu-id="cc96c-115">Wenn Sie auf die Vorlage im Microsoft PowerApps Admin Center zugreifen möchten, wählen Sie **Projekte** aus, und klicken Sie dann in der oberen rechten Ecke auf **Neues Projekt**, um öffentliche Vorlagen auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="cc96c-115">To access the template, in the Microsoft PowerApps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="cc96c-116">Die folgende Vorlage und zugrunde liegende Aufgabe werden verwendet, um Projektaufgaben von Project Service Automation mit Finance and Operations zu synchronisieren:</span><span class="sxs-lookup"><span data-stu-id="cc96c-116">The following template and underlying task are used to synchronize project tasks from Project Service Automation to Finance and Operations:</span></span>

- <span data-ttu-id="cc96c-117">**Name der Vorlage in der Datenintegration:** Projektaufgaben (PSA zu Fin und Ops)</span><span class="sxs-lookup"><span data-stu-id="cc96c-117">**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="cc96c-118">**Name der Aufgabe im Projekt:** Projektaufgaben</span><span class="sxs-lookup"><span data-stu-id="cc96c-118">**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="cc96c-119">Vor der Synchronisierung von Projektaufgaben müssen Sie zunächst Projektverträge und Projekte synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="cc96c-119">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="cc96c-120">Entitätssatz</span><span class="sxs-lookup"><span data-stu-id="cc96c-120">Entity set</span></span>

| <span data-ttu-id="cc96c-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="cc96c-121">Project Service Automation</span></span> | <span data-ttu-id="cc96c-122">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cc96c-122">Finance and Operations</span></span>              |
|----------------------------|-------------------------------------|
| <span data-ttu-id="cc96c-123">Projekt-Aufgaben</span><span class="sxs-lookup"><span data-stu-id="cc96c-123">Project Tasks</span></span>              | <span data-ttu-id="cc96c-124">Integrationsentität für Projektaufgabe</span><span class="sxs-lookup"><span data-stu-id="cc96c-124">Integration entity for project task</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="cc96c-125">Entitätsfluss</span><span class="sxs-lookup"><span data-stu-id="cc96c-125">Entity flow</span></span>

<span data-ttu-id="cc96c-126">Projektaufgaben werden in der Project Service Automation verwaltet und nach Finance and Operations als Projektaktivitäten verwaltet.</span><span class="sxs-lookup"><span data-stu-id="cc96c-126">Project tasks are managed in Project Service Automation, and they are synchronized to Finance and Operations as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="cc96c-127">Voraussetzungen und Zuordnungseinrichtung</span><span class="sxs-lookup"><span data-stu-id="cc96c-127">Prerequisites and mapping setup</span></span>

<span data-ttu-id="cc96c-128">Vor der Synchronisierung von Projektaufgaben müssen Sie zunächst Projektverträge und Projekte synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="cc96c-128">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="cc96c-129">Powerabfrage</span><span class="sxs-lookup"><span data-stu-id="cc96c-129">Power Query</span></span>

<span data-ttu-id="cc96c-130">Sie müssen Microsoft Power Query für Excel verwenden, um Daten zu filtern, wenn diese Bedingung erfüllt ist:</span><span class="sxs-lookup"><span data-stu-id="cc96c-130">You must use Microsoft Power Query for Excel to filter data if this condition is met:</span></span>

- <span data-ttu-id="cc96c-131">Sie haben ressourcenspezifische Datensätze in einer Projektaufgabe.</span><span class="sxs-lookup"><span data-stu-id="cc96c-131">You have resource-specific records in a project task.</span></span>

<span data-ttu-id="cc96c-132">Wenn Sie Power Query verwenden müssen, folgen Sie dieser Richtlinie:</span><span class="sxs-lookup"><span data-stu-id="cc96c-132">If you must use Power Query, follow this guideline:</span></span>

- <span data-ttu-id="cc96c-133">Die Projektaufgabenvorlage (PSA zu Fin and Opss) weist einen Standardfilter auf, der ressourcenspezifisce Datensätze aus einer Projektaufgabe ausschließt, indem der Filter in **IsLineTask** auf **Falsch** festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="cc96c-133">The Project tasks (PSA to Fin and Ops) template has a default filter that excludes resource-specific records from a project task by setting the filter on **IsLineTask** to **False**.</span></span> <span data-ttu-id="cc96c-134">Wenn Sie Ihre eigenen Vorlagen erstellen, müssen Sie diese dem Filter hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="cc96c-134">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="cc96c-135">Vorlagenzuordnung in Datenintegration</span><span class="sxs-lookup"><span data-stu-id="cc96c-135">Template mapping in Data integration</span></span>

<span data-ttu-id="cc96c-136">Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenaufgabenzuordnung im Datenintegrator.</span><span class="sxs-lookup"><span data-stu-id="cc96c-136">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="cc96c-137">Die Zuordnung zeigt, welche Feldinformationen von Project Service Automation zu Finance and Operations synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="cc96c-137">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="cc96c-138">[![Vorlagenzuordnung](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="cc96c-138">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>

