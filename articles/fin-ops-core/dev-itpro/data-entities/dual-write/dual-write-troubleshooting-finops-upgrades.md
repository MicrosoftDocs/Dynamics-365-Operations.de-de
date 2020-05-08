---
title: Probleme bezüglich Aktualisierungen von Finance and Operations Apps beheben
description: Dieses Thema enthält Informationen zur Fehlerbehebung, mit denen Sie Probleme beheben können, die mit dem Upgrade von Finance and Operations Apps zusammenhängen.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 53df00de82b101aa02160d865a9c3bbebcfcae15
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275463"
---
# <a name="troubleshoot-issues-related-to-upgrades-of-finance-and-operations-apps"></a>Probleme bezüglich Aktualisierungen von Finance and Operations Apps beheben

[!include [banner](../../includes/banner.md)]



Dieses Thema enthält Problembehandlungsinformationen zur dualen Schreibintegration zwischen den Apps Finance and Operations und Common Data Service. Dieses Thema enthält speziell Informationen zur Fehlerbehebung, mit denen Sie Probleme beheben können, die mit dem Upgrade von Finance and Operations Apps zusammenhängen.

> [!IMPORTANT]
> Einige der in diesem Thema behandelten Probleme erfordern möglicherweise entweder die Systemadministratorrolle oder Microsoft Azure Active Directory (Azure AD) Anmeldeinformationen des Mandantenadministrators. Im Abschnitt zu jedem Problem wird erläutert, ob eine bestimmte Rolle oder Anmeldeinformationen erforderlich sind.

## <a name="database-synchronization-errors"></a>Datenbanksynchronisierungsfehler

**Erforderliche Rolle zum Beheben der Fehler:** System Administrator

Möglicherweise erhalten Sie eine Fehlermeldung, die dem folgenden Beispiel ähnelt, wenn Sie versuchen, die **DualWriteProjectConfiguration** Entität zu verwenden, um eine Finance and Operations App auf Plattform Update 30 zu aktualisieren.

```console
Infolog diagnostic message: 'Cannot select a record in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
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

## <a name="missing-entity-fields-issue-on-maps"></a>Fehlende Entitätsfelder treten auf Zuordnungen auf

**Erforderliche Rolle zum Beheben der Fehler:** System Administrator

Auf der Seite **Duales Schreiben** wird möglicherweise eine Fehlermeldung angezeigt, die dem folgenden Beispiel ähnelt:

*Fehlendes Quellfeld \<Feldname\> im Schema.*

![Beispiel für die fehlende Quellfeldfehlermeldung](media/error_missing_field.png)

Führen Sie die folgenden Schritte aus, um das Problem zu beheben und sicherzustellen, dass sich die Felder in der Entität befinden.

1. Melden Sie sich bei der virtuellen Maschine (VM) an für die Finance and Operations App.
2. Gehen Sie zu **Arbeitsbereiche \> Datenmanagement** und wählen Sie die Kachel **Framework-Parameter** und wählen dann auf der **Entitätseinstellungen** Registerkarte **Entitätsliste aktualisieren**, um die Entitäten zu aktualisieren.
3. Gehen Sie zu **Arbeitsbereiche \> Datenmanagement**, wählen Sie die Registerkarte **Datenentitäten** und stellen Sie sicher, dass die Entität aufgelistet ist. Wenn die Entität nicht aufgeführt ist, melden Sie sich bei der VM für die Finance and Operations App an und stellen Sie sicher, dass die Entität verfügbar ist.
4. Öffnen Sie die Seite **Entitätszuordnung** von der Seite **Duales Schreiben** in der Finance and Operations App.
5. Wählen Sei **Entitätsliste aktualisieren**, um die Felder in den Entitätszuordnungen automatisch auszufüllen.

Wenn das Problem immer noch nicht behoben ist, führen Sie die folgenden Schritte aus.

> [!IMPORTANT]
> Diese Schritte führen Sie durch den Vorgang des Löschens und anschließenden Hinzufügens einer Entität. Befolgen Sie die Schritte genau, um Probleme zu vermeiden.

1. In der Finance and Operations App, gehen Sie zu **Arbeitsbereiche \> Datenmanagement** und wählen Sie die Kachel **Datenentitäten**.
2. Suchen Sie die Entität, der das Attribut fehlt. Klicken Sie in der Symbolleiste auf **Zielzuordnung ändern**.
3. Klicken Sie im Bereich **Abbildung auf Ziel** auf **Zuordnung generieren**.
4. Öffnen Sie die Seite **Entitätszuordnung** von der Seite **Duales Schreiben** in der Finance and Operations App.
5. Wenn das Attribut nicht automatisch in die Zuordnung eingefügt wird, fügen Sie es manuell hinzu, indem Sie auf **Attribut hinzufügen** und dann auf **Speichern** klicken. 
6. Wählen Sie die Zuordnung aus, und klicken Sie auf **Ausführen**.
