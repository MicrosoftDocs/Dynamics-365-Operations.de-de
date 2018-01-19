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
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 12294
ms.assetid: 30820be0-d943-4f8b-8c25-6414ec393b3d
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: 7626928bdb8c44036a8f995ccf6d5fd5c684438d
ms.contentlocale: de-de
ms.lasthandoff: 01/19/2018

---

# <a name="income-statement-financial-report"></a><span data-ttu-id="0c53e-104">Finanzbericht für die Einkommensaufstellung</span><span class="sxs-lookup"><span data-stu-id="0c53e-104">Income statement financial report</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="0c53e-105">In diesem Artikel werden die Standardberichte für Einkommensaufstellung beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0c53e-105">This article describes the default report for income statements.</span></span> <span data-ttu-id="0c53e-106">Er beschreibt zudem die die Bausteine, die diesen Bericht zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="0c53e-106">It also describes the building blocks that are associated with this report.</span></span> 

<a name="default-income-statement-report"></a><span data-ttu-id="0c53e-107">Standardbericht für die Einkommensaufstellung</span><span class="sxs-lookup"><span data-stu-id="0c53e-107">Default income statement report</span></span>
-------------------------------

| <span data-ttu-id="0c53e-108">Standardbericht</span><span class="sxs-lookup"><span data-stu-id="0c53e-108">Default report</span></span>             | <span data-ttu-id="0c53e-109">Funktionsweise</span><span class="sxs-lookup"><span data-stu-id="0c53e-109">What it does</span></span>                                                                                              |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c53e-110">Einkommensaufstellung – Standard</span><span class="sxs-lookup"><span data-stu-id="0c53e-110">Income Statement – Default</span></span> | <span data-ttu-id="0c53e-111">Enthält eine Ansicht der Rentabilität der Organisation für die aktuelle Periode und seit Jahresbeginn.</span><span class="sxs-lookup"><span data-stu-id="0c53e-111">Provides a view of the organization’s profitability for the current period and also for the year to date.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="0c53e-112">Bausteine</span><span class="sxs-lookup"><span data-stu-id="0c53e-112">Building blocks</span></span>
<span data-ttu-id="0c53e-113">Der Finanzbericht für die Einkommensaufstellung verwendet die folgenden Bausteine.</span><span class="sxs-lookup"><span data-stu-id="0c53e-113">The income statement financial report uses the following building blocks.</span></span>

| <span data-ttu-id="0c53e-114">Standardbericht</span><span class="sxs-lookup"><span data-stu-id="0c53e-114">Default report</span></span>             | <span data-ttu-id="0c53e-115">Zeilendefinition</span><span class="sxs-lookup"><span data-stu-id="0c53e-115">Row definition</span></span>                     | <span data-ttu-id="0c53e-116">Spaltendefinition</span><span class="sxs-lookup"><span data-stu-id="0c53e-116">Column definition</span></span>          |
|----------------------------|------------------------------------|----------------------------|
| <span data-ttu-id="0c53e-117">Einkommensaufstellung - Standard</span><span class="sxs-lookup"><span data-stu-id="0c53e-117">Income Statement - Default</span></span> | <span data-ttu-id="0c53e-118">Zusammengefasste Einkommensaufstellung - Standard</span><span class="sxs-lookup"><span data-stu-id="0c53e-118">Summary Income Statement - Default</span></span> | <span data-ttu-id="0c53e-119">Periodisch und seit Jahresbeginn - Standard</span><span class="sxs-lookup"><span data-stu-id="0c53e-119">Periodic and YTD - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="0c53e-120">Zeilendefinition</span><span class="sxs-lookup"><span data-stu-id="0c53e-120">Row definition</span></span>

<span data-ttu-id="0c53e-121">Die Zeilendefinition, zusammengefasste Einkommensaufstellung - Standard enthält einen Abschnitt für jeden Teil einer herkömmlichen Einkommensaufstellung.</span><span class="sxs-lookup"><span data-stu-id="0c53e-121">The row definition, Summary Income Statement – Default, contains a section for each part of a traditional income statement.</span></span> <span data-ttu-id="0c53e-122">Die Hauptkontokategoriedimension wird verwendet, um diese Zeilendefinition aufzubauen.</span><span class="sxs-lookup"><span data-stu-id="0c53e-122">The Main Account Category dimension is used to build this row definition.</span></span> <span data-ttu-id="0c53e-123">Daher kann jeder Benutzer den Bericht erstellen, ohne Änderungen vorzunehmen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="0c53e-123">Therefore, anyone can generate the report without having to make any modifications.</span></span>

### <a name="column-definition"></a><span data-ttu-id="0c53e-124">Spaltendefinition</span><span class="sxs-lookup"><span data-stu-id="0c53e-124">Column Definition</span></span>

<span data-ttu-id="0c53e-125">Die Spaltendefinitionen enthalten verschieden Spaltentypen, um verschiedene Stufen der Genauigkeit und der Finanzdaten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="0c53e-125">The column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="0c53e-126">**Periodisch und seit Jahresbeginn - Standardspaltentypen:**</span><span class="sxs-lookup"><span data-stu-id="0c53e-126">**Periodic and YTD – Default column types:**</span></span>
    -   <span data-ttu-id="0c53e-127">**DESC** - Die Beschreibung der Zeilendefinition</span><span class="sxs-lookup"><span data-stu-id="0c53e-127">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="0c53e-128">**FD** - Finanzdaten für die aktuelle Periode</span><span class="sxs-lookup"><span data-stu-id="0c53e-128">**FD** – Financial data for the current period</span></span>
    -   <span data-ttu-id="0c53e-129">**FD** - Finanzdaten seit Jahresbeginn</span><span class="sxs-lookup"><span data-stu-id="0c53e-129">**FD** – Financial data for the year to date</span></span>

 

<a name="see-also"></a><span data-ttu-id="0c53e-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0c53e-130">See also</span></span>
--------

[<span data-ttu-id="0c53e-131">Finanzberichterstellung</span><span class="sxs-lookup"><span data-stu-id="0c53e-131">Financial reporting</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="0c53e-132">Finanzberichte anzeigen</span><span class="sxs-lookup"><span data-stu-id="0c53e-132">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="0c53e-133">Dynamics Financial Reporting-Blog</span><span class="sxs-lookup"><span data-stu-id="0c53e-133">Dynamics Financial Reporting Blog</span></span>](http://blogs.msdn.com/b/dynamics_financial_reporting/)




