---
title: Sie können eine Sendung nicht bestätigen, weil die Menge gleich Null ist
description: Sie können eine Sendung nicht bestätigen, weil die Menge gleich Null ist
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: b2f9f8deaca30e318d0393fb1d7911eebf63060ccca83dc6f1de9b04b9e30e11
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712885"
---
# <a name="you-cant-confirm-a-shipment-because-there-is-zero-quantity"></a>Sie können eine Sendung nicht bestätigen, weil die Menge gleich Null ist

Fehlercode: LoadLineWarningUpdatedToZero

## <a name="symptoms"></a>Symptome

Wenn Sie versuchen, eine Sendung zu bestätigen, zeigt das System die folgende Fehlermeldung an:

> Die Auslastungsposition für Artikel „%1“ und Lieferung „%2“ wurde auf die Menge „Null“ aktualisiert, da die Einstellungen für Unterlieferung keine Liefermengen für diesen Artikel zulassen.

Daher können Sie die Sendung für die Ladung nicht bestätigen.

## <a name="cause"></a>Ursache

Das System wertet aus, ob die entnommene Menge innerhalb der erwarteten Grenzen liegt, basierend auf der entnommenen Menge, der Menge der Ladung in der Zeile und dem Prozentsatz der Unterlieferung. Wenn das System feststellt, dass die entnommene Menge in der Zeile mit der Ladung 0 (Null) ist, können Sie die Sendung nicht bestätigen. Dieses Problem könnte z. B. auftreten, wenn Arbeit storniert wurde und der Prozentsatz der Unterlieferung auf der Ladung 100 Prozent beträgt.

## <a name="resolution"></a>Lösung

Überprüfen Sie Ihre Zeilen für die Ladung, um sicherzustellen, dass der Prozentsatz der Unterlieferung und die Mengen mit der entnommenen Arbeit übereinstimmen.

1. Gehen Sie zu **Lagerortverwaltung \> Ladungen \> Alle Ladungen**.
1. Wählen Sie die Ladung, für die die Sendung nicht bestätigt werden kann.
1. Wählen Sie auf der Registerkarte **Ladezeilen** die Zeile für die Ladung des Elements aus, das den Prozentsatz der Unterlieferung überschreitet.
1. Passen Sie den Wert des Feldes **Unterlieferung** oder des Feldes **Menge** nach Bedarf an.

> [!TIP]
> Wenn das Problem immer noch nicht behoben ist, müssen Sie möglicherweise weitere Entnahmearbeiten für die zugehörigen Verkaufsaufträge oder Umlagerungsaufträge durchführen, bis die verfügbare Menge mit der Ladung oder dem Versand abgeglichen ist.
