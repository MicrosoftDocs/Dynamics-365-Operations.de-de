--- 
title: " Einen Einzelvorgang konfigurieren und aktivieren, um Auszüge zu buchen"
description: "Diese Prozedur führt Sie Schritt für Schritt durch das Konfigurieren und Ausführen eines wiederkehrenden Batchauftrags zum Buchen von Auszügen für einen ausgewählten Shop oder eine Gruppe von Shops."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: d05e37790aa1068222f2e98ff71fc3fa5eedb0ed
ms.contentlocale: de-de
ms.lasthandoff: 01/19/2018

---
# <a name="configure-and-run-a-job-to-post-statements"></a><span data-ttu-id="61489-103"> Einen Einzelvorgang konfigurieren und aktivieren, um Auszüge zu buchen</span><span class="sxs-lookup"><span data-stu-id="61489-103">Configure and run a job to post statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="61489-104">Diese Prozedur führt Sie Schritt für Schritt durch das Konfigurieren und Ausführen eines wiederkehrenden Batchauftrags zum Buchen von Auszügen für einen ausgewählten Shop oder eine Gruppe von Shops.</span><span class="sxs-lookup"><span data-stu-id="61489-104">This procedure walks through configuring and running a recurrent batch job to post statements for a selected store or group of stores.</span></span> <span data-ttu-id="61489-105">Für diese Prozedur wird das Demo-Datenunternehmen USRT verwendet.</span><span class="sxs-lookup"><span data-stu-id="61489-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="61489-106">Gehen Sie zu Alle Arbeitsbereiche >..</span><span class="sxs-lookup"><span data-stu-id="61489-106">Go to All workspaces > ..</span></span> <span data-ttu-id="61489-107">> Finanzdaten für den Einzelhandelsshop.</span><span class="sxs-lookup"><span data-stu-id="61489-107">> Retail store financials.</span></span>
2. <span data-ttu-id="61489-108">Klicken Sie auf "Auszüge buchen".</span><span class="sxs-lookup"><span data-stu-id="61489-108">Click Post statements.</span></span>
    * <span data-ttu-id="61489-109">Wählen Sie eine Organisationshierarchie und anschließend in der Organisationsknotenstruktur einen einzelnen Shop oder einen Knoten aus.</span><span class="sxs-lookup"><span data-stu-id="61489-109">Select an organizational hierarchy and then in the organization nodes tree, select either an individual store or a node.</span></span> <span data-ttu-id="61489-110">Wählen Sie einen Knoten aus, wenn Sie den Batchauftrag für eine Gruppe von Shops erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="61489-110">Select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="61489-111">Klicken Sie auf den Pfeil, um die Auswahl hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="61489-111">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="61489-112">Klicken Sie auf die Registerkarte "Im Hintergrund ausführen".</span><span class="sxs-lookup"><span data-stu-id="61489-112">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="61489-113">Aktivieren oder deaktivieren Sie das Kontrollkästchen ''Stapelverarbeitung".</span><span class="sxs-lookup"><span data-stu-id="61489-113">Check or uncheck the Batch processing checkbox.</span></span>
5. <span data-ttu-id="61489-114">Klicken Sie auf "Wiederholung".</span><span class="sxs-lookup"><span data-stu-id="61489-114">Click Recurrence.</span></span>
6. <span data-ttu-id="61489-115">Geben Sie im Feld "Startdatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="61489-115">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="61489-116">Geben Sie im Startzeit-Feld eine Zeit ein.</span><span class="sxs-lookup"><span data-stu-id="61489-116">In the Start time field, enter a time.</span></span>
    * <span data-ttu-id="61489-117">Wählen Sie aus, ob die Wiederholung beenden möchten nach einer bestimmten Anzahl von Ausführungen, an einem bestimmten Datum, oder nie.</span><span class="sxs-lookup"><span data-stu-id="61489-117">Choose whether you want to end the recurrence after a specific number of runs, at a specific date, or never.</span></span> <span data-ttu-id="61489-118">Wählen Sie dann die verschiedenen Optionen aus, um zu definieren, wie häufig der Einzelvorgang ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="61489-118">Then choose the various options to define how frequently you want the job to run.</span></span>  
8. <span data-ttu-id="61489-119">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="61489-119">Click OK.</span></span>
9. <span data-ttu-id="61489-120">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="61489-120">Click OK.</span></span>


