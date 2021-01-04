---
title: Benutzer aus Azure Active Directory importieren
description: Diese Prozedur kann von Systemadministratoren verwendet werden, um ausgewählte Benutzer manuell oder viele Benutzer aus Azure Active Directory zu importieren.
author: peakerbl
manager: AnnBe
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 56b6666310309817ff30ccb3902721880b829ee0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679813"
---
# <a name="import-users-from-azure-active-directory"></a><span data-ttu-id="ae6d6-103">Benutzer aus Azure Active Directory importieren</span><span class="sxs-lookup"><span data-stu-id="ae6d6-103">Import users from Azure Active Directory</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="import-select-users"></a><span data-ttu-id="ae6d6-104">Ausgewählte Benutzer importieren</span><span class="sxs-lookup"><span data-stu-id="ae6d6-104">Import select users</span></span>

<span data-ttu-id="ae6d6-105">Diese Prozedur kann von Systemadministratoren verwendet werden, um ausgewählte Benutzer aus Azure Active Directory (Azure AD) zu importieren.</span><span class="sxs-lookup"><span data-stu-id="ae6d6-105">This procedure can be used by system administrators to import select users from Azure Active Directory (Azure AD).</span></span>

1. <span data-ttu-id="ae6d6-106">Der Benutzer wird mit dem aktuellen Sitzungsunternehmen als Standardunternehmen importiert.</span><span class="sxs-lookup"><span data-stu-id="ae6d6-106">User will be imported with the current session company as their default company.</span></span> <span data-ttu-id="ae6d6-107">Ändern Sie gegebenenfalls das aktuelle Unternehmen, bevor Sie Benutzer importieren.</span><span class="sxs-lookup"><span data-stu-id="ae6d6-107">Change current company if applicable before importing users.</span></span>
2. <span data-ttu-id="ae6d6-108">Wechseln Sie zu **Systemverwaltung > Benutzer > Benutzer**.</span><span class="sxs-lookup"><span data-stu-id="ae6d6-108">Go to **System administration > Users > User** s.</span></span>
3. <span data-ttu-id="ae6d6-109">Klicken Sie auf **Benutzer importieren**.</span><span class="sxs-lookup"><span data-stu-id="ae6d6-109">Click **Import users**.</span></span>
4. <span data-ttu-id="ae6d6-110">Wählen Sie die Benutzer aus, die importiert werden sollen, und wählen Sie dann **Benutzer importieren** aus.</span><span class="sxs-lookup"><span data-stu-id="ae6d6-110">Select the users that should be imported and select **Import users**.</span></span>

<span data-ttu-id="ae6d6-111">Nach Abschluss des Imports müssen den Benutzern Rollen zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="ae6d6-111">After import is completed it will be required to assign roles to users.</span></span>

## <a name="import-users-in-bulk"></a><span data-ttu-id="ae6d6-112">Massenimport von Benutzern</span><span class="sxs-lookup"><span data-stu-id="ae6d6-112">Import users in bulk</span></span>

<span data-ttu-id="ae6d6-113">Diese Prozedur kann von Systemadministratoren verwendet werden, um viele Benutzer aus Azure Active Directory zu importieren.</span><span class="sxs-lookup"><span data-stu-id="ae6d6-113">This procedure can be used by system administrators to import a large number of users from Azure Active Directory.</span></span>
<span data-ttu-id="ae6d6-114">Beachten Sie, dass bei Verwendung der Stapelimportoption keine Benutzer ausgewählt werden können.</span><span class="sxs-lookup"><span data-stu-id="ae6d6-114">Note that it is not possible to select users when using the Batch import option.</span></span>

## <a name="run-the-import-as-a-batch-job"></a><span data-ttu-id="ae6d6-115">Import als Stapelverarbeitungslauf ausühren</span><span class="sxs-lookup"><span data-stu-id="ae6d6-115">Run the import as a batch job</span></span>
1. <span data-ttu-id="ae6d6-116">Der Benutzer wird mit dem aktuellen Sitzungsunternehmen als Standardunternehmen importiert.</span><span class="sxs-lookup"><span data-stu-id="ae6d6-116">User will be imported with the current session company as their default company.</span></span> <span data-ttu-id="ae6d6-117">Ändern Sie gegebenenfalls das aktuelle Unternehmen, bevor Sie Benutzer importieren.</span><span class="sxs-lookup"><span data-stu-id="ae6d6-117">Change current company if applicable before importing users.</span></span>
2. <span data-ttu-id="ae6d6-118">Wechseln Sie zu **Systemverwaltung > Benutzer > Benutzer**.</span><span class="sxs-lookup"><span data-stu-id="ae6d6-118">Go to **System administration > Users > Users**.</span></span>
3. <span data-ttu-id="ae6d6-119">Klicken Sie auf **Stapelimport**.</span><span class="sxs-lookup"><span data-stu-id="ae6d6-119">Click **Batch import**.</span></span>
4. <span data-ttu-id="ae6d6-120">Erweitern Sie den Abschnitt **Im Hintergrund ausführen**.</span><span class="sxs-lookup"><span data-stu-id="ae6d6-120">Expand the **Run in the background** section.</span></span>
4. <span data-ttu-id="ae6d6-121">Wählen Sie „Ja“ im Feld **Stapelverarbeitung** aus.</span><span class="sxs-lookup"><span data-stu-id="ae6d6-121">Select \*\*Yes in the **Batch processing** field.</span></span>
6. <span data-ttu-id="ae6d6-122">Geben Sie im Feld **Stapelverarbeitungsgruppe** einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="ae6d6-122">In the **Batch group** field, enter or select a value.</span></span> <span data-ttu-id="ae6d6-123">Dieser Schritt ist optional.</span><span class="sxs-lookup"><span data-stu-id="ae6d6-123">This is an optional step.</span></span>  
7. <span data-ttu-id="ae6d6-124">Wählen Sie **Ja** im Feld **Privat** aus.</span><span class="sxs-lookup"><span data-stu-id="ae6d6-124">Select **Yes** in the **Private** field.</span></span> <span data-ttu-id="ae6d6-125">Dieser Schritt ist optional.</span><span class="sxs-lookup"><span data-stu-id="ae6d6-125">This is an optional step.</span></span>  
8. <span data-ttu-id="ae6d6-126">Wählen Sie **Ja** im Feld **Kritische Aufgabe** aus.</span><span class="sxs-lookup"><span data-stu-id="ae6d6-126">Select **Yes** in the **Critical job** field.</span></span> <span data-ttu-id="ae6d6-127">Dieser Schritt ist optional.</span><span class="sxs-lookup"><span data-stu-id="ae6d6-127">bThis is an optional step.</span></span>  
9. <span data-ttu-id="ae6d6-128">Wählen Sie im Feld „Kategorie überwachen“ eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="ae6d6-128">In the \*\*Monitoring category field, select an option.</span></span>
10. <span data-ttu-id="ae6d6-129">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="ae6d6-129">Click **OK**.</span></span>

<span data-ttu-id="ae6d6-130">Nach Abschluss des Imports müssen den Benutzern Rollen zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="ae6d6-130">After import is completed, it will be required to assign roles to users.</span></span>

## <a name="run-in-a-sandbox-environment"></a><span data-ttu-id="ae6d6-131">Eine Sandkastenumgebung ausführen</span><span class="sxs-lookup"><span data-stu-id="ae6d6-131">Run in a sandbox environment</span></span>
1. <span data-ttu-id="ae6d6-132">Wählen Sie **Stapelimport** aus.</span><span class="sxs-lookup"><span data-stu-id="ae6d6-132">Select **Batch import**.</span></span>
2. <span data-ttu-id="ae6d6-133">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="ae6d6-133">Select **OK**.</span></span>
