---
title: Lieferungen mithilfe der automatischen Auftragsfreigabe konsolidieren, wenn sie im Lager freigegeben werden
description: In diesem Thema wird ein Szenario vorgestellt, in dem mehrere Bestellungen in derselben automatisierten periodischen Freigabe an das Lager freigegeben werden.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, WHSShipmentConsolidation, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 376c7418b61c0192f9071a879b50b9ece7699894
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4970355"
---
# <a name="consolidate-shipments-when-they-are-released-to-the-warehouse-by-using-automatic-release-of-sales-orders"></a>Lieferungen mithilfe der automatischen Auftragsfreigabe konsolidieren, wenn sie im Lager freigegeben werden

[!include [banner](../includes/banner.md)]

In diesem Thema wird ein Szenario vorgestellt, in dem mehrere Bestellungen in derselben automatisierten periodischen Freigabe an das Lager freigegeben werden. Die Bestellungen werden automatisch in Lieferungen konsolidiert, basierend auf Regeln, die als Richtlinien zur Lieferungskonsolidierung definiert sind.

Während des Szenarios erstellen Sie Sätze von Kundenaufträgen und geben jeden Satz an das Lager frei. Anschließend überprüfen Sie die Lieferungen, die während der Lieferungskonsolidierung erstellt oder aktualisiert werden, basierend auf den konfigurierten Richtlinien.

## <a name="make-demo-data-available"></a>Demodaten zur Verfügung stellen

Das Szenario in diesem Thema verweist auf Werte und Datensätze, die in den für Microsoft Dynamics 365 Supply Chain Management bereitgestellten Standarddemodaten enthalten sind. Wenn Sie die hier angegebenen Werte während der Übungen verwenden möchten, müssen Sie in einer Umgebung arbeiten, in der die Demodaten installiert sind, und die juristische Person auf **USMF** festlegen, bevor Sie beginnen.

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a>Richten Sie Richtlinien zur Lieferungskonsolidierung und Produktfilter ein

In dem hier beschriebenen Szenario wird davon ausgegangen, dass Sie die Funktion bereits aktiviert und die Übungen in [Richtlinien zur Lieferungskonsolidierung konfigurieren](configure-shipment-consolidation-policies.md) ausgeführt haben und die dort beschriebenen Richtlinien und anderen Datensätze erstellt haben. Stellen Sie sicher, dass Sie diese Übungen ausführen, bevor Sie mit diesem Szenario fortfahren.

## <a name="create-the-sales-orders-for-this-scenario"></a>Erstellen Sie die Kundenaufträge für dieses Szenario

Erstellen Sie zunächst eine Sammlung von Kundenaufträgen, mit denen Sie arbeiten können. Sie müssen mit einem Lagerort arbeiten, der für WMS-Prozesse (Advanced Warehouse) aktiviert ist. Sofern nicht ausdrücklich ein anderes Lager erwähnt wird, muss dasselbe Lager für jeden der folgenden Auftragssätze verwendet werden.

Wechseln Sie zu **Debitoren \> Aufträge \> Alle Kundenaufträge**, und erstellen Sie eine Sammlung von Kundenaufträgen mit den Einstellungen, die in den folgenden Unterabschnitten beschrieben werden.

### <a name="create-order-set-1"></a>Auftragssatz 1 erstellen

#### <a name="sales-order-1-1"></a>Auftrag 1-1

1. Erstellen Sie einen Auftrag mit den folgenden Einstellungen:

    - **Debitorenkonto:** *US-001*
    - **Lieferart:** *Airwa-Air*

1. Eine Auftragsposition hat die folgenden Einstellungen:

    - **Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)
    - **Menge** *1.00*

#### <a name="sales-order-1-2"></a>Auftrag 1-2

1. Erstellen Sie einen Auftrag mit den folgenden Einstellungen:

    - **Debitorenkonto:** *US-001*
    - **Lieferart:** *Airwa-Air*

1. Eine Auftragsposition hat die folgenden Einstellungen:

    - **Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)
    - **Menge** *1.00*

#### <a name="sales-order-1-3"></a>Auftrag 1-3

1. Erstellen Sie einen Auftrag mit den folgenden Einstellungen:

    - **Debitorenkonto:** *US-001*
    - **Lieferart:** *10*

1. Eine Auftragsposition hat die folgenden Einstellungen:

    - **Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)
    - **Menge** *1.00*

1. Fügen Sie eine zweite Auftragsposition mit den folgenden Einstellungen hinzu:

    - **Artikelnummer:** *A0002* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)
    - **Menge** *1.00*
    - **Lieferart:** *Airwa-Air*

### <a name="create-order-set-2"></a>Auftragssatz 2 erstellen

#### <a name="sales-orders-2-1-and-2-2"></a>Aufträge 2-1 und 2-2

1. Erstellen Sie zwei identische Aufträge mit den folgenden Einstellungen:

    - **Debitorenkonto:** *US-002*

1. Eine Auftragsposition hat die folgenden Einstellungen:

    - **Artikelnummer:** *M9200* (ein Artikel, bei dem der **Code 4**-Filter auf *Brennbar* eingestellt ist)
    - **Menge** *1.00*

1. Fügen Sie eine zweite Auftragsposition mit den folgenden Einstellungen hinzu:

    - **Artikelnummer:** *M9201* (ein Artikel, bei dem der **Code 4**-Filter auf *Explosiv* eingestellt ist)
    - **Menge** *1.00*
    - **Lieferart:** *Airwa-Air*

### <a name="create-order-set-3"></a>Auftragssatz 3 erstellen

#### <a name="sales-order-3-1"></a>Auftrag 3-1

1. Erstellen Sie einen Auftrag mit den folgenden Einstellungen:

    - **Debitorenkonto:** *US-002*

1. Eine Auftragsposition hat die folgenden Einstellungen:

    - **Artikelnummer:** *M9200* (ein Artikel, bei dem der **Code 4**-Filter auf *Brennbar* eingestellt ist)
    - **Menge** *1.00*

1. Fügen Sie eine zweite Auftragsposition mit den folgenden Einstellungen hinzu:

    - **Artikelnummer:** *M9201* (ein Artikel, bei dem der **Code 4**-Filter auf *Explosiv* eingestellt ist)
    - **Menge** *1.00*
    - **Lieferart:** *Airwa-Air*

> [!NOTE]
> Diese Bestellung ist identisch mit den beiden Bestellungen, die Sie für Auftragssatz 2 erstellt haben. Es wird jedoch als eigener Auftragssatz aufgeführt, da Sie ihn später in diesem Szenario separat freigeben werden.

### <a name="create-order-set-4"></a>Auftragssatz 4 erstellen

#### <a name="sales-order-4-1"></a>Auftrag 4-1

1. Erstellen Sie einen Auftrag mit den folgenden Einstellungen:

    - **Debitorenkonto:** *US-001*
    - **Debitorenanforderung:** *1*

1. Eine Auftragsposition hat die folgenden Einstellungen:

    - **Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)
    - **Menge** *1.00*

### <a name="create-order-set-5"></a>Auftragssatz 5 erstellen

#### <a name="sales-orders-5-1-and-5-2"></a>Aufträge 5-1 und 5-2

1. Erstellen Sie zwei identische Aufträge mit den folgenden Einstellungen:

    - **Debitorenkonto:** *US-001*
    - **Debitorenanforderung:** *2*

1. Eine Auftragsposition hat die folgenden Einstellungen:

    - **Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)
    - **Menge** *1.00*

#### <a name="sales-order-5-3"></a>Auftrag 5-3

1. Erstellen Sie einen Auftrag mit den folgenden Einstellungen:

    - **Debitorenkonto:** *US-001*
    - **Debitorenanforderung:** *1*

1. Eine Auftragsposition hat die folgenden Einstellungen:

    - **Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)
    - **Menge** *1.00*

### <a name="create-order-set-6"></a>Auftragssatz 6 erstellen

#### <a name="sales-orders-6-1-and-6-2"></a>Aufträge 6-1 und 6-2

1. Erstellen Sie zwei identische Aufträge mit den folgenden Einstellungen:

    - **Debitorenkonto:** *US-003*
    - **Debitorenanforderung:** *2*

1. Eine Auftragsposition hat die folgenden Einstellungen:

    - **Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)
    - **Menge** *1.00*

#### <a name="sales-orders-6-3-and-6-4"></a>Aufträge 6-3 und 6-4

1. Erstellen Sie zwei identische Aufträge mit den folgenden Einstellungen:

    - **Debitorenkonto:** *US-004*
    - **Debitorenanforderung:** *1*

1. Eine Auftragsposition hat die folgenden Einstellungen:

    - **Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)
    - **Menge** *1.00*

#### <a name="sales-orders-6-5-and-6-6"></a>Aufträge 6-5 und 6-6

1. Erstellen Sie zwei identische Aufträge mit den folgenden Einstellungen:

    - **Debitorenkonto:** *US-007*
    - **Standort:** *6*
    - **Lagerort:** *61*
    - **Pool:** *ShipCons*

1. Eine Auftragsposition hat die folgenden Einstellungen:

    - **Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)
    - **Menge** *1.00*

#### <a name="sales-orders-6-7-and-6-8"></a>Aufträge 6-7 und 6-8

1. Erstellen Sie zwei identische Aufträge mit den folgenden Einstellungen:

    - **Debitorenkonto:** *US-007*
    - **Standort:** *6*
    - **Lagerort:** *61*
    - **Pool:** Lassen Sie dieses Feld leer.

1. Eine Auftragsposition hat die folgenden Einstellungen:

    - **Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)
    - **Menge** *1.00*

## <a name="automatic-release-of-sales-orders-to-the-warehouse"></a>Automatische Freigabe von Aufträgen für den Lagerort

Für jeden Satz von Kundenaufträgen, den Sie zuvor erstellt haben, führen Sie einen Vorgang für die automatische Freigabe an das Lager durch. In jedem Fall werden Sie [grundlegende Verfahren für die Freigabe an das Lager](#release-procedure) durcharbeiten, die hier beschrieben sind.

### <a name="basic-release-to-warehouse-procedure"></a><a name="release-procedure"></a>Grundlegendes Lagerfreigabeverfahren

Für jeden Satz von Kundenaufträgen, den Sie zuvor erstellt haben, führen Sie die drei in den folgenden Unterabschnitten beschriebenen Verfahren aus.

#### <a name="update-the-wave-template-that-will-be-used-during-release"></a>Aktualisieren Sie die Wellenvorlage, die während der Veröffentlichung verwendet wird

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Wellen \> Wellenvorlagen**.
1. Stellen Sie das Feld **Wellenvorlagentyp** auf *Versand* ein.
1. Suchen Sie die Wellenvorlage, die dem Lager zugeordnet ist, das Sie in den Auftragssätzen verwendet haben, die Sie für dieses Szenario erstellt haben, und wählen Sie sie aus. Zum Beispiel, wenn Sie ein Lager *24* verwendet haben, wählen Sie **Standard-24-Lieferung**-Wellenvorlage. Wenn Sie ein Lager *61* verwendet haben, wählen Sie die **61-Lieferung**-Wellenvorlage.
1. Wählen Sie im Aktionsbereich **Bearbeiten** aus.
1. Legen Sie die Option **Welle bei Freigabe für Lagerort verarbeiten** auf *Nein* fest.

#### <a name="release-to-the-warehouse"></a>Für Lagerort freigeben

1. Wechseln Sie zu **Lagerortverwaltung \> An Lager freigeben \> Automatische Freigabe von Aufträgen für den Lagerort**.
1. Stellen Sie die **Freizugebende Menge** auf *Alle* ein.
1. Wählen Sie auf dem Inforegister **Aufzeichnungen enthalten** **Filter** aus, um das Abfragedialogfeld zu öffnen.
1. Wählen Sie auf der Registerkarte **Bereich** **Hinzufügen** aus, um eine Zeile mit den folgenden Einstellungen zum Raster hinzuzufügen:

    - **Tabelle:** *Auftrag*
    - **Abgeleitete Tabelle:** *Auftrag*
    - **Feld:** *Auftrag*
    - **Kriterien:** Geben Sie eine durch Kommas getrennte Liste der Kundenauftragsnummern aus dem gewünschten Auftragssatz ein.

1. Wählen Sie **OK** aus, um Ihre Anfrage zu speichern.
1. Wählen Sie **OK** aus, um das Verfahren *Automatische Freigabe an das Lager* zu starten.

#### <a name="review-the-shipment-that-is-created-or-updated"></a>Überprüfen Sie die Lieferung, die erstellt oder aktualisiert wurde

1. Gehen Sie zu **Lagerortverwaltung \> Lieferungen \> Alle Lieferungen**.
1. Suchen Sie die gewünschte Lieferung und wählen Sie sie aus.
1. Wenn beim Erstellen oder Aktualisieren der Lieferung eine Konsolidierungsrichtlinie verwendet wurde, sollte diese im Feld **Richtlinie für Lieferungskonsolidierung** angezeigt werden.

### <a name="release-sales-orders-from-order-set-1"></a>Kundenaufträge aus Auftragssatz 1 freigeben

Folgen Sie dem [Grundlegenden Verfahren für die Freigabe an das Lager](#release-procedure), um die Kundenaufträge aus dem Auftragssatz 1 freizugeben.

Wenn Sie fertig sind, sollten Sie sehen, dass zwei Lieferungen erstellt wurden:

- Die erste Lieferung enthält drei Zeilen und wurde mit der *CustomerMode*-Lieferungskonsolidierungsrichtlinie erstellt.
- Die zweite Lieferung, die nicht *Airways* als Transportart der Lieferung verwendet, wurde unter Verwendung der *CustomerOrderNo*-Lieferungskonsolidierungsrichtlinie erstellt.

### <a name="release-sales-orders-from-order-set-2"></a>Kundenaufträge aus Auftragssatz 2 freigeben

Folgen Sie dem [Grundlegenden Verfahren für die Freigabe an das Lager](#release-procedure), um die Kundenaufträge aus dem Auftragssatz 2 freizugeben.

Wenn Sie fertig sind, sollten Sie sehen, dass drei Lieferungen erstellt wurden:

- Die erste Lieferung enthält die *Brennbar*-Artikel.
- Jede der beiden anderen Lieferungen enthält eine Position mit dem *Explosiv*-Artikel.

### <a name="release-sales-orders-from-order-set-3"></a>Kundenaufträge aus Auftragssatz 3 freigeben

Folgen Sie dem [Grundlegenden Verfahren für die Freigabe an das Lager](#release-procedure), um die Kundenaufträge aus dem Auftragssatz 3 freizugeben.

Wenn Sie fertig sind, sollten Sie sehen, dass die folgenden Aktionen ausgeführt wurden:

- Eine vorhandene Lieferung (die Lieferung, die erstellt wurde, als Auftragssatz 2 für das Lager freigegeben wurde) wurde aktualisiert. Eine Zeile mit dem *Brennbar*-Artikel wurde hinzugefügt.
- Es wurde eine neue Lieferung erstellt, die die *Explosiv*-Artikel enthält.

### <a name="release-sales-orders-from-order-set-4"></a>Kundenaufträge aus Auftragssatz 4 freigeben

Folgen Sie dem [Grundlegenden Verfahren für die Freigabe an das Lager](#release-procedure), um die Kundenaufträge aus dem Auftragssatz 4 freizugeben.

Wenn Sie fertig sind, sollten Sie sehen, dass eine vorhandene Lieferung (wo das **Debitorenanforderung**-Feld auf *1* gesetzt ist) aktualisiert wurde. Eine neue Zeile wurde hinzugefügt.

### <a name="release-sales-orders-from-order-set-5"></a>Kundenaufträge aus Auftragssatz 5 freigeben

Folgen Sie dem [Grundlegenden Verfahren für die Freigabe an das Lager](#release-procedure), um die Kundenaufträge aus dem Auftragssatz 5 freizugeben.

Wenn Sie fertig sind, sollten Sie sehen, dass die folgenden Aktionen ausgeführt wurden:

- Eine vorhandene Lieferung (wo das **Debitorenanforderung**-Feld auf *1* gesetzt ist) wurde aktualisiert. Eine Zeile aus Kundenauftrag 5-3 (wo das **Kundenanforderung**-Feld auf *1* gesetzt ist) wurde hinzugefügt.
- Eine neue Lieferung wurde erstellt, in der die Zeilen aus den Kundenaufträgen 5-1 und 5-2 zu einer Lieferung zusammengefasst sind.

### <a name="release-sales-orders-from-order-set-6"></a>Kundenaufträge aus Auftragssatz 6 freigeben

Folgen Sie dem [Grundlegenden Verfahren für die Freigabe an das Lager](#release-procedure), um die Kundenaufträge aus dem Auftragssatz 6 freizugeben.

Wenn Sie fertig sind, sollten Sie sehen, dass vier Lieferungen erstellt wurden:

- Positionen aus zwei Bestellungen für Debitor *US-003* wurden unter Verwendung der *Auftragspool*-Lieferungskonsolidierungsrichtlinie zu einer Lieferung zusammengefasst.
- Positionen aus zwei Bestellungen für Debitor *US-004* wurden unter Verwendung der *Auftragspool*-Lieferungskonsolidierungsrichtlinie zu einer Lieferung zusammengefasst.
- Positionen aus aus den Aufträgen 6-5 und 6-6 für Debitor *US-007* wurden unter Verwendung der *Auftragspool*-Lieferungskonsolidierungsrichtlinie zu einer Lieferung zusammengefasst.
- Positionen aus aus den Aufträgen 6-7 und 6-8 für Debitor *US-007* wurden unter Verwendung der *CrossOrder*-Lieferungskonsolidierungsrichtlinie zu einer Lieferung zusammengefasst.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Lieferungskonsolidierungsrichtlinien](about-shipment-consolidation-policies.md)
- [Richtlinien zur Lieferungskonsolidierung konfigurieren](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]