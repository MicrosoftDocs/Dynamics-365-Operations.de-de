---
title: Neuerungen oder Änderungen in Dynamics 365 Talent (5. November 2019)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 Talent entweder neu oder geändert sind.
author: Darinkramer
manager: AnnBe
ms.date: 11/05/2019
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
ms.search.validFrom: 2019-11-05
ms.dyn365.ops.version: Talent
ms.openlocfilehash: c4068cf81782d2f9559179b91da31e049c006059
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527119"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-november-5-2019"></a>Neuerungen oder Änderungen in Dynamics 365 Talent (5. November 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

In diesem Thema werden die Funktionen beschrieben, die in Dynamics 365 Talent neu oder geändert wurden.

## <a name="changes-in-attract"></a>Änderungen in Attract

Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Änderungen in Onboard

Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Core HR-Änderungen

Die in diesem Abschnitt beschriebenen Änderungen gelten für Buildnummer 8.1.2598. Die Zahlen in Klammern in einigen Überschriften beziehen sich auf Supportnummern in Microsoft Dynamics Lifecycle Services (LCS).

### <a name="copy-a-core-hr-instance"></a>Kopieren einer Core HR-Instanz

In der aktuellen Version können Sie mit Microsoft Dynamics Lifecycle Services (LCS) eine Microsoft Dynamics 365 Talent: Core HR-Datenbank in eine Sandbox-Umgebung kopieren. Wenn Sie eine andere Sandbox-Umgebung haben, können Sie die Datenbank auch aus dieser Umgebung in eine bestimmte Sandbox-Umgebung kopieren. Weitere Informationen finden Sie hier:

- [Breiteres Umgebungsmanagement](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/broader-environment-management) im Dynamics 365: 2019 Release Wave 2 Plan

- [Kopieren einer Core HR-Instanz](hr-copy-instance.md) in der Talentdokumentation

### <a name="common-data-service-integration-batch-jobs-arent-created-when-common-data-service-integration-is-enabled-388030"></a>Common Data Service Integration Batchjobs werden nicht erstellt, wenn die Common Data Service Integration aktiviert ist (388030).

Diese Änderung erstellt Batch-Jobs für die Common Data Service-Integration, wenn sie aktiviert ist.

### <a name="the-hcmpersonimageentity-doesnt-resize-the-person-image-when-uploaded-369469"></a>Die HcmPersonImageEntity ändert die Größe des Personenbildes beim Hochladen nicht (369469).

Die Veröffentlichung dieser Woche ändert die Größe der Bilder, um die Leistung beim Import über die Datenverwaltung zu verbessern.

### <a name="a-positions-available-for-assignment-date-can-be-earlier-than-the-activation-date-340103"></a>Das Datum der Verfügbarkeit für die Zuordnung einer Position kann vor dem Aktivierungsdatum (340103) liegen.

Bei dieser Änderung erscheint eine Warnung, wenn Sie ein **Verfügbar für Zuordnungsdatum** auswählen, das vor dem **Aktivierungsdatum** der Position liegt.

### <a name="cant-create-a-compensation-change-request-in-employee-self-service-for-step-based-plans-376872"></a>Es kann kein Vergütungsänderungsantrag im Employee Self-Service für schrittbasierte Pläne erstellt werden (376872).

Diese Freigabe behebt ein Problem bei der Beantragung von Vergütungsänderungen durch die Mitarbeiter-Self-Service für stufenbasierte Pläne. 

### <a name="reason-code-doesnt-sync-to-common-data-service-if-the-description-is-longer-than-30-characters-core-hr-allows-60-352682"></a>Der Begründungscode wird nicht mit Common Data Service synchronisiert, wenn die Beschreibung länger als 30 Zeichen ist, Core HR erlaubt 60 (352682).

mit dieser Änderung werden Differenzcodes mit mehr als 30 Zeichen in Common Data Service aktualisiert. Änderungen in Common Data Service werden auch in Talent berücksichtigt.

### <a name="address-integration-from-talent-to-finance-and-operations-351961"></a>Adressintegration von Talent nach Finance and Operations (351961)

Diese Version behebt ein Problem, bei dem in Talent aktualisierte Adressen nicht in Finance and Operations aktualisiert wurden. Änderungen an Adressblöcken werden nun aktualisiert.

## <a name="coming-soon"></a>Bald verfügbar

### <a name="print-performance-reviews"></a>Leistungsbeurteilungen drucken

Weitere Informationen finden Sie unter [Leistungsbeurteilungen drucken](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) in Dynamics 365: Plan der 2. Veröffentlichungswelle 2019.

### <a name="feature-management-workspace"></a>Arbeitsbereich für die Funktionsverwaltung

Funktionen werden in jeder Version hinzugefügt und aktualisiert. Die Funktionsverwaltungserfahrung bietet einen Arbeitsbereich, in dem Sie eine Liste mit Funktionen anzeigen können, die in jeder Version geliefert wurden. Standardmäßig sind neue Funktionen ausgeschaltet. Sie können den Arbeitsbereich verwenden, um sie zu aktivieren und die Dokumentation für sie anzuzeigen.

Weitere Informationen über die Änderungen, die in der Funktionsverwaltung enthalten sind, finden Sie unter [Überblick über die Funktionsverwaltung](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).
