---
title: Automatische Aktualisierung von Lieferungen
description: Dieses Thema bietet einen Überblick über Funktionen, die automatische Aktualisierungen für Lieferungen bereitstellen.
author: josaw1
manager: tfehr
ms.date: 11/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTemplateTable,SalesTableListPage,SalesTable,WHSWaveTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7fa2684340f5ce45b99ff9aee9937071f936b81a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428501"
---
# <a name="shipment-auto-updates"></a>Automatische Aktualisierung von Lieferungen

[!include [banner](../includes/banner.md)]

Die Funktion zur automatischen Aktualisierung von Lieferungen aktualisiert automatisch die Mengen (Erhöhungen und Senkungen) in einer Ladungsposition, die einer Lieferung zugeordnet ist, nachdem die Ladung an einen Lagerort geschickt wurde. Diese Funktion bleibt aktiviert, bis die Ladungsposition in der Lieferung oder Ladung in einer Welle verarbeitet wird. Wenn sie verwendet wird, können Auftragsaktualisierungen den Lagerort automatisch durchfließen, ohne manuelle Aktivitäten festlegen zu müssen, bis Lagerortarbeit erstellt wurde.

Wenn die Funktion zur automatischen Lieferungsktualisierung nicht verwendet wird, werden nur Mengensenkungen automatisch fließen, bis Lagerortarbeit erstellt wurde. Benutzer müssen Positionen manuell aktualisieren oder löschen und sie müssen Positionen erneut freigeben, wenn Auftragsmengen erhöht oder neue Auftragspositionen hinzugefügt werden. Indem die Funktion zur automatischen Lieferungsaktualisierung verwendet wird, können Unternehmen dem Lagerort nahtlos Aktualisierungen bereitstellen, ohne sich zu sorgen, dass zugehörige Lieferungen und Ladungen aktualisierte Auftragspositionen nicht widerspiegeln.

Die Funktion zur automatischen Lieferungsaktualisierung gilt sowohl für Auftragspositionen und Umlagerungspositionen und sie wurde für einen bestimmten Lagerort aktiviert. Daher können Unternehmen je nach Bedarf verschiedene Richtlinien zur automatischen Lieferungsaktualisierung in unterschiedlichen Lagerorten anwenden. Standardmäßig wird die Richtlinie zur automatischen Lieferungsaktualisierung für Mengensenkungen für alle Lagerorte verwendet, die Lagerortverwaltungsprozesse verwenden. Wenn diese Standardrichtlinieneinstellung verwendet wird, fließen nur Mengensenkungen automatisch durch eine Lieferung und Ladung, bis Lagerortarbeit erstellt wurde. Dieses Verhalten ähnelt dem Verhalten, das verwendet wurde, bevor die Funktion zur automatischen Lieferungsaktualisierung eingeführt wurde.

## <a name="main-elements-of-the-functionality"></a>Wichtigste Elemente der Funktion

Die Funktion zur automatischen Lieferungsaktualisierung verlässt sich vorrangig auf den Lieferstatus, um zu bestimmen, ob die Menge in einer Ladungsposition geändert werden sollte, wenn einer Änderung an einer Auftragsposition oder einer Umlagerungsposition vorgenommen wird. Sie verlässt sich auch in erster Linie auf den Lieferungsstatus, um festzustellen, wann eine neue Ladungsposition einer vorhandenen Ladung automatisch hinzugefügt werden soll. Wenn der Status **In Wellen** oder höher ist, erfolgt keine automatische Aktualisierung.

Der Wellenstatus wird auch für automatische Aktualisierungen berücksichtigt. Wenn die Welle, die der Ladungsposition zugeordnet ist, den Status **Abgehalten**, **Ausführung**, **Freigegeben**, **Entnommen** oder **Versendet** hat, wenn ein Benutzer versucht, die Menge in einer Ladungsposition oder Umlagerungsposition (über eine Menegensenkung in der Auftragsposition oder Umlagerungsauftragsposition) zu reduzieren, wird die folgende Fehlermeldung angezeigt: „Reservierungen können nicht entfernt werden, da es erstellte Arbeit gibt, die auf den Reservierungen basieren“. Wenn die Welle außerdem einen der oben genannten Wellenstatus hat, wenn ein Benutzer versucht, die Menge der Ladungsposition indirekt zu erhöhen, indem er die Menge in der Auftragsposition oder die Umlagerungsauftragsposition verringert, wird die Menge auf der Ladungsposition nicht automatisch erhöht. In diesem Fall muss die Ladungsposition manuell aktualisiert werden.

## <a name="scenarios"></a>Szenarien

Die Funktion zur automatischen Lieferungsaktualisierung unterstützt vier Szenarien: eine neue Auftragsposition hinzufügen, die Menge in eine Auftragsposition erhöhen, die Menge in einer Auftragsposition verringern und eine Auftragsposition entfernen.

- **Eine neue Auftragsposition hinzufügen** – Wenn das Feld **Lieferung automatisch aktualisieren** auf der Inforegister **Lagerort** der Seite **Lagerorte** page (**LAgerortverwaltung \> Einstellungen \> Lagerort \> Lagerorte**) auf **Immer** festgelegt ist, wenn eine Lieferung für den Auftrag vorhanden ist, und eine neue Auftragsposition zu einem Auftrag oder Umlagerungsauftrag hinzugefügt wird, nachdem bereits eine Ladung für den Auftrag erstellt wurde, wird die vorhandene Ladung nicht aktualisiert. Eine neue Ladungsposition, die keine Referenz zu dieser vorhandenen Ladung aufweist, wird erstellt und der bereits vorhandenen Lieferung zugeordnet. Die neue Position wird der Ladung hinzugefügt und freigegeben.
- **Die Menge in einer Auftragsposition erhöhen** – Wenn das Feld **Lieferung automatisch aktualisieren** auf **Immer** festgelegt wird, wenn eine Lieferung für den Auftrag vorhanden ist und die Menge in einer vorhandenen Auftragsposition oder Umlagerungsauftragsposition erhöht wird, nachdem bereits eine Ladung für den Auftrag erstellt wurde, wird die Ladungsposition um dieselbe Menge wie die Auftragsposition erhöht. Wenn die Ladung freigegeben wurde, jedoch keine Arbeit erstellt wurde, wird die Ladungsposition um dieselbe Menge wie die Auftragsposition erhöht.
- **Die Menge in einer Auftragsposition senken** – Wenn das Feld **Lieferung automatisch aktualisieren** auf **Immer** oder **Mengenverringerung ein** festgelegt wird, wenn eine Lieferung für den Auftrag vorhanden ist und die Menge in einer vorhandenen Auftragsposition oder Umlagerungsauftragsposition reduziert wird, nachdem bereits eine Ladung für den Auftrag erstellt wurde, wird wird die Menge der zugehörigen Ladungsposition entsprechend aktualisiert, es sei denn, die Menge in der Ladungsposition ist bereits gleich oder kleiner als die neue Menge in der Ladungsposition. In diesem Fall ist die Ladungsposition nicht betroffen. Wenn Ladung freigegeben wurde, jedoch keine Arbeit erstellt wurde, wird wird die Menge der zugehörigen Ladungsposition entsprechend aktualisiert, es sei denn, die Menge in der Ladungsposition ist bereits gleich oder kleiner als die neue Menge in der Ladungsposition. In diesem Fall ist die Ladungsposition betroffen.
- **Eine Auftragsposition entfernen** – Wenn das Feld **Lieferung automatisch aktualisieren** auf **Immer** oder **Mengenverringerung an** festgelegt wird, wenn der Benutzer versucht, eine Auftragsposition zu entfernen, für die eine Ladungsposition vorhanden ist, wird eine Fehlermeldung angezeigt.

## <a name="example-scenario"></a>Beispielszenario

Für dieses Szenario müssen Demodaten eingerichtet werden, und Sie müssen das **USMF**-Demodatunternehmen verwenden.

### <a name="turn-on-the-auto-update-shipment-functionality"></a>Die Funktion zur automatischen Lieferungsaktualisierung ausschalten

Befolgen Sie die Schritte, um die Funktion zur automatischen Lieferungsaktualisierung auszuschalten.

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerort \> Lagerorte**.
2. Wählen Sie Lagerort **24**.
3. Ändern Sie im Inforegister **Lagerort** im Feld **Lieferung automatisch aktualisieren** den Wert von **Bei Mengensenkung** zu **Immer**.

Nachdem Sie den Wert auf **Immer** geändert haben, werden alle Erhöhungen oder Senkungen der Mengen in Auftragspositionen und Umlagerungsauftragspositionen und Ergänzungen neuer Positionen in Lieferungen und Ladungen für den ausgewählten Lagerort angezeigt, wobei die genannten Aktualisierungseinschränkungen gelten.

### <a name="change-the-wave-template-so-that-load-lines-arent-automatically-processed"></a>Die Wellenvorlage ändern, damit Ladungspositionen nicht automatisch verarbeitet werden

Befolgen Sie folgende Schritte, um die Wellenvorlage so zu konfigurieren, dass Ladungspositionen nicht automatisch verarbeitet werden.

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Wellen \> Wellenvorlagen**.
2. Wählen Sie die Wellenvorlage **Standard-24-Lieferung** aus.
3. Wählen Sie **Bearbeiten** aus.
4. Legen Sie im Inforegister **Allgemeines** die Option **Wellenerstellung automatisieren** auf **Ja** fest, und stellen Sie sicher, dass alle anderen Optionen auf **Nein** festgelegt werden.

Es ist wichtig, dass als Teil des Wellenerstellungsprozesses nicht automatisch Arbeit erstellt und freigegeben wurde. Nachdem Arbeit erstellt wurde, die zu der Ladungsposition gehört, die für die Auftragsposition erstellt wurde, wird die Ladungsposition nicht mehr automatisch aktualisiert, wenn die Menge in der Auftragsposition geändert wird.

### <a name="create-a-sales-order"></a>Auftrag erstellen

Gehen Sie folgendermaßen vor, um einen Auftrag zu erstellen.

1. Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.
2. Wählen Sie Debitor **US-003**.
3. Erstellen Sie eine Position für Artikelnummer **A0001**.
4. Geben Sie eine Menge von **10** ein. (Stellen Sie sicher, dass Sie Lagerort **24** verwenden.)
5. Wählen Sie **Speichern**.
6. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerort**, in der Gruppe **Aktivitäten**, **Für Lagerort freigeben** aus. Eine Lieferung eine Welle werden erstellt.

Da Sie die Wellenvorlage im vorherigen Verfahren geändert haben, wird keine Ladung oder Arbeit erstellt. Der Lieferstatus ist **Offen** und der Wellenstatus ist **Erstellt**

### <a name="decrease-the-quantity-on-a-sales-order-line"></a>Menge in einer Auftragsposition reduzieren

Befolgen Sie folgende Schritte, um die Menge in einer Auftragsposition zu senken.

1. Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.
2. Wählen Sie den Auftrag aus, den Sie soeben für den Lagerort freigaben.
3. Wählen Sie die Auftragsposition aus. Ändern Sie im Feld **Menge** den Wert von **10** auf **8**.
4. In der Auftragsposition wählen Sie **Lagerort \> Lieferdetails** aus. Auf der Seite **Lieferdetails** auf dem Inforegister **Ladungspositionen** spiegelt die Menge die Änderung in der Auftragsposition wider.

### <a name="increase-the-quantity-on-a-sales-order-line"></a>Menge in einer Auftragsposition erhöhen

Befolgen Sie folgende Schritte, um die Menge in einer Auftragsposition zu erhöhen.

1. Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.
2. Wählen Sie den Auftrag aus, den Sie soeben für den Lagerort freigaben.
3. Ändern Sie die Positionsmenge von **8** **12**.
4. Wählen Sie **Speichern**.
5. Kehren Sie zur Seite **Alle Aufträge** zurück und wählen Sie den Auftrag erneut aus.
5. Wählen Sie im Aktivitätsbereich, auf der Registerkarte **Lagerort** in der Gruppe **Zugehörige Informationen** die Option **Lieferdetails**. Auf der Seite **Lieferdetails** auf dem Inforegister **Ladungspositionen** spiegelt die Menge die Änderung in der Auftragsposition wider.

Obgleich die Menge in der Ladungsposition von 8 in 12 erhöht wurde, bleiben nur acht Artikel reserviert, es sei denn, die automatische Reservierung ist aktiviert. Da die Menge, die der vorhandenen Lieferung hinzugefügt wurde, nicht reserviert wurde, wird, wenn die Welle zu diesem Zeitpunkt ohne Reservierung verarbeitet wird, Arbeit nur für die Menge erstellt, die bereits reservierte wurde.

> [!NOTE]
> Wenn die Menge einer Auftragsposition verringert wird, ist die Menge in der Ladeungsposition nicht betroffen, falls sie bereits gleich oder kleiner als die neue Menge in der Auftragsposition ist. Wenn die Menge in einer Auftragspositionen erhöht wird, wird die Ladungsposition um dieselbe Menge wie die Auftragsposition erhöht. Wenn die Menge in der Auftragsposition sich von der Mengen in der Ladungsposition unterscheidet, verbleibt die Differenz.

### <a name="add-a-sales-order-line"></a>Eine Auftragsposition hinzufügen

Um eine Auftragsposition, führen Sie folgende Schritte aus:

1. Wechseln Sie zu **Vertrieb und Marketing \> Aufträge \> Alle Aufträge**.
2. Wählen Sie den Auftrag aus, den Sie soeben für den Lagerort freigaben.
3. Erstellen Sie eine Position für Artikelnummer **A0002**.
4. Geben Sie im Feld **Menge** den Wert **10** ein. (Stellen Sie sicher, dass Sie Lagerort **24** verwenden.) Die neue Zeile wird automatisch dieser vorhandenen Lieferung hinzugefügt.
5. Wählen Sie **Speichern**.
6. Kehren Sie zur Seite **Alle Aufträge** zurück und wählen Sie den Auftrag erneut aus.
7. Wählen Sie im Aktivitätsbereich, auf der Registerkarte **Lagerort** in der Gruppe **Zugehörige Informationen** die Option **Lieferdetails**. Beachten Sie auf der Seite **Lieferdetails** auf dem Inforegister **Ladungspositionen** die zweite Ladungsposition.

Da die Auftragsposition, die Sie gerade der vorhandenen Lieferung hinzugefügt haben, nicht reserviert wurde, wird, wenn die Welle zu diesem Zeitpunkt verarbeitet wird, nur Arbeit für die Menge in der ersten Auftragsposition und der ersten Ladungsposition erstellt.

### <a name="process-a-wave"></a>Eine Welle verarbeiten

Führen Sie folgende Schritte aus, um die Welle zu verarbeiten:

1. Wechseln Sie zu **Lagerortverwaltung \> Ausgehende Wellen \> Lieferungswellen \> Alle Wellen**.
2. Wählen Sie die Welle aus, die Sie zuvor erstellt haben.
3. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Welle** in der Gruppe **Welle** auf **Verarbeiten**.

Die Welle wird verarbeitet und Arbeit für die reservierten Mengen in der Ladungsposition erstellt. Der Lieferstatus wird von **Offen** auf **In Wellen** aktualisiert. Wird der Lieferstatus auf **In Wellen** aktualisiert, wirken sich Änderungen wie Verringerungen oder Erhöhungen in Positionsmengen oder die Ergänzung neuer Positionen zum Auftrag nicht auf die vorhandenen Ladungspositionen aus, die der Lieferung in Wellen zugeordnet sind.

Wenn eine Lieferung den Status **In Wellen** oder höher hat, werden Aktualisierungen der Menge in einer Auftragsposition nicht angezeigt oder gegen eine Ladungsposition geprüft, die der Lieferung zugeordnet ist. Änderungen an der Menge in der Ladungsposition müssen direkt in der Ladungsposition vorgenommen werden.

Die Prüfung wird durchgeführt, nachdem Arbeit für die Ladungsposition erstellt und eine Reservierung vorgenommen wurde. Eine Verringerung der Menge in der Auftragsposition wird dann gegen die Arbeitspositionsreservierung geprüft.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]