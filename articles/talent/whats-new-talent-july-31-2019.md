---
title: Neuerungen und Änderungen in Dynamics 365 for Talent (31. Juli 2019)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 for Talent entweder neu oder geändert sind.
author: Darinkramer
manager: AnnBe
ms.date: 7/30/2019
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
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 1fffe1bd8739723294c027c174d5e959c1c6010a
ms.sourcegitcommit: 4ff8c2c2f3705d8045df66f2c4393253e05b49ed
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2019
ms.locfileid: "1864578"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-july-30-2019"></a>Neuerungen und Änderungen in Dynamics 365 for Talent (30. Juli 2019)

[!include [banner](includes/banner.md)]

In diesem Thema werden die Funktionen beschrieben, die in Dynamics 365 for Talent neu oder geändert wurden.

## <a name="changes-in-attract"></a>Änderungen in Attract
Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Änderungen in Onboard
Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Core HR-Änderungen
Die in diesem Abschnitt beschriebenen Änderungen gelten für Buildnummer 8.1.2409.


### <a name="region-support-for-canada-and-southeast-asia"></a>Regionssupport für Kanada und Südostasien

Wir freuen uns anzukündigen, dass Kanada- und Südostasien nun für Microsoft Dynamics 365 for Talent am 1. August 2019 verfügbar sind. Mit dieser Änderung können Umgebungen in kanadischen asiatischen Regionen erstellen, und alle Talentdaten werden nur innerhalb dieser Standorte verwaltet. Sie können eine Umgebung in diesen neuen Regionen erstellen, indem Sie die elektronische Adresse im neuen Umgebungsdialogfeld auswählen und diese Umgebung verwenden, um Talent in LCS wie unter [Talent bereitstellen](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent) beschrieben nutzen

Datenmigration vorhandener Projekte aus anderen Regionen in kanadische und asiatische Regionen wird nicht unterstützt. Nur neue Projekte können zu den neuen unterstützten Regionen bereitgestellt werden.

### <a name="new-active-positions-list-page"></a>Neue aktive Positionslistenseite

Die Optionen für positionsbasierte Listen enthalten nun: **Alle Positionen**, **Aktive Positionen**, **Offene Positionen** und **Inaktive Positionen**. Die Listenseite neue **Aktive Positionen** zeigt nur die Positionen an, offen oder besetzt, die zum aktuellen Datum aktiv sind. 

### <a name="allow-course-participants-to-be-added-to-open-courses"></a>Ermöglichen Sie den Kursteilnehmer, offenen Kursen hinzugefügt zu werden

Die Änderungen dieser Woche beheben ein Problem, bei dem nur Direktunterstellte für offene Kurse erfasst werden können.

### <a name="fte-analysis-displaying-incorrect-fte-number"></a>FTE-Analyse, die falsche FTE-Nummer anzeigt

**FTE-Analyse** ist auf der Registerkarte **Analyse** von **Personalführung** korrigiert worden.

### <a name="final-comments-label-translation"></a>Abschließende Kommentarbeschriftungsübersetzung

Das Feld **Abschließende Kommentare** wird nun in der Prüfungsform übersetzt.

## <a name="in-preview"></a>Vorschau

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>Vorschaufunktionen werden nur in den Sandkasteninstanzen aktiviert

Wenn Sie eine neue Instanz von Talent bereitstellen, können Sie angeben, ob der Instanztyp **Produktion** oder **Sandkasten** ist. Die Instanzen vom **Sandkasten** Typ ermöglichen ein frühzeitiges Testen neuer Funktionen. Alle vorhandenen Talent-Instanzen werden zum Instanztyp **Produktion** aktualisiert. Wenn eine der vorhandenen Instanzen auf den aktualisierten Instanztyp **Sandkasten** aktualisiert werden soll, wenden Sie sich an den [Support](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support), um die Änderungsanforderung zu initiieren.

Weitere Informationen dazu, wie Änderungen veröffentlicht werden, finden unter [Talent bereitstellen](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>Anzeigen von erweiterten Informationen, um die Leistung im Manager Self-Service zu melden

Mit einer neuen Option können Manager die Leistung von ihren direkten Mitarbeitern und den erweiterten Mitarbeitern anzeigen. Aktuell können Linienmanager Leistungsziele zuweisen und aktualisieren und neue Überprüfungen ausstellen. Darüber hinaus können Vorgesetzte und ihre Mitarbeiter Leistungserfassungen verwalten und aktualisieren, um sicherzustellen, dass der Leistungsprüfungsprozess problemlos verläuft. Wenn diese Änderung implementiert ist, sind Manager in der Lage, leistungsbezogene Informationen neben jenen für die direkt unterstellten Mitarbeitern auch jene für ihre erweiterten Mitarbeiter anzuzeigen und zu verwalten.
