---
title: Übersicht
description: Der Arbeitsbereich **Urlaub und Abwesenheit** in Dynamics 365 Human Resources bietet einen flexiblen Rahmen zum Erstellen neuer Urlaubspläne, Workflows zum Verwalten von Anfragen und eine intuitive Self-Service-Seite, auf der Mitarbeiter eine Freizeitanforderung beantragen können.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 493bc3abe82103541125914896252b2eae596b38
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/28/2020
ms.locfileid: "3091747"
---
# <a name="overview"></a>Übersicht

Dynamics 365 Human Resources hilft Ihnen dabei, Ihren Arbeitnehmern großartige Urlaubsleistungen zu bieten. Der Arbeitsbereich **Urlaub und Abwesenheit** bietet einen flexiblen Rahmen zum Erstellen neuer Urlaubspläne, Workflows zum Verwalten von Anfragen und eine intuitive Self-Service-Seite, auf der Mitarbeiter eine Freizeitanforderung beantragen können. Mithilfe von Analysen kann Ihr Unternehmen Urlaubsguthaben und -Verwendung für Ihre Urlaubspläne messen und überwachen.

## <a name="set-up-leave-and-absence"></a>Einrichten von Urlaub und Abwesenheit

Bevor Sie Urlaubspläne für Ihre Mitarbeiter erstellen können, müssen Sie einige Einrichtungsschritte ausführen:

- [Urlaub- und Abwesenheitsparameter konfigurieren](hr-leave-and-absence-parameters.md)
- [Einen Arbeitszeitkalender erstellen](hr-leave-and-absence-working-time-calendar.md)
- [Einen Urlaubsanforderungsworkflow erstellen](hr-leave-and-absence-workflow.md)

## <a name="create-and-manage-leave-plans"></a>Dient zum Erstellen und Verwalten von Abwesenheitsplänen

Bevor Sie Urlaubspläne für Ihre Mitarbeiter erstellen, müssen Sie Urlaubs- und Abwesenheitsarten erstellen. Nachdem Sie einen Urlaubsplan erstellt haben, können Sie Mitarbeiter für den Plan registrieren. Sie können auch den Abgrenzungsprozess ausführen, Warnungen erstellen und Analysen für Ihre Pläne anzeigen.

- [Urlaubs- und Abwesenheitstypen konfigurieren](hr-leave-and-absence-types.md)
- [Einen Urlaubs- und Abwesenheitsplan erstellen](hr-leave-and-absence-plans.md)
- [Eine Arbeitskraft einem Urlaubsplan zuweisen](hr-leave-and-absence-enroll.md)
- [Urlaubs- und Abwesenheitspläne antizipieren](hr-leave-and-absence-accrue.md)
- [Analyse für Urlaub und Abwesenheit anzeigen](hr-leave-and-absence-analytics.md)

## <a name="request-time-off-and-manage-requests"></a>Freistellung beantragen und Anfragen verwalten

Ihre Mitarbeiter können Freizeitanträge einreichen und Sie können sie im Arbeitsbereich **Mitarbeiter Selbstservice** verwalten.

- [Arbeitsfreie Zeit anfordern](hr-employee-self-service-request-time-off.md)
- [Urlaubs- und Abwesenheitsanforderungen verwalten](hr-employee-self-service-manage-requests.md)

## <a name="leave-and-absence-preview-features"></a>Vorschaufunktionen für Urlaub und Abwesenheit

Sie können neue Funktionen für die Vorschau von Abwesenheiten und Urlaubszeiten in einer **Sandkasten** Umgebung ausprobieren. Weitere Informationen zum Aktivieren von Vorschaufunktionen finden Sie unter [Funktionen verwalten](hr-admin-manage-features.md). Die Vorschaufunktionen umfassen:

- **Urlaubs‑ und Abwesenheitskalender** – die Parameter für Urlaub und Abwesenheit befinden sich nicht mehr unter **Personalverwaltungsparameter**, sondern auf einem neuen Bildschirm namens **Urlaubs‑ und Abwesenheitsparameter**. Der neue Bildschirm enthält eine neue Registerkarte **Kalender**. Diese Vorschau ermöglicht nur eine Teilmenge der Parameter. Sie können den neuen Bildschirm über die Registerkarte **Links** im Arbeitsbereich **Urlaub und Abwesenheit** aufrufen. Die Kalender beinhalten:
  - **Firmenkalender** – zeigt alle Freizeitanforderungen der Mitarbeiter an. Menschen mit der Rolle **Personalverwaltung** können auf diesen Kalender über die Registerkarte **Links** im Arbeitsbereich **Urlaub und Abwesenheit** zugreifen.
  - **Manager-Teamkalender** – zeigt alle Freizeitanforderungen von Mitarbeitern an. Manager können über die Registerkarte **Mein Team** im Mitarbeiter-Self-Service unter **Urlaub und Abwesenheit** auf den Kalender zugreifen. 

- **Urlaubs‑ und Abwesenheitskalender** – Urlaubstypen enthalten eine neue Option **Feiertag**, die in Verbindung mit dem Arbeitszeitkalender verwendet wird. Tage, die durch Feiertage und Schließungen definiert sind, werden jetzt als **Feiertag** bezeichnet, wenn Arbeitstage generiert werden. Bei der Verarbeitung von Rückstellungen werden die dem Kalender zugewiesenen Mitarbeiter angepasst, um die auf einen Arbeitstag fallenden Feiertage zu berücksichtigen.

- **Überwachen von Urlaubsrückstellung** – In einem neuen Bildschirm können Sie überprüfen, wann Rückstellungen verarbeitet und gelöscht wurden, sowohl von allen Mitarbeitern als auch von einzelnen Mitarbeitern. Sie können diesen neuen Bildschirm über die Registerkarte **Links** im Arbeitsbereich **Urlaub und Abwesenheit** aufrufen.

- **Löschen von Urlaubsrückstellung** – Sie können jetzt Rückstellungsdatensätze für bestimmte Urlaubspläne löschen. Sie können diese neue Option über die Registerkarte **Links** im Arbeitsbereich **Urlaub und Abwesenheit** aufrufen. Für einzelne Mitarbeiter erscheint diese Option in der Gruppierung **Urlaub und Abwesenheit** im Mitarbeiterprofil. 

- **Runden von Urlaubsrückstellung** – Neue Optionen für **Urlaubstyp** definieren, welche Rundungsart für die Rückstellung verwendet werden soll, sowie die Dezimalgenauigkeit der Rundung während des Rückstellungsprozesses. Bei der Verarbeitung von Rückstellungen werden Rundung und Genauigkeit auf die Rückstellungsdatensätze angewendet. 

- **Mehrere Urlaubstypen in einem einzigen Urlaubsplan konfigurieren** – In einer neuen Spalte im Urlaubsrückstellungsplan für Urlaubstypen können Sie mehrere Urlaubstypen in einem Urlaubs‑ und Abwesenheitsplan mit unterschiedlichen Rückstellungsplänen definieren. Der vorherige Feld **Urlaubstyp** wird entfernt. Bei der Mitarbeiterregistrierung werden die Salden für die Urlaubstypen jetzt in einer Tabelle angezeigt und nicht mehr oben auf dem Bildschirm.

  > [!IMPORTANT]
  > Sie können diese Funktion nicht deaktivieren, nachdem Sie sie aktiviert haben.

- **Vollzeitäquivalent (FTE) eines Mitarbeiters für die Rückstellung verwenden** – Eine neue Spalte im Urlaubsrückstellungsplan ermöglicht die Verwendung des FTE für die Rückstellung. Bei der Verarbeitung von Rückstellungen verwendet die Anwendung die primäre Position des Mitarbeiters und das definierte FTE, um den anteiligen Rückstellungsbetrag zu bestimmen.

  > [!NOTE]
  > Diese Funktion ist nur verfügbar, wenn Sie **Mehrere Urlaubstypen pro Urlaubsplan konfigurieren** aktivieren. 
