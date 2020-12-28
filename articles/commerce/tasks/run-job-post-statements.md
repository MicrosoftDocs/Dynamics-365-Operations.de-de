---
title: Konfigurieren und Aktivieren eines Einzelvorgangs, um Auszüge zu buchen
description: Diese Prozedur führt Sie Schritt für Schritt durch das Konfigurieren und Ausführen eines wiederkehrenden Batchauftrags zum Buchen von Auszügen für einen ausgewählten Shop oder eine Gruppe von Shops.
author: josaw1
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f89203850b302b769b22920fa5c42d2b0b877684
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4412597"
---
# <a name="configure-and-run-job-to-post-statements"></a><span data-ttu-id="2eaf8-103">Konfigurieren und Aktivieren eines Einzelvorgangs, um Auszüge zu buchen</span><span class="sxs-lookup"><span data-stu-id="2eaf8-103">Configure and run job to post statements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2eaf8-104">Diese Prozedur führt Sie Schritt für Schritt durch das Konfigurieren und Ausführen eines wiederkehrenden Batchauftrags zum Buchen von Auszügen für einen ausgewählten Shop oder eine Gruppe von Shops.</span><span class="sxs-lookup"><span data-stu-id="2eaf8-104">This procedure walks through configuring and running a recurrent batch job to post statements for a selected store or group of stores.</span></span> <span data-ttu-id="2eaf8-105">Für diese Prozedur wird das Demo-Datenunternehmen USRT verwendet.</span><span class="sxs-lookup"><span data-stu-id="2eaf8-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="2eaf8-106">Gehen Sie zu Alle Arbeitsbereiche >..</span><span class="sxs-lookup"><span data-stu-id="2eaf8-106">Go to All workspaces > ..</span></span> <span data-ttu-id="2eaf8-107">> Finanzdaten für Shop.</span><span class="sxs-lookup"><span data-stu-id="2eaf8-107">> Store financials.</span></span>
2. <span data-ttu-id="2eaf8-108">Klicken Sie auf „Aufstellungen in Charge buchen“.</span><span class="sxs-lookup"><span data-stu-id="2eaf8-108">Click Post statements in batch.</span></span>
    * <span data-ttu-id="2eaf8-109">Wählen Sie eine Organisationshierarchie und anschließend in der Organisationsknotenstruktur einen einzelnen Shop oder einen Knoten aus.</span><span class="sxs-lookup"><span data-stu-id="2eaf8-109">Select an organizational hierarchy and then in the organization nodes tree, select either an individual store or a node.</span></span> <span data-ttu-id="2eaf8-110">Wählen Sie einen Knoten aus, wenn Sie den Batchauftrag für eine Gruppe von Shops erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="2eaf8-110">Select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="2eaf8-111">Klicken Sie auf den Pfeil, um die Auswahl hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="2eaf8-111">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="2eaf8-112">Klicken Sie auf die Registerkarte „Im Hintergrund ausführen“. ![Im Hintergrund ausführen](../dev-itpro/media/runbackground.png "Im Hintergrund ausführen")</span><span class="sxs-lookup"><span data-stu-id="2eaf8-112">Click the Run in the background tab. ![Run in the background](../dev-itpro/media/runbackground.png "Run in the background")</span></span> 
4. <span data-ttu-id="2eaf8-113">Aktivieren oder deaktivieren Sie das Kontrollkästchen ''Stapelverarbeitung".</span><span class="sxs-lookup"><span data-stu-id="2eaf8-113">Check or uncheck the Batch processing checkbox.</span></span>
<span data-ttu-id="2eaf8-114">![Stapelverarbeitung](../dev-itpro/media/batchprocessing.png "Stapelverarbeitung und Wiederholung")</span><span class="sxs-lookup"><span data-stu-id="2eaf8-114">![Batch Processing](../dev-itpro/media/batchprocessing.png "Batch Processing & Recurrance")</span></span> 
5. <span data-ttu-id="2eaf8-115">Klicken Sie auf "Wiederholung".</span><span class="sxs-lookup"><span data-stu-id="2eaf8-115">Click Recurrence.</span></span>
6. <span data-ttu-id="2eaf8-116">Geben Sie im Feld "Startdatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="2eaf8-116">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="2eaf8-117">Geben Sie im Startzeit-Feld eine Zeit ein.</span><span class="sxs-lookup"><span data-stu-id="2eaf8-117">In the Start time field, enter a time.</span></span>
    * <span data-ttu-id="2eaf8-118">Wählen Sie aus, ob die Wiederholung beenden möchten nach einer bestimmten Anzahl von Ausführungen, an einem bestimmten Datum, oder nie.</span><span class="sxs-lookup"><span data-stu-id="2eaf8-118">Choose whether you want to end the recurrence after a specific number of runs, at a specific date, or never.</span></span> <span data-ttu-id="2eaf8-119">Wählen Sie dann die verschiedenen Optionen aus, um zu definieren, wie häufig der Einzelvorgang ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2eaf8-119">Then choose the various options to define how frequently you want the job to run.</span></span>  
8. <span data-ttu-id="2eaf8-120">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="2eaf8-120">Click OK.</span></span>
9. <span data-ttu-id="2eaf8-121">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="2eaf8-121">Click OK.</span></span>

