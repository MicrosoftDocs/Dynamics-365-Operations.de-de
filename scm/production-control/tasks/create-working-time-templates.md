--- 
title: Erstellen von Schichtmodellen
description: "Schichtmodelle definieren die Arbeitsstunden in einer Woche und werden verwendet, um die Arbeitszeiten für einen bestimmten Zeitraum zu generieren."
author: sorenva
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 2df37747601618fc3d45734152a05aedd39500a6
ms.contentlocale: de-de
ms.lasthandoff: 08/29/2017

---
# <a name="create-working-time-templates"></a><span data-ttu-id="b9ee3-103">Erstellen von Schichtmodellen</span><span class="sxs-lookup"><span data-stu-id="b9ee3-103">Create working time templates</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b9ee3-104">Schichtmodelle definieren die Arbeitsstunden in einer Woche und werden verwendet, um die Arbeitszeiten für einen bestimmten Zeitraum zu generieren.</span><span class="sxs-lookup"><span data-stu-id="b9ee3-104">Working time templates define the working hours throughout a week and are used to generate working times for a period of time.</span></span> <span data-ttu-id="b9ee3-105">Dieses Verfahren zeigt Ihnen, wie ein Schichtmodell mithilfe der Arbeitszeit-Planungseigenschaften für die Kategorisierung von Arbeitszeitintervallen definiert wird.</span><span class="sxs-lookup"><span data-stu-id="b9ee3-105">This procedure shows you how to define a working time template using working time scheduling properties for categorizing working time intervals.</span></span> <span data-ttu-id="b9ee3-106">Sie können diese Prozedur Schritt für Schritt im Demodatenunternehmen USMF durchführen oder können Ihre eigenen Daten verwenden.</span><span class="sxs-lookup"><span data-stu-id="b9ee3-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="b9ee3-107">Wechseln Sie zu "Alle Arbeitsbereiche" > "Ressourcenlebenszyklusverwaltung".</span><span class="sxs-lookup"><span data-stu-id="b9ee3-107">Go to All workspaces > Resource lifecycle management.</span></span>
2. <span data-ttu-id="b9ee3-108">Klicken Sie auf "Schichtmodelle".</span><span class="sxs-lookup"><span data-stu-id="b9ee3-108">Click Working time templates.</span></span>

## <a name="create-working-time-template"></a><span data-ttu-id="b9ee3-109">Erstellen von Schichtmodellen</span><span class="sxs-lookup"><span data-stu-id="b9ee3-109">Create working time template</span></span>
1. <span data-ttu-id="b9ee3-110">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="b9ee3-110">Click New.</span></span>
2. <span data-ttu-id="b9ee3-111">Geben Sie im Feld "Schichtmodell" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="b9ee3-111">In the Working time template field, type a value.</span></span>
3. <span data-ttu-id="b9ee3-112">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="b9ee3-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="b9ee3-113">Erweitern Sie den Abschnitt "Montag".</span><span class="sxs-lookup"><span data-stu-id="b9ee3-113">Expand the Monday section.</span></span>
5. <span data-ttu-id="b9ee3-114">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b9ee3-114">Click Add.</span></span>
6. <span data-ttu-id="b9ee3-115">Geben Sie im Feld "Von" eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="b9ee3-115">In the From field, enter a time.</span></span>
    * <span data-ttu-id="b9ee3-116">Geben Sie die Uhrzeit an, zu der die Arbeit am Morgen beginnt.</span><span class="sxs-lookup"><span data-stu-id="b9ee3-116">Specify the time when work begins in the morning.</span></span>  
7. <span data-ttu-id="b9ee3-117">Geben Sie im Feld "Bis" eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="b9ee3-117">In the To field, enter a time.</span></span>
    * <span data-ttu-id="b9ee3-118">Geben Sie die Uhrzeit an, zu der Arbeitskräfte zum Mittagessen gehen.</span><span class="sxs-lookup"><span data-stu-id="b9ee3-118">Specify the time when workers break for lunch.</span></span>  
8. <span data-ttu-id="b9ee3-119">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b9ee3-119">Click Add.</span></span>
9. <span data-ttu-id="b9ee3-120">Geben Sie im Feld "Von" eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="b9ee3-120">In the From field, enter a time.</span></span>
    * <span data-ttu-id="b9ee3-121">Geben Sie die Uhrzeit an, zu der die Arbeitskräfte vom Mittagessen kommen.</span><span class="sxs-lookup"><span data-stu-id="b9ee3-121">Specify the time when work resumes after lunch.</span></span>  
10. <span data-ttu-id="b9ee3-122">Geben Sie im Feld "Bis" eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="b9ee3-122">In the To field, enter a time.</span></span>
    * <span data-ttu-id="b9ee3-123">Geben Sie das Ende des Arbeitstages an.</span><span class="sxs-lookup"><span data-stu-id="b9ee3-123">Specify the end of the work day.</span></span>  

## <a name="replicate-working-times-to-all-week-days"></a><span data-ttu-id="b9ee3-124">Replikation von Arbeitszeiten auf alle Wochentage</span><span class="sxs-lookup"><span data-stu-id="b9ee3-124">Replicate working times to all week days</span></span>
1. <span data-ttu-id="b9ee3-125">Klicken Sie auf "Tag kopieren".</span><span class="sxs-lookup"><span data-stu-id="b9ee3-125">Click Copy day.</span></span>
    * <span data-ttu-id="b9ee3-126">Kopieren Sie die Arbeitszeitdefinitionen von Montag zu Dienstag.</span><span class="sxs-lookup"><span data-stu-id="b9ee3-126">Copy the working times definitions from Monday to Tuesday.</span></span>  
2. <span data-ttu-id="b9ee3-127">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="b9ee3-127">Click OK.</span></span>
3. <span data-ttu-id="b9ee3-128">Klicken Sie auf "Tag kopieren".</span><span class="sxs-lookup"><span data-stu-id="b9ee3-128">Click Copy day.</span></span>
    * <span data-ttu-id="b9ee3-129">Kopieren Sie die Arbeitszeitdefinitionen von Montag zu Mittwoch.</span><span class="sxs-lookup"><span data-stu-id="b9ee3-129">Copy the working times definitions from Monday to Wednesday.</span></span>  
4. <span data-ttu-id="b9ee3-130">Wählen Sie im Feld "Bis Wochentag" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="b9ee3-130">In the To weekday field, select an option.</span></span>
5. <span data-ttu-id="b9ee3-131">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="b9ee3-131">Click OK.</span></span>
6. <span data-ttu-id="b9ee3-132">Klicken Sie auf "Tag kopieren".</span><span class="sxs-lookup"><span data-stu-id="b9ee3-132">Click Copy day.</span></span>
    * <span data-ttu-id="b9ee3-133">Kopieren Sie die Arbeitszeitdefinitionen von Montag zu Donnerstag.</span><span class="sxs-lookup"><span data-stu-id="b9ee3-133">Copy the working times definitions from Monday to Thursday.</span></span>  
7. <span data-ttu-id="b9ee3-134">Wählen Sie im Feld "Bis Wochentag" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="b9ee3-134">In the To weekday field, select an option.</span></span>
8. <span data-ttu-id="b9ee3-135">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="b9ee3-135">Click OK.</span></span>
9. <span data-ttu-id="b9ee3-136">Klicken Sie auf "Tag kopieren".</span><span class="sxs-lookup"><span data-stu-id="b9ee3-136">Click Copy day.</span></span>
    * <span data-ttu-id="b9ee3-137">Kopieren Sie die Arbeitszeitdefinitionen von Montag zu Freitag.</span><span class="sxs-lookup"><span data-stu-id="b9ee3-137">Copy the working times definitions from Monday to Friday.</span></span>  
10. <span data-ttu-id="b9ee3-138">Wählen Sie im Feld "Bis Wochentag" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="b9ee3-138">In the To weekday field, select an option.</span></span>
11. <span data-ttu-id="b9ee3-139">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="b9ee3-139">Click OK.</span></span>

## <a name="define-time-slots-for-special-operations"></a><span data-ttu-id="b9ee3-140">Definieren von Zeitrahmen für spezielle Vorgänge</span><span class="sxs-lookup"><span data-stu-id="b9ee3-140">Define time slots for special operations</span></span>
1. <span data-ttu-id="b9ee3-141">Erweitern Sie den Abschnitt "Freitag".</span><span class="sxs-lookup"><span data-stu-id="b9ee3-141">Expand the Friday section.</span></span>
2. <span data-ttu-id="b9ee3-142">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="b9ee3-142">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="b9ee3-143">Geben Sie im Feld "Eigenschaft" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="b9ee3-143">In the Property field, enter or select a value.</span></span>
4. <span data-ttu-id="b9ee3-144">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="b9ee3-144">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="b9ee3-145">Geben Sie im Feld "Eigenschaft" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="b9ee3-145">In the Property field, enter or select a value.</span></span>

## <a name="mark-weekend-days-as-closed-for-pickup"></a><span data-ttu-id="b9ee3-146">Markieren von Wochenendentagen als "Keine Abholung"</span><span class="sxs-lookup"><span data-stu-id="b9ee3-146">Mark weekend days as closed for pickup</span></span>
1. <span data-ttu-id="b9ee3-147">Erweitern Sie den Abschnitt "Samstag".</span><span class="sxs-lookup"><span data-stu-id="b9ee3-147">Expand the Saturday section.</span></span>
2. <span data-ttu-id="b9ee3-148">Wählen Sie "Ja" im Feld "Keine Abholung" aus.</span><span class="sxs-lookup"><span data-stu-id="b9ee3-148">Select Yes in the Closed for pickup field.</span></span>
3. <span data-ttu-id="b9ee3-149">Erweitern Sie den Abschnitt "Sonntag".</span><span class="sxs-lookup"><span data-stu-id="b9ee3-149">Expand the Sunday section.</span></span>
4. <span data-ttu-id="b9ee3-150">Wählen Sie "Ja" im Feld "Keine Abholung" aus.</span><span class="sxs-lookup"><span data-stu-id="b9ee3-150">Select Yes in the Closed for pickup field.</span></span>


