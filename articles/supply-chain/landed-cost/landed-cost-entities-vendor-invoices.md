---
title: Kreditorenrechnungsentitäten
description: Dieses Thema enthält Informationen über Entitäten von Kreditor-Rechnungen, die es ermöglichen, Kostenartencodes für interne Kosten oder extern abgeleitete Kosten zu konfigurieren.
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
ms.openlocfilehash: 4bbe0fdbf95050ebfa707224f602e5e71ddb3a8f
ms.sourcegitcommit: 611202adaa080250636efabb3b3b32b850d92d04
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/28/2022
ms.locfileid: "8813078"
---
# <a name="vendor-invoice-entities"></a>Entitäten für Kreditorenrechnungen

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until GA with 10.0.28 -->

Mit dem Modul **Gesamttransportkosten** können Sie Kostenartencodes für interne Kosten oder extern abgeleitete Kosten konfigurieren. Wenn es sich um externe Kosten handelt, wird eine Rechnung vom Serviceanbieter erwartet. Diese Rechnung wird als Rechnungsjournal verarbeitet, das mit einer Fahrt verknüpft werden kann, und der Wert der Rechnung kann auf eine oder mehrere Nachkalkulationen der Fahrt verteilt werden.

Die Entitäten der Kreditor-Rechnung ermöglichen die Umlage des Wertes einer Buchungsblattzeile auf eine oder mehrere Kosten einer Fahrt, die denselben Kostenartencode haben.

Eine Nachkalkulation ist nur möglich, wenn der Rechnungsjournal-Kopf und die Buchungsblattzeilen vorhanden sind.

## <a name="vendor-voyage-cost-allocations-itmledgerjournalcostlinesvoyagesentity"></a>Nachkalkulationen von Kreditor Fahrten (ITMLedgerJournalCostLinesVoyagesEntity)

Die Entität für die Nachkalkulation einer Fahrt ermöglicht es, eine Rechnungszeile des Kreditors einer oder mehreren Kosten zuzuordnen, die auf den Kostenbereich der Fahrt entfallen. Diese Funktionalität wird von der Entität `ITMLedgerJournalCostLinesVoyagesEntity` unterstützt. In der folgenden Tabelle sind die Felder und Zuordnungen aufgeführt, aus denen diese Entität besteht.

| Name | Zuordnung | Datentyp | Schlüssel | Obligatorisch |
|---|---|---|---|---|
| Zugeteilter Betrag | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | Nein | Nein |
| Nummer der Kostentransaktionsposition | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **Ja** | Nein |
| Erfassungspositionsnummer | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **Ja** | Nein |
| Erfassungsnummer | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Ja** | Nein |
| Seereise | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Ja** | Nein |

## <a name="vendor-shipping-container-cost-allocations-itmledgerjournalcostlinescontainersentity"></a>Kreditor Transportcontainer Nachkalkulationen (ITMLedgerJournalCostLinesContainersEntity)

Die Entität Transportcontainer-Kostenzuordnung ermöglicht die Zuordnung einer Lieferantenrechnungszeile zu einer oder mehreren Kosten, die auf den Kostenbereich des Transportcontainers entfallen. Diese Funktionalität wird von der Entität `ITMLedgerJournalCostLinesContainersEntity` unterstützt. In der folgenden Tabelle sind die Felder und Zuordnungen aufgeführt, aus denen diese Entität besteht.

| Name | Zuordnung | Datentyp | Schlüssel | Obligatorisch |
|---|---|---|---|---|
| Zugeteilter Betrag | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | Nein | Nein |
| Versandcontainer | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Ja** | Nein |
| Nummer der Kostentransaktionsposition | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **Ja** | Nein |
| Erfassungspositionsnummer | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **Ja** | Nein |
| Erfassungsnummer | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Ja** | Nein |
| Seereise | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Ja** | Nein |

## <a name="vendor-folio-cost-allocations-itmledgerjournalcostlinesfoliosentity"></a>Nachkalkulationen für Kreditor Paletten (ITMLedgerJournalCostLinesFoliosEntity)

Die Entitäten für die Nachkalkulation von Kreditor-Folio-Kosten ermöglichen die Zuordnung einer Kreditor-Rechnungszeile zu einer oder mehreren Kosten, die auf den Folio-Kostenbereich angewendet werden. Diese Funktionalität wird von der Entität `ITMLedgerJournalCostLinesFoliosEntity` unterstützt. In der folgenden Tabelle sind die Felder und Zuordnungen aufgeführt, aus denen diese Entität besteht.

| Name | Zuordnung | Datentyp | Schlüssel | Obligatorisch |
|---|---|---|---|---|
| Zugeteilter Betrag | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | Nein | Nein |
| Nummer der Kostentransaktionsposition | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **Ja** | Nein |
| Folio | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Ja** | Nein |
| Erfassungspositionsnummer | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **Ja** | Nein |
| Erfassungsnummer | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Ja** | Nein |

## <a name="vendor-purchase-order-cost-allocations-itmledgerjournalcostlinespurchtableentity"></a>Kreditor-Bestellkosten-Zuordnungen (ITMLedgerJournalCostLinesPurchTableEntity)

Die Entität Einkaufsrechnungen des Kreditors ermöglicht die Zuordnung einer oder mehrerer Kosten, die auf den Kostenbereich der Bestellung angewendet werden, zu einer Einkaufsrechnung. Diese Funktionalität wird von der Entität `ITMLedgerJournalCostLinesPurchTableEntity` unterstützt. In der folgenden Tabelle sind die Felder und Zuordnungen aufgeführt, aus denen diese Entität besteht.

| Name | Zuordnung | Datentyp | Schlüssel | Obligatorisch |
|---|---|---|---|---|
| Zugeteilter Betrag | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | Nein | Nein |
| Nummer der Kostentransaktionsposition | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **Ja** | Nein |
| Erfassungspositionsnummer | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **Ja** | Nein |
| Erfassungsnummer | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Ja** | Nein |
| Bestellung | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Ja** | Nein |

## <a name="vendor-item-cost-allocations-itmledgerjournalcostlinespurchlineentity"></a>Nachkalkulationen für Artikel des Lieferanten (ITMLedgerJournalCostLinesPurchLineEntity)

Die Entitäten der Kreditor Artikel-Kostenzuordnung ermöglichen die Zuordnung einer Kreditor Rechnungszeile zu einer oder mehreren Kosten, die auf den Artikel-Kostenbereich angewandt werden. Der Bereich Artikelkosten umfasst die Nachkalkulationen für die Zeile der Bestellung. Diese Funktionalität wird von der Entität `ITMLedgerJournalCostLinesPurchLineEntity` unterstützt. In der folgenden Tabelle sind die Felder und Zuordnungen aufgeführt, aus denen diese Entität besteht.

| Name | Zuordnung | Datentyp | Schlüssel | Obligatorisch |
|---|---|---|---|---|
| Zugeteilter Betrag | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | Nein | Nein |
| Nummer der Kostentransaktionsposition | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **Ja** | Nein |
| Erfassungspositionsnummer | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **Ja** | Nein |
| Erfassungsnummer | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Ja** | Nein |
| Bestellung | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Ja** | Nein |
| Nummer der Bestellposition | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **Ja** | Nein |

## <a name="vendor-transfer-order-line-cost-allocations-itmledgerjournalcostlinestransferlineentity"></a>Kreditor Umlagerungsauftrag Zeilen-Kostenzuordnungen (ITMLedgerJournalCostLinesTransferLineEntity)

Die Entität Lieferantenumlagerungsauftrag Zeile Kostenzuordnungen ermöglicht die Zuordnung einer Lieferantenrechnungszeile zu einer oder mehreren Kosten, die auf den Kostenbereich der Umlagerungsaufträge entfallen. Diese Funktionalität wird von der Entität `ITMLedgerJournalCostLinesTransferLineEntity` unterstützt. In der folgenden Tabelle sind die Felder und Zuordnungen aufgeführt, aus denen diese Entität besteht.

| Name | Zuordnung | Datentyp | Schlüssel | Obligatorisch |
|---|---|---|---|---|
| Zugeteilter Betrag | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | Nein | Nein |
| Nummer der Kostentransaktionsposition | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **Ja** | Nein |
| Erfassungspositionsnummer | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **Ja** | Nein |
| Erfassungsnummer | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Ja** | Nein |
| Umlagerungsauftrag | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Ja** | Nein |
| Nummer der Umlagerungsauftragsposition | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **Ja** | Nein |

### <a name="reference-table"></a>Bezugstabelle

Reisekostenzeilen haben eine direkte Verbindung zu einem Datensatz der Nachkalkulation. Dieser Datensatz enthält den Wert **Referenztabelle ID**. Dieser Wert ist für jeden Kostenbereich (Fahrt, Transportcontainer usw.) eindeutig. Wenn für Daten, die mit Hilfe von Datenentitäten erstellt werden, auf bestimmte Tabellennummern verwiesen wird, werden die Entitäten anhand von **Referenztabellen-ID**-Werten aufgeteilt.

Die Werte für die Referenztabelle (`RefTableId`) und die Transaktionsart (`TransType`) sind implizit in der Auswahl der Entität Gesamttransportkosten kalkulierte Zeile oder Gesamttransportkosten kalkulierte Zeile enthalten.

## <a name="vendor-invoice-journal-lines-vendorinvoicejournallineentity"></a>Erfassungsblattzeilen für Lieferantenrechnungen (VendorInvoiceJournalLineEntity)

Bevor der Wert einer Buchungsblattzeile einer oder mehreren Kosten im Modul **Gesamttransportkosten** zugeordnet werden kann, muss die Buchungsblattzeile mit einem Kostenbereich verbunden sein. Um diese Funktionalität zu unterstützen, fügt das Modul **Gesamttransportkosten** einige neue Felder zur Tabelle der Buchungsblattzeilen hinzu (`LedgerJournalTrans`).

### <a name="fields-added-to-the-vendor-invoice-journal-line-entity"></a>Felder, die der Entität Buchungsblattzeile der Kreditor-Rechnung hinzugefügt wurden

In der folgenden Tabelle sind die Felder aufgeführt, die das Modul **Gesamttransportkosten** der Entität Buchungsblattzeile der Kreditor-Rechnung (`VendorInvoiceJournalLineEntity`) hinzufügt. Diese Felder ermöglichen es dem System, Buchungsblattzeilen zu erstellen und ihnen Kosten zuzuordnen.

| Name | Zuordnung | Datentyp | Schlüssel | Obligatorisch |
|---|---|---|---|---|
| Kostenbereich | LedgerJournalTrans.ITMCostArea | Int | Nein | Nein |
| Kostentypcode | LedgerJournalTrans.ITMCostTypeId | Nvarchar(20) | Nein | Nein |

### <a name="mainoffset-account"></a>Haupt-/Verrechnungskonto

Das Haupt-/Gegenkonto für eine Buchungsblattzeile, die mit einer kalkulierten Gesamttransportkosten-Fahrt verbunden ist, wird durch den Kostenartencode bestimmt. Wenn der Kostenartencode in der Buchungsblattzeile der Rechnung enthalten ist, wird das Verrechnungskonto für den Code je nach Szenario entweder als Hauptkonto oder als Gegenkonto verwendet:

- **Einzelzeiliges Buchungsblatt** - Wenn ein Hauptkonto (mit anderen Worten, das Kreditorenkonto) definiert ist und ein Kostenartencode angegeben wird, wird der Wert des Verrechnungskontos für diesen Kostenartencode im Gegenkonto eingetragen.
- **Mehrzeiliges Buchungsblatt** - Wenn ein Hauptkonto nicht definiert ist, aber ein Kostenartencode angegeben wird, wird der Wert des Verrechnungskontos für diesen Kostenartencode in das Hauptkonto eingetragen. Die Buchungsblattzeile, die den Kreditor entlastet, verweist nicht auf einen Kostenartencode.

## <a name="sequencing"></a>Abfolge

Aufgrund von Abhängigkeiten zwischen den Tabellen Journal und Buchungsblattzeilen muss der Datensatz für die Fahrt zuerst erstellt werden. Die Reisezeilen können erst erstellt werden, nachdem die Reise, der Transportcontainer und die Paletten erstellt worden sind.

Um eine Fahrt-Rechnung zuzuordnen, muss das System die Entitäten in der folgenden Reihenfolge verarbeiten:

1. Kopfzeile des Rechnungsjournals (`VendInvoiceJournalHeaderEntity`)
1. Buchungsblattzeile für Rechnungen (`VendInvoiceJournalLineEntity`)
1. Gesamttransportkosten Nachkalkulationen (`ITMLedgerJournalEntities`)
