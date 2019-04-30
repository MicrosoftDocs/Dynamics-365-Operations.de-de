---
title: Bestandsumlagerungen und Regulierungen von Field Service mit Finance and Operations synchronisieren
description: In diesem Thema werden die Vorlagen und die zugrunde liegenden Aufgaben erläutert, die zur Synchronisierung von Bestandsanpassungen und Übertragungen von Microsoft Dynamics 365 for Finance and Operations auf Microsoft Dynamics 365 for Field Service verwendet werden.
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 75181661c41d238cdc06ffbb6969a2efd7d88d46
ms.sourcegitcommit: a6d385db6636ef2b7fb6b24d37a2160c8d5a3c0f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/14/2019
ms.locfileid: "842414"
---
# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a>Bestandsumlagerungen und Regulierungen von Field Service mit Finance and Operations synchronisieren

[!include[banner](../includes/banner.md)]

In diesem Thema werden die Vorlagen und die zugrunde liegenden Aufgaben erläutert, die zur Synchronisierung von Bestandsanpassungen und Übertragungen von Microsoft Dynamics 365 for Finance and Operations auf Microsoft Dynamics 365 for Field Service verwendet werden.

[![Synchronisierung von Geschäftsprozessen zwischen Finance and Operations und Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)

## <a name="templates-and-tasks"></a>Vorlagen und Aufgaben
Die folgende Vorlage und die zugrunde liegenden Aufgaben werden verwendet, um Bestandsanpassungen und Übertragungen von Microsoft Dynamics 365 for Field Service auf Microsoft Dynamics 365 for Finance and Operations zu synchronisieren.

**Vorlagen in der Datenintegration**
- Bestandregulierung (Field Service zu Finance and Operations)
- Bestandübertragung (Field Service zu Finance and Operations)

**Aufgaben im Datenintegrationsprojekt**
- Lagerbestandsregulierungen
- Lagerumlagerungen

## <a name="entity-set"></a>Entitätssatz
| Field Service                     | Finance and Operations                             |
|-----------------------------------|----------------------------------------------------|
| msdyn_inventoryadjustmentproducts |   Kopfzeilen und Positionen zur CDS-Bestandsanpassungserfassung |
| msdyn_inventoryadjustmentproducts | Kopfzeilen und Positionen zur CDS-Bestandsübertragungserfassung   |

## <a name="entity-flow"></a>Entitätsfluss
Bestandsanpassungen und Umbuchungen in Field Service werden mit Finance and Operations synchronisiert, nachdem sich der **Buchungsstatus** von **Erstellt** auf **Gebucht** geändert hat. In diesem Fall wird die Anpassung oder der Transportauftrag gesperrt und wird schreibgeschützt. Dies bedeutet, dass Korrekturen und Umbuchungen in Finance and Operations gebucht werden können, aber nicht geändert werden können. In Finance and Operations können Sie einen Batch-Job einrichten, um die bei der Integration erzeugten Korrekturen und Transferbestandsjournale automatisch zu buchen. In den folgenden Voraussetzungen erfahren Sie, wie Sie den Batch-Job aktivieren können.

## <a name="field-service-crm-solution"></a>Field Service CRM-Lösung 
Das Feld **Bestandseinheit** wurde der **Produktentität** hinzugefügt. Dieses Feld wird benötigt, da die Verkaufs- und Lagereinheit in Finance and Operations nicht immer gleich ist und die Lagereinheit für den Lagerbestand in Finance and Operations benötigt wird.
Wenn Sie das Produkt auf einem Bestandskorrekturprodukt sowohl für Bestandskorrekturen als auch für Bestandsumlagerungen einstellen, wird die Einheit aus dem Bestandsproduktwert geholt. Wenn ein Wert gefunden wird, wird das Feld **Einheit** für das Bestandskorrekturprodukt gesperrt.

Das Feld **Buchungsstatus** wurde sowohl bei der **Bestandskorrektureinheit** als auch bei der **Bestandsumlagerungseinheit** hinzugefügt. Dieses Feld wird als Filter verwendet, wenn eine Anpassung oder Übertragung an Finance and Operations gesendet wird. Der Standard für dieses Feld ist Erstellt (1), es wird jedoch nicht an Finance and Operations gesendet. Wenn Sie den Wert auf Gebucht (2) aktualisieren, wird er an Finance and Operations gesendet, aber danach können Sie die Anpassung nicht mehr ändern, übertragen oder neue Zeilen hinzufügen.

Die Entität **Bestandskorrekturprodukt** wurde um das Feld **Nummernfolge** erweitert. Dieses Feld stellt sicher, dass die Integration eine eindeutige Nummer hat, damit die Integration den Abgleich erstellen und aktualisieren kann. Wenn Sie Ihr erstes Bestandsanpassungsprodukt erstellen, erstellt es einen neuen Datensatz in der Entität **P2C AutoNumber**, um die Nummernkreise und das verwendete Präfix zu pflegen.

## <a name="prerequisites-and-mapping-setup"></a>Voraussetzungen und Zuordnungseinrichtung

### <a name="finance-and-operations"></a>Finance and Operations
Die Integrationslagererfassungen, die bei der Integration generiert werden, können mit einem Stapelverarbeitungslauf automatisch gebucht werden. Diese wird aktiviert von: **Lagerverwaltung > periodische Aufgaben > CD-Integration > Beitragsintegrationslagererfassungen**

## <a name="template-mapping-in-data-integration"></a>Vorlagenzuordnung in Datenintegration

Die folgenden Abbildungen zeigen die Vorlagenzuordnung in Datenintegration.

### <a name="inventory-adjustment-field-service-to-fin-and-ops-inventory-adjustment"></a>Bestandregulierung (Field Service zu Finance and Operations): Bestandregulierung

[![Vorlagenzuordnung in Datenintegration](./media/FSAdj1.png)](./media/FSAdj1.png)


### <a name="inventory-transfer-field-service-to-fin-and-ops-inventory-transfer"></a>Bestandandübertragung (Field Service zu Finance and Operations): Bestandübertragung

[![Vorlagenzuordnung in Datenintegration](./media/FSTrans1.png)](./media/FSTrans1.png)
