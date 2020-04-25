---
title: Organisationshierarchie in Common Data Service
description: In diesem Thema wird die Integration von Organisationsdaten zwischen Finance and Operations Apps und Common Data Service beschrieben.
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
ms.openlocfilehash: fc5db8d04a2860df0c917816e2910c6fbda941ff
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173153"
---
# <a name="organization-hierarchy-in-common-data-service"></a>Organisationshierarchie in Common Data Service

[!include [banner](../../includes/banner.md)]



Da Dynamics 365 Finance ein Finanzsystem ist, ist *Organisation* ein Grundkonzept, und die Systemeinrichtung beginnt mit der Konfiguration einer Organisationshierarchie. Unternehmensfinanzen können auf Organisationsebene und auch auf jeder anderen Ebene in der Organisationshierarchie verfolgt werden.

Obwohl es in Common Data Service nicht das Konzept einer Organisationshierarchie gibt, gibt es mehrere lose Konzepte, beispielsweise Gesamtverkaufserlös. Im Rahmen der Common Data Service-Integration wird die Datenstruktur der Organisationshierarchie zu Common Data Service hinzugefügt.

## <a name="data-flow"></a>Datenfluss

Ein Geschäftsökosystem, das aus Finance and Operations Apps und Common Data Service besteht, wird weiterhin eine Organisationshierarchie haben. Diese Organisationshierarchie basiert auf Finance and Operations Apps, wird aber in Common Data Service zu Informations- und Erweiterbarkeitszwecken verfügbar gemacht. Die folgende Abbildung zeigt die Organisationshierarchieinformationen, die in Common Data Service als unidirektionaler Datenfluss von Finance and Operations Apps nach Common Data Service verfügbar gemacht werden.

![Architekturabbildung](media/dual-write-data-flow.png)

## <a name="templates"></a>Vorlagen

Entitätszuordnungen der Organisationshierarchie sind für die unidirektionale Synchronisierung Finance and Operations Apps zu Common Data Service  verfügbar.

## <a name="templates"></a>Vorlagen

Produktinformationen enthält alle Informationen, die mit dem Produkt und seiner Definition in Verbindung stehen, z. B. den Produktdimensionen oder den Nachverfolgungs- und Lagerdimensionen. Wie die folgende Tabelle zeigt, darstellt, wird eine Sammlung von Entitätszuordnungen erstellt, um Produkte und zugehörige Informationen zu synchronisieren.

Finance and Operations Apps | Sonstige Dynamics 365-Apps | Beschreibung
-----------------------|--------------------------------|---
Organisationshierarchiezwecke | msdyn_internalorganizationhierarchypurposes | Diese Vorlage ermöglicht eine unidirektionale Synchronisierung der Entität „Zweck der Organisationshierarchie“.
Organisationshierarchietyp | msdyn_internalorganizationhierarchytypes | Diese Vorlage ermöglicht eine unidirektionale Synchronisierung der Entität „Organisationshierarchietyp“.
Organisationshierarchie – veröffentlicht | msdyn_internalorganizationhierarchies | Diese Vorlage bietet eine unidirektionale Synchronisierung der Entität „Veröffentlichte Organisationshierarchie“.
Organisationseinheit | msdyn_internalorganizations | 
Juristische Personen | msdyn_internalorganizations | 
Juristische Personen | cdm_companies | Bietet eine bidirektionale Synchronisierung von Daten von juristischen Person (Unternehmen).


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a>Interne Organisation

Informationen zur internen Organisation in Common Data Service stammen aus zwei Entitäten, **Organisationseinheit** und **juristische Personen**.

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]

