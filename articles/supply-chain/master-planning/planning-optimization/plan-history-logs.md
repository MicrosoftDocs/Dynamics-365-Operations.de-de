---
title: Anzeigen der Planhistorie und der Planungsprotokolle
description: In diesem Thema wird erläutert, wie Sie die Historie von Planungsjobs anzeigen, die durch die Funktionalität der Planungsoptimierung ausgelöst werden.
author: ChristianRytt
ms.date: 10/30/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MPSPlanRegenerationJobList, MPSPlanRegenerationJobLogs
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: d7bba084b03f8698c8bf31d171d5e4e486ed06ad
ms.sourcegitcommit: a7649b361ec54b49c0e9ee1c1c63a8815f320225
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187246"
---
# <a name="view-plan-history-and-planning-logs"></a><span data-ttu-id="bfbdc-103">Anzeigen der Planhistorie und der Planungsprotokolle</span><span class="sxs-lookup"><span data-stu-id="bfbdc-103">View plan history and planning logs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bfbdc-104">In diesem Thema wird erläutert, wie Sie die Historie von Planungsjobs anzeigen, die durch die Funktionalität der Planungsoptimierung in Microsoft Dynamics 365 Supply Chain Management ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="bfbdc-104">This topic explains how to view the history of planning jobs that are triggered by the Planning Optimization functionality in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="bfbdc-105">Um die Historie für einen Plan anzuzeigen, öffnen Sie den Plan, indem Sie zu **Masterplanung** \> **Einrichtung** \> **Pläne** \> **Masterpläne** gehen und **Historie** auswählen.</span><span class="sxs-lookup"><span data-stu-id="bfbdc-105">To view the history for a plan, open the plan by going to **Master planning** \> **Setup** \> **Plans** \> **Master plans** and selecting **History**.</span></span> <span data-ttu-id="bfbdc-106">Die Historie listet alle Aufträge für den ausgewählten Plan auf.</span><span class="sxs-lookup"><span data-stu-id="bfbdc-106">The history lists all the jobs for the selected plan.</span></span> <span data-ttu-id="bfbdc-107">Die Liste enthält erledigte und aktive Aufträge.</span><span class="sxs-lookup"><span data-stu-id="bfbdc-107">The list includes completed and active jobs.</span></span>

<span data-ttu-id="bfbdc-108">Die Historie der Jobs für die Masterplanungsläufe der Planungsoptimierung enthält nur bis zu 60 Datensätze pro Masterplan.</span><span class="sxs-lookup"><span data-stu-id="bfbdc-108">The history of jobs for Planning Optimization master planning runs keeps only up to 60 records per master plan.</span></span> <span data-ttu-id="bfbdc-109">Wenn Sie eine neue Hauptplanungsberechnung ausführen, wird der früheste Historiensatz dieses Plans gelöscht.</span><span class="sxs-lookup"><span data-stu-id="bfbdc-109">Whenever you run a new master planning calculation, that plan's earliest history record is deleted.</span></span>

<span data-ttu-id="bfbdc-110">Sie können nicht nur die Startzeit und den Status der Jobs einsehen, sondern auch das Protokoll für einen bestimmten Job anzeigen.</span><span class="sxs-lookup"><span data-stu-id="bfbdc-110">In addition to seeing the start time and status of jobs, you can view the log for a specific job.</span></span> <span data-ttu-id="bfbdc-111">Das Protokoll enthält zusätzliche Informationen und Warnungen.</span><span class="sxs-lookup"><span data-stu-id="bfbdc-111">The log includes additional information and warnings.</span></span> <span data-ttu-id="bfbdc-112">Nicht alle Aufträge haben ein Protokoll.</span><span class="sxs-lookup"><span data-stu-id="bfbdc-112">Not all jobs have a log.</span></span> <span data-ttu-id="bfbdc-113">Um das Protokoll für einen Auftrag anzuzeigen, wählen Sie **Protokoll**.</span><span class="sxs-lookup"><span data-stu-id="bfbdc-113">To view the log for a job, select **Log**.</span></span> <span data-ttu-id="bfbdc-114">Log-Einträge werden nur 30 Tage nach Auftragsende gespeichert und danach automatisch gelöscht.</span><span class="sxs-lookup"><span data-stu-id="bfbdc-114">Log entries are only stored for 30 days after the date the job finished, after that they are automatically deleted.</span></span>

## <a name="related-resources"></a><span data-ttu-id="bfbdc-115">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="bfbdc-115">Related resources</span></span>

- [<span data-ttu-id="bfbdc-116">Übersicht zur Planungsoptimierung</span><span class="sxs-lookup"><span data-stu-id="bfbdc-116">Planning Optimization overview</span></span>](planning-optimization-overview.md)
- [<span data-ttu-id="bfbdc-117">Erste Schritte mit der Planungsoptimierung</span><span class="sxs-lookup"><span data-stu-id="bfbdc-117">Get started with Planning Optimization</span></span>](get-started.md)
- [<span data-ttu-id="bfbdc-118">Planungsoptimierung Fit-Analyse</span><span class="sxs-lookup"><span data-stu-id="bfbdc-118">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)
- [<span data-ttu-id="bfbdc-119">Filter auf einen Plan anwenden</span><span class="sxs-lookup"><span data-stu-id="bfbdc-119">Apply filters to a plan</span></span>](plan-filters.md)
- [<span data-ttu-id="bfbdc-120">Abbrechen eines Planungsauftrags</span><span class="sxs-lookup"><span data-stu-id="bfbdc-120">Cancel a planning job</span></span>](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]