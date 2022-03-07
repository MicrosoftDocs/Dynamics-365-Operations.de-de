---
title: Bestandsumlagerungen und Regulierungen von Field Service mit Supply Chain Management synchronisieren
description: In diesem Thema werden die Vorlagen und die zugrunde liegenden Aufgaben erläutert, die zur Synchronisierung von Bestandsanpassungen und Übertragungen von Dynamics 365 Supply Chain Management auf Dynamics 365 Field Service verwendet werden.
author: Henrikan
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: henrikan
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: cfa7f617cbc4cd75d669972b35f8d33ba3cbcc56
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8061678"
---
# <a name="synchronize-inventory-transfers-and-adjustments-from-field-service-to-supply-chain-management"></a>Bestandsumlagerungen und Regulierungen von Field Service mit Supply Chain Management synchronisieren

[!include[banner](../includes/banner.md)]



In diesem Thema werden die Vorlagen und die zugrunde liegenden Aufgaben erläutert, die zur Synchronisierung von Bestandsanpassungen und Übertragungen von Dynamics 365 Supply Chain Management auf Dynamics 365 Field Service verwendet werden.

[![Synchronisierung von Geschäftsprozessen zwischen Supply Chain Management und Field Service.](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)

## <a name="templates-and-tasks"></a>Vorlagen und Aufgaben
Die folgende Vorlage und die zugrunde liegenden Aufgaben werden verwendet, um Bestandsanpassungen und Übertragungen von Field Service zu Supply Chain Management zu synchronisieren.

**Vorlagen in der Datenintegration**
- Bestandsanpassung (Field Service zu Supply Chain Management)
- Bestandsübertragung (Field Service zu Supply Chain Management)

**Aufgaben im Datenintegrationsprojekt**
- Lagerbestandsregulierungen
- Lagerumlagerungen

## <a name="table-set"></a>Tabellensatz
| Field Service                     | Lieferkettenverwaltung                          |
|-----------------------------------|----------------------------------------------------|
| msdyn_inventoryadjustmentproducts | Kopfzeilen und Positionen zur Dataverse-Bestandsanpassungserfassung |
| msdyn_inventoryadjustmentproducts | Kopfzeilen und Positionen zur Dataverse-Bestandsübertragungserfassung   |

## <a name="table-flow"></a>Tabellenfluss
Bestandsanpassungen und Umbuchungen in Field Service werden mit Supply Chain Management synchronisiert, nachdem sich der **Buchungsstatus** von **Erstellt** auf **Gebucht** geändert hat. In diesem Fall wird die Anpassung oder der Transportauftrag gesperrt und wird schreibgeschützt. Dies bedeutet, dass Korrekturen und Umbuchungen in Supply Chain Management gebucht werden können, aber nicht geändert werden können. In Supply Chain Management können Sie einen Batch-Job einrichten, um die bei der Integration erzeugten Korrekturen und Transferbestandsjournale automatisch zu buchen. In den folgenden Voraussetzungen erfahren Sie, wie Sie den Batch-Job aktivieren können.

## <a name="field-service-crm-solution"></a>Field Service CRM-Lösung 
Die Spalte **Bestandseinheit** wurde der Tabelle **Produkt** hinzugefügt. Diese Spalte wird benötigt, da die Verkaufs- und Bestandseinheit in Supply Chain Management nicht immer gleich ist und die Bestandseinheit für den Lagerortbestand in Supply Chain Management benötigt wird.
Wenn Sie das Produkt auf einem Bestandskorrekturprodukt sowohl für Bestandskorrekturen als auch für Bestandsumlagerungen einstellen, wird die Einheit aus dem Bestandsproduktwert geholt. Wenn ein Wert gefunden wird, wird die Spalte **Einheit** für das Bestandskorrekturprodukt gesperrt.

Die Spalte **Buchungsstatus** wurde sowohl der Tabelle **Bestandsregulierung** als auch der Tabelle **Bestandsumlagerung** hinzugefügt. Diese Spalte wird als Filter verwendet, wenn eine Anpassung oder Übertragung an Supply Chain Management gesendet wird. Der Standard für diese Spalte ist „Erstellt (1)“, er wird jedoch nicht an Supply Chain Management gesendet. Wenn Sie den Wert auf Gebucht (2) aktualisieren, wird er an Supply Chain Management gesendet, aber danach können Sie die Anpassung nicht mehr ändern, übertragen oder neue Zeilen hinzufügen.

Die Spalte **Nummernkreis** wurde zur Tabelle **Bestandskorrekturprodukt** hinzugefügt. Diese Spalte stellt sicher, dass die Integration eine eindeutige Nummer hat, damit die Integration den Abgleich erstellen und aktualisieren kann. Wenn Sie Ihr erstes Bestandsanpassungsprodukt erstellen, erstellt es einen neuen Datensatz in der Tabelle **P2C AutoNumber**, um die Nummernkreise und das verwendete Präfix zu pflegen.

## <a name="prerequisites-and-mapping-setup"></a>Voraussetzungen und Zuordnungseinrichtung

### <a name="supply-chain-management"></a>Lieferkettenverwaltung
Die Integrationslagererfassungen, die bei der Integration generiert werden, können mit einem Stapelverarbeitungslauf automatisch gebucht werden. Diese wird aktiviert über **Bestandsverwaltung > Periodische Aufgaben > Dataverse-Integration > Bestandserfassung nach Integration**.

## <a name="template-mapping-in-data-integration"></a>Vorlagenzuordnung in Datenintegration

Die folgenden Abbildungen zeigen die Vorlagenzuordnung in Datenintegration.

### <a name="inventory-adjustment-field-service-to-supply-chain-management-inventory-adjustment"></a>Lagerregulierung (Field Service zu Supply Chain Management): Lagerregulierung

[![Vorlagenzuordnung in der Datenintegration, Bestandsanpassung (Field Service zu Supply Chain Management): Bestandsanpassung](./media/FSAdj1.png)](./media/FSAdj1.png)


### <a name="inventory-transfer-field-service-to-supply-chain-management-inventory-transfer"></a>Lagerumlagerung (Field Service zu Supply Chain Management): Lagerumlagerung

[![Vorlagenzuordnung in der Datenintegration, Bestandsübertragung (Field Service zu Supply Chain Management): Bestandsübertragung.](./media/FSTrans1.png)](./media/FSTrans1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]