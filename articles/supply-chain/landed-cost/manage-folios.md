---
title: Paletten verwalten
description: Dieses Thema beschreibt, wie Sie mit Paletten arbeiten. Eine Palette besteht normalerweise aus den Waren eines Lieferanten für eine Entität oder Firma pro Sendung. Die Waren in einer Palette können sich in einem Container befinden, oder sie können auf mehrere Container verteilt sein.
author: Weijiesa
ms.date: 12/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMFolioTable, ITMFolioTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: f908ae3c150a09af61bb0ee97469619744cd1079
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8695301"
---
# <a name="manage-folios"></a>Paletten verwalten

[!include [banner](../../includes/banner.md)]

Eine Palette wird oft durch Zollbestimmungen bestimmt. Es kann aus den Waren eines Lieferanten für eine Entität oder Firma pro Sendung bestehen. Die Waren einer Palette werden in einem Container verwaltet.

Um die Seite **Alle Paletten** zu öffnen, gehen Sie auf **Gesamttransportkosten \> Paletten \> Alle Paletten**. Diese Seite zeigt eine Liste aller aktuellen Paletten. Sie können die Schaltflächen im Aktivitätsbereich verwenden, um Paletten zu erstellen, zu löschen und mit ihnen zu arbeiten. Wählen Sie ein beliebiges Palette in der Liste aus, um seine Details auf der Seite **Paletten** anzuzeigen.

## <a name="action-pane"></a>Aktivitätsbereich

Der Aktivitätsbereich auf den Seiten **Alle Paletten** und **Paletten** bietet Schaltflächen, mit denen Sie mit einem ausgewählten Palette arbeiten können. Jede Schaltfläche führt eine einzelne Aktion aus. Der Aktivitätsbereich enthält auch Registerkarten, von denen jede wiederum eine Reihe von zugehörigen Schaltflächen bereitstellt. Wenn nicht anders angegeben, sind alle Schaltflächen und Registerkarten, die in den folgenden Unterabschnitten beschrieben werden, sowohl in der Listenansicht (d. h. auf der Seite **Alle Paletten**) als auch in der Detailansicht (d. h. auf der Seite **Paletten**) verfügbar.

### <a name="buttons-that-appear-directly-on-the-action-pane"></a>Schaltflächen, die direkt im Aktivitätsbereich erscheinen

Die folgende Tabelle beschreibt die Schaltflächen, die direkt im Aktivitätsbereich verfügbar sind.

| Schaltfläche | Beschreibung |
|---|---|
| Neue | Ein Palette erstellen. |
| Löschen | Das geöffnete oder ausgewählte Palette löschen. |
| Seereisekosten | Öffnen Sie die Seite **Fahrtkosten**, auf der Sie die Kosten auf Paletteebene für alle Waren der Fahrt anzeigen und hinzufügen können. Wenn Palette-Kosten manuell zur Fahrt hinzugefügt werden, werden sie automatisch zur Seite Kostenabfrage hinzugefügt und auf jede Ware gemäß der Methode aufgeteilt, die auf der Seite **Fahrtkosten** angegeben ist. |

### <a name="buttons-on-the-manage-tab"></a>Schaltflächen auf der Registerkarte Manage

Die folgende Tabelle beschreibt die Schaltflächen, die auf der Registerkarte **Verwalten** des Aktivitätsbereichs verfügbar sind.

| Schaltfläche | Beschreibung |
|---|---|
| Zugangsliste buchen | Eine Eingangsliste für alle Zeilen der Einkaufsbestellung in der Palette buchen. Wenn Sendungen mit mehreren Firmen verwendet werden, wird für jede Firma ein neues Dialogfenster zum Buchen einer Bonliste geöffnet. |
| Produktzugang buchen | Buchen Sie einen Wareneingang für alle Zeilen der Einkaufsbestellung in der Palette. Wenn Fahrten mit mehreren Firmen verwendet werden, wird für jede Firma ein neues Dialogfenster zum Buchen eines Produkteingangs geöffnet. |
| Rechnung buchen | Buchen Sie eine Rechnung für alle Zeilen der Einkaufsbestellung in der Palette. Wenn Fahrten mit mehreren Firmen verwendet werden, wird für jede Firma eine neue Dialogbox für die Rechnungsbuchung geöffnet. |
| Umlagerungsauftrag versenden | Buchen Sie einen Umlagerungsauftrag für alle Transportauftragszeilen, die sich auf die aktuelle Palette in der zugehörigen Sendung beziehen. |
| Umlagerungsauftrag empfangen | Buchen Sie einen Umlagerungsauftrags-Eingang für alle Transportauftragszeilen, die sich auf die aktuelle Palette in der zugehörigen Sendung beziehen. |
| Waren in Zustellung empfangen | Empfangen Sie alle Auftragszeilen, die sich in Zustellung in der Palette befinden. |
| Belege empfangen | Aktualisieren Sie die Einstellung der Option **Dokumente empfangen** auf *Ja*. Mit dieser Schaltfläche können Sie den Artikel und/oder die Kauf-Zeile sperren, so dass sie nicht weiter aktualisiert werden können. |
| Automatische Kosten suchen | Finden Sie relevante Kalkulationen für die Fahrt. Wenn diese Kalkulationen bereits gefunden oder aktualisiert wurden, erhalten Sie die folgende Meldung: „Es existieren nicht kalkulierte Kostenzeilen. Möchten Sie diese überschreiben?“ Beachten Sie, dass Fahrtkosten, die an die Palette angehängt sind und die kalkuliert wurden, nicht überschrieben werden. |
| Eingangserfassung erstellen | Erzeugen Sie eine Wareneingangserfassung für Organisationen mit Hilfe der erweiterten Funktionen für Lagerorte. Sie können wählen **Menge initialisieren** (empfohlen), **Erstellen aus Waren in Zustellung** und/oder **Erstellen aus Einkaufsbestellungen**. Die letzte Option hängt davon ab, ob die Verarbeitung von Waren in Zustellung verwendet wird. |
| Kosten antizipieren | Kosten kalkulieren, wenn für eine Kostenart ein Hauptbuchkonto für die Belastung angegeben ist. Diese Schaltfläche wird typischerweise verwendet, wenn sich der Bestand in Zustellung befindet oder wenn Waren eingegangen sind und in Rechnung gestellt wurden. |

### <a name="buttons-on-the-general-tab"></a>Schaltflächen auf der Registerkarte Allgemein

Die folgende Tabelle beschreibt die Schaltflächen, die auf der Registerkarte **Allgemein** des Aktivitätsbereichs verfügbar sind.

| Schaltfläche | Beschreibung |
|---|---|
| Zugangsliste | Eine Eingangsliste für alle Zeilen der Einkaufsbestellung in der Palette buchen. Wenn Fahrten mit mehreren Firmen verwendet werden, wird für jede Firma ein neues Dialogfeld für die Buchung der Eingangsliste geöffnet. |
| Produktzugang | Zeigen Sie den Wareneingangsdatensatz an, wenn er verwendet wird. |
| Wareneingang | Zeigen Sie die Wareneingangserfassung an, wenn sie verwendet wird. |
| Kostenabfrage | Öffnen Sie die Seite für die Abfrage der Kosten, um alle Kalkulationen einer Fahrt anzuzeigen, einschließlich Transportcontainer, Palette und Einkaufsbestellung. Sie können die genaue Ansicht der Seite mit der Aktion Ansicht anpassen. Auf der Seite für die Abfrage der Kosten können Sie alle Bereiche sowie den Code des Artikels und der Kalkulation anzeigen. Indem Sie diese Artikel entfernen, können Sie die Seite anpassen, indem Sie die Kalkulationen gruppieren. Diese Funktionalität kann nützlich sein, wenn Sie Größen und Farben verwenden. Sie können die Dimensionen, die auf der Seite angezeigt werden, ändern. Die Seite **Kosten** zeigt nur Kostenartencodes an, bei denen der Eintrag **Dr** auf der Registerkarte **Buchung** auf *Artikel* festgelegt ist. |

## <a name="header-view"></a>Kopfzeilenansicht

Um die Ansicht **Kopfzeile** zu öffnen, öffnen Sie ein Palette und wählen dann die Registerkarte **Kopfzeile** oben rechts in der Paletteüberschrift.

### <a name="settings-on-the-general-fasttab"></a>Einstellungen auf der Registerkarte Allgemein

Die folgende Tabelle beschreibt die Felder, die auf der Registerkarte **Allgemein** des Inforegisters in der Ansicht **Kopfzeile** eines Paletten verfügbar sind.

| Feld | Beschreibung |
|---|---|
| Folio | Der Name des Paletten. Dieser Name wird automatisch generiert, wenn das Palette erstellt wird.|
| Seereise | Die Fahrt, die mit dem Palette verknüpft ist. |
| Zollbroker | Wählen Sie den Zoll Broker für das Palette. Zoll-Broker werden auf dem Verkäufer definiert. Sie ermöglichen die automatische Ermittlung der erstellten Kalkulationen. |
| Haus-Luftfrachtbrief/-Frachtbrief | Geben Sie den Haus-Luftfrachtbrief oder das Konnossement an, das für die Palette gilt. |
| Firma | Die juristische Entität (Firma), die mit dem Palette verbunden ist. |
| Frachtkontrollnummer | Dieses Feld wird von Zollabteilungen in einigen Ländern oder Regionen verwendet. |
| Verbrauchsberechnung | Mit diesem Feld kann eine Messung im Modul **Gesamttransportkosten** angegeben werden. Kennzahlen werden oft von Organisationen verwendet, die das individuelle Volumen oder Gewicht von Waren nicht kennen, aber eine genauere Aufteilung benötigen, als die Menge oder Quantität liefert. Der Spediteur stellt das Gewicht oder die kubische Messung zur Verfügung, und Sie können es entweder auf der Ebene eines Artikels oder der Einkaufsbestellung einlagern. Es kann automatisch aktualisiert werden, wenn der Parameter ausgewählt oder manuell eingegeben wird. |
| Maßeinheit | Die Einheit, die für die angegebene Messung gilt. |
| Anzahl der Kartons | Die Anzahl der Kartons in der Palette. Dieses Feld kann automatisch aktualisiert werden, abhängig von der Auswahl des Parameters. |
| Kreditorenkonto | Wählen Sie den Verkäufer, der mit der Palette verbunden ist. Dieses Feld dient nur zu Informationszwecken. Es hat keinen Einfluss auf die Funktionalität. |
| Name | Der Name des gewählten Lieferantenkontos. |
| Bemerkungen | Geben Sie alle zusätzlichen Informationen ein, die sich auf die Palette beziehen. |
| Warenbeschreibung | Wählen Sie eine Warenbeschreibung, um die Palette zu identifizieren. Weitere Informationen finden Sie unter [Beschreibung der Waren](shipping-information-setup.md#description-of-goods). |
| Bewertungsdatum | Dieses Feld bezieht sich auf die Seite für die Zollerfassung. Das Modul **Gesamttransportkosten** verwendet den Zoll-Wechselkurs für das Datum, das Sie hier festlegen. Der Standardwert ist das Datum auf der Zolleingabeseite. |
| Zoll-ID | Geben Sie die Zoll-ID ein. Die Zollabteilungen der Länder oder Regionen stellen diese ID zur Verfügung. |
| Tarifcode | Geben Sie einen Zollsatz-Code ein, der mit der Palette verknüpft werden soll. Dieser Code wird normalerweise von dem Land oder der Region, in das/die Sie versenden, benötigt (und definiert). |

### <a name="settings-on-the-delivery-fasttab"></a>Einstellungen auf dem Inforegister Lieferung

Die folgende Tabelle beschreibt die Einstellungen, die auf der Inforegisterkarte **Lieferung** der Ansicht **Kopfzeile** einer Palette verfügbar sind.

| Feld | Beschreibung |
|---|---|
| Foliodatum | Wählen Sie ein Datum, das mit der Palette verknüpft werden soll. Der Standardwert ist das Erstellungsdatum der Fahrt. |
| ETA am Versandport. | Das Datum der geschätzten Ankunftszeit (ETA) am Zielhafen („An Hafen“). |
| Vorkalkuliertes Lieferdatum | Normalerweise ist dies das Datum, an dem die Waren im Lagerort eintreffen sollen. Dieses Feld wird nicht verwendet, wenn das geschätzte Lieferdatum berechnet wird. (Stattdessen wird das geschätzte Lieferdatum der Tracking-Kontrolle verwendet.) Um dieses Feld so festzulegen, dass der Wert mit dem geschätzten Lieferdatum der Tracking-Kontrolle übereinstimmt, verwenden Sie das [Tracking-Control-Center](delivery-information-setup.md#tracking-control-center). |
| Ursprüngliche Belege empfangen | Das Datum, an dem die Originaldokumente empfangen wurden. |
| Vom Broker empfohlen | Das Datum, an dem der Broker benachrichtigt wurde. |
| Ursprünglicher Frachtbrief gesendet | Das Datum, an dem der Originalkonnossement gesendet wurde. |
| Warenfreigabe | Das Datum, an dem die Waren freigegeben wurden. |
| Debitorentermin | Das Datum, an dem der Kunde benachrichtigt wurde. |
| Auslieferung am Lagerort | Das Datum, an dem die Waren im Lagerort angeliefert wurden. |
| Überprüfungsdatum | Das Datum der Überprüfung. |
| Lieferanweisungen | Das Datum, an dem die Lieferanweisungen empfangen wurden. |
| Von-Port | Der Hafen, von dem die Fahrt ausgeht. |
| Bis-Port | An Hafen, in dem die Fahrt ankommt. Der Transportcontainer kann einen anderen Hafen haben, weil das Schiff möglicherweise in mehreren Häfen anhält. |

### <a name="settings-on-the-export-fasttab"></a>Einstellungen auf dem Inforegister Export

Die folgende Tabelle beschreibt die Einstellungen, die auf der Inforegisterkarte **Export** der Ansicht **Kopfzeile** einer Palette verfügbar sind.

| Feld | Beschreibung |
|---|---|
| Exporteur | Der Exporter kann in der Palette gespeichert werden. Im internationalen Handel kann es vorkommen, dass Sie eine Einkaufsbestellung an eine Firma senden, aber die Waren von einer anderen Firma erhalten. Die Verfolgung und Dokumentation wird vom Zoll verlangt. Der Name und die Adresse des Ausführers können hier gespeichert werden. |
| Name | Der Name des ausgewählten Ausführers. |

## <a name="lines-view"></a>Ansicht Zeilen

Um die Ansicht **Zeilen** zu öffnen, öffnen Sie ein Palette und wählen dann die Registerkarte **Zeilen** oben rechts in der Palette-Überschrift.

### <a name="information-on-the-folio-fasttab"></a>Informationen über das Inforegister Palette

Die Inforegister-Registerkarte **Palette** in der Ansicht **Zeilen** zeigt Informationen über das Palette an. Die meisten dieser Informationen erscheinen auch in der Ansicht **Kopfzeile**, wie weiter oben in diesem Thema beschrieben.

### <a name="information-and-buttons-on-the-lines-fasttab"></a>Informationen und Schaltflächen auf dem Inforegister Zeilen

Das Inforegister **Zeilen** in der Ansicht **Zeilen** zeigt Details zu jeder vollständigen oder teilweisen Zeile der Einkaufsbestellung, die in der aktuellen Palette enthalten ist.

Die folgende Tabelle beschreibt die Schaltflächen, die auf der Registerkarte **Zeilen** des Inforegisters in der Ansicht **Zeilen** verfügbar sind.

| Schaltfläche | Beschreibung |
|---|---|
| Entfernen | Entfernen Sie die ausgewählte Zeile der Einkaufsbestellung aus der Fahrt. |
| Bestand \>-Transaktionen | Zeigen Sie Bestandstransaktionen für die ausgewählte Zeile der Einkaufsbestellung an. Beachten Sie, dass bei Waren in Zustellung auch die ursprüngliche Bestellung und die Bestellungen von Waren in Zustellung angezeigt werden. |
| Bestand \> Dimensionen anzeigen | Öffnet ein Dialogfeld, in dem Sie die Bestandsdimensionen auswählen können, die für die angezeigten Transaktionen erscheinen. |
| Aktualisier. | Informationen aktualisieren, die sich auf den Zeilenbetrag, das Gewicht oder das Volumen der ausgewählten Zeile der Einkaufsbestellung beziehen. |

### <a name="information-on-the-lines-details-fasttab"></a>Informationen auf dem Inforegister Zeilen-Details

Das Inforegister **Zeilen-Details** in der Ansicht **Zeilen** zeigt Details zur Zeile der Einkaufsbestellung an, die gerade auf dem Inforegister **Zeilen** ausgewählt ist.
