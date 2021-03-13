---
title: Neuerungen und Änderungen in Dynamics 365 Human Resources (11. Juni 2020)
description: Dieses Thema beschreibt Funktionen, die in Microsoft Dynamics 365 Human Resources für den 11. Juni 2020 neu sind oder geändert wurden.
author: andreabichsel
manager: tfehr
ms.date: 06/16/2020
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
ms.search.validFrom: 2020-06-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6ff359f65afc03a1b5691fddc078f73682e99e44
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127800"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-11-2020"></a>Neuerungen und Änderungen in Dynamics 365 Human Resources (11. Juni 2020)

Dieser Artikel beschreibt Funktionen, die entweder neu oder geändert in Dynamics 365 Human Resources sind. Änderungen gelten für Build-Nummer 8.1.3316. Die Zahlen in Klammern in einigen Überschriften beziehen sich zur Referenz auf die LCS-Supportnummern.

## <a name="streamlined-employee-form-sometimes-causes-child-form-close-x-buttons-to-stop-working-442369"></a>Ein optimiertes Mitarbeiterformular führt manchmal dazu, dass die Schaltflächen zum Schließen des untergeordneten Formulars (X) nicht mehr funktionieren (442369)

Wenn das neue Formular **Arbeitskraft** aktiviert ist, funktioniert die Schaltfläche Schließen (**X**) gelegentlich nicht bei untergeordneten Formularen. Dieses Problem trat zeitweise auf. Sie können das Formular schließen, nachdem Sie es verlassen und wieder aufgerufen haben. Sie können beispielsweise links einen Menüpunkt auswählen und zurück zum Formular **Arbeitskraft** navigieren und dieses schließen. Die Veröffentlichung dieser Woche behebt dieses Problem. 

## <a name="the-worker-personal-contact-person-entity-doesnt-export-personal-contacts-with-a-parent-relationship-type"></a>Die Entität der persönlichen Kontaktperson des Arbeitnehmers exportiert keine persönlichen Kontakte mit einem übergeordneten Beziehungstyp

Mit dieser Version exportiert die **Persönlicher Ansprechpartner des Arbeitnehmers** alle Beziehungstypen.

## <a name="the-hcmpositionworkerassignmentv2entity-should-be-part-of-the-ceridian-payroll-integration-package-by-default-448506"></a>Die HcmPositionWorkerAssignmentV2Entity sollte standardmäßig Teil des Ceridian Payroll-Integrationspakets sein (448506)

Mit dieser Änderung ist die **HcmPositionWorkerAssignmentV2Entity** im Ceridian Payroll Integration Package enthalten.

## <a name="in-preview"></a>Vorschau

## <a name="database-logging"></a>Datenbankprotokollierung

Mit der Datenbankprotokollierungsfunktion können Sie festlegen, welche Tabelle und Felder überwacht werden. Außerdem können Sie die Ereignisse bestimmen, die die Änderungsverfolgung auslösen sollen. Sie verwenden Datenbankprotokollierungsfunktionen, um diese Änderungen im Laufe der Zeit anzuzeigen. Weitere Informationen finden Sie unter [Konfigurieren und verwalten Sie die Datenbankprotokollierung](hr-admin-database-logging.md).

## <a name="human-resources-application-in-teams"></a>Human Resources Anwendung in Teams

Mitarbeiter können Abwesenheiten von der Arbeit mit Microsoft Teams anfordern. Sie können mit einem Bot interagieren, um Urlaubsanträge zu erstellen. Weitere Informationen finden Sie unter [Human Resources App in Teams](https://go.microsoft.com/fwlink/?linkid=2127841). 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>Data Management Framework (DMF) Entitäten für das Leistungsmanagement
 
Leistungsverwaltungsentitäten geben frei. Mit DMF-Entitäten können Daten importiert und exportiert werden, um so das Leistungsmanagement einfach zu konfigurieren. Zum Verschieben von Daten steht auch eine Vorlage für das Leistungsmanagement bereit. Die Vorlage exportiert und importiert die Daten nacheinander, um die Datenabhängigkeiten zu berücksichtigen.

## <a name="buy-and-sell-leave"></a>Urlaub kaufen und verkaufen 

Einige Organisationen bieten eine Leistung, mit dem Mitarbeiter ihren Urlaub kaufen oder verkaufen können. Dieser Prozess wird häufig manuell verwaltet. Diese Funktion automatisiert die Verwaltung von Richtlinien und Anforderungen für die Personalabteilung. Es rationalisiert den Urlaubsmanagementprozess und hilft, Fehler zu beseitigen. Weitere Informationen finden Sie hier:

- [Kauf- und Verkaufsurlaubsrichtlinien verwalten](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [Urlaub kaufen und verkaufen](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a>Hinterlassen Sie die Rückstellung für ein einzelnes Unternehmen oder einen einzelnen Plan

Kunden können Rückstellungen für ein einzelnes Unternehmen oder einen einzelnen Urlaubs- und Abwesenheitsplan bearbeiten. Diese Fähigkeit bietet Kunden mit unterschiedlichen Urlaubsjahren oder Abgrenzungsrichtlinien Klarheit über den Abgrenzungsprozess. Weitere Informationen finden Sie unter [Urlaub pro Unternehmen oder pro Urlaubsplan](hr-leave-and-absence-accrue.md).

## <a name="add-attachments-to-time-off-requests"></a>Fügen Sie Anhänge zu Freizeitanfragen hinzu

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

## <a name="new-platform-capabilities"></a>Neue Plattformfunktionen 

Mithilfe der Personalisierung können Sie Felder obligatorisch machen. Für diese Funktion müssen Sie **Gespeicherte Ansichten** aktivieren.

## <a name="configure-the-name-of-employee-self-service"></a>Name des Mitarbeiter-Self-Service konfigurieren

In den Human Resources-Parametern ist eine neue Option verfügbar, mit der der Name des Mitarbeiter-Self-Service-Arbeitsbereichs auf Self-Service aktualisiert werden kann. 

## <a name="see-also"></a>Siehe auch

[Neuerungen oder Änderungen in Human Resources](hr-admin-whats-new.md)</br>
[Übersicht zu Dynamics 365 Human Resources 2019 Versionswelle 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Aktualisierungsprozess](hr-admin-setup-update-process.md)</br>
[Funktionen verwalten](hr-admin-manage-features.md)