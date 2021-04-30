---
title: Neuerungen oder Änderungen in Dynamics 365 Human Resources (28. Mai 2020)
description: Dieses Thema beschreibt Funktionen, die in Microsoft Dynamics 365 Human Resources für den 28. Mai 2020 neu sind oder geändert wurden.
author: andreabichsel
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 79026c6047f3a10366ef3b22d74caee13b371b66
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891960"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-28-2020"></a>Neuerungen oder Änderungen in Dynamics 365 Human Resources (28. Mai 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In diesem Thema werden die Funktionen beschrieben, die in Dynamics 365 Human Resources neu oder geändert wurden. Änderungen gelten für Build-Nummer 8.1.3287. Die Zahlen in Klammern in einigen Überschriften beziehen sich zur Referenz auf die LCS-Supportnummern.

## <a name="leaverequest-entity-doesnt-work-when-you-enable-multiple-types-per-leave-plan-447498"></a>Die LeaveRequest-Entität funktioniert nicht, wenn Sie mehrere Typen pro Urlaubsplan aktivieren (447498)

Mit dieser Änderung ist die **LeaveEnrollmentV2Entity** verfügbar, um den Fehler zu korrigieren, der auftritt, wenn Sie mehrere Urlaubstypen aktivieren.

## <a name="batch-contention-reduction-feature-preview-446619"></a>Funktion zur Reduzierung von Stapelkonflikten (Vorschau) (446619)

Wenn Sie diese Funktion aktivieren, können Sie eine Verringerung der Blockierung von Batch-Framework-Tabellen erwarten, während Sie Aufgaben auswählen und Jobs beenden.

## <a name="updateconflict-while-saving-worker-prevents-editing-a-record-in-people-427915"></a>UpdateConflict beim Speichern der Arbeitskraft verhindert das Bearbeiten eines Datensatzes in People (427915)

Diese Änderung behebt einen Fehler beim Hinzufügen einer neuen Arbeitskraft beim Aktualisieren der Adressinformationen und beim Ändern der Spracheinstellungen. In diesem einzigartigen Szenario wurde ein Fehler angezeigt, der darauf hinweist, dass der Datensatz nicht aktualisiert werden konnte. 

## <a name="unable-to-add-an-attachment-to-an-approved-leave-request-to-resubmit-425407"></a>Einer genehmigten Urlaubsanforderung kann kein Anhang hinzugefügt werden und neu eingereicht werden (425407)

Diese Änderung ermöglicht jetzt Anhänge zu genehmigten Urlaubsanträgen.

## <a name="user-can-enter-compensation-for-an-employee-in-a-different-legal-entity-form-409529"></a>Der Benutzer kann eine Vergütung für einen Mitarbeiter in einer anderen juristischen Person eingeben (409529)

Diese Änderung deaktiviert die Vergütungsoptionen, um die versehentliche Eingabe von Vergütungsdatensätzen für die falsche juristische Person zu verhindern.

## <a name="error-when-you-transfer-an-employee-and-the-worker-position-assignment-date-is-before-the-position-duration-429402"></a>Fehler beim Übertragen eines Mitarbeiters und das Datum der Zuweisung der Mitarbeiterposition liegt vor der Positionsdauer (429402)

Fehlermeldungen beim Übertragen eines Mitarbeiters in diesem Szenario wurden aktualisiert, um die zur Behebung des Problems erforderlichen Änderungen besser zu beschreiben.

## <a name="attachments-capabilities-in-employee-self-service-benefits-enrollment"></a>Funktionen für Anhänge in der Registrierung für Self-Service-Vorteile für Mitarbeiter
 
Jetzt können Sie während des Leistungsregistrierungsprozesses Anhänge für jeden Plan hinzufügen, für den sich der Mitarbeiter anmeldet. Sie können dann die Anhänge in Formular **Von der Arbeitskraft angeforderte Leistungen**.

## <a name="in-preview"></a>Vorschau

## <a name="human-resources-application-in-teams"></a>Human Resources Anwendung in Teams

Mitarbeiter können Abwesenheiten von der Arbeit mit Microsoft Teams anfordern. Sie können mit einem Bot interagieren, um Urlaubsanträge zu erstellen. Weitere Informationen finden Sie unter [Human Resources App in Teams](./hr-admin-teams-leave-app.md). 

## <a name="leave-suspension"></a>Urlaub aussetzen

Sie können Urlaub und Abwesenheit in der Personalabteilung für einen Mitarbeiter aussetzen. Durch das Aussetzen des Urlaubs werden die Urlaubsrückstellungen für ausgewählte Urlaubstypen gestoppt. Wenn die Aussetzung erfolgt, nachdem eine Rückstellung bearbeitet wurde, führt die Aussetzung des Urlaubs zu einer anteiligen Anpassung des Urlaubssaldos des Mitarbeiters. Weitere Informationen finden Sie unter [Urlaub aussetzen](hr-leave-and-absence-suspend-leave.md).

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a>Update der Benutzererfahrung, um anzuzeigen, dass die Ansammlung ausgesetzt ist (429550)

Die Benutzererfahrung zeigt nun an, dass das Ansammlung für einen Plan ausgesetzt wurde.

## <a name="coming-soon"></a>Bald verfügbar

## <a name="database-logging-in-preview-in-june"></a>Datenbankprotokollierung (in der Vorschau im Juni)

Mit der Datenbankprotokollierungsfunktion können Sie festlegen, welche Tabelle und Felder überwacht werden sollen. Außerdem können Sie die Ereignisse bestimmen, die die Änderungsverfolgung auslösen sollen. Es stehen Abfragefunktionen zur Verfügung, um diese Änderungen im Laufe der Zeit anzuzeigen.

## <a name="buy-and-sell-leave-in-preview-june-1"></a>Kauf und Verkauf von Urlaub (in der Vorschau am 1. Juni)

Einige Organisationen bieten eine Leistung, mit dem Mitarbeiter ihren Urlaub kaufen oder verkaufen können. Dieser Prozess wird häufig manuell verwaltet. Diese Funktion bietet eine automatisiertere Möglichkeit zur Verwaltung von Richtlinien und Anforderungen für die Personalabteilung und hilft, Fehler zu vermeiden und gleichzeitig den Urlaubsverwaltungsprozess zu optimieren. Weitere Informationen finden Sie hier:

- [Kauf- und Verkaufsurlaubsrichtlinien verwalten](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [Urlaub kaufen und verkaufen](hr-employee-self-service-buy-sell-leave.md)

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>Data Management Framework (DMF) Entitäten für das Leistungsmanagement
 
Leistungsverwaltungsentitäten geben frei. Mit DMF-Entitäten können Daten importiert und exportiert werden, um das Leistungsmanagement einfach zu konfigurieren. Zum Verschieben von Daten steht auch eine Vorlage für das Leistungsmanagement zur Verfügung. Die Vorlage exportiert und importiert die Daten nacheinander, um Datenabhängigkeiten zu berücksichtigen.

## <a name="add-reason-code-to-accrual-suspensions-june-1"></a>Ursachencode für Ansammlungsaussetzungen hinzufügen (1. Juni)

Ursachencodes, die der Ansammlungsaussetzung hinzugefügt wurden.

## <a name="carry-forward-rules-june-1"></a>Vortragungsregeln (1. Juni)

Sie können einen Vortragsabwesenheitstyp für Vortragssalden angeben, bei denen Vortragsanpassungen übertragen werden. Wenn ein Mitarbeiter beispielsweise 10 Tage vorzieht, können Sie für diese 10 Tage einen anderen Urlaubstyp auswählen. Weitere Informationen finden Sie unter [Konfigurieren Sie Urlaubs- und Abwesenheitstypen](hr-leave-and-absence-types.md).

## <a name="suspend-leave-accrual-for-specified-leave-types-june-1"></a>Urlaubsansammlung für angegebene Abwesenheitstypen aussetzen (1. Juni)

In dieser Version kann die Personalverwaltung eine Regel erstellen, um Abwesenheitsansammlungen für Mitarbeiter mit Abwesenheitsanträgen für unbezahlte Abwesenheit auszusetzen. Unbezahlte Abwesenheit kann ein Typ sein, muss es aber nicht sein. Sie können jede Abwesenheit basierend auf einem anderen Abwesenheitstyp aussetzen.

## <a name="dmf-entity-available-for-accrual-suspensions-june-1"></a>DMF-Entität verfügbar für Ansammlungsaussetzungen (1. Juni)

Eine DMF-Entität ist jetzt verfügbar für Ansammlungsaussetzungen.

## <a name="see-also"></a>Siehe auch

[Neuerungen oder Änderungen in Human Resources](hr-admin-whats-new.md)</br>
[Übersicht zu Dynamics 365 Human Resources 2019 Versionswelle 2 ](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Aktualisierungsprozess](hr-admin-setup-update-process.md)</br>
[Funktionen verwalten](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]