---
title: Regression Suite Automation Tool-Tutorial
description: Dieses Thema zeigt, wie das Regression Suite Automation Tool (RSAT) verwendet wird. Es beschreibt die verschiedenen Funktionen und enthält Beispiele, die erweiterte Skripterstellung verwenden.
author: FrankDahl
ms.date: 09/23/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: tfehr
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: e2273aefb98880a1ae746ef7ec65b4f2262f3560
ms.sourcegitcommit: 49c97b0c94e916db5efca5672d85df70c3450755
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/29/2022
ms.locfileid: "8492919"
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

2. Speichern Sie den Datensatz der Aufgabe als **Entwickleraufzeichnung** und hängen Sie ihn an Ihren Testfall in Azure DevOps an.
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

- Um diese Funktion beim Ausführen des RSAT mit der Benutzeroberfläche zu verwenden, öffnen Sie die Datei **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** im RSAT-Installationsordner (beispielsweise **C:\\Programme (x86)\\Regression Suite Automation Tool**), und ändern Sie den Wert des folgenden Elements von **false** in **true**.

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

- Um diese Funktion beim Ausführen des RSAT durch die CLI (z. B. Azure DevOps) zu verwenden, öffnen Sie die Datei **Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe.config** im RSAT-Installationsordner (z. B. **C:\\Program Files (x86)\\Regression Suite Automation Tool**), und ändern Sie den Wert des folgenden Elements von **false** in **true**.

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

Wenn Sie Testfälle ausführen, erstellt RSAT Momentaufnahmen (Bilder) der Schritte und speichert sie im Wiedergabeordner der Testfälle im Arbeitsverzeichnis. Im Wiedergabeordner wird ein separater Unterordner mit dem Namen **SchrittSchnappschüsse** erstellt. Dieser Ordner enthält Snapshots für die ausgeführten Testfälle.

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
        downloadsuite
        edit
        generate
        generatederived
        generatetestonly
        generatetestsuite
        help
        list
        listtestplans
        listtestsuite
        listtestsuitebyid
        listtestsuitenames
        playback
        playbackbyid
        playbackmany
        playbacksuite
        playbacksuitebyid
        quit
        upload
        uploadrecording
        usage
    ```

#### <a name=""></a>?

Listet alle Befehle auf oder zeigt die Hilfe für einen bestimmten Befehl zusammen mit den verfügbaren Parametern an.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="-optional-parameters"></a>?: Optionale Parameter

`command`: Wobei ``[command]`` einer der Befehle aus der vorangegangenen Liste ist.

#### <a name="about"></a>Info

Zeigt die Version des installierten RSAT an.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a>cls

Löscht den Bildschirm.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**

#### <a name="download"></a>herunterladen

Lädt Anhänge (Aufzeichnungs-, Ausführungs- und Parameterdateien) für den angegebenen Testfall von Azure DevOps in das Ausgabeverzeichnis. Mit dem Befehl ``list`` können Sie alle verfügbaren Testfälle abrufen und einen beliebigen Wert aus der ersten Spalte als **test_case_id** Parameter verwenden.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[/retry[=<seconds>]] [test_case_id] [output_dir]``

##### <a name="download-optional-switches"></a>download: optionale Schalter

+ `/retry[=seconds]`: Wenn dieser Schalter angegeben ist und die Testfälle durch andere RSAT-Instanzen blockiert werden, wartet der Download-Prozess die angegebene Anzahl von Sekunden und versucht es dann noch einmal. Der Standardwert für \[Sekunden\] ist 120 Sekunden. Ohne diesen Schalter wird der Prozess sofort abgebrochen, wenn Testfälle blockiert sind.

##### <a name="download-required-parameters"></a>download: erforderliche Parameter

+ `test_case_id`: Steht für die Kennung des Testfalls.

##### <a name="download-optional-parameters"></a>download: optionale Parameter

+ `output_dir`: Stellt das Arbeitsverzeichnis der Ausgabe dar. Das Verzeichnis muss vorhanden sein. Wenn dieser Parameter nicht festgelegt ist, wird das Arbeitsverzeichnis aus den Einstellungen verwendet.

##### <a name="download-examples"></a>download: Beispiele

`download 123 c:\temp\rsat`

`download /retry=240 765`

#### <a name="downloadsuite"></a>downloadsuite

Lädt Anhänge (Aufzeichnungs-, Ausführungs- und Parameterdateien) für alle Testfälle der angegebenen Testsuite von Azure DevOps in das Ausgabeverzeichnis herunter. Mit dem Befehl ``listtestsuitenames`` können Sie alle verfügbaren Testsuiten abrufen und einen beliebigen Wert als **Testsuite_Name** Parameter verwenden.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``downloadsuite``**``[/retry[=<seconds>]] ([test_suite_name] | [/byid] [test_suite_id]) [output_dir]``

##### <a name="downloadsuite-optional-switches"></a>downloadsuite: optionale Schalter

+ `/retry[=seconds]`: Wenn dieser Schalter angegeben ist und die Testfälle durch andere RSAT-Instanzen blockiert werden, wartet der Download-Prozess die angegebene Anzahl von Sekunden und versucht es dann noch einmal. Der Standardwert für \[Sekunden\] ist 120 Sekunden. Ohne diesen Schalter wird der Prozess sofort abgebrochen, wenn Testfälle blockiert sind.
+ `/byid`: Dieser Schalter zeigt an, dass die gewünschte Testsuite durch ihre Azure DevOps ID identifiziert wird, anstatt durch den Namen der Testsuite.

##### <a name="downloadsuite-required-parameters"></a>downloadsuite: erforderliche Parameter

+ `test_suite_name` Steht für den Namen der Testsuite. Dieser Parameter ist erforderlich, wenn der Schalter /byid **nicht** angegeben ist. Dieser Name ist der Name der Testsuite Azure DevOps.
+ `test_suite_id` Steht für die Kennung der Testsuite. Dieser Parameter ist erforderlich, wenn der Schalter /byid **angegeben ist**. Diese ID ist die ID der Testsuite Azure DevOps.

##### <a name="downloadsuite-optional-parameters"></a>downloadsuite: optionale Parameter

+ `output_dir`: Stellt das Arbeitsverzeichnis der Ausgabe dar. Das Verzeichnis muss vorhanden sein. Wenn dieser Parameter nicht festgelegt ist, wird das Arbeitsverzeichnis aus den Einstellungen verwendet.

##### <a name="downloadsuite-examples"></a>downloadsuite: Beispiele

`downloadsuite NameOfTheSuite c:\temp\rsat`

`downloadsuite /byid 123 c:\temp\rsat`

`downloadsuite /retry=240 /byid 765`

`downloadsuite /retry=240 /byid 765 c:\temp\rsat`

#### <a name="edit"></a>Bearbeiten

Erlaubt Ihnen, die Parameterdatei im Programm Excel zu öffnen und zu bearbeiten.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="edit-required-parameters"></a>edit: erforderliche Parameter

+ `excel_file`: Muss einen vollständigen Pfad zu einer vorhandenen Excel-Datei enthalten.

##### <a name="edit-examples"></a>edit: Beispiele

`edit c:\RSAT\123\TestCase_123_Base.xlsx`

`edit e:\temp\TestCase_456_Base.xlsx`

#### <a name="generate"></a>erzeugen.

Erzeugt im Ausgabeverzeichnis Testausführungs- und Parameterdateien für den angegebenen Testfall. Sie können den Befehl ``list`` verwenden, um alle verfügbaren Testfälle zu erhalten. Verwenden Sie einen beliebigen Wert aus der ersten Spalte als Parameter **test_case_id**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[/retry[=<seconds>]] [/dllonly] [/keepcustomexcel] [test_case_id] [output_dir]``

##### <a name="generate-optional-switches"></a>generate: optionale Schalter

+ `/retry[=seconds]`: Wenn dieser Schalter angegeben ist und Falltestfälle durch andere RSAT-Instanzen blockiert werden, wartet der Generierungsprozess die angegebene Anzahl von Sekunden und versucht es dann noch einmal. Der Standardwert für \[Sekunden\] ist 120 Sekunden. Ohne diesen Schalter wird der Prozess sofort abgebrochen, wenn Testfälle blockiert sind.
+ `/dllonly`: Nur Testausführungsdateien generieren. Regenerieren Sie die Excel-Parameterdatei nicht.
+ `/keepcustomexcel`: Aktualisieren Sie die vorhandene Parameterdatei. Regenerieren Sie auch Ausführungsdateien.

##### <a name="generate-required-parameters"></a>generate: erforderliche Parameter

+ `test_case_id`: Steht für die Kennung des Testfalls.

##### <a name="generate-optional-parameters"></a>generate: optionale Parameter

+ `output_dir`: Stellt das Arbeitsverzeichnis der Ausgabe dar. Das Verzeichnis muss vorhanden sein. Wenn dieser Parameter nicht festgelegt ist, wird das Arbeitsverzeichnis aus den Einstellungen verwendet.

##### <a name="generate-examples"></a>generate: Beispiele

`generate 123 c:\temp\rsat`

`generate /retry=240 765 c:\rsat\last`

`generate /retry=240 /dllonly 765`

`generate /retry=240 /keepcustomexcel 765`

#### <a name="generatederived"></a>erzeugt

Erzeugt einen neuen abgeleiteten Testfall (untergeordneter Testfall) für den angegebenen Testfall. Der neue Testfall wird auch der angegebenen Testsuite hinzugefügt. Mit dem Befehl ``list`` können Sie alle verfügbaren Testfälle abrufen und einen beliebigen Wert aus der ersten Spalte als **test_case_id** Parameter verwenden.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[/retry[=<seconds>]] [parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="generatederived-optional-switches"></a>generatederived: optionale Schalter

+ `/retry[=seconds]`: Wenn dieser Schalter angegeben ist und Falltestfälle durch andere RSAT-Instanzen blockiert werden, wartet der Generierungsprozess die angegebene Anzahl von Sekunden und versucht es dann noch einmal. Der Standardwert für \[Sekunden\] ist 120 Sekunden. Ohne diesen Schalter wird der Prozess sofort abgebrochen, wenn Testfälle blockiert sind.

##### <a name="generatederived-required-parameters"></a>generatederived: erforderliche Parameter

+ `parent_test_case_id`: Steht für die Kennung des übergeordneten Testfalls.
+ `test_plan_id`: Steht für die Kennung des Testplans.
+ `test_suite_id` Steht für die Kennung der Testsuite.

##### <a name="generatederived-examples"></a>generatederived: Beispiele

`generatederived 123 8901 678`

`generatederived /retry 123 8901 678`

#### <a name="generatetestonly"></a>generatetestonly

Erzeugt nur Testausführungsdateien für den angegebenen Testfall. Die Excel-Parameterdatei wird nicht generiert. Die Dateien werden in dem angegebenen Ausgabeverzeichnis erstellt. Mit dem Befehl ``list`` können Sie alle verfügbaren Testfälle abrufen und einen beliebigen Wert aus der ersten Spalte als **test_case_id** Parameter verwenden.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[/retry[=<seconds>]] [test_case_id] [output_dir]``

##### <a name="generatetestonly-optional-switches"></a>generatetestonly: optionale Schalter

+ `/retry[=seconds]`: Wenn dieser Schalter angegeben ist und Falltestfälle durch andere RSAT-Instanzen blockiert werden, wartet der Generierungsprozess die angegebene Anzahl von Sekunden und versucht es dann noch einmal. Der Standardwert für \[Sekunden\] ist 120 Sekunden. Ohne diesen Schalter wird der Prozess sofort abgebrochen, wenn Testfälle blockiert sind.

##### <a name="generatetestonly-required-parameters"></a>generatetestonly: erforderliche Parameter

+ `test_case_id`: Steht für die Kennung des Testfalls.

##### <a name="generatetestonly-optional-parameters"></a>generatetestonly: optionale Parameter

+ `output_dir`: Stellt das Arbeitsverzeichnis der Ausgabe dar. Das Verzeichnis muss vorhanden sein. Wenn dieser Parameter nicht festgelegt ist, wird das Arbeitsverzeichnis aus den Einstellungen verwendet.

##### <a name="generatetestonly-examples"></a>generatetestonly: Beispiele

`generatetestonly 123 c:\temp\rsat`

`generatetestonly /retry=240 765`

#### <a name="generatetestsuite"></a>generatetestsuite

Generiert Testautomatisierungsdateien für alle Testfälle in der angegebenen Testsuite. Mit dem Befehl ``listtestsuitenames`` können Sie alle verfügbaren Testsuiten abrufen und einen beliebigen Wert als **Testsuite_Name** Parameter verwenden.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[/retry[=<seconds>]] [/dllonly] [/keepcustomexcel] ([test_suite_name] | [/byid] [test_suite_id]) [output_dir]``

##### <a name="generatetestsuite-optional-switches"></a>generatetestsuite: optionale Schalter

+ `/retry[=seconds]`: Wenn dieser Schalter angegeben ist und Falltestfälle durch andere RSAT-Instanzen blockiert werden, wartet der Generierungsprozess die angegebene Anzahl von Sekunden und versucht es dann noch einmal. Der Standardwert für \[Sekunden\] ist 120 Sekunden. Ohne diesen Schalter wird der Prozess sofort abgebrochen, wenn Testfälle blockiert sind.
+ `/dllonly`: Nur Testausführungsdateien generieren. Regenerieren Sie die Excel-Parameterdatei nicht.
+ `/keepcustomexcel`: Vorhandene Parameterdatei aktualisieren. Regenerieren Sie auch Ausführungsdateien.
+ `/byid`: Dieser Schalter zeigt an, dass die gewünschte Testsuite durch ihre Azure DevOps ID identifiziert wird, anstatt durch den Namen der Testsuite.

##### <a name="generatetestsuite-required-parameters"></a>generatetestsuite: erforderliche Parameter

+ `test_suite_name` Steht für den Namen der Testsuite. Dieser Parameter ist erforderlich, wenn der Schalter /byid **nicht** angegeben ist. Dieser Name ist der Name der Testsuite Azure DevOps.
+ `test_suite_id` Steht für die Kennung der Testsuite. Dieser Parameter ist erforderlich, wenn der Schalter /byid **angegeben ist**. Diese ID ist die ID der Testsuite Azure DevOps.

##### <a name="generatetestsuite-optional-parameters"></a>generatetestsuite: optionale Parameter

+ `output_dir`: Stellt das Arbeitsverzeichnis der Ausgabe dar. Das Verzeichnis muss vorhanden sein. Wenn dieser Parameter nicht festgelegt ist, wird das Arbeitsverzeichnis aus den Einstellungen verwendet.

##### <a name="generatetestsuite-examples"></a>generatetestsuite: Beispiele

`generatetestsuite Tests c:\temp\rsat`

`generatetestsuite /retry Purchase c:\rsat\last`

`generatetestsuite /dllonly /byid 121`

`generatetestsuite /keepcustomexcel /byid 121`

#### <a name="help"></a>help

Identisch mit dem [?](#section) Befehl.

#### <a name="list"></a>Liste

Listet alle verfügbaren Testfälle im aktuellen Testplan auf.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**

#### <a name="listtestplans"></a>listtestplans

Listet alle verfügbaren Testpläne auf.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**

#### <a name="listtestsuite"></a>listtestsuite

Listet Testfälle für die angegebene Testsuite auf. Mit dem Befehl ``listtestsuitenames`` können Sie alle verfügbaren Testsuiten abrufen und einen beliebigen Wert aus der Liste als **Suite_name**-Parameter verwenden.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[test_suite_name]``

##### <a name="listtestsuite-required-parameters"></a>listtestsuite: erforderliche Parameter

+ `test_suite_name`: Der Name der gewünschten Suite.

##### <a name="listtestsuite-examples"></a>listtestsuite: Beispiele

`listtestsuite "sample suite name"`

`listtestsuite NameOfTheSuite`

#### <a name="listtestsuitebyid"></a>listtestsuitebyid

Listet Testfälle für die angegebene Testsuite auf.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitebyid``**``[test_suite_id]``

##### <a name="listtestsuitebyid-required-parameters"></a>listtestsuitebyid: erforderliche Parameter

+ `test_suite_id`: Die ID der gewünschten Suite.

##### <a name="listtestsuitebyid-examples"></a>listtestsuitebyid: Beispiele

`listtestsuitebyid 12345`

#### <a name="listtestsuitenames"></a>listtestsuitenames

Listet alle verfügbaren Testsuiten im aktuellen Testplan auf.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**

#### <a name="playback"></a>playback

Spielt den Testfall ab, der mit der angegebenen Excel-Parameterdatei verknüpft ist. Dieser Befehl verwendet vorhandene lokale Automatisierungsdateien und lädt keine Dateien von Azure DevOps herunter. Dieser Befehl wird für POS Commerce Testfälle nicht unterstützt.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[/retry[=<seconds>]] [/comments[="comment"]] [excel_parameter_file]``

##### <a name="playback-optional-switches"></a>playback: optionale Schalter

+ `/retry[=seconds]`: Wenn dieser Schalter angegeben ist und Case-Testfälle durch andere RSAT-Instanzen blockiert werden, wartet der Abspielprozess die angegebene Anzahl von Sekunden und versucht es dann noch einmal. Der Standardwert für \[Sekunden\] ist 120 Sekunden. Ohne diesen Schalter wird der Prozess sofort abgebrochen, wenn Testfälle blockiert sind.
+ `/comments[="comment"]`: Geben Sie einen angepassten Informationsstring an, der in das Feld **Kommentare** auf den Zusammenfassungs- und Testergebnisseiten für Azure DevOps ausgeführte Testfälle aufgenommen wird.

##### <a name="playback-required-parameters"></a>playback: erforderliche Parameter

+ `excel_parameter_file`: Der vollständige Pfad zu einer Excel-Parameterdatei. Die Datei muss vorhanden sein.

##### <a name="playback-examples"></a>playback: Beispiele

`playback c:\RSAT\2745\attachments\Create_Purchase_Order_2745_Base.xlsx`

`playback /retry e:\temp\test.xlsx`

`playback /retry=300 e:\temp\test.xlsx`

`playback /comments="Payroll solution 10.0.0" e:\temp\test.xlsx`

#### <a name="playbackbyid"></a>playbackbyid

Spielt mehrere Testfälle gleichzeitig ab. Die Testfälle werden durch ihre ID identifiziert. Dieser Befehl lädt Dateien von Azure DevOps herunter. Sie können den Befehl ``list`` verwenden, um alle verfügbaren Testfälle abzurufen, und einen beliebigen Wert aus der ersten Spalte als **Testfall-ID** Parameter verwenden.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[/retry[=<seconds>]] [/comments[="comment"]] [test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="playbackbyid-optional-switches"></a>playbackbyid: optionale Schalter

+ `/retry[=seconds]`: Wenn dieser Schalter angegeben ist und Case-Testfälle durch andere RSAT-Instanzen blockiert werden, wartet der Abspielprozess die angegebene Anzahl von Sekunden und versucht es dann noch einmal. Der Standardwert für \[Sekunden\] ist 120 Sekunden. Ohne diesen Schalter wird der Prozess sofort abgebrochen, wenn Testfälle blockiert sind.
+ `/comments[="comment"]`: Geben Sie einen angepassten Informationsstring an, der in das Feld **Kommentare** auf den Zusammenfassungs- und Testergebnisseiten für Azure DevOps ausgeführte Testfälle aufgenommen wird.

##### <a name="playbackbyid-required-parameters"></a>playbackbyid: erforderliche Parameter

+ `test_case_id1`: Die ID eines bestehenden Testfalls.
+ `test_case_id2`: Die ID eines bestehenden Testfalls.
+ `test_case_idN`: Die ID eines bestehenden Testfalls.

##### <a name="playbackbyid-examples"></a>playbackbyid: Beispiele

`playbackbyid 878`

`playbackbyid 2345 667 135`

`playbackbyid /comments="Payroll solution 10.0.0" 2345 667 135`

`playbackbyid /retry /comments="Payroll solution 10.0.0" 2345 667 135`

#### <a name="playbackmany"></a>playbackmany

Spielt viele Testfälle gleichzeitig ab. Die Testfälle werden durch Excel-Parameterdateien identifiziert. Dieser Befehl verwendet vorhandene lokale Automatisierungsdateien und lädt keine Dateien von Azure DevOps herunter.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[/retry[=<seconds>]] [/comments[="comment"]] [excel_parameter_file1] [excel_parameter_file2] ... [excel_parameter_fileN]``

##### <a name="playbackmany-optional-switches"></a>playbackmany: optionale Schalter

+ `/retry[=seconds]`: Wenn dieser Schalter angegeben ist und Case-Testfälle durch andere RSAT-Instanzen blockiert werden, wartet der Abspielprozess die angegebene Anzahl von Sekunden und versucht es dann noch einmal. Der Standardwert für \[Sekunden\] ist 120 Sekunden. Ohne diesen Schalter wird der Prozess sofort abgebrochen, wenn Testfälle blockiert sind.
+ `/comments[="comment"]`: Geben Sie einen angepassten Informationsstring an, der in das Feld **Kommentare** auf den Zusammenfassungs- und Testergebnisseiten für Azure DevOps ausgeführte Testfälle aufgenommen wird.

##### <a name="playbackmany-required-parameters"></a>playbackmany: erforderliche Parameter

+ `excel_parameter_file1`: Der vollständige Pfad der Excel-Parameterdatei. Die Datei muss vorhanden sein.
+ `excel_parameter_file2`: Der vollständige Pfad der Excel-Parameterdatei. Die Datei muss vorhanden sein.
+ `excel_parameter_fileN`: Der vollständige Pfad der Excel-Parameterdatei. Die Datei muss vorhanden sein.

##### <a name="playbackmany-examples"></a>playbackmany: Beispiele

`playbackmany c:\RSAT\2745\attachments\Create_Purchase_Order_2745_Base.xlsx`

`playbackmany e:\temp\test.xlsx f:\RSAT\sample1.xlsx c:\RSAT\sample2.xlsx`

`playbackmany /retry=180 /comments="Payroll solution 10.0.0" e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx`

#### <a name="playbacksuite"></a>playbacksuite

Spielt alle Testfälle aus einer oder mehreren angegebenen Testsuiten ab. Wenn der Schalter /local angegeben ist, werden lokale Anhänge für die Wiedergabe verwendet. Andernfalls werden die Anhänge von Azure DevOps heruntergeladen. Mit dem Befehl ``listtestsuitenames`` können Sie alle verfügbaren Testsuiten abrufen und einen beliebigen Wert aus der ersten Spalte als **suite_name** Parameter verwenden.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[/updatedriver] [/local] [/retry[=<seconds>]] [/comments[="comment"]] ([test_suite_name1] .. [test_suite_nameN] | [/byid] [test_suite_id1] .. [test_suite_idN])``

##### <a name="playbacksuite-optional-switches"></a>playbacksuite: optionale Schalter

+ `/updatedriver`: Wenn dieser Schalter angegeben ist, wird der Webdriver des Internet-Browsers bei Bedarf aktualisiert, bevor der Abspielprozess ausgeführt wird.
+ `/local`: Dieser Schalter zeigt an, dass lokale Anhänge für die Wiedergabe verwendet werden sollen, anstatt Dateien von Azure DevOps herunterzuladen.
+ `/retry[=seconds]`: Wenn dieser Schalter angegeben ist und Case-Testfälle durch andere RSAT-Instanzen blockiert werden, wartet der Abspielprozess die angegebene Anzahl von Sekunden und versucht es dann noch einmal. Der Standardwert für \[Sekunden\] ist 120 Sekunden. Ohne diesen Schalter wird der Prozess sofort abgebrochen, wenn Testfälle blockiert sind.
+ `/comments[="comment"]`: Geben Sie einen angepassten Informationsstring an, der in das Feld **Kommentare** auf den Zusammenfassungs- und Testergebnisseiten für Azure DevOps ausgeführte Testfälle aufgenommen wird.
+ `/byid`: Dieser Schalter zeigt an, dass die gewünschte Testsuite durch ihre Azure DevOps ID identifiziert wird, anstatt durch den Namen der Testsuite.

##### <a name="playbacksuite-required-parameters"></a>playbacksuite: erforderliche Parameter

+ `test_suite_name1` Steht für den Namen der Testsuite. Dieser Parameter ist erforderlich, wenn der Schalter /byid **nicht** angegeben ist. Dieser Name ist der Name der Testsuite Azure DevOps.
+ `test_suite_nameN` Steht für den Namen der Testsuite. Dieser Parameter ist erforderlich, wenn der Schalter /byid **nicht** angegeben ist. Dieser Name ist der Name der Testsuite Azure DevOps.
+ `test_suite_id1` Steht für die Kennung der Testsuite. Dieser Parameter ist erforderlich, wenn der Schalter /byid **angegeben ist**. Bei dieser ID handelt es sich um die ID der Testsuite Azure DevOps.
+ `test_suite_idN` Steht für die Kennung der Testsuite. Dieser Parameter ist erforderlich, wenn der Schalter /byid **angegeben ist**. Bei dieser ID handelt es sich um die ID der Testsuite Azure DevOps.

##### <a name="playbacksuite-examples"></a>playbacksuite: Beispiele

`playbacksuite suiteName`

`playbacksuite suiteName suiteNameToo`

`playbacksuite /updatedriver /local /retry=180 /byid 151 156`

`playbacksuite /updatedriver /local /comments="Payroll solution 10.0.0" /byid 150`

#### <a name="playbacksuitebyid"></a>playbacksuitebyid

Ausführen aller Testfälle in der angegebenen Azure DevOps-Testsuite.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuitebyid``**``[/updatedriver] [/local] [/retry[=<seconds>]] [/comments[="comment"]] [test_suite_id]``

##### <a name="playbacksuitebyid-optional-switches"></a>playbacksuitebyid: optionale Schalter

+ `/retry[=seconds]`: Wenn dieser Schalter angegeben ist und Case-Testfälle durch andere RSAT-Instanzen blockiert werden, wartet der Abspielprozess die angegebene Anzahl von Sekunden und versucht es dann noch einmal. Der Standardwert für \[Sekunden\] ist 120 Sekunden. Ohne diesen Schalter wird der Prozess sofort abgebrochen, wenn Testfälle blockiert sind.
+ `/comments[="comment"]`: Geben Sie einen angepassten Informationsstring an, der in das Feld **Kommentare** auf den Zusammenfassungs- und Testergebnisseiten für Azure DevOps ausgeführte Testfälle aufgenommen wird.
+ `/byid`: Dieser Schalter zeigt an, dass die gewünschte Testsuite durch ihre Azure DevOps ID identifiziert wird, anstatt durch den Namen der Testsuite.

##### <a name="playbacksuitebyid-required-parameters"></a>playbacksuitebyid: erforderliche Parameter

+ `test_suite_id`: Steht für die ID der Testsuite, wie sie in Azure DevOps steht.

##### <a name="playbacksuitebyid-examples"></a>playbacksuitebyid: Beispiele

`playbacksuitebyid 2900`

`playbacksuitebyid /retry 2099`

`playbacksuitebyid /retry=200 2099`

`playbacksuitebyid /retry=200 /comments="some comment" 2099`

#### <a name="quit"></a>quit

Schließt die Anwendung. Dieser Befehl ist nur sinnvoll, wenn die Anwendungen im interaktiven Modus ausgeführt werden.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**

##### <a name="quit-examples"></a>Beenden: Beispiele

`quit`

#### <a name="upload"></a>upload

Lädt Anhangsdateien (Aufzeichnungs-, Ausführungs- und Parameterdateien), die zu einer bestimmten Testsuite oder zu Testfällen gehören, auf Azure DevOps hoch.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``([test_suite_name] | [test_case_id1] .. [test_case_idN])``

##### <a name="upload-required-parameters"></a>upload: erforderliche Parameter

+ `test_suite_name`: Alle Dateien, die zu der angegebenen Testsuite gehören, werden hochgeladen.
+ `test_case_id1`: Steht für die erste Testfall-ID, die hochgeladen werden soll. Verwenden Sie diesen Parameter nur, wenn kein Name für die Testsuite angegeben wurde.
+ `test_case_idN`: Stellt die letzte Testfall-ID dar, die hochgeladen werden soll. Verwenden Sie diesen Parameter nur, wenn kein Name für die Testsuite angegeben wurde.

##### <a name="upload-examples"></a>upload: Beispiele

`upload sample_suite`

`upload 2900`

`upload 123 456`

#### <a name="uploadrecording"></a>uploadrecording

Lädt nur die Aufzeichnungsdatei, die zu einem oder mehreren angegebenen Testfällen gehört, auf Azure DevOps hoch.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[test_case_id1] .. [test_case_idN]``

##### <a name="uploadrecording-required-parameters"></a>uploadrecording: erforderliche Parameter

+ `test_case_id1`: Stellt die erste Testfall-ID für die Aufzeichnung dar, die auf Azure DevOps hochgeladen werden soll.
+ `test_case_idN`: Steht für die letzte Testfall-ID für die Aufzeichnung, die auf Azure DevOps hochgeladen werden soll.

##### <a name="uploadrecording-examples"></a>uploadrecording: Beispiele

`uploadrecording 123`

`uploadrecording 123 456`

#### <a name="usage"></a>Verwendung

Zeigt die drei Verwendungsmodi dieser Anwendung an.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**

Interaktives Ausführen der Anwendung:

+ ``Microsoft.Dynamics.RegressionSuite.ConsoleApp``

Ausführen der Anwendung durch Angabe eines Befehls:

+ ``Microsoft.Dynamics.RegressionSuite.ConsoleApp ``**``[command]``**

Ausführen der Anwendung durch Angabe einer Einstellungsdatei:

+ ``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``/settings [drive:\Path to\file.settings] [command]``**

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

```powershell
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
