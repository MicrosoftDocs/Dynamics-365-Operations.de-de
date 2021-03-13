---
title: Neuigkeiten oder Änderungen in Dynamics 365 Human Resources (3. April, 2020)
description: Dieser Artikel beschreibt Funktionen, die in Microsoft Dynamics 365 Human Resources für den 03. April 2020 neu sind oder geändert wurden.
author: andreabichsel
manager: tfehr
ms.date: 04/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-04-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b00ef61cdd7ceac6c6f57187a0e6c98e94c8cb71
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127920"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-3-2020"></a>Neuigkeiten oder Änderungen in Dynamics 365 Human Resources (3. April, 2020)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dieser Artikel beschreibt Funktionen, die entweder neu oder geändert in Dynamics 365 Human Resources sind. Änderungen gelten für Build-Nummer 8.1.3111. Die Zahlen in Klammern in einigen Überschriften beziehen sich zur Referenz auf die Supportnummern in Lifecycle Services (LCS).

## <a name="features-that-are-generally-available-the-week-of-april-6"></a>Funktionen, die in der Woche vom 6. April allgemein verfügbar sind

- **Funktion Urlaub und Abwesenheiten** - Weitere Informationen zu Urlaub und Abwesenheit finden Sie unter [Urlaubs- und Abwesenheitsübersicht](hr-leave-and-absence-overview.md).

- **Funktion Vorteilsverwaltung** - Weitere Informationen zur Vorteilsverwaltung finden Sie unter [Vorteilsübersicht](hr-benefits-management-overview.md).

## <a name="human-resources-environment-limits-are-now-based-on-updated-licensing-394595"></a>Die Umgebungsgrenzen für die Personalabteilung basieren jetzt auf einer aktualisierten Lizenzierung (394595).

Die Begrenzung der Anzahl der Umgebungen pro Projekt in LCS hat sich geändert. Die vorherige Grenze war zwei Umgebungen. Die Begrenzung der Anzahl von Produktions- und Sandkastenumgebungen, die Sie für die Personalabteilung in LCS erstellen können, basiert jetzt auf einer aktualisierten Lizenzierung. Abhängig von der Anzahl der erworbenen Lizenzen können Sie jetzt pro LCS-Projekt beliebig viele Umgebungen erstellen. Mit der neuen Lizenzierung, die am 1. Februar 2020 aktualisiert wurde, können Kunden zusätzliche Umgebungen erwerben. Weitere Informationen zu den Lizenzanforderungen für zusätzliche Umgebungen finden Sie unter [Dynamics 365-Lizenzierungshandbuch](https://dynamics.microsoft.com/pricing/#HumanResources).
 
## <a name="error-when-trying-to-delete-a-questionnaire-428603"></a>Fehler beim Löschen eines Fragebogens (428603)

Das Update dieser Woche behebt ein Problem, bei dem beim Versuch, einen Fragebogen zu löschen, der folgende Fehler angezeigt wird:

Ein unausgeglichenes X ++ TTSBEGIN/TTSCOMMIT-Paar wurde erkannt.

## <a name="performance-journal-and-professional-certificates-security-issue-428499"></a>Sicherheitsproblem mit Leistungsjournal und professionellen Zertifikaten (428499)

Diese Änderung schränkt die Sichtbarkeit sowohl von Leistungsjournalen als auch von Berufszertifikaten basierend auf den Unternehmen ein, auf die sie Zugriff haben. 

## <a name="the-abbreviation-for-quebec-and-manitoba-387510"></a>Die Abkürzung für Quebec und Manitoba (387510)

Die Startdaten wurden aktualisiert, um die korrekte Abkürzung für Manitoba und Quebec wiederzugeben.

## <a name="new-entities-available-in-data-management-framework"></a>Neue verfügbare Entitäten im Datenverwaltungsframework

Die folgenden Entitäten sind jetzt verfügbar. Wenn diese Entitäten nicht in der Entitätsliste aufgeführt sind, verwenden Sie die Option **Entitäten aktualisieren** unter **Framework-Parameter > Entitätseinstellungen > Entitätsliste aktualisieren**.

 - Buchung für Urlaubs- und Abwesenheitszeitkonto V2
 - Urlaubs- und Abwesenheitsregistrierung V2
 - Stufe des Urlaubs- und Abwesenheitsplans V2
 - Urlaubs- und Abwesenheitsplan V2

## <a name="dataverse-solution-is-now-available-with-the-following-changes"></a>Dataverse Lösung ist jetzt mit den folgenden Änderungen verfügbar:

| Beschreibung | Rückgeld |
| --- | --- |
| **Stelle/Position** Entitätsänderungen | <ul><li>**Kompensationsregion** hinzugefügt</li>|
| **Dimension der Jobposition** Entität hinzugefügt | <ul><li>**Finanzdimensionen** hinzugefügt</li>
| **Arbeitskraft** Entitätsänderungen | <ul><li>**Namensfolge** hinzugefügt</li><li>**Arbeitet von zu Hause** hinzugefügt</li><li>**Sprache** hinzugefügt</li><li>**Dienstalterdatum** hinzugefügt</li><li>**Jahrestag** hinzugefügt</li><li>**Ursprüngliches Einstellungsdatum** hinzugefügt</li></ul> |
| **Beschäftigung** Entitätsänderungen | <ul><li>**Finanzdimensionen** hinzugefügt</li><li>**Kündigungsgrund** hinzugefügt</li><li>**Kündigungsdatum** umbenannt von **Übergangsdatum**</li><li>**Probezeitdatum** hinzugefügt</li></ul> |
| **Arbeitskraftadresse** Entitätsänderungen | <ul><li>**Straße** hinzugefügt</li><li>**Adresszeile 1**, **Adresszeile 2**, und **Adresszeile 3** als veraltet markiert</li></ul> |
| Neue variable Vergütung-Einrichtungsentitäten | <ul><li>**Plantyp für variable Vergütung**</li><li>**Plan für variable Vergütung**</li><li>**Übertragungsregeln**</li><li>**Variable Planstufe zur Vergütung**</li></ul> |
| Neue **Arbeitskraftkalender-Beschäftigung** Entität | <ul><li>**Arbeitkraftkalender-Entität** hinzugefügt</li></ul> |
| Neue **Lohnpositionsdetail** Entität | <ul><li>**Lohnpositionsdetail** hinzugefügt</li></ul> |
| Neue **Titel** Entität | <ul><li>**Titel** hinzugefügt</li></ul>Die neue Entität **Titel** ist enthalten in Dataverse wird aber aktuell nicht aus den Entitäten **Berufliche Stellung** oder **Job** referenziert. |

> [!NOTE]
> Finanzielle Dimensionen für Positionen und Beschäftigung bieten eine Integration in eine Richtung für Aktualisierungen von der Personalabteilung bis Dataverse. Aktualisierungen der Finanzdimensionen werden derzeit nicht synchronisiert von Dataverse zu Human Resources.

In den nächsten Wochen werden diese Entitätsänderungen in allen Umgebungen verfügbar sein. So installieren Sie die neueste Dataverse Lösung für Human Resources manuell:

1.  Gehen Sie zum [Power Platform Admin Center](https://admin.powerplatform.microsoft.com).

2.  Wählen Sie **Umgebungen** aus.

3.  Suchen Sie die Umgebung, die Sie aktualisieren möchten. Die Umgebung sollte dem **Umgebungsname** im Abschnitt **Dataverse Information** im Formular **Über** in Human Resources entsprechen.

4.  Wählen Sie die Umgebung aus, um die Umgebungsdetails anzuzeigen.

5.  Wählen Sie auf der Aktivitätsleiste oben **Lösungen verwalten**. Ein neues Browserfenster wird geöffnet und navigiert zu **Dynamics 365 Admin Center** im Kontext Ihrer Umgebung.

6.  Wählen Sie in der Liste **Lösung** den Eintrag **Dynamics 365 Human Resources Anker**.

7.  Wählen Sie **Aktualisierung**, um die neueste Lösung anzuwenden.

## <a name="in-preview"></a>In Vorschau

## <a name="leave-suspension"></a>Urlaub aussetzen

Sie können Urlaub und Abwesenheit in der Personalabteilung für einen Mitarbeiter aussetzen. Durch das Aussetzen des Urlaubs werden die Urlaubsrückstellungen für ausgewählte Urlaubstypen gestoppt. Wenn die Aussetzung erfolgt ist, nachdem eine Rückstellung bearbeitet wurde, führt die Aussetzung des Urlaubs zu einer anteiligen Anpassung des Urlaubssaldos des Mitarbeiters. Weitere Informationen finden Sie unter [Urlaub aussetzen](hr-leave-and-absence-suspend-leave.md).

## <a name="carry-forward-rules"></a>Vortragungsregeln

Sie können einen Vortragsabwesenheitstyp für Vortragssalden angeben, bei denen Vortragsanpassungen übertragen werden. Wenn ein Mitarbeiter beispielsweise 10 Tage vorzieht, können Sie für diese 10 Tage einen anderen Urlaubstyp auswählen. Weitere Informationen finden Sie unter [Konfigurieren Sie Urlaubs- und Abwesenheitstypen](hr-leave-and-absence-types.md).

## <a name="coming-soon"></a>Bald verfügbar

## <a name="new-production-release-cadence"></a>Neue Trittfrequenz für Produktionsfreigaben

Ab April wird die Veröffentlichungskadenz für die Personalabteilung von einem wöchentlichen auf ein zweiwöchentliches Update umgestellt. Um die Angleichung an sichere Bereitstellungspraktiken sicherzustellen und hohe Standards für Stabilität und Zuverlässigkeit des Dienstes aufrechtzuerhalten, dauert die Bereitstellung von Dienstaktualisierungen für die Regionen jetzt zwei Wochen. Wir führen zusätzliche Tests und Überwachungen ein, um die erfolgreiche Bereitstellung in jeder Phase des Prozesses prüfen zu können. Weitere Informationen zu der Veröffentlichungshäufigkeit finden Sie unter [Aktualisierungsprozess](hr-admin-setup-update-process.md).

## <a name="known-issues"></a>Bekannte Probleme

## <a name="employment-detail-entity"></a>Anstellungsdetailsentität

Die Entität **Beschäftigungsdetail** wurde mit den folgenden Feldern aktualisiert: **PayFrequency**, **ID der Beschäftigungskategorie**, **Beschäftigungsverhältnis**, **EmploymentType ID**, und **Beschäftigungsstatus**. Die Einrichtungsdaten für diese Felder hängen davon ab, dass das Leistungsmanagement im Arbeitsplatz Funktionsverwaltung aktiviert ist. Diese Felder sollten nicht in der Entität **Beschäftigungsdetail** ausgefüllt oder aktualisiert werden, weil dies beim Import zu Fehlern führt.

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a>Die SharePoint-Vorschau funktioniert in einigen Umgebungen nicht.

Wenn die Dokumentvorschau für in SharePoint gespeicherte Dokumente nicht funktioniert, versuchen Sie das folgende Verfahren:

1. Stellen Sie sicher, dass dem Administrator-Benutzerkonto eine E-Mail mit dem Benutzerdatensatz zugeordnet ist. Diese Informationen können auf der Seite **Benutzer** angezeigt werden. Wenn E-Mail nicht eingerichtet ist, müssen Sie die E-Mail und den Anbieter mit dem OData-Excel-Add-In hinzufügen. Standardmäßig ist die E-Mail-Adresse im Excel-Design nicht vorhanden. Sie müssen das Excel-Design bearbeiten, alle Felder hinzufügen, anwenden und aktualisieren. Sobald Sie diese Schritte ausgeführt haben, können Sie das Administratorkonto aktualisieren.

2. Nachdem dem Administratorkonto ein E-Mail-Konto zugeordnet ist, melden Sie sich mit Administratorrechten bei der Personalabteilung an.

3. Greifen Sie auf einen Anhang in SharePoint zu, um die Dokumentvorschau zu starten.

4. Melden Sie sich mit einem anderen Benutzerkonto an, das Zugriff auf Anhänge hat, und überprüfen Sie, ob die Vorschau wie erwartet funktioniert.

## <a name="see-also"></a>Siehe auch

[Neuerungen oder Änderungen in Human Resources](hr-admin-whats-new.md)</br>
[Übersicht zu Dynamics 365 Human Resources 2019 Versionswelle 2 ](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Aktualisierungsprozess](hr-admin-setup-update-process.md)</br>
[Funktionen verwalten](hr-admin-manage-features.md)