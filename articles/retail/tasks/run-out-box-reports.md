---
title: Generieren und Ausführung von Fertigberichten
description: Führen Sie mithilfe dieses Aufgabenhandbuchs Fertigberichte in der Zentralverwaltung aus verschiedenen Arbeitsbereichen und Abfrage- und Verkaufsberichte unter Einzelhandel und Handel aus.
author: ashishmsft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailCategoryAndProductWorkspace, RetailOrgHierarchyTreeLookup, SrsReportViewerForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: afd4509bc9bdff345e48a590a12cc84ae25aebb8
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2019
ms.locfileid: "2018431"
---
# <a name="generate-and-run-out-of-box-reports"></a><span data-ttu-id="72165-103">Generieren und Ausführung von Fertigberichten</span><span class="sxs-lookup"><span data-stu-id="72165-103">Generate and run out of box reports</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="72165-104">Führen Sie mithilfe dieses Aufgabenhandbuchs Fertigberichte in der Zentralverwaltung aus verschiedenen Arbeitsbereichen und Abfrage- und Verkaufsberichte unter Einzelhandel und Handel aus.</span><span class="sxs-lookup"><span data-stu-id="72165-104">Use this task guide to run out of box reports in headquarters from different workspaces and Inquiries & Sales reports located under Retail & Commerce.</span></span>



<span data-ttu-id="72165-105">Das Demodatenunternehmen, das verwendet wird, um diese Aufzeichnung zu erstellen, ist USRT.</span><span class="sxs-lookup"><span data-stu-id="72165-105">The demo data company used to create this recording is USRT.</span></span> <span data-ttu-id="72165-106">Diese Aufzeichnung ist für die Systemadministratorrolle vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="72165-106">This recording is intended for the System administrator role.</span></span>


## <a name="launch-reports-from-workspaces"></a><span data-ttu-id="72165-107">Starten von Berichten aus den Arbeitsbereichen</span><span class="sxs-lookup"><span data-stu-id="72165-107">Launch reports from workspaces</span></span>
1. <span data-ttu-id="72165-108">Navigieren Sie zu Einzelhandel und Handel > Produkte und Kategorien > Kategorie- und Produktverwaltung.</span><span class="sxs-lookup"><span data-stu-id="72165-108">Go to Retail and commerce > Products and categories > Category and product management.</span></span>
2. <span data-ttu-id="72165-109">Klicken Sie zum Erweitern oder Reduzieren des Abschnitts ''Berichte" auf den Pfeil.</span><span class="sxs-lookup"><span data-stu-id="72165-109">Click the arrow to expand or collapse the Reports section.</span></span>
3. <span data-ttu-id="72165-110">Klicken Sie auf "Bericht über Top-Produkte".</span><span class="sxs-lookup"><span data-stu-id="72165-110">Click Top products report.</span></span>
4. <span data-ttu-id="72165-111">Geben Sie in das Feld "Von Datum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="72165-111">In the From date field, enter a date.</span></span>
5. <span data-ttu-id="72165-112">Geben Sie in das Feld "Bis Datum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="72165-112">In the To date field, enter a date.</span></span>
6. <span data-ttu-id="72165-113">Klicken Sie im Feld "Kanal" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="72165-113">In the Channel field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="72165-114">Wählen Sie in der Struktur "Contoso Retail\Contoso Retail USA\Central\Houston" aus.</span><span class="sxs-lookup"><span data-stu-id="72165-114">In the tree, select 'Contoso Retail\Contoso Retail USA\Central\Houston'.</span></span>
    * <span data-ttu-id="72165-115">Hier wird die standardmäßige Einzelhandelsorganisationshierarchie für Einzelhandelsberichterstellungszwecke angezeigt.</span><span class="sxs-lookup"><span data-stu-id="72165-115">This shows the default retail organization hierarchy for Retail reporting purpose.</span></span>   <span data-ttu-id="72165-116">Wechseln Sie zu Organisationsverwaltung > Organisationen > Organisationshierarchiezwecke und wählen Sie „Berichterstellung im Einzelhandel“ aus. Aktivieren Sie unter „Zugewiesene Hierarchien“ den Hierarchienamen, für den die Standard-Spalte aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="72165-116">Go to Organization administration >  Organizations > Organization hierarchy purposes and choose Retail reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span> <span data-ttu-id="72165-117">Im Rahmen der Demodaten (für diese Aufgabenerfassung) ist "Einzelhandelsgeschäfte nach Region" die standardmäßige Organisationshierarchie für Einzelhandelsberichterstellungszwecke.</span><span class="sxs-lookup"><span data-stu-id="72165-117">As part of demo data (used for this task recording) you would notice, Retail Stores by Region, is the default organization hierarchy for the Retail reporting purpose.</span></span>     
8. <span data-ttu-id="72165-118">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="72165-118">Click OK.</span></span>
9. <span data-ttu-id="72165-119">Wählen Sie im Feld "Ansicht" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="72165-119">In the View field, select an option.</span></span>
10. <span data-ttu-id="72165-120">Wählen Sie im Feld "Von" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="72165-120">In the By field, select an option.</span></span>
11. <span data-ttu-id="72165-121">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="72165-121">Click OK.</span></span>

## <a name="launch-reports-from-the-inquiries-and-sales-reports-located-under-retail--commerce-app-link"></a><span data-ttu-id="72165-122">Starten Sie Berichte von Abfrage- und Verkaufsberichten unter dem App-Link "Einzelhandel und Handel".</span><span class="sxs-lookup"><span data-stu-id="72165-122">Launch reports from the inquiries and sales reports located under Retail & Commerce app link.</span></span>
1. <span data-ttu-id="72165-123">Navigieren Sie zu Einzelhandel und Handel > Abfragen und Berichte > Umsatzberichte > Kategorieverkaufsbericht.</span><span class="sxs-lookup"><span data-stu-id="72165-123">Go to Retail and commerce > Inquiries and reports > Sales reports > Category sales report.</span></span>
2. <span data-ttu-id="72165-124">Geben Sie in das Feld "Von Datum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="72165-124">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="72165-125">Geben Sie in das Feld "Bis Datum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="72165-125">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="72165-126">Klicken Sie im Feld "Kanal" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="72165-126">In the Channel field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="72165-127">Wählen Sie in der Struktur "Contoso Retail\Contoso Retail USA\West\Seattle" aus.</span><span class="sxs-lookup"><span data-stu-id="72165-127">In the tree, select 'Contoso Retail\Contoso Retail USA\West\Seattle'.</span></span>
    * <span data-ttu-id="72165-128">Hier wird die standardmäßige Einzelhandelsorganisationshierarchie für Einzelhandelsberichterstellungszwecke angezeigt.</span><span class="sxs-lookup"><span data-stu-id="72165-128">This shows the default retail organization hierarchy for Retail reporting purpose.</span></span>   <span data-ttu-id="72165-129">Wechseln Sie zu Organisationsverwaltung > Organisationen > Organisationshierarchiezwecke und wählen Sie „Berichterstellung im Einzelhandel“ aus. Aktivieren Sie unter „Zugewiesene Hierarchien“ den Hierarchienamen, für den die Standard-Spalte aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="72165-129">Go to Organization administration  > Organizations > Organization hierarchy purposes and choose Retail reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span> <span data-ttu-id="72165-130">Im Rahmen der Demodaten (für diese Aufgabenerfassung) ist "Einzelhandelsgeschäfte nach Region" die standardmäßige Organisationshierarchie für Einzelhandelsberichterstellungszwecke.</span><span class="sxs-lookup"><span data-stu-id="72165-130">As part of demo data (used for this task recording) you would notice, Retail Stores by Region, is the default organization hierarchy for the Retail reporting purpose.</span></span>     
6. <span data-ttu-id="72165-131">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="72165-131">Click OK.</span></span>
7. <span data-ttu-id="72165-132">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="72165-132">Click OK.</span></span>

## <a name="export-an-hq-reports"></a><span data-ttu-id="72165-133">Exportieren von HQ-Berichten</span><span class="sxs-lookup"><span data-stu-id="72165-133">Export an HQ reports</span></span>
1. <span data-ttu-id="72165-134">Navigieren Sie zu Einzelhandel und Handel > Abfragen und Berichte > Umsatzberichte > Bericht 'Organisationsumsatz''.</span><span class="sxs-lookup"><span data-stu-id="72165-134">Go to Retail and commerce > Inquiries and reports > Sales reports > Organization sales report.</span></span>
2. <span data-ttu-id="72165-135">Geben Sie in das Feld "Von Datum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="72165-135">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="72165-136">Geben Sie in das Feld "Bis Datum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="72165-136">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="72165-137">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="72165-137">Click OK.</span></span>
5. <span data-ttu-id="72165-138">Klicken Sie auf "Export".</span><span class="sxs-lookup"><span data-stu-id="72165-138">Click Export.</span></span>
6. <span data-ttu-id="72165-139">Klicken Sie auf "PDF".</span><span class="sxs-lookup"><span data-stu-id="72165-139">Click PDF.</span></span>

