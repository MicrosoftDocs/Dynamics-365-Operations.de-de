---
title: Debitorenzahlungsbedingungen einrichten
description: Diese Prozedur definiert eine Skonto- und Fälligkeitsdatumseinstellung.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PaymDay, PaymTerm, CashDisc
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f641d75e06b11ca325d2624f836fc2a7c92d69e4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4443480"
---
# <a name="establish-customer-payment-terms"></a>Debitorenzahlungsbedingungen einrichten

[!include [banner](../../includes/banner.md)]

Diese Prozedur definiert eine Skonto- und Fälligkeitsdatumseinstellung. Für diese Aufgabenanleitung wird das Demo-Unternehmen USMF verwendet.

1. Wechseln Sie zu **Navigationsbereich > Module > Debitorenkonten > Zahlungseinrichtung > Zahlungstage**. Die Einstellungen für die **Zahlungsbedingungen** werden für **Debitoren** und **Kreditoren** freigegeben. Wenn Sie diese im Modul definieren, ist dies auch im anderen Modul verfügbar. Für diese Aufgabenanleitung richte ich alle Zahlungsbedingungen unter **Debitoren** ein.
2. Klicken Sie auf **Neu**. Erstellen Sie einen Zahlungstag, wenn Ihre Zahlungsbedingungen einen bestimmten Wochentag (Montag, Dienstag, usw.) oder ein bestimmtes Datum des Monats (5., 10., usw.) erfordern. 
3. Geben Sie im Feld **Zahlungstag** eine Kennung ein.
4. Geben Sie im Feld **Beschreibung** eine kurze Beschreibung den Zahlungstag ein.
5. Wählen Sie im Feld **Woche/Monat** entweder „Woche“ oder „Monat“ aus. Wenn Sie einen Wochentag eingeben möchten, wie beispielsweise Montag, wählen Sie "Woche" aus. Wenn Sie ein Datum im Monat eingeben möchten, wie beispielsweise der 10., wählen Sie "Monat" aus. Wählen Sie "Monat" für dieses Beispiel aus. 
6. Geben Sie im Feld **Tag des Monats** ein Datum ein. Das Datum sollte als Zahl eingegeben werden, wie beispielsweise "10", und nicht als "10.". 
7. Klicken Sie auf **Speichern**.
8. Schließen Sie die Seite.
9. Wechseln Sie zu **Navigationsbereich > Module > Debitorenkonten > Zahlungseinrichtung > Zahlungsbedingungen**.
10. Klicken Sie auf **Neu**. "Zahlungsbedingungen" werden verwendet, um zu definieren, wie die Fälligkeitsdaten berechnet werden. Die Skontodatumseinstellungen werden auf einer separaten Seite definiert. 
11. Geben Sie im Feld **Zahlungsbedingungen** eine Kennung ein.
12. Geben Sie im Feld **Beschreibung** eine Beschreibung ein.
13. Wählen Sie eine **Zahlungsmethode** wie Zahlung bei Lieferung, Netto-, Aktueller Monat usw. aus. Die Zahlungsmethode wird verwendet, um den Anfang der Berechnungsweise der Verbindlichkeiten festzulegen. Beispielsweise wird "Netto" verwendet, wenn das Fälligkeitsdatum immer eine festgelegte Anzahl von Monaten oder Tagen seit dem Rechnungsdatum ist. Zahlung bei Lieferung kann verwendet werden, wenn die Zahlung nach Rechnung erforderlich ist, damit würde kein Fälligkeitsdatum berechnet. Wählen Sie „Aktueller Monat“ für diese Aufgabenleitfaden aus.  
14. Wählen Sie einen **Zahlungstag** aus, wenn ein bestimmter Wochentag oder ein Datum in die Berechnung einbezogen werden. Abhängig von Ihren Zahlungsbedingungen können Sie eine Menge in Monaten oder Tagen eingeben. Oder Sie können den **Zahlungsplan** oder **Zahlungstag** verwenden zum „Hinzufügen“ an das Ende der „Zahlungsmethode“. Wenn das Fälligkeitsdatum immer der 10. des nächsten Monats ist, wählen Sie als **Zahlungstag** den 10. aus. 
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
25. Wählen Sie im Feld **Rabattgegenkonten** eine Option aus. Wenn Sie "Konten zu den Rechnungspositionen" auswählen, wird der Skonto zu denselben Anlagen-/Ausgabenhauptkonto auf den Positionen in der Kreditorenrechnung gebucht. Wenn Sie "Hauptkonto für Kreditoren verwenden" auswählen, wird der Skonto zum Hauptkonto gebucht, das Sie unter "Hauptkonto für Kreditorenrechnungen" definieren. Wählen Sie für dieses Beispiel „Hauptkonto für Kreditorenrechnungen verwenden“ aus. 
26. Geben Sie im Feld **Hauptkonto für Kreditorenrabatte** das Hauptkonto an, auf das das Skonto für Kreditorenrechnungen gebucht wird.
27. Klicken Sie auf **Speichern**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]