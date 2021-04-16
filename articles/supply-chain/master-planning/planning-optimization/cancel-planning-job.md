---
title: Abbrechen eines Planungsauftrags
description: In diesem Thema wird erläutert, wie ein aktiver Planungsauftrag, der die Planungsoptimierungsfunktionalität verwendet, abgebrochen werden kann.
author: ChristianRytt
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: e9cf4902251c3c2b93af12a8ad9bd571930ef769
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833328"
---
# <a name="cancel-a-planning-job"></a><span data-ttu-id="58ad8-103">Abbrechen eines Planungsvorgangs</span><span class="sxs-lookup"><span data-stu-id="58ad8-103">Cancel a planning job</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="58ad8-104">In Microsoft Dynamics 365 Supply Chain Management können Sie einen aktiven Planungsauftrag, der die Planungsoptimierungsfunktionalität verwendet, abbrechen.</span><span class="sxs-lookup"><span data-stu-id="58ad8-104">In Microsoft Dynamics 365 Supply Chain Management, you can cancel an active planning job that uses the Planning optimization functionality.</span></span> <span data-ttu-id="58ad8-105">Wenn Sie im Dialogfenster **Abbrechen** wählen, wenn ein Planungsoptimierungsjob direkt von der Benutzeroberfläche aus (nicht im Hintergrund) ausgelöst wird, wird der Planungsoptimierungsjob nicht abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="58ad8-105">When you select **Cancel** in the dialog box when a Planning optimization job is triggered directly from the user interface (not in the background), this will not cancel the Planning optimization job.</span></span> <span data-ttu-id="58ad8-106">Selbst wenn Sie eine Warnung wie „Vorgang abgebrochen“ erhalten, müssen Sie die folgenden Schritte durchführen, um einen Planungsjob mit Planungsoptimierung abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="58ad8-106">Even if you receive a warning such as “Operation canceled”, you will still need to use the following steps to cancel a planning job with Planning optimization.</span></span>


<span data-ttu-id="58ad8-107">Um einen aktiven Planungseinzelvorgang zu stornieren, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="58ad8-107">To cancel an active planning job, follow these steps.</span></span> 

> [!NOTE]
> <span data-ttu-id="58ad8-108">Es können nur aktive Aufträge abgebrochen werden.</span><span class="sxs-lookup"><span data-stu-id="58ad8-108">Only active jobs can be canceled.</span></span>

1. <span data-ttu-id="58ad8-109">Wechseln Sie zu **Produktprogrammplanung \> Einrichtung \> Pläne**.</span><span class="sxs-lookup"><span data-stu-id="58ad8-109">Go to **Master planning \> Setup \> Plans**.</span></span>
2. <span data-ttu-id="58ad8-110">Wählen Sie einen entsprechenden Plan für den Planungslauf aus.</span><span class="sxs-lookup"><span data-stu-id="58ad8-110">Select an appropriate plan for the planning run.</span></span>
3. <span data-ttu-id="58ad8-111">Wählen Sie **Verlauf** aus.</span><span class="sxs-lookup"><span data-stu-id="58ad8-111">Select **History**.</span></span>
4. <span data-ttu-id="58ad8-112">Wählen Sie den zu stornierenden Planungseinzelvorgang aus.</span><span class="sxs-lookup"><span data-stu-id="58ad8-112">Select the planning job to cancel.</span></span>
5. <span data-ttu-id="58ad8-113">Wählen Sie **Abbrechen** aus.</span><span class="sxs-lookup"><span data-stu-id="58ad8-113">Select **Cancel**.</span></span>

<span data-ttu-id="58ad8-114">Der Status des Einzelvorgangs lautet **Wird storniert**, bis der Planungsoptimierungsdienst bestätigt, dass der Auftrag storniert wurde.</span><span class="sxs-lookup"><span data-stu-id="58ad8-114">The job status will be **Canceling** until the Planning Optimization service confirms that the job has been canceled.</span></span> <span data-ttu-id="58ad8-115">Der Status wird anschließend in **Storniert** geändert.</span><span class="sxs-lookup"><span data-stu-id="58ad8-115">The status will then be changed to **Canceled**.</span></span>

> [!NOTE]
> <span data-ttu-id="58ad8-116">Um Statusänderungen anzuzeigen, müssen Sie die Seite aktualisieren, indem Sie die Schaltfläche **Aktualisieren** auswählen.</span><span class="sxs-lookup"><span data-stu-id="58ad8-116">To see status changes, you must refresh the page by selecting the **Refresh** button.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="58ad8-117">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="58ad8-117">Additional resources</span></span>

[<span data-ttu-id="58ad8-118">Übersicht zur Planungsoptimierung</span><span class="sxs-lookup"><span data-stu-id="58ad8-118">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="58ad8-119">Erste Schritte mit der Planungsoptimierung</span><span class="sxs-lookup"><span data-stu-id="58ad8-119">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="58ad8-120">Planungsoptimierung Fit-Analyse</span><span class="sxs-lookup"><span data-stu-id="58ad8-120">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="58ad8-121">Planhistorie und Planungsprotokolle anzeigen</span><span class="sxs-lookup"><span data-stu-id="58ad8-121">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="58ad8-122">Filter auf einen Plan anwenden</span><span class="sxs-lookup"><span data-stu-id="58ad8-122">Apply filters to a plan</span></span>](plan-filters.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]