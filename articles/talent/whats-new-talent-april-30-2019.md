---
title: Neuigkeiten oder Änderungen in Dynamics 365 Talent (30. April, 2019)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 Talent entweder neu oder geändert sind.
author: Darinkramer
manager: AnnBe
ms.date: 04/30/2019
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
ms.search.validFrom: 2019-04-30
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 38158948dbcf8966edf49bcce5b1e5da7eddb8dc
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2019
ms.locfileid: "2026035"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-april-30-2019"></a>Neuigkeiten oder Änderungen in Dynamics 365 Talent (30. April, 2019)

[!include [banner](includes/banner.md)]

In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 Talent entweder neu oder geändert sind.

## <a name="changes-in-attract"></a>Änderungen in Attract

Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Änderungen in Onboard

Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Core HR-Änderungen

Die in diesem Abschnitt beschriebenen Änderungen gelten für Buildnummer 8.1.2270. Die Zahlen in Klammern in einigen Überschriften beziehen sich auf Supportnummern in Microsoft Dynamics Lifecycle Services (LCS).

### <a name="provide-feedback"></a>Feedback geben

Die Option, zum Bereitstellen von Feedback befindet sich im Menü **Hilfe** (**?**) in Talent. Dieses Menü bietet Zugriff auf den folgenden Ressourcen:

- Feedback
- Hilfe
- Erste Schritte
- Unterstützung
- Ideen
- Info

### <a name="improvements-to-the-user-interface-for-duplicate-employee-detection"></a>Verbesserungen an der Benutzeroberfläche, um doppelten Mitarbeiter zu erkennen

Aufgrund dieser Änderung werden Duplikate nun beim Festlegen von Namensfeldern erkannt und eine Statusanzeige zeigt die Anzahl der Duplikate an, die erfasst wurden. Ein bereitgestellter Link öffnet eine Seite, auf der Sie bewerten können, ob Sie eines der Duplikate verwenden sollen. Die Duplikatsseite wird nicht automatisch geöffnet, damit die Dateneingabe nicht unterbrochen wird. Sie müssen den Link auswählen, um die Seite zu öffnen.

### <a name="common-data-service-entity-support-for-custom-fields"></a>Common Data Service-Entitätssupport für benutzerdefinierte Felder

In der Version dieser Woche unterstützen die folgenden Entitäten nun benutzerdefinierte Felder: Anstellung, Vorteilstyp und Lohnzyklus.

### <a name="an-error-occurs-when-an-off-boarding-checklist-is-assigned-299877"></a>Ein Fehler tritt auf, wenn eine Offboarding-Checkliste zugeordnet wird (299877 )

Mit dieser Änderung wird eine Fehlermeldung korrigiert, die angezeigt wird, wenn Sie einem Mitarbeiter außerhalb des Kündigungsprozesses eine Offboarding-Checkliste zuweisen.

### <a name="the-exited-workers-link-opens-the-wrong-worker-309939"></a>Der Link für beendete Arbeitskräfte öffnet die falsche Arbeitskraft (309939)

Mit dieser Änderung wird ein Problem behoben, das auftritt, wenn Sie einen Mitarbeiter aus einer anderen juristischen Person neu anwerben und versuchen, aus der Liste der beendeten Arbeitskräfte zu dem Mitarbeiter zu wechseln.

### <a name="the-employee-self-service-compensation-card-doesnt-show-summary-values-when-advanced-security-is-turned-on-315231"></a>Die Mitarbeiter-Self-Service-Kompensationskarte zeigt keine Zusammenfassungswerte an, wenn die erweiterte Sicherheit eingeschaltet wird (315231 )

Mit dieser Änderung wird ein Problem behoben, das auftritt, wenn Sie erweiterte Kompensationssicherheit verwenden. Wenn die erweiterte Sicherheit aktiviert ist, zeigt der Mitarbeiter-Self-Service nun die zusammengefassten Kompensationsbeträge für Mitarbeiter und Manager an. Vor dieser Änderung wurden zusammenfassende Werte als 0 (null) angezeigt.

### <a name="if-a-position-without-a-title-is-created-in-common-data-service-no-position-is-created-in-talent-314562"></a>Wenn eine Position ohne einen Titel in Common Data Service erstellt wird, wird keine Position im Talent erstellt(314562)

Mit den Änderungen dieser Woche wird ein Problem behoben, das auftritt, wenn Sie Positionen in Common Data Service erstellen, jedoch keinen Titel hinzufügen.

### <a name="error-message-in-performance-journal-entries-in-employee-self-service-314134"></a>Fehlermeldung in den Leistungsjournaleinträgen im Mitarbeiter-Self-Service (314134 )

Mit dieser Änderung wird ein Problem behoben, das auftritt, wenn Sie den Leistungsjournaleinträgen Leistungsziele im Mitarbeiter-Self-Service zuordnen.

## <a name="in-preview"></a>Vorschau

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>Ermöglichen Sie, dass Ursachencodes für Sonderurlaubstypen angegeben werden können

Organisationen brauchen möglicherweise zusätzliche Informationen zu Freizeitanforderungen. Sie können nun Ursachencodes für Sonderurlaubstypen definieren und Mitarbeiter aktivieren, damit sie einen Ursachencode für ihre Freizeitanforderungen auszuwählen können.

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>Erfordert Ursachencodes für bestimmte Urlaubstypen bei Freizeitanforderungen

Organisationen brauchen ggf. bestimmte Ursachencodes für Sonderurlaubstypen, wenn Mitarbeiter Freizeit beantragen. Diese Anforderung ist möglicherweise aufgrund der Unternehmensrichtlinie oder der gesetzlichen Vorgaben vorhanden. Sie können nun angeben, welche Urlaubstypen einen Ursachencodes erfordern und Sie können von Mitarbeitern verlangen, dass sie einen Ursachencode für den Sonderurlaubstyp für ihre Freizeitanforderungen angeben.

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>Erstellen Sie eine Urlaub- und Abwesenheitsbuchungsliste für die Personalverwaltung

Die Möglichkeit zum Nachverfolgen von Mitarbeiterfreizeit und ein Verständnis dafür, wie Freizeit berechnet wird, hilft nicht nur der Personalverwaltung, Fragen von Mitarbeitern zu beantworten sondern garantiert auch, dass die Freizeit für Mitarbeiter korrekt ist. Personalverwaltung besitzt nun eine neue Anzeige in den Transaktionen (Abgrenzungen, Zuschüsse, Regulierungen und Anforderungen), sodass die Mitarbeiter der Personalverwaltung die Gründe hinter den Salden anzeigen können.

## <a name="coming-soon"></a>Bald verfügbar

### <a name="email-support-for-alerts"></a>E-Mail-Support für Warnungen

In Platform update 26 für Finance and Operations können Benutzer Warnregeln erstellen, dass automatisch E-Mail-Benachrichtigungen an Kontakte gesendet werden, wenn dies von einem Ereignis ausgelöst wird.
