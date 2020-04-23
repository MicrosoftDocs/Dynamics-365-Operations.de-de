---
title: Bestellungen genehmigen und bestätigen
description: Dieser Artikel beschreibt die Statuswerte einer Bestellung nach der Erstellung und den Effekt des Änderungsmanagements für Bestellungen.
author: mkirknel
manager: tfehr
ms.date: 04/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Retail
ms.custom: 93143
ms.assetid: cd12a944-c52c-4579-a301-7abe1d237c72
ms.search.region: Global
ms.search.industry: ''
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6b331b7e7725b3dd284deb02e59fcf2d699822c4
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207993"
---
# <a name="approve-and-confirm-purchase-orders"></a>Bestellungen genehmigen und bestätigen

[!include [banner](../includes/banner.md)]

Dieser Artikel beschreibt die Statuswerte einer Bestellung (PO) nach der Erstellung und den Effekt des Änderungsmanagements für Bestellungen.

Nachdem eine Bestellung (PO) erstellt wurde, muss diese möglicherweise einen Genehmigungsprozess durchlaufen. Nachdem der Kreditor der Bestellung zugestimmt hat, erhält die Bestellung den Status **Bestätigt**.

## <a name="approval-of-purchase-orders"></a>Genehmigung von Bestellungen
PO ohne Änderungsmanagement haben den Status **Genehmigt**, sobald sie erstellt wurden. POs mit Änderungsmanagement haben den Status **Entwurf**, wenn sie erstellt werden. Eine Bestellungen, die durch Umwandeln von geplanten Bestellungen aus dem Produktprogrammplan erstellt wurden, haben, unabhängig von den Einstellungen der Änderungsverwaltung, den Status **Genehmigt**. Eine Bestellung erstellt Lagertransaktionen nur bei Erreichen des Status **Genehmigt**. Daher wird der Bestand nicht als verfügbar für Reservierung angezeigt oder markiert, bis die Bestellung akzeptiert wird.

Sie aktivieren das Änderungsmanagement für POs über die Option **Änderungsmanagement aktivieren** auf der Seite **Beschaffungsparameter**. Wenn das Änderungsmanagement aktiviert ist, müssen POs einen Genehmigungsworkflow durchlaufen, nachdem sie abgeschlossen wurden. Supply Chain Management hat einen Workflow-Prozess-Editor, über den Sie einen Workflow für den Genehmigungsprozess definieren können. Dieser Workflow kann Regeln für automatische die Genehmigung, Regeln für die Zuweisung der Genehmigung von bestimmten POs und Regeln zur Eskalation eines Workflows mit länger ausstehender Genehmigung enthalten. Sie können den Änderungsmanagementprozess für alle Kreditoren oder für bestimmte Kreditoren aktivieren. Sie können den Prozess auch so einrichten, dass er für einzelne POs überschrieben werden kann.

Bei aktiviertem Änderungsmanagement durchlaufen POs sechs Genehmigungsstatuswerte (von **Entwurf** bis **Abgeschlossen**). Nachdem eine Bestellung genehmigt wurde, müssen Benutzer zur Bearbeitung die **Änderung anfordern**-Aktion nutzen.

| Genehmigungsstatus | Beschreibung                                                                      | Änderung anfordern aktiviert |
|-----------------|----------------------------------------------------------------------------------|---------------------------|
| Tratte           | Die Bestellung ist ein Entwurf und wurde nicht zur Genehmigung im PO-Workflow übermittelt.     | Nein                        |
| Wird überprüft       | Die Bestellung wurde zur Genehmigung im PO-Workflow übermittelt. Eine Genehmigung steht aus.       | Nein                        |
| Abgelehnt        | Die Bestellung wurde im Rahmen des Genehmigungsprozesses abgelehnt.                                 | Nein                        |
| Genehmigt        | Die Bestellung wurde genehmigt.                                                             | Ja                       |
| Bestätigt       | Die Bestellung wurde bestätigt. Eine Bestellung kann erst bestätigt werden, nachdem sie genehmigt wurde.        | Ja                       |
| Zum Abschluss gebracht       | Die Bestellung wurde endgültig festgelegt. Sie ist nun wertmäßig abgeschlossen und kann nicht mehr geändert werden. | Nein                        |

## <a name="confirming-purchase-orders"></a>Bestellungen bestätigen
POs mit dem Genehmigungsstatus **Genehmigt** können vor der Bestätigung weitere Schritte durchlaufen. Sie können beispielsweise eine Bestellungsanfrage an den Kreditor zu Preisen, Rabatten und Lieferdaten senden. In diesem Fall legen Sie die Bestellung mithilfe der **Einkaufsabfrage**-Aktion auf den Status **In externer Prüfung** fest.

Kreditoren, die für die Verwendung des Kreditorenportal eingerichtet sind, können Aufträge im Portal überprüfen und genehmigen oder ablehnen. Während dieser Überprüfung hat die Bestellung den Status **In externer Prüfung**. Der Kreditorenportal kann so konfiguriert werden, dass eine Bestätigung vom Kreditor automatisch den Auftrag in Supply Chain Management bestätigt. Alternativ können Sie eine Bestellung nach Bestätigung des Kreditors manuell bestätigen. Wenn ein Kreditor eine Bestellung ablehnt, wird die Ablehnung zusammen mit dem Grund für die Ablehnung sowie Vorschlägen zu Änderungen empfangen. In diesem Fall bleibt der Status der Bestellung auf **In externer Prüfung**.

Es ist auch Option zur Generierung einer Proforma-Bestätigung einer Bestellung vor der eigentlichen Bestätigung verfügbar. Diese Option erstellt einfach einen Bericht, den Sie für den Kreditor freigeben können. Sie erstellt keine Erfassungsinformationen.

Nachdem der Kreditor der Bestellung zugestimmt hat, ist der nächste Schritt die Einstufung der Bestellung als "Zugesagt". Sie können diesen Schritt über die Aktion **Bestätigung** oder **Bestätigen** durchführen. Beide Aktionen legen den Genehmigungsstatus der Bestellung auf **Bestätigt** fest. Die Bestätigung einer Bestellung löst zwei zusätzliche Prozesse aus:

-   Es wird eine Erfassung zur Speicherung einer Kopie der Bestätigung im System erstellt. Manchmal müssen Bestellungen geändert werden und zusätzliche Erfassungen werden nach der Bestätigung der aktualisierten Bestellung erstellt. In diesen Erfassungen können Sie den Verlauf der verschiedenen Versionen der bestätigten Bestellung anzeigen.
-   Wenn diese Funktionalität aktiviert wurde, werden Buchhaltungsverteilungen erstellt und Bestell- und Budgetprüfungen durchgeführt. Wenn eine Prüfung fehlschlägt, erhalten Sie eine Fehlermeldung, die besagt, dass die Bestellung geändert werden muss, bevor sie erneut bestätigt werden kann.

Ein Kreditor kann eine Sicherheit für die Zahlung für eine Bestellung anfordern. Es gibt verschiedene Methoden zum Bereitstellen dieser Garantie im Rahmen der Kreditorenprozesse. Angenommen, die **Vorauszahlung**-Aktion reserviert Mittel für die PO und diese Vorauszahlung wird für die Bestellung festgehalten.

## <a name="changing-purchase-orders"></a>Ändern von Bestellungen
In einigen Situationen müssen Sie möglicherweise eine Bestellung ändern nachdem der Genehmigungsstatus **Genehmigt** oder **Bestätigt** erreicht wurde.

Wenn die Bestellung über einen Änderungsmanagementprozess erstellt wurde, können Sie Änderungen über das erneute Aufrufen der Bestellung oder (wenn sie bereits genehmigt ist) über die Aktion **Änderung anfordern** durchführen. In diesem Fall wird der Genehmigungsstatus wieder auf **Entwurf** geändert, und Sie können die Bestellung ändern. Nachdem Sie die Änderungen abgeschlossen haben, müssen Sie die Bestellung möglicherweise zur erneuten Genehmigung senden. Sie können die Änderungen konfigurieren, die eine erneute Genehmigung erfordern. Nutzen Sie hierzu eine **Regel für die erneute Genehmigung von Bestellungen**-Richtlinienregel auf der **Einkaufsrichtlinien**-Seite.

Wenn ein Teil der bestellten Menge für eine Bestellposition geliefert wurde, können Sie die bestellte Menge nicht ändern, wenn die Bestellung im Zustand **Entwurf** ist. Sie können jedoch die Menge **Rest liefern** in der Zeile für die Bestellung ändern, die im Status **Entwurf** ist.

Wenn eine Bestellung bestätigt ist, können Sie diese nicht mehr löschen. Sie können jedoch die Gesamtmenge oder die verbleibende Menge einer Bestellung stornieren (solange die Menge noch nicht empfangen oder fakturiert wurde). Anschließend können Sie die Aktion **Abschließen** nutzen, um die Positionen zu stornieren und die weitere Verarbeitung zu verhindern. 


## <a name="canceling-purchase-orders"></a>Bestellungen stornieren

Eine Bestellung kann storniert werden, indem die Aktivität **Abbrechen** im Kopf verwendet wird.

Wenn die Menge teilweise erfasst oder fakturiert wurde oder eingegangen ist, können Sie nur die Restmenge stornieren, die nicht erfasst oder fakturiert wurde oder eingegangen ist. Die Auftragsmenge wird dann entsprechend reduziert. Wenn die Menge in der Position aktualisiert wird, wird der Positionsstatus ebenfalls aktualisiert. Beispielsweise ist die ursprüngliche Menge in der Position 5 und die Menge 3 geht ein. In diesem Fall kann nur eine Menge von zwei storniert werden. Die Position wird dann mit dem Status **Eingegangen** aktualisiert.

Wenn eine Restliefermenge der Auftragsposition hinzugefügt wird und sie die Menge in der Auftragsposition übersteigt, storniert die Aktivität **Abbrechen** nicht die Überschussmenge. Stattdessen verbleibt die Position im Status **Offener Auftrag**, da sie eine Restmenge hat. Beispielsweise ist die ursprüngliche Menge in der Position 5 und die verbleibende Liefermenge ist 7. Wenn der Auftrag storniert wird, wird eine Menge von fünf storniert und eine Menge von 2 verbleibt, wie Sie in den Lagerbuchungen sehen können.

Um die gesamte Menge einer Bestellposition zu stornieren, sollten Sie die verbleibende Liefermenge in der Position stornieren. Die Position wird dann mit dem Status **Storniert** aktualisiert.

Wenn eine Bestellung im Änderungsmanagement ist, muss jede Änderung, z. B. eine Stornierung des Auftrags oder des Lieferungsrestes, an das Workflowsystem übermittelt und genehmigt werden, bevor der Prozess vollständig durchgeführt werden kann und die Lagerbuchungen als storniert aktualisiert werden können.

<a name="additional-resources"></a>Zusätzliche Ressourcen
--------

[Übersicht über Bestellungen](purchase-order-overview.md)

[Bestellungen erstellen](purchase-order-creation.md)

[Produkteingang für Bestellungen](product-receipt-against-purchase-orders.md)

[Kreditorenrechnungen – Übersicht](../../finance/accounts-payable/vendor-invoices-overview.md)



