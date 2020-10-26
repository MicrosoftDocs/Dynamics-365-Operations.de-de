---
title: Erstellen neuer Benutzer
description: Benutzer sind interne Mitarbeiter der Organisation oder externe Debitoren und Kreditoren, die Zugriff auf Microsoft Dynamics AX anfordern, ihre Einzelvorgänge auszuführen.
author: maertenm
manager: AnnBe
ms.date: 06/08/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5e84130ff2b1cf83b7d2b95eefc72175dc57743c
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982501"
---
# <a name="create-new-users"></a><span data-ttu-id="48a90-103">Erstellen neuer Benutzer</span><span class="sxs-lookup"><span data-stu-id="48a90-103">Create new users</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="48a90-104">Benutzer sind interne Mitarbeiter der Organisation oder externe Debitoren und Kreditoren, die Zugriff auf das System anfordern, um ihre Einzelvorgänge auszuführen.</span><span class="sxs-lookup"><span data-stu-id="48a90-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to do their jobs.</span></span>

## <a name="associate-a-user-with-a-license-new-license-types-only"></a><span data-ttu-id="48a90-105">Zuordnen eines Benutzers zu einer Lizenz (nur neue Lizenztypen)</span><span class="sxs-lookup"><span data-stu-id="48a90-105">Associate a user with a license (new license types only)</span></span>
<span data-ttu-id="48a90-106">Für Debitoren mit einem der neuen Lizenztypen, die im Oktober 2019 hinzugefügt wurden, müssen Benutzern eine Lizenz zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="48a90-106">For customers who are on one of the new license types that were added in October 2019, users must be associated with a license.</span></span> <span data-ttu-id="48a90-107">Benutzer, die einer Lizenz zugeordnet sind, werden automatisch als Systembenutzer hinzugefügt, die bei der ersten Anmeldung keine Rollen haben.</span><span class="sxs-lookup"><span data-stu-id="48a90-107">Users who are associated with a license are automatically added as system users who have no roles the first time that they sign in.</span></span>

<span data-ttu-id="48a90-108">Systemadministratoren können [Benutzern Lizenzen zuordnen](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) – im [Microsoft 365 Admin Center](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="48a90-108">System admins can [assign licenses to users](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) in the [Microsoft 365 admin center](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span></span>

## <a name="associate-an-external-user-with-a-license-new-license-types-only"></a><span data-ttu-id="48a90-109">Zuordnen eines externen Benutzers zu einer Lizenz (nur neue Lizenztypen)</span><span class="sxs-lookup"><span data-stu-id="48a90-109">Associate an external user with a license (new license types only)</span></span>
<span data-ttu-id="48a90-110">Benutzer außerhalb des Mandanten, in dem die Umgebung bereitgestellt wurde, müssen im Host-Mandantenverzeichnis vertreten sein ( Azure Active Directory ( Azure AD)), damit ihnen Lizenzen zugewiesen werden können.</span><span class="sxs-lookup"><span data-stu-id="48a90-110">Users external to the tenant that the environment was deployed into need to be represented in the host tenant directory (Azure Active Directory (Azure AD)) so that they can be assigned licenses.</span></span> <span data-ttu-id="48a90-111">Diese externen Benutzer sollten dem Mandanten in Azure AD als Gastbenutzer hinzugefügt werden und dann sollten ihnen die entsprechenden Lizenzen zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="48a90-111">Those external users should be added to the tenant in Azure AD as guest users and then assigned the appropriate licenses.</span></span> <span data-ttu-id="48a90-112">Weitere Informationen finden Sie unter [Azure Active Directory Benutzer der B2B-Zusammenarbeit im Azure-Portal hinzufügen](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).</span><span class="sxs-lookup"><span data-stu-id="48a90-112">For more information, see [Add Azure Active Directory B2B collaboration users in the Azure portal](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).</span></span>

## <a name="add-a-new-user"></a><span data-ttu-id="48a90-113">Hinzufügen eines neuen Benutzers</span><span class="sxs-lookup"><span data-stu-id="48a90-113">Add a new user</span></span>
1. <span data-ttu-id="48a90-114">Wechseln Sie zu **Systemverwaltung \> Benutzer \> Benutzer**.</span><span class="sxs-lookup"><span data-stu-id="48a90-114">Go to **System administration \> Users \> Users**.</span></span>
2. <span data-ttu-id="48a90-115">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="48a90-115">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="48a90-116">Geben Sie im Feld **Benutzerkennung** eine eindeutige Kennung für den Benutzer ein.</span><span class="sxs-lookup"><span data-stu-id="48a90-116">In the **User ID** field, enter a unique identifier for the user.</span></span> <span data-ttu-id="48a90-117">Geben Sie ein Kennwort ein.</span><span class="sxs-lookup"><span data-stu-id="48a90-117">A user ID is required.</span></span>  
4. <span data-ttu-id="48a90-118">Geben Sie im Feld **Benutzername** den Namen des Benutzers ein.</span><span class="sxs-lookup"><span data-stu-id="48a90-118">In the **User name** field, enter the user's name.</span></span>  
5. <span data-ttu-id="48a90-119">Geben Sie im Feld **Domain** die Domäne des Benutzers ein.</span><span class="sxs-lookup"><span data-stu-id="48a90-119">In the **Domain** field, enter the user's domain.</span></span>  
6. <span data-ttu-id="48a90-120">Geben Sie im Feld **Alias** den Alias des Benutzers ein.</span><span class="sxs-lookup"><span data-stu-id="48a90-120">In the **Alias** field, enter the user's alias.</span></span>  
7. <span data-ttu-id="48a90-121">Wählen Sie im Feld **Unternehmen** das gewünschte Unternehmen aus.</span><span class="sxs-lookup"><span data-stu-id="48a90-121">In the **Company** field, select the desired company.</span></span> 
8. <span data-ttu-id="48a90-122">Wählen Sie im Inforegister **Benutzerrollen** die Option **Rollen zuweisen** aus, um Sicherheitsrollen zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="48a90-122">On the **User's roles** FastTab, select **Assign roles** to assign users to security roles.</span></span> <span data-ttu-id="48a90-123">Ausführlichere Informationen finden Sie unter [Zuweisen von Benutzern zu Sicherheitsrollen](assign-users-security-roles.md).</span><span class="sxs-lookup"><span data-stu-id="48a90-123">For more information, see [Assign users to security roles](assign-users-security-roles.md).</span></span>
9. <span data-ttu-id="48a90-124">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="48a90-124">Select **OK**.</span></span>
10. <span data-ttu-id="48a90-125">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="48a90-125">Select **Save**.</span></span>

## <a name="import-users"></a><span data-ttu-id="48a90-126">Benutzer importieren</span><span class="sxs-lookup"><span data-stu-id="48a90-126">Import users</span></span>
1. <span data-ttu-id="48a90-127">Wechseln Sie zu **Systemverwaltung \> Benutzer \> Benutzer**.</span><span class="sxs-lookup"><span data-stu-id="48a90-127">Go to **System administration \> Users \> Users**.</span></span>
2. <span data-ttu-id="48a90-128">Wählen Sie im Aktivitätsbereich **Benutzer importieren** aus.</span><span class="sxs-lookup"><span data-stu-id="48a90-128">On the Action Pane, select **Import users**.</span></span>
3. <span data-ttu-id="48a90-129">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="48a90-129">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="48a90-130">Wählen Sie **Benutzer importieren** aus.</span><span class="sxs-lookup"><span data-stu-id="48a90-130">Select **Import users**.</span></span>
5. <span data-ttu-id="48a90-131">Wählen Sie **Schließen** aus.</span><span class="sxs-lookup"><span data-stu-id="48a90-131">Select **Close**.</span></span>

