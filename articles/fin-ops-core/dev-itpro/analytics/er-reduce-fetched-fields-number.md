---
title: Verbessern der Leistung von ER-Lösungen, indem die Anzahl der Tabellenfelder reduziert wird, die zur Laufzeit abgerufen werden
description: Dieses Thema erklärt, wie Sie dabei helfen können, die Leistung von ER-Lösungen zu verbessern, indem Sie die Anzahl der Tabellenfelder reduzieren, die zur Laufzeit abgerufen werden.
author: NickSelin
ms.date: 05/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: dd192a7718ac4fd8bcb636ede6c005ca29ee5f08
ms.sourcegitcommit: 336a0ad772fb55d52b4dcf2fafaa853632373820
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/28/2022
ms.locfileid: "8811956"
---
# <a name="improve-performance-of-er-solutions-by-reducing-the-number-of-table-fields-that-are-fetched-at-runtime"></a>Verbessern der Leistung von ER-Lösungen, indem die Anzahl der Tabellenfelder reduziert wird, die zur Laufzeit abgerufen werden

[!include[banner](../includes/banner.md)]

Sie können [Elektronische Berichterstellung](general-electronic-reporting.md) (ER)-[Formate](er-overview-components.md#format-components-for-outgoing-electronic-documents) entwerfen, die ausgehende Dokumente in verschiedenen Formaten generieren. Wenn ein Dokument erzeugt wird, ruft ein ER-Format Datenquellen auf, die in einem entsprechender ER-[Modellzuordnung](er-overview-components.md#model-mapping-component) konfiguriert wurden. Um den Zugriff auf Anwendungstabellen, Abfragen oder Entitäten für das Abrufen von Datensätzen zu konfigurieren, können Sie ER-Datenquellen vom Typ *Tabellendatensätze* verwenden. Standardmäßig ruft eine Datenquelle des *Tabellendatensätze*-Typs die Werte aller Felder in den angeforderten Datensätzen ab. Sie können diese Art von Datenquelle jedoch so konfigurieren, dass sie nur die Feldwerte abruft, die für das laufende ER-Format erforderlich sind. Diese Konfiguration trägt dazu bei, den Speicherverbrauch des Anwendungsservers zu reduzieren, der den Datenabruf und das weitere Zwischenspeichern von Datensätzen durchführt.

Um mehr darüber zu erfahren, wie Sie die Liste der abgerufenen Felder von Datenquellen des *Tabellenaufzeichnungen*-Typs einschränken, schließen Sie das Beispiel in diesem Thema ab.

## <a name="example-reduce-the-number-of-table-fields-that-are-fetched-at-runtime"></a>Beispiel: Reduzieren der Anzahl der Tabellenfelder, die zur Laufzeit abgerufen werden

Die folgenden Verfahren zeigen, wie ein Benutzer in der Rolle „Systemadministrator“ oder „Entwickler für elektronische Berichterstellung“ eine ER-Modellzuordnung so konfigurieren kann, dass nur die Felder abgerufen werden, die zum Ausführen des ER-Formats erforderlich sind, um den Verbrauch des Anwendungsserverspeichers zu reduzieren.

Diese Prozeduren können im Unternehmen **USMF** in Microsoft Dynamics 365 Finance ausgeführt werden. Eine Codierung ist nicht erforderlich.

Um das Beispiel in diesem Thema abzuschließen, müssen Sie für eine der folgenden Rollen Zugriff auf das **USMF**-Unternehmen haben:

- Funktionaler Berater für elektronische Berichterstellung
- Systemadministrator

In diesem Beispiel verwenden Sie die erforderlichen ER-[Konfigurationen](general-electronic-reporting.md#Configuration), die für die Beispielfirma **Litware, Inc.** bereitgestellt werden. Stellen Sie sicher, dass der Konfigurationsanbieter für die Beispielfirma **Litware, Inc.** (`http://www.litware.com`) für das ER Framework aufgeführt und als **Aktiv** markiert ist. Wenn dieser Konfigurationsanbieter nicht aufgeführt ist oder nicht als **Aktiv** markiert ist, folgen Sie den Schritten unter [Erstellen Sie einen Konfigurationsanbieter und markieren Sie ihn als aktiv](tasks/er-configuration-provider-mark-it-active-2016-11.md).

### <a name="configure-the-er-framework"></a>Konfigurieren des EB-Frameworks

Befolgen Sie die Schritte in [ER-Framework konfigurieren](er-quick-start2-customize-report.md#ConfigureFramework), um den minimalen Satz von ER-Parametern einzurichten. Sie müssen diese Einrichtung abschließen, bevor Sie das ER Framework zum Ändern der Datenquellen einer bereitgestellten ER-Lösung verwenden können.

### <a name="import-the-sample-er-configurations"></a>ER-Beispielkonfigurationsdateien importieren

Wenn Sie das Beispiel im [Entwerfen einer neue ER-Lösung, um einen benutzerdefinierten Bericht zu drucken](er-quick-start1-new-solution.md)-Thema noch nicht abgeschlossen haben, laden Sie die XML-Dateien für die folgenden Konfigurationen der bereitgestellten ER-Lösung herunter und speichern Sie sie lokal.

| Inhaltsbeschreibung            | Dateiname |
|--------------------------------|-----------|
| ER-Datenmodell-Konfiguration    | [Questionnaires model.version.1.xml](https://download.microsoft.com/download/b/6/3/b633bd34-d200-4422-96d9-8f62eb5218f8/Questionnaires_model.version.1.xml) |
| Konfiguration der ER-Modellzuordnung | [Questionnaires mapping.version.1.1.xml](https://download.microsoft.com/download/7/b/2/7b258e4e-4bd5-46a4-8114-27419ae4acd8/Questionnaires_mapping.version.1.1.xml) |
| ER-Formatkonfiguration        | [Questionnaires format.version.1.1.xml](https://download.microsoft.com/download/1/b/a/1ba39ec2-257a-44d8-972f-25bf7d18fb41/Questionnaires_format.version.1.1.xml) |

Befolgen Sie dann diese Schritte, um die Konfigurationen der bereitgestellten ER-Lösung in Ihre Finance-Instanz hochzuladen.

1. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
2. Wählen Sie **Berichterstellungskonfigurationen** aus.
3. Importieren Sie auf der Seite **Konfigurationen** die Konfiguration des ER-Datenmodells.

    1. Wählen Sie **Austausch** und dann **Aus XML-Datei laden** aus.
    2. Klicken Sie auf **Durchsuchen**, und wählen Sie die Datei **Questionnaires model.version.1.xml** aus. Wählen Sie dann **OK**.

4. Importieren Sie die Konfiguration für die ER-Modellzuordnung.

    1. Wählen Sie **Austausch** und dann **Aus XML-Datei laden** aus.
    2. Klicken Sie auf **Durchsuchen** und wählen Sie die Datei **Questionnaires mapping.version.1.1.xml** aus. Wählen Sie dann **OK**.

5. Importieren Sie die ER-Formatkonfiguration.

    1. Wählen Sie **Austausch** und dann **Aus XML-Datei laden** aus.
    2. Klicken Sie auf **Durchsuchen** und wählen Sie die Datei **Questionnaires format.version.1.1.xml** aus. Wählen Sie dann **OK**.

6. Erweitern Sie im Konfigurationsbaum **Fragebogenmodell**.
7. Überprüfen Sie die Liste der importierten ER-Konfigurationen in der Konfigurationsstruktur.

    ![Überprüfen der Liste der importierten ER-Konfigurationen auf der Seite „Konfigurationen“.](./media/er-reduce-fetched-fields-number-configurations.png)

### <a name="review-the-provided-er-model-mapping"></a>Überprüfung der bereitgestellten ER-Modellzuordnung

1. Wählen Sie auf der Seite **Konfigurationen** **Fragebogenzuordnung**.
2. Wählen Sie im Aktivitätsbereich **Designer** aus.
3. Wählen Sie auf der Seite **Modell für Datenquellenzuordnung** **Designer** aus.
4. Wählen Sie auf der Seite **Modellzuordnungs-Designer** im Aktionsbereich **Gruppenansicht** aus, um die **Gruppe**-Ansicht zu aktivieren.
5. Erweiteren Sie **Fragebogen** im Bereich **Datenmodell**.

    Beachten Sie, dass die Datenquelle **Fragebogen** so konfiguriert wurde, dass sie auf die Anwendungstabelle `KMCollection` zugreift.

6. Erweitern Sie im Bereich **Datenquellen** den Eintrag **Tabellendatensätze** \> **Fragebogen** \> **Felder** aus.

    Beachten Sie, wie viele Felder aus der `KMCollection`-Anwendungstabelle durch die **Fragebogen**-Datenquelle des *Tabellendatensätze*-Typs dargestellt werden.

    ![Überprüfen der bereitgestellten Modellzuordnung auf der Modellzuordnungs-Designer-Seite, wenn die Gruppenansicht aktiviert ist.](./media/er-reduce-fetched-fields-number-mapping1.png)

7. Wählen Sie im Aktivitätsbereich erneut **Gruppenansicht** aus, um die **Gruppe**-Ansicht zu deaktivieren, und wählen Sie dann **Alle anzeigen** \> **Nur zugeordnete anzeigen** aus.

    Beachten Sie, dass einige Felder der `KMCollection`-Anwendungstabelle zum Ausfüllen der **Fragebogen**-Datensatzliste im ER-Datenmodell verwendet werden:

    - `Active`
    - `Description`
    - `questionMode`
    - `kmCollectionId`

    ![Überprüfen der bereitgestellten Modellzuordnung auf der Modellzuordnungs-Designer-Seite, wenn die Gruppenansicht deaktiviert ist.](./media/er-reduce-fetched-fields-number-mapping2.png)

### <a name="turn-on-the-er-performance-trace"></a>Aktivieren der EB-Leistungsnachverfolgung

Folgen Sie den Schritten in [Die ER-Leistungsverfolgung aktivieren](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace), um die ER-Benutzerparameter zu setzen, die es ermöglichen, die Ausführung von ER-Komponenten nachzuvollziehen.

### <a name="run-the-provided-er-format-by-using-the-provided-model-mapping"></a>Das bereitgestellte ER-Format mithilfe der bereitgestellten Modellzuordnung ausführen

Folgen Sie den Schritten in [Ein entworfenes Format von ER aus ausführen](er-quick-start1-new-solution.md#RunFormatFromER), um das bereitgestellte ER-Format für einen einzelnen Fragebogen auf der **Konfigurationen**-Seite auszuführen.

### <a name="review-the-execution-trace-of-the-first-run"></a>Die Ausführungsablaufverfolgung der ersten Ausführung überprüfen

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung \> Konfigurationen**.
2. Erweitern Sie auf der **Konfigurationen**-Seite **Fragebogen-Modell**, und wählen Sie **Zuordnung von Fragebögen** aus.

    > [!NOTE]
    > Die Angaben auf dem **Versionen**-Inforegister zeigen an, dass Sie die Entwurfsversion der **Zuordnung von Fragebögen**-Konfiguration ausgewählt haben. Daher können Sie den Inhalt dieser Modellzuordnung ändern.

3. Wählen Sie im Aktivitätsbereich **Designer** aus.
4. Wählen Sie auf der Seite **Modell für Datenquellenzuordnung** **Designer** aus.
5. Auf der Seite **Modellzuordnungsdesigner** im Aktivitätsbereich wählen Sie **Leistungsnachverfolgung** aus.
6. Wählen Sie im Dialogfeld **Leistungsablaufverfolgungs-Ergebniseinstellungen** den Trace aus, der beim letzten Formatierungslauf generiert wurde.

    ![Auswählen des Trace im Dialogfeld Leistungsnachverfolgungs-Ergebniseinstellungen.](./media/er-reduce-fetched-fields-number-select-trace-1.png)

7. Wählen Sie **OK** aus. 
8. Filtern Sie auf dem Inforegister **Details** den **Fragebogen**-Pfad, der auf die **Fragebogen**-Datenquelle weist.
9. Überprüfen Sie die Details der Datenbankabfrage, die generiert wurde, als die **Fragebogen**-Datenquelle aufgerufen wurde.

    Beachten Sie, dass alle Felder der `KMCollection`-Anwendungstabelle zur Laufzeit abgerufen wurden, als die **Fragebogen**-Datenquelle aufgerufen wurde.

    ![Überprüfen der Details der Datenbankabfrage auf der Modellzuordnungs-Designer-Seite.](./media/er-reduce-fetched-fields-number-query1.png)

### <a name="modify-the-provided-er-model-mapping"></a>Ändern der bereitgestellten ER-Modellzuordnung

1. Auf der Seite **Modellzuordnungs-Designer** im Bereich **Datenquellen** wählen Sie die Datenquelle **Fragebogen** aus.
2. Wählen Sie im **Datenquellen**-Bereich **Bearbeiten** aus.
3. Wählen Sie im **Datenquelleneigenschaften**-Dialogfeld **Felder auswählen**, um die Liste der Felder der referenzierten `KMCollection`-Anwendungstabelle zu spezifizieren, die zur Laufzeit abgerufen wird, wenn sie bearbeitbare **Fragebogen**-Datenquelle aufgerufen wird.

    ![Wählen Sie „Felder auswählen“ im Datenquelleneigenschaften-Dialogfeld Felder aus, um die Konfiguration der Liste der Felder zu beginnen, die mit der bearbeitbaren Datenquelle aus der Anwendungstabelle abgerufen wird.](./media/er-reduce-fetched-fields-number-select-fields1.png)

4. Wählen Sie auf der **Felder auswählen**-Seite **Automatisches Ausfüllen**.

    Die **Ausgewählte Felder**-Liste wird automatisch basierend auf vorkonfigurierten Artefakten der Modellzuordnung ausgefüllt. Alle Felder und Relationen der referenzierten Tabelle, die in einer Bindung, Formel oder Datenquelle der Modellzuordnung erwähnt werden, werden der Liste hinzugefügt.

    ![Auf der Seite „Felder auswählen“ die Liste der Felder, die aus der Anwendungstabelle abgerufen werden auswählen.](./media/er-reduce-fetched-fields-number-select-fields2.png)

5. Wählen Sie **Speichern** und schließen Sie die Seite **Felder auswählen**.
6. Wählen Sie **OK**, um die Änderungen zu speichern, die Sie an den Datenquelleneinstellungen vorgenommen haben.
7. Wählen Sie im Aktivitätsbereich **Alle anzeigen** aus.

    Beachten Sie, dass die **Fragebogen**-Datenquelle jetzt den Text **\<Fields are filtered\>** zeigt. Dieser Text gibt an, dass die Datenquelle so konfiguriert wurde, dass sie eine begrenzte Anzahl von Feldern aus der referenzierten Anwendungstabelle abruft.

    ![Überprüfen der aktualisierten Modellzuordnung auf der Seite „Modellzuordnungs-Designer“.](./media/er-reduce-fetched-fields-number-mapping3.png)

8. Wählen Sie **Speichern**, um die Änderungen zu speichern, die Sie an den bearbeitbaren Modellzuordnung vorgenommen haben.

    > [!NOTE]
    > Zur Laufzeit analysiert ER die hinzugefügten Beziehungen und fügt alle Felder, die darin verwendet werden, zur Datenbankabfrage hinzu, selbst wenn diese Felder zur Entwurfszeit nicht explizit zur Liste der abgerufenen Felder hinzugefügt wurden.

### <a name="run-the-provided-er-format-by-using-the-updated-model-mapping"></a>Das bereitgestellte ER-Format mithilfe der aktualisierten Modellzuordnung ausführen

Folgen Sie den Schritten in [Ein entworfenes Format von ER aus ausführen](er-quick-start1-new-solution.md#RunFormatFromER), um das bereitgestellte ER-Format für einen einzelnen Fragebogen auf der **Konfigurationen**-Seite auszuführen.

### <a name="review-the-execution-trace-of-the-second-run"></a>Die Ausführungsablaufverfolgung der zweiten Ausführung überprüfen

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. Erweitern Sie auf der **Konfigurationen**-Seite **Fragebogen-Modell**, und wählen Sie **Zuordnung von Fragebögen** aus.
3. Wählen Sie im Aktivitätsbereich **Designer** aus.
4. Wählen Sie auf der Seite **Modell für Datenquellenzuordnung** **Designer** aus.
5. Auf der Seite **Modellzuordnungsdesigner** im Aktivitätsbereich wählen Sie **Leistungsnachverfolgung** aus.
6. Wählen Sie im Dialogfeld **Leistungsablaufverfolgungs-Ergebniseinstellungen** den Trace aus, der beim letzten Formatierungslauf generiert wurde.
7. Wählen Sie **OK** aus.
8. Filtern Sie auf dem Inforegister **Details** den **Fragebogen**-Pfad, der auf die **Fragebogen**-Datenquelle weist.
9. Überprüfen Sie die Details der Datenbankabfrage, die generiert wurde, als die **Fragebogen**-Datenquelle aufgerufen wurde.

    Beachten Sie, dass nur die Felder, die zum Ausfüllen der Datenquelle erforderlich sind, zur Laufzeit aus der `KMCollection`-Anwendungstabelle abgerufen wurden, wenn die **Fragebogen**-Datenquelle aufgerufen wurde.

    > [!NOTE]
    > Einige Felder, z. B. die Felder für die Partitions-ID, die Datenbereichs-ID und die Datensatz-ID, werden automatisch vom Datenmanagement-Framework der Finance-App hinzugefügt.

    ![Überprüfen der Details der Datenbankabfrage für die aktualisierte Modellzuordnung auf der Modellzuordnungs-Designer-Seite.](./media/er-reduce-fetched-fields-number-query2.png)

Sie können diese Technik verwenden, um die Anzahl der abgerufenen Datensätze zu reduzieren, wenn Sie den Speicherverbrauch durch die laufende ER-Modellzuordnung und das ER-Format reduzieren müssen.

## <a name="limitations"></a>Einschränkungen

Wenn Sie die Anzahl der abgerufenen Felder für eine Datenquelle des *Tabellenaufzeichnungen*-Typs begrenzen, können Sie die Methoden einer Anwendungstabelle, auf die sich die Datenquelle bezieht, nicht verwenden, da die Anwendungsmetadaten keine Informationen zu Tabellenfeldern bereitstellen, die zum Aufrufen dieser Methoden erforderlich sind.

## <a name="usage-notes"></a>Anwendungshinweise

Obwohl der **Automatisches Ausfüllen**-Befehl automatisch Felder hinzufügt, werden jedoch zuvor hinzugefügte Felder nicht automatisch gelöscht, auch wenn sie nicht mehr in Bindungen, Formeln und Datenquellen der bearbeitbaren Modellzuordnung verwendet werden.

Wenn Sie **Automatisches Ausfüllen** auswählen, analysiert ER Bindungen, Formeln und die Datenquellen, die die bearbeitbare Modellzuordnung hatte, als Sie sie zur Bearbeitung geöffnet haben. Wenn Sie Bindungen, Formeln und Datenquellen der bearbeitbaren Modellzuordnung ändern und den **Automatisches Ausfüllen**-Befehl verwenden möchten, schließen Sie den Modellzuordnungs-Designer und öffnen Sie ihn dann erneut, um Ihre Modellzuordnung zu bearbeiten. 

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Überwachen der Ausführung von ER-Formaten zur Behebung von Leistungsproblemen](trace-execution-er-troubleshoot-perf.md)
- [Beheben von Leistungsproblemen in ER-Konfigurationen](er-troubleshoot-perf-issues-in-configurations.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
