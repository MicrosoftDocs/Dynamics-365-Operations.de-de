---
title: Erste Schritte mit der Planungsoptimierung
description: In diesem Thema wird erläutert, wie Sie mit der Verwendung der Funktionalität der Planungsoptimierung beginnen.
author: ChristianRytt
manager: tfehr
ms.date: 05/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: ce1bbb18e9a448e84d001a4195421d2b0e4af5be
ms.sourcegitcommit: c0d37fdd70f3dec4605fdee6f981f84a49be9b9e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/06/2020
ms.locfileid: "3339877"
---
# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="e65de-103">Erste Schritte mit der Planungsoptimierung</span><span class="sxs-lookup"><span data-stu-id="e65de-103">Get started with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e65de-104">Die Funktionalität der Planungsoptimierung unterstützt derzeit nicht alle Funktionen, die in der in Microsoft Dynamics 365 Supply Chain Management integrierten Planungs-Engine verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="e65de-104">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="e65de-105">Daher ist es wichtig, dass Sie prüfen, ob der derzeit in der Planungsoptimierung verfügbare Funktionsumfang Ihren Anforderungen entspricht.</span><span class="sxs-lookup"><span data-stu-id="e65de-105">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="e65de-106">Standardmäßig ist die Funktionalität der Planungsoptimierung in Dynamics Lifecycle Services (LCS) nicht standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="e65de-106">By default, the Planning Optimization functionality isn't turned on in Dynamics Lifecycle Services (LCS) by default.</span></span> <span data-ttu-id="e65de-107">Daher haben Sie die Möglichkeit, Ihre Bewertung durchzuführen, bevor sie eingeschaltet wird.</span><span class="sxs-lookup"><span data-stu-id="e65de-107">Therefore, you have an opportunity to do your evaluation before it's turned on.</span></span>

<span data-ttu-id="e65de-108">Schließlich wird die Planungsoptimierung die bestehende integrierte Supply Chain Management Planungs-Engine ersetzen.</span><span class="sxs-lookup"><span data-stu-id="e65de-108">Eventually, Planning Optimization will replace the existing built-in Supply Chain Management planning engine.</span></span>

<span data-ttu-id="e65de-109">Bevor Sie die Planungsoptimierung einschalten, empfehlen wir Ihnen dringend, die Ergebnisse der Anpassungsanalyse der Planungsoptimierung auszuwerten.</span><span class="sxs-lookup"><span data-stu-id="e65de-109">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="e65de-110">Weitere Informationen finden Sie unter [Planungsoptimierung Fit-Analyse](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="e65de-110">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="availability"></a><span data-ttu-id="e65de-111">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="e65de-111">Availability</span></span>
<span data-ttu-id="e65de-112">Die Planungsoptimierung ist derzeit in den folgenden geografischen Azure-Regionen verfügbar: USA, Kanada, Europa, Großbritannien und Australien.</span><span class="sxs-lookup"><span data-stu-id="e65de-112">Planning Optimization is currently available in the following Azure geographies: United States, Canada, Europe, United Kingdom, and Australia.</span></span> <span data-ttu-id="e65de-113">Wenn Sie versuchen, das Add-In aus einer anderen geografischen Region zu installieren, zeigt LCS die Meldung an, dass diese geografische Region nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="e65de-113">If you try to install the add-in from another geographic region, then LCS will show a message that this geographic is not supported.</span></span>

<span data-ttu-id="e65de-114">Beachten Sie, dass Planungsoptimierung keine lokalen Bereitstellungen von Dynamics 365 Supply Chain Management unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e65de-114">Note that Planning Optimization does not support on-premises deployments of Dynamics 365 Supply Chain Management.</span></span>

### <a name="licensing"></a><span data-ttu-id="e65de-115">Lizenzierung</span><span class="sxs-lookup"><span data-stu-id="e65de-115">Licensing</span></span>

<span data-ttu-id="e65de-116">Wenn Sie die Masterplanung mit Ihrer aktuellen Lizenz durchführen können, müssen Sie keine zusätzliche Lizenz kaufen, um mit der Planungsoptimierung zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="e65de-116">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="e65de-117">Installieren des Add-Ins</span><span class="sxs-lookup"><span data-stu-id="e65de-117">Install the add-in</span></span>

<span data-ttu-id="e65de-118">Um die Planungsoptimierung zu nutzen, installieren Sie das Add-In Planungsoptimierung für Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e65de-118">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="e65de-119">Sie können auf das Add-In aus Ihrem LCS-Projekt zugreifen und die Funktionalität der Planungsoptimierung über die Benutzeroberfläche (UI) von Supply Chain Management einschalten.</span><span class="sxs-lookup"><span data-stu-id="e65de-119">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

> [!NOTE]
> <span data-ttu-id="e65de-120">Die Voraussetzung für die Planungsoptimierung ist eine LCS-fähige Hochverfügbarkeitsumgebung, Ebene 2 oder höher (keine OneBox-Umgebung) mit Dynamics 365 Supply Chain Management Version 10.0.7 oder höher.</span><span class="sxs-lookup"><span data-stu-id="e65de-120">The requirement for Planning Optimization is an LCS enabled high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="e65de-121">Wenn Sie versuchen, das Add-In in einer OneBox-Umgebung zu installieren, wird die Installation nicht abgeschlossen und Sie müssen die Installation abbrechen.</span><span class="sxs-lookup"><span data-stu-id="e65de-121">If you try to install the add-in on a OneBox environment, the installation will not complete and you will need to cancel the installation.</span></span>

1. <span data-ttu-id="e65de-122">Melden Sie sich bei LCS an und öffnen Sie die gewünschte Umgebung.</span><span class="sxs-lookup"><span data-stu-id="e65de-122">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="e65de-123">Gehen Sie zu **Vollständige Details**.</span><span class="sxs-lookup"><span data-stu-id="e65de-123">Go to **Full details**.</span></span>
1. <span data-ttu-id="e65de-124">Scrollen Sie zum Inforegister **Umgebungs-Add-Ins**.</span><span class="sxs-lookup"><span data-stu-id="e65de-124">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="e65de-125">Wählen Sie **Installieren Sie ein neues Add-In**.</span><span class="sxs-lookup"><span data-stu-id="e65de-125">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="e65de-126">Wählen Sie **Planungsoptimierung**.</span><span class="sxs-lookup"><span data-stu-id="e65de-126">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="e65de-127">Befolgen Sie die Installationsanleitung und erklären Sie sich mit den Allgemeinen Geschäftsbedingungen einverstanden.</span><span class="sxs-lookup"><span data-stu-id="e65de-127">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="e65de-128">Wählen Sie **Installieren**.</span><span class="sxs-lookup"><span data-stu-id="e65de-128">Select **Install**.</span></span>
1. <span data-ttu-id="e65de-129">Auf dem Inforegister **Umgebungs-Add-Ins** sollte die Installation der Planungsoptimierung angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="e65de-129">On the **Environment add-ins** FastTab you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="e65de-130">Nach ein paar Minuten sollte sich **Wird installiert ...** in **Installiert** ändern (möglicherweise müssen Sie die Seite aktualisieren).</span><span class="sxs-lookup"><span data-stu-id="e65de-130">After a few minutes **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="e65de-131">Nach der Installation können Sie die Planungsoptimierung in Dynamics 365 Supply Chain Management aktivieren.</span><span class="sxs-lookup"><span data-stu-id="e65de-131">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="e65de-132">Integration der Planungsoptimierung</span><span class="sxs-lookup"><span data-stu-id="e65de-132">Planning Optimization integration</span></span>

<span data-ttu-id="e65de-133">Um zu konfigurieren, ob das Planungsoptimierungs-Add-In für die Masterplanung verwendet werden soll, gehen Sie zu **Produktprogrammplanung** \> **Setup** \> **Parameter für Planungsoptimierung**.</span><span class="sxs-lookup"><span data-stu-id="e65de-133">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="e65de-134">Verbindungsstatus</span><span class="sxs-lookup"><span data-stu-id="e65de-134">Connection status</span></span>

<span data-ttu-id="e65de-135">Der Verbindungsstatus zeigt den aktuellen Status der Verbindung zwischen Supply Chain Management und dem Service Planungsoptimierung an.</span><span class="sxs-lookup"><span data-stu-id="e65de-135">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="e65de-136">Die folgende Tabelle zeigt die möglichen Werte.</span><span class="sxs-lookup"><span data-stu-id="e65de-136">The following table shows the possible values.</span></span>

| <span data-ttu-id="e65de-137">Verbindungsstatus</span><span class="sxs-lookup"><span data-stu-id="e65de-137">Connection status</span></span> | <span data-ttu-id="e65de-138">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e65de-138">Description</span></span> | <span data-ttu-id="e65de-139">Kann die Planungsoptimierung genutzt werden?</span><span class="sxs-lookup"><span data-stu-id="e65de-139">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="e65de-140">Verbindung hergestellt</span><span class="sxs-lookup"><span data-stu-id="e65de-140">Connected</span></span> | <span data-ttu-id="e65de-141">Es wurde eine Verbindung zwischen dem Service Planungsoptimierung und dem Supply Chain Management hergestellt.</span><span class="sxs-lookup"><span data-stu-id="e65de-141">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="e65de-142">Ja</span><span class="sxs-lookup"><span data-stu-id="e65de-142">Yes</span></span> |
| <span data-ttu-id="e65de-143">Aktivieren der Verbindung</span><span class="sxs-lookup"><span data-stu-id="e65de-143">Enabling connection</span></span> | <span data-ttu-id="e65de-144">Eine Aufforderung zum Einschalten der Verbindung zum Dienst Planungsoptimierung ist derzeit in Bearbeitung.</span><span class="sxs-lookup"><span data-stu-id="e65de-144">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="e65de-145">Nein</span><span class="sxs-lookup"><span data-stu-id="e65de-145">No</span></span> |
| <span data-ttu-id="e65de-146">Verbindung getrennt</span><span class="sxs-lookup"><span data-stu-id="e65de-146">Disconnected</span></span> | <span data-ttu-id="e65de-147">Es besteht keine Verbindung zum Service Planungsoptimierung.</span><span class="sxs-lookup"><span data-stu-id="e65de-147">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="e65de-148">Die Verbindung kann vom LCS aus eingeschaltet werden, wie bereits in diesem Thema beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e65de-148">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="e65de-149">Nein</span><span class="sxs-lookup"><span data-stu-id="e65de-149">No</span></span> |
| <span data-ttu-id="e65de-150">Verbindung wird deaktiviert</span><span class="sxs-lookup"><span data-stu-id="e65de-150">Disabling connection</span></span> | <span data-ttu-id="e65de-151">Eine Aufforderung zum Deaktivieren der Verbindung zum Dienst Planungsoptimierung ist derzeit in Bearbeitung.</span><span class="sxs-lookup"><span data-stu-id="e65de-151">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="e65de-152">Nein</span><span class="sxs-lookup"><span data-stu-id="e65de-152">No</span></span> |
| <span data-ttu-id="e65de-153">Status wird abgerufen...</span><span class="sxs-lookup"><span data-stu-id="e65de-153">Getting status</span></span> | <span data-ttu-id="e65de-154">Das System wartet auf Statusinformationen vom Service Planungsoptimierung.</span><span class="sxs-lookup"><span data-stu-id="e65de-154">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="e65de-155">Nein</span><span class="sxs-lookup"><span data-stu-id="e65de-155">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="e65de-156">Die Option Planungsoptimierung verwenden</span><span class="sxs-lookup"><span data-stu-id="e65de-156">The Use Planning Optimization option</span></span>

<span data-ttu-id="e65de-157">Die Einstellung der Option **Verwendungsplanoptimierung** bestimmt, welche Planungs-Engine für die Masterplanung verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="e65de-157">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="e65de-158">**Ja** - Die Planungsoptimierung wird für die Masterplanung verwendet.</span><span class="sxs-lookup"><span data-stu-id="e65de-158">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="e65de-159">**Nein** - Die eingebaute Supply Chain Management Planning Engine wird für die Masterplanung verwendet.</span><span class="sxs-lookup"><span data-stu-id="e65de-159">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="e65de-160">Wenn bestehende Planungs-Batchjobs, die für die eingebaute Supply Chain Management Planungs-Engine erstellt wurden, ausgelöst werden, während die Option **Verwendungsplanoptimierung** auf **Ja** gesetzt ist, werden diese Jobs fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="e65de-160">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="e65de-161">Integration mit dem Setup</span><span class="sxs-lookup"><span data-stu-id="e65de-161">Integration with the setup</span></span>

<span data-ttu-id="e65de-162">Wenn die Vorschau der Planungsoptimierung eingeschaltet ist, erfolgt die Masterplanung mit Hilfe des Add-Ins Planungsoptimierung.</span><span class="sxs-lookup"><span data-stu-id="e65de-162">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="e65de-163">In diesem Fall sind die Ergebnisse und Merkmale der Masterplanung betroffen.</span><span class="sxs-lookup"><span data-stu-id="e65de-163">In this case, master planning results and features are affected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e65de-164">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e65de-164">Additional resources</span></span>

[<span data-ttu-id="e65de-165">Allgemeine Geschäftsbedingungen für die Vorschau</span><span class="sxs-lookup"><span data-stu-id="e65de-165">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="e65de-166">Übersicht zur Planungsoptimierung</span><span class="sxs-lookup"><span data-stu-id="e65de-166">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="e65de-167">Planungsoptimierung Fit-Analyse</span><span class="sxs-lookup"><span data-stu-id="e65de-167">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="e65de-168">Planhistorie und Planungsprotokolle anzeigen</span><span class="sxs-lookup"><span data-stu-id="e65de-168">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="e65de-169">Filter auf einen Plan anwenden</span><span class="sxs-lookup"><span data-stu-id="e65de-169">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="e65de-170">Abbrechen eines Planungsauftrags</span><span class="sxs-lookup"><span data-stu-id="e65de-170">Cancel a planning job</span></span>](cancel-planning-job.md)
