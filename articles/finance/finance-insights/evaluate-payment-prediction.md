---
title: Bewerten des anfänglichen Kundenzahlungsvorhersagemodells (Vorschau)
description: In diesem Thema werden die Schritte beschrieben, die Sie ausführen können, um das Kundenvorhersagemodell zu verstehen und seine Wirksamkeit zu bewerten.
author: ShivamPandey-msft
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: f45392d540b6696d23261a6b2197c3185f5ede2b7c646f6b751480145dcacfdc
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768866"
---
# <a name="evaluate-the-initial-customer-payment-prediction-model-preview"></a>Bewerten des anfänglichen Kundenzahlungsvorhersagemodells (Vorschau)

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie ein Vorhersagemodell bewerten, nachdem Sie Finance Insights aktiviert und anschließend Ihr erstes Modell generiert und trainiert haben. Dieses Thema befasst sich mit Modellen zur Vorhersage von Kundenzahlungen. Darin werden die Schritte beschrieben, die Sie ausführen können, um das Kundenvorhersagemodell zu verstehen und seine Wirksamkeit zu bewerten.

## <a name="getting-details-about-the-model"></a>Details zum Modell abrufen

Auf der **Finance Insights-Parameter**-Seite in Microsoft Dynamics 365 Finance wird ein **Modellgenauigkeit verbessern**-Link neben der Genauigkeitsbewertung angezeigt.

[![Link „Verbessern der Modellgenauigkeit“.](./media/prediction-model.png)](./media/prediction-model.png)

Über diesen Link gelangen Sie zum AI Builder, wo Sie mehr über das aktuelle Modell erfahren und Schritte unternehmen können, um es zu verbessern. Die folgende Abbildung zeigt die Seite, die geöffnet wird.

[![AI Builder.](./media/what-to-predict.png)](./media/what-to-predict.png)

Die Seite, die geöffnet wird, zeigt die Folgenden Informationen:

- Im Abschnitt **Leistung** bietet der Modellleistungsgrad einen Überblick über die Qualität des Modells. Weitere Informationen zu dieser Klasse finden Sie unter [Leistung des Vorhersagemodells](/ai-builder/prediction-performance) in der AI Builder-Dokumentation.
- Der Abschnitt **Die einflussreichsten Daten** zeigt, wie wichtig verschiedene Eingabetypen für Ihr Modell waren. Sie können diese Liste und die entsprechenden Prozentsätze auswerten, um festzustellen, ob die Informationen mit Ihren Kenntnissen über Ihr Unternehmen und Ihren Markt übereinstimmen.

    [![Die Abschnitte zur Leistung und zu den einflussreichsten Daten für das Vorhersagemodell.](./media/models.png)](./media/models.png)

- Wählen Sie im Abschnitt **Leistung** **Siehe Einzelheiten** aus, um mehr über den Grad und andere Überlegungen zu erfahren. In der folgenden Abbildung zeigen die Details, dass das Modell weniger Informationen verwendet als empfohlen. Daher hat das System eine Warnmeldung generiert.

    [![Warnungen zur Leistung des Modells.](./media/details.png)](./media/details.png)

## <a name="digging-deeper"></a>Tiefergehen

Obwohl Genauigkeit ein guter Ausgangspunkt für die Bewertung eines Modells ist und die Leistungsstufe eine Perspektive bietet, bietet AI Builder detailliertere Metriken, die Sie für Ihre Bewertung verwenden können. Um die Details herunterzuladen, wählen Sie im Abschnitt **Leistung** die Schaltfläche mit den Auslassungspunkten (**...**) neben der **Modell verwenden**-Schaltfläche und dann **Detaillierte Messdaten herunterladen** aus.

[![Befehl für detaillierte Metriken herunterladen.](./media/performance.png)](./media/performance.png)

Die folgende Abbildung zeigt das Format, in dem Sie die Daten herunterladen können.

[![Format der heruntergeladenen Daten.](./media/data-format.png)](./media/data-format.png)

Für eine eingehendere Analyse der Ergebnisse ist es ein guter Ausgangspunkt, die Metrik „Verwirrungsmatrix“ zu überprüfen. Hier sind beispielsweise die Daten, die für diese Metrik in der vorherigen Abbildung gezeigt wurden.

`{"name": "Confusion Matrix", "value": {"schema_type": "confusion_matrix", "schema_version": "1.0.0", "data": {"class_labels": ["0", "1", "2"], "matrix": [[71, 9, 21], [5, 0, 27], [2, 0, 45]]}}, "type": "dictionaryNumericalList", "isGlobalScore": false}`

Sie können diese Daten folgendermaßen erweitern.

| &nbsp;                   | Als pünktlich vorhergesagt | Als verspätet vorhergesagt | Als sehr spät vorhergesagt |
|--------------------------|-------------------|----------------|---------------------|
| Tatsächliche pünktliche Zahlung   | **71**            | 0              | 21                  |
| Tatsächliche verspätete Zahlung      | 5                 | **0**          | 27                  |
| Tatsächliche sehr späte Zahlung | 2                 | 0              | **45**              |

Die Verwirrungsmatrix zeigt die Ergebnisse eines zufällig ausgewählten Testdatensatzes aus dem Trainingsprozess. Da diese geschlossenen Rechnungen nicht zum Trainieren des Modells verwendet wurden, sind sie gute Testfälle für das Modell. Da der tatsächliche Status der Rechnung bekannt ist, kann außerdem die Leistung des Modells angezeigt werden.

Das erste, wonach gesucht werden muss, ist der häufigste tatsächliche Wert. Obwohl dieser Wert möglicherweise nicht perfekt mit dem Gesamtdatensatz übereinstimmt, ist dies eine vernünftige Annäherung. In diesem Fall tritt **Tatsächliche pünktliche Zahlung** bei 92 der insgesamt 171 Rechnungen auf und ist der häufigste Istwert. Daher ist es eine gute Basis für Ihr Modell. Wenn Sie nur vermutet hätten, dass alle Rechnungen pünktlich wären, hätten Sie 92 von 171 Mal Recht gehabt (d.h. in 54 Prozent der Fälle).

Es ist wichtig, dass Sie verstehen, wie ausgewogen Ihr Datensatz ist. In diesem Fall wurden 92 von 171 Rechnungen pünktlich, 32 verspätet und 47 sehr spät bezahlt. Diese Werte weisen auf einen angemessen ausgewogenen Datensatz hin, da jede Klassifizierung nicht triviale Ergebnisse enthält. Eine Situation, in der einer der Zustände nur sehr wenige Ergebnisse erzielt, kann für ein Machine Learning-Modell eine Herausforderung darstellen.

Die Genauigkeit des Modells gibt die Anzahl der korrekten Vorhersagen für den Testdatensatz an. Diese korrekten Vorhersagen sind die Werte, die im vorhergehenden Beispiel fett dargestellt sind. In diesem Fall ergeben die Werte eine berechnete Genauigkeit von 67,8 Prozent (= \[71 + 0 + 45\] ÷ 171). Dieser Wert stellt eine Verbesserung von 14 Prozent gegenüber der Basisschätzung von 54 Prozent dar und ist ein Indikator für die Qualität des Modells.

Wenn Sie sich die Verwirrungsmatrix genauer ansehen, werden Sie feststellen, dass das Modell pünktliche und sehr späte Rechnungszahlungen gut vorhersagt. Es ist jedoch falsch, wenn alle 32 Rechnungen tatsächlich verspätet (aber nicht sehr spät) bezahlt wurden. Dieses Ergebnis legt nahe, dass zusätzliche Untersuchungen und Verbesserungen des Modells erforderlich sind.

Eine Zahl, die die Leistung des Modells besser als die Genauigkeit darstellt, ist der F1-Makro-Wert. Diese Bewertung berücksichtigt die Ergebnisse jedes Klassifizierungsstatus (pünktlich, verspätet und sehr spät). Hier sind beispielsweise die Daten, die für diese „F1-Makro“-Metrik in der vorherigen Abbildung gezeigt wurden.

`{"name": "F1 Macro", "value": 0.4927170868347339, "type": "percentage", "isGlobalScore": false}`

In diesem Fall zeigt der F1-Makro-Wert von ungefähr 49,3 Prozent an, dass das Modell trotz eines relativ hohen Gesamtgenauigkeitswerts nicht für jeden Zustand effektive Vorhersagen liefert.

## <a name="improving-the-model"></a>Das Modell verbessern

Nachdem Sie die Ergebnisse Ihres ersten Modells besser verstanden haben, möchten Sie das Modell möglicherweise verbessern, indem Sie Funktionsspalten hinzufügen oder entfernen oder Teile des Datasets filtern, die keine genauen Vorhersagen unterstützen. Schließen Sie AI Builder und verwenden Sie dann den **Modell verbessern** -Link in Dynamics 365 Finance, um den AI Builder-Prozess neu zu starten. Sie können mit verschiedenen Merkmalen experimentieren, ohne das veröffentlichte Modell zu beeinflussen. Das veröffentlichte Modell ist nur betroffen, wenn Sie **Buchen** auswählen. Denken Sie daran, dass für Ihre Instanz von Dynamics 365 Finance ein einzelnes Modell verwendet wird. Daher sollten Sie jedes neue Modell sorgfältig prüfen, bevor Sie es veröffentlichen.

## <a name="for-more-information"></a>Weitere Informationen

Weitere Informationen dazu, wie Sie Vorhersagemodelle bewerten, finden Sie unter [Ergebnisse von Machine Learning-Modellen](/confusion-matrix.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
