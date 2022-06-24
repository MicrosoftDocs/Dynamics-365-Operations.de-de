---
title: Intercompany-Aufträge und -Rücklieferungsaufträge
description: In diesem Artikel werden Intercompany-Aufträge und -Rücklieferungsaufträge erläutert.
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
ms.openlocfilehash: 65d0dc6049969ff7d8f84ca4eb3baf486ddad660
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859026"
---
# <a name="intercompany-orders-and-return-orders"></a>Intercompany-Aufträge und -Rücklieferungsaufträge

[!include [banner](../../includes/banner.md)]

In diesem Artikel wird beschrieben, wie Intercompany-Bestellungen, Aufträge, Rücklieferungen, Kaufverträge und Verkaufsverträge erstellt und aktualisiert werden.

## <a name="about-intercompany-orders"></a>Info über Intercompany-Aufträge

Beim Erstellen eines Intercompany-Auftrags erstellt Microsoft Dynamics 365 Supply Chain Management automatisch eine entsprechende Bestellung. Analog löst das Erstellen einer Intercompany-Bestellung die automatische Erstellung eines entsprechenden Intercompany-Auftrags aus.

Dies gilt für zweibeinige Aufträge (Buchungen zwischen zwei verbundenen Unternehmen) und für die meisten dreibeinigen Unternehmen (wenn eine innerbetriebliche Buchung mit einem Auftrag für einen externen Debitor entsteht).

## <a name="intercompany-order-example"></a>Beispiel für Intercompany-Aufträge

Es sind zwei verbundene Unternehmen vorhanden. Unternehmen A ist eine Vertriebs-Tochtergesellschaft, Unternehmen B eine Distributionseinheit. Intercompany-Aufträge und -Bestellungen werden in den folgenden Szenarien automatisch erstellt:

- Wenn Unternehmen A eine Bestellung erstellt und Unternehmen B der Kreditor ist, wird in Unternehmen B automatisch ein Intercompany-Auftrag erstellt. Die zweibeinige Auftragskette besteht aus einer Bestellung in Unternehmen A und einem Intercompany-Auftrag in Unternehmen B.
- Wenn Unternehmen B einen Auftrag erstellt und Unternehmen A der Debitor ist, wird in Unternehmen A automatisch ein Intercompany-Auftrag erstellt. Die zweibeinige Auftragskette besteht aus einer Bestellung in Unternehmen B und einer Intercompany-Bestellung in Unternehmen A.
- Wenn Unternehmen A zuerst einen Auftrag für einen externen Debitor erstellt, kann in Unternehmen A automatisch eine Bestellung erstellt werden. Dies löst wiederum die automatische Erstellung eines Intercompany-Auftrags in Unternehmen B aus. Die dreibeinige Auftragskette besteht aus einem Auftrag und einer Bestellung in Unternehmen A und einem Intercompany-Auftrag in Unternehmen B.

## <a name="about-intercompany-return-orders"></a>Info über Intercompany-Rücklieferungen

Intercompany-Artikel können auf die gleiche Weise zurückgeliefert werden wie normale Artikel. Allerdings wird bei der Rücklieferung von Intercompany-Artikeln durch den externen Debitor eine Intercompany-Bestellung angelegt, Dies führt wiederum automatisch zur Erstellung einer Rücklieferung für einen Intercompany-Auftrag. Ein Intercompany-Artikel kann auch ohne eine externe Debitorenrücklieferung zurückgeliefert werden.

Intercompany-Rücklieferungen werden genau wie reguläre Rücklieferungen auf der Seite **Rücklieferung erstellen** initiiert.

In Microsoft Dynamics 365 Supply Chain Management werden Intercompany-Aufträgen und Kaufverträge automatisch aktualisiert, um einen zurückgelieferten Artikels widerzuspiegeln. Die Auftrags- oder Kaufvertragszusage für diesen Artikel wird automatisch angepasst, um die Änderung in der Menge oder im Betrag widerzuspiegeln, wenn ein Artikel zurückgegeben wird.

## <a name="intercompany-return-order-example"></a>Beispiel für Intercompany-Rücklieferung

Unternehmen A erstellt eine Bestellung, die mit einem Kaufvertrag für einen Intercompany-Artikel verknüpft ist. Ein Intercompany-Auftrag, der mit dem entsprechenden Kaufvertrag verknüpft ist, wird in Unternehmen B automatisch erstellt. Der Rahmenbestellung und der Kaufvertrag werden als Intercompany-Vereinbarungen zugeordnet.

Unternehmen A gibt den Intercompany-Artikel an Unternehmen B zu. Unternehmen B erstellt den Rücklieferungsauftrag für den Artikel, und eine Einkaufsrücklieferung wird in Unternehmen A automatisch erstellt. Die Zusagen zum Kaufvertrag und der Rahmenbestellung, die mit den ursprünglichen Aufträgen verknüpft sind, werden automatisch angepasst, um die Änderung in der Menge oder im Betrag widerzuspiegeln.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
