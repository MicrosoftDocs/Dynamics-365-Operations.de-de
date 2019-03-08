---
title: Power BI-Inhalt zu Ist im Vergleich mit Budget
description: In diesem Thema wird der Power BI-Inhalt zu Ist im Vergleich mit Budget beschrieben. Es wird beschrieben, wie auf die Berichte, die im Inhalt enthalten sind, zugegriffen wird und es werden Informationen zum Datenmodell und den Entitäten bereitgestellt, die zum Erstellen des Inhalts verwendet wurden.
author: ryansandness
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetTrackingWorkspace
audience: Application user, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: c801544e9e37a528203f5a1730aa8cb526d63dbf
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "343488"
---
# <a name="actual-vs-budget-power-bi-content"></a><span data-ttu-id="db9f5-104">Power BI-Inhalt zu Ist im Vergleich mit Budget</span><span class="sxs-lookup"><span data-stu-id="db9f5-104">Actual vs budget Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="db9f5-105">In diesem Thema wird der Power BI-Inhalt zu **Ist im Vergleich mit Budget** beschrieben.</span><span class="sxs-lookup"><span data-stu-id="db9f5-105">This topic describes the **Actual vs budget** Microsoft Power BI content.</span></span> <span data-ttu-id="db9f5-106">Es erläutert, wie Sie auf die Power BI-Berichte zugreifen, und enthält Informationen zum Datenmodell und zu den Entitäten, die verwendet wurden, um den Inhalt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="db9f5-106">It explains how to access the Power BI reports, and provides information about the data model and entities that were used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="db9f5-107">Übersicht</span><span class="sxs-lookup"><span data-stu-id="db9f5-107">Overview</span></span>

<span data-ttu-id="db9f5-108">Der Power BI-Inhalt zu **Ist im Vergleich mit Budget** wurde für Personen erstellt, die für die Überwachung der tatsächlichen Leistung im Vergleich zur Budgetleistung in ihrer Organisation verantwortlich sind.</span><span class="sxs-lookup"><span data-stu-id="db9f5-108">The **Actual vs budget** Power BI content was created for individuals who are responsible for monitoring actual versus budget performance in their organization.</span></span> <span data-ttu-id="db9f5-109">Der Power BI-Inhalt zu **Ist im Vergleich mit Budget** bietet Einblicke in Budgetabweichungen.</span><span class="sxs-lookup"><span data-stu-id="db9f5-109">The **Actual vs budget** Power BI content provides visibility into your budget variances.</span></span> <span data-ttu-id="db9f5-110">Sie können Budgets für das aktuelle Jahr nach Firmenkategorie, Budgetcode, Hauptkonto, Hauptkontobeschreibungen oder Finanzzeitraum analysieren, um ein besseres Verständnis für die Ursache von Abweichungen zu bekommen.</span><span class="sxs-lookup"><span data-stu-id="db9f5-110">You can analyze budget for the current year by account category, budget code, main account, main account descriptions, or fiscal period to get a better understanding of the cause of any variances.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="db9f5-111">Zugreifen auf den Power BI-Inhalt</span><span class="sxs-lookup"><span data-stu-id="db9f5-111">Accessing the Power BI content</span></span>
<span data-ttu-id="db9f5-112">Berichte vom Power BI-Inhalt zu **Ist im Vergleich mit Budget** werden in den Arbeitsbereichen **Sachkontobudget und Planungen** und **CFO** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="db9f5-112">Reports from the **Actual vs budget** Power BI content are shown in the **Ledger budget and forecasts** and **CFO** workspaces.</span></span>

## <a name="reports-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="db9f5-113">Berichte, die im Power BI-Inhalt enthalten sind</span><span class="sxs-lookup"><span data-stu-id="db9f5-113">Reports that are included in the Power BI content</span></span>
<span data-ttu-id="db9f5-114">Die folgende Tabelle enthält Details zur Metrik, die sich auf jeder Berichtsseite im Power BI-Inhalt zu **Ist im Vergleich mit Budget** befindet.</span><span class="sxs-lookup"><span data-stu-id="db9f5-114">The following table provides details about the metrics that are found on each report page in the **Actual vs budget** Power BI content.</span></span>

| <span data-ttu-id="db9f5-115">Bericht</span><span class="sxs-lookup"><span data-stu-id="db9f5-115">Report</span></span>                      | <span data-ttu-id="db9f5-116">Metriken</span><span class="sxs-lookup"><span data-stu-id="db9f5-116">Metrics</span></span>                                                                             |
|-----------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="db9f5-117">Ausgaben – Istwert verglichen mit Budget</span><span class="sxs-lookup"><span data-stu-id="db9f5-117">Expenses - Actual vs budget</span></span> | <ul><li><span data-ttu-id="db9f5-118">Diesjährige Gesamtausgaben</span><span class="sxs-lookup"><span data-stu-id="db9f5-118">Total expenses this year</span></span></li><li><span data-ttu-id="db9f5-119">Diesjährige Budgetgesamtausgaben</span><span class="sxs-lookup"><span data-stu-id="db9f5-119">Budget total expenses this year</span></span></li></ul>  |
| <span data-ttu-id="db9f5-120">Umsatzerlös – Istwert im Vergleich zu Budget</span><span class="sxs-lookup"><span data-stu-id="db9f5-120">Revenue - Actual vs budget</span></span>  | <ul><li><span data-ttu-id="db9f5-121">Diesjähriger Gesamtumsatz</span><span class="sxs-lookup"><span data-stu-id="db9f5-121">Total revenue this year</span></span></li><li><span data-ttu-id="db9f5-122">Diesjähriger Budgetgesamtumsatz</span><span class="sxs-lookup"><span data-stu-id="db9f5-122">Budget total revenue this year</span></span></li><ul>     |
| <span data-ttu-id="db9f5-123">Spesen</span><span class="sxs-lookup"><span data-stu-id="db9f5-123">Expense</span></span>                     | <ul><li><span data-ttu-id="db9f5-124">Diesjährige Gesamtausgaben</span><span class="sxs-lookup"><span data-stu-id="db9f5-124">Total expenses this year</span></span></li><li><span data-ttu-id="db9f5-125">Ziel der Ausgaben basierend auf Budget</span><span class="sxs-lookup"><span data-stu-id="db9f5-125">Goal for expenses based on budget</span></span></li><ul> |
| <span data-ttu-id="db9f5-126">Umsatzerlös</span><span class="sxs-lookup"><span data-stu-id="db9f5-126">Revenue</span></span>                     | <ul><li><span data-ttu-id="db9f5-127">Diesjähriger Gesamtumsatz</span><span class="sxs-lookup"><span data-stu-id="db9f5-127">Total revenue this year</span></span></li><li><span data-ttu-id="db9f5-128">Ziel der Umsatzerlöse basierend auf Budget</span><span class="sxs-lookup"><span data-stu-id="db9f5-128">Goal for revenue based on budget</span></span></li><ul>   |
| <span data-ttu-id="db9f5-129">Nettoeinkommen</span><span class="sxs-lookup"><span data-stu-id="db9f5-129">Net income</span></span>                  | <ul><li><span data-ttu-id="db9f5-130">Diesjähriges Nettoeinkommen</span><span class="sxs-lookup"><span data-stu-id="db9f5-130">Net income this year</span></span></li><li><span data-ttu-id="db9f5-131">Ziel des Nettoeinkommens basierend auf Budget</span><span class="sxs-lookup"><span data-stu-id="db9f5-131">Goal for net income based on budget</span></span></li><ul>   |

## <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="db9f5-132">Das Datenmodells und die Entitäten verstehen</span><span class="sxs-lookup"><span data-stu-id="db9f5-132">Understanding the data model and entities</span></span>

| <span data-ttu-id="db9f5-133">Entität</span><span class="sxs-lookup"><span data-stu-id="db9f5-133">Entity</span></span>                    | <span data-ttu-id="db9f5-134">Inhalt</span><span class="sxs-lookup"><span data-stu-id="db9f5-134">Contents</span></span>                                                                         |
|---------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="db9f5-135">Hauptbuchaktivitäten</span><span class="sxs-lookup"><span data-stu-id="db9f5-135">General Ledger Activities</span></span> | <span data-ttu-id="db9f5-136">Buchungsbeträge für das Hauptbuch</span><span class="sxs-lookup"><span data-stu-id="db9f5-136">Transaction amounts for the general ledger</span></span>                                       |
| <span data-ttu-id="db9f5-137">Budgetaktivitäten</span><span class="sxs-lookup"><span data-stu-id="db9f5-137">Budget Activities</span></span>         | <span data-ttu-id="db9f5-138">Buchungsbeträge für das Budgetregister</span><span class="sxs-lookup"><span data-stu-id="db9f5-138">Transaction amounts for the budget register</span></span>                                      |
| <span data-ttu-id="db9f5-139">Hauptkonten</span><span class="sxs-lookup"><span data-stu-id="db9f5-139">Main Accounts</span></span>             | <span data-ttu-id="db9f5-140">Hauptkonten, nach denen Berichte gefiltert werden können</span><span class="sxs-lookup"><span data-stu-id="db9f5-140">Main accounts to filter reports by</span></span>                                               |
| <span data-ttu-id="db9f5-141">Steuerkalender</span><span class="sxs-lookup"><span data-stu-id="db9f5-141">Fiscal Calendars</span></span>          | <span data-ttu-id="db9f5-142">Steuerkalender, nach denen Berichte gefiltert werden können</span><span class="sxs-lookup"><span data-stu-id="db9f5-142">Fiscal calendars to filter reports by</span></span>                                            |
| <span data-ttu-id="db9f5-143">Sachkonten</span><span class="sxs-lookup"><span data-stu-id="db9f5-143">Ledgers</span></span>                   | <span data-ttu-id="db9f5-144">Sachkonten, die verwendet werden können, um den Bericht nach dem aktuellen Sachkonto zu filtern</span><span class="sxs-lookup"><span data-stu-id="db9f5-144">Ledgers that can be used to filter the report to the current ledger</span></span>              |
| <span data-ttu-id="db9f5-145">Budgetcodes</span><span class="sxs-lookup"><span data-stu-id="db9f5-145">Budget Codes</span></span>              | <span data-ttu-id="db9f5-146">Budgetcodes, nach denen Berichte gefiltert werden können</span><span class="sxs-lookup"><span data-stu-id="db9f5-146">Budget codes to filter reports by</span></span>                                                |
| <span data-ttu-id="db9f5-147">Juristische Personen</span><span class="sxs-lookup"><span data-stu-id="db9f5-147">Legal Entities</span></span>            | <span data-ttu-id="db9f5-148">Juristische Personen, die verwendet werden können, um nach der aktuellen juristischen Person zu filtern.</span><span class="sxs-lookup"><span data-stu-id="db9f5-148">Legal entities that can be used to filter the report to the current legal entity</span></span> |
