---
title: Zuweisen von Benutzern zu Sicherheitsrollen
description: Für den Zugriff auf Microsoft Dynamics 365 for Finance and Operations Enterprise Edition müssen Benutzer Sicherheitsrollen zugewiesen werden.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: 55cb085bb5170aa4894a2240a12f6ca451b922fb
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "349951"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="ca332-103">Zuweisen von Benutzern zu Sicherheitsrollen</span><span class="sxs-lookup"><span data-stu-id="ca332-103">Assign users to security roles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ca332-104">Für den Zugriff auf Microsoft Dynamics 365 for Finance and Operations Enterprise Edition müssen Benutzer Sicherheitsrollen zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="ca332-104">To access Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, users must be assigned to security roles.</span></span> <span data-ttu-id="ca332-105">Diese Prozedur zeigt, wie Systemadministratoren Benutzer automatisch zu Rollen zuweisen können, basierend auf Geschäftsdaten.</span><span class="sxs-lookup"><span data-stu-id="ca332-105">This procedure explains how system administrators can assign users to roles automatically, based on business data.</span></span> <span data-ttu-id="ca332-106">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="ca332-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="ca332-107">Weisen Sie Benutzer automatisch Rollen zu</span><span class="sxs-lookup"><span data-stu-id="ca332-107">Automatically assign users to roles</span></span>
1. <span data-ttu-id="ca332-108">Wechseln Sie zu "Systemverwaltung"  "Sicherheit"  "Benutzer zu Rollen zuweisen".</span><span class="sxs-lookup"><span data-stu-id="ca332-108">Go to System administration > Security > Assign users to roles.</span></span>
2. <span data-ttu-id="ca332-109">In der Struktur wählen Sie "Supervisor Buchhaltung" aus.</span><span class="sxs-lookup"><span data-stu-id="ca332-109">In the tree, select 'Accounting supervisor'.</span></span>
    * <span data-ttu-id="ca332-110">Wählen Sie die Rolle aus, für die Sie die Regel konfigurieren möchten.</span><span class="sxs-lookup"><span data-stu-id="ca332-110">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="ca332-111">In diesem Beispiel wählen Sie "Supervisor Buchhaltung" aus.</span><span class="sxs-lookup"><span data-stu-id="ca332-111">In this example, select Accounting supervisor.</span></span>  
3. <span data-ttu-id="ca332-112">Klicken Sie auf "Regel hinzufügen", um das Ablagedialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ca332-112">Click Add rule to open the drop dialog.</span></span>
4. <span data-ttu-id="ca332-113">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="ca332-113">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ca332-114">Wählen Sie die Abfrage aus, die für diese Regel zu verwenden ist.</span><span class="sxs-lookup"><span data-stu-id="ca332-114">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="ca332-115">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="ca332-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="ca332-116">(Zum Bearbeiten klicken)</span><span class="sxs-lookup"><span data-stu-id="ca332-116">Click Edit query.</span></span>
    * <span data-ttu-id="ca332-117">Bearbeiten Sie die Abfrage nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="ca332-117">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="ca332-118">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="ca332-118">Click OK.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="ca332-119">Schließen Sie Benutzer von der automatischen Rollenzuweisung aus</span><span class="sxs-lookup"><span data-stu-id="ca332-119">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="ca332-120">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="ca332-120">Close the page.</span></span>
2. <span data-ttu-id="ca332-121">Wechseln Sie zu "Systemverwaltung"  "Sicherheit"  "Benutzer zu Rollen zuweisen".</span><span class="sxs-lookup"><span data-stu-id="ca332-121">Go to System administration > Security > Assign users to roles.</span></span>
3. <span data-ttu-id="ca332-122">In der Struktur wählen Sie "Supervisor Buchhaltung" aus.</span><span class="sxs-lookup"><span data-stu-id="ca332-122">In the tree, select 'Accounting supervisor'.</span></span>
    * <span data-ttu-id="ca332-123">Wählen Sie hier eine Rolle aus.</span><span class="sxs-lookup"><span data-stu-id="ca332-123">Select a role.</span></span> <span data-ttu-id="ca332-124">Wählen Sie für dieses Beispiel "Supervisor Buchhaltung" aus.</span><span class="sxs-lookup"><span data-stu-id="ca332-124">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="ca332-125">Klicken Sie auf "Benutzer manuell zuweisen/ausschließen".</span><span class="sxs-lookup"><span data-stu-id="ca332-125">Click Manually assign / exclude users.</span></span>
5. <span data-ttu-id="ca332-126">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="ca332-126">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="ca332-127">Wählen Sie einen Benutzer aus.</span><span class="sxs-lookup"><span data-stu-id="ca332-127">Select a user.</span></span>  
6. <span data-ttu-id="ca332-128">Klicken Sie auf "Von Rolle ausschließen".</span><span class="sxs-lookup"><span data-stu-id="ca332-128">Click Exclude from role.</span></span>
    * <span data-ttu-id="ca332-129">Klicken Sie auf "Von Rolle ausschließen", um die ausgewählten Benutzer von der Rolle auszuschließen.</span><span class="sxs-lookup"><span data-stu-id="ca332-129">Click Exclude from role to exclude the selected users from the role.</span></span> <span data-ttu-id="ca332-130">Um Ausschlüsse zu entfernen, wählen Sie die Benutzer aus, für die Sie Ausschlüsse entfernen möchten, und klicken Sie dann auf "Status zurücksetzen".</span><span class="sxs-lookup"><span data-stu-id="ca332-130">To remove exclusions, select the users that you want to remove exclusions for, and then click Reset status.</span></span> <span data-ttu-id="ca332-131">Wenn Sie einen Ausschluss entfernen, indem Sie den Status des Benutzers zurücksetzen, wird die Rolle des Benutzers erneut automatisch zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="ca332-131">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="ca332-132">Allerdings wird der Benutzer nicht sofort der Rolle zugewiesen oder von der Rolle ausgeschlossen, wenn Sie den Status zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="ca332-132">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="ca332-133">Stattdessen wird der Benutzer entweder der Rolle zugewiesen oder von der Rolle entfernt, und zwar das nächste Mal, wenn die Regeln für automatische Rollenzuweisung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ca332-133">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  

