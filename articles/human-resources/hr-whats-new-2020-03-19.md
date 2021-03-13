---
title: Neuerungen oder Änderungen in Dynamics 365 Human Resources (19. März 2020)
description: Dieser Artikel beschreibt Funktionen, die in Microsoft Dynamics 365 Human Resources für den 19. März 2020 neu sind oder geändert wurden.
author: andreabichsel
manager: tfehr
ms.date: 03/19/2020
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
ms.search.validFrom: 2020-03-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6eddce5b8efa1d62dff3238a5a0b69510ed4c387
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127968"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-19-2020"></a>Neuerungen oder Änderungen in Dynamics 365 Human Resources (19. März 2020)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dieser Artikel beschreibt Funktionen, die entweder neu oder geändert in Dynamics 365 Human Resources sind. Änderungen gelten für Build-Nummer 8.1.3014. Die Zahlen in Klammern in einigen Überschriften beziehen sich zur Referenz auf die Supportnummern in Lifecycle Services (LCS).

## <a name="human-resources-environment-limits-are-now-based-on-updated-licensing-394595"></a>Die Umgebungsgrenzen für die Personalabteilung basieren jetzt auf einer aktualisierten Lizenzierung (394595).

Die Begrenzung der Anzahl der Umgebungen pro Projekt in Lifecycle Services (LCS) hat sich geändert. Die vorherige Grenze war zwei Umgebungen. Die Begrenzung der Anzahl von Produktions- und Sandkastenumgebungen, die Sie für die Personalabteilung in LCS erstellen können, basiert jetzt auf einer aktualisierten Lizenzierung. Abhängig von der Anzahl der erworbenen Lizenzen können Sie jetzt pro LCS-Projekt beliebig viele Umgebungen erstellen. Mit der neuen Lizenzierung, die am 1. Februar 2020 aktualisiert wurde, können Kunden zusätzliche Umgebungen erwerben. Weitere Informationen zu den Lizenzanforderungen für zusätzliche Umgebungen finden Sie unter [Dynamics 365-Lizenzierungshandbuch](https://dynamics.microsoft.com/pricing/#HumanResources).

## <a name="provide-cross-company-viewing-of-compensation-data-for-employees-and-managers-403904"></a>Unternehmensübergreifende Anzeige von Vergütungsdaten für Mitarbeiter und Manager (403904)

Diese Funktion aktivieren Sie im Arbeitsbereich **Funktionsverwaltung**. Weitere Informationen zu Vorschaufunktionen finden Sie unter [Vorschaufunktionen aktivieren oder deaktivieren](hr-admin-manage-features.md#enable-or-disable-preview-features).

Wenn Sie diese Funktion aktivieren, können Manager die Vergütung für direkte und erweiterte Berichte anzeigen, ohne sich bei der Beschäftigungsfirma anmelden zu müssen. Die vollständige Vergütungshistorie ist bei jedem angemeldeten Unternehmen verfügbar, auf das der Manager zugreifen kann. Weitere Informationen finden Sie unter [Self-Service-Übersicht für Mitarbeiter und Manager](hr-employee-manager-self-service-overview.md).

## <a name="enable-global-address-book-merge-functionality-427189"></a>Die Zusammenführungsfunktion für globale Adressbücher (427189) aktivieren

Sie können jetzt doppelte Adressbucheinträge zusammenführen, indem Sie die doppelten Datensätze auswählen und **Zusammenführen** auf der Seite **Globales Adressbuch** auswählen.

## <a name="unable-to-adjust-leave-balance-for-a-plan-with-no-accruals-that-was-created-with-the-multiple-leave-type-feature-on-419635"></a>Das Urlaubsguthaben für einen Plan ohne Rückstellungen, der mit der Funktion „Mehrere Urlaubstypen“ aktiviert wurde (419635), kann nicht angepasst werden.

Sie können jetzt Salden für Urlaubspläne anpassen, die mit der in der Funktionsverwaltung aktivierten Vorschaufunktion **Mehrere Urlaubstypen** erstellt wurden.

## <a name="primary-position-field-in-the-workerpositionassignmententity-when-an-employee-is-terminated-420774"></a>Feld für die primäre Position in der WorkerPositionAssignmentEntity, wenn ein Mitarbeiter gekündigt wird (420774)

Bei Mitarbeitern mit einem gekündigten Arbeitsverhältnis wird die primäre Position, die zum Zeitpunkt der Kündigung aktiv war, in der Entität angezeigt. Für Integrationen wird kein doppelter Datensatz mehr für die Mitarbeiterposition des Mitarbeiters erstellt. 

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

3.  Suchen Sie die Umgebung, die Sie aktualisieren möchten. Die Umgebung sollte dem **Umgebungsname** im Abschnitt **Common Data Service Information** im Formular **Über** in Human Resources entsprechen.

4.  Wählen Sie die Umgebung aus, um die Umgebungsdetails anzuzeigen.

5.  Wählen Sie auf der Aktivitätsleiste oben **Lösungen verwalten**. Ein neues Browserfenster wird geöffnet und navigiert zu **Dynamics 365 Admin Center** im Kontext Ihrer Umgebung.

6.  Wählen Sie in der Liste **Lösung** den Eintrag **Dynamics 365 Human Resources Anker**.

7.  Wählen Sie **Aktualisierung**, um die neueste Lösung anzuwenden.

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a>Die SharePoint-Vorschau funktioniert in einigen Umgebungen nicht.

Wenn die Dokumentvorschau für in SharePoint gespeicherte Dokumente nicht funktioniert, versuchen Sie das folgende Verfahren:

1. Stellen Sie sicher, dass dem Administrator-Benutzerkonto eine E-Mail mit dem Benutzerdatensatz zugeordnet ist. Diese Informationen können auf der Seite **Benutzer** angezeigt werden. Wenn E-Mail nicht eingerichtet ist, müssen Sie die E-Mail und den Anbieter mit dem OData-Excel-Add-In hinzufügen. Standardmäßig ist die E-Mail-Adresse im Excel-Design nicht vorhanden. Sie müssen das Excel-Design bearbeiten, alle Felder hinzufügen, anwenden und aktualisieren. Sobald Sie diese Schritte ausgeführt haben, können Sie das Administratorkonto aktualisieren.

2. Nachdem dem Administratorkonto ein E-Mail-Konto zugeordnet ist, melden Sie sich mit Administratorrechten bei der Personalabteilung an.

3. Greifen Sie auf einen Anhang in SharePoint zu, um die Dokumentvorschau zu starten.

4. Melden Sie sich mit einem anderen Benutzerkonto an, das Zugriff auf Anhänge hat, und überprüfen Sie, ob die Vorschau wie erwartet funktioniert.

## <a name="coming-soon"></a>Bald verfügbar

### <a name="platform-update-33"></a>Plattformupdate 33

- Ganzseitige Apps (Vorschau) – Diese Vorschaufunktion, für die Sie die Funktion Gespeicherte Ansichten aktivieren müssen, ermöglicht Power Apps und Apps von Drittanbietern, die über das Dashboard als ganzseitige Erlebnisse hinzugefügt werden.

- Gespeicherte Ansichten (Vorschau) – Diese Vorschaufunktion ermöglicht gespeicherte Ansichten, was eine erhebliche Verbesserung des Personalisierungssubsystems darstellt. Mit dieser Funktion können Benutzer mehrere benannte Sätze von Personalisierungen pro Seite haben. Sie können Ansichten auch für Sicherheitsrollen veröffentlichen.

- Optimiert ist eine vonr Filtererfahrung – Diese Funktion ermöglicht eine optimierte ist eine von Filtererfahrung, die die Eingabe mehrerer Filterwerte erleichtert, einen einfacheren Mechanismus zum Entfernen einzelner oder aller Filterwerte bietet und eine kompaktere und intuitivere Visualisierung von Filterwerten ist.

- Empfohlene Felder – Benutzer müssen häufig Felder zu einem Raster oder einer Seite hinzufügen. Dies kann bei so vielen verfügbaren Feldern schwierig sein. Anstatt eine große Liste durchsuchen zu müssen, kann das System mit dieser Funktion eine Reihe empfohlener Felder anzeigen, die darauf basieren, was andere Benutzer in ähnlichen Szenarien am häufigsten hinzufügen.

- Feste Standardaktionen in Rastern – Diese Funktion stellt sicher, dass die Standardaktion in einem Raster mit einer bestimmten Spalte in einem Raster verknüpft ist, unabhängig davon, ob diese Spalte verschoben oder ausgeblendet wird.

## <a name="new-production-release-cadence"></a>Neue Trittfrequenz für Produktionsfreigaben

Ab April wird die Veröffentlichungskadenz für die Personalabteilung von einem wöchentlichen Update auf ein zweiwöchentliches Update umgestellt. Dies stellt die Ausrichtung auf sichere Bereitstellungspraktiken sicher und gewährleistet hohe Standards für Stabilität und Zuverlässigkeit im Service. Wir führen zusätzliche Tests und Überwachungen ein, um die erfolgreiche Bereitstellung in jeder Phase des Prozesses zu überprüfen. Weitere Informationen zur Veröffentlichungshäufigkeit finden Sie unter [Aktualisierungsprozess](hr-admin-setup-update-process.md).

## <a name="in-preview"></a>Vorschau

Die folgenden Vorschaufunktionen sind am 3. Februar 2020 verfügbar:

- **Urlaubs- und Abwesenheitsfunktion** - Weitere Informationen finden Sie unter [Urlaub- und Abwesenheitsverwaltung, Vorschaufunktion](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **Vorschaufunktion für das Leistungsmanagement** – Weitere Informationen, einschließlich bekannter Probleme, finden Sie unter [Übersicht über das Leistungsmanagement](hr-benefits-management-overview.md).

## <a name="see-also"></a>Siehe auch

[Neuerungen oder Änderungen in Human Resources](hr-admin-whats-new.md)</br>
[Übersicht zu Dynamics 365 Human Resources 2019 Versionswelle 2 ](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Aktualisierungsprozess](hr-admin-setup-update-process.md)</br>
[Funktionen verwalten](hr-admin-manage-features.md)