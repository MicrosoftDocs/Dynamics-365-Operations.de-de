---
title: Aufträge als Direktlieferungen versenden
description: Dieses Thema zeigt, wie eine Direktauslieferung für einen Auftrag erstellt wird.
author: omulvad
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, PurchCreateFromSalesOrder, VendAccountItemLookup, SalesTableReferences, PurchTable, PurchEditLines, PurchTableReferences, MCRDropShipWorkbench
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 81ebd845d9900d891b17618b3719d45060a1968f
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148422"
---
# <a name="ship-orders-as-direct-deliveries"></a>Aufträge als Direktlieferungen versenden

[!include [banner](../../includes/banner.md)]

Dieses Thema zeigt, wie eine Direktauslieferung für einen Auftrag erstellt wird. Sie verwenden die Direktlieferung, wenn Sie Waren an den Debitor direkt vom Kreditor versenden möchten, anstatt sie zunächst an den eigenen Lagerort zu versenden. Sie können diese Prozedur im Demodatenunternehmen USMF oder für Ihre eigenen Daten ausführen. Um die zweite Unteraufgabe "Erstellen Sie Direktlieferungen von der Workbench" erfolgreich abzuschließen, stellen Sie sicher, dass der Artikel, den Sie im Auftrag ausgewählt haben, einem standardmäßigen Kreditoren zugeordnet ist, der im Einkauf-Inforegister des "Freigegebenen Produktmasters" angegeben ist.

## <a name="set-an-individual-order-for-direct-delivery"></a>Legen Sie einen einzelnen Auftrag für die Direktlieferung fest
1. Wechseln Sie zu **Navigationsbereich > Module > Debitoren > Aufträge > Alle Aufträge**.
2. Wählen Sie **Neu** aus.
3. Geben Sie im Feld **Debitorenkonto** einen Wert ein, oder wählen Sie einen Wert aus, und wählen Sie dann **OK**.
4. Geben Sie Werte in die Felder **Artikelnummer** und **Standort** ein, oder wählen Sie Werte aus, und wählen Sie dann **Speichern**.
5. Wählen Sie im Aufgabenbereich **Auftrag** und dann **Direktlieferung** aus. Die Seite "Lieferung erstellen" zeigt alle offenen Auftragspositionen an, wie vom Auftrag kopiert. Sie können die Auftragsdetails prüfen und, falls erforderlich, zudem Details wie die Bestellmenge und Preisgestaltungsbedingungen modifizieren, bevor Sie die Direktlieferung erstellen.  
6. Wählen Sie **Ja** im Feld **Alle übernehmen** aus.
    - Wenn Sie eine Direktlieferung für nur eine Teilmenge der Auftragspositionen generieren möchten, wählen Sie diese einzeln aus.  
    - Das Feld **Kreditorenkonto** ist bereits möglicherweise mit einer Kreditorennummer ausgefüllt. Wenn der Standardkreditor für das Produkt (in der zugehörigen Artikeldeckung) eingerichtet ist, wird dieser Kreditor in die Position kopiert. Andernfalls muss ein Kreditor manuell eingegeben werden. In diesem Beispiel wählen wir einen neuen Kreditor im nächsten Schritt aus, sogar wenn dieser bereits ausgefüllt ist.   
7. Geben Sie im Feld **Kreditorenkonto** einen Wert ein, oder wählen Sie einen Wert aus, und wählen Sie dann **OK**. Die Nachricht informiert Sie darüber, dass die Bestellung nun erstellt wurde.   
8. Erweitern Sie den Abschnitt **Positionsdetails**.
9. Wählen Sie die Registerkarte **Lieferung** aus, und vergewissern Sie sich, dass das Feld **Direktlieferung** auf **Ja** festgelegt ist.
10. Wählen Sie im Aktivitätsbereich **Allgemein** aus.
11. Wählen Sie **Zugeordnete Aufträge** aus.
12. Wählen Sie den Link im Feld **Bestellung** aus.
13. Erweitern Sie den Bereich **Positionsdetails**, und wählen Sie die Registerkarte **Adresse** aus.
    - Die Lieferadresse für diese Bestellposition ist die Lieferadresse des Debitors und nicht die Adresse des Unternehmens.  
    - Wenn Sie die Lieferadresse entweder in der Bestellposition oder der ursprünglichen Auftragsposition ändern, wird die Adresse in der entsprechenden Auftragsposition automatisch aktualisiert.  
14. Wählen Sie die Registerkarte **Lieferung** aus.
    - Wie die Auftragsposition wird der zugeordnete Bestellpositionstyp auch auf "Direktlieferung" festgelegt.  
    - Das Lieferdatum und das bestätigte Lieferdatum der Bestellposition werden entsprechend dem angeforderten Wareneingangsdatum und dem bestätigten Wareneingangsdatum der ursprünglichen Auftragsposition festgelegt.   
    - Wenn Sie beliebige Datumsangaben entweder in der Bestellposition oder der Verkaufsposition aktualisieren, werden die Daten im entsprechenden Auftrag automatisch aktualisiert.     
    - Die zur direkten Lieferung der Waren an den Debitor festgelegte Bestellung wird mit dem ursprünglichen Auftrag anhand einer speziellen Zuordnung verknüpft. Diese Zuordnung erlegt die Regel auf, dass die Lieferscheinaktualisierung des Auftrags nicht aus dem Auftrag selbst ausgeführt werden kann, sondern so über die Bestellung erfolgen muss. Die Debitorenrechnungsstellung muss jedoch über den Auftrag ausgeführt werden.  
15. Wählen Sie im Aktivitätsbereich **Einkauf** aus.
16. Wählen Sie **Bestätigung** aus.
17. Wählen Sie **OK**.
18. Wählen Sie im Aktivitätsbereich **Wareneingang** aus.
19. Wählen Sie **Produktzugang** aus.
20. Geben Sie im Feld **Produktzugang** einen Wert ein.
21. Wählen Sie **OK**.
22. Wählen Sie im Aktivitätsbereich **Allgemein** aus.
23. Wählen Sie **Zugeordnete Aufträge** aus, und markieren Sie den gewünschten Datensatz.
    - Nachdem die Bestellung als "Eingegangen" aktualisiert wurde, oder in anderen Worten, nachdem der Kreditor die Waren an die Adresse des Debitors geliefert hat, wird der Status des ursprünglichen Auftrags automatisch als "Geliefert" aktualisiert.  
    - Der Auftrag kann nun fakturiert werden.    
24. Wählen Sie **OK**.
25. Schließen Sie die Seite.
26. Wählen Sie **OK**. Schließen Sie die Seiten, und kehren Sie zur Startseite zurück.

## <a name="create-direct-deliveries-from-the-workbench"></a>Erstellen Sie direkte Lieferungen über die Workbench
1. Wechseln Sie zu **Navigation > Module > Debitoren > Aufträge > Alle Aufträge**.
2. Wählen Sie **Neu** aus.
3. Geben Sie im Feld **Debitorenkonto** einen Wert ein, oder wählen Sie einen Wert aus, und wählen Sie dann **OK**.
4. Geben Sie in den Feldern **Artikelnummer** und **Standort** einen Wert ein, oder wählen Sie einen Wert aus.
5. Erweitern Sie den Abschnitt **Positionsdetails**, und wählen Sie dann die Registerkarte **Lieferung** aus. Anstatt eine Direktlieferung wie im vorherigen Verfahren als Teil der Auftragsverarbeitung zu erstellen, können Sie diese Aufgabe einem Einkäufer übergeben. Um die Auftragsposition in den Direktlieferungshandlungsprozess einzubeziehen, müssen Sie die Position für die Direktlieferung markieren.  
6. Wählen Sie **Ja** im Feld **Direktlieferung** aus.
    - Wenn der Artikel bereits für Direktlieferung standardmäßig eingerichtet wurde, wird das Feld automatisch auf "Ja" bei der Auftragspositionserfassung festgelegt. Sie können einen Artikel für Direktlieferung im Master des "Freigegebenen Produkt" einrichten, indem Sie die Option "Direktlieferung" mit "Ja" festlegen sowie einen standardmäßigen Direktlieferungslagerort auswählen.  
    - Da die Bestellung noch nicht erstellt wurde, wird der Direktlieferungsstatus auf „Direkt zu liefern“ festgelegt.   
7. Wählen Sie **Speichern**.
8. Schließen Sie Seiten, bis Sie zur Startseite zurückkehren.
9. Geben Sie `Direct delivery` in das Suchfeld ein.
    - Die Direktlieferungsseite fungiert als eine workbench, die dem Einkaufsvertreter einen Überblick über alle Auftragspositionen bereitstellt, die direkt geliefert werden sollen, und dadurch ermöglicht, die jeweiligen Bestellungen zu erstellen. Darüber hinaus können sie die offenen Direktlieferungslieferaufträge und die bestätigten Aufträge auf den Registerkarten "Bestätigung" und "Lieferung" anzeigen.  
    - Nachdem Sie einen Direktlieferungsauftrag erstellt haben, wurde er automatisch zur Registerkarte „Bestätigung” verschoben. Sie können wählen, den Auftrag direkt von dieser Seite aus zu bestätigen. Wenn der Einkauf bestätigt ist, wird er automatisch auf die Registerkarte "Lieferung" verschoben, von der aus Sie seinen Zugang erfassen können.  

