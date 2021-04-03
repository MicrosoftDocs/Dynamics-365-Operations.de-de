---
title: Mobiler Arbeitsbereich für mein Team
description: Dieses Thema enthält Informationen zum Mein Team mobilen Arbeitsbereich, mit dem Manager ihre eigenen Mitarbeiter und erweitertes Personal anzeigen können.
author: ShielaSogge
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 5dc2f8b5195fb5210ca6399cbf744f210671f475
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570086"
---
# <a name="my-team-mobile-workspace"></a><span data-ttu-id="89ee4-103">Mobiler Arbeitsbereich für mein Team</span><span class="sxs-lookup"><span data-stu-id="89ee4-103">My team mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="89ee4-104">Dieses Thema enthält Informationen zum mobilen Arbeitsbereich **Mein Team**.</span><span class="sxs-lookup"><span data-stu-id="89ee4-104">This topic provides information about the **My team** mobile workspace.</span></span> <span data-ttu-id="89ee4-105">Mit dem Arbeitsbereich können Manager ihre eigenen Mitarbeiter und erweitertes Personal anzeigen.</span><span class="sxs-lookup"><span data-stu-id="89ee4-105">This workspace lets managers view their direct reports and extended staff.</span></span> <span data-ttu-id="89ee4-106">Sie können auch Lob an Personen innerhalb der Mitarbeitergruppe senden.</span><span class="sxs-lookup"><span data-stu-id="89ee4-106">They can also send praise to individuals in their reporting chain.</span></span>

<span data-ttu-id="89ee4-107">Dieser mobile Arbeitsbereich soll mit der Finance and Operations Mobile-App verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="89ee4-107">This mobile workspace is intended to be used with the Finance and Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="89ee4-108">Übersicht</span><span class="sxs-lookup"><span data-stu-id="89ee4-108">Overview</span></span> 
<span data-ttu-id="89ee4-109">Der mobile Arbeitsbereich **Mein Team** ermöglicht Managern, folgende Aufgaben auszuführen:</span><span class="sxs-lookup"><span data-stu-id="89ee4-109">The **My team** mobile workspace lets managers perform these tasks:</span></span>

- <span data-ttu-id="89ee4-110">Liste der eigenen Mitarbeiter des Managers anzeigen.</span><span class="sxs-lookup"><span data-stu-id="89ee4-110">View a list of the manager’s direct reports.</span></span>
- <span data-ttu-id="89ee4-111">Liste des erweiterten Mitarbeiterstamm des Managers anzeigen.</span><span class="sxs-lookup"><span data-stu-id="89ee4-111">View a list of the manager’s extended reporting team.</span></span>
- <span data-ttu-id="89ee4-112">Anzeigen von detaillierten Informationen zu einzelnen Teammitgliedern wie Geburtsdatum, Dienstalter, Dienstjahre sowie Informationen zu Vergütung und Leistung.</span><span class="sxs-lookup"><span data-stu-id="89ee4-112">View detailed information for each team member, such as birth date, seniority date, years of service, and compensation and performance information.</span></span>
- <span data-ttu-id="89ee4-113">Senden von Lob an einzelne Personen aus dem erweiterten Mitarbeiterteam des Managers.</span><span class="sxs-lookup"><span data-stu-id="89ee4-113">Send praise to any individual in the manager’s extended reporting team.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="89ee4-114">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="89ee4-114">Prerequisites</span></span>
<span data-ttu-id="89ee4-115">Bevor Sie diesen mobilen Arbeitsbereich verwenden können, müssen die folgenden Voraussetzungen erfüllt werden.</span><span class="sxs-lookup"><span data-stu-id="89ee4-115">Before you can use this mobile workspace, the following prerequisites must be met.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="89ee4-116">Voraussetzung</span><span class="sxs-lookup"><span data-stu-id="89ee4-116">Prerequisite</span></span></th>
<th><span data-ttu-id="89ee4-117">Rolle</span><span class="sxs-lookup"><span data-stu-id="89ee4-117">Role</span></span></th>
<th><span data-ttu-id="89ee4-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="89ee4-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="89ee4-119">Eines der folgenden Produkte muss in der Organisation bereitgestellt werden:</span><span class="sxs-lookup"><span data-stu-id="89ee4-119">One of the following products must be deployed in your organization:</span></span>
<ul><li><span data-ttu-id="89ee4-120">Eine Finance and Operations App</span><span class="sxs-lookup"><span data-stu-id="89ee4-120">A Finance and Operations app</span></span></li>
<li><span data-ttu-id="89ee4-121">Microsoft Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="89ee4-121">Microsoft Dynamics 365 Human Resources</span></span></li>
</ul>
</td>
<td><span data-ttu-id="89ee4-122">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="89ee4-122">System administrator</span></span></td>
<td><span data-ttu-id="89ee4-123">Wenn keine Finance and Operations-App in der Organisation bereitgestellt wurde, finden Sie Informationen unter <a href="../deployment/deploy-demo-environment.md">Eine Demoumgebung bereitstellen</a>.</span><span class="sxs-lookup"><span data-stu-id="89ee4-123">If you don&#39;t already have a Finance and Operations app deployed in your organization, see <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span> <span data-ttu-id="89ee4-124">Wenn Personal nicht bereits in der Organisation bereitgestellt wurde, kann der Systemadministrator von der <a href="https://dynamics.microsoft.com/human-resources/overview/">Personal-Webseite</a> auf eine Testversion zugreifen.</span><span class="sxs-lookup"><span data-stu-id="89ee4-124">If you don&#39;t already have Human Resources deployed in your organization, the system administrator can access a trial version from the <a href="https://dynamics.microsoft.com/human-resources/overview/">Human Resources webpage</a>.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="89ee4-125">Der mobile Arbeitsbereich <strong>Mein Team</strong> muss veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="89ee4-125">The <strong>My team</strong> mobile workspace must be published.</span></span></td>
<td><span data-ttu-id="89ee4-126">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="89ee4-126">System administrator</span></span></td>
<td><span data-ttu-id="89ee4-127">Siehe <a href="publish-mobile-workspace.md">Einen mobilen Arbeitsbereich veröffentlichen</a>.</span><span class="sxs-lookup"><span data-stu-id="89ee4-127">See <a href="publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="89ee4-128">Herunterladen und Installieren der mobilen App</span><span class="sxs-lookup"><span data-stu-id="89ee4-128">Download and install the mobile app</span></span>

<span data-ttu-id="89ee4-129">Herunterladen und Installieren der Finance and Operations mobilen App:</span><span class="sxs-lookup"><span data-stu-id="89ee4-129">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="89ee4-130">Für Android-Smartphones</span><span class="sxs-lookup"><span data-stu-id="89ee4-130">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="89ee4-131">Für iPhones</span><span class="sxs-lookup"><span data-stu-id="89ee4-131">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="89ee4-132">Bei der mobile App anmelden</span><span class="sxs-lookup"><span data-stu-id="89ee4-132">Sign in to the mobile app</span></span>
1.  <span data-ttu-id="89ee4-133">Starten Sie die App auf Ihrem mobilen Gerät.</span><span class="sxs-lookup"><span data-stu-id="89ee4-133">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="89ee4-134">Geben Sie die Microsoft Dynamics 365-URL ein.</span><span class="sxs-lookup"><span data-stu-id="89ee4-134">Enter your Microsoft Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="89ee4-135">Bei der erstmaligen Anwendung werden Sie nach Ihrem Benutzernamen und dem Kennwort gefragt.</span><span class="sxs-lookup"><span data-stu-id="89ee4-135">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="89ee4-136">Geben Sie Ihre Anmeldeinformationen ein.</span><span class="sxs-lookup"><span data-stu-id="89ee4-136">Enter your credentials.</span></span>
4.  <span data-ttu-id="89ee4-137">Nachdem Sie sich angemeldet haben, werden verfügbare Arbeitsbereiche für Ihr Unternehmen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="89ee4-137">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="89ee4-138">Beachten Sie, dass Sie, wenn Ihr Systemadministrator einen neuen Arbeitsbereich später veröffentlicht, die Liste der mobilen Arbeitsbereiche aktualisieren müssen.</span><span class="sxs-lookup"><span data-stu-id="89ee4-138">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="89ee4-139">[![Zum Aktualisieren ziehen](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="89ee4-139">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="view-team-members-by-using-the-my-team-mobile-workspace"></a><span data-ttu-id="89ee4-140">Anzeigen von Teammitglieder mit dem Mein Team-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="89ee4-140">View team members by using the My team mobile workspace</span></span>
1.  <span data-ttu-id="89ee4-141">Wählen Sie in der mobilen App den Arbeitsbereich **Mein Team** aus.</span><span class="sxs-lookup"><span data-stu-id="89ee4-141">In the mobile app, select the **My team** workspace.</span></span> <span data-ttu-id="89ee4-142">Eine Liste von Teammitgliedern wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="89ee4-142">A list of team members is shown.</span></span> <span data-ttu-id="89ee4-143">Die Liste enthält auch die Titel jedes Teammitglieds sowie alle eigenen Mitarbeiter.</span><span class="sxs-lookup"><span data-stu-id="89ee4-143">The list also shows each team member's title, and any direct reports that the member has.</span></span>
2.  <span data-ttu-id="89ee4-144">Wählen Sie ein Teammitglied aus.</span><span class="sxs-lookup"><span data-stu-id="89ee4-144">Select a team member.</span></span> <span data-ttu-id="89ee4-145">Die Seite **Teammitgliedszusammenfassung** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="89ee4-145">The **Team member summary** page appears.</span></span> <span data-ttu-id="89ee4-146">Die Informationen auf dieser Seite enthalten das Geburtsdatum des Teammitglieds, das Dienstalter, die Dienstjahre, die Jahre in der aktuellen Position sowie Informationen zur Vergütung.</span><span class="sxs-lookup"><span data-stu-id="89ee4-146">The information on this page includes the team member's birth date, seniority date, years of service, years in the current position, and compensation information.</span></span>

## <a name="view-extended-team-members-by-using-the-my-team-mobile-workspace"></a><span data-ttu-id="89ee4-147">Anzeigen von erweiterten Teammitgliedern mit dem Mein Team-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="89ee4-147">View extended team members by using the My team mobile workspace</span></span>
1.  <span data-ttu-id="89ee4-148">Wählen Sie in der mobilen App den Arbeitsbereich **Mein Team** aus.</span><span class="sxs-lookup"><span data-stu-id="89ee4-148">In the mobile app, select the **My team** workspace.</span></span> <span data-ttu-id="89ee4-149">Eine Liste von Teammitgliedern wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="89ee4-149">A list of team members is shown.</span></span> <span data-ttu-id="89ee4-150">Die Liste enthält auch die Titel jedes Teammitglieds sowie alle eigenen Mitarbeiter.</span><span class="sxs-lookup"><span data-stu-id="89ee4-150">The list also shows each team member's title, and any direct reports that the member has.</span></span>
1.  <span data-ttu-id="89ee4-151">Wählen Sie den Link **Eigene Mitarbeiter** aus.</span><span class="sxs-lookup"><span data-stu-id="89ee4-151">Select the **Direct reports** link.</span></span> <span data-ttu-id="89ee4-152">Eine Liste des erweiterten Teams wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="89ee4-152">A list of your extended team is shown.</span></span>
1.  <span data-ttu-id="89ee4-153">Wählen Sie ein Teammitglied aus.</span><span class="sxs-lookup"><span data-stu-id="89ee4-153">Select a team member.</span></span> <span data-ttu-id="89ee4-154">Die Seite **Teammitgliedszusammenfassung** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="89ee4-154">The **Team member summary** page appears.</span></span> <span data-ttu-id="89ee4-155">Die Informationen auf dieser Seite enthalten das Geburtsdatum des Teammitglieds, das Dienstalter, die Dienstjahre, die Jahre in der aktuellen Position sowie Informationen zur Vergütung.</span><span class="sxs-lookup"><span data-stu-id="89ee4-155">The information on this page includes the team member's birth date, seniority date, years of service, years in the current position, and compensation information.</span></span>

## <a name="send-praise-about-team-members-by-using-the-my-team-mobile-workspace"></a><span data-ttu-id="89ee4-156">Senden von Lob an Teammitgliedern mit dem Mein Team-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="89ee4-156">Send praise about team members by using the My team mobile workspace</span></span>
1.  <span data-ttu-id="89ee4-157">Wählen Sie in der mobilen App den Arbeitsbereich **Mein Team** aus.</span><span class="sxs-lookup"><span data-stu-id="89ee4-157">In the mobile app, select the **My team** workspace.</span></span> <span data-ttu-id="89ee4-158">Eine Liste von Teammitgliedern wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="89ee4-158">A list of team members is shown.</span></span> <span data-ttu-id="89ee4-159">Die Liste enthält auch die Titel jedes Teammitglieds sowie alle eigenen Mitarbeiter.</span><span class="sxs-lookup"><span data-stu-id="89ee4-159">The list also shows each team member's title, and any direct reports that the member has.</span></span>
1.  <span data-ttu-id="89ee4-160">Wählen Sie ein Teammitglied aus.</span><span class="sxs-lookup"><span data-stu-id="89ee4-160">Select a team member.</span></span> <span data-ttu-id="89ee4-161">Die Seite **Teammitgliedszusammenfassung** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="89ee4-161">The **Team member summary** page appears.</span></span>
1.  <span data-ttu-id="89ee4-162">Wählen Sie **Lob versenden**.</span><span class="sxs-lookup"><span data-stu-id="89ee4-162">Select **Send praise**.</span></span> 
1. <span data-ttu-id="89ee4-163">Geben Sie den Text des Lobs ein, das Sie übermitteln möchten.</span><span class="sxs-lookup"><span data-stu-id="89ee4-163">Enter the text of the praise that you want to send.</span></span> 
1. <span data-ttu-id="89ee4-164">Wählen Sie **Fertig**.</span><span class="sxs-lookup"><span data-stu-id="89ee4-164">Select **Done**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]