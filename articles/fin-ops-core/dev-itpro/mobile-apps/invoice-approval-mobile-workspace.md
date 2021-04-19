---
title: Rechnungsgenehmigungen im mobilen Arbeitsbereich
description: Dieses Thema enthält Informationen zur Rechnungsgenehmigung im mobilen Arbeitsbereich.
author: abruer
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: c3414d6ef5f2df62f37f1ef2e7e2ff43ce040e5e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752249"
---
# <a name="invoice-approvals-mobile-workspace"></a><span data-ttu-id="5be2d-103">Rechnungsgenehmigungen im mobilen Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="5be2d-103">Invoice approvals mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5be2d-104">Dieses Thema enthält Informationen zur **Rechnungsgenehmigung** im mobilen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="5be2d-104">This topic provides information about the **Invoice approvals** mobile workspace.</span></span> <span data-ttu-id="5be2d-105">Der Arbeitsbereich enthält eine Liste von Rechnungen, die Ihnen über den Kreditorenrechnungskopfworkflowprozess zugewiesen wurden.</span><span class="sxs-lookup"><span data-stu-id="5be2d-105">This workspace provides a list of invoices that have been assigned to you through the vendor invoice header workflow process.</span></span> 

<span data-ttu-id="5be2d-106">Dieser mobile Arbeitsbereich soll mit der Finance and Operations Mobile-App verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5be2d-106">This mobile workspace is intended to be used with the Finance and Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="5be2d-107">Übersicht</span><span class="sxs-lookup"><span data-stu-id="5be2d-107">Overview</span></span>

<span data-ttu-id="5be2d-108">Mit dem mobilen Arbeitsbereich **Rechnungsgenehmigungen** können Mitarbeiter und Vorgesetzte für Kreditorenkonten Rechnungen anzeigen, die ihnen als Teil des Kreditorenrechnungskopfworkflowprozesses zugewiesen wurden.</span><span class="sxs-lookup"><span data-stu-id="5be2d-108">The **Invoice approvals** mobile workspace lets Accounts payable clerks and managers view invoices that have been assigned to them as part of the vendor invoice header workflow process.</span></span> <span data-ttu-id="5be2d-109">Sie können Rechnungsinformationen und sogar die Positions- und Verteilungsdetails anzeigen, um informierte Genehmigungsentscheidungen zu treffen.</span><span class="sxs-lookup"><span data-stu-id="5be2d-109">You can view the invoice information, and even the line and distribution details, to help you make informed approval decisions.</span></span> <span data-ttu-id="5be2d-110">Über den Arbeitsbereich können Sie Maßnahmen ergreifen, um die Rechnung durch den Workflowprozess durchlaufen zu lassen.</span><span class="sxs-lookup"><span data-stu-id="5be2d-110">From the workspace, you can take action to move the invoice through the workflow process.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="5be2d-111">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="5be2d-111">Prerequisites</span></span>

<span data-ttu-id="5be2d-112">Bevor Sie diesen mobilen Arbeitsbereich verwenden können, müssen die folgenden Voraussetzungen erfüllt werden.</span><span class="sxs-lookup"><span data-stu-id="5be2d-112">Before you can use this mobile workspace, the following prerequisites must be met.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="5be2d-113">Voraussetzung</span><span class="sxs-lookup"><span data-stu-id="5be2d-113">Prerequisite</span></span></th>
<th><span data-ttu-id="5be2d-114">Rolle</span><span class="sxs-lookup"><span data-stu-id="5be2d-114">Role</span></span></th>
<th><span data-ttu-id="5be2d-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5be2d-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5be2d-116">Microsoft Dynamics 365 Finance muss in der Organisation bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="5be2d-116">Microsoft Dynamics 365 Finance must be deployed in your organization.</span></span></td>
<td><span data-ttu-id="5be2d-117">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="5be2d-117">System administrator</span></span></td>
<td><span data-ttu-id="5be2d-118">Siehe auch <a href="../deployment/deploy-demo-environment.md">Eine Demoumgebung bereitstellen</a></span><span class="sxs-lookup"><span data-stu-id="5be2d-118">See <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="5be2d-119">Der mobile Arbeitsbereich <strong>Rechnungsgenehmigungen</strong> muss bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="5be2d-119">The <strong>Invoice approvals</strong> mobile workspace must be published.</span></span></td>
<td><span data-ttu-id="5be2d-120">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="5be2d-120">System administrator</span></span></td>
<td><span data-ttu-id="5be2d-121">Siehe <a href="publish-mobile-workspace.md">Einen mobilen Arbeitsbereich veröffentlichen</a>.</span><span class="sxs-lookup"><span data-stu-id="5be2d-121">See <a href="publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="5be2d-122">Herunterladen und Installieren der mobilen App</span><span class="sxs-lookup"><span data-stu-id="5be2d-122">Download and install the mobile app</span></span>

<span data-ttu-id="5be2d-123">Herunterladen und Installieren der Finance and Operations mobilen App:</span><span class="sxs-lookup"><span data-stu-id="5be2d-123">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="5be2d-124">Für Android-Smartphones</span><span class="sxs-lookup"><span data-stu-id="5be2d-124">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="5be2d-125">Für iPhones</span><span class="sxs-lookup"><span data-stu-id="5be2d-125">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="5be2d-126">Bei der mobile App anmelden</span><span class="sxs-lookup"><span data-stu-id="5be2d-126">Sign in to the mobile app</span></span>

1.  <span data-ttu-id="5be2d-127">Starten Sie die App auf Ihrem mobilen Gerät.</span><span class="sxs-lookup"><span data-stu-id="5be2d-127">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="5be2d-128">Geben Sie die Microsoft Dynamics 365-URL ein.</span><span class="sxs-lookup"><span data-stu-id="5be2d-128">Enter your Microsoft Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="5be2d-129">Bei der erstmaligen Anwendung werden Sie nach Ihrem Benutzernamen und dem Kennwort gefragt.</span><span class="sxs-lookup"><span data-stu-id="5be2d-129">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="5be2d-130">Geben Sie Ihre Anmeldeinformationen ein.</span><span class="sxs-lookup"><span data-stu-id="5be2d-130">Enter your credentials.</span></span>
4.  <span data-ttu-id="5be2d-131">Nachdem Sie sich angemeldet haben, werden verfügbare Arbeitsbereiche für Ihr Unternehmen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5be2d-131">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="5be2d-132">Beachten Sie, dass Sie, wenn Ihr Systemadministrator einen neuen Arbeitsbereich später veröffentlicht, die Liste der mobilen Arbeitsbereiche aktualisieren müssen.</span><span class="sxs-lookup"><span data-stu-id="5be2d-132">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

    <span data-ttu-id="5be2d-133">[![Zum Aktualisieren ziehen](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="5be2d-133">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="approve-invoices-by-using-the-invoice-approvals-mobile-workspace"></a><span data-ttu-id="5be2d-134">Genehmigen von Rechnungen mit dem mobilen Arbeitsbereich für Rechnungsgenehmigungen</span><span class="sxs-lookup"><span data-stu-id="5be2d-134">Approve invoices by using the Invoice approvals mobile workspace</span></span>
1.  <span data-ttu-id="5be2d-135">Wählen Sie auf Ihrem mobilen Gerät den Arbeitsbereich **Rechnungsgenehmigungen**.</span><span class="sxs-lookup"><span data-stu-id="5be2d-135">On your mobile device, select the **Invoice approvals** workspace.</span></span>
2.  <span data-ttu-id="5be2d-136">Wählen Sie die Rechnung aus, die Ihnen über den Kreditorenrechnungskopfworkflowprozess zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="5be2d-136">Select the invoice that has been assigned to you by the vendor invoice header workflow process.</span></span>
3.  <span data-ttu-id="5be2d-137">Auf der Seite **Rechnungsdetails** können Sie die Rechnungskopfinformationen prüfen, beispielsweise Kreditor- und die Datumsinformationen.</span><span class="sxs-lookup"><span data-stu-id="5be2d-137">On the **Invoice details** page, review the invoice header information, such as the vendor and date information.</span></span>
4.  <span data-ttu-id="5be2d-138">Wählen Sie eine Position in der Rechnung aus, um ausführlichere Informationen dazu in der Ansicht **Rechnungspositionsdetails** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="5be2d-138">Select a line on the invoice to view more detailed information about it in the **Invoice line details** view.</span></span>
5.  <span data-ttu-id="5be2d-139">Wählen Sie in der Ansicht **Rechnungspositionsdetails** **Verteilungen** aus, um Positionsverteilungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="5be2d-139">In the **Invoice line details** view, select **Distributions** to show the line distributions.</span></span> <span data-ttu-id="5be2d-140">Hier können Sie die Buchhaltung für die Rechnungsposition anzeigen.</span><span class="sxs-lookup"><span data-stu-id="5be2d-140">Here, you can view the accounting for the invoice line.</span></span> <span data-ttu-id="5be2d-141">Die Informationen, die angezeigt werden, schließen die Finanzdimensionen und das Hauptkonto ein.</span><span class="sxs-lookup"><span data-stu-id="5be2d-141">The information that is shown includes the financial dimensions and the main account.</span></span>
6.  <span data-ttu-id="5be2d-142">Wählen Sie auf der Seite **Rechnungsdetails** **Verteilungen** aus, um alle Verteilungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="5be2d-142">On the **Invoice details** page, select **Distributions** to show all distributions.</span></span> <span data-ttu-id="5be2d-143">Hier können Sie die Buchhaltung für die gesamte Rechnung anzeigen.</span><span class="sxs-lookup"><span data-stu-id="5be2d-143">Here, you can view the accounting for the whole invoice.</span></span> <span data-ttu-id="5be2d-144">Die Informationen, die angezeigt werden, schließen die Finanzdimensionen und das Hauptkonto ein.</span><span class="sxs-lookup"><span data-stu-id="5be2d-144">The information that is shown includes the financial dimensions and the main accounts.</span></span> 
7.  <span data-ttu-id="5be2d-145">Wählen Sie die Ansicht **Anhänge** aus, um alle Hinweise oder Dateien anzuzeigen, die der Rechnung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="5be2d-145">Select **Attachments** to view any notes or files that are attached to the invoice.</span></span>
8.  <span data-ttu-id="5be2d-146">Wählen Sie auf der Seite **Rechnungsdetails** eine geeignete Workflowaktivität aus, um den Prüfprozess abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="5be2d-146">On the **Invoice details** page, select the appropriate workflow action to complete your review process.</span></span>
9.  <span data-ttu-id="5be2d-147">Wählen Sie **Fertig**.</span><span class="sxs-lookup"><span data-stu-id="5be2d-147">Select **Done**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]