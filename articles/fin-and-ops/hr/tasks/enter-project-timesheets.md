---
title: Arbeitsnachweise des Projekts eingeben
description: In dieser Prozedur erstellen Sie einen Arbeitszeitnachweis, indem Sie ein leeres Arbeitszeitnachweisformular verwenden.
author: andreabichsel
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.search.industry: Service industries
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3f1be02f0080ee23359ad905b1e997d8cd5adfd2
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1510381"
---
# <a name="enter-project-timesheets"></a><span data-ttu-id="43490-103">Arbeitsnachweise des Projekts eingeben</span><span class="sxs-lookup"><span data-stu-id="43490-103">Enter project timesheets</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="43490-104">In dieser Prozedur erstellen Sie einen Arbeitszeitnachweis, indem Sie ein leeres Arbeitszeitnachweisformular verwenden.</span><span class="sxs-lookup"><span data-stu-id="43490-104">This procedure lets you create a timesheet by using an empty timesheet form.</span></span> <span data-ttu-id="43490-105">Der neue Arbeitszeitnachweis kann auf Informationen aus einem vorherigen Arbeitszeitnachweis auf aus Projekt- und Aktivitätszuweisungen auf der Seite "Eigene Favoriten" basieren.</span><span class="sxs-lookup"><span data-stu-id="43490-105">The new timesheet can be based on information from a previous timesheet, or from project and activity assignments in the My favorites page.</span></span> <span data-ttu-id="43490-106">Standardmäßig werden auf der Listenseite "Alle Arbeitszeitnachweise" alle Arbeitszeitnachweise für die aktuelle Periode angezeigt.</span><span class="sxs-lookup"><span data-stu-id="43490-106">By default, the All timesheets list page displays all your timesheets for the current period.</span></span> <span data-ttu-id="43490-107">Sie können über die Dropdownliste für das Feld "Anzeigen" auf der Seite "Eigene Arbeitszeitnachweise" die Arbeitszeitnachweise nach Zeitraum oder Projekt filtern oder Arbeitszeitnachweise anzeigen, die im Auftrag anderer Arbeitskräfte erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="43490-107">You can use the drop-down list for the Show field in the My timesheets page to filter the timesheet list by time period or project, or to view timesheets that were created on behalf of other workers.</span></span> <span data-ttu-id="43490-108">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USSI.</span><span class="sxs-lookup"><span data-stu-id="43490-108">The demo data company used to create this procedure is USSI.</span></span> <span data-ttu-id="43490-109">Um diese Prozedur zu starten, wechseln Sie zu "Projektverwaltung und Buchhaltung" > "Arbeitszeitnachweis" > "Eigene Arbeitszeitnachweise".</span><span class="sxs-lookup"><span data-stu-id="43490-109">To begin this procedure, go to Project management and accounting > Timesheets >My timesheets</span></span>

1. <span data-ttu-id="43490-110">Um einen neuen Arbeitszeitnachweis einzugeben, klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="43490-110">To enter a new timesheet, click New.</span></span>
    * <span data-ttu-id="43490-111">Die Dropdownliste "Ressourcen" zeigt die Arbeitskraft an, die dem aktuellen Benutzer standardmäßig zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="43490-111">The Resource drop-down list shows the worker assigned to the current user, by default.</span></span>  
    * <span data-ttu-id="43490-112">Wenn der Benutzer als Stellvertreter ausgewählt wird, werden die Namen aufgeführt, damit ein Benutzer einen Arbeitszeitnachweis in dessen Namen eingeben kann.</span><span class="sxs-lookup"><span data-stu-id="43490-112">If the user is designated as a delegate, this will list the names so that a user can enter a timesheet on their behalf.</span></span>  
2. <span data-ttu-id="43490-113">Geben Sie ein Datum in das Feld "Datum" ein.</span><span class="sxs-lookup"><span data-stu-id="43490-113">In the Date field, enter a date.</span></span>
    * <span data-ttu-id="43490-114">Wenn diese Option ausgewählt ist, werden neue Arbeitszeitnachweispositionen über Arbeitszeitnachweiseinstellungen erstellt, die als Favoriten konfiguriert wurden.</span><span class="sxs-lookup"><span data-stu-id="43490-114">If this option is selected, new timesheet lines will be created by using the timesheet settings that were configured as favorites.</span></span>  
3. <span data-ttu-id="43490-115">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="43490-115">Click OK.</span></span>
4. <span data-ttu-id="43490-116">Klicken Sie auf "Neue Position".</span><span class="sxs-lookup"><span data-stu-id="43490-116">Click New line.</span></span>
5. <span data-ttu-id="43490-117">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="43490-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="43490-118">Das Feld "Juristische Person" enthält standardmäßige die aktuelle juristische Person.</span><span class="sxs-lookup"><span data-stu-id="43490-118">The Legal Entity field displays the current Legal entity by default.</span></span>   
6. <span data-ttu-id="43490-119">Klicken Sie im Feld "Projekt" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="43490-119">In the Project field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="43490-120">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="43490-120">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="43490-121">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="43490-121">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="43490-122">Klicken Sie im Feld "Aktivität" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="43490-122">In the Activity field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="43490-123">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="43490-123">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="43490-124">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="43490-124">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="43490-125">Klicken Sie im Feld "Kategorie" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="43490-125">In the Category field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="43490-126">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="43490-126">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="43490-127">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="43490-127">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="43490-128">Geben Sie die Anzahl der pro Tag gearbeiteten Stunden ein.</span><span class="sxs-lookup"><span data-stu-id="43490-128">Enter the number of hours worked each day.</span></span>
    * <span data-ttu-id="43490-129">Die Stunden sollen im Dezimalformat eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="43490-129">Hours should be entered in a decimal format.</span></span>  <span data-ttu-id="43490-130">Beispiel: Wenn Sie zwei Stunden und 15 Minuten gearbeitet haben, geben Sie "2,25" ein.</span><span class="sxs-lookup"><span data-stu-id="43490-130">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
16. <span data-ttu-id="43490-131">Geben Sie die Anzahl der pro Tag gearbeiteten Stunden ein.</span><span class="sxs-lookup"><span data-stu-id="43490-131">Enter the number of hours worked each day.</span></span>
    * <span data-ttu-id="43490-132">Die Stunden sollen im Dezimalformat eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="43490-132">Hours should be entered in a decimal format.</span></span>  <span data-ttu-id="43490-133">Beispiel: Wenn Sie zwei Stunden und 15 Minuten gearbeitet haben, geben Sie "2,25" ein.</span><span class="sxs-lookup"><span data-stu-id="43490-133">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
17. <span data-ttu-id="43490-134">Geben Sie die Anzahl der pro Tag gearbeiteten Stunden ein.</span><span class="sxs-lookup"><span data-stu-id="43490-134">Enter the number of hours worked each day.</span></span>
    * <span data-ttu-id="43490-135">Die Stunden sollen im Dezimalformat eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="43490-135">Hours should be entered in a decimal format.</span></span>  <span data-ttu-id="43490-136">Beispiel: Wenn Sie zwei Stunden und 15 Minuten gearbeitet haben, geben Sie "2,25" ein.</span><span class="sxs-lookup"><span data-stu-id="43490-136">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
18. <span data-ttu-id="43490-137">Geben Sie die Anzahl der pro Tag gearbeiteten Stunden ein.</span><span class="sxs-lookup"><span data-stu-id="43490-137">Enter the number of hours worked each day.</span></span>
    * <span data-ttu-id="43490-138">Die Stunden sollen im Dezimalformat eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="43490-138">Hours should be entered in a decimal format.</span></span>  <span data-ttu-id="43490-139">Beispiel: Wenn Sie zwei Stunden und 15 Minuten gearbeitet haben, geben Sie "2,25" ein.</span><span class="sxs-lookup"><span data-stu-id="43490-139">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
19. <span data-ttu-id="43490-140">Geben Sie die Anzahl der pro Tag gearbeiteten Stunden ein.</span><span class="sxs-lookup"><span data-stu-id="43490-140">Enter the number of hours worked each day.</span></span>
    * <span data-ttu-id="43490-141">Die Stunden sollen im Dezimalformat eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="43490-141">Hours should be entered in a decimal format.</span></span>  <span data-ttu-id="43490-142">Beispiel: Wenn Sie zwei Stunden und 15 Minuten gearbeitet haben, geben Sie "2,25" ein.</span><span class="sxs-lookup"><span data-stu-id="43490-142">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
    * <span data-ttu-id="43490-143">Unter ausführlich Positionsdetails sind die folgenden Optionen verfügbar: o Einfügen von Informationen über Steuern und Finanzdimensionen.</span><span class="sxs-lookup"><span data-stu-id="43490-143">In Line details, the following options are available:  o  Add information about taxes and financial dimensions.</span></span>  <span data-ttu-id="43490-144">o    Kommentare zu Arbeitszeitnachweispositionen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="43490-144">o    Add comments about the timesheet line.</span></span>  
20. <span data-ttu-id="43490-145">Klicken Sie zum Öffnen des Dropdown-Dialogfeldformulars auf ''.</span><span class="sxs-lookup"><span data-stu-id="43490-145">Click Workflow to open the drop dialog.</span></span>
21. <span data-ttu-id="43490-146">Klicken Sie auf Absenden.</span><span class="sxs-lookup"><span data-stu-id="43490-146">Click Submit.</span></span>
22. <span data-ttu-id="43490-147">Klicken Sie auf Absenden.</span><span class="sxs-lookup"><span data-stu-id="43490-147">Click Submit.</span></span>

