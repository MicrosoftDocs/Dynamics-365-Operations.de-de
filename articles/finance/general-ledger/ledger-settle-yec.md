---
title: Unterschied zwischen Sachkontoausgleichfunktion vor dem Jahresendabschluss
description: In diesem Artikel wird erläutert, wie Sie die Funktion „Unterschied zwischen Sachkontoausgleichen“ verwenden, bevor der Jahresabschlussprozess des Hauptbuchs ausgeführt wurde.
author: kweekley
ms.date: 12/02/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: c79b6f50296560e1534be0621bb2aa8eaa2c1dc8
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2022
ms.locfileid: "9832164"
---
# <a name="awareness-between-ledger-settlement-feature-before-year-end-close"></a>Unterschied zwischen Sachkontoausgleichfunktion vor dem Jahresendabschluss

[!include [banner](../includes/banner.md)]

## <a name="preparing-for-the-ledger-settlement-awareness-feature-before-year-end-close"></a>Vorbereiten auf den Unterschied zwischen Sachkontoausgleichfunktion vor dem Jahresendabschluss

Eine wichtige Änderung der Funktion **Unterschied zwischen Sachkontoausgleich und Jahresendabschluss** (der **Unterschied** Funktion) besteht darin, dass Die Sachkontoabrechnung nicht über Geschäftsjahre hinweg durchgeführt werden kann. Diese jahresübergreifende Beschränkung ist nur für den Sachkontoausgleich relevant, nicht für den Debitoren- oder Kreditorenausgleich.

Bevor die Funktion **Unterschied** aktiviert wird, darf das Geschäftsjahr, das dem Jahresabschluss unterzogen wird, keine Sachkontobuchungen aufweisen, die über Geschäftsjahre hinweg abgerechnet werden. Insbesondere alle Transaktionen, die in das Geschäftsjahr gebucht wurden, für das Sie den Jahresabschluss ausführen, müssen von Transaktionen abgeglichen werden, die in ein anderes Geschäftsjahr gebucht wurden. Die Buchungen können dann mit Buchungen im selben Geschäftsjahr verrechnet werden.

In diesem Artikel wurden die Schritte beschrieben, die erforderlich sind, um die Sachkontobuchungen, die über Geschäftsjahre hinweg ausgeglichen werden, zu identifizieren, aufzuheben und neu auszugleichen. In dem bereitgestellten Beispiel wurde das Geschäftsjahr 2021 abgeschlossen, und Sie bereiten den Jahresabschluss für das Geschäftsjahr 2022 vor.

## <a name="example-setup"></a>Beispiel für die Einrichtung

Die folgende Abbildung zeigt die Transaktionen, die für das Hauptkonto 110190 gebucht wurden. Die grün hinterlegten Hauptbuchbuchungen werden im selben Geschäftsjahr abgerechnet und müssen sich nicht ändern. Die Transaktionen in Rot werden im Hauptbuch abgerechnet, aber sie haben Transaktionsdaten in unterschiedlichen Geschäftsjahren. Diese Transaktionen müssen identifiziert werden, und die Hauptbuchabrechnung muss möglicherweise rückgängig gemacht werden.

![Sachkontobuchungen.](./media/YEC1.png)

## <a name="example"></a>Beispiel:

Befolgen Sie diese Schritte, wenn Ihre Organisation die Funktion **Unterschied** verwenden möchte, bevor der Jahresabschluss für das Geschäftsjahr 2022 ausgeführt wurde.

> [!NOTE]
> Der Jahresabschluss für 2021 und frühere Geschäftsjahre muss nur dann erneut ausgeführt werden, wenn neue Transaktionen in das Geschäftsjahr 2021 oder früher gebucht werden. Wenn Sie das folgende Verfahren abschließen, werden keine neuen Transaktionen in 2021 gebucht. Deshalb muss der Jahresabschluss nicht erneut ausgeführt werden.
>
> Sachkontobuchungen, die über Geschäftsjahre hinweg abgerechnet werden, können im Sachkonto abgerechnet bleiben, wenn sie nicht mit einer Buchung abgerechnet werden, die in 2022 oder später gebucht wurde. Wenn Sie beispielsweise Transaktionen in den Jahren 2019 und 2020 abgerechnet haben, können sie abgerechnet bleiben.

1. Optional: Aktivieren Sie vorübergehend die Funktion **Unterschied** .

    - Wenn Sie die Funktion aktivieren möchten, müssen Sie sie wie erwähnt in späteren Schritten deaktivieren. Wenn Sie die Funktion jetzt aktivieren, haben Sie den Vorteil, dass Sie Benutzer zeitweise daran hindern, Hauptbuchtransaktionen auszugleichen, die in verschiedenen Geschäftsjahren gebucht wurden.
    - Wenn Sie die Funktion nicht aktivieren möchten, empfehlen wir Ihnen, Ihr Team zu bitten, Transaktionen nicht über Geschäftsjahre hinweg abzurechnen. Wenn die jahresübergreifende Abrechnung erfolgt, nachdem die folgenden Schritte abgeschlossen sind, müssen Sie die Schritte wiederholen, um die Hauptbuchtransaktionen zu identifizieren und abzurechnen.

2. Identifizieren Sie auf der Seite **Sachkontoabrechnung** die Gesamtsumme aller Transaktionen, die in den Geschäftsjahren 2021 und 2022 abgerechnet werden.

    1. Geben Sie einen Datumsbereich für das gesamte Geschäftsjahr 2021 an. Geben Sie beispielsweise den 1. Januar 2021 bis zum 31. Dezember 2021 ein, wenn Sie ein Kalenderjahr als Geschäftsjahr verwenden.

        Wenn die Funktion **Unterschied** aktiviert ist, erhalten Sie eine Warnung, dass Transaktionen für ein abgeschlossenes Geschäftsjahr nicht abgerechnet oder nicht abgerechnet werden können. Die Warnung ist nicht relevant, da in diesem Schritt keine Abrechnung oder Aufhebung stattfindet.

    2. Wählen Sie im Feld **Status** die Option **Ausgeglichen** aus.
    3. Filtern Sie jeweils nach einem Sachkonto.

        - Sie müssen diese Schritte für jedes Sachkonto wiederholen, für das der Sachkontoausgleich erfolgt.
        - Wenn andere Sachkonten nicht mehr für den Sachkontoausgleich eingerichtet sind, müssen Sie sie möglicherweise vorübergehend wieder zur Sachkontoausgleichseinrichtung hinzufügen. Führen Sie dann diese Schritte aus, wenn diese Sachkonten Transaktionen im Jahr 2022 aufweisen, die mit Transaktionen in einem anderen Geschäftsjahr abgerechnet werden.

    4. Wählen Sie aus oder halten Sie (mit der rechten Maustaste klicken) in die **Status** Spalte und wählen Sie dann nach dieser Spalte gruppieren.
    5. Wählen Sie aus oder halten Sie (mit der rechten Maustaste klicken) in die **Betrag in Buchungswährung** Spalte und wählen Sie dann diese Spalte zusammenrechnen.

        - Wenn Sie Transaktionen erst im Jahr 2021 abgerechnet haben, ist die Summe 0 (Null).
        - Wenn Sie Transaktionen haben, die über Geschäftsjahre hinweg abgerechnet wurden, ist die Summe nicht 0 (Null).

        In der folgenden Abbildung gibt es einen Saldo von $525,00. Dieser Saldo ist die Summe der Transaktionen, die mit Transaktionen in einem anderen Geschäftsjahr verrechnet wurden. Ihre Summe kann Transaktionen enthalten, die zwischen 2021 und 2022 abgewickelt wurden, und Transaktionen, die zwischen 2022 und 2023 abgerechnet wurden.

        ![Sachkontobuchungen 2021-2022.](./media/YEC2.png)

    6. Identifizieren Sie, welche Transaktionen zwischen 2020 und 2021 abgerechnet wurden, indem Sie weiter nach dem Wert **Abrechnungsdatum** filtern. Geben Sie einen Datumsbereichsfilter vom 1. Januar 2021 bis zum 31. Dezember 2021 an. Es werden keine Transaktionen angezeigt, da keine 2020-Transaktionen mit Transaktionen abgerechnet wurden, die in 2021 gebucht wurden.
    7. Identifizieren Sie, welche Transaktionen zwischen 2021 und 2022 abgerechnet wurden, indem Sie den Datumsfilter auf dem Wert **Abrechnungsdatum** ändern. Geben Sie einen Datumsbereichsfilter vom 1. Januar 2022 bis zum 31. Dezember 2022 an. Die Transaktionen werden erneut angezeigt, und die Summe ist $525.00, da alle Transaktionen zwischen 2021 und 2022 abgewickelt wurden.

3. Identifizieren Sie auf der Seite **Sachkontoabrechnung** die Gesamtsumme aller Transaktionen, die in den Geschäftsjahren 2021 und 2022 abgerechnet werden.

    1. Geben Sie einen Datumsbereich für das gesamte Geschäftsjahr 2022 an. Geben Sie beispielsweise den 1. Januar 2022 bis zum 31. Dezember 2022 an, wenn Sie ein Kalenderjahr als Geschäftsjahr verwenden.
    2. Wählen Sie im Feld **Status** die Option **Ausgeglichen** aus.
    3. Filtern Sie jeweils nach einem Sachkonto.
    4. Wählen Sie aus oder halten Sie (mit der rechten Maustaste klicken) in die **Status** Spalte und wählen Sie dann nach dieser Spalte gruppieren.
    5. Wählen Sie aus oder halten Sie (mit der rechten Maustaste klicken) in die **Betrag in der Buchungswährung** Spalte und wählen Sie dann diese Spalte zusammenrechnen.

        ![Gesamtbeträge der Sachkontotransaktionen.](./media/YEC3.png)

    6. Fügen Sie einen zusätzlichen Filter für den Wert **Abrechnungsdatum** hinzu. Geben Sie einen Datumsbereichsfilter vom 1. Januar 2022 bis zum 31. Dezember 2022 an. Die gleiche Summe von $525.00 wird angezeigt. Dieses Ergebnis bestätigt, dass der Gesamtbetrag der Transaktionen, die in den Jahren 2021 und 2022 abgewickelt werden, $525,00 beträgt.

        ![Hauptbuchtransaktionen für Abrechnungsdaten in 2022 und 2023.](./media/YEC4.png)

    7. Ändern Sie den zusätzlichen Filter für den Wert **Abrechnungsdatum**. Geben Sie einen Datumsbereichsfilter vom 1. Januar 2023 bis zum 31. Dezember 2023 an. Eine neue Gesamtzahl von $700 wird angezeigt. Diese Summe ist der Gesamtbetrag der Transaktionen, die in den Jahren 2022 und 2023 abgewickelt wurden.
 
4. Wiederholen Sie Schritt 3 für das Geschäftsjahr 2023. Die Summe sollte mit der $700 von 2022 übereinstimmen, da keine 2023-Transaktionen gegen 2024-Transaktionen abgerechnet wurden.
5. Wenn Sie die Funktion **Unterschied** in Schritt 1 aktiviert haben, deaktivieren Sie sie, bevor Sie mit Schritt 6 fortfahren. In den nächsten Schritten stornieren Sie den geschäftsjahresübergreifenden Sachkontoausgleich. Wenn die Funktion **Unterschied** aktiviert ist, kann die Sachkontoabrechnung für das Geschäftsjahr 2021 nicht rückgängig gemacht werden. Daher müssen Sie die Funktion deaktivieren, bevor Sie fortfahren.
6. Nachdem die Funktion **Unterschied** deaktiviert wurde, verwenden Sie dieselben Filter auf der Seite **Hauptbuchabrechnung**, um die Hauptbuchabrechnung von rückgängig zu machen die detaillierten Transaktionen.

    1. Kehren Sie zur Seite **Hauptbuchabrechnung** zurück und filtern Sie nach Transaktionsdaten für 2021. Fügen Sie einen zusätzlichen Filter für den Wert **Abrechnungsdatum** hinzu. Geben Sie einen Datumsbereichsfilter vom 1. Januar 2022 bis zum 31. Dezember 2022 an. Suchen Sie dann die detaillierten Transaktionen, die die Gesamtsumme von $525 ausmachen. Das Filtern nach diesen Informationen ist möglicherweise nicht einfach. Eventuell müssen Sie die Daten zur Auswertung an Microsoft Excel senden.
    2. Nachdem Sie die Liste der Buchungen haben, wählen Sie die Hauptbuchbuchungen auf der Seite **Hauptbuchausgleich** und dann **Ausgewählt markieren** aus. Sie müssen nicht beide Seiten der Buchhaltungstransaktionen sehen, die abgerechnet wurden. Wenn Sie entweder die Belastung oder die Gutschrift markieren, wird alles, was den gleichen **Abrechnungs-ID** Wert hat, storniert, auch wenn der **markierte Betrag** Wert ist nicht **0** (Null).
    3. Wählen Sie **Markierte Transaktionen stornieren**, um die Transaktionen abzubrechen.

    ![Markierte Transaktionen rückgängig machen.](./media/YEC5.png)

7. Wiederholen Sie Schritt 6, um die Abrechnung für die Transaktionen zu stornieren, die in den Jahren 2022 und 2023 abgerechnet wurden.

    ![Rückbuchung von Sachkontobuchungen](./media/YEC6.png)

8. Buchen Sie ein Anpassungshauptbuchblatt, um die Eröffnungsbilanz für 2022 in zwei Beträge aufzuteilen: den Teil, der mit der Buchung für das Geschäftsjahr 2021 ausgeglichen wird, und den Teil, der 2022 noch nicht ausgeglichen wird.

    - **Teil des Eröffnungssaldos, der mit dem Vorjahr verrechnet wird:** Der erste Betrag ist $525, basierend auf den ermittelten Summen, die über die Jahre 2021 und 2022 verrechnet wurden.
    - **Teil des Eröffnungssaldos, der nicht mit dem Vorjahr verrechnet wird:** Der zweite Betrag ist die Differenz zwischen dem Eröffnungssaldo und dem ausgeglichenen Betrag von $525. Der Restbetrag ist $1025 – $525 = $500.

    Auf diese Weise können Sie die 2022-Transaktionen gegen die $525 abrechnen, die ursprünglich gegen die 2021-Transaktion abgerechnet wurden. Dieser Schritt ist erforderlich, da die Sachkontoabrechnung keine Teilabrechnung zulässt.

    1. Wechseln Sie in das allgemeine Journal und buchen Sie die Anpassung. Ihre Organisation muss basierend auf den offenen Zeiträumen entscheiden, welches Transaktionsdatum verwendet werden soll. Diese Transaktionen wurden möglicherweise unter Verwendung eines Abwicklungsdatums im Januar oder Februar 2022 abgerechnet, aber die Anpassung muss möglicherweise im Dezember gebucht werden, wenn dies der einzige offene Zeitraum ist.
    2. Möglicherweise müssen Sie den Parameter **Manuelle Eingabe nicht zulassen** auf der Seite **Hauptkonto** vorübergehend deaktivieren. Diese Anpassung wird nicht gebucht, wenn das Hauptkonto keine manuelle Eingabe zulässt.

    ![Regulierungen nicht gebucht werden.](./media/YEC7.png)

9. Sie können nun die offenen Transaktionen zurücksetzen. Kehren Sie zur Seite **Hauptbuchausgleich** zurück und begrenzen Sie den Datumsbereich auf den 1. Januar 2022 bis zum 31. Dezember 2022. Die folgende Abbildung zeigt die nicht ausgeglichenen Transaktionen, die jetzt vorhanden sind.

    ![Nicht ausgeglichene Buchungen.](./media/YEC8.png)

    - Der Eröffnungssaldo von $1,025 kann mit der Anpassung für -1.025 $ verrechnet werden.
    - Die detaillierten Transaktionen, die für -$400, -$50 und -$75 nicht abgerechnet wurden, können mit der Anpassung für $525,00 abgerechnet werden.

    ![Ausführliche Buchungen.](./media/YEC9.png)

10. Aktivieren Sie die Funktion **Unterschied**. Sie können nun den Jahresabschluss ausführen.

    - Bevor Sie den Jahresabschluss ausführen, sollten Sie in Betracht ziehen, die Option **Details beibehalten** in der Sachkontoausgleichseinstellung für alle Bilanzkonten auszuwählen. Weitere Informationen zu den Vorteilen dieses Schritts finden Sie im Awareness-Dokument.
    - Wenn Sie mit dem Jahresabschluss für 2022 beginnen und noch Transaktionen gefunden werden, die über Geschäftsjahre hinweg abgerechnet werden, werden Sie vom Jahresabschlussprozess sofort benachrichtigt.
    - Wenn die Transaktionen für 2021 und 2022 noch abgerechnet werden, müssen Sie die Funktion **Unterschied** erneut deaktivieren und die vorherigen Schritte wiederholen, um die Transaktionen abzubrechen. Dieser Ansatz ist erforderlich, da das Jahr 2021 abgeschlossen ist und Transaktionen in einem abgeschlossenen Geschäftsjahr nicht verrechnet werden können.
    - Wenn Transaktionen für 2022 und 2023 noch abgerechnet werden, müssen Sie **nicht** die Funktion **Unterschied** deaktivieren. Da weder 2022 noch 2023 geschlossen sind, können Sie die vorherigen Schritte verwenden, um die Transaktionen zu verunsichern.

Nachdem der Jahresabschluss für 2022 erfolgreich durchgeführt wurde, können Sie die Funktion **Unterschied** von nun an aktiviert lassen.
