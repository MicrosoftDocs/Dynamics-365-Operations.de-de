--- 
title: Mahnschreibensequenzen einrichten
description: Erstellen Sie mithilfe dieser Aufgabenanleitung eine Mahnschreibensequenz.
author: mikefalkner
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6331c3680169b305c4bfbfada4ba106b619be092
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-collection-letter-sequence"></a>Mahnschreibensequenzen einrichten

[!include[task guide banner](../../includes/task-guide-banner.md)]

Erstellen Sie mithilfe dieser Aufgabenanleitung eine Mahnschreibensequenz. Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet.

1. Wechseln Sie zu "Kredit und Inkasso" > "Einstellungen > "Mahnschreibensequenz einrichten".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Mahnschreibensequenz" eine Sequenzkennung ein, die die Reihenfolge darstellt. Sie wird verwendet, wenn Sie ein Buchungsprofil einrichten.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
    * Die Zahlungsbedingungen sind optional. Wenn Sie einen Wert hier eingeben, verwendet die Mahngebührenrechnung diese Zahlungsbedingungen anstelle der Zahlungsbedingungen, die beim Debitor gespeichert sind.  
5. Wählen Sie im Mahnschreibencode-Feld den Code für das erste Mahnschreiben aus, das Sie senden möchten.
    * Das erste Mahnschreiben wird gemäß dem Fälligkeitsdatum auf der Rechnung, der Toleranzperiode, die Sie im Feld "Tage" auf dieser Position eingegeben haben und anderen Informationen, die Sie auf dieser Position eingeben, erstellt.  
6. Geben Sie im Feld "Beschreibung" einen Wert ein.
    * Die Währung für die Gebühr ist standardmäßig die Währung des Debitors. Dieser Währungscode kann sich von der Rechnungswährung unterscheiden.  
7. Klicken Sie auf "Hinzufügen", um das nächste Mahnschreiben hinzuzufügen, das in der Reihenfolge gesendet wird.
    * In vielen Fällen ist das erste Mahnschreiben nur eine Warnung. Sie können Gebühren nach Bedarf hinzufügen.  
8. Wählen Sie im Mahnschreibencode-Feld das nächste Mahnschreiben aus, das in der Reihenfolge gesendet wird.
9. Geben Sie im Feld "Beschreibung" einen Wert ein.
10. Wählen Sie im Hauptkontofeld das Umsatzerlöskonto aus, das für Gebühren verwendet wird.
11. Geben Sie die Gebühr ein, die berechnet wird, wenn dieses Mahnschreiben gesendet wird.
12. Klicken Sie im Feld "Artikel-Mehrwertsteuergruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Wählen Sie eine Artikel-Mehrwertsteuergruppe aus, wenn Mehrwertsteuern auf die Gebühr berechnet werden müssen.  
13. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
14. Geben Sie den überfälligen Mindestsaldo ein, der erforderlich ist, bevor ein Mahnschreiben gesendet wird.
15. Geben Sie die Anzahl der Toleranztage ein, die Sie gestatten werden.
    * Dies ist die Anzahl von Tagen nach dem Fälligkeitsdatum, damit ein Mahnschreiben generiert werden kann. Das Fälligkeitsdatum, das für die Berechnung verwendet wird, hängt von der Position des Mahnschreibens in der Mahnschreibensequenz ab: ⦁ Die Toleranzperiode für Mahnschreiben 1 ist relativ zum Fälligkeitsdatum auf der Rechnung.  ⦁ Die Toleranzperiode für Mahnschreiben 2 und höhere ist relativ zum Datum, an dem das vorherige Mahnschreiben gebucht oder gedruckt wird, abhängig von der Auswahl im Feld "Mahnschreibencode aktualisieren" auf der Seite "Debitorenparameter".  
16. Klicken Sie auf "Hinzufügen", um das letzte Mahnschreiben in der Reihenfolge hinzuzufügen.
    * Sie können für eine Mahnschreibensequenz bis zu fünf Mahnschreibencodes hinzufügen.  
17. Wählen Sie im Mahnschreibencode-Feld das nächste Mahnschreiben aus, das in der Reihenfolge gesendet wird.
18. Geben Sie im Feld "Beschreibung" einen Wert ein.
19. Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.
20. Geben Sie eine Zahl in das Feld "Gebühr in Währung" ein.
21. Klicken Sie im Feld "Mehrwertsteuergruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
22. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
23. Geben Sie im Feld "Überfälliger Mindestsaldo" eine Zahl ein.
24. Geben Sie im Feld "Tage" eine Zahl ein.
25. Aktivieren Sie dieses Kontrollkästchen, um den Debitor von zusätzlichen Lieferungen und der Rechnungsstellung auszuschließen.
    * Damit das Konto entsperrt wird, wählen Sie im Feld "Rechnungsstellung und Lieferung gesperrt" der Seite "Debitoren" "Nein" aus.  
26. Erweitern Sie das Inforegister "Hinweis".
27. Geben Sie den Text ein, der im Mahnschreiben für den ausgewählten Mahnschreibencode angezeigt werden soll.
    * Sie können diesen Text in mehrere Sprachen mithilfe des Menüs "Übersetzungen" über dem Hinweisfeld übersetzen.  


