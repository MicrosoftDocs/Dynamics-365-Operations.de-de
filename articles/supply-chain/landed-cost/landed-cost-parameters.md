---
title: Einrichten der Gesamttransportkosten-Parameter
description: Hier wird beschrieben, wie Sie allgemeine Informationen und Konfigurationseinstellungen festlegen, die im gesamten Modul für kalkulierte Transportkosten für Buchungen, Statusaktualisierungen, Sequenzen und Verhalten verwendet werden.
author: sherry-zheng
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 973f23a18166abeb05bdea660ef69230d9a8c4c0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833904"
---
# <a name="landed-cost-parameters-setup"></a>Einrichten der Gesamttransportkosten-Parameter

[!include [banner](../../includes/banner.md)]

Sie verwenden die Seite **Gesamttransportkosten-Parameter**, um allgemeine Informationen und Konfigurationseinstellungen festzulegen, die im gesamten Modul **Gesamttransportkosten** für Buchungen, Statusaktualisierungen, Nummernkreise und Verhalten verwendet werden. Das Einrichten der Parameter wird von allen juristischen Entitäten gemeinsam genutzt und kann von einem Administrator geändert werden.

## <a name="open-the-landed-cost-parameters-page"></a>Öffnen Sie die Seite Gesamttransportkosten-Parameter

Um mit den Parametern zu arbeiten, gehen Sie zu **Gesamttransportkosten \> Einrichtung \> Gesamttransportkosten-Parameter** und legen dann die Felder fest, wie in den folgenden Unterabschnitten beschrieben.

![Gesamttransportkosten-Parameter Seite](media/landed-cost-parameters.png "Seite Gesamttransportkosten-Parameter")

## <a name="general-tab"></a>Registerkarte „Allgemeines“

### <a name="general-fasttab"></a>Allgemeines Inforegister

Die folgende Tabelle beschreibt die Felder, die auf dem Inforegister **Allgemein** der Registerkarte **Allgemein** der Seite **Gesamttransportkosten-Parameter** verfügbar sind.

| Einstellung | Beschreibung |
|---|---|
| Versandrate verwenden | Ein Versandsatz wird für einen definierten Zeitraum festgelegt und dient zur Kalkulation von Waren, die mehrere Währungen verwenden. Legen Sie diese Option auf *Ja* fest, um einen Versandsatz zu verwenden. |
| Wechselkurstyp | Die Standard-Sammlung von Wechselkursen, die für Berechnungen mit mehreren Währungen für eine Fahrt und die Kosten einer Fahrt verwendet wird. |
| Bestellmenge aktualisieren | Wählen Sie aus, was passiert, wenn ein Benutzer die Menge in einer Zeile einer Einkaufsbestellung ändert:<ul><li>**Akzeptieren** - Die Menge für die Fahrt wird automatisch angepasst.</li><li>**Warnung** - Wenn die Zeile an eine Fahrt angehängt ist, wird eine Warnung angezeigt, aber die Fahrtmenge wird aktualisiert.</li><li>**Fehler** - Wenn die Zeile an eine Fahrt angehängt ist, wird eine Fehlermeldung angezeigt, und die Einkaufsbestellung kann nicht aktualisiert werden. Daher muss die Bestellzeile zuerst von der Fahrt entfernt werden.</li></ul> |
| Anzahl der Kartons automatisch aktualisieren | Wenn diese Option auf *Ja* festgelegt ist, werden alle Kartons addiert und auf Fahrt- und Containerebene angezeigt. Wenn sie auf *Nein* festgelegt ist, wird die Anzahl der Kartons zunächst auf 0 (Null) festgelegt und kann bei Bedarf manuell bearbeitet werden. |

### <a name="costing-fasttab"></a>Kalkulation Inforegister

Die folgende Tabelle beschreibt die Felder, die auf dem Inforegister **Kalkulation** der Registerkarte **Allgemein** der Seite **Gesamttransportkosten-Parameter** verfügbar sind.

| Einstellung | Beschreibung |
|---|---|
| Buchungsspezifikation | Wählen Sie die Wertberichtigung im Hauptbuch aus:<ul><li>**Summe** - Es wird eine Gesamtsumme in das Hauptbuch gebucht.</li><li>**Postengruppe** - Die Anpassung wird pro Artikelgruppe angegeben.</li><li>**Positionsnummer** - Die Anpassung wird pro Artikel angegeben. Dieser Wert liefert die meisten Details.</li></ul> |
| Nullkosten zulassen | Legen Sie diese Option auf *Nein* fest, um einen Fehler anzuzeigen, wenn ein Benutzer versucht, eine Kalkulation für eine Rechnung oder Einkaufsbestellung für eine Fahrt zu buchen, die keinen Wert für die erwarteten Fahrtkosten enthält. Die Fehlermeldung besagt, dass eine Kalkulation von 0 (Null) nicht zugewiesen werden kann und die Rechnungsbuchung fehlschlägt. In diesem Fall kann der Benutzer die Schätzung manuell aktualisieren (oder die Autokalkulation neu konfigurieren) und dann entweder den aktualisierten Wert einziehen oder die Kosten löschen, wenn sie nicht zutreffen.<p>Legen Sie diese Option auf *Ja* fest, damit die Kalkulation für die Fahrt leer bleibt. In diesem Fall wird ein Preis von 0 (Null) entsprechend dem Kostenbereich zugewiesen. Eine Lieferanten-Kostenrechnung kann dann gegen die Null-Preis-Kosten verarbeitet werden, wenn die Fahrt empfangen wird.</p><p>Wir empfehlen, die Schätzung im Autokalkulations-Datensatz zu konfigurieren, um zu verhindern, dass eine Nullpreis-Kalkulation auftritt. Obwohl diese Kalkulation nicht ganz genau ist, sollte sie doch genauer sein als eine angenommene Null-Kosten Kalkulation.</p> |
| Regulierungsbuchungsdatum | Wenn Sie eine kreditorische Fahrtkostenrechnung buchen, wird auch die Abrechnungstabelle (Bestandsanpassungen) aktualisiert. Wählen Sie das Datum, das standardmäßig auf der Seite **Fahrtkosten kalkulieren** festgelegt ist, während Sie sich in der Rechnungserfassung befinden:<ul><li>**Transaktionsdatum** - Verwenden Sie das Datum der Transaktion (Buchungsdatum).</li><li>**Rechnungsdatum der Einkaufsbestellung** - Verwenden Sie das finanzielle Buchungsdatum der Rechnung des Lagers (Einkaufsbestellung).</li><li>**Ausgewähltes Datum** - Der Benutzer kann ein Buchungsdatum angeben. Obwohl das Datum leer gelassen werden kann, erhält der Benutzer eine Fehlermeldung, wenn es beim Buchen der Kostenrechnung noch leer ist.</li></ul> |
| Einkaufsrechnungsbeleg verwenden | Wenn diese Option auf *Ja* festgelegt ist, verwenden Transaktionen zur Kostenabgrenzung die gleiche Belegnummer, die auch für die Kaufrechnung verwendet wird. Wenn sie auf *Nein* festgelegt ist, verwendet das System die nächste verfügbare Nummer für die **Kostenabgrenzungsbeleg** Nummernfolge, die auf der Registerkarte **Nummernfolgen** der Seite **Gesamttransportkosten-Parameter** festgelegt ist.<p>Diese Option wirkt sich nur aus, wenn die Option **Buchen auf Kostenkonto im Hauptbuch** auf der Registerkarte **Rechnung** der Seite **Kostenabgrenzungsparameter** auf *Ja* festgelegt ist.</p> |
| Manuelle Buchung auf Clearingkonto sperren | Legen Sie diese Option auf *Ja* fest, um die Buchung auf Verrechnungskonten zu verhindern, bei denen die Transaktion nicht mit einer Fahrt verknüpft wurde, indem Sie **Funktionen \> Fahrtkosten kalkulieren** im Aktivitätsbereich der Kreditoren-Rechnungserfassung wählen. Wir empfehlen, diese Option auf *Ja* festzulegen, damit die Fahrt und das Verrechnungskonto korrekt abgerechnet werden können. |
| Kostentyp-Belastungsabgrenzungskonto verwenden | Wenn diese Option auf *Ja* festgelegt ist, wird das Kostenabgrenzungskonto, das für den entsprechenden Kostenartencode auf der Seite **Kostenartencodes** konfiguriert ist, für die Abgrenzung der Kosten als Aufwand verwendet.<p>Diese Option wirkt sich nur aus, wenn die Option **Buchen auf Kostenkonto im Hauptbuch** auf der Registerkarte **Rechnung** der Seite **Kostenabgrenzungsparameter** auf *Ja* festgelegt ist. |
| Regulierungen als Abweichung buchen | Wenn diese Option auf *Ja* festgelegt ist, setzt sie die Standardfunktionalität außer Kraft und erzwingt, dass die Transaktionen zur Bestandsanpassung, die sich auf Abweichungen zwischen geschätzten Kosten und tatsächlichen Kosten beziehen, auf ein Abweichungskonto gebucht werden.<p>Wenn diese Option auf *Nein* festgelegt ist, werden die Bestandskorrektur-Transaktionen, die sich auf Abweichungen beziehen, basierend auf der Konfiguration der Kalkulationsmethode und des Kostenartencodes behandelt. Für die Standardkalkulation werden Abweichungen weiterhin auf das Abweichungskonto gebucht. Bei gleitendem gewichteten Durchschnitt (WMA) werden die Abweichungen entweder auf das Abweichungskonto oder auf den Bestand gebucht.</p><p>Diese Option wirkt sich nur aus, wenn die Option **Buchen auf Kostenkonto im Hauptbuch** auf der Registerkarte **Rechnung** der Seite **Kostenabgrenzungsparameter** auf *Ja* festgelegt ist.</p> |

### <a name="validation-fasttab"></a>Validierung Inforegister

Die folgende Tabelle beschreibt die Felder, die auf dem Inforegister **Validierung** der Registerkarte **Allgemein** der Seite **Gesamttransportkosten-Parameter** verfügbar sind.

| Einstellung | Beschreibung |
|---|---|
| Mehrere Kostenrechnungen | Wählen Sie aus, was geschehen soll, wenn mehr als eine Rechnung für eine Fahrt, Palette oder einen Container für dieselbe sonstige Gebühr verarbeitet wird.<ul><li>**Akzeptieren** - Das System sollte mehrere Kalkulationen zulassen.</li><li>**Warnung** - Es wird eine Warnung angezeigt.</li><li>**Fehler** - Es wird eine Fehlermeldung angezeigt.</li></ul> |
| Mehrere Kreditoren pro Folio | Wählen Sie aus, was passieren soll, wenn einer Palette mehr als eine Einkaufsbestellung eines Lieferanten hinzugefügt wird.<ul><li>**Akzeptieren** - Das System soll die Aktion zulassen.</li><li>**Warnung** - Es wird eine Warnung angezeigt, aber die Aktion kann trotzdem ausgeführt werden.</li><li>**Fehler** - Es wird eine Fehlermeldung angezeigt, und die Aktion wird verhindert.</li></ul><p>Ihr Zoll Broker oder lokale Gesetze können einen bestimmten Wert für dieses Feld vorschreiben.</p> |
| Toleranz für mehrere Lieferarten | Wählen Sie aus, was passiert, wenn Waren aus einer Einkaufsbestellung, die eine andere Lieferart als die Fahrt verwendet, zu dieser Fahrt hinzugefügt werden.<ul><li>**Akzeptieren** - Das System soll die Aktion zulassen.</li><li>**Warnung** - Es wird eine Warnung angezeigt, aber die Aktion kann trotzdem ausgeführt werden.</li><li>**Fehler** - Es wird eine Fehlermeldung angezeigt, und die Aktion wird verhindert.</li></ul> |
| Toleranz für mehrere Lagerorte | Wählen Sie aus, was geschieht, wenn eine Fahrt mehrere Bestellzeilen enthält, die an verschiedene Lagerorte geliefert werden müssen. Diese Bestellzeilen können auf eine oder mehrere Einkaufsbestellungen verteilt sein.<ul><li>**Akzeptieren** - Das System soll die Aktion zulassen.</li><li>**Warnung** - Es wird eine Warnung angezeigt.</li><li>**Fehler** - Es wird eine Fehlermeldung angezeigt.</li></ul> |
| Fehlendes Volumen | Wählen Sie aus, was passiert, wenn ein Benutzer einen Artikel ohne Volumen zu einer Fahrt hinzufügt.<ul><li>**Akzeptieren** - Das System soll den Artikel akzeptieren.</li><li>**Warnung** - Es wird eine Warnung angezeigt.</li><li>**Fehler** - Es wird eine Fehlermeldung angezeigt.</li></ul><p>Wenn Volumen zur Kalkulation und Aufteilung der Kosten verwendet wird, empfehlen wir, entweder *Warnung* oder *Fehler* zu wählen.</p> |
| Dienstanbieter ohne Seereisekosten | Wählen Sie aus, was passiert, wenn ein Benutzer versucht, eine Rechnung für einen Dienstleister zu bearbeiten, der nicht mit einer Fahrt verknüpft wurde. <ul><li>**Akzeptieren** - Das System soll die Aktion zulassen.</li><li>**Warnung** - Es wird eine Warnung angezeigt.</li><li>**Fehler** - Es wird eine Fehlermeldung angezeigt.</li></ul><p>Wir empfehlen, dass Sie *Warnung* wählen.</p> |

### <a name="defaults-fasttab"></a>Voreinstellungen Inforegister

Die folgende Tabelle beschreibt die Felder, die auf dem Inforegister **Vorgaben** der Registerkarte **Allgemein** der Seite **Gesamttransportkosten-Parameter** verfügbar sind.

| Einstellung | Beschreibung |
|---|---|
| Journal | Wählen Sie das Standard-Journal, das die Funktion *Ankunftserfassung erstellen* verwenden soll. |
| Seereisestatus | Wählen Sie den Status, den eine Fahrt haben muss, bevor Benutzer einen Miet-Transportcontainer für sie im System festlegen können. Diese Aktion erfolgt normalerweise, wenn die Waren in Zustellung oder am Dock sind. |
| Reisevorlage | Wählen Sie die Standardvorlage für die Route, die für neue Miet-Transportcontainer verwendet werden soll. In der Regel werden Sie eine Routenvorlage wählen, die die Kalkulation der Mietkosten enthält. |
| Bewegung | Wenn die Über-/Untermenge für eine Lieferung innerhalb der definierten Toleranz liegt, wird automatisch ein Umlagerungserfassung verarbeitet. Wählen Sie das zu verwendende Standard-Umlagerungserfassung aus. Das Feld **Vergleichskonto** für den gewählten Namen des Umlagerungserfassungs muss einen Wert haben. |
| Übertrag | Wenn eine Unterlieferung verarbeitet wird, wird die Unterlieferungsmenge in ein Unterlieferungslagerort übertragen. Wählen Sie die standardmäßig zu verwendende Umlagerungserfassung aus. |
| Bestellungen, die keine Seereisebestellungen sind, deaktivieren | Schalten Sie die Funktion Gesamttransportkosten Über-/Unterlieferung für Einkaufsbestellungen aus, die nicht an eine Fahrt gekoppelt sind. |
| Aufträge, die keine Waren in Zustellung-Aufträge sind, deaktivieren | Schalten Sie die Gesamttransportkosten-Über-/Unterlieferungsfunktionalität für Kaufsbestellungen aus, die nicht die Funktionalität für Waren in Zustellung verwenden. |
| Waren in Zustellung – Wareneingangs-Übertoleranzperiode | Geben Sie an, wie viele Tage nach dem ersten Eingang eines Transportcontainers noch weitere Über-Eingänge für diesen Transportcontainer abgeschlossen werden können. |

## <a name="status-updates-tab"></a>Registerkarte Statusaktualisierungen

Das System verwendet Statuswerte, um den Status der einzelnen Fahrten anzuzeigen. Fahrtstatuswerte können automatisch über die Fahrtverfolgung oder periodische Batch-Jobs auf Fahrten angewendet werden. Alternativ können Sie sie manuell anwenden, indem Sie die Fahrt öffnen und dann einen Status in der Gruppe **Fahrtaktualisierung** auf der Registerkarte **Verwalten** des Aktivitätsbereichs auswählen. 

Sie können so viele Statuswerte für die Fahrt erstellen, wie Sie möchten. Vier davon müssen jedoch auf der Registerkarte **Statusaktualisierungen** der Seite **Gesamttransportkosten-Parameter** als für einen speziellen Zweck verwendet definiert werden. Die folgende Tabelle beschreibt die Felder, die dort verfügbar sind.

| Einstellung | Beschreibung |
|---|---|
| Mit Kosten | Wählen Sie den Fahrtstatus aus, der angibt, dass eine Fahrt abgeschlossen wurde. |
| Unterwegs | Wählen Sie den Fahrtstatus aus, der angibt, dass sich eine Fahrt in Zustellung befindet. |
| Bereit für die Nachkalkulation | Wählen Sie den Fahrtstatus aus, der angibt, dass eine Fahrt für die Kalkulation bereit ist. Dieser Status wird verwendet, wenn alle Rechnungen für den Kauf von Lagerbeständen und Rechnungen für die Kalkulation der Fahrt, bei denen das Feld **Gutschrift auf die Fahrtkosten** auf *Lieferant* festgelegt ist, für die Fahrt verarbeitet wurden. Fahrten, die nicht kalkuliert werden, haben den Status *Bereit zur Kalkulation*.|
| Vorkalkuliert | Wählen Sie den Status der Fahrt, der angibt, dass eine Fahrt vorkalkuliert wird. Dieser Status wird verwendet, wenn eine neue Kostentransaktion zu einer Fahrt hinzugefügt wird, nachdem sie bereits kalkuliert wurde. Neue Kostentransaktionen können zu einer bereits kalkulierten Fahrt hinzugefügt werden, wenn eine zweite Frachtrechnung oder eine unerwartete Liegegebühr eingeht. Dieser Status wird automatisch angewendet, wenn einer kalkulierten Fahrt neue Fahrtkosten hinzugefügt werden. |

## <a name="voyage-creator-tab"></a>Registerkarte Fahrt-Ersteller

Die folgende Tabelle beschreibt die Abschnitte auf der Registerkarte **Fahrtersteller** der Seite **Gesamttransportkosten Parameter**.

| Abschnitt | Beschreibung |
|---|---|
| Toleranzen | Die Felder **Außenvolumentoleranz** und **Außengewichtstoleranz** definieren Schwellenwerte, oberhalb derer Waren als zu voluminös und zu schwer angesehen werden. Wenn ein Benutzer Waren auf der Seite **Fahrt-Editor** hinzufügt, zeigt das System eine Warnung an, wenn das Volumen oder das Gewicht den hier festgelegten Wert überschreitet. Der Wert jedes Feldes wird als Prozentsatz des maximalen Volumens oder Gewichts ausgedrückt, das für den jeweiligen Transportcontainer-Typ festgelegt ist. Wir empfehlen, dass der Wert zwischen 5 und 10 Prozent des maximalen Volumens oder Gewichts liegt. |
| Einstellungen für Folioerstellung | Das System kann mehrere Paletten während der Erstellung der Fahrt erstellen. Verwenden Sie diesen Abschnitt, um festzulegen, wann eine neue Palette erstellt werden soll. Für jede Zeile in diesem Abschnitt prüft das System die angegebene Tabelle und das angegebene Feld und erstellt ein Palette für jeden eindeutigen Feldwert. |

## <a name="cost-estimates-tab"></a>Registerkarte Kalkulationen

Die Registerkarte **Kostenschätzungen** der Seite **Gesamttransportkosten-Parameter** enthält nur ein Feld: **Standardversion der Kalkulation**. Dieses Feld gilt nur, wenn die Kalkulationsmethode *Standardkalkulation* ist. Wählen Sie die Standardkalkulationsversion, die für die periodische Aufgabe *Kostenpreisaktualisierung des Artikels* verwendet werden soll. Möglicherweise müssen Sie diese Einstellung jedes Mal ändern, wenn ein neues Geschäftsjahr beginnt.

## <a name="inventory-dimensions-tab"></a>Registerkarte Bestandsdimensionen

Über die Registerkarte **Bestandsdimensionen** der Seite **Gesamttransportkosten-Parameter** steuern Sie, welche verfügbaren Bestandsdimensionen standardmäßig auf jeder Seite der Gesamttransportkosten angezeigt werden sollen, auf der Dimensionen verwendet werden.

Wählen Sie eine Dimension aus und legen Sie dann die Option **Fahrtrouten**, **Waren in Zustellung** und/oder **Kalkulationen** auf *Ja* für jede Seite fest, auf der diese Dimension standardmäßig angezeigt werden soll. Wiederholen Sie diesen Schritt für andere Dimensionen, je nach Bedarf.

Die Einstellungen auf dieser Registerkarte legen die Standarddimensionen für jede bezeichnete Seite über juristische Entitäten hinweg fest. Benutzer, die auf einer der benannten Seiten arbeiten, können jedoch die Standarddimensionen außer Kraft setzen, indem sie **Bestand \> Dimensionen anzeigen** im Aktivitätsbereich wählen.

## <a name="number-sequences-tab"></a>Registerkarte Nummernkreise

Die Registerkarte **Nummernfolgen** der Seite **Gesamttransportkosten-Parameter** listet alle Arten von Nummernkreisen auf, die für die Gesamttransportkosten erforderlich sind, die aber nicht für alle juristischen Entitäten gelten. Wählen Sie für jede Referenz in der Liste einen Code für die Nummernkreis-Sequenz.

> [!NOTE]
> In einer Konfiguration mit mehreren Firmen müssen für jede Firma (juristische Entität) unterschiedliche Sequenzen erstellt werden.

## <a name="shared-number-sequences-tab"></a>Registerkarte Gemeinsam genutzte Nummernkreise

Die Registerkarte **Gemeinsame Nummernkreise** der Seite **Gesamttransportkosten-Parameter** listet alle Arten von Referenznummernkreisen auf, die von juristischen Entitäten für Gesamttransportkosten gemeinsam genutzt werden. Derzeit gibt es nur eine Nummernkreis-Sequenz in der Liste. Diese Nummernkreis-Sequenz wird für die Fahrt-ID verwendet.

Auf der Seite **Alle Fahrten** können Benutzer alle Fahrten über alle juristischen Entitäten hinweg einsehen. Um eine Fahrt zu bearbeiten, müssen sich die Benutzer jedoch in der juristischen Entität des ausgewählten Datensatzes befinden.

## <a name="feature-visibility-tab"></a>Registerkarte Sichtbarkeit der Funktionen

Gesamttransportkosten fügt Funktionen (Felder und Funktionen) zu mehreren häufig verwendeten Seiten in Microsoft Dynamics 365 Supply Chain Management hinzu. Zu diesen Seiten gehören Seiten, die sich auf Lieferantenstammdaten, freigegebene Produkte, Kaufsbestellungen, Transportaufträge und die Einrichtung von Lagerorten beziehen. Wenn Sie Gesamttransportkosten verwenden, müssen Sie diese Funktionen überall sichtbar machen, bevor Sie sie nutzen können. Wenn Sie die Gesamttransportkosten nicht kalkuliert haben, können Sie die Funktionen ausblenden, um sie aus dem Weg zu räumen.

Legen Sie auf der Registerkarte **Sichtbarkeit der Funktionen** der Seite **Parameter für kalkulierte Kosten** die Option **Aktivieren** auf *Ja* fest, um Funktionen für kalkulierte Kosten überall sichtbar zu machen, wo sie verfügbar sind. Legen Sie sie auf *Nein* fest, um die Funktionen auf allgemeinen Seiten außerhalb der Gesamttransportkosten auszublenden. Aber auch wenn die Option auf *Nein* festgelegt ist, bleibt das Modul selbst, einschließlich der Seite **Gesamttransportkosten-Parameter**, für Benutzer verfügbar, die die richtigen Berechtigungen für den Zugriff darauf haben.
