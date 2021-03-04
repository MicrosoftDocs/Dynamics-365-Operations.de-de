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
ms.search.scope: Core, Operations
ms.custom: 72704
ms.assetid: e7c5d44e-07bc-40b1-a4b3-8ba46483ef9e
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9dc5d1812fa926216a75b6fc4e3cf820ccc3ef6d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428941"
---
# <a name="make-manual-adjustments-to-the-baseline-forecast"></a>Manuelle Anpassungen an der Grundplanung

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie manuelle Anpassungen an einer Grundplanung vornehmen und Details der Planung anzeigen können. 

Bevor Sie manuelle Anpassungen vornehmen, ist es wichtig, dass Sie einige Konzepte für verschiedene Seiten verstehen.

## <a name="grid-on-the-adjusted-demand-forecast-page"></a>Raster auf der Seite "Angepasste Bedarfsplanung“
Die Seite **Angepasste Bedarfsplanung** umfasst ein Raster, das die folgende Struktur hat:

-   Die erste Spalte enthält Artikel, Artikelverteilungsschlüssel, Unternehmen usw., für die die Planung generiert wurde. Der Untertitel der Seite enthält eine Beschreibung der aktuellen Planungsdimensionen, die im Raster angezeigt werden. Wenn beispielsweise der Untertitel der Seite **Unternehmen / Standort / Artikelverteilungsschlüssel** ist und eine der Zeilenbeschriftungen im Raster **USMF / 1 / D\_Alloc** ist, enthält diese Zeile die Planung für das Unternehmen USMF, Standort 1 und den Artikelverteilungsschlüssel **D\_Alloc**.
-   Nachfolgende Spalten stellen die Planungszeitrahmen dar, für die die Planung für generiert wurde. Jede Spaltenüberschrift ist das erste Datum des Planungszeitrahmens, den die Spalte anzeigt.
-   Die Werte in den Zellen stellen die Planung für einen Artikel, Artikelverteilungsschlüssel usw. für diesen bestimmten Planungszeitrahmen dar.

## <a name="forecast-aggregation-and-de-aggregation"></a>Planungsaggregation und -disaggregation
Der Untertitel der Seite enthält die Ebene der Planungsaggregation. 

Wenn beispielsweise der Untertitel der Seite **Unternehmen/Standort/Verteilungsschlüssel/Artikelnummer/Farbe/Größe/Konfiguration/Stil** lautet, gibt es keine Planungsaggregation, und die Planung wird auf der Ebene des Artikels und der Dimensionen angezeigt. Um die Aggregation zu ändern, verwenden Sie die Seite **Planungsdimensionen ändern**, die Sie über das Anwendungsmenü öffnen können. 

Um die Planung zu ändern, klicken Sie in eine der Zellen, die verfügbar sind, und geben Sie den angepassten Planungswert ein. Die bearbeitete Zelle wird sofort fett angezeigt, um anzugeben, dass die Planung, die angezeigt wird, nicht die Planung ist, die der Bedarfsplanungsdienstleistung erstellt hat, sondern dass sie manuell angepasst wurde. 

Wenn Sie die Aggregation ändern, um in der Seite aggregiertere Daten anzuzeigen, können Sie die Seite **Bedarfsplanungspositionen** verwenden, um die einzelnen Planungspositionen zu sehen, die die aggregierte Planung bilden. 

Beispielsweise haben Sie die Planung auf Artikelebene erzeugt, aber Sie wissen, dass der Bedarf für diesen Artikel für alle Standorte aufgrund einer verkaufsfördernden Maßnahme oder eines anderen ähnlichen Ereignisses zunimmt. In diesem Fall können Sie die Aggregation **Unternehmen/Artikelverteilungsschlüssel/Artikel** auf der Seite **Planungsdimensionen ändern** festlegen. Sie können die globale Planung für den Artikel für alle Standorte im Raster **Angepasste Bedarfsplanung** anpassen. Um die Auswirkung der Änderung für alle Standorte anzuzeigen, öffnen Sie die Seite **Bedarfsplanungspositionen**. Auf dieser Seite finden Sie eine Position für den Artikel für jeden Standort, die regulierte geplante Menge und die ursprüngliche geplante Menge. 

Wenn die Anpassung der geplanten Menge auf einer aggregierten Ebene vorgenommen wird, verwendet das System die gewichtete Zuteilung, um die Änderung unter den Positionen zu verteilen, die die Aggregation erstellen. 

Sie können auch manuelle Anpassungen auf der Seite **Bedarfsplanungspositionen** vornehmen, indem Sie entweder den Wert **Gesamtmenge** oder die Zellen **Menge** im Raster für die Disaggregation ändern.

## <a name="viewing-details-of-the-forecast"></a>Anzeigen von Details der Planung
Sie können die Seite **Bedarfsplanungsdetails** öffnen, um weitere Informationen zur Planung anzeigen. 

Auf der Seite **Bedarfsplanungsdetails** werden die folgenden Informationen in grafischen und Tabellenformaten angezeigt:

-   Der historische Bedarf, auf dem die Planungsvorhersagen basieren.
-   Die aktuelle Planung, die von der Produktprogrammplanung verwendet wird.
-   Die neuen Bedarfsplanungswerte und die Beträge, mit denen sie manuell angepasst wurden.
-   Das Zuverlässigkeitsintervall für die geplanten Werte.
-   Das Planzahlenmodell, das verwendet wurde, um die Planung zu generieren. Wenn Sie aggregierte Daten anzeigen, sehen Sie die Liste aller Methoden, die für alle aggregierten Zeitreihen verwendet wurden.
-   Die interne Modellgenauigkeit (MAPE). Weitere Informationen zur Prognosegenauigkeit finden Sie unter [Monitor Prognosegenauigkeit](monitor-forecast-accuracy.md).

**Hinweise:**

-   Wenn Sie **Auswahl des Prognosemodells bei Bedarfsplanungsdetails** über die Funktionsverwaltung aktivieren, können Sie die Prognosemodelle, die für die historische Prognose einbezogen werden sollen, auf der Seite **Bedarfsplanungsdetails** auswählen.
-   Das Zuverlässigkeitsintervall, das im Abschnitt **Planung** der Seite angezeigt wird, stellt die Differenz zwischen der Obergrenze des Zuverlässigkeitsintervalls und der Untergrenze des Zuverlässigkeitsintervalls dar. Um die Werte für den oberen und unteren Grenzwert anzuzeigen, bewegen Sie die Maus über das Diagramm im Abschnitt **Historische(r) Bedarf und Planung, grafisch**.
-   Wenn Sie den Microsoft Azure Machine Learning-Dienst der Bedarfsplanung verwenden, können Sie die Zuverlässigkeitsstufe angeben, die die generierte Planung haben soll. Eine Zuverlässigkeitsintervall besteht aus einem Wertebereich, der eine gute Einschätzung der Bedarfsplanung ermöglicht. Eine Zuverlässigkeitsstufe von 95 % bedeutet beispielsweise, dass die Bedarfsplanung mit einer Chance von 5 % aus dem Intervallbereich der Zuverlässigkeit fällt.

Sie können manuelle Anpassungen an der Planung auf der Seite **Bedarfsplanungsdetails** vornehmen, indem Sie die Werte in der Zeile **Planung** im Abschnitt **Planung** ändern.

<a name="additional-resources"></a>Zusätzliche Ressourcen
--------

[Planungsgenauigkeit überwachen](monitor-forecast-accuracy.md)

[Eine statistische Grundplanung generieren](generate-statistical-baseline-forecast.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]