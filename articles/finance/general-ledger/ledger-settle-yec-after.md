---
title: Unterschied zwischen Sachkontoausgleichfunktion nach dem Jahresendabschluss
description: In diesem Artikel wird erläutert, wie Sie die Funktion „Unterschied zwischen Sachkontoausgleich“ verwenden, nachdem der Jahresabschlussprozess des Hauptbuchs ausgeführt wurde.
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
ms.openlocfilehash: 7efa9d652d74bd836f51b5b1c5f6bfaf8934ea40
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2022
ms.locfileid: "9832177"
---
# <a name="awareness-between-ledger-settlement-feature-after-year-end-close"></a>Unterschied zwischen Sachkontoausgleichfunktion nach Jahresendabschluss

[!include [banner](../includes/banner.md)]

## <a name="preparing-for-the-ledger-settlement-awareness-feature-after-year-end-close"></a>Vorbereiten auf den Unterschied zwischen Sachkontoausgleichfunktion nach dem Jahresendabschluss

Eine wichtige Änderung der Funktion **Unterschied zwischen Sachkontoausgleich und Jahresendabschluss** (der **Unterschied** Funktion) besteht darin, dass Die Sachkontoabrechnung nicht über Geschäftsjahre hinweg durchgeführt werden kann. Diese jahresübergreifende Beschränkung ist nur für den Sachkontoausgleich relevant, nicht für den Debitoren- oder Kreditorenausgleich.

Bevor die Funktion **Unterschied** aktiviert wird, darf das Geschäftsjahr, das dem Jahresabschluss unterzogen wird, keine Sachkontobuchungen aufweisen, die über Geschäftsjahre hinweg abgerechnet werden. Insbesondere alle Transaktionen, die in das Geschäftsjahr gebucht wurden, für das Sie den Jahresabschluss ausführen, müssen von Transaktionen abgeglichen werden, die in ein anderes Geschäftsjahr gebucht wurden. Die Buchungen können dann mit Buchungen im selben Geschäftsjahr verrechnet werden.

In diesem Artikel wurden die Schritte beschrieben, die erforderlich sind, um die Sachkontobuchungen, die über Geschäftsjahre hinweg ausgeglichen werden, zu identifizieren, aufzuheben und neu auszugleichen. In dem bereitgestellten Beispiel wurde das Geschäftsjahr 2022 abgeschlossen. Der Schwerpunkt liegt auf der Vorbereitung der Hauptbuchabwicklungstransaktionen lange vor dem Jahresabschluss 2023.

## <a name="example-setup"></a>Beispiel für die Einrichtung

Die folgende Abbildung zeigt die Transaktionen, die für das Hauptkonto 110190 gebucht wurden. Die grün hinterlegten Hauptbuchbuchungen werden im selben Geschäftsjahr abgerechnet und müssen sich nicht ändern. Die Transaktionen in Rot werden im Hauptbuch abgerechnet, aber sie haben Transaktionsdaten in unterschiedlichen Geschäftsjahren. Diese Transaktionen müssen identifiziert werden, und die Hauptbuchabrechnung muss möglicherweise rückgängig gemacht werden.

![Sachkontobuchungen.](./media/afterYEC1.png)

## <a name="example"></a>Beispiel:

Befolgen Sie diese Schritte, wenn Ihre Organisation die Funktion **Unterschied** verwenden möchte, nachdem der Jahresabschluss für das Geschäftsjahr 2022 ausgeführt wurde.

> [!NOTE]
> Der Jahresabschluss für 2022 und frühere Geschäftsjahre muss nur dann erneut ausgeführt werden, wenn neue Transaktionen in das Geschäftsjahr 2022 oder früher gebucht werden. Wenn Sie das folgende Verfahren abschließen, sollten keine neuen Transaktionen in 2022 gebucht werden. Deshalb muss der Jahresabschluss nicht erneut ausgeführt werden.
>
> Sachkontobuchungen, die über Geschäftsjahre hinweg abgerechnet werden, können im Sachkonto abgerechnet bleiben, wenn sie nicht mit einer Buchung abgerechnet werden, die in 2023 oder später gebucht wurde. Wenn Sie beispielsweise Transaktionen in den Jahren 2019 und 2020 abgerechnet haben, können sie abgerechnet bleiben.

1. Schließen Sie den Jahresabschluss für 2022 ab, ohne dass die Funktion **Unterschied** aktiviert ist.
2. Optional: Aktivieren Sie nach Abschluss des Jahresabschlusses für 2022 die Funktion **Unterschied**. Ein Jahresabschluss gilt als abgeschlossen, wenn alle Anpassungen gebucht wurden und der Jahresabschlussprozess nicht erneut ausgeführt wird.

    > [!IMPORTANT]
    > Die **Unterschied** Funktion darf nicht aktiviert werden, wenn der Jahresabschluss für 2022 erneut durchgeführt wird. Wenn Sie die Funktion jetzt aktivieren, haben Sie den Vorteil, dass Sie Benutzer daran hindern, Hauptbuchtransaktionen auszugleichen, die in verschiedenen Geschäftsjahren gebucht wurden.

    Wenn der Jahresabschluss noch nicht abgeschlossen ist, können Sie die nächsten Schritte trotzdem abschließen, ohne die Funktion **Unterschied** zu aktivieren. Sie aktivieren die Funktion wie erwähnt in einem späteren Schritt.

3. Identifizieren Sie auf der Seite **Sachkontoabrechnung** die Gesamtsumme aller Transaktionen, die in den Geschäftsjahren 2022 und 2023 abgerechnet werden. Beachten Sie, dass 2021-Transaktionen, die mit 2022-Transaktionen abgerechnet werden, nicht relevant sind, da 2022 bereits abgeschlossen wurde. Diese Buchungen können ausgeglichen bleiben.

    1. Geben Sie einen Datumsbereich für das gesamte Geschäftsjahr 2022 an. Geben Sie beispielsweise den 1. Januar 2022 bis zum 31. Dezember 2022 an, wenn Sie ein Kalenderjahr als Geschäftsjahr verwenden.
    2. Wählen Sie im Feld **Status** die Option **Ausgeglichen** aus.
    3. Filtern Sie jeweils nach einem Sachkonto.

        - Sie müssen diese Schritte für jedes Sachkonto wiederholen, für das der Sachkontoausgleich erfolgt.
        - Wenn andere Sachkonten nicht mehr für den Sachkontoausgleich eingerichtet sind, müssen Sie sie möglicherweise vorübergehend wieder zur Sachkontoausgleichseinrichtung hinzufügen. Führen Sie dann diese Schritte aus, wenn diese Sachkonten Transaktionen im Jahr 2023 aufweisen, die mit Transaktionen im Jahr 2022 oder früher abgerechnet werden.

    4. Wählen Sie aus oder halten Sie (mit der rechten Maustaste klicken) in die **Status** Spalte und wählen Sie dann nach dieser Spalte gruppieren.
    5. Wählen Sie aus oder halten Sie (mit der rechten Maustaste klicken) in die **Betrag in Buchungswährung** Spalte und wählen Sie dann diese Spalte zusammenrechnen.

        - Wenn Sie Transaktionen erst im Jahr 2022 abgerechnet haben, ist die Summe 0 (Null).
        - Wenn Sie Transaktionen haben, die über Geschäftsjahre hinweg abgerechnet wurden, ist die Summe nicht 0 (Null).

    6. Identifizieren Sie, welche Transaktionen zwischen 2022 und 2023 abgerechnet wurden, indem Sie nach dem Wert **Abrechnungsdatum** filtern. Wenn Sie nach einem Abwicklungsdatum vom 1. Januar 2023 bis zum 31. Dezember 2023 filtern, erhalten Sie eine Gesamtzahl von $700, d. h. die Gesamtzahl der Transaktionen, die in den Jahren 2022 und 2023 im Hauptbuch abgerechnet wurden.

    ![Hauptbuchbuchungen gesamt 2022.](./media/afterYEC2.png)

4. Wiederholen Sie Schritt 3 für das Geschäftsjahr 2023. Die Summe sollte mit der $700 von 2022 übereinstimmen, da keine 2023-Transaktionen gegen 2024-Transaktionen abgerechnet wurden.

    ![Hauptbuchbuchungen gesamt 2023.](./media/afterYEC3.png)

5. Wenn Sie die Funktion **Unterschied** in Schritt 2 aktiviert haben, deaktivieren Sie sie, bevor Sie mit Schritt 6 fortfahren. In den nächsten Schritten stornieren Sie den geschäftsjahresübergreifenden Sachkontoausgleich. Wenn die Funktion **Unterschied** aktiviert ist, kann die Sachkontoabrechnung für das Geschäftsjahr 2022 nicht rückgängig gemacht werden. Daher müssen Sie die Funktion deaktivieren, bevor Sie fortfahren.
6. Nachdem die Funktion **Unterschied** deaktiviert wurde, verwenden Sie dieselben Filter auf der Seite **Hauptbuchabrechnung**, um die Hauptbuchabrechnung von rückgängig zu machen die detaillierten Transaktionen.

    1. Kehren Sie zur Seite **Hauptbuchabrechnung** zurück und filtern Sie nach Transaktionsdaten für 2023. Suchen Sie dann die detaillierten Transaktionen, die die Gesamtsumme von $700 ausmachen. Das Filtern nach diesen Informationen ist möglicherweise nicht einfach. Eventuell müssen Sie die Daten zur Auswertung an Microsoft Excel senden.
    2. Nachdem Sie die Liste der Buchungen haben, wählen Sie die Hauptbuchbuchungen auf der Seite **Hauptbuchausgleich** und dann **Ausgewählt markieren** aus. Sie müssen nicht beide Seiten der Buchhaltungstransaktionen sehen, die abgerechnet wurden. Wenn Sie entweder die Belastung oder die Gutschrift markieren, wird alles, was den gleichen **Abrechnungs-ID** Wert hat, storniert, auch wenn der **markierte Betrag** Wert ist nicht **0** (Null).
    3. Wählen Sie **Markierte Transaktionen stornieren**, um die Transaktionen abzubrechen.

    ![Transaktionen stornieren.](./media/afterYEC4.png)

7. Buchen Sie ein Anpassungshauptbuchblatt, um die Eröffnungsbilanz für 2023 in zwei Beträge aufzuteilen: den Teil, der mit der Buchung für das Geschäftsjahr 2022 ausgeglichen wird, und den Teil, der 2023 noch nicht ausgeglichen wird.

    - **Teil des Eröffnungssaldos, der mit dem Vorjahr verrechnet wird:** Der erste Betrag ist $700, basierend auf den ermittelten Summen, die über die Jahre 2022 und 2023 verrechnet werden.
    - **Teil des Eröffnungssaldos, der nicht mit dem Vorjahr verrechnet wird:** Der zweite Betrag ist die Differenz zwischen dem Eröffnungssaldo und dem ersten Betrag von $525. Der Restbetrag ist $1700 – $700 = $1000.

    Auf diese Weise können Sie die 2023-Transaktionen gegen die $700 abrechnen, die ursprünglich gegen die 2022-Transaktion abgerechnet wurden. Dieser Schritt ist erforderlich, da die Sachkontoabrechnung keine Teilabrechnung zulässt.

    1. Wechseln Sie in das allgemeine Journal und buchen Sie die Anpassung. Ihre Organisation muss basierend auf den im Jahr 2023 offenen Zeiträumen entscheiden, welches Transaktionsdatum verwendet werden soll.
    2. Möglicherweise müssen Sie den Parameter **Manuelle Eingabe nicht zulassen** auf der Seite **Hauptkonto** vorübergehend deaktivieren. Diese Anpassung wird nicht gebucht, wenn das Hauptkonto keine manuelle Eingabe zulässt.

    ![Regulierungen nicht gebucht werden.](./media/afterYEC5.png)

8. Sie können nun die offenen Transaktionen zurücksetzen. Kehren Sie zur Seite **Hauptbuchausgleich** zurück und begrenzen Sie den Datumsbereich auf den 1. Januar 2022 bis zum 31. Dezember 2022. Die folgende Abbildung zeigt die nicht ausgeglichenen Transaktionen, die jetzt vorhanden sind.

    ![Nicht ausgeglichene Buchungen.](./media/afterYEC6.png)

    - Der Eröffnungssaldo von $1,700 kann mit der Anpassung für -1.700 $ verrechnet werden.
    - Die detaillierten Transaktionen, die für -$700 nicht abgerechnet wurden, können mit der Anpassung für $700.00 abgerechnet werden.

9. Aktivieren Sie die Funktion **Unterschied** wieder.
10. Nachdem die Funktion **Unterschied** aktiviert ist, kann die Sachkontoabrechnung nicht über Geschäftsjahre hinweg durchgeführt werden. Möglicherweise müssen Sie das verbleibende Guthaben von $1.000 weiter in kleinere Beträge aufteilen, bevor Sie 2023 mit neuen Transaktionen abrechnen können. Einige Kunden entscheiden sich dafür, dieses Detail in Schritt 8 zu veröffentlichen, wo $1.000 weiter unterteilt wird, um die noch nicht abgerechneten Transaktionen aus dem Jahr 2022 darzustellen. Dieser Ansatz ahmt im Wesentlichen nach, was die Funktion **Unterschied** nur für das aktuelle Jahr tut. Nächstes Jahr erfolgt dies automatisch über die Einstellung **Details beibehalten** in der Einrichtung der Hauptbuchabrechnung.
