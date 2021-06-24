---
title: Die Menge kann nicht reduziert werden, wenn ein Auftrag storniert wird
description: Die Menge kann nicht reduziert werden, wenn ein Auftrag storniert wird.
author: hja-ms
ms.date: 5/17/2021
ms.topic: troubleshooting
ms.search.form: SalesTable_SalesCancelOrder, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: hja
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1a2cc9c9fd3d085508fc652bc9ee0a352d869dee
ms.sourcegitcommit: a02d3d64c899f8554b74342d5a1856d824bf1abe
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2021
ms.locfileid: "6230835"
---
# <a name="the-quantity-cant-be-reduced-when-a-sales-order-is-canceled"></a>Die Menge kann nicht reduziert werden, wenn ein Auftrag storniert wird

Fehlercode: SYS138831

## <a name="symptoms"></a>Symptome

Das System zeigt die folgende Fehlermeldung an:

> Die Menge kann nicht reduziert werden. Die Anzahl der Lagerbuchungen auf Bestellung ist zu gering, weil die Menge oder ein Teil davon von einem Ausgabeauftrag oder einem Produktionsauftrag referenziert wird oder gegen andere Buchungen gekennzeichnet ist.

## <a name="cause"></a>Ursache

Wenn einem Auftrag eine Arbeit zugeordnet ist, können Sie den Auftrag erst stornieren, wenn die Arbeit storniert und entfernt wurde. Diese Anforderung gilt auch dann, wenn die mit dem Auftrag verbundene Arbeit abgeschlossen ist.

## <a name="resolution"></a>Lösung

Um dieses Problem zu beheben, führen Sie die folgenden Aufgaben aus:

1. Offene Arbeit abbrechen.
1. Löschen Sie die Auslastung.
1. Die entnommenen Mengen reduzieren.

### <a name="cancel-open-work"></a>Offene Arbeit abbrechen

Um die offene Arbeit abzubrechen, führen Sie diese Schritte aus.

1. Gehen Sie zu **Lagerortverwaltung \> Periodische Aufgaben \> Aufräumen \> Arbeit stornieren**.
1. Geben Sie im Feld **Arbeits-ID** die ID der Arbeit an, die Sie stornieren möchten und die derzeit einen **Arbeitsstatus**-Wert von *Offen*, *In Bearbeitung*, *Abgebrochen*, *Zusammengeführt* oder *Geschlossen* hat.
1. Wählen Sie **OK** aus.
1. Wählen Sie **Ja**, um zu bestätigen, dass Sie die Arbeit abbrechen wollen.

### <a name="delete-the-load"></a>Die Auslastung löschen

Um eine Auslastung zu löschen, tun Sie Folgendes.

1. Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.
1. Öffnen Sie den entsprechenden Auftrag.
1. Wählen Sie auf dem Inforegister **Auftragspositionen** **Lagerort \> Arbeitsdetails** aus.
1. Wählen Sie auf der Seite **Arbeit** im Aktivitätsbereich auf der Registerkarte **Arbeit** in der Gruppe **Arbeit** die Option **Arbeit aufteilen**.
1. Bestätigen Sie, dass das Feld **Arbeitsstatus** auf *Storniert* gesetzt ist.
1. Schließen Sie die Seite **Arbeit**.
1. Wählen Sie auf der Auftragsdetailseite im Inforegister **Auftragspositionen** **Lagerort \> Details laden**.
1. Wählen Sie im Aktivitätsbereich **Löschen**.
1. Wählen Sie **Ja**, um zu bestätigen, dass Sie die Auslastung löschen wollen.
1. Schließen Sie die Seite **Auslastung**.

### <a name="reduce-the-picked-quantity"></a>Die entnommenen Mengen reduzieren

Nachdem alle Arbeiten storniert wurden, führen Sie diese Schritte aus, um die kommissionierte Menge zu reduzieren.

1. Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.
1. Öffnen Sie den entsprechenden Auftrag.
1. Wählen Sie im Inforegister **Auftragspositionen** **Position aktualisieren \> Wählen** aus der Symbolleiste.
1. Wählen Sie auf der Seite **Wählen** im Abschnitt **Transaktionen** die Zeile aus, in der das Feld **Problemstatus** auf *Ausgewählt* gesetzt ist.
1. Wählen Sie im Abschnitt **Transaktionen** **Entnahmeposition hinzufügen** aus der Symbolleiste.
1. Wählen Sie im Abschnitt **Entnahmeposition** **Alle entnehmen bestätigen** aus der Symbolleiste.
1. Schließen Sie die Seite **Wählen**.
1. Auf der Seite Auftragsdetails im Aktivitätsbereich, auf der Registerkarte **Auftrag** in der Gruppe **Verwalten** wählen Sie **Abbrechen** aus.
1. Wählen Sie **Ja**, um zu bestätigen, dass Sie den Auftrag abbrechen wollen.
