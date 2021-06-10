---
title: Steckengebliebene Batchaufträge zurücksetzen
description: In diesem Thema wird erläutert, wie Sie Probleme mit steckengebliebenen Batchaufträgen beheben können.
author: andreabichsel
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: Platform update 42
ms.openlocfilehash: d0b12908993070a41d21ac57d6fb504fc6e3b06a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053514"
---
# <a name="reset-stuck-batch-jobs"></a><span data-ttu-id="f8fa0-103">Steckengebliebene Batchaufträge zurücksetzen</span><span class="sxs-lookup"><span data-stu-id="f8fa0-103">Reset stuck batch jobs</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="issue"></a><span data-ttu-id="f8fa0-104">Abgang</span><span class="sxs-lookup"><span data-stu-id="f8fa0-104">Issue</span></span>

<span data-ttu-id="f8fa0-105">In Microsoft Dynamics 365 Human Resources können Probleme mit Batchaufträgen auftreten, die entweder im Zustand **Ausführen** oder **Abbrechen** steckenbleiben und nicht abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="f8fa0-105">Microsoft Dynamics 365 Human Resources can experience issues with batch jobs that are stuck in either an **Executing** or **Canceling** state and don't complete.</span></span>

## <a name="resolution"></a><span data-ttu-id="f8fa0-106">Lösung</span><span class="sxs-lookup"><span data-stu-id="f8fa0-106">Resolution</span></span>

<span data-ttu-id="f8fa0-107">Wenn ein Batchauftrag im Status **Ausführen** oder **Abbrechen** steckenbleibt, können Sie den Status zurücksetzen, indem Sie die Stornierung des Auftrags erzwingen.</span><span class="sxs-lookup"><span data-stu-id="f8fa0-107">When a batch job is stuck in an **Executing** or **Canceling** state, you can reset the status by forcing the cancellation of the job.</span></span> <span data-ttu-id="f8fa0-108">Nachdem Sie ihn abgebrochen haben, können Sie den Batchauftrag zurücksetzen, indem Sie ihn auf den Status **Im Wartezustand** setzen.</span><span class="sxs-lookup"><span data-stu-id="f8fa0-108">After you cancel it, you can reset the batch job by setting it to a **Waiting** status.</span></span> <span data-ttu-id="f8fa0-109">Er wird dann zur Ausführung im nächsten geplanten Batch-Lauf wieder aufgenommen.</span><span class="sxs-lookup"><span data-stu-id="f8fa0-109">It will then be picked up again for execution in the next scheduled batch run.</span></span>

1. <span data-ttu-id="f8fa0-110">Wählen Sie im **Systemadministration**-Arbeitsbereich die **Links**-Seite und wählen Sie **Batchaufträge**.</span><span class="sxs-lookup"><span data-stu-id="f8fa0-110">In the **System administration** workspace, select the **Links** page, and select **Batch jobs**.</span></span>

2. <span data-ttu-id="f8fa0-111">Wählen Sie auf der Listenseite **Batchauftrag** den Auftrag aus, der zurückgesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f8fa0-111">On the **Batch job** list page, select the job that needs to be reset.</span></span>

3. <span data-ttu-id="f8fa0-112">Wählen Sie in der Aktionsleiste **Abbrechen erzwingen** aus und bestätigen Sie die Aktion.</span><span class="sxs-lookup"><span data-stu-id="f8fa0-112">On the action ribbon, select **Force cancel**, and confirm the action.</span></span>

   > [!NOTE]
   > <span data-ttu-id="f8fa0-113">Die Aktion **Abbrechen erzwingen** ist nur verfügbar, wenn der ausgewählte Batchauftrag den Status **Ausführen** oder **Abbrechen** hat und für den Auftrag keine Batchausführungs- oder -stornierungsprozesse ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f8fa0-113">The **Force cancel** action is only available when the selected batch job has a status of either **Executing** or **Canceling**, and no batch execution or cancellation processes are running for the job.</span></span>

4. <span data-ttu-id="f8fa0-114">Wählen Sie im Aktionsband **Status ändern** aus.</span><span class="sxs-lookup"><span data-stu-id="f8fa0-114">On the action ribbon, select **Change status**.</span></span>

5. <span data-ttu-id="f8fa0-115">Wählen Sie auf der **Neuen Status auswählen**-Seite **Im Wartezustand** und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="f8fa0-115">On the **Select new status** page, select **Waiting**, and then select **OK**.</span></span>

   ![Einen neuen Batchauftragsstatus auswählen](./media/hr-admin-reset-batch-job-status.png)

## <a name="see-also"></a><span data-ttu-id="f8fa0-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f8fa0-117">See also</span></span>

[<span data-ttu-id="f8fa0-118">Leistung durch Einplanung von Batchaufträgen nach Stunden verbessern</span><span class="sxs-lookup"><span data-stu-id="f8fa0-118">Optimize performance by scheduling batch jobs after hours</span></span>](hr-admin-troubleshooting-batch-jobs.md)<br>
[<span data-ttu-id="f8fa0-119">Leistung durch automatische Bereinigungsaufgaben verbessern</span><span class="sxs-lookup"><span data-stu-id="f8fa0-119">Optimize performance with auto cleanup tasks</span></span>](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
