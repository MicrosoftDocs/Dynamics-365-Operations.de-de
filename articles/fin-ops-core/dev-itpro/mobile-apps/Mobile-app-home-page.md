---
title: Startseite der mobilen App
description: In diesem Thema wird die Finance and Operations (Dynamics 365) Mobile-App beschrieben. Zudem werden Links zu Ressourcen bereitgestellt, die bei der Implementierung in der Organisation helfen.
author: sericks007
manager: AnnBe
ms.date: 01/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 272853
ms.assetid: c99f818f-27b3-4e45-92b4-74272dad0e17
ms.search.region: Global
ms.author: sericks
ms.dyn365.ops.version: Platform update 4
ms.search.validFrom: 2017-02-28
ms.openlocfilehash: 012b51b66c831a66a54c7c868735e310f05eb8c1
ms.sourcegitcommit: f939bc6292840e29bc0f498efc8f4641dfe8f994
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/22/2020
ms.locfileid: "2975196"
---
# <a name="mobile-app-home-page"></a><span data-ttu-id="54d24-103">Startseite der mobilen App</span><span class="sxs-lookup"><span data-stu-id="54d24-103">Mobile app home page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="54d24-104">In diesem Thema wird die **Finance and Operations (Dynamics 365)** Mobile-App beschrieben. Zudem werden Links zu Ressourcen bereitgestellt, die bei der Implementierung in der Organisation helfen.</span><span class="sxs-lookup"><span data-stu-id="54d24-104">This topic describes the **Finance and Operations (Dynamics 365)** mobile app and provides links to resources that can help you implement it in your organization.</span></span>

<a name="overview"></a><span data-ttu-id="54d24-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="54d24-105">Overview</span></span>
--------

<span data-ttu-id="54d24-106">Die mobile App ermöglicht es Ihrer Organisation, Geschäftsprozesse auf mobilen Geräten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="54d24-106">The mobile app enables your organization to make its business processes available on mobile devices.</span></span> <span data-ttu-id="54d24-107">Nachdem Ihr IT-Administrator den mobilen Arbeitsbereich für Ihre Organisation bereitgestellt hat, können sich Benutzer bei der App anmelden und sofort damit beginnen, Geschäftsprozesse über ihre mobilen Geräte auszuführen.</span><span class="sxs-lookup"><span data-stu-id="54d24-107">After your IT admin enables the mobile workspaces for your organization, users can sign in to the app and immediately begin to run business processes from their mobile devices.</span></span> <span data-ttu-id="54d24-108">Die mobile App umfasst folgende Funktionen, die helfen, die Produktivität zu steigern:</span><span class="sxs-lookup"><span data-stu-id="54d24-108">The mobile app includes the following features that can help increase productivity:</span></span>

- <span data-ttu-id="54d24-109">Benutzer können Geschäftsdaten anzeigen, bearbeiten und ausführen, selbst wenn die Netzwerkverbindung unterbrochen ist oder ihre mobilen Geräte vollständig offline sind.</span><span class="sxs-lookup"><span data-stu-id="54d24-109">Users can view, edit, and act on business data, even if they have intermittent network connectivity or their mobile devices are completely offline.</span></span> <span data-ttu-id="54d24-110">Wenn ein Gerät eine Netzwerkverbindung erneut einrichtet, werden die Offline-Vorgänge automatisch synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="54d24-110">When a device reestablishes a network connection, offline data operations are automatically synchronized.</span></span>
- <span data-ttu-id="54d24-111">IT-Administratoren oder Entwickler können mobile Arbeitsbereiche erstellen und veröffentlichen, die auf die Organisation zugeschnitten wurden.</span><span class="sxs-lookup"><span data-stu-id="54d24-111">IT admins or developers can build and publish mobile workspaces that have been tailored to their organization.</span></span> <span data-ttu-id="54d24-112">Die App verwendet die vorhandenen Codeanlagen.</span><span class="sxs-lookup"><span data-stu-id="54d24-112">The app uses your existing code assets.</span></span> <span data-ttu-id="54d24-113">Daher müssen Sie den Validierungsprozess, Geschäftslogik oder Sicherheitskonfiguration nicht erneut implementieren.</span><span class="sxs-lookup"><span data-stu-id="54d24-113">Therefore, you don't have to re-implement your validation procedures, business logic, or security configuration.</span></span>
- <span data-ttu-id="54d24-114">IT-Administratoren oder -Entwickler können ganz einfach mobile Arbeitsbereiche entwerfen, indem sie den Arbeitsbereichdesigner zum Anzeigen und Klicken verwenden, der im Webclient enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="54d24-114">IT admins or developers can easily design mobile workspaces by using the point-and-click workspace designer that is included with the web client.</span></span>
- <span data-ttu-id="54d24-115">IT-Administratoren oder Entwickler können die Offline-Funktionalität von Arbeitsbereichen optional optimieren, indem das Geschäftslogikerweiterbarkeitsframework verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="54d24-115">IT admins or developers can optionally optimize the offline capabilities of workspaces by using the Business logic extensibility framework.</span></span> <span data-ttu-id="54d24-116">Da Daten weiter verarbeitet werden, wenn ein Gerät offline ist, bleiben die mobilen Szenarien erhalten. auch wenn die Geräte keine permanente Netzwerkkonnektivität haben.</span><span class="sxs-lookup"><span data-stu-id="54d24-116">Because data continues to be processed while a device is offline, your mobile scenarios remain rich and fluid, even if devices don't have constant network connectivity.</span></span>

## <a name="elements-of-the-mobile-app"></a><span data-ttu-id="54d24-117">Elemente der mobilen App</span><span class="sxs-lookup"><span data-stu-id="54d24-117">Elements of the mobile app</span></span>
<span data-ttu-id="54d24-118">Die Navigation in der mobilen App besteht aus vier grundlegenden Konzepten: Dashboard, Arbeitsbereiche, Seiten und Aktivitäten.</span><span class="sxs-lookup"><span data-stu-id="54d24-118">Navigation in the mobile app consists of four basic concepts: the dashboard, workspaces, pages, and actions.</span></span> 

<span data-ttu-id="54d24-119">[![Navigationskonzepte in der mobilen App](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)</span><span class="sxs-lookup"><span data-stu-id="54d24-119">[![Navigation concepts in the mobile app](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)</span></span>

1. <span data-ttu-id="54d24-120">Wenn Sie die App starten, gehen Sie zu **Dashboard**.</span><span class="sxs-lookup"><span data-stu-id="54d24-120">When you start the app, you go to the **dashboard**.</span></span>
2. <span data-ttu-id="54d24-121">Auf dem Dashboard wird eine Liste der veröffentlichten **Arbeitsbereiche** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="54d24-121">On the dashboard, you can see a list of **workspaces** that have been published.</span></span>
3. <span data-ttu-id="54d24-122">In jedem Arbeitsbereich können Sie eine Liste der **Seiten** finden, die für diesen Arbeitsbereich verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="54d24-122">In each workspace, you can see a list of **pages** that are available for that workspace.</span></span>
4. <span data-ttu-id="54d24-123">Nachdem Sie auf einer Seite sind, können Sie eine Reihe von Aktivitäten ausführen.</span><span class="sxs-lookup"><span data-stu-id="54d24-123">After you're on a page, you can perform several actions.</span></span> <span data-ttu-id="54d24-124">Nachfolgend finden Sie einige Beispiele:</span><span class="sxs-lookup"><span data-stu-id="54d24-124">Here are some examples:</span></span>

    - <span data-ttu-id="54d24-125">Zeigen Sie detaillierte Daten an.</span><span class="sxs-lookup"><span data-stu-id="54d24-125">View detailed data.</span></span>
    - <span data-ttu-id="54d24-126">Navigieren Sie zu anderen Seiten mit zugehörige Daten wie Entitätsdetails oder Positionen.</span><span class="sxs-lookup"><span data-stu-id="54d24-126">Navigate to other pages for related data, such as entity details or lines.</span></span>
    - <span data-ttu-id="54d24-127">Zeigen Sie eine Liste mit **Aktivitäten** an, die für die Seite verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="54d24-127">See a list of **actions** that are available for that page.</span></span> <span data-ttu-id="54d24-128">Mit Aktivitäten können Sie vorhandenen Daten erstellen oder bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="54d24-128">Actions let you create or edit existing data.</span></span>

## <a name="implementation-process"></a><span data-ttu-id="54d24-129">Implementierungsprozess</span><span class="sxs-lookup"><span data-stu-id="54d24-129">Implementation process</span></span>
<span data-ttu-id="54d24-130">Die folgende Abbildung veranschaulicht den Prozess des Implementierens beider mobiler Arbeitsbereiche, die von Microsoft und benutzerdefinierten mobilen Arbeitsbereichen bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="54d24-130">The following illustration shows the process for implementing both mobile workspaces that are provided by Microsoft and custom mobile workspaces.</span></span> 

<span data-ttu-id="54d24-131">[![Implementierungsprozess für mobile Apps](./media/Mobile-implementation-process-5.png)](./media/Mobile-implementation-process-5.png)</span><span class="sxs-lookup"><span data-stu-id="54d24-131">[![Mobile apps implementation process](./media/Mobile-implementation-process-5.png)](./media/Mobile-implementation-process-5.png)</span></span>

<span data-ttu-id="54d24-132">Die folgende Tabelle enthält Links zu Ressourcen, die Ihnen beim Implementieren beider mobilen Arbeitsbereiche helfen, die von Microsoft und benutzerdefinierten mobilen Arbeitsbereichen bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="54d24-132">The following table includes links to resources that can help you implement both mobile workspaces that are provided by Microsoft and custom mobile workspaces.</span></span> <span data-ttu-id="54d24-133">Die Nummern in der ersten Spalte entsprechen den nummerierten Schritten in der vorherigen Abbildung.</span><span class="sxs-lookup"><span data-stu-id="54d24-133">The numbers in the first column correspond to the numbered steps in the previous illustration.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="54d24-134">Schritt</span><span class="sxs-lookup"><span data-stu-id="54d24-134">Step</span></span></th>
<th><span data-ttu-id="54d24-135">Rolle</span><span class="sxs-lookup"><span data-stu-id="54d24-135">Role</span></span></th>
<th><span data-ttu-id="54d24-136">Vorgang</span><span class="sxs-lookup"><span data-stu-id="54d24-136">Action</span></span></th>
<th><span data-ttu-id="54d24-137">Ressourcen, die Ihnen beim Erfüllen der Aktivität helfen</span><span class="sxs-lookup"><span data-stu-id="54d24-137">Resources to help you complete the action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="54d24-138">1</span><span class="sxs-lookup"><span data-stu-id="54d24-138">1</span></span></td>
<td><span data-ttu-id="54d24-139">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="54d24-139">System administrator</span></span></td>
<td><span data-ttu-id="54d24-140">Implementieren Sie die Finance and Operations App in Ihrer Organisation.</span><span class="sxs-lookup"><span data-stu-id="54d24-140">Implement the Finance and Operations app in your organization.</span></span></td>
<td><ul><li><span data-ttu-id="54d24-141">Wenn Sie noch keine Version von Microsoft Dynamics 365 bereitgestellt haben, siehe <a href="../deployment/deploy-demo-environment.md">Eine Demoumgebung bereitstellen</a>.</span><span class="sxs-lookup"><span data-stu-id="54d24-141">If you haven&#39;t yet deployed a version of Microsoft Dynamics 365, see <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span></li><li><span data-ttu-id="54d24-142">Um eine Liste mobiler Arbeitsbereiche anzuzeigen, die verwendet werden können, siehe <a href="mobile-workspaces-released.md">Vor Kurzem freigegebene mobile Arbeitsbereiche</a>.</span><span class="sxs-lookup"><span data-stu-id="54d24-142">To see a list of mobile workspaces that can be used, see <a href="mobile-workspaces-released.md">Mobile workspaces recently released</a>.</span></span></li></ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54d24-143">2</span><span class="sxs-lookup"><span data-stu-id="54d24-143">2</span></span></td>
<td><span data-ttu-id="54d24-144">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="54d24-144">System administrator</span></span></td>
<td><span data-ttu-id="54d24-145"><strong>Falls Sie Microsoft Dynamics 365 for Operations Version 1611 verwenden:</strong>Laden Sie KBs herunter und installieren Sie diese. Sie aktivieren die mobilen Arbeitsbereiche, die von Microsoft bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="54d24-145"><strong>If you&#39;re using Microsoft Dynamics 365 for Operations version 1611:</strong> Download and install KBs that enable the mobile workspaces that are provided by Microsoft.</span></span></td>
<td><span data-ttu-id="54d24-146">Weitere Informationen finden Sie in folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="54d24-146">See the following topics for more information:</span></span>
<ul>

<li><span data-ttu-id="54d24-147"><a href="../../../finance/cost-accounting/cost-controlling-mobile-workspace.md">Mobiler Arbeitsbereich für die Kostensteuerung</a></span><span class="sxs-lookup"><span data-stu-id="54d24-147"><a href="../../../finance/cost-accounting/cost-controlling-mobile-workspace.md">Cost controlling mobile workspaces</a></span></span></li>
<li><span data-ttu-id="54d24-148"><a href="../../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">Mobiler Arbeitsbereich für Lagerbestand</a></span><span class="sxs-lookup"><span data-stu-id="54d24-148"><a href="../../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">Inventory on-hand mobile workspace</a></span></span></li>
<li><span data-ttu-id="54d24-149"><a href="../../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">Aufträge, mobiler Arbeitsbereich</a></span><span class="sxs-lookup"><span data-stu-id="54d24-149"><a href="../../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">Sales orders mobile workspaces</a></span></span></li>
<li><span data-ttu-id="54d24-150"><a href="../../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">Mobiler Arbeitsbereich für Kreditorenzusammenarbeit</a></span><span class="sxs-lookup"><span data-stu-id="54d24-150"><a href="../../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">Vendor collaboration mobile workspace</a></span></span></li>
<li><span data-ttu-id="54d24-151"><a href="../../../finance/project-management/project-time-entry-mobile-workspace.md">Mobiler Arbeitsbereich für Projektzeiterfassung</a></span><span class="sxs-lookup"><span data-stu-id="54d24-151"><a href="../../../finance/project-management/project-time-entry-mobile-workspace.md">Project time entry mobile workspace</a></span></span></li>
<li><span data-ttu-id="54d24-152"><a href="../../../finance/expense-management/expense-management-mobile-workspace.md">Mobiler Arbeitsbereich für Spesenverwaltung</a></span><span class="sxs-lookup"><span data-stu-id="54d24-152"><a href="../../../finance/expense-management/expense-management-mobile-workspace.md">Expense management mobile workspace</a></span></span></li>

</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54d24-153">3</span><span class="sxs-lookup"><span data-stu-id="54d24-153">3</span></span></td>
<td><span data-ttu-id="54d24-154">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="54d24-154">System administrator</span></span></td>
<td><span data-ttu-id="54d24-155">Veröffentlichen Sie die mobilen Arbeitsbereiche, die von Microsoft zur Verfügung gestellt werden.</span><span class="sxs-lookup"><span data-stu-id="54d24-155">Publish the mobile workspaces that are provided by Microsoft.</span></span></td>
<td><span data-ttu-id="54d24-156"><a href="publish-mobile-workspace.md">Mobilen Arbeitsbereich veröffentlichen</a>
</span><span class="sxs-lookup"><span data-stu-id="54d24-156"><a href="publish-mobile-workspace.md">Publish a mobile workspace</a>
</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54d24-157">4</span><span class="sxs-lookup"><span data-stu-id="54d24-157">4</span></span></td>
<td><span data-ttu-id="54d24-158">Entwickler oder unabhängiger Softwarehersteller (ISV)</span><span class="sxs-lookup"><span data-stu-id="54d24-158">Developer or independent software vendor (ISV)</span></span></td>
<td><span data-ttu-id="54d24-159">Nutzen Sie die mobile Plattform, um benutzerdefinierte mobile Arbeitsbereiche zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="54d24-159">Use the mobile platform to create custom mobile workspaces.</span></span></td>
<td><span data-ttu-id="54d24-160"><a href="platform/mobile-platform-home-page.md">Mobile Plattform</a></span><span class="sxs-lookup"><span data-stu-id="54d24-160"><a href="platform/mobile-platform-home-page.md">Mobile platform</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54d24-161">5</span><span class="sxs-lookup"><span data-stu-id="54d24-161">5</span></span></td>
<td><span data-ttu-id="54d24-162">ISV</span><span class="sxs-lookup"><span data-stu-id="54d24-162">ISV</span></span></td>
<td><span data-ttu-id="54d24-163">Erstellen Sie ein Bereitstellungspaket, das benutzerdefinierte mobile Arbeitsbereiche enthält, und laden Sie das Paket zu Microsoft Dynamics Lifecycle Services (LCS) hoch.</span><span class="sxs-lookup"><span data-stu-id="54d24-163">Create a deployable package that contains custom mobile workspaces, and upload the package to Microsoft Dynamics Lifecycle Services (LCS).</span></span></td>
<td><span data-ttu-id="54d24-164"><a href="../deployment/create-apply-deployable-package.md">Ein bereitstellbares Paket erstellen</a></span><span class="sxs-lookup"><span data-stu-id="54d24-164"><a href="../deployment/create-apply-deployable-package.md">Create a deployable package</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54d24-165">6</span><span class="sxs-lookup"><span data-stu-id="54d24-165">6</span></span></td>
<td><span data-ttu-id="54d24-166">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="54d24-166">System administrator</span></span></td>
<td><span data-ttu-id="54d24-167">Wenden Sie das Bereitstellungspaket an, das die benutzerdefinierten Arbeitsbereiche enthält, die vom unabhängigen Softwareanbieter (ISV) bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="54d24-167">Apply the deployable package that contains the custom workspaces that are provided by the independent software vendor (ISV).</span></span></td>
<td><span data-ttu-id="54d24-168"><a href="../deployment/apply-deployable-package-system.md">Bereitstellbare Pakete übernehmen</a></span><span class="sxs-lookup"><span data-stu-id="54d24-168"><a href="../deployment/apply-deployable-package-system.md">Apply a deployable package</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54d24-169">7</span><span class="sxs-lookup"><span data-stu-id="54d24-169">7</span></span></td>
<td><span data-ttu-id="54d24-170">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="54d24-170">System administrator</span></span></td>
<td><span data-ttu-id="54d24-171">Veröffentlichen Sie die benutzerdefinierten mobilen Arbeitsbereiche, die von ISV zur Verfügung gestellt werden.</span><span class="sxs-lookup"><span data-stu-id="54d24-171">Publish the custom mobile workspaces that are provided by the ISV.</span></span></td>
<td><span data-ttu-id="54d24-172"><a href="publish-mobile-workspace.md">Veröffentlichen eines mobilen Arbeitsbereichs</a></span><span class="sxs-lookup"><span data-stu-id="54d24-172"><a href="publish-mobile-workspace.md">Publish a mobile workspace</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54d24-173">8</span><span class="sxs-lookup"><span data-stu-id="54d24-173">8</span></span></td>
<td><span data-ttu-id="54d24-174">Benutzer</span><span class="sxs-lookup"><span data-stu-id="54d24-174">User</span></span></td>
<td><span data-ttu-id="54d24-175">Laden Sie die mobile App herunter, und installieren Sie diese.</span><span class="sxs-lookup"><span data-stu-id="54d24-175">Download and install the mobile app.</span></span></td>
<td><span data-ttu-id="54d24-176">
<a href="https://go.microsoft.com/fwlink/?linkid=850662">Finance and Operations App für Office Android</a></span><span class="sxs-lookup"><span data-stu-id="54d24-176">
<a href="https://go.microsoft.com/fwlink/?linkid=850662">Finance and Operations app for Android</a></span></span><BR/><span data-ttu-id="54d24-177">
<a href="https://go.microsoft.com/fwlink/?linkid=850663">Finance and Operations App für iOS</a></span><span class="sxs-lookup"><span data-stu-id="54d24-177">
<a href="https://go.microsoft.com/fwlink/?linkid=850663">Finance and Operations app for iOS</a></span></span><BR/>
<span data-ttu-id="54d24-178">(Windows Phone nicht unterstützt)</span><span class="sxs-lookup"><span data-stu-id="54d24-178">(Windows Phone unsupported)</span></span>
</td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54d24-179">9</span><span class="sxs-lookup"><span data-stu-id="54d24-179">9</span></span></td>
<td><span data-ttu-id="54d24-180">Benutzer</span><span class="sxs-lookup"><span data-stu-id="54d24-180">User</span></span></td>
<td><span data-ttu-id="54d24-181">Melden Sie sich an, und verwenden Sie die mobile App.</span><span class="sxs-lookup"><span data-stu-id="54d24-181">Sign in, and use the mobile app.</span></span> <span data-ttu-id="54d24-182">Die App umfasst die mobilen Arbeitsbereiche, die vom Systemadministrator veröffentlicht wurden.</span><span class="sxs-lookup"><span data-stu-id="54d24-182">The app includes the mobile workspaces that have been published by the system administrator.</span></span></td>
<td><span data-ttu-id="54d24-183">Um eine Liste mobiler Arbeitsbereiche anzuzeigen, die von Microsoft bereitgestellt werden, rufen Sie <a href="mobile-workspaces-released.md">Vor Kurzem freigegebene mobile Arbeitsbereiche</a> auf.</span><span class="sxs-lookup"><span data-stu-id="54d24-183">To see a list of mobile workspaces that are provided by Microsoft, see <a href="mobile-workspaces-released.md">Mobile workspaces recently released</a>.</span></span>
</td>
</tr>
</tbody>
</table>

## <a name="troubleshooting"></a><span data-ttu-id="54d24-184">Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="54d24-184">Troubleshooting</span></span>
[<span data-ttu-id="54d24-185">Mobile Plattformressourcen</span><span class="sxs-lookup"><span data-stu-id="54d24-185">Mobile platform resources</span></span>](platform/mobile-platform-home-page.md#troubleshooting-the-app)
