--- 
title: "Aufträge als Direktlieferungen versenden"
description: "Diese Prozedur zeigt, wie eine Direktauslieferung für einen Auftrag erstellt wird."
author: omulvad
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f674de4877dd2d6e6f1ff02f16a68cb4805d9864
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="ship-orders-as-direct-deliveries"></a>Aufträge als Direktlieferungen versenden

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Diese Prozedur zeigt, wie eine Direktauslieferung für einen Auftrag erstellt wird. Sie verwenden die Direktlieferung, wenn Sie Waren an den Debitor direkt vom Kreditor versenden möchten, anstatt sie zunächst an den eigenen Lagerort zu versenden. Sie können diese Prozedur im Demodatenunternehmen USMF oder für Ihre eigenen Daten ausführen. Um die zweite Unteraufgabe "Erstellen Sie Direktlieferungen von der Workbench" erfolgreich abzuschließen, stellen Sie sicher, dass der Artikel, den Sie im Auftrag ausgewählt haben, einem standardmäßigen Kreditoren zugeordnet ist, der im Einkauf-Inforegister des "Freigegebenen Produktmasters" angegeben ist.


## <a name="set-an-individual-order-for-direct-delivery"></a>Legen Sie einen einzelnen Auftrag für die Direktlieferung fest
1. Wechseln Sie zu "Alle Aufträge".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Debitorenkonto" einen Wert ein oder wählen Sie einen Wert aus.
    * Wenn Sie USMF verwenden, können Sie Konto US-001 auswählen.  
4. Klicken Sie auf "OK".
5. Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.
    * Wenn Sie USMF verwenden, können Sie Artikel T0020 auswählen.  
6. Klicken Sie auf "Speichern".
7. Klicken Sie im Aktivitätsbereich auf "Auftrag".
8. Klicken Sie auf "Direktlieferung".
    * Die Seite "Lieferung erstellen" zeigt alle offenen Auftragspositionen an, wie vom Auftrag kopiert. Sie können die Auftragsdetails prüfen und, falls erforderlich, zudem Details wie die Bestellmenge und Preisgestaltungsbedingungen modifizieren, bevor Sie die Direktlieferung erstellen.  
9. Wählen Sie im Feld "Alle übernehmen" "Ja" aus.
    * Wenn Sie eine Direktlieferung für nur eine Teilmenge der Auftragspositionen generieren möchten, wählen Sie diese einzeln aus.  
    * Das Feld "Kreditorenkonto" ist bereits möglicherweise mit einer Kreditorennummer ausgefüllt. Wenn der Standardkreditor für das Produkt (in der zugehörigen Artikeldeckung) eingerichtet ist, wird dieser Kreditor in die Position kopiert. Andernfalls muss ein Kreditor manuell eingegeben werden. In diesem Beispiel wählen wir einen neuen Kreditor im nächsten Schritt aus, sogar wenn dieser bereits ausgefüllt ist.   
10. Geben Sie im Feld "Kreditorenkonto" einen Wert ein, oder wählen Sie einen Wert aus.
    * Wenn Sie USMF verwenden, können Sie Konto 1001 auswählen.  
11. Klicken Sie auf "OK".
    * Die Nachricht informiert Sie darüber, dass die Bestellung nun erstellt wurde.   
12. Erweitern Sie den Abschnitt "Positionsdetails".
13. Klicken Sie auf die Registerkarte "Lieferung".
    * Das Feld "Direktlieferung" ist nun auf "Ja" festgelegt.  
    * Der Direktlieferungsstatus zeigt die erstellte Bestellung.   
14. Klicken Sie im Aktivitätsbereich auf "Allgemein".
15. Klicken Sie auf "Zugeordnete Aufträge".
16. Klicken Sie, um dem Link im Feld "Bestellung" zu folgen.
17. Erweitern Sie den Abschnitt "Positionsdetails".
18. Klicken Sie auf die Registerkarte "Adresse".
    * Beachten Sie, dass die Lieferadresse für diese Bestellposition die Lieferadresse des Debitors und nicht die Adresse des Unternehmens ist.  
    * Wenn Sie die Lieferadresse entweder in der Bestellposition oder der ursprünglichen Auftragsposition ändern, wird die Adresse in der entsprechenden Auftragsposition automatisch aktualisiert.  
19. Klicken Sie auf die Registerkarte "Lieferung".
    * Wie die Auftragsposition wird der zugeordnete Bestellpositionstyp auch auf "Direktlieferung" festgelegt.  
    * Das Lieferdatum und das bestätigte Lieferdatum der Bestellposition werden entsprechend dem angeforderten Wareneingangsdatum und dem bestätigten Wareneingangsdatum der ursprünglichen Auftragsposition festgelegt.   
    * Wenn Sie beliebige Datumsangaben entweder in der Bestellposition oder der Verkaufsposition aktualisieren, werden die Daten im entsprechenden Auftrag automatisch aktualisiert.     
    * Die zur direkten Lieferung der Waren an den Debitor festgelegte Bestellung wird mit dem ursprünglichen Auftrag anhand einer speziellen Zuordnung verknüpft. Diese Zuordnung erlegt die Regel auf, dass die Lieferscheinaktualisierung des Auftrags nicht aus dem Auftrag selbst ausgeführt werden kann, sondern so über die Bestellung erfolgen muss. Die Debitorenrechnungsstellung muss jedoch über den Auftrag ausgeführt werden.  
20. Klicken Sie im Aktivitätsbereich auf "Einkauf".
21. Klicken Sie auf Bestätigung.
22. Klicken Sie auf "OK".
23. Klicken Sie im Aktivitätsbereich auf "Empfangen".
24. Klicken Sie auf "Produktzugang".
25. Geben Sie im Feld "Produktzugang" einen Wert ein.
26. Klicken Sie auf "OK".
27. Klicken Sie im Aktivitätsbereich auf "Allgemein".
28. Klicken Sie auf "Zugeordnete Aufträge".
29. Markieren Sie in der Liste die ausgewählte Zeile.
    * Nachdem die Bestellung als "Eingegangen" aktualisiert wurde, oder in anderen Worten, nachdem der Kreditor die Waren an die Adresse des Debitors geliefert hat, wird der Status des ursprünglichen Auftrags automatisch als "Geliefert" aktualisiert.  
    * Der Auftrag kann nun fakturiert werden.    
30. Klicken Sie auf "OK".
31. Schließen Sie die Seite.
32. Klicken Sie auf "OK".

## <a name="create-direct-deliveries-from-the-workbench"></a>Erstellen Sie direkte Lieferungen über die Workbench
1. Schließen Sie die Seite.
2. Schließen Sie die Seite.
3. Wechseln Sie zu "Alle Aufträge".
4. Klicken Sie auf "Neu".
5. Geben Sie im Feld "Debitorenkonto" einen Wert ein oder wählen Sie einen Wert aus.
6. Klicken Sie auf "OK".
7. Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.
8. Erweitern Sie den Abschnitt "Positionsdetails".
9. Klicken Sie auf die Registerkarte "Lieferung".
    * Anstatt eine Direktlieferung wie im vorherigen Verfahren als Teil der Auftragsverarbeitung zu erstellen, können Sie diese Aufgabe einem Einkäufer übergeben. Um die Auftragsposition in den Direktlieferungshandlungsprozess einzubeziehen, müssen Sie die Position für die Direktlieferung markieren.  
10. Wählen Sie "Ja" im Feld "Direktlieferung".
    *   Wenn der Artikel bereits für Direktlieferung standardmäßig eingerichtet wurde, wird das Feld automatisch auf "Ja" bei der Auftragspositionserfassung festgelegt. Sie können einen Artikel für Direktlieferung im Master des "Freigegebenen Produkt" einrichten, indem Sie die Option "Direktlieferung" mit "Ja" festlegen sowie einen standardmäßigen Direktlieferungslagerort auswählen.  
    * Da die Bestellung noch nicht erstellt wurde, wird der Direktlieferungsstatus auf "Direkt zu liefern" festgelegt.   
11. Schließen Sie die Seite.
12. Schließen Sie die Seite.
13. Wechslen Sie dann zu "Direktlieferung".
    * Die Direktlieferungsseite fungiert als eine workbench, die dem Einkaufsvertreter einen Überblick über alle Auftragspositionen bereitstellt, die direkt geliefert werden sollen, und dadurch ermöglicht, die jeweiligen Bestellungen zu erstellen. Darüber hinaus können sie die offenen Direktlieferungslieferaufträge und die bestätigten Aufträge auf den Registerkarten "Bestätigung" und "Lieferung" anzeigen.   
14. Klicken Sie auf "Direktlieferung erstellen".
15. Klicken Sie auf die Registerkarte "Bestätigung".
    * Nachdem Sie einen Direktlieferungsauftrag erstellt haben, wurde er automatisch zur Registerkarte „Bestätigung” verschoben. Sie können wählen, den Auftrag direkt von dieser Seite aus zu bestätigen. Wenn der Einkauf bestätigt ist, wird er automatisch auf die Registerkarte "Lieferung" verschoben, von der aus Sie seinen Zugang erfassen können.  


