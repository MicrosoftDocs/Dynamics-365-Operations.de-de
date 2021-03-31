---
title: Mobiler Arbeitsbereich für die Kostensteuerung
description: Dieses Thema enthält Informationen zur Kostensteuerung im mobilen Arbeitsbereich. Dieser Arbeitsbereich Kostenstellenmanager zeigt Informationen über die Kostenstellenleistung, jederzeit und überall.
author: AndersGirke
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMMobileCostObjectOverviewDetailsCurrentPeriod, CAMMobileCostObjectList, CAMMobileCostObjectOverviewDetailsPreviousPeriod, CAMMobileCostObjectOverview, CAMMobileCostObjectOverviewDetailsYearToDate, CAMMobileCostControlWorkspaceConfiguration
audience: Application User
ms.reviewer: roschlom
ms.custom: 267114
ms.assetid: 612f2988-b2b9-420d-9825-40b99dc0e204
ms.search.region: global
ms.author: aevengir
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: f75a868acd8ae7e77c7080e2afe81788490bcccb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5226412"
---
# <a name="cost-controlling-mobile-workspace"></a><span data-ttu-id="4dfdc-104">Mobiler Arbeitsbereich für die Kostensteuerung</span><span class="sxs-lookup"><span data-stu-id="4dfdc-104">Cost controlling mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4dfdc-105">Dieses Thema enthält Informationen zur **Kostensteuerung** im mobilen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="4dfdc-105">This topic provides information about the **Cost controlling** mobile workspace.</span></span> <span data-ttu-id="4dfdc-106">Dieser Arbeitsbereich Kostenstellenmanager zeigt Informationen über die Kostenstellenleistung, jederzeit und überall.</span><span class="sxs-lookup"><span data-stu-id="4dfdc-106">This workspace lets cost center managers view information about cost center performance anytime and anywhere.</span></span>

<span data-ttu-id="4dfdc-107">Dieser mobile Arbeitsbereich soll mit der Finance and Operations Mobile-App verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4dfdc-107">This mobile workspace is intended to be used with the Finance and Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="4dfdc-108">Übersicht</span><span class="sxs-lookup"><span data-stu-id="4dfdc-108">Overview</span></span>
<span data-ttu-id="4dfdc-109">Der Arbeitsbereich **Kostensteuerung** enthält eine einzige Ansicht der Leistung der aktuellen Kostenstellen aus dem Vergleich von Ist-Kosten im Vergleich zu den geplanten Kosten.</span><span class="sxs-lookup"><span data-stu-id="4dfdc-109">The **Cost controlling** mobile workspace provides an instant view of the current performance of cost centers by comparing actual costs against the budgeted costs.</span></span> <span data-ttu-id="4dfdc-110">Sie können den Status einzelner Kostenelemente mit Detailinformationen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="4dfdc-110">You can drill down to the status of individual cost elements.</span></span>

<span data-ttu-id="4dfdc-111">Zum Beispiel empfängt ein Mitarbeiter eine Einladung zu einer internationalen Konferenz, aber die Organisation muss alle Reisespesen enthalten.</span><span class="sxs-lookup"><span data-stu-id="4dfdc-111">For example, an employee receives an invitation to an international conference, but the organization must cover all the travel expenses.</span></span> <span data-ttu-id="4dfdc-112">Der Mitarbeiter fragt den Vorgesetzten, ob er an der Konferenz teilnehmen darf.</span><span class="sxs-lookup"><span data-stu-id="4dfdc-112">The employee asks their manager whether they can attend the conference.</span></span> <span data-ttu-id="4dfdc-113">Der Vorgesetzte öffnet schnell den Arbeitsbereich **Kostenkontrolle** auf seinem Mobiltelefon, um festzustellen, ob er das Budget hat, und der Mitarbeiter die Konferenz besuchen kann.</span><span class="sxs-lookup"><span data-stu-id="4dfdc-113">The manager opens the **Cost controlling** mobile workspace on their mobile device to see whether there is budget for the employee to attend the conference.</span></span>

### <a name="data-security"></a><span data-ttu-id="4dfdc-114">Datensicherheit</span><span class="sxs-lookup"><span data-stu-id="4dfdc-114">Data security</span></span>
<span data-ttu-id="4dfdc-115">Die Daten im mobilen Arbeitsbereich **Kostensteuerung** werden mit Anmeldeinformationen geschützt.</span><span class="sxs-lookup"><span data-stu-id="4dfdc-115">The data in the **Cost controlling** mobile workspace is secured through user credentials.</span></span> <span data-ttu-id="4dfdc-116">Ein Kostenstellenmanager kann nur Daten für seine eigene Kostenstelle sehen.</span><span class="sxs-lookup"><span data-stu-id="4dfdc-116">Cost center managers are allowed to see data only for their own cost center.</span></span> <span data-ttu-id="4dfdc-117">Die Zugriffsebenensicherheit wird im Modul **Kostenrechnung** verwaltet.</span><span class="sxs-lookup"><span data-stu-id="4dfdc-117">The access-level security is managed in the **Cost accounting** module.</span></span>

<span data-ttu-id="4dfdc-118">Buchhalter definieren den mobilen Arbeitsbereich **Kostensteuerung** im Modul **Buchhaltungskosten**.</span><span class="sxs-lookup"><span data-stu-id="4dfdc-118">Cost accountants define the configuration of the **Cost controlling** mobile workspace in the **Cost accounting** module.</span></span> <span data-ttu-id="4dfdc-119">Nachdem der Arbeitsbereich auf der App veröffentlicht ist, ist er in der mobilen App für Microsoft Dynamics 365 for Operations verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4dfdc-119">After the workspace is published to the mobile app, it's available in the app.</span></span> <span data-ttu-id="4dfdc-120">Dadurch wird sichergestellt, dass alle Kostenstellenmanager in der gleichen Organisation Daten im selben Format sehen.</span><span class="sxs-lookup"><span data-stu-id="4dfdc-120">Therefore, all cost center managers in the organization can view data in the same format.</span></span>

### <a name="actions-views-and-links"></a><span data-ttu-id="4dfdc-121">Aktivitäten, Ansichten und Links</span><span class="sxs-lookup"><span data-stu-id="4dfdc-121">Actions, views, and links</span></span>
<span data-ttu-id="4dfdc-122">Der mobile Arbeitsbereich **Kostensteuerung** bietet folgende Aktivitäten, Ansichten und Links:</span><span class="sxs-lookup"><span data-stu-id="4dfdc-122">The **Cost controlling** mobile workspace provides the following actions, views, and links:</span></span>

-   <span data-ttu-id="4dfdc-123">**Aktivitäten:**</span><span class="sxs-lookup"><span data-stu-id="4dfdc-123">**Actions:**</span></span>

    -   <span data-ttu-id="4dfdc-124">Verwenden Sie **Konfiguration auswählen**, um ein Layout auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="4dfdc-124">Use **Select configuration** to select a layout.</span></span>
    -   <span data-ttu-id="4dfdc-125">Verwenden Sie **Kostenträger auswählen**, um die Daten auszuwählen, nach denen Kostenstellen gefiltert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4dfdc-125">Use **Select cost object** to select the cost centers to filter data on.</span></span>
    
        > [!NOTE]
        > <span data-ttu-id="4dfdc-126">Die Kostenstellen, die in der Liste angezeigt werden, hängen vom Zugriff ab, der im Modul **Kostenrechnung** gewährt wird.</span><span class="sxs-lookup"><span data-stu-id="4dfdc-126">The cost centers that appear in the list depend on the access that is granted in the **Cost accounting** module.</span></span>

-   <span data-ttu-id="4dfdc-127">**Ansichten:** Auf Grundlage der ausgewählten Aktivitäten und der Konfiguration im Modul **Kostenrechnung** können Sie folgende Informationen in den Karten anzeigen:</span><span class="sxs-lookup"><span data-stu-id="4dfdc-127">**Views:** Based on the actions that are selected and the configuration in the **Cost accounting** module, you can view the following information on the cards:</span></span>

    -   <span data-ttu-id="4dfdc-128">Ist-Wert verglichen mit Budget (aktuelle Periode)</span><span class="sxs-lookup"><span data-stu-id="4dfdc-128">Actual vs budget (current period)</span></span>
    -   <span data-ttu-id="4dfdc-129">Ist-Wert verglichen mit überarbeitetem Budget (aktuelle Periode)</span><span class="sxs-lookup"><span data-stu-id="4dfdc-129">Actual vs revised budget (current period)</span></span>
    -   <span data-ttu-id="4dfdc-130">Ist-Wert verglichen mit Budget (vorherige Periode)</span><span class="sxs-lookup"><span data-stu-id="4dfdc-130">Actual vs budget (previous period)</span></span>
    -   <span data-ttu-id="4dfdc-131">Aktuelle Periode verglichen mit überarbeitetem Budget (vorherige Periode)</span><span class="sxs-lookup"><span data-stu-id="4dfdc-131">Actual vs revised budget (previous period)</span></span>
    -   <span data-ttu-id="4dfdc-132">Istwert und Budget (seit Jahresbeginn)</span><span class="sxs-lookup"><span data-stu-id="4dfdc-132">Actual vs budget (year to date)</span></span>
    -   <span data-ttu-id="4dfdc-133">Istwert und überarbeitetes Budget (Seit Jahresbeginn)</span><span class="sxs-lookup"><span data-stu-id="4dfdc-133">Actual vs revised budget (year to date)</span></span>

    <span data-ttu-id="4dfdc-134">Die folgenden Beträge werden für jede Karte angezeigt: Ist, Budget, Abweichung und Abweichung %.</span><span class="sxs-lookup"><span data-stu-id="4dfdc-134">The following amounts are shown on every card: Actual, Budget, Variance, and Variance %.</span></span>

-   <span data-ttu-id="4dfdc-135">**Verknüpfungen:**</span><span class="sxs-lookup"><span data-stu-id="4dfdc-135">**Links:**</span></span>

    -   <span data-ttu-id="4dfdc-136">Details für aktuelle Periode</span><span class="sxs-lookup"><span data-stu-id="4dfdc-136">Details for current period</span></span>
    -   <span data-ttu-id="4dfdc-137">Details für vorherige Periode</span><span class="sxs-lookup"><span data-stu-id="4dfdc-137">Details for previous period</span></span>
    -   <span data-ttu-id="4dfdc-138">Details für Jahr bis jetzt</span><span class="sxs-lookup"><span data-stu-id="4dfdc-138">Details for year to date</span></span>

    <span data-ttu-id="4dfdc-139">Wenn Sie eine Verknüpfung aktivieren, wird für jeden Ausgaben eine Karte angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4dfdc-139">When you select a link, a card is shown for each cost element.</span></span> <span data-ttu-id="4dfdc-140">Die folgenden Beträge werden in den jeweiligen Karten angezeigt: Ist, Budget, Planabweichung, Planabweichung %, überarbeitetes Budget, Abweichung vom überarbeiteten Budget und Abweichung vom überarbeiteten Budget %.</span><span class="sxs-lookup"><span data-stu-id="4dfdc-140">The following amounts are shown on every card: Actual, Budget, Budget variance, Budget variance %, Revised budget, Revised budget variance, and Revised budget variance %.</span></span>
    
    <span data-ttu-id="4dfdc-141">[![Karte für ein Kostenelement](./media/Cost-controlling.png)](./media/Cost-controlling.png)</span><span class="sxs-lookup"><span data-stu-id="4dfdc-141">[![Card for a cost element](./media/Cost-controlling.png)](./media/Cost-controlling.png)</span></span>

## <a name="prerequisites"></a><span data-ttu-id="4dfdc-142">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="4dfdc-142">Prerequisites</span></span>
<span data-ttu-id="4dfdc-143">Die Voraussetzungen unterscheiden sich basierend auf der Version von Microsoft Dynamics 365, die für Ihre Organisation bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="4dfdc-143">The prerequisites differ, based on the version of Microsoft Dynamics 365 that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-finance"></a><span data-ttu-id="4dfdc-144">Voraussetzungen, wenn Sie Microsoft Dynamics 365 Finance verwenden</span><span class="sxs-lookup"><span data-stu-id="4dfdc-144">Prerequisites if you use Microsoft Dynamics 365 Finance</span></span>
<span data-ttu-id="4dfdc-145">Wenn Finance für Ihre Organisation bereitgestellt wurde, muss der Systemadministrator den mobilen Arbeitsbereich **Kostensteuerung** veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="4dfdc-145">If Finance has been deployed for your organization, the system administrator must publish the **Cost controlling** mobile workspace.</span></span> <span data-ttu-id="4dfdc-146">Anweisungen finden Sie unter [Einen mobilen Arbeitsbereich veröffentlichen](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="4dfdc-146">For instructions, see [Publish a mobile workspace](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span></span>

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="4dfdc-147">Voraussetzungen, wenn Sie Version 1611 mit Plattformupdate 3 oder höher verwenden</span><span class="sxs-lookup"><span data-stu-id="4dfdc-147">Prerequisites if you use version 1611 with Platform update 3 or later</span></span>
<span data-ttu-id="4dfdc-148">Wenn Version 1611 mit Plattformupdate 3 oder höher für Ihre Organisation bereitgestellt wurde, muss der Systemadministrator die folgenden Voraussetzungen erfüllen.</span><span class="sxs-lookup"><span data-stu-id="4dfdc-148">If version 1611 with Platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4dfdc-149">Voraussetzung</span><span class="sxs-lookup"><span data-stu-id="4dfdc-149">Prerequisite</span></span></th>
<th><span data-ttu-id="4dfdc-150">Rolle</span><span class="sxs-lookup"><span data-stu-id="4dfdc-150">Role</span></span></th>
<th><span data-ttu-id="4dfdc-151">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4dfdc-151">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4dfdc-152">Implementieren Sie KB 4013633.</span><span class="sxs-lookup"><span data-stu-id="4dfdc-152">Implement KB 4013633.</span></span></td>
<td><span data-ttu-id="4dfdc-153">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="4dfdc-153">System administrator</span></span></td>

<td><span data-ttu-id="4dfdc-154">KB 4013633 ist ein X++-Aktualisierungs- oder -Metadatenhotfix, der den mobilen Arbeitsbereich <strong>Kostensteuerung</strong> enthält.</span><span class="sxs-lookup"><span data-stu-id="4dfdc-154">KB 4013633 is an X++ update or metadata hotfix that contains the <strong>Cost controlling</strong> mobile workspace.</span></span> <span data-ttu-id="4dfdc-155">Um KB 4013633 muss Ihr Systemadministrator folgende Schritte ausführen.</span><span class="sxs-lookup"><span data-stu-id="4dfdc-155">To implement KB 4013633, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="4dfdc-156"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Den Metadatenhotfix von Microsoft Dynamics Lifecycle Services (LCS) herunterladen</a>.</span><span class="sxs-lookup"><span data-stu-id="4dfdc-156"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="4dfdc-157"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Installieren Sie den Metadatenhotfix</a>.</span><span class="sxs-lookup"><span data-stu-id="4dfdc-157"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="4dfdc-158"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Erstellen eines zur Bereitstellung geeigneten Paket</a>, das das <strong>SCMMobile</strong> Modell enthält und laden Sie dann das zur Bereitstellung geeignete Paket in LCS hoch.</span><span class="sxs-lookup"><span data-stu-id="4dfdc-158"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Create a deployable package</a> that contains the <strong>SCMMobile</strong> model, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="4dfdc-159"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Das bereitstellbare Paket übernehmen</a>.</span><span class="sxs-lookup"><span data-stu-id="4dfdc-159"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Apply the deployable package</a>.</span></span></li>

</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4dfdc-160">Den mobilen Arbeitsbereich <strong>Kostensteuerung</strong> veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="4dfdc-160">Publish the <strong>Cost controlling</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="4dfdc-161">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="4dfdc-161">System administrator</span></span></td>
<td><span data-ttu-id="4dfdc-162">Siehe <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Einen mobilen Arbeitsbereich veröffentlichen</a>.</span><span class="sxs-lookup"><span data-stu-id="4dfdc-162">See <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>


## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="4dfdc-163">Herunterladen und Installieren der mobilen App</span><span class="sxs-lookup"><span data-stu-id="4dfdc-163">Download and install the mobile app</span></span>
<span data-ttu-id="4dfdc-164">Herunterladen und Installieren der Finance and Operations mobilen App:</span><span class="sxs-lookup"><span data-stu-id="4dfdc-164">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="4dfdc-165">Für Android-Smartphones</span><span class="sxs-lookup"><span data-stu-id="4dfdc-165">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="4dfdc-166">Für iPhones</span><span class="sxs-lookup"><span data-stu-id="4dfdc-166">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="4dfdc-167">Bei der mobile App anmelden</span><span class="sxs-lookup"><span data-stu-id="4dfdc-167">Sign in to the mobile app</span></span>

1.  <span data-ttu-id="4dfdc-168">Starten Sie die App auf Ihrem mobilen Gerät.</span><span class="sxs-lookup"><span data-stu-id="4dfdc-168">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="4dfdc-169">Geben Sie die URL Dynamics 365 ein.</span><span class="sxs-lookup"><span data-stu-id="4dfdc-169">Enter your Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="4dfdc-170">Bei der erstmaligen Anwendung werden Sie nach Ihrem Benutzernamen und dem Kennwort gefragt.</span><span class="sxs-lookup"><span data-stu-id="4dfdc-170">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="4dfdc-171">Geben Sie Ihre Anmeldeinformationen ein.</span><span class="sxs-lookup"><span data-stu-id="4dfdc-171">Enter your credentials.</span></span>
4.  <span data-ttu-id="4dfdc-172">Nachdem Sie sich angemeldet haben, werden verfügbare Arbeitsbereiche für Ihr Unternehmen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4dfdc-172">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="4dfdc-173">Beachten Sie, dass Sie, wenn Ihr Systemadministrator einen neuen Arbeitsbereich später veröffentlicht, die Liste der mobilen Arbeitsbereiche aktualisieren müssen.</span><span class="sxs-lookup"><span data-stu-id="4dfdc-173">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="4dfdc-174">[![Zum Aktualisieren ziehen](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="4dfdc-174">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="view-the-performance-of-your-cost-center-by-using-the-cost-controlling-mobile-workspace"></a><span data-ttu-id="4dfdc-175">Hier können Sie die Leistungsfähigkeit der Kostenstellen sehen, indem Sie den mobilen Arbeitsbereich Kostensteuerung verwenden</span><span class="sxs-lookup"><span data-stu-id="4dfdc-175">View the performance of your cost center by using the Cost controlling mobile workspace</span></span>

1.  <span data-ttu-id="4dfdc-176">Wählen Sie auf Ihrem mobilen Gerät den Arbeitsbereich **Kostensteuerung**.</span><span class="sxs-lookup"><span data-stu-id="4dfdc-176">On your mobile device, select the **Cost controlling** workspace.</span></span>
2.  <span data-ttu-id="4dfdc-177">Wählen Sie **Kostenträgersteuerung**.</span><span class="sxs-lookup"><span data-stu-id="4dfdc-177">Select **Cost object controlling**.</span></span>
3.  <span data-ttu-id="4dfdc-178">Wählen Sie **Aktivitäten**.</span><span class="sxs-lookup"><span data-stu-id="4dfdc-178">Select **Actions**.</span></span>
4.  <span data-ttu-id="4dfdc-179">Klicken Sie auf **Konfiguration auswählen**, um das Layout der Kostensteuerung zu wählen.</span><span class="sxs-lookup"><span data-stu-id="4dfdc-179">Select **Select configuration** to select a cost controlling layout.</span></span>
5.  <span data-ttu-id="4dfdc-180">Wählen Sie **Fertig**.</span><span class="sxs-lookup"><span data-stu-id="4dfdc-180">Select **Done**.</span></span>
6.  <span data-ttu-id="4dfdc-181">Wählen Sie **Aktivitäten**.</span><span class="sxs-lookup"><span data-stu-id="4dfdc-181">Select **Actions**.</span></span>
7.  <span data-ttu-id="4dfdc-182">Klicken Sie auf **Kostenträger auswählen**, um die Kostenstelle auszuwählen, auf die Sie Zugriff haben.</span><span class="sxs-lookup"><span data-stu-id="4dfdc-182">Select **Select cost object** to select the cost centers that you've been granted access to.</span></span>
8.  <span data-ttu-id="4dfdc-183">Wählen Sie **Fertig**.</span><span class="sxs-lookup"><span data-stu-id="4dfdc-183">Select **Done**.</span></span>
9.  <span data-ttu-id="4dfdc-184">Hier können Sie die Leistung der Kostenstelle anzeigen.</span><span class="sxs-lookup"><span data-stu-id="4dfdc-184">View the overall performance of your cost center.</span></span>
10. <span data-ttu-id="4dfdc-185">Wählen Sie den Link aus **Details für aktuelle Periode**.</span><span class="sxs-lookup"><span data-stu-id="4dfdc-185">Select the **Details for current period** link.</span></span>
11. <span data-ttu-id="4dfdc-186">Hier können Sie die Leistung der einzelnen Kostenelemente anzeigen</span><span class="sxs-lookup"><span data-stu-id="4dfdc-186">View the performance of individual cost elements.</span></span>
12. <span data-ttu-id="4dfdc-187">Sie können auch nach bestimmten Kostenfaktoren suchen.</span><span class="sxs-lookup"><span data-stu-id="4dfdc-187">You can also search for specific cost elements.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]