---
title: Instanz kopieren
description: Sie können mit Microsoft Dynamics Lifecycle Services (LCS) eine Microsoft Dynamics 365 Human Resources-Datenbank in eine Sandkastenumgebung kopieren.
author: twheeloc
ms.date: 07/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 20a2ffb44f9b99800146e3365e6f0d6df8e9a75e
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2022
ms.locfileid: "9324259"
---
# <a name="copy-an-instance"></a>Instanz kopieren

_**Gilt für:** Human Resources in der eigenständigen Infrastruktur_ 

> [!NOTE]
> Ab Juni 2022 können Human Resources Umgebungen nur noch auf der Finanz- und Betriebs-App-Infrastruktur bereitgestellt werden. Weitere Informationen finden Sie unter [Personal Resources in der Finanzen und Betrieb Infrastruktur bereitstellen](hr-admin-setup-provision-fo.md).

> [!IMPORTANT]
> Die Finanzen und Betrieb-Infrastruktur unterstützt keine Funktion zum Kopieren von Instanzen. Sie können neue Umgebungen bereitstellen und Datenbankumlagerungen verwenden, um Kopien zu erstellen. Weitere Informationen zum Bereitstellen von Self-Service finden Sie unter [Überblick über die Self-Service-Bereitstellung](../fin-ops-core/dev-itpro/deployment/infrastructure-stack.md). Weitere Informationen über Lagerplatzumlagerungen in der Finanzen und Betrieb-Infrastruktur finden Sie auf der [Homepage für Datenbankumlagerungen](../fin-ops-core/dev-itpro/database/dbmovement-operations.md).

Sie können mit Microsoft Dynamics Lifecycle Services (LCS) eine Microsoft Dynamics 365 Human Resources-Datenbank in eine Sandkastenumgebung kopieren. Wenn Sie eine andere Sandbox-Umgebung haben, können Sie die Datenbank auch aus dieser Umgebung in eine bestimmte Sandbox-Umgebung kopieren.

Beachten Sie beim Kopieren einer Instanz die folgenden Hinweise:

- Die Human Resources-Instanz, die Sie überschreiben möchten, muss eine Sandkastenumgebung sein.

- Die Umgebungen, aus denen Sie kopieren, müssen sich in derselben Region befinden. Sie können nicht über Regionen hinweg kopieren.

- Sie müssen ein Administrator in der Zielumgebung sein, damit Sie sich nach dem Kopieren der Instanz anmelden können.

- Wenn Sie die Human Resources-Datenbank kopieren, kopieren Sie nicht die Elemente (Apps oder Daten), die in einer Microsoft Power Apps-Umgebung enthalten sind. Informationen zum Kopieren von Elementen in einer Power Apps-Umgebung finden Sie in [Umgebung kopieren](/power-platform/admin/copy-environment). Die Power Apps-Umgebung, die Sie überschreiben möchten, muss eine Sandkastenumgebung sein. Sie müssen ein globaler Mandantenadministrator sein, um eine Power Apps-Produktionsumgebung zu einer Sandkastenumgebung umzuwandeln. Weitere Informationen zum Ändern einer Power Apps-Umgebung finden Sie in [Instanz wechseln](/dynamics365/admin/switch-instance).

- Wenn Sie eine Instanz in Ihre Sandbox-Umgebung kopieren und Ihre Sandbox-Umgebung in Dataverse integrieren möchten, müssen Sie benutzerdefinierte Felder erneut auf Dataverse-Tabellen anwenden. Sehen Sie [Anwenden benutzerdefinierter Felder auf Dataverse](hr-admin-setup-copy-instance.md?apply-custom-fields-to-common-data-service).

## <a name="effects-of-copying-a-human-resources-database"></a>Auswirkungen des Kopierens einer Human Resources-Datenbank

> [!Note]
> Ab August 2022 sind Dokumente in Microsoft Azure Blob Storage Kopieren einer Produktionsumgebung in eine Sandbox-Umgebung enthalten. Alle angehängten Dokumente und Vorlagen werden aus der Quellumgebung in die Zielumgebung kopiert.

Die folgenden Ereignisse treten auf, wenn Sie eine Human Resources-Datenbank kopieren:

- Der Kopiervorgang löscht die vorhandene Datenbank in der Zielumgebung. Nach Abschluss des Kopiervorgangs können Sie die vorhandene Datenbank nicht wiederherstellen.

- Die Zielumgebung ist erst verfügbar, wenn der Kopiervorgang abgeschlossen ist.

- Alle Benutzer außer denen mit der Sicherheitsrolle „Systemadministrator“ und andere interne Dienstbenutzerkonten sind nicht verfügbar. Der Admin-Benutzer kann Daten löschen, bevor andere Benutzer wieder in das System zugelassen werden.

- Ein Benutzer mit der Sicherheitsrolle „Systemadministrator“ muss die erforderlichen Konfigurationsänderungen vornehmen, z. B. das erneute Verbinden von Integrationsendpunkten mit bestimmten Diensten oder URLs.

## <a name="copy-the-human-resources-database"></a>Human Resources-Datenbank kopieren

Um diese Aufgabe abzuschließen, kopieren Sie zuerst eine Instanz und melden sich dann im Microsoft Power Platform Admin Center an, um Ihre Power Apps-Umgebung zu kopieren.

> [!WARNING]
> Wenn Sie eine Instanz kopieren, wird die Datenbank in der Zielinstanz gelöscht. Die Zielinstanz ist während dieses Vorgangs nicht verfügbar.

1. Melden Sie sich bei LCS an und wählen Sie das LCS-Projekt aus, das die zu kopierende Instanz enthält.

2. In Ihrem LCS-Projekt wählen Sie die Kachel **Human Resources App-Verwaltung** aus.

3. Wählen Sie die zu kopierende Instanz aus und wählen Sie dann **Kopieren**.

4. Wählen Sie im Aufgabenbereich **Instanz kopieren** die zu überschreibende Instanz und anschließend **Kopieren** aus. Warten Sie, bis das Feld **Kopierstatus** auf **Erledigt** aktualisiert wird.

   ![[Zu überschreibende Instanz auswählen.](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. Wählen Sie **Power Platform** aus und melden Sie sich im Microsoft Power Platform Admin Center an.

   ![[Power Platform auswählen.](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. Wählen Sie die zu kopierende Power Apps-Umgebung aus und wählen Sie dann **Kopieren**.

Weitere Informationen zum Kopieren von Power Apps-Umgebungen finden Sie unter [Kopieren einer Umgebung](/power-platform/admin/copy-environment#copy-an-environment-1).

7. Wenn der Kopiervorgang abgeschlossen ist, melden Sie sich bei der Zielinstanz an und aktivieren Sie die Dataverse-Integration. Weitere Informationen und Anleitungen finden Sie unter [Dataverse-Integration konfigurieren](./hr-admin-integration-common-data-service.md).

## <a name="data-elements-and-statuses"></a>Datenelemente und ‑status

Die folgenden Datenelemente werden beim Kopieren einer Human Resources-Instanz nicht kopiert:

- E-Mail-Adressen in der Tabelle **LogisticsElectronicAddress**

- Die Batchauftrag-Historie in den Tabellen **BatchJobHistory**, **BatchHistory** und **BatchConstraintHistory**

- Das SMTP-Kennwort (Simple Mail Transfer Protocol) in der Tabelle **SysEmailSMTPPassword**

- Der SMTP-Relay-Server in der Tabelle **SysEmailParameters**

- Druckverwaltungseinstellungen in den Tabellen **PrintMgmtSettings** und **PrintMgmtDocInstance**

- Umgebungsspezifische Datensätze in den Tabellen **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig** und **BatchServerGroup**

- Dokumentanhänge in der DocuValue-Tabelle. Diese Anhänge enthalten alle Microsoft Office-Vorlagen, die in der Quellumgebung überschrieben wurden

- Die Verbindungszeichenfolge in der Tabelle **PersonnelIntegrationConfiguration**

Einige dieser Elemente werden nicht kopiert, da sie umgebungsspezifisch sind. Dazu zählen beispielsweise die Datensätze **BatchServerConfig** und **SysCorpNetPrinters**. Andere Elemente werden aufgrund des Umfangs der Support-Tickets nicht kopiert. Beispiel:

- Möglicherweise werden doppelte E-Mails gesendet, da SMTP in der Umgebung für Benutzerakzeptanztests (Sandkasten) weiterhin aktiviert ist.

- Möglicherweise werden ungültige Integrationsnachrichten gesendet, da Batchaufträge noch aktiviert sind.

- Benutzer werden möglicherweise aktiviert, bevor Administratoren Bereinigungsaktionen nach der Aktualisierung ausführen können.

Außerdem ändern sich die folgenden Status beim Kopieren einer Instanz:

- Alle Benutzer außer denen mit der Sicherheitsrolle „Systemadministrator“ sind **Deaktiviert**.

- Alle Batchaufträge außer einigen Systemaufträgen werden auf **Zurückhalten** gesetzt.

## <a name="environment-admin"></a>Umgebungsadministrator

Alle Benutzer in der Ziel-Sandkastenumgebung, einschließlich Administratoren, werden durch die Benutzer der Quellumgebung ersetzt. Stellen Sie vor dem Kopieren einer Instanz sicher, dass Sie ein Administrator in der Quellumgebung sind. Ist dies nicht der Fall, können Sie sich nach Abschluss des Kopiervorgangs nicht in der Sandbox-Umgebung des Ziels anmelden.

Alle Nicht-Administrator-Benutzer in der Ziel-Sandkastenumgebung sind deaktiviert, um unerwünschte Anmeldungen in der Sandkastenumgebung zu verhindern. Administratoren können Benutzer bei Bedarf erneut aktivieren.

## <a name="apply-custom-fields-to-dataverse"></a>Benutzerdefinierte Felder auf Dataverse anwenden

Wenn Sie eine Instanz in Ihre Sandbox-Umgebung kopieren und Ihre Sandbox-Umgebung in Dataverse integrieren möchten, müssen Sie benutzerdefinierte Felder erneut auf Dataverse-Tabellen anwenden.

Für jedes benutzerdefinierte Feld, das in Dataverse-Tabellen angezeigt wird, führen Sie die folgenden Schritte aus:

1. Gehen Sie zum benutzerdefinierten Feld und wählen Sie **Bearbeiten** aus.

2. Deaktivieren Sie das Feld **Aktiviert** für jede cdm_*-Entität, für die das benutzerdefinierte Feld aktiviert ist.

3. Wählen Sie **Änderungen übernehmen** aus.

4. Wählen Sie erneut **Bearbeiten** aus.

5. Wählen Sie das Feld **Aktiviert** für jede cdm_*-Entität aus, für die das benutzerdefinierte Feld aktiviert ist.

6. Wählen Sie erneut **Änderungen übernehmen** aus.

Beim Aufheben der Auswahl, dem Anwenden von Änderungen, dem erneuten Auswählen und erneuten Anwenden von Änderungen wird das Schema zur Aktualisierung in Dataverse aufgefordert, die benutzerdefinierten Felder einzuschließen.

Weitere Informationen über benutzerdefinierte Felder finden Sie unter [Erstellen und Arbeiten mit benutzerdefinierten Feldern](../fin-ops-core/fin-ops/get-started/user-defined-fields.md).

## <a name="see-also"></a>Siehe auch

[Personalverwaltung bereitstellen](hr-admin-setup-provision.md)</br>
[Eine Instanz entfernen](hr-admin-setup-remove-instance.md)</br>
[Aktualisierungsprozess](hr-admin-setup-update-process.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
