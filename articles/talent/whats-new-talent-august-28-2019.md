---
title: Neuerungen und Änderungen in Dynamics 365 for Talent (27. August 2019)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 for Talent entweder neu oder geändert sind.
author: Darinkramer
manager: AnnBe
ms.date: 8/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: andreabichsel
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-08-27
ms.dyn365.ops.version: Talent
ms.openlocfilehash: a405ee96c36dd803fb46894ab58eca9dbfd81b5f
ms.sourcegitcommit: 097492a9e4f53a5e1fd5385d8764798518326818
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/29/2019
ms.locfileid: "1927985"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-august-27-2019"></a>Neuerungen und Änderungen in Dynamics 365 for Talent (27. August 2019)

[!include [banner](includes/banner.md)]

In diesem Thema werden die Funktionen beschrieben, die in Dynamics 365 for Talent neu oder geändert wurden.

## <a name="changes-in-attract"></a>Änderungen in Attract

Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Änderungen in Onboard

Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Core HR-Änderungen

Die in diesem Abschnitt beschriebenen Änderungen gelten für Buildnummer 8.1.2447. Die Zahlen in Klammern in einigen Überschriften beziehen sich auf Supportnummern in Microsoft Dynamics Lifecycle Services (LCS).

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>Vorschaufunktionen werden nur in den Sandkasteninstanzen aktiviert

Wenn Sie eine neue Instanz von Talent bereitstellen, können Sie angeben, ob der Instanztyp Produktion oder Sandkasten ist. Die Instanzen vom Sandkasten Typ ermöglichen ein frühzeitiges Testen neuer Funktionen. Alle vorhandenen Talent-Instanzen werden zum Instanztyp Produktion aktualisiert. Wenn eine der vorhandenen Instanzen auf den aktualisierten Instanztyp Sandkasten aktualisiert werden soll, wenden Sie sich an den Support, um die Änderungsanforderung zu initiieren.

Weitere Informationen dazu, wie Änderungen veröffentlicht werden, finden unter [Talent bereitstellen](./provisioning-talent.md).

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>Anzeigen von erweiterten Informationen, um die Leistung im Manager Self-Service zu melden

Mit einer neuen Option können Manager die Leistung von ihren direkten Mitarbeitern und den erweiterten Mitarbeitern anzeigen. Aktuell können Linienmanager Leistungsziele zuweisen und aktualisieren und neue Überprüfungen ausstellen. Darüber hinaus können Vorgesetzte und ihre Mitarbeiter Leistungserfassungen verwalten und aktualisieren, um sicherzustellen, dass der Leistungsprüfungsprozess problemlos verläuft. Wenn diese Änderung implementiert ist, sind Manager in der Lage, leistungsbezogene Informationen neben jenen für die direkt unterstellten Mitarbeitern auch jene für ihre erweiterten Mitarbeiter anzuzeigen und zu verwalten.

### <a name="deleting-legal-entities-isnt-allowed-if-employees-exist-within-the-company-339849"></a>Das Löschen von juristischen Personen ist nicht zulässig, wenn Mitarbeiter innerhalb des Unternehmens (339849) vohanden sind

Mit dieser Änderung können Sie Unternehmen nicht entfernen oder löschen, wenn Mitarbeiter und zugehöriger Daten für die juristische Person vorhanden sind.

### <a name="compensation-management-business-intelligence-analytics-dont-match-on-the-compensation-workspace-322493"></a>Vergütungsverwaltungs-BusinessIntelligence-Analyse entspricht nicht dem Kompensationsarbeitsbereich stornieren (322493)

In dieser Version wurde die Kompensationsanalyse angepasst, um die Pläne genau wiederzugeben, die Mitarbeitern zugewiesen werden.

### <a name="workflow-placeholder-company-displays-dat-when-hiring-employees-through-workflow-343905"></a>Workflowplatzhalter zeigt %company% zeigt DAT an, wenn Mitarbeiter durch den Workflow (343905) eingestellt werden 

Mit dieser Version zeigt der Unternehmensplatzhalter die juristische Person an, die mit dem neuen Beschäftigungsverhältnis des Mitarbeiters verknüpft ist.

### <a name="the-cdsjobposition-entity-displays-an-error-when-valid-to-date-is-set-349387"></a>Die CDSJobPositions-Entität zeigt einen Fehler an, wenn das Datum gültig bis (349387) festgelegt wurde

In diesem Release lassen die **Positionsdetails** und die **Positionsdauer** Datenquellen in der **CDSJobPosition** Entität das Bearbeiten der Felder von Common Data Service bis zum **Gültigkeitsdatum** zu. 

### <a name="for-employee-termination-the-last-day-worked-is-populated-on-assignment-end-date-332496"></a>Für Mitarbeiterkündigung wird der letzte Arbeitstag im Zuweisungsenddatum (332496 ) bearbeitet

Dies ändert nun die Standardposition **Enddatum der Zuordnung** zu **Datum des Beschäftigungsendes**. Sie können dieser Standards beim Eingeben der Daten ändern.

### <a name="legal-entities-arent-limited-with-hire-338871"></a>Juristische Personen sind nicht eingeschränkt mit der Einstellung (338871)
 
Diese Änderung schränkt den Einstellungsprozess ein, um lediglich diese juristischen Personen anzuzeigen, auf die der Benutzer Zugriff hat.  

## <a name="in-preview"></a>Vorschau

### <a name="streamlined-employee-entry-and-navigation"></a>Fortschrittlicher Mitarbeitereintrag und ‑Navigation

Diese Funktionalität ist in der Sandbox- und Testumgebung verfügbar. Um diese Funktion zu aktivieren, navigieren Sie zu **> Systemverwaltung > Verknüpfung > Einstellungen > Systemparameter- > Vorschaufunktionen**. Wählen Sie **Verbessertes Arbeitskraftformular und Navigation** aus. Dies ermöglicht diese Änderungen für alle Benutzer. Sie können diese Option jederzeit deaktivieren.

Weitere Informationen finden Sie unter [Fortschrittlicher Mitarbeitereintrag und -Navigation](./streamlined-employee-entry.md).

## <a name="coming-soon"></a>Bald verfügbar

### <a name="platform-update-29"></a>Plattformupdate 29

Zusätzliche Details zur Plattformaktualisierung 29 finden Sie unter [Vorschaufunktionen in Dynamics 365 for Finance and Operations Plattformaktualisierung 29 (Oktober 2019)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-29).
