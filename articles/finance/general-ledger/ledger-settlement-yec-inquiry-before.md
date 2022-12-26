---
title: Unterschied zwischen Sachkontoausgleichfunktion vor dem Jahresendabschluss mithilfe der Abfrageseite
description: In diesem Artikel wird erläutert, wie Sie die Funktion „Unterschied zwischen Sachkontoausgleichen“ mithilfe der neuen Abfrageseite verwenden, bevor der Jahresabschluss des Hauptbuchs ausgeführt wurde.
author: kweekley
ms.date: 12/15/2022
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
ms.openlocfilehash: b138d2d5e88ff7f2ca2240cf256a4938f55a5606
ms.sourcegitcommit: 9f3a60a583da21382a14f32ce146fc9ce03f2a09
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/15/2022
ms.locfileid: "9853137"
---
# <a name="awareness-between-ledger-settlement-feature-before-year-end-close-using-the-inquiry-page"></a>Unterschied zwischen Sachkontoausgleichfunktion vor dem Jahresendabschluss mithilfe der Abfrageseite

Eine Hauptänderung der Funktion **Unterschied zwischen Sachkontoausgleich und Jahresendabschluss** (der **Unterschied** Funktion) besteht darin, dass Die Sachkontoabrechnung nicht über Geschäftsjahre hinweg durchgeführt werden kann. Diese jahresübergreifende Beschränkung ist nur für den Sachkontoausgleich relevant, nicht für den Debitoren- oder Kreditorenausgleich.

Bevor Sie die Funktion **Unterschied** aktivieren, darf das Geschäftsjahr, das dem Jahresabschluss unterzogen wird, keine Sachkontobuchungen aufweisen, die über Geschäftsjahre hinweg abgerechnet werden. Insbesondere alle Transaktionen, die in das Geschäftsjahr gebucht wurden, für das Sie den Jahresabschluss ausführen, müssen von Transaktionen abgeglichen werden, die in ein anderes Geschäftsjahr gebucht wurden. Die Buchungen können dann mit Buchungen im selben Geschäftsjahr verrechnet werden.

In diesem Artikel wurden die Schritte beschrieben, die erforderlich sind, um Sachkontobuchungen, die über Geschäftsjahre hinweg ausgeglichen werden, zu identifizieren, aufzuheben und neu auszugleichen. In dem bereitgestellten Beispiel wurde das Geschäftsjahr 2021 abgeschlossen, und Sie bereiten den Jahresabschluss für das Geschäftsjahr 2022 vor.

Ab Microsoft Dynamics 365 Finance Version 10.0.29 können Sie Hauptbuchtransaktionen mithilfe einer neuen verfügbaren Abfrageseite identifizieren, aufheben und zurücksetzen. Wenn Sie derzeit nicht Finance Version 10.0.29 oder höher verwenden, finden Sie die Schritte zum Identifizieren, Aufheben und Zurücksetzen der Hauptbuchtransaktionen in den folgenden Artikeln:

- [Unterschied zwischen Sachkontoausgleichfunktion vor dem Jahresendabschluss](ledger-settle-yec.md)
- [Unterschied zwischen Sachkontoausgleichfunktion nach Jahresendabschluss](ledger-settle-yec-after.md)

Weitere Informationen zum neuen Abfragefenster finden Sie unter [Abfrage zur Abrechnung des Sachkontos](ledger-settlement-inquiry.md). 

## <a name="example-setup"></a>Beispiel für die Einrichtung

Die folgende Abbildung zeigt die Transaktionen, die für das Hauptkonto 110200 gebucht wurden. Die grün hinterlegten Hauptbuchbuchungen wurden im selben Geschäftsjahr über das Hauptkonto abgerechnet und müssen sich nicht ändern. Die Transaktionen in Rot wurden im Hauptbuch abgerechnet, aber sie haben Transaktionsdaten in unterschiedlichen Geschäftsjahren. Diese Transaktionen müssen identifiziert werden, und die Hauptbuchabrechnung muss möglicherweise rückgängig gemacht werden.

![Gebuchte Sachkontobuchungen.](./media/ledgersettlement.png)

## <a name="example"></a>Beispiel:

Befolgen Sie diese Schritte, wenn Ihre Organisation die Funktion **Unterschied** verwenden möchte, bevor Sie den Jahresabschluss für das Geschäftsjahr 2022 ausführen.

> [!NOTE]
> Der Jahresabschluss für 2021 und frühere Geschäftsjahre muss nur dann erneut ausgeführt werden, wenn neue Transaktionen in das Geschäftsjahr 2021 oder früher gebucht werden. Wenn Sie das folgende Verfahren abschließen, werden keine neuen Transaktionen in 2021 gebucht. Deshalb muss der Jahresabschluss nicht erneut ausgeführt werden.
>
> Sachkontobuchungen, die über Geschäftsjahre hinweg abgerechnet werden, können im Sachkonto abgerechnet bleiben, wenn sie nicht mit einer Buchung abgerechnet werden, die in 2022 (das Jahr des Abschlusses) oder später gebucht wurde. Wenn Sie beispielsweise Transaktionen in den Jahren 2019 und 2020 abgerechnet haben, können sie abgerechnet bleiben.

1. Aktivieren Sie **nicht** die Funktion **Unterschied**.
2. Wählen Sie auf der Seite **Sachkontoabrechnungen** die Option **Jahresübergreifende Ausgleiche prüfen**.
3. Identifizieren Sie alle Transaktionen, die in andere Geschäftsjahre gebucht, aber mit Transaktionen verrechnet wurden, die in 2022 gebucht wurden.

    1. Wählen Sie das Geschäftsjahr 2022 aus, für das Sie den Jahresabschlussprozess durchführen möchten.
    2. Wählen Sie einen Wert im Feld **Finanzdimensionssatz** aus, um die Finanzdimensionen anzuzeigen, die Sie für das Sachkonto anzeigen möchten. Das Hauptkonto wird immer angezeigt, auch wenn der ausgewählte Dimensionssatz kein Hauptkonto enthält.
    3. Wählen Sie **Transaktionen anzeigen**.

    Die Abfrageseite zeigt alle Transaktionen für alle Sachkonten (auch wenn sie sich nicht mehr in der Sachkontoabrechnungseinstellung befinden) aus allen anderen Geschäftsjahren, die mit Transaktionen abgerechnet werden, die in 2022 gebucht wurden. Es werden drei verschiedene Sachkonten angezeigt.

    ![Jahresübergreifende Ausgleiche für 2022 prüfen](./media/review-cross-year.png)

3. Wählen und halten Sie (oder klicken Sie mit der rechten Maustaste) im Raster und wählen Sie dann **Alle Zeilen exportieren**. Diese Zeilen sind alle Transaktionen, die von den Transaktionen im Jahr 2022 abgeglichen werden müssen, bevor der Jahresabschluss ausgeführt werden kann. Sie möchten die detaillierte Transaktionsliste, um später die Transaktionen korrekt zurückrechnen zu können.
4. Beachten Sie die Geschäftsjahre, für die die Transaktionen gebucht wurden. In diesem Beispiel gibt es Transaktionen in 2021 und 2023.
5. Ändern Sie auf der Abfrageseite das Geschäftsjahr in 2021, das erste Geschäftsjahr, das Transaktionen enthält, die mit Transaktionen von 2022 verrechnet wurden.
6. Filtern Sie nach der Spalte **Transaktionsdatum**, sodass nur Transaktionen enthalten sind, die in das Jahr 2022 gebucht wurden. Diese Transaktionen sind die detaillierten Transaktionen aus dem Jahr 2022, die mit Transaktionen im Jahr 2021 verrechnet wurden.
7. Wählen und halten Sie (oder klicken Sie mit der rechten Maustaste) im Raster und wählen Sie dann **Alle Zeilen exportieren**.

    > [!IMPORTANT]
    > In den folgenden Schritten werden diese Transaktionen verrechnet und dann gegen Transaktionen im Jahr 2022 neu verrechnet. Es ist wichtig, dass Sie dieses Detail in Excel pflegen.

    ![Jahresübergreifende Ausgleiche für 2021 prüfen](./media/review-cross-year.png)

8. Ändern Sie auf der Abfrageseite das Geschäftsjahr in 2023, das nächste Geschäftsjahr, das Transaktionen enthält, die mit Transaktionen von 2022 verrechnet wurden. 
9. Filtern Sie nach der Spalte **Transaktionsdatum**, sodass nur Transaktionen enthalten sind, die in das Jahr 2022 gebucht wurden. Diese Transaktionen sind die detaillierten Transaktionen aus dem Jahr 2023, die mit Transaktionen im Jahr 2022 verrechnet wurden. 
10. Wählen und halten Sie (oder klicken Sie mit der rechten Maustaste) im Raster und wählen Sie dann **Alle Zeilen exportieren**.

    > [!IMPORTANT]
    > In den folgenden Schritten werden diese Transaktionen verrechnet und dann gegen Transaktionen im Jahr 2022 neu verrechnet. Es ist wichtig, dass Sie dieses Detail in Excel pflegen.

    ![Jahresübergreifende Ausgleiche für 2023 prüfen](./media/filter-transactions.png)

11. Wiederholen Sie die vorherigen Schritte für jedes Geschäftsjahr mit Transaktionen, die mit Transaktionen im Jahr 2022 verrechnet wurden. Exportieren Sie die detaillierten Transaktionen immer nach Excel.

    Nachdem alle detaillierten Transaktionen aus den Jahren 2021 und 2023 nach Excel exportiert wurden, können Sie die Transaktionen über die neue Anfrageseite ins Wanken bringen.

12. Ändern Sie das Geschäftsjahr zu 2022.
13. Wählen Sie alle Datensätze im Raster aus und wählen Sie dann **Markierte Datensätze aufheben** aus. Der Ausgleich für alle ausgewählten Transaktionen im Raster wird aufgehoben.

    Es werden zwei Warnmeldungen angezeigt, um sicherzustellen, dass die Transaktionsdetails nach Excel exportiert werden, bevor die Transaktionen nicht abgewickelt werden. Wenn Sie versehentlich Hauptbuchtransaktionen aufheben, bevor Sie die Details an Excel senden, gibt es keine Möglichkeit, die Aufhebung rückgängig zu machen.

    ![Beunruhigende Cross-Settlement-Transaktionen.](./media/revert-unsettle.png)

14. Verwenden Sie die Excel-Daten, um den Gesamtbetrag der Transaktionen in den Jahren 2021 und 2023 zu finden, die gegen Transaktionen im Jahr 2022 abgerechnet wurden. In diesem Beispiel belaufen sich die Transaktionen für 2021 auf $525 und die Transaktionen für 2023 auf $700.
15. Buchen Sie ein Anpassungshauptbuchblatt, um die Eröffnungsbilanz für 2022 in zwei Beträge aufzuteilen: den Teil, der für das Geschäftsjahr 2021 ausgeglichen wird, und den Teil, der 2022 noch nicht ausgeglichen wurde.

    - **Teil des Eröffnungssaldos, der mit dem Vorjahr verrechnet wurde:** Der erste Betrag ist $525, basierend auf den ermittelten Summen, die über die Jahre 2021 und 2022 verrechnet wurden.
    - **Teil des Eröffnungssaldos, der nicht mit dem Vorjahr verrechnet wurde:** Der zweite Betrag ist die Differenz zwischen dem Eröffnungssaldo und dem ausgeglichenen Betrag von $525. Der Restbetrag ist $1025 – $525 = $500.

    Auf diese Weise können Sie die 2022-Transaktionen gegen die $525 abrechnen, die ursprünglich gegen die 2021-Transaktion abgerechnet wurden. Dieser Schritt ist erforderlich, da die Sachkontoabrechnung keine Teilabrechnung zulässt.

    1. Wechseln Sie in das allgemeine Journal und buchen Sie die Anpassung. Ihre Organisation muss basierend auf den offenen Zeiträumen entscheiden, welches Transaktionsdatum verwendet werden soll. Diese Transaktionen wurden möglicherweise unter Verwendung eines Abwicklungsdatums im Januar oder Februar 2022 abgerechnet, aber die Anpassung muss möglicherweise im Dezember gebucht werden, wenn dies der einzige offene Zeitraum ist.
    2. Möglicherweise müssen Sie den Parameter **Manuelle Eingabe nicht zulassen** für Konto 110200 auf der Seite **Hauptkonto** vorübergehend deaktivieren. Diese Anpassung wird nicht gebucht, wenn das Hauptkonto keine manuelle Eingabe zulässt.

    ![Buchen einer Anpassungshauptbuch.-Blatt.](./media/not-post.png)

16. Sie können nun die offenen Transaktionen zurücksetzen. Kehren Sie zur Seite **Hauptbuchabrechnungen** zurück, geben Sie einen Datumsbereich vom 1. Januar bis 31. Dezember 2022 an und filtern Sie nach dem Hauptkonto 110200. Verwenden Sie dann die detaillierten Transaktionen, die Sie nach Excel exportiert haben, um die spezifischen Transaktionen zu finden, die zurückgesetzt werden müssen. Die folgende Abbildung zeigt die nicht ausgeglichenen Transaktionen, die jetzt vorhanden sind.

    ![Nicht ausgeglichene Transaktionen.](./media/updated-unsettled.png)

    - Der Eröffnungssaldo von $1,025 kann mit der Anpassung für -1.025 $ verrechnet werden.
    - Die detaillierten Transaktionen, die für -$400, -$50 und -$75 nicht abgerechnet wurden, können mit der Anpassung für $25 abgerechnet werden.

17. Aktivieren Sie die Funktion **Unterschied**. Sie können nun den Jahresabschluss ausführen.

    - Bevor Sie den Jahresabschluss ausführen, sollten Sie in Betracht ziehen, die Option **Details beibehalten** in der Sachkontoausgleichseinstellung für alle Bilanzkonten auszuwählen. Weitere Informationen finden Sie unter [Unterschied zwischen Sachkontoausgleich und Jahresendabschluss](awareness-between-ledger-settlement-year-end-close.md).
    - Wenn Sie mit dem Jahresabschluss für 2022 beginnen und noch Transaktionen gefunden wurden, die über Geschäftsjahre hinweg abgerechnet werden, werden Sie vom Jahresabschlussprozess sofort benachrichtigt. Diese Situation kann auftreten, wenn Benutzer Transaktionen über Geschäftsjahre hinweg abgerechnet haben, nachdem Sie den vorherigen Schritt abgeschlossen haben.
    - Wenn die Transaktionen für 2021 und 2022 noch abgerechnet werden, müssen Sie die Funktion **Unterschied** erneut deaktivieren und dann die vorherigen Schritte wiederholen, um diese Transaktionen abzubrechen. Dieser Ansatz ist erforderlich, da das Jahr 2021 abgeschlossen ist und Transaktionen in einem abgeschlossenen Geschäftsjahr nicht verrechnet werden können.
    - Wenn Transaktionen für 2022 und 2023 noch abgerechnet werden, müssen Sie nicht die Funktion **Unterschied** deaktivieren. Da weder 2022 noch 2023 geschlossen sind, können Sie die vorherigen Schritte verwenden, um die Transaktionen zu verunsichern.

18. Sie können die $700-Transaktion aus dem Jahr 2023 mit den detaillierten Transaktionen verrechnen, die als Eröffnungssalden im Jahr 2023 übernommen wurden. Diese Transaktion wird nicht mit der ursprünglichen Transaktion im Jahr 2022 verrechnet.

Nachdem der Jahresabschluss für 2022 erfolgreich durchgeführt wurde, können Sie die Funktion **Unterschied** von nun an aktiviert lassen.
