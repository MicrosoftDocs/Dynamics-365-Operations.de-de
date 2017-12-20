---
title: Ist-Wert im Vergleich mit Budget-Power BI-Inhalt
description: "In diesem Thema wird der Ist-Wert im Vergleich mit Budget-Power BI-Inhalt beschrieben. Es wird beschrieben, wie auf die Berichte, die im Inhalt enthalten sind, zugegriffen wird und es werden Informationen zum Datenmodell und den Entitäten bereitgestellt, die zum Erstellen des Inhalts verwendet wurden."
author: ryansandness
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application user, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 6e64337f19600b18320550d91c134949c33af7b0
ms.openlocfilehash: 2a0ad5af4e4d7da09690331dc9d1a51d2e97a664
ms.contentlocale: de-de
ms.lasthandoff: 12/01/2017

---

# <a name="actual-vs-budget-power-bi-content"></a><span data-ttu-id="4a55d-104">Ist-Wert im Vergleich mit Budget-Power BI-Inhalt</span><span class="sxs-lookup"><span data-stu-id="4a55d-104">Actual vs budget Power BI content</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="4a55d-105">In diesem Thema wird der **Istwert verglichen mit Budget**-Inhalt von Microsoft Power BI beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4a55d-105">This topic describes the **Actual vs budget** Microsoft Power BI content.</span></span> <span data-ttu-id="4a55d-106">Es wird erläutert, wie Sie auf die Power Bl-Berichte zugreifen und enthält Informationen zum Datenmodell und zu den Entitäten, die verwendet werden, um den Inhalt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4a55d-106">It explains how to access the Power BI reports, and provides information about the data model and entities that were used to build the content.</span></span> 

# <a name="overview"></a><span data-ttu-id="4a55d-107">Überblick</span><span class="sxs-lookup"><span data-stu-id="4a55d-107">Overview</span></span>

<span data-ttu-id="4a55d-108">Der **Istwert verglichen mit Budget**-Inhalt von Power BI wurde für Personen erstellt, die für die Überwachung der tatsächlichen Leistung im Vergleich zur Budgetleistung in ihrer Organisation verantwortlich sind.</span><span class="sxs-lookup"><span data-stu-id="4a55d-108">The **Actual vs budget** Power BI content was created for individuals who are responsible for monitoring actual versus budget performance in their organization.</span></span> <span data-ttu-id="4a55d-109">Der **Ist-Wert im Vergleich mit Budget**-Inhalt für Power BI bietet Einblicke in Budgetabweichungen.</span><span class="sxs-lookup"><span data-stu-id="4a55d-109">The **Actual vs budget** Power BI content provides visibility into your budget variances.</span></span> <span data-ttu-id="4a55d-110">Sie können Budgets für das aktuelle Jahr nach Firmenkategorie, Budgetcode, Hauptkonto, Hauptkontobeschreibungen oder Finanzzeitraum analysieren, um ein besseres Verständnis für die Ursache von Abweichungen zu bekommen.</span><span class="sxs-lookup"><span data-stu-id="4a55d-110">You can analyze budget for the current year by account category, budget code, main account, main account descriptions, or fiscal period to get a better understanding of the cause of any variances.</span></span> 

# <a name="accessing-the-power-bi-content"></a><span data-ttu-id="4a55d-111">Zugreifen au Power BI Inhalt</span><span class="sxs-lookup"><span data-stu-id="4a55d-111">Accessing the Power BI content</span></span>
<span data-ttu-id="4a55d-112">Berichte vom **Istwert verglichen mit Budget** Power BI-Inhalt werden in **Sachkontobudget und Planungen** in **CFO** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4a55d-112">Reports from the **Actual vs budget** Power BI content are shown in the **Ledger budget and forecasts** and **CFO** workspaces.</span></span>

# <a name="reports-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="4a55d-113">Berichte, die im Power BI Inhalt enthalten sind</span><span class="sxs-lookup"><span data-stu-id="4a55d-113">Reports that are included in the Power BI content</span></span>
<span data-ttu-id="4a55d-114">Die folgende Tabelle enthält Details zur Metrik, die sich auf jeder Berichtsseite im **Ist-Wert im Vergleich mit Budget**-Power BI-Inhalt befindet.</span><span class="sxs-lookup"><span data-stu-id="4a55d-114">The following table provides details about the metrics that are found on each report page in the **Actual vs budget** Power BI content.</span></span>

| <span data-ttu-id="4a55d-115">Bericht</span><span class="sxs-lookup"><span data-stu-id="4a55d-115">Report</span></span>                      | <span data-ttu-id="4a55d-116">Metriken</span><span class="sxs-lookup"><span data-stu-id="4a55d-116">Metrics</span></span> |
|-----------------------------|---------|
| <span data-ttu-id="4a55d-117">Ausgaben – Istwert verglichen mit Budget</span><span class="sxs-lookup"><span data-stu-id="4a55d-117">Expenses - Actual vs budget</span></span> | <ul><li><span data-ttu-id="4a55d-118">Diesjährige Gesamtausgaben</span><span class="sxs-lookup"><span data-stu-id="4a55d-118">Total expenses this year</span></span></li><li><span data-ttu-id="4a55d-119">Diesjährige Budgetgesamtausgaben</span><span class="sxs-lookup"><span data-stu-id="4a55d-119">Budget total expenses this year</span></span></li></ul> |
| <span data-ttu-id="4a55d-120">Umsatzerlös – Istwert im Vergleich zu Budget</span><span class="sxs-lookup"><span data-stu-id="4a55d-120">Revenue - Actual vs budget</span></span>  | <ul><li><span data-ttu-id="4a55d-121">Diesjähriger Gesamtumsatz</span><span class="sxs-lookup"><span data-stu-id="4a55d-121">Total revenue this year</span></span></li><li><span data-ttu-id="4a55d-122">Diesjähriger Budgetgesamtumsatz</span><span class="sxs-lookup"><span data-stu-id="4a55d-122">Budget total revenue this year</span></span></li><ul> |
| <span data-ttu-id="4a55d-123">Spesen</span><span class="sxs-lookup"><span data-stu-id="4a55d-123">Expense</span></span>                     | <ul><li><span data-ttu-id="4a55d-124">Diesjährige Gesamtausgaben</span><span class="sxs-lookup"><span data-stu-id="4a55d-124">Total expenses this year</span></span></li><li><span data-ttu-id="4a55d-125">Ziel der Ausgaben basierend auf Budget</span><span class="sxs-lookup"><span data-stu-id="4a55d-125">Goal for expenses based on budget</span></span> </li><ul> |
| <span data-ttu-id="4a55d-126">Umsatzerlös</span><span class="sxs-lookup"><span data-stu-id="4a55d-126">Revenue</span></span>                     | <ul><li><span data-ttu-id="4a55d-127">Diesjähriger Gesamtumsatz</span><span class="sxs-lookup"><span data-stu-id="4a55d-127">Total revenue this year</span></span></li><li><span data-ttu-id="4a55d-128">Ziel der Umsatzerlöse basierend auf Budget</span><span class="sxs-lookup"><span data-stu-id="4a55d-128">Goal for revenue based on budget</span></span> </li><ul> |
| <span data-ttu-id="4a55d-129">Nettoeinkommen</span><span class="sxs-lookup"><span data-stu-id="4a55d-129">Net income</span></span>                  | <ul><li><span data-ttu-id="4a55d-130">Diesjähriges Nettoeinkommen</span><span class="sxs-lookup"><span data-stu-id="4a55d-130">Net income this year</span></span></li><li><span data-ttu-id="4a55d-131">Ziel des Nettoeinkommens basierend auf Budget</span><span class="sxs-lookup"><span data-stu-id="4a55d-131">Goal for net income based on budget</span></span> </li><ul> |

## <a name="extending-the-power-bi-content"></a><span data-ttu-id="4a55d-132">Erweitern des Power BI-Inhalts</span><span class="sxs-lookup"><span data-stu-id="4a55d-132">Extending the Power BI content</span></span>
<span data-ttu-id="4a55d-133">Wenn Sie die Inhaltspakete verwenden, die in Microsoft Dynamics Lifecycle Services (LCS) verfügbar sind, können Sie großartige Analysen für Person bereitstellen, die sich nicht in Microsoft Dynamics 365 anmelden.</span><span class="sxs-lookup"><span data-stu-id="4a55d-133">By using the content packs that are available in Microsoft Dynamics Lifecycle Services (LCS), you can provide great analytics to people who don't sign in to Microsoft Dynamics 365.</span></span> <span data-ttu-id="4a55d-134">Sie können diese Inhaltspakete so ändern, dass sie andere Berichte oder grafische Elemente umfassen, und die Inhaltspakete dann für die Analyse auf Ihrem Power BI.com-Mandanten veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="4a55d-134">You can modify these content packs so that they include other reports or visuals, and then publish the content packs to your Power BI.com tenant for analysis.</span></span> 

<span data-ttu-id="4a55d-135">Sie können den **Ist-Wert im Vergleich mit Budget**-Power BI-Inhalt in der freigebenen Anlagenbibliothek in LCS finden.</span><span class="sxs-lookup"><span data-stu-id="4a55d-135">You can find the **Actual vs budget** Power BI content in the Shared assets library in LCS.</span></span> <span data-ttu-id="4a55d-136">Weitere Informationen dazu, wie Sie Power BI-Inhalte herunterladen und in Ihrer Organisation implementieren, finden Sie unter [Power BI-Inhalt in LCS von Microsoft und Ihren Partnern](power-bi-content-microsoft-partners.md).</span><span class="sxs-lookup"><span data-stu-id="4a55d-136">For more information about how to download the content and implement it in your organization, see [Power BI content in LCS from Microsoft and your partners](power-bi-content-microsoft-partners.md).</span></span> <span data-ttu-id="4a55d-137">Um eine Vorführung anzusehen, die zeigt, wie der Power BI-Inhalt impementiert wird, zeigen Sie den Office Mix [Power BI-Inhalt von Microsoft und Ihren Partnern in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) an.</span><span class="sxs-lookup"><span data-stu-id="4a55d-137">To watch a demo that shows how to implement the Power BI content, see the [Power BI content from Microsoft and your partners in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) Office Mix.</span></span>

# <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="4a55d-138">Das Datenmodells und die Entitäten verstehen</span><span class="sxs-lookup"><span data-stu-id="4a55d-138">Understanding the data model and entities</span></span>

| <span data-ttu-id="4a55d-139">Entität</span><span class="sxs-lookup"><span data-stu-id="4a55d-139">Entity</span></span>                    | <span data-ttu-id="4a55d-140">Inhalt</span><span class="sxs-lookup"><span data-stu-id="4a55d-140">Contents</span></span> |
|---------------------------|----------|
| <span data-ttu-id="4a55d-141">Hauptbuchaktivitäten</span><span class="sxs-lookup"><span data-stu-id="4a55d-141">General Ledger Activities</span></span> | <span data-ttu-id="4a55d-142">Buchungsbeträge für das Hauptbuch</span><span class="sxs-lookup"><span data-stu-id="4a55d-142">Transaction amounts for the general ledger</span></span> |
| <span data-ttu-id="4a55d-143">Budgetaktivitäten</span><span class="sxs-lookup"><span data-stu-id="4a55d-143">Budget Activities</span></span>         | <span data-ttu-id="4a55d-144">Buchungsbeträge für das Budgetregister</span><span class="sxs-lookup"><span data-stu-id="4a55d-144">Transaction amounts for the budget register</span></span> |
| <span data-ttu-id="4a55d-145">Hauptkonten</span><span class="sxs-lookup"><span data-stu-id="4a55d-145">Main Accounts</span></span>             | <span data-ttu-id="4a55d-146">Hauptkonten, nach denen Berichte gefiltert werden können</span><span class="sxs-lookup"><span data-stu-id="4a55d-146">Main accounts to filter reports by</span></span> |
| <span data-ttu-id="4a55d-147">Steuerkalender</span><span class="sxs-lookup"><span data-stu-id="4a55d-147">Fiscal Calendars</span></span>          | <span data-ttu-id="4a55d-148">Steuerkalender, nach denen Berichte gefiltert werden können</span><span class="sxs-lookup"><span data-stu-id="4a55d-148">Fiscal calendars to filter reports by</span></span> |
| <span data-ttu-id="4a55d-149">Sachkonten</span><span class="sxs-lookup"><span data-stu-id="4a55d-149">Ledgers</span></span>                   | <span data-ttu-id="4a55d-150">Sachkonten, die verwendet werden können, um den Bericht nach dem aktuellen Sachkonto zu filtern</span><span class="sxs-lookup"><span data-stu-id="4a55d-150">Ledgers that can be used to filter the report to the current ledger</span></span> |
| <span data-ttu-id="4a55d-151">Budgetcodes</span><span class="sxs-lookup"><span data-stu-id="4a55d-151">Budget Codes</span></span>              | <span data-ttu-id="4a55d-152">Budgetcodes, nach denen Berichte gefiltert werden können</span><span class="sxs-lookup"><span data-stu-id="4a55d-152">Budget codes to filter reports by</span></span> |
| <span data-ttu-id="4a55d-153">Juristische Personen</span><span class="sxs-lookup"><span data-stu-id="4a55d-153">Legal Entities</span></span>            | <span data-ttu-id="4a55d-154">Juristische Personen, die verwendet werden können, um nach der aktuellen juristischen Person zu filtern.</span><span class="sxs-lookup"><span data-stu-id="4a55d-154">Legal entities that can be used to filter the report to the current legal entity</span></span> |

