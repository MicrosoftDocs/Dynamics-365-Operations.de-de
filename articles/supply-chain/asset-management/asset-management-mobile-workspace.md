---
title: Mobilen Arbeitsbereich für Anlagenverwaltung verwenden
description: Dieses Thema enthält Informationen zum mobilen Arbeitsbereich „Anlageverwaltung“.
author: johanhoffmann
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.dyn365.ops.version: 10.0.5
ms.search.validFrom: 2019-08-31
ms.openlocfilehash: 98f935a11ad8a5272cde0270f9ae0471411b914a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837944"
---
# <a name="use-the-asset-management-mobile-workspace"></a><span data-ttu-id="0d071-103">Mobilen Arbeitsbereich für Anlagenverwaltung verwenden</span><span class="sxs-lookup"><span data-stu-id="0d071-103">Use the Asset management mobile workspace</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0d071-104">Dieses Thema enthält Informationen zum mobilen Arbeitsbereich **Anlageverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="0d071-104">This topic provides information about the **Asset management** mobile workspace.</span></span> <span data-ttu-id="0d071-105">Mit dem Arbeitsbereich können Benutzer Wartungsanforderungen und Arbeitsaufträge anzeigen und erstellen.</span><span class="sxs-lookup"><span data-stu-id="0d071-105">This workspace lets users view and create maintenance requests and work orders.</span></span> <span data-ttu-id="0d071-106">Benutzer können auch die zugeordneten Arbeitsauftragseinzelvorgänge in einer Listenansicht anzeigen.</span><span class="sxs-lookup"><span data-stu-id="0d071-106">Users can also view the assigned work order jobs in a calendar or list view.</span></span> <span data-ttu-id="0d071-107">Anlagen und funktionale Standorte können auch angezeigt und gesucht werden.</span><span class="sxs-lookup"><span data-stu-id="0d071-107">Assets and functional locations can also be viewed and searched for.</span></span>

## <a name="overview"></a><span data-ttu-id="0d071-108">Übersicht</span><span class="sxs-lookup"><span data-stu-id="0d071-108">Overview</span></span>

<span data-ttu-id="0d071-109">Anlagenverwaltung ist ein erweitertes Modul für die Verwaltung von Anlagen und Arbeitsauftragseinzelvorgänge in Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="0d071-109">Asset Management is an advanced module for managing assets and work order jobs in Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="0d071-110">Der mobile Arbeitsbereich **Asset-Management** ermöglicht Benutzern, zugewiesene Arbeitsauftragseinzelvorgänge schnell im mobilen Gerät ihrer Wahl anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="0d071-110">The **Asset management** mobile workspace lets users quickly view assigned work order jobs on the mobile device of their choice.</span></span> <span data-ttu-id="0d071-111">Benutzer können auch Wartungsanfragen erstellen und verwalten, Lebenszyklusstatus aktualisieren, und Anlagen und funktionale Standortdetail mit ihrem mobilen Gerät anzeigen.</span><span class="sxs-lookup"><span data-stu-id="0d071-111">Users can also create and manage maintenance requests, update lifecycle state, and view asset and functional location details by using their mobile device.</span></span>

<span data-ttu-id="0d071-112">Insbesondere ermöglicht der mobile Arbeitsbereich für die **Anlagenverwaltung** den Benutzern, die folgenden Aufgaben auszuführen:</span><span class="sxs-lookup"><span data-stu-id="0d071-112">Specifically, the **Asset management** mobile workspace lets users perform these tasks:</span></span>

- <span data-ttu-id="0d071-113">Wartungsanfragen erstellen, anzeigen und bearbeiten, ein Foto machen oder ein vorhandenes Bild an die Wartungsanfrage anhängen, den Lebenszyklusstatus der Wartungsanfrage ändern</span><span class="sxs-lookup"><span data-stu-id="0d071-113">Create, view, and edit maintenance requests, take a photo or attach an existing image to the maintenance request, change the maintenance request lifecycle state.</span></span> 
- <span data-ttu-id="0d071-114">Arbeitsaufträge erstellen, anzeigen und bearbeiten, ein Foto machen oder ein vorhandenes Bild an den Wartungsauftrag anhängen, den Lebenszyklusstatus der Wartungsanfrage ändern, Wartungsauftragseinzelvorgänge anzeigen</span><span class="sxs-lookup"><span data-stu-id="0d071-114">Create, view, and edit work orders, take a photo or attach an existing image to the work order, change the work order lifecycle state, view work order jobs.</span></span>
- <span data-ttu-id="0d071-115">Zugewiesene Arbeitsauftrageinzelaufträge in einer Kalenderansicht anzeigen</span><span class="sxs-lookup"><span data-stu-id="0d071-115">View assigned work order jobs in a calendar view.</span></span>
- <span data-ttu-id="0d071-116">Arbeitsauftragseinzelvorgänge erstellen, anzeigen und bearbeiten, Anlagenzähler aktualisieren, Wartungsprüflisten anzeigen, Notizen zu Arbeitsauftrageinzelvorgängen anzeigen und bearbeiten, die erforderlichen Werkzeuge für den Arbeitsauftrageinzelvorgang anzeigen.</span><span class="sxs-lookup"><span data-stu-id="0d071-116">Create, view, and edit work order job, update asset counters, view maintenance checklist, view and edit work order job notes, view the tools required for the work order job.</span></span>
- <span data-ttu-id="0d071-117">Bestimmte Anlagen oder funktionale Standorte anzeigen oder suchen</span><span class="sxs-lookup"><span data-stu-id="0d071-117">View or search for a specific asset or functional location.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0d071-118">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="0d071-118">Prerequisites</span></span>

<span data-ttu-id="0d071-119">Bevor Sie den mobilen Arbeitsbereich **Anlagenverwaltung** verwenden können, muss Ihr Administrator die erforderlichen Benutzer- und Arbeiterkonten einrichten und den Arbeitsbereich veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="0d071-119">Before you can use the **Asset management** mobile workspace, your admin must set up the required user and worker accounts, and publish the workspace.</span></span> <span data-ttu-id="0d071-120">Weitere Informationen finden Sie unter [Einrichten des mobilen Arbeitsbereichs zur Anlagenverwaltung](set-up-asset-management-mobile.md).</span><span class="sxs-lookup"><span data-stu-id="0d071-120">For more information, see [Set up the Asset management mobile workspace](set-up-asset-management-mobile.md).</span></span>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="0d071-121">Herunterladen und Installieren der mobilen App</span><span class="sxs-lookup"><span data-stu-id="0d071-121">Download and install the mobile app</span></span>

<span data-ttu-id="0d071-122">Laden Sie die mobile App für Dynamics 365 for Unified Operations herunter und installieren Sie diese:</span><span class="sxs-lookup"><span data-stu-id="0d071-122">Download and install the Dynamics 365 for Unified Operations mobile app:</span></span>

- [<span data-ttu-id="0d071-123">Für Android-Smartphones</span><span class="sxs-lookup"><span data-stu-id="0d071-123">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
- [<span data-ttu-id="0d071-124">Für iPhones</span><span class="sxs-lookup"><span data-stu-id="0d071-124">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="0d071-125">Bei der mobile App anmelden</span><span class="sxs-lookup"><span data-stu-id="0d071-125">Sign in to the mobile app</span></span>

1. <span data-ttu-id="0d071-126">Starten Sie die App auf Ihrem mobilen Gerät.</span><span class="sxs-lookup"><span data-stu-id="0d071-126">Start the app on your mobile device.</span></span>

1. <span data-ttu-id="0d071-127">Geben Sie die URL Dynamics 365 ein.</span><span class="sxs-lookup"><span data-stu-id="0d071-127">Enter your Dynamics 365 URL.</span></span>

1. <span data-ttu-id="0d071-128">Bei der erstmaligen Anwendung werden Sie nach Ihrem Benutzernamen und dem Kennwort gefragt.</span><span class="sxs-lookup"><span data-stu-id="0d071-128">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="0d071-129">Geben Sie Ihre Anmeldeinformationen ein.</span><span class="sxs-lookup"><span data-stu-id="0d071-129">Enter your credentials.</span></span>

1. <span data-ttu-id="0d071-130">Nachdem Sie sich angemeldet haben, werden verfügbare Arbeitsbereiche für Ihr Unternehmen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0d071-130">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="0d071-131">Beachten Sie, dass Sie, wenn Ihr Systemadministrator einen neuen Arbeitsbereich später veröffentlicht, die Liste der mobilen Arbeitsbereiche aktualisieren müssen.</span><span class="sxs-lookup"><span data-stu-id="0d071-131">Note that if your system administrator publishes a new workspace later, you'll have to refresh the list of mobile workspaces.</span></span>

    <span data-ttu-id="0d071-132">![Arbeitsbereich auswählen](media/am-mobile-01.png "Arbeitsbereich auswählen")</span><span class="sxs-lookup"><span data-stu-id="0d071-132">![Select a workspace](media/am-mobile-01.png "Select a workspace")</span></span>

## <a name="view-assigned-work-order-jobs-in-calendar-view"></a><span data-ttu-id="0d071-133">Zugewiesene Arbeitsauftrageinzelaufträge in Kalenderansicht anzeigen</span><span class="sxs-lookup"><span data-stu-id="0d071-133">View assigned work order jobs in calendar view</span></span>

1. <span data-ttu-id="0d071-134">Öffnen Sie auf Ihrem mobilen Gerät den Arbeitsbereich für die **Anlagenverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="0d071-134">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="0d071-135">Wählen Sie **Mein Arbeitsauftragseinzelvorgangskalender** aus.</span><span class="sxs-lookup"><span data-stu-id="0d071-135">Select **My work order jobs calendar**.</span></span>

1. <span data-ttu-id="0d071-136">Wählen Sie das Datum aus, für das Sie archivierte Arbeitsauftrageinzelvorgänge anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="0d071-136">Select the date you want to view work order jobs for.</span></span> <span data-ttu-id="0d071-137">In der Liste finden Sie die Anlagenkennung und die Kennung des funktionalen Standorts für jeden Arbeitsauftragseinzelvorgang.</span><span class="sxs-lookup"><span data-stu-id="0d071-137">In the list, you'll see the asset ID and functional location ID for each work order job.</span></span>

1. <span data-ttu-id="0d071-138">Wählen Sie einen Arbeitsauftragseinzelvorgang in der Liste aus, um Detail zum Einzelvorgang anzuzeigen: Details zu Anlage und funktionalem Standort sowie andere Navigationslinks, um **Anhänge**, **Prüflisten**, **Tools**, **Anlagenzähler**, **Notizen**, **Erfassungen** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="0d071-138">Select a work order job in the list to see job details: Asset and functional location details as well as other navigation links to view **Attachments**, **Checklists**, **Tools**, **Asset counters**, **Notes**, **Journals**.</span></span>

    <span data-ttu-id="0d071-139">![Zugewiesene Arbeitsauftrageinzelaufträge in Kalenderansicht anzeigen](media/am-mobile-02.png "Zugewiesene Arbeitsauftrageinzelaufträge in Kalenderansicht anzeigen")</span><span class="sxs-lookup"><span data-stu-id="0d071-139">![View assigned work order jobs in calendar view](media/am-mobile-02.png "View assigned work order jobs in calendar view")</span></span>

## <a name="create-a-work-order-job"></a><span data-ttu-id="0d071-140">Arbeitsauftrageinzelvorgang erstellen</span><span class="sxs-lookup"><span data-stu-id="0d071-140">Create a work order job</span></span>

1. <span data-ttu-id="0d071-141">Öffnen Sie auf Ihrem mobilen Gerät den Arbeitsbereich für die **Anlagenverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="0d071-141">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="0d071-142">Wählen Sie **Alle Wartungsarbeitsaufträge** aus.</span><span class="sxs-lookup"><span data-stu-id="0d071-142">Select **All maintenance work orders**.</span></span>

1. <span data-ttu-id="0d071-143">Wählen Sie den Arbeitsauftrag aus, für den Sie einen neuen Arbeitsauftragseinzelvorgang erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="0d071-143">Select the work order you want to create a new work order job for.</span></span>

1. <span data-ttu-id="0d071-144">Wählen Sie die Schaltfläche **Position hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="0d071-144">Select the **Add line** button.</span></span>

1. <span data-ttu-id="0d071-145">Wählen Sie die **Anlage** aus, für die Sie einen Arbeitsauftragseinzelvorgang erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="0d071-145">Select the **Asset** you want to create a work order job for.</span></span>

1. <span data-ttu-id="0d071-146">Wählen Sie **Wartungsauftragstyp**, **Wartungsauftragsartenvariante** und **Art** aus.</span><span class="sxs-lookup"><span data-stu-id="0d071-146">Select **Maintenance job type**, **Maintenance job type variant** and **Trade**.</span></span>

1. <span data-ttu-id="0d071-147">Wählen Sie **Fertig**.</span><span class="sxs-lookup"><span data-stu-id="0d071-147">Select **Done**.</span></span>

    <span data-ttu-id="0d071-148">![Der Bildschirm „Position hinzufügen“](media/am-mobile-03.png "Der Bildschirm „Position hinzufügen“")</span><span class="sxs-lookup"><span data-stu-id="0d071-148">![The Add line screen](media/am-mobile-03.png "The Add line screen")</span></span>


## <a name="add-attachment-to-a-work-order-job"></a><span data-ttu-id="0d071-149">Einem Arbeitsauftragseinzelvorgang einen Anhang hinzufügen</span><span class="sxs-lookup"><span data-stu-id="0d071-149">Add attachment to a work order job</span></span>

1. <span data-ttu-id="0d071-150">Öffnen Sie auf Ihrem mobilen Gerät den Arbeitsbereich für die **Anlagenverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="0d071-150">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="0d071-151">Wählen Sie **Alle Wartungsarbeitsaufträge** aus.</span><span class="sxs-lookup"><span data-stu-id="0d071-151">Select **All maintenance work orders**.</span></span>

1. <span data-ttu-id="0d071-152">Wählen Sie den Arbeitsauftrag > Arbeitsauftragseinzelvorgang aus, dem Sie einen Anhang hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="0d071-152">Select the work order > work order job you want to add an attachment to.</span></span>
    - <span data-ttu-id="0d071-153">Alternativ können Sie auch **Mein Arbeitsauftragseinzelvorgangskalender** oder **Eigene Arbeitsauftragseinzelvorgangsliste** auf der Startseite auswählen, um zur Seite **Arbeitsauftragseinzelvorgangsdetails** zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="0d071-153">Alternatively, you can also select **My work order jobs calendar** or **My work order jobs list** on the home page to navigate to the **Work order job details** page.</span></span>

1. <span data-ttu-id="0d071-154">Wählen Sie **Anhänge** auf der Seite **Arbeitsauftragseinzelvorgangsdetails** aus.</span><span class="sxs-lookup"><span data-stu-id="0d071-154">Select **Attachments** on the **Work order job details** page.</span></span>

1. <span data-ttu-id="0d071-155">Sie finden vorhandene Anhänge im Arbeitsauftragseinzelvorgang.</span><span class="sxs-lookup"><span data-stu-id="0d071-155">You'll see existing attachments on the work order job.</span></span> <span data-ttu-id="0d071-156">Wählen Sie **Anhang hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="0d071-156">Select **Add attachment**.</span></span>

1. <span data-ttu-id="0d071-157">Geben Sie **Name** und **Notizen** für dien Anhang ein.</span><span class="sxs-lookup"><span data-stu-id="0d071-157">Enter **Name** and **Notes** for the attachment.</span></span>

1. <span data-ttu-id="0d071-158">Wählen Sie **Bild auswählen** aus, um ein Foto aus der mobilen Galerie auszuwählen, oder **Foto aufnehmen**, um ein Foto zu machen.</span><span class="sxs-lookup"><span data-stu-id="0d071-158">Select **Choose image** to select a photo from the mobile gallery, or **Take photo** to take a photo.</span></span>

1. <span data-ttu-id="0d071-159">Wählen Sie **Fertig**.</span><span class="sxs-lookup"><span data-stu-id="0d071-159">Select **Done**.</span></span>

    <span data-ttu-id="0d071-160">![Anzeigen und Hinzufügen von Anhängen für einen Arbeitsauftrageinzelvorgang](media/am-mobile-04.png "Anzeigen und Hinzufügen von Anhängen für einen Arbeitsauftrageinzelvorgang")</span><span class="sxs-lookup"><span data-stu-id="0d071-160">![View and add attachments for a work order job](media/am-mobile-04.png "View and add attachments for a work order job")</span></span>

## <a name="view-maintenance-checklist-on-a-work-order-job"></a><span data-ttu-id="0d071-161">Wartungsprüfliste zu einem Arbeitsauftragseinzelvorgang anzeigen</span><span class="sxs-lookup"><span data-stu-id="0d071-161">View maintenance checklist on a work order job</span></span>

1. <span data-ttu-id="0d071-162">Öffnen Sie auf Ihrem mobilen Gerät den Arbeitsbereich für die **Anlagenverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="0d071-162">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="0d071-163">Wählen Sie **Alle Wartungsarbeitsaufträge** aus.</span><span class="sxs-lookup"><span data-stu-id="0d071-163">Select **All maintenance work orders**.</span></span>

1. <span data-ttu-id="0d071-164">Wählen Sie den Arbeitsauftrag > Arbeitsauftragseinzelvorgang aus, für den Sie Prüflisten anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="0d071-164">Select the work order > work order job you want to view checklists for.</span></span>
    - <span data-ttu-id="0d071-165">Alternativ können Sie auch **Mein Arbeitsauftragseinzelvorgangskalender** oder **Eigene Arbeitsauftragseinzelvorgangsliste** auf der Startseite auswählen, um zur Seite **Arbeitsauftragseinzelvorgangsdetails** zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="0d071-165">Alternatively, you can also select **My work order jobs calendar** or **My work order jobs list** on the home page to navigate to the **work order job details** page.</span></span>

1. <span data-ttu-id="0d071-166">Wählen Sie **Prüflisten** auf der Seite **Arbeitsauftragseinzelvorgangsdetails** aus.</span><span class="sxs-lookup"><span data-stu-id="0d071-166">Select **Checklists** on the **Work order job details** page.</span></span>

1. <span data-ttu-id="0d071-167">Es wird eine Liste der Prüflistenpositionen angezeigt, die dem Arbeitsauftragseinzelvorgang zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="0d071-167">You'll see a list of checklist lines related to the work order job.</span></span> <span data-ttu-id="0d071-168">Wählen Sie eine Prüflistenposition aus, um **Anweisungen** anzuzeigen und **Notizen** hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="0d071-168">Select a checklist line to view **Instructions** and add **Notes**.</span></span>

1. <span data-ttu-id="0d071-169">Klicken Sie auf die Zurück-Schaltfläche (**<**), um zur vorherigen Seite zurückzugelangen.</span><span class="sxs-lookup"><span data-stu-id="0d071-169">Select the back button (**<**) to return to the previous page.</span></span>

    <span data-ttu-id="0d071-170">![Wartungsprüfliste und Positionsdetails](media/am-mobile-05.png "Wartungsprüfliste und Positionsdetails")</span><span class="sxs-lookup"><span data-stu-id="0d071-170">![Maintenance checklist and line details](media/am-mobile-05.png "Maintenance checklist and line details")</span></span>

## <a name="view-and-update-asset-counters-on-a-work-order-job"></a><span data-ttu-id="0d071-171">nlagenzähler zu einem Arbeitsauftragseinzelvorgang anzeigen und aktualisieren</span><span class="sxs-lookup"><span data-stu-id="0d071-171">View and update asset counters on a work order job</span></span>

1. <span data-ttu-id="0d071-172">Öffnen Sie auf Ihrem mobilen Gerät den Arbeitsbereich für die **Anlagenverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="0d071-172">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="0d071-173">Wählen Sie **Alle Wartungsarbeitsaufträge** aus.</span><span class="sxs-lookup"><span data-stu-id="0d071-173">Select **All maintenance work orders**.</span></span>

1. <span data-ttu-id="0d071-174">Wählen Sie den Arbeitsauftrag > Arbeitsauftragseinzelvorgang aus, für den Sie Anlagenzähler anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="0d071-174">Select the work order > work order job you want to view asset counters for.</span></span>
    - <span data-ttu-id="0d071-175">Alternativ können Sie auch **Mein Arbeitsauftragseinzelvorgangskalender** oder **Eigene Arbeitsauftragseinzelvorgangsliste** auf der Startseite auswählen, um zur Seite **Arbeitsauftragseinzelvorgangsdetails** zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="0d071-175">Alternatively, you can also select **My work order jobs calendar** or **My work order jobs list** on the home page to navigate to the **work order job details** page.</span></span>

1. <span data-ttu-id="0d071-176">Wählen Sie **Anlagenzähler** auf der Seite **Arbeitsauftragseinzelvorgangsdetails** aus.</span><span class="sxs-lookup"><span data-stu-id="0d071-176">Select **Asset counters** on the **Work order job details** page.</span></span>

1. <span data-ttu-id="0d071-177">Es wird eine Liste der Anlagenzähler angezeigt, die dem Arbeitsauftragseinzelvorgang zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="0d071-177">You see a list of asset counters related to the work order job.</span></span> <span data-ttu-id="0d071-178">Wählen Sie das Bleistiftsymbol in einer Anlagenzählerposition aus, um den Gegenwert zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="0d071-178">Select the pencil icon on an asset counter line to update the counter value.</span></span>

1. <span data-ttu-id="0d071-179">Geben Sie einen neuen Gegenwert ein, und wählen Sie **Fertig** aus.</span><span class="sxs-lookup"><span data-stu-id="0d071-179">Enter a new counter value, and select **Done**.</span></span>

    <span data-ttu-id="0d071-180">![Anlagenzähler anzeigen und aktualisieren](media/am-mobile-06.png "Anlagenzähler anzeigen und aktualisieren")</span><span class="sxs-lookup"><span data-stu-id="0d071-180">![View and update asset counters](media/am-mobile-06.png "View and update asset counters")</span></span>

## <a name="register-consumption-on-a-work-order-job"></a><span data-ttu-id="0d071-181">Verbrauch in einem Arbeitsauftragseinzelvorgang erfassen</span><span class="sxs-lookup"><span data-stu-id="0d071-181">Register consumption on a work order job</span></span>

1. <span data-ttu-id="0d071-182">Öffnen Sie auf Ihrem mobilen Gerät den Arbeitsbereich für die **Anlagenverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="0d071-182">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="0d071-183">Wählen Sie **Alle Wartungsarbeitsaufträge** aus.</span><span class="sxs-lookup"><span data-stu-id="0d071-183">Select **All maintenance work orders**.</span></span>

1. <span data-ttu-id="0d071-184">Wählen Sie den Arbeitsauftrag > Arbeitsauftragseinzelvorgang aus, für den Sie Verbrauchserfassungen hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="0d071-184">Select the work order > work order job you want to add consumption registrations for.</span></span>
    - <span data-ttu-id="0d071-185">Alternativ können Sie auch **Mein Arbeitsauftragseinzelvorgangskalender** oder **Eigene Arbeitsauftragseinzelvorgangsliste** auf der Startseite auswählen, um zur Seite **Arbeitsauftragseinzelvorgangsdetails** zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="0d071-185">Alternatively, you can also select **My work order jobs calendar** or **My work order jobs list** on the home page to navigate to the **work order job details** page.</span></span>

1. <span data-ttu-id="0d071-186">Wählen Sie **Erfassungen** auf der Seite **Arbeitsauftragseinzelvorgangsdetails** aus.</span><span class="sxs-lookup"><span data-stu-id="0d071-186">Select **Journals** on the **Work order job details** page.</span></span>

1. <span data-ttu-id="0d071-187">Wählen Sie **Stunden hinzufügen** aus, um Arbeitsstundenerfassungen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0d071-187">Select **Add hours** to create work hour registrations.</span></span>
    1. <span data-ttu-id="0d071-188">Wählen Sie aus der Suche die **Kategorie** aus.</span><span class="sxs-lookup"><span data-stu-id="0d071-188">Select the **Category** from the lookup.</span></span>
    1. <span data-ttu-id="0d071-189">Geben Sie im Feld **Stunden** die Anzahl der Arbeitsstunden ein, die für den Arbeitsauftragseinzelvorgang aufgewendet wurden.</span><span class="sxs-lookup"><span data-stu-id="0d071-189">In the **Hours** field, enter the number of work hours spent on the work order job.</span></span>
    1. <span data-ttu-id="0d071-190">Wählen Sie die geeignete **Positionseigenschaft** aus.</span><span class="sxs-lookup"><span data-stu-id="0d071-190">Select the appropriate **Line property**.</span></span>
    1. <span data-ttu-id="0d071-191">Wählen Sie **Fertig**.</span><span class="sxs-lookup"><span data-stu-id="0d071-191">Select **Done**.</span></span>

1. <span data-ttu-id="0d071-192">Wählen Sie **Artikel hinzufügen** aus, um Artikelerfassungen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0d071-192">Select **Add items** to create item registrations.</span></span>
    1. <span data-ttu-id="0d071-193">Wählen Sie die **Artikelnummer** aus der Suche aus.</span><span class="sxs-lookup"><span data-stu-id="0d071-193">Select the **Item number** from the lookup.</span></span>
    1. <span data-ttu-id="0d071-194">Wählen Sie den **Standort** aus der Suche aus.</span><span class="sxs-lookup"><span data-stu-id="0d071-194">Select the **Site** from the lookup.</span></span>
    1. <span data-ttu-id="0d071-195">Geben Sie die **Menge** der verbrauchten Artikel an.</span><span class="sxs-lookup"><span data-stu-id="0d071-195">Enter the **Quantity** of items consumed.</span></span>
    1. <span data-ttu-id="0d071-196">Wählen Sie **Fertig**.</span><span class="sxs-lookup"><span data-stu-id="0d071-196">Select **Done**.</span></span>

1. <span data-ttu-id="0d071-197">Wählen Sie **Ausgaben hinzufügen** aus, um Ausgabenerfassungen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0d071-197">Select **Add expense** to create expense registrations.</span></span>
    1. <span data-ttu-id="0d071-198">Wählen Sie aus der Suche die **Kategorie** aus.</span><span class="sxs-lookup"><span data-stu-id="0d071-198">Select the **Category** from the lookup.</span></span>
    1. <span data-ttu-id="0d071-199">Geben Sie die Menge für die Ausgabenerfassung ein.</span><span class="sxs-lookup"><span data-stu-id="0d071-199">Enter the quantity for the expense registration.</span></span>
    1. <span data-ttu-id="0d071-200">Wählen Sie **Verkaufswährung** aus der Suche aus.</span><span class="sxs-lookup"><span data-stu-id="0d071-200">Select the **Sales currency** from the lookup.</span></span>
    1. <span data-ttu-id="0d071-201">Geben Sie den **Einstandspreis** für die Ausgabenerfassung ein.</span><span class="sxs-lookup"><span data-stu-id="0d071-201">Enter the **Cost price** for the expense registration.</span></span>
    1. <span data-ttu-id="0d071-202">Wählen Sie **Fertig**.</span><span class="sxs-lookup"><span data-stu-id="0d071-202">Select **Done**.</span></span>

    <span data-ttu-id="0d071-203">![Arbeitsauftragserfassung aktualisieren](media/am-mobile-07.png "Arbeitsauftragserfassung aktualisieren")</span><span class="sxs-lookup"><span data-stu-id="0d071-203">![Update a work order journal](media/am-mobile-07.png "Update a work order journal")</span></span>

## <a name="update-lifecycle-state-on-a-work-order"></a><span data-ttu-id="0d071-204">Lebenszyklusstatus eines Arbeitsauftrags aktualisieren</span><span class="sxs-lookup"><span data-stu-id="0d071-204">Update lifecycle state on a work order</span></span>

1. <span data-ttu-id="0d071-205">Öffnen Sie auf Ihrem mobilen Gerät den Arbeitsbereich für die **Anlagenverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="0d071-205">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="0d071-206">Wählen Sie **Alle Wartungsarbeitsaufträge** aus.</span><span class="sxs-lookup"><span data-stu-id="0d071-206">Select **All maintenance work orders**.</span></span>

1. <span data-ttu-id="0d071-207">Wählen Sie den Arbeitsauftrag aus, für den Sie den Lebenszyklusstatus aktualisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="0d071-207">Select the work order you want to update lifecycle state for.</span></span>

1. <span data-ttu-id="0d071-208">Wählen Sie die Schaltfläche **Status aktualisieren** am unteren Bildschirmrand aus.</span><span class="sxs-lookup"><span data-stu-id="0d071-208">Select the **Update state** button at the bottom of the screen.</span></span>

1. <span data-ttu-id="0d071-209">Wählen Sie einen neuen Lebenszyklusstatus aus der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="0d071-209">Select a new lifecycle state from the list.</span></span>

1. <span data-ttu-id="0d071-210">Wählen Sie **Fertig**.</span><span class="sxs-lookup"><span data-stu-id="0d071-210">Select **Done**.</span></span>

    <span data-ttu-id="0d071-211">![Lebenszyklusstatus eines Arbeitsauftrags aktualisieren](media/am-mobile-08.png "Lebenszyklusstatus eines Arbeitsauftrags aktualisieren")</span><span class="sxs-lookup"><span data-stu-id="0d071-211">![Update lifecycle state on a work order](media/am-mobile-08.png "Update lifecycle state on a work order")</span></span>

## <a name="create-a-maintenance-request"></a><span data-ttu-id="0d071-212">Eine Wartungsanfrage erstellen</span><span class="sxs-lookup"><span data-stu-id="0d071-212">Create a maintenance request</span></span>

1. <span data-ttu-id="0d071-213">Öffnen Sie auf Ihrem mobilen Gerät den Arbeitsbereich für die **Anlagenverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="0d071-213">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="0d071-214">Wählen Sie **Alle Wartungsanfragen** aus.</span><span class="sxs-lookup"><span data-stu-id="0d071-214">Select **All maintenance requests**.</span></span>

1. <span data-ttu-id="0d071-215">Wählen Sie am unteren Bildschirmrand **Aktivitäten** und dann **Wartungsanfrage erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="0d071-215">Select **Actions** at the bottom of the screen, and select **Create maintenance request**.</span></span>

1. <span data-ttu-id="0d071-216">Wenn für Wartungsanfragen in **Anlagenverwaltung** Nummernkreis aktiviert ist, wird das Feld **Wartungsanfrage** ausgeblendet, da es automatisch aufgefüllt wird. Wenn das Feld **Wartungsanfrage** angezeigt wird, geben Sie eine Wartungsanfragenkennung ein.</span><span class="sxs-lookup"><span data-stu-id="0d071-216">If number sequence is enabled for maintenance requests in **Asset management**, the **Maintenance request** field is hidden because it is automatically filled out. If the **Maintenance request** field is visible, enter a maintenance request ID.</span></span>

1. <span data-ttu-id="0d071-217">Wählen Sie einen **Wartungsanfragetyp** aus.</span><span class="sxs-lookup"><span data-stu-id="0d071-217">Select a **Maintenance request type**.</span></span>

1. <span data-ttu-id="0d071-218">Geben Sie eine **Beschreibung** für die Wartungsanfrage ein.</span><span class="sxs-lookup"><span data-stu-id="0d071-218">Enter a **Description** for the maintenance request.</span></span>

1. <span data-ttu-id="0d071-219">Wählen Sie die **Anlage** aus, für die Sie eine Anfrage erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="0d071-219">Select the **Asset** you want to create the request for.</span></span>

1. <span data-ttu-id="0d071-220">Wählen Sie die **Leistungsebene** für die Wartungsanfrage aus.</span><span class="sxs-lookup"><span data-stu-id="0d071-220">Select the **Service level** for the maintenance request.</span></span>

1. <span data-ttu-id="0d071-221">Wählen Sie **Fertig**.</span><span class="sxs-lookup"><span data-stu-id="0d071-221">Select **Done**.</span></span>

    <span data-ttu-id="0d071-222">![Eine Wartungsanfrage erstellen](media/am-mobile-09.png "Eine Wartungsanfrage erstellen")</span><span class="sxs-lookup"><span data-stu-id="0d071-222">![Create a maintenance request](media/am-mobile-09.png "Create a maintenance request")</span></span>

## <a name="add-attachment-to-a-maintenance-request"></a><span data-ttu-id="0d071-223">Einer Wartungsanforderung einen Anhang hinzufügen</span><span class="sxs-lookup"><span data-stu-id="0d071-223">Add attachment to a maintenance request</span></span>

1. <span data-ttu-id="0d071-224">Öffnen Sie auf Ihrem mobilen Gerät den Arbeitsbereich für die **Anlagenverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="0d071-224">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="0d071-225">Wählen Sie **Alle Wartungsanfragen** aus.</span><span class="sxs-lookup"><span data-stu-id="0d071-225">Select **All maintenance requests**.</span></span>

1. <span data-ttu-id="0d071-226">Wählen Sie die Wartungsanfrage aus, der Sie einen Anhang hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="0d071-226">Select the maintenance request you want to add an attachment to.</span></span>

1. <span data-ttu-id="0d071-227">Wählen Sie **Anhänge** am unteren Bildschirmrand aus.</span><span class="sxs-lookup"><span data-stu-id="0d071-227">Select **Attachments** at the bottom of the screen.</span></span>

1. <span data-ttu-id="0d071-228">Wählen Sie **Anhänge hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="0d071-228">Select **Add attachments**.</span></span>

1. <span data-ttu-id="0d071-229">Geben Sie **Name** und **Notizen** für dien Anhang ein.</span><span class="sxs-lookup"><span data-stu-id="0d071-229">Enter **Name** and **Notes** for the attachment.</span></span>

1. <span data-ttu-id="0d071-230">Wählen Sie **Bild auswählen** aus, um ein Foto aus der mobilen Galerie auszuwählen, oder **Foto aufnehmen**, um ein Foto zu machen.</span><span class="sxs-lookup"><span data-stu-id="0d071-230">Select **Choose image** to select a photo from the mobile gallery or **Take photo** to take a photo.</span></span>

1. <span data-ttu-id="0d071-231">Wählen Sie **Fertig**.</span><span class="sxs-lookup"><span data-stu-id="0d071-231">Select **Done**.</span></span>

    <span data-ttu-id="0d071-232">![Einer Wartungsanfrage einen Anhang hinzufügen](media/am-mobile-10.png "Einer Wartungsanfrage einen Anhang hinzufügen")</span><span class="sxs-lookup"><span data-stu-id="0d071-232">![Add an attachment to a maintenance request](media/am-mobile-10.png "Add an attachment to a maintenance request")</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]