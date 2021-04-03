---
title: Einführung der API zur Integration des Bewerber-Tracking-Systems
description: Dieses Thema beschreibt die Dynamics 365 Human Resources-API zur Integration des Bewerber-Tracking-System (ATS).
author: andreabichsel
manager: tfehr
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 61d8502a8f420d387b5b7f48fca2f8a680f6f3f8
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464031"
---
# <a name="applicant-tracking-system-integration-api-introduction"></a><span data-ttu-id="3b39b-103">Einführung der API zur Integration des Bewerber-Tracking-Systems</span><span class="sxs-lookup"><span data-stu-id="3b39b-103">Applicant Tracking System integration API introduction</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="3b39b-104">Dieses Thema beschreibt die Dynamics 365 Human Resources-API zur Integration des Bewerber-Tracking-System (ATS).</span><span class="sxs-lookup"><span data-stu-id="3b39b-104">This topic describes the Dynamics 365 Human Resources Applicant Tracking System (ATS) integration API.</span></span> <span data-ttu-id="3b39b-105">Die Absicht der API ist es, optimierte Integrationen zwischen Dynamics 365 Human Resources und ATSs, die eine Partnerschaft eingehen, zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="3b39b-105">The intent of the API is to enable streamlined integrations between Dynamics 365 Human Resources and partnering ATSs.</span></span>

![Flow der ATS-Integration](media/hr-admin-integration-ats-api-introduction-flow.png)

<span data-ttu-id="3b39b-107">Die integrierte Erfahrung beginnt in der Personalabteilung, wenn ein Personalchef einen Personalbeschaffungsantrag erstellt.</span><span class="sxs-lookup"><span data-stu-id="3b39b-107">The integrated experience begins in Human Resources when a hiring manager creates a recruiting request.</span></span> <span data-ttu-id="3b39b-108">Wenn die Anfrage aktiviert ist, ruft der ATS die Details für die Anfrage ab, um ein Rekrutierungsprojekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3b39b-108">When the request is activated, the ATS pulls the detail for the request to create a recruiting project.</span></span> <span data-ttu-id="3b39b-109">Anschließend folgt er die Rekrutierungspipeline, um einen Kandidaten für die Position(en) auszuwählen und einzustellen.</span><span class="sxs-lookup"><span data-stu-id="3b39b-109">Then it follows the recruiting pipeline to select and hire a candidate for the position(s).</span></span> <span data-ttu-id="3b39b-110">Schließlich schließt der ATS die umfassende Integration ab, indem er den Datensatz des ausgewählten Kandidaten an die Personalabteilung sendet.</span><span class="sxs-lookup"><span data-stu-id="3b39b-110">Finally, the ATS completes the round-trip integration by sending the selected candidate’s record into Human Resources.</span></span> <span data-ttu-id="3b39b-111">Der Kandidatendatensatz kann dann weitere Onboarding-Validierungen und Workflows durchlaufen, um den Mitarbeiterdatensatz zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3b39b-111">The candidate record can then go through more onboarding validations and workflows to create the employee record.</span></span>

<span data-ttu-id="3b39b-112">Um die Integration zu ermöglichen, hat Human Resources die folgenden Komponenten hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="3b39b-112">To enable the integration, Human Resources has added the following components:</span></span>

1.  <span data-ttu-id="3b39b-113">Funktionalität zum Erstellen eines Personalbeschaffungsantrags.</span><span class="sxs-lookup"><span data-stu-id="3b39b-113">Functionality to create a recruiting request.</span></span>
2.  <span data-ttu-id="3b39b-114">Ein erweitertes Kandidatenprofil und zugehörige Workflows.</span><span class="sxs-lookup"><span data-stu-id="3b39b-114">An expanded candidate profile and related workflows.</span></span>
3.  <span data-ttu-id="3b39b-115">Eine Integrations-API öffnet die neue Funktionalität für die Integration von Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="3b39b-115">An integration API opening up the new functionality to integrating applications.</span></span>

<span data-ttu-id="3b39b-116">Weitere Informationen zum Einrichten und Verwenden des Personalbeschaffungsantrags und der Kandidatenfunktionalität finden Sie unter [Rekrutieren von Bewerbern auf eine Stelle](hr-personnel-recruit.md).</span><span class="sxs-lookup"><span data-stu-id="3b39b-116">For more information about setting up and using the recruiting request and candidate functionality, see [Recruit job candidates](hr-personnel-recruit.md).</span></span>

## <a name="microsoft-dataverse"></a><span data-ttu-id="3b39b-117">Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="3b39b-117">Microsoft Dataverse</span></span>

<span data-ttu-id="3b39b-118">Diese API basiert auf Microsoft Dataverse (früher Common Data Service).</span><span class="sxs-lookup"><span data-stu-id="3b39b-118">This API is built on Microsoft Dataverse (formerly Common Data Service).</span></span> <span data-ttu-id="3b39b-119">Alle RESTful-Interaktionen mit dieser API erfolgen über die Microsoft Dataverse-Web-API, die OData verwendet.</span><span class="sxs-lookup"><span data-stu-id="3b39b-119">All RESTful interaction with this API is done via the Microsoft Dataverse Web API, which uses OData.</span></span> <span data-ttu-id="3b39b-120">Diese API ist eine Teilmenge der Dataverse-Web-API.</span><span class="sxs-lookup"><span data-stu-id="3b39b-120">This API is a subset of the Dataverse Web API.</span></span> <span data-ttu-id="3b39b-121">Die Dataverse-Web-API definiert Merkmale wie Authentifizierung, SLAs, Stapelverarbeitung, Parallelitätskontrolle und Fehlerbehandlung.</span><span class="sxs-lookup"><span data-stu-id="3b39b-121">The Dataverse Web API defines characteristics such as authentication, SLAs, batch, concurrency control, and error handling.</span></span>

<span data-ttu-id="3b39b-122">Weitere allgemeine Informationen zur Microsoft Dataverse-Web-API finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="3b39b-122">For more general information about the Microsoft Dataverse Web API, see:</span></span>

- [<span data-ttu-id="3b39b-123">Was ist Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="3b39b-123">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)
- [<span data-ttu-id="3b39b-124">Verwenden der Microsoft Dataverse-Web-API</span><span class="sxs-lookup"><span data-stu-id="3b39b-124">Use the Microsoft Dataverse Web API</span></span>](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/overview)
- [<span data-ttu-id="3b39b-125">Microsoft Dataverse-Entwicklerhandbuch</span><span class="sxs-lookup"><span data-stu-id="3b39b-125">Microsoft Dataverse developer guide</span></span>](https://docs.microsoft.com/powerapps/developer/data-platform)

<span data-ttu-id="3b39b-126">Die obige Dokumentation enthält detaillierte und Entwickleranleitungen zur Verwendung der Dataverse-Web-API mit der API, z. B.[Authentifizierung verwalten](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/authenticate-web-api), [Vorgänge durchführen](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/perform-operations-web-api), [Postman mit der API verwenden](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/use-postman-web-api) und [Änderungsverfolgung oder Delta-Token verwenden](https://docs.microsoft.com/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems).</span><span class="sxs-lookup"><span data-stu-id="3b39b-126">The above documentation includes detail and developer guidance on using the Dataverse Web API, such as [managing authentication](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/authenticate-web-api), [performing operations](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/perform-operations-web-api), [using Postman with the API](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/use-postman-web-api), and [using change tracking or delta tokens](https://docs.microsoft.com/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems) with the API.</span></span>

### <a name="option-sets"></a><span data-ttu-id="3b39b-127">Optionssätze</span><span class="sxs-lookup"><span data-stu-id="3b39b-127">Option sets</span></span>

<span data-ttu-id="3b39b-128">Das in diesem Dokument beschriebene Datenmodell für die ATS-Integrations-API enthält Optionssätze, die Aufzählungswerte für Entitätseigenschaften bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="3b39b-128">The data model for the ATS integration API described in this document includes option sets that provide enumerated values associated with entity properties.</span></span> <span data-ttu-id="3b39b-129">Ausführliche Informationen zum Arbeiten mit Optionssätzen finden Sie in der Dataverse-Web-API unter [Erstellen und Aktualisieren von Optionssätze mithilfe der Web-API](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-update-optionsets).</span><span class="sxs-lookup"><span data-stu-id="3b39b-129">For detail on working with option sets in the Dataverse Web API, see [Create and update option sets using the Web API](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-update-optionsets).</span></span> <span data-ttu-id="3b39b-130">Optionssätze sind für jede Dataverse-Umgebung definiert.</span><span class="sxs-lookup"><span data-stu-id="3b39b-130">Option sets are defined for each Dataverse environment.</span></span>

### <a name="virtual-tables-for-human-resources-in-dataverse"></a><span data-ttu-id="3b39b-131">Virtuelle Tabellen für Human Resources in Dataverse</span><span class="sxs-lookup"><span data-stu-id="3b39b-131">Virtual tables for Human Resources in Dataverse</span></span>

<span data-ttu-id="3b39b-132">Die Endpunkte für die ATS-Integrations-API verwenden die Funktionen der Plattform für virtuelle Tabellen von Microsoft Dataverse.</span><span class="sxs-lookup"><span data-stu-id="3b39b-132">The endpoints for the ATS integration API use the virtual table platform capabilities of Microsoft Dataverse.</span></span> <span data-ttu-id="3b39b-133">Standardmäßig werden die virtuellen Tabellen und die zugehörigen API-Endpunkte nicht für Human Resources-Umgebungen bereitgestellt, sodass Unternehmen bestimmen können, welche OData-Endpunkte für die Umgebung verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="3b39b-133">By default, the virtual tables and their associated API endpoints are not deployed for Human Resources environments, enabling organizations to determine which OData endpoints will be exposed for the environment.</span></span> <span data-ttu-id="3b39b-134">Um die API verwenden zu können, müssen die virtuellen Tabellen für die Personalentitäten für die Umgebung generiert werden.</span><span class="sxs-lookup"><span data-stu-id="3b39b-134">To use the API, the virtual tables for the Human Resources entities must be generated for the environment.</span></span> 

<span data-ttu-id="3b39b-135">Informationen zum Generieren der virtuellen Tabellen für die API finden Sie unter [Konfigurieren von virtuellen Dataverse-Tabellen](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).</span><span class="sxs-lookup"><span data-stu-id="3b39b-135">For information on generating the virtual tables for the API, see [Configure Dataverse virtual tables](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).</span></span>

## <a name="data-model"></a><span data-ttu-id="3b39b-136">Datenmodell</span><span class="sxs-lookup"><span data-stu-id="3b39b-136">Data model</span></span>

<span data-ttu-id="3b39b-137">Das Datenmodell konzentriert sich auf zwei Hauptentitäten:</span><span class="sxs-lookup"><span data-stu-id="3b39b-137">The data model is centered around two main entities:</span></span>

- <span data-ttu-id="3b39b-138">**RecruitingRequest** stellt eine Anfrage an einen ATS dar, für eine oder mehrere offene Positionen zu rekrutieren. Eine Beispielabfrage finden Sie unter [Beispielabfrage für den Personalbeschaffungsantrag](hr-admin-integration-ats-api-recruiting-request-example-query.md).</span><span class="sxs-lookup"><span data-stu-id="3b39b-138">**RecruitingRequest** represents a request to an ATS to recruit for one or more open positions.For an example query, see [Example query for Recruiting request](hr-admin-integration-ats-api-recruiting-request-example-query.md).</span></span>
- <span data-ttu-id="3b39b-139">**CandidateToHire** stellt Details eines Kandidaten dar, der ein Angebot für eine Position angenommen hat.</span><span class="sxs-lookup"><span data-stu-id="3b39b-139">**CandidateToHire** represents details of a candidate who has accepted an offer for a position.</span></span> <span data-ttu-id="3b39b-140">**Person** repräsentiert die Person, die der Kandidat ist.</span><span class="sxs-lookup"><span data-stu-id="3b39b-140">**Person** represents the individual who is the candidate.</span></span> <span data-ttu-id="3b39b-141">Eine Person kann mehrere Rollen im Unternehmen haben, z. B. ein Kandidat, eine Arbeitskraft, ein Mitarbeiter oder ein Auftragnehmer.</span><span class="sxs-lookup"><span data-stu-id="3b39b-141">A person can have multiple roles in the company, such as candidate, worker, employee, or contractor.</span></span> <span data-ttu-id="3b39b-142">Eine Beispielabfrage finden Sie unter [Beispielabfrage für Kandidaten zur Einstellung](hr-admin-integration-ats-api-candidate-to-hire-example-query.md).</span><span class="sxs-lookup"><span data-stu-id="3b39b-142">For an example query, see [Example query for Candidate to hire](hr-admin-integration-ats-api-candidate-to-hire-example-query.md).</span></span>

<span data-ttu-id="3b39b-143">Das folgende Diagramm veranschaulicht die Beziehungen innerhalb der API.</span><span class="sxs-lookup"><span data-stu-id="3b39b-143">The following diagram illustrates relationships within the API.</span></span> <span data-ttu-id="3b39b-144">Einige Typen verfügen über Fremdschlüssel für andere bereits vorhandene Entitäten in Human Resources, die hier nicht dargestellt sind.</span><span class="sxs-lookup"><span data-stu-id="3b39b-144">Several types have foreign keys to other, pre-existing entities in Human Resources that aren't illustrated here.</span></span> <span data-ttu-id="3b39b-145">Dieses Dokument enthält Informationen zu Entitäten, die für die Rekrutierung von Integrationsszenarien spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="3b39b-145">This document provides information on entities that are specific to recruiting integration scenarios.</span></span> <span data-ttu-id="3b39b-146">Es gibt jedoch viele andere Entitäten in der Dataverse-Web-API für Dynamics 365 Human Resources, die auch für Ihre Integration relevant sein können.</span><span class="sxs-lookup"><span data-stu-id="3b39b-146">However, there are many other entities in the Dataverse Web API for Dynamics 365 Human Resources that may also be relevant to your integration.</span></span> <span data-ttu-id="3b39b-147">Beispielsweise benötigen Sie möglicherweise auch Details für Mitarbeiter, Stellen, Positionen oder andere Entitäten, die hier nicht definiert sind.</span><span class="sxs-lookup"><span data-stu-id="3b39b-147">For example, you may also need detail for workers, jobs, positions, or other entities not defined here.</span></span> <span data-ttu-id="3b39b-148">Viele dieser Entitäten werden in Fremdschlüsselbeziehungen oder Navigationseigenschaften referenziert.</span><span class="sxs-lookup"><span data-stu-id="3b39b-148">Many of these entities are referenced in foreign key relationships or navigation properties.</span></span>

![Datenmodell von ATS-Integrations-API](media/hr-admin-integration-ats-api-data-model.png)

## <a name="recruiting-request-and-related-entities-and-option-sets"></a><span data-ttu-id="3b39b-150">Personalbeschaffungsantrag und zugehörige Entitäten und Optionssätze</span><span class="sxs-lookup"><span data-stu-id="3b39b-150">Recruiting request and related entities and option sets</span></span>

<span data-ttu-id="3b39b-151">Beispielabfrage:</span><span class="sxs-lookup"><span data-stu-id="3b39b-151">Example query:</span></span> 

- [<span data-ttu-id="3b39b-152">Beispielabfrage für den Personalbeschaffungsantrag</span><span class="sxs-lookup"><span data-stu-id="3b39b-152">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)

<span data-ttu-id="3b39b-153">Entitäten:</span><span class="sxs-lookup"><span data-stu-id="3b39b-153">Entities:</span></span>

- [<span data-ttu-id="3b39b-154">Personalbeschaffungsantrag</span><span class="sxs-lookup"><span data-stu-id="3b39b-154">Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request.md)
- [<span data-ttu-id="3b39b-155">Personalbeschaffungsantragsposition</span><span class="sxs-lookup"><span data-stu-id="3b39b-155">Recruiting request position</span></span>](hr-admin-integration-ats-api-recruiting-request-position.md)
- [<span data-ttu-id="3b39b-156">Qualifikation des Personalbeschaffungsantrags</span><span class="sxs-lookup"><span data-stu-id="3b39b-156">Recruiting request skill</span></span>](hr-admin-integration-ats-api-recruiting-request-skill.md)
- [<span data-ttu-id="3b39b-157">Ausbildung des Personalbeschaffungsantrags</span><span class="sxs-lookup"><span data-stu-id="3b39b-157">Recruiting request education</span></span>](hr-admin-integration-ats-api-recruiting-request-education.md)
- [<span data-ttu-id="3b39b-158">Personalbeschaffungsantragsstandort</span><span class="sxs-lookup"><span data-stu-id="3b39b-158">Recruiting request location</span></span>](hr-admin-integration-ats-api-recruiting-request-location.md)

<span data-ttu-id="3b39b-159">Optionssätze:</span><span class="sxs-lookup"><span data-stu-id="3b39b-159">Option sets:</span></span>

- [<span data-ttu-id="3b39b-160">Stellenbefreiungsstatus</span><span class="sxs-lookup"><span data-stu-id="3b39b-160">Job exempt status</span></span>](hr-admin-integration-ats-api-job-exempt-status.md)
- [<span data-ttu-id="3b39b-161">Positionsstatus des Personalbeschaffungsantrags</span><span class="sxs-lookup"><span data-stu-id="3b39b-161">Recruiting request position status</span></span>](hr-admin-integration-ats-api-recruiting-request-position-status.md)
- [<span data-ttu-id="3b39b-162">Status des Personalbeschaffungsantrags</span><span class="sxs-lookup"><span data-stu-id="3b39b-162">Recruiting request status</span></span>](hr-admin-integration-ats-api-recruiting-request-status.md)
- [<span data-ttu-id="3b39b-163">Regulatorische Stellenkategorie</span><span class="sxs-lookup"><span data-stu-id="3b39b-163">Regulatory job category</span></span>](hr-admin-integration-ats-api-regulatory-job-category.md)

## <a name="candidate-to-hire-and-related-entities-and-option-sets"></a><span data-ttu-id="3b39b-164">Kandidat für die Einstellung und verwandte Unternehmen und Optionssätze</span><span class="sxs-lookup"><span data-stu-id="3b39b-164">Candidate to hire and related entities and option sets</span></span>

<span data-ttu-id="3b39b-165">Beispielabfrage:</span><span class="sxs-lookup"><span data-stu-id="3b39b-165">Example query:</span></span>

- [<span data-ttu-id="3b39b-166">Beispielabfrage für Kandidaten zur Einstellung</span><span class="sxs-lookup"><span data-stu-id="3b39b-166">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

<span data-ttu-id="3b39b-167">Entitäten:</span><span class="sxs-lookup"><span data-stu-id="3b39b-167">Entities:</span></span>

- [<span data-ttu-id="3b39b-168">Kandidat, der eingestellt werden kann</span><span class="sxs-lookup"><span data-stu-id="3b39b-168">Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire.md)
- [<span data-ttu-id="3b39b-169">Person</span><span class="sxs-lookup"><span data-stu-id="3b39b-169">Person</span></span>](hr-admin-integration-ats-api-person.md)
- [<span data-ttu-id="3b39b-170">Personenausbildung</span><span class="sxs-lookup"><span data-stu-id="3b39b-170">Person education</span></span>](hr-admin-integration-ats-api-person-education.md)
- [<span data-ttu-id="3b39b-171">Berufserfahrung der Person</span><span class="sxs-lookup"><span data-stu-id="3b39b-171">Person professional experience</span></span>](hr-admin-integration-ats-api-person-professional-experience.md)
- [<span data-ttu-id="3b39b-172">Personenadresse</span><span class="sxs-lookup"><span data-stu-id="3b39b-172">Person address</span></span>](hr-admin-integration-ats-api-person-address.md)
- [<span data-ttu-id="3b39b-173">Parteikontakt</span><span class="sxs-lookup"><span data-stu-id="3b39b-173">Party contact</span></span>](hr-admin-integration-ats-api-party-contact.md)
- [<span data-ttu-id="3b39b-174">Qualifikation der Person</span><span class="sxs-lookup"><span data-stu-id="3b39b-174">Person skill</span></span>](hr-admin-integration-ats-api-person-skill.md)
- [<span data-ttu-id="3b39b-175">Bewertungsebene</span><span class="sxs-lookup"><span data-stu-id="3b39b-175">Rating level</span></span>](hr-admin-integration-ats-api-rating-level.md)
- [<span data-ttu-id="3b39b-176">Zertifkat der Person</span><span class="sxs-lookup"><span data-stu-id="3b39b-176">Person certificate</span></span>](hr-admin-integration-ats-api-person-certificate.md)
- [<span data-ttu-id="3b39b-177">Bescheinigungstyp</span><span class="sxs-lookup"><span data-stu-id="3b39b-177">Certificate type</span></span>](hr-admin-integration-ats-api-certificate-type.md)
- [<span data-ttu-id="3b39b-178">Personenprüfung</span><span class="sxs-lookup"><span data-stu-id="3b39b-178">Person screening</span></span>](hr-admin-integration-ats-api-person-screening.md)
- [<span data-ttu-id="3b39b-179">Prüfungstypen</span><span class="sxs-lookup"><span data-stu-id="3b39b-179">Screening types</span></span>](hr-admin-integration-ats-api-screening-types.md)
- [<span data-ttu-id="3b39b-180">Personenidentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="3b39b-180">Person identification number</span></span>](hr-admin-integration-ats-api-person-identification-number.md)

<span data-ttu-id="3b39b-181">Optionssätze:</span><span class="sxs-lookup"><span data-stu-id="3b39b-181">Option sets:</span></span>

- [<span data-ttu-id="3b39b-182">Bewerberintegrationsergebnis</span><span class="sxs-lookup"><span data-stu-id="3b39b-182">Applicant integration result</span></span>](hr-admin-integration-ats-api-applicant-integration-result.md)
- [<span data-ttu-id="3b39b-183">Leer Ja Nein</span><span class="sxs-lookup"><span data-stu-id="3b39b-183">Blank Yes No</span></span>](hr-admin-integration-ats-api-blank-yes-no.md)
- [<span data-ttu-id="3b39b-184">Abschlussstatus</span><span class="sxs-lookup"><span data-stu-id="3b39b-184">Completion status</span></span>](hr-admin-integration-ats-api-completion-status.md)
- [<span data-ttu-id="3b39b-185">Art des Kontakts</span><span class="sxs-lookup"><span data-stu-id="3b39b-185">Contact type</span></span>](hr-admin-integration-ats-api-contact-type.md)
- [<span data-ttu-id="3b39b-186">Ausbildungsgrundlage</span><span class="sxs-lookup"><span data-stu-id="3b39b-186">Education credit basis</span></span>](hr-admin-integration-ats-api-education-credit-basis.md)
- [<span data-ttu-id="3b39b-187">Geschlecht</span><span class="sxs-lookup"><span data-stu-id="3b39b-187">Gender</span></span>](hr-admin-integration-ats-api-gender.md)
- [<span data-ttu-id="3b39b-188">Familienstand</span><span class="sxs-lookup"><span data-stu-id="3b39b-188">Marital status</span></span>](hr-admin-integration-ats-api-marital-status.md)
- [<span data-ttu-id="3b39b-189">Monate des Jahres</span><span class="sxs-lookup"><span data-stu-id="3b39b-189">Months of year</span></span>](hr-admin-integration-ats-api-months-of-year.md)
- [<span data-ttu-id="3b39b-190">Nein Ja</span><span class="sxs-lookup"><span data-stu-id="3b39b-190">No Yes</span></span>](hr-admin-integration-ats-api-no-yes.md)
- [<span data-ttu-id="3b39b-191">Periodeneinheit</span><span class="sxs-lookup"><span data-stu-id="3b39b-191">Period unit</span></span>](hr-admin-integration-ats-api-period-unit.md)
- [<span data-ttu-id="3b39b-192">Screening-Häufigkeit</span><span class="sxs-lookup"><span data-stu-id="3b39b-192">Screening frequency</span></span>](hr-admin-integration-ats-api-screening-frequency.md)
- [<span data-ttu-id="3b39b-193">Screening-Häufigkeit erzeugen aus</span><span class="sxs-lookup"><span data-stu-id="3b39b-193">Screening frequency generate from</span></span>](hr-admin-integration-ats-api-screening-frequency-generate-from.md)
- [<span data-ttu-id="3b39b-194">Typ der Qualifikationsstufe</span><span class="sxs-lookup"><span data-stu-id="3b39b-194">Skill level type</span></span>](hr-admin-integration-ats-api-skill-level-type.md)

## <a name="see-also"></a><span data-ttu-id="3b39b-195">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3b39b-195">See also</span></span>

[<span data-ttu-id="3b39b-196">Kandidaten für Stelle anwerben</span><span class="sxs-lookup"><span data-stu-id="3b39b-196">Recruit job candidates</span></span>](hr-personnel-recruit.md)<br>
[<span data-ttu-id="3b39b-197">Was ist Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="3b39b-197">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="3b39b-198">Verwenden der Microsoft Dataverse-Web-API</span><span class="sxs-lookup"><span data-stu-id="3b39b-198">Use the Microsoft Dataverse Web API</span></span>](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/overview)<br>
[<span data-ttu-id="3b39b-199">Erstellen und Aktualisieren von Optionssätzen mithilfe der Web-API</span><span class="sxs-lookup"><span data-stu-id="3b39b-199">Create and update option sets using the Web API</span></span>](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-update-optionsets)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]