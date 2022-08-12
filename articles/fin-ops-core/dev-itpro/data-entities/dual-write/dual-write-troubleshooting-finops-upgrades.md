---
title: Problembehandlung von Problemen bei Upgrades von Finanz- und Betriebs-Apps
description: Dieser Artikel enthält Informationen zur Problembehandlung, die Ihnen helfen können, Probleme im Zusammenhang mit Upgrades von Finanz- und Betriebs-Apps zu beheben.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: b75034cbc8ca7a24472cfec1ad93d3dfef4a8fdc
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111139"
---
# <a name="troubleshoot-issues-from-upgrades-of-finance-and-operations-apps"></a>Problembehandlung von Problemen bei Upgrades von Finanz- und Betriebs-Apps

[!include [banner](../../includes/banner.md)]





Dieser Artikel enthält Informationen zur Problembehandlung für die Dual-write Integration zwischen Finanz- und Betriebs-Apps und Dataverse. Insbesondere erhalten Sie Informationen, die Ihnen helfen können, Probleme zu beheben, die mit Upgrades von Finanz- und Betriebs-Apps zusammenhängen.

> [!IMPORTANT]
> Einige der in diesem Artikel behandelten Probleme erfordern möglicherweise entweder die Systemadministratorrolle oder Microsoft Azure Active Directory (Azure AD)-Anmeldeinformationen des Mandantenadministrators. Im Abschnitt zu jedem Problem wird erläutert, ob eine bestimmte Rolle oder Anmeldeinformationen erforderlich sind.

## <a name="database-synchronization-errors"></a>Datenbanksynchronisierungsfehler

**Erforderliche Rolle zum Beheben der Fehler:** System Administrator

Sie könnten eine Fehlermeldung erhalten, die dem folgenden Beispiel ähnelt, wenn Sie versuchen, die Tabelle **DualWriteProjectConfiguration** zu verwenden, um eine Finanz- und Betriebs-App auf Platform update 30 zu aktualisieren.

```console
Infolog diagnostic message: 'Cannot select a row in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

Führen Sie folgende Schritte aus, um das Problem zu beheben.

1. Melden Sie sich bei der virtuellen Maschine (VM) für die Finanz- und Betriebs-App an.
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

![Beispiel für die Fehlermeldung zu fehlenden Quellspalten.](media/error_missing_field.png)

Führen Sie die folgenden Schritte aus, um das Problem zu beheben und sicherzustellen, dass sich die Spalten in der Tabelle befinden.

1. Melden Sie sich bei der VM für die Finanz- und Betriebs-App an.
2. Wechseln Sie zu **Arbeitsbereiche \> Datenverwaltung**, wählen Sie die Kachel **Framework-Parameter** aus, und wählen Sie dann auf der Registerkarte **Tabelleneinstellungen** die Option **Tabellenliste aktualisieren** aus, um die Tabellen zu aktualisieren.
3. Wechseln Sie zu **Arbeitsbereiche \> Datenverwaltung**, wählen Sie die Registerkarte **Datentabellen** aus und stellen Sie sicher, dass die Tabelle aufgelistet ist. Wenn die Tabelle nicht aufgeführt ist, melden Sie sich bei der VM für die Finanz- und Betriebs-App an und stellen Sie sicher, dass die Tabelle verfügbar ist.
4. Öffnen Sie die Seite **Tabelle Zuordnung** von der Seite **Dual-write** in der Finanz- und Betriebs-App.
5. Wählen Sie **Tabellenliste aktualisieren** aus, um die Spalten in den Tabellenzuordnungen automatisch auszufüllen.

Wenn das Problem immer noch nicht behoben ist, führen Sie die folgenden Schritte aus.

> [!IMPORTANT]
> Diese Schritte führen Sie durch den Vorgang des Löschens und anschließenden Hinzufügens einer Tabelle. Befolgen Sie die Schritte genau, um Probleme zu vermeiden.

1. Gehen Sie in der Finanz- und Betriebs-App auf **Arbeitsbereiche \> Datenmanagement** und wählen Sie die Kachel **Datentabellen**.
2. Suchen Sie die Tabelle, der das Attribut fehlt. Klicken Sie in der Symbolleiste auf **Zielzuordnung ändern**.
3. Klicken Sie im Bereich **Abbildung auf Ziel** auf **Zuordnung generieren**.
4. Öffnen Sie die Seite **Tabelle Zuordnung** von der Seite **Dual-write** in der Finanz- und Betriebs-App.
5. Wenn das Attribut nicht automatisch in die Zuordnung eingefügt wird, fügen Sie es manuell hinzu, indem Sie auf **Attribut hinzufügen** und dann auf **Speichern** klicken. 
6. Wählen Sie die Zuordnung aus, und klicken Sie auf **Ausführen**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
