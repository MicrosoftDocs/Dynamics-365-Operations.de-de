---
title: Wartungszeitplan
description: In diesem Thema wird der Wartungszeitplan in Asset Management erläutert.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 780b633af04c38705f8321d19924f3802b2d5c67
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875672"
---
# <a name="maintenance-schedule"></a><span data-ttu-id="d7b2d-103">Wartungszeitplan</span><span class="sxs-lookup"><span data-stu-id="d7b2d-103">Maintenance schedule</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="d7b2d-104">Der Wartungszeitplan enthält eine Liste aller zu erwartenden vorbeugenden Wartungspläne, Wartungsanfragen und durchzuführenden Wartungsdurchgängen. Einige Zeitplanpositionen wurden möglicherweise in Arbeitsaufträge umgewandelt.</span><span class="sxs-lookup"><span data-stu-id="d7b2d-104">The maintenance schedule contains a list of all the expected preventive maintenance plans, maintenance requests, and maintenance rounds to be carried out. Some schedule lines may have been converted to work orders.</span></span>

<span data-ttu-id="d7b2d-105">Die vier Wartungszeitplanansichten unterscheiden sich leicht, je nachdem, welche Wartungszeitplanpositionen Sie sehen möchten.</span><span class="sxs-lookup"><span data-stu-id="d7b2d-105">The four maintenance schedule views are slightly different, depending on which maintenance schedule lines you want to see.</span></span>

| <span data-ttu-id="d7b2d-106">Menüoption</span><span class="sxs-lookup"><span data-stu-id="d7b2d-106">Menu item</span></span>                  | <span data-ttu-id="d7b2d-107">Beschreibung des Inhalts</span><span class="sxs-lookup"><span data-stu-id="d7b2d-107">Description of contents</span></span>                                                                                                                                             |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7b2d-108">Gesamter Wartungszeitplan</span><span class="sxs-lookup"><span data-stu-id="d7b2d-108">All maintenance schedule</span></span>       | <span data-ttu-id="d7b2d-109">Alle Wartungszeitplanpositionen werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d7b2d-109">All maintenance schedule lines are shown.</span></span>     |
| <span data-ttu-id="d7b2d-110">Mein Anlagenzeitplan</span><span class="sxs-lookup"><span data-stu-id="d7b2d-110">My asset schedule</span></span>        | <span data-ttu-id="d7b2d-111">Alle Wartungseinteilungen, die Anlagen enthalten, die auf funktionalen Standorten installiert sind, mit denen Sie als Arbeitskraft in Bezug stehen (eingerichtet in [Wartungsarbeiter und Arbeitskraftgruppen](../setup-for-objects/workers-and-worker-groups.md)), werden in dieser Liste angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d7b2d-111">All maintenance schedule lines containing assets installed on functional locations to which you are related as a worker (set up in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md)) are shown in this list.</span></span> |
| <span data-ttu-id="d7b2d-112">Offene Wartungszeitplanpositionen</span><span class="sxs-lookup"><span data-stu-id="d7b2d-112">Open maintenance schedule lines</span></span> | <span data-ttu-id="d7b2d-113">Wartungszeitplanpositionen mit dem Status „Erstellt“ - d.h. sie wurden noch nicht in einen Arbeitsauftrag umgewandelt oder verworfen - werden in dieser Liste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d7b2d-113">Maintenance schedule lines with status "Created" - meaning they have not yet been converted to a work order or discarded - are shown in this list.</span></span>                                            |
| <span data-ttu-id="d7b2d-114">Wartungszeitplanpools öffnen</span><span class="sxs-lookup"><span data-stu-id="d7b2d-114">Open maintenance schedule pools</span></span> | <span data-ttu-id="d7b2d-115">Wartungszeitplanpositionen, die sich auf einen Arbeitsauftragspool beziehen, werden in dieser Liste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d7b2d-115">Maintenance schedule lines related to a work order pool are shown in this list.</span></span>                                                                                                                  |

>[!NOTE]
><span data-ttu-id="d7b2d-116">Wenn eine Wartungszeitplanposition in mehreren Arbeitsauftragspools enthalten ist (siehe [Arbeitsauftragspools](../work-orders/work-order-pools.md)), wird für jeden Pool ein Datensatz in **Wartungszeitplanpools öffnen** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d7b2d-116">If a maintenance schedule line is included in several work order pools (refer to [Work order pools](../work-orders/work-order-pools.md)), one record is shown for each pool in **Open maintenance schedule pools**.</span></span> <span data-ttu-id="d7b2d-117">Dies erfolgt, um Filtermöglichkeiten für Arbeitsauftragspools zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="d7b2d-117">This is done to optimize filtering options on work order pools.</span></span>

<span data-ttu-id="d7b2d-118">Um einen Wartungsplan zu öffnen:</span><span class="sxs-lookup"><span data-stu-id="d7b2d-118">To open a maintenance schedule:</span></span>

1. <span data-ttu-id="d7b2d-119">Klicken Sie auf **Anlagenverwaltung** > **Allgemein** > **Wartungszeitplan** > **Alle Wartungszeitpläne** oder **Wartungszeitplanpositionen öffnen** oder **Wartungszeitplanpools öffnen**.</span><span class="sxs-lookup"><span data-stu-id="d7b2d-119">Click **Asset management** > **Common** > **Maintenance schedule** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools**.</span></span>

2. <span data-ttu-id="d7b2d-120">Um den Wartungszeitplan zu aktualisieren, klicken Sie **Wartungsplan** oder **Wartungsdurchgang**.</span><span class="sxs-lookup"><span data-stu-id="d7b2d-120">To update the maintenance schedule, click **Maintenance plan** or **Maintenance rounds**.</span></span> 

3. <span data-ttu-id="d7b2d-121">Sie können eine Wartungszeitplanposition bearbeiten, indem Sie sie auswählen und auf **Bearbeiten** klicken.</span><span class="sxs-lookup"><span data-stu-id="d7b2d-121">You can edit a maintenance schedule line by selecting it and clicking **Edit**.</span></span> <span data-ttu-id="d7b2d-122">So können Sie beispielsweise den Servicelevel oder die Arbeitskraft, die für den Auftrag zuständig sind, aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="d7b2d-122">For example, you can easily update the service level or the worker responsible for the job.</span></span> <span data-ttu-id="d7b2d-123">Sie können nur Wartungsplanpositionen bearbeiten, die noch nicht mit einen Arbeitsauftrag verknüpft wurden.</span><span class="sxs-lookup"><span data-stu-id="d7b2d-123">You can only edit maintenance schedule lines that have not yet been connected to a work order.</span></span>

4. <span data-ttu-id="d7b2d-124">Sie können eine Wartungsplanposition löschen, indem Sie sie auf der Listenseite auswählen und **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="d7b2d-124">You can delete a maintenance schedule line by selecting it in the list page and clicking **Delete**.</span></span>

5. <span data-ttu-id="d7b2d-125">Sie können eine Wartungsplanposition verwerfen, indem Sie sie auf der Listenseite auswählen und **Verwerfen**.</span><span class="sxs-lookup"><span data-stu-id="d7b2d-125">You can discard a maintenance schedule line by selecting it in the list page and clicking **Discard**.</span></span> <span data-ttu-id="d7b2d-126">Diese Funktion ist z.B. sinnvoll, wenn eine Anlage einen 2.000 km Wartungsplan und einen 10.000 km Wartungsplan hat.</span><span class="sxs-lookup"><span data-stu-id="d7b2d-126">This function is useful if, for example, an asset has a 2,000 km maintenance plan and a 10,000 km maintenance plan.</span></span> <span data-ttu-id="d7b2d-127">Dann können Sie die aus dem 2.000 km Wartungsplan angelegte Position verwerfen, wenn sie mit 10.000 km, 20.000 km, 30.000 km usw. übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="d7b2d-127">Then, you may want to discard the line created from the 2,000 km maintenance plan when it coincides with 10,000 km, 20,000 km, 30,000 km, and so on.</span></span> <span data-ttu-id="d7b2d-128">Wenn Sie eine Wartungszeitplanposition zu einem Wartungsplan verwerfen, wird diese Position nie wieder angezeigt, wenn dieser Wartungsplan terminiert wird.</span><span class="sxs-lookup"><span data-stu-id="d7b2d-128">If you discard a maintenance schedule line related to a maintenance plan, that line will never again appear when that maintenance plan is scheduled.</span></span>

6. <span data-ttu-id="d7b2d-129">Sie können unter **Alle Wartungszeitpläne** eine Reihe von Wartungszeitplanpositionen auswählen und auf **Arbeitsauftragspool** klicken, wenn Sie möchten, dass alle ausgewählten Positionen in den gleichen Arbeitsauftragspool aufgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="d7b2d-129">You can select a number of maintenance schedule lines in **All maintenance schedule** and click **Work order pool**, if you want all selected lines to be included in the same work order pool.</span></span>

7. <span data-ttu-id="d7b2d-130">Sie können eine Anzahl von Wartungszeitplanpositionen in **Alle Wartungszeitpläne** oder **Wartungszeitplanpositionen öffnen** oder **Wartungszeitplanpools öffnen** auswählen und auf **Zeitplan anpassen** klicken, wenn Sie die gleichen Anpassungen auf mehreren Positionen vornehmen möchten.</span><span class="sxs-lookup"><span data-stu-id="d7b2d-130">You can select a number of maintenance schedule lines in **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools** and click **Adjust schedule** if you want to make the same adjustments on several lines.</span></span> <span data-ttu-id="d7b2d-131">Sie können die erwarteten Beginn- und Endtermine, Servicelevel und die verantwortliche Wartungsarbeitergruppe oder den verantwortlichen Wartungsmitarbeiter in Bezug auf die ausgewählten Wartungszeitplanpositionen ändern.</span><span class="sxs-lookup"><span data-stu-id="d7b2d-131">You can change expected start and end dates, service level, and the responsible maintenance worker group or responsible maintenance worker related to the selected maintenance schedule lines.</span></span>

- <span data-ttu-id="d7b2d-132">Wenn eine Wartungszeitplanposition einem Arbeitsauftrag zugeordnet wurde, wird die Arbeitsauftragskennung im Feld **Arbeitsauftrag** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d7b2d-132">When a maintenance schedule line has been related to a work order, the work order ID will be displayed in the **Work order** field.</span></span>  
- <span data-ttu-id="d7b2d-133">In der Detailansicht **Alle Anlagen** > Inforegister **Anlagenwartungspläne** können Sie Wartungspläne für die Anlage auswählen.</span><span class="sxs-lookup"><span data-stu-id="d7b2d-133">In **All assets** details view > **Asset maintenance plans** FastTab, you can select maintenance plans for the asset.</span></span> <span data-ttu-id="d7b2d-134">Wenn Sie später eine Wartungsplanposition löschen, die sich auf eine Anlage in **Alle Anlagen** bezieht, löschen Sie auch automatisch alle Wartungszeitplanpositionen mit dem Status „Erstellt“, die aufgrund dieses Wartungsplans angelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="d7b2d-134">Later, if you delete a maintenance plan line related to an asset in **All assets**, you also automatically delete all maintenance schedule lines with status "Created" that have been created based on that maintenance plan.</span></span> <span data-ttu-id="d7b2d-135">Siehe auch [Erstellen einer Anlage](../objects/create-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="d7b2d-135">See also [Create an asset](../objects/create-an-object.md).</span></span>

<span data-ttu-id="d7b2d-136">Die folgende Abbildung zeigt die Listenseite **Alle Wartungszeitpläne** an.</span><span class="sxs-lookup"><span data-stu-id="d7b2d-136">The figure below shows the **All maintenance schedule** list page.</span></span>

![Abbildung 1](media/16-preventive-maintenance.png)
