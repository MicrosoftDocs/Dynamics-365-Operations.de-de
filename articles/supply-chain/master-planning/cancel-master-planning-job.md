---
title: Masterplanungsauftrag abbrechen
description: In diesem Thema wird erläutert, wie Sie einen aktiven Planungsauftrag abbrechen, der die Funktion „Integrierte Planung“ verwendet.
author: ChristianRytt
manager: tfehr
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace, ReqProcessList
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-12-16
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6f5ce460cc2915d1d4d9b5699723a62ed7f94599
ms.sourcegitcommit: cde71bc7d14ea6cdff2c4e991057d39a6a0473d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2020
ms.locfileid: "3886870"
---
# <a name="cancel-a-master-planning-job"></a><span data-ttu-id="37cec-103">Masterplanungsauftrag abbrechen</span><span class="sxs-lookup"><span data-stu-id="37cec-103">Cancel a master planning job</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="37cec-104">In Microsoft Dynamics 365 Supply Chain Management gibt es mehrere Möglichkeiten, einen Masterplanungsauftrag abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="37cec-104">In Microsoft Dynamics 365 Supply Chain Management, there are multiple options for canceling a master planning job.</span></span> <span data-ttu-id="37cec-105">Beispielsweise möchten Sie vielleicht einen Masterplanungsauftrag abbrechen, wenn er versehentlich gestartet wurde oder länger als erwartet ausgeführt wird, und Sie möchten ihn beenden.</span><span class="sxs-lookup"><span data-stu-id="37cec-105">For example, you may want to cancel a master planning job if it was started by mistake or is running longer than expected and you want to end it.</span></span> <span data-ttu-id="37cec-106">Am besten brechen Sie einen Planungsauftrag über die Seite **Nicht abgeschlossene Planungsprozesse** ab.</span><span class="sxs-lookup"><span data-stu-id="37cec-106">The best way to cancel a planning job is from  the **Unfinished planning processes** page.</span></span> <span data-ttu-id="37cec-107">Alternative Optionen auf den Seiten **Batchaufträge** und **Erweiterte Batchaufträge** sollten nur verwendet werden, wenn das Abbrechen des Masterplanungsauftrags über die Seite **Nicht abgeschlossene Prozesse** nicht innerhalb weniger Minuten abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="37cec-107">Alternative options from the **Batch jobs** and **Batch jobs enhanced** pages should only be used if canceling the master planning job from the **Unfinished planning processes** page did not complete within a few minutes.</span></span>

## <a name="preferred-cancel-option"></a><span data-ttu-id="37cec-108">Bevorzugte Option zum Abbrechen</span><span class="sxs-lookup"><span data-stu-id="37cec-108">Preferred cancel option</span></span>
### <a name="cancel-master-planning-job-from-unfinished-planning-processes-page"></a><span data-ttu-id="37cec-109">Masterplanungsauftrag über die Seite **Nicht abgeschlossene Prozesse** abbrechen</span><span class="sxs-lookup"><span data-stu-id="37cec-109">Cancel master planning job from **Unfinished planning processes** page</span></span>
1. <span data-ttu-id="37cec-110">Gehen Sie zu **Produktprogrammplanung > Abfragen und Berichte > Produktprogrammplanung > Nicht abgeschlossene Prozesse**.</span><span class="sxs-lookup"><span data-stu-id="37cec-110">Go to **Master planning > Inquiries and reports > Master planning > Unfinished planning processes**.</span></span>
2. <span data-ttu-id="37cec-111">Wählen Sie die Position mit dem abzubrechenden Planungsprozess aus.</span><span class="sxs-lookup"><span data-stu-id="37cec-111">Select the line with the planning process that you want to cancel.</span></span>
3. <span data-ttu-id="37cec-112">Klicken Sie auf **Abbrechen**.</span><span class="sxs-lookup"><span data-stu-id="37cec-112">Click **Cancel**.</span></span>

## <a name="additional-cancel-options"></a><span data-ttu-id="37cec-113">Weitere Optionen zum Abbrechen</span><span class="sxs-lookup"><span data-stu-id="37cec-113">Additional cancel options</span></span>
<span data-ttu-id="37cec-114">Diese sollten nur dann verwendet werden, wenn der Abbruch des Generalplanungsjobs von der Seite **Unerledigte Planungsprozesse** nicht innerhalb weniger Minuten abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="37cec-114">These should only be used if canceling the master planning job from the **Unfinished planning processes** page did not complete within a few minutes.</span></span>

### <a name="delete-master-planning-job-from-the-batch-jobs-page"></a><span data-ttu-id="37cec-115">Masterplanungsauftrag über die Seite **Batchaufträge** löschen</span><span class="sxs-lookup"><span data-stu-id="37cec-115">Delete master planning job from the **Batch jobs** page</span></span>
1. <span data-ttu-id="37cec-116">Wechseln Sie zu **Systemverwaltung > Anfragen > Batchaufträge**.</span><span class="sxs-lookup"><span data-stu-id="37cec-116">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="37cec-117">Wählen Sie die Position mit dem zu löschenden Planungsauftrag aus.</span><span class="sxs-lookup"><span data-stu-id="37cec-117">Select the line with the planning job that you want to delete.</span></span>
3. <span data-ttu-id="37cec-118">Klicken Sie auf **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="37cec-118">Click **Delete**.</span></span>

### <a name="abort-master-planning-job-task-from-the-batch-jobs-enhanced-page"></a><span data-ttu-id="37cec-119">Aufgabe des Masterplanungsauftrags über die Seite **Erweiterte Batchaufträge** abbrechen</span><span class="sxs-lookup"><span data-stu-id="37cec-119">Abort master planning job task from the **Batch jobs enhanced** page</span></span>
1. <span data-ttu-id="37cec-120">Wechseln Sie zu **Systemverwaltung > Anfragen > Batchaufträge**.</span><span class="sxs-lookup"><span data-stu-id="37cec-120">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="37cec-121">Wenn die Auftrags-ID nicht in der Liste angezeigt wird, klicken Sie auf **Zum erweiterten Formular wechseln**. Fahren Sie andernfalls mit dem nächsten Schritt fort.</span><span class="sxs-lookup"><span data-stu-id="37cec-121">If the job ID is not shown in the list, click **Switch to enhanced form**, otherwise proceed with the next step.</span></span>
3. <span data-ttu-id="37cec-122">Öffnen Sie den Batchauftrag.</span><span class="sxs-lookup"><span data-stu-id="37cec-122">Open the batch job.</span></span> <span data-ttu-id="37cec-123">Klicken Sie auf die **Auftrags-ID** für den Batchauftrag, der Aufgaben enthält, die Sie beenden möchten.</span><span class="sxs-lookup"><span data-stu-id="37cec-123">Click the **Job ID** for the batch job with tasks that you want to end.</span></span>
4. <span data-ttu-id="37cec-124">Wählen Sie in **Batchaufgaben** die zu beendenden Aufgaben aus.</span><span class="sxs-lookup"><span data-stu-id="37cec-124">In **Batch tasks**, select the tasks to end.</span></span>
5. <span data-ttu-id="37cec-125">Klicken Sie auf **Status ändern**, wählen Sie **Abbrechen**, und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="37cec-125">Click **Change status**, choose **Canceling** and click **OK**.</span></span>
6. <span data-ttu-id="37cec-126">Klicken Sie auf dem Inforegister **Batchaufgaben** auf **Abbrechen**.</span><span class="sxs-lookup"><span data-stu-id="37cec-126">On the **Batch tasks** FastTab, click **Abort**.</span></span>
