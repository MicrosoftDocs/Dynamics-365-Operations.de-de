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
ms.openlocfilehash: 470cc0c39f211a5d0f106c4c6e193867388e2b53
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249105"
---
# <a name="import-inbound-asns-through-the-v2-data-entity"></a><span data-ttu-id="e306c-103">Eingehende ASNs über die Entität V2-Daten importieren</span><span class="sxs-lookup"><span data-stu-id="e306c-103">Import inbound ASNs through the V2 data entity</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e306c-104">Vorabliefernotizen (ASNs) benachrichtigen Sie über Lieferungen von Kreditor.</span><span class="sxs-lookup"><span data-stu-id="e306c-104">Advanced shipping notices (ASNs) notify you about vendor deliveries.</span></span> <span data-ttu-id="e306c-105">Sie helfen dem Absender, den Inhalt einer Sendung und zusätzliche Informationen darüber zu beschreiben, wie z. B. die Elemente und die Verpackung.</span><span class="sxs-lookup"><span data-stu-id="e306c-105">They help the sender describe the contents of a shipment and additional information about it, such as the items and packaging.</span></span>

<span data-ttu-id="e306c-106">ASNs können den Arbeitskräften am Lagerort helfen, zu erfahren, was wann eintrifft.</span><span class="sxs-lookup"><span data-stu-id="e306c-106">ASNs can help warehouse workers learn what is arriving when.</span></span> <span data-ttu-id="e306c-107">Daher können sie sich vorbereiten.</span><span class="sxs-lookup"><span data-stu-id="e306c-107">Therefore, they can prepare.</span></span> <span data-ttu-id="e306c-108">Darüber hinaus können Arbeitskräfte im Lagerort ASNs verwenden, um die Details einer Sendung mit der zugehörigen Einkaufsbestellung abzugleichen, die zuvor erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="e306c-108">In addition, warehouse workers can use ASNs to match the details of a shipment to the related purchase order that was previously created.</span></span>

<span data-ttu-id="e306c-109">In diesem Thema wird eine Sammlung von Szenarien vorgestellt, die anhand von Beispielen zeigen, wie man mit ASN-Dateien arbeitet.</span><span class="sxs-lookup"><span data-stu-id="e306c-109">This topic presents a collection of scenarios that show, through examples, how to work with ASN files.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e306c-110">*Der eingehende ASN*-Import gilt nur für Elemente, die für die erweiterte Lagerortverwaltung (WMS) aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="e306c-110">*Inbound ASN* import applies only to items that are enabled for advanced warehouse management (WMS).</span></span> <span data-ttu-id="e306c-111">Bevor Sie einen Lieferavis erhalten, muss eine Einkaufsbestellung im System gegen den Kreditor, der diesen Lieferavis sendet, registriert werden.</span><span class="sxs-lookup"><span data-stu-id="e306c-111">Before you receive an ASN, a purchase order must be registered in the system against the vendor who is sending that ASN.</span></span>

## <a name="inbound-asn-v2-entity"></a><span data-ttu-id="e306c-112">Eingehende ASN V2 Entität</span><span class="sxs-lookup"><span data-stu-id="e306c-112">Inbound ASN V2 entity</span></span>

<span data-ttu-id="e306c-113">Sie importieren eingehende Lieferavise, indem Sie die zusammengesetzte Entität *Inbound ASN V2* verwenden.</span><span class="sxs-lookup"><span data-stu-id="e306c-113">You import inbound ASNs by using the *Inbound ASN V2* composite data entity.</span></span> <span data-ttu-id="e306c-114">*Inbound ASN V2* macht sich die folgenden Entitäten zunutze:</span><span class="sxs-lookup"><span data-stu-id="e306c-114">*Inbound ASN V2* takes advantage of the following entities:</span></span>

- <span data-ttu-id="e306c-115">Kopfzeile für eingehende Ladung</span><span class="sxs-lookup"><span data-stu-id="e306c-115">Inbound load header</span></span>
- <span data-ttu-id="e306c-116">Kopfzeile für eingehende Lieferung</span><span class="sxs-lookup"><span data-stu-id="e306c-116">Inbound shipment header</span></span>
- <span data-ttu-id="e306c-117">Verpackungsstrukturen eingehender Ladung</span><span class="sxs-lookup"><span data-stu-id="e306c-117">Inbound load packing structures</span></span>
- <span data-ttu-id="e306c-118">Verpackungsstrukturanfragen eingehender Ladung</span><span class="sxs-lookup"><span data-stu-id="e306c-118">Inbound load packing structure cases</span></span>
- <span data-ttu-id="e306c-119">Verpackungsstruktur-Anfragepositionen eingehender Ladung</span><span class="sxs-lookup"><span data-stu-id="e306c-119">Inbound load packing structure case lines</span></span>
- <span data-ttu-id="e306c-120">Verpackungsstrukturpositionen eingehender Ladung</span><span class="sxs-lookup"><span data-stu-id="e306c-120">Inbound load packing structure lines</span></span>

<span data-ttu-id="e306c-121">Die *Inbound ASN V2* Composite Data Entität ist für asynchrone Integrationsszenarien gedacht, in denen XML-Datei-basierte Importe verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e306c-121">The *Inbound ASN V2* composite data entity is intended for asynchronous integration scenarios where XML file–based imports are used.</span></span>

## <a name="xml-format-for-importing-asns"></a><span data-ttu-id="e306c-122">XML-Format für den Import von ASNs</span><span class="sxs-lookup"><span data-stu-id="e306c-122">XML format for importing ASNs</span></span>

<span data-ttu-id="e306c-123">Microsoft Dynamics 365 Supply Chain Management unterstützt das folgende XML-Format für den Import von ASNs.</span><span class="sxs-lookup"><span data-stu-id="e306c-123">Microsoft Dynamics 365 Supply Chain Management supports the following XML format for importing ASNs.</span></span> <span data-ttu-id="e306c-124">Jeder Knoten in der XML-Datei repräsentiert ein Attribut von einer einzelnen Entität.</span><span class="sxs-lookup"><span data-stu-id="e306c-124">Each node in the XML file represents an attribute from an individual entity.</span></span>

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

## <a name="examples"></a><span data-ttu-id="e306c-125">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e306c-125">Examples</span></span>

<span data-ttu-id="e306c-126">In den folgenden Unterabschnitten finden Sie Beispiele für ASN-XML-Importdateien für Kreditor-Lieferungen.</span><span class="sxs-lookup"><span data-stu-id="e306c-126">The following subsections provide examples of ASN XML import files for vendor shipments.</span></span>

### <a name="example-1"></a><span data-ttu-id="e306c-127">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e306c-127">Example 1</span></span>

<span data-ttu-id="e306c-128">Das folgende Beispiel zeigt eine XML-Datei für den Import von Kreditor-Sendungen für eine Bestellung, wenn keine Falldetails enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="e306c-128">The following example shows an XML file for importing vendor shipments for one purchase order when no case details are included.</span></span>

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

### <a name="example-2"></a><span data-ttu-id="e306c-129">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e306c-129">Example 2</span></span>

<span data-ttu-id="e306c-130">Das folgende Beispiel zeigt eine XML-Datei für den Import von Kreditorlieferungen für eine Bestellung, wenn Falldetails enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="e306c-130">The following example shows an XML file for importing vendor shipments for one purchase order when case details are included.</span></span>

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

### <a name="example-3"></a><span data-ttu-id="e306c-131">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="e306c-131">Example 3</span></span>

<span data-ttu-id="e306c-132">Das folgende Beispiel zeigt eine XML-Datei für den Import von Kreditorlieferungen für mehrere Bestellungen, wenn Falldetails enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="e306c-132">The following example shows an XML file for importing vendor shipments for multiple purchase orders when case details are included.</span></span>

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

## <a name="inspect-the-results-of-importing-an-asn-file"></a><span data-ttu-id="e306c-133">Prüfen der Ergebnisse des Imports einer ASN-Datei</span><span class="sxs-lookup"><span data-stu-id="e306c-133">Inspect the results of importing an ASN file</span></span>

<span data-ttu-id="e306c-134">Gehen Sie wie folgt vor, um die Ergebnisse des Imports einer ASN-Datei zu prüfen.</span><span class="sxs-lookup"><span data-stu-id="e306c-134">Follow these steps to inspect the results of importing an ASN file.</span></span>

1. <span data-ttu-id="e306c-135">Gehen Sie zu **Lagerortverwaltung \> Ladungen \> Alle Ladungen**.</span><span class="sxs-lookup"><span data-stu-id="e306c-135">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="e306c-136">Suchen und öffnen Sie eine Ladung, die als Teil eines ASN-Imports erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="e306c-136">Find and open a load that was created as part of an ASN import.</span></span>
1. <span data-ttu-id="e306c-137">Auf der Inforegisterkarte **Laden** sollten Sie Werte sehen, die auf der XML-Datei basieren.</span><span class="sxs-lookup"><span data-stu-id="e306c-137">On the **Load** FastTab, you should see values that are based on the XML file.</span></span>
1. <span data-ttu-id="e306c-138">Auf der Registerkarte **Laden** Inforegister sollten Sie Bestellnummern und Artikeldetails sehen, die auf der XML-Datei basieren.</span><span class="sxs-lookup"><span data-stu-id="e306c-138">On the **Load lines** FastTab, you should see purchase order numbers and item details that are based on the XML file.</span></span>
1. <span data-ttu-id="e306c-139">Wählen Sie im Aktionsbereich auf der Registerkarte **Versand und Empfang** in der Gruppe **Empfang** die Option **Packungsstruktur**, um die Verpackungsstruktur der Ladung zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="e306c-139">On the Action Pane, on the **Ship and receive** tab, in the **Receive** group, select **Packing structure** to review the packing structure of the load.</span></span>
1. <span data-ttu-id="e306c-140">Auf dem Inforegister **Paletten** sollten Sie Ladungsträger sehen, die auf der XML-Datei basieren.</span><span class="sxs-lookup"><span data-stu-id="e306c-140">On the **Pallets** FastTab, you should see license plates that are based on the XML file.</span></span>
1. <span data-ttu-id="e306c-141">Auf der Registerkarte **Koffer** sollten Sie Koffer sehen, die auf der XML-Datei basieren.</span><span class="sxs-lookup"><span data-stu-id="e306c-141">On the **Cases** FastTab, you should see cases that are based on the XML file.</span></span>
1. <span data-ttu-id="e306c-142">Auf der Registerkarte **Elemente** des Inforegisters sollten Sie Elemente und Mengen sehen, die auf der XML-Datei basieren.</span><span class="sxs-lookup"><span data-stu-id="e306c-142">On the **Items** FastTab, you should see items and quantities that are based on the XML file.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
