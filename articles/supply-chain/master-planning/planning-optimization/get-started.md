---
title: Erste Schritte mit der Planungsoptimierung
description: In diesem Thema wird erläutert, wie Sie mit der Verwendung der Funktionalität der Planungsoptimierung beginnen.
author: ChristianRytt
manager: tfehr
ms.date: 02/10/2020
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
ms.openlocfilehash: 4f9124e824a0b6d5035b2567cb19c2c494390d55
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213514"
---
# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="1c67f-103">Erste Schritte mit der Planungsoptimierung</span><span class="sxs-lookup"><span data-stu-id="1c67f-103">Get started with Planning Optimization</span></span>

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1c67f-104">Die Funktionalität der Planungsoptimierung unterstützt derzeit nicht alle Funktionen, die in der in Microsoft Dynamics 365 Supply Chain Management integrierten Planungs-Engine verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="1c67f-104">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="1c67f-105">Daher ist es wichtig, dass Sie prüfen, ob der derzeit in der Planungsoptimierung verfügbare Funktionsumfang Ihren Anforderungen entspricht.</span><span class="sxs-lookup"><span data-stu-id="1c67f-105">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="1c67f-106">Standardmäßig ist die Funktionalität der Planungsoptimierung in Dynamics Lifecycle Services (LCS) nicht standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="1c67f-106">By default, the Planning Optimization functionality isn't turned on in Dynamics Lifecycle Services (LCS) by default.</span></span> <span data-ttu-id="1c67f-107">Daher haben Sie die Möglichkeit, Ihre Bewertung durchzuführen, bevor sie eingeschaltet wird.</span><span class="sxs-lookup"><span data-stu-id="1c67f-107">Therefore, you have an opportunity to do your evaluation before it's turned on.</span></span>

<span data-ttu-id="1c67f-108">Schließlich wird die Planungsoptimierung die bestehende integrierte Supply Chain Management Planungs-Engine ersetzen.</span><span class="sxs-lookup"><span data-stu-id="1c67f-108">Eventually, Planning Optimization will replace the existing built-in Supply Chain Management planning engine.</span></span>

<span data-ttu-id="1c67f-109">Bevor Sie die Planungsoptimierung einschalten, empfehlen wir Ihnen dringend, die Ergebnisse der Anpassungsanalyse der Planungsoptimierung auszuwerten.</span><span class="sxs-lookup"><span data-stu-id="1c67f-109">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="1c67f-110">Weitere Informationen finden Sie unter [Planungsoptimierung Fit-Analyse](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="1c67f-110">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="licensing"></a><span data-ttu-id="1c67f-111">Lizenzierung</span><span class="sxs-lookup"><span data-stu-id="1c67f-111">Licensing</span></span>

<span data-ttu-id="1c67f-112">Wenn Sie die Masterplanung mit Ihrer aktuellen Lizenz durchführen können, müssen Sie keine zusätzliche Lizenz kaufen, um mit der Planungsoptimierung zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="1c67f-112">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="1c67f-113">Installieren des Add-Ins</span><span class="sxs-lookup"><span data-stu-id="1c67f-113">Install the add-in</span></span>

<span data-ttu-id="1c67f-114">Um die Planungsoptimierung zu nutzen, installieren Sie das Add-In Planungsoptimierung für Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="1c67f-114">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="1c67f-115">Sie können auf das Add-In aus Ihrem LCS-Projekt zugreifen und die Funktionalität der Planungsoptimierung über die Benutzeroberfläche (UI) von Supply Chain Management einschalten.</span><span class="sxs-lookup"><span data-stu-id="1c67f-115">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

> [!NOTE]
> <span data-ttu-id="1c67f-116">Die Voraussetzung für die Planungsoptimierung ist eine LCS-fähige Hochverfügbarkeitsumgebung (keine OneBox-Umgebung) mit Dynamics 365 Supply Chain Management Version 10.0.7 oder höher.</span><span class="sxs-lookup"><span data-stu-id="1c67f-116">The requirement for Planning Optimization is an LCS enabled high-availability environment (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span>

1. <span data-ttu-id="1c67f-117">Melden Sie sich bei LCS an und öffnen Sie die gewünschte Umgebung.</span><span class="sxs-lookup"><span data-stu-id="1c67f-117">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="1c67f-118">Gehen Sie zu **Vollständige Details**.</span><span class="sxs-lookup"><span data-stu-id="1c67f-118">Go to **Full details**.</span></span>
1. <span data-ttu-id="1c67f-119">Scrollen Sie zum Inforegister **Umgebungs-Add-Ins**.</span><span class="sxs-lookup"><span data-stu-id="1c67f-119">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="1c67f-120">Wählen Sie **Installieren Sie ein neues Add-In**.</span><span class="sxs-lookup"><span data-stu-id="1c67f-120">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="1c67f-121">Wählen Sie **Planungsoptimierung**.</span><span class="sxs-lookup"><span data-stu-id="1c67f-121">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="1c67f-122">Befolgen Sie die Installationsanleitung und erklären Sie sich mit den Allgemeinen Geschäftsbedingungen einverstanden.</span><span class="sxs-lookup"><span data-stu-id="1c67f-122">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="1c67f-123">Wählen Sie **Installieren**.</span><span class="sxs-lookup"><span data-stu-id="1c67f-123">Select **Install**.</span></span>
1. <span data-ttu-id="1c67f-124">Auf dem Inforegister **Umgebungs-Add-Ins** sollte die Installation der Planungsoptimierung angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="1c67f-124">On the **Environment add-ins** FastTab you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="1c67f-125">Nach ein paar Minuten sollte sich **Wird installiert ...** in **Installiert** ändern (möglicherweise müssen Sie die Seite aktualisieren).</span><span class="sxs-lookup"><span data-stu-id="1c67f-125">After a few minutes **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="1c67f-126">Nach der Installation können Sie die Planungsoptimierung in Dynamics 365 Supply Chain Management aktivieren.</span><span class="sxs-lookup"><span data-stu-id="1c67f-126">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="1c67f-127">Integration der Planungsoptimierung</span><span class="sxs-lookup"><span data-stu-id="1c67f-127">Planning Optimization integration</span></span>

<span data-ttu-id="1c67f-128">Um zu konfigurieren, ob das Planungsoptimierungs-Add-In für die Masterplanung verwendet werden soll, gehen Sie zu **Produktprogrammplanung** \> **Setup** \> **Parameter für Planungsoptimierung**.</span><span class="sxs-lookup"><span data-stu-id="1c67f-128">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="1c67f-129">Verbindungsstatus</span><span class="sxs-lookup"><span data-stu-id="1c67f-129">Connection status</span></span>

<span data-ttu-id="1c67f-130">Der Verbindungsstatus zeigt den aktuellen Status der Verbindung zwischen Supply Chain Management und dem Service Planungsoptimierung an.</span><span class="sxs-lookup"><span data-stu-id="1c67f-130">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="1c67f-131">Die folgende Tabelle zeigt die möglichen Werte.</span><span class="sxs-lookup"><span data-stu-id="1c67f-131">The following table shows the possible values.</span></span>

| <span data-ttu-id="1c67f-132">Verbindungsstatus</span><span class="sxs-lookup"><span data-stu-id="1c67f-132">Connection status</span></span> | <span data-ttu-id="1c67f-133">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1c67f-133">Description</span></span> | <span data-ttu-id="1c67f-134">Kann die Planungsoptimierung genutzt werden?</span><span class="sxs-lookup"><span data-stu-id="1c67f-134">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="1c67f-135">Verbindung hergestellt</span><span class="sxs-lookup"><span data-stu-id="1c67f-135">Connected</span></span> | <span data-ttu-id="1c67f-136">Es wurde eine Verbindung zwischen dem Service Planungsoptimierung und dem Supply Chain Management hergestellt.</span><span class="sxs-lookup"><span data-stu-id="1c67f-136">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="1c67f-137">Ja</span><span class="sxs-lookup"><span data-stu-id="1c67f-137">Yes</span></span> |
| <span data-ttu-id="1c67f-138">Aktivieren der Verbindung</span><span class="sxs-lookup"><span data-stu-id="1c67f-138">Enabling connection</span></span> | <span data-ttu-id="1c67f-139">Eine Aufforderung zum Einschalten der Verbindung zum Dienst Planungsoptimierung ist derzeit in Bearbeitung.</span><span class="sxs-lookup"><span data-stu-id="1c67f-139">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="1c67f-140">Nein</span><span class="sxs-lookup"><span data-stu-id="1c67f-140">No</span></span> |
| <span data-ttu-id="1c67f-141">Verbindung getrennt</span><span class="sxs-lookup"><span data-stu-id="1c67f-141">Disconnected</span></span> | <span data-ttu-id="1c67f-142">Es besteht keine Verbindung zum Service Planungsoptimierung.</span><span class="sxs-lookup"><span data-stu-id="1c67f-142">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="1c67f-143">Die Verbindung kann vom LCS aus eingeschaltet werden, wie bereits in diesem Thema beschrieben.</span><span class="sxs-lookup"><span data-stu-id="1c67f-143">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="1c67f-144">Nein</span><span class="sxs-lookup"><span data-stu-id="1c67f-144">No</span></span> |
| <span data-ttu-id="1c67f-145">Verbindung wird deaktiviert</span><span class="sxs-lookup"><span data-stu-id="1c67f-145">Disabling connection</span></span> | <span data-ttu-id="1c67f-146">Eine Aufforderung zum Deaktivieren der Verbindung zum Dienst Planungsoptimierung ist derzeit in Bearbeitung.</span><span class="sxs-lookup"><span data-stu-id="1c67f-146">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="1c67f-147">Nein</span><span class="sxs-lookup"><span data-stu-id="1c67f-147">No</span></span> |
| <span data-ttu-id="1c67f-148">Status wird abgerufen...</span><span class="sxs-lookup"><span data-stu-id="1c67f-148">Getting status</span></span> | <span data-ttu-id="1c67f-149">Das System wartet auf Statusinformationen vom Service Planungsoptimierung.</span><span class="sxs-lookup"><span data-stu-id="1c67f-149">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="1c67f-150">Nein</span><span class="sxs-lookup"><span data-stu-id="1c67f-150">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="1c67f-151">Die Option Planungsoptimierung verwenden</span><span class="sxs-lookup"><span data-stu-id="1c67f-151">The Use Planning Optimization option</span></span>

<span data-ttu-id="1c67f-152">Die Einstellung der Option **Verwendungsplanoptimierung** bestimmt, welche Planungs-Engine für die Masterplanung verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="1c67f-152">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="1c67f-153">**Ja** - Die Planungsoptimierung wird für die Masterplanung verwendet.</span><span class="sxs-lookup"><span data-stu-id="1c67f-153">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="1c67f-154">**Nein** - Die eingebaute Supply Chain Management Planning Engine wird für die Masterplanung verwendet.</span><span class="sxs-lookup"><span data-stu-id="1c67f-154">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="1c67f-155">Wenn bestehende Planungs-Batchjobs, die für die eingebaute Supply Chain Management Planungs-Engine erstellt wurden, ausgelöst werden, während die Option **Verwendungsplanoptimierung** auf **Ja** gesetzt ist, werden diese Jobs fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="1c67f-155">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="1c67f-156">Integration mit dem Setup</span><span class="sxs-lookup"><span data-stu-id="1c67f-156">Integration with the setup</span></span>

<span data-ttu-id="1c67f-157">Wenn die Vorschau der Planungsoptimierung eingeschaltet ist, erfolgt die Masterplanung mit Hilfe des Add-Ins Planungsoptimierung.</span><span class="sxs-lookup"><span data-stu-id="1c67f-157">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="1c67f-158">In diesem Fall sind die Ergebnisse und Merkmale der Masterplanung betroffen.</span><span class="sxs-lookup"><span data-stu-id="1c67f-158">In this case, master planning results and features are affected.</span></span>

## <a name="related-resources"></a><span data-ttu-id="1c67f-159">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1c67f-159">Related resources</span></span>

[<span data-ttu-id="1c67f-160">Allgemeine Geschäftsbedingungen für die Vorschau</span><span class="sxs-lookup"><span data-stu-id="1c67f-160">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="1c67f-161">Planungsoptimierung – Übersicht</span><span class="sxs-lookup"><span data-stu-id="1c67f-161">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="1c67f-162">Planungsoptimierung Fit-Analyse</span><span class="sxs-lookup"><span data-stu-id="1c67f-162">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="1c67f-163">Planhistorie und Planungsprotokolle anzeigen</span><span class="sxs-lookup"><span data-stu-id="1c67f-163">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="1c67f-164">Filter auf einen Plan anwenden</span><span class="sxs-lookup"><span data-stu-id="1c67f-164">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="1c67f-165">Abbrechen eines Planungsauftrags</span><span class="sxs-lookup"><span data-stu-id="1c67f-165">Cancel a planning job</span></span>](cancel-planning-job.md)
