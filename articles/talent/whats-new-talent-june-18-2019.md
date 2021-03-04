---
title: Neuerungen und Änderungen in Dynamics 365 Talent (18. Juni 2019)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 Talent entweder neu oder geändert sind.
author: Darinkramer
manager: AnnBe
ms.date: 06/18/2019
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
ms.search.validFrom: 2019-06-18
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 6a8b17fbeba591c20253bc4ec66767ac0dea64e6
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528074"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-june-18-2019"></a>Neuerungen und Änderungen in Dynamics 365 Talent (18. Juni 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 Talent entweder neu oder geändert sind.

## <a name="changes-in-attract"></a>Änderungen in Attract

Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Attract.

## <a name="coming-soon-in-attract"></a>Bald verfügbar in Attract

### <a name="job-approvals-appear-on-the-home-page"></a>Stellengenehmigungen werden auf der Startseite angezeigt

Genehmigungen werden im Abschnitt **Genehmigungen** im Dashboard angezeigt. Genehmiger können ihre Genehmigungen unter **Ihnen zugewiesen** überprüfen. Sie zeigen die Stellen-ID, den Stellen-Titel, andere Genehmiger und das Datum an, an der die Stelle zugewiesen wurde. Benutzer, die eine Stelle zur Genehmigung übermitteln, können ihre Stellen unter **Von Ihnen angefordert** überprüfen. Dort werden die Genehmiger angezeigt, die immer noch die übermittelte Stelle genehmigen müssen.

## <a name="changes-in-onboard"></a>Änderungen in Onboard

Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Core HR-Änderungen

Die in diesem Abschnitt beschriebenen Änderungen gelten für Buildnummer 8.1.2347.

### <a name="confirmation-of-course-participants-causes-an-error"></a>Bestätigung der Kursteilnehmer verursacht einen Fehler

Das Dialogfeld für die Ausgabe des Berichts über Kursteilnehmer wurde entfernt. Dieser Bericht wird nicht in Talent unterstützt.

### <a name="the-compensation-section-of-the-transfer-worker-page-isnt-available-in-some-scenarios"></a>Der Kompensationsabschnitt der Übergangsarbeitskraftseite ist in einigen Szenarien nicht verfügbar

Diese Änderung ermöglicht Benutzern Vergütungsdaten einzugeben, wenn sie die Seite **Arbeitskraft versetzen** ausfüllen.

## <a name="in-preview"></a>Vorschau

### <a name="preview-features-will-be-enabled-only-in-sandbox-environments"></a>Vorschaufunktionen werden nur in der Sandkastenumgebung aktiviert

Weitere Informationen dazu, wie Änderungen veröffentlicht werden, finden unter [Talent bereitstellen](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

Wenn Sie eine neue Instanz von Talent bereitstellen, können Sie angeben, ob der Instanztyp **Produktion** oder **Sandkasten** ist. Die **Sandkasten** Instanz ermöglicht ein frühzeitiges Testen neuer Funktionen. Alle vorhandenen Talent-Instanzen werden zum Instanztyp **Produktion** aktualisiert. Wenn eine der vorhandenen Instanzen auf den aktualisierten Instanztyp **Sandkasten** aktualisiert werden soll, wenden Sie sich an den [Support](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support), um die Änderungsanforderung zu initiieren.

### <a name="restrict-the-leave-types-in-time-off-requests"></a>Begrenzen der Sonderurlaubstypen in den Abwesenheitsanforderungen

Organisationen können Mitarbeitern viele unterschiedliche Arten von Sonderurlaub anbieten. Allerdings ist er möglicherweise nicht angebracht, dass Mitarbeiter einen Freizeitantrag für bestimmte Sonderurlaubstypen senden. Diese Sonderurlaubstypen können von der Personalverwaltung (HR) verwaltet werden. Mit dieser Version können Sie konfigurieren, für welche Sonderurlaubstypen die Mitarbeiter Abwesenheitsanforderungen übermitteln können. 

## <a name="coming-soon-in-core-hr"></a>Bald in Core HR verfügbar

### <a name="common-data-service-entity-support-for-custom-fields"></a>Common Data Service-Entitätssupport für benutzerdefinierte Felder

Die folgenden Entitäten unterstützen benutzerdefinierte Felder: Lohn-Einnahmecode und Kompensationsreferenzpunkt. 

### <a name="new-common-data-service-entities"></a>Neue Common Data Service Entitäten

Die Ursachencodeentität wird Common Data Service hinzugefügt.

### <a name="view-performance-information-for-direct-and-extended-reports-in-manager-self-service"></a>Anzeigen von Leistungsinformationen für direkte und erweiterten Berichte im Manager Self-Service

Mit einer neuen Option können Manager die Leistung von ihren direkten Mitarbeitern und den erweiterten Mitarbeitern anzeigen. Aktuell können Linienmanager Leistungsziele zuweisen und aktualisieren und neue Überprüfungen ausstellen. Darüber hinaus können Vorgesetzte und ihre Mitarbeiter Leistungserfassungen verwalten und aktualisieren, um sicherzustellen, dass der Leistungsprüfungsprozess problemlos verläuft. Wenn diese Änderung implementiert ist, sind Manager in der Lage, leistungsbezogene Informationen neben jenen für die direkt unterstellten Mitarbeitern auch jene für ihre erweiterten Mitarbeiter anzuzeigen und zu verwalten.

### <a name="print-performance-reviews"></a>Leistungsbeurteilungen drucken

Mitarbeiter, Manager und Personalverwaltung können dann die Leistungsbeurteilung eines Mitarbeiters drucken.


[!INCLUDE[footer-include](../includes/footer-banner.md)]