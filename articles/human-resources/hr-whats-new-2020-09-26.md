---
title: Neuerungen oder Änderungen in Dynamics 365 Human Resources 26. September 2020
description: Dieser Artikel beschreibt Funktionen, die in Microsoft Dynamics 365 Human Resources für den 26. September 2020 neu sind oder geändert wurden.
author: jcart1106
ms.date: 09/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2f78201585101e2848eded69e03d5eb4c22d7e9a
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066761"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-26-2020"></a>Neuerungen oder Änderungen in Dynamics 365 Human Resources 26. September 2020

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Dieser Artikel beschreibt Funktionen, die in Dynamics 365 Human Resources neu oder geändert sind oder bald eingeführt werden. Weitere Informationen zu unserem Aktualisierungsprozess und Zeitplan finden Sie unter [Aktualisierungsprozess](hr-admin-setup-update-process.md).

Weitere Informationen zu neuen Funktionen und den voraussichtlichen allgemeinen Verfügbarkeitsterminen finden Sie unter [Überblick Dynamics 365 Human Resources 2020 Veröffentlichungszyklus 2](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>In dieser Version

Diese Version enthält die folgenden neuen Funktionen und Fehlerbehebungen. Änderungen gelten für Build-Nummer 8.1.3589-hf.3.

### <a name="new-features"></a>Neue Features

Die folgende Funktion ist in dieser Version allgemein verfügbar:

- **Plattform-Update 10.0.13 ist jetzt verfügbar**: Weitere Informationen zu dem Update finden Sie unter [Plattform-Updates für Version 10.0.13 der Finanz- und Betriebs-Apps (Oktober 2020)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-13.md).

### <a name="bug-fixes"></a>Fehlerkorrekturen

Die folgenden Fehlerkorrekturen sind in diesem Release enthalten.

> [!NOTE]
> Unser Ziel ist es, Ihnen diese Informationen so rasch wie möglich zukommen zu lassen. Es gibt möglicherweise Aktualisierungen zu diesem Artikel, um Fehlerbehebungen aufzunehmen, die es nach der Erstveröffentlichung dieses Artikels in den Build geschafft haben.

| Problemnummer | Problem | Description |
| --- | --- | --- |
| 469495 | Aktualisieren Sie den Raster und das Dialogfeld für die Finanzdimension | Der Raster für Finanzdimensionen und Dialogfeld ist im gesamten Human Resources aktualisiert. |
| 474887 | Das Element Arbeitsanforderung öffnet einen falschen Link in einer manuellen Entscheidung | Wenn eine Workflow-Konfiguration eine manuelle Entscheidung enthält, navigieren Sie zur Urlaubsanfrage von **Mir zugewiesene Arbeitselemente** öffnet den falschen Link und zeigt entweder ein leeres Formular oder einen Urlaubsantrag an, der vom aktuellen Benutzer erstellt wurde, anstatt des Formulars, das ihm für die manuelle Entscheidung zugewiesen wurde. |
| 474962 | Die Entität Parameter für Urlaub und Abwesenheit enthält Felder mit mehrdeutigen Beschriftungen | Entitätsbezeichnungen für Urlaubs- und Abwesenheitsparameter werden übersichtlicher aktualisiert. |
| 481401 | Die Abgrenzungsverarbeitung hängt ab, wenn die Basis für das Abgrenzungsdatum nach dem Abgrenzungsstartdatum und am Monatsende liegt | Die Abgrenzungsverarbeitung wird aktualisiert, um keine Verzögerung zu haben, wenn die Abgrenzungsdatenbasis nach dem Abgrenzungsstartdatum und am Monatsende liegt. |
| 447167 | Ablaufende Datensatzlisten enthalten inaktive Mitarbeiter | Die Registerkarte **Ablaufende Datensätze** in **Personalmanagement** schließt inaktive Arbeitnehmer ein. Jetzt sind nur noch aktive Arbeitnehmer eingeschlossen. |
| 486840 | Falscher Urlaubsantrag öffnet ab **Mir zugewiesene Arbeitselemente** | Auswahl eines Urlaubsantrags aus **Mir zugewiesene Arbeitselemente** öffnet nicht mehr die letzte Abwesenheitsanfrage, die dem aktuellen Benutzer zugewiesen wurde. |
| 506868 | Dataverse **Titel** Feld nicht gesetzt für Entität **Berufliche Stellung** | Das Feld **Titel** in den Entitäten **Beruf** und **Berufliche Stellung** werden als nicht angegeben angezeigt. Das **Titel** Feld wird jetzt angezeigt. |
| 430359 | Zugriff auf Offboarding-Checklistenaufgaben mit zugewiesenen Manager- und Mitarbeiterrollen ist nicht möglich | Mitarbeiter mit einem zukünftigen Kündigungsdatum könnten nicht auf ihre Checklistenaufgaben zugreifen, wenn sie nur eine Mitarbeiter- oder Managerrolle hätten. Jetzt können Benutzer mit nur einer Mitarbeiter- oder Manager-Rolle mit einem zukünftigen Kündigungsdatum auf Offboarding-Aufgaben zugreifen. |
| 458102 | Neuer Mitarbeiter erscheint nicht auf der **Informationen zur Arbeitnehmerabrechnung** Entität beim Erstellen | Neue Mitarbeiter werden in die Entität der Mitarbeiterabrechnungsinformationen aufgenommen, ohne dass die Abrechnungsinformationen für den Mitarbeiter vor dem Exportieren der Entität geöffnet werden müssen. |

## <a name="in-preview"></a>Vorschau

Die folgenden neuen Funktionen stehen in der Vorschau zur Verfügung. Weitere Informationen zur Aktivierung oder Deaktivierung von Vorschaufunktionen finden Sie unter [Funktionen verwalten](hr-admin-manage-features.md).

| Funktion | Freigabeplan | Dokumentation |
| --- | --- | --- |
| Human Resources-App in Microsoft Teams | [Mitarbeiterurlaub und Abwesenheitserfahrung in Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Human Resources-App in Teams](./hr-admin-teams-leave-app.md)<br>[Urlaubsanträge in Teams verwalten](hr-teams-leave-app.md) |
| Erweiterte Workflow-Anforderungen und Genehmigungen | [Organisations- und Personalmanagement-Workflow wird verbessert](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Konfigurationsoption zum Positionieren der Liste der mir zugewiesenen Arbeitselemente](./hr-whats-new-2020-09-03.md#configuration-option-to-position-work-items-assigned-to-me-list-477004) |

## <a name="coming-soon"></a>Bald verfügbar

Die folgende neue Funktion ist für eine zukünftige Version geplant:

- [Benutzerdefinierte Links im Manager-Self-Service](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service)

Eine vollständige Liste der geplanten Funktionen und ihrer geplanten Versionen finden Sie unter [Überblick über Dynamics 365 Human Resources 2019 Veröffentlichungszyklus 2](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Was ist neu oder geändert in der Personalabteilung](hr-admin-whats-new.md)
[Überblick Dynamics 365 Human Resources 2020 Veröffentlichungszyklus 2](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)
[Aktualisierungsprozess](hr-admin-setup-update-process.md)
[Funktionen verwalten](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
