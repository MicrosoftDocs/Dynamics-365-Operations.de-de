---
title: Die kommissionierte Menge ist bei der Lieferscheinerstellung nicht ausreichend
description: Wenn Sie einen Lieferschein generieren, enthält die ausgehende Ladung eine kommissionierte Menge, die nicht mit der erstellten Arbeitsmenge auf der Ladelinie übereinstimmt.
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
ms.openlocfilehash: fa6054dc26e4306ec16e37b0e6c320342ed40fe0
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249108"
---
# <a name="picked-quantity-isnt-sufficient-during-packing-slip-generation"></a>Die kommissionierte Menge ist bei der Lieferscheinerstellung nicht ausreichend

Fehlercode: SYS54073

## <a name="symptoms"></a>Symptome

Wenn Sie einen Lieferschein generieren, enthält die ausgehende Ladung eine kommissionierte Menge, die nicht mit der erstellten Arbeitsmenge auf der Ladelinie übereinstimmt.

Wenn Sie versuchen, einen Lieferschein zu generieren, zeigt das System die folgende Fehlermeldung an:

> Da %1 entnommen wurden, ist es nicht ausreichend, %2 zu aktualisieren, wenn der Rest anschließend %3 sein muss.

Daher können Sie den Lieferschein für die Ladung nicht generieren.

## <a name="cause"></a>Ursache

Der Lieferschein kann in seinem aktuellen Status nicht generiert werden, weil eine der folgenden Bedingungen vorliegen könnte:

- Die zugehörige Arbeit wurde noch nicht entnommen und an den endgültigen Versandort gebracht.
- Die entnommene Arbeitsmenge stimmt nicht mit der erstellten Arbeitsmenge in der Ladung überein.
- Die Menge der Ladelinie, die erstellte Arbeitsmenge und die kommissionierte Menge stimmen nicht überein.

## <a name="resolution"></a>Lösung

Die Ladung oder Sendung befindet sich derzeit in einem Status, in dem die Lieferscheinerstellung fehlschlägt. Um dieses Problem zu beheben, führen Sie eine der folgenden Aufgaben aus:

- Überprüfen Sie Ihre Ladungszeilen und stellen Sie sicher, dass alle zugehörigen Arbeiten am endgültigen Versandort abgeschlossen wurden und dass die Mengen übereinstimmen.
- Passen Sie die Menge für die Ladung an.
- Stornieren Sie alle Kommissionierregistrierungen und führen Sie die Kommissionierung erneut durch.

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>Überprüfen Sie Ihre Ladungszeilen und stellen Sie sicher, dass alle zugehörigen Arbeiten am endgültigen Versandort abgeschlossen sind und dass die Mengen übereinstimmen.

Gehen Sie wie folgt vor, um Ihre Ladungszeilen zu überprüfen und sicherzustellen, dass alle zugehörigen Arbeiten am endgültigen Versandort abgeschlossen wurden und dass die Mengen übereinstimmen.

1. Gehen Sie zu **Lagerortverwaltung \> Ladungen \> Alle Ladungen**.
1. Wählen Sie die Ladung aus, für die der Lieferschein nicht generiert werden kann.
1. Wählen Sie auf der Registerkarte **Ladezeilen** Inforegister die Zeile für die Ladung aus.
1. Notieren Sie sich den Wert des Feldes **Werk erstellte Menge**.
1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Ladungen** in der Gruppe **Zugehörige Informationen** die Option **Arbeit**.
1. Überprüfen Sie, ob die Arbeit am endgültigen Versandort abgeschlossen wurde und ob die entnommene Arbeitsmenge mit der erstellten Arbeitsmenge in der Ladung übereinstimmt.
1. Wiederholen Sie diesen Vorgang für alle Ladungs-Zeilen, um sicherzustellen, dass alle Kriterien erfüllt sind.

### <a name="adjust-the-load-line-quantity"></a>Justieren Sie die Menge der Ladung in der Zeile

Gehen Sie wie folgt vor, um die Menge der Ladung in der Zeile anzupassen.

1. Gehen Sie zu **Lagerortverwaltung \> Ladungen \> Alle Ladungen**.
1. Wählen Sie die Ladung aus, für die der Lieferschein nicht generiert werden kann.
1. Wählen Sie im Aktionsbereich auf der Registerkarte **Versand und Empfang** in der Gruppe **Stornieren** die Option **Sendungsbestätigung stornieren**.
1. Wählen Sie auf der Registerkarte **Ladungszeilen** die Ladung des Elements, das ein Problem verursacht.
1. Wählen Sie **Reduzieren Sie die kommissionierte Menge**, um die kommissionierte Menge anzupassen.
1. Legen Sie das Feld **Ladung reduzieren** fest, um Anpassungen an der Ladung zu reflektieren.

### <a name="reverse-all-pick-registrations-and-redo-picking"></a>Stornieren Sie alle Kommissionierregistrierungen und wiederholen Sie die Kommissionierung.

Das Problem kann auftreten, weil jemand die Kommissionierregistrierung verwendet hat, um eine Ladung ohne Arbeit zu schließen. In diesem Fall muss die manuelle Kommissionierregistrierung rückgängig gemacht werden, und die Kommissionierung muss dann mit der Warehouse Management Mobile-App abgeschlossen werden.

Gehen Sie wie folgt vor, um die Kommissionierregistrierung rückgängig zu machen.

1. Gehen Sie zu **Debitoren \> Aufträge \> Alle Aufträge**.
1. Wählen Sie den Verkaufsauftrag aus, für den Sie keinen Lieferschein für die Ladung buchen können.
1. Wählen Sie auf der Registerkarte  **Verkaufsauftragszeilen** die Zeile des Verkaufsauftrags, für den die Kommissionierregistrierung durchgeführt wurde.
1. Wählen Sie **Zeile \> Kommissionierung rückgängig machen**, um die Entnahme rückgängig zu machen.
