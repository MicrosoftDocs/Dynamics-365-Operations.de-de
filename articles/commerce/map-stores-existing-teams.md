---
title: Shops und Teams zuordnen, wenn in Microsoft Teams bereits Teams vorhanden sind
description: In diesem Thema wird beschrieben, wie Sie Shops und dazugehörige Teams in der Dynamics 365 Commerce-Zentralverwaltung zuordnen, wenn Ihre Organisation bereits vor der Commerce-Integration Teams in Microsoft Teams erstellt hat.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: ccc2cbf11e405facf310d93e5458cfe12a43146d
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020218"
---
# <a name="map-stores-and-teams-if-there-are-pre-existing-teams-in-microsoft-teams"></a><span data-ttu-id="3f16c-103">Shops und Teams zuordnen, wenn in Microsoft Teams bereits Teams vorhanden sind</span><span class="sxs-lookup"><span data-stu-id="3f16c-103">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3f16c-104">In diesem Thema wird beschrieben, wie Sie Shops und dazugehörige Teams in der Dynamics 365 Commerce-Zentralverwaltung zuordnen, wenn Ihre Organisation bereits vor der Commerce-Integration Teams in Microsoft Teams erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="3f16c-104">This topic covers how to map stores and corresponding teams in Dynamics 365 Commerce headquarters if your organization has already created teams in Microsoft Teams before Commerce integration.</span></span>

<span data-ttu-id="3f16c-105">Ihre Organisation hat vielleicht schon vor der Integration von Dynamics 365 Commerce und Microsoft Teams Teams für einige oder alle Ihre Shops erstellt.</span><span class="sxs-lookup"><span data-stu-id="3f16c-105">Your organization may have teams created for some or all of your stores before integrating Dynamics 365 Commerce and Microsoft Teams.</span></span> <span data-ttu-id="3f16c-106">Wenn dies der Fall ist, müssen Sie für die Aufgabensynchronisierung zwischen Commerce POS und Microsoft Teams die Zuordnung der Shops und des dazugehörigen Teams in der Commerce-Zentralverwaltung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="3f16c-106">If this is the case, to establish task synchronization between Commerce POS and Microsoft Teams you must provide the mapping of stores and corresponding team in Commerce headquarters.</span></span>

## <a name="map-stores-and-corresponding-teams-in-commerce-headquarters"></a><span data-ttu-id="3f16c-107">Shops und dazugehörige Teams in der Commerce-Zentralverwaltung zuordnen</span><span class="sxs-lookup"><span data-stu-id="3f16c-107">Map stores and corresponding teams in Commerce headquarters</span></span> 

<span data-ttu-id="3f16c-108">Gehen Sie wie folgt vor, um Shops und dazugehörige Teams in der Commerce-Zentralverwaltung zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="3f16c-108">To map stores and corresponding teams in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="3f16c-109">Gehen Sie zu **Systemverwaltung \> Arbeitsbereich \> Datenverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="3f16c-109">Go to **System Administration \> Workspace \> Data management**.</span></span>
1. <span data-ttu-id="3f16c-110">Wählen Sie **Exportieren**.</span><span class="sxs-lookup"><span data-stu-id="3f16c-110">Select **Export**.</span></span> 
1. <span data-ttu-id="3f16c-111">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="3f16c-111">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="3f16c-112">Gehen Sie als **Gruppenname** „Teams-Zuordnung exportieren“ ein.</span><span class="sxs-lookup"><span data-stu-id="3f16c-112">Under **Group name**, enter "Export Teams mapping".</span></span>
1. <span data-ttu-id="3f16c-113">Wählen Sie im Inforegister **Ausgewählte Entitäten** **Entität hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="3f16c-113">On the **Selected entities** FastTab, select **Add entity**.</span></span> <span data-ttu-id="3f16c-114">Das Dialogfeld **Entität hinzufügen** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3f16c-114">The **Add entity** dialog box appears.</span></span>  
1. <span data-ttu-id="3f16c-115">Wählen Sie aus der Dropdownliste **Entitätsname** **Teams-Zuordnung zwischen Quelle und Team** aus.</span><span class="sxs-lookup"><span data-stu-id="3f16c-115">In the **Entity name** drop-down list, select **Teams mapping between source and team**.</span></span>
1. <span data-ttu-id="3f16c-116">Wählen Sie in der Dropdownliste **Zieldatenformat** **CSV** aus.</span><span class="sxs-lookup"><span data-stu-id="3f16c-116">In the **Target data format** drop-down list, select **CSV**.</span></span>
1. <span data-ttu-id="3f16c-117">Wählen Sie **Hinzufügen** und anschließend **Schließen** aus.</span><span class="sxs-lookup"><span data-stu-id="3f16c-117">Select **Add**, and then select **Close**.</span></span>
1. <span data-ttu-id="3f16c-118">Wählen Sie oben links im Aktivitätsbereich **Jetzt exportieren** aus.</span><span class="sxs-lookup"><span data-stu-id="3f16c-118">On the top left under the Action Pane, select **Export now**.</span></span>
1. <span data-ttu-id="3f16c-119">Wählen Sie unter **Verarbeitungsstatus der Entität** **Datei herunterladen** aus.</span><span class="sxs-lookup"><span data-stu-id="3f16c-119">Under **Entity processing status**, select **Download file**.</span></span>
1. <span data-ttu-id="3f16c-120">Geben Sie in der exportierten CSV-Datei Werte für **SOURCETYE**, **SOURCEID** und **TEAMID** wie folgt ein:</span><span class="sxs-lookup"><span data-stu-id="3f16c-120">In the exported CSV file, enter values for **SOURCETYPE**, **SOURCEID**, and **TEAMID** as follows:</span></span>
    - <span data-ttu-id="3f16c-121">Geben Sie für **SOURCETYPE** „RetailStore“ ein.</span><span class="sxs-lookup"><span data-stu-id="3f16c-121">For **SOURCETYPE**, enter "RetailStore".</span></span> 
    - <span data-ttu-id="3f16c-122">Geben Sie als **SOURCEID** die Shopnummer ein (z. B. „000135“ für den Shop in San Francisco).</span><span class="sxs-lookup"><span data-stu-id="3f16c-122">For **SOURCEID**, enter the store number (for example, "000135" for the San Francisco store).</span></span> <span data-ttu-id="3f16c-123">Geschäftsnummern finden Sie unter **Einzelhandel und Handel \> Kanäle \> Shops**.</span><span class="sxs-lookup"><span data-stu-id="3f16c-123">You can find store numbers at **Retail and Commerce \> Channels \> Stores**.</span></span>
    - <span data-ttu-id="3f16c-124">Geben Sie als **TEAMID** die entsprechende Team-ID aus Microsoft Teams ein (z. B. „5f8bc92b-6aa8-451e-85d1-3949c01ddc6c“).</span><span class="sxs-lookup"><span data-stu-id="3f16c-124">For **TEAMID**, enter the corresponding team ID from Microsoft Teams (for example, "5f8bc92b-6aa8-451e-85d1-3949c01ddc6c").</span></span> <span data-ttu-id="3f16c-125">Informationen zur Team-ID finden Sie unter [admin.teams.microsoft.com](https://admin.teams.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="3f16c-125">You can find team ID information at [admin.teams.microsoft.com](https://admin.teams.microsoft.com).</span></span>
1. <span data-ttu-id="3f16c-126">Speichern Sie die CSV-Datei auf Ihrem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="3f16c-126">Save the CSV file to your local machine.</span></span>
1. <span data-ttu-id="3f16c-127">Gehen Sie zu **Systemverwaltung \> Arbeitsbereich \> Datenverwaltung** und wählen Sie dann **Importieren**.</span><span class="sxs-lookup"><span data-stu-id="3f16c-127">Go to **System Administration \> Workspace \> Data management**, and then select **Import**.</span></span>
1. <span data-ttu-id="3f16c-128">Wählen Sie im Inforegister **Ausgewählte Entitäten** **Datei hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="3f16c-128">On the **Selected entities** FastTab, select **Add file**.</span></span> <span data-ttu-id="3f16c-129">Das Dialogfeld **Datei hinzufügen** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3f16c-129">The **Add file** dialog box appears.</span></span>
1. <span data-ttu-id="3f16c-130">Wählen Sie aus der Dropdownliste **Entitätsname** **Teams-Zuordnung zwischen Quelle und Team** aus.</span><span class="sxs-lookup"><span data-stu-id="3f16c-130">In the **Entity name** drop-down list, select **Teams mapping between source and team**.</span></span>
1. <span data-ttu-id="3f16c-131">Wählen Sie in der Dropdownliste **Quelldatenformat** **CSV** aus.</span><span class="sxs-lookup"><span data-stu-id="3f16c-131">In the **Source data format** drop-down list, select **CSV**.</span></span>
1. <span data-ttu-id="3f16c-132">Wählen Sie **Hochladen und hinzufügen**. Wählen Sie dann die CSV-Datei aus, die Sie zuvor gespeichert haben, und wählen Sie **Öffnen** aus.</span><span class="sxs-lookup"><span data-stu-id="3f16c-132">Select **Upload and add**, select the CSV file that you saved previously, and then select **Open**.</span></span>
1. <span data-ttu-id="3f16c-133">Wählen Sie im Dialogfeld **Datei hinzufügen** **Schließen** aus.</span><span class="sxs-lookup"><span data-stu-id="3f16c-133">In the **Add file** dialog box, select **Close**.</span></span>
1. <span data-ttu-id="3f16c-134">Wählen Sie im Aktivitätsbereich **Speichern** und dann **Importieren**.</span><span class="sxs-lookup"><span data-stu-id="3f16c-134">On the Action Pane, select **Save** , and then select **Import**.</span></span>

<span data-ttu-id="3f16c-135">Das folgende Beispielbild zeigt Gruppe **Teams-Zuordnung exportieren** in Commerce. Die Elemente **Entität hinzufügen** und die Kopfzeilen der exportierten CSV-Datei sind hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="3f16c-135">The following example image shows the **Export teams mapping** group in Commerce with **Add entity** elements and the exported CSV file headers highlighted.</span></span>

![Gruppe „Teams-Zuordnung exportieren“ in Commerce, Elemente „Entität hinzufügen“ und Kopfzeilen der exportierten CSV-Datei hervorgehoben](media/d365-commerce-data-mgmt-export-entity.png)

> [!NOTE]
> <span data-ttu-id="3f16c-137">Befolgen Sie nach Abschluss der vorherigen Schritte die Schritte in [Aufgabenverwaltung zwischen Microsoft Teams und POS synchronisieren](synchronize-tasks-teams-pos.md), um die Aufgabenverwaltung zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="3f16c-137">After you complete the preceeding steps, follow the steps in [Synchronize task management between Microsoft Teams and POS](synchronize-tasks-teams-pos.md) to synchronize task management.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="3f16c-138">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="3f16c-138">Additional resources</span></span>

[<span data-ttu-id="3f16c-139">Überblick Integration Dynamics 365 Commerce und Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="3f16c-139">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="3f16c-140">Integration von Dynamics 365 Commerce und Microsoft Teams aktivieren</span><span class="sxs-lookup"><span data-stu-id="3f16c-140">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="3f16c-141">Microsoft Teams aus Dynamics 365 Commerce bereitstellen</span><span class="sxs-lookup"><span data-stu-id="3f16c-141">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="3f16c-142">Aufgabenverwaltung zwischen Microsoft Teams und Dynamics 365 Commerce POS synchronisieren</span><span class="sxs-lookup"><span data-stu-id="3f16c-142">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="3f16c-143">Benutzerrollen in Microsoft Teams verwalten</span><span class="sxs-lookup"><span data-stu-id="3f16c-143">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="3f16c-144">Integration von Dynamics 365 Commerce und Microsoft Teams – FAQ</span><span class="sxs-lookup"><span data-stu-id="3f16c-144">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
