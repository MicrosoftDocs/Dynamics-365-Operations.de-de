---
title: Aufgabenverwaltung zwischen Microsoft Teams und Dynamics 365 Commerce POS synchronisieren
description: In diesem Thema wird beschrieben, wie Sie die Aufgabenverwaltung zwischen Microsoft Teams und der Verkaufsstelle (POS) in Dynamics 365 Commerce synchronisieren.
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: ca0cb32ac3ee508ddcd5346a895fb9904fa92517
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842671"
---
# <a name="synchronize-task-management-between-microsoft-teams-and-dynamics-365-commerce-pos"></a><span data-ttu-id="ce1ce-103">Aufgabenverwaltung zwischen Microsoft Teams und Dynamics 365 Commerce POS synchronisieren</span><span class="sxs-lookup"><span data-stu-id="ce1ce-103">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="ce1ce-104">In diesem Thema wird beschrieben, wie Sie die Aufgabenverwaltung zwischen Microsoft Teams und der Verkaufsstelle (POS) in Dynamics 365 Commerce synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="ce1ce-104">This topic describes how to synchronize task management between Microsoft Teams and Dynamics 365 Commerce point of sale (POS).</span></span>

<span data-ttu-id="ce1ce-105">Einer der Hauptzwecke der Teams-Integration besteht darin, die Synchronisierung der Aufgabenverwaltung zwischen der POS-Anwendung und Teams zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="ce1ce-105">One of the main purposes of Teams integration is to enable the synchronization of task management between the POS application and Teams.</span></span> <span data-ttu-id="ce1ce-106">Auf diese Weise können Filialmitarbeiter entweder die POS-Anwendung oder Teams zum Verwalten von Aufgaben verwenden und müssen nicht zwischen Anwendungen wechseln.</span><span class="sxs-lookup"><span data-stu-id="ce1ce-106">In this way, store employees can use either the POS application or Teams to manage tasks, and don't have to switch applications.</span></span>

<span data-ttu-id="ce1ce-107">Da Planner als Repository für Aufgaben in Teams verwendet wird, muss eine Verknüpfung zwischen Teams und Dynamics 365 Commerce bestehen.</span><span class="sxs-lookup"><span data-stu-id="ce1ce-107">Because Planner is used as a repository for tasks in Teams, there must be a link between Teams and Dynamics 365 Commerce.</span></span> <span data-ttu-id="ce1ce-108">Diese Verknüpfung wird mithilfe einer bestimmten Plan-ID für ein bestimmtes Filialteam hergestellt.</span><span class="sxs-lookup"><span data-stu-id="ce1ce-108">This link is established by using a specific plan ID for a given store team.</span></span>

<span data-ttu-id="ce1ce-109">Die folgenden Prozeduren zeigen, wie Sie die Synchronisierung der Aufgabenverwaltung zwischen der POS- und der Teams-Anwendung einrichten.</span><span class="sxs-lookup"><span data-stu-id="ce1ce-109">The following procedures show how to set up task management synchronization between the POS and Teams applications.</span></span>

## <a name="publish-a-test-task-list-in-teams"></a><span data-ttu-id="ce1ce-110">Eine Testaufgabenliste in Teams veröffentlichen</span><span class="sxs-lookup"><span data-stu-id="ce1ce-110">Publish a test task list in Teams</span></span>

<span data-ttu-id="ce1ce-111">Die folgende Prozedur setzt voraus, dass Ihre Filialteams die Aufgabenverwaltungsintegration von Microsoft Teams mit Commerce zum ersten Mal verwenden.</span><span class="sxs-lookup"><span data-stu-id="ce1ce-111">The following procedure assumes that your store teams are using Microsoft Teams task management integration with Commerce for the first time.</span></span>

<span data-ttu-id="ce1ce-112">Führen Sie die folgenden Schritte aus, um eine Testaufgabenliste in Teams zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="ce1ce-112">To publish a test task list in Teams, follow these steps.</span></span>

1. <span data-ttu-id="ce1ce-113">Melden Sie sich in Teams als Kommunikationsmanager an.</span><span class="sxs-lookup"><span data-stu-id="ce1ce-113">Sign in to Teams as a communications manager.</span></span> <span data-ttu-id="ce1ce-114">In der Regel sind Kommunikationsmanager Benutzer, die über in Commerce über die Rolle **Regionalmanager** verfügen.</span><span class="sxs-lookup"><span data-stu-id="ce1ce-114">Typically, communications managers are users who have the **Regional manager** role in Commerce.</span></span>
1. <span data-ttu-id="ce1ce-115">Wählen Sie im linken Navigationsbereich **Aufgaben aus Planner** aus.</span><span class="sxs-lookup"><span data-stu-id="ce1ce-115">In the left navigation pane, select **Tasks by Planner**.</span></span>
1. <span data-ttu-id="ce1ce-116">Wählen Sie auf der Registerkarte **Veröffentlichte Listen** unten links **Neue Liste** aus und benennen Sie die neue Liste **Testaufgabenliste**.</span><span class="sxs-lookup"><span data-stu-id="ce1ce-116">On the **Published lists** tab, select **New list** in the lower left, and name the new list **Test task list**.</span></span>
1. <span data-ttu-id="ce1ce-117">Wählen Sie **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="ce1ce-117">Select **Create**.</span></span> <span data-ttu-id="ce1ce-118">Die neue Liste wird unter **Entwürfe** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ce1ce-118">The new list appears under **Drafts**.</span></span>
1. <span data-ttu-id="ce1ce-119">Geben Sie unter **Aufgabentitel** der ersten Aufgabe den Titel **Teams-Integration testen**.</span><span class="sxs-lookup"><span data-stu-id="ce1ce-119">Under **Task title**, give the first task the title **Testing Teams integration**.</span></span> <span data-ttu-id="ce1ce-120">Wählen Sie dann **Eingeben** aus.</span><span class="sxs-lookup"><span data-stu-id="ce1ce-120">Then select **Enter**.</span></span>
1. <span data-ttu-id="ce1ce-121">Wählen Sie in der Liste **Entwürfe** die Aufgabenliste aus.</span><span class="sxs-lookup"><span data-stu-id="ce1ce-121">In the **Drafts** list, select the task list.</span></span> <span data-ttu-id="ce1ce-122">Dann wählen Sie dann  **Veröffentlichen**  in der oberen rechten Ecke.</span><span class="sxs-lookup"><span data-stu-id="ce1ce-122">Then select **Publish** in the upper-right corner.</span></span>
1. <span data-ttu-id="ce1ce-123">Im Dialogfeld **Auswählen, an wen veröffentlicht werden soll** wählen Sie die Teams aus, die die Liste der Testaufgaben erhalten sollen.</span><span class="sxs-lookup"><span data-stu-id="ce1ce-123">In the **Select who to publish to** dialog box, select the teams that should receive the test task list.</span></span>
1. <span data-ttu-id="ce1ce-124">Wählen Sie **Weiter**, um Ihren Veröffentlichungsplan zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="ce1ce-124">Select **Next** to review your publication plan.</span></span> <span data-ttu-id="ce1ce-125">Wenn Sie Änderungen vornehmen müssen, wählen Sie  **Zurück**.</span><span class="sxs-lookup"><span data-stu-id="ce1ce-125">If you must make changes, select **Back**.</span></span> 
1. <span data-ttu-id="ce1ce-126">Wählen Sie **Bestätigen und fortfahren** und dann **Veröffentlichen**.</span><span class="sxs-lookup"><span data-stu-id="ce1ce-126">Select **Confirm to proceed**, and then select **Publish**.</span></span>
1. <span data-ttu-id="ce1ce-127">Nach Abschluss der Veröffentlichung wird oben auf der Registerkarte **Veröffentlichte Listen** eine Meldung angezeigt, ob Ihre Aufgabenliste erfolgreich zugestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="ce1ce-127">After publishing is completed, a message at the top of the **Published lists** tab indicates whether your task list was successfully delivered.</span></span>

<span data-ttu-id="ce1ce-128">Weitere Informationen finden Sie unter [Veröffentlichen von Aufgabenlisten zum Erstellen und Nachverfolgen der Arbeit in Ihrer Organisation](https://support.microsoft.com/office/publish-task-lists-to-create-and-track-work-in-your-organization-095409b3-f5af-40aa-9f9e-339b54e705df).</span><span class="sxs-lookup"><span data-stu-id="ce1ce-128">For more information, see [Publish task lists to create and track work in your organization](https://support.microsoft.com/office/publish-task-lists-to-create-and-track-work-in-your-organization-095409b3-f5af-40aa-9f9e-339b54e705df).</span></span>

## <a name="link-pos-and-teams-for-task-management"></a><span data-ttu-id="ce1ce-129">POS und Teams für die Aufgabenverwaltung verknüpfen</span><span class="sxs-lookup"><span data-stu-id="ce1ce-129">Link POS and Teams for task management</span></span>

<span data-ttu-id="ce1ce-130">Um die POS- und Microsoft Teams-Anwendungen für die Aufgabenverwaltung in der Commerce-Zentralverwaltung zu verknüpfen, gehen Sie wie folgt vor.</span><span class="sxs-lookup"><span data-stu-id="ce1ce-130">To link the POS and Microsoft Teams applications for task management in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="ce1ce-131">Gehen Sie zu **Einzelhandel und Handel \> Aufgabenverwaltung \> Aufgabenintegration mit Microsoft Teams**.</span><span class="sxs-lookup"><span data-stu-id="ce1ce-131">Go to **Retail and Commerce \> Task management \> Tasks integration with Microsoft Teams**.</span></span>
1. <span data-ttu-id="ce1ce-132">Wählen Sie im Aktionsbereich **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="ce1ce-132">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="ce1ce-133">Setzen Sie die Option **Aufgabenverwaltungsintegration aktivieren** auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="ce1ce-133">Set the **Enable Task Management Integration** option to **Yes**.</span></span>
1. <span data-ttu-id="ce1ce-134">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="ce1ce-134">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="ce1ce-135">Wählen Sie im Aktivitätsbereich **Aufgabenverwaltung einrichten** aus.</span><span class="sxs-lookup"><span data-stu-id="ce1ce-135">On the Action Pane, select **Setup task management**.</span></span> <span data-ttu-id="ce1ce-136">Sie sollten eine Benachrichtigung erhalten, die angibt, dass ein Stapelverarbeitungsauftrag namens **Teams-Bereitstellung** erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="ce1ce-136">You should receive a notification that indicates that a batch job that is named **Teams provision** is being created.</span></span>
1. <span data-ttu-id="ce1ce-137">Gehen Sie zu **Systemadministration \> Anfragen \> Stapelverarbeitungsaufträge** und finden Sie den neuesten Auftrag mit der Beschreibung **Teams-Bereitstellung**.</span><span class="sxs-lookup"><span data-stu-id="ce1ce-137">Go to **System administration \> Inquiries \> Batch jobs**, and find the most recent job that has the description **Teams provision**.</span></span> <span data-ttu-id="ce1ce-138">Warten Sie, bis dieser Auftrag ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="ce1ce-138">Wait until this job has finished running.</span></span>
1. <span data-ttu-id="ce1ce-139">Führen Sie die den **CDX-Auftrag 1070** aus, um die Plan-ID zu veröffentlichen und Referenzen auf dem Retail Server zu speichern.</span><span class="sxs-lookup"><span data-stu-id="ce1ce-139">Run the **CDX job 1070** to publish the plan ID and store references to Retail Server.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ce1ce-140">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ce1ce-140">Additional resources</span></span>

[<span data-ttu-id="ce1ce-141">Überblick Integration Dynamics 365 Commerce und Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="ce1ce-141">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="ce1ce-142">Integration von Dynamics 365 Commerce und Microsoft Teams aktivieren</span><span class="sxs-lookup"><span data-stu-id="ce1ce-142">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="ce1ce-143">Microsoft Teams aus Dynamics 365 Commerce bereitstellen</span><span class="sxs-lookup"><span data-stu-id="ce1ce-143">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="ce1ce-144">Benutzerrollen in Microsoft Teams verwalten</span><span class="sxs-lookup"><span data-stu-id="ce1ce-144">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="ce1ce-145">Shops und Teams zuordnen, wenn in Microsoft Teams bereits Teams vorhanden sind</span><span class="sxs-lookup"><span data-stu-id="ce1ce-145">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="ce1ce-146">Integration von Dynamics 365 Commerce und Microsoft Teams – FAQ</span><span class="sxs-lookup"><span data-stu-id="ce1ce-146">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
