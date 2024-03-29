---
title: Was ist neu oder geändert in Dynamics 365 Human Resources 8. März 2021
description: Dieser Artikel beschreibt Funktionen, die in Microsoft Dynamics 365 Human Resources für den 8. März 2021 neu sind oder geändert wurden.
author: marcelbf
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9280e85f9701573717c4115b4d752ed11be4862e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868053"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-08-2021"></a>Was ist neu oder geändert in Dynamics 365 Human Resources März 08, 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dieser Artikel beschreibt Funktionen, die in Dynamics 365 Human Resources neu oder geändert sind oder bald eingeführt werden.

Weitere Informationen zu unserem Aktualisierungsprozess und Zeitplan finden Sie unter [Aktualisierungsprozess](hr-admin-setup-update-process.md).

Weitere Informationen zu neuen Funktionen und den voraussichtlichen allgemeinen Verfügbarkeitsterminen finden Sie unter [Überblick Dynamics 365 Human Resources 2021 Veröffentlichungszyklus 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>In dieser Version

Diese Version enthält die folgenden neuen Funktionen und Fehlerbehebungen. Änderungen gelten für Build-Nummer 8.1.4017.

### <a name="new-features"></a>Neue Features

Die folgenden Funktionen sind in dieser Version allgemein verfügbar.

| Funktion | Freigabeplan | Dokumentation |
| --- | --- | --- |
| Unternehmensübergreifende Urlaubsansicht für Manager | [Unternehmensübergreifende Ansicht des Mitarbeiterurlaubs für Manager](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Urlaub- und Abwesenheitsparameter konfigurieren](./hr-leave-and-absence-parameters.md) |

### <a name="bug-fixes"></a>Fehlerkorrekturen

Die folgenden Fehlerkorrekturen sind in diesem Release enthalten.

> [!NOTE]
> Unser Ziel ist es, Ihnen diese Informationen so schnell wie möglich zukommen zu lassen. Wir können diesen Artikel aktualisieren, um Fehlerbehebungen aufzunehmen, die es nach der Erstveröffentlichung dieses Artikels in den Build geschafft haben.

| Problemnummer | Problem |  Description |
| --- | --- | --- |
| 486611 | Abwesenheit wird im Urlaubskalender angezeigt, wenn **Abwesenheit in allen Kalendern deaktivieren** aktiviert ist | Wenn **Urlaub auf allen Kalendern deaktivieren** aktiviert ist, werden die Urlaubsinformationen nicht mehr angezeigt, wenn die Funktion „Erweiterungen für Urlaubs- und Abwesenheitskalender“ aktiviert ist.|
| 508972 | Entität „Urlaubs- und Abwesenheits-Bank-Transaktion“ fehlt Validierung der Registrierung | Bei Verwendung der Entität Urlaubs- und Abwesenheitsbank-Transaktion können Mitarbeiter, die nicht in einem Plan eingeschrieben sind, nicht mehr importiert werden. |
| 554854 | Fehler beim Aktualisieren des Kalenders in der Entität „Beschäftigung“, wenn die juristische Entität in den Benutzeroptionen anders eingestellt ist | Die Verwendung der Entität „Beschäftigung“ zum Aktualisieren des Kalenders für einen Mitarbeiter führt nicht mehr zu einem Fehler, wenn die standardmäßige juristische Entität in den Benutzeroptionen unterschiedlich ist. |
| 558347 | „Cannot create a record in Form configurations (FormRunConfiguration)“ erscheint beim Laden der Startseite. | Personalisierungen führen dazu, dass beim Laden der Startseite der Fehler „Cannot create a record in Form configurations (FormRunConfiguration)“ erscheint. |
| 557327 | Arbeitsbereich des Vergütungsverwaltung: Lücke erscheint oberhalb des Rasters. | Es wurde ein Problem mit der Benutzerfreundlichkeit behoben, bei dem eine unbeabsichtigte Lücke an den Rändern des Tabellenrasters im Arbeitsbereich „Benefits“ erschien. |
| 557334 | Arbeitsbereich des Vergütungsverwaltung: Die Dropdown-Box für die **Periode**-Auswahl sollte nur auf der Registerkarte **Zusammenfassung** erscheinen | Das Dropdown-Feld für die **Periode**-Auswahl wird jetzt nur angezeigt, wenn die Registerkarte **Zusammenfassung** im Arbeitsbereich „Leistungen“ aktiv ist, und nicht in den Bereichen **Prozessergebnisse** und **Links**. |
| 557336 | Arbeitsbereich des Vergütungsverwaltungs: **Anmeldung mit ausgecheckten Plänen öffnen** Text wird in der Kachelansicht abgeschnitten | Der Text in der Kachelansicht wurde in **Ausgecheckte Pläne...offene Anmeldung** geändert, um das Abschneiden von notwendigem Kontext zu vermeiden. |

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