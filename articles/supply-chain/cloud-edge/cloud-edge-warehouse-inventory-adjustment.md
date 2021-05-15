---
title: Lagerregulierung des Lagerorts
description: Dieses Thema enthält Informationen über die Erfassung und Verarbeitung von Lagerort-Bestandsanpassungen, wenn Sie Scale-Units verwenden.
author: perlynne
manager: tfehr
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSInventoryAdjustmentJournal, InventJournalCount
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: be386539ea7addf20256ac2b1f8a2a72736fcbec
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938225"
---
# <a name="warehouse-inventory-adjustment"></a>Lagerregulierung des Lagerorts

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Die Funktion Lagerbestand-Anpassung wird beim Ausführen von Cloud- und Edge-Scale-Einheiten für [Fertigungs-Workloads](cloud-edge-workload-manufacturing.md) und [Workloads der Lagerortverwaltung](cloud-edge-workload-warehousing.md) verwendet.

enn eine Arbeitskraft eine Bestandsanpassung mit der Lager-App gegen einen Scale-Unit-Workload der Lagerortverwaltung durchführt, muss die physische Bestandsaktualisierung durch den Batch-Auftrag **Lagerort-Bestandsanpassungs-Journal** verarbeitet werden, den Sie unter **Lagerverwaltung > Periodische Aufgaben > Lagerort-Bestandsanpassungs-Journal** ausführen und planen.

Die folgenden Lagerort-App-Arbeitsprozesse verwenden derzeit die **Erfassung von Bestandskorrekturen** bei Scale-Unit Workloads:

- Anpassung ein/aus
- Permanente Inventur
- Ladungsträgerladung

Mehrere Transaktionen bei der Bestandsanpassung werden als Teil von Cloud und Edge erstellt, da die Hub- und Scale-Unit-Einsätze die Datensätze für den Bestand gemeinsam nutzen.

## <a name="inventory-adjustment-example"></a>Beispiel für Bestandsanpassung

In diesem Beispiel hat eine Arbeitskraft im Lagerort die App Lagerort verwendet, um das Hinzufügen von Lagerbestand zu registrieren.

Der Scale-Unit Workload erstellt zunächst eine Lagerort-Bestandsanpassungstransaktion für die positive physische Anpassung, die dann mit dem Hub synchronisiert wird und zu einer Erhöhung des Lagerbestands auf dem Hub führt.

| Typ                                    | Skalierungseinheit | Planungsrichtung | Hub |
|-----------------------------------------|------------|-----------|-----|
| Lagerregulierung des Lagerorts          | +1         | ->        | +1  |

Der Hub verarbeitet dann eine Zähljournalbuchung, die über [Nachrichtenprozessor-Nachrichten](cloud-edge-message-processor-messages.md) empfangen wird. Damit wird der zusätzliche Lagerbestand aktualisiert. Um doppelte Bestände zu vermeiden, erstellt der Hub als Teil dieses Prozesses eine Offset-Transaktion und entfernt den zuvor erfassten Lagerbestand, der sich auf den Lagerort-Bestandsabgleich bezieht.

| Typ                                    | Skalierungseinheit | Planungsrichtung | Hub |
|-----------------------------------------|------------|-----------|-----|
| Inventur                                | +1         | <-        | +1  |
| Lagerort-Bestandsanpassung (Offset) | -1         | <-        | -1  |

Nachdem eine Scale-Unit ein **Abgleichsjournal für den Lagerort** auf dem Hub erstellt hat, können Sie sowohl das **Zähljournal** als auch das **Gegenbuchung** überprüfen, die vom Hub als Teil des Abgleichsprozesses erstellt werden.

Sie können jede dieser Journaleinträge und Transaktionen im Supply Chain Management überprüfen, indem Sie die folgenden Schritte ausführen:

1. Melden Sie sich bei der Scale-Unit an.
1. Gehe zu **Lagerortverwaltung \> Periodische Aufgaben \> Erfassung des Lagerort-Bestandes**.
1. Suchen und öffnen Sie auf der Seite **Lagerort-Bestandsanpassungsjournal** das Journal, das die Änderung des Lagerbestands erfasst hat. Der Bereich **Journalzeilen** zeigt jede Anpassung, die von diesem Journal erfasst wird.
1. Melden Sie sich am Hub an.
1. Gehe zu **Lagerortverwaltung \> Periodische Aufgaben \> Erfassung des Lagerort-Bestandes**.
1. Auf der Seite **Lagerort-Bestandsanpassungsjournal** sollte das gleiche Journal aufgeführt sein, wenn Hub und Scale-Unit synchronisiert wurden.
1. Öffnen Sie die Erfassung. Wenn die [Nachrichten des Nachrichtenverarbeiters](cloud-edge-message-processor-messages.md) verarbeitet wurden, sehen Sie in der Kopfzeile Verknüpfungen zum **Zähljournal** und zur **Gegenbuchung**.
    - Das **Zähljournal** sollte die gleichen Dimensionswerte wie die Journalzeilen aufweisen.
    - Die **Gegenbuchung** sollte den Offset anzeigen, der die doppelte Bestandskorrektur beseitigt.
    > [!NOTE]
    > Wenn alle Synchronisierungen und Verarbeitungen abgeschlossen sind, werden das **Zähljournal** und das **Gegenbuchung** wieder mit der Scale-Unit synchronisiert. Diese können auch auf der entsprechenden Seite **Erfassung der Lagerort-Bestandsanpassung** eingesehen werden.
