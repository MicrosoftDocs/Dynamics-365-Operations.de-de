---
title: Mobiler Arbeitsbereich für Bestellungsgenehmigung
description: Dieses Thema enthält Informationen zum mobilen Arbeitsbereich für Bestellungsgenehmigungen, mit dem Sie Bestellungen anzeigen und auf sie durch Aktionen antworten können. Sie können beispielsweise eine Bestellung genehmigen oder ablehnen.
author: mkirknel
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchVendorPortalRequests
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 30211
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b7f5d61ade071e75d53d5036a47fea438d8afbe6
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249424"
---
# <a name="purchase-order-approval-mobile-workspace"></a><span data-ttu-id="c9e7e-104">Mobiler Arbeitsbereich für Bestellungsgenehmigung</span><span class="sxs-lookup"><span data-stu-id="c9e7e-104">Purchase order approval mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

<span data-ttu-id="c9e7e-105">Dieses Thema enthält Informationen zur **Bestellungsgenehmigung** im mobilen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-105">This topic provides information about the **Purchase order approval** mobile workspace.</span></span> <span data-ttu-id="c9e7e-106">In diesem Arbeitsbereich können Sie Bestellungen anzeigen und auf sie antworten.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-106">This workspace lets you view purchase orders and respond to them through actions.</span></span> <span data-ttu-id="c9e7e-107">Sie können beispielsweise eine Bestellung genehmigen oder ablehnen.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-107">For example, you can approve or reject a purchase order.</span></span>
 
## <a name="overview"></a><span data-ttu-id="c9e7e-108">Überblick</span><span class="sxs-lookup"><span data-stu-id="c9e7e-108">Overview</span></span> 
<span data-ttu-id="c9e7e-109">Bestellungen, die Genehmigungen erfordern, durchlaufen einen Genehmigungsworkflow.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-109">Purchase orders that requires approval go through an approval workflow.</span></span> <span data-ttu-id="c9e7e-110">Der Workflow kann unterschiedliche Schritte umfassen, die erfordern, dass mindestens eine Person eine Maßnahme ergreift.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-110">The workflow can include various steps that require that one or more people take action.</span></span> <span data-ttu-id="c9e7e-111">Beispielsweise kann eine Person eine Aufgabe abschließen oder die Bestellung genehmigen.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-111">For example, a person might have to complete a task or approve the purchase order.</span></span> 

<span data-ttu-id="c9e7e-112">Im Arbeitsbereich **mobile Bestellungsgenehmigung** können Sie Bestellungen vom mobilen Gerät anzeigen und beantworten.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-112">The **Purchase order approval** mobile workspace lets you easily view and respond to purchase orders from your mobile device.</span></span> <span data-ttu-id="c9e7e-113">Im Arbeitsbereich können Sie die gleichen Workflowaktivitäten tätigen, die Sie vom Webclient aus tätigen können.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-113">This workspace also lets you take the same workflow actions that you can take from the web client.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c9e7e-114">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="c9e7e-114">Prerequisites</span></span>
<span data-ttu-id="c9e7e-115">Die Voraussetzungen unterscheiden sich basierend auf der Version von Supply Chain Management, die für Ihre Organisation bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-115">The prerequisites vary, depending on the version of Supply Chain Management that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-supply-chain-management"></a><span data-ttu-id="c9e7e-116">Voraussetzungen, wenn Sie verwenden Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="c9e7e-116">Prerequisites if you use Supply Chain Management</span></span> 
<span data-ttu-id="c9e7e-117">Wenn Finance and Operations für Ihre Organisation bereitgestellt wurde, muss der Systemadministrator den mobilen **Arbeitsbereich Bestellungsgenehmigung** veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-117">If Finance and Operations has been deployed for your organization, the system administrator must publish the **Purchase order approval** mobile workspace.</span></span> <span data-ttu-id="c9e7e-118">Anweisungen finden Sie unter [Einen mobilen Arbeitsbereich veröffentlichen](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="c9e7e-118">For instructions, see [Publish a mobile workspace](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="c9e7e-119">Voraussetzungen, wenn Sie Microsoft Dynamics 365 for Operations Version 1611 mit Plattformupdate 3 oder höher verwenden</span><span class="sxs-lookup"><span data-stu-id="c9e7e-119">Prerequisites if you use Microsoft Dynamics 365 for Operations version 1611 with Platform update 3 or later</span></span>
<span data-ttu-id="c9e7e-120">Wenn Microsoft Dynamics 365 for Operations Version 1611 mit Plattformupdate 3 oder höher für Ihre Organisation bereitgestellt wurde, muss der Systemadministrator die folgenden Voraussetzungen erfüllen.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-120">If Microsoft Dynamics 365 for Operations version 1611 with Platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span> 

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c9e7e-121">Voraussetzung</span><span class="sxs-lookup"><span data-stu-id="c9e7e-121">Prerequisite</span></span></th>
<th><span data-ttu-id="c9e7e-122">Rolle</span><span class="sxs-lookup"><span data-stu-id="c9e7e-122">Role</span></span></th>
<th><span data-ttu-id="c9e7e-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c9e7e-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c9e7e-124">Implementieren Sie KB 4017918.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-124">Implement KB 4017918.</span></span></td>
<td><span data-ttu-id="c9e7e-125">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="c9e7e-125">System administrator</span></span></td>
<td><span data-ttu-id="c9e7e-126">4017918 KB ist ein X++-Aktualisierungs- oder -Metadatenhotfix, der den mobilen Arbeitsbereich <strong>Bestellungsgenehmigung</strong> enthält.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-126">KB 4017918 is an X++ update or metadata hotfix that contains the <strong>Purchase order approval</strong> mobile workspace.</span></span> <span data-ttu-id="c9e7e-127">Um KB 4017918 muss Ihr Systemadministrator folgende Schritte ausführen.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-127">To implement KB 4017918, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="c9e7e-128"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Den Metadatenhotfix von Microsoft Dynamics Lifecycle Services (LCS) herunterladen</a>.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-128"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="c9e7e-129"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Installieren Sie den Metadatenhotfix</a>.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-129"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="c9e7e-130"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Erstellen eines zur Bereitstellung geeigneten Paket</a>, das das <strong>SCMMobile</strong> Modell enthält und laden Sie dann das zur Bereitstellung geeignete Paket in LCS hoch.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-130"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Create a deployable package</a> that contains the <strong>SCMMobile</strong> model, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="c9e7e-131"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Das bereitstellbare Paket übernehmen</a>.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-131"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Apply the deployable package</a>.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9e7e-132">Mobiler Arbeitsbereich für <strong>Bestellungsgenehmigung</strong> veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-132">Publish the <strong>Purchase order approval</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="c9e7e-133">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="c9e7e-133">System administrator</span></span></td>
<td><span data-ttu-id="c9e7e-134">Siehe <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Einen mobilen Arbeitsbereich veröffentlichen</a>.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-134">See <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="c9e7e-135">Herunterladen und Installieren der mobilen App</span><span class="sxs-lookup"><span data-stu-id="c9e7e-135">Download and install the mobile app</span></span>
<span data-ttu-id="c9e7e-136">Laden Sie die mobile Finance and Operations-App herunter und installieren Sie diese:</span><span class="sxs-lookup"><span data-stu-id="c9e7e-136">Download and install the Finance and Operations mobile app:</span></span>

- [<span data-ttu-id="c9e7e-137">Für Android-Smartphones</span><span class="sxs-lookup"><span data-stu-id="c9e7e-137">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
- [<span data-ttu-id="c9e7e-138">Für iPhones</span><span class="sxs-lookup"><span data-stu-id="c9e7e-138">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)


## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="c9e7e-139">Bei der mobile App anmelden</span><span class="sxs-lookup"><span data-stu-id="c9e7e-139">Sign in to the mobile app</span></span>

1. <span data-ttu-id="c9e7e-140">Starten Sie die App auf Ihrem mobilen Gerät.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-140">Start the app on your mobile device.</span></span>
2. <span data-ttu-id="c9e7e-141">Geben Sie die Microsoft Dynamics 365-URL ein.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-141">Enter your Microsoft Dynamics 365 URL.</span></span>
3. <span data-ttu-id="c9e7e-142">Bei der erstmaligen Anwendung werden Sie nach Ihrem Benutzernamen und dem Kennwort gefragt.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-142">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="c9e7e-143">Geben Sie Ihre Anmeldeinformationen ein.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-143">Enter your credentials.</span></span>
4. <span data-ttu-id="c9e7e-144">Nachdem Sie sich angemeldet haben, werden verfügbare Arbeitsbereiche für Ihr Unternehmen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-144">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="c9e7e-145">Beachten Sie, dass Sie, wenn Ihr Systemadministrator einen neuen Arbeitsbereich später veröffentlicht, die Liste der mobilen Arbeitsbereiche aktualisieren müssen.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-145">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

![Bestellungsgenehmigungsarbeitsbereich in der Liste verfügbarer Arbeitsbereiche](./media/po-workspaces.png)

## <a name="view-orders-that-are-assigned-to-you"></a><span data-ttu-id="c9e7e-147">Anzeigen der Ihnen zugewiesenen Aufträge</span><span class="sxs-lookup"><span data-stu-id="c9e7e-147">View orders that are assigned to you</span></span>
1. <span data-ttu-id="c9e7e-148">Wählen Sie auf Ihrem mobilen Gerät den Arbeitsbereich **Bestellungsgenehmigung**.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-148">On your mobile device, select the **Purchase order approval** workspace.</span></span>
2. <span data-ttu-id="c9e7e-149">Wählen Sie **Mir zugewiesene Aufträge**, um alle Bestellungen anzeigen, für die Sie angefordert wurden, im Bestellungsgenehmigungsworkflow aktiv zu werden.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-149">Select **Orders assigned to me** to view all the purchase orders for which you've been asked to take action in the purchase order approval workflow.</span></span>
3. <span data-ttu-id="c9e7e-150">Wählen Sie einen Auftrag aus.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-150">Select an order.</span></span> <span data-ttu-id="c9e7e-151">Auf der Seite **Auftragsdetails** finden Sie die Angaben im Auftragskopf und Positionen.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-151">On the **Order details** page, you will see the order header information and lines.</span></span> <span data-ttu-id="c9e7e-152">Sie sehen auch Richtlinien für die Workflowaufgabe.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-152">You can also find guidelines from the workflow task.</span></span>
4. <span data-ttu-id="c9e7e-153">Wählen Sie **Buchhaltungsverteilungen**, um die Seite **Kopfbuchhaltungsverteilungen** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-153">Select **Accounting distributions** to open the **Header accounting distributions** page.</span></span>
5. <span data-ttu-id="c9e7e-154">Hiermit kehren Sie zur Seite **Auftragsdetails** zurück, und wählen Sie eine Position aus.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-154">Return to the **Order details** page, and select a line.</span></span> <span data-ttu-id="c9e7e-155">Aus den Auftragspositionsdetails können Sie auch positionsspezfische Buchhaltungsverteilungen untersuchen.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-155">From the order line details, you can also explore the line-specific accounting distributions.</span></span>

## <a name="complete-an-action-on-the-purchase-order"></a><span data-ttu-id="c9e7e-156">Verbinden einer Aktivität auf der Bestellung</span><span class="sxs-lookup"><span data-stu-id="c9e7e-156">Complete an action on the purchase order</span></span>
<span data-ttu-id="c9e7e-157">Nachdem die Bestellung angezeigt wurde, die Ihnen zugewiesen wurde und Sie die Workflowanweisungen gelesen haben, sollten Sie bereit sein, die Ihnen zugewiesenen Aktivitäten auszuführen.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-157">After you've viewed the purchase order that is assigned to you and read the workflow instructions, you should be ready to take action.</span></span>

1. <span data-ttu-id="c9e7e-158">Wählen Sie auf Ihrem mobilen Gerät den Arbeitsbereich **Bestellungsgenehmigung**.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-158">On your mobile device, select the **Purchase order approval** workspace.</span></span>
2. <span data-ttu-id="c9e7e-159">Wählen Sie **Mir zugewiesene Aufträge**, um alle Bestellungen anzeigen, für die Sie angefordert wurden, im Bestellungsgenehmigungsworkflow aktiv zu werden.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-159">Select **Orders assigned to me** to view all the purchase orders for which you've been asked to take action in the purchase order approval workflow.</span></span>
3. <span data-ttu-id="c9e7e-160">Wählen Sie einen Auftrag aus, um die Details anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-160">Select an order, and view the details page.</span></span>
4. <span data-ttu-id="c9e7e-161">Wählen Sie **Aktivitäten** aus, um die verfügbaren Aktivitäten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-161">Select **Actions** to show the available actions.</span></span> <span data-ttu-id="c9e7e-162">Die Aktivitäten, die verfügbar sind, hängen von der Aufgabe ab, die Ihnen zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-162">The actions that are available depend on the task that has been assigned to you.</span></span>

    | <span data-ttu-id="c9e7e-163">Aufgabenaktivität</span><span class="sxs-lookup"><span data-stu-id="c9e7e-163">Task action</span></span>    | <span data-ttu-id="c9e7e-164">Genehmigungsaktivität</span><span class="sxs-lookup"><span data-stu-id="c9e7e-164">Approval action</span></span>  |
    |----------------|------------------|
    | <span data-ttu-id="c9e7e-165">Komplett</span><span class="sxs-lookup"><span data-stu-id="c9e7e-165">Complete</span></span>       | <span data-ttu-id="c9e7e-166">Genehmigen</span><span class="sxs-lookup"><span data-stu-id="c9e7e-166">Approve</span></span>          |
    | <span data-ttu-id="c9e7e-167">Zurück</span><span class="sxs-lookup"><span data-stu-id="c9e7e-167">Return</span></span>         | <span data-ttu-id="c9e7e-168">Ablehnen</span><span class="sxs-lookup"><span data-stu-id="c9e7e-168">Reject</span></span>           |
    | <span data-ttu-id="c9e7e-169">Änderung anfordern</span><span class="sxs-lookup"><span data-stu-id="c9e7e-169">Request change</span></span> | <span data-ttu-id="c9e7e-170">Änderung anfordern</span><span class="sxs-lookup"><span data-stu-id="c9e7e-170">Request change</span></span>   |
    | <span data-ttu-id="c9e7e-171">Delegat</span><span class="sxs-lookup"><span data-stu-id="c9e7e-171">Delegate</span></span>       | <span data-ttu-id="c9e7e-172">Delegat</span><span class="sxs-lookup"><span data-stu-id="c9e7e-172">Delegate</span></span>         |

5. <span data-ttu-id="c9e7e-173">Wählen Sie die entsprechende Aktivität aus.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-173">Select the appropriate action.</span></span>
6. <span data-ttu-id="c9e7e-174">Auf der Seite **Aufgabe beenden** geben Sie einen Kommentar ein.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-174">On the **Complete task** page, enter a comment.</span></span> <span data-ttu-id="c9e7e-175">Beachten Sie, dass, wenn Sie die Aktivität **Delegieren** auswählen, müssen Sie einen Benutzer auswählen, an die Aufgabe delegiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-175">Note that if you select the **Delegate** action, you must select a user to delegate the task to.</span></span>
7. <span data-ttu-id="c9e7e-176">Wählen Sie **Fertig**.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-176">Select **Done**.</span></span> <span data-ttu-id="c9e7e-177">Nachdem Sie den Arbeitsbereich aktualisiert haben, ist die Bestellung nicht mehr in der Liste.</span><span class="sxs-lookup"><span data-stu-id="c9e7e-177">After you refresh your workspace, the purchase order will no longer be in your list.</span></span> 
