---
title: Eine Lieferung kann nicht bestätigt werden, weil Ladungspositionen keine Menge haben
description: Eine Lieferung kann nicht bestätigt werden, weil Ladungspositionen keine Menge haben.
author: GalynaFedorova
ms.date: 07/30/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 15aa7f5e72ff8f2c027b5b020a23328978aa02b0
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344233"
---
# <a name="you-cant-confirm-a-shipment-because-load-lines-have-zero-quantity"></a>Eine Lieferung kann nicht bestätigt werden, weil Ladungspositionen keine Menge haben

Fehlercode: WAX:LoadTableWarningAllLinesZero, WAX2543

## <a name="symptoms"></a>Symptome

Wenn Sie versuchen, eine Sendung zu bestätigen, zeigt das System die folgende Fehlermeldung an:

> Alle Positionen in Auslastung „%1“ haben die Menge „Null“.  
> Die Lieferung für Ladung "%1" konnte nicht bestätigt werden.

Daher können Sie die Sendung für die Ladung nicht bestätigen.

## <a name="cause"></a>Ursache

Das System beurteilt anhand der angelegten Arbeitskennung, der Ladungspositionsmenge und des Prozentsatzes für die Unterlieferung aus, ob die Ladungsposition für den Versand bestätigt werden kann. Wenn das System feststellt, dass keine Arbeitskennungen vorhanden sind und der Prozentsatz für die Unterlieferung auf 100 % gesetzt ist, können Sie die Lieferung nicht bestätigen.

Dieses Problem könnte z. B. auftreten, wenn die Arbeit storniert wurde und der Prozentsatz der Unterlieferung auf der Ladungsposition 100 % beträgt.

## <a name="resolution"></a>Lösung

Die Ladung oder Sendung befindet sich derzeit in einem Status, in dem die Versandbestätigung fehlschlägt. Um dieses Problem zu beheben, führen Sie eine der folgenden Aufgaben aus:

- Überprüfen Sie Ihre Ladungspositionen und stellen Sie sicher, dass alle zugehörigen Arbeiten am endgültigen Versandort abgeschlossen wurden und die Mengen übereinstimmen.
- Überprüfen Sie Ihre Ladungspositionen, um sicherzustellen, dass der Prozentsatz der Unterlieferung und die Mengen mit der entnommenen Arbeit übereinstimmen.

### <a name="review-your-load-lines-to-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>Überprüfen Sie Ihre Ladungspositionen und stellen Sie sicher, dass alle zugehörigen Arbeiten am endgültigen Versandort abgeschlossen wurden und die Mengen übereinstimmen

Gehen Sie wie folgt vor, um Ihre Ladungspositionen zu überprüfen und sicherzustellen, dass alle zugehörigen Arbeiten am endgültigen Versandort abgeschlossen wurden und dass die Mengen übereinstimmen.

1. Gehen Sie zu **Lagerortverwaltung \> Ladungen \> Alle Ladungen**.
1. Öffnen Sie die Ladung, für die die Lieferung nicht bestätigt werden kann.
1. Wählen Sie auf der Registerkarte **Ladezeilen** Inforegister die Zeile für die Ladung aus.
1. Notieren Sie sich den Wert des Feldes **Werk erstellte Menge**.
1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Ladungen** in der Gruppe **Zugehörige Informationen** die Option **Arbeit**.
1. Überprüfen Sie, ob die Arbeit am endgültigen Versandort abgeschlossen wurde und ob die entnommene Arbeitsmenge mit der erstellten Arbeitsmenge in der Ladung übereinstimmt.
1. Wenn Sie eine Diskrepanz feststellen, brechen Sie die entsprechende Arbeit ab, konfigurieren Sie die Lagerplatzrichtlinie neu und geben Sie die Ladung erneut frei. Weitere Anweisungen finden Sie unter [Eine Lieferung kann nicht bestätigt werden, weil Artikel nicht kommissioniert wurden](picked-quantity-is-not-on-final.md).
1. Wiederholen Sie diesen Vorgang für alle Ladungs-Zeilen, um sicherzustellen, dass alle Kriterien erfüllt sind.

### <a name="review-your-load-lines-to-make-sure-that-the-underdelivery-percentage-and-quantities-are-aligned-with-the-picked-work"></a>Überprüfen Sie Ihre Ladungspositionen, um sicherzustellen, dass der Prozentsatz der Unterlieferung und die Mengen mit der entnommenen Arbeit übereinstimmen

Gehen Sie wie folgt vor, um Ihre Ladungspositionen zu überprüfen, um sicherzustellen, dass der Prozentsatz der Unterlieferung und die Mengen mit der entnommenen Arbeit übereinstimmen.

1. Gehen Sie zu **Lagerortverwaltung \> Ladungen \> Alle Ladungen**.
1. Öffnen Sie die Ladung, für die die Lieferung nicht bestätigt werden kann.
1. Wählen Sie auf der Registerkarte **Ladezeilen** die Zeile für die Ladung des Elements aus, das den Prozentsatz der Unterlieferung überschreitet.
1. Passen Sie den Wert des Feldes **Unterlieferung** oder des Feldes **Menge** nach Bedarf an.

> [!TIP]
> Wenn das Problem immer noch nicht behoben ist, müssen Sie möglicherweise weitere Entnahmearbeiten für die zugehörigen Verkaufsaufträge oder Umlagerungsaufträge durchführen, bis die verfügbare Menge mit der Ladung oder dem Versand abgeglichen ist.
