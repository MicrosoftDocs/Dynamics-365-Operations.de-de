---
title: Arbeitsnachweise des Projekts eingeben
description: In dieser Prozedur erstellen Sie einen Arbeitszeitnachweis, indem Sie ein leeres Arbeitszeitnachweisformular verwenden.
author: andreabichsel
manager: AnnBe
ms.date: 08/08/2019
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
ms.openlocfilehash: d2fd5c1e6c38c2e4380a8c8b061b08bce2dd43c8
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916506"
---
# <a name="enter-project-timesheets"></a><span data-ttu-id="cec7d-103">Arbeitsnachweise des Projekts eingeben</span><span class="sxs-lookup"><span data-stu-id="cec7d-103">Enter project timesheets</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cec7d-104">In dieser Prozedur erstellen Sie einen Arbeitszeitnachweis, indem Sie ein leeres Arbeitszeitnachweisformular verwenden.</span><span class="sxs-lookup"><span data-stu-id="cec7d-104">This procedure lets you create a timesheet by using an empty timesheet form.</span></span> <span data-ttu-id="cec7d-105">Der neue Arbeitszeitnachweis kann auf Informationen aus einem vorherigen Arbeitszeitnachweis oder Projekt- und Aktivitätszuweisungen auf der Seite **Eigene Favoriten** basieren.</span><span class="sxs-lookup"><span data-stu-id="cec7d-105">The new timesheet can be based on information from a previous timesheet, or from project and activity assignments in the **My favorites** page.</span></span> <span data-ttu-id="cec7d-106">Standardmäßig werden auf der Listenseite **Alle Arbeitszeitnachweise** alle Arbeitszeitnachweise für die aktuelle Periode angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cec7d-106">By default, the **All timesheets** list page displays all your timesheets for the current period.</span></span> <span data-ttu-id="cec7d-107">Sie können über die Dropdownliste für das Feld **Anzeigen** auf der Seite **Eigene Arbeitszeitnachweise** die Arbeitszeitnachweisliste nach Zeitraum oder Projekt filtern oder Arbeitszeitnachweise anzeigen, die im Auftrag anderer Arbeitskräfte erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="cec7d-107">You can use the drop-down list for the **Show** field in the **My timesheets** page to filter the timesheet list by time period or project, or to view timesheets that were created on behalf of other workers.</span></span> <span data-ttu-id="cec7d-108">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USSI.</span><span class="sxs-lookup"><span data-stu-id="cec7d-108">The demo data company used to create this procedure is USSI.</span></span> 

1. <span data-ttu-id="cec7d-109">Wechseln Sie im **Navigationsbereich** zu **Module > Projektverwaltung und -verrechnung > Arbeitszeitnachweise > Meine Arbeitszeitnachweise**.</span><span class="sxs-lookup"><span data-stu-id="cec7d-109">In the **Navigation pane**, go to **Modules > Project management and accounting > Timesheets > My timesheets**.</span></span>
2. <span data-ttu-id="cec7d-110">Um einen neuen Arbeitszeitnachweis einzugeben, klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="cec7d-110">To enter a new timesheet, click **New**.</span></span>
    - <span data-ttu-id="cec7d-111">Die Dropdownliste "Ressourcen" zeigt die Arbeitskraft an, die dem aktuellen Benutzer standardmäßig zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="cec7d-111">The Resource drop-down list shows the worker assigned to the current user, by default.</span></span>  
    - <span data-ttu-id="cec7d-112">Wenn der Benutzer als Stellvertreter ausgewählt wird, werden die Namen aufgeführt, damit ein Benutzer einen Arbeitszeitnachweis in dessen Namen eingeben kann.</span><span class="sxs-lookup"><span data-stu-id="cec7d-112">If the user is designated as a delegate, this will list the names so that a user can enter a timesheet on their behalf.</span></span>  
3. <span data-ttu-id="cec7d-113">Geben Sie ein Datum in das Feld **Datum** ein.</span><span class="sxs-lookup"><span data-stu-id="cec7d-113">In the **Date** field, enter a date.</span></span> <span data-ttu-id="cec7d-114">Wenn diese Option ausgewählt ist, werden neue Arbeitszeitnachweispositionen über Arbeitszeitnachweiseinstellungen erstellt, die als Favoriten konfiguriert wurden.</span><span class="sxs-lookup"><span data-stu-id="cec7d-114">If this option is selected, new timesheet lines will be created by using the timesheet settings that were configured as favorites.</span></span>  
4. <span data-ttu-id="cec7d-115">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="cec7d-115">Click **OK**.</span></span>
5. <span data-ttu-id="cec7d-116">Klicken Sie auf **Neue Position**.</span><span class="sxs-lookup"><span data-stu-id="cec7d-116">Click **New line**.</span></span>
6. <span data-ttu-id="cec7d-117">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="cec7d-117">In the list, mark the selected row.</span></span> <span data-ttu-id="cec7d-118">Das Feld **Juristische Person** enthält standardmäßig die aktuelle juristische Person.</span><span class="sxs-lookup"><span data-stu-id="cec7d-118">The **Legal Entity** field displays the current Legal entity by default.</span></span>   
7. <span data-ttu-id="cec7d-119">Klicken Sie im Feld **Projekt** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="cec7d-119">In the **Project** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="cec7d-120">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="cec7d-120">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="cec7d-121">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="cec7d-121">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="cec7d-122">Klicken Sie im Feld **Aktivitätsnummer** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="cec7d-122">In the **Activity number** field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="cec7d-123">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="cec7d-123">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="cec7d-124">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="cec7d-124">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="cec7d-125">Klicken Sie im Feld **Kategorie** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="cec7d-125">In the **Category** field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="cec7d-126">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="cec7d-126">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="cec7d-127">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="cec7d-127">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="cec7d-128">Geben Sie die Anzahl der pro Tag gearbeiteten Stunden ein.</span><span class="sxs-lookup"><span data-stu-id="cec7d-128">Enter the number of hours worked each day.</span></span> <span data-ttu-id="cec7d-129">Geben Sie die Stunden mit Dezimalstellen ein.</span><span class="sxs-lookup"><span data-stu-id="cec7d-129">Enter the hours in decimal format.</span></span> <span data-ttu-id="cec7d-130">Beispiel: Wenn Sie zwei Stunden und 15 Minuten gearbeitet haben, geben Sie "2,25" ein.</span><span class="sxs-lookup"><span data-stu-id="cec7d-130">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
17. <span data-ttu-id="cec7d-131">In den **Positionsdetails** sind die folgende Optionen verfügbar:</span><span class="sxs-lookup"><span data-stu-id="cec7d-131">In **Line details**, the following options are available:</span></span>
    - <span data-ttu-id="cec7d-132">Fügen Sie Informationen zu Steuern und Finanzdimensionen in der Registerkarte **Allgemein** und **Finanzdimensionen** hinzu.</span><span class="sxs-lookup"><span data-stu-id="cec7d-132">Add information about taxes and financial dimensions in the **General** and the **Financial Dimensions** tab.</span></span>
    - <span data-ttu-id="cec7d-133">Fügen Sie Kommentare zur Arbeitszeitnachweisposition in der Registerkarte **Kommentar** hinzu.</span><span class="sxs-lookup"><span data-stu-id="cec7d-133">Add comments about the timesheet line in the **Comment** tab.</span></span>
20. <span data-ttu-id="cec7d-134">Klicken Sie im **Aktivitätsbereich** auf **Workflow**, um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="cec7d-134">In the **Action pane**, click **Workflow** to open the drop dialog.</span></span>
21. <span data-ttu-id="cec7d-135">Klicken Sie auf **Absenden**.</span><span class="sxs-lookup"><span data-stu-id="cec7d-135">Click **Submit**.</span></span>
22. <span data-ttu-id="cec7d-136">Klicken Sie auf **Absenden**.</span><span class="sxs-lookup"><span data-stu-id="cec7d-136">Click **Submit**.</span></span>

