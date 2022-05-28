---
title: Vorhersagen für Kundenzahlungen verwenden
description: In diesem Thema werden die Voraussetzungen und die allgemeinen Schritte erläutert, die für die Verwendung einer Testversion von Finance Insights erforderlich sind.
author: ShivamPandey-msft
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-11-16
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: ecc864485dfc106df22b48e92a85f2c73d58e0e8
ms.sourcegitcommit: d70f66a98eff0a2836e3033351b482466bd9c290
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2022
ms.locfileid: "8740623"
---
# <a name="use-customer-payment-predictions"></a>Vorhersagen für Kundenzahlungen verwenden

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie die Zahlungsvorhersagen des Kunden verwenden. Stellen Sie vor der Verwendung dieser Funktion sicher, dass Sie die Einrichtungsschritte für diese Funktion ausgeführt haben. Weitere Informationen finden Sie unter [Zahlungsvorhersagen von Debitoren aktivieren](enable-cust-paymnt-prediction.md).

Sie können Debitorenzahlungsvorhersagen im **Debitorenkredit und Inkassi verwalten**-Arbeitsbereich und auf zwei neuen Listenseiten anzeigen: **Zahlungsvorhersagen für Transaktion** und **Zahlungsvorhersagen für Debitor**.

### <a name="manage-customer-credit-and-collections-workspace"></a>Debitorenkredit und -inkasso-Arbeitsbereich verwalten

Der **Debitorenkredit und Inkassi verwalten**-Arbeitsbereich enthält zwei neue Kacheln: **Zahlungsvorhersagen für Transaktion** und **Zahlungsvorhersagen für Debitoren**.

### <a name="transaction-payment-predictions-list-page"></a>Listenseite der Zahlungsvorhersagen für Transaktion

Auf der Listenseite **Zahlungsvorhersagen für Transaktion** können Sie die Zahlungswahrscheinlichkeit für offene Transaktionen im Bucket **Pünktlich**, **Verspätet** und **Sehr spät** anzeigen. Für jede Transaktion im Raster wird zeigt die Spalte **Pünktliche Wahrscheinlichkeit** die Wahrscheinlichkeit, dass die Rechnung am oder vor dem Fälligkeitsdatum bezahlt wird. Wenn die Wahrscheinlichkeit einer pünktlichen Zahlung weniger als 50 Prozent beträgt, wird neben dem Prozentsatz in der Spalte **Pünktliche Wahrscheinlichkeit** ein roter Kreis angezeigt, um das Risiko einer verspäteten Zahlung anzuzeigen.

[![Listenseite für Zahlungsvorhersagen pro Transaktion.](./media/payment-predictions-per-transaction.png)](./media/payment-predictions-per-transaction.png)

Der Bereich **Verwandte Informationen** auf der rechten Seite zeigt weitere Details zu den Vorhersagen:

- Für die im Raster ausgewählte Transaktion zeigt das Inforegister **Zahlungsvorhersage** die Details der Zahlungsvorhersagen im Bucket **Pünktlich**, **Verspätet** und **Sehr spät** an. Der Abschnitt **Wichtigste Faktoren** zeigt die wichtigsten Faktoren, die die Vorhersagen beeinflusst haben. Die wichtigsten Faktoren sind Attribute der ausgewählten Transaktion und/oder des Debitors für diese Transaktion.
- Das Inforegister **Customer Insights** zeigt die aktuellen Rechnungs-, Zahlungs- und Inkassostatistiken für den Debitor für die ausgewählte Transaktion an.
- Das Inforegister **Debitorenverlauf** zeigt den Zahlungsverlauf des Debitors im Bucket **Pünktlich**, **Verspätet** und **Sehr spät** an.

Die Daten im Abschnitt **Wichtigsten Faktoren** und auf den Inforegistern **Customer Insights** und **Debitorenverlauf** helfen bei der Erläuterung der Zahlungsvorhersagen. Dies kann dazu beitragen, Ihr Vertrauen in die Wirksamkeit der Vorhersagen zu stärken.

[![Grafische Indikatoren für Zahlungsvorhersagen im Bereich „Verwandte Informationen“.](./media/payment-prediction-gauges.png)](./media/payment-prediction-gauges.png)

### <a name="customer-payment-predictions-list-page"></a>Listenseite der Zahlungsvorhersagen für Debitor

Die Listenseite **Zahlungsvorhersage für Debitor** zeigt in den Buckets **Pünktlich**, **Verspätet** und **Sehr spät** den gesamten offenen Kontostand und den Betrag, der voraussichtlich gezahlt wird.

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

- Für die im Raster ausgewählte Transaktion zeigt das Inforegister **Zahlungsvorhersagen** die Details der Zahlungsvorhersagen im Bucket **Pünktlich**, **Verspätet** und **Sehr spät** an.
- Das Inforegister **Customer Insights** zeigt die aktuellen Rechnungs-, Zahlungs- und Inkassostatistiken für den Debitor für die ausgewählte Transaktion an.
- Das Inforegister **Debitorenverlauf** zeigt den Zahlungsverlauf des Debitors im Bucket **Pünktlich**, **Verspätet** und **Sehr spät** an.

Die Daten in den Inforegistern **Customer Insights** und **Debitorenhistorie** helfen bei der Erläuterung der Zahlungsvorhersagen. Dies kann dazu beitragen, Ihr Vertrauen in die Wirksamkeit der Vorhersagen zu stärken.

## <a name="improving-the-accuracy-of-payment-predictions"></a>Verbesserung der Genauigkeit von Zahlungsvorhersagen

Sie können die Genauigkeit der Zahlungsvorhersagen anzeigen, indem Sie zu **Kredit und Inkasso \> Einstellungen \> Finance insights \> Parameter für Finance insights** wechseln. Auf der **Debitorenzahlungseinblicke in die Kundenzahlung**-Registerkarte zeigt der **Vorhersagemodell**-Abschnitt die Genauigkeit des Vorhersagemodells in Prozent.

Wenn Sie mit der Genauigkeit nicht zufrieden sind, wählen Sie den **Modellgenauigkeit verbessern**-Link zum Öffnen der AI Builder-Erweiterungserfahrung. In der AI Builder-Erweiterungserfahrung können Sie die Feldauswahl auswählen oder abbrechen, bis Sie die Felder ausgewählt haben, die Ihrer Meinung nach für die genaue Vorhersage von Zahlungswahrscheinlichkeiten am wichtigsten sind. Wenn Sie fertig sind, können Sie das Vorhersagemodell einfach neu trainieren und Ihre Änderungen veröffentlichen. Das neu trainierte Vorhersagemodell wird automatisch für Vorhersagen in Dynamics 365 Finance aufgenommen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
