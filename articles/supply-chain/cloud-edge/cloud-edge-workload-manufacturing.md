---
title: Arbeitsauslastungen bei der Fertigungsausführung für Cloud- und Edge-Scale-Einheiten
description: Dieses Thema beschreibt, wie Arbeitsauslastungen für die Fertigungsausführung mit Cloud- und Edge Scale-Units funktionieren.
author: johanhoffmann
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: johanho
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: b30e16489b0b0169f08e52c70cf4489c9bf4ce1b
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8674053"
---
# <a name="manufacturing-execution-workloads-for-cloud-and-edge-scale-units"></a>Workloads in der Fertigungsausführung für Cloud- und Edge-Skalierungseinheiten

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> Der Manufacturing Execution Workload ist derzeit nur in der Vorschau verfügbar.
>
> Einige Geschäftsfunktionen werden in der öffentlichen Vorschau nicht vollständig unterstützt, wenn Arbeitsauslastungen mit Scale-Units verwendet werden.
>
> Sie können den Preview Manufacturing Execution Workload nicht auf einer Scale-Unit ausführen, auf der auch der Warehouse Execution Workload installiert ist.

Bei der Ausführung der Fertigung bieten Skalierungseinheiten die folgenden Funktionen:

- Maschinenbediener und Werkstattleiter können auf den operativen Produktionsplan zugreifen.
- Maschinenbediener können den Plan auf dem neuesten Stand halten, indem sie diskrete und Prozessfertigungsaufträge ausführen.
- Der Fertigungsleiter kann den Betriebsplan anpassen.
- Die Arbeiter können auf die Zeiterfassung zugreifen, um die korrekte Berechnung der Löhne sicherzustellen.

Dieses Thema beschreibt, wie Arbeitsauslastungen für die Fertigungsausführung mit Cloud- und Edge Scale-Units funktionieren.

## <a name="the-manufacturing-lifecycle"></a>Der Fertigungslebenszyklus

Wie die folgende Abbildung zeigt, ist der Fertigungslebenszyklus in drei Phasen unterteilt: *Planen*, *Ausführen* und *Fertigstellen*.

[![Phasen der Fertigungsausführung bei Verwendung einer einzigen Umgebung](media/mes-phases.png "Phasen der Fertigungsausführung bei Verwendung einer einzigen Umgebung.")](media/mes-phases-large.png)

Die Phase _Planen_ umfasst Produktdefinition, Planung, Auftragserstellung und -terminierung sowie Freigabe. Der Freigabeschritt kennzeichnet den Übergang von der Phase _Planen_ zur Phase _Ausführen_. Wenn ein Produktionsauftrag freigegeben wird, sind die Produktionsaufträge auf der Produktionsfläche sichtbar und bereit zur Ausführung.

Wenn ein Produktionsauftrag als abgeschlossen markiert wird, wechselt er von der Phase _Ausführen_ in die Phase _Finalisieren_. In der Phase _Finalisieren_ durchlaufen die Registrierungen aus der Phase *Ausführen* einen Workflow zur Genehmigung, wo sie berechnet, genehmigt und übertragen werden. An diesem Punkt ist der Produktionsauftrag abgeschlossen. Damit ist die Grundlage für die Entlohnung der Arbeitskräfte geschaffen.

## <a name="splitting-the-execute-phase-into-a-separate-workload"></a>Aufteilung der Phase „Ausführen“ in eine separate Arbeitsauslastung

Wie die folgende Abbildung zeigt, wird bei Verwendung von Scale-Units die Phase _Ausführen_ als separate Arbeitsauslastung aufgeteilt.

[![Ausführungsphasen, wenn Scale-Units verwendet werden](media/mes-phases-workloads.png "Fertigungsausführungsphasen bei Verwendung von Scale-Units.")](media/mes-phases-workloads-large.png)

Das Modell geht nun von einer Einzelinstanz-Installation zu einem Modell über, das auf dem Hub und Scale-Units basiert. Die Phasen _Planen_ und _Finalisieren_ laufen als Back-Office-Operationen auf dem Hub, und die Arbeitsauslastung der Fertigungsausführung läuft auf den Scale-Units. Die Daten werden asynchron zwischen dem Hub und den Scale-Units übertragen.

Wenn ein Produktionsauftrag auf dem Hub freigegeben wird, werden alle Daten, die zur Verarbeitung von Produktionsaufträgen erforderlich sind, an die Scale-Unit übertragen. Zu diesen Daten gehören Produktionsaufträge, Arbeitspläne, Stücklisten und Produkte. Daten, die sich nicht auf einen Produktionsauftrag beziehen (z. B. indirekte Aktivitäten, Abwesenheitscodes und Produktionsparameter), werden ebenfalls vom Hub an die Scale-Unit übertragen. In der Regel können Daten, die aus dem Hub stammen und an die Scale-Unit übertragen werden, nur im Hub erstellt oder aktualisiert werden. Zum Beispiel kann ein neuer Abwesenheitscode oder eine indirekte Aktivität nicht auf der Scale-Unit erstellt werden – sie können nur für die Registrierung verwendet werden. Die Registrierungen, die während der Ausführung auf der Scale-Unit vorgenommen werden, werden dann an den Hub übertragen, wo die Zeit- und Anwesenheitsgenehmigung, der Bestand und die finanziellen Aktualisierungen verarbeitet werden.

## <a name="manufacturing-execution-tasks-that-can-be-run-on-workloads"></a>Manufacturing Execution Tasks, die auf Arbeitsauslastungen ausgeführt werden können

Die folgenden Manufacturing Execution Tasks können derzeit auf Arbeitsauslastungen ausgeführt werden, wenn Scale-Units verwendet werden:

- Einbuchung, Anmeldung, Ausbuchung und Abwesenheit
- Einzelvorgang starten
- Aufträge bündeln
- Fortschritt melden
- Ausschuss melden
- Indirekte Aktivität
- Pause
- Fertig melden und einlagern (erfordert, dass Sie auch den Workload für die Lagerausführung auf Ihrer Skalierungseinheit ausführen, siehe auch [Fertig melden und auf einer Skalierungseinheit einlagern](#RAF))

## <a name="working-with-manufacturing-execution-workloads-on-the-hub"></a>Arbeiten mit Arbeitsauslastungen zur Fertigungsausführung auf dem Hub

Normalerweise laufen die Prozesse, die für die Ausführung von Arbeitsauslastungen in der Fertigungsausführung erforderlich sind, automatisch, um den Hub und alle Scale-Units bei Bedarf synchron zu halten. Wenn Sie jedoch Probleme haben, können Sie die Verarbeitung von Rohregistrierungen, die von Arbeitsauslastungen empfangen werden, manuell auslösen und/oder das Protokoll der Registrierungsverarbeitung überprüfen.

### <a name="manually-process-raw-registrations"></a>Manuelles Verarbeiten von Rohregistrierungen

Ein Batch-Job im Supply Chain Management läuft automatisch, um alle Registrierungen zu verarbeiten, die von den Arbeitsauslastungen empfangen wurden. Dieser Job erstellt die erforderlichen Produktionserfassungen und Logbucheinträge, wenn eine Registrierung für einen abgeschlossenen Auftrag in der Arbeitsauslastung verarbeitet wird.

Obwohl der Job normalerweise automatisch läuft, können Sie ihn jederzeit manuell ausführen, indem Sie sich am Hub anmelden und zu **Produktionssteuerung \> Periodische Aufgaben \> Backoffice-Arbeitsauslastung \> Rohregistrierungen verarbeiten** gehen.

### <a name="check-the-raw-registration-processing-log"></a>Prüfen Sie das Verarbeitungsprotokoll für Rohregistrierungen

Um das Protokoll der Registrierungsverarbeitung zu überprüfen, melden Sie sich beim Hub an und gehen Sie zu **Produktionssteuerung \> Periodische Aufgaben \> Backoffice Arbeitsauslastung \> Rohregistrierungsverarbeitungsprotokoll**. Die Seite **Rohregistrierungs-Verarbeitungsprotokoll** zeigt eine Liste der verarbeiteten Rohregistrierungen und den Status der einzelnen Registrierungen.

![Rohregistrierungs-Verarbeitungsprotokoll-Seite.](media/mes-processing-log.png "Rohregistrierungs-Verarbeitungsprotokollseite")

Sie können jede Registrierung in der Liste bearbeiten, indem Sie sie auswählen und dann eine der folgenden Schaltflächen im Aktivitätsbereich wählen:

- **Bearbeiten** - Manuelles Bearbeiten der ausgewählten Registrierung. Diese Aktion kann nützlich sein, wenn der Job _Rohregistrierungen verarbeiten_ nicht gelaufen ist oder fehlgeschlagen ist.
- **Abbrechen** - Bricht die ausgewählte Registrierung ab.

## <a name="working-with-manufacturing-execution-workloads-on-a-scale-unit"></a>Arbeiten mit Arbeitsauslastungen der Fertigungsausführung auf einer Scale-Unit

Normalerweise laufen die Prozesse, die für die Ausführung von Arbeitsauslastungen in der Fertigungsausführung erforderlich sind, automatisch, um den Hub und alle Scale-Units bei Bedarf synchron zu halten. Wenn Sie jedoch Probleme haben, können Sie den Verlauf der Aufträge prüfen, die auf einer Scale-Unit verarbeitet wurden, oder den Auftrag _Manufacturing Hub to Scale-Unit message processor_ manuell ausführen.

### <a name="view-the-history-of-manufacturing-jobs-that-have-been-processed-on-a-scale-unit"></a>Prüfen der Historie von Fertigungsaufträgen, die auf einer Scale-Unit verarbeitet wurden

Um die Historie der Fertigungsaufträge einzusehen, die auf einer Scale-Unit verarbeitet wurden, melden Sie sich an der Scale-Unit-Maschine an und gehen Sie zu **Produktionssteuerung \> Periodische Aufgaben \> Backoffice-Arbeitsauslastung \> Historie der Verarbeitung von Fertigungsaufträgen**. Die Seite **Verarbeitungshistorie von Fertigungsaufträgen** zeigt die Verarbeitungshistorie der Produktionsaufträge auf der Scale-Unit. Sie können jeden Produktionsauftrag in der Liste bearbeiten, indem Sie ihn auswählen und dann eine der folgenden Schaltflächen im Aktivitätsbereich wählen:

- **Bearbeiten** - Den ausgewählten Produktionsauftrag manuell bearbeiten.
- **Abbrechen** - Den ausgewählten Produktionsauftrag abbrechen.

### <a name="manufacturing-hub-to-scale-unit-message-processor-job"></a>Fertigungs-Hub zu Scale-Unit Nachrichtenprozessorauftrag

Der Job _Manufacturing hub to scale unit message processor_ verarbeitet Daten vom Hub zur Scale-Unit. Dieser Job wird automatisch gestartet, wenn die Arbeitsauslastung der Fertigungsausführung bereitgestellt wird. Sie können ihn jedoch jederzeit manuell ausführen, indem Sie zu **Produktionssteuerung \> Periodische Aufgaben \> Backoffice-Arbeitsauslastung \> Manufacturing Hub to Scale-Unit Message Processor** gehen.

<a name="RAF"></a>

## <a name="report-as-finished-and-putaway-on-a-scale-unit"></a>Fertig melden und auf einer Skalierungseinheit einlagern

<!-- KFM: 
This section describes how to enable the abilities to report as finished and then putaway finished items when you are using to a scale unit.

### Enable and use report as finished and putaway on a scale unit -->

Im aktuellen Release werden Vorgänge zum Fertig melden und einlagern (für Fertig-, Co- und Nebenprodukte) vom [Workload für die Lagerausführung](cloud-edge-workload-warehousing.md) unterstützt (nicht der Workload für die Fertigungsausführung). Um diese Funktionalität bei der Verbindung mit einer Skalierungseinheit zu verwenden, müssen Sie daher Folgendes tun:

- Installieren Sie sowohl den Workload für die Lagerausführungs als auch für die Fertigungsausführung auf Ihrer Skalierungseinheit.
- Verwenden Sie die Mobile Warehouse Management-App, um den Abschluss zu melden und die Einlagerungsarbeiten zu verarbeiten. Die Produktionsausführungsoberfläche unterstützt diese Prozesse derzeit nicht.

<!-- KFM: API details needed

### Customize report as finished and putaway functionality

 -->

## <a name="enable-and-use-the-start-operation-on-a-scale-unit"></a>Aktivieren und verwenden Sie den Vorgang „Start“ für eine Scale-Unit.

In der aktuellen Version wird der Startvorgang für Produktions- und Batch-Aufträge vom [Warehouse Execution Workload](cloud-edge-workload-warehousing.md) unterstützt (nicht vom Manufacturing Execution Workload). Um diese Funktionalität zu nutzen, wenn Sie mit einer Scale-Unit verbunden sind, müssen Sie daher diese Aufgaben erledigen:

- Installieren Sie sowohl den Workload für die Lagerausführungs als auch für die Fertigungsausführung auf Ihrer Skalierungseinheit.
- Aktivieren Sie die Funktion *Produktionsauftrag auf dem Workload der Lagerverwaltung für die Scale-Unit-Manager der Cloud und des Edge* in [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
- Verwenden Sie die Warehouse Management Mobile-App, um die Produktion oder den Batch-Auftrag zu starten.

## <a name="enable-and-use-material-consumption-on-a-scale-unit"></a>Materialverbrauch für eine Scale-Unit aktivieren und verwenden

In der aktuellen Version wird der Flow in der Warehouse Management Mobile-App für die Registrierung des Materialverbrauchs vom [Workload Lagerausführung](cloud-edge-workload-warehousing.md) (nicht vom Workload Fertigungsausführung) unterstützt. Um diese Funktionalität zu nutzen, wenn Sie mit einer Scale-Unit verbunden sind, müssen Sie daher diese Aufgaben erledigen:

- Installieren Sie sowohl den Workload für die Lagerausführungs als auch für die Fertigungsausführung auf Ihrer Skalierungseinheit.
- Aktivieren Sie die Funktion *Materialverbrauch in der Mobile-App für eine Scale-Unit* in der [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
- Verwenden Sie die Warehouse Management Mobile-App, um den Materialverbrauch zu registrieren.

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
