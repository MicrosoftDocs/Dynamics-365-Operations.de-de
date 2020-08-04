---
title: Neuerungen oder Änderungen in Dynamics 365 Human Resources (3. März 2020)
description: Dieser Artikel beschreibt Funktionen, die in Microsoft Dynamics 365 Human Resources neu oder geändert wurden.
author: Darinkramer
manager: AnnBe
ms.date: 03/03/2020
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
ms.author: dkrame
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d85ce8ccfcd7f1b975244cc2f65535101013ac89
ms.sourcegitcommit: bd9ff0d28718d535356ffbe1cffaaf60310dd430
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/13/2020
ms.locfileid: "3555290"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-3-2020"></a>Neuerungen oder Änderungen in Dynamics 365 Human Resources (3. März 2020)

Dieser Artikel beschreibt Funktionen, die entweder neu oder geändert in Dynamics 365 Human Resources sind. Änderungen gelten für Build-Nummer 8.1.2955. Die Zahlen in Klammern in einigen Überschriften beziehen sich zur Referenz auf die LCS-Supportnummern.

## <a name="common-data-service-solution-is-now-available-with-the-following-changes"></a>Common Data Service Lösung ist jetzt mit den folgenden Änderungen verfügbar:

Eine neue Common Data Service Lösung wird in Kürze mit den folgenden Änderungen verfügbar sein:

| Beschreibung | Änderung |
| ----------------------------------------- | --- |
| **Stelle/Position** Entitätsänderungen | **Kompensationsregion** hinzugefügt</br>**Finanzdimensionen** hinzugefügt |
| **Arbeitskraft** Entitätsänderungen | **Namensfolge** hinzugefügt</br>**Arbeitet von zu Hause** hinzugefügt</br>**Sprache** hinzugefügt</br>**Dienstalterdatum** hinzugefügt</br>**Jahrestag** hinzugefügt</br>**Ursprüngliches Einstellungsdatum** hinzugefügt |
| **Beschäftigung** Entitätsänderungen | **Finanzdimensionen** hinzugefügt</br>**Kündigungsgrund** hinzugefügt</br>**Kündigungsdatum** umbenannt von **Übergangsdatum**</br>**Probezeitdatum** hinzugefügt |
| **Arbeitskraftadresse** Entitätsänderungen | **Straße** hinzugefügt</br>**Adresszeile 1**, **Adresszeile 2**, und **Adresszeile 3** als veraltet markiert |
| Neue variable Vergütung-Einrichtungsentitäten | **Plantyp für variable Vergütung**</br>**Plan für variable Vergütung**</br>**Übertragungsregeln**</br>**Variable Planstufe zur Vergütung** |
| Neue **Arbeitskraftkalender-Beschäftigung** Entität | **Arbeitkraftkalender-Entität** hinzugefügt |
| Neue **Lohnpositionsdetail** Entität | **Lohnpositionsdetail** hinzugefügt |
| Neue **Titel** Entität | **Titel** hinzugefügt. Die neue Einheit **Titel** wird in den Synchronisationsprozess zwischen Human Resources und Common Data Service einbezogen. Sie wird nicht zunächst von **Job-Position** oder **Job** Entitäten referenziert. |

In den nächsten Wochen werden diese Entitätsänderungen in allen Umgebungen verfügbar sein. So installieren Sie die neueste Common Data Service Lösung für Human Resources manuell:

1.  Gehen Sie zum [Power Platform Admin Center](https://admin.powerplatform.microsoft.com).

2.  Wählen Sie **Umgebungen** aus.

3.  Suchen Sie die Umgebung, die Sie aktualisieren möchten. Die Umgebung sollte dem **Umgebungsname** im Abschnitt **Common Data Service Information** im Formular **Über** in Human Resources entsprechen.

4.  Wählen Sie die Umgebung aus, um die Umgebungsdetails anzuzeigen.

5.  Wählen Sie auf der Aktivitätsleiste oben **Lösungen verwalten**. Ein neues Browserfenster wird geöffnet und navigiert zu **Dynamics 365 Admin Center** im Kontext Ihrer Umgebung.

6.  Wählen Sie in der Liste **Lösung** den Eintrag **Dynamics 365 Human Resources Anker**.

7.  Wählen Sie **Aktualisierung**, um die neueste Lösung anzuwenden.

## <a name="import-issues-with-the-leave-enrollment-data-entity-406082"></a>Importieren Sie Probleme mit der Entität Registrierungsdaten verlassen (406082)

Sie können jetzt einen Mitarbeiter in einen neuen Urlaubsplan des gleichen Typs einschreiben, sofern das neue Einschreibungsdatum nach dem abgelaufenen Einschreibungsdatum des vorherigen Plans liegt.

## <a name="issue-with-exporting-contribution-rates-in-the-401k-payrollworkerenrolledbenefitdetail-entity-in-dmf-420700"></a>Problem beim Exportieren von Beitragssätzen in der Entität 401k payrollWorkerEnrolledBenefitDetail in DMF (420700)

Diese Änderung korrigiert die Exportfunktionalität für die Entität **payrollWorkerEnrolledBenefitDetail**, um die aktuellen Werte für den Arbeitgeberbeitrag widerzuspiegeln.

## <a name="searching-in-the-streamlined-worker-form-causes-message-saying-person-field-must-be-filled-in-402525"></a>Die Suche im optimierten Arbeitskraft-Formular führt zu der Meldung, dass das Feld Person ausgefüllt werden muss (402525)

Wenn Sie nach einem Mitarbeiter suchen, erhalten Sie keine Nachricht mehr, dass Sie das Feld **Person** ausfüllen müssen.

## <a name="note-field-value-doesnt-render-on-the-add-more-skills-form-380134"></a>Beachten Sie, dass der Feldwert im Formular eitere Fähigkeiten hinzufügen (380134) nicht gerendert wird

Diese Änderung behebt ein Problem, wenn Sie das Formular **Fügen Sie weitere Fähigkeiten hinzu** in Employee Self Service personalisieren.

## <a name="multiple-fixed-compensation-plans-dont-expire-when-transferring-employees-389466"></a>Mehrere feste Vergütungspläne verfallen nicht, wenn Mitarbeiter versetzt werden (389466)

Mit dieser Änderung verfallen alle aktiven festen Vergütungsdatensätze für die alte Position am Übergangsdatum.

## <a name="in-preview"></a>Vorschau

Die folgenden Vorschaufunktionen wird am 3. Februar 2020 verfügbar:

- **Urlaubs- und Abwesenheitsfunktion** - Weitere Informationen finden Sie unter [Urlaub- und Abwesenheitsverwaltung, Vorschaufunktion](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **Vorschaufunktion für das Leistungsmanagement** – Weitere Informationen, einschließlich bekannter Probleme, finden Sie unter [Übersicht über das Leistungsmanagement](hr-benefits-management-overview.md).

## <a name="see-also"></a>Siehe auch

[Neuerungen oder Änderungen in Human Resources](hr-admin-whats-new.md)</br>
[Übersicht zu Dynamics 365 Human Resources 2019 Versionswelle 2 ](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Aktualisierungsprozess](hr-admin-setup-update-process.md)</br>
[Funktionen verwalten](hr-admin-manage-features.md)