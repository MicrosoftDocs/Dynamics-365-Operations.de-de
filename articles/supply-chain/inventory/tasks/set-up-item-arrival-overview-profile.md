---
title: Übersichtsprofil zum Wareneingang einrichten
description: In diesem Thema geht es um die Einrichtung eines Ankunftsübersichtsprofils.
author: ShylaThompson
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WMSArrivalOverviewProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b0394d1b4288dac0ff913b125017571a8c0bc95a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829835"
---
# <a name="set-up-an-item-arrival-overview-profile"></a><span data-ttu-id="dca2c-103">Übersichtsprofil zum Wareneingang einrichten</span><span class="sxs-lookup"><span data-stu-id="dca2c-103">Set up an item arrival overview profile</span></span>

<span data-ttu-id="dca2c-104">[!include [banner](../../includes/banner.md)]]</span><span class="sxs-lookup"><span data-stu-id="dca2c-104">[!include [banner](../../includes/banner.md)]]</span></span>

<span data-ttu-id="dca2c-105">In diesem Thema geht es um die Einrichtung eines Ankunftsübersichtsprofils.</span><span class="sxs-lookup"><span data-stu-id="dca2c-105">This topic focuses on the setup of an arrival overview profile.</span></span> <span data-ttu-id="dca2c-106">Das Wareneingangsübersichtprofil ist eine Regelsammlung, die angewendet werden, wenn die Wareneingangsübersichtseite von einem Benutzer geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="dca2c-106">The arrival overview profile is a collection of rules that will be applied when the Arrival overview page is opened by a user.</span></span> <span data-ttu-id="dca2c-107">Sie können diese Prozedur im Demodatunternehmen USMF verwenden.</span><span class="sxs-lookup"><span data-stu-id="dca2c-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="dca2c-108">Diese Prozedur wird normalerweise von einem Sachbearbeiter Zugänge ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dca2c-108">This procedure would typically be carried out by a receiving clerk.</span></span>

1. <span data-ttu-id="dca2c-109">Gehen Sie im Navigationsbereich zu **Module > Bestandsverwaltung > Einrichtung > Verteilung > Verteilung > Ankunftsübersichtsprofile**.</span><span class="sxs-lookup"><span data-stu-id="dca2c-109">In the navigation pane, go to **Modules > Inventory management > Setup > Distribution > Arrival overview profiles**.</span></span>
2. <span data-ttu-id="dca2c-110">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="dca2c-110">Select **New**.</span></span> <span data-ttu-id="dca2c-111">Da Sie fast immer im gleichen Lagerort zusammenarbeiten, der vollständige LKW-Auslastungen auslädt, sollten Sie ein Wareneingangsübersichtprofil erstellen, um den Vorgang des zum Erfassen der empfangenen Artikeln zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="dca2c-111">Because you will almost always work in the same warehouse offloading full truck loads, you should create an arrival overview profile to simplify the process of registering received items.</span></span>  
3. <span data-ttu-id="dca2c-112">Geben Sie im Feld **Ankunftsübersicht Profilname** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="dca2c-112">In the **Arrival overview profile name** field, type a value.</span></span>
4. <span data-ttu-id="dca2c-113">Wählen Sie im Feld **Zeilen anzeigen** eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="dca2c-113">In the **Show lines** field, select an option.</span></span> <span data-ttu-id="dca2c-114">Wählen Sie aus, welche Zeilen für die Belege angezeigt werden sollen:</span><span class="sxs-lookup"><span data-stu-id="dca2c-114">Select which lines to show for the receipts:</span></span>  

    - <span data-ttu-id="dca2c-115">**Alle** - Zeigt alle Zeilen an, unabhängig vom Status.</span><span class="sxs-lookup"><span data-stu-id="dca2c-115">**All** – Show all lines, regardless of status.</span></span>   
    - <span data-ttu-id="dca2c-116">**In Bearbeitung** - Zeigt Zeilen für Belege an, in denen der Fortschritt vollständig oder teilweise ist.</span><span class="sxs-lookup"><span data-stu-id="dca2c-116">**In progress** – Show lines for receipts in which the progress is Complete or Partly.</span></span> <span data-ttu-id="dca2c-117">Dies bedeutet, dass die Menge für jede Position vollständig oder teilweise in einer Wareneingangserfassung erfasst wurde.</span><span class="sxs-lookup"><span data-stu-id="dca2c-117">This means that for each line, either the full quantity or part of the quantity has been registered in an arrival journal.</span></span>   
    - <span data-ttu-id="dca2c-118">**Nicht vollständig** - Zeigt Zeilen für Belege an, bei denen der Fortschritt None oder Partly ist.</span><span class="sxs-lookup"><span data-stu-id="dca2c-118">**Not complete** – Show lines for receipts in which the progress is None or Partly.</span></span> <span data-ttu-id="dca2c-119">Dies bedeutet, dass für jede Position keine oder nur ein Teil der Menge in einer Wareneingangserfassung erfasst wurde.</span><span class="sxs-lookup"><span data-stu-id="dca2c-119">This means that for each line, nothing or only part of the quantity has been registered in an arrival journal.</span></span>  

5. <span data-ttu-id="dca2c-120">Erweitern oder komprimieren Sie den Abschnitt **Anreiseoptionen**.</span><span class="sxs-lookup"><span data-stu-id="dca2c-120">Expand or collapse the **Arrival options** section.</span></span>
6. <span data-ttu-id="dca2c-121">Geben Sie im Feld **Tage vorwärts** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="dca2c-121">In the **Days forward** field, type a value.</span></span> <span data-ttu-id="dca2c-122">Damit werden die einen Filter festgelegt, um die Zugangspositionen anzeigen, die erwartet werden, innerhalb der nächsten Tage Zustellung des (abhängig von der Anzahl Sie festgelegt wurde).</span><span class="sxs-lookup"><span data-stu-id="dca2c-122">This sets a filter to show the receipt lines expected to be received within the next few days (depending on the number you set).</span></span>  
7. <span data-ttu-id="dca2c-123">Geben Sie im Feld **Tage zurück** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="dca2c-123">In the **Days back** field, type a value.</span></span> <span data-ttu-id="dca2c-124">Damit werden die einen Filter festgelegt, um die Zugangspositionen anzeigen, die erwartet werden, mehrere Tage aktuellen Monat empfangen zu werden.</span><span class="sxs-lookup"><span data-stu-id="dca2c-124">This sets a filter to show the receipt lines expected to be received a number of days before today.</span></span>  
8. <span data-ttu-id="dca2c-125">Geben Sie in das Feld **Lager** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="dca2c-125">In the **Warehouses** field, type a value.</span></span> <span data-ttu-id="dca2c-126">Filtern Sie nach einen oder mehrere Lagerorte.</span><span class="sxs-lookup"><span data-stu-id="dca2c-126">Filter on one or more warehouses.</span></span>  
9. <span data-ttu-id="dca2c-127">Wählen Sie im Feld **Lieferart** einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="dca2c-127">In the **Mode of delivery** field, select a value.</span></span> <span data-ttu-id="dca2c-128">Damit wird einen Filter festgelegt, um nur die Zugangspositionen mit diesem Lieferart anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="dca2c-128">This sets a filter to show only the receipt lines with this Mode of delivery.</span></span>  
10. <span data-ttu-id="dca2c-129">Wählen Sie im Feld **Name** WHS.</span><span class="sxs-lookup"><span data-stu-id="dca2c-129">In the **Name** field, select WHS.</span></span>
11. <span data-ttu-id="dca2c-130">Wählen Sie im Feld **Lager** Lager 24.</span><span class="sxs-lookup"><span data-stu-id="dca2c-130">In the **Warehouse** field, select warehouse 24.</span></span> <span data-ttu-id="dca2c-131">Dies ist der Standardlagerort, der für registrierte Zugangspositionen verwendet wird, die dieses Profil verwenden.</span><span class="sxs-lookup"><span data-stu-id="dca2c-131">This is the default warehouse that will be used for registered receipt lines that use this profile.</span></span>  
12. <span data-ttu-id="dca2c-132">Wählen Sie im Feld **Standort** **Baydoor**.</span><span class="sxs-lookup"><span data-stu-id="dca2c-132">In the **Location** field, select **Baydoor**.</span></span> <span data-ttu-id="dca2c-133">Dies ist der Standardlagerort, der für registrierte Zugangspositionen verwendet wird, die dieses Profil verwenden.</span><span class="sxs-lookup"><span data-stu-id="dca2c-133">This is the default location that will be used for registered receipt lines that use this profile.</span></span>  
13. <span data-ttu-id="dca2c-134">Erweitern oder komprimieren Sie den Abschnitt **Ankunftsabfrage Details**.</span><span class="sxs-lookup"><span data-stu-id="dca2c-134">Expand or collapse the **Arrival query details** section.</span></span>
14. <span data-ttu-id="dca2c-135">Wählen Sie im Feld **Einschränken auf Standort** den Standort 2 aus.</span><span class="sxs-lookup"><span data-stu-id="dca2c-135">In the **Restrict to site** field, select site 2.</span></span> <span data-ttu-id="dca2c-136">Damit wird einen Filter festgelegt, um nur die Zugangspositionen an diesem Lagerort anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="dca2c-136">This sets a filter to show only the receipt lines with this site.</span></span>  
15. <span data-ttu-id="dca2c-137">Setzen Sie die Option **Bestellungen** auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="dca2c-137">Set the **Purchase orders** option to **Yes**.</span></span> <span data-ttu-id="dca2c-138">Wählen Sie Positionen aus offenen Bestellungen aus.</span><span class="sxs-lookup"><span data-stu-id="dca2c-138">Select receipt lines from purchase orders.</span></span>  
16. <span data-ttu-id="dca2c-139">Stellen Sie die Option **Transfer** Bestellungen auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="dca2c-139">Set the **Transfer** orders option to **Yes**.</span></span> <span data-ttu-id="dca2c-140">Wählen Sie Positionen aus offenen Umlagerungsaufträgen aus.</span><span class="sxs-lookup"><span data-stu-id="dca2c-140">Select receipt lines from transfer orders.</span></span>  
17. <span data-ttu-id="dca2c-141">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="dca2c-141">Select **Save**.</span></span>
18. <span data-ttu-id="dca2c-142">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="dca2c-142">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]