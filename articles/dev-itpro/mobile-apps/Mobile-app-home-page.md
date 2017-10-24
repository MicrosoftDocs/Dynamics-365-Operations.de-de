---
title: Mobile App-Startseite
description: In diesem Thema wird die mobile Microsoft Dynamics 365 for Unified Operations-App beschrieben. Zudem werden Links zu Ressourcen bereitgestellt, die bei der Implementierung in der Organisation helfen.
author: sericks007
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, UnifiedOperations, Platform
ms.custom: 272853
ms.assetid: c99f818f-27b3-4e45-92b4-74272dad0e17
ms.search.region: Global
ms.author: sericks
ms.dyn365.ops.intro: Platform update 4
ms.search.validFrom: 2017-02-28
ms.translationtype: HT
ms.sourcegitcommit: c73eeaaf28df8db720431d4bcd317c9721baa99d
ms.openlocfilehash: 08dcdf2f5c03de17d50910e617d20e734e6ee31e
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="mobile-app-home-page"></a><span data-ttu-id="c77e3-103">Mobile App-Startseite</span><span class="sxs-lookup"><span data-stu-id="c77e3-103">Mobile app home page</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c77e3-104">In diesem Thema wird die mobile Microsoft Dynamics 365 for Unified Operations-App beschrieben. Zudem werden Links zu Ressourcen bereitgestellt, die bei der Implementierung in der Organisation helfen.</span><span class="sxs-lookup"><span data-stu-id="c77e3-104">This topic describes the Microsoft Dynamics 365 for Unified Operations mobile app and provides links to resources that can help you implement it in your organization.</span></span>

> [!NOTE]
> <span data-ttu-id="c77e3-105">Die mobile App wurde zuvor als *Microsoft Dynamics 365 for Finance and Operations* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="c77e3-105">The mobile app was previously named *Microsoft Dynamics 365 for Finance and Operations*.</span></span>

<a name="overview"></a><span data-ttu-id="c77e3-106">Überblick</span><span class="sxs-lookup"><span data-stu-id="c77e3-106">Overview</span></span>
--------

<span data-ttu-id="c77e3-107">Die mobile App ermöglicht es Ihrer Organisation, Geschäftsprozesse auf mobilen Geräten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="c77e3-107">The mobile app enables your organization to make its business processes available on mobile devices.</span></span> <span data-ttu-id="c77e3-108">Nachdem Ihr IT-Administrator den mobilen Arbeitsbereich für Ihre Organisation bereitgestellt hat, können sich Benutzer bei der App anmelden und sofort damit beginnen, Geschäftsprozesse über ihre mobilen Geräte auszuführen.</span><span class="sxs-lookup"><span data-stu-id="c77e3-108">After your IT admin enables the mobile workspaces for your organization, users can sign in to the app and immediately begin to run business processes from their mobile devices.</span></span> <span data-ttu-id="c77e3-109">Die mobile App umfasst folgende Funktionen, die helfen, die Produktivität zu steigern:</span><span class="sxs-lookup"><span data-stu-id="c77e3-109">The mobile app includes the following features that can help increase productivity:</span></span>

- <span data-ttu-id="c77e3-110">Benutzer können Geschäftsdaten anzeigen, bearbeiten und ausführen, selbst wenn die Netzwerkverbindung unterbrochen ist oder ihre mobilen Geräte vollständig offline sind.</span><span class="sxs-lookup"><span data-stu-id="c77e3-110">Users can view, edit, and act on business data, even if they have intermittent network connectivity or their mobile devices are completely offline.</span></span> <span data-ttu-id="c77e3-111">Wenn ein Gerät eine Netzwerkverbindung erneut einrichtet, werden Offline-Datenoperationen automatisch mit Dynamics 365 for Finance and Operations, Enterprise edition oder Microsoft Dynamics 365 for Finance and Operations synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="c77e3-111">When a device reestablishes a network connection, offline data operations are automatically synchronized with Dynamics 365 for Finance and Operations, Enterprise edition, or Microsoft Dynamics 365 for Finance and Operations.</span></span>
- <span data-ttu-id="c77e3-112">IT-Administratoren oder Entwickler können mobile Arbeitsbereiche erstellen und veröffentlichen, die auf die Organisation zugeschnitten wurden.</span><span class="sxs-lookup"><span data-stu-id="c77e3-112">IT admins or developers can build and publish mobile workspaces that have been tailored to their organization.</span></span> <span data-ttu-id="c77e3-113">Die App verwendet die vorhandenen Codeanlagen.</span><span class="sxs-lookup"><span data-stu-id="c77e3-113">The app uses your existing code assets.</span></span> <span data-ttu-id="c77e3-114">Daher müssen Sie den Validierungsprozess, Geschäftslogik oder Sicherheitskonfiguration nicht erneut implementieren.</span><span class="sxs-lookup"><span data-stu-id="c77e3-114">Therefore, you don't have to re-implement your validation procedures, business logic, or security configuration.</span></span>
- <span data-ttu-id="c77e3-115">IT-Administratoren oder -Entwickler können ganz einfach mobile Arbeitsbereiche entwerfen, indem sie den Arbeitsbereichdesigner zum Anzeigen und Klicken verwenden, der im Webclient enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="c77e3-115">IT admins or developers can easily design mobile workspaces by using the point-and-click workspace designer that is included with the web client.</span></span>
- <span data-ttu-id="c77e3-116">IT-Administratoren oder Entwickler können die Offline-Funktionalität von Arbeitsbereichen optional optimieren, indem das Geschäftslogikerweiterbarkeitsframework verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c77e3-116">IT admins or developers can optionally optimize the offline capabilities of workspaces by using the Business logic extensibility framework.</span></span> <span data-ttu-id="c77e3-117">Da Daten weiter verarbeitet werden, wenn ein Gerät offline ist, bleiben die mobilen Szenarien erhalten. auch wenn die Geräte keine permanente Netzwerkkonnektivität haben.</span><span class="sxs-lookup"><span data-stu-id="c77e3-117">Because data continues to be processed while a device is offline, your mobile scenarios remain rich and fluid, even if devices don't have constant network connectivity.</span></span>

## <a name="elements-of-the-mobile-app"></a><span data-ttu-id="c77e3-118">Elemente der mobilen App</span><span class="sxs-lookup"><span data-stu-id="c77e3-118">Elements of the mobile app</span></span>
<span data-ttu-id="c77e3-119">Die Navigation in der mobilen App besteht aus vier grundlegenden Konzepten: Dashboard, Arbeitsbereiche, Seiten und Aktivitäten.</span><span class="sxs-lookup"><span data-stu-id="c77e3-119">Navigation in the mobile app consists of four basic concepts: the dashboard, workspaces, pages, and actions.</span></span> 

<span data-ttu-id="c77e3-120">[![Navigationskonzepte in der mobilen App](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)</span><span class="sxs-lookup"><span data-stu-id="c77e3-120">[![Navigation concepts in the mobile app](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)</span></span>

1. <span data-ttu-id="c77e3-121">Wenn Sie die App starten, gehen Sie zu **Dashboard**.</span><span class="sxs-lookup"><span data-stu-id="c77e3-121">When you start the app, you go to the **dashboard**.</span></span>
2. <span data-ttu-id="c77e3-122">Auf dem Dashboard wird eine Liste der veröffentlichten **Arbeitsbereiche** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c77e3-122">On the dashboard, you can see a list of **workspaces** that have been published.</span></span>
3. <span data-ttu-id="c77e3-123">In jedem Arbeitsbereich können Sie eine Liste der **Seiten** finden, die für diesen Arbeitsbereich verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="c77e3-123">In each workspace, you can see a list of **pages** that are available for that workspace.</span></span>
4. <span data-ttu-id="c77e3-124">Nachdem Sie auf einer Seite sind, können Sie eine Reihe von Aktivitäten ausführen.</span><span class="sxs-lookup"><span data-stu-id="c77e3-124">After you're on a page, you can perform several actions.</span></span> <span data-ttu-id="c77e3-125">Nachfolgend finden Sie einige Beispiele:</span><span class="sxs-lookup"><span data-stu-id="c77e3-125">Here are some examples:</span></span>

    - <span data-ttu-id="c77e3-126">Zeigen Sie detaillierte Daten an.</span><span class="sxs-lookup"><span data-stu-id="c77e3-126">View detailed data.</span></span>
    - <span data-ttu-id="c77e3-127">Navigieren Sie zu anderen Seiten mit zugehörige Daten wie Entitätsdetails oder Positionen.</span><span class="sxs-lookup"><span data-stu-id="c77e3-127">Navigate to other pages for related data, such as entity details or lines.</span></span>
    - <span data-ttu-id="c77e3-128">Zeigen Sie eine Liste mit **Aktivitäten** an, die für die Seite verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="c77e3-128">See a list of **actions** that are available for that page.</span></span> <span data-ttu-id="c77e3-129">Mit Aktivitäten können Sie vorhandenen Daten erstellen oder bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="c77e3-129">Actions let you create or edit existing data.</span></span>

## <a name="implementation-process"></a><span data-ttu-id="c77e3-130">Implementierungsprozess</span><span class="sxs-lookup"><span data-stu-id="c77e3-130">Implementation process</span></span>
<span data-ttu-id="c77e3-131">Die folgende Abbildung veranschaulicht den Prozess des Implementierens beider mobiler Arbeitsbereiche, die von Microsoft und benutzerdefinierten mobilen Arbeitsbereichen bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c77e3-131">The following illustration shows the process for implementing both mobile workspaces that are provided by Microsoft and custom mobile workspaces.</span></span> 

![Implementierungsprozess für mobile Apps](./media/Mobile-implementation-process-5.png)

<span data-ttu-id="c77e3-133">Die folgende Tabelle enthält Links zu Ressourcen, die Ihnen beim Implementieren beider mobilen Arbeitsbereiche helfen, die von Microsoft und benutzerdefinierten mobilen Arbeitsbereichen bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c77e3-133">The following table includes links to resources that can help you implement both mobile workspaces that are provided by Microsoft and custom mobile workspaces.</span></span> <span data-ttu-id="c77e3-134">Die Nummern in der ersten Spalte entsprechen den nummerierten Schritten in der vorherigen Abbildung.</span><span class="sxs-lookup"><span data-stu-id="c77e3-134">The numbers in the first column correspond to the numbered steps in the previous illustration.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c77e3-135">Schritt</span><span class="sxs-lookup"><span data-stu-id="c77e3-135">Step</span></span></th>
<th><span data-ttu-id="c77e3-136">Rolle</span><span class="sxs-lookup"><span data-stu-id="c77e3-136">Role</span></span></th>
<th><span data-ttu-id="c77e3-137">Vorgang</span><span class="sxs-lookup"><span data-stu-id="c77e3-137">Action</span></span></th>
<th><span data-ttu-id="c77e3-138">Ressourcen, die Ihnen beim Erfüllen der Aktivität helfen</span><span class="sxs-lookup"><span data-stu-id="c77e3-138">Resources to help you complete the action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c77e3-139">1</span><span class="sxs-lookup"><span data-stu-id="c77e3-139">1</span></span></td>
<td><span data-ttu-id="c77e3-140">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="c77e3-140">System administrator</span></span></td>
<td><span data-ttu-id="c77e3-141">Implementieren Sie Finance and Operations in Ihre Organisation.</span><span class="sxs-lookup"><span data-stu-id="c77e3-141">Implement Finance and Operations or Finance and Operations in your organization.</span></span></td>
<td><ul><li><span data-ttu-id="c77e3-142">Wenn Sie noch keine Version von Microsoft Dynamics 365 bereitgestellt haben, siehe <a href="../deployment/deploy-demo-environment.md">Erstellen einer Demoumgebung</a>.</span><span class="sxs-lookup"><span data-stu-id="c77e3-142">If you haven't yet deployed a version of Microsoft Dynamics 365, see <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span></li><li><span data-ttu-id="c77e3-143">Um eine Liste mobiler Arbeitsbereiche anzuzeigen, die verwendet werden können, siehe <a href="mobile-workspaces-released.md">Vor Kurzem freigegebene mobile Arbeitsbereiche</a>.</span><span class="sxs-lookup"><span data-stu-id="c77e3-143">To see a list of mobile workspaces that can be used, see <a href="mobile-workspaces-released.md">Mobile workspaces recently released</a>.</span></span></li></ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c77e3-144">2</span><span class="sxs-lookup"><span data-stu-id="c77e3-144">2</span></span></td>
<td><span data-ttu-id="c77e3-145">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="c77e3-145">System administrator</span></span></td>
<td><span data-ttu-id="c77e3-146"><strong>Wenn Sie Microsoft Dynamics 365 for Finance and Operations, Version 1611, verwenden:</strong> Laden und installieren Sie KBs, die die von Microsoft bereitgestellten mobilen Arbeitsbereiche aktivieren.</span><span class="sxs-lookup"><span data-stu-id="c77e3-146"><strong>If you're using Microsoft Dynamics 365 for Finance and Operations version 1611:</strong> Download and install KBs that enable the mobile workspaces that are provided by Microsoft.</span></span></td>
<td><span data-ttu-id="c77e3-147">Weitere Informationen finden Sie in folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="c77e3-147">See the following topics for more information:</span></span>
<ul>

<li><span data-ttu-id="c77e3-148"><a href="../../financials/cost-accounting/cost-controlling-mobile-workspace.md">Mobiler Arbeitsbereich für die Kostensteuerung</a></span><span class="sxs-lookup"><span data-stu-id="c77e3-148"><a href="../../financials/cost-accounting/cost-controlling-mobile-workspace.md">Cost controlling mobile workspaces</a></span></span></li>
<li><span data-ttu-id="c77e3-149"><a href="../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">Mobiler Arbeitsbereich für Lagerbestand</a></span><span class="sxs-lookup"><span data-stu-id="c77e3-149"><a href="../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">Inventory on-hand mobile workspace</a></span></span></li>
<li><span data-ttu-id="c77e3-150"><a href="../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">Aufträge, mobiler Arbeitsbereich</a></span><span class="sxs-lookup"><span data-stu-id="c77e3-150"><a href="../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">Sales orders mobile workspaces</a></span></span></li>
<li><span data-ttu-id="c77e3-151"><a href="../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">Mobiler Arbeitsbereich für Kreditorenzusammenarbeit</a></span><span class="sxs-lookup"><span data-stu-id="c77e3-151"><a href="../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">Vendor collaboration mobile workspace</a></span></span></li>
<li><span data-ttu-id="c77e3-152"><a href="../../financials/project-management/project-time-entry-mobile-workspace.md">Mobiler Arbeitsbereich für Projektzeiterfassung</a></span><span class="sxs-lookup"><span data-stu-id="c77e3-152"><a href="../../financials/project-management/project-time-entry-mobile-workspace.md">Project time entry mobile workspace</a></span></span></li>
<li><span data-ttu-id="c77e3-153"><a href="../../financials/expense-management/expense-management-mobile-workspace.md">Mobiler Arbeitsbereich für Spesenverwaltung</a></span><span class="sxs-lookup"><span data-stu-id="c77e3-153"><a href="../../financials/expense-management/expense-management-mobile-workspace.md">Expense management mobile workspace</a></span></span></li>

</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c77e3-154">3</span><span class="sxs-lookup"><span data-stu-id="c77e3-154">3</span></span></td>
<td><span data-ttu-id="c77e3-155">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="c77e3-155">System administrator</span></span></td>
<td><span data-ttu-id="c77e3-156">Veröffentlichen Sie die mobilen Arbeitsbereiche, die von Microsoft zur Verfügung gestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c77e3-156">Publish the mobile workspaces that are provided by Microsoft.</span></span></td>
<td><span data-ttu-id="c77e3-157"><a href="publish-mobile-workspace.md">Mobilen Arbeitsbereich veröffentlichen</a>
</span><span class="sxs-lookup"><span data-stu-id="c77e3-157"><a href="publish-mobile-workspace.md">Publish a mobile workspace</a>
</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c77e3-158">4</span><span class="sxs-lookup"><span data-stu-id="c77e3-158">4</span></span></td>
<td><span data-ttu-id="c77e3-159">Entwickler oder unabhängiger Softwarehersteller (ISV)</span><span class="sxs-lookup"><span data-stu-id="c77e3-159">Developer or independent software vendor (ISV)</span></span></td>
<td><span data-ttu-id="c77e3-160">Nutzen Sie die mobile Plattform, um benutzerdefinierte mobile Arbeitsbereiche zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c77e3-160">Use the mobile platform to create custom mobile workspaces.</span></span></td>
<td><span data-ttu-id="c77e3-161"><a href="platform/mobile-platform-home-page.md">Mobile Plattform</a></span><span class="sxs-lookup"><span data-stu-id="c77e3-161"><a href="platform/mobile-platform-home-page.md">Mobile platform</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c77e3-162">5</span><span class="sxs-lookup"><span data-stu-id="c77e3-162">5</span></span></td>
<td><span data-ttu-id="c77e3-163">ISV</span><span class="sxs-lookup"><span data-stu-id="c77e3-163">ISV</span></span></td>
<td><span data-ttu-id="c77e3-164">Erstellen eines Bereitstellungspaket, das benutzerdefinierte mobile Arbeitsbereiche enthält, und laden Sie das Paket zu den Microsoft Dynamics Lifecycle Services (LCS) hoch.</span><span class="sxs-lookup"><span data-stu-id="c77e3-164">Create a deployable package that contains custom mobile workspaces, and upload the package to Microsoft Dynamics Lifecycle Services (LCS).</span></span></td>
<td><span data-ttu-id="c77e3-165"><a href="../deployment/create-apply-deployable-package.md">Ein Bereitstellungspaket erstellen</a></span><span class="sxs-lookup"><span data-stu-id="c77e3-165"><a href="../deployment/create-apply-deployable-package.md">Create a deployable package</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c77e3-166">6</span><span class="sxs-lookup"><span data-stu-id="c77e3-166">6</span></span></td>
<td><span data-ttu-id="c77e3-167">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="c77e3-167">System administrator</span></span></td>
<td><span data-ttu-id="c77e3-168">Wenden Sie das Bereitstellungspaket an, das die benutzerdefinierten Arbeitsbereiche enthält, die vom unabhängigen Softwareanbieter (ISV) bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c77e3-168">Apply the deployable package that contains the custom workspaces that are provided by the independent software vendor (ISV).</span></span></td>
<td><span data-ttu-id="c77e3-169"><a href="../deployment/apply-deployable-package-system.md">Bereitstellbare Pakete übernehmen</a></span><span class="sxs-lookup"><span data-stu-id="c77e3-169"><a href="../deployment/apply-deployable-package-system.md">Apply a deployable package</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c77e3-170">7</span><span class="sxs-lookup"><span data-stu-id="c77e3-170">7</span></span></td>
<td><span data-ttu-id="c77e3-171">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="c77e3-171">System administrator</span></span></td>
<td><span data-ttu-id="c77e3-172">Veröffentlichen Sie die benutzerdefinierten mobilen Arbeitsbereiche, die von ISV zur Verfügung gestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c77e3-172">Publish the custom mobile workspaces that are provided by the ISV.</span></span></td>
<td><span data-ttu-id="c77e3-173"><a href="publish-mobile-workspace.md">Einen mobilen Arbeitsbereich veröffentlichen</a></span><span class="sxs-lookup"><span data-stu-id="c77e3-173"><a href="publish-mobile-workspace.md">Publish a mobile workspace</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c77e3-174">8</span><span class="sxs-lookup"><span data-stu-id="c77e3-174">8</span></span></td>
<td><span data-ttu-id="c77e3-175">Benutzer</span><span class="sxs-lookup"><span data-stu-id="c77e3-175">User</span></span></td>
<td><span data-ttu-id="c77e3-176">Laden Sie die mobile App herunter, und installieren Sie diese.</span><span class="sxs-lookup"><span data-stu-id="c77e3-176">Download and install the mobile app.</span></span></td>
<td><ul>
<li><span data-ttu-id="c77e3-177"><a href="https://go.microsoft.com/fwlink/?linkid=850662">Für Androide-Smartphones</a></span><span class="sxs-lookup"><span data-stu-id="c77e3-177"><a href="https://go.microsoft.com/fwlink/?linkid=850662">For Android phones</a></span></span></li>
<li><span data-ttu-id="c77e3-178"><a href="https://go.microsoft.com/fwlink/?linkid=850663">Für iPhones</a></span><span class="sxs-lookup"><span data-stu-id="c77e3-178"><a href="https://go.microsoft.com/fwlink/?linkid=850663">For iPhones</a></span></span></li></ul>
</td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c77e3-179">9</span><span class="sxs-lookup"><span data-stu-id="c77e3-179">9</span></span></td>
<td><span data-ttu-id="c77e3-180">Benutzer</span><span class="sxs-lookup"><span data-stu-id="c77e3-180">User</span></span></td>
<td><span data-ttu-id="c77e3-181">Melden Sie sich an, und verwenden Sie die mobile App.</span><span class="sxs-lookup"><span data-stu-id="c77e3-181">Sign in, and use the mobile app.</span></span> <span data-ttu-id="c77e3-182">Die App umfasst die mobilen Arbeitsbereiche, die vom Systemadministrator veröffentlicht wurden.</span><span class="sxs-lookup"><span data-stu-id="c77e3-182">The app includes the mobile workspaces that have been published by the system administrator.</span></span></td>
<td><span data-ttu-id="c77e3-183">Um eine Liste mobiler Arbeitsbereiche anzuzeigen, die von Microsoft bereitgestellt werden, rufen Sie <a href="mobile-workspaces-released.md">Vor Kurzem freigegebene mobile Arbeitsbereiche</a> auf.</span><span class="sxs-lookup"><span data-stu-id="c77e3-183">To see a list of mobile workspaces that are provided by Microsoft, see <a href="mobile-workspaces-released.md">Mobile workspaces recently released</a>.</span></span>
</td>
</tr>
</tbody>
</table>

