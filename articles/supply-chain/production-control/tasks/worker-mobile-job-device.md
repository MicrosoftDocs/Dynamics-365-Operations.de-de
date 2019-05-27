---
title: Eine Arbeitskraft konfigurieren, die das mobile Einzelvorgangsgerät verwendet
description: Dieses Verfahren zeigt Ihnen an, wie Sie richtigen Rollen zu einem Benutzerkonto einer Arbeitskraft zuzuordnen und dann die Arbeitskraft für Fertigungsbereichregistrierungen aktivieren.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, HcmWorker, JmgRegistrationSetupTouch, JmgRegistrationSetupAssignUsers
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1bb4d806810660e55ef13a9ff21c07e0ce194496
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571357"
---
# <a name="configure-a-worker-using-the-mobile-job-device"></a><span data-ttu-id="7a0c9-103">Eine Arbeitskraft konfigurieren, die das mobile Einzelvorgangsgerät verwendet</span><span class="sxs-lookup"><span data-stu-id="7a0c9-103">Configure a worker using the mobile job device</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7a0c9-104">Dieses Verfahren zeigt Ihnen an, wie Sie richtigen Rollen zu einem Benutzerkonto einer Arbeitskraft zuzuordnen und dann die Arbeitskraft für Fertigungsbereichregistrierungen aktivieren.</span><span class="sxs-lookup"><span data-stu-id="7a0c9-104">This procedure shows you how to assign the correct roles to the user account of a worker, and then enable the worker to do shop floor registrations.</span></span>


## <a name="assign-roles-to-user-account"></a><span data-ttu-id="7a0c9-105">Zuweisen von Rollen zum Benutzerkonto</span><span class="sxs-lookup"><span data-stu-id="7a0c9-105">Assign roles to user account</span></span>
1. <span data-ttu-id="7a0c9-106">Wechseln Sie zu "Systemverwaltung" > "Benutzer" > "Benutzer".</span><span class="sxs-lookup"><span data-stu-id="7a0c9-106">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="7a0c9-107">Verwenden Sie den Schnellfilter, um nach dem Namen einer Arbeitskraft zu filtern, deren Benutzerkonto der Rolle Maschinist zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="7a0c9-107">Use the Quick Filter to filter on the name of a worker where the user account is associated with the machine operator role.</span></span> <span data-ttu-id="7a0c9-108">In den Beispieldaten wäre der Name "Shannon".</span><span class="sxs-lookup"><span data-stu-id="7a0c9-108">In the sample data, the name would be Shannon.</span></span>
3. <span data-ttu-id="7a0c9-109">Markieren Sie den Benutzerkontodatensatz.</span><span class="sxs-lookup"><span data-stu-id="7a0c9-109">Highlight the user account record.</span></span>
4. <span data-ttu-id="7a0c9-110">Klicken Sie in der Liste auf den Link "Name" in der ausgewählten Zeile, um die Details des Benutzerkontos anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="7a0c9-110">In the list, click the "Name" link in the selected row to view the details of the user account.</span></span>
5. <span data-ttu-id="7a0c9-111">Wählen Sie in der Struktur "Rollen\Maschinist" aus.</span><span class="sxs-lookup"><span data-stu-id="7a0c9-111">In the tree, select 'Roles\Machine operator'.</span></span>
6. <span data-ttu-id="7a0c9-112">Schließen Sie die Seite "Benutzerkontodetails".</span><span class="sxs-lookup"><span data-stu-id="7a0c9-112">Close the user account details page.</span></span>
7. <span data-ttu-id="7a0c9-113">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="7a0c9-113">Close the page.</span></span>

## <a name="configure-worker-account"></a><span data-ttu-id="7a0c9-114">Konfigurieren von Arbeitskräftekonten</span><span class="sxs-lookup"><span data-stu-id="7a0c9-114">Configure worker account.</span></span>
1. <span data-ttu-id="7a0c9-115">Wechseln Sie zu "Personalverwaltung" > "Arbeitskräfte" > "Arbeitskräfte".</span><span class="sxs-lookup"><span data-stu-id="7a0c9-115">Go to Human resources > Workers > Workers.</span></span>
2. <span data-ttu-id="7a0c9-116">Verwenden Sie den Schnellfilter, um nach dem Namen einer Arbeitskraft zu filtern, deren Benutzerkonto der Rolle Maschinist zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="7a0c9-116">Use the Quick Filter to filter on the name of a worker where the user account is associated with the machine operator role.</span></span> <span data-ttu-id="7a0c9-117">In den Beispieldaten wäre der Name "Shannon".</span><span class="sxs-lookup"><span data-stu-id="7a0c9-117">In the sample data, the name would be Shannon.</span></span>
3. <span data-ttu-id="7a0c9-118">Markieren Sie den Benutzerkontodatensatz.</span><span class="sxs-lookup"><span data-stu-id="7a0c9-118">Highlight the user account record.</span></span>
4. <span data-ttu-id="7a0c9-119">Klicken Sie in der Liste auf den Link "Name" in der ausgewählten Zeile, um die Details des Benutzerkontos anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="7a0c9-119">In the list, click the "Name" link in the selected row to view the details of the user account.</span></span>
5. <span data-ttu-id="7a0c9-120">Klicken Sie auf die Registerkarte "Anstellung".</span><span class="sxs-lookup"><span data-stu-id="7a0c9-120">Click the Employment tab.</span></span>
6. <span data-ttu-id="7a0c9-121">Erweitern Sie das Zeiterfassungs-Inforegister und klicken auf "In Erfassungsterminals aktivieren".</span><span class="sxs-lookup"><span data-stu-id="7a0c9-121">Expand the Time registration FastTab and click Activate on registration terminals.</span></span>
7. <span data-ttu-id="7a0c9-122">Klicken Sie auf "In Erfassungsterminals aktivieren".</span><span class="sxs-lookup"><span data-stu-id="7a0c9-122">Click Activate on registration terminals.</span></span>
8. <span data-ttu-id="7a0c9-123">Geben Sie im Feld "Berechnungsgruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="7a0c9-123">In the Calculation group field, enter or select a value.</span></span>
9. <span data-ttu-id="7a0c9-124">Geben Sie im Feld "Standardberechnungsgruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="7a0c9-124">In the Default calculation group field, enter or select a value.</span></span>
10. <span data-ttu-id="7a0c9-125">Geben Sie im Feld "Genehmigungsgruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="7a0c9-125">In the Approval group field, enter or select a value.</span></span>
11. <span data-ttu-id="7a0c9-126">Geben Sie im Feld "Standardprofil" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="7a0c9-126">In the Standard profile field, enter or select a value.</span></span>
12. <span data-ttu-id="7a0c9-127">Geben Sie im Feld "Profilgruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="7a0c9-127">In the Profile group field, enter or select a value.</span></span>
13. <span data-ttu-id="7a0c9-128">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="7a0c9-128">Click OK.</span></span>
14. <span data-ttu-id="7a0c9-129">Klicken Sie auf "Bearbeiten", um eine Nummer auf der Kennkarte für die neue Zeiterfassungsarbeitskraft einzugeben.</span><span class="sxs-lookup"><span data-stu-id="7a0c9-129">Click Edit to enter a badge number for the new time registration worker.</span></span>
15. <span data-ttu-id="7a0c9-130">Geben Sie im Feld "Kennkartenkennung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="7a0c9-130">In the Badge ID field, type a value.</span></span>
16. <span data-ttu-id="7a0c9-131">Klicken Sie auf Speichern.</span><span class="sxs-lookup"><span data-stu-id="7a0c9-131">Click Save.</span></span>
17. <span data-ttu-id="7a0c9-132">Verwenden Sie das Tastenkürzel SaveRecord.</span><span class="sxs-lookup"><span data-stu-id="7a0c9-132">Use the SaveRecord shortcut.</span></span>
18. <span data-ttu-id="7a0c9-133">Schließen Sie die Seite "Arbeitskräftedetails".</span><span class="sxs-lookup"><span data-stu-id="7a0c9-133">Close the worker details page.</span></span>
19. <span data-ttu-id="7a0c9-134">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="7a0c9-134">Close the page.</span></span>

## <a name="assign-worker-to-device-group"></a><span data-ttu-id="7a0c9-135">Zuweisen von Arbeitskräften zu Gerätegruppen</span><span class="sxs-lookup"><span data-stu-id="7a0c9-135">Assign worker to device group.</span></span>
1. <span data-ttu-id="7a0c9-136">Wechseln Sie zu "Produktionssteuerung" > "Einrichtung" > "Fertigungssteuerung" > "Einzelvorgangsliste für Geräte konfigurieren".</span><span class="sxs-lookup"><span data-stu-id="7a0c9-136">Go to Production control > Setup > Manufacturing execution > Configure job card for devices.</span></span>
2. <span data-ttu-id="7a0c9-137">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="7a0c9-137">Click Add.</span></span>
3. <span data-ttu-id="7a0c9-138">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="7a0c9-138">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="7a0c9-139">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="7a0c9-139">Click OK.</span></span>
5. <span data-ttu-id="7a0c9-140">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="7a0c9-140">Click Edit.</span></span>
6. <span data-ttu-id="7a0c9-141">Im Feld "Produktionseinheits" können Sie den standardmäßigen Filter für die Arbeitskraft festlegen.</span><span class="sxs-lookup"><span data-stu-id="7a0c9-141">In the Production unit field, you can set the default filter for the worker.</span></span> <span data-ttu-id="7a0c9-142">Dadurch wird sichergestellt, dass nur Produktions-Einzelvorgänge für die ausgewählte Produktionseinheit angezeigt werden, wenn die Arbeitskraft sich beim Gerät anmeldet.</span><span class="sxs-lookup"><span data-stu-id="7a0c9-142">This will ensure that only production jobs for the selected production unit are shown when the worker logs on to the device.</span></span>
7. <span data-ttu-id="7a0c9-143">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="7a0c9-143">Close the page.</span></span>

