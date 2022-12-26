---
title: Integration mit Dataverse-Tabellen konfigurieren
description: In diesem Artikel wird die Integration zwischen Microsoft Dynamics 365 Human Resources und Dataverse beschrieben.
author: anschmidt
ms.date: 12/06/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2022-12-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 63c25020b7026a76ecc6e2c3563f8299627ec8a8
ms.sourcegitcommit: bdee5e642d417a13abdb778c14ec5f2dbbf8dee7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2022
ms.locfileid: "9838625"
---
# <a name="configure-integration-with-dataverse-tables"></a>Integration mit Dataverse Tabellen konfigurieren

>[!Important]
>Die in diesem Artikel beschriebene Funktionalität ist derzeit für Kunden aus dem Bereich Dynamics 365 Human Resources auf der Finanzen und Betrieb-Infrastruktur verfügbar. 


Um Microsoft Dynamics 365 Human Resources mit Dataverse zu integrieren, können Sie den [Data Integrator](/powerapps/administrator/data-integrator) verwenden. Die Vorlage Human Resources–to–Dataverse ermöglicht es, dass Daten für Jobs, Positionen, Arbeiter und andere von Human Resources nach Dataverse und von Dataverse nach Human Resources fließen Ressourcen, Erstellen eines Schreibvorgangs in beiden Systemen.

## <a name="system-requirements-for-human-resources"></a>Systemanforderungen für Human Resources

Die Integrationslösung erfordert die folgenden Versionen von Human Resources und Dynamics 365 Finance: 

- Dynamics 365 Finance Version 7.2 und höher
- Dynamics CRM Umgebung, in der eine Datenbank erstellt wurde und Dynamics 365-Apps zulässig sind

## <a name="template-and-tasks"></a>Vorlage und Aufgaben

Befolgen Sie diese Schritte, um auf die Vorlage Human Resources to Finance zuzugreifen.

1. Öffnen Sie das [Power Apps Admin Center](https://admin.powerapps.com/). 
2. Wählen Sie unter Ihrer Umgebung **Dynamics 365-Apps** und dann auf der Symbolleiste **App-Quelle** aus.
3. Um die Vorlage zu installieren, suchen Sie nach „Dual-write Human Resources“ oder rufen Sie direkt die folgende Adresse auf: <https://appsource.microsoft.com/product/dynamics-365/mscrm.hcm_dualwrite>.
3. Öffnen Sie nach Abschluss der Installation Dynamics 365 Finance.
4. Öffnen Sie den Arbeitsbereich **Datenverwaltung**. 
5. Wählen Sie **Duales Schreiben**. 
6. Befolgen Sie den Prozess zum Verknüpfen Ihrer Umgebung mit mindestens einem Unternehmen in Ihrer Organisation. 
7. Wenn Sie mit dem Einrichten eines Links zu Ihrer Dataverse Umgebung fertig sind, wählen Sie **Lösung anwenden** aus. Die Lösung wird angewendet und die Zuordnungen werden in der Integrator-App installiert.

## <a name="template-mappings"></a>Vorlagenzuordnungen

In den folgenden Vorlagenzuordnungstabellen bezeichnet der Name der Aufgabe die in jeder Anwendung verwendeten Entitäten. Finanzen befindet sich auf der linken Seite und Dataverse auf der rechten Seite.

### <a name="bank-account-disbursements-dual-write-to-bank-account-disbursement"></a>Bankkontoauszahlungen (Dual-Write) an Bankkontoauszahlungen

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| ACCOUNTIDENTIFICATIONID        | cdm\_bankaccountid.cdm\_accountidentification        |
| BETRAG                         | cdm\_amount                                         |
| Priorität                       | cdm\_disbursementpriority                           |
| PERSONALNUMMER                | cdm\_bankaccountid.cdm\_workerid.cdm\_workernumber    |
| Rest                      | cdm\_isremainder                                    |

### <a name="benefit-calculation-rate-detail-dual-write-to-benefit-calculation-rate-detail"></a>Der Vorteilsberechnungssatz des Vorteilsberechnungssatz-Details (Duales Schreiben)

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| CONTRIBUTIONMETHOD             | cdm\_contributionmethod                             |
| Effektiv                      | cdm\_effective                                      |
| EMPLOYERCONTRIBUTION           | cdm\_employercontribution                           |
| Ablauf                     | cdm\_expiration                                     |
| WORKERDEDUCTION                | cdm\_workerdeduction                                |
| NAME                           | cdm\_calculationrateid.cdm\_name                     |

### <a name="benefit-calculation-rate-header-to-benefit-calculation-rate"></a>Die Kopfzeile des Vorteilsberechnungssatzes des Vorteilsberechnungssatzes

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| BESCHREIBUNG                    | cdm\_description                                    |
| NAME                           | cdm\_name                                           |
| TIERTYPE                       | cdm\_tiertype                                       |

### <a name="benefit-option-to-benefit-option"></a>Vorteilsoption zu Vorteilsoption

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| ALLOWBENEFICIARYDESIGNATIONS   | cdm\_allowbeneficiarydesignations                   |
| ALLOWDEPENDENTCOVERAGE         | cdm\_allowdependentcoverage                         |
| BENEFITOPTIONID                | cdm\_name                                           |
| BESCHREIBUNG                    | cdm\_description                                    |
| ISWAIVE                        | cdm\_iswaived                                       |

### <a name="benefit-type-to-benefit-type"></a>Leistungstyp zu Leistungstyp

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| BENEFITTYPEID                  | cdm\_name                                           |
| CONCURRENTENROLLMENT           | cdm\_concurrentenrollment                           |
| BESCHREIBUNG                    | cdm\_description                                    |
| PAYROLLCATEGORY                | cdm\_payrollcategory                                |

### <a name="business-calendar-to-business-process-calendar"></a>Geschäftskalender zum Geschäftsprozesskalender

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| CALENDARID                     | cdm\_name                                           |
| NAME                           | cdm\_calendarname                                   |
| STARTDATE                      | cdm\_startdate                                      |
| ENDDATE                        | cdm\_enddate                                        |
| ISOPENMONDAY                   | cdm\_ismondayopen                                   |
| ISOPENTTUESDAY                  | cdm\_istuesdayopen                                  |
| ISOPENWEDNESDAY                | cdm\_iswednesdayopen                                |
| ISOPENTHURSDAY                 | cdm\_isthursdayopen                                 |
| ISOPENFRIDAY                   | cdm\_isfridayopen                                   |
| ISOPENSATURDAY                 | cdm\_issaturdayopen                                 |
| ISOPENSUNDAY                   | cdm\_issundayopen                                   |

### <a name="business-process-to-business-process-header"></a>Geschäftsprozess zu Geschäftsprozesskopfzeile

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| PROCESSID                      | cdm\_processid                                      |
| PROCESSTYPE                    | cdm\_processtype                                    |
| GENERICSUBTYPE                 | cdm\_genericsubtype                                 |
| NAME                           | cdm\_name                                           |
| BESCHREIBUNG                    | cdm\_description                                    |
| Status                         | cdm\_status                                         |
| TARGETDATE                     | cdm\_targetdate                                     |
| STARTDATETIME                  | cdm\_startdatetime                                  |
| ENDDATETIME                    | cdm\_enddatetime                                    |
| RESOLVEDBYPERSONNELNUMBER      | cdm\_resolvedbyid.cdm\_workernumber                  |
| PROCESSOWNERPERSONNELNUMBER    | cdm\_processownerid.cdm\_workernumber                |
| SOURCETEMPLATENAME             | cdm\_sourcetemplateid.cdm\_name                      |
| SOURCETEMPLATEPROCESSTYPE      | cdm\_sourcetemplateid.cdm\_businessprocesstype       |
| SOURCETEMPLATEGENERICSUBTYPE   | cdm\_sourcetemplateid.cdm\_genericsubtype            |

### <a name="business-process-library-task-group-to-business-process-library-task-group"></a>Aufgabengruppe Geschäftsprozessbibliothek zu Aufgabengruppe Geschäftsprozessbibliothek

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| PROCESSTYPE                    | cdm\_processtype                                    |
| NAME                           | cdm\_name                                           |
| BESCHREIBUNG                    | cdm\_description                                    |

### <a name="business-process-stage-to-business-process-stage"></a>Geschäftsprozessstufe zu Geschäftsprozessstufe

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| PROCESSTYPE                    | cdm\_businessprocesstype                            |
| NAME                           | cdm\_name                                           |
| BESCHREIBUNG                    | cdm\_description                                    |
| SEQUENCENUMBER                 | cdm\_sequencenumber                                 |

### <a name="business-process-task-to-business-process-task"></a>Geschäftsprozessaufgabe zu Geschäftsprozessaufgabe

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| BESCHREIBUNG                    | cdm\_description                                    |
| DUEDATE                        | cdm\_duedate                                        |
| TASKID                         | cdm\_taskid                                         |
| Anleitung                   | cdm\_instructions                                   |
| COMPLETIONDATETIME             | cdm\_completiondatetime                             |
| ASSIGNMENTTYPE                 | cdm\_assignmenttype                                 |
| ISOPTIONAL                     | cdm\_isoptional                                     |
| NAME                           | cdm\_name                                           |
| Status                         | cdm\_status                                         |
| RESOLVEDBY\_PERSONNELNUMBER     | cdm\_resolvedbyid.cdm\_workernumber                  |
| TEMPLATETASKID                 | cdm\_templatetaskid.cdm\_taskid                      |
| ASSIGNEDWORKER\_PERSONNELNUMBER | cdm\_assignedworkerid.cdm\_workernumber              |
| PROCESSID                      | cdm\_processheaderid.cdm\_processid                  |
| ASSIGNEDGROUP\_NAME             | cdm\_assignedgroupid.cdm\_name                       |
| ASSIGNEDPOSITION\_POSITIONID    | cdm\_assignedposition.cdm\_jobpositionnumber         |

### <a name="business-process-template-to-checklist-template-header"></a>Geschäftsprozessvorlage zum Checklistenvorlagenkopf

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| PROCESSTYPE                    | cdm\_businessprocesstype                            |
| GENERICSUBTYPE                 | cdm\_genericsubtype                                 |
| NAME                           | cdm\_name                                           |
| BESCHREIBUNG                    | cdm\_description                                    |
| CALENDARID                     | cdm\_businessprocesscalendarid.cdm\_name             |
| PERSONALNUMMER                | cdm\_processownerid.cdm\_workernumber                |
| ISACTIVE                       | cdm\_isactive                                       |

### <a name="business-process-template-task-to-checklist-template-task"></a>Geschäftsprozessvorlageaufgabe zum Checklistenvorlagenaufgabe

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| TASKID                         | cdm\_taskid                                         |
| NAME                           | cdm\_name                                           |
| TEMPLATEHEADER\_PROCESSTYPE     | cdm\_businessprocesstemplateheaderid.cdm\_businessprocesstype |
| TEMPLATEHEADER\_GENERICSUBTYPE  | cdm\_businessprocesstemplateheaderid.cdm\_genericsubtype |
| TEMPLATEHEADER\_NAME            | cdm\_businessprocesstemplateheaderid.cdm\_name       |
| BESCHREIBUNG                    | cdm\_description                                    |
| DUEDATEOFFSETDAYS              | cdm\_duedateoffsetdays                              |
| MENUITEMTYPE                   | cdm\_tasklinktype                                   |
| MENUITEM                       | cdm\_tasklink                                       |
| CONTACTPERSON\_PERSONNELNUMBER  | cdm\_contactpersonid.cdm\_workernumber               |
| ASSIGNMENTTYPE                 | cdm\_assignmenttype                                 |
| ASSIGNEDWORKER\_PERSONNELNUMBER | cdm\_assignedworkerid.cdm\_workernumber              |
| ASSIGNEDPOSITION\_POSITIONID    | cdm\_assignedpositionid.cdm\_jobpositionnumber       |
| ASSIGNEDGROUP\_NAME             | cdm\_assignedgroupid.cdm\_name                       |
| ISOPTIONAL                     | cdm\_isoptional                                     |
| Anleitung                   | cdm\_instructions                                   |

### <a name="calculation-frequency-to-benefit-calculation-frequency"></a>Berechnungshäufigkeit zu Leistungsberechnungshäufigkeit

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| BESCHREIBUNG                    | cdm\_description                                    |
| FREQUENCY                      | cdm\_name                                           |
| FREQUENCYCONTROL               | cdm\_frequencycontrol                               |
| ISIMMUTABLE                    | cdm\_isimmutable                                    |

### <a name="calculation-frequency-pay-period-to-benefit-calculation-frequency-pay-period"></a>Berechnungsfrequenz-Lohnperiode zu Vorteilberechnungsfrequenz-Lohnperiode

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| CALCULATIONFREQUENCYID         | cdm\_benefitcalculationfrequencyid.cdm\_name         |
| PERIODSTARTDATE                | cdm\_payperiodid.cdm\_periodstartdate                |
| PAYCYCLEID                     | cdm\_payperiodid.cdm\_paycycleid.cdm\_name            |

### <a name="calendar-to-work-calendar"></a>Kalender zum Arbeitskalender

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| CALENDARID                     | cdm\_name                                           |
| CALENDARNAME                   | cdm\_description                                    |
| WORKCALENDARHOLIDAYID          | cdm\_workcalendarholidayid.cdm\_name                 |

### <a name="compensation-fixed-action-table-to-fixed-compensation-event"></a>Feste Aktionstabelle der Vergütung zum Ereignis der festen Vergütung

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| Aktion                         | cdm\_name                                           |
| Aktiv                         | cdm\_isactive                                       |
| BESCHREIBUNG                    | cdm\_description                                    |
| TYP                           | cdm\_eventtype                                      |

### <a name="compensation-fixed-plan-to-compensation-fixed-plan"></a>Fester Vergütungsplan zu Fester Vergütungsplan

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| Plan                           | cdm\_name                                           |
| BESCHREIBUNG                    | cdm\_description                                    |
| TYP                           | cdm\_type                                           |
| EFFECTIVEDATE                  | cdm\_effectivedate                                  |
| EXPIRATIONDATE                 | cdm\_expirationdate                                 |
| WÄHRUNG                       | cdm\_transactioncurrencyid.isocurrencycode          |
| PAYFREQUENCY                   | cdm\_payfrequency.cdm\_name                          |
| HIRERULE                       | cdm\_hirerule                                       |
| OUTOFRANGETOLERANCE            | cdm\_outofrangetolerance                            |
| RECOMMENDATIONALLOWED          | cdm\_recommendationallowed                          |
| COMPENSATIONSTRUCTURE          | cdm\_compensationgrid.cdm\_name                      |
| REFPOINTSETUPID                | cdm\_referencepointsetupline.cdm\_referencepointsetupid.cdm\_name |
| CONTROLPOINT                   | cdm\_referencepointsetupline.cdm\_name               |

### <a name="compensation-grids-to-compensation-grid"></a>Vergütungsraster zu Vergütungsraster

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| GRIDID                         | cdm\_name                                           |
| BESCHREIBUNG                    | cdm\_description                                    |
| EFFECTIVEDATE                  | cdm\_effectivedate                                  |
| EXPIRATIONDATE                 | cdm\_expirationdate                                 |
| REFERENCESETUP                 | cdm\_referencepointsetupid.cdm\_name                 |
| TYP                           | cdm\_type                                           |
| WÄHRUNG                       | cdm\_transactioncurrencyid.isocurrencycode          |

### <a name="compensation-job-function-to-job-function"></a>Job-Funktion zu Vergütung zu Job-Funktion

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| JOBFUNCTIONID                  | cdm\_name                                           |
| BESCHREIBUNG                    | cdm\_description                                    |

### <a name="compensation-job-type-to-job-type"></a>Stellentyp zu Vergütung zu Stellentyp

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| JOBTYPEID                      | cdm\_name                                           |
| BESCHREIBUNG                    | cdm\_description                                    |
| EXEMPTSTATUS                   | cdm\_exemptstatus                                   |

### <a name="compensation-pay-frequency-to-compensation-pay-frequency"></a>Häufigkeit der Vergütungszahlung zu Häufigkeit der Vergütungszahlungen

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| PAYRATECONVERSION              | cdm\_name                                           |
| Periode                         | cdm\_period                                         |
| BESCHREIBUNG                    | cdm\_description                                    |
| ANNUALCONVERSIONFACTOR         | cdm\_annualconversionfactor                         |
| HOURLYCONVERSIONFACTOR         | cdm\_hourlyconversionfactor                         |
| MONTHLYCONVERSIONFACTOR        | cdm\_monthlyconversionfactor                        |
| WEEKLYCONVERSIONFACTOR         | cdm\_weeklyconversionfactor                         |

### <a name="compensation-regions-to-compensation-region"></a>Kompensationsregionen zu Kompensationsregionen

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| BESCHREIBUNG                    | cdm\_description                                    |
| LAGERPLATZ                       | cdm\_name                                           |

### <a name="compensation-variable-plan-v2-to-compensation-variable-plan"></a>Variabler Vergütungsplan V2 zu variabler Vergütungsplan

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| VARIABLEAWARDBASIS             | cdm\_awardbasis                                     |
| AWARDBASISCALCULATION          | cdm\_awardbasiscalculation                          |
| CALCULATIONTYPE                | cdm\_calculationtype                                |
| BESCHREIBUNG                    | cdm\_description                                    |
| ENABLEENROLLMENT               | cdm\_enableenrollment                               |
| ENABLELEVELS                   | cdm\_enablelevels                                   |
| ENABLERECOMMENDATION           | cdm\_enablerecommendation                           |
| HIRERULE                       | cdm\_hirerule                                       |
| LEVERAGE100PERCENT             | cdm\_leverage100percent                             |
| LEVERAGEMAXIMUM                | cdm\_leveragemaximum                                |
| LEVERAGEMINIMUM                | cdm\_leverageminimum                                |
| LEVERAGEOVEROBJECTIVE          | cdm\_leverageoverobjective                          |
| LEVERAGEUNDEROBJECTIVE         | cdm\_leverageunderobjective                         |
| PERCENTOFBASIS                 | cdm\_percentofbasis                                 |
| PLANID                         | cdm\_name                                           |
| VARIABLECOMPENSATIONTYPE       | cdm\_variablecompensationtypeid.cdm\_name            |
| UNITCURRENCYCODE               | transactioncurrencyid.isocurrencycode              |
| UNITRELATIONSHIP               | cdm\_unitrelationship                               |
| UNITVALUE                      | cdm\_unitvalue                                      |
| NUMBEROFUNITSREAL              | cdm\_numberofunits                                  |
| EFFECTIVEDATE                  | cdm\_effectivedate                                  |
| EXPIRATIONDATE                 | cdm\_expirationdate                                 |
| VESTINGRULE                    | cdm\_vestingruleid.cdm\_name                         |
| LEVERAGETOLERANCEMAX           | cdm\_leveragetolerancemax                           |
| LEVERAGETOLERANCEMIN           | cdm\_leveragetolerancemin                           |

### <a name="compensation-variable-type-to-compensation-variable-plan-type"></a>Variabler Vergütungstyp zu variabler Vergütungstyp

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| BESCHREIBUNG                    | cdm\_description                                    |
| TYP                           | cdm\_awardtype                                      |
| VARIABLECOMPENSATIONTYPE       | cdm\_name                                           |

### <a name="compensation-vesting-rules-to-vesting-rule"></a>Vergütungs-Unverfallbarkeitsregeln zur Unverfallbarkeitsregel

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| BESCHREIBUNG                    | cdm\_description                                    |
| HINWEIS                           | cdm\_notes                                          |
| VESTINGRULE                    | cdm\_name                                           |

### <a name="department-v2-to-department"></a>Abteilung V2 an Abteilung

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| OPERATINGUNITNUMBER            | cdm\_departmentnumber                               |
| NAME                           | cdm\_name                                           |
| SEARCHNAME                     | cdm\_description                                    |
| PARTYTYPE                      | cdm\_partytype                                      |

### <a name="dual-write-tax-region-to-tax-region"></a>Doppelte Schreibsteuerregion zu Steuerregion

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| CITY                           | cdm\_city                                           |
| COUNTRYORREGION                | cdm\_countryorregion                                |
| Verwaltungsbezirk                         | cdm\_county                                         |
| STATE                          | cdm\_stateorprovince                                |
| TAXREGIONNAME                  | cdm\_name                                           |

### <a name="dual-write-worker-identification-to-worker-person-identification-number"></a>Dual-Schreib-Arbeiteridentifikation zur Arbeiter-Identifikationsnummer

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| BESCHREIBUNG                    | cdm\_description                                    |
| ENTRYTYPE                      | cdm\_entrytype                                      |
| EXPIRATIONDATE                 | cdm\_expirationdate                                 |
| IDENTIFICATIONNUMBER           | cdm\_identificationnumber                           |
| IDENTIFICATIONTYPEID           | cdm\_identificationtypeid.cdm\_name                  |
| ISPRIMARY                      | cdm\_isprimary                                      |
| ISSUEDATE                      | cdm\_issuedate                                      |
| ISSUINGAGENCYID                | cdm\_issuingagencyid.cdm\_name                       |
| WORKERNUMBER                   | cdm\_workerid.cdm\_workernumber                      |

### <a name="compensation-structure-to-compensation-structure"></a>Vergütungsstruktur zu Vergütungsstruktur

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| BETRAG                         | cdm\_amount                                         |
| Raster                           | cdm\_compensationgridid.cdm\_name                    |
| LEVELID                        | cdm\_compensationlevelid.cdm\_name                   |
| REFERENCEPOINTLINENUMBER       | cdm\_referencepointid.cdm\_linenumber                |
| REFERENCESETUP                 | cdm\_referencepointid.cdm\_referencepointsetupid.cdm\_name |
| REFERENCEPOINT                 | cdm\_referencepointid.cdm\_name                      |

### <a name="earning-code-to-payroll-earning-code"></a>Earning-Code zu Payroll Earning Code

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| EARNINGCODE                    | cdm\_name                                           |
| BESCHREIBUNG                    | cdm\_description                                    |
| INCLUDEINPAYMENTTYPE           | cdm\_includeinpaymenttype                           |
| QUANTITYUNIT                   | cdm\_quantityunit                                   |
| TRACKFMLAHOURS                 | cdm\_trackfmlahours                                 |
| ISPRODUCTIVE                   | cdm\_isproductive                                   |

### <a name="employee-fixed-compensation-to-worker-fixed-compensation"></a>Feste Vergütung für Mitarbeiter zu feste Vergütung für Mitarbeiter

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| COMPENSATIONLEVELID            | cdm\_compensationlevelid.cdm\_name                   |
| TYP                           | cdm\_compensationtype                               |
| EFFECTIVEDATE                  | cdm\_effectivedate                                  |
| EXPIRATIONDATE                 | cdm\_expirationdate                                 |
| LINENUMBER                     | cdm\_linenumber                                     |
| PAYFREQUENCY                   | cdm\_payfrequencyid.cdm\_name                        |
| PAYRATE                        | cdm\_payrate                                        |
| Plan                           | cdm\_planid.cdm\_name                                |
| POSITIONID                     | cdm\_positionid.cdm\_jobpositionnumber               |
| PROCESSTYPE                    | cdm\_processtype                                    |
| PERSONALNUMMER                | cdm\_workerid.cdm\_workernumber                      |
| Aktion                         | cdm\_eventid.cdm\_name                               |
| Schritt                           | cdm\_referencepointsetuplineid.cdm\_name             |
| REFPOINTSETUPID                | cdm\_referencepointsetuplineid.cdm\_referencepointsetupid.cdm\_name |

### <a name="employment-per-company-to-employment"></a>Beschäftigung pro Unternehmen zur Beschäftigung

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| EMPLOYMENTENDDATE              | cdm\_employmentenddate                              |
| PERSONALNUMMER                | cdm\_workerid.cdm\_workernumber                      |
| EMPLOYMENTSTARTDATE            | cdm\_employmentstartdate                            |
| WORKERTYPE                     | cdm\_workertype                                     |
| DIMENSIONDISPLAYVALUE          | cdm\_dimensiondisplayvalue                          |
| ADJUSTEDWORKERSTARTDATE        | cdm\_adjustedworkerstartdate                        |
| EMPLOYERNOTICEAMOUNT           | cdm\_employernoticeamount                           |
| EMPLOYERUNITOFNOTICE           | cdm\_employerunitofnotice                           |
| WORKERUNITOFNOTICE             | cdm\_workerunitofnotice                             |
| WORKERNOTICEAMOUNT             | cdm\_workernoticeamount                             |
| LASTDATEWORKED                 | cdm\_lastdateworked                                 |
| PROBATIONENDDATE               | cdm\_probationenddate                               |
| TRANSITIONDATE                 | cdm\_transitiondate                                 |
| TRANSITIONREASONCODENAME       | cdm\_transitionreasoncode.cdm\_name                  |
| WORKERSTARTDATE                | cdm\_workerstartdate                                |
| VALIDTO                        | cdm\_validto                                        |
| VALIDFROM                      | cdm\_validfrom                                      |

### <a name="ethnic-origins-to-ethnic-origin"></a>Ethnische Herkunft zu ethnische Herkunft

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| ETHNICORIGINID                 | cdm\_name                                           |
| BESCHREIBUNG                    | cdm\_description                                    |

### <a name="group-assignment-to-business-process-group-assignment"></a>Gruppenzuweisung zu Zuweisung der Geschäftsprozessgruppe

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| NAME                           | cdm\_name                                           |
| BESCHREIBUNG                    | cdm\_description                                    |
| ISACTIVE                       | cdm\_isactive                                       |

### <a name="identification-type-to-worker-person-identification-type"></a>Kennungstyp zu Personenkennungstyps der Arbeitskraft

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| BESCHREIBUNG                    | cdm\_description                                    |
| IDENTIFICATIONTYPEID           | cdm\_name                                           |
| ALLOWEDVALUES                  | cdm\_allowedvalues                                  |
| FIXEDLENGTH                    | cdm\_fixedlength                                    |
| IDENTIFICATIONNUMBERFORMAT     | cdm\_identificationnumberformat                     |

### <a name="issuing-agency-to-person-identification-issuing-agency"></a>Ausstellende Behörde zu Ausstellende Behörde für Personenkennungen

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| E-MAIL                          | cdm\_email                                          |
| Durchwahl                      | cdm\_extension                                      |
| Fax                            | cdm\_fax                                            |
| ISSUINGAGENCY                  | cdm\_name                                           |
| MOBILEPHONE                    | cdm\_mobilephone                                    |
| INTERNETADDRESS                | cdm\_websiteurl                                     |
| NAME                           | cdm\_description                                    |
| PAGER                          | cdm\_pager                                          |
| SMS                            | cdm\_sms                                            |
| TELEPHONE                      | cdm\_telephone                                      |
| TELEXNUMBER                    | cdm\_telex                                          |
| ADDRESSCITY                    | cdm\_city                                           |
| ADDRESSCOUNTY                  | cdm\_county                                         |
| ADDRESSDESCRIPTION             | cdm\_addressdescription                             |
| ADDRESSSTATE                   | cdm\_stateorprovince                                |
| ADDRESSSTREET                  | cdm\_street                                         |
| ADDRESSZIPCODE                 | cdm\_postalcode                                     |
| ADDRESSCOUNTRYREGIONISOCODE    | cdm\_countryregion                                  |

### <a name="job-positions-dual-write-to-job-position"></a>Stellenangebote Duales Schreiben in Jobposition

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| POSITIONID                     | cdm\_jobpositionnumber                              |
| ACTIVATION                     | cdm\_activation                                     |
| AVAILABLEFORASSIGNMENT         | cdm\_availableforassignment                         |
| COMPENSATIONREGIONID           | cdm\_compensationregionid.cdm\_name                  |
| DEPARTMENTID                   | cdm\_departmentid.cdm\_departmentnumber              |
| BESCHREIBUNG                    | cdm\_description                                    |
| FULLTIMEEQUIVALENT             | cdm\_fulltimeequivalent                             |
| JOBID                          | cdm\_jobid.cdm\_name                                 |
| PARENTPOSITIONID               | cdm\_parentjobpositionid.cdm\_jobpositionnumber      |
| POSITIONTYPEID                 | cdm\_positiontypeid.cdm\_name                        |
| RETIREMENT                     | cdm\_retirement                                     |
| TITLEID                        | cdm\_titleid.cdm\_name                               |
| VALIDFROM                      | cdm\_validfrom                                      |
| VALIDTO                        | cdm\_validto                                        |

### <a name="jobs-dual-write-to-job"></a>Jobs Duales Schreiben in Job

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| JOBID                          | cdm\_name                                           |
| BESCHREIBUNG                    | cdm\_description                                    |
| JOBDESCRIPTION                 | cdm\_jobdescription                                 |
| ALLOWUNLIMITEDPOSITIONS        | cdm\_allowunlimitedpositions                        |
| MAXIMUMNUMBEROFPOSITIONS       | cdm\_maximumnumberofpositions                       |
| JOBFUNCTIONID                  | cdm\_jobfunctionid.cdm\_name                         |
| JOBTYPEID                      | cdm\_jobtypeid.cdm\_name                             |
| TITLEID                        | cdm\_titleid.cdm\_name                               |
| VALIDFROM                      | cdm\_validfrom                                      |
| VALIDTO                        | cdm\_validto                                        |
| DEFAULTFULLTIMEEQUIVALENCY     | cdm\_defaultfulltimeequivalent                      |

### <a name="language-codes-to-language"></a>Sprachcode in Sprache

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| LANGUAGECODEID                 | cdm\_name                                           |
| BESCHREIBUNG                    | cdm\_description                                    |

### <a name="leave-and-absence-bank-transaction-v2-to-leave-bank-transaction"></a>Beurlaubung und Abwesenheit Banktransaktion V2 zum Verlassen der Banktransaktion

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| BETRAG                         | cdm\_amount                                         |
| LEAVETYPEID                    | cdm\_leavetypeid.cdm\_type                           |
| LEAVEPLANID                    | cdm\_leaveplanid.cdm\_name                           |
| TRANSACTIONDATE                | cdm\_transactiondate                                |
| TRANSACTIONNUMBER              | cdm\_transactionnumber                              |
| PERSONALNUMMER                | cdm\_workerid.cdm\_workernumber                      |
| TRANSACTIONTYPE                | cdm\_transactiontype                                |

### <a name="leave-and-absence-enrollment-v2-to-leave-enrollment"></a>Einschreibung für Urlaub und Abwesenheit V2 zur Urlaubsanmeldung

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| STARTDATE                      | cdm\_startdate                                      |
| ENDDATE                        | cdm\_enddate                                        |
| CUSTOMDATE                     | cdm\_customdate                                     |
| ACCRUALSTARTDATE               | cdm\_accrualstartdate                               |
| ACCRUALDATEBASIS               | cdm\_accrualdatebasis                               |
| ISACCRUALSUSPENDED             | cdm\_isaccrualsuspended                             |
| LEAVEPLANID                    | cdm\_leaveplanid.cdm\_name                           |
| TIERBASIS                      | cdm\_tierbasis                                      |
| PERSONALNUMMER                | cdm\_workerid.cdm\_workernumber                      |

### <a name="leave-and-absence-plan-v2-to-leave-plan"></a>Plan für Urlaub und Abwesenheit V2 zur Urlaubsplan

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| ACCRUALFREQUENCY               | cdm\_accrualfrequency                               |
| NAME                           | cdm\_name                                           |
| BESCHREIBUNG                    | cdm\_description                                    |
| STARTDATE                      | cdm\_startdate                                      |
| LEAVETYPEID                    | cdm\_leavetypeid.cdm\_type                           |

### <a name="leave-and-absence-type-to-leave-type"></a>Urlaubs- und Abwesenheitstyp zu Urlaubstyp

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| BESCHREIBUNG                    | cdm\_description                                    |
| TYP                           | cdm\_type                                           |
| EARNINGCODEID                  | cdm\_earningcodeid.cdm\_name                         |

### <a name="leave-and-absence-type-reason-code-to-leave-type-reason-code"></a>Ursachencode zu Urlaubs- und Abwesenheitstyp zu Urlaubstyp Ursachencode

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| LEAVETYPE                      | cdm\_typeid.cdm\_type                                |
| REASONCODEID                   | cdm\_reasoncodeid.cdm\_name                          |

### <a name="leave-time-off-request-detail-to-leave-request-detail"></a>Überlassen Sie die Details des Urlaubsantrags dem Leave Request Detail

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| BETRAG                         | cdm\_amount                                         |
| LEAVEDATE                      | cdm\_leavedate                                      |
| REQUESTID                      | cdm\_leaverequestid.cdm\_leaverequestnumber          |
| TYP                           | cdm\_leavetypeid.cdm\_type                           |

### <a name="leave-time-off-request-header-to-leave-request"></a>Anforderungsheader für Arbeitsfreie Zeit zu Urlaubsantrag

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| REQUESTID                      | cdm\_leaverequestnumber                             |
| REQUESTDATE                    | cdm\_requestdate                                    |
| Status                         | cdm\_status                                         |
| COMMENT                        | cdm\_comment                                        |
| PERSONALNUMMER                | cdm\_workerid.cdm\_workernumber                      |

### <a name="levels-to-compensation-level"></a>Ebenen zu Vergütungsebenen

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| TYP                           | cdm\_type                                           |
| BESCHREIBUNG                    | cdm\_description                                    |
| Ebene                          | cdm\_name                                           |

### <a name="onboarding-process-header-to-onboard-process-header"></a>Onboardingprozesskopfzeile für Onboardingprozess-Kopfzeile

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| PROCESSID                      | cdm\_processheaderid.cdm\_processid                  |
| ONBOARDEDEMPLOYEEPERSONALNUMMER | cdm\_onboardedemployeeid.cdm\_workernumber           |
| EMPLOYMENTPERSONNELNUMBER      | cdm\_employmentid.cdm\_workerid.cdm\_workernumber     |
| LEGALENTITYID                  | cdm\_employmentid.cdm\_companyid.cdm\_companycode     |
| EMPLOYMENTSTARTDATE            | cdm\_employmentid.cdm\_employmentstartdate           |

### <a name="pay-cycle-to-pay-cycle"></a>Lohnzyklus zu Bezahlzyklus

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| PAYCYCLEID                     | cdm\_name                                           |
| BESCHREIBUNG                    | cdm\_description                                    |
| PAYCYCLEFREQUENCY              | cdm\_frequency                                      |

### <a name="pay-period-to-pay-period"></a>Zahlungsperiode zu Zahlungsperiode

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| COMMENTS                       | cdm\_description                                    |
| DEFAULTPAYMENTDATE             | cdm\_defaultpaymentdate                             |
| PAYCYCLEID                     | cdm\_paycycleid.cdm\_name                            |
| PERIODENDDATE                  | cdm\_periodenddate                                  |
| PERIODSTARTDATE                | cdm\_periodstartdate                                |
| Status                         | cdm\_status                                         |

### <a name="payroll-details-for-positions-to-payroll-position-detail"></a>Abrechnungsdetails für Positionen zu Payroll Position Detail

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| PAYCYCLEID                     | cdm\_paycycle.cdm\_name                              |
| POSITIONID                     | cdm\_position.cdm\_jobpositionnumber                 |
| VALIDFROM                      | cdm\_validfrom                                      |
| VALIDTO                        | cdm\_validto                                        |
| ANNUALREGULARHOURS             | cdm\_annualregularhours                             |
| PAIDBYLEGALENTITY              | cdm\_paidby.cdm\_companycode                         |

### <a name="position-default-dimensions-dual-write-to-job-position-dimension"></a>Standarddimensionen positionieren Duales Schreiben in Jobpositionsdimension

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| DIMENSIONDISPLAYVALUE          | cdm\_dimensiondisplayvalue                          |
| POSITIONID                     | cdm\_jobpositionid.cdm\_jobpositionnumber            |

### <a name="position-type-to-position-type"></a>Positionstyp zu Positionstyp

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| POSITIONTYPEID                 | cdm\_name                                           |
| BESCHREIBUNG                    | cdm\_description                                    |
| CLASSIFICATION                 | cdm\_classification                                 |

### <a name="position-worker-assignments-v2-to-position-worker-assignment"></a>Position der Arbeitskraftzuordnung V2 zu Position der Arbeitskraftzuordnung

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| PERSONALNUMMER                | cdm\_workerid.cdm\_workernumber                      |
| POSITIONID                     | cdm\_jobpositionid.cdm\_jobpositionnumber            |
| VALIDFROM                      | cdm\_validfrom                                      |
| VALIDTO                        | cdm\_validto                                        |
| IsPrimaryPosition              | cdm\_isprimaryposition                              |

### <a name="reason-codes-to-reason-code"></a>Ursachencodes zu Ursachencode

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| REASONCODEID                   | cdm\_name                                           |
| BESCHREIBUNG                    | cdm\_description                                    |
| ISABSENCEAPPLICABLE            | cdm\_isabsenceapplicable                            |
| ISAPPLICATIONAPPLICABLE        | cdm\_isapplicationapplicable                        |
| ISCOMPENSATIONAPPLICABLE       | cdm\_iscompensationapplicable                       |
| ISCREATENEWPOSITIONAPPLICABLE  | cdm\_iscreatenewpositionapplicable                  |
| ISEDITPOSITIONAPPLICABLE       | cdm\_iseditpositionapplicable                       |
| ISHIREAPPLICABLE               | cdm\_ishireapplicable                               |
| ISSKILLMAPPINGAPPLICABLE       | cdm\_isskillmappingapplicable                       |
| ISTERMINATIONAPPLICABLE        | cdm\_isterminationapplicable                        |
| ISTRANSFERAPPLICABLE           | cdm\_istransferapplicable                           |

### <a name="reference-point-setup-line-dual-write-to-compensation-reference-point-setup-line"></a>Referenzpunkt-Setup-Linie (Dual-Write) zu Kompensations-Referenzpunkt-Setup-Linie

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| BESCHREIBUNG                    | cdm\_description                                    |
| LINENUM                        | cdm\_linenumber                                     |
| REFPOINTID                     | cdm\_name                                           |
| REFPOINTSETUPID                | cdm\_referencepointsetupid.cdm\_name                 |

### <a name="reference-point-setups-to-compensation-reference-point-setup"></a>Referenzpunkt-Setups zu Kompensations-Referenzpunkt-Setup

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| REFERENCESETUP                 | cdm\_name                                           |
| BESCHREIBUNG                    | cdm\_description                                    |
| TYP                           | cdm\_compensationtype                               |

### <a name="skill-types-to-skill-type"></a>Fertigkeitstypen zu Fertigkeitstypen

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| SKILLTYPE                      | cdm\_name                                           |
| BESCHREIBUNG                    | cdm\_description                                    |

### <a name="titles-to-title"></a>Titel zu Titel

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| TITLEID                        | cdm\_name                                           |

### <a name="variable-compensation-level-v2-to-compensation-variable-plan-level"></a>Variabler Vergütungsebene V2 zu variabler Vergütungsplanebene

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| AWARDAMOUNT                    | cdm\_awardamount                                    |
| AWARDPERCENT                   | cdm\_awardpercent                                   |
| AWARDUNITSREAL                 | cdm\_awardunits                                     |
| COMPENSATIONLEVELID            | cdm\_compensationlevelid.cdm\_name                   |
| PLANID                         | cdm\_compensationvariableplanid.cdm\_name            |

### <a name="veteran-status-to-veteran-status"></a>Veteranenstatus zu Veteranenstatus

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| VETERANSTATUSID                | cdm\_name                                           |
| BESCHREIBUNG                    | cdm\_description                                    |
| ISPROTECTEDVETERAN             | cdm\_isprotectedveteran                             |

### <a name="work-calendar-enrollments-to-work-calendar-enrollment"></a>Arbeitskalenderanmeldungen für die Arbeitskalenderregistrierung

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| STARTDATE                      | cdm\_employmentid.cdm\_employmentstartdate           |
| PERSONALNUMMER                | cdm\_employmentid.cdm\_workerid.cdm\_workernumber     |
| CALENDARID                     | cdm\_workcalendarid.cdm\_name                        |
| COMPANYID                      | cdm\_employmentid.cdm\_companyid.cdm\_companycode     |

### <a name="work-calendar-holiday-to-work-calendar-holiday"></a>Arbeitskalenderurlaub für die Arbeitskalenderurlaub

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| Kennung                             | cdm\_name                                           |
| BESCHREIBUNG                    | cdm\_description                                    |

### <a name="work-calendar-holiday-line-to-work-calendar-holiday-line"></a>Arbeitskalenderurlaublinie für die Arbeitskalenderurlaublinie

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| HOLIDAYID                      | cdm\_workcalendarholidayid.cdm\_name                 |
| NAME                           | cdm\_name                                           |
| HOLIDAYDATE                    | cdm\_holidaydate                                    |

### <a name="worker-to-worker"></a>Arbeitskraft zu Arbeitskraft

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| PERSONALNUMMER                | cdm\_workernumber                                   |
| FIRSTNAME                      | cdm\_firstname                                      |
| MIDDLENAME                     | cdm\_middlename                                     |
| LASTNAME                       | cdm\_lastname                                       |
| WORKERTYPE                     | cdm\_type                                           |
| WORKERSTATUS                   | cdm\_status                                         |
| PRIMARYCONTACTEMAIL            | cdm\_primaryemailaddress                            |
| PRIMARYCONTACTPHONE            | cdm\_primarytelephone                               |
| PRIMARYCONTACTFACEBOOK         | cdm\_facebookidentity                               |
| PRIMARYCONTACTTWITTER          | cdm\_twitteridentity                                |
| PRIMARYCONTACTLINKEDIN         | cdm\_linkedinidentity                               |
| PRIMARYCONTACTURL              | cdm\_websiteurl                                     |
| GENDER                         | cdm\_gender                                         |
| BIRTHDATE                      | cdm\_birthdate                                      |
| NAME                           | cdm\_fullname                                       |

### <a name="worker-bank-accounts-to-worker-bank-account"></a>Worker-Bankkonten auf Worker-Bankkonto

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| ACCOUNTIDENTIFICATION          | cdm\_accountidentification                          |
| ADDRESSCITY                    | cdm\_city                                           |
| ADDRESSCOUNTRYREGIONID         | cdm\_countryorregion                                |
| ADDRESSCOUNTY                  | cdm\_county                                         |
| ADDRESSDESCRIPTION             | cdm\_addressdescription                             |
| ADDRESSDISTRICTNAME            | cdm\_districtname                                   |
| ADDRESSPOSTBOX                 | cdm\_postofficebox                                  |
| ADDRESSSTATE                   | cdm\_stateorprovince                                |
| ADDRESSZIPCODE                 | cdm\_postalcode                                     |
| PERSONALNUMMER                | cdm\_workerid.cdm\_workernumber                      |
| BANKACCOUNTNUMBER              | cdm\_bankaccountnumber                              |
| BANKACCOUNTTYPE                | cdm\_bankaccounttype                                |
| E-MAIL                          | cdm\_email                                          |
| EXTENSION                      | cdm\_extension                                      |
| Fax                            | cdm\_fax                                            |
| INTERNETADDRESS                | cdm\_websiteurl                                     |
| MOBILEPHONE                    | cdm\_mobilephone                                    |
| ROUTINGNUMBER                  | cdm\_routingnumber                                  |
| TELEPHONE                      | cdm\_telephone                                      |
| TELEXNUMBER                    | cdm\_telexnumber                                    |
| BANKIBAN                       | cdm\_iban                                           |
| SWIFTNO                        | cdm\_swiftcode                                      |
| BANKLOCATIONCODE               | cdm\_banklocationcode                               |
| BRANCHNAME                     | cdm\_branchname                                     |
| BRANCHNUMBER                   | cdm\_branchnumber                                   |
| ROUTINGNUMBERTYPE              | cdm\_routingnumbertype                              |
| ACCOUNTHOLDER                  | cdm\_accountholder                                  |
| NAMEOFPERSON                   | cdm\_nameofperson                                   |
| NAME                           | cdm\_description                                    |
| ADDRESSSTREET                  | cdm\_line1                                          |
| ADDRESSSTREETNUMBER            | cdm\_line2                                          |

### <a name="worker-personal-details-to-worker-personal-detail"></a>Persönliche Daten des Mitarbeiters zu persönliche Daten des Mitarbeiters

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| PERSONALNUMMER                | cdm\_workerid.cdm\_workernumber                      |
| BIRTHDATE                      | cdm\_birthdate                                      |
| PERSONBIRTHCITY                | cdm\_birthcity                                      |
| GENDER                         | cdm\_gender                                         |
| EXPATRIATEENDDATE              | cdm\_expatriateenddate                              |
| EXPATRIATESTARTDATE            | cdm\_expatriatestartdate                            |
| DISABLEDVETERAN                | cdm\_isdisabledveteran                              |
| DECEASEDDATE                   | cdm\_deceaseddate                                   |
| DISABLEDVERIFICATIONDATE       | cdm\_disabledveteranverificationdate                |
| EDUCATION                      | cdm\_education                                      |
| ETHNICORIGINID                 | cdm\_ethnicoriginid.cdm\_name                        |
| ISDISABLED                     | cdm\_isdisabled                                     |
| ISFULLTIMESTUDENT              | cdm\_isfulltimestudent                              |
| ISEXPATRIATERULINGAPPLICABLE   | cdm\_isexpatriaterulingapplicable                   |
| MARITALSTATUS                  | cdm\_maritalstatus                                  |
| MILITARYSERVICESTARTDATE       | cdm\_militaryservicestartdate                       |
| MILITARYSERVICEENDDATE         | cdm\_militaryserviceenddate                         |
| NUMBEROFDEPENDENTS             | cdm\_numberofdependents                             |
| NATIVELANGUAGEID               | cdm\_nativelanguageidid.cdm\_name                    |
| NATIONALITYCOUNTRYREGION       | cdm\_nationalitycountryregion                       |
| PERSONBIRTHCOUNTRYREGION       | cdm\_birthcountryregion                             |
| FATHERBIRTHCOUNTRYREGION       | cdm\_fatherbirthcountryregion                       |
| MOTHERBIRTHCOUNTRYREGION       | cdm\_motherbirthcountryregion                       |
| CITIZENSHIPCOUNTRYREGION       | cdm\_citizenshipcountryregion                       |
| VETERANSTATUSID                | cdm\_veteranstatusid.cdm\_name                       |

### <a name="worker-postal-addresses-dual-write-to-worker-address"></a>Arbeitskräfteadressen zu Arbeitskraft-Postanschrift Duales Schreiben

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| PERSONALNUMMER                | cdm\_workerid.cdm\_workernumber                      |
| ADDRESSLOCATIONID              | cdm\_addressnumber                                  |
| ADDRESSLOCATIONROLES           | cdm\_addresstype                                    |
| Effektiv                      | cdm\_effectivedate                                  |
| Ablauf                     | cdm\_expirationdate                                 |
| ADDRESSSTREET                  | cdm\_street                                         |
| ADDRESSSTREETNUMBER            | cdm\_streetnumber                                   |
| ADDRESSCITY                    | cdm\_city                                           |
| ADDRESSCOUNTRYREGIONISOCODE    | cdm\_countryregion                                  |
| ADDRESSSTATE                   | cdm\_stateorprovince                                |
| ADDRESSCOUNTYID                | cdm\_county                                         |
| ADDRESSDESCRIPTION             | cdm\_description                                    |
| ADDRESSLATITUDE                | cdm\_latitude                                       |
| ADDRESSLONGITUDE               | cdm\_longitude                                      |
| ADDRESSZIPCODE                 | cdm\_postalcode                                     |
| ADDRESSPOSTBOX                 | cdm\_postofficebox                                  |
| ISPRIMARY                      | cdm\_ispreferred                                    |

### <a name="working-time-to-work-calendar-time-interval"></a>Arbeitszeit zu Arbeitskalender-Zeitintervall

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| ENDTIME                        | cdm\_endtime                                        |
| STARTTIME                      | cdm\_starttime                                      |
| WORKCALENDARDATE               | cdm\_workcalendardayid.cdm\_calendardate             |
| WORKCALENDARID                 | cdm\_workcalendarid.cdm\_name                        |
| WORKCALENDARID                 | cdm\_workcalendardayid.cdm\_workcalendarid.cdm\_name  |

### <a name="working-times-to-work-calendar-day"></a>Arbeitszeiten zum Arbeitskalendertag

| Finanzentität                 | Dataverse-Tabelle                                    | 
|--------------------------------|----------------------------------------------------|
| CALENDARDATE                   | cdm\_calendardate                                   |
| WORKCALENDARID                 | cdm\_workcalendarid.cdm\_name                        |
| WORKINGDAYDEFINITION           | cdm\_status                                         |

## <a name="integration-considerations"></a>Überlegungen zur Integration

- Alle Änderungen, die an Daten in einem der beiden Systeme vorgenommen werden, unterliegen der Validierung durch das andere System. Wenn ein Fehler auftritt, werden keine Daten in beide Systeme geschrieben. 
- Alle Schreibvorgänge unterliegen Datenvorgaben (wenn benutzerdefinierte Logik in Finanzen auftritt).
- Die Dual-Write-Integrator-App verwendet Integrationsschlüssel zur Zuordnung zwischen den beiden Systemen. Manchmal ist es schwierig, den richtigen Integrationsschlüssel auszuwählen, insbesondere wenn mehrere Integrationsschlüssel die Anforderungen erfüllen. Um Ihnen bei dieser Auswahl zu helfen, listet die folgende Tabelle die vorgeschlagenen Integrationsschlüssel für Ihre Zuordnungen auf.

| Dataverse-Tabelle                          | Integrationsschlüssel |
|------------------------------------------|------------------|
| Bankkontoauszahlungen                | cdm\_bankaccountid.cdm\_accountidentification, cdm\_bankaccountid.cdm\_workerid.cdm\_workernumber, cdm\_companyid.cdm\_companycode |
| Vorteilsberechnungshäufigkeit            | cdm\_name |
| Berechnungshäufigkeit Lohnperiode für Vergütungen | cdm\_payperiodid.cdm\_periodstartdate, cdm\_payperiodid.cdm\_paycycleid.cdm\_name, cdm\_benefitcalculationfrequencyid.cdm\_name |
| Vergütungsberechnungssatz                 | cdm\_name |
| Vergütungsberechnungssatz-Detail          | cdm\_workerdeduction, cdm\_effective, cdm\_calculationrateid.cdm\_name |
| Vergütungsoption                           | cdm\_name |
| Vergütungstyp                             | cdm\_name |
| Geschäftsprozesskalender                | cdm\_name |
| Zuweisung der Geschäftsprozessgruppe        | cdm\_name |
| Geschäftsprozesskopfzeile                  | cdm\_processid |
| Geschäftsprozessbibliothek-Aufgabengruppe      | cdm\_processtype, cdm\_name |
| Geschäftsprozessphase                   | cdm\_name, cdm\_businessprocesstype, cdm\_companyid.cdm\_companycode |
| Geschäftsprozessaufgabe                    | cdm\_taskid |
| Unternehmenseinheit                            | |
| Kopfzeile der Prüflistenvorlage                | cdm\_businessprocesstype, cdm\_name, cdm\_genericsubtype |
| Prüflistenvorlagen-Aufgabe                  | cdm\_taskid |
| Firma                                  | cdm\_companycode |
| Plan mit fester Vergütung                  | cdm\_name, cdm\_company.cdm\_companycode |
| Vergütungsraster                        | cdm\_name, cdm\_companyid.cdm\_companycode |
| Vergütungsstufe                       | cdm\_name |
| Häufigkeit der Vergütungszahlung               | cdm\_name, cdm\_companyid.cdm\_companycode |
| Vergütungsreferenzpunkten einrichten       | cdm\_name, cdm\_companyid.cdm\_companycode |
| Vergütungsreferenzpunktzeile einrichten  | cdm\_name, cdm\_referencepointsetupid.cdm\_name, cdm\_referencepointsetupid.cdm\_companyid.cdm\_companycode |
| Vergütungsregion                      | cdm\_name |
| Vergütungsstruktur                   | cdm\_compensationlevelid.cdm\_name, cdm\_referencepointid.cdm\_name, cdm\_referencepointid.cdm\_referencepointsetupid.cdm\_name, cdm\_referencepointid.cdm\_referencepointsetupid.cdm\_companyid.cdm\_companycode, cdm\_companyid.cdm\_companycode, cdm\_compensationgridid.cdm\_name, cdm\_compensationgridid.cdm\_companyid.cdm\_companycode |
| Variabler Plan für Vergütung               | cdm\_name, cdm\_companyid.cdm\_companycode |
| Variable Planstufe für Vergütung         | cdm\_companyid.cdm\_companycode, cdm\_compensationvariableplanid.cdm\_name, cdm\_compensationvariableplanid.cdm\_companyid.cdm\_companycode, cdm\_compensationlevelid.cdm\_name |
| Plantyp für variable Vergütung          | cdm\_name, cdm\_companyid.cdm\_companycode |
| Währung                                 | isocurrencycode |
| Abteilung                               | cdm\_departmentnumber |
| Beschäftigung                               | cdm\_employmentstartdate, cdm\_workerid.cdm\_workernumber, cdm\_companyid.cdm\_companycode |
| Nationalität                            | cdm\_name |
| Ereignis für feste Vergütung                 | cdm\_name, cdm\_companyid.cdm\_companycode |
| Auftrag                                      | cdm\_name |
| Stellenfunktion                             | cdm\_name |
| Position                             | cdm\_jobpositionnumber |
| Positionsdimension                   | cdm\_jobpositionid.cdm\_jobpositionnumber, cdm\_companyid.cdm\_companycode |
| Stellentyp                                 | cdm\_name |
| Sprache                                 | cdm\_name |
| Urlaubsbankbuchung                   | cdm\_transactiondate, cdm\_transactiontype, cdm\_transactionnumber, cdm\_leavetypeid.cdm\_type, cdm\_leavetypeid.cdm\_companyid.cdm\_companycode, cdm\_companyid.cdm\_companycode, cdm\_workerid.cdm\_workernumber |
| Urlaubsregistrierung                         | cdm\_startdate, cdm\_leaveplanid.cdm\_name, cdm\_leaveplanid.cdm\_companyid.cdm\_companycode, cdm\_companyid.cdm\_companycode, cdm\_workerid.cdm\_workernumber |
| Urlaubsplan                               | cdm\_name, cdm\_companyid.cdm\_companycode |
| Urlaubsantrag                            | cdm\_leaverequestnumber, cdm\_companyid.cdm\_companycode |
| Urlaubsantragdetail                     | cdm\_leavedate, cdm\_leavetypeid.cdm\_type, cdm\_leavetypeid.cdm\_companyid.cdm\_companycode, cdm\_leaverequestid.cdm\_leaverequestnumber, cdm\_leaverequestid.cdm\_companyid.cdm\_companycode |
| Urlaubstyp                               | cdm\_type, cdm\_companyid.cdm\_companycode |
| Ursachencode für Abwesenheitstyp                   | cdm\_reasoncodeid.cdm\_name, cdm\_typeid.cdm\_type, cdm\_typeid.cdm\_companyid.cdm\_companycode |
| Onboardingprozesskopfzeile                   | cdm\_processheaderid.cdm\_processid |
| Organisation                             | |
| Zahlungszyklus                                | cdm\_name |
| Lohnperiode                               | cdm\_periodstartdate, cdm\_paycycleid.cdm\_name, cdm\_periodenddate |
| Lohneinkommenscode                     | cdm\_name |
| Lohnposition - Detail                  | cdm\_validfrom, cdm\_validto, cdm\_position.cdm\_jobpositionnumber |
| Ausstellende Behörde für Personenkennungen     | cdm\_name |
| Positionstyp                            | cdm\_name |
| Arbeitskraftzuweisung für die Position               | cdm\_validfrom, cdm\_jobpositionid.cdm\_jobpositionnumber |
| Ursachencode                              | cdm\_name |
| Qualifikationstyp                               | cdm\_name |
| Steuerregion                               | cdm\_stateorprovince, cdm\_name, cdm\_countryorregion, cdm\_county, cdm\_city |
| Team                                     | azureactivedirectoryobjectid, membershiptype |
| Titel                                    | cdm\_name |
| User                                     | azureactivedirectoryobjectid |
| Übertragungsregel                             | cdm\_name, cdm\_companyid.cdm\_companycode |
| Veteranenstatus                           | cdm\_name |
| Arbeitskalender                            | cdm\_name, cdm\_companyid.cdm\_companycode |
| Arbeitskalendertag                        | cdm\_calendardate, cdm\_companyid.cdm\_companycode, cdm\_workcalendarid.cdm\_name, cdm\_workcalendarid.cdm\_companyid.cdm\_companycode |
| Arbeitskalenderregistrierung                 | cdm\_employmentid.cdm\_employmentstartdate, cdm\_employmentid.cdm\_workerid.cdm\_workernumber, cdm\_employmentid.cdm\_companyid.cdm\_companycode |
| Arbeitskalenderurlaub                    | cdm\_name |
| Arbeitskalender-Datumsposition               | cdm\_holidaydate, cdm\_workcalendarholidayid.cdm\_name |
| Arbeitskalender-Zeitintervall              | cdm\_starttime, cdm\_workcalendardayid.cdm\_calendardate, cdm\_workcalendardayid.cdm\_companyid.cdm\_companycode, cdm\_workcalendardayid.cdm\_workcalendarid.cdm\_name, cdm\_workcalendardayid.cdm\_workcalendarid.cdm\_companyid.cdm\_companycode, cdm\_companyid.cdm\_companycode, cdm\_workcalendarid.cdm\_name, cdm\_workcalendarid.cdm\_companyid.cdm\_companycode |
| Worker                                   | cdm\_workernumber |
| Arbeitskraftadresse                           | cdm\_addressnumber, cdm\_addresstype, cdm\_workerid.cdm\_workernumber |
| Arbeitskraftbankkonto                      | cdm\_accountidentification, cdm\_workerid.cdm\_workernumber |
| Feste Arbeitskraftvergütung                | cdm\_linenumber, cdm\_effectivedate, cdm\_companyid.cdm\_companycode, cdm\_positionid.cdm\_jobpositionnumber, cdm\_workerid.cdm\_workernumber, cdm\_eventid.cdm\_name, cdm\_eventid.cdm\_companyid.cdm\_companycode, cdm\_planid.cdm\_name, cdm\_planid.cdm\_company.cdm\_companycode |
| Personenidentifikationsnummer Arbeitskraft      | cdm\_identificationnumber, cdm\_workerid.cdm\_workernumber, cdm\_identificationtypeid.cdm\_name |
| Personenidentifikationstyp Arbeitskraft        | cdm\_name |
| Persönliches Detail der Arbeitskraft                   | cdm\_workerid.cdm\_workernumber |
