---
title: Erstellen von Schichtmodellen
description: Schichtmodelle definieren die Arbeitsstunden in einer Woche und werden verwendet, um die Arbeitszeiten für einen bestimmten Zeitraum zu generieren.
author: sorenva
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkTimeTable, WorkTimeCopyDayDialog, WorkPeriodTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b5bd1b384fe66dd7d59b776bdf1154cc5b8262ce
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428410"
---
# <a name="create-working-time-templates"></a><span data-ttu-id="7399e-103">Erstellen von Schichtmodellen</span><span class="sxs-lookup"><span data-stu-id="7399e-103">Create working time templates</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7399e-104">Schichtmodelle definieren die Arbeitsstunden in einer Woche und werden verwendet, um die Arbeitszeiten für einen bestimmten Zeitraum zu generieren.</span><span class="sxs-lookup"><span data-stu-id="7399e-104">Working time templates define the working hours throughout a week and are used to generate working times for a period of time.</span></span> <span data-ttu-id="7399e-105">Dieses Verfahren zeigt Ihnen, wie ein Schichtmodell mithilfe der Arbeitszeit-Planungseigenschaften für die Kategorisierung von Arbeitszeitintervallen definiert wird.</span><span class="sxs-lookup"><span data-stu-id="7399e-105">This procedure shows you how to define a working time template using working time scheduling properties for categorizing working time intervals.</span></span> <span data-ttu-id="7399e-106">Sie können diese Prozedur Schritt für Schritt im Demodatenunternehmen USMF durchführen oder können Ihre eigenen Daten verwenden.</span><span class="sxs-lookup"><span data-stu-id="7399e-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="7399e-107">Wechseln Sie zu "Alle Arbeitsbereiche" > "Ressourcenlebenszyklusverwaltung".</span><span class="sxs-lookup"><span data-stu-id="7399e-107">Go to All workspaces > Resource lifecycle management.</span></span>
2. <span data-ttu-id="7399e-108">Klicken Sie auf "Schichtmodelle".</span><span class="sxs-lookup"><span data-stu-id="7399e-108">Click Working time templates.</span></span>

## <a name="create-working-time-template"></a><span data-ttu-id="7399e-109">Erstellen von Schichtmodellen</span><span class="sxs-lookup"><span data-stu-id="7399e-109">Create working time template</span></span>
1. <span data-ttu-id="7399e-110">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="7399e-110">Click New.</span></span>
2. <span data-ttu-id="7399e-111">Geben Sie im Feld "Schichtmodell" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="7399e-111">In the Working time template field, type a value.</span></span>
3. <span data-ttu-id="7399e-112">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="7399e-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="7399e-113">Erweitern Sie den Abschnitt "Montag".</span><span class="sxs-lookup"><span data-stu-id="7399e-113">Expand the Monday section.</span></span>
5. <span data-ttu-id="7399e-114">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="7399e-114">Click Add.</span></span>
6. <span data-ttu-id="7399e-115">Geben Sie im Feld "Von" eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="7399e-115">In the From field, enter a time.</span></span>
    * <span data-ttu-id="7399e-116">Geben Sie die Uhrzeit an, zu der die Arbeit am Morgen beginnt.</span><span class="sxs-lookup"><span data-stu-id="7399e-116">Specify the time when work begins in the morning.</span></span>  
7. <span data-ttu-id="7399e-117">Geben Sie im Feld "Bis" eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="7399e-117">In the To field, enter a time.</span></span>
    * <span data-ttu-id="7399e-118">Geben Sie die Uhrzeit an, zu der Arbeitskräfte zum Mittagessen gehen.</span><span class="sxs-lookup"><span data-stu-id="7399e-118">Specify the time when workers break for lunch.</span></span>  
8. <span data-ttu-id="7399e-119">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="7399e-119">Click Add.</span></span>
9. <span data-ttu-id="7399e-120">Geben Sie im Feld "Von" eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="7399e-120">In the From field, enter a time.</span></span>
    * <span data-ttu-id="7399e-121">Geben Sie die Uhrzeit an, zu der die Arbeitskräfte vom Mittagessen kommen.</span><span class="sxs-lookup"><span data-stu-id="7399e-121">Specify the time when work resumes after lunch.</span></span>  
10. <span data-ttu-id="7399e-122">Geben Sie im Feld "Bis" eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="7399e-122">In the To field, enter a time.</span></span>
    * <span data-ttu-id="7399e-123">Geben Sie das Ende des Arbeitstages an.</span><span class="sxs-lookup"><span data-stu-id="7399e-123">Specify the end of the work day.</span></span>  

## <a name="replicate-working-times-to-all-week-days"></a><span data-ttu-id="7399e-124">Replikation von Arbeitszeiten auf alle Wochentage</span><span class="sxs-lookup"><span data-stu-id="7399e-124">Replicate working times to all week days</span></span>
1. <span data-ttu-id="7399e-125">Klicken Sie auf "Tag kopieren".</span><span class="sxs-lookup"><span data-stu-id="7399e-125">Click Copy day.</span></span>
    * <span data-ttu-id="7399e-126">Kopieren Sie die Arbeitszeitdefinitionen von Montag zu Dienstag.</span><span class="sxs-lookup"><span data-stu-id="7399e-126">Copy the working times definitions from Monday to Tuesday.</span></span>  
2. <span data-ttu-id="7399e-127">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="7399e-127">Click OK.</span></span>
3. <span data-ttu-id="7399e-128">Klicken Sie auf "Tag kopieren".</span><span class="sxs-lookup"><span data-stu-id="7399e-128">Click Copy day.</span></span>
    * <span data-ttu-id="7399e-129">Kopieren Sie die Arbeitszeitdefinitionen von Montag zu Mittwoch.</span><span class="sxs-lookup"><span data-stu-id="7399e-129">Copy the working times definitions from Monday to Wednesday.</span></span>  
4. <span data-ttu-id="7399e-130">Wählen Sie im Feld "Bis Wochentag" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="7399e-130">In the To weekday field, select an option.</span></span>
5. <span data-ttu-id="7399e-131">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="7399e-131">Click OK.</span></span>
6. <span data-ttu-id="7399e-132">Klicken Sie auf "Tag kopieren".</span><span class="sxs-lookup"><span data-stu-id="7399e-132">Click Copy day.</span></span>
    * <span data-ttu-id="7399e-133">Kopieren Sie die Arbeitszeitdefinitionen von Montag zu Donnerstag.</span><span class="sxs-lookup"><span data-stu-id="7399e-133">Copy the working times definitions from Monday to Thursday.</span></span>  
7. <span data-ttu-id="7399e-134">Wählen Sie im Feld "Bis Wochentag" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="7399e-134">In the To weekday field, select an option.</span></span>
8. <span data-ttu-id="7399e-135">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="7399e-135">Click OK.</span></span>
9. <span data-ttu-id="7399e-136">Klicken Sie auf "Tag kopieren".</span><span class="sxs-lookup"><span data-stu-id="7399e-136">Click Copy day.</span></span>
    * <span data-ttu-id="7399e-137">Kopieren Sie die Arbeitszeitdefinitionen von Montag zu Freitag.</span><span class="sxs-lookup"><span data-stu-id="7399e-137">Copy the working times definitions from Monday to Friday.</span></span>  
10. <span data-ttu-id="7399e-138">Wählen Sie im Feld "Bis Wochentag" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="7399e-138">In the To weekday field, select an option.</span></span>
11. <span data-ttu-id="7399e-139">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="7399e-139">Click OK.</span></span>

## <a name="define-time-slots-for-special-operations"></a><span data-ttu-id="7399e-140">Definieren von Zeitrahmen für spezielle Vorgänge</span><span class="sxs-lookup"><span data-stu-id="7399e-140">Define time slots for special operations</span></span>
1. <span data-ttu-id="7399e-141">Erweitern Sie den Abschnitt "Freitag".</span><span class="sxs-lookup"><span data-stu-id="7399e-141">Expand the Friday section.</span></span>
2. <span data-ttu-id="7399e-142">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="7399e-142">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="7399e-143">Geben Sie im Feld "Eigenschaft" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="7399e-143">In the Property field, enter or select a value.</span></span>
4. <span data-ttu-id="7399e-144">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="7399e-144">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="7399e-145">Geben Sie im Feld "Eigenschaft" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="7399e-145">In the Property field, enter or select a value.</span></span>

## <a name="mark-weekend-days-as-closed-for-pickup"></a><span data-ttu-id="7399e-146">Markieren von Wochenendentagen als "Keine Abholung"</span><span class="sxs-lookup"><span data-stu-id="7399e-146">Mark weekend days as closed for pickup</span></span>
1. <span data-ttu-id="7399e-147">Erweitern Sie den Abschnitt "Samstag".</span><span class="sxs-lookup"><span data-stu-id="7399e-147">Expand the Saturday section.</span></span>
2. <span data-ttu-id="7399e-148">Wählen Sie "Ja" im Feld "Keine Abholung" aus.</span><span class="sxs-lookup"><span data-stu-id="7399e-148">Select Yes in the Closed for pickup field.</span></span>
3. <span data-ttu-id="7399e-149">Erweitern Sie den Abschnitt "Sonntag".</span><span class="sxs-lookup"><span data-stu-id="7399e-149">Expand the Sunday section.</span></span>
4. <span data-ttu-id="7399e-150">Wählen Sie "Ja" im Feld "Keine Abholung" aus.</span><span class="sxs-lookup"><span data-stu-id="7399e-150">Select Yes in the Closed for pickup field.</span></span>

