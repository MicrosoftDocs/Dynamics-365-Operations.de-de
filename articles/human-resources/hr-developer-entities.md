---
title: Common Data Service-Entitäten
description: Microsoft Dynamics 365 Human Resources verwendet Common Data Service, um Erweiterbarkeit und Integrationsszenarien zu ermöglichen.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6879a45dd1fcc1ba718747aaaf0d7936c2eac49f
ms.sourcegitcommit: 3cad15f8ecc257d3a45c1bc1fada7c094ff4bcec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/26/2020
ms.locfileid: "3087345"
---
# <a name="common-data-service-entities"></a>Common Data Service-Entitäten

Microsoft Dynamics 365 Human Resources verwendet Common Data Service, um Erweiterbarkeit und Integrationsszenarien zu ermöglichen.

Weitere Informationen zu Common Data Service finden Sie unter [Was ist Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).

Die folgenden Human Resources-Entitäten sind in Common Data Service verfügbar.

## <a name="benefit-entities"></a>Vorteilsentitäten

| Name | Entität |
| --- | --- |
| Vorteilsberechnungshäufigkeit | cdm_benefitcalculationfrequency |
| Berechnungshäufigkeit Lohnperiode für Vergütungen | cdm_benefitcalculationfrequencypayperiod |
| Vergütungsberechnungssatz | cdm_benefitcalculationrate |
| Vergütungsberechnungssatz-Detail | cdm_benefitcalculationratedetail |
| Vergütungsoption | cdm_benefitoption |
| Vergütungsplan | cdm_benefitplan (Nicht aktiviert für benutzerdefinierte Feldunterstützung) |
| Vergütungstyp | cdm_benefittype |

## <a name="business-process-tasks-entities"></a>Entitäten von Geschäftsprozessaufgaben

| Name | Entität |
| --- | --- |
| Geschäftsprozesskalender | cdm_businessprocesscalendar |
| Zuweisung der Geschäftsprozessgruppe | cdm_businessprocessgroupassignment |
| Geschäftsprozessbibliothek-Aufgabengruppe | cdm_businessprocesslibrarytaskgroup |
| Geschäftsprozessphase | cdm_businessprocessstage |
| Kopfzeile der Prüflistenvorlage | cdm_businessprocesstemplateheader |
| Prüflistenvorlagen-Aufgabe | cdm_businessprocesstemplatetask |

## <a name="compensation-entities"></a>Entschädigungseinheiten

| Name | Entität |
| --- | --- |
| Plan mit fester Vergütung | cdm_compensationfixedplan |
| Vergütungsraster | cdm_compensationgrid |
| Vergütungsstufe | cdm_compensationlevel |
| Häufigkeit der Vergütungszahlung | cdm_compensationpayfrequency |
| Vergütungsreferenzpunkten einrichten | cdm_compensationreferencepointsetup |
| Vergütungsreferenzpunktzeile einrichten | cdm_compensationreferencepointsetupline |
| Vergütungsregion | cdm_compensationregion |
| Vergütungsstruktur | cdm_compensationstructure |
| Variabler Plan für Vergütung | cdm_compensationvariableplan |
| Variable Planstufe für Vergütung | cdm_compensationvariableplanlevel |
| Plantyp für variable Vergütung | cdm_compensationvariableplantype |
| Ereignis für feste Vergütung | cdm_fixedcompensationevent |
| Übertragungsregel | cdm_vestingrule |
| Feste Vergütung für Arbeitskraft | cdm_workerfixedcompensation |

## <a name="organization-entities"></a>Organisationsentitäten

| Name | Entität |
| --- | --- |
| Abteilung | cdm_department |
| Beschäftigung | cdm_employment |
| Firma | cdm_company |
| Auftrag | cdm_job |
| Stellenfunktion | cdm_jobfunction |
| Position | cdm_jobposition |
| Positionstyp | cdm_positiontype |
| Arbeitskraftzuweisung für die Position | cdm_positionworkerassignmentmap |
| Stellentyp | cdm_jobtype |
| Sprache | cdm_language |

## <a name="leave-and-absence-entities"></a>Urlaubs- und Abwesenheitsentitäten

| Name | Entität |
| --- | --- |
| Bankgeschäft verlassen | cdm_leavebanktransaction |
| Urlaubsregistrierung | cdm_leaveenrollment |
| Urlaubsplan | cdm_leaveplan |
| Urlaubsantrag | cdm_leaverequest |
| Urlaubsantragdetail | cdm_leaverequestdetail |
| Urlaubstyp | cdm_leavetype |
| Ursachencode für Abwesenheitstyp | cdm_leavetypereasoncode |

## <a name="payroll-entities"></a>Lohnentitäten

| Name | Entität |
| --- | --- |
| Zahlungszyklus | cdm_paycycle |
| Lohnperiode | cdm_payperiod |
| Einkommenscode | cdm_payrollearningcode |
| Bankkontoauszahlungen | cdm_bankaccountdisbursement |
| Steuerregion | cdm_taxregion |

## <a name="worker-entities"></a>Arbeitskraftentitäten

| Name | Entität |
| --- | --- |
| Arbeitskraft | cdm_worker |
| Adresse Arbeitskraft | cdm_workeraddress |
| Persönliches Detail der Arbeitskraft | cdm_workerpersonaldetail |
| Personenidentifikationsnummer Arbeitskraft | cdm_workerpersonidentificationnumber |
| Personenidentifikationstyp Arbeitskraft | cdm_workerpersonidentificationtype |
| Arbeitskalender | cdm_workcalendar |
| Arbeitskalendertag | cdm_workcalendarday |
| Arbeitskalenderurlaub |cdm_workcalendarholiday |
| Arbeitskalender-Datumsposition | cdm_workcalendarholidayline |
| Arbeitskalender-Zeitintervall | cdm_workcalendartimeinterval (Nicht aktiviert für benutzerdefinierte Feldunterstützung) |
| Arbeitskraftbankkonto | cdm_workerbankaccount |

## <a name="worker-setup-entities"></a>Arbeiter-Einrichtungseinheiten

| Name | Entität |
| --- | --- |
| Veteranenstatus | cdm_veteranstatus |
| Nationalität | cdm_ethnicorigin |
| Ursachencode | cdm_reasoncode |
| Ausstellende Agentur für Personenidentifikation | cdm_personidentificationissuingagency |

## <a name="competency-entities"></a>Zuständigkeitseinheiten

| Name | Entität |
| --- | --- |
| Qualifikationstyp | cdm_skilltype |

## <a name="entity-relationship-models"></a>Entitätsbeziehungsmodelle

### <a name="worker"></a>Arbeitskraft

![Arbeitskraft](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a>Stelle und Stellenposition

![Stelle und Stellenposition](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a>Vergütungen

![Vergütungen](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a>Kompensation

![Kompensation](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a>Verlasen

![Verlasen](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a>Arbeitskalender

![Arbeitskalender](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a>Siehe auch

[Eine Datenintegrationstechnologie auswählen](hr-admin-integration-choose-technology.md)</br>
[Common Data Service-Integration konfigurieren](hr-admin-integration-common-data-service.md)