---
title: Instanz kopieren
description: Sie können mit Microsoft Dynamics Lifecycle Services (LCS) eine Microsoft Dynamics 365 Human Resources-Datenbank in eine Sandkastenumgebung kopieren.
author: andreabichsel
manager: AnnBe
ms.date: 07/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 40ca0a4d9733fc2a163daa4ea1c27a3bfae6d3bf
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527836"
---
# <a name="copy-an-instance"></a>Instanz kopieren

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Sie können mit Microsoft Dynamics Lifecycle Services (LCS) eine Microsoft Dynamics 365 Human Resources-Datenbank in eine Sandkastenumgebung kopieren. Wenn Sie eine andere Sandbox-Umgebung haben, können Sie die Datenbank auch aus dieser Umgebung in eine bestimmte Sandbox-Umgebung kopieren.

Beachten Sie beim Kopieren einer Instanz die folgenden Hinweise:

- Die Human Resources-Instanz, die Sie überschreiben möchten, muss eine Sandkastenumgebung sein.

- Die Umgebungen, aus denen Sie kopieren, müssen sich in derselben Region befinden. Sie können nicht über Regionen hinweg kopieren.

- Sie müssen ein Administrator in der Zielumgebung sein, damit Sie sich nach dem Kopieren der Instanz anmelden können.

- Wenn Sie die Human Resources-Datenbank kopieren, kopieren Sie nicht die Elemente (Apps oder Daten), die in einer Microsoft Power Apps-Umgebung enthalten sind. Informationen zum Kopieren von Elementen in einer Power Apps-Umgebung finden Sie in [Umgebung kopieren](https://docs.microsoft.com/power-platform/admin/copy-environment). Die Power Apps-Umgebung, die Sie überschreiben möchten, muss eine Sandkastenumgebung sein. Sie müssen ein globaler Mandantenadministrator sein, um eine Power Apps-Produktionsumgebung zu einer Sandkastenumgebung umzuwandeln. Weitere Informationen zum Ändern einer Power Apps-Umgebung finden Sie in [Instanz wechseln](https://docs.microsoft.com/dynamics365/admin/switch-instance).

- Wenn Sie eine Instanz in Ihre Sandbox-Umgebung kopieren und Ihre Sandbox-Umgebung in Common Data Service integrieren möchten, müssen Sie benutzerdefinierte Felder erneut auf Common Data Service-Entitäten anwenden. Sehen Sie [Anwenden benutzerdefinierter Felder auf Common Data Service](hr-admin-setup-copy-instance.md?apply-custom-fields-to-common-data-service).

## <a name="effects-of-copying-a-human-resources-database"></a>Auswirkungen des Kopierens einer Human Resources-Datenbank

Die folgenden Ereignisse treten auf, wenn Sie eine Human Resources-Datenbank kopieren:

- Der Kopiervorgang löscht die vorhandene Datenbank in der Zielumgebung. Nach Abschluss des Kopiervorgangs können Sie die vorhandene Datenbank nicht wiederherstellen.

- Die Zielumgebung ist erst verfügbar, wenn der Kopiervorgang abgeschlossen ist.

- Dokumente im Microsoft Azure Blob-Speicher werden nicht von einer Umgebung in eine andere kopiert. Als Ergebnis werden angehängte Dokumente und Vorlagen nicht kopiert und verbleiben in der Quellumgebung.

- Bis auf den Administrator und andere interne Servicebenutzer werden alle Benutzer deaktiviert. Der Administrator kann Daten löschen oder verschleiern, bevor andere Benutzer wieder Zugriff auf das System erhalten.

- Der Administrator muss die erforderlichen Konfigurationsänderungen vornehmen, z. B. das erneute Verbinden von Integrationsendpunkten mit bestimmten Diensten oder URLs.

## <a name="copy-the-human-resources-database"></a>Human Resources-Datenbank kopieren

Um diese Aufgabe abzuschließen, kopieren Sie zuerst eine Instanz und melden sich dann im Microsoft Power Platform Admin Center an, um Ihre Power Apps-Umgebung zu kopieren.

> [!WARNING]
> Wenn Sie eine Instanz kopieren, wird die Datenbank in der Zielinstanz gelöscht. Die Zielinstanz ist während dieses Vorgangs nicht verfügbar.

1. Melden Sie sich bei LCS an und wählen Sie das LCS-Projekt aus, das die zu kopierende Instanz enthält.

2. In Ihrem LCS-Projekt wählen Sie die Kachel **Human Resources App-Verwaltung** aus.

3. Wählen Sie die zu kopierende Instanz aus und wählen Sie dann **Kopieren**.

4. Wählen Sie im Aufgabenbereich **Instanz kopieren** die zu überschreibende Instanz und anschließend **Kopieren** aus. Warten Sie, bis der Wert des Felds **Kopierstatus** zu **Abgeschlossen** aktualisiert wird.

   ![[Zu überschreibende Instanz auswählen](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. Wählen Sie **Power Platform** aus und melden Sie sich im Microsoft Power Platform Admin Center an.

   ![[Power Platform auswählen](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. Wählen Sie die zu kopierende Power Apps-Umgebung aus und wählen Sie dann **Kopieren**.

7. Wenn der Kopiervorgang abgeschlossen ist, melden Sie sich bei der Zielinstanz an und aktivieren Sie die Common Data Service-Integration. Weitere Informationen und Anleitungen finden Sie unter [Common Data Service-Integration konfigurieren](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).

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

- Alle Benutzer außer Administratoren werden auf **Deaktiviert** gestellt.

- Alle Batchaufträge außer einigen Systemaufträgen werden auf **Zurückhalten** gesetzt.

## <a name="environment-admin"></a>Umgebungsadministrator

Alle Benutzer in der Ziel-Sandkastenumgebung, einschließlich Administratoren, werden durch die Benutzer der Quellumgebung ersetzt. Stellen Sie vor dem Kopieren einer Instanz sicher, dass Sie ein Administrator in der Quellumgebung sind. Andernfalls können Sie sich nach Abschluss des Kopiervorgangs nicht bei der Ziel-Sandkastenumgebung anmelden.

Alle Nicht-Administrator-Benutzer in der Ziel-Sandkastenumgebung sind deaktiviert, um unerwünschte Anmeldungen in der Sandkastenumgebung zu verhindern. Administratoren können Benutzer bei Bedarf erneut aktivieren.

## <a name="apply-custom-fields-to-common-data-service"></a>Benutzerdefinierte Felder auf Common Data Service anwenden

Wenn Sie eine Instanz in Ihre Sandbox-Umgebung kopieren und Ihre Sandbox-Umgebung in Common Data Service integrieren möchten, müssen Sie benutzerdefinierte Felder erneut auf Common Data Service-Entitäten anwenden.

Für jedes benutzerdefinierte Feld, das in Common Data Service-Entitäten angezeigt wird, führen Sie die folgenden Schritte aus:

1. Gehen Sie zum benutzerdefinierten Feld und wählen Sie **Bearbeiten** aus.

2. Deaktivieren Sie das Feld **Aktiviert** für jede cdm_*-Entität, für die das benutzerdefinierte Feld aktiviert ist.

3. Wählen Sie **Änderungen übernehmen** aus.

4. Wählen Sie erneut **Bearbeiten** aus.

5. Wählen Sie das Feld **Aktiviert** für jede cdm_*-Entität aus, für die das benutzerdefinierte Feld aktiviert ist.

6. Wählen Sie erneut **Änderungen übernehmen** aus.

Beim Aufheben der Auswahl, dem Anwenden von Änderungen, dem erneuten Auswählen und erneuten Anwenden von Änderungen wird das Schema zur Aktualisierung in Common Data Service aufgefordert, die benutzerdefinierten Felder einzuschließen.

Weitere Informationen über benutzerdefinierte Felder finden Sie unter [Erstellen und Arbeiten mit benutzerdefinierten Feldern](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/user-defined-fields).

## <a name="see-also"></a>Siehe auch

[Personalverwaltung bereitstellen](hr-admin-setup-provision.md)</br>
[Eine Instanz entfernen](hr-admin-setup-remove-instance.md)</br>
[Aktualisierungsprozess](hr-admin-setup-update-process.md)

