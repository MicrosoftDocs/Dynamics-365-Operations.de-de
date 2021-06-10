---
title: Einführung Lohnintegrations-API
description: Dieses Thema beschreibt die Lohnintegrations-API in Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e6d8a1cb9619a863184460a74e472af3f06934b6
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6058559"
---
# <a name="payroll-integration-api-introduction"></a><span data-ttu-id="807c0-103">Einführung Lohnintegrations-API</span><span class="sxs-lookup"><span data-stu-id="807c0-103">Payroll integration API introduction</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="807c0-104">Dieses Dokument beschreibt die Lohnintegrations-API in Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="807c0-104">This document describes the Dynamics 365 Human Resources Payroll integration API.</span></span> <span data-ttu-id="807c0-105">Die API ermöglicht eine optimierte End-to-End-Integration zwischen Human Resources und Partner-Lohnsystemen.</span><span class="sxs-lookup"><span data-stu-id="807c0-105">The API enables streamlined end-to-end integrations between Human Resources and partnering payroll systems.</span></span> <span data-ttu-id="807c0-106">Die integrierte Erfahrung beginnt in Human Resources mit dem Mitarbeiterprofil, dem Gehalt und dem Abzug sowie den Beitragsinformationen.</span><span class="sxs-lookup"><span data-stu-id="807c0-106">The integrated experience begins in Human Resources with the employee profile, salary and deduction, and contribution information.</span></span> <span data-ttu-id="807c0-107">Wenn Sie einen Mitarbeiter einstellen und das erforderliche Profil und die Zahlungsinformationen in Human Resources eingeben, ruft das Lohnsystem diese Informationen ab, um sie bei der Lohnabrechnung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="807c0-107">When you hire an employee and enter the required profile and pay information into Human Resources, the payroll system pulls this information to use when processing payroll.</span></span> <span data-ttu-id="807c0-108">Alle am Mitarbeiter oder den Gehaltsinformationen vorgenommenen Aktualisierungen werden auch zur Verwendung in späteren Zahlungsläufen abgerufen.</span><span class="sxs-lookup"><span data-stu-id="807c0-108">Any updates made to the employee or pay information are also pulled for use in later pay runs.</span></span>

![Lohnintegrations-Flow](media/hr-admin-integration-payroll-api-introduction-flow.png)

<span data-ttu-id="807c0-110">Um die Integration zu ermöglichen, enthält Human Resources die folgenden Komponenten:</span><span class="sxs-lookup"><span data-stu-id="807c0-110">To enable the integration, Human Resources includes the following components:</span></span>

- <span data-ttu-id="807c0-111">Funktionalität, um einen Mitarbeiter als „Bereit für Zahlung“ zu kennzeichnen</span><span class="sxs-lookup"><span data-stu-id="807c0-111">Functionality to mark an employee as ready to pay</span></span>
- <span data-ttu-id="807c0-112">Eine Integrations-API öffnet die neue Funktionalität für die Integration von Anwendungen</span><span class="sxs-lookup"><span data-stu-id="807c0-112">An integration API opening up the new functionality to integrating applications</span></span>

## <a name="microsoft-dataverse"></a><span data-ttu-id="807c0-113">Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="807c0-113">Microsoft Dataverse</span></span>

<span data-ttu-id="807c0-114">Diese API basiert auf Microsoft Dataverse (früher Common Data Service).</span><span class="sxs-lookup"><span data-stu-id="807c0-114">This API is built on Microsoft Dataverse (formerly Common Data Service).</span></span> <span data-ttu-id="807c0-115">Alle RESTful-Interaktionen mit dieser API erfolgen über die Microsoft Dataverse-Web-API, die OData verwendet.</span><span class="sxs-lookup"><span data-stu-id="807c0-115">All RESTful interaction with this API is done via the Microsoft Dataverse Web API, which uses OData.</span></span> <span data-ttu-id="807c0-116">Diese API ist eine Teilmenge der Dataverse-Web-API.</span><span class="sxs-lookup"><span data-stu-id="807c0-116">This API is a subset of the Dataverse Web API.</span></span> <span data-ttu-id="807c0-117">Die Dataverse-Web-API definiert Merkmale wie Authentifizierung, SLAs, Stapelverarbeitung, Parallelitätskontrolle und Fehlerbehandlung.</span><span class="sxs-lookup"><span data-stu-id="807c0-117">The Dataverse Web API defines characteristics such as authentication, SLAs, batch, concurrency control, and error handling.</span></span>

<span data-ttu-id="807c0-118">Weitere allgemeine Informationen zur Microsoft Dataverse-Web-API finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="807c0-118">For more general information about the Microsoft Dataverse Web API, see:</span></span>

- [<span data-ttu-id="807c0-119">Was ist Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="807c0-119">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)
- [<span data-ttu-id="807c0-120">Verwenden der Microsoft Dataverse-Web-API</span><span class="sxs-lookup"><span data-stu-id="807c0-120">Use the Microsoft Dataverse Web API</span></span>](/powerapps/developer/data-platform/webapi/overview)
- [<span data-ttu-id="807c0-121">Microsoft Dataverse-Entwicklerhandbuch</span><span class="sxs-lookup"><span data-stu-id="807c0-121">Microsoft Dataverse developer guide</span></span>](/powerapps/developer/data-platform)

<span data-ttu-id="807c0-122">Diese Dokumentation enthält Details und Entwickleranleitungen für die Verwendung der Dataverse Web-API, einschließlich der folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="807c0-122">This documentation includes details and developer guidance for using the Dataverse Web API, including the following topics:</span></span>

- [<span data-ttu-id="807c0-123">Authentifizierung bei Microsoft Dataverse mit der Web-API</span><span class="sxs-lookup"><span data-stu-id="807c0-123">Authenticate to Microsoft Dataverse with the Web API</span></span>](/powerapps/developer/data-platform/webapi/authenticate-web-api)
- [<span data-ttu-id="807c0-124">Vorgänge mit der Web-API ausführen</span><span class="sxs-lookup"><span data-stu-id="807c0-124">Perform operations using the Web API</span></span>](/powerapps/developer/data-platform/webapi/perform-operations-web-api)
- [<span data-ttu-id="807c0-125">Postman mit der Web-API verwenden</span><span class="sxs-lookup"><span data-stu-id="807c0-125">Use Postman with the Web API</span></span>](/powerapps/developer/data-platform/webapi/use-postman-web-api)
- [<span data-ttu-id="807c0-126">Die Änderungsverfolgung zum Synchronisieren von Daten mit externen Systemen verwenden</span><span class="sxs-lookup"><span data-stu-id="807c0-126">Use change tracking to synchronize data with external systems</span></span>](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems)

### <a name="virtual-tables-for-human-resources-in-dataverse"></a><span data-ttu-id="807c0-127">Virtuelle Tabellen für Human Resources in Dataverse</span><span class="sxs-lookup"><span data-stu-id="807c0-127">Virtual tables for Human Resources in Dataverse</span></span>

<span data-ttu-id="807c0-128">Die Endpunkte für die Lohnintegrations-API verwenden die Funktionen der Plattform für virtuelle Tabellen von Microsoft Dataverse.</span><span class="sxs-lookup"><span data-stu-id="807c0-128">The endpoints for the Payroll integration API use the virtual table platform capabilities of Microsoft Dataverse.</span></span> <span data-ttu-id="807c0-129">Standardmäßig werden die virtuellen Tabellen und die zugehörigen API-Endpunkte nicht für Human Resources-Umgebungen bereitgestellt, sodass Unternehmen bestimmen können, welche OData-Endpunkte für die Umgebung verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="807c0-129">By default, the virtual tables and their associated API endpoints aren't deployed for Human Resources environments, enabling organizations to determine which OData endpoints will be exposed for the environment.</span></span> <span data-ttu-id="807c0-130">Um die API verwenden zu können, müssen die virtuellen Tabellen für die Personalentitäten für die Umgebung generiert werden.</span><span class="sxs-lookup"><span data-stu-id="807c0-130">To use the API, the virtual tables for the Human Resources entities must be generated for the environment.</span></span>

<span data-ttu-id="807c0-131">Informationen zum Generieren der virtuellen Tabellen für die API finden Sie unter [Konfigurieren von virtuellen Dataverse-Tabellen](./hr-admin-integration-common-data-service-virtual-entities.md).</span><span class="sxs-lookup"><span data-stu-id="807c0-131">For information on generating the virtual tables for the API, see [Configure Dataverse virtual tables](./hr-admin-integration-common-data-service-virtual-entities.md).</span></span>

## <a name="data-model"></a><span data-ttu-id="807c0-132">Datenmodell</span><span class="sxs-lookup"><span data-stu-id="807c0-132">Data model</span></span>

<span data-ttu-id="807c0-133">Das folgende Diagramm veranschaulicht die Beziehungen innerhalb der API.</span><span class="sxs-lookup"><span data-stu-id="807c0-133">The following diagram illustrates relationships within the API.</span></span> <span data-ttu-id="807c0-134">Einige Typen verfügen über Fremdschlüssel für andere bereits vorhandene Entitäten in Human Resources, die hier nicht dargestellt sind.</span><span class="sxs-lookup"><span data-stu-id="807c0-134">Several types have foreign keys to other, pre-existing entities in Human Resources that aren't illustrated here.</span></span> <span data-ttu-id="807c0-135">Dieses Dokument enthält Informationen zu Entitäten, die für die Lohnintegrationsszenarien spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="807c0-135">This document provides information on entities that are specific to payroll integration scenarios.</span></span> <span data-ttu-id="807c0-136">Es gibt jedoch viele andere Entitäten in der Dataverse-Web-API für Human Resources, die auch für Ihre Integration relevant sein können.</span><span class="sxs-lookup"><span data-stu-id="807c0-136">However, there are many other entities in the Dataverse Web API for Human Resources that may also be relevant to your integration.</span></span> <span data-ttu-id="807c0-137">Einige dieser Entitäten werden in Fremdschlüsselbeziehungen oder Navigationseigenschaften referenziert.</span><span class="sxs-lookup"><span data-stu-id="807c0-137">Some of these entities are referenced in foreign key relationships or navigation properties.</span></span>

![Datenmodell der Lohnintegrations-API](media/hr-admin-payroll-api-data-model.png)

## <a name="payroll-employee-and-related-entities"></a><span data-ttu-id="807c0-139">Mitarbeiter der Lohnbuchhaltung und verbindene Entitäten</span><span class="sxs-lookup"><span data-stu-id="807c0-139">Payroll employee and related entities</span></span>

<span data-ttu-id="807c0-140">Entitäten:</span><span class="sxs-lookup"><span data-stu-id="807c0-140">Entities:</span></span>

- [<span data-ttu-id="807c0-141">Mitarbeiter der Lohnbuchhaltung</span><span class="sxs-lookup"><span data-stu-id="807c0-141">Payroll employee</span></span>](hr-admin-integration-payroll-api-payroll-employee.md)
- [<span data-ttu-id="807c0-142">Lohn – Adresse der Arbeitskraft</span><span class="sxs-lookup"><span data-stu-id="807c0-142">Payroll worker address</span></span>](hr-admin-integration-payroll-api-payroll-worker-address.md)
- [<span data-ttu-id="807c0-143">Fester Vergütungsplan für Lohnabrechnung</span><span class="sxs-lookup"><span data-stu-id="807c0-143">Payroll fixed compensation plan</span></span>](hr-admin-integration-ats-api-recruiting-request-education.md)
- [<span data-ttu-id="807c0-144">Lohnpositions-Einzelvorgang</span><span class="sxs-lookup"><span data-stu-id="807c0-144">Payroll position job</span></span>](hr-admin-integration-payroll-api-payroll-position-job.md)
- [<span data-ttu-id="807c0-145">Lohnposition</span><span class="sxs-lookup"><span data-stu-id="807c0-145">Payroll position</span></span>](hr-admin-integration-payroll-api-payroll-position.md)

## <a name="see-also"></a><span data-ttu-id="807c0-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="807c0-146">See also</span></span>

[<span data-ttu-id="807c0-147">Lohnentitäten generieren und überprüfen</span><span class="sxs-lookup"><span data-stu-id="807c0-147">Generate and review payroll entities</span></span>](hr-admin-integration-payroll-api-generate-review-entities.md)<br>
[<span data-ttu-id="807c0-148">Parameter in Human Resources konfigurieren</span><span class="sxs-lookup"><span data-stu-id="807c0-148">Configure Human Resources parameters</span></span>](hr-setup-parameters.md)<br>
[<span data-ttu-id="807c0-149">Freigegebene Human Resources Parameter konfigurieren</span><span class="sxs-lookup"><span data-stu-id="807c0-149">Configure Human Resources shared parameters</span></span>](hr-setup-shared-parameters.md)<br>
[<span data-ttu-id="807c0-150">Was ist Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="807c0-150">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="807c0-151">Verwenden der Microsoft Dataverse-Web-API</span><span class="sxs-lookup"><span data-stu-id="807c0-151">Use the Microsoft Dataverse Web API</span></span>](/powerapps/developer/data-platform/webapi/overview)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]