---
title: Buchhaltungsregel „Auf Belastungskonto buchen“
description: Dieser Artikel bietet einen Überblick über die Buchhaltungsregel „Auf Belastungskonto buchen“.
author: rachel-profitt
ms.date: 05/02/2022
ms.topic: article
ms.search.form: InventPosting, InventItemGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2022-05-02
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: c03109baaa341b25af70840b791ddf04f692fb1a
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016564"
---
# <a name="post-to-charge-account-accounting-principle"></a>Buchhaltungsregel „Auf Belastungskonto buchen“

Mit der Buchhaltungsregel *Auf Belastungskonto buchen* können Sie alle Differenzen berücksichtigen und leichter abstimmen, die im Einheitspreis zwischen einer physischen Buchung und einer Finanzbuchung, indirekten Kosten für gekaufte Artikel oder Belastungen für eine Bestellung auftreten.

Zwei Konfigurationen für Codes für Kreditorenkontengebühren auf der Seite **Gebührencode** (**Kreditorenkonten \> Belastungen einrichten \> Belastungscode**) kann dazu führen, dass eine Bestellung die Bewertung des Vorratsvermögens beeinflusst:

- Für Belastungscodes, bei denen das Feld **Lastschriftart** auf *Artikel* und das Feld **Kreditart** auf *Sachkonto* eingestellt ist, fungiert das als Absorptionskonto ausgewählte Sachkonto als Bestandsänderungskonto.
- Für Belastungscodes, bei denen das Feld **Lastschriftart** auf *Artikel* und das Feld **Kreditart** auf *Kunde/Kreditor* eingestellt ist, wird die Belastung als Materialkosten verbucht und das Bestandsabweichungskonto des Artikels wird verwendet.

## <a name="european-special-accounting-rule"></a>Europäische Sonderbuchhaltungsregel

In Europa wird die Buchhaltungsregel *Auf Belastungskonto buchen* häufig verwendet, um eine Sonderbuchhaltungsregel zu berücksichtigen. Zum Beispiel wird normalerweise eine der folgenden Methoden verwendet, um Bestandsänderungen zu berücksichtigen:

- **Verfahren „Umsatzkosten“** – Die Standardkonfiguration des Bestandsbuchungsprofils unterstützt diese Methode. Die Buchhaltungsregel *Auf Belastungskonto buchen* ist nicht erforderlich.
- **Verfahren „Art der Ausgaben“** – Kleinere Organisationen verwenden häufig diese Methode. Es umfasst typischerweise die folgenden Schritte:

    1. Waren oder Dienstleistungen werden zum Zeitpunkt des Erhalts vollständig abgerechnet.
    2. Am Ende der Periode wird eine Zykluszählung durchgeführt.
    3. Eine manuelle Anpassungen für die Menge und den Wert wird in den Bestand gebucht. (Das Gegenkonto ist ein Bestandsänderungskonto, das die in Schritt 1 gebuchten Ausgaben ausgleicht. Daher sehen Sie die Variation des Bestandswerts nur auf diesem Konto.)

Mit der Regel *Auf Belastungskonto buchen* können Sie die beiden Buchungen vollständig automatisieren. Auf diese Weise können Sie eine manuelle Korrekturbuchung zum Periodenende eliminieren.

## <a name="enable-the-post-to-charge-account-accounting-principle"></a>Buchhaltungsregel „Auf Belastungskonto buchen“ aktivieren

Um die Buchhaltungsregel *Auf Belastungskonto buchen* zu aktivieren, gehen Sie wie folgt vor.

1. Wechseln Sie zu **Kreditoren \> Einstellung \> Kreditorenparameter**.
2. Legen Sie auf der Registerkarte **Rechnung** im Inforegister **Rechnung** die Option **Auf Belastungskonto im Sachkonto buchen** auf *Ja* fest.
3. Schließen Sie die Seite.

## <a name="prerequisites-and-recommended-parameters-for-the-post-to-charge-account-accounting-principle"></a>Voraussetzungen und empfohlene Parameter für die Buchhaltungsregel „Auf Belastungskonto buchen“

Wenn Sie Kaufgebühren und Bestandsschwankungen berücksichtigen möchten, müssen die folgenden Voraussetzungen erfüllt sein:

- Auf der Registerkarte **Rechnung** auf der Seite **Kreditorenkontenparameter** (**Kreditorenkonten \> Einrichtung \> Kreditorenkontenparameter**) muss die Option **Auf Belastungskonto im Sachkonto buchen** auf *Ja* eingestellt sein.
- Auf der Seite **Artikelmodellgruppen** (**Kostenmanagement \> Einrichtung der Bestandsbuchhaltungsrichtlinien \> Artikelmodellgruppen**) müssen alle folgenden Optionen auf *Ja* für jede relevante Modellgruppe eingestellt sein, die Artikel enthält, die in einer Bestellung enthalten sind:

    - Physischen Bestand buchen
    - Wertmäßigen Bestand buchen
    - Verbindlichkeiten bei Produktzugang abgrenzen

- Auf der Registerkarte **Lieferung** der Seite **Beschaffungsparameter** (**Beschaffung \> Einrichtung \> Beschaffungsparameter**) muss die Option **Gebühren bei Produktzugang generieren** auf *Ja* eingestellt sein.
- Auf der Registerkarte **Bestandsbuchhaltung** der Seite **Parameter für Lager- und Lagerortverwaltung** (**Lagerverwaltung \> Einstellungen \> Parameter für Lager- und Lagerortverwaltung**) muss die Option **Lieferschein auf Sachkonto buchen** auf *Ja* eingestellt sein.
- Auf der Registerkarte **Bestellung** der Seite **Buchung** (**Lagerverwaltung \> Einstellungen \> Buchung \> Buchung**) müssen für jede der folgenden Buchungsarten Hauptkonten angegeben werden, die für jeden relevanten Posten gelten:

    - Einkaufsaufwendungen, nicht fakturiert
    - Einkaufswendungen für Produkt
    - Bestandsveränderung

## <a name="example-scenario-1-change-in-unit-cost-price"></a>Beispielszenario 1: Änderung des Einstandspreises je Einheit

Dieses Beispielszenario hat folgende Voraussetzungen:

- First-in-first-out(FIFO)-Kostenmodell

Das folgende Verfahren ist ein Beispiel, das zeigt, was passiert, wenn Sie den Einstandspreis pro Einheit in einer Bestellung ändern.

1. Erstellen Sie eine Bestellung mit der Menge 1 eines Elements, das einen Preis je Einheit von 100,00 hat.
2. Bestätigen Sie die Bestellung.
3. Buchen Sie den Produkteingang für die Bestellung.
4. Validieren Sie den Gutschein auf dem Produktbeleg. Die folgende Tabelle zeigt einen Beispielgutschein.

    | Buchungstyp | Hauptkonto | Hauptkontoname | Kontotyp | Soll/Haben? | Clearingkonto | Physisch/Wertmäßig? | Betrag |
    |---|---|---|---|---|---|---|---|
    | Einkauf, Bestandsveränderung | 600170 | Bestandsveränderungsmaterialien | Ausgaben | Gutschrift | Nein | Physisch | -100,00 |
    | Kosten der eingekauften, eingegangenen Materialien | 140100 | Materialbestand | Anlage | Belastung | Ja | Physisch | 100.00 |
    | Einkaufsaufwendungen, nicht fakturiert | 600180 | Materialeingänge | Ausgaben | Belastung | Ja | Physisch | 100.00 |
    | Einkauf, Abgrenzung | 200140 | Antizipierte Einkäufe | Passivposten | Gutschrift | Ja | Physisch | -100,00 |

5. Buchen Sie die Rechnung für die Bestellung mit einem aktualisierten Stückpreis von 110,00.
6. Validieren Sie den Gutschein auf der Rechnung. Die folgende Tabelle zeigt einen Beispielgutschein.

    | Buchungstyp | Hauptkonto | Hauptkontoname | Kontotyp | Soll/Haben? | Clearingkonto | Physisch/Wertmäßig? | Betrag |
    |---|---|---|---|---|---|---|---|
    | Einkauf, Bestandsveränderung | 600170 | Bestandsveränderungsmaterialien | Ausgaben | Gutschrift | Nein | Kosten | -10,00 |
    | Kosten der eingekauften, eingegangenen Materialien | 140100 | Materialbestand | Anlage | Belastung | Ja | Kosten | -100,00 |
    | Einkaufsaufwendungen, nicht fakturiert | 600180 | Materialeingänge | Ausgaben | Belastung | Ja | Kosten | -100,00 |
    | Einkauf, Abgrenzung | 200140 | Antizipierte Einkäufe | Passivposten | Gutschrift | Ja | Kosten | 100.00 |
    | Kosten der eingekauften, fakturierten Materialien | 140100 | Materialbestand | Anlage | Belastung | Nein | Kosten | 110.00 |
    | Einkaufswendungen für Produkt | 600180 | Materialeingang | Ausgaben | Gutschrift | Nein | Kosten | 110.00 |
    | Kreditorensaldo | 211000 | Kreditorenkonten – Handel | Passivposten | Gutschrift | Nein | Kosten | -110,00 |

## <a name="example-2-charges-and-indirect-costs-on-the-purchase-order"></a>Beispiel 2: Gebühren und indirekte Kosten auf der Bestellung

Dieses Beispielszenario hat folgende Voraussetzungen:

- FIFO-Kostenmodell
- **Gebührencode 1:** Soll- und Habensachkonto für 10 Prozent
- **Gebührencode 2:** Soll- und Haben Kunde/Lieferant für 10,00 Prozent proportional
- **Indirekte Kosten:** 2,00 Prozent auf den Kaufpreis aufgeschlagen

Das folgende Verfahren ist ein Beispiel, das zeigt, was passiert, wenn Sie die Gebühren und indirekten Kosten bei einer Bestellung berücksichtigen.

1. Erstellen Sie eine Bestellung mit der Menge 1 eines Elements, das einen Preis je Einheit von 100,00 hat.
2. Fügen Sie einen Belastungscode von 10 Prozent hinzu, der den Artikel belastet und die Kosten dem Sachkonto gutschreibt.
3. Fügen Sie einen Belastungscode von 10.00 hinzu, der den Artikel belastet und die Kosten dem Kunden/Lieferanten gutschreibt.
4. Ordnen Sie die Belastungen den Bestellpositionen zu.
5. Bestätigen Sie die Bestellung.
6. Buchen Sie den Produkteingang für die Bestellung.
7. Validieren Sie den Gutschein auf dem Produktbeleg. Die folgende Tabelle zeigt einen Beispielgutschein.

    | Buchungstyp | Hauptkonto | Hauptkontoname | Kontotyp | Soll/Haben? | Clearingkonto | Physisch oder wertmäßig | Betrag |
    |---|---|---|---|---|---|---|---|
    | Einkauf, Bestandsveränderung | 600170 | Bestandsveränderungsmaterialien | Ausgaben | Gutschrift | Nein | Physisch | -110,00 |
    | Vorkalkulierte indirekte absorbierte Kosten | 600520 | Absorbierte indirekte Kosten | Ausgaben | Gutschrift | Ja | Physisch | -2,40 |
    | Fracht auf Einkauf | 600120 | Fracht-/Transportkosten | Ausgaben | Gutschrift | Nein | Physisch | -10,00 |
    | Kosten der eingekauften, eingegangenen Materialien | 140100 | Materialbestand | Anlage | Belastung | Ja | Physisch | 122.40 |
    | Einkaufsaufwendungen, nicht fakturiert | 600180 | Materialeingänge | Ausgaben | Belastung | Ja | Physisch | 110.00 |
    | Einkauf, Abgrenzung | 200140 | Antizipierte Einkäufe | Passivposten | Gutschrift | Ja | Physisch | -110,00 |

8. Buchen Sie die Rechnung für die Bestellung.
9. Validieren Sie den Gutschein auf der Rechnung. Die folgende Tabelle zeigt einen Beispielgutschein.

    | Buchungstyp | Hauptkonto | Hauptkontoname | Kontotyp | Soll/Haben? | Clearingkonto | Physisch/Wertmäßig? | Betrag |
    |---|---|---|---|---|---|---|---|
    | Einkauf, Bestandsveränderung | 600170 | Bestandsveränderungsmaterialien | Ausgaben | Gutschrift | Nein | Kosten | 0,00 |
    | Vorkalkulierte indirekte absorbierte Kosten | 600520 | Absorbierte indirekte Kosten | Ausgaben | Belastung | Ja | Kosten | 2.40 |
    | Absorbierte indirekte Kosten | 600520 | Absorbierte indirekte Kosten | Ausgaben | Belastung | Nein | Kosten | -2,40 |
    | Kosten der eingekauften, eingegangenen Materialien | 140100 | Materialbestand | Anlage | Gutschrift | Ja | Kosten | -110,00 |
    | Einkaufsaufwendungen, nicht fakturiert | 600180 | Materialeingänge | Ausgaben | Gutschrift | Ja | Kosten | -110,00 |
    | Einkauf, Abgrenzung | 200140 | Antizipierte Einkäufe | Passivposten | Belastung | Ja | Kosten | 110.00 |
    | Kosten der eingekauften, fakturierten Materialien | 140100 | Materialbestand | Anlage | Belastung | Nein | Kosten | 110.00 |
    | Einkaufswendungen für Produkt | 600180 | Materialeingang | Ausgaben | Gutschrift | Nein | Kosten | 110.00 |
    | Kreditorensaldo | 211000 | Kreditorenkonten – Handel | Passivposten | Gutschrift | Nein | Kosten | -110,00 |
