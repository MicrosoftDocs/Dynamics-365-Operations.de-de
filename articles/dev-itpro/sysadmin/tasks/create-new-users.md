---
title: Erstellen neuer Benutzer
description: Benutzer sind interne Mitarbeiter der Organisation oder externe Debitoren und Kreditoren, die Zugriff auf Microsoft Dynamics AX anfordern, ihre Einzelvorgänge auszuführen.
author: maertenm
manager: AnnBe
ms.date: 07/01/2019
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
ms.openlocfilehash: a542ece226750330262e0c44427e5654fa4f6369
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916483"
---
# <a name="create-new-users"></a><span data-ttu-id="13a24-103">Erstellen neuer Benutzer</span><span class="sxs-lookup"><span data-stu-id="13a24-103">Create new users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="13a24-104">Benutzer sind interne Mitarbeiter der Organisation oder externe Debitoren und Kreditoren, die Zugriff auf Microsoft Dynamics AX anfordern, ihre Einzelvorgänge auszuführen.</span><span class="sxs-lookup"><span data-stu-id="13a24-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to perform their jobs.</span></span> <span data-ttu-id="13a24-105">Systemadministratoren können diese Verfahren ausführen, um dem System Benutzer hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="13a24-105">System administrators can complete this procedure to add users to the system.</span></span> <span data-ttu-id="13a24-106">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="13a24-106">The demo data company used to create this procedure is USMF.</span></span> 


## <a name="add-a-new-user"></a><span data-ttu-id="13a24-107">Hinzufügen eines neuen Benutzers</span><span class="sxs-lookup"><span data-stu-id="13a24-107">Add a new user</span></span>
1. <span data-ttu-id="13a24-108">Wechseln Sie zu **Navigationsbereich > Module > Systemverwaltung > Benutzer > Benutzer**.</span><span class="sxs-lookup"><span data-stu-id="13a24-108">Go to **Navigation pane > Modules > System administration > Users > Users**.</span></span>
2. <span data-ttu-id="13a24-109">Klicken Sie im **Aktivitätsbereich** auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="13a24-109">On the **Action pane**, click **New**.</span></span>
3. <span data-ttu-id="13a24-110">Geben Sie im Feld **Benutzer-ID** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="13a24-110">In the **User ID** field, type a value.</span></span> <span data-ttu-id="13a24-111">Geben Sie eine eindeutige Kennung für die Gruppe ein.</span><span class="sxs-lookup"><span data-stu-id="13a24-111">Enter a unique identifier for the user.</span></span> <span data-ttu-id="13a24-112">Geben Sie ein Kennwort ein.</span><span class="sxs-lookup"><span data-stu-id="13a24-112">A user ID is required.</span></span>  
4. <span data-ttu-id="13a24-113">Geben Sie im Feld **Benutzername** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="13a24-113">In the **User name** field, type a value.</span></span> <span data-ttu-id="13a24-114">Geben Sie den Namen des Kreditors ein</span><span class="sxs-lookup"><span data-stu-id="13a24-114">Enter the user's name.</span></span>  
5. <span data-ttu-id="13a24-115">Geben Sie im Feld **Domäne** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="13a24-115">In the **Domain** field, type a value.</span></span> <span data-ttu-id="13a24-116">Geben Sie den Namen des Kreditors ein</span><span class="sxs-lookup"><span data-stu-id="13a24-116">Enter the user's domain.</span></span>  
6. <span data-ttu-id="13a24-117">Geben Sie im Feld **Alias** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="13a24-117">In the **Alias** field, type a value.</span></span> <span data-ttu-id="13a24-118">Geben Sie den Namen des Kreditors ein</span><span class="sxs-lookup"><span data-stu-id="13a24-118">Enter the user's alias.</span></span>  
7. <span data-ttu-id="13a24-119">Klicken Sie im Feld **Unternehmen** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="13a24-119">In the **Company** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="13a24-120">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="13a24-120">In the list, find and select the desired record.</span></span> 
9. <span data-ttu-id="13a24-121">Klicken Sie im Abschnitt **Benutzerrollen** auf **Rollen zuweisen**.</span><span class="sxs-lookup"><span data-stu-id="13a24-121">In the **User's roles** section, click **Assign roles**.</span></span>
10. <span data-ttu-id="13a24-122">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="13a24-122">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="13a24-123">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="13a24-123">Click **OK**.</span></span>
12. <span data-ttu-id="13a24-124">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="13a24-124">Click **Save**.</span></span>

## <a name="import-users"></a><span data-ttu-id="13a24-125">Benutzer importieren</span><span class="sxs-lookup"><span data-stu-id="13a24-125">Import users</span></span>
1. <span data-ttu-id="13a24-126">Klicken Sie im **Aktivitätsbereich** auf **Benutzer importieren**.</span><span class="sxs-lookup"><span data-stu-id="13a24-126">On the **Action pane**, click **Import users**.</span></span>
2. <span data-ttu-id="13a24-127">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="13a24-127">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="13a24-128">Klicken Sie auf **Benutzer importieren**.</span><span class="sxs-lookup"><span data-stu-id="13a24-128">Click **Import users**.</span></span>
4. <span data-ttu-id="13a24-129">Klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="13a24-129">Click **Close**.</span></span>

