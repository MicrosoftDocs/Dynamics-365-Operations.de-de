---
title: Menge überschreitet Überlieferungsprozentsatz bei Lieferscheinerstellung
description: Wenn Sie einen Lieferschein generieren, enthält die ausgehende Ladung eine Menge, die den Überlieferungsprozentsatz überschreitet.
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
ms.openlocfilehash: bc74c5748950b1f0f001fd89acb2e023640065ee
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920049"
---
# <a name="quantity-exceeds-over-delivery-percentage-during-packing-slip-generation"></a>Menge überschreitet Überlieferungsprozentsatz bei Lieferscheinerstellung

Fehlercode: SYS24920

## <a name="symptoms"></a>Symptome

Wenn Sie einen Lieferschein generieren, enthält die ausgehende Ladung eine Menge, die den Überlieferungsprozentsatz überschreitet.

Wenn Sie versuchen, einen Lieferschein zu generieren, zeigt das System die folgende Fehlermeldung an:

> Überlieferung von Position ist %1 Prozent, doch die erlaubte Überlieferung beträgt nur %2 Prozent.

Daher können Sie den Lieferschein für die Ladung nicht generieren.

## <a name="cause"></a>Ursache

Die kommissionierte Menge für die Ladung oder den Transport ist größer als die bestellte Menge und liegt nicht im Bereich der Überlieferungsquote.

## <a name="resolution"></a>Lösung

Die Ladung oder Sendung befindet sich derzeit in einem Status, in dem die Lieferscheinerstellung fehlschlägt. Um dieses Problem zu beheben, führen Sie eine der folgenden Aufgaben aus:

- Passen Sie die Menge für die Ladung an.
- Passen Sie den Überlieferungsprozentsatz an.
- Stornieren Sie und nehmen Sie Anpassungen vor.

### <a name="adjust-the-load-line-quantity"></a>Justieren Sie die Menge der Ladung in der Zeile

Gehen Sie wie folgt vor, um die Menge der Ladung in der Zeile anzupassen.

1. Gehen Sie zu **Lagerortverwaltung \> Ladungen \> Alle Ladungen**.
1. Wählen Sie die Ladung aus, für die der Lieferschein nicht generiert werden kann.
1. Wählen Sie im Aktionsbereich auf der Registerkarte **Versand und Empfang** in der Gruppe **Stornieren** die Option **Sendungsbestätigung stornieren**.
1. Wählen Sie auf der Registerkarte **Ladungszeilen** die Zeile für die Ladung des Elements aus, das den Prozentsatz für die Überlieferung überschreitet.
1. Wählen Sie **Reduzieren Sie die kommissionierte Menge**, um die kommissionierte Menge anzupassen.
1. Auf der Registerkarte **Zeilendetails** wählen Sie **Auftrag**.
1. Legen Sie das Feld **Menge** auf die kommissionierte Menge fest (d. h. den Wert des Feldes **Werk erstellte Menge**), damit die Erstellung des Lieferscheins fortgesetzt werden kann.

### <a name="adjust-the-over-delivery-percentage"></a>Anpassen des Überlieferungsprozentsatzes

Gehen Sie wie folgt vor, um den Überlieferungsprozentsatz anzupassen.

1. Gehen Sie zu **Debitoren \> Aufträge \> Alle Aufträge**.
1. Wählen Sie den Verkaufsauftrag aus, für den Sie keinen Lieferschein für die Ladung buchen können.
1. Wählen Sie auf der Registerkarte **Kundenauftragszeilen** die Verkaufsauftragszeile für das Element aus, das den Überlieferungsprozentsatz überschreitet.
1. Auf der Registerkarte **Zeilendetails** wählen Sie **Lieferung**.
1. Legen Sie das Feld **Überlieferung** auf einen größeren Prozentsatz fest, der die kommissionierte Menge gegen die Ladungsmenge aufwiegt, so dass die Lieferscheinerstellung fortgesetzt werden kann.

### <a name="reverse-and-make-adjustments"></a>Stornieren und Anpassungen vornehmen

Stornieren Sie alles, was für die Ladung gebucht wurde (z. B. den Lieferschein, die Versandbestätigung und die Arbeit), nehmen Sie Anpassungen am Verkaufsauftrag vor, geben Sie den Auftrag erneut für das Lagerort frei und schließen Sie den Versandvorgang ab.

Gehen Sie wie folgt vor, um einen Lieferschein zu stornieren.

1. Gehen Sie zu **Lagerortverwaltung \> Ladungen \> Alle Ladungen**.
1. Wählen Sie im Aktionsbereich auf der Registerkarte **Versand und Empfang** in der Gruppe **Umkehren** die Option **Lieferscheine stornieren**.

Gehen Sie wie folgt vor, um eine Versandbestätigung zu stornieren.

1. Gehen Sie zu **Lagerortverwaltung \> Ladungen \> Alle Ladungen**.
1. Wählen Sie im Aktionsbereich auf der Registerkarte **Versand und Empfang** in der Gruppe **Stornieren** die Option **Sendungsbestätigung stornieren**.

Gehen Sie wie folgt vor, um Arbeiten zu stornieren.

1. Gehen Sie zu **Lagerortverwaltung \> Ladungen \> Alle Ladungen**.
1. Im Aktionsbereich, auf der Registerkarte **Ladungen**, wählen Sie in der Gruppe **Arbeit** die Option **Arbeit umkehren**.
