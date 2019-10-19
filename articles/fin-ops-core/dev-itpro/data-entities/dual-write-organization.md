---
title: Organisationshierarchie in Common Data Service
description: In diesem Thema wird die Integration von Organisationsdaten zwischen Finance and Operations-Apps und Common Data Service beschrieben.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: fd159b38f69305dcaecb364ba0ccb3befabb3582
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182024"
---
## <a name="organization-hierarchy-in-common-data-service"></a>Organisationshierarchie in Common Data Service

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Da Dynamics 365 Finance ein Finanzsystem ist, ist *Organisation* ein Grundkonzept, und die Systemeinrichtung beginnt mit der Konfiguration einer Organisationshierarchie. Unternehmensfinanzen können auf Organisationsebene und auch auf jeder anderen Ebene in der Organisationshierarchie verfolgt werden.

Obwohl es in Common Data Service nicht das Konzept einer Organisationshierarchie gibt, gibt es mehrere lose Konzepte, beispielsweise Gesamtverkaufserlös. Im Rahmen der Common Data Service-Integration wird die Datenstruktur der Organisationshierarchie zu Common Data Service hinzugefügt.

## <a name="data-flow"></a>Datenfluss

Ein Geschäftsökosystem, das aus Finance and Operations-Apps and Common Data Service besteht, wird weiterhin eine Organisationshierarchie haben. Diese Organisationshierarchie basiert auf Finance and Operations-Apps, wird aber in Common Data Service zu Informations- und Erweiterbarkeitszwecken verfügbar gemacht. Die folgende Abbildung zeigt die Organisationshierarchieinformationen, die in Common Data Service als unidirektionaler Datenfluss von Finance and Operations-Apps nach Common Data Service verfügbar gemacht werden.

![Architekturabbildung](media/dual-write-data-flow.png)

## <a name="templates"></a>Vorlagen

Entitätszuordnungen der Organisationshierarchie sind für die unidirektionale Synchronisierung von Daten aus Finance and Operations-Apps nach Common Data Service verfügbar.

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="internal-organization-hierarchy-purpose"></a>Zweck der internen Organisationshierarchie

Diese Vorlage bietet eine unidirektionale Synchronisierung der Entität „Zweck der Organisationshierarchie“ von Finance and Operations nach anderen Dynamics 365-Apps.

<!-- ![architecture image](media/dual-write-purpose.png) -->

Quellfeld | Zuordnungstyp | Zielfeld
---|---|---
HIERARCHIETYP | \> | msdyn\_hierarchypurposetypename
HIERARCHIETYP | \> | msdyn\_hierarchytype.msdyn\_name
HIERARCHIEZWECK | \>\> | msdyn\_hierarchypurpose
UNVERÄNDERLICH | \>\> | msdyn\_immutable
SETASDEFAULT | \>\> | msdyn\_setasdefault

## <a name="internal-organization-hierarchy-type"></a>Interner Organisationshierarchietyp

Diese Vorlage bietet eine unidirektionale Synchronisierung der Entität „Organisationshierarchietyp“ von Finance and Operations nach anderen Dynamics 365-Apps.

<!-- ![architecture image](media/dual-write-type.png) -->

Quellfeld | Zuordnungstyp | Zielfeld
---|---|---
NAME | \> | msdyn\_name

## <a name="internal-organization-hierarchy"></a>Interner Organisationshierarchietyp

Diese Vorlage bietet eine unidirektionale Synchronisierung der Entität „Veröffentlichte Organisationshierarchie“ von Finance and Operations nach anderen Dynamics 365-Apps.

<!-- ![architecture image](media/dual-write-organization.png) -->

Quellfeld | Zuordnungstyp | Zielfeld
---|---|---
VALIDTO | \> | msdyn\_validto
VALIDFROM | \> | msdyn\_validfrom
HIERARCHYTYPE | \> | msdyn\_hierarchytypename
PARENTORGANIZATIONPARTYNUMBER | \> | msdyn\_parentpartyid
CHILDORGANIZATIONPARTYNUMBER | \> | msdyn\_childpartyid
HIERARCHYTYPE | \> | msdyn\_hierarchytypeid.msdyn\_name
CHILDORGANIZATIONPARTYNUMBER | \> | msdyn\_childid.msdyn\_partynumber
PARENTORGANIZATIONPARTYNUMBER | \> | msdyn\_parentid.msdyn\_partynumber

## <a name="internal-organization"></a>Interne Organisation

Informationen zur internen Organisation in Common Data Service stammen aus zwei Entitäten, **Organisationseinheit** und **juristische Personen**.

<!-- ![architecture image](media/dual-write-operating-unit.png) -->

<!-- ![architecture image](media/dual-write-legal-entities.png) -->

### <a name="operating-unit"></a>Organisationseinheit

Quellfeld | Zuordnungstyp | Zielfeld
---|---|---
LANGUAGEID | \> | msdyn\_languageid
NAMEALIAS | \> | msdyn\_namealias
NAME | \> | msdyn\_name
PARTYNUMBER | \> | msdyn\_partynumber
OPERATINGUNITTYPE | \>\> | msdyn\_type

### <a name="legal-entity"></a>Juristische Person

Quellfeld | Zuordnungstyp | Zielfeld
---|---|---
NAMEALIAS | \> | msdyn\_namealias
LANGUAGEID | \> | msdyn\_languageid
NAME | \> | msdyn\_name
PARTEINUMMER | \> | msdyn\_partynumber
Kein | \>\> | msdyn\_type
LEGALENTITYID | \> | msdyn\_companycode

## <a name="company"></a>Firma

Bietet eine bidirektionale Synchronisierung von Daten von juristischen Person (Unternehmen) zwischen Finance and Operations und anderen Dynamics 365-Apps.

<!-- ![architecture image](media/dual-write-company.png) -->

Quellfeld | Zuordnungstyp | Zielfeld
---|---|---
NAME | = | cdm\_name
LEGALENTITYID | = | cdm\_companycode
