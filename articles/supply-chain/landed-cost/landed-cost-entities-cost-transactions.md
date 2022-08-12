---
title: Entitäten für Kostentransaktionen
description: Dieser Artikel enthält Informationen zu Kostenbuchungsentitäten, die es ermöglichen, den Wert von Kosten durch die Auswahl einer Aufteilungsmethode auf die Inhalte eines Kostenbereichs aufzuteilen.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 0084d47bf85050749b2668d273db07670aaeae2a
ms.sourcegitcommit: 5b34b41ae74269ba639e2876bc5862ef468da1cc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2022
ms.locfileid: "9166802"
---
# <a name="cost-transaction-entities"></a>Kostenbuchungsentitäten

[!include [banner](../includes/banner.md)]

## <a name="apportionment"></a>Umlage

Gesamttransportkosten ermöglichen die Aufteilung des Kostenwerts auf die Inhalte eines Kostenbereichs (Reise, Schiffscontainer usw.) durch die Auswahl einer Aufteilungsmethode. Die Aufteilungsmethode wird im Rahmen der Konfiguration automatischer Kosten festgelegt, die auf Geschäftsregeln basiert. Sie wird als Teil der Kosten durchgezogen, wenn eine Seereiseposition erstellt wird.

### <a name="configure-the-apportionment-mapping-for-use-with-data-entities"></a>Konfigurieren der Aufteilungszuordnung für die Verwendung mit Datenentitäten

Wenn Kosten von einer externen Quelle wie einem Spediteur erstellt werden, kann diese externe Quelle die bevorzugte Methode für die Aufteilung des Kostenwerts nicht angeben. Die Umlagezuordnung definiert die Standardaufteilungsmethode für jeden Kostenartencode. Auf die Umlagezuordnungstabelle wird von der **Aufteilungskartierung**-Seite in Microsoft Dynamics 365 Supply Chain Management (**Gesamttransportkosten \> Einstellungen für Nachkalkulation \> Umlagezuordnung**) aus zugegriffen.

Wenn eine Zuordnungskombination definiert wurde und Kosten, die dem Kostenartencode entsprechen, mithilfe einer Kostenbuchungsentität erstellt werden, wird die zugeordnete Umlagemethode anstelle eines Werts verwendet, der der Entität bereitgestellt wurde.

Wenn in der Zuordnungstabelle kein Wert vorhanden ist, der Entität jedoch ein Wert bereitgestellt wurde, wird der bereitgestellte Wert verwendet.

Wenn weder in der Zuordnungstabelle noch im Datensatz, der an die Entität übermittelt wurde, ein Wert vorhanden ist, schlägt die Erstellung fehl.

### <a name="apportionment-mapping-itmapportionmentmapping"></a>Umlagezuordnung (ITMApportionmentMapping)

Die Entität der Umlagezuordnung (`ITMApportionmentMapping`) erstellt Umlagezuordnungsbeziehungen und ermöglicht Benutzern das Erstellen oder Aktualisieren von Datensätzen.

| Name | Zuordnung | Datentyp | Schlüssel | Obligatorisch |
|---|---|---|---|---|
| Umlagemethode | ITMApportionmentMapping.ApportionmentMethod | Int | Nein | Nein |
| Kostentypcode | ITMApportionmentMapping.ShipCostTypeId | Nvarchar(20) | **Ja** | Nein |

## <a name="voyage-costs-itmcosttransvoyageentity"></a>Seereisekosten (ITMCostTransVoyageEntity)

Die Seereisekostenentität (`ITMCostTransVoyageEntity`) erstellt Seereisekostenbuchungen, die auf Seereiseebene angewendet werden. Während des Importvorgangs verwendet das System die Werte **Kategorie** und **Umlagemethode**, die in der Entität enthalten sind, um zu bestimmen, wie der Wert der Kosten auf den Inhalt der Seereise verteilt wird.

| Name | Zuordnung | Datentyp | Schlüssel | Obligatorisch |
|---|---|---|---|---|
| Umlagemethode | ITMCostTrans.ApportionmentMethod | Int | Nein | Nein |
| Einstandswert | ITMCostTrans.CostValue | Numeric(32, 6) | Nein | Nein |
| Währung | ITMCostTrans.CurrencyCode | Nvarchar(3) | Nein | **Ja** |
| Positionsnummer | ITMCostTrans.LineNum | Numeric(32, 16) | **Ja** | Nein |
| Verknüpfter Kostentyp | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | Nein | Nein |
| Mindestkosten | ITMCostTrans.MinCostAmount | Numeric(32, 6) | Nein | Nein |
| Kategorie | ITMCostTrans.ShipCostCategory | Int | Nein | Nein |
| Kostentypcode | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | Nein | Nein |
| Unternehmen | ITMCostTrans.ShipDataArea | Nvarchar(4) | Nein | **Ja** |
| Seereise | ITMCostTrans.TransRecId | Nvarchar(20) | **Ja** | Nein |
| Artikel-Mehrwertsteuergruppe | ITMCostTrans.TaxItemGroup | Nvarchar(10) | Nein | Nein |

## <a name="shipping-container-costs-itmcosttransshippingcontainerentity"></a>Kosten für Versandbehälter (ITMCostTransShippingContainerEntity)

Die Kosteneinheit des Versandbehälters (`ITMCostTransShippingContainerEntity`) erstellt Versandbehälterkosten, die auf Versandbehälterebene angewendet werden. Während des Importvorgangs verwendet das System die Werte **Kategorie** und **Umlagemethode**, die in der Entität enthalten sind, um zu bestimmen, wie der Wert der Kosten auf den Inhalt des Versandbehälters verteilt wird.

Die Felder **Aggregat**, **Teilstrecke** und **Verknüpfte Teilstrecke** sind spezifisch für Datensätze, in denen der **Kostenbereich**-Wert *Versandbehälter* ist. Daher sind sie in Datenentitäten für andere Kostenbereiche nicht vorhanden.

| Name | Zuordnung | Datentyp | Schlüssel | Obligatorisch |
|---|---|---|---|---|
| Zusammenführen | ITMCostTrans.AggregatedCost | Int | Nein | Nein |
| Umlagemethode | ITMCostTrans.ApportionmentMethod | Int | Nein | Nein |
| Einstandswert | ITMCostTrans.CostValue | Numeric(32, 6) | Nein | Nein |
| Währung | ITMCostTrans.CurrencyCode | Nvarchar(3) | Nein | **Ja** |
| Positionsnummer | ITMCostTrans.LineNum | Numeric(32, 16) | **Ja** | Nein |
| Verknüpfter Kostentyp | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | Nein | Nein |
| Verknüpfte Teilstrecke | ITMCostTrans.LinkLegId | Nvarchar(20) | Nein | Nein |
| Mindestkosten | ITMCostTrans.MinCostAmount | Numeric(32, 6) | Nein | Nein |
| Versandcontainer | ITMCostTrans.TransRecId | Nvarchar(20) | **Ja** | Nein |
| Kategorie | ITMCostTrans.ShipCostCategory | Int | Nein | Nein |
| Kostentypcode | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | Nein | Nein |
| Unternehmen | ITMCostTrans.ShipDataArea | Nvarchar(4) | Nein | **Ja** |
| Seereise | ITMCostTrans.TransRecId | Nvarchar(20) | **Ja** | Nein |
| Teilstrecke | ITMCostTrans.ShipLegId | Nvarchar(20) | Nein | Nein |
| Artikel-Mehrwertsteuergruppe | ITMCostTrans.TaxItemGroup | Nvarchar(10) | Nein | Nein |

## <a name="folio-costs-itmcosttransfolioentity"></a>Palette-Kosten (ITMCostTransFolioEntity)

Die Palette-Kosteneinheit (`ITMCostTransFolioEntity`) erstellt Kostentransaktionsdatensätze, die für die Palette-Ebene gelten. Während des Importvorgangs verwendet das System die Werte **Kategorie** und **Umlagemethode**, die in der Entität enthalten sind, um zu bestimmen, wie der Wert der Kosten auf den Inhalt jeder Palette verteilt wird.

| Name | Zuordnung | Datentyp | Schlüssel | Obligatorisch |
|---|---|---|---|---|
| Umlagemethode | ITMCostTrans.ApportionmentMethod | Int | Nein | Nein |
| Einstandswert | ITMCostTrans.CostValue | Numeric(32, 6) | Nein | Nein |
| Währung | ITMCostTrans.CurrencyCode | Nvarchar(3) | Nein | **Ja** |
| Positionsnummer | ITMCostTrans.LineNum | Numeric(32, 16) | **Ja** | Nein |
| Verknüpfter Kostentyp | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | Nein | Nein |
| Mindestkosten | ITMCostTrans.MinCostAmount | Numeric(32, 6) | Nein | Nein |
| Kategorie | ITMCostTrans.ShipCostCategory | Int | Nein | Nein |
| Kostentypcode | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | Nein | Nein |
| Unternehmen | ITMCostTrans.ShipDataArea | Nvarchar(4) | Nein | **Ja** |
| Folio | ITMCostTrans.TransRecId | Nvarchar(20) | **Ja** | Nein |
| Artikel-Mehrwertsteuergruppe | ITMCostTrans.TaxItemGroup | Nvarchar(10) | Nein | Nein |

## <a name="purchase-order-costs-itmcosttranspurchaseentity"></a>Bestellkosten (ITMCostTransPurchaseEntity)

Die Bestellkostenentität (`ITMCostTransPurchaseEntity`) erstellt Kostenbuchungen, die für die Bestellkopfzeile gelten. Während des Importvorgangs verwendet das System die Werte **Kategorie** und **Umlagemethode**, die in der Entität enthalten sind, um zu bestimmen, wie der Wert der Kosten auf den Inhalt jeder Palette verteilt wird.

| Name | Zuordnung | Datentyp | Schlüssel | Obligatorisch |
|---|---|---|---|---|
| Umlagemethode | ITMCostTrans.ApportionmentMethod | Int | Nein | Nein |
| Einstandswert | ITMCostTrans.CostValue | Numeric(32, 6) | Nein | Nein |
| Währung | ITMCostTrans.CurrencyCode | Nvarchar(3) | Nein | **Ja** |
| Positionsnummer | ITMCostTrans.LineNum | Numeric(32, 16) | **Ja** | Nein |
| Verknüpfter Kostentyp | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | Nein | Nein |
| Mindestkosten | ITMCostTrans.MinCostAmount | Numeric(32, 6) | Nein | Nein |
| Bestellung | ITMCostTrans.TransRecId | Nvarchar(20) | **Ja** | Nein |
| Kategorie | ITMCostTrans.ShipCostCategory | Int | Nein | Nein |
| Kostentypcode | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | Nein | Nein |
| Unternehmen | ITMCostTrans.ShipDataArea | Nvarchar(4) | Nein | **Ja** |
| Artikel-Mehrwertsteuergruppe | ITMCostTrans.TaxItemGroup | Nvarchar(10) | Nein | Nein |

## <a name="item-costs-itmcosttransitementity"></a>Artikelkosten (ITMCostTransItemEntity)

Die Artikelkosteneinheit (`ITMCostTransItemEntity`) erstellt Kostenbuchungen, die für die Artikelebene gelten. Diese Entität ist spezifisch für Artikel in Bestellpositionen. Der Wert der Kosten wird vollständig auf die Position angewendet.

Die Felder **Regulierungsbetrag** und **Wertregulierung** sind spezifisch für die Kostenbereiche auf Positionsebene. Daher sind sie in Datenentitäten für andere Kostenbereiche nicht vorhanden.

| Name | Zuordnung | Datentyp | Schlüssel | Obligatorisch |
|---|---|---|---|---|
| Regulierungsbetrag | ITMCostTrans.AdjustmentAmount | Numeric(32, 6) | Nein | Nein |
| Einstandswert | ITMCostTrans.CostValue | Numeric(32, 6) | Nein | Nein |
| Währung | ITMCostTrans.CurrencyCode | Nvarchar(3) | Nein | **Ja** |
| Positionsnummer | ITMCostTrans.LineNum | Numeric(32, 16) | **Ja** | Nein |
| Verknüpfter Kostentyp | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | Nein | Nein |
| Mindestkosten | ITMCostTrans.MinCostAmount | Numeric(32, 6) | Nein | Nein |
| Bestellung | ITMCostTrans.TransRecId | Nvarchar(20) | **Ja** | Nein |
| Nummer der Bestellposition | ITMCostTrans.TransRecId | Nvarchar(20) | **Ja** | Nein |
| Kategorie | ITMCostTrans.ShipCostCategory | Int | Nein | Nein |
| Kostentypcode | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | Nein | Nein |
| Unternehmen | ITMCostTrans.ShipDataArea | Nvarchar(4) | Nein | **Ja** |
| Artikel-Mehrwertsteuergruppe | ITMCostTrans.TaxItemGroup | Nvarchar(10) | Nein | Nein |
| Wertregulierung | ITMCostTrans.ValueAdjustmentMethod | Int | Nein | Nein |

## <a name="transfer-line-costs-itmcosttranstransferlineentity"></a>Umlagerungspositionskosten (ITMCostTransTransferLineEntity)

Die Kostenentität der Umlagerungsposition (`ITMCostTransTransferLineEntity`) erstellt Kostenbuchungen, die für die Ebene der Umlagerungsauftragsposition gelten. Der Wert dieser Kosten wird vollständig auf die Umlagerungsauftragsposition angewendet.

Die Felder **Regulierungsbetrag** und **Wertregulierung** sind spezifisch für die Kostenbereiche auf Positionsebene. Daher sind sie in Datenentitäten für andere Kostenbereiche nicht vorhanden.

| Name | Zuordnung | Datentyp | Schlüssel | Obligatorisch |
|---|---|---|---|---|
| Regulierungsbetrag | ITMCostTrans.AdjustmentAmount | Numeric(32, 6) | Nein | Nein |
| Einstandswert | ITMCostTrans.CostValue | Numeric(32, 6) | Nein | Nein |
| Währung | ITMCostTrans.CurrencyCode | Nvarchar(3) | Nein | **Ja** |
| Positionsnummer | ITMCostTrans.LineNum | Numeric(32, 16) | **Ja** | Nein |
| Verknüpfter Kostentyp | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | Nein | Nein |
| Mindestkosten | ITMCostTrans.MinCostAmount | Numeric(32, 6) | Nein | Nein |
| Kategorie | ITMCostTrans.ShipCostCategory | Int | Nein | Nein |
| Kostentypcode | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | Nein | Nein |
| Unternehmen | ITMCostTrans.ShipDataArea | Nvarchar(4) | Nein | **Ja** |
| Umlagerungsauftrag | ITMCostTrans.TransRecId | Nvarchar(20) | **Ja** | Nein |
| Nummer der Umlagerungsauftragsposition | ITMCostTrans.TransRecId | Nvarchar(20) | **Ja** | Nein |
| Artikel-Mehrwertsteuergruppe | ITMCostTrans.TaxItemGroup | Nvarchar(10) | Nein | Nein |
| Wertregulierung | ITMCostTrans.ValueAdjustmentMethod | Int | Nein | Nein |

### <a name="transaction-table"></a>Buchungstabelle

Ein Kostenbuchungsdatensatz wird einem Kostenbereich durch die Zuweisung einer Buchungstabellennummer (`TransTableId`) zugewiesen. Wenn bestimmte Tabellenidentifikationsnummern erforderlich sind, werden die Entitäten basierend auf diesen Werten aufgeteilt, sodass für jeden Kostenbereich eine Entität vorhanden ist.

Der Wert für die Buchungstabelle (`TransTableId`) ist in der Auswahl der Kostenbuchungseinheit implizit enthalten.

### <a name="calculated-fields"></a>Berechnete Felder

Die folgenden Felder stehen nicht zum Einfügen oder Aktualisieren zur Verfügung, wenn eine Kostenbuchungseinheit verwendet wird, da diese Felder nur festgelegt werden, wenn bestimmte Aktionen für den Seereisedatensatz durchgeführt werden:

- **Vorkalkulierte Kosten** – dieses Feld wird gesetzt, wenn eine Rechnung für die Seereise (Bestellung) gebucht oder eine Umlagerung empfangen wird.
- **Währung der vorkalkulierten Kosten** – dieses Feld wird gesetzt, wenn eine Rechnung für die Seereise (Bestellung) gebucht oder eine Umlagerung empfangen wird.
- **Istkosten** – dieses Feld wird gesetzt, wenn eine Kreditorenrechnung gebucht wird. Es ist den Kosten zugeordnet.

### <a name="find-auto-costs"></a>Automatische Kosten suchen

Eine **Automatische Kosten suchen**-Schaltfläche, die für jeden Kostenbereich (Seereise, Schiffscontainer usw.) verfügbar ist, bietet eine Möglichkeit, die Kostenbuchungen für diesen Kostenbereich anhand der Informationen in den Konfigurationstabellen zu aktualisieren. Wenn Sie die Schaltfläche für einen Kostenbereich auswählen, löscht das System vorhandene Kosten für diesen Kostenbereich und erstellt neue Datensätze, basierend auf der aktuellen Konfiguration der Tabellen für die automatische Kosteneinrichtung.

Kostenbuchungsdatensätze, die mithilfe einer Datenentität erstellt wurden, werden als importiert gekennzeichnet. Diese Datensätze werden nicht gelöscht, wenn Sie **Automatische Kosten suchen** auswählen, da sie nicht aus den Tabellen für die Einrichtung der automatischen Kosten neu erstellt werden. Ein als importiert gekennzeichneter Kostenbuchungssatz kann jedoch weiterhin gelöscht werden.

### <a name="linked-fields"></a>Verknüpfte Felder

Jede Kostenbuchung kann einem anderen Datensatz im selben Kostenbereich zugeordnet werden. Diese Zuordnung wird über das Feld **Verknüpfter Kostentyp** erreicht. Es ermöglicht die Berechnung eines Kostenwerts als Prozentsatz anderer Kosten.

Das Feld **Verknüpfter Kostentyp** kann nur validiert werden, wenn der Datensatz, auf den verwiesen wird, zuerst verarbeitet wird, oder wenn er bereits in der Tabelle vorhanden ist. Die gleiche Anforderung gilt für das **Verknüpfte Teilstrecke**-Feld, das nur für Kosten im Kostenbereich für Versandbehälter verwendet wird.
