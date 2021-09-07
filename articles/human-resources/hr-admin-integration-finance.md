---
title: Integration mit Finance konfigurieren
description: Dieses Thema beschreibt die Integration zwischen Dynamics 365 Human Resources und Dynamics 365 Finance.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ba984d26c5c0b1376c0ad85e5c0665da004a46a5
ms.sourcegitcommit: 72a82e9aeabbdecf57e1aee72975c63eba75143a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/24/2021
ms.locfileid: "7414687"
---
# <a name="configure-integration-with-finance"></a>Integration mit Finance konfigurieren

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Um Dynamics 365 Human Resources in Dynamics 365 Finance zu integrieren, können Sie die Vorlage „Human Resources to Finance“ in [Datenintegrator](/powerapps/administrator/data-integrator) verwenden. Die Vorlage „Human Resources to Finance“ ermöglicht den Datenfluss für Jobs, Positionen und Mitarbeiter. Die Vorlage ermöglicht den Datenfluss von der Personalabteilung in die Finanzabteilung, jedoch nicht den Datenfluss von der Finanzabteilung in die Personalabteilung.

![Human Resources nach Finance – Integrationsfluss.](./media/hr-admin-integration-finance-flow.png)

Die Human Resources zu Finance-Lösung bietet die folgenden Arten der Datensynchronisierung:

- Verwalten von Jobs in Human Resources und Synchronisierung dieser von Human Resources nach Finance
- Verwalten von Positionen und Positionszuweisungen in Human Resources und Synchronisierung von diesen von Human Resources nach Finance
- Verwalten von Beschäftigungsverhältnissen in Human Resources und Synchronisierung dieser von Human Resources nach Finance
- Verwalten von Arbeitskräften und Arbeitskräfteadressen in Human Resources und Synchronisierung von diesen von Human Resources nach Finance

## <a name="system-requirements-for-human-resources"></a>Systemanforderungen für Human Resources

Die Integrationslösung erfordert die folgenden Versionen von Human Resources und Finance: 

- Dynamics 365 Human Resources am Dataverse
- Dynamics 365 Finance Version 7.2 und höher

## <a name="template-and-tasks"></a>Vorlage und Aufgaben

So greifen Sie auf die Vorlage Human Resources to Finance zu.

1. Öffnen Sie das [Power Apps Admin Center](https://admin.powerapps.com/). 

2. Wählen Sie **Projekte** und dann **Neues Projekt** in der oberen rechten Ecke aus. Erstellen Sie für jede juristische Person, die Sie in Finance integrieren möchten, ein neues Projekt.

3. Wählen Sie **Personalverwaltung (Human Resources Dataverse to Finance)**, um Datensätze von Human Resources nach Finance zu synchronisieren.

Die folgenden zugrunde liegenden Aufgaben werden verwendet, um Datensätze von Human Resources nach Finance zu synchronisieren:

- **Job-Funktionen zu Vergütung (Stellenfunktion)**
- **Abteilungen zu Organisationseinheit**
- **Stellentypen zu Vergütung (Stellentyp)**
- **Stellen zu Stellen**
- **Stellen zu Stellendetails**
- **Positionstypen zu Positionstyp**
- **Stellenpositionen zu Basisposition**
- **Stellenpositionen zu Positionsdetails**
- **Stellenpositionen zu Positionsdauern**
- **Stellenpositionen zu Positionshierarchien**
- **Arbeitskräfte zu Arbeitskraft**
- **Beschäftigungen zu Beschäftigung**
- **Beschäftigungen zu Beschäftigung - Details**
- **Position der Arbeitskraftzuordnung zu Position der Arbeitskraftzuordnungen**
- **Arbeitskräfteadressen zu Arbeitskraft-Postanschrift V2**

## <a name="template-mappings"></a>Vorlagenzuordnungen

In den folgenden Vorlagenzuordnungstabellen enthält der Name der Aufgabe die in jeder Anwendung verwendeten Entitäten. Die Quelle (Human Resources) befindet sich links und das Ziel (Finance) rechts.

### <a name="job-functions-to-compensation-job-function"></a>Job-Funktionen zu Vergütung (Stellenfunktion)

| Dataverse-Tabelle (Quelle) | Finance-Entität (Ziel) |
|-------------------------------------|---------------------------------------------|
| cdm_name (cdm_Job Funktionsname)  | JOBFUNCTIONID   (JOBFUNCTIONID)            |
| cdm_description   (cdm_description) | BESCHREIBUNG   (BESCHREIBUNG)                 |

### <a name="departments-to-operating-unit"></a>Abteilungen zu Organisationseinheit

| Dataverse-Tabelle (Quelle)           | Finance-Entität (Ziel) |
|-----------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                           | NAME (NAME)                                 |
| cdm_departmentnumber   (cdm_departmentnumber) | OPERATINGUNITNUMBER   (OPERATINGUNITNUMBER) |
|                                               | OPERATINGUNITTYPE   (OPERATINGUNITTYPE)     |
| cdm_description   (cdm_description)           | NAMEALIAS   (NAMEALIAS)                     |

### <a name="job-types-to-compensation-job-type"></a>Stellentypen zu Vergütung (Stellentyp)

| Dataverse-Tabelle (Quelle)   | Finance-Entität (Ziel) |
|---------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                   | JOBTYPEID   (JOBTYPEID)                     |
| cdm_description   (cdm_description)   | BESCHREIBUNG   (BESCHREIBUNG)                 |
| cdm_exemptstatus   (cdm_exemptstatus) | EXEMPTSTATUS   (EXEMPTSTATUS)               |

### <a name="jobs-to-jobs"></a>Stellen zu Stellen

| Dataverse-Tabelle (Quelle)                           | Finance-Entität (Ziel)           |
|---------------------------------------------------------------|-------------------------------------------------------|
| cdm_name (cdm_name)                                           | JOBID (JOBID)                                         |
| cdm_maximumnumberofpositions   (cdm_maximumnumberofpositions) | MAXIMUMNUMBEROFPOSITIONS   (MAXIMUMNUMBEROFPOSITIONS) |
| cdm_allowedunlimitedpositions   (cdm_allowunlimitedpositions) | ALLOWUNLIMITEDPOSITIONS   (ALLOWUNLIMITEDPOSITIONS)   |
| cdm_description   (cdm_description)                           | BESCHREIBUNG   (BESCHREIBUNG)                           |
| cdm_jobdescription   (cdm_jobdescription)                     | JOBDESCRIPTION   (JOBDESCRIPTIONS)                    |

### <a name="jobs-to-job-detail"></a>Stellen zu Stellendetails

| Dataverse-Tabelle (Quelle)                             | Finance-Entität (Ziel) |
|-----------------------------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                                             | JOBID (JOBID)                               |
| cdm_jobtypeid.cdm_name   (Job-Typ (Job-Typ-Name))             | JOBTYPEID   (JOBTYPEID)                     |
| cdm_jobfunctionid.cdm_name (Stellenfuntion (Stellenfunktionsname)) | FUNCTIONID   (FUCNTIONID)                   |
| cdm_validfrom   (gültig von)                                    | VALIDFROM   (VALIDFROM)                     |
| cdm_validto (gültig bis)                                        | VALIDTO (VALIDTO)                           |
| cdm_defaultfulltimeequivalent   (Standard-Vollzeitäquivalent)   | FULLTIMEEQUIVALENT   (FULLTIMEEQUIVALENT)   |

### <a name="position-types-to-position-type"></a>Positionstypen zu Positionstyp

| Dataverse-Tabelle (Quelle)       | Finance-Entität (Ziel) |
|-------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                       | POSITIONTYPEID   (POSITIONTYPEID)           |
| cdm_description   (cdm_description)       | BESCHREIBUNG   (BESCHREIBUNG)                 |
| cdm_classification   (cdm_classification) | KLASSIFIZIERUNG   (KLASSIFIZIERUNG)           |

### <a name="job-positions-to-base-position"></a>Stellenpositionen zu Basisposition

| Dataverse-Tabelle (Quelle)           | Finance-Entität (Ziel) |
|-----------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber (Stellenpositionsnummer) | POSITIONID (POSITIONID)                      |

### <a name="job-positions-to-position-details"></a>Stellenpositionen zu Positionsdetails

| Dataverse-Tabelle (Quelle)              | Finance-Entität (Ziel)       |
|--------------------------------------------------------------------------|---------------------------------------------------|
| cdm_jobpositionnumber (Stellenpositionsnummer)                            | POSITIONID (POSITIONID)                             |
| cdm_jobid.cdm_name   (Stelle (Name))                                        | JOBID (JOBID)                                    |
| cdm_description   (cdm_description)                                        | BESCHREIBUNG   (BESCHREIBUNG)                       |
| cdm_departmentid.cdm_departmentnumber   (Abteilung (Abteilungsnummer)) | DEPARTMENTNUMBER   (DEPARTMENTNUMBER)             |
| cdm_positiontypeid.cdm_name   (Positionstyp (Name))                     | POSITIONTYPEID   (POSITIONTYPEID)                 |
| cdm_avaialableforassignment   (Verfügbar für Zuweisung)                 | AVAILABLEFORASSIGNMENT   (AVAILABLEFORASSIGNMENT) |
| cdm_validfrom   (gültig von)                                            | VALIDFROM   (VALIDFROM)                           |
| cdm_validto (gültig bis)                                                 | VALIDTO (VALIDTO)                               |
| cdm_fulltimeequivalent   (Vollzeitäquivalent)                           | FULLTIMEEQUIVALENT   (FULLTIMEEQUIVALENT)         |

### <a name="job-positions-to-position-durations"></a>Stellenpositionen zu Positionsdauern

| Dataverse-Tabelle (Quelle)             | Finance-Entität (Ziel) |
|-------------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber (Stellenpositionsnummer)   | POSITIONID (POSITIONID)                      |
| Berechnete Aktivierung (Berechnete Aktivierung) | VALIDFROM (VALIDFROM)                        |
| Berechnete Pensionierung (Berechnete Pensionierung) | VALIDTO (VALIDTO)                         |

### <a name="job-positions-to-position-hierarchies"></a>Stellenpositionen zu Positionshierarchien

| Dataverse-Tabelle (Quelle)        | Finance-Entität (Ziel) |
|-----------------------------------------------------------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber (Stellenpositionsnummer)                                                 | POSITIONID(POSITIONID)                      |
| cdm_parentjobpositionid.cdmjobpositionnumber   (cdm_parentjobpositionid.cdmjobpositionnumber) | PARENTPOSITIONID (PARENTPOSITIONID)         |
| cdm_validfrom   (gültig von)                                                                  | VALIDFROM   (VALIDFROM)                     |
| cdm_validto (gültig   bis)                                                                      | VALIDTO (VALIDTO)                           |
| HIERARCHYTYPENAME   (HIERARCHYTYPENAME)                                                       | HIERARCHYTYPENAME   (HIERARCHYTYPENAME)     |


### <a name="workers-to-worker"></a>Arbeitskräfte zu Arbeitskraft
| Dataverse-Tabelle (Quelle)           | Finance-Entität (Ziel)       |
|-----------------------------------------------|---------------------------------------------------|
| cdm_birthdate   (cdm_birthdate)               | GEBURTSDATUM   (GEBURTSDATUM)                           |
| cdm_gender   (cdm_gender)                     | GENDER (GENDER)                                   |
| cdm_primaryaddress   (cdm_primaryaddress)     | PRIMARYCONTACTEMAIL   (PRIMARYCONTACTEMAIL )      |
| cdm_primarytelephone   (cdm_primarytelephone) | PRIMARYCONTACTPHONE   (PRIMARYCONTACTPHONE)       |
| cdm_facebookidentity   (cdm_facebookidentity) | PRIMARYCONTACTFACEBOOK   (PRIMARYCONTACTFACEBOOK) |
| cdm_twitteridentity   (cdm_twitteridentity)   | PRIMARYCONTACTTWITTER   (PRIMARYCONTACTTWITTER)   |
| cdm_linkedinIdentity   (cdm_linkedinIdentity) | PRIMARYCONTACTLINKEDIN   (PRIMARYCONTACTLINKEDIN) |
| cdm_websiteurl   (cdm_websiteurl)             | PRIMARYCONTACTURL   (PRIMARYCONTACTURL)           |
| cdm_firstname   (cdm_firstname)               | VORNAME   (VORNAME)                           |
| cdm_middlename   (cdm_middlename)             | MIDDLENAME   (MIDDLENAME)                         |
| cdm_lastname   (cdm_lastname)                 | NACHNAME (NACHNAME)                               |
| cdm_workernumber   (cdm_workernumber)         | PERSONNELNUMBER   (PERSONNELNUMBER)               |
| cdm_type (cdm_type)                           | WORKERTYPE   (WORKERTYPE)                         |
| cdm_state   (cdm_state)                       | WORKSTATUS (WORKERSTATUS)                       |

### <a name="employments-to-employment"></a>Beschäftigungen zu Beschäftigung

| Dataverse-Tabelle (Quelle)                             | Finance-Entität (Ziel) |
|-----------------------------------------------------------------|---------------------------------------------|
| cdm_employmentstartdate   (cdm_employmentstartdate)             | EMPLOYMENTSTARTDATE   (EMPLOYMENTSTARTDATE) |
| cdm_employmentenddate   (cdm_employmentenddate)                 | EMPLOYMENTENDDATE   (EMPLOYMENTENDDATE)     |
| cdm_workertype   (cdm_workertype)                               | WORKERTYPE   (WORKERTYPE)                   |
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)         |
| cdm_companyid.cdm_companycode   (cdm_companyid.cdm_companycode) | LEGALENTITYID   (LEGALENTITYID)             |

### <a name="employments-to-employment-detail"></a>Beschäftigungen zu Beschäftigung - Details

| Dataverse-Tabelle (Quelle)                             | Finance-Entität (Ziel)   |
|-----------------------------------------------------------------|-----------------------------------------------|
| cdm_employmentstartdate   (cdm_employmentstartdate)             | EMPLOYMENTSTARTDATE   (EMPLOYMENTSTARTDATE)   |
| cdm_employmentenddate   (cdm_employmentenddate)                 | EMPLOYMENTENDDATE   (EMPLOYMENTENDDATE)       |
| cdm_validfrom   (gültig von)                                    | VALIDFROM   (VALIDFROM)                       |
| cdm_validto (gültig   bis)                                        | VALIDTO (VALIDTO)                             |
| cdm_workerstartdate   (cdm_workerstartdate)                     | WORKERSTARTDATE   (WORKERSTARTDATE)           |
| cdm_lastdateworked   (cdm_lastdateworked)                       | LASTDATEWORKED   (LASTDATEWORKED)             |
| cdm_transitiondate   (cdm_transitiondate)                       | TRANSITIONDATE   (TRANSITIONDATE)             |
| cdm_employerunitofnotice   (cdm_employerunitofnotice)           | EMPLOYERUNITOFNOTICE   (EMPLOYERUNITOFNOTICE) |
| cdm_workerunitofnotice   (cdm_workerunitofnotice)               | WORKERUNITOFNOTICE   (WORKERUNITOFNOTICE)     |
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)           |
| cdm_companyid.cdm_companycode   (cdm_companyid.cdm_companycode) | LEGALENTITYID   (LEGALENTITYID)               |
| cdm_employernoticeamount   (cdm_employernoticeamount)           | EMPLOYERNOTICEAMOUNT   (EMPLOYERNOTICEAMOUNT) |
| cdm_workernoticeamount   (cdm_workernoticeamount )              | WORKERNOTICEAMOUNT   (WORKERNOTICEAMOUNT)     |

### <a name="position-worker-assignment-to-position-worker-assignments"></a>Position der Arbeitskraftzuordnung zu Position der Arbeitskraftzuordnungen

| Dataverse-Tabelle (Quelle)                             | Finance-Entität (Ziel)   |
|-----------------------------------------------------------------|-----------------------------------------------|
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)           |
| cdm_jobpositionnumber (Stellenpositionsnummer)                   | POSITIONID(POSITIONID)                        |
| cdm_validfrom   (gültig von)                                    | VALIDFROM   (VALIDFROM)                       |
| cdm_validto (gültig bis)                                        | VALIDTO (VALIDTO)                             |

### <a name="worker-addresses-to-worker-postal-address-v2"></a>Arbeitskräfteadressen zu Arbeitskraft-Postanschrift V2

| Dataverse-Tabelle (Quelle)                             | Finance-Entität (Ziel)   |
|-----------------------------------------------------------------|-----------------------------------------------|
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)           |
| cdm_addresstype   (cdm_addresstype)                             | ADDRESSLOCATIONROLES   (ADDRESSLOCATIONROLES) |
| cdm_line1   (cdm_line1)                                         | ADDRESSSTREET   (ADDRESSSTREET)               |
| cdm_city (cdm_city)                                             | ADDRESSCITY   (ADDRESSCITY)                   |
| cdm_stateorprovince   (cdm_stateorprovince)                     | ADDRESSSTATE   (ADDRESSSTATE)                 |
| cdm_postalcode   (cdm_postalcode)                               | ADDRESSZIPCODE(ADDRESSZIPCODE)                |
| cdm_countryregion   (cdm_countryregion)                         | ADDRESSCOUNTRYREGION(ADDRESSCOUNTRYREGION)    |
| cdm_addressnumber   (cdm_addressnumber)                         | ADDRESSLOCATIONID(ADDRESSLOCATIONID)          |
| cdm_ispreferred   (cdm_ispreferred)                             | ISPRIMARY   (ISPRIMARY)                       |
| cdm_county   (cdm_county)                                       | ADDRESSCOUNTYID(ADDRESSCOUNTYID)              |
| cdm_addresstype   (cdm_addresstype)                             | ADDRESSDESCRIPTION(ADDRESSDESCRIPTION)        |

## <a name="integration-considerations"></a>Überlegungen zur Integration

Bei der Integration von Daten von Human Resources in Finance wird versucht, Datensätze basierend auf der ID miteinander abzugleichen. Bei einer Übereinstimmung der Datensätze werden die Daten in Finance vom Datenintegrator mit den Werten aus Human Resources überschrieben. Ein Problem kann jedoch auftreten, wenn es sich logisch um unterschiedliche Datensätze handelt und dieselbe ID in Human Resources oder Finance basierend auf dem jeweiligen Nummernkreis generiert wurde.

Dieses Problem kann bei **Arbeitskraft** auftreten. Diese nutzen **Personalnummer** und **Positionen** zum Abgleich. Für Stellen werden keine Nummernkreise verwendet. Wenn also dieselbe Stellen-ID in Human Resources und Finance vorhanden ist, überschreiben die Daten aus Human Resources die Daten aus Dynamics 365 Finance. 

Um Probleme mit doppelten IDs zu vermeiden, können Sie entweder ein Präfix zum [Nummernkreis](/dynamics365/unified-operations/fin-and-ops/organization-administration/number-sequence-overview?toc=%2fdynamics365%2funified-operations%2ftalent%2ftoc.json) hinzufügen oder eine Anfangsnummer für den Nummernkreis festlegen, die außerhalb des Bereichs des anderen Systems liegt. 

Die Lagerplatzkennung, die für die Arbeitskraftadresse verwendet wird, gehört nicht zum Nummernkreis. Wenn eine Arbeitskraftadresse von Human Resources in Finance integriert wird und die Arbeitskraft bereits in Finance vorhanden ist, wird möglicherweise ein neuer Datensatz erstellt. 

Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenzuordnung im Datenintegrator. 

![Vorlagenzuordnung.](./media/IntegrationMapping.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
