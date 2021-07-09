---
title: Menge überschreitet Unterlieferungsprozentsatz bei Lieferscheinerstellung
description: Wenn Sie einen Lieferschein erzeugen, enthält die ausgehende Ladung eine Menge, die den Unterlieferungsprozentsatz überschreitet.
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSSalesPackingSlipPost,WHSLoadPlanningListPage_WHSSalesPackingSlipPost,WHSLoadPlanningWorkbench_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: ecdd377d12faf40f64736e93671dcf42ff132403
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249104"
---
# <a name="quantity-exceeds-under-delivery-percentage-during-packing-slip-generation"></a>Menge überschreitet Unterlieferungsprozentsatz bei Lieferscheinerstellung

Fehlercode: SYS24921

## <a name="symptoms"></a>Symptome

Wenn Sie einen Lieferschein erzeugen, enthält die ausgehende Ladung eine Menge, die den Unterlieferungsprozentsatz überschreitet.

Wenn Sie versuchen, einen Lieferschein zu generieren, zeigt das System die folgende Fehlermeldung an:

> Unterlieferung von Position ist %1 Prozent, doch die erlaubte Unterlieferung beträgt nur %2 Prozent.

Daher können Sie den Lieferschein für die Ladung nicht generieren.

## <a name="cause"></a>Ursache

Die kommissionierte Menge für die Ladung oder Sendung ist kleiner als die bestellte Menge und liegt nicht im Bereich des Unterlieferungsprozentsatzes.

## <a name="resolution"></a>Lösung

Die Ladung oder Sendung befindet sich derzeit in einem Status, in dem die Lieferscheinerstellung fehlschlägt. Um dieses Problem zu beheben, führen Sie eine der folgenden Aufgaben aus:

- Passen Sie den Unterlieferungsprozentsatz an.
- Stornieren Sie und nehmen Sie Anpassungen vor.

### <a name="adjust-the-under-delivery-percentage"></a>Anpassen des Unterlieferungsprozentsatzes

Gehen Sie wie folgt vor, um den Unterlieferungsprozentsatz anzupassen.

1. Gehen Sie zu **Debitoren \> Aufträge \> Alle Aufträge**.
1. Wählen Sie den Verkaufsauftrag aus, für den Sie keinen Lieferschein für die Ladung buchen können.
1. Wählen Sie auf der Registerkarte  **Kundenauftragszeilen** die Kundenauftragszeile für das Element, das den Unterlieferungsprozentsatz überschreitet.
1. Auf der Registerkarte  **Zeilendetails** wählen Sie **Lieferung**.
1. Legen Sie das Feld **Unterlieferung** auf einen größeren Prozentsatz fest, der die kommissionierte Menge gegen die Ladungsmenge aufwiegt, so dass die Lieferscheinerstellung fortgesetzt werden kann.

### <a name="reverse-and-make-adjustments"></a>Stornieren und Anpassungen vornehmen

Stornieren Sie alles, was für die Ladung gebucht wurde (z. B. den Lieferschein, die Versandbestätigung und die Arbeit), nehmen Sie Anpassungen am Verkaufsauftrag vor, geben Sie den Auftrag erneut für das Lagerort frei und schließen Sie den Versandvorgang ab.

Gehen Sie wie folgt vor, um einen Lieferschein zu stornieren.

1. Gehen Sie zu **Lagerortverwaltung \> Ladungen \> Alle Ladungen**.
1. Wählen Sie im Aktionsbereich auf der Registerkarte **Versand und Empfang** in der Gruppe **Stornieren** die Option **Lieferscheine stornieren**.

Gehen Sie wie folgt vor, um eine Versandbestätigung zu stornieren.

1. Gehen Sie zu **Lagerortverwaltung \> Ladungen \> Alle Ladungen**.
1. Wählen Sie im Aktionsbereich auf der Registerkarte **Versand und Empfang** in der Gruppe **Stornieren** die Option **Sendungsbestätigung stornieren**.

Gehen Sie wie folgt vor, um Arbeiten zu stornieren.

1. Gehen Sie zu **Lagerortverwaltung \> Ladungen \> Alle Ladungen**.
1. Wählen Sie im Aktionsbereich auf der Registerkarte **Ladungen** in der Gruppe **Arbeit** die Option **Arbeit stornieren**.
