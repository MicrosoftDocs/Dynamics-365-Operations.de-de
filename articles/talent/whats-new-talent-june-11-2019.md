---
title: Neuerungen und Änderungen in Dynamics 365 Talent (11. Juni 2019)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 Talent entweder neu oder geändert sind.
author: Darinkramer
manager: AnnBe
ms.date: 06/11/2019
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
ms.search.validFrom: 2019-06-11
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 20dc0768463d9a5d6762cb062deb0bdbe4d53fe3
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528668"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-june-11-2019"></a>Neuerungen und Änderungen in Dynamics 365 Talent (11. Juni 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 Talent entweder neu oder geändert sind.

## <a name="changes-in-attract"></a>Änderungen in Attract

### <a name="search-engine-optimization-for-job-posts"></a>Suchmaschinenoptimierung für Stellenausschreibungen

Nachdem Sie die **Suchmaschinen-Optimierung** im Dynamics 365 Talent: Attract Admin Center aktiviert haben, informiert Attract die Google-Indizierungsanwendungsprogrammierschnittstelle (API), um die Webseite zu durchsuchen, wenn Sie eine neue Stelle aktivieren und veröffentlichen oder eine bestehende Stelle aktualisieren. Auf diese Weise wird die Stelle in den Suchergebnissen für Google und andere Suchmodule angezeigt.

Ebenso wird, sobald Sie eine Stelle verbergen, Attract die indezierende API informieren, dass die gelöschte Stelle nicht mehr in den Suchergebnissen angezeigt werden soll.

> [!NOTE]
> Internet-Crawler haben keinen bestimmten Zeitrahmen für das Durchforsten von Webseiten oder Aktualisierung von Suchergebnissen.

## <a name="coming-soon-in-attract"></a>Bald verfügbar in Attract

### <a name="job-approvals-appear-on-the-home-page"></a>Stellengenehmigungen werden auf der Startseite angezeigt

Genehmigungen werden im Abschnitt **Genehmigungen** im Dashboard angezeigt. Genehmiger können ihre Genehmigungen unter **Ihnen zugewiesen** überprüfen. Sie zeigen die Stellen-ID, den Stellen-Titel, andere Genehmiger und das Datum an, an der die Stelle zugewiesen wurde. Benutzer, die eine Stelle zur Genehmigung übermitteln, können ihre Stellen unter **Von Ihnen angefordert** überprüfen. Dort werden die Genehmiger angezeigt, die immer noch die übermittelte Stelle genehmigen müssen.

## <a name="changes-in-onboard"></a>Änderungen in Onboard

Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Core HR-Änderungen

Die in diesem Abschnitt beschriebenen Änderungen gelten für Buildnummer 8.1.2337.

### <a name="platform-update-27-for-finance-and-operations"></a>Plattformupdate 27 für Finance and Operations

Zusätzliche Details zum Plattformupdate 27 für Finance and Operations finden Sie unter [Vorschaufunktionen im Plattformupdate 27 für Dynamics 365 Finance and Operations (Juni 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-27).

### <a name="feature-management-workspace-in-talent"></a>Funktionsverwaltungsarbeitsbereich im Talent

Im Arbeitsbereich **Funktionsverwaltung** in **Systemverwaltung** können Sie Funktionen anzuzeigen, aktivieren, deaktivieren und Planen, die in jeder Version geliefert wurden. Standardmäßig sind neue Funktionen ausgeschaltet. Sie können den Arbeitsbereich **Funktionsverwaltung** verwenden, um sie zu aktivieren und die Dokumentation für sie anzuzeigen.

### <a name="common-data-service-entity-support-for-custom-fields"></a>Common Data Service-Entitätssupport für benutzerdefinierte Felder

Die ausgebende Entität unterstützt nun benutzerdefinierte Felder.

### <a name="new-common-data-service-entities"></a>Neue Common Data Service Entitäten

Die Aufgabengruppenentität wird hinzugefügt.

## <a name="in-preview"></a>Vorschau

### <a name="preview-features-will-be-enabled-only-in-sandbox-environments"></a>Vorschaufunktionen werden nur in der Sandkastenumgebung aktiviert

Weitere Informationen dazu, wie Änderungen veröffentlicht werden, finden unter [Talent bereitstellen](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

Wenn Sie eine neue Instanz von Talent bereitstellen, können Sie angeben, ob der Instanztyp Produktion oder Sandkasten ist. Die Sandkasten Instanz ermöglicht ein frühzeitiges Testen neuer Funktionen. Alle vorhandenen Talent-Instanzen werden zum Instanztyp **Produktion** aktualisiert. Wenn eine der vorhandenen Instanzen auf den aktualisierten Instanztyp **Sandkasten** aktualisiert werden soll, wenden Sie sich an den [Support](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support), um die Änderungsanforderung zu initiieren.

### <a name="restrict-the-leave-types-in-time-off-requests"></a>Begrenzen der Sonderurlaubstypen in den Abwesenheitsanforderungen

Organisationen können Mitarbeitern viele unterschiedliche Arten von Sonderurlaub anbieten. Allerdings ist er möglicherweise nicht angebracht, dass Mitarbeiter einen Freizeitantrag für bestimmte Sonderurlaubstypen senden. Diese Sonderurlaubstypen können von der Personalverwaltung (HR) verwaltet werden. Mit dieser Version können Sie konfigurieren, für welche Sonderurlaubstypen die Mitarbeiter Abwesenheitsanforderungen übermitteln können. 

## <a name="coming-soon-in-core-hr"></a>Bald in Core HR verfügbar

### <a name="view-extended-information-about-report-performance-in-manager-self-service"></a>Anzeigen von erweiterten Informationen um die Leistung im Manager Self-Service zu melden

Mit einer neuen Option können Manager die Leistung von ihren direkten Mitarbeitern und den erweiterten Mitarbeitern anzeigen. Aktuell können Linienmanager Leistungsziele zuweisen und aktualisieren und neue Überprüfungen ausstellen. Darüber hinaus können Vorgesetzte und ihre Mitarbeiter Leistungserfassungen verwalten und aktualisieren, um sicherzustellen, dass der Leistungsprüfungsprozess problemlos verläuft. Wenn diese Änderung implementiert ist, sind Manager in der Lage, leistungsbezogene Informationen neben jenen für die direkt unterstellten Mitarbeitern auch jene für ihre erweiterten Mitarbeiter anzuzeigen und zu verwalten.

### <a name="print-performance-reviews"></a>Leistungsbeurteilungen drucken

Mitarbeiter, Manager und Personalverwaltung können dann die Leistungsbeurteilung eines Mitarbeiters drucken.
