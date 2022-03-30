---
title: Unterstützung parametrisierter Aufrufe von ER-Datenmodellen
description: In diesem Thema wird erläutert, wie parametrisierte Aufrufe von Datenmodellen für die elektronische Berichterstattung (ER) implementiert werden.
author: NickSelin
ms.date: 03/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula, ERDataModelDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-10-01
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 968b0769607e9fdbed57c25b727ed44988a92913
ms.sourcegitcommit: 399d0d3f8e2ebb81b6b9d640365ebe182690bab2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2022
ms.locfileid: "8419470"
---
# <a name="support-parameterized-calls-of-er-data-models"></a>Unterstützung parametrisierter Aufrufe von ER-Datenmodellen

[!include [banner](../includes/banner.md)]

Um Geschäftsdokumente zu generieren, konfigurieren Sie eine [Elektronische Berichterstellung (ER, Electronic Reporting)](general-electronic-reporting.md)-Lösung, die die folgenden ER-Komponenten enthält:

- **[Format](er-overview-components.md#format-component)** – Diese Komponente legt die Struktur eines Geschäftsdokuments fest.
- **Formatzuordnung** – Diese Komponente steuert, wie ein Geschäftsdokument zur Laufzeit ausgefüllt wird.
- **[Modellzuordnung](er-overview-components.md#model-mapping-component)** – Diese Komponente gibt an, was die Daten aus der Anwendung in eine Formatzuordnung ziehen.
- **[Datenmodell](er-overview-components.md#data-model-component)** – Diese Komponente gibt Informationen zwischen einzelnen Komponenten weiter.

Wenn Sie ein ER-Format ausführen, wird jedes Formatelement ausgeführt, beginnend mit dem Stammformatelement. Immer wenn ein ausgeführtes Formatelement eine Bindung zu einer [Datenquelle](general-electronic-reporting.md#configuring-data-model-mappings-for-outgoing-documents) enthält, wird die Datenquelle ausgeführt, um die erwarteten Daten zu liefern und sie zum Ausfüllen des Formatelements zu verwenden. Wenn eine Datenquelle des Typs *Modell* aufgerufen wird, wird die entsprechende Modellzuordnung aufgerufen, um Daten basierend auf den Modellzuordnungseinstellungen aus der Anwendung abzurufen.

Bisher konnten diese Modellzuordnungsaufrufe nicht parametrisiert werden, um sie von der Logik des ausgeführten Formats abhängig zu machen. Nur der folgende Datenfluss wurde unterstützt.

<table>
<tbody>
<tr align="center">
<td>
<b>Format</b><br>
Formatelement&nbsp;<br>
&nbsp;
</td>
<td>
<i>Bindung</i><br>
&gt;&nbsp;Anforderung&nbsp;&gt;<br>
&lt;&nbsp;Wert&nbsp;&lt;
</td>
<td><b>Formatzuordnung&nbsp;</b><br>
Datenquelle<br>
&nbsp;
</td>
<td>
<i>Datenmodell&nbsp;</i><br>
&gt;&nbsp;Anforderung&nbsp;&gt;<br>
&lt;&nbsp;Wert&nbsp;&lt;
</td>
<td>
<b>Modellzuordnung&nbsp;</b><br>
Datenquelle&nbsp;<br>
&nbsp;
</td>
<td>
<i>Bindung</i><br>
&gt;&nbsp;Anforderung&nbsp;&gt;<br>
&lt;&nbsp;Wert&nbsp;&lt;
</td>
<td>
<b>Tabelle</b><br>
Aufzeichnen<br>
Feld
</td>
</tr>
</tbody>
</table>

In Version 10.0.15 und höher können Sie jedoch Datenmodellfelder konfigurieren, die nur aufgerufen werden können, wenn die Werte der konfigurierten Parameter bereitgestellt werden. Wenn ein solches Feld konfiguriert und von einer Formatkomponente aufgerufen wird, müssen die erforderlichen Parameter in einer Formatbindung als Argumente des Aufrufs bereitgestellt werden. In diesen Fällen können die Werte der Argumente basierend auf formatspezifischen Werten angegeben werden. Daher können Sie **dynamische Laufzeitparametrierung** für Datenmodellaufrufe zur Unterstützung des folgenden Datenflusses verwenden.

<table>
<tbody>
<tr align="center">
<td>
<b>Format</b><br>
Formatelement&nbsp;1&nbsp;<br>
<br>
Formatelement&nbsp;2&nbsp;<br>
&nbsp;<br>
&nbsp;
</td>
<td>
<i>Bindung</i><br>
&gt;&nbsp;Anforderung&nbsp;1&nbsp;&gt;<br>
&lt;&nbsp;Wert&nbsp;1&nbsp;&lt;<br>
&gt;&nbsp;Anforderung&nbsp;2&nbsp;&gt;<br>
&lt;&nbsp;Wert&nbsp;3&nbsp;&lt;<br>
&nbsp;
</td>
<td>
<b>Formatzuordnung&nbsp;</b><br>
Datenquelle&nbsp;1&nbsp;<br>
&nbsp;<br>
<b>value2=Func(value1)</b><br>
&nbsp;<br>
&nbsp;
</td>
<td>
<i>Datenmodell&nbsp;</i><br>
&gt;&nbsp;field1&nbsp;&gt;<br>
&lt;&nbsp;Wert&nbsp;1&nbsp;&lt;<br>
<b>&gt;&nbsp;field2(value2)&nbsp;&gt;</b><br>
&lt;&nbsp;Wert&nbsp;3&nbsp;&lt;<br>
&nbsp;
</td>
<td>
<b>Modellzuordnung&nbsp;</b><br>
Datenquelle&nbsp;1&nbsp;<br>
<br>
Datenquelle&nbsp;2&nbsp;<br>
&nbsp;<br>
&nbsp;
</td>
<td>
<i>Bindung</i><br>
&gt;&nbsp;Anforderung&nbsp;1&nbsp;&gt;<br>
&lt;&nbsp;Wert&nbsp;1&nbsp;&lt;<br>
&gt;&nbsp;Anforderung&nbsp;2&nbsp;&gt;<br>
&lt;&nbsp;Wert&nbsp;3&nbsp;&lt;<br>
&nbsp;
</td>
<td>
<b>Tabelle&nbsp;1</b><br>
Datensatz&nbsp;1<br>
Feld&nbsp;1<br>
<b>Tabelle&nbsp;2</b><br>
Datensatz&nbsp;2<br>
Feld&nbsp;2
</td>
</tr>
</tbody>
</table>

Mit der neuen Funktionalität können Sie den Aufruf beliebiger Datenmodellfelder des Typs [*Datensatz*](er-formula-supported-data-types-composite.md#record) oder [*Datensatzliste*](er-formula-supported-data-types-composite.md#record-list) parametrisieren. Für die Parameter eines Datenmodellfeldes werden folgende Datentypen unterstützt:

- [Boolesch](er-formula-supported-data-types-primitive.md#boolean)
- [Behälter](er-formula-supported-data-types-composite.md#container)
- [Datum](er-formula-supported-data-types-primitive.md#date)
- [DateTime](er-formula-supported-data-types-primitive.md#datetime)
- [GUID](er-formula-supported-data-types-primitive.md#guid)
- [Int64](er-formula-supported-data-types-primitive.md#int64)
- [Ganzzahl](er-formula-supported-data-types-primitive.md#integer)
- [Gleitkommazahl](er-formula-supported-data-types-primitive.md#real)
- [Zeichenfolge](er-formula-supported-data-types-primitive.md#string)

Sie können jeden Parameter eines Datenmodellfeldes angeben, für das das Argument als Einzelwert des definierten Datentyps bereitgestellt werden kann, und die [*Liste*](er-formula-supported-data-types-composite.md#record-list) solcher Werte.

> [!NOTE]
> Der Standardwert für den Parameter eines Datenmodellfelds wird nicht unterstützt. Wenn Sie einem Feld in einem Datenmodell einen Parameter hinzufügen und die Version dieses Datenmodells bereits freigegeben und veröffentlicht wurde, müssen Sie alle entsprechenden Modellzuordnungen und -formate auf die neue Version dieses Modells [zurücksetzen](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase), da diese Datenmodelländerung nicht abwärts kompatibel ist.

Sie können parametrisierte Datenmodellfelder konfigurieren, um Modellzuordnungsaufrufe formatspezifisch zu machen. Dieser Ansatz kann Ihnen helfen, die Anzahl der Modellzuordnungen zu reduzieren, die für viele Formate eines einzelnen Datenmodells konfiguriert werden müssen. Sie können diesen Ansatz auch verwenden, um die Ausführungsleistung Ihrer Formate zu verbessern und die Zeit zu reduzieren, die zum Generieren von Geschäftsdokumenten erforderlich ist. Weitere Informationen über diese Funktion erhalten Sie, wenn Sie das Beispiel in diesem Thema abschließen.

## <a name="example-use-parameterized-calls-of-er-data-models"></a>Beispiel: Verwendung parametrisierter Aufrufe von ER-Datenmodellen

In den folgenden Schritten wird erläutert, wie ein Benutzer in der Rolle „Systemadministrator“ oder „Entwickler für elektronische Berichterstellung“ eine ER-Lösung entwerfen kann, die ein Datenmodell, eine Modellzuordnung und eine Format-ER-Komponente enthält, die so konfiguriert sind, dass sie eine Modellzuordnung aus einem Format aufrufen, indem sie ein Argument für den Aufruf bereitstellen, dessen Wert zur Laufzeit mit Hilfe der Formel des laufenden Formats berechnet wurde. 

Diese Schritte können im Unternehmen **DEMF** ausgeführt werden. Es sind keine Codeänderungen erforderlich. 

In diesem Beispiel erstellen Sie die erforderlichen ER [Konfigurationen](general-electronic-reporting.md#Configuration) für die Beispielfirma **Litware, Inc.**. Stellen Sie sicher, dass der Konfigurationsanbieter für die Beispielfirma **Litware, Inc.** (`http://www.litware.com`) für das ER Framework aufgeführt und als **Aktiv** markiert ist. Wenn dieser Konfigurationsanbieter nicht aufgeführt ist oder nicht als **Aktiv** markiert ist, folgen Sie den Schritten unter [Erstellen Sie einen Konfigurationsanbieter und markieren Sie ihn als aktiv](tasks/er-configuration-provider-mark-it-active-2016-11.md).

### <a name="business-scenario"></a>Geschäftsszenario

Sie haben eine ER-Lösung, die ein Format enthält, das Sie ausführen können, um ein elektronisches Dokument für Prüfungszwecke zu generieren. Dieses Format enthält Steuertransaktionen, die sich auf Verkaufsaufträge und Bestellungen beziehen und die erforderlichen Details enthalten, wie z. B. das Transaktionsdatum und den Steuerwert. Zum neuen Geschäftsjahr hat sich die Struktur dieses Dokuments geändert. Sie müssen jetzt ein erweitertes Dokument einreichen, das zusätzliche Details (Namen) aller Parteien (Kunden und Lieferanten) enthält, deren Transaktionen in generierten Berichten dargestellt werden. Daher müssen Sie Ihre ER-Lösung so ändern, dass sie Dokumente generiert, die dieser neuen Anforderung entsprechen.

### <a name="configure-the-er-framework"></a>Konfigurieren des EB-Frameworks

Befolgen Sie die Schritte in [ER-Framework konfigurieren](er-quick-start2-customize-report.md#ConfigureFramework), um den minimalen Satz von ER-Parametern einzurichten. Sie müssen diese Einrichtung abschließen, bevor Sie das ER Framework zum Entwerfen einer neuen ER-Lösung verwenden können.

### <a name="design-a-domain-specific-data-model"></a>Entwerfen eines domänenspezifischen Datenmodells

Sie müssen eine neue ER-Konfiguration erstellen, die die erforderliche Datenmodellkomponente enthält. Dieses Datenmodell wird später als Datenquelle verwendet, wenn Sie ein ER-Format für die Erstellung eines Prüfungsberichts entwerfen.

Führen Sie diese Schritte aus, um das erforderliche Datenmodell aus einer von Microsoft bereitgestellten XML-Datei zu importieren.

1. Laden Sie die Datei [Sample audit model.version.1.xml](https://download.microsoft.com/download/7/1/9/719b0132-fed7-4c73-8afa-90cac29c2fee/Sample-audit-model.version.1.xml) herunter und speichern Sie sie auf Ihrem lokalen Computer.
2. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
3. Wählen Sie im Arbeitsbereich **Elektronische Berichterstellung** die Option **Berichterstellungskonfigurationen** aus.
4. Wählen Sie auf der Seite **Konfigurationen** im Aktionsbereich **Exchange** \> **Laden aus XML-Datei**.
5. Wählen Sie **Durchsuchen**, und wählen Sie dann die Datei **Sample audit model.version.1.xml** aus.
6. Wählen Sie **OK** aus, um die Konfiguration zu importieren.

    ![Importierte ER-Datenmodell-Konfiguration auf der Seite Konfigurationen.](./media/er-data-model-parameterized-calls-imported-model.png)

Die folgende Abbildung zeigt die bearbeitbare Version des konfigurierten Datenmodells auf der Seite **Datenmodelldesigner**.

![Struktur des ER-Datenmodells auf der Seite Datenmodell-Designer.](./media/er-data-model-parameterized-calls-model1.png)

Derzeit ist das Modell so konzipiert, dass nur Steuertransaktionen angezeigt werden, die die erforderlichen Details enthalten.

### <a name="design-a-model-mapping-for-the-configured-data-model"></a>Entwerfen einer Modellzuordnung für das konfigurierte Datenmodell

Als Benutzer in der Rolle „Entwickler für elektronische Berichterstellung“ müssen Sie eine neue ER-Konfiguration erstellen, die eine Modellzuordnungskomponente für das Beispiel-Prüfungsdatenmodell enthält. Diese Komponente implementiert das konfigurierte Datenmodell für Microsoft Dynamics 365 Finance und ist spezifisch für diese App. Sie müssen die Modellzuordnungskomponente so konfigurieren, dass die Anwendungsobjekte angegeben werden, die zum Ausfüllen des konfigurierten Datenmodells mit Anwendungsdaten zur Laufzeit verwendet werden müssen. Um diese Aufgabe abzuschließen, müssen Sie verstehen, wie die Datenstruktur der Steuergeschäftsdomäne in Finance implementiert ist.

Führen Sie diese Schritte aus, um die erforderliche Modellzuordnung aus einer von Microsoft bereitgestellten XML-Datei zu importieren.

1. Laden Sie die Datei [Sample audit model mapping.version.1.1.xml](https://download.microsoft.com/download/c/0/3/c03a4673-b1b1-4ef8-96d0-bf96518be6e0/Sample-audit-model-mapping.version.1.1.xml) herunter und speichern Sie sie auf Ihrem lokalen Computer.
2. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
3. Wählen Sie im Arbeitsbereich **Elektronische Berichterstellung** die Option **Berichterstellungskonfigurationen** aus.
4. Wählen Sie auf der Seite **Konfigurationen** im Aktionsbereich **Exchange** \> **Laden aus XML-Datei**.
5. Wählen Sie **Durchsuchen** und suchen und wählen Sie dann die Datei **Sample audit model mapping.version.1.1.xml**.
6. Wählen Sie **OK** aus, um die Konfiguration zu importieren.

    ![Importierte ER-Model-Zuordnungskonfiguration auf der Seite Konfigurationen.](./media/er-data-model-parameterized-calls-imported-mapping.png)

Die folgende Abbildung zeigt die bearbeitbare Version der konfigurierten Modellzuordnung auf der Seite **Modellzuordnungsdesigner**.

![Struktur der ER-Model-Zuordnung auf der Seite Modellzuordnung Designer.](./media/er-data-model-parameterized-calls-mapping1.png)

Derzeit ist die Modellzuordnung so konzipiert, dass nur Steuertransaktionen angezeigt werden, die die erforderlichen Details enthalten. Es holt diese Informationen aus der `TaxTrans`-Anwendungstabelle mithilfe der konfigurierten ER-Datenquellen `TaxTrans` und `TaxTransFiltered`.

### <a name="design-a-new-format"></a>Entwurf eines neuen Formats

Als Benutzer in der Rolle des Electronic Reporting Functional Consultant müssen Sie eine neue EB-Konfiguration erstellen, die eine Komponente Format enthält. Sie müssen die Formatkomponente konfigurieren, um generierte Berichte mit Steuertransaktionen auszufüllen, die alle erforderlichen Details enthalten.

Führen Sie diese Schritte aus, um das erforderliche Format aus einer von Microsoft bereitgestellten XML-Datei zu importieren.

1. Laden Sie die Datei [Sample audit format.version.1.1.xml](https://download.microsoft.com/download/e/b/7/eb7e126e-2bb3-4bbb-a735-ffd4c48920b1/Sample-audit-format.version.1.1.xml) herunter und speichern Sie sie auf Ihrem lokalen Computer.
2. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
3. Wählen Sie im Arbeitsbereich **Elektronische Berichterstellung** die Option **Berichterstellungskonfigurationen** aus.
4. Wählen Sie auf der Seite **Konfigurationen** im Aktionsbereich **Exchange** \> **Laden aus XML-Datei**.
5. Wählen Sie **Durchsuchen** und wählen Sie dann die Datei **Sample audit format.version.1.1.xml** aus.
6. Wählen Sie **OK** aus, um die Konfiguration zu importieren.

    ![Importierte ER-Format-Konfiguration auf der Seite Konfigurationen.](./media/er-data-model-parameterized-calls-imported-format.png)

Die folgende Abbildung zeigt die bearbeitbare Version des konfigurierten Formats auf der Seite **Formatdesigner**.

![Struktur des ER-Formats auf der Seite Formatdesigner.](./media/er-data-model-parameterized-calls-format1.png)

Das ER-Format ist so konfiguriert, dass ein Bericht als Textdatei im CSV-Format (durch Kommas getrennte Werte) generiert wird.

### <a name="run-the-imported-format"></a>Importiertes Format ausführen

1. Auf der **Konfigurationen**-Seite wählen Sie die **Beispiel-Überwachungsformat**-Konfiguration und dann im Aktivitätsbereich **Ausführen** aus.
2. Wählen Sie im Dialogfeld **Elektronische Berichtsparameter** auf der Registerkarte **Einzuschließende Datensätze** die Option **Filter**.
3. Geben Sie die Bedingungen an, um die Steuertransaktionen der Belege **PIV-110000004** und **INV-10000001** auszuwählen.
4. Wählen Sie **OK** aus.
5. Wählen Sie **OK** aus.
6. Überprüfen Sie das generierte Dokument, das die Steuertransaktionen der ausgewählten Belege enthält.

    ![Vorschauversion des generierten Dokuments mit Steuertransaktionen.](./media/er-data-model-parameterized-calls-output1.png)

### <a name="adjust-the-imported-er-solution"></a>Anpassen der importierten ER-Lösung

Gemäß der neuen Anforderung muss das Dokument, das Sie einreichen müssen, die Namen der Kunden und Lieferanten enthalten, deren Transaktionen enthalten sind. Daher müssen Sie die importierte ER-Lösung so ändern, dass sie ein Dokument generiert, das dieser neuen Anforderung entspricht.

Entscheiden Sie, wie Sie die erforderlichen Modifikationen der importierten ER-Komponenten implementieren möchten.

Der naheliegende Ansatz besteht darin, die folgenden Modifikationen zu implementieren:

- Fügen Sie in Ihrem Datenmodell das neue `Transaction.Party.Name`-Datenmodellfeld vom Typ *Zeichenfolge* hinzu.
- Konfigurieren Sie in Ihrer Modellzuordnung die Bindung für das neue Datenmodellfeld, indem Sie verfügbare Tabellenbeziehungen verwenden, um auf den relevanten Datensatz der `DirPartyTable`-Anwendungstabelle zuzugreifen und den Wert des `Name`-Felds daraus abzurufen.

Obwohl dieser Ansatz funktioniert, kann er Leistungsprobleme in der SQL-Datenbank verursachen, weil `TaxTrans` ist die Transaktionstabelle und kann daher eine große Menge an Datensätzen enthalten. In diesem Fall muss die Anzahl der Aufrufe an `DirPartyTable` gleich der Anzahl der Datensätze in der `TaxTrans`-Tabelle sein, die Leistungsprobleme verursachen kann.

Alternativ können Sie die folgenden Änderungen implementieren:

- Fügen Sie in Ihrem Datenmodell den neuen `Party`-Stamm und das neue `Party.Name`-Feld hinzu.
- Fügen Sie in Ihrer Modellzuordnung eine neue Datenquelle hinzu, die alle Datensätze von Tabellen verbindet, die in Tabellenbeziehungen verwendet werden, um auf den relevanten Datensatz der `DirPartyTable`-Anwendungstabelle zuzugreifen, ausgehend von der `TaxTrans`-Tabelle.

Obwohl dieser Ansatz funktioniert, kann er einige Probleme mit dem Speicherverbrauch verursachen. Auch wenn eine neue [JOIN](er-join-data-sources.md)-Datenquelle als einzelne SQL-Anforderung an die Anwendungsdatenbank ausgeführt wird, um Probleme mit der Datenbankleistung zu vermeiden, muss das Ergebnis in den Speicher des Anwendungsservers abgerufen werden. Da die Anzahl der Datensätze und die Anzahl der Felder in diesen Datensätzen ziemlich groß sein wird, kann dieser Ansatz einen sehr hohen Speicherverbrauch verursachen. Es kann sogar eine Laufzeitausnahme aufgrund fehlenden Arbeitsspeichers ausgelöst werden.

Sie können die Änderungen implementieren, wenn ein laufendes Format im Speicher die eindeutigen Identifikationscodes von Kunden und Lieferanten für alle Steuertransaktionen sammelt, die in einem generierten Bericht angezeigt werden. Da nur eindeutige Codes beibehalten werden sollten, ist der endgültige Satz von Codes nicht groß genug, um den Speicherverbrauch zu beeinflussen. Der Satz von Codes wird dann als Argument eines weiteren Aufrufs der Datenquelle vom Typ *Modell* an die Modellzuordnung übergeben. Basierend auf diesem Aufruf führt die Modellzuordnung eine neue ER-Datenquelle aus, die eine einzelne SQL-Anforderung an die Anwendungsdatenbank sendet, um aus der `DirPartyTable`-Tabelle Datensätze nur für die Parteien abzurufen, deren Codes in dem bereitgestellten Codesatz enthalten sind.

### <a name="adjust-the-imported-data-model"></a>Anpassen des importierten Datenmodells

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. Wählen Sie auf der Seite **Konfigurationen** in der Konfigurationsstruktur im linken Bereich **Beispiel-Überwachungsmodell** aus.
3. Wählen Sie im Inforegister **Versionen** die Version **2** mit dem Status **[Entwurf](general-electronic-reporting.md#component-versioning)** aus.
4. Wählen Sie die Option **Konfigurationskomponenten** Inforegister.
5. Wählen Sie **Designer**, um das Datenmodell für die Bearbeitung zu öffnen.
6. Auf der **Datenmodell**-Seite vergewissern Sie sich, dass das `Root`-Feld ausgewählt ist und wählen dann **Neu** aus.
7. Führen Sie im Drop-Down-Dialogfeld die folgenden Schritte aus:

    1. In der **Neuer Knoten als**-Feldgruppe wählen Sie die Option **Untergeordnetes Element eines aktiven Knotens** aus.
    2. Geben Sie im Feld **Name** die Bezeichnung **Partei** ein.
    3. Wählen Sie im Feld **Artikeltyp** **Datensatzliste** aus.
    4. Wählen Sie **Hinzufügen** aus, um das Hinzufügen des neuen Felds fertigzustellen.

8. Stellen Sie sicher, dass das `Root.Party`-Feld ausgewählt ist, und wählen Sie dann auf der **Knoten**-Registerkarte **Parameter** aus.
9. Führen Sie im Dialogfeld **Parameter** die folgenden Schritte aus:

    1. Auf der Registerkarte **Parameter** wählen Sie **Neu**.
    2. Geben Sie im Feld **Name** die Bezeichnung **PartyRefRecId** ein.
    3. Wählen Sie im Feld **Typ** **Int64** aus.
    4. Aktivieren Sie das **Listen**-Kontrollkästchen.
    5. Wählen Sie **OK** aus, um die Eingabe der Parameter abzuschließen.

    > [!NOTE]
    > Sie haben gerade das `Root.Party`-Datenmodellfeld als Feld konfiguriert, das aufgerufen wird, wenn ein Wert im **PartyRefRecId**-Parameter bereitgestellt wird. Dieser Wert muss in der Liste der Datensätze vorhanden sein, die ein `Value`-Feld des Datentyps *Int64* enthalten.

    ![Parameter-Dialogfeld.](./media/er-data-model-parameterized-calls-model2a.png)

10. Vergewissern Sie sich, dass das `Root.Party`-Feld noch ausgewählt ist, und wählen Sie dann **Neu** aus.
11. Führen Sie im Drop-Down-Dialogfeld die folgenden Schritte aus:

    1. In der **Neuer Knoten als**-Feldgruppe wählen Sie die Option **Untergeordnetes Element eines aktiven Knotens** aus.
    2. Geben Sie im Feld **Name** **Name** ein.
    3. Wählen Sie im Feld **Artikeltyp** **Zeichenfolge** aus.
    4. Wählen Sie **Hinzufügen** aus, um das Hinzufügen des neuen Felds fertigzustellen.

12. Wählen Sie **Speichern** aus, und dann schließen Sie die Seite **Datenmodell**.

    ![Struktur des angepassten ER-Datenmodells auf der Datenmodell-Designerseite.](./media/er-data-model-parameterized-calls-model2b.png)

13. Wählen Sie auf dem Inforegister **Versionen** für Version **2** und dann **Status ändern** \> **Abgeschlossen** aus. Wählen Sie dann **OK** aus.

    > [!NOTE]
    > Ihre Datenmodelländerungen werden in der zweiten Revision der **Beispiel-Überwachungsmodell**- Datenmodellkomponente gespeichert, die sich in der zweiten Version der ER-Konfiguration **Beispiel-Überwachungsmodell** befindet.

![Aktualisierte ER-Datenmodell-Konfiguration auf der Seite „Konfigurationen“.](./media/er-data-model-parameterized-calls-updated-model.png)

### <a name="adjust-the-imported-model-mapping"></a>Anpassung der importierten Modellzuordnung

1. Erweitern Sie auf der Seite **Konfigurationen** in der Konfigurationsstruktur im linken Bereich **Beispiel-Überwachungsmodell**.
2. Wählen Sie **Beispiel für die Zuordnung von Überwachungsmodellen** und dann im **Versionen**-Inforegister die zweite Zuordnungsversion aus, die auf der ersten Datenmodellversion (Version **1.2**) basiert, und die hat einen Status **Entwurf**.
3. Wählen Sie **Zurücksetzen**.
4. In dem **Zielversion**-Feld lassen Sie Version **2** des **Beispiel-Überwachungsmodell**-Basismodells.
5. Wählen Sie **OK** aus, um Ihre Modellzuordnung zurückzusetzen und an den jüngsten Änderungen des Datenmodells auszurichten.

    Beachten Sie, dass sich die Versionsnummer Ihrer bearbeitbaren Modellzuordnung von **1.2** in **2.2** geändert hat, um anzuzeigen, dass die zweite Modellversion derzeit als Basis verwendet wird.

6. Wählen Sie **Designer** aus.
7. Wählen Sie auf der Seite **Zuordnung Modell zu Datenquelle** für die aktuelle Modellzuordnung **Designer** aus.
8. Befolgen Sie diese Schritte, um eine neue Datenquelle zum Zugreifen auf die `DirPartyTable`-Anwendungstabelle hinzuzufügen:

    1. Wählen Sie im Bereich **Datenquellentyp** den Eintrag **Dynamics 365 for Operations \> Tabellendatensätze** aus.
    2. Wählen Sie **Stamm hinzufügen** im Bereich **Datenquellen** aus.
    3. Geben Sie im Feld **Name** die Bezeichnung **PartyTable** ein.
    4. Geben Sie im Feld **Tabelle** den Eintrag **DirPartyTable** ein.
    5. Wählen Sie **OK** aus, um das Hinzufügen der neuen Datenquelle fertigzustellen.

9. Führen Sie diese Schritte aus, um eine neue Datenquelle zur Anforderung von `DirPartyTable`-Datensätzen basierend auf der bereitgestellten Liste von Datensatzidentifikationscodes hinzuzufügen:

    1. Wählen Sie im Bereich **Datenquellentyp** den Eintrag **Allgemein \> Leerer Container** aus.
    2. Wählen Sie **Stamm hinzufügen** im Bereich **Datenquellen** aus.
    3. Geben Sie im Feld **Name** **Daten** ein.
    4. Wählen Sie **OK** aus, um das Hinzufügen der neuen Datenquelle fertigzustellen.
    5. Wählen Sie im Bereich **Datenquellen** die Datenquelle **Daten**.
    6. Wählen Sie im Bereich **Datenquellentyp** den Eintrag **Funktionen \> Berechnetes Feld** aus.
    7. Wählen Sie **Hinzufügen** im Bereich **Datenquellen** aus.
    8. Geben Sie im Feld **Name** die Bezeichnung **DirParty** ein.
    9. Wählen Sie **Formel bearbeiten** aus.
    10. Wählen Sie **Parameter** auf der Seite **Formeldesigner** aus.
    11. Führen Sie im Dialogfeld **Parameter** die folgenden Schritte aus:

        1. Auf der Registerkarte **Parameter** wählen Sie **Neu**.
        2. Geben Sie im Feld **Name** die Bezeichnung **DirPartyID** ein.
        3. Wählen Sie im Feld **Typ** **Int64** aus.
        4. Aktivieren Sie das **Listen**-Kontrollkästchen.
        5. Wählen Sie **OK** aus.

        > [!NOTE]
        > Sie haben dieses berechnete Feld gerade so konfiguriert, dass es zur Laufzeit das Argument eines einzelnen Parameters akzeptiert, der als Datensatzliste mit einem einzigen `Value`-Feld vom Typ *Int64* konfiguriert ist.

    12. Geben Sie im Feld **Formel** den folgenden Ausdruck ein:

        `FILTER(PartyTable, VALUEINLARGE(PartyTable.RecId, DirPartyId, DirPartyId.Value))`

        > [!NOTE]
        > Sie haben gerade das berechnete Feld `DirParty` so konfiguriert, dass nur `DirPartyTable`-Datensätze abgerufen werden, in denen die Datensatzidentifikationscodes in der `DirPartyId`-Liste enthalten sind, die als Argument bereitgestellt wird, wenn das `DirParty`-Feld aufgerufen wird.

        ![Formel zum Abrufen von Parteinamen aus der Anwendungstabelle auf der Formeldesigner-Seite.](./media/er-data-model-parameterized-calls-formula1.png)

    13. Wählen Sie **Speichern** und schließen Sie die Seite **Formeldesginer**.
    14. Wählen Sie **Speichern** und dann **OK** aus, um das Hinzufügen der neuen Datenquelle abzuschließen.

10. Führen Sie die folgenden Schritte aus, um die neue Datenquelle an das neue Datenmodellfeld zu binden, sodass das Datenmodell verwendet wird, um Parteinamen anzuzeigen:

    1. Wählen Sie im **Datenmodell**-Bereich das `Root.Party`-Datenmodellfeld aus.
    2. Wählen Sie **Bearbeiten** im Bereich **Datenmodell** aus.
    3. Geben Sie auf der Seite **Formeldesigner** im Feld **Formel** den Ausdruck `Data.DirParty(PartyRefRecId)` ein.
    4. Wählen Sie **Speichern** und schließen Sie die Seite **Formeldesginer**.

        > [!NOTE]
        > Sie haben gerade die Bindung konfiguriert, um die konfigurierte `Data.DirParty`-Datenquelle aufzurufen und die Liste der Datensatzidentifikationscodes bereitzustellen, die in dem Format angegeben werden, wenn das `Root.Party`-Datenmodellfeld aufgerufen wird.

    5. Wählen Sie im **Datenmodell**-Bereich das `Root.Party.Name`-Datenmodellfeld aus.
    6. Wählen Sie **Bearbeiten** im Bereich **Datenmodell** aus.
    7. Erweitern Sie auf der Seite **Formeldesigner** im Bereich **Datenquelle** den Eintrag **Daten \> DirParty**, und wählen Sie **Name** aus.
    8. Wählen Sie **Datenquelle hinzufügen** aus:
    9. Wählen Sie **Speichern** und schließen Sie die Seite **Formeldesginer**.

    ![Struktur der angepassten ER-Modellzuordnung auf der Seite vom Modellzuordnungsdesigner.](./media/er-data-model-parameterized-calls-mapping2.png)

11. Wählen Sie **Speichern** und schließen Sie die Seite **Modellzuordnungsdesigner**.
12. Schließen Sie die Seite **Zuordnung Modell zu Datenquelle**.
13. Wählen Sie auf dem Inforegister **Versionen** für Version **2.2** und dann **Status ändern \> Abgeschlossen** aus. Wählen Sie dann **OK** aus.

### <a name="adjust-the-imported-format"></a>Anpassung des importierten Formats

1. Wählen Sie auf der Seite **Konfigurationen** **Beispiel-Überwachungsformat**.
2. Wählen Sie im Inforegister **Versionen** die Version **1.2** mit dem Status **Entwurf** aus.
3. Wählen Sie **Zurücksetzen**.
4. In dem **Zielversion**-Feld lassen Sie Version **2** des **Beispiel-Überwachungsmodell**-Basismodells.
5. Wählen Sie **OK** aus, um Ihr Format zurückzusetzen und an den jüngsten Änderungen des Datenmodells auszurichten.
6. Wählen Sie **Designer** aus.
7. Wählen Sie auf der Seite **Formatdesigner** im Formatstrukturbaum im linken Bereich **Aufklappen/Zuklappen** aus.
8. Befolgen Sie diese Schritte, um ein neues Formatelement hinzuzufügen, um Datensatzidentifikationscodes von Parteien zu sammeln, deren Transaktionen in generierten Berichten dargestellt werden.

    1. Wählen Sie im Formatstrukturbaum das Sequenzelement **Report.Row.Trans** aus.
    2. Wählen Sie **Hinzufügen** aus.
    3. Wählen Sie im **Hinzufügen**-Dialogfeld **Datenquelle \> Artikel** aus.
    4. Geben Sie im Dialogfeld **Komponenteneigenschaften** im Feld **Name** **Id** ein.
    5. Wählen Sie im Feld **Datentyp** **Int64** aus.
    6. Wählen Sie **OK** aus.

    > [!NOTE]
    > Ein Element **Datenquelle \> Artikel** kann verwendet werden, um interne Berechnungen und Datentransformationen nur im Rahmen des laufenden Formats durchzuführen. Daher ändern Sie durch Hinzufügen dieses Formatelements nicht den Inhalt eines generierten Dokuments.

9. Befolgen Sie diese Schritte, um neue Formatelemente hinzuzufügen, um Parteinamen in generierte Berichte einzugeben:

    1. Wählen Sie das **Report.Row**-Sequenzelement aus.
    2. Wählen Sie **Hinzufügen** aus.
    3. Wählen Sie im Dialogfeld **Hinzufügen** **Text \> Sequenz** aus.
    4. Geben Sie im Dialogfeld **Komponenteneigenschaften** im Feld **Name** **Party** ein.
    5. Wählen Sie **OK** aus.
    6. Wählen Sie das **Report.Row.Party**-Sequenzelement aus.
    7. Wählen Sie **Hinzufügen** aus.
    8. Wählen Sie im Dialogfeld **Hinzufügen** **Text \> Zeichenfolge** aus.
    9. Geben Sie im Dialogfeld **Komponenteneigenschaften** im Feld **Name** **Name** ein.
    10. Wählen Sie **OK** aus.

10. Befolgen Sie diese Schritte, um eine neue Datenquelle hinzuzufügen, um Datensatzidentifikationscodes von Parteien zu sammeln, deren Transaktionen in generierten Berichten dargestellt werden.

    1. Wählen Sie auf der Registerkarte **Zuordnung** die Option **Stamm hinzufügen** aus.
    2. Im Dialogfeld **Datenquelle hinzufügen** wählen Sie **Funktionen \> Datensammlung**.
    3. Geben Sie im Dialogfeld **Datenquelleneigenschaften „Datensammlung“** im Feld **Name** **PartyIds** ein.
    4. Wählen Sie im Feld **Artikeltyp** **Int64** aus.
    5. Wählen Sie **OK** aus.

11. Befolgen Sie diese Schritte, um eine neue Bindung hinzuzufügen, um Datensatzidentifikationscodes von Parteien zu sammeln, deren Transaktionen in generierten Berichten dargestellt werden.

    1. Wählen Sie im Formatstrukturbaum das Dateneintragelement **Report.Row.Trans.Id** aus.
    2. Wählen Sie **Formel bearbeiten** aus.
    3. Auf der **Formeldesigner**-Seite geben Sie den Ausdruck `PartyIds.Collect(model.Transaction.Party.RecId)` ein.
    4. Wählen Sie **Speichern** und schließen Sie die Seite **Formeldesginer**.

12. Befolgen Sie diese Schritte, um neue Bindungen hinzuzufügen, um Parteinamen in generierte Berichte einzugeben:

    1. Wählen Sie im Formatstrukturbaum das Sequenzelement **Report.Party** aus.
    2. Wählen Sie **Formel bearbeiten** aus.
    3. Auf der **Formeldesigner**-Seite geben Sie den Ausdruck `model.Party(PartyIds.Result)` ein.
    4. Wählen Sie **Speichern** und schließen Sie die Seite **Formeldesginer**.
    5. Wählen Sie im Formatstrukturbaum das Sequenzelement **Report.Party.Name** aus.
    6. Wählen Sie auf der Registerkarte **Zuordnung** das Datenmodellfeld `model.Party.Name` aus.
    7. Wählen Sie **Bindung** aus.

    ![Struktur des angepassten ER-Formats auf der Seite „Formatdesigner“.](./media/er-data-model-parameterized-calls-format2.png)

13. Wählen Sie **Speichern** und schließen Sie die Seite **Formatdesigner**.
14. Schließen Sie die Seite **Zuordnung Modell zu Datenquelle**.
15. Wählen Sie auf dem Inforegister **Versionen** für Version **2.2** und dann **Status ändern** \> **Abgeschlossen** aus. Wählen Sie dann **OK** aus.

### <a name="run-the-adjusted-format"></a>Angepasstes Format ausführen

1. Auf der **Konfigurationen**-Seite wählen Sie **Beispiel-Überwachungsformat** und dann im Aktivitätsbereich **Ausführen** aus.
2. Wählen Sie im Dialogfeld **Elektronische Berichtsparameter** auf der Registerkarte **Einzuschließende Datensätze** die Option **Filter**.
3. Geben Sie die Bedingungen an, um Steuertransaktionen der Belege **PIV-110000004** und **INV-10000001** auszuwählen.
4. Wählen Sie **OK** aus.
5. Wählen Sie **OK** aus.
6. Überprüfen Sie das generierte Dokument, das Steuertransaktionen der ausgewählten Belege und die Namen der entsprechenden Debitoren und Kreditoren enthält.

    ![Vorschauversion des generierten Dokuments mit Steuertransaktionen und Parteinamen.](./media/er-data-model-parameterized-calls-output2.png)

7. Gehen Sie zu **Kreditorenkonten** \> **Kreditoren** \> **Alle Kreditoren**, und überprüfen Sie die Details des ausgewählten Belegs **PIV-110000004**, einschließlich des Kreditorennamens.

    ![Überprüfen der Kaufbelegdetails auf den Seiten „Alle Kreditoren“ und „Rechnungserfassung“.](./media/er-data-model-parameterized-calls-review1.gif)

8. Gehen Sie zu **Debitorenkonten** \> **Debitoren** \> **Alle Debitoren**, und überprüfen Sie die Details des ausgewählten Belegs **INV-10000001**, einschließlich des Debitorennamens.

    ![Überprüfen der Kaufbelegdetails auf den Seiten „Alle Debitoren“ und „Gebuchte Mehrwertsteuer“.](./media/er-data-model-parameterized-calls-review2.gif)

Für weitere Einzelheiten zu dieser Ausführung der ER-Lösung verwenden Sie den integrierten ER-[Leistungsnachverfolgungs](trace-execution-er-troubleshoot-perf.md)-Parser.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Unterstützen parametrisierter Aufrufe von ER-Datenquellen des Typs „Berechnetes Feld“](er-calculated-field-type.md)
- [Überwachen der Ausführung von ER-Formaten zur Behebung von Leistungsproblemen](trace-execution-er-troubleshoot-perf.md)
- [Verwendung von DATA COLLECTION Datenquellen in elektronischen Berichtsformaten](er-data-collection-data-sources.md)
- [ValueInLarge-ER-Funktion](er-functions-logical-valueinlarge.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
