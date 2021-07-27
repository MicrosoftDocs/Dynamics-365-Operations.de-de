---
title: Verzögern der Ausführung von Sequenz-Elementen in ER-Formaten
description: In diesem Thema wird erläutert, wie die Ausführung eines Sequenz-Elements in einem ER-Format verzögert wird.
author: NickSelin
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-01
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 3a8d4c57ca6b1fee5f4eb1414bfb503470b5e570
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6348090"
---
# <a name="defer-the-execution-of-sequence-elements-in-er-formats"></a>Verzögern der Ausführung von Sequenz-Elementen in ER-Formaten

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Übersicht

Sie können den Arbeitsgangdesigner des Frameworks für [Elektronische Berichterstattung (ER)](general-electronic-reporting.md) für das [Konfigurieren](tasks/er-format-configuration-2016-11.md) der [Formatkomponente](general-electronic-reporting.md#FormatComponentOutbound) einer ER-Lösung verwenden, die zum Generieren ausgehender Dokumente im Textformat-Format verwendet wird. Die hierarchische Struktur der konfigurierten Formatkomponente besteht aus Formatelementen verschiedener Typen. Diese Formatelemente werden verwendet, um generierte Dokumente zur Laufzeit mit den erforderlichen Informationen zu füllen. Wenn Sie ein ER-Format ausführen, werden die Formatelemente standardmäßig in der Reihenfolge ausgeführt, in der sie in der Formathierarchie dargestellt werden: einzeln nacheinander, von oben nach unten. Zur Entwurfszeit können Sie jedoch die Ausführungsreihenfolge für alle Sequenz-Elemente der konfigurierten Formatkomponente ändern.

Durch Aktivieren der Option <a name="DeferredSequenceExecution"></a>**Verzögerte Ausführung** für ein Sequenz-Element im konfigurierten Format können Sie die Ausführung des Elements verzögern (hinausschieben). In diesem Fall wird das Element erst ausgeführt, wenn alle anderen Elemente des übergeordneten Elements ausgeführt wurden.

Weitere Informationen über diese Funktion erhalten Sie, wenn Sie das Beispiel in diesem Thema abschließen.

## <a name="limitations"></a>Einschränkungen

Die Option **Verzögerte Ausführung** wird nur für Sequenz-Elemente unterstützt, die für ein ER-Format konfiguriert sind, das zum Generieren **ausgehender** Dokumente im Textformat verwendet wird.

Die Option **Verzögerte Ausführung** gilt nicht für Sequenzen, die als zugeschnittene Sequenzen konfiguriert wurden und deren maximale Länge begrenzt ist.

## <a name="example-defer-the-execution-of-a-sequence-element-in-an-er-format"></a><a name="Example"></a>Beispiel: Verzögern der Ausführung eines Sequenz-Elements in einem ER-Format

In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Systemadministrator- oder der Funktionaler Berater für elektronische Berichterstellung-[Rolle](../sysadmin/tasks/assign-users-security-roles.md) ein ER-Format konfigurieren kann, das ein Sequenz-Element enthält, dessen Ausführungsreihenfolge von der Reihenfolge in der Formathierarchie abweicht.

Diese Schritte können im **USMF**-Unternehmen in Microsoft Dynamics 365 Finance durchgeführt werden.

### <a name="prerequisites"></a>Voraussetzungen

Um das Beispiel in diesem Thema abzuschließen, müssen Sie für eine der folgenden Rollen Zugriff auf das **USMF**-Unternehmen in Finance haben:

- Funktionaler Berater für elektronische Berichterstellung
- Systemadministrator

Wenn Sie das Beispiel im Thema [Verzögern der Ausführung von XML-Elementen in ER-Formaten](er-defer-xml-element.md#Example) noch nicht abgeschlossen haben, laden Sie die folgenden [Konfigurationen](general-electronic-reporting.md#Configuration) der ER-Beispiellösung herunter.

| Inhaltsbeschreibung            | Dateiname |
|--------------------------------|-----------|
| ER-Datenmodell-Konfiguration    | [Model to learn deferred elements.version.1.xml](https://download.microsoft.com/download/7/6/0/760933ca-4ac3-4f50-bc0c-c35e596ee066/Modeltolearndeferredelements.version.1.xml) |
| Konfiguration der ER-Modellzuordnung | [Mapping to learn deferred elements.version.1.1.xml](https://download.microsoft.com/download/c/9/c/c9c4b9dd-b700-4385-a087-a84ce9fc1d0f/Mappingtolearndeferredelements.version.1.1.xml) |

Bevor Sie beginnen, müssen Sie auch die folgende Konfiguration der ER-Beispiellösung herunterladen und speichern.

| Inhaltsbeschreibung     |Dateiname |
|-------------------------|----------|
| ER-Formatkonfiguration | [Format to learn deferred sequences.version.1.1.xml](https://download.microsoft.com/download/0/f/5/0f55c341-8285-4d92-a46d-475d9a010927/Formattolearndeferredsequences.version.1.1.xml) |

### <a name="import-the-sample-er-configurations"></a>ER-Beispielkonfigurationsdateien importieren

1. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
2. Wählen Sie **Berichterstellungskonfigurationen** aus.
3. Wenn auf der Seite **Konfigurationen** die Konfiguration für **Model zum Erlernen verzögerter Elemente** nicht im Konfigurationsbaum verfügbar ist, importieren Sie die ER-Datenmodellkonfiguration.

    1. Wählen Sie **Austausch** und dann **Aus XML-Datei laden** aus.
    2. Wählen Sie **Durchsuchen** aus, um die Datei **Model to learn deferred elements.1.xml** zu finden und auszuwählen und klicken Sie dann auf **OK**.

4. Wenn die Konfiguration für **Zuordnung zum Verstehen verzögerter Elemente** nicht im Konfigurationsbaum verfügbar ist, importieren Sie die ER-Modellzuordnungskonfiguration:

    1. Wählen Sie **Austausch** und dann **Aus XML-Datei laden** aus.
    2. Wählen Sie **Durchsuchen** aus, um die Datei **Mapping to learn deferred elements.1.1.xml** zu finden und auszuwählen und klicken Sie dann auf **OK**.

5. Import der ER-Formatkonfiguration:

    1. Wählen Sie **Austausch** und dann **Aus XML-Datei laden** aus.
    2. Wählen Sie **Durchsuchen** aus, um die Datei **Format to learn deferred sequences.1.1.xml** zu finden und auszuwählen und klicken Sie dann auf **OK**.

6. Erweitern Sie in der Konfigurationsstruktur **Modell zum Erlernen verzögerter Elemente**.
7. Überprüfen Sie die Liste der importierten ER-Konfigurationen in der Konfigurationsstruktur.

    ![Importierte EB-Konfigurationen auf der Seite „Konfigurationen“.](./media/ER-DeferredSequence-Configurations.png)

### <a name="activate-a-configurations-provider"></a>Aktivieren eines Konfigurationsanbieters

1. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
2. Überprüfen Sie auf der Seite **Lokalisierungskonfigurationen** im Abschnitt **Konfigurationsanbieter**, ob der [Konfigurationsanbieter](general-electronic-reporting.md#Provider) für das Beispielunternehmen Litware, Inc. (`http://www.litware.com`) aufgeführt und als „Aktiv“ markiert ist. Wenn dieser Konfigurationsanbieter nicht aufgeführt oder nicht als „Aktiv“ markiert ist, befolgen Sie die Schritte im Thema [Konfigurationsanbieter erstellen und als aktiv markieren](./tasks/er-configuration-provider-mark-it-active-2016-11.md).

    ![Beispielfirma Litware, Inc. auf der Seite „Lokalisierungskonfigurationen“.](./media/ER-DeferredSequence-ElectronicReportingWorkspace.png)

### <a name="review-the-imported-model-mapping"></a>Überprüfung der importierten Modellzuordnung

Überprüfen Sie die Einstellungen der ER-Modellzuordnungskomponente, die für den Zugriff auf Steuerbuchungen konfiguriert ist, und stellen Sie auf Anforderung die aufgerufenen Daten bereit.

1. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
2. Wählen Sie **Berichterstellungskonfigurationen** aus.
3. Erweitern Sie auf der Seite **Konfigurationen** die Konfigurationsstruktur für **Modell zum Erlernen verzögerter Elemente**.
4. Wähle Sie die Konfiguration für **Zuordnung zum Verstehen verzögerter Elemente** aus.
5. Wählen Sie **Designer** aus, um die Liste der Zuordnungen zu öffnen.
6. Wählen Sie **Designer** aus, um die Zuordnungsdetails zu prüfen.
7. Wählen Sie **Details anzeigen**.
8. Überprüfen Sie die Datenquellen, die für den Zugriff auf Steuerbuchungen konfiguriert sind:

    - Die Datenquelle **Transaktionen** vom Typ *Tabellendatensatz* ist für den Zugriff auf Datensätze der Anwendungstabelle **TaxTrans** konfiguriert.
    - Die Datenquelle **Belege** vom Typ *Berechnetes Feld* ist so konfiguriert, dass die erforderlichen Belegcodes (**INV-10000349** und **INV-10000350**) als Liste von Datensätzen zurückgegeben werden.
    - Die Datenquelle **Gefiltert** vom Typ *Berechnetes Feld* ist so konfiguriert, dass sie aus der Datenquelle **Transaktionen** nur Steuerbuchungen der erforderlichen Belege auswählt.
    - Das Feld **\$TaxAmount** vom Typ *Berechnetes Feld* wird zur Datenquelle **Gefiltert** hinzugefügt, um den Steuerwert anzuzeigen, der das entgegengesetzte Vorzeichen hat.
    - Die Datenquelle **Gruppiert** vom Typ *Gruppieren nach* ist so konfiguriert, dass gefilterte Steuerbuchungen der Datenquelle **Gefiltert** gruppiert werden.
    - Das Aggregationsfeld **TotalSum** der Datenquelle **Gruppiert** ist so konfiguriert, dass Werte des Felds **\$TaxAmount** der Datenquelle **Gefiltert** für alle gefilterten Steuerbuchungen dieser Datenquelle zusammengefasst werden.

        ![Aggregationsfeld „TotalSum“ auf der Bearbeitungsseite „‚GroupBy‘ Parameter“.](./media/ER-DeferredSequence-GroupByParameters.png)

9. Überprüfen Sie, wie die konfigurierten Datenquellen an das Datenmodell gebunden sind und wie sie aufgerufene Daten verfügbar machen, um sie in einem ER-Format verfügbar zu machen:

    - Die Datenquelle **Gefiltert** ist an das Feld **Data.List** des Datenmodells gebunden.
    - Das Feld **\$TaxAmount** der Datenquelle **Gefiltert** ist an das Feld **Data.List.Value** des Datenmodells gebunden.
    - Das Feld **TotalSum** der Datenquelle **Gruppiert** ist an das Feld **Data.Summary.Total** es Datenmodells gebunden.

    ![Modellzuordnungsdesigner-Seite.](./media/ER-DeferredSequence-ModelMapping.png)

10. Schließen Sie die Seiten **Modellzuordnungsdesigner** und **Modellzuordnungen**.

### <a name="review-the-imported-format"></a>Überprüfen Sie das importierte Format

1. Wählen Sie auf der Seite **Konfigurationen** in der Konfigurationsstruktur die Konfiguration für **Format zum Verstehen verzögerter Sequenzen** aus.
2. Wählen Sie **Designer** aus, um die Formatdetails zu prüfen.
3. Wählen Sie **Details anzeigen**.
4. Überprüfen Sie die Einstellungen der ER-Formatkomponenten, die so konfiguriert sind, dass sie ein ausgehendes Dokument im Textformat generieren, das Details zu den Steuerbuchungen enthält:

    - Das Sequenzformatelement **Bericht\\Zeilen** ist so konfiguriert, dass es das ausgehende Dokument mit einer einzelnen Zeile füllt, die aus den verschachtelten Sequenz-Elementen generiert wird (**Header**, **Datensatz** und **Zusammenfassung**).

        ![Zeilensequenzformat-Elemente und verschachtelte Elemente auf der Formatdesignerseite.](./media/ER-DeferredSequence-Format.png)

    - Das Sequenzformatelement **Bericht\\Zeilen\\Header** ist so konfiguriert, dass es das ausgehende Dokument mit einer einzelnen Header-Zeile füllt, die das Datum und die Uhrzeit der Bearbeitungsbeginns zeigt.
    - Das Sequenzformatelement **Bericht \\Zeilen\\Datensatz** ist so konfiguriert, dass es das ausgehende Dokument mit einer einzelnen Zeile füllt, die die Details einer einzelnen Steuerbuchung anzeigt. Diese Steuerbuchungen sind durch ein Semikolon getrennt.

        ![Datensatzsequenz-Formatelement, das ein Semikolon als Trennzeichen verwendet.](./media/ER-DeferredSequence-Format1.png)

    - Das Sequenzformatelement **Bericht\\Zeilen\\Zusammenfassung** ist so konfiguriert, dass das ausgehende Dokument mit einer einzelnen Zusammenfassungszeile gefüllt wird, die die Summe der Steuerwerte aus den verarbeiteten Steuerbuchungen enthält.

4. Überprüfen Sie auf der Registerkarte **Zuordnung** die folgenden Details:

    - Das Element **Bericht\\Nachricht\\Zusammenfassung** muss nicht an eine Datenquelle gebunden sein, um eine einzelne Zeile in einem ausgehenden Dokument zu generieren.
    - Das **Prefix1**-Element erzeugt **P1**-Symbole, die darauf hinweisen, dass es sich bei der hinzugefügten Zeile um die Berichtskopfzeile handelt.
    - Das **ExecutionDateTime**-Element generiert das Datum und die Uhrzeit (einschließlich Millisekunden), zu dem bzw. zu der die Header-Zeile hinzugefügt wurde.
    - Das Element **Bericht\\Zeilen\\Datensatz** ist an die Liste **model.Data.List** gebunden, um eine einzelne Zeile für jeden Datensatz aus der gebundenen Liste zu generieren.
    - Das **Prefix2**-Element erzeugt **P2**-Symbole, die darauf hinweisen, dass die hinzugefügte Zeile für Steuerbuchungsdetails verwendet wird.
    - Das Element **TaxAmount** ist an **model.Data.List.Value** gebunden (wird als **\@.Value** in der relativen Pfadansicht gezeigt), um den Steuerwert des aktuellen Steuerbuchung zu generieren.
    - Das **RunningTotal**-Element ist ein Platzhalter für die laufende Summe der Steuerwerte. Derzeit hat dieses Element keine Ausgabe, da für dieses Attribut weder eine Bindung noch ein Standardwert konfiguriert ist.
    - Das **ExecutionDateTime**-Element generiert das Datum und die Uhrzeit (einschließlich Millisekunden), zu dem bzw. zu der die aktuelle Transaktion in diesem Bericht verarbeitet wird.
    - Das Element **Bericht\\Zeilen\\Zusammenfassung** muss nicht an eine Datenquelle gebunden sein, um eine einzelne Zeile in einem ausgehenden Dokument zu generieren.
    - Das **Prefix3**-Element erzeugt **P3**-Symbole, die darauf hinweisen, dass die hinzugefügte Zeile den Gesamtsteuerwert enthält.
    - Das **TotalTaxAmount**-Element ist an **model.Data.Summary.Total** gebunden, um die Summe der Steuerwerte der verarbeiteten Steuerbuchungen zu generieren.
    - Das **ExecutionDateTime**-Element generiert das Datum und die Uhrzeit (einschließlich Millisekunden), zu dem bzw. zu der die Zusammenfassungszeile hinzugefügt wurde.

    ![Registerkarte „Zuordnung“ auf der Formatdesignerseite.](./media/ER-DeferredSequence-Format2.png)

### <a name="run-the-imported-format"></a>Importiertes Format ausführen

1. Wählen Sie auf der Seite **Formatdesigner** die Option **Ausführen** aus.
2. Laden Sie die vom Webbrowser angebotene Datei herunter und öffnen Sie sie zur Überprüfung.

    ![Heruntergeladene Beispiel-Berichtsdatei.](./media/ER-DeferredSequence-Run.png)

Beachten Sie, dass die Zusammenfassungszeile 22 die Summe der Steuerwerte für die verarbeiteten Transaktionen anzeigt. Weil das Format für die Verwendung der **model.Data.Summary.Total**-Bindung zum Zurückgeben der Summe konfiguriert ist, wird die Summe berechnet, indem die **TotalSum**-Aggregation der Datenquelle **Gruppiert** vom Typ *GroupBy*, die die Modellzuordnung verwendet, aufgerufen wird. Um diese Aggregation zu berechnen, durchläuft die Modellzuordnung alle Transaktionen, die in der Datenquelle **Gefiltert** ausgewählt wurden. Durch Vergleichen der Ausführungszeiten der Zeilen 21 und 22 können Sie feststellen, dass die Berechnung der Summe 10 Millisekunden (ms) gedauert hat. Durch Vergleichen der Ausführungszeiten der Zeilen 2 und 21 können Sie feststellen, dass das Generieren aller Transaktionszeilen 7 Millisekunden (ms) gedauert hat. Daher waren insgesamt 17 ms erforderlich.

### <a name="modify-the-format-so-that-the-summing-is-based-on-generated-output"></a>Ändern des Formats, sodass die Summierung auf der generierten Ausgabe basiert

Wenn das Transaktionsvolumen viel größer als das Volumen im aktuellen Beispiel ist, kann sich die Summierungszeit verlängern und Leistungsprobleme verursachen. Indem Sie die Einstellung des Formats ändern, können Sie diese Leistungsprobleme vermeiden. Da Sie auf Steuerwerte zugreifen, um diese in den generierten Bericht aufzunehmen, können Sie diese Informationen zur Summierung von Steuerwerten wiederverwenden. Weitere Informationen finden Sie unter [Konfigurieren des Formats für Inventuren und Summierungen](./tasks/er-format-counting-summing-1.md).

1. Wählen Sie auf der Seite **Formatdesigner** auf der Registerkarte **Format** das Dateielement **Bericht** in der Formatierungsstruktur aus.
2. Legen Sie die Option **Ausgabendetails sammeln** auf **Ja** fest. Sie können dieses Format jetzt konfigurieren, indem Sie den Inhalt eines bestehenden Berichts als Datenquelle verwenden, auf die mit den integrierten ER-Funktionen der Kategorie [Datensammlung](er-functions-category-data-collection.md) zugegriffen werden kann.
3. Wählen Sie auf der Registerkarte **Zuordnung** das Sequenz-Element **Bericht\\Zeilen** aus.
4. Konfigurieren Sie den Ausdruck **Gesammelter Datenschlüsselname** als `WsColumn`.
5. Konfigurieren Sie den Ausdruck **Gesammelter Datenschlüsselwert** als `WsRow`.

    ![Zeilensequenz-Element auf der Formatdesignerseite.](./media/ER-DeferredSequence-Format3.png)

6. Wählen Sie das numerische Element **Bericht\\Zeilen\\Datensatz\\TaxAmount** aus.
7. Konfigurieren Sie den Ausdruck **Gesammelter Datenschlüsselname** als `SummingAmountKey`.

    ![Numerisches Element „TaxAmount“ auf der Formatdesignerseite.](./media/ER-DeferredSequence-Format4.png)

    Sie können diese Einstellung als Erfüllung eines virtuellen Arbeitsblatts betrachten, bei dem der Wert der Zelle A1 durch den Wert des Steuerbetrags aus jeder verarbeiteten Steuerbuchung ergänzt wird.

8. Wählen Sie das numerische Element **Bericht\\Zeilen\\Datensatz\\RunningTotal** und **Formel bearbeiten** aus.
9. Konfigurieren Sie den Ausdruck `SUMIF(SummingAmountKey, WsColumn, WsRow)` mit der integrierten ER-Funktion [SUMIF](er-functions-datacollection-sumif.md).
10. Wählen Sie **Speichern** aus.

    ![SUMIF-Ausdruck.](./media/ER-DeferredSequence-FormulaDesigner.png)

11. Schließen Sie die Seite **Formeldesigner**.
12. Wählen Sie **Speichern** und dann **Ausführen** aus.
13. Laden Sie die vom Webbrowser angebotene Datei herunter und öffnen Sie sie zur Überprüfung.

    ![Heruntergeladene Datei – Summierte Steuerwerte.](./media/ER-DeferredSequence-Run1.png)

    Zeile 21 enthält die laufende Summe der Steuerwerte, die für alle verarbeiteten Transaktionen unter Verwendung der generierten Ausgabe als Datenquelle berechnet werden. Diese Datenquelle beginnt am Anfang des Berichts und geht bis zur letzten Steuerbuchung. Zeile 22 enthält die Summe der Steuerwerte für alle verarbeiteten Transaktionen, die in der Modellzuordnung unter Verwendung der Datenquelle des Typs *GroupBy* berechnet werden. Beachten Sie, dass diese Werte gleich sind. Daher kann die ausgabenbasierte Summierung anstelle von **GroupBy** verwendet werden. Durch Vergleichen der Ausführungszeiten der Zeilen 2 und 21 können Sie feststellen, dass das Generieren aller Transaktionszeilen und das Summieren 9 Millisekunden (ms) gedauert hat. Daher ist das geänderte Format hinsichtlich der Erzeugung von Detailzeilen und der Summierung von Steuerwerten ungefähr zweimal schneller als das ursprüngliche Format.

14. Wählen Sie das numerische Element **Bericht\\Zeilen\\Zusammenfassung\\TotalTaxAmount** und **Formel bearbeiten** aus.
15. Geben Sie den Ausdruck `SUMIF(SummingAmountKey, WsColumn, WsRow)` anstelle des vorhandenen Ausdrucks ein.
16. Wählen Sie **Speichern** und dann **Ausführen** aus.
17. Laden Sie die vom Webbrowser angebotene Datei herunter und öffnen Sie sie zur Überprüfung.

    ![Heruntergeladene Datei mit bearbeiteter Formel.](./media/ER-DeferredSequence-Run2.png)

    Beachten Sie, dass die laufende Summe der Steuerwerte in der letzten Transaktionsdetailzeile jetzt der Summe in der Zusammenfassungszeile gleicht.

### <a name="put-values-of-output-based-summing-in-the-report-header"></a>Ausgabenbasierte Summierungswerte im Berichtskopf angeben

Wenn Sie beispielsweise die Summe der Steuerwerte in der Kopfzeile Ihres Berichts angeben müssen, können Sie Ihr Format ändern.

1. Wählen Sie auf der Seite **Formatdesigner** auf der Registerkarte **Format** das Sequenz-Element **Bericht\\Zeilen\\Zusammenfassung** aus.
2. Wählen Sie **Nach oben**.
3. Wählen Sie **Speichern** und dann **Ausführen** aus.
4. Laden Sie die vom Webbrowser angebotene Datei herunter und öffnen Sie sie zur Überprüfung.

    ![Heruntergeladene Datei für die Summierung im Berichtskopf.](./media/ER-DeferredSequence-Run3.png)

    Beachten Sie, dass die Summe der Steuerwerte in der Zusammenfassungszeile 2 jetzt gleich 0 (Null) ist, da diese Summe jetzt auf der Grundlage der generierten Ausgabe berechnet wird. Wenn Zeile 2 generiert wird, enthält die generierte Ausgabe noch keine Zeilen mit Transaktionsdetails. Sie können dieses Format so konfigurieren, dass die Ausführung des Sequenz-Elements **Bericht\\Zeilen\\Zusammenfassung** verzögert wird, bis das Element **Bericht\\Zeilen\\Datensatz** für alle Steuerbuchungen ausgeführt wurde.

### <a name="defer-the-execution-of-the-summary-sequence-so-that-the-calculated-total-is-used"></a>Verzögern der Ausführung der Zusammenfassungssequenz, sodass die berechnete Gesamtsumme verwendet wird

1. Wählen Sie auf der Seite **Formatdesigner** auf der Registerkarte **Format** das Sequenz-Element **Bericht\\Zeilen\\Zusammenfassung** aus.
2. Legen Sie die Option **Verzögerte Ausführung** auf **Ja** fest.

    ![Option „Verzögerte Ausführung“ des Zusammenfassungs-Sequenz-Elements auf der Formatdesignerseite.](./media/ER-DeferredSequence-Format5.png)

3. Wählen Sie **Speichern** und dann **Ausführen** aus.
4. Laden Sie die vom Webbrowser angebotene Datei herunter und öffnen Sie sie zur Überprüfung.

    ![Heruntergeladene Datei – aufgeschobene Ausführung.](./media/ER-DeferredSequence-Run4.png)

    Das Sequenz-Element **Bericht\\Zeilen\\Zusammenfassung** wird jetzt nur dann ausgeführt, wenn alle Elemente unter dem übergeordneten Element, **Bericht\\Zeilen**, bereits ausgeführt wurden. Deshalb wird es nach Ausführung des Sequenz-Elements **Bericht\\Zeilen\\Datensatz** für alle Steuerbuchungen der Datenquelle **model.Data.List** ausgeführt. Die Ausführungszeiten der Zeilen 1, 2 und 3 sowie der letzten Zeile 22 belegen diese Tatsache.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Konfigurieren des Formats für Inventuren und Summierungen](./tasks/er-format-counting-summing-1.md)
- [Ausführung des EB-Formats nachverfolgen, um Leistungsprobleme zu behandeln](trace-execution-er-troubleshoot-perf.md)
- [Verzögern der Ausführung von XML-Elementen in ER-Formaten](er-defer-xml-element.md#Example)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
