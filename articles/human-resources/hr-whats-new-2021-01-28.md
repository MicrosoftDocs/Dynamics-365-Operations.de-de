---
title: Neuerungen oder Änderungen in Dynamics 365 Human Resources 28. Januar 2021
description: Dieses Thema beschreibt Funktionen, die in Microsoft Dynamics 365 Human Resources für den 28. Januar 2021 neu sind oder geändert wurden.
author: marcelbf
manager: tfehr
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d9a28ceb74a6cf90e72ccdc91186b685d7d838cb
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463357"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-january-28-2021"></a>Neuerungen oder Änderungen in Dynamics 365 Human Resources 28. Januar 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In diesem Thema werden die Funktionen beschrieben, die in Dynamics 365 Human Resources neu oder geändert wurden oder demnächst verfügbar sind.

Weitere Informationen zu unserem Aktualisierungsprozess und Zeitplan finden Sie unter [Aktualisierungsprozess](hr-admin-setup-update-process.md).

Weitere Informationen zu neuen Funktionen und den voraussichtlichen allgemeinen Verfügbarkeitsterminen finden Sie unter [Überblick Dynamics 365 Human Resources 2021 Veröffentlichungszyklus 1](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>In dieser Version

Diese Version enthält die folgenden neuen Funktionen und Fehlerbehebungen. Änderungen gelten für Build-Nummer 8.1.3906.

### <a name="new-features"></a>Neue Features

Die folgenden Funktionen sind in dieser Version allgemein verfügbar.

| Funktion | Freigabeplan | Dokumentation |
| --- | --- | --- |
| Vorteilsursachencodes in den **Personalverwaltung**-Arbeitsbereich integrieren | -- | [Ursachencodes einrichten](hr-benefits-setup-reason-codes.md) |

### <a name="bug-fixes"></a>Fehlerkorrekturen

Die folgenden Fehlerkorrekturen sind in diesem Release enthalten.

> [!NOTE]
> Unser Ziel ist es, Ihnen diese Informationen so schnell wie möglich zukommen zu lassen. Wir können dieses Thema aktualisieren, um Fehlerbehebungen aufzunehmen, die es nach der Erstveröffentlichung dieses Themas in den Build geschafft haben.


| Problemnummer | Abgang |  Beschreibung |
| --- | --- | --- |
| 539456 | Der Kalender zeigt den Urlaubstyp im Schwebetext an, wenn der Parameter **Abwesenheit nur ohne Details anzeigen** aktiviert ist. | Wenn die Option **Abwesenheit nur ohne Details anzeigen** aktiviert ist, wird das Datum der Anforderung jetzt beim Schweben angezeigt. |
| 528907 | Die Gewährung von Zugriff auf eine juristische Person für die Mitarbeiterrolle führt dazu, dass Manager die Urlaubsbilanzaktivität für Mitarbeiter nicht im **Mein Team**-Bereich des Mitarbeiter-Self-Service anzeigen können. |Wenn Sie diese Option jetzt einstellen, können Manager weiterhin die Urlaubsguthabenaktivität anzeigen. |
| 526280 | Berechtigungsfehler für HcmWorkerEntity, HcmEmployeeEntity und HcmContractorEntity. | Benutzer in einer Nicht-Systemadministratorrolle konnten die aufgelisteten Entitäten aufgrund eines Berechtigungsfehlers im Feld NationalityCountryRegion nicht exportieren. Benutzer benötigen weiterhin die folgenden Berechtigungen, um diese Informationen zu exportieren: HcmWorkerEntityView, HcmEmployeeEntityMaintain, HcmEmployeeEntityMaintain, HcmEmployeeEntityView, HcmContractorEntityMaintain, and HCMContractorEntityView. |
| 542147 | **Kontonummer**- und **Bankleitzahl**-Felder sind obligatorisch, wenn ein Bankkonto über das Mitarbeiter-Self-Service hinzugefügt wird. | Wir haben den Fehler behoben, bei dem Mitarbeiter die Felder **Kontonummer** und **Bankleitzahl** Felder beim Hinzufügen von Bankkontodaten eingeben mussten. Diese Felder sind beim Speichern neuer Bankkontoinformationen nicht mehr obligatorisch. |
| 543641 | Postleitzahl wird in elektronische Berichterstattung nicht eingetragen. | Es wurde ein Fehler behoben, bei dem die Postleitzahl im ACA-Bericht für die Dispositionsverfahren L bis Q nicht ausgefüllt wurde. |
| 545402 | Fügen Sie eine Umleitungsänderung für die Datei UserBranding.js hinzu, um 404-Fehler zu entfernen. | Der Benutzer sollte keine 404-Fehler mehr in der Konsole sehen. |

## <a name="in-preview"></a>Vorschau   

Die folgenden neuen Funktionen stehen in der Vorschau zur Verfügung. Weitere Informationen zur Aktivierung oder Deaktivierung von Vorschaufunktionen finden Sie unter [Funktionen verwalten](hr-admin-manage-features.md).

| Funktion | Freigabeplan | Dokumentation |
| --- | --- | --- |
| Human Resources-App in Microsoft Teams | [Mitarbeiterurlaub und Abwesenheitserfahrung in Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Human Resources-App in Teams](https://go.microsoft.com/fwlink/?linkid=2127841)<br>[Urlaubsanträge in Teams verwalten](hr-teams-leave-app.md) |
| Unternehmensübergreifende Urlaubsansicht für Manager | [Unternehmensübergreifende Ansicht des Mitarbeiterurlaubs für Manager](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Urlaub- und Abwesenheitsparameter konfigurieren](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-parameters) |

## <a name="coming-soon"></a>Bald verfügbar

| Funktion | Detaildaten |
| --- | --- |
| E-Mail-Bestätigung für Vorteilsregistrierung | Diese Funktion bietet eine Option zum Senden einer Bestätigungs-E-Mail an Mitarbeiter, wenn sie sich aus der Umgebung zur Vorteilsregistrierung im Mitarbeiter-Self-Service abmelden. Diese Funktion ist am 1. Februar verfügbar. Weitere Informationen finden Sie unter [Vorteilsverwaltungsparameter pro Unternehmen konfigurieren](hr-benefits-setup-parameters-per-company.md). |
| Von einem Manager für seine Mitarbeiter eingegebene Qualifikationen können von einem Workflow automatisch genehmigt werden | Bald verfügbar. |

Eine vollständige Liste der geplanten Funktionen und ihrer geplanten Versionen finden Sie unter [Überblick über Dynamics 365 Human Resources 2021 Veröffentlichungszyklus 1](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="terminology-updates-for-microsoft-dataverse"></a>Terminologie-Updates für Microsoft Dataverse

Gültig ab November 2020, Common Data Service wurde umbenannt in [Microsoft Dataverse](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro). Siehe die [offizielle Ankündigung](https://powerapps.microsoft.com/blog/reshape-the-future-of-work-with-microsoft-dataverse-for-teams-now-generally-available/) im Power Apps-Blog, um mehr zu erfahren. In Verbindung mit dieser Namensänderung wurde manche Terminologie in Dataverse aktualisiert. Beispielsweise ist *Entität* jetzt *Tabelle* und *Feld* *Säule*. Weitere Informationen finden Sie unter [Terminologie-Aktualisierungen](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro#terminology-updates).

In dieser Version wurde Terminologie, die sich auf die Dynamics 365 Human Resources-Integration mit Dataverse bezieht, in der gesamten Anwendung aktualisiert, um diese Änderungen widerzuspiegeln. Zum Beispiel ist das **Common Data Service-Integration**-Formular jetzt **Microsoft Dataverse-Integration**.

Weitere Informationen zur Dynamics 365 Human Resources-Integration in Microsoft Dataverse finden Sie unter [Konfigurieren der Microsoft Dataverse-Integration](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service) und [Konfigurieren virtueller Microsoft Dataverse-Tabellen](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).

## <a name="see-also"></a>Siehe auch

[Neuerungen oder Änderungen in Human Resources](hr-admin-whats-new.md)</br>
[Übersicht zu Dynamics 365 Human Resources 2021 Versionswelle 1](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Aktualisierungsprozess](hr-admin-setup-update-process.md)</br>
[Funktionen verwalten](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]