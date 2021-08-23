---
title: Dioppelte Berichterstellung
description: Dieses Thema führt Sie durch ein Beispiel, das zeigt, wie Sie die Anforderungen sowohl für die Berichterstattung nach dem International Financial Reporting Standard (IFRS) als auch für die gesetzliche Berichterstattung im Analgenleasing erfüllen können.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseBookMaster
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 406fbb53fc4cd17a7c257b5f5463227118c9051f44d81db000fbe87dca142efe
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6767055"
---
# <a name="dual-reporting"></a>Dioppelte Berichterstellung

[!include [banner](../includes/banner.md)]

Dieses Thema führt Sie durch ein Beispiel, das zeigt, wie Sie die Anforderungen sowohl für die Berichterstattung nach dem International Financial Reporting Standard (IFRS) als auch für die gesetzliche Berichterstattung im Analgenleasing erfüllen können. Sie müssen mit Buchungsbenenen in Microsoft Dynamics 365 Finance vertraut sein. Dies erleichtert das Verständnis des Beispiels.

## <a name="example"></a>Beispiel

Das folgende Beispiel berücksichtigt einen Mietvertrag nach italienischer gesetzlicher Berichterstattung, wobei sowohl die Cash-Basis-Methode als auch die IFRS-Berichtsmethode angewendet werden. Das Unternehmen muss drei Bücher erstellen, um sowohl die italienischen gesetzlichen Anforderungen als auch die Anforderungen von IFRS 16 zu berücksichtigen. Für IFRS 16 ist ein Buch erforderlich, für die gesetzlichen Anforderungen ein Buch und für die automatische Stornierung gesetzlicher Buchungen ein Buch. Die Bücher sind wie in den folgenden Tabellen gezeigt aufgebaut.

**IFRS 16-Buch**

Das IFRS 16-Buch ist so angelegt, dass es dem Rechnungslegungsstandard IFRS 16 entspricht. Alle Einträge, die in diesem Buch gebucht werden, werden auf einer benutzerdefinierten Ebene gebucht.

| Name                                    | Beschreibung    |
|-----------------------------------------|----------------|
| Buchtyp                               | IFRS 16        |
| Buchbeschreibung                        | IFRS 16        |
| Buchungsebene                           | Benutzerdefinierte Ebene 1 |
| Mietvertragstyp                              | Finance        |
| Buchhaltungsframework                    | IFRS 16        |
| Einrichtung von Mietdauer/Nutzungsdauer         | 0,00           |
| Einrichtung von Barwert/Anlagenzeitwert | 0,00           |
| Kurzfristiger Schwellenwert                    | 12             |
| Schwellenwert für geringen Wert                     | 5,000.00       |
| An Kreditor bezahlen                           | Nr.             |

**Gesetzliches Buch**

Das gesetzliche Buch ist ein Cash-Basis-Buch, in dem das Unternehmen die Mietkosten als den Betrag an Bargeld verbucht, der jeden Monat für die Miete gezahlt wird. Dieses Buch enthält keine Nutzungsrechte (ROU) für Vermögenswerte oder Mietverbindlichkeiten.

| Name                                    | Beschreibung |
|-----------------------------------------|-------------|
| Buchtyp                               | Gesetzlich   |
| Buchbeschreibung                        | Lokale GAAP  |
| Buchungsebene                           | Aktuell     |
| Mietvertragstyp                              | Automatisch   |
| Buchhaltungsframework                    | Einnahmen/Ausgaben  |
| Einrichtung von Mietdauer/Nutzungsdauer         | 0,00        |
| Einrichtung von Barwert/Anlagenzeitwert | 0,00        |
| Kurzfristiger Schwellenwert                    | 0           |
| Schwellenwert für geringen Wert                     | 0           |
| An Kreditor bezahlen                           | Nr.          |

**Gesetzliches Stornobuch**

Das gesetzliche Stornobuch ist wie das gesetzliche Buch aufgebaut.

| Name                                    | Beschreibung                    |
|-----------------------------------------|--------------------------------|
| Buchtyp                               | Gesetzliches Buch – Stornobuchungen           |
| Buchbeschreibung                        | Buch für die Rückbuchung des gesetzlichen Buchs |
| Buchungsebene                           | Benutzerdefinierte Ebene 1                 |
| Mietvertragstyp                              | Automatisch                      |
| Buchhaltungsframework                    | Einnahmen/Ausgaben                     |
| Einrichtung von Mietdauer/Nutzungsdauer         | 0,00                           |
| Einrichtung von Barwert/Anlagenzeitwert | 0,00                           |
| Kurzfristiger Schwellenwert                    | 0                              |
| Schwellenwert für geringen Wert                     | 0                              |
| An Kreditor bezahlen                           | Nr.                             |

In diesem Beispiel wurde ein Mietvertrag mit den folgenden Einstellungen auf den Registerkarten **Allgemein** und **Zahlungspläne** erstellt.

**Registerkarte „Allgemeines“**

| Feld                      | Wert            |
|----------------------------|------------------|
| Zinssatz für Neukredit | 5 %               |
| Anfangsdatum          | 1/1/2020         |
| Mietvertragsgruppe                | Gebäude        |
| Lieferant                     | 1001             |
| Zeitwert der Anlage    | 245,000          |
| Nutzungsdauer für Anlagen          | 120              |
| Annuitätstyp               | Normale Annuität |
| Aufzinsungsintervall       | Monatlich          |

**Registerkarte „Zahlungsplanpositionen“**

| Feld             | Wert      |
|-------------------|------------|
| Startdatum        | 1/1/2020   |
| Periodenintervall   | Monate     |
| Perioden           | 24         |
| Enddatum          | 31/12/2020 |
| Zahlungshäufigkeit | Monatlich    |
| Zahlungsbetrag    | 1.000      |

Um diesen Mietvertrag in zwei Frameworks zu berücksichtigen, verwenden Sie eine aktuelle Buchungsebene und eine benutzerdefinierte Buchungsebene. Die folgende Tabelle zeigt ein Beispiel für jeden Journaleintrag, der erforderlich ist, um die Finanzdaten unter den einzelnen Berichtsstandards fair darzustellen. Anschließend wird eine detaillierte Beschreibung jedes Journaleintrags für den ersten Monat des Mietvertrags bereitgestellt.

<table>
<thead>
<tr>
<th rowspan='3'>Kontonummer</th>
<th rowspan='3'>Beschreibung</th>
<th colspan='3'>Gesetzliches Buch (aktuelle Ebene)</th>
<th rowspan='3'>Aktuelle Ebene insgesamt</th>
<th>Stornobuch (benutzerdefinierte Ebene)</th>
<th colspan='4'>IFRS 16-Buch (benutzerdefinierte Ebene)</th>
<th rowspan='3'>Aktuelle Ebene + benutzerdefinierte Ebene insgesamt</th>
</tr>
<tr>
<th>JE-100</th>
<th>JE-110</th>
<th>JE-120</th>
<th>JE-130</th>
<th>JE-140</th>
<th>JE-150</th>
<th>JE-160</th>
<th>JE-170</th>
</tr>
<tr>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
</tr>
</thead>
<tbody>
<tr>
<td>1</td>
<td>Mietvertragsausgaben</td>
<td>1,000.00</td>
<td></td>
<td></td>
<td>1,000.00</td>
<td>-1.000,00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>2</td>
<td>Bankgebühr</td>
<td></td>
<td>3.00</td>
<td></td>
<td>3.00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>3.00</td>
</tr>
<tr>
<td>3</td>
<td>MwSt.-Ausgaben</td>
<td></td>
<td>5.00</td>
<td></td>
<td>5.00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>5.00</td>
</tr>
<tr>
<td>4</td>
<td>Clearingkonto</td>
<td>-1.000,00</td>
<td>1,000.00</td>
<td></td>
<td>0,00</td>
<td>1,000.00</td>
<td></td>
<td>-1.000,00</td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>5</td>
<td>Kreditorenkonten</td>
<td></td>
<td>-1.008,00</td>
<td>1,008.00</td>
<td>0,00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>6</td>
<td>Nutzungsrecht am Leasingobjekt</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
<td></td>
<td>22,794.00</td>
<td></td>
<td></td>
<td></td>
<td>22,793.90</td>
</tr>
<tr>
<td>7</td>
<td>Finanzierungsleasingsverpflichtung</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
<td></td>
<td>-22.794,00</td>
<td>1,000.00</td>
<td>-94,97</td>
<td></td>
<td>-21.888,87</td>
</tr>
<tr>
<td>8</td>
<td>Zinsausgaben</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
<td></td>
<td></td>
<td></td>
<td>94.97</td>
<td></td>
<td>94.97</td>
</tr>
<tr>
<td>9</td>
<td>Bargeld</td>
<td></td>
<td></td>
<td>-1.008,00</td>
<td>-1.008,00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>-1.008,00</td>
</tr>
<tr>
<td>10</td>
<td>Abschreibungsausgaben</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>949.75</td>
<td>949.75</td>
</tr>
<tr>
<td>11</td>
<td>Kumulierte Abschreibung</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>-949,75</td>
<td>-949,75</td>
</tr>
</tbody>
</table>

Wie die vorstehende Tabelle zeigt, müssen drei Bücher sowohl nach der gesetzlichen Berichterstattung als auch nach der IFRS-Berichterstattung ausgewiesen werden.

- Das gesetzliche Buch erfasst die Mietzahlung gemäß den Regeln für die Barabrechnung unter der aktuellen Ebene.
- Das gesetzliche Stornobuch storniert die gesetzlichen Journaleinträgen.
- Das IFRS 16-Buch erstellt die Journaleinträgen, die nach IFRS 16 erforderlich sind.

Sie müssen einen Mietvertrag nur einmal abschließen. Sie können dann die Seite **Bücher** öffnen, um alle Bücher zu sehen, die mit dem Mietvertrag verbunden sind.

> [!NOTE]
> Wenn Sie die Bücher erstellen, müssen alle drei mit demselben Mietvertragsdatensatz verknüpft sein.

Der erste Journaleintrag erfasst die Mietkosten im gesetzlichen Buch. Sie können die Zahlungen entweder in einem Batch oder durch Auswahl des Zahlungsplans im gesetzlichen Buch erstellen.

In diesem Beispiel wird der folgende Journaleintrag für das gesetzliche Buch aus dem Zahlungsplan erstellt.

### <a name="lease-payment--1312020--je-100"></a>Mietzahlung – 31.01.2020 – JE 100

| Kontenart | Kontonummer | Ebene   | Kontobeschreibung | Belastung    | Gutschrift   |
|--------------|----------------|---------|---------------------|----------|----------|
| Unternehmen       | 1              | Aktuell | Mietvertragsausgaben       | 1,000.00 |          |
| Unternehmen       | 4              | Aktuell | Clearingkonto    |          | 1,000.00 |

Ein Kreditorenbuchhalter verwendet die Standardfunktionalität von Dynamics 365, um eine Rechnung für die Zahlung des Mietvertrags außerhalb des Anlagenleasings zu erstellen. Anstatt jedoch **Mietaufwand** als Debitkonto auszuwählen, wählt der Kreditorenbuchhalter ein Verrechnungskonto aus, um den folgenden Eintrag zu generieren.

### <a name="ap-process--1312020--je-110"></a>AP-Prozess – 31.01.2020 – JE 110

| Kontenart | Kontonummer | Ebene   | Kontobeschreibung | Belastung    | Gutschrift   |
|--------------|----------------|---------|---------------------|----------|----------|
| Unternehmen       | 4              | Aktuell | Clearingkonto    | 1,000.00 |          |
| Unternehmen       | 2              | Aktuell | Bankgebühr            | 3.00     |          |
| Unternehmen       | 3              | Aktuell | MwSt.-Ausgaben         | 5.00     |          |
| Lieferant       | 5              | Aktuell | Kreditorenkonten    |          | 1,008.00 |

Wenn die Abrechnung an den Verkäufer ausgestellt wird, folgen Sie dem regulären Zahlungsvorgang. Während dieses Vorgangs wird der folgende Journaleintrag generiert.

### <a name="cash-payment--1312020--je-120"></a>Barzahlung – 31.01.2020 – JE 120

| Kontenart | Kontonummer | Ebene   | Kontobeschreibung | Belastung    | Gutschrift   |
|--------------|----------------|---------|---------------------|----------|----------|
| Lieferant       | 5              | Aktuell | Kreditoren    | 1,008.00 |          |
| Bank         | 9              | Aktuell | Bargeld                |          | 1,008.00 |

Zu diesem Zeitpunkt haben Sie diesen Mietvertrag gemäß den gesetzlichen Meldepflichten vollständig bilanziert und können mithilfe der aktuellen Ebene einen Probesaldo erstellen. Das System gibt eine Testbilanz mit den folgenden Zahlen zurück.

<table>
<thead>
<tr>
<th rowspan='3'>Kontonummer</th>
<th rowspan='3'>Beschreibung</th>
<th colspan='3'>Gesetzliches Buch (aktuelle Ebene)</th>
<th rowspan='3'>Aktuelle Ebene insgesamt</th>
</tr>
<tr>
<th>JE-100</th>
<th>JE-110</th>
<th>JE-120</th>
</tr>
<tr>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
</tr>
</thead>
<tbody>
<tr>
<td>1</td>
<td>Mietvertragsausgaben</td>
<td>1,000.00</td>
<td></td>
<td></td>
<td>1,000.00</td>
</tr>
<tr>
<td>2</td>
<td>Bankgebühr</td>
<td></td>
<td>3.00</td>
<td></td>
<td>3.00</td>
</tr>
<tr>
<td>3</td>
<td>MwSt.-Ausgaben</td>
<td></td>
<td>5.00</td>
<td></td>
<td>5.00</td>
</tr>
<tr>
<td>4</td>
<td>Clearingkonto</td>
<td>-1.000,00</td>
<td>1,000.00</td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>5</td>
<td>Kreditorenkonten</td>
<td></td>
<td>-1.008,00</td>
<td>1,008.00</td>
<td>0,00</td>
</tr>
<tr>
<td>6</td>
<td>Nutzungsrecht am Leasingobjekt</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>7</td>
<td>Finanzierungsleasingsverpflichtung</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>8</td>
<td>Zinsausgaben</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>9</td>
<td>Bargeld</td>
<td></td>
<td></td>
<td>-1.008,00</td>
<td>-1.008,00</td>
</tr>
<tr>
<td>10</td>
<td>Abschreibungsausgaben</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>11</td>
<td>Kumulierte Abschreibung</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
</tbody>
</table>

Wenn Sie die IFRS 16-Zahlen verwenden möchten, um denselben Probesaldo zu erstellen, müssen die gesetzlichen Buchungsführungsjournaleinträge storniert und die IFRS 16-Journaleinträge gebucht werden. Um die gesetzlichen Journaleinträge zu stornieren, enthält dieses Beispiel ein gesetzliches Stornobuch, das den gleichen Aufbau wie das gesetzliche Buch hat, jedoch ein entgegengesetztes Buchungsprofil aufweist. Zum Beispiel *belastet* das gesetzliche Buch ein Mietaufwandskonto, aber im Stornobuch wird in diesem Konto ein *Haben* verbucht. Diese Beziehungen lassen sich leicht in den Buchungen für das Anlagenleasing auf dem Konto **Parameter für das Anlagenleasing** auf der Seite (**Anlagenleasing \> Einrichtung \> Parameter für das Anlagenleasing**) definieren.

Wenn derselbe Prozess, der für das gesetzliche Buch verwendet wurde, für das Stornobuch verwendet wird, wird der folgende Journaleintrag erstellt. Der Unterschied besteht darin, dass das Stornobuch die Stornobuchungen aus dem gesetzlichen Buch bucht. Die Stornoeinträge werden auch auf der benutzerdefinierten Ebene vorgenommen. Wenn auf der aktuellen Ebene ein Testhaben ausgeführt wird, sind die Stornojournaleinträge nicht enthalten.

### <a name="lease-payment--1312020--je-130"></a>Mietzahlung – 31.01.2020 – JE 130

| Kontenart | Kontonummer | Ebene  | Kontobeschreibung | Belastung    | Gutschrift   |
|--------------|----------------|--------|---------------------|----------|----------|
| Unternehmen       | 4              | Benutzerdefiniert | Clearingkonto    | 1,000.00 |          |
| Unternehmen       | 1              | Benutzerdefiniert | Mietvertragsausgaben       |          | 1,000.00 |

Nachdem Sie die gesetzlichen Journaleinträge entfernt haben, buchen Sie alle Journaleinträge , die nach IFRS 16 erforderlich sind, im IFRS 16-Buch. Diese Einträge umfassen die erstmaligen Erfassung des Nutzungsrechts am Leasingobjekt und der Verbindlichkeit sowie die Aufzeichnung von Zinsen und Abschreibungen.

### <a name="initial-recognition--112020--je-140"></a>Erstmalige Erfassung – 01.01.2020 – JE 140

| Kontenart | Kontonummer | Ebene  | Kontobeschreibung      | Belastung     | Gutschrift    |
|--------------|----------------|--------|--------------------------|-----------|-----------|
| Unternehmen       | 6              | Benutzerdefiniert | Nutzungsrecht am Leasingobjekt                | 22,793.90 |           |
| Unternehmen       | 7              | Benutzerdefiniert | Finanzierungsleasingsverpflichtung |           | 22,793.90 |

Die Mietzahlung wird wie die anderen Mietzahlungen gebucht. Der Grund für die Verwendung des Verrechnungskontos besteht darin, sicherzustellen, dass Bargeld nur einmal gutgeschrieben wird.

### <a name="lease-payment--1312020--je-150"></a>Mietzahlung – 31.01.2020 – JE 150

| Kontenart | Kontonummer | Ebene  | Kontobeschreibung      | Belastung    | Gutschrift   |
|--------------|----------------|--------|--------------------------|----------|----------|
| Unternehmen       | 7              | Benutzerdefiniert | Finanzierungsleasingsverpflichtung | 1,000.00 |          |
| Unternehmen       | 4              | Benutzerdefiniert | Clearingkonto         |          | 1,000.00 |

Die Buchung des Zinsaufwandsjournals wird aus dem Tilgungsplan für Verbindlichkeiten generiert.

### <a name="interest-expense--1312020--je-160"></a>Zinsausgaben – 31.01.2020 – JE 160

| Kontenart | Kontonummer | Ebene  | Kontobeschreibung      | Belastung | Gutschrift |
|--------------|----------------|--------|--------------------------|-------|--------|
| Unternehmen       | 8              | Benutzerdefiniert | Zinsausgaben         | 94.97 |        |
| Unternehmen       | 7              | Benutzerdefiniert | Finanzierungsleasingsverpflichtung |       | 94.97  |

Die Abschreibung des Zinsaufwandsjournals wird aus dem Tilgungsplan für Anlageabschreibungen generiert.

### <a name="depreciation-expense--1312020--je-170"></a>Abschreibungsausgaben – 31.01.2020 – JE 170

| Kontenart | Kontonummer | Ebene  | Kontobeschreibung      | Belastung  | Gutschrift |
|--------------|----------------|--------|--------------------------|--------|--------|
| Unternehmen       | 10             | Benutzerdefiniert | Abschreibungsausgaben     | 949.75 |        |
| Unternehmen       | 11             | Benutzerdefiniert | Kumulierte Abschreibung |        | 949.75 |

Nachdem alle diese Journaleinträge erstellt und gebucht wurden, werden die folgenden Werte für „benutzerdefinierte Ebene 1“ angezeigt. Beachten Sie, dass die letzte Spalte die Bankgebühr, den Mehrwertsteueraufwand und die Reduzierung des Bargeldes aus der vorherigen Ebene enthält, jedoch nicht die gesetzlich vorgeschriebenen Journaleinträge. Auf diese Weise erzielen Sie echte Funktionen für doppelte Berichterstattung. Zu diesem Zeitpunkt muss das Unternehmen lediglich seine Testbilanz ausführen und die aktuelle Ebene und die benutzerdefinierte Ebene kombinieren, um eine IFRS-Testbilanz zu erstellen.

| Kontonr. | Beschreibung              | Gesetzliches Buch\-Aktuelle Ebene\-JE\-100\-Dr \(Cr\) | Gesetzliches Buch\-Aktuelle Ebene\-JE\-110\-Dr \(Cr\) | Gesetzliches Buch\-Aktuelle Ebene\-JE\-120\-Dr \(Cr\) | Aktuelle Ebene \- Insgesamt | - | Stornobuch\-Benutzerdefinierte Ebene\-JE\-130\-Dr \(Cr\) | IFRS 16-Buch\-Benutzerdefinierte Ebene\-JE\-140\-Dr \(Cr\) | IFRS 16-Buch\-Benutzerdefinierte Ebene\-JE\-150\-Dr \(Cr\) | IFRS 16-Buch\-Benutzerdefinierte Ebene\-JE\-160\-Dr \(Cr\) | IFRS 16-Buch\-Benutzerdefinierte Ebene\-JE\-170\-Dr \(Cr\) | Benutzerdefinierte Ebene \+ Aktuelle Ebene \- Insgesamt |
|------------|--------------------------|---------------------------------------------------|---------------------------------------------------|---------------------------------------------------|-------------------------|---|-------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------|
| 1          | Mietvertragsausgaben            | 1,000\.00                                         |                                                   |                                                   | 1,000\.00               |   | \-1.000                                         |                                                |                                                |                                                |                                                | 0\.00                                   |
| 2          | Bankgebühr                 |                                                   | 3\.00                                             |                                                   | 3\.00                   |   |                                                 |                                                |                                                |                                                |                                                | 3\.00                                   |
| 3          | MwSt.-Ausgaben              |                                                   | 5\.00                                             |                                                   | 5\.00                   |   |                                                 |                                                |                                                |                                                |                                                | 5\.00                                   |
| 4          | Clearingkonto         | \-1.000\.00                                       | 1,000\.00                                         |                                                   | 0\.00                   |   | 1.000                                           |                                                | \-1.000                                        |                                                |                                                | 0\.00                                   |
| 5          | Kreditorenkonten         |                                                   | \-1.008\.00                                       | 1,008\.00                                         | 0\.00                   |   |                                                 |                                                |                                                |                                                |                                                | 0\.00                                   |
| 6          | Nutzungsrecht am Leasingobjekt                |                                                   |                                                   |                                                   | 0\.00                   |   |                                                 | 22,794                                         |                                                |                                                |                                                | 22,793\.90                              |
| 7          | Finanzierungsleasingsverpflichtung |                                                   |                                                   |                                                   | 0\.00                   |   |                                                 | \-22.794                                       | 1.000                                          | \-94\.97                                       |                                                | \-21.888\.87                            |
| 8          | Zinsausgaben         |                                                   |                                                   |                                                   | 0\.00                   |   |                                                 |                                                |                                                | 94\.97                                         |                                                | 94\.97                                  |
| 9          | Bargeld                     |                                                   |                                                   | \-1.008\.00                                       | \-1.008\.00             |   |                                                 |                                                |                                                |                                                |                                                | \-1.008\.00                             |
| 10         | Abschreibungsausgaben     |                                                   |                                                   |                                                   | 0\.00                   |   |                                                 |                                                |                                                |                                                | 949\.75                                        | 949\.75                                 |
| 11         | Kumulierte Abschreibung |                                                   |                                                   |                                                   | 0\.00                   |   |                                                 |                                                |                                                |                                                | \-949\.75                                      | \-949\.75                               |




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
