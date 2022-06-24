---
title: Integration in Fertigungssteuerungssysteme von Drittanbietern
description: In diesem Artikel wird erläutert, wie Sie Microsoft Dynamics 365 Supply Chain Management in ein Fertigungssteuerungssystem (Manufacturing Execution System, MES) eines Drittanbieters integrieren können.
author: johanhoffmann
ms.date: 10/01/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-10-01
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 208ed2d6c8b411d12888966d9c175730e828eb44
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860637"
---
# <a name="integrate-with-third-party-manufacturing-execution-systems"></a>Integration in Fertigungssteuerungssysteme von Drittanbietern

[!include [banner](../includes/banner.md)]

Einige Fertigungsunternehmen, die Microsoft Dynamics 365 Supply Chain Management verwenden, verwenden die native Funktionalität in Dynamics 365, um ihre Fertigungsaktivitäten für Maschinen, Ausrüstung und Personal zu steuern. Andere Fertigungsunternehmen, insbesondere solche mit erweiterten Fertigungsanforderungen, verwenden jedoch stattdessen ein Drittanbieter-MES. Unternehmen entscheiden sich möglicherweise für eine MES-Lösung eines Drittanbieters, weil sie beispielsweise speziell auf ihre vertikale Branche zugeschnitten ist.

In der integrierten Lösung erfolgt der Datenaustausch vollautomatisiert und nahezu in Echtzeit. Daher werden die Daten in beiden Systemen aktuell gehalten, und es ist keine manuelle Dateneingabe erforderlich. Wenn beispielsweise der Materialverbrauch im MES erfasst wird, sorgt die Integration dafür, dass derselbe Verbrauch auch in Dynamics 365 erfasst wird. Somit stehen aktuelle Bestandsaufzeichnungen anderen wichtigen Prozessen wie Planung und Verkauf zur Verfügung.

Die Lösung macht es für Supply Chain Management-Benutzer schneller, einfacher und kostengünstiger, sich in MESs von Drittanbietern zu integrieren. Sie bietet die folgenden Funktionen:

- Geschäftsereignisse und Schnittstellen, die [Schlüsselprozesse der Fertigungssteuerung](#processes-available-for-mes-integration) unterstützen
- Ein zentralisiertes Dashboard, in dem Sie den Verlauf der Ereignisverarbeitung verfolgen und fehlgeschlagene Prozesse behandeln und beheben können

Die folgende Abbildung zeigt eine typische Sammlung von Geschäftsereignissen, Prozessen und Nachrichten, die in einer integrierten Lösung ausgetauscht werden.

![Typisches Integrationsszenario.](media/3p-mes-scenario.png "Typisches Integrationsszenario.")

## <a name="turn-on-the-mes-integration-feature"></a>Aktivieren der MES-Integrationsfunktion

Bevor Sie diese Funktion nutzen können, muss ein Administrator sie in Ihrem System aktivieren, wie im folgenden Verfahren beschrieben.

1. Gehen Sie zu **Systemadministration \> Einrichten \> Lizenzkonfiguration**.
1. Stellen Sie sicher, dass der **Zeit und Anwesenheit**-Lizenzschlüssel aktiviert ist (Häkchen). Dieser Lizenzschlüssel ist erforderlich, da er die Funktionalität und Daten des Fertigungssteuerungssystems steuert. Wenn es nicht aktiviert ist, führen Sie die folgenden Schritte aus:
    1. Legen Sie Ihr System in den Wartungsmodus ein, wie in [Wartungsmodus](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) beschrieben.
    1. Auf der Seite **Lizenzkonfiguration** wählen Sie das **Zeit und Anwesenheit**-Kontrollkästchen aus.
    1. Schalten Sie den Wartungsmodus aus, wie in [Wartungsmodus](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) beschrieben.
1. Wechseln Sie zu **Systemverwaltung \> Arbeitsbereiche \> Funktionsverwaltung**.
1. Schalten Sie die Funktion ein, die auf folgende Weise aufgelistet ist (siehe auch [Übersicht über die Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)):
    - **Modul:** *Produktionssteuerung*
    - **Funktionsname:** *Integration des Fertigungssteuerungssystems*

## <a name="processes-available-for-mes-integration"></a>Verfügbare Prozesse für die MES-Integration

Sie können einen oder alle der folgenden Prozesse für die Integration aktivieren.

| Prozessname | Description |
|---|---|
| Produktionsaufträge und Geschäftsereignisse zur Änderung des Produktionsauftragsstatus freigeben | Dieser Prozess stellt ein Geschäftsereignis bereit, das das MES abhören kann, um Informationen über die zu produzierenden Produktionsaufträge zu erhalten. Es wird erwartet, dass Referenzdaten, die sich auf den Produktionsauftrag beziehen, von Supply Chain Management über Open Data Protocol (OData) oder Datenentitäten an das MES weitergegeben werden. |
| Produktionsauftrag starten | Dieser Prozess liefert Supply Chain Management Informationen über Produktionsaufträge, die über das MES gestartet werden. Er stellt sicher, dass beide Systeme einen aktuellen Überblick über alle Fertigungsaktivitäten haben. |
| Produzierte oder verschrottete Menge melden | Dieser Prozess liefert Supply Chain Management Informationen über die Gut- und Ausschussmengen, die zu einem Produktionsauftrag mithilfe von MES gemeldet werden. Er stellt sicher, dass die Fertigungsleiter einen aktuellen Überblick über den Fortschritt des Produktionsplans haben. |
| Materialverbrauch melden | Dieser Prozess liefert Supply Chain Management Informationen aus dem MES über die verbrauchten Materialmengen. Er stellt aktuelle Bestandsaufzeichnungen anderen wichtigen Prozessen wie Planung und Verkauf zur Verfügung. |
| Zeitaufwand für den Vorgang melden | Dieser Prozess liefert Supply Chain Management Informationen über die Zeit, die für einen bestimmten Vorgang verwendet wird. |
| Produktionsauftrag beenden | Dieser Prozess informiert Supply Chain Management darüber, dass das MES einen Produktionsauftrag auf den Endstatus *Beendet* aktualisiert hat. Dieser Status zeigt an, dass auf dem Produktionsauftrag keine Mengen mehr produziert werden. |

## <a name="monitor-incoming-messages"></a>Eingehende Nachrichten überwachen

Um die eingehenden Nachrichten an das System zu überwachen, öffnen Sie die Seite für die **Integration von Fertigungssteuerungssystemen**. Dort können Sie Probleme anzeigen, verarbeiten und beheben.

Alle Nachrichten für einen bestimmten Produktionsauftrag werden in der Sequenz verarbeitet, in der sie eingegangen sind. Allerdings werden Nachrichten für verschiedene Produktionsaufträge möglicherweise nicht in der empfangenen Sequenz verarbeitet, da Batchaufträge parallel verarbeitet werden. Im Falle eines Fehlschlags versucht der Batchauftrag, jede Nachricht dreimal zu verarbeiten, bevor er den Status *Fehlgeschlagen* festlegt.

## <a name="call-the-api"></a>API aufrufen

Um die MES-Integrations-API aufzurufen, senden Sie eine `POST`-Anfrage an die folgende Endpunkt-URL:

`/api/services/SysMessageServices/SysMessageService/SendMessage`

Der Text der Anforderung, die Sie senden, sollte dem folgenden Beispiel ähneln. Ersetzen Sie die Werte für `_companyId`, `_messageType` und `_messageContent` nach Bedarf. Informationen zu den verschiedenen Nachrichtentypen, die die API unterstützt, und zum Entwerfen ihres Inhalts finden Sie im nächsten Abschnitt.

```json
{
    "_companyId": "USMF",
    "_messageQueue": "JmgMES3P",
    "_messageType": "ProdProductionOrderReportFinished",
    "_messageContent":
    "{\"ProductionOrderNumber\": \"P000123\", \"ReportFinishedLines\": [{\"ItemNumber\": \"A0001\", \"ReportedGoodQuantity\": 10, \"ReportAsFinishedDate\": \"2021-01-01\"}]}"
}
```

## <a name="api-message-types-and-content"></a>API-Nachrichtentypen und -inhalt

In diesem Abschnitt werden alle Nachrichtentypen beschrieben, die über die MES-Integrations-API ausgetauscht werden können.

### <a name="start-production-order-message"></a>Nachricht zum Start eines Produktionsauftrags

Für die Nachricht *Produktionsauftrag starten* ist der `_messageType`-Wert `ProdProductionOrderStart`. Die folgende Tabelle zeigt die Felder, die von dieser Nachricht unterstützt werden.

| Feldname | Status | Typ |
|---|---|---|
| `ProductionOrderNumber` | Obligatorisch | Zeichenfolge |
| `StartedQuantity` | Optional | Gleitkommazahl |
| `StartedDate` | Optional | Datum |
| `AutomaticBOMConsumptionRule` | Optional | Enumeration (FlushingPrincip \| Always \| Never) |

### <a name="report-as-finished-message"></a>Nachricht zur Fertigmeldung

Für die Nachricht zur *Fertigmeldung* ist der `_messageType`-Wert `ProdProductionOrderReportFinished`. Die folgende Tabelle zeigt die Felder, die von dieser Nachricht unterstützt werden.

| Feldname | Status | Typ |
|---|---|---|
| `ProductionOrderNumber` | Obligatorisch | Zeichenfolge |
| `ReportFinishedLines` | Obligatorisch | Eine Liste von Zeilen (mindestens eine), von denen jede die Nutzlast enthält, die in der nächsten Tabelle beschrieben sind |

Die folgende Tabelle zeigt die Felder, die jede Zeile im `ReportFinishedLines`-Abschnitt der `ProdProductionOrderReportFinished`-Nachricht unterstützt.

| Feldname | Status | Typ |
|---|---|---|
| `LineNumber` | Optional | Gleitkommazahl |
| `ItemNumber` | Optional | Zeichenfolge|
| `ProductionType` | Optional | Enumeration (MainItem \| Formula \| BOM \| Co_Product \| By_Product \| None), erweiterbar |
| `ReportedErrorQuantity` | Optional | Gleitkommazahl|
| `ReportedGoodQuantity` | Optional | Gleitkommazahl|
| `ReportedErrorCatchWeightQuantity` | Optional | Gleitkommazahl |
| `ReportedGoodCatchWeightQuantity` | Optional | Gleitkommazahl |
| `AcceptError` | Optional | Enum (Ja \| Nein) |
| `ErrorCause` | Optional | Enumeration (None \| Material \| Machine \| OperatingStaff), erweiterbar |
| `ExecutedDateTime` | Optional | DateTime |
| `ReportAsFinishedDate` | Optional | Datum |
| `AutomaticBOMConsumptionRule` | Optional | Enumeration (FlushingPrincip \| Always \| Never) |
| `AutomaticRouteConsumptionRule` | Optional |Enumeration (RouteDependent \| Always \| Never) |
| `RespectFlushingPrincipleDuringOverproduction` | Optional | Enum (Ja \| Nein) |
| `ProductionJournalNameId` | Optional | Zeichenfolge |
| `PickingListProductionJournalNameId` | Optional | Zeichenfolge|
| `RouteCardProductionJournalNameId` | Optional | Zeichenfolge |
| `FromOperationNumber` | Optional | Ganzzahl|
| `ToOperationNumber` | Optional | Ganzzahl|
| `InventoryLotId` | Optional | Zeichenfolge |
| `BaseValue` | Optional | Zeichenfolge |
| `EndJob` | Optional | Enum (Ja \| Nein) |
| `EndPickingList` | Optional | Enum (Ja \| Nein) |
| `EndRouteCard` | Optional | Enum (Ja \| Nein) |
| `PostNow` | Optional | Enum (Ja \| Nein) |
| `AutoUpdate` | Optional | Enum (Ja \| Nein) |
| `ProductColorId` | Optional | Zeichenfolge|
| `ProductConfigurationId` | Optional | Zeichenfolge |
| `ProductSizeId` | Optional | Zeichenfolge |
| `ProductStyleId` | Optional | Zeichenfolge |
| `ProductVersionId` | Optional | Zeichenfolge |
| `ItemBatchNumber` | Optional | Zeichenfolge |
| `ProductSerialNumber` | Optional | Zeichenfolge |
| `LicensePlateNumber` | Optional | Zeichenfolge |
| `InventoryStatusId` | Optional | Zeichenfolge |
| `ProductionWarehouseId` | Optional | Zeichenfolge |
| `ProductionSiteId` | Optional | Zeichenfolge |
| `ProductionWarehouseLocationId` | Optional | Zeichenfolge |
| `InventoryDimension1` bis `InventoryDimension12` | Optional | Zeichenfolge |

Die 12 erweiterbaren Dimensionen (`InventoryDimension1` bis `InventoryDimension12`) erfordern eine Anpassung und werden nicht immer verwendet. Weitere Informationen zu ihnen finden Sie unter [Neue Inventardimensionen durch Erweiterung hinzufügen](../../fin-ops-core/dev-itpro/extensibility/inventory-dimensions.md).

### <a name="material-consumption-picking-list-message"></a>Meldung zum Materialverbrauch (Kommissionierliste)

Für die Nachricht zum *Materialverbrauch (Kommissionierliste)* ist der `_messageType`-Wert `ProdProductionOrderPickingList`. Die folgende Tabelle zeigt die Felder, die von dieser Nachricht unterstützt werden.

| Feldname | Status | Typ |
|---|---|---|
| `ProductionOrderNumber` | Obligatorisch | Zeichenfolge |
| `JournalNameId` | Optional | Zeichenfolge |
| `PickingListLines` | Obligatorisch | Eine Liste von Zeilen (mindestens eine), von denen jede die Nutzlast enthält, die in der nächsten Tabelle beschrieben sind |

Die folgende Tabelle zeigt die Felder, die jede Zeile im `PickingListLines`-Abschnitt der `ProdProductionOrderPickingList`-Nachricht unterstützt.

| Feldname | Status | Typ |
|---|---|---|
| `ItemNumber` | Obligatorisch | Zeichenfolge |
| `ConsumptionBOMQuantity` | Optional | Gleitkommazahl |
| `ProposalBOMQuantity` | Optional | Gleitkommazahl |
| `ScrapBOMQuantity` | Optional | Gleitkommazahl |
| `BOMUnitSymbol` | Optional | Zeichenfolge |
| `ConsumptionInventoryQuantity` | Optional | Gleitkommazahl |
| `ProposalInventoryQuantity` | Optional | Gleitkommazahl |
| `ConsumptionCatchWeightQuantity` | Optional | Gleitkommazahl |
| `ProposalCatchWeightQuantity` | Optional | Gleitkommazahl |
| `ConsumptionDate` | Optional | Datum |
| `OperationNumber` | Optional | Ganzzahl |
| `LineNumber` | Optional | Gleitkommazahl |
| `PositionNumber` | Optional | Zeichenfolge |
| `IsConsumptionEnded` | Optional | Enum (Ja \| Nein) |
| `ErrorCause` | Optional | Enumeration (None \| Material \| Machine \| OperatingStaff), erweiterbar |
| `InventoryLotId` | Optional | Zeichenfolge |

### <a name="time-used-for-operation-route-card-message"></a>Nachricht zur für den Vorgang verwendeten Zeit (Arbeitsplanliste)

Für die *Für den Vorgang verwendete Zeit (Arbeitsplanliste)*-Nachricht ist der `_messageType`-Wert `ProdProductionOrderRouteCard`. Die folgende Tabelle zeigt die Felder, die von dieser Nachricht unterstützt werden.

| Feldname | Status | Typ |
|---|---|---|
| `ProductionOrderNumber` | Obligatorisch | Zeichenfolge |
| `JournalNameId` | Optional | Zeichenfolge |
| `RouteCardLines` | Obligatorisch | Eine Liste von Zeilen (mindestens eine), von denen jede die Nutzlast enthält, die in der nächsten Tabelle beschrieben sind |

Die folgende Tabelle zeigt die Felder, die jede Zeile im `RouteCardLines`-Abschnitt der `ProdProductionOrderRouteCard`-Nachricht unterstützt.

| Feldname | Status | Typ |
|---|---|---|
| `OperationNumber` | Obligatorisch | Ganzzahl |
| `OperationPriority` | Optional | Enumeration (Primary \| Secondary1 \| Secondary2 \| ... \| Secondary20) |
| `OperationId` | Optional | Zeichenfolge |
| `OperationsResourceId` | Optional | Zeichenfolge |
| `Worker` | Optional | Zeichenfolge |
| `HoursRouteCostCategoryId` | Optional | Zeichenfolge |
| `QuantityRouteCostCategoryId` | Optional | Zeichenfolge |
| `HourlyRate` | Optional | Gleitkommazahl |
| `Hours` | Optional | Gleitkommazahl |
| `GoodQuantity` | Optional | Gleitkommazahl |
| `ErrorQuantity` | Optional | Gleitkommazahl |
| `CatchWeightGoodQuantity` | Optional | Gleitkommazahl |
| `CatchWeightErrorQuantity` | Optional | Gleitkommazahl |
| `QuantityPrice` | Optional | Gleitkommazahl |
| `ProcessingPercentage` | Optional | Gleitkommazahl |
| `ConsumptionDate` | Optional | Datum |
| `TaskType` | Optional | Enumeration (QueueBefore \| Setup \| Process \| Overlap \| Transport \| QueueAfter \| Burden) |
| `ErrorCause` | Optional | Enumeration (None \| Material \| Machine \| OperatingStaff), erweiterbar |
| `OperationCompleted` | Optional | Enum (Ja \| Nein) |
| `BOMConsumption` | Optional | Enum (Ja \| Nein) |
| `ReportAsFinished` | Optional | Enum (Ja \| Nein) |

### <a name="end-production-order-message"></a>Nachricht zum Ende eines Produktionsauftrags

Für die Nachricht *Produktionsauftrag beenden* ist der `_messageType`-Wert `ProdProductionOrderEnd`. Die folgende Tabelle zeigt die Felder, die von dieser Nachricht unterstützt werden.

| Feldname | Status | Typ |
|---|---|---|
| `ProductionOrderNumber` | Obligatorisch | Zeichenfolge |
| `ExecutedDateTime` | Optional | DateTime |
| `EndedDate` | Optional | Datum |
| `UseTimeAndAttendanceCost` | Optional | Enum (Ja \| Nein) |
| `AutoReportAsFinished` | Optional | Enum (Ja \| Nein) |
| `AutoUpdate` | Optional | Enum (Ja \| Nein) |

## <a name="other-production-information"></a>Andere Produktionsinformationen

Die Nachrichten unterstützen Aktionen oder Ereignisse, die in der Werkstatt stattfinden. Sie werden über das in diesem Artikel beschriebene MES-Integrations-Framework verarbeitet. Der Entwurf geht davon aus, dass andere Referenzinformationen, die mit dem MES ausgetauscht werden sollen (wie z.B. produktbezogene Informationen oder die Stückliste oder Route (mit ihren spezifischen Einrichtungs- und Konfigurationszeiten), die in einem bestimmten Produktionsauftrag verwendet werden), mit Hilfe von [Daten Entitäten](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md#data-entities) über Filetransfer oder OData vom System abgerufen werden.

## <a name="receive-feedback-about-the-state-of-a-message"></a>Feedback zum Status einer Nachricht erhalten

Nachdem das MES eine Nachricht an Supply Chain Management gesendet hat, kann es für Supply Chain Management relevant sein, Feedback zum Status der Nachricht zurückzugeben. Hier sind einige Beispiele für Fälle, in denen dieses Verhalten relevant sein könnte:

- Es gibt keine Person, die für die ständige Überwachung der MES-Integration verantwortlich ist.
- Die für die Überwachung der MES-Integration verantwortliche Person möchte per E-Mail benachrichtigt werden, wenn eine Nachricht fehlschlägt, damit sie weiß, dass sie handeln muss.
- Das MES muss eine Fehlermeldung anzeigen, um den Bediener im Fertigungsbereich oder jemanden aus der IT-Abteilung zu informieren, dass er handeln muss.
- Das MES muss den Auftragsplan nach Erhalt einer Fehlermeldung (z. B. weil ein Produktionsauftrag nicht gestartet wurde) neu berechnen.

In diesen Fällen können Sie die Standardwarnungsfunktion in Supply Chain Management nutzen. Informationen zur Funktionsweise von Standardwarnungen finden Sie in den folgenden Ressourcen:

- Hilfeartikel: [Überblick über Warnungen](../../fin-ops-core/fin-ops/get-started/alerts-overview.md)
- Video: [Warnregeloptionen in Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=cpzimwOjicM&ab_channel=MicrosoftDynamics365)

Sie können beispielsweise die folgenden Benachrichtigungen einrichten, um Feedback zum Status einer Nachricht zu geben:

- Erstellen Sie ein Geschäftsereignis („Extern senden“), das verwendet wird, wenn eine Nachricht *Fehlgeschlagen* ist.
- Senden Sie eine Benachrichtigung und eine E-Mail an den IT-Administrator oder den Produktionsleiter.
