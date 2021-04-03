---
title: Über-/Unterbuchungen
description: Dieses Thema enthält Informationen, die Ihnen dabei helfen, die Details der Richtlinien für Über-/Unter-Transaktionen festzulegen, damit das System bestimmen kann, wie die Über- und Unterbearbeitung von Waren zum Zeitpunkt des Eingangs gehandhabt werden soll.
author: sherry-zheng
manager: tfehr
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMOverUnderTrans, ITMOverUnderToleranceTable, ITMOverUnderReasonTable, ITMOverUnderToleranceGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 9027d5dc73ebd78a65429f7bc63a1ebf8ef60dac
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500981"
---
# <a name="overunder-transactions"></a>Über-/Unterbuchungen

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Wenn die Bestellungen einer Fahrt verarbeitet werden, erwartet das System, dass die Artikelmenge, die im endgültigen Ziellagerort zum Verbrauch eintrifft, mit der Menge übereinstimmt, die auf den Zeilen der Einkaufsbestellung angegeben ist, die mit der Fahrt verbunden sind. Da jedoch nicht immer die exakte Menge auf den Zeilen der Einkaufsbestellung im Lagerort eintrifft, definiert das Modul **Gesamttransportkosten** eine Reihe von Regeln, die verwendet werden, um Über- und Unterempfang von Waren zu behandeln. Diese Regeln sind besonders wichtig, weil die ursprüngliche Einkaufsbestellung bereits fakturiert wurde und nicht mehr geändert werden kann. Indem Sie die Details der Richtlinien für Über-/Unter-Transaktionen festlegen, ermöglichen Sie dem System, zu bestimmen, wie die Über- und Unterbearbeitung von Waren zum Zeitpunkt des Eingangs gehandhabt werden soll. Sie können Über- und Unterbestände auch manuell verwalten, indem Sie die Seite **Über-/Unter-Transaktionen** verwenden.

## <a name="overunder-tolerances"></a>Über-/Untertoleranzen

Sie legen Über- und Unterlieferungstoleranzen fest, um die Über- und Untermengen oder Volumina anzugeben, die auf einer Fahrt verarbeitet werden können, ohne einen Fehler zu verursachen. Wenn der Eingang einer Fahrt außerhalb dieser Toleranzen liegt, muss er geändert und aufgelöst werden, bevor die Fahrt zur weiteren Verarbeitung geschlossen werden kann.

Um die Toleranzen zu konfigurieren, gehen Sie zu **Gesamttransportkosten \> Über/Unter-Einstellung \> Über/Unter-Toleranzen**. Dort können Sie Toleranzsätze anzeigen, bearbeiten, hinzufügen und entfernen. Die folgende Tabelle beschreibt die Felder, die für jeden Datensatz verfügbar sind.

| Feld | Beschreibung |
|---|---|
| Kontocode | <p>Legen Sie den Umfang der Lieferanten fest, für die die Toleranz gilt, indem Sie einen der folgenden Werte wählen:</p><ul><li>**Tabelle** - Die Über-/Untertoleranz gilt nur für den Lieferanten, der für die Zeile ausgewählt ist.</li><li>**Gruppe** - Die Über-/Untertoleranz gilt für alle Lieferanten in der Lieferanten-Toleranzgruppe, die für die Zeile ausgewählt ist.</li><li>**Alle** - Die Über-/Untertoleranz gilt für alle Lieferanten.</li></ul> |
| Kontenbeziehung | Wählen Sie den Lieferanten oder die Lieferantengruppe, für den/die die Über-/Untertoleranz gilt, abhängig von dem Wert, den Sie im Feld **Kontocode** gewählt haben. |
| Artikelcode | <p>Definieren Sie den Umfang der Artikel, für die die Toleranz gilt, indem Sie einen der folgenden Werte wählen:</p><ul><li>**Tabelle** - Die Über-/Untertoleranz gilt nur für den Artikel, der für die Zeile ausgewählt ist.</li><li>**Gruppe** - Die Über-/Untertoleranz gilt für alle Artikel in der Artikeltoleranzgruppe, die für die Zeile ausgewählt ist.</li><li>**Alle** - Die Über-/Untertoleranz gilt für alle Artikel.</li></ul> |
| Artikelrelation | Wählen Sie den Artikel oder die Artikelgruppe aus, für den/die die Über-/Untertoleranz gilt, abhängig von dem Wert, den Sie im Feld **Artikelcode** ausgewählt haben. |
| Betragstoleranz | Geben Sie die Betragstoleranz ein, die auf eine ganze Einkaufsbestellung angewendet werden soll. |
| Toleranzprozentsatz | Geben Sie die prozentuale Toleranz ein, die auf eine einzelne Zeile der Einkaufsbestellung angewendet werden soll. |

## <a name="overunder-reasons"></a>Gründe für Über/Unter

Wenn eine Über- oder Untermenge mit einer eingegangenen Fahrt-Zeile verbunden ist, müssen Sie eventuell den Grund für die Über- oder Untermenge identifizieren. In diesem Fall können Sie den Grund für die Über- oder Unterlieferung in der Empfangszeile beim Empfang der Waren auswählen.

Um Über- und Unterlieferungsgründe festzulegen, gehen Sie zu **Gesamttransportkosten \> Über/Unter-Einstellung \> Über/Unter-Gründe**. Dort können Sie die verfügbaren Über- und Unterlieferungsgründe ansehen, bearbeiten, hinzufügen und entfernen. Die folgende Tabelle beschreibt die Felder, die für jeden Grund verfügbar sind.

| Feld | Beschreibung |
|---|---|
| Grund für Über/Unter | Geben Sie einen eindeutigen Namen für den Grund der Über- bzw. Unterlieferungs-Transaktion ein. |
| Beschreibung | Geben Sie eine Beschreibung für den Über-/Unterlieferungsgrund ein. |
| Bewegung | Wählen Sie das Umlagerungserfassung, das mit dem Über-/Untererfassungsgrund verbunden ist. Dieses Feld listet alle verfügbaren Journale auf, die mit einem Journaltyp *Bewegung* auf der Seite **Bestandserfassunge** (**Bestandsverwaltung einrichten \> Journale \> Bestand**) verknüpft sind. |

## <a name="item-overunder-tolerance-groups"></a>Über/Unter-Toleranzgruppen für Artikel

Artikel, die ähnliche Toleranzen haben, können in Gruppen zusammengefasst werden. Auf diese Weise können Sie die Über-/Untertoleranz für alle Artikel in dieser Gruppe gleichzeitig festlegen.

Um Artikel-Über-/Unter-Toleranzgruppen festzulegen, gehen Sie zu **Gesamttransportkosten \> Über-/Unter-Einstellung \> Artikel-Über-/Unter-Toleranzgruppen**. Dort können Sie Über-/Unter-Toleranzgruppendatensätze anzeigen, bearbeiten, hinzufügen und entfernen. Die folgende Tabelle beschreibt die Felder, die für jeden Datensatz verfügbar sind.

| Feld | Beschreibung |
|---|---|
| Über/Untertoleranzgruppe | Geben Sie einen eindeutigen Namen für die Gruppe ein. Wählen Sie einen Namen, der die Toleranz beschreibt, z.B. *1% Var*. |
| Beschreibung | Geben Sie eine Beschreibung der Gruppe ein. |

## <a name="vendor-overunder-tolerance-groups"></a>Über/Unter-Toleranzgruppen für Kreditor

Sie können Lieferanten zusammenfassen, die regelmäßig Über- oder Unterlieferungen haben. Sie können dann die Über-/Untertoleranz pro Gruppe festlegen.

Um Lieferanten-Über-/Unter-Toleranzgruppen einzurichten, gehen Sie zu **Gesamttransportkosten \> Über-/Unter-Einstellung \> Lieferanten-Über-/Unter-Toleranzgruppen**. Dort können Sie Über-/Unter-Toleranzgruppendatensätze anzeigen, bearbeiten, hinzufügen und entfernen. Die folgende Tabelle beschreibt die Felder, die für jeden Datensatz verfügbar sind.

| Feld | Beschreibung |
|---|---|
| Über/Unter-Gruppen | Geben Sie einen eindeutigen Namen für die Gruppe ein. Wählen Sie einen Namen, der die Art der Lieferanten beschreibt, die zu dieser Gruppe gehören. |
| Beschreibung | Geben Sie eine Beschreibung der Gruppe ein. |

## <a name="view-and-process-overunder-transactions"></a>Anzeigen und Bearbeiten von Über-/Unter-Transaktionen

Über- und Untertransaktionen werden erzeugt, wenn die Menge der eingelagerten Waren nicht mit der initialisierten Menge übereinstimmt. Die Menge in der Wareneingangserfassung sollte nur mit der Menge aktualisiert werden, die eingelagert wurde.

Bei der Verarbeitung des Eingangs von Fahrt-Zeilen können Über-/Unter-Toleranzen für einen Lieferanten festgelegt werden. Die Artikel werden dann überprüft und validiert. Die Toleranz kann als Prozentsatz, ein lokaler Betrag oder beides festgelegt werden.

Wenn ein Artikel, der empfangen wird, innerhalb der Toleranz liegt, erzeugt das System ein Umlagerungserfassung. Dieses Journal kann auf der Seite mit den Parametern für die Fahrt angegeben werden. Außerdem wird eine Über-/Unter-Transaktion erstellt. Beispiel: Der Bestellwert ist $100, der Eingangswert ist $99 und diese Werte entsprechen den Toleranzregeln. In diesem Fall wird eine negative Bewegungserfassung für die zu wenig erhaltene Menge erstellt.

Wenn ein empfangener Artikel außerhalb der Toleranz liegt, erzeugt das System eine Über-/Unter-Transaktion für die Mengendifferenz.

Um Über-/Unter-Transaktionen anzuzeigen und zu bearbeiten, gehen Sie zu **Gesamttransportkosten \> Abfragen \> Über-/Unter-Transaktionen**. Dort wird eine Über-/Unter-Transaktion mit allen Artikeln einer Fahrt verknüpft, die zu viel oder zu wenig erhalten haben. Wir empfehlen, dass Sie die Seite **Über-/Unter-Transaktionen** verwenden, um alle Über-/Unter-Transaktionen aufzulösen, die mit Fahrten verknüpft sind. Wir empfehlen Ihnen auch, **keine** Bewegungs- oder Zählerfassunge zu verwenden, um manuell Transaktionen für Lagerorte mit Unterlieferungen aufzulösen. Stattdessen sollten Sie die Seite **Über-/Unter-Transaktionen** verwenden, um die Lagerorte mit Unterlieferungen zu verwalten.

### <a name="upper-overview-tab"></a>Registerkarte Obere Übersicht

Um Ihre Über-/Unter-Transaktionen anzuzeigen, wählen Sie die Registerkarte **Übersicht** im oberen Teil der Seite **Über-/Unter-Transaktionen**. Die folgende Tabelle beschreibt die Felder, die in dem Raster verfügbar sind.

| Feld | Beschreibung |
|---|---|
| Über-/Unterbuchungsnummer | Der eindeutige Name des Datensatzes der Über/Unter-Transaktion, der automatisch erstellt wurde, als die Wareneingangserfassung verarbeitet wurde. |
| Seereise | Die Fahrt, an die die Kauf-Zeile angehängt wurde. |
| Versandcontainer | Der Container, an den die Kaufzeile angehängt war. |
| Eingangserfassung | Die Wareneingangserfassung, aus der die Over/Under-Zeile erzeugt wurde. |
| Referenz | Ein Verweis auf die Einkaufsbestellung oder den Umlagerungsauftrag, der mit der Über/Unter-Transaktion verknüpft ist. |
| Anzahl | Die Einkaufsbestellung, auf die in der Über-/Unter-Transaktion verwiesen wird. |
| Kreditorenkonto | Der Lieferant, auf den sich die Über- oder Unterschreitung bezieht. |
| Waren in Zustellung – Nummer | Die Nummer der Waren in Zustellung, falls zutreffend. |
| Artikelnummer | Die Nummer des Artikels, auf den sich die Über- oder Unterschreitung bezieht. |
| Ursprüngliche Menge | Die ursprüngliche Menge der Zeile der Einkaufsbestellung, die an die Sendung angehängt ist. |
| Eingangsmenge | Die Menge, die tatsächlich eingegangen ist. |
| Differenz | Die Differenz zwischen dem erwarteten Betrag in der Wareneingangserfassung und dem Betrag, der in der Wareneingangserfassung gebucht wurde. Ein negativer Wert weist auf eine Überlieferung von Waren hin. |
| Restmenge | Die Menge, die in der Zeile der Wareneingangserfassung verbleibt. |
| Über-/Unterlieferung | Ein Wert, der angibt, ob es sich bei der eingegangenen Menge um eine Über- oder Unterlieferung handelt. |
| Status | Der Status der Über-/Unter-Transaktion. Je nach den Einstellungen auf der Seite **[Gesamttransportkosten-Parameter](landed-cost-parameters.md)** kann die Überlieferung automatisch ein Umlagerungserfassung für den Überlieferungsbetrag erstellen und das Journal buchen. In diesem Fall hat die Über-/Unterlieferungstransaktion den Status *Erledigt*. Wenn eine Aktion erforderlich ist, um die Waren aus dem Lagerort der Unterlieferung zu bewegen, hat der Datensatz den Status *In Bearbeitung*. |
| Grund für Über/Unter | Der Grund, der mit der Über-/Unter-Transaktion verbunden ist. |
| Andere Bestandsdimensionen | Sie können nach Bedarf Spalten für zusätzliche Dimensionen im Raster einblenden. Zu diesen Dimensionen gehören Chargennummer, Bestandsstatus und Lagerort. Wählen Sie im Aktivitätsbereich **Inventar \> Dimensionen anzeigen**, um ein Dialogfeld zu öffnen, in dem Sie die einzuschließenden Dimensionen auswählen können. |

### <a name="upper-general-tab"></a>Obere Registerkarte Allgemein

Um weitere Informationen über die Zeile anzuzeigen, die gerade auf der oberen **Übersicht** ausgewählt ist, wählen Sie die Registerkarte **Allgemein** im oberen Teil der Seite **Über/unter Transaktionen**. Die Informationen auf dieser Registerkarte enthalten die Werte für alle verfügbaren Dimensionen. Diese Informationen werden aus der verursachenden Einkaufsbestellung gezogen.

### <a name="lower-overview-tab"></a>Untere Registerkarte Übersicht

Um den Dokumenttyp für die Zeile anzuzeigen, die auf der oberen Registerkarte **Übersicht** ausgewählt ist, wählen Sie die Registerkarte **Übersicht** im unteren Teil der Seite **Über/unter Transaktionen**. In der folgenden Tabelle werden die Felder beschrieben, die zur Verfügung stehen.

| Feld | Beschreibung |
|---|---|
| Neuer Dokumenttyp | Dieses Feld ist entweder auf *Umlagerungserfassung* oder *Einkaufsbestellung* festgelegt, abhängig von der Aktion, die in der ausgewählten Über/Unter-Transaktionszeile angezeigt wird. |
| Anzahl | Ein Verweis und eine Verknüpfung entweder zur Einkaufsbestellung oder zum Umlagerungserfassung, die mit der ausgewählten Über/Unter-Transaktionszeile verknüpft ist. |
| Grund für Über/Unter | Der Grund, der mit der ausgewählten Über/Unter-Transaktionszeile verknüpft ist. |
| Leistung | Die Menge, die Sie für die Einkaufsbestellung oder das Umlagerungserfassung ausgewählt haben, das mit der ausgewählten Über/Unter-Transaktionszeile verknüpft ist. |

### <a name="lower-general-tab"></a>Untere Registerkarte Allgemein

Um die Nummer der Über/Unter-Transaktion, die Los-ID und die Dimensionsnummer anzuzeigen, die mit der ausgewählten Über/Unter-Transaktionszeile verbunden sind, wählen Sie die Registerkarte **Allgemein** im unteren Teil der Seite **Über/Unter-Transaktionen**. 

### <a name="process-overunder-transactions"></a>Über/Unter-Transaktionen bearbeiten

Der Aktivitätsbereich auf der Seite **Über/Unter-Transaktionen** bietet die folgenden Befehle zur Verarbeitung der Transaktionen, die auf der Seite ausgewählt sind. Mit jedem Befehl können Sie wählen, wie die einzelnen Transaktionen verarbeitet werden sollen.

- **Bewegung \> erstellen** - Erzeugt und bucht ein Umlagerungserfassung für die ausgewählte Transaktion. Für Unter-Transaktionen wird automatisch ein Umlagerungserfassung für die Differenz zwischen der erwarteten und der tatsächlichen Eingangsmenge erstellt und gebucht. Wählen Sie diesen Befehl für Über-Transaktionen, wenn Sie möchten, dass der Lieferant die Kostendifferenz realisiert.
- **Erstelle \> Bestellung** - Erzeugt eine Einkaufsbestellung für die Differenz zwischen der erwarteten und der tatsächlich erhaltenen Menge der ausgewählten Transaktion. Wählen Sie diesen Befehl für Über-Transaktionen, wenn Ihr Unternehmen die Kostendifferenz realisieren wird.
- **Erstellen von \> Umlagerungsauftrag** - Dieser Befehl gilt nur für Umlagerungsaufträge. Wählen Sie ihn, wenn Sie die Über- oder Untermenge an das Ziellagerort übertragen wollen.
- **Erstellen von \> Transfer zum Ursprung** - Dieser Befehl gilt nur für Umlagerungsaufträge. Wählen Sie ihn, wenn Sie die Über- oder Untermenge in das Ursprungslagerort übertragen möchten.
