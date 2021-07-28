---
title: Einführung der API zur Integration des Bewerber-Tracking-Systems
description: Dieses Thema beschreibt die Dynamics 365 Human Resources-API zur Integration des Bewerber-Tracking-System (ATS).
author: andreabichsel
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5038a1a1b3fa4c32f54ea87b03f886504e0b004f
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6357387"
---
# <a name="applicant-tracking-system-integration-api-introduction"></a>Einführung der API zur Integration des Bewerber-Tracking-Systems

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dieses Thema beschreibt die Dynamics 365 Human Resources-API zur Integration des Bewerber-Tracking-System (ATS). Die Absicht der API ist es, optimierte Integrationen zwischen Dynamics 365 Human Resources und ATSs, die eine Partnerschaft eingehen, zu ermöglichen.

![Flow der ATS-Integration.](media/hr-admin-integration-ats-api-introduction-flow.png)

Die integrierte Erfahrung beginnt in der Personalabteilung, wenn ein Personalchef einen Personalbeschaffungsantrag erstellt. Wenn die Anfrage aktiviert ist, ruft der ATS die Details für die Anfrage ab, um ein Rekrutierungsprojekt zu erstellen. Anschließend folgt er die Rekrutierungspipeline, um einen Kandidaten für die Position(en) auszuwählen und einzustellen. Schließlich schließt der ATS die umfassende Integration ab, indem er den Datensatz des ausgewählten Kandidaten an die Personalabteilung sendet. Der Kandidatendatensatz kann dann weitere Onboarding-Validierungen und Workflows durchlaufen, um den Mitarbeiterdatensatz zu erstellen.

Um die Integration zu ermöglichen, hat Human Resources die folgenden Komponenten hinzugefügt:

1.  Funktionalität zum Erstellen eines Personalbeschaffungsantrags.
2.  Ein erweitertes Kandidatenprofil und zugehörige Workflows.
3.  Eine Integrations-API öffnet die neue Funktionalität für die Integration von Anwendungen.

Weitere Informationen zum Einrichten und Verwenden des Personalbeschaffungsantrags und der Kandidatenfunktionalität finden Sie unter [Rekrutieren von Bewerbern auf eine Stelle](hr-personnel-recruit.md).

## <a name="microsoft-dataverse"></a>Microsoft Dataverse

Diese API basiert auf Microsoft Dataverse (früher Common Data Service). Alle RESTful-Interaktionen mit dieser API erfolgen über die Microsoft Dataverse-Web-API, die OData verwendet. Diese API ist eine Teilmenge der Dataverse-Web-API. Die Dataverse-Web-API definiert Merkmale wie Authentifizierung, SLAs, Stapelverarbeitung, Parallelitätskontrolle und Fehlerbehandlung.

Weitere allgemeine Informationen zur Microsoft Dataverse-Web-API finden Sie unter:

- [Was ist Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)
- [Verwenden der Microsoft Dataverse-Web-API](/powerapps/developer/data-platform/webapi/overview)
- [Microsoft Dataverse-Entwicklerhandbuch](/powerapps/developer/data-platform)

Die obige Dokumentation enthält detaillierte und Entwickleranleitungen zur Verwendung der Dataverse-Web-API mit der API, z. B. [Authentifizierung verwalten](/powerapps/developer/data-platform/webapi/authenticate-web-api), [Vorgänge durchführen](/powerapps/developer/data-platform/webapi/perform-operations-web-api), [Postman mit der API verwenden](/powerapps/developer/data-platform/webapi/use-postman-web-api) und [Änderungsverfolgung oder Delta-Token verwenden](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems).

### <a name="option-sets"></a>Optionssätze

Das in diesem Dokument beschriebene Datenmodell für die ATS-Integrations-API enthält Optionssätze, die Aufzählungswerte für Entitätseigenschaften bereitstellen. Ausführliche Informationen zum Arbeiten mit Optionssätzen finden Sie in der Dataverse-Web-API unter [Erstellen und Aktualisieren von Optionssätze mithilfe der Web-API](/powerapps/developer/data-platform/webapi/create-update-optionsets). Optionssätze sind für jede Dataverse-Umgebung definiert.

### <a name="virtual-tables-for-human-resources-in-dataverse"></a>Virtuelle Tabellen für Human Resources in Dataverse

Die Endpunkte für die ATS-Integrations-API verwenden die Funktionen der Plattform für virtuelle Tabellen von Microsoft Dataverse. Standardmäßig werden die virtuellen Tabellen und die zugehörigen API-Endpunkte nicht für Human Resources-Umgebungen bereitgestellt, sodass Unternehmen bestimmen können, welche OData-Endpunkte für die Umgebung verfügbar gemacht werden. Um die API verwenden zu können, müssen die virtuellen Tabellen für die Personalentitäten für die Umgebung generiert werden. 

Informationen zum Generieren der virtuellen Tabellen für die API finden Sie unter [Konfigurieren von virtuellen Dataverse-Tabellen](./hr-admin-integration-common-data-service-virtual-entities.md).

## <a name="data-model"></a>Datenmodell

Das Datenmodell konzentriert sich auf zwei Hauptentitäten:

- **RecruitingRequest** stellt eine Anfrage an einen ATS dar, für eine oder mehrere offene Positionen zu rekrutieren. Eine Beispielabfrage finden Sie unter [Beispielabfrage für den Personalbeschaffungsantrag](hr-admin-integration-ats-api-recruiting-request-example-query.md).
- **CandidateToHire** stellt Details eines Kandidaten dar, der ein Angebot für eine Position angenommen hat. **Person** repräsentiert die Person, die der Kandidat ist. Eine Person kann mehrere Rollen im Unternehmen haben, z. B. ein Kandidat, eine Arbeitskraft, ein Mitarbeiter oder ein Auftragnehmer. Eine Beispielabfrage finden Sie unter [Beispielabfrage für Kandidaten zur Einstellung](hr-admin-integration-ats-api-candidate-to-hire-example-query.md).

Das folgende Diagramm veranschaulicht die Beziehungen innerhalb der API. Einige Typen verfügen über Fremdschlüssel für andere bereits vorhandene Entitäten in Human Resources, die hier nicht dargestellt sind. Dieses Dokument enthält Informationen zu Entitäten, die für die Rekrutierung von Integrationsszenarien spezifisch sind. Es gibt jedoch viele andere Entitäten in der Dataverse-Web-API für Dynamics 365 Human Resources, die auch für Ihre Integration relevant sein können. Beispielsweise benötigen Sie möglicherweise auch Details für Mitarbeiter, Stellen, Positionen oder andere Entitäten, die hier nicht definiert sind. Viele dieser Entitäten werden in Fremdschlüsselbeziehungen oder Navigationseigenschaften referenziert.

![Datenmodell von ATS-Integrations-API.](media/hr-admin-integration-ats-api-data-model.png)

## <a name="recruiting-request-and-related-entities-and-option-sets"></a>Personalbeschaffungsantrag und zugehörige Entitäten und Optionssätze

Beispielabfrage: 

- [Beispielabfrage für den Personalbeschaffungsantrag](hr-admin-integration-ats-api-recruiting-request-example-query.md)

Entitäten:

- [Personalbeschaffungsantrag](hr-admin-integration-ats-api-recruiting-request.md)
- [Personalbeschaffungsantragsposition](hr-admin-integration-ats-api-recruiting-request-position.md)
- [Qualifikation des Personalbeschaffungsantrags](hr-admin-integration-ats-api-recruiting-request-skill.md)
- [Ausbildung des Personalbeschaffungsantrags](hr-admin-integration-ats-api-recruiting-request-education.md)
- [Personalbeschaffungsantragsstandort](hr-admin-integration-ats-api-recruiting-request-location.md)

Optionssätze:

- [Stellenbefreiungsstatus](hr-admin-integration-ats-api-job-exempt-status.md)
- [Positionsstatus des Personalbeschaffungsantrags](hr-admin-integration-ats-api-recruiting-request-position-status.md)
- [Status des Personalbeschaffungsantrags](hr-admin-integration-ats-api-recruiting-request-status.md)
- [Regulatorische Stellenkategorie](hr-admin-integration-ats-api-regulatory-job-category.md)

## <a name="candidate-to-hire-and-related-entities-and-option-sets"></a>Kandidat für die Einstellung und verwandte Unternehmen und Optionssätze

Beispielabfrage:

- [Beispielabfrage für Kandidaten zur Einstellung](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

Entitäten:

- [Kandidat, der eingestellt werden kann](hr-admin-integration-ats-api-candidate-to-hire.md)
- [Person](hr-admin-integration-ats-api-person.md)
- [Personenausbildung](hr-admin-integration-ats-api-person-education.md)
- [Berufserfahrung der Person](hr-admin-integration-ats-api-person-professional-experience.md)
- [Personenadresse](hr-admin-integration-ats-api-person-address.md)
- [Parteikontakt](hr-admin-integration-ats-api-party-contact.md)
- [Qualifikation der Person](hr-admin-integration-ats-api-person-skill.md)
- [Bewertungsebene](hr-admin-integration-ats-api-rating-level.md)
- [Zertifkat der Person](hr-admin-integration-ats-api-person-certificate.md)
- [Bescheinigungstyp](hr-admin-integration-ats-api-certificate-type.md)
- [Personenprüfung](hr-admin-integration-ats-api-person-screening.md)
- [Prüfungstypen](hr-admin-integration-ats-api-screening-types.md)
- [Personenidentifikationsnummer](hr-admin-integration-ats-api-person-identification-number.md)

Optionssätze:

- [Bewerberintegrationsergebnis](hr-admin-integration-ats-api-applicant-integration-result.md)
- [Leer Ja Nein](hr-admin-integration-ats-api-blank-yes-no.md)
- [Abschlussstatus](hr-admin-integration-ats-api-completion-status.md)
- [Art des Kontakts](hr-admin-integration-ats-api-contact-type.md)
- [Ausbildungsgrundlage](hr-admin-integration-ats-api-education-credit-basis.md)
- [Geschlecht](hr-admin-integration-ats-api-gender.md)
- [Familienstand](hr-admin-integration-ats-api-marital-status.md)
- [Monate des Jahres](hr-admin-integration-ats-api-months-of-year.md)
- [Nein Ja](hr-admin-integration-ats-api-no-yes.md)
- [Periodeneinheit](hr-admin-integration-ats-api-period-unit.md)
- [Screening-Häufigkeit](hr-admin-integration-ats-api-screening-frequency.md)
- [Screening-Häufigkeit erzeugen aus](hr-admin-integration-ats-api-screening-frequency-generate-from.md)
- [Typ der Qualifikationsstufe](hr-admin-integration-ats-api-skill-level-type.md)

## <a name="see-also"></a>Siehe auch

[Kandidaten für Stelle anwerben](hr-personnel-recruit.md)<br>
[Was ist Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)<br>
[Verwenden der Microsoft Dataverse-Web-API](/powerapps/developer/data-platform/webapi/overview)<br>
[Erstellen und Aktualisieren von Optionssätzen mithilfe der Web-API](/powerapps/developer/data-platform/webapi/create-update-optionsets)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]