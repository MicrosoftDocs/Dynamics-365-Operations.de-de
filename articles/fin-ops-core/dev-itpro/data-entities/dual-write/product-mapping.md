---
title: Einheitliche Produkterfahrung
description: In diesem Thema wird die Integration von Produktdaten zwischen Finance and Operations-Apps und Common Data Service beschrieben.
author: t-benebo
manager: AnnBe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 9593e8e54b18c6fe723a133eca699a30baabfdd0
ms.sourcegitcommit: e0e013fa8a4cc994ef6d1e0a1a3389b36b5afffa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/21/2020
ms.locfileid: "3081150"
---
# <a name="unified-product-experience"></a>Einheitliche Produktumgebung

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

Wenn ein Geschäftsökosystem aus Dynamics 365-Anwendungen besteht, wie Finance, Supply Chain Management und Sales, verwenden Unternehmen diese Anwendungen häufig für Quellproduktdaten. Der Grund dafür ist, dass diese Apps eine robuste Produktinfrastruktur bieten, die durch ausgeklügelte Preiskonzepte und genaue Bestandsverfügbarkeitsdaten abgerundet werden. Unternehmen, die ein externes Product Lifecycle Management (PLM)-System für die Beschaffung von Produktdaten verwenden, können Produkte von Finance and Operations-Apps in andere Dynamics 365-Apps kanalisieren. Die einheitliche Produkterfahrung bringt das integrierte Produktdatenmodell in Common Data Service, sodass alle Anwendungsbenutzer einschließlich Power Platform-Benutzer den Vorteil der umfassenden Produktdaten aus Finance and Operations-Apps nutzen können.

Hier ist das Produktdatenmodell aus Sales.

![Datenmodell für Produkte in CE](media/dual-write-product-4.jpg)

Hier ist das Produktdatenmodell aus Finance and Operations-Apps.

![Datenmodell für Produkte in Finance and Operations](media/dual-write-products-5.jpg)

Diese beiden Produktdatenmodelle wurden wie unten dargestellt in Common Data Service integriert.

![Datenmodell für Produkte in Dynamics 365-Apps](media/dual-write-products-6.jpg)

Die Entitätszuordnungen für duales Schreiben sind so konzipiert, dass Daten nur unidirektional weitergeleitet werden. Dies erfolgt nahezu in Echtzeit von Finance and Operations-Apps nach Common Data Service. Allerdings wurde die Produktinfrastruktur offen gestaltet, um sie bei Bedarf auch bidirektional nutzen zu können. Obwohl Sie sie auf eigene Gefahr anpassen können, empfiehlt Microsoft diese Methode nicht.

## <a name="templates"></a>Vorlagen

Produktinformationen enthält alle Informationen, die mit dem Produkt und seiner Definition in Verbindung stehen, z. B. den Produktdimensionen oder den Nachverfolgungs- und Lagerdimensionen. Wie die folgende Tabelle zeigt, darstellt, wird eine Sammlung von Entitätszuordnungen erstellt, um Produkte und zugehörige Informationen zu synchronisieren.

Finance and Operations | Sonstige Dynamics 365-Apps | Beschreibung
-----------------------|--------------------------------|---
Freigegebene Produkte V2 | msdyn\_sharedproductdetails | Die Entität **msdyn\_sharedproductdetails** enthält die Felder aus Finance and Operations-Apps, die das Produkt definieren, und die die Finanz- und Verwaltungsinformationen des Produkts enthalten. 
Von Common Data Service freigegebene eindeutig identifizierbare Produkte | Produkt | Die Entität **Produkt** enthält die Felder, die das Produkt definieren. Sie enthält Einzelprodukte (Produkte mit Untertypprodukt) und die Produktvarianten. Die Zuordnungen werden in der folgenden Tabelle veranschaulicht.
Durch Produktnummer identifizierter Strichcode | msdyn\_productbarcodes | Produktstrichcodes werden verwendet, um Produkte eindeutig zu kennzeichnen.
Standardauftragseinstellungen | msdyn\_productdefaultordersettings
Produktspezifische Standardauftragseinstellungen | msdyn_productdefaultordersettings
Produktdimensionsgruppen | msdyn\_productdimensiongroups | Die Produktdimensionsgruppe definierten, welche Produktdimensionen das Produkt definieren. 
Lagerdimensionsgruppen | msdyn\_productstoragedimensiongroups | Die Produkt-Lagerdimensionsgruppe stellt die Methode dar, die verwendet wird, um die Position des Produkts im Lagerort zu definieren.
Rückverfolgungsangabengruppen | msdyn\_producttrackingdimensiongroups | Die Produktnachverfolgungsdimensionsgruppe stellt die Methode dar, die verwendet wird, um das Produkt im Bestand nachzuverfolgen.
Farben | msdyn\_productcolors
Größen | msdyn\_productsizes
Formatvorlagen | msdyn\_productsytles
Konfigurationen | msdyn\_productconfigurations
Produktmasterfarben | msdyn_sharedproductcolors | Die Entität **Freigegebene Produktfarbe** gibt die Farben an, die ein bestimmter Produktmaster haben kann. Dieses Konzept wird zu Common Data Service migriert, um Daten einheitlich zu halten.
Produktmastergrößen | msdyn_sharedproductsizes | Die Entität **Freigegebene Produktgröße** gibt die Größen an, die ein bestimmter Produktmaster haben kann. Dieses Konzept wird zu Common Data Service migriert, um Daten einheitlich zu halten.
Produktmasterstile | msdyn_sharedproductstyles | Die Entität **Freigegebener Produktstil** gibt die Stile an, die ein bestimmter Produktmaster haben kann. Dieses Konzept wird zu Common Data Service migriert, um Daten einheitlich zu halten.
Produktmasterkonfigurationen | msdyn_sharedproductconfigurations | Die Entität **Freigegebener Produktkonfiguration** gibt die Konfigurationen an, die ein bestimmter Produktmaster haben kann. Dieses Konzept wird zu Common Data Service migriert, um Daten einheitlich zu halten.
Alle Produkte | msdyn_globalproducts | Die Entität „Alle Produkte“ enthält alle in Finance and Operations-Apps verfügbaren Produkte, sowohl die freigegebenen Produkte als auch die nicht freigegebenen Produkte.
Einheit | uoms
Einheitenumrechnungen | msdyn_ unitofmeasureconversions
Produktspezifische Maßeinheit-Umrechnung | msdyn_productspecificunitofmeasureconversion
Produktkategorien | msdyn_productcategories | Jede der Produktkategorien und -informationen über die Struktur und Eigenschaften ist in der Produktkategorieentität enthalten. 
Produktkategoriehierarchien | msdyn_productcategoryhierarhies | Sie verwenden Produkthierarchien, um Produkte zu kategorisieren oder zu gruppieren. Die Kategoriehierarchien sind in Common Data Service über die Entität Produktkategoriehierarchie verfügbar. 
Produktkategoriehierarchie-Rollen | msdyn_productcategoryhierarchies | Produkthierarchien können für verschiedene Rollen in D365 Finance and Operations verwendet werden. Um festzulegen, welche Kategorie in jeder Rolle verwendet wird, wird die Entität „Produktkategorierolle“ verwendet. 
Produktkategoriezuweisungen | msdyn_productcategoryassignments | Zum Zuweisen eines Produkts zu einer Kategorie kann die Entität „Produktkategoriezuweisungen“ verwendet werden.

## <a name="integration-of-products"></a>Integration von Produkten

In diesem Modell wird das Produkt durch die Kombination aus beiden Entitäten in Common Data Service dargestellt: **Produkt** und **msdyn\_sharedproductdetails**. Während die erste Entität die Definition eines Produkts (den eindeutige Bezeichner für das Produkt, den Produktname und die Beschreibung) beinhaltet, enthält die zweite Entität die Felder, die auf der Produktebene gespeichert werden. Die Kombination aus diesen beiden Entitäten wird verwendet, um das Produkt entsprechend des Konzepts der Lagermengeneinheit (SKU) zu definieren. Jedes freigegebene Produkt hat seine Informationen in den genannten Entitäten (Produkt und freigegebene Produktdetails). Um sämtliche Produkte zu verfolgen (freigegeben und nicht freigegeben), wird die Entität **Globale Produkte** verwendet. 

Da das Produkt als SKU dargestellt wird, können die Konzepte von eindeutig identifizierbaren Produkten, Produktmastern und Produktvarianten in Common Data Service folgendermaßen erfasst werden:

- **Produkte mit Untertypprodukt** sind Produkte, die auch durch sie selbst definiert werden. Es müssen keine Dimensionen festgelegt werden. Ein Beispiel ist ein bestimmtes Buch. Für diese Produkte wird ein Datensatz in der Entität **Produkt** erstellt, und ein Datensatz wird in der Entität **msdyn\_sharedproductdetails** erstellt. Es wird kein Produktfamiliendatensatz erstellt.
- **Produktmaster** werden als generische Produkte verwendet, die die Definition und die Regeln verwenden, mit denen das Verhalten in Geschäftsprozessen bestimmt wird. Auf Grundlage dieser Definitionen können eindeutig identifizierbare Produkte, bekannt als Produktvarianten, generiert werden. Beispielsweise ist das T-Shirt der Produktmaster, und es kann Farbe und Größe als Dimensionen haben. Varianten können freigegeben werden, die unterschiedliche Kombinationen dieser Dimensionen aufweisen, z. B. ein kleines blaues T-Shirt oder ein mittelgroßes grünes T-Shirt. In der Integration wird ein Datensatz pro Variante in der Produkttabelle erstellt. Dieser Datensatz enthält die variantenspezifischen Informationen, wie beispielsweise die verschiedenen Dimensionen. Die allgemeinen Informationen für das Produkt werden in der Entität **msdyn\_sharedproductdetails** gespeichert. (Diese allgemeinen Informationen werden im Produktmaster aufbewahrt.) Darüber hinaus wird ein Produktfamiliendatensatz pro Produktmaster erstellt. Die Produktmasterinformationen werden mit Common Data Service synchronisiert, sobald der freigegebene Produktmaster erstellt wird (aber bevor die Varianten freigegeben werden).
- **Eindeutig identifizierbare Produkte** verweisen auf alle Produktuntertypprodukte und alle Produktvarianten an. 

![Datenmodell für Produkte](media/dual-write-product.png)

Wenn die Dual-Write-Funktionalität aktiviert ist, werden die Anwendungen aus Finance and Operations in anderen Dynamics 365-Anwendungen im Zustand **Entwurf** synchronisiert. Sie werden der ersten Preisliste mit derselben Währung hinzugefügt. Das bedeutet, sie werden der ersten Preisliste in einer Dynamics 365-App hinzugefügt, die mit der Währung Ihrer juristischen Person übereinstimmt, in der das Produkt in einer Finance and Operations-App freigegeben wird. 

Produkte aus Finance and Operations-Apps werden standardmäßig mit anderen Dynamics 365-Apps im Status **Entwurf** synchronisiert. Um das Produkt mit dem Status **Aktiv** zu synchronisieren, können Sie es direkt in Auftragsangeboten verwenden, beispielsweise muss die folgende Einstellung ausgewählt werden. Wechseln Sie dazu zur Registerkarte **System > Verwaltung > Systemverwaltung > Systemeinstellungen > Verkauf**, und wählen Sie **Produkte im Status „Aktiv“ erstellen = ja** aus. 

Beachten Sie, dass die Synchronisierung der Produkte aus Finance and Operations-Apps nach Common Data Service erfolgt. Dies bedeutet, dass die Werte der Produktentitätsfelder in Common Data Service zwar geändert werden können, die Werte beim Auslösen der Synchronisierung in Common Data Service jedoch überschrieben werden (wenn ein Produktfeld in einer Finance and Operations-App geändert wird). 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [products](includes/EcoResReleasedDistinctProductCDSEntity-products.md)]

[!include [product details](includes/EcoResReleasedProductV2-msdyn-sharedproductdetails.md)]

[!include [global products](includes/EcoResEveryProductEntity-msdyn-globalproducts.md)]

## <a name="product-dimensions"></a>Produktdimensionen 

Produktdimensionen sind Merkmale, die eine Produktvariante identifizieren. Die vier Produktdimensionen (Farbe, Größe, Stil und Konfiguration) werden auch Common Data Service zugeordnet, um die Produktvarianten zu definieren. Die folgende Abbildung zeigt das Datenmodell für die Produktdimension „Farbe”. Dasselbe Modell wird auf die Größen, Stile und Konfigurationen angewendet. 

![Datenmodell für Produkte](media/dual-write-product-two.png)

[!include [product colors](includes/EcoResProductColorEntity-msdyn-productcolor.md)]

[!include [product sizes](includes/EcoResProductSizeEntity-msdyn-productsizes.md)]

[!include [product sizes](includes/EcoResProductStyleEntity-msdyn-productstyles.md)]

[!include [product sizes](includes/EcoResProductConfigurationsEntity-msdyn-productconfigurations.md)]

Wenn ein Produkt unterschiedliche Produktdimensionen (z. B. ein Produktmaster hat Größe und Farbe als Produktdimensionen), jedes eindeutig identifizierbare Produkt (das heißt, jede Produktvariante) ist als Kombination dieser Produktdimensionen definiert. Beispielsweise ist eine Produktnummer B0001 ein extra kleines schwarzes T-Shirt und Produktnummer B0002 ein kleines schwarzes T-Shirt. In diesem Fall werden die vorhandenen Kombinationen von Produktdimensionen definiert. Beispielsweise kann das T-Shirt aus dem vorhergehenden Beispiel extra klein und schwarz, klein und schwarz, mittelgroß und schwarz oder groß und schwarz sein, aber es kann nicht extra groß und schwarz sein. Das bedeutet, die Produktdimensionen, die ein Produktmaster auswählen kann, sind festgelegt, und Varianten können anhand dieser Werte freigegeben werden.

Wenn Sie die Produktdimensionen nachverfolgen möchten, die ein Produktmaster wählen kann, werden die folgenden Entitäten in Common Data Service für jede Produktdimension erstellt und zugeordnet. Weitere Informationen finden Sie unter [Überblick über die Produktinformationen](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/pim/product-information).

[!include [product colors](includes/EcoResProductMasterColorEntity-msdyn-sharedproductcolors.md)]

[!include [product sizes](includes/EcoResProductMasterSize-msdyn-sharedproductsizes.md)]

[!include [product styles](includes/EcoResProductMasterStyleEntity-msdyn-sharedproductstyles.md)]

[!include [product configurations](includes/EcoResProductMasterConfigurationEntity-msdyn-sharedproductconfigurations.md)]

[!include [product bar codes](includes/EcoResProductNumberIdentifiedBarcode-msdyn-productbarcodes.md)]

## <a name="default-order-settings-and-product-specific-default-order-settings"></a>Standardauftragseinstellungen und produktspezifische Standardauftragseinstellungen

Standardauftragseinstellungen definieren den Standort und Lagerort, aus dem Artikel bezogen oder in dem sie gelagert werden, die Mindest-, Höchst-, Mehrfach- und Standardmengen, die für den Handel oder die Lagerverwaltung verwendet werden, die Lieferzeiten, das Beendigungskennzeichen sowie die Auftragszusagemethode. Diese Informationen sind in Common Data Service über die Standardauftragseinstellungen und die Entität für produktspezifische Standardauftragseinstellungen verfügbar. Weitere Informationen zu den Funktionen finden Sie unter [Standardauftragseinstellungen](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/default-order-settings).

[!include [product sizes](includes/InventProductDefaultOrderSettingsEntity-msdyn-productdefaultordersetting.md)]

[!include [product sizes](includes/InventProductSpecificOrderSettingsV2Entity-msdyn-productspecificdefaultordersetting.md)]

## <a name="unit-of-measure-and-unit-of-measure-conversions"></a>Maßeinheit und Maßeinheitsumrechnungen

Die Maßeinheiten und die jeweiligen Umrechungen sind in Common Data Service entsprechend des Datenmodells im Diagramm verfügbar.

![Datenmodell für Produkte](media/dual-write-product-three.png)

Das Maßeinheitskonzept wird in Finance and Operations-Apps und anderen Dynamics 365-Apps integriert. Für jede Einheitenklasse in einer Finance and Operations-App wird eine Einheitengruppe in einer Dynamics 365-App erstellt, die die Einheiten enthält, die zur Einheitenklasse gehören. Eine Standardbasiseinheit wird auch für jede Einheitsgruppe erstellt. 

[!include [unit of measure](includes/UnitOfMeasureEntity-uom.md)]

[!include [unit of measure conversions](includes/UnitOfMeasureConversionEntity-msdyn-unitofmeasureconversions.md)]

[!include [product specific unit of measure conversions](includes/EcoResProductSpecificUnitConversionEntity-msdyn-productspecificunitofmeasureconversions.md)]

## <a name="initial-synchronization-of-units-data-matching-between-finance-and-operations-and-common-data-service"></a>Datenabgleich bei der Erstsynchronisierung zwischen Finance and Operations und Common Data Service

### <a name="initial-synchronization-of-units"></a>Erstsynchronisierung von Einheiten

Wenn die Option für duales Schreiben aktiviert ist, werden Einheiten aus Finance and Operations-Apps mit anderen Dynamics 365-Apps synchronisiert. Die Einheitengruppen, die aus Finance and Operations-Apps in Common Data Service synchronisiert werden, verfügen über eine festgelegte Markierung, die angibt, dass sie „extern verwaltet“ werden.

### <a name="matching-units-and-unit-classesgroups-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>Datenabgleich von Einheiten und Einheitenklassen/-gruppen aus Finance and Operations- und anderen Dynamics 365-Apps

Zunächst ist es wichtig zu beachten, dass der Integrationsschlüssel für die Einheit msdyn_symbol ist. Daher muss dieser Wert in Common Data Service- oder anderen Dynamics 365-Apps eindeutig sein. Da die Eindeutigkeit einer Einheit in anderen Dynamics 365-Apps anhand des Paares „Kennung der Einheitengruppe“ und „Name“ definiert wird, müssen Sie verschiedene Szenarien für den Datenabgleich zwischen Finance and Operations-Apps und Common Data Service berücksichtigen.

Für Einheiten, die in Finance and Operations- und anderen Dynamics 365-Apps übereinstimmen/überlappen:

+ **Die Einheit gehört zu einer Einheitengruppe in anderen Dynamics 365-Apps, die der zugeordneten Einheitenklasse in Finance and Operations-Apps entspricht**. In diesem Fall muss das Feld „msdyn_symbol“ in anderen Dynamics 365-Apps mit dem Einheitensymbol aus Finance and Operations-Apps ausgefüllt werden. Daher wird in anderen Dynamics 365-Apps der Zeitpunkt für den Abgleich der Daten und die Einheitengruppe als „Extern gepflegt“ festgelegt.
+ **Die Einheit gehört zu einer Einheitengruppe in anderen Dynamics 365-Apps, die nicht der zugeordneten Einheitenklasse in Finance and Operations-Apps entspricht (keine vorhandene Einheitenklasse in Finance and Operations-Apps für die Einheitenklasse in anderen Dynamics 365-Apps).** In diesem Fall muss das msdyn_symbol mit einer zufälligen Zeichenfolge ausgefüllt werden. Beachten Sie, dass dieser Wert in anderen Dynamics 365-Apps eindeutig sein muss.

Für Einheiten und Einheitenklassen in Finance and Operations, die nicht in anderen Dynamics 365-Apps vorhanden sind:

Im Rahmen des dualen Schreibens werden die Einheitengruppen aus Finance and Operations-Apps und die entsprechenden Einheiten erstellt und mit anderen Dynamics 365-Apps und Common Data Service synchronisiert und die Einheitengruppe wird als „extern verwaltet“ festgelegt. Es ist kein zusätzlicher Bootstrapping-Aufwand erforderlich.

Für Einheiten in anderen Dynamics 365-Apps, die nicht in Finance and Operations-Apps vorhanden sind:

Dem Feld „msdyn_symbol“ muss für alle Einheiten ausgefüllt werden. Die Einheiten können immer in Finance and Operations-Apps in der entsprechenden Einheitenklasse, sofern vorhanden, erstellt werden. Wenn die Einheitsklasse nicht existiert, muss zuerst die Einheitsklasse erstellt werden (beachten Sie, dass Sie keine Einheitsklasse in Finance and Operations-Apps erstellen können, außer durch Erweiterung, wenn Sie die Aufzählung erweitern), die zu der anderen Einheitsgruppe der Dynamics 365-Apps passt. Dann können Sie die Einheit erstellen. Beachten Sie, dass das Einheitensymbol in Finance and Operations-Apps „msdyn_symbol“ lauten muss, das zuvor in anderen Dynamics 365-Apps für die Einheit angegeben wurde.

## <a name="product-policies-dimension-tracking-and-storage-groups"></a>Produktrichtlinien: Dimension, Nachverfolgung und Lagergruppen

Bei den Produktrichtlinien handelt es sich um Gruppen von Richtlinien, die für die Definition von Produkten und deren Merkmalen im Bestand verwendet werden. Die Produktdimensionsgruppe, die Produktnachverfolgungsdimensionsgruppe und die Lagerdimensionsgruppe können als Produktrichtlinien gefunden werden. 

[!include [product dimension group](includes/EcoResProductDimensionGroup-msdyn-productdimensiongroups.md)]

[!include [product tracking dimension group](includes/EcoResTrackingDimensionGroup-msdyn-producttrackingdimensiongroups.md)]

[!include [product storage dimension group](includes/EcoResStorageDimensionGroup-msdyn-productstoragedimensiongroups.md)]

## <a name="product-hierarchies"></a>Produkthierarchien

[!include [product category hierarchy](includes/EcoResProductCategoryHierarchyEntity-msdyn-productcategoryhierarchy.md)]

[!include [product category](includes/EcoResProductCategoryEntity-msdyn-productcategory.md)]

[!include [product category assignments](includes/EcoResProductCategoryAssignmentEntity-msdyn-productcategoryassignment.md)]

[!include [product category role](includes/EcoResProductCategoryHierarchyRoleEntity-msdyn-productcategoryhierarchyrole.md)]


## <a name="integration-key-for-products"></a>Integrationsschlüssel für Produkte 

Integrationsschlüssel werden verwendet, um Produkte zwischen Dynamics 365 for Finance and Operations und Produkte in Common Data Service eindeutig zu identifizieren. Für Produkte ist **(productnumber)** der eindeutige Schlüssel, der ein Produkt in Common Data Service identifiziert. Sie wird durch die Verkettung von zusammengesetzt: **(Firma, msdyn_productnumber)**. Das **Unternehmen** gibt die juristische Person in Finance and Operations und **msdyn_productnumber** gibt die Produktnummer für das jeweilige Produkt in Finance and Operations an. 

Für einen anderen Benutzer von Dynamics 365-Apps wird das Produkt in der Benutzeroberfläche mit **msdyn_productnumber** gekennzeichnet (beachten Sie, dass die Feldbeschriftung **Produktnummer** lautet). Im Produktformular werden das Unternehmen und das Feld „msydn_productnumber“ angezeigt. Das Feld (productnumber), bei dem es sich um den eindeutigen Schlüssel für ein Produkt handelt, wird jedoch nicht angezeigt. 

Wenn Sie Apps auf Common Data Service aufbauen, sollten Sie darauf achten, dass Sie den Integrationsschlüssel **Produktnummer** (die eindeutige Produkt-ID) verwenden. Verwenden Sie nicht **msdyn_productnumber**, da sie nicht eindeutig ist. 

## <a name="initial-synchronization-of-products-and-migration-of-data-from-common-data-service-to-finance-and-operations"></a>Erstsynchronisierung von Produkten und Migration von Daten aus Common Data Service nach Finance and Operations

### <a name="initial-synchronization-of-products"></a>Erstsynchronisierung von Produkten 

Wenn Dual-Write aktiviert ist, werden Produkte von Finance and Operations-Anwendungen mit Common Data Service und anderen modellgesteuerten Anwendungen in Dynamics 365 synchronisiert. Produkte, die in Common Data Service und anderen Dynamics 365-Anwendungen vor der Freigabe von Dual-Write erstellt wurden, werden nicht aktualisiert oder mit den Produktdaten von Finance and Operations Anwendungen abgeglichen.

### <a name="matching-product-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>Abgleich von Produktdaten aus Finance and Operations- und anderen Dynamics 365-Apps

Wenn identische Produkte (überlappend/übereinstimmend) in Finance and Operations- sowie in Common Data Service- und anderen Dynamics 365-Apps beibehalten werden, findet beim Aktivieren des dualen Schreibens eine Synchronisierung der Produkte aus Finance and Operations statt. In Common Data Service werden für dasselbe Produkt doppelte Datensätze angezeigt.
Um die vorherige Situation zu vermeiden, wenn andere Dynamics 365-Apps mit Finance and Operations überlappende/übereinstimmende Produkte aufweisen, muss der Administrator, der duales Schreiben aktiviert, ein Bootstrap für die Felder **Unternehmen** (Beispiel: „USMF“) und **msdyn_productnumber** (Beispiel: „1234:Black:S“) ausführen, bevor die Produkte synchronisiert werden. Das bedeutet, dass diese beiden Felder des Produkts in Common Data Service mit dem jeweiligen Unternehmen, mit dem das Produkt abgeglichen werden muss, und mit seiner Produktnummer in Finance and Operations ausgefüllt werden müssen. 

Wenn die Synchronisierung aktiviert und ausgeführt wird, werden die Produkte aus Finance and Operations anschließend mit den abgeglichenen Produkten in Common Data Service- und anderen Dynamics 365-Apps synchronisiert. Dies gilt für eindeutig identifizierbare Produkte und für Produktvarianten. 


### <a name="migration-of-product-data-from-other-dynamics-365-apps-to-finance-and-operations"></a>Migration von Produktdaten aus anderen Dynamics 365-Apps zu Finance and Operations

Wenn andere Dynamics 365-Apps Produkte haben, die nicht in Finance and Operations vorhanden sind, kann der Administrator zunächst die **EcoResReleasedProductCreationV2Entity** für den Import dieser Produkte in Finance and Operations verwenden. Und anschließend kann er die Produktdaten aus Finance and Operations- und anderen Dynamics 365-Apps abgleichen, wie oben beschrieben. 
