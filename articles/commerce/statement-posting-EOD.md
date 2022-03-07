---
title: Verbesserungen der Auszugsbuchungsfunktionalität
description: In diesem Thema wird beschrieben, welche Verbesserungen der Auszugsbuchungsfunktion vorgenommen wurden.
author: josaw1
ms.date: 05/14/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: retail
ms.author: anpurush
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 7e9f41a65ca092606e79d5aaa4e3af0ec444604f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795308"
---
# <a name="improvements-to-statement-posting-functionality"></a>Verbesserungen der Auszugsbuchungsfunktionalität

[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, welche Verbesserungen der Auszugsbuchungsfunktion vorgenommen wurden. Verbesserungen Diese sind in Microsoft Dynamics 365 for Finance and Operations 7.3.2 verfügbar.

## <a name="activation"></a>Aktivierung

Standardmäßig ist das Programm bei der Bereitstellung von Finance and Operations 7.3.2 so eingestellt, dass es die Legacy-Funktion für Kontoauszugsbuchungen verwendet. Um die verbesserte Auszugsbuchung zu aktivieren, müssen Sie den Konfigurationsschlüssel dafür einschalten.

- Gehen Sie zu **Systemverwaltung** \> **Einrichtung** \> **Lizenzkonfiguration**, und deaktivieren Sie dann unter dem Knoten **Retail and Commerce** das Kontrollkästchen **Auszüge (Veraltet)**, und markieren Sie das Kontrollkästchen **Auszüge**.

Wenn die neue Konfigurationsschaltfläche **Auszüge** eingeschaltet ist, steht ein neuer Menüpunkt mit dem Namen **Auszüge** zur Verfügung. Mit diesem Menüeintrag können Sie Auszüge manuell erstellen, berechnen und buchen. Jede Auszug, der bei der Verwendung des Stapelbuchungsprozesses einen Fehler verursacht, ist ebenfalls über diesen Menüeintrag verfügbar. (Wenn der Konfigurationsschlüssel **Auszüge (Legacy)** eingeschaltet ist, wird der Menüpunkt **Anweisungen öffnen** genannt).

Der Handel umfasst die folgenden Validierungen, die sich auf diese Konfigurationsschlüssel beziehen:

- Beide Konfigurationsschlüssel können nicht gleichzeitig eingeschaltet werden.
- Für alle Operationen, die während des Lebenszyklus einer Anweisung durchgeführt werden (Anlegen, Berechnen, Löschen, Buchen usw.), müssen dieselben Konfigurationsschlüssel verwendet werden. Sie können z.B. keine Aussage erstellen und berechnen, während der Konfigurationsschlüssel **Auszüge (Veraltet)** eingeschaltet ist, und dann versuchen, dieselbe Aussage zu buchen, während der Konfigurationsschlüssel **Auszüge** eingeschaltet ist.

> [!NOTE]
> Wir empfehlen Ihnen, den Konfigurationsschlüssel **Auszüge** für die verbesserte Funktion zur Buchung von Kontoauszügen zu verwenden, es sei denn, Sie haben triftige Gründe, stattdessen den Konfigurationsschlüssel **Auszüge (Veraltet)** zu verwenden. Microsoft wird weiterhin in die neue und verbesserte Funktion zur Kontoauszugsbuchung investieren, und es ist wichtig, dass Sie so schnell wie möglich darauf umsteigen, um davon zu profitieren. Die Funktion zur Verbuchung von Vorversion-Auszügen ist ab Version 8.0 veraltet.

## <a name="setup"></a>Setup

Als Teil der Verbesserungen der Kontoauszugsbuchungsfunktion wurden drei neue Parameter auf der Seite **Auszug** auf der Registerkarte **Buchung** der Seite **Commerce-Parameter** eingeführt:

- **Klare Aufstellung deaktivieren** – Diese Option ist nur für die Vorversions-Auszugsbuchungsfunktion anwendbar. Wir empfehlen, diese Option auf **Nein** zu setzen, um zu verhindern, dass Benutzer Clearing-Anweisungen, die sich in einem halbgebuchten Zustand befinden, löschen. Wenn Anweisungen, die sich in einem halbgebuchten Zustand befinden, gelöscht werden, werden die Daten beschädigt. Sie sollten diese Option nur in Ausnahmefällen auf **Ja** setzen.
- **Bestand bei der Berechnung reservieren** – Es empfiehlt sich, dass Sie den **Lager buchen**-Stapelverarbeitungsauftrag für die Lagerreservierung verwenden und Sie die Option auf **Nein** setzen. Wenn diese Option auf **Nein** gesetzt ist, versucht die verbesserte Auszugsbuchungsfunktion nicht, Bestandsreservierungseinträge zum Zeitpunkt der Berechnung zu erstellen (wenn die Einträge nicht bereits über den Batch-Job **Bestandsbuchung** erstellt wurden). Stattdessen erzeugt die Funktion Bestandsreservierungseinträge nur zum Zeitpunkt der Buchung. Diese Implementierung war eine Designwahl und basierte auf der Tatsache, dass das Zeitfenster zwischen dem Berechnungsvorgang und dem Buchungsvorgang typischerweise klein ist. Wenn Sie jedoch den Bestand zum Zeitpunkt der Berechnung reservieren möchten, können Sie diese Option auf **Ja** setzen.

    Die Funktion zur Verbuchung von Vorversion-Auszügen reserviert den Bestand immer während der Auszugsberechnung (wenn die Reservierung nicht bereits über den Batch-Job **Lager buchen** durchgeführt wurde), unabhängig von der Einstellung dieser Option.

- **Deaktivierung der Zählung erforderlich** - Wenn diese Option auf **Ja** gesetzt ist, wird der Buchungsvorgang für einen Auszug fortgesetzt, auch wenn die Differenz zwischen dem gezählten Betrag und dem Transaktionsbetrag auf dem Auszug außerhalb des Schwellenwerts liegt, der auf der Seite **Auszug** für Filialen definiert ist.

Zusätzlich wurden die folgenden Parameter auf der Seite **Batch-Verarbeitung** auf der Registerkarte **Buchung** der Seite **Commerce-Parameter** eingeführt: 

- **Maximale Anzahl von parallelen Auszugsbuchungen** – Dieses Feld definiert die Anzahl der Stapelverarbeitungsaufgaben, die verwendet werden, um mehrere Aufstellungen zu buchen. 
- **Maximaler Thread für die Auftragsverarbeitung pro Abrechnung** – Dieses Feld stellt die maximale Anzahl der Threads dar, die vom Batchauftrag für die Abrechnungsbuchung verwendet wird, um Aufträge für eine einzelne Abrechnung zu erstellen und zu fakturieren. Die Gesamtanzahl der Threads, die vom Abrechnungsbuchungsprozess verwendet werden, wird auf Grundlage des Werts in diesem Parameter multipliziert mit dem Wert im Parameter **Maximale Anzahl von parallelen Abrechnungsbuchungen** berechnet. Wird der Wert dieses Parameters zu hoch festgelegt, kann dies die Leistung des Abrechnungsbuchungsprozesses negativ beeinflussen.
- **Maximale Buchungspositionen in der Aggregierung** – Dieses Feld definiert die Anzahl von Transaktionspositionen, die in einer einzelnen zusammengefassten Transaktion eingeschlossen sind, bevor eine neue erstellt wird. Aggregierte Transaktionen werden auf Grundlage unterschiedlicher Aggregationskriterien erstellt, beispielsweise Debitor, Geschäftsdatum oder Finanzdimensionen. Es ist wichtig zu beachten, dass die Zeilen einer einzelnen Transaktion nicht auf verschiedene aggregierte Transaktionen aufgeteilt werden. Das bedeutet, dass es eine Möglichkeit gibt, dass die Anzahl der Positionen in eine zusammengefassten Transaktion etwas höher oder nidriger liegt, je nach solchen Faktoren wie Anzahl der eindeutig identifizierbare Produkte.
- **Maximale Anzahl von Threads zur Validierung von Speichertransaktionen** - Dieses Feld definiert die Anzahl der Threads, die zur Validierung von Transaktionen verwendet werden. Die Validierung von Transaktionen ist ein erforderlicher Schritt, der durchgeführt werden muss, bevor die Transaktionen in die Anweisungen gezogen werden können. Sie müssen auch ein **Geschenkkartenprodukt** auf der Seite **Geschenkkarte** auf der Registerkarte **Buchung** der Seite **Commerce-Parameter** definieren. Dies muss auch definiert werden, wen Geschenkkarten nicht von der Organisation verwendet werden.

> [!NOTE]
> Alle Einstellungen und Parameter, die sich auf Auszugsbuchungen beziehen und die in den Geschäften und auf der Seite **Commerce-Parameter** definiert sind, sind auf die verbesserte Funktion zur Auszugsbuchung anwendbar.

## <a name="processing"></a>Bearbeitung

Auszüge können über die Menüpunkte **Auszüge im Stapel berechnen** und **Auszüge im Stapel buchen** berechnet und gebucht werden. Alternativ können Auszüge manuell berechnet und gebucht werden, indem Sie den Menüpunkt **Auszüge** verwenden, den die verbesserte Funktion zur Auszugsbuchung bietet.

Der Ablauf und die Schritte für die Berechnung und Buchung von Auszügen in einem Stapel sind derselbe wie in der Funktion zum Buchen von Altauszügen. Allerdings wurden wesentliche Verbesserungen in der Kern-Backend-Verarbeitung der Auszüge vorgenommen. Diese Verbesserungen machen den Prozess widerstandsfähiger und sorgen für eine bessere Einsicht in die Zustände und Fehlerinformationen. So kann der Benutzer die Fehlerursache beheben und den Buchungsprozess fortsetzen, ohne dass es zu Datenbeschädigungen kommt und ohne dass Datenkorrekturen erforderlich sind.

In den folgenden Abschnitten werden einige der wichtigsten Verbesserungen für die Kontoauszugsbuchungsfunktion beschrieben, die in der Benutzeroberfläche für Kontoauszüge und gebuchte Auszüge erscheinen.

### <a name="status-details"></a>Statusdetails

In der Auszugsbuchungsroutine wurde ein neues Zustandsmodell über die Berechnungs- und Buchungsprozesse hinweg eingeführt.

Die folgende Tabelle beschreibt die verschiedenen Zustände und deren Reihenfolge bei der Berechnung.

| Statusreihenfolge | Zustand      | Beschreibung |
|-------------|------------|-------------|
| 1           | Gestartet    | Der Auszug wurde erstellt und ist bereit zur Berechnung. |
| 2           | Markiert     | Die Transaktionen, die in den Umfang des Auszugs fallen, werden anhand der Auszugsparameter identifiziert und mit der Auszugs-ID gekennzeichnet. |
| 3           | Berechnet | Die Auszugspositionen sind berechnet und angezeigt. |

Die folgende Tabelle beschreibt die verschiedenen Zustände und deren Reihenfolge während des Buchungsvorgangs.

| Statusreihenfolge | Zustand                   | Beschreibung |
|-------------|-------------------------|-------------|
| 1           | Geprüft                 | Es werden mehrere Validierungen durchgeführt, die sich auf Parameter (z.B. die Dispositionsgebühr) und auf die Auszugs- und Auszugspositionen (z.B. die Differenz zwischen dem gezählten Betrag und dem Transaktionsbetrag) beziehen. |
| 2           | Zusammengeführt              | Verkaufstransaktionen für benannte und unbenannte Kunden werden anhand der Konfiguration aggregiert. Jede aggregierte Transaktion wird schließlich in einen Auftrag umgesetzt. |
| 3           | Debitorenauftrag erstellt  | Abhängig von der aggretierten Transaktion werden Aufträge im System erstellt. |
| 4           | Debitorenauftrag fakturiert | Aufträge sind fakturiert. |
| 5           | Rabatte gebucht        | Abhängig von der Konfiguration werden periodische Rabatterfassungen gebucht. |
| 6           | Erträge/Aufwendungen gebucht   | Erträge/Aufwendungen werden als Belege gebucht. |
| 7           | Belege verknüpft         | Zahlungsjournale werden erstellt und mit der entsprechenden Rechnung verknüpft. |
| 8           | Zahlungen gebucht         | Zahlungsjournale werden gebucht. |
| 9           | Geschenkkarten gebucht       | Geschenkkartentransaktionen werden als Gutscheine gebucht. |
| 10          | Veröffentlicht                  | Der Auszug wird als gebucht gekennzeichnet. |

Jeder Zustand in den vorhergehenden Tabellen ist unabhängig und es wird eine hierarchische Abhängigkeit zwischen den Statusarten aufgebaut. Diese Abhängigkeit fließt von oben nach unten. Wenn das System während der Verarbeitung eines Zustands auf Fehler stößt, wird der Status des Auszugs auf den vorherigen Zustand zurückgesetzt. Jeder nachfolgende Wiederholungsversuch des Prozesses setzt sich aus dem gescheiterten Zustand fort und geht weiter. Dieser Ansatz hat folgende Vorteile:

- Der Benutzer hat vollständige Einsicht in den Zustand, in dem der Fehler aufgetreten ist.
- Datenkorruption wird vermieden. So gab es z. B. bei der Verbuchung von Legacy-Auszügen Situationen, in denen einige Debitorenaufträge fakturiert, andere aber offen gelassen wurden. Es gab auch Fälle, in denen einige Zahlungsjournale keine entsprechende Rechnung zu begleichen hatten, weil die Rechnungsbuchung fehlerhaft war.
- Benutzer können den aktuellen Status eines Auszugs mit der Schaltfläche **Statusdetails** in der Gruppe **Ausführungsdetails** des Auszugs sehen. Die Status-Detailseite besteht aus drei Abschnitten:

    - Der erste Abschnitt zeigt den aktuellen Status des Auszugs zusammen mit dem Fehlercode und einer detaillierten Fehlermeldung, falls ein Fehler aufgetreten ist.
    - Der zweite Abschnitt zeigt die verschiedenen Zustände des Berechnungsprozesses. Visuelle Hinweise zeigen Zustände an, die erfolgreich ausgeführt wurden, Zustände, die aufgrund von Fehlern nicht ausgeführt werden konnten, und Zustände, die noch nicht ausgeführt wurden.
    - Der dritte Abschnitt zeigt die verschiedenen Zustände des Buchungsprozesses. Visuelle Hinweise zeigen Zustände an, die erfolgreich ausgeführt wurden, Zustände, die aufgrund von Fehlern nicht ausgeführt werden konnten, und Zustände, die noch nicht ausgeführt wurden.

Zusätzlich zeigt die Kopfzeile des zweiten und dritten Abschnitts den Gesamtstatus des jeweiligen Prozesses an.

### <a name="event-logs"></a>Ereignisprotokolle

Ein Auszug durchläuft mehrere Operationen (z.B. Anlegen, Berechnen, Löschen und Buchen), wobei mehrere Instanzen desselben Vorgangs während des Lebenszyklus des Auszugs aufgerufen werden können. Beispielsweise kann ein Benutzer nach der Erstellung und Berechnung eines Auszugs den Auszug löschen und neu berechnen. Die Schaltfläche **Ereignisprotokolle** in der Gruppe **Ausführungsdetails** der Anweisung bietet einen vollständigen Audit-Trail der verschiedenen Operationen, die auf einer Anweisung aufgerufen wurden, zusammen mit Informationen darüber, wann diese Operationen aufgerufen wurden.

### <a name="aggregated-transactions"></a>Zusammengeführte Transaktionen

Während des Buchungsvorgangs werden die Verkaufsbuchungen gemäß den Einstellungen zusammengefasst. Diese aggregierten Transaktionen werden im System gespeichert und zum Anlegen von Debitorenaufträgen verwendet. Jede aggregierte Transaktion erzeugt einen entsprechenden Debitorenauftrag im System. Sie können die aggregierten Transaktionen über die Schaltfläche **Zusammengeführte Transaktionen** in der Gruppe **Ausführungsdetails** des Auszugs anzeigen.

Die Registerkarte **Debitorenauftragsdetail** einer aggregierten Transaktion zeigt die folgenden Informationen an:

- **Datensatz-ID** - Die ID der aggregierten Transaktion.
- **Auszugsnumber** - Der Auszug, zu dem die aggregierte Transaktion gehört.
- **Datum** - Das Datum, an dem die aggregierte Transaktion angelegt wurde.
- **Verkaufskennung** - Beim Anlegen eines Debitorenauftrags aus der aggregierten Transaktion wird die Debitorenauftrags-ID angezeigt. Wenn dieses Feld leer ist, wurde der entsprechende Debitorenauftrag nicht angelegt.
- **Anzahl aggregierter Positionen** - Gesamtzahl der Zeilen für den aggregierten Vorgang und Debitorenauftrag.
- **Status** - Der letzte Status der aggregierten Transaktion.
- **Rechnungskennung** - Wenn der Debitorenauftrag für den aggregierten Vorgang fakturiert wird, wird die Verkaufsrechnungs-ID angezeigt. Wenn dieses Feld leer ist, wurde die Rechnung für den Debitorenauftrag nicht gebucht.

Das Register **Transaktionsdetails** einer aggregierten Transaktion zeigt alle Transaktionen, die in die aggregierte Transaktion gezogen wurden. Die aggregierten Zeilen der aggregierten Transaktion zeigen alle aggregierten Datensätze aus den Transaktionen an. Die aggregierten Positionen zeigen auch Details wie Artikel, Variante, Menge, Preis, Nettobetrag, Einheit und Lager. Grundsätzlich entspricht jede aggregierte Zeile einer Auftragszeile.

Von der Seite **Aggregierte Transaktionen** können Sie das XML für eine bestimmte aggregierte Transaktion über die Schaltfläche **Auftrags-XML exportieren** herunterladen. Sie können das XML verwenden, um Probleme zu debuggen, die das Anlegen und Buchen von Aufträgen betreffen. Laden Sie einfach das XML herunter, laden Sie es in eine Testumgebung hoch und debuggen Sie das Problem in der Testumgebung. Die Funktionalität zum Herunterladen des XML für aggregierte Transaktionen steht für gebuchte Auszüge nicht zur Verfügung.

Die aggregierte Transaktionssicht bietet folgende Vorteile:

- Der Benutzer hat Einblick in die aggregierten Transaktionen, die bei der Debitorenauftragserstellung fehlgeschlagen sind, und die Debitorenaufträge, die bei der Fakturierung fehlgeschlagen sind.
- Der Benutzer hat Transparenz darüber, wie Transaktionen aggregiert werden.
- Der Benutzer verfügt über einen vollständigen Prüfpfad, von Transaktionen über Kundenaufträge bis hin zu Verkaufsrechnungen. Diese Historie war in der Funktion zum Buchen von Legacy-Auszügen nicht verfügbar.
- Eine aggregierte XML-Datei erleichtert die Identifizierung von Problemen bei der Auftragserstellung und Fakturierung.

### <a name="journal-vouchers"></a>Erfassungsbelege

Die Schaltfläche **Erfassungsbelege** in der Gruppe **Ausführungsdetails** des Auszugs zeigt alle verschiedenen Belegtransaktionen, die für einen Auszug erstellt werden und die sich auf Rabatte, Einnahmen-/Ausgabenkonten, Geschenkkarten usw. beziehen.

Derzeit zeigt das Programm diese Daten nur für gebuchte Auszüge an.

### <a name="payment-journals"></a>Zahlungserfassungen

Die Schaltfläche **Zahlungserfassungen** in der Gruppe **Ausführungsdetails** des Auszugs zeigt alle verschiedenen Zahlungsjournale, die zu einem Auszug erstellt werden.

Derzeit zeigt das Programm diese Daten nur für gebuchte Auszüge an.

## <a name="other-improvements"></a>Weitere Verbesserungen

Weitere Backend-Verbesserungen, die der Benutzer sehen kann, wurden an der Auszugsbuchung vorgenommen. Nachfolgend finden Sie einige Beispiele:

- Die Aggregation berücksichtigt nicht die Personal-, Terminal- und Schicht-Einheiten. Da es weniger Aggregationsparameter gibt, müssen weniger Auftragszeilen bearbeitet werden.
- Das Auftreten von Blockierungen in Transaktionstabellen wird durch die Einführung zusätzlicher Erweiterungstabellen und durch Einfügeoperationen anstelle von Aktualisierungsoperationen in den Transaktionstabellen reduziert.
- Die Anzahl der laufenden Stapelaufgaben wurde parametrisiert und begrenzt. Daher kann diese Zahl speziell auf die Umgebung des Kunden abgestimmt werden. In der Funktion zum Buchen von Legacy-Auszügen wurde eine unbegrenzte Anzahl von Stapelaufgaben gleichzeitig angelegt. Die Folge waren unüberschaubare Lasten, Overhead und Engpässe auf dem Batch-Server.
- Anweisungen werden effizient zur Verarbeitung in die Warteschlange gestellt, indem die Anweisungen mit der maximalen Anzahl von Transaktionen priorisiert werden.
- Stapelprozesse wie z. B. **Aufstellungen in Charge berechnen** und **Aufstellungen in Charge buchen** werden nur im Stapelbetrieb ausgeführt. In der Funktion zum Buchen von Legacy-Auszügen können Benutzer diese Stapelprozesse in einem interaktiven Modus ausführen, der im Gegensatz zu Stapelprozessen mit mehreren Threads nur ein Thread ist.
- In der Funktion zum Buchen von Legacy-Auszügen führt jeder Ausfall einer Stapelaufgabe dazu, dass der gesamte Stapeljob in einen Fehlerzustand versetzt wird. In der verbesserten Funktion wird der Stapelauftrag nicht in einen Fehlerzustand versetzt, wenn andere Stapelaufträge erfolgreich abgeschlossen werden. Sie sollten den Buchungsstatus für einen Batch-Ausführungslauf beurteilen, indem Sie die Seite **Auszüge** verwenden, auf der Sie alle Auszüge sehen können, die aufgrund von Fehlern nicht gebucht wurden.
- In der Funktion zum Buchen von Legacy-Auszügen führt das erste Auftreten eines Auszugsfehlers zum Ausfall des gesamten Stapels. Die restlichen Auszüge werden nicht verarbeitet. In der verbesserten Funktion verarbeitet der Stapelprozess weiterhin alle Auszüge, auch wenn einige der Auszüge fehlschlagen. Ein Vorteil ist, dass der Anwender die genaue Anzahl der fehlerhaften Auszüge einsehen kann. Daher müssen die Benutzer nicht in einer kontinuierlichen Schleife der Fehlerbehebung und des Buchungsanweisungsprozesses stecken bleiben, bis alle Auszüge gebucht sind.

## <a name="general-guidance-about-the-statement-posting-process"></a>Allgemeine Hinweise zum Ablauf der Auszugsbuchung

- Wir empfehlen, den Prozess der Auszugsbuchung im Stapel laufen zu lassen, da Batchläufe die Vorteile des Batch-Frameworks im Sinne von Multithreading nutzen. Multithreading ist erforderlich, um die großen Transaktionsvolumina zu bewältigen, die normalerweise bei Auszugsbuchungen anfallen.
- Wir empfehlen Ihnen, die negative Inventur auf der Artikelmodellgruppe einzuschalten, um eine reibungslose Buchung zu ermöglichen. In einigen Szenarien können negative Auszüge nur dann gebucht werden, wenn eine negative Inventur vorliegt. Wenn sich beispielsweise theoretisch nur eine Einheit eines Artikels im Bestand befindet und ein Verkaufsvorgang und ein Rückgabevorgang für den Artikel stattgefunden haben, sollte der Vorgang auch dann gebucht werden können, wenn der negative Bestand nicht aktiviert ist. Da der Prozess der Auszugsbuchung jedoch sowohl den Verkaufsvorgang als auch den Retourenvorgang in einem einzigen Auftrag zieht, gibt es keine Garantie dafür, dass die Verkaufsposition zuerst gebucht wird, gefolgt von der Retourenposition. Daher können Fehler auftreten. Wenn in diesem Szenario der negative Bestand eingeschaltet ist, wird die Transaktionsbuchung nicht negativ beeinflusst, und das System spiegelt den Bestand korrekt wider.
- Wir empfehlen, bei der Berechnung und Buchung von Auszügen die Aggregation zu verwenden. Daher werden für einige der Aggregationsparameter die folgenden Einstellungen empfohlen:

    - Gehen Sie zu **Retail and Commerce** \> **Heaquaters einrichten** \> **Parameter** \> **Commerce-Parameter**. Stellen Sie anschließend auf der Registerkarte **Buchung**, auf dem Inforegister **Lageraktualisierung**, auf dem Feld **Detailebene**, wählen Sie **Zusammenfassung** aus.
    - Gehen Sie zu **Retail and Commerce** \> **Heaquaters einrichten** \> **Parameter** \> **Commerce-Parameter**. Stellen Sie anschließend auf der Registerkarte **Buchung**, auf dem Inforegister **Aggregation**, Satz **Belegbuchungen** die Option **Ja**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]