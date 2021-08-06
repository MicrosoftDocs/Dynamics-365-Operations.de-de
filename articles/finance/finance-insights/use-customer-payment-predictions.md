---
title: Verwenden der Zahlungsvorhersagen für Debitoren (Vorschau)
description: In diesem Thema werden die Voraussetzungen und die allgemeinen Schritte erläutert, die für die Verwendung einer Testversion von Finance Insights erforderlich sind.
author: ShivamPandey-msft
ms.date: 07/17/2021
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
ms.search.validFrom: 2020-11-16
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 144de66678beea64b9f96239b519a19926d87ab5
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/17/2021
ms.locfileid: "6638317"
---
# <a name="use-customer-payment-predictions-preview"></a>Verwenden der Zahlungsvorhersagen für Debitoren (Vorschau)

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie die Zahlungsvorhersagen des Kunden verwenden. Stellen Sie vor der Verwendung dieser Funktion sicher, dass Sie die Einrichtungsschritte für diese Funktion ausgeführt haben. Weitere Informationen finden Sie unter [Zahlungsvorhersagen von Debitoren aktivieren](enable-cust-paymnt-prediction.md).

Sie können Debitorenzahlungsvorhersagen im **Debitorenkredit und -inkasso verwalten**-Arbeitsbereich und auf zwei neuen Listenseiten **Zahlungsvorhersagen pro Transaktion** und **Zahlungsvorhersage pro Debitor** anzeigen.

### <a name="manage-customer-credit-and-collections-workspace"></a>Debitorenkredit und -inkasso-Arbeitsbereich verwalten

Der **Debitorenkredite und -inkasso verwalten**-Arbeitsbereich enthält zwei neue Kacheln **Zahlungsvorhersage pro Transaktion** und **Debitoren mit prognostizierten sehr späten Salden**.

- Die Kachel **Zahlungsvorhersage pro Transaktion** zeigt die Anzahl der offenen Debitorentransaktionen mit einer Zahlungswahrscheinlichkeit von weniger als 50 Prozent im Bucket **Pünktlich** an. Sie können diese Kachel auswählen, um die Listenseite **Zahlungsvorhersagen pro Transaktion** zu öffnen.
- Die Kachel **Debitoren mit prognostizierten sehr späten Salden** zeigt die Anzahl der Kunden, für die mehr als die Hälfte (50 Prozent) des Gesamtbetrags voraussichtlich verspätet und/oder sehr spät bezahlt wird. Sie können diese Kachel auswählen, um die Listenseite **Zahlungsvorhersagen pro Debitor** zu öffnen.

[![Debitorenkredit und -inkasso-Arbeitsbereich verwalten.](./media/manage-customer-credit-collections.png)](./media/manage-customer-credit-collections.png)

### <a name="payment-predictions-per-transaction-list-page"></a>Zahlungsvorhersagen pro Transaktionslistenseite

Auf der Listenseite **Zahlungsvorhersagen pro Transaktion** können Sie die Zahlungswahrscheinlichkeit für offene Transaktionen im Bucket **Pünktlich**, **Verspätet** und **Sehr spät** anzeigen. Für jede Transaktion im Raster wird zeigt die Spalte **Pünktliche Wahrscheinlichkeit** die Wahrscheinlichkeit, dass die Rechnung am oder vor dem Fälligkeitsdatum bezahlt wird. Wenn die Wahrscheinlichkeit einer pünktlichen Zahlung weniger als 50 Prozent beträgt, wird neben dem Prozentsatz in der Spalte **Pünktliche Wahrscheinlichkeit** ein roter Kreis angezeigt, um das Risiko einer verspäteten Zahlung anzuzeigen.

[![Listenseite für Zahlungsvorhersagen pro Transaktion.](./media/payment-predictions-per-transaction.png)](./media/payment-predictions-per-transaction.png)

Der Bereich **Verwandte Informationen** auf der rechten Seite zeigt weitere Details zu den Vorhersagen:

- Für die im Raster ausgewählte Transaktion zeigt das Inforegister **Zahlungsvorhersage** die Details der Zahlungsvorhersagen im Bucket **Pünktlich**, **Verspätet** und **Sehr spät** an. Der Abschnitt **Wichtigste Faktoren** zeigt die wichtigsten Faktoren, die die Vorhersagen beeinflusst haben. Die wichtigsten Faktoren sind Attribute der ausgewählten Transaktion und/oder des Debitors für diese Transaktion.
- Das Inforegister **Customer Insights** zeigt die aktuellen Rechnungs-, Zahlungs- und Inkassostatistiken für den Debitor für die ausgewählte Transaktion an.
- Das Inforegister **Debitorenverlauf** zeigt den Zahlungsverlauf des Debitors im Bucket **Pünktlich**, **Verspätet** und **Sehr spät** an.

Die Daten im Abschnitt **Wichtigsten Faktoren** und auf den Inforegistern **Customer Insights** und **Debitorenverlauf** helfen bei der Erläuterung der Zahlungsvorhersagen. Dies kann dazu beitragen, Ihr Vertrauen in die Wirksamkeit der Vorhersagen zu stärken.

[![Grafische Indikatoren für Zahlungsvorhersagen im Bereich „Verwandte Informationen“.](./media/payment-prediction-gauges.png)](./media/payment-prediction-gauges.png)

### <a name="payment-prediction-per-customer-list-page"></a>Listenseite der Zahlungsvorhersage pro Debitor

Die Listenseite **Zahlungsvorhersage pro Debitor** zeigt in den Buckets **Pünktlich**, **Verspätet** und **Sehr spät** den gesamten offenen Kontostand und den Betrag, der voraussichtlich gezahlt wird.

[![Seite der Zahlungsvorhersagen pro Debitor.](./media/payment-predictions-per-transaction-02.png)](./media/payment-predictions-per-transaction-02.png)

Der Zahlungsbetrag in jedem Bucket wird als Summe des gewichteten Durchschnitts des Transaktionssaldos berechnet. Dieser Betrag wird basierend auf den Zahlungswahrscheinlichkeiten in jedem Bucket berechnet.

Ein Debitor hat beispielsweise drei offene Transaktionen mit den folgenden Zahlungswahrscheinlichkeiten in jedem Bucket.

| Transaktion | Dauer | Wahrscheinlichkeit einer pünktlichen Zahlung | Wahrscheinlichkeit einer verspäteten Zahlung | Wahrscheinlichkeit einer sehr späten Zahlung |
|-------------|--------|-----------------------------|--------------------------|-------------------------------|
| T1          | 100    | 10 Prozent                  | 50 Prozent               | 40 Prozent                    |
| T2          | 1.000  | 50 Prozent                  | 30 Prozent               | 20 Prozent                    |
| T3          | 10,000 | 1 Prozent                   | 4 Prozent                | 95 Prozent                    |

In diesem Fall werden die Zahlungen für jeden Bucket folgendermaßen projiziert.

| Buckets   | Transaktion T1      | Transaktion T2         | Transaktion T3            | Summe |
|-----------|---------------------|------------------------|---------------------------|-------|
| Termingerecht   | 100 × 10 ÷ 100 = 10 | 1.000 × 50 ÷ 100 = 500 | 10.000 × 1 ÷ 100 = 100    | 610   |
| Verspätet      | 100 × 50 ÷ 100 = 50 | 1.000 × 30 ÷ 100 = 300 | 10.000 × 4 ÷ 100 = 400    | 750   |
| Sehr verspätet | 100 × 40 ÷ 100 = 40 | 1.000 × 20 ÷ 100 = 200 | 10.000 × 95 ÷ 100 = 9.500 | 9,740 |

Der Abschnitt **Verwandte Informationen** auf der rechten Seite zeigt weitere Details zu den Vorhersagen:

- Für die im Raster ausgewählte Transaktion zeigt das Inforegister **Zahlungsvorhersagen** die Details der Zahlungsvorhersagen im Bucket **Pünktlich**, **Verspätet** und **Sehr spät** an. Der Abschnitt **Wichtigste Faktoren** zeigt die wichtigsten Faktoren, die die Zahlungen beeinflusst haben. Die wichtigsten Faktoren sind Attribute der ausgewählten Transaktion und/oder des Debitors für diese Transaktion.
- Das Inforegister **Customer Insights** zeigt die aktuellen Rechnungs-, Zahlungs- und Inkassostatistiken für den Debitor für die ausgewählte Transaktion an.
- Das Inforegister **Debitorenverlauf** zeigt den Zahlungsverlauf des Debitors im Bucket **Pünktlich**, **Verspätet** und **Sehr spät** an.

Die Daten im Abschnitt **Wichtigsten Faktoren** und auf den Inforegistern **Customer Insights** und **Debitorenverlauf** helfen bei der Erläuterung der Zahlungsvorhersagen. Dies kann dazu beitragen, Ihr Vertrauen in die Wirksamkeit der Vorhersagen zu stärken.

## <a name="improving-the-accuracy-of-payment-predictions"></a>Verbesserung der Genauigkeit von Zahlungsvorhersagen

Sie können die Genauigkeit der Zahlungsvorhersagen anzeigen, indem Sie zu **Kredit und Inkasso \> Einstellungen \> Finance insights \> Parameter für Finance insights** wechseln. Auf der **Debitorenzahlungseinblicke in die Kundenzahlung**-Registerkarte zeigt der **Vorhersagemodell**-Abschnitt die Genauigkeit des Vorhersagemodells in Prozent.

[![Genauigkeit von Zahlungsvorhersagen.](./media/finance-insights-parameters-accuracy-2nd.png)](./media/finance-insights-parameters-accuracy-2nd.png)

Wenn Sie mit der Genauigkeit nicht zufrieden sind, wählen Sie den **Modellgenauigkeit verbessern**-Link zum Öffnen der AI Builder-Erweiterungserfahrung. In der AI Builder-Erweiterungserfahrung können Sie die Feldauswahl auswählen oder abbrechen, bis Sie die Felder ausgewählt haben, die Ihrer Meinung nach für die genaue Vorhersage von Zahlungswahrscheinlichkeiten am wichtigsten sind. Wenn Sie fertig sind, können Sie das Vorhersagemodell einfach neu trainieren und Ihre Änderungen veröffentlichen. Das neu trainierte Vorhersagemodell wird automatisch für Vorhersagen in Dynamics 365 Finance aufgenommen.

[![AI Builder-Erweiterungserfahrung.](./media/ai-builder.png)](./media/ai-builder.png)

## <a name="release-details"></a>Freigabedetails

Die öffentliche Finance Insights-Vorschau ist für Testbereitstellungen in den Vereinigten Staaten von Amerika, Europa und Großbritannien verfügbar. Microsoft fügt schrittweise Unterstützung für weitere Regionen hinzu.

Öffentliche Vorschaufunktionen können und sollten nur in Sandbox-Umgebungen der Stufe 2 aktiviert werden. Einrichtungs- und KI-Mopelle, die in einer Sandbox-Umgebung erstellt werden, können nicht in eine Produktionsumgebung migriert werden. Weitere Informationen finden Sie unter [Ergänzende Nutzungsbedingungen für Microsoft Dynamics 365 Vorschauen](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
