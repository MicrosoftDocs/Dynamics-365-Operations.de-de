---
title: Einheitliche Produktumgebung
description: Dieser Artikel beschreibt die Integration von Produktdaten zwischen Finanz- und Betriebs-Apps und Dataverse.
author: t-benebo
ms.date: 06/23/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 89ef56510ec971ef97fc9eb5c80768527abf5f88
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288921"
---
# <a name="unified-product-experience"></a>Einheitliche Produktumgebung

[!include [banner](../../includes/banner.md)]



Wenn ein Geschäftsökosystem aus Dynamics 365-Anwendungen besteht, wie Finance, Supply Chain Management und Sales, verwenden Unternehmen diese Anwendungen häufig für Quellproduktdaten. Der Grund dafür ist, dass diese Apps eine robuste Produktinfrastruktur bieten, die durch ausgeklügelte Preiskonzepte und genaue Bestandsverfügbarkeitsdaten abgerundet werden. Unternehmen, die ein externes Product Lifecycle Management (PLM)-System für die Beschaffung von Produktdaten verwenden, können Produkte aus den Finanz- und Betriebs-Apps in andere Dynamics 365-Apps kanalisieren. Die vereinheitlichte Produkterfahrung bringt das integrierte Produktdatenmodell in Dataverse, sodass alle Benutzer der Anwendungen, einschließlich der Power Platform-Benutzer, die reichhaltigen Produktdaten aus den Finanz- und Betriebs-Apps nutzen können.

Hier ist das Produktdatenmodell aus Sales.

![Datenmodell für Produkte in CE.](media/dual-write-product-4.jpg)

Hier ist das Produktdatenmodell von Finanz- und Betriebs-Apps.

![Datenmodell für Produkte in Finanzen und Betrieb.](media/dual-write-products-5.jpg)

Diese beiden Produktdatenmodelle wurden wie unten dargestellt in Dataverse integriert.

![Datenmodell für Produkte in Dynamics 365-Apps.](media/dual-write-products-6.jpg)

Die Dual-write Table Maps für Produkte wurden so konzipiert, dass Daten nur in eine Richtung fließen, und zwar nahezu in Echtzeit von Finanz- und Betriebs-Apps zu Dataverse. Allerdings wurde die Produktinfrastruktur offen gestaltet, um sie bei Bedarf auch bidirektional nutzen zu können. Obwohl Sie sie auf eigene Gefahr anpassen können, empfiehlt Microsoft diese Methode nicht.

## <a name="templates"></a>Vorlagen

Produktinformationen enthält alle Informationen, die mit dem Produkt und seiner Definition in Verbindung stehen, z. B. den Produktdimensionen oder den Nachverfolgungs- und Lagerdimensionen. Wie die folgende Tabelle zeigt, wird eine Sammlung von Tabellenzuordnungen erstellt, um Produkte und zugehörige Informationen zu synchronisieren.

Finanz- und Betriebs-Apps | Sonstige Dynamics 365-Apps | Description
-----------------------|--------------------------------|---
[Alle Produkte](mapping-reference.md#138) | msdyn_globalproducts | Die Tabelle Alle Produkte enthält alle in Finanz- und Betriebs-Apps verfügbaren Produkte, sowohl die freigegebenen als auch die nicht freigegebenen Produkte.
[Von CDS freigegebene eindeutig identifizierbare Produkte](mapping-reference.md#213) | Produkt | Die Tabelle **Produkt** enthält die Spalten, die das Produkt definieren. Sie enthält Einzelprodukte (Produkte mit Untertypprodukt) und die Produktvarianten. Die Zuordnungen werden in der folgenden Tabelle veranschaulicht.
[Farben](mapping-reference.md#170) | msdyn\_productcolors
[Varianten](mapping-reference.md#171) | msdyn\_productconfigurations
[Standardauftragseinstellungen](mapping-reference.md#172) | msdyn_productdefaultordersettings |
[Produktkategorien](mapping-reference.md#166) | msdyn_productcategories | Jede der Produktkategorien und -informationen über die Struktur und Eigenschaften ist in der Produktkategorietabelle enthalten.
[Produktkategoriezuweisungen](mapping-reference.md#167) | msdyn_productcategoryassignments | Zum Zuweisen eines Produkts zu einer Kategorie kann die Tabelle „Produktkategoriezuweisungen“ verwendet werden.
[Produktkategoriehierarchien](mapping-reference.md#168) | msdyn_productcategoryhierarchies | Sie verwenden Produkthierarchien, um Produkte zu kategorisieren oder zu gruppieren. Die Kategoriehierarchien sind in Dataverse über die Tabelle „Produktkategoriehierarchie“ verfügbar.
[Produktkategoriehierarchie-Rollen](mapping-reference.md#169) | msdyn_productcategoryhierarchyrole | Produkthierarchien können für verschiedene Rollen in D365 Finanzen und Betrieb verwendet werden. Sie legen fest, welche Kategorie in jeder Rolle verwendet wird, in der die Tabelle „Produktkategorierolle“ verwendet wird.
[Standardmäßige Produktauftragseinstellungen V2](mapping-reference.md#175) | msdyn_productspecificdefaultordersettings |
[Produktdimensionsgruppen](mapping-reference.md#173) | msdyn\_productdimensiongroups | Die Produktdimensionsgruppe definierten, welche Produktdimensionen das Produkt definieren.
[Produktmasterfarben](mapping-reference.md#187) | msdyn_sharedproductcolors | Die Tabelle **Freigegebene Produktfarbe** gibt die Farben an, die ein bestimmter Produktmaster haben kann. Dieses Konzept wird zu Dataverse migriert, um Daten einheitlich zu halten.
[Produktmasterkonfigurationen](mapping-reference.md#188) | msdyn_sharedproductconfigurations | Die Tabelle **Freigegebener Produktkonfiguration** gibt die Konfigurationen an, die ein bestimmter Produktmaster haben kann. Dieses Konzept wird zu Dataverse migriert, um Daten einheitlich zu halten.
[Produktmastergrößen](mapping-reference.md#190) | msdyn_sharedproductsizes | Die Tabelle **Freigegebene Produktgröße** gibt die Größen an, die ein bestimmter Produktmaster haben kann. Dieses Konzept wird zu Dataverse migriert, um Daten einheitlich zu halten.
[Produktmasterstile](mapping-reference.md#191) | msdyn_sharedproductstyles | Die Tabelle **Freigegebener Produktstil** gibt die Stile an, die ein bestimmter Produktmaster haben kann. Dieses Konzept wird zu Dataverse migriert, um Daten einheitlich zu halten.
[Durch Produktnummer identifizierter Strichcode](mapping-reference.md#164) | msdyn\_productbarcodes | Produktstrichcodes werden verwendet, um Produkte eindeutig zu kennzeichnen.
[Produktspezifische Einheitenumrechnungen](mapping-reference.md#176) | msdyn_productspecificunitofmeasureconversions |
[Freigegebene Produkte V2](mapping-reference.md#189) | msdyn\_sharedproductdetails | Die Tabelle **msdyn\_sharedproductdetails** enthält die Spalten aus Finanz- und Betriebs-Apps, die das Produkt definieren und die die Finanz- und Verwaltungsinformationen des Produkts enthalten.
[Größen](mapping-reference.md#174) | msdyn\_productsizes
[Lagerdimensionsgruppen](mapping-reference.md#177) | msdyn_productstoragedimensiongroups | Die Produkt-Lagerdimensionsgruppe stellt die Methode dar, die verwendet wird, um die Position des Produkts im Lagerort zu definieren.
[Stile](mapping-reference.md#178) | msdyn\_productstyles
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

Wenn die Dual-write-Funktionalität aktiviert ist, werden die Produkte aus Finanzen und Betrieb in anderen Dynamics 365 Produkten im Status **Draft** synchronisiert. Sie werden der ersten Preisliste mit der gleichen Währung hinzugefügt, die in der Customer-Engagement-App verwendet wird, und unter Verwendung der alphabetischen Sortierung des Preislistennamens. Mit anderen Worten, sie werden der ersten Preisliste in einer Dynamics 365 App hinzugefügt, die mit der Währung Ihrer gesetzlichen Tabelle übereinstimmt, in der das Produkt in einer Finanz- und Betriebs-App freigegeben ist. Wenn für die angegebene Währung keine Preisliste vorhanden ist, wird automatisch eine Preisliste erstellt und das Produkt dieser zugewiesen.

Die derzeitige Implementierung der Dual-write-Plugins, die die Standardpreisliste mit der Einheit verknüpfen, suchen nach der Währung, die mit der Finanz- und Betriebs-App verbunden ist, und finden die erste Preisliste in der Customer-Engagement-App anhand der alphabetischen Sortierung des Preislistennamens. Wenn Sie mehrere Preislisten für eine Währung haben und eine Standardpreisliste für diese Währung festlegen möchten, müssen Sie den Preislistennamen auf einen Namen aktualisieren, der in der alphabetischen Reihenfolge früher erscheint als alle anderen Preislisten derselben Währung. Wenn es keine Preisliste für die angegebene Währung gibt, wird eine neue erstellt.

Standardmäßig werden Produkte aus Finanz- und Betriebs-Apps mit anderen Dynamics 365 Apps im Status **Entwurf** synchronisiert. Um das Produkt mit dem Status **Aktiv** zu synchronisieren, können Sie es direkt in Auftragsangeboten verwenden, beispielsweise muss die folgende Einstellung ausgewählt werden. Wechseln Sie dazu zur Registerkarte **System > Verwaltung > Systemverwaltung > Systemeinstellungen > Verkauf**, und wählen Sie **Produkte im Status „Aktiv“ erstellen = ja** aus.

Wenn Produkte synchronisiert werden, müssen Sie in der Finanz- und Betriebs-App einen Wert für das Feld **Verkaufseinheit** eingeben, da es sich um ein Pflichtfeld im Verkauf handelt.

Die Erstellung von Produktfamilien aus Dynamics 365 Sales wird bei der Synchronisierung von Produkten über duales Schreiben nicht unterstützt.

Die Synchronisierung von Produkten erfolgt von der Finanz- und Betriebs-App auf Dataverse. Das bedeutet, dass die Werte der Produkttabellenspalten in Dataverse geändert werden können, aber wenn die Synchronisierung ausgelöst wird (wenn eine Produktspalte in einer Finanz- und Betriebs-App geändert wird), überschreibt dies die Werte in Dataverse.

Finanz- und Betriebs-Apps | Customer Engagement-Apps |
---|---
[Von CDS freigegebene eindeutig identifizierbare Produkte](mapping-reference.md#213) | Produkt |
[Freigegebene Produkte V2](mapping-reference.md#189) | msdyn_sharedproductdetails |
[Alle Produkte](mapping-reference.md#138) | msdyn_globalproducts |

## <a name="product-dimensions"></a>Produktdimensionen

Produktdimensionen sind Merkmale, die eine Produktvariante identifizieren. Die vier Produktdimensionen (Farbe, Größe, Stil und Konfiguration) werden auch Dataverse zugeordnet, um die Produktvarianten zu definieren. Die folgende Abbildung zeigt das Datenmodell für die Produktdimension „Farbe”. Dasselbe Modell wird auf die Größen, Stile und Konfigurationen angewendet.

![Datenmodell für Produktdimensionen.](media/dual-write-product-two.png)

Finanz- und Betriebs-Apps | Customer Engagement-Apps |
---|---
[Farben](mapping-reference.md#170) | msdyn\_productcolors
[Größen](mapping-reference.md#174) | msdyn\_productsizes
[Stile](mapping-reference.md#178) | msdyn\_productstyles
[Varianten](mapping-reference.md#171) | msdyn\_productconfigurations

Wenn ein Produkt unterschiedliche Produktdimensionen (z. B. ein Produktmaster hat Größe und Farbe als Produktdimensionen), jedes eindeutig identifizierbare Produkt (das heißt, jede Produktvariante) ist als Kombination dieser Produktdimensionen definiert. Beispielsweise ist eine Produktnummer B0001 ein extra kleines schwarzes T-Shirt und Produktnummer B0002 ein kleines schwarzes T-Shirt. In diesem Fall werden die vorhandenen Kombinationen von Produktdimensionen definiert. Beispielsweise kann das T-Shirt aus dem vorhergehenden Beispiel extra klein und schwarz, klein und schwarz, mittelgroß und schwarz oder groß und schwarz sein, aber es kann nicht extra groß und schwarz sein. Das bedeutet, die Produktdimensionen, die ein Produktmaster auswählen kann, sind festgelegt, und Varianten können anhand dieser Werte freigegeben werden.

Wenn Sie die Produktdimensionen nachverfolgen möchten, die ein Produktmaster wählen kann, werden die folgenden Tabellen in Dataverse für jede Produktdimension erstellt und zugeordnet. Weitere Informationen finden Sie unter [Überblick über die Produktinformationen](../../../../supply-chain/pim/product-information.md).

Finanz- und Betriebs-Apps | Customer Engagement-Apps |
---|---
[Produktmasterfarben](mapping-reference.md#187) | msdyn_sharedproductcolors |
[Produktmasterkonfigurationen](mapping-reference.md#188) | msdyn_sharedproductconfigurations |
[Produktmastergrößen](mapping-reference.md#190) | msdyn_sharedproductsizes |
[Produktmasterstile](mapping-reference.md#191) | msdyn_sharedproductstyles |
[Durch Produktnummer identifizierter Strichcode](mapping-reference.md#164) | msdyn\_productbarcodes |

## <a name="default-order-settings-and-product-specific-default-order-settings"></a>Standardauftragseinstellungen und produktspezifische Standardauftragseinstellungen

Standardauftragseinstellungen definieren den Standort und Lagerort, aus dem Artikel bezogen oder in dem sie gelagert werden, die Mindest-, Höchst-, Mehrfach- und Standardmengen, die für den Handel oder die Lagerverwaltung verwendet werden, die Lieferzeiten, das Beendigungskennzeichen sowie die Auftragszusagemethode. Diese Informationen sind in Dataverse über die Standardauftragseinstellungen und die Entität für produktspezifische Standardauftragseinstellungen verfügbar. Weitere Informationen zu den Funktionen finden Sie im [Artikel zu Standardauftragseinstellungen](../../../../supply-chain/production-control/default-order-settings.md).

Finanz- und Betriebs-Apps | Customer Engagement-Apps |
---|---
[Standardauftragseinstellungen](mapping-reference.md#172) | msdyn_productdefaultordersettings |
[Standardmäßige Produktauftragseinstellungen V2](mapping-reference.md#175) | msdyn_productspecificdefaultordersettings |

## <a name="unit-of-measure-and-unit-of-measure-conversions"></a>Maßeinheit und Maßeinheitsumrechnungen

Die Maßeinheiten und die jeweilige Umrechung sind in Dataverse entsprechend dem im Diagramm angezeigten Datenmodell verfügbar.

![Datenmodell für Maßeinheit.](media/dual-write-product-three.png)

Das Konzept der Maßeinheiten ist zwischen Finanz- und Betriebs-Apps und anderen Dynamics 365 Apps integriert. Für jede Einheitenklasse in einer Finanz- und Betriebs-App wird eine Einheitengruppe in einer Dynamics 365 App erstellt, die die zur Einheitenklasse gehörenden Einheiten enthält. Eine Standardbasiseinheit wird auch für jede Einheitsgruppe erstellt.

Finanz- und Betriebs-Apps | Customer Engagement-Apps |
---|---
[Produktspezifische Einheitenumrechnungen](mapping-reference.md#176) | msdyn_productspecificunitofmeasureconversions |
[Einheiten](mapping-reference.md#219) | uoms
[Einheitenumrechnungen](mapping-reference.md#199) | msdyn_ unitofmeasureconversions

## <a name="initial-synchronization-of-units-data-matching-between-finance-and-operations-and-dataverse"></a>Erstsynchronisation der Einheiten und Datenabgleich zwischen Finanzen und Betrieb und Dataverse.

### <a name="initial-synchronization-of-units"></a>Erstsynchronisierung von Einheiten

Wenn Dual-write aktiviert ist, werden Einheiten aus Finanz- und Betriebs-Apps mit anderen Dynamics 365 Apps synchronisiert. Die von Finanz- und Betriebs-Apps in Dataverse synchronisierten Einheitengruppen haben ein Flag festgelegt, das anzeigt, dass sie „extern gepflegt“ sind.

### <a name="matching-units-and-unit-classesgroups-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>Abgleich von Daten zu Einheiten und Einheitsklassen/-gruppen aus Finanzen und Betrieb und anderen Dynamics 365 Apps

Zunächst ist es wichtig zu beachten, dass der Integrationsschlüssel für die Einheit msdyn_symbol ist. Daher muss dieser Wert in Dataverse- oder anderen Dynamics 365-Apps eindeutig sein. Da in anderen Dynamics 365 Apps das Paar „Gruppen-ID der Einheit“ und „Name“ die Einzigartigkeit einer Einheit definiert, müssen Sie verschiedene Szenarien für den Abgleich von Einheitsdaten zwischen Finanz- und Betriebs-Apps und Dataverse in Betracht ziehen.

Für Einheiten, die in Finanz- und Betriebs-Apps und anderen Dynamics 365 Apps übereinstimmen/überlappen:

+ **Die Einheit gehört zu einer Einheitengruppe in anderen Dynamics 365 Apps, die der zugehörigen Einheitenklasse in den Finanz- und Betriebs-Apps entspricht**. In diesem Fall muss die Spalte msdyn_symbol in anderen Dynamics 365 Apps mit dem Symbol der Einheit aus den Finanz- und Betriebs-Apps ausgefüllt werden. Daher wird in anderen Dynamics 365-Apps der Zeitpunkt für den Abgleich der Daten und die Einheitengruppe als „Extern gepflegt“ festgelegt.
+ **Die Einheit gehört zu einer Einheitengruppe in anderen Dynamics 365 Apps, die nicht mit der zugehörigen Einheitenklasse in Finanz- und Betriebs-Apps übereinstimmt (keine vorhandene Einheitenklasse in Finanz- und Betriebs-Apps für die Einheitenklasse in anderen Dynamics 365 Apps).** In diesem Fall muss das msdyn_symbol mit einer zufälligen Zeichenfolge ausgefüllt werden. Beachten Sie, dass dieser Wert in anderen Dynamics 365-Apps eindeutig sein muss.

Für Einheiten und Einheitsklassen in Finanzen und Betrieb, die nicht in anderen Dynamics 365 Apps vorhanden sind:

Im Rahmen von Dual-write werden die Einheitengruppen aus den Finanz- und Betriebs-Apps und die entsprechenden Einheiten in anderen Dynamics 365 Apps erstellt und synchronisiert und Dataverse und die Einheitengruppe wird als „Extern gepflegt“ festgelegt. Es ist kein zusätzlicher Bootstrapping-Aufwand erforderlich.

Für Einheiten in anderen Dynamics 365 Apps, die in den Finanz- und Betriebs-Apps nicht vorhanden sind:

Die Spalte „msdyn_symbol“ muss für alle Einheiten ausgefüllt werden. Die Einheiten können in Finanz- und Betriebs-Apps immer in der entsprechenden Einheitenklasse erstellt werden (falls vorhanden). Wenn die Einheitsklasse nicht existiert, muss sie zunächst erstellt werden (beachten Sie, dass Sie in Finanz- und Betriebs-Apps keine Einheitsklasse erstellen können, außer durch eine Erweiterung, wenn Sie die Aufzählung erweitern), die mit der Einheitengruppe der anderen Dynamics 365 Apps übereinstimmt. Dann können Sie die Einheit erstellen. Beachten Sie, dass das Einheitensymbol in Finanz- und Betriebs-Apps das msdyn_symbol sein muss, das zuvor in anderen Dynamics 365 Apps für die Einheit angegeben wurde.

## <a name="product-policies-dimension-tracking-and-storage-groups"></a>Produktrichtlinien: Dimension, Nachverfolgung und Lagergruppen

Bei den Produktrichtlinien handelt es sich um Gruppen von Richtlinien, die für die Definition von Produkten und deren Merkmalen im Bestand verwendet werden. Die Produktdimensionsgruppe, die Produktnachverfolgungsdimensionsgruppe und die Lagerdimensionsgruppe können als Produktrichtlinien gefunden werden.

Finanz- und Betriebs-Apps | Customer Engagement-Apps |
---|---
[Produktdimensionsgruppen](mapping-reference.md#173) | msdyn\_productdimensiongroups |
[Lagerdimensionsgruppen](mapping-reference.md#177) | msdyn_productstoragedimensiongroups |
[Rückverfolgungsangabengruppen](mapping-reference.md#179) | msdyn_producttrackingdimensiongroups |

## <a name="product-hierarchies"></a>Produkthierarchien

Finanz- und Betriebs-Apps | Customer Engagement-Apps |
---|---
[Produktkategoriezuweisungen](mapping-reference.md#167) | msdyn_productcategoryassignments |
[Produktkategoriehierarchien](mapping-reference.md#168) | msdyn_productcategoryhierarchies |
[Produktkategoriehierarchie-Rollen](mapping-reference.md#169) | msdyn_productcategoryhierarchyrole |

## <a name="integration-key-for-products"></a>Integrationsschlüssel für Produkte

Um Produkte zwischen Dynamics 365 Finance und Produkten in Dataverse eindeutig zu identifizieren, werden die Integrationsschlüssel verwendet.
Für Produkte ist **(productnumber)** der eindeutige Schlüssel, der ein Produkt in Dataverse identifiziert. Sie wird durch die Verkettung von zusammengesetzt: **(Firma, msdyn_productnumber)**. Die **Firma** gibt die juristische Entität in Finanzen und Betrieb an und **msdyn_productnumber** gibt die Produktnummer für das spezifische Produkt in Finanzen und Betrieb an.

Für Benutzer anderer Dynamics 365-Apps wird das Produkt in der Benutzeroberfläche mit **msdyn_productnumber** gekennzeichnet (beachten Sie, dass die Spaltenbeschriftung **Produktnummer** lautet). Im Produktformular werden das Unternehmen und das Feld „msydn_productnumber“ angezeigt. Die Spalte (productnumber), bei der es sich um den eindeutigen Schlüssel für ein Produkt handelt, wird jedoch nicht angezeigt.

Wenn Sie Apps auf Dataverse aufbauen, sollten Sie darauf achten, dass Sie den Integrationsschlüssel **Produktnummer** (die eindeutige Produkt-ID) verwenden. Verwenden Sie nicht **msdyn_productnumber**, da sie nicht eindeutig ist.

## <a name="initial-synchronization-of-products-and-migration-of-data-from-dataverse-to-finance-and-operations"></a>Initiale Synchronisierung von Produkten und Migration der Daten von Dataverse zu Finanzen und Betrieb

### <a name="initial-synchronization-of-products"></a>Erstsynchronisierung von Produkten

Wenn Dual-write aktiviert ist, werden Produkte aus Finanz- und Betriebs-Apps mit Dataverse und Customer-Engagement-Apps synchronisiert. Produkte, die in Dataverse und anderen Dynamics 365 Apps erstellt wurden, bevor Dual-write freigegeben wurde, werden nicht aktualisiert oder mit Produktdaten aus Finanz- und Betriebs-Apps abgeglichen.

### <a name="matching-product-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>Abgleich von Produktdaten aus Finanzen und Betrieb und anderen Dynamics 365 Apps

Wenn in Finanzen und Betrieb und in Dataverse und anderen Dynamics 365 Apps die gleichen Produkte geführt werden (Überschneidungen/Übereinstimmungen), findet bei Aktivierung von Dual-write die Synchronisierung der Produkte aus Finanzen und Betrieb statt und in Dataverse erscheinen doppelte Zeilen für dasselbe Produkt.
Wenn andere Dynamics 365 Apps Produkte haben, die sich mit Finanzen und Betrieb überschneiden, muss der Administrator, der Dual-write aktiviert, die Spalten **Firma** (Beispiel: „USMF“) und **msdyn_productnumber** (Beispiel: „1234:Black:S“) booten, bevor die Synchronisierung der Produkte stattfindet. Mit anderen Worten, diese beiden Spalten im Produkt in Dataverse müssen mit der jeweiligen Firma in Finanzen und Betrieb, der das Produkt zugeordnet werden muss, und mit seiner Produktnummer ausgefüllt werden.

Wenn dann die Synchronisierung aktiviert ist und stattfindet, werden die Produkte aus Finanzen und Betrieb mit den entsprechenden Produkten in Dataverse und anderen Dynamics 365 Apps synchronisiert. Dies gilt für eindeutig identifizierbare Produkte und für Produktvarianten.

### <a name="migration-of-product-data-from-other-dynamics-365-apps-to-finance-and-operations"></a>Migration von Produktdaten aus anderen Dynamics 365 Apps zu Finanzen und Betrieb

Wenn andere Apps in Dynamics 365 Produkte haben, die in Finanzen und Betrieb nicht vorhanden sind, kann der Administrator zunächst die **EcoResReleasedProductCreationV2Entity** verwenden, um diese Produkte in Finanzen und Betrieb zu importieren. Und zweitens gleichen Sie die Produktdaten aus Finanzen und Betrieb und anderen Dynamics 365 Apps wie oben beschrieben ab.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

