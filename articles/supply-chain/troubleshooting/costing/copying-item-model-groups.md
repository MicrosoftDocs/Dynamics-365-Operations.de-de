---
title: Feldeinstellungen fehlen, wenn Artikelmodellgruppen in eine andere juristische Person kopiert werden
description: Feldeinstellungen fehlen, wenn Artikelmodellgruppen in eine andere juristische Person kopiert werden.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6f6fdfef0bc377418ed8a9c8830e74526a0b95eb
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026536"
---
# <a name="missing-field-settings-when-item-model-groups-are-copied-to-another-legal-entity"></a>Feldeinstellungen fehlen, wenn Artikelmodellgruppen in eine andere juristische Person kopiert werden

KB-Nummer: 4612800

## <a name="symptoms"></a>Symptome

Wenn Sie Artikelmodellgruppen mithilfe der Entität *Bestandsrichtlinien für Artikelmodellgruppen* in eine andere juristische Person (Firma) kopieren, fehlen in der neuen Modellgruppe in der als Ziel angegebenen juristischen Person einige Feldeinstellungen (z. B. das Bestandsmodell und die Beschreibung).

## <a name="resolution"></a>Lösung

Um eine vollständige Kopie einer Artikelmodellgruppe für eine andere juristische Person zu erstellen, müssen Sie auch die Bestandsrichtlinien für Artikelmodellgruppen (`InventInventoryPolicyEntity`) sowie die Richtlinien zur Kostenflussannahme (`InventCostFlowAssumptionPolicyEntity`), die der Artikelmodellgruppe zugeordnet sind, auswählen.
