---
title: Finanzbericht für die Einkommensaufstellung
description: In diesem Artikel werden die Standardberichte für Einkommensaufstellung beschrieben. Er beschreibt zudem die die Bausteine, die diesen Bericht zugeordnet werden.
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 12294
ms.assetid: 30820be0-d943-4f8b-8c25-6414ec393b3d
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6322001ea8ccbd2e06e15dc6bc8c273608de895b
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771775"
---
# <a name="income-statement-financial-report"></a><span data-ttu-id="df2fb-104">Finanzbericht für die Einkommensaufstellung</span><span class="sxs-lookup"><span data-stu-id="df2fb-104">Income statement financial report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="df2fb-105">In diesem Artikel werden die Standardberichte für Einkommensaufstellung beschrieben.</span><span class="sxs-lookup"><span data-stu-id="df2fb-105">This article describes the default report for income statements.</span></span> <span data-ttu-id="df2fb-106">Er beschreibt zudem die die Bausteine, die diesen Bericht zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="df2fb-106">It also describes the building blocks that are associated with this report.</span></span> 

<a name="default-income-statement-report"></a><span data-ttu-id="df2fb-107">Standardbericht für die Einkommensaufstellung</span><span class="sxs-lookup"><span data-stu-id="df2fb-107">Default income statement report</span></span>
-------------------------------

| <span data-ttu-id="df2fb-108">Standardbericht</span><span class="sxs-lookup"><span data-stu-id="df2fb-108">Default report</span></span>             | <span data-ttu-id="df2fb-109">Funktionsweise</span><span class="sxs-lookup"><span data-stu-id="df2fb-109">What it does</span></span>                                                                                              |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df2fb-110">Einkommensaufstellung – Standard</span><span class="sxs-lookup"><span data-stu-id="df2fb-110">Income Statement – Default</span></span> | <span data-ttu-id="df2fb-111">Enthält eine Ansicht der Rentabilität der Organisation für die aktuelle Periode und seit Jahresbeginn.</span><span class="sxs-lookup"><span data-stu-id="df2fb-111">Provides a view of the organization’s profitability for the current period and also for the year to date.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="df2fb-112">Bausteine</span><span class="sxs-lookup"><span data-stu-id="df2fb-112">Building blocks</span></span>
<span data-ttu-id="df2fb-113">Der Finanzbericht für die Einkommensaufstellung verwendet die folgenden Bausteine.</span><span class="sxs-lookup"><span data-stu-id="df2fb-113">The income statement financial report uses the following building blocks.</span></span>

| <span data-ttu-id="df2fb-114">Standardbericht</span><span class="sxs-lookup"><span data-stu-id="df2fb-114">Default report</span></span>             | <span data-ttu-id="df2fb-115">Zeilendefinition</span><span class="sxs-lookup"><span data-stu-id="df2fb-115">Row definition</span></span>                     | <span data-ttu-id="df2fb-116">Spaltendefinition</span><span class="sxs-lookup"><span data-stu-id="df2fb-116">Column definition</span></span>          |
|----------------------------|------------------------------------|----------------------------|
| <span data-ttu-id="df2fb-117">Einkommensaufstellung - Standard</span><span class="sxs-lookup"><span data-stu-id="df2fb-117">Income Statement - Default</span></span> | <span data-ttu-id="df2fb-118">Zusammengefasste Einkommensaufstellung - Standard</span><span class="sxs-lookup"><span data-stu-id="df2fb-118">Summary Income Statement - Default</span></span> | <span data-ttu-id="df2fb-119">Periodisch und seit Jahresbeginn - Standard</span><span class="sxs-lookup"><span data-stu-id="df2fb-119">Periodic and YTD - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="df2fb-120">Zeilendefinition</span><span class="sxs-lookup"><span data-stu-id="df2fb-120">Row definition</span></span>

<span data-ttu-id="df2fb-121">Die Zeilendefinition, zusammengefasste Einkommensaufstellung - Standard enthält einen Abschnitt für jeden Teil einer herkömmlichen Einkommensaufstellung.</span><span class="sxs-lookup"><span data-stu-id="df2fb-121">The row definition, Summary Income Statement – Default, contains a section for each part of a traditional income statement.</span></span> <span data-ttu-id="df2fb-122">Die Hauptkontokategoriedimension wird verwendet, um diese Zeilendefinition aufzubauen.</span><span class="sxs-lookup"><span data-stu-id="df2fb-122">The Main Account Category dimension is used to build this row definition.</span></span> <span data-ttu-id="df2fb-123">Daher kann jeder Benutzer den Bericht erstellen, ohne Änderungen vorzunehmen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="df2fb-123">Therefore, anyone can generate the report without having to make any modifications.</span></span>

### <a name="column-definition"></a><span data-ttu-id="df2fb-124">Spaltendefinition</span><span class="sxs-lookup"><span data-stu-id="df2fb-124">Column Definition</span></span>

<span data-ttu-id="df2fb-125">Die Spaltendefinitionen enthalten verschieden Spaltentypen, um verschiedene Stufen der Genauigkeit und der Finanzdaten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="df2fb-125">The column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="df2fb-126">**Periodisch und seit Jahresbeginn - Standardspaltentypen:**</span><span class="sxs-lookup"><span data-stu-id="df2fb-126">**Periodic and YTD – Default column types:**</span></span>
    -   <span data-ttu-id="df2fb-127">**DESC** - Die Beschreibung der Zeilendefinition</span><span class="sxs-lookup"><span data-stu-id="df2fb-127">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="df2fb-128">**FD** - Finanzdaten für die aktuelle Periode</span><span class="sxs-lookup"><span data-stu-id="df2fb-128">**FD** – Financial data for the current period</span></span>
    -   <span data-ttu-id="df2fb-129">**FD** - Finanzdaten seit Jahresbeginn</span><span class="sxs-lookup"><span data-stu-id="df2fb-129">**FD** – Financial data for the year to date</span></span>



<a name="additional-resources"></a><span data-ttu-id="df2fb-130">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="df2fb-130">Additional resources</span></span>
--------

[<span data-ttu-id="df2fb-131">Finanzberichterstellung – Übersicht</span><span class="sxs-lookup"><span data-stu-id="df2fb-131">Financial reporting overview</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="df2fb-132">Finanzberichte anzeigen</span><span class="sxs-lookup"><span data-stu-id="df2fb-132">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="df2fb-133">Dynamics Financial Reporting-Blog</span><span class="sxs-lookup"><span data-stu-id="df2fb-133">Dynamics Financial Reporting Blog</span></span>](https://blogs.msdn.com/b/dynamics_financial_reporting/)



