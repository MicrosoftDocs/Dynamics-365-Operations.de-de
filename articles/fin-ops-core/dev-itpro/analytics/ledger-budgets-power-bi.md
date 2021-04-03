---
title: Power BI-Inhalt zu Ist im Vergleich mit Budget
description: In diesem Thema wird der Power BI-Inhalt zu Ist im Vergleich mit Budget beschrieben. Es wird erläutert, wie auf Berichte zugegriffen wird, und es werden Informationen zum Datenmodell bereitgestellt.
author: panolte
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetTrackingWorkspace
audience: Application user, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: f3e2f62b666559ba9a356e4948c2033da9cc95d5
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568572"
---
# <a name="actual-vs-budget-power-bi-content"></a><span data-ttu-id="f10f4-104">Power BI-Inhalt zu Ist im Vergleich mit Budget</span><span class="sxs-lookup"><span data-stu-id="f10f4-104">Actual vs budget Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f10f4-105">In diesem Thema wird der Microsoft Power BI-Inhalt **Istwert vs. Budget** beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f10f4-105">This topic describes the **Actual vs budget** Microsoft Power BI content.</span></span> <span data-ttu-id="f10f4-106">Es erläutert, wie Sie auf die Power BI-Berichte zugreifen, und enthält Informationen zum Datenmodell und zu den Entitäten, die verwendet wurden, um den Inhalt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f10f4-106">It explains how to access the Power BI reports, and provides information about the data model and entities that were used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="f10f4-107">Übersicht</span><span class="sxs-lookup"><span data-stu-id="f10f4-107">Overview</span></span>

<span data-ttu-id="f10f4-108">Der Power BI-Inhalt zu **Ist im Vergleich mit Budget** wurde für Personen erstellt, die für die Überwachung der tatsächlichen Leistung im Vergleich zur Budgetleistung in ihrer Organisation verantwortlich sind.</span><span class="sxs-lookup"><span data-stu-id="f10f4-108">The **Actual vs budget** Power BI content was created for individuals who are responsible for monitoring actual versus budget performance in their organization.</span></span> <span data-ttu-id="f10f4-109">Der Power BI-Inhalt zu **Ist im Vergleich mit Budget** bietet Einblicke in Budgetabweichungen.</span><span class="sxs-lookup"><span data-stu-id="f10f4-109">The **Actual vs budget** Power BI content provides visibility into your budget variances.</span></span> <span data-ttu-id="f10f4-110">Sie können Budgets für das aktuelle Jahr nach Firmenkategorie, Budgetcode, Hauptkonto, Hauptkontobeschreibungen oder Finanzzeitraum analysieren, um ein besseres Verständnis für die Ursache von Abweichungen zu bekommen.</span><span class="sxs-lookup"><span data-stu-id="f10f4-110">You can analyze budget for the current year by account category, budget code, main account, main account descriptions, or fiscal period to get a better understanding of the cause of any variances.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="f10f4-111">Zugreifen auf den Power BI-Inhalt</span><span class="sxs-lookup"><span data-stu-id="f10f4-111">Accessing the Power BI content</span></span>
<span data-ttu-id="f10f4-112">Berichte vom Power BI-Inhalt zu **Ist im Vergleich mit Budget** werden in den Arbeitsbereichen **Sachkontobudget und Planungen** und **CFO** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f10f4-112">Reports from the **Actual vs budget** Power BI content are shown in the **Ledger budget and forecasts** and **CFO** workspaces.</span></span>

## <a name="reports-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="f10f4-113">Berichte, die im Power BI-Inhalt enthalten sind</span><span class="sxs-lookup"><span data-stu-id="f10f4-113">Reports that are included in the Power BI content</span></span>
<span data-ttu-id="f10f4-114">Die folgende Tabelle enthält Details zur Metrik, die sich auf jeder Berichtsseite im Power BI-Inhalt zu **Ist im Vergleich mit Budget** befindet.</span><span class="sxs-lookup"><span data-stu-id="f10f4-114">The following table provides details about the metrics that are found on each report page in the **Actual vs budget** Power BI content.</span></span>

| <span data-ttu-id="f10f4-115">Bericht</span><span class="sxs-lookup"><span data-stu-id="f10f4-115">Report</span></span>                      | <span data-ttu-id="f10f4-116">Metriken</span><span class="sxs-lookup"><span data-stu-id="f10f4-116">Metrics</span></span>                                                                             |
|-----------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f10f4-117">Ausgaben – Istwert verglichen mit Budget</span><span class="sxs-lookup"><span data-stu-id="f10f4-117">Expenses - Actual vs budget</span></span> | <ul><li><span data-ttu-id="f10f4-118">Diesjährige Gesamtausgaben</span><span class="sxs-lookup"><span data-stu-id="f10f4-118">Total expenses this year</span></span></li><li><span data-ttu-id="f10f4-119">Diesjährige Budgetgesamtausgaben</span><span class="sxs-lookup"><span data-stu-id="f10f4-119">Budget total expenses this year</span></span></li></ul>  |
| <span data-ttu-id="f10f4-120">Umsatzerlös – Istwert im Vergleich zu Budget</span><span class="sxs-lookup"><span data-stu-id="f10f4-120">Revenue - Actual vs budget</span></span>  | <ul><li><span data-ttu-id="f10f4-121">Diesjähriger Gesamtumsatz</span><span class="sxs-lookup"><span data-stu-id="f10f4-121">Total revenue this year</span></span></li><li><span data-ttu-id="f10f4-122">Diesjähriger Budgetgesamtumsatz</span><span class="sxs-lookup"><span data-stu-id="f10f4-122">Budget total revenue this year</span></span></li><ul>     |
| <span data-ttu-id="f10f4-123">Spesen</span><span class="sxs-lookup"><span data-stu-id="f10f4-123">Expense</span></span>                     | <ul><li><span data-ttu-id="f10f4-124">Diesjährige Gesamtausgaben</span><span class="sxs-lookup"><span data-stu-id="f10f4-124">Total expenses this year</span></span></li><li><span data-ttu-id="f10f4-125">Ziel der Ausgaben basierend auf Budget</span><span class="sxs-lookup"><span data-stu-id="f10f4-125">Goal for expenses based on budget</span></span></li><ul> |
| <span data-ttu-id="f10f4-126">Umsatzerlös</span><span class="sxs-lookup"><span data-stu-id="f10f4-126">Revenue</span></span>                     | <ul><li><span data-ttu-id="f10f4-127">Diesjähriger Gesamtumsatz</span><span class="sxs-lookup"><span data-stu-id="f10f4-127">Total revenue this year</span></span></li><li><span data-ttu-id="f10f4-128">Ziel der Umsatzerlöse basierend auf Budget</span><span class="sxs-lookup"><span data-stu-id="f10f4-128">Goal for revenue based on budget</span></span></li><ul>   |
| <span data-ttu-id="f10f4-129">Nettoeinkommen</span><span class="sxs-lookup"><span data-stu-id="f10f4-129">Net income</span></span>                  | <ul><li><span data-ttu-id="f10f4-130">Diesjähriges Nettoeinkommen</span><span class="sxs-lookup"><span data-stu-id="f10f4-130">Net income this year</span></span></li><li><span data-ttu-id="f10f4-131">Ziel des Nettoeinkommens basierend auf Budget</span><span class="sxs-lookup"><span data-stu-id="f10f4-131">Goal for net income based on budget</span></span></li><ul>   |

## <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="f10f4-132">Das Datenmodells und die Entitäten verstehen</span><span class="sxs-lookup"><span data-stu-id="f10f4-132">Understanding the data model and entities</span></span>

| <span data-ttu-id="f10f4-133">Entität</span><span class="sxs-lookup"><span data-stu-id="f10f4-133">Entity</span></span>                    | <span data-ttu-id="f10f4-134">Inhalt</span><span class="sxs-lookup"><span data-stu-id="f10f4-134">Contents</span></span>                                                                         |
|---------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f10f4-135">Hauptbuchaktivitäten</span><span class="sxs-lookup"><span data-stu-id="f10f4-135">General Ledger Activities</span></span> | <span data-ttu-id="f10f4-136">Buchungsbeträge für das Hauptbuch</span><span class="sxs-lookup"><span data-stu-id="f10f4-136">Transaction amounts for the general ledger</span></span>                                       |
| <span data-ttu-id="f10f4-137">Budgetaktivitäten</span><span class="sxs-lookup"><span data-stu-id="f10f4-137">Budget Activities</span></span>         | <span data-ttu-id="f10f4-138">Buchungsbeträge für das Budgetregister</span><span class="sxs-lookup"><span data-stu-id="f10f4-138">Transaction amounts for the budget register</span></span>                                      |
| <span data-ttu-id="f10f4-139">Hauptkonten</span><span class="sxs-lookup"><span data-stu-id="f10f4-139">Main Accounts</span></span>             | <span data-ttu-id="f10f4-140">Hauptkonten, nach denen Berichte gefiltert werden können</span><span class="sxs-lookup"><span data-stu-id="f10f4-140">Main accounts to filter reports by</span></span>                                               |
| <span data-ttu-id="f10f4-141">Steuerkalender</span><span class="sxs-lookup"><span data-stu-id="f10f4-141">Fiscal Calendars</span></span>          | <span data-ttu-id="f10f4-142">Steuerkalender, nach denen Berichte gefiltert werden können</span><span class="sxs-lookup"><span data-stu-id="f10f4-142">Fiscal calendars to filter reports by</span></span>                                            |
| <span data-ttu-id="f10f4-143">Sachkonten</span><span class="sxs-lookup"><span data-stu-id="f10f4-143">Ledgers</span></span>                   | <span data-ttu-id="f10f4-144">Sachkonten, die verwendet werden können, um den Bericht nach dem aktuellen Sachkonto zu filtern</span><span class="sxs-lookup"><span data-stu-id="f10f4-144">Ledgers that can be used to filter the report to the current ledger</span></span>              |
| <span data-ttu-id="f10f4-145">Budgetcodes</span><span class="sxs-lookup"><span data-stu-id="f10f4-145">Budget Codes</span></span>              | <span data-ttu-id="f10f4-146">Budgetcodes, nach denen Berichte gefiltert werden können</span><span class="sxs-lookup"><span data-stu-id="f10f4-146">Budget codes to filter reports by</span></span>                                                |
| <span data-ttu-id="f10f4-147">Juristische Personen</span><span class="sxs-lookup"><span data-stu-id="f10f4-147">Legal Entities</span></span>            | <span data-ttu-id="f10f4-148">Juristische Personen, die verwendet werden können, um nach der aktuellen juristischen Person zu filtern.</span><span class="sxs-lookup"><span data-stu-id="f10f4-148">Legal entities that can be used to filter the report to the current legal entity</span></span> |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]