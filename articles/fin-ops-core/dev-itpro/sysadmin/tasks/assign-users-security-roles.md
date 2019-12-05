---
title: Zuweisen von Benutzern zu Sicherheitsrollen
description: Um auf Finance and Operations-Apps zuzugreifen, müssen Benutzer Sicherheitsrollen zugewiesen werden.
author: ChrisGarty
manager: AnnBe
ms.date: 11/14/2019
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
ms.openlocfilehash: e4f4ef4535de9e371829c2d86d4fdc1400510c7b
ms.sourcegitcommit: 6aa74f66f1abd3a7977050a5339b0b17e62ff053
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/15/2019
ms.locfileid: "2807995"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="c6aee-103">Zuweisen von Benutzern zu Sicherheitsrollen</span><span class="sxs-lookup"><span data-stu-id="c6aee-103">Assign users to security roles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c6aee-104">Um etwas außerhalb der allgemeinen Funktionen verwenden zu können, müssen Benutzern Sicherheitsrollen zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="c6aee-104">To use anything other than common capabilities, users must be assigned to security roles.</span></span> <span data-ttu-id="c6aee-105">Diese Prozedur zeigt, wie Systemadministratoren Benutzer automatisch zu Rollen zuweisen können, basierend auf Geschäftsdaten.</span><span class="sxs-lookup"><span data-stu-id="c6aee-105">This procedure explains how system administrators can automatically assign users to roles, based on business data.</span></span> 

## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="c6aee-106">Weisen Sie Benutzer automatisch Rollen zu</span><span class="sxs-lookup"><span data-stu-id="c6aee-106">Automatically assign users to roles</span></span>
1. <span data-ttu-id="c6aee-107">Wechseln Sie zu **Navigationsbereich > Module > Systemverwaltung > Sicherheit > Benutzer zu Rollen zuweisen**.</span><span class="sxs-lookup"><span data-stu-id="c6aee-107">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
2. <span data-ttu-id="c6aee-108">In der Struktur wählen Sie "Supervisor Buchhaltung" aus.</span><span class="sxs-lookup"><span data-stu-id="c6aee-108">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="c6aee-109">Wählen Sie die Rolle aus, für die Sie die Regel konfigurieren möchten.</span><span class="sxs-lookup"><span data-stu-id="c6aee-109">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="c6aee-110">In diesem Beispiel wählen Sie "Supervisor Buchhaltung" aus.</span><span class="sxs-lookup"><span data-stu-id="c6aee-110">In this example, select Accounting supervisor.</span></span> 
3. <span data-ttu-id="c6aee-111">Klicken Sie auf **Regel hinzufügen**, um das Ablagedialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c6aee-111">Click **Add rule** to open the drop dialog.</span></span>
4. <span data-ttu-id="c6aee-112">In der Liste **Eine Abfrage auswählen** den gewünschten Datensatz suchen und auswählen.</span><span class="sxs-lookup"><span data-stu-id="c6aee-112">In the **Select a query**list, find and select the desired record.</span></span> <span data-ttu-id="c6aee-113">Wählen Sie die Abfrage aus, die für diese Regel zu verwenden ist.</span><span class="sxs-lookup"><span data-stu-id="c6aee-113">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="c6aee-114">Klicken Sie in der Liste **Mitgliederregelname** auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="c6aee-114">In the **Membership rule name** list, click the link in the selected row.</span></span>
6. <span data-ttu-id="c6aee-115">Klicken Sie auf **Abtrage bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="c6aee-115">Click **Edit query**.</span></span> <span data-ttu-id="c6aee-116">Bearbeiten Sie die Abfrage nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="c6aee-116">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="c6aee-117">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="c6aee-117">Click **OK**.</span></span>
8. <span data-ttu-id="c6aee-118">Klicken Sie auf **Automatische Rollenzuweisung ausführen**.</span><span class="sxs-lookup"><span data-stu-id="c6aee-118">Click **Run automatic role assignment**.</span></span>
9. <span data-ttu-id="c6aee-119">Wechseln Sie zu **Navigationsbereich > Module > Systemverwaltung > Benutzer > Benutzer** (idealerweise in einer separaten Browserregisterkarte).</span><span class="sxs-lookup"><span data-stu-id="c6aee-119">Go to **Navigation pane > Modules > System administration > Users > Users** (ideally in a separate browser tab).</span></span>
10. <span data-ttu-id="c6aee-120">Überprüfen Sie die Rollen, die unterschiedlichen Benutzern zugewiesen sind, um zu bestätigen, dass die Rollenzuweisungsabfrage korrekt war.</span><span class="sxs-lookup"><span data-stu-id="c6aee-120">Review the roles assigned to various users to confirm that the role assignment query was correct.</span></span> <span data-ttu-id="c6aee-121">Passen Sie bei Bedarf die Werte an, und führen Sie den Vorgang erneut aus.</span><span class="sxs-lookup"><span data-stu-id="c6aee-121">Adjust and re-run if needed.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="c6aee-122">Schließen Sie Benutzer von der automatischen Rollenzuweisung aus</span><span class="sxs-lookup"><span data-stu-id="c6aee-122">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="c6aee-123">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="c6aee-123">Close the page.</span></span>
2. <span data-ttu-id="c6aee-124">Wechseln Sie zu **Navigationsbereich > Module > Systemverwaltung > Sicherheit > Benutzer zu Rollen zuweisen**.</span><span class="sxs-lookup"><span data-stu-id="c6aee-124">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
3. <span data-ttu-id="c6aee-125">In der Struktur wählen Sie "Supervisor Buchhaltung" aus.</span><span class="sxs-lookup"><span data-stu-id="c6aee-125">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="c6aee-126">Wählen Sie hier eine Rolle aus.</span><span class="sxs-lookup"><span data-stu-id="c6aee-126">Select a role.</span></span> <span data-ttu-id="c6aee-127">Wählen Sie für dieses Beispiel "Supervisor Buchhaltung" aus.</span><span class="sxs-lookup"><span data-stu-id="c6aee-127">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="c6aee-128">Im Menü **Der Rolle zugewiesene Benutzer** wählen Sie **Benutzer manuell zuweisen/ausschließen** aus.</span><span class="sxs-lookup"><span data-stu-id="c6aee-128">In the **Users assigned to role** menu, select **Manually assign / exclude users**.</span></span>
5. <span data-ttu-id="c6aee-129">Markieren Sie in der Liste **Benutzer der Rolle zuweisen oder davon ausschließen** die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="c6aee-129">In the **Assign users to or exclude users from role** list, mark the selected row.</span></span> <span data-ttu-id="c6aee-130">Wählen Sie einen Benutzer aus.</span><span class="sxs-lookup"><span data-stu-id="c6aee-130">Select a user.</span></span>  
6. <span data-ttu-id="c6aee-131">Wählen Sie im **Aktivitätsbereich** die Option **Von Rolle ausschließen** aus.</span><span class="sxs-lookup"><span data-stu-id="c6aee-131">On the **Action pane**, select **Exclude from role**.</span></span>
    
    <span data-ttu-id="c6aee-132">Klicken Sie auf **Von Rolle ausschließen**, um die ausgewählten Benutzer von der Rolle auszuschließen.</span><span class="sxs-lookup"><span data-stu-id="c6aee-132">Click **Exclude from role** to exclude the selected users from the role.</span></span> <span data-ttu-id="c6aee-133">Um Ausschlüsse zu entfernen, wählen Sie die Benutzer aus, für die Sie Ausschlüsse entfernen möchten, und klicken Sie dann auf **Status zurücksetzen**.</span><span class="sxs-lookup"><span data-stu-id="c6aee-133">To remove exclusions, select the users that you want to remove exclusions for, and then click **Reset status**.</span></span> <span data-ttu-id="c6aee-134">Wenn Sie einen Ausschluss entfernen, indem Sie den Status des Benutzers zurücksetzen, wird die Rolle des Benutzers erneut automatisch zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="c6aee-134">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="c6aee-135">Allerdings wird der Benutzer nicht sofort der Rolle zugewiesen oder von der Rolle ausgeschlossen, wenn Sie den Status zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="c6aee-135">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="c6aee-136">Stattdessen wird der Benutzer entweder der Rolle zugewiesen oder von der Rolle entfernt, und zwar das nächste Mal, wenn die Regeln für automatische Rollenzuweisung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c6aee-136">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  
