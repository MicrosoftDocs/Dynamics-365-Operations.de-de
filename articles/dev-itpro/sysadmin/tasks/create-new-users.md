---
title: Erstellen neuer Benutzer
description: Benutzer sind interne Mitarbeiter der Organisation oder externe Debitoren und Kreditoren, die Zugriff auf Microsoft Dynamics AX anfordern, ihre Einzelvorgänge auszuführen.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: 89e492ef5030dd28020094152259b615010aa676
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851310"
---
# <a name="create-new-users"></a><span data-ttu-id="23fe3-103">Erstellen neuer Benutzer</span><span class="sxs-lookup"><span data-stu-id="23fe3-103">Create new users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="23fe3-104">Benutzer sind interne Mitarbeiter der Organisation oder externe Debitoren und Kreditoren, die Zugriff auf Microsoft Dynamics AX anfordern, ihre Einzelvorgänge auszuführen.</span><span class="sxs-lookup"><span data-stu-id="23fe3-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to perform their jobs.</span></span> <span data-ttu-id="23fe3-105">Systemadministratoren können diese Verfahren ausführen, um dem System Benutzer hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="23fe3-105">System administrators can complete this procedure to add users to the system.</span></span> <span data-ttu-id="23fe3-106">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="23fe3-106">The demo data company used to create this procedure is USMF.</span></span> 


## <a name="add-a-new-user"></a><span data-ttu-id="23fe3-107">Hinzufügen eines neuen Benutzers</span><span class="sxs-lookup"><span data-stu-id="23fe3-107">Add a new user</span></span>
1. <span data-ttu-id="23fe3-108">Wechseln Sie zu "Systemverwaltung" > "Benutzer" > "Benutzer".</span><span class="sxs-lookup"><span data-stu-id="23fe3-108">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="23fe3-109">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="23fe3-109">Click New.</span></span>
3. <span data-ttu-id="23fe3-110">Geben Sie im Feld "Benutzer-ID" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="23fe3-110">In the User ID field, type a value.</span></span>
    * <span data-ttu-id="23fe3-111">Geben Sie eine eindeutige Kennung für die Gruppe ein.</span><span class="sxs-lookup"><span data-stu-id="23fe3-111">Enter a unique identifier for the user.</span></span> <span data-ttu-id="23fe3-112">Geben Sie ein Kennwort ein.</span><span class="sxs-lookup"><span data-stu-id="23fe3-112">A user ID is required.</span></span>  
4. <span data-ttu-id="23fe3-113">Geben Sie im Feld "Geldmittelname" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="23fe3-113">In the User name field, type a value.</span></span>
    * <span data-ttu-id="23fe3-114">Geben Sie den Namen des Kreditors ein</span><span class="sxs-lookup"><span data-stu-id="23fe3-114">Enter the user's name.</span></span>  
5. <span data-ttu-id="23fe3-115">Geben Sie im Feld "Domäne" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="23fe3-115">In the Domain field, type a value.</span></span>
    * <span data-ttu-id="23fe3-116">Geben Sie den Namen des Kreditors ein</span><span class="sxs-lookup"><span data-stu-id="23fe3-116">Enter the user's domain.</span></span>  
6. <span data-ttu-id="23fe3-117">Geben Sie im Feld Alias einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="23fe3-117">In the Alias field, type a value.</span></span>
    * <span data-ttu-id="23fe3-118">Geben Sie den Namen des Kreditors ein</span><span class="sxs-lookup"><span data-stu-id="23fe3-118">Enter the user's alias.</span></span>  
7. <span data-ttu-id="23fe3-119">Klicken Sie im Feld Unternehmen auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="23fe3-119">In the Company field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="23fe3-120">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="23fe3-120">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="23fe3-121">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="23fe3-121">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="23fe3-122">Das Unternehmenskonto des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="23fe3-122">Select the user's company</span></span>  
10. <span data-ttu-id="23fe3-123">Rollen zuweisen</span><span class="sxs-lookup"><span data-stu-id="23fe3-123">Click Assign roles.</span></span>
11. <span data-ttu-id="23fe3-124">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="23fe3-124">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="23fe3-125">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="23fe3-125">Click OK.</span></span>
13. <span data-ttu-id="23fe3-126">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="23fe3-126">Click Save.</span></span>

## <a name="import-users"></a><span data-ttu-id="23fe3-127">Benutzer importieren</span><span class="sxs-lookup"><span data-stu-id="23fe3-127">Import users</span></span>
1. <span data-ttu-id="23fe3-128">Benutzer importieren</span><span class="sxs-lookup"><span data-stu-id="23fe3-128">Click Import users.</span></span>
2. <span data-ttu-id="23fe3-129">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="23fe3-129">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="23fe3-130">Benutzer importieren</span><span class="sxs-lookup"><span data-stu-id="23fe3-130">Click Import users.</span></span>
4. <span data-ttu-id="23fe3-131">Klicken Sie auf "Schließen".</span><span class="sxs-lookup"><span data-stu-id="23fe3-131">Click Close.</span></span>

