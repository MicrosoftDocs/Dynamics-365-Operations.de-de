---
title: In der Planungsoptimierung verwendete Datums- und Zeitparameter
description: Dieser Artikel enthält Informationen zu den Datums- und Uhrzeitparametern, die Planning Optimization während des Betriebs verwendet.
author: t-benebo
ms.date: 09/21/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-09-21
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 807834bf5cd062ed24e5e3f3512d8389717a2d39
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885898"
---
# <a name="date-and-time-parameters-used-by-planning-optimization"></a>In der Planungsoptimierung verwendete Datums- und Zeitparameter

[!include [banner](../../includes/banner.md)]

Dieser Artikel enthält Informationen zu den Datums- und Uhrzeitparametern, die Planning Optimization während des Betriebs verwendet.

Während die integrierte Masterplanungs-Engine in allen Berechnungen Transaktionsdaten verwendet, arbeitet die Planungsoptimierung mit Datums- und Uhrzeitwerten, die in Datumsangaben umgewandelt werden. Dieses unterschiedliche Verhalten kann zu Situationen führen, in denen beispielsweise Prognosetransaktionen, die am Tag der Ausführung der Masterplanung um Mitternacht erstellt werden, nicht berücksichtigt werden, da die Planungsoptimierung davon ausgeht, dass sie vor dem aktuellen Datum erstellt wurden.

## <a name="parameters-for-issue-and-demand-transactions"></a>Parameter für Ausgabe- und Bedarfstransaktionen

In der folgenden Tabelle sind die Parameter aufgeführt, die Planning Optimization bei der Verarbeitung von Ausgabe- und Bedarfstransaktionen verwendet.

| Parameter | Parametername in Planning Optimization  | Beschreibung | Äquivalentes Feld in Microsoft Dynamics 365 Supply Chain Management (in der ReqTrans-Tabelle) |
|---|---|---|---|
| Geplante Uhrzeit der Ausstellung | `PlannedIssueTime` | Das Datum zum dem die Ausgabe derzeit geplant ist. | **Bis jetzt** (`FuturesDate`) und **Verzögert bis Uhrzeit** (`FuturesTime`) |
| Angeforderte Ausgabezeit | `RequestedIssueTime` | Das Ausstellungsdatum, das vom Benutzer angefordert und in Supply Chain Management festgelegt wurde. Dieser Parameter gilt nur für freigegebene oder genehmigte Planaufträge. Bei Planaufträgen ist er standardmäßig leer. | **Angefordertes Datum** (`ReqDateDlvOrig`) |
| Erforderliche Ausgabezeit | `RequiredIssueTime` | Das erforderliche Ausstellungsdatum, das von der Planning Optimization angepasst wird. Wenn die angeforderte Ausgabezeit beim Ausführen von Planning Optimization in der Vergangenheit liegt, wird die erforderliche Ausgabezeit an den ersten offenen Tag angepasst, der nicht vor dem heutigen Datum liegt. Ist die gewünschte Ausgabezeit im Kalender als gesperrt gekennzeichnet, wird die gewünschte Ausgabezeit an den ersten offenen Tag vor diesem Datum angepasst. | **Anforderungsdatum** (`ReqDate`) und **Anforderungszeit** (`ReqTime`) |
| Verzögerung der Ausgabezeit | `IssueTimeDelay` | Der Zeitunterschied zwischen der geplanten Ausgabezeit und entweder der angeforderten Ausgabezeit für genehmigte und freigegebene Aufträge oder der erforderlichen Ausgabezeit. | **Verzögerung (in Tagen)** (`FuturesDays`) |

## <a name="parameters-for-receipt-and-supply-transactions"></a>Parameter für Eingangs- und Liefertransaktionen

In der folgenden Tabelle sind die Parameter aufgeführt, die Planning Optimization bei der Verarbeitung von Eingangs- und Ausgabe- und Lieferungstransaktionen verwendet.

| Parameter | Parametername in Planning Optimization  | Beschreibung | Äquivalentes Feld im Supply Chain Management (in der Tabelle ReqTrans oder ReqPO) |
|---|---|---|---|
| Geplante Verfügbarkeitszeit | `PlannedAvailabilityTime` | Das Datum, an dem die Verfügbarkeit des Eingangs geplant ist. | **Anforderungsdatum** (`ReqDate`) und **Anforderungszeit** (`ReqTime`) |
| Geplante Eingangszeit | `PlannedReceiptTime` | Das Datum, an dem der Eingang am Standort eintrifft. | **Bis jetzt** (`FuturesDate`), **Zeitverzögert** (`FuturesTime`) und **Lieferdatum** (`ReqDateDlv`) oder **Wunschtermin** (`ReqDateDlvOrig`), wenn die Bestellung noch nicht freigegeben ist. |
| Erforderliche Verfügbarkeitszeit | `RequiredAvailabilityTime` | Das erforderliche Verfügbarkeitsdatum, das von der Planning Optimization angepasst wird. | **Anforderungsdatum** (`ReqDate`) und **Anforderungszeit** (`ReqTime`) |
| Erwartete Eingangszeit | `ExpectedReceiptTime` | Das erwartete Eingangsdatum für einen freigegebenen Eingang. Der Wert wird vom Benutzer im Supply Chain Management festgelegt und nicht von Planning Optimization angepasst. Dieser Parameter gilt nur für freigegebene Eingänge. | **Angefordertes Datum** (`ReqDateDlvOrig`) |
| Erforderliche Eingangszeit | `RequiredReceiptTime` | Das erforderliche Eingangsdatum, das von der Planning Optimization angepasst wird. | **Anforderungsdatum** (`ReqDate`) und **Anforderungszeit** (`ReqTime`) |
| Geplante Bestellzeit | `PlannedOrderingTime` | Das Bestelldatum, das von Planning Optimization berechnet wird. | **Bestelldatum** (`ReqDateOrder`) und **Bestellzeitpunkt** (`ReqTimeOrder`) |
| Geplante Startzeit der Aktivität | `PlannedActivityStartTime` | Das Datum, an dem die Aktivität für diesen Eingang beginnen soll. | **Startdatum** (`SchedFromDate`) |
| Eingangszeitverzögerung | `ReceiptTimeDelay` | Die Zeitdifferenz zwischen der geplanten Eingangszeit und der gewünschten Eingangszeit. | **Verzögerung (Tage)** (`FuturesDays`) und **Verzögern zur Zeit** (`FuturesTime`) |

## <a name="examples-of-date-parameter-use-by-planning-optimization"></a>Beispiele der Datumsparameterverwendung von Planning Optimization

Die Pläne in den folgenden Abbildungen sind auf Tagesebene, aber Planning Optimization wird auf einer detaillierteren Ebene ausgeführt. Da Margen beispielsweise in Stunden angegeben werden können, kann die Planungsbestellungszeit der 22. Januar 2021, 11:35 Uhr usw. sein.

### <a name="example-1-simple-scenario"></a>Beispiel 1: Einfaches Szenario

Ein Auftrag mit einem angeforderten Ausgabezeitpunkt am 22. Januar wird durch eine Bestellung abgedeckt. Die folgenden Einstellungen werden verwendet:

- Keine Vorlaufzeit
- Keine Kalender (Alle Tage sind geöffnet.)
- Keine Margen

Die folgende Abbildung zeigt dieses Szenario. (Wählen Sie die Abbildung aus, um eine größere Version zu öffnen.)

[![Einfaches Szenario.](media/planning-service-dates-1-small.png)](media/planning-service-dates-1.png)

### <a name="example-2-lead-time-scenario"></a>Beispiel 2: Vorlaufzeitszenario

Ein Auftrag mit einem angeforderten Ausgabezeitpunkt am 22. Januar wird durch eine Bestellung abgedeckt. Die folgenden Einstellungen werden verwendet:

- Drei Tage Vorlaufzeit
- Keine Kalender (Alle Tage sind geöffnet.)
- Keine Margen

Die folgende Abbildung zeigt dieses Szenario. (Wählen Sie die Abbildung aus, um eine größere Version zu öffnen.)

[![Vorlaufzeitszenario.](media/planning-service-dates-2-small.png)](media/planning-service-dates-2.png)

### <a name="example-3-margin-scenario"></a>Beispiel 3: Margen-Szenario

Ein Auftrag mit einem angeforderten Ausgabezeitpunkt am 22. Januar wird durch eine Bestellung abgedeckt. Die folgenden Einstellungen werden verwendet:

- Drei Tage Vorlaufzeit
- Vier-Tage-Bestellmarge
- Fünf-Tage-Verfügbarkeitsmarge
- Keine Kalender (Alle Tage sind geöffnet.)

Die folgende Abbildung zeigt dieses Szenario. (Wählen Sie die Abbildung aus, um eine größere Version zu öffnen.)

[![Margen-Szenario.](media/planning-service-dates-3-small.png)](media/planning-service-dates-3.png)

### <a name="example-4-delay-scenario"></a>Beispiel 4: Verzögerungsszenario

Ein Auftrag mit einem angeforderten Ausgabezeitpunkt am 22. Januar wird durch eine Bestellung abgedeckt. In diesem Beispiel werden dieselben Einstellungen wie in Beispiel 3 verwendet, das Planungsdatum wurde jedoch auf den 15. Januar verschoben. Die Rückwärtsterminierung (rote Markierungen) schlägt fehl, da die geplante Bestellzeit vor dem heutigen Datum liegen müsste. Daher muss die Masterplanung nach vorne terminieren, und es kommt zu Verzögerungen.

Die folgende Abbildung zeigt dieses Szenario. (Wählen Sie die Abbildung aus, um eine größere Version zu öffnen.)

[![Verzögerungsszenario.](media/planning-service-dates-4-small.png)](media/planning-service-dates-4.png)

### <a name="example-5-transfer-scenario"></a>Beispiel 5: Übertragungsszenario

Ein Kundenauftrag aus Lagerort 1 mit gewünschtem Ausgabezeitpunkt am 22. Januar wird durch einen Umlagerungsauftrag aus Lagerort 2 abgedeckt, der durch eine geplante Einkaufsbestellung abgedeckt ist. Die folgenden Einstellungen werden verwendet:

- Drei Tage Umlagerungsvorlaufzeit (Lagerort 1)
- Zwei Tage Einkaufsvorlaufzeit (Lagerort 2)
- Keine Kalender (Alle Tage sind geöffnet.)

Die folgende Abbildung zeigt dieses Szenario. (Wählen Sie die Abbildung aus, um eine größere Version zu öffnen.)

[![Umlagerungsszenario.](media/planning-service-dates-5-small.png)](media/planning-service-dates-5.png)

### <a name="example-6-lead-time-with-calendars-scenario"></a>Beispiel 6: Vorlaufzeit mit Kalenderszenario

Ein Auftrag mit einem angeforderten Ausgabezeitpunkt am 22. Januar wird durch eine Bestellung abgedeckt. Die folgenden Einstellungen werden verwendet:

- Drei Tage Vorlaufzeit
- Ausgabekalender (Freitag geschlossen)
- Verfügbarkeitskalender (Donnerstag und Freitag geschlossen)
- Eingangskalender (Dienstag, Mittwoch und Sonntag geschlossen)
- Volaufszeitkalender (Donnerstag und Freitag geschlossen)
- Bestellkalender (Montag und Samstag geöffnet)

Die folgende Abbildung zeigt dieses Szenario. (Wählen Sie die Abbildung aus, um eine größere Version zu öffnen.)

[![Vorlaufzeit mit Kalenderszenario.](media/planning-service-dates-6-small.png)](media/planning-service-dates-6.png)

### <a name="example-7-delay-with-calendars-scenario"></a>Beispiel 7: Verzögerung mit Kalenderszenario

Ein Auftrag mit einem angeforderten Ausgabezeitpunkt am 22. Januar wird durch eine Bestellung abgedeckt. In diesem Beispiel werden dieselben Einstellungen wie in Beispiel 6 verwendet, das Planungsdatum wurde jedoch auf den 13. Januar verschoben. Die Rückwärtsterminierung (rote Markierungen) schlägt fehl, da die geplante Bestellzeit vor dem heutigen Datum liegen müsste. Daher muss die Masterplanung nach vorne terminieren, und es kommt zu Verzögerungen.

Die folgende Abbildung zeigt dieses Szenario. (Wählen Sie die Abbildung aus, um eine größere Version zu öffnen.)

[![Verzögerung mit Kalenderszenario.](media/planning-service-dates-7-small.png)](media/planning-service-dates-7.png)
