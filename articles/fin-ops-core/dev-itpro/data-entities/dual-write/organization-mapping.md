---
title: Organisationshierarchie in Dataverse
description: Dieser Artikel beschreibt die Integration von Organisationsdaten zwischen Finanz- und Betriebs-Apps und Dataverse.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 48533dd104f62080d0ebd47389a4a829c772db13
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289045"
---
# <a name="organization-hierarchy-in-dataverse"></a>Organisationshierarchie in Dataverse

[!include [banner](../../includes/banner.md)]



Da Dynamics 365 Finance ein Finanzsystem ist, ist *Organisation* ein Grundkonzept, und die Systemeinrichtung beginnt mit der Konfiguration einer Organisationshierarchie. Unternehmensfinanzen können auf Organisationsebene und auch auf jeder anderen Ebene in der Organisationshierarchie verfolgt werden.

Obwohl es in Dataverse nicht das Konzept einer Organisationshierarchie gibt, gibt es mehrere lose Konzepte, beispielsweise Gesamtverkaufserlös. Im Rahmen der Dataverse-Integration wird die Datenstruktur der Organisationshierarchie zu Dataverse hinzugefügt.

## <a name="data-flow"></a>Datenfluss

Ein Business-Ökosystem, das aus Finanz- und Betriebs-Apps und Dataverse besteht, wird weiterhin eine Organisationshierarchie haben. Diese Organisationshierarchie ist auf Finanz- und Betriebs-Apps aufgebaut, wird aber zu Informations- und Erweiterungszwecken in Dataverse dargestellt. Die folgende Abbildung zeigt die Informationen zur Organisationshierarchie, die in Dataverse als einseitiger Datenfluss von Finanz- und Betriebs-Apps zu Dataverse dargestellt werden.

![Architekturabbildung.](media/dual-write-data-flow.png)

Für die einseitige Synchronisierung von Daten aus Finanz- und Betriebs-Apps mit Dataverse stehen Zuordnungen von Organisationshierarchien zur Verfügung.

## <a name="templates"></a>Vorlagen

Eine Organisation ist eine Gruppe von Personen, die zusammenarbeiten, um einen Geschäftsprozess durchzuführen oder ein Ziel zu erreichen. Organisationshierarchien stellen die Beziehungen zwischen den Organisationen dar, aus denen das Unternehmen besteht. Sie können die folgenden Typen von internen Organisationen definieren: juristische Personen, Organisationseinheiten und Teams. Wie die folgende Tabelle zeigt, wird eine Sammlung von Tabellenzuordnungen erstellt, um die juristischen Entitäten, die operativen Einheiten und die zugehörigen Hierarchieinformationen der Organisation zu synchronisieren.

Finanz- und Betriebs-Apps | Customer Engagement-Apps     | Description
-----------------------|--------------------------------|---
[Juristische Personen](mapping-reference.md#102) | cdm_companies | 
[Juristische Personen](mapping-reference.md#142) | msdyn_internalorganizations |
[Organisationseinheit](mapping-reference.md#143) | msdyn_internalorganizations |
[Organisationshierarchie – veröffentlicht](mapping-reference.md#139) | msdyn_internalorganizationhierarchies | Diese Vorlage bietet eine unidirektionale Synchronisierung der Tabelle „Veröffentlichte Organisationshierarchie“.
[Organisationshierarchiezwecke](mapping-reference.md#140) | msdyn_internalorganizationhierarchypurposes | Diese Vorlage ermöglicht eine unidirektionale Synchronisierung der Tabelle „Zweck der Organisationshierarchie“.
[Organisationshierarchietyp](mapping-reference.md#141) | msdyn_internalorganizationhierarchytypes | Diese Vorlage ermöglicht eine unidirektionale Synchronisierung der Tabelle „Organisationshierarchietyp“.

## <a name="internal-organization"></a>Interne Organisation

Interne Organisationsinformationen in Dataverse stammen aus zwei Tabellen, **Organisationseinheit** und **Juristische Personen**.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

