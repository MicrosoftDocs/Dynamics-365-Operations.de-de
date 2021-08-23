---
title: Einführung Lohnintegrations-API
description: Dieses Thema beschreibt die Lohnintegrations-API in Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7122dc7325c7fb33c4bf90e3d1a6cf1c95bd73e72232b9060f7cc04899223765
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6782706"
---
# <a name="payroll-integration-api-introduction"></a>Einführung Lohnintegrations-API

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dieses Dokument beschreibt die Lohnintegrations-API in Dynamics 365 Human Resources. Die API ermöglicht eine optimierte End-to-End-Integration zwischen Human Resources und Partner-Lohnsystemen. Die integrierte Erfahrung beginnt in Human Resources mit dem Mitarbeiterprofil, dem Gehalt und dem Abzug sowie den Beitragsinformationen. Wenn Sie einen Mitarbeiter einstellen und das erforderliche Profil und die Zahlungsinformationen in Human Resources eingeben, ruft das Lohnsystem diese Informationen ab, um sie bei der Lohnabrechnung zu verwenden. Alle am Mitarbeiter oder den Gehaltsinformationen vorgenommenen Aktualisierungen werden auch zur Verwendung in späteren Zahlungsläufen abgerufen.

[![Lohnintegrations-Flow.](media/hr-admin-integration-payroll-api-introduction-flow.png)](media/hr-admin-integration-payroll-api-introduction-flow-2.png#lightbox)

Um die Integration zu ermöglichen, enthält Human Resources die folgenden Komponenten:

- [Funktionalität, um einen Mitarbeiter als „Bereit für Zahlung“ zu kennzeichnen.](hr-compensation-payroll.md)
- Eine Integrations-API öffnet die neue Funktionalität für die Integration von Anwendungen.

## <a name="microsoft-dataverse"></a>Microsoft Dataverse

Diese API basiert auf Microsoft Dataverse (früher Common Data Service). Alle RESTful-Interaktionen mit dieser API erfolgen über die Microsoft Dataverse-Web-API, die OData verwendet. Diese API ist eine Teilmenge der Dataverse-Web-API. Die Dataverse-Web-API definiert Merkmale wie Authentifizierung, SLAs, Stapelverarbeitung, Parallelitätskontrolle und Fehlerbehandlung.

Weitere allgemeine Informationen zur Microsoft Dataverse-Web-API finden Sie unter:

- [Was ist Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)
- [Verwenden der Microsoft Dataverse-Web-API](/powerapps/developer/data-platform/webapi/overview)
- [Microsoft Dataverse-Entwicklerhandbuch](/powerapps/developer/data-platform)

Diese Dokumentation enthält Details und Entwickleranleitungen für die Verwendung der Dataverse Web-API, einschließlich der folgenden Themen:

- [Authentifizierung bei Microsoft Dataverse mit der Web-API](/powerapps/developer/data-platform/webapi/authenticate-web-api)
- [Vorgänge mit der Web-API ausführen](/powerapps/developer/data-platform/webapi/perform-operations-web-api)
- [Postman mit der Web-API verwenden](/powerapps/developer/data-platform/webapi/use-postman-web-api)
- [Die Änderungsverfolgung zum Synchronisieren von Daten mit externen Systemen verwenden](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems)

### <a name="virtual-tables-for-human-resources-in-dataverse"></a>Virtuelle Tabellen für Human Resources in Dataverse

Die Endpunkte für die Lohnintegrations-API verwenden die Funktionen der Plattform für virtuelle Tabellen von Microsoft Dataverse. Standardmäßig werden die virtuellen Tabellen und die zugehörigen API-Endpunkte nicht für Human Resources-Umgebungen bereitgestellt, sodass Unternehmen bestimmen können, welche OData-Endpunkte für die Umgebung verfügbar gemacht werden. Um die API verwenden zu können, müssen die virtuellen Tabellen für die Personalentitäten für die Umgebung generiert werden.

Informationen zum Generieren der virtuellen Tabellen für die API finden Sie unter [Konfigurieren von virtuellen Dataverse-Tabellen](./hr-admin-integration-common-data-service-virtual-entities.md).

## <a name="data-model"></a>Datenmodell

Das folgende Diagramm veranschaulicht die Beziehungen innerhalb der API. Einige Typen verfügen über Fremdschlüssel für andere bereits vorhandene Entitäten in Human Resources, die hier nicht dargestellt sind. Dieses Dokument enthält Informationen zu Entitäten, die für die Lohnintegrationsszenarien spezifisch sind. Es gibt jedoch viele andere Entitäten in der Dataverse-Web-API für Human Resources, die auch für Ihre Integration relevant sein können. Einige dieser Entitäten werden in Fremdschlüsselbeziehungen oder Navigationseigenschaften referenziert.

[![Datenmodell der Lohnintegrations-API.](media/hr-admin-payroll-api-data-model.png)](media/hr-admin-payroll-api-data-model.png#lightbox)

## <a name="payroll-employee-and-related-entities"></a>Mitarbeiter der Lohnbuchhaltung und verbindene Entitäten

Entitäten:

- [Mitarbeiter der Lohnbuchhaltung](hr-admin-integration-payroll-api-payroll-employee.md)
- [Lohn – Adresse der Arbeitskraft](hr-admin-integration-payroll-api-payroll-worker-address.md)
- [Fester Vergütungsplan für Lohnabrechnung](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md)
- [Variabler Vergütungsplan für Lohnabrechnung](hr-admin-integration-payroll-api-payroll-variable-compensation-plan.md)
- [Lohnpositions-Einzelvorgang](hr-admin-integration-payroll-api-payroll-position-job.md)
- [Lohnposition](hr-admin-integration-payroll-api-payroll-position.md)

## <a name="see-also"></a>Siehe auch

[Lohnentitäten generieren und überprüfen](hr-admin-integration-payroll-api-generate-review-entities.md)<br>
[Parameter in Human Resources konfigurieren](hr-setup-parameters.md)<br>
[Freigegebene Human Resources Parameter konfigurieren](hr-setup-shared-parameters.md)<br>
[Was ist Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)<br>
[Verwenden der Microsoft Dataverse-Web-API](/powerapps/developer/data-platform/webapi/overview)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
