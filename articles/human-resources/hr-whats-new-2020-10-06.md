---
title: Neuerungen oder Änderungen in Dynamics 365 Human Resources (6. Oktober 2020)
description: Dieses Thema beschreibt Funktionen, die in Microsoft Dynamics 365 Human Resources für den 6. Oktober 2020 neu sind oder geändert wurden.
author: jcart1106
manager: tfehr
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 330b037e2ba50ed090fd41b0990d6cf37d9d8b01
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463549"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-october-6-2020"></a>Neuerungen oder Änderungen in Dynamics 365 Human Resources (6. Oktober 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

In diesem Thema werden die Funktionen beschrieben, die in Dynamics 365 Human Resources neu oder geändert wurden oder demnächst verfügbar sind. Weitere Informationen zu unserem Aktualisierungsprozess und Zeitplan finden Sie unter [Aktualisierungsprozess](hr-admin-setup-update-process.md).

Weitere Informationen zu neuen Funktionen und den voraussichtlichen allgemeinen Verfügbarkeitsterminen finden Sie unter [Überblick Dynamics 365 Human Resources 2020 Veröffentlichungszyklus 2](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>In dieser Version

Diese Version enthält die folgenden neuen Funktionen und Fehlerbehebungen. Änderungen gelten für Build-Nummer 8.1.3636.

### <a name="new-features"></a>Neue Features

Die folgende Funktion ist in dieser Version allgemein verfügbar.

| Funktion | Freigabeplan | Dokumentation |
| --- | --- | --- |
| Zusätzlicher Einblick in Urlaubskalender | [Zusätzlicher Einblick in Urlaubskalenderansichten](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/provide-additional-insight-leave-calendar-views) | [Team- und Unternehmenskalender anzeigen](hr-employee-self-service-calendar.md) |

### <a name="bug-fixes"></a>Fehlerkorrekturen

Die folgenden Fehlerkorrekturen sind in diesem Release enthalten.

>[!NOTE]
> Unser Ziel ist es, Ihnen diese Informationen so rasch wie möglich zukommen zu lassen. Es gibt möglicherweise Aktualisierungen zu diesem Thema, um Fehlerbehebungen aufzunehmen, die es nach der Erstveröffentlichung dieses Themas in den Build geschafft haben.

| Problemnummer | Abgang | Beschreibung |
| --- | --- | --- |
| 448806 | **Standardidentifikationstyp** Exporte als **RecID** in HCM-Parametern | Diese Änderung an der Entität Human Resources-Parameter fügt eine zusätzliche Spalte hinzu, in der der **Standardidentifikationstyp** angezeigt wird. |
| 492923 | Aufgabenaufzeichnungen werden in Lifecycle Services (LCS) nicht gespeichert | Aufgabenaufzeichnungen können nun im LCS gespeichert werden. |
| 429950 | Die feste Kompensation läuft beim Positionswechsel nicht korrekt ab | Beim Ändern der Position eines Arbeiters auf der Seite **Arbeiter übertragen** wurde das Datum der Endvergütung einen Tag vor dem Ende der Position festgelegt. Das Enddatum der Vergütung entspricht jetzt dem Enddatum der Position. |
| 467214 | **Entlöhungs-Analytik** wird nur angezeigt, wenn **Name der Umrechnung der Zahlungsrate** auf **Jährlich** eingestellt ist | Lohnsätze mit einem anderen Namen als **Jährlich** wurde in Compensation Analytics nicht angezeigt. Mit diesem Update verwendet Kompensations-Analytics jetzt alle Lohnratenwechsel. Beim Ausführen der Berichte von **Stündlich** oder **Gehalt** werden alle Lohnumrechnungen, die einen anderen Zeitraum als stündlich verwenden, im Filter **Gehalt** eingeschlossen. Nur Gehaltsraten mit einem Zeitraum von **Stunden** sind im Filter **Stunden** enthalten. |
| 482464 | Beim Anzeigen von **Bewertungen** ändert die Ansicht **Einzelheiten** die Rasteransicht nicht, nachdem ein Filter angewendet wurde | Nach dem Anwenden eines Filters wird der Überprüfungsraster wie erwartet angezeigt. |
| 483184 | Die Personalabteilung generiert bei Ihrer Auswahl keine Urlaubsrückstellungen, wenn Sie **Stufengrundlage** als das **angepasste Startdatum** im Datensatz **Beitritt verlassen** auswählen |Das **Angepasste Startdatum** wird ausgefüllt und bei der Generierung von Urlaubsrückstellungen verwendet.  |
| 509731 | Die Freistellungsanforderung für künftig gekündigte Arbeitnehmer verursacht Probleme, wenn sie nach dem Kündigungsdatum eine Freistellung beantragen | Freistellungsanfragen können jetzt für Mitarbeiter mit einem zukünftigen Kündigungsdatum eingereicht werden, solange die Anfrage vor dem Kündigungsdatum liegt. |
| 510716 | Kompensations Analytics umfasst sowohl männliche als auch weibliche Mitarbeiter für **Männlicher durchschnittlicher Stundenlohn** | In Kompensations-Analytics wird der **Männliche durchschnittliche Stundenlohn** auf der **Demografischen Analyse der Vergütung** inklusive weiblichem Durchschnittslohn angezeigt. Jetzt sind nur noch Männer dabei. |
| 511348 | Die Self-Service-Leistungen sollte nur Leistungspläne anzeigen, die von heute bis zum Ende des Leistungszeitraums gültig sind | Abgelaufene Leistungspläne wurden den Mitarbeitern auf der Seite **Leistungsregistrierung** angezeigt. Dieser Fix entfernt diese Pläne. |
| 512706 | Stellen Sie die folgenden Felder schreibgeschützt ein:<ul><li>BenefitPlanEmployeeEntity</li><li>EnrollmentConfirmed</li><li>EnrollmentConfirmedBy</li><li>EnrollmentConfirmedDateTime | Die Schaltflächen **Hinzufügen** und **Entfernen** für Bemaßungsdetails wurden nach Abschluss der Aktion falsch aktiviert. Dieses Update für die Seite **Positionsaktionsdetail** macht die Felder nach Abschluss der Aktion nicht mehr bearbeitbar. |

## <a name="in-preview"></a>Vorschau

Die folgenden neuen Funktionen stehen in der Vorschau zur Verfügung. Weitere Informationen zur Aktivierung oder Deaktivierung von Vorschaufunktionen finden Sie unter [Funktionen verwalten](hr-admin-manage-features.md).

| Funktion | Freigabeplan | Dokumentation |
| --- | --- | --- |
| Human Resources-App in Microsoft Teams | [Mitarbeiterurlaub und Abwesenheitserfahrung in Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Human Resources-App in Teams](https://go.microsoft.com/fwlink/?linkid=2127841)<br>[Urlaubsanträge in Teams verwalten](hr-teams-leave-app.md) |
| Erweiterte Workflow-Anforderungen und Genehmigungen | [Organisations- und Personalmanagement-Workflow wird verbessert](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Konfigurationsoption zum Positionieren der Liste der mir zugewiesenen Arbeitselemente](https://docs.microsoft.com/dynamics365/human-resources/hr-whats-new-2020-09-03#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| Virtuelle Entitäten in Dataverse für die Personalabteilung | [Erweitern der Dynamics 365 Human Resources Kerndaten in Dataverse](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/expand-dynamics-365-human-resources-core-data-common-data-service) | [Konfigurieren von Dataverse virtuellen Entitäten](hr-admin-integration-common-data-service-virtual-entities.md) |

## <a name="coming-soon"></a>Bald verfügbar

Die folgende neuen Funktionen sind für eine zukünftige Version geplant:

- **Prüflistenentitäten in Dataverse**: Prüflistenentitäten für Onboarding, Offboarding, Übergänge und Geschäftsprozesse werden in Kürze in Dataverse verfügbar sein.

- **Leistungsverwaltungs-Ursachencodes**: Ursachencodes für die Leistungsverwaltung werden in Kürze mit vorhandenen Ursachencodes in Human Resources kombiniert. Wenn Sie in der Vergütungsverwaltung Ursachencodes mit mehr als 15 Zeichen erstellt haben, müssen Sie den Namen des Ursachencodes im Vergütungsverwaltungsformular **Ursachencodes** auf maximal 15 Zeichen ändern. Nachdem Sie den Namen aktualisiert haben, wird der Ursachencode unter dem vorhandenen Ursachencodeformular in der Personalverwaltung angezeigt. Diese Änderung wird in Zukunft verfügbar sein und sich nicht auf vorhandene Funktionen auswirken.

- **Benutzerdefinierte Links im Manager-Self-Service**: Um Manager zu unterstützen, erweitern wir die Funktionen im Manager-Self-Service. Wir fügen die Möglichkeit hinzu, benutzerdefinierte Links zur Registerkarte **Mein Team** hinzuzufügen. Diese Funktion ähnelt der Funktion für benutzerdefinierte Links auf der **Registerkarte Meine Informationen** im Mitarbeiter-Self-Service. Weitere Informationen finden Sie unter [Benutzerdefinierte Links im Manager-Self-Service](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service).

Eine vollständige Liste der geplanten Funktionen und ihrer geplanten Versionen finden Sie unter [Überblick über Dynamics 365 Human Resources 2019 Veröffentlichungszyklus 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Neuerungen oder Änderungen in Human Resources](hr-admin-whats-new.md)</br>
[Übersicht zu Dynamics 365 Human Resources 2020 Versionswelle 2](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[Aktualisierungsprozess](hr-admin-setup-update-process.md)</br>
[Funktionen verwalten](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]