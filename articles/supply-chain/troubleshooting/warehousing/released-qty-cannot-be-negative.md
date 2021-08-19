---
title: Eine Ladungsposition kann nicht aktualisiert werden, da die freigegebene Menge negativ wäre
description: Dieses Problem tritt auf, wenn das Aktualisieren oder Löschen einer Ladungsposition eine negative freigegebene Menge verursachen würde.
author: GalynaFedorova
ms.date: 6/30/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningListPage_WHSLoadLineUnShipQty,WHSLoadTable_WHSLoadLineUnShipQty,WHSLoadPlanningWorkbench_WHSLoadLineUnShipQty,WHSShipmentDetails_WHSLoadLineUnShipQty,WHSLoadPlanningListPage_DeleteButtonLoadLine,WHSLoadTable_DeleteButtonLoadLine,WHSLoadPlanningWorkbench_DeleteButtonLoadLine,WHSShipmentDetails_DeleteButtonShipment
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: a6325a632e1f68a0a3a9cb6b6091c48da014a405e8ce9ad69ea841f5cceb216f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6728458"
---
# <a name="cant-update-a-load-line-because-the-released-quantity-would-be-negative"></a>Eine Ladungsposition kann nicht aktualisiert werden, da die freigegebene Menge negativ wäre

Fehlercode: @WAX:ReleasedQtyCannotBeNegative

## <a name="symptoms"></a>Symptome

Dieses Problem tritt auf, wenn das Aktualisieren oder Löschen einer Ladungsposition eine negative freigegebene Menge verursachen würde. In diesem Fall zeigt das System beim Versuch, die Ladungszeile zu aktualisieren oder zu löschen, die folgende Fehlermeldung an:

> Die freigegebene Menge kann für Artikel %1, Los %2 nicht negativ sein.

Daher können Sie die Ladungszeile nicht aktualisieren oder löschen.

## <a name="cause"></a>Ursache

Nachdem Sie eine Ladungszeile aktualisiert oder gelöscht haben, aktualisiert das System die freigegebene Menge der zugehörigen Verkaufsposition (*whsSalesLine.ReleaseQty*). Das System wertet die freigegebene Menge aus und wenn es feststellt, dass die freigegebene Menge der Position nach der Aktualisierung negativ wäre, können Sie die Position nicht aktualisieren oder löschen. Diese Prüfung erfolgt immer dann, wenn Sie versuchen, entweder die Ladungspositionsmenge oder die Maßeinheit durch verschiedene Aktionen zu aktualisieren, wie eine Ladungsposition löschen, eine Lieferung löschen, die Menge einer Ladungsposition löschen, die entnommene Quantität verringern oder zu wenig entnehmen.

Die häufigste Ursache für dieses Problem ist eine Änderung der Einheitenumrechnung, die für offene Ladungspositionen verwendet wird. Zum Beispiel war die Einheitenumrechnung bei der Freigabe eines Auftrags *50 EA = 1 PL*. Bevor jedoch die entsprechende Ladungslieferung abgeschlossen war, wurde die Einheitenumrechnung geändert auf *100 EA = 1 PL*.

## <a name="resolution"></a>Lösung

Die Lösung besteht darin, die Änderungen der Einheitenumrechnung rückgängig zu machen, die Ladungsposition zu aktualisieren oder zu löschen und dann die Umrechnung erneut zu durchzuführen. Sie müssen verhindern, dass andere Ladungen verarbeitet werden, die den Artikel enthalten, der das Problem verursacht hat, bis das Problem behoben ist. Andernfalls werden die neuen Umrechnungen möglicherweise für andere bereits geöffnete Ladungen verwendet.

Um dieses Problem zu beheben, führen Sie die folgenden Aufgaben aus:

1. Überprüfen Sie die Einheitenumrechnung, die für die Ladungsposition verwendet wurde.
2. Überprüfen Sie die aktuelle Einheitenumrechnung für den Artikel und nehmen Sie Regulierungen vor, damit die Ladungsposition aktualisiert oder gelöscht werden kann.
3. Aktualisieren oder löschen Sie die Ladungsposition und machen Sie die Regulierung der Einheitenumrechnung rückgängig.

### <a name="review-the-unit-conversion-that-was-used-for-the-load-line"></a>Überprüfen Sie die Einheitenumrechnung, die für die Ladungsposition verwendet wurde

Gehen Sie wie folgt vor, um Ihre Ladungsposition zu überprüfen und die Einheitenumrechnung zu notieren, die für die Ladungsposition verwendet wurde.

1. Gehen Sie zu **Lagerortverwaltung \> Ladungen \> Alle Ladungen**.
1. Wählen Sie die Ladung aus, die die Ladungsposition enthält, die nicht gelöscht oder aktualisiert werden kann.
1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Ladungen** in der Gruppe **Zugehörige Informationen** die Option **Arbeit**.
1. Wählen Sie im oberen Raster die entsprechende Arbeitskennung aus.
1. Berechnen Sie in der Registerkarte **Allgemein** unten auf der Seite die Umrechnungsquote zwischen dem Wert der **Bestandsarbeitsmenge** Wert und dem Wert der **Arbeitsmenge**. Notieren Sie die Quote.
1. Wiederholen Sie diesen Vorgang für alle relevanten Arbeitskennungen, um sicherzustellen, dass dieselbe Umrechnung verwendet wurde.

### <a name="review-the-current-unit-conversion-for-the-item-and-make-adjustments"></a>Überprüfen Sie die aktuelle Einheitenumrechnung für den Artikel und nehmen Sie Regulierungen vor

Gehen Sie wie folgt vor, um die Einheitenumrechnung Ihres Produkts zu überprüfen und Regulierungen vorzunehmen, um sicherzustellen, dass die Einheitenumrechnung und die Ladungsposition übereinstimmen.

1. Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**.
1. Öffnen Sie das relevante Produkt, um zu seiner Seite **Details für freigegebene Produkte** zu gelangen.
1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Produkt** in der Gruppe **Einrichten** auf **Einheitenumrechnung**.
1. Wählen Sie die Umrechnung zwischen den Einheiten aus und nehmen Sie Regulierungen vor, indem Sie die Umrechnung verwenden, die Sie im vorherigen Abschnitt gefunden haben.

### <a name="update-or-delete-the-load-line-and-revert-the-unit-conversion-adjustments"></a>Aktualisieren oder löschen Sie die Ladungsposition und machen Sie die Regulierung der Einheitenumrechnung rückgängig

Gehen Sie wie folgt vor, um die Ladungsposition nach Bedarf zu verarbeiten und die Einheitenumrechnungen rückgängig zu machen.

1. Gehen Sie zu **Lagerortverwaltung \> Ladungen \> Alle Ladungen**.
1. Öffnen Sie die Ladung, die die Ladungsposition enthält, die nicht gelöscht oder aktualisiert werden kann.
1. Wählen Sie auf der Registerkarte **Ladezeilen** Inforegister die Zeile für die Ladung aus.
1. Fahren Sie nach Bedarf mit den erforderlichen Aktionen fort. (Löschen Sie beispielsweise die Ladungsposition oder ändern Sie ihre Menge.)
1. Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**.
1. Öffnen Sie das relevante Produkt, um zu seiner Seite **Details für freigegebene Produkte** zu gelangen.
1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Produkt** in der Gruppe **Einrichten** auf **Einheitenumrechnung**.
1. Wählen Sie die Umrechnung zwischen den Einheiten aus und machen Sie die Regulierungen aus dem vorherigen Abschnitt rückgängig.
