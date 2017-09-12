--- 
title: Erstellen eines Stapelverarbeitungsauftrags
description: "Bei einem Batchauftrag handelt es sich um eine Gruppe von Aufgaben, die zur automatischen Verarbeitung an eine Anwendungsobjektserver-Instanz (AOS) übermittelt werden."
author: maertenm
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 31c8e2ba87ef8c17a3147e1159104585258d4164
ms.contentlocale: de-de
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-batch-job"></a><span data-ttu-id="e1a98-103">Erstellen eines Stapelverarbeitungsauftrags</span><span class="sxs-lookup"><span data-stu-id="e1a98-103">Create a batch job</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e1a98-104">Bei einem Batchauftrag handelt es sich um eine Gruppe von Aufgaben, die zur automatischen Verarbeitung an eine Anwendungsobjektserver-Instanz (AOS) übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="e1a98-104">A batch job is a group of tasks that are submitted to an Application Object Server (AOS) instance for automatic processing.</span></span> <span data-ttu-id="e1a98-105">Stapelverarbeitungsaufträge werden unter Verwendung der Sicherheitsanmeldeinformationen des Benutzers ausgeführt, von dem der Auftrag erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="e1a98-105">Batch jobs are run by using the security credentials of the user who created the job.</span></span> <span data-ttu-id="e1a98-106">Verwenden Sie die folgende Prozedur, um einen Batchauftrag zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e1a98-106">Use the following procedure to create a batch job.</span></span> <span data-ttu-id="e1a98-107">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="e1a98-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-the-batch-job"></a><span data-ttu-id="e1a98-108">Den Batchauftrag erstellen</span><span class="sxs-lookup"><span data-stu-id="e1a98-108">Create the batch job</span></span>
1. <span data-ttu-id="e1a98-109">Wechseln Sie zu "Systemverwaltung" > "Anfragen" > "Batchaufträge".</span><span class="sxs-lookup"><span data-stu-id="e1a98-109">Go to System administration > Inquiries > Batch jobs.</span></span>
2. <span data-ttu-id="e1a98-110">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="e1a98-110">Click New.</span></span>
3. <span data-ttu-id="e1a98-111">Geben Sie im Feld "Stellenbeschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="e1a98-111">In the Job description field, type a value.</span></span>
4. <span data-ttu-id="e1a98-112">Geben Sie im Feld "Geplantes Startdatum/-uhrzeit" ein Datum und eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="e1a98-112">In the Scheduled start date/time field, enter a date and time.</span></span>
5. <span data-ttu-id="e1a98-113">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="e1a98-113">Click Save.</span></span>

## <a name="create-a-recurrence"></a><span data-ttu-id="e1a98-114">Eine Wiederholung erstellen</span><span class="sxs-lookup"><span data-stu-id="e1a98-114">Create a recurrence</span></span>
1. <span data-ttu-id="e1a98-115">Klicken Sie im Aktivitätsbereich auf "Batchauftrag".</span><span class="sxs-lookup"><span data-stu-id="e1a98-115">On the Action Pane, click Batch job.</span></span>
2. <span data-ttu-id="e1a98-116">Klicken Sie auf "Wiederholung".</span><span class="sxs-lookup"><span data-stu-id="e1a98-116">Click Recurrence.</span></span>
    * <span data-ttu-id="e1a98-117">Verwenden Sie diese Optionen, um einen Bereich und ein Muster für die Wiederholung einzugeben.</span><span class="sxs-lookup"><span data-stu-id="e1a98-117">Use these options to enter a range and pattern for the recurrence.</span></span>  
3. <span data-ttu-id="e1a98-118">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="e1a98-118">Click OK.</span></span>

## <a name="add-alerts"></a><span data-ttu-id="e1a98-119">Warnungen hinzufügen</span><span class="sxs-lookup"><span data-stu-id="e1a98-119">Add alerts</span></span>
1. <span data-ttu-id="e1a98-120">Klicken Sie im Aktivitätsbereich auf "Batchauftrag".</span><span class="sxs-lookup"><span data-stu-id="e1a98-120">On the Action Pane, click Batch job.</span></span>
2. <span data-ttu-id="e1a98-121">Klicken Sie auf "Warnungen".</span><span class="sxs-lookup"><span data-stu-id="e1a98-121">Click Alerts.</span></span>
    * <span data-ttu-id="e1a98-122">Geben Sie an, ob Sie möchten, dass Warnmeldungen gesendet werden, wenn der Batchauftrag endet, einen Fehler aufweist oder abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="e1a98-122">Indicate if you want alert messages sent when the batch job ends, has an error, or is canceled.</span></span> <span data-ttu-id="e1a98-123">Geben Sie dann an, ob Sie möchten, dass die Warnungen als Popupmeldungen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="e1a98-123">Then specify if you want the alerts to be displayed as pop-up messages.</span></span>   
3. <span data-ttu-id="e1a98-124">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="e1a98-124">Click OK.</span></span>


