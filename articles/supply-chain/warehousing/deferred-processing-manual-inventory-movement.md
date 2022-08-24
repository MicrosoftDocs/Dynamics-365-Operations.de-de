---
title: Aufgeschobene Verarbeitung von manuellen Bestandsbewegungen
description: Dieser Artikel beschreibt, wie Sie die verzögerte Verarbeitung von manuellen Bestandsbewegungen in Microsoft Dynamics 365 Supply Chain Management verwenden können.
author: Mirzaab
ms.date: 04/27/2021
ms.topic: article
ms.search.form: WHSWorkProcessingPolicy, WHSWorkDeferredPutProcessingTask
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-04-27
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 4a8dd322446843af41214e8daa0822939d0468f0
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/02/2022
ms.locfileid: "9219807"
---
# <a name="deferred-processing-of-manual-inventory-movement"></a>Aufgeschobene Verarbeitung von manuellen Bestandsbewegungen

[!include [banner](../includes/banner.md)]

Dieser Artikel beschreibt, wie Sie die verzögerte Verarbeitung von manuellen Bestandsbewegungen in Microsoft Dynamics 365 Supply Chain Management verwenden können.

Durch die verzögerte Verarbeitung können die Arbeitskräfte am Lagerort weiterhin andere Arbeiten erledigen, während ein PUT-Vorgang im Hintergrund verarbeitet wird. Die aufgeschobene Verarbeitung ist nützlich, wenn es auf dem Server zu gelegentlichen oder ungeplanten Erhöhungen der Verarbeitungszeit kommen kann und die erhöhte Verarbeitungszeit die Produktivität der Arbeitskräfte beeinträchtigen könnte. Der Arbeitstyp *Bestandsbewegung* wurde jetzt auf den Satz von Arbeitstypen, die diese Funktion unterstützt, festgelegt.

Die Verarbeitung im Hintergrund wird durch die Funktion [Verarbeiten von Lagerort App Ereignissen](warehouse-app-events.md) erreicht.

## <a name="turn-on-this-feature-for-your-system"></a>Schalten Sie diese Funktion für Ihr System ein

Um diese Funktion verfügbar zu machen, schalten Sie die folgenden Funktionen in der [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ein. Sie müssen sie in dieser Reihenfolge einschalten:

1. *Organisationsweite Arbeitssperrung*<br>(Ab Supply Chain Management Version 10.0.21 ist diese Funktion obligatorisch, daher ist sie standardmäßig aktiviert und kann nicht wieder deaktiviert werden.)
1. *Lagerort-App-Ereignisse verarbeiten*<br>(Ab Supply Chain Management Version 10.0.25 ist diese Funktion standardmäßig aktiviert. Ab Supply Chain Management Version 10.0.29 ist diese Funktion obligatorisch. Daher ist es standardmäßig aktiviert und kann nicht wieder deaktiviert werden.)
1. *Verzögerte Put-Vorgänge*
1. *Verzögerte Verarbeitung des manuellen Bestandsumlagerungsvorgangs*<br>(Ab Supply Chain Management Version 10.0.25 ist diese Funktion obligatorisch, daher ist sie standardmäßig aktiviert und kann nicht wieder deaktiviert werden.)

## <a name="configure-the-work-processing-policies"></a>Konfigurieren Sie die Richtlinien für die Verarbeitung von Arbeit

Um die aufgeschobene Verarbeitung zu verwenden, müssen Sie eine Richtlinie für die Arbeitsverarbeitung festlegen und verwenden. Für die aufgeschobene Put-Verarbeitung unterstützt die Funktion [Aufgeschobene Verarbeitung von Lagerortarbeit](deferred-put.md) die folgenden Arbeitstypen: *Verkaufsauftrag*, *Umlagerungsauftragsausgabe* und *Wiederbeschaffung*. Die Funktion *Aufgeschobene Verarbeitung von manuellen Vorgängen der Bestandsbewegung* fügt einen neuen Arbeitstyp hinzu: *Inventarbewegung*.

Um eine Richtlinie zur Verarbeitung von Arbeit festzulegen, befolgen Sie diese Schritte.

1. Wechseln Sie zu **Lagerverwaltung \> Einrichten \> Arbeit \> Richtlinien für die Verarbeitung von Arbeit**.
1. Wählen Sie entweder eine vorhandene Richtlinie in der Liste aus oder erstellen Sie eine neue Richtlinie, indem Sie **Neu** im Aktivitätsbereich wählen. Der Kopf jeder Richtlinie hat die folgenden Felder:

    - **Name der Richtlinie zur Verarbeitung von Arbeit** – Der Name der Richtlinie zur Verarbeitung von Arbeit.
    - **Beschreibung** – Eine Beschreibung der Richtlinie für die Verarbeitung von Arbeit.

1. Legen Sie auf dem Inforegister **Verarbeitungsregeln** die Sammlung von Regeln fest, die die Richtlinie anwenden soll. Verwenden Sie die Schaltflächen in der Symbolleiste, um Regeln nach Bedarf hinzuzufügen oder zu entfernen. Legen Sie für jede Regel die folgenden Felder fest:

    - **Arbeitsauftragstyp** – Wählen Sie den Arbeitsauftragstyp, für den die Richtlinie gilt.
    - **Vorgang** – Wählen Sie den Vorgang aus, der mit der Richtlinie verarbeitet wird. Wenn Sie *Bestandsbewegung* im Feld **Arbeitsauftragstyp** gewählt haben, müssen Sie dieses Feld nicht festlegen, da sowohl Entnahme- als auch Einlegevorgänge als ein Ereignis verarbeitet werden.
    - **Arbeitsverarbeitungsmethode** – Wählen Sie die Methode, mit der die Zeile verarbeitet wird. Wenn Sie *Sofort* wählen, ähnelt das Verhalten dem Verhalten, wenn keine Richtlinien zur Verarbeitung der Zeile verwendet werden. Wenn Sie *Aufgeschoben* wählen, wendet das System eine aufgeschobene Verarbeitung an, die den Batch-Rahmen verwendet.
    - **Schwellenwert für aufgeschobene Verarbeitung** – Wenn Sie dieses Feld auf *0* (Null) festlegen, gibt es keinen Schwellenwert. In diesem Fall wird, wenn möglich, die Verarbeitungsmethode *Aufgeschoben* verwendet. Wenn die spezifische Schwellenwertberechnung unter dem Schwellenwert liegt, wird die Methode *Immediate* verwendet. Andernfalls wird, wenn möglich, die Methode *Aufgeschoben* verwendet. Bei verkaufs- und übertragungsbezogenen Arbeiten wird der Schwellenwert als die Zahl zugeordneter Quellladungspositionen berechnet, die für die Arbeit verarbeitet werden. Für wird der Wiederbeschaffungsarbeiten wird der Schwellenwert als die Anzahl von Arbeitspositionen berechnet, die wiederbeschafft werden. Indem Sie einen Schwellenwert von z.B. *5* für Verkäufe festlegen, stellen Sie sicher, dass kleinere Werke, die weniger als fünf Zeilen für die initiale Quell-Ladung haben, die verzögerte Verarbeitung nicht nutzen, größere Werke aber schon. Der Schwellenwert wirkt sich nur aus, wenn das Feld **Verarbeitungsmethode** auf *Aufgeschoben* festgelegt ist.
    - **Aufgeschobene Verarbeitung Batch-Gruppe** – Geben Sie die Batch-Gruppe an, die für die Verarbeitung verwendet wird. Wenn Sie *Bestandsbewegung* im Feld **Arbeitsauftragstyp** gewählt haben, müssen Sie dieses Feld nicht festlegen, weil die Batch-Gruppe in der Dialogbox **Verarbeiten von Lagerort App-Ereignissen** ausgewählt ist.

## <a name="assign-the-work-creation-policy"></a>Weisen Sie die Richtlinie für die Arbeitserstellung zu

Details zum Zuweisen einer Richtlinie für die Arbeitserstellung finden Sie unter [Aufgeschobene Verarbeitung von Lagerortarbeit](deferred-put.md).

## <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a>Richten Sie einen Stapelauftrag ein, um Lager-App-Ereignisse zu verarbeiten

Um den Prozess *Aufgeschobene Verarbeitung des manuellen Vorgangs der Bestandsbewegung* zu verwenden, legen Sie einen geplanten Batch-Auftrag fest.

1. Gehen Sie zu **Lagerortverwaltung \> Periodische Aufgaben \> Lager-App-Ereignisse verarbeiten**.
1. Legen Sie im Dialogfeld **Ereignisse der Lagerort App verarbeiten** auf der Registerkarte **Im Hintergrund ausführen** die Option **Batch-Verarbeitung** auf *Ja* fest.
1. Wählen Sie **Wiederholung**, und legen Sie einen Ausführungsplan fest, der den Anforderungen Ihres Unternehmens entspricht.
1. Wählen Sie in jedem Dialogfeld **OK**.

## <a name="inquire-about-the-warehouse-app-events"></a>Erkundigen Sie sich nach den Ereignissen der Lagerort-App

Sie können die Ereignis-Warteschlange und die Nachrichten, die die Lagerort-App erzeugt, unter **Lagerortverwaltung \> Abfragen und Berichte \> Mobile-Geräte-Protokolle \> Ereignisse der Lagerort-App** einsehen.

Die *Bestandsbewegung* Nachrichten für Ereignisse haben den Status *Warteschlange*, wenn sie erstmals erstellt werden. Dieser Status zeigt an, dass der Batchauftrag **Warehouse-App-Ereignisse verarbeiten** die Nachrichten der Ereignisse entnimmt und verarbeitet. Wenn der Status auf *Erledigt* aktualisiert wird, werden alle zugehörigen Ereignisse aus der Warteschlange gelöscht.

Alle *Bestandsbewegungen* Ereignisse werden unter einer Sammlung pro Ereignistyp und Lagerort zusammengefasst.

Der Batchauftrag verarbeitet die Lagerort-App-Ereignisse entsprechend der Wiederholung, die im Dialogfeld **Lagerort-App-Ereignisse verarbeiten** festgelegt ist. Solange eine Nachricht nicht verarbeitet ist, können Sie daher die Lagerort-ID im Feld **Bezeichner** nachsehen.

Die Details der Nachricht enthalten die Angaben zur Bewegung (z. B. die Lagerplätze „von“ und „nach“).

Weitere Informationen finden Sie unter [Verarbeitung von Lagerort-App-Ereignissen](warehouse-app-events.md).

## <a name="configure-the-mobile-device-menu-to-skip-the-deferred-processing-policy"></a>Konfigurieren Sie das Menü für mobile Geräte, um die Richtlinie für die verzögerte Verarbeitung zu überspringen

Details darüber, wie Sie das Menü des mobilen Geräts so konfigurieren, dass die Richtlinie für die verzögerte Verarbeitung übersprungen wird, finden Sie unter [Verzögerte Verarbeitung von Lagerortarbeit](deferred-put.md).

## <a name="impact-on-closed-work-dates"></a>Auswirkungen auf abgeschlossene Arbeitstermine

Details zu den Auswirkungen auf abgeschlossene Arbeitstermine finden Sie unter [Aufgeschobene Verarbeitung von Lagerortarbeit](deferred-put.md).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Verzögerte Verarbeitung der Lagerarbeit](deferred-put.md)
- [Verarbeitung von Ereignissen der Lagerort-App](warehouse-app-events.md)
- [Mobile Geräte für Lagerarbeiten einrichten](configure-mobile-devices-warehouse.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
