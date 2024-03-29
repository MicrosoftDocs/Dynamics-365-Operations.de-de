---
title: EUR-00002 - Angeben einer Ladungsadresse für eine Innergemeinschaftliche Buchung
description: Dieses Verfahren zeigt, wie eine Ladungsadresse für eine innergemeinschaftliche Handelsbuchung festgelegt wird.
author: AdamTrukawka
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: atrukawk
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form:
- PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, TransportationDocument, LogisticsPostalAddress, SysLookupMultiSelectGrid
- VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog, Intrastat, SysQueryForm
ms.openlocfilehash: 2094d24f256647ee3193f7e069e33bf4d99c1b70
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280600"
---
# <a name="eur-00002-specifying-a-lading-address-for-an-intra-community-transaction"></a>EUR-00002 - Angeben einer Ladungsadresse für eine Innergemeinschaftliche Buchung

[!include [banner](../../includes/banner.md)]

Dieses Verfahren zeigt, wie eine Ladungsadresse für eine innergemeinschaftliche Handelsbuchung festgelegt wird. Zum Beispiel ein deutsches Unternehmens bestellt Artikel von einem Kreditor mit einer deutschen Geschäftsadresse. Dieser Kreditor hat einen Lagerort in Italien und liefert die Artikel von dort. Die Lieferung muss in Intrastat gemeldet werden. Dasselbe Verhalten gilt für Debitorenrücklieferungen.
Diese Prozedur gilt für alle europäischen Länder/Regionen. Diese Aufgabe wurde mithilfe des Demodatenunternehmens DEMF mit der primären Adresse in Deutschland erstellt. Bevor Sie dieses Verfahren ausführen können, müssen Sie Intrastat-Berichte konfigurieren. Diese Prozedur ist für Buchhalter vorgesehen. Diese Prozedur ist eine Funktion, für die in Dynamics 365 for Operations Version 1611 hinzugefügt wurde.

1. Wechseln Sie zu "Kreditoren" > "Bestellungen" > "Alle Bestellungen".
2. Klicken Sie auf "Neu".
3. Wert eingeben oder auswählen
    * Wählen Sie z. B. DE-001 aus. Dieser Kreditor hat eine deutsche Geschäftsadresse.  
4. Klicken Sie auf "OK".
5. Markieren Sie in der Liste die ausgewählte Zeile.
6. Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie den Wert "D0001" aus.
7. Klicken Sie auf Speichern.
8. Klicken Sie im Aktivitätsbereich auf "Entgegennehmen".
9. Klicken Sie auf Transportdetails.
10. Geben Sie im Feld "Beladungsdatum und -uhrzeit" ein Datum und eine Uhrzeit ein.
11. Klicken Sie auf "Adresse hinzufügen".
12. Klicken Sie auf "Neu" und erstellen Sie eine neue Adresse mit dem Zweck "Beladen".
13. Geben Sie im Feld "Name oder Beschreibung" "Italienisch" ein.
14. Wählen Sie "Beladung" als Wert aus.
    * Beachten Sie, das der Adresszweck "Beladen" muss.  
15. Wählen Sie im Feld Name/Region "ITA" aus oder geben Sie einen Wert ein.
16. Klicken Sie auf "Speichern".
17. Schließen Sie die Seite.
18. Klicken Sie auf "Speichern".
    * Überprüfen Sie, ob die Beladungsadresse korrekt ist.  
19. Schließen Sie die Seite.
20. Klicken Sie im Aktivitätsbereich auf "Einkauf".
21. Klicken Sie auf "Bestätigen".
22. Klicken Sie im Aktivitätsbereich auf "Rechnung".
23. Klicken Sie auf "Rechnung".
24. Geben Sie im Feld "Zahl" einen Wert ein.
25. Geben Sie in das Feld "Rechnungsdatum" ein Datum ein.
26. Klicken Sie auf "Standard von: Menge im Produktzugang", um das Ablagedialogfeld zu öffnen.
27. Wählen Sie im Feld "Standardmenge für Positionen" "Menge im Produktzugang" aus.
28. Klicken Sie auf "OK".
29. Klicken Sie auf Transportdetails.
    * Überprüfen Sie, dass Waren aus Italien versendet wurden. Bei Bedarf können Sie die Ladungsdetails bearbeiten.  
30. Schließen Sie die Seite.
31. Klicken Sie auf "Buchen".
32. Schließen Sie die Seite.
33. Wechseln Sie zu "Steuer" > "Meldungen" > "Außenhandel" > "Intrastat".
34. Klicken Sie auf Übertragen.
35. Wählen Sie "Ja" im Feld "Kreditorenrechnung" aus.
36. Klicken Sie auf "OK".
37. Klicken Sie auf die Registerkarte "Allgemein".
    * Suchen Sie eine neu erstellte Position und vergewissern Sie sich, dass der Absender die Waren aus Italien liefert.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
