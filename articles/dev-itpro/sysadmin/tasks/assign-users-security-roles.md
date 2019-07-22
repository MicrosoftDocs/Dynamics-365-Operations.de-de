---
title: Zuweisen von Benutzern zu Sicherheitsrollen
description: Für den Zugriff auf Microsoft Dynamics 365 for Finance and Operations Enterprise Edition müssen Benutzer Sicherheitsrollen zugewiesen werden.
author: maertenm
manager: AnnBe
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ab9f2f5ea07ae1d616c48dffa8810b966f7dbb2f
ms.sourcegitcommit: 33e98f89294086334fe9c0a350abb6a52ef9dacb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/28/2019
ms.locfileid: "1711130"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="93ced-103">Zuweisen von Benutzern zu Sicherheitsrollen</span><span class="sxs-lookup"><span data-stu-id="93ced-103">Assign users to security roles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="93ced-104">Für den Zugriff auf Microsoft Dynamics 365 for Finance and Operations Enterprise Edition müssen Benutzer Sicherheitsrollen zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="93ced-104">To access Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, users must be assigned to security roles.</span></span> <span data-ttu-id="93ced-105">Diese Prozedur zeigt, wie Systemadministratoren Benutzer automatisch zu Rollen zuweisen können, basierend auf Geschäftsdaten.</span><span class="sxs-lookup"><span data-stu-id="93ced-105">This procedure explains how system administrators can assign users to roles automatically, based on business data.</span></span> <span data-ttu-id="93ced-106">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="93ced-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="93ced-107">Weisen Sie Benutzer automatisch Rollen zu</span><span class="sxs-lookup"><span data-stu-id="93ced-107">Automatically assign users to roles</span></span>
1. <span data-ttu-id="93ced-108">Wechseln Sie zu **Navigationsbereich > Module > Systemverwaltung > Sicherheit > Benutzer zu Rollen zuweisen**.</span><span class="sxs-lookup"><span data-stu-id="93ced-108">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
2. <span data-ttu-id="93ced-109">In der Struktur wählen Sie "Supervisor Buchhaltung" aus.</span><span class="sxs-lookup"><span data-stu-id="93ced-109">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="93ced-110">Wählen Sie die Rolle aus, für die Sie die Regel konfigurieren möchten.</span><span class="sxs-lookup"><span data-stu-id="93ced-110">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="93ced-111">In diesem Beispiel wählen Sie "Supervisor Buchhaltung" aus.</span><span class="sxs-lookup"><span data-stu-id="93ced-111">In this example, select Accounting supervisor.</span></span> 
3. <span data-ttu-id="93ced-112">Klicken Sie auf **Regel hinzufügen**, um das Ablagedialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="93ced-112">Click **Add rule** to open the drop dialog.</span></span>
4. <span data-ttu-id="93ced-113">In der Liste **Eine Abfrage auswählen** den gewünschten Datensatz suchen und auswählen.</span><span class="sxs-lookup"><span data-stu-id="93ced-113">In the **Select a query**list, find and select the desired record.</span></span> <span data-ttu-id="93ced-114">Wählen Sie die Abfrage aus, die für diese Regel zu verwenden ist.</span><span class="sxs-lookup"><span data-stu-id="93ced-114">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="93ced-115">Klicken Sie in der Liste **Mitgliederregelname** auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="93ced-115">In the **Membership rule name** list, click the link in the selected row.</span></span>
6. <span data-ttu-id="93ced-116">Klicken Sie auf **Abtrage bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="93ced-116">Click **Edit query**.</span></span> <span data-ttu-id="93ced-117">Bearbeiten Sie die Abfrage nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="93ced-117">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="93ced-118">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="93ced-118">Click **OK**.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="93ced-119">Schließen Sie Benutzer von der automatischen Rollenzuweisung aus</span><span class="sxs-lookup"><span data-stu-id="93ced-119">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="93ced-120">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="93ced-120">Close the page.</span></span>
2. <span data-ttu-id="93ced-121">Wechseln Sie zu **Navigationsbereich > Module > Systemverwaltung > Sicherheit > Benutzer zu Rollen zuweisen**.</span><span class="sxs-lookup"><span data-stu-id="93ced-121">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
3. <span data-ttu-id="93ced-122">In der Struktur wählen Sie "Supervisor Buchhaltung" aus.</span><span class="sxs-lookup"><span data-stu-id="93ced-122">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="93ced-123">Wählen Sie hier eine Rolle aus.</span><span class="sxs-lookup"><span data-stu-id="93ced-123">Select a role.</span></span> <span data-ttu-id="93ced-124">Wählen Sie für dieses Beispiel "Supervisor Buchhaltung" aus.</span><span class="sxs-lookup"><span data-stu-id="93ced-124">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="93ced-125">Im Menü **Der Rolle zugewiesene Benutzer** wählen Sie **Benutzer manuell zuweisen/ausschließen** aus.</span><span class="sxs-lookup"><span data-stu-id="93ced-125">In the **Users assigned to role** menu, select **Manually assign / exclude users**.</span></span>
5. <span data-ttu-id="93ced-126">Markieren Sie in der Liste **Benutzer der Rolle zuweisen oder davon ausschließen** die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="93ced-126">In the **Assign users to or exclude users from role** list, mark the selected row.</span></span> <span data-ttu-id="93ced-127">Wählen Sie einen Benutzer aus.</span><span class="sxs-lookup"><span data-stu-id="93ced-127">Select a user.</span></span>  
6. <span data-ttu-id="93ced-128">Wählen Sie im **Aktivitätsbereich** die Option **Von Rolle ausschließen** aus.</span><span class="sxs-lookup"><span data-stu-id="93ced-128">On the **Action pane**, select **Exclude from role**.</span></span>
    
    <span data-ttu-id="93ced-129">Klicken Sie auf **Von Rolle ausschließen**, um die ausgewählten Benutzer von der Rolle auszuschließen.</span><span class="sxs-lookup"><span data-stu-id="93ced-129">Click **Exclude from role** to exclude the selected users from the role.</span></span> <span data-ttu-id="93ced-130">Um Ausschlüsse zu entfernen, wählen Sie die Benutzer aus, für die Sie Ausschlüsse entfernen möchten, und klicken Sie dann auf **Status zurücksetzen**.</span><span class="sxs-lookup"><span data-stu-id="93ced-130">To remove exclusions, select the users that you want to remove exclusions for, and then click **Reset status**.</span></span> <span data-ttu-id="93ced-131">Wenn Sie einen Ausschluss entfernen, indem Sie den Status des Benutzers zurücksetzen, wird die Rolle des Benutzers erneut automatisch zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="93ced-131">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="93ced-132">Allerdings wird der Benutzer nicht sofort der Rolle zugewiesen oder von der Rolle ausgeschlossen, wenn Sie den Status zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="93ced-132">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="93ced-133">Stattdessen wird der Benutzer entweder der Rolle zugewiesen oder von der Rolle entfernt, und zwar das nächste Mal, wenn die Regeln für automatische Rollenzuweisung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="93ced-133">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  
