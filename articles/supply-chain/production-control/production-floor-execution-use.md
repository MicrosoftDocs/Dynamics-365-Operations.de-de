---
title: Verwendung der Produktionsausführungsoberfläche durch Arbeitskräfte
description: In diesem Artikel wird beschrieben, wie Sie die Produktionsausführungsoberfläche aus Sicht einer Arbeitskraft verwenden.
author: johanhoffmann
ms.date: 01/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgProductionFloorExecution
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 876ee36c75a31ca89a9351d0ee1484e66076b6aa
ms.sourcegitcommit: 4abf9b375fed6885ea11a425c524958fea29c3b9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/07/2022
ms.locfileid: "9748712"
---
# <a name="how-workers-use-the-production-floor-execution-interface"></a>Verwendung der Produktionsausführungsoberfläche durch Arbeitskräfte

[!include [banner](../includes/banner.md)]

Die Produktionsausführungsoberfläche ist für die Touch-Interaktion optimiert. Das Design bietet einen visuellen Kontrast, der die Barrierefreiheitsanforderungen für Werkstattumgebungen erfüllt. Es bietet dieselben Funktionsfunktionen wie das Einzelvorgangskartengerät. Es ermöglicht jedoch auch das parallele Starten mehrerer Einzelvorgänge aus einer Einzelvorgangsliste. (Diese Funktion wird auch als *Einzelvorgangsbündelung* bezeichnet.) Darüber hinaus können Mitarbeiter aus einer Einzelvorgangsliste einen Leitfaden öffnen, der im Microsoft Dynamics 365 Handbuch erstellt wurde. Auf diese Weise können sie visuelle Anweisungen auf einem HoloLens erhalten.

## <a name="sign-in-to-the-production-floor-execution-interface-as-a-worker"></a>Melden Sie sich bei der Produktionsausführungsoberfläche als Arbeitskraft an

Bevor Arbeitskräfte das Gerät verwenden können, muss es von einem Vorgesetzten oder technischen Personal vorbereitet und in Dynamics 365 Supply Chain Management die richtige Seite geöffnet werden. Weitere Informationen zum Einrichten eines Geräts finden Sie unter [Konfigurieren Sie die Produktionsausführungsoberfläche](production-floor-execution-setup.md).

Nachdem das Gerät vorbereitet wurde, wird die Anmeldeseite darauf angezeigt. Diese Seite enthält Informationen zum Status von Einzelvorgängen für die lokale Arbeitsgruppe. Diese Informationen werden regelmäßig aktualisiert. Auf der Seite verwenden Mitarbeiter ihre Batch-IDs zum Signieren. Obwohl Mitarbeiter kein Benutzerkonto für Supply Chain Management haben müssen, müssen sie ein Konto *Zeit registrierte Arbeitskraft* haben, das sie beim Anmelden verwenden können.

![Produktionsausführungsoberfläche Anmeldeseite.](media/pfei-sign-in-page.png "Produktionsausführungsoberfläche Anmeldeseite")

In den verbleibenden Abschnitten dieses Artikels wird beschrieben, wie Arbeitskräfte mit der Schnittstelle interagieren.

## <a name="all-jobs-tab"></a>Registerkarte alle Einzelvorgänge

Die Registerkarte **Alle Einzelvorgänge** enthält eine Einzelauftragsliste, in der alle Produktionsjobs mit dem Status angezeigt werden *Nicht angefangen*, *Gestoppt*, oder *Gestartet*. (Dieser Registerkartenname ist anpassbar und kann für Ihr System unterschiedlich sein.)

![Registerkarte alle Einzelvorgänge.](media/pfei-all-jobs-tab.png "Registerkarte alle Einzelvorgänge")

Die Einzelvorgangsliste enthält die folgenden Spalten. Die Nummern entsprechen den Nummern in der vorherigen Abbildung.

1. **Auswahlspalte** – In der Spalte ganz links werden Häkchen verwendet, um Jobs anzuzeigen, die vom Mitarbeiter ausgewählt wurden. Arbeitskräfte können mehrere Einzelaufträge gleichzeitig in der Liste auswählen. Um alle Einzelaufträge in der Liste auszuwählen, aktivieren Sie das Häkchen in der Spaltenüberschrift. Wenn ein einzelner Einzelvorgang ausgewählt wird, werden Details zu diesem Einzelvorgang im unteren Teil der Seite angezeigt.
1. **Einzelvorgangsstatusspalte** – In dieser Spalte werden Symbole verwendet, um den Status jedes Einzelvorganges anzuzeigen. Einzelvorgänge, die in dieser Spalte kein Symbol haben, haben den Status *Nicht angefangen*. Ein grünes Dreieck zeigt Einzelvorgänge mit dem Status *Gestartet* an. Zwei gelbe vertikale Linien kennzeichnen Einzelvorgänge mit dem Status *Gestoppt*.
1. **Spalte mit hoher Priorität** – In dieser Spalte werden Ausrufezeichen verwendet, um Einzelvorgänge mit hoher Priorität anzuzeigen.
1. **Bestellung** – In dieser Spalte wird die Produktionsauftragsnummer für einen Auftrag angezeigt.
1. **Beschreibung** – Diese Spalte enthält eine Beschreibung des Vorgangs, zu der ein Job gehört.
1. **Angefordert** – Diese Spalte zeigt die Menge, die ein Einzelauftrag produzieren soll.
1. **Gestartet** – Diese Spalte zeigt die Menge, die bereits für einen Einzelvorgang gestartet wurde.
1. **Abgeschlossen** – Diese Spalte zeigt die Menge, die bereits für einen Einzelvorgang abgeschlossen wurde.
1. **Verschrottet** – Diese Spalte zeigt die Menge, die bereits für einen Einzelvorgang verschrottet wurde.
1. **Verbleibend** – In dieser Spalte wird die Menge angezeigt, die für einen Einzelvorgang noch zu erledigen ist.

## <a name="active-jobs-tab"></a>Registerkarte Aktive Einzelvorgänge

Die Registerkarten **Aktive Aufträge** zeigen eine Liste aller Aufträge an, die die angemeldete Arbeitskraft bereits gestartet hat. (Dieser Registerkartenname ist anpassbar und kann für Ihr System unterschiedlich sein.)

![Registerkarte „Aktive Einzelvorgänge“.](media/pfei-active-jobs-tab.png "Registerkarte Aktive Einzelvorgänge")

Die Liste der aktiven Aufträge enthält die folgenden Spalten:

- **Auswahlspalte** – In der Spalte ganz links werden Häkchen verwendet, um Jobs anzuzeigen, die vom Mitarbeiter ausgewählt wurden. Arbeitskräfte können mehrere Einzelaufträge gleichzeitig in der Liste auswählen. Um alle Einzelaufträge in der Liste auszuwählen, aktivieren Sie das Häkchen in der Spaltenüberschrift. Wenn ein einzelner Einzelvorgang ausgewählt wird, werden Details zu diesem Einzelvorgang im unteren Teil der Seite angezeigt.
- **Bestellung** – In dieser Spalte wird die Produktionsauftragsnummer für einen Auftrag angezeigt.
- **Beschreibung** – Diese Spalte enthält eine Beschreibung des Vorgangs, zu der ein Job gehört.
- **Angefordert** – Diese Spalte zeigt die Menge, die ein Einzelauftrag produzieren soll.
- **Gestartet** – Diese Spalte zeigt die Menge, die bereits für einen Einzelvorgang gestartet wurde.
- **Abgeschlossen** – Diese Spalte zeigt die Menge, die bereits für einen Einzelvorgang abgeschlossen wurde.
- **Verschrottet** – Diese Spalte zeigt die Menge, die bereits für einen Einzelvorgang verschrottet wurde.
- **Verbleibend** – In dieser Spalte wird die Menge angezeigt, die für einen Einzelvorgang noch zu erledigen ist.

## <a name="my-jobs-tab"></a>Registerkarte Meine Aufträge

Auf der Registerkarte **Meine Aufträge** können Arbeitskräfte ganz einfach alle nicht gestarteten und nicht beendeten Aufträge einsehen, die ihnen speziell zugewiesen sind. Es ist nützlich in Unternehmen, in denen Aufträge manchmal oder immer bestimmten Arbeitskräften (Human Resources) statt anderen Arten von Ressourcen (z.B. Maschinen) zugewiesen werden.

Das Planungssystem ordnet jeden Produktionsauftrag automatisch einem bestimmten Datensatz zu, und jeder Ressourcendatensatz hat einen Typ (z.B. Maschine oder Mensch). Wenn Sie einen Mitarbeiter als Arbeitskraft in der Produktion festlegen, können Sie das Konto des Mitarbeiters mit einem eindeutigen Datensatz der Humanressourcen verknüpfen.

Die Registerkarte **Meine Aufträge** listet alle nicht gestarteten und nicht beendeten Aufträge auf, die dem Datensatz der angemeldeten Arbeitskraft zugewiesen wurden, sofern eine Arbeitskraft angemeldet ist. Es listet niemals Aufträge auf, die einer Maschine oder einer anderen Art von Ressource zugewiesen wurden, selbst wenn die angemeldete Arbeitskraft mit der Arbeit an diesen Aufträgen begonnen hat.

Um alle Aufträge anzuzeigen, die von der angemeldeten Arbeitskraft gestartet wurden, unabhängig von der Art der Ressource, der der jeweilige Auftrag zugewiesen ist, verwenden Sie die Registerkarte **Aktive Aufträge**. Um alle nicht beendeten Aufträge anzuzeigen, die der Konfiguration des lokalen Auftragsfilters entsprechen, unabhängig von der Arbeitskraft oder dem Startstatus, verwenden Sie die Registerkarte **Alle Aufträge**.

![Registerkarte „Meine Aufträge“](media/pfei-my-jobs-tab.png "Registerkarte Meine Aufträge")

## <a name="my-machine-tab"></a>Registerkarte „Meine Maschine“

Auf der Registerkarte **Meine Maschine** können Arbeitskräfte eine Anlage auswählen, die mit einer Maschinenressource innerhalb des auf der Registerkarte **Alle Aufträge** festgelegten Filters liegt. Die Arbeitskraft kann dann den Status und den Zustand der ausgewählten Anlage anzeigen, indem sie Werte für bis zu vier ausgewählte Zähler und Listen der letzten Wartungsanfragen und registrierten Ausfallzeiten abliest. Die Arbeitskraft kann auch eine Wartung für die ausgewählte Anlage anfordern und Ausfallzeiten der Maschine registrieren und bearbeiten. (Dieser Registerkartenname ist anpassbar und kann für Ihr System unterschiedlich sein.)

![Die Registerkarte „Meine Maschine“.](media/pfei-my-machine-tab.png "Die Registerkarte „Meine Maschine“")

Die Registerkarte **Meine Maschine** enthält die folgenden Spalten. Die Nummern entsprechen den Nummern in der vorherigen Abbildung.

1. **Maschinenanlage** – Wählen Sie die Maschinenanlage aus, die Sie nachverfolgen möchten. Geben Sie einen Namen ein, um aus einer Liste übereinstimmender Anlagen auszuwählen, oder wählen Sie das Lupensymbol aus, um aus einer Liste aller Anlagen auszuwählen, die den Ressourcen zugeordnet sind, die sich im Filter der Auftragsliste befinden.

    > [!NOTE]
    > Benutzer von Supply Chain Management können jeder Anlage über die Seite **Alle Anlagen** (auf der Registerkarte **Anlage** über die Dropdownliste **Ressource**) nach Bedarf eine Ressource zuweisen. Weitere Informationen finden Sie unter [Erstellen einer Anlage](../asset-management/objects/create-an-object.md).

1. **Einstellungen** – Wählen Sie das Zahnradsymbol aus, um ein Dialogfeld zu öffnen, in dem Sie auswählen können, welche Zähler für die ausgewählte Maschinenanlage angezeigt werden sollen. Die Werte für diese Zähler werden oben auf der Registerkarte **Anlagenverwaltung** angezeigt. Über das Menü **Einstellungen** (siehe den folgenden Screenshot) können Sie bis zu vier Zähler aktivieren. Verwenden Sie für jeden Zähler, den Sie aktivieren möchten, das Suchfeld oben auf der Kachel, um einen Zähler auszuwählen. Das Suchfeld listet alle Zähler auf, die der oben auf der Seite **Vermögensverwaltung** ausgewählten Anlage zugeordnet sind. Stellen Sie jeden Zähler so ein, dass für den Zähler entweder der Wert **Aggregiert** oder der aktuelle Wert **Tatsächlich** überwacht wird. Wenn Sie beispielsweise einen Zähler festlegen, der nachverfolgt, wie viele Stunden die Maschine gelaufen ist, sollten Sie ihn auf **Aggregiert** festlegen. Wenn Sie einen Zähler zum Messen der zuletzt aktualisierten Temperatur oder des zuletzt aktualisierten Drucks verwenden, sollten Sie ihn auf **Tatsächlich** festlegen. Wählen Sie **OK**, um Ihre Einstellungen zu speichern und das Dialogfeld zu schließen.

    ![Einstellungen der Registerkarte „Meine Maschine“.](media/pfei-my-machine-tab-settings.png "Einstellungen der Registerkarte „Meine Maschine“")

1. **Wartung anfordern** – Wählen Sie diese Schaltfläche aus, um ein Dialogfeld zu öffnen, in dem Sie eine Wartungsanfrage erstellen können. Sie können eine Beschreibung und eine Notiz angeben. Die Anfrage wird an einen Benutzer von Supply Chain Management weitergeleitet, der dann in der Lage ist, die Wartungsanfrage in einen Wartungsarbeitsauftrag umzuwandeln.
1. **Ausfallzeiten erfassen** – Wählen Sie diese Schaltfläche aus, um ein Dialogfeld zu öffnen, in dem Sie Ausfallzeiten der Maschine erfassen können. Sie können einen Ursachencode auswählen und ein Datum bzw. eine Zeitspanne für die Ausfallzeit eingeben. Die Erfassung der Ausfallzeit der Maschine wird zur Berechnung der Effizienz des Maschinenanlage verwendet.
1. **Anzeigen oder bearbeiten** – Wählen Sie diese Schaltfläche aus, um ein Dialogfeld zu öffnen, in dem Sie vorhandene Ausfallzeitdatensätze bearbeiten oder anzeigen können.

## <a name="starting-and-completing-production-jobs"></a>Einzelvorgänge starten und abschließen

Arbeiter starten einen Produktions-Einzelvorgang, indem sie einen Einzelvorgang auf der Registerkarte **Alle Einzelvorgänge** auswählen und dann **Einzelvorgang starten** wählen und das Dialogfeld **Einzelvorgang starten** öffnen.

![Dialogfeld Einzelvorgang starten.](media/pfei-start-job-dialog.png "Dialogfeld Einzelvorgang starten")

Arbeitskräfte benutzen das Dialogfeld **Einzelvorgang starten**, um die Produktionsmenge zu bestätigen und dann den Einzelvorgang zu starten. Arbeitskräfte können die Menge anpassen, indem sie das Feld **Menge** auswählen und dann die numerische Tastatur verwenden, die angezeigt wird. Arbeitskräfte wählen **Start**, um mit dem Einzelvorgang zu beginnen. Das Dialogfeld **Einzelvorgang starten** wird geschlossen und der Einzelvorgang zur Registerkarte **Aktive Einzelvorgänge** hinzugefügt.

Arbeitskräfte können einen Einzelvorgang starten, der sich in einem beliebigen Status befindet. Wenn ein Mitarbeiter einen Einzelvorgang mit dem Status beginnt *Nicht angefangen*, zeigt das Feld **Menge** im Dialogfeld **Einzelvorgang starten** zunächst die volle Menge an. Wenn eine Arbeitskraft einen Einzelvorgang mit dem Status beginnt *Gestartet* oder *Gestoppt* zeigt das Feld **Menge** zunächst die verbleibende Menge an.

## <a name="reporting-good-quantities"></a>Gute Mengen melden

Wenn ein Mitarbeiter einen Einzelvorgang abschließt oder teilweise abschließt, kann er gute Mengen melden, die durch Auswahl eines Einzelauftrages auf der Registerkarte **Aktive Einzelvorgänge** ausgewählt werden und dann **Fortschritt melden** auswählen. Im Dialogfeld **Fortschritt melden** gibt die Arbeitskraft dann die gute Menge über die Zifferntastatur ein. Die Menge ist standardmäßig leer. Nachdem eine Menge eingegeben wurde, kann die Arbeitskraft den Status des Einzelvorgangs auf *In Bearbeitung*, *Gestoppt*, oder *Abgeschlossen* aktualisieren.

![Dialogfeld „Fortschritt melden“.](media/pfei-report-progress-dialog.png "Dialogfeld Fortschritt melden")

## <a name="reporting-good-quantities-on-batch-orders-that-have-co-products-and-by-products"></a>Melden von Gutmengen bei Chargenaufträgen mit Kuppel- und Nebenprodukten

Mitarbeiter können die Ausführungsschnittstelle der Produktionshalle verwenden, um den Fortschritt von Batchaufträgen zu melden. Diese Berichte umfassen Kuppel- und Nebenprodukten.

Einige Hersteller, insbesondere in der Prozessindustrie, verwenden Chargenaufträge, um ihre Produktionsprozesse zu verwalten. Chargenaufträge werden aus Formeln erstellt, und diese Formeln können so definiert werden, dass sie Kuppel- und Nebenprodukte als Ausgabe haben. Wenn Rückmeldungen zu diesen Chargenaufträgen gemeldet werden, muss die Produktionsmenge sowohl auf der Formelposition als auch auf den Kuppel- und Nebenprodukten registriert werden.

Wenn eine Arbeitskraft einen Auftrag in einem Chargenauftrag abschließt oder teilweise abschließt, kann sie Gut- oder Ausschussmengen für jedes Produkt melden, das als Output für den Auftrag definiert ist. Produkte, die als Output für einen Chargenauftrag definiert sind, können folgende sein: *Formel*, *Kuppelprodukt*, oder *Nebenprodukt* Typ.

Um gute Mengen an den Produkten zu melden, wählt ein Arbeiter einen Job auf der Registerkarte **Aktive Jobs** und wählt dann **Fortschritt melden**.

Im Dialogfenster **Fortschritt melden** kann die Arbeitskraft dann unter den Produkten auswählen, die als Ausgabe für den Chargenauftrag definiert sind, über die er berichten soll. Der Arbeiter kann ein oder mehrere Produkte in der Liste auswählen und dann **Fortschritt melden** auswählen. Für jedes Produkt ist die Menge standardmäßig leer, und der Arbeiter kann die numerische Tastatur verwenden, um die Menge einzugeben. Der Arbeiter kann die Schaltflächen **Vorherige** und **Nächste** auswählen, um zwischen den ausgewählten Produkten zu wechseln. Nachdem die Menge für jedes Produkt eingegeben wurde, kann die Arbeitskraft den Status des Einzelvorgangs auf *In Bearbeitung*, *Gestoppt*, oder *Abgeschlossen* aktualisieren.

![Kuppel- und Nebenprodukte melden.](media/report-co-by-products.png "Kuppel- und Nebenprodukte melden")

### <a name="reporting-on-batch-orders-for-planning-items"></a>Berichte zu Chargenaufträgen für Planungsartikel

Wenn eine Arbeitskraft einen Auftrag für einen Chargenauftrag für einen Planungsartikel abschließt, meldet sie Mengen nur für Kuppel- und Nebenprodukte, da Planungsartikel keinen Artikel der *Formel* Typ.

### <a name="reporting-co-product-variation"></a>Kuppelproduktvariation melden

Wenn ein Chargenauftrag aus einer Formelversion erstellt wird, in der die Option **Kuppelproduktvarianten** auf *Ja* eingestellt ist, kann die Arbeitskraft Kuppelprodukte melden, die nicht Teil der Definition für die Chargenaufträge sind. Diese Funktionalität wird in Szenarien verwendet, in denen unerwartete Produktausgaben im Produktionsprozess auftreten können.

In diesem Fall kann die Arbeitskraft das Kuppelprodukt und die zu meldende Menge angeben, indem sie **Kuppelproduktvarianten** im Dialogfeld Berichtsfortschritt auswählt. Die Arbeitskraft kann dann aus allen freigegebenen Produkten auswählen, die als Kuppelprodukte definiert sind.

### <a name="reporting-catch-weight-items"></a>Bericht Artikelgewicht

Arbeitskräfte können die Produktionsausführungsoberfläche verwenden, um über den Fortschritt von Batch-Aufträgen zu berichten, die für Artikel mit Catch-Gewicht erstellt wurden. Batch-Aufträge werden aus Formeln erstellt, die so definiert werden können, dass Artikelgewichte als Formelpositionen, Kuppelprodukte und Nebenprodukte enthalten sind. Eine Formel kann auch so definiert werden, dass sie Formelzeilen für Zutaten enthält, die für das Artikelgewicht definiert sind. Artikel mit Artikelgewicht verwenden zwei Maßeinheiten, um den Bestand zu verfolgen: die Menge des Artikelgewichts und die Menge des Bestands. In der Lebensmittelbranche kann z.B. verpacktes Fleisch als Element mit Artikelgewicht definiert werden, wobei die Menge des Artikelgewichts zur Erfassung der Anzahl der Kartons und die Bestandsmenge zur Erfassung des Gewichts der Kartons verwendet wird.

## <a name="reporting-scrap"></a>Schrott melden

Wenn ein Mitarbeiter einen Einzelvorgang abschließt oder teilweise abschließt, kann er Schrott melden, indem er den Einzelvorgang auf der Registerkarte **Aktive Einzelvorgänge** auswählt und dann **Schrott melden** auswählt. Im Dialogfeld **Schrott melden** gibt die Arbeitskraft dann die Schrottmengen über die Zifferntastatur ein. Die Arbeitskraft wählt auch einen Grund aus (*Keiner*, *Maschine*, *Operator*, oder *Material*).

![Dialogfeld „Ausschuss melden“.](media/pfei-report-scrap-dialog.png "Dialogfeld Schrott melden")

## <a name="adjust-material-consumption-and-make-material-reservations"></a>Materialverbrauch anpassen und Materialreservierungen vornehmen

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: preview until further notice -->

Arbeitskräfte können den Materialverbrauch für jeden Produktionsauftrag anpassen. Diese Funktion wird in Szenarien verwendet, in denen die tatsächliche Menge an Materialien, die durch einen Produktionsauftrag verbraucht wurde, mehr oder weniger als die geplante Menge war. Daher muss sie angepasst werden, um die Bestände aktuell zu halten.

Arbeitskräfte können auch Reservierungen für die Batch- und Seriennummern von Materialien vornehmen. Diese Funktion wird in Szenarien verwendet, in denen eine Arbeitskraft manuell angeben muss, welche Batches oder Seriennummern verbraucht wurden, um die Anforderungen an die Rückverfolgbarkeit von Materialien zu erfüllen.

Arbeitskräfte können die anzupassende Menge angeben, indem sie **Material anpassen** wählen. Diese Schaltfläche ist an den folgenden Stellen verfügbar:

- In der Dialogbox **Ausschuss melden**
- Im Dialogfeld **Fortschritt des Berichts**
- In der Symbolleiste auf der rechten Seite

### <a name="adjust-material-consumption-from-the-report-scrap-and-report-progress-dialog-boxes"></a>Passen Sie den Materialverbrauch über die Dialogfelder Bericht Ausschuss und Bericht Fortschritt an

Nachdem eine Arbeitskraft die zu meldende Menge in das Dialogfeld **Fortschritt melden** oder **Ausschuss melden** eingegeben hat, wird die Schaltfläche **Material anpassen** verfügbar. Wenn der Benutzer diese Schaltfläche auswählt, erscheint das Dialogfeld **Material anpassen**. In diesem Dialogfeld werden die Artikel aufgelistet, die verbraucht werden sollen, wenn die Waren- oder Verschrottungsmenge für den Auftrag gemeldet wird.

Die Liste im Dialogfenster zeigt die folgenden Informationen an:

- **Produktnummer** - Der Produktstamm und die Produktvariante.
- **Produktname** - Der Name des Produkts.
- **Vorschlag** - Die geschätzte Materialmenge, die verbraucht wird, wenn für die angegebene Menge für den Auftrag Fortschritt oder Ausschuss gemeldet wird.
- **Verbrauch** - Die tatsächliche Menge an Material, die bei der Meldung von Fortschritt oder Ausschuss für die angegebene Menge für den Auftrag verbraucht wird.
- **Reserviert** - Die Menge des Materials, die im Bestand physisch reserviert wurde.
- **Einheit** - Die Einheit der Stückliste (Stückliste).

Auf der rechten Seite des Dialogfelds werden die folgenden Informationen angezeigt:

- **Produktnummer** - Der Produktstamm und die Produktvariante.
- **Geschätzt** - Die geschätzte zu verbrauchende Menge.
- **Gestartet** - Die Menge, die mit dem Produktionsauftrag gestartet wurde.
- **Restmenge** - Von der geschätzten Menge die Menge, die noch verbraucht werden muss.
- **Abgegebene Menge** - Die Menge, die verbraucht wurde.

Die folgenden Aktionen können durchgeführt werden:

- Die Arbeitskraft kann die Menge angeben, die für ein Material angepasst werden soll, indem sie **Verbrauch anpassen** wählt. Nachdem die Menge bestätigt wurde, wird die Menge in der Spalte **Verbrauch** mit der angepassten Menge aktualisiert.
- Wenn die Arbeitskraft **Material anpassen** auswählt, wird ein Produktions-Kommissionierlisten-Journal erstellt. Diese Erfassung enthält die gleichen Artikel und Mengen wie die Liste **Material anpassen**.
- Wenn die Arbeitskraft eine Menge in der Dialogbox **Material anpassen** anpasst, wird das Feld **Vorschlag** in der entsprechenden Buchungsblattzeile mit derselben Menge aktualisiert. Wenn die Arbeitskraft im Dialogfeld **Material anpassen** **Abbrechen** auswählt, wird die Kommissionierliste gelöscht.
- Wenn die Arbeitskraft **OK** wählt, wird die Kommissionierliste nicht gelöscht. Es wird gepostet, wenn der Auftrag im Dialogfeld **Ausschuss melden** oder **Fortschritt melden** gemeldet wird.
- Wenn die Arbeitskraft **Abbrechen** in der Dialogbox **Fortschrittsbericht** oder **Ausschussbericht** wählt, wird die Kommissionierliste gelöscht.

### <a name="adjust-material-from-the-primary-or-secondary-toolbar"></a>Material über die primäre oder sekundäre Symbolleiste anpassen

Die Schaltfläche **Material anpassen** kann so konfiguriert werden, dass sie in der primären oder sekundären Symbolleiste erscheint. (Weitere Informationen finden Sie unter [Design der Produktionsausführungsoberfläche](production-floor-execution-tabs.md).) Eine Arbeitskraft kann **Material anpassen** für einen laufenden Produktionsauftrag auswählen. In diesem Fall erscheint das Dialogfenster **Material anpassen**, in dem die Arbeitskraft die gewünschten Anpassungen vornehmen kann. Wenn das Dialogfenster geöffnet wird, wird für den Produktionsauftrag eine Kommissionierliste erstellt, die Zeilen für die angepassten Mengen enthält. Wählt die Arbeitskraft **Jetzt buchen**, wird die Anpassung bestätigt und die Kommissionierliste wird gebucht. Wenn die Arbeitskraft **Abbrechen** wählt, wird die Kommissionierliste gelöscht und keine Anpassung vorgenommen.

### <a name="adjust-material-consumption-for-catch-weight-items"></a>Anpassung des Materialverbrauchs für Artikel mit Artikelgewicht

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: preview until further notice -->

Arbeitskräfte können den Materialverbrauch für Artikel mit Artikelgewicht anpassen. Diese Funktionalität wird in Szenarien verwendet, in denen die tatsächliche Menge eines Materials mit Artikelgewicht, die von einem Produktionsauftrag verbraucht wurde, mehr oder weniger als die geplante Menge war. Daher muss sie angepasst werden, um die Bestände aktuell zu halten. Wenn eine Arbeitskraft den Verbrauch eines Elements mit Artikelgewicht anpasst, kann sie sowohl die Menge des Artikelgewichts als auch die Menge des Bestands anpassen. Wenn beispielsweise ein Produktionsauftrag fünf Kartons mit einem geschätzten Gewicht von 2 Kilogramm pro Karton verbrauchen soll, kann die Arbeitskraft sowohl die Anzahl der zu verbrauchenden Kartons als auch das Gewicht der Kartons anpassen. Das System prüft, ob das angegebene Gewicht der Kisten innerhalb der für das freigegebene Produkt definierten Mindest- und Höchstwerte liegt.

### <a name="reserve-materials"></a>Materialien reservieren

In der Dialogbox **Material anpassen** kann eine Arbeitskraft Materialreservierungen vornehmen und anpassen, indem sie **Material reservieren** wählt. Das angezeigte Dialogfenster **Reservematerial** zeigt den physisch verfügbaren Bestand für den Artikel für jede Lager- und Tracking-Dimension an.

Wenn das Material für Lagerverwaltungsprozesse (WMS) aktiviert ist, zeigt die Liste nur den physisch verfügbaren Bestand für den Produktionseingangsort des Materials an. Der Ort der Produktionseingabe wird auf der Ressource definiert, auf der der Produktionsauftrag geplant ist. Wenn die Artikelnummer über eine Batch- oder Seriennummer gesteuert wird, wird die vollständige Liste der physisch verfügbaren Batch- und Seriennummern angezeigt. Um eine zu reservierende Menge anzugeben, kann die Arbeitskraft **Material reservieren** wählen. Um eine bestehende Reservierung zu entfernen, kann die Arbeitskraft **Reservierung entfernen** wählen.

Weitere Informationen darüber, wie Sie den Ort der Produktionseingabe festlegen, finden Sie in dem folgenden Blog-Beitrag: [Einrichten des Produktions-Eingabeortes](/archive/blogs/axmfg/deliver-picked-materials-to-the-locations-where-the-materials-are-consumed-by-operations-in-production).

> [!NOTE]
> Reservierungen, die eine Arbeitskraft im Dialogfeld **Material reservieren** vornimmt, bleiben bestehen, wenn die Arbeitskraft im Dialogfeld **Fortschritt melden** oder **Ausschuss melden** die Option **Stornieren** wählt.
>
> Es ist nicht möglich, Reservierungen für Elemente mit Artikelgewicht anzupassen.

## <a name="completing-a-job-and-starting-a-new-job"></a>Einen Einzelvorgang abschließen und einen neuen Einzelvorgang beginnen

Normalerweise schließen Arbeitskräfte einen Einzelvorgang ab, indem sie einen oder mehrere aktuelle Einzelvorgänge auf der Registerkarte **Aktive Einzelvorgänge** auswählen und dann **Fortschritt melden** wählen. Sie geben dann die produzierte Menge (die gute Menge) ein und setzen den Status auf *Komplett*. Wenn mehr als ein Einzelvorgang ausgewählt wurde, verwendet ein Mitarbeiter die Schaltflächen **Zurück** und **Weiter**, um zwischen ihnen zu navigieren. Um einen neuen Einzelvorgang zu starten, wählt die Arbeitskraft auf der Registerkarte **Alle Einzelvorgänge** und wählt dann **Einzelvorgang starten**.

Eine Arbeitskraft kann auch einen neuen Einzelvorgang beginnen, während sein vorheriger Einzelvorgang noch offen ist. Um einen neuen Einzelvorgang zu starten, wählt die Arbeitskraft auf der Registerkarte erneut **Alle Einzelvorgänge** und wählt dann **Einzelvorgang starten**. In diesem Fall informiert das Dialogfeld **Einzelvorgang starten** die Arbeitskraft darüber, dass sie gerade an einem Einzelvorgang arbeitet und dass sie diesen Einzelvorgang daher entweder beenden oder abschließen muss, bevor sie den neuen Einzelvorgang startet.

## <a name="working-on-multiple-jobs-in-parallel"></a>Paralleles Arbeiten an mehreren Einzelvorgängen

Eine Arbeitskraft kann gleichzeitig an mehreren Einzelvorgängen arbeiten (d.h. parallel). In diesem Fall wird die Sammlung von Einzelvorgängen, an denen denen die Arbeitskraft arbeitet, als ein *Einzelvorgang-Bündel* bezeichnet. Die Arbeitskraft kann dem Bündel neue Einzelvorgänge hinzufügen oder einen oder mehreren Einzelvorgang im Bündel abschließen. Die folgenden beiden Szenarien zeigen, wie eine Arbeitskraft parallel an Einzelvorgängen arbeiten kann.

### <a name="scenario-1-a-worker-who-has-no-active-jobs-wants-to-start-two-jobs-and-work-on-them-in-parallel"></a>Szenario 1: Eine Arbeitskraft, die keine aktiven Einzelvorgänge hat, möchte zwei Einzelvorgänge starten und parallel daran arbeiten

Die Arbeitskraft wählt auf der Registerkarte **Alle Einzelvorgänge** die zwei Einzelvorgänge und wählt dann **Einzelvorgang starten**. Das Dialogfeld **Einzelvorgang starten** zeigt beide ausgewählten Einzelvorgänge an, und die Arbeitskraft kann die Anzahl anpassen, die für jeden Einzelvorgang gestartet werden soll. Die Arbeitskraft bestätigt dann das Dialogfeld und kann beide Einzelvorgänge starten.

### <a name="scenario-2-a-worker-who-has-two-active-jobs-that-are-in-progress-wants-to-start-a-third-job-and-work-on-it-in-parallel-with-the-other-two"></a>Szenario 2: Eine Arbeitskraft mit zwei aktiven Einzelvorgängen, die gerade ausgeführt werden, möchte einen dritten Einzelvorgang starten und parallel zu den beiden anderen daran arbeiten

Die Arbeitskraft wählt auf der Registerkarte **Alle Einzelvorgänge** den dritten Einzelvorgang aus und wählt dann **Bündel**. In dem Dialogfeld **Bündel** kann die Arbeitskraft die zu startende Menge anpassen. Die Arbeitskraft bestätigt dann das Dialogfeld durch Auswahl von **Bündel**.

## <a name="working-on-indirect-activities"></a>Arbeiten an indirekten Aktivitäten

Indirekte Aktivitäten sind Aktivitäten, die nicht direkt mit einem Produktionsauftrag zusammenhängen. Indirekte Aktivitäten können flexibel definiert werden, wie beschrieben unter [Richten Sie indirekte Aktivitäten für Zeit und Anwesenheit ein](/dynamicsax-2012/appuser-itpro/set-up-indirect-activities-for-time-and-attendance).

Zum Beispiel möchte Shannon, eine Werkstatt-Arbeitskraft bei Contoso, an einer Firmenbesprechung teilnehmen, und Besprechungen werden als indirekte Aktivität betrachtet. Es gilt eines der folgenden beiden Szenarien:

- **Shannon arbeitet an einem oder mehreren aktiven Einzelvorgängen.** Shannon wählt **Aktivität** aus, identifiziert die Aktivität (Besprechung) und bestätigt ihre Auswahl. Eine Meldung informiert sie darüber, dass sie gerade laufende Einzelvorgänge hat. In der Nachricht kann Shannon auswählen, ob die Einzelvorgänge, an denen sie arbeitet, abgeschlossen oder gestoppt werden sollen, bevor sie zur Besprechung geht.
- **Shannon hat keine aktiven Einzelvorgänge.** Shannon wählt **Aktivität** aus, identifiziert die Aktivität (Besprechung) und bestätigt ihre Auswahl. Sie ist jetzt als Teilnehmerin der Besprechung registriert.

In beiden Szenarien wechselt Shannon, nachdem sie ihre Auswahl bestätigt hat, entweder zur Anmeldeseite oder zu einer Seite, die darauf wartet, dass sie bestätigt, dass sie von ihrer indirekten Aktivität zurückgekehrt ist. Die angezeigte Seite hängt von der Konfiguration der Produktionsausführungsoberfläche ab. (Weitere Informationen finden Sie unter [Einrichten der Produktionsausführungsoberfläche](production-floor-execution-configure.md).)

## <a name="registering-breaks"></a>Erfassen von Pausen

Arbeitskräfte können Pausen registrieren. Pausen können flexibel definiert werden, wie beschrieben in [Lohn auf Basis von Erfassungen](pay-based-on-registrations.md).

Eine Arbeitskraft erfasst eine Pause, indem er **Pause** auswählt und dann die Karte auswählt, die den Pausentyp darstellt (z. B. Mittagessen). Nachdem die Arbeitskraft die Auswahl bestätigt hat, zeigt das Gerät entweder die Anmeldeseite oder eine Seite an, die darauf wartet, dass die Arbeitskraft bestätigt, dass er von der Pause zurückgekehrt ist. Die angezeigte Seite hängt von der Konfiguration der Produktionsausführungsoberfläche ab. (Weitere Informationen finden Sie unter [Einrichten der Produktionsausführungsoberfläche](production-floor-execution-configure.md).)

## <a name="view-the-my-day-dialog"></a>Dialogfeld „Mein Tag“ anzeigen

Das Dialogfeld **Mein Tag** gibt Arbeitskräften einen Überblick über ihre Registrierungen und Salden. Der Dialog ist in die folgenden drei Abschnitte unterteilt:

- Der Hauptbereich listet die Registrierungen auf, die die aktuelle Arbeitskraft an einem ausgewählten Datum vorgenommen hat. Er zeigt beim Öffnen die Registrierungen für den aktuellen Tag an. Außerdem bietet er eine Datumsauswahl, mit der die Arbeitskraft andere Tage anzeigen kann.
- Der Abschnitt **Zuletzt berechneter Tagessaldo** zeigt die aktuellen Salden der Arbeitskraft für entlohnte Zeit, entlohnte Überstunden, Abwesenheit und entlohnte Abwesenheit. Diese Werte basieren auf den Registrierungen, die während des Genehmigungsverfahrens berechnet wurden.
- Der Abschnitt **Salden** bietet einen Überblick über die Salden innerhalb eines definierten Zeitraums für ausgewählte Registrierungskategorien (z. B. Urlaub, Standardzeit und Überstunden). Diese Salden basieren auf der Art und Weise, wie statistische Salden im Modul **Zeit und Anwesenheit** erstellt werden. Weitere Informationen zum Einrichten finden Sie unter [Urlaubssalden in der Produktionsausführungsoberfläche anzeigen](production-floor-execution-payroll-stats.md).

Administratoren können diese Funktion zur Benutzeroberfläche hinzufügen, indem sie die Schaltfläche **Mein Tag** auf einer Symbolleiste für jede relevante Registerkarte platzieren, wie beschrieben in [Produktionsausführungsoberfläche entwerfen](production-floor-execution-tabs.md).

## <a name="working-in-teams"></a>In Teams arbeiten

Wenn mehrere Arbeitskräfte demselben Produktions-Einzelvorgang zugewiesen werden, können sie ein Team bilden. Das Team kann einen Mitarbeiter als Pilot ernennen. Die verbleibenden Arbeitskräfte werden dann automatisch zu Assistenten dieses Piloten. Für das resultierende Team muss nur der Pilot den Einzelvorgangstatus registrieren. Zeiterfassungen gelten für alle Teammitglieder.

### <a name="prerequisites"></a>Voraussetzungen

Um Teams zu verwenden, muss ein Administrator die Aktion **Assistent** für die primäre Symbolleiste auf der Registerkarte **Alle Einzelvorgänge** der Produktionsausführungsoberfläche aktivieren. Anweisungen finden Sie unter [Produktionsausführungsoberfläche entwerfen](production-floor-execution-tabs.md).

### <a name="form-a-new-team-that-has-a-pilot-and-an-assistant"></a>Ein neues Team mit einem Piloten und einem Assistenten bilden

Eine Arbeitskraft kann sich als Assistent registrieren, indem sie **Assistent** in der Registerkarte **Alle Einzelvorgänge** auswählt. Dann kann die Arbeitskraft im angezeigten Dialogfeld **Mitarbeiter zur Unterstützung auswählen** einen Piloten aus einer Liste von Arbeitskräften auswählen, die aktiv an einem Auftrag arbeiten. Nachdem die Arbeitskraft ihre Auswahl bestätigt hat, wird sie zum Assistenten der ausgewählten Arbeitskraft, die zum Piloten für das neue Team wird.

### <a name="assign-a-new-pilot-to-an-existing-team"></a>Neuen Piloten zu einem vorhandenen Team zuweisen

Wenn ein Team einen neuen Piloten auswählen möchte, muss der aktuelle Pilot eine andere Arbeitskraft im Team als neuen Piloten ernennen. Um einen neuen Piloten zu nominieren, wählt der aktuelle Pilot **Assistent** auf der Registerkarte **Alle Einzelvorgänge** aus. Im angezeigten Dialogfeld **Pilot wechseln** kann der Pilot nun einen neuen Piloten aus einer Liste von Arbeitskräften auswählen, die bereits im Team sind. Nachdem der aktuelle Pilot seine Auswahl bestätigt hat, wird er vollständig aus dem Team gestrichen. Er kann dem Team jedoch bei Bedarf wieder beitreten.

### <a name="assistant-clocks-out"></a>Assistent stempelt aus

Wenn eine Arbeitskraft, die als Assistent arbeitet, ausstempelt, verlässt sie das Team. Wenn die Optionen **Permanente Teams** und **Beim Einstempeln erneut starten** auf *Ja* eingestellt sind, wird eine Arbeitskraft, die sich ausstempelt, automatisch wieder dem Team beitreten, wenn sie sich das nächste Mal einstempelt. Sie finden diese Optionen auf der Registerkarte **Allgemein** der Seite **Zeit‑ und Anwesenheitsparameter**.

## <a name="opening-instructions"></a>Anweisungen zum Öffnen

Arbeitskräfte können ein Dokument öffnen, das an einen Einzelvorgang angehängt ist, indem sie **Anleitung** auswählen. Die Schaltfläche **Anleitung** ist nur verfügbar, wenn ein Dokument dem Einzelvorgang in den Stammdaten zugeordnet ist. Zum Beispiel ein Dokument, das an ein Produkt auf der Seite **Freigegebene Produkte** in Supply Chain Management angehängt ist, kann von Arbeitskräften in der Produktionsausführungsoberfläche geöffnet werden.

## <a name="opening-mixed-reality-guides-for-hololens"></a>Öffnen von Mixed Reality-Anleitungen für HoloLens

[Dynamics 365 Guides](https://dynamics.microsoft.com/mixed-reality/guides/) kann dazu beitragen, die Arbeitskräfte zu befähigen, indem praktisches Lernen unter Verwendung von Mixed Reality angeboten wird. Sie können standardisierte Prozesse mit schrittweisen Anweisungen definieren, die Ihre Arbeitskräfte zu den benötigten Werkzeugen und Teilen führen und den Arbeitskräften zeigen, wie sie diese Werkzeuge in realen Arbeitssituationen einsetzen können. Hier ein Überblick über den Prozess.

1. Immer, wenn eine Arbeitskraft eine Einzelvorgangsliste auf der Produktionsausführungsoberfläche öffnet, zeigt die Schnittstelle alle relevanten Anleitungen für die angezeigten Einzelvorgänge an.
1. Die Arbeitskraft wählt **Anleitungen**, um die Liste der Anleitungen anzuzeigen.
1. Die Arbeitskraft wählt einen relevanten Leitfaden in der Liste aus.
1. Die Produktionsausführungsoberfläche zeigt einen QR-Code für die ausgewählte Anleitung an.
1. Die Arbeitskraft nimmt eine HoloLens und wirft einen Blick auf den QR-Code, um die Anleitung zu starten.
1. Die Arbeitskraft arbeitet die Anleitung durch, um die Aufgabe zu lernen.

Weitere Informationen zum Erstellen, Zuweisen und Verwenden von Anleitungen für HoloLens, finden Sie unter [Bereitstellung von Mixed Reality-Leitfäden für Arbeitskräfte in der Produktion](instruction-guides-in-production-overview.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
