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
ms.custom: 12294
ms.assetid: 30820be0-d943-4f8b-8c25-6414ec393b3d
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fab0e9d5e550b1848c3483b3172836e258353ebb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249070"
---
# <a name="income-statement-financial-report"></a><span data-ttu-id="5242c-104">Finanzbericht für die Einkommensaufstellung</span><span class="sxs-lookup"><span data-stu-id="5242c-104">Income statement financial report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5242c-105">In diesem Artikel werden die Standardberichte für Einkommensaufstellung beschrieben.</span><span class="sxs-lookup"><span data-stu-id="5242c-105">This article describes the default report for income statements.</span></span> <span data-ttu-id="5242c-106">Er beschreibt zudem die die Bausteine, die diesen Bericht zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="5242c-106">It also describes the building blocks that are associated with this report.</span></span> 

<a name="default-income-statement-report"></a><span data-ttu-id="5242c-107">Standardbericht für die Einkommensaufstellung</span><span class="sxs-lookup"><span data-stu-id="5242c-107">Default income statement report</span></span>
-------------------------------

| <span data-ttu-id="5242c-108">Standardbericht</span><span class="sxs-lookup"><span data-stu-id="5242c-108">Default report</span></span>             | <span data-ttu-id="5242c-109">Funktionsweise</span><span class="sxs-lookup"><span data-stu-id="5242c-109">What it does</span></span>                                                                                              |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5242c-110">Einkommensaufstellung – Standard</span><span class="sxs-lookup"><span data-stu-id="5242c-110">Income Statement – Default</span></span> | <span data-ttu-id="5242c-111">Enthält eine Ansicht der Rentabilität der Organisation für die aktuelle Periode und seit Jahresbeginn.</span><span class="sxs-lookup"><span data-stu-id="5242c-111">Provides a view of the organization’s profitability for the current period and also for the year to date.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="5242c-112">Bausteine</span><span class="sxs-lookup"><span data-stu-id="5242c-112">Building blocks</span></span>
<span data-ttu-id="5242c-113">Der Finanzbericht für die Einkommensaufstellung verwendet die folgenden Bausteine.</span><span class="sxs-lookup"><span data-stu-id="5242c-113">The income statement financial report uses the following building blocks.</span></span>

| <span data-ttu-id="5242c-114">Standardbericht</span><span class="sxs-lookup"><span data-stu-id="5242c-114">Default report</span></span>             | <span data-ttu-id="5242c-115">Zeilendefinition</span><span class="sxs-lookup"><span data-stu-id="5242c-115">Row definition</span></span>                     | <span data-ttu-id="5242c-116">Spaltendefinition</span><span class="sxs-lookup"><span data-stu-id="5242c-116">Column definition</span></span>          |
|----------------------------|------------------------------------|----------------------------|
| <span data-ttu-id="5242c-117">Einkommensaufstellung - Standard</span><span class="sxs-lookup"><span data-stu-id="5242c-117">Income Statement - Default</span></span> | <span data-ttu-id="5242c-118">Zusammengefasste Einkommensaufstellung - Standard</span><span class="sxs-lookup"><span data-stu-id="5242c-118">Summary Income Statement - Default</span></span> | <span data-ttu-id="5242c-119">Periodisch und seit Jahresbeginn - Standard</span><span class="sxs-lookup"><span data-stu-id="5242c-119">Periodic and YTD - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="5242c-120">Zeilendefinition</span><span class="sxs-lookup"><span data-stu-id="5242c-120">Row definition</span></span>

<span data-ttu-id="5242c-121">Die Zeilendefinition, zusammengefasste Einkommensaufstellung - Standard enthält einen Abschnitt für jeden Teil einer herkömmlichen Einkommensaufstellung.</span><span class="sxs-lookup"><span data-stu-id="5242c-121">The row definition, Summary Income Statement – Default, contains a section for each part of a traditional income statement.</span></span> <span data-ttu-id="5242c-122">Die Hauptkontokategoriedimension wird verwendet, um diese Zeilendefinition aufzubauen.</span><span class="sxs-lookup"><span data-stu-id="5242c-122">The Main Account Category dimension is used to build this row definition.</span></span> <span data-ttu-id="5242c-123">Daher kann jeder Benutzer den Bericht erstellen, ohne Änderungen vorzunehmen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="5242c-123">Therefore, anyone can generate the report without having to make any modifications.</span></span>

### <a name="column-definition"></a><span data-ttu-id="5242c-124">Spaltendefinition</span><span class="sxs-lookup"><span data-stu-id="5242c-124">Column Definition</span></span>

<span data-ttu-id="5242c-125">Die Spaltendefinitionen enthalten verschieden Spaltentypen, um verschiedene Stufen der Genauigkeit und der Finanzdaten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="5242c-125">The column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="5242c-126">**Periodisch und seit Jahresbeginn - Standardspaltentypen:**</span><span class="sxs-lookup"><span data-stu-id="5242c-126">**Periodic and YTD – Default column types:**</span></span>
    -   <span data-ttu-id="5242c-127">**DESC** - Die Beschreibung der Zeilendefinition</span><span class="sxs-lookup"><span data-stu-id="5242c-127">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="5242c-128">**FD** - Finanzdaten für die aktuelle Periode</span><span class="sxs-lookup"><span data-stu-id="5242c-128">**FD** – Financial data for the current period</span></span>
    -   <span data-ttu-id="5242c-129">**FD** - Finanzdaten seit Jahresbeginn</span><span class="sxs-lookup"><span data-stu-id="5242c-129">**FD** – Financial data for the year to date</span></span>



<a name="additional-resources"></a><span data-ttu-id="5242c-130">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5242c-130">Additional resources</span></span>
--------

[<span data-ttu-id="5242c-131">Finanzberichterstellung – Übersicht</span><span class="sxs-lookup"><span data-stu-id="5242c-131">Financial reporting overview</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="5242c-132">Finanzberichte anzeigen</span><span class="sxs-lookup"><span data-stu-id="5242c-132">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="5242c-133">Dynamics Financial Reporting-Blog</span><span class="sxs-lookup"><span data-stu-id="5242c-133">Dynamics Financial Reporting Blog</span></span>](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]