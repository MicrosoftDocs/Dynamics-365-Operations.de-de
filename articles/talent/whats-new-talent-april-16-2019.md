---
title: Neuigkeiten oder Änderungen in Dynamics 365 Talent (16. April, 2019)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 Talent entweder neu oder geändert sind.
author: Darinkramer
manager: AnnBe
ms.date: 04/16/2019
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
ms.search.validFrom: 2019-04-16
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d9802848c90b2b1c8d5e3cb3280dfa6ebc948ff2
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527176"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-april-16-2019"></a>Neuigkeiten oder Änderungen in Dynamics 365 Talent (16. April, 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

In diesem Thema werden die Funktionen beschrieben, die in Dynamics 365 Talent neu oder geändert wurden.

## <a name="changes-in-attract"></a>Änderungen in Attract

### <a name="process-auditing"></a>Prozessüberwachung

Sie können nun die Änderungen nachverfolgen, die an den Kandidaten, den Stellenangeboten und den Stellenbewerbungen vorgenommen werden. Weitere Informationen finden Sie unter [Änderungen an den Rekrutierungsdaten vornehmen](process-auditing.md).

## <a name="changes-in-onboard"></a>Änderungen in Onboard

Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Core HR-Änderungen

Die in diesem Abschnitt beschriebenen Änderungen gelten für Buildnummer 8.1.2239. Zahlen in Klammern beziehen sich auf Supportnummern in Lifecycle Services (LCS).

### <a name="compensation-region-compensation-level-benefit-option-and-skill-type-entities-in-common-data-service-updated-to-include-customer-field-support"></a>Entitäten für Kompensationsregion, Kompensationsstufe, Vorteilsoption und Fähigkeitstypen in Common Data Service wurden aktualisiert, um Debitorenfeldsupport einzuschließen

Mit dieser Version wurden diese Common Data Service-Entitäten aktualisiert, um die Möglichkeit abzudecken, dass ein benutzerdefiniertes Feld einbezogen wird, das über Talent: Core HR eingeschlossen wird.

### <a name="powerbi-refresh-issues-314342"></a>PowerBI-Aktualisierungsproblem (314342)

Diese Änderung korrigiert ein Problem beim ordnungsgemäßen Aktualisieren von PowerBI-Berichten.

### <a name="unable-to-click-directly-through-on-transition-tasks-in-employee-self-service-303309"></a>Unmöglich, bei „Mitarbeiter im Self-Service“ direkt in die Übergangsaufgabe durchzuklicken (303309)

Diese Änderung ermöglicht es Benutzern mit der Rolle „Mitarbeiter“, Übergangsaufgaben aus der Talent-Aufgabenliste auszuwählen und zu aktualisieren.

### <a name="performance-feedback-email-message-updated-309615"></a>Leistungsrückmeldungs-E-Mail-Nachricht aktualisiert (309615)

Mit dieser Änderung wird eine Bestätigungsmeldung angezeigt, wenn das Feedback erfolgreich gesendet wird.

### <a name="missing-tables-in-word-template-308048"></a>Fehlende Tabellen in Wordvorlage (308048)

Mit dieser Änderung werden bei Erstellung einer Word-Dokumentvorlage mit Mitarbeiter- und Qualifikationsinformationen nur die Fähigkeiten für den ausgewählten Mitarbeiter im Word-Dokument angezeigt.

### <a name="when-applying-an-offboarding-checklist-an-error-is-displayed-299877"></a>Bei Anwendung einer Offboarding-Checkliste wird ein Fehler angezeigt. (299877)

Diese Änderung korrigiert ein Problem bei der Anwendung von Offboarding-Checklisten direkt aus dem Arbeitskraftformular.

## <a name="in-preview"></a>Vorschau

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>Ermöglichen Sie, dass Ursachencodes für Sonderurlaubstypen angegeben werden können

Organisationen brauchen möglicherweise zusätzliche Informationen zu Freizeitanforderungen. Sie können nun Ursachencodes für Sonderurlaubstypen definieren und Mitarbeiter aktivieren, damit sie einen Ursachencode für ihre Freizeitanforderungen auszuwählen können.

### <a name="require-reason-codes-for-certain-leave-types-on-time-off-requests"></a>Erfordert Ursachencodes für bestimmte Urlaubstypen bei Freizeitanforderungen

Organisationen brauchen ggf. bestimmte Ursachencodes für Sonderurlaubstypen, wenn Mitarbeiter Freizeit senden. Dies kann möglicherweise aufgrund der Unternehmensrichtlinie oder von gesetzlichen Vorgaben der Fall sein. Sie können nun angeben, welche Urlaubstypen einen Ursachencodes erfordern und Sie können von Mitarbeitern verlangen, dass sie einen Ursachencode für den Sonderurlaubstyp für ihre Freizeitanforderungen angeben.

### <a name="provide-leave-and-absence-transaction-list-for-hr"></a>Erstellen Sie Urlaub- und Abwesenheitsbuchungslisten für die Personalverwaltung

Nachverfolgung von Mitarbeiterfreizeit und Verständnis dafür, wie Freizeit berechnet wird, hilft nicht nur der Personalverwaltung, Fragen von Mitarbeitern zu beantworten sonder stellt auch sicher, dass die Freizeit für Mitarbeiter korrekt ist. Personalverwaltung besitzt nun eine neue Anzeige in den Transaktionen (Abgrenzungen, Zuschüsse, Regulierungen und Anforderungen), die die Gründe hinter den Salden anzeigen.

## <a name="coming-soon"></a>Bald verfügbar

### <a name="improvements-to-the-user-interface-for-duplicate-employee-check"></a>Verbesserungen zur Benutzeroberfläche, um doppelten Mitarbeiter zu überprüfen

Mit dieser Änderung werden Duplikate erkannt, während Sie Namenfelder eingeben, und ein Status zeigt, wie viele Duplikate gefunden wurden. Sie können die zur Verfügung gestellte Verknüpfung aktivieren, um eine neue Seite zu öffnen, um zu prüfen, ob die gefundene Übereinstimmung verwendet werden soll. Das Duplikatsformular wird nicht automatisch geöffnet, damit die Dateneingabe nicht unterbrochen wird.

### <a name="email-support-for-alerts"></a>E-Mail-Support für Warnungen

Mit der Plattformaktualisierung 25 für Finance and Operations können Benutzer Warnregeln erstellen, dass automatisch E-Mail-Benachrichtigungen an Kontakte gesendet werden, wenn dies von einem Ereignis ausgelöst wird.




[!INCLUDE[footer-include](../includes/footer-banner.md)]