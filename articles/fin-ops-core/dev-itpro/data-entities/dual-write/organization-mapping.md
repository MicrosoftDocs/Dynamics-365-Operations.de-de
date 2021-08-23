---
title: Organisationshierarchie in Dataverse
description: In diesem Thema wird die Integration von Organisationsdaten zwischen Finance and Operations Apps und Dataverse beschrieben.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 30826bf69525a85bede6ec0b64ec1a579aea26a0a6c487583739ad3fcb787a28
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6769244"
---
# <a name="organization-hierarchy-in-dataverse"></a>Organisationshierarchie in Dataverse

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Da Dynamics 365 Finance ein Finanzsystem ist, ist *Organisation* ein Grundkonzept, und die Systemeinrichtung beginnt mit der Konfiguration einer Organisationshierarchie. Unternehmensfinanzen können auf Organisationsebene und auch auf jeder anderen Ebene in der Organisationshierarchie verfolgt werden.

Obwohl es in Dataverse nicht das Konzept einer Organisationshierarchie gibt, gibt es mehrere lose Konzepte, beispielsweise Gesamtverkaufserlös. Im Rahmen der Dataverse-Integration wird die Datenstruktur der Organisationshierarchie zu Dataverse hinzugefügt.

## <a name="data-flow"></a>Datenfluss

Ein Geschäftsökosystem, das aus Finance and Operations Apps und Dataverse besteht, wird weiterhin eine Organisationshierarchie haben. Diese Organisationshierarchie basiert auf Finance and Operations Apps, wird aber in Dataverse zu Informations- und Erweiterbarkeitszwecken verfügbar gemacht. Die folgende Abbildung zeigt die Organisationshierarchieinformationen, die in Dataverse als unidirektionaler Datenfluss von Finance and Operations Apps nach Dataverse verfügbar gemacht werden.

![Architekturabbildung.](media/dual-write-data-flow.png)

Tabellenzuordnungen der Organisationshierarchie sind für die unidirektionale Synchronisierung von Finance and Operations-Apps zu Dataverse verfügbar.

## <a name="templates"></a>Vorlagen

Produktinformationen enthält alle Informationen, die mit dem Produkt und seiner Definition in Verbindung stehen, z. B. den Produktdimensionen oder den Nachverfolgungs- und Lagerdimensionen. Wie die folgende Tabelle zeigt, wird eine Sammlung von Tabellenzuordnungen erstellt, um Produkte und zugehörige Informationen zu synchronisieren.

Finance and Operations-Apps | Customer Engagement-Apps     | Beschreibung
-----------------------|--------------------------------|---
[Juristische Personen](mapping-reference.md#102) | cdm_companies | Bietet eine bidirektionale Synchronisierung von Daten von juristischen Person (Unternehmen).
[Juristische Personen](mapping-reference.md#142) | msdyn_internalorganizations |
[Organisationseinheit](mapping-reference.md#143) | msdyn_internalorganizations |
[Organisationshierarchie – veröffentlicht](mapping-reference.md#139) | msdyn_internalorganizationhierarchies | Diese Vorlage bietet eine unidirektionale Synchronisierung der Tabelle „Veröffentlichte Organisationshierarchie“.
[Organisationshierarchiezwecke](mapping-reference.md#140) | msdyn_internalorganizationhierarchypurposes | Diese Vorlage ermöglicht eine unidirektionale Synchronisierung der Tabelle „Zweck der Organisationshierarchie“.
[Organisationshierarchietyp](mapping-reference.md#141) | msdyn_internalorganizationhierarchytypes | Diese Vorlage ermöglicht eine unidirektionale Synchronisierung der Tabelle „Organisationshierarchietyp“.

## <a name="internal-organization"></a>Interne Organisation

Interne Organisationsinformationen in Dataverse stammen aus zwei Tabellen, **Organisationseinheit** und **Juristische Personen**.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
