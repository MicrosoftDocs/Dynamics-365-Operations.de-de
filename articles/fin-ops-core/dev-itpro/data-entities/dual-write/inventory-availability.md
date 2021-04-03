---
title: Inventarverfügbarkeit in dualem Schreiben
description: Dieses Thema bietet Informationen zum Prüfen der Bestandverfügbarkeit in dualem Schreiben.
author: yijialuan
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: 48e54c043967ea5db15938857bd8f020dd4dfc64
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5566738"
---
# <a name="inventory-availability-in-dual-write"></a>Inventarverfügbarkeit in dualem Schreiben

[!include [banner](../../includes/banner.md)]

Mithilfe der Bestandverfügbarkeit können Sie Ihr Inventar überprüfen, bevor Sie ein Produkt zu den Formularen **Zitate**, **Aufträge** oder **Rechnungen** in Microsoft Dynamics 365 Sales hinzufügen. Zum Beispiel ist die Überprüfung des Inventars und die Bestimmung eines Erfüllungstermins eine Schlüsselaufgabe in [Aussicht auf Bargeld](dual-write-prospect-to-cash.md) Prozess.

Wenn Sie nicht über genügend Bestand verfügen, können Sie einen Liefertermin basierend auf den projizierten Bestandeinnahmen und -Problemen schätzen. Sie können auch die ATP-Informationen des Produkts überprüfen, in denen Sie die ATP-Menge in dem vordefinierten Zeitrahmen finden.

## <a name="on-hand-inventory"></a>Verfügbarer Lagerbestand

In der Kopfzeile der Seiten **Angebote**, **Aufträge** und **Rechnungen** in Dynamics 365 Sales wurde eine neue Schaltfläche **Lagerbestand** hinzugefügt. Wenn Sie auf die Schaltfläche klicken, wird ein Dialogfeld angezeigt, in dem Sie das Unternehmen und das Produkt angeben können, für das Sie dann den Lagerbestand überprüfen möchten. Dieses Dialogfeld zeigt die gleichen Informationen wie [Lagerbestand](../../../../supply-chain/inventory/tasks/check-availability-stock.md).

Das Dialogfeld gibt die Inventarinformationen von Dynamics 365 Supply Chain Management zurück. Diese Informationen umfassen die folgenden Mengen:

- Verfügbare Menge
- Die verfügbare Menge in Reserve
- Die verfügbare Menge
- Bestellte Menge
- Die Auftragsmenge
- Reservierte bestellte Menge
- Die insgesamt verfügbare Menge

## <a name="atp-information"></a>VfZ-Informationen

In Sales wurde eine neue Schaltfläche **ATP-Informationen** wurde zu den Seite **Zitate**, **Aufträge**, und **Rechnungen** hinzugefügt. Wenn Sie auf diese Schaltfläche klicken, wird ein Dialogfeld angezeigt, in dem Sie das Unternehmen, Produkt, Lagerstandort, Lagerbestand und bestellte Menge angeben können.. Dieses Dialogfeld hat dieselben Einstellungen wie in [Bestellung vielversprechend](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).

Das Dialogfeld gibt die ATP-Informationen aus dem Supply Chain Management zurück. Diese Informationen umfassen die folgenden Mengen:

- VfZ-Menge
- Zugangsmenge
- Abgangsmenge
- Verfügbare Menge

## <a name="how-it-works"></a>Funktionsweise

Wenn Sie die Schaltfläche **Verfügbarer Bestand** auf der Seite **Angebote**, **Aufträge** oder **Rechnungen** auswählen, wird ein Live-Aufruf zum dualen Schreiben an die API **Verfügbarer Lagerbestand** durchgeführt. Die API berechnet den verfügbaren Lagerbestand für das jeweilige Produkt. Das Ergebnis wird in den Tabellen **InventCDSInventoryOnHandRequestEntity** und **InventCDSInventoryOnHandEntryEntity** gespeichert und dann mit dualem Schreiben in Dataverse geschrieben. Um diese Funktionalität nutzen zu können, müssen Sie die folgenden Zuordnungen für duales Schreiben ausführen. Überspringen Sie die anfängliche Synchronisierung, wenn Sie die Zuordnungen ausführen.

- Einträge zu verfügbarem CDS-Lagerbestand (msdyn_inventoryonhandentries)
- Anforderungen zu verfügbarem CDS-Lagerbestand (msdyn_inventoryonhandrequests)

## <a name="templates"></a>Vorlagen
Die folgenden Vorlagen stehen zur Verfügung, um die Daten zu vorhandenen Lagerbestand verfügbar zu machen.

Finance and Operations Apps | Customer Engagement-App | Beschreibung 
---|---|---
[Einträge für verfügbaren CDS-Bestand](#145) | msdyn_inventoryonhandentries |
[Anfragen für verfügbaren CDS-Bestand](#147) | msdyn_inventoryonhandrequests |

[!include [banner](../../includes/dual-write-symbols.md)]

###  <a name="cds-inventory-on-hand-entries-msdyn_inventoryonhandentries"></a><a name="145"></a>Einträge zu verfügbarem CDS-Lagerbestand (msdyn_inventoryonhandentries)

Diese Vorlage synchronisiert Daten zwischen Finance and Operations-Apps und Dataverse.

Finance and Operations-Feld | Zuordnungstyp | Customer Engagement-Feld | Standardwert
---|---|---|---
`REQUESTID` | = | `msdyn_request.msdyn_requestid` |
`INVENTORYSITEID` | = | `msdyn_inventorysite.msdyn_siteid` |
`INVENTORYWAREHOUSEID` | = | `msdyn_inventorywarehouse.msdyn_warehouseidentifier` |
`AVAILABLEONHANDQUANTITY` | > | `msdyn_availableonhandquantity` |
`AVAILABLEORDEREDQUANTITY` | > | `msdyn_availableorderedquantity` |
`ONHANDQUANTITY` | > | `msdyn_onhandquantity` |
`ONORDERQUANTITY` | > | `msdyn_onorderquantity` |
`ORDEREDQUANTITY` | > | `msdyn_orderedquantity` |
`RESERVEDONHANDQUANTITY` | > | `msdyn_reservedonhandquantity` |
`RESERVEDORDEREDQUANTITY` | > | `msdyn_reservedorderedquantity` |
`TOTALAVAILABLEQUANTITY` | > | `msdyn_totalavailablequantity` |
`ATPDATE` | = | `msdyn_atpdate` |
`ATPQUANTITY` | > | `msdyn_atpquantity` |
`PROJECTEDISSUEQUANTITY` | > | `msdyn_projectedissuequantity` |
`PROJECTEDONHANDQUANTITY` | > | `msdyn_projectedonhandquantity` |
`PROJECTEDRECEIPTQUANTITY` | > | `msdyn_projectedreceiptquantity` |
`ORDERQUANTITY` | > | `msdyn_orderquantity` |
`UNAVAILABLEONHANDQUANTITY` | > | `msdyn_unavailableonhandquantity` |

###  <a name="cds-inventory-on-hand-requests-msdyn_inventoryonhandrequests"></a><a name="147"></a>Anforderungen zu verfügbarem CDS-Lagerbestand (msdyn_inventoryonhandrequests)

Diese Vorlage synchronisiert Daten zwischen Finance and Operations-Apps und Dataverse.

Finance and Operations-Feld | Zuordnungstyp | Customer Engagement-Feld | Standardwert
---|---|---|---
`REQUESTID` | = | `msdyn_requestid` |
`PRODUCTNUMBER` | < | `msdyn_product.msdyn_productnumber` |
`ISATPCALCULATION` | << | `msdyn_isatpcalculation` |
`ORDERQUANTITY` | < | `msdyn_orderquantity` |
`INVENTORYSITEID` | < | `msdyn_inventorysite.msdyn_siteid` |
`INVENTORYWAREHOUSEID` | < | `msdyn_inventorywarehouse.msdyn_warehouseidentifier` |
`REFERENCENUMBER` | < | `msdyn_referencenumber` |
`LINECREATIONSEQUENCENUMBER` | < | `msdyn_linecreationsequencenumber` |






[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]