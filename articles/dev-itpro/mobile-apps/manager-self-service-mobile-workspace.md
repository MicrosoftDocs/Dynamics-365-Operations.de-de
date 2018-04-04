---
title: "Mobiler Arbeitsbereich für mein Team"
description: "Dieses Thema enthält Informationen zum Mein Team mobilen Arbeitsbereich, mit dem Manager ihre eigenen Mitarbeiter und erweitertes Personal anzeigen können. Benutzer können auch Lob an Personen in der Mitarbeitergruppe senden."
author: ShielaSogge
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: aa2bbfab4afa59c15e28526192cc07be13da11d7
ms.contentlocale: de-de
ms.lasthandoff: 03/26/2018

---

# <a name="my-team-mobile-workspace"></a><span data-ttu-id="5bdee-104">Mobiler Arbeitsbereich für mein Team</span><span class="sxs-lookup"><span data-stu-id="5bdee-104">My team mobile workspace</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="5bdee-105">Dieses Thema enthält Informationen zum mobilen Arbeitsbereich **Mein Team**.</span><span class="sxs-lookup"><span data-stu-id="5bdee-105">This topic provides information about the **My team** mobile workspace.</span></span> <span data-ttu-id="5bdee-106">Mit dem Arbeitsbereich können Manager ihre eigenen Mitarbeiter und erweitertes Personal anzeigen.</span><span class="sxs-lookup"><span data-stu-id="5bdee-106">This workspace lets managers view their direct reports and extended staff.</span></span> <span data-ttu-id="5bdee-107">Sie können auch Lob an Personen innerhalb der Mitarbeitergruppe senden.</span><span class="sxs-lookup"><span data-stu-id="5bdee-107">They can also send praise to individuals in their reporting chain.</span></span>

<span data-ttu-id="5bdee-108">Dieser mobile Arbeitsbereich soll mit der Mobil-App für Microsoft Dynamics 365 für Unified Operations verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5bdee-108">This mobile workspace is intended to be used with the Microsoft Dynamics 365 for Unified Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="5bdee-109">Überblick</span><span class="sxs-lookup"><span data-stu-id="5bdee-109">Overview</span></span> 
<span data-ttu-id="5bdee-110">Der mobile Arbeitsbereich **Mein Team** ermöglicht Managern, folgende Aufgaben auszuführen:</span><span class="sxs-lookup"><span data-stu-id="5bdee-110">The **My team** mobile workspace lets managers perform these tasks:</span></span>

- <span data-ttu-id="5bdee-111">Liste der eigenen Mitarbeiter des Managers anzeigen.</span><span class="sxs-lookup"><span data-stu-id="5bdee-111">View a list of the manager’s direct reports.</span></span>
- <span data-ttu-id="5bdee-112">Liste des erweiterten Mitarbeiterstamm des Managers anzeigen.</span><span class="sxs-lookup"><span data-stu-id="5bdee-112">View a list of the manager’s extended reporting team.</span></span>
- <span data-ttu-id="5bdee-113">Anzeigen von detaillierten Informationen zu einzelnen Teammitgliedern wie Geburtsdatum, Dienstalter, Dienstjahre sowie Informationen zu Vergütung und Leistung.</span><span class="sxs-lookup"><span data-stu-id="5bdee-113">View detailed information for each team member, such as birth date, seniority date, years of service, and compensation and performance information.</span></span>
- <span data-ttu-id="5bdee-114">Senden von Lob an einzelne Personen aus dem erweiterten Mitarbeiterteam des Managers.</span><span class="sxs-lookup"><span data-stu-id="5bdee-114">Send praise to any individual in the manager’s extended reporting team.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5bdee-115">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="5bdee-115">Prerequisites</span></span>
<span data-ttu-id="5bdee-116">Bevor Sie diesen mobilen Arbeitsbereich verwenden können, müssen die folgenden Voraussetzungen erfüllt werden.</span><span class="sxs-lookup"><span data-stu-id="5bdee-116">Before you can use this mobile workspace, the following prerequisites must be met.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="5bdee-117">Voraussetzung</span><span class="sxs-lookup"><span data-stu-id="5bdee-117">Prerequisite</span></span></th>
<th><span data-ttu-id="5bdee-118">Rolle</span><span class="sxs-lookup"><span data-stu-id="5bdee-118">Role</span></span></th>
<th><span data-ttu-id="5bdee-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5bdee-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5bdee-120">Eines der folgenden Produkte muss in der Organisation bereitgestellt werden:</span><span class="sxs-lookup"><span data-stu-id="5bdee-120">One of the following products must be deployed in your organization:</span></span>
<ul><li><span data-ttu-id="5bdee-121">Microsoft Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5bdee-121">Microsoft Dynamics 365 for Finance and Operations</span></span></li>
<li><span data-ttu-id="5bdee-122">Microsoft Dynamics 365 for Talent</span><span class="sxs-lookup"><span data-stu-id="5bdee-122">Microsoft Dynamics 365 for Talent</span></span></li>
</ul>
</td>
<td><span data-ttu-id="5bdee-123">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="5bdee-123">System administrator</span></span></td>
<td><span data-ttu-id="5bdee-124">Wenn Finance und Operations nicht bereits in der Organisation bereitgestellt wurde, finden Sie Informationen unter <a href="../deployment/deploy-demo-environment.md">Eine Demoumgebung bereitstellen</a>.</span><span class="sxs-lookup"><span data-stu-id="5bdee-124">If you don't already have Finance and Operations deployed in your organization, see <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span> <span data-ttu-id="5bdee-125">Wenn Talent nicht bereits in der Organisation bereitgestellt wurde, kann der Systemadministrator von der <a href="https://www.microsoft.com/en-us/dynamics365/talent">Talent-Webseite</a> auf eine Testversion zugreifen.</span><span class="sxs-lookup"><span data-stu-id="5bdee-125">If you don't already have Talent deployed in your organization, the system administrator can access a trial version from the <a href="https://www.microsoft.com/en-us/dynamics365/talent">Talent webpage</a>.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="5bdee-126">Der mobile Arbeitsbereich <strong>Mein Team</strong> muss veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="5bdee-126">The <strong>My team</strong> mobile workspace must be published.</span></span></td>
<td><span data-ttu-id="5bdee-127">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="5bdee-127">System administrator</span></span></td>
<td><span data-ttu-id="5bdee-128">Siehe <a href="publish-mobile-workspace.md">Einen mobilen Arbeitsbereich veröffentlichen</a>.</span><span class="sxs-lookup"><span data-stu-id="5bdee-128">See <a href="publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="5bdee-129">Herunterladen und Installieren der mobilen App</span><span class="sxs-lookup"><span data-stu-id="5bdee-129">Download and install the mobile app</span></span>

<span data-ttu-id="5bdee-130">Laden Sie die mobile App für Dynamics 365 for Unified Operations herunter und installieren Sie diese:</span><span class="sxs-lookup"><span data-stu-id="5bdee-130">Download and install the Dynamics 365 for Unified Operations mobile app:</span></span>

-   [<span data-ttu-id="5bdee-131">Für Androide-Smartphones</span><span class="sxs-lookup"><span data-stu-id="5bdee-131">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="5bdee-132">Für iPhones</span><span class="sxs-lookup"><span data-stu-id="5bdee-132">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="5bdee-133">Bei der mobile App anmelden</span><span class="sxs-lookup"><span data-stu-id="5bdee-133">Sign in to the mobile app</span></span>
1.  <span data-ttu-id="5bdee-134">Starten Sie die App auf Ihrem mobilen Gerät.</span><span class="sxs-lookup"><span data-stu-id="5bdee-134">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="5bdee-135">Geben Sie die Microsoft Dynamics 365-URL ein.</span><span class="sxs-lookup"><span data-stu-id="5bdee-135">Enter your Microsoft Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="5bdee-136">Bei der erstmaligen Anwendung werden Sie nach Ihrem Benutzernamen und dem Kennwort gefragt.</span><span class="sxs-lookup"><span data-stu-id="5bdee-136">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="5bdee-137">Geben Sie Ihre Anmeldeinformationen ein.</span><span class="sxs-lookup"><span data-stu-id="5bdee-137">Enter your credentials.</span></span>
4.  <span data-ttu-id="5bdee-138">Nachdem Sie sich angemeldet haben, werden verfügbare Arbeitsbereiche für Ihr Unternehmen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5bdee-138">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="5bdee-139">Beachten Sie, dass Sie, wenn Ihr Systemadministrator einen neuen Arbeitsbereich später veröffentlicht, die Liste der mobilen Arbeitsbereiche aktualisieren müssen.</span><span class="sxs-lookup"><span data-stu-id="5bdee-139">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="5bdee-140">[![Zum Aktualisieren ziehen](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="5bdee-140">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="view-team-members-by-using-the-my-team-mobile-workspace"></a><span data-ttu-id="5bdee-141">Anzeigen von Teammitglieder mit dem Mein Team-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="5bdee-141">View team members by using the My team mobile workspace</span></span>
1.  <span data-ttu-id="5bdee-142">Wählen Sie in der mobilen App den Arbeitsbereich **Mein Team** aus.</span><span class="sxs-lookup"><span data-stu-id="5bdee-142">In the mobile app, select the **My team** workspace.</span></span> <span data-ttu-id="5bdee-143">Eine Liste von Teammitgliedern wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5bdee-143">A list of team members is shown.</span></span> <span data-ttu-id="5bdee-144">Die Liste enthält auch die Titel jedes Teammitglieds sowie alle eigenen Mitarbeiter.</span><span class="sxs-lookup"><span data-stu-id="5bdee-144">The list also shows each team member's title, and any direct reports that he or she has.</span></span>
2.  <span data-ttu-id="5bdee-145">Wählen Sie ein Teammitglied aus.</span><span class="sxs-lookup"><span data-stu-id="5bdee-145">Select a team member.</span></span> <span data-ttu-id="5bdee-146">Die Seite **Teammitgliedszusammenfassung** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5bdee-146">The **Team member summary** page appears.</span></span> <span data-ttu-id="5bdee-147">Die Informationen auf dieser Seite enthalten das Geburtsdatum des Teammitglieds, das Dienstalter, die Dienstjahre, die Jahre in der aktuellen Position sowie Informationen zur Vergütung.</span><span class="sxs-lookup"><span data-stu-id="5bdee-147">The information on this page includes the team member's birth date, seniority date, years of service, years in his or her current position, and compensation information.</span></span>

## <a name="view-extended-team-members-by-using-the-my-team-mobile-workspace"></a><span data-ttu-id="5bdee-148">Anzeigen von erweiterten Teammitgliedern mit dem Mein Team-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="5bdee-148">View extended team members by using the My team mobile workspace</span></span>
1.  <span data-ttu-id="5bdee-149">Wählen Sie in der mobilen App den Arbeitsbereich **Mein Team** aus.</span><span class="sxs-lookup"><span data-stu-id="5bdee-149">In the mobile app, select the **My team** workspace.</span></span> <span data-ttu-id="5bdee-150">Eine Liste von Teammitgliedern wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5bdee-150">A list of team members is shown.</span></span> <span data-ttu-id="5bdee-151">Die Liste enthält auch die Titel jedes Teammitglieds sowie alle eigenen Mitarbeiter.</span><span class="sxs-lookup"><span data-stu-id="5bdee-151">The list also shows each team member's title, and any direct reports that he or she has.</span></span>
1.  <span data-ttu-id="5bdee-152">Wählen Sie den Link **Eigene Mitarbeiter** aus.</span><span class="sxs-lookup"><span data-stu-id="5bdee-152">Select the **Direct reports** link.</span></span> <span data-ttu-id="5bdee-153">Eine Liste des erweiterten Teams wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5bdee-153">A list of your extended team is shown.</span></span>
1.  <span data-ttu-id="5bdee-154">Wählen Sie ein Teammitglied aus.</span><span class="sxs-lookup"><span data-stu-id="5bdee-154">Select a team member.</span></span> <span data-ttu-id="5bdee-155">Die Seite **Teammitgliedszusammenfassung** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5bdee-155">The **Team member summary** page appears.</span></span> <span data-ttu-id="5bdee-156">Die Informationen auf dieser Seite enthalten das Geburtsdatum des Teammitglieds, das Dienstalter, die Dienstjahre, die Jahre in der aktuellen Position sowie Informationen zur Vergütung.</span><span class="sxs-lookup"><span data-stu-id="5bdee-156">The information on this page includes the team member's birth date, seniority date, years of service, years in his or her current position, and compensation information.</span></span>

## <a name="send-praise-about-team-members-by-using-the-my-team-mobile-workspace"></a><span data-ttu-id="5bdee-157">Senden von Lob an Teammitgliedern mit dem Mein Team-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="5bdee-157">Send praise about team members by using the My team mobile workspace</span></span>
1.  <span data-ttu-id="5bdee-158">Wählen Sie in der mobilen App den Arbeitsbereich **Mein Team** aus.</span><span class="sxs-lookup"><span data-stu-id="5bdee-158">In the mobile app, select the **My team** workspace.</span></span> <span data-ttu-id="5bdee-159">Eine Liste von Teammitgliedern wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5bdee-159">A list of team members is shown.</span></span> <span data-ttu-id="5bdee-160">Die Liste enthält auch die Titel jedes Teammitglieds sowie alle eigenen Mitarbeiter.</span><span class="sxs-lookup"><span data-stu-id="5bdee-160">The list also shows each team member's title, and any direct reports that he or she has.</span></span>
1.  <span data-ttu-id="5bdee-161">Wählen Sie ein Teammitglied aus.</span><span class="sxs-lookup"><span data-stu-id="5bdee-161">Select a team member.</span></span> <span data-ttu-id="5bdee-162">Die Seite **Teammitgliedszusammenfassung** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5bdee-162">The **Team member summary** page appears.</span></span>
1.  <span data-ttu-id="5bdee-163">Wählen Sie **Lob versenden**.</span><span class="sxs-lookup"><span data-stu-id="5bdee-163">Select **Send praise**.</span></span> 
1. <span data-ttu-id="5bdee-164">Geben Sie den Text des Lobs ein, das Sie übermitteln möchten.</span><span class="sxs-lookup"><span data-stu-id="5bdee-164">Enter the text of the praise that you want to send.</span></span> 
1. <span data-ttu-id="5bdee-165">Wählen Sie **Fertig**.</span><span class="sxs-lookup"><span data-stu-id="5bdee-165">Select **Done**.</span></span>

