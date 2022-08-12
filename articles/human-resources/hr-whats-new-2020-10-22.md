---
title: Neuerungen oder Änderungen in Dynamics 365 Human Resources 22. Oktober 2020
description: Dieser Artikel beschreibt Funktionen, die in Microsoft Dynamics 365 Human Resources für den 22. Oktober 2020 neu sind oder geändert wurden.
author: jcart1106
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-10-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b183ea08a2decc2696ca3bc3997b5cf7f04652d4
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9068060"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-october-22-2020"></a>Neuerungen oder Änderungen in Dynamics 365 Human Resources 22. Oktober 2020

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Dieser Artikel beschreibt Funktionen, die in Dynamics 365 Human Resources neu oder geändert sind oder bald eingeführt werden. Weitere Informationen zu unserem Aktualisierungsprozess und Zeitplan finden Sie unter [Aktualisierungsprozess](hr-admin-setup-update-process.md).

Weitere Informationen zu neuen Funktionen und den voraussichtlichen allgemeinen Verfügbarkeitsterminen finden Sie unter [Überblick Dynamics 365 Human Resources 2020 Veröffentlichungszyklus 2](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>In dieser Version

Diese Version enthält die folgenden neuen Funktionen und Fehlerbehebungen. Änderungen gelten für Build-Nummer 8.1.3680.

### <a name="new-features"></a>Neue Features

Die folgenden Funktionen sind in dieser Version allgemein verfügbar.

| Funktion | Freigabeplan | Dokumentation |
| --- | --- | --- |
| Platform Update 10.0.14(38) | -- | [Plattform-Updates für die Version 10.0.14 der Finanz- und Betriebs-Apps (November 2020)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-14.md) |
| Organisations- und Personalmanagement-Workflows werden verbessert | [Organisations- und Personalmanagement-Workflow wird verbessert](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Konfigurationsoption zum Positionieren der Liste der mir zugewiesenen Arbeitselemente (477004)](./hr-whats-new-2020-09-03.md#configuration-option-to-position-work-items-assigned-to-me-list-477004) |


### <a name="bug-fixes"></a>Fehlerkorrekturen

Die folgenden Fehlerkorrekturen sind in diesem Release enthalten.

> [!NOTE]
> Unser Ziel ist es, Ihnen diese Informationen so schnell wie möglich zukommen zu lassen. Wir können diesen Artikel aktualisieren, um Fehlerbehebungen aufzunehmen, die es nach der Erstveröffentlichung dieses Artikels in den Build geschafft haben.

| Problemnummer| Problem  | Description|
| --- | --- | --- |
| 437922 | Das Importieren von FMLA-Stunden mit der DMF-Entität führt zu einem schreibgeschützten Fehler. | Die Verwendung der Entität FMLA-Stunden zum Importieren von Stunden, die einem FMLA-Fall zugeordnet sind, ist fehlgeschlagen. Wir haben eine Logik hinzugefügt, um sicherzustellen, dass die importierten Stunden die für den Fall verbleibenden Stunden nicht überschreiten. |
| 512019 | Falscher **Letzter Vortrag** Betrag. | Auf der Seite **Auszeit** ändern Sie **Stand Datum** bis zum ersten Tag der nächsten Geschäftsperiode und es wird ein falscher **Letzter Vortrag** Betrag für **Jährliche Urlaubs**-Art angezeigt. Es wird nun die richtige Menge angezeigt. |
| 458639 | Die **Arbeiterkontakte** Entität unterstützt den Änderungsverfolgungsmodus nicht. | Wir haben die **Arbeiterkontakte** Entität aktualisiert, damit Sie sie in eigene Datenbank nutzen (BYOD) verwenden können.|
| 505347 | Schulungsmanager konnten einen Urlaubsantrag für einen Mitarbeiter stellen, wenn die Funktion "optimierte Mitarbeiter" aktiviert war. | Andere Rollen als HR-Assistent und HR-Manager dürfen keine Time-off-Anfragen für Mitarbeiter einreichen. |
| 513490 | Protokollierung des Leistungsmanagements: Fügen Sie die Protokollierung für Pläne ohne Deckungsoptionen hinzu. | Wir haben die Protokollierungsergebnisse für **Planen Sie ohne Deckungsoptionen** aktiviert. Sie werden jetzt in der Tabelle **Ergebnisse verarbeiten** angezeigt und sind korrekt sortiert, um oben angezeigt zu werden. |
| 517021 | Es können nicht mehrere Pläne mit demselben **Planart** Code verwendet werden, wenn **Planart** eine Einschreibung pro Typ hat. | Wir haben die Einschränkungen für die Auswahl von Plänen geändert, bei denen nur eine Registrierung zulässig ist. Die Einschränkungen sind jnun auf **Plan-Typcode**-Ebene statt auf **Planart**. Diese Änderung ermöglicht Pläne wie HSA und FSA, die beide vom gleichen Typ sind, aber Sie können ihnen einen separaten **Plan-Typcode** geben. Auf diese Weise können Sie beide für denselben Registrierungszeitraum auswählen. |
| 444791 | Die Vergütung kann im Mitarbeiter-Self-Service nicht angezeigt werden, wenn **Zugriff einschränken** im Vergütungsplan aktiviert ist. | In der Mitarbeiter-Self-Service-Karte **Vergütung** wird der aktuelle Vergütungsbetrag und der Erhöhungsprozentsatz 0 angezeigt, wenn der Mitarbeiter in einen Plan mit **Zugriff einschränken** aktiviert aufgenommen und bestimmten Rollen zugewiesen wurde. Wir haben dieses Problem behoben, damit Mitarbeiter und Manager immer Vergütungsdetails für sich und ihre direkten Mitarbeiter sehen können. |
| 457542 | Durch das Aktualisieren der Kursdetails nach Abschluss des Kurses werden nicht dieselben Informationen für den Mitarbeiter aktualisiert, der an dem Kurs teilgenommen hat. | Die Mitarbeiterinformationen werden jetzt ordnungsgemäß aktualisiert, wenn Sie die Kursdetails ändern, nachdem ein Kurs geschlossen und erneut geöffnet wurde. |
| 515342 | Daten können nicht eingefügt werden über **CDSLeaveRequestDetailEntity**. Firma wird nicht gefunden oder existiert nicht. | Sie können nun **CDSLeaveRequestDetailEntity** verwenden, um Daten einzufügen. |
| 514743 | Fehler im Formular **E-Mail-Parameter** bei Verwendung von Microsoft Exchange. | Die Meldung Dateien oder Assembly konnten nicht geladen werden ...wird auf der Seite **E-Mail-Parameter** angezeigt, wenn der E-Mail-Anbieter auf **Austausch** eingestellt war. Dieser Fix ermöglicht auch, dass die Seite **E-Mail-Parameter** zum Laden und Speichern verwendet wird wie erwartet. |


## <a name="in-preview"></a>Vorschau

Die folgenden neuen Funktionen stehen in der Vorschau zur Verfügung. Weitere Informationen zur Aktivierung oder Deaktivierung von Vorschaufunktionen finden Sie unter [Funktionen verwalten](hr-admin-manage-features.md).

| Funktion | Freigabeplan | Dokumentation |
| --- | --- | --- |
| Human Resources-App in Microsoft Teams | [Mitarbeiterurlaub und Abwesenheitserfahrung in Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Human Resources-App in Teams](./hr-admin-teams-leave-app.md)<br>[Urlaubsanträge in Teams verwalten](hr-teams-leave-app.md) |
| Erweiterte Workflow-Anforderungen und Genehmigungen | [Organisations- und Personalmanagement-Workflow wird verbessert](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Konfigurationsoption zum Positionieren der Liste der mir zugewiesenen Arbeitselemente](./hr-whats-new-2020-09-03.md#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| Virtuelle Entitäten in Dataverse für die Personalabteilung | [Erweitern der Dynamics 365 Human Resources Kerndaten in Dataverse](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/expand-dynamics-365-human-resources-core-data-common-data-service) | [Konfigurieren von Dataverse virtuellen Entitäten](hr-admin-integration-common-data-service-virtual-entities.md) |
| Integration mit LinkedIn Talent Hub | [Integration mit LinkedIn Talent Hub](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/integration-linkedin-talent-hub) | [In LinkedIn Talent Hub integrieren](./hr-admin-integration-linkedin.md) |
| Benutzerdefinierte Links im Manager-Self-Service | [Benutzerdefinierte Links im Manager-Self-Service](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service) | [Benutzerdefinierte Links im Manager-Self-Service](./hr-employee-manager-self-service-custom-links.md) |

## <a name="coming-soon"></a>Bald verfügbar

Eine vollständige Liste der geplanten Funktionen und ihrer geplanten Versionen finden Sie unter [Überblick über Dynamics 365 Human Resources 2020 Veröffentlichungszyklus 2](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).


## <a name="see-also"></a>Siehe auch

[Neuerungen oder Änderungen in Human Resources](hr-admin-whats-new.md)</br>
[Übersicht zu Dynamics 365 Human Resources 2020 Versionswelle 2](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[Aktualisierungsprozess](hr-admin-setup-update-process.md)</br>
[Funktionen verwalten](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
