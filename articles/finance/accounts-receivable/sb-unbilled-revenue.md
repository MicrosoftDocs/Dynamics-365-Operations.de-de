---
title: Nicht abgerechneter Umsatzerlös
description: In diesem Thema wird erklärt, wie Sie Artikel und Konten einrichten, um die Funktion für nicht abgerechnete Umsatzerlöse in der Abonnementabrechnung zu verwenden.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: a70786291822a85ec41c98ab8ce706f2ad79b08d
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8691244"
---
# <a name="unbilled-revenue"></a>Nicht abgerechneter Umsatzerlös

In diesem Thema wird die Funktion für nicht abgerechnete Umsatzerlöse beschrieben, mit der Sie die Beträge für ganze Abrechnungszeitpläne in die Bilanz aufnehmen können. Diese Beträge werden in ein Konto für nicht abgerechnete Umsatzerlöse und ein Gegenkonto für nicht abgerechnete Umsatzerlöse aufgenommen, und der Vertrag wird in Raten abgerechnet.

## <a name="set-up-unbilled-revenue"></a>Nicht abgerechnete Umsatzerlöse einrichten

Gehen Sie zum Einrichten nicht abgerechneter Umsatzerlöse folgendermaßen vor.

- Legen Sie auf der Seite **Wiederkehrende Abrechnungsparameter für Vertrag** die Felder im Abschnitt **Nicht abgerechneter Umsatzerlös** fest.
- Die Funktion für nicht abgerechnete Umsatzerlöse kann für Artikel verwendet werden, bei denen das Feld **Artikeltyp** auf **Standard** festgelegt ist. Es kann auch für Stundungspositionen verwendet werden. Um nicht abgerechnete Umsatzerlöse mit der kurzfristigen Funktion zu nutzen, richten Sie die kurzfristigen Optionen auf der Seite **Wiederkehrende Abrechnungsparameter für Vertrag** ein.

Gehen Sie zum Einrichten von Artikeln für die Verwendung nicht abgerechneter Umsatzerlöse folgendermaßen vor.

1. Auf der Seite **Einstellungen für nicht abgerechneten Umsatzerlös** auf der Registerkarte **Artikel** wählen Sie **Hinzufügen** aus.
2. Wählen Sie in der neuen Position unter **Artikelcode** den Artikelcode aus.
3. Wählen Sie im Feld **Artikelrelation** die Artikelrelation aus.
4. Wiederholen Sie diese Schritte, um weitere Positionen hinzuzufügen.
5. Wählen Sie **Speichern** aus.

Gehen Sie zum Einrichten von Artikeln und der Konten für nicht abgerechneten Umsatzerlös folgendermaßen vor.

1. Auf der Seite **Einstellungen für nicht abgerechneten Umsatzerlös** auf der Registerkarte **Konten** wählen Sie **Hinzufügen** aus.
2. Wählen Sie in der neuen Position unter **Artikelcode** den Artikelcode aus.
3. Wählen Sie im Feld **Artikelrelation** die Artikelrelation aus.
4. Wählen Sie die Konten für nicht abgerechnete Umsatzerlöse, nicht abgerechneten Rabatt und nicht fakturierte Umsatzerlöse. Um die Kurzzeitkonten nutzen zu können, müssen Sie das Feld **Kurzfristige nicht abgerechnete Methode** auf **Rollierende Zeiträume** oder **Festes Jahr** auf der Seite **Wiederkehrende Abrechnungsparameter für Vertrag** festlegen.
5. Wiederholen Sie diese Schritte, um weitere Positionen hinzuzufügen.
6. Wählen Sie **Speichern** aus.

## <a name="use-unbilled-revenue"></a>Nicht abgerechneten Umsatzerlös verwenden

1. Erstellen Sie einen Abrechnungszeitplan auf der Seite **Alle Abrechnungszeitpläne**.
2. Wenn der Artikel noch nicht für die Verwendung von nicht abgerechnetem Umsatzerlös eingerichtet ist, aktivieren Sie das Kontrollkästchen **Nicht abgerechneter Umsatzerlös** in der Abrechnungszeitplanposition.
3. Legen Sie die Option **Nicht abgerechneter Umsatzerlös** auf **Ja** fest. Prüfen und bearbeiten Sie dann ggf. die Konten für nicht abgerechnete Umsatzerlöse, Rabatt und nicht fakturierte Umsatzerlöse.
4. Wählen Sie auf dem Abrechnungszeitplan unter **Verarbeitung nicht abgerechneter Umsatzerlöse** die Option **Journaleintrag erstellen**, um den ersten Journaleintrag für nicht abgerechnete Umsatzerlöse zu erstellen. Dieser Schritt muss abgeschlossen sein, bevor der Abrechnungszeitplan in Rechnung gestellt wird.
5. Nachdem der erste Journaleintrag erstellt wurde, wählen Sie **Rechnung generieren**, um Aufträge zu erstellen und die Rechnungen für die Abrechnungszeitpläne zu buchen.
6. Nachdem die Rechnungen gebucht wurden, können Sie die Prüfungsinformationen auf der Registerkarte **Verlängerungen** der Seite **Alle Abrechnungszeitpläne** überprüfen.

### <a name="milestone-billing"></a>Meilenstein Abrechnung

Die Abrechnung nach Meilenstein funktioniert mit nicht abgerechneten Umsatzerlös unter den folgenden Bedingungen:

- Wenn der übergeordnete Meilensteinartikel noch nicht fakturiert ist (das Kontrollkästchen **Nicht abgerechneter Umsatzserlös** ist aktiviert) und die untergeordneten Meilensteinartikel abgerechnet werden (das Kontrollkästchen **Nicht abgerechneter Umsatzserlös** ist deaktiviert), müssen das Start- und Enddatum für den übergeordnete Artikel angegeben werden. Diese Daten werden verwendet, um den ersten Journaleintrag zu erstellen.
- Wenn der übergeordnete Meilensteinartikel noch nicht fakturiert ist (das Kontrollkästchen **Nicht abgerechneter Umsatzserlös** ist deaktiviert) und die untergeordneten Meilensteinartikel abgerechnet werden (das Kontrollkästchen **Nicht abgerechneter Umsatzserlös** ist aktiviert), muss das Enddatum nur für die untergeordneten Artikel angegeben werden, für die Sie den ersten Journaleintrag erstellen möchten.

Jeder untergeordnete Meilensteinartikel kann separat verarbeitet werden. Die Enddaten können angegeben werden, wenn Sie bereit sind, den ersten Journaleintrag zu erstellen.

> [!NOTE]
> Wenn der erste Journaleintrag für den übergeordneten oder die untergeordneten Meilensteinartikel bereits erstellt wurde oder eine Rechnung erstellt wurde, können die Start- und Enddaten nicht bearbeitet werden.

### <a name="unbilled-revenue-with-straight-line-deferrals"></a>Nicht abgerechneter Umsatzerlös mit linearen Stundungen

Führen Sie die folgenden Schritte aus, um nicht abgerechnete Umsatzerlöse mit linearen Stundungszeitplänen zu verwenden.

1. Erstellen Sie einen Abrechnungszeitplan auf der Seite **Alle Abrechnungszeitpläne**.
2. Fügen Sie einen Artikel zu den Abrechnungszeitplanpositionen hinzu.
3. Wählen Sie **Stundungen** für die Position aus.
4. Führen Sie auf der Seite **Transaktionsstundung** die folgenden Schritte aus:

    1. Legen Sie die Option **Verzögert** auf **Ja** fest.
    2. Ändern Sie die Konten nach Wunsch.
    3. Wählen Sie im Abschnitt **Zeitplan** die Option **Linear** und bearbeiten Sie andere Werte nach Bedarf.
    4. Wählen Sie **OK** aus.

5. Wählen Sie **Nicht abgerechneter Umsatzerlös** für die Position und folgen Sie dann diesen Schritten:

    1. Legen Sie die Option **Nicht abgerechneter Umsatzerlös** auf **Ja** fest.
    2. Wählen Sie die Konten für die Verwendung von Umsatzerlösen, Rabatt und Umsatzerlösen (Gegenkonto).

6. Wählen Sie auf dem Abrechnungszeitplan unter **Verarbeitung nicht abgerechneter Umsatzerlöse** die Option **Journaleintrag erstellen**. Verwenden Sie alternativ die Seite **Massenverarbeitung nicht abgerechneter Umsatzerlöse**, um den Journaleintrag zu erstellen.
7. Der Stundungszeitplan wurde erstellt. Sie können die Details auf der Seite **Alle Stundungszeitpläne** prüfen. Nachdem der Stundungszeitplan erstellt wurde, können Sie verschiedene Werte für die Abrechnungszeitplanpositionen bearbeiten. Beispielsweise können Sie den Stückpreis, die Menge oder Daten bearbeiten.

### <a name="unbilled-revenue-with-event-based-deferrals"></a>Nicht abgerechneter Umsatzerlös mit ereignisbasierte Stundungen

Führen Sie die folgenden Schritte aus, um nicht abgerechnete Umsatzerlöse mit ereignisbasierten Stundungszeitplänen zu verwenden.

1. Erstellen Sie einen Abrechnungszeitplan auf der Seite **Alle Abrechnungszeitpläne**.
2. Fügen Sie einen Artikel zu den Abrechnungszeitplanpositionen hinzu.
3. Wählen Sie **Stundungen** für die Position aus.
4. Führen Sie auf der Seite **Transaktionsstundung** die folgenden Schritte aus:

    1. Legen Sie die Option **Verzögert** auf **Ja** fest.
    2. Ändern Sie die Konten nach Wunsch.
    3. Wählen Sie im Abschnitt **Zeitplan** die Optionen **Ereignisbasiert**, **Vorlage**, **Zuordnungstyp** und **Ablaufkonto**.
    4. Wählen Sie **OK** aus.

5. Wählen Sie **Nicht abgerechneter Umsatzerlös** für die Position und folgen Sie dann diesen Schritten:

    - Legen Sie die Option **Nicht abgerechneter Umsatzerlös** auf **Ja** fest.
    - Wählen Sie die Konten für die Verwendung von Umsatzerlösen, Rabatt und Umsatzerlösen (Gegenkonto).

6. Wählen Sie auf dem Abrechnungszeitplan unter **Verarbeitung nicht abgerechneter Umsatzerlöse** die Option **Journaleintrag erstellen**. Verwenden Sie alternativ die Seite **Massenverarbeitung nicht abgerechneter Umsatzerlöse**, um den Journaleintrag zu erstellen.
7. Der Stundungszeitplan wurde erstellt. Sie können die Details auf der Seite **Alle Stundungszeitpläne** prüfen. Nachdem der Stundungszeitplan erstellt wurde, können Sie verschiedene Werte für die Abrechnungszeitplanpositionen bearbeiten. Beispielsweise können Sie den Stückpreis, die Menge oder Daten bearbeiten. Der Stundungszeitplan wird basierend auf den neuen Werten neu berechnet.

Die Verteilungen werden basierend auf dem ausgewählten Zuteilungstyp neu berechnet (**Prozentsatz**, **Vollendungsgrad in Prozent** oder **Gleiche Beträge**). Für den Zuteilungstyp **Variable Beträge** wird die Verteilung basierend auf dem prozentualen Äquivalent des Anfangswerts für das Ereignis neu berechnet. Beispiel: Der ursprüngliche Stückpreis ist beispielsweise 100,00 $ und der Prozentsatz des Anfangswerts ist 55,00 $ (55 Prozent). Wenn der Stückpreis auf 200,00 $ geändert wird, wird der variable Betrag des Ereignisses 110,00 $ (immer noch 55 Prozent).

> [!NOTE]
> Wenn Stundungszeitplanpositionen erkannt wurden, kann die Abrechnungszeitplanposition nicht bearbeitet werden. Um die Position zu bearbeiten, müssen Sie zuerst die erkannten Positionen stornieren. Die Abrechnungszeitplanposition kann dann aktualisiert werden.

### <a name="unbilled-revenue-and-top-billing"></a>Nicht abgerechneter Umsatzerlös und Top-Abrechnung

Ein Abrechnungszeitplan wird für drei Jahre eingegeben, und die Rechnungen werden jährlich über einen Zeitraum von drei Jahren in Rechnung gestellt. Der gesamte Vertragsbetrag wird auf dem Konto für nicht abgerechneten Umsatzerlös erfasst, aus dem jährliche Rechnungen erstellt werden. Das Gegenkonto ist das Konto für Umsatzerlöse oder verzögerte Umsatzerlöse.

Beachten Sie, dass Top-Abrechnung und nicht abgerechneter Umsatzerlös nicht zusammen funktionieren, da im Hauptbuch Abstimmungsprobleme auftreten können. Zum Beispiel ist auf der Seite **Artikelgruppeneinstellungen** die Artikelgruppe A so eingerichtet, dass das Feld **Anzahl oberer Positionen** auf **2** eingestellt ist. Auf der Seite **Abrechnungszeitpläne** werden drei Artikel hinzugefügt. Alle drei Artikel gehören zur Artikelgruppe A. Wenn der erste Journaleintrag für die Funktion für nicht abgerechnete Umsatzerlöse erstellt wird, wird der Betrag für alle drei Artikel auf das Konto für nicht abgerechneten Umsatzerlös verarbeitet. Bei der Erstellung der Rechnung für den Abrechnungszeitplan werden nur die Beträge für die beiden obersten Artikel berücksichtigt. Daher stimmt der Rechnungsbetrag nicht mit dem Betrag überein, der auf dem Konto für nicht abgerechneten Umsatzerlös verarbeitet wurde, und im Hauptbuch treten Abstimmungsprobleme auf.

Wenn Sie nicht abgerechneten Umsatzerlös verwenden möchten, lassen Sie die Seite **Artikelgruppeneinstellungen** leer oder richten Sie alle Artikelgruppen so ein, dass das Feld **Anzahl oberer Positionen** auf **0** (Null) eingestellt ist. Wenn Sie die Top-Abrechnung verwenden möchten, sind keine Aktionen für nicht abgerechneten Umsatzerlös verfügbar.

### <a name="examples"></a>Beispiele

Ab Version 10.0.27 wird ein neues Konto eingeführt, wenn nicht abgerechneter Umsatzerlös verwendet wird. Wenn der erste Prozess **Journaleintrag erstellen** gebucht wird, erfolgt die Gutschrift auf ein neues Gegenkonto für nicht abgerechneten Umsatzerlös. Dieses Konto wird anstelle des Konto für Umsatzerlös verwendet, da derselbe Wert bei der Fakturierung des Abrechnungszeitplans storniert werden muss. Treten Kurs- oder Rundungsdifferenzen auf, können sich die Beträge unterscheiden, die während des Prozess **Rechnung generieren** berechnet werden. Dieses Verhalten stellt sicher, dass der Nettobetrag der Konten 0 (Null) ist.

Dieses Beispiel zeigt, wie Sie nicht abgerechneten Umsatzerlös verwenden, um den gesamten Betrag eines Vertrags in der Bilanz als nicht abgerechneten Umsatzerlös zu erfassen. Die andere Seite des Eintrags ist der nicht abgerechnete Umsatzerlös, Gegenkonto. Wenn Sie dem Kunden eine Rechnung stellen, werden der nicht abgerechnete Umsatzerlös und der nicht abgerechnete Umsatzerlös, Gegenkonto, storniert. Die Umsatzerkennung erfolgt entweder zum Zeitpunkt der Rechnungsstellung oder gemäß dem festgelegten Stundungserkennungszeitplan.

#### <a name="assumptions"></a>Voraussetzungen

- Am 1. Januar des laufenden Jahres unterschreibt ein Kunde einen Dreijahresvertrag für 390 $.
- Der Vertrag umfasst zwei Teile: Lizenzen und einen Wartungsvertrag.
- Der Verkaufspreis der Lizenzgebühr beträgt 300 $, und dem Kunden wird am 1. Januar jedes Vertragsjahres 100 $ in Rechnung gestellt. Die Lizenzgebühr von 300 $ wird bei Vertragsunterzeichnung als Umsatzerlös verrechnet.
- Der Verkaufspreis der Wartungsgebühr beträgt 90 $, und dem Kunden wird am 1. Januar jedes Vertragsjahres 30 $ in Rechnung gestellt. Die 90 $ Wartungsgebühr wird gestundet und 2,50 $ wird jeden Monat der Vertragslaufzeit anerkannt.
- Dem Kunden wird 130 $ zu Beginn (1. Januar) jedes der drei Vertragsjahre in Rechnung gestellt.

#### <a name="steps"></a>Schritte

1. Richten Sie die beiden freigegebenen Artikel als nicht abgerechnete Artikel ein. Verwenden Sie die Seite **Einstellungen für nicht abgerechneten Umsatzerlös**, um die Artikel und Konten einzurichten, die nicht abgerechneten Umsatzerlös verwenden.
2. In diesem Beispiel wird die Wartungsgebühr gestundet. Der Artikel erfordert eine Stundungsvorlage, die auf der Seite **Stundungsvorlagen** eingerichtet wird. Die Vorlage hat die Zeitraumfrequenz **Monatlich** und eine Anerkennungsdauer von 36 Monaten. Daher ist der Umsatzerlös pro Monat 2,50 $.
3. Stellen Sie auf der Seite **Standardmäßig verzögerte Artikel** das Feld **Wartungsgebühr** auf **Stundbarer Artikel**. Dieser und der nächste Schritt bewirken, dass die Wartungsgebühr zurückgestellt wird, wenn sie verkauft oder in einen Abrechnungszeitplan aufgenommen wird.
4. Wählen Sie **Standardstundungseinstellungen** \> **Vorlage** und fügen Sie den Artikel für die Wartungsgebühr und die lineare Vorlage aus Schritt 2 hinzu. Die Wartungsgebühr wird mit einem 36-monatigen Stundungszeitplan verknüpft.
5. Erstellen Sie einen Abrechnungszeitplan, der die beiden nicht abgerechneten Artikel enthält. Der Abrechnungszeitplan für den Vertrag wird mit den folgenden Artikeln eingerichtet.

    | Element | Startdatum | Enddatum | Betrag | Abrechnungsfrequenz | Stundungsartikel | Nicht abgerechneter Umsatzerlös | Description |
    |---|---|---|---|---|---|---|---|
    | Lizenz | 1. Januar, CY | 31. Dezember, CY+2 | 100,00 $ | Jährlich | Nein | Ja | Dem Kunden wird jedes Jahr 100,00 $ in Rechnung gestellt. Die Gesamtsumme von 300,00 $ wird im Voraus als nicht abgerechneter Umsatzerlös in der Bilanz und als Umsatzerlös in der Gewinn- und Verlustrechnung erfasst. Jede Rechnung reduziert den nicht abgerechneten Betrag. |
    | Wartung | 1. Januar, CY | 31. Dezember, CY+2 | 30,00 $ | Jährlich | Ja | Ja | Dem Kunden wird jedes Jahr 30,00 $ in Rechnung gestellt. Die Gesamtsumme von 90,00 $ wird im Voraus als nicht abgerechneter Umsatzerlös und verzögerter Umsatzerlös in der Bilanz erfasst. Jede Rechnung reduziert den nicht abgerechneten Betrag. Der verzögerte Umsatzerlös wird monatlich über 36 Monate erkannt. |

6. Verwenden Sie auf der Seite **Alle Abrechnungszeitpläne** den Prozess **Journaleintrag erstellen**, um den Vertragswert als nicht abgerechneten Umsatzerlös in die Bilanz zu buchen.

Es werden zwei Journaleinträge erstellt, einer für jede Position im Abrechnungszeitplan.

| Konto für nicht abgerechneten Umsatzerlös | Gegenkonto für nicht fakturierten Umsatzerlös | Sollbetrag | Habenbetrag |
|---|---|---|---|
| Konto für nicht abgerechneten Umsatzerlös | | 300,00 $ | |
| | Gegenkonto für nicht fakturierten Umsatzerlös | | 300,00 $ |

| Konto für nicht abgerechneten Umsatzerlös | Verzögerter Umsatzerlös | Sollbetrag | Habenbetrag |
|---|---|---|---|
| Konto für nicht abgerechneten Umsatzerlös | | 90,00 $ | |
| |Verzögerter Wartungsumsatzerlös | | 90,00 $ |

Der erste Journaleintrag wird auf ein Gegenkonto für nicht abgerechnete Umsatzerlöse gebucht, die zweite auf ein Konto für verzögerte Umsatzerlöse. Wenn die Abrechnungsposition sowohl nicht abgerechneten Umsatzerlös als auch verzögerten Umsatzerlös aufweist, wird das Konto für verzögerte Umsatzerlöse verwendet, nicht der nicht abgerechnete Umsatzerlös, Gegenkonto. Der Vertrag sieht vor, dass die Rechnung für den Kunden zu Beginn eines jeden Jahres erstellt wird. Verwenden Sie den Prozess **Rechnung generieren** zum Erstellen der Rechnung. Wenn die Rechnung erstellt wird, werden die folgenden Journaleinträge erstellt.

| Hauptkonto | Konto für nicht abgerechneten Umsatzerlös | Sollbetrag | Habenbetrag |
|---|---|---|---|
| Nicht abgerechneter Umsatzerlös, Gegenkonto | | 100,00 $ | |
| | Konto für nicht abgerechneten Umsatzerlös | | 100,00 $ |
| Debitorenkonten | | 100,00 $ | |
| | Konto für Umsatzerlöse | | 100,00 $ |

| Hauptkonto | Konto für nicht abgerechneten Umsatzerlös | Sollbetrag | Habenbetrag |
|---|---|---|---|
| Konto für verzögerte Wartungsumsatzerlöse | | 30,00 $ | |
| | Konto für nicht abgerechneten Umsatzerlös | | 30,00 $ |
| Debitorenkonten | | 30,00 $ | |
| | Konto für verzögerte Wartungsumsatzerlöse | | 30,00 $ |

Derselbe Journaleintrag wird durch Rechnungen erstellt, die zu Beginn der nächsten zwei Jahre gebucht werden. Der Nettobetrag des Kontos für verzögerte Umsatzerlöse ist 0 (Null), da es keine Rundungs- oder Wechselkursdifferenzen gibt. Der verzögerte Umsatzerlös muss genau so storniert werden, wie er im Prozess **Journaleintrag erstellen** gutgeschrieben wurde. Da Umsatzerlöse noch gestundet sind und erst später erfasst werden, erfolgt die Gutschrift auf dem Konto für verzögerte Umsatzerlöse erneut.

Im letzten Schritt wird jeden Monat der Erfassungsjournaleintrag erstellt, um den verzögerten Wartungsgebührenumsatzerlös zu erfassen. Der Journaleintrag kann auf der Seite **Erkennungsverarbeitung** erstellt werden. Alternativ kann es auch durch Auswählen von **Erkennen** für die Positionen auf der Seite **Stundungszeitplan** erstellt werden.

| Konto für verzögerte Umsatzerlöse | Konto für Umsatzerlöse | Sollbetrag | Habenbetrag |
|---|---|---|---|
| Verzögerter Wartungsumsatzerlös | | 2,50 $ | |
| | Wartungsumsatzerlös | | 2,50 $ |

Dieser Journaleintrag wird jedes Mal erstellt, wenn der Anerkennungsprozess für diesen gestundeten Artikel durchgeführt wird (insgesamt 36 Mal).

#### <a name="short-term-fixed-year"></a>Kurzfristig: Festes Jahr

Sie können nicht abgerechnete Umsatzerlöse zusammen mit der kurzfristigen Funktion nutzen, indem Sie das Feld **Kurzfristig nicht abgerechnet** auf der Seite **Wiederkehrende Abrechnungsparameter für Vertrag** einstellen. Das folgende Beispiel zeigt die Berechnungen, die durchgeführt werden, wenn nicht abgerechneter Umsatzerlös zusammen mit der kurzfristigen nicht abgerechneten Methode **Festes Jahr** verwendet wird.

Es wird ein Abrechnungszeitplan mit den folgenden Kriterien erstellt:

- **Startdatum:** 1. Juni 2020
- **Enddatum:** 31. Dezember 2021
- **Einzelpreis:** 100 $
- **Frequenz:** Monatlich

Auf der Seite **Alle Abrechnungszeitpläne** wird der erste Journaleintrag vom Prozess **Journaleintrag erstellen** erstellt. Die aktuellen kurzfristigen und langfristigen Beträge werden wie folgt berechnet:

- **Aktueller kurzfristiger nicht abgerechneter Umsatzerlösbetrag:** 700 $
- **Aktueller langfristiger nicht abgerechneter Umsatzerlösbetrag:** 1.200 $

Die Rechnung wird für den Abrechnungszeitraum vom 1. Juni 2020 bis 30. November 2020 erstellt. Die aktuellen kurzfristigen und langfristigen Beträge werden wie folgt berechnet:

- **Aktueller kurzfristiger nicht abgerechneter Umsatzerlösbetrag:** 100 $
- **Aktueller langfristiger nicht abgerechneter Umsatzerlösbetrag:** 1.200 $

Die Rechnung wird für den Abrechnungszeitraum vom 1. Dezember 2020 bis 31. Dezember 2020 erstellt. Die aktuellen kurzfristigen und langfristigen Beträge werden wie folgt berechnet:

- **Aktueller kurzfristiger nicht abgerechneter Umsatzerlösbetrag:** 1.200 $
- **Aktueller langfristiger nicht abgerechneter Umsatzerlösbetrag:** 0 $

#### <a name="short-term-rolling-periods"></a>Kurzfristig: Rollierende Zeiträume

Sie können nicht abgerechnete Umsatzerlöse zusammen mit der kurzfristigen Funktion nutzen, indem Sie die kurzfristig nicht abgerechnete Methode auf der Seite **Wiederkehrende Abrechnungsparameter für Vertrag** einstellen. Das folgende Beispiel zeigt die Berechnungen, die durchgeführt werden, wenn nicht abgerechneter Umsatzerlös zusammen mit der kurzfristigen nicht abgerechneten Methode **Rollierende Zeiträume** verwendet wird.

Es wird ein Abrechnungszeitplan mit den folgenden Kriterien erstellt:

- **Startdatum:** 1. Juni 2020
- **Enddatum:** 31. Dezember 2021
- **Einzelpreis:** 100 $
- **Frequenz:** Monatlich

Auf der Seite **Alle Abrechnungszeitpläne** wird der erste Journaleintrag vom Prozess **Journaleintrag erstellen** erstellt. Die aktuellen kurzfristigen und langfristigen Beträge werden wie folgt berechnet:

- **Aktueller kurzfristiger nicht abgerechneter Umsatzerlösbetrag:** 1.200 $
- **Aktueller langfristiger nicht abgerechneter Umsatzerlösbetrag:** 700 $

Die Rechnung wird für den Abrechnungszeitraum vom 1. Juni 2020 bis 30. November 2020 erstellt. Die aktuellen kurzfristigen und langfristigen Beträge werden wie folgt berechnet:

- **Aktueller kurzfristiger nicht abgerechneter Umsatzerlösbetrag:** 1.200 $
- **Aktueller langfristiger nicht abgerechneter Umsatzerlösbetrag:** 100 $

Die Rechnung wird für den Abrechnungszeitraum vom 1. Dezember 2020 bis 31. Dezember 2020 erstellt. Die aktuellen kurzfristigen und langfristigen Beträge werden wie folgt berechnet:

- **Aktueller kurzfristiger nicht abgerechneter Umsatzerlösbetrag:** 1.200 $
- **Aktueller langfristiger nicht abgerechneter Umsatzerlösbetrag:** 0 $

### <a name="items-with-revenue-allocation"></a>Artikel mit Umsatzerlöszuteilung

Einem Abrechnungszeitplan werden zwei Artikel mit unterschiedlichen Abrechnungsintervallen hinzugefügt. Beide verwenden nicht abgerechnete Umsatzerlöse und sind stundbare Artikel.

- **Artikelnummer 1000:** Surface Pro 128 GB

    - **Abrechnungsfrequenz:** Einmal
    - **Einzelpreis:** 1.500 $
    - **Eigenständiger Verkaufspreis:** 1.600 $
    - **Vertragsumsatzerlös:** 1.465,26 $

- **Artikelnummer S0021:** Versicherung, die zusammen mit der Artikelnummer 1000 verkauft wird

    - **Abrechnungsfrequenz:** Monatlich für 12 Monate
    - **Einzelpreis:** 20 $ pro Monat
    - **Eigenständiger Verkaufspreis:** 25 $
    - **Vertragsumsatzerlös:** 264,74 $

Da beide Artikel nicht abgerechneten Umsatzerlös und Umsatzerlöszuteilung verwenden, ist der Gesamtvertragsbetrag in der Verlängerungsposition 0 (Null). Die Spalte **Vertragsumsatzerlös** wird hinzugefügt und zeigt den Betrag des Vertragsumsatzerlöses an.

Die folgende Tabelle zeigt den ersten Journaleintrag für die Artikel und die Rechnung.

| Konto für nicht abgerechneten Umsatzerlös | Konto für verzögerte Umsatzerlöse | Sollbetrag | Habenbetrag |
|---|---|---|---|
| **Artikel 1000 Journaleintrag** | | | |
| Belastung Konto für nicht abgerechneten Umsatzerlös (401250) | | 1.465,26 $ | |
| | Gutschrift Konto für verzögerte Umsatzerlöse (250600) | | 1.465,26 $ |
| **Artikel 0021 Journaleintrag** | | | |
| Belastung Konto für nicht abgerechneten Umsatzerlös (401250) | | 274,74 $ | |
| | Gutschrift Konto für verzögerte Umsatzerlöse (250600) | | 274,74 $ |
| **Rechnung** | | | |
| | Gutschrift Konto für nicht abgerechnete Umsatzerlös | | 1.465,26 $ |
| | Gutschrift Konto für nicht abgerechnete Umsatzerlös | | 274,74 $ |
| Belastung AR-Konto (130100) | | 1.488,16 $ | |

#### <a name="changes-to-the-billing-schedule-line-billing-detail-line-or-revenue-allocation"></a>Änderungen an der Abrechnungszeitplanposition, Abrechnungsdetailposition oder Umsatzerlöszuteilung

Wenn der Stückpreis oder die Menge geändert wird, muss der Betrag des Vertragsumsatzerlöses für jeden Artikel, der Teil der Umsatzerlöszuteilung ist, aktualisiert werden. Daher wird der Journaleintrag neu berechnet.

Beispielsweise wird der Stückpreis für Artikel 1000 von 1.500 $ zu 1.600 $ geändert. In diesem Fall wird der Betrag des Vertragsumsatzerlöses automatisch als 1.549,47 $ neu berechnet. Der Vertragsumsatzerlös für Artikel S0021 wird als 290,53 $ neu berechnet.

Wenn die Änderung bestätigt und festgeschrieben ist, werden die ersten Journaleinträge für beide Artikel storniert und neue Journaleinträge erstellt:

- **Artikel 1000:** Der erste Journaleintrag von 1.465,26 $ wird storniert. Ein neuer Journaleintrag von 1.549,47 $ wird erstellt.
- **Artikel S0021:** Der erste Journaleintrag von 274,74 $ wird storniert. Ein neuer Journaleintrag von 290,53 $ wird erstellt.

#### <a name="termination"></a>Beendigung

Artikel S0021 hat ein Startdatum im Januar 2020 und ein Enddatum im Dezember 2020, wird aber im Juni 2020 beendet. Der Betrag des Vertragsumsatzerlöses für beide Artikel muss neu berechnet werden:

- **Artikel 1000:** Der Vertragsumsatzerlös wird als 1.567,67 $ neu berechnet.
- **Artikel S0021:** Der Vertragsumsatzerlös wird als 124,00 $ neu berechnet.

Für die beendete Position wird eine Regulierungsjournaleintrag erstellt. Der Journaleintrag für die Position, die zu derselben MEA-Nummer (Anordnung für mehrere Elemente) gehört, wird storniert und ein neuer Journaleintrag wird erstellt:

- **Artikel 1000:** Der erste Journaleintrag von 1.465,26 $ wird storniert. Ein Regulierungserfassungseintrag von 1.549,47 $ wird erstellt.
- **Artikel S0021:** Der erste Journaleintrag von 274,74 $ wird storniert. Ein neuer Journaleintrag von 124,00 $ wird erstellt.
