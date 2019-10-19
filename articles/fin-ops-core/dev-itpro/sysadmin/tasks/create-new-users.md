---
title: Erstellen neuer Benutzer
description: Benutzer sind interne Mitarbeiter der Organisation oder externe Debitoren und Kreditoren, die Zugriff auf Microsoft Dynamics AX anfordern, ihre Einzelvorgänge auszuführen.
author: maertenm
manager: AnnBe
ms.date: 08/30/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4a5635f96132b2e52227b569e7e480fa55e82d61
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180943"
---
# <a name="create-new-users"></a><span data-ttu-id="afad6-103">Erstellen neuer Benutzer</span><span class="sxs-lookup"><span data-stu-id="afad6-103">Create new users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]
[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="afad6-104">Benutzer sind interne Mitarbeiter der Organisation oder externe Debitoren und Kreditoren, die Zugriff auf das System anfordern, um ihre Einzelvorgänge auszuführen.</span><span class="sxs-lookup"><span data-stu-id="afad6-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to do their jobs.</span></span>

## <a name="associate-a-user-with-a-license-new-license-types-only"></a><span data-ttu-id="afad6-105">Zuordnen eines Benutzers zu einer Lizenz (nur neue Lizenztypen)</span><span class="sxs-lookup"><span data-stu-id="afad6-105">Associate a user with a license (new license types only)</span></span>
<span data-ttu-id="afad6-106">Für Debitoren mit einem der neuen Lizenztypen, die im Oktober 2019 hinzugefügt wurden, müssen Benutzern eine Lizenz zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="afad6-106">For customers who are on one of the new license types that were added in October 2019, users must be associated with a license.</span></span> <span data-ttu-id="afad6-107">Benutzer, die einer Lizenz zugeordnet sind, werden automatisch als Systembenutzer hinzugefügt, die bei der ersten Anmeldung keine Rollen haben.</span><span class="sxs-lookup"><span data-stu-id="afad6-107">Users who are associated with a license are automatically added as system users who have no roles the first time that they sign in.</span></span> <span data-ttu-id="afad6-108">Benutzer, denen keine Lizenz zugeordnet ist, erhalten eine Warnmeldung.</span><span class="sxs-lookup"><span data-stu-id="afad6-108">Users who aren't associated with a licence receive a warning message.</span></span>

<span data-ttu-id="afad6-109">Systemadministratoren können [Benutzern Lizenzen zuordnen](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) – im [Microsoft 365 Admin Center](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="afad6-109">System admins can [assign licenses to users](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) in the [Microsoft 365 admin center](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span></span>

## <a name="add-a-new-user"></a><span data-ttu-id="afad6-110">Hinzufügen eines neuen Benutzers</span><span class="sxs-lookup"><span data-stu-id="afad6-110">Add a new user</span></span>
1. <span data-ttu-id="afad6-111">Wechseln Sie zu **Systemverwaltung \> Benutzer \> Benutzer**.</span><span class="sxs-lookup"><span data-stu-id="afad6-111">Go to **System administration \> Users \> Users**.</span></span>
2. <span data-ttu-id="afad6-112">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="afad6-112">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="afad6-113">Geben Sie im Feld **Benutzerkennung** eine eindeutige Kennung für den Benutzer ein.</span><span class="sxs-lookup"><span data-stu-id="afad6-113">In the **User ID** field, enter a unique identifier for the user.</span></span> <span data-ttu-id="afad6-114">Geben Sie ein Kennwort ein.</span><span class="sxs-lookup"><span data-stu-id="afad6-114">A user ID is required.</span></span>  
4. <span data-ttu-id="afad6-115">Geben Sie im Feld **Benutzername** den Namen des Benutzers ein.</span><span class="sxs-lookup"><span data-stu-id="afad6-115">In the **User name** field, enter the user's name.</span></span>  
5. <span data-ttu-id="afad6-116">Geben Sie im Feld **Domain** die Domäne des Benutzers ein.</span><span class="sxs-lookup"><span data-stu-id="afad6-116">In the **Domain** field, enter the user's domain.</span></span>  
6. <span data-ttu-id="afad6-117">Geben Sie im Feld **Alias** den Alias des Benutzers ein.</span><span class="sxs-lookup"><span data-stu-id="afad6-117">In the **Alias** field, enter the user's alias.</span></span>  
7. <span data-ttu-id="afad6-118">Wählen Sie im Feld **Unternehmen** das gewünschte Unternehmen aus.</span><span class="sxs-lookup"><span data-stu-id="afad6-118">In the **Company** field, select the desired company.</span></span> 
8. <span data-ttu-id="afad6-119">Setzen Sie im Inforegister **Benutzerrollen** die Option **Rollen zuweisen** auf [Zuweisen von Benutzern zu Sicherheitsrollen](assign-users-security-roles.md)</span><span class="sxs-lookup"><span data-stu-id="afad6-119">On the **User's roles** FastTab, select **Assign roles** to [assign users to security roles](assign-users-security-roles.md)</span></span>
9. <span data-ttu-id="afad6-120">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="afad6-120">Select **OK**.</span></span>
10. <span data-ttu-id="afad6-121">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="afad6-121">Select **Save**.</span></span>

## <a name="import-users"></a><span data-ttu-id="afad6-122">Benutzer importieren</span><span class="sxs-lookup"><span data-stu-id="afad6-122">Import users</span></span>
1. <span data-ttu-id="afad6-123">Wählen Sie im Aktivitätsbereich **Benutzer importieren** aus.</span><span class="sxs-lookup"><span data-stu-id="afad6-123">On the Action Pane, select **Import users**.</span></span>
2. <span data-ttu-id="afad6-124">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="afad6-124">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="afad6-125">Wählen Sie **Benutzer importieren** aus.</span><span class="sxs-lookup"><span data-stu-id="afad6-125">Select **Import users**.</span></span>
4. <span data-ttu-id="afad6-126">Wählen Sie **Schließen** aus.</span><span class="sxs-lookup"><span data-stu-id="afad6-126">Select **Close**.</span></span>

