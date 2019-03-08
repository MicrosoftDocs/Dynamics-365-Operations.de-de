---
title: Unternehmensverzeichnis für mobilen Arbeitsbereich
description: Dieses Thema enthält Informationen über den mobilen Arbeitsbereich "Unternehmensverzeichnis", mit dem Benutzer andere Mitarbeiter in ihrer Organisation anzeigen und Kontakt mit ihnen aufnehmen können.
author: jcart1106
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 527d40452bcf52875e3f7b04d328110147417072
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "308620"
---
# <a name="company-directory-mobile-workspace"></a><span data-ttu-id="58a75-103">Unternehmensverzeichnis für mobilen Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="58a75-103">Company directory mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="58a75-104">Dieses Thema enthält Informationen zum **Unternehmensverzeichnis** im mobilen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="58a75-104">This topic provides information about the **Company directory** mobile workspace.</span></span> <span data-ttu-id="58a75-105">Dieser Arbeitsbereich ermöglicht Benutzern das Anzeigen von Kontakten und Mitarbeitern in der Organisation.</span><span class="sxs-lookup"><span data-stu-id="58a75-105">This workspace lets users view and contact other employees in their organization.</span></span>

<span data-ttu-id="58a75-106">Dieser mobile Arbeitsbereich kann mit der Microsoft Dynamics 365 for Unified Operations Mobile-App verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="58a75-106">This mobile workspace can be used with the Microsoft Dynamics 365 for Unified Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="58a75-107">Übersicht</span><span class="sxs-lookup"><span data-stu-id="58a75-107">Overview</span></span>
<span data-ttu-id="58a75-108">Der mobile Arbeitsbereich **Unternehmensverzeichnis** ermöglicht Benutzern, folgende Aufgaben auszuführen:</span><span class="sxs-lookup"><span data-stu-id="58a75-108">The **Company directory** mobile workspace lets users perform these tasks:</span></span>

- <span data-ttu-id="58a75-109">Zeigen Sie eine Liste der Mitarbeiter in der Organisation an.</span><span class="sxs-lookup"><span data-stu-id="58a75-109">View a list of employees in the organization.</span></span>
- <span data-ttu-id="58a75-110">Suchen Sie nach Mitarbeitern in der Organisation.</span><span class="sxs-lookup"><span data-stu-id="58a75-110">Search for employees in the organization.</span></span>
- <span data-ttu-id="58a75-111">Zeigen Sie Kontaktinformationen für Mitarbeiter an.</span><span class="sxs-lookup"><span data-stu-id="58a75-111">View contact information for employees.</span></span>
- <span data-ttu-id="58a75-112">Kontaktieren Sie Mitarbeiter aus den Profilinformationen heraus.</span><span class="sxs-lookup"><span data-stu-id="58a75-112">Contact employees from the profile information.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="58a75-113">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="58a75-113">Prerequisites</span></span>
<span data-ttu-id="58a75-114">Bevor Sie diesen mobilen Arbeitsbereich verwenden können, müssen die folgenden Voraussetzungen erfüllt werden.</span><span class="sxs-lookup"><span data-stu-id="58a75-114">Before you can use this mobile workspace, the following prerequisites must be met.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="58a75-115">Voraussetzung</span><span class="sxs-lookup"><span data-stu-id="58a75-115">Prerequisite</span></span></th>
<th><span data-ttu-id="58a75-116">Rolle</span><span class="sxs-lookup"><span data-stu-id="58a75-116">Role</span></span></th>
<th><span data-ttu-id="58a75-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="58a75-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="58a75-118">Eines der folgenden Produkte muss in der Organisation bereitgestellt werden:</span><span class="sxs-lookup"><span data-stu-id="58a75-118">One of the following products must be deployed in your organization:</span></span>
<ul><li><span data-ttu-id="58a75-119">Microsoft Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="58a75-119">Microsoft Dynamics 365 for Finance and Operations</span></span></li>
<li><span data-ttu-id="58a75-120">Microsoft Dynamics 365 for Talent</span><span class="sxs-lookup"><span data-stu-id="58a75-120">Microsoft Dynamics 365 for Talent</span></span></li>
</ul>
</td>
<td><span data-ttu-id="58a75-121">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="58a75-121">System administrator</span></span></td>
<td><span data-ttu-id="58a75-122">Wenn Finance and Operations nicht bereits in der Organisation bereitgestellt wurde, finden Sie Informationen unter <a href="../deployment/deploy-demo-environment.md">Eine Demoumgebung bereitstellen</a>.</span><span class="sxs-lookup"><span data-stu-id="58a75-122">If you don&#39;t already have Finance and Operations deployed in your organization, see <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span> <span data-ttu-id="58a75-123">Wenn Talent nicht bereits in der Organisation bereitgestellt wurde, kann der Systemadministrator von der <a href="https://www.microsoft.com/en-us/dynamics365/talent">Talent-Webseite</a> auf eine Testversion zugreifen.</span><span class="sxs-lookup"><span data-stu-id="58a75-123">If you don&#39;t already have Talent deployed in your organization, the system administrator can access a trial version from the <a href="https://www.microsoft.com/en-us/dynamics365/talent">Talent webpage</a>.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="58a75-124">Der mobile Arbeitsbereich <strong>Unternehmensverzeichnis</strong> muss bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="58a75-124">The <strong>Company directory</strong> mobile workspace must be published.</span></span></td>
<td><span data-ttu-id="58a75-125">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="58a75-125">System administrator</span></span></td>
<td><span data-ttu-id="58a75-126">Siehe <a href="publish-mobile-workspace.md">Einen mobilen Arbeitsbereich veröffentlichen</a>.</span><span class="sxs-lookup"><span data-stu-id="58a75-126">See <a href="publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="58a75-127">Herunterladen und Installieren der mobilen App</span><span class="sxs-lookup"><span data-stu-id="58a75-127">Download and install the mobile app</span></span>
<span data-ttu-id="58a75-128">Laden Sie die mobile App für Dynamics 365 for Unified Operations herunter und installieren Sie diese:</span><span class="sxs-lookup"><span data-stu-id="58a75-128">Download and install the Dynamics 365 for Unified Operations mobile app:</span></span>

-   [<span data-ttu-id="58a75-129">Für Android-Smartphones</span><span class="sxs-lookup"><span data-stu-id="58a75-129">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="58a75-130">Für iPhones</span><span class="sxs-lookup"><span data-stu-id="58a75-130">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="58a75-131">Bei der mobile App anmelden</span><span class="sxs-lookup"><span data-stu-id="58a75-131">Sign in to the mobile app</span></span>
1.  <span data-ttu-id="58a75-132">Starten Sie die App auf Ihrem mobilen Gerät.</span><span class="sxs-lookup"><span data-stu-id="58a75-132">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="58a75-133">Geben Sie die Microsoft Dynamics 365-URL ein.</span><span class="sxs-lookup"><span data-stu-id="58a75-133">Enter your Microsoft Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="58a75-134">Bei der erstmaligen Anwendung werden Sie nach Ihrem Benutzernamen und dem Kennwort gefragt.</span><span class="sxs-lookup"><span data-stu-id="58a75-134">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="58a75-135">Geben Sie Ihre Anmeldeinformationen ein.</span><span class="sxs-lookup"><span data-stu-id="58a75-135">Enter your credentials.</span></span>
4.  <span data-ttu-id="58a75-136">Nachdem Sie sich angemeldet haben, werden verfügbare Arbeitsbereiche für Ihr Unternehmen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="58a75-136">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="58a75-137">Beachten Sie, dass Sie, wenn Ihr Systemadministrator einen neuen Arbeitsbereich später veröffentlicht, die Liste der mobilen Arbeitsbereiche aktualisieren müssen.</span><span class="sxs-lookup"><span data-stu-id="58a75-137">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="58a75-138">[![Zum Aktualisieren ziehen](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="58a75-138">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="view-the-company-directory-by-using-the-mobile-workspace"></a><span data-ttu-id="58a75-139">Anzeigen des Unternehmensverzeichnisses mithilfe des mobilen Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="58a75-139">View the company directory by using the mobile workspace</span></span>
1.  <span data-ttu-id="58a75-140">Wählen Sie in der mobilen App den Arbeitsbereich **Unternehmensverzeichnis** aus.</span><span class="sxs-lookup"><span data-stu-id="58a75-140">In the mobile app, select the **Company directory** workspace.</span></span> <span data-ttu-id="58a75-141">Eine Liste von Mitgliedern wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="58a75-141">A list of employees is shown.</span></span>
3.  <span data-ttu-id="58a75-142">Wählen Sie einen Mitarbeiter aus.</span><span class="sxs-lookup"><span data-stu-id="58a75-142">Select an employee.</span></span> <span data-ttu-id="58a75-143">Die Seite **Mitarbeiterprofil** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="58a75-143">The **Employee profile** page appears.</span></span> <span data-ttu-id="58a75-144">Die Informationen auf dieser Seite umfassen den Vornamen, Nachnamen, Titel und die Abteilung des Mitarbeiters.</span><span class="sxs-lookup"><span data-stu-id="58a75-144">The information on this page includes the employee's first name, last name, title, and department.</span></span>

## <a name="search-the-company-directory-by-using-the-mobile-workspace"></a><span data-ttu-id="58a75-145">Suchen des Unternehmensverzeichnisses mithilfe des mobilen Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="58a75-145">Search the company directory by using the mobile workspace</span></span>
1.  <span data-ttu-id="58a75-146">Wählen Sie in der mobilen App den Arbeitsbereich **Unternehmensverzeichnis** aus.</span><span class="sxs-lookup"><span data-stu-id="58a75-146">In the mobile app, select the **Company directory** workspace.</span></span>
2.  <span data-ttu-id="58a75-147">Geben Sie im Feld **Suchen** den Vornamen, den Nachnamen, den Titel oder die Abteilung des Mitarbeiters ein, um die Suche zu starten.</span><span class="sxs-lookup"><span data-stu-id="58a75-147">In the **Search** field, enter an employee's first name, last name, title, or department to start the search.</span></span>
3.  <span data-ttu-id="58a75-148">Wählen Sie einen Mitarbeiter aus.</span><span class="sxs-lookup"><span data-stu-id="58a75-148">Select an employee.</span></span> <span data-ttu-id="58a75-149">Die Seite **Mitarbeiterprofil** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="58a75-149">The **Employee profile** page appears.</span></span> <span data-ttu-id="58a75-150">Die Informationen auf dieser Seite umfassen den Vornamen, Nachnamen, Titel und die Abteilung des Mitarbeiters.</span><span class="sxs-lookup"><span data-stu-id="58a75-150">The information on this page includes the employee's first name, last name, title, and department.</span></span>
