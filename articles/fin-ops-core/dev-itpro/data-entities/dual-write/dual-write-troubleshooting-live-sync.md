---
title: Probleme mit der Live-Synchronisierung behandeln
description: Dieser Artikel enthält Informationen zur Fehlerbehebung, mit denen Sie Probleme beheben können, die mit der Live-Synchronisierung zusammenhängen.
author: RamaKrishnamoorthy
ms.date: 08/19/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: b6650c92d22aee5394460e4e32bfd0ad3a7698c7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289453"
---
# <a name="troubleshoot-live-synchronization-issues"></a>Probleme mit der Live-Synchronisierung behandeln

[!include [banner](../../includes/banner.md)]



Dieser Artikel enthält Informationen zur Problembehandlung für die Dual-write Integration zwischen Finanz- und Betriebs-Apps und Microsoft Dataverse. Dieses Thema enthält speziell Informationen zur Fehlerbehebung, mit denen Sie Probleme beheben können, die mit der Live-Synchronisierung zusammenhängen.

> [!IMPORTANT]
> Einige der in diesem Artikel behandelten Probleme erfordern möglicherweise entweder die Systemadministratorrolle oder Mandantenadministrator-Anmeldeinformationen für Azure Active Directory (Azure AD). Jeder Abschnitt erläutert, ob eine bestimmte Rolle oder bestimmte Anmeldeinformationen erforderlich sind.

## <a name="live-synchronization-shows-an-error-when-you-create-a-row"></a>Live-Synchronisierung zeigt beim Erstellen einer Zeile einen Fehler an

Sie erhalten möglicherweise die folgende Fehlermeldung, wenn Sie eine Zeile in einer Finanz- und Betriebs-App erstellen:

*\[{\\„Fehler\\“:{\\„Code\\“:\\„0x80072560\\“,\\„Botschaft\\“:\\„Der Benutzer ist kein Mitglied der Organisation.\\“}}\], Der Remote-Server hat einen Fehler zurückgegeben: (403) Verboten. „}}“.*

Befolgen Sie die Schritte, um das Problem zu beheben unter [Systemanforderungen und -voraussetzungen](requirements-and-prerequisites.md). Um diese Schritte auszuführen, müssen die Benutzer der Dual-Write-Anwendung, die in Dataverse erstellt wurden, die Systemadministratorrolle haben. Das Standard-Besitzerteam muss auch die Systemadministratorrolle haben.

## <a name="live-synchronization-shows-an-error-when-you-try-to-save-table-data"></a>Live-Synchronisierung zeigt beim Versuch, Tabellendaten zu speichern, einen Fehler an

**Erforderliche Rolle zum Beheben der Fehler:** System Administrator

Möglicherweise erhalten Sie die folgende Fehlermeldung, wenn Sie versuchen, Tabellendaten in einer Finanz- und Betriebs-App zu speichern:

*Die Änderungen können nicht in der Datenbank gespeichert werden. Arbeitseinheit kann keine Transaktion festschreiben. Daten können nicht in Entitäts-Uoms geschrieben werden. Das Schreiben in UnitOfMeasureEntity ist mit der Fehlermeldung fehlgeschlagen. Synchronisierung mit Entitäts-Uoms nicht möglich.*

Um das Problem zu beheben, stellen Sie sicher, dass die erforderlichen Referenzdaten sowohl in der Finanz- und Betriebs-App als auch in der App Dataverse vorhanden sind. Wenn beispielsweise ein Kundendatensatz zu einer bestimmten Kundengruppe gehört, stellen Sie sicher, dass der Kundengruppendatensatz in Dataverse vorhanden ist.

Wenn die Daten in beiden Fällen vorhanden sind und Sie bestätigt haben, dass das Problem nicht datenbezogen ist, führen Sie die folgenden Schritte aus.

1. Öffnen Sie die Entität **DualWriteProjectConfigurationEntity** mithilfe des Excel-Add-Ins. Um das Add-in zu verwenden, aktivieren Sie den Entwurfsmodus im Excel-Add-in für Finanzen und Betrieb und fügen Sie **DualWriteProjectConfigurationEntity** zu einem Arbeitsblatt hinzu. Weitere Informationen finden Sie unter [Entitätsdaten mit Excel anzeigen und aktualisieren](../../office-integration/use-excel-add-in.md).
2. Wählen Sie die Datensätze aus, bei denen Probleme bei der Zuordnung beim dualen Schreiben und im Projekt auftreten. Für jede Zuordnung beim dualen Schreiben gibt es zwei Datensätze.
3. Veröffentlichen Sie die Änderungen mithilfe des Excel-Add-Ins. Dieser Schritt ist wichtig, da er die Datensätze aus der Entität und den zugrunde liegenden Tabellen löscht.

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a>Behandeln Sie Lese- oder Schreibberechtigungsfehler, wenn Sie Daten in einer Finanz- und Betriebs-App erstellen

Möglicherweise erhalten Sie eine Fehlermeldung „Bad Request“, wenn Sie Daten in einer Finanz- und Betriebs-App erstellen.

![Beispiel für die Fehlermeldung „Ungültige Anforderung“.](media/error_record_id_source.png)

Um das Problem zu beheben, müssen Sie die fehlenden Berechtigungen aktivieren, indem Sie dem Team der zugeordneten Geschäftseinheit Dynamics 365 Sales oder Dynamics 365 Customer Service die richtige Sicherheitsrolle zuweisen.

1. Suchen Sie in der Finanz- und Betriebs-App die Unternehmenseinheit, die im Verbindungsset Data Integration festgelegt ist.

    ![Organisationszuordnung.](media/mapped_business_unit.png)

2. Melden Sie sich in der Kundenbindungs-App bei der Umgebung an, gehen Sie zu **Einstellungen \> Sicherheit** und finden Sie das Team der zugeordneten Geschäftseinheit.

    ![Team des zugeordneten Geschäftsbereichs.](media/setting_security_page.png)

3. Öffnen Sie die Seite für das Team zum Bearbeiten und wählen Sie dann **Rollen verwalten** aus.

    ![Schaltfläche Rollen verwalten.](media/manage_team_roles.png)

4. Weisen Sie im Dialogfeld **Teamrollen verwalten** die Rolle mit Lese-/Schreibberechtigung für die entsprechenden Tabellen zu und wählen Sie dann **OK** aus.

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-dataverse-environment"></a>Beheben Sie Synchronisierungsprobleme in einer Umgebung, die eine kürzlich geändert Dataverse Umgebung hat

**Erforderliche Rolle zum Beheben der Fehler:** System Administrator

Möglicherweise erhalten Sie die folgende Fehlermeldung, wenn Sie Daten in einer Finanz- und Betriebs-App erstellen:

*{„entityName“:„CustCustomerV3Entity“,„executeStatus“:2,„fieldResponses“:\[\],„recordResponses“:\[{„Fehlermeldung“:„**Nutzdaten für die Entität CustCustomerV3Entity können nicht generiert werden**“,„logDateTime“:„2019-08-27T18:51:52.5843124Z“,„verboseError“:„Die Erstellung der Nutzdaten ist mit dem Fehler fehlgeschlagen. Ungültiger URI: URI ist leer.“}\],„isErrorCountUpdated“: true}*

So sieht der Fehlermeldung in der Kundenbindungs-App aus:

> Ein unerwarteter Fehler ist im ISV-Code aufgetreten. (ErrorType = ClientError) Unerwartete Ausnahme vom Plug-In (Ausführen): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: Entitätskonto konnte nicht verarbeitet werden – (Ein Verbindungsversuch ist fehlgeschlagen, da die verbundene Partei nach einer bestimmten Zeit nicht ordnungsgemäß geantwortet hat oder der Verbindungsaufbau fehlgeschlagen ist, da der verbundene Host nicht reagiert hat.)

Dieser Fehler tritt auf, wenn die Umgebung Dataverse fälschlicherweise zurückgesetzt wird, wenn Sie versuchen, Daten in der Finanz- und Betriebs-App zu erstellen.

> [!IMPORTANT]
> Wenn Sie die Umgebungen erneut verknüpft haben, müssen Sie alle Entitätszuordnungen stoppen, bevor Sie mit den Maßnahmen zur Risikominderung fortfahren.

Um das Problem zu beheben, müssen Sie die Schritte sowohl in Dataverse als auch in der Finanz- und Betriebs-App ausführen.

1. Führen Sie in der Finanz- und Betriebs-App die folgenden Schritte aus:

    1. Öffnen Sie die Entität **DualWriteProjectConfigurationEntity** mithilfe des Excel-Add-Ins. Um das Add-in zu verwenden, aktivieren Sie den Entwurfsmodus im Excel-Add-in für Finanzen und Betrieb und fügen Sie **DualWriteProjectConfigurationEntity** zu einem Arbeitsblatt hinzu. Weitere Informationen finden Sie unter [Entitätsdaten mit Excel anzeigen und aktualisieren](../../office-integration/use-excel-add-in.md).
    2. Wählen Sie die Datensätze aus, bei denen Probleme bei der Zuordnung beim dualen Schreiben und im Projekt auftreten. Für jede Zuordnung beim dualen Schreiben gibt es zwei Datensätze.
    3. Veröffentlichen Sie die Änderungen mithilfe des Excel-Add-Ins. Dieser Schritt ist wichtig, da er die Datensätze aus der Entität und den zugrunde liegenden Tabellen löscht.
    4. Um Fehler zu vermeiden, wenn Sie die Umgebungen Finance und Operations oder Dataverse neu verknüpfen, stellen Sie sicher, dass keine Dual-write-Konfigurationen übrig bleiben.

2. Führen Sie in Dataverse die folgenden Schritte aus:

    1. Melde dich bei Ihrer Dataverse-Umgebung an (z. B. `https://*****.crm.dynamics.com/`).
    2. Gehen Sie zu **Erweiterte Einstellungen** \> **Erweiterte Suche**.
    3. Wählen Sie **DualWrite-Runtime-Konfiguration** aus.
    4. Wählen Sie die anzuzeigende Spalte aus.
    5. Wählen Sie **Ergebnisse** aus, um die Konfigurationen anzuzeigen.
    6. Löschen Sie alle Instanzen.

3. Führen Sie in der Finanz- und Betriebs-App die folgenden Schritte aus:

    1. Öffnen Sie die Entität **DualWriteProjectConfigurationEntity** mithilfe des Excel-Add-Ins. Um das Add-in zu verwenden, aktivieren Sie den Entwurfsmodus im Excel-Add-in für Finanzen und Betrieb und fügen Sie **DualWriteProjectConfigurationEntity** zu einem Arbeitsblatt hinzu. Weitere Informationen finden Sie unter [Entitätsdaten mit Excel anzeigen und aktualisieren](../../office-integration/use-excel-add-in.md).
    2. Wählen Sie die Datensätze aus, bei denen Probleme bei der Zuordnung beim dualen Schreiben und im Projekt auftreten. Für jede Zuordnung beim dualen Schreiben gibt es zwei Datensätze.
    3. Veröffentlichen Sie die Änderungen mithilfe des Excel-Add-Ins. Dieser Schritt ist wichtig, da er die Datensätze aus der Entität und den zugrunde liegenden Tabellen löscht.
    4. Um Fehler zu vermeiden, wenn Sie die Umgebungen Finance und Operations oder Dataverse neu verknüpfen, stellen Sie sicher, dass keine Dual-write-Konfigurationen übrig bleiben.

## <a name="live-synchronization-error-after-you-do-a-full-database-copy"></a>Live-Synchronisierungsfehler nach dem Kopieren der vollständigen Datenbank

Möglicherweise erhalten Sie die folgende Fehlermeldung, nachdem Sie eine vollständige Datenbank von einem System auf ein anderes kopiert und anschließend versucht haben, einen Datenbankvorgang auszuführen:

*SecureConfig-Organisation (???) stimmt nicht mit tatsächlicher CRM-Organisation (???) überein.*

Die Fehlermeldung wird vom Runtime-Plug-In für duales Schreiben angezeigt, um sicherzustellen, dass die in einem System eingerichtete Konfiguration für duales Schreiben nicht in einem anderen System verwendet werden kann.

Um das Problem zu beheben, löschen Sie alle Datensätze in der Tabelle **msdyn_dualwriteruntimeconfig**, nachdem Sie die Datenbank wiederhergestellt haben. Weitere Informationen finden Sie unter [Umgebungen für duales Schreiben trennen und erneut verknüpfen](relink-environments.md).

## <a name="live-synchronization-issues-that-are-caused-by-incorrect-query-filter-syntax-on-the-dual-write-maps"></a>Live-Synchronisierungsprobleme, die durch falsche Abfragefiltersyntax für die Zuordnungen für duales Schreiben verursacht werden

Auch wenn der Abfrageausdruck für einen Zuordnungsfilter für duales Schreiben syntaktisch korrekt ist, funktioniert er möglicherweise nicht wie erwartet. Der Filterausdruck befindet sich in einer Entität, nicht in einer einzelnen Datenquelle eines Abfrageobjekts. Daher gibt die generierte SQL-Abfrage nicht die erwarteten Ergebnisse zurück.

Hier ist ein Beispiel.

```dos
Query entity = PROJECTENTITY
Query expression = (ParentProject == "")
```

Möglicherweise erwarten Sie, dass Projekte ohne übergeordnetes Element herausgefiltert werden. Der Filter funktioniert jedoch nicht, da er in eine Abfrage übersetzt wird, die dem folgenden Beispiel ähnelt.

```sql
SELECT T1.RECID,T1.MODIFIEDDATETIME,T1.RECVERSION,T1.RECID,T1.DIMENSION,
T1.LOCATION,T1.PROJECTCONTROLLER,T1.PROJECTID,T1.PROJECTMANAGER,T1.REFERENCE,
T1.SALESMANAGER,T1.SCHEDULED,T1.RECVERSION#8,T1.RECVERSION#7,
T1.RECVERSION#6,T1.RECVERSION#5,T1.RECVERSION#4,T1.RECVERSION#3,
T1.RECVERSION#2,T1.RECID#8,T1.RECID#7,T1.RECID#6,T1.RECID#5,
T1.RECID#4,T1.RECID#3,T1.RECID#2,T1.PARTITION FROM PROJECTENTITY T1 
WHERE(((((((((((PARTITION=5637144576) AND (DATAAREAID=N'usmf')) AND 
((PARTITION#2=5637144576) OR (PARTITION#2 IS NULL))) AND 
((PARTITION#3=5637144576) OR (PARTITION#3 IS NULL))) AND 
((PARTITION#4=5637144576) OR (PARTITION#4 IS NULL))) AND 
((PARTITION#5=5637144576) OR (PARTITION#5 IS NULL))) AND 
((PARTITION#6=5637144576) OR (PARTITION#6 IS NULL))) AND 
((PARTITION#7=5637144576) OR (PARTITION#7 IS NULL))) AND 
((PARTITION#8=5637144576) OR (PARTITION#8 IS NULL))) AND 
((DATAAREAID#8=N'usmf') OR (DATAAREAID#8 IS NULL))) AND 
(PARENTPROJECT='')) 
ORDER BY T1.PROJECTID
```

Das eigentliche Ergebnis ist, dass das Feld `parentProject` mit `null` ausgewertet wird. `null` ist jedoch nicht mit der leeren Zeichenfolge identisch. Aufgrund dieser Nichtübereinstimmung gibt der Abfragefilter keine gültigen Ergebnisse zurück.

Führen Sie folgende Schritte aus, um das Problem zu beheben.

1. Fügen Sie eine berechnete Spalte hinzu, die in einem Erweiterungsmodell hinzugefügt werden kann und die von einer Logik unterstützt wird, die `null` in die leere Zeichenfolge konvertiert.

    ```dos
    SysComputedColumn::if(SysComputedColumn::isNullExpression(ParentProject), SysComputedColumn::returnLiteral(""), fieldName);
    ```

2. Wenden Sie den Filter auf die neue berechnete Spalte an und nicht auf die Standardspalte.

Um den Filter in einer Entwicklungsumgebung auszuwerten, können Sie den folgenden X++-Code verwenden, um die Ergebnisse zu überprüfen. Führen Sie diesen Code als eigenständiges Programm aus. Sie können damit verschiedene Arten von Filtern auswerten, die für eine Entität anwendbar sind, bevor Sie diese Filter auf Zuordnungen für duales Schreiben anwenden. Die Abfrage kann für die Datenbank ausgeführt werden, um Abweichungen auszuwerten.

```xpp
var entityName = "PROJECTENTITY";
var filterExpression = '(ParentProject == "")';
Query query = new Query();
query.literals(NoYes::Yes); 
QueryBuildDataSource qbd = query.addDataSource(tablename2id(entityName));
qbd.addRange(fieldname2id(qbd.table(),identifierStr(RecVersion))).value(filterExpression);
qbd.addSelectionField(fieldname2id(qbd.table(),identifierStr(RecId)));
QueryRun qRun = new QueryRun(query);
// This provides the actual sql statement to execute
var actualSqlStatement = query.getSQLStatement();
while(qRun.next())
{
    var rec = qRun.get(tableName2Id(entityName));
}
```

## <a name="data-from-finance-and-operations-apps-isnt-synced-to-dataverse"></a>Daten aus Finanz- und Betriebs-Apps werden nicht mit Dataverse synchronisiert

Bei der Live-Synchronisierung kann es vorkommen, dass nur ein Teil der Daten aus den Finanz- und Betriebs-Apps mit Dataverse synchronisiert wird oder dass die Daten überhaupt nicht synchronisiert werden.

> [!NOTE]
> Sie müssen dieses Problem während der Entwicklung beheben.

Bevor Sie mit der Behebung des Problems beginnen, überprüfen Sie die folgenden Voraussetzungen:

+ Stellen Sie sicher, dass Ihre benutzerdefinierten Änderungen in einem einzigen Transaktionsbereich geschrieben werden.
+ Geschäftsereignisse und das Framework für duales Schreiben können die Vorgänge `doinsert()`, `doUpdate()` und `recordset()` oder Datensätze, bei denen `skipBusinessEvents(true)` markiert ist, nicht verarbeiten. Wenn sich Ihr Code in diesen Funktionen befindet, wird das duale Schreiben nicht ausgelöst.
+ Geschäftsereignisse müssen für die zugeordnete Datenquelle registriert werden. Einige Datenquellen verwenden möglicherweise eine äußere Verknüpfung und können in Finanz- und Betriebs-Apps als schreibgeschützt gekennzeichnet sein. Diese Datenquellen werden nicht nachverfolgt.
+ Änderungen werden nur ausgelöst, wenn die Änderungen die zugeordneten Felder betreffen. Änderungen an nicht zugeordneten Feldern lösen kein duales Schreiben aus.
+ Stellen Sie sicher, dass Filterauswertungen ein gültiges Ergebnis liefern.

### <a name="troubleshooting-steps"></a>Schritte zur Problembehandlung

1. Überprüfen Sie die Feldzuordnungen auf der Administratorseite für duales Schreiben. Wenn ein Feld in den Finanz- und Betriebs-Apps nicht auf Dataverse zugeordnet ist, wird es nicht verfolgt. In der folgenden Abbildung zum Beispiel wird das Feld **Beschreibung** von Dataverse aus verfolgt, aber nicht von den Apps Finanzen und Betrieb. Änderungen an diesem Feld innerhalb der Finanz- und Betriebs-Apps werden nicht nachverfolgt.

    ![Verfolgtes Feld.](media/live-sync-troubleshooting-1.png)

2. Bestimmen Sie, ob die Datenquelle in der Geschäftsereignisdefinition verfolgt wird. In der folgenden Abbildung beispielsweise wird kein Feld aus der Tabelle **DefaultDimensionDAVs** und zugrunde liegende Tabellen auf Änderungen verfolgt. Datenquellen, die eine äußere Verknüpfung verwenden und als schreibgeschützt markiert sind, werden nicht verfolgt.

    ![Feld, das nicht verfolgt wird.](media/live-sync-troubleshooting-2.png)

3. Bestimmen Sie, ob die zugeordneten Tabellenfelder in der Tabelle **BUSINESSEVENTSDEFINITION** angezeigt werden, wie in der folgenden Abbildung gezeigt. Wenn Sie das gesuchte Feld im Abfrageergebnis nicht finden, wird es nicht durch duales Schreiben ausgelöst.

    ![Verfolgtes Feld in der Tabelle.](media/live-sync-troubleshooting-3.png)

### <a name="sample-scenario"></a>Beispielszenario

In Finanz- und Betriebs-Apps wird die Adresse eines Datensatzes aktualisiert, aber die Adressänderung wird nicht mit Dataverse synchronisiert. Dieses Szenario tritt auf, weil kein Datensatz in der Tabelle **BusinessEventsDefinition** über die Kombination aus der betroffenen Tabelle und der Entität verfügt. Insbesondere die Tabelle **LogisticsPostalAddress** ist nicht die direkte Datenquelle für die Entität **smmContactpersonCDSV**. Die Entität **smmContactpersonCDSV2Entity** verwendet **smmContactPersonV2Entity** als Datenquelle, wohingegen **smmContactPersonV2Entity** die Datenquelle **LogisticsPostalAddressBaseEntity** verwendet. Die Tabelle **LogisticsPostalAddress** ist die Datenquelle für **LogisticsPostalAddressBaseEntity**.

Eine ähnliche Situation kann bei einigen nicht standardisierten Mustern auftreten, z.B. in Fällen, in denen die Tabelle, die in Finanz- und Betriebs-Apps geändert wird, nicht offensichtlich mit der Entität verknüpft ist, die sie enthält. Zum Beispiel werden die primären Adressdaten auf der Entität **smmKontaktPersonCDSV2Entity** berechnet. Das Framework für duales Schreiben versucht zu bestimmen, wie eine Änderung an einer zugrunde liegenden Tabelle zurück auf Entitäten abzubilden ist. Normalerweise ist dieser Ansatz ausreichend. In einigen Fällen ist der Link jedoch so komplex, dass Sie spezifisch sein müssen. Sie müssen sicherstellen, dass die **RecId** der verknüpften Tabelle direkt auf der Entität verfügbar ist. Fügen Sie dann eine statische Methode hinzu, um die Tabelle auf Änderungen zu überwachen.

Sehen Sie sich als Beispiel die Methode **smmContactPersonCDSV2Entity::getEntityDataSourceToFieldMapping()** an. **CustCustomerV3entity** und **VendVendorV2Entity** wurden geändert, um diese Situation zu lösen.

Führen Sie folgende Schritte aus, um das Problem zu beheben.

1. Fügen Sie ein Feld **PrimaryPostalAddressRecId** zur Entität **smmContactPersonV2Entity** hinzu. Machen Sie es zu einem internen Feld.

    ![Feld, das zur Entität „smmContactPersonV2Entity“ hinzugefügt wurde.](media/Troubleshoot_live_sync_issue_1.png)

2. Fügen Sie dasselbe Feld zur Entität **smmContactPersonCDSV2Entity** hinzu.

    ![Feld, das zur Entität „smmContactPersonCDSV2Entity“ hinzugefügt wurde.](media/Troubleshoot_live_sync_issue_2.png)

3. Fügen Sie die folgende Methode zur Klasse **smmContactPersonCDSV2Entity** hinzu.

    ```xpp
    public static container getEntityDataSourceToFieldMapping(container mapping)
    {
        mapping += [[tablestr(smmContactPersonCDSV2Entity), tablenum(LogisticsPostalAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryPostalAddressRecId)]];
        return mapping;
    }
    ```

4. Synchronisieren Sie die Datenbank und erstellen Sie die Anwendung.
5. Stoppen Sie alle Zuordnungen für duales Schreiben, die auf der Entität **smmContactPersonCDSV2Entity** erstellt werden.
6. Starten Sie die Zuordnung. Sie sollten die neue Tabelle (in diesem Beispiel **LogisticsPostalAddress**) sehen, für die Sie die Verfolgung begonnen haben, indem Sie die Spalte **RefTableName** für die Zeile verwenden, in der der Wert **refentityname** gleich **smmContactPersonCDSV2Entity** in der Tabelle **BusinessEventsDefinition** ist.

## <a name="error-when-you-create-a-record-where-multiple-records-are-sent-from-a-finance-and-operations-app-to-dataverse-in-the-same-batch"></a>Fehler beim Erstellen eines Datensatzes, bei dem mehrere Datensätze von einer Finanz- und Betriebs-App an Dataverse im selben Batch gesendet werden

Für jede Transaktion erstellt eine Finanz- und Betriebs-App Daten in einem Batch und sendet sie als Batch an Dataverse. Wenn zwei Datensätze als Teil derselben Transaktion erstellt werden und sich gegenseitig referenzieren, erhalten Sie in der Finanz- und Betriebs-App möglicherweise eine Fehlermeldung, die dem folgenden Beispiel ähnelt:

*Daten können nicht in die Entität aaa_fundingsources geschrieben werden. ebecsfs_contracts mit Werten {PC00...} können nicht gesucht werden. aaa_fundingsources mit Werten {PC00...} können nicht gesucht werden. Schreibvorgänge in aaa_fundingsources schlugen mit Ausnahme-Fehlermeldung fehl: Der Remote-Server hat einen Fehler zurückgegeben: (400) Bad Request.*

Um das Problem zu beheben, erstellen Sie Entitätsbeziehungen in der Finanz- und Betriebs-App, um anzuzeigen, dass die beiden Entitäten miteinander in Beziehung stehen und dass die zugehörigen Datensätze in derselben Transaktion behandelt werden.

## <a name="enable-verbose-logging-of-error-messages"></a>Ausführliche Protokollierung von Fehlermeldungen aktivieren

In einer Finanz- und Betriebs-App könnten Sie auf Fehler stoßen, die mit der Umgebung Dataverse zusammenhängen. Die Fehlermeldung enthält möglicherweise nicht den vollständigen Text der Meldung oder andere relevante Daten. Um weitere Informationen zu erhalten, können Sie die ausführliche Protokollierung aktivieren, indem Sie das Flag **IsDebugMode** setzen, das auf der Entität **DualWriteProjectConfigurationEntity** in allen Projektkonfigurationen in Finanz- und Betriebs-Apps vorhanden ist.

1. Öffnen Sie die Entität **DualWriteProjectConfigurationEntity** mithilfe des Excel-Add-Ins. Um das Add-in zu verwenden, aktivieren Sie den Entwurfsmodus im Excel-Add-in für Finanzen und Betrieb und fügen Sie **DualWriteProjectConfigurationEntity** zu einem Arbeitsblatt hinzu. Weitere Informationen finden Sie unter [Entitätsdaten mit Excel anzeigen und aktualisieren](../../office-integration/use-excel-add-in.md).
2. Legen Sie die Markierung **IsDebugMode** für das Projekt auf **Ja** fest.
3. Führen Sie das Szenario aus.
4. Die ausführlichen Protokolle sind in der Tabelle **DualWriteErrorLog** verfügbar. Um mithilfe des Tabellenbrowsers nach Daten zu suchen, verwenden Sie die folgende URL: `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog`.
5. Um weitere Protokolle im Debugmodus zu erfassen, installieren Sie das Update in [KB 4595434 (Fix für die Weitergabe von Leerwerten in der Live-Synchronisierung für duales Schreiben)](https://fix.lcs.dynamics.com/Issue/Details?kb=4595434&bugId=527820&dbType=3&qc=c29ce15a80e6b3b4c01a722d9bdae1d7e71aa3662a044cfd0b765f736cfa98e9).

## <a name="error-when-you-add-an-address-for-a-customer-or-contact"></a>Fehler beim Hinzufügen einer Adresse für einen Kunden oder Kontakt

Sie erhalten möglicherweise die folgende Fehlermeldung, wenn Sie versuchen, eine Adresse für einen Debitor oder einen Kontakt in Finanz- und Betriebs-Apps oder Dataverse hinzuzufügen:

*Daten können nicht in die Entität „msdyn_partypostaladdresses“ geschrieben werden. Scheibvorgänge in „DirPartyPostalAddressLocationCDSEntity“ schlugen mit der Fehlermeldung „Anfrage fehlgeschlagen mit Statuscode BadRequest und CDS-Fehlercode: 0x80040265“ Antwortnachricht: Im Plug-In ist ein Fehler aufgetreten. Ein Datensatz mit den Attributwerten „Standort-ID“ ist bereits vorhanden. Der Entitätsschlüssel „Standort-ID-Schlüssel“ erfordert, dass dieser Satz von Attributen eindeutige Werte enthält. Wählen Sie eindeutige Werte aus und versuchen Sie es erneut.*

Um das Problem zu beheben, installieren Sie die Orchestrierungspaketversion für duales Schreiben (2.2.2.60), sodass die Schlüssel für die Tabeolle **Adress** wie in der folgenden Tabelle dargestellt definiert werden.

| Eigenschaft | Wert |
|---|---|
| Anzeigename | **Lagerplatzschlüssel** |
| Name | **msdyn_locationkey** |
| Felder | **msdyn_locationid**, **parentid** |
| Status | **Aktiv** |
| Systemeinzelvorgang | Leer |

## <a name="error-when-you-add-a-customer-in-dataverse"></a>Fehler beim Hinzufügen eines Kunden in Dataverse

Möglicherweise wird die folgende Fehlermeldung angezeigt, wenn Sie versuchen, einen Kunden in Dataverse hinzuzufügen:

*"RecordError0":"Schreibvorgang für Entität „Customers V3“ mit unbekannter Ausnahme fehlgeschlagen – Parteidatensatz für Parteityp „Organisation“ nicht gefunden"}.*

Wenn ein Kunde in Dataverse erstellt wird, wird eine neue Parteinummer generiert. Die Fehlermeldung wird angezeigt, wenn der Datensatz des Debitors zusammen mit der Partei mit den Finanz- und Betriebs-Apps synchronisiert wird, aber bereits ein Datensatz des Debitors mit einer anderen Parteinummer vorhanden ist.

Um das Problem zu beheben, suchen Sie den Kunden über die Parteisuche. Falls der Kunde nicht vorhanden ist, erstellen Sie einen neuen Kundendatensatz. Wenn der Kunde vorhanden ist, verwenden Sie die vorhandene Partei, um den neuen Kundendatensatz zu erstellen.

## <a name="error-when-you-create-a-new-customer-vendor-or-contact-in-dataverse"></a>Fehler beim Erstellen eines neuen Kunden, Lieferanten oder Kontakts in Dataverse

Möglicherweise erhalten Sie die folgende Fehlermeldung, wenn Sie versuchen, einen neuen Kunden, Lieferanten oder Kontakt in Dataverse zu erstellen:

*Der Typ einer Partei kann nicht von „DirOrganization“ zu „DirPerson“ aktualisiert werden. Stattdessen sollte die vorhandene Partei gelöscht und anschließend mit dem neuen Typ eingefügt werden.*

In Dataverse gibt es einen Nummernkreis in der Tabelle **msdyn_party**. Wenn in Dataverse ein Konto erstellt wird, eine neue Partei erstellt (zum Beispiel **Partei-001** vom Typ **Organisation**). Diese Daten werden an die Finanz- und Betriebs-App gesendet. Wenn die Dataverse-Umgebung zurückgesetzt wird oder die Finanzen und Betrieb-Umgebung mit einer anderen Dataverse-Umgebung verknüpft wird und dann ein neuer Datensatz in Dataverse erstellt wird, wird ein neuer Parteiwert erstellt, der mit **Partei-001** beginnt. Diesmal ist der erstellte Parteidatensatz **Partei-001** vom Typ **Person** Wenn diese Daten synchronisiert werden, zeigen die Finanz- und Betriebs-Apps die vorstehende Fehlermeldung an, da der Datensatz **Partei-001** des Typs **Organisation** bereits existiert.

Um das Problem zu beheben, ändern Sie den automatischen Nummernkreis für das Feld **msdyn_partynummer** in der Tabelle **msdyn_party** in Dataverse in einen anderen automatischen Nummernkreis.

## <a name="performance-issue-with-customer-or-contact-mappings"></a>Leistungsproblem mit Kunden- oder Kontaktzuordnungen

Möglicherweise können Sie die Leistung der Live-Synchronisierung für Kunden und Kontakte geringfügig verbessern, indem Sie die Methode **getEntityDataSourceToFieldMapping** (in der Entität **CustCustomerV3Entity**) und die Methode **getEntityDataSourceToFieldMapping** (in der Entität **smmContactPersonCDSV2Entity** anpassen). Diese Anpassungen reduzieren die Anzahl der Datensätze in der Tabelle **BusinessEventsDefinition**. Diese Reduzierung der Anzahl an Datensätzen reduziert wiederum die Anzahl der ausgelösten Ereignisse.

Die Methode **getEntityDataSourceToFieldMapping** in der Entität **CustCustomerV3Entity** stellt sicher, dass eine Aktualisierung der elektronischen Adresse oder Postanschrift des Kunden Geschäftsereignisse auslöst, sodass die aktualisierten Daten an Dataverse gesendet werden. Wenn Sie nicht alle Felder verwenden und die Informationen nicht für das duale Schreiben benötigen, können Sie die entsprechenden Zeilen in der Methode auskommentieren. Alle verfolgten Felder und Tabeleln, die in dieser Methode hinzugefügt werden, fügen einen Datensatz in der Tabelle **BusinessEventsDefinition** hinzu für die Kombination der verfolgten Tabelle und der verfolgten Entität.

```xpp
public static container getEntityDataSourceToFieldMapping(container mapping)
{
    mapping += [
        [tablestr(DirPartyBaseEntity), tablenum(LogisticsPostalAddress), fieldstr(CustCustomerV3Entity, AddressRecordId)],
        [identifierstr(DirPartyBaseEntity), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactURLRecordId)],
        [identifierstr(DirPartyBaseEntity1), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactPhoneRecordId)],
        [identifierstr(DirPartyBaseEntity2), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactEmailRecordId)],
        [identifierstr(DirPartyBaseEntity3), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactFaxRecordId)],
        [identifierstr(DirPartyBaseEntity4), tablenum(DirPartyLocation), fieldstr(CustCustomerV3Entity, DirPartyLocationRecordId)],
        [identifierstr(DirPartyBaseEntity5), tablenum(LogisticsPostalAddress), fieldstr(CustCustomerV3Entity, InvoiceAddressRecordId)],
        [identifierstr(DirPartyBaseEntity6), tablenum(LogisticsPostalAddress), fieldstr(CustCustomerV3Entity, DeliveryAddressRecordId)],
        [identifierStr(DirPartyBaseEntity7), tablenum(DirPartyTable), fieldstr(CustCustomerV3Entity, PartyRecordId)]];
    return mapping;
}
```

Auf ähnliche Weise stellt die Methode **getEntityDataSourceToFieldMapping** in der Entität **smmContactPersonCDSV2Entity** sicher, dass jede Aktualisierung der elektronischen Adresse oder Postanschrift des Kontakts Geschäftsereignisse auslöst, sodass die aktualisierten Daten an Dataverse gesendet werden. In der Methode können Sie die Zeilen für alle Felder auskommentieren, die Sie nicht verwenden.

```xpp
public static container getEntityDataSourceToFieldMapping(container mapping)
{
    mapping += [
        [tablestr(DirPartyBaseEntity), tablenum(LogisticsPostalAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryPostalAddressRecId)],
        [identifierStr(DirPartyBaseEntity), tablenum(DirPartyTable), fieldstr(smmContactPersonCDSV2Entity, PrimaryAddressLocation)],
        [identifierStr(DirPartyBaseEntity1), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactEmailRecordId)],
        [identifierStr(DirPartyBaseEntity2), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactFaxRecordId)],
        [identifierStr(DirPartyBaseEntity3), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactPhoneRecordId)],
        [identifierStr(DirPartyBaseEntity4), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactFacebookRecordId)],
        [identifierStr(DirPartyBaseEntity5), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactTwitterRecordId)],
        [identifierStr(DirPartyBaseEntity6), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactURLRecordId)],
        [identifierStr(DirPartyBaseEntity7), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactLinkedInRecordId)],
        [identifierStr(DirPartyBaseEntity8), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactTelexRecordId)],
        [identifierStr(DirPartyBaseEntity9), tablenum(DirPartyTable), fieldstr(smmContactPersonCDSV2Entity, PartyRecordId)]];
    return mapping;
}
```

Gehen Sie folgendermaßen vor, nachdem Sie die Methoden aktualisiert haben.

1. Synchronisieren Sie die Datenbank und erstellen Sie die Anwendung.
2. Stoppen Sie alle Zuordnungen für duales Schreiben auf den Entitäten **smmContactPersonCDSV2Entity** und **CustCustomerV3Entity**.
3. Starten Sie die Zuordnungen. In den Entitäten **smmContactPersonCDSV2Entity** und **CustCustomerV3Entity** sowie in der Tabelle **BusinessEventsDefinition** sollten weniger Datensätze angezeigt werden und die Leistung hat sich möglicherweise geringfügig verbessert.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

