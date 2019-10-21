---
title: Neuigkeiten oder Änderungen in Dynamics 365 Talent (23. April, 2019)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 Talent entweder neu oder geändert sind.
author: Darinkramer
manager: AnnBe
ms.date: 04/23/2019
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
ms.search.validFrom: 2019-04-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 1a70be88e3ab65bb0bdd844347e8ba69e4ba61a5
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024113"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-april-23-2019"></a>Neuigkeiten oder Änderungen in Dynamics 365 Talent (23. April, 2019)

[!include [banner](includes/banner.md)]

In diesem Thema werden die Funktionen beschrieben, die in Dynamics 365 Talent neu oder geändert wurden.

## <a name="changes-in-attract"></a>Änderungen in Attract
Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Änderungen in Onboard
Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Core HR-Änderungen
Die in diesem Abschnitt beschriebenen Änderungen gelten für Buildnummer 8.1.2253. Zahlen in Klammern beziehen sich auf Supportnummern in Lifecycle Services (LCS).

### <a name="common-data-service-entity-support-for-custom-fields"></a>Common Data Service-Entitätssupport für benutzerdefinierte Felder
Bei der Version dieser Woche unterstützen die folgenden Entitäten benutzerdefinierte Felder: Kompensationsstufe, Vorteilsoption, Fähigkeitstyp und Kompensationsregion.

### <a name="additional-odata-entities-302992"></a>Zusätzliche OData-Entitäten (302992)
Die folgenden Entitäten werden jetzt in ODatas unterstützt: Arbeitskraftberufserfahrung und -ausbildung.
   
### <a name="performance-journal-attachments-for-managers-and-employees-308248"></a>Leistungserfassungsanhänge für Manager und Mitarbeiter (308248)
Mit dieser Version sind jetzt Anhänge für Manager und Mitarbeiter verfügbar, wenn sie Leistungsjournaleinträge erstellen und aktualisieren.

### <a name="employee-rehire-flag-always-available-310047"></a>Die Markierung „Neueinstellen“ ist bei Mitarbeitern immer sichtbar (310047)
Der Option zur Neueinstellung von Mitarbeitern kann nun außerhalb des Kündigungsprozesses aktualisiert werden. 

### <a name="cannot-change-the-name-of-my-payment-method-308815"></a>Der Namen von **Meine Zahlungsmethode** kann nicht geändert werden (308815)
Die Personalisierung wurde aktiviert, damit die Bezeichnung **Meine Zahlungsmethode** im „Mitarbeiter-Self-Service“ geändert werden kann.

### <a name="financial-dimensions-against-a-position-cant-be-deleted-293908"></a>Finanzdimensionen für eine Position können nicht gelöscht werden (293908)
Finanzdimensionen lassen sich nun entfernen, wenn eine Änderung für eine vorhandene Position angefordert wird und die Finanzdimensionen unternehmensübergreifend sind. 

### <a name="customer-is-unable-to-publish-back-data-into-talent-when-opening-the-data-from-excel-302955"></a>Der Debitor ist nicht in der Lage, Daten wieder in Talent zu veröffentlichen, wenn die Daten aus Excel geöffnet werden(302955)
Diese Änderung korrigiert ein Veröffentlichungsproblem bei der Verwendung verknüpfter Tabellen.

## <a name="in-preview"></a>Vorschau

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>Ermöglichen Sie, dass Ursachencodes für Sonderurlaubstypen angegeben werden können
Organisationen brauchen möglicherweise zusätzliche Informationen zu Freizeitanforderungen. Sie können nun Ursachencodes für Sonderurlaubstypen definieren und Mitarbeiter aktivieren, damit sie einen Ursachencode für ihre Freizeitanforderungen auszuwählen können.

### <a name="require-reason-codes-for-certain-leave-types-on-time-off-requests"></a>Erfordert Ursachencodes für bestimmte Urlaubstypen bei Freizeitanforderungen
Organisationen brauchen ggf. bestimmte Ursachencodes für Sonderurlaubstypen, wenn Mitarbeiter Freizeit senden. Dies kann möglicherweise aufgrund der Unternehmensrichtlinie oder von gesetzlichen Vorgaben der Fall sein. Sie können nun angeben, welche Urlaubstypen einen Ursachencodes erfordern und Sie können von Mitarbeitern verlangen, dass sie einen Ursachencode für den Sonderurlaubstyp für ihre Freizeitanforderungen angeben.

### <a name="provide-leave-and-absence-transaction-list-for-hr"></a>Erstellen Sie Urlaub- und Abwesenheitsbuchungslisten für die Personalverwaltung
Nachverfolgung von Mitarbeiterfreizeit und Verständnis dafür, wie Freizeit berechnet wird, hilft nicht nur der Personalverwaltung, Fragen von Mitarbeitern zu beantworten sonder stellt auch sicher, dass die Freizeit für Mitarbeiter korrekt ist. Personalverwaltung besitzt nun eine neue Anzeige in den Transaktionen (Abgrenzungen, Zuschüsse, Regulierungen und Anforderungen), die die Gründe hinter den Salden anzeigen.

## <a name="coming-soon"></a>Bald verfügbar

### <a name="improvements-to-the-user-interface-for-duplicate-employee-check"></a>Verbesserungen zur Benutzeroberfläche, um doppelten Mitarbeiter zu überprüfen
Mit dieser Änderung werden Duplikate erkannt, während Sie Namenfelder eingeben, und ein Status zeigt, wie viele Duplikate gefunden wurden. Sie können die zur Verfügung gestellte Verknüpfung aktivieren, um eine neue Seite zu öffnen, um zu prüfen, ob die gefundene Übereinstimmung verwendet werden soll. Das Duplikatsformular wird nicht automatisch geöffnet, damit die Dateneingabe nicht unterbrochen wird.
## <a name="known-issues"></a>Bekannte Probleme

### <a name="email-support-for-alerts"></a>E-Mail-Support für Warnungen
Durch Platform update 26 für Finance and Operations können Benutzer Warnregeln erstellen, dass automatisch E-Mail-Benachrichtigungen an Kontakte gesendet werden, wenn dies von einem Ereignis ausgelöst wird.
