---
title: Probleme bei Aktualisierungen von Finance and Operations-Apps beheben
description: Dieses Thema enthält Informationen zur Fehlerbehebung, mit denen Sie Probleme beheben können, die mit dem Upgrade von Finance and Operations Apps zusammenhängen.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 97509ac662fad6181cbd60e5e0a44f674410acb9
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754037"
---
# <a name="troubleshoot-issues-from-upgrades-of-finance-and-operations-apps"></a>Probleme bei Aktualisierungen von Finance and Operations-Apps beheben

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Dieses Thema enthält Problembehandlungsinformationen zur dualen Schreibintegration zwischen den Apps Finance and Operations und Dataverse. Dieses Thema enthält speziell Informationen zur Fehlerbehebung, mit denen Sie Probleme beheben können, die mit dem Upgrade von Finance and Operations Apps zusammenhängen.

> [!IMPORTANT]
> Einige der in diesem Thema behandelten Probleme erfordern möglicherweise entweder die Systemadministratorrolle oder Microsoft Azure Active Directory (Azure AD) Anmeldeinformationen des Mandantenadministrators. Im Abschnitt zu jedem Problem wird erläutert, ob eine bestimmte Rolle oder Anmeldeinformationen erforderlich sind.

## <a name="database-synchronization-errors"></a>Datenbanksynchronisierungsfehler

**Erforderliche Rolle zum Beheben der Fehler:** System Administrator

Möglicherweise erhalten Sie eine Fehlermeldung, die dem folgenden Beispiel ähnelt, wenn Sie versuchen, die Tabelle **DualWriteProjectConfiguration** zu verwenden, um eine Finance and Operations-App auf Plattform Update 30 zu aktualisieren.

```console
Infolog diagnostic message: 'Cannot select a row in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

Führen Sie folgende Schritte aus, um das Problem zu beheben.

1. Melden Sie sich bei der virtuellen Maschine (VM) für die Finance and Operations App an.
2. Öffnen von Visual Studio als Administrator und öffnen Sie den Application Object Tree (AOT).
3. Suchen nach **DualWriteProjectConfiguration**.
4. Klicken Sie im AOT mit der rechten Maustaste auf **DualWriteProjectConfiguration** und wählen Sie **Zu neuem Projekt hinzufügen**. Wählen Sie **OK**, um das neue Projekt zu erstellen, das Standardoptionen verwendet.
5. Klicken Sie im Projektmappen-Explorer mit der rechten Maustaste auf **Projekteigenschaften** und setzen Sie **Datenbank beim Erstellen synchronisieren** auf **Wahr** fest.
6. Erstellen Sie das Projekt und bestätigen Sie, dass der Build erfolgreich ist.
7. Auf dem **Dynamics 365** Menü wählen Sie **Datenbank synchronisieren**.
8. Wählen Sie **Synchronisieren**, um eine vollständige Datenbanksynchronisation durchzuführen.
9. Nachdem die vollständige Datenbanksynchronisierung erfolgreich war, führen Sie den Schritt zur Datenbanksynchronisierung erneut aus in Microsoft Dynamics Lifecycle Services (LCS) und verwenden Sie gegebenenfalls die manuellen Upgrade-Skripte, damit Sie mit dem Update fortfahren können.

## <a name="missing-table-columns-issue-on-maps"></a>Fehlende Tabellenspalten in Zuordnungen

**Erforderliche Rolle zum Beheben der Fehler:** System Administrator

Auf der Seite **Duales Schreiben** wird möglicherweise eine Fehlermeldung angezeigt, die dem folgenden Beispiel ähnelt:

*Fehlendes Quellfeld \<field name\> im Schema.*

![Beispiel für die Fehlermeldung zu fehlenden Quellspalten](media/error_missing_field.png)

Führen Sie die folgenden Schritte aus, um das Problem zu beheben und sicherzustellen, dass sich die Spalten in der Tabelle befinden.

1. Melden Sie sich bei der virtuellen Maschine (VM) an für die Finance and Operations App.
2. Wechseln Sie zu **Arbeitsbereiche \> Datenverwaltung**, wählen Sie die Kachel **Framework-Parameter** aus, und wählen Sie dann auf der Registerkarte **Tabelleneinstellungen** die Option **Tabellenliste aktualisieren** aus, um die Tabellen zu aktualisieren.
3. Wechseln Sie zu **Arbeitsbereiche \> Datenverwaltung**, wählen Sie die Registerkarte **Datentabellen** aus und stellen Sie sicher, dass die Tabelle aufgelistet ist. Wenn die Tabelle nicht aufgeführt ist, melden Sie sich bei der VM für die Finance and Operations-App an, und stellen Sie sicher, dass die Tabelle verfügbar ist.
4. Öffnen Sie die Seite **Tabellenzuordnung** über die Seite **Duales Schreiben** in der Finance and Operations-App.
5. Wählen Sie **Tabellenliste aktualisieren** aus, um die Spalten in den Tabellenzuordnungen automatisch auszufüllen.

Wenn das Problem immer noch nicht behoben ist, führen Sie die folgenden Schritte aus.

> [!IMPORTANT]
> Diese Schritte führen Sie durch den Vorgang des Löschens und anschließenden Hinzufügens einer Tabelle. Befolgen Sie die Schritte genau, um Probleme zu vermeiden.

1. Gehen Sie in der Finance and Operations-App zu **Arbeitsbereiche \> Datenmanagement** und wählen Sie die Kachel **Datentabellen** aus.
2. Suchen Sie die Tabelle, der das Attribut fehlt. Klicken Sie in der Symbolleiste auf **Zielzuordnung ändern**.
3. Klicken Sie im Bereich **Abbildung auf Ziel** auf **Zuordnung generieren**.
4. Öffnen Sie die Seite **Tabellenzuordnung** über die Seite **Duales Schreiben** in der Finance and Operations-App.
5. Wenn das Attribut nicht automatisch in die Zuordnung eingefügt wird, fügen Sie es manuell hinzu, indem Sie auf **Attribut hinzufügen** und dann auf **Speichern** klicken. 
6. Wählen Sie die Zuordnung aus, und klicken Sie auf **Ausführen**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]