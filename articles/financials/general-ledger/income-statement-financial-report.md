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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 9310508082ff710cd040b74519044f5a90c23988
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---

# <a name="income-statement-financial-report"></a><span data-ttu-id="88c75-104">Finanzbericht für die Einkommensaufstellung</span><span class="sxs-lookup"><span data-stu-id="88c75-104">Income statement financial report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="88c75-105">In diesem Artikel werden die Standardberichte für Einkommensaufstellung beschrieben.</span><span class="sxs-lookup"><span data-stu-id="88c75-105">This article describes the default report for income statements.</span></span> <span data-ttu-id="88c75-106">Er beschreibt zudem die die Bausteine, die diesen Bericht zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="88c75-106">It also describes the building blocks that are associated with this report.</span></span> 

<a name="default-income-statement-report"></a><span data-ttu-id="88c75-107">Standardbericht für die Einkommensaufstellung</span><span class="sxs-lookup"><span data-stu-id="88c75-107">Default income statement report</span></span>
-------------------------------

| <span data-ttu-id="88c75-108">Standardbericht</span><span class="sxs-lookup"><span data-stu-id="88c75-108">Default report</span></span>             | <span data-ttu-id="88c75-109">Funktionsweise</span><span class="sxs-lookup"><span data-stu-id="88c75-109">What it does</span></span>                                                                                              |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88c75-110">Einkommensaufstellung – Standard</span><span class="sxs-lookup"><span data-stu-id="88c75-110">Income Statement – Default</span></span> | <span data-ttu-id="88c75-111">Enthält eine Ansicht der Rentabilität der Organisation für die aktuelle Periode und seit Jahresbeginn.</span><span class="sxs-lookup"><span data-stu-id="88c75-111">Provides a view of the organization’s profitability for the current period and also for the year to date.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="88c75-112">Bausteine</span><span class="sxs-lookup"><span data-stu-id="88c75-112">Building blocks</span></span>
<span data-ttu-id="88c75-113">Der Finanzbericht für die Einkommensaufstellung verwendet die folgenden Bausteine.</span><span class="sxs-lookup"><span data-stu-id="88c75-113">The income statement financial report uses the following building blocks.</span></span>

| <span data-ttu-id="88c75-114">Standardbericht</span><span class="sxs-lookup"><span data-stu-id="88c75-114">Default report</span></span>             | <span data-ttu-id="88c75-115">Zeilendefinition</span><span class="sxs-lookup"><span data-stu-id="88c75-115">Row definition</span></span>                     | <span data-ttu-id="88c75-116">Spaltendefinition</span><span class="sxs-lookup"><span data-stu-id="88c75-116">Column definition</span></span>          |
|----------------------------|------------------------------------|----------------------------|
| <span data-ttu-id="88c75-117">Einkommensaufstellung - Standard</span><span class="sxs-lookup"><span data-stu-id="88c75-117">Income Statement - Default</span></span> | <span data-ttu-id="88c75-118">Zusammengefasste Einkommensaufstellung - Standard</span><span class="sxs-lookup"><span data-stu-id="88c75-118">Summary Income Statement - Default</span></span> | <span data-ttu-id="88c75-119">Periodisch und seit Jahresbeginn - Standard</span><span class="sxs-lookup"><span data-stu-id="88c75-119">Periodic and YTD - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="88c75-120">Zeilendefinition</span><span class="sxs-lookup"><span data-stu-id="88c75-120">Row definition</span></span>

<span data-ttu-id="88c75-121">Die Zeilendefinition, zusammengefasste Einkommensaufstellung - Standard enthält einen Abschnitt für jeden Teil einer herkömmlichen Einkommensaufstellung.</span><span class="sxs-lookup"><span data-stu-id="88c75-121">The row definition, Summary Income Statement – Default, contains a section for each part of a traditional income statement.</span></span> <span data-ttu-id="88c75-122">Die Hauptkontokategoriedimension wird verwendet, um diese Zeilendefinition aufzubauen.</span><span class="sxs-lookup"><span data-stu-id="88c75-122">The Main Account Category dimension is used to build this row definition.</span></span> <span data-ttu-id="88c75-123">Daher kann jeder Benutzer den Bericht erstellen, ohne Änderungen vorzunehmen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="88c75-123">Therefore, anyone can generate the report without having to make any modifications.</span></span>

### <a name="column-definition"></a><span data-ttu-id="88c75-124">Spaltendefinition</span><span class="sxs-lookup"><span data-stu-id="88c75-124">Column Definition</span></span>

<span data-ttu-id="88c75-125">Die Spaltendefinitionen enthalten verschieden Spaltentypen, um verschiedene Stufen der Genauigkeit und der Finanzdaten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="88c75-125">The column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="88c75-126">**Periodisch und seit Jahresbeginn - Standardspaltentypen:**</span><span class="sxs-lookup"><span data-stu-id="88c75-126">**Periodic and YTD – Default column types:**</span></span>
    -   <span data-ttu-id="88c75-127">**DESC** - Die Beschreibung der Zeilendefinition</span><span class="sxs-lookup"><span data-stu-id="88c75-127">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="88c75-128">**FD** - Finanzdaten für die aktuelle Periode</span><span class="sxs-lookup"><span data-stu-id="88c75-128">**FD** – Financial data for the current period</span></span>
    -   <span data-ttu-id="88c75-129">**FD** - Finanzdaten seit Jahresbeginn</span><span class="sxs-lookup"><span data-stu-id="88c75-129">**FD** – Financial data for the year to date</span></span>



<a name="additional-resources"></a><span data-ttu-id="88c75-130">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="88c75-130">Additional resources</span></span>
--------

[<span data-ttu-id="88c75-131">Finanzberichterstellung</span><span class="sxs-lookup"><span data-stu-id="88c75-131">Financial reporting</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="88c75-132">Finanzberichte anzeigen</span><span class="sxs-lookup"><span data-stu-id="88c75-132">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="88c75-133">Dynamics Financial Reporting-Blog</span><span class="sxs-lookup"><span data-stu-id="88c75-133">Dynamics Financial Reporting Blog</span></span>](http://blogs.msdn.com/b/dynamics_financial_reporting/)




