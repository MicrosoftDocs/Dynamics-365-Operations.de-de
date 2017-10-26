---
title: Genehmigen und Freigeben von Bestellungen
description: "Dieser Artikel beschreibt die Statuswerte einer Bestellung (PO) nach der Erstellung und den Effekt des Änderungsmanagements für Bestellungen."
author: FrankDahl
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 93143
ms.assetid: cd12a944-c52c-4579-a301-7abe1d237c72
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: 325807509601d02bad079e5ac60576e1f708e5cd
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="approve-and-confirm-purchase-orders"></a>Genehmigen und Freigeben von Bestellungen

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]

Dieser Artikel beschreibt die Statuswerte einer Bestellung (PO) nach der Erstellung und den Effekt des Änderungsmanagements für Bestellungen.

Nachdem eine Bestellung (PO) erstellt wurde, muss diese möglicherweise einen Genehmigungsprozess durchlaufen. Nachdem der Kreditor der Bestellung zugestimmt hat, erhält die Bestellung den Status **Bestätigt**.

## <a name="approval-of-purchase-orders"></a>Genehmigung von Bestellungen
PO ohne Änderungsmanagement haben den Status **Genehmigt** sobald sie erstellt wurden. POs mit Änderungsmanagement haben den Status **Entwurf** wenn sie erstellt werden. Eine Bestellungen, die durch Umwandeln von geplanten Bestellungen aus dem Produktprogrammplan erstellt wurden, haben, unabhängig von den Einstellungen der Änderungsverwaltung, den Status **Genehmigt**. Eine Bestellung erstellt Lagertransaktionen nur bei Erreichen des Status **Genehmigt**. Daher wird der Bestand nicht als verfügbar für Reservierung angezeigt oder markiert, bis die Bestellung akzeptiert wird.  

Sie aktivieren das Änderungsmanagement für POs über die Option **Änderungsmanagement aktivieren** auf der Seite **Beschaffungsparameter**. Wenn das Änderungsmanagement aktiviert ist, müssen POs einen Genehmigungsworkflow durchlaufen, nachdem sie abgeschlossen wurden. Microsoft Dynamics 365 for Finance and Operations hat einen Workflow-Prozess-Editor, über den Sie einen Workflow für den Genehmigungsprozess definieren können. Dieser Workflow kann Regeln für automatische die Genehmigung, Regeln für die Zuweisung der Genehmigung von bestimmten POs und Regeln zur Eskalation eines Workflows mit länger ausstehender Genehmigung enthalten. Sie können den Änderungsmanagementprozess für alle Kreditoren oder für bestimmte Kreditoren aktivieren. Sie können den Prozess auch so einrichten, dass er für einzelne POs überschrieben werden kann.  

Bei aktiviertem Änderungsmanagement durchlaufen POs sechs Genehmigungsstatuswerte (von **Entwurf** bis **Abgeschlossen**). Nachdem eine Bestellung genehmigt wurde, müssen Benutzer zur Bearbeitung die **Änderung anfordern**-Aktion nutzen.

| Genehmigungsstatus | Beschreibung                                                                      | Änderung anfordern aktiviert |
|-----------------|----------------------------------------------------------------------------------|---------------------------|
| Überblick           | Die Bestellung ist ein Entwurf und wurde nicht zur Genehmigung im PO-Workflow übermittelt.     | Nein                        |
| Wird überprüft       | Die Bestellung wurde zur Genehmigung im PO-Workflow übermittelt. Eine Genehmigung steht aus.       | Nein                        |
| Abgelehnt        | Die Bestellung wurde im Rahmen des Genehmigungsprozesses abgelehnt.                                 | Nein                        |
| Genehmigt        | Die Bestellung wurde genehmigt.                                                             | Ja                       |
| Bestätigt       | Die Bestellung wurde bestätigt. Eine Bestellung kann erst bestätigt werden, nachdem sie genehmigt wurde.        | Ja                       |
| Abgeschlossen       | Die Bestellung wurde endgültig festgelegt. Sie ist nun wertmäßig abgeschlossen und kann nicht mehr geändert werden. | Nein                        |

## <a name="confirming-purchase-orders"></a>Bestellungen bestätigen
POs mit dem Genehmigungsstatus **Genehmigt** können vor der Bestätigung weitere Schritte durchlaufen. Sie können beispielsweise eine Bestellungsanfrage an den Kreditor zu Preisen, Rabatten und Lieferdaten senden. In diesem Fall legen Sie die Bestellung mithilfe der **Einkaufsabfrage**-Aktion auf den Status **In externer Prüfung** fest.  

Kreditoren, die für die Verwendung des Kreditorenportal eingerichtet sind, können Aufträge im Portal überprüfen und genehmigen oder ablehnen. Während dieser Überprüfung hat die Bestellung den Status **In externer Prüfung**. Der Kreditorenportal kann so konfiguriert werden, dass eine Bestätigung vom Kreditor automatisch den Auftrag in Finance and Operations bestätigt. Alternativ können Sie eine Bestellung nach Bestätigung des Kreditors manuell bestätigen. Wenn ein Kreditor eine Bestellung ablehnt, wird die Ablehnung zusammen mit dem Grund für die Ablehnung sowie Vorschlägen zu Änderungen empfangen. In diesem Fall bleibt der Status der Bestellung auf **In externer Prüfung**.  

Es ist auch Option zur Generierung einer Proforma-Bestätigung einer Bestellung vor der eigentlichen Bestätigung verfügbar. Diese Option erstellt einfach einen Bericht, den Sie für den Kreditor freigeben können. Sie erstellt keine Erfassungsinformationen.  

Nachdem der Kreditor der Bestellung zugestimmt hat, ist der nächste Schritt die Einstufung der Bestellung als "Zugesagt". Sie können diesen Schritt über die Aktion **Bestätigung** oder **Bestätigen** durchführen. Beide Aktionen legen den Genehmigungsstatus der Bestellung auf **Bestätigt** fest. Die Bestätigung einer Bestellung löst zwei zusätzliche Prozesse aus:

-   Es wird eine Erfassung zur Speicherung einer Kopie der Bestätigung im System erstellt. Manchmal müssen Bestellungen geändert werden und zusätzliche Erfassungen werden nach der Bestätigung der aktualisierten Bestellung erstellt. In diesen Erfassungen können Sie den Verlauf der verschiedenen Versionen der bestätigten Bestellung anzeigen.
-   Wenn diese Funktionalität aktiviert wurde, werden Buchhaltungsverteilungen erstellt und Bestell- und Budgetprüfungen durchgeführt. Wenn eine Prüfung fehlschlägt, erhalten Sie eine Fehlermeldung, die besagt, dass die Bestellung geändert werden muss, bevor sie erneut bestätigt werden kann.

Ein Kreditor kann eine Sicherheit für die Zahlung für eine Bestellung anfordern. Es gibt verschiedene Methoden zum Bereitstellen dieser Garantie im Rahmen der Kreditorenprozesse. Angenommen, die **Vorauszahlung**-Aktion reserviert Mittel für die PO und diese Vorauszahlung wird für die Bestellung festgehalten.

## <a name="changing-purchase-orders"></a>Ändern von Bestellungen
In einigen Situationen müssen Sie möglicherweise eine Bestellung ändern nachdem der Genehmigungsstatus **Genehmigt** oder **Bestätigt** erreicht wurde.  

Wenn die Bestellung über einen Änderungsmanagementprozess erstellt wurde, können Sie Änderungen über das erneute Aufrufen der Bestellung oder (wenn sie bereits genehmigt ist) über die Aktion **Änderung anfordern** durchführen. In diesem Fall wird der Genehmigungsstatus wieder auf **Entwurf** geändert, und Sie können die Bestellung ändern. Nachdem Sie die Änderungen abgeschlossen haben, müssen Sie die Bestellung möglicherweise zur erneuten Genehmigung senden. Sie können die Änderungen konfigurieren, die eine erneute Genehmigung erfordern. Nutzen Sie hierzu eine **Regel für die erneute Genehmigung von Bestellungen**-Richtlinienregel auf der **Einkaufsrichtlinien**-Seite.  

Wenn ein Teil der bestellten Menge für eine Bestellposition geliefert wurde, können Sie die bestellte Menge nicht ändern. Sie können jedoch die **Rest liefern**-Menge der Position ändern. Anschließend können Sie die **Abschließen**-Aktion nutzen, um die Positionen zu stornieren und die weitere Verarbeitung zu verhindern. 

Wenn eine Bestellung bestätigt ist, können Sie diese nicht mehr löschen. Sie können jedoch die Gesamtmenge oder die verbleibende Menge einer Bestellung stornieren (solange die Menge noch nicht empfangen oder fakturiert wurde).

<a name="see-also"></a>Siehe auch
--------

[Überblick über Bestellungen](purchase-order-overview.md)

[Bestellungserstellung](purchase-order-creation.md)

[Produkteingang für Bestellungen](product-receipt-against-purchase-orders.md)

[Überblick über Kreditorenrechnungen](../../financials/accounts-payable/vendor-invoices-overview.md)




