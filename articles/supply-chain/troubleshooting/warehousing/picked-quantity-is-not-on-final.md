---
title: Sie können eine Sendung nicht bestätigen, weil Elemente nicht entnommen worden sind
description: Sie können eine Sendung nicht bestätigen, weil Elemente nicht entnommen worden sind
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
ms.openlocfilehash: 23a517e7769dc86ebec30e4f17c62172a6ad8801
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938476"
---
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a>Sie können eine Sendung nicht bestätigen, weil Elemente nicht entnommen worden sind

Fehlercode: LoadNotPickedAndMovedToFinalShippingLocation

## <a name="symptoms"></a>Symptome

Wenn Sie versuchen, eine Sendung zu bestätigen, zeigt das System die folgende Fehlermeldung an:

> Einige der Artikel, die für Ladung %1 benötigt werden, sind noch nicht entnommen und zum endgültigen Versandort verschoben worden.

Daher können Sie die Sendung für die Ladung nicht bestätigen.

## <a name="cause"></a>Ursache

Die Ladung oder Sendung kann in ihrem aktuellen Status nicht bestätigt werden, weil eine der folgenden Bedingungen vorliegen könnte:

- Die zugehörige Arbeit wurde noch nicht entnommen und an den endgültigen Versandort gebracht.
- Die entnommene Arbeitsmenge stimmt nicht mit der erstellten Arbeitsmenge in der Ladung überein.

## <a name="resolution"></a>Lösung

Prüfen Sie die zugehörigen Verkaufsaufträge oder Umlagerungsaufträge für die Ladung oder den Transport. Stellen Sie sicher, dass alle zugehörigen Arbeiten am endgültigen Versandort abgeschlossen sind und dass die Mengen übereinstimmen.

1. Gehen Sie zu **Lagerortverwaltung \> Ladungen \> Alle Ladungen**.
1. Wählen Sie die Ladung, für die die Sendung nicht bestätigt werden kann.
1. Wählen Sie auf der Registerkarte **Ladezeilen** Inforegister die Zeile für die Ladung aus.
1. Notieren Sie sich den Wert des Feldes **Werk erstellte Menge**.
1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Ladungen** in der Gruppe **Zugehörige Informationen** die Option **Arbeit**.
1. Überprüfen Sie, ob die Arbeit am endgültigen Versandort abgeschlossen wurde und ob die entnommene Arbeitsmenge mit der erstellten Arbeitsmenge in der Ladung übereinstimmt.
1. Wiederholen Sie diesen Vorgang für alle Ladungs-Zeilen, um sicherzustellen, dass alle Kriterien erfüllt sind.
