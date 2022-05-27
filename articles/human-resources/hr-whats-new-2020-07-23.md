---
title: Neuerungen und Änderungen in Dynamics 365 Human Resources (23. Juli 2020)
description: Dieses Thema beschreibt Funktionen, die in Microsoft Dynamics 365 Human Resources für den 23. Juli 2020 neu sind oder geändert wurden.
author: andreabichsel
ms.date: 07/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-07-23
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: baf92234bc63449435324cc2d199a0529e53857a
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8692029"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-23-2020"></a>Neuerungen und Änderungen in Dynamics 365 Human Resources (23. Juli 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



In diesem Thema werden die Funktionen beschrieben, die in Dynamics 365 Human Resources neu oder geändert wurden. Änderungen gelten für Build-Nummer 8.1.3416. Die Zahlen in Klammern in einigen Überschriften beziehen sich zur Referenz auf die LCS-Supportnummern.

## <a name="deleting-financial-dimensions-on-a-position-doesnt-work-as-expected-445476"></a>Das Löschen von Finanzdimensionen für eine Position funktioniert nicht wie erwartet (445476)

Durch das Entfernen von Dimensionen aus einer Position werden jetzt dieselben Positionen aus Dataverse entfernt.

## <a name="positions-not-in-hierarchy-show-inactive-positions-397257"></a>Nicht in der Hierarchie enthaltene Positionen zeigen inaktive Positionen (397257)

Inaktive Positionen (mit abgelaufener Dauer) werden in der Positionshierarchie nicht mehr als **Positionen nicht in Hierarchie** angezeigt. 

## <a name="validation-occurring-between-leaveenrollmententity-and-hcmworkerentity-on-data-management-framework-dmf-import-causes-slow-data-loads-442324"></a>Die Prüfung zwischen LeaveEnrollmentEntity und HcmWorkerEntity bei Importen im Datenverwaltungsframework (DMF) führt zu langsamen Datenladevorgängen (442324)

Änderungen in diesem Release erhöhen die Leistung von **LeaveEnrollmentEntity**.

## <a name="unable-to-personalize-in-organization-administration-447490"></a>Personalisierung in der Organisationsverwaltung nicht möglich (447490)

Mit dieser Änderung können Sie jetzt die Links in der **Organisationsverwaltung** personalisieren.

## <a name="in-preview"></a>Vorschau

## <a name="mandatory-fields"></a>Pflichtfelder 

Mithilfe der Personalisierungsfunktionen für die Personalabteilung können Sie Felder jetzt zu Pflichtfeldern machen. Diese Funktion erfordert **Gespeicherte Ansichten**.

## <a name="human-resources-application-in-teams"></a>Human Resources Anwendung in Teams

Mitarbeiter können Abwesenheiten von der Arbeit mit Microsoft Teams anfordern. Sie können mit einem Bot interagieren, um Urlaubsanträge zu erstellen. Weitere Informationen finden Sie unter [Human Resources App in Teams](./hr-admin-teams-leave-app.md). 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>Data Management Framework (DMF) Entitäten für das Leistungsmanagement
 
Leistungsverwaltungsentitäten geben frei. Mit DMF-Entitäten können Daten importiert und exportiert werden, um so das Leistungsmanagement einfach zu konfigurieren. Zum Verschieben von Daten steht auch eine Vorlage für das Leistungsmanagement bereit. Die Vorlage exportiert und importiert die Daten nacheinander, um die Datenabhängigkeiten zu berücksichtigen.

## <a name="buy-and-sell-leave"></a>Urlaub kaufen und verkaufen 

Einige Organisationen bieten eine Leistung, mit dem Mitarbeiter ihren Urlaub kaufen oder verkaufen können. Dieser Prozess wird häufig manuell verwaltet. Diese Funktion automatisiert die Verwaltung von Richtlinien und Anforderungen für die Personalabteilung. Es rationalisiert den Urlaubsmanagementprozess und hilft, Fehler zu beseitigen. Weitere Informationen finden Sie hier:

- [Kauf- und Verkaufsurlaubsrichtlinien verwalten](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [Urlaub kaufen und verkaufen](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a>Hinterlassen Sie die Rückstellung für ein einzelnes Unternehmen oder einen einzelnen Plan

Kunden können Rückstellungen für ein einzelnes Unternehmen oder einen einzelnen Urlaubs- und Abwesenheitsplan bearbeiten. Diese Fähigkeit bietet Kunden mit unterschiedlichen Urlaubsjahren oder Urlaubsfälligkeitsrichtlinien Klarheit für den Fälligkeitsprozess. Weitere Informationen finden Sie unter [Urlaub pro Unternehmen oder pro Urlaubsplan](hr-leave-and-absence-accrue.md).

## <a name="add-attachments-to-time-off-requests"></a>Anhänge zu Abwesenheitsfragen hinzufügen

Die Möglichkeit, genehmigten Urlaubsanträgen Anhänge hinzuzufügen, ist in der aktuellen COVID-19-Umgebung von entscheidender Bedeutung. Mitarbeiter können diese Anhänge jetzt hinzufügen. Sie haben auch mehr Einblick, wie Aktualisierungen vorgenommen werden, um Anfragen zu hinterlassen. Weitere Informationen finden Sie unter [Fügen Sie einer vorhandenen Anforderung einen Anhang hinzu](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).

## <a name="add-reason-code-to-accrual-suspensions"></a>Ursachencode für Ansammlungsaussetzungen hinzufügen 

Ursachencodes, die der Ansammlungsaussetzung hinzugefügt wurden.

## <a name="carry-forward-rules"></a>Vortragungsregeln 

Sie können einen Vortragsabwesenheitstyp für Vortragssalden angeben, bei denen Vortragsanpassungen übertragen werden. Wenn ein Mitarbeiter beispielsweise 10 Tage vorzieht, können Sie für diese 10 Tage einen anderen Urlaubstyp auswählen. Weitere Informationen finden Sie unter [Konfigurieren Sie Urlaubs- und Abwesenheitstypen](hr-leave-and-absence-types.md).

## <a name="suspend-leave-accrual-for-specified-leave-types"></a>Urlaubsansammlung für angegebene Abwesenheitstypen aussetzen

Sie können eine Regel erstellen, um Abwesenheitsansammlungen für Mitarbeiter mit Abwesenheitsanträgen für unbezahlte Abwesenheit auszusetzen. Unbezahlte Abwesenheit kann ein Typ sein, muss es aber nicht sein. Sie können jede Abwesenheit basierend auf einem anderen Abwesenheitstyp aussetzen.

## <a name="dmf-entity-available-for-accrual-suspensions"></a>DMF-Entität verfügbar für Ansammlungsaussetzungen 

Eine DMF-Entität ist jetzt verfügbar für Ansammlungsaussetzungen.

## <a name="coming-soon"></a>Bald verfügbar

## <a name="checklist-entities-included-in-dataverse"></a>In Dataverse enthaltene Prüflistenentitäten

Prüflistenentitäten für Onboarding, Offboarding, Übergänge und Geschäftsprozesse werden in Kürze in Dataverse verfügbar sein.

## <a name="platform-changes"></a>Plattformänderungen

Plattformupdate 10.0.12 (36)

## <a name="see-also"></a>Siehe auch

[Neuerungen oder Änderungen in Human Resources](hr-admin-whats-new.md)</br>
[Übersicht zu Dynamics 365 Human Resources 2019 Versionswelle 2](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Aktualisierungsprozess](hr-admin-setup-update-process.md)</br>
[Funktionen verwalten](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]