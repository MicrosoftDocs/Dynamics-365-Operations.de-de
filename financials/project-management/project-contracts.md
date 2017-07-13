---
title: "Projektverträge"
description: "Dieses Thema beschreibt Beispiele für Projektverträge, die Sie für Projekte und Finanzierungsquellen erstellen können, und zeigt, wie Sie in Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, Verträge verwalten und Rechnungen für Projektdebitoren erstellen können."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 2aa70e050bf068a26e2d0d86c26045fc000931eb
ms.contentlocale: de-de
ms.lasthandoff: 06/13/2017


---

# <a name="project-contracts"></a>Projektverträge

[!include[banner](../includes/banner.md)]


Dieses Thema beschreibt Beispiele für Projektverträge, die Sie für Projekte und Finanzierungsquellen erstellen können, und zeigt, wie Sie in Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, Verträge verwalten und Rechnungen für Projektdebitoren erstellen können.

Der für einen Projektvertrag erstellte Projekttyp definiert die Methode, nach der das Projekt den Debitoren in Rechnung gestellt wird. Ein Projektvertrag und das zugehörige Projekt können geändert werden, der Projekttyp jedoch nicht. 

Mithilfe eines Projektvertrags können ein oder mehrere Projekte gleichzeitig fakturiert werden. Durch einen Projektvertrag wird zudem sichergestellt, dass für die einzelnen Unterprojekte in einer Projektstruktur die gleiche Rechnungsstellungsprozedur verwendet wird. 

Jedes Projekt, das fakturiert wird, muss einem Projektvertrag zugeordnet sein. Einstellungen für einen Projektvertrag gelten für alle Projekte und Unterprojekte, die dem Projektvertrag zugeordnet sind. 

In einem Projektvertrag können eine oder mehrere Finanzierungsquellen angegeben werden. Dadurch können Sie die Fakturierung auf mehrere Geldgeber aufteilen, Finanzierungslimits einrichten, damit Finanzierungsquellen nicht mehr als ein angegebener Betrag berechnet wird, und Finanzierungsregeln für die Berechnung von Ausgaben konfigurieren.

## <a name="funding-for-project-contracts"></a>Finanzierung von Projektverträgen
In einigen Projektverträgen ist möglicherweise festgelegt, dass mehrere Parteien für die Finanzierung der Projektkosten verantwortlich sind. Nachfolgend finden Sie einige Beispiele:

-   Ein großer Debitor, der mehrere Divisionen hat, fordert die Finanzierung eines Projekts nach Divisionen an.
-   Ihre Unternehmen teilt die Kosten eines umfangreichen Projekts mit einer externen Organisation.
-   Ein Straßenprojekt wird durch zwei Gemeinden finanziert.
-   Ein Brückenprojekt wird durch einen staatlicher Zuschuss und von einem Privatunternehmen finanziert.

In Finance and Operations können Sie die Rechnungsstellung für eine Transaktion oder ein gesamtes Projekt unter mehreren Debitoren, Zuschüssen oder Organisationen aufteilen. 

In Projekten mit mehreren Finanzierern werden alle Parteien, die zur Finanzierung eines erweiterten Finanzierungsprojekts beitragen, als Finanzierungsquellen bezeichnet. Nachdem ein Debitor, eine Organisation oder ein Zuschuss als Finanzierungsquelle definiert wurde, kann diese einer oder mehreren Finanzierungsregeln zugewiesen werden. Finanzierungsregeln enthalten die Kriterien, nach denen Zuordnungen verschiedener Finanzierungsquellen für ein Projekt vorgenommen werden. 

Da gelagerte Artikel, z. B. in Bestellanforderungen und Bestellungen, nicht geteilt werden können, kann der Kostenbetrag nicht auf mehrere Finanzierungsquellen zum Zeitpunkt der Verteilung aufgeteilt werden. Der Finanzierungsquellenwert bleibt folglich null, bis der Lagerbestand gebucht wurde. Wenn der Lagerabgang gebucht wird, wird der Kostenbetrag in Übereinstimmung mit den Kontoverteilungsregeln für das Projekt verteilt.

Nachfolgend finden Sie einige Schritte, die Sie ausführen können, um die Fakturierung auf mehrere Finanzierungsquellen aufzuteilen:

-   Geben Sie an, dass für alle Buchungen zu einem Projekt dieselbe Verkaufswährung im Projektvertrag verwenden.
-   Richten Sie Finanzierungslimits ein, sodass eine Finanzierungsquelle für ein Projekt nicht höher als mit dem angegebenen Betrag fakturiert wird.
-   Konfigurieren Sie Finanzierungsregeln und Finanzierungslimits für die einzelnen Arbeitskräfte, Artikel, Kategorien, Kategoriengruppen und Bankbuchungsarten (oder für die Buchungsarten insgesamt).
-   Wählen Sie ein optionales Start- und Enddatum für den Zeitraum, für den die jeweilige Finanzierungsregel gültig ist.
-   Geben Sie den Prozentsatz an, mit dem jede Finanzierungsquelle beteiligt ist.
-   Geben Sie die Finanzierungsquelle an, der Rundungsdifferenzen aus den Berechnungen der Finanzierungszuordnung zugewiesen werden sollen.
-   Richten Sie Regeln ein, die festlegen, wie Projektkosten für externe Debitoren fakturiert und wie sie internen Organisationen zugerechnet werden sollen.
-   Erfassen Sie Buchungen in einem gesperrten Finanzierungskonto, bis eine zusätzliche Finanzierung bereitsteht oder bis die Kosten intern übernommen werden.

Zur Bestimmung der Steuergruppe, die einer Buchung zugewiesen werden soll, wird das Projekt nach einer Steuergruppenzuweisung durchsucht. Wurde auf Projektebene keine Steuergruppenzuweisung vorgenommen, wird nach dem Projektvertrag gesucht.

### <a name="example-multiple-funding-sources-simple"></a>Beispiel: Mehrere Finanzierungsquellen (einfach)

Die folgende Tabelle enthält Szenarien für die Verwaltung der Finanzierungszuteilung mir mehreren Finanzierungsquellen. Diese Szenarien basieren auf den folgenden Annahmen:

-   Die Prioritätseinstellungen werden in die Zuweisung von Geldmitteln einbezogen, bevor andere Finanzierungsregelkriterien angewendet werden.
-   Kein Datumsbereich ist angegeben worden, um die Periode zu definieren, in der die Finanzierungsregel gültig ist.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Szenario</strong></td>
<td><strong>Finanzierungsquelle </strong></td>
<td><strong>Zuteilung in Prozent </strong></td>
<td><strong>Zuweisungspriorität </strong></td>
</tr>
<tr class="even">
<td>Sie möchten einer Finanzierungsquelle Kosten zuweisen, bis die Mittel erschöpft sind, dann einer zweiten Finanzierungsquelle Kosten zuweisen, bis die Mittel erschöpft sind, und die verbleibenden Kosten schließlich einer dritten Finanzierungsquelle zuweisen.</td>
<td><ul>
<li>Finanzierungsquelle 1</li>
<li>Finanzierungsquelle 2</li>
<li>Finanzierungsquelle 3</li>
</ul></td>
<td><ul>
<li>100 %</li>
<li>100 %</li>
<li>100 %</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
<li>3</li>
</ul></td>
</tr>
<tr class="odd">
<td>Sie möchten 75 Prozent der Kosten einer Finanzierungsquelle und 25 Prozent der Kosten einer zweiten Finanzierungsquelle zuweisen. Wenn eine dieser Finanzierungsquellen erschöpft ist, möchten Sie die verbleibenden Kosten aus einer dritten Finanzierungsquelle decken.</td>
<td><ul>
<li>Finanzierungsquelle 1</li>
<li>Finanzierungsquelle 2</li>
<li>Finanzierungsquelle 3</li>
</ul></td>
<td><ul>
<li>75 %</li>
<li>25 %</li>
<li>100 %</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
<tr class="even">
<td>Sie möchten 75 Prozent der Kosten einer Finanzierungsquelle und 25 Prozent der Kosten einer zweiten Finanzierungsquelle zuweisen. Wenn eine der beiden Finanzierungsquellen erschöpft ist, möchten Sie die verbleibenden Kosten zwischen einer dritten und vierten Finanzierungsquelle aufteilen.</td>
<td><ul>
<li>Finanzierungsquelle 1</li>
<li>Finanzierungsquelle 2</li>
<li>Finanzierungsquelle 3</li>
<li>Finanzierungsquelle 4</li>
</ul></td>
<td><ul>
<li>75 %</li>
<li>25 %</li>
<li>50 %</li>
<li>50 %</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
<li>2</li>
</ul></td>
</tr>
<tr class="odd">
<td>Sie möchten die ersten 25 Prozent der Kosten einer Finanzierungsquelle und den Rest der zweiten Finanzierungsquelle zuweisen.</td>
<td><ul>
<li>Finanzierungsquelle 1</li>
<li>Finanzierungsquelle 2</li>
</ul></td>
<td><ul>
<li>25 %</li>
<li>100 %</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a>Beispiel Mehrere Finanzierungsquellen (komplex)

Sie haben drei Finanzierungsquellen, und Sie möchten sie in der folgenden Reihenfolge verwenden:

1.  Verwenden Sie Finanzierungsquelle 2 und Finanzierungsquelle 3 zu gleichen Teilen, bis Finanzierungsquelle 2 erschöpft ist.
2.  Fahren Sie mit der Nutzung von Finanzierungsquelle 3 fort, bis sie erschöpft ist.
3.  Verwenden Sie Finanzierungsquelle 1, nachdem Finanzierungsquelle 3 erschöpft ist.

Um dies zu erreichen, gehen Sie folgendermaßen vor:

-   Richten Sie Finanzierungslimits für Finanzierungsquelle 2 und Finanzierungsquelle 3 für die entsprechenden Beträge ein.
-   Erstellen Sie die folgenden Finanzierungsregeln:
    -   Regel 1 (Priorität 1): Weisen Sie 50 Prozent der Buchungen der Finanzierungsquelle 2 und 50 Prozent der Buchungen der Finanzierungsquelle 3 zu.
    -   Regel 2 (Priorität 2): Weisen Sie 100 Prozent der Buchungen der Finanzierungsquelle 3 zu.
    -   Regel 3 (Priorität 3): Weisen Sie 100 Prozent der Buchungen der Finanzierungsquelle 1 zu.

Diese Einstellung funktioniert, da bei Buchungen alle Regeln und Grenzwerte auf ihre Relevanz für die aktuell auszuführende Buchung geprüft werden. Wenn keine Regeln oder Grenzwerte für die Buchung gelten, trifft die Regel Alle Buchungen zu. Die Regel "Alle Buchungen" gilt für alle Buchungen. 

Wenn das System eine Regel findet, die einer bestimmten Buchung entspricht, wird der Prozentsatz zunächst nach dieser Regel zugewiesen, aber erst angewendet, nachdem die restlichen Grenzwerte geprüft werden, die eingerichtet worden sind. Wenn ein Grenzwert erreicht wurde und die Mittel einer Finanzierungsquelle erschöpft sind, wird die dem Finanzierungsgrenzwert zugeordnete Finanzierungsregel ignoriert und die nächste Regel gesucht, die anwendbar ist. 

In einigen Fällen kann nur ein Teil der Buchung anhand einer Regel zugewiesen werden. Dies kann der Fall sein, wenn ein Grenzwert beim Zuweisen der Buchung erreicht wird. In diesem Fall wird nur ein bestimmter Betrag gemäß der Regel zugewiesen, beispielsweise jeder Finanzierungsquelle 50 Prozent. Dies ist gewöhnlich bei Regel 1 der Fall (weiter oben in diesem Abschnitt beschrieben). Der Rest wird gemäß der nachfolgenden Regel in der Sequenz zugewiesen. 

In der folgenden Tabelle wird dieses Szenario detaillierter überprüft.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Fokus </strong></td>
<td><strong>Detailinformationen </strong></td>
</tr>
<tr class="even">
<td>Finanzierungsregeln</td>
<td><ul>
<li>Regel 1 (Priorität 1): Alle Buchungen. Finanzierungsquelle 2 50% und Finanzierungsquelle 3 50% zuweisen.</li>
<li>Regel 2 (Priorität 2): Alle Buchungen. Finanzierungsquelle 3 100% zuweisen.</li>
<li>Regel 3 (Priorität 2): Alle Buchungen. Finanzierungsquelle 1 100% zuweisen.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Finanzierungslimits</td>
<td><ul>
<li>Grenzwert für Finanzierungsquelle 1 = 10.000,00</li>
<li>Grenzwert für Finanzierungsquelle 2 = 500,00</li>
<li>Grenzwert für Finanzierungsquelle 3 = 750,00</li>
</ul></td>
</tr>
<tr class="even">
<td>Buchung 1</td>
<td><strong>Buchungsbetrag:</strong> 100,00<strong>Finanzierung:</strong> Die Buchung wurde nur gemäß Regel 1 bezahlt, da die Buchung vollständig bezahlt ist, nachdem Regel 1 angewendet wurde. Die Buchung wird zu gleichen Teilen von Finanzierungsquelle 2 und Finanzierungsquelle 3 finanziert.
<ul>
<li>Finanzierungsquelle 2: 50,00</li>
<li>Finanzierungsquelle 3: 50,00</li>
</ul></td>
</tr>
<tr class="odd">
<td>Buchung 2</td>
<td><strong>Buchungsbetrag:</strong> 5.000,00<strong>Finanzierung:</strong> Die Zahlung der Buchung gemäß allen drei <strong>Regeln</strong>
<ul>
<li>Finanzierungsquelle 2: 450,00</li>
<li>Finanzierungsquelle 3: 450,00</li>
</ul>
<strong>Regel 2</strong>
<ul>
<li>Finanzierungsquelle 3: 250,00 (= 750,00 – 50,00 – 450,00)</li>
</ul>
<strong>Regel 3</strong>
<ul>
<li>Finanzierungsquelle 1: 3.850,00 (= 5.000,00 – 450,00 – 450,00 – 250,00)</li>
</ul></td>
</tr>
<tr class="even">
<td>Gesamtbeträge, die auf die einzelnen Finanzierungsquellen verteilt werden</td>
<td><ul>
<li>Finanzierungsquelle 1: 3.850,00</li>
<li>Finanzierungsquelle 2: 500,00</li>
<li>Finanzierungsquelle 3: 750,00</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a>Abrechnungsregeln
Wenn Sie mit einem Debitor einen Projektvertrag aushandeln, legen Sie fest, wie und wann dem Debitor Rechnungen für Arbeit an einem Projekt ausgestellt werden können. Nachdem Sie den Projektvertrag und das Projekt eingerichtet haben, können Sie Fakturierungsregeln für das Projekt einrichten. Fakturierungsregeln basieren auf den Projektbedingungen, die im Projektvertrag angegeben wurden. Die Fakturierungsregeln, die erstellt werden können, hängen von den Bedingungen im Projektvertrag und dem der Fakturierungsregel zugeordneten Projekttyp ab, z. B. Termin und Material, Festpreis oder Meilenstein. Sie können mehrere Fakturierungsregeln für einen Projektvertrag erstellen. Sie können eine Fakturierungsregel auch mehreren Projekten zuweisen, die dem gleichen Projektvertrag zugeordnet sind und ähnliche Rechnungsstellungsbedingungen haben. 

Sie können folgende Arten von Fakturierungsregeln einrichten:

-   **Liefereinheit** – Rechnungsstellung an einen Debitor, wenn Sie eine Liefereinheit abschließen. Sie definieren die Liefereinheiten im Vertrag.
-   **Fortschritt** – Rechnungsstellung an einen Debitor erfolgt beim Abschluss eines angegebenen Prozentsatzes des Projekts. Sie können eine Fakturierungsregel einrichten, um den Prozentsatz der abgeschlossenen Arbeit automatisch zu berechnen, oder Sie können den abgeschlossenen Prozentsatz der Arbeit und des Betrags manuell berechnen, der dem Debitor in Rechnung gestellt wird.
-   **Meilenstein** – Der vollständige Betrag für einen Meilenstein wird dem Debitor beim Erreichen eines Projektmeilensteins in Rechnung gestellt.
-   **Gebühr** – Es erfolgt die Rechnungsstellung an den Debitor hinsichtlich der Dienstleistungen und einer Verwaltungsgebühr (normalerweise ein Prozentsatz der Dienstleistungskosten).
-   **Nach Aufwand** – Berechnen Sie einem Debitor eine Rechnung die Stunden und Materialien für ein Projekt.

Für alle Typen von Fakturierungsregeln können Sie einen einzubehaltenden Prozentsatz angeben, der von einer Debitorenrechnung abzuziehen ist, bis ein Projekt eine vereinbarte Phase erreicht. Der Zahlungseinbehaltungsprozentsatz wird im Projektvertrag angegeben. Der Betrag wird an berechnet und abgezogen vom Gesamtwert der Positionen in einer Debitorenrechnung. 

Für **Zeit und Aufwand** und **Fortschritt**-Fakturierungsregeln können Sie fakturierbare Kategorien zuweisen. Fakturierbare Kategorien geben die Buchungen an, die in die Debitorenrechnungen eingeschlossen werden sollen. 

Wenn eine Rechnung für den Debitor ausgestellt werden kann, wird der für das Projekt in Rechnung zu stellende Betrag auf Grundlage der Fakturierungsregeln berechnet, und es wird ein Vorschlag für eine Projektrechnung generiert. 

In den folgenden Abschnitten finden Sie Beispiele, die zeigen, wie eine Fakturierungsregel für ein Projekt eingerichtet und verwaltet wird.

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a>Beispiel: Erstellen einer Fakturierungsregel auf Grundlage der Anzahl gelieferter Einheiten

Ihre Organisation vereinbart, insgesamt fünf Schulungssitzungen für die Mitarbeiter eines Debitors mit Kosten von 10.000 Euro pro Schulung bereitzustellen. Sie stellen bei Abschluss jeder Schulungssitzung eine Rechnung an den Debitor aus. 

Bei der Einrichtung der Fakturierungsregeln für den Vertrag verwenden Sie die folgenden Werte:

-   Die Liefereinheit ist eine Schulungssitzung.
-   Der Preis je Einheit beträgt 10.000 Euro pro Schulungssitzung.
-   Die Gesamtanzahl von Einheiten ist fünf Schulungssitzungen.

Wenn Sie eine Schulungssitzung abgeschlossen haben, können Sie eine Rechnung über 10.000 Euro für die erste gelieferte Einheit erstellen und die Rechnung an den Debitor senden.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a>Beispiel: Erstellen einer Fakturierungsregel auf Grundlage eines angegebenen Prozentsatzes der Projektfertigstellung (manuelle Berechnung)

Ihre Organisation, eine Softwareberatungsfirma, vereinbart mit einem Debitor, einen Teil eines Produkts zu entwickeln, das der Debitor entwickelt. Ihre Organisation sagt zu, den Softwarecode über einen Zeitraum von sechs Monaten zu liefern. Der Debitor erklärt sich einverstanden, Ihrer Organisation insgesamt 100.000 Euro für die Arbeit zu bezahlen. Sie erstellen eine Fakturierungsregel, um dem Debitor auf Grundlage eines Prozentsatzes, zu dem die Arbeit am Projekt gemäß Vertrag abgeschlossen wurde, eine Rechnung zu stellen.

-   Am Ende des ersten Monats ermitteln Sie in einer Besprechung mit dem Debitor den abgeschlossenen Prozentsatz der Arbeit. Nach einer Prüfung des Projekts durch Sie und den Debitor entscheiden Sie, dass 15 % des Projekts abgeschlossen sind.
-   Sie erstellen eine Rechnung in Höhe von 15.000 Euro (15 % von 100.000 Euro) und senden sie an den Debitor.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a>Beispiel: Erstellen einer Fakturierungsregel auf Grundlage eines angegebenen Prozentsatzes der Projektfertigstellung (automatische Berechnung)

Ihre Organisation, eine Softwareentwicklungsfirma, entwickelt ein Lohnbuchhaltungspaket für einen Debitor für 30.000 Euro. Der Debitor erklärt sich einverstanden, Ihre Organisation basierend auf dem abgeschlossenen Prozentsatz der Arbeit zu bezahlen. Ihre Vorkalkulation der Projektkosten beläuft sich auf 20.000 Euro. Die im Abrechnungsprozess zu verwendenden Arbeitskategorien sind im Projektvertrag festgelegt. Sie richten Fakturierungsregeln ein, durch die die Rechnungsbeträge für den abgeschlossenen Prozentsatz der Arbeit für jede Kategorie automatisch berechnet werden. Sie richten ein Budget für jede Kategorie ein:

-   **Entwicklung** – Kosten von 15.000 Euro und Umsatzerlös von 20.000 Euro
-   **Installation** – Kosten von 5.000 Euro und Umsatzerlös von 10.000 Euro.

Bei der ersten Rechnungsstellung an den Debitor wird der Rechnungsbetrag automatisch anhand der folgenden Informationen berechnet:

-   Nach einem Monat sendet die Arbeitskraft bei dem Projekt einen Arbeitszeitnachweis für das Projekt. Die Kosten für die Arbeitsstunden der Arbeitskraft belaufen sich auf 5.000 Euro für Entwicklung und 1.000 Euro für Installation. Die Entwicklungsarbeit ist zu 33 Prozent abgeschlossen (5.000 Euro tatsächliche Kosten/15.000 Euro Budgetkosten), und die Installationsarbeit ist zu 20 Prozent abgeschlossen (1.000 Euro tatsächliche Kosten/5.000 Euro Budgetkosten).
-   Der Rechnungsbetrag von 8.667 wird automatisch berechnet (33 Prozent von 20.000 plus 20 Prozent von 10.000).
-   Sie erstellen eine Rechnung in Höhe von 8.667 Euro und senden sie an den Debitor.

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a>Beispiel: Erstellen einer Fakturierungsregel auf Grundlage vereinbarter Meilensteine

Ihre Organisation, eine Unternehmensberatungsfirma, führt eine Marktforschung für ein Produkt durch, das der Debitor zu verkaufen plant. Der Debitor erklärt sich einverstanden, Ihre Dienstleistungen ab März für einen Zeitraum von drei Monaten in Anspruch zu nehmen und Ihrer Organisation 50.000 Euro zu bezahlen. Das Projekt umfasst drei Meilensteine:

-   Meilenstein 1: Sammeln von Verbraucherdaten – 31. März
-   Meilenstein 2: Analyse der Verbraucherdaten – 30. April
-   Meilenstein 3: Präsentation eines Realisierbarkeitsplans für das Produkt – 31. Mai

Der Debitor erklärt sich einverstanden, Ihrer Organisation 10.000 Euro für den ersten Meilenstein und jeweils 20.000 Euro für den zweiten und dritten Meilenstein zu bezahlen. 

Beim Einrichten des Projektvertrags vereinbaren Sie, basierend auf den abgeschlossenen Meilensteinen Rechnungen an den Debitor auszustellen. Zum Einrichten der Fakturierungsregel führen Sie die folgenden Schritte aus:

-   Definieren Sie die Projektmeilensteine.
-   Definieren Sie den Betrag, der dem Debitor beim Erreichen des Projektmeilensteins in Rechnung gestellt wird.

Nach Abschluss des ersten Meilensteins am 31. März markieren Sie diesen als abgeschlossen und erstellen eine Rechnung über 10.000 Euro und senden sie an den Debitor. Sie können eine Rechnung für einen Meilenstein erst erstellen, wenn Sie den Meilenstein als abgeschlossen markiert haben.

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a>Beispiel: Erstellen einer Fakturierungsregel auf Grundlage von Dienstleistungen und einer Verwaltungsgebühr

Ihre Organisation führt Managementberatungen durch. Sie führt eine Marktforschung zur Bewertung der Realisierbarkeit eines beim Debitor in der Entwicklung befindlichen Produkts durch. Die Vereinbarungen legen fest, die Dienstleistungen Ihrer drei besten Unternehmensberater für die Marktforschung auf Aufwandsbasis bereitzustellen. Der Debitor stimmt zu, einen Stundensatz von 100 Euro und eine zusätzliche Verwaltungsgebühr von 10 Prozent für die anfallenden Beratungsstunden für das Projekt zu zahlen. 

Beim Einrichten des Projektvertrags erstellen Sie eine Fakturierungsregel, mit der eine Verwaltungsgebühr von 10 Prozent zu den berechneten Beratungsstunden für das Projekt addiert wird. 

Wenn Sie eine Rechnung für den Debitor erstellen, wird dem Debitor zusätzlich zu den Kosten der Beratungsstunden eine Verwaltungsgebühr von 10 Prozent in Rechnung gestellt. Wenn die drei Berater z. B. insgesamt 200 Stunden am Projekt gearbeitet haben, wird anhand der folgenden Berechnung eine Rechnung in Höhe von 22.000 Euro erstellt:

-   200 Stunden zu 100 Euro pro Stunde = 20.000 Euro
-   10-Prozent-Bearbeitungsgebühr = 2.000
-   Gesamter Rechnungsbetrag = 22.000

Wenn Gebühren für einen Debitor steuerpflichtig sind und Sie eine Mehrwertsteuergruppe im Projektvertrag auswählen, wird die Mehrwertsteuergruppe automatisch in eine Fakturierungsregel für Gebühren eingegeben.

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a>Beispiel: Erstellen einer Fakturierungsregel für die Aufwandskosten

Ihre Organisation führt Softwareberatungen durch, und hat mit dem Debitor vereinbart, fünf technische Berater für ein Softwareentwicklungsprojekt die nächsten sechs Monate bereitzustellen. Der Debitor erklärt sich damit einverstanden, einen Betrag von 150 Euro für jede Beratungsstunde und die Kosten für das Büromaterial zu bezahlen. Ihre Organisation sendet am Ende jedes Monats eine Rechnung an den Debitor. 

Beim Einrichten des Projektvertrags können Sie zustimmen, den Debitor monatlich für den Aufwand für das Projekt zu fakturieren. Sie erstellen eine Fakturierungsregel die die folgenden Informationen beinhaltet:

-   Die Vertragsdauer beträgt sechs Monate.
-   Die Beratungsdauer wird mit einem Satz von 150 Euro pro Stunde berechnet.
-   Büromaterial wird zu Anschaffungskosten in Rechnung gestellt. Dabei darf die Summe für das Projekt maximal 10.000 Euro betragen.
-   Während des Projekts erstellen Sie am Ende jedes Kalendermonats eine Debitorenrechnung.

Im ersten Monat wurden von den Beratern insgesamt 800 Stunden im Projekt erfasst. Die Kosten für das Büromaterial, die für das Projekt berechnet werden, betragen 2.000 Euro. Am Ende des Monats erstellen Sie eine Rechnung über 122.000, berechnet als 800 Stunden zu 150 pro Stunde plus 2.000 für Büromaterial.




