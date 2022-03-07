---
title: Alle Aktivitäten für Mehrfach-SKU-Lagerplatzrichtlinien auswerten
description: Eine neue Funktion wurde hinzugefügt, um alle Aktionen für Mehrfach-SKU Lagerplatzrichtlinien auszuwerten. Diese Seite führt Sie zu Informationen zum Aktivieren dieser Funktion.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ea265166902f85c2c09cae08ee6de5cd7094e1b4
ms.sourcegitcommit: 8cb031501a2b2505443599aabffcfece50e01263
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/09/2021
ms.locfileid: "7778401"
---
# <a name="multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a>Die Option „Mehrfach-SKU“ wertet nicht mehrere Lagerplatzrichtlinien-Aktivitäten aus.

## <a name="symptoms"></a>Symptome

Lagerplatzrichtlinien der Arbeitsauftragsart *Verkaufsaufträge* und der Arbeitsauftragsart *Einlagern* werten nicht mehrere Lagerplatzrichtlinien-Aktionen aus, wenn die Option **Mehrere SKU** ausgewählt ist. Es wird nur die erste Aktion der Lagerplatzrichtlinie ausgewertet.

## <a name="resolution"></a>Lösung

Eine neue Funktion, *Alle Aktionen für Multi SKU Lagerplatzrichtlinien auswerten*, wurde in Version 10.0.15 hinzugefügt (siehe [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)). Diese Funktion wertet alle Aktionen für Multi-SKU Lagerplatzrichtlinien aus. Ab Supply Chain Management Version 10.0.21 ist diese Funktion standardmäßig aktiviert. Administratoren können die Seite [Funktionsverwaltung](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) verwenden, um den Status der Funktion zu überprüfen und sie bei Bedarf zu aktivieren oder zu deaktivieren.
