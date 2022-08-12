---
title: Neuigkeiten oder Änderungen in Dynamics 365 Human Resources 5. April 2021
description: Dieser Artikel beschreibt Funktionen, die in Microsoft Dynamics 365 Human Resources für den 5. April 2021 neu sind oder geändert wurden.
author: marcelbf
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-04-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9388b2f43762bedf07c89a7a565935d2043ee90c
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9068000"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-5-2021"></a>Neuigkeiten oder Änderungen in Dynamics 365 Human Resources 5. April 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dieser Artikel beschreibt Funktionen, die in Dynamics 365 Human Resources neu oder geändert sind oder bald eingeführt werden.

Weitere Informationen zu unserem Aktualisierungsprozess und Zeitplan finden Sie unter [Aktualisierungsprozess](hr-admin-setup-update-process.md).

Weitere Informationen zu neuen Funktionen und den voraussichtlichen allgemeinen Verfügbarkeitsterminen finden Sie unter [Überblick Dynamics 365 Human Resources 2021 Veröffentlichungszyklus 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>In dieser Version

Diese Version enthält die folgenden neuen Funktionen und Fehlerbehebungen. Änderungen gelten für Build-Nummer 8.1.4074.

### <a name="new-features"></a>Neue Features

Die folgenden Funktionen sind in dieser Version allgemein verfügbar.

| Funktion | Freigabeplan | Dokumentation |
| --- | --- | --- |
| Einschränkung der Mitarbeiter bei der Bearbeitung von Geschäftskontaktdetails | [Einschränkung der Mitarbeiter bei der Bearbeitung von geschäftlichen Kontaktdetails](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/restrict-employees-editing-business-contact-details) | [Bearbeitung persönlicher Informationen beschränken](./hr-employee-self-service-restrict-editing.md)|

### <a name="bug-fixes"></a>Fehlerkorrekturen

Die folgenden Fehlerkorrekturen sind in diesem Release enthalten.

> [!NOTE]
> Unser Ziel ist es, Ihnen diese Informationen so schnell wie möglich zukommen zu lassen. Wir können diesen Artikel aktualisieren, um Fehlerbehebungen aufzunehmen, die es nach der Erstveröffentlichung dieses Artikels in den Build geschafft haben.

| Problemnummer | Problem |  Description |
| --- | --- | --- |
| 550852 | Das Schaltfläche **Genehmigung** überprüft keine im Formular **Überprüfen** festgelegten Pflichtfelder. | Wenn Sie ein Feld im Formular **Überprüfen** als Pflichtfeld festlegen und die Änderungen für die Managerrolle veröffentlicht, führt das Formular die Überprüfung nicht wie erwartet durch. |
| 559564 | Historische Arbeitskräfteaktivitäten für feste Vergütungsänderungen führen zu Fehlern für gekündigte Benutzer. | Arbeitskraftaktivitäten einer Vergütung eines ausgeschiedenen Mitarbeiters führt zu einem Fehler. Nachdem ein Mitarbeiter gekündigt wurde, gibt die Arbeitskräfteaktivität Beförderung vor der Kündigung einen Fehler aus. |
| 560074 | Das Dropdownmenü für die Beschäftigungskategorie filtern nicht nach **Arbeitskräftetyp** und zeigt Kategorien für Mitarbeiter und Auftragnehmer an. | Im Formular **Mitarbeiter** sollte die Dropdownliste **Beschäftigungskategorie** entweder Mitarbeiter- oder Auftragnehmerkategorien anzeigen, basierend auf dem Arbeitskrafttyp des Mitarbeiters. |
| 567388 | Einige der Informationen für neu erstellte Mitarbeiter werden nicht sofort mit der Tabelle **cdm_worker** in Dataverse synchronisiert. | Beim Erstellen eines neuen Mitarbeiterdatensatzes wird der neue Datensatz mit der Tabelle **cdm_worker** in Dataverse synchronisiert, aber nicht alle Eigenschaften sind im Dataverse-Datensatz enthalten. |
| 563837 | Funktionen, die in der Anzeige von Human Resources nicht verfügbar sind. | Einige Funktionen, die nicht für Human Resources gelten, werden in der Funktionsverwaltung angezeigt. Diese Funktionen werden jetzt aus der Liste der Funktionen entfernt, die in Human Resources aktiviert werden können. |

## <a name="in-preview"></a>Vorschau

Die folgenden neuen Funktionen stehen in der Vorschau zur Verfügung. Weitere Informationen zur Aktivierung oder Deaktivierung von Vorschaufunktionen finden Sie unter [Funktionen verwalten](hr-admin-manage-features.md).

| Funktion | Freigabeplan | Dokumentation |
| --- | --- | --- |
| Arbeitsbereich für Vorteilsverwaltung | [Arbeitsbereich für die Verwaltung von Zusatzleistungen (Vorschau)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Arbeitsbereich „Vorteilsverwaltung“](hr-benefits-management-workspace.md) |

## <a name="coming-soon"></a>Bald verfügbar

| Funktion | Informationen |
| --- | --- |
| Von einem Manager für seine Mitarbeiter eingegebene Qualifikationen können von einem Workflow automatisch genehmigt werden | Bald verfügbar. |
| Plattformupdate 10.0.17 (41) | Das Plattformupdate 10.0.17 soll mit dem nächsten Release am 19. April 2021 eingeführt werden. Weitere Informationen finden Sie unter [Plattform-Updates für Version 10.0.17 der Finanz- und Betriebs-Apps (April 2021)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-17.md). |

Eine vollständige Liste der geplanten Funktionen und ihrer geplanten Versionen finden Sie unter [Überblick über Dynamics 365 Human Resources 2021 Veröffentlichungszyklus 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Siehe auch

[Neuerungen oder Änderungen in Human Resources](hr-admin-whats-new.md)</br>
[Übersicht zu Dynamics 365 Human Resources 2021 Versionswelle 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Aktualisierungsprozess](hr-admin-setup-update-process.md)</br>
[Funktionen verwalten](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
