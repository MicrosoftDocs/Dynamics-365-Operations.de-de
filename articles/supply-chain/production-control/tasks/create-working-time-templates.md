---
title: Erstellen von Schichtmodellen
description: Schichtmodelle definieren die Arbeitsstunden in einer Woche und werden verwendet, um die Arbeitszeiten für einen bestimmten Zeitraum zu generieren.
author: sorenva
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkTimeTable, WorkTimeCopyDayDialog, WorkPeriodTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ed1981b7c1427c902f237f0aa95f63e89bc345ab
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920928"
---
# <a name="create-working-time-templates"></a><span data-ttu-id="020b3-103">Erstellen von Schichtmodellen</span><span class="sxs-lookup"><span data-stu-id="020b3-103">Create working time templates</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="020b3-104">Schichtmodelle definieren die Arbeitsstunden in einer Woche und werden verwendet, um die Arbeitszeiten für einen bestimmten Zeitraum zu generieren.</span><span class="sxs-lookup"><span data-stu-id="020b3-104">Working time templates define the working hours throughout a week and are used to generate working times for a period of time.</span></span> <span data-ttu-id="020b3-105">Dieses Verfahren zeigt Ihnen, wie ein Schichtmodell mithilfe der Arbeitszeit-Planungseigenschaften für die Kategorisierung von Arbeitszeitintervallen definiert wird.</span><span class="sxs-lookup"><span data-stu-id="020b3-105">This procedure shows you how to define a working time template using working time scheduling properties for categorizing working time intervals.</span></span> <span data-ttu-id="020b3-106">Sie können diese Prozedur Schritt für Schritt im Demodatenunternehmen USMF durchführen oder können Ihre eigenen Daten verwenden.</span><span class="sxs-lookup"><span data-stu-id="020b3-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="020b3-107">Wechseln Sie zu **Arbeitsbereiche > Ressourcenlebenszyklusverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="020b3-107">Go to **Workspaces > Resource lifecycle management**.</span></span>
1. <span data-ttu-id="020b3-108">Wählen Sie **Arbeitszeitvorlagen**.</span><span class="sxs-lookup"><span data-stu-id="020b3-108">Select **Working time templates**.</span></span>

## <a name="create-working-time-template"></a><span data-ttu-id="020b3-109">Erstellen von Schichtmodellen</span><span class="sxs-lookup"><span data-stu-id="020b3-109">Create working time template</span></span>

1. <span data-ttu-id="020b3-110">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="020b3-110">Select **New**.</span></span>
1. <span data-ttu-id="020b3-111">Geben Sie im Feld **Arbeitszeitvorlage** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="020b3-111">In the **Working time template** field, type a value.</span></span>
1. <span data-ttu-id="020b3-112">Geben Sie im Feld **Name** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="020b3-112">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="020b3-113">Erweitern Sie den Abschnitt **Montag**.</span><span class="sxs-lookup"><span data-stu-id="020b3-113">Expand the **Monday** section.</span></span>
1. <span data-ttu-id="020b3-114">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="020b3-114">Select **Add**.</span></span>
1. <span data-ttu-id="020b3-115">Geben Sie im Feld **Von** eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="020b3-115">In the **From** field, enter a time.</span></span>
    * <span data-ttu-id="020b3-116">Geben Sie die Uhrzeit an, zu der die Arbeit am Morgen beginnt.</span><span class="sxs-lookup"><span data-stu-id="020b3-116">Specify the time when work begins in the morning.</span></span>  
1. <span data-ttu-id="020b3-117">Geben Sie im Feld **Bis** eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="020b3-117">In the **To** field, enter a time.</span></span>
    * <span data-ttu-id="020b3-118">Geben Sie die Uhrzeit an, zu der Arbeitskräfte zum Mittagessen gehen.</span><span class="sxs-lookup"><span data-stu-id="020b3-118">Specify the time when workers break for lunch.</span></span>  
1. <span data-ttu-id="020b3-119">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="020b3-119">Select **Add**.</span></span>
1. <span data-ttu-id="020b3-120">Geben Sie im Feld **Von** eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="020b3-120">In the **From** field, enter a time.</span></span>
    * <span data-ttu-id="020b3-121">Geben Sie die Uhrzeit an, zu der die Arbeitskräfte vom Mittagessen kommen.</span><span class="sxs-lookup"><span data-stu-id="020b3-121">Specify the time when work resumes after lunch.</span></span>  
1. <span data-ttu-id="020b3-122">Geben Sie im Feld **Bis** eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="020b3-122">In the **To** field, enter a time.</span></span>
    * <span data-ttu-id="020b3-123">Geben Sie das Ende des Arbeitstages an.</span><span class="sxs-lookup"><span data-stu-id="020b3-123">Specify the end of the work day.</span></span>  

## <a name="replicate-working-times-to-all-week-days"></a><span data-ttu-id="020b3-124">Replikation von Arbeitszeiten auf alle Wochentage</span><span class="sxs-lookup"><span data-stu-id="020b3-124">Replicate working times to all week days</span></span>

1. <span data-ttu-id="020b3-125">Wählen Sie **Kopieren Tag**.</span><span class="sxs-lookup"><span data-stu-id="020b3-125">Select **Copy day**.</span></span>
    * <span data-ttu-id="020b3-126">Kopieren Sie die Arbeitszeitdefinitionen von Montag zu Dienstag.</span><span class="sxs-lookup"><span data-stu-id="020b3-126">Copy the working times definitions from Monday to Tuesday.</span></span>  
1. <span data-ttu-id="020b3-127">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="020b3-127">Select **OK**.</span></span>
1. <span data-ttu-id="020b3-128">Wählen Sie **Kopieren Tag**.</span><span class="sxs-lookup"><span data-stu-id="020b3-128">Select **Copy day**.</span></span>
    * <span data-ttu-id="020b3-129">Kopieren Sie die Arbeitszeitdefinitionen von Montag zu Mittwoch.</span><span class="sxs-lookup"><span data-stu-id="020b3-129">Copy the working times definitions from Monday to Wednesday.</span></span>  
1. <span data-ttu-id="020b3-130">Wählen Sie im Feld **Bis Wochentag** eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="020b3-130">In the **To weekday** field, select an option.</span></span>
1. <span data-ttu-id="020b3-131">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="020b3-131">Select **OK**.</span></span>
1. <span data-ttu-id="020b3-132">Wählen Sie **Kopieren Tag**.</span><span class="sxs-lookup"><span data-stu-id="020b3-132">Select **Copy day**.</span></span>
    * <span data-ttu-id="020b3-133">Kopieren Sie die Arbeitszeitdefinitionen von Montag zu Donnerstag.</span><span class="sxs-lookup"><span data-stu-id="020b3-133">Copy the working times definitions from Monday to Thursday.</span></span>  
1. <span data-ttu-id="020b3-134">Wählen Sie im Feld **Bis Wochentag** eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="020b3-134">In the **To weekday** field, select an option.</span></span>
1. <span data-ttu-id="020b3-135">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="020b3-135">Select **OK**.</span></span>
1. <span data-ttu-id="020b3-136">Wählen Sie **Kopieren Tag**.</span><span class="sxs-lookup"><span data-stu-id="020b3-136">Select **Copy day**.</span></span>
    * <span data-ttu-id="020b3-137">Kopieren Sie die Arbeitszeitdefinitionen von Montag zu Freitag.</span><span class="sxs-lookup"><span data-stu-id="020b3-137">Copy the working times definitions from Monday to Friday.</span></span>  
1. <span data-ttu-id="020b3-138">Wählen Sie im Feld **Bis Wochentag** eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="020b3-138">In the **To weekday** field, select an option.</span></span>
1. <span data-ttu-id="020b3-139">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="020b3-139">Select **OK**.</span></span>

## <a name="define-time-slots-for-special-operations"></a><span data-ttu-id="020b3-140">Definieren von Zeitrahmen für spezielle Vorgänge</span><span class="sxs-lookup"><span data-stu-id="020b3-140">Define time slots for special operations</span></span>

1. <span data-ttu-id="020b3-141">Erweitern Sie den Abschnitt **Freitag**.</span><span class="sxs-lookup"><span data-stu-id="020b3-141">Expand the **Friday** section.</span></span>
1. <span data-ttu-id="020b3-142">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="020b3-142">In the list, find and select the desired record.</span></span>
1. <span data-ttu-id="020b3-143">Geben Sie in das Feld **Eigenschaft** einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="020b3-143">In the **Property** field, enter or select a value.</span></span>
1. <span data-ttu-id="020b3-144">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="020b3-144">In the list, find and select the desired record.</span></span>
1. <span data-ttu-id="020b3-145">Geben Sie in das Feld **Eigenschaft** einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="020b3-145">In the **Property** field, enter or select a value.</span></span>

## <a name="mark-weekend-days-as-closed-for-pickup"></a><span data-ttu-id="020b3-146">Markieren von Wochenendentagen als "Keine Abholung"</span><span class="sxs-lookup"><span data-stu-id="020b3-146">Mark weekend days as closed for pickup</span></span>

1. <span data-ttu-id="020b3-147">Erweitern Sie den Abschnitt **Samstag**.</span><span class="sxs-lookup"><span data-stu-id="020b3-147">Expand the **Saturday** section.</span></span>
1. <span data-ttu-id="020b3-148">Wählen Sie *Ja* im Feld **Zur Abholung geschlossen**.</span><span class="sxs-lookup"><span data-stu-id="020b3-148">Select *Yes* in the **Closed for pickup** field.</span></span>
1. <span data-ttu-id="020b3-149">Erweitern Sie den Abschnitt **Sonntag**.</span><span class="sxs-lookup"><span data-stu-id="020b3-149">Expand the **Sunday** section.</span></span>
1. <span data-ttu-id="020b3-150">Wählen Sie *Ja* im Feld **Zur Abholung geschlossen**.</span><span class="sxs-lookup"><span data-stu-id="020b3-150">Select *Yes* in the **Closed for pickup** field.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]