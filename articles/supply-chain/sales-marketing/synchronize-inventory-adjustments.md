---
title: Bestandsumlagerungen und Regulierungen von Field Service mit Supply Chain Management synchronisieren
description: In diesem Thema werden die Vorlagen und die zugrunde liegenden Aufgaben erläutert, die zur Synchronisierung von Bestandsanpassungen und Übertragungen von Dynamics 365 Supply Chain Management auf Dynamics 365 Field Service verwendet werden.
author: ChristianRytt
manager: AnnBe
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: c989e6efff88768f0b370fc81eea971c5c11bcef
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251633"
---
# <a name="synchronize-inventory-adjustments-from-field-service-to-supply-chain-management"></a>Bestandsanpassungen von Field Service mit Supply Chain Management synchronisieren

[!include[banner](../includes/banner.md)]

In diesem Thema werden die Vorlagen und die zugrunde liegenden Aufgaben erläutert, die zur Synchronisierung von Bestandsanpassungen und Übertragungen von Dynamics 365 Supply Chain Management auf Dynamics 365 Field Service verwendet werden.

[![Synchronisierung von Geschäftsprozessen zwischen Supply Chain Management und Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)

## <a name="templates-and-tasks"></a>Vorlagen und Aufgaben
Die folgende Vorlage und die zugrunde liegenden Aufgaben werden verwendet, um Bestandsanpassungen und Übertragungen von Field Service zu Supply Chain Management zu synchronisieren.

**Vorlagen in der Datenintegration**
- Bestandsanpassung (Field Service zu Supply Chain Management)
- Bestandsübertragung (Field Service zu Supply Chain Management)

**Aufgaben im Datenintegrationsprojekt**
- Lagerbestandsregulierungen
- Lagerumlagerungen

## <a name="entity-set"></a>Entitätssatz
| Field Service                     | Lieferkettenverwaltung                          |
|-----------------------------------|----------------------------------------------------|
| msdyn_inventoryadjustmentproducts |   Kopfzeilen und Positionen zur CDS-Bestandsanpassungserfassung |
| msdyn_inventoryadjustmentproducts | Kopfzeilen und Positionen zur CDS-Bestandsübertragungserfassung   |

## <a name="entity-flow"></a>Entitätsfluss
Bestandsanpassungen und Umbuchungen in Field Service werden mit Supply Chain Management synchronisiert, nachdem sich der **Buchungsstatus** von **Erstellt** auf **Gebucht** geändert hat. In diesem Fall wird die Anpassung oder der Transportauftrag gesperrt und wird schreibgeschützt. Dies bedeutet, dass Korrekturen und Umbuchungen in Supply Chain Management gebucht werden können, aber nicht geändert werden können. In Supply Chain Management können Sie einen Batch-Job einrichten, um die bei der Integration erzeugten Korrekturen und Transferbestandsjournale automatisch zu buchen. In den folgenden Voraussetzungen erfahren Sie, wie Sie den Batch-Job aktivieren können.

## <a name="field-service-crm-solution"></a>Field Service CRM-Lösung 
Das Feld **Bestandseinheit** wurde der **Produktentität** hinzugefügt. Dieses Feld wird benötigt, da die Verkaufs- und Lagereinheit in Supply Chain Management nicht immer gleich ist und die Lagereinheit für den Lagerbestand in Supply Chain Management benötigt wird.
Wenn Sie das Produkt auf einem Bestandskorrekturprodukt sowohl für Bestandskorrekturen als auch für Bestandsumlagerungen einstellen, wird die Einheit aus dem Bestandsproduktwert geholt. Wenn ein Wert gefunden wird, wird das Feld **Einheit** für das Bestandskorrekturprodukt gesperrt.

Das Feld **Buchungsstatus** wurde sowohl bei der **Bestandskorrektureinheit** als auch bei der **Bestandsumlagerungseinheit** hinzugefügt. Dieses Feld wird als Filter verwendet, wenn eine Anpassung oder Übertragung an Supply Chain Management gesendet wird. Der Standard für dieses Feld ist Erstellt (1), es wird jedoch nicht an Supply Chain Management gesendet. Wenn Sie den Wert auf Gebucht (2) aktualisieren, wird er an Supply Chain Management gesendet, aber danach können Sie die Anpassung nicht mehr ändern, übertragen oder neue Zeilen hinzufügen.

Die Entität **Bestandskorrekturprodukt** wurde um das Feld **Nummernfolge** erweitert. Dieses Feld stellt sicher, dass die Integration eine eindeutige Nummer hat, damit die Integration den Abgleich erstellen und aktualisieren kann. Wenn Sie Ihr erstes Bestandsanpassungsprodukt erstellen, erstellt es einen neuen Datensatz in der Entität **P2C AutoNumber**, um die Nummernkreise und das verwendete Präfix zu pflegen.

## <a name="prerequisites-and-mapping-setup"></a>Voraussetzungen und Zuordnungseinrichtung

### <a name="supply-chain-management"></a>Lieferkettenverwaltung
Die Integrationslagererfassungen, die bei der Integration generiert werden, können mit einem Stapelverarbeitungslauf automatisch gebucht werden. Diese wird aktiviert von: **Lagerverwaltung > periodische Aufgaben > CD-Integration > Beitragsintegrationslagererfassungen**

## <a name="template-mapping-in-data-integration"></a>Vorlagenzuordnung in Datenintegration

Die folgenden Abbildungen zeigen die Vorlagenzuordnung in Datenintegration.

### <a name="inventory-adjustment-field-service-to-supply-chain-management-inventory-adjustment"></a>Lagerregulierung (Field Service zu Supply Chain Management): Lagerregulierung

[![Vorlagenzuordnung in Datenintegration](./media/FSAdj1.png)](./media/FSAdj1.png)


### <a name="inventory-transfer-field-service-to-supply-chain-management-inventory-transfer"></a>Lagerumlagerung (Field Service zu Supply Chain Management): Lagerumlagerung

[![Vorlagenzuordnung in Datenintegration](./media/FSTrans1.png)](./media/FSTrans1.png)
