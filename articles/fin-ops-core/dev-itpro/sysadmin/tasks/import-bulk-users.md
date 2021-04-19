---
title: Benutzer aus Azure Active Directory importieren
description: Diese Prozedur kann von Systemadministratoren verwendet werden, um ausgewählte Benutzer manuell oder viele Benutzer aus Azure Active Directory zu importieren.
author: peakerbl
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
ms.openlocfilehash: e9f03ae7197790c1aac6ebf3cb94ff7963b1291e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745788"
---
# <a name="import-users-from-azure-active-directory"></a><span data-ttu-id="47e8e-103">Benutzer aus Azure Active Directory importieren</span><span class="sxs-lookup"><span data-stu-id="47e8e-103">Import users from Azure Active Directory</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="import-select-users"></a><span data-ttu-id="47e8e-104">Ausgewählte Benutzer importieren</span><span class="sxs-lookup"><span data-stu-id="47e8e-104">Import select users</span></span>

<span data-ttu-id="47e8e-105">Diese Prozedur kann von Systemadministratoren verwendet werden, um ausgewählte Benutzer aus Azure Active Directory (Azure AD) zu importieren.</span><span class="sxs-lookup"><span data-stu-id="47e8e-105">This procedure can be used by system administrators to import select users from Azure Active Directory (Azure AD).</span></span>

1. <span data-ttu-id="47e8e-106">Der Benutzer wird mit dem aktuellen Sitzungsunternehmen als Standardunternehmen importiert.</span><span class="sxs-lookup"><span data-stu-id="47e8e-106">User will be imported with the current session company as their default company.</span></span> <span data-ttu-id="47e8e-107">Ändern Sie gegebenenfalls das aktuelle Unternehmen, bevor Sie Benutzer importieren.</span><span class="sxs-lookup"><span data-stu-id="47e8e-107">Change current company if applicable before importing users.</span></span>
2. <span data-ttu-id="47e8e-108">Wechseln Sie zu **Systemverwaltung > Benutzer > Benutzer**.</span><span class="sxs-lookup"><span data-stu-id="47e8e-108">Go to **System administration > Users > User** s.</span></span>
3. <span data-ttu-id="47e8e-109">Klicken Sie auf **Benutzer importieren**.</span><span class="sxs-lookup"><span data-stu-id="47e8e-109">Click **Import users**.</span></span>
4. <span data-ttu-id="47e8e-110">Wählen Sie die Benutzer aus, die importiert werden sollen, und wählen Sie dann **Benutzer importieren** aus.</span><span class="sxs-lookup"><span data-stu-id="47e8e-110">Select the users that should be imported and select **Import users**.</span></span>

<span data-ttu-id="47e8e-111">Nach Abschluss des Imports müssen den Benutzern Rollen zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="47e8e-111">After import is completed it will be required to assign roles to users.</span></span>

## <a name="import-users-in-bulk"></a><span data-ttu-id="47e8e-112">Massenimport von Benutzern</span><span class="sxs-lookup"><span data-stu-id="47e8e-112">Import users in bulk</span></span>

<span data-ttu-id="47e8e-113">Diese Prozedur kann von Systemadministratoren verwendet werden, um viele Benutzer aus Azure Active Directory zu importieren.</span><span class="sxs-lookup"><span data-stu-id="47e8e-113">This procedure can be used by system administrators to import a large number of users from Azure Active Directory.</span></span>
<span data-ttu-id="47e8e-114">Beachten Sie, dass bei Verwendung der Stapelimportoption keine Benutzer ausgewählt werden können.</span><span class="sxs-lookup"><span data-stu-id="47e8e-114">Note that it is not possible to select users when using the Batch import option.</span></span>

## <a name="run-the-import-as-a-batch-job"></a><span data-ttu-id="47e8e-115">Import als Stapelverarbeitungslauf ausühren</span><span class="sxs-lookup"><span data-stu-id="47e8e-115">Run the import as a batch job</span></span>
1. <span data-ttu-id="47e8e-116">Der Benutzer wird mit dem aktuellen Sitzungsunternehmen als Standardunternehmen importiert.</span><span class="sxs-lookup"><span data-stu-id="47e8e-116">User will be imported with the current session company as their default company.</span></span> <span data-ttu-id="47e8e-117">Ändern Sie gegebenenfalls das aktuelle Unternehmen, bevor Sie Benutzer importieren.</span><span class="sxs-lookup"><span data-stu-id="47e8e-117">Change current company if applicable before importing users.</span></span>
2. <span data-ttu-id="47e8e-118">Wechseln Sie zu **Systemverwaltung > Benutzer > Benutzer**.</span><span class="sxs-lookup"><span data-stu-id="47e8e-118">Go to **System administration > Users > Users**.</span></span>
3. <span data-ttu-id="47e8e-119">Klicken Sie auf **Stapelimport**.</span><span class="sxs-lookup"><span data-stu-id="47e8e-119">Click **Batch import**.</span></span>
4. <span data-ttu-id="47e8e-120">Erweitern Sie den Abschnitt **Im Hintergrund ausführen**.</span><span class="sxs-lookup"><span data-stu-id="47e8e-120">Expand the **Run in the background** section.</span></span>
4. <span data-ttu-id="47e8e-121">Wählen Sie **Ja** im Feld **Stapelverarbeitung** aus.</span><span class="sxs-lookup"><span data-stu-id="47e8e-121">Select **Yes** in the **Batch processing** field.</span></span>
6. <span data-ttu-id="47e8e-122">Geben Sie im Feld **Stapelverarbeitungsgruppe** einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="47e8e-122">In the **Batch group** field, enter or select a value.</span></span> <span data-ttu-id="47e8e-123">Dieser Schritt ist optional.</span><span class="sxs-lookup"><span data-stu-id="47e8e-123">This is an optional step.</span></span>  
7. <span data-ttu-id="47e8e-124">Wählen Sie **Ja** im Feld **Privat** aus.</span><span class="sxs-lookup"><span data-stu-id="47e8e-124">Select **Yes** in the **Private** field.</span></span> <span data-ttu-id="47e8e-125">Dieser Schritt ist optional.</span><span class="sxs-lookup"><span data-stu-id="47e8e-125">This is an optional step.</span></span>  
8. <span data-ttu-id="47e8e-126">Wählen Sie **Ja** im Feld **Kritische Aufgabe** aus.</span><span class="sxs-lookup"><span data-stu-id="47e8e-126">Select **Yes** in the **Critical job** field.</span></span> <span data-ttu-id="47e8e-127">Dieser Schritt ist optional.</span><span class="sxs-lookup"><span data-stu-id="47e8e-127">This is an optional step.</span></span>  
9. <span data-ttu-id="47e8e-128">Wählen Sie im Feld **Kategorie überwachen** eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="47e8e-128">In the **Monitoring category** field, select an option.</span></span>
10. <span data-ttu-id="47e8e-129">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="47e8e-129">Click **OK**.</span></span>

<span data-ttu-id="47e8e-130">Nach Abschluss des Imports müssen den Benutzern Rollen zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="47e8e-130">After import is completed, it will be required to assign roles to users.</span></span>

## <a name="run-in-a-sandbox-environment"></a><span data-ttu-id="47e8e-131">Eine Sandkastenumgebung ausführen</span><span class="sxs-lookup"><span data-stu-id="47e8e-131">Run in a sandbox environment</span></span>
1. <span data-ttu-id="47e8e-132">Wählen Sie **Stapelimport** aus.</span><span class="sxs-lookup"><span data-stu-id="47e8e-132">Select **Batch import**.</span></span>
2. <span data-ttu-id="47e8e-133">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="47e8e-133">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]