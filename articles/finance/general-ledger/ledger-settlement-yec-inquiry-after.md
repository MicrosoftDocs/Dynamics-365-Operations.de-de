---
title: Unterschied zwischen Sachkontoausgleichfunktion nach dem Jahresendabschluss mithilfe der Abfrageseite
description: In diesem Artikel wird erläutert, wie Sie die Funktion „Unterschied zwischen Sachkontoausgleichen“ mithilfe der neuen Abfrageseite verwenden, nachdem der Jahresabschluss des Hauptbuchs ausgeführt wurde.
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
ms.openlocfilehash: 921d2a17409ae10cd9c22eeca11557ba1248b9bc
ms.sourcegitcommit: 9f3a60a583da21382a14f32ce146fc9ce03f2a09
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/15/2022
ms.locfileid: "9853130"
---
# <a name="awareness-between-ledger-settlement-feature-after-year-end-close-using-the-inquiry-page"></a>Unterschied zwischen Sachkontoausgleichfunktion nach dem Jahresendabschluss mithilfe der Abfrageseite

Eine Hauptänderung der Funktion **Unterschied zwischen Sachkontoausgleich und Jahresendabschluss** (der **Unterschied** Funktion) besteht darin, dass Die Sachkontoabrechnung nicht über Geschäftsjahre hinweg durchgeführt werden kann. Diese jahresübergreifende Beschränkung ist nur für den Sachkontoausgleich relevant, nicht für den Debitoren- oder Kreditorenausgleich.

Bevor Sie die Funktion **Unterschied** aktivieren, darf das Geschäftsjahr, das dem Jahresabschluss unterzogen wird, keine Sachkontobuchungen aufweisen, die über Geschäftsjahre hinweg abgerechnet werden. Insbesondere alle Transaktionen, die in das Geschäftsjahr gebucht wurden, für das Sie den Jahresabschluss ausführen, müssen von Transaktionen abgeglichen werden, die in ein anderes Geschäftsjahr gebucht wurden. Die Buchungen können dann mit Buchungen im selben Geschäftsjahr verrechnet werden.

In diesem Artikel wurden die Schritte beschrieben, die erforderlich sind, um die Sachkontobuchungen, die über Jahre hinweg ausgeglichen werden, zu identifizieren, aufzuheben und neu auszugleichen. In dem bereitgestellten Beispiel wurde das Geschäftsjahr 2022 abgeschlossen. Der Schwerpunkt liegt auf der Vorbereitung der Hauptbuchabwicklungstransaktionen vor dem Jahresabschluss 2023.

Ab Microsoft Dynamics 365 Finance Version 10.0.29 können Sie Hauptbuchtransaktionen mithilfe einer neuen verfügbaren Abfrageseite identifizieren, aufheben und zurücksetzen. Wenn Sie derzeit nicht Microsoft Dynamics 365 Finance Version 10.0.29 oder höher verwenden, finden Sie die Schritte zum Identifizieren, Aufheben und Zurücksetzen der Hauptbuchtransaktionen in den folgenden Artikeln:

- [Unterschied zwischen Sachkontoausgleichfunktion vor dem Jahresendabschluss](ledger-settle-yec.md)
- [Unterschied zwischen Sachkontoausgleichfunktion nach Jahresendabschluss](ledger-settle-yec-after.md)

Weitere Informationen zum neuen Abfragefenster finden Sie unter [Abfrage zur Abrechnung des Sachkontos](ledger-settlement-inquiry.md). 

## <a name="example-setup"></a>Beispiel für die Einrichtung

Die folgende Abbildung zeigt die Transaktionen, die für das Hauptkonto 110200 gebucht wurden. Die grün hinterlegten Hauptbuchbuchungen wurden im selben Geschäftsjahr über das Hauptkonto abgerechnet und müssen sich nicht ändern. Die Transaktionen in Rot wurden im Hauptbuch abgerechnet, aber sie haben Transaktionsdaten in unterschiedlichen Geschäftsjahren. Diese Transaktionen müssen identifiziert werden, und die Hauptbuchabrechnung muss möglicherweise rückgängig gemacht werden.

![Gebuchte Sachkontobuchungen.](./media/excel.png)

## <a name="example"></a>Beispiel:

Befolgen Sie diese Schritte, wenn Ihre Organisation die Funktion **Unterschied** verwenden möchte, nachdem der Jahresabschluss für das Geschäftsjahr 2022 ausgeführt wurde.

> [!NOTE]
> Der Jahresabschluss für 2022 und frühere Geschäftsjahre muss nur dann erneut ausgeführt werden, wenn neue Transaktionen in das Geschäftsjahr 2022 oder früher gebucht werden. Wenn Sie das folgende Verfahren abschließen, werden keine neuen Transaktionen in 2022 gebucht. Deshalb muss der Jahresabschluss nicht erneut ausgeführt werden.
>
> Sachkontobuchungen, die über Geschäftsjahre hinweg abgerechnet werden, können im Sachkonto abgerechnet bleiben, wenn sie nicht mit einer Buchung abgerechnet werden, die in 2022 oder später gebucht wurde. Wenn Sie beispielsweise Transaktionen in den Jahren 2019 und 2020 abgerechnet haben, können sie abgerechnet bleiben.

1. Schließen Sie den Jahresabschluss für 2022 ab, ohne dass die Funktion **Unterschied** aktiviert ist.
2. Identifizieren Sie alle Transaktionen, die in andere Geschäftsjahre gebucht, aber mit Transaktionen verrechnet wurden, die in 2023 gebucht wurden (das nächste Geschäftsjahr, das abgeschlossen wird).

    > [!NOTE]
    > 2021-Transaktionen, die mit 2022-Transaktionen abgerechnet wurden, nicht relevant sind, da das Jahr bereits 2022 geschlossen wurde. Diese Buchungen können ausgeglichen bleiben.

    1. Wählen Sie auf der Seite **Sachkontoabrechnungen** die Option **Jahresübergreifende Ausgleiche prüfen**.
    2. Wählen Sie das Geschäftsjahr 2023 aus, für das Sie als nächstes den Jahresabschlussprozess durchführen möchten.
    3. Wählen Sie einen Wert im Feld **Finanzdimensionssatz** aus, um die Finanzdimensionen anzuzeigen, die Sie für das Sachkonto anzeigen möchten. Das Hauptkonto wird immer angezeigt, auch wenn der ausgewählte Dimensionssatz kein Hauptkonto enthält.
    4. Wählen Sie **Transaktionen anzeigen**.

    Auf der Abfrageseite werden alle Transaktionen aus anderen Geschäftsjahren angezeigt, die mit Transaktionen verrechnet werden, die im Jahr 2023 gebucht wurden.

    ![Jahresübergreifende Ausgleiche für 2023 prüfen](./media/2023-cross-settlement.png)

3. Wählen und halten Sie (oder klicken Sie mit der rechten Maustaste) im Raster und wählen Sie dann **Alle Zeilen exportieren**. Diese Zeilen sind alle Transaktionen, die von den Transaktionen im Jahr 2022 abgeglichen werden müssen, bevor der Jahresabschluss für das nächste Jahr (2023) ausgeführt werden kann. Sie möchten eine Aufzeichnung dieser Transaktionen.

    Nachdem alle detaillierten Transaktionen aus dem Jahr 2022 nach Excel exportiert wurden, können Sie die Transaktionen über die Anfrageseite ins Wanken bringen.

4. Wählen Sie alle Datensätze im Raster aus und wählen Sie dann **Markierte Datensätze aufheben** aus. Der Ausgleich für alle ausgewählten Transaktionen im Raster wird aufgehoben.

    Es werden zwei Warnmeldungen angezeigt, um sicherzustellen, dass die Transaktionsdetails nach Excel exportiert werden, bevor die Transaktionen nicht abgewickelt werden. Wenn Sie versehentlich Hauptbuchtransaktionen aufheben, bevor Sie die Details an Excel senden, gibt es keine Möglichkeit, die Aufhebung rückgängig zu machen.

    ![Jahresübergreifende Ausgleiche aufheben.](./media/revert-settlement.png)

5. Verwenden Sie die Excel-Daten, um den Gesamtbetrag der Transaktionen im Jahr 2022 zu finden, die mit Transaktionen im Jahr 2023 abgerechnet wurden. In diesem Beispiel sind die Transaktionen für 2023 insgesamt $700.
6. Buchen Sie ein Anpassungshauptbuchblatt, um die Eröffnungsbilanz für 2022 in zwei Beträge aufzuteilen: den Teil, der mit der Buchung für das Geschäftsjahr 2022 ausgeglichen wird, und den Teil, der 2023 noch nicht ausgeglichen wurde.

    - **Teil des Eröffnungssaldos, der mit dem Vorjahr verrechnet wurde:** Der erste Betrag ist $700, basierend auf den ermittelten Summen, die über die Jahre 2021 und 2022 verrechnet wurden.
    - **Teil des Eröffnungssaldos, der nicht mit dem Vorjahr verrechnet wurde:** Der zweite Betrag ist die Differenz zwischen dem Eröffnungssaldo und dem ausgeglichenen Betrag von $700. Der Restbetrag ist $1.700 – $700 = $1.000.

    Auf diese Weise können Sie die 2023-Transaktionen gegen die $700 abrechnen, die ursprünglich gegen die 2022-Transaktion abgerechnet wurden. Dieser Schritt ist erforderlich, da die Sachkontoabrechnung keine Teilabrechnung zulässt.

    1. Wechseln Sie in das allgemeine Journal und buchen Sie die Anpassung. Ihre Organisation muss basierend auf den im Jahr 2023 offenen Zeiträumen entscheiden, welches Transaktionsdatum verwendet werden soll.
    2. Möglicherweise müssen Sie den Parameter **Manuelle Eingabe nicht zulassen** auf der Seite **Hauptkonto** vorübergehend deaktivieren. Diese Anpassung wird nicht gebucht, wenn das Hauptkonto keine manuelle Eingabe zulässt.

    ![Buchen einer Anpassungshauptbuch.-Blatt.](./media/no-manual4.png)

7. Sie können nun die offenen Transaktionen zurücksetzen. Kehren Sie zur Seite **Hauptbuchausgleiche** zurück und begrenzen Sie den Datumsbereich auf den 1. Januar bis zum 31. Dezember 2023. Verwenden Sie dann die detaillierten Transaktionen, die Sie nach Excel exportiert haben, um die spezifischen Transaktionen zu finden, die zurückgesetzt werden müssen. Die folgende Abbildung zeigt die nicht ausgeglichenen Transaktionen, die jetzt vorhanden sind.

    ![Nicht ausgeglichene Buchungen für 2023.](./media/2023-unsettled5.png)

    - Der Eröffnungssaldo von $1,700 kann mit der Anpassung für -1.700 $ verrechnet werden.
    - Die detaillierten Transaktionen, die für -$700 nicht abgerechnet wurden, können mit der Anpassung für $700.00 abgerechnet werden.

8. Aktivieren Sie die Funktion **Unterschied**. Sie können nun den Jahresabschluss ausführen.

    - Bevor Sie den Jahresabschluss für 2023 ausführen, sollten Sie in Betracht ziehen, die Option **Details beibehalten** in der Sachkontoausgleichseinstellung für alle Bilanzkonten auszuwählen. Weitere Informationen finden Sie unter [Unterschied zwischen Sachkontoausgleich und Jahresendabschluss](awareness-between-ledger-settlement-year-end-close.md).
    - Wenn Sie mit dem Jahresabschluss für 2023 beginnen und noch Transaktionen gefunden wurden, die über Geschäftsjahre hinweg abgerechnet werden, werden Sie vom Jahresabschlussprozess sofort benachrichtigt. Diese Situation kann auftreten, wenn Benutzer Transaktionen über Geschäftsjahre hinweg abgerechnet haben, bevor die Funktion **Unterschied** aktiviert wurde.
    - Wenn die Transaktionen für 2022 und 2023 noch abgerechnet werden, müssen Sie die Funktion **Unterschied** erneut deaktivieren und dann die vorherigen Schritte wiederholen, um diese Transaktionen abzubrechen. Dieser Ansatz ist erforderlich, da das Jahr 2022 abgeschlossen ist und Transaktionen in einem abgeschlossenen Geschäftsjahr nicht verrechnet werden können.

Nachdem der Jahresabschluss für 2022 erfolgreich durchgeführt wurde, können Sie die Funktion **Unterschied** von nun an aktiviert lassen.
