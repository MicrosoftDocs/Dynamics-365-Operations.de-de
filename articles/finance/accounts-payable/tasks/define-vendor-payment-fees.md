---
title: Gebühren für Kreditorenzahlung definieren
description: Richten Sie Kreditorenzahlungsgebühren ein.
author: abruer
ms.date: 02/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendPaymFee, VendPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c490bb4d15fa03742b12f337046f26976ab70d29
ms.sourcegitcommit: 3105642fca2392edef574b60b4748a82cda0a386
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2022
ms.locfileid: "8109830"
---
# <a name="define-vendor-payment-fees"></a>Gebühren für Kreditorenzahlung definieren

[!include [banner](../../includes/banner.md)]

Richten Sie Kreditorenzahlungsgebühren ein. Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet.

1. Wechseln Sie zu **Kreditorenkonten > Zahlungseinstellungen > Zahlungsgebühr**.
2. Klicken Sie auf **Neu**.
3. Geben Sie im Feld **Gebührenkennung** einen Wert ein.
    * Die **Gebührenkennung** sollte beschreiben, wann diese Gebühr verwendet wird, beispielsweise „Gebühr für Überweisung (elektronisch)“.  
4. Geben Sie im Feld **Name** einen Wert ein.
5. Geben Sie im Feld **Gebührenbeschreibung** einen Wert ein.
    * Fügen Sie eine Beschreibung hinzu, um weitere Informationen dazu bereitzustellen, wann die Gebühr veranschlagt wird.  
6. Wählen Sie im Feld **Belastung** entweder **Kreditor** oder **Sachkonto** aus.
    * **Sachkonto** wird verwendet, wenn die Gebühr zu Ihrer Organisation in Aufwand gebucht wird. **Kreditor** wird verwendet, wenn die Gebühr dem Kreditor veranschlagt wird.  
7. Geben Sie ein Hauptkonto ein, für das die Gebühr in Aufwand gebucht wird.
    * Diese Option ist nur verfügbar, wenn **Sachkonto** als Option für **Belastung** ausgewählt wurde.  
8. Wählen Sie die Erfassung aus, für die diese Gebühr verwendet werden kann. 
    * Für eine Kreditorenzahlungsgebühr würden Sie die Erfassung "Kreditorenzahlung" auswählen.  
9. Klicken Sie auf **Speichern**.
10. Klicken Sie auf **Zahlungsgebühreinstellungen**.
    * Fahren Sie fort zu den **Zahlungsgebühreneinstellungen**, um zu definieren, wann sich die Gebühr standardmäßig auf die Erfassung, die Sie ausgewählt haben, beziehen soll.  
11. Wählen Sie entweder **Tabelle**, **Gruppe** oder **Alle** aus.
    * **Tabelle** wird verwendet, um ein einzelnes Bankkonto auszuwählen, **Gruppe** wird verwendet, um eine Bankgruppe auszuwählen, und **Alle** wird verwendet, um diese Gebühreneinstellungen für alle Bankkonten zu verwenden.  
12. Wählen Sie entweder eine Bankgruppe oder ein Bankkonto aus.
    * Die Suche wird Bankgruppe anzeigen, wenn Sie **Gruppe** ausgewählt haben, und wird Bankkonten anzeigen, wenn Sie **Tabelle** ausgewählt haben.  
13. Wählen Sie die Zahlungsmethode aus, für wann diese Gebühr veranschlagt wird.
14. Wählen Sie die **Zahlungsspezifikation** für die ausgewählte Zahlungsmethode aus.
    * Die **Zahlungsspezifikation** wird mit Methoden des elektronischen Geldverkehrs für Zahlungen verwendet.  
15. Wählen Sie aus, ob die Gebühr ein Prozentsatz, ein Betrag oder ein Intervall ist.
16. Geben Sie den Prozentsatz oder Betrag der Gebühr ein.
    * Wenn die **Gebühr** ein Prozentsatz ist, geben Sie den Prozentsatz ein. Wenn die **Gebühr** ein Betrag ist, geben Sie den Betrag der Gebühr ein. Wenn die **Gebühr** ein Intervall ist, verwenden Sie die Registerkarte **Intervall**, um die gestaffelten Gebühren zu definieren.  
17. Wählen Sie im Feld **Währung der Gebühr** die Währung aus, in der die Gebühr berechnet wird.
    * Diese Währung ist für die Gebühr. Die Zahlungswährung wird verwendet, um zu definieren, wann die Gebührenregel basierend auf der Währung der Zahlung veranschlagt werden soll. Beispielsweise erhebt Ihre Bank möglicherweise eine Gebühr, wenn eine Zahlung in EUR geleistet wird, aber bei allen anderen Zahlungen wird keine Gebühr veranschlagt.  
18. Klicken Sie auf **Speichern**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
