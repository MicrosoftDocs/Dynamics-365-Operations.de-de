--- 
title: Bericht 'Zusammenfassende Meldung' generieren
description: "Diese Prozedur führt Sie durch das Generieren eines Berichts für zusammenfassende Meldungen."
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 10e7399b058695fb1c1b0db8c696c926619c995a
ms.contentlocale: de-de
ms.lasthandoff: 07/27/2017

---
# <a name="generate-an-eu-sales-list-report"></a>Bericht 'Zusammenfassende Meldung' generieren

[!include[task guide banner](../../includes/task-guide-banner.md)]

Diese Prozedur führt Sie durch das Generieren eines Berichts für zusammenfassende Meldungen. Hierzu zählen das Übertragen von innergemeinschaftlichen Handelsbuchungen zur zusammenfassenden Meldung und das Ausführen des Berichts. Diese Prozedur umfasst auch das Erstellen einer innergemeinschaftlichen Handelsbuchung zu Demonstrationszwecken. Weitere Informationen über zusammenfassende Meldungen, einschließlich erforderliche Voraussetzungen, finden Sie in der Hilfe von Dynamics 365 for Finance and Operations Help.

Diese Prozedur gilt für alle europäischen Länder/Regionen. Die Prozedur wurde mithilfe des Demodatenunternehmens DEMF und somit mit Deutschland als Beispielland erstellt. Die Prozedur verwendet ebenfalls Portugal als Beispielland. Bevor Sie dieses Verfahren ausführen können, müssen Sie zusammenfassende Meldungen konfigurieren.

Diese Prozedur ist für Buchhalter vorgesehen.


## <a name="create-an-intra-community-sales-transaction-for-demo-purposes"></a>Erstellen einer innergemeinschaftlichen Verkaufsbuchung für Demonstrationszwecke
1. Wechseln Sie zu "Debitoren" > "Aufträge" > "Alle Aufträge".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Debitorenkonto" den Wert 'PRT-001' ein.
4. Klicken Sie auf "OK".
5. Geben Sie im Feld "Artikelnummer" die Zeichenfolge "D0001" ein.
6. Erweitern Sie den Abschnitt "Positionsdetails".
7. Klicken Sie auf die Registerkarte Einstellungen.
8. Geben Sie im Feld "Artikel-Mehrwertsteuergruppe" einen Wert "Voll" ein.
9. Klicken Sie auf "Position hinzufügen".
10. Geben Sie im Feld "Artikelnummer" die Zeichenfolge "D0003" ein.
11. Geben Sie im Feld "Artikel-Mehrwertsteuergruppe" einen Wert "ROT" ein.
12. Klicken Sie auf "Speichern".
13. Klicken Sie im Aktivitätsbereich auf "Rechnung".
14. Klicken Sie auf "Rechnung".
15. Erweitern Sie den Abschnitt "Parameter".
16. Wählen Sie im Feld "Menge" die Option "Alle" aus.
17. Erweitern Sie den Abschnitt 'Einstellungen'.
18. Legen Sie im Feld "Rechnungsdatum" das Datum "11.01.2016" fest.
19. Klicken Sie auf "OK".
20. Klicken Sie auf "OK".

## <a name="transfer-intra-community-trade-transactions-to-the-eu-sales-list"></a>Übertragen von innergemeinschaftlichen Verkaufsbuchungen zur zusammenfassenden Meldung
1. Wechseln Sie zu "Steuer" > "Meldungen" > "Außenhandel" > "Zusammenfassende Meldung".
2. Klicken Sie auf Übertragen.
3. Wählen Sie "Ja" im Feld "Artikel", um Artikelbuchungen zu übertragen.
4. Wählen Sie "Ja" im Feld "Leistung", um Leistungsbuchungen zu übertragen.
    * Sie können zusätzliche Filter auf zu übertragende innergemeinschaftliche Handelsbuchung anwenden.  
5. Klicken Sie auf Übertragen.
    * Überprüfen Sie, ob die innergemeinschaftlichen Handelsbuchung erfolgreich in die zusammenfassende Meldung übertragen wird.  

## <a name="generate-the-eu-sales-list-report"></a>Erstellen des Berichts für die zusammenfassende Meldung
1. Klicken Sie auf "Berichterstellung".
2. Wählen Sie im Feld "Berichtszeitraum" "Monatlich" aus.
3. Legen Sie das Von-Datum auf "01.01.2016" fest.
4. Wählen Sie "Ja" im Feld "Datei generieren" aus.
5. Wählen Sie "Ja" im Feld "Bericht erzeugen" aus.
6. Geben Sie im Feld "Dateiname" "EUSalesList" ein.
7. Geben Sie im Feld "Berichtdatei" "EUSalesList" ein.
8. Geben Sie im Feld "Registrierungs-ID Zusammenfassende Meldung" "123" ein.
    * Dieses Feld ist für Deutschland verfügbar.  
    * Sie können zusätzliche Filter auf die im Bericht angezeigte innergemeinschaftliche Handelsbuchung anwenden.  
9. Klicken Sie auf "OK".
    * Überprüfen Sie, ob Popupfenster für das Herunterladen der die Datei und des Kontrollberichts erscheinen.  

## <a name="mark-eu-sales-list-lines-as-reported"></a>Markieren der zusammenfassenden Meldung als "Berichtet"
1. Klicken Sie auf "Markieren".
2. Klicken Sie auf "Als berichtet markieren".
3. In der Liste wählen Sie die Zeile für das Feld "Rechnungsdatum" aus.
4. Geben Sie im Feld "Kriterien" den Wert "01.01.2016..31.01.2016" ein.
5. In der Liste wählen Sie die Zeile für das Feld "Berichtsstatus" aus.
6. Wählen Sie im Feld "Kriterien" den Wert "Enthalten" aus.
    * Sie können zusätzliche Filter auf die als "Berichtet" angezeigten innergemeinschaftlichen Handelsbuchungen anwenden.  
7. Klicken Sie auf "OK".
8. Wählen Sie im Feld "Abschnitt" "Berichtet" aus.

## <a name="mark-eu-sales-list-lines-as-closed"></a>Markieren der zusammenfassenden Meldung als "Abgeschlossen"
1. Klicken Sie auf "Markieren".
2. Klicken Sie auf "Als geschlossen markieren".
3. In der Liste markieren Sie die Zeile für das Feld "Rechnungsdatum" aus.
4. Geben Sie im Feld "Kriterien" den Wert "01.01.2016..31.01.2016" ein.
5. In der Liste markieren Sie die Zeile für das Feld "Berichtstatus" aus.
6. Wählen Sie im Feld "Kriterien" den Wert "Berichtet" aus.
    * Sie können zusätzliche Filter auf als "Abgeschlossen" markieren innergemeinschaftlichen Handelsbuchungn anwenden.  
7. Klicken Sie auf "OK".
8. Wählen Sie im Feld "Abschnitt" "Abgeschlossen" aus.


