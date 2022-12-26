---
title: Dynamics 365 Human Resources Kundenmigration auf die Finanzen und Betriebsinfrastruktur
description: Dieser Artikel beschreibt die Kundenmigration von Microsoft Dynamics 365 Human Resources auf die Finanz- und Betriebsinfrastruktur.
author: twheeloc
ms.date: 12/06/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ab9680c2d1caa08c15aed325f4153aac6eae63c3
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831719"
---
# <a name="dynamics-365-human-resources-customer-migration"></a>Dynamics 365 Human Resources Kundenmigration

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]
[!include [preview banner](../includes/preview-banner.md)]

Die Kundenmigration ist eine Migration per Lift und Shift (verschieben) einer Kundendatenbank in die Finanz- und Betriebsinfrastruktur. Dafür werden automatisierte Migrationstools verwendet. Das Ergebnis ist eine neue Finanz- und Betriebsumgebung, die die Human Resources-Datenbank des Debitors verwendet.

## <a name="prerequisites"></a>Voraussetzungen

### <a name="user-access-and-permissions"></a>Benutzerzugriff und -berechtigungen

- Der Microsoft Dynamics Lifecycle Services Benutzer sollte die Rolle **Organisationsadministrator** haben.
- Der Benutzer sollte in der Lage sein, [Azure DevOps-Projekte zu erstellen](/azure/devops/organizations/projects/create-project) oder ein vorhandenes Azure DevOps-Projekt zu verwenden.
- Der Benutzer sollte Zugriff auf die [Erstellung eines Azure DevOps Sicherheitstokens für den persönlichen Zugriff](/azure/devops/organizations/accounts/use-personal-access-tokens-to-authenticate) haben oder ihm sollte ein Token zur Verwendung zur Verfügung stehen.

### <a name="dataverse-environment-backup-sandbox"></a>Dataverse-Umgebungsbackup (Sandbox)

 - Optional, aber empfohlen: Aktualisieren Sie die vorhandene Human Resources-Sandbox-Umgebung mithilfe einer Kopie der Human Resources-Produktionsumgebung.
 - Erstellen Sie eine neue Dataverse Umgebung mit dem Power Platform Admin Center.
 - Kopieren Sie die vorhandene Dataverse-Umgebung, die mit der eigenständigen Human Resources-App verknüpft ist, in die Umgebung, die Sie im vorherigen Schritt erstellt haben.

> [!NOTE]
> Stellen Sie beim Hinzufügen einer Datenbank sicher, dass die Option **Dynamics 365-Apps aktivieren** auf **Ja** gestellt ist. Ausführliche Informationen finden Sie unter [Vorbereiten einer Power Platform Umgebung](hr-cust-migration.md#prepare-a-power-platform-environment).

### <a name="dataverse-capacity"></a>Dataverse-Kapazität

1. Verwenden Sie die Seite **Zusammenfassung** im Power Platform Admin Center, um zu überprüfen, ob der [Dataverse-Speicher](/power-platform/admin/finance-operations-storage-capacity) über genügend freie Kapazität für die Umgebungskopie verfügt.
2. Wenn die verfügbare Kapazität nicht ausreicht, verwenden Sie die [Anleitung zum Freigeben von Speicherplatz](/power-platform/admin/free-storage-space), um den Gesamtverbrauch zu reduzieren. Kunden können auch [zusätzliche Speicherkapazität hinzufügen](/power-platform/admin/add-storage).

## <a name="customer-migration-process"></a>Kundenmigrationsprozess

### <a name="create-a-lifecycle-services-project-for-human-resources-migration"></a>Ein Lifecycle Services-Projekt für die Human Resources-Migration erstellen

Im ersten Schritt erstellen Sie ein neues Finanz- und Betriebsimplementierungsprojekt in Lifecycle Services. Der Kunde verfügt über ein bestehendes Human Resources Lifecycle Services-Projekt. Die vorhandenen Human Resources-Umgebungen werden in das neue Finanz- und Betriebsimplementierungsprojekt migriert.

Gehen Sie folgendermaßen vor, um ein neues Projekt zu erstellen.

1. Melden Sie sich bei Lifecycle Services als globaler Administrator oder als designierter Dienstkontobenutzer an.
2. Wählen Sie auf der Startseite von Lifecycle Services **Erstellen/neu (+)** aus.
3. Wählen Sie als Produkt Finanz- und Betriebs-Apps aus.
4. Wählen Sie im Feld **Projektzweck** die Option **Implementierung** aus.
5. Geben Sie einen Projektnamen und eine Beschreibung ein.
6. Wählen Sie im Feld **Benutzerdefinierter Projekttyp** **Microsoft Dynamics 365 Human Resources Migration** aus.
7. Aktivieren Sie das Kontrollkästchen, um den allgemeinen Geschäftsbedingungen zuzustimmen
8. Wählen Sie **Erstellen** aus.

Nachdem Sie ein neues Lifecycle Services-Projekt erstellt haben, gehen Sie wie folgt vor, um das Projekt einzurichten und zu konfigurieren.

1. Wählen Sie **Projekt-Onboarding**, um das Projekt-Onboarding abzuschließen. Weitere Informationen finden Sie unter [Projekt-Einführung](../fin-ops-core/dev-itpro/lifecycle-services/project-onboarding.md).

    - Wählen Sie dieselbe Region aus, die in Ihren aktuellen Umgebungen eingestellt ist. Diese Auswahl wirkt sich nicht auf die Migration aus.
    - Wählen Sie für Legacy-Systeme **Sonstiges** aus.

2. Wählen Sie die Projekteinstellungen aus. Im Rahmen dieses Schrittes sollten Sie, falls erforderlich, die SharePoint-Online-Bibliothek, Azure DevOps und Azure-Verbindungen. Weitere Informationen finden Sie im [Benutzerhandbuch zu Lifecycle Services (LCS)](../dev-itpro/lifecycle-services/lcs-user-guide.md).

> [!NOTE]
> Kunden können ein vorhandenes Azure DevOps-Projekt und das zugehörige Sicherheitstoken für den persönlichen Zugriff verwenden. Wird ein bestehendes Projekt verwendet, sind die projektbezogenen Konfigurationen automatisch verfügbar und können auf ihre Richtigkeit überprüft werden.

### <a name="migrate-a-human-resources-sandbox-environment"></a>Eine Human Resources-Sandbox-Umgebung migrieren

#### <a name="prepare-to-migrate-the-sandbox-environment"></a>Die Migration der Sandbox-Umgebung vorbereiten

Nachdem Sie ein neues Lifecycle Services-Projekt erstellt und den Projekt-Onboarding-Prozess abgeschlossen haben, können Sie Ihre erste Umgebung migrieren. Bevor Sie diesen Prozess starten, sollten Sie die Sandbox-Umgebung aktualisieren, die Sie von Ihrer Produktionsumgebung auf die eigenständige Infrastruktur migrieren möchten.

#### <a name="prepare-a-power-platform-environment"></a>Eine Power Platform-Umgebung vorbereiten

> [!NOTE]
> Dieser Schritt gilt nur für die Migration von Sandbox-Umgebungen. Wenn Sie die Produktionsumgebung migrieren, wird die vorhandene Power Platform Admin-Center-Umgebung, die an die Produktionsumgebung angefügt ist, übernommen. Stellen Sie beim Hinzufügen einer Datenbank sicher, dass die Schaltfläche **Dynamics 365-Apps aktivieren** auf **Ja** gestellt ist. 

- Im Power Platform Admin Center [Erstellen einer Umgebung mit einer Datenbank](/power-platform/admin/create-environment#create-an-environment-with-a-database), die Sie für die Sandbox-Migration verwenden möchten, oder wählen Sie eine vorhandene Umgebung aus.
- [Kopieren Sie eine Umgebung](/power-platform/admin/copy-environment) um die Power Platform-Umgebung, die für das Mapping verwendet wird, zu aktualisieren.

#### <a name="migrate-the-sandbox-environment"></a>Die Sandbox-Umgebung migrieren

1. Melden Sie sich bei Lifecycle Services als globaler Administrator oder als designierter Dienstkontobenutzer an.

    > [!NOTE]
    > Es wird empfohlen, ein benanntes Benutzerkonto zu verwenden. Der angemeldete Benutzer sollte in dem eigenständigen Human Resources Lifecycle Services-Projekt die Sicherheitsrolle **Projektbesitzer** oder **Umgebungsmanager** haben.

2. Öffnen Sie das neu erstellte Human Resources-Migrationsprojekt.
3. Überprüfen und vervollständigen Sie die entsprechenden Phasen der Migrationsmethodik und des Projekt-Onboardings.
4. Wählen Sie auf dem Projekt-Dashboard im Bereich **Standard: Standardakzeptanztest** **HR migrieren** aus.
5. Wählen Sie in dem Bereich **Umgebung für die Migration auswählen** das entsprechende Lifecycle Services-Projekt und die ursprüngliche Human Resources-Umgebung (aus Ihrer eigenständigen Human Resources-Quellanwendung) aus.
6. Aktivieren Sie **Neuer Power Platform-Umgebung zuordnen** und wählen Sie die entsprechende Power Platform-Umgebung aus. Wählen Sie dann **Weiter** aus.
7. Vervollständigen Sie den Assistenten **Bereitstellungseinstellungen (Finanzen und Betrieb – Sandbox)**, um die Details und die Kundenabmeldung zu bestätigen, und wählen Sie dann **Bereitstellen** aus.

Der Umgebungsstatus zeigt den Fortschritt an. Der Status wird von **Wird geladen** auf **Wird bereitgestellt** auf **Bereitgestellt** geändert.

> [!NOTE]
> Der Produktionsbereich ist erst verfügbar, wenn die Checkliste für die Bereitschaft des Projekts zur Liveschaltung abgeschlossen ist. Weitere Informationen finden Sie unter [Vorbereiten auf den Start](../fin-ops-core/fin-ops/imp-lifecycle/prepare-go-live.md).

#### <a name="considerations-and-assumptions"></a>Überlegungen und Annahmen

In einem Lifecycle Services-Projekt auf dem Mandanten ist eine Human Resources-Sandbox-Umgebung mit den folgenden Merkmalen vorhanden:

- Die Human Resources-Sandbox-Umgebung ist nicht mit einer vorhandenen zusammengeführten Umgebung verknüpft. Für eine bestimmte Human Resources-Umgebung kann jeweils nur eine Migration ausgeführt werden.
- Die Anzahl der gleichzeitig zulässigen Sandbox-Umgebungen richtet sich nach der Lizenzierung der Personalabteilung. Wenn genügend Lizenzen für den Mandanten erworben wurden, werden zusätzliche Sandbox-Umgebungen im Bereich **Umgebungen** des Projekts aufgeführt.
- Migrationen müssen in Umgebungen desselben Typs durchgeführt werden. Mit anderen Worten, es können nur Migrationen von Sandbox zu Sandbox oder von Produktion zu Produktion durchgeführt werden.

    > [!NOTE]
    > Bei der Festlegung des Produktions- oder Sandbox-Status werden nur Umgebungstypen von Human Resources berücksichtigt. Wenn die Umgebungen falsch kategorisiert sind (d. h. wenn eine Produktionsumgebung als Sandbox-Umgebung oder eine Sandbox-Umgebung als Produktionsumgebung gekennzeichnet ist), wenden Sie sich an den Support.

- Wenn die Migration nicht erfolgreich ist, wird eine Fehlermeldung angezeigt und eine Schaltfläche **Löschen** wird verfügbar. Verwenden Sie diese Schaltfläche, um die fehlgeschlagene Migration zu löschen. Sie können die Umgebung dann erneut migrieren.

#### <a name="validate-the-sandbox-migration"></a>Die Sandbox-Migration überprüfen

Nachdem der Sandbox-Migrationsprozess erfolgreich abgeschlossen wurde, erstellen Sie einen detaillierten Testplan, um alle Geschäftsprozesse zu überprüfen und abzuzeichnen.

Überprüfen Sie die folgenden Details, bevor Sie mit dem Testen beginnen:

- Bestätigen Sie, dass über die generierte URL auf die migrierte Umgebung zugegriffen werden kann.
- Bestätigen Sie, dass Benutzer auf die migrierte Sandbox zugreifen können.
- Versichern Sie sich, dass die Dataverse-Umgebung, die der migrierten Sandbox-Umgebung zugeordnet ist, zugänglich ist.
- Überprüfen Sie stichprobenartig verschiedene Daten, um sicherzustellen, dass die aktuellsten Daten verfügbar sind.
- Schließen Sie die kritischen Geschäftsprozesse für die Überprüfung ab.
- Bestätigen Sie, dass Ihre Sicherheitsrichtlinien anwendbar sind.
- Bestätigen Sie, dass Stapelverarbeitungsaufträge wie erwartet ausgelöst werden.

Sie haben keinen Remotedesktopzugriff auf die migrierte Sandbox. Sie können Self-Service-Funktionen und -Tools verwenden, um für Ihre Tier-2+-Sandbox-Umgebungen die folgenden Aktionen auszuführen:

- Greifen Sie auf die [Azure SQL-Datenbank](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#access-the-azure-sql-database) zu.
- Greifen Sie auf die [Protokolldateien](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#access-log-files) zu.
- Verwenden Sie die [Perfmon-Tools](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#use-perfmon-tools).
- Schalten Sie den [Wartungsmodus ein/aus](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#access-self-service-logs).
- Starten Sie die [Dienste](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#restart-services) erneut.
- Konfigurieren Sie das [Regression Suite Automation Tool](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#configure-the-regression-suite-automation-tool).

Weitere Informationen finden Sie unter [FAQ für Self-Service-Bereitstellung](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md).

### <a name="migrate-a-human-resources-production-environment"></a>Eine Human Resources-Produktionsumgebung migrieren

Nachdem Sie die Migration und Überprüfung einer Sandbox-Umgebung abgeschlossen haben, gehen Sie wie folgt vor, um die Produktionsumgebung zu migrieren.

#### <a name="prerequisites"></a>Voraussetzungen

- Der Dauerauftragskalkulator sollte vervollständigt sein.
- Die [Bewertung der Bereitschaft](../fin-ops-core/fin-ops/imp-lifecycle/prepare-go-live.md) für die Liveschaltung sollte abgeschlossen werden.
- Der Benutzer, der die Produktionsmigration in Lifecycle Services initiiert, sollte eine Systemadministratorrolle auf der Power Platform haben. 

#### <a name="migrate-the-production-environment"></a>Die Produktionsumgebung migrieren

1. Melden Sie sich bei Lifecycle Services als globaler Administrator oder als designierter Dienstkontobenutzer an.

    > [!NOTE]
    > Es wird empfohlen, ein benanntes Benutzerkonto zu verwenden. Der angemeldete Benutzer sollte in dem Lifecycle Services-Projekt die Sicherheitsrolle **Projektbesitzer** oder **Umgebungsmanager** haben.

2. Öffnen Sie das neue Human Resources-Migrationsprojekt.
3. Überprüfen und vervollständigen Sie die entsprechenden Phasen der Migrationsmethodik und des Projekt-Onboardings.
4. Wählen Sie auf dem Projekt-Dashboard im Bereich **Produktion** **HR migrieren** aus.
5. Wählen Sie in dem Bereich **Umgebung für die Migration auswählen** das entsprechende Lifecycle Services-Projekt und die ursprüngliche Human Resources-Umgebung (aus Ihrer eigenständigen Human Resources-Quellanwendung) aus. Wählen Sie dann **Weiter** aus.
6. Vervollständigen Sie den Assistenten **Bereitstellungseinstellungen (Finanzen und Betrieb – Sandbox)**, um die Details und die Kundenabmeldung zu bestätigen, und wählen Sie dann **Bereitstellen** aus.

Der Umgebungsstatus zeigt den Fortschritt der Bereitstellung an. Der Status wird von **Wird geladen** auf **Wird bereitgestellt** auf **Bereitgestellt** geändert.

#### <a name="post-migration-considerations"></a>Überlegungen nach der Migration

- Wenden Sie die [Qualitätsupdates](/fin-ops-core/fin-ops/get-started/quality-updates) auf Ihre Umgebungen an.
- Wenn Sie [virtuelle Tabellen](hr-admin-integration-common-data-service-virtual-entities.md) verwenden, konfigurieren Sie die Endpunkte neu.
- Konfigurieren Sie die Integration für duales Schreiben erneut. Bewerten Sie, welche Entitäten aktiviert werden müssen.
- Erwägen Sie die Verwendung virtueller Tabellen, um duales Schreiben für die Integration zu ersetzen.

#### <a name="dual-write-integration"></a>Duales Schreiben – Integration

##### <a name="set-up-microsoft-power-platform-dual-write-integration"></a>Microsoft Power Platform Integration für duales Schreiben einrichten

1. Gehen Sie zum Power Platform Admin Center und wählen Sie im linken Navigationsbereich **Umgebungen** aus.
2. Wählen Sie die zuvor kopierte/aktualisierte Umgebung aus und versichern Sie sich, dass der Status **Bereit** lautet.
3. Gehen Sie zu Lifecycle Services und versichern Sie sich, dass der Status des Migrationsprojekts **Bereitgestellt** lautet.
4. Wählen Sie unter der migrierten Umgebung **Alle Details** aus, um weitere Details zu überprüfen und [richten Sie eine Anwendung für duales Schreiben ein](../fin-ops-core/dev-itpro/data-entities/dual-write/lcs-setup.md#set-up-dual-write-for-new-or-existing-dataverse-environments).
5. Wählen Sie im Bereich **Konfiguration der Anwendung für duales Schreiben** das Kontrollkästchen aus, um der Zuordnung und Synchronisierung von Daten zwischen Datenbanken zuzustimmen, und wählen Sie dann **Konfigurieren** aus.
6. Wenn eine Meldung erscheint, die bestätigt, dass die Konfiguration für duales Schreiben erfolgreich war, wählen Sie **OK**.
7. In den Details können Sie den Fortschritt der Konfiguration verfolgen.
8. Wenn die Konfiguration abgeschlossen ist, wählen Sie **Mit Power Platform-Umgebung verlinken**, um die verfügbaren Datenentitäten zu synchronisieren.
9. Wenn der Status anzeigt, dass die Umgebungen erfolgreich verknüpft wurden, gehen Sie zum Power Platform Admin Center, um die entsprechenden Datenentitäten zu überprüfen und auszuwählen.
10. Wählen Sie im linken Bereich **Dynamics 365-Apps \> Ressourcen** aus.
11. Bestätigen Sie, dass der Status der Human-Resources-App für duales Schreiben **Aktiviert** lautet.
12. Wählen Sie die Human Resources-App für duales Schreiben und dann **Installieren** aus.
13. Wählen Sie im Bereich **Dynamics 365 Human Resources App für duales Schreiben installieren** die entsprechende Umgebung aus, in der das Paket installiert werden soll.
14. Aktivieren Sie das Kontrollkästchen, um den Vertragsbedingungen zuzustimmen, und wählen Sie dann **Installieren** aus.
15. Der Status in der Dynamics 365-App-Umgebung lautet **Wird installiert**, während die Installation läuft. Wenn die Installation abgeschlossen ist, wird er auf **Installiert** aktualisiert.

##### <a name="review-and-apply-a-dual-write-solution"></a>Eine Lösung für duales Schreiben überprüfen und anwenden

1. Gehen Sie in der neuen Finanz- und Betriebsumgebung zu **Datenverwaltung \> Duales Schreiben**.
2. Wählen Sie **Lösung anwenden** aus.
3. Wählen Sie im Bereich **In Dynamics installierte Lösungen**, **Kernentitätszuordnungen für Anwendungen für duales Schreiben** und **Dynamics 365 Human Resources Zuordnungen** aus. Wählen Sie dann **Anwenden** aus. Eine Meldung bestätigt, dass die Lösung angewendet wird. Nachdem die Lösung erfolgreich angewendet wurde, werden alle verfügbaren Tabellenzuordnungen angezeigt.
4. Überprüfen Sie die verfügbaren Tabellenzuordnungen, um die Integration mithilfe von dualem Schreiben auszuwählen und auszuführen.
5. Wenn Sie die Integration von dualem Schreiben zum ersten Mal für Tabellenzuordnungen ausführen, wählen Sie das Kontrollkästchen **Erste Synchronisierung**. Wenn eine vorhandene Integration aus der Human Resources-Quellumgebung vorhanden ist, müssen Sie das Kontrollkästchen **Erste Synchronisierung** aus, wenn Sie die Integration für Tabellenzuordnungen ausführen.

#### <a name="recommended-practices"></a>Empfohlene Praktiken

Dieser Abschnitt enthält Empfehlungen für die Migration von der eigenständigen Infrastruktur zur Finanz- und Betriebsinfrastruktur.

- Wir empfehlen Ihnen dringend, mit Ihrem Microsoft Dynamics-Partner zusammenzuarbeiten, um Hilfe bei der Migration Ihrer Human Resources-Umgebung zu erhalten.
- Planen Sie ausreichend Zeit ein, um den vollständigen Benutzerfunktionstest (UAT) in der migrierten Sandbox-Umgebung durchzuführen.
- Planen und dokumentieren Sie die detaillierten Schritte zur Migration von Integrationen in die migrierte Umgebung.
- Erstellen Sie eine detaillierte Checkliste, um den Umstellungsprozess für Ihre Migration zu skizzieren.
- Planen Sie im Verlauf der Migration eine angemessene Downtime für Ihr Unternehmen ein.
- Wir empfehlen dringend, dass FastTrack-qualifizierte Kunden mit ihrem FastTrack-Lösungsarchitekten zusammenarbeiten, um Hilfe bei der Überwachung des Migrationsprozesses zu erhalten.
- Wir empfehlen dringend, dass Sie Ihre Sandbox-Umgebung in der eigenständigen Infrastruktur aktualisieren, bevor Sie die erste Migration durchführen. Diese Aktualisierung sollte auch Ihre Dataverse-Umgebung umfassen, die mit der Sandbox-Umgebung verbunden ist, zu der Sie migrieren möchten.
- Wir empfehlen dringend, ein Dienstkonto zu verwenden, wenn Sie Ihr Lifecycle Services-Projekt bereitstellen, migrieren und erstellen.
- Planen Sie ein Upgrade der Sandbox-Umgebung für die UAT-Prüfung auf die neueste Version mit allgemeiner Verfügbarkeit (GA). Weitere Informationen finden Sie unter [Überlegungen](hr-infrastructure-merge.md#considerations).
