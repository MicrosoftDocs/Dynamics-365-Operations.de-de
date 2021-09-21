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
ms.openlocfilehash: 45995ed6f051cdf6be2b2985ff0e2cb1decf4cf0
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476427"
---
# <a name="multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a>Die Option „Mehrfach-SKU“ wertet nicht mehrere Lagerplatzrichtlinien-Aktivitäten aus.

## <a name="symptoms"></a>Symptome

Lagerplatzrichtlinien der Arbeitsauftragsart *Verkaufsaufträge* und der Arbeitsauftragsart *Einlagern* werten nicht mehrere Lagerplatzrichtlinien-Aktionen aus, wenn die Option **Mehrere SKU** ausgewählt ist. Es wird nur die erste Aktion der Lagerplatzrichtlinie ausgewertet.

## <a name="resolution"></a>Lösung

Eine neue Funktion, *Alle Aktionen für Multi SKU Lagerplatzrichtlinien auswerten*, wurde in Version 10.0.15 hinzugefügt (siehe [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)). Diese Funktion wertet alle Aktionen für Multi-SKU Lagerplatzrichtlinien aus. Wenn Sie diese Funktion benötigen, verwenden Sie [Funktionsverwaltung](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview), um sie zu aktivieren.
