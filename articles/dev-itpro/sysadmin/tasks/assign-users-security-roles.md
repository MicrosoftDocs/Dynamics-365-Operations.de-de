--- 
title: Weisen Sie Benutzer zu Sicherheitsrollen zu
description: "Um auf Microsoft Dynamics 365 for Finance and Operations zuzugreifen, müssen Benutzer Sicherheitsrollen zugewiesen werden."
author: maertenm
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 0ab51a56c33a84dea9cf945e808fa7bc42d3727c
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="4c9a4-103">Zuweisen von Benutzern zu Sicherheitsrollen</span><span class="sxs-lookup"><span data-stu-id="4c9a4-103">Assign users to security roles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4c9a4-104">Um auf Microsoft Dynamics 365 for Finance and Operations zuzugreifen, müssen Benutzer Sicherheitsrollen zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="4c9a4-104">To access Microsoft Dynamics 365 for Finance and Operations, users must be assigned to security roles.</span></span> <span data-ttu-id="4c9a4-105">Diese Prozedur zeigt, wie Systemadministratoren Benutzer automatisch zu Rollen zuweisen können, basierend auf Geschäftsdaten.</span><span class="sxs-lookup"><span data-stu-id="4c9a4-105">This procedure explains how system administrators can assign users to roles automatically, based on business data.</span></span> <span data-ttu-id="4c9a4-106">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="4c9a4-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="4c9a4-107">Weisen Sie Benutzer automatisch Rollen zu</span><span class="sxs-lookup"><span data-stu-id="4c9a4-107">Automatically assign users to roles</span></span>
1. <span data-ttu-id="4c9a4-108">Wechseln Sie zu "Systemverwaltung"  "Sicherheit"  "Benutzer zu Rollen zuweisen".</span><span class="sxs-lookup"><span data-stu-id="4c9a4-108">Go to System administration > Security > Assign users to roles.</span></span>
2. <span data-ttu-id="4c9a4-109">In der Struktur wählen Sie "Supervisor Buchhaltung" aus.</span><span class="sxs-lookup"><span data-stu-id="4c9a4-109">In the tree, select 'Accounting supervisor'.</span></span>
    * <span data-ttu-id="4c9a4-110">Wählen Sie die Rolle aus, für die Sie die Regel konfigurieren möchten.</span><span class="sxs-lookup"><span data-stu-id="4c9a4-110">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="4c9a4-111">In diesem Beispiel wählen Sie "Supervisor Buchhaltung" aus.</span><span class="sxs-lookup"><span data-stu-id="4c9a4-111">In this example, select Accounting supervisor.</span></span>  
3. <span data-ttu-id="4c9a4-112">Klicken Sie auf "Regel hinzufügen", um das Ablagedialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="4c9a4-112">Click Add rule to open the drop dialog.</span></span>
4. <span data-ttu-id="4c9a4-113">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="4c9a4-113">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4c9a4-114">Wählen Sie die Abfrage aus, die für diese Regel zu verwenden ist.</span><span class="sxs-lookup"><span data-stu-id="4c9a4-114">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="4c9a4-115">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="4c9a4-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="4c9a4-116">(Zum Bearbeiten klicken)</span><span class="sxs-lookup"><span data-stu-id="4c9a4-116">Click Edit query.</span></span>
    * <span data-ttu-id="4c9a4-117">Bearbeiten Sie die Abfrage nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="4c9a4-117">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="4c9a4-118">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="4c9a4-118">Click OK.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="4c9a4-119">Schließen Sie Benutzer von der automatischen Rollenzuweisung aus</span><span class="sxs-lookup"><span data-stu-id="4c9a4-119">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="4c9a4-120">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="4c9a4-120">Close the page.</span></span>
2. <span data-ttu-id="4c9a4-121">Wechseln Sie zu "Systemverwaltung"  "Sicherheit"  "Benutzer zu Rollen zuweisen".</span><span class="sxs-lookup"><span data-stu-id="4c9a4-121">Go to System administration > Security > Assign users to roles.</span></span>
3. <span data-ttu-id="4c9a4-122">In der Struktur wählen Sie "Supervisor Buchhaltung" aus.</span><span class="sxs-lookup"><span data-stu-id="4c9a4-122">In the tree, select 'Accounting supervisor'.</span></span>
    * <span data-ttu-id="4c9a4-123">Wählen Sie hier eine Rolle aus.</span><span class="sxs-lookup"><span data-stu-id="4c9a4-123">Select a role.</span></span> <span data-ttu-id="4c9a4-124">Wählen Sie für dieses Beispiel "Supervisor Buchhaltung" aus.</span><span class="sxs-lookup"><span data-stu-id="4c9a4-124">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="4c9a4-125">Klicken Sie auf "Benutzer manuell zuweisen/ausschließen".</span><span class="sxs-lookup"><span data-stu-id="4c9a4-125">Click Manually assign / exclude users.</span></span>
5. <span data-ttu-id="4c9a4-126">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="4c9a4-126">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="4c9a4-127">Wählen Sie einen Benutzer aus.</span><span class="sxs-lookup"><span data-stu-id="4c9a4-127">Select a user.</span></span>  
6. <span data-ttu-id="4c9a4-128">Klicken Sie auf "Von Rolle ausschließen".</span><span class="sxs-lookup"><span data-stu-id="4c9a4-128">Click Exclude from role.</span></span>
    * <span data-ttu-id="4c9a4-129">Klicken Sie auf "Von Rolle ausschließen", um die ausgewählten Benutzer von der Rolle auszuschließen.</span><span class="sxs-lookup"><span data-stu-id="4c9a4-129">Click Exclude from role to exclude the selected users from the role.</span></span> <span data-ttu-id="4c9a4-130">Um Ausschlüsse zu entfernen, wählen Sie die Benutzer aus, für die Sie Ausschlüsse entfernen möchten, und klicken Sie dann auf "Status zurücksetzen".</span><span class="sxs-lookup"><span data-stu-id="4c9a4-130">To remove exclusions, select the users that you want to remove exclusions for, and then click Reset status.</span></span> <span data-ttu-id="4c9a4-131">Wenn Sie einen Ausschluss entfernen, indem Sie den Status des Benutzers zurücksetzen, wird die Rolle des Benutzers erneut automatisch zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="4c9a4-131">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="4c9a4-132">Allerdings wird der Benutzer nicht sofort der Rolle zugewiesen oder von der Rolle ausgeschlossen, wenn Sie den Status zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="4c9a4-132">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="4c9a4-133">Stattdessen wird der Benutzer entweder der Rolle zugewiesen oder von der Rolle entfernt, und zwar das nächste Mal, wenn die Regeln für automatische Rollenzuweisung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="4c9a4-133">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  


