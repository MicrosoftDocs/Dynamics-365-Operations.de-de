---
title: Lagerort-App-Ereignisse
description: In diesem Thema wird die Verarbeitung von Lager-App-Ereignissen beschrieben, mit der Lager-App-Ereignismeldungen als Teil eines Stapelauftrags verarbeitet werden.
author: perlynne
manager: tfehr
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileDeviceQueueEvent
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 210008c4a1366773f465c59b38eca30f11f0b38c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428564"
---
# <a name="warehouse-app-event-processing"></a>Verarbeitung von Lager-App-Ereignissen

[!include [banner](../includes/banner.md)]

Batchaufträge, die in Supply Chain Management ausgeführt werden, können Daten aus einer Warteschlange zur Verarbeitung von Ereignissen verwenden, die von der Lager-App ausgegeben wurden, um bei Bedarf auf die signalisierten Ereignisse zu reagieren. Diese Funktion fügt der Warteschlange relevante Ereignisse als Reaktion auf bestimmte Arten von Aktionen hinzu, die von Mitarbeitern ausgeführt werden, die die App verwenden. Ein Beispiel ist die Verwendung von **Erstellen und Verarbeiten von Umlagerungsaufträgen über die Lager-App**. Mit dieser Funktion werden die Überschrift und Positionen des Umlagerungsauftrags im Back-End erstellt und aktualisiert, wenn das System den Stapelauftrag **Verarbeiten von Lager-App-Ereignissen** ausführt.

## <a name="enable-the-process-warehouse-app-events-feature"></a>Aktivieren Sie die Funktion Lager-App-Ereignisse verarbeiten

Bevor Sie diese Funktion nutzen können, müssen Sie diese auf Ihrem System aktivieren. Administratoren können die Seite [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) verwenden, um den Status der Funktion zu überprüfen und sie bei Bedarf zu aktivieren. Die Funktion Lager-App-Ereignisse verarbeiten ist aufgeführt als:

- **Module** ‑ Lagerortverwaltung
- **Funktionsname** - Lager-App-Ereignisse verarbeiten

## <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a>Richten Sie einen Stapelauftrag ein, um Lager-App-Ereignisse zu verarbeiten

### <a name="process-warehouse-app-events"></a>Lagerort-App-Ereignisse verarbeiten

Richten Sie einen geplanten Stapelauftrag ein, um die Lager-App-Ereignisse für die Erstellung des Umlagerungsauftrags und die Positionenaktualisierungen zu verarbeiten.

1. Gehen Sie zu **Lagerortverwaltung \> Periodische Aufgaben \> Lager-App-Ereignisse verarbeiten**.
1. Das Dialogfeld Lager-App-Ereignisse verarbeiten wird geöffnet. Erweitern Sie das Inforegister **Im Hintergrund ausführen** und setzen Sie **Batchverarbeitung** auf **Ja**.
1. Wählen Sie im Inforegister **Im Hintergrund ausführen** **Serie**.
1. Das Dialogfeld **Serie festlegen** öffnet sich. Legen Sie den passenden Zeitplan für Ihr Unternehmen fest.
1. Wählen Sie **OK**, um zum Dialogfeld **Verarbeiten von Lager-App-Ereignissen** zurückzukehren.
1. Wählen Sie **OK** im Dialogfeld **Lager-App-Ereignisse verarbeiten**, um den Stapelauftrag der Stapelwarteschlange hinzuzufügen.

## <a name="query-warehouse-app-events"></a>Abfrage von Lager-App-Ereignissen

Sie können die Ereigniswarteschlange und die von der Lager-App generierten Ereignismeldungen anzeigen, indem Sie zu **Lagerortverwaltung \> Abfragen und Berichte \> Protokolle für mobile Geräte\> Lager-App-Ereignisse** gehen.

## <a name="the-standard-event-queue-process"></a>Der Standardprozess für Ereigniswarteschlangen

Die Ereigniswarteschlange für Lager-Apps wird normalerweise mit dem folgenden beschriebenen Flow verwendet:

1. Ein Ereignis wird mit einer Ereignismeldung zur Warteschlange hinzugefügt. Die neue Nachricht hat zunächst den Ereignisstatus **Warten**, was bedeutet, dass der Stapelauftrag **Verarbeiten von Lager-App-Ereignissen** diese Nachricht nicht aufnimmt und nicht verarbeitet.
1. Sobald der Nachrichtenstatus auf **In Warteschlange** aktualisiert wird, nimmt der Stapelauftrag **Lager-App-Ereignisse verarbeiten** das Ereignis auf und verarbeitet es.
1. Der Stapelauftrag aktualisiert die Ereigniszustände entweder auf **Abgeschlossen** oder **Fehlgeschlagen**, abhängig davon, ob der angeforderte Prozess möglich war.
1. Wenn alle zugehörigen Ereignismeldungen **Abgeschlossen** sind, wird das Ereignis aus der Warteschlange gelöscht.

 Ein detailliertes Beispiel finden Sie unter [Erstellen eines Umlagerungsauftrags aus der Lager-App-Verarbeiten](create-transfer-order-from-warehouse-app.md).

## <a name="handle-event-errors"></a>Behandeln von Ereignisfehlern

Im Rahmen der Lager-Ereignisverarbeitung empfängt die angeforderte Nachrichtenaktivität möglicherweise keine Prozesse vom Stapelauftrag. In diesem Fall ändert sich die Ereignismeldung in **Fehlgeschlagen**. Sie können die **Stapelverarbeitungsprotokoll**-Informationen verwenden, um zu erfahren, warum und welche Maßnahmen erforderlich sind, um Probleme zu beheben.

Ein detailliertes Beispiel finden Sie unter [Erstellen eines Umlagerungsauftrags aus der Lager-App](create-transfer-order-from-warehouse-app.md).

So setzen Sie eine fehlgeschlagene Lager-App-Ereignismeldung zurück:

1. Gehen Sie zu **Lagerortverwaltung \> Abfragen und Berichte \> Protokolle für mobile Geräte \> Lager-App-Ereignisse**.
1. Auf dem Inforegister **Lager-App-Ereignismeldungen** suchen und wählen Sie ein relevantes Ereignis aus, das **Fehlgeschlagen** in der Spalte **Ereignisstatus** anzeigt.
1. Wählen Sie **Zurücksetzen** auf der Symbolleiste **Lager-App-Ereignismeldungen** .
1. Arbeiten Sie weiter, bis alle relevanten Meldungen zurückgesetzt sind.

Sie können auch eine **Fehlgeschlagen**-Ereignismeldung mit der Option **Löschen** auf der Symbolleiste **Lager-App-Ereignismeldungen** entfernen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]