---
title: 'Analytische Berichte in Microsoft Dynamics 365 Talent: Attract nutzen'
description: 'In diesem Thema werden die möglichen analytischen Berichte für Einstellungsprozess-Einblicke in Microsoft Dynamics 365 Talent: Attract beschrieben'
author: fewatson
manager: AnnBe
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: fewatson
ms.search.validFrom: 2019-04-30
ms.dyn365.ops.version: Talent April 2019 update
ms.openlocfilehash: 5a4d160e8c90725d5ea129a76fd48da1c5af7900
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551517"
---
# <a name="use-analytic-reports-in-microsoft-dynamics-365-talent---attract"></a><span data-ttu-id="ba495-103">Analytische Berichte in Microsoft Dynamics 365 Talent: Attract nutzen</span><span class="sxs-lookup"><span data-stu-id="ba495-103">Use analytic reports in Microsoft Dynamics 365 Talent - Attract</span></span>

<span data-ttu-id="ba495-104">Analytische Berichte in Microsoft Dynamics 365 Talent: Attract ermöglichen eine standardmäßige Lösung (OOTB) für die Gewinnen von Einblicken in den Einstellungsprozess.</span><span class="sxs-lookup"><span data-stu-id="ba495-104">Analytic reports in Microsoft Dynamics 365 Talent: Attract provide an out-of-the-box (OOTB) solution for hiring process insights.</span></span> <span data-ttu-id="ba495-105">Verfügbare Funktionen umfassen:</span><span class="sxs-lookup"><span data-stu-id="ba495-105">Availabe features include:</span></span>

- <span data-ttu-id="ba495-106">**Stellen-Analyse** – Klicken Sie auf die Registerkarte **Analyse**  innerhalb einer Stelle, um die Metrik des Bewerbers für die Stelle zu sehen.</span><span class="sxs-lookup"><span data-stu-id="ba495-106">**Job analytics:** Click the **Analytics** tab within a job for metrics on the job's applicants.</span></span>
- <span data-ttu-id="ba495-107">**Analysehub:**  Klicken Sie auf **Analyse** auf der linken Navigation für die aggregierte Metrik innerhalb der Stellen.</span><span class="sxs-lookup"><span data-stu-id="ba495-107">**Analytics hub:** Click **Analytics** on the left navigation for aggregated metrics across jobs.</span></span>
- <span data-ttu-id="ba495-108">**Benutzerspezifische Sicherheit** Der Zugriff auf die Berichte wird durch Attract [Rollen](security-attract.md)  und die Stellenteilnehmerrolle gesteuert.</span><span class="sxs-lookup"><span data-stu-id="ba495-108">**User-specific security:** Access to reports is controlled by Attract [role](security-attract.md) and job participant role.</span></span>
- <span data-ttu-id="ba495-109">**Übergreifende Filterung:** Klicken Sie auf die graphischen Elemente im Bericht, um andere Metriken anzuzeigen, die nach ausgewählten Daten gefiltert werden.</span><span class="sxs-lookup"><span data-stu-id="ba495-109">**Cross-filtering:** Click visuals within a report to view other metrics filtered by selected data.</span></span>

>[!NOTE] 
>- <span data-ttu-id="ba495-110">Diese Funktion befindet sich derzeit in der [Vorschau](access-preview-feature.md).</span><span class="sxs-lookup"><span data-stu-id="ba495-110">This feature is currently in [preview](access-preview-feature.md).</span></span> <span data-ttu-id="ba495-111">Um sie zu testen, müssen Sie das [**Umfassendes Einstellungs-Add-On**](attract-comprehensive-hiring.md) haben.</span><span class="sxs-lookup"><span data-stu-id="ba495-111">To try it, you must have the [**Comprehensive Hiring Add-On**](attract-comprehensive-hiring.md).</span></span>
>- <span data-ttu-id="ba495-112">Alle öffentlichen Vorschauberichte werden in Englisch angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ba495-112">All public preview reports are displayed in English.</span></span>
>- <span data-ttu-id="ba495-113">Berichte werden alle 3 Stunden aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="ba495-113">Reports refresh every 3 hours.</span></span> <span data-ttu-id="ba495-114">Die letzte Aktualisierungszeit  (in der lokalen Zeitzone) befindet sich am oberen Rand des Berichts.</span><span class="sxs-lookup"><span data-stu-id="ba495-114">The last refresh time (in the local timezone) is located at the top of the report.</span></span> <span data-ttu-id="ba495-115">Aktualisierungszeiten sind ungefähre Angaben und basieren auf dem Datenvolumen und der Ressourcenauslastung in Ihrer Region.</span><span class="sxs-lookup"><span data-stu-id="ba495-115">Refresh times are an approximation and vary based on data volume and resource load in your region.</span></span>

## <a name="job-analytics"></a><span data-ttu-id="ba495-116">Stellenanalysen</span><span class="sxs-lookup"><span data-stu-id="ba495-116">Job Analytics</span></span>

<span data-ttu-id="ba495-117">Stellen-Analyse-Berichte  geben eine Momentaufnahme des Einstellungsprozesses für eine Stelle.</span><span class="sxs-lookup"><span data-stu-id="ba495-117">Job Analytics reports are a snapshot of the hiring process for a job.</span></span>  <span data-ttu-id="ba495-118">Entscheidende Metrik enthalten:</span><span class="sxs-lookup"><span data-stu-id="ba495-118">Key metrics include:</span></span>

- <span data-ttu-id="ba495-119">Aktive Bewerber nach Phase</span><span class="sxs-lookup"><span data-stu-id="ba495-119">Active applicants by stage</span></span>
- <span data-ttu-id="ba495-120">Bewerber-Quelle</span><span class="sxs-lookup"><span data-stu-id="ba495-120">Applicant source</span></span>
- <span data-ttu-id="ba495-121">Bewerbertyp (intern versus extern)</span><span class="sxs-lookup"><span data-stu-id="ba495-121">Applicant type (internal or external)</span></span>

## <a name="analytics-hub"></a><span data-ttu-id="ba495-122">Analyse-Hub</span><span class="sxs-lookup"><span data-stu-id="ba495-122">Analytics Hub</span></span>

<span data-ttu-id="ba495-123">Analyse-Hub-Berichte erstellen Daten der Stellen, um Trends im Einstellungsprozess darzustellen.</span><span class="sxs-lookup"><span data-stu-id="ba495-123">Analytics Hub reports aggregate data across jobs to surface trends in the hiring process.</span></span> <span data-ttu-id="ba495-124">Attract umfasst zwei OOTB-Berichte: Pipeline-Zusammenfassung und Trichter-Analyse.</span><span class="sxs-lookup"><span data-stu-id="ba495-124">Attract includes two OOTB reports: Pipeline Summary and Funnel Analysis.</span></span>

### <a name="pipeline-summary"></a><span data-ttu-id="ba495-125">Pipeline – Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="ba495-125">Pipeline Summary</span></span>

<span data-ttu-id="ba495-126">Der Pipeline-Zusammenfassungsbericht fasst Daten für offene Stellen zusammen.</span><span class="sxs-lookup"><span data-stu-id="ba495-126">The Pipeline Summary report aggregates data for open jobs.</span></span> <span data-ttu-id="ba495-127">Entscheidende Metrik enthalten:</span><span class="sxs-lookup"><span data-stu-id="ba495-127">Key metrics include:</span></span>

- <span data-ttu-id="ba495-128">Bewerber über alle Stellen nach Phasen</span><span class="sxs-lookup"><span data-stu-id="ba495-128">Applicants across all jobs by stage</span></span>
- <span data-ttu-id="ba495-129">Bewerber-Quelle</span><span class="sxs-lookup"><span data-stu-id="ba495-129">Applicant source</span></span>
- <span data-ttu-id="ba495-130">Offene Stellen nach Funktionsstufe</span><span class="sxs-lookup"><span data-stu-id="ba495-130">Open jobs by seniority level</span></span>

### <a name="funnel-analysis"></a><span data-ttu-id="ba495-131">Trichteranalysen</span><span class="sxs-lookup"><span data-stu-id="ba495-131">Funnel Analysis</span></span>

<span data-ttu-id="ba495-132">Der Trichter-Analysebericht fasst Daten für Stellen zusammen, die als besetzt abgeschlossen wurden.</span><span class="sxs-lookup"><span data-stu-id="ba495-132">The Funnel Analysis report aggregates data for jobs that have been closed as filled.</span></span> <span data-ttu-id="ba495-133">Entscheidende Metrik enthalten:</span><span class="sxs-lookup"><span data-stu-id="ba495-133">Key metrics include:</span></span>

- <span data-ttu-id="ba495-134">Benötigte Zeit für die Besetzung der Stelle</span><span class="sxs-lookup"><span data-stu-id="ba495-134">Time to hire</span></span>
- <span data-ttu-id="ba495-135">Umrechnungsmetrik (mit Maus darüber fahren)</span><span class="sxs-lookup"><span data-stu-id="ba495-135">Conversion metrics (on hover)</span></span>
- <span data-ttu-id="ba495-136">Angebotakzeptanzrate</span><span class="sxs-lookup"><span data-stu-id="ba495-136">Offer acceptance rate</span></span>

<span data-ttu-id="ba495-137">Hinweis: Um die Zeit der Einstellung möglichst genau zu berichten, ist die Nutzung der [Angebotsverwaltung](offer-setup.md) empfohlen, eine Funktion, die Teil es empfohlen, die als Teil des umfassenden Einstellungs-Add-On verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="ba495-137">Note: For the most accurate time to hire reporting, it is recommended that you use [Offer management](offer-setup.md), a feature available as part of the Comprehensive Hiring Add-On.</span></span>

>[!TIP] 
><span data-ttu-id="ba495-138">Probieren Sie, für zusätzliche Informationen mit der Maus über die Grafik zu fahren.</span><span class="sxs-lookup"><span data-stu-id="ba495-138">Try hovering over visuals for additional information.</span></span> <span data-ttu-id="ba495-139">Fahren Sie beispielsweise über **Aktive Bewerber** zeigen die Grafiken die durchschnittlichen Tage in der Phase an.</span><span class="sxs-lookup"><span data-stu-id="ba495-139">For example, hovering over **Active applicants** visuals will display the average days in stage.</span></span> <span data-ttu-id="ba495-140">Durch Analysieren dieser Informationen gewinnt man Einblicke, die zentral sind, um die notwendige Zeit für die Einstellung zu reduzieren und Personalbeschaffer die Möglichkeit zu geben, sich darauf zu konzentrieren, die erforderliche Zeit für jede Phase zu reduzieren.</span><span class="sxs-lookup"><span data-stu-id="ba495-140">Analyzing this information can provide insights critical to reducing time to hire and enable recruiters to focus on ways to reduce the time spent in each stage.</span></span>

## <a name="user-specific-security"></a><span data-ttu-id="ba495-141">Benutzerspezifische Sicherheit</span><span class="sxs-lookup"><span data-stu-id="ba495-141">User-specific security</span></span>

<span data-ttu-id="ba495-142">Attract Berichte stehen für die [Rollen](security-attract.md) Administratoren, nur Lesezgriffe, Personalbeschaffer und zukünftige Vorgesetzte bereit.</span><span class="sxs-lookup"><span data-stu-id="ba495-142">Attract reports are accessible for Admin, Read All, Recruiter, and Hiring Manager [roles](security-attract.md).</span></span> <span data-ttu-id="ba495-143">Nicht zugewiesene Benutzer haben keinen Zugriff auf die Analyse-Berichtsseiten (Stellen-Analyse und Analyse-Hub).</span><span class="sxs-lookup"><span data-stu-id="ba495-143">Unassigned users do not have access to either of the analytic report pages (Job Analytics or Analytics Hub).</span></span>

<span data-ttu-id="ba495-144">Stellen-Analyse Berichte zeigen Daten für die ausgewählte Stelle.</span><span class="sxs-lookup"><span data-stu-id="ba495-144">Job Analytics reports display data for the selected job.</span></span> <span data-ttu-id="ba495-145">Analyse-Hub-Berichte umfassen Daten über alle Stellen, die ein Benutzer anzeigen kann.</span><span class="sxs-lookup"><span data-stu-id="ba495-145">Analytics Hub reports aggregate data across all jobs a user can view.</span></span> <span data-ttu-id="ba495-146">Benutzer, die sowohl "Meine Stellen" und "Alle Stellen" auf der Stellenseite anzeigen können, haben im Analyse-Hub die gleichen Ansichten zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="ba495-146">Users that can view both My jobs and All jobs on the Jobs page have the same views available in the Analytics Hub.</span></span>

## <a name="cross-filter"></a><span data-ttu-id="ba495-147">Übergreifende Filter</span><span class="sxs-lookup"><span data-stu-id="ba495-147">Cross-filter</span></span>

<span data-ttu-id="ba495-148">Eine der tollen Funktionen von Power BI ist die Art, wie alle Grafiken auf einer Berichtsseite untereinander verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="ba495-148">One of the great features of Power BI is the way all visuals on a report page are interconnected.</span></span> <span data-ttu-id="ba495-149">Wenn Sie einen Datenpunkt auf einem der grafischen Elemente auswählen, ändern alle anderen grafischen Elemente auf der Seite, die diese Datenenänderung basierend auf dieser Auswahl enthalten.</span><span class="sxs-lookup"><span data-stu-id="ba495-149">If you select a data point on one of the visuals, all the other visuals on the page that contain that data change, based on that selection.</span></span> <span data-ttu-id="ba495-150">Mehr Informationen und ein Beispiel finden Sie unter [Wie Grafiken mit einem Filter in einem Power BI Bericht miteinander verbunden sind](https://docs.microsoft.com/power-bi/consumer/end-user-interactions)</span><span class="sxs-lookup"><span data-stu-id="ba495-150">Find out more and see an example in [How visuals cross-filter each other in a Power BI report](https://docs.microsoft.com/power-bi/consumer/end-user-interactions).</span></span>

## <a name="export-to-excel"></a><span data-ttu-id="ba495-151">Nach Excel exportieren</span><span class="sxs-lookup"><span data-stu-id="ba495-151">Export to Excel</span></span>

<span data-ttu-id="ba495-152">Um Berichtsdaten in Excel anzuzeigen, können Sie auf das Optionsmenü (drei Punkte) in einer Grafik klicken und **Zugrunde liegende Daten exportieren** auswählen.</span><span class="sxs-lookup"><span data-stu-id="ba495-152">To view report data in Excel, you can click the options menu (three dots) on a visual and select **Export underlying data**.</span></span> <span data-ttu-id="ba495-153">Exportierte Daten werden als gefiltert exportiert und berücksichtigen die Benutzerberechtigungen in Attract.</span><span class="sxs-lookup"><span data-stu-id="ba495-153">Exported data will export as filtered, respecting user permissions in Attract.</span></span> <span data-ttu-id="ba495-154">Weitere Informationen finden Sie unter [Exportieren von Daten aus Visualisierungen](https://docs.microsoft.com/power-bi/visuals/power-bi-visualization-export-data).</span><span class="sxs-lookup"><span data-stu-id="ba495-154">For more information, see [Export data from visualizations](https://docs.microsoft.com/power-bi/visuals/power-bi-visualization-export-data).</span></span>
