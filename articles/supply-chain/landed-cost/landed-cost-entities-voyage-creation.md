---
title: Entitäten zur Reiseerstellung
description: In diesem Artikel finden Sie Informationen zu den Entitäten für die Erstellung von Fahrten, in denen die Entitäten zusammengefasst sind, die zum Erstellen einer Arbeitsfahrt erforderlich sind.
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
ms.openlocfilehash: 6234dfa61a5859e2ecaca75594c69c49ba326629
ms.sourcegitcommit: 5b34b41ae74269ba639e2876bc5862ef468da1cc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2022
ms.locfileid: "9167670"
---
# <a name="voyage-creation-entities"></a>Entitäten zur Erstellung von Fahrten

[!include [banner](../includes/banner.md)]

Die Entitäten zur Erstellung von Fahrten fassen die Entitäten zusammen, die zum Erstellen einer Arbeitsfahrt erforderlich sind. Sie oder Ihr Spediteur können diese Entitäten verwenden, um Datensätze für Fahrten, Transportcontainer, Paletten und Umlagerungsaufträge zu erstellen, die auf bestehende Bestellungen oder Umlagerungsaufträge verweisen.

## <a name="voyages-itmtableentity"></a>Fahrten (ITMTableEntity)

Die Reise stellt den Verlauf der eingehenden Waren dar und dient als oberster Kostenbereich der Gesamttransportkosten. Es enthält Informationen auf Kopfebene, die sich auf das Schiff, den Ursprungshafen und den Zielhafen beziehen. Diese Funktionalität wird von der Entität `ITMTableEntity` unterstützt. In der folgenden Tabelle sind die Felder und Zuordnungen aufgeführt, aus denen diese Entität besteht.

| Name | Zuordnung | Datentyp | Schlüssel | Obligatorisch |
|---|---|---|---|---|
| Lieferart | ITMTable.DlvModeId | Nvarchar(10) | Nein | Nein |
| Vom Broker empfohlen | ITMTable.ITMBrokerAdvised | Datetime | Nein | Nein |
| Debitorentermin | ITMTable.ITMCustomerAppointment | Datetime | Nein | Nein |
| Auslieferung am Lagerort | ITMTable.ITMDelAtWarehouse | Datetime | Nein | Nein |
| Lieferanweisungen | ITMTable.ITMDeliveryInstructions | Datetime | Nein | Nein |
| Abgangsdatum | ITMTable.ITMDepartureDate | Datetime | Nein | Nein |
| Warenfreigabe | ITMTable.ITMGoodsReleased | Datetime | Nein | Nein |
| Datum des lokalen Transports | ITMTable.ITMLocalTransportDate | Datetime | Nein | Nein |
| Uhrzeit des lokalen Transports | ITMTable.ITMLocalTransportTime | Int | Nein | Nein |
| Ursprünglicher Frachtbrief gesendet | ITMTable.ITMOriginalBOLSebt | Datetime | Nein | Nein |
| Ursprüngliche Belege empfangen | ITMTable.ITMOriginalDocsReceived | Datetime | Nein | Nein |
| Bestellungsstatus | ITMTable.ITMPurchStatus | Int | Nein | Nein |
| Überprüfungsdatum | ITMTable.ITMVerificationDate | Datetime | Nein | Nein |
| Zolleintrags-ID | ITMTable.ShipCustomsEntryId | Nvarchar(20) | Nein | Nein |
| Versanddatum | ITMTable.ShipDate | Datetime | Nein | Nein |
| Description | ITMTable.ShipDescription | Nvarchar(60) | Nein | Nein |
| Belege empfangen | ITMTable.ShipDocReceived | Int | Nein | Nein |
| Vorkalkuliertes Lieferdatum | ITMTable.ShipEstDlvDate | Datetime | Nein | Nein |
| ETA am Versandport. | ITMTable.ShipEstPortDate | Datetime | Nein | Nein |
| Von-Port | ITMTable.ShipFromPort | Nvarchar(20) | Nein | Nein |
| Haus-Luftfrachtbrief/Konnossement | ITMTable.ShipHAWB | Nvarchar(20) | Nein | Nein |
| Seereise | ITMTable.ShipId | Nvarchar(20) | **Ja** | **Ja** |
| Buchungsreferenz | ITMTable.ShipIdExternal | Nvarchar(20) | Nein | Nein |
| Reisevorlage | ITMTable.ShipJourneyId | Nvarchar(20) | Nein | Nein |
| Lokale Weiterleitung | ITMTable.ShipLocalForwarder | Nvarchar(20) | Nein | Nein |
| Hauptluftfrachtbrief/Konnossement | ITMTable.ShipMAWB | Nvarchar(20) | Nein | Nein |
| Verbrauchsberechnung | ITMTable.ShipMeasurement | Numeric(32, 6) | Nein | Nein |
| Maßeinheit | ITMTable.ShipMeasurementUnit | Int | Nein | Nein |
| Anzahl der Paletten | ITMTable.ShipNoOfPallets | Int | Nein | Nein |
| Ausstehende Seereise | ITMTable.ShipPending | Int | Nein | Nein |
| Bemerkungen | ITMTable.ShipRemarks | Nvarchar(MAX) | Nein | Nein |
| Vermietung | ITMTable.ShipRental | Int | Nein | Nein |
| Seereisestatus | ITMTable.ShipStatusId | Nvarchar(20) | Nein | Nein |
| Tally in Nummer | ITMTable.ShipTallyInNumber | Nvarchar(20) | Nein | Nein |
| Bis-Port | ITMTable.ShipToPort | Nvarchar(20) | Nein | Nein |
| Bewertungsdatum | ITMTable.ShipValuationDate | Datetime | Nein | Nein |
| Versandunternehmen | ITMTable.ShipVendAccount | Nvarchar(20) | Nein | Nein |
| Schiff | ITMTable.ShipVesselId | Nvarchar(20) | Nein | **Ja** |
| Externe Seereise-ID | ITMTable.ShipVoyage | Nvarchar(20) | Nein | Nein |

### <a name="number-sequences-for-voyages"></a>Nummernkreise für Fahrten

Die gemeinsame Sequenz für Fahrten steuert die Zuweisung von Reise-IDs.

Der Wert, der als **Reise-ID** (`ShipId`) an die Entität übergeben wird, dient zur Identifizierung eines bestehenden Datensatzes für die Aktualisierung. Wenn dieser Datensatz nicht vorhanden ist, hängt das Verhalten davon ab, ob die zugewiesene Sequenz so konfiguriert ist, dass eine manuelle Eingabe zugelassen wird:

- Wenn die manuelle Eingabe aktiviert ist, wird ein neuer Datensatz erstellt, der den übergebenen Wert verwendet.
- Wenn die manuelle Eingabe nicht aktiviert ist, wird anstelle des übergebenen Wertes die nächste Nummer in der zugewiesenen Sequenz verwendet.

Während des Imports wird der Platzhalterwert, der als ID der Fahrt importiert wird, beibehalten. Dieses Verhalten stellt sicher, dass Transportcontainer und Reisezeilen, die auf den Platzhalter verweisen, in die Fahrt einbezogen werden und dass sie aktualisiert werden, um den Wert widerzuspiegeln, der aus der Sequenz zugewiesen wird.

### <a name="automatic-cost-transactions"></a>Automatische Nachkalkulationen

Automatische Kosten können einer Fahrt von der Seite **Autokalkulation** in Microsoft Dynamics 365 Supply Chain Management (**Nachkalkulation \> Einrichtung \> Autokalkulation**) hinzugefügt werden. Datensätze für automatische Kosten können auch durch die Verwendung von Entitäten für Kostentransaktionsdaten für jeden Kostenbereich erstellt werden, den Gesamttransportkosten unterstützt.

Automatische Kosten, die im Supply Chain Management konfiguriert sind, werden auf die Fahrt angewendet, wenn eine Fahrtlinie erstellt wird. Es werden keine Nachkalkulationen für den Datensatz angezeigt, bis der Kopfdatensatz mit Zeileninformationen verknüpft ist.

## <a name="shipping-containers-itmcontainersentity"></a>Transportcontainer (ITMContainersEntity)

Ein Transportcontainer stellt einen physischen Container dar, in dem Waren transportiert werden. Dieser physische Container kann ein Frachtcontainer für Seefracht oder eine einzelne Palette für Luftfracht sein. Der Transportcontainer enthält Informationen auf Kopfebene, die sich auf die Transportcontainer-ID, die Siegelnummer und den Transportcontainer-Typ beziehen. (Der Typ des Transportcontainers liefert Informationen zu den Dimensionen.) Diese Funktion wird von der Entität `ITMContainersEntity` unterstützt. In der folgenden Tabelle sind die Felder und Zuordnungen aufgeführt, aus denen diese Entität besteht.

| Name | Zuordnung | Datentyp | Schlüssel | Obligatorisch |
|---|---|---|---|---|
| Abgangsdatum | ITMContainers.ITMDepartureDate | Datetime | Nein | Nein |
| Datum des lokalen Transports | ITMContainers.ITMLocalTransportDate | Datetime | Nein | Nein |
| Uhrzeit des lokalen Transports | ITMContainers.ITMLocalTransportTime | Int | Nein | Nein |
| Ursprüngliche Seereise | ITMContainers.OrigShipId | Nvarchar(20) | Nein | Nein |
| Tatsächliches Gewicht | ITMContainers.ShipActualWeight | Numeric(32, 6) | Nein | Nein |
| Vom Broker empfohlen | ITMContainers.ShipBrokerAdvised | Datetime | Nein | Nein |
| Versandcontainer | ITMContainers.ShipContainerId | Nvarchar(20) | **Ja** | **Ja** |
| Versandcontainertyp | ITMContainers.ShipContainerTypeId | Nvarchar(20) | Nein | Nein |
| Einheitstyp | ITMContainers.ShipContainerUnitTypeId | Nvarchar(10) | Nein | Nein |
| In Vermietung konvertiert | ITMContainers.ShipConvertedToRental | Int | Nein | Nein |
| Debitorentermin | ITMContainers.ShipCustomerAppointment | Datetime | Nein | Nein |
| Versanddatum | ITMContainers.ShipDate | Datetime | Nein | Nein |
| Auslieferung am Lagerort | ITMContainers.ShipDelAtWarehouse | Datetime | Nein | Nein |
| Lieferanweisungen | ITMContainers.ShipDeliveryInstructions | Datetime | Nein | Nein |
| Anwendungsdatum des Prüfungszertifikats | ITMContainers.ShipECAppliedDate | Datetime | Nein | Nein |
| Ablaufdatum des Prüfungszertifikats | ITMContainers.ShipECExpiryDate | Datetime | Nein | Nein |
| Prüfungszertifikatsnummer | ITMContainers.ShipECNum | Nvarchar(20) | Nein | Nein |
| Eingangsdatum des Prüfungszertifikats | ITMContainers.ShipECReceivedDate | Datetime | Nein | Nein |
| Vorkalkuliertes Lieferdatum | ITMContainers.ShipEstDlvDate | Datetime | Nein | Nein |
| ETA am Versandport. | ITMContainers.ShipEstPortDate | Datetime | Nein | Nein |
| Erwartetes Verladungsdatum | ITMContainers.ShipExpectedLoadingDate | Datetime | Nein | Nein |
| Von-Port | ITMContainers.ShipFromPort | Nvarchar(20) | Nein | Nein |
| Warenbeschreibung | ITMContainers.ShipGoodsDesc | Nvarchar(60) | Nein | Nein |
| Warenfreigabe | ITMContainers.ShipGoodsReleased | Datetime | Nein | Nein |
| GPS-Protokollierungseinheit | ITMContainers.ShipGPSUnit | Nvarchar(30) | Nein | Nein |
| Haus-Luftfrachtbrief/Konnossement | ITMContainers.ShipHAWB | Nvarchar(20) | Nein | Nein |
| Seereise | ITMContainers.ShipId | Nvarchar(20) | **Ja** | **Ja** |
| Reisevorlage | ITMContainers.ShipJourneyId | Nvarchar(20) | Nein | Nein |
| Lokale Weiterleitung | ITMContainers.ShipLocalForwarder | Nvarchar(20) | Nein | Nein |
| Verbrauchsberechnung | ITMContainers.ShipMeasurement | Numeric(32, 6) | Nein | Nein |
| Maßeinheit | ITMContainers.ShipMeasurementUnit | Int | Nein | Nein |
| Anzahl der Kartons | ITMContainers.ShipNoOfCartons | Numeric(32, 6) | Nein | Nein |
| Ursprünglicher Frachtbrief gesendet | ITMContainers.ShipOriginalBOLSebt | Datetime | Nein | Nein |
| Ursprüngliche Belege empfangen | ITMContainers.ShipOriginalDocsReceived | Datetime | Nein | Nein |
| Unsere Siegelnummer | ITMContainers.ShipOurSealNum | Nvarchar(20) | Nein | Nein |
| Verwendet | ITMContainers.ShipPendingUsed | Int | Nein | Nein |
| Bestellungsstatus | ITMContainers.ShipPurchStatus | Int | Nein | Nein |
| Kühlungsart | ITMContainers.ShipRefrigerationTypeId | Nvarchar(10) | Nein | Nein |
| Bemerkungen | ITMContainers.ShipRemarks | Nvarchar(MAX) | Nein | Nein |
| Vermietung | ITMContainers.ShipRental | Int | Nein | Nein |
| Retourfähig | ITMContainers.ShipReturnable | Int | Nein | Nein |
| Seereisestatus | ITMContainers.ShipStatusId | Nvarchar(20) | Nein | Nein |
| Siegelnummer des Versandunternehmens | ITMContainers.ShipTheirSealNum | Nvarchar(20) | Nein | Nein |
| Bis-Port | ITMContainers.ShipToPort | Nvarchar(20) | Nein | Nein |
| Überprüfungsdatum | ITMContainers.ShipVerificationDate | Datetime | Nein | Nein |
| Schiff | ITMContainers.ShipVesselId | Nvarchar(20) | Nein | **Ja** |

### <a name="voyage-id-validation"></a>Validierung der Reise-ID

Die ID des Transportcontainers wird nicht durch eine Sequenz von Nummern gesteuert. Er ist nur im Zusammenhang mit der Fahrt, für die er verwendet wird, eindeutig.

Wenn die Entität Transportcontainer (`ITMContainersEntity`) unabhängig von der Entität Reise (`ITMTableEntity`) verwendet wird, muss der Wert **Reise-ID** (`ShipId`) mit einem bestehenden Datensatz in der Tabelle Reise übereinstimmen. Andernfalls wird der Import fehlschlagen.

Wenn die Entität Transportcontainer (`ITMContainersEntity`) und die Entität Fahrt (`ITMTableEntity`) als Teil desselben Importvorgangs verwendet werden, muss die Entität Fahrt vor der Erstellung eines Transportcontainers erstellt werden. Andernfalls kann der Wert **Reise-ID** (`ShipId`) nicht erfolgreich validiert werden. Wenn für den Wert **Reise-ID** (`ShipId`) ein Platzhalterwert verwendet wird, kann die Assoziation nur erstellt werden, wenn der gleiche Platzhalter als **Reise-ID** (`ShipId`) in der Entität Transportcontainer verwendet wird.

### <a name="other-field-validations"></a>Andere Feldüberprüfungen

Die folgende Tabelle zeigt die Felder in der Tabelle der Transportcontainer (`ITMContainers`), die mit den Tabellen der Einrichtung für Gesamttransportkosten abgeglichen werden. Es zeigt auch die Entitäten der Gesamttransportkosten an, die ein Spediteur verwenden kann, um die vorhandenen Werte zu lesen und sicherzustellen, dass in Ihrer Umgebung gültige Werte empfangen werden.

| Feld in der Tabelle ITMContainers | Gesamttransportkosten Entität |
|---|---|
| Versandcontainertyp | ITMShippingContainerTypeEntity |
| Warenbeschreibung | ITMGoodsDescriptionEntity |
| Kühlungsart | ITMShippingContainerRefrigerationTypeEntity |

## <a name="folios-itmfolioentity"></a>Folios (ITMFolioEntity)

Eine Palette stellt eine Gruppierung von Artikeln in einem Transportcontainer für die Zwecke von Zollerklärungen dar. Die Palette enthält Informationen auf Kopfebene, die sich auf den Zoll Broker und eine Beschreibung der Waren beziehen. Diese Funktionalität wird von der Entität `ITMFolioEntity` unterstützt. In der folgenden Tabelle sind die Felder und Zuordnungen aufgeführt, aus denen diese Entität besteht.

| Name | Zuordnung | Datentyp | Schlüssel | Obligatorisch |
|---|---|---|---|---|
| Vom Broker empfohlen | ITMFolioTable.ShipBrokerAdvised | Datetime | Nein | Nein |
| Frachtkontrollnummer | ITMFolioTable.ShipCargoControlNumber | Nvarchar(20) | Nein | Nein |
| Debitorentermin | ITMFolioTable.ShipCustomerAppointment | Datetime | Nein | Nein |
| Zollbroker | ITMFolioTable.ShipCustomsBroker | Nvarchar(20) | Nein | Nein |
| Zoll-ID | ITMFolioTable.ShipCustomsId | Nvarchar(60) | Nein | Nein |
| Unternehmen | ITMFolioTable.ShipDataArea | Nvarchar(4) | Nein | **Ja** |
| Auslieferung am Lagerort | ITMFolioTable.ShipDelAtWarehouse | Datetime | Nein | Nein |
| Lieferanweisungen | ITMFolioTable.ShipDeliveryInstructions | Datetime | Nein | Nein |
| Belege empfangen | ITMFolioTable.ShipDocReceived | Int | Nein | Nein |
| Vorkalkuliertes Lieferdatum | ITMFolioTable.ShipEstDlvDate | Datetime | Nein | Nein |
| ETA am Versandport. | ITMFolioTable.ShipEstPortDate | Datetime | Nein | Nein |
| Exporteur | ITMFolioTable.ShipExporterId | Nvarchar(20) | Nein | Nein |
| Name | ITMFolioTable.ShipExporterName | Nvarchar(60) | Nein | Nein |
| Foliodatum | ITMFolioTable.ShipFolioDate | Datetime | Nein | Nein |
| Folio | ITMFolioTable.ShipFolioId | Nvarchar(20) | **Ja** | **Ja** |
| Von-Port | ITMFolioTable.ShipFromPort | Nvarchar(20) | Nein | Nein |
| Warenbeschreibung | ITMFolioTable.ShipGoodsDesc | Nvarchar(60) | Nein | Nein |
| Warenfreigabe | ITMFolioTable.ShipGoodsReleased | Datetime | Nein | Nein |
| Haus-Luftfrachtbrief/Konnossement | ITMFolioTable.ShipHAWB | Nvarchar(20) | Nein | Nein |
| Seereise | ITMFolioTable.ShipId | Nvarchar(20) | Nein | **Ja** |
| Verbrauchsberechnung | ITMFolioTable.ShipMeasurement | Numeric(32, 6) | Nein | Nein |
| Maßeinheit | ITMFolioTable.ShipMeasurementUnit | Int | Nein | Nein |
| Anzahl der Kartons | ITMFolioTable.ShipNoOfCartons | Numeric(32, 6) | Nein | Nein |
| Ursprünglicher Frachtbrief gesendet | ITMFolioTable.ShipOriginalBOLSebt | Datetime | Nein | Nein |
| Ursprüngliche Belege empfangen | ITMFolioTable.ShipOriginalDocsReceived | Datetime | Nein | Nein |
| Bestellungsstatus | ITMFolioTable.ShipPurchStatus | Int | Nein | Nein |
| Bemerkungen | ITMFolioTable.ShipRemarks | Nvarchar(MAX) | Nein | Nein |
| Seereisestatus | ITMFolioTable.ShipStatusId | Nvarchar(20) | Nein | Nein |
| Tarifcode | ITMFolioTable.ShipTariffCode | Nvarchar(10) | Nein | Nein |
| Bis-Port | ITMFolioTable.ShipToPort | Nvarchar(20) | Nein | Nein |
| Bewertungsdatum | ITMFolioTable.ShipValuationDate | Datetime | Nein | Nein |
| Überprüfungsdatum | ITMFolioTable.ShipVerificationDate | Datetime | Nein | Nein |
| Kreditorenkonto | ITMFolioTable.VendAccount | Nvarchar(20) | Nein | Nein |

### <a name="number-sequences-for-folios"></a>Nummernkreise für Paletten

Der Nummernkreis für Paletten steuert die Zuordnung der Paletten-IDs.

Der Wert, der als **Folio ID** (`FolioId`) an die Entität übergeben wird, dient zur Identifizierung eines bestehenden Datensatzes für die Aktualisierung. Wenn dieser Datensatz nicht vorhanden ist, hängt das Verhalten davon ab, ob die zugewiesene Sequenz so konfiguriert ist, dass eine manuelle Eingabe zugelassen wird:

- Wenn die manuelle Eingabe aktiviert ist, wird ein neuer Datensatz erstellt, der den übergebenen Wert verwendet.
- Wenn die manuelle Eingabe nicht aktiviert ist, wird anstelle des übergebenen Wertes die nächste Nummer in der zugewiesenen Sequenz verwendet.

Während des Imports wird der Platzhalterwert, der als Paletten-ID importiert wird, beibehalten. Dieses Verhalten stellt sicher, dass Fahrtlinien, die auf den Platzhalter verweisen, korrekt zugeordnet werden und dass sie aktualisiert werden, um den Wert widerzuspiegeln, der aus der Sequenz zugewiesen wird.

### <a name="field-validations"></a>Feldüberprüfungen

Das Feld **Beschreibung der Waren** in der Palette (`ITMFolioTable`) wird mit der gleichnamigen Tabelle für die Einrichtung der Gesamttransportkosten abgeglichen. Ein Spediteur kann die Entität `ITMGoodsDescriptionEntity` für kalkulierte Gesamttransportkosten verwenden, um die vorhandenen Werte zu lesen und sicherzustellen, dass in Ihrer Umgebung gültige Werte eingehen.

## <a name="voyage-lines-for-purchase-orders-itmpurchaselineentity"></a>Fahrt-Zeilen für Kauf-Bestellungen (ITMPurchaseLineEntity)

Die Zeile für die Reise stellt eine einzelne Zeile für eine Bestellung dar, die in der Reise enthalten ist. Diese Beziehung wird über die Felder **Bestellnummer** und **Einkaufszeilennummer** hergestellt. Die Reisezeile verweist auf jeden vorherigen Datensatz, der für die Fahrt, den Transportcontainer und die Palette erstellt wurde. Diese Funktionalität wird von der Entität `ITMPurchaseLineEntity` unterstützt. In der folgenden Tabelle sind die Felder und Zuordnungen aufgeführt, aus denen diese Entität besteht.

| Name | Zuordnung | Datentyp | Schlüssel | Obligatorisch |
|---|---|---|---|---|
| Währung | ITMLine.CurrencyCode | Nvarchar(3) | Nein | Nein |
| Nettobetrag | ITMLine.LineAmountMST | Numeric(32, 6) | Nein | Nein |
| Bestellpositionsnummer | ITMLine.RefRecId | Numeric(32, 6) | **Ja** | Nein |
| Versandcontainer | ITMLine.ShipContainerId | Int | Nein | Nein |
| Unternehmen | ITMLine.ShipDataArea | Nvarchar(20) | **Ja** | Nein |
| Deklarierte Menge | ITMLine.ShipDeclaredQty | Nvarchar(4) | Nein | Nein |
| Folio | ITMLine.ShipFolioId | Numeric(32, 6) | Nein | Nein |
| Seereise | ITMLine.ShipId | Nvarchar(20) | **Ja** | Nein |
| Artikelnummer | ITMLine.ShipItemId | Nvarchar(20) | Nein | Nein |
| Verbrauchsberechnung | ITMLine.ShipMeasurement | Nvarchar(20) | Nein | Nein |
| Maßeinheit | ITMLine.ShipMeasurementUnit | Numeric(32, 6) | Nein | Nein |
| Anzahl der Kartons | ITMLine.ShipNoOfCartons | Int | Nein | Nein |
| Lagerplatz | ITMLine.ShipPosition | Numeric(32, 6) | Nein | Nein |
| Menge | ITMLine.ShipQty | Int | Nein | Nein |
| Bestellnummer | ITMLine.TransRefId | Numeric(32, 6) | **Ja** | Nein |
| Einheit | ITMLine.UnitId | Int | Nein | Nein |
| Volume | ITMLine.Volume | Nvarchar(10) | Nein | Nein |
| Gewicht | ITMLine.Weight | Numeric(32, 6) | Nein | Nein |

## <a name="voyage-lines-for-transfer-orders-itmtransferlineentity"></a>Zeilen für Fahrten zu Umlagerungsaufträgen (ITMTransferLineEntity)

Die Zeile für die Fahrt stellt eine einzelne Zeile für einen Umlagerungsauftrag dar, der in der Fahrt enthalten ist. Diese Beziehung wird über die Felder **Umlagerungsauftragsnummer** und **Übertragungszeilennummer** hergestellt. Die Reisezeile verweist auf jeden vorherigen Datensatz, der für die Fahrt, den Transportcontainer und die Palette erstellt wurde. Diese Funktionalität wird von der Entität `ITMTransferLineEntity` unterstützt. In der folgenden Tabelle sind die Felder und Zuordnungen aufgeführt, aus denen diese Entität besteht.

| Name | Zuordnung | Datentyp | Schlüssel | Obligatorisch |
|---|---|---|---|---|
| Währung | ITMLine.CurrencyCode | Nvarchar(3) | Nein | Nein |
| Nettobetrag | ITMLine.LineAmountMST | Numeric(32, 6) | Nein | Nein |
| Versandcontainer | ITMLine.ShipContainerId | Int | Nein | Nein |
| Unternehmen | ITMLine.ShipDataArea | Nvarchar(20) | **Ja** | Nein |
| Deklarierte Menge | ITMLine.ShipDeclaredQty | Nvarchar(4) | Nein | Nein |
| Folio | ITMLine.ShipFolioId | Numeric(32, 6) | Nein | Nein |
| Seereise | ITMLine.ShipId | Nvarchar(20) | **Ja** | Nein |
| Artikelnummer | ITMLine.ShipItemId | Nvarchar(20) | Nein | Nein |
| Verbrauchsberechnung | ITMLine.ShipMeasurement | Nvarchar(20) | Nein | Nein |
| Maßeinheit | ITMLine.ShipMeasurementUnit | Numeric(32, 6) | Nein | Nein |
| Anzahl der Kartons | ITMLine.ShipNoOfCartons | Int | Nein | Nein |
| Lagerplatz | ITMLine.ShipPosition | Numeric(32, 6) | Nein | Nein |
| Menge | ITMLine.ShipQty | Int | Nein | Nein |
| Umlagerungspositionsnummer | ITMLine.TransferLineNumber | Numeric(32, 6) | **Ja** | Nein |
| Umlagerungsauftragsnummer | ITMLine.TransRefId | Numeric(32, 6) | **Ja** | Nein |
| Einheit | ITMLine.UnitId | Int | Nein | Nein |
| Volume | ITMLine.Volume | Nvarchar(10) | Nein | Nein |
| Gewicht | ITMLine.Weight | Numeric(32, 6) | Nein | Nein |

### <a name="reference-table"></a>Bezugstabelle

Reisezeilen werden durch eine Verknüpfung mit einer offenen eingehenden Auftragszeile erstellt. Diese Zeile kann sich auf einer Bestellung befinden, oder sie kann die Empfangstransaktion auf einem Umlagerungsauftrag sein. Das Feld `RefTableId` in der Tabelle der Fahrt-Zeilen (`ITMLine`) gibt an, auf welche Auftragsart sich die Zeile bezieht, indem es sich auf die Tabellennummer bezieht. Wenn in der Tabelle, in der die Daten erstellt werden, auf bestimmte Tabellennummern verwiesen wird, werden die Entitäten basierend auf diesen Werten aufgeteilt.

Die Werte für die Referenztabelle (`RefTableId`) und die Transaktionsart (`TransType`) sind implizit in der Auswahl der Entität Gesamttransportkosten kalkulierte Zeile oder Gesamttransportkosten kalkulierte Zeile enthalten.

### <a name="validation"></a>Prüfung

Eine Zeile für eine Fahrt verweist direkt auf einen Datensatz für eine Fahrt, einen Datensatz für einen Transportcontainer und einen Datensatz für eine Palette. Wenn die Entität der Kaufzeile (`ITMPurchaseLinesEntity`) oder der Überweisungszeile (`ITMPurchaseLinesEntity`) unabhängig von den Entitäten verwendet wird, die zum Erstellen dieser Referenzdatensätze verwendet werden, müssen die Werte **Reise-ID** (`ShipId`), **Transportcontainer** (`ShipContainerId`) und **Folio** (`ShipFolioId`) mit einem vorhandenen Datensatz in den entsprechenden Tabellen übereinstimmen. Andernfalls wird der Import fehlschlagen.

Wenn eine der beiden Entitäten für eine Zeile als Teil desselben Importvorgangs verwendet wird, müssen diese anderen Entitäten vor der Erstellung einer Zeile für eine Fahrt erstellt werden. Andernfalls können die Werte nicht erfolgreich validiert werden. Wenn ein Platzhalterwert für die Fahrt- oder Folionummer verwendet wird, kann die Assoziation nur erstellt werden, wenn derselbe Platzhalter für die Fahrt- oder Folionummer in der Entität Fahrtlinie verwendet wird.

Wenn die Zeile für die Bestellung oder den Umlagerungsauftrag bereits einer bestehenden Zeile für die Fahrt zugeordnet ist, wird die neue Zeile für die Fahrt nicht erstellt. Bevor die Auftragszeile einer neuen Fahrt zugewiesen werden kann, muss sie von ihrer aktuellen Fahrt entfernt werden.

### <a name="order-line-identification"></a>Identifikation der Auftragszeilen

Voyage-Zeilen verweisen direkt auf die Referenzwerte **Datensatz-ID** (`RefRecId`), **Bestandsdimensions-ID** (`InventDimId`) und **Bestandstransaktions-ID** (`InventTransId`). Diese Werte müssen nicht mehr berücksichtigt werden, wenn die Entität Daten verwendet wird. Stattdessen muss nun die Nummer der Auftragszeile angegeben werden. Anhand der Zeilen- und der Auftragsnummer können Sie jeden dieser Referenzwerte identifizieren.

### <a name="voyage-line-quantity"></a>Menge der Fahrt-Zeilen

Da eine Reisezeile direkt mit einer Auftragszeile verknüpft ist, muss der **Menge** (`ShipQty`) Wert, der über die Entität eingegeben wird, mit den Werten übereinstimmen. Die Validierung wird anhand der Menge in der Zeile der Bestellung oder des Umlagerungsauftrags ausgeführt. Wenn die Validierung fehlschlägt, wird der Datensatz nicht verarbeitet.

### <a name="calculated-fields"></a>Berechnete Felder

Die berechneten Felder **Gewicht** und **Volumen** akzeptieren die Werte, die über die Entität Daten empfangen werden. Werden keine Werte angegeben, werden die Systemwerte zur Aktualisierung dieser Felder verwendet, sofern Systemwerte verfügbar sind. Für die Gesamttransportkosten werden die Werte wie folgt berechnet:

- *Gewicht* = *Menge* × *Artikel Bruttogewicht*
- *Volumen* = *Menge* × (*Artikel-Bruttotiefe* × *Artikel-Brutto-Höhe* × *Artikel-Brutto-Breite*)

## <a name="sequencing"></a>Abfolge

Aufgrund von Abhängigkeiten zwischen den Tabellen muss der Datensatz für die Fahrt zuerst erstellt werden. Die Zeile für die Reise kann erst erstellt werden, nachdem die Reise, der Transportcontainer und die Paletten erstellt wurden.

Um eine Fahrt ohne Validierungswarnungen zu erstellen, muss das System die Entitäten in der folgenden Reihenfolge verarbeiten:

1. Fahrten (`ITMTableEntity`)
1. Transportcontainer (`ITMContainersEntity`)
1. Paletten (`ITMFolioTableEntity`)
1. Reisezeilen (`ITMPurchaseLinesEntity` oder `ITMTransferLinesEntity`)
