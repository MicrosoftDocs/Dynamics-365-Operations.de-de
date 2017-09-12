---
title: "Finanzbericht für die Einkommensaufstellung"
description: "In diesem Artikel werden die Standardberichte für Einkommensaufstellung beschrieben. Er beschreibt zudem die die Bausteine, die diesen Bericht zugeordnet werden."
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 12294
ms.assetid: 30820be0-d943-4f8b-8c25-6414ec393b3d
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 0017d13b7f7594462dfff4ef896f4139607d4bc5
ms.contentlocale: de-de
ms.lasthandoff: 08/29/2017

---

# <a name="income-statement-financial-report"></a><span data-ttu-id="411f6-104">Finanzbericht für die Einkommensaufstellung</span><span class="sxs-lookup"><span data-stu-id="411f6-104">Income statement financial report</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="411f6-105">In diesem Artikel werden die Standardberichte für Einkommensaufstellung beschrieben.</span><span class="sxs-lookup"><span data-stu-id="411f6-105">This article describes the default report for income statements.</span></span> <span data-ttu-id="411f6-106">Er beschreibt zudem die die Bausteine, die diesen Bericht zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="411f6-106">It also describes the building blocks that are associated with this report.</span></span> 

<a name="default-income-statement-report"></a><span data-ttu-id="411f6-107">Standardbericht für die Einkommensaufstellung</span><span class="sxs-lookup"><span data-stu-id="411f6-107">Default income statement report</span></span>
-------------------------------

| <span data-ttu-id="411f6-108">Standardbericht</span><span class="sxs-lookup"><span data-stu-id="411f6-108">Default report</span></span>             | <span data-ttu-id="411f6-109">Funktionsweise</span><span class="sxs-lookup"><span data-stu-id="411f6-109">What it does</span></span>                                                                                              |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="411f6-110">Einkommensaufstellung – Standard</span><span class="sxs-lookup"><span data-stu-id="411f6-110">Income Statement – Default</span></span> | <span data-ttu-id="411f6-111">Enthält eine Ansicht der Rentabilität der Organisation für die aktuelle Periode und seit Jahresbeginn.</span><span class="sxs-lookup"><span data-stu-id="411f6-111">Provides a view of the organization’s profitability for the current period and also for the year to date.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="411f6-112">Bausteine</span><span class="sxs-lookup"><span data-stu-id="411f6-112">Building blocks</span></span>
<span data-ttu-id="411f6-113">Der Finanzbericht für die Einkommensaufstellung verwendet die folgenden Bausteine.</span><span class="sxs-lookup"><span data-stu-id="411f6-113">The income statement financial report uses the following building blocks.</span></span>

| <span data-ttu-id="411f6-114">Standardbericht</span><span class="sxs-lookup"><span data-stu-id="411f6-114">Default report</span></span>             | <span data-ttu-id="411f6-115">Zeilendefinition</span><span class="sxs-lookup"><span data-stu-id="411f6-115">Row definition</span></span>                     | <span data-ttu-id="411f6-116">Spaltendefinition</span><span class="sxs-lookup"><span data-stu-id="411f6-116">Column definition</span></span>          |
|----------------------------|------------------------------------|----------------------------|
| <span data-ttu-id="411f6-117">Einkommensaufstellung - Standard</span><span class="sxs-lookup"><span data-stu-id="411f6-117">Income Statement - Default</span></span> | <span data-ttu-id="411f6-118">Zusammengefasste Einkommensaufstellung - Standard</span><span class="sxs-lookup"><span data-stu-id="411f6-118">Summary Income Statement - Default</span></span> | <span data-ttu-id="411f6-119">Periodisch und seit Jahresbeginn - Standard</span><span class="sxs-lookup"><span data-stu-id="411f6-119">Periodic and YTD - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="411f6-120">Zeilendefinition</span><span class="sxs-lookup"><span data-stu-id="411f6-120">Row definition</span></span>

<span data-ttu-id="411f6-121">Die Zeilendefinition, zusammengefasste Einkommensaufstellung - Standard enthält einen Abschnitt für jeden Teil einer herkömmlichen Einkommensaufstellung.</span><span class="sxs-lookup"><span data-stu-id="411f6-121">The row definition, Summary Income Statement – Default, contains a section for each part of a traditional income statement.</span></span> <span data-ttu-id="411f6-122">Die Hauptkontokategoriedimension wird verwendet, um diese Zeilendefinition aufzubauen.</span><span class="sxs-lookup"><span data-stu-id="411f6-122">The Main Account Category dimension is used to build this row definition.</span></span> <span data-ttu-id="411f6-123">Daher kann jeder Benutzer den Bericht erstellen, ohne Änderungen vorzunehmen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="411f6-123">Therefore, anyone can generate the report without having to make any modifications.</span></span>

### <a name="column-definition"></a><span data-ttu-id="411f6-124">Spaltendefinition</span><span class="sxs-lookup"><span data-stu-id="411f6-124">Column Definition</span></span>

<span data-ttu-id="411f6-125">Die Spaltendefinitionen enthalten verschieden Spaltentypen, um verschiedene Stufen der Genauigkeit und der Finanzdaten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="411f6-125">The column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="411f6-126">**Periodisch und seit Jahresbeginn - Standardspaltentypen:**</span><span class="sxs-lookup"><span data-stu-id="411f6-126">**Periodic and YTD – Default column types:**</span></span>
    -   <span data-ttu-id="411f6-127">**DESC** - Die Beschreibung der Zeilendefinition</span><span class="sxs-lookup"><span data-stu-id="411f6-127">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="411f6-128">**FD** - Finanzdaten für die aktuelle Periode</span><span class="sxs-lookup"><span data-stu-id="411f6-128">**FD** – Financial data for the current period</span></span>
    -   <span data-ttu-id="411f6-129">**FD** - Finanzdaten seit Jahresbeginn</span><span class="sxs-lookup"><span data-stu-id="411f6-129">**FD** – Financial data for the year to date</span></span>

 

<a name="see-also"></a><span data-ttu-id="411f6-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="411f6-130">See also</span></span>
--------

[<span data-ttu-id="411f6-131">Finanzberichterstellung</span><span class="sxs-lookup"><span data-stu-id="411f6-131">Financial reporting</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="411f6-132">Finanzberichte anzeigen</span><span class="sxs-lookup"><span data-stu-id="411f6-132">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="411f6-133">Dynamics Financial Reporting-Blog</span><span class="sxs-lookup"><span data-stu-id="411f6-133">Dynamics Financial Reporting Blog</span></span>](http://blogs.msdn.com/b/dynamics_financial_reporting/)




