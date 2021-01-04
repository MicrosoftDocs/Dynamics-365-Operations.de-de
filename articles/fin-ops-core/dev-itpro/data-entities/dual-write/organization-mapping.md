---
title: Organisationshierarchie in Dataverse
description: In diesem Thema wird die Integration von Organisationsdaten zwischen Finance and Operations Apps und Dataverse beschrieben.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: e2b652f11db62eb58ffc2ec2fc4322149e7d45d1
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680071"
---
# <a name="organization-hierarchy-in-dataverse"></a>Organisationshierarchie in Dataverse

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Da Dynamics 365 Finance ein Finanzsystem ist, ist *Organisation* ein Grundkonzept, und die Systemeinrichtung beginnt mit der Konfiguration einer Organisationshierarchie. Unternehmensfinanzen können auf Organisationsebene und auch auf jeder anderen Ebene in der Organisationshierarchie verfolgt werden.

Obwohl es in Dataverse nicht das Konzept einer Organisationshierarchie gibt, gibt es mehrere lose Konzepte, beispielsweise Gesamtverkaufserlös. Im Rahmen der Dataverse-Integration wird die Datenstruktur der Organisationshierarchie zu Dataverse hinzugefügt.

## <a name="data-flow"></a>Datenfluss

Ein Geschäftsökosystem, das aus Finance and Operations Apps und Dataverse besteht, wird weiterhin eine Organisationshierarchie haben. Diese Organisationshierarchie basiert auf Finance and Operations Apps, wird aber in Dataverse zu Informations- und Erweiterbarkeitszwecken verfügbar gemacht. Die folgende Abbildung zeigt die Organisationshierarchieinformationen, die in Dataverse als unidirektionaler Datenfluss von Finance and Operations Apps nach Dataverse verfügbar gemacht werden.

![Architekturabbildung](media/dual-write-data-flow.png)

Tabellenzuordnungen der Organisationshierarchie sind für die unidirektionale Synchronisierung von Finance and Operations-Apps zu Dataverse verfügbar.

## <a name="templates"></a>Vorlagen

Produktinformationen enthält alle Informationen, die mit dem Produkt und seiner Definition in Verbindung stehen, z. B. den Produktdimensionen oder den Nachverfolgungs- und Lagerdimensionen. Wie die folgende Tabelle zeigt, wird eine Sammlung von Tabellenzuordnungen erstellt, um Produkte und zugehörige Informationen zu synchronisieren.

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

Interne Organisationsinformationen in Dataverse stammen aus zwei Tabellen, **Organisationseinheit** und **Juristische Personen**.

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]
