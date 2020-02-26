---
title: Verwenden des Regression Suite Automation Tool-Tutorials
description: Dieses Thema zeigt, wie das Regression Suite Automation Tool (RSAT) verwendet wird. Es beschreibt die verschiedenen Funktionen und enthält Beispiele, die erweiterte Skripterstellung verwenden.
author: kfend
manager: AnnBe
ms.date: 06/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 21761
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 026d1d743b5150f152ef70aa642dcf6841a4e398
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025803"
---
# <a name="use-the-regression-suite-automation-tool-tutorial"></a>Das Regression Suite Automation Tool-Tutorial anweden

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Verwenden Sie das Internet-Browsertool, um die Seite in pdf-Format herunterzuladen und zu speichern. 

Dies Tutorial führt Sie durch mehrere der erweiterten Funktionen des Regression Suite Automation Tool (RSAT), enthält eine Demozuweisung und beschreibt Strategie und wichtige Lernpunkte.

## <a name="features-of-rsattask-recorder"></a>Funktionen von RSAT/Aufgabenaufzeichnung

### <a name="validate-a-field-value"></a>Einen Feldwert überprüfen

Informationen zu dieser Funktion finden Sie unter [Erstellen einer neuen Aufgabenaufzeichnung mit einer Validierungsfunktion](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function) Sie unter.

### <a name="saved-variable"></a>Variable gespeichert

Informationen zu dieser Funktion finden Sie unter [Ändern einer vorhandenen Aufgabenaufzeichnung, um eine gespeicherte Variable zu erstellen](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable).

### <a name="derived-test-case"></a>Abgeleitete Testfälle

1. Öffnen Sie das Regression Suite Automation Tool (RSAT) und wählen Sie beide Testfälle aus, die Sie in [Einrichtung und Installation des Regression Suite Automation Tools](./hol-set-up-regression-suite-automation-tool.md) erstellt haben.
2. Wählen Sie **Neu \>Abgeleiteten Testfall berechnen** aus.

    ![Abgeleiteten Testfallbefehl im Menü „Neu“ erstellen](./media/use_rsa_tool_01.png)

3. Sie erhalten eine Meldung, die angibt, dass ein abgeleiteter Testfall für jeden ausgewählten Testfall in der aktuellen Testsuite erstellt wird und dass jeder abgeleitete Testfall eine eigene Kopie der Excel-Parameterdatei hat. Wählen Sie **OK**.

    > [!NOTE]
    > Wenn Sie einen abgeleiteten Testfall ausführen, verwendet er die Aufgabenaufzeichnung des übergeordneten Testfalls und die eigene Kopie der Excel-Parameterdatei. Auf diese Weise können Sie den gleichen Test mit unterschiedlichen Parametern erstellen, ohne mehr als eine Aufgabenaufzeichnung verwalten zu müssen. Ein abgeleiteter Testfall muss kein Teil der gleichen Testsuite wie der übergeordneter Testfall sein.

    ![Meldungsfeld](./media/use_rsa_tool_02.png)

    Zwei zusätzliche abgeleitete Testfälle werden erstellt, und das Kontrollkästchen **Abgeleitet?** für sie wird aktiviert.

    ![Abgeleitete Testfälle erstellt](./media/use_rsa_tool_03.png)

    Ein abgeleiteter Testfall wird automatisch in Azure DevOps erstellt. Es ist ein untergeordnetes Element des Testfalls **Neues Produkt erstellen** und es ist mit einem speziellen Schlüsselwort markiert: **RSAT:DerivedTestSteps**. Diese Testfälle werden ebenfalls automatisch dem Testplan in Azure DevOps hinzugefügt.

    ![RSAT:DerivedTestSteps-Schlüsselwort](./media/use_rsa_tool_04.png)

    > [!NOTE]
    > Wenn die abgeleiteten Testfälle, die erstellt werden, aus irgendeinem Grund nicht in der richtigen Reihenfolge vorliegen, wechseln Sie zu Azure DevOps und ordnen Sie die Testfälle in der Testsuite neu an, damit RSAT sie in der richtigen Reihenfolge ausführen kann.

4. Wählen Sie die abgeleiteten Testfälle aus, und wählen Sie dann **Bearbeiten** aus, um die entsprechenden Excel-Parameterdateien zu öffnen.
5. Bearbeiten Sie diese Excel-Parameterdateien auf die gleiche Weise, wie Sie die übergeordneten Dateien bearbeitet haben. Stellen Sie also sicher, dass die Produktkennung so festgelegt ist, dass sie automatisch generiert wird. Stellen Sie außerdem sicher, dass die gespeicherte Variable in die relevanten Felder kopiert wird.
6. Aktualisieren Sie auf der Registerkarte **Allgemein** beider Excel-Parameterdateien den Wert des Felds **Unternehmen** auf **USSI**, sodass die abgeleiteten Testfälle für eine andere juristische Person als der übergeordnete Testfall ausgeführt werden. Um die Testfälle für einen bestimmten Benutzer (oder die Rolle, die einem bestimmten Benutzer zugeordnet ist) auszuführen, können Sie den Wert des Felds **Testbenutzer** aktualisieren.
7. Wählen Sie **Ausführen** aus, und überprüfen Sie, dass das Produkt in der juristischen USMF-Person und in der juristischen USSI-Person erstellt wird.

### <a name="validate-notifications"></a>Benachrichtigungen validieren

Diese Funktion kann verwendet werden, um zu überprüfen, ob eine Aktivität stattfand. Wenn ein Produktionsauftrag beispielsweise erstellt, vorkalkuliert und dann gestartet wird, zeigt die App eine „Produktion – Start“-Nachricht, die Sie darüber zu informieren, dass der Produktionsauftrag gestartet wurde.

![Produktion – Start-Benachrichtigung](./media/use_rsa_tool_05.png)

Sie können diese Meldung über RSAT überprüfen, indem Sie den Nachrichtentext auf der Registerkarte **MessageValidation** der Excel-Parameterdatei für die entsprechende Erfassung eingeben.

![Registerkarte Nachrichtenvalidierung](./media/use_rsa_tool_06.png)

Nachdem der Testfall ausgeführt wurde, wird die Nachricht in der Excel-Parameterdatei mit der Nachricht verglichen, die angezeigt wird. Wenn die Nachrichten nicht übereinstimmen, schlägt der Testfall fehl.

> [!NOTE]
> Sie können mehrere Nachrichten auf der Registerkarte **MessageValidation** in der Excel-Parameterdatei eingeben. Die Nachrichten können auch Fehler- oder Warnmeldungen anstelle der Informationsmeldungen sein.

### <a name="validate-values-by-using-operators"></a>Überprüfen der Werte mithilfe von Operatoren

In früheren Versionen von RSAT, konnten Sie Werte nur überprüfen, wenn ein Kontrollwert einem erwarteten Wert entsprach. Mit der neuen Funktion können Sie prüfen, dass eine Variable ungleich, kleiner oder größer als ein angegebener Wert ist.

- Um diese Funktion zu verwenden, öffnen Sie die Datei **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** im RSAT-Installationsordner (beispielsweise **C:\\Programme (x86)\\Regression Suite Automation Tool**), und ändern Sie den Wert im folgenden Element von **false** auf **true**.

    ```xml
    <add key="AddOperatorFieldsToExcelValidation" value="false" />
    ```

    In der Excel-Parameterdatei wird das neue Feld **Operator** angezeigt.

    > [!NOTE]
    > Wenn Sie eine ältere Version von RSAT verwendet haben, müssen Sie neue Excel-Parameterdateien generieren.

    ![Feld „Operator“](./media/use_rsa_tool_07.png)

Das folgende Beispiel veranschaulicht, wie Sie diese Funktion verwenden können, um zu prüfen, ob der Lagerbestand mehr als 0 (null) ist.

1. In den Demodaten im **USMF**-Unternehmen erstellen Sie eine Aufgabenaufzeichnung, die die folgenden Schritte ausführt:

    1. Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \>Freigegebene Produkte**.
    2. Verwenden Sie den Schnellfilter, um Datensätze zu suchen. Filtern Sie beispielsweise auf einen Wert von **1000** für das Feld **Artikelnummer**.
    3. Wählen Sie **Verfügbarer Lagerbestand** aus
    4. Verwenden Sie den Schnellfilter, um Datensätze zu suchen. Filtern Sie beispielsweise auf einen Wert von **1** für das Feld **Website**.
    5. Markieren Sie in der Liste die ausgewählte Zeile.
    6. Überprüfen Sie, dass der Wert des Feldes **Verfügbare Summe** **411,0000000000000000** ist.

2. Speichern Sie die Aufgabenaufzeichnung in der die BPM-Bibliothek in LCS und synchronisieren Sie sie mit Azure DevOps.
3. Fügen Sie den Testfall dem Testplan hinzu, und laden Sie den Testfall in RSAT.
4. Öffnen Sie die Excel-Parameterdatei. Auf der Registerkarte **InventOnhandItem** wird ein Abschnitt **InventOnhandItem validieren** angezeigt, die ein **Operator**-Feld enthält.

    ![Feld „Operator“](./media/use_rsa_tool_08.png)

5. Um zu Prüfen, ob der verfügbare Bestand immer größer als 0 ist, ändern Sie den Wert des Feldes **Wert** von **411** auf **0** und den Wert des Felds **Operator** von einem Gleichheitszeichen (**=**) zu einem Größer-als-Zeichen (**\>**).

    ![Geänderte Werte der Felder „Wert“ und „Operator“](./media/use_rsa_tool_09.png)

6. Speichern und schließen Sie die Excel-Parameterdatei.
7. Wählen Sie **Hochladen** aus, um die Änderungen zu speichern, die Sie an der Excel-Parameterdatei vorgenommen haben Azure DevOps.

Wenn der Wert des Feldes **Verfügbare Summe** jetzt für den angegebenen Artikel im Bestand größer als 0 (null) ist, sind Tests unabhängig vom tatsächlichen Wert des verfügbaren Bestands erfolgreich.

### <a name="generator-logs"></a>Generatorprotokolle

Diese Funktion erstellt einen Ordner, der die Protokolle der durchgeführten Testfälle enthält.

- Um diese Funktion zu verwenden, öffnen Sie die Datei **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** im RSAT-Installationsordner (beispielsweise **C:\\Programme (x86)\\Regression Suite Automation Tool**), und ändern Sie den Wert im folgenden Element von **false** auf **true**.

    ```xml
    <add key="LogGeneration" value="false" />
    ```

Nachdem die Testfälle ausgeführt werden, finden Sie die Protokolldateien unter **C:\\Benutzer\\\<Benutzername\>\\AppData\\Roaming\\regressionTool\\generatorLogs**.

![GeneratorLogs-Ordner](./media/use_rsa_tool_10.png)

> [!NOTE]
> Wenn Testfälle vorhanden waren, bevor Sie den Wert in der CONFIG-Datei geändert haben, werden keine Protokolle für diese Testfälle generiert, bis Sie neue Testausführungsdateien generieren.
> 
> ![Befehl „Nur Textbewertungsfelder generieren“ im Menü „Neu“](./media/use_rsa_tool_11.png)

### <a name="snapshot"></a>Momentaufnahme

Diese Funktion nimmt Screenshots der Schritte auf, die während der Aufgabenaufzeichnung ausgeführt wurden.

- Um diese Funktion zu verwenden, öffnen Sie die Datei **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** im RSAT-Installationsordner (beispielsweise **C:\\Programme (x86)\\Regression Suite Automation Tool**), und ändern Sie den Wert des folgenden Elements von **false** auf **true**.

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

Unter **C:\\Benutzer\\\<Benutzername\>\\AppData\\Roaming\\regressionTool\\Playback** wird ein separater Ordner für jeden Testfall erstellt, der ausgeführt wird.

![Momentaufnahme-Ordner für einen Testfall](./media/use_rsa_tool_12.png)

In jedem dieser Ordner können Sie Momentaufnahmen der Schritte finden, die ausgeführt wurden, als die Testfälle ausgeführt wurden.

![Momentaufnahmedateien](./media/use_rsa_tool_13.png)

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

![Ablauf für das Demoszenario](./media/use_rsa_tool_14.png)

Die folgende Abbildung zeigt den Geschäftsprozess für dieses Szenario in RSAT.

![Geschäftsprozesse für das Demoszenario](./media/use_rsa_tool_15.png)

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

### <a name="command-line"></a>Befehlszeile

RSAT kann von einem Fenster **Eingabeaufforderung** aufgerufen werden.

> [!NOTE]
> Überprüfen Sie, dass die Umgebungsvariable **TestRoot** auf den RSAT-Installationspfad festgelegt ist. (Öffnen Sie Microsoft Windows in der **Systemsteuerung**, wählen Sie **System und Sicherheit \> System \> Erweiterte Systemeinstellungen** und **Umgebungsvariablen** aus.)

1. Öffnen Sie ein Fenster **Eingabeaufforderung** als Administrator.
2. Führen Sie das Tool im Installationsverzeichnis aus.

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
        list
        listtestsuite suite_name
        download test_case_id output_dir
        generate test_case_id output_dir
        generatederived parent_test_case_id test_plan_id test_suite_id
        generatetestonly test_case_id output_dir
        edit excel_file
        playback excel_file
        playbackmany excel_file1 [excel_file2 [.. excel_fileN]]
        playbackbyid test_case_id1 [test_case_id2 [.. test_case_idN]]
        playbacksuite suite_name
        clear
        help
        about
        quit
    ```

### <a name="windows-powershell-examples"></a>Windows PowerShell-Beispiele

#### <a name="run-a-test-case-in-a-loop"></a>Ausführen eines Testfalls in einer Schleife

Sie haben ein Testskript, das einen neuen Debitor erstellt. Über Skripterstellung kann dieser Testfall in einer Schleife ausgeführt werden, indem Sie die folgenden Daten zufällig generieren, bevor jede Iteration ausgeführt wird:

- Debitorkennung
- Name des Debitors
- Adresse des Debitors

Die Debitorenkennung hat das Format *ATCUS \<Nummer\>*, wobei \<Nummer\> ein Wert zwischen **000000001** und **999999999** ist.

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
$excelFilename = "full path to excel file parameter file"
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
