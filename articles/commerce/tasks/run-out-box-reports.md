---
title: Generieren und Ausführung von Fertigberichten
description: Führen Sie mithilfe dieses Aufgabenhandbuchs Fertigberichte in der Hauptniederlassung aus verschiedenen Arbeitsbereichen und Abfrage- und Verkaufsberichte in Commerce aus.
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
ms.openlocfilehash: 0d148fa36a116860af8c44043d90759b8a2d76fb
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140760"
---
# <a name="generate-and-run-out-of-box-reports"></a><span data-ttu-id="a55b0-103">Generieren und Ausführung von Fertigberichten</span><span class="sxs-lookup"><span data-stu-id="a55b0-103">Generate and run out of box reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a55b0-104">Führen Sie mithilfe dieses Aufgabenhandbuchs Fertigberichte in der Hauptniederlassung aus verschiedenen Arbeitsbereichen und Abfrage- und Verkaufsberichte in Commerce aus.</span><span class="sxs-lookup"><span data-stu-id="a55b0-104">Use this task guide to run out of box reports in Headquarters from different workspaces and Inquiries & Sales reports located in Commerce.</span></span>

<span data-ttu-id="a55b0-105">Das Demodatenunternehmen, das verwendet wird, um diese Aufzeichnung zu erstellen, ist USRT.</span><span class="sxs-lookup"><span data-stu-id="a55b0-105">The demo data company used to create this recording is USRT.</span></span> <span data-ttu-id="a55b0-106">Diese Aufzeichnung ist für die Systemadministratorrolle vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="a55b0-106">This recording is intended for the System administrator role.</span></span>

## <a name="launch-reports-from-workspaces"></a><span data-ttu-id="a55b0-107">Starten von Berichten aus den Arbeitsbereichen</span><span class="sxs-lookup"><span data-stu-id="a55b0-107">Launch reports from workspaces</span></span>
1. <span data-ttu-id="a55b0-108">Gehen Sie zu Retail und Commerce > Produkte und Kategorien > Kategorie- und Produktverwaltung.</span><span class="sxs-lookup"><span data-stu-id="a55b0-108">Go to Retail and Commerce > Products and categories > Category and product management.</span></span>
2. <span data-ttu-id="a55b0-109">Klicken Sie zum Erweitern oder Reduzieren des Abschnitts ''Berichte" auf den Pfeil.</span><span class="sxs-lookup"><span data-stu-id="a55b0-109">Click the arrow to expand or collapse the Reports section.</span></span>
3. <span data-ttu-id="a55b0-110">Klicken Sie auf "Bericht über Top-Produkte".</span><span class="sxs-lookup"><span data-stu-id="a55b0-110">Click Top products report.</span></span>
4. <span data-ttu-id="a55b0-111">Geben Sie in das Feld "Von Datum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="a55b0-111">In the From date field, enter a date.</span></span>
5. <span data-ttu-id="a55b0-112">Geben Sie in das Feld "Bis Datum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="a55b0-112">In the To date field, enter a date.</span></span>
6. <span data-ttu-id="a55b0-113">Klicken Sie im Feld "Kanal" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="a55b0-113">In the Channel field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="a55b0-114">Wählen Sie in der Struktur "Contoso Retail\Contoso Retail USA\Central\Houston" aus.</span><span class="sxs-lookup"><span data-stu-id="a55b0-114">In the tree, select 'Contoso Retail\Contoso Retail USA\Central\Houston'.</span></span>
    * <span data-ttu-id="a55b0-115">Hier wird die standardmäßige Organisationshierarchie für Commerce-Berichterstellungszwecke angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a55b0-115">This shows the default organization hierarchy for Commerce reporting purpose.</span></span>   <span data-ttu-id="a55b0-116">Wechseln Sie zu Organisationsverwaltung > Organisationen > Organisationshierarchiezwecke und wählen Sie „Berichterstellung in Commerce“ aus. Aktivieren Sie unter „Zugewiesene Hierarchien“ den Hierarchienamen, für den die Standard-Spalte aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="a55b0-116">Go to Organization administration > Organizations > Organization hierarchy purposes and choose Commerce reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span> <span data-ttu-id="a55b0-117">Im Rahmen der Demodaten (für diese Aufgabenaufzeichnung) ist „Filialen nach Region“ die standardmäßige Organisationshierarchie für Berichterstellungszwecke.</span><span class="sxs-lookup"><span data-stu-id="a55b0-117">As part of demo data (used for this task recording) you would notice, Stores by Region, is the default organization hierarchy for the reporting purpose.</span></span>     
8. <span data-ttu-id="a55b0-118">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="a55b0-118">Click OK.</span></span>
9. <span data-ttu-id="a55b0-119">Wählen Sie im Feld "Ansicht" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="a55b0-119">In the View field, select an option.</span></span>
10. <span data-ttu-id="a55b0-120">Wählen Sie im Feld "Von" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="a55b0-120">In the By field, select an option.</span></span>
11. <span data-ttu-id="a55b0-121">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="a55b0-121">Click OK.</span></span>

## <a name="launch-reports-from-the-inquiries-and-sales-reports"></a><span data-ttu-id="a55b0-122">Starten von Berichten aus Abfrage- und Verkaufsberichten</span><span class="sxs-lookup"><span data-stu-id="a55b0-122">Launch reports from the inquiries and sales reports</span></span>
1. <span data-ttu-id="a55b0-123">Gehen Sie zu Retail und Commerce > Abfragen und Berichte > Verkaufsberichte > Kategorieverkaufsbericht.</span><span class="sxs-lookup"><span data-stu-id="a55b0-123">Go to Retail and Commerce > Inquiries and reports > Sales reports > Category sales report.</span></span>
2. <span data-ttu-id="a55b0-124">Geben Sie in das Feld "Von Datum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="a55b0-124">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="a55b0-125">Geben Sie in das Feld "Bis Datum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="a55b0-125">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="a55b0-126">Klicken Sie im Feld "Kanal" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="a55b0-126">In the Channel field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="a55b0-127">Wählen Sie in der Struktur "Contoso Retail\Contoso Retail USA\West\Seattle" aus.</span><span class="sxs-lookup"><span data-stu-id="a55b0-127">In the tree, select 'Contoso Retail\Contoso Retail USA\West\Seattle'.</span></span>
    * <span data-ttu-id="a55b0-128">Hier wird die standardmäßige Organisationshierarchie für Commerce-Berichterstellungszwecke angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a55b0-128">This shows the default organization hierarchy for Commerce reporting purpose.</span></span> <span data-ttu-id="a55b0-129">Wechseln Sie zu Organisationsverwaltung > Organisationen > Organisationshierarchiezwecke und wählen Sie „Berichterstellung in Commerce“ aus. Aktivieren Sie unter „Zugewiesene Hierarchien“ den Hierarchienamen, für den die Standard-Spalte aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="a55b0-129">Go to Organization administration > Organizations > Organization hierarchy purposes and choose Commerce reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span> <span data-ttu-id="a55b0-130">Im Rahmen der Demodaten (für diese Aufgabenaufzeichnung) ist „Filialen nach Region“ die standardmäßige Organisationshierarchie für Berichterstellungszwecke.</span><span class="sxs-lookup"><span data-stu-id="a55b0-130">As part of demo data (used for this task recording) you would notice, Stores by Region, is the default organization hierarchy for the reporting purpose.</span></span>     
6. <span data-ttu-id="a55b0-131">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="a55b0-131">Click OK.</span></span>
7. <span data-ttu-id="a55b0-132">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="a55b0-132">Click OK.</span></span>

## <a name="export-an-hq-reports"></a><span data-ttu-id="a55b0-133">Exportieren von HQ-Berichten</span><span class="sxs-lookup"><span data-stu-id="a55b0-133">Export an HQ reports</span></span>
1. <span data-ttu-id="a55b0-134">Gehen Sie zu Retail und Commerce > Abfragen und Berichte > Verkaufsberichte > Organisationsverkaufsbericht.</span><span class="sxs-lookup"><span data-stu-id="a55b0-134">Go to Retail and Commerce > Inquiries and reports > Sales reports > Organization sales report.</span></span>
2. <span data-ttu-id="a55b0-135">Geben Sie in das Feld "Von Datum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="a55b0-135">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="a55b0-136">Geben Sie in das Feld "Bis Datum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="a55b0-136">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="a55b0-137">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="a55b0-137">Click OK.</span></span>
5. <span data-ttu-id="a55b0-138">Klicken Sie auf "Export".</span><span class="sxs-lookup"><span data-stu-id="a55b0-138">Click Export.</span></span>
6. <span data-ttu-id="a55b0-139">Klicken Sie auf "PDF".</span><span class="sxs-lookup"><span data-stu-id="a55b0-139">Click PDF.</span></span>

