---
title: Regression Suite Automation Tool-Tutorial
description: Dieses Thema zeigt, wie das Regression Suite Automation Tool (RSAT) verwendet wird. Es beschreibt die verschiedenen Funktionen und enthält Beispiele, die erweiterte Skripterstellung verwenden.
author: robinarh
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: 21761
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: d70b2e7cf497fbf165a452f7977a14a98b9e1956e5a964d42c7bf8a6c3abe0bd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6714548"
---
# <a name="regression-suite-automation-tool-tutorial"></a>Regression Suite Automation Tool-Tutorial

[!include [banner](../../includes/banner.md)]

> [!NOTE]
> Verwenden Sie das Internet-Browsertool, um die Seite in pdf-Format herunterzuladen und zu speichern.

Dies Tutorial führt Sie durch mehrere der erweiterten Funktionen des Regression Suite Automation Tool (RSAT), enthält eine Demozuweisung und beschreibt Strategie und wichtige Lernpunkte.

## <a name="notable-features-of-rsat-and-task-recorder"></a>Bemerkenswerte Funktionen von RSAT und Aufgabenaufzeichnung

### <a name="validate-a-field-value"></a>Einen Feldwert überprüfen

Mit RSAT können Sie Validierungsschritte in Ihren Testfall aufnehmen, um die erwarteten Werte zu validieren. Informationen zu dieser Funktion finden Sie im Artikel [Überprüfen Sie die erwarteten Werte](rsat-validate-expected.md).

Das folgende Beispiel veranschaulicht, wie Sie diese Funktion verwenden können, um zu prüfen, ob der Lagerbestand mehr als 0 (null) ist.

1. In den Demodaten im **USMF**-Unternehmen erstellen Sie eine Aufgabenaufzeichnung, die die folgenden Schritte ausführt:

    1. Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**.
    2. Verwenden Sie den Schnellfilter, um Datensätze zu suchen. Filtern Sie beispielsweise auf einen Wert von **1000** für das Feld **Artikelnummer**.
    3. Wählen Sie **Verfügbarer Lagerbestand** aus
    4. Verwenden Sie den Schnellfilter, um Datensätze zu suchen. Filtern Sie beispielsweise auf einen Wert von **1** für das Feld **Website**.
    5. Markieren Sie in der Liste die ausgewählte Zeile.
    6. Überprüfen Sie, dass der Wert des Feldes **Verfügbare Summe** **411,0000000000000000** ist.

2. Speichern Sie die Aufgabenaufzeichnung als eine **Entwickleraufzeichnung** und hängen Sie sie in Azure DevOps an Ihren Testfall an.
3. Fügen Sie den Testfall dem Testplan hinzu, und laden Sie den Testfall in RSAT.
4. Öffnen Sie die Excel-Parameterdatei und wechseln Sie zum Register **TestCaseSteps**.
5. Um zu überprüfen, ob der verfügbare Bestand immer größer ist als **0**, wechseln Sie zum Schritt **Gesamtverfügbarkeit prüfen** und ändern Sie seinen Wert von **411** zu **0**. Ändern Sie den Wert im Feld **Operator** von einem Gleichheitszeichen (**=**) in ein Größer-als-Zeichen (**\>**).
6. Speichern und schließen Sie die Excel-Parameterdatei.
7. Wählen Sie **Hochladen** aus, um die Änderungen zu speichern, die Sie an der Excel-Parameterdatei vorgenommen haben Azure DevOps.

Wenn der Wert des Feldes **Verfügbare Summe** jetzt für den angegebenen Artikel im Bestand größer als 0 (null) ist, sind Tests unabhängig vom tatsächlichen Wert des verfügbaren Bestands erfolgreich.

### <a name="saved-variables-and-chaining-of-test-cases"></a>Gespeicherte Variablen und Verkettung von Testfällen

Eine wichtige zentrale Funktion von RSAT ist das Verketten von Testfällen, das heißt, die Fähigkeit eines Tests, Variablen an andere Tests zu übergebe. Weitere Informationen finden Sie im Artikel [Kopieren Sie Variablen in Kettentestfälle](rsat-chain-test-cases.md).

### <a name="derived-test-case"></a>Abgeleitete Testfälle

Mit RSAT können Sie dieselbe Aufgabenaufzeichnung mit mehreren Testfällen verwenden, sodass eine Aufgabe mit unterschiedlichen Datenkonfigurationen ausgeführt werden kann. Siehe Artikel [Abgeleitete Testfälle](rsat-derived-test-cases.md) für mehr Informationen.

### <a name="validate-notifications-and-messages"></a>Überprüfen Sie Benachrichtigungen und Nachrichten

Diese Funktion kann verwendet werden, um zu überprüfen, ob eine Aktivität stattfand. Wenn ein Produktionsauftrag beispielsweise erstellt, vorkalkuliert und dann gestartet wird, zeigt die App eine „Produktion – Start“-Nachricht, die Sie darüber zu informieren, dass der Produktionsauftrag gestartet wurde.

![Produktion – Start-Benachrichtigung.](./media/use_rsa_tool_05.png)

Sie können diese Meldung über RSAT überprüfen, indem Sie den Nachrichtentext auf der Registerkarte **MessageValidation** der Excel-Parameterdatei für die entsprechende Erfassung eingeben.

![Registerkarte „Nachrichtenvalidierung“.](./media/use_rsa_tool_06.png)

Nachdem der Testfall ausgeführt wurde, wird die Nachricht in der Excel-Parameterdatei mit der Nachricht verglichen, die angezeigt wird. Wenn die Nachrichten nicht übereinstimmen, schlägt der Testfall fehl.

> [!NOTE]
> Sie können mehrere Nachrichten auf der Registerkarte **MessageValidation** in der Excel-Parameterdatei eingeben. Die Nachrichten können auch Fehler- oder Warnmeldungen anstelle der Informationsmeldungen sein.

### <a name="snapshot"></a>Momentaufnahme

Diese Funktion nimmt Screenshots der Schritte auf, die während der Aufgabenaufzeichnung ausgeführt wurden. Es ist nützlich für Prüf- oder Debugging-Zwecke.

- Um diese Funktion zu verwenden, öffnen Sie die Datei **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** im RSAT-Installationsordner (beispielsweise **C:\\Programme (x86)\\Regression Suite Automation Tool**), und ändern Sie den Wert des folgenden Elements von **false** auf **true**.

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

Wenn Sie den Testfall ausführen, generiert RSAT Snapshots (Bilder) der Schritte im Wiedergabeordner der Testfälle im Arbeitsverzeichnis. Wenn Sie eine ältere Version von RSAT verwenden, werden die Bilder in **C\\Benutzer\\\<Username\>\\AppData\\Roaming\\regressionTool\\Playback** gespeichert und für jeden Testfall, der ausgeführt wird, wird ein separater Ordner erstellt.

## <a name="assignment"></a>Zuweisung

### <a name="scenario"></a>Szenario

1. Der Produktdesigner erstellt ein neues veröffentlichtes Produkt.
2. Der Produktions-Manager initiiert einen Produktionsauftrag, um den Lagerbestand auf zwei Stück aufzufüllen.
3. Die Fertigung startet und beendet den Produktionsauftrag und überprüft, ob die verfügbare Menge zwei Stück beträgt.
4. Das Vertriebsteam erhält einen Auftrag für vier Stück des neuen Produkts. Daher aktualisiert das Vertriebsteam den Nettobedarf anhand des dynamischen Plans. Da keine Mehrkapazität verfügbar ist, wird die Standardauftragsrichtlinie aus „kaufen statt herstellen“ festgelegt. Daher wird eine geplante Einkaufsbestellung erstellt.
5. Der Käufer fügt einen Lieferanten hinzu, wandelt die geplante Einkaufsbestellung um und bestätigt die Bestellung anschließend.
6. Nachdem die gekauften Waren in Laden eingehen, sucht der Ladeninhaber die zugehörige Bestellung erhält die Waren. Da die Bestellung nun abgeschlossen ist, können Waren für den Auftrag entnommen und verpackt werden.
7. Finance bucht die Einkaufsrechnung und die Verkaufsrechnung.

Die folgende Abbildung zeigt den Ablauf für dieses Szenario.

![Ablauf für das Demoszenario.](./media/use_rsa_tool_14.png)

Die folgende Abbildung zeigt die Geschäftsprozesshierarchie für dieses Szenario im LCS Business Process Modeler.

![Geschäftsprozesse für das Demoszenario.](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a>Strategie – Wichtige Lernpunkte

### <a name="data"></a>Daten

- Stellen Sie sicher, dass Sie repräsentative Datenmengen haben (eine Kopie der Produktion bzw. der goldenen Konfigurationsdaten und migrierte Daten).
- Wenn Sie neue Daten über die Aufgabenaufzeichnung generieren, erstellen Sie Testnamen, die nicht mit vorhandenen Namen kollidieren, (verwenden Sie beispielsweise das Präfix **RSATxxx**).
- Verwenden Sie Point-In-Time-Wiederherstellung von Azure, um Tests in der nicht-Ebene-1-Umgebung zu wiederholen.
- Zwar können Sie die Excel-Funktionen **ZUFÄLLIG** und **JETZT** verwenden, um eine eindeutige Kombination zu generieren, der Aufwand ist ausgesprochen hoch. Hier ist ein Beispiel.

    ```Excel
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a>Aufgabenaufzeichnung

- Definieren Sie Szenarien, bevor Sie mit der Aufzeichnung beginnen. Ein in gut verwaltetes Projekt hat vordefinierte Testszenarien. Um einen Testfall zu erstellen, berücksichtigen Sie, wie vorhersagbar das Ergebnis dieser Testszenarien ist.
- Teilen Sie Aufzeichnungen, wenn Sie durch verschiedene Rollen ausgeführt werden oder wenn es Wartezeit gibt oder ein externes Ereignis vor dem nächsten Schritt ausgeführt wird.
- Vermeiden Sie es, Werte in Listen auszuwählen. Verwenden Sie stattdessen Textformate, wie **FIFO**, **AudioRM** und **SiteWH**. Wenn Sie in einer Liste auswählen, wird die Position des Werts in der Liste aufgenommen, nicht der Wert selbst. Wenn dieser Liste Artikel hinzugefügt werden, kann sich die Position des Werts ändern. Daher verwendet Ihre Aufzeichnung einen anderen Parameter, und der Rest des Szenarios wird möglicherweise davon beeinflusst.
- Denken Sie an ein Verhalten bei mehreren Benutzern. Nehmen Sie beispielsweise nicht an, dass Ihr neu erstellter Auftrag automatisch immer aktiviert ist. Verwenden Sie stattdessen immer den Filter, um die korrekte Reihenfolge zu suchen.
- Verwenden Sie die Kopierfunktion in der Aufgabenaufzeichnung, um den Namen eines neu erstellten Produkts zu speichern, damit sie in verketteten Testfällen verwendet werden kann.
- Verwenden Sie die Validierungsfunktion in der Aufgabenaufzeichnung, um Prüfpunkte festzulegen, die sicherstellen, dass Schritte ordnungsgemäß ausgeführt wurden.

### <a name="rsat"></a>RSAT

- Um den Test in einem anderen Unternehmen auszuführen, können Sie das Unternehmen auf der Registerkarte **Allgemein** der Excel-Parameterdatei ändern. Stellen Sie sicher, dass die Einstellungen und Daten im derzeit ausgewählten Unternehmen verfügbar sind.
- Sie können den Testbenutzer auf der Registerkarte **Allgemein** der Excel-Parameterdatei ändern. Geben Sie die E-Mail-Kennung des Benutzers ein, der den Testfall ausführt. Auf diese Weise kann der Testfall durchgeführt werden, indem die Sicherheitsberechtigungen des angegebenen Benutzers verwendet werden.
- Um zu warten, bis der Test begonnen wird, können Sie auf der Registerkarte **Allgemein** der Excel-Parameterdatei eine Pause definieren. Diese Pause kann in einem Batchauftrag verwendet werden (beispielsweise, wenn ein Workflow ausgeführt werden muss, bevor der nächste Schritt ausgeführt werden kann).

## <a name="advanced-scripting"></a>Erweiterte Skripterstellung

### <a name="cli"></a>CLI

RSAT kann von einem Fenster **Befehlseingabeaufforderung** oder **PowerShell** aufgerufen werden.

> [!NOTE]
> Überprüfen Sie, dass die Umgebungsvariable **TestRoot** auf den RSAT-Installationspfad festgelegt ist. (Öffnen Sie Microsoft Windows in der **Systemsteuerung**, wählen Sie **System und Sicherheit \> System \> Erweiterte Systemeinstellungen** und **Umgebungsvariablen** aus.)

1. Öffnen Sie als Administrator ein Fenster **Kommandozeile** oder **PowerShell**.
2. Navigieren Sie zum RSAT-Installationsverzeichnis.

    ```Console
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. Alle Befehle auflisten.

    ```Console
    C:\Program Files (x86)\Regression Suite Automation Tool>Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe help

    Usage:
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe command
        or
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe /settings "C:\Path to\file.settings" command

    Available commands:
        ?
        about
        cls
        download
        edit
        generate
        generatederived
        generatetestonly
        generatetestsuite
        help
        list
        listtestplans
        listtestsuite
        listtestsuitenames
        playback
        playbackbyid
        playbackmany
        playbacksuite
        quit
        upload
        uploadrecording
        usage
    ```

#### <a name=""></a>?

Zeigt die Hilfe zu allen verfügbaren Befehlen und ihren Parametern an.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="-optional-parameters"></a>?: Optionale Parameter

`command`: Hierbei ist ``[command]`` einer der unten angegebenen Befehle.

#### <a name="about"></a>Info

Zeigt die aktuelle Version an.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a>cls

Löscht den Bildschirm.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**

#### <a name="download"></a>herunterladen

Lädt Anhänge für den angegebenen Testfall in das Ausgabeverzeichnis herunter.
Sie können den Befehl ``list`` verwenden, um alle verfügbaren Testfälle zu erhalten. Verwenden Sie einen beliebigen Wert aus der ersten Spalte als Parameter **test_case_id**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[test_case_id] [output_dir]``

##### <a name="download-required-parameters"></a>download: erforderliche Parameter

+ `test_case_id`: Steht für die Kennung des Testfalls.
+ `output_dir`: Steht für das Ausgabeverzeichnis. Das Verzeichnis muss vorhanden sein.

##### <a name="download-examples"></a>download: Beispiele

`download 123 c:\temp\rsat`

`download 765 c:\rsat\last`

#### <a name="edit"></a>Bearbeiten

Erlaubt Ihnen, die Parameterdatei im Programm Excel zu öffnen und zu bearbeiten.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="edit-required-parameters"></a>edit: erforderliche Parameter

+ `excel_file`: Muss einen vollständigen Pfad zu einer vorhandenen Excel-Datei enthalten.

##### <a name="edit-examples"></a>edit: Beispiele

`edit c:\RSAT\TestCase_123_Base.xlsx`

`edit e:\temp\TestCase_456_Base.xlsx`

#### <a name="generate"></a>erzeugen.

Erzeugt im Ausgabeverzeichnis Testausführungs- und Parameterdateien für den angegebenen Testfall. Sie können den Befehl ``list`` verwenden, um alle verfügbaren Testfälle zu erhalten. Verwenden Sie einen beliebigen Wert aus der ersten Spalte als Parameter **test_case_id**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[test_case_id] [output_dir]``

##### <a name="generate-required-parameters"></a>generate: erforderliche Parameter

+ `test_case_id`: Steht für die Kennung des Testfalls.
+ `output_dir`: Steht für das Ausgabeverzeichnis. Das Verzeichnis muss vorhanden sein.

##### <a name="generate-examples"></a>generate: Beispiele

`generate 123 c:\temp\rsat`

`generate 765 c:\rsat\last`

#### <a name="generatederived"></a>erzeugt

Erzeugt einen neuen Testfall, der aus dem bereitgestellten Testfall abgeleitet wird. Sie können den Befehl ``list`` verwenden, um alle verfügbaren Testfälle zu erhalten. Verwenden Sie einen beliebigen Wert aus der ersten Spalte als Parameter **test_case_id**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="generatederived-required-parameters"></a>generatederived: erforderliche Parameter

+ `parent_test_case_id`: Steht für die Kennung des übergeordneten Testfalls.
+ `test_plan_id`: Steht für die Kennung des Testplans.
+ `test_suite_id` Steht für die Kennung der Testsuite.

##### <a name="generatederived-examples"></a>generatederived: Beispiele

`generatederived 123 8901 678`

#### <a name="generatetestonly"></a>generatetestonly

Erzeugt nur die Testausführungsdatei für den angegebenen Testfall im Ausgabeverzeichnis. Sie können den Befehl ``list`` verwenden, um alle verfügbaren Testfälle zu erhalten. Verwenden Sie einen beliebigen Wert aus der ersten Spalte als Parameter **test_case_id**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[test_case_id] [output_dir]``

##### <a name="generatetestonly-required-parameters"></a>generatetestonly: erforderliche Parameter

+ `test_case_id`: Steht für die Kennung des Testfalls.
+ `output_dir`: Steht für das Ausgabeverzeichnis. Das Verzeichnis muss vorhanden sein.

##### <a name="generatetestonly-examples"></a>generatetestonly: Beispiele

`generatetestonly 123 c:\temp\rsat`

`generatetestonly 765 c:\rsat\last`

#### <a name="generatetestsuite"></a>generatetestsuite

Erzeugt alle Testfälle für die angegebene Suite im Ausgabeverzeichnis. Sie können den Befehl ``listtestsuitenames`` verwenden, um alle verfügbaren Testanzüge zu erhalten. Verwenden Sie einen beliebigen Wert aus der Spalte als **Test_suite_name** Parameter.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[test_suite_name] [output_dir]``

##### <a name="generatetestsuite-required-parameters"></a>generatetestsuite: erforderliche Parameter

+ `test_suite_name` Steht für den Namen der Testsuite.
+ `output_dir`: Steht für das Ausgabeverzeichnis. Das Verzeichnis muss vorhanden sein.

##### <a name="generatetestsuite-examples"></a>generatetestsuite: Beispiele

`generatetestsuite Tests c:\temp\rsat`

`generatetestsuite Purchase c:\rsat\last`

#### <a name="help"></a>help

Identisch mit dem [?](#section) Befehl.

#### <a name="list"></a>Liste

Listet alle verfügbaren Testfälle auf.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**

#### <a name="listtestplans"></a>listtestplans

Listet alle verfügbaren Testpläne auf.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**

#### <a name="listtestsuite"></a>listtestsuite

Listet Testfälle für die angegebene Testsuite auf. Sie können den Befehl ``listtestsuitenames`` verwenden, um alle verfügbaren Testsuiten zu erhalten. Verwenden Sie einen beliebigen Wert aus der ersten Spalte als **Suitename** Parameter.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[suite_name]``

##### <a name="listtestsuite-required-parameters"></a>listtestsuite: erforderliche Parameter

+ `suite_name`: Der Name der gewünschten Testsuite.

##### <a name="listtestsuite-examples"></a>listtestsuite: Beispiele

`listtestsuite "sample suite name"`

`listtestsuite NameOfTheSuite`

#### <a name="listtestsuitenames"></a>listtestsuitenames

Listet alle verfügbaren Testsuiten auf.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**

#### <a name="playback"></a>playback

Spielt einen Testfall mit Hilfe einer Excel-Datei ab.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[excel_file]``

##### <a name="playback-required-parameters"></a>playback: erforderliche Parameter

+ `excel_file`: Ein vollständiger Pfad zur Excel-Datei. Die Datei muss vorhanden sein.

##### <a name="playback-examples"></a>playback: Beispiele

`playback c:\RSAT\TestCaseParameters\sample1.xlsx`

`playback e:\temp\test.xlsx`

#### <a name="playbackbyid"></a>playbackbyid

Spielt mehrere Testfälle gleichzeitig ab. Sie können den Befehl ``list`` verwenden, um alle verfügbaren Testfälle zu erhalten. Verwenden Sie einen beliebigen Wert aus der ersten Spalte als Parameter **test_case_id**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="playbackbyid-required-parameters"></a>playbackbyid: erforderliche Parameter

+ `test_case_id1`: Die Kennung des vorhandenen Testfalls.
+ `test_case_id2`: Die Kennung des vorhandenen Testfalls.
+ `test_case_idN`: Die Kennung des vorhandenen Testfalls.

##### <a name="playbackbyid-examples"></a>playbackbyid: Beispiele

`playbackbyid 878`

`playbackbyid 2345 667 135`

#### <a name="playbackmany"></a>playbackmany

Spielt viele Testfälle auf einmal ab, wobei Excel-Dateien verwendet werden.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[excel_file1] [excel_file2] ... [excel_fileN]``

##### <a name="playbackmany-required-parameters"></a>playbackmany: erforderliche Parameter

+ `excel_file1`: Vollständiger Pfad zur Excel-Datei. Die Datei muss vorhanden sein.
+ `excel_file2`: Vollständiger Pfad zur Excel-Datei. Die Datei muss vorhanden sein.
+ `excel_fileN`: Vollständiger Pfad zur Excel-Datei. Die Datei muss vorhanden sein.

##### <a name="playbackmany-examples"></a>playbackmany: Beispiele

`playbackmany c:\RSAT\TestCaseParameters\param1.xlsx`

`playbackmany e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx`

#### <a name="playbacksuite"></a>playbacksuite

Spielt alle Testfälle aus der angegebenen Testsuite ab.
Sie können den Befehl ``listtestsuitenames`` verwenden, um alle verfügbaren Testsuiten zu erhalten. Verwenden Sie einen beliebigen Wert aus der ersten Spalte als **Suitename** Parameter.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[suite_name]``

##### <a name="playbacksuite-required-parameters"></a>playbacksuite: erforderliche Parameter

+ `suite_name`: Der Name der gewünschten Testsuite.

##### <a name="playbacksuite-examples"></a>playbacksuite: Beispiele

`playbacksuite suiteName`

`playbacksuite sample_suite`

#### <a name="quit"></a>quit

Schließt die Anwendung.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**

#### <a name="upload"></a>upload

Lädt alle Dateien hoch, die zu der angegebenen Testsuite oder den angegebenen Testfällen gehören.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``[suite_name] [testcase_id]``

#### <a name="upload-required-parameters"></a>upload: erforderliche Parameter

+ `suite_name`: Alle Dateien, die zu der angegebenen Testsuite gehören, werden hochgeladen.
+ `testcase_id`: Alle Dateien, die zu den angegebenen Testfällen gehören, werden hochgeladen.

##### <a name="upload-examples"></a>upload: Beispiele

`upload sample_suite`

`upload 123`

`upload 123 456`

#### <a name="uploadrecording"></a>uploadrecording

Lädt nur die Aufzeichnungsdatei hoch, die zu den angegebenen Testfällen gehört.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[testcase_id]``

##### <a name="uploadrecording-required-parameters"></a>uploadrecording: erforderliche Parameter

+ `testcase_id`: Die Aufzeichnungsdatei, die zu den angegebenen Testfällen gehört, wird hochgeladen.

##### <a name="uploadrecording-examples"></a>uploadrecording: Beispiele

`uploadrecording 123`

`uploadrecording 123 456`

#### <a name="usage"></a>Verwendung

Zeigt zwei Möglichkeiten, diese Anwendung aufzurufen: eine mit einer Standardeinstellungsdatei, eine andere mit einer Einstellungsdatei.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**

### <a name="windows-powershell-examples"></a>Windows PowerShell-Beispiele

#### <a name="run-a-test-case-in-a-loop"></a>Ausführen eines Testfalls in einer Schleife

Sie haben ein Testskript, das einen neuen Debitor erstellt. Über Skripterstellung kann dieser Testfall in einer Schleife ausgeführt werden, indem Sie die folgenden Daten zufällig generieren, bevor jede Iteration ausgeführt wird:

- Debitorkennung
- Name des Debitors
- Adresse des Debitors

Die Debitorenkennung hat das Format *ATCUS\<number\>*, wobei \<number\> ein Wert zwischen **000000001** und **999999999** ist.

Das folgende Beispiel verwendet den Parameter **Start**, um die erste Nummer zu definieren, die verwendet wird. Es wird ein zweiter Parameter **nr** verwendet, um die Anzahl der Debitoren zu definieren, die erstellt werden müssen. Für jede Iteration werden die Parameter in der Excel-Parameterdatei geändert, indem eine UpdateCustomer-Funktion verwendet wird. Danach wird die RSAT-Befehlszeile in einer RunTestCase-Funktion aufgerufen.

Öffnet Sie die Microsoft Windows integrierte Skiptumgebung (ISE) von PowerShell im Administratormodus, und fügen Sie den folgenden Code im Fenster mit dem Namen **Untitled1.ps1** ein.

```powershell
param ( [int]$start = 1, [int]$nr = 1 )
function UpdateCustomer
{
    param ([string]$paramFilename, [string]$sheetName, [string]$CustId)
    $xl = New-Object -COM "Excel.Application"
    $xl.Visible = $false
    $wb = $xl.Workbooks.Open($paramFilename)
    $ws = $wb.Sheets.Item($sheetName)
    $ws.Cells.Item(3, 2).Value = "ATCUS" + $CustId
    $ws.Cells.Item(4, 2).Value = "Automated Test Customer " + $CustId
    $ws.Cells.Item(8, 2).Value = "Automated Test Street " + $CustId
    $wb.Save()
    $wb.Close()
    $xl.Quit()
    [System.Runtime.Interopservices.Marshal]::ReleaseComObject($xl)
}
function RunTestCase
{
    param ( [string]$filename )
    $cmd = "cd c:\Program Files (x86)\Regression Suite Automation Tool\ &&  "
    $cmd = $cmd + "Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe playback "
    $cmd = $cmd + $filename
    cmd /c $cmd
}
$excelFilename = "full path to Excel parameter file"
l$sheetName = "DirPartyQuickCreateForm"
for ($i = $start; $i -lt $start + $nr; $i++ )
{
    $CustomerId = $i.ToString("000000000")
    Write-Host "customer : " $CustomerId
    UpdateCustomer $excelFilename $sheetName $CustomerId
    RunTestCase $excelFilename
```

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a>Führen Sie ein Skript aus, das von den Daten in Microsoft Dynamics 365 abhängt

Das folgende Beispiel verwendet einen Aufruf des Open Data Protocol (OData), um den Status einer Bestellung zu suchen. Wenn der Status nicht **fakturiert** ist, können Sie beispielsweise einen RSAT-Testfall anrufen, der die Rechnung bucht.

```xpp
function Odata_Get
{
    Param ( [string] $environment, [string] $cmd )
    [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12
    $tenant = "your tenant"
    $creds = @{
        grant_type = "client_credentials"
        client_id = "your client application Id"
        client_secret = "your client secret"
        resource = $environment
    }
    $headers = $null
    $bearer = Invoke-RestMethod https://login.microsoftonline.com/$tenant/oauth2/token -Method Post -Body $creds -Headers $headers;
    $headers = @{
        Authorization = "Bearer " + $bearer.access_token
    }
    $Odata_cmd = $environment + '/data/' + $cmd
    return (Invoke-RestMethod -Uri $Odata_cmd -Method Get -Headers $headers -ContentType application/json )
}
function PurchaseOrderStatus
{
    Param ( [string] $environment, [string] $purchaseOrderNumber )
    $cmd = 'PurchaseOrderHeaders?$filter=PurchaseOrderNumber eq '
    $cmd = $cmd + "'" + $purchaseOrderNumber + "'"
    $response = Odata_Get -environment $environment -cmd $cmd
    return $response.value.PurchaseOrderStatus
}
$environment = "https://your environment"
$orderStatus = PurchaseOrderStatus -environment $environment -purchaseOrderNumber '000003'
if ($orderStatus -eq $null) {   write-host 'doesn''t exist'}
elseif ($orderStatus -ne 'invoiced') { RunTestCase "PostInvoice" }
```


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]