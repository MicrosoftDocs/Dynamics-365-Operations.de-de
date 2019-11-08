---
title: Neuerungen oder Änderungen in Dynamics 365 Talent (8. Oktober 2019)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 Talent entweder neu oder geändert sind.
author: Darinkramer
manager: AnnBe
ms.date: 10/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-10-08
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 159320dcbdf257862378b347172ef71832e293dc
ms.sourcegitcommit: deb87e518a151d8bb084891851a39758938a96e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/15/2019
ms.locfileid: "2626061"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-8-2019"></a>Neuerungen oder Änderungen in Dynamics 365 Talent (8. Oktober 2019)

[!include [banner](includes/banner.md)]

In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 Talent entweder neu oder geändert sind.

## <a name="changes-in-attract"></a>Änderungen in Attract

Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Änderungen in Onboard

Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Core HR-Änderungen

Die in diesem Abschnitt beschriebenen Änderungen gelten für Buildnummer 8.1.2542. Die Zahlen in Klammern in einigen Überschriften beziehen sich auf Supportnummern in Microsoft Dynamics Lifecycle Services (LCS).

### <a name="removal-of-benefits-open-enrollment-from-public-preview"></a>Entfernen der Vorteile eines offenen Registrierungsprozesses aus der öffentlichen Vorschau

In Verbindung mit unserer Ankündigung im Blogbeitrag zum Thema [„Strategische Investitionen in Core HR steigern die operative Exzellenz“](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence/) entfernt Microsoft die Funktion für Vorteile eines offenen Registrierungsprozesses aus der öffentlichen Vorschau ab dem 18. Oktober 2019. Stattdessen werden neue Funktionen in der Zukunft verwendet. Der Produktionsgebrauch von Vorteilen eines offenen Registrierungsprozesses, der gerade in der öffentlichen Vorschau enthalten ist, wird nicht unterstützt. 

### <a name="common-data-service-integration-is-now-turned-off-by-default-on-new-provisions-343675"></a>Common Data Service-Integration ist in neuen Bereitstellungen jetzt standardmäßig deaktiviert (343675)
 
Wenn neue Umgebungen bereitgestellt werden, ist die Common Data Service-Integration nun deaktiviert. Weitere Informationen finden Sie unter [Konfigurieren der Common Data Service-Integration](hr-common-data-service-integration.md).

### <a name="streamlined-employee-entry-and-navigation"></a>Fortschrittlicher Mitarbeitereintrag und ‑Navigation

Funktionen für Mitarbeitereingaben und Navigation sind jetzt in allen Umgebungen verfügbar. Um diese Funktion zu aktivieren, gehen Sie zu **Systemverwaltung \> Links \> Einstellungen \> Systemparameter \> Vorschaufunktionen** und wählen Sie **Verbessertes Arbeitskraftformular und Navigation** aus. Die Funktion wird dann für alle Benutzer aktiviert. Sie können diese Option jederzeit deaktivieren.

Weitere Informationen finden Sie unter [Fortschrittlicher Mitarbeitereintrag](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/streamlined-employee-data-entry) in Dynamics 365: Plan der 2. Veröffentlichungswelle 2019.

### <a name="issue-attract-and-onboard-create-inactive-workers-in-core-hr-380517"></a>Problem: Attract und Onboard erstellen inaktive Arbeitskräfte in Core HR (380517)

In der Version dieser Woche wurde ein Problem behoben, bei dem Attract und Onboard inaktive Arbeitskräfte in Core HR erstellen.

### <a name="issue-the-workflow-fails-when-the-manager-is-signed-in-to-another-company-while-terminating-an-employee-346852"></a>Problem: Der Workflow ist nicht erfolgreich, wenn der Manager bei einer anderen Firma angemeldet ist, wenn er einem Mitarbeiter kündigt (346852)

Der Workflow schlägt nicht mehr fehl auf Basis der juristischen Person, bei der der Manager angemeldet ist.

### <a name="issue-missing-information-on-hcmonboardingworkerchecklisttaskentity-349591"></a>Problem: Fehlende Informationen zu HcmOnboardingWorkerChecklistTaskEntity (349591)

Diese Version enthält weitere Informationen zu **HcmOnboardingWorkerChecklistTaskEntity**. Nachfolgend finden Sie einige Beispiele:

- **Gruppenname**, wenn der zugewiesene Typ **Gruppe** ist
- **Mitarbeitername**, wenn der zugewiesene Typ **Mitarbeiter** ist
- **Manangername**, wenn der zugewiesene Typ **Manager** ist

### <a name="issue-entities-arent-listed-in-alphabetical-order-in-common-data-service-administration-377414"></a>Problem: Entitäten werden nicht in alphabetischer Reihenfolge in der Common Data Service-Verwaltung aufgelistet (377414)

Entitäten werden jetzt in alphabetischer Reihenfolge auf der Seite **CDS-Verwaltung** aufgelistet.

### <a name="issue-changing-the-employment-type-with-a-future-date-doesnt-allow-a-position-assignment-339958"></a>Problem: Das Ändern des Beschäftigungstyps mit einem zukünftigen Datum ermöglicht keine Positionszuweisung (339958)

Diese Änderung ermöglicht Positionszuweisungen, wenn Arbeitskrafttypen geändert werden (z. B. von Mitarbeiter in Auftragnehmer).

### <a name="issue-updating-the-common-data-service-leave-bank-transaction-entity-creates-a-new-record-in-talent-352938"></a>Problem: Die Common Data Service-Entität Urlaubsbankbuchung erstellt einen neuen Datensatz in Talent (352938 )

Die Urlaubbuchung wird nun aktualisiert, wenn in Common Data Service Urlaubbankbuchungen aktualisiert werden.

### <a name="issue-the-title-of-attachments-for-feedback-items-shows-the-feedback-description-343765"></a>Problem: Der Titel der Anlagen für Rückmeldungsartikel zeigt die Rückmeldungsbeschreibung (343765)

Die Rückmeldungsbeschreibung wird nicht mehr im Anlagentitel angezeigt.

### <a name="issue-compensation-workflow-comments-field-shows-incorrect-content-339297"></a>Problem: Kommentarfeld des Kompensationsworkflows enthält falschen Inhalt (339297)

Diese Änderung zeigt den Inhalt des Feldes **%HcmActionState.HcmWorkerActionComment.Comments%** an.

### <a name="issue-workcalendarentity-and-workcalendardayentity-arent-exposed-through-odata-376329"></a>Problem: WorkCalendarEntity und WorkCalendarDayEntity werden nicht über OData verfügbar gemacht (376329)

In dieser Version sind **WorkCalendarEntity** und **WorkCalendarDayEntity** jetzt über Open Data Protocol (OData) verfügbar.

### <a name="issue-hcmworkerentity-is-slow-when-odata-is-used-375221"></a>Problem: HCMWorkerEntity ist langsam, wenn OData verwendet wird (375221)

Änderungen beeinträchtigen die Leistung von **HCMWorkerEntity**, wenn der Arbeitsmappen-Designer von Microsoft Excel verwendet wird.

### <a name="issue-manager-performance-journal-entry-shows-an-error-after-deleting-a-performance-journal-and-creating-a-new-one-336061"></a>Problem: Der Managerleistungsjournaleintrag zeigt einen Fehler an, nachdem eine Leistungserfassung gelöscht und eine neue erstellt wurde (336061)

Diese Version korrigiert ein Problem, das auftritt, nachdem eine Leistungserfassung gelöscht wurde und umgehend danach eine neue erstellt wurde. Die Korrektur ändert das Verhalten im Manager-Self-Service.

## <a name="coming-soon"></a>Bald verfügbar

### <a name="print-performance-reviews"></a>Leistungsbeurteilungen drucken

Weitere Informationen finden Sie unter [Leistungsbeurteilungen drucken](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) in Dynamics 365: Plan der 2. Veröffentlichungswelle 2019.
