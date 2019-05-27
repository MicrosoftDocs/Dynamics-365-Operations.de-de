---
title: Erstellen eines Stapelverarbeitungsauftrags
description: Bei einem Batchauftrag handelt es sich um eine Gruppe von Aufgaben, die zur automatischen Verarbeitung an eine Anwendungsobjektserver-Instanz (AOS) übermittelt werden.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fbb844ebcf8d4b47b127132a5bf0ea45fa40f747
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562880"
---
# <a name="create-a-batch-job"></a><span data-ttu-id="ad7f4-103">Erstellen eines Stapelverarbeitungsauftrags</span><span class="sxs-lookup"><span data-stu-id="ad7f4-103">Create a batch job</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ad7f4-104">Bei einem Batchauftrag handelt es sich um eine Gruppe von Aufgaben, die zur automatischen Verarbeitung an eine Anwendungsobjektserver-Instanz (AOS) übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="ad7f4-104">A batch job is a group of tasks that are submitted to an Application Object Server (AOS) instance for automatic processing.</span></span> <span data-ttu-id="ad7f4-105">Stapelverarbeitungsaufträge werden unter Verwendung der Sicherheitsanmeldeinformationen des Benutzers ausgeführt, von dem der Auftrag erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="ad7f4-105">Batch jobs are run by using the security credentials of the user who created the job.</span></span> <span data-ttu-id="ad7f4-106">Verwenden Sie die folgende Prozedur, um einen Batchauftrag zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ad7f4-106">Use the following procedure to create a batch job.</span></span> <span data-ttu-id="ad7f4-107">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="ad7f4-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-the-batch-job"></a><span data-ttu-id="ad7f4-108">Den Batchauftrag erstellen</span><span class="sxs-lookup"><span data-stu-id="ad7f4-108">Create the batch job</span></span>
1. <span data-ttu-id="ad7f4-109">Wechseln Sie zu "Systemverwaltung" > "Anfragen" > "Batchaufträge".</span><span class="sxs-lookup"><span data-stu-id="ad7f4-109">Go to System administration > Inquiries > Batch jobs.</span></span>
2. <span data-ttu-id="ad7f4-110">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="ad7f4-110">Click New.</span></span>
3. <span data-ttu-id="ad7f4-111">Geben Sie im Feld "Stellenbeschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="ad7f4-111">In the Job description field, type a value.</span></span>
4. <span data-ttu-id="ad7f4-112">Geben Sie im Feld "Geplantes Startdatum/-uhrzeit" ein Datum und eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="ad7f4-112">In the Scheduled start date/time field, enter a date and time.</span></span>
5. <span data-ttu-id="ad7f4-113">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="ad7f4-113">Click Save.</span></span>

## <a name="create-a-recurrence"></a><span data-ttu-id="ad7f4-114">Eine Wiederholung erstellen</span><span class="sxs-lookup"><span data-stu-id="ad7f4-114">Create a recurrence</span></span>
1. <span data-ttu-id="ad7f4-115">Klicken Sie im Aktivitätsbereich auf "Batchauftrag".</span><span class="sxs-lookup"><span data-stu-id="ad7f4-115">On the Action Pane, click Batch job.</span></span>
2. <span data-ttu-id="ad7f4-116">Klicken Sie auf "Wiederholung".</span><span class="sxs-lookup"><span data-stu-id="ad7f4-116">Click Recurrence.</span></span>
    * <span data-ttu-id="ad7f4-117">Verwenden Sie diese Optionen, um einen Bereich und ein Muster für die Wiederholung einzugeben.</span><span class="sxs-lookup"><span data-stu-id="ad7f4-117">Use these options to enter a range and pattern for the recurrence.</span></span>  
3. <span data-ttu-id="ad7f4-118">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="ad7f4-118">Click OK.</span></span>

## <a name="add-alerts"></a><span data-ttu-id="ad7f4-119">Warnungen hinzufügen</span><span class="sxs-lookup"><span data-stu-id="ad7f4-119">Add alerts</span></span>
1. <span data-ttu-id="ad7f4-120">Klicken Sie im Aktivitätsbereich auf "Batchauftrag".</span><span class="sxs-lookup"><span data-stu-id="ad7f4-120">On the Action Pane, click Batch job.</span></span>
2. <span data-ttu-id="ad7f4-121">Klicken Sie auf "Warnungen".</span><span class="sxs-lookup"><span data-stu-id="ad7f4-121">Click Alerts.</span></span>
    * <span data-ttu-id="ad7f4-122">Geben Sie an, ob Sie möchten, dass Warnmeldungen gesendet werden, wenn der Batchauftrag endet, einen Fehler aufweist oder abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="ad7f4-122">Indicate if you want alert messages sent when the batch job ends, has an error, or is canceled.</span></span> <span data-ttu-id="ad7f4-123">Geben Sie dann an, ob Sie möchten, dass die Warnungen als Popupmeldungen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ad7f4-123">Then specify if you want the alerts to be displayed as pop-up messages.</span></span>   
3. <span data-ttu-id="ad7f4-124">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="ad7f4-124">Click OK.</span></span>

