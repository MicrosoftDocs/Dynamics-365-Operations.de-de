---
title: Microsoft Teams aus Dynamics 365 Commerce bereitstellen
description: In diesem Thema wird Sie Microsoft Teams durch die Verwendung von Organisationsdaten aus Dynamics 365 Commerce bereitstellen.
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
ms.openlocfilehash: 96382c072e03506294d72899072a358091bda8ab
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842673"
---
# <a name="provision-microsoft-teams-from-dynamics-365-commerce"></a><span data-ttu-id="aca38-103">Microsoft Teams aus Dynamics 365 Commerce bereitstellen</span><span class="sxs-lookup"><span data-stu-id="aca38-103">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="aca38-104">In diesem Thema wird Sie Microsoft Teams durch die Verwendung von Organisationsdaten aus Dynamics 365 Commerce bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="aca38-104">This topic describes how to provision Microsoft Teams by using organizational data from Dynamics 365 Commerce.</span></span>

<span data-ttu-id="aca38-105">Dynamics 365 Commerce bietet eine einfache Möglichkeit, Teams bereitzustellen, wenn Sie dort noch keine Teams für Ihre Einzelhandelsgeschäfte eingerichtet haben.</span><span class="sxs-lookup"><span data-stu-id="aca38-105">Dynamics 365 Commerce offers an easy way to provision Teams if you haven't yet set up teams for your retail stores there.</span></span> <span data-ttu-id="aca38-106">Indem Sie genau definierte Informationen aus Commerce nutzen, die Sie in Teams verwenden möchten, können Sie Ihren Filialmitarbeitern den Einstieg in Teams erleichtern.</span><span class="sxs-lookup"><span data-stu-id="aca38-106">By taking advantage of well-defined information from Commerce that you want to use in Teams, you can help your store employees get started in Teams.</span></span> <span data-ttu-id="aca38-107">Diese Informationen umfassen die Organisationshierarchie, Geschäftsnamen, Mitarbeiterinformationen und Azure Active Directory-Konten (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="aca38-107">This information includes the organizational hierarchy, store names, employee information, and Azure Active Directory (Azure AD) accounts.</span></span> 

<span data-ttu-id="aca38-108">Der Prozess der Bereitstellung von Teams besteht aus zwei Hauptschritten:</span><span class="sxs-lookup"><span data-stu-id="aca38-108">The process of provisioning Teams has two main steps:</span></span>

1. <span data-ttu-id="aca38-109">Erstellen Sie in Teams ein Team für jedes Einzelhandelsgeschäft und fügen Sie Filialmitarbeiter als Mitglieder des entsprechenden Teams hinzu.</span><span class="sxs-lookup"><span data-stu-id="aca38-109">In Teams, create a team for each retail store, and add store workers as members of the appropriate team.</span></span> <span data-ttu-id="aca38-110">Wenn ein Mitarbeiter mit mehr als einem Einzelhandelsgeschäft verbunden ist, spiegelt die Teammitgliedschaft diese Tatsache wider.</span><span class="sxs-lookup"><span data-stu-id="aca38-110">If an employee is associated with more than one retail store, team membership will reflect that fact.</span></span> <span data-ttu-id="aca38-111">Ein Kommunikationsteam, dem Regionalmanager als Mitglieder angehören, wird erstellt, um die Veröffentlichung von Aufgaben aus Teams zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="aca38-111">A communications team that includes regional managers as members will be created to help publish tasks from Teams.</span></span>
1. <span data-ttu-id="aca38-112">Laden Sie Ihre Organisationshierarchie von Commerce in Teams hoch.</span><span class="sxs-lookup"><span data-stu-id="aca38-112">Upload your organizational hierarchy from Commerce to Teams.</span></span>

## <a name="provision-teams-in-commerce-headquarters"></a><span data-ttu-id="aca38-113">Teams in der Commerce-Zentralverwaltung bereitstellen</span><span class="sxs-lookup"><span data-stu-id="aca38-113">Provision Teams in Commerce headquarters</span></span>

<span data-ttu-id="aca38-114">Bevor Sie Microsoft Teams bereitstellen führen Sie die folgenden Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="aca38-114">Before you provision Microsoft Teams, complete these tasks:</span></span>

- <span data-ttu-id="aca38-115">Bestätigen Sie, dass alle Regionalmanager zu Kommunikationsmanagern ernannt wurden.</span><span class="sxs-lookup"><span data-stu-id="aca38-115">Confirm that all regional managers have been made communications managers.</span></span>
- <span data-ttu-id="aca38-116">Stellen Sie sicher, dass das Azure-Konto jedes Filialleiters und Worker mit dem Arbeitsdatensatz dieses Managers oder Workers in der Commerce-Zentralverwaltung verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="aca38-116">Confirm that the Azure account of every store manager and worker has been associated with that manager's or worker's worker record in Commerce headquarters.</span></span>

<span data-ttu-id="aca38-117">Führen Sie die folgenden Schritte aus, um Teams in der Commerce-Zentralverwaltung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="aca38-117">To provision Teams in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="aca38-118">Gehen Sie zu **Einzelhandel und Handel \> Kanaleinstellungen \> Microsoft Teams Integrationskonfiguration**.</span><span class="sxs-lookup"><span data-stu-id="aca38-118">Go to **Retail and Commerce \> Channel setup \> Microsoft Teams Integration Configuration**.</span></span>
1. <span data-ttu-id="aca38-119">Wählen Sie im Aktivitätsbereich **Teams bereitstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="aca38-119">On the Action Pane, select **Provision teams**.</span></span> <span data-ttu-id="aca38-120">Ein Stapelverarbeitungsauftrag mit Namen **Teams bereitstellen** wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="aca38-120">A batch job that is named **Teams provision** is created.</span></span>
1. <span data-ttu-id="aca38-121">Gehen Sie zu **Systemadministration \> Anfragen \> Stapelverarbeitungsaufträge** und finden Sie den neuesten Auftrag mit der Beschreibung **Teams-Bereitstellung**.</span><span class="sxs-lookup"><span data-stu-id="aca38-121">Go to **System administration \> Inquiries \> Batch jobs**, and find the most recent job that has the description **Teams provision**.</span></span> <span data-ttu-id="aca38-122">Warten Sie, bis dieser Auftrag ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="aca38-122">Wait until this job has finished running.</span></span>

> [!TIP]
> <span data-ttu-id="aca38-123">Wenn keinem Ihrer Regionalmanager, Filialleiter und Geschäftsmitarbeiter eine Teams-Lizenz zugeordnet wurde, wird möglicherweise die folgende Fehlermeldung angezeigt: „Anwendbare Sku-Kategorien für den Benutzer konnten nicht abgerufen werden.“</span><span class="sxs-lookup"><span data-stu-id="aca38-123">If none of your regional managers, store managers, and store workers have been associated with a Teams license, you might receive the following error message: "Failed to retrieve appliable Sku categories for the user."</span></span> <span data-ttu-id="aca38-124">Wählen Sie, um das Problem zu beheben, im Aktivitätsbereich **Teams und Mitglieder synchronisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="aca38-124">To correct the issue, select **Sync teams and members** on the Action Pane.</span></span>

<!-- ![Dynamics 365 Commerce - Teams integration configuration](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)-->

## <a name="validate-teams-provisioning-in-the-teams-admin-center"></a><span data-ttu-id="aca38-125">Teams-Bereitstellung im Teams Admin Center überprüfen</span><span class="sxs-lookup"><span data-stu-id="aca38-125">Validate Teams provisioning in the Teams admin center</span></span>

<span data-ttu-id="aca38-126">Um die Microsoft Teams-Bereitstellung im Microsoft Teams Admin Center zu überprüfen, befolgen Sie diese Schritte.</span><span class="sxs-lookup"><span data-stu-id="aca38-126">To validate Microsoft Teams provisioning in the Microsoft Teams admin center, follow these steps.</span></span>
    
1. <span data-ttu-id="aca38-127">Gehen Sie zum [Teams Admin Center](https://admin.teams.microsoft.com/) und melden Sie sich als Administrator Ihres E-Commerce-Mandanten an.</span><span class="sxs-lookup"><span data-stu-id="aca38-127">Go to the [Teams admin center](https://admin.teams.microsoft.com/), and sign in as the administrator of your e-commerce tenant.</span></span>
1. <span data-ttu-id="aca38-128">Wählen Sie im linken Navigationsbereich **Teams** aus, um es zu erweitern, und wählen Sie dann **Teams verwalten** aus.</span><span class="sxs-lookup"><span data-stu-id="aca38-128">In the left navigation pane, select **Teams** to expand it, and then select **Manage teams**.</span></span>
1. <span data-ttu-id="aca38-129">Bestätigen Sie, dass für jedes Commerce-Einzelhandelsgeschäft ein Team erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="aca38-129">Confirm that one team has been created for each Commerce retail store.</span></span>
1. <span data-ttu-id="aca38-130">Wählen Sie ein Team aus und bestätigen Sie, dass Filialmitarbeiter als Mitglieder hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="aca38-130">Select a team, and confirm that store workers have been added to it as members.</span></span>
1. <span data-ttu-id="aca38-131">Wählen Sie im linken Navigationsbereich **Benutzer** aus und bestätigen Sie, dass alle Filialmitarbeiter in allen Filialen als Benutzer hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="aca38-131">In the left navigation pane, select **Users**, and confirm that all store employees in all stores have been added as users.</span></span>

<span data-ttu-id="aca38-132">Die folgende Abbildung zeigt ein Beispiel für die Seite **Teams verwalten** im Team Admin Center.</span><span class="sxs-lookup"><span data-stu-id="aca38-132">The following illustration shows an example of the **Manage teams** page in the Teams admin center.</span></span>

![Beispiel für die Seite „Teams verwalten“ im Teams Admin Center](media/Teams-FLW-Admin-Teams.png)

## <a name="upload-a-commerce-organizational-hierarchy-to-teams"></a><span data-ttu-id="aca38-134">Eine Commerce-Organisationshierarchie in Teams hochladen</span><span class="sxs-lookup"><span data-stu-id="aca38-134">Upload a Commerce organizational hierarchy to Teams</span></span>
    
<span data-ttu-id="aca38-135">Die Commerce-Organisationshierarchie kann in Microsoft Teams verwendet werden, um Aufgaben in allen oder ausgewählten Geschäften zu veröffentlichen, die dieselbe Hierarchiestruktur verwenden.</span><span class="sxs-lookup"><span data-stu-id="aca38-135">The Commerce organizational hierarchy can be used in Microsoft Teams to publish tasks to all or selected stores that use the same hierarchy structure.</span></span>

<span data-ttu-id="aca38-136">Um eine Commerce-Organisationshierarchie in Teams hochzuladen, folgen Sie diesen Schritten.</span><span class="sxs-lookup"><span data-stu-id="aca38-136">To upload a Commerce organizational hierarchy to Teams, follow these steps.</span></span>
    
1. <span data-ttu-id="aca38-137">Gehen Sie in der Commerce-Zentralverwaltung zu **Einzelhandel und Handel \> Kanaleinstellungen \> Microsoft Teams-Integrationskonfiguration**.</span><span class="sxs-lookup"><span data-stu-id="aca38-137">In Commerce headquarters, go to **Retail and Commerce \> Channel setup \> Microsoft Teams Integration Configuration**.</span></span>
1. <span data-ttu-id="aca38-138">Wählen Sie **Adressierungshierarchie herunterladen** und dann **Einzelhandelsgeschäfte nach Regionen** aus, um die Organisationshierarchie als Datei mit kommagetrennten Werten (CSV-Datei) herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="aca38-138">Select **Download targeting hierarchy**, and then select **Retail Stores by Region** to download a comma-separated values (CSV) file of the organizational hierarchy.</span></span>
1. <span data-ttu-id="aca38-139">Installieren Sie das Microsoft Teams PowerShell-Modul mithilfe der Schritte in [Microsoft Teams Power Shell installieren](https://docs.microsoft.com/microsoftteams/teams-powershell-install).</span><span class="sxs-lookup"><span data-stu-id="aca38-139">Install the Microsoft Teams PowerShell module by following the steps in [Install Microsoft Teams PowerShell](https://docs.microsoft.com/microsoftteams/teams-powershell-install).</span></span>
1. <span data-ttu-id="aca38-140">Wenn Sie im Team PowerShell-Fenster dazu aufgefordert werden, melden Sie sich mit dem Administratorkonto für Ihren Azure AD-Mandanten an.</span><span class="sxs-lookup"><span data-stu-id="aca38-140">When you're prompted in the Teams PowerShell window, sign in by using the administrator account for your Azure AD tenant.</span></span>
1. <span data-ttu-id="aca38-141">Befolgen Sie die Schritte in [Einrichten Ihrer Team-Adressierungshierarchie](https://docs.microsoft.com/microsoftteams/set-up-your-team-hierarchy), um die CSV-Datei für die Adressierungshierarchie hochzuladen.</span><span class="sxs-lookup"><span data-stu-id="aca38-141">Follow the steps in [Set up your team targeting hierarchy](https://docs.microsoft.com/microsoftteams/set-up-your-team-hierarchy) to upload the CSV file for the targeting hierarchy.</span></span>

## <a name="verify-that-the-organizational-hierarchy-was-uploaded-to-teams"></a><span data-ttu-id="aca38-142">Sicherstellen, dass die Organisationshierarchie in Teams hochgeladen wurde</span><span class="sxs-lookup"><span data-stu-id="aca38-142">Verify that the organizational hierarchy was uploaded to Teams</span></span>

<span data-ttu-id="aca38-143">Um sicherzustellen, dass die Organisationshierarchie in Microsoft Teams hochzuladen, gehen Sie wie folgt vor.</span><span class="sxs-lookup"><span data-stu-id="aca38-143">To verify that the organizational hierarchy was uploaded to Microsoft Teams, follow these steps.</span></span>

1. <span data-ttu-id="aca38-144">Melden Sie sich in Teams als Kommunikationsmanager an.</span><span class="sxs-lookup"><span data-stu-id="aca38-144">Sign in to Teams as a communications manager.</span></span>
1. <span data-ttu-id="aca38-145">Wählen Sie im linken Navigationsbereich **Aufgaben aus Planner** aus.</span><span class="sxs-lookup"><span data-stu-id="aca38-145">In the left navigation pane, select **Tasks by Planner**.</span></span>
1. <span data-ttu-id="aca38-146">Erstellen Sie auf der Registerkarte **Veröffentlichte Listen** eine neue Liste mit einer Dummy-Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="aca38-146">On the **Published lists** tab, create a new list that has a dummy task.</span></span>
1. <span data-ttu-id="aca38-147">Wählen Sie **Veröffentlichen** aus.</span><span class="sxs-lookup"><span data-stu-id="aca38-147">Select **Publish**.</span></span> <span data-ttu-id="aca38-148">Die Organisationshierarchie sollte im Dialogfeld **Auswählen, an wen veröffentlicht werden soll** erscheinen wie im Beispiel in der folgenden Abbildung gezeigt.</span><span class="sxs-lookup"><span data-stu-id="aca38-148">The organizational hierarchy should appear in the **Select who to publish to** dialog box, as shown in the example in the following illustration.</span></span>

![Beispiel für eine Organisationshierarchie im Dialogfeld „Auswählen, an wen veröffentlicht werden soll“](media/Microsoft-teams-verify-org-hierarchy.png)

## <a name="additional-resources"></a><span data-ttu-id="aca38-150">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="aca38-150">Additional resources</span></span>

[<span data-ttu-id="aca38-151">Überblick Integration Dynamics 365 Commerce und Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="aca38-151">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="aca38-152">Integration von Dynamics 365 Commerce und Microsoft Teams aktivieren</span><span class="sxs-lookup"><span data-stu-id="aca38-152">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="aca38-153">Aufgabenverwaltung zwischen Microsoft Teams und Dynamics 365 Commerce POS synchronisieren</span><span class="sxs-lookup"><span data-stu-id="aca38-153">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="aca38-154">Benutzerrollen in Microsoft Teams verwalten</span><span class="sxs-lookup"><span data-stu-id="aca38-154">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="aca38-155">Shops und Teams zuordnen, wenn in Microsoft Teams bereits Teams vorhanden sind</span><span class="sxs-lookup"><span data-stu-id="aca38-155">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="aca38-156">Integration von Dynamics 365 Commerce und Microsoft Teams – FAQ</span><span class="sxs-lookup"><span data-stu-id="aca38-156">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
