---
title: Erste Schritte mit der Planungsoptimierung
description: In diesem Thema wird erläutert, wie Sie mit der Verwendung der Funktionalität der Planungsoptimierung beginnen.
author: ChristianRytt
manager: AnnBe
ms.date: 10/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 37c2acb2397b2a0ad69272c0645bd200a8d7910d
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773963"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="1e9de-103">Erste Schritte mit der Planungsoptimierung</span><span class="sxs-lookup"><span data-stu-id="1e9de-103">Get started with Planning Optimization</span></span>

<span data-ttu-id="1e9de-104">Die Funktionalität der Planungsoptimierung unterstützt derzeit nicht alle Funktionen, die in der in Microsoft Dynamics 365 Supply Chain Management integrierten Planungs-Engine verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="1e9de-104">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="1e9de-105">Daher ist es wichtig, dass Sie prüfen, ob der derzeit in der Planungsoptimierung verfügbare Funktionsumfang Ihren Anforderungen entspricht.</span><span class="sxs-lookup"><span data-stu-id="1e9de-105">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="1e9de-106">Standardmäßig ist die Funktionalität der Planungsoptimierung in Dynamics Lifecycle Services (LCS) nicht standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="1e9de-106">By default, the Planning Optimization functionality isn't turned on in Dynamics Lifecycle Services (LCS) by default.</span></span> <span data-ttu-id="1e9de-107">Daher haben Sie die Möglichkeit, Ihre Bewertung durchzuführen, bevor sie eingeschaltet wird.</span><span class="sxs-lookup"><span data-stu-id="1e9de-107">Therefore, you have an opportunity to do your evaluation before it's turned on.</span></span>

<span data-ttu-id="1e9de-108">Schließlich wird die Planungsoptimierung die bestehende integrierte Supply Chain Management Planungs-Engine ersetzen.</span><span class="sxs-lookup"><span data-stu-id="1e9de-108">Eventually, Planning Optimization will replace the existing built-in Supply Chain Management planning engine.</span></span>

<span data-ttu-id="1e9de-109">Bevor Sie die Planungsoptimierung einschalten, empfehlen wir Ihnen dringend, die Ergebnisse der Anpassungsanalyse der Planungsoptimierung auszuwerten.</span><span class="sxs-lookup"><span data-stu-id="1e9de-109">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="1e9de-110">Weitere Informationen finden Sie unter [Planungsoptimierung Fit-Analyse](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="1e9de-110">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="licensing"></a><span data-ttu-id="1e9de-111">Lizenzierung</span><span class="sxs-lookup"><span data-stu-id="1e9de-111">Licensing</span></span>

<span data-ttu-id="1e9de-112">Wenn Sie die Masterplanung mit Ihrer aktuellen Lizenz durchführen können, müssen Sie keine zusätzliche Lizenz kaufen, um mit der Planungsoptimierung zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="1e9de-112">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="1e9de-113">Installieren des Add-Ins</span><span class="sxs-lookup"><span data-stu-id="1e9de-113">Install the add-in</span></span>

<span data-ttu-id="1e9de-114">Um die Planungsoptimierung zu nutzen, installieren Sie das Add-In Planungsoptimierung für Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="1e9de-114">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="1e9de-115">Sie können auf das Add-In aus Ihrem LCS-Projekt zugreifen und die Funktionalität der Planungsoptimierung über die Benutzeroberfläche (UI) von Supply Chain Management einschalten.</span><span class="sxs-lookup"><span data-stu-id="1e9de-115">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

1. <span data-ttu-id="1e9de-116">Melden Sie sich bei LCS an und öffnen Sie die gewünschte Umgebung.</span><span class="sxs-lookup"><span data-stu-id="1e9de-116">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="1e9de-117">Gehen Sie zu **Vollständige Details**.</span><span class="sxs-lookup"><span data-stu-id="1e9de-117">Go to **Full details**.</span></span>
1. <span data-ttu-id="1e9de-118">Wählen Sie **Beibehalten**, oder scrollen Sie nach unten zu den **Umgebungs-Add-Ins** Inforegister.</span><span class="sxs-lookup"><span data-stu-id="1e9de-118">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="1e9de-119">Wählen Sie **Installieren Sie ein neues Add-In**.</span><span class="sxs-lookup"><span data-stu-id="1e9de-119">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="1e9de-120">Wählen Sie **Planungsoptimierung**.</span><span class="sxs-lookup"><span data-stu-id="1e9de-120">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="1e9de-121">Befolgen Sie die Installationsanleitung und erklären Sie sich mit den Allgemeinen Geschäftsbedingungen einverstanden.</span><span class="sxs-lookup"><span data-stu-id="1e9de-121">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="1e9de-122">Wählen Sie **Installieren**.</span><span class="sxs-lookup"><span data-stu-id="1e9de-122">Select **Install**.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="1e9de-123">Integration der Planungsoptimierung</span><span class="sxs-lookup"><span data-stu-id="1e9de-123">Planning Optimization integration</span></span>

<span data-ttu-id="1e9de-124">Um zu konfigurieren, ob das Planungsoptimierungs-Add-In für die Masterplanung verwendet werden soll, gehen Sie zu **Masterplanung** \> **Setup** \> **Planungsoptimierungsintegration** \> **Integrationsparameter**.</span><span class="sxs-lookup"><span data-stu-id="1e9de-124">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization integration** \> **Integration parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="1e9de-125">Verbindungsstatus</span><span class="sxs-lookup"><span data-stu-id="1e9de-125">Connection status</span></span>

<span data-ttu-id="1e9de-126">Der Verbindungsstatus zeigt den aktuellen Status der Verbindung zwischen Supply Chain Management und dem Service Planungsoptimierung an.</span><span class="sxs-lookup"><span data-stu-id="1e9de-126">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="1e9de-127">Die folgende Tabelle zeigt die möglichen Werte.</span><span class="sxs-lookup"><span data-stu-id="1e9de-127">The following table shows the possible values.</span></span>

| <span data-ttu-id="1e9de-128">Verbindungsstatus</span><span class="sxs-lookup"><span data-stu-id="1e9de-128">Connection status</span></span> | <span data-ttu-id="1e9de-129">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1e9de-129">Description</span></span> | <span data-ttu-id="1e9de-130">Kann die Planungsoptimierung genutzt werden?</span><span class="sxs-lookup"><span data-stu-id="1e9de-130">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="1e9de-131">Verbindung hergestellt</span><span class="sxs-lookup"><span data-stu-id="1e9de-131">Connected</span></span> | <span data-ttu-id="1e9de-132">Es wurde eine Verbindung zwischen dem Service Planungsoptimierung und dem Supply Chain Management hergestellt.</span><span class="sxs-lookup"><span data-stu-id="1e9de-132">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="1e9de-133">Ja</span><span class="sxs-lookup"><span data-stu-id="1e9de-133">Yes</span></span> |
| <span data-ttu-id="1e9de-134">Aktivieren der Verbindung</span><span class="sxs-lookup"><span data-stu-id="1e9de-134">Enabling connection</span></span> | <span data-ttu-id="1e9de-135">Eine Aufforderung zum Einschalten der Verbindung zum Dienst Planungsoptimierung ist derzeit in Bearbeitung.</span><span class="sxs-lookup"><span data-stu-id="1e9de-135">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="1e9de-136">Nein</span><span class="sxs-lookup"><span data-stu-id="1e9de-136">No</span></span> |
| <span data-ttu-id="1e9de-137">Verbindung getrennt</span><span class="sxs-lookup"><span data-stu-id="1e9de-137">Disconnected</span></span> | <span data-ttu-id="1e9de-138">Es besteht keine Verbindung zum Service Planungsoptimierung.</span><span class="sxs-lookup"><span data-stu-id="1e9de-138">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="1e9de-139">Die Verbindung kann vom LCS aus eingeschaltet werden, wie bereits in diesem Thema beschrieben.</span><span class="sxs-lookup"><span data-stu-id="1e9de-139">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="1e9de-140">Nein</span><span class="sxs-lookup"><span data-stu-id="1e9de-140">No</span></span> |
| <span data-ttu-id="1e9de-141">Verbindung wird deaktiviert</span><span class="sxs-lookup"><span data-stu-id="1e9de-141">Disabling connection</span></span> | <span data-ttu-id="1e9de-142">Eine Aufforderung zum Deaktivieren der Verbindung zum Dienst Planungsoptimierung ist derzeit in Bearbeitung.</span><span class="sxs-lookup"><span data-stu-id="1e9de-142">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="1e9de-143">Nein</span><span class="sxs-lookup"><span data-stu-id="1e9de-143">No</span></span> |
| <span data-ttu-id="1e9de-144">Status wird abgerufen...</span><span class="sxs-lookup"><span data-stu-id="1e9de-144">Getting status</span></span> | <span data-ttu-id="1e9de-145">Das System wartet auf Statusinformationen vom Service Planungsoptimierung.</span><span class="sxs-lookup"><span data-stu-id="1e9de-145">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="1e9de-146">Nein</span><span class="sxs-lookup"><span data-stu-id="1e9de-146">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="1e9de-147">Die Option Planungsoptimierung verwenden</span><span class="sxs-lookup"><span data-stu-id="1e9de-147">The Use Planning Optimization option</span></span>

<span data-ttu-id="1e9de-148">Die Einstellung der Option **Verwendungsplanoptimierung** bestimmt, welche Planungs-Engine für die Masterplanung verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="1e9de-148">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="1e9de-149">**Ja** - Die Planungsoptimierung wird für die Masterplanung verwendet.</span><span class="sxs-lookup"><span data-stu-id="1e9de-149">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="1e9de-150">**Nein** - Die eingebaute Supply Chain Management Planning Engine wird für die Masterplanung verwendet.</span><span class="sxs-lookup"><span data-stu-id="1e9de-150">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="1e9de-151">Wenn bestehende Planungs-Batchjobs, die für die eingebaute Supply Chain Management Planungs-Engine erstellt wurden, ausgelöst werden, während die Option **Verwendungsplanoptimierung** auf **Ja** gesetzt ist, werden diese Jobs fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="1e9de-151">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="1e9de-152">Integration mit dem Setup</span><span class="sxs-lookup"><span data-stu-id="1e9de-152">Integration with the setup</span></span>

<span data-ttu-id="1e9de-153">Wenn die Vorschau der Planungsoptimierung eingeschaltet ist, erfolgt die Masterplanung mit Hilfe des Add-Ins Planungsoptimierung.</span><span class="sxs-lookup"><span data-stu-id="1e9de-153">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="1e9de-154">In diesem Fall sind die Ergebnisse und Merkmale der Masterplanung betroffen.</span><span class="sxs-lookup"><span data-stu-id="1e9de-154">In this case, master planning results and features are affected.</span></span>

## <a name="related-resources"></a><span data-ttu-id="1e9de-155">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1e9de-155">Related resources</span></span>

[<span data-ttu-id="1e9de-156">Allgemeine Geschäftsbedingungen für die Vorschau</span><span class="sxs-lookup"><span data-stu-id="1e9de-156">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="1e9de-157">Planungsoptimierung – Übersicht</span><span class="sxs-lookup"><span data-stu-id="1e9de-157">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="1e9de-158">Planungsoptimierung Fit-Analyse</span><span class="sxs-lookup"><span data-stu-id="1e9de-158">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="1e9de-159">Planhistorie und Planungsprotokolle anzeigen</span><span class="sxs-lookup"><span data-stu-id="1e9de-159">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="1e9de-160">Filter auf einen Plan anwenden</span><span class="sxs-lookup"><span data-stu-id="1e9de-160">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="1e9de-161">Abbrechen eines Planungsauftrags</span><span class="sxs-lookup"><span data-stu-id="1e9de-161">Cancel a planning job</span></span>](cancel-planning-job.md)
