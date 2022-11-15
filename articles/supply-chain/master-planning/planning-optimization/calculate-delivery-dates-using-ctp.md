---
title: Liefertermine für Aufträge mit CTP berechnen
description: Mit der Funktionalität der Verfügbarkeitszusage (CTP) können Sie Ihren Kunden realistische Termine nennen, wann Sie bestimmte Waren zusichern können. In diesem Artikel wird beschrieben, wie Sie CTP für jedes Planungsmodul (Planungsoptimierung und das veraltete Produktprogrammplanungsmodul) einrichten und verwenden.
author: t-benebo
ms.date: 07/20/2022
ms.topic: article
ms.search.form: SalesAvailableDlvDates, SalesTable, CustParameters, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-07-20
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 4a3b8ba89d9fb224026cf32cad89d7f28321ee79
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2022
ms.locfileid: "9741202"
---
# <a name="calculate-sales-order-delivery-dates-using-ctp"></a>Liefertermine für Aufträge mit CTP berechnen

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->
<!-- KFN: Split into two topics, one for PO and one for classic. -->

Mit der Funktionalität der Verfügbarkeitszusage (CTP) können Sie Ihren Kunden realistische Termine nennen, wann Sie bestimmte Waren zusichern können. Sie können für jede Verkaufsposition ein Datum angeben, das den vorhandenen Bestand, die Produktionskapazität und die Transportzeiten berücksichtigt.

CTP erweitert die Funktionalität [verfügbar für Zusage](../../sales-marketing/delivery-dates-available-promise-calculations.md) (VfZ) durch Berücksichtigung von Kapazitätsinformationen. Während die VfZ nur die Materialverfügbarkeit berücksichtigt und von unendlichen Kapazitätsressourcen ausgeht, berücksichtigt die CTP sowohl die Material- als auch die Kapazitätsverfügbarkeit. Daher liefert sie ein realistischeres Bild davon, ob die Nachfrage innerhalb eines bestimmten Zeitrahmens gedeckt werden kann.

Die CTP funktioniert jedoch ein wenig anders, je nachdem, welches Produktprogrammplanungsmodul sie verwenden (Planungsoptimierung oder veraltetes Produktprogrammplanungsmodul). In diesem Artikel wird beschrieben, wie Sie die einzelnen Module einrichten. Die CTP für Planungsoptimierung unterstützt derzeit nur eine Teilmenge der CTP-Szenarien, die das veraltete Produktprogrammplanungsmodul unterstützt.

## <a name="turn-on-ctp-for-planning-optimization"></a>CTP für Planungsoptimierung einschalten

Die CTP für das veraltete Produktprogrammplanungsmodul steht immer nur Verfügung. Wenn Sie jedoch die CTP für Planungsoptimierung verwenden möchten, muss sie für Ihr System aktiviert werden. Administratoren können mit den Einstellungen [Funktionsverwaltung](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und sie aktivieren. Im Arbeitsbereich **Funktionsverwaltung** ist die Funktion wie folgt aufgeführt:

- **Modul:** *Produktprogrammplanung*
- **Funktionsname:** *(Vorschauversion) CTP für Planungsoptimierung*

## <a name="how-ctp-compares-to-atp"></a>Vergleich zwischen CTP und ATP

CTP und ATP ähneln sich, aber die CTP kann oft ein genaueres Ergebnis liefern, wie das folgende Beispiel zeigt.

Artikel A ist ein Artikel, der sich aus den Artikeln B und C zusammensetzt. Die vorrätige Menge von Artikel A ist 0 (null). Wenn Sie eine ATP-Prüfung durchführen, die nur Materialien berücksichtigt, ist die ATP-Menge ebenfalls 0 (null). Wenn Sie jedoch eine CTP-Prüfung durchführen, prüft das System die Verfügbarkeit der ArtikelBB und C, prüft die Ressourcen, die erforderlich sind, um aus ihnen Artikel A zu fertigen, und berechnet, wie viele Stück von Artikel A hergestellt werden können. Darüber hinaus kann die CTP-Berechnung die Ressourcen und Materialien prüfen, die erforderlich sind, um mehr Stück der Artikel B und C herzustellen und aus ihnen wiederum mehr von Artikel A zu machen.

Eine CTP-Berechnung, die sowohl Materialien als auch Ressourcen berücksichtigt, kann eine größere Menge anzeigen als eine Berechnung, die nur Materialien prüft, insbesondere wenn es sich bei dem geprüften Artikel um einen Auftragsmontageartikel handelt. Mit anderen Worten, die CTP-Funktion basiert auf der aufgeschlüsselten Funktion und kann für eine ausgewählte Auftragsposition ausgeführt werden, um das erwartete Lieferdatum zu berechnen.

## <a name="how-ctp-differs-depending-on-the-master-planning-engine-that-you-use"></a>Wie sich die CTP je nach verwendetem Produktprogrammplanungsmodul unterscheidet

Die folgende Tabelle fasst die Unterschiede zwischen der CTP für die Planungsoptimierung und der CTP für das veraltete Produktprogrammplanungsmodul zusammen.

| Element | Planungsoptimierung | Veraltetes Produktprogrammplanungsmodul |
|---|---|---|
| Einstellungen der **Lieferterminkontrolle** für Aufträge, Auftragspositionen und Produkte | *CTP für Planungsoptimierung* | *CTP* |
| Berechnungszeit | Die Berechnung wird ausgelöst, indem ein dynamischer Plan als geplante Aufgabe ausgeführt wird. | Die Berechnung wird jedes Mal sofort ausgelöst, wenn Sie eine Auftragsposition eingeben oder aktualisieren. |
| Wert des Felds **CTP für den Planungsoptimierungsstatus** | <p>Der Wert *Nicht bereit* wird für Aufträge und Auftragspositionen angezeigt, bei denen der dynamische Plan nicht ausgeführt wurde, seit die Aufträge und Positionen erstellt oder zuletzt aktualisiert wurden.</p><p>Der Wert *Bereit* wird für Aufträge und Positionen angezeigt, bei denen die CTP verwendet wurde, um mithilfe des dynamischen Plans bestätigte Liefertermine zu berechnen.</p> | Der Wert *Bereit* wird immer angezeigt. |

## <a name="set-default-delivery-date-control-methods"></a><a name="default-methods"></a>Standardmethoden für die Lieferdatumskontrolle festlegen

Das System kann eine von mehreren Methoden verwenden, um geschätzte Liefertermine für jeden Auftrag und jede Auftragsposition zu berechnen. Sie sollten die Methode der Lieferdatumskontrolle, die Sie am häufigsten verwenden möchten, als globale Standardmethode festlegen. Sie können für jedes Produkt eine individuelle Überschreibung einrichten. Später können Sie die Standardmethoden für jeden Auftrag und/oder jede Auftragsposition nach Bedarf überschreiben.

### <a name="set-the-global-default-delivery-date-control"></a><a name="global-default"></a>Die globale Lieferdatumskontrolle festlegen

Die Standardmethode für die Lieferdatumskontrolle wird auf alle neuen Auftragspositionen angewendet, für die keine Überschreibung gilt. Sie können wie folgt eine auswählen.

1. Gehen Sie zu **Debitoren \> Einrichtung \> Debitorenparameter**.
1. Wählen Sie auf der Registerkarte **Lieferung** im Inforegister **Lieferungskontrolle** im Feld **Lieferterminkontrolle** die Methode aus, die Sie als Standardmethode für Ihr Unternehmen verwenden möchten:

    - *Keine*: Lieferdaten werden nicht berechnet.
    - *Verkaufslieferzeit* – Die Verkaufslieferzeit ist die Zeit, die zwischen dem Erstellen des Auftrags und dem Versand der Artikel verstreicht. Die Berechnung des Lieferdatums basiert auf einer Standardanzahl von Tagen und berücksichtigt nicht die Verfügbarkeit am Lager, den bekannten Bedarf oder eine geplante Lieferung.
    - *VfZ*: Die VfZ ist die Menge eines Artikels, der verfügbar ist und einem Kunden für ein bestimmtes Datum zugesichert werden kann. Bei der VfZ-Berechnung werden nicht zugesicherter Bestand, Lieferzeiten und geplante Zu- und Abgänge berücksichtigt.
    - *VfZ + Sicherheitszuschlag für Warenabgang*: Das Versanddatum entspricht dem VfZ-Datum plus dem Sicherheitszuschlag für den Artikel. Der Sicherheitszuschlag für Warenabgang ist die zur Vorbereitung der Artikel für die Lieferung erforderliche Zeit.
    - *CTP*: Verwenden Sie die CTP-Berechnung, die von dem veralteten Produktprogrammplanungsmodul bereitgestellt wird. Wenn Sie die Planungsoptimierung verwenden, ist die *CTP*-Methode zur Lieferdatumskontrolle nicht zulässig und führt, wenn sie ausgewählt ist, bei Durchführung der Berechnung zu einem Fehler.
    - *CTP für die Planungsoptimierung*: Verwenden Sie die CTP-Berechnung, die von der Planungsoptimierung bereitgestellt wird. Diese Option hat keinerlei Wirkung, wenn Sie das veraltete Produktprogrammplanungsmodul verwenden.

### <a name="set-delivery-date-control-overrides-for-individual-products"></a>Überschreibungen für die Lieferdatumskontrolle für einzelne Produkte festlegen

Sie können Überschreibungen für bestimmte Produkte zuweisen, wenn Sie eine andere Methode zur Lieferdatumskontrolle als die verwenden möchten, die als Ihre globale Standardmethode festgelegt ist.

1. Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**.
1. Wählen Sie aus, das Sie einrichten möchten.
1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Lagerbestand verwalten** in der Gruppe **Auftragseinstellungen** die Option **Standardauftragseinstellungen** aus.
1. Setzen Sie auf der Seite **Standardauftragseinstellungen** auf dem Inforegister **Auftrag** die Option **Lieferungskontrolle überschreiben** auf *Ja*.
1. Wählen Sie im Feld **Lieferdatumskontrolle** die Methode aus, die für das ausgewählte Produkt verwendet werden soll. Es stehen dieselben Optionen zur Verfügung, die im Abschnitt [Die globale Lieferdatumskontrolle festlegen](#global-default) beschrieben sind.

## <a name="schedule-ctp-for-planning-optimization-calculations"></a><a name="batch-job"></a>Die CTP für Berechnungen der Planungsoptimierung planen

Wenn Sie die CTP für die Planungsoptimierung verwenden, müssen Sie einen dynamischen Plan ausführen, damit das System die CTP-Berechnung auslöst, und dann die bestätigten Versand- und Wareneingangsdaten für alle relevanten Aufträge festlegen. Der Plan muss alle Artikel enthalten, für die bestätigte Versand- und Wareneingangsdaten erforderlich sind. (Wenn Sie die CTP für das veraltete Masterplanungsmodul verwenden, werden die CTP-Berechnungen sofort lokal durchgeführt. Daher müssen Sie keinen dynamischen Plan ausführen, um die CTP-Ergebnisse anzuzeigen.)

Damit die Termine für alle Benutzer rechtzeitig verfügbar sind, empfehlen wir Ihnen, Stapelverarbeitungsaufträge einzurichten, um die entsprechenden Pläne auf wiederkehrender Basis auszuführen. Beispielsweise legt ein Stapelverarbeitungsauftrag, der so eingerichtet ist, dass alle 30 Minuten ein dynamischer Plan ausgeführt wird, die bestätigten Versand- und Wareneingangsdaten alle 30 Minuten fest. Daher müssen Benutzer, die Aufträge eingeben und importieren, maximal 30 Minuten warten, um die bestätigten Versand- und Wareneingangsdaten zu erhalten.

Gehen Sie wie folgt vor, um einen Stapelverarbeitungsauftrag zum regelmäßigen Ausführen eines dynamischen Plans einzurichten.

1. Wechseln Sie zu **Produktprogrammplanung \> Produktprogrammplanung \> Ausführen \> Produktprogrammplanung**.
1. Legen Sie im Dialogfeld **Produktprogrammplanung** auf dem Inforegister **Parameter** das Feld **Produktprogrammplanung** auf den dynamischen Plan fest, den Sie ausführen möchten.
1. Legen Sie im Inforegister **Im Hintergrund ausführen** die Option **Stapelverarbeitung** auf *Ja* fest.
1. Wählen Sie **Wiederholung** und richten Sie den Zeitplan nach Bedarf ein.
1. Wählen Sie **OK**, um den Plan zu speichern.
1. Wählen Sie **OK** aus, um den Stapelverarbeitungsauftrag zu erstellen und das Dialogfeld zu schließen.

## <a name="use-ctp-for-the-deprecated-master-planning-engine"></a>Verwenden Sie CTP für die veraltete Hauptplanungs-Engine

### <a name="create-a-new-order-by-using-ctp-for-the-deprecated-master-planning-engine"></a>Erstellen Sie einen neuen Auftrag, indem Sie die CTP für das veraltete Produktprogrammplanungsmodul verwenden

Jedes Mal, wenn Sie einen neuen Auftrag oder eine neue Auftragsposition hinzufügen, weist das System diesem bzw. dieser eine standardmäßige Methode zur Lieferdatumskontrolle zu. Der Auftragskopf beginnt immer mit der globalen Standardmethode. Wenn einem bestellten Artikel eine Überschreibung zugewiesen wird, verwendet die neue Auftragsposition diese Überschreibung. Andernfalls verwendet die neue Auftragsposition ebenfalls die globale Standardmethode. Deshalb sollten Sie Ihre Standardmethoden so einrichten, dass sie dem Lieferdatum entsprechen, das Sie am häufigsten verwenden möchten. Nachdem Sie einen Auftrag erstellt haben, können Sie die Standardmethode auf Ebene des Auftragskopfs und/oder der Auftragsposition nach Bedarf überschreiben. Weitere Informationen finden Sie unter [Standardmethoden für die Lieferdatumskontrolle festlegen](#default-methods) und [Vorhandene Aufträge auf Verwendung von CTP abändern](#change-orders).

### <a name="view-confirmed-delivery-dates-when-you-use-ctp-for-the-deprecated-master-planning-engine"></a>Bestätigte Liefertermine anzeigen, wenn Sie die CTP für das veraltete Produktprogrammplanungsmodul verwenden

Wenn Sie das veraltete Produktprogrammplanungsmodul verwenden, werden CTP-Berechnungen auf Aufträge und/oder Auftragspositionen angewendet, bei denen das Feld **Lieferterminkontrolle** auf *CTP* festgelegt ist.

Für Auftragspositionen, welche die CTP für das veraltete Produktprogrammplanungsmodul verwenden, legt das System die Felder **Bestätigtes Lieferdatum** und **Bestätigtes Wareneingangsdatum** jedes Mal fest, wenn Sie eine Auftragsposition speichern. Wenn Sie später eine relevante Änderung an einer Auftragsposition vornehmen (z. B. durch Änderung der Menge oder des Standorts), werden die Termine sofort neu berechnet.

- Um die bestätigten Liefertermine für eine Auftragsposition anzuzeigen, öffnen Sie den Auftrag und wählen Sie die Auftragsposition aus. Überprüfen Sie dann im Inforegister **Positionsdetails** der Registerkarte **Lieferung** die Werte für **Bestätigtes Lieferdatum** und **Bestätigtes Wareneingangsdatum**.
- Um die bestätigten Liefertermine für einen gesamten Auftrag anzuzeigen, öffnen Sie den Auftrag und wählen Sie die Ansicht **Kopf** aus. Überprüfen Sie dann im Inforegister **Lieferung** die Werte für **Bestätigtes Lieferdatum** und **Bestätigtes Wareneingangsdatum**.

## <a name="use-ctp-for-planning-optimization"></a>CTP für die Planungsoptimierung verwenden

### <a name="create-a-new-order-by-using-ctp-for-planning-optimization"></a>Einen neuen Auftrag durch die Verwendung der CTP für die Planungsoptimierung erstellen

Jedes Mal, wenn Sie einen neuen Auftrag oder eine neue Auftragsposition hinzufügen, weist das System diesem bzw. dieser eine standardmäßige Methode zur Lieferdatumskontrolle zu. Der Auftragskopf beginnt immer mit der globalen Standardmethode. Wenn einem bestellten Artikel eine Überschreibung zugewiesen wird, verwendet die neue Auftragsposition diese Überschreibung. Andernfalls verwendet die neue Auftragsposition ebenfalls die globale Standardmethode. Deshalb sollten Sie Ihre Standardmethoden so einrichten, dass sie dem Lieferdatum entsprechen, das Sie am häufigsten verwenden möchten. Nachdem Sie einen Auftrag erstellt haben, können Sie die Standardmethode auf Ebene des Auftragskopfs und/oder der Auftragsposition nach Bedarf überschreiben. Weitere Informationen finden Sie unter [Standardmethoden für die Lieferdatumskontrolle festlegen](#default-methods) und [Vorhandene Aufträge auf Verwendung von CTP abändern](#change-orders).

### <a name="view-confirmed-delivery-dates-when-using-ctp-for-planning-optimization"></a>Bestätigte Liefertermine bei der Verwendung der CTP für die Planungsoptimierung anzeigen

Wenn Sie die Planungsoptimierung verwenden, werden CTP-Berechnungen auf Aufträge und/oder Auftragspositionen angewendet, bei denen das Feld **Lieferterminkontrolle** auf *CTP für die Planungsoptimierung* festgelegt ist.

Für Auftragspositionen, welche die CTP für die Planungsoptimierung verwenden, bleiben die Felder **Bestätigtes Lieferdatum** und **Bestätigtes Wareneingangsdatum** leer, bis Sie den entsprechenden dynamischen Plan ausführen (in der Regel durch Verwendung eines regelmäßigen Stapelverarbeitungsauftrags). Sie werden dann automatisch eingestellt. Weitere Informationen finden Sie unter [Die CTP für Berechnungen der Planungsoptimierung planen](#batch-job).

Das Feld **Status der CTP für die Planungsoptimierung** gibt an, ob bereits bestätigte Termine für jede Position berechnet wurden, welche die CTP für die Planungsoptimierung verwendet. Das Feld zeigt einen Wert von *Nicht bereit* für Positionen und Aufträge, bei denen die bestätigten Liefertermine entweder noch nicht berechnet wurden oder aufgrund anderer Änderungen nicht mehr gültig sind. Es zeigt einen Wert von *Bereit* für berechnete Positionen und Aufträge an. Sie können den Status für jede Position und für den gesamten Auftrag anzeigen.

- Um den Status für eine Auftragsposition anzuzeigen, öffnen Sie den Auftrag und wählen Sie die Auftragsposition aus. Überprüfen Sie dann im Inforegister **Auftragspositionen** der Registerkarte **Lieferung** die Werte des **Status der CTP für die Planungsoptimierung**. Die Felder **Bestätigtes Lieferdatum** und **Bestätigtes Wareneingangsdatum** für die Position werden auch auf dieser Registerkarte angezeigt, nachdem sie berechnet wurden.
- Um den Status für einen gesamten Auftrag anzuzeigen, öffnen Sie den Auftrag und wählen Sie die Ansicht **Kopf** aus. Überprüfen Sie dann im Inforegister **Lieferung** den Wert des **Status der CTP für die Planungsoptimierung**. Die Felder **Bestätigtes Lieferdatum** und **Bestätigtes Wareneingangsdatum** für den Auftrag werden auch auf dieser Registerkarte angezeigt, nachdem sie berechnet wurden.

<!-- KFM: The following text may be untrue and needs to be reviewed with the PM for next revision:

The sales orders that are *Ready* or *Not ready* are shown in the **All sales orders** list page. You can check the sales order that are *Ready* or *Not ready* from the sales order list page by filtering on this new status field.

-->

> [!NOTE]
> - Wenn Sie eine Auftragsposition aktualisieren, nachdem die CTP für die Planungsoptimierung bestätigte Daten dafür berechnet hat, löscht das System diese Daten, bis der entsprechende dynamische Plan das nächste Mal ausgeführt wird.
> - Wenn Sie eine zugehörige Einstellung bearbeiten, die sich auf bestehende bestätigte Termine auswirken könnte (z. B. durch Ändern von Lieferzeiten, Reservierungen oder Markierungen), sollten Sie die bestätigten Termine für die relevanten bestehenden Aufträge löschen. Diese Aktion bewirkt, dass der Status jeder relevanten Position auf *Nicht bereit* geändert wird. Diese Änderung wiederum bewirkt, dass das System die bestätigten Daten neu berechnet, wenn es den dynamischen Plan das nächste Mal ausführt.

## <a name="change-existing-sales-orders-so-that-they-use-ctp"></a><a name="change-orders"></a>Vorhandene Aufträge so ändern, dass sie CTP verwenden

Sie können den Wert der **Lieferterminkontrolle** für jeden offenen Auftrag jederzeit ändern. Sie können den Wert auf Kopfebene und/oder für jede Position nach Bedarf ändern.

### <a name="change-to-ctp-at-the-order-header-level"></a>Auf Auftragskopfebene zu CTP wechseln

<!-- KFM: Would be nice to mention how changing this setting on the header affects the individual lines. -->

Gehen Sie wie folgt vor, um einen Auftrag so zu ändern, dass sie CTP auf Bestellkopfebene verwendet.

1. Wechseln Sie zu **Debitoren \> Aufträge \> Alle Aufträge**.
1. Öffnen Sie den Auftrag, den Sie einrichten möchten, oder erstellen Sie einen neuen.
1. Wählen Sie **Kopf** aus, um auf der Seite **Auftragsdetails** die Kopfzeileninformationen zu öffnen.
1. Legen Sie auf dem Inforegister **Lieferung** das Feld **Lieferterminkontrolle** auf einen der folgenden Werte fest, je nachdem, welches Planungsmodul Sie verwenden:

    - *CTP*: Verwenden Sie die CTP-Berechnung, die von dem veralteten Produktprogrammplanungsmodul bereitgestellt wird. Wenn Sie die Planungsoptimierung verwenden, ist die Methode *CTP* zur Lieferterminkontrolle nicht zulässig. Wenn Sie diesen Wert auswählen, tritt daher ein Fehler auf, wenn die Berechnung ausgeführt wird.
    - *CTP für die Planungsoptimierung*: Verwenden Sie die CTP-Berechnung, die von der Planungsoptimierung bereitgestellt wird. Diese Einstellung hat keinerlei Wirkung, wenn Sie das veraltete Produktprogrammplanungsmodul verwenden.

<!-- KFM: Additional dialogs are shown here. Review these with the PM and expand this procedure at next revision. -->
1. Wählen Sie **OK**, um Ihre Änderungen zu übernehmen.

### <a name="change-to-ctp-at-the-order-line-level"></a>Auf Auftragspositionsebene zu CTP wechseln

Wenn Sie eine Auftragsposition mit einer anderen Methode der Lieferdatumskontrolle erstellt haben, können Sie jederzeit zu CTP wechseln. Änderungen, die Sie auf Positionsebene vornehmen, wirken sich nicht auf andere Positionen aus. Sie können jedoch dazu führen, dass sich die Lieferdaten des gesamten Auftrags nach vorne oder hinten verschieben, je nachdem, wie sich die einzelnen aktualisierten Positionsberechnungen ändern. <!-- KFM: Confirm this intro at next revision -->

Gehen Sie wie folgt vor, um einen Auftrag so zu ändern, dass er die CTP für das veraltete Produktprogrammplanungsmodul auf Positionsebene verwendet.

1. Wechseln Sie zu **Debitoren \> Aufträge \> Alle Aufträge**.
1. Öffnen Sie den Auftrag, den Sie einrichten möchten, oder erstellen Sie einen neuen.
1. Wählen Sie auf der Seite **Auftragsdetails** auf dem Inforegister **Auftragsposition** die Auftragsposition aus, die Sie einrichten möchten.
1. Legen Sie auf dem Inforegister **Positionsdetails** auf der Registerkarte **Lieferung** das Feld **Lieferterminkontrolle** auf einen der folgenden Werte fest, je nachdem, welches Planungsmodul Sie verwenden:

    - *CTP*: Verwenden Sie die CTP-Berechnung, die von dem veralteten Produktprogrammplanungsmodul bereitgestellt wird. Wenn Sie die Planungsoptimierung verwenden, ist die Methode *CTP* zur Lieferterminkontrolle nicht zulässig. Wenn Sie diesen Wert auswählen, tritt daher ein Fehler auf, wenn die Berechnung ausgeführt wird.
    - *CTP für die Planungsoptimierung*: Verwenden Sie die CTP-Berechnung, die von der Planungsoptimierung bereitgestellt wird. Diese Einstellung hat keinerlei Wirkung, wenn Sie das veraltete Produktprogrammplanungsmodul verwenden.

    Das Dialogfeld **Verfügbare Versand- und Wareneingangsdaten** wird angezeigt und zeigt die verfügbaren Versand- und Wareneingangsdaten an. Dieses Dialogfeld funktioniert für Auftragspositionen genauso wie für den Auftragskopf, wie im vorherigen Abschnitt beschrieben.

1. Wählen Sie im Aktionsbereich **Speichern** aus.
