---
title: Optimieren der Leistung mit automatischen Bereinigungsaufgaben
description: In diesem Artikel wird erläutert, wie einige Leistungsprobleme mit Microsoft Dynamics 365 Human Resources behoben werden, indem Sie den Verlauf der Stapelverarbeitungsaufträge bereinigen.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: a983fde8ba393ab25f2b330014e04a1379f0e4d0
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009107"
---
# <a name="optimize-performance-with-auto-cleanup-tasks"></a><span data-ttu-id="cf68f-103">Optimieren Sie die Leistung mit automatischen Bereinigungsaufgaben</span><span class="sxs-lookup"><span data-stu-id="cf68f-103">Optimize performance with auto cleanup tasks</span></span>

<span data-ttu-id="cf68f-104">**Abgang**</span><span class="sxs-lookup"><span data-stu-id="cf68f-104">**Issue**</span></span>

<span data-ttu-id="cf68f-105">Microsoft Dynamics 365 Human Resources kann Leistungsprobleme aufweisen, wenn der Verlauf der Stapelverarbeitungsaufträge zu umfangreich wird.</span><span class="sxs-lookup"><span data-stu-id="cf68f-105">Microsoft Dynamics 365 Human Resources can experience performance issues if the batch job history grows too large.</span></span>

<span data-ttu-id="cf68f-106">**Ursache**</span><span class="sxs-lookup"><span data-stu-id="cf68f-106">**Cause**</span></span>

<span data-ttu-id="cf68f-107">Stapelverarbeitungsaufträge, die oft ausgeführt werden, können so umfangreich werden, dass sie sich nicht mehr verwalten lassen.</span><span class="sxs-lookup"><span data-stu-id="cf68f-107">Batch jobs that run frequently can lead to unsustainable growth of the batch job history.</span></span> <span data-ttu-id="cf68f-108">Dieses kann zu Leistungsproblemen führen.</span><span class="sxs-lookup"><span data-stu-id="cf68f-108">This can cause performance issues.</span></span> 

<span data-ttu-id="cf68f-109">**Lösung**</span><span class="sxs-lookup"><span data-stu-id="cf68f-109">**Resolution**</span></span>

<span data-ttu-id="cf68f-110">Planen Sie eine automatische Aufgabe, um den Verlauf der Stapelverarbeitungsaufträge zu bereinigen.</span><span class="sxs-lookup"><span data-stu-id="cf68f-110">Schedule an automatic task to clean up your batch job history.</span></span> <span data-ttu-id="cf68f-111">Es wird empfohlen, die Aufgabe wöchentlich auszuführen, Sie müssen jedoch möglicherweise die Bereinigung häufiger ausführen, je nach Größe Ihrer Umgebung.</span><span class="sxs-lookup"><span data-stu-id="cf68f-111">We recommend setting up the task to run weekly, but you might need to run the cleanup more or less frequently, depending on your environment.</span></span> <span data-ttu-id="cf68f-112">Die folgenden Verfahren enthalten unsere empfohlenen Einstellungen, die Sie Ihren Anforderungen entsprechend ändern können.</span><span class="sxs-lookup"><span data-stu-id="cf68f-112">The following procedure contains our recommended settings, but you can change these according to your needs.</span></span>

1. <span data-ttu-id="cf68f-113">Wählen Sie in Human Resources **Systemverwaltung** aus.</span><span class="sxs-lookup"><span data-stu-id="cf68f-113">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="cf68f-114">Geben Sie auf der Leiste **Suchen** **Verlauf der Stapelverarbeitungsaufträge bereinigen** ein.</span><span class="sxs-lookup"><span data-stu-id="cf68f-114">In the **Search** bar, enter **Batch job history clean-up**.</span></span>

   ![Suche nach „Verlauf der Stapelverarbeitungsaufträge bereinigen“](media/talent-batch-history-cleanup-search-bar.png)

3. <span data-ttu-id="cf68f-116">In **Historienlimit (Tage)** geben Sie **30** ein.</span><span class="sxs-lookup"><span data-stu-id="cf68f-116">In **History limit (days)**, enter **30**.</span></span>

   ![Historienlimit auf 30 festlegen](media/talent-batch-history-cleanup-history-limit.png)

4. <span data-ttu-id="cf68f-118">Wählen Sie **Im Hintergrund ausführen** und **Wiederholung** aus.</span><span class="sxs-lookup"><span data-stu-id="cf68f-118">Select **Run in the background** and then select **Recurrence**.</span></span>

   ![Wiederholung festlegen](media/talent-batch-history-cleanup-recurrence.png)

5. <span data-ttu-id="cf68f-120">Unter **Wiederholung definieren** legen Sie die Option **Startdatum** und **Startzeit** fest, um während der Arbeitszeit oder am Wochenende auszuführen, und wählen Sie dann **KEIN ENDDATUM** aus.</span><span class="sxs-lookup"><span data-stu-id="cf68f-120">Under **Define recurrence**, set the **Start date** and **Start time** to occur during off-hours or the weekend, and then select **NO END DATE**.</span></span> 

   ![Startdatum und -zeit der Wiederholung definieren](media/talent-batch-history-cleanup-define-recurrence.png)

6. <span data-ttu-id="cf68f-122">Wählen Sie unter **WIEDERHOLUNGSMUSTER** die Option **Tage** aus und legen Sie **NACH DEM ANGEGEBENEN INTERVALL WIEDERHOLEN** auf **7** fest.</span><span class="sxs-lookup"><span data-stu-id="cf68f-122">Under **RECURRENCE PATTERN**, select **Days** and set **REPEAT AFTER SPECIFIED INTERVAL** to **7**.</span></span>

   ![Legen Sie fest, dass die Bereinigung wöchentlich ausgeführt wird](media/talent-batch-history-cleanup-recurrence-pattern.png)

7. <span data-ttu-id="cf68f-124">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="cf68f-124">Select **OK**.</span></span>

8. <span data-ttu-id="cf68f-125">Ändern Sie ggf. weitere Parameter unter **Im Hintergrund ausführen** und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="cf68f-125">Change any other parameters under **Run in the background** as necessary, and then select **OK**.</span></span>

