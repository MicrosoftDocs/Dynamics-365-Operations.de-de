---
title: Die Menge, die Sie zu aktualisieren versuchen, übersteigt die empfangene/gelieferte Menge.
description: Wenn Sie einen Lieferschein erzeugen, enthält die ausgehende Ladung eine Menge, die die für den Arbeitsauftrag kommissionierte und reservierte Arbeitsmenge übersteigt.
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
ms.openlocfilehash: 66d9cd80cc61e00d1d88ab4f59d03054d746cdd9
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249109"
---
# <a name="quantity-that-youre-trying-to-update-exceeds-the-receiveddelivered-quantity"></a>Die Menge, die Sie zu aktualisieren versuchen, übersteigt die empfangene/gelieferte Menge

Fehlercode: SYS7676

## <a name="symptoms"></a>Symptome

Wenn Sie einen Lieferschein erzeugen, enthält die ausgehende Ladung eine Menge, die die für den Arbeitsauftrag kommissionierte und reservierte Arbeitsmenge übersteigt.

Wenn Sie versuchen, einen Lieferschein zu generieren, zeigt das System die folgende Fehlermeldung an:

> Physische Restmenge und Gesamtmenge müssen dasselbe Vorzeichen haben.

Daher können Sie den Lieferschein für die Ladung nicht generieren.

## <a name="cause"></a>Ursache

Die entnommene Arbeitsmenge stimmt nicht mit der erstellten Arbeitsmenge in der Ladung überein. Dieses Problem kann z. B. auftreten, wenn die Menge der Ladungszeile, der erstellten Arbeit oder der kommissionierten Menge nicht korrekt ist.

## <a name="resolution"></a>Lösung

Die Ladung oder Sendung befindet sich derzeit in einem Status, in dem die Lieferscheinerstellung fehlschlägt. Um dieses Problem zu beheben, führen Sie eine der folgenden Aufgaben aus:

- Überprüfen Sie Ihre Ladungszeilen und stellen Sie sicher, dass alle zugehörigen Arbeiten am endgültigen Versandort abgeschlossen wurden und dass die Mengen übereinstimmen.
- Passen Sie die Menge für die Ladung an.
- Stornieren Sie alle Kommissionierregistrierungen und führen Sie die Kommissionierung erneut durch.

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>Überprüfen Sie Ihre Ladungszeilen und stellen Sie sicher, dass alle zugehörigen Arbeiten am endgültigen Versandort abgeschlossen sind und dass die Mengen übereinstimmen.

Gehen Sie wie folgt vor, um Ihre Ladungszeilen zu überprüfen und sicherzustellen, dass alle zugehörigen Arbeiten am endgültigen Versandort abgeschlossen wurden und dass die Mengen übereinstimmen.

1. Gehen Sie zu **Lagerortverwaltung \> Ladungen \> Alle Ladungen**.
1. Wählen Sie die Ladung aus, für die die Sendung nicht erstellt werden kann.
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

Wenn jemand die Kommissionierregistrierung verwendet hat, um eine Ladung ohne Arbeit zu schließen, kann eine Diskrepanz zwischen der Ladelinienmenge und der kommissionierten Menge auftreten. In diesem Fall muss die manuelle Kommissionierregistrierung rückgängig gemacht werden, und die Kommissionierung muss dann mit der Warehouse Management Mobile-App abgeschlossen werden.

Gehen Sie wie folgt vor, um die Kommissionierregistrierung rückgängig zu machen.

1. Gehen Sie zu **Debitoren \> Aufträge \> Alle Aufträge**.
1. Wählen Sie den Verkaufsauftrag aus, für den Sie keinen Lieferschein für die Ladung buchen können.
1. Wählen Sie auf der Registerkarte  **Verkaufsauftragszeilen** die Zeile des Verkaufsauftrags, für den die Kommissionierregistrierung durchgeführt wurde.
1. Wählen Sie **Zeile \> Kommissionierung rückgängig machen**, um die Entnahme rückgängig zu machen.
