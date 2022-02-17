---
title: Neuerungen oder Änderungen in Dynamics 365 Human Resources (25. Februar 2020)
description: Dieser Artikel beschreibt Funktionen, die in Microsoft Dynamics 365 Human Resources für den 25. Februar 2020 neu sind oder geändert wurden.
author: andreabichsel
ms.date: 02/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6f8a8795b1af59339e920281ffc46139fb9c45e2
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8061200"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-25-2020"></a>Neuerungen oder Änderungen in Dynamics 365 Human Resources (25. Februar 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Dieser Artikel beschreibt Funktionen, die entweder neu oder geändert in Dynamics 365 Human Resources sind. Änderungen gelten für Build-Nummer 8.1.2927. Die Zahlen in Klammern in einigen Überschriften beziehen sich zur Referenz auf die LCS-Supportnummern.

## <a name="enable-case-management-navigation-and-data-management-framework-dmf-entity-414754"></a>Aktivieren Sie die DMF-Entität (Case Management Navigation and Data Management Framework) (414754)

Diese Vorschaufunktion ermöglicht eine zusätzliche Navigation zu Fällen der Fallverwaltung. Sie können diese Vorschaufunktion im Arbeitsbereich **Funktionsverwaltung** aktivieren. Diese Menüpunkte erscheinen im Arbeitsbereich **Compliance** von Dynamics 365 Human Resources. Mit dieser Änderung kann die Personalabteilung auf Folgendes zugreifen:

- Alle Anfragen
- Meine Anfragen
- Meine offenen Anfragen
- Meine überfälligen Anfragen
- Per Workflow zugewiesene Anfragen

Zusammen mit diesen neuen Ansichten in Fällen, ist die **Falldetail** DMF-Entität ebenfalls verfügbar.

## <a name="enable-relationship-definitions-in-global-address-bbook-414762"></a>Aktivieren Sie Beziehungsdefinitionen in der globalen Adresse bBook (414762)

Beziehungen sind jetzt im globalen Adressbuch aktiviert. Vor der Veröffentlichung dieser Woche hat das **Beziehung** Faktenfeld alle systemdefinierten Beziehungen angezeigt. Jetzt können Sie diese Beziehungen auf der globalen Adressbuchseite definieren.

## <a name="a-position-can-be-removed-when-active-compensation-records-exist-for-the-position-414568"></a>Eine Position kann entfernt werden, wenn für die Position aktive Vergütungsdatensätze vorhanden sind (414568)

Bei dieser Änderung wird eine Warnung angezeigt, wenn Sie versuchen, eine Position zu löschen, und ein Mitarbeiter über einen aktiven Vergütungsdatensatz für dieselbe Position verfügt. In diesem Fall müssen Sie den festen Vergütungsdatensatz des Mitarbeiters aktualisieren, bevor Sie die Position entfernen.

## <a name="performance-review-workflow-occasionally-adds-sign-offs-from-people-who-are-not-part-of-the-process-414171"></a>Der Workflow zur Leistungsüberprüfung fügt gelegentlich Abmeldungen von Personen hinzu, die nicht Teil des Prozesses sind (414171)

Diese Änderung behebt ein Problem, bei dem zusätzliche Abmeldeteilnehmer zur Leistungsüberprüfung hinzugefügt werden.

## <a name="worker-position-assignment-not-created-in-dataverse-when-selected-on-the-new-worker-dialog-413479"></a>Arbeitskraftposition-Zuordnung nicht erstellt in Dataverse, wenn im Dialogfeld Neuer Mitarbeiter (413479) ausgewählt

Diese Änderung behebt ein Problem, wenn ein neuer Mitarbeiter eingestellt und die neue Einstellung einer Position über den Dialog **Neue Arbeitskraft** zugewiesen wird. Jetzt spiegelt sich die Positionszuweisung in Dataverse wider.

## <a name="coming-soon"></a>Bald verfügbar

### <a name="updated-dataverse-solution"></a>Aktualisierte Dataverse-Lösung

Eine neue Dataverse Lösung wird in Kürze mit den folgenden Änderungen verfügbar sein:

| Beschreibung | Änderung |
| ----------------------------------------- | --- |
| **Stelle/Position** Entitätsänderungen | **Kompensationsregion** hinzugefügt</br>**Finanzdimensionen** hinzugefügt |
| **Arbeitskraft** Entitätsänderungen | **Namensfolge** hinzugefügt</br>**Arbeitet von zu Hause** hinzugefügt</br>**Sprache** hinzugefügt</br>**Dienstalterdatum** hinzugefügt</br>**Jahrestag** hinzugefügt</br>**Ursprüngliches Einstellungsdatum** hinzugefügt |
| **Beschäftigung** Entitätsänderungen | **Finanzdimensionen** hinzugefügt</br>**Kündigungsgrund** hinzugefügt</br>**Kündigungsdatum** umbenannt von **Übergangsdatum**</br>**Probezeitdatum** hinzugefügt |
| **Arbeitskraftadresse** Entitätsänderungen | **Straße** hinzugefügt</br>**Adresszeile 1**, **Adresszeile 2**, und **Adresszeile 3** als veraltet markiert |
| Neue variable Vergütung-Einrichtungsentitäten | **Plantyp für variable Vergütung**</br>**Plan für variable Vergütung**</br>**Übertragungsregeln**</br>**Variable Planstufe zur Vergütung** |
| Neue **Arbeitskraftkalender-Beschäftigung** Entität | **Arbeitkraftkalender-Entität** hinzugefügt |
| Neue **Lohnpositionsdetail** Entität | **Lohnpositionsdetail** hinzugefügt |
| Neue **Titel** Entität | **Titel** hinzugefügt. Die neue Einheit **Titel** wird in den Synchronisationsprozess zwischen Human Resources und Dataverse einbezogen. Sie wird nicht zunächst von **Job-Position** oder **Job** Entitäten referenziert. |

In den nächsten Wochen werden diese Entitätsänderungen in allen Umgebungen verfügbar sein. So installieren Sie die neueste Dataverse Lösung für Human Resources manuell:

1.  Gehen Sie zum [Power Platform Admin Center](https://admin.powerplatform.microsoft.com).

2.  Wählen Sie **Umgebungen** aus.

3.  Suchen Sie die Umgebung, die Sie aktualisieren möchten. Dies sollte dem **Umgebungsname** im Abschnitt **Common Data Service Information** im Formular **Über** in Human Resources entsprechen.

4.  Wählen Sie die Umgebung aus, um die Umgebungsdetails anzuzeigen.

5.  Wählen Sie auf der Aktivitätsleiste oben **Lösungen verwalten**. Ein neues Browserfenster wird geöffnet und navigiert zu **Dynamics 365 Admin Center** im Kontext Ihrer Umgebung.

6.  Wählen Sie in der Liste **Lösung** den Eintrag **Dynamics 365 Human Resources Anker**.

7.  Wählen Sie **Aktualisierung**, um die neueste Lösung anzuwenden.

## <a name="in-preview"></a>Vorschau

Die folgenden Vorschaufunktionen wird am 3. Februar 2020 verfügbar:

- **Urlaubs- und Abwesenheitsfunktion** - Weitere Informationen finden Sie unter [Urlaub- und Abwesenheitsverwaltung, Vorschaufunktion](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **Vorschaufunktion für das Leistungsmanagement** – Weitere Informationen, einschließlich bekannter Probleme, finden Sie unter [Übersicht über das Leistungsmanagement](hr-benefits-management-overview.md).

## <a name="see-also"></a>Siehe auch

[Neuerungen oder Änderungen in Human Resources](hr-admin-whats-new.md)</br>
[Übersicht zu Dynamics 365 Human Resources 2019 Versionswelle 2 ](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Aktualisierungsprozess](hr-admin-setup-update-process.md)</br>
[Funktionen verwalten](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]