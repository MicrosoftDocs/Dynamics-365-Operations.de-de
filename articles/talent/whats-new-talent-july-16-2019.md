---
title: Neuerungen und Änderungen in Dynamics 365 Talent (16. Juli 2019)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 Talent entweder neu oder geändert sind.
author: Darinkramer
manager: AnnBe
ms.date: 07/16/2019
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
ms.search.validFrom: 2019-07-16
ms.dyn365.ops.version: Talent
ms.openlocfilehash: fd70b29089a4bf05c8fa9e3591fdb22383ea0cdc
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009715"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-july-16-2019"></a>Neuerungen und Änderungen in Dynamics 365 Talent (16. Juli 2019)

[!include [banner](includes/banner.md)]

In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 Talent entweder neu oder geändert sind.

## <a name="changes-in-attract"></a>Änderungen in Attract
Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Attract.

### <a name="coming-soon-in-attract"></a>Bald verfügbar in Attract
#### <a name="job-approvals-appear-on-the-home-page"></a>Stellengenehmigungen werden auf der Startseite angezeigt

Genehmigungen werden im Abschnitt **Genehmigungen** im Dashboard angezeigt. Genehmiger können ihre Genehmigungen unter **Ihnen zugewiesen** überprüfen. Sie zeigen die Stellen-ID, den Stellen-Titel, andere Genehmiger und das Datum an, an der die Stelle zugewiesen wurde. Benutzer, die eine Stelle zur Genehmigung übermitteln, können ihre Stellen unter **Von Ihnen angefordert** überprüfen. Dort werden die Genehmiger angezeigt, die immer noch die übermittelte Stelle genehmigen müssen.

## <a name="changes-in-onboard"></a>Änderungen in Onboard
Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Core HR-Änderungen
Die in diesem Abschnitt beschriebenen Änderungen gelten für Buildnummer 8.1.2390.

### <a name="common-data-service-entities-that-now-support-custom-fields"></a>Common Data Service Entitäten, die nun benutzerdefinierte Felder unterstützen

- BusinessProcessCalendar                     
- BusinessProcessGroupAssignment         
- BusinessProcessStage                          
- BusinessProcessTemplateHeader          
- BusinessProcessTemplateTask            
- HcmBenefitOption                              
- HcmBenefitType                                  
- HcmCompensationGrid                            
- HcmCompensationLevel                          
- HcmCompensationPayFrequency                 
- HcmCompensationReferencePointSetup        
- HcmCompensationReferencePointSetupLine 
- HcmCompensationRegion                     
- HcmCompFixedPlanTable                     
- HcmEmployment                                
- HcmEthnicOrigin                                
- HcmFixedCompensationEvent                 
- HcmJob                                           
- HcmJobFunction
- HcmJobType
- HcmLanguageCode
- HcmPayrollCalculationFrequency
- HcmPosition
- HcmPositionType
- HcmSkillType
- HcmVeteranStatus
- HcmWorkCalendarHoliday
- HcmWorkCalendarHolidayLine
- HcmWorker
- HcmWorkerPersonalDetail
- LeaveType
- OMDepartment
- OMLegalEntity
- PayCycle
- PayPeriod
- PayrollBenefitCalculationRate
- PayrollBenefitCalculationRateDetail
- PayrollEarningCode

### <a name="unable-to-see-goals-and-reviews-in-manager-self-service"></a>Unfähig, Zielen und Bewertungen im Self-Service-Manager anzuzeigen

Die Änderungen dieser Woche lassen jetzt die Anzeige und Bearbeitung von Zielen und Bewertungen zum Überspringen -Stufenmanager im Manager-Self-Service zu.

### <a name="goal-form-cannot-be-closed-after-a-user-edits-any-goal-field"></a>Zielformular kann nicht abgeschlossen werden, nachdem ein Benutzer ein beliebiges Zielfeld bearbeitet hat

Diese Version behebt ein Problem, in dem das Zielformular nicht geschlossen wird, wenn **Schließen** ausgewählt wird.

### <a name="creating-new-goals-and-saving-displays-error"></a>Neue Ziele erstellen und Speicherfehler anzeigen

Diese Version behebt ein Problem beim Speichern von Zielen im Mitarbeiter- und Manager-Self-Service.

### <a name="unable-to-add-a-field-to-position-details"></a>Unfähig, ein Feld den Positionsdetails hinzuzufügen 

Mit dieser Version werden benutzerdefinierte Felder nun in den Positionsdetails unterstützt.
 
### <a name="unable-to-set-up-expiring-date-on-the-earning-code-through-data-management"></a>Unfähig Ablaufdaten auf den Einkommenscode über die Datenverwaltung einzurichten

Änderungen können Sie nun zum festgelegten Ablaufdatum auf Einkommenscodes für die Datenverwaltung festlegen

### <a name="new-custom-fields-dont-sync-quickly-enough"></a>Neue benutzerdefinierte Felder synchronisieren nicht schnell genug

Leistung der benutzerdefinierten Feldsynchronisierung auf Common Data Service wurde mit der Version dieser Woche verbessert.

### <a name="entity-export-to-database-jobs-fail-with-error-message-format-of-the-initialization-string-does-not-conform-to-specification-starting-at-index-0"></a>Entitätsexport zu den Datenbankstellen schlagen fehl mit der Fehlermeldung: Format der Initialisierungszeichenfolge entspricht nicht der Spezifikation, der Start erfolgt mit Index 0.

Diese Version korrigiert das Problem, in dem Datenbankstapelverarbeitungsaufträge fehlschlagen. Um manuell zu aktualisieren:

1. Wechseln Sie zu **Datenverwaltung**.
2. Wählen Sie **Entitätsexport in Datenbank konfigurieren**.
3. Hier können Sie die Verbindungszeichenfolge für die Zieldatenbank erneut eingeben und wählen Sie dann **Speichern** aus.

### <a name="smtp-email-configuration-suddenly-fails-with-error-message-the-smtp-server-requires-a-secure-connection-or-the-client-was-not-authenticated"></a>SMTP-E-Mail-Konfiguration zeigt plötzlich Fehlermeldung an: „Der SMTP-Server erfordert eine sichere Verbindung oder der Client wurde nicht authentifiziert“.

Diese Version korrigiert eine SMTP-E-Mail-Konfiguration, die plötzlich fehlschlägt. Um manuell zu aktualisieren:

1. Gehen Sie zu **Systemverwaltung**.
2. Wählen Sie **E-Mail-Parameter anzeigen**.
3. Wählen Sie **SMTP-Einstellungen**. 
4. Geben Sie Benutzername und Kennwort erneut für den SMTP-Server ein und wählen Sie **Speichern** aus.

## <a name="in-preview"></a>Vorschau

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>Vorschaufunktionen werden nur in den Sandkasteninstanzen aktiviert

Wenn Sie eine neue Instanz von Talent bereitstellen, können Sie angeben, ob der Instanztyp **Produktion** oder **Sandkasten** ist. Die Instanzen vom **Sandkasten** Typ ermöglichen ein frühzeitiges Testen neuer Funktionen. Alle vorhandenen Talent-Instanzen werden zum Instanztyp **Produktion** aktualisiert. Wenn eine der vorhandenen Instanzen auf den aktualisierten Instanztyp **Sandkasten** aktualisiert werden soll, wenden Sie sich an den [Support](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support), um die Änderungsanforderung zu initiieren.

Weitere Informationen dazu, wie Änderungen veröffentlicht werden, finden unter [Talent bereitstellen](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

### <a name="restrict-leave-types-in-time-off-requests"></a>Begrenzen der Sonderurlaubstypen in den Abwesenheitsanforderungen

Organisationen können Mitarbeitern viele unterschiedliche Arten von Sonderurlaub anbieten. Allerdings ist er möglicherweise nicht angebracht, dass Mitarbeiter einen Freizeitantrag für bestimmte Sonderurlaubstypen senden. Diese Sonderurlaubstypen können stattdessen von der Personalverwaltung (HR) verwaltet werden. Mit dieser Version können Sie konfigurieren, für welche Sonderurlaubstypen die Mitarbeiter Abwesenheitsanforderungen übermitteln können. 

### <a name="view-performance-information-for-direct-and-extended-reports-in-manager-self-service"></a>Anzeigen von Leistungsinformationen für direkte und erweiterten Berichte im Manager Self-Service

Mit einer neuen Option können Manager die Leistung von ihren direkten Mitarbeitern und den erweiterten Mitarbeitern anzeigen. Aktuell können Linienmanager Leistungsziele zuweisen und aktualisieren und neue Überprüfungen ausstellen. Darüber hinaus können Vorgesetzte und ihre Mitarbeiter Leistungserfassungen verwalten und aktualisieren, um sicherzustellen, dass der Leistungsprüfungsprozess problemlos verläuft. Wenn diese Änderung implementiert ist, sind Manager in der Lage, leistungsbezogene Informationen neben jenen für die direkt unterstellten Mitarbeitern auch jene für ihre erweiterten Mitarbeiter anzuzeigen und zu verwalten.
