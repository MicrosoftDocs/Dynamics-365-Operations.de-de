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
ms.openlocfilehash: 6210cdeed99f26a6b58b75d9f5405c0e1ee5aef1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5213329"
---
# <a name="configure-a-worker-using-the-mobile-job-device"></a><span data-ttu-id="e3c23-103">Eine Arbeitskraft konfigurieren, die das mobile Einzelvorgangsgerät verwendet</span><span class="sxs-lookup"><span data-stu-id="e3c23-103">Configure a worker using the mobile job device</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e3c23-104">In diesem Thema wird erklärt, wie Sie dem Benutzerkonto einer Arbeitskraft die richtigen Rollen zuweisen und dann die Arbeitskraft für Fertigungsbereichregistrierungen aktivieren.</span><span class="sxs-lookup"><span data-stu-id="e3c23-104">This topic explains how to assign the correct roles to the user account of a worker, and then enable the worker to do shop floor registrations.</span></span>

## <a name="verify-that-a-worker-is-assigned-a-certain-role"></a><span data-ttu-id="e3c23-105">Überprüfen, ob einer Arbeitskraft eine bestimmte Rolle zugewiesen ist</span><span class="sxs-lookup"><span data-stu-id="e3c23-105">Verify that a worker is assigned a certain role</span></span>

<span data-ttu-id="e3c23-106">Bei diesem Beispiel sollen Sie überprüfen, ob dem Benutzer „SHANNON“ die Maschinistenrolle zugewiesen ist, bevor Sie das Arbeitskraftkonto konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="e3c23-106">For this example, verify that user "SHANNON" is assigned the machine operator role before you configure the worker account.</span></span>

1. <span data-ttu-id="e3c23-107">Wechseln Sie zu **Navigationsbereich > Module > Systemverwaltung > Benutzer > Benutzer**.</span><span class="sxs-lookup"><span data-stu-id="e3c23-107">Go to **Navigation pane > Modules > System administration > Users > Users**.</span></span>
2. <span data-ttu-id="e3c23-108">Suche im Schnellfilter nach einem Benutzer.</span><span class="sxs-lookup"><span data-stu-id="e3c23-108">Search for a user in the quick filter.</span></span> <span data-ttu-id="e3c23-109">Geben Sie für dieses Beispiel `shannon` ein.</span><span class="sxs-lookup"><span data-stu-id="e3c23-109">For this example, enter `shannon`.</span></span>
3. <span data-ttu-id="e3c23-110">Wählen Sie den Link in der Spalte **Benutzerkennung** des Benutzerkontos aus, das angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e3c23-110">Select the link in the **User ID** column of the user account that appears.</span></span>
4. <span data-ttu-id="e3c23-111">Wählen Sie in der Struktur **Benutzerrollen** den Eintrag **Rollen> Maschinist** aus.</span><span class="sxs-lookup"><span data-stu-id="e3c23-111">In the **User's roles** tree, select **Roles > Machine operator**.</span></span>
5. <span data-ttu-id="e3c23-112">Schließen Sie die Seiten **Benutzerdetails** und **Benutzer**, um zur Startseite zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="e3c23-112">Close the **user details** and **users** pages to return to the home page.</span></span>

## <a name="configure-worker-account"></a><span data-ttu-id="e3c23-113">Arbeitskräftekonten konfigurieren</span><span class="sxs-lookup"><span data-stu-id="e3c23-113">Configure worker account</span></span>
1. <span data-ttu-id="e3c23-114">Wechseln Sie zu **Navigationsbereich > Module > Personalverwaltung > Arbeitskräfte > Arbeitskräfte**.</span><span class="sxs-lookup"><span data-stu-id="e3c23-114">Go to **Navigation pane > Modules > Human resources > Workers > Workers**.</span></span>
2. <span data-ttu-id="e3c23-115">Suche im Schnellfilter nach einem Benutzer.</span><span class="sxs-lookup"><span data-stu-id="e3c23-115">Search for a user in the quick filter.</span></span> <span data-ttu-id="e3c23-116">Geben Sie für dieses Beispiel `shannon` ein.</span><span class="sxs-lookup"><span data-stu-id="e3c23-116">For this example, enter `shannon`.</span></span>
3. <span data-ttu-id="e3c23-117">Wählen Sie den Link in der Spalte **Name** des Benutzerkontos aus, das angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e3c23-117">Select the link in the **Name** column of the user account that appears.</span></span>
4. <span data-ttu-id="e3c23-118">Wählen Sie die Registerkarte **Zeiterfassung** aus.</span><span class="sxs-lookup"><span data-stu-id="e3c23-118">Select the **Time registration** tab.</span></span>
5. <span data-ttu-id="e3c23-119">Wählen Sie **In Erfassungsterminals aktivieren** aus.</span><span class="sxs-lookup"><span data-stu-id="e3c23-119">Select **Activate on registration terminals**.</span></span>
6. <span data-ttu-id="e3c23-120">Geben Sie in den folgenden Feldern Werte ein, oder wählen Sie Werte aus:</span><span class="sxs-lookup"><span data-stu-id="e3c23-120">Enter or select values in the following fields:</span></span>  

    - <span data-ttu-id="e3c23-121">**Berechnungsgruppe**</span><span class="sxs-lookup"><span data-stu-id="e3c23-121">**Calculation group**</span></span>  
    - <span data-ttu-id="e3c23-122">**Standardberechnungsgruppe**</span><span class="sxs-lookup"><span data-stu-id="e3c23-122">**Default calculation group**</span></span>  
    - <span data-ttu-id="e3c23-123">**Genehmigungsgruppe**</span><span class="sxs-lookup"><span data-stu-id="e3c23-123">**Approval group**</span></span>  
    - <span data-ttu-id="e3c23-124">**Standardprofil**</span><span class="sxs-lookup"><span data-stu-id="e3c23-124">**Standard profile**</span></span>  
    - <span data-ttu-id="e3c23-125">**Profilgruppe**</span><span class="sxs-lookup"><span data-stu-id="e3c23-125">**Profile group**</span></span>  

7. <span data-ttu-id="e3c23-126">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="e3c23-126">Select **OK**.</span></span>
8. <span data-ttu-id="e3c23-127">Wählen Sie **Bearbeiten** aus, um eine Kennkartennummer für die neue Zeiterfassungsarbeitskraft einzugeben.</span><span class="sxs-lookup"><span data-stu-id="e3c23-127">Select **Edit** to enter a badge number for the new time registration worker.</span></span> <span data-ttu-id="e3c23-128">Geben Sie im Feld **Kennkartenkennung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="e3c23-128">Enter a value in the **Badge ID** field.</span></span>
9. <span data-ttu-id="e3c23-129">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="e3c23-129">Select **Save**.</span></span>
10. <span data-ttu-id="e3c23-130">Schließen Sie die Seiten **Details zur Arbeitskraft** und **Arbeitskräfte**.</span><span class="sxs-lookup"><span data-stu-id="e3c23-130">Close the **Worker details** and **Workers** pages.</span></span>

## <a name="assign-worker-to-device-group"></a><span data-ttu-id="e3c23-131">Arbeitskräfte zu Gerätegruppen zuweisen</span><span class="sxs-lookup"><span data-stu-id="e3c23-131">Assign worker to device group</span></span>
1. <span data-ttu-id="e3c23-132">Wechseln Sie zu **Produktionssteuerung > Einstellungen > Fertigungssteuerung > Einzelvorgangsliste für Geräte konfigurieren**.</span><span class="sxs-lookup"><span data-stu-id="e3c23-132">Go to **Production control > Setup > Manufacturing execution > Configure job card for devices**.</span></span>
2. <span data-ttu-id="e3c23-133">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="e3c23-133">Select **Add**.</span></span>
3. <span data-ttu-id="e3c23-134">Wählen Sie in der Liste die gewünschte Arbeitskraft aus.</span><span class="sxs-lookup"><span data-stu-id="e3c23-134">In the list, select the desired worker.</span></span> <span data-ttu-id="e3c23-135">Wählen Sie für dieses Beispiel **SHANNON** aus.</span><span class="sxs-lookup"><span data-stu-id="e3c23-135">For this example, select **SHANNON**.</span></span>
4. <span data-ttu-id="e3c23-136">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="e3c23-136">Select **OK**.</span></span>
5. <span data-ttu-id="e3c23-137">Wählen Sie **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="e3c23-137">Select **Edit**.</span></span>
6. <span data-ttu-id="e3c23-138">Im Feld **Produktionseinheit** können Sie den Standardfilter für die Arbeitskraft festlegen.</span><span class="sxs-lookup"><span data-stu-id="e3c23-138">In the **Production unit** field, you can set the default filter for the worker.</span></span> <span data-ttu-id="e3c23-139">Dadurch wird sichergestellt, dass nur Produktions-Einzelvorgänge für die ausgewählte Produktionseinheit angezeigt werden, wenn die Arbeitskraft sich beim Gerät anmeldet.</span><span class="sxs-lookup"><span data-stu-id="e3c23-139">This will ensure that only production jobs for the selected production unit are shown when the worker logs on to the device.</span></span> <span data-ttu-id="e3c23-140">Geben Sie den gewünschten Wert ein.</span><span class="sxs-lookup"><span data-stu-id="e3c23-140">Enter the desired value.</span></span>
7. <span data-ttu-id="e3c23-141">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="e3c23-141">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]