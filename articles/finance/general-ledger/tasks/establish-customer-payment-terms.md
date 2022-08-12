---
title: Debitorenzahlungsbedingungen einrichten
description: Diese Prozedur definiert eine Skonto- und Fälligkeitsdatumseinstellung.
author: aprilolson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PaymDay, PaymTerm, CashDisc
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6069d28d84ab1705fd62a33cea7e0b923f0e0705
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9065707"
---
# <a name="establish-customer-payment-terms"></a>Debitorenzahlungsbedingungen einrichten

[!include [banner](../../includes/banner.md)]

Diese Prozedur definiert eine Skonto- und Fälligkeitsdatumseinstellung. Für diese Aufgabenanleitung wird das Demo-Unternehmen USMF verwendet.

1. Wechseln Sie zu **Navigationsbereich > Module > Debitorenkonten > Zahlungseinrichtung > Zahlungstage**. Die Einstellungen für die **Zahlungsbedingungen** werden für **Debitoren** und **Kreditoren** freigegeben. Wenn Sie diese im Modul definieren, ist dies auch im anderen Modul verfügbar. Für diesen Aufgabenleitfaden werden alle Zahlungsbedingungen unter **Debitoren** eingerichtet.
2. Klicken Sie auf **Neu**. Erstellen Sie einen Zahlungstag, wenn Ihre Zahlungsbedingungen einen bestimmten Wochentag (Montag, Dienstag, usw.) oder ein bestimmtes Datum des Monats (5., 10., usw.) erfordern. 
3. Geben Sie im Feld **Zahlungstag** eine Kennung ein.
4. Geben Sie im Feld **Beschreibung** eine kurze Beschreibung den Zahlungstag ein.
5. Wählen Sie im Feld **Woche/Monat** entweder „Woche“ oder „Monat“ aus. Wenn Sie einen Wochentag eingeben möchten, wie beispielsweise Montag, wählen Sie "Woche" aus. Wenn Sie ein Datum im Monat eingeben möchten, wie beispielsweise der 10., wählen Sie "Monat" aus. Wählen Sie "Monat" für dieses Beispiel aus. 
6. Geben Sie im Feld **Tag des Monats** ein Datum ein. Das Datum sollte als Zahl eingegeben werden, wie beispielsweise "10", und nicht als "10.". 
7. Klicken Sie auf **Speichern**.
8. Schließen Sie die Seite.
9. Wechseln Sie zu **Navigationsbereich > Module > Debitorenkonten > Zahlungseinrichtung > Zahlungsbedingungen**.
10. Klicken Sie auf **Neu**. **Zahlungsbedingungen** – Legen Sie fest, wie die Fälligkeitstermine berechnet werden sollen. Die Skontodatumseinstellungen werden auf einer separaten Seite definiert. 
11. Geben Sie im Feld **Zahlungsbedingungen** eine Kennung ein.
12. Geben Sie im Feld **Beschreibung** eine Beschreibung ein.
13. Wählen Sie eine **Zahlungsmethode** wie **COD**, **Netto**, **aktueller Monat**, usw. Mit der **Zahlungsmethode** legen Sie fest, ab wann die Fälligkeit berechnet wird. Zum Beispiel wird **Net** verwendet, wenn das Fälligkeitsdatum immer eine festgelegte Anzahl von Monaten oder Tagen nach dem Rechnungsdatum liegt. **COD** kann verwendet werden, wenn die Zahlung auf Rechnung erforderlich ist, damit kein Fälligkeitsdatum berechnet wird. Wählen Sie **Aktueller Monat** für diese Anleitung.  
14. Wählen Sie einen **Zahlungstag** aus, wenn ein bestimmter Wochentag oder ein Datum in die Berechnung einbezogen werden. Abhängig von Ihren Zahlungsbedingungen können Sie eine Menge in Monaten oder Tagen eingeben. Oder Sie können den **Zahlungszeitplan** oder **Zahlungstag** am Ende der **Zahlungsmethode** 'anhängen'. Wenn das Fälligkeitsdatum immer der 10. des nächsten Monats ist, wählen Sie als **Zahlungstag** den 10. aus. Wenn Sie einen **Zahlungskalender** verwenden, können Sie festlegen, wie das Fälligkeitsdatum bestimmt wird, wenn das berechnete Datum auf einen Nicht-Arbeitstag fällt. Das erste Fälligkeitsdatum wird in Kalendertagen berechnet. Wenn das berechnete Datum auf einen Nicht-Arbeitstag fällt, können Sie das berechnete Fälligkeitsdatum entweder auf das nächste Arbeitsdatum oder einen früheren Arbeitstag einstellen.
15. Klicken Sie auf **Speichern**.
16. Schließen Sie die Seite.
17. Wechseln Sie zu **Debitoren > Zahlungseinstellungen > Skonti**.
18. Klicken Sie auf **Neu**. Diese Seite wird verwendet, um zu definieren, wie das Skontodatum berechnet wird. 
19. Geben Sie im Feld **Skonto** eine Kennung ein.
20. Geben Sie im Feld **Beschreibung** eine Beschreibung ein.
21. Wenn ein gestaffelter Skonto verfügbar ist, wählen Sie den **Nächster Skontocode** aus, der nach diesem neuen Skonto relevant ist.
22. Geben Sie im Feld **Tage** die Anzahl der Tage ein, die verwendet werden, um das Skontodatum zu berechnen. Wenn **Nettoprinzip** ausgewählt ist, wird die Anzahl der Tage zum Rechnungsdatum hinzugefügt, um das Skontodatum zu berechnen.  
23. Geben Sie im Feld **Rabattprozentsatz** den Prozentsatz des Skontos ein.
24. Geben Sie im **Hauptkonto für Debitorenrabatte** das Hauptkonto an, auf das das Skonto für Debitorenrechnungen gebucht wird.
25. Wählen Sie im Feld **Rabattgegenkonten** eine Option aus. Wenn Sie "Konten zu den Rechnungspositionen" auswählen, wird der Skonto zu denselben Anlagen-/Ausgabenhauptkonto auf den Positionen in der Kreditorenrechnung gebucht. Wenn Sie **Hauptkonto für Lieferantenrechnungen verwenden** wählen, wird der Skonto auf das Hauptkonto gebucht, das Sie unter **Hauptkonto für Lieferantenrechnungen** definieren. Wählen Sie für dieses Beispiel **Hauptkonto für Rechnungen von Kreditoren verwenden**. 
26. Geben Sie im Feld **Hauptkonto für Kreditorenrabatte** das Hauptkonto an, auf das das Skonto für Kreditorenrechnungen gebucht wird.
27. Klicken Sie auf **Speichern**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
