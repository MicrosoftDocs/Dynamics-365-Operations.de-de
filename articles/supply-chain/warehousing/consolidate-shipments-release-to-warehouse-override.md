---
title: Lieferungen konsolidieren, wenn die Richtlinie zur Lieferungskonsolidierung auf der Seite „Freigabe an Lager“ überschrieben wird
description: In diesem Thema wird ein Szenario vorgestellt, in dem eine oder mehrere Verkaufspositionen von der Seite „Freigabe an Lager“ manuell an das Lager freigegeben werden müssen und die systemdefinierte Lieferungskonsolidierungsrichtlinie vor der Freigabe überschrieben werden muss.
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
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 406ff268eede4a9d448b3b9c1729a00fcec8f21e
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986743"
---
# <a name="consolidate-shipments-when-the-shipment-consolidation-policy-is-overridden-from-the-release-to-warehouse-page"></a>Lieferungen konsolidieren, wenn die Richtlinie zur Lieferungskonsolidierung auf der Seite „Freigabe an Lager“ überschrieben wird

[!include [banner](../includes/banner.md)]

In diesem Thema wird ein Szenario vorgestellt, in dem eine oder mehrere Verkaufspositionen von der Seite **Freigabe an Lager** manuell an das Lager freigegeben werden müssen und die systemdefinierte Lieferungskonsolidierungsrichtlinie vor der Freigabe überschrieben werden muss. Eine Überschreibung der Lieferungskonsolidierungsrichtlinie kann erforderlich sein, wenn beispielsweise ein Auftrag, der normalerweise nicht mit offenen Lieferungen konsolidiert wird, mit offenen Lieferungen konsolidiert werden muss.

Während des Szenarios erstellen Sie eine Reihe von Aufträgen und überschreiben dann die Standardrichtlinie für die Lieferungskonsolidierung, bevor Sie die Aufträge an das Lager freigeben.

## <a name="make-demo-data-available"></a>Demodaten zur Verfügung stellen

Das Szenario in diesem Thema verweist auf Werte und Datensätze, die in den für Microsoft Dynamics 365 Supply Chain Management bereitgestellten Standarddemodaten enthalten sind. Wenn Sie die hier angegebenen Werte während der Übungen verwenden möchten, müssen Sie in einer Umgebung arbeiten, in der die Demodaten installiert sind, und die juristische Person auf **USMF** festlegen, bevor Sie beginnen.

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a>Richten Sie Richtlinien zur Lieferungskonsolidierung und Produktfilter ein

In dem hier beschriebenen Szenario wird davon ausgegangen, dass Sie die Funktion bereits aktiviert und die Übungen in [Richtlinien zur Lieferungskonsolidierung konfigurieren](configure-shipment-consolidation-policies.md) ausgeführt haben und die dort beschriebenen Richtlinien und anderen Datensätze erstellt haben. Stellen Sie sicher, dass Sie diese Übungen ausführen, bevor Sie mit diesem Szenario fortfahren.

## <a name="create-the-sales-orders-for-this-scenario"></a>Erstellen Sie die Kundenaufträge für dieses Szenario

1. Wechseln Sie zu **Debitoren \> Aufträge \> Alle Aufträge**, und erstellen Sie drei identische Aufträge mit den folgenden Einstellungen:

    - **Debitorenkonto:** *US-002*

1. Eine Auftragsposition hat die folgenden Einstellungen:

    - **Artikelnummer:** *A0001* (ein Artikel, dem kein **Code 4**-Filter zugeordnet ist)
    - **Menge** *1.00*

1. Wählen Sie **Lager \> Reservierung** und dann im Aktionsbereich die Option **Los reservieren** aus, um die Bestellposition zu reservieren.

## <a name="release-the-sales-orders-from-the-release-to-warehouse-page"></a>Geben Sie die Aufträge von der Seite „Freigabe an Lager“ frei

Befolgen Sie diese Schritte, um die Lieferungskonsolidierungsrichtlinie während der Freigabe an das Lager zu überschreiben.

1. Wechseln Sie zu **Lagerortverwaltung \> An Lager freigeben \> An Lager freigeben**.
1. Wählen Sie im oberen Bereich den ersten Auftrag aus, den Sie für dieses Szenario erstellt haben.
1. Wählen Sie **Hinzufügen** aus, um die Position zur Freigabe zum Lager hinzuzufügen. Beachten Sie, dass die *Standard*-Lieferungskonsolidierungsrichtlinie im unteren Bereich angewendet wird.
1. Wählen Sie im unteren Bereich **Neue Lieferungskonsolidierungsrichtlinie auswählen** aus.
1. Wählen Sie eine Richtlinie aus, die eine Konsolidierung mit anderen offenen Lieferungen derselben Richtlinie ermöglicht. Wählen Sie zum Beispiel die *CustomerOrderNo*-Richtlinie aus.
1. Wählen Sie **An Lager freigeben** aus.
1. Wählen Sie im oberen Bereich den zweiten und dritten Auftrag aus, die Sie für dieses Szenario erstellt haben.
1. Wählen Sie **Hinzufügen** aus, um die Positionen zur Freigabe zum Lager hinzuzufügen. Beachten Sie, dass die *Standard*-Richtlinie im unteren Bereich angewendet wird.
1. Wählen Sie die zweite Zeile Position und dann im Feld **Neue Lieferungskonsolidierungsrichtlinie auswählen** die *CustomerOrderNo*-Richtlinie aus.
1. Wählen Sie **An Lager freigeben** für beide Positionen aus.

## <a name="verify-the-shipments"></a>Überprüfen Sie die Lieferungen

Es sollten zwei Lieferungen erstellt worden sein:

- Die erste Lieferung enthält zwei Zeilen und wurde mit der *CustomerOrderNo*-Lieferungskonsolidierungsrichtlinie erstellt.
- Die zweite Lieferung enthält eine Position und wurde mit der *Standard*-Lieferungskonsolidierungsrichtlinie erstellt.

Befolgen Sie diese Schritte, um die erstellten Lieferungen zu überprüfen.

1. Gehen Sie zu **Lagerortverwaltung \> Lieferungen \> Alle Lieferungen**.
1. Suchen Sie die gewünschte Lieferung und wählen Sie sie aus.
1. Überprüfen Sie die Konsolidierungsrichtlinie, die verwendet wurde, als die Lieferung erstellt wurde, im Feld **Richtlinie für Lieferungskonsolidierung**.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Lieferungskonsolidierungsrichtlinien](about-shipment-consolidation-policies.md)
- [Richtlinien zur Lieferungskonsolidierung konfigurieren](configure-shipment-consolidation-policies.md)
