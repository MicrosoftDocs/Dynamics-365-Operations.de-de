---
title: Rechnungsgenehmigungen im mobilen Arbeitsbereich
description: "Dieses Thema enthält Informationen zur Rechnungsgenehmigung im mobilen Arbeitsbereich. Der Arbeitsbereich enthält eine Liste von Rechnungen, die Ihnen über den Kreditorenrechnungskopfworkflowprozess zugewiesen wurden."
author: abruer
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 6c95c2779d996f489679c8dda4cda462ba0a05ac
ms.contentlocale: de-de
ms.lasthandoff: 03/26/2018

---

# <a name="invoice-approvals-mobile-workspace"></a><span data-ttu-id="20de2-104">Rechnungsgenehmigungen im mobilen Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="20de2-104">Invoice approvals mobile workspace</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="20de2-105">Dieses Thema enthält Informationen zur **Rechnungsgenehmigung** im mobilen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="20de2-105">This topic provides information about the **Invoice approvals** mobile workspace.</span></span> <span data-ttu-id="20de2-106">Der Arbeitsbereich enthält eine Liste von Rechnungen, die Ihnen über den Kreditorenrechnungskopfworkflowprozess zugewiesen wurden.</span><span class="sxs-lookup"><span data-stu-id="20de2-106">This workspace provides a list of invoices that have been assigned to you through the vendor invoice header workflow process.</span></span> 

<span data-ttu-id="20de2-107">Dieser mobile Arbeitsbereich soll mit der Mobil-App für Microsoft Dynamics 365 für Unified Operations verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="20de2-107">This mobile workspace is intended to be used with the Microsoft Dynamics 365 for Unified Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="20de2-108">Überblick</span><span class="sxs-lookup"><span data-stu-id="20de2-108">Overview</span></span>

<span data-ttu-id="20de2-109">Mit dem mobilen Arbeitsbereich **Rechnungsgenehmigungen** können Mitarbeiter und Vorgesetzte für Kreditorenkonten Rechnungen anzeigen, die ihnen als Teil des Kreditorenrechnungskopfworkflowprozesses zugewiesen wurden.</span><span class="sxs-lookup"><span data-stu-id="20de2-109">The **Invoice approvals** mobile workspace lets Accounts payable clerks and managers view invoices that have been assigned to them as part of the vendor invoice header workflow process.</span></span> <span data-ttu-id="20de2-110">Sie können Rechnungsinformationen und sogar die Positions- und Verteilungsdetails anzeigen, um informierte Genehmigungsentscheidungen zu treffen.</span><span class="sxs-lookup"><span data-stu-id="20de2-110">You can view the invoice information, and even the line and distribution details, to help you make informed approval decisions.</span></span> <span data-ttu-id="20de2-111">Über den Arbeitsbereich können Sie Maßnahmen ergreifen, um die Rechnung durch den Workflowprozess durchlaufen zu lassen.</span><span class="sxs-lookup"><span data-stu-id="20de2-111">From the workspace, you can take action to move the invoice through the workflow process.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="20de2-112">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="20de2-112">Prerequisites</span></span>

<span data-ttu-id="20de2-113">Bevor Sie diesen mobilen Arbeitsbereich verwenden können, müssen die folgenden Voraussetzungen erfüllt werden.</span><span class="sxs-lookup"><span data-stu-id="20de2-113">Before you can use this mobile workspace, the following prerequisites must be met.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="20de2-114">Voraussetzung</span><span class="sxs-lookup"><span data-stu-id="20de2-114">Prerequisite</span></span></th>
<th><span data-ttu-id="20de2-115">Rolle</span><span class="sxs-lookup"><span data-stu-id="20de2-115">Role</span></span></th>
<th><span data-ttu-id="20de2-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="20de2-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="20de2-117">Microsoft Dynamics 365 for Finance and Operations muss in Ihrer Organisation bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="20de2-117">Microsoft Dynamics 365 for Finance and Operations must be deployed in your organization.</span></span></td>
<td><span data-ttu-id="20de2-118">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="20de2-118">System administrator</span></span></td>
<td><span data-ttu-id="20de2-119">Siehe auch <a href="../deployment/deploy-demo-environment.md">Eine Demoumgebung bereitstellen</a></span><span class="sxs-lookup"><span data-stu-id="20de2-119">See <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="20de2-120">Der mobile Arbeitsbereich <strong>Rechnungsgenehmigungen</strong> muss bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="20de2-120">The <strong>Invoice approvals</strong> mobile workspace must be published.</span></span></td>
<td><span data-ttu-id="20de2-121">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="20de2-121">System administrator</span></span></td>
<td><span data-ttu-id="20de2-122">Siehe <a href="publish-mobile-workspace.md">Einen mobilen Arbeitsbereich veröffentlichen</a>.</span><span class="sxs-lookup"><span data-stu-id="20de2-122">See <a href="publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="20de2-123">Herunterladen und Installieren der mobilen App</span><span class="sxs-lookup"><span data-stu-id="20de2-123">Download and install the mobile app</span></span>

<span data-ttu-id="20de2-124">Laden Sie die mobile App für Dynamics 365 for Unified Operations herunter und installieren Sie diese:</span><span class="sxs-lookup"><span data-stu-id="20de2-124">Download and install the Dynamics 365 for Unified Operations mobile app:</span></span>

-   [<span data-ttu-id="20de2-125">Für Androide-Smartphones</span><span class="sxs-lookup"><span data-stu-id="20de2-125">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="20de2-126">Für iPhones</span><span class="sxs-lookup"><span data-stu-id="20de2-126">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="20de2-127">Bei der mobile App anmelden</span><span class="sxs-lookup"><span data-stu-id="20de2-127">Sign in to the mobile app</span></span>

1.  <span data-ttu-id="20de2-128">Starten Sie die App auf Ihrem mobilen Gerät.</span><span class="sxs-lookup"><span data-stu-id="20de2-128">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="20de2-129">Geben Sie die Microsoft Dynamics 365-URL ein.</span><span class="sxs-lookup"><span data-stu-id="20de2-129">Enter your Microsoft Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="20de2-130">Bei der erstmaligen Anwendung werden Sie nach Ihrem Benutzernamen und dem Kennwort gefragt.</span><span class="sxs-lookup"><span data-stu-id="20de2-130">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="20de2-131">Geben Sie Ihre Anmeldeinformationen ein.</span><span class="sxs-lookup"><span data-stu-id="20de2-131">Enter your credentials.</span></span>
4.  <span data-ttu-id="20de2-132">Nachdem Sie sich angemeldet haben, werden verfügbare Arbeitsbereiche für Ihr Unternehmen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="20de2-132">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="20de2-133">Beachten Sie, dass Sie, wenn Ihr Systemadministrator einen neuen Arbeitsbereich später veröffentlicht, die Liste der mobilen Arbeitsbereiche aktualisieren müssen.</span><span class="sxs-lookup"><span data-stu-id="20de2-133">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

    <span data-ttu-id="20de2-134">[![Zum Aktualisieren ziehen](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="20de2-134">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="approve-invoices-by-using-the-invoice-approvals-mobile-workspace"></a><span data-ttu-id="20de2-135">Genehmigen von Rechnungen mit dem mobilen Arbeitsbereich für Rechnungsgenehmigungen</span><span class="sxs-lookup"><span data-stu-id="20de2-135">Approve invoices by using the Invoice approvals mobile workspace</span></span>
1.  <span data-ttu-id="20de2-136">Wählen Sie auf Ihrem mobilen Gerät den Arbeitsbereich **Rechnungsgenehmigungen**.</span><span class="sxs-lookup"><span data-stu-id="20de2-136">On your mobile device, select the **Invoice approvals** workspace.</span></span>
2.  <span data-ttu-id="20de2-137">Wählen Sie die Rechnung aus, die Ihnen über den Kreditorenrechnungskopfworkflowprozess zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="20de2-137">Select the invoice that has been assigned to you by the vendor invoice header workflow process.</span></span>
3.  <span data-ttu-id="20de2-138">Auf der Seite **Rechnungsdetails** können Sie die Rechnungskopfinformationen prüfen, beispielsweise Kreditor- und die Datumsinformationen.</span><span class="sxs-lookup"><span data-stu-id="20de2-138">On the **Invoice details** page, review the invoice header information, such as the vendor and date information.</span></span>
4.  <span data-ttu-id="20de2-139">Wählen Sie eine Position in der Rechnung aus, um ausführlichere Informationen dazu in der Ansicht **Rechnungspositionsdetails** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="20de2-139">Select a line on the invoice to view more detailed information about it in the **Invoice line details** view.</span></span>
5.  <span data-ttu-id="20de2-140">Wählen Sie in der Ansicht **Rechnungspositionsdetails** **Verteilungen** aus, um Positionsverteilungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="20de2-140">In the **Invoice line details** view, select **Distributions** to show the line distributions.</span></span> <span data-ttu-id="20de2-141">Hier können Sie die Buchhaltung für die Rechnungsposition anzeigen.</span><span class="sxs-lookup"><span data-stu-id="20de2-141">Here, you can view the accounting for the invoice line.</span></span> <span data-ttu-id="20de2-142">Die Informationen, die angezeigt werden, schließen die Finanzdimensionen und das Hauptkonto ein.</span><span class="sxs-lookup"><span data-stu-id="20de2-142">The information that is shown includes the financial dimensions and the main account.</span></span>
6.  <span data-ttu-id="20de2-143">Wählen Sie auf der Seite **Rechnungsdetails** **Verteilungen** aus, um alle Verteilungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="20de2-143">On the **Invoice details** page, select **Distributions** to show all distributions.</span></span> <span data-ttu-id="20de2-144">Hier können Sie die Buchhaltung für die gesamte Rechnung anzeigen.</span><span class="sxs-lookup"><span data-stu-id="20de2-144">Here, you can view the accounting for the whole invoice.</span></span> <span data-ttu-id="20de2-145">Die Informationen, die angezeigt werden, schließen die Finanzdimensionen und das Hauptkonto ein.</span><span class="sxs-lookup"><span data-stu-id="20de2-145">The information that is shown includes the financial dimensions and the main accounts.</span></span> 
7.  <span data-ttu-id="20de2-146">Wählen Sie die Ansicht **Anhänge** aus, um alle Hinweise oder Dateien anzuzeigen, die der Rechnung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="20de2-146">Select **Attachments** to view any notes or files that are attached to the invoice.</span></span>
8.  <span data-ttu-id="20de2-147">Wählen Sie auf der Seite **Rechnungsdetails** eine geeignete Workflowaktivität aus, um den Prüfprozess abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="20de2-147">On the **Invoice details** page, select the appropriate workflow action to complete your review process.</span></span>
9.  <span data-ttu-id="20de2-148">Wählen Sie **Fertig**.</span><span class="sxs-lookup"><span data-stu-id="20de2-148">Select **Done**.</span></span>

