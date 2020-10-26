---
title: Übersichtsprofil zum Wareneingang einrichten
description: In diesem Thema geht es um die Einrichtung eines Ankunftsübersichtsprofils.
author: ShylaThompson
manager: tfehr
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverviewProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 69389dd3a53ffec11116e16512bd038b45eda4d4
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3979691"
---
# <a name="set-up-an-item-arrival-overview-profile"></a><span data-ttu-id="935db-103">Übersichtsprofil zum Wareneingang einrichten</span><span class="sxs-lookup"><span data-stu-id="935db-103">Set up an item arrival overview profile</span></span>

<span data-ttu-id="935db-104">[!include [banner](../../includes/banner.md)]]</span><span class="sxs-lookup"><span data-stu-id="935db-104">[!include [banner](../../includes/banner.md)]]</span></span>

<span data-ttu-id="935db-105">In diesem Thema geht es um die Einrichtung eines Ankunftsübersichtsprofils.</span><span class="sxs-lookup"><span data-stu-id="935db-105">This topic focuses on the setup of an arrival overview profile.</span></span> <span data-ttu-id="935db-106">Das Wareneingangsübersichtprofil ist eine Regelsammlung, die angewendet werden, wenn die Wareneingangsübersichtseite von einem Benutzer geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="935db-106">The arrival overview profile is a collection of rules that will be applied when the Arrival overview page is opened by a user.</span></span> <span data-ttu-id="935db-107">Sie können diese Prozedur im Demodatunternehmen USMF verwenden.</span><span class="sxs-lookup"><span data-stu-id="935db-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="935db-108">Diese Prozedur wird normalerweise von einem Sachbearbeiter Zugänge ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="935db-108">This procedure would typically be carried out by a receiving clerk.</span></span>

1. <span data-ttu-id="935db-109">Gehen Sie im Navigationsbereich zu **Module > Bestandsverwaltung > Einrichtung > Verteilung > Verteilung > Ankunftsübersichtsprofile**.</span><span class="sxs-lookup"><span data-stu-id="935db-109">In the navigation pane, go to **Modules > Inventory management > Setup > Distribution > Arrival overview profiles**.</span></span>
2. <span data-ttu-id="935db-110">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="935db-110">Select **New**.</span></span> <span data-ttu-id="935db-111">Da Sie fast immer im gleichen Lagerort zusammenarbeiten, der vollständige LKW-Auslastungen auslädt, sollten Sie ein Wareneingangsübersichtprofil erstellen, um den Vorgang des zum Erfassen der empfangenen Artikeln zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="935db-111">Because you will almost always work in the same warehouse offloading full truck loads, you should create an arrival overview profile to simplify the process of registering received items.</span></span>  
3. <span data-ttu-id="935db-112">Geben Sie im Feld **Ankunftsübersicht Profilname** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="935db-112">In the **Arrival overview profile name** field, type a value.</span></span>
4. <span data-ttu-id="935db-113">Wählen Sie im Feld **Zeilen anzeigen** eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="935db-113">In the **Show lines** field, select an option.</span></span> <span data-ttu-id="935db-114">Wählen Sie aus, welche Zeilen für die Belege angezeigt werden sollen:</span><span class="sxs-lookup"><span data-stu-id="935db-114">Select which lines to show for the receipts:</span></span>  

    - <span data-ttu-id="935db-115">**Alle** - Zeigt alle Zeilen an, unabhängig vom Status.</span><span class="sxs-lookup"><span data-stu-id="935db-115">**All** – Show all lines, regardless of status.</span></span>   
    - <span data-ttu-id="935db-116">**In Bearbeitung** - Zeigt Zeilen für Belege an, in denen der Fortschritt vollständig oder teilweise ist.</span><span class="sxs-lookup"><span data-stu-id="935db-116">**In progress** – Show lines for receipts in which the progress is Complete or Partly.</span></span> <span data-ttu-id="935db-117">Dies bedeutet, dass die Menge für jede Position vollständig oder teilweise in einer Wareneingangserfassung erfasst wurde.</span><span class="sxs-lookup"><span data-stu-id="935db-117">This means that for each line, either the full quantity or part of the quantity has been registered in an arrival journal.</span></span>   
    - <span data-ttu-id="935db-118">**Nicht vollständig** - Zeigt Zeilen für Belege an, bei denen der Fortschritt None oder Partly ist.</span><span class="sxs-lookup"><span data-stu-id="935db-118">**Not complete** – Show lines for receipts in which the progress is None or Partly.</span></span> <span data-ttu-id="935db-119">Dies bedeutet, dass für jede Position keine oder nur ein Teil der Menge in einer Wareneingangserfassung erfasst wurde.</span><span class="sxs-lookup"><span data-stu-id="935db-119">This means that for each line, nothing or only part of the quantity has been registered in an arrival journal.</span></span>  

5. <span data-ttu-id="935db-120">Erweitern oder komprimieren Sie den Abschnitt **Anreiseoptionen**.</span><span class="sxs-lookup"><span data-stu-id="935db-120">Expand or collapse the **Arrival options** section.</span></span>
6. <span data-ttu-id="935db-121">Geben Sie im Feld **Tage vorwärts** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="935db-121">In the **Days forward** field, type a value.</span></span> <span data-ttu-id="935db-122">Damit werden die einen Filter festgelegt, um die Zugangspositionen anzeigen, die erwartet werden, innerhalb der nächsten Tage Zustellung des (abhängig von der Anzahl Sie festgelegt wurde).</span><span class="sxs-lookup"><span data-stu-id="935db-122">This sets a filter to show the receipt lines expected to be received within the next few days (depending on the number you set).</span></span>  
7. <span data-ttu-id="935db-123">Geben Sie im Feld **Tage zurück** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="935db-123">In the **Days back** field, type a value.</span></span> <span data-ttu-id="935db-124">Damit werden die einen Filter festgelegt, um die Zugangspositionen anzeigen, die erwartet werden, mehrere Tage aktuellen Monat empfangen zu werden.</span><span class="sxs-lookup"><span data-stu-id="935db-124">This sets a filter to show the receipt lines expected to be received a number of days before today.</span></span>  
8. <span data-ttu-id="935db-125">Geben Sie in das Feld **Lager** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="935db-125">In the **Warehouses** field, type a value.</span></span> <span data-ttu-id="935db-126">Filtern Sie nach einen oder mehrere Lagerorte.</span><span class="sxs-lookup"><span data-stu-id="935db-126">Filter on one or more warehouses.</span></span>  
9. <span data-ttu-id="935db-127">Wählen Sie im Feld **Lieferart** einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="935db-127">In the **Mode of delivery** field, select a value.</span></span> <span data-ttu-id="935db-128">Damit wird einen Filter festgelegt, um nur die Zugangspositionen mit diesem Lieferart anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="935db-128">This sets a filter to show only the receipt lines with this Mode of delivery.</span></span>  
10. <span data-ttu-id="935db-129">Wählen Sie im Feld **Name** WHS.</span><span class="sxs-lookup"><span data-stu-id="935db-129">In the **Name** field, select WHS.</span></span>
11. <span data-ttu-id="935db-130">Wählen Sie im Feld **Lager** Lager 24.</span><span class="sxs-lookup"><span data-stu-id="935db-130">In the **Warehouse** field, select warehouse 24.</span></span> <span data-ttu-id="935db-131">Dies ist der Standardlagerort, der für registrierte Zugangspositionen verwendet wird, die dieses Profil verwenden.</span><span class="sxs-lookup"><span data-stu-id="935db-131">This is the default warehouse that will be used for registered receipt lines that use this profile.</span></span>  
12. <span data-ttu-id="935db-132">Wählen Sie im Feld **Standort** **Baydoor**.</span><span class="sxs-lookup"><span data-stu-id="935db-132">In the **Location** field, select **Baydoor**.</span></span> <span data-ttu-id="935db-133">Dies ist der Standardlagerort, der für registrierte Zugangspositionen verwendet wird, die dieses Profil verwenden.</span><span class="sxs-lookup"><span data-stu-id="935db-133">This is the default location that will be used for registered receipt lines that use this profile.</span></span>  
13. <span data-ttu-id="935db-134">Erweitern oder komprimieren Sie den Abschnitt **Ankunftsabfrage Details**.</span><span class="sxs-lookup"><span data-stu-id="935db-134">Expand or collapse the **Arrival query details** section.</span></span>
14. <span data-ttu-id="935db-135">Wählen Sie im Feld **Einschränken auf Standort** den Standort 2 aus.</span><span class="sxs-lookup"><span data-stu-id="935db-135">In the **Restrict to site** field, select site 2.</span></span> <span data-ttu-id="935db-136">Damit wird einen Filter festgelegt, um nur die Zugangspositionen an diesem Lagerort anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="935db-136">This sets a filter to show only the receipt lines with this site.</span></span>  
15. <span data-ttu-id="935db-137">Setzen Sie die Option **Bestellungen** auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="935db-137">Set the **Purchase orders** option to **Yes**.</span></span> <span data-ttu-id="935db-138">Wählen Sie Positionen aus offenen Bestellungen aus.</span><span class="sxs-lookup"><span data-stu-id="935db-138">Select receipt lines from purchase orders.</span></span>  
16. <span data-ttu-id="935db-139">Stellen Sie die Option **Transfer** Bestellungen auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="935db-139">Set the **Transfer** orders option to **Yes**.</span></span> <span data-ttu-id="935db-140">Wählen Sie Positionen aus offenen Umlagerungsaufträgen aus.</span><span class="sxs-lookup"><span data-stu-id="935db-140">Select receipt lines from transfer orders.</span></span>  
17. <span data-ttu-id="935db-141">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="935db-141">Select **Save**.</span></span>
18. <span data-ttu-id="935db-142">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="935db-142">Close the page.</span></span>

