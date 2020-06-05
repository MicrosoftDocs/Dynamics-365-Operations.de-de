---
title: Lieferungen manuell auf der Seite zur Lieferungskonsolidierung konsolidieren
description: In diesem Thema wird ein Szenario vorgestellt, in dem mehrere Aufträge an das Lager freigegeben werden und anschließend später auf der Lieferungskonsolidierungsseite konsolidiert werden.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: v-olbara
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: acc6e1d09894b57d2bb063bacbcddef239c1a8bd
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383774"
---
# <a name="consolidate-shipments-manually-by-using-the-consolidate-shipments-page"></a>Lieferungen manuell auf der Seite zur Lieferungskonsolidierung konsolidieren

[!include [banner](../includes/banner.md)]

In diesem Thema wird ein Szenario vorgestellt, in dem mehrere Aufträge an das Lager freigegeben werden und anschließend später auf der Seite **Lieferungskonsolidierung** konsolidiert werden.

## <a name="make-demo-data-available"></a>Demodaten zur Verfügung stellen

Das Szenario in diesem Thema verweist auf Werte und Datensätze, die in den für Microsoft Dynamics 365 Supply Chain Management bereitgestellten Standarddemodaten enthalten sind. Wenn Sie die hier angegebenen Werte während der Übungen verwenden möchten, müssen Sie in einer Umgebung arbeiten, in der die Demodaten installiert sind, und die juristische Person auf **USMF** festlegen, bevor Sie beginnen.

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a>Richten Sie Richtlinien zur Lieferungskonsolidierung und Produktfilter ein

In dem hier beschriebenen Szenario wird davon ausgegangen, dass Sie die Funktion bereits aktiviert und die Übungen in [Richtlinien zur Lieferungskonsolidierung konfigurieren](configure-shipment-consolidation-policies.md) ausgeführt haben und die dort beschriebenen Richtlinien und anderen Datensätze erstellt haben. Stellen Sie sicher, dass Sie diese Übungen ausführen, bevor Sie mit diesem Szenario fortfahren.

## <a name="create-the-sales-orders-for-this-scenario"></a>Erstellen Sie die Kundenaufträge für dieses Szenario

Erstellen Sie zunächst eine Sammlung von Kundenaufträgen, mit denen Sie arbeiten können. Sie müssen mit einem Lagerort arbeiten, der für WMS-Prozesse (Advanced Warehouse) aktiviert ist. Sofern nicht ausdrücklich ein anderes Lager erwähnt wird, muss dasselbe Lager für jeden der folgenden Auftragssätze verwendet werden.

Wechseln Sie zu **Debitoren \> Aufträge \> Alle Kundenaufträge**, und erstellen Sie eine Sammlung von Kundenaufträgen mit den Einstellungen, die in den folgenden Unterabschnitten beschrieben werden.

### <a name="create-sales-orders-1-and-2"></a>Aufträge 1 und 2 erstellen

1. Erstellen Sie zwei identische Aufträge mit den folgenden Einstellungen:

    - **Debitorenkonto:** *US-007*
    - **Pool:** *ShipCons*

1. Eine Auftragsposition hat die folgenden Einstellungen:

    - **Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)
    - **Menge** *1.00*

1. Wählen Sie **Lager \> Reservierung** und dann im Aktionsbereich die Option **Los reservieren** aus, um die Bestellposition zu reservieren.

### <a name="create-sales-orders-3-and-4"></a>Aufträge 3 und 4 erstellen

1. Erstellen Sie zwei identische Aufträge mit den folgenden Einstellungen:

    - **Debitorenkonto:** *US-007*
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

## <a name="consolidate-shipments"></a>Lieferungen konsolidieren

1. Gehen Sie zu **Lagerortverwaltung \> Lieferungen \> Alle Lieferungen**.
1. Suchen und wählen Sie eine Lieferung aus, die erstellt wurde, als Kundenauftrag 1 für das Lager freigegeben wurde. (Das **Lieferungskonsolidierungsrichtlinie**-Feld sollte auf *Auftragspool* gesetzt sein.)
1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lieferungen** auf **Lieferungen \> Lieferungen konsolidieren**.
1. Überprüfen Sie die Lieferungen, die zur Konsolidierung vorgeschlagen werden. Für die Konsolidierung sollte nur eine Lieferung mit derselben Richtlinie vorgeschlagen werden.
1. Schließen Sie die Seite **Lieferungskonsolidierung**.
1. Suchen und wählen Sie eine Lieferung aus, die erstellt wurde, als Kundenauftrag 3 für das Lager freigegeben wurde. (Das **Lieferungskonsolidierungsrichtlinie**-Feld sollte auf *Standard* gesetzt sein.)
1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lieferungen** auf **Lieferungen \> Lieferungen konsolidieren**.
1. Überprüfen Sie, dass keine Lieferungen zur Konsolidierung vorgeschlagen werden.
1. Wählen Sie **Filter anzeigen** aus.
1. Entfernen Sie im **Filter**-Bereich den Filter **Auftragsnummer** und wählen Sie dann **Anwenden** aus.
1. Überprüfen Sie die Lieferungen, die zur Konsolidierung vorgeschlagen werden. Für die Konsolidierung sollte nur eine Lieferung mit derselben Richtlinie vorgeschlagen werden.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Lieferungskonsolidierungsrichtlinien](about-shipment-consolidation-policies.md)
- [Richtlinien zur Lieferungskonsolidierung konfigurieren](configure-shipment-consolidation-policies.md)