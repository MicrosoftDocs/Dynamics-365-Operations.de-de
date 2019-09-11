---
title: Anlagenfehleranalyse
description: In diesem Thema wird die Anlagenfehleranalyse in Asset Management erläutert.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7c9330cc7b3a8839d94c8945418548033254786b
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918440"
---
# <a name="asset-fault-analysis"></a><span data-ttu-id="94799-103">Anlagenfehleranalyse</span><span class="sxs-lookup"><span data-stu-id="94799-103">Asset fault analysis</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="94799-104">In Asset Management können Sie Anlagenfehlererfassungen analysieren, um eine Übersicht über die Gesamtzahl der Fehler zu erhalten, die für einen bestimmten Zeitraum erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="94799-104">In Asset Management, you can analyze asset fault registrations to get an overview of the total number of faults registered during a specific period.</span></span> <span data-ttu-id="94799-105">Fehlererfassungen können aus verschiedenen Perspektiven analysiert werden, beispielsweise mit dem Fokus auf Anlagen, Anlagentypen, funktionalen Standorten, Fehlersymptomen oder Fehlerarten.</span><span class="sxs-lookup"><span data-stu-id="94799-105">Fault registrations can be analyzed from different perspectives, for example with focus on assets, asset types, functional locations, fault symptoms, or fault types.</span></span>

1. <span data-ttu-id="94799-106">Klicken Sie auf **Anlagenverwaltung** > **Abfragen** > **Anlagenfehler** > **Anlagenfehleranalyse**.</span><span class="sxs-lookup"><span data-stu-id="94799-106">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset fault analysis**.</span></span>

2. <span data-ttu-id="94799-107">Im Dialogfeld **Anlagenfehleranalyseberechnung** können Sie das Feld **Ebene** verwenden, um anzugeben, wie detailliert die Anlagenfehlerpositionen in Bezug auf funktionale Standorte sein soll.</span><span class="sxs-lookup"><span data-stu-id="94799-107">In the **Asset fault analysis calculation** dialog, you can use the **Level** field to indicate how detailed you want the asset fault lines to be regarding functional locations.</span></span> <span data-ttu-id="94799-108">Wenn Sie beispielsweise die Zahl „1“ im Feld einfügen und eine funktionale Standortstruktur auf mehreren Ebenen haben, werden alle Anlagenfehlerpositionen für einen funktionalen Standort auf der höchsten Ebene angezeigt, und daher werden die Stunden in einer Position von den funktionalen Standorten auf einer niedrigeren Ebene hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="94799-108">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all asset fault lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="94799-109">Wenn Sie die Zahl „0“ im Feld **Ebene** eingeben, wird ein detailliertes Ergebnis mit allen Anlagenfehlerpositionen für alle funktionalen Standortebenen angezeigt, denen sie zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="94799-109">If you insert the number "0" in the **Level** field, you will see a detailed result showing all asset fault lines on all the functional location level to which they are related.</span></span>

3. <span data-ttu-id="94799-110">Wenn Sie die Suche begrenzen möchten, können Sie bestimmte Anlagen, Fehlerdaten, Fehlerursachen und Fehlerlösungen auf dem Inforegister **Einzuschließende Datensätze** auswählen.</span><span class="sxs-lookup"><span data-stu-id="94799-110">If you want to limit the search, you can select specific assets, fault dates, fault causes, and fault remedies on the **Records to include** FastTab.</span></span>

4. <span data-ttu-id="94799-111">Klicken Sie auf **OK**, um die Berechnung zu starten.</span><span class="sxs-lookup"><span data-stu-id="94799-111">Click **OK** to start the calculation.</span></span>

5. <span data-ttu-id="94799-112">Klicken Sie auf der Registerkarte **Anlagenfehleranalyse** auf eine oder mehrere Schaltflächen in den Aktivitätsbereichsgruppen **Gruppieren nach…**, um die Detailebene anzuzeigen, die Sie anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="94799-112">On the **Asset fault analysis** tab, click one or more buttons in the **Group by...** action pane groups to display the detail level you want to see.</span></span> <span data-ttu-id="94799-113">Aktivierte Schaltflächen werden hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="94799-113">Activated buttons are highlighted.</span></span> <span data-ttu-id="94799-114">Aktivieren oder deaktivieren Sie Schaltflächen, indem Sie sie auf klicken.</span><span class="sxs-lookup"><span data-stu-id="94799-114">Activate or deactivate buttons by clicking on them.</span></span>

6. <span data-ttu-id="94799-115">Klicken Sie auf **Berechnungen aktualisieren**, um die Auswahl auf dem Bildschirm anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="94799-115">Click **Update calculations** to show your selections on the screen.</span></span> 

>[!NOTE]
><span data-ttu-id="94799-116">Denken Sie bei jedem Aktivieren oder Deaktivieren der Schaltflächen in den Aktivitätsbereichsgruppen **Gruppieren nach…** daran, auf die Schaltfläche **Berechnungen aktualisieren** zu klicken, wenn Sie die Auswahl ändern.</span><span class="sxs-lookup"><span data-stu-id="94799-116">Every time you activate or deactivate buttons in the **Group by...** action pane groups, remember to click the **Update calculations** button after you changed the selections.</span></span> <span data-ttu-id="94799-117">Dies ist erforderlich, da eine große Datenmenge verarbeitet wird, während Sie die Fehlerwahrscheinlichkeit neu berechnen.</span><span class="sxs-lookup"><span data-stu-id="94799-117">This is required because a large amount of data is processed as you are recalculating fault probability.</span></span>

<span data-ttu-id="94799-118">Es gibt mehrere Möglichkeiten, Fehlererfassungen zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="94799-118">There are many ways to analyze fault registrations.</span></span> <span data-ttu-id="94799-119">Unten finden Sie in fünf Screenshots Beispiele dazu, wie verschiedene Datenauswahlen verschiedene Informationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="94799-119">Below you see examples in five screenshots of how different data selections provide different pieces of information.</span></span> <span data-ttu-id="94799-120">Sie sehen, wie verschiedene Auswahlen mehr Einblick und Details bieten, wenn Anlagenfehlererfassungen analysiert werden.</span><span class="sxs-lookup"><span data-stu-id="94799-120">You will see how different selections provide more insight and detail when analyzing asset fault registrations.</span></span>

<span data-ttu-id="94799-121">Im Screenshot unten ist nur die Schaltfläche **Symptom** aktiviert.</span><span class="sxs-lookup"><span data-stu-id="94799-121">In the screenshot below, only the **Symptom** button is selected.</span></span>

- <span data-ttu-id="94799-122">Fehlererfassungen sind für drei Fehlersymptome erfolgt: „Luftdurchlässigkeit“, „durchgebrannte Sicherung“ und „Gerät gestört“.</span><span class="sxs-lookup"><span data-stu-id="94799-122">Fault registrations have been made on three fault symptoms: "Air leak", "Blown fuse", and "Equipment jammed".</span></span>  
- <span data-ttu-id="94799-123">In der Spalte **Wahrscheinlichkeit %** summieren sich alle Prozentsätze auf 100 %.</span><span class="sxs-lookup"><span data-stu-id="94799-123">In the **Probability %** column, all percentages add up to 100%.</span></span> <span data-ttu-id="94799-124">Die Wahrscheinlichkeit basiert auf allen **Symptom**-Erfassungen in dieser Fehleranalyse.</span><span class="sxs-lookup"><span data-stu-id="94799-124">Probability is based on all **Symptom** registrations in this fault analysis.</span></span>

![Abbildung 1](media/06-controlling-and-reporting.png)


<span data-ttu-id="94799-126">Im Screenshot unten wurden **Jahr** und **Monat** hinzugefügt, um anzuzeigen, wie Sie Fehlererfassungen für eine ausgewählte Periode anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="94799-126">In the screenshot below, **Year** and **Month** are added to show how you can view fault registrations during a selected period.</span></span>

- <span data-ttu-id="94799-127">Die Fehlersymptome werden nun als Erfassungen pro Monat/Jahr angezeigt.</span><span class="sxs-lookup"><span data-stu-id="94799-127">The fault symptoms are now shown as registrations per year/month.</span></span>  
- <span data-ttu-id="94799-128">In der Spalte **Wahrscheinlichkeit %** ergeben alle Sie Prozentsätze für jeden Monat 100 %, wenn Sie addiert werden.</span><span class="sxs-lookup"><span data-stu-id="94799-128">In the **Probability %** column, if you add all percentages for each month, they add up to 100%.</span></span> <span data-ttu-id="94799-129">Die Wahrscheinlichkeit basiert auf den **Symptom**-Erfassungen in dieser Fehleranalyse.</span><span class="sxs-lookup"><span data-stu-id="94799-129">Probability is based on the **Symptom** registrations in this fault analysis.</span></span> <span data-ttu-id="94799-130">Wenn Sie viele Positionen in einer Anlage haben, aber eine Position einen sehr hohen Prozentsatz aufweist, ist dies ein Hinweis darauf, dass ein Fehlersymptom sorgfältiger untersucht werden sollte, um die Anzahl von Erfassungen für dieses Fehlersymptom einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="94799-130">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault symptom to examine more closely to find a way to limit the number of registrations for that fault symptom.</span></span>

![Abbildung 2](media/07-controlling-and-reporting.png)


- <span data-ttu-id="94799-132">Die Kombination von Anlagen und Anlagentyp wird als Grundlage für die Berechnung verwendet, die in den drei Screenshots unten angezeigt werden, was die Detailebene erhöht.</span><span class="sxs-lookup"><span data-stu-id="94799-132">The combination of assets and an asset type is used as a basis for the calculations shown in the three screenshots below, which will increase in detail level.</span></span>  
- <span data-ttu-id="94799-133">Im Allgemeinen enthalten die Schaltflächen in den Aktivitätsbereichsgruppen **Nach Datum gruppieren**, **Nach Anlage gruppieren**, **Nach funktionalem Standort gruppieren** sowie die Schaltfläche **Fehler** (Fehlerkennung) Perioden oder Anlagenbeziehungen.</span><span class="sxs-lookup"><span data-stu-id="94799-133">Generally, the buttons in the **Group by date**, **Group by asset**, **Group by functional location** action pane groups, as well as the **Fault** button (Fault ID), contain periods or asset relations.</span></span> <span data-ttu-id="94799-134">Die Schaltflächen **Symptom**, **Bereich**, **Typ**, **Ursache** und **Behebung** sind die , die in der Fehlerverwaltung verwendet werden, um Anlagenfehlererfassungen zu analysieren und Problembereiche zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="94799-134">The **Symptom**, **Area**, **Type**, **Cause**, and **Remedy** buttons are categorizations used in fault management to analyze asset fault registrations and pinpoint problem areas.</span></span>  

<span data-ttu-id="94799-135">Im Screenshot unten wurden **Anlage** und **Anlagentyp** hinzugefügt, um weitere Informationen zu Fehlererfassungen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="94799-135">In the screenshot below, **Asset** and **Asset type** were added to provide more detail regarding fault registrations.</span></span>

- <span data-ttu-id="94799-136">Die Fehlersymptome werden jetzt in Kombinationen **Anlage** / **Anlagentyp** / **Symptom** eingeteilt.</span><span class="sxs-lookup"><span data-stu-id="94799-136">The fault symptoms are now split up in **Asset** / **Asset type** / **Symptom** combinations.</span></span>  
- <span data-ttu-id="94799-137">Wenn Sie in der Spalte **Wahrscheinlichkeit %** alle Prozentsätze für die Kombination **Anlage** / **Anlagetyp** / **Symptom** jeweils addieren, ergeben sie jeweils 100 %.</span><span class="sxs-lookup"><span data-stu-id="94799-137">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** respectively, they each add up to 100%.</span></span> <span data-ttu-id="94799-138">Die Wahrscheinlichkeit basiert auf den **Symptom**-Erfassungen in dieser Fehleranalyse.</span><span class="sxs-lookup"><span data-stu-id="94799-138">Probability is based on **Symptom** registrations in this fault analysis.</span></span> <span data-ttu-id="94799-139">Wenn Sie viele Positionen in einer Anlage haben, aber eine Position einen sehr hohen Prozentsatz aufweist, ist dies ein Hinweis darauf, dass ein Fehlersymptom sorgfältiger untersucht werden sollte, um die Anzahl von Erfassungen für dieses Fehlersymptom einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="94799-139">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault symptom to examine more closely to find a way to limit the number of registrations for that fault symptom.</span></span>

![Abbildung 3](media/08-controlling-and-reporting.png)


<span data-ttu-id="94799-141">Im Screenshot unten wurden **Bereich** zu **Symptom**, **Anlage** und **Anlagentyp** hinzugefügt, um weitere Informationen zu Fehlererfassungen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="94799-141">In the screenshot below, **Area** was added to **Symptom**, **Asset**, and **Asset type** to provide more detail regarding fault registrations.</span></span>

- <span data-ttu-id="94799-142">Wenn Sie in der Spalte **Wahrscheinlichkeit %** alle Prozentsätze für die Kombination **Anlage** / **Anlagetyp** / **Symptom** für eine Anlage addieren, ergeben sie jeweils 100 %.</span><span class="sxs-lookup"><span data-stu-id="94799-142">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** on an asset, they each add up to 100%.</span></span> <span data-ttu-id="94799-143">Die Wahrscheinlichkeit basiert auf der Kombination aus **Symptom** und **Bereich** in dieser Fehleranalyse.</span><span class="sxs-lookup"><span data-stu-id="94799-143">Probability is based on the combination of **Symptom** and **Area** in this fault analysis.</span></span> <span data-ttu-id="94799-144">Wenn Sie viele Positionen in einer Anlage haben, aber eine Position einen sehr hohen Prozentsatz aufweist, ist dies ein Hinweis darauf, dass ein Fehlerbereich sorgfältiger untersucht werden sollte, um die Anzahl von Erfassungen für diesen Fehlerbereich einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="94799-144">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault area to examine more closely to find a way to limit the number of registrations for that fault area.</span></span>  

![Abbildung 4](media/09-controlling-and-reporting.png)


<span data-ttu-id="94799-146">Im Screenshot unten wurde **Typ** hinzugefügt, und in diesem Beispiel wird die detaillierteste Berechnung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="94799-146">In the screenshot below, **Type** was added, and the most detailed calculation in this example is shown.</span></span>
 
- <span data-ttu-id="94799-147">Wenn Sie in der Spalte **Wahrscheinlichkeit %** alle Prozentsätze für die Kombination **Anlage** / **Anlagetyp** / **Symptom** für eine Anlage addieren, ergeben sie jeweils 100 %.</span><span class="sxs-lookup"><span data-stu-id="94799-147">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** on an asset, they each add up to 100%.</span></span> <span data-ttu-id="94799-148">Die Wahrscheinlichkeit basiert auf der Kombination aus **Symptom**, **Bereich** und **Typ** in dieser Fehleranalyse.</span><span class="sxs-lookup"><span data-stu-id="94799-148">Probability is based on the combination of **Symptom**, **Area**, and **Type** in this fault analysis.</span></span> <span data-ttu-id="94799-149">Wenn Sie viele Positionen in einer Anlage haben, aber eine Position einen sehr hohen Prozentsatz aufweist, ist dies ein Hinweis darauf, dass ein Fehlertyp sorgfältiger untersucht werden sollte, um die Anzahl von Erfassungen für diesen Fehlertyp einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="94799-149">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault type to examine more closely to find a way to limit the number of registrations on that fault type.</span></span>

![Abbildung 5](media/10-controlling-and-reporting.png)


>[!NOTE]
><span data-ttu-id="94799-151">Einen Überblick über alle erstellten Fehlererfassungen für Arbeitsaufträgen und Wartungsanfragen erhalten Sie, indem Sie auf **Anlagenverwaltung** > **Abfragen** > **Anlagenfehler** > **Anlagenfehler** klicken.</span><span class="sxs-lookup"><span data-stu-id="94799-151">For an overview of all fault registrations created on work orders and maintenance requests, click **Asset management** > **Inquiries** > **Asset fault** > **Asset faults**.</span></span> <span data-ttu-id="94799-152">Wählen Sie auf der Seite **Anlagenfehler** eine Anlagenfehlererfassung aus, und erweitern Sie den Bereich **Zugehörige Informationen**, um Informationen zum zugehörigen Arbeitsauftrag oder zur zugehörigen Wartungsanforderung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="94799-152">On the **Asset faults** page, select an asset fault registration and expand the **Related information** pane to see information regarding the related work order or maintenance request.</span></span>
