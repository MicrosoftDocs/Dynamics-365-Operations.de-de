---
title: Automatisiertes Testen mit elektronischen Berichten
description: In diesem Thema wird erläutert, wie Sie die Basisfunktion des Frameworks für elektronische Berichterstellung (ER) verwenden können, um Funktionstests zu automatisieren.
author: NickSelin
manager: AnnBe
ms.date: 07/02/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERFormatBaselineTable, ERFormatMappingRunLogTable, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 503d4ca562df5c60ee7c475ac146dffbe0edc0c9
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569044"
---
# <a name="automate-testing-with-electronic-reporting"></a>Automatisiertes Testen mit elektronischen Berichten

[!include[banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie das Framework für elektronische Berichterstellung (ER) verwenden können, um das Testen einiger Funktionen zu automatisieren. Das Beispiel in diesem Thema zeigt, wie die die Tests der Kreditorenzahlungsverarbeitung automatisiert werden kann.

Die Anwendung verwendet das ER-Framework, um Zahlungsdateien und entsprechende Dokumente während des Lieferantenzahlungsvorgangs zu generieren. Das ER-Framework besteht aus einem Datenmodell, Modellzuordnungen und Formatkomponenten, die die Zahlungsverarbeitung für verschiedene Zahlungsarten und die Erstellung von Dokumenten in verschiedenen Formaten unterstützen. Diese Komponenten können von Microsoft Dynamics Lifecycle Services (LCS) heruntergeladen und in die Instanz importiert werden.

Sie können auch jede Microsoft-Komponente anpassen und als Grundlage Ihrer eigenen benutzerdefinierten Komponente verwenden. Wenn Sie eine benutzerdefinierte Version erstellen, können Sie Änderungen vornehmen, die bestimmte Anforderungen unterstützen. Beispielsweise können Sie das ER-Datenmodell und die ER-Modellzuordnung anpassen, um auf kundenspezifische Anwendungsdaten zuzugreifen, oder Sie können ein ER-Format ändern, um das Layout eines generierten Dokuments zu ändern.

Sie können benutzerdefinierte ER-Formate verwenden, um Zahlungsdateien zu verarbeiten, die Lieferantenzahlungen generieren, und um Steuerungsberichte zu verarbeiten. Die Versionsverwaltung wird in ER-Komponenten unterstützt. Daher kann Microsoft aktualisierte Versionen von ER-Lösungen für die Verarbeitung von Lieferantenzahlungen bereitstellen, und Sie können die aktualisierte Version automatisch mit der benutzerdefinierten Komponente zusammenführen, indem Sie eine Rebasierung dafür durchführen. Sie müssen jedoch die erneut basierte Version jedoch testen, um sicherzustellen, dass sie erwartungsgemäß arbeitet.

ER-Datenmodelle und ER-Modellzuordnungen sind für viele ER-Formate üblich, die, verwendet werden, um Zahlungen verschiedener Arten zu verarbeiten und länder-/regionsspezifische Zahlungsdokumente zu generieren. Daher ist es unbedingt geboten, Benutzerakzeptanz und Integrationstests zu automatisieren, sodass sie automatisch in mehreren Unternehmen ausgeführt werden, aber den Landes-/Regionskontext jedes Zielunternehmens berücksichtigen, verschiedene Datasets verwenden usw.

Weitere Informationen dazu, wie Sie eine benutzerdefinierte Version eines Formats erstellen, das auf dem Format basiert, das Sie von einem Konfigurationsanbieter erhalten haben, finden Sie unter [ER – Aktualisieren Sie Ihr Format durch Verwendung einer neuen Basisversion dieses Formats](./tasks/er-upgrade-format.md).

## <a name="key-concepts"></a>Schlüsselkonzepte

Funktionale Poweruser können Benutzerakzeptanz- und Integrationstests erstellen, ohne Quellcode zu schreiben.

- Verwenden Sie die ER-Ausgangswertefunktion, um generierte Dokumente mit Masterkopien zu vergleichen. Weitere Informationen finden Sie unter [Nachverfolgung erstellter Berichtsergebnisse und Vergleich mit Ausgangswerten](er-trace-reports-compare-baseline.md).
- Verwenden Sie die Aufgabenaufzeichnung, um Testfälle zu erfassen, und schließen Sie eine Ausgangswertebewertung ein. Weitere Informationen finden Sie unter [Ressourcen für Aufgabenaufzeichnung](../user-interface/task-recorder.md).
- Gruppieren von Testfällen für erforderliche Testszenarien. Weitere Informationen finden Sie unter [Benutzerakzeptanztests erstellen und automatisieren](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md).

    - Verwenden Sie Geschäftsprozessmodellierer (BPM) in LCS , um Bibliotheken für Benutzerakzeptanztests zu erstellen.
    - Verwenden Sie BPM-Testbibliotheken, um in Microsoft Azure DevOps Services (Azure DevOps) einen Testplan und Testsuiten zu erstellen.

Funktionale Powernutzer können Benutzerakzeptanz- und Integrationstests durchführen.

- Verwenden Sie das Regression Suite Automation Tool (RSAT), um Testfälle der gewünschten Testsuite auszuführen.
- Melden Sie die Ergebnisse der Tests in Azure DevOps, und verwenden Sie diesen Dienst, um diese Ergebnisse zu untersuchen.

## <a name="prerequisites"></a>Voraussetzungen

Bevor Sie die Aufgaben in diesem Thema abschließen können, müssen die folgenden Voraussetzungen abgeschlossen werden:

- Stellen Sie eine Topologie bereit, die Testautomatisierung unterstützt. Sie müssen Zugriff auf die Instanz dieser Topologie für die **Systemadministrator**-Rolle haben. Diese Topologie muss die Demodaten enthalten, die in diesem Beispiel verwendet werden. Weitere Informationen finden Sie unter [Bereitstellen und Verwenden von Umgebungen, die fortlaufende und Build- und Testautomatisierung unterstützen](../perf-test/continuous-build-test-automation.md).
- Um Benutzerakzeptanz- und Integrationstests automatisch zu erstellen, müssen Sie RSAT in der Topologie installieren, die Sie verwenden und in der entsprechenden Art konfigurieren. Informationen darüber, wie Sie RSAT installieren und so konfigurieren, dass es mit den Finance and Operations-Apps und Azure DevOps funktioniert, finden Sie unter [Regression Suite Automation Tool](https://www.microsoft.com/download/details.aspx?id=57357). Beachten Sie die Voraussetzungen für die Verwendung des Tools. Die folgende Abbildung zeigt ein Beispiel der RSAT-Einstellungen. Das blaue Rechteck schließt die Parameter ein, die den Zugriff auf Azure DevOps angeben. Das grüne Rechteck schließt die Parameter ein, die den Zugriff auf die Instanz angeben.

    ![RSAT-Einstellungen](media/GER-Configure.png "Screenshot des Dialogfelds „RSAT-Einstellungen“")

- Um Testfälle in den Suiten zu organisieren, mit deren Hilfe die korrekte Ausführungssequenz sichergestellt wird, damit Sie Protokolle der Testausführungen für weitere Berichterstellung und Untersuchung erfassen können, müssen Sie über die bereitgestellte Topologie auf Azure DevOps zugreifen können.
- Um das Beispiel in diesem Thema durchzuführen, sollten Sie [Er-Verwendung für RSAT-Tests](https://go.microsoft.com/fwlink/?linkid=874684) herunterladen. Diese ZIP-Datei enthält die folgenden Aufgaben-Guides:

    | Inhalt                                           | Dateiname und Speicherort |
    |---------------------------------------------------|------------------------|
    | Beispielaufgabenaufzeichnung, um Daten für das Testen vorbereiten | Recording.xml\\vorbereiten |
    | Beispielaufgabenaufzeichnung für die Verarbeitung von Kreditorenzahlung   | Recording.xml\\verarbeiten |

## <a name="prepare-the-accounts-payable-module-to-process-vendor-payments"></a>Bereiten Sie die Kreditorenkontenmodul vor, um Kreditorenzahlungen zu verarbeiten

1. Anmelden bei Ihrer Instanz.
2. Laden Sie die folgenden ER-Konfigurationen aus LCS herunter. Anwendungen finden Sie unter [ER Import einer Konfiguration von Lifecycle Services](./tasks/er-import-configuration-lifecycle-services.md).

    - **Zahlungsmodell**-ER-Modell-Konfiguration
    - **Zahlungsmodellzuordnung 1611** ER-Modellzuordnungskonfiguration
    - **BACS (UK)**-ER-Formatkonfiguration

    ![Elektronische Berichtskonfigurationen](media/GER-Configurations.png "Screenshot der Konfigurationsseite in der elektronischen Berichterstellung")

3. Wählen Sie die **GBSI**-Demodatunternehmen aus, das einen Land-/Regionskontext in Großbritannien hat.
4. Kreditorenkontenparameter konfigurieren:

    1. Wechseln Sie zu **Kreditorenkonten \> Zahlungseinstellungen \> Zahlungsmethoden**.
    2. Wählen Sie die Zahlungsmethode **Elektronisch** aus.
    3. Konfigurieren Sie die ausgewählte Zahlungsmethode, damit sie das ER-Format **BACS (UK)** verwendet, das Sie zuvor für die Kreditorenzahlungsverarbeitung heruntergeladen haben:

        1. Legen Sie im Inforegister **Dateiformate** die Option **Generisches elektronisches Exportformat** auf **Ja** fest.
        2. Wählen Sie im Feld **Exportformatkonfiguration** **BACS (UK)** aus.

    ![Seite für Zahlungsmethoden](media/GER-APParameters.png "Screenshot der Seite der Zahlungsmethode")

    > [!NOTE]
    > Wenn Sie die abgeleitete Version dieses ER-Formats haben, die erstellt wurde, um Anpassungen zu unterstützen, können Sie diese Konfiguration in der Zahlungsmethode **Elektronisch** auswählen.

5. Erstellen Sie eine Beispielskreditorenzahlung:

    1. Wechseln Sie zu **Kreditorenkonten \> Zahlungen \> Zahlungserfassung**.
    2. Stellen Sie sicher, dass Sie nicht die Zahlungserfassung nicht gebucht haben.

        ![Seite für Zahlungserfassung](media/GER-APJournal.png "Screenshot der Seite der Zahlungserfassung")

    3. Wählen Sie **Positionen** aus, und geben Sie eine Position ein, die die folgenden Informationen enthält.

        | Feld               | Beispielswert   |
        |---------------------|-----------------|
        | Kreditorenname         | GB\_SI\_000001  |
        | Soll               | 1,000.00        |
        | Währung            | GBP             |
        | Gegenkontenart | Bank            |
        | Gegenkonto      | GBSI OPER       |
        | Zahlungsmethode   | Elektronisch      |

    ![Seite für Kreditorenzahlungen](media/GER-APJournalLines.png "Screenshot der Seite der Lieferantenzahlung")

## <a name="prepare-the-er-framework-to-test-vendor-payment-processing"></a>Bereiten Sie das ER-Framework vor, um die Kreditorenzahlungsverarbeitung zu testen

### <a name="configure-er-parameters"></a>Parameter der elektronischen Berichterstellung konfigurieren

1. Wechseln Sie zu **Organisationsverwaltung \>Elektronische Berichterstellung \> Parameter für elektronische Berichterstellung**.
2. Wählen Sie auf der Registerkarte **Anhänge** im Feld **Ausgangswert** **Datei** als den Dokumenttyp aus, das vom Dokumenteverwaltungs(DM)-Framework verwendet wird, um Dokumente zu behalten, die als DM-Anhänge der Ausgangswertefunktion zugeordnet sind.

    ![Parameterseite der elektronischen Berichterstellung](media/GER-ERParameters.png "Screenshot der Seite der Parameter für elektronische Berichterstellung")

### <a name="generate-baseline-copies-of-vendor-paymentrelated-documents"></a>Generieren Sie Ausgangswertekopien von Kreditorzahlungen in Zusammenhang mit Dokumenten

1. Wechseln Sie zu **Kreditorenkonten \> Zahlungen \> Zahlungserfassung**.
2. Wählen Sie **Positionen** aus.
3. Wählen Sie **Zahlungen generieren** aus.
4. Wählen Sie die Zahlungsmethode **Elektronisch** aus.
5. Wählen Sie das Bankkonto **GBSI OPER** aus.
6. legen Sie die **Kontrollbereicht drucken** auf **Ja** fest.
7. Laden Sie die generierte Ausgabe als ZIP-Datei herunter.
8. Die heruntergeladene Datei öffnen.
9. Extrahieren Sie die folgenden Dateien aus der heruntergeladenen Datei:

    - **Datei** Zahlungsdatei im Textformat
    - **ERVendOutPaymControlReport**-Kontrollberichtdatei in XLSX-Format

    ![Extrahierte Dateien](media/GER-APJournalProcessed.png "Screenshot der extrahierten Dateinamen im Windows-Explorer")

### <a name="turn-on-the-er-baseline-feature"></a>Aktivieren Sie die ER-Ausgangswertefunktion

1. Wechseln Sie zu **Organisationsverwaltung \> Elektronische Berichterstellung \> Konfigurationen**.
2. Klicken Sie im Aktivitätsbereich auf die Registerkarte **Konfigurationen**, und wählen Sie **Benutzerparameter** aus.
3. Legen Sie die Option **In Debugmodus ausführen** auf **Ja** fest.

Wenn Sie den Parameter **In Debugmodus ausführen** aktivieren, möchten,zwingen Sie das ER-Framework, nach der Ausführung eines beliebigen ER-Formats die folgenden Aktivitäten auszuführen, das ausgehende Dokumente generiert:

1. Legen Sie fest, ob ein Ausgangswert für jede Komponente des ausgeführten ER-Formats konfiguriert wurde.
2. Bestimmen Sie, ob jeder konfigurierter Ausgangswert in den aktuellen Bedingungen gilt (Unternehmenscode der angemeldeten Unternehmens, des Dateinamens und der Dateinamenerweiterung der generierten Ausgabe, usw.).
3. Für jeden entsprechenden Ausgangswert führen Sie die folgenden Aktivitäten aus:

    1. Vergleichen Sie die Ausgabe, die bei der Ausführung des ER-Formats mit dem entsprechenden Ausgangswert generiert wird.
    2. Speichern Sie die Ergebnisse des Vergleichs im Debug-Protokoll der ER-Konfigurationen.

### <a name="configure-er-baselines-for-vendor-payment-processing"></a>Konfigurieren Sie ER-Ausgangswerte für die Kreditorenzahlungsverarbeitung

1. Wechseln Sie zu **Organisationsverwaltung \> Elektronische Berichterstellung \> Konfigurationen**.
2. Wählen Sie **Ausgangswerte** aus.
3. Wählen Sie **Neu** aus.
4. Wählen Sie im Feld **Verweis** das Format **BACS (UK)** aus.
5. Wählen Sie **Anhänge** aus.
6. Fügen Sie einen neuen Ausgangswert für die Kreditorenzahlungsdatei hinzu:

    1. Wählen Sie **Neu** aus.
    2. Wählen Sie im Feld **Typ** den DM-Dokumenttyp **Datei** aus, den Sie in den ER-Parametern konfigurierten, um Ausgangswertartefakte zu speichern.
    3. Durchsuchen Sie sich, um die lokal gespeicherte Zahlungsdatei **Datei** im Textformat auszuwählen.
    4. Geben Sie im Feld **Beschreibung** **Zahlungs-TXT-Datei** ein.

7. Fügen Sie dem Kontrollbericht für die Kreditorenzahlung einen neuen Ausgangswert hinzu:

    1. Wählen Sie **Neu** aus.
    2. Wählen Sie im Feld **Typ** den DM-Dokumenttyp **Datei** aus, den Sie in den ER-Parametern konfigurierten, um Ausgangswertartefakte zu speichern.
    3. Durchsuchen Sie sie, um die lokal gespeicherte Zahlungsdatei **ERVendOutPaymControlReport** im XLSSX-Format auszuwählen.
    4. Geben Sie im Feld **Beschreibung** **Zahlungs-XLSX-Kontrollbericht** ein.

    ![Ausgangswere für die Kreditorenzahlungsdatei und den Kontrollbericht](media/GER-BaselineAttachments.png "Screenshot der Konfigurationsseite mit dem ausgewählten Zahlungs-XLSX-Kontrolblericht")

8. Schließen Sie die Seite.
9. Auf dem Inforegister **Ausgangswerte** wählen Sie **Neu** aus, um einen Ausgangswert für die Zahlungsdatei zu konfigurieren:

    1. Geben Sie der Zeile den Namen **Ausgangswerteinstellungen für Zahlungsdatei**.
    2. Wählen Sie im Feld **Dateikomponentenname** **Datei** aus, um diese Ausgangswerte bei der ER-Formatausgabe anzuwenden, die die Zahlungsdatei im Textformat BACS (UK) generiert.
    3. Wählen Sie im Feld **Unternehmen** **GBSI** aus, um diesen Ausgangswert anzuwenden, wenn das ER-Format **BACS (UK)** im GBSI-Unternehmen ausgeführt wird.
    4. Im Feld **Dateinamenmaske** geben Sie **\*.TXT** ein, um den Ausgangswert nur auf Ausgaben der Formatkomponente **Datei** anzuwenden, die die **.txt**-Dateinamenserweiterung haben.
    5. Wählen Sie im Feld **Ausgangswert** **TXT-Datei für Zahlung** aus, damit dieser Ausgangswert für den Vergleich mit der generierten Ausgabe verwendet wird.

10. Wählen Sie **Neu** aus, um einen Ausgangswert für den Kontrollbericht zu konfigurieren:

    1. Geben Sie der Zeile den Namen **Ausgangswerteinstellungen für Kontrollbericht**.
    2. Wählen Sie im Feld **Dateikomponentenname** **ERVendOutPaymControlReport** aus, um diese Ausgangswerte bei der ER-Formatausgabe anzuwenden, die den Kontrollbericht generiert.
    3. Wählen Sie im Feld **Unternehmen** **GBSI** aus, um diesen Ausgangswert anzuwenden, wenn das ER-Format **BACS (UK)** im GBSI-Unternehmen ausgeführt wird.
    4. Im Feld **Dateinamenmaske** geben Sie **\*.XLSX** ein, um den Ausgangswert nur auf Ausgaben der Formatkomponente **ERVendOutPaymControlReport** anzuwenden, die die **.xlsx**-Dateinamenserweiterung haben.
    5. Wählen Sie im Feld **Ausgangswert** **XLSX-Kontrollbericht für Zahlung** aus, damit dieser Ausgangswert für den Vergleich mit der generierten Ausgabe verwendet wird.

    ![Inforegister „Grundlagen“ auf der Seite „Konfigurationen“](media/GER-BaselineRules.png "Screenshot des Inforegisters „Grundlagen“ auf der Seite „Konfigurationen“")

## <a name="record-tests-to-validate-vendor-payment-processing"></a>Erfassen Sie Tests, um die Kreditorenzahlungsverarbeitung zu überprüfen

Als funktionaler Poweruser können Sie Ihre eigenen Schritte erfassen, um die Kreditorenzahlungsverarbeitung zu testen. Es wird empfohlen, dass Sie die Aufgabenaufzeichnung **Recording.xml\\vorbereiten** wiedergeben (und nach Bedarf bearbeiten), die Sie zuvor heruntergeladen haben. Diese Aufnahme wird verwendet, um alle Testdaten auf den korrekte Status festzulegen. Dieser Schritt ist erforderlich, da die Tests mehrmals durchgeführt werden können und für jeden Test Daten verwendet werden müssen, die den gleichen Status besitzen.

### <a name="reset-user-settings"></a>Benutzereinstellungen zurücksetzen

1. Öffnen Sie das Standard-Dashboard.
2. Wählen Sie die Schaltfläche **Einstellungen** (Zahnradsymbol) aus.
3. Wählen Sie **Benutzeroptionen** aus.
4. Wählen Sie **Nutzungsdaten** aus.
5. Wählen Sie **Zurücksetzen** aus.
6. Wählen Sie **Ja** aus, um zu bestätigen, dass Sie die Nutzungsdaten zurücksetzen möchten.
7. Schließen Sie die Seite.

### <a name="record-the-steps-to-prepare-data-for-testing"></a>Erfassen Sie die Schritte, um Daten für das Testen vorbereiten

1. Wählen Sie die Schaltfläche **Einstellungen** (Zahnradsymbol) aus.
2. Wählen Sie **Aufgabenaufzeichnung** aus.
3. Wählen Sie **Aufzeichnung wiedergeben** aus.
4. Wählen Sie **Von diesem PC öffnen** aus.
5. Wählen Sie **Durchsuchen** und die lokal gespeicherte Datei **Recording.xml\\vorbereiten** aus.
6. Wählen Sie **Starten** aus.
7. Wählen Sie weiterhin **Nächsten ausstehenden Schritt wiedergeben** aus, bis alle Schritte in die Aufzeichnung wiedergegeben wurden.

Diese Aufgabenaufzeichnung führt die folgenden Aktivitäten aus:

1. Dden Status der verarbeiteten Zahlungsposition auf **Keiner** festlegen.

    ![Aufgabenaufzeichnungsschritte 3 bis 4](media/GER-Recording1Review1.png "Screenshot der Aufgabenaufzeichnungsschritte 3 bis 4")

2. Schalten Sie den Benutzerparameter **In Debugmodus ausführen** ein.

    ![Aufgabenaufzeichnungsschritte 9 bis 10](media/GER-Recording1Review2.png "Screenshot der Aufgabenaufzeichnungsschritte 9 bis 10")

3. Säubern Sie das ER-Debug-Protokoll, in dem die Ergebnisse des Vergleichs der generierten Dateien mit den Ausgangswerten enthalten sind.

    ![Aufgabenaufzeichnungsschritte 13 bis 15](media/GER-Recording1Review3.png "Screenshot der Aufgabenaufzeichnungsschritte 13 bis 15")

### <a name="record-the-steps-to-test-vendor-payment-processing"></a>Erfassen Sie die Schritte zum Testen der Kreditorenzahlungsverarbeitung

Es wird empfohlen, dass Sie die Aufgabenaufzeichnung **Recording.xml\\verarbeiten** wiedergeben (und nach Bedarf bearbeiten), die Sie zuvor heruntergeladen haben. Diese Erfassung wird verwendet, um Kreditorenzahlungen zu verarbeiten und die Ergebnisse des Vergleichs der generierten Dokumente mit den entsprechenden Ausgangswerten zu prüfen.

1. Wählen Sie die Schaltfläche **Einstellungen** (Zahnradsymbol) aus.
2. Wählen Sie **Aufgabenaufzeichnung** aus.
3. Wählen Sie **Aufzeichnung wiedergeben** aus.
4. Wählen Sie **Von diesem PC öffnen** aus.
5. Wählen Sie **Durchsuchen** und die lokal gespeicherte Datei **Recording.xml\\vberarbeiten** aus.
6. Wählen Sie **Starten** aus.
7. Wählen Sie weiterhin **Nächsten ausstehenden Schritt wiedergeben** aus, bis alle Schritte in die Aufzeichnung wiedergegeben wurden.

Diese Aufgabenaufzeichnung führt die folgenden Aktivitäten aus:

1. Kreditorenzahlungsverarbeitung starten
2. Legen Sie die richtigen Laufzeitparameter fest, und schalten Sie Generierung eines Kontrollberichts ein.

    ![Aufgabenaufzeichnungsschritte 3 bis 8](media/GER-Recording2Review1.png "Screenshot der Aufgabenaufzeichnungsschritte 3 bis 8")

3. Greifen Sie auf das ER-Debug-Protokoll zu, um die Ergebnisse des Vergleichs der generierten Ausgaben mit den ensprechenden Ausgangswerten aufzuzeichnen.

    Im ER-Debug-Protokoll werden die Ergebnisse des Vergleichs im Feld **Generierter Text** angezeigt. Die Felder **Formatkomponente** und **Formatpfad, der einen Protokolleintrag verursacht hat** beziehen sich auf die Dateikomponente, mit dem die generierte Ausgabe des Ausgangswerts verglichen wurde.

    ![Einträge auf der Seite für Elektronische Berichterstellungsausführungsprotokolle](media/GER-ERDebugLog.png "Screenshot der Einträge auf der Seite für Elektronische Berichterstellungsausführungsprotokolle")

4. Der Vergleich der aktuellen Ausgabe zu den Ausgangswerten wird aufgezeichnet, indem Sie die Aufgabenaufzeichnungsoption **Überprüfen** verwenden und **Aktueller Wert** auswählen.

    ![Verwendung der Option „Überprüfen“ für den Vergleich mit dem aktuellen Wert](media/GER-TRRecordValidation.png "Screenshot der Verwendung der Option „Überprüfen“ für den Vergleich mit dem aktuellen Wert")

    Die folgende Abbildung zeigt, wie die aufgezeichneten Prüfungsschritte in der Aufgabenaufzeichnung aussehen.

    ![Aufgabenaufzeichnungsschritte 13 und 15](media/GER-Recording2Review2.png "Screenshot der Aufgabenaufzeichnungsschritte 13 und 15")

## <a name="add-the-recorded-tests-to-azure-devops"></a>Fügen Sie die aufgezeichneten Tests Azure DevOps hinzu

1. Öffnen Sie die Azure DevOps-Umgebung.
2. Wählen Sie das Projekt aus, das Sie in den RSAT-Parametern definiert haben, als Sie [das Tool konfiguriert](#prerequisites) haben.
3. Wählen Sie den Testplan aus, das Sie in den RSAT-Parametern definiert haben, als Sie [das Tool konfiguriert](#prerequisites) haben.
4. Neuen Testfall für den ausgewählten Testplan erstellen:

    1. Geben Sie dem Testfall den Namen **Daten zum Testen der Verarbeitung der elektronischen Zahlung des Kreditors vorbereiten**.
    2. Fügen Sie die Datei **Recording.xml** aus dem Ordner **Vorbereiten** an, den Sie zuvor heruntergeladen haben.

5. Neuen Testfall für den ausgewählten Testplan erstellen:

    1. Geben Sie dem Testfall den Namen **Testen der Verarbeitung von Kreditorenzahlungen unter Verwendung des ER-Format BACS (UK)**.
    2. Fügen Sie die Datei **Recording.xml** aus dem Ordner **Verarbeiten** an, den Sie zuvor heruntergeladen haben.

    ![Neuen Testfälle für den ausgewählten Testplan](media/GER-RSAT-DevOps-Tests-Passed.png "Screenshot der neuen Testfälle für den ausgewählten Testplan")

> [!NOTE]
> Beachten Sie die korrekte Ausführungsreihenfolge der Tests, die hinzugefügt werden.

## <a name="prepare-rsat-to-run-the-recorded-tests"></a>Bereiten Sie RSAT vor, um die aufgezeichneten Tests vorzunehmen

### <a name="load-the-tests-from-azure-devops-to-rsat"></a>Laden Sie die Tests von Azure DevOps auf RSAT

1. Öffnen Sie die lokale RSAT-Anwendung in der aktuellen Topologie.
2. Wählen Sie **Laden** aus, um die Tests zu laden, die sich derzeit in Azure DevOps befinden in RSAT.

    ![In RSAT geladene Tests](media/GER-RSAT-RSAT-Tests-Loaded.png "Screenshot der in RSAT geladenen Tests")

### <a name="create-automation-and-parameters-files"></a>Automatisierungs- und Parameterdateien erstellen

1. Wählen Sie in RSAT die Tests aus, die Sie von Azure DevOps geladen haben.
2. Wählen Sie **Neu** aus, um RAST-Automatisierungs- und -Parameterdateien zu erstellen.

    ![In RAST erstellte RSAT-Automatisierungs- und -Parameterdateien](media/GER-RSAT-RSAT-Tests-Initiated.png "Screenshot der in RAST erstellten RSAT-Automatisierungs- und -Parameterdateien")

### <a name="modify-the-parameters-files"></a>Ändern der Parameterdateien

1. Wählen Sie in RAST den Testfall **Daten zum Testen der Verarbeitung der elektronischen Zahlung des Kreditors vorbereiten** aus.
2. Wählen Sie **Bearbeiten** aus.
3. Ändern Sie in der Microsoft Excel-Arbeitsmappe, die im Arbeitsblatt **Allgemein** geöffnet ist, den Unternehmenscode zu **GBSI**, da dieses Unternehmen für die Testausführung verwendet wird.
4. Wählen Sie in RSAT den Testfall **Testen der Verarbeitung von Kreditorenzahlungen unter Verwendung des ER-Format BACS (UK)** aus.
5. Wählen Sie **Bearbeiten** aus.
6. In der Excel-Arbeitsmappe, die im Arbeitsblatt **Allgemein** geöffnet ist, ändern Sie den Unternehmenscode zu **GBSI**.
7. Beachten Sie im Arbeitsblatt **ERFormatMappingRunLogTable**, dass die Zellen A :3 und C: 3 den Text der Felder in der ER-Debug-Protokolltabelle enthalten, die verwendet werden, um die Ergebnisse des Vergleichs der Ausgabe mit den Ausgangswerten zu prüfen. Diese Texte werden verwendet, um ER-Debug-Protokolldatensätze auszuwerten, die während der Testausführung erstellt werden.

    ![ERFormatMappingRunLogTable-Arbeitsblatt](media/GER-RSAT-RSAT-ExcelParameters.png "Screenshot des ERFormatMappingRunLogTable-Arbeitsblatts")

## <a name="run-the-tests-and-analyze-the-results"></a>Ausführen des Tests und Analysieren der Ergebnisse

### <a name="run-the-tests-in-rsat"></a>Ausführen der Tests in RSAT

1. Auswählen der geladenen Tests in RSAT
2. Wählen Sie **Ausführen** aus.

Beachten Sie, dass Testfälle in der Anwendung automatisch ausgeführt werden, indem ein Webbrowser verwendet wird.

### <a name="analyze-the-results-of-test-execution"></a>Analysieren der Ergebnisse der Testausführung

Die Ergebnisse der Testausführung werden in RSAT gespeichert. Beachten Sie, dass beide Tests erfolgreich waren.

![Tests, die in RSAT erfolgreich waren](media/GER-RSAT-RSAT-Tests-Passed.png "Screenshot der Tests, die in RSAT erfolgreich waren")

Beachten Sie, dass die Ergebnisse der Testausführung auch an Azure DevOps gesendet werden, damit Sie weitere Analysen ausführen können.

![Ergebnisse der Testausführung in Azure DevOps](media/GER-RSAT-DevOps-Tests-Added.png "Screenshot der Ergebnisse der Testausführung in Azure DevOps")

### <a name="simulate-a-situation-where-tests-fail"></a>Simulieren einer Situation, in der der Test fehlschlägt

Diese Testsuite muss fehlschlagen, wenn mindestens eine der generierten Ausgaben nicht mit dem entsprechenden Ausgangswert übereinstimmt. Um diese Situation zu erreichen, können Sie die abgeleitete Version des Formats **BACS (UK)** verwenden, das eine Zahlungsdatei mit unterschiedlichem Inhalt als der entsprechende Ausgangswert generiert. Um diese Situation zu simulieren, können Sie dasselbe Format **BACS (UK)** verwenden, aber den Zahlungsbetrag auf der Position für verarbeitete Zahlungen ändern.

1. Öffnen Sie die Anwendung, und wechseln Sie zu **Kreditorenkonten \> Zahlungen \> Zahlungserfassung**.
2. Wählen Sie **Positionen** aus.
3. Wählen Sie die Zahlungsposition aus, und wählen Sie dann **Zahlungsstatus \> Kein** aus.
4. Ändern Sie im Feld **Soll** den Wert von **1.000,00** auf **2.000,00**.
5. Wählen Sie **Speichern** aus, um die Änderungen zu speichern.

### <a name="run-the-tests-in-rsat"></a>Ausführen der Tests in RSAT

1. Auswählen der geladenen Tests in RSAT
2. Wählen Sie **Ausführen** aus.

Beachten Sie, dass Testfälle in der Anwendung automatisch ausgeführt werden, indem ein Webbrowser verwendet wird.

### <a name="analyze-the-results-of-test-execution"></a>Analysieren der Ergebnisse der Testausführung

Die Ergebnisse der Testausführung werden in RSAT gespeichert. Beachten Sie, dass der zweite Test bei der zweiten Ausführung fehlschlug.

![Fehlgeschlagene Testergebnisse in RSAT](media/GER-RSAT-RSAT-Tests-Failed.png "Screenshot der fehlgeschlagenen Testergebnisse in RSAT")

Beachten Sie, dass die Ergebnisse der Testausführung auch an Azure DevOps gesendet werden, damit Sie weitere Analysen ausführen können.

![Fehlgeschlagene Testergebnisse in Azure DevOps](media/GER-RSAT-DevOps-Tests-Failed.png "Screenshot der fehlgeschlagenen Testergebnisse in Azure DevOps")

Sie können auf den Status eines Tests zugreifen. Sie können auch auf das Ausführungsprotokoll zugreifen, um die Gründe für einen Fehler zu analysieren. In der folgenden Abbildung zeigt das Ausführungsprotokoll, dass der Fehler aufgetreten aufgrund des Unterschieds im Inhalt zwischen der generierten Zahlungsdatei und dem Ausgangswert aufgetreten ist.

![Ausführungsprotokoll zum Analysieren des Fehlers in Azure DevOps](media/GER-RSAT-DevOps-Tests-Failed-Log.png "Screenshot des Ausführungsprotokolls zum Analysieren des Fehlers in Azure DevOps")

Daher kann die Funktion eines beliebigen ER-Formats, wie Sie gesehen haben, automatisch überprüft werden, indem RSAT als die Testplattform verwendet wird, und indem die auf die Aufgabenaufzeichnung basierenden Testfälle verwendet werden, die die ER-Ausgangswertefunktion verwenden.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Ressourcen für Aufgabenaufzeichnung](../user-interface/task-recorder.md)
- [Regression Suite Automation Tool](https://www.microsoft.com/download/details.aspx?id=57357)
- [Benutzerakzeptanztests erstellen und automatisieren](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md)
- [Bereitstellen und Verwenden von Umgebungen, die fortlaufende und Build- und Testautomatisierung unterstützen](../perf-test/continuous-build-test-automation.md)
- [Nachverfolgung erstellter Berichtsergebnisse und Vergleich mit Ausgangswerten](er-trace-reports-compare-baseline.md)
- [ER – Aktualisieren Sie Ihr Format durch Verwendung einer neuen Basisversion dieses Formats](tasks/er-upgrade-format.md)
- [ER Import einer Konfiguration von Lifecycle Services](tasks/er-import-configuration-lifecycle-services.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]