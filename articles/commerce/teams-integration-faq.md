---
title: Integration von Dynamics 365 Commerce und Microsoft Teams – FAQ
description: Dieses Thema enthält Antworten auf häufig gestellte Fragen zur Integration von Microsoft Dynamics 365 Commerce und Microsoft Teams.
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
ms.openlocfilehash: bf9aebb1c8ba7cf4fee3f0471a10872de1e23ce6
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908855"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-faq"></a><span data-ttu-id="ee672-103">Integration von Dynamics 365 Commerce und Microsoft Teams – FAQ</span><span class="sxs-lookup"><span data-stu-id="ee672-103">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ee672-104">Dieses Thema enthält Antworten auf häufig gestellte Fragen zur Integration von Microsoft Dynamics 365 Commerce und Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="ee672-104">This topic provides answers to frequently asked questions regarding Microsoft Dynamics 365 Commerce and Microsoft Teams integration.</span></span>

### <a name="who-in-the-store-becomes-an-owner-of-a-team-while-provisioning-teams-from-commerce"></a><span data-ttu-id="ee672-105">Wer im Shop wird Besitzer eines Teams, wenn Teams aus Commerce bereitgestellt werden?</span><span class="sxs-lookup"><span data-stu-id="ee672-105">Who in the store becomes an owner of a team while provisioning Teams from Commerce?</span></span> 

<span data-ttu-id="ee672-106">Alle Filialleiter werden automatisch als Besitzer zur entsprechenden Teamgruppe hinzugefügt, damit sie Vorgänge wie das Hinzufügen eines privaten Kanals und das Hinzufügen oder Löschen von Mitgliedern ausführen können.</span><span class="sxs-lookup"><span data-stu-id="ee672-106">All store managers are automatically added as owners to the corresponding team group so that they can perform operations such as adding a private channel and adding or deleting members.</span></span> 

### <a name="how-do-i-assign-the-communications-manager-role-to-an-employee-in-commerce-headquarters"></a><span data-ttu-id="ee672-107">Wie ordne ich einem Mitarbeiter in der Commerce-Zentralverwaltung die Rolle „Kommunikationsmanager“ zu?</span><span class="sxs-lookup"><span data-stu-id="ee672-107">How do I assign the "communications manager" role to an employee in Commerce headquarters?</span></span> 

<span data-ttu-id="ee672-108">Kommunikationsmanager können in Microsoft Teams Aufgabenlisten erstellen und veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="ee672-108">Communication managers in Microsoft Teams have the ability to create and publish task lists.</span></span> <span data-ttu-id="ee672-109">Organisationsmitarbeiter, die Kommunikationsmanager werden müssen, muss die Rolle des „Retail Task Managers“ in der Commerce-Zentralverwaltung zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="ee672-109">Organization employees who need to become communication managers must have the "retail task manager" role assigned to them in Commerce headquarters.</span></span>

<span data-ttu-id="ee672-110">Führen Sie die folgenden Schritte aus, um einem Mitarbeiter in der Commerce-Zentralverwaltung die Rolle des Retails Task Managers zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="ee672-110">To assign the retail task manager role to an employee in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="ee672-111">Gehen Sie zu **Retail and Commerce \> Mitarbeiter \> Benutzer**.</span><span class="sxs-lookup"><span data-stu-id="ee672-111">Go to **Retail and Commerce \> Employees \> Users**.</span></span>
1. <span data-ttu-id="ee672-112">Wählen Sie einen Mitarbeiter aus.</span><span class="sxs-lookup"><span data-stu-id="ee672-112">Select an employee.</span></span>
1. <span data-ttu-id="ee672-113">Wählen Sie auf der Registerkarte **Rollen des Benutzers** **Rollen zuweisen**.</span><span class="sxs-lookup"><span data-stu-id="ee672-113">On the **User's roles** FastTab, select **Assign roles**.</span></span>
1. <span data-ttu-id="ee672-114">Wählen Sie im Dialogfenster **Rollen zu Benutzer** die Rolle **Retail Task Manager** und dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="ee672-114">In the **Assign roles to user** dialog box, select the **Retail task manager** role, and then select **OK**.</span></span>

### <a name="how-do-i-make-a-specific-organization-hierarchy-available-to-upload-into-microsoft-teams"></a><span data-ttu-id="ee672-115">Wie stelle ich eine bestimmte Organisationshierarchie zum Hochladen in Microsoft Teams zur Verfügung?</span><span class="sxs-lookup"><span data-stu-id="ee672-115">How do I make a specific organization hierarchy available to upload into Microsoft Teams?</span></span>

<span data-ttu-id="ee672-116">In der Commerce-Zentralverwaltung ist die Hierarchie jeder Organisation einem oder mehreren Zwecken zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="ee672-116">In Commerce headquarters, every organization's hierarchy is associated with one or more purposes.</span></span> <span data-ttu-id="ee672-117">Stellen Sie sicher, dass der Hierarchie, die Sie in Microsoft Teams bereitstellen möchten, der Zweck **Einzelhandelsberichterstellung** wie im folgenden Beispielbild gezeigt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ee672-117">Make sure the hierarchy that you want to provision into Microsoft Teams has the **Retail reporting** purpose associated with it, as shown in the following example image.</span></span> 

![Beispiel für einen Organisationshierarchiezweck in der Commerce-Zentralverwaltung](media/d365-commerce-organization-hierarchies-purpose.png)

### <a name="how-do-i-enable-retail-store-workers-to-sign-in-to-commerce-point-of-sale-pos-using-azure-active-directory-azure-ad"></a><span data-ttu-id="ee672-119">Wie kann ich Mitarbeitern von Einzelhandelsgeschäften ermöglichen, sich bei Commerce Point of Sale (POS) mit Azure Active Directory (Azure AD) anzumelden?</span><span class="sxs-lookup"><span data-stu-id="ee672-119">How do I enable retail store workers to sign in to Commerce point of sale (POS) using Azure Active Directory (Azure AD)?</span></span>

<span data-ttu-id="ee672-120">Informationen zum Konfigurieren der zu verwendenden Commerce POS-Anmeldeumgebung zur Verwendung der Azure AD-Authentifizierung finden Sie unter [Azure Active Directory-Authentifizierung bei POS-Anmeldung aktivieren](aad-pos-logon.md).</span><span class="sxs-lookup"><span data-stu-id="ee672-120">For information about how to configure the Commerce POS sign-in experience to use Azure AD authentication, see [Enable Azure Active Directory authentication for POS sign-in](aad-pos-logon.md).</span></span>

### <a name="how-do-i-map-stores-and-corresponding-teams-in-commerce-headquarters-if-my-organization-has-already-created-teams-in-microsoft-teams"></a><span data-ttu-id="ee672-121">Wie ordne ich Shops und entsprechende Teams in der Commerce-Zentralverwaltung zu, wenn meine Organisation bereits Teams in Microsoft Teams erstellt hat?</span><span class="sxs-lookup"><span data-stu-id="ee672-121">How do I map stores and corresponding teams in Commerce headquarters if my organization has already created teams in Microsoft Teams?</span></span>

<span data-ttu-id="ee672-122">Informationen zum Zuordnen von Shops und Teams, wenn bereits Teams vorhanden sind, finden Sie unter [Shops und entsprechende Teams zuordnen, wenn in Ihrer Organisation bereits Teams Microsoft Teams vorhanden sind](map-stores-existing-teams.md).</span><span class="sxs-lookup"><span data-stu-id="ee672-122">For information on how to map stores and teams if there are pre-existing teams, see [Map stores and corresponding teams if your organization has pre-existing teams in Microsoft Teams](map-stores-existing-teams.md).</span></span>

### <a name="how-do-i-clear-the-microsoft-graph-api-token-stored-in-the-session-storage"></a><span data-ttu-id="ee672-123">Wie lösche ich das im Sitzungsspeicher gespeicherte Microsoft Graph API-Token?</span><span class="sxs-lookup"><span data-stu-id="ee672-123">How do I clear the Microsoft Graph API token stored in the session storage?</span></span>

<span data-ttu-id="ee672-124">Ein Benutzer, der sich am Point of Sale (POS) mit einem Azure Active Directory (Azure AD) Konto angemeldet hat, sollte sich vom POS abmelden oder die Anwendung schließen, um den Sitzungsspeicher zu löschen.</span><span class="sxs-lookup"><span data-stu-id="ee672-124">A user who has signed in to the point of sale (POS) with an Azure Active Directory (Azure AD) account should sign out from the POS or close the application to clear the session storage.</span></span> 

> [!TIP]
> <span data-ttu-id="ee672-125">Es hat sich bewährt, dass die Mitarbeiter des Shops das POS-Terminal immer sperren oder sich von einer Sitzung abmelden, wenn sie das Terminal nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="ee672-125">A recommended best practice is to always have store workers lock the POS terminal or sign out from a session when not using the terminal.</span></span> 

### <a name="what-happens-if-a-store-doesnt-have-store-managers"></a><span data-ttu-id="ee672-126">Was passiert, wenn ein Shop keinen Filialleiter hat?</span><span class="sxs-lookup"><span data-stu-id="ee672-126">What happens if a store doesn't have store managers?</span></span>

<span data-ttu-id="ee672-127">Wenn ein Shop keinen Leiter hat, wird keine Teamgruppe für das Shop oder in Teams erstellt.</span><span class="sxs-lookup"><span data-stu-id="ee672-127">If a store doesn't have managers, a team group will not be created for the store or in Teams.</span></span> 

### <a name="what-happens-if-a-store-manager-leaves-the-company"></a><span data-ttu-id="ee672-128">Was passiert, wenn ein Filialleiter das Unternehmen verlässt?</span><span class="sxs-lookup"><span data-stu-id="ee672-128">What happens if a store manager leaves the company?</span></span>

<span data-ttu-id="ee672-129">Jeder mit der Besitzerrolle kann einen neuen Filialleiter in der Commerce-Zentralverwaltung hinzufügen und Teams erneut bereitstellen, damit der neue Leiter über die erforderlichen Berechtigungen in Teams für die Gruppe verfügt.</span><span class="sxs-lookup"><span data-stu-id="ee672-129">Anyone with the owner role can add a new store manager in Commerce headquarters and reprovision Teams so that the new manager will have the necessary privileges in Teams for the group.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="ee672-130">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ee672-130">Additional resources</span></span>

[<span data-ttu-id="ee672-131">Überblick Integration Dynamics 365 Commerce und Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="ee672-131">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="ee672-132">Integration von Dynamics 365 Commerce und Microsoft Teams aktivieren</span><span class="sxs-lookup"><span data-stu-id="ee672-132">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="ee672-133">Microsoft Teams aus Dynamics 365 Commerce bereitstellen</span><span class="sxs-lookup"><span data-stu-id="ee672-133">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="ee672-134">Aufgabenverwaltung zwischen Microsoft Teams und Dynamics 365 Commerce POS synchronisieren</span><span class="sxs-lookup"><span data-stu-id="ee672-134">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="ee672-135">Benutzerrollen in Microsoft Teams verwalten</span><span class="sxs-lookup"><span data-stu-id="ee672-135">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="ee672-136">Shops und Teams zuordnen, wenn in Microsoft Teams bereits Teams vorhanden sind</span><span class="sxs-lookup"><span data-stu-id="ee672-136">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)
