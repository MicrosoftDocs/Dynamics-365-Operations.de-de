---
title: Mobilen Arbeitsbereich für die Anlagenverwaltung einrichten
description: In diesem Thema wird beschrieben, wie Sie Microsoft Dynamics 365 Supply Chain Management und die mobile Finance and Operations-App (Dynamics 365) einrichten, um einen mobilen Arbeitsbereich für die Anlagenverwaltung auszuführen, mit dem Arbeitskräfte Anlagenverwaltungsaufgaben durchführen können.
author: johanhoffmann
manager: tfehr
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-22
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 9c2410c50b5d289792e2cc364674e1e093653590
ms.sourcegitcommit: 995c678b4715be267f1f97148902a6b3dde3bcab
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/20/2021
ms.locfileid: "5033209"
---
# <a name="set-up-the-asset-management-mobile-workspace"></a><span data-ttu-id="ad5e4-103">Mobilen Arbeitsbereich für die Anlagenverwaltung einrichten</span><span class="sxs-lookup"><span data-stu-id="ad5e4-103">Set up the Asset management mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ad5e4-104">In diesem Thema wird beschrieben, wie Sie Microsoft Dynamics 365 Supply Chain Management und die mobile Finance and Operations-App (Dynamics 365) einrichten, um einen mobilen Arbeitsbereich für die **Anlagenverwaltung** auszuführen, mit dem Arbeitskräfte Anlagenverwaltungsaufgaben durchführen können.</span><span class="sxs-lookup"><span data-stu-id="ad5e4-104">This topic describes how to set up Microsoft Dynamics 365 Supply Chain Management and the Finance and Operations (Dynamics 365) mobile app to run an **Asset management** mobile workspace that workers can use to perform asset management tasks.</span></span>

## <a name="set-up-maintenance-worker-users-in-supply-chain-management"></a><span data-ttu-id="ad5e4-105">Einrichten von Benutzern als Wartungsarbeiter in Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="ad5e4-105">Set up maintenance worker users in Supply Chain Management</span></span>

<span data-ttu-id="ad5e4-106">Führen Sie für jeden Benutzer, der Zugriff auf den mobilen Arbeitsbereich für die **Anlalgenverwaltung** benötigt, die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="ad5e4-106">For each user that requires access to the **Asset management** mobile workspace, follow these steps.</span></span>

1. <span data-ttu-id="ad5e4-107">Wechseln Sie in Supply Chain Management zu **Personalverwaltung \> Arbeitskräfte** und stellen Sie sicher, dass ein Arbeitskraftdatensatz für den Benutzer vorhanden ist, den Sie einrichten möchten.</span><span class="sxs-lookup"><span data-stu-id="ad5e4-107">In Supply Chain Management, go to **Human resources \> Workers**, and make sure that a worker record exists for the user that you want to set up.</span></span> <span data-ttu-id="ad5e4-108">Erstellen Sie gegebenenfalls einen neuen Arbeitskraftdatensatz.</span><span class="sxs-lookup"><span data-stu-id="ad5e4-108">Create a new worker record as required.</span></span>
1. <span data-ttu-id="ad5e4-109">Wechseln Sie zu **Anlagenverwaltung \> Einrichten \> Arbeitskräfte \> Arbeitskräfte** und stellen Sie sicher, dass der Arbeitskraftdatensatz, den Sie im vorherigen Schritt gesucht (oder erstellt) haben, einem Wartungsarbeiterdatensatz zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ad5e4-109">Go to **Asset management \> Setup \> Workers \> Workers**, and make sure that the worker record that you identified (or created) in the previous step is mapped to a maintenance worker record.</span></span> <span data-ttu-id="ad5e4-110">Erstellen Sie gegebenenfalls einen neuen Wartungsarbeiterdatensatz und legen Sie das Feld **Arbeiter** auf den Arbeitskraftdatensatz aus dem vorherigen Schritt fest.</span><span class="sxs-lookup"><span data-stu-id="ad5e4-110">Create a new maintenance worker record as required, and set the **Worker** field to the worker record from the previous step.</span></span>
1. <span data-ttu-id="ad5e4-111">Wechseln Sie zu **Anlagenverwaltung \> Einrichten \> Arbeitskräfte \> Wartungsarbeitergruppen** und stellen Sie sicher, dass der Wartungsarbeiterdatensatz, den Sie im vorherigen Schritt gesucht (oder erstellt) haben, einer Wartungsarbeitergruppe angehört.</span><span class="sxs-lookup"><span data-stu-id="ad5e4-111">Go to **Asset management \> Setup \> Workers \> Maintenance worker groups**, and make sure that the maintenance worker record that you identified (or created) in the previous step belongs to a maintenance worker group.</span></span>
1. <span data-ttu-id="ad5e4-112">Wechseln Sie zu **Systemverwaltung \> Benutzer**.</span><span class="sxs-lookup"><span data-stu-id="ad5e4-112">Go to **System administration \> Users**.</span></span>
1. <span data-ttu-id="ad5e4-113">Wählen Sie den relevanten Benutzer im Raster aus.</span><span class="sxs-lookup"><span data-stu-id="ad5e4-113">Select the relevant user in the grid.</span></span>
1. <span data-ttu-id="ad5e4-114">Legen Sie im Inforegister **Nutzerdetails** das Feld **Person** auf das Arbeitskraftkonto fest, das Sie dem aktuellen Benutzerkonto zuordnen möchten.</span><span class="sxs-lookup"><span data-stu-id="ad5e4-114">On the **User Details** FastTab, set the **Person** field to the worker account that you want to associate with the current user account.</span></span> <span data-ttu-id="ad5e4-115">Dieses Arbeitskraftkonto sollte der Arbeitskraftdatensatz sein, den Sie in Schritt 1 gesucht (oder erstellt) und in Schritt 2 einem Wartungsarbeiterdatensatz zugeordnet haben.</span><span class="sxs-lookup"><span data-stu-id="ad5e4-115">This worker account should be the worker record that you identified (or created) in step 1 and mapped to a maintenance worker record in step 2.</span></span>

> [!NOTE]
> <span data-ttu-id="ad5e4-116">Benutzerberechtigungen und Sicherheitsrollen gelten für die Funktionen des mobilen Arbeitsbereichs für die **Anlagenverwaltung** ebenso wie für die Funktionen der Benutzeroberfläche von Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ad5e4-116">User permissions and security roles apply to the features of the **Asset management** mobile workspace just as they apply to the features of the Supply Chain Management user interface.</span></span> <span data-ttu-id="ad5e4-117">Daher muss jeder Benutzer, den Sie für den Zugriff auf den mobilen Arbeitsbereich für die **Anlagenverwaltung** einrichten, über die Sicherheitsrollen verfügen, die zur Ausführung ähnlicher Vorgänge direkt in Supply Chain Management erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="ad5e4-117">Therefore, every user that you set up to access the **Asset management** mobile workspace must have the security roles that are required to perform similar operations directly in Supply Chain Management.</span></span>

## <a name="publish-the-asset-management-mobile-workspace"></a><span data-ttu-id="ad5e4-118">Mobilen Arbeitsbereich für die Anlagenverwaltung veröffentlichen</span><span class="sxs-lookup"><span data-stu-id="ad5e4-118">Publish the Asset management mobile workspace</span></span>

<span data-ttu-id="ad5e4-119">Um Funktionen für das Anlagenmanagement in der mobilen Finance and Operations-App (Dynamics 365) verfügbar zu machen, müssen Sie den mobilen Arbeitsbereich für die **Anlagenverwaltung** veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="ad5e4-119">To make asset management features available in the Finance and Operations (Dynamics 365) mobile app, you must publish the **Asset management** mobile workspace.</span></span>

1. <span data-ttu-id="ad5e4-120">Wählen Sie in Supply Chain Management die Schaltfläche **Einstellungen** aus (das Zahnradsymbol oben rechts) und wählen Sie dann im Menü **Mobile App** aus.</span><span class="sxs-lookup"><span data-stu-id="ad5e4-120">In Supply Chain Management, select the **Settings** button (the gear symbol in upper-right corner), and then select **Mobile app** on the menu.</span></span>
1. <span data-ttu-id="ad5e4-121">Suchen Sie im Dialogfeld **Mobile App verwalten** die Kachel **Anlagenverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="ad5e4-121">In the **Manage mobile app** dialog box, find the **Asset Management** tile.</span></span> <span data-ttu-id="ad5e4-122">Wenn sie den Text „In Metadaten – nicht veröffentlicht“ enthält, wurde der Arbeitsbereich noch nicht veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="ad5e4-122">If it contains the text "In metadata - not published," the workspace hasn't yet been published.</span></span> <span data-ttu-id="ad5e4-123">Wenn sie den Text „In Metadaten – veröffentlicht“ enthält, wurde der Arbeitsbereich bereits veröffentlicht und Sie können den Rest dieser Prozedur überspringen.</span><span class="sxs-lookup"><span data-stu-id="ad5e4-123">If it contains the text "In metadata - published," the workspace has already been published, and you can skip the rest of this procedure.</span></span>

    <span data-ttu-id="ad5e4-124">![Das Dialogfeld „Mobile App verwalten“](media/mobile-workspaces.png "Das Dialogfeld „Mobile App verwalten“")</span><span class="sxs-lookup"><span data-stu-id="ad5e4-124">![Manage mobile app dialog box](media/mobile-workspaces.png "Manage mobile app dialog box")</span></span>

1. <span data-ttu-id="ad5e4-125">Wähle Sie die Kachel **Anlagenverwaltung** aus und wählen Sie dann auf der Symbolleiste **Veröffentlichen** aus.</span><span class="sxs-lookup"><span data-stu-id="ad5e4-125">Select the **Asset Management** tile, and then select **Publish** on the toolbar.</span></span> <span data-ttu-id="ad5e4-126">Nach einigen Sekunden sollten Sie eine Benachrichtigung erhalten, dass der Arbeitsbereich erfolgreich veröffentlicht wurde.</span><span class="sxs-lookup"><span data-stu-id="ad5e4-126">After a few seconds, you should receive a notification that states that the workspace has been successfully published.</span></span> <span data-ttu-id="ad5e4-127">Außerdem sollte sich der Text auf der Kachel in „In Metadaten – veröffentlicht“ ändern.</span><span class="sxs-lookup"><span data-stu-id="ad5e4-127">Additionally, the text on the tile should change to "In metadata - published."</span></span>

## <a name="install-and-set-up-the-finance-and-operations-dynamics-365-mobile-app"></a><span data-ttu-id="ad5e4-128">Installieren und einrichten der mobilen Finance and Operations-App (Dynamics 365)</span><span class="sxs-lookup"><span data-stu-id="ad5e4-128">Install and set up the Finance and Operations (Dynamics 365) mobile app</span></span>

1. <span data-ttu-id="ad5e4-129">Öffnen Sie einen der folgenden App-Stores, um die App **Microsoft Finance and Operations (Dynamics 365)** auf Ihrem Mobilgerät zu installieren:</span><span class="sxs-lookup"><span data-stu-id="ad5e4-129">Go to one of the following app stores to install the **Microsoft Finance and Operations (Dynamics 365)** app on your mobile device:</span></span>

    - [<span data-ttu-id="ad5e4-130">Für Google Android-Geräte</span><span class="sxs-lookup"><span data-stu-id="ad5e4-130">For Google Android devices</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
    - [<span data-ttu-id="ad5e4-131">Für Apple iOS-Geräte</span><span class="sxs-lookup"><span data-stu-id="ad5e4-131">For Apple iOS devices</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

1. <span data-ttu-id="ad5e4-132">Öffnen Sie die Finance and Operations-App (Dynamics 365).</span><span class="sxs-lookup"><span data-stu-id="ad5e4-132">Open the Finance and Operations (Dynamics 365) app.</span></span> <span data-ttu-id="ad5e4-133">Die Anmeldeseite sollte angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ad5e4-133">The sign-in page should appear.</span></span> <span data-ttu-id="ad5e4-134">Geben Sie im Feld **Anmelden** Ihre Supply Chain Management-URL ein oder wählen Sie in der Liste **Letzte Umgebungen** eine aktuelle URL aus und tippen Sie dann auf **Verbinden**.</span><span class="sxs-lookup"><span data-stu-id="ad5e4-134">In the **Sign in** field, enter your Supply Chain Management URL, or select a recent URL in the **Recent environments** list, and then tap **Connect**.</span></span>

    <span data-ttu-id="ad5e4-135">![Anmeldeseite](media/mobile-app-sign-in.png "Anmeldeseite")</span><span class="sxs-lookup"><span data-stu-id="ad5e4-135">![Sign-in page](media/mobile-app-sign-in.png "Sign-in page")</span></span>

1. <span data-ttu-id="ad5e4-136">Wenn Sie aufgefordert werden, die Verbindung zu bestätigen, aktivieren Sie das Kontrollkästchen **Verstanden** und tippen Sie anschließend auf **Verbinden**.</span><span class="sxs-lookup"><span data-stu-id="ad5e4-136">If you're prompted to confirm the connection, select the **I understand** check box, and then tap **Connect**.</span></span>
1. <span data-ttu-id="ad5e4-137">Verwenden Sie auf der Seite **Konto auswählen** Ihr Microsoft-Konto aus, um sich bei der mobilen Anwendung anzumelden.</span><span class="sxs-lookup"><span data-stu-id="ad5e4-137">On the **Pick an account** page, use your Microsoft account to sign in to the mobile application.</span></span>

    <span data-ttu-id="ad5e4-138">Die Seite **Arbeitsbereiche** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ad5e4-138">The **Workspaces** page appears.</span></span> <span data-ttu-id="ad5e4-139">Sie listet jeden mobilen Arbeitsbereich auf, der von Ihrer Supply Chain Management-Instanz veröffentlicht wurde.</span><span class="sxs-lookup"><span data-stu-id="ad5e4-139">It lists every mobile workspace that has been published by your Supply Chain Management instance.</span></span>

    <span data-ttu-id="ad5e4-140">![Liste der Arbeitsbereiche](media/mobile-app-workspaces.png "Liste der Arbeitsbereiche")</span><span class="sxs-lookup"><span data-stu-id="ad5e4-140">![List of workspaces](media/mobile-app-workspaces.png "List of workspaces")</span></span>

1. <span data-ttu-id="ad5e4-141">Wenn Sie die juristische Person (Firma) ändern müssen, tippen Sie oben links auf die Menütaste (manchmal auch als Hamburger oder Hamburgertaste bezeichnet) und anschließend auf **Firma ändern**.</span><span class="sxs-lookup"><span data-stu-id="ad5e4-141">If you must change the legal entity (company), tap the Menu button (sometimes referred to as the hamburger or the hamburger button) in the upper-left corner, and then tap **Change company**.</span></span>

    <span data-ttu-id="ad5e4-142">![Ändern der juristischen Person](media/mobile-app-change-comp.png "Ändern der juristischen Person")</span><span class="sxs-lookup"><span data-stu-id="ad5e4-142">![Changing the legal entity](media/mobile-app-change-comp.png "Changing the legal entity")</span></span>

1. <span data-ttu-id="ad5e4-143">Wählen Sie auf der Seite **Arbeitsbereiche** den Arbeitsbereich aus, mit dem Sie arbeiten möchten, um ihn zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ad5e4-143">On the **Workspaces** page, select the workspace that you want to work with to open it.</span></span>

    <span data-ttu-id="ad5e4-144">![Mobiler Arbeitsbereich für Anlagenverwaltung](media/mobile-app-asset-workspace.png "Mobiler Arbeitsbereich für Anlagenverwaltung")</span><span class="sxs-lookup"><span data-stu-id="ad5e4-144">![Asset management mobile workspace](media/mobile-app-asset-workspace.png "Asset management mobile workspace")</span></span>

## <a name="work-with-the-asset-management-mobile-workspace"></a><span data-ttu-id="ad5e4-145">Arbeiten mit dem mobilen Arbeitsbereich für die Anlagenverwaltung</span><span class="sxs-lookup"><span data-stu-id="ad5e4-145">Work with the Asset management mobile workspace</span></span>

<span data-ttu-id="ad5e4-146">Weitere Informationen zum Arbeiten mit dem mobilen Arbeitsbereich für die **Anlagenverwaltung** finden Sie unter [Mobilen Arbeitsbereich für die Anlagenverwaltung nutzen](asset-management-mobile-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="ad5e4-146">For more information about how to work with the **Asset management** mobile workspace, see [Use the Asset management mobile workspace](asset-management-mobile-workspace.md).</span></span>

<span data-ttu-id="ad5e4-147">Weitere Informationen zur mobilen Finance and Operations-App (Dynamics 365) finden Sie unter [Startseite der mobilen App](../../fin-ops-core/dev-itpro/mobile-apps/Mobile-app-home-page.md).</span><span class="sxs-lookup"><span data-stu-id="ad5e4-147">For more information about the Finance and Operations (Dynamics 365) mobile app, see the [Mobile app home page](../../fin-ops-core/dev-itpro/mobile-apps/Mobile-app-home-page.md).</span></span>
