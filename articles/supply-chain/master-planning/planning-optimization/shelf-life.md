---
title: Produktprogrammplanung für Produkte mit begrenzter Haltbarkeit
description: Dieser Artikel beschreibt, wie Sie Planungsfunktionen einrichten und verwenden, die die Haltbarkeit verderblicher Produkte berücksichtigen.
author: t-benebo
ms.date: 08/10/2022
ms.topic: article
ms.search.form: ReqPlanSched, CustTable, EcoResProductDetailsExtended, InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-08-10
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 95c905cbcc3c057dbccf2b7d6e894b1e99ddfba5
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2022
ms.locfileid: "9337146"
---
# <a name="master-planning-for-products-with-limited-shelf-life"></a>Produktprogrammplanung für Produkte mit begrenzter Haltbarkeit

[!include [banner](../../includes/banner.md)]

Die Haltbarkeit ist die Zeit, die ein Produkt gelagert werden kann, bis es nicht mehr verwendet oder verkauft werden kann. Bei Produkten mit begrenzter Haltbarkeit verwenden Sie wahrscheinlich eine First-Expire-First-Out-(FEFO-)Lagerstrategie, die den Verbrauch und Verkauf von Artikeln aufgrund ihrer verbleibenden Haltbarkeit priorisiert. Diese Lagerstrategie ist für Lebensmittel, Medikamente und andere Waren mit einer kurzen Lagerzeit relevant. Laut FEFO werden Artikel im Lager wie Waren in einem Supermarktregal gelagert: Produkte mit langer Haltbarkeit werden weiter hinten in den Regalen gelagert, sodass Produkte mit einer kürzeren Resthaltbarkeit zuerst versendet werden.

## <a name="using-shelf-life-in-master-planning"></a>Verwendung der Haltbarkeit in der Produktprogrammplanung

In diesem Abschnitt wird erläutert, wie die Produktprogrammplanung Lieferungen für Haltbarkeitsartikel vorschlägt.

Wenn Sie einen Produktprogrammplan ausführen, generiert er vorgeschlagene geplante Aufträge (Lieferung), die Ihren Bedarf decken und darüber hinaus Verzögerungen minimieren. Wenn Ihr Plan Artikel mit begrenzter Haltbarkeit enthält, werden die Planungsberechnungen komplexer, da der Plan nicht nur Verzögerungen minimieren, sondern auch den vorhandenen Bestand nutzen muss, bevor er abläuft. Der Plan muss versuchen, Vorräte, die ihrem Ablaufdatum am nächsten sind, vor solchen zu verwenden, die später ablaufen. Daher strebt die Produktprogrammplanung folgende Ziele in dieser Reihenfolge an:

1. Die Anzahl der Verzögerungen minimieren.
1. Die Summe der FEFO-Bereitstellung maximieren.
1. Die Wiederbeschaffung des Bestands minimieren.

In einigen Fällen kann es zu einem Konflikt zwischen den ersten beiden Zielen kommen und eine Entscheidung muss getroffen werden: Möchten Sie eine Lieferung verzögern oder lieber einen Vorrat verwenden, der später abläuft, anstatt eines Vorrats, der früher abläuft? Um diesen Konflikt während der Produktprogrammplanung zu lösen, priorisiert das System die Minimierung von Verzögerungen gegenüber dem Verbrauch von bald ablaufenden Vorräten. Im Allgemeinen tritt diese Art von Konflikt auf, wenn es zu Verzögerungen und einem Planungshorizont nach Intervall kommen kann. Sie sollten daher ein Sammelbedarfsintervall verwenden, das kürzer ist als die Haltbarkeit eines Artikels. Bei anderen Planungshorizontarten (z. B. Anforderung) ist es unwahrscheinlich, dass diese Art von Konflikt auftritt.

## <a name="set-up-shelf-life"></a>Haltbarkeit einrichten

### <a name="configure-each-master-plan-to-consider-shelf-life"></a>Jeden Produktprogrammplan konfigurieren, sodass er die Haltbarkeit berücksichtigt

Standardmäßig berücksichtigen Produktprogrammpläne die Haltbarkeit nicht. Gehen Sie wie folgt vor, um Haltbarkeitsberechnungen für jeden Produktprogrammplan zu aktivieren, der sie erfordert.

1. Wechseln Sie zu **Produktprogrammplanung \> Einrichten \> Pläne \> Produktprogrammpläne**.
1. Wählen Sie entweder einen Produktprogrammplan im Listenbereich aus oder erstellen Sie einen neuen.
1. Legen Sie auf dem Inforegister **Allgemein** die Option **Haltbarkeitsdaten verwenden** auf *Ja* fest.

### <a name="configure-tracking-dimension-groups-to-track-the-batch-dimension"></a>Rückverfolgungsangabengruppen zur Verfolgung von Chargen-Lagerdimensionen

Die Haltbarkeit eines Artikels kann nur nachverfolgt werden, wenn dieser Artikel in Chargen-Lagerdimension nachverfolgt wird. Mit anderen Worten, die Chargenreferenz und die erforderlichen Daten müssen beim Wareneingang oder bei der Herstellung und bei jeder Bestandstransaktion des Artikels aufgezeichnet werden. Um diese Option zu verwalten, richten Sie eine oder mehrere Rückverfolgungsangabengruppen ein, um die erforderliche Nachverfolgung durchzuführen, und weisen Sie diesen Gruppen dann die relevanten Artikel nach Bedarf zu.

Verwenden Sie das folgende Verfahren, um eine Rückverfolgungsangabengruppe einzurichten, um die Chargen-Lieferdimension zu verfolgen.

1. Gehen Sie zu **Produktinformationsmanagement \> Einrichten \> Dimension und Variantengruppen \> Rückverfolgungsangabengruppen**.
1. Führen Sie einen dieser Schritte aus:

    - Wählen Sie im Aktivitätsbereich **Neu** aus, um eine neue Rückverfolgungsangabengruppe zu erstellen. Geben Sie einen Namen und eine Beschreibung ein und wählen Sie im Aktionsbereich **Neu** aus.
    - Wählen Sie im Listenbereich die vorhandene Rückverfolgungsangabengruppe aus, die Sie zum Nachverfolgen der Chargen-Lieferdimension einrichten möchten.

1. Wählen Sie im Inforegister **Rückverfolgungsangaben** in der Zeile **Chargennummer** die Kontrollkästchen in den Spalten **Aktiv** und **Physischer Bestand** aus.

### <a name="set-up-shelf-life-for-a-product"></a>Das Haltbarkeitsdatum für ein Produkt einrichten

Verwenden Sie das folgende Verfahren, um das Haltbarkeitsdatum für ein Produkt einzurichten.

1. Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**.
1. Legen Sie ein Produkt an oder öffnen Sie eines, das Sie einrichten möchten.
1. Um die Haltbarkeitseinstellungen zu verwenden, legen Sie im Inforegister **Allgemein** das Feld **Rückverfolgungsangabengruppe** auf eine Rückverfolgungsangabengruppe fest, die dafür eingerichtet ist, die Chargen-Lieferdimensionen nachzuverfolgen. Sie können dieses Feld nur festlegen, wenn Sie ein Produkt das erste Mal erstellen. Sie können den Wert für vorhandene Produkte nicht ändern.
1. Legen Sie im Inforegister **Bestand verwalten** die folgenden Felder fest:

    - **Empfohlener Prüfzeitraum in Tagen**: Geben Sie den Zeitraum (in Tagen) an, in dem eine Charge dieses Produkts überprüft werden muss, um sicherzustellen, dass sie für den Verbrauch oder den Wiederverkauf geeignet ist. Der Wert dieses Felds wird zu dem *Herstellungsdatum* einer Charge hinzugerechnet, um das *Datum der Haltbarkeitsinformation* zu bestimmen. Sie können das System so konfigurieren, dass Qualitätsprüfungsaufträge generiert werden, wenn sich eine Charge ihrem Haltbarkeitsdatum nähert.
    - **Haltbarkeitsdauer in Tagen**: Geben Sie die Anzahl der Tage an, nach denen eine Charge dieses Produkts abläuft. Dieser Wert wird zum *Herstellungsdatum* hinzugerechnet, um das *Ablaufdatum* zu errechnen. Nach diesem Datum gilt die Charge als unbrauchbar.
    - **Mindesthaltbarkeitsdauer in Tagen**: Geben Sie den Zeitraum (in Tagen) an, nach dem eine Charge dieses Produkts noch als verkaufsfähig gilt, aber einige ihrer ursprünglichen Eigenschaften verliert. Dieser Wert wird zum *Herstellungsdatum* hinzugerechnet, um das *Mindesthaltbarkeitsdatum* zu errechnen. Sie können Berichte ausführen, um Bestände zu identifizieren, die das Mindesthaltbarkeitsdatum überschritten haben. 

### <a name="set-a-sellable-days-rule-for-each-customer"></a>Für jeden Kunden eine Regel für Tage für Verkauf festlegen

Die Funktionalität *Tage für Verkauf* stellt sicher, dass Produkte aus einer Charge, die bald abläuft, nicht an Kunden verschickt werden. Darüber hinaus stellt sie sicher, dass beim Versand von Produkten an einen Kunden nach der Lieferung noch eine ausreichende Anzahl von Tagen für Verkauf verbleibt.

Um die Funktion „Tage für Verkauf“ zu verwenden, müssen Sie die Anzahl der Tage für Verkauf festlegen, die für jeden Kunden für jedes Produkt (oder jede Produktgruppe) gilt. Sie müssen diesen Vorgang manuell abschließen, da es keine Datenentität dafür gibt.

Verwenden Sie das folgende Verfahren, um für jedes Produkt die Tage für Verkauf für jeden Kunden einzurichten.

1. Wechseln Sie zu **Vertrieb und Marketing \> Debitoren \> Alle Debitoren**.
1. Suchen Sie nach dem Kunden, den Sie einrichten möchten, und wählen Sie ihn aus.
1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Verkaufen** in der Gruppe **Einrichten** auf **Verkaufen \> Tage für Verkauf** aus.
1. Auf der Seite **Tage für Verkauf für Kunden** sind im Raster die vorhandene Regeln für die Tage für Verkauf für jedes Produkt oder jede Produktgruppe aufgeführt. Verwenden Sie die Schaltflächen im Aktivitätsbereich, um im Raster Zeilen nach Bedarf hinzuzufügen oder zu bearbeiten. Mit dem bereitgestellten **Filter** können Sie vorhandene Zeilen finden.
1. Legen Sie für jede Position die folgenden Felder fest:

    - **Artikelcode**: Wählen Sie einen der folgenden Werte aus, um den Umfang der betroffenen Artikel anzugeben:

        - *Tabelle*: Die Zeile gilt für einen bestimmten Artikel.
        - *Gruppe* - Die Zeile gilt für eine bestimmte Artikelgruppe.
        - *Alle*: Die Zeile gilt für alle Artikel.

    - **Artikelrelation**: Wenn Sie das Feld **Artikelcode** auf *Tabelle* festlegen, wählen Sie einen bestimmten Artikel aus. Wenn Sie das Feld **Artikelcode** auf *Gruppe* festgelegt haben, wählen Sie eine Artikelgruppe aus. Falls Sie das Feld **Artikelcode** auf *Alle* festgelegt haben, ist das Feld nicht verfügbar.
    - **Tage für Verkauf**: Geben Sie die Mindestanzahl an Tagen ein, die der Kunde vor Ablauf der Charge braucht, um passende Produkte verkaufen zu können. Der Wert der Tage für Verkauf basiert auf dem angeforderten Wareneingangsdatum (oder, falls festgelegt, dem bestätigten Wareneingangsdatum) für die übereinstimmenden Produkte im Auftrag.
    - *(Andere Produktdimensionen)*: Um den Umfang einer Zeile weiter einzuschränken, geben Sie nach Bedarf andere Dimensionswerte an (z. B. **Größe** und **Farbe**). Um festzulegen, welche Dimensionen im Raster angezeigt werden, wählen Sie im Aktionsbereich **Dimensionen anzeigen** aus.

### <a name="set-up-all-relevant-products-so-that-they-are-fefo-date-controlled"></a>Alle relevanten Produkte so einrichten, dass sie FEFO-datumsgesteuert sind

Damit die Tage für Verkauf funktionieren, muss jeder relevante Artikel zu einer Artikelmodellgruppe gehören, in der das Kästchen **FEFO-datumsgesteuert** aktiviert ist.

Gehen Sie wie folgt vor, um eine Artikelmodellgruppe so einzurichten, dass sie die Funktion „Tage für Verkauf“ unterstützt.

1. Gehen Sie zu **Lagerverwaltung \> Einstellungen \> Bestand \> Element-Modellgruppen**.
1. Wählen Sie entweder eine vorhandene Gruppe im Bereich aus oder erstellen Sie eine neue, indem Sie **Neu** im Aktionsbereich wählen.
1. Aktivieren Sie im Inforegister **Richtlinie für Lagerbestand** das Kontrollkästchen **FEFO-datumsbesteuert** aus.
1. Legen Sie andere Felder für die Gruppe nach Bedarf fest.

Verwenden Sie das folgende Verfahren, um die Artikelmodellgruppe, zu der ein Produkt gehört, anzuzeigen oder festzulegen.

1. Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**.
1. Öffnen Sie das Produkt, das Sie untersuchen oder bearbeiten möchten.
1. Legen Sie im Inforegister **Allgemein** das Feld **Artikelmodellgruppe** auf eine Gruppe fest, in der das Kästchen **FEFO-datumsgesteuert** aktiviert ist.

## <a name="example-1-simple-fefo-10-day-period-zero-days-of-lead-time"></a>Beispiel 1: Einfaches FEFO, 10-Tage-Zeitraum, null Tage Vorlaufzeit

Dieses Beispiel zeigt ein grundlegendes Beispiel für die Haltbarkeit, bei mithilfe des Bedarfsverursachers zwischen den Lieferaufträgen und der Nachfrage die folgenden Ziele des Systems erreicht werden:

- Die Anzahl der Verzögerungen minimieren.
- Die Summe der FEFO-Bereitstellung maximieren.
- Die Wiederbeschaffung des Bestands minimieren.

Das System verfügt über die folgenden Artikel- und Produktprogrammplaneinstellungen:

- **Dispositionsverfahren (Wiederbeschaffungsstrategie):** Zeitraum 
- **Sammelbedarfsintervall:** 10 Tage (entspricht der Haltbarkeit)
- **Haltbarkeit:** 10 Tage
- **Tage für Verkauf:** 0 Tage
- **Vorlaufzeit:** 0 Tage
- **Negative Tage:** 0 Tage
- **Art des Bestellvorschlags (Standardauftragseinstellungen des Artikels):** Bestellung

Die folgenden Kundenaufträge für den Artikel sind im System vorhanden:

- **SO1:** Menge (Mge) = 2, gewünschter Liefertermin = heute + 1 Tag
- **SO2:** Mge = 1, gewünschter Liefertermin = heute + 4 Tage
- **SO3:** Mge = 1, gewünschter Liefertermin = heute + 5 Tage

Alle diese Aufträge erzeugen eine Nachfrage nach dem Artikel.

Für den Artikel ist folgendes Angebot vorhanden:

- **Verfügbarer Lagerbestand:** Mge = 1, Ablaufdatum = heute + 5 Tage
- **Bestellung 1 (PO1):** Wareneingangsdatum = heute + 2 Tage, Mge = 1, Ablaufdatum = heute + 4 Tage

Das System erstellt eine Lieferliste, die diesen Bedarf decken kann, und sortiert die Liste nach dem Ablaufdatum (unter Verwendung von FEFO).

Die Produktprogrammplanung erstellt den erforderlichen Bedarfsverursacher zwischen Angebot und Nachfrage. Sie erstellt auch jeden erforderlichen Bedarf basierend auf der Lieferliste (unter Verwendung von FEFO) und berücksichtigt das Verfügbarkeitsdatum.

- SO1 kann durch die verfügbare Menge erfüllt werden, aber nicht durch PO1, da das Verfügbarkeitsdatum für PO1 einen Tag später liegt als für SO1 erforderlich. Daher erzeugt SO1 Nachfrage nach einer Wareneinheit.
- SO2 kann durch PO1 abgedeckt werden, da PO1 zum gewünschten Zeitpunkt eintrifft und das Ablaufdatum weiterhin gültig ist. Daher wird der SO2-Bedarf vollständig durch PO1 gedeckt.
- SO3 wird nicht abgedeckt, da keine Ressourcen verfügbar sind. Daher erzeugt SO3 Nachfrage nach einer Wareneinheit.

Um alle verbleibenden Bedarfe zu decken, muss das System folgende geplante Einkaufsbesstellung anlegen:

- **PPO1:** Wareneingangsdatum = heute, Mge = 2, Ablaufdatum = heute + 10 Tage

Die folgende Tabelle fasst das Ergebnis zusammen.

| Bedarf | Bedarfsverursacher |
|---|---|
| **SO1:** Liefertermin = heute + 1 Tag, Mge = 2 | <p>**Verfügbar:** Mge = 1, Ablaufdatum = heute + 5 Tage</p><p>**PPO1:** Wareneingangsdatum = heute, Mge = 1, Ablaufdatum = heute + 10 Tage</p> |
| **SO2:** Liefertermin = heute + 4 Tage, Mge = 1 | **PO1:** Wareneingangsdatum = heute + 2 Tage, 1 Mge, Ablaufdatum = heute + 4 Tage |
| **SO3:** Liefertermin = heute + 5 Tage, Mge = 1 | **PPO1:** Wareneingangsdatum = heute, Mge = 2, Ablaufdatum = heute + 10 Tage |

Die folgende Abbildung zeigt die Zeitskala für dieses Beispiel.

![Beispiel 1: Einfaches FEFO, 10-Tage-Zeitraum, null Tage Vorlaufzeit.](media/fefo-example-1.png "Beispiel 1: Einfaches FEFO, 10-Tage-Zeitraum, null Tage Vorlaufzeit")

## <a name="example-2-simple-fefo-requirement-three-days-of-lead-time"></a>Beispiel 2: Einfaches FEFO, Anforderung, drei Tage Vorlaufzeit

Dieses Beispiel zeigt, wie der Versuch des Systems, Verzögerungen zu minimieren, manchmal zu einer Überbestellung führen kann.

Das System verfügt über die folgenden Artikel- und Produktprogrammplaneinstellungen:

- **Dispositionsverfahren (Wiederbeschaffungsstrategie):** Anforderung
- **Haltbarkeit:** 10 Tage
- **Tage für Verkauf:** 0 Tage
- **Vorlaufzeit:** Durch die folgenden Lieferanten-Handelsvereinbarungen festgelegt:

    - **Handelsvereinbarung 1:** Wenn Mge = 1, Vorlaufzeit = 4
    - **Handelsvereinbarung 2:** Wenn Mge = 2, Vorlaufzeit = 3

- **Negative Tage:** 0 Tage
- **Art des Bestellvorschlags (Standardauftragseinstellungen des Artikels):** Bestellung

Im System ist der folgende Auftrag vorhanden:

- **SO1:** Mge = 2, gewünschter Liefertermin = heute + 3 Tage

Dieser Bedarf wird durch das vorhandene Angebot und eine bestätigte Bestellung gedeckt:

- **Verfügbarer Lagerbestand:** Verfügbar = heute, Mge = 1, Ablaufdatum = heute + 2 Tage
- **PO1:** Wareneingangsdatum = heute + 3 Tage, Mge = 1, Ablaufdatum = heute + 4 Tage

SO1 kann nicht durch den verfügbaren Bestand erfüllt werden, da das Ablaufdatum des Bestands vor dem Versanddatum liegt. PO1 kann den SO1-Bedarf mit einer Menge von nur 1 decken. Daher erzeugt SO1 Nachfrage nach einer Wareneinheit. Um diesen Bedarf zu decken, legt das System eine geplante Einkaufbestellung (PPO1) an.

Das System verfügt über zwei Handelsvereinbarungen (eine für Menge = 1, Vorlaufzeit = 4 Tage und eine für Menge = 2, Vorlaufzeit = 3 Tage). Daher versucht das System, Verzögerungen zu minimieren, indem es eine geplante Einkaufsbestellung (PPO1) erstellt, die der zweiten Handelsvereinbarung entspricht. Das Ergebnis ist eine Überlieferung (Menge = 2, Ablaufdatum = heute + 10 Tage).

Die folgende Tabelle fasst das Ergebnis zusammen.

| Bedarf | Bedarfsverursacher |
|---|---|
| **SO1:** Liefertermin = heute + 3 Tage, Mge = 2 | <p>**PO1:** Wareneingangsdatum = heute + 3 Tage, Mge = 1, Ablaufdatum = heute + 4 Tage</p><p>**PPO1:** Wareneingangsdatum = heute + 3 Tage, Mge = 1, Ablaufdatum = heute + 10 Tage</p> |

Die folgende Abbildung zeigt die Zeitskala für dieses Beispiel.

![Beispiel 2: Einfaches FEFO, Anforderung, drei Tage Vorlaufzeit.](media/fefo-example-2.png "Beispiel 2: Einfaches FEFO, Anforderung, drei Tage Vorlaufzeit")

## <a name="example-3-simple-fefo-requirement-three-days-of-lead-time-five-sellable-days"></a>Beispiel 3: Einfaches FEFO, Anforderung, drei Tage Vorlaufzeit, fünf Tage für Verkauf

Dieses Beispiel zeigt, wie die Haltbarkeit funktioniert, wenn für einen Artikel Tage für Verkauf hinzugefügt werden.

Das System verfügt über die folgenden Artikel- und Produktprogrammplaneinstellungen:

- **Dispositionsverfahren (Wiederbeschaffungsstrategie):** Anforderung
- **Haltbarkeit:** 10 Tage
- **Tage für Verkauf:** 5 Tage
- **Vorlaufzeit:** 5 Tage
- **Negative Tage:** 0 Tage
- **Art des Bestellvorschlags (Standardauftragseinstellungen des Artikels):** Bestellung

Im System sind die folgenden Aufträge vorhanden:

- **SO1:** Mge = 2, gewünschter Liefertermin = heute + 2 Tage
- **SO2:** Mge = 1, gewünschter Liefertermin = heute + 3 Tage
- **SO3:** Mge = 1, gewünschter Liefertermin = heute + 5 Tage

Dieser Bedarf kann durch das vorhandene Angebot und eine bestätigte Bestellung gedeckt werden:

- **Verfügbarer Lagerbestand:** Verfügbar = heute, Mge = 1, Ablaufdatum = heute + 6 Tage
- **PO1:** Wareneingangsdatum = heute + 2 Tage, Mge = 3, Ablaufdatum = heute + 10 Tage

Das System erstellt eine Liste mit Bedarfsverursacher-Kandidaten auf der Grundlage der Lieferliste (FEFO) und der Verfügbarkeitsdaten. Daher kann SO1 nicht durch den verfügbaren Lagerbestand erfüllt werden, da dieser Lagerbestand vor dem Ende der Tage für Verkauf abläuft, die der Kunde benötigt (angefordertes Wareneingangsdatum + 5 Tage). PO1 kann den SO1-Bedarf mit zwei Einheiten und den SO2-Bedarf mit einer Einheit decken. Daher hat nur noch SO3 einen ungedeckten Bedarf für eine Wareneinheit. Um diesen Bedarf zu decken, legt das System die folgende geplante Einkaufbestellung an:

- **PP01:** Wareneingangsdatum = heute + 5 Tage, Mge = 1, Ablaufdatum = heute + 10 Tage

Die folgende Tabelle fasst das Ergebnis zusammen.

| Bedarf | Bedarfsverursacher |
|---|---|
| **SO1:** Liefertermin = heute + 2 Tage, Mge = 2 | **PO1:** Wareneingangsdatum = heute + 2 Tage, Mge = 2, Ablaufdatum = heute + 10 Tage |
| **SO2:** Liefertermin = heute + 3 Tage, Mge = 1 | **PO1:** Wareneingangsdatum = heute + 2 Tage, Mge = 1, Ablaufdatum = heute + 10 Tage |
| **SO3:** Liefertermin = heute + 5 Tage, Mge = 1 | **PPO1:** Wareneingangsdatum = heute + 5 Tage, Mge = 1, Ablaufdatum = heute + 10 Tage |

Die folgende Abbildung zeigt die Zeitskala für dieses Beispiel.

![Beispiel 3: Einfaches FEFO, Anforderung, drei Tage Vorlaufzeit, fünf Tage für Verkauf.](media/fefo-example-3.png "Beispiel 3: Einfaches FEFO, Anforderung, drei Tage Vorlaufzeit, fünf Tage für Verkauf")

## <a name="example-4-simple-fefo-period-lead-time-depends-on-the-quantity"></a>Beispiel 4: Einfaches FEFO, Zeitraum, Vorlaufzeit abhängig von der Menge

Dieses Beispiel zeigt, wie der Versuch des Systems, Verzögerungen zu minimieren, manchmal zu einer Überbestellung führen kann.

Das System verfügt über die folgenden Artikel- und Produktprogrammplaneinstellungen:

- **Dispositionsverfahren (Wiederbeschaffungsstrategie):** Zeitraum
- **Sammelbedarfsintervall:** 10 Tage (entspricht der Haltbarkeit)
- **Haltbarkeit:** 10 Tage
- **Tage für Verkauf:** 0 Tage
- **Vorlaufzeit:** Durch die folgenden Lieferanten-Handelsvereinbarungen festgelegt:

    - **Handelsvereinbarung 1:** Wenn Mge = 1, Vorlaufzeit = 5
    - **Handelsvereinbarung 2:** Wenn Mge = 2, Vorlaufzeit = 0

- **Negative Tage:** 0 Tage
- **Art des Bestellvorschlags (Standardauftragseinstellungen des Artikels):** Bestellung

Im System sind die folgenden Aufträge vorhanden:

- **SO1:** Mge = 1, gewünschter Liefertermin = heute
- **SO2:** Mge = 1, gewünschter Liefertermin = heute + 6 Tage

Dieser Bedarf kann teilweise durch vorhandene Lieferungen aus den folgenden bestätigten Bestellungen gedeckt werden:

- **PO1:** Wareneingangsdatum = heute + 1 Tage, Mge = 1, Ablaufdatum = heute + 2 Tage
- **PO2:** Wareneingangsdatum = heute + 3 Tage, Mge = 1, Ablaufdatum = heute + 7 Tage

Das System verfügt über zwei Handelsvereinbarungen (eine für Menge = 1, Vorlaufzeit = 5 Tage und eine für Menge = 2, Vorlaufzeit = 0 Tage). Daher versucht das System, die Verzögerung zu minimieren, indem es die folgende geplante Einkaufsbestellung erstellt, die der zweiten Handelsvereinbarung entspricht:

- **PP01:** Wareneingangsdatum = heute, Mge = 2, Ablaufdatum = heute + 10 Tage

SO1 wird von einer Einheit aus PPO1 abgedeckt. SO2 wird von PO2 abgedeckt, da PO2 früher abläuft als PPO1.

Die folgende Tabelle fasst das Ergebnis zusammen.

| Bedarf | Bedarfsverursacher |
|---|---|
| **SO1:** Liefertermin = heute, Mge = 1 | **PPO1:** Wareneingangsdatum = heute, Mge = 1, Ablaufdatum = heute + 10 Tage |
| **SO2:** Liefertermin = heute + 6 Tage, Mge = 1 | **PO2:** Wareneingangsdatum = heute + 3 Tage, Mge = 1, Ablaufdatum = heute + 7 Tage |

> [!NOTE]
> PO1 wird nicht verwendet, da sie für S01 zu spät eintrifft und abläuft, bevor S02 geliefert wird. PPO1 hat um eine Einheit überbestellt, damit die Vorlaufzeit gemäß Handelsvereinbarung 2 0 (null) sein kann.

Die folgende Abbildung zeigt die Zeitskala für dieses Beispiel.

![Beispiel 4: Einfaches FEFO, Zeitraum, Vorlaufzeit abhängig von der Menge.](media/fefo-example-4.png "Beispiel 4: Einfaches FEFO, Zeitraum, Vorlaufzeit abhängig von der Menge")

## <a name="example-5-simple-fefo-requirement-10-negative-days"></a>Beispiel 5: Einfaches FEFO, Anforderung, 10 negative Tage

<!-- KFM: This is more of a negative days example than a shelf life example. We should point out more explicitly how shelf life affects this situation (or maybe otherwise remove this example). -->

Dieses Beispiel zeigt, wie die Haltbarkeit funktioniert, wenn einem Artikel eine große Anzahl negativer Tage hinzugefügt wird. Unter negativen Tagen versteht man die Anzahl an Tagen, die Sie bereit sind zu warten, bevor Sie einen Artikel mit negativem Bestand wiederbeschaffen. Das System erstellt keine Lieferung, es sei denn, die Anzahl der negativen Tage wird überschritten.

Das System verfügt über die folgenden Artikel- und Produktprogrammplaneinstellungen:

- **Dispositionsverfahren (Wiederbeschaffungsstrategie):** Anforderung
- **Vorlaufzeit:** 0 Tage
- **Negative Tage:** 10 Tage
- **Art des Bestellvorschlags (Standardauftragseinstellungen des Artikels):** Bestellung

Im System ist der folgende Auftrag vorhanden:

- **SO1:** Mge = 1, gewünschter Liefertermin = heute

Dieser Bedarf kann durch vorhandene Lieferungen aus der folgenden bestätigten Bestellung gedeckt werden:

- **PO1:** Wareneingangsdatum = heute + 3 Tage, Mge = 1, Ablaufdatum = heute + 5 Tage

Da das System so konfiguriert ist, dass es 10 negative Tage zulässt, deckt es den Bedarf von SO1 durch Verwendung von PO1, obwohl sich daraus eine Verzögerung von drei Tagen ergeben wird, da SO1 negativen Bestand erstellt, bis PO1 eintrifft. Es wird keine geplante Einkaufsbestellung angelegt, obwohl die Vorlaufzeit 0 (null) ist und das Anlegen einer geplanten Einkaufsbestellung Verzögerungen reduzieren würde.

Die folgende Tabelle fasst das Ergebnis zusammen.

| Bedarf | Bedarfsverursacher |
|---|---|
| **SO1:** Liefertermin = heute, Mge = 1 | **PO1:** Wareneingangsdatum = heute + 3 Tage, Mge = 1, Ablaufdatum = heute + 5 Tage |

Die folgende Abbildung zeigt die Zeitskala für dieses Beispiel.

![Beispiel 5: Einfaches FEFO, Anforderung, 10 negative Tage.](media/fefo-example-5.png "Beispiel 5: Einfaches FEFO, Anforderung, 10 negative Tage")

## <a name="example-6-simple-fefo-requirement-five-negative-days"></a>Beispiel 6: Einfaches FEFO, Anforderung, fünf negative Tage

Dieses Beispiel zeigt, wie die Haltbarkeit funktioniert, wenn die Anzahl negativer Tage für einen Artikel unter dem Haltbarkeitszeitraum liegt.

Das System verfügt über die folgenden Artikel- und Produktprogrammplaneinstellungen:

- **Dispositionsverfahren (Wiederbeschaffungsstrategie):** Anforderung
- **Tage für Verkauf:** 0 Tage
- **Vorlaufzeit:** 0 Tage
- **Negative Tage:** 5 Tage
- **Art des Bestellvorschlags (Standardauftragseinstellungen des Artikels):** Bestellung

Im System ist der folgende Auftrag vorhanden:

- **SO1:** Mge = 2, gewünschter Liefertermin = heute

Dieser Bedarf kann durch vorhandene Lieferungen aus den folgenden bestätigten Bestellungen gedeckt werden:

- **PO1:** Wareneingangsdatum = heute, Mge = 1, Ablaufdatum = heute + 1 Tag
- **PO2:** Wareneingangsdatum = heute + 2 Tage, Mge = 1, Ablaufdatum = heute + 3 Tage

Das System muss jedoch die Einschränkung berücksichtigen, dass versendete Artikel zum Zeitpunkt des Versands nicht abgelaufen sein dürfen. Daher können PO2 und PO1 nicht beide für SO1 verwendet werden, da PO1 abläuft, bevor PO2 ankommt. Das System legt die folgende geplante Einkaufbestellung an, um den Bedarf für SO1 fertig abzudecken:

- **PPO1:** Wareneingangsdatum = heute, Mge = 1, Ablaufdatum = heute + 10 Tage

Das System kann die fünf negativen Tage nutzen und PO2 und PPO1 verwenden, um SO1 abzudecken. Dieser Ansatz führt jedoch dazu, dass sich die Lieferung verzögert, bis PO2 eintrifft, und PO1 in der Zwischenzeit abläuft. Daher deckt das System SO1 ab, indem es PPO1 und PO1 verwendet.

Die folgende Tabelle fasst das Ergebnis zusammen.

| Bedarf | Bedarfsverursacher |
|---|---|
| **SO1:** Liefertermin = heute, Mge = 2 | <p>**PO1:** Wareneingangsdatum = heute, Mge = 1, Ablaufdatum = heute + 1 Tag</p><p>**PPO1:** Wareneingangsdatum = heute, Mge = 1, Ablaufdatum = heute + 10 Tage</p> |

Die folgende Abbildung zeigt die Zeitskala für dieses Beispiel.

![Beispiel 6: Einfaches FEFO, Anforderung, fünf negative Tage.](media/fefo-example-6.png "Beispiel 6: Einfaches FEFO, Anforderung, fünf negative Tage")
