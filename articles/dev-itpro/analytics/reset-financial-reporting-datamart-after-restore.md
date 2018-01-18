---
title: "Finanzberichterstellungs-Data Mart zurücksetzen"
description: "In diesem Thema wird beschrieben, wie der Rechnungslegungs-Damart zurückgesetzt wird."
author: aolson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 261824
ms.search.region: Global
ms.author: aloson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 5b956dcc5a4a93033396ae0ffcf8b7aeba2cf3f2
ms.openlocfilehash: a07e8b5bae2c4f71e9212cd2f8080d2481769818
ms.contentlocale: de-de
ms.lasthandoff: 12/14/2017

---

# <a name="reset-the-financial-reporting-data-mart"></a>Finanzberichterstellungs-Data Mart zurücksetzen

[!include[banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie der Rechnungslegungs-Datamart für die folgenden Versionen zurückgesetzt wird:

- Microsoft Dynamics 365 for Finance and Operations Financial Reporting Release 7.2.6.0 und später
- Microsoft Dynamics 365 for Finance and Operations Financial Reporting Release 7.0.10000.4 und später
- Microsoft Dynamics 365 for Finance and Operations, Enterprise-Edition (lokal)

Um Finance and Operations Finanzberichterstellung Version 7.2.6.0 abzurufen, können Sie KB 4052514 von <https://fix.lcs.dynamics.com/Issue/Resolved?kb=4052514> herunterladen.

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-7260-and-later"></a>Setzt den Rechnungslegungs-Datamart für Finance and Operations Rechnungslegungsfreigabe 7.2.6.0 und später zurück

### <a name="reset-the-financial-reporting-data-mart-from-report-designer"></a>Setzt den Rechnungslegungs-Datamart im Berichts-Designer zurück

> [!NOTE]
> Die Schritte dieses Prozesses werden für Finance and Operations Finanzbericht Release 7.2.6.0 und später unterstützt. Wenn Sie nur eine ältere Version besitzen, wenden Sie sich für Hilfe an das Support-Team.

In bestimmten Szenarien kann es nötig sein, den Datenmarkt für die Finanzberichterstellung zurückzsetzen. Sie können diese Aufgabe im Berichts-Designer Client abschließen. Nachfolgend sind mehrere Szenarios, wo Sie möglicherweise den Data Mart zurücksetzen müssen:

- Die Finance and Operations Datenbank wurde wiederhergestellt, aber die Data Mart-Datenbank wurde nicht wiederhergestellt.
- Sie finden falsche Daten für eine Periode.
- Unterstützung weist Sie an, den Data Mart als Teil eines Problembehandlungsschritts zurückzusetzen.

Die Data Mart-Rücksetzung sollte nur für Zeiten ausgeführt werden, wenn der Betrag des Verarbeitens für die Datenbank klein ist. Finanzberichterstellung ist während dem Rücksetzungsprozesses nicht verfügbar.

#### <a name="reset-the-data-mart"></a>Data Mart zurücksetzen

Um den Data Mart im Berichts-Designer im Menü **Extras** zurückzusetzen, wählen Sie **Data Mart zurücksetzen** aus. Das Dialogfeld, das angezeigt wird, verfügt über zwei Abschnitte: **Statistik** und **Zurücksetzen**.

[![Dialogfeld Data Mart zurücksetzen](./media/Reset-72.jpg)](./media/Reset-72.jpg)

##### <a name="integration-attempts"></a>Integrationsversuche

Das Raster **Integrationsversuche** zeigt, wie oft das System versucht hat, Buchungen zu integrieren. Das System versucht weiter, Daten über einen Zeitraum von Tagen zu integrieren, wenn die ersten Versuche nicht erfolgreich sind. Sie wissen, dass der Data Mart zurückgesetzt werden muss, wenn die Anzahl von Versuchen 8 oder höher ist und wenn es viele Dimensionskombination oder Buchungsdatensätze gibt. In diesem Fall sind die Daten nicht gemeldet.

##### <a name="data-status"></a>Datenstatus

Das Raster **Datenenstatus** enthält eine Momentaufnahme der Buchungen, der Wechselkurse und Dimensionswerten im Data Mart. Eine große Anzahl von Datensätzen gibt an, dass verschiedene Aktualisierungen an Datensätzen erfolgt sind. Diese Situation kann langsamere Berichterstellungszeiten verursachen.

##### <a name="misaligned-main-account-categories"></a>Falsch ausgerichtete Hauptkontokategorien

Wenn Sie eine Version verwenden, die früher als Microsoft Dynamics 365 for Finance and Operations Financial Reporting 7.2.1 ist, müssen Sie den Data Mart zurücksetzen, wenn Sie Konten umbenennen und zwischen Kontokategorien Konten verschieben. Diese Aktivitäten können dafür verantwortlich sein, dass Hauptkontokategorien nicht korrekt abgestimmt werden. Das Feld **Falsch ausgerichtete Hauptkontokategorien** zeigt an, ob Sie dieses Problem ermitteln.

### <a name="reset-the-data-mart-in-finance-and-operations-financial-reporting-release-7260"></a>Setzt den Data Mart in Finance and Operations Financial Reporting, Release 7.2.6.0 zurück

Um den Data Mart im Bereich Finance and Operations Financial Reporting, Release 7.2.6.0 und früher zurückzusetzen im Dialogfeld **Data Mart zurücksetzen** wählen Sie **Setzen Sie Data Mart zurück**, und wählen Sie dann **OK** aus. Sie sollten den Data Marts nur während einer geplanten Ausfallzeit zurücksetzen.

[![Dialogfeld Data Mart zurücksetzen](./media/Reset-72.jpg)](./media/Reset-72.jpg)

### <a name="reset-the-data-mart-and-select-a-reason-in-microsoft-dynamics-365-for-finance-and-operations-financial-reporting-release-730"></a>Data Mart zurücksetzen und wählen Sie einen Grund in Microsoft Dynamics 365 for Finance and Operations Financial Reporting Release 7.3.0 aus.

Stellt sich heraus, dass eine Data Mart-Rücksetzung erforderlich ist, aktivieren Sie das Kontrollkästchen **Setzen Sie Data Mart zurück**, und wählen Sie dann einen Grund im Feld **Grund** aus. Die folgenden Optionen sind verfügbar:

- **Fehlende oder falsche Daten** – Basierend auf Statistiken haben Sie festgestellt, dass Daten möglicherweise fehlen. Bevor Sie fortfahren, wird empfohlen, dass Sie mit Support arbeiten, um festzustellen, was den Fehler verursacht.
- **Datenbank wiederherstellen** - Die Finance und Operations Datenbank wurde wiederhergestellt, aber die Data Mart-Datenbank wurde nicht wiederhergestellt.
- **Sonstiges** – Setzen Sie den Data Mart für einen anderen Grund zurück. Wenn Sie göaibem. dass ein Problem besteht, kontaktieren Sie den Support, um das Problem zu identifizieren.

[![Data Mart zurücksetzen](./media/Integration.png)](./media/Integration.png)

> [!NOTE]
> Überprüfen Sie, ob durch alle Data Mart-Zurücksetzungsaufgaben ein erstmaliges Laden abgeschlossen wurde, bevor Sie mit dem Zurücksetzen beginnen. Sie können dies bestätigen, indem Sie nach einem Wert in der Spalte „Letzte Laufzeit” suchen, indem Sie **Extras** &gt; **Integrationsstatus** auswählen.

#### <a name="clear-users-and-companies"></a>Benutzer und Unternehmen löschen

Aktivieren Sie das Kontrollkästchen **Deaktivieren von Benutzern und Unternehmen**, wenn die Datenbank wiederhergestellt wurde, aber Sie dann Änderungen an Benutzern oder an Unternehmen vorgenommenen haben. Sie sollten dieses Kontrollkästchen nur selten auswählen müssen.

Wenn Sie bereit sind, den Rücksetzungsprozess zu verwenden, aktivieren Sie **OK**. Sie werden aufgefordert zu bestätigen, dass, Sie bereit sind, den Prozess zu starten. Beachten Sie, dass die Finanzberichterstellung nicht verfügbar ist während der Rücksetzung und der ersten Datenintegration, die dann erfolgt.

Wenn Sie den Status bei der Integration erneut ausführen, wählen Sie **Extras** &gt; **Integrationsstatus**, um das letzte Mal zu sehen, als die Integration ausgeführt wurde und den Status.

[![Zeigt den Status der Integration](./media/New-integration.PNG)](./media/New-integration.PNG)

> [!NOTE]
> Die Zurücksetzung ist abgeschlossen, wenn alle Zuordnungen den Status „RanToCompletion” anzeigen und das Fenster „Integrationsstatus” die Meldung „Integration abgeschlossen” in der Ecke unten links wiedergibt.

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-70100004-and-later"></a>Setzt den Rechnungslegungs-Datamart für Finance and Operations Rechnungslegungsfreigabe 7.0.10000.4 und später zurück

Wenn Sie ggf. die Finance and Operations-Datenbank aus einer Sicherung wiederherstellen oder die Datenbank aus einer anderen Umgebung kopieren, müssen Sie die Schritte in diesem Thema ausführen, um sicherzustellen, dass der Rechnungslegungs-datamart ordnungsgemäß die zu stornierenden Finance and Operations-Datenbank verwendet.

> [!NOTE]
> Beachten Sie, dass die Schritte dieses Prozesses für Microsoft Dynamics AX Anwendungsversion 7.0.1 (Mai 2016 ) (Anwendungs-Build 7.0.1265.23014 und Financial Reporting Build 7.0.10000.4) und später Versionen unterstützt werden. Wenn Sie eine frühere Version von Finance and Operations nutzen, wenden Sie sich bitte an unser Support-Team.

### <a name="export-report-definitions"></a>Exportieren von Berichtsdefinitionen

Gehen Sie folgendermaßen vor, um die Berichtsdesigne im Berichts-Designer zu exportieren.

1. Wechseln Sie im Berichts-Designer zu **Unternehmen** &gt; **Bausteingruppen**.
2. Wählen Sie die Bausteingruppe aus, die exportiert werden soll, und klicken Sie **Export**.

    > [!NOTE]
    > Für Finance and Operations wird nur eine Bausteingruppe, unterstützt **Standard**.

3. Wählen Sie die Berichtsdefinition für den Export aus:

    - Klicken Sie auf **Alles markieren**, um die Berichtsdefinitionen und die dazugehörigen Bausteine zu exportieren.
    - Um bestimmte Berichte, Zeilen, Spalten, Strukturen oder Dimensionssätze zu exportieren, klicken Sie auf die entsprechende Registerkarte und wählen die Artikel aus, die exportiert werden sollen. Drücken und halten Sie die STRG-Taste gedrückt, um mehrere Elemente auf einer Registerkarte auszuwählen. Wenn Sie Berichte für den Export auswählen, werden die zugeordneten Zeilen, Spalten, Strukturen und Dimensionssätze ausgewählt.

4. Wählen Sie **Exportieren**.
5. Geben Sie einen Dateinamen eingeben und einen sicheren Ort aus, an dem Sie die exportierten Berichtsdefinitionen speichern möchten.
6. Wählen Sie **Speichern**.

Anschließend können Sie die Datei an einen sicheren Standort kopieren oder hochladen. Auf diese Weise kann die Datei in einer anderen Umgebung zu einem späteren Zeitpunkt importiert werden. Informationen zur Verwendung eines Microsoft Azure Storage-Kontos können gefunden werden in [Daten mit dem AzCopy-Kommandozeilenutility übertragen](/azure/storage/storage-use-azcopy).

> [!NOTE]
> Microsoft stellt kein Speicherkonto im Rahmen der Finance and Operations Vereinbarung bereit. Sie müssen entweder ein Speicherkonto kaufen oder ein Speicherkonto von einem separaten Azure-Abonnement verwenden.

> [!WARNING]
> Wichtig: Berücksichtigen Sie das Verhalten des D-Laufwerks von Azure Virtual Machines (VMs). Speichern Sie die exportierten Bausteingruppen auf Laufwerk D nicht permanent. Weitere Informationen zu temporären Laufwerken finden Sie unter [Einverständnis des temporären Laufwerks auf Windows Azure-virtuellen Computern](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).

### <a name="stop-services"></a>Services anhalten

Die olgenden Microsoft Windows Dienste haben offene Verbindungen zur Finance and Operations-Datenbank. Verwenden den Microsoft Remotedesktop, um sich mit allen Computern in der Umgebung zu verbinden und die folgenden Windows-Dienste zu beenden, indem Sie services.msc verwenden:

- Internet-Publishing-Dienst (Anwendungsopbjekt-Server [AOS]-Computer)
- Microsoft Dynamics 365 for Finance and Operations Batch Management Service (nur nicht-private AOS-Computern)
- Management Reporter 2012 Process Service (nur Business Intelligence [BI]-Computer)

### <a name="reset"></a>Zurücksetzen

#### <a name="download-the-latest-minorversiondataupgradezip-package"></a>Suchen und laden Sie das letzte MinorVersionDataUpgrade.zip-Paket herunter

Suchen und laden Sie das letzte MinorVersionDataUpgrade.zip-Paket herunter. Anweisungen dazu, wie Sie die korrekte Version des Datenaktualisierungspakets suchen, finden Sie unter und[Das letzte Datenaktualisierungbereitstellungspaket herunterladen](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package). 

Eine Aktualisierung ist nicht erforderlich, um das MinorVersionDataUpgrade.zip-Paket herunterzuladen. Deshalb müssen Sie derzeit die Schritte ausführen unter "Herunterladen zur Bereitstellung geeigneter Paket der Datenaktualisierung". Sie können alle anderen Schritte im Thema überspringen.

#### <a name="run-scripts-against-the-finance-and-operations-database"></a>Ausführen von Skripts für die Finance and Operations-Datenbank

Führen Sie die folgenden Skripts für die Finance and Operations-Datenbank aus (nicht für die Financial-Reporting-Datenbank):

- DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql
- DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql

Diese Skripts helfen sicherzustellen, dass die Benutzer, die Rollen und die Änderungsnachverfolgungseinstellungen korrekt sind.

#### <a name="run-a-windows-powershell-command-to-reset-the-database"></a>Führen Sie Windows PowerShell-Befehls aus, um Datenbankfeinabstimmungen zurückzusetzen

Starten Sie auf einem Microsoft Windows PowerShell als Administrator und führen Sie die folgenden Schritte aus, um die Integration zwischen Finance and Operations und Financial Reporting zurückzusetzen.

```
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail "<reason for resetting>"
```

Ist eine kurze Erläuterung der im Parameter im Befehl **Zurückgesetzt-DatamartIntegration**:

- Die gültigen Werte für **Reason** sind **SERVICING**, **BADDATA**, und **OTHER**.
- Der **ReasonDetail**-Parameter ist Freitext.
- Grund und Grund-Detail werden in der Telemetrie-/Umgebungsüberwachung erfasst.

> [!NOTE]
> Nachdem Sie die Befehle ausgeführt haben, werden Sie gebeten, **J** einzugeben, um zu bestätigen, dass Sie die Datenbank zurücksetzen möchten.

#### <a name="restart-services"></a>Dienste neu starten

Verwenden Sie services.msc, um die Services neu zu starten, die Sie eben beendeten:

- Per Internet WWW-Publishing-Dienst (für alle AOS-Computer)
- Microsoft Dynamics 365 for Finance and Operations Batch Management Service (nur nicht-private AOS-Computern)
- Management Reporter 2012 Process Service (nur BI-Computer)

#### <a name="import-report-definitions"></a>Imporiteren von Berichtsdefinitionen

Importieren Sie die Berichtsdesigns im Berichts-Designer, und zwar mithilfe der Datei, die während des Exports erstellt wird.

1. Wechseln Sie im Berichts-Designer zu **Unternehmen** &gt; **Bausteingruppen**.
2. Wählen Sie die Bausteingruppe aus, die exportiert werden soll, und klicken Sie **Export**.

    > [!NOTE]
    > Für Finance and Operations wird nur eine Bausteingruppe, unterstützt **Standard**.

3. Wählen Sie den **Standard**-Baustein und klicken Sie auf **Importieren**.
4. Wählen Sie die Datei aus, welche die exportierten Berichtsdefinitionen enthält und klicken Sie auf **Öffnen**.
5. Wählen Sie im Dialogfeld **Importieren** die Berichtsdefinitionen für den Import aus:

    - Klicken Sie auf **Alles markieren**, um die Berichtsdefinitionen und die dazugehörigen Bausteine zu importieren.
    - Zum Importieren bestimmter Berichte, Zeilen, Spalten, Strukturen oder Dimensionssätze wählen Sie die entsprechenden Berichte, Spalten, Strukturen oder Dimensionssätze aus.

6. **Import** auswählen

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-on-premises"></a>Setzt den Data Mart in Finance and Operations Financial Reporting (lokal) zurück

1. Weisen Sie alle Benutzer an, den Berichts-Designer und den Rechnungslegungsbereich in Finance and Operations. zu beenden.
2. Führen Sie das folgende Skript für die Rechnungslegungsdatenbank aus (MRDB).

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ```

3. Schneiden oder löschen Sie alle Datensätze aus der FINANCIALREPORTS-Tabelle in der Finance and Operations-Datenbank (AXDB).
4. Schneiden oder löschen Sie alle Datensätze aus der FINANCIALREPORTS-Tabelle in der Finance and Operations-Datenbank. Wenn die Tabelle nicht in der Finance and Operations-Datenbank vorhanden ist, können Sie diesen Schritt überspringen.
5. Führen Sie das **ResetDatamart.sql** Skript für die Rechnungslegungsdatenbank aus (MRDB). Dieses Skript deaktiviert die Data Mart-Integration, löscht alle Data Mart-Daten Data und aktiviert anschließend Data Mart erneut.

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ------------------------------
    PRINT 'Drop archive tables'
    ------------------------------
    DECLARE @tableId nvarchar(max)
    DECLARE dropCursor CURSOR LOCAL FAST_FORWARD FOR
    SELECT Id FROM [Datamart].Archive
    OPEN dropCursor
    FETCH NEXT FROM dropCursor INTO @tableId
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'FactStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].FactStaging' + @tableId)
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationStaging' + @tableId)
        FETCH NEXT FROM dropCursor INTO @tableId
    END
    CLOSE dropCursor
    DEALLOCATE dropCursor
    IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationProcessing' and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationProcessing')
    ------------------------------
    PRINT 'Begin Truncating tables'
    ------------------------------
    DECLARE @tablename nvarchar(200)
    DECLARE @schemaname nvarchar(200)
    DECLARE clear_tables CURSOR
        FOR SELECT TABLE_NAME, TABLE_SCHEMA FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_SCHEMA = 'Datamart' AND TABLE_TYPE='BASE TABLE'
    PRINT 'remove check constraints'
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename + '] NOCHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'delete data from tables and rebuild indexes'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
            IF(EXISTS (select TOP 1 1 from sys.foreign_keys where referenced_object_id = OBJECT_ID(@schemaname + '.' + @tablename)) OR
            EXISTS(SELECT TOP 1 1 FROM sys.sql_expression_dependencies sed
            INNER JOIN sys.objects o ON sed.referencing_id = o.[object_id]
            WHERE o.[type] = 'V' 
            AND referenced_schema_name = @schemaname
            AND referenced_entity_name = @tablename))
            BEGIN
            PRINT 'deleting from ' + @tablename
            EXEC('DELETE FROM [' + @schemaname + '].[' + @tablename + ']')
            END
            ELSE
            BEGIN
            PRINT 'truncating from ' + @tablename
            EXEC('TRUNCATE TABLE [' + @schemaname + '].[' + @tablename + ']')
            END
        END
        EXEC('ALTER INDEX ALL ON [' + @schemaname + '].[' + @tablename + '] REBUILD')
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'reenable check constraints'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename +'] WITH CHECK CHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    DEALLOCATE clear_tables
    ------------------------------
    PRINT 'Complete Truncating tables'
    ------------------------------
    ------------------------------
    PRINT 'Remove indexes from DimensionCombination'
    ------------------------------
    DECLARE @indexname nvarchar(200)
    DECLARE drop_indexes CURSOR
    FOR SELECT Name FROM sys.indexes WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]') AND is_primary_key = 0
    OPEN drop_indexes
    FETCH NEXT FROM drop_indexes INTO @indexname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('DROP INDEX [' + @indexname + '] on [Datamart].[DimensionCombination]')
        FETCH NEXT FROM drop_indexes INTO @indexname
    END
    CLOSE drop_indexes
    DEALLOCATE drop_indexes
    ------------------------------
    PRINT 'Drop Columns on DimensionCombination'
    ------------------------------
    DECLARE @objectname nvarchar(200)
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId', 'InactiveDimensions')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombination] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationResolving'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationResolving]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationResolving] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationStaging'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationStaging]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'OrganizationId', 'Description', 'SourceKey', 'OrganizationKey', 'FreshnessDate')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationStaging] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationUnreferenced'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationUnreferenced]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationUnreferenced] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionValueAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionValueAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('DimensionValueId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionValueAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on FactAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[FactAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('FactId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[FactAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalance'
    ------------------------------
    DECLARE @name nvarchar(200)
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalance'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    -- Rebuild dropped indexes that are dynamic
    EXEC [Datamart].ConfigureIndexesAndConstraints
    ------------------------------------------
    ------------------------------------------
    PRINT 'Reset the map tokens'
    UPDATE [Connector].[Map] SET InitalLoad = 0, ReaderToken=NULL, LastQuerySuccess='1900-01-01' WHERE MapId IN (SELECT t.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Reset the tasks'
    UPDATE [Scheduling].[TaskState] SET StateType = 0, Progress = 0.0, LastRunTime = NULL, NextRunTime = NULL WHERE TaskId IN (SELECT ts.[TaskId]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8'))
    PRINT 'Enable integration tasks, RunImmediately'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 1, StartBoundary = '1900-01-01' 
    WHERE Id in (SELECT [id] from @triggerIds WHERE taskTypeId = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Enable the Maintenance Task'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 0, StartBoundary = GETDATE() WHERE Id in
    (SELECT [id] from @triggerIds WHERE taskTypeId = 'D81C1197-D486-4FB7-AF8C-078C110893A0')
    ------------------------------------------
    ------------------------------------------
    ```

6. Nach dem Zurücksetzen können Sie das Neuladen der Daten manuell prüfen, indem Sie in der Abfrage für die Rechnungslegungsdatenbank ausführen.

    ```
    select ReaderObjectName, WriterObjectName, LastRunTime, StateType from Connector.MapsWithDetail with (nolock)
    ```

    Bestätigen Sie, ob alle Zeilen **LastRunTime** einen Wert angeben und dass **StateType** auf **5** festgelegt ist. Ein **StateType**-Wert **5** gibt an, dass die Daten erfolgreich erneut geladen wurden. Ein Wert von **7** wird ein falsches Bundesland angezeigt. Manchmal hat die Organisationshierarchiezuordnung dieses Status das erste Mal, wenn sie ausgeführt wird. Allerdings sollte das bemängelte Bundesland jedoch automatisch gelöst werden.

