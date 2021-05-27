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
# <a name="missing-field-settings-when-item-model-groups-are-copied-to-another-legal-entity"></a><span data-ttu-id="ec7c5-103">Feldeinstellungen fehlen, wenn Artikelmodellgruppen in eine andere juristische Person kopiert werden</span><span class="sxs-lookup"><span data-stu-id="ec7c5-103">Missing field settings when item model groups are copied to another legal entity</span></span>

<span data-ttu-id="ec7c5-104">KB-Nummer: 4612800</span><span class="sxs-lookup"><span data-stu-id="ec7c5-104">KB number: 4612800</span></span>

## <a name="symptoms"></a><span data-ttu-id="ec7c5-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="ec7c5-105">Symptoms</span></span>

<span data-ttu-id="ec7c5-106">Wenn Sie Artikelmodellgruppen mithilfe der Entität *Bestandsrichtlinien für Artikelmodellgruppen* in eine andere juristische Person (Firma) kopieren, fehlen in der neuen Modellgruppe in der als Ziel angegebenen juristischen Person einige Feldeinstellungen (z. B. das Bestandsmodell und die Beschreibung).</span><span class="sxs-lookup"><span data-stu-id="ec7c5-106">When you copy item model groups to another legal entity (company) by using the *Item model group inventory policies* entity, some field settings (for example, the inventory model and description) are missing in the new model group in the destination legal entity.</span></span>

## <a name="resolution"></a><span data-ttu-id="ec7c5-107">Lösung</span><span class="sxs-lookup"><span data-stu-id="ec7c5-107">Resolution</span></span>

<span data-ttu-id="ec7c5-108">Um eine vollständige Kopie einer Artikelmodellgruppe für eine andere juristische Person zu erstellen, müssen Sie auch die Bestandsrichtlinien für Artikelmodellgruppen (`InventInventoryPolicyEntity`) sowie die Richtlinien zur Kostenflussannahme (`InventCostFlowAssumptionPolicyEntity`), die der Artikelmodellgruppe zugeordnet sind, auswählen.</span><span class="sxs-lookup"><span data-stu-id="ec7c5-108">To create a complete copy of an item model group to another legal entity, you must also select both the item model group inventory policies (`InventInventoryPolicyEntity`) and the cost flow assumption policies (`InventCostFlowAssumptionPolicyEntity`) that are associated with the item model group.</span></span>
