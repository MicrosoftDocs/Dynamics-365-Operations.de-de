---
title: Planungsoptimierung – Übersicht
description: Dieses Thema gibt einen Überblick über die Funktionalität der Planungsoptimierung.
author: ChristianRytt
manager: tfehr
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: f5b51047dbfc95406ebcdda2255b58e41044a6a6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992619"
---
# <a name="planning-optimization-overview"></a><span data-ttu-id="85e03-103">Planungsoptimierung – Übersicht</span><span class="sxs-lookup"><span data-stu-id="85e03-103">Planning Optimization overview</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="85e03-104">Das Planning Optimization Add-in für Microsoft Dynamics 365 Supply Chain Management ermöglicht die Berechnung der Masterplanung außerhalb von Dynamics 365 Supply Chain Management und der zugehörigen SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="85e03-104">The Planning Optimization Add-in for Microsoft Dynamics 365 Supply Chain Management enables master planning calculation to occur outside Dynamics 365 Supply Chain Management and the related SQL database.</span></span> <span data-ttu-id="85e03-105">Zu den Vorteilen, die mit der Funktionalität der Planungsoptimierung verbunden sind, gehören eine verbesserte Leistung und minimale Auswirkungen auf die SQL-Datenbank während der Durchführung der Masterplanung.</span><span class="sxs-lookup"><span data-stu-id="85e03-105">The benefits that are associated with the Planning Optimization functionality include improved performance and minimal impact on SQL database during master planning runs.</span></span> <span data-ttu-id="85e03-106">Schnelle Planungsläufe können auch während der Bürozeiten durchgeführt werden, so dass der Planer sofort auf Bedarfs- oder Parameteränderungen reagieren kann.</span><span class="sxs-lookup"><span data-stu-id="85e03-106">Quick planning runs can be done even during office hours, so that planners can immediately react to demand or parameter changes.</span></span>

<span data-ttu-id="85e03-107">Um die Planungsoptimierung nutzen zu können, müssen Sie das Add-In Planungsoptimierung aus Ihrem Projekt in Microsoft Dynamics Lifecycle Services (LCS) installieren und die Funktionalität der Planungsoptimierung im Supply Chain Management einschalten.</span><span class="sxs-lookup"><span data-stu-id="85e03-107">To use Planning Optimization, you must install the Planning Optimization Add-in from your project in Microsoft Dynamics Lifecycle Services (LCS) and turn on the Planning Optimization functionality in Supply Chain Management.</span></span> <span data-ttu-id="85e03-108">Weitere Informationen finden Sie unter [Erststart mit Planungsoptimierung](get-started.md).</span><span class="sxs-lookup"><span data-stu-id="85e03-108">For more information, see [Get started with Planning Optimization](get-started.md).</span></span>

<span data-ttu-id="85e03-109">Die folgende Abbildung zeigt den Vorteil der Planungsoptimierung während der Bürozeiten.</span><span class="sxs-lookup"><span data-stu-id="85e03-109">The following illustration shows the advantage of running Planning Optimization during office hours.</span></span>

![Vorteil der laufenden Planungsoptimierung während der Bürozeiten](media/PlanningOptimization1.png)

## <a name="improved-performance"></a><span data-ttu-id="85e03-111">Verbesserte Leistung</span><span class="sxs-lookup"><span data-stu-id="85e03-111">Improved performance</span></span>

<span data-ttu-id="85e03-112">Die Planungsoptimierung kann in Szenarien eingesetzt werden, die langlaufende Masterpläne beinhalten.</span><span class="sxs-lookup"><span data-stu-id="85e03-112">Planning Optimization can be used in scenarios that involve long-running master plans.</span></span> <span data-ttu-id="85e03-113">Es wurde speziell für sehr schnelle Berechnungen mit sehr großen Datenmengen entwickelt.</span><span class="sxs-lookup"><span data-stu-id="85e03-113">It's specifically designed for very fast calculations that involve very large volumes of data.</span></span> <span data-ttu-id="85e03-114">Da es sich um einen hyperskalierbaren mandantenfähigen Dienst handelt, können mehrere Instanzen gleichzeitig zusammenarbeiten, um den Plan zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="85e03-114">Because it's built as a hyper-scalable multitenant service, multiple instances can work together simultaneously to calculate the plan.</span></span> <span data-ttu-id="85e03-115">Darüber hinaus entfernt der Planungsservice die Last der Masterplanung aus Ihrem System und arbeitet mit einem Datenstrom, der die Serverlast minimiert.</span><span class="sxs-lookup"><span data-stu-id="85e03-115">Additionally, the planning service removes the load of master planning from your system and works with a data stream that minimizes the server load.</span></span>

<span data-ttu-id="85e03-116">Die Planungsoptimierung kann Ihnen helfen, die folgenden Ziele zu erreichen:</span><span class="sxs-lookup"><span data-stu-id="85e03-116">Planning Optimization can help you achieve the following goals:</span></span>

- <span data-ttu-id="85e03-117">Verbessern Sie die Planungsleistung durch eine kürzere Laufzeit.</span><span class="sxs-lookup"><span data-stu-id="85e03-117">Improve planning performance through a shorter runtime.</span></span>
- <span data-ttu-id="85e03-118">Reduzieren Sie die Auswirkungen auf andere Prozesse während des Masterplanungslaufs.</span><span class="sxs-lookup"><span data-stu-id="85e03-118">Reduce the impact on other processes during the master planning run.</span></span>
- <span data-ttu-id="85e03-119">Führen Sie häufigere Planungsläufe durch.</span><span class="sxs-lookup"><span data-stu-id="85e03-119">Do more frequent planning runs.</span></span> <span data-ttu-id="85e03-120">(Sie sind nicht auf tägliche Läufe beschränkt.)</span><span class="sxs-lookup"><span data-stu-id="85e03-120">(You aren't limited to daily runs.)</span></span>
- <span data-ttu-id="85e03-121">Seien Sie zuversichtlich, dass das zukünftige Geschäftswachstum das Planungssystem nicht überlastet.</span><span class="sxs-lookup"><span data-stu-id="85e03-121">Be confident that future business growth won't overload the planning system.</span></span>

## <a name="architecture-and-data-flow"></a><span data-ttu-id="85e03-122">Architektur und Datenfluss</span><span class="sxs-lookup"><span data-stu-id="85e03-122">Architecture and data flow</span></span>

<span data-ttu-id="85e03-123">Wenn das Planungsoptimierung Add-In aus dem LCS installiert wird, wird eine sichere Verbindung zum Dienst Planungsoptimierung hergestellt.</span><span class="sxs-lookup"><span data-stu-id="85e03-123">When the Planning Optimization Add-in is installed from LCS, a secure connection to the Planning Optimization service is established.</span></span> <span data-ttu-id="85e03-124">Der Service befindet sich im selben Land oder in derselben Region des Rechenzentrums wie die zugehörige Supply Chain Management Instanz.</span><span class="sxs-lookup"><span data-stu-id="85e03-124">The service is located in the same data center country or region as the related Supply Chain Management instance.</span></span> <span data-ttu-id="85e03-125">Nach dem Einrichten der Planungsoptimierung werden zur Laufzeit der Masterplanung Stamm- und Bewegungsdaten aus dem Supply Chain Management an den Service Planungsoptimierung gesendet.</span><span class="sxs-lookup"><span data-stu-id="85e03-125">After Planning Optimization is set up, when master planning is run, master data and transactional data are sent from Supply Chain Management to the Planning Optimization service.</span></span>

<span data-ttu-id="85e03-126">Wenn das Add-In Planungsoptimierung deinstalliert wird, werden alle zugehörigen Daten im Service Planungsoptimierung entfernt.</span><span class="sxs-lookup"><span data-stu-id="85e03-126">If the Planning Optimization Add-in is uninstalled, all related data in the Planning Optimization service is removed.</span></span>

### <a name="high-level-data-flow-for-regeneration-runs"></a><span data-ttu-id="85e03-127">Hochwertiger Datenfluss für Regenerationsläufe</span><span class="sxs-lookup"><span data-stu-id="85e03-127">High-level data flow for regeneration runs</span></span>

1. <span data-ttu-id="85e03-128">Der Supply Chain Management Client sendet ein Signal, um von der Planungsoptimierung einen Planungslauf anzufordern.</span><span class="sxs-lookup"><span data-stu-id="85e03-128">The Supply Chain Management client sends a signal to request a planning run from Planning Optimization.</span></span>
2. <span data-ttu-id="85e03-129">Die Planungsoptimierung fordert über den integrierten Konnektor die erforderlichen Daten an.</span><span class="sxs-lookup"><span data-stu-id="85e03-129">Planning Optimization requests the required data via the integrated connector.</span></span>
3. <span data-ttu-id="85e03-130">Die SQL-Datenbank sendet die angeforderten Informationen über Setup-, Master- und Transaktionsdaten über den Konnektor an die Planungsoptimierung.</span><span class="sxs-lookup"><span data-stu-id="85e03-130">The SQL database sends the requested information about setup, master, and transactional data to Planning Optimization via the connector.</span></span> <span data-ttu-id="85e03-131">Der Konnektor übersetzt Informationen zwischen Supply Chain Management und dem Service Planungsoptimierung.</span><span class="sxs-lookup"><span data-stu-id="85e03-131">The connector translates information between Supply Chain Management and the Planning Optimization service.</span></span>
4. <span data-ttu-id="85e03-132">Der Service Planungsoptimierung hält planungsrelevante Daten im Speicher und führt die erforderlichen Berechnungen durch.</span><span class="sxs-lookup"><span data-stu-id="85e03-132">The Planning Optimization service holds planning-related data in memory and does the required calculations.</span></span>
5. <span data-ttu-id="85e03-133">Das Planungsergebnis wird über den Konnektor an die Supply Chain Management Datenbank gesendet.</span><span class="sxs-lookup"><span data-stu-id="85e03-133">The planning result is sent to the Supply Chain Management database via the connector.</span></span> <span data-ttu-id="85e03-134">Zu den Ergebnissen gehören Informationen wie Planaufträge und Verursacherinformationen.</span><span class="sxs-lookup"><span data-stu-id="85e03-134">The results include information such as planned orders and pegging information.</span></span> <span data-ttu-id="85e03-135">Die Planungsoptimierung sendet ein Signal an das Supply Chain Management, um anzuzeigen, dass der Planungslauf abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="85e03-135">Planning Optimization sends a signal to Supply Chain Management to indicate that the planning run has been completed.</span></span> <span data-ttu-id="85e03-136">Es sendet auch alle relevanten Meldungen und Warnungen.</span><span class="sxs-lookup"><span data-stu-id="85e03-136">It also sends any relevant messages and warnings.</span></span>

<span data-ttu-id="85e03-137">Die folgende Abbildung zeigt den Datenfluss.</span><span class="sxs-lookup"><span data-stu-id="85e03-137">The following illustration shows the data flow.</span></span>

![Datenfluss für Regenerationsläufe](media/PlanningOptimization2.png)

## <a name="related-resources"></a><span data-ttu-id="85e03-139">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="85e03-139">Related resources</span></span>

[<span data-ttu-id="85e03-140">Erste Schritte mit der Planungsoptimierung</span><span class="sxs-lookup"><span data-stu-id="85e03-140">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="85e03-141">Planungsoptimierung Fit-Analyse</span><span class="sxs-lookup"><span data-stu-id="85e03-141">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="85e03-142">Planhistorie und Planungsprotokolle anzeigen</span><span class="sxs-lookup"><span data-stu-id="85e03-142">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="85e03-143">Filter auf einen Plan anwenden</span><span class="sxs-lookup"><span data-stu-id="85e03-143">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="85e03-144">Abbrechen eines Planungsauftrags</span><span class="sxs-lookup"><span data-stu-id="85e03-144">Cancel a planning job</span></span>](cancel-planning-job.md)
