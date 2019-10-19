---
title: Zuweisen von Benutzern zu Sicherheitsrollen
description: Um auf Finance and Operations-Apps zuzugreifen, müssen Benutzer Sicherheitsrollen zugewiesen werden.
author: ChrisGarty
manager: AnnBe
ms.date: 09/16/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a4daecc1acd589cd1656402244e5325382a407e7
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180966"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="25dd4-103">Zuweisen von Benutzern zu Sicherheitsrollen</span><span class="sxs-lookup"><span data-stu-id="25dd4-103">Assign users to security roles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="25dd4-104">Um etwas außerhalb der allgemeinen Funktionen verwenden zu können, müssen Benutzern Sicherheitsrollen zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="25dd4-104">To use anything other than common capabilities, users must be assigned to security roles.</span></span> <span data-ttu-id="25dd4-105">Diese Prozedur zeigt, wie Systemadministratoren Benutzer automatisch zu Rollen zuweisen können, basierend auf Geschäftsdaten.</span><span class="sxs-lookup"><span data-stu-id="25dd4-105">This procedure explains how system administrators can automatically assign users to roles, based on business data.</span></span> 

## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="25dd4-106">Weisen Sie Benutzer automatisch Rollen zu</span><span class="sxs-lookup"><span data-stu-id="25dd4-106">Automatically assign users to roles</span></span>
1. <span data-ttu-id="25dd4-107">Wechseln Sie zu **Navigationsbereich > Module > Systemverwaltung > Sicherheit > Benutzer zu Rollen zuweisen**.</span><span class="sxs-lookup"><span data-stu-id="25dd4-107">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
2. <span data-ttu-id="25dd4-108">In der Struktur wählen Sie "Supervisor Buchhaltung" aus.</span><span class="sxs-lookup"><span data-stu-id="25dd4-108">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="25dd4-109">Wählen Sie die Rolle aus, für die Sie die Regel konfigurieren möchten.</span><span class="sxs-lookup"><span data-stu-id="25dd4-109">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="25dd4-110">In diesem Beispiel wählen Sie "Supervisor Buchhaltung" aus.</span><span class="sxs-lookup"><span data-stu-id="25dd4-110">In this example, select Accounting supervisor.</span></span> 
3. <span data-ttu-id="25dd4-111">Klicken Sie auf **Regel hinzufügen**, um das Ablagedialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="25dd4-111">Click **Add rule** to open the drop dialog.</span></span>
4. <span data-ttu-id="25dd4-112">In der Liste **Eine Abfrage auswählen** den gewünschten Datensatz suchen und auswählen.</span><span class="sxs-lookup"><span data-stu-id="25dd4-112">In the **Select a query**list, find and select the desired record.</span></span> <span data-ttu-id="25dd4-113">Wählen Sie die Abfrage aus, die für diese Regel zu verwenden ist.</span><span class="sxs-lookup"><span data-stu-id="25dd4-113">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="25dd4-114">Klicken Sie in der Liste **Mitgliederregelname** auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="25dd4-114">In the **Membership rule name** list, click the link in the selected row.</span></span>
6. <span data-ttu-id="25dd4-115">Klicken Sie auf **Abtrage bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="25dd4-115">Click **Edit query**.</span></span> <span data-ttu-id="25dd4-116">Bearbeiten Sie die Abfrage nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="25dd4-116">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="25dd4-117">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="25dd4-117">Click **OK**.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="25dd4-118">Schließen Sie Benutzer von der automatischen Rollenzuweisung aus</span><span class="sxs-lookup"><span data-stu-id="25dd4-118">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="25dd4-119">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="25dd4-119">Close the page.</span></span>
2. <span data-ttu-id="25dd4-120">Wechseln Sie zu **Navigationsbereich > Module > Systemverwaltung > Sicherheit > Benutzer zu Rollen zuweisen**.</span><span class="sxs-lookup"><span data-stu-id="25dd4-120">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
3. <span data-ttu-id="25dd4-121">In der Struktur wählen Sie "Supervisor Buchhaltung" aus.</span><span class="sxs-lookup"><span data-stu-id="25dd4-121">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="25dd4-122">Wählen Sie hier eine Rolle aus.</span><span class="sxs-lookup"><span data-stu-id="25dd4-122">Select a role.</span></span> <span data-ttu-id="25dd4-123">Wählen Sie für dieses Beispiel "Supervisor Buchhaltung" aus.</span><span class="sxs-lookup"><span data-stu-id="25dd4-123">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="25dd4-124">Im Menü **Der Rolle zugewiesene Benutzer** wählen Sie **Benutzer manuell zuweisen/ausschließen** aus.</span><span class="sxs-lookup"><span data-stu-id="25dd4-124">In the **Users assigned to role** menu, select **Manually assign / exclude users**.</span></span>
5. <span data-ttu-id="25dd4-125">Markieren Sie in der Liste **Benutzer der Rolle zuweisen oder davon ausschließen** die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="25dd4-125">In the **Assign users to or exclude users from role** list, mark the selected row.</span></span> <span data-ttu-id="25dd4-126">Wählen Sie einen Benutzer aus.</span><span class="sxs-lookup"><span data-stu-id="25dd4-126">Select a user.</span></span>  
6. <span data-ttu-id="25dd4-127">Wählen Sie im **Aktivitätsbereich** die Option **Von Rolle ausschließen** aus.</span><span class="sxs-lookup"><span data-stu-id="25dd4-127">On the **Action pane**, select **Exclude from role**.</span></span>
    
    <span data-ttu-id="25dd4-128">Klicken Sie auf **Von Rolle ausschließen**, um die ausgewählten Benutzer von der Rolle auszuschließen.</span><span class="sxs-lookup"><span data-stu-id="25dd4-128">Click **Exclude from role** to exclude the selected users from the role.</span></span> <span data-ttu-id="25dd4-129">Um Ausschlüsse zu entfernen, wählen Sie die Benutzer aus, für die Sie Ausschlüsse entfernen möchten, und klicken Sie dann auf **Status zurücksetzen**.</span><span class="sxs-lookup"><span data-stu-id="25dd4-129">To remove exclusions, select the users that you want to remove exclusions for, and then click **Reset status**.</span></span> <span data-ttu-id="25dd4-130">Wenn Sie einen Ausschluss entfernen, indem Sie den Status des Benutzers zurücksetzen, wird die Rolle des Benutzers erneut automatisch zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="25dd4-130">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="25dd4-131">Allerdings wird der Benutzer nicht sofort der Rolle zugewiesen oder von der Rolle ausgeschlossen, wenn Sie den Status zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="25dd4-131">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="25dd4-132">Stattdessen wird der Benutzer entweder der Rolle zugewiesen oder von der Rolle entfernt, und zwar das nächste Mal, wenn die Regeln für automatische Rollenzuweisung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="25dd4-132">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  
