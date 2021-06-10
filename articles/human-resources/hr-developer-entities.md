---
title: Dataverse-Tabellen
description: Microsoft Dynamics 365 Human Resources verwendet Dataverse, um Erweiterbarkeit und Integrationsszenarien zu ermöglichen.
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 325bd8a9de07e3978ff6c513975a0e8db22854e0
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054355"
---
# <a name="dataverse-tables"></a>Dataverse-Tabellen

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Dynamics 365 Human Resources verwendet Dataverse, um Erweiterbarkeit und Integrationsszenarien zu ermöglichen.

> [!NOTE]
> Human Resources-Entitäten entsprechen Dataverse-Tabellen. Weitere Informationen zu Dataverse (früher Common Data Service) und Terminologie-Updates finden Sie unter [Was ist Microsoft Dataverse ?](/powerapps/maker/data-platform/data-platform-intro)

Die folgenden Dataverse-Tabellen sind basierend auf Human Resources-Entitäten verfügbar.

## <a name="benefit-tables"></a>Vorteilstabellen

| Name | Tabelle |
| --- | --- |
| Vorteilsberechnungshäufigkeit | cdm_benefitcalculationfrequency |
| Berechnungshäufigkeit Lohnperiode für Vergütungen | cdm_benefitcalculationfrequencypayperiod |
| Vergütungsberechnungssatz | cdm_benefitcalculationrate |
| Vergütungsberechnungssatz-Detail | cdm_benefitcalculationratedetail |
| Vergütungsoption | cdm_benefitoption |
| Vergütungsplan | cdm_benefitplan (Nicht aktiviert für benutzerdefinierte Feldunterstützung) |
| Vergütungstyp | cdm_benefittype |

## <a name="business-process-tasks-tables"></a>Tabellen von Geschäftsprozessaufgaben

| Name | Tabelle |
| --- | --- |
| Geschäftsprozesskalender | cdm_businessprocesscalendar |
| Zuweisung der Geschäftsprozessgruppe | cdm_businessprocessgroupassignment |
| Geschäftsprozessbibliothek-Aufgabengruppe | cdm_businessprocesslibrarytaskgroup |
| Geschäftsprozessphase | cdm_businessprocessstage |
| Kopfzeile der Prüflistenvorlage | cdm_businessprocesstemplateheader |
| Prüflistenvorlagen-Aufgabe | cdm_businessprocesstemplatetask |

## <a name="compensation-tables"></a>Vergütungstabellen

| Name | Tabelle |
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
| Feste Arbeitskraftvergütung | cdm_workerfixedcompensation |

## <a name="organization-tables"></a>Organisationstabellen

| Name | Tabelle |
| --- | --- |
| Abteilung | cdm_department |
| Beschäftigung | cdm_employment |
| Firma | cdm_company |
| Auftrag | cdm_job |
| Stellenfunktion | cdm_jobfunction |
| Position | cdm_jobposition |
| Positionstyp | cdm_positiontype |
| Arbeitskraftzuweisung für die Position | cdm_positionworkerassignmentmap |
| Positionsdimension | cdm_jobpositiondimension|
| Stellentyp | cdm_jobtype |
| Sprache | cdm_language |
| Titel | cdm_title |

> [!NOTE]
> Finanzielle Dimensionen für **Positionstyp**, **Arbeitskraftzuweisung für die Position**, und **Beschäftigung** bieten eine einseitige Integration in Dataverse. Aktualisierungen der Finanzdimensionen werden derzeit nicht synchronisiert von Dataverse zu Human Resources. 

## <a name="leave-and-absence-tables"></a>Tabelle „Urlaub und Abwesenheit“

| Name | Tabelle |
| --- | --- |
| Urlaubsbankbuchung | cdm_leavebanktransaction |
| Urlaubsregistrierung | cdm_leaveenrollment |
| Urlaubsplan | cdm_leaveplan |
| Urlaubsantrag | cdm_leaverequest |
| Urlaubsantragdetail | cdm_leaverequestdetail |
| Urlaubstyp | cdm_leavetype |
| Ursachencode für Abwesenheitstyp | cdm_leavetypereasoncode |

## <a name="payroll-tables"></a>Lohntabellen

| Name | Tabelle |
| --- | --- |
| Lohnzyklus | cdm_paycycle |
| Lohnperiode | cdm_payperiod |
| Lohneinkommenscode | cdm_payrollearningcode |
| Bankkontoauszahlungen | cdm_bankaccountdisbursement |
| Steuerregion | cdm_taxregion |

## <a name="worker-tables"></a>Arbeitskräftetabellen

| Name | Tabelle |
| --- | --- |
| Worker | cdm_worker |
| Arbeitskraftadresse | cdm_workeraddress |
| Persönliches Detail der Arbeitskraft | cdm_workerpersonaldetail |
| Personenidentifikationsnummer Arbeitskraft | cdm_workerpersonidentificationnumber |
| Personenidentifikationstyp Arbeitskraft | cdm_workerpersonidentificationtype |
| Arbeitskalender | cdm_workcalendar |
| Arbeitskalendertag | cdm_workcalendarday |
| Arbeitskalenderurlaub |cdm_workcalendarholiday |
| Arbeitskalender-Datumsposition | cdm_workcalendarholidayline |
| Arbeitskalender-Zeitintervall | cdm_workcalendartimeinterval (Nicht aktiviert für benutzerdefinierte Feldunterstützung) |
| Arbeitskraftbankkonto | cdm_workerbankaccount |

## <a name="worker-setup-tables"></a>Arbeitskräfteeinrichtungstabellen

| Name | Tabelle |
| --- | --- |
| Veteranenstatus | cdm_veteranstatus |
| Nationalität | cdm_ethnicorigin |
| Ursachencode | cdm_reasoncode |
| Ausstellende Behörde für Personenkennungen | cdm_personidentificationissuingagency |

## <a name="competency-tables"></a>Kompetenztabellen

| Name | Tabelle |
| --- | --- |
| Qualifikationstyp | cdm_skilltype |

## <a name="table-relationship-models"></a>Tabellenbeziehungsmodelle

### <a name="worker"></a>Worker

![Worker](./media/HCMCommon-worker-entity-diagram.png)

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

[Eine Datenintegrationstechnologie auswählen](hr-admin-integration-choose-technology.md)<br>
[Dataverse-Integration konfigurieren](hr-admin-integration-common-data-service.md)<br>
[Virtuelle Dataverse-Tabellen konfigurieren](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[FAQ zu virtuellen Tabellen für Human Resources](hr-admin-virtual-entity-faq.md)<br>
[Was ist Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)<br>
[Terminologie-Updates](/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]