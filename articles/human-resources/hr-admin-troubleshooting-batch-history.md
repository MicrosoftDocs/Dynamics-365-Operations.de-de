---
title: Optimieren der Leistung mit automatischen Bereinigungsaufgaben
description: In diesem Artikel wird erläutert, wie einige Leistungsprobleme mit Microsoft Dynamics 365 Human Resources behoben werden, indem Sie den Verlauf der Stapelverarbeitungsaufträge bereinigen.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 6a9e94e282aa8f101b42c1378ef21c6c1fe0477e
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053490"
---
# <a name="optimize-performance-with-auto-cleanup-tasks"></a><span data-ttu-id="8d318-103">Optimieren Sie die Leistung mit automatischen Bereinigungsaufgaben</span><span class="sxs-lookup"><span data-stu-id="8d318-103">Optimize performance with auto cleanup tasks</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="8d318-104">**Abgang**</span><span class="sxs-lookup"><span data-stu-id="8d318-104">**Issue**</span></span>

<span data-ttu-id="8d318-105">Microsoft Dynamics 365 Human Resources kann Leistungsprobleme aufweisen, wenn der Verlauf der Stapelverarbeitungsaufträge zu umfangreich wird.</span><span class="sxs-lookup"><span data-stu-id="8d318-105">Microsoft Dynamics 365 Human Resources can experience performance issues if the batch job history grows too large.</span></span>

<span data-ttu-id="8d318-106">**Ursache**</span><span class="sxs-lookup"><span data-stu-id="8d318-106">**Cause**</span></span>

<span data-ttu-id="8d318-107">Stapelverarbeitungsaufträge, die oft ausgeführt werden, können so umfangreich werden, dass sie sich nicht mehr verwalten lassen.</span><span class="sxs-lookup"><span data-stu-id="8d318-107">Batch jobs that run frequently can lead to unsustainable growth of the batch job history.</span></span> <span data-ttu-id="8d318-108">Dieses kann zu Leistungsproblemen führen.</span><span class="sxs-lookup"><span data-stu-id="8d318-108">This can cause performance issues.</span></span> 

<span data-ttu-id="8d318-109">**Lösung**</span><span class="sxs-lookup"><span data-stu-id="8d318-109">**Resolution**</span></span>

<span data-ttu-id="8d318-110">Planen Sie eine automatische Aufgabe, um den Verlauf der Stapelverarbeitungsaufträge zu bereinigen.</span><span class="sxs-lookup"><span data-stu-id="8d318-110">Schedule an automatic task to clean up your batch job history.</span></span> <span data-ttu-id="8d318-111">Es wird empfohlen, die Aufgabe wöchentlich auszuführen, Sie müssen jedoch möglicherweise die Bereinigung häufiger ausführen, je nach Größe Ihrer Umgebung.</span><span class="sxs-lookup"><span data-stu-id="8d318-111">We recommend setting up the task to run weekly, but you might need to run the cleanup more or less frequently, depending on your environment.</span></span> <span data-ttu-id="8d318-112">Die folgenden Verfahren enthalten unsere empfohlenen Einstellungen, die Sie Ihren Anforderungen entsprechend ändern können.</span><span class="sxs-lookup"><span data-stu-id="8d318-112">The following procedure contains our recommended settings, but you can change these according to your needs.</span></span>

1. <span data-ttu-id="8d318-113">Wählen Sie in Human Resources **Systemverwaltung** aus.</span><span class="sxs-lookup"><span data-stu-id="8d318-113">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="8d318-114">Geben Sie auf der Leiste **Suchen** **Verlauf der Stapelverarbeitungsaufträge bereinigen** ein.</span><span class="sxs-lookup"><span data-stu-id="8d318-114">In the **Search** bar, enter **Batch job history clean-up**.</span></span>

   ![Suche nach „Verlauf der Stapelverarbeitungsaufträge bereinigen“](media/talent-batch-history-cleanup-search-bar.png)

3. <span data-ttu-id="8d318-116">In **Historienlimit (Tage)** geben Sie **30** ein.</span><span class="sxs-lookup"><span data-stu-id="8d318-116">In **History limit (days)**, enter **30**.</span></span>

   ![Historienlimit auf 30 festlegen](media/talent-batch-history-cleanup-history-limit.png)

4. <span data-ttu-id="8d318-118">Wählen Sie **Im Hintergrund ausführen** und **Wiederholung** aus.</span><span class="sxs-lookup"><span data-stu-id="8d318-118">Select **Run in the background** and then select **Recurrence**.</span></span>

   ![Wiederholung festlegen](media/talent-batch-history-cleanup-recurrence.png)

5. <span data-ttu-id="8d318-120">Unter **Wiederholung definieren** legen Sie die Option **Startdatum** und **Startzeit** fest, um während der Arbeitszeit oder am Wochenende auszuführen, und wählen Sie dann **KEIN ENDDATUM** aus.</span><span class="sxs-lookup"><span data-stu-id="8d318-120">Under **Define recurrence**, set the **Start date** and **Start time** to occur during off-hours or the weekend, and then select **NO END DATE**.</span></span> 

   ![Startdatum und -zeit der Wiederholung definieren](media/talent-batch-history-cleanup-define-recurrence.png)

6. <span data-ttu-id="8d318-122">Wählen Sie unter **WIEDERHOLUNGSMUSTER** die Option **Tage** aus und legen Sie **NACH DEM ANGEGEBENEN INTERVALL WIEDERHOLEN** auf **7** fest.</span><span class="sxs-lookup"><span data-stu-id="8d318-122">Under **RECURRENCE PATTERN**, select **Days** and set **REPEAT AFTER SPECIFIED INTERVAL** to **7**.</span></span>

   ![Legen Sie fest, dass die Bereinigung wöchentlich ausgeführt wird](media/talent-batch-history-cleanup-recurrence-pattern.png)

7. <span data-ttu-id="8d318-124">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="8d318-124">Select **OK**.</span></span>

8. <span data-ttu-id="8d318-125">Ändern Sie ggf. weitere Parameter unter **Im Hintergrund ausführen** und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="8d318-125">Change any other parameters under **Run in the background** as necessary, and then select **OK**.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]