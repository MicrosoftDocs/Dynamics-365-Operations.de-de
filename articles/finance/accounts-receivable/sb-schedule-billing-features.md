---
title: Funktionen von Abrechnungszeitplänen
description: In diesem Thema werden die Funktionen von Abrechnungszeitplänen erläutert, z. B. Preisfindungsmethoden, Eskalationen und Rabatte, Ausrichtungsdatumsangaben, anteilige Verrechnung, umgekehrte Fakturierung und geteilte Artikelgruppen.
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
ms.openlocfilehash: 0ce323565a94e8e70d90a65b7a3143e984a1c159
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8700722"
---
# <a name="billing-schedule-features"></a>Funktionen von Abrechnungszeitplänen

[!include [banner](../includes/banner.md)]

In diesem Thema werden die Funktionen von Abrechnungszeitplänen und Abrechnungszeitplanpositionen erläutert. Es werden die verschiedenen Methoden beschrieben, die für die Preisgestaltung verwendet werden, wie Sie mit Eskalationen und Rabatten arbeiten und wie ein Abrechnungszeitraum storniert wird. Das Thema enthält auch Beispiele für anteilige Verrechnungen und geteilte Artikelgruppen.

## <a name="pricing-methods"></a>Preisgestaltungsmethoden

Sie können eine der folgenden Preisgestaltungsmethoden verwenden, um den Einheitspreis eines Artikels zu berechnen:

* Flach
* Standard
* Stufe
* Pauschaltarif

### <a name="flat-pricing"></a>Pauschalpreis

Wenn die Pauschalpreismethode verwendet wird, kann der Einheitspreis für eine Abrechnungszeitplanposition auf der Seite **Alle Abrechnungszeitpläne** in jeden gewünschten Wert geändert werden. Der Wert **Preiseinheit** ist immer **1**. Deshalb sind die Werte für **Preis je Einheit** und **Nettobetrag** für einen Artikel gleich.

### <a name="standard-pricing-without-a-trade-agreement"></a>Standardpreis (ohne Handelsvereinbarung)

Wenn die Standardpreismethode ohne Handelsvereinbarung verwendet wird, richten Sie den Einheitspreis für eine Abrechnungszeitplanposition ein, indem Sie **Produktinformationsverwaltung** auf der Seite **Produktdetails freigeben** auswählen. Der Einheitspreis wird im Abschnitt **Basisverkaufspreis** angezeigt. Er wird berechnet als *Preis* &divide; *Preis Menge*.

### <a name="standard-pricing-with-a-trade-agreement"></a>Standardpreis (mit Handelsvereinbarung)

Die folgenden Beispiele zeigen die Standardpreisberechnungen, wenn eine Handelsvereinbarung besteht. Sie können Handelsvereinbarungen auf der Seite **Produktdetails freigeben** erstellen.

Beide Beispiele verwenden einen Artikel mit den folgenden Preisstufen.

| Von-Menge | Bis-Menge | ME | Preis | Preiseinheit |
|---|---|---|---|---|
| 0 | 100 | Pro Stück | 1.50 | 1 |
| 100 | 200 | Pro Stück | 1.25 | 1 |
| 200 | 999999 | Pro Stück | 1.00 | 1 |

**Beispiel 1**

Die Rechnungsmenge beträgt 250, und es wird die Standardpreisfindungsmethode verwendet. Da die Menge im Preismengenbereich von 200 bis 999.999 liegt, beträgt der Einheitspreis 1,00. 

Der Nettobetrag wird folgendermaßen berechnet:

*Nettobetrag* = (*Menge* &times; *Preis*) &divide; *Preiseinheit* = (250 &times; 1,00) &divide; 1 = 250

**Beispiel 2**

Die Rechnungsmenge beträgt 100, und es wird die Standardpreisfindungsmethode verwendet. Da die Rechnungsmenge im Preismengenbereich von 0 bis 100 liegt, beträgt der Einheitspreis 1,50.

> [!NOTE]
> Die Rechnungsmenge liegt im Bereich von 0 bis 100 statt im Bereich von 100 bis 200, da beim standardmäßigen Mengenabgleich eine Menge übereinstimmt, wenn sie *größer oder gleich* der Von-Menge und *Kleiner* als die Bis-Menge ist.

Der Nettobetrag wird folgendermaßen berechnet:

*Nettobetrag* = (100 &times; 1,50) &divide; 1 = 150

### <a name="tier-pricing"></a>Staffelpreise

Beim folgenden Beispiel verwendet ein Artikel die folgenden Preisstufen.

| Von-Menge | Bis-Menge | ME | Preis | Preiseinheit |
|---|---|---|---|---|
| 0 | 100 | Pro Stück | 1.50 | 10 |
| 100 | 200 | Pro Stück | 1.25 | 10 |
| 200 | 999999 | Pro Stück | 1.00 | 10 |

Wenn die Rechnungsmenge 250 beträgt und die Staffelpreismethode verwendet wird, werden die Preise der Artikel basierend auf den Preisstufen wie folgt berechnet:

- **Erste 100 Artikel:** 100 &times; 1,50 = 150,00
- **Zweite 100 Artikel:** 100 &times; 1,25 = 125,00
- **Verbleibende Artikel:** 50 &times; 1,00 = 50,00

Der Nettobetrag wird folgendermaßen berechnet:

*Nettobetrag* = (150,00 &divide; 10) + (125,00 &divide; 10) + (50,00 &divide; 10) = 15,00 + 12,50 + 5,00 = 32,50

Nachdem der Nettobetrag berechnet wurde, wird der Einheitspreis berechnet, indem der Nettobetrag durch die Menge dividiert wird:

*Preis je Einheit* = 32,50 &divide; 250 = 0,13

### <a name="flat-tier-pricing"></a>Pauschale Staffelpreise

Beim folgenden Beispiel verwendet ein Artikel die folgenden Preisstufen.

| Von-Menge | Bis-Menge | ME | Pauschaltarifbetrag | Preiseinheit |
|---|---|---|---|---|
| 0 | 50 | Pro Stück | 100.00 | 50 |
| 50 | 200 | Pro Stück | 150.00 | 200 |

Die folgende Tabelle zeigt die Rechnungen und Einheitspreise für die verschiedenen Abnahmemengen. Zuerst wird der Nettobetrag berechnet und dann der Einheitspreis.

| Rechnung | Menge eingekauft | Preis je Einheit | Nettobetrag |
|---|---|---|---|
| 1 | 25 | 2,00 &divide; 25 = 0,08 | 100 &divide; 50 = 2,00 |
| 2 | 20 | 2.00 &divide; 20 = 0,10 | 100 &divide; 50 = 2,00 |
| 3 | 50 | 2.00 &divide; 50 = 0,04 | 100 &divide; 50 = 2,00 |
| 4 | 60 | 0,75 &divide; 60 = 0,0125 = 0,01 | 150 &divide; 200 = 0,75 |

## <a name="escalations-and-discounts"></a>Eskalationen und Rabatte

Eine *Eskalation* ist eine Preiserhöhung für einen zukünftigen Abrechnungszeitraum, für den die Rechnung noch nicht erstellt wurde. Ein *Rabatt* ist eine Preisreduzierung für einen zukünftigen Abrechnungszeitraum, für den die Rechnung noch nicht erstellt wurde.

Bei der Abonnementabrechnung können Eskalationen und Rabatte nicht rückwirkend auf einen Abrechnungszeitplan angewendet werden. Beispielsweise können Sie eine Eskalation nicht auf einen Abrechnungszeitplan anwenden und verarbeiten, der drei Monate in der Vergangenheit liegt. Mit anderen Worten: Sie können keine Preiserhöhung anwenden, die vor drei Monaten stattgefunden hat.

Sie können eine Eskalation oder einen Rabatt auf einen Abrechnungszeitplan oder eine Abrechnungszeitplanposition an einer der folgenden Stellen anwenden:

- Die Seite **Alle/Aktive Fakturierungszeitpläne** Liste
- Bestimmter Abrechnungszeitplan
- Bestimmte Abrechnungszeitplanposition

### <a name="apply-an-escalation-or-discount"></a>Eskalation oder Rabatt anwenden

Gehen Sie wie folgt vor, um eine Eskalation oder einen Rabatt auf einen Abrechnungszeitplan anzuwenden.

1. Wählen Sie einen Abrechnungszeitplan oder eine Abrechnungszeitplanposition aus.
2. Wählen Sie **Eskalation und Rabatt** entweder auf der Registerkarte **Eskalation und Rabatt** oder in der Abrechnungszeitplanposition.
3. Wenn zur Berechnung der Eskalation oder des Rabatts ein Verbraucherpreisindex verwendet wird, wählen Sie einen Wert im Feld **Berechnung des Verbraucherpreisindex** aus.
4. Wählen Sie **Neu** aus, um eine Eskalations- oder Rabattposition hinzuzufügen.
5. Aktivieren Sie für einen Rabatt das Kontrollkästchen **Rabatt**. Lassen Sie für eine Eskalation das Kontrollkästchen **Rabatt** deaktiviert.
6. Legen Sie die Felder **Startdatum** und **Frequenz** fest.
7. Legen Sie für Abgrenzungsposten, die die Funktion für nicht abgerechnete Umsatzerlöse verwenden, das Feld **Enddatum** fest.
8. Legen Sie das Feld **Prozentsatz**, **Menge** oder **Verbraucherpreisindex-Plan** fest.
9. Legen Sie das Feld **Enddatum** fest.
10. Wählen Sie **OK** aus.
11. Wiederholen Sie die Schritte 4 bis 10 für jede zusätzliche Eskalations- oder Rabattposition, die Sie benötigen.

### <a name="fields-on-the-billing-schedule-lines-page"></a>Felder auf der Seite mit den Abrechnungszeitplanpositionen

Die Seite **Abrechnungszeitplanpositionen** enthält die folgenden Felder.

| Feld | Description |
|---|---|
| Artikelnummer | Die Nummer des Artikels der Abrechnungszeitplanposition. Dieses Feld ist nur verfügbar, wenn die Seite von einer Abrechnungszeitplanposition geöffnet wurde. |
| Berechnung des Verbraucherpreisindex | <p>Wählen Sie die Methode aus, die zur Berechnung der Verbraucherpreisindex-Eskalation verwendet wird:</p><ul><li>**Vorheriger Verbraucherpreisindex** – Verwenden Sie den vorherigen Verbraucherpreisindexwert für die Eskalationsberechnung.</li><li>**Basis-Verbraucherpreisindex** – Verwenden Sie den Basis-Verbraucherpreisindex für die Eskalationsberechnung.</li></ul> |
| Raster **Zeile** | |
| Rabatt | <p>Aktivieren Sie das Kontrollkästchen, um anzugeben, ob es sich bei der Betragsänderung um eine Eskalation oder einen Rabatt handelt:</p><ul><li>**Ausgewählt** – Die Änderung wendet einen Rabatt auf den Abrechnungszeitplan oder die Abrechnungszeitplanposition an.</li><li>**Gelöscht** – Die Änderung wendet eine Eskalation auf einen Abrechnungszeitplan oder eine Abrechnungszeitplanposition an.</li></ul><p>Die Einstellung dieses Kontrollkästchens kann für Artikel, die die Funktion für nicht abgerechnete Umsatzerlöse verwenden, nicht geändert werden. Darüber hinaus können Rabatte nicht auf Artikel angewendet werden, die eine Umsatzerlösverteilung verwenden.</p> |
| Startdatum | Wählen Sie das Startdatum der Eskalation oder des Rabatts aus. |
| Häufigkeit | Wählen Sie die Frequenz der Eskalation oder des Rabatts aus: **Keine**, **Monatlich**, **Vierteljährlich**, **Halbjährlich** oder **Jährlich**. |
| Prozentsatz | Geben Sie den Prozentsatz der Eskalation oder des Rabatts an. |
| Betrag | Geben Sie den Betrag der Eskalation oder des Rabatts an. |
| Zeitplan für Verbraucherpreisindex | Wählen Sie den Verbraucherpreisindex-Plan aus, der für die Berechnungen verwendet wird. |
| Enddatum | <p>Wählen Sie das Enddatum der Eskalation oder des Rabatts aus.</p><p>**Hinweis:** Dieses Feld ist für Artikel erforderlich, die die Funktion für nicht abgerechnete Umsatzerlöse verwenden.</p> |
| Nummer des Abgrenzungsschemas | <p>Die Nummer des Stundungszeitplans.</p><p>Dieses Feld ist nur verfügbar, wenn die Seite von einer Abrechnungszeitplanposition geöffnet wurde.</p> |
| Lfd. Nummer | <p>Die Nummer der Stapelverarbeitungserfassung.</p><p>Dieses Feld ist nur verfügbar, wenn die Seite von einer Abrechnungszeitplanposition geöffnet wurde.</p> |
| Gesamter Rabattbetrag | <p>Die Summe der Rabattbeträge für alle Zeilen im Raster.</p><p>Dieses Feld ist nur verfügbar, wenn die Seite von einer Abrechnungszeitplanposition geöffnet wurde.</p> |
| Aktueller kurzfristiger nicht abgerechneter Umsatzerlösbetrag | <p>Der aktuelle kurzfristige nicht abgerechnete Umsatzerlösbetrag.</p><p>Dieser Betrag erscheint, wenn auf der Seite **Parameter für wiederkehrende Vertragsabrechnungen** ein kurzfristiges Abgrenzungsschema ausgewählt wird. Die Konten für die Position werden auf der Seite **Einrichtung von nicht fakturierten Umsätzen** eingerichtet.</p> |
| Aktueller langfristiger nicht abgerechneter Umsatzerlösbetrag | <p>Der aktuelle langfristige nicht abgerechnete Umsatzerlösbetrag.</p><p>Dieser Betrag erscheint, wenn auf der Seite **Parameter für wiederkehrende Vertragsabrechnungen** ein kurzfristiges Abgrenzungsschema ausgewählt wird. Die Konten für die Position werden auf der Seite **Einrichtung von nicht fakturierten Umsätzen** eingerichtet.</p> |

## <a name="proration-examples"></a>Beispiele für die anteilige Verrechnung

Berechnungen für die anteilige Verrechnung können auf der Anzahl der Tage oder der Anzahl der Monate basieren. Die Methode, die für die anteilige Verrechnung verwendet wird, wird auf der Seite **Parameter für wiederkehrende Vertragsabrechnungen** festgelegt. Die Methode der anteiligen Verrechnung wirkt sich in den folgenden Situationen darauf aus, wie die Beträge für einen Abrechnungszeitplan berechnet werden:

- Anfängliche Erstellung
- Anwendung einer Eskalation oder eines Rabatts
- Beendigung
- Platzieren oder Entfernen einer Sperre
- Hinzufügen von Support oder Verlängerung

Die Methode der anteiligen Verrechnung wirkt sich auch auf die Berechnungen im Bericht zu monatlich wiederkehrenden Umsatzerlösen (MRR) aus.

### <a name="example-1"></a>Beispiel 1

Der jährliche Betrag eines Abrechnungszeitplans beträgt 5.000 $. Das Startdatum ist der 12. August 2019 und das Enddatum der 22. Dezember 2019. Das Fakturierungsintervall ist jährlich. Der anteilige Betrag wird auf folgende Weise berechnet, je nachdem, ob die tägliche oder die monatliche Berechnungsmethode verwendet wird:

- **Täglich**

    - *Anzahl der Tage* = *Enddatum* – *Startdatum* + 1 = 133 Tage
    - *Anzahl der Tage im Jahr* = 11. August 2020 – 12. August 2019 + 1 = 366 Tage
    - *Anteiliger Betrag* = 5.000 &times; (133 &divide; 366) = 1.816,94

- **Monatlich**

    - *Anteil Monatsbeginn* = (31 – 12 + 1) &divide; 31 = 20 &divide; 31
    - *Monatsmitte* = 3
    - *Anteil Monatsende* = 22 &divide; 31
    - Anteiliger Betrag = 5.000 &divide; 12 &times; \[(20 &divide; 31) + 3 + (22 &divide; 31)\] = 1.814,52

### <a name="example-2"></a>Beispiel 2

Der jährliche Betrag eines Abrechnungszeitplans beträgt 12.000 $. Das Startdatum ist der 1. August 2019 und das Enddatum der 31. Dezember 2019. Das Fakturierungsintervall ist jährlich. Der anteilige Betrag wird je nach Berechnungsmethode wie folgt berechnet:

- **Täglich**

    - *Anzahl der Tage* = *Enddatum* – *Startdatum* + 1 = 153 Tage
    - *Anzahl der Tage im Jahr* = 31. Juli 2020 – 1. August 2019 + 1 = 366 Tage
    - *Anteiliger Betrag* = 12.000 &times; (153 &divide; 366) = 5.016,39

- **Monatlich (Ganzer Monat)**

    - *Anzahl Monate* = 5
    - *Monate gesamt* = 12
    - *Anteiliger Betrag* = (12.000 &times; 5) &divide; 12 = 5.000

## <a name="reversing-a-period-billing"></a>Stornieren einer Periodenabrechnung

In diesem Beispiel hat ein Abrechnungszeitplan nur eine Zeile:

- Die Abrechnung erfolgt monatlich für 12 Monate von Januar bis Dezember.
- Rechnungen wurden für alle Perioden bis April erstellt.

Sie möchten die Rechnung für den Abrechnungszeitraum April stornieren.

Wenn für den Abrechnungszeitraum April noch keine Verkaufsrechnung erstellt wurde, könnten Sie den Auftrag löschen. In diesem Fall würde der Status **Fakturiert** für das Detail entfernt. Da jedoch für den Abrechnungszeitraum eine Rechnung erstellt wurde, kann der Status **Fakturiert** für das Detail nicht gelöscht werden. Um die Abrechnung von April zu stornieren, müssen Sie daher eine Gegengutschrift für die Position erstellen.

1. Erstellen Sie auf der Seite **Alle Abrechnungszeitpläne** eine Zeitplanposition für den gleichen Artikel.
2. Ändern Sie den Wert unter **Menge** für den Artikel in den Negativwert der ursprünglichen Menge.
3. Legen Sie das Feld **Fakturierungsintervall** auf **Einmalig** fest.
4. Aktualisieren Sie die Start- und Enddaten so, dass sie mit den Datumsangaben der Fakturierungsdetailposition übereinstimmen, für die Sie eine Gutschrift erstellen möchten. Legen Sie für dieses Beispiel das Startdatum auf den 1. April 2019 und das Enddatum auf den 30. April 2019 fest.
5. Speichern Sie die Änderungen.
6. Öffnen Sie die Seite **Rechnung erstellen**, und erstellen Sie den Auftrag mit der Gutschrift für den angegebenen Zeitraum.
7. Optional: Buchen Sie die Rechnung.

Wenn Sie die Zeilen für den Abrechnungszeitplan überprüfen, werden Sie feststellen, dass die neue Zeile einen Link zur Gutschrift enthält. Die ursprüngliche Zeile hat weiterhin einen Link zur ursprünglichen April-Rechnung.

## <a name="split-item-group-examples"></a>Beispiele für geteilte Artikelgruppen

Für dieses Beispiel ist die folgende Einrichtung vorhanden:

- Auf der Seite **Parameter für wiederkehrende Vertragsabrechnungen** ist die Option **Nach Artikelgruppe teilen** ausgewählt, und das Feld **Eindeutiger Zeitplantyp** ist auf **Debitor** festgelegt.
- Es wurden drei Artikelgruppen erstellt: **PREFIX**, **DATAHUB** und **SPP**.
- Kunde US-001 hat mehrere Abrechnungszeitpläne, bei denen die Artikelgruppe PREFIX oder DATAHUB ist.
- Kunde US-002 hat mehrere Abrechnungszeitpläne, bei denen die Artikelgruppe PREFIX oder SPP ist.

| Abrechnungszeitplannummer | Kunde | Artikelgruppe |
|---|---|---|
| SCH001 | US-001 | PREFIX |
| SCH002 | US-001 | DATAHUB |
| SCH003 | US-002 | PREFIX |
| SCH004 | US-002 | SPP |

Kunde US-001 kauft einen Verlängerungsartikel, der zur Artikelgruppe PREFIX gehört. Diese Transaktion ist ein neuer Auftrag.

| Auftragsnummer | Kunde | Hauptartikel | Verlängerungsartikel | Artikelgruppe Verlängerung | Abrechnungszeitplannummer |
|---|---|---|---|---|---|
| SO0001 | US-001 | D0001 | D0002 | PREFIX | SCH001 |

Wenn die Rechnung für den Auftrag gebucht wird, wird der Verlängerungsartikel dem bestehenden Abrechnungszeitplan (SCH001) für den Kunden hinzugefügt. Dieser Abrechnungszeitplan verwendet die Artikelgruppe PREFIX. Alle Verlängerungsartikel, die zu derselben Artikelgruppe gehören, werden in den gleichen Abrechnungszeitplan gestellt.

**Übergeordnet**
 
| Abrechnungszeitplannummer | Kunde | Artikelgruppe |
|---|---|---| 
| SCH001 | US-001 | PREFIX |

**Position**

| Abrechnungszeitplannummer | Kunde | Artikelgruppe |
|---|---|---|
| SCH001 | US-001 | D0002 |

Kunde US-001 kauft nun einen Verlängerungsartikel, der zur Artikelgruppe SPP gehört. Diese Transaktion ist ein neuer Auftrag.

| Auftragsnummer | Kunde | Hauptartikel | Verlängerungsartikel | Artikelgruppe Verlängerung | Abrechnungszeitplannummer |
|---|---|---|---|---|---|
| SO0002 | US-001 | D0003 | D0004 | SPP | |

Derzeit hat Kunde US-001 keinen Abrechnungszeitplan, der die Artikelgruppe SPP verwendet. Daher wird ein neuer Abrechnungszeitplan erstellt.

**Übergeordnet**

| Abrechnungszeitplannummer| Kunde | Artikelgruppe |
|---|---|---|
| SCH005 | US-001 | SPP |

**Position**

| Abrechnungszeitplannummer | Kunde | Artikelgruppe |
|---|---|---|
| SCH005 | US-001 | D0004 |

### <a name="multiple-billing-schedules-for-the-same-end-user-and-customer"></a>Mehrere Abrechnungszeitpläne für denselben Endbenutzenden und Kunden

Für dieses Beispiel ist die folgende Einrichtung vorhanden:

- Auf der Seite **Parameter für wiederkehrende Vertragsabrechnungen** ist die Option **Nach Artikelgruppe teilen** ausgewählt, und das Feld **Eindeutiger Zeitplantyp** ist auf **Endbenutzer** festgelegt.
- Auf der Seite **Endbenutzer** ist die folgende Kunden- und Endbenutzer\*innenbeziehung eingerichtet.

    | Kundenkonto | Endbenutzerkonto |
    |---|---|
    | US-001 | US-221 |

Mehrere Abrechnungszeitpläne werden für die Kombination aus Kunde und Endbenutzer\*in erstellt. Da auf der Seite **Parameter für wiederkehrende Vertragsabrechnungen** die Option **Nach Artikelgruppe teilen** ausgewählt ist, können mehrere Abrechnungszeitpläne für dieselbe Kunden- und Endbenutzer\*innenbeziehung erstellt werden.

| Abrechnungszeitplannummer | Kunde | Endbenutzerkonto | Kopfzeile Artikelgruppe |
|---|---|---|---|
| SCH005 | US-001 | US-221 | IG1 |
| SCH006 | US-001 | US-221 | IG2 |
| SCH007 | US-001 | US-221 | IG3 |

Auf der Seite **Artikeleinstellungen** erstellen Sie Beziehungen zwischen Support- und Verlängerungsartikeln.

| Artikelcode | Artikelrelation | Supportartikel | Verlängerungsartikel | Artikelgruppe Verlängerung |
|---|---|---|---|---|
| Tabelle | D001 | ITEM27 | D007 | IG1 |
| Tabelle | D002 | ITEM28 | D005 | IG2 |
| Tabelle | D003 | ITEM29 | D006 | IG3 |

Sie erstellen nun einen Auftrag für den Kunden US-001. Dieser Auftrag enthält Artikel von der Seite **Artikeleinstellungen**. Wenn Sie den Auftrag erstellen, öffnen Sie die Seite **Support- und Verlängerungsprozess**, und definieren Sie das Feld **Endbenutzerkonto** sowie und alle anderen erforderlichen Informationen für den Verlängerungsartikel.

Wenn die Rechnung für die Transaktion erstellt und gebucht wird, werden verschiedene Abrechnungszeitpläne für die Kombination aus Kunde/Endbenutzer\*in und Artikelgruppe erstellt. Dem gleichen Abrechnungszeitplan kann mehr als eine Position in demselben Auftrag zugewiesen werden.

| Auftragsnummer | Kunde | Endbenutzerkonto | Hauptartikel | Supportartikel | Verlängerungsartikel | Abrechnungszeitplannummer |
|---|---|---|---|---|---|---|
| SO0001 | US-001 | US-221 | D001 | ITEM27 | D007 | SCH005 |
| SO0001 | US-001 | US-221 | D002 | ITEM28 | D005 | SCH006 |
| SO0001 | US-001 | US-221 | D003 | ITEM29 | D006 | SCH005 |
