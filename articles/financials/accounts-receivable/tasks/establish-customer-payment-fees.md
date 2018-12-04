--- 
title: "Debitorenzahlungsgebühren einrichten"
description: "Erstellen Sie Zahlungsgebühren für Debitorenzahlungen."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPaymFee, CustPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 659f4560747cea73c61a9b748a980946ca252bd6
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="establish-customer-payment-fees"></a>Debitorenzahlungsgebühren einrichten

[!include [task guide banner](../../includes/task-guide-banner.md)]

Erstellen Sie Zahlungsgebühren für Debitorenzahlungen.

Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet.

1. Wechseln Sie zu "Debitoren" > "Zahlungseinstellungen" > "Zahlungsgebühr".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Gebührenkennung" eine Gebührenkennung ein.
    * Die "Gebührenkennung" wird auf Zahlungserfassungen angezeigt, damit sind sie beschreibend, um zu verstehen, welche Gebühr veranschlagt wird.  
4. Geben Sie im Feld "Name" einen Gebührennamen ein.
5. Geben Sie im Feld "Gebührenbeschreibung" eine Beschreibung für die Gebühr ein.
6. Wählen Sie aus, ob der Debitor oder ein Sachkonto mit der Gebühr belastet wird.
    * Wenn die Gebühr für den Debitor veranschlagt wird, wählen Sie "Debitor" aus. Wenn die Gebühr für Ihre Organisation als Ausgaben veranschlagt wird, wählen Sie "Sachkonto" aus. Wählen Sie für diese Aufgabe "Debitor" aus.  
7. Wählen Sie den Erfassungstyp aus, der diese Zahlungsgebühr verwenden kann.
    * Wenn diese Gebühren für Debitorenzahlungen verwendet werden, wird der Erfassungstyp wahrscheinlich "Debitorenzahlung" sein.  
8. Klicken Sie auf "Speichern".
9. Klicken Sie auf "Zahlungsgebühreinstellungen".
    * Die Zahlungsgebühreneinstellungen werden verwendet, um die Kriterien zu definieren, wann die Zahlungsgebühr veranschlagt wird.  So können Sie beispielsweise definieren, dass die Gebühr berechnet wird, wenn das Bankkonto USMF-OPERATION ist und die Zahlungsmethode per Scheck ist.  
10. Wählen Sie entweder "Tabelle", "Gruppe" oder "Alle" aus, um zu definieren, welche Bankkonten für diese Gebühr bewertet werden.
    * Wenn Sie "Alle" auswählen, könnte für alle Bankkonten diese Gebühr veranschlagt werden.  Wenn Sie "Tabelle" auswählen, kann nur für das Bankkonto, das Sie auswählen, diese Gebühr veranschlagt werden. Wenn Sie "Gruppe" auswählen, könnte nur für Bankkonten in der ausgewählten Bankgruppe diese Gebühr veranschlagt bewertet werden.  
11. Wählen Sie entweder eine Bankgruppe oder ein Bankkonto aus.
    * Wenn Sie "Tabelle" ausgewählt haben, zeigt die Suche Bankkonten an. Wenn Sie "Gruppe" ausgewählt haben, zeigt die Suche Bankgruppen an.  
12. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
13. Wählen Sie die "Zahlungsmethode" aus, für die diese Gebühr veranschlagt wird.
    * Beispielsweise veranschlagen Sie möglicherweise eine Gebühr für Ihre Debitoren, wenn sie Zahlungen als Scheck senden, anstatt als elektronische Zahlung.  
14. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
15. Falls relevant, geben Sie eine Zahlungswährung ein.
    * Die Zahlungswährung wird als zusätzliches Kriterien dafür verwendet, ob die Gebühr veranschlagt wird.  Beispielsweise erhebt möglicherweise Ihrer Bank eine zusätzliche Gebühr für Zahlungseingänge in der USD-Währung, da sie normalerweise ihre Geschäfte nur in der EUR-Währung abwickelt.  
16. Wählen Sie aus, ob die Gebühr ein Prozentsatz, ein Betrag oder ein Intervall ist.
17. Geben Sie entweder Prozentsatz oder Betrag der Gebühr ein.
    * Wenn das Feld "Prozentsatz/Betrag" die Bezeichnung "Prozent" hat, ist der Wert, den Sie hier eingeben, ein Prozentsatz. Wenn das Feld "Prozentsatz/Betrag" die Bezeichnung "Betrag" hat, ist der Wert, den Sie hier eingeben, ein Betrag. Wenn das Feld "Prozentsatz/Betrag" die Bezeichnung "Intervall" hat, verwenden Sie die Registerkarte "Intervall", um die Ebenen zu definieren.  
18. Wählen Sie im Feld "Gebührenwährung" die Währung der Gebühr aus.
    * Dies ist die Währung, in der die Gebühr erstellt wird.  
19. Klicken Sie auf "Speichern".


