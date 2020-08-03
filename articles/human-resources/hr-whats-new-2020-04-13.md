---
title: Neuigkeiten oder Änderungen in Dynamics 365 Human Resources (13. April, 2020)
description: Dieser Artikel beschreibt Funktionen, die in Microsoft Dynamics 365 Human Resources neu oder geändert wurden.
author: Darinkramer
manager: AnnBe
ms.date: 4/13/2020
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
ms.search.validFrom: 2020-04-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4f61283f3bab26f54d55ffe7cbea21b1201ed234
ms.sourcegitcommit: bd9ff0d28718d535356ffbe1cffaaf60310dd430
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/13/2020
ms.locfileid: "3555146"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-13-2020"></a>Neuigkeiten oder Änderungen in Dynamics 365 Human Resources (13. April, 2020)

Dieser Artikel beschreibt Funktionen, die entweder neu oder geändert in Dynamics 365 Human Resources sind. Änderungen gelten für Build-Nummer 8.1.3136. Die Zahlen in Klammern in einigen Überschriften beziehen sich zur Referenz auf die LCS-Supportnummern.

## <a name="new-production-release-cadence"></a>Neue Trittfrequenz für Produktionsfreigaben

Mit dem Release von dieser Woche wird die Veröffentlichungskadenz für die Personalabteilung von einem wöchentlichen Update auf ein zweiwöchentliches Update umgestellt. Um die Angleichung an sichere Bereitstellungspraktiken sicherzustellen und hohe Standards für Stabilität und Zuverlässigkeit des Dienstes aufrechtzuerhalten, dauert die Bereitstellung von Dienstaktualisierungen für alle Regionen jetzt zwei Wochen. Wir führen zusätzliche Tests und Überwachungen ein, um die erfolgreiche Bereitstellung in jeder Phase des Prozesses zu prüfen. Weitere Informationen zu der Veröffentlichungshäufigkeit finden Sie unter [Aktualisierungsprozess](hr-admin-setup-update-process.md).

## <a name="rounding-precision-field-isnt-editable-after-specifying-a-rounding-type-435616"></a>Das Rundungsgenauigkeitsfeld kann nach Angabe eines Rundungstyps (435616) nicht bearbeitet werden

Mit dieser Änderung wird das Feld **Rundungsgenauigkeit** jetzt verfügbar gemacht, nachdem Sie das Feld **Rundungsart** aktualisiert haben

## <a name="cant-edit-leave-enrollment-end-date-when-the-leave-plan-doesnt-have-accrual-periods-413628"></a>Das Enddatum der Urlaubsregistrierung kann nicht bearbeitet werden, wenn der Urlaubsplan keine Abgrenzungsfristen hat (413628)

Sie können jetzt das Enddatum der Registrierung bearbeiten, ohne die Fehlermeldung „Feldabgrenzungsdatum muss ausgefüllt werden“ erhalten.

## <a name="employment-entity-doesnt-sync-to-common-data-service-430834"></a>Die Beschäftigungseinheit wird nicht mit Common Data Service (430834) synchronisiert

Diese Änderung behebt ein Problem, mit dem die Beschäftigungsdaten nicht mit Common Data Service synchronisiert wurden nach dem Hinzufügen von finanziellen Dimensionen. 

## <a name="remove-multi-parenting-for-work-calendar-time-interval-entity-431775"></a>Entfernen Sie die mehrfachen übergeordneten Zuordnungen für die Entität Arbeitskalender-Zeitintervall (431775)

Entfernen Sie die mehrfachen übergeordneten Zuordnungen für die Entität **Arbeitskalender-Zeitintervall**.

## <a name="filter-with-cast-function-doesnt-work-on-odata-call-position-worker-assignment-entity-431699"></a>Filter mit CAST-Funktion funktioniert nicht bei OData-Aufruf Position Arbeitskraftzuweisungs-Entität (431699)

Dieses Update enthält eine Änderung, um Filter mit CAST-Funktion in OData für die Entität **Position -Arbeitskraftzuweisung** zuzulassen.

## <a name="in-preview"></a>In Vorschau

## <a name="leave-suspension"></a>Urlaub aussetzen

Sie können Urlaub und Abwesenheit in der Personalabteilung für einen Mitarbeiter aussetzen. Durch das Aussetzen des Urlaubs werden die Urlaubsrückstellungen für ausgewählte Urlaubstypen gestoppt. Wenn die Aussetzung erfolgt, nachdem eine Rückstellung bearbeitet wurde, führt die Aussetzung des Urlaubs zu einer anteiligen Anpassung des Urlaubssaldos des Mitarbeiters. Weitere Informationen finden Sie unter [Urlaub aussetzen](hr-leave-and-absence-suspend-leave.md).

## <a name="carry-forward-rules"></a>Vortragungsregeln

Sie können einen Vortragsabwesenheitstyp für Vortragssalden angeben, bei denen Vortragsanpassungen übertragen werden. Wenn ein Mitarbeiter beispielsweise 10 Tage vorzieht, können Sie für diese 10 Tage einen anderen Urlaubstyp auswählen. Weitere Informationen finden Sie unter [Konfigurieren Sie Urlaubs- und Abwesenheitstypen](hr-leave-and-absence-types.md).

## <a name="known-issues"></a>Bekannte Probleme

## <a name="employment-details-entity"></a>Anstellungsdetailsentität

Die Entität **Beschäftigungsdetail** wurde mit den folgenden Feldern aktualisiert:

- **PayFrequency**
- **Employment Category ID**
- **Employment Type**
- **EmploymentType ID**
- **Status Beschäftigungsvorteil**

Die Einrichtungsdaten für diese Felder hängen davon ab, dass das Leistungsmanagement im Arbeitsplatz **Funktionsverwaltung** aktiviert ist. Füllen oder aktualisieren Sie diese Felder nicht in der Entität **Beschäftigungsdetail**, da dies beim Import zu Fehlern führt.

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