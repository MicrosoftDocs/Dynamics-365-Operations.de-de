---
title: Wellenvorlagen
description: In diesem Thema wird beschrieben, wie die Kriterien eingerichtet werden, die bestimmen, ob Wellen manuell oder automatisch verarbeitet werden, und die Arbeit, die für einen Lagerort generiert wird, wenn eine Welle verarbeitet wird.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: aca03e3fda4405fa6fe2b427a47066af5bb95b644b7f5b47d22736347208a8bd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6751624"
---
# <a name="wave-templates"></a>Wellenvorlagen

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie die Kriterien eingerichtet werden, die bestimmen, ob Wellen manuell oder automatisch verarbeitet werden, und die Arbeit, die für einen Lagerort generiert wird, wenn eine Welle verarbeitet wird. Sie geben die Kriterien an, indem Sie Wellenvorlagen und Abfragen einrichten, die mit einer Welle mit freigegebenen Positionen in Aufträgen, Produktionsaufträgen und in Kanbans übereinstimmen.

## <a name="settings-for-wave-templates"></a>Einstellungen für Wellenvorlagen

Wenn Sie eine Wellenvorlage einrichten, geben Sie Folgendes an:

- Der **Standort** und der **Lagerort**, für die die Vorlage Arbeit erstellt.
- Die Reihenfolge, in der die Vorlagen ausgewertet werden. Die Reihenfolge, in der die Vorlagen freigegebenen Positionen in Aufträgen, Produktionsaufträgen und Kanbans zugeordnet werden. Wenn eine Position freigegeben wird, wendet das System die erste Wellenvorlage an, deren Kriterien die Position erfüllt. Je weiter die Kriterien gefasst sind, desto wahrscheinlicher ist es, dass eine Position die Kriterien erfüllt. Daher sollten Sie die Vorlagen mit den spezifischsten Kriterien ganz oben auf die Liste setzen. Verwenden Sie die Schaltflächen **Nach oben** und **Nach unten** im Aktivitätsbereich, um die Vorlagen in der Liste zu ordnen.
- Die von jeder Vorlage ausgeführten Aktivitäten. Die **Methoden** der Welle, die die Aktivitäten ausführen, die von ausgewählten Vorlage erstellt werden, wie Erstellen oder Verteilen von Arbeit für jeden Typ von Wellenvorlage.
- Die Wellenattribute (Filter), die für die Verwendung der Wellenvorlage gelten müssen.

> [!NOTE]
> Bei Bedarf kann ein Entwickler zusätzliche Methoden erstellen. Sie können die vollständige Liste der Methoden auf der Seite **Wellenverarbeitungsmethoden** einsehen.

Einige Einstellungen stellen strategische Entscheidungen für die Wellenverarbeitung dar, wie folgt:

- Wenn die Vorlage für den Versand von Artikeln für Aufträge und Umlagerungsaufträge verwendet wird oder zum Bewegen von Artikeln für Produktion für Produktionsaufträge oder Kanbans.
- Wenn eine Welle manuell oder automatisch verarbeitet wird, wie folgt:

  - **Manuelle Verarbeitung** – Die Position wird einer Welle hinzugefügt und der Bestand wird reserviert, Sie müssen jedoch auf **Prozess** auf der Listenseite **Alle Wellen** klicken, um die Entnahmearbeit für den Auftrag zu erstellen.
  - **Automatische Verarbeitung** – Sie können die Wellenverarbeitung vollständig oder teilweise automatisieren. Wenn Sie die Wellenverarbeitung vollständig automatisieren, wird eine Welle erstellt, die die Position aus dem Auftrag, dem Produktionsauftrag oder dem Kanban umfasst, wenn ein Auftrag, ein Produktionsauftrag oder ein Kanban erstellt wird. Die Artikel werden vom verfügbaren Bestand abgezogen und die Entnahmearbeit wird erstellt. Wenn Sie die Wellenverarbeitung teilweise automatisieren, können Sie Werte angeben, die eine Wellenverarbeitung auslösen. So können Sie ein Höchstgewicht für Lieferungen festlegen, das die Wellenverarbeitung auslöst, wenn das Gesamtgewicht der Positionen in der Welle den Wert erreicht.

- Wenn Sie Lieferungen einer offenen Welle zuweisen. Wenn Sie beispielsweise Debitoren zusichern, dass ein Auftrag, der bis 12:00 Uhr aufgeben wird, innerhalb von 24 Stunden geliefert wird, können Sie die Wellenvorlage einrichten, um Auftragspositionen einer offenen Welle bis 12:00 Uhr zuzuordnen. Zu dieser Zeitpunkt wird die Welle automatisch verarbeitet.

Wenn eine Welle verarbeitet wird, basiert die Entnahmearbeit, die erstellt wird, auf der Arbeitsvorlage und der Lagerplatzrichtlinie, die für den Lagerort angegeben ist. Die Arbeitsvorlage gibt an, wie die Entnahmearbeit erstellt wird, und die Lagerplatzrichtlinie gibt die Entnahme- und Einlagerungs-Lagerorte an.

## <a name="create-a-wave-template"></a>Eine Wellenvorlage erstellen

Gehen Sie zum Einrichten einer Wellenvorlage folgendermaßen vor:

1. Wechseln Sie zu **Lagerortverwaltung** \> **Einstellungen** \> **Wellen** \> **Wellenvorlagen**.
1. Wählen Sie **Neu** aus, um eine neue Wellenvorlage zu erstellen.
1. Wählen Sie im Feld **Wellenvorlagentyp** eine der folgenden Optionen aus:

    - *Versand* – Verwenden Sie die Wellenvorlage für das Versenden von Artikeln für Aufträge und Umlagerungsaufträge.
    - *Produktionsaufträge* – Verwenden Sie die Wellenvorlage, um Artikel für Produktionsaufträge zu verschieben.
    - *Kanban* – Verwenden Sie die Wellenvorlage, um Artikel für Kanban-Aufträge zu verschieben.

1. Geben Sie in den Feldern **Wellenvorlagenname** und **Wellenvorlagenbeschreibung** einen Namen und eine Beschreibung für die Wellenvorlage ein.

    > [!NOTE]
    > Wenn mehr als eine Vorlage für einen Lagerort erstellt wird, gibt die Zahl im Feld **Wellenvorlagenreihenfolge** die Position der Vorlage in der Reihenfolge an, in der die Vorlagen angewendet werden, wenn die Kriterien der Vorlage erfüllt sind. Sie können die Reihenfolge der Vorlagen mit **Nach oben** oder **Nach unten** neu ordnen.

1. Wählen Sie die Felder **Standort** und **Lagerort** aus, wählen Sie den Standort und den Lagerort aus, für die die Wellenvorlage Wellen und Entnahmearbeit erstellt.
1. Wenn Sie die Wellenverarbeitung automatisieren möchten, nehmen Sie nach Bedarf die folgenden Einstellungen vor:

    - **Wellenerstellung automatisieren** – Setzen Sie diese Option auf *Ja*, um eine Welle automatisch zu erstellen, wenn ein Auftrag, ein Produktionsauftrag oder ein Kanban für den Lagerort freigegeben wird.
    - **Offenen Wellen zuweisen** – Stellen Sie diese Option auf *Ja*, um einer offenen Welle automatisch Positionen zuzuweisen, wenn die Positionen freigegeben werden. Positionen werden Wellen basierend auf den Abfragefilter für die Wellenvorlage zugewiesen.
    - **Welle bei Freigabe für Lagerort verarbeiten** – Stellen Sie diese Option auf *Ja*, um die Welle automatisch zu verarbeiten und Arbeit zu erstellen, wenn eine Position an den Lagerort freigegeben wird.
    - **Welle bei Schwelle automatisch verarbeiten** – Stellen Sie diese Option auf *Ja*, um die Welle automatisch zu verarbeiten, wenn die Werte die Schwellenwerte für Gewicht, Lieferung und die Positionen erreichen, die in der Feldgruppe **Wellenschwellenwerte** angegeben sind. Diese Einstellung steht nur zur Verfügung, wenn *Versand* im Feld **Wellenvorlagentyp** aktiviert wurde.
    - **Wellenfreigabe automatisieren** – Stellen Sie diese Option auf *Ja*, um die Welle automatisch freizugeben. Die Entnahmearbeit wird auf mobilen Geräten erstellt und bereitgestellt.
    - **Freigabe der Wiederbeschaffungsarbeit automatisieren** – Stellen Sie diese Option auf *Ja*, um bedarfsbasierte Wiederbeschaffungsarbeit zu erstellen und automatisch freizugeben. Sie müssen die Wiederbeschaffungswellenmethode der Wellenvorlage hinzufügen und eine Wiederbeschaffungsvorlage vom Typ *Wellenbedarf* benutzen. Richten Sie eine Wiederbeschaffungsvorlage auf der Seite **Wiederbeschaffungsvorlagen** ein. Dies erfordert, dass Sie die Wiederbeschaffungs-Methode der Wellenvorlage hinzufügen.
    - **Wellenverarbeitung fortsetzen, wenn Arbeitserstellung fehlschlägt** – Wenn diese Option auf *Ja* ist, verwendet das System einen leeren Lagerort, wenn es kein Bestand an dem von der Lagerplatzrichtlinie vorgeschlagenen Lagerplatz reservieren kann (z. B. weil der Bestand nicht mehr verfügbar ist). Ist die Option auf *Nein* gesetzt, schlägt die Welle fehl, falls das System den Bestand nicht reservieren kann.

1. Legen Sie die Feldgruppe **Wellenschwellenwerte** nach Bedarf wie folgt ein:
    - **Wellengewichtsschwellenwert** – Geben Sie das Höchstgewicht ein, das eine Welle enthalten kann.
    - **Versandschwellenwert** – Geben Sie die maximale Anzahl von Lieferungen ein, die in einer Welle enthalten sein können.
    - **Positionsschwellenwert** – Geben Sie die maximale Anzahl von Positionen ein, die in einer Welle enthalten sein können.

1. Wählen Sie in der Feldgruppe **Standardwerte** die Wellenattribute aus, die als zusätzliche Kriterien für die Wellenvorlage zu verwenden sind. Wellenattribute sind nützlich für die Zuweisung von zusätzlichen Kriterien, etwa eines bestimmten Debitorennamens, zu einer Wellenvorlage. Sie können diese Attribute auf der Seite **Wellenattribute** erstellen. 

1. Legen Sie **Wellenbenachrichtigungsrichtlinie** auf die Richtlinie fest, die Sie zum Generieren von Benachrichtigungen für Wellen verwenden möchten, die diese Vorlage nutzen. Ein Beispiel für eine Wellenbenachrichtigungsrichtlinie finden Sie unter [Wellenausführungsbenachrichtigungen](wave-execution-notifications.md).

1. Im Inforegister **Methoden** listet der Bereich **Ausgewählte Methoden** die Methoden für den ausgewählten Wellenvorlagentyp auf. Die Wellenmethoden führen die Aktivitäten aus, die von ausgewählten Vorlage erstellt werden, wie Erstellen oder Verteilen von Arbeit. Diese Aktivitäten wird auch bezeichnet als Wellenschritte. Wellenmethoden sind für jeden Wellenvorlagentyp vordefiniert. Sie können die vordefinierten Wellenmethoden nicht entfernen. Sie können jedoch die Reihenfolge der Methoden neu anordnen und zusätzliche Methoden hinzufügen. Wenn Sie beispielsweise eine Wellenvorlage für den Versand erstellen, können Sie Methoden für Wiederbeschaffung und Containerisierung hinzufügen. Die Wellencontainerisierung kann zu einer Abfolge von Wellenmethoden hinzugefügt werden, um die Containerisierung der Positionen festzulegen, die in einer Wellenvorlage verarbeitet werden. Um eine zusätzliche Methode hinzuzufügen, gehen Sie folgendermaßen vor:

    - Wählen Sie im Bereich **Verbleibende Methoden** eine Methode aus, und klicken Sie anschließend auf den **Links**-Pfeil, um sie dem Bereich **Ausgewählte Methoden** hinzuzufügen.
    - Um die Reihenfolge zu ändern, wählen Sie eine Methode aus, und wählen Sie dann den **Nach oben**- oder **Nach unten**-Pfeil.

    > [!NOTE]
    > Wenn Sie eine Methode hinzufügen, wird diese automatisch im geeigneten Speicherort in der Reihenfolge der Schritte aufgeführt.

1. Um die Abfrage einzurichten, mit der freigegebene Positionen einer geeigneten Welle zugeteilt werden, wählen Sie im Aktivitätsbereich **Abfrage bearbeiten**.
1. Um sicherzustellen dass die Wellenvorlageneinstellungen gültig sind, wählen Sie **Vorlage prüfen** aus.
