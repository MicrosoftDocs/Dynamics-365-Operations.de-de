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
ms.openlocfilehash: b42f86fc243312d18654b1a048f9dffb29afd187
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "365246"
---
# <a name="generate-and-run-out-of-box-reports"></a><span data-ttu-id="ffb70-103">Generieren und Ausführung von Fertigberichten</span><span class="sxs-lookup"><span data-stu-id="ffb70-103">Generate and run out of box reports</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="ffb70-104">Führen Sie mithilfe dieses Aufgabenhandbuchs Fertigberichte in der Zentralverwaltung aus verschiedenen Arbeitsbereichen und Abfrage- und Verkaufsberichte unter Einzelhandel und Handel aus.</span><span class="sxs-lookup"><span data-stu-id="ffb70-104">Use this task guide to run out of box reports in headquarters from different workspaces and Inquiries & Sales reports located under Retail & Commerce.</span></span>



<span data-ttu-id="ffb70-105">Das Demodatenunternehmen, das verwendet wird, um diese Aufzeichnung zu erstellen, ist USRT.</span><span class="sxs-lookup"><span data-stu-id="ffb70-105">The demo data company used to create this recording is USRT.</span></span> <span data-ttu-id="ffb70-106">Diese Aufzeichnung ist für die Systemadministratorrolle vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="ffb70-106">This recording is intended for the System administrator role.</span></span>


## <a name="launch-reports-from-workspaces"></a><span data-ttu-id="ffb70-107">Starten von Berichten aus den Arbeitsbereichen</span><span class="sxs-lookup"><span data-stu-id="ffb70-107">Launch reports from workspaces</span></span>
1. <span data-ttu-id="ffb70-108">Navigieren Sie zu Einzelhandel und Handel > Produkte und Kategorien > Kategorie- und Produktverwaltung.</span><span class="sxs-lookup"><span data-stu-id="ffb70-108">Go to Retail and commerce > Products and categories > Category and product management.</span></span>
2. <span data-ttu-id="ffb70-109">Klicken Sie zum Erweitern oder Reduzieren des Abschnitts ''Berichte" auf den Pfeil.</span><span class="sxs-lookup"><span data-stu-id="ffb70-109">Click the arrow to expand or collapse the Reports section.</span></span>
3. <span data-ttu-id="ffb70-110">Klicken Sie auf "Bericht über Top-Produkte".</span><span class="sxs-lookup"><span data-stu-id="ffb70-110">Click Top products report.</span></span>
4. <span data-ttu-id="ffb70-111">Geben Sie in das Feld "Von Datum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="ffb70-111">In the From date field, enter a date.</span></span>
5. <span data-ttu-id="ffb70-112">Geben Sie in das Feld "Bis Datum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="ffb70-112">In the To date field, enter a date.</span></span>
6. <span data-ttu-id="ffb70-113">Klicken Sie im Feld "Kanal" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ffb70-113">In the Channel field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="ffb70-114">Wählen Sie in der Struktur "Contoso Retail\Contoso Retail USA\Central\Houston" aus.</span><span class="sxs-lookup"><span data-stu-id="ffb70-114">In the tree, select 'Contoso Retail\Contoso Retail USA\Central\Houston'.</span></span>
    * <span data-ttu-id="ffb70-115">Hier wird die standardmäßige Einzelhandelsorganisationshierarchie für Einzelhandelsberichterstellungszwecke angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ffb70-115">This shows the default retail organization hierarchy for Retail reporting purpose.</span></span>   <span data-ttu-id="ffb70-116">Wechseln Sie zu Organisationsverwaltung   Organisationen > Organisationshierarchiezwecke und wählen Sie "Berichterstellung im Einzelhandel" aus. Aktivieren Sie unter "Zugewiesene Hierarchien" den Hierarchienamen, für den die Standard-Spalte aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="ffb70-116">Go to Organization administration >Organizations >Organization hierarchy purposes and choose Retail reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span>      <span data-ttu-id="ffb70-117">Im Rahmen der Demodaten (für diese Aufgabenerfassung) ist "Einzelhandelsgeschäfte nach Region" die standardmäßige Organisationshierarchie für Einzelhandelsberichterstellungszwecke.</span><span class="sxs-lookup"><span data-stu-id="ffb70-117">As part of demo data (used for this task recording) you would notice, Retail Stores by Region, is the default organization hierarchy for the Retail reporting purpose.</span></span>     
8. <span data-ttu-id="ffb70-118">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="ffb70-118">Click OK.</span></span>
9. <span data-ttu-id="ffb70-119">Wählen Sie im Feld "Ansicht" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="ffb70-119">In the View field, select an option.</span></span>
10. <span data-ttu-id="ffb70-120">Wählen Sie im Feld "Von" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="ffb70-120">In the By field, select an option.</span></span>
11. <span data-ttu-id="ffb70-121">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="ffb70-121">Click OK.</span></span>

## <a name="launch-reports-from-the-inquiries-and-sales-reports-located-under-retail--commerce-app-link"></a><span data-ttu-id="ffb70-122">Starten Sie Berichte von Abfrage- und Verkaufsberichten unter dem App-Link "Einzelhandel und Handel".</span><span class="sxs-lookup"><span data-stu-id="ffb70-122">Launch reports from the inquiries and sales reports located under Retail & Commerce app link.</span></span>
1. <span data-ttu-id="ffb70-123">Navigieren Sie zu Einzelhandel und Handel > Abfragen und Berichte > Umsatzberichte > Kategorieverkaufsbericht.</span><span class="sxs-lookup"><span data-stu-id="ffb70-123">Go to Retail and commerce > Inquiries and reports > Sales reports > Category sales report.</span></span>
2. <span data-ttu-id="ffb70-124">Geben Sie in das Feld "Von Datum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="ffb70-124">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="ffb70-125">Geben Sie in das Feld "Bis Datum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="ffb70-125">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="ffb70-126">Klicken Sie im Feld "Kanal" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ffb70-126">In the Channel field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="ffb70-127">Wählen Sie in der Struktur "Contoso Retail\Contoso Retail USA\West\Seattle" aus.</span><span class="sxs-lookup"><span data-stu-id="ffb70-127">In the tree, select 'Contoso Retail\Contoso Retail USA\West\Seattle'.</span></span>
    * <span data-ttu-id="ffb70-128">Hier wird die standardmäßige Einzelhandelsorganisationshierarchie für Einzelhandelsberichterstellungszwecke angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ffb70-128">This shows the default retail organization hierarchy for Retail reporting purpose.</span></span>   <span data-ttu-id="ffb70-129">Wechseln Sie zu Organisationsverwaltung   Organisationen > Organisationshierarchiezwecke und wählen Sie "Berichterstellung im Einzelhandel" aus. Aktivieren Sie unter "Zugewiesene Hierarchien" den Hierarchienamen, für den die Standard-Spalte aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="ffb70-129">Go to Organization administration >Organizations >Organization hierarchy purposes and choose Retail reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span>      <span data-ttu-id="ffb70-130">Im Rahmen der Demodaten (für diese Aufgabenerfassung) ist "Einzelhandelsgeschäfte nach Region" die standardmäßige Organisationshierarchie für Einzelhandelsberichterstellungszwecke.</span><span class="sxs-lookup"><span data-stu-id="ffb70-130">As part of demo data (used for this task recording) you would notice, Retail Stores by Region, is the default organization hierarchy for the Retail reporting purpose.</span></span>     
6. <span data-ttu-id="ffb70-131">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="ffb70-131">Click OK.</span></span>
7. <span data-ttu-id="ffb70-132">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="ffb70-132">Click OK.</span></span>

## <a name="export-an-hq-reports"></a><span data-ttu-id="ffb70-133">Exportieren von HQ-Berichten</span><span class="sxs-lookup"><span data-stu-id="ffb70-133">Export an HQ reports</span></span>
1. <span data-ttu-id="ffb70-134">Navigieren Sie zu Einzelhandel und Handel > Abfragen und Berichte > Umsatzberichte > Bericht 'Organisationsumsatz''.</span><span class="sxs-lookup"><span data-stu-id="ffb70-134">Go to Retail and commerce > Inquiries and reports > Sales reports > Organization sales report.</span></span>
2. <span data-ttu-id="ffb70-135">Geben Sie in das Feld "Von Datum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="ffb70-135">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="ffb70-136">Geben Sie in das Feld "Bis Datum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="ffb70-136">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="ffb70-137">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="ffb70-137">Click OK.</span></span>
5. <span data-ttu-id="ffb70-138">Klicken Sie auf "Export".</span><span class="sxs-lookup"><span data-stu-id="ffb70-138">Click Export.</span></span>
6. <span data-ttu-id="ffb70-139">Klicken Sie auf "PDF".</span><span class="sxs-lookup"><span data-stu-id="ffb70-139">Click PDF.</span></span>

