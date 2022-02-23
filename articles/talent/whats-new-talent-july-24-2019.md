---
title: Neuerungen und Änderungen in Dynamics 365 Talent (23. Juli 2019)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 Talent entweder neu oder geändert sind.
author: Darinkramer
manager: AnnBe
ms.date: 07/23/2019
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
ms.search.validFrom: 2019-07-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 360574d3c8e0b349119e0987f2453a5d5be21e90
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528146"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-july-23-2019"></a>Neuerungen und Änderungen in Dynamics 365 Talent (23. Juli 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

In diesem Thema werden die Funktionen beschrieben, die in Dynamics 365 Talent neu oder geändert wurden.

## <a name="changes-in-attract"></a>Änderungen in Attract

### <a name="pdf-renderer-for-candidate-documents"></a>PDF-Renderer für Kandidatendokumente

Attract-Benutzer können nun PDF-Anhänge für Kandidaten im Dokumentviewer anzeigen, anstatt die Anhänge herunterzuladen.

### <a name="signing-up-for-attract-user-research-group"></a>Für Attract Nutzer Fehlergruppe anmelden 

Da die Funktionalität der neuen Produktdimensionsgruppen planen oder Vorschaufunktionen versenden, suchen wir Benutzer, mit deren Hilfe wir über unsere Richtung informieren können. Interessierte Benutzer können sich anmelden, um Teil der Benutzerforschungsgruppe zu sein, indem Sie den Registrierungslink unserer App verwenden.

### <a name="job-approvals-appear-on-the-home-page"></a>Stellengenehmigungen werden auf der Startseite angezeigt

Genehmigungen werden im Abschnitt **Genehmigungen** im Dashboard angezeigt. Genehmiger können ihre Genehmigungen unter **Ihnen zugewiesen** überprüfen. Sie zeigen die Stellen-ID, den Stellen-Titel, andere Genehmiger und das Datum an, an der die Stelle zugewiesen wurde. Benutzer, die eine Stelle zur Genehmigung übermitteln, können ihre Stellen unter **Von Ihnen angefordert** überprüfen. Dort werden die Genehmiger angezeigt, die immer noch die übermittelte Stelle genehmigen müssen.

## <a name="changes-in-onboard"></a>Änderungen in Onboard
Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Core HR-Änderungen
Die in diesem Abschnitt beschriebenen Änderungen gelten für Buildnummer 8.1.2394.

### <a name="entity-support-for-custom-fields-in-common-data-service"></a>Entitätssupport für benutzerdefinierte Felder in Common Data Service 

Mit dieser Version **Arbeitskalender** und **Arbeitskalender**-Tag werden nun benutzerdefinierte Felder in Common Data Service unterstützt.

### <a name="restrict-leave-types-in-time-off-requests"></a>Begrenzen der Sonderurlaubstypen in den Abwesenheitsanforderungen

Organisationen können Mitarbeitern viele unterschiedliche Arten von Sonderurlaub anbieten. Allerdings ist er möglicherweise nicht angebracht, dass Mitarbeiter einen Freizeitantrag für bestimmte Sonderurlaubstypen senden. Diese Sonderurlaubstypen können stattdessen von der Personalverwaltung (HR) verwaltet werden. Mit dieser Version können Sie konfigurieren, für welche Sonderurlaubstypen die Mitarbeiter Abwesenheitsanforderungen übermitteln können. 

## <a name="in-preview"></a>Vorschau

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>Vorschaufunktionen werden nur in den Sandkasteninstanzen aktiviert

Wenn Sie eine neue Instanz von Talent bereitstellen, können Sie angeben, ob der Instanztyp **Produktion** oder **Sandkasten** ist. Die Instanzen vom **Sandkasten** Typ ermöglichen ein frühzeitiges Testen neuer Funktionen. Alle vorhandenen Talent-Instanzen werden zum Instanztyp **Produktion** aktualisiert. Wenn eine der vorhandenen Instanzen auf den aktualisierten Instanztyp **Sandkasten** aktualisiert werden soll, wenden Sie sich an den [Support](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support), um die Änderungsanforderung zu initiieren.

Weitere Informationen dazu, wie Änderungen veröffentlicht werden, finden unter [Talent bereitstellen](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>Anzeigen von erweiterten Informationen, um die Leistung im Manager Self-Service zu melden

Mit einer neuen Option können Manager die Leistung von ihren direkten Mitarbeitern und den erweiterten Mitarbeitern anzeigen. Aktuell können Linienmanager Leistungsziele zuweisen und aktualisieren und neue Überprüfungen ausstellen, die ihre Mitarbeiter mitverwalten. Darüber hinaus können Vorgesetzte und ihre Mitarbeiter Leistungserfassungen verwalten und aktualisieren, um sicherzustellen, dass der Leistungsprüfungsprozess problemlos verläuft. Wenn diese Änderung implementiert ist, sind Manager in der Lage, leistungsbezogene Informationen neben jenen für die direkt unterstellten Mitarbeitern auch jene für ihre erweiterten Mitarbeiter anzuzeigen und zu verwalten. 

## <a name="coming-soon"></a>Bald verfügbar

### <a name="region-support-for-canada-and-southeast-asia"></a>Regionssupport für Kanada und Südostasien

Wir freuen uns anzukündigen, dass Kanada- und Südostasien nun für Talent am 1. August 2019 verfügbar sind. Mit dieser Änderung können Umgebungen in kanadischen asiatischen Regionen erstellen, und alle Talentdaten werden nur innerhalb dieser Standorte verwaltet. Sie können eine Umgebung in diesen neuen Regionen erstellen, indem Sie die elektronische Adresse im neuen Umgebungsdialogfeld auswählen und diese Umgebung verwenden, um Talent in LCS wie hier unter [Talent bereitstellen](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent) beschrieben nutzen

Datenmigration vorhandener Projekte aus anderen Regionen in kanadische und asiatische Regionen wird nicht unterstützt. Nur neue Projekte können zu den neuen unterstützten Regionen bereitgestellt werden.
