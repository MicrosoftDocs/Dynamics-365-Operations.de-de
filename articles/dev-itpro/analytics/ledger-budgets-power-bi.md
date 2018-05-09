---
title: Ist-Wert im Vergleich mit Budget-Power BI-Inhalt
description: "In diesem Thema wird der Ist-Wert im Vergleich mit Budget-Power BI-Inhalt beschrieben. Es wird beschrieben, wie auf die Berichte, die im Inhalt enthalten sind, zugegriffen wird und es werden Informationen zum Datenmodell und den Entitäten bereitgestellt, die zum Erstellen des Inhalts verwendet wurden."
author: ryansandness
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetTrackingWorkspace
audience: Application user, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 6a01d28d642ab3846c18955a1fced0dbabfb85d4
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---

# <a name="actual-vs-budget-power-bi-content"></a><span data-ttu-id="06f66-104">Ist-Wert im Vergleich mit Budget-Power BI-Inhalt</span><span class="sxs-lookup"><span data-stu-id="06f66-104">Actual vs budget Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="06f66-105">In diesem Thema wird der **Istwert verglichen mit Budget**-Inhalt von Microsoft Power BI beschrieben.</span><span class="sxs-lookup"><span data-stu-id="06f66-105">This topic describes the **Actual vs budget** Microsoft Power BI content.</span></span> <span data-ttu-id="06f66-106">Es wird erläutert, wie Sie auf die Power Bl-Berichte zugreifen und enthält Informationen zum Datenmodell und zu den Entitäten, die verwendet werden, um den Inhalt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="06f66-106">It explains how to access the Power BI reports, and provides information about the data model and entities that were used to build the content.</span></span> 

## <a name="overview"></a><span data-ttu-id="06f66-107">Überblick</span><span class="sxs-lookup"><span data-stu-id="06f66-107">Overview</span></span>

<span data-ttu-id="06f66-108">Der **Istwert verglichen mit Budget**-Inhalt von Power BI wurde für Personen erstellt, die für die Überwachung der tatsächlichen Leistung im Vergleich zur Budgetleistung in ihrer Organisation verantwortlich sind.</span><span class="sxs-lookup"><span data-stu-id="06f66-108">The **Actual vs budget** Power BI content was created for individuals who are responsible for monitoring actual versus budget performance in their organization.</span></span> <span data-ttu-id="06f66-109">Der **Ist-Wert im Vergleich mit Budget**-Inhalt für Power BI bietet Einblicke in Budgetabweichungen.</span><span class="sxs-lookup"><span data-stu-id="06f66-109">The **Actual vs budget** Power BI content provides visibility into your budget variances.</span></span> <span data-ttu-id="06f66-110">Sie können Budgets für das aktuelle Jahr nach Firmenkategorie, Budgetcode, Hauptkonto, Hauptkontobeschreibungen oder Finanzzeitraum analysieren, um ein besseres Verständnis für die Ursache von Abweichungen zu bekommen.</span><span class="sxs-lookup"><span data-stu-id="06f66-110">You can analyze budget for the current year by account category, budget code, main account, main account descriptions, or fiscal period to get a better understanding of the cause of any variances.</span></span> 

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="06f66-111">Zugreifen au Power BI Inhalt</span><span class="sxs-lookup"><span data-stu-id="06f66-111">Accessing the Power BI content</span></span>
<span data-ttu-id="06f66-112">Berichte vom **Istwert verglichen mit Budget** Power BI-Inhalt werden in **Sachkontobudget und Planungen** in **CFO** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="06f66-112">Reports from the **Actual vs budget** Power BI content are shown in the **Ledger budget and forecasts** and **CFO** workspaces.</span></span>

## <a name="reports-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="06f66-113">Berichte, die im Power BI Inhalt enthalten sind</span><span class="sxs-lookup"><span data-stu-id="06f66-113">Reports that are included in the Power BI content</span></span>
<span data-ttu-id="06f66-114">Die folgende Tabelle enthält Details zur Metrik, die sich auf jeder Berichtsseite im **Ist-Wert im Vergleich mit Budget**-Power BI-Inhalt befindet.</span><span class="sxs-lookup"><span data-stu-id="06f66-114">The following table provides details about the metrics that are found on each report page in the **Actual vs budget** Power BI content.</span></span>


|           <span data-ttu-id="06f66-115">Bericht</span><span class="sxs-lookup"><span data-stu-id="06f66-115">Report</span></span>            |                                       <span data-ttu-id="06f66-116">Metriken</span><span class="sxs-lookup"><span data-stu-id="06f66-116">Metrics</span></span>                                        |
|-----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="06f66-117">Ausgaben – Istwert verglichen mit Budget</span><span class="sxs-lookup"><span data-stu-id="06f66-117">Expenses - Actual vs budget</span></span> |  <ul><li><span data-ttu-id="06f66-118">Diesjährige Gesamtausgaben</span><span class="sxs-lookup"><span data-stu-id="06f66-118">Total expenses this year</span></span></li><li><span data-ttu-id="06f66-119">Diesjährige Budgetgesamtausgaben</span><span class="sxs-lookup"><span data-stu-id="06f66-119">Budget total expenses this year</span></span></li></ul>  |
| <span data-ttu-id="06f66-120">Umsatzerlös – Istwert im Vergleich zu Budget</span><span class="sxs-lookup"><span data-stu-id="06f66-120">Revenue - Actual vs budget</span></span>  |   <ul><li><span data-ttu-id="06f66-121">Diesjähriger Gesamtumsatz</span><span class="sxs-lookup"><span data-stu-id="06f66-121">Total revenue this year</span></span></li><li><span data-ttu-id="06f66-122">Diesjähriger Budgetgesamtumsatz</span><span class="sxs-lookup"><span data-stu-id="06f66-122">Budget total revenue this year</span></span></li><ul>    |
|           <span data-ttu-id="06f66-123">Spesen</span><span class="sxs-lookup"><span data-stu-id="06f66-123">Expense</span></span>           | <ul><li><span data-ttu-id="06f66-124">Diesjährige Gesamtausgaben</span><span class="sxs-lookup"><span data-stu-id="06f66-124">Total expenses this year</span></span></li><li><span data-ttu-id="06f66-125">Ziel der Ausgaben basierend auf Budget</span><span class="sxs-lookup"><span data-stu-id="06f66-125">Goal for expenses based on budget</span></span> </li><ul> |
|           <span data-ttu-id="06f66-126">Umsatzerlös</span><span class="sxs-lookup"><span data-stu-id="06f66-126">Revenue</span></span>           |  <ul><li><span data-ttu-id="06f66-127">Diesjähriger Gesamtumsatz</span><span class="sxs-lookup"><span data-stu-id="06f66-127">Total revenue this year</span></span></li><li><span data-ttu-id="06f66-128">Ziel der Umsatzerlöse basierend auf Budget</span><span class="sxs-lookup"><span data-stu-id="06f66-128">Goal for revenue based on budget</span></span> </li><ul>  |
|         <span data-ttu-id="06f66-129">Nettoeinkommen</span><span class="sxs-lookup"><span data-stu-id="06f66-129">Net income</span></span>          |  <ul><li><span data-ttu-id="06f66-130">Diesjähriges Nettoeinkommen</span><span class="sxs-lookup"><span data-stu-id="06f66-130">Net income this year</span></span></li><li><span data-ttu-id="06f66-131">Ziel des Nettoeinkommens basierend auf Budget</span><span class="sxs-lookup"><span data-stu-id="06f66-131">Goal for net income based on budget</span></span> </li><ul>  |

## <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="06f66-132">Das Datenmodells und die Entitäten verstehen</span><span class="sxs-lookup"><span data-stu-id="06f66-132">Understanding the data model and entities</span></span>

|          <span data-ttu-id="06f66-133">Entität</span><span class="sxs-lookup"><span data-stu-id="06f66-133">Entity</span></span>           |                                     <span data-ttu-id="06f66-134">Inhalt</span><span class="sxs-lookup"><span data-stu-id="06f66-134">Contents</span></span>                                     |
|---------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="06f66-135">Hauptbuchaktivitäten</span><span class="sxs-lookup"><span data-stu-id="06f66-135">General Ledger Activities</span></span> |                    <span data-ttu-id="06f66-136">Buchungsbeträge für das Hauptbuch</span><span class="sxs-lookup"><span data-stu-id="06f66-136">Transaction amounts for the general ledger</span></span>                    |
|     <span data-ttu-id="06f66-137">Budgetaktivitäten</span><span class="sxs-lookup"><span data-stu-id="06f66-137">Budget Activities</span></span>     |                   <span data-ttu-id="06f66-138">Buchungsbeträge für das Budgetregister</span><span class="sxs-lookup"><span data-stu-id="06f66-138">Transaction amounts for the budget register</span></span>                    |
|       <span data-ttu-id="06f66-139">Hauptkonten</span><span class="sxs-lookup"><span data-stu-id="06f66-139">Main Accounts</span></span>       |                        <span data-ttu-id="06f66-140">Hauptkonten, nach denen Berichte gefiltert werden können</span><span class="sxs-lookup"><span data-stu-id="06f66-140">Main accounts to filter reports by</span></span>                        |
|     <span data-ttu-id="06f66-141">Steuerkalender</span><span class="sxs-lookup"><span data-stu-id="06f66-141">Fiscal Calendars</span></span>      |                      <span data-ttu-id="06f66-142">Steuerkalender, nach denen Berichte gefiltert werden können</span><span class="sxs-lookup"><span data-stu-id="06f66-142">Fiscal calendars to filter reports by</span></span>                       |
|          <span data-ttu-id="06f66-143">Sachkonten</span><span class="sxs-lookup"><span data-stu-id="06f66-143">Ledgers</span></span>          |       <span data-ttu-id="06f66-144">Sachkonten, die verwendet werden können, um den Bericht nach dem aktuellen Sachkonto zu filtern</span><span class="sxs-lookup"><span data-stu-id="06f66-144">Ledgers that can be used to filter the report to the current ledger</span></span>        |
|       <span data-ttu-id="06f66-145">Budgetcodes</span><span class="sxs-lookup"><span data-stu-id="06f66-145">Budget Codes</span></span>        |                        <span data-ttu-id="06f66-146">Budgetcodes, nach denen Berichte gefiltert werden können</span><span class="sxs-lookup"><span data-stu-id="06f66-146">Budget codes to filter reports by</span></span>                         |
|      <span data-ttu-id="06f66-147">Juristische Personen</span><span class="sxs-lookup"><span data-stu-id="06f66-147">Legal Entities</span></span>       | <span data-ttu-id="06f66-148">Juristische Personen, die verwendet werden können, um nach der aktuellen juristischen Person zu filtern.</span><span class="sxs-lookup"><span data-stu-id="06f66-148">Legal entities that can be used to filter the report to the current legal entity</span></span> |


