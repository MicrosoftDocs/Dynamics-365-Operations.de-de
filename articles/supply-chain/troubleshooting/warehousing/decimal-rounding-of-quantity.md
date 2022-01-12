---
title: Dezimale Rundung der physischen Aktualisierungsmenge ist falsch
description: Wenn Sie einen Lieferschein erzeugen, enthält die ausgehende Ladung eine Menge, die nicht mit der in der Einheit definierten Dezimalgenauigkeit übereinstimmt.
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
ms.openlocfilehash: a9e0475aab452daa9e1a6f012e17a59e611010da
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920472"
---
# <a name="decimal-rounding-of-the-physical-updating-quantity-is-incorrect"></a>Dezimale Rundung der physischen Aktualisierungsmenge ist falsch

Fehlercode: SYS19589

## <a name="symptoms"></a>Symptome

Wenn Sie einen Lieferschein erzeugen, enthält die ausgehende Ladung eine Menge, die nicht mit der in der Einheit definierten Dezimalgenauigkeit übereinstimmt.

Wenn Sie versuchen, einen Lieferschein zu generieren, zeigt das System die folgende Fehlermeldung an:

> Dezimalstelle der physischen Buchungsmenge in Einheit '%1' wurde falsch gerundet.

Daher können Sie den Lieferschein für die Ladung nicht generieren.

## <a name="cause"></a>Ursache

Das System wertet aus, ob die dezimale Rundung der Versandmenge mit der dezimalen Genauigkeit übereinstimmt, die für die Versandeinheit definiert ist. Wenn das System die Versandmenge auf die angegebene Anzahl von Dezimalstellen rundet und feststellt, dass die gerundete Versandmenge nicht mit der tatsächlichen Versandmenge übereinstimmt, können Sie den Lieferschein nicht erzeugen. Dieses Problem kann zum Beispiel auftreten, wenn die Verkaufsmenge 1,75 Kilogramm (kg) beträgt, die Dezimalgenauigkeit aber auf *1* festgelegt ist.

## <a name="resolution"></a>Lösung

Die Ladung oder Sendung befindet sich derzeit in einem Status, in dem die Lieferscheinerstellung fehlschlägt. Um dieses Problem zu beheben, führen Sie eine der folgenden Aufgaben aus:

- Überprüfen Sie Ihre Ladungszeilen und nehmen Sie Anpassungen vor, um sicherzustellen, dass die Menge sauber umgewandelt werden kann, ohne Dezimalzahlen und andere Rundungsprobleme.
- Überprüfen Sie Ihre Ladungszeilen und nehmen Sie Anpassungen vor, um sicherzustellen, dass die Einheit und die Menge mit der Dezimalgenauigkeit der Einheit übereinstimmen.

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-decimal-numbers-and-any-other-rounding-issues"></a>Überprüfen Sie die Zeilen mit den Ladungen und nehmen Sie Anpassungen vor, um sicherzustellen, dass die Menge sauber umgerechnet werden kann, ohne Dezimalzahlen und andere Rundungsprobleme

Gehen Sie wie folgt vor, um Ihre Zeilen mit den Ladungen zu überprüfen und Anpassungen vorzunehmen, um sicherzustellen, dass die Menge sauber umgerechnet werden kann, ohne Dezimalzahlen und andere Rundungsprobleme.

1. Gehen Sie zu **Lagerortverwaltung \> Ladungen \> Alle Ladungen**.
1. Wählen Sie die Ladung aus, für die der Lieferschein nicht generiert werden kann.
1. Wählen Sie im Aktionsbereich auf der Registerkarte **Versand und Empfang** in der Gruppe **Stornieren** die Option **Sendungsbestätigung stornieren**.
1. Wählen Sie auf der Registerkarte **Ladungszeilen** die Ladung des Elements, das ein Problem verursacht.
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
