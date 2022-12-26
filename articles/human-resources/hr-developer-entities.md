---
title: Dataverse-Tabellen
description: Microsoft Dynamics 365 Human Resources verwendet Dataverse, um Erweiterbarkeit und Integrationsszenarien zu ermöglichen.
author: twheeloc
ms.date: 12/08/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 51be30f10c8e5f5e962f54f720f66c712a785835
ms.sourcegitcommit: bdee5e642d417a13abdb778c14ec5f2dbbf8dee7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2022
ms.locfileid: "9838581"
---
# <a name="dataverse-tables"></a>Dataverse-Tabellen


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Dynamics 365 Human Resources verwendet Dataverse, um Erweiterbarkeit und Integrationsszenarien zu ermöglichen.

> [!NOTE]
> Human Resources-Entitäten entsprechen Dataverse-Tabellen. Weitere Informationen zu Dataverse (früher Common Data Service) und Terminologie-Updates finden Sie unter [Was ist Microsoft Dataverse ?](/powerapps/maker/data-platform/data-platform-intro)

Die folgenden Dataverse-Tabellen sind basierend auf Human Resources-Entitäten verfügbar.

Weitere Informationen zu bekannten Problemen finden Sie unter [Problemsuche in Lifecycle Services (LCS)](/dev-itpro/lifecycle-services/issue-search-lcs).

## <a name="benefit-tables"></a>Vorteilstabellen

| Name | Tabelle | Bekannte Probleme  | Status |
| --- | --- |    --------|----------  |
| Vorteilsberechnungshäufigkeit | cdm_benefitcalculationfrequency |     |     |
| Berechnungshäufigkeit Lohnperiode für Vergütungen | cdm_benefitcalculationfrequencypayperiod |     |     |
| Vergütungsberechnungssatz | cdm_benefitcalculationrate |    |     |
| Vergütungsberechnungssatz-Detail | cdm_benefitcalculationratedetail |753225 | Geklärt  |
| Vergütungsoption | cdm_benefitoption |    |     |
| Vergütungsplan | cdm_benefitplan (Nicht aktiviert für benutzerdefinierte Feldunterstützung) |    |     |
| Vergütungstyp | cdm_benefittype |    |     |

## <a name="business-process-tasks-tables"></a>Tabellen von Geschäftsprozessaufgaben

| Name | Tabelle |Bekannte Probleme  | Status |
| --- | --- |   --------|----------   |
| Geschäftsprozesskalender | cdm_businessprocesscalendar | 751867 | Geklärt |
| Zuweisung der Geschäftsprozessgruppe | cdm_businessprocessgroupassignment | 751869/751863 | Aktiv|
| Geschäftsprozessbibliothek-Aufgabengruppe | cdm_businessprocesslibrarytaskgroup |751866 | Abgeschlossen |
| Geschäftsprozessphase | cdm_businessprocessstage |      |     |
| Kopfzeile der Prüflistenvorlage | cdm_businessprocesstemplateheader |     |     |
| Prüflistenvorlagen-Aufgabe | cdm_businessprocesstemplatetask |      |     |

## <a name="compensation-tables"></a>Vergütungstabellen

| Name | Tabelle |Bekannte Probleme  | Status |
| --- | --- | ----------      | -------    |
| Plan mit fester Vergütung | cdm_compensationfixedplan |754453 | Abgeschlossen |
| Vergütungsraster | cdm_compensationgrid |             |     |
| Vergütungsstufe | cdm_compensationlevel |           |     |
| Häufigkeit der Vergütungszahlung | cdm_compensationpayfrequency |                  |     |
| Vergütungsreferenzpunkten einrichten | cdm_compensationreferencepointsetup |               |     |
| Vergütungsreferenzpunktzeile einrichten | cdm_compensationreferencepointsetupline |             |     |
| Vergütungsregion | cdm_compensationregion |                   |     |
| Vergütungsstruktur | cdm_compensationstructure |    754456        | Abgeschlossen    |
| Variabler Plan für Vergütung | cdm_compensationvariableplan |               |     |
| Variable Planstufe für Vergütung | cdm_compensationvariableplanlevel |                |     |
| Plantyp für variable Vergütung | cdm_compensationvariableplantype |               |     |
| Ereignis für feste Vergütung | cdm_fixedcompensationevent |               |     |
| Übertragungsregel | cdm_vestingrule |              |     |
| Feste Arbeitskraftvergütung | cdm_workerfixedcompensation |              |     |

## <a name="organization-tables"></a>Organisationstabellen

| Name | Tabelle |Bekannte Probleme  | Status |
| --- | --- | ----------      | -------    |
| Abteilung | cdm_department |  752194    | Abgeschlossen    |
| Beschäftigung | cdm_employment | 762414  |  Abgeschlossen  |
| Firma | cdm_company |  |     |
| Auftrag | cdm_job |  |     |
| Stellenfunktion | cdm_jobfunction |        |     |
| Position | cdm_jobposition | 752214      | Abgeschlossen    |
| Positionstyp | cdm_positiontype |            |     |
| Arbeitskraftzuweisung für die Position | cdm_positionworkerassignmentmap | 752224    |  Abgeschlossen   |
| Positionsdimension | cdm_jobpositiondimension|       |     |
| Stellentyp | cdm_jobtype |      |     |
| Sprache | cdm_language |        |     |
| Titel | cdm_title |       |     |

> [!NOTE]
> Finanzielle Dimensionen für **Positionstyp**, **Arbeitskraftzuweisung für die Position**, und **Beschäftigung** bieten eine einseitige Integration in Dataverse. Aktualisierungen der Finanzdimensionen werden derzeit nicht synchronisiert von Dataverse zu Human Resources. 

## <a name="leave-and-absence-tables"></a>Tabelle „Urlaub und Abwesenheit“

| Name | Tabelle | Bekannte Probleme  | Status |
| --- | --- |   ----------      | -------    |
| Urlaubsbankbuchung | cdm_leavebanktransaction |  752252    |    Geklärt |
| Urlaubsregistrierung | cdm_leaveenrollment |  752934    |Abgeschlossen     |
| Urlaubsplan | cdm_leaveplan |   752232   |   Abgeschlossen  |
| Urlaubsantrag | cdm_leaverequest | 753207     | Abgeschlossen    |
| Urlaubsantragdetail | cdm_leaverequestdetail | 753207     |   Abgeschlossen  |
| Urlaubstyp | cdm_leavetype |      |     |
| Ursachencode für Abwesenheitstyp | cdm_leavetypereasoncode |         |     |

>[!NOTE]
>Die Dual-Write-Integration mit Dataverse Tabellen für Urlaub und Abwesenheit ist nur verfügbar, wenn die Funktion **Mehrere Urlaubstypen in einem einzigen Urlaubsplan konfigurieren** aktiviert ist Microsoft Dynamics 365 Finance mit **Funktionsverwaltung**. 

## <a name="payroll-tables"></a>Lohntabellen

| Name | Tabelle |Bekannte Probleme  | Status |
| --- | --- |  ----------      | -------    |
| Zahlungszyklus | cdm_paycycle |    |     |
| Lohnperiode | cdm_payperiod |          |     |
| Lohneinkommenscode | cdm_payrollearningcode |   754458        |   Abgeschlossen  |
| Bankkontoauszahlungen | cdm_bankaccountdisbursement |    751904     |   Abgeschlossen  |
| Steuerregion | cdm_taxregion |          |     |

## <a name="worker-tables"></a>Arbeitskräftetabellen

| Name | Tabelle |Bekannte Probleme  | Status |
| --- | --- |----------      | -------    |
| Worker | cdm_worker |    751906    |    Abgeschlossen |
| Arbeitskraftadresse | cdm_workeraddress |   754465     |Abgeschlossen     |
| Persönliches Detail der Arbeitskraft | cdm_workerpersonaldetail |   751906     |   Abgeschlossen  |
| Personenidentifikationsnummer Arbeitskraft | cdm_workerpersonidentificationnumber |  766704      |   Abgeschlossen  |
| Personenidentifikationstyp Arbeitskraft | cdm_workerpersonidentificationtype |        |     |
| Arbeitskalender | cdm_workcalendar |        |     |
| Arbeitskalendertag | cdm_workcalendarday |        |     |
| Arbeitskalenderurlaub |cdm_workcalendarholiday |        |     |
| Arbeitskalender-Datumsposition | cdm_workcalendarholidayline |        |     |
| Arbeitskalender-Zeitintervall | cdm_workcalendartimeinterval (Nicht aktiviert für benutzerdefinierte Feldunterstützung) |        |     |
| Arbeitskraftbankkonto | cdm_workerbankaccount |        |     |

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

![Arbeitskraft](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a>Stelle und Stellenposition

![Stelle und Stellenposition.](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a>Leistungen

![Leistungen.](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a>Vergütung

![Vergütung.](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a>Verlassen

![Verlassen.](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a>Arbeitskalender

![Arbeitskalender.](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a>Siehe auch

[Eine Datenintegrationstechnologie auswählen](hr-admin-integration-choose-technology.md)<br>
[Dataverse-Integration konfigurieren](hr-admin-integration-common-data-service.md)<br>
[Virtuelle Dataverse-Tabellen konfigurieren](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[FAQ zu virtuellen Tabellen für Human Resources](hr-admin-virtual-entity-faq.md)<br>
[Was ist Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)<br>
[Terminologie-Updates](/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
