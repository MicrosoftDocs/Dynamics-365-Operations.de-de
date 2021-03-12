---
title: Eine Arbeitskraft konfigurieren, die das mobile Einzelvorgangsgerät verwendet
description: In diesem Thema wird erklärt, wie Sie dem Benutzerkonto einer Arbeitskraft die richtigen Rollen zuweisen und dann die Arbeitskraft für Fertigungsbereichregistrierungen aktivieren.
author: ShylaThompson
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, HcmWorker, JmgRegistrationSetupTouch, JmgRegistrationSetupAssignUsers
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 89b75936ea9c0f25f82175a1871088da8fd74ad6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980930"
---
# <a name="configure-a-worker-using-the-mobile-job-device"></a><span data-ttu-id="3db24-103">Eine Arbeitskraft konfigurieren, die das mobile Einzelvorgangsgerät verwendet</span><span class="sxs-lookup"><span data-stu-id="3db24-103">Configure a worker using the mobile job device</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3db24-104">In diesem Thema wird erklärt, wie Sie dem Benutzerkonto einer Arbeitskraft die richtigen Rollen zuweisen und dann die Arbeitskraft für Fertigungsbereichregistrierungen aktivieren.</span><span class="sxs-lookup"><span data-stu-id="3db24-104">This topic explains how to assign the correct roles to the user account of a worker, and then enable the worker to do shop floor registrations.</span></span>

## <a name="verify-that-a-worker-is-assigned-a-certain-role"></a><span data-ttu-id="3db24-105">Überprüfen, ob einer Arbeitskraft eine bestimmte Rolle zugewiesen ist</span><span class="sxs-lookup"><span data-stu-id="3db24-105">Verify that a worker is assigned a certain role</span></span>

<span data-ttu-id="3db24-106">Bei diesem Beispiel sollen Sie überprüfen, ob dem Benutzer „SHANNON“ die Maschinistenrolle zugewiesen ist, bevor Sie das Arbeitskraftkonto konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="3db24-106">For this example, verify that user "SHANNON" is assigned the machine operator role before you configure the worker account.</span></span>

1. <span data-ttu-id="3db24-107">Wechseln Sie zu **Navigationsbereich > Module > Systemverwaltung > Benutzer > Benutzer**.</span><span class="sxs-lookup"><span data-stu-id="3db24-107">Go to **Navigation pane > Modules > System administration > Users > Users**.</span></span>
2. <span data-ttu-id="3db24-108">Suche im Schnellfilter nach einem Benutzer.</span><span class="sxs-lookup"><span data-stu-id="3db24-108">Search for a user in the quick filter.</span></span> <span data-ttu-id="3db24-109">Geben Sie für dieses Beispiel `shannon` ein.</span><span class="sxs-lookup"><span data-stu-id="3db24-109">For this example, enter `shannon`.</span></span>
3. <span data-ttu-id="3db24-110">Wählen Sie den Link in der Spalte **Benutzerkennung** des Benutzerkontos aus, das angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="3db24-110">Select the link in the **User ID** column of the user account that appears.</span></span>
4. <span data-ttu-id="3db24-111">Wählen Sie in der Struktur **Benutzerrollen** den Eintrag **Rollen> Maschinist** aus.</span><span class="sxs-lookup"><span data-stu-id="3db24-111">In the **User's roles** tree, select **Roles > Machine operator**.</span></span>
5. <span data-ttu-id="3db24-112">Schließen Sie die Seiten **Benutzerdetails** und **Benutzer**, um zur Startseite zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="3db24-112">Close the **user details** and **users** pages to return to the home page.</span></span>

## <a name="configure-worker-account"></a><span data-ttu-id="3db24-113">Arbeitskräftekonten konfigurieren</span><span class="sxs-lookup"><span data-stu-id="3db24-113">Configure worker account</span></span>
1. <span data-ttu-id="3db24-114">Wechseln Sie zu **Navigationsbereich > Module > Personalverwaltung > Arbeitskräfte > Arbeitskräfte**.</span><span class="sxs-lookup"><span data-stu-id="3db24-114">Go to **Navigation pane > Modules > Human resources > Workers > Workers**.</span></span>
2. <span data-ttu-id="3db24-115">Suche im Schnellfilter nach einem Benutzer.</span><span class="sxs-lookup"><span data-stu-id="3db24-115">Search for a user in the quick filter.</span></span> <span data-ttu-id="3db24-116">Geben Sie für dieses Beispiel `shannon` ein.</span><span class="sxs-lookup"><span data-stu-id="3db24-116">For this example, enter `shannon`.</span></span>
3. <span data-ttu-id="3db24-117">Wählen Sie den Link in der Spalte **Name** des Benutzerkontos aus, das angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="3db24-117">Select the link in the **Name** column of the user account that appears.</span></span>
4. <span data-ttu-id="3db24-118">Wählen Sie die Registerkarte **Zeiterfassung** aus.</span><span class="sxs-lookup"><span data-stu-id="3db24-118">Select the **Time registration** tab.</span></span>
5. <span data-ttu-id="3db24-119">Wählen Sie **In Erfassungsterminals aktivieren** aus.</span><span class="sxs-lookup"><span data-stu-id="3db24-119">Select **Activate on registration terminals**.</span></span>
6. <span data-ttu-id="3db24-120">Geben Sie in den folgenden Feldern Werte ein, oder wählen Sie Werte aus:</span><span class="sxs-lookup"><span data-stu-id="3db24-120">Enter or select values in the following fields:</span></span>  

    - <span data-ttu-id="3db24-121">**Berechnungsgruppe**</span><span class="sxs-lookup"><span data-stu-id="3db24-121">**Calculation group**</span></span>  
    - <span data-ttu-id="3db24-122">**Standardberechnungsgruppe**</span><span class="sxs-lookup"><span data-stu-id="3db24-122">**Default calculation group**</span></span>  
    - <span data-ttu-id="3db24-123">**Genehmigungsgruppe**</span><span class="sxs-lookup"><span data-stu-id="3db24-123">**Approval group**</span></span>  
    - <span data-ttu-id="3db24-124">**Standardprofil**</span><span class="sxs-lookup"><span data-stu-id="3db24-124">**Standard profile**</span></span>  
    - <span data-ttu-id="3db24-125">**Profilgruppe**</span><span class="sxs-lookup"><span data-stu-id="3db24-125">**Profile group**</span></span>  

7. <span data-ttu-id="3db24-126">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="3db24-126">Select **OK**.</span></span>
8. <span data-ttu-id="3db24-127">Wählen Sie **Bearbeiten** aus, um eine Kennkartennummer für die neue Zeiterfassungsarbeitskraft einzugeben.</span><span class="sxs-lookup"><span data-stu-id="3db24-127">Select **Edit** to enter a badge number for the new time registration worker.</span></span> <span data-ttu-id="3db24-128">Geben Sie im Feld **Kennkartenkennung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="3db24-128">Enter a value in the **Badge ID** field.</span></span>
9. <span data-ttu-id="3db24-129">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="3db24-129">Select **Save**.</span></span>
10. <span data-ttu-id="3db24-130">Schließen Sie die Seiten **Details zur Arbeitskraft** und **Arbeitskräfte**.</span><span class="sxs-lookup"><span data-stu-id="3db24-130">Close the **Worker details** and **Workers** pages.</span></span>

## <a name="assign-worker-to-device-group"></a><span data-ttu-id="3db24-131">Arbeitskräfte zu Gerätegruppen zuweisen</span><span class="sxs-lookup"><span data-stu-id="3db24-131">Assign worker to device group</span></span>
1. <span data-ttu-id="3db24-132">Wechseln Sie zu **Produktionssteuerung > Einstellungen > Fertigungssteuerung > Einzelvorgangsliste für Geräte konfigurieren**.</span><span class="sxs-lookup"><span data-stu-id="3db24-132">Go to **Production control > Setup > Manufacturing execution > Configure job card for devices**.</span></span>
2. <span data-ttu-id="3db24-133">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="3db24-133">Select **Add**.</span></span>
3. <span data-ttu-id="3db24-134">Wählen Sie in der Liste die gewünschte Arbeitskraft aus.</span><span class="sxs-lookup"><span data-stu-id="3db24-134">In the list, select the desired worker.</span></span> <span data-ttu-id="3db24-135">Wählen Sie für dieses Beispiel **SHANNON** aus.</span><span class="sxs-lookup"><span data-stu-id="3db24-135">For this example, select **SHANNON**.</span></span>
4. <span data-ttu-id="3db24-136">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="3db24-136">Select **OK**.</span></span>
5. <span data-ttu-id="3db24-137">Wählen Sie **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="3db24-137">Select **Edit**.</span></span>
6. <span data-ttu-id="3db24-138">Im Feld **Produktionseinheit** können Sie den Standardfilter für die Arbeitskraft festlegen.</span><span class="sxs-lookup"><span data-stu-id="3db24-138">In the **Production unit** field, you can set the default filter for the worker.</span></span> <span data-ttu-id="3db24-139">Dadurch wird sichergestellt, dass nur Produktions-Einzelvorgänge für die ausgewählte Produktionseinheit angezeigt werden, wenn die Arbeitskraft sich beim Gerät anmeldet.</span><span class="sxs-lookup"><span data-stu-id="3db24-139">This will ensure that only production jobs for the selected production unit are shown when the worker logs on to the device.</span></span> <span data-ttu-id="3db24-140">Geben Sie den gewünschten Wert ein.</span><span class="sxs-lookup"><span data-stu-id="3db24-140">Enter the desired value.</span></span>
7. <span data-ttu-id="3db24-141">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="3db24-141">Close the page.</span></span>

