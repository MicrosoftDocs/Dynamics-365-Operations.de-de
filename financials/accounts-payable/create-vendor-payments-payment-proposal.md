---
title: Kreditorenrzahlung unter Verwendung eines Zahlungsvorschlags erstellen
description: "Dieser Artikel gibt einen Überblick über die Zahlungsvorschlagsoptionen und umfasst einige Beispiele, die zeigen, wie Zahlungsvorschläge funktionieren. Zahlungsvorschläge werden oft verwendet, um Kreditorenzahlungen zu erstellen, da die Abfrage dazu verwendet werden kann, Kreditorenrechnungen für die Zahlung, basierend auf Kriterien wie dem Fälligkeitsdatum und dem Skonto, schnell auszuwählen."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/17/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14312
ms.assetid: 585d5b0b-1b79-4a03-ab18-528918070377
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: aac70abc25c45ef4479425cdb648f4450d5db2dc
ms.contentlocale: de-de
ms.lasthandoff: 07/27/2017

---

# <a name="create-vendor-payments-by-using-a-payment-proposal"></a>Kreditorenrzahlung unter Verwendung eines Zahlungsvorschlags erstellen

[!include[banner](../includes/banner.md)]


Dieser Artikel gibt einen Überblick über die Zahlungsvorschlagsoptionen und umfasst einige Beispiele, die zeigen, wie Zahlungsvorschläge funktionieren. Zahlungsvorschläge werden oft verwendet, um Kreditorenzahlungen zu erstellen, da die Abfrage dazu verwendet werden kann, Kreditorenrechnungen für die Zahlung, basierend auf Kriterien wie dem Fälligkeitsdatum und dem Skonto, schnell auszuwählen. 

Organisationen verwenden oft Zahlungsvorschläge, um Kreditorenzahlungen zu erstellen, da die Zahlungsvorschlagsabfrage verwendet werden kann, um Kreditorenrechnungen für die Zahlung, basierend auf dem Fälligkeitsdatum, dem Skonto und andere Kriterien, schnell auszuwählen. 

Die Zahlungsvorschlagsabfrage enthält verschiedene Registerkarten. Jede davon hat unterschiedliche Optionen für das Auswählen von Rechnungen, die zu zahlen sind. Die Registerkarte **Parameter** enthält Optionen, die die Mehrheit der Organisationen am häufigsten verwenden. Im Inforegister **Datensätze einbeziehen** können Sie angeben, welche Rechnungen oder Kreditoren für Zahlungen einzubeziehen sind, indem Bereiche für verschiedene Merkmale definiert werden. Wenn Sie beispielsweise nur einen bestimmten Bereich von Kreditoren zahlen möchten, können Sie einen Filter für den Kreditorenbereich definieren. Diese Funktion wird häufig verwendet, um Rechnungen für eine bestimmte Zahlungsmethode auszuwählen. Wenn Sie beispielsweise einen Filter unter **Zahlungsmethode** = **Scheck** definieren, werden nur Rechnungen ausgewählt, die dieser Zahlungsmethode entsprechen, vorausgesetzt, dass diese auch anderen Kriterien entsprechen, die in der Abfrage angegebenen sind. Die Registerkarte **Erweiterte Parameter** enthält zusätzliche Optionen, von denen einige möglicherweise für Ihre Organisation nicht relevant sind. So enthält diese Registerkarte beispielsweise die Optionen für die Bezahlung von Rechnungen für zentralisierte Zahlungen.

## <a name="parameters"></a>Parameter
-   **Wählen Sie Rechnungen nach**  – Rechnungen innerhalb des Datumsbereichs aus, der nach ** **Von-Datum** angegeben wird und **Bis-Datum** ** Felder definiert wird und nach Fälligkeitsdatum, Skontodatum oder beidem aktiviert werden kann. Wenn Sie das Skontodatum verwenden, sucht das System zuerst nach Rechnungen, die zwischen dem Von-Datum und dem Bis-Datum liegen. Das System bestimmt dann, ob die Rechnung für das Skonto berechtigt ist, indem es Sitzungsdatum verwendet, um zu überprüfen, dass das Skontodatum nicht bereits verstrichen ist.
-   **Von Datum** und **Bis Datum** – Rechnungen, die ein Fälligkeitsdatum oder Skontodatum innerhalb dieses Datumsbereichs haben, werden zur Zahlung ausgewählt.
-   **Zahlungsdatum** – Dieses wird nur verwendet, wenn das Feld **Zeitraum** für die Zahlungsmethode auf **Summe** gesetzt ist. Wenn ein Datum definiert ist, werden alle Zahlungen an diesem Datum erzeugt. Das Feld **Mindestzahlungsdatum** wird ignoriert.
-   **Mindestzahlungsdatum** – Geben Sie das Mindestzahlungsdatum ein. Beispielsweise zeigen die Felder **Von-Datum** und **Bis Datum** einen Bereich vom 1. September bis zum 10. September anzeigen und das und das Mindestzahlungsdatum ist.am 5. September In diesem Fall haben alle Rechnungen ein Fälligkeitsdatum vom 1. September bis zum 5. September und ein Zahlungsdatum vom 5. September. Allerdings haben alle Rechnungen, die ein Fälligkeitsdatum vom 5. September bis zum 10. September, ein Zahlungsdatum, das dem Fälligkeitsdatum jeder Rechnung entspricht.
-   **Betragsgrenze** – Geben Sie den maximalen Gesamtbetrag für alle Zahlungen ein.
-   **Erstellen Sie Zahlungen ohne Rechnungsvorschau** – Wenn Sie die Option auf **Ja** festlegen, werden Zahlungen umgehend auf der Seite **Kreditorenzahlungen** erstellt. Die Seite **Zahlungsvorschlag** wird übersprungen. Daher werden Zahlungen schneller erstellt. Zahlungen können von der Seite **Kreditorenzahlungen** aus immer noch geändert werden. Alternativ können Sie zur Seite **Zahlungsvorschlag** zurückkehren, indem Sie die Schaltfläche **Rechnungen für ausgewählte Zahlung bearbeiten** verwenden.

## <a name="advanced-options"></a>Erweiterte Optionen
-   **Kreditorensaldo überprüfen** – Wenn diese Option auf **Ja** festgelegt ist, prüft das System, ob der Kreditor kein Sollsaldo hat, bevor irgendeine Rechnung bezahlt wird. Wenn ein Kreditor einen Sollsaldo hat, wird keine Zahlung erstellt. So kann beispielsweise der Kreditor Zahlungen oder Gutschriften haben, die gebucht wurden, jedoch noch nicht ausgeglichen wurden. In diesen Fällen sollte dem Kreditor nicht bezahlt werden. Stattdessen sollten die Gutschriften oder die Zahlungen für die ausstehenden Rechnungen ausgeglichen werden.
-   **Negative Zahlungen löschen** – Diese Option funktioniert unterschiedlich, je nachdem, ob Zahlungen für einzelne Rechnungen oder für die Summe der Rechnungen erfolgen, die die Zahlungskriterien erfüllen. Dieses Verhalten wird bei der Zahlungsmethode definiert.
-   **Zahlung für jede Rechnung** – Wenn die Option **Negative Zahlungen löschen** auf **Ja** festgelegt ist und eine nicht beglichene Rechnung und Zahlung für einen Kreditor vorhanden sind, wird nur die Rechnung zur Zahlung ausgewählt. Die vorhandene Zahlung wird nicht mit der Rechnung ausgeglichen. Wenn die Option **Negative Zahlungen löschen** auf **Nein** festgelegt ist und eine Rechnung sowie eine Zahlung nicht ausgeglichen werden, werden sowohl die Rechnung als auch die Zahlung zur Zahlung ausgewählt. Eine Zahlung wird für die Zahlung erstellt, und eine Rückerstattung (negative Zahlung) wird für die Zahlung erstellt.
-   **Zahlung für Summe der Rechnungen** – Wenn die Option **Negative Zahlungen löschen** auf **Ja** festgelegt ist und eine nicht ausgeglichene Rechnung und Zahlung für einen Kreditor vorhanden sind, werden sowohl die nicht ausgeglichene Rechnung als auch die Zahlung zur Zahlung ausgewählt, und die Beträge werden zusammengezählt, um den gesamten Zahlungsbetrag zu erzeugen. Die einzige Ausnahme tritt auf, wenn die Summe zu einer Rückerstattung führt. In diesem Fall wird weder die Rechnung noch die Zahlung ausgewählt. Wenn die Option **Negative Zahlungen löschen** auf **Nein** festgelegt ist und eine Rechnung und eine Zahlung nicht ausgeglichen sind, werden sowohl die Rechnung als auch die Zahlung zur Zahlung ausgewählt, und die Beträge werden zusammengezählt, um den gesamten Zahlungsbetrag zu erzeugen.
-   **Nur Druckbericht** – Legen Sie diese Option auf **Ja** fest, um die Ergebnisse des Zahlungsvorschlags in einem Bericht zu sehen, aber, ohne irgendwelche Zahlungen zu erstellen.
-   **Kreditorenrechnungen aus anderen juristischen Personen einbeziehen** – Wenn in Ihrer Organisation ein zentralisierte Prozess für Zahlungen vorhanden ist und der Zahlungsvorschlag Rechnungen von anderen juristischen Personen einbeziehen sollte, die in den Suchkriterien enthalten sind, legen Sie diese Option auf **Ja** fest.
-   **Separate Kreditorenzahlung pro juristischer Person vorschlagen** – Wenn diese Option auf **Ja** festgelegt ist, wird eine separate Zahlung für jede juristische Person pro Kreditor erstellt. Der Kreditor auf der Zahlung ist der Kreditor aus der Rechnung von jeder juristischen Person. Wenn diese Option auf **Nein** festgelegt ist und derselbe Kreditor Rechnungen in mehreren juristischen Personen hat, wird eine Zahlung für den Gesamtbetrag der ausgewählten Rechnungen erstellt. Der Kreditor zur Zahlung ist der Kreditor in der aktuellen juristischen Person. Wenn das Kreditorenkonto in der aktuellen juristischen Person nicht vorhanden ist, wird das Kreditorenkonto der ersten zu bezahlenden Rechnung verwendet.
-   **Zahlungswährung**  – Dieses Feld gibt die Währung an, in der alle Zahlungen erstellt werden. Wenn eine Währung nicht definiert ist, wird die Rechnung in der Währung der Rechnung bezahlt.
-   **Wochentag für Zahlung** – Geben Sie den Wochentag ein, an dem die Zahlung erfolgen soll. Dieses Feld wird nur verwendet, wenn die Zahlungsmethode für gesamte Rechnungen zur Zahlung an einem bestimmten Wochentag eingerichtet ist.
-   **Gegenkontenart** und **Gegenkonto** - Legen Sie diese Felder fest, um einen bestimmten Typ des Kontos (wie **Sachkonto** oder **Bank**) und Gegenkonto (wie ein bestimmtes Ausgleichskonto) zu definieren. Die Zahlungsmethode für die Rechnung legt die Standardgegenkontenart und das Gegenkonto fest, doch Sie können diese Felder verwenden, um die Standardwerte zu überschreiben.
-   **Zusätzliche Filter**– Im Inforegister **Einzubeziehen Datensätze** können Sie weitere Bereiche von Kriterien definieren. Wenn Sie beispielsweise nur einen bestimmten Bereich von Kreditoren zahlen möchten, können Sie einen Filter für den Kreditorenbereich definieren. Diese Funktion wird häufig verwendet, um Rechnungen für eine bestimmte Zahlungsmethode auszuwählen. Wenn Sie beispielsweise einen Filter unter **Zahlungsmethode** = **Scheck** definieren, werden nur Rechnungen ausgewählt, die dieser Zahlungsmethode entsprechen, vorausgesetzt, dass diese auch anderen Kriterien entsprechen, die in der Abfrage angegebenen sind.

## <a name="scenarios"></a>Szenarien
| Händler | Rechnung | Rechnungsdatum | Rechnungsbetrag | Fälligkeitsdatum | Skontodatum | Skontobetrag |
|--------|---------|--------------|----------------|----------|--------------------|----------------------|
| 3050   | 1001    | 15. Juni      | 500,00         | 15. Juli  | 29. Juni            | 10,00                |
| 3050   | 1002    | 20. Juni      | 600,00         | 20. Juli  | 4. Juli             | 12,00                |
| 3075   | 1003    | 15. Juni      | 250,00         | 29. Juni  |                    | 0,00                 |
| 3100   | 1004    | 17. Juni      | 100,00         | 17. Juli  | 1. Juli             | 1,00                 |

Am 1. Juli zahlt April Kreditoren aus. Sie verwendet einen Zahlungsvorschlag, um diese Aufgabe effizienter durchzuführen.

### <a name="option-1-by-cash-discount"></a>Option 1:Nach Skonto

April wählt **Skonto** als Vorschlagstyp aus. Sie gibt einen Datumsbereich vom 26. Juni bis zum 10. Juli ein. Die nachfolgenden Rechnungen werden in den Vorschlag einbezogen:

-   1002, da das Skontodatum vom 4. Juni im Bereich der Zahlungsdaten ist.
-   1004, da das Skontodatum vom 1. Juni im Bereich der Zahlungsdaten ist.

Die nachfolgenden Rechnungen werden nicht in den Vorschlag einbezogen:

-   1001, da das Rabattdatum vom 29. Juni bereits abgelaufen ist, ist diese Rechnung daher nicht mehr für das Skonto freigegeben.
-   1003, da diese Rechnung kein Rabattdatum hat.

### <a name="option-2-by-due-date"></a>Option 2: Nach Fälligkeitsdatum

April wählt **Nach Fälligkeitsdatum** als Vorschlagstyp aus. Sie gibt einen Datumsbereich vom 26. Juni bis zum 10. Juli ein. Die nachfolgenden Rechnungen werden in den Vorschlag einbezogen:

-   1003, da das Fälligkeitsdatum vom 29. Juni im Bereich der Zahlungsdaten ist.

Die nachfolgenden Rechnungen werden nicht in den Vorschlag einbezogen:

-   1001, da das Fälligkeitsdatum vom 15. Juni außerhalb des Bereichs der Zahlungsdaten ist.
-   1002, da das Fälligkeitsdatum vom 20. Juni außerhalb des Bereichs der Zahlungsdaten ist.
-   1004, da das Fälligkeitsdatum vom 17. Juni außerhalb des Bereichs der Zahlungsdaten ist.

### <a name="option-3-by-due-date-and-cash-discount"></a>Option 3: Nach Fälligkeitsdatum und Skonto

April wählt **Fälligkeitsdatum und Skonto** als Vorschlagstyp aus. Sie gibt einen Datumsbereich vom 26. Juni bis zum 10. Juli ein. Die nachfolgenden Rechnungen werden in den Vorschlag einbezogen:

-   1003, da das Fälligkeitsdatum vom 29. Juni im Bereich der Zahlungsdaten ist.
-   1002, da das Skontodatum vom 4. Juni im Bereich der Zahlungsdaten ist.
-   1004, da das Skontodatum vom 1. Juni im Bereich der Zahlungsdaten ist.

Die nachfolgenden Rechnungen werden nicht in den Vorschlag einbezogen:

-   1001, da das Rabattdatum vom 29. Juni bereits abgelaufen ist, ist daher diese Rechnung nicht mehr für den Skonto freigegeben, und das Fälligkeitsdatum vom 15. Juli ist auch außerhalb des Datumsbereichs.

## <a name="country-specific-considerations"></a>Landesspezifische Betrachtungen
### <a name="norway"></a>Norwegen

#### <a name="dimension-control"></a>Dimensionskontrolle

Mit der Dimensionssteuerung können Steuergruppierung von generierten Positionen durch Zahlungsvorschlags- und Satzstandarddimensionen auf Grundlage der Finanzdimensionen für die angewendeten Rechnungen verwenden. Unter norwegischem Landkontext besteht für jede Zahlungsmethode eine Registerkarte "Finanzdimensionen", in der Sie die Dimensionskontrolle sowie Gruppierungen für jede Dimension aktivieren können. Mögliche Optionen sind:

-   Das Feld **Dimensionskontrolle** wird deaktiviert. Der Zahlungsvorschlag verhält sich wie für jedes andere Land.
-   Das Feld **Dimensionskontrolle** ist ohne weitere Definition der Dimensionen aktiviert. Der Zahlungsvorschlag wird erstellt, ohne Dimensionen des Artikeleingangs zu berücksichtigen. Die erstellte Buchung übernimmt keine Dimensionen auf dem angewendeten Eintrag.
-   Das Feld **Dimensionskontrolle** ist und die weiteren Dimensionen sind aktiviert. Jetzt können Sie definieren, wie die Dimensionen in das Journal kopiert werden. Beispiel: • Wählen Sie das **BusinessUnit** Kontrollkästchen, um einen Zahlungsvorschlag pro Unternehmenseinheit für die Zahlungsmethode zu erstellen, • Wählen Sie das **CostCenter**, um für die Zahlungsmethode einen Zahlungsvorschlag pro Kostenstelle zu erstellen

**Hinweis:** Bei Auswahl mehrerer Dimensionen wird eine dritte Option, ein Zahlungsvorschlag für die ausgewählte Kombination aus Dimensionen erstellt.

#### <a name="bank-account-selection"></a>Bankkontoauswahl

Sie können ein Zahlungsstandardkonto pro Zahlungsmethode definieren, unbeachtet den Landkontext. Dies wird in Zahlungspositionen festgelegt, die durch einen Vorschlag generiert werden. Mit der Bankkontofunktion können Sie mehrere Bankkonten definieren, die nach Dimension und Währung oder einer Kombination dieser verwaltet wird, um verschiedene belastende Bankkonten zu nutzen, abhängig von der Kombination. Sie können diese Kombinationen auf der Seite **Zahlungsmahethoden** einrichten, indem Sie die Schaltfläche **Bankkonten** verwenden, die für jede Zahlungsmethode mit **Buchungskontotyp**  = **Bank** verfügbar ist.




