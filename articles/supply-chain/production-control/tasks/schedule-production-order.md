---
title: Einen Produktionsauftrag planen
description: Diese Prozedur zeigt, wie ein Produktionsauftrag geplant wird.
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob, WrkCtrCapResSum
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c6fa2ea9d38c4f4d00f742ccfbf714c237f0ce4d
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843456"
---
# <a name="schedule-a-production-order"></a><span data-ttu-id="e581e-103">Einen Produktionsauftrag planen</span><span class="sxs-lookup"><span data-stu-id="e581e-103">Schedule a production order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e581e-104">Diese Prozedur zeigt, wie ein Produktionsauftrag geplant wird.</span><span class="sxs-lookup"><span data-stu-id="e581e-104">This procedure shows how to schedule a production order.</span></span> <span data-ttu-id="e581e-105">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="e581e-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="e581e-106">Dies ist die dritte Prozedur von sieben, die den Produktionsauftrags-Lebenszyklus erklärt.</span><span class="sxs-lookup"><span data-stu-id="e581e-106">This is the third procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="schedule-a-production-order"></a><span data-ttu-id="e581e-107">Einen Produktionsauftrag planen</span><span class="sxs-lookup"><span data-stu-id="e581e-107">Schedule a production order</span></span>
1. <span data-ttu-id="e581e-108">Wechseln Sie zu "Produktionssteuerung" > "Produktionsaufträge" > "Alle Produktionsaufträge".</span><span class="sxs-lookup"><span data-stu-id="e581e-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="e581e-109">Wählen Sie einen Produktionsauftrag aus, der den Status "Vorkalkuliert" aufweist.</span><span class="sxs-lookup"><span data-stu-id="e581e-109">Select a production order that has the Estimated status.</span></span>  
2. <span data-ttu-id="e581e-110">Klicken Sie im Aktivitätsbereich auf "Zeitplan".</span><span class="sxs-lookup"><span data-stu-id="e581e-110">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="e581e-111">Klicken Sie auf Einzelvorgänge planen.</span><span class="sxs-lookup"><span data-stu-id="e581e-111">Click Schedule jobs.</span></span>
    * <span data-ttu-id="e581e-112">Die für die Planung eingerichteten Parameter werden auf dieser Seite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e581e-112">The parameters for scheduling are set up on this page.</span></span> <span data-ttu-id="e581e-113">Sie können die Parameter für bestimmte Benutzer oder alle Benutzer einrichten.</span><span class="sxs-lookup"><span data-stu-id="e581e-113">You can set up the parameters for specific users or all users.</span></span>  
4. <span data-ttu-id="e581e-114">Wählen Sie im Feld Planungsrichtung "Vorwärts ab Lieferdatum" aus.</span><span class="sxs-lookup"><span data-stu-id="e581e-114">In the Scheduling direction field, select 'Forward from today'.</span></span>
5. <span data-ttu-id="e581e-115">Geben Sie ein Datum in das Feld "Planungsdatum" ein.</span><span class="sxs-lookup"><span data-stu-id="e581e-115">In the Scheduling date field, enter a date.</span></span>
6. <span data-ttu-id="e581e-116">Aktivieren oder deaktivieren Sie das Kontrollkästchen "Begrenzte Kapazität".</span><span class="sxs-lookup"><span data-stu-id="e581e-116">Select or clear the Finite capacity check box.</span></span>
7. <span data-ttu-id="e581e-117">Aktivieren oder deaktivieren Sie das Kontrollkästchen "Begrenztes Material".</span><span class="sxs-lookup"><span data-stu-id="e581e-117">Select or clear the Finite material check box.</span></span>
8. <span data-ttu-id="e581e-118">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="e581e-118">Click OK.</span></span>

## <a name="view-the-scheduling-results"></a><span data-ttu-id="e581e-119">Planungsergebnisse anzeigen</span><span class="sxs-lookup"><span data-stu-id="e581e-119">View the scheduling results</span></span>
1. <span data-ttu-id="e581e-120">Klicken Sie im Aktivitätsbereich auf "Produktionsauftrag".</span><span class="sxs-lookup"><span data-stu-id="e581e-120">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="e581e-121">Klicken Sie auf "Alle Einzelvorgänge".</span><span class="sxs-lookup"><span data-stu-id="e581e-121">Click All jobs.</span></span>
    * <span data-ttu-id="e581e-122">Auf dieser Seite werden die geplanten Einzelvorgänge angezeigt, die Sie gerade generiert haben.</span><span class="sxs-lookup"><span data-stu-id="e581e-122">This page displays the scheduled jobs that you have just generated.</span></span>  
3. <span data-ttu-id="e581e-123">Erweitern oder reduzieren Sie den Abschnitt 'Planung'.</span><span class="sxs-lookup"><span data-stu-id="e581e-123">Expand or collapse the Scheduling section.</span></span>
    * <span data-ttu-id="e581e-124">Im Planungs-Inforegister können Sie das geplante Datum und die Uhrzeit anzeigen.</span><span class="sxs-lookup"><span data-stu-id="e581e-124">On the Scheduling FastTab, you can view the scheduled date and time.</span></span>  
4. <span data-ttu-id="e581e-125">Klicken Sie auf Abfragen.</span><span class="sxs-lookup"><span data-stu-id="e581e-125">Click Inquiries.</span></span>
5. <span data-ttu-id="e581e-126">Klicken Sie"Kapazitätsauslastung"</span><span class="sxs-lookup"><span data-stu-id="e581e-126">Click Capacity load.</span></span>
    * <span data-ttu-id="e581e-127">Die Kapazitätsauslastungsseite stellt die Kapazitäten dar, die für die Feinterminierung reserviert sind, die Gesamtanzahl von Stunden, die zur Zeit für die Ressource reserviert werden und die Anzahl der Stunden ,die für die Feinterminierung der Ressource verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="e581e-127">The Capacity load page displays the capacity that is reserved through job scheduling, the total number of hours that are currently reserved on the resource, and the number of hours that remain available for job scheduling on the resource.</span></span>  
6. <span data-ttu-id="e581e-128">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="e581e-128">Close the page.</span></span>
7. <span data-ttu-id="e581e-129">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="e581e-129">Close the page.</span></span>

