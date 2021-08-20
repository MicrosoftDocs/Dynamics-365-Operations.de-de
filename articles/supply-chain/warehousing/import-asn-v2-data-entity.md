---
title: Eingehende ASNs über die Entität V2-Daten importieren
description: In diesem Thema wird erklärt, wie Sie den Import eingehender Vorabliefernotizen (ASNs) über die Entität „Inbound ASN V2 data“ verwalten.
author: GalynaFedorova
ms.date: 05/31/2021
ms.topic: article
ms.search.form: WHSInboundASNV2Entity, WHSInboundASNEntity
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-04
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 8f3c42e28b01afd3b7ca8b1af8381dd5377e17eb31da655a397bd7805779f879
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6751696"
---
# <a name="import-inbound-asns-through-the-v2-data-entity"></a>Eingehende ASNs über die Entität V2-Daten importieren

[!include [banner](../../includes/banner.md)]

Vorabliefernotizen (ASNs) benachrichtigen Sie über Lieferungen von Kreditor. Sie helfen dem Absender, den Inhalt einer Sendung und zusätzliche Informationen darüber zu beschreiben, wie z. B. die Elemente und die Verpackung.

ASNs können den Arbeitskräften am Lagerort helfen, zu erfahren, was wann eintrifft. Daher können sie sich vorbereiten. Darüber hinaus können Arbeitskräfte im Lagerort ASNs verwenden, um die Details einer Sendung mit der zugehörigen Einkaufsbestellung abzugleichen, die zuvor erstellt wurde.

In diesem Thema wird eine Sammlung von Szenarien vorgestellt, die anhand von Beispielen zeigen, wie man mit ASN-Dateien arbeitet.

> [!IMPORTANT]
> *Der eingehende ASN*-Import gilt nur für Elemente, die für die erweiterte Lagerortverwaltung (WMS) aktiviert sind. Bevor Sie einen Lieferavis erhalten, muss eine Einkaufsbestellung im System gegen den Kreditor, der diesen Lieferavis sendet, registriert werden.

## <a name="inbound-asn-v2-entity"></a>Eingehende ASN V2 Entität

Sie importieren eingehende Lieferavise, indem Sie die zusammengesetzte Entität *Inbound ASN V2* verwenden. *Inbound ASN V2* macht sich die folgenden Entitäten zunutze:

- Kopfzeile für eingehende Ladung
- Kopfzeile für eingehende Lieferung
- Verpackungsstrukturen eingehender Ladung
- Verpackungsstrukturanfragen eingehender Ladung
- Verpackungsstruktur-Anfragepositionen eingehender Ladung
- Verpackungsstrukturpositionen eingehender Ladung

Die *Inbound ASN V2* Composite Data Entität ist für asynchrone Integrationsszenarien gedacht, in denen XML-Datei-basierte Importe verwendet werden.

## <a name="xml-format-for-importing-asns"></a>XML-Format für den Import von ASNs

Microsoft Dynamics 365 Supply Chain Management unterstützt das folgende XML-Format für den Import von ASNs. Jeder Knoten in der XML-Datei repräsentiert ein Attribut von einer einzelnen Entität.

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity>
        <WHSInboundShipmentHeaderEntity>
            <WHSInboundLoadPackingStructureEntity>
                <WHSInboundLoadPackingStructureCaseEntity>
                    <WHSInboundPackingStructureCaseLineV2Entity>
                    </WHSInboundPackingStructureCaseLineV2Entity>
                </WHSInboundLoadPackingStructureCaseEntity>
                <WHSInboundLoadPackingStructureLineV2Entity>
                </WHSInboundLoadPackingStructureLineV2Entity>
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

## <a name="examples"></a>Beispiele

In den folgenden Unterabschnitten finden Sie Beispiele für ASN-XML-Importdateien für Kreditor-Lieferungen.

### <a name="example-1"></a>Beispiel 1

Das folgende Beispiel zeigt eine XML-Datei für den Import von Kreditor-Sendungen für eine Bestellung, wenn keine Falldetails enthalten sind.

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity TRACTORNUMBER="0000101">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_01" VENDORADDRESSCOUNTRYREGIONID = "USA" VENDORADDRESSSTREET = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000176" ITEMNUMBER="A0001" QUANTITY="1" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

### <a name="example-2"></a>Beispiel 2

Das folgende Beispiel zeigt eine XML-Datei für den Import von Kreditorlieferungen für eine Bestellung, wenn Falldetails enthalten sind.

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity ESTIMATEDARRIVALDATETIME="2021-04-25T11:00:00+00:00">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="MVR_SNN_0004">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="MVR_SNN_0004" PACKEDTOTALQUANTITY="2.00">
                <WHSInboundLoadPackingStructureCaseEntity PARENTPACKINGSTRUCTURELICENSEPLATENUMBER="MVR_SNN_0004" LICENSEPLATENUMBER="MVR_SNN_0004A" PACKEDTOTALQUANTITY="2.00" />
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000175" ITEMNUMBER="A0001" PURCHASEORDERLINENUMBER="1" QUANTITY="2.00" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

### <a name="example-3"></a>Beispiel 3

Das folgende Beispiel zeigt eine XML-Datei für den Import von Kreditorlieferungen für mehrere Bestellungen, wenn Falldetails enthalten sind.

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity TRACTORNUMBER="0000101">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_01" VENDORADDRESSCOUNTRYREGIONID = "USA" VendorAddressStreet = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000176" ITEMNUMBER="A0001" QUANTITY="100" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_02" VENDORADDRESSCOUNTRYREGIONID = "USA" VendorAddressStreet = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="A0001" QUANTITY="200" UNITSYMBOL="ea" />
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="P0004" QUANTITY="300" UNITSYMBOL="ea" ITEMBATCHNUMBER="BN0001" />
            </WHSInboundLoadPackingStructureEntity>
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_002">
                <WHSInboundLoadPackingStructureCaseEntity LICENSEPLATENUMBER="LP_ASN_002_C01">
                    <WHSInboundLoadPackingStructureCaseLineV2Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="A0001" QUANTITY="400" UNITSYMBOL="ea" />
                </WHSInboundLoadPackingStructureCaseEntity>
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

## <a name="inspect-the-results-of-importing-an-asn-file"></a>Prüfen der Ergebnisse des Imports einer ASN-Datei

Gehen Sie wie folgt vor, um die Ergebnisse des Imports einer ASN-Datei zu prüfen.

1. Gehen Sie zu **Lagerortverwaltung \> Ladungen \> Alle Ladungen**.
1. Suchen und öffnen Sie eine Ladung, die als Teil eines ASN-Imports erstellt wurde.
1. Auf der Inforegisterkarte **Laden** sollten Sie Werte sehen, die auf der XML-Datei basieren.
1. Auf der Registerkarte **Laden** Inforegister sollten Sie Bestellnummern und Artikeldetails sehen, die auf der XML-Datei basieren.
1. Wählen Sie im Aktionsbereich auf der Registerkarte **Versand und Empfang** in der Gruppe **Empfang** die Option **Packungsstruktur**, um die Verpackungsstruktur der Ladung zu überprüfen.
1. Auf dem Inforegister **Paletten** sollten Sie Ladungsträger sehen, die auf der XML-Datei basieren.
1. Auf der Registerkarte **Koffer** sollten Sie Koffer sehen, die auf der XML-Datei basieren.
1. Auf der Registerkarte **Elemente** des Inforegisters sollten Sie Elemente und Mengen sehen, die auf der XML-Datei basieren.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
