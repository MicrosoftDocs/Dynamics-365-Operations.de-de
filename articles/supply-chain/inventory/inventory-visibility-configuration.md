---
title: Konfiguration der Inventory Visibility
description: In diesem Thema wird beschrieben, wie Sie Inventory Visibility konfigurieren.
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 92e42b22d424ab80303d771f760cfcf0599b9f4c
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2021
ms.locfileid: "7345032"
---
# <a name="inventory-visibility-configuration"></a>Konfiguration der Inventory Visibility

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

In diesem Thema wird beschrieben, wie Sie Inventory Visibility konfigurieren.

## <a name="introduction"></a><a name="introduction"></a>Einführung

Bevor Sie mit Inventory Visibility arbeiten können, müssen Sie die folgende Konfiguration wie in diesem Thema beschrieben durchführen:

- [Datenquellenkonfiguration](#data-source-configuration)
- [Partitionskonfiguration](#partition-configuration)
- [Produktindex-Hierarchie-Konfiguration](#index-configuration)
- [Reservierungskonfiguration (optional)](#reservation-configuration)
- [Beispiel für die Standardkonfiguration](#default-configuration-sample)

> [!NOTE]
> Sie können Konfigurationen für Inventory Visibility in [Microsoft Power Apps](./inventory-visibility-power-platform.md#configuration) ansehen und bearbeiten. Nachdem die Konfiguration abgeschlossen ist, wählen Sie **Konfiguration aktualisieren** in der App.

## <a name="data-source-configuration"></a><a name="data-source-configuration"></a>Datenquellenkonfiguration

Die Datenquelle steht für das System, aus dem Ihre Daten stammen. Beispiele sind `fno` (was für "Dynamics 365 Finance and Operations Apps" steht) und `pos` (was für "Point of Sale" steht).

Die Datenquellenkonfiguration umfasst die folgenden Teile:

- Dimension (Zuordnung von Dimensionen)
- Physikalische Messung
- Berechnete Messung

> [!NOTE]
> Die Datenquelle `fno` ist für Dynamics 365 Supply Chain Management reserviert.

### <a name="dimension-dimension-mapping"></a><a name="data-source-configuration-dimension"></a>Dimension (Dimension Zuordnung)

Der Zweck der Dimensionskonfiguration ist die Standardisierung der Multisystem-Integration für Buchungsereignisse und Abfragen, basierend auf Dimensionskombinationen.

Inventory Visibility unterstützt die folgenden allgemeinen Basisdimensionen.

| Dimensionstyp | Basis-Dimensionen |
|---|---|
| Produkt | `ColorId` |
| Produkt | `SizeId` |
| Produkt | `StyleId` |
| Produkt | `ConfigId` |
| Nachverfolgung | `BatchId` |
| Nachverfolgung | `SerialId` |
| Speicherort | `LocationId` |
| Speicherort | `SiteId` |
| Bestandsstatus | `StatusId` |
| Lagerspezifisch | `WMSLocationId` |
| Lagerspezifisch | `WMSPalletId` |
| Lager spezifisch | `LicensePlateId` |
| Andere | `VersionId` |
| Bestand (angepasst) | `InventDimension1` bis `InventDimension12` |
| Erweiterung | `ExtendedDimension1` bis `ExtendedDimension8` |

> [!NOTE]
> Die Dimensionen, die in der vorangehenden Tabelle aufgeführt sind, dienen nur als Referenz. Sie müssen sie nicht in Inventory Visibility definieren.
>
> (Angepasste) Dimensionen für den Bestand können für das Supply Chain Management reserviert sein. In diesem Fall können Sie stattdessen die erweiterten Dimensionen verwenden.

Externe Systeme können über die RESTful-APIs von Inventory Visibility zugreifen. Für die Integration können Sie in Inventory Visibility die _externe Datenquelle_ und die Zuordnung von den _externen Dimensionen_ zu den _Basisdimensionen_ konfigurieren. Hier ist ein Beispiel für eine Tabelle zur Zuordnung von Dimensionen.

| Externe Dimension | Basis Dimensionen |
|---|---|
| `MyColorId` | `ColorId` |
| `MySizeId` | `SizeId` |
| `MyStyleId` | `StyleId` |
| `MyDimension1` | `ExtendedDimension1` |
| `MyDimension2` | `ExtendedDimension2` |

Indem Sie eine Zuordnung von Dimensionen konfigurieren, können Sie die externen Dimensionen direkt an Inventory Visibility senden. Inventory Visibility wandelt dann die externen Dimensionen automatisch in Basisdimensionen um.

### <a name="physical-measures"></a>Physikalische Messungen

Physikalische Messungen verändern die Menge und spiegeln den Status des Bestands wider. Sie können Ihre eigenen physikalischen Messungen, basierend auf Ihren Anforderungen, definieren.

Inventory Visibility bietet eine Liste von standardmäßigen physikalischen Messungen, die mit Supply Chain Management (der Datenquelle `fno`) verknüpft sind. Die folgende Tabelle enthält ein Beispiel für physikalische Messungen.

| Name der physikalischen Messung | Beschreibung |
|---|---|
| `NotSpecified` | Nicht angegeben |
| `Arrived` | Angekommen |
| `AvailOrdered` | Verfügbar Bestellt |
| `AvailPhysical` | Physisch verfügbar |
| `Deducted` | Abgesetzt |
| `OnOrder` | BeiBestellung |
| `Ordered` | Bestellt |
| `PhysicalInvent` | Physischer Bestand |
| `Picked` | Entnommen |
| `PostedQty` | Gebuchte Menge |
| `QuotationIssue` | Angebotsabgang |
| `QuotationReceipt` | Angebotszugang |
| `Received` | Eingegangen |
| `Registered` | Erfasst |
| `ReservOrdered` | Bestellt reserviert |
| `ReservPhysical` | Physisch reserviert |

### <a name="calculated-measures"></a><a name="data-source-configuration-calculated-measure"></a>Berechnete Messungen

Berechnete Maße bieten eine angepasste Berechnungsformel, die aus einer Kombination von physikalischen Messungen besteht. Mit dieser Funktionalität können Sie eine Reihe von physikalischen Kennzahlen festlegen, die addiert werden, und/oder eine Reihe von physikalischen Kennzahlen, die subtrahiert werden, um das Formular für die angepasste Messung zu bilden.

Sie haben zum Beispiel das folgende Abfrageergebnis.

```json
[
    {
        "productId": "T-shirt",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red"
        },
        "quantities": {
            "pos": {
                "inbound": 80.0,
                "outbound": 20.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "externalchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            }
        }
    }
]
```

Sie konfigurieren dann eine berechnete Messung, die den Namen `MyCustomAvailableforReservation` trägt, wie in der folgenden Tabelle gezeigt. Diese berechnete Kennzahl wird vom Verbrauchssystem verbraucht.

| Verbrauchs-System | Berechnete Messung | Datenquelle | Physikalische Messung | Berechnungstyp |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `pos` | `inbound` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `pos` | `outbound` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `received` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `scheduled` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `issued` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `reserved` | `Subtraction` |

Wenn diese Berechnungsformel verwendet wird, wird das neue Abfrageergebnis die angepasste Messung enthalten.

```json
[
    {
        "productId": "T-shirt",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red"
        },
        "quantities": {
            "pos": {
                "inbound": 80.0,
                "outbound": 20.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "externalchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

Die `MyCustomAvailableforReservation` Ausgabe, basierend auf der Berechnungseinstellung in den angepassten Messungen, ist 100 + 50 + 80 + 90 + 30 - 10 - 20 - 60 - 40 = 220.

## <a name="partition-configuration"></a><a name="partition-configuration"></a>Partitionskonfiguration

Die Partitionskonfiguration besteht aus einer Kombination von Basisdimensionen. Sie definiert das Datenverteilungsmuster. Datenvorgänge in derselben Partition unterstützen eine hohe Leistung und verursachen nicht zu hohe Kalkulationen. Daher können gute Partitionsmuster erhebliche Vorteile bringen.

Inventory Visibility bietet die folgende Standard-Partitionskonfiguration.

| Basis-Dimension | Hierarchie |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |

> [!NOTE]
> Die Standard-Partitionskonfiguration dient nur als Referenz. Sie müssen sie nicht in Inventory Visibility definieren. Derzeit wird das Upgrade der Partitionskonfiguration nicht unterstützt.

## <a name="product-index-hierarchy-configuration"></a><a name="index-configuration"></a>Produktindex-Hierarchie-Konfiguration

In den meisten Fällen wird die Abfrage des Lagerbestands nicht nur auf der höchsten Ebene "Gesamt" erfolgen. Stattdessen möchten Sie vielleicht auch Ergebnisse sehen, die auf Basis der Bestandsdimensionen aggregiert sind.

Inventory Visibility bietet Flexibilität, indem Sie die _Indizes_ festlegen können. Diese Indizes basieren auf einer Dimension oder einer Kombination von Dimensionen. Ein Index besteht aus einer *Satznummer*, einer *Dimension* und einer *Hierarchie*, wie in der folgenden Tabelle festgelegt.

| Name | Beschreibung |
|---|---|
| Set-Nummer festlegen | Dimensionen, die zum gleichen Set (Index) gehören, werden gruppiert, und ihnen wird die gleiche Set-Nummer zugewiesen. |
| Dimensionen | Basisdimensionen, über die das Abfrageergebnis aggregiert wird. |
| Hierarchie | Die Hierarchie wird verwendet, um die unterstützten Dimensionen-Kombinationen zu definieren, die abgefragt werden können. Sie legen z. B. ein Dimensionen-Set fest, das eine Hierarchie-Sequenz von `(ColorId, SizeId, StyleId)` hat. In diesem Fall unterstützt das System Abfragen auf vier Dimensionen-Kombinationen. Die erste Kombination ist leer, die zweite ist `(ColorId)`, die dritte ist `(ColorId, SizeId)` und die vierte ist `(ColorId, SizeId, StyleId)`. Die anderen Kombinationen werden nicht unterstützt. Weitere Informationen finden Sie im folgenden Beispiel. |

### <a name="example"></a>Beispiel

In diesem Abschnitt finden Sie ein Beispiel, das zeigt, wie die Hierarchie funktioniert.

Sie haben die folgenden Elemente in Ihrem Bestand.

| Artikel | ColorId | SizeId | StyleId | Leistung |
|---|---|---|---|---|
| T-Shirt | Schwarz | Klein | Breit | 1 |
| T-Shirt | Schwarz | Klein | Regelmäßig | 2 |
| T-Shirt | Schwarz | Groß | Breit | 3 |
| T-Shirt | Schwarz | Groß | Regelmäßig | 4 |
| T-Shirt | Red | Klein | Breit | 5 |
| T-Shirt | Red | Klein | Regelmäßig | 6 |
| T-Shirt | Red | Groß | Regelmäßig | 7 |

Hier ist der Index.

| Nummer festlegen | Dimensionen | Hierarchie |
|---|---|---|
| 1 | `ColorId` | 1 |
| 1 | `SizeId` | 2 |
| 1 | `StyleId` | 3 |

Mit dem Index können Sie den Lagerbestand auf die folgenden Arten abfragen:

- `()` - gruppiert nach allen

    - T-Shirt, 28

- `(ColorId)` - gruppiert nach `ColorId`

    - T-Shirt, Schwarz, 10
    - T-Shirt, Rot, 18

- `(ColorId, SizeId)` - gruppiert nach der Kombination von `ColorId` und `SizeId`

    - T-Shirt, Schwarz, Small, 3
    - T-Shirt, Schwarz, Large, 7
    - T-Shirt, Rot, Small, 11
    - T-Shirt, Rot, Large, 7

- `(ColorId, SizeId, StyleId)` - gruppiert nach der Kombination von `ColorId`, `SizeId` und `StyleId`

    - T-Shirt, Schwarz, Small, Wide, 1
    - T-Shirt, Schwarz, Small, Regular, 2
    - T-Shirt, Schwarz, Large, Wide, 3
    - T-Shirt, Schwarz, Large, Regular, 4
    - T-Shirt, Rot, Small, Wide, 5
    - T-Shirt, Rot, Small, Regular, 6
    - T-Shirt, Rot, Large, Regular, 7

> [!NOTE]
> Basisdimensionen, die in der Partitionskonfiguration definiert sind, sollten nicht in Indexkonfigurationen definiert werden.

## <a name="reservation-configuration-optional"></a><a name="reservation-configuration"></a>Reservierungskonfiguration (optional)

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Die Reservierungskonfiguration ist erforderlich, wenn Sie die Funktion der Soft-Reservierung verwenden möchten. Die Konfiguration besteht aus zwei grundlegenden Teilen:

- Soft-Reservierungs-Zuordnung
- Soft-Reservierungs-Hierarchie

### <a name="soft-reservation-mapping"></a>Zuordnung der Soft-Reservierung

Wenn Sie eine Reservierung vornehmen, möchten Sie vielleicht wissen, ob der Lagerbestand aktuell für die Reservierung verfügbar ist. Die Validierung ist mit einer berechneten Messung verknüpft, die eine Berechnungsformel aus einer Kombination von physikalischen Messungen darstellt.

Zum Beispiel basiert eine Reservierungsmaßnahme auf der physikalischen Messung `SoftReservOrdered` aus der Datenquelle `iv` (Inventory Visibility). In diesem Fall können Sie die berechnete Kennzahl `AvailableToReserve` der Datenquelle `iv` wie hier gezeigt festlegen.

| Berechnungstyp | Datenquelle | Physikalische Messung |
|---|---|---|
| Addition | `fno` | `AvailPhysical` |
| Addition | `pos` | `Inbound` |
| Subtraktion | `pos` | `Outbound` |
| Subtraktion | `iv` | `SoftReservOrdered` |

Legen Sie dann eine weiche Reservierungszuordnung fest, um eine Zuordnung von der `SoftReservOrdered`-Reservierungskennzahl zur `AvailableToReserve`-berechneten Kennzahl herzustellen.

| Datenquelle für physikalische Messungen | Physikalische Messung | Verfügbar für Reservierungsdatenquelle | Verfügbar für die berechnete Messung der Reservierung |
|---|---|---|---|
| `iv` | `SoftReservOrdered` | `iv` | `AvailableToReserve` |

Wenn Sie nun eine Reservierung für `SoftReservOrdered` vornehmen, findet Inventory Visibility automatisch `AvailableToReserve` und die zugehörige Berechnungsformel, um die Reservierungsvalidierung durchzuführen.

Sie haben z. B. den folgenden Lagerbestand in Inventory Visibility.

```json
{
    "productId": "T-shirt",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red"
    },
    "quantities": {
        "iv": {
            "SoftReservOrdered": 90
        },
        "fno": {
            "availphysical": 70.0,
        },
        "pos": {
            "inbound": 50.0,
            "outbound": 20.0
        }
    }
}
```

In diesem Fall gilt die folgende Berechnung:

`AvailableToReserve` = `fno.availphysical` + `pos.inbound` – `pos.outbound` – `iv.SoftReservOrdered`  
= 70 + 50 – 20 – 90  
= 10

Wenn Sie also versuchen, eine Reservierung für `iv.SoftReservOrdered` vorzunehmen, und die Menge kleiner oder gleich `AvailableToReserve` (10) ist, können Sie die Reservierung durchführen.

### <a name="soft-reservation-hierarchy"></a>Weiche Reservierungshierarchie

Die Reservierungshierarchie beschreibt die Sequenz von Dimensionen, die bei der Reservierung angegeben werden müssen. Sie funktioniert genauso wie die Produktindexhierarchie bei Lagerbestandsabfragen.

Die Reservierungshierarchie ist unabhängig von der Produktindexhierarchie. Diese Unabhängigkeit ermöglicht die Implementierung einer Kategorieverwaltung, bei der Benutzer die Dimensionen in Details aufschlüsseln können, um die Anforderungen für genauere Reservierungen zu spezifizieren.

Hier ist ein Beispiel für eine weiche Reservierungshierarchie.

| Basis-Dimension | Hierarchie |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |
| `ColorId` | 3 |
| `SizeId` | 4 |
| `StyleId` | 5 |

In diesem Beispiel können Sie Reservierungen in den folgenden Sequenzen von Dimensionen vornehmen:

- `()` - Es ist keine Dimension angegeben.
- `(SiteId)`
- `(SiteId, LocationId)`
- `(SiteId, LocationId, ColorId)`
- `(SiteId, LocationId, ColorId, SizeId)`
- `(SiteId, LocationId, ColorId, SizeId, StyleId)`

Eine gültige Sequenz von Dimensionen sollte strikt der Reservierungshierarchie folgen, Dimension für Dimension. Die Hierarchiesequenz `(SiteId, LocationId, SizeId)` ist z. B. nicht gültig, weil `ColorId` fehlt.

## <a name="default-configuration-sample"></a><a name="default-configuration-sample"></a>Standardkonfigurationsbeispiel

Inventory Visibility legt bei seiner Initialisierung eine Standardkonfiguration fest. Sie können die Konfiguration nach Bedarf ändern.

### <a name="data-source-configuration"></a>Konfiguration der Datenquelle

#### <a name="configuration-of-the-iv-data-source"></a>Konfiguration der iv-Datenquelle

Dieser Abschnitt beschreibt, wie die Datenquelle `iv` konfiguriert wird.

##### <a name="physical-measures-configured-for-the-iv-data-source"></a>Konfigurierte physikalische Messungen für die iv-Datenquelle

Die folgenden physikalischen Messungen sind für die Datenquelle `iv` konfiguriert:

- `Ordered`
- `SoftReservPhysical`
- `SoftReservOrdered`
- `ReservOrdered`
- `ReservPhysical`

##### <a name="orderedtotal-calculated-measure"></a>OrderedTotal berechnete Messung

Die berechnete Kennzahl `OrderedTotal` wird für die Datenquelle `iv` wie in der folgenden Tabelle gezeigt konfiguriert.

| Berechnungstyp | Datenquelle | Physikalische Messung |
|---|---|---|
| Addition | `fno` | `Ordered` |
| Addition | `fno` | `Arrived` |
| Addition | `iv` | `Ordered` |

##### <a name="onhand-calculated-measure"></a>OnHand berechnete Messung

Die berechnete Messung `OnHand` ist für die Datenquelle `iv` konfiguriert, wie in der folgenden Tabelle dargestellt.

| Berechnungstyp | Datenquelle | Physikalische Messung |
|---|---|---|
| Addition | `fno` | `PhysicalInvent` |
| Addition | `iom` | `OnHand` |
| Addition | `erp` | `Unrestricted` |
| Addition | `erp` | `QualityInspection` |
| Addition | `pos` | `PosInbound` |
| Subtraktion | `pos` | `PosOutbound` |

##### <a name="reservedtotal-calculated-measure"></a>ReserviertGesamt berechnete Messung

Die berechnete Messung `ReservedTotal` ist für die Datenquelle `iv` konfiguriert, wie in der folgenden Tabelle dargestellt.

| Berechnungstyp | Datenquelle | Physikalische Messung |
|---|---|---|
| Addition | `fno` | `ReservPhysical` |
| Addition | `fno` | `ReservOrdered` |
| Addition | `iv` | `SoftReservPhysical` |
| Addition | `iv` | `SoftReservOrdered` |
| Addition | `iv` | `ReservPhysical` |
| Addition | `iv` | `ReservOrdered` |

##### <a name="softreserved-calculated-measure"></a>SoftReserved berechnete Messung

Die berechnete Messung `SoftReserved` ist für die Datenquelle `iv` konfiguriert, wie in der folgenden Tabelle dargestellt.

| Berechnungstyp | Datenquelle | Physikalische Messung |
|---|---|---|
| Addition | `iv` | `SoftReservPhysical` |
| Addition | `iv` | `SoftReservOrdered` |

##### <a name="hardreserved-calculated-measure"></a>HardReserved berechnete Messung

Die `HardReserved` berechnete Messung ist für die Datenquelle `iv` konfiguriert, wie in der folgenden Tabelle gezeigt.

| Berechnungstyp | Datenquelle | Physikalische Messung |
|---|---|---|
| Addition | `fno` | `ReservPhysical` |
| Addition | `fno` | `ReservOrdered` |
| Addition | `iv` | `ReservPhysical` |
| Addition | `iv` | `ReservOrdered` |

##### <a name="openorder-calculated-measure"></a>OpenOrder berechnete Messung

Die berechnete Messung `OpenOrder` ist für die Datenquelle `iv` konfiguriert, wie in der folgenden Tabelle dargestellt.

| Berechnungstyp | Datenquelle | Physikalische Messung |
|---|---|---|
| Addition | `fno` | `OnOrder` |
| Addition | `iom` | `OnOrder` |

##### <a name="onhandavailable-calculated-measure"></a>OnHandAvailable berechnete Messung

Die berechnete Messung `OnHandAvailable` ist für die Datenquelle `iv` konfiguriert, wie in der folgenden Tabelle dargestellt.

| Berechnungstyp | Datenquelle | Physikalische Messung |
|---|---|---|
| Addition | `fno` | `PhysicalInvent` |
| Addition | `iom` | `OnHand` |
| Addition | `erp` | `Unrestricted` |
| Addition | `erp` | `QualityInspection` |
| Addition | `pos` | `PosInbound` |
| Subtraktion | `fno` | `ReservPhysical` |
| Subtraktion | `iv` | `SoftReservPhysical` |
| Subtraktion | `pos` | `PosOutbound` |

##### <a name="availabletoreserve-calculated-measure"></a>AvailableToReserve berechnete Messung

Die berechnete Messung `AvailableToReserve` ist für die Datenquelle `iv` konfiguriert, wie in der folgenden Tabelle dargestellt.

| Berechnungstyp | Datenquelle | Physikalische Messung |
|---|---|---|
| Addition | `fno` | `PhysicalInvent` |
| Addition | `iom` | `OnHand` |
| Addition | `erp` | `Unrestricted` |
| Addition | `erp` | `QualityInspection` |
| Addition | `pos` | `PosInbound` |
| Addition | `fno` | `Ordered` |
| Addition | `fno` | `Arrived` |
| Addition | `iv` | `Ordered` |
| Subtraktion | `fno` | `ReservPhysical` |
| Subtraktion | `fno` | `ReservOrdered` |
| Subtraktion | `iv` | `SoftReservPhysical` |
| Subtraktion | `iv` | `SoftReservOrdered` |
| Subtraktion | `iv` | `ReservPhysical` |
| Subtraktion | `iv` | `ReservOrdered` |
| Subtraktion | `pos` | `PosOutbound` |

##### <a name="inventorysupply-calculated-measure"></a>InventorySupply berechnete Messung

Die berechnete Messung `InventorySupply` ist für die Datenquelle `iv` konfiguriert, wie in der folgenden Tabelle dargestellt.

| Berechnungstyp | Datenquelle | Physikalische Messung |
|---|---|---|
| Addition | `fno` | `Ordered` |
| Addition | `fno` | `Arrived` |
| Addition | `iv` | `Ordered` |
| Addition | `fno` | `PhysicalInvent` |
| Addition | `iom` | `OnHand` |
| Addition | `erp` | `Unrestricted` |
| Addition | `erp` | `QualityInspection` |
| Addition | `pos` | `PosInbound` |
| Subtraktion | `pos` | `PosOutbound` |

##### <a name="inventorydemand-calculated-measure"></a>InventoryDemand berechnete Kennzahl

Die berechnete Messung `InventoryDemand` ist für die Datenquelle `iv` konfiguriert, wie in der folgenden Tabelle dargestellt.

| Berechnungstyp | Datenquelle | Physikalische Messung |
|---|---|---|
| Addition | `fno` | `OnOrder` |
| Addition | `iom` | `OnOrder` |
| Addition | `iv` | `SoftReservPhysical` |
| Addition | `iv` | `SoftReservOrdered` |
| Addition | `fno` | `ReservPhysical` |
| Addition | `fno` | `ReservOrdered` |
| Addition | `iv` | `ReservPhysical` |
| Addition | `iv` | `ReservOrdered` |

#### <a name="configuration-of-the-fno-data-source"></a>Konfiguration der Datenquelle "fno

Dieser Abschnitt beschreibt, wie die Datenquelle `fno` konfiguriert wird.

##### <a name="dimension-mappings-for-the-fno-data-source"></a>Dimensionen-Zuordnungen für die fno-Datenquelle

Für die Datenquelle `fno` sind die Dimensionen-Zuordnungen konfiguriert, die in der folgenden Tabelle aufgeführt sind.

| Externe Dimension | Basis-Dimension |
|---|---|
| `InventBatchId` | `BatchId` |
| `InventColorId` | `ColorId` |
| `InventLocationId` | `LocationId` |
| `InventSerialId` | `SerialId` |
| `InventSiteId` | `SiteId` |
| `InventSizeId` | `SizeId` |
| `InventStatusId` | `StatusId` |
| `InventStyleId` | `StyleId` |
| `LicensePlateId` | `LicensePlateId` |
| `WMSLocationId` | `WMSLocationId` |
| `WMSPalletId` | `WMSPalletId` |
| `ConfigId` | `ConfigId` |
| `InventVersionId` | `VersionId` |
| `InventDimension1` | `CustomDimension1` |
| `InventDimension2` | `CustomDimension2` |
| `InventDimension3` | `CustomDimension3` |
| `InventDimension4` | `CustomDimension4` |
| `InventDimension5` | `CustomDimension5` |
| `InventDimension6` | `CustomDimension6` |
| `InventDimension7` | `CustomDimension7` |
| `InventDimension8` | `CustomDimension8` |
| `InventDimension9` | `CustomDimension9` |
| `InventDimension10` | `CustomDimension10` |
| `InventDimension11` | `CustomDimension11` |
| `InventDimension12` | `CustomDimension12` |

##### <a name="physical-measures-configured-for-the-fno-data-source"></a>Für die Datenquelle "fno" konfigurierte physikalische Messungen

Die folgenden physikalischen Messungen sind für die Datenquelle `fno` konfiguriert:

- `Ordered`
- `Arrived`
- `AvailPhysical`
- `PhysicalInvent`
- `ReservPhysical`
- `ReservOrdered`
- `OnOrder`

#### <a name="configuration-of-the-pos-data-source"></a>Konfiguration der pos-Datenquelle

Dieser Abschnitt beschreibt, wie die Datenquelle `pos` konfiguriert ist.

##### <a name="physical-measures-for-the-pos-data-source"></a>Physikalische Messungen für die pos-Datenquelle

Die folgenden physikalischen Messungen sind für die Datenquelle `pos` konfiguriert:

- `PosInbound`
- `PosOutbound`

##### <a name="availquantity-calculated-measure"></a>AvailQuantity berechnete Messung

Die berechnete Kennzahl `AvailQuantity` wird für die Datenquelle `pos` wie in der folgenden Tabelle gezeigt konfiguriert.

| Berechnungstyp | Datenquelle | Physikalische Messung |
|---|---|---|
| Addition | `fno` | `AvailPhysical` |
| Addition | `pos` | `PosInbound` |
| Subtraktion | `pos` | `PosOutbound` |

#### <a name="configuration-of-the-iom-data-source"></a>Konfiguration der iom-Datenquelle

Die folgenden physikalischen Messungen sind für die Datenquelle `iom` (intelligente Auftragsverwaltung) konfiguriert:

- `OnOrder`
- `OnHand`

#### <a name="configuration-of-the-erp-data-source"></a>Konfiguration der erp-Datenquelle

Die folgenden physikalischen Messungen sind für die Datenquelle `erp` (Enterprise Resource Planning) konfiguriert:

- `Unrestricted`
- `QualityInspection`

### <a name="partition-configuration"></a>Partitionskonfiguration

Die folgende Tabelle zeigt die Standard-Partitionskonfiguration.

| Basis-Dimension | Hierarchie |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |

### <a name="index-configuration"></a>Index-Konfiguration

Die folgende Tabelle zeigt die Standard-Indexkonfiguration.

| Nummer festlegen | Dimensionen | Hierarchie |
|---|---|---|
| 1 | `ColorId` | 1 |
| 1 | `SizeId` | 2 |
| 1 | `StyleId` | 3 |

### <a name="reservation-configuration"></a>Reservierungs-Konfiguration

Dieser Abschnitt beschreibt die standardmäßige Reservierungskonfiguration.

#### <a name="reservation-mapping"></a>Zuordnung der Reservierung

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Die folgende Tabelle zeigt die standardmäßige Zuordnung von Reservierungen.

| Datenquelle für physikalische Messungen | Physikalische Messung | Verfügbar für Reservierungsdatenquelle | Verfügbar für die berechnete Messung der Reservierung |
|---|---|---|---|
| `iv` | `SoftReservOrdered` | `iv` | `AvailableToReserve` |

#### <a name="reservation-hierarchy"></a>Reservierungshierarchie

Die folgende Tabelle zeigt die Standard-Reservierungshierarchie.

| Basis-Dimension | Hierarchie |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |
| `ColorId` | 3 |
| `SizeId` | 4 |
| `StyleId` | 5 |
| `BatchId` | 6 |
| `SerialId` | 7 |
| `StatusId` | 8 |
| `LicensePlateId` | 9 |
| `WMSLocationId` | 10 |
| `WMSPalletId` | 11 |
| `ConfigId` | 12 |
| `VersionId` | 13 |
| `CustomDimension1` | 14 |
| `CustomDimension2` | 15 |
| `CustomDimension3` | 16 |
| `CustomDimension4` | 17 |
| `CustomDimension5` | 18 |
| `CustomDimension6` | 19 |
| `CustomDimension7` | 20 |
| `CustomDimension8` | 21 |
| `CustomDimension9` | 22 |
| `CustomDimension10` | 23 |
| `CustomDimension11` | 24 |
| `CustomDimension12` | 25 |
| `ExtendedDimension1` | 26 |
| `ExtendedDimension2` | 27 |
| `ExtendedDimension3` | 28 |
| `ExtendedDimension4` | 29 |
| `ExtendedDimension5` | 30 |
| `ExtendedDimension6` | 31 |
| `ExtendedDimension7` | 32 |
| `ExtendedDimension8` | 33 |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
