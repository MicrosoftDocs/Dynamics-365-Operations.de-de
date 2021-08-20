---
title: Lieferungen mithilfe der Workbench zur Lieferungskonsolidierung konsolidieren
description: In diesem Thema wird ein Szenario vorgestellt, in dem mehrere Bestellungen an das Lager freigegeben werden und anschließend mit der Workbench zur Lieferungskonsolidierung später in Lieferungen automatisch konsolidiert werden.
author: GarmMSFT
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSShipConsolidationSetShipment
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 5c4234cbe591079daf45aef6309cc84da16246ba6461a513b93589b2e1e6bf28
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6728434"
---
# <a name="consolidate-shipments-by-using-the-shipment-consolidation-workbench"></a>Lieferungen mithilfe der Workbench zur Lieferungskonsolidierung konsolidieren

[!include [banner](../includes/banner.md)]

In diesem Thema wird ein Szenario vorgestellt, in dem mehrere Bestellungen an das Lager freigegeben werden und anschließend mit der Workbench zur Lieferungskonsolidierung später in Lieferungen automatisch konsolidiert werden.

## <a name="make-demo-data-available"></a>Demodaten zur Verfügung stellen

Das Szenario in diesem Thema verweist auf Werte und Datensätze, die in den für Microsoft Dynamics 365 Supply Chain Management bereitgestellten Standarddemodaten enthalten sind. Wenn Sie die hier angegebenen Werte während der Übungen verwenden möchten, müssen Sie in einer Umgebung arbeiten, in der die Demodaten installiert sind, und die juristische Person auf **USMF** festlegen, bevor Sie beginnen.

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a>Richten Sie Richtlinien zur Lieferungskonsolidierung und Produktfilter ein

In dem hier beschriebenen Szenario wird davon ausgegangen, dass Sie die Funktion bereits aktiviert und die Übungen in [Richtlinien zur Lieferungskonsolidierung konfigurieren](configure-shipment-consolidation-policies.md) ausgeführt haben und die dort beschriebenen Richtlinien und anderen Datensätze erstellt haben. Stellen Sie sicher, dass Sie diese Übungen ausführen, bevor Sie mit diesem Szenario fortfahren.

## <a name="turn-on-the-manual-shipment-consolidation-feature"></a>Manuelle Lieferungskonsolidierung aktivieren

Bevor Sie die Funktion *Manuelle Lieferungskonsolidierung* verwenden können, müssen Sie sie in Ihrem System aktivieren. Administratoren können mit den Einstellungen [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und sie aktivieren. Im Arbeitsbereich **Funktionsverwaltung** ist die Funktion wie folgt aufgeführt:

- **Module:** *Lagerortverwaltung*
- **Funktionsname:** *Manuelle Lieferungskonsolidierung*

Wie unter [Richtlinien zur Lieferungskonsolidierung konfigurieren](configure-shipment-consolidation-policies.md) erwähnt, müssen Sie auch die *Lieferung konsolidieren*-Funktion einschalten, bevor Sie Richtlinien erstellen können. Sie sollten diesen Schritt jedoch bereits abgeschlossen haben.

## <a name="create-the-sales-orders-for-this-scenario"></a>Erstellen Sie die Kundenaufträge für dieses Szenario

Erstellen Sie zunächst eine Sammlung von Kundenaufträgen, mit denen Sie arbeiten können. Sie müssen mit einem Lagerort arbeiten, der für WMS-Prozesse (Advanced Warehouse) aktiviert ist. Sofern nicht ausdrücklich ein anderes Lager erwähnt wird, muss dasselbe Lager für jeden der folgenden Auftragssätze verwendet werden.

Wechseln Sie zu **Debitoren \> Aufträge \> Alle Kundenaufträge**, und erstellen Sie eine Sammlung von Kundenaufträgen mit den Einstellungen, die in den folgenden Unterabschnitten beschrieben werden.

### <a name="create-order-set-1"></a>Auftragssatz 1 erstellen

#### <a name="sales-orders-1-1-and-1-2"></a>Aufträge 1-1 und 1-2

1. Erstellen Sie zwei identische Aufträge mit den folgenden Einstellungen:

    - **Debitorenkonto:** *US-001*
    - **Lieferart:** *Airwa-Air*

1. Eine Auftragsposition hat die folgenden Einstellungen:

    - **Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)
    - **Menge** *1.00*

1. Wählen Sie **Lager \> Reservierung** und dann im Aktionsbereich die Option **Los reservieren** aus, um die Bestellposition zu reservieren.

#### <a name="sales-order-1-3"></a>Auftrag 1-3

1. Erstellen Sie einen Auftrag mit den folgenden Einstellungen:

    - **Debitorenkonto:** *US-001*
    - **Lieferart:** *10*

1. Eine Auftragsposition hat die folgenden Einstellungen:

    - **Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)
    - **Menge** *1.00*

1. Wählen Sie **Lager \> Reservierung** und dann im Aktionsbereich die Option **Los reservieren** aus, um die Bestellposition zu reservieren.
1. Fügen Sie eine zweite Auftragsposition mit den folgenden Einstellungen hinzu:

    - **Artikelnummer:** *A0002* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)
    - **Menge** *1.00*
    - **Lieferart:** *Airwa-Air*

1. Wählen Sie **Lager \> Reservierung** und dann im Aktionsbereich die Option **Los reservieren** aus, um die zweite Bestellposition zu reservieren.

### <a name="create-order-set-2"></a>Auftragssatz 2 erstellen

#### <a name="sales-orders-2-1-and-2-2"></a>Aufträge 2-1 und 2-2

1. Erstellen Sie zwei identische Aufträge mit den folgenden Einstellungen:

    - **Debitorenkonto:** *US-002*
    - **Lieferart:** *Airwa-Air*

1. Eine Auftragsposition hat die folgenden Einstellungen:

    - **Artikelnummer:** *M9200* (ein Artikel, bei dem der **Code 4**-Filter auf *Brennbar* eingestellt ist)
    - **Menge** *1.00*

1. Wählen Sie **Lager \> Reservierung** und dann im Aktionsbereich die Option **Los reservieren** aus, um die Bestellposition zu reservieren.
1. Fügen Sie eine zweite Auftragsposition mit den folgenden Einstellungen hinzu:

    - **Artikelnummer:** *M9201* (ein Artikel, bei dem der **Code 4**-Filter auf *Explosiv* eingestellt ist)
    - **Menge** *1.00*
    - **Lieferart:** *Airwa-Air*

1. Wählen Sie **Lager \> Reservierung** und dann im Aktionsbereich die Option **Los reservieren** aus, um die zweite Bestellposition zu reservieren.

### <a name="create-order-set-3"></a>Auftragssatz 3 erstellen

#### <a name="sales-orders-3-1-and-3-2"></a>Aufträge 3-1 und 3-2

1. Erstellen Sie zwei identische Aufträge mit den folgenden Einstellungen:

    - **Debitorenkonto:** *US-001*
    - **Debitorenanforderung:** *1*

1. Eine Auftragsposition hat die folgenden Einstellungen:

    - **Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)
    - **Menge** *1.00*

1. Wählen Sie **Lager \> Reservierung** und dann im Aktionsbereich die Option **Los reservieren** aus, um die Bestellposition zu reservieren.

#### <a name="sales-orders-3-3-and-3-4"></a>Aufträge 3-3 und 3-4

1. Erstellen Sie zwei identische Aufträge mit den folgenden Einstellungen:

    - **Debitorenkonto:** *US-001*
    - **Debitorenanforderung:** *2*

1. Eine Auftragsposition hat die folgenden Einstellungen:

    - **Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)
    - **Menge** *1.00*

1. Wählen Sie **Lager \> Reservierung** und dann im Aktionsbereich die Option **Los reservieren** aus, um die Bestellposition zu reservieren.

### <a name="create-order-set-4"></a>Auftragssatz 4 erstellen

#### <a name="sales-orders-4-1-and-4-2"></a>Aufträge 4-1 und 4-2

1. Erstellen Sie zwei identische Aufträge mit den folgenden Einstellungen:

    - **Debitorenkonto:** *US-003*

1. Eine Auftragsposition hat die folgenden Einstellungen:

    - **Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)
    - **Menge** *1.00*

1. Wählen Sie **Lager \> Reservierung** und dann im Aktionsbereich die Option **Los reservieren** aus, um die Bestellposition zu reservieren.

#### <a name="sales-orders-4-3-and-4-4"></a>Aufträge 4-3 und 4-4

1. Erstellen Sie zwei identische Aufträge mit den folgenden Einstellungen:

    - **Debitorenkonto:** *US-004*

1. Eine Auftragsposition hat die folgenden Einstellungen:

    - **Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)
    - **Menge** *1.00*

1. Wählen Sie **Lager \> Reservierung** und dann im Aktionsbereich die Option **Los reservieren** aus, um die Bestellposition zu reservieren.

#### <a name="sales-orders-4-5-and-4-6"></a>Aufträge 4-5 und 4-6

1. Erstellen Sie zwei identische Aufträge mit den folgenden Einstellungen:

    - **Debitorenkonto:** *US-007*
    - **Standort:** *6*
    - **Lagerort:** *61*
    - **Pool:** *ShipCons*

1. Eine Auftragsposition hat die folgenden Einstellungen:

    - **Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)
    - **Menge** *1.00*

1. Wählen Sie **Lager \> Reservierung** und dann im Aktionsbereich die Option **Los reservieren** aus, um die Bestellposition zu reservieren.

#### <a name="sales-orders-4-7-and-4-8"></a>Aufträge 4-7 und 4-8

1. Erstellen Sie zwei identische Aufträge mit den folgenden Einstellungen:

    - **Debitorenkonto:** *US-007*
    - **Standort:** *6*
    - **Lagerort:** *61*
    - **Pool:** Lassen Sie dieses Feld leer.

1. Eine Auftragsposition hat die folgenden Einstellungen:

    - **Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)
    - **Menge** *1.00*

1. Wählen Sie **Lager \> Reservierung** und dann im Aktionsbereich die Option **Los reservieren** aus, um die Bestellposition zu reservieren.

## <a name="release-the-orders-to-the-warehouse"></a>Aufträge für den Lagerort freigeben

Führen Sie die folgenden Schritte aus, um jeden Auftrag, den Sie für dieses Szenario erstellt haben, für das Lager freizugeben.

1. Wechseln Sie zu **Debitoren \> Aufträge \> Alle Aufträge**.
1. Suchen und wählen Sie den freizugebenden Auftrag aus.
1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerort**, in der Gruppe **Aktivitäten \> Für Lagerort freigeben**, um die ausgewählten Aufträge freizugeben.
1. Wiederholen Sie diesen Vorgang für alle anderen Aufträge, die Sie für dieses Szenario erstellt haben.

## <a name="consolidate-the-shipments-by-using-the-shipment-consolidation-workbench"></a>Lieferungen mithilfe der Workbench zur Lieferungskonsolidierung konsolidieren

1. Wechseln Sie zu **Lagerortverwaltung \> An Lager freigeben \> Lieferungskonsolidierungs-Workbench**.
1. Wählen Sie im Aktionsbereich **Abfrage bearbeiten** aus.
1. Wählen Sie im Abfrageeditor-Dialogfeld auf der Registerkarte **Bereich** **Hinzufügen** aus, um eine Zeile mit den folgenden Einstellungen zum Raster hinzuzufügen:

    - **Tabelle:** *Aufträge*
    - **Feld:** *Auftrag*
    - **Kriterien:** Geben Sie eine durch Kommas getrennte Liste der Auftragsnummern für jeden Auftragssatz ein, den Sie für dieses Szenario erstellt haben.

1. Wählen Sie **OK** aus, um die Abfrage zu speichern und das Dialogfeld zu schließen.
1. Wählen Sie im Aktionsbereich **Lieferungen konsolidieren** aus.
1. Wählen Sie alle Lieferungen und dann im Aktionsbereich **Konsolidieren** aus.

## <a name="verify-the-shipments"></a>Überprüfen Sie die Lieferungen

Mit dem folgenden Verfahren können Sie die Lieferungen überprüfen, die als Ergebnis der Lieferungskonsolidierung erstellt oder aktualisiert wurden. Verwenden Sie diese Option, um jeden Auftragssatz zu überprüfen, den Sie für dieses Szenario erstellt haben, und überprüfen Sie anschließend die folgenden Unterabschnitte, um sicherzustellen, dass Sie die erwarteten Ergebnisse erhalten haben.

1. Gehen Sie zu **Lagerortverwaltung \> Lieferungen \> Alle Lieferungen**.
1. Suchen Sie die gewünschte Lieferung und wählen Sie sie aus.
1. Wenn beim Erstellen oder Aktualisieren der Lieferung eine Konsolidierungsrichtlinie verwendet wurde, sollte diese im Feld **Richtlinie für Lieferungskonsolidierung** angezeigt werden.

### <a name="related-shipments-for-order-set-1"></a>Verwandte Lieferungen für Auftragssatz 1

Es sollten zwei Lieferungen erstellt worden sein:

- Die erste Lieferung enthält drei Zeilen und wurde mit der *CustomerMode*-Lieferungskonsolidierungsrichtlinie erstellt.
- Die zweite Lieferung, die nicht *Airways* als Transportart der Lieferung verwendet, wurde unter Verwendung der *CustomerOrderNo*-Lieferungskonsolidierungsrichtlinie erstellt.

### <a name="related-shipments-for-order-set-2"></a>Verwandte Lieferungen für Auftragssatz 2

Es sollten drei Lieferungen erstellt worden sein:

- Die erste Lieferung enthält die *Brennbar*-Artikel.
- Jede der beiden anderen Lieferungen enthält eine Position mit dem *Explosiv*-Artikel.

### <a name="related-shipments-for-order-set-3"></a>Verwandte Lieferungen für Auftragssatz 3

Es sollten zwei Lieferungen erstellt worden sein:

- Die erste Lieferung enthält Bestellpositionen aus dem Auftrag, in dem das **Debitorenanforderung**-Feld auf *1* gesetzt ist.
- Die zweite Lieferung enthält Bestellpositionen aus dem Auftrag, in dem das **Debitorenanforderung**-Feld auf *2* gesetzt ist.

### <a name="related-shipments-for-order-set-4"></a>Verwandte Lieferungen für Auftragssatz 4

Es sollten vier Lieferungen erstellt worden sein:

- Positionen aus zwei Bestellungen für Debitor *US-003* wurden unter Verwendung der *Auftragspool*-Lieferungskonsolidierungsrichtlinie zu einer Lieferung zusammengefasst.
- Positionen aus zwei Bestellungen für Debitor *US-004* wurden unter Verwendung der *Auftragspool*-Lieferungskonsolidierungsrichtlinie zu einer Lieferung zusammengefasst.
- Positionen aus aus den Aufträgen 4-5 und 4-6 für Debitor *US-007* wurden unter Verwendung der *Auftragspool*-Lieferungskonsolidierungsrichtlinie zu einer Lieferung zusammengefasst.
- Positionen aus aus den Aufträgen 4-7 und 4-8 für Debitor *US-007* wurden unter Verwendung der *CrossOrder*-Lieferungskonsolidierungsrichtlinie zu einer Lieferung zusammengefasst.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Lieferungskonsolidierungsrichtlinien](about-shipment-consolidation-policies.md)
- [Richtlinien zur Lieferungskonsolidierung konfigurieren](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]