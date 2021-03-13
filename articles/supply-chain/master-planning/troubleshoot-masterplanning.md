---
title: Behebung von Problemen bei der Produktprogrammplanung
description: Dieses Thema beschreibt, wie Sie Probleme beheben können, die bei der Arbeit mit der Produktprogrammplanung auftreten können.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 44291f5bcd9ffedf717150f8efe32e9eeda02f2e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011346"
---
# <a name="troubleshoot-master-planning"></a>Fehlerbehebung bei der Produktprogrammplanung

Dieses Thema beschreibt, wie Sie Probleme beheben können, die bei der Arbeit mit der Produktprogrammplanung auftreten können.

## <a name="bill-of-materials-explosion-behaves-differently-for-firmed-production-orders-and-for-estimated-production-orders-for-manually-created-work"></a>Die Stücklistenauflösung verhält sich für umgewandelte Produktionsaufträge und für geschätzte Produktionsaufträge für manuell erstellte Arbeiten unterschiedlich.

### <a name="issue-description"></a>Problembeschreibung

Wenn ein Produktionsauftrag umgewandelt ist, werden die Elemente nicht aufgelöst, wenn Sie die Stückliste auflösen. Wenn Sie jedoch einen Arbeitsauftrag manuell erstellen und dann den Produktionsauftrag schätzen, werden die Elemente aufgelöst.

### <a name="issue-resolution"></a>Problemlösung

Das System arbeitet wie erwartet. Die Auflösung, die erfolgt, wenn der Produktionsauftrag umgewandelt wird, zeigt auf den Planauftrag, aber es scheint nicht so, als ob der Planauftrag in diesem Fall aktuell umgewandelt ist. Wenn der Produktionsauftrag jedoch geschätzt wurde, wird die Auflösung vom freigegebenen Produktionsauftrag ausgelöst, wenn kein Planauftrag vorhanden ist.

## <a name="the-delay-value-isnt-updated-when-i-reschedule-a-planned-order"></a>Der Wert Verzögerung wird nicht aktualisiert, wenn ich einen Planauftrag neu terminiere.

Um die Verzögerung für Planaufträge zu aktualisieren, öffnen Sie das Dialogfeld **Umplanung** für den Planauftrag. Stellen Sie auf dem Inforegister **Auflösung** sicher, dass die Option **Auflösung nach Neuterminierung durchführen** auf *Ja* festgelegt ist.

## <a name="production-scheduling-doesnt-consider-the-safety-margins-that-are-set-on-the-item-coverage-for-pegged-supply"></a>Die Produktionsplanung berücksichtigt nicht die Sicherheitsmargen, die in der Elementabdeckung für Bedarfsverursacher festgelegt sind.

### <a name="issue-description"></a>Problembeschreibung

Die Produktprogrammplanung berücksichtigt die Sicherheitsabstände. Bei der Terminierung von geplanten Produktionsaufträgen werden die Sicherheitsmargen jedoch ignoriert.

### <a name="issue-resolution"></a>Problemlösung

Ränder werden nur bei der Produktprogrammplanung berücksichtigt, nicht bei der manuellen Terminierung. Die Sicherheitsmargen sind als Puffer während der Planungsphase gedacht, um einen gewissen „Spielraum“ für den tatsächlichen Prozess zu haben.

Um das gewünschte Ergebnis zu erhalten, können Sie die Marge entfernen. Der Arbeitsplan muss dann so aktualisiert werden, dass er die gewünschte Zeit enthält (z. B. als Warteschlangenzeit). Sowohl die Produktprogrammplanung als auch die manuelle Terminierung sollten dann das gleiche Ergebnis liefern.

## <a name="planned-orders-are-generated-even-though-we-have-items-in-stock-and-production-orders-already-exist-for-them"></a>Planaufträge werden generiert, obwohl wir Elemente auf Lager haben und bereits Produktionsaufträge für sie existieren.

Sie können dieses Problem möglicherweise beheben, indem Sie den Wert **Positive Tage** für die betreffenden Gruppen auf der Seite **Deckungsgruppe** erhöhen. Diese Änderung bewirkt, dass das System ermittelt, ob der vorhandene Bestand für den Bedarf verwendet werden kann. Dann wird für die Elemente, die auf Lager sind, kein neuer Planauftrag generiert.

## <a name="master-planning-doesnt-seem-to-respect-capacity-limitations-and-is-scheduling-more-than-the-available-capacity"></a>Die Produktprogrammplanung scheint Kapazitätsbeschränkungen nicht zu respektieren und terminiert mehr als die verfügbare Kapazität.

### <a name="issue-description"></a>Problembeschreibung

Wenn Sie eine Vorgangsterminierung verwenden, bei der es eine endliche Kapazität gibt und der Arbeitsplan eine Mischung aus Bedarfen sowohl für eine Ressourcengruppe als auch für einzelne Ressourcen angibt, besteht eine kleine Chance auf Überbuchung aufgrund der Art und Weise, wie der Algorithmus auf Kapazitätskonflikte prüft. Diese Überbuchung kann auftreten, wenn Sie Helfer zur Ausführung der Produktprogrammplanung verwenden. Sie tritt am ehesten auf, wenn es viele Aufträge gibt, die eine relativ kurze Laufzeit haben.

### <a name="issue-resolution"></a>Problemlösung

Wenn es wichtig ist, dass bei der Vorgangsterminierung keine Überbuchung auftritt, können Sie den Terminierungsteil der Produktprogrammplanung single-threaded machen, indem Sie die Option **Genaue endliche Kapazität für Vorgangsterminierung** auf der Seite **Parameter der Produktprogrammplanung** aktivieren. Diese Option ist standardmäßig nicht verfügbar. Sie müssen sie manuell auf der Seite hinzufügen, indem Sie die Funktionen zur Personalisierung verwenden. Wenn Sie diese Option verwenden, läuft die Planung aufgrund der fehlenden Parallelverarbeitung langsamer.

## <a name="planned-orders-take-a-long-time-to-update"></a>Die Aktualisierung geplanter Aufträge nimmt viel Zeit in Anspruch.

### <a name="issue-description"></a>Problembeschreibung

Wenn Sie die Bedarfsmenge und/oder das Lieferdatum eines Planauftrags aktualisieren, dauert es normalerweise mindestens 30 Sekunden pro Auftrag, bis die Aktualisierung gespeichert ist.

### <a name="issue-resolution"></a>Problemlösung

Dies ist ein bekanntes Problem mit der integrierten Produktprogrammplanung. Es wird durch die zugrundeliegende Autoauflösung durch die Stücklisten-Struktur während der Bearbeitungen verursacht. Dieses Problem wird in der Planungsoptimierung behoben, wo ein Planer die relevanten Aufträge aktualisieren und genehmigen kann und, wenn gewünscht, einen Planungslauf auslöst, um die Planaufträge für die zugrunde liegende Stückliste zu aktualisieren.

Eine Möglichkeit, die Leistung mit der eingebauten Produktprogrammplanung zu verbessern, ist Folgendes:

1. Wechseln Sie zu **Produktprogrammplanung \> Einrichtung \> Pläne \> Produktprogrammpläne**.
1. Wählen Sie einen Plan aus.
1. Erweitern Sie das Inforegister **Zeitfenster in Tagen**.
1. Legen Sie **Auflösung** auf *Ja* fest und setzen Sie das Feld unterhalb dieser Einstellung auf 0 (Null).

> [!NOTE]
> Dadurch wird der Zeitraum für Auflösungen, die für diesen Masterplan durchgeführt werden, auf einen Tag begrenzt.
