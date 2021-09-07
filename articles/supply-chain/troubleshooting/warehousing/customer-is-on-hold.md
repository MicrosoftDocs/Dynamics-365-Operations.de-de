---
title: Eine Lieferung kann nicht bestätigt werden, weil der Debitor gesperrt ist
description: Eine Lieferung kann nicht bestätigt werden, weil der Debitor gesperrt ist.
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
ms.openlocfilehash: 801778fc8f04b106bf168a3dcd5a89767a837740
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344263"
---
# <a name="you-cant-confirm-a-shipment-because-the-customer-is-on-hold"></a>Eine Lieferung kann nicht bestätigt werden, weil der Debitor gesperrt ist

Fehlercode: WAX:CustomerOnHoldShipmentCannotBeConfirmed

## <a name="symptoms"></a>Symptome

Wenn Sie versuchen, eine Sendung zu bestätigen, zeigt das System die folgende Fehlermeldung an:

> Lieferung %1 kann nicht bestätigt werden, da Debitor für %2 gesperrt ist.

Daher können Sie die Sendung für die Ladung nicht bestätigen.

## <a name="cause"></a>Ursache

Das Debitorenkonto der Ladung oder Lieferung wird gesperrt. Daher verhindert der Status des Debitors eine Versandbestätigung.

## <a name="resolution"></a>Lösung

Gehen Sie wie folgt vor, um das Debitorenkonto zu entsperren.

1. Gehen Sie zu **Debitorenkonten \> Debitoren \> Alle Debitoren**.
1. Öffnen Sie das Debitorenkonto, für das die Lieferung nicht bestätigt werden kann.
1. Legen Sie auf dem Inforegister **Kredit und Inkasso** das Feld **Rechnungsstellung und Lieferung gesperrt** auf *Nein* fest.
1. Wiederholen Sie diesen Vorgang für alle gesperrten Debitoren für die Ladung.
