---
title: Synchronisieren Sie Projektaufgaben aus der der Project Service Automation
description: "Dieses Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Produkte direkt aus Microsoft Dynamics 365 for Project Service Automation in Dynamics 365 for Finance and Operations zu synchronisieren."
author: KimANelson
manager: AnnBe
ms.date: 04/02/2018
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
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: 399b519ab0da4de405aeb06f3e7f4bf29a6c5cc3
ms.openlocfilehash: 89df0d99d780441ad08cd6bff3e1fd203694eb8e
ms.contentlocale: de-de
ms.lasthandoff: 05/30/2018

---

# <a name="synchronize-project-tasks-from-project-service-automation-directly-to-project-activities-in-finance-and-operations"></a><span data-ttu-id="d6619-103">Synchronisieren Sie Projektaufgaben von der Project Service Automation direkt in Projektaktivitäten von Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d6619-103">Synchronize project tasks from Project Service Automation directly to project activities in Finance and Operations</span></span>

<span data-ttu-id="d6619-104">Dieses Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Produkte direkt aus Microsoft Dynamics 365 for Project Service Automation in Dynamics 365 for Finance and Operations zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="d6619-104">This topic describes the template and underlying task that is used to synchronize project tasks directly from Microsoft Dynamics 365 for Project Service Automation to Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="d6619-105">Projektaufgaben-Integration, Ausgabenbuchungskategorien, StundensDynamics 365 for Finance and Operations version 8.0.chätzungen, Ausgabenenschätzungen und Funktionenssperre sind in Dynamics 365 for Finance and Operations Version 8.0 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d6619-105">Project tasks integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in Dynamics 365 for Finance and Operations version 8.0.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="d6619-106">Datenfluss für Project Service Automation zu Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d6619-106">Data flow for Project Service Automation to Finance and Operations</span></span>

<span data-ttu-id="d6619-107">Die Project Service Automation zu Finance and Operations Integrationslösung nutzt die  Datenenintegrationsfunktion, um Daten in Instanzen von Project Service Automation und Finance and Operations zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="d6619-107">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="d6619-108">Die Integrationsvorlage, die der Datenenintegrationsfunktion verfügbar ist, ermöglicht den Datenfluss zu Projektaufgaben von Project Service Automation zu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d6619-108">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="d6619-109">Die folgende Abbildung zeigt, wie Daten als Teil der Integration zwischen Project Service Automation und Finance and Operations synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="d6619-109">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="d6619-110">[![Datenfluss für Project Service Automation Integration mit Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="d6619-110">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="d6619-111">Vorlage und Aufgabe</span><span class="sxs-lookup"><span data-stu-id="d6619-111">Template and task</span></span>

<span data-ttu-id="d6619-112">Wenn Sie auf die Vorlage im Microsoft PowerApps Admin Center zugreifen möchten, wählen Sie **Projekte**, und klicken Sie dann in der oberen rechten Ecke auf **Neues Projekt**, um die öffentliche Vorlage auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="d6619-112">To access the template, in the Microsoft PowerApps Admin Center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="d6619-113">Die folgenden Vorlagen und zugrunde liegenden Aufgaben werden verwendet, um Projektaufgaben von Project Service Automation zu Finance and Operations zu synchronisieren:</span><span class="sxs-lookup"><span data-stu-id="d6619-113">The following template and underlying task is used to synchronize project tasks from Project Service Automation to Finance and Operations:</span></span>

<span data-ttu-id="d6619-114">-**Bezeichnung der Vorlage in der Datenintegration:** Projektaufgabe (PSA zu Fin and Ops) - **Name der Aufgabe im Projekt** Projektaufgaben</span><span class="sxs-lookup"><span data-stu-id="d6619-114">-**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops) -**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="d6619-115">Vor der Synchronisierung von Projektaufgaben müssen Sie zunächst Projektverträge und Projekte synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="d6619-115">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="d6619-116">Entitätssatz</span><span class="sxs-lookup"><span data-stu-id="d6619-116">Entity set</span></span>

|<span data-ttu-id="d6619-117">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="d6619-117">Project Service Automation</span></span>               | <span data-ttu-id="d6619-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d6619-118">Finance and Operations</span></span>                |
|-----------------------------------------|---------------------------------------|
| <span data-ttu-id="d6619-119">Projekt-Aufgaben</span><span class="sxs-lookup"><span data-stu-id="d6619-119">Project Tasks</span></span>                           | <span data-ttu-id="d6619-120">Integrationsentität für Projektaufgabe.</span><span class="sxs-lookup"><span data-stu-id="d6619-120">Integration entity for project task.</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="d6619-121">Entitätsfluss</span><span class="sxs-lookup"><span data-stu-id="d6619-121">Entity flow</span></span>

<span data-ttu-id="d6619-122">Projektaufgaben werden in der Project Service Automation verwaltet und nach Finance and Operations als Projektaktivitäten verwaltet.</span><span class="sxs-lookup"><span data-stu-id="d6619-122">Project tasks are managed in Project Service Automation, and they are synchronized to Finance and Operations as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="d6619-123">Voraussetzungen und Zuordnungseinrichtung</span><span class="sxs-lookup"><span data-stu-id="d6619-123">Prerequisites and mapping setup</span></span>

<span data-ttu-id="d6619-124">Vor der Synchronisierung von Projektaufgaben müssen Sie zunächst Projektverträge und Projekte synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="d6619-124">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="d6619-125">Powerabfrage</span><span class="sxs-lookup"><span data-stu-id="d6619-125">Power Query</span></span>

<span data-ttu-id="d6619-126">Sie müssen Microsoft Power Abfrage verwenden, um Daten zu filtern, wenn die Bedingungen erfüllt sind:</span><span class="sxs-lookup"><span data-stu-id="d6619-126">You must use Microsoft Power Query to filter data if these conditions are met:</span></span>

- <span data-ttu-id="d6619-127">Sie haben Ressourcen spezifische Datensätze innerhalb der Projektaufgabe.</span><span class="sxs-lookup"><span data-stu-id="d6619-127">You have resource specific records within a project task.</span></span>

<span data-ttu-id="d6619-128">Wenn Sie Power Query verwenden möchten, folgen Sie diesen Richtlinien:</span><span class="sxs-lookup"><span data-stu-id="d6619-128">If you must use Power Query, follow these guidelines:</span></span>

- <span data-ttu-id="d6619-129">Die Projektaufgaben der Vorlage (PSA zu Fin and Opss) weist einen der Standardfilter auf, um bestimmte Datensätze der Ressource aus einer Projektaufgabe auszuschließen mithilfe des Filters im **IsLineTask** auf **Falsch**.</span><span class="sxs-lookup"><span data-stu-id="d6619-129">The Project tasks (PSA to Fin and Ops) template has a default filter to exclude resource specific records from within a project task by setting the filter on the **IsLineTask** to **False**.</span></span> <span data-ttu-id="d6619-130">Wenn Sie Ihre eigenen Vorlagen erstellen, müssen Sie diese dem Filter hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d6619-130">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="d6619-131">Vorlagenzuordnung in Datenintegration</span><span class="sxs-lookup"><span data-stu-id="d6619-131">Template mapping in Data integration</span></span>

<span data-ttu-id="d6619-132">Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenaufgabenzuordnung im Datenintegrator.</span><span class="sxs-lookup"><span data-stu-id="d6619-132">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="d6619-133">Die Zuordnung zeigt, welche Feldinformationen von Project Service Automation zu Finance and Operations synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="d6619-133">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="d6619-134">[![Vorlagenzuordnung](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="d6619-134">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>


