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
ms.openlocfilehash: f3ebd47ffc85d4ca257b404579d60d679f7929b6
ms.sourcegitcommit: f9b145ef4a81cec81f420871b4130b05db4f4500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301304"
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
- Die Lagerplatzrichtlinie wurde mit dem Packplatz als endgültigem Versandort konfiguriert, während Sie die Wave-Template-Containerisierung verwenden.

## <a name="resolution"></a>Lösung

Die Ladung oder Sendung befindet sich derzeit in einem Status, in dem die Versandbestätigung fehlschlägt. Um dieses Problem zu beheben, führen Sie eine der folgenden Aufgaben aus:

- Überprüfen Sie Ihre Ladungs-Zeilen und stellen Sie sicher, dass alle zugehörigen Arbeiten am endgültigen Versandort abgeschlossen wurden und die Mengen übereinstimmen.
- Stornieren Sie die Arbeits-IDs, die mit dem Verpackungsort als endgültigem Versandort erstellt wurden, konfigurieren Sie die Lagerplatzrichtlinie neu und geben Sie die Ladung erneut frei.

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>Überprüfen Sie die Zeilen Ihrer Ladung und stellen Sie sicher, dass alle zugehörigen Arbeiten am endgültigen Versandort abgeschlossen wurden und dass die Mengen übereinstimmen.

Gehen Sie wie folgt vor, um Ihre Ladungszeilen zu überprüfen und sicherzustellen, dass alle zugehörigen Arbeiten am endgültigen Versandort abgeschlossen wurden und dass die Mengen übereinstimmen.

1. Gehen Sie zu **Lagerortverwaltung \> Ladungen \> Alle Ladungen**.
1. Wählen Sie die Ladung, für die die Sendung nicht bestätigt werden kann.
1. Wählen Sie auf der Registerkarte **Ladezeilen** Inforegister die Zeile für die Ladung aus.
1. Notieren Sie sich den Wert des Feldes **Werk erstellte Menge**.
1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Ladungen** in der Gruppe **Zugehörige Informationen** die Option **Arbeit**.
1. Überprüfen Sie, ob die Arbeit am endgültigen Versandort abgeschlossen wurde und ob die entnommene Arbeitsmenge mit der erstellten Arbeitsmenge in der Ladung übereinstimmt.
1. Wiederholen Sie diesen Vorgang für alle Ladungs-Zeilen, um sicherzustellen, dass alle Kriterien erfüllt sind.

### <a name="cancel-the-work-ids-that-have-been-created-with-the-packing-location-as-the-final-shipping-location-reconfigure-the-location-directive-and-rerelease-the-load"></a>Stornieren Sie die Arbeits-IDs, die mit dem Verpackungsort als endgültigem Versandort erstellt wurden, konfigurieren Sie die Lagerplatzrichtlinie neu und geben Sie die Ladung erneut frei

Gehen Sie wie folgt vor, um die Arbeits-IDs zu stornieren, die den Packort als endgültigen Lagerplatz mit automatischer Containerisierung haben.

1. Gehen Sie zu **Lagerortverwaltung \> Periodische Aufgaben \> Aufräumen \> Arbeit stornieren**.
1. Der Dialog **Arbeit stornieren** wird geöffnet. Geben Sie im Feld **Arbeits-ID** die ID der Arbeit an, die Sie abbrechen wollen. Die ausgewählte Arbeits-ID muss einen **Arbeitsstatus**-Wert von *Offen*, *In Bearbeitung*, *Abgebrochen*, *Zusammengeführt* oder *Geschlossen* haben.
1. Wählen Sie **OK** aus.
1. Wählen Sie **Ja**, um zu bestätigen, dass Sie die Arbeit abbrechen wollen.
1. Wiederholen Sie diesen Vorgang für die anderen Arbeits-IDs nach Bedarf.

Weitere Informationen finden Sie unter [Stornieren von Lagerort-Arbeiten zur Ausnahmebehandlung](../../warehousing/cancel-warehouse-work.md).

Gehen Sie wie folgt vor, um die Lagerplatzrichtlinie so umzukonfigurieren, dass sie nicht den Verpackungsplatz als endgültigen Versandort verwendet, wenn die automatische Containerisierung für die Wellenvorlage festgelegt ist.

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerplatzrichtlinien**.
1. Wählen Sie im Feld **Arbeitsauftragsart** *Arbeitsaufträge* aus.
1. Wählen Sie die Lagerplatzrichtlinie aus, die Sie für die automatisierte Containerisierung verwenden.
1. Wählen Sie in der Symbolleiste **Aktionen der Lagerplatzrichtlinie** Inforegister **Abfrage bearbeiten**.
1. Suchen Sie im Abfrage-Editor-Dialog auf der Registerkarte **Bereich** die Zeile, in der **Feld** auf *Lagerplatzprofil* festgelegt ist, und stellen Sie sicher, dass das Feld **Kriterien** für diese Zeile nicht auf ein Lagerplatzprofil festgelegt ist, das einen **Lagerplatztyp** von *Verpackung* hat. Passen Sie das Feld **Kriterien** an, um den endgültigen PUT-Lagerplatz zu korrigieren.

Gehen Sie wie folgt vor, um die Ladung erneut freizugeben und Arbeits-IDs mit dem korrekten endgültigen Versandort zu erstellen.

1. Wechseln Sie zu **Transportverwaltung \> Planung \> Ladungsplanungsworkbench**.
1. Suchen Sie im Bereich **Ladungen** die Ladung, die freigegeben werden muss.
1. Wählen Sie in der Symbolleiste des Bereichs **Ladungen** die Option **Freigeben \> Freigabe an Lagerort**, um die ausgewählte Ladung an den Lagerort freizugeben.
1. Wiederholen Sie diesen Vorgang für die anderen Ladungen nach Bedarf.
