---
title: Optimieren der Leistung durch Planung von Batch-Jobs außerhalb der Geschäftszeiten
description: In diesem Thema wird erläutert, wie einige Leistungsprobleme mit Microsoft Dynamics 365 Human Resources behoben werden, indem Sie Batch-Jobs mit langer Laufzeit außerhalb der Geschäftszeiten planen.
author: andreabichsel
ms.date: 06/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: a5aeaeb7311d87a154882b7058b6da430900bd56
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053466"
---
# <a name="optimize-performance-by-scheduling-batch-jobs-after-hours"></a><span data-ttu-id="196e1-103">Optimieren der Leistung durch Planung von Batch-Jobs außerhalb der Geschäftszeiten</span><span class="sxs-lookup"><span data-stu-id="196e1-103">Optimize performance by scheduling batch jobs after hours</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="issue"></a><span data-ttu-id="196e1-104">Abgang</span><span class="sxs-lookup"><span data-stu-id="196e1-104">Issue</span></span>

<span data-ttu-id="196e1-105">In Microsoft Dynamics 365 Human Resources können Leistungsprobleme auftreten, wenn Batch-Jobs mit langer Laufzeit während der üblichen Geschäftszeiten ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="196e1-105">Microsoft Dynamics 365 Human Resources can experience performance issues if long-running batch jobs run during typical business hours.</span></span>

## <a name="resolution"></a><span data-ttu-id="196e1-106">Lösung</span><span class="sxs-lookup"><span data-stu-id="196e1-106">Resolution</span></span>

<span data-ttu-id="196e1-107">Planen Sie die folgenden Batch-Jobs außerhalb der Geschäftszeiten.</span><span class="sxs-lookup"><span data-stu-id="196e1-107">Schedule the following batch jobs during off hours.</span></span> <span data-ttu-id="196e1-108">Wir empfehlen außerdem, die Frequenz von häufig ausgeführten Batch-Jobs zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="196e1-108">We also recommend reviewing the frequency of batch jobs that run frequently.</span></span> <span data-ttu-id="196e1-109">Reduzieren Sie nach Möglichkeit die Wiederholung des Batch-Jobs.</span><span class="sxs-lookup"><span data-stu-id="196e1-109">If possible, reduce the recurrence of the batch job.</span></span> <span data-ttu-id="196e1-110">In vielen Fällen ist die Standardfrequenz ausreichend.</span><span class="sxs-lookup"><span data-stu-id="196e1-110">In many cases, the default frequency is sufficient.</span></span>

<span data-ttu-id="196e1-111">Die folgenden Batch-Jobs sollten nachts oder nach Geschäftsschluss ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="196e1-111">The following batch jobs should run at night or after hours.</span></span> <span data-ttu-id="196e1-112">Überprüfen Sie unbedingt die Zeitzone für diese sich wiederholenden Batch-Jobs.</span><span class="sxs-lookup"><span data-stu-id="196e1-112">Be sure to check the time zone for these recurring batch jobs.</span></span> <span data-ttu-id="196e1-113">Einige Batch-Jobs verwenden möglicherweise Pacific Standard Time (PST).</span><span class="sxs-lookup"><span data-stu-id="196e1-113">Some batch jobs might use Pacific Standard Time (PST).</span></span>

| <span data-ttu-id="196e1-114">Stapelverarbeitungsauftrag</span><span class="sxs-lookup"><span data-stu-id="196e1-114">Batch job</span></span> | <span data-ttu-id="196e1-115">Standardhäufigkeit</span><span class="sxs-lookup"><span data-stu-id="196e1-115">Default occurrence</span></span> |
| --- | --- |
| <span data-ttu-id="196e1-116">Bereinigung des Batch-Jobs</span><span class="sxs-lookup"><span data-stu-id="196e1-116">Batch job history cleanup</span></span> | <span data-ttu-id="196e1-117">1 Mal pro Monat</span><span class="sxs-lookup"><span data-stu-id="196e1-117">1 time per month</span></span> |
| <span data-ttu-id="196e1-118">Stagingbereinigung exportieren</span><span class="sxs-lookup"><span data-stu-id="196e1-118">Export staging cleanup</span></span> | <span data-ttu-id="196e1-119">1 Mal pro Tag</span><span class="sxs-lookup"><span data-stu-id="196e1-119">1 time per day</span></span> |
| <span data-ttu-id="196e1-120">Fehlende Anforderungssynchronisierung bei der Common Data Service-Integration</span><span class="sxs-lookup"><span data-stu-id="196e1-120">Common Data Service integration missed request sync</span></span> | <span data-ttu-id="196e1-121">1 Mal pro Tag</span><span class="sxs-lookup"><span data-stu-id="196e1-121">1 time per day</span></span> |
| <span data-ttu-id="196e1-122">Job zur Datenbankkomprimierung, der außerhalb der Geschäftszeiten regelmäßig ausgeführt werden muss</span><span class="sxs-lookup"><span data-stu-id="196e1-122">Database compression system job that needs to run regularly during off hours</span></span> | <span data-ttu-id="196e1-123">1 Mal pro Tag</span><span class="sxs-lookup"><span data-stu-id="196e1-123">1 time per day</span></span> |
| <span data-ttu-id="196e1-124">Job zur erneuten Erstellung des Datenbankindex, der außerhalb der Geschäftszeiten regelmäßig ausgeführt werden muss</span><span class="sxs-lookup"><span data-stu-id="196e1-124">Database index rebuild system job that needs to run regularly during off hours</span></span> | <span data-ttu-id="196e1-125">1 Mal pro Tag</span><span class="sxs-lookup"><span data-stu-id="196e1-125">1 time per day</span></span> |

1. <span data-ttu-id="196e1-126">Wählen Sie in Human Resources **Systemverwaltung** aus.</span><span class="sxs-lookup"><span data-stu-id="196e1-126">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="196e1-127">Verwenden Sie die Leiste **Suchen**, um nach einem der oben genannten Batch-Jobs zu suchen.</span><span class="sxs-lookup"><span data-stu-id="196e1-127">In the **Search** bar, search for one of the above batch jobs.</span></span>

3. <span data-ttu-id="196e1-128">Wählen Sie **Im Hintergrund ausführen** aus und wählen Sie dann **Wiederholung** aus.</span><span class="sxs-lookup"><span data-stu-id="196e1-128">Select **Run in the background**, and then select **Recurrence**.</span></span>

   ![Wiederholung festlegen](media/talent-batch-history-cleanup-recurrence.png)

4. <span data-ttu-id="196e1-130">Legen Sie unter **Wiederholung definieren** das **Startdatum** und die **Startzeit** für die Wiederholungen außerhalb der Geschäftszeiten oder an Wochenenden fest.</span><span class="sxs-lookup"><span data-stu-id="196e1-130">Under **Define recurrence**, set the **Start date** and **Start time** to occur during off hours or the weekend.</span></span> <span data-ttu-id="196e1-131">Wählen Sie **Kein Enddatum** aus.</span><span class="sxs-lookup"><span data-stu-id="196e1-131">Select **No end date**.</span></span> 

   ![Startdatum und -zeit der Wiederholung definieren](media/talent-batch-history-cleanup-define-recurrence.png)

5. <span data-ttu-id="196e1-133">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="196e1-133">Select **OK**.</span></span>

6. <span data-ttu-id="196e1-134">Ändern Sie gegebenenfalls weitere Parameter unter **Im Hintergrund ausführen** und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="196e1-134">If needed, change any other parameters under **Run in the background**, and then select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="196e1-135">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="196e1-135">Additional resources</span></span>

[<span data-ttu-id="196e1-136">Leistung mit automatischen Bereinigungsaufgaben optimieren</span><span class="sxs-lookup"><span data-stu-id="196e1-136">Optimize performance with auto cleanup tasks</span></span>](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]