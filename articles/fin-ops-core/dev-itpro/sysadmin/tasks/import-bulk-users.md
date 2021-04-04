---
title: Benutzer aus Azure Active Directory importieren
description: Diese Prozedur kann von Systemadministratoren verwendet werden, um ausgewählte Benutzer manuell oder viele Benutzer aus Azure Active Directory zu importieren.
author: peakerbl
manager: AnnBe
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0c2600ad8f441e6b73b143c27afa08ad0a5c2748
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5571004"
---
# <a name="import-users-from-azure-active-directory"></a><span data-ttu-id="2a437-103">Benutzer aus Azure Active Directory importieren</span><span class="sxs-lookup"><span data-stu-id="2a437-103">Import users from Azure Active Directory</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="import-select-users"></a><span data-ttu-id="2a437-104">Ausgewählte Benutzer importieren</span><span class="sxs-lookup"><span data-stu-id="2a437-104">Import select users</span></span>

<span data-ttu-id="2a437-105">Diese Prozedur kann von Systemadministratoren verwendet werden, um ausgewählte Benutzer aus Azure Active Directory (Azure AD) zu importieren.</span><span class="sxs-lookup"><span data-stu-id="2a437-105">This procedure can be used by system administrators to import select users from Azure Active Directory (Azure AD).</span></span>

1. <span data-ttu-id="2a437-106">Der Benutzer wird mit dem aktuellen Sitzungsunternehmen als Standardunternehmen importiert.</span><span class="sxs-lookup"><span data-stu-id="2a437-106">User will be imported with the current session company as their default company.</span></span> <span data-ttu-id="2a437-107">Ändern Sie gegebenenfalls das aktuelle Unternehmen, bevor Sie Benutzer importieren.</span><span class="sxs-lookup"><span data-stu-id="2a437-107">Change current company if applicable before importing users.</span></span>
2. <span data-ttu-id="2a437-108">Wechseln Sie zu **Systemverwaltung > Benutzer > Benutzer**.</span><span class="sxs-lookup"><span data-stu-id="2a437-108">Go to **System administration > Users > User** s.</span></span>
3. <span data-ttu-id="2a437-109">Klicken Sie auf **Benutzer importieren**.</span><span class="sxs-lookup"><span data-stu-id="2a437-109">Click **Import users**.</span></span>
4. <span data-ttu-id="2a437-110">Wählen Sie die Benutzer aus, die importiert werden sollen, und wählen Sie dann **Benutzer importieren** aus.</span><span class="sxs-lookup"><span data-stu-id="2a437-110">Select the users that should be imported and select **Import users**.</span></span>

<span data-ttu-id="2a437-111">Nach Abschluss des Imports müssen den Benutzern Rollen zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="2a437-111">After import is completed it will be required to assign roles to users.</span></span>

## <a name="import-users-in-bulk"></a><span data-ttu-id="2a437-112">Massenimport von Benutzern</span><span class="sxs-lookup"><span data-stu-id="2a437-112">Import users in bulk</span></span>

<span data-ttu-id="2a437-113">Diese Prozedur kann von Systemadministratoren verwendet werden, um viele Benutzer aus Azure Active Directory zu importieren.</span><span class="sxs-lookup"><span data-stu-id="2a437-113">This procedure can be used by system administrators to import a large number of users from Azure Active Directory.</span></span>
<span data-ttu-id="2a437-114">Beachten Sie, dass bei Verwendung der Stapelimportoption keine Benutzer ausgewählt werden können.</span><span class="sxs-lookup"><span data-stu-id="2a437-114">Note that it is not possible to select users when using the Batch import option.</span></span>

## <a name="run-the-import-as-a-batch-job"></a><span data-ttu-id="2a437-115">Import als Stapelverarbeitungslauf ausühren</span><span class="sxs-lookup"><span data-stu-id="2a437-115">Run the import as a batch job</span></span>
1. <span data-ttu-id="2a437-116">Der Benutzer wird mit dem aktuellen Sitzungsunternehmen als Standardunternehmen importiert.</span><span class="sxs-lookup"><span data-stu-id="2a437-116">User will be imported with the current session company as their default company.</span></span> <span data-ttu-id="2a437-117">Ändern Sie gegebenenfalls das aktuelle Unternehmen, bevor Sie Benutzer importieren.</span><span class="sxs-lookup"><span data-stu-id="2a437-117">Change current company if applicable before importing users.</span></span>
2. <span data-ttu-id="2a437-118">Wechseln Sie zu **Systemverwaltung > Benutzer > Benutzer**.</span><span class="sxs-lookup"><span data-stu-id="2a437-118">Go to **System administration > Users > Users**.</span></span>
3. <span data-ttu-id="2a437-119">Klicken Sie auf **Stapelimport**.</span><span class="sxs-lookup"><span data-stu-id="2a437-119">Click **Batch import**.</span></span>
4. <span data-ttu-id="2a437-120">Erweitern Sie den Abschnitt **Im Hintergrund ausführen**.</span><span class="sxs-lookup"><span data-stu-id="2a437-120">Expand the **Run in the background** section.</span></span>
4. <span data-ttu-id="2a437-121">Wählen Sie **Ja** im Feld **Stapelverarbeitung** aus.</span><span class="sxs-lookup"><span data-stu-id="2a437-121">Select **Yes** in the **Batch processing** field.</span></span>
6. <span data-ttu-id="2a437-122">Geben Sie im Feld **Stapelverarbeitungsgruppe** einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="2a437-122">In the **Batch group** field, enter or select a value.</span></span> <span data-ttu-id="2a437-123">Dieser Schritt ist optional.</span><span class="sxs-lookup"><span data-stu-id="2a437-123">This is an optional step.</span></span>  
7. <span data-ttu-id="2a437-124">Wählen Sie **Ja** im Feld **Privat** aus.</span><span class="sxs-lookup"><span data-stu-id="2a437-124">Select **Yes** in the **Private** field.</span></span> <span data-ttu-id="2a437-125">Dieser Schritt ist optional.</span><span class="sxs-lookup"><span data-stu-id="2a437-125">This is an optional step.</span></span>  
8. <span data-ttu-id="2a437-126">Wählen Sie **Ja** im Feld **Kritische Aufgabe** aus.</span><span class="sxs-lookup"><span data-stu-id="2a437-126">Select **Yes** in the **Critical job** field.</span></span> <span data-ttu-id="2a437-127">Dieser Schritt ist optional.</span><span class="sxs-lookup"><span data-stu-id="2a437-127">This is an optional step.</span></span>  
9. <span data-ttu-id="2a437-128">Wählen Sie im Feld **Kategorie überwachen** eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="2a437-128">In the **Monitoring category** field, select an option.</span></span>
10. <span data-ttu-id="2a437-129">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="2a437-129">Click **OK**.</span></span>

<span data-ttu-id="2a437-130">Nach Abschluss des Imports müssen den Benutzern Rollen zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="2a437-130">After import is completed, it will be required to assign roles to users.</span></span>

## <a name="run-in-a-sandbox-environment"></a><span data-ttu-id="2a437-131">Eine Sandkastenumgebung ausführen</span><span class="sxs-lookup"><span data-stu-id="2a437-131">Run in a sandbox environment</span></span>
1. <span data-ttu-id="2a437-132">Wählen Sie **Stapelimport** aus.</span><span class="sxs-lookup"><span data-stu-id="2a437-132">Select **Batch import**.</span></span>
2. <span data-ttu-id="2a437-133">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="2a437-133">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]