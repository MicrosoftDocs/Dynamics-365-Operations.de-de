---
title: Manuelle Anpassungen an der Grundplanung
description: In diesem Thema wird beschrieben, wie Sie manuelle Anpassungen an einer Grundplanung vornehmen und Details der Planung anzeigen können.
author: roxanadiaconu
manager: tfehr
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanForecastViewer
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72704
ms.assetid: e7c5d44e-07bc-40b1-a4b3-8ba46483ef9e
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 90d19e9465abc71125931a7946febe2d633c3181
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251960"
---
# <a name="make-manual-adjustments-to-the-baseline-forecast"></a><span data-ttu-id="36597-103">Manuelle Anpassungen an der Grundplanung</span><span class="sxs-lookup"><span data-stu-id="36597-103">Make manual adjustments to the baseline forecast</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="36597-104">In diesem Thema wird beschrieben, wie Sie manuelle Anpassungen an einer Grundplanung vornehmen und Details der Planung anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="36597-104">This topic explains how you can make manual adjustments to a baseline forecast and view details of the forecast.</span></span> 

<span data-ttu-id="36597-105">Bevor Sie manuelle Anpassungen vornehmen, ist es wichtig, dass Sie einige Konzepte für verschiedene Seiten verstehen.</span><span class="sxs-lookup"><span data-stu-id="36597-105">Before you make manual adjustments, it's important that you understand a few concepts on various pages.</span></span>

## <a name="grid-on-the-adjusted-demand-forecast-page"></a><span data-ttu-id="36597-106">Raster auf der Seite "Angepasste Bedarfsplanung“</span><span class="sxs-lookup"><span data-stu-id="36597-106">Grid on the Adjusted demand forecast page</span></span>
<span data-ttu-id="36597-107">Die Seite **Angepasste Bedarfsplanung** umfasst ein Raster, das die folgende Struktur hat:</span><span class="sxs-lookup"><span data-stu-id="36597-107">The **Adjusted demand forecast** page includes a grid that has the following structure:</span></span>

-   <span data-ttu-id="36597-108">Die erste Spalte enthält Artikel, Artikelverteilungsschlüssel, Unternehmen usw., für die die Planung generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="36597-108">The first column shows the items, item allocation keys, companies, and so on, that the forecast has been generated for.</span></span> <span data-ttu-id="36597-109">Der Untertitel der Seite enthält eine Beschreibung der aktuellen Planungsdimensionen, die im Raster angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="36597-109">The subtitle of the page provides a description of the current forecast dimensions that are shown in the grid.</span></span> <span data-ttu-id="36597-110">Wenn beispielsweise der Untertitel der Seite **Unternehmen / Standort / Artikelverteilungsschlüssel** ist und eine der Zeilenbeschriftungen im Raster **USMF / 1 / D\_Alloc** ist, enthält diese Zeile die Planung für das Unternehmen USMF, Standort 1 und den Artikelverteilungsschlüssel **D\_Alloc**.</span><span class="sxs-lookup"><span data-stu-id="36597-110">For example, if the subtitle of the page is **Company / Site / Item allocation key**, and one of the row headers in the grid is **USMF / 1 / D\_Alloc**, that row shows the forecast for the USMF company, site 1, and the **D\_Alloc** item allocation key.</span></span>
-   <span data-ttu-id="36597-111">Nachfolgende Spalten stellen die Planungszeitrahmen dar, für die die Planung für generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="36597-111">Subsequent columns represent the forecast buckets that the forecast has been generated for.</span></span> <span data-ttu-id="36597-112">Jede Spaltenüberschrift ist das erste Datum des Planungszeitrahmens, den die Spalte anzeigt.</span><span class="sxs-lookup"><span data-stu-id="36597-112">Each column header is the first date of the forecast bucket that the column shows.</span></span>
-   <span data-ttu-id="36597-113">Die Werte in den Zellen stellen die Planung für einen Artikel, Artikelverteilungsschlüssel usw. für diesen bestimmten Planungszeitrahmen dar.</span><span class="sxs-lookup"><span data-stu-id="36597-113">The values in the cells represent the forecast for one item, item allocation key, and so on, for that specific forecast bucket.</span></span>

## <a name="forecast-aggregation-and-de-aggregation"></a><span data-ttu-id="36597-114">Planungsaggregation und -disaggregation</span><span class="sxs-lookup"><span data-stu-id="36597-114">Forecast aggregation and de-aggregation</span></span>
<span data-ttu-id="36597-115">Der Untertitel der Seite enthält die Ebene der Planungsaggregation.</span><span class="sxs-lookup"><span data-stu-id="36597-115">The subtitle of the page shows the level of forecast aggregation.</span></span> 

<span data-ttu-id="36597-116">Wenn beispielsweise der Untertitel der Seite **Unternehmen/Standort/Verteilungsschlüssel/Artikelnummer/Farbe/Größe/Konfiguration/Stil** lautet, gibt es keine Planungsaggregation, und die Planung wird auf der Ebene des Artikels und der Dimensionen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="36597-116">For example, if the subtitle of the page is **Company / Site / Allocation key / Item number / Color / Size / Configuration / Style**, there is no forecast aggregation, and the forecast is shown at the level of the item and its dimensions.</span></span> <span data-ttu-id="36597-117">Um die Aggregation zu ändern, verwenden Sie die Seite **Planungsdimensionen ändern**, die Sie über das Anwendungsmenü öffnen können.</span><span class="sxs-lookup"><span data-stu-id="36597-117">To change the aggregation, use the **Change forecast dimensions** page, which you can open from the application menu.</span></span> 

<span data-ttu-id="36597-118">Um die Planung zu ändern, klicken Sie in eine der Zellen, die verfügbar sind, und geben Sie den angepassten Planungswert ein.</span><span class="sxs-lookup"><span data-stu-id="36597-118">To modify the forecast, click in any of the cells that are available, and type the adjusted forecast value.</span></span> <span data-ttu-id="36597-119">Die bearbeitete Zelle wird sofort fett angezeigt, um anzugeben, dass die Planung, die angezeigt wird, nicht die Planung ist, die der Bedarfsplanungsdienstleistung erstellt hat, sondern dass sie manuell angepasst wurde.</span><span class="sxs-lookup"><span data-stu-id="36597-119">The edited cell immediately becomes bold to indicate that the forecast that it shows isn't the forecast that the demand forecasting service created, but has been manually adjusted.</span></span> 

<span data-ttu-id="36597-120">Wenn Sie die Aggregation ändern, um in der Seite aggregiertere Daten anzuzeigen, können Sie die Seite **Bedarfsplanungspositionen** verwenden, um die einzelnen Planungspositionen zu sehen, die die aggregierte Planung bilden.</span><span class="sxs-lookup"><span data-stu-id="36597-120">If you change the aggregation to make the page show more aggregated data, you can use the **Demand forecast lines** page to see the individual forecast lines that make up the aggregated forecast.</span></span> 

<span data-ttu-id="36597-121">Beispielsweise haben Sie die Planung auf Artikelebene erzeugt, aber Sie wissen, dass der Bedarf für diesen Artikel für alle Standorte aufgrund einer verkaufsfördernden Maßnahme oder eines anderen ähnlichen Ereignisses zunimmt.</span><span class="sxs-lookup"><span data-stu-id="36597-121">For example, you've generated the forecast at the item level, but you know that the demand for this item will increase across all sites because of a promotion or another similar event.</span></span> <span data-ttu-id="36597-122">In diesem Fall können Sie die Aggregation **Unternehmen/Artikelverteilungsschlüssel/Artikel** auf der Seite **Planungsdimensionen ändern** festlegen.</span><span class="sxs-lookup"><span data-stu-id="36597-122">In this case, you can set the aggregation to **Company / Item allocation key / Item** on the **Change forecast dimensions** page.</span></span> <span data-ttu-id="36597-123">Sie können die globale Planung für den Artikel für alle Standorte im Raster **Angepasste Bedarfsplanung** anpassen.</span><span class="sxs-lookup"><span data-stu-id="36597-123">You can adjust the global forecast for the item across all sites in the **Adjusted demand forecast** grid.</span></span> <span data-ttu-id="36597-124">Um die Auswirkung der Änderung für alle Standorte anzuzeigen, öffnen Sie die Seite **Bedarfsplanungspositionen**.</span><span class="sxs-lookup"><span data-stu-id="36597-124">To see the effect of your change across all sites, open the **Demand forecast lines** page.</span></span> <span data-ttu-id="36597-125">Auf dieser Seite finden Sie eine Position für den Artikel für jeden Standort, die regulierte geplante Menge und die ursprüngliche geplante Menge.</span><span class="sxs-lookup"><span data-stu-id="36597-125">On this page, you will see one line for the item for each site, the adjusted forecast quantity, and the original forecast quantity.</span></span> 

<span data-ttu-id="36597-126">Wenn die Anpassung der geplanten Menge auf einer aggregierten Ebene vorgenommen wird, verwendet das System die gewichtete Zuteilung, um die Änderung unter den Positionen zu verteilen, die die Aggregation erstellen.</span><span class="sxs-lookup"><span data-stu-id="36597-126">When the adjustment of the forecasted quantity is made at an aggregated level, the system uses weighted allocation to distribute the change among the lines that create the aggregation.</span></span> 

<span data-ttu-id="36597-127">Sie können auch manuelle Anpassungen auf der Seite **Bedarfsplanungspositionen** vornehmen, indem Sie entweder den Wert **Gesamtmenge** oder die Zellen **Menge** im Raster für die Disaggregation ändern.</span><span class="sxs-lookup"><span data-stu-id="36597-127">You can also make manual adjustments on the **Demand forecast lines** page, by modifying either the **Total quantity** value or the **Quantity** cells in the de-aggregation grid.</span></span>

## <a name="viewing-details-of-the-forecast"></a><span data-ttu-id="36597-128">Anzeigen von Details der Planung</span><span class="sxs-lookup"><span data-stu-id="36597-128">Viewing details of the forecast</span></span>
<span data-ttu-id="36597-129">Sie können die Seite **Bedarfsplanungsdetails** öffnen, um weitere Informationen zur Planung anzeigen.</span><span class="sxs-lookup"><span data-stu-id="36597-129">You can open the **Demand forecast details** page to view more information about the forecast.</span></span> 

<span data-ttu-id="36597-130">Auf der Seite **Bedarfsplanungsdetails** werden die folgenden Informationen in grafischen und Tabellenformaten angezeigt:</span><span class="sxs-lookup"><span data-stu-id="36597-130">The **Demand forecast details** page shows the following information in graphical and tabular formats:</span></span>

-   <span data-ttu-id="36597-131">Der historische Bedarf, auf dem die Planungsvorhersagen basieren.</span><span class="sxs-lookup"><span data-stu-id="36597-131">The historical demand that the forecast predictions are based on.</span></span>
-   <span data-ttu-id="36597-132">Die aktuelle Planung, die von der Produktprogrammplanung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="36597-132">The current forecast that is used by Master planning.</span></span>
-   <span data-ttu-id="36597-133">Die neuen Bedarfsplanungswerte und die Beträge, mit denen sie manuell angepasst wurden.</span><span class="sxs-lookup"><span data-stu-id="36597-133">The new demand forecast values and the amounts they have been manually adjusted by.</span></span>
-   <span data-ttu-id="36597-134">Das Zuverlässigkeitsintervall für die geplanten Werte.</span><span class="sxs-lookup"><span data-stu-id="36597-134">The confidence interval for the forecasted values.</span></span>
-   <span data-ttu-id="36597-135">Das Planzahlenmodell, das verwendet wurde, um die Planung zu generieren.</span><span class="sxs-lookup"><span data-stu-id="36597-135">The forecast model that was used to generate the forecast.</span></span> <span data-ttu-id="36597-136">Wenn Sie aggregierte Daten anzeigen, sehen Sie die Liste aller Methoden, die für alle aggregierten Zeitreihen verwendet wurden.</span><span class="sxs-lookup"><span data-stu-id="36597-136">If you're viewing aggregated data, you will see the list of all the methods that were used for all the aggregated time series.</span></span>
-   <span data-ttu-id="36597-137">Die interne Modellgenauigkeit (MAPE).</span><span class="sxs-lookup"><span data-stu-id="36597-137">The internal model accuracy (MAPE).</span></span> <span data-ttu-id="36597-138">Weitere Informationen zur Prognosegenauigkeit finden Sie unter [Monitor Prognosegenauigkeit](monitor-forecast-accuracy.md).</span><span class="sxs-lookup"><span data-stu-id="36597-138">For more information about forecast accuracy, see [Monitor forecast accuracy](monitor-forecast-accuracy.md).</span></span>

<span data-ttu-id="36597-139">**Hinweise:**</span><span class="sxs-lookup"><span data-stu-id="36597-139">**Notes:**</span></span>

-   <span data-ttu-id="36597-140">Wenn Sie **Auswahl des Prognosemodells bei Bedarfsplanungsdetails** über die Funktionsverwaltung aktivieren, können Sie die Prognosemodelle, die für die historische Prognose einbezogen werden sollen, auf der Seite **Bedarfsplanungsdetails** auswählen.</span><span class="sxs-lookup"><span data-stu-id="36597-140">If you enable **Forecast model selection on Demand forecast details** from Feature management, you will be able to select the forecast models to be include, for the historical forecast, on the **Demand forecast details** page.</span></span>
-   <span data-ttu-id="36597-141">Das Zuverlässigkeitsintervall, das im Abschnitt **Planung** der Seite angezeigt wird, stellt die Differenz zwischen der Obergrenze des Zuverlässigkeitsintervalls und der Untergrenze des Zuverlässigkeitsintervalls dar.</span><span class="sxs-lookup"><span data-stu-id="36597-141">The confidence interval that appears in the **Forecast** section of the page represents the difference between the confidence interval upper limit and the confidence interval lower limit.</span></span> <span data-ttu-id="36597-142">Um die Werte für den oberen und unteren Grenzwert anzuzeigen, bewegen Sie die Maus über das Diagramm im Abschnitt **Historische(r) Bedarf und Planung, grafisch**.</span><span class="sxs-lookup"><span data-stu-id="36597-142">To see the values for the upper and lower limits, hover over the chart in the **Historical demand and forecast graphically** section.</span></span>
-   <span data-ttu-id="36597-143">Wenn Sie den Microsoft Azure Machine Learning-Dienst der Bedarfsplanung verwenden, können Sie die Zuverlässigkeitsstufe angeben, die die generierte Planung haben soll.</span><span class="sxs-lookup"><span data-stu-id="36597-143">If you use the Demand forecasting Microsoft Azure Machine Learning, you can specify the confidence level percentage that the forecast that is generated should have.</span></span> <span data-ttu-id="36597-144">Eine Zuverlässigkeitsintervall besteht aus einem Wertebereich, der eine gute Einschätzung der Bedarfsplanung ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="36597-144">A confidence interval consists of a range of values that act as good estimates for the demand forecast.</span></span> <span data-ttu-id="36597-145">Eine Zuverlässigkeitsstufe von 95 % bedeutet beispielsweise, dass die Bedarfsplanung mit einer Chance von 5 % aus dem Intervallbereich der Zuverlässigkeit fällt.</span><span class="sxs-lookup"><span data-stu-id="36597-145">A 95-percent confidence level percentage indicates that there is a 5-percent risk that the demand forecast falls outside the confidence interval range.</span></span>

<span data-ttu-id="36597-146">Sie können manuelle Anpassungen an der Planung auf der Seite **Bedarfsplanungsdetails** vornehmen, indem Sie die Werte in der Zeile **Planung** im Abschnitt **Planung** ändern.</span><span class="sxs-lookup"><span data-stu-id="36597-146">You can also make manual adjustments to the forecast on the **Demand forecast details** page, by modifying the values in the **Forecast** row in the **Forecast** section.</span></span>

<a name="additional-resources"></a><span data-ttu-id="36597-147">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="36597-147">Additional resources</span></span>
--------

[<span data-ttu-id="36597-148">Planungsgenauigkeit überwachen</span><span class="sxs-lookup"><span data-stu-id="36597-148">Monitor forecast accuracy</span></span>](monitor-forecast-accuracy.md)

[<span data-ttu-id="36597-149">Eine statistische Grundplanung generieren</span><span class="sxs-lookup"><span data-stu-id="36597-149">Generate a statistical baseline forecast</span></span>](generate-statistical-baseline-forecast.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]