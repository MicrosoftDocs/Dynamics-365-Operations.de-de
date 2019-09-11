---
title: Planen Sie den Arbeitsauftrag auf ein bestimmtes Datum und eine bestimmte Uhrzeit.
description: In diesem Abschnitt wird erläutert, wie Sie einen Arbeitsauftrag zu einem bestimmten Datum und einer bestimmten Uhrzeit im Anlagenmanagement einplanen.
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0f818c4c3b669cc94e37cba1e3571c57b5c0dd1b
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887364"
---
# <a name="schedule-work-order-on-specific-date-and-time"></a><span data-ttu-id="6454f-103">Planen Sie den Arbeitsauftrag auf ein bestimmtes Datum und eine bestimmte Uhrzeit.</span><span class="sxs-lookup"><span data-stu-id="6454f-103">Schedule work order on specific date and time</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="6454f-104">Wenn ein Arbeitsauftrag zu einem bestimmten Datum *und* Uhrzeit terminiert werden muss, können Sie die Standardterminierung in der Anlagenverwaltung übersteuern und einen bestimmten Zeitplan für einen Arbeitsauftrag erstellen.</span><span class="sxs-lookup"><span data-stu-id="6454f-104">If a work order must be scheduled on a specific date *and* time, you can override the standard scheduling process in Asset Management and create a specific schedule for a work order.</span></span>

1. <span data-ttu-id="6454f-105">Klicken Sie auf **Anlagenverwaltung** > **Allgemein** > **Arbeitsaufträge** > **Alle Arbeitsaufträge** oder **Aktive Arbeitsaufträge**.</span><span class="sxs-lookup"><span data-stu-id="6454f-105">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="6454f-106">Klicken Sie in der Arbeitsauftragsliste auf die Arbeitsauftrags-ID in der Spalte **Auftrag**.</span><span class="sxs-lookup"><span data-stu-id="6454f-106">In the work order list, click on the Work order ID in the **Work order** column.</span></span>

3. <span data-ttu-id="6454f-107">Klicken Sie auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="6454f-107">Click **Edit**.</span></span>

4. <span data-ttu-id="6454f-108">Fügen Sie in den Feldern **Arbeitsauftragskopf** FastTab Start- und Enddaten und -zeiten in die Felder **Erwarteter Start** und **Erwartetes Ende** ein.</span><span class="sxs-lookup"><span data-stu-id="6454f-108">On the **Work order header** FastTab, insert start and end dates and times in the **Expected start** and **Expected end** fields.</span></span>

![Abbildung 1](media/05-work-order-scheduling.png)

5. <span data-ttu-id="6454f-110">Klicken Sie auf der Registerkarte **Allgemein** auf **Terminplan**, um den Standardplanungsprozess zu verwenden, oder klicken Sie auf **Terminierung**, wenn Sie den Arbeitsauftrag für einen bestimmten Mitarbeiter planen möchten.</span><span class="sxs-lookup"><span data-stu-id="6454f-110">On the **General** tab, click **Schedule** to use the standard scheduling process, or click **Dispatch** if you want to schedule the work order to a specific worker.</span></span>

6. <span data-ttu-id="6454f-111">Um vorhandene Kapazitätsreservierungen zu überschreiben, um sicherzustellen, dass der Arbeitsauftrag im erwarteten Zeitraum terminiert wird, treffen Sie die Auswahl wie in der folgenden Abbildung im Abschnitt **Arbeitsauftrag terminieren**Dialog > **Endliche Kapazität** gezeigt.</span><span class="sxs-lookup"><span data-stu-id="6454f-111">In order to override any existing capacity reservations to ensure that the work order is scheduled in the expected period, make the selections as shown in the figure below in the **Schedule work order** dialog > **Finite capacity** section.</span></span> <span data-ttu-id="6454f-112">Dies bedeutet, dass der Terminierungsprozess bestehende Kapazitätsreservierungen ignoriert, da der Arbeitsauftrag zum erwarteten Startzeitpunkt beginnen muss.</span><span class="sxs-lookup"><span data-stu-id="6454f-112">This means that the scheduling process will ignore existing capacity reservations because the work order must start on the expected start time.</span></span>

![Abbildung 2](media/06-work-order-scheduling.png)

7. <span data-ttu-id="6454f-114">Klicken Sie auf **OK**, um die Planung zu starten.</span><span class="sxs-lookup"><span data-stu-id="6454f-114">Click **OK** to start scheduling.</span></span>

8. <span data-ttu-id="6454f-115">Wenn die Terminierung zu Doppelbuchungen führt, erhalten Sie eine Meldung auf dem Bildschirm und können die zugehörigen Arbeitsaufträge anpassen.</span><span class="sxs-lookup"><span data-stu-id="6454f-115">If the scheduling process results in double bookings, you will see a message on the screen, and you can adjust the related work orders.</span></span>

>[!NOTE]
><span data-ttu-id="6454f-116">Um einen Instandhalter für den Arbeitsauftrag zu planen, muss dieser zum erwarteten Starttermin verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="6454f-116">In order to schedule a maintenance worker for the work order, that maintenance worker must be available at the expected start date and time.</span></span> <span data-ttu-id="6454f-117">Die Verfügbarkeit der Mitarbeiter wird im [Arbeiterkalender](../work-order-scheduling/maintenance-worker-calendar-and-scheduling.md) eingestellt.</span><span class="sxs-lookup"><span data-stu-id="6454f-117">Worker availability is set up in the [worker calendar](../work-order-scheduling/maintenance-worker-calendar-and-scheduling.md).</span></span> 
