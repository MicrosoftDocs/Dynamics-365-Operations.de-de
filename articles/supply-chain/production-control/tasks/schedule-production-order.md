---
title: Einen Produktionsauftrag planen
description: Diese Prozedur zeigt, wie ein Produktionsauftrag geplant wird.
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob, WrkCtrCapResSum, ProdRouteJobSched, ProductionOrderScheduleDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 93ec5bd6984dd1a8f970834070fd77873078b3b0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5237130"
---
# <a name="schedule-a-production-order"></a><span data-ttu-id="3cec0-103">Einen Produktionsauftrag planen</span><span class="sxs-lookup"><span data-stu-id="3cec0-103">Schedule a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3cec0-104">Diese Prozedur zeigt, wie ein Produktionsauftrag geplant wird.</span><span class="sxs-lookup"><span data-stu-id="3cec0-104">This procedure shows how to schedule a production order.</span></span> <span data-ttu-id="3cec0-105">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="3cec0-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="3cec0-106">Dies ist die dritte Prozedur von sieben, die den Produktionsauftrags-Lebenszyklus erklärt.</span><span class="sxs-lookup"><span data-stu-id="3cec0-106">This is the third procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="schedule-a-production-order"></a><span data-ttu-id="3cec0-107">Einen Produktionsauftrag planen</span><span class="sxs-lookup"><span data-stu-id="3cec0-107">Schedule a production order</span></span>
1. <span data-ttu-id="3cec0-108">Wechseln Sie zu "Produktionssteuerung" > "Produktionsaufträge" > "Alle Produktionsaufträge".</span><span class="sxs-lookup"><span data-stu-id="3cec0-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="3cec0-109">Wählen Sie einen Produktionsauftrag aus, der den Status "Vorkalkuliert" aufweist.</span><span class="sxs-lookup"><span data-stu-id="3cec0-109">Select a production order that has the Estimated status.</span></span>  
2. <span data-ttu-id="3cec0-110">Klicken Sie im Aktivitätsbereich auf "Zeitplan".</span><span class="sxs-lookup"><span data-stu-id="3cec0-110">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="3cec0-111">Klicken Sie auf Einzelvorgänge planen.</span><span class="sxs-lookup"><span data-stu-id="3cec0-111">Click Schedule jobs.</span></span>
    * <span data-ttu-id="3cec0-112">Die für die Planung eingerichteten Parameter werden auf dieser Seite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3cec0-112">The parameters for scheduling are set up on this page.</span></span> <span data-ttu-id="3cec0-113">Sie können die Parameter für bestimmte Benutzer oder alle Benutzer einrichten.</span><span class="sxs-lookup"><span data-stu-id="3cec0-113">You can set up the parameters for specific users or all users.</span></span>  
4. <span data-ttu-id="3cec0-114">Wählen Sie im Feld Planungsrichtung "Vorwärts ab Lieferdatum" aus.</span><span class="sxs-lookup"><span data-stu-id="3cec0-114">In the Scheduling direction field, select 'Forward from today'.</span></span>
5. <span data-ttu-id="3cec0-115">Geben Sie ein Datum in das Feld "Planungsdatum" ein.</span><span class="sxs-lookup"><span data-stu-id="3cec0-115">In the Scheduling date field, enter a date.</span></span>
6. <span data-ttu-id="3cec0-116">Aktivieren oder deaktivieren Sie das Kontrollkästchen "Begrenzte Kapazität".</span><span class="sxs-lookup"><span data-stu-id="3cec0-116">Select or clear the Finite capacity check box.</span></span>
7. <span data-ttu-id="3cec0-117">Aktivieren oder deaktivieren Sie das Kontrollkästchen "Begrenztes Material".</span><span class="sxs-lookup"><span data-stu-id="3cec0-117">Select or clear the Finite material check box.</span></span>
8. <span data-ttu-id="3cec0-118">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3cec0-118">Click OK.</span></span>

## <a name="view-the-scheduling-results"></a><span data-ttu-id="3cec0-119">Planungsergebnisse anzeigen</span><span class="sxs-lookup"><span data-stu-id="3cec0-119">View the scheduling results</span></span>
1. <span data-ttu-id="3cec0-120">Klicken Sie im Aktivitätsbereich auf "Produktionsauftrag".</span><span class="sxs-lookup"><span data-stu-id="3cec0-120">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="3cec0-121">Klicken Sie auf "Alle Einzelvorgänge".</span><span class="sxs-lookup"><span data-stu-id="3cec0-121">Click All jobs.</span></span>
    * <span data-ttu-id="3cec0-122">Auf dieser Seite werden die geplanten Einzelvorgänge angezeigt, die Sie gerade generiert haben.</span><span class="sxs-lookup"><span data-stu-id="3cec0-122">This page displays the scheduled jobs that you have just generated.</span></span>  
3. <span data-ttu-id="3cec0-123">Erweitern oder reduzieren Sie den Abschnitt 'Planung'.</span><span class="sxs-lookup"><span data-stu-id="3cec0-123">Expand or collapse the Scheduling section.</span></span>
    * <span data-ttu-id="3cec0-124">Im Planungs-Inforegister können Sie das geplante Datum und die Uhrzeit anzeigen.</span><span class="sxs-lookup"><span data-stu-id="3cec0-124">On the Scheduling FastTab, you can view the scheduled date and time.</span></span>  
4. <span data-ttu-id="3cec0-125">Klicken Sie auf Abfragen.</span><span class="sxs-lookup"><span data-stu-id="3cec0-125">Click Inquiries.</span></span>
5. <span data-ttu-id="3cec0-126">Klicken Sie"Kapazitätsauslastung"</span><span class="sxs-lookup"><span data-stu-id="3cec0-126">Click Capacity load.</span></span>
    * <span data-ttu-id="3cec0-127">Die Kapazitätsauslastungsseite stellt die Kapazitäten dar, die für die Feinterminierung reserviert sind, die Gesamtanzahl von Stunden, die zur Zeit für die Ressource reserviert werden und die Anzahl der Stunden ,die für die Feinterminierung der Ressource verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="3cec0-127">The Capacity load page displays the capacity that is reserved through job scheduling, the total number of hours that are currently reserved on the resource, and the number of hours that remain available for job scheduling on the resource.</span></span>  
6. <span data-ttu-id="3cec0-128">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="3cec0-128">Close the page.</span></span>
7. <span data-ttu-id="3cec0-129">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="3cec0-129">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]