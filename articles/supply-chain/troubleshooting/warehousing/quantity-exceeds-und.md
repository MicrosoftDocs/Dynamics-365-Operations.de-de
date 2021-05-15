---
title: Sie können eine Sendung nicht bestätigen, weil die Menge den Prozentsatz für die Unterlieferung überschreitet
description: Sie können eine Sendung nicht bestätigen, weil die Menge den Prozentsatz für die Unterlieferung überschreitet
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
ms.openlocfilehash: 5339b9d800f7454e2a00c230a8d5deca3979c074
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938474"
---
# <a name="you-cant-confirm-a-shipment-because-the-quantity-exceeds-the-underdelivery-percentage"></a>Sie können eine Sendung nicht bestätigen, weil die Menge den Prozentsatz für die Unterlieferung überschreitet

Fehlercode: WAX1687

## <a name="symptoms"></a>Symptome

Wenn Sie versuchen, eine Sendung zu bestätigen, zeigt das System die folgende Fehlermeldung an:

> Die Lieferung für Ladung %1 konnte nicht bestätigt werden, weil die Menge für Element %2 den Prozentsatz überschreitet, der für Unterlieferung definiert ist.

Daher können Sie die Sendung für die Ladung nicht bestätigen.

## <a name="cause"></a>Ursache

Die Menge der Ladung oder Sendung wurde nur teilweise entnommen. Die Menge ist derzeit um einen Prozentsatz geringer als die entnommene Menge, der außerhalb des zulässigen Prozentsatzes für die Unterlieferung liegt.

## <a name="resolution"></a>Lösung

Um dieses Problem zu beheben, führen Sie eine der folgenden Aufgaben aus:

- Legen Sie die Menge der Ladung in der Zeile fest.
- Legen Sie den Prozentsatz für die Unterlieferung fest.

### <a name="set-the-load-line-quantity"></a>Die Menge der Ladung der Zeile festlegen

Um die Menge für die Ladung festzulegen, folgen Sie diesen Schritten.

1. Gehen Sie zu **Lagerortverwaltung \> Ladungen \> Alle Ladungen**.
1. Wählen Sie die Ladung, für die die Sendung nicht bestätigt werden kann.
1. Wählen Sie auf der Registerkarte **Ladezeilen** die Zeile für die Ladung des Elements aus, das den Prozentsatz der Unterlieferung überschreitet.
1. Wählen Sie auf der Registerkarte **Zeilendetails** Inforegister **Auftrag**.
1. Legen Sie im Feld **Menge** den Wert auf die entnommene Menge fest (d.h. auf den Wert **Werk erstellte Menge**), damit die Versandbestätigung erfolgen kann.

### <a name="set-the-underdelivery-percentage"></a>Den Prozentsatz der Unterlieferung festlegen

Um den Prozentsatz der Unterlieferung festzulegen, führen Sie diese Schritte aus.

1. Gehen Sie zu **Lagerortverwaltung \> Ladungen \> Alle Ladungen**.
1. Wählen Sie die Ladung, für die die Sendung nicht bestätigt werden kann.
1. Wählen Sie auf der Registerkarte **Ladezeilen** die Zeile für die Ladung des Elements aus, das den Prozentsatz der Unterlieferung überschreitet.
1. Wählen Sie auf der Seite **Zeilendetails** Inforegister **Allgemein**.
1. Legen Sie im Feld **Unterlieferung** den Wert auf einen größeren Prozentsatz fest, der die entnommene Menge gegen die Ladungsmenge aufwiegt, damit eine Versandbestätigung erfolgen kann.
