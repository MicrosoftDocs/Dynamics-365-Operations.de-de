--- 
title: "Einen Zeitplan für einen Standort erstellen"
description: "Diese Prozedur zeigt, wie Produktionsaufträge geplant werden sollen, die noch nicht für einen Standort gestartet wurden."
author: YuyuScheller
manager: AnnBe
ms.date: 06/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 775428bf84a752c03c492e764fa9ed576ab64fb8
ms.contentlocale: de-de
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-schedule-for-a-site"></a><span data-ttu-id="b8a35-103">Einen Zeitplan für einen Standort erstellen</span><span class="sxs-lookup"><span data-stu-id="b8a35-103">Create a schedule for a site</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b8a35-104">Diese Prozedur zeigt, wie Produktionsaufträge geplant werden sollen, die noch nicht für einen Standort gestartet wurden.</span><span class="sxs-lookup"><span data-stu-id="b8a35-104">This procedure shows how to schedule production orders that are not yet started for a site.</span></span>  <span data-ttu-id="b8a35-105">Das Demodatenunternehmen USMF wird verwendet, um diese Prozedur abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="b8a35-105">The demo data company USMF is used to complete this procedure.</span></span>


## <a name="identify-production-orders-that-are-not-started"></a><span data-ttu-id="b8a35-106">Identifizieren Sie Produktionsaufträge, die noch nicht gestartet wurden.</span><span class="sxs-lookup"><span data-stu-id="b8a35-106">Identify production orders that are not started</span></span>
1. <span data-ttu-id="b8a35-107">Wechseln Sie zu "Produktionssteuerung" > "Produktionsaufträge" > "Alle Produktionsaufträge".</span><span class="sxs-lookup"><span data-stu-id="b8a35-107">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="b8a35-108">Verwenden Sie den Schnellfilter, um Datensätze zu suchen.</span><span class="sxs-lookup"><span data-stu-id="b8a35-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="b8a35-109">Filtern Sie beispielsweise zum Feld "Standort" mit einem Wert von "1".</span><span class="sxs-lookup"><span data-stu-id="b8a35-109">For example, filter on the Site field with a value of '1'.</span></span>
    * <span data-ttu-id="b8a35-110">1 stellt einen Standort in USMF dar.</span><span class="sxs-lookup"><span data-stu-id="b8a35-110">1 represents a site in USMF.</span></span> <span data-ttu-id="b8a35-111">Wenn Sie nicht USMF verwenden, wählen Sie eine Standort von Ihrem eigenen Unternehmen aus.</span><span class="sxs-lookup"><span data-stu-id="b8a35-111">If you are not using USMF, select a site from your own company.</span></span>  
3. <span data-ttu-id="b8a35-112">Öffnen Sie den Spaltenfilter "Status".</span><span class="sxs-lookup"><span data-stu-id="b8a35-112">Open the Status column filter.</span></span>
4. <span data-ttu-id="b8a35-113">Wenden Sie einen Filter für das Feld "Status" an, mit einem Wert "Eingeplant", mithilfe des Filteroperators "ist genau".</span><span class="sxs-lookup"><span data-stu-id="b8a35-113">Apply a filter on the "Status" field, with a value of "Scheduled", using the "is exactly" filter operator.</span></span>

## <a name="create-a-schedule"></a><span data-ttu-id="b8a35-114">Erstellen Sie einen Zeitplan</span><span class="sxs-lookup"><span data-stu-id="b8a35-114">Create a schedule</span></span>
1. <span data-ttu-id="b8a35-115">Markieren Sie alle Zeilen in der Liste, oder heben Sie die Markierung auf.</span><span class="sxs-lookup"><span data-stu-id="b8a35-115">In the list, mark or unmark all rows.</span></span>
2. <span data-ttu-id="b8a35-116">Klicken Sie im Aktivitätsbereich auf "Zeitplan".</span><span class="sxs-lookup"><span data-stu-id="b8a35-116">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="b8a35-117">Klicken Sie auf "Einzelvorgänge planen".</span><span class="sxs-lookup"><span data-stu-id="b8a35-117">Click Schedule jobs.</span></span>
4. <span data-ttu-id="b8a35-118">Wählen Sie im Feld Planungsrichtung "Rückwärts ab Lieferdatum" aus.</span><span class="sxs-lookup"><span data-stu-id="b8a35-118">In the Scheduling direction field, select 'Backward from delivery date'.</span></span>
5. <span data-ttu-id="b8a35-119">Wählen Sie "Nein" im Feld "Begrenzte Kapazität" aus.</span><span class="sxs-lookup"><span data-stu-id="b8a35-119">Select No in the Finite capacity field.</span></span>
6. <span data-ttu-id="b8a35-120">Wählen Sie "Nein" im Feld "Begrenztes Material" aus.</span><span class="sxs-lookup"><span data-stu-id="b8a35-120">Select No in the Finite material field.</span></span>
7. <span data-ttu-id="b8a35-121">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="b8a35-121">Click OK.</span></span>
    * <span data-ttu-id="b8a35-122">Dies kann einige Zeit in Anspruch nehmen.</span><span class="sxs-lookup"><span data-stu-id="b8a35-122">This may take a while.</span></span>  

## <a name="view-the-result-of-scheduled-production-orders"></a><span data-ttu-id="b8a35-123">Zeigen Sie das Ergebnis geplanter Produktionsaufträge an.</span><span class="sxs-lookup"><span data-stu-id="b8a35-123">View the result of scheduled production orders</span></span>
1. <span data-ttu-id="b8a35-124">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="b8a35-124">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="b8a35-125">Sie können jede beliebige Zeile markieren.</span><span class="sxs-lookup"><span data-stu-id="b8a35-125">You can mark any row.</span></span>  
2. <span data-ttu-id="b8a35-126">Klicken Sie im Aktivitätsbereich auf "Produktionsauftrag".</span><span class="sxs-lookup"><span data-stu-id="b8a35-126">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="b8a35-127">Klicken Sie auf "Alle Einzelvorgänge".</span><span class="sxs-lookup"><span data-stu-id="b8a35-127">Click All jobs.</span></span>
    * <span data-ttu-id="b8a35-128">Auf dieser Seite können Sie die Liste der Einzelvorgänge anzeigen.</span><span class="sxs-lookup"><span data-stu-id="b8a35-128">On this page, you can see the list of jobs.</span></span> <span data-ttu-id="b8a35-129">Auf der Registerkarte "Planung" können Sie das Start- und Enddatum für einen Einzelvorgang anzeigen.</span><span class="sxs-lookup"><span data-stu-id="b8a35-129">On the Scheduling tab, you can see the Start date and End date for a job.</span></span>  
4. <span data-ttu-id="b8a35-130">Klicken Sie auf "Material".</span><span class="sxs-lookup"><span data-stu-id="b8a35-130">Click Materials.</span></span>
    * <span data-ttu-id="b8a35-131">Auf dieser Seite können Sie die vorkalkulierte Materialentnahme für die Arbeitsgänge im Produktionsauftrag und den aktuellen verfügbaren Bestand anzeigen.</span><span class="sxs-lookup"><span data-stu-id="b8a35-131">On this page, you can see the estimated material consumption for the operations on the production order and the current available inventory.</span></span>  


