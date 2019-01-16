---
title: "Einrichten von Aktualitäts-, Häufigkeits- und Finanzanalyse (RFM)"
description: "In diesem Thema wird erläutert, wie ein Recency-, Häufigkeits- und monetäre (RFM) Analyse Ihrer Debitoren eingerichtet wird."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: MCRRFMDefinition
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 78943
ms.assetid: 8ff9aac3-5ada-4150-85fd-18901c926d53
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: 4314c81823940ce3192da23dfdf777e8ebf781f2
ms.contentlocale: de-de
ms.lasthandoff: 01/04/2019

---

# <a name="set-up-recency-frequency-and-monetary-rfm-analysis"></a>Einrichten von Aktualitäts-, Häufigkeits- und Finanzanalyse (RFM)

[!include [banner](includes/banner.md)]

In diesem Thema wird erläutert, wie ein Recency-, Häufigkeits- und monetäre (RFM) Analyse Ihrer Debitoren eingerichtet wird.

RFM-Analysen (Aktualität, Häufigkeit, Geldbetrag) sind ein Marketinginstrument, das Ihre Organisation verwenden kann, um die Daten zu bewerten, die von Debitorenkäufen generiert werden. Nachdem Sie RFM-Analyse eingerichtet haben, wird Debitoren eine berechnete RFM-Punktzahl zugewiesen, während diese Einkäufe tätigen. Die RFM-Punktzahl kann eine dreistellige Bewertung oder eine Gesamtzahl sein, je nachdem, wie Ihre Organisation RFM-Analyse konfiguriert hat. Hier sehen Sie, wie die Bewertung funktioniert, wenn Ihre Organisation eine dreistellige Bewertung für die Punktzahl verwendet:

- Die erste Stelle ist die „Recency”-Bewertung bezüglich des Kunden, das heißt, wie kurz es her ist, seit der Kunde einen Einkauf bei Ihre Organisation tätigte.
- Die zweite Stelle ist eine Bewertung der Häufigkeit beim Kunden, das heißt, wie oft der Kunde Einkäufe bei Ihrer Organisation tätigt.
- Die dritte Stelle ist eine Bewertung des Geldbetrags, das heißt, wie viel der Kunde ausgibt, wenn er Einkäufe bei Ihrer Organisation tätigt.

So verfügt beispielsweise Ihre Organisation ein Bewertungssystem mit einer Skala von 1 bis 5, wobei 5 die höchste Bewertung ist. In diesem Fall gibt die Kundenbewertung 535 Ihnen folgenden Informationen zum Debitor:

- **Aktualitätsbewertung von 5** – Der Kunde hat erst vor kurzem einen Einkauf getätigt.
- **Häufigkeitsbewertung 3** - Der Kunde erwirbt Produkte von Ihrer Organisation mit mäßiger Häufigkeit.
- **Geldbetragwertung 5** – Wenn der Kunde einen Einkauf tätigt, gibt er einen beträchtlichen Geldbetrag aus.

Wenn Ihre Organisation für die Bewertung eine Aggregatzahl verwendet, werden die einzelnen Bewertungen zusammengezählt. Für das gleiche Beispiel hat der Debitor eine Bewertung von 13 (5 + 3 + 5).

## <a name="to-set-up-rfm-analysis-for-the-customers-in-your-organization"></a>So wird eine Analyse des Modus mit eingeschränkter Funktionalität (RFM) für die Kunden in Ihrer Organisation eingerichtet.

1. Wechseln Sie zu **Callcenter**\>**Periodisch**\>**RFM-Analyse**.
2. Auf der Seite **RFM-Analyse** wählen Sie **Neu** aus. Geben Sie im Feld **RFM-Definition** einen Namen für die RFM-Definition ein. Beispielsweise können Sie die Definition RFM-A nennen.
3. Geben Sie ein Startdatum und ein Enddatum für diese RFM-Definition ein.
4. Führen Sie auf dem Inforegister **Allgemein** die folgenden Schritte aus:

    - Wenn jeder Abschnitt der RFM-Punktzahl eine gleiche Anzahl von Debitoren enthalten muss, aktivieren Sie das Kontrollkästchen **Gleiche Verteilung**.
    - Aktivieren Sie das Kontrollkästchen **Bewertungen hinzufügen**, um die drei Bewertungen zusammenzuzählen. Dies würde beispielsweise einem Debitor eine RFM-Punktzahl von 13 statt 535 geben.
    - Aktivieren Sie das Kontrollkästchen **Historie speichern**, um festzulegen, dass das System die statistischen Daten für Debitoren speichert, sodass die Daten verwendet werden können, um die RFM-Punktzahl zu berechnen.

5. Führen Sie auf dem Inforegister **Recency** die folgenden Schritte aus:

    - Geben Sie im Feld **Divisionen** die Anzahl der Divisionen oder Gruppen ein, die verwendet werden, um die Recency-Punktzahl für Debitoren zu berechnen. Wenn Sie beispielsweise 100 Debitoren haben, bedeutet eine Division 5, dass es 20 Debitoren für jede Bewertung gibt. Die 20 Debitoren, die zuletzt Einkäufe tätigten, haben eine Recency-Punktzahl von 5. Die nächsten 20 Debitoren haben eine Recency-Punktzahl von 4, usw. Wenn Sie 50 Debitoren haben, haben 10 Debitoren eine Recency-Punktzahl 5, 10 haben eine Recency-Punktzahl 4, usw.
    - Wählen Sie im Feld **Priorität** aus, wie viel Gewicht der Recency-Parameter im Verhältnis zu den anderen Parametern haben soll, wenn die RFM-Punktzahl für einen Debitor berechnet wird. Beispielsweise können Sie mehr Gewicht auf die Recency-Punktzahl als die monetäre Punktzahl legen.
    - Geben Sie im Feld **Multiplizierer** den Wert ein, mit dem die Recency-Punktzahl multipliziert werden soll. Wenn Sie keinen Wert eingeben, wird die Punktzahl nicht multipliziert.
    - Wählen Sie im Feld **Periode** die Zeitperiode aus, bis zu der die Recency-Punktzahl berechnet wird. Beispielsweise nach Wochen oder nach Monaten.

6. Führen Sie auf dem Inforegister **Häufigkeit** die folgenden Schritte aus:

    - Geben Sie im Feld **Divisionen** die Anzahl der Divisionen oder Gruppen ein, die verwendet werden, um die Häufigkeitspunktzahl für Debitoren zu berechnen.
    - Wählen Sie im Feld **Priorität** aus, wie viel Gewicht der Häufigkeitsparameter im Verhältnis zu den anderen haben soll, wenn die RFM-Punktzahl für einen Debitor berechnet wird.
    - Geben Sie im Feld **Multiplizierer** den Wert ein, mit dem die Häufigkeitspunktzahl multipliziert werden soll. Wenn Sie keinen Wert eingeben, wird die Punktzahl nicht multipliziert.

7. Führen Sie auf dem Inforegister **Geldbetrag** die folgenden Schritte aus:

    - Geben Sie im Feld **Divisionen** die Anzahl der Divisionen oder Gruppen ein, die verwendet werden, um die Geldbetragspunktzahl für Debitoren zu berechnen.
    - Wählen Sie im Feld **Priorität** aus, wie viel Gewicht der Geldbetragsparameter im Verhältnis zu den anderen haben soll, wenn die RFM-Punktzahl für einen Debitor berechnet wird.
    - Geben Sie im Feld **Multiplizierer** den Wert ein, mit dem die Geldbetragspunktzahl multipliziert werden soll. Wenn Sie keinen Wert eingeben, wird die Punktzahl nicht multipliziert.
    - Wählen Sie Feld **Brutto/netto** aus, ob die Geldbetragspunktzahl des Debitors nach dem Brutto- oder Nettobetrag der Rechnung berechnet werden soll.
    - Wenn die Retourenbeträge eines Debitors von der gesamten Rechnungsberechnung des Debitors subtrahiert werden sollen, aktivieren Sie das Kontrollkästchen **Retouren subtrahieren**.

## <a name="view-a-customers-rfm-score"></a>RFM-Punktzahl eines Debitoren anzeigen

Verwenden Sie diese Prozedur, um die RFM-Punktzahl eines Debitors anzuzeigen.

1. Wechseln Sie zu **Callcenter** \> **Erfassungen** \> **Kundenservice**.
2. Wählen Sie auf der Seite **Kundenservice** im Bereich **Kundenservice** in den Suchfeldern den Schlüsselworttyp aus, nach dem gesucht werden soll, und geben Sie den Suchtext ein.
3. Wählen Sie **Suchen** aus.
4. Wählen Sie auf der Seite **Debitorensuche** den Debitorendatensatz aus, den Sie möchten, und klicken Sie dann auf **Debitor auswählen**.

Die RFM-Punktzahl wird in der Gruppe **Auftragshistorie** auf der rechten Seite der Seite **Kundenservice** angezeigt.

## <a name="view-or-clear-the-history-of-an-rfm-analysis-record"></a>Historie eines RFM-Analysedatensatzes anzeigen oder löschen

Verwenden Sie diese Prozedur, um die Historie eines RFM-Analysedatendsatzes anzuzeigen oder zu löschen.

1. Wechseln Sie zu **Callcenter**\>**Periodisch**\>**RFM-Analyse**.
2. Wählen Sie auf der Seite **RFM-Analyse** den anzuzeigenden Datensatz aus.
3. Um die Historie des Datensatzes anzuzeigen, wählen Sie das Inforegister **Historie**.
4. Um die Historie des Datensatzes zu löschen, wählen Sie **Historie löschen** aus.

