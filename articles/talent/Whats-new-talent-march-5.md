---
title: Neuerungen oder Änderungen in Dynamics 365 for Talent (5. März 2019)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 for Talent entweder neu oder geändert sind.
author: Darinkramer
manager: AnnBe
ms.date: 03/05/2019
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
ms.search.validFrom: 2019-03-05
ms.dyn365.ops.version: Talent
ms.openlocfilehash: fe24846ab98a75d474df045a62a72bfc41c64866
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/12/2019
ms.locfileid: "1741889"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-march-5-2019"></a>Neuerungen oder Änderungen in Dynamics 365 for Talent (5. März 2019)

[!include [banner](includes/banner.md)]

In diesem Thema werden die Funktionen beschrieben, die in Talent entweder neu oder geändert sind.

## <a name="changes-in-attract"></a>Änderungen in Attract

### <a name="extending-option-sets-in-attract"></a>Erweitern von Optionsätzen in Attract

In Attract gibt es mehrere Felder, die Optionssätze in Common Data Service sind. Neue Funktionen zur Erweiterung der Optionssätze eingeführt, beginnend mit dem Begründungsfeld **Ablehnung**, Feld **Beschäftigungstyp** und dem Feld **Dienstaltertyp**.

> [!IMPORTANT]
> Die Funktion zur Stellenausschreibung auf LinkedIn erfordert die Nutzung der Felder **Beschäftigungstyp** und **Dienstaltertyp** auf der Seite **Stellendetails**. Die Standardwerte in den Feldern werden von LinkedIn unterstützt und angezeigt, wenn die Stelle gebucht wird. Wenn Sie Stellen in LinkedIn veröffentlichen und die vorhandenen Optionssatzwerte für diese Felder ändern, wird die Stelle noch veröffentlicht, aber LinkedIn zeigt keine benutzerdefinierten Werte für **Beschäftigungstyp** und **Dienstaltertyp**.

## <a name="changes-in-onboarding"></a>Änderungen in Onboarding

### <a name="private-preview-for-onboard-teams"></a>Private Vorschau für Onboard-Teams
Sie können jetzt in der gesamten Organisation Vorlagen gemeinsam nutzen und leicht zusammenarbeiten. Weitere Informationen finden Sie unter [Bewährte Verfahren in der Organisation mit Onboard-Teams gemeinsam verwenden](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-talent/onboard/share-best-practices-teams).

### <a name="private-preview-for-assignee-placeholders"></a>Private Vorschau für Zuweisungsplatzhalter
Sie können Ihren Vorlagen anreichern, indem Sie Aktivitäten zu Rollen anstelle von Personen zuweisen. Die Rollen werden dann zum Zeitpunkt der Handbucherstellung Personen zugewiesen. Weitere Informationen finden Sie unter [Optimieren der Handbuchverwaltung durch Zuweisung von Aktivitäten zu Rollen](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-talent/onboard/assign-activities-roles).

## <a name="changes-in-core-hr"></a>Core HR-Änderungen
**Build 8.1.2178**

### <a name="configure-workflow-to-auto-approve-or-follow-workflow-when-an-hr-or-line-manager-submits-or-updates-time-off-requests"></a>Konfigurieren Sie Workflows für die Auto-Genehmigung oder folgen Sie Workflows, wenn ein Personalverwaltungsmitarbeiter von Anforderungen arbeitsfreier Zeit übermittelt oder aktualisiert
Neue Workflow-Bedingungen wurden hinzugefügt, um Urlaubsanforderungen automatisch genehmigen zu lassen, wenn sie an den Vorgesetzten eines Mitarbeiters oder zur Personalverwaltung übermittelt werden. Eine Möglichkeit, diese Auto-Genehmigung für einen Workflow zu erreichen ist die Aktivierung einer automatischen Aktivität zur Workflowgenehmigung.

Die folgenden Bedingungen wurden hinzugefügt:

- Übermittelt von - Wird verwendet, um die Systembenutzerkennung des Benutzers zu bewerten, der die Anforderung an den Workflow gesendet hat.
- Übermittelt im Auftrag von - Wird verwendet, um zu bewerten, ob die Urlaubsanforderung im Auftrag der Arbeitskraft gesendet wurde, die der Anforderung zugeordnet ist.
- Übermittelt von Personalverwaltung - Wird verwendet, um zu bewerten, ob der Systembenutzer, der die Anforderung an den Workflow gesendet hat, in einer Personalverwaltungsrolle ist.
- Übermittelt von Vorgesetztem - wird verwendet, um zu bewerten, ob der Benutzer, der die Urlaubsanforderung an den Workflow übermittelt hat, ein Positionshierarchiemanager der Arbeitskraft ist, die der Anforderung zugeordnet ist.

### <a name="enable-employee-fixed-compensation-for-future-position-assignments"></a>Feste Mitarbeitervergütung für zukünftige Positionszuweisungen aktivieren
Mitarbeiter werden üblicherweise mit einen zukünftigen Startdatum zu einer Organisation hinzugefügt. Diese Änderung ermöglicht das Definieren der festen Mitarbeitervergütung für Mitarbeiter mit zukünftigen Positionszuweisungen.

### <a name="position-payroll-fields-are-blank-when-editing-the-position"></a>Positionslohnfelder sind leer, wenn sie die Position bearbeiten
Mit dieser Änderung werden die Lohnfelder bei Änderungsanfragen an den vorhandenen Zeilen jetzt auf die Standardwerte zurückgesetzt.

### <a name="other-miscellaneous-bug-fixes"></a>Verschiedene andere Fehlerkorrekturen
Es gibt weitere kleinere Fehlerkorrekturen in dieser Version.

### <a name="upgrade-to-common-data-service"></a>Upgrade auf Common Data Service
Die Fristen für das Upgrade auf Common Data Service kommen schnell näher. Melden Sie sich im PowerApps-Administratorcenter an, um zu bestimmen, ob die Datenbank aktualisiert werden muss. Weitere Informationen über die Termine und erforderlichen Schritte finden Sie unter[ Upgrade auf Common Data Service](https://docs.microsoft.com/common-data-service/upgradecds/introduction-upgrade-cds).

## <a name="coming-soon"></a>Bald verfügbar

###  <a name="advanced-compensation-security-fixed-and-variable"></a>Erweiterte Vergütungssicherheit (feste oder variable)
In vielen Organisationen können Vergütungs- und Vorteilsmanager nur auf bestimmte Vergütungsdatensätze zugreifen, wie z. B. für Führungskräfte oder regional-basierte Mitarbeiter. Mit dieser Änderung können Sie die Vergütungspläne für verschiedene Mitarbeitergruppen in der Organisation verwalten. Den festen und variablen Plänen können Sicherheitsrollen zugewiesen werden, die den Zugriff auf die Pläne und die Mitarbeiterdaten in Verbindung mit den Plänen bestimmen, wie Gehalts- oder Zulagedatensätze. Nur die Rollen mit Zugriff sind in der Lage, Vergütungen für solche Mitarbeiter zu verarbeiten.

###  <a name="platform-update-24"></a>Plattformupdate 24
Weitere Details zu Platform update 24 finden Sie unter [Neues oder Änderungen in Finance and Operations platform update 24 (März 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24).
