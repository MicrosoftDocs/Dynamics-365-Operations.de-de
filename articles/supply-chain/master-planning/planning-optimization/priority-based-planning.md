---
title: Prioritätsbasierte Planung
description: In diesem Artikel wird die prioritätsbasierte Planungsfunktion von Microsoft Dynamics 365 Supply Chain Management beschrieben.
author: t-benebo
ms.date: 10/15/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-10-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 1a952fe5734f01325842a8a130b9322eadc67951
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740591"
---
# <a name="priority-based-planning"></a>Prioritätsbasierte Planung

[!include [banner](../../includes/banner.md)]

In diesem Artikel wird die prioritätsbasierte Planungsfunktion von Microsoft Dynamics 365 Supply Chain Management beschrieben. Die Funktion fügt Unterstützung für bedarfsgesteuerte Planung hinzu, die eine Stufe von [Demand Driven Material Requirements Planning (DDMRP)](ddmrp-overview.md) ist. Die prioritätsbasierte Planung ermöglicht es dem System, Bestellvorschläge zu generieren, die von Planungsprioritäten anstelle von Bedarfsterminen gesteuert werden.

Mit der prioritätsbasierten Planung können Sie Wiederbeschaffungsaufträge priorisieren, um sicherzustellen, dass dringender Bedarf gegenüber weniger wichtigem Bedarf priorisiert wird. Zum Beispiel wird ein Wiederbeschaffungsauftrag für Fehlbestände gegenüber einem Wiederbeschaffungsauftrag für Standardnachschub priorisiert. Das System kann größere Aufträge automatisch in separate kleinere Aufträge aufteilen, wobei Auftragspositionen nach Priorität gruppiert sind. Es kann dann alle Aufträge mit hoher Priorität zuerst bearbeiten.

Um einen schnellen Überblick über diese Funktion zu erhalten, sehen Sie sich das folgende Video zur [Unterstützung der Planungsoptimierung für prioritätsbasierte Planung in Dynamics 365 Supply Chain Management](https://youtu.be/GmMHzFETTQc) an.

## <a name="turn-on-priority-based-planning-in-your-system"></a>Prioritätsbasierte Planung in Ihrem System aktivieren

Bevor Sie diese Funktion nutzen können, muss sie für Ihr System aktiviert werden. Administratoren können mit den Einstellungen [Funktionsverwaltung](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und sie aktivieren. Im Arbeitsbereich **Funktionsverwaltung** ist die Funktion wie folgt aufgeführt:

- **Modul:** *Produktprogrammplanung*
- **Funktionsname:** *Prioritätsgesteuerte MRP-Unterstützung für die Planungsoptimierung*

## <a name="where-and-how-planning-priorities-are-assigned"></a>Wo und wie Planungsprioritäten vergeben werden

*Planungspriorität*-Informationen über Angebot und Nachfrage sind das Rückgrat der prioritätsbasierten Planung. Die Planungspriorität definiert die Bedeutung einer Bedarfs- oder Angebotslinie. Die Produktprogrammplanung verwendet sie, wenn das Feld **Dispositionsverfahren** auf *Priorität* gesetzt ist.

Die Planungspriorität ist in der Regel eine Zahl zwischen 0 (null) und 100, wobei 0 die höchste Bedeutung darstellt. Es wird gezeigt und eingestellt im Feld **Planungspriorität**. Dieses Feld finden Sie auf den folgenden Seiten: **Bedarfsplanungspositionen**, **Auftragsdetails**, **Bestellungsdetails**, **Umlagerungsauftragsdetails** und **Details zum Bestellvorschlag**.

Wenn das Feld **Dispositionsverfahren** für die entsprechende Position oder Dispositionssteuerungsgruppe auf *Priorität* gesetzt ist, gleicht die Masterplanung Angebot und Nachfrage durch einen bedarfsorientierten Ansatz aus, indem sie die Planungspriorität berechnet und für jedes freigegebene Produkt die Werte berücksichtigt, die für die Felder **Minimum**, **Neubestellungspunkt** und **Maximum** auf der Seite **Artikeldeckung** festgelegt sind.

> [!NOTE]
> Der *Priorität*-Wert ist für das **Dispositionsverfahren**-Feld nur verfügbar, wenn die Planungsoptimierung aktiviert ist.

Die zugehörigen *Planungsprioritätsmodelle* steuern die Planungspriorität und teilen Bestellvorschläge nach Prioritätsbereich auf. Sie ermöglichen Ihnen außerdem, Standardwerte für die Planungspriorität für jede Angebots- oder Bedarfsart festzulegen und die Prioritätsberechnungsmethode zu definieren.

## <a name="types-of-priority-calculation-methods"></a>Typen von Prioritätsberechnungsmethoden

Jedes Planungsprioritätsmodell hat eine Einstellung für die **Prioritätsberechnungsmethode**, die steuert, wie die Produktprogrammplanung die Priorität auf Bestellvorschläge anwendet. Die verfügbaren Werte sind *Prozentsatz der maximalen Bestandsmenge* und *Prioritätsbereiche*. *Prioritätsbereiche* stellt eine fortgeschrittene Version der Methode *Prozentsatz der maximalen Bestandsmenge* dar.

### <a name="percent-of-maximum-inventory-quantity"></a>Prozentsatz der maximalen Bestandsmenge

In der Berechnungsmethode *Prozentsatz der maximalen Bestandsmenge* findet die Berechnung der Versorgungspriorität den aktuellen *insgesamt verfügbaren Bestand* (Nettofluss) in Prozent des Werts **Maximale Bestandsmenge**, der für einen Artikel festgelegt wird. Pro Artikel und Lieferant wird dann ein einzelner Bestellvorschlag erstellt (es sei denn, die maximale Bestellmenge wird verwendet, um eine Aufteilung zu erzwingen). Die Planungspriorität des Auftrags wird als Prozentsatz des Maximums berechnet.

Verwendete Formel:

*Prozentsatz des Maximums* = (*Nettoflussposition* × 100) ÷ *Maximaler Bestandsmengenwert aus der Artikeldeckung*

In dieser Formel wird *Nettoflussposition* wie folgt berechnet:

*Nettoflussposition* = *Verfügbar* + *In Auftrag* – *Qualifizierter Bedarf*

- *In Auftrag* ist die erwartete Lieferung.
- *Qualifizierter Bedarf* stellt die Nettobedarfe dar, deren Bedarfsdatum innerhalb des Planungszeitraums liegt.

Während des Produktprogrammplanungslaufs werden neue Bestellvorschläge angelegt, wenn die Nettoflussposition kleiner als die Neubestellungspunktmenge für einen Artikel ist. Die Menge für Bestellvorschläge ist die Differenz zwischen dem Wert **Maximale Bestandsmenge**, der auf Artikelebene festgelegt wird, und der Nettoflussposition. Die Bestellvorschlagspriorität wird berechnet als ein *Nettoflussposition*-Prozentsatz des Werts für die **Maximale Bestandsmenge**.

> [!NOTE]
> Die berechnete Priorität darf nicht negativ sein, selbst wenn die Nachfrage das Gesamtangebot übersteigt. Übersteigt die Nachfrage das Gesamtangebot, wird die berechnete Priorität auf 0 (Null) gesetzt.

### <a name="priority-ranges"></a>Prioritätsbereiche

Die *Prioritätsbereiche*-Berechnungsmethode ist fortgeschrittener als die Methode *Prozentsatz der maximalen Bestandsmenge* und wird auf der Ebene des Planungsprioritätsmodells konfiguriert. Es können mehrere neue geplante Lieferaufträge erstellt werden, um den Bedarf pro Artikel zu decken. Die Prioritäten der geplanten Versorgung folgen den Werten, die im Raster **Planungsprioritätsbereiche** auf der Seite **Planungsprioritätsmodelle** definiert sind.

Die folgenden zusätzlichen Regeln treten in Kraft, wenn das Feld **Prioritätsberechnungsmethode** auf *Prioritätsbereiche* gesetzt ist:

- Wenn die Option **Bedarfspriorität berücksichtigen** für das geplante Prioritätsmodell auf *Ja* gesetzt ist, begrenzt die Priorität, die für jede Bedarfsposition festgelegt wird, den Prioritätsbereich-Bucket. Die Priorität eines neuen Bestellvorschlags für die Lieferung wird nicht niedriger sein als die Priorität des Bedarfs. Der obere Wert des Bereichs wird als Schwellenwert betrachtet, mit dem der Prioritätswert des Bedarfs verglichen wird. Liegt die Priorität des Bedarfs genau in der Mitte zwischen den oberen Schwellenwerten zweier Bereiche, wird der Bereich mit der höchsten Priorität (also dem niedrigsten Prioritätswert) ausgewählt.
- Wenn das Feld **Bestellvorschlagerstellung** für das geplante Prioritätsmodell *Einzellieferung mit der wichtigsten Priorität* gesetzt ist, wird nur eine Lieferung erstellt, um das Maximum zu erfüllen. Die Priorität wird auf die Priorität des ersten Bereichs gesetzt, der eine Lieferung auslöst.
- Wenn kein Lagerbestand, kein Angebot und keine Nachfrage vorhanden sind, wird die Zeile im Raster **Planungsprioritätsbereiche**, wo das Feld **Von Menge** auf *Null* gesetzt ist, verwendet werden.
- Wenn Bedarf vorhanden ist, aber kein Lagerbestand oder keine erwartete Lieferung, wird die Zeile im Raster **Planungsprioritätsbereiche**, wo das Feld **Von Menge** auf *Kleiner oder gleich null* gesetzt ist, verwendet werden.
- Wenn der Bereich bewertet wird, zu dem der Bedarf gehört, hat die Einstellung der Option **Bedarfspriorität berücksichtigen** noch Wirkung.

## <a name="differences-between-traditional-timeline-calculations-and-priority-based-planning"></a>Unterschiede zwischen traditionellen Zeitachsenberechnungen und prioritätsbasierter Planung

Die prioritätsbasierte Planung unterscheidet sich in folgenden Punkten von herkömmlichen Zeitachsenberechnungen:

- Alle regulären Vorplanungsprozessoren sind noch in Kraft. Zu diesen Vorprozessoren gehören Bedarfsverursacher genehmigter Bestellvorschläge für Verkaufsbedarf, die Zuordnung von Bestellanforderungen und die Reservierungslogik. Es wird nur Bedarf verarbeitet, der von diesen Vorprozessoren nicht erfüllt wird.
- Bei der Bedarfsverursachung wird das gesamte Angebot unabhängig von seiner Priorität berücksichtigt. Dieses Angebot umfasst den Lagerbestand, den freigegebenen Bestand und den nicht zugeordneten Teil genehmigter Planaufträge.
- Während des gesamten Planungszeitraums kann keine Nachfrage für „negative Tage“ an das Angebot gekoppelt werden.
- Wenn das Angebot an die Nachfrage gekoppelt ist, wird das Angebot mit der höchsten Priorität (also dem niedrigsten Prioritätswert) zuerst aufgebraucht. Es wird davon ausgegangen, dass der Lagerbestand einen Prioritätswert von 0 (Null) hat. Daher wird es als die allererste Quelle konsumiert.
- Neue geplante Lieferpositionen werden gemäß den regulären Regeln für Mindestauftragsgröße, maximale Auftragsgröße, Mengenmultiplikator usw. erstellt.

## <a name="planning-priority-models"></a>Planungsprioritätsmodelle

*Planungsprioritätsmodelle* werden Dispositionssteuerungsgruppen zugeordnet und steuern die Planungspriorität für Bestellvorschläge. Sie definieren die Logik, die bestimmt, wie der Planungsprioritätswert für jeden Bestellvorschlag berechnet wird und wie Bestellvorschlägen, Angebotspositionen und Bedarfspositionen Priorität zugewiesen wird.

Um mit den Planungsprioritätsmodellen zu arbeiten, gehen Sie zu **Produktprogrammplanung \> Einrichtung \> Planungsprioritätsmodelle**. Wie bereits erwähnt, ist eine der wichtigsten Einstellungen eines Modells der Wert **Prioritätsberechnungsmethode**. Diese Einstellung steuert die Berechnungsmethode, die verwendet wird, wenn die Produktprogrammplanung Bestellvorschlägen einen Prioritätswert zuweist.

> [!NOTE]
> Planungsprioritätsmodelle gelten organisationsweit über alle juristischen Personen hinweg.

### <a name="coverage-group"></a>Dispositionssteuerungsgruppe

Richten Sie eine neue Dispositionssteuerungsgruppe ein, die Sie für die prioritätsbasierte Planung verwenden möchten, wie in [Dispositionsregeln für Artikel definieren](../tasks/define-coverage-rules-items.md) beschrieben. Nachdem Sie die Dispositionssteuerungsgruppe erstellt haben, legen Sie die folgenden zusätzlichen Felder fest:

- **Dispositionsverfahren** – Wählen Sie *Priorität* aus, wenn die Dispositionssteuerungsgruppe eine prioritätsbasierte Planung verwendet.
- **Planungsprioritätsmodell** – Wählen Sie ein beliebiges organisationsweites Planungsprioritätsmodell aus.

### <a name="item-coverage"></a>Artikeldeckung

Richten Sie die Einstellungen für die Artikeldeckung ein, wie in [Dispositionseinstellungen](../coverage-settings.md) beschrieben. Standardmäßig wird der für die Dispositionssteuerungsgruppe ausgewählte Wert **Dispositionsverfahren** in die Artikeldeckungseinstellungen kopiert. Allerdings können Sie den Standardwert nach Bedarf ändern. In einigen Fällen ist das Feld **Dispositionsverfahren** für einen Artikeldeckungsdatensatz auf *Planung* gesetzt, aber für die zugehörige Dispositionssteuerungsgruppe ist kein Planungsprioritätsmodell definiert. In diesen Fällen wird jedes Modell, bei dem das Feld **Prioritätsberechnungsmethode** auf *Prozentsatz der maximalen Bestandsmenge* und das Feld **Bestellvorschlagerstellung** auf *Einzellieferung mit der wichtigsten Priorität* gesetzt ist, standardmäßig angewendet.

Legen Sie das Feld **Dispositionsverfahren** auf *Priorität* fest, um das Feld **Wiederbestellpunkt** in den Artikeldeckungseinstellungen verfügbar zu machen. Geben Sie in dieses Feld die Wiederbestellpunktmenge ein, die das System verwenden soll, wenn es bestimmt, wann Bestellvorschläge mit einem **Dispositionsverfahren**-Wert von *Priorität* platziert werden sollen.

Die Wiederbestellpunktmenge wird häufig als Bedarf während der Vorlaufzeit plus einem Mindestwert (Sicherheitsbestand) berechnet. Es muss ein Wert zwischen dem **Minimum**- und **Maximum**-Wert sein.

Sie können die Felder beispielsweise wie folgt festlegen:

- **Minimum:** *10*
- **Wiederbestellpunkt:** *45*
- **Maximal:** *60*

In diesem Beispiel basiert die Wiederbestellpunktmenge auf einer Vorlaufzeit von sieben Tagen und einer durchschnittlichen täglichen Nutzung von 5. Daher beträgt die Nachfrage während der Vorlaufzeit 35. Der Mindestwert von 10 (Sicherheitsbestand) wird dann addiert, um einen Wiederbestellpunkt von 45 zu erhalten. Wenn dieses Setup verwendet wird, wird die Beschaffung vorgeschlagen, wenn der projizierte Lagerbestand unter 45 liegt. Die Auftragspriorität basiert auf der Einrichtung der Planungspriorität.

### <a name="manage-planning-priority-models"></a>Planungsprioritätsmodelle verwalten

Um mit Ihren Planungsprioritätsmodellen zu arbeiten, führen Sie die folgenden Schritte aus.

1. Wechseln Sie zu **Produktprogrammplanung \> Einrichtung \> Planungsprioritätsmodelle**.
1. Wählen Sie entweder ein vorhandenes Modell im Listenbereich, oder wählen Sie **Neu** im Aktivitätsbereich, um ein neues Modell zu erstellen.
1. Legen Sie in der Kopfzeile des Datensatzes die folgenden Felder fest:

    - **Name** – Geben Sie einen Namen für das Modell ein. Der Name muss für alle juristischen Personen in Ihrer Organisation eindeutig sein.
    - **Beschreibung** – Geben Sie eine Beschreibung für das Modell ein.
    - **Prioritätsberechnungsmethode** – Wählen Sie einen der folgenden Werte aus:

        - *Prioritätsbereiche* – Wenn Sie diesen Wert auswählen, wird das Raster **Planungsprioritätsbereiche** verfügbar. Dort müssen Sie mehrere Prioritätsbereiche festlegen, um den Planungsprioritätswert zu definieren.
        - *Prozentsatz der maximalen Bestandsmenge* – Berechnen Sie den Wert der Planungspriorität als Prozentsatz, basierend auf dem prognostizierten Lagerbestand über der maximalen Bestandsmenge.

    - **Bestellvorschlagerstellung** – Dieses Feld ist verfügbar, wenn das Feld **Prioritätsberechnungsmethode** auf *Prioritätsbereiche* gesetzt ist. Wählen Sie einen der folgenden Werte aus:

        - *Einzellieferung mit der wichtigsten Priorität* – Teilen Sie Bestellvorschläge nicht basierend auf dem Prioritätsbereich auf. Die Planungspriorität für einen Bestellvorschlag basiert auf dem wichtigsten Prioritätsbereich (also dem niedrigsten Wert der Planungspriorität).
        - *Gemäß Prioritätsbereichen aufteilen* – Teilen Sie den Bedarf in mehrere Bestellvorschläge auf, basierend auf den Planungsprioritätsbereichen. Die Planungspriorität für einzelne Bestellvorschläge wird durch die Planungspriorität des zugehörigen Planungsprioritätsbereichs definiert.

    - **Bedarfspriorität berücksichtigen** – Setzen Sie diese Option auf *Ja*, um die Priorität eines neuen Bestellvorschlags zu begrenzen, der für die Lieferung angelegt wird. (Die Priorität ist nicht niedriger als die Priorität des entsprechenden Bedarfs.) Wenn Sie diese Option auf *Nein* festlegen, wird die Priorität des Bedarfsauftrags bei der Berechnung der Priorität des Beschaffungsauftrags nicht berücksichtigt.

1. Wenn Sie das Feld **Prioritätsberechnungsmethode** auf *Prioritätsbereiche* festlegen, verwenden Sie die Schaltflächen **Hinzufügen** und **Entfernen** in der Symbolleiste des Inforegisters **Planungsprioritätsbereiche** zum Hinzufügen oder Entfernen von Prioritätsbereichszeilen nach Bedarf. Wenn mehrere Zeilen vorhanden sind und Sie eine neue Zeile einfügen, wird die Planungspriorität automatisch auf den Durchschnitt der ausgewählten Zeile und der darüber liegenden Zeile gesetzt. Legen Sie für jede Position die folgenden Felder fest:

    - **Planungspriorität** – Geben Sie einen beliebigen Wert zwischen 0,00 und 100,00 ein. Dieser Wert stellt die Planungspriorität dar, die für die Zeile verwendet wird. Der niedrigste Prioritätswert repräsentiert die höchste Priorität. Ein Standardwert wird zugewiesen, aber Sie können ihn nach Bedarf ändern. Der gleiche **Planungspriorität**-Wert kann nicht für mehr als einen Planungsprioritätsbereich im selben Planungsprioritätsmodell verwendet werden.
    - **Beschreibung** – Geben Sie eine Beschreibung des Planungsprioritätsbereichs ein (z. B. *Wiederbestellpunkt auf Maximum*).
    - **Von Menge** – Die untere Grenze des Planungsprioritätenbereichs. Dieser Wert ist schreibgeschützt und basiert auf Werten **Bis Menge** und **Prozent von Bis-Menge** für den vorherigen Planungsprioritätsbereich.
    - **Bis Menge** – Wählen Sie das Feld aus der Artikeldeckung aus, das verwendet werden soll, um die obere Grenze des Bereichs zu definieren. Die folgenden Werte werden unterstützt und beeinflussen den **Von Menge**-Wert des nächsten Bereichs:

        - *Null* – Dieser Wert stellt einen negativen bis Nullbereich dar (*Kleiner oder gleich null* bis *Null*). Für Zeilen, in denen dieser Wert ausgewählt ist, ist das Feld **Prozent von Bis-Menge** schreibgeschützt und wird immer auf *100* Prozent gesetzt.
        - *Minimale Bestandsmenge* – Dieser Wert repräsentiert den **Minimum**-Wert für einen Artikel auf der **Artikeldeckung**-Seite. Für Zeilen, in denen dieser Wert ausgewählt ist, ist das Feld **Prozent von Bis-Menge** editierbar und wird verwendet, um den Wert **Von Menge** des nächsten Bereichs festzulegen (zum Beispiel auf *80% der minimalen Bestandsmenge*).
        - *Wiederbestellpunkt* – Dieser Wert repräsentiert den **Wiederbestellpunkt**-Wert für einen Artikel auf der **Artikeldeckung**-Seite. Für Zeilen, in denen dieser Wert ausgewählt ist, ist das Feld **Prozent von Bis-Menge** editierbar und wird verwendet, um den Wert **Von Menge** für den nächsten Bereich festzulegen (zum Beispiel auf *80% des Wiederbestellpunkts*).
        - *Maximale Bestandsmenge* – Dieser Wert repräsentiert den **Maximum**-Wert für einen Artikel auf der **Artikeldeckung**-Seite. Für Zeilen, in denen dieser Wert ausgewählt ist, ist das Feld **Prozent von Bis-Menge** editierbar und wird verwendet, um **Von Menge** des nächsten Bereichs festzulegen (zum Beispiel auf *80% der minimalen Bestandsmenge*).
        - *Unendlich* – Dieser Wert stellt eine unendliche Obergrenze des Bereichs dar (*Unendlich oder weniger* bis *Unendlich*). Für Zeilen, in denen dieser Wert ausgewählt ist, ist das Feld **Prozent von Bis-Menge** schreibgeschützt und wird immer auf *100* Prozent gesetzt.

    - **Prozent von Bis-Menge** – Geben Sie einen Prozentwert ein, der zur Berechnung der Obergrenze des Planungsprioritätsbereichs verwendet wird, basierend auf dem Wert, der im Feld **Bis Menge** ausgewählt wurde. Zum Beispiel, wenn das Feld **Bis Menge** auf *Minimale Bestandsmenge* gesetzt ist und das Feld **Prozent von Bis-Menge** auf *50* gesetzt ist, beträgt die Obergrenze 50 Prozent der Mindestbestandsmenge aus der zugehörigen Artikeldeckung.

1. Legen Sie im Inforegister **Standardwerte für Planungsprioritäten** die Felder nach Bedarf fest, um Standardplanungsprioritäten für jede Art von Angebots- oder Bedarfspositionen (Auftrag, Bestellung, Umlagerungsauftrag oder Bedarfsplanung) zu definieren. Es können nur positive Werte eingegeben werden.

## <a name="view-and-maintain-planning-priority"></a>Planungspriorität anzeigen und verwalten

Die Planungspriorität wird im Feld **Planungspriorität** angezeigt und eingestellt. Dieses Feld finden Sie auf den Seiten, die in der folgenden Tabelle aufgeführt sind. Die Priorität ist als Zahl zwischen 0 (null) und 100 festgelegt, wobei 0 die höchste Bedeutung darstellt.

| Seite | Feldspeicherort | Wertquelle |
|---|---|---|
| Bedarfsplanungspositionen | <p>Registerkarte **Artikel**</p><p>(Wählen Sie im oberen Bereich eine Position aus, und wählen Sie dann die Registerkarte **Artikel**.)</p> | Standardwert oder manuell eingestellter Wert |
| Auftragsdetails | <p>Registerkarte **Lieferung** im Inforegister **Positionsdetails**</p><p>(Wählen Sie eine Position im Inforegister **Auftragspositionen** und dann im Inforegister **Positionsdetails** die Registerkarte **Lieferung** aus.)</p> | Standardwert, Wert von Intercompany oder manuell eingestellter Wert |
| Bestellungsdetails | <p>Registerkarte **Lieferung** im Inforegister **Positionsdetails**</p><p>(Wählen Sie eine Position im Inforegister **Bestellpositionen** und dann im Inforegister **Positionsdetails** die Registerkarte **Lieferung** aus.)</p> | Wert, der bei der Fixierung aus Bestellvorschlägen festgelegt wird, Wert aus Intercompany oder manuell gesetzter Wert |
| Umlagerungsauftragsdetails | <p>Registerkarte **Lieferung** im Inforegister **Positionsdetails**</p><p>(Wählen Sie eine Position im Inforegister **Umlagerungsauftragspositionen** und dann im Inforegister **Positionsdetails** die Registerkarte **Lieferung** aus.)</p> | Wert, der bei der Fixierung aus Bestellvorschlägen festgelegt wird, oder manuell gesetzter Wert |
| Details zum Auftragsvorschlag | **Allgemein**-Inforegister | Wert, der während der Produktprogrammplanung berechnet wird oder manuell gesetzt wird |

### <a name="intercompany-trade"></a>Intercompany-Handel

Der **Planungspriorität**-Wert zu Positionen von Intercompany-Angebot und -Nachfrage wird zwischen den verbundenen Einheiten geteilt. Änderungen auf beiden Seiten werden in der verknüpften Auftragsposition widergespiegelt.

Im Folgenden finden Sie einige Beispiele hierfür:

- Ein Benutzer ändert die Planungspriorität für eine Intercompany-Auftragsposition von 20 auf 30. Diese Änderung spiegelt sich in der verknüpften Intercompany-Bestellposition wider.
- Ein Benutzer ändert die Planungspriorität für eine Intercompany-Bestellposition von 40 auf 50. Diese Änderung spiegelt sich in der verknüpften Intercompany-Auftragsposition wider.
