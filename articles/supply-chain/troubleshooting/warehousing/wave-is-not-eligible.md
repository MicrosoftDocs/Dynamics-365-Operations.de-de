---
title: Welle ist nicht für Bereinigung geeignet
description: Welle ist nicht für Bereinigung geeignet
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWaveTable_WHSWaveProcessingDataCleanup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3e5142cf40a6c0d308e8e952bbe17e85b498826d
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924326"
---
# <a name="wave-isnt-eligible-for-cleanup"></a><span data-ttu-id="2348d-103">Welle ist nicht für Bereinigung geeignet</span><span class="sxs-lookup"><span data-stu-id="2348d-103">Wave isn't eligible for cleanup</span></span>

<span data-ttu-id="2348d-104">Fehlercode: WaveNotEligibleForCleanup</span><span class="sxs-lookup"><span data-stu-id="2348d-104">Error code: WaveNotEligibleForCleanup</span></span>

## <a name="symptoms"></a><span data-ttu-id="2348d-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="2348d-105">Symptoms</span></span>

<span data-ttu-id="2348d-106">Das System zeigt die folgende Fehlermeldung an:</span><span class="sxs-lookup"><span data-stu-id="2348d-106">The system shows the following error message:</span></span>

> <span data-ttu-id="2348d-107">Serie %1 ist nicht für Bereinigung berechtigt.</span><span class="sxs-lookup"><span data-stu-id="2348d-107">Wave %1 is not eligible for cleanup.</span></span>

<span data-ttu-id="2348d-108">Die Wellendaten können nicht bereinigt werden.</span><span class="sxs-lookup"><span data-stu-id="2348d-108">The wave data can't be cleaned up.</span></span>  

## <a name="cause"></a><span data-ttu-id="2348d-109">Ursache</span><span class="sxs-lookup"><span data-stu-id="2348d-109">Cause</span></span>

<span data-ttu-id="2348d-110">Die Welle wird gerade verarbeitet, was durch eine der folgenden Bedingungen angezeigt wird:</span><span class="sxs-lookup"><span data-stu-id="2348d-110">The wave is currently being processed, as indicated by one of the following conditions:</span></span>

- <span data-ttu-id="2348d-111">Das Feld **Wellenstatus** ist auf *Ausgeführt* festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2348d-111">The **Wave status** field is set to *Executing*.</span></span>
- <span data-ttu-id="2348d-112">Wenn Sie **Batchauftrag** in der Gruppe **Welle** auf der Registerkarte **Welle** des Aktivitätsbereichs wählen, ist das Feld **Status** nicht auf *Beendet*, *Fehler* oder *Abgebrochen* festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2348d-112">When you select **Batch job** in the **Wave** group on the **Wave** tab of the Action Pane, the **Status** field isn't set to *Ended*, *Error*, or *Canceled*.</span></span> <span data-ttu-id="2348d-113">Daher wird gerade ein Batchauftrag ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2348d-113">Therefore, a batch job is currently running.</span></span>

## <a name="resolution"></a><span data-ttu-id="2348d-114">Lösung</span><span class="sxs-lookup"><span data-stu-id="2348d-114">Resolution</span></span>

<span data-ttu-id="2348d-115">Wählen Sie im Aktivitätsbereich auf der Registerkarte **Welle** in der Gruppe **Welle** die Option **Batchauftrag**, und führen Sie dann einen der folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="2348d-115">On the Action Pane, on the **Wave** tab, in the **Wave** group, select **Batch job**, and then follow one of these steps:</span></span>

- <span data-ttu-id="2348d-116">Wenn das Feld **Status** auf *Ausgeführt* festgelegt ist: Wählen Sie im Aktivitätsbereich auf der Registerkarte **Batchauftrag** in der Gruppe **Batchauftrag** die Option **Ansicht Aufgaben**.</span><span class="sxs-lookup"><span data-stu-id="2348d-116">If the **Status** field is set to *Executing*: On the Action Pane, on the **Batch job** tab, in the **Batch job** group, select **View tasks**.</span></span> <span data-ttu-id="2348d-117">Sie können den Fortschritt verfolgen, indem Sie die Seite **Batch-Aufgaben** aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="2348d-117">You can follow the progress by refreshing the **Batch tasks** page.</span></span>
- <span data-ttu-id="2348d-118">Wenn das Feld **Status** nicht auf *Ausführend* festgelegt ist: Wählen Sie im Aktivitätsbereich auf der Registerkarte **Batchauftrag** in der Gruppe **Funktionen** die Option **Status ändern**.</span><span class="sxs-lookup"><span data-stu-id="2348d-118">If the **Status** field isn't set to *Executing*: On the Action Pane, on the **Batch job** tab, in the **Functions** group, select **Change status**.</span></span> <span data-ttu-id="2348d-119">Wählen Sie im Feld **Neuen Status wählen** die Option *Warten*.</span><span class="sxs-lookup"><span data-stu-id="2348d-119">In the **Select new status** field, select *Waiting*.</span></span> <span data-ttu-id="2348d-120">Wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="2348d-120">Then select **OK**.</span></span>
