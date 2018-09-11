--- 
title: "Übersicht Debitorenzahlung"
description: "Dieser Aufgabenleitfaden führt durch verschiedene Methoden zum Eingeben von Debitorenzahlungen."
author: kweekley
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTable, CustPaymEntry, CustTableLookup, LedgerJournalTransCustPaym, CustOpenTrans, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e6e10d0d0a05b0594ba5cf6a77f474b461bd9dca
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="customer-payment-overview"></a>Übersicht Debitorenzahlung

[!include [task guide banner](../../includes/task-guide-banner.md)]

Dieser Aufgabenleitfaden führt durch verschiedene Methoden zum Eingeben von Debitorenzahlungen. Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet.

1. Wechseln Sie zu "Debitoren" > "Zahlungen" > "Zahlungserfassung".
2. Klicken Sie auf "Neu".
3. Wählen Sie die Zahlungserfassung aus, in der die Debitorenzahlungen gespeichert werden sollen.
4. Wählen Sie die Erfassung aus, oder geben Sie sie manuell ein.
5. Klicken Sie auf "Debitorenzahlungen eingeben".
    * "Debitorenzahlungen eingeben" wird verwendet, um jeweils eine Debitorenzahlung zu erfassen. Sie geben die Zahlungsinformationen oben ein, anschließend können Sie auf derselben Seite die Rechnungen markieren, die anhand der Zahlung bezahlt wurden.  
6. Geben Sie den Debitor ein, von dem Sie die Zahlung erhalten haben.
    * Wenn Sie den Debitor nicht kennen, aber wissen, dass eine Buchung bezahlt wurde, können Sie das Buchungsfeld verwenden, um die Zahlung einzugeben. Geben Sie die Rechnung ins Transaktionsfeld ein oder wählen Sie sie aus. Der Debitor wird automatisch auf den Standardwert gesetzt, wenn Sie die Buchung ausgewählt haben.  
7. Geben Sie im Feld "Zahlungsreferenz" eine Zahlungsreferenz ein.
    * Die Zahlungsreferenz könnte die Schecknummer oder Referenz des Debitors von der elektronischen Zahlung des Debitors sein. Die Zahlungsreferenz ist nur erforderlich, wenn Sie angegeben haben, dass die Zahlung auf einem Einzahlungsbeleg enthalten sein soll.  
8. Wählen Sie aus, ob die Zahlung in einem Einzahlungsbeleg einbezogen ist. 
9. Hier können Sie den Betrag der Debitorenzahlung eingeben.
    * Der Zahlungsbetrag wird nicht standardmäßig festgelegt. Er muss manuell eingegeben werden.  
10. Markieren Sie die Rechnungen, die vom Debitor bezahlt wurden.
    * Wenn es sich bei der Zahlung um eine Vorauszahlung handelt, müssen Sie keine Rechnungen für den Ausgleich markieren. Die Zahlung kann dennoch gespeichert und gebucht werden. Der Ausgleich einer Rechnung kann zu einem späteren Zeitpunkt erfolgen.  
11. Geben Sie den Betrag der Zahlung ein, der mit der ausgewählten Rechnunge ausgeglichen werden soll. 
    * Dieses Feld kann verwendet werden, wenn die Zahlung für eine Teilzahlung ist. Wenn Sie keinen Betrag eingeben, wird automatisch der auszugleichende Betrag für Sie bestimmt.  
12. Klicken Sie auf "In Erfassung speichern".
    * Bevor Sie die Zahlung in der Erfassung speichern, vergewissern Sie sich, dass das Gegenkonto definiert ist. Beim Speichern in der Erfassung wird die Zahlung gespeichert und in die Erfassung verschoben. Sie können dann mit dem Eingeben der nächsten Zahlung fortfahren.  
13. Schließen Sie die Seite.
14. Klicken Sie auf "Positionen".
    * Beim Öffnen von Positionen sehen Sie alle Zahlungen, die Sie auf der Seite "Debitorenzahlungen eingeben" erfasst und in der Erfassung gespeichert haben. Sie können diese Seite auch nutzen, um neue Debitorenzahlungen einzugeben oder bestehende Debitorenzahlungen zu bearbeiten, bevor sie gebucht werden.  
15. Klicken Sie auf "Neu", um eine weitere Zahlung zu erstellen. 
16. Wählen Sie den Debitor aus, von dem Sie die Zahlung erhalten haben.
    * Wenn Sie den Debitor nicht kennen, jedoch wissen, dass durch die Zahlung eine Rechnung bezahlt wurde, verwenden Sie das Rechnungsfeld, um die Rechnung manuell einzugeben oder auszuwählen. Der Debitor wird standardmäßig festgelegt, nachdem die Rechnung ausgewählt ist.  
17. Klicken Sie auf "Buchungen ausgleichen", um Rechnungen zu markieren, die bezahlt wurden.
    * Sie müssen die Zahlung keinen Rechnungen zuordnen. Wenn es sich um eine Vorauszahlung handelt oder Sie nicht wissen, welche Rechnung bezahlt wurde, können Sie die Zahlung eingeben und buchen. Die Zahlung kann einer Rechnung zu einem späteren Zeitpunkt zugeordnet werden.  
18. Markieren Sie bezahlte Rechnungen. 
19. Geben Sie den Betrag der Zahlung ein, der mit der ausgewählten Rechnung ausgeglichen werden soll.
20. Klicken Sie auf "OK".
21. Geben Sie im Feld "Zahlungsreferenz" eine Zahlungsreferenz ein.  
    * Die Zahlungsreferenz ist nur erforderlich, wenn Sie angegeben haben, dass die Zahlung auf einem Einzahlungsbeleg enthalten sein soll.  
22. Buchen Sie die Debitorenzahlungen. 


