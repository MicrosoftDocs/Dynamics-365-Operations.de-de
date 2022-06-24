---
title: Dispositionscodes synchronisieren
description: In diesem Artikel wird die Synchronisierung von Dispositionscodes für den Intercompany-Handel erläutert.
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: d347181dd6ba12de0e114d74d43cd46230ba4fb7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905659"
---
# <a name="synchronize-intercompany-disposition-codes"></a>Intercompany-Dispositionscodes synchronisieren

[!include [banner](../../includes/banner.md)]

Zur Unterstützung von Intercompany-Retouren ermöglicht Microsoft Dynamics 365 Supply Chain Management das Zuordnen extern definierter Dispositionscodes zu entsprechenden internen Dispositionscodes. Beim Einrichten einer Intercompany-Kette müssen die Dispositionsaktivitäten der beiden Unternehmen, die sich gegenseitig zugeordnet werden, übereinstimmen. Andernfalls ist die Synchronisierung nicht erfolgreich.

## <a name="about-disposition-codes-for-three-legged-direct-returns"></a>Informationen zu Dispositionscodes für dreigliedrige Direktretouren

Dispositionscodes werden aus der Intercompany-Auftragsposition heraus mit der ursprünglichen Auftragsposition synchronisiert. Die Synchronisierung hat jedoch lediglich eine einzige direkte Auswirkung auf die ursprüngliche Auftragsposition: Die sonstigen Zuschläge für Positionen werden auf der Grundlage des Dispositionscodes und der im Unternehmen A eingerichteten sonstigen Zuschläge gelöscht. Unternehmen A ist das Unternehmen, von dem die Rücklieferung erstellt wird.

In einer dreigliedrigen Direktlieferungskette werden alle Dispositionsaktivitäten in der Intercompany-Auftragsposition unterstützt. Wird das Produkt jedoch an den Debitor zurückgeliefert, muss sichergestellt werden, dass die Lieferadresse der Rücklieferung mit der Lieferadresse des Debitors übereinstimmt, die im ursprünglichen Auftrag angegeben ist.

> [!NOTE]
> Für Bestellungen sind keine Dispositionscodes vorhanden. Aus diesem Grund muss die Synchronisierung von Dispositionscodes zwischen Intercompany-Auftrag und ursprünglicher Rücklieferung von Auftrag zu Auftrag erfolgen.

## <a name="replacing-returned-items"></a>Austauschen zurückgelieferter Artikel

Wird ein zurückgelieferter Artikel ausgetauscht, und in Unternehmen B wurde bereits ein Ersetzungsauftrag erstellt, kann kein Dispositionscode ausgewählt werden, und in Unternehmen A wird kein zusätzlicher Ersetzungsauftrag erstellt.

## <a name="rules-for-intercompany-direct-deliveries"></a>Regeln für Intercompany-Direktlieferungen

Für ursprüngliche Rücklieferungen in Szenarios mit Intercompany-Direktlieferung gelten die folgenden allgemeinen Regeln:

- Liegt der ursprünglichen Auftragsposition die Dispositionsaktivität „Entlastung und Aussonderung“, „Entlastung“ oder „Rückgabe an den Debitor“ zugrunde, wird die Dispositionsaktivität „Entlastung“ verwendet. Durch den Aktivitätscode „Rückgabe an den Debitor“ wird jedoch der Nettobetrag der vorhandenen Position und der neu synchronisierten Position aus dem Intercompany-Auftrag auf Null festgelegt. Ausschusspositionen werden zudem niemals synchronisiert. Wird einem Intercompany-Auftrag eine Position hinzugefügt, wird diese für einen Auftrag mit einer positiven Menge und der Dispositionsaktivität „Ausschuss“ niemals synchronisiert (Beispiel: „Entlastung und Aussonderung“ oder „Ersatz und Aussonderung“).
- Liegt eine Dispositionsaktivität vom Typ „Entlastung und Aussonderung“ oder „Ersatz und Aussonderung“ zugrunde, wird diese nicht außer Kraft gesetzt. Sie wird als Dispositionsaktivität vom Typ „Entlastung und Aussonderung“ oder „Ersatz und Aussonderung“ behandelt. Diese Regel gilt auch, wenn in Unternehmen A keine Ausschussposition und in Unternehmen B (dem Unternehmen, bei dem der zurückgelieferte Artikel eingeht) kein Ersetzungsauftrag erstellt wird. In Unternehmen A wird nur dann ein Ersetzungsauftrag erstellt, wenn eine Lieferscheinaktualisierung ausgeführt wird.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
