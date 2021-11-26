---
title: Einheitliche Produkterfahrung
description: In diesem Thema wird die Integration von Produktdaten zwischen Finance and Operations-Apps und Dataverse beschrieben.
author: t-benebo
ms.date: 12/12/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 81f49cf08dcd1b4b1c3d71ff286a1f070e65e914
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782331"
---
# <a name="unified-product-experience"></a>Einheitliche Produktumgebung

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Wenn ein Geschäftsökosystem aus Dynamics 365-Anwendungen besteht, wie Finance, Supply Chain Management und Sales, verwenden Unternehmen diese Anwendungen häufig für Quellproduktdaten. Der Grund dafür ist, dass diese Apps eine robuste Produktinfrastruktur bieten, die durch ausgeklügelte Preiskonzepte und genaue Bestandsverfügbarkeitsdaten abgerundet werden. Unternehmen, die ein externes Product Lifecycle Management (PLM)-System für die Beschaffung von Produktdaten verwenden, können Produkte von Finance and Operations-Apps in andere Dynamics 365-Apps kanalisieren. Die einheitliche Produkterfahrung bringt das integrierte Produktdatenmodell in Dataverse, sodass alle Anwendungsbenutzer einschließlich Power Platform-Benutzer den Vorteil der umfassenden Produktdaten aus Finance and Operations-Apps nutzen können.

Hier ist das Produktdatenmodell aus Sales.

![Datenmodell für Produkte in CE.](media/dual-write-product-4.jpg)

Hier ist das Produktdatenmodell aus Finance and Operations-Apps.

![Datenmodell für Produkte in Finance and Operations.](media/dual-write-products-5.jpg)

Diese beiden Produktdatenmodelle wurden wie unten dargestellt in Dataverse integriert.

![Datenmodell für Produkte in Dynamics 365-Apps.](media/dual-write-products-6.jpg)

Die Tabellenzuordnungen für duales Schreiben sind so konzipiert, dass Daten nur unidirektional weitergeleitet werden. Dies erfolgt nahezu in Echtzeit von Finance and Operations-Apps nach Dataverse. Allerdings wurde die Produktinfrastruktur offen gestaltet, um sie bei Bedarf auch bidirektional nutzen zu können. Obwohl Sie sie auf eigene Gefahr anpassen können, empfiehlt Microsoft diese Methode nicht.

## <a name="templates"></a>Vorlagen

Produktinformationen enthält alle Informationen, die mit dem Produkt und seiner Definition in Verbindung stehen, z. B. den Produktdimensionen oder den Nachverfolgungs- und Lagerdimensionen. Wie die folgende Tabelle zeigt, wird eine Sammlung von Tabellenzuordnungen erstellt, um Produkte und zugehörige Informationen zu synchronisieren.

Finance and Operations Apps | Sonstige Dynamics 365-Apps | Beschreibung
-----------------------|--------------------------------|---
[Alle Produkte](mapping-reference.md#138) | msdyn_globalproducts | Die Tabelle „Alle Produkte“ enthält alle in Finance and Operations-Apps verfügbaren Produkte, sowohl die freigegebenen als auch die nicht freigegebenen.
[Von CDS freigegebene eindeutig identifizierbare Produkte](mapping-reference.md#213) | Produkt | Die Tabelle **Produkt** enthält die Spalten, die das Produkt definieren. Sie enthält Einzelprodukte (Produkte mit Untertypprodukt) und die Produktvarianten. Die Zuordnungen werden in der folgenden Tabelle veranschaulicht.
[Farben](mapping-reference.md#170) | msdyn\_productcolors
[Varianten](mapping-reference.md#171) | msdyn\_productconfigurations
[Standardauftragseinstellungen](mapping-reference.md#172) | msdyn_productdefaultordersettings |
[Produktkategorien](mapping-reference.md#166) | msdyn_productcategories | Jede der Produktkategorien und -informationen über die Struktur und Eigenschaften ist in der Produktkategorietabelle enthalten.
[Produktkategoriezuweisungen](mapping-reference.md#167) | msdyn_productcategoryassignments | Zum Zuweisen eines Produkts zu einer Kategorie kann die Tabelle „Produktkategoriezuweisungen“ verwendet werden.
[Produktkategoriehierarchien](mapping-reference.md#168) | msdyn_productcategoryhierarchies | Sie verwenden Produkthierarchien, um Produkte zu kategorisieren oder zu gruppieren. Die Kategoriehierarchien sind in Dataverse über die Tabelle „Produktkategoriehierarchie“ verfügbar.
[Produktkategoriehierarchie-Rollen](mapping-reference.md#169) | msdyn_productcategoryhierarchyrole | Produkthierarchien können für verschiedene Rollen in D365 Finance and Operations verwendet werden. Sie legen fest, welche Kategorie in jeder Rolle verwendet wird, in der die Tabelle „Produktkategorierolle“ verwendet wird.
[Standardmäßige Produktauftragseinstellungen V2](mapping-reference.md#175) | msdyn_productspecificdefaultordersettings |
[Produktdimensionsgruppen](mapping-reference.md#173) | msdyn\_productdimensiongroups | Die Produktdimensionsgruppe definierten, welche Produktdimensionen das Produkt definieren.
[Produktmasterfarben](mapping-reference.md#187) | msdyn_sharedproductcolors | Die Tabelle **Freigegebene Produktfarbe** gibt die Farben an, die ein bestimmter Produktmaster haben kann. Dieses Konzept wird zu Dataverse migriert, um Daten einheitlich zu halten.
[Produktmasterkonfigurationen](mapping-reference.md#188) | msdyn_sharedproductconfigurations | Die Tabelle **Freigegebener Produktkonfiguration** gibt die Konfigurationen an, die ein bestimmter Produktmaster haben kann. Dieses Konzept wird zu Dataverse migriert, um Daten einheitlich zu halten.
[Produktmastergrößen](mapping-reference.md#190) | msdyn_sharedproductsizes | Die Tabelle **Freigegebene Produktgröße** gibt die Größen an, die ein bestimmter Produktmaster haben kann. Dieses Konzept wird zu Dataverse migriert, um Daten einheitlich zu halten.
[Produktmasterstile](mapping-reference.md#191) | msdyn_sharedproductstyles | Die Tabelle **Freigegebener Produktstil** gibt die Stile an, die ein bestimmter Produktmaster haben kann. Dieses Konzept wird zu Dataverse migriert, um Daten einheitlich zu halten.
[Durch Produktnummer identifizierter Strichcode](mapping-reference.md#164) | msdyn\_productbarcodes | Produktstrichcodes werden verwendet, um Produkte eindeutig zu kennzeichnen.
[Produktspezifische Einheitenumrechnungen](mapping-reference.md#176) | msdyn_productspecificunitofmeasureconversions |
[Freigegebene Produkte V2](mapping-reference.md#189) | msdyn\_sharedproductdetails | Die Tabelle **msdyn\_sharedproductdetails** enthält die Spalten aus Finance and Operations-Apps, die das Produkt definieren und die die Finanz- und Verwaltungsinformationen des Produkts enthalten.
[Größen](mapping-reference.md#174) | msdyn\_productsizes
[Lagerdimensionsgruppen](mapping-reference.md#177) | msdyn_productstoragedimensiongroups | Die Produkt-Lagerdimensionsgruppe stellt die Methode dar, die verwendet wird, um die Position des Produkts im Lagerort zu definieren.
[Stile](mapping-reference.md#178) | msdyn\_productsytles
[Rückverfolgungsangabengruppen](mapping-reference.md#179) | msdyn_producttrackingdimensiongroups | Die Produktnachverfolgungsdimensionsgruppe stellt die Methode dar, die verwendet wird, um das Produkt im Bestand nachzuverfolgen.
[Einheiten](mapping-reference.md#219) | uoms
[Einheitenumrechnungen](mapping-reference.md#199) | msdyn_ unitofmeasureconversions

## <a name="integration-of-products"></a>Integration von Produkten

In diesem Modell wird das Produkt durch die Kombination aus beiden Tabellen in Dataverse dargestellt: **Produkt** und **msdyn\_sharedproductdetails**. Während in der ersten Tabelle die Definition eines Produkts (den eindeutige Bezeichner für das Produkt, den Produktnamen und die Beschreibung) enthalten ist, enthält die zweite Tabelle die Spalten, die auf der Produktebene gespeichert werden. Die Kombination aus diesen beiden Tabellen wird verwendet, um das Produkt entsprechend des Konzepts der Lagermengeneinheit (SKU) zu definieren. Jedes freigegebene Produkt hat seine Informationen in den genannten Tabellen (Produkt und freigegebene Produktdetails). Um sämtliche Produkte zu verfolgen (freigegebene und nicht freigegebene), wird die Tabelle **Globale Produkte** verwendet.

Da das Produkt als SKU dargestellt wird, können die Konzepte von eindeutig identifizierbaren Produkten, Produktmastern und Produktvarianten in Dataverse folgendermaßen erfasst werden:

- **Produkte mit Untertypprodukt** sind Produkte, die auch durch sie selbst definiert werden. Es müssen keine Dimensionen festgelegt werden. Ein Beispiel ist ein bestimmtes Buch. Für diese Produkte wird eine Zeile in der Tabelle **Produkt** und eine Zeile in der Tabelle **msdyn\_sharedproductdetails** erstellt. Es wird keine Produktfamilienzeile erstellt.
- **Produktmaster** werden als generische Produkte verwendet, die die Definition und die Regeln verwenden, mit denen das Verhalten in Geschäftsprozessen bestimmt wird. Auf Grundlage dieser Definitionen können eindeutig identifizierbare Produkte, bekannt als Produktvarianten, generiert werden. Beispielsweise ist das T-Shirt der Produktmaster, und es kann Farbe und Größe als Dimensionen haben. Varianten können freigegeben werden, die unterschiedliche Kombinationen dieser Dimensionen aufweisen, z. B. ein kleines blaues T-Shirt oder ein mittelgroßes grünes T-Shirt. In der Integration wird eine Zeile pro Variante in der Produkttabelle erstellt. Diese Zeile enthält die variantenspezifischen Informationen, wie beispielsweise die verschiedenen Dimensionen. Die allgemeinen Informationen für das Produkt werden in der Tabelle **msdyn\_sharedproductdetails** gespeichert. (Diese allgemeinen Informationen werden im Produktmaster gespeichert.) Die Produktmasterinformationen werden mit Dataverse synchronisiert, sobald der freigegebene Produktmaster erstellt wird (aber bevor die Varianten freigegeben werden).
- **Eindeutig identifizierbare Produkte** verweisen auf alle Produktuntertypprodukte und alle Produktvarianten an.

![Datenmodell für Produkte.](media/dual-write-product.png)

Wenn die Dual-Write-Funktionalität aktiviert ist, werden die Produkte aus Finance and Operations in anderen Dynamics 365-Produkten im Zustand **Entwurf** synchronisiert. Sie werden der ersten Preisliste mit der gleichen Währung hinzugefügt, die in der Customer-Engagement-App verwendet wird, und unter Verwendung der alphabetischen Sortierung des Preislistennamens. Das bedeutet, sie werden der ersten Preisliste in einer Dynamics 365-App hinzugefügt, die mit der Währung Ihrer juristischen Tabelle übereinstimmt, in der das Produkt in einer Finance and Operations-App freigegeben wird. Wenn für die angegebene Währung keine Preisliste vorhanden ist, wird automatisch eine Preisliste erstellt und das Produkt dieser zugewiesen.

Die aktuelle Implementierung der Plugins für duales Schreiben, die der Einheit die Standardpreisliste zuordnet, nach der mit der Finance and Operations-App verknüpften Währung sucht und die erste Preisliste in der Kundenbindungs-App mithilfe alphabetischer Sortierung der Preislistennamen findet. Wenn Sie mehrere Preislisten für eine Währung haben und eine Standardpreisliste für diese Währung festlegen möchten, müssen Sie den Preislistennamen auf einen Namen aktualisieren, der in der alphabetischen Reihenfolge früher erscheint als alle anderen Preislisten derselben Währung. Wenn es keine Preisliste für die angegebene Währung gibt, wird eine neue erstellt.

Produkte aus Finance and Operations-Apps werden standardmäßig mit anderen Dynamics 365-Apps im Status **Entwurf** synchronisiert. Um das Produkt mit dem Status **Aktiv** zu synchronisieren, können Sie es direkt in Auftragsangeboten verwenden, beispielsweise muss die folgende Einstellung ausgewählt werden. Wechseln Sie dazu zur Registerkarte **System > Verwaltung > Systemverwaltung > Systemeinstellungen > Verkauf**, und wählen Sie **Produkte im Status „Aktiv“ erstellen = ja** aus.

Wenn Produkte synchronisiert werden, müssen Sie einen Wert in das Feld **Verkaufseinheit** in der Finance and Operations-App eingeben, weil es in Sales ein Pflichtfeld ist.

Die Erstellung von Produktfamilien aus Dynamics 365 Sales wird bei der Synchronisierung von Produkten über duales Schreiben nicht unterstützt.

Die Synchronisierung der Produkte erfolgt von den Finance and Operations-Apps nach Dataverse. Das bedeutet, dass die Werte in den Spalten der Produkttabelle in Dataverse zwar geändert werden können, die Werte beim Auslösen der Synchronisierung (durch Ändern einer Produktspalte in einer Finance and Operations-App) in Dataverse jedoch überschrieben werden.

Finance and Operations-Apps | Customer Engagement-Apps |
---|---
[Von CDS freigegebene eindeutig identifizierbare Produkte](mapping-reference.md#213) | Produkt |
[Freigegebene Produkte V2](mapping-reference.md#189) | msdyn_sharedproductdetails |
[Alle Produkte](mapping-reference.md#138) | msdyn_globalproducts |

## <a name="product-dimensions"></a>Produktdimensionen

Produktdimensionen sind Merkmale, die eine Produktvariante identifizieren. Die vier Produktdimensionen (Farbe, Größe, Stil und Konfiguration) werden auch Dataverse zugeordnet, um die Produktvarianten zu definieren. Die folgende Abbildung zeigt das Datenmodell für die Produktdimension „Farbe”. Dasselbe Modell wird auf die Größen, Stile und Konfigurationen angewendet.

![Datenmodell für Produktdimensionen.](media/dual-write-product-two.png)

Finance and Operations-Apps | Customer Engagement-Apps |
---|---
[Farben](mapping-reference.md#170) | msdyn\_productcolors
[Größen](mapping-reference.md#174) | msdyn\_productsizes
[Stile](mapping-reference.md#178) | msdyn\_productsytles
[Varianten](mapping-reference.md#171) | msdyn\_productconfigurations

Wenn ein Produkt unterschiedliche Produktdimensionen (z. B. ein Produktmaster hat Größe und Farbe als Produktdimensionen), jedes eindeutig identifizierbare Produkt (das heißt, jede Produktvariante) ist als Kombination dieser Produktdimensionen definiert. Beispielsweise ist eine Produktnummer B0001 ein extra kleines schwarzes T-Shirt und Produktnummer B0002 ein kleines schwarzes T-Shirt. In diesem Fall werden die vorhandenen Kombinationen von Produktdimensionen definiert. Beispielsweise kann das T-Shirt aus dem vorhergehenden Beispiel extra klein und schwarz, klein und schwarz, mittelgroß und schwarz oder groß und schwarz sein, aber es kann nicht extra groß und schwarz sein. Das bedeutet, die Produktdimensionen, die ein Produktmaster auswählen kann, sind festgelegt, und Varianten können anhand dieser Werte freigegeben werden.

Wenn Sie die Produktdimensionen nachverfolgen möchten, die ein Produktmaster wählen kann, werden die folgenden Tabellen in Dataverse für jede Produktdimension erstellt und zugeordnet. Weitere Informationen finden Sie unter [Überblick über die Produktinformationen](../../../../supply-chain/pim/product-information.md).

Finance and Operations-Apps | Customer Engagement-Apps |
---|---
[Produktmasterfarben](mapping-reference.md#187) | msdyn_sharedproductcolors |
[Produktmasterkonfigurationen](mapping-reference.md#188) | msdyn_sharedproductconfigurations |
[Produktmastergrößen](mapping-reference.md#190) | msdyn_sharedproductsizes |
[Produktmasterstile](mapping-reference.md#191) | msdyn_sharedproductstyles |
[Durch Produktnummer identifizierter Strichcode](mapping-reference.md#164) | msdyn\_productbarcodes |

## <a name="default-order-settings-and-product-specific-default-order-settings"></a>Standardauftragseinstellungen und produktspezifische Standardauftragseinstellungen

Standardauftragseinstellungen definieren den Standort und Lagerort, aus dem Artikel bezogen oder in dem sie gelagert werden, die Mindest-, Höchst-, Mehrfach- und Standardmengen, die für den Handel oder die Lagerverwaltung verwendet werden, die Lieferzeiten, das Beendigungskennzeichen sowie die Auftragszusagemethode. Diese Informationen sind in Dataverse über die Standardauftragseinstellungen und die Entität für produktspezifische Standardauftragseinstellungen verfügbar. Weitere Informationen zu den Funktionen finden Sie unter [Standardauftragseinstellungen](../../../../supply-chain/production-control/default-order-settings.md).

Finance and Operations-Apps | Customer Engagement-Apps |
---|---
[Standardauftragseinstellungen](mapping-reference.md#172) | msdyn_productdefaultordersettings |
[Standardmäßige Produktauftragseinstellungen V2](mapping-reference.md#175) | msdyn_productspecificdefaultordersettings |

## <a name="unit-of-measure-and-unit-of-measure-conversions"></a>Maßeinheit und Maßeinheitsumrechnungen

Die Maßeinheiten und die jeweilige Umrechung sind in Dataverse entsprechend dem im Diagramm angezeigten Datenmodell verfügbar.

![Datenmodell für Maßeinheit.](media/dual-write-product-three.png)

Das Maßeinheitskonzept wird in Finance and Operations-Apps und anderen Dynamics 365-Apps integriert. Für jede Einheitenklasse in einer Finance and Operations-App wird eine Einheitengruppe in einer Dynamics 365-App erstellt, die die Einheiten enthält, die zur Einheitenklasse gehören. Eine Standardbasiseinheit wird auch für jede Einheitsgruppe erstellt.

Finance and Operations-Apps | Customer Engagement-Apps |
---|---
[Produktspezifische Einheitenumrechnungen](mapping-reference.md#176) | msdyn_productspecificunitofmeasureconversions |
[Einheiten](mapping-reference.md#219) | uoms
[Einheitenumrechnungen](mapping-reference.md#199) | msdyn_ unitofmeasureconversions

## <a name="initial-synchronization-of-units-data-matching-between-finance-and-operations-and-dataverse"></a>Datenabgleich bei der Erstsynchronisierung zwischen Finance and Operations und Dataverse

### <a name="initial-synchronization-of-units"></a>Erstsynchronisierung von Einheiten

Wenn die Option für duales Schreiben aktiviert ist, werden Einheiten aus Finance and Operations-Apps mit anderen Dynamics 365-Apps synchronisiert. Die Einheitengruppen, die aus Finance and Operations-Apps in Dataverse synchronisiert werden, verfügen über eine festgelegte Markierung, die angibt, dass sie „extern verwaltet“ werden.

### <a name="matching-units-and-unit-classesgroups-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>Datenabgleich von Einheiten und Einheitenklassen/-gruppen aus Finance and Operations- und anderen Dynamics 365-Apps

Zunächst ist es wichtig zu beachten, dass der Integrationsschlüssel für die Einheit msdyn_symbol ist. Daher muss dieser Wert in Dataverse- oder anderen Dynamics 365-Apps eindeutig sein. Da die Eindeutigkeit einer Einheit in anderen Dynamics 365-Apps anhand des Paares „Kennung der Einheitengruppe“ und „Name“ definiert wird, müssen Sie verschiedene Szenarien für den Datenabgleich zwischen Finance and Operations-Apps und Dataverse berücksichtigen.

Für Einheiten, die in Finance and Operations- und anderen Dynamics 365-Apps übereinstimmen/überlappen:

+ **Die Einheit gehört zu einer Einheitengruppe in anderen Dynamics 365-Apps, die der zugeordneten Einheitenklasse in Finance and Operations-Apps entspricht**. In diesem Fall muss die Spalte „msdyn_symbol“ in anderen Dynamics 365-Apps mit dem Einheitensymbol aus Finance and Operations-Apps ausgefüllt werden. Daher wird in anderen Dynamics 365-Apps der Zeitpunkt für den Abgleich der Daten und die Einheitengruppe als „Extern gepflegt“ festgelegt.
+ **Die Einheit gehört zu einer Einheitengruppe in anderen Dynamics 365-Apps, die nicht der zugeordneten Einheitenklasse in Finance and Operations-Apps entspricht (keine vorhandene Einheitenklasse in Finance and Operations-Apps für die Einheitenklasse in anderen Dynamics 365-Apps).** In diesem Fall muss das msdyn_symbol mit einer zufälligen Zeichenfolge ausgefüllt werden. Beachten Sie, dass dieser Wert in anderen Dynamics 365-Apps eindeutig sein muss.

Für Einheiten und Einheitenklassen in Finance and Operations, die nicht in anderen Dynamics 365-Apps vorhanden sind:

Im Rahmen des dualen Schreibens werden die Einheitengruppen aus Finance and Operations-Apps und die entsprechenden Einheiten erstellt und mit anderen Dynamics 365-Apps und Dataverse synchronisiert und die Einheitengruppe wird als „Extern verwaltet“ festgelegt. Es ist kein zusätzlicher Bootstrapping-Aufwand erforderlich.

Für Einheiten in anderen Dynamics 365-Apps, die nicht in Finance and Operations-Apps vorhanden sind:

Die Spalte „msdyn_symbol“ muss für alle Einheiten ausgefüllt werden. Die Einheiten können immer in Finance and Operations-Apps in der entsprechenden Einheitenklasse, sofern vorhanden, erstellt werden. Wenn die Einheitsklasse nicht existiert, muss zuerst die Einheitsklasse erstellt werden (beachten Sie, dass Sie keine Einheitsklasse in Finance and Operations-Apps erstellen können, außer durch Erweiterung, wenn Sie die Aufzählung erweitern), die zu der anderen Einheitsgruppe der Dynamics 365-Apps passt. Dann können Sie die Einheit erstellen. Beachten Sie, dass das Einheitensymbol in Finance and Operations-Apps „msdyn_symbol“ lauten muss, das zuvor in anderen Dynamics 365-Apps für die Einheit angegeben wurde.

## <a name="product-policies-dimension-tracking-and-storage-groups"></a>Produktrichtlinien: Dimension, Nachverfolgung und Lagergruppen

Bei den Produktrichtlinien handelt es sich um Gruppen von Richtlinien, die für die Definition von Produkten und deren Merkmalen im Bestand verwendet werden. Die Produktdimensionsgruppe, die Produktnachverfolgungsdimensionsgruppe und die Lagerdimensionsgruppe können als Produktrichtlinien gefunden werden.

Finance and Operations-Apps | Customer Engagement-Apps |
---|---
[Produktdimensionsgruppen](mapping-reference.md#173) | msdyn\_productdimensiongroups |
[Lagerdimensionsgruppen](mapping-reference.md#177) | msdyn_productstoragedimensiongroups |
[Rückverfolgungsangabengruppen](mapping-reference.md#179) | msdyn_producttrackingdimensiongroups |

## <a name="product-hierarchies"></a>Produkthierarchien

Finance and Operations-Apps | Customer Engagement-Apps |
---|---
[Produktkategoriezuweisungen](mapping-reference.md#167) | msdyn_productcategoryassignments |
[Produktkategoriehierarchien](mapping-reference.md#168) | msdyn_productcategoryhierarchies |
[Produktkategoriehierarchie-Rollen](mapping-reference.md#169) | msdyn_productcategoryhierarchyrole |

## <a name="integration-key-for-products"></a>Integrationsschlüssel für Produkte

Integrationsschlüssel werden verwendet, um Produkte zwischen Dynamics 365 for Finance and Operations und Produkte in Dataverse eindeutig zu identifizieren.
Für Produkte ist **(productnumber)** der eindeutige Schlüssel, der ein Produkt in Dataverse identifiziert. Sie wird durch die Verkettung von zusammengesetzt: **(Firma, msdyn_productnumber)**. Das **Unternehmen** gibt die juristische Person in Finance and Operations und **msdyn_productnumber** gibt die Produktnummer für das jeweilige Produkt in Finance and Operations an.

Für Benutzer anderer Dynamics 365-Apps wird das Produkt in der Benutzeroberfläche mit **msdyn_productnumber** gekennzeichnet (beachten Sie, dass die Spaltenbeschriftung **Produktnummer** lautet). Im Produktformular werden das Unternehmen und das Feld „msydn_productnumber“ angezeigt. Die Spalte (productnumber), bei der es sich um den eindeutigen Schlüssel für ein Produkt handelt, wird jedoch nicht angezeigt.

Wenn Sie Apps auf Dataverse aufbauen, sollten Sie darauf achten, dass Sie den Integrationsschlüssel **Produktnummer** (die eindeutige Produkt-ID) verwenden. Verwenden Sie nicht **msdyn_productnumber**, da sie nicht eindeutig ist.

## <a name="initial-synchronization-of-products-and-migration-of-data-from-dataverse-to-finance-and-operations"></a>Erstsynchronisierung von Produkten und Migration von Daten aus Dataverse nach Finance and Operations

### <a name="initial-synchronization-of-products"></a>Erstsynchronisierung von Produkten

Wenn Dual-Write aktiviert ist, werden Produkte aus Finance and Operations-Apps nach Dataverse und Customer Engagement-Apps synchronisiert. Produkte, die in Dataverse und anderen Dynamics 365-Anwendungen vor der Freigabe von Dual-Write erstellt wurden, werden nicht aktualisiert oder mit den Produktdaten von Finance and Operations Anwendungen abgeglichen.

### <a name="matching-product-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>Abgleich von Produktdaten aus Finance and Operations- und anderen Dynamics 365-Apps

Wenn identische Produkte (überlappend/übereinstimmend) in Finance and Operations-Apps sowie in Dataverse und anderen Dynamics 365-Apps beibehalten werden, findet bei Aktivierung von Dual-Write eine Synchronisierung der Produkte von Finance and Operations statt und in Dataverse werden für dasselbe Produkt doppelte Zeilen angezeigt.
Um die vorherige Situation zu vermeiden, wenn andere Dynamics 365-Apps mit Finance and Operations überlappende/übereinstimmende Produkte aufweisen, muss der Administrator, der Dual-Write aktiviert, ein Bootstrap für die Spalten **Unternehmen** (Beispiel: „USMF“) und **msdyn_productnumber** (Beispiel: „1234:Black:S“) ausführen, bevor die Produkte synchronisiert werden. Das bedeutet, dass diese beiden Spalten des Produkts in Dataverse mit dem jeweiligen Unternehmen, mit dem das Produkt abgeglichen werden muss, und mit seiner Produktnummer in Finance and Operations ausgefüllt werden müssen.

Wenn die Synchronisierung aktiviert und ausgeführt wird, werden die Produkte aus Finance and Operations anschließend mit den abgeglichenen Produkten in Dataverse- und anderen Dynamics 365-Apps synchronisiert. Dies gilt für eindeutig identifizierbare Produkte und für Produktvarianten.

### <a name="migration-of-product-data-from-other-dynamics-365-apps-to-finance-and-operations"></a>Migration von Produktdaten aus anderen Dynamics 365-Apps zu Finance and Operations

Wenn andere Dynamics 365-Apps Produkte haben, die nicht in Finance and Operations vorhanden sind, kann der Administrator zunächst die **EcoResReleasedProductCreationV2Entity** für den Import dieser Produkte in Finance and Operations verwenden. Und anschließend kann er die Produktdaten aus Finance and Operations- und anderen Dynamics 365-Apps abgleichen, wie oben beschrieben.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
