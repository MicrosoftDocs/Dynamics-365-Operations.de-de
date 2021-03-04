---
title: Neuerungen oder Änderungen in Dynamics 365 Talent (29. Oktober 2019)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 Talent entweder neu oder geändert sind.
author: Darinkramer
manager: AnnBe
ms.date: 10/29/2019
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
ms.search.validFrom: 2019-10-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 09d53c82b4244f20d0d7f301691b01263258a32f
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529683"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-29-2019"></a>Neuerungen oder Änderungen in Dynamics 365 Talent (29. Oktober 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

In diesem Thema werden die Funktionen beschrieben, die in Dynamics 365 Talent neu oder geändert wurden.

## <a name="changes-in-attract"></a>Änderungen in Attract

Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Änderungen in Onboard

Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Core HR-Änderungen

Die in diesem Abschnitt beschriebenen Änderungen gelten für Buildnummer 8.1.2586. Die Zahlen in Klammern in einigen Überschriften beziehen sich auf Supportnummern in Microsoft Dynamics Lifecycle Services (LCS).

### <a name="delete-parties-with-no-roles-should-be-on-by-default-371233"></a>Löschparteien ohne Rollen sollten standardmäßig eingeschaltet sein (371233).

Wenn Sie eine neue Umgebung in Talent bereitstellen, ist **Partner löschen, wenn keine Rollen vorhanden sind** standardmäßig eingeschaltet. Wenn Sie einen Mitarbeiter löschen, wird die mit dem Mitarbeiter verbundene Partei nur dann entfernt, wenn diese Einstellung eingeschaltet ist. Diese Änderung begrenzt doppelte Datensätze im globalen Adressbuch, wenn Sie Mitarbeiter importieren, ändern oder reimportieren müssen.

### <a name="draft-and-cancelled-leave-requests-should-be-allowed-to-be-deleted-in-common-data-service-376999"></a>Entwürfe und stornierte Urlaubsanträge sollten in Common Data Service (376999) gelöscht werden können.

Mit dieser Änderung können Sie nun in Common Data Service Urlaubsanträge mit dem Status **Entwurf** oder **Storniert** löschen.

### <a name="additional-list-values-in-custom-fields-arent-reflected-in-common-data-service-after-clicking-apply-on-the-custom-fields-form-379599"></a>Zusätzliche Listenwerte in benutzerdefinierten Feldern werden nach dem Klicken auf Übernehmen im Formular Benutzerdefinierte Felder (379599) nicht in Common Data Service angezeigt.

Wenn Sie neue Listenwerte zu einem bestehenden benutzerdefinierten Feld hinzufügen, das bereits mit Common Data Service synchronisiert wurde, sind sie nun im Gemeinsamen Datenservice verfügbar, nachdem Sie Ihre Änderungen im Formular **Benutzerdefinierte Felder** übernommen haben.

### <a name="apply-onboarding-checklists-across-legal-entities-when-more-than-one-employment-exists-371270"></a>Anwendung von Onboarding-Checklisten bei mehr als einer Beschäftigung in allen Rechtspersonen (371270)

In der Freigabe dieser Woche können Sie Checklisten auf Mitarbeiter mit mehr als einer Beschäftigung in **Arbeiterformular > Checklisten** anwenden.

### <a name="benefits-open-enrollment-preview-feature-has-been-removed"></a>Die Vorschau der Vorteile der offenen Registrierung wurde entfernt.

In Verbindung mit unserer Ankündigung in der Rubrik [Strategische Investitionen in Core HR fördern die operative Exzellenz](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence) Blog-Post, hat Microsoft die Vorteile der offenen Registrierungsfunktion aus der öffentlichen Vorschau entfernt. Neue Funktionen werden in Zukunft veröffentlicht. Die produktive Nutzung der Vorteile der offenen Registrierungsfunktion wird nicht unterstützt.

## <a name="coming-soon"></a>Bald verfügbar

### <a name="print-performance-reviews"></a>Leistungsbeurteilungen drucken

Weitere Informationen finden Sie unter [Leistungsbeurteilungen drucken](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) in Dynamics 365: Plan der 2. Veröffentlichungswelle 2019.

### <a name="feature-management-workspace"></a>Arbeitsbereich für die Funktionsverwaltung

Funktionen werden in jeder Version hinzugefügt und aktualisiert. Die Funktionsverwaltungserfahrung bietet einen Arbeitsbereich, in dem Sie eine Liste mit Funktionen anzeigen können, die in jeder Version geliefert wurden. Standardmäßig sind neue Funktionen ausgeschaltet. Sie können den Arbeitsbereich verwenden, um sie zu aktivieren und die Dokumentation für sie anzuzeigen.

Weitere Informationen über die Änderungen, die in der Funktionsverwaltung enthalten sind, finden Sie unter [Überblick über die Funktionsverwaltung](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).


[!INCLUDE[footer-include](../includes/footer-banner.md)]