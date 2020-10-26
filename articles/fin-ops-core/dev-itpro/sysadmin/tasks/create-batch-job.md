---
title: Erstellen eines Stapelverarbeitungsauftrags
description: Bei einem Batchauftrag handelt es sich um eine Gruppe von Aufgaben, die zur automatischen Verarbeitung an eine Anwendungsobjektserver-Instanz (AOS) übermittelt werden.
author: maertenm
manager: AnnBe
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4903724adc9deaa40b6cd04c215273dd4b0522d4
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982525"
---
# <a name="create-a-batch-job"></a><span data-ttu-id="9522d-103">Erstellen eines Stapelverarbeitungsauftrags</span><span class="sxs-lookup"><span data-stu-id="9522d-103">Create a batch job</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9522d-104">Bei einem Batchauftrag handelt es sich um eine Gruppe von Aufgaben, die zur automatischen Verarbeitung an eine Anwendungsobjektserver-Instanz (AOS) übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="9522d-104">A batch job is a group of tasks that are submitted to an Application Object Server (AOS) instance for automatic processing.</span></span> <span data-ttu-id="9522d-105">Stapelverarbeitungsaufträge werden unter Verwendung der Sicherheitsanmeldeinformationen des Benutzers ausgeführt, von dem der Auftrag erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="9522d-105">Batch jobs are run by using the security credentials of the user who created the job.</span></span> <span data-ttu-id="9522d-106">Verwenden Sie die folgende Prozedur, um einen Batchauftrag zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9522d-106">Use the following procedure to create a batch job.</span></span> <span data-ttu-id="9522d-107">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="9522d-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-the-batch-job"></a><span data-ttu-id="9522d-108">Den Batchauftrag erstellen</span><span class="sxs-lookup"><span data-stu-id="9522d-108">Create the batch job</span></span>
1. <span data-ttu-id="9522d-109">Wechseln Sie zu **Navigationsbereich > Module > Systemverwaltung > Anfragen > Batchauftrag**.</span><span class="sxs-lookup"><span data-stu-id="9522d-109">Go to **Navigation pane > Modules > System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="9522d-110">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="9522d-110">Click **New**.</span></span>
3. <span data-ttu-id="9522d-111">Geben Sie im Feld **Stellenbeschreibung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="9522d-111">In the **Job description** field, type a value.</span></span>
4. <span data-ttu-id="9522d-112">Geben Sie im Feld **Geplantes Startdatum/-uhrzeit** ein Datum und eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="9522d-112">In the **Scheduled start date/time** field, enter a date and time.</span></span>
5. <span data-ttu-id="9522d-113">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="9522d-113">Click **Save**.</span></span>

## <a name="create-a-recurrence"></a><span data-ttu-id="9522d-114">Eine Wiederholung erstellen</span><span class="sxs-lookup"><span data-stu-id="9522d-114">Create a recurrence</span></span>
1. <span data-ttu-id="9522d-115">Klicken Sie im Aktivitätsbereich auf **Batchauftrag**.</span><span class="sxs-lookup"><span data-stu-id="9522d-115">On the Action Pane, click **Batch job**.</span></span>
2. <span data-ttu-id="9522d-116">Klicken Sie auf **Wiederholung**.</span><span class="sxs-lookup"><span data-stu-id="9522d-116">Click **Recurrence**.</span></span> <span data-ttu-id="9522d-117">Verwenden Sie diese Optionen, um einen Bereich und ein Muster für die Wiederholung einzugeben.</span><span class="sxs-lookup"><span data-stu-id="9522d-117">Use these options to enter a range and pattern for the recurrence.</span></span>  
3. <span data-ttu-id="9522d-118">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="9522d-118">Click **OK**.</span></span>

## <a name="add-alerts"></a><span data-ttu-id="9522d-119">Warnungen hinzufügen</span><span class="sxs-lookup"><span data-stu-id="9522d-119">Add alerts</span></span>
1. <span data-ttu-id="9522d-120">Klicken Sie im Aktivitätsbereich auf **Batchauftrag**.</span><span class="sxs-lookup"><span data-stu-id="9522d-120">On the Action Pane, click **Batch job**.</span></span>
2. <span data-ttu-id="9522d-121">Klicken Sie auf **Warnungen**.</span><span class="sxs-lookup"><span data-stu-id="9522d-121">Click **Alerts**.</span></span> <span data-ttu-id="9522d-122">Geben Sie an, ob Sie möchten, dass Warnmeldungen gesendet werden, wenn der Batchauftrag endet, einen Fehler aufweist oder abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="9522d-122">Indicate if you want alert messages sent when the batch job ends, has an error, or is canceled.</span></span> <span data-ttu-id="9522d-123">Geben Sie dann an, ob Sie möchten, dass die Warnungen als Popupmeldungen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="9522d-123">Then specify if you want the alerts to be displayed as pop-up messages.</span></span>   
3. <span data-ttu-id="9522d-124">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="9522d-124">Click **OK**.</span></span>

## <a name="adjust-batch-job-status"></a><span data-ttu-id="9522d-125">Status des Stapelverarbeitungsauftrags anpassen</span><span class="sxs-lookup"><span data-stu-id="9522d-125">Adjust batch job status</span></span>
1. <span data-ttu-id="9522d-126">Wechseln Sie zu **Systemverwaltung > Anfragen > Batchaufträge**.</span><span class="sxs-lookup"><span data-stu-id="9522d-126">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="9522d-127">Wählen Sie den entsprechenden Batchauftrag aus.</span><span class="sxs-lookup"><span data-stu-id="9522d-127">Select the appropriate batch job.</span></span>
3. <span data-ttu-id="9522d-128">Klicken Sie im Aktivitätsbereich auf **Batchauftrag > Funktionen > Status ändern**.</span><span class="sxs-lookup"><span data-stu-id="9522d-128">On the Action Pane, click **Batch job > Functions > Change status**.</span></span>
4. <span data-ttu-id="9522d-129">Wählen Sie den entsprechenden Status aus.</span><span class="sxs-lookup"><span data-stu-id="9522d-129">Select the appropriate status:</span></span>
    - <span data-ttu-id="9522d-130">**Zurückhalten**: Legen Sie für den Batchauftrag **Zurückhalten** fest, damit er vom Planungsprogramm für Batchaufträge zurückgehalten wird.</span><span class="sxs-lookup"><span data-stu-id="9522d-130">**Withhold**: Set the batch job as **withhold** so it is withheld from the batch job scheduler.</span></span> <span data-ttu-id="9522d-131">Entspricht *Stopp*.</span><span class="sxs-lookup"><span data-stu-id="9522d-131">Equivalent to *stop*.</span></span>
    - <span data-ttu-id="9522d-132">**Im Wartezustand**: Legen Sie für den Batchauftrag **Im Wartezustand** fest, damit er darauf wartet, vom Planungsprogramm fpr Batchaufträge aufgenommen zu werden.</span><span class="sxs-lookup"><span data-stu-id="9522d-132">**Waiting**: Set the batch job as **waiting** so it is waiting to be picked up by the batch job scheduler.</span></span> <span data-ttu-id="9522d-133">Entspricht *Los*.</span><span class="sxs-lookup"><span data-stu-id="9522d-133">Equivalent to *go*.</span></span>
5. <span data-ttu-id="9522d-134">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="9522d-134">Click **OK**.</span></span>
