---
title: Was ist neu oder geändert in Dynamics 365 Human Resources 22. März 2021
description: Dieses Thema beschreibt Funktionen, die in Microsoft Dynamics 365 Human Resources für den 22. März 2021 entweder neu sind oder geändert wurden.
author: marcelbf
ms.date: 03/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-03-22
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0f08dc966353cc612c8145f29e2cd8c303da5b359292a8f928d97f0e0de99585
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6777087"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-22-2021"></a>Was ist neu oder geändert in Dynamics 365 Human Resources 22. März 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In diesem Thema werden die Funktionen beschrieben, die in Dynamics 365 Human Resources neu oder geändert wurden oder demnächst verfügbar sind.

Weitere Informationen zu unserem Aktualisierungsprozess und Zeitplan finden Sie unter [Aktualisierungsprozess](hr-admin-setup-update-process.md).

Weitere Informationen zu neuen Funktionen und den voraussichtlichen allgemeinen Verfügbarkeitsterminen finden Sie unter [Überblick Dynamics 365 Human Resources 2021 Veröffentlichungszyklus 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>In dieser Version

Diese Version enthält die folgenden neuen Funktionen und Fehlerbehebungen. Änderungen gelten für Build-Nummer 8.1.4049.

### <a name="new-features"></a>Neue Features

Die folgenden Funktionen sind in dieser Version allgemein verfügbar.

| Funktion | Freigabeplan | Dokumentation |
| --- | --- | --- |
| Option zum Erzwingen des Abbrechens und Zurücksetzens von festgefahrenen Batchaufträgen (560976) | NA | [Steckengebliebene Batchaufträge zurücksetzen](./hr-admin-troubleshooting-batch-execution.md) |
| Kleinere UX-Updates zum Erstellen eines neuen Vorteilsplans (419941) | NA | [Vorteilsplan erstellen](hr-benefits-plans-setup.md) |

### <a name="bug-fixes"></a>Fehlerkorrekturen

Die folgenden Fehlerkorrekturen sind in diesem Release enthalten.

> [!NOTE]
> Unser Ziel ist es, Ihnen diese Informationen so schnell wie möglich zukommen zu lassen. Wir können dieses Thema aktualisieren, um Fehlerbehebungen aufzunehmen, die es nach der Erstveröffentlichung dieses Themas in den Build geschafft haben.

| Problemnummer | Abgang |  Beschreibung |
| --- | --- | --- |
| 554239 | Leistungsverbesserungen für Entitäten im Zusammenhang mit der **BusinessProcessTaskAssignment**-Tabelle | Verbesserung der Leistung von Entitäten im Zusammenhang mit der **BusinessProcessTaskAssignment**-Tabelle durch Hinzufügen von vorgeschlagenen Indizes zur Tabelle. |
| 566061 | Entfernen von Fallback-Code der V2-Entität aus der nächtlichen Synchronisierung | Entfernen Sie den V2-Fallback-Code für die nächtliche Dataverse-Synchronisierung. Der Fallback ist nicht mehr erforderlich und verhindert, dass die gefilterte Synchronisierung wie erwartet funktioniert. Die Änderung verbessert die Konsistenz der Dataverse-Datensynchronisation. |
| 538024 | Vergütungspläne für Arbeitskräfte > Fehlerausgabe beim Entfernen des Auscheckens | Fehler beim Entfernen des Auscheckens für die Vergütungsplanoption im Formular für Arbeitnehmervergütungen behoben. |
| 557965 | **Vergütungen**-Arbeitsbereich: **Aktive Lebensereignisse**-Link sollte immer im Abschnitt **Links** sichtbar sein | Problem behoben, bei dem der **Aktive Lebensereignisse**-Link im Abschnitt **Links** sichtbar war, aber beim Versuch zu navigieren einen Fehler ausgab, wenn die Funktion **(Vorschau) Arbeitsbereich für Vorteilsverwaltung** nicht aktiviert ist. Weitere Informationen zum Aktivieren des Arbeitsbereichs finden Sie unter [Arbeitsbereich „Vorteilsverwaltung“](hr-benefits-management-workspace.md). |
| 556672 | Rückstellungen für einen gekündigten Mitarbeiter können nicht verarbeitet werden, wenn **Fortschrittlicher Mitarbeitereintrag** in der Funktionsverwaltung aktiviert ist | Die Option, Urlaubs- und Abwesenheitspläne zu antizipieren, wurde zu **Weitere Optionen** unter **Arbeitshistorie** für Mitarbeiter hinzugefügt, wenn **Fortschrittlicher Mitarbeitereintrag** in der Funktionsverwaltung aktiviert ist. |
| 562656 | Der Menüpunkt **SysRecordChangeLogValidTimeState** sollte in einem Sicherheitsrecht und einer Erweiterung der **SystemExternalBasicMaintain**-Sicherheitspflicht enthalten sein | Nicht-Systemadministratorrollen fehlte die **Änderungen anzeigen**-Schaltfläche auf den Datumsmanager-Formularen. |
| 505989 | Verarbeitung von Lebensereignissen: Änderung der Berechtigung aufgrund des verwendeten Datums nicht korrekt verarbeitet | Problem behoben, bei dem die Änderung der Berechtigungsverarbeitung vom Startdatum der Position und nicht nur von der aktuellen Position abhing. |
| 562286 | Arbeitskraft kündigen sendet mehrere Updates an Dataverse | Wenn eine Arbeitskraft gekündigt wird, wird mehr als ein Aktualisierungsvorgang an Dataverse gesendet. Dies führt zu zwei Aktualisierungsbenachrichtigungen für dieselbe Änderung. Dies kann mehrere Auslöser verursachen, wenn ein Power Automate-Flow so konfiguriert ist, dass er von der Aktion ausgelöst wird. |
| 527340 | Der Fehler „Nicht darstellbare DateTime“ wird beim Öffnen von Urlaubs- und Abwesenheitsregistrierungen angezeigt | Bei Auswahl einer Urlaubs- und Abwesenheitsregistrierung wird der Fehler nicht mehr angezeigt. |
| 561663 | Erhöhen des Wartezeitintervalls für die Clusterbereitstellung | Verbessern Sie die Stabilität der Infrastruktur und die Konsistenz der Bereitstellung durch Aktualisierungen der Clusterbereitstellung. |
| 486129 | Benutzerdefinierte Felder in **Positionen > Änderungen verwalten** können nicht bearbeitet werden | Es wurde ein Problem behoben, bei dem benutzerdefinierte Felder auf der **Änderungen verwalten**-Registerkarte für **Positionen** nicht bearbeitet werden konnten. |

## <a name="in-preview"></a>Vorschau

Die folgenden neuen Funktionen stehen in der Vorschau zur Verfügung. Weitere Informationen zur Aktivierung oder Deaktivierung von Vorschaufunktionen finden Sie unter [Funktionen verwalten](hr-admin-manage-features.md).

| Funktion | Freigabeplan | Dokumentation |
| --- | --- | --- |
| Arbeitsbereich für Vorteilsverwaltung | [Arbeitsbereich für die Verwaltung von Zusatzleistungen (Vorschau)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Arbeitsbereich für Vorteilsverwaltung](hr-benefits-management-workspace.md) |
| Einschränkung der Mitarbeiter bei der Bearbeitung von Geschäftskontaktdetails | [Einschränkung der Mitarbeiter bei der Bearbeitung von geschäftlichen Kontaktdetails](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/restrict-employees-editing-business-contact-details) | [Bearbeitung von persönlichen Informationen einschränken](hr-employee-self-service-restrict-editing.md)|

## <a name="coming-soon"></a>Bald verfügbar

| Funktion | Detaildaten |
| --- | --- |
| Von einem Manager für seine Mitarbeiter eingegebene Qualifikationen können von einem Workflow automatisch genehmigt werden | Bald verfügbar. |

Eine vollständige Liste der geplanten Funktionen und ihrer geplanten Versionen finden Sie unter [Überblick über Dynamics 365 Human Resources 2021 Veröffentlichungszyklus 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Siehe auch

[Neuerungen oder Änderungen in Human Resources](hr-admin-whats-new.md)</br>
[Übersicht zu Dynamics 365 Human Resources 2021 Versionswelle 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Aktualisierungsprozess](hr-admin-setup-update-process.md)</br>
[Funktionen verwalten](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]