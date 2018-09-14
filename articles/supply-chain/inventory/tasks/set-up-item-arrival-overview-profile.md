--- 
title: "Übersichtsprofil zum Wareneingang einrichten"
description: "Dieser Aufgabe konzentriert sich auf den Einstellungen eines Wareneingangsübersichtprofils."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSArrivalOverviewProfile
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 2b61d77072358083a35de28003176cb88e53453e
ms.contentlocale: de-de
ms.lasthandoff: 09/14/2018

---
# <a name="set-up-an-item-arrival-overview-profile"></a><span data-ttu-id="418c1-103">Übersichtsprofil zum Wareneingang einrichten</span><span class="sxs-lookup"><span data-stu-id="418c1-103">Set up an item arrival overview profile</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="418c1-104">Dieser Aufgabe konzentriert sich auf den Einstellungen eines Wareneingangsübersichtprofils.</span><span class="sxs-lookup"><span data-stu-id="418c1-104">This task focuses on the setup of an arrival overview profile.</span></span> <span data-ttu-id="418c1-105">Das Wareneingangsübersichtprofil ist eine Regelsammlung, die angewendet werden, wenn die Wareneingangsübersichtseite von einem Benutzer geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="418c1-105">The arrival overview profile is a collection of rules that will be applied when the Arrival overview page is opened by a user.</span></span> <span data-ttu-id="418c1-106">Sie können diese Prozedur im Demodatunternehmen USMF verwenden.</span><span class="sxs-lookup"><span data-stu-id="418c1-106">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="418c1-107">Diese Prozedur wird normalerweise von einem Sachbearbeiter Zugänge ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="418c1-107">This procedure would typically be carried out by a receiving clerk.</span></span>





1. <span data-ttu-id="418c1-108">Wechseln Sie zu Lagerverwaltung > Einrichtung > Verteilung > Wareneingangsübersichtprofile.</span><span class="sxs-lookup"><span data-stu-id="418c1-108">Go to Inventory management > Setup > Distribution > Arrival overview profiles.</span></span>
2. <span data-ttu-id="418c1-109">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="418c1-109">Click New.</span></span>
    * <span data-ttu-id="418c1-110">Da Sie fast immer im gleichen Lagerort zusammenarbeiten, der vollständige LKW-Auslastungen auslädt, sollten Sie ein Wareneingangsübersichtprofil erstellen, um den Vorgang des zum Erfassen der empfangenen Artikeln zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="418c1-110">Because you will almost always work in the same warehouse offloading full truck loads, you should create an arrival overview profile to simplify the process of registering received items.</span></span>  
3. <span data-ttu-id="418c1-111">Geben Sie im Feld Ankunftsübersichts-Profilname einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="418c1-111">In the Arrival overview profile name field, type a value.</span></span>
4. <span data-ttu-id="418c1-112">Wählen Sie im Feld 'Zeilen anzeigen' eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="418c1-112">In the Show lines field, select an option.</span></span>
    * <span data-ttu-id="418c1-113">Wählen Sie aus, welche Positionen für die Zugänge angezeigt werden sollen: Alle - Alle Positionen anzeigenm, unabhängig vom Status.</span><span class="sxs-lookup"><span data-stu-id="418c1-113">Select which lines to show for the receipts:   All – Show all lines, regardless of status.</span></span>   <span data-ttu-id="418c1-114">In Bearbeitung – Zeigen Sie Positionen für Zugänge an, deren Bearbeitung den Status Komplett oder Teilweise aufweist.</span><span class="sxs-lookup"><span data-stu-id="418c1-114">In progress – Show lines for receipts in which the progress is Complete or Partly.</span></span> <span data-ttu-id="418c1-115">Dies bedeutet, dass die Menge für jede Position vollständig oder teilweise in einer Wareneingangserfassung erfasst wurde.</span><span class="sxs-lookup"><span data-stu-id="418c1-115">This means that for each line, either the full quantity or part of the quantity has been registered in an arrival journal.</span></span>   <span data-ttu-id="418c1-116">Nicht vollständig – Zeigen Sie Positionen für Zugänge an, deren Bearbeitung den Status Keiner oder Teilweise aufweist.</span><span class="sxs-lookup"><span data-stu-id="418c1-116">Not complete – Show lines for receipts in which the progress is None or Partly.</span></span> <span data-ttu-id="418c1-117">Dies bedeutet, dass für jede Position keine oder nur ein Teil der Menge in einer Wareneingangserfassung erfasst wurde.</span><span class="sxs-lookup"><span data-stu-id="418c1-117">This means that for each line, nothing or only part of the quantity has been registered in an arrival journal.</span></span>  
5. <span data-ttu-id="418c1-118">Erweitern oder reduzieren Sie den Abschnitt "Wareneingangsoptionen".</span><span class="sxs-lookup"><span data-stu-id="418c1-118">Expand or collapse the Arrival options section.</span></span>
6. <span data-ttu-id="418c1-119">Geben Sie im Feld Tage im Voraus einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="418c1-119">In the Days forward field, type a value.</span></span>
    * <span data-ttu-id="418c1-120">Damit werden die einen Filter festgelegt, um die Zugangspositionen anzeigen, die erwartet werden, innerhalb der nächsten Tage Zustellung des (abhängig von der Anzahl Sie festgelegt wurde).</span><span class="sxs-lookup"><span data-stu-id="418c1-120">This sets a filter to show the receipt lines expected to be received within the next few days (depending on the number you set).</span></span>  
7. <span data-ttu-id="418c1-121">Geben Sie im Feld Tage zurück einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="418c1-121">In the Days back field, type a value.</span></span>
    * <span data-ttu-id="418c1-122">Damit werden die einen Filter festgelegt, um die Zugangspositionen anzeigen, die erwartet werden, mehrere Tage aktuellen Monat empfangen zu werden.</span><span class="sxs-lookup"><span data-stu-id="418c1-122">This sets a filter to show the receipt lines expected to be received a number of days before today.</span></span>  
8. <span data-ttu-id="418c1-123">Geben Sie im Feld Lagerorte einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="418c1-123">In the Warehouses field, type a value.</span></span>
    * <span data-ttu-id="418c1-124">Filtern Sie nach einen oder mehrere Lagerorte.</span><span class="sxs-lookup"><span data-stu-id="418c1-124">Filter on one or more warehouses.</span></span>  
9. <span data-ttu-id="418c1-125">Wählen Sie im Feld "Lieferart" einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="418c1-125">In the Mode of delivery field, select a value.</span></span>
    * <span data-ttu-id="418c1-126">Damit wird einen Filter festgelegt, um nur die Zugangspositionen mit diesem Lieferart anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="418c1-126">This sets a filter to show only the receipt lines with this Mode of delivery.</span></span>  
10. <span data-ttu-id="418c1-127">Wählen Sie im Feld "Name" die Option "WHS" aus.</span><span class="sxs-lookup"><span data-stu-id="418c1-127">In the Name field, select WHS.</span></span>
11. <span data-ttu-id="418c1-128">Wählen Sie im Feld "Lagerort" den Lagerort 24 aus.</span><span class="sxs-lookup"><span data-stu-id="418c1-128">In the Warehouse field, select warehouse 24.</span></span>
    * <span data-ttu-id="418c1-129">Dies ist der Standardlagerort, der für registrierte Zugangspositionen verwendet wird, die dieses Profil verwenden.</span><span class="sxs-lookup"><span data-stu-id="418c1-129">This is the default warehouse that will be used for registered receipt lines that use this profile.</span></span>  
12. <span data-ttu-id="418c1-130">Wählen Sie im Feld "Lagerplatz" die Option "Ladebereichstor" aus.</span><span class="sxs-lookup"><span data-stu-id="418c1-130">In the Location field, select Baydoor.</span></span>
    * <span data-ttu-id="418c1-131">Dies ist der Standardlagerort, der für registrierte Zugangspositionen verwendet wird, die dieses Profil verwenden.</span><span class="sxs-lookup"><span data-stu-id="418c1-131">This is the default location that will be used for registered receipt lines that use this profile.</span></span>  
13. <span data-ttu-id="418c1-132">Erweitern oder reduzieren Sie den Abschnitt "Wareneingangs-Abfragedetails".</span><span class="sxs-lookup"><span data-stu-id="418c1-132">Expand or collapse the Arrival query details section.</span></span>
14. <span data-ttu-id="418c1-133">Wählen Sie im Feld "Auf Standort beschränken" den Standort 2 aus.</span><span class="sxs-lookup"><span data-stu-id="418c1-133">In the Restrict to site field, select site 2.</span></span>
    * <span data-ttu-id="418c1-134">Damit wird einen Filter festgelegt, um nur die Zugangspositionen an diesem Lagerort anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="418c1-134">This sets a filter to show only the receipt lines with this site.</span></span>  
15. <span data-ttu-id="418c1-135">Legen Sie die Option "Bestellungen" auf "Ja" fest.</span><span class="sxs-lookup"><span data-stu-id="418c1-135">Set the Purchase orders option to Yes.</span></span>
    * <span data-ttu-id="418c1-136">Wählen Sie Positionen aus offenen Bestellungen aus.</span><span class="sxs-lookup"><span data-stu-id="418c1-136">Select receipt lines from purchase orders.</span></span>  
16. <span data-ttu-id="418c1-137">Legen Sie die Option "Umlagerungsaufträge" auf "Ja" fest.</span><span class="sxs-lookup"><span data-stu-id="418c1-137">Set the Transfer orders option to Yes.</span></span>
    * <span data-ttu-id="418c1-138">Wählen Sie Positionen aus offenen Umlagerungsaufträgen aus.</span><span class="sxs-lookup"><span data-stu-id="418c1-138">Select receipt lines from transfer orders.</span></span>  
17. <span data-ttu-id="418c1-139">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="418c1-139">Click Save.</span></span>
18. <span data-ttu-id="418c1-140">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="418c1-140">Close the page.</span></span>


