---
title: Neuerungen und Änderungen in Dynamics 365 for Talent (25. Juni 2019)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 for Talent entweder neu oder geändert sind.
author: Darinkramer
manager: AnnBe
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-06-25
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e32768c898e2934b95eb8ab7b212337aff0c1556
ms.sourcegitcommit: fbe6d35ed35aa01f438990e2880c3a3cf223ea8c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/27/2019
ms.locfileid: "1704468"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-june-25-2019"></a>Neuerungen und Änderungen in Dynamics 365 for Talent (25. Juni 2019)

[!include [banner](includes/banner.md)]

In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 for Talent entweder neu oder geändert sind.

## <a name="changes-in-attract"></a>Änderungen in Attract

Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Attract.

## <a name="coming-soon-in-attract"></a>Bald verfügbar in Attract

### <a name="job-approvals-appear-on-the-home-page"></a>Stellengenehmigungen werden auf der Startseite angezeigt

Genehmigungen werden im Abschnitt **Genehmigungen** im Dashboard angezeigt. Genehmiger können ihre Genehmigungen unter **Ihnen zugewiesen** überprüfen. Sie zeigen die Stellen-ID, den Stellen-Titel, andere Genehmiger und das Datum an, an der die Stelle zugewiesen wurde. Benutzer, die eine Stelle zur Genehmigung übermitteln, können ihre Stellen unter **Von Ihnen angefordert** überprüfen. Dort werden die Genehmiger angezeigt, die immer noch die übermittelte Stelle genehmigen müssen.

## <a name="changes-in-onboard"></a>Änderungen in Onboard
Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Core HR-Änderungen

Die in diesem Abschnitt beschriebenen Änderungen gelten für Buildnummer 8.1.2357.

### <a name="incorrect-value-displayed-for-primary-position-314266"></a>Falscher Wert für primäre Position angezeigt (314266)

Diese Änderungen werden stets zunächst die Einstellungen **Primäre Position** auf allen Seiten anzeigen.

### <a name="cant-edit-after-recalling-the-workflow-in-review-318180"></a>Kann nicht bearbeitet werden, nachdem der Workflow in Bearbeitung aufgerufen wird (318180)

Prüfungen, die mittels Workflow zurückgerufen wurden, können nun bearbeitet werden.

### <a name="final-comments-field-in-reviews-isnt-translated-325921"></a>Abschließendes Kommentarfeld in den Prüfungen wird nicht übersetzt (325921)

Die Bezeichnung **Abschließende Kommentare** wird im Talent übersetzt.

### <a name="preview-features-will-be-enabled-only-in-sandbox-environments"></a>Vorschaufunktionen werden nur in der Sandkastenumgebung aktiviert

Wenn Sie eine neue Instanz von Talent bereitstellen, können Sie angeben, ob der Instanztyp **Produktion** oder **Sandkasten** ist. Die **Sandkasten** Instanz ermöglicht ein frühzeitiges Testen neuer Funktionen. Alle vorhandenen Talent-Instanzen werden zum Instanztyp **Produktion** aktualisiert. Wenn eine der vorhandenen Instanzen auf den aktualisierten Instanztyp **Sandkasten** aktualisiert werden soll, wenden Sie sich an den [Support](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support), um die Änderungsanforderung zu initiieren.

Weitere Informationen dazu, wie Änderungen veröffentlicht werden, finden unter [Talent bereitstellen](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

## <a name="in-preview"></a>Vorschau

### <a name="restrict-the-leave-types-in-time-off-requests"></a>Begrenzen der Sonderurlaubstypen in den Abwesenheitsanforderungen

Organisationen können Mitarbeitern viele unterschiedliche Arten von Sonderurlaub anbieten. Allerdings ist er möglicherweise nicht angebracht, dass Mitarbeiter einen Freizeitantrag für bestimmte Sonderurlaubstypen senden. Diese Sonderurlaubstypen können von der Personalverwaltung (HR) verwaltet werden. Mit dieser Version können Sie konfigurieren, für welche Sonderurlaubstypen die Mitarbeiter Abwesenheitsanforderungen übermitteln können. 

## <a name="coming-soon-in-core-hr"></a>Bald in Core HR verfügbar

### <a name="feature-management-area-in-talent"></a>Funktionsverwaltungsbereich im Talent

**Funktionsverwaltung** wird von der **Systemverwaltung** aufgrund der Probleme mit der Funktion entfernt. Wir führen die **Funktionsverwaltung** in einer späteren Version wieder ein. 

### <a name="common-data-service-entity-support-for-custom-fields"></a>Common Data Service-Entitätssupport für benutzerdefinierte Felder

Die folgenden Entitäten unterstützen benutzerdefinierte Felder: **Lohneinkommenscode**, **Ereignis der festen Vergütung**, **Vergütungsraster**, **Lohnperiode** und **Kompensationsreferenzpunkt**. 

### <a name="new-common-data-service-entities"></a>Neue Common Data Service Entitäten

Die**Ursachencode** Entität wird hinzugefügt in Common Data Service.

### <a name="view-performance-information-for-direct-and-extended-reports-in-manager-self-service"></a>Anzeigen von Leistungsinformationen für direkte und erweiterten Berichte im Manager Self-Service

Mit einer neuen Option können Manager die Leistung von ihren direkten Mitarbeitern und den erweiterten Mitarbeitern anzeigen. Aktuell können Linienmanager Leistungsziele zuweisen und aktualisieren und neue Überprüfungen ausstellen. Darüber hinaus können Vorgesetzte und ihre Mitarbeiter Leistungserfassungen verwalten und aktualisieren, um sicherzustellen, dass der Leistungsprüfungsprozess problemlos verläuft. Wenn diese Änderung implementiert ist, sind Manager in der Lage, leistungsbezogene Informationen neben jenen für die direkt unterstellten Mitarbeitern auch jene für ihre erweiterten Mitarbeiter anzuzeigen und zu verwalten.

### <a name="print-performance-reviews"></a>Leistungsbeurteilungen drucken

Mitarbeiter, Manager und Personalverwaltung können dann die Leistungsbeurteilung eines Mitarbeiters drucken.
