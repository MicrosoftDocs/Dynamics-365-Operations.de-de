---
title: Neuerungen oder Änderungen in Dynamics 365 Talent (1. Oktober 2019)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 Talent entweder neu oder geändert sind.
author: Darinkramer
manager: AnnBe
ms.date: 10/01/2019
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
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 69c0a805027f215b2a2a42d826ee7a346cfdd511
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529659"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-1-2019"></a>Neuerungen oder Änderungen in Dynamics 365 Talent (1. Oktober 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

In diesem Thema werden die Funktionen beschrieben, die in Dynamics 365 Talent neu oder geändert wurden.

## <a name="changes-in-attract"></a>Änderungen in Attract

Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Änderungen in Onboard

Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Core HR-Änderungen

Die in diesem Abschnitt beschriebenen Änderungen gelten für Buildnummer 8.1.2509. Die Zahlen in Klammern in einigen Überschriften beziehen sich auf Supportnummern in Microsoft Dynamics Lifecycle Services (LCS).

### <a name="streamlined-employee-entry-and-navigation"></a>Fortschrittlicher Mitarbeitereintrag und ‑Navigation

Diese Funktionalität ist in allen Umgebungen verfügbar. Um diese Funktion zu aktivieren, navigieren Sie zu **> Systemverwaltung > Verknüpfung > Einstellungen > Systemparameter- > Vorschaufunktionen**. Wählen Sie **Verbessertes Arbeitskraftformular und Navigation** aus. Dies ermöglicht diese Änderungen für alle Benutzer. Sie können diese Option jederzeit deaktivieren.

Weitere Informationen finden Sie unter [Fortschrittlicher Mitarbeitereintrag und -Navigation](./streamlined-employee-entry.md). Um ein Video dieser Änderungen anzusehen, rufen Sie die Übersicht zu [Dynamics 365 for Talent 2019 Versionswelle 2](https://aka.ms/ROGT19RW2ROV) auf.

### <a name="you-can-enable-preview-features-in-sandbox-and-trial-environments"></a>Sie können Vorschaufunktionen in der Sandbox- und Testumgebung aktivieren

Wenn Sie eine neue Instanz von Talent bereitstellen, können Sie angeben, ob der Instanztyp Produktion oder Sandkasten ist. Die Instanzen vom Sandkasten Typ ermöglichen ein frühzeitiges Testen neuer Funktionen. Wenn eine der vorhandenen Instanzen auf den aktualisierten Instanztyp Sandkasten aktualisiert werden soll, wenden Sie sich an den Support, um die Änderungsanforderung zu initiieren.

Weitere Informationen dazu, wie Änderungen veröffentlicht werden, finden unter [Talent bereitstellen](./provisioning-talent.md).

### <a name="compensation-date-defaults-to-a-different-date-than-the-position-assignment-337694"></a>Vergütungsdatum hat ein anderes Standarddatum als die Positionszuweisung (337694)

Durch diese Änderung startet das Vergütungsdatum standardmäßig am Startdatum der Positionszuweisung.

### <a name="not-able-to-end-compensation-along-with-its-position-assignment-328993"></a>Die Vergütung kann nicht mit der Positionszuweisung beendet werden (328993)

Mit dieser Änderung können Sie die Vergütung beenden, wenn Sie die Positionszuweisung beenden, indem Sie **Zuordnung beenden** auf der Seite **Arbeitskraft-Positionszuordnungen** aktivierten Mitarbeiter Aktivitäten verwenden.

### <a name="bank-account-validation-requires-routing-and-account-numbers-in-all-locations-340403"></a>Bankkontoprüfung erfordert Routing und Kontonummern an allen Lagerplätzen (340403 )

Mit den Änderungen dieser Woche wurde eine neue Konfigurationsoption hinzugefügt, um die erforderliche Prüfung der **Bankleitzahl** und **Kontonummer** zu deaktivieren. 

### <a name="attachments-are-not-enabled-in-mss-performance-journals-for-performance-feedback-341794"></a>Anhänge werden nicht in den MSS-Leistungserfassungen für Leistungsrückmeldung aktiviert (341794)

Bei der Version dieser Woche werden die Anlagen für Rückmeldungsartikel in der Leistungserfassungsseite aktiviert.

### <a name="leave-request-details-dont-sync-from-common-data-service-to-talent-369608"></a>Urlaubsanforderungsdetails werden nicht von Common Data Service an Talent synchronisiert (369608)

Mithilfe dieser Änderungen, werden Urlaubanforderungsdetails an Talent synchronisiert, die in Common Data Service aktualisiert wurden.

### <a name="job-description-doesnt-display-for-the-job-in-the-skill-gap-analysis-page-369398"></a>Stellenbeschreibung wird für die Stelle nicht in der Analyse der Qualifikationslücken angezeigt (369398)

Im Build dieser Woche wird die Beschreibung angezeigt, wenn sie die Stelle auf der Seite **Analyse der Qualifikationslücken** auswählen.

## <a name="coming-soon"></a>Bald verfügbar

### <a name="print-performance-reviews"></a>Leistungsbeurteilungen drucken

Mitarbeiter, Manager und Personalverwaltungsmitarbeiter können dann die Leistungsbeurteilung eines Mitarbeiters drucken.


[!INCLUDE[footer-include](../includes/footer-banner.md)]