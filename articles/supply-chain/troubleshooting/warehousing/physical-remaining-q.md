---
title: Physikalische Restmenge in der Einheit darf nicht Null sein
description: Wenn Sie einen Lieferschein erzeugen, haben die Daten, die ihm zugeführt werden, eine Bestandsmenge ungleich Null, aber eine Verkaufsmenge von Null.
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningListPage_WHSSalesPackingSlipPost, WHSLoadTable_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d767fdce861ccb481a3fe289480a51a7534dc207
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920223"
---
# <a name="physical-remaining-quantity-in-the-unit-must-not-be-zero"></a>Physikalische Restmenge in der Einheit darf nicht Null sein

Fehlercode: SYS19591

## <a name="symptoms"></a>Symptome

Wenn Sie einen Lieferschein erzeugen, haben die Daten, die ihm zugeführt werden, eine Bestandsmenge ungleich Null, aber eine Verkaufsmenge von Null.

Wenn Sie versuchen, den Lieferschein zu generieren, zeigt das System die folgende Fehlermeldung an:

> Physische Restmenge in Einheit '%1' darf nicht Null sein.

Daher können Sie den Lieferschein für die Ladung nicht generieren.

## <a name="cause"></a>Ursache

Das System wertet die physische Restmenge in der Einheit des Bestands und die physische Restmenge im Versandelement aus. Wenn das System feststellt, dass die physische Restmenge in der Versandeinheit 0 (Null) ist, die physische Restmenge in der Bestandseinheit aber nicht 0 ist, können Sie den Lieferschein nicht generieren. Dieses Problem kann z. B. auftreten, wenn die Verkaufseinheit und die Bestandseinheit für das Element unterschiedlich sind und die Umrechnung zwischen den Einheiten nicht korrekt ist.

## <a name="resolution"></a>Lösung

Die Ladung oder Sendung befindet sich derzeit in einem Status, in dem die Lieferscheinerstellung fehlschlägt. Um dieses Problem zu beheben, führen Sie eine der folgenden Aufgaben aus:

- Überprüfen Sie Ihre Ladungszeilen und stellen Sie sicher, dass alle zugehörigen Arbeiten am endgültigen Versandort abgeschlossen wurden und dass die Mengen übereinstimmen.
- Überprüfen Sie Ihre Ladungszeilen und nehmen Sie Anpassungen vor, um sicherzustellen, dass die Mengen sauber umgerechnet werden können, ohne dass Rundungsprobleme auftreten.
- Überprüfen Sie Ihre Ladungszeilen und nehmen Sie Anpassungen vor, um sicherzustellen, dass die Einheit und die Menge mit der Dezimalgenauigkeit der Einheit übereinstimmen.
- Stellen Sie sicher, dass die Maßeinheit des Bestands kleiner ist als die Maßeinheit des Verkaufs.

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>Überprüfen Sie Ihre Ladungszeilen und stellen Sie sicher, dass alle zugehörigen Arbeiten am endgültigen Versandort abgeschlossen sind und dass die Mengen übereinstimmen.

Gehen Sie wie folgt vor, um Ihre Ladungszeilen zu überprüfen und sicherzustellen, dass alle zugehörigen Arbeiten am endgültigen Versandort abgeschlossen wurden und dass die Mengen übereinstimmen.

1. Gehen Sie zu **Lagerortverwaltung \> Ladungen \> Alle Ladungen**.
1. Wählen Sie die Ladung, für die die Sendung nicht bestätigt werden kann.
1. Wählen Sie auf der Registerkarte **Ladezeilen** Inforegister die Zeile für die Ladung aus.
1. Notieren Sie sich den Wert des Feldes **Werk erstellte Menge**.
1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Ladungen** in der Gruppe **Zugehörige Informationen** die Option **Arbeit**.
1. Überprüfen Sie, ob die Arbeit am endgültigen Versandort abgeschlossen wurde und ob die entnommene Arbeitsmenge mit der erstellten Arbeitsmenge in der Ladung übereinstimmt.
1. Wiederholen Sie diesen Vorgang für alle Ladungs-Zeilen, um sicherzustellen, dass alle Kriterien erfüllt sind.

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-rounding-issues"></a>Überprüfen Sie Ihre Ladungszeilen und nehmen Sie Anpassungen vor, um sicherzustellen, dass die Menge sauber und ohne Rundungsprobleme umgerechnet werden kann

Gehen Sie wie folgt vor, um Ihre Ladungszeilen zu überprüfen und Anpassungen vorzunehmen, um sicherzustellen, dass die Menge sauber und ohne Rundungsprobleme umgerechnet werden kann.

1. Gehen Sie zu **Lagerortverwaltung \> Ladungen \> Alle Ladungen**.
1. Wählen Sie die Ladung aus, für die der Lieferschein nicht generiert werden kann.
1. Wählen Sie im Aktionsbereich auf der Registerkarte **Versand und Empfang** in der Gruppe **Stornieren** die Option **Sendungsbestätigung stornieren**.
1. Wählen Sie auf der Registerkarte **Ladungszeilen** die Ladung für das Element aus, das die Überlieferung überschreitet.
1. Wählen Sie **Reduzieren Sie die kommissionierte Menge**, um die kommissionierte Menge anzupassen.
1. Auf der Registerkarte **Zeilendetails** wählen Sie **Auftrag**.
1. Legen Sie das Feld **Menge** auf die kommissionierte Menge fest (d. h. den Wert des Feldes **Werk erstellte Menge**), damit die Erstellung des Lieferscheins fortgesetzt werden kann.

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-unit-and-quantity-are-aligned-with-the-decimal-precision-of-the-unit"></a>Überprüfen Sie Ihre Ladungszeilen und nehmen Sie Anpassungen vor, um sicherzustellen, dass die Einheit und die Menge mit der Dezimalgenauigkeit der Einheit übereinstimmen

Gehen Sie wie folgt vor, um Ihre Ladungszeilen zu überprüfen und Anpassungen vorzunehmen, um sicherzustellen, dass die Einheit und die Menge mit der Dezimalgenauigkeit der Einheit übereinstimmen.

1. Gehen Sie zu **Lagerortverwaltung \> Ladungen \> Alle Ladungen**.
1. Wählen Sie die Ladung aus, für die der Lieferschein nicht generiert werden kann.
1. Wählen Sie im Inforegister **Ladungszeilen** die Ladungszeile für das Element, das ein Problem verursacht. Notieren Sie sich den Wert der Felder **Menge** und **Einheit**.
1. Gehen Sie zu **Organisationsverwaltung \> Einheiten \> Einheiten**.
1. Wählen Sie die Einheit aus, für die der Lieferschein nicht generiert werden kann.
1. Passen Sie den Wert des Feldes **Dezimalgenauigkeit** wie gewünscht an.

### <a name="make-sure-that-the-inventory-unit-of-measure-is-smaller-than-the-sales-unit-of-measure"></a>Stellen Sie sicher, dass die Maßeinheit des Bestandes kleiner ist als die Maßeinheit des Verkaufs.

Stellen Sie sicher, dass die Maßeinheit des Bestands kleiner ist als die Maßeinheit des Verkaufs. Ziehen Sie in Erwägung, die Maßeinheit für das Element bei Bedarf neu zu konfigurieren.
