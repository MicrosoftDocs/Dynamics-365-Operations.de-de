---
title: Konfigurierte EB-Komponente überprüfen, um Laufzeitprobleme zu vermeiden
description: In diesem Artikel wird erläutert, wie Sie die konfigurierten EB-Komponenten (Elektronische Berichterstellung) überprüfen, um mögliche Laufzeitprobleme zu vermeiden.
author: kfend
ms.date: 09/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.custom: 220314
ms.assetid: ''
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner
ms.openlocfilehash: 1ca59d6c26dbcf065adb952409da30002d951f62
ms.sourcegitcommit: a1d14836b40cfc556f045c6a0d2b4cc71064a6af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/14/2022
ms.locfileid: "9476853"
---
# <a name="inspect-the-configured-er-component-to-prevent-runtime-issues"></a>Konfigurierte EB-Komponente überprüfen, um Laufzeitprobleme zu vermeiden

[!include[banner](../includes/banner.md)]

Alle konfigurierten [Formate](er-overview-components.md#format-components-for-outgoing-electronic-documents) und [Modellzuordnungskomponenten](er-overview-components.md#model-mapping-component) der [elektronischen Berichterstellung (EB)](general-electronic-reporting.md) können zur Entwurfszeit [bestätigt](er-fillable-excel.md#validate-an-er-format) werden. Während dieser Prüfung wird eine Konsistenzprüfung durchgeführt, um mögliche Laufzeitprobleme, wie etwa Ausführungsfehler und Leistungseinbußen, zu vermeiden. Für jedes gefundene Problem wird der Pfad eines problematischen Elements angegeben. Für einige Probleme ist eine automatische Korrektur verfügbar.

Standardmäßig wird die Prüfung in den folgenden Fällen automatisch für eine EB-Konfiguration angewendet, die die zuvor genannten EB-Komponenten enthält:

- Sie [importieren](general-electronic-reporting.md#importing-an-er-component-from-lcs-to-use-it-internally) eine neue Version einer EB-Konfiguration in Ihre Instanz von Microsoft Dynamics 365 Finance.
- Sie ändern den Status der bearbeitbaren EB-Konfiguration von **Entwurf** zu **Abgeschlossen**.
- Sie können eine bearbeitbare EB-Konfiguration [zurücksetzen](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase), indem Sie eine neue Basisversion anwenden.

Sie können diese Prüfung explizit ausführen. Wählen Sie eine der folgenden drei Optionen aus und befolgen Sie die angegebenen Schritte:

- Option 1:

    1. Wechseln Sie zu **Organisationsverwaltung \> Elektronische Berichterstellung \> Konfigurationen**.
    2. Wählen Sie im Konfigurationsbaum im linken Bereich die gewünschte EB-Konfiguration aus, die das EB-Format oder die EB-Modellzuordnungskomponente enthält.
    3. Wählen Sie im Inforegister **Versionen** die gewünschte Version der ausgewählten EB-Konfiguration aus.
    4. Wählen Sie im Aktivitätsbereich **Überprüfen** aus.

- Option 2 für ein EB-Format:

    1. Wechseln Sie zu **Organisationsverwaltung \> Elektronische Berichterstellung \> Konfigurationen**.
    2. Wählen Sie im Konfigurationsbaum im linken Bereich die gewünschte EB-Konfiguration aus, die das EB-Format enthält.
    3. Wählen Sie im Inforegister **Versionen** die gewünschte Version der ausgewählten EB-Konfiguration aus.
    4. Wählen Sie im Aktivitätsbereich **Designer** aus.
    5. Wählen Sie auf der Seite **Formatdesigner** im Aktivitätsbereich die Option **Überprüfen** aus.

- Option 3 für eine EB-Modellzuordnung:

    1. Wechseln Sie zu **Organisationsverwaltung \> Elektronische Berichterstellung \> Konfigurationen**.
    2. Wählen Sie im Konfigurationsbaum im linken Bereich die gewünschte EB-Konfiguration aus, die die EB-Modellzuordnungskomponente enthält.
    3. Wählen Sie im Inforegister **Versionen** die gewünschte Version der ausgewählten EB-Konfiguration aus.
    4. Wählen Sie im Aktivitätsbereich **Designer** aus.
    5. Wählen Sie auf der Seite **Modell für Datenquellenzuordnung** im Aktionsbereich **Designer** aus.
    6. Wählen Sie auf der Seite **Modellzuordnungsdesigner** im Aktionsbereich die Option **Überprüfen** aus.

Führen Sie die folgenden Schritte aus, um die Prüfung beim Importieren der Konfiguration zu überspringen.

1. Wechseln Sie zu **Organisationsverwaltung \> Elektronische Berichterstellung \> Konfigurationen**.
2. Auf der Seite **Konfigurationen** im Aktivitätsbereich, auf der Registerkarte **Konfigurationen** in der Gruppe **Erweiterte Einstellungen** wählen Sie **Benutzerparameter** aus.
3. Legen Sie die Option **Konfiguration nach dem Import überprüfen** auf **Nein** fest.

Führen Sie die folgenden Schritte aus, um die Überprüfung zu überspringen, wenn der Status der Version geändert oder zurückgesetzt wird.

1. Wechseln Sie zu **Organisationsverwaltung \> Elektronische Berichterstellung \> Konfigurationen**.
2. Auf der Seite **Konfigurationen** im Aktivitätsbereich, auf der Registerkarte **Konfigurationen** in der Gruppe **Erweiterte Einstellungen** wählen Sie **Benutzerparameter** aus.
3. Legen Sie die Option **Prüfung bei geändertem oder zurückgesetztem Konfigurationsstatus überspringen** auf **Ja** fest.

Die EB verwendet die folgenden Kategorien, um Konsistenzprüfungen zu gruppieren:

- **Ausführbarkeit** – Inspektionen, die kritische Probleme erkennen, die zur Laufzeit auftreten können. Bei diesen Problemen handelt es sich meistens um **Fehler**. 
- **Leistung** – Inspektionen, die Probleme erkennen, die zu einer ineffizienten Ausführung konfigurierter EB-Komponenten führen können. Bei diesen Problemen handelt es sich meistens um **Warnungen**.
- **Datenintegrität** – Inspektionen, bei denen Probleme festgestellt werden, die zu Datenverlust oder Laufzeitproblemen führen können. Bei diesen Problemen handelt es sich meistens um **Warnungen**.

## <a name="list-of-inspections"></a>Liste der Inspektionen

Die folgende Tabelle enthält eine Übersicht der Inspektionen, die die EB bietet. Weitere Informationen zu diesen Inspektionen erhalten Sie über die Links in der ersten Spalte, um zu den entsprechenden Abschnitten dieses Artikels zu gelangen. In diesen Abschnitten werden die Komponententypen erläutert, für die die EB Inspektionen bereitstellt, sowie die Neukonfiguration von EB-Komponenten, um Probleme zu vermeiden.

<table>
<thead>
<tr>
<th>Name</th>
<th>Kategorie</th>
<th>Stufe</th>
<th>Meldung</th>
</tr>
</thead>
<tbody>
<tr>
<td><a href='#i1'>Typenumrechnung</a></td>
<td>Ausführbarkeit</td>
<td>Fehler</td>
<td>
<p>Ausdruck vom Typ &lt;Typ&gt; kann nicht zu Feld vom Typ &lt;Typ&gt; konvertiert werden.</p>
<p><b>Laufzeitfehler:</b> Ausnahme fü Typ</p>
</td>
</tr>
<tr>
<td><a href='#i2'>Typkompatibilität</a></td>
<td>Ausführbarkeit</td>
<td>Fehler</td>
<td>
<p>Der konfigurierte Ausdruck kann nicht als Bindung des aktuellen Formatelements an eine Datenquelle verwendet werden, da dieser Ausdruck einen Wert vom Datentyp &lt;Typ&gt; zurückgibt. Dieser Datentyp liegt außerhalb des Bereichs der Datentypen, die vom aktuellen Formatelement vom Typ &lt;Typ&gt; unterstützt werden.</p>
<p><b>Laufzeitfehler:</b> Ausnahme vom Typ</p>
</td>
</tr>
<tr>
<td><a href='#i3'>Fehlendes Konfigurationselement</a></td>
<td>Ausführbarkeit</td>
<td>Fehler</td>
<td>
<p>Pfad &lt;Pfad&gt; nicht gefunden.</p>
<p><b>Laufzeitfehler:</b> Element der Konfiguration &lt;Pfad&gt; nicht gefunden</p>
</td>
</tr>
<tr>
<td><a href='#i4'>Ausführbarkeit eines Ausdrucks mit FILTER-Funktion</a></td>
<td>Ausführbarkeit</td>
<td>Fehler</td>
<td>
<p>Der Listenausdruck der FILTER-Funktion ist nicht abfragbar.</p>
<p><b>Laufzeitfehler:</b> Filterung wird nicht unterstützt. Überprüfen Sie die Konfiguration für weitere Details hierzu.</p>
</td>
</tr>
<tr>
<td rowspan='2'><a href='#i5'>Ausführbarkeit einer GROUPBY-Datenquelle</a></td>
<td>Ausführbarkeit</td>
<td>Fehler</td>
<td>Pfad &lt;Pfad&gt; unterstützt keine Abfragen.</td>
</tr>
<tr>
<td>Ausführbarkeit</td>
<td>Fehler</td>
<td>
<p>Gruppierung nach Funktion kann mit Abfrage nicht ausgeführt werden.</p>
<p><b>Laufzeitfehler:</b> Gruppierung nach Funktion kann mit Abfrage nicht ausgeführt werden.</p>
</td>
</tr>
<tr>
<td><a href='#i6'>Ausführbarkeit einer JOIN-Datenquelle</a></td>
<td>Ausführbarkeit</td>
<td>Fehler</td>
<td>
<p>Kann keiner Liste &lt;Pfad&gt; beitreten, die kein Filter in der Abfrage ist.</p>
<p><b>Laufzeitfehler:</b> Die Funktion „Verknüpfte Datenquelle“ sollte ein Filterausdruck sein. Das berechnete Feld wurde falsch aufgerufen.</p>
</td>
</tr>
<tr>
<td><a href='#i7'>Bevorzugung der FILTER- gegenüber der WHERE-Funktion</a></td>
<td>Leistung</td>
<td>Achtung</td>
<td>Die FILTER-Funktion für den Ausdruck ist aus Sicht der Leistung der WHERE-Funktion vorzuziehen. Wählen Sie „Beheben“ aus, um sie automatisch zu ersetzen.</td>
</tr>
<tr>
<td><a href='#i8'>Bevorzugung der ALLITEMSQUERY- gegenüber der ALLITEMS-Funktion</a></td>
<td>Leistung</td>
<td>Achtung</td>
<td>Die ALLITEMSQUERY-Funktion für den Ausdruck ist aus Sicht der Leistung der ALLITEMS-Funktion vorzuziehen. Wählen Sie „Beheben“ aus, um sie automatisch zu ersetzen.</td>
</tr>
<tr>
<td><a href='#i9'>Berücksichtigung leerer Listenfälle</a></td>
<td>Ausführbarkeit</td>
<td>Achtung</td>
<td>
<p>Die Liste &lt;Pfad&gt; wird nicht auf leere Listenfälle überprüft. Dies kann zur Laufzeit zu einem Fehler führen. Fügen Sie eine Überprüfung für einen leeren Listenfall hinzu.</p>
<p><b>Laufzeitfehler:</b> Liste ist leer bei &lt;Pfad&gt;</p>
<p><b><a href='#i9a'>Mögliches Problem</a>:</b> Die Position wird einmal ausgefüllt, während eine Datenquelle, aus der sie ausgefüllt wird, mehrere Datensätze enthält.</p>
</td>
</tr>
<tr>
<td><a href='#i10'>Ausführbarkeit eines Ausdrucks mit FILTER-Funktion (Zwischenspeicherung)</a></td>
<td>Ausführbarkeit</td>
<td>Fehler</td>
<td>
<p>Die FILTER-Funktion kann nicht auf den ausgewählten Datenquellentyp angewendet werden. Eine Datenquelle vom Typ „Tabellendatensätze“ ist nur anwendbar, wenn sie nicht zwischengespeichert ist und keine manuell hinzugefügten verschachtelten Datenquellen enthält.</p>
<p><b>Laufzeitfehler:</b> Filterung wird nicht unterstützt. Überprüfen Sie die Konfiguration für weitere Details hierzu.</p>
</td>
</tr>
<tr>
<td><a href='#i11'>Fehlende Bindung</a></td>
<td>Ausführbarkeit</td>
<td>Achtung</td>
<td>
<p>Der Pfad &lt;Pfad&gt; hat keine Bindung an eine Datenquelle bei der Verwendung der Modellzuordnung.</p>
<p><b>Laufzeitfehler:</b> Pfad &lt;Pfad&gt; ist nicht gebunden</p>
</td>
</tr>
<tr>
<td><a href='#i12'>Nicht verknüpfte Vorlage</a></td>
<td>Datenintegrität</td>
<td>Achtung</td>
<td>Die Datei &lt;Name&gt; ist mit keinen Dateikomponenten verknüpft und wird nach Änderung des Status der Konfigurationsversion entfernt.</td>
</tr>
<tr>
<td><a href='#i13'>Nicht synchronisiertes Format</a></td>
<td>Datenintegrität</td>
<td>Achtung</td>
<td>Der definierte Name &lt;Komponentenname&gt; existiert nicht in der Excel-Tabelle &lt;Tabellenname&gt;.</td>
</tr>
<tr>
<td><a href='#i14'>Nicht synchronisiertes Format</a></td>
<td>Datenintegrität</td>
<td>Achtung</td>
<td>
<p>Die Markierung &lt;Markiertes Word-Inhaltssteuerelement&gt; ist in der Word-Vorlagendatei nicht vorhanden</p>
<p><b>Laufzeitfehler:</b> Die Markierung &lt;Markiertes Word-Inhaltssteuerelement&gt; ist in der Word-Vorlagendatei nicht vorhanden.</p>
</td>
</tr>
<tr>
<td><a href='#i15'>Keine Standardzuordnung</a></td>
<td>Datenintegrität</td>
<td>Fehler</td>
<td>
<p>Es gibt mehr als eine Modellzuordnung für das Datenmodell &lt;Modellname (Stammdeskriptor)&gt; in den Konfigurationen &lt;Konfigurationsnamen durch Komma getrennt&gt;. Eine der Konfigurationen als Standard festlegen</p>
<p><b>Laufzeitfehler:</b> Es gibt mehr als eine Modellzuordnung für das Datenmodell &lt;Modellname (Stammdeskriptor)&gt; in den Konfigurationen &lt;Konfigurationsnamen durch Komma getrennt&gt;. Legen Sie eine der Konfigurationen als Standard fest.</p>
</td>
</tr>
<tr>
<td><a href='#i16'>Inkonsistente Einstellung der Kopf- oder Fußzeilenkomponenten</a></td>
<td>Datenintegrität</td>
<td>Fehler</td>
<td>
<p>Kopf-/Fußzeilen (&lt;Komponententyp: Kopf- oder Fußzeile&gt;) sind inkonsistent</p>
<p><b>Laufzeit:</b> Die zuletzt konfigurierte Komponente wird während der Laufzeit verwendet, wenn die Entwurfsversion des konfigurierten EB-Formats ausgeführt wird.</p>
</td>
</tr>
<tr>
<td><a href='#i17'>Inkonsistente Einstellung der Seitenkomponente</a></td>
<td>Datenintegrität</td>
<td>Fehler</td>
<td>Es gibt mehr als zwei Bereichskomponenten ohne Replikation. Bitte entfernen Sie nicht benötigte Komponenten.</td>
</tr>
<tr>
<td><a href='#i18'>Ausführbarkeit eines Ausdrucks mit der Funktion ORDERBY</a></td>
<td>Ausführbarkeit</td>
<td>Fehler</td>
<td>
<p>Der Listenausdruck der ORDERBY-Funktion ist nicht abfragbar.</p>
<p><b>Laufzeitfehler:</b> Die Sortierung wird nicht unterstützt. Überprüfen Sie die Konfiguration für weitere Details hierzu.</p>
</td>
</tr>
<tr>
<td><a href='#i19'>Veraltetes Anwendungsartefakt</a></td>
<td>Datenintegrität</td>
<td>Achtung</td>
<td>
<p>Das Element &lt;Pfad&gt; ist als veraltet markiert.<br>oder<br>Das Element &lt;Pfad&gt; ist mit der Meldung &lt;Meldungstext&gt; als veraltet markiert.</p>
<p><b>Beispiel für Laufzeitfehler:</b> Klasse „&lt;Pfad&gt;“ nicht gefunden.</p>
</td>
</tr>
</tbody>
</table>

## <a name="type-conversion"></a><a id="i1"></a>Typenumrechnung

Die EB überprüft, ob der Datentyp eines Datenmodellfelds mit dem Datentyp eines Ausdrucks kompatibel ist, der als Bindung dieses Felds konfiguriert ist. Wenn die Datentypen nicht kompatibel sind, tritt im EB-Modellzuordnungsdesigner ein Prüfungsfehler auf. Die Nachricht, die Sie erhalten, besagt, dass die EB einen Ausdruck vom Typ A nicht in ein Feld vom Typ B konvertieren kann.

Die folgenden Schritte zeigen, wie dieses Problem auftreten kann.

1. Beginnen Sie gleichzeitig mit der Konfiguration des EB-Datenmodells und der EB-Modellzuordnungskomponenten.
2. Fügen Sie im Datenmodellbaum ein Feld mit dem Namen **X** hinzu und wählen Sie **Integer** als Datentyp aus.

    ![Das Feld „X“ und der Datentyp „Integer“ wurden dem Datenmodusbaum auf der Seite „Datenmodell“ hinzugefügt.](./media/er-components-inspections-01.png)

3. Fügen Sie im Bereich **Datenquellen** des Modellzuordnungsdesigners eine Datenquelle vom Typ **Berechnetes Feld** hinzu.
4. Nennen Sie die neue Datenquelle **Y** und konfigurieren Sie sie so, dass sie den Ausdruck `INTVALUE(100)` enthält.
5. Binden Sie **X** an **Y**.
6. Ändern Sie im Datenmodelldesigner den Datentyp des Felds **X** von **Integer** zu **Int64**.
7. Wählen Sie **Überprüfen** aus, um die bearbeitbare Modellzuordnungskomponente auf der Seite **Modellzuordnungsdesigner** zu überprüfen.

    ![Überprüfen der bearbeitbaren Modellzuordnungskomponente auf der Seite „Modellzuordnungsdesigner“.](./media/er-components-inspections-01.gif)

8. Wählen Sie **Überprüfen** aus, um die Modellzuordnungskomponente der ausgewählten EB-Konfiguration auf der Seite **Konfigurationen** zu überprüfen.

    ![Untersuchen der Modellzuordnungskomponente auf der Seite „Konfigurationen“.](./media/er-components-inspections-01a.png)

9. Beachten Sie, dass ein Prüfungsfehler auftritt. Die Nachricht gibt an, dass der Wert vom Typ **Integer**, der vom Ausdruck `INTVALUE(100)` der Datenquelle **Y** zurückgegeben wird, nicht im Datenmodellfeld **X** vom Typ **Int64** gespeichert werden kann.

Die folgende Abbildung zeigt den Laufzeitfehler, der auftritt, wenn Sie die Warnung ignorieren und **Ausführen** auswählen, um ein Format auszuführen, das für die Verwendung der Modellzuordnung konfiguriert ist.

![Laufzeitfehler auf der Seite „Formatdesigner“.](./media/er-components-inspections-01b.png)

### <a name="automatic-resolution"></a>Automatische Lösung

Es ist keine Option verfügbar, um dieses Problem automatisch zu beheben.

### <a name="manual-resolution"></a>Manuelle Lösung

#### <a name="option-1"></a>Option 1

Aktualisieren Sie die Datenmodellstruktur, indem Sie den Datentyp des Datenmodellfelds so ändern, dass er mit dem Datentyp des Ausdrucks übereinstimmt, der für die Bindung dieses Felds konfiguriert ist. Für das vorstehende Beispiel muss der Datentyp des Felds **X** wieder zu **Integer** geändert werden.

#### <a name="option-2"></a>Option 2

Aktualisieren Sie die Modellzuordnung, indem Sie den Ausdruck der Datenquelle ändern, die an das Datenmodellfeld gebunden ist. Für das vorstehende Beispiel muss der Ausdruck der Datenquelle **Y** zu `INT64VALUE(100)` geändert werden.

## <a name="type-compatibility"></a><a id="i2"></a>Typkompatibilität

Die EB überprüft, ob der Datentyp eines Formatelements mit dem Datentyp eines Ausdrucks kompatibel ist, der als Bindung dieses Formatelements konfiguriert ist. Wenn die Datentypen nicht kompatibel sind, tritt im EB-Arbeitsgangsdesigner ein Prüfungsfehler auf. Die Nachricht, die Sie erhalten, besagt, dass der konfigurierte Ausdruck kann nicht als Bindung des aktuellen Formatelements an eine Datenquelle verwendet werden, da dieser Ausdruck einen Wert vom Datentyp A zurückgibt. Dieser Datentyp liegt außerhalb des Bereichs der Datentypen, die vom aktuellen Formatelement vom Typ B unterstützt werden.

Die folgenden Schritte zeigen, wie dieses Problem auftreten kann.

1. Beginnen Sie gleichzeitig mit der Konfiguration der EB-Datenmodells und der EB-Formatkomponenten.
2. Fügen Sie im Datenmodellbaum ein Feld mit dem Namen **X** hinzu und wählen Sie **Integer** als Datentyp aus.
3. Fügen Sie im Formatstrukturbaum ein Formatelement vom Typ **Numerisch** hinzu.
4. Nennen Sie das neue Formatelement **Y**. Wählen Sie im Feld **Numerischer Typ** die Option **Integer** als Datentyp aus.
5. Binden Sie **X** an **Y**.
6. Ändern Sie im Formatstrukturbaum den Datentyp des Formatelements **Y** von **Integer** zu **Int64**.
7. Wählen Sie **Überprüfen** aus, um die bearbeitbare Formatkomponente auf der Seite **Formatdesigner** zu überprüfen.

    ![Überprüfen der Typkompatibilität auf der Seite „Formatdesigner“.](./media/er-components-inspections-02.gif)

8. Beachten Sie, dass ein Prüfungsfehler auftritt. Die Nachricht besagt, dass der konfigurierte Ausdruck nur Werte vom Typ **Int64** akzeptieren kann. Daher kann der Wert des Datenmodellfelds **X** vom Typ **Integer** nicht in das Formatelement **Y** eingegeben werden.

### <a name="automatic-resolution"></a>Automatische Lösung

Es ist keine Option verfügbar, um dieses Problem automatisch zu beheben.

### <a name="manual-resolution"></a>Manuelle Lösung

#### <a name="option-1"></a>Option 1

Aktualisieren Sie die Formatstruktur, indem Sie den Datentyp des Formatelements **Numerisch** so ändern, dass er mit dem Datentyp des Ausdrucks übereinstimmt, der für die Bindung dieses Elements konfiguriert ist. Im vorstehenden Beispiel muss der Wert **Numerischer Typ** des Formatelements **X** wieder zu **Integer** geändert werden.

#### <a name="option-2"></a>Option 2

Aktualisieren Sie die Formatzuordnung des Formatelements **X**, indem Sie den Ausdruck von `model.X` zu `INT64VALUE(model.X)` ändern.

## <a name="missing-configuration-element"></a><a id="i3"></a>Fehlendes Konfigurationselement

Die EB prüft, ob die Bindungsausdrücke nur Datenquellen enthalten, die in der bearbeitbaren EB-Komponente konfiguriert sind. Für jede Bindung, die eine Datenquelle enthält, die in der bearbeitbaren EB-Komponente fehlt, tritt im EB-Vorgangsdesigner oder im EB-Modellzuordnungsdesigner ein Prüfungsfehler auf.

Die folgenden Schritte zeigen, wie dieses Problem auftreten kann.

1. Beginnen Sie gleichzeitig mit der Konfiguration des EB-Datenmodells und der EB-Modellzuordnungskomponenten.
2. Fügen Sie im Datenmodellbaum ein Feld mit dem Namen **X** hinzu und wählen Sie **Integer** als Datentyp aus.

    ![Datenmodellbaum mit Feld „X“ und Datentyp „Integer“ auf der Seite „Datenmodell“.](./media/er-components-inspections-01.png)

3. Fügen Sie im Bereich **Datenquellen** des Modellzuordnungsdesigners eine Datenquelle vom Typ **Berechnetes Feld** hinzu.
4. Nennen Sie die neue Datenquelle **Y** und konfigurieren Sie sie so, dass sie den Ausdruck `INTVALUE(100)` enthält.
5. Binden Sie **X** an **Y**.
6. Löschen Sie im Modellzuordnungsdesigner im Bereich **Datenquellen** die Datenquelle **Y**.
7. Wählen Sie **Überprüfen** aus, um die bearbeitbare Modellzuordnungskomponente auf der Seite **Modellzuordnungsdesigner** zu überprüfen.

    ![Untersuchen der bearbeitbaren EB-Modellzuordnungskomponente auf der Seite „Modellzuordnungsdesigner“.](./media/er-components-inspections-03.gif)

8. Beachten Sie, dass ein Prüfungsfehler auftritt. Die Nachricht besagt, dass die Bindung des Datenmodellfelds **X** den Pfad enthält, der auf die Datenquelle **Y** verweist, diese Datenquelle jedoch nicht gefunden wurde.

### <a name="automatic-resolution"></a>Automatische Lösung

Wählen Sie **Bindung aufheben** aus, um dieses Problem automatisch zu beheben, indem die fehlende Datenquellenbindung entfernt wird.

### <a name="manual-resolution"></a>Manuelle Lösung

#### <a name="option-1"></a>Option 1

Heben Sie die Bindung für das Datenmodellfeld **X** auf, damit es nicht mehr auf das nicht vorhandene Datenquelle **Y** verweist.

#### <a name="option-2"></a>Option 2

Fügen Sie im Bereich **Datenquellen** des Modellzuordnungsdesigners erneut die Datenquelle **Y** hinzu.

## <a name="executability-of-an-expression-with-filter-function"></a><a id="i4"></a>Ausführbarkeit eines Ausdrucks mit FILTER-Funktion

Die in die EB integrierte [FILTER](er-functions-list-filter.md)-Funktion wird verwendet, um auf Anwendungstabellen, Ansichten oder Datenentitäten zuzugreifen, indem ein einzelner SQL-Aufruf getätigt wird, um die erforderlichen Daten als Liste von Datensätzen abzurufen. Eine Datenquelle vom Typ **Datensatzliste** wird als Argument dieser Funktion verwendet und gibt die Anwendungsquelle für den Aufruf an. Die EB prüft, ob eine direkte SQL-Abfrage an eine Datenquelle gerichtet werden kann, auf die in der `FILTER`-Funktion verwiesen wird. Wenn keine direkte Abfrage möglich ist, tritt im EB-Modellzuordnungsdesigner ein Prüfungsfehler auf. Die Nachricht, die Sie erhalten, besagt, dass der EB-Ausdruck, der die `FILTER`-Funktion enthält, nicht zur Laufzeit ausgeführt werden kann.

Die folgenden Schritte zeigen, wie dieses Problem auftreten kann.

1. Beginnen Sie mit der Konfiguration der EB-Modellzuordnungskomponente.
2. Fügen Sie eine Datenquelle vom Typ **Dynamics 365 for Operations \\ Tabellendatensätze** hinzu.
3. Nennen Sie die neue Datenquelle **Lieferant**. Wählen Sie im Feld **Tabelle** die Option **VendTable** aus, um anzugeben, dass diese Datenquelle die VendTable-Tabelle anfordert.
4. Fügen Sie eine Datenquelle vom Typ **Berechnetes Feld** hinzu.
5. Nennen Sie die neue Datenquelle **FilteredVendor** und konfigurieren Sie sie so, dass sie den Ausdruck `FILTER(Vendor, Vendor.AccountNum="US-101")` enthält.
6. Wählen Sie **Überprüfen** aus, um die bearbeitbare Modellzuordnungskomponente auf der Seite **Modellzuordnungsdesigner** zu überprüfen. Vergewissern Sie sich dann, ob der Ausdruck `FILTER(Vendor, Vendor.AccountNum="US-101")` in der Datenquelle **Liefernant** abgefragt werden kann.
7. Ändern Sie die Datenquelle **Lieferant**, indem sie ein verschachteltes Feld vom Typ **Berechnetes Feld** hinzufügen, um die gekürzte Lieferantenkontonummer abzurufen.
8. Nennen Sie die das verschachtelte Feld **$AccNumber** und konfigurieren Sie es so, dass es den Ausdruck `TRIM(Vendor.AccountNum)` enthält.
9. Wählen Sie **Überprüfen** aus, um die bearbeitbare Modellzuordnungskomponente auf der Seite **Modellzuordnungsdesigner** zu überprüfen. Vergewissern Sie sich dann, ob der Ausdruck `FILTER(Vendor, Vendor.AccountNum="US-101")` in der Datenquelle **Liefernant** abgefragt werden kann.

    ![Überprüfen Sie, ob der Ausdruck mit der Funktion FILTER auf der Designerseite für die Modellzuordnung abgefragt werden kann.](./media/er-components-inspections-04.gif)

10. Beachten Sie, dass ein Prüfungsfehler auftritt, da die Datenquelle **Lieferant** ein verschachteltes Feld vom Typ **Berechnetes Feld** enthält, das nicht zulässt, dass der Ausdruck aus der Datenquelle **FilteredVendor** in die direkte SQL-Anweisung übersetzt wird.

Die folgende Abbildung zeigt den Laufzeitfehler, der auftritt, wenn Sie die Warnung ignorieren und **Ausführen** auswählen, um ein Format auszuführen, das für die Verwendung der Modellzuordnung konfiguriert ist.

![Laufzeitfehler, die auftreten, wenn Sie das bearbeitbare Format auf der Seite „Formatdesigner“ ausführen.](./media/er-components-inspections-04a.png)

### <a name="automatic-resolution"></a>Automatische Lösung

Es ist keine Option verfügbar, um dieses Problem automatisch zu beheben.

### <a name="manual-resolution"></a>Manuelle Lösung

#### <a name="option-1"></a>Option 1

Anstatt ein verschachteltes Feld vom Typ **Berechnetes Feld** zur Datenquelle **Lieferant** hinzuzufügen, fügen Sie das verschachtelte Feld **$AccNumber** zur Datenquelle **FilteredVendor** hinzu und konfigurieren es so, dass es den Ausdruck `TRIM(FilteredVendor.AccountNum)` enthält. Auf diese Weise kann der Ausdruck `FILTER(Vendor, Vendor.AccountNum="US-101")` auf SQL-Ebene ausgeführt werden und das verschachtelte Feld **$AccNumber** danach berechnen.

#### <a name="option-2"></a>Option 2

Ändern Sie den Ausdruck der Datenquelle **FilteredVendor** von `FILTER(Vendor, Vendor.AccountNum="US-101")` zu `WHERE(Vendor, Vendor.AccountNum="US-101")`. Es wird nicht empfohlen, den Ausdruck für eine Tabelle mit einem großen Datenvolumen (Transaktionstabelle) zu ändern, da alle Datensätze abgerufen werden und die Auswahl der erforderlichen Datensätze im Speicher erfolgt. Daher kann dieser Ansatz eine Verschlechterung der Leistung verursachen. Weitere Informationen finden Sie unter [WHERE EB-Funktion](er-functions-list-where.md).

## <a name="executability-of-a-groupby-data-source"></a><a id="i5"></a>Ausführbarkeit einer GROUPBY-Datenquelle

Die **GROUPBY**-Datenquelle unterteilt das Abfrageergebnis in Gruppen von Datensätzen, normalerweise zum Zweck einer oder mehrerer Aggregationen für jede Gruppe. Jede **GROUPBY**-Datenquelle kann so konfiguriert werden, dass sie entweder auf Datenbankebene oder im Speicher ausgeführt wird. Wenn eine **GROUPBY**-Datenquelle so konfiguriert ist, dass sie auf Datenbankebene ausgeführt wird, prüft die EB, ob eine direkte SQL-Abfrage für eine Datenquelle eingerichtet werden kann, auf die in dieser Datenquelle verwiesen wird. Wenn keine direkte Abfrage möglich ist, tritt im EB-Modellzuordnungsdesigner ein Prüfungsfehler auf. Die Nachricht, die Sie erhalten, besagt, dass die konfigurierte **GROUPBY**-Datenquelle nicht zur Laufzeit ausgeführt werden kann.

Die folgenden Schritte zeigen, wie dieses Problem auftreten kann.

1. Beginnen Sie mit der Konfiguration der EB-Modellzuordnungskomponente.
2. Fügen Sie eine Datenquelle vom Typ **Dynamics 365 for Operations \\ Tabellendatensätze** hinzu.
3. Nennen Sie die neue Datenquelle **Trans**. Wählen Sie im Feld **Tabelle** die Option **VendTrans** aus, um anzugeben, dass diese Datenquelle die VendTrans-Tabelle anfordert.
4. Fügen Sie eine Datenquelle vom Typ **Gruppieren nach** hinzu.
5. Nennen Sie die neue Datenquelle **GroupedTrans** und konfigurieren Sie sie folgendermaßen:

    - Wählen Sie die Datenquelle **Trans** als Quelle für Datensätze aus, die gruppiert werden sollen.
    - Wählen Sie im Feld **Ausführungsort** die Option **Abfrage** aus, um anzugeben, dass Sie diese Datenquelle auf Datenbankebene ausführen möchten.

    ![Konfigurieren der Datenquelle auf der Seite „Parameter für „Gruppieren nach“ bearbeiten“.](./media/er-components-inspections-05a.gif)

6. Wählen Sie **Überprüfen** aus, um die bearbeitbare Modellzuordnungskomponente auf der Seite **Modellzuordnungsdesigner** zu überprüfen. Vergewissern Sie sich dann, ob die konfigurierte Datenquelle **GroupedTrans** abgefragt werden kann.
7. Ändern Sie die Datenquelle **Trans**, indem sie ein verschachteltes Feld vom Typ **Berechnetes Feld** hinzufügen, um die gekürzte Lieferantenkontonummer abzurufen.
8. Nennen Sie die neue Datenquelle **$AccNumber** und konfigurieren Sie sie so, dass sie den Ausdruck `TRIM(Trans.AccountNum)` enthält.

    ![Konfigurieren der Datenquelle auf der Seite „Modellzuordnungsdesigner“.](./media/er-components-inspections-05a.png)

9. Wählen Sie **Überprüfen** aus, um die bearbeitbare Modellzuordnungskomponente auf der Seite **Modellzuordnungsdesigner** zu überprüfen. Vergewissern Sie sich dann, ob die konfigurierte Datenquelle **GroupedTrans** abgefragt werden kann.

    ![Überprüfen der EB-Modellzuordnungskomponente und Sicherstellen, dass die Datenquelle „GroupedTrans“ auf der Seite „Modellzuordnungsdesigner“ abgefragt werden kann.](./media/er-components-inspections-05b.png)

10. Beachten Sie, dass ein Prüfungsfehler auftritt, da die Datenquelle **Trans** ein verschachteltes Feld vom Typ **Berechnetes Feld** enthält, das nicht zulässt, dass die Datenquelle **GroupedTrans** in die direkte SQL-Anweisung übersetzt wird.

Die folgende Abbildung zeigt den Laufzeitfehler, der auftritt, wenn Sie die Warnung ignorieren und **Ausführen** auswählen, um ein Format auszuführen, das für die Verwendung der Modellzuordnung konfiguriert ist.

![Auftretende Laufzeitfehler, wenn die Warnung auf der Seite „Formatdesigner“ ignoriert wird.](./media/er-components-inspections-05c.png)

### <a name="automatic-resolution"></a>Automatische Lösung

Es ist keine Option verfügbar, um dieses Problem automatisch zu beheben.

### <a name="manual-resolution"></a>Manuelle Lösung

#### <a name="option-1"></a>Option 1

Anstatt ein verschachteltes Feld vom Typ **Berechnetes Feld** zur Datenquelle **Trans** hinzuzufügen, fügen Sie das verschachtelte Feld **$AccNumber** für das Element **GroupedTrans.lines** zur Datenquelle **GroupedTrans** hinzu und konfigurieren es so, dass es den Ausdruck `TRIM(GroupedTrans.lines.AccountNum)` enthält. Auf diese Weise kann die Datenquelle **GroupedTrans** auf SQL-Ebene ausgeführt werden und das verschachtelte Feld **$AccNumber** danach berechnen.

#### <a name="option-2"></a>Option 2

Ändern Sie den Wert des Felds **Ausführungsort** für die Datenquelle **GroupedTrans** von **Abfrage** zu **Im Speicher**. Es wird nicht empfohlen, den Wert für eine Tabelle mit einem großen Datenvolumen (Transaktionstabelle) zu ändern, da alle Datensätze abgerufen werden und die Gruppierung und Aggregation im Speicher erfolgen. Daher kann dieser Ansatz eine Verschlechterung der Leistung verursachen.

## <a name="executability-of-a-join-data-source"></a><a id="i6"></a>Ausführbarkeit einer JOIN-Datenquelle

Die [JOIN](er-join-data-sources.md)-Datenquelle kombiniert Datensätze aus zwei oder mehr Datenbanktabellen basierend auf verwandten Feldern. Jede **JOIN**-Datenquelle kann so konfiguriert werden, dass sie entweder auf Datenbankebene oder im Speicher ausgeführt wird. Wenn eine **JOIN**-Datenquelle so konfiguriert ist, dass sie auf Datenbankebene ausgeführt wird, prüft die EB, ob eine direkte SQL-Abfrage für Datenquellen eingerichtet werden kann, auf die in dieser Datenquelle verwiesen wird. Wenn keine direkte SQL-Abfrage mit mindestens einer der referenzierten Datenquellen möglich ist, tritt im EB-Modellzuordnungsdesigner ein Prüfungsfehler auf. Die Nachricht, die Sie erhalten, besagt, dass die konfigurierte **JOIN**-Datenquelle nicht zur Laufzeit ausgeführt werden kann.

Die folgenden Schritte zeigen, wie dieses Problem auftreten kann.

1. Beginnen Sie mit der Konfiguration der EB-Modellzuordnungskomponente.
2. Fügen Sie eine Datenquelle vom Typ **Dynamics 365 for Operations \\ Tabellendatensätze** hinzu.
3. Nennen Sie die neue Datenquelle **Lieferant**. Wählen Sie im Feld **Tabelle** die Option **VendTable** aus, um anzugeben, dass diese Datenquelle die VendTable-Tabelle anfordert.
4. Fügen Sie eine Datenquelle vom Typ **Dynamics 365 for Operations \\ Tabellendatensätze** hinzu.
5. Nennen Sie die neue Datenquelle **Trans**. Wählen Sie im Feld **Tabelle** die Option **VendTrans** aus, um anzugeben, dass diese Datenquelle die VendTrans-Tabelle anfordert.
6. Fügen Sie eine Datenquelle vom Typ **Berechnetes Feld** als verschachteltes Feld der Datenquelle **Lieferant** hinzu.
7. Nennen Sie die neue Datenquelle **FilteredTrans** und konfigurieren Sie sie so, dass sie den Ausdruck `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)` enthält.
8. Fügen Sie eine Datenquelle vom Typ **Join** hinzu.
9. Nennen Sie die neue Datenquelle **JoinedList** und konfigurieren Sie sie folgendermaßen:

    1. Fügen Sie die Datenquelle **Lieferant** als den ersten Satz Datensätze hinzu, die verknüpft werden sollen.
    2. Fügen Sie die Datenquelle **Vendor.FilteredTrans** als den zweiten Satz Datensätze hinzu, die verknüpft werden sollen. Wählen Sie **INNER** als Typ aus.
    3. Wählen Sie im Feld **Ausführen** die Option **Abfrage** aus, um anzugeben, dass Sie diese Datenquelle auf Datenbankebene ausführen möchten.

    ![Konfigurieren der Datenquelle auf der Seite „Verknüpfungsdesigner“.](./media/er-components-inspections-06a.gif)

10. Wählen Sie **Überprüfen** aus, um die bearbeitbare Modellzuordnungskomponente auf der Seite **Modellzuordnungsdesigner** zu überprüfen. Vergewissern Sie sich dann, ob die konfigurierte Datenquelle **JoinedList** abgefragt werden kann.
11. Ändern Sie den Ausdruck der Datenquelle **Vendor.FilteredTrans** von `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)` zu `WHERE(Trans, Trans.AccountNum=Vendor.AccountNum)`.
12. Wählen Sie **Überprüfen** aus, um die bearbeitbare Modellzuordnungskomponente auf der Seite **Modellzuordnungsdesigner** zu überprüfen. Vergewissern Sie sich dann, ob die konfigurierte Datenquelle **JoinedList** abgefragt werden kann.

    ![Überprüfen der bearbeitbaren Modellzuordnungskomponente und Sicherstellen, dass die konfigurierte Datenquelle „JoinedList“ auf der Seite „Modellzuordnungsdesigner“ abgefragt werden kann.](./media/er-components-inspections-06b.png)

13. Beachten Sie, dass ein Prüfungsfehler auftritt, da der Ausdruck der Datenquelle **Vendor.FilteredTrans** nicht in den direkten SQL-Aufruf übersetzt werden kann. Darüber hinaus erlaubt der direkte SQL-Aufruf nicht den Aufruf der Datenquelle **JoinedList**, die in die direkte SQL-Anweisung übersetzt werden soll.

    ![Laufzeitfehler aufgrund der fehlgeschlagenen Prüfung der Datenquelle „JoinedList“ auf der Seite „Modellzuordnungsdesigner“.](./media/er-components-inspections-06c.png)

Die folgende Abbildung zeigt den Laufzeitfehler, der auftritt, wenn Sie die Warnung ignorieren und **Ausführen** auswählen, um ein Format auszuführen, das für die Verwendung der Modellzuordnung konfiguriert ist.

![Ausführen des bearbeitbaren Formats auf der Seite „Formatdesigner“.](./media/er-components-inspections-06e.png)

### <a name="automatic-resolution"></a>Automatische Lösung

Es ist keine Option verfügbar, um dieses Problem automatisch zu beheben.

### <a name="manual-resolution"></a>Manuelle Lösung

#### <a name="option-1"></a>Option 1

Ändern Sie den Ausdruck der Datenquelle **Vendor.FilteredTrans** von `WHERE(Trans, Trans.AccountNum=Vendor.AccountNum)` zurück zu `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)`, wie es die Warnung vorschlug.

![Aktualisierter Ausdruck der Datenquelle auf der Seite „Modellzuordnungsdesigner“.](./media/er-components-inspections-06d.png)

#### <a name="option-2"></a>Option 2

Ändern Sie den Wert des Felds **Ausführung** für die Datenquelle **JoinedList** von **Abfrage** zu **Im Speicher**. Es wird nicht empfohlen, den Wert für eine Tabelle mit einem großen Datenvolumen (Transaktionstabelle) zu ändern, da alle Datensätze abgerufen werden und die Verknüpfung im Speicher erfolgt. Daher kann dieser Ansatz eine Verschlechterung der Leistung verursachen. Eine Prüfungswarnung informiert Sie über dieses Risiko.

## <a name="preferability-of-filter-vs-where-function"></a><a id="i7"></a>Bevorzugung der FILTER- gegenüber der WHERE-Funktion

Die in die EB integrierte [FILTER](er-functions-list-filter.md)-Funktion wird verwendet, um auf Anwendungstabellen, Ansichten oder Datenentitäten zuzugreifen, indem ein einzelner SQL-Aufruf getätigt wird, um die erforderlichen Daten als Liste von Datensätzen abzurufen. Die [WHERE](er-functions-list-where.md)-Funktion ruft alle Datensätze aus der angegebenen Quelle ab und führt die Datensatzauswahl im Speicher durch. Eine Datenquelle vom Typ **Datensatzliste** wird als Argument beider Funktionen verwendet und gibt eine Quelle für das Abrufen von Datensätzen an. Die EB prüft, ob ein direkter SQL-Aufruf an eine Datenquelle gerichtet werden kann, auf die in der **WHERE**-Funktion verwiesen wird. Wenn kein direkter Aufruf möglich ist, tritt im EB-Modellzuordnungsdesigner eine Prüfungswarnung auf. Die Nachricht, die Sie erhalten, empfiehlt, die **FILTER**-Funktion anstelle der **WHERE**-Funktion zur Verbesserung der Effizienz zu verwenden.

Die folgenden Schritte zeigen, wie dieses Problem auftreten kann.

1. Beginnen Sie mit der Konfiguration der EB-Modellzuordnungskomponente.
2. Fügen Sie eine Datenquelle vom Typ **Dynamics 365 for Operations \\ Tabellendatensätze** hinzu.
3. Nennen Sie die neue Datenquelle **Trans**. Wählen Sie im Feld **Tabelle** die Option **VendTrans** aus, um anzugeben, dass diese Datenquelle die VendTrans-Tabelle anfordert.
4. Fügen Sie eine Datenquelle vom Typ **Berechnetes Feld** als verschachteltes Feld der Datenquelle **Lieferant** hinzu.
5. Nennen Sie die neue Datenquelle **FilteredTrans** und konfigurieren Sie sie so, dass sie den Ausdruck `WHERE(Trans, Trans.AccountNum="US-101")` enthält.
6. Fügen Sie eine Datenquelle vom Typ **Dynamics 365 for Operations \\ Tabellendatensätze** hinzu.
7. Nennen Sie die neue Datenquelle **Lieferant**. Wählen Sie im Feld **Tabelle** die Option **VendTable** aus, um anzugeben, dass diese Datenquelle die VendTable-Tabelle anfordert.
8. Fügen Sie eine Datenquelle vom Typ **Berechnetes Feld** hinzu.
9. Nennen Sie die neue Datenquelle **FilteredVendor** und konfigurieren Sie sie so, dass sie den Ausdruck `WHERE(Vendor, Vendor.AccountNum="US-101")` enthält.
10. Wählen Sie **Überprüfen** aus, um die bearbeitbare Modellzuordnungskomponente auf der Seite **Modellzuordnungsdesigner** zu überprüfen.

    ![Untersuchen der bearbeitbaren Modellzuordnungskomponente auf der Seite „Modellzuordnungsdesigner“.](./media/er-components-inspections-07a.png)

11. Beachten Sie, dass Prüfungswarnungen die Verwendung der **FILTER**-Funktion anstelle der **WHERE**-Funktion für die Datenquellen **FilteredVendor** und **FilteredTrans** empfehlen.

    ![Empfehlung zur Nutzung der FILTER-Funktion anstelle der WHERE-Funktion auf der Seite „Modellzuordnungsdesigner“.](./media/er-components-inspections-07b.png)

### <a name="automatic-resolution"></a>Automatische Lösung

Wählen Sie **Beheben** aus, um die **WHERE**-Funktion automatisch durch die **FILTER**-Funktion zu ersetzen im Ausdruck aller Datenquellen, die im Raster auf der Registerkarte **Warnungen** für diese Art der Überprüfung angezeigt werden.

Alternativ können Sie die Zeile für eine einzelne Warnung im Raster auswählen und dann **Ausgewählte beheben** auswählen. In diesem Fall wird der Ausdruck automatisch nur in der Datenquelle geändert, die in der ausgewählten Warnung angegeben ist.

![Auswählen von „Beheben“, um die WHERE-Funktion auf der Seite „Modellzuordnungsdesigner“ automatisch durch die FILTER-Funktion zu ersetzen.](./media/er-components-inspections-07c.png)

### <a name="manual-resolution"></a>Manuelle Lösung

Sie können die Ausdrücke aller Datenquellen im Prüfungsraster manuell anpassen, indem Sie die **WHERE**-Funktion durch die **FILTER**-Funktion ersetzen.

## <a name="preferability-of-allitemsquery-vs-allitems-function"></a><a id="i8"></a>Bevorzugung der ALLITEMSQUERY- gegenüber der ALLITEMS-Funktion

Die integrierten EB-Funktionen [ALLITEMS](er-functions-list-allitems.md) und [ALLITEMSQUERY](er-functions-list-allitemsquery.md) geben einen vereinfachten Wert von **Datensatzliste** zurück, der aus einer Liste von Datensätzen besteht, die alle Elemente darstellen, die dem angegebenen Pfad entsprechen. Die EB prüft, ob ein direkter SQL-Aufruf an eine Datenquelle gerichtet werden kann, auf die in der **ALLITEMS**-Funktion verwiesen wird. Wenn kein direkter Aufruf möglich ist, tritt im EB-Modellzuordnungsdesigner eine Prüfungswarnung auf. Die Nachricht, die Sie erhalten, empfiehlt, die **ALLITEMSQUERY**-Funktion anstelle der **ALLITEMS**-Funktion zur Verbesserung der Effizienz zu verwenden.

Die folgenden Schritte zeigen, wie dieses Problem auftreten kann.

1. Beginnen Sie mit der Konfiguration der EB-Modellzuordnungskomponente.
2. Fügen Sie eine Datenquelle vom Typ **Dynamics 365 for Operations \\ Tabellendatensätze** hinzu.
3. Nennen Sie die neue Datenquelle **Lieferant**. Wählen Sie im Feld **Tabelle** die Option **VendTable** aus, um anzugeben, dass diese Datenquelle die VendTable-Tabelle anfordert.
4. Fügen Sie eine Datenquelle vom Typ **Berechnetes Feld** hinzu, um Datensätze für mehrere Lieferanten zu erhalten.
5. Nennen Sie die neue Datenquelle **FilteredVendor** und konfigurieren Sie sie so, dass sie den Ausdruck `FILTER(Vendor, OR(Vendor.AccountNum="US-101",Vendor.AccountNum="US-102"))` enthält.
6. Fügen Sie eine Datenquelle vom Typ **Berechnetes Feld** hinzu, um die Transaktionen aller gefilterten Kreditoren zu erhalten.
7. Nennen Sie die neue Datenquelle **FilteredVendorTrans** und konfigurieren Sie sie so, dass sie den Ausdruck `ALLITEMS(FilteredVendor.'<Relations'.'VendTrans.VendTable_AccountNum')` enthält.
8. Wählen Sie **Überprüfen** aus, um die bearbeitbare Modellzuordnungskomponente auf der Seite **Modellzuordnungsdesigner** zu überprüfen.

    ![Untersuchen der bearbeitbaren Modellzuordnungskomponente auf der Seite „Modellzuordnungsdesigner“.](./media/er-components-inspections-08a.png)

9. Beachten Sie, dass eine Prüfungswarnung auftritt. Die Nachricht empfiehlt, die **ALLITEMSQUERY**-Funktion anstelle der **ALLITEMS**-Funktion für die Datenquelle **FilteredVendorTrans** zu verwenden.

    ![Empfehlung zur Nutzung der ALLITEMSQUERY-Funktion anstelle der ALLITEMS-Funktion auf der Seite „Modellzuordnungsdesigner“.](./media/er-components-inspections-08b.png)

### <a name="automatic-resolution"></a>Automatische Lösung

Wählen Sie **Beheben** aus, um die **ALLITEMS**-Funktion automatisch durch die **ALLITEMSQUERY**-Funktion zu ersetzen im Ausdruck aller Datenquellen, die im Raster auf der Registerkarte **Warnungen** für diese Art der Überprüfung angezeigt werden.

Alternativ können Sie die Zeile für eine einzelne Warnung im Raster auswählen und dann **Ausgewählte beheben** auswählen. In diesem Fall wird der Ausdruck automatisch nur in der Datenquelle geändert, die in der ausgewählten Warnung angegeben ist.

![Auswählen von „Beheben“ auf der Seite „Modellzuordnungsdesigner“.](./media/er-components-inspections-08c.png)

### <a name="manual-resolution"></a>Manuelle Lösung

Sie können die Ausdrücke aller im Prüfungsraster genannten Datenquellen manuell anpassen, indem Sie die **ALLITEMS**-Funktion durch die **ALLITEMSQUERY**-Funktion ersetzen.

## <a name="consideration-of-empty-list-cases"></a><a id="i9"></a>Berücksichtigung leerer Listenfälle

Sie können Ihr EB-Format oder Ihre Modellzuordnungskomponente so konfigurieren, dass der Feldwert aus einer Datenquelle vom Typ **Datensatzliste** abgerufen wird. Die EB überprüft, ob Ihr Entwurf den Fall berücksichtigt, dass eine aufgerufene Datenquelle keine Datensätze enthält (d. h., dass sie leer ist), um Laufzeitfehler zu vermeiden, wenn ein Wert aus einem Feld eines nicht vorhandenen Datensatzes abgerufen wird.

Die folgenden Schritte zeigen, wie dieses Problem auftreten kann.

1. Beginnen Sie gleichzeitig mit der Konfiguration der EB-Datenmodell-, der EB-Modellzuordnungs- und der EB-Formatkomponenten.
2. Fügen Sie im Datenmodellbaum ein Stammelement mit dem Namen **Root3** hinzu.
3. Ändern Sie das Element **Root3**, indem Sie ein verschachteltes Element vom Typ **Datensatzliste** hinzufügen.
4. Nennen Sie das neue verschachtelte Element **Lieferant**.
5. Ändern Sie das Element **Lieferant** auf folgende Weise:

    - Fügen Sie ein verschachteltes Feld vom Typ **Zeichenfolge** hinzu und nennen Sie es **Name**.
    - Fügen Sie ein verschachteltes Feld vom Typ **Zeichenfolge** hinzu und nennen Sie es **AccountNumber**.

    ![Hinzufügen verschachtelter Felder auf der Seite „Datenmodell“.](./media/er-components-inspections-09a.png)

6. Fügen Sie im Bereich **Datenquellen** des Modellzuordnungsdesigners eine Datenquelle vom Typ **Dynamics 365 for Operations \\ Tabellendatensätze** hinzu.
7. Nennen Sie die neue Datenquelle **Lieferant**. Wählen Sie im Feld **Tabelle** die Option **VendTable** aus, um anzugeben, dass diese Datenquelle die VendTable-Tabelle anfordert.
8. Fügen Sie eine Datenquelle vom Typ **Allgemein \\ Benutzereingabeparameter** hinzu, um im Dialogfeld zur Laufzeit nach einem Lieferantenkonto zu suchen.
9. Nennen Sie die neue Datenquelle **RequestedAccountNum**. Geben Sie in das Feld **Beschriftung** den Text **Lieferantenkontonummer** ein. Behalten Sie im Feld **Name des Betriebsdatentyps** den Standardwert **Beschreibung** bei.
10. Fügen Sie eine Datenquelle vom Typ **Berechnetes Feld** hinzu, um nach einem Lieferanten zu filtern, zu dem eine Abfrage durchgeführt wird.
11. Nennen Sie die neue Datenquelle **FilteredVendor** und konfigurieren Sie sie so, dass sie den Ausdruck `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)` enthält.
12. Binden Sie die Datenmodellelemente wie folgt an konfigurierte Datenquellen:

    - Binden Sie **FilteredVendor** an **Lieferant**.
    - Binden Sie **FilteredVendor.AccountNum** an **Vendor.AccountNumber**.
    - Binden Sie **FilteredVendor.'name()'** an **Vendor.Name**.

    ![Binden der Datenmodellelemente auf der Seite „Modellzuordnungsdesigner“.](./media/er-components-inspections-09b.png)

13. Fügen Sie im Formatstrukturbaum die folgenden Elemente hinzu, um ein ausgehendes Dokument im XML-Format zu generieren, das die Lieferantendetails enthält:

    1. Fügen Sie das Root-XML-Element **Anweisung** hinzu.
    2. Fügen Sie für das XML-Element **Anweisung** das verschachtelte XML-Element **Partei** hinzu.
    3. Fügen Sie für das XML-Element **Partei** die folgenden verschachtelten XML-Attribute hinzu.

        - Name
        - AccountNum

14. Binden Sie Formatelemente auf die folgende Weise an bereitgestellte Datenquellen:

    - Binden Sie das Formatelement **Anweisung\\Partei\\Name** an das Datenquellenfeld **model.Vendor.Name**.
    - Binden Sie das Formatelement **Anweisung\\Partei\\AccountNum** an das Datenquellenfeld **model.Vendor.AccountNumber**.

15. Wählen Sie **Überprüfen** aus, um die bearbeitbare Formatkomponente auf der Seite **Formatdesigner** zu überprüfen.

    ![Überprüfen der Formatelemente, die Sie auf der Seite „Formatdesigner“ an Datenquellen gebunden haben.](./media/er-components-inspections-09c.png)

16. Beachten Sie, dass ein Prüfungsfehler auftritt. Die Nachricht besagt, dass zur Laufzeit möglicherweise ein Fehler für die konfigurierten Formatkomponenten **Anweisung\\Partei\\Name** und **Anweisung\\Partei\\AccountNum** auftritt, wenn die Liste `model.Vendor` leer ist.

    ![Prüfungsfehler hinsichtlich eines möglichen Fehlers bei den konfigurierten Formatkomponenten.](./media/er-components-inspections-09d.png)

Die folgende Abbildung zeigt den Laufzeitfehler, der auftritt, wenn Sie die Warnung ignorieren, für das Format **Ausführen** auswählen und die Kontonummer eines nicht existierenden Lieferanten auswählen. Da der angeforderte Kreditor nicht existiert, wird die Liste `model.Vendor` leer sein (d. h., sie enthält keine Datensätze).

![Laufzeitfehler, die während der Ausführung der Formatzuordnung auftreten.](./media/er-components-inspections-09e.png)

### <a name="automatic-resolution"></a>Automatische Lösung

Für die ausgewählte Zeile im Raster auf der Registerkarte **Warnungen** können Sie **Bindung aufheben** auswählen. Die Bindung, auf die in der Spalte **Pfad** verwiesen wird, wird automatisch aus den Formatelementen entfernt.

### <a name="manual-resolution"></a>Manuelle Lösung

#### <a name="option-1"></a>Option 1

Sie können das Formatelement **Anweisung\\Partei\\Name** an das Datenquellenelement `model.Vendor` binden. Zur Laufzeit ruft diese Bindung zuerst die Datenquelle `model.Vendor` auf. Wenn `model.Vendor` eine leere Datensatzliste zurückgibt, werden die verschachtelten Formatelemente nicht ausgeführt. Daher treten für diese Formatkonfiguration keine Prüfungswarnungen auf.

![Binden des Formatelements an das Datenquellenelement auf der Seite „Formatdesigner“.](./media/er-components-inspections-09e.gif)

#### <a name="option-2"></a>Option 2

Ändern Sie die Bindung des Formatelements **Anweisung\\Partei\\Name** von `model.Vendor.Name` zu `FIRSTORNULL(model.Vendor).Name`. Die aktualisierte Bindung konvertiert bedingt den ersten Datensatz der Datenquelle `model.Vendor` vom Typ **Datensatzliste** an eine neue Datenquelle vom Typ **Datensatz**. Diese neue Datenquelle enthält denselben Satz von Feldern.

- Wenn mindestens ein Datensatz in der Datenquelle `model.Vendor` verfügbar ist, werden die Felder dieses Datensatzes mit den Werten der Felder des ersten Datensatzes der Datenquelle `model.Vendor` gefüllt. In diesem Fall gibt die aktualisierte Bindung den Lieferantennamen zurück.
- Andernfalls wird jedes Feld des erstellten Datensatzes mit dem Standardwert für den Datentyp dieses Felds gefüllt. In diesem Fall wird die leere Zeichenfolge als Standardwert für den Datentyp **Zeichenfolge** zurückgegeben.

Daher treten für das Formatelement **Anweisung\\Partei\\Name** keine Prüfungswarnungen auf, wenn es an den Ausdruck `FIRSTORNULL(model.Vendor).Name` gebunden ist.

![Geänderte Bindung löst Prüfungswarnungen auf der Seite „Formatdesigner“.](./media/er-components-inspections-09f.gif)

#### <a name="option-3"></a>Option 3

Wenn Sie die Daten, die in ein generiertes Dokument eingegeben werden, explizit angeben möchten, wenn die Datenquelle `model.Vendor` vom Typ **Datensatzliste** keine Datensätze zurückgibt (in diesem Beispiel den Text **Nicht verfügbar**), ändern Sie die Bindung des Formatelements **Anweisung\\Partei\\Name** von `model.Vendor.Name` in `IF(NOT(ISEMPTY(model.Vendor)), model.Vendor.Name, "Not available")`. Sie können auch den Ausdruck `IF(COUNT(model.Vendor)=0, model.Vendor.Name, "Not available")` verwenden.

### <a name="additional-consideration"></a><a id="i9a"></a>Zusätzliche Überlegung

Die Inspektion warnt Sie auch vor einem anderen potenziellen Problem. Wenn Sie die Formatelemente **Anweisung\\Partei\\Name** und **Anweisung\\Partei\\AccountNum** an die entsprechenden Felder der Datenquelle `model.Vendor` vom Typ **Datensatzliste** binden, werden diese Bindungen standardmäßig ausgeführt und verwenden die Werte aus den entsprechenden Feldern des ersten Datensatzes aus der Datenquelle `model.Vendor`, falls diese Liste nicht leer ist.

Da Sie das Formatelement **Anweisung\\Partei** nicht an die Datenquelle `model.Vendor` gebunden haben, wird das Element **Anweisung\\Partei** während der Formatausführung nicht für jeden Datensatz der Datenquelle `model.Vendor` wiederholt. Stattdessen wird ein generiertes Dokument nur mit Informationen aus dem ersten Datensatz der Datensatzliste gefüllt, wenn diese Liste mehrere Datensätze enthält. Daher kann ein Problem auftreten, wenn das Format ein generiertes Dokument mit Informationen zu allen Lieferanten aus der Datenquelle `model.Vendor` füllen soll. Um dieses Problem zu beheben, binden Sie das Element **Anweisung\\Partei** an die Datenquelle `model.Vendor`.

## <a name="executability-of-an-expression-with-filter-function-caching"></a><a id="i10"></a>Ausführbarkeit eines Ausdrucks mit FILTER-Funktion (Zwischenspeicherung)

Mehrere integrierte EB-Funktionen, einschließlich [FILTER](er-functions-list-filter.md) und [ALLITEMSQUERY](er-functions-list-allitemsquery.md), werden verwendet, um auf Anwendungstabellen, Ansichten oder Datenentitäten zuzugreifen, indem ein einzelner SQL-Aufruf getätigt wird, um die erforderlichen Daten als Liste von Datensätzen abzurufen. Eine Datenquelle vom Typ **Datensatzliste** wird als Argument für jede dieser Funktionen verwendet und gibt eine Anwendungsquelle für den Aufruf an. Die EB prüft, ob ein direkter SQL-Aufruf an eine Datenquelle gerichtet werden kann, auf die in einer dieser Funktionen verwiesen wird. Wenn kein direkter Aufruf möglich ist, weil die Datenquelle als [zwischengespeichert](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace) gekennzeichnet wurde, tritt im EB-Modellzuordnungsdesigner ein Prüfungsfehler auf. Die Nachricht, die Sie erhalten, besagt, dass der EB-Ausdruck, der eine dieser Funktionen enthält, nicht zur Laufzeit ausgeführt werden kann.

Die folgenden Schritte zeigen, wie dieses Problem auftreten kann.

1. Beginnen Sie mit der Konfiguration der EB-Modellzuordnungskomponente.
2. Fügen Sie eine Datenquelle vom Typ **Dynamics 365 for Operations \\ Tabellendatensätze** hinzu.
3. Nennen Sie die neue Datenquelle **Lieferant**. Wählen Sie im Feld **Tabelle** die Option **VendTable** aus, um anzugeben, dass diese Datenquelle die VendTable-Tabelle anfordert.
4. Fügen Sie eine Datenquelle vom Typ **Allgemein \\ Benutzereingabeparameter** hinzu, um im Dialogfeld zur Laufzeit nach einem Lieferantenkonto zu suchen.
5. Nennen Sie die neue Datenquelle **RequestedAccountNum**. Geben Sie in das Feld **Beschriftung** den Text **Lieferantenkontonummer** ein. Behalten Sie im Feld **Name des Betriebsdatentyps** den Standardwert **Beschreibung** bei.
6. Fügen Sie eine Datenquelle vom Typ **Berechnetes Feld** hinzu, um nach einem Lieferanten zu filtern, zu dem eine Abfrage durchgeführt wird.
7. Nennen Sie die neue Datenquelle **FilteredVendor** und konfigurieren Sie sie so, dass sie den Ausdruck `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)` enthält.
8. Markieren Sie die konfigurierte Datenquelle **Lieferant** als zwischengespeichert.

    ![Konfigurieren der Modellzuordnungskomponente auf der Seite „Modellzuordnungsdesigner“.](./media/er-components-inspections-10a.gif)

9. Wählen Sie **Überprüfen** aus, um die bearbeitbare Modellzuordnungskomponente auf der Seite **Modellzuordnungsdesigner** zu überprüfen.

    ![Überprüfen der FILTER-Funktion, die auf die Datenquelle „Kreditor“ im Zwischenspeicher auf der Seite „Modellzuordnungsdesigner“ angewendet wird.](./media/er-components-inspections-10a.png)

10. Beachten Sie, dass ein Prüfungsfehler auftritt. Die Nachricht besagt, dass die **FILTER**-Funktion nicht auf die zwischengespeicherte Datenquelle **Lieferant** angewendet werden kann.

Die folgende Abbildung zeigt den Laufzeitfehler, der auftritt, wenn Sie die Warnung ignorieren und **Ausführen** auswählen, um das Format auszuführen.

![Laufzeitfehler, der während der Ausführung der Formatzuordnung auf der Seite „Formatdesigner“ auftritt.](./media/er-components-inspections-10b.png)

### <a name="automatic-resolution"></a>Automatische Lösung

Es ist keine Option verfügbar, um dieses Problem automatisch zu beheben.

### <a name="manual-resolution"></a>Manuelle Lösung

#### <a name="option-1"></a>Option 1

Entfernen Sie die Markierung **Zwischenspeicher** aus der Datenquelle **Lieferant**. Die Datenquelle **FilteredVendor** wird dann ausführbar, aber auf die Datenquelle **Lieferant**, auf die in der VendTable-Tabelle verwiesen wird, wird jedes Mal zugegriffen, wenn die Datenquelle **FilteredVendor** aufgerufen wird.

#### <a name="option-2"></a>Option 2

Ändern Sie den Ausdruck der Datenquelle **FilteredVendor** von `FILTER(Vendor, Vendor.AccountNum="US-101")` zu `WHERE(Vendor, Vendor.AccountNum="US-101")`. In diesem Fall wird auf die Datenquelle **Lieferant**, auf die in der VendTable-Tabelle verwiesen wird, nur beim ersten Aufruf der Datenquelle **Lieferant** zugegriffen. Die Auswahl der Datensätze erfolgt jedoch im Speicher. Daher kann dieser Ansatz eine Verschlechterung der Leistung verursachen.

## <a name="missing-binding"></a><a id="i11"></a>Fehlende Bindung

Wenn Sie eine EB-Formatkomponente konfigurieren, wird das Basis-EB-Datenmodell als Standarddatenquelle für das EB-Format angeboten. Wenn das konfigurierte EB-Format ausgeführt wird, wird die [Standardmodellzuordnung](er-country-dependent-model-mapping.md) für das Basismodell verwendet, um das Datenmodell mit Anwendungsdaten zu fillen. Der EB-Formatdesigner zeigt eine Warnung an, wenn Sie ein Formatelement an ein Datenmodellelement binden, das nicht an eine Datenquelle in der Modellzuordnung gebunden ist, die derzeit als Standardmodellzuordnung für das bearbeitbare Format ausgewählt ist. Diese Art der Bindung kann nicht zur Laufzeit ausgeführt werden, da das ausgeführte Format ein gebundenes Element nicht mit Anwendungsdaten füllen kann. Daher tritt zur Laufzeit ein Fehler auf.

Die folgenden Schritte zeigen, wie dieses Problem auftreten kann.

1. Beginnen Sie gleichzeitig mit der Konfiguration der EB-Datenmodell-, der EB-Modellzuordnungs- und der EB-Formatkomponenten.
2. Fügen Sie im Datenmodellbaum ein Stammelement mit dem Namen **Root3** hinzu.
3. Ändern Sie das Element **Root3**, indem Sie ein neues verschachteltes Element vom Typ **Datensatzliste** hinzufügen.
4. Nennen Sie das neue verschachtelte Element **Lieferant**.
5. Ändern Sie das Element **Lieferant** auf folgende Weise:

    - Fügen Sie ein verschachteltes Feld vom Typ **Zeichenfolge** hinzu und nennen Sie es **Name**.
    - Fügen Sie ein verschachteltes Feld vom Typ **Zeichenfolge** hinzu und nennen Sie es **AccountNumber**.

    ![Hinzufügen verschachtelter Felder zum Kreditorelement auf der Seite „Datenmodell“.](./media/er-components-inspections-11a.png)

6. Fügen Sie im Bereich **Datenquellen** des Modellzuordnungsdesigners eine Datenquelle vom Typ **Dynamics 365 for Operations \\ Tabellendatensätze** hinzu.
7. Nennen Sie die neue Datenquelle **Lieferant**. Wählen Sie im Feld **Tabelle** die Option **VendTable** aus, um anzugeben, dass diese Datenquelle die VendTable-Tabelle anfordert.
8. Fügen Sie eine Datenquelle vom Typ **Allgemein \\ Benutzereingabeparameter** hinzu, um im Dialogfeld zur Laufzeit ein Lieferantenkonto abzufragen.
9. Nennen Sie die neue Datenquelle **RequestedAccountNum**. Geben Sie in das Feld **Beschriftung** den Text **Lieferantenkontonummer** ein. Behalten Sie im Feld **Name des Betriebsdatentyps** den Standardwert **Beschreibung** bei.
10. Fügen Sie eine Datenquelle vom Typ **Berechnetes Feld** hinzu, um nach einem Lieferanten zu filtern, zu dem eine Abfrage durchgeführt wird.
11. Nennen Sie die neue Datenquelle **FilteredVendor** und konfigurieren Sie sie so, dass sie den Ausdruck `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)` enthält.
12. Binden Sie die Datenmodellelemente wie folgt an konfigurierte Datenquellen:

    - Binden Sie **FilteredVendor** an **Lieferant**.
    - Binden Sie **FilteredVendor.AccountNum** an **Vendor.AccountNumber**.

    > [!NOTE]
    > Das Datenmodell **Vendor.Name** bleibt ungebunden.

    ![Datenmodellelemente, die an konfigurierte Datenquellen gebunden sind, und ein Datenmodellelement, das ungebunden auf der Seite „Modellzuordnungsdesigner“ verbleibt.](./media/er-components-inspections-11b.png)

13. Fügen Sie im Formatstrukturbaum die folgenden Elemente hinzu, um ein ausgehendes Dokument im XML-Format zu generieren, das die Details zu den abgefragten Lieferanten enthält:

    1. Fügen Sie das Root-XML-Element **Anweisung** hinzu.
    2. Fügen Sie für das XML-Element **Anweisung** das verschachtelte XML-Element **Partei** hinzu.
    3. Fügen Sie für das XML-Element **Partei** die folgenden verschachtelten XML-Attribute hinzu.

        - Name
        - AccountNum

14. Binden Sie die Formatelemente auf die folgende Weise an bereitgestellte Datenquellen:

    - Binden Sie das Formatelement **Anweisung\\Partei** an das Datenquellenelement `model.Vendor`.
    - Binden Sie das Formatelement **Anweisung\\Partei\\Name** an das Datenquellenfeld **model.Vendor.Name**.
    - Binden Sie das Formatelement **Anweisung\\Partei\\AccountNum** an das Datenquellenfeld **model.Vendor.AccountNumber**.

15. Wählen Sie **Überprüfen** aus, um die bearbeitbare Formatkomponente auf der Seite **Formatdesigner** zu überprüfen.

    ![EB-Formatkomponente auf der Seite „Formatdesigner“ prüfen.](./media/er-components-inspections-11c.png)

16. Beachten Sie, dass eine Prüfungswarnung auftritt. Die Nachricht besagt, dass das Datenquellenfeld **model.Vendor.Name** nicht an eine Datenquelle in der Modellzuordnung gebunden ist, die zur Verwendung durch das Format konfiguriert ist. Deshalb wird das Formatelement **Anweisung\\Partei\\Name** zur Laufzeit möglicherweise nicht gefüllt und es kann zu einer Laufzeitausnahme kommen.

    ![Prüfen der EB-Formatkomponente auf der Seite „Formatdesigner“.](./media/er-components-inspections-11d.png)

Die folgende Abbildung zeigt den Laufzeitfehler, der auftritt, wenn Sie die Warnung ignorieren und **Ausführen** auswählen, um das Format auszuführen.

![Ausführen des bearbeitbaren Formats auf der Seite „Formatdesigner“.](./media/er-components-inspections-11e.png)

### <a name="automatic-resolution"></a>Automatische Lösung

Es ist keine Option verfügbar, um dieses Problem automatisch zu beheben.

### <a name="manual-resolution"></a>Manuelle Lösung

#### <a name="option-1"></a>Option 1

Ändern Sie die konfigurierte Modellzuordnung, indem Sie eine Bindung für das Datenquellenfeld **model.Vendor.Name** hinzufügen.

#### <a name="option-2"></a>Option 2

Ändern Sie das konfigurierte Format, indem Sie die Bindung des Formatelements **Anweisung\\Partei\\Name** entfernen.

## <a name="not-linked-template"></a><a id="i12"></a>Nicht verknüpfte Vorlage

Wenn Sie [manuell](er-fillable-excel.md#manual-entry) eine EB-Formatkomponente so konfigurieren, dass sie eine Vorlage zum Generieren eines ausgehenden Dokuments verwendet, müssen Sie das Element **Excel\\Datei** manuell hinzufügen, die erforderliche Vorlage als Anhang der bearbeitbaren Komponente hinzufügen und diesen Anhang im hinzugefügten Element **Excel\\Datei** auswählen. Auf diese Weise geben Sie an, dass das hinzugefügte Element zur Laufzeit die ausgewählte Vorlage ausfüllt. Wenn Sie eine Formatkomponentenversion im Status **Entwurf** konfigurieren, können Sie der bearbeitbaren Komponente mehrere Vorlagen hinzufügen und dann jede Vorlage im Element **Excel\\Datei** auswählen, um das EB-Format auszuführen. Auf diese Weise können Sie sehen, wie verschiedene Vorlagen zur Laufzeit gefüllt werden. Wenn Sie Vorlagen haben, die in keinem Elemen **Excel\\Datei** ausgewählt sind, warnt Sie der EB-Formatdesigner, dass diese Vorlagen aus der bearbeitbaren EB-Formatkomponentenversion gelöscht werden, wenn ihr Status von **Entwurf** zu **Abgeschlossen** geändert wird.

Die folgenden Schritte zeigen, wie dieses Problem auftreten kann.

1. Beginnen Sie mit der Konfiguration der EB-Formatkomponente.
2. Fügen Sie im Formatstrukturbaum das Element **Excel\\Datei** hinzu.
3. Fügen Sie für das soeben hinzugefügte Element **Excel\\Datei** eine Excel-Arbeitsmappendatei (**A.xlsx**) als Anhang hinzu. Verwenden Sie den Dokumenttyp, der in den [EB-Parametern](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) konfiguriert ist, um die Speicherung von EB-Formatvorlagen festzulegen.
4. Fügen Sie für das Element **Excel\\Datei** eine weitere Excel-Arbeitsmappendatei (**B.xlsx**) als Anhang hinzu. Verwenden Sie denselben Dokumenttyp, der für die Arbeitsmappendatei A verwendet wird.
5. Wählen Sie im Element **Excel\\Datei** die Arbeitsmappendatei A aus.
6. Wählen Sie **Überprüfen** aus, um die bearbeitbare Formatkomponente auf der Seite **Formatdesigner** zu überprüfen.

    ![Überprüfen der bearbeitbaren Formatkomponente der Arbeitsmappendatei auf der Seite „Formatdesigner“.](./media/er-components-inspections-12a.gif)

7. Beachten Sie, dass eine Prüfungswarnung auftritt. Die Nachricht gibt an, dass die Arbeitsmappendatei B.xlsx mit keinen Komponenten verknüpft ist und entfernt wird, nachdem der Status der Konfigurationsversion geändert wurde.

### <a name="automatic-resolution"></a>Automatische Lösung

Es ist keine Option verfügbar, um dieses Problem automatisch zu beheben.

### <a name="manual-resolution"></a>Manuelle Lösung

Ändern Sie das konfigurierte Format, indem Sie alle Vorlagen entfernen, die mit keinem Element **Excel\\Datei** verknüpft sind.

## <a name="not-synced-format"></a><a id="i13"></a>Nicht synchronisiertes Format

Wenn Sie eine EB-Formatkomponente so [konfigurieren](er-fillable-excel.md), dass sie eine Excel-Vorlage zum Generieren eines ausgehenden Dokuments verwendet, können Sie das Element **Excel\\Datei** manuell hinzufügen, die erforderliche Vorlage als Anhang der bearbeitbaren Komponente hinzufügen und diesen Anhang im hinzugefügten Element **Excel\\Datei** auswählen. Auf diese Weise geben Sie an, dass das hinzugefügte Element zur Laufzeit die ausgewählte Vorlage ausfüllt. Da die hinzugefügte Excel-Vorlage extern entworfen wurde, enthält das bearbeitbare EB-Format möglicherweise Excel-Namen, die in der hinzugefügten Vorlage fehlen. Der EB-Formatdesigner warnt Sie vor Inkonsistenzen zwischen den Eigenschaften der EB-Formatelemente, die sich auf Namen beziehen, die nicht in der hinzugefügten Excel-Vorlage enthalten sind.

Die folgenden Schritte zeigen, wie dieses Problem auftreten kann.

1. Beginnen Sie mit der Konfiguration der EB-Formatkomponente.
2. Fügen Sie im Formatstrukturbaum das **Excel\\Datei**-Element **Bericht** hinzu.
3. Fügen Sie für das soeben hinzugefügte Element **Excel\\Datei** eine Excel-Arbeitsmappendatei (**A.xlsx**) als Anhang hinzu. Verwenden Sie den Dokumenttyp, der in den [EB-Parametern](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) konfiguriert ist, um die Speicherung von EB-Formatvorlagen festzulegen.

    > [!IMPORTANT]
    > Stellen Sie sicher, dass die hinzugefügte Excel-Arbeitsmappe den Namen **ReportTitle** nicht enthält.

4. Fügen Sie das **Excel\\Zelle**-Element **Titel** als verschachteltes Element des Elements **Bericht** hinzu. Wählen Sie im Feld **Excel-Bereich** die Option **ReportTitle** aus.
5. Wählen Sie **Überprüfen** aus, um die bearbeitbare Formatkomponente auf der Seite **Formatdesigner** zu überprüfen.

    ![Überprüfen der verschachtelten Elemente und Felder auf der Seite „Formatdesigner“.](./media/er-components-inspections-13a.png)

6. Beachten Sie, dass eine Prüfungswarnung auftritt. Die Nachricht besagt, dass der Name **ReportTitle** in der Tabelle **Sheet1** der von Ihnen verwendeten Excel-Vorlage nicht enthalten ist.

    ![Prüfungswarnung, dass der Name „ReportTitle“ in „Sheet1“ der Excel-Vorlage nicht vorhanden ist.](./media/er-components-inspections-13b.png)

### <a name="automatic-resolution"></a>Automatische Lösung

Es ist keine Option verfügbar, um dieses Problem automatisch zu beheben.

### <a name="manual-resolution"></a>Manuelle Lösung

#### <a name="option-1"></a>Option 1

Ändern Sie das konfigurierte Format, indem Sie alle Elemente entfernen, die auf Excel-Namen verweisen, die in der Vorlage fehlen.

#### <a name="option-2"></a>Option 2

[Aktualisieren](er-fillable-excel.md#template-import) Sie das bearbeitbare EB-Format durch Importieren einer Excel-Vorlage. Die Struktur des bearbeitbaren EB-Formats wird mit der Struktur der importierten EB-Vorlage [synchronisiert](modify-electronic-reporting-format-reapply-excel-template.md).

### <a name="additional-consideration"></a>Zusätzliche Überlegung

Informationen dazu, wie die Formatstruktur mit einer EB-Vorlage im Vorlageneditor von der [Geschäftsdokumentverwaltung](er-business-document-management.md) synchronisiert werden kann, finden Sie unter [Struktur einer Geschäftsdokumentvorlage aktualisieren](er-bdm-update-structure.md).

## <a name="not-synced-with-a-word-template-format"></a><a id="i14"></a>Nicht mit einem Word-Vorlagenformat synchronisiert

Wenn Sie eine EB-Formatkomponente so [konfigurieren](er-fillable-excel.md), dass sie eine Word-Vorlage zum Generieren eines ausgehenden Dokuments verwendet, können Sie das Element **Excel\\Datei** manuell hinzufügen, die erforderliche Word-Vorlage als Anhang der bearbeitbaren Komponente hinzufügen und diesen Anhang im hinzugefügten Element **Excel\\Datei** auswählen.

> [!NOTE]
> Wenn das Word-Dokument angehängt ist, zeigt der EB-Formatdesigner das bearbeitbare Element als **Word\\Datei** an.

Auf diese Weise geben Sie an, dass das hinzugefügte Element zur Laufzeit die ausgewählte Vorlage ausfüllt. Da die hinzugefügte Word-Vorlage extern entworfen wurde, enthält das bearbeitbare EB-Format möglicherweise Verweise auf Word-Inhaltssteuerelemente, die in der hinzugefügten Vorlage fehlen. Der EB-Formatdesigner warnt Sie vor Inkonsistenzen zwischen den Eigenschaften der EB-Formatelemente, die sich auf Inhaltssteuerelemente beziehen, die nicht in der hinzugefügten Word-Vorlage enthalten sind.

Ein Beispiel, das zeigt, wie dieses Problem auftreten kann, finden Sie unter [Das bearbeitbare Format zum Unterdrücken des Zusammenfassungsabschnitts konfigurieren](er-design-configuration-word-suppress-controls.md#configure-to-suppress-control).

### <a name="automatic-resolution"></a>Automatische Lösung

Es ist keine Option verfügbar, um dieses Problem automatisch zu beheben.

### <a name="manual-resolution"></a>Manuelle Lösung

#### <a name="option-1"></a>Option 1

Ändern Sie das konfigurierte Format, indem Sie die **Entfernt**-Formelaus dem Formatelement löschen, das in der Validierungswarnung erwähnt wird.

#### <a name="option-2"></a>Option 2

Ändern Sie die verwendete Word-Vorlage, indem Sie dem entsprechenden Word-Inhaltssteuerelement die erforderliche Markierung [hinzufügen](er-design-configuration-word-suppress-controls.md#tag-control).

## <a name="no-default-mapping"></a><a id="i15"></a>Keine Standardzuordnung

Wenn die Untersuchung [Fehlende Bindung](#i11) abgeschlossen ist, werden die untersuchten Formatbindungen anhand der Bindungen der relevanten Modellzuordnungskomponente bewertet. Da Sie [mehrere](./tasks/er-manage-model-mapping-configurations-july-2017.md) EB-Modellzuordnungskonfigurationen in Ihre Finance-Instanz importieren können, und jede Konfiguration möglicherweise die entsprechende Modellzuordnungskomponente enthält, muss eine Konfiguration als Standardkonfiguration ausgewählt werden. Andernfalls tritt beim Versuch, das untersuchte EB-Format auszuführen, zu bearbeiten oder zu validieren, eine Ausnahme auf, und Sie erhalten die folgende Meldung: „Für das \<model name (root descriptor)\>-Datenmodell ist in den Konfigurationen mehr als eine Modellzuordnung vorhanden \<configuration names separated by comma\>. Legen Sie eine der Konfigurationen als Standard fest.“

Ein Beispiel, das zeigt, wie dieses Problem auftreten und behoben werden kann, finden Sie unter [Mehrere abgeleitete Zuordnungen für einen einzelnen Modellstamm verwalten](er-multiple-model-mappings.md).

## <a name="inconsistent-setting-of-header-or-footer-components"></a><a id="i16"></a>Inkonsistente Einstellung der Kopf- oder Fußzeilenkomponenten

Wenn Sie eine EB-Formatkomponente [konfigurieren](er-fillable-excel.md), um eine Excel-Vorlage zum Generieren eines ausgehenden Dokuments zu verwenden, können Sie die **Excel\\Kopfzeile**-Komponente zum Ausfüllen von Kopfzeilen in einem Arbeitsblatt einer Excel-Arbeitsmappe hinzufügen. Sie können auch die **Excel\\Fußzeile**-Komponente zum Ausfüllen von Fußzeilen in einem Arbeitsblatt hinzufügen. Für jede **Excel\\Kopfzeile**- oder **Excel\\Fußzeile**-Komponente, die Sie hinzufügen, müssen Sie die Eigenschaft **Kopf-/Fußzeilendarstellung** festlegen, um die Seiten anzugeben, für die die Komponente ausgeführt wird. Da Sie mehrere **Excel\\Kopfzeile**- oder **Excel\\Fußzeile**-Komponenten für eine einzelne **Blatt**-Komponente konfigurieren und verschiedene Kopf- oder Fußzeilen für verschiedene Seitentypen in einem Excel-Arbeitsblatt generieren können, müssen Sie eine einzelne **Excel\\Kopfzeile**- oder **Excel\\Fußzeile**-Komponente für einen bestimmten Wert der Eigenschaft **Kopf-/Fußzeile** konfigurieren. Wenn mehr als eine **Excel\\Kopfzeile**- oder **Excel\\Fußzeile**-Komponente für einen bestimmten Wert der Eigenschaft **Kopf-/Fußzeilendarstellung** konfiguriert ist, tritt ein Überprüfungsfehler auf, und Sie erhalten die folgende Fehlermeldung: „Kopf-/Fußzeilen (&lt;Komponententyp: Kopf- oder Fußzeile&gt;) sind inkonsistent.“

### <a name="automatic-resolution"></a>Automatische Lösung

Es ist keine Option verfügbar, um dieses Problem automatisch zu beheben.

### <a name="manual-resolution"></a>Manuelle Lösung

#### <a name="option-1"></a>Option 1

Ändern Sie das konfigurierte Format, indem Sie eine der inkonsistenten **Excel\\Kopfzeile**- oder **Excel\\Fußzeile**-Komponenten löschen.

#### <a name="option-2"></a>Option 2

Ändern Sie den Wert der Eigenschaft **Kopf-/Fußzeile** für eine der inkonsistenten **Excel\\Kopfzeile**- oder **Excel\\Fußzeile**-Komponenten.

## <a name="inconsistent-setting-of-page-component"></a><a id="i17"></a>Inkonsistente Einstellung der Seitenkomponente

Wenn Sie eine ER-Formatkomponente [konfigurieren](er-fillable-excel.md) zur Verwendung einer Excel-Vorlage zum Generieren eines ausgehenden Dokuments generieren, können Sie die Komponente **Excel\\Seite** hinzufügen, um ein generiertes Dokument mithilfe von ER-Formeln zu paginieren. Für jede **Excel\\Seite**-Komponente, die Sie hinzufügen, können Sie zahlreiche verschachtelte [Bereich](er-fillable-excel.md#range-component)-Komponenten hinzufügen und dennoch die folgende [Struktur](er-fillable-excel.md#page-component-structure) einhalten:

- Die erste verschachtelte **Bereich**-Komponente kann so konfiguriert werden, dass die Eigenschaft **Replikationsrichtung** auf **Keine Replikation** eingestellt ist. Dieser Bereich wird verwendet, um Seitenüberschriften in generierten Dokumenten zu erstellen.
- Sie können zahlreiche andere verschachtelte **Bereich**-Komponenten hinzufügen, bei denen die Eigenschaft **Replikationsrichtung** auf **Vertikal** eingestellt ist. Diese Bereiche werden verwendet, um generierte Dokumente auszufüllen.
- Die letzte verschachtelte **Bereich**-Komponente kann so konfiguriert werden, dass die Eigenschaft **Replikationsrichtung** auf **Keine Replikation** eingestellt ist. Dieser Bereich wird verwendet, um Seitenfußzeilen in generierten Dokumenten zu erstellen und die erforderlichen Seitenumbrüche hinzuzufügen.

Wenn Sie diese Struktur für ein ER-Format im ER-Formatdesigner zur Entwurfszeit nicht befolgen, tritt ein Validierungsfehler auf und Sie erhalten folgende Fehlermeldung: „Es gibt mehr als zwei Bereichskomponenten ohne Replikation. Bitte entfernen Sie nicht benötigte Komponenten.“

### <a name="automatic-resolution"></a>Automatische Lösung

Es ist keine Option verfügbar, um dieses Problem automatisch zu beheben.

### <a name="manual-resolution"></a>Manuelle Lösung

#### <a name="option-1"></a>Option 1

Ändern Sie das konfigurierte Format, indem Sie die Eigenschaft **Replikationsrichtung** für alle inkonsistenten **Excel\\Bereich**-Komponenten ändern.

## <a name="executability-of-an-expression-with-orderby-function"></a><a id="i18"></a>Ausführbarkeit eines Ausdrucks mit der Funktion ORDERBY

Die integrierte [ORDERBY](er-functions-list-orderby.md) ER-Funktion wird verwendet, um die Datensätze einer ER-Datenquelle vom Typ **[Datensatzliste](er-formula-supported-data-types-composite.md#record-list)** zu sortieren, die als Argument der Funktion angegeben wird.

Die Argumente der Funktion `ORDERBY` können [angegeben](er-functions-list-orderby.md#syntax-2) werden, um Datensätze von Anwendungstabellen, Ansichten oder Entitäten durch einen einzigen Datenbankaufruf zu sortieren und die sortierten Daten als Liste von Datensätzen zu erhalten. Eine Datenquelle vom Typ **Datensatzliste** wird als Argument der Funktion verwendet und gibt die Anwendungsquelle für den Aufruf an.

ER prüft, ob eine direkte Datenbankabfrage zu einer Datenquelle, auf die in der Funktion `ORDERBY` verwiesen wird, eingerichtet werden kann. Wenn keine direkte Abfrage möglich ist, tritt im EB-Modellzuordnungsdesigner ein Prüfungsfehler auf. Die Nachricht, die Sie erhalten, besagt, dass der EB-Ausdruck, der die `ORDERBY`-Funktion enthält, nicht zur Laufzeit ausgeführt werden kann.

Die folgenden Schritte zeigen, wie dieses Problem auftreten kann.

1. Beginnen Sie mit der Konfiguration der EB-Modellzuordnungskomponente.
2. Fügen Sie eine Datenquelle vom Typ **Dynamics 365 for Operations \\ Tabellendatensätze** hinzu.
3. Nennen Sie die neue Datenquelle **Lieferant**. Wählen Sie im Feld **Tabelle** die Option **VendTable**, um anzugeben, dass diese Datenquelle die Tabelle **VendTable** abfragt.
4. Fügen Sie eine Datenquelle vom Typ **Berechnetes Feld** hinzu.
5. Nennen Sie die neue Datenquelle **OrderedVendors**, und konfigurieren Sie sie so, dass sie den Ausdruck `ORDERBY("Query", Vendor, Vendor.AccountNum)` enthält.
 
    ![Konfigurieren Sie die Datenquellen auf der Designerseite für die Modellzuordnung.](./media/er-components-inspections-18-1.png)

6. Wählen Sie **Validieren**, um die bearbeitbare Komponente für die Modellzuordnung auf der Seite **Modellzuordnungsdesigner** zu überprüfen und sicherzustellen, dass der Ausdruck in der Datenquelle **OrderedVendors** abgefragt werden kann.
7. Ändern Sie die Datenquelle **Lieferant**, indem sie ein verschachteltes Feld vom Typ **Berechnetes Feld** hinzufügen, um die gekürzte Lieferantenkontonummer abzurufen.
8. Nennen Sie die das verschachtelte Feld **$AccNumber** und konfigurieren Sie es so, dass es den Ausdruck `TRIM(Vendor.AccountNum)` enthält.
9. Wählen Sie **Validieren**, um die bearbeitbare Komponente für die Modellzuordnung auf der Seite **Modellzuordnungsdesigner** zu prüfen und sicherzustellen, dass der Ausdruck in der Datenquelle **Lieferant** abgefragt werden kann.

    ![Überprüfen, ob der Ausdruck in der Datenquelle Kreditor auf der Designerseite für die Modellzuordnung abgefragt werden kann.](./media/er-components-inspections-18-2.png)

10. Beachten Sie, dass ein Überprüfungsfehler auftritt, weil die Datenquelle **Kreditor** ein verschachteltes Feld des Typs **Berechnetes Feld** enthält, das es nicht zulässt, dass der Ausdruck der Datenquelle **OrderedVendors** in die direkte Datenbankanweisung übersetzt wird. Der gleiche Fehler tritt zur Laufzeit auf, wenn Sie den Validierungsfehler ignorieren und **Ausführen** wählen, um diese Modellzuordnung auszuführen.

### <a name="automatic-resolution"></a>Automatische Lösung

Es ist keine Option verfügbar, um dieses Problem automatisch zu beheben.

### <a name="manual-resolution"></a>Manuelle Lösung

#### <a name="option-1"></a>Option 1

Anstatt ein verschachteltes Feld vom Typ **Berechnetes Feld** zur Datenquelle **Kreditor** hinzuzufügen, fügen Sie das verschachtelte Feld **$AccNumber** zur Datenquelle **FilteredVendors** hinzu und konfigurieren das Feld so, dass es den Ausdruck `TRIM(FilteredVendor.AccountNum)` enthält. Auf diese Weise kann der Ausdruck `ORDERBY("Query", Vendor, Vendor.AccountNum)` auf der Datenbankebene ausgeführt werden und die Berechnung des verschachtelten Feldes **$AccNumber** kann danach erfolgen.

#### <a name="option-2"></a>Option 2

Ändern Sie den Ausdruck der Datenquelle **FilteredVendors** von `ORDERBY("Query", Vendor, Vendor.AccountNum)` auf `ORDERBY("InMemory", Vendor, Vendor.AccountNum)`. Wir empfehlen Ihnen nicht, den Ausdruck für eine Tabelle mit einem großen Datenvolumen (Transaktionstabelle) zu ändern, da alle Datensätze abgerufen werden und die Reihenfolge der benötigten Datensätze im Speicher erfolgt. Daher kann dieser Ansatz eine Verschlechterung der Leistung verursachen.

## <a name="obsolete-application-artifact"></a><a id="i19"></a>Veraltetes Anwendungsartefakt

Wenn Sie eine ER-Modellzuordnungskomponente oder eine ER-Formatkomponente entwerfen, können Sie einen ER-Ausdruck konfigurieren, um ein Anwendungsartefakt in ER aufzurufen, z. B. eine Datenbanktabelle, eine Methode einer Klasse usw. In Finanzversion 10.0.30 und höher, können Sie ER zwingen, Sie zu warnen, dass das verwiesene Anwendungsartefakt im Quellcode als veraltet gekennzeichnet ist. Diese Warnung kann nützlich sein, da veraltete Artefakte normalerweise irgendwann aus dem Quellcode entfernt werden. Die Information über den Status eines Artefakts kann Sie davon abhalten, das veraltete Artefakt in der bearbeitbaren ER-Komponente zu verwenden, bevor es aus dem Quellcode entfernt wird, und hilft, Fehler beim Aufrufen nicht vorhandener Anwendungsartefakte von einer ER-Komponente zur Laufzeit zu vermeiden.

Aktivieren Sie die Funktion **Veraltete Elemente von Datenquellen in der elektronischen Berichterstellung überprüfen** im **Funktionsverwaltung**-Arbeitsbereich, um mit der Bewertung des obsoleten Attributs von Anwendungsartefakten während der Inspektion einer bearbeitbaren ER-Komponente zu beginnen. Das veraltete Attribut wird derzeit für die folgenden Arten von Anwendungsartefakten ausgewertet:

- Datenbanktabelle
    - Feld einer Tabelle
    - Methode einer Tabelle
- Anwendungs-Klasse
    - Methode einer Klasse

> [!NOTE]
> Bei der Prüfung der bearbeitbaren ER-Komponente auf eine Datenquelle, die auf ein veraltetes Artefakt verweist, erfolgt nur dann eine Warnung, wenn diese Datenquelle in mindestens einer Bindung dieser ER-Komponente verwendet wird.

> [!TIP]
> Wenn die [SysObsoleteAttribute](../dev-ref/xpp-attribute-classes.md#sysobsoleteattribute)-Klasse verwendet wird, um den Compiler zu benachrichtigen, Warnmeldungen anstelle von Fehlern auszugeben, stellt die Inspektionswarnung die im Quellcode angegebene Warnung zur Entwurfszeit im **Details**-Inforegister auf der **Model-Mapping-Designer** oder **Format-Designer**-Seite dar.

Die folgende Abbildung zeigt die Validierungswarnung, die auftritt, wenn das obsolete `DEL_Email`-Feld der `CompanyInfo`-Anwendungstabelle mithilfe der konfigurierten `company`-Datenquelle an ein Datenmodellfeld gebunden wird.

![Überprüfen Sie die Validierungswarnungen auf der Registerkarte Details auf der Seite Modellzuordnungsdesigner.](./media/er-components-inspections-19a.png)

### <a name="automatic-resolution"></a>Automatische Lösung

Es ist keine Option verfügbar, um dieses Problem automatisch zu beheben.

### <a name="manual-resolution"></a>Manuelle Lösung

Ändern Sie die konfigurierte Modellzuordnung oder das Format, indem Sie alle Bindungen an eine Datenquelle entfernen, die auf ein veraltetes Anwendungsartefakt verweist.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[ALLITEMS EB-Funktion](er-functions-list-allitems.md)

[ALLITEMSQUERY EB-Funktion](er-functions-list-allitemsquery.md)

[INT64VALUE EB-Funktion](er-functions-conversion-int64value.md)

[INTVALUE EB-Funktion](er-functions-conversion-intvalue.md)

[FILTER EB-Funktion](er-functions-list-filter.md)

[WHERE EB-Funktion](er-functions-list-where.md)

[Verwenden von JOIN-Datenquellen, um Daten aus mehreren Anwendungstabellen in EB-Modellzuweisungen abzurufen](er-join-data-sources.md)

[Überwachen der Ausführung von ER-Formaten zur Behebung von Leistungsproblemen](trace-execution-er-troubleshoot-perf.md)

[Geschäftsdokumentverwaltung – Übersicht](er-business-document-management.md)

[Steuerelemente für Word-Inhalte in generierten Berichten unterdrücken](er-design-configuration-word-suppress-controls.md)

[Mehrere abgeleitete Zuordnungen für eine einzelne Modellwurzel verwalten](er-multiple-model-mappings.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
