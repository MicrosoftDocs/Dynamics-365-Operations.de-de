---
title: Service Level und Beschreibung
description: In diesem Thema werden Service Level und Beschreibung im Anlagenmanagement erläutert.
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7dd577c930c6cc17da6baee30d3558656de01a09
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/10/2019
ms.locfileid: "2569822"
---
# <a name="service-level-and-description"></a><span data-ttu-id="291f9-103">Service Level und Beschreibung</span><span class="sxs-lookup"><span data-stu-id="291f9-103">Service level and description</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="291f9-104">Wenn Sie einen Arbeitsauftrag anlegen, möchten Sie möglicherweise die Service Levels für ihn definieren und ihm eine allgemeine Beschreibung hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="291f9-104">When you create a work order, you might want to define the service levels for it and add a general description to it.</span></span> <span data-ttu-id="291f9-105">Sie können Service Level für Arbeitsaufträge auf der Seite **Service Level für Arbeitsaufträge** und Beschreibungen auf der Seite **Beschreibung für Arbeitsaufträge** anlegen.</span><span class="sxs-lookup"><span data-stu-id="291f9-105">You can create work order service levels on the **Work order service levels** page and descriptions on the **Work order description** page.</span></span>

## <a name="create-a-service-level"></a><span data-ttu-id="291f9-106">Erstellen eines Service Levels</span><span class="sxs-lookup"><span data-stu-id="291f9-106">Create a service level</span></span>

1. <span data-ttu-id="291f9-107">Wählen Sie **Anlagenmanagement** \> **Einrichtung** \> **Aufträge** \> **Service Level**.</span><span class="sxs-lookup"><span data-stu-id="291f9-107">Select **Asset management** \> **Setup** \> **Work orders** \> **Service level**.</span></span>
2. <span data-ttu-id="291f9-108">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="291f9-108">Select **New**.</span></span>
3. <span data-ttu-id="291f9-109">Geben Sie im Feld **Servicegrad** das Service Level (z.B. eine Nummer) ein.</span><span class="sxs-lookup"><span data-stu-id="291f9-109">In the **Service level** field, enter the service level (for example, a number).</span></span>
4. <span data-ttu-id="291f9-110">Geben Sie im Feld **Name** einen Namen ein.</span><span class="sxs-lookup"><span data-stu-id="291f9-110">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="291f9-111">Auf der Registerkarte **Arbeitsaufträge** FastTab können Sie erwartete Start- und Enddaten und -zeiten definieren.</span><span class="sxs-lookup"><span data-stu-id="291f9-111">On the **Work orders** FastTab, you can define expected start and end dates and times.</span></span> <span data-ttu-id="291f9-112">Die Felder auf dieser Schnellabfrage definieren den Zeitraum, in dem Arbeitsaufträge gestartet und beendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="291f9-112">The fields on this FastTab define the period that work orders should be started and ended during.</span></span> <span data-ttu-id="291f9-113">Sie werden für manuell angelegte Arbeitsaufträge und Arbeitsaufträge verwendet, die aufgrund von Wartungsanforderungen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="291f9-113">They are used for work orders that are manually created and work orders that are created based on maintenance requests.</span></span> 

5. <span data-ttu-id="291f9-114">Geben Sie im Feld **Starttag** eine Anzahl von Tagen ein, um den Zeitraum zu definieren, in dem der Arbeitsauftrag beginnen soll.</span><span class="sxs-lookup"><span data-stu-id="291f9-114">In the **Start day** field, enter a number of days to define the period that the work order should start during.</span></span> <span data-ttu-id="291f9-115">Die Anzahl der Tage errechnet sich aus dem Erstellungsdatum des Arbeitsauftrags.</span><span class="sxs-lookup"><span data-stu-id="291f9-115">The number of days is calculated from the creation date of the work order.</span></span> <span data-ttu-id="291f9-116">Wenn der Arbeitsauftrag beispielsweise beim Erstellen beginnen soll, geben Sie **0** ein.</span><span class="sxs-lookup"><span data-stu-id="291f9-116">For example, if the work order should start when it's created, enter **0**.</span></span> <span data-ttu-id="291f9-117">Wenn der Arbeitsauftrag innerhalb einer Woche nach seiner Erstellung beginnen soll, geben Sie **7** ein.</span><span class="sxs-lookup"><span data-stu-id="291f9-117">If the work order should start within one week after it's created, enter **7**.</span></span>
6. <span data-ttu-id="291f9-118">Um eine Startzeit für den Arbeitsauftrag festzulegen, stellen Sie zusätzlich zu einem Startdatum die Option **Startzeit einstellen** auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="291f9-118">To set a start time for the work order, in addition to a start date, set the **Set start time** option to **Yes**.</span></span> <span data-ttu-id="291f9-119">Geben Sie dann die Startzeit in das Feld **Startzeit** ein.</span><span class="sxs-lookup"><span data-stu-id="291f9-119">Then enter the start time in the **Start time** field.</span></span> <span data-ttu-id="291f9-120">Wenn Sie die Option auf **Nein** setzen, wird die aktuelle Tageszeit verwendet.</span><span class="sxs-lookup"><span data-stu-id="291f9-120">If you set the option to **No**, the current time of day is used.</span></span>
7. <span data-ttu-id="291f9-121">Geben Sie im Feld **Endtag** eine Anzahl von Tagen ein, um den Zeitraum zu definieren, in dem der Arbeitsauftrag enden soll.</span><span class="sxs-lookup"><span data-stu-id="291f9-121">In the **End day** field, enter a number of days to define the period that the work order should end during.</span></span> <span data-ttu-id="291f9-122">Die Anzahl der Tage wird ab dem Startdatum des Arbeitsauftrags berechnet.</span><span class="sxs-lookup"><span data-stu-id="291f9-122">The number of days is calculated from the start date of the work order.</span></span> <span data-ttu-id="291f9-123">Wenn der Arbeitsauftrag beispielsweise innerhalb einer Woche nach seinem Beginndatum enden soll, geben Sie **7** ein.</span><span class="sxs-lookup"><span data-stu-id="291f9-123">For example, if the work order should end within one week of its start date, enter **7**.</span></span>
8. <span data-ttu-id="291f9-124">Um eine Endzeit für den Arbeitsauftrag festzulegen, stellen Sie zusätzlich zu einem Enddatum die Option **Endzeit einstellen** auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="291f9-124">To set an end time for the work order, in addition to an end date, set the **Set end time** option to **Yes**.</span></span> <span data-ttu-id="291f9-125">Geben Sie dann die Endzeit in das Feld **Endzeit** ein.</span><span class="sxs-lookup"><span data-stu-id="291f9-125">Then enter the end time in the **End time** field.</span></span> <span data-ttu-id="291f9-126">Wenn Sie die Option auf **Nein** setzen, wird die aktuelle Tageszeit verwendet.</span><span class="sxs-lookup"><span data-stu-id="291f9-126">If you set the option to **No**, the current time of day is used.</span></span>
9. <span data-ttu-id="291f9-127">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="291f9-127">Select **Save**.</span></span>

![Seite „Arbeitsauftrags-Leistungsebene“](media/19-setup-for-work-orders.png)

## <a name="create-a-description"></a><span data-ttu-id="291f9-129">Erstellen einer Beschreibung</span><span class="sxs-lookup"><span data-stu-id="291f9-129">Create a description</span></span>

1. <span data-ttu-id="291f9-130">Wählen Sie **Anlagenmanagement** \> **Einrichtung** \> **Aufträge** \> **Beschreibungen**.</span><span class="sxs-lookup"><span data-stu-id="291f9-130">Select **Asset management** \> **Setup** \> **Work orders** \> **Descriptions**.</span></span>
2. <span data-ttu-id="291f9-131">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="291f9-131">Select **New**.</span></span>
3. <span data-ttu-id="291f9-132">Geben Sie im Feld **Beschreibung** die Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="291f9-132">In the **Description** field, enter the description.</span></span>
4. <span data-ttu-id="291f9-133">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="291f9-133">Select **Save**.</span></span>
