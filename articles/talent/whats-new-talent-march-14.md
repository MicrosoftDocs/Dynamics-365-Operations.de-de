---
title: Neuerungen oder Änderungen in Dynamics 365 for Talent (14. März 2019)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 for Talent entweder neu oder geändert sind.
author: Darinkramer
manager: AnnBe
ms.date: 03/14/2019
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
ms.search.validFrom: 2019-03-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 38641d6a84340112ce15335533795ed7faf91123
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518111"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-march-14-2019"></a>Neuerungen oder Änderungen in Dynamics 365 for Talent (14. März 2019)

[!include [banner](includes/banner.md)]

In diesem Thema werden die Funktionen beschrieben, die in Talent entweder neu oder geändert sind.

## <a name="changes-in-attract"></a>Änderungen in Attract
Es gibt kleinere Fehlerkorrekturen in dieser Version.

## <a name="changes-in-onboarding"></a>Änderungen in Onboarding
Es gibt kleinere Fehlerkorrekturen in dieser Version.

## <a name="changes-in-core-hr"></a>Core HR-Änderungen
**Build 8.1.2186**

### <a name="performance-management-not-working-in-all-scenarios-when-using-duplicate-security-roles"></a>Die Leistungsverwaltung arbeitet nicht in allen Szenarien, wenn doppelte Sicherheitsrollen verwendet werden
Änderungen, die in dieser Version vorgenommen werden, aktivieren Leistungsverwaltungsszenarien, wenn die Standardeinstellung oder die duplizierten Rollen verwendet werden.

### <a name="mass-assign-checklists-to-workers"></a>Massenzuweisung von Checklisten zu Arbeitskräften
Mit dieser Änderung können Sie nun mehrere Mitarbeiterauswählen und eine oder mehrere Checklisten auf einmal diesen Mitarbeitern zuweisen. 

### <a name="platform-update-24"></a>Plattformupdate 24
Weitere Details zu Platform update 24 finden Sie unter [Neues oder Änderungen in Finance and Operations platform update 24 (März 2019)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24). Signifikante Veränderungen in Plattform 24 umfassen: 

- Warnungen werden in Talent aktiviert.
- Die aktualisierte Navigationsleiste stimmt nun mit dem Office-Kopf überein.

### <a name="office-location-update-switches-the-context-to-the-top-of-the-worker-list"></a>Bürostandortaktualisierung schaltet den Kontext der Arbeitskräfteliste ganz nach oben
Mit der aktuellen Version wird der Wechsel des Bürostandorts nicht mehr den Kontext der Arbeitskraft ändern, den Sie anzeigen, wenn Sie den Bürostandort zuweisen.

### <a name="position-assignment-end-date-doesnt-display-correctly-on-worker-hire-and-transfer-actions"></a>Positionszuweisungsenddatum wird nicht ordnungsgemäß sangestellt, wenn eine Arbeitskraft eingestellt oder transferiert wird
Positionszuweisungsenddatum wird nun ordnungsgemäß basierend auf der bevorzugten Zeitzone des Benutzers angezeigt, wenn Aktivitäten verwendet wird.

### <a name="common-data-service-job-entity-doesnt-allow-job-type-and-job-function-fields-to-update"></a>Common Data Service Stellenentität erlaubt keine Stellentypen-  und Stellenfunktionsfelder zur Aktualisierung
Common Data Service Entitäten synchronisiert nun einwandfrei, wenn sie mithilfe der  Common Data Serviceaktualisiert werden.

## <a name="coming-soon"></a>Bald verfügbar

###  <a name="advanced-compensation-security-fixed-and-variable"></a>Erweiterte Vergütungssicherheit (feste oder variable)
In vielen Organisationen hat der Vergütungs- und Vorteilsmanager nur Zugriff auf bestimmte Kompensationsdatensätze. Diese Datensätze sind möglicherweise für Führungskräfte oder regionale Mitarbeiter. Mit dieser Änderung kann HR Kompensationspläne für verschiedene Mitarbeitergruppen in der Organisation verwalten. Sie können Sicherheitsrollen festen und variablen Plänen zuordnen, die den Zugriff auf die Pläne und die Mitarbeiterdaten in Verbindung mit den Plänen bestimmen, wie Gehalts- oder Zulagedatensätze. Nur die Rollen mit Zugriff sind in der Lage, Vergütungen für solche Mitarbeiter zu verarbeiten.

###  <a name="email-support-for-alerts"></a>E-Mail-Support für Warnungen
Mit der Plattformaktualisierung 24 können Benutzer die Warnregeln erstellen, dass automatisch E-Mail-Benachrichtigungen an Kontakte gesendet werden, wenn dies von einem Ereignis ausgelöst wird.

### <a name="duplicate-employee-check-interface-changes"></a>Mitarbeiterscheck duplizieren: Schnittstellenänderungen
Mit dieser Änderung werden Duplikate erkannt, während Sie Namenfelder eingeben, und ein Status zeigt, wie viele gefunden wurden. Sie können die zur Verfügung gestellte Verknüpfung aktivieren, um eine neue Seite zu öffnen, um zu prüfen, ob die gefundene Übereinstimmung verwendet werden soll. Das Duplikatsformular wird nicht automatisch geöffnet, um die Dateneingabe nicht zu unterbrechen.
