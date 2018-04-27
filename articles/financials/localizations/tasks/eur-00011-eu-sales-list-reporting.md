--- 
title: Zusammenfassende Meldung einrichten
description: "Diese Aufgabe führt Sie durch einen Überblick über die Voraussetzungen, die für zusammenfassende Meldungen erforderlich sind."
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 11/14/2016
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 5c415b06debc882c9ecdacc1c89e64325df4d4c7
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-eu-sales-list-reporting"></a>Zusammenfassende Meldung einrichten

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Diese Aufgabe führt Sie durch einen Überblick über die Voraussetzungen, die für zusammenfassende Meldungen erforderlich sind. Weitere Informationen über zusammenfassende Meldungen, einschließlich erforderliche Voraussetzungen, finden Sie in der Hilfe von Dynamics 365 for Finance and Operations Help.

Diese Aufgabe gilt für alle europäischen Länder/Regionen. Das Handbuch wurde mithilfe des Demodatenunternehmens DEMF und folglich Deutschland als Exemplarinlandsland/region erstellt. Das Handbuch verwendet ebenfalls Portugal als Exemplar EU-Land/Region.

Diese Aufgaben richten sich an Systemadministratoren.


## <a name="import-electronic-reporting-configurations-for-eu-sales-list-reporting"></a>Elektronische Berichterstellungskonfigurationen für zusammenfassende Meldungen importieren
1. Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.
2. Klicken Sie auf "Als aktiv festlegen"
3. Klicken Sie auf Repositorys.
4. Klicken Sie auf "Öffnen".
5. Klicken Sie im Aktivitätsbereich auf "Optionen".
6. Klicken Sie auf "Erweitertes Filtern/Sortieren".
7. Klicken Sie auf Hinzufügen.
8. Wählen Sie im Feld "Feld" "Konfigurationsname" aus.
9. Geben Sie im Feld "Kriterien""Zusammenfassende Meldung (DE)" ein.
10. Klicken Sie auf "OK".
11. Klicken Sie auf Import.
12. Klicken Sie auf "Ja".
13. Klicken Sie im Aktivitätsbereich auf "Optionen".
14. Klicken Sie auf "Erweitertes Filtern/Sortieren".
15. Klicken Sie auf 'Zurücksetzen'.
16. Klicken Sie auf Hinzufügen.
17. Wählen Sie im Feld "Feld" "Konfigurationsname" aus.
18. Geben Sie im Feld "Kriterien""Zusammenfassende Meldung nach Zeilen anzeigen" ein.
19. Klicken Sie auf "OK".
20. Klicken Sie auf Import.
21. Klicken Sie auf "Ja".

## <a name="set-up-sales-tax-codes-for-eu-sales-list-reporting"></a>Mehrwertsteuercodes für zusammenfassende Meldungen einrichten
1. Wechseln Sie zu "Steuer" > "Indirekte Steuern" > "Mehrwertsteuer" > "Mehrwertsteuercodes".
2. Verwenden Sie den Schnellfilter, um im Feld "Mehrwertsteuercode" nach dem Wert 'VAT19' zu filtern.
3. Erweitern Sie den Abschnitt "Berichtseinstellungen".
    * Überprüfen Sie, ob die Auswahl "Ausgeschlossen" auf "Nein" festgelegt ist.  
    * Sie müssen möglicherweise den Aufgabenleitfaden entsperren, um diese Einstellung zu ändern.  

## <a name="set-up-sales-tax-groups-for-eu-sales-list-reporting"></a>Mehrwertsteuergruppen für zusammenfassende Meldungen einrichten
1. Wechseln Sie zu "Steuer" > "Indirekte Steuern" > "Mehrwertsteuer" > "Mehrwertsteuergruppen".
2. Verwenden Sie den Schnellfilter, um im Feld "Mehrwertsteuergruppe" nach dem Wert 'AR-DOM' zu filtern.
3. Klicken Sie auf Bearbeiten.
4. Erweitern Sie den Abschnitt 'Einstellungen'.
5. Markieren Sie in der Liste die erste Zeile.
6. Aktivieren Sie das Kontrollkästchen "Befreit".
7. Markieren Sie in der Liste die zweite Zeile.
8. Aktivieren Sie das Kontrollkästchen "Befreit".
9. Markieren Sie in der Liste die dritte Zeile.
10. Aktivieren Sie das Kontrollkästchen "Befreit".

## <a name="set-up-item-sales-tax-groups-for-eu-sales-list-reporting"></a>Artikel-Mehrwertsteuergruppen für zusammenfassende Meldungen einrichten
1. Wechseln Sie zu "Steuer" > "Indirekte Steuern" > "Mehrwertsteuer" > "Artikel-Mehrwertsteuergruppen".
2. Verwenden Sie den Schnellfilter, um im Feld "Artikel-Mehrwertsteuergruppe" nach dem Wert 'FULL' zu filtern.
    * Überprüfen Sie, ob die Auswahl "Berichtstyp" auf "Artikel" festgelegt ist.  
    * Sie müssen möglicherweise den Aufgabenleitfaden entsperren, um den Wert für dieses Feld zu ändern.  
3. Verwenden Sie den Schnellfilter, um im Feld "Artikel-Mehrwertsteuergruppe" nach dem Wert 'RED' zu filtern.
    * Überprüfen Sie, ob die Auswahl "Berichtstyp" auf "Dienstleistung" festgelegt ist.  
    * Sie müssen möglicherweise den Aufgabenleitfaden entsperren, um den Wert für dieses Feld zu ändern.  

## <a name="set-up-countryregion-parameters-for-eu-sales-list-reporting"></a>Länder-/Regionsparameter für zusammenfassende Meldungen einrichten
1. Wechseln Sie zu "Steuer" > "Einstellungen" > "Mehrwertsteuer" > "Länder-/Regionsparameter".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Land/Region" "PRT" ein.
4. Geben Sie im Feld "Mehrwertsteuer" "PT" ein.

## <a name="create-tax-exempt-numbers"></a>Umsatzsteuernummern erstellen
1. Wechseln Sie zu "Steuer" > "Einstellungen" > "Mehrwertsteuer" > "USt-IdNr.".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Land/Region" "PRT" ein.
4. Geben Sie im Feld "USt-IdNr." die Zeichenfolge "PT12345" ein.

## <a name="set-up-eu-sales-list-reporting-parameters"></a>Parameter für Zusammenfassende Meldung einrichten
1. Wechseln Sie zu "Steuer" > "Einstellungen" > "Außenhandel" > "Außenhandelsparameter".
2. Klicken Sie auf die Registerkarte "Zusammenfassenden Meldung".
3. Wählen Sie "Ja" im Feld "Einkäufe übertragen"aus.
4. Erweitern Sie den Abschnitt "Rundungsregeln".
5. Legen Sie die Rundungsregel auf "0,1" fest.
6. Wählen Sie "Ja" im Feld "Mindestwert verwenden".
7. Geben Sie im Feld "Dezimalstellen '2' ein.
8. Erweitern Sie den Bereich "Elektronische Berichterstellung".
9. Wählen Sie im Feld "Dateiformatzuordnung" "Zusammenfassende Meldung (DE)"aus.
10. Geben Sie im Feld "Berichtformatzuordnung" "Zusammenfassende Meldung nach Zeilen anzeigen" ein.
11. Klicken Sie auf die Schaltfläche "Länder-/Regionseigenschaften".
    * Vergewissern Sie sich, dass das Feld "Länder-/Regionsart" auf "Inland" für Land/Region DEU ist.  
    * Sie müssen möglicherweise den Aufgabenleitfaden entsperren, um den Wert für dieses Feld zu ändern.  
12. Klicken Sie auf "Neu".
13. Geben Sie im Feld "Land/Region" "PRT" ein.
14. Geben Sie im Feld "Intrastat-Code" "PT" ein.
15. Wählen Sie im Feld "Land/Region" 'EU'.
16. Klicken Sie auf die Registerkarte "Nummernkreis".
    * Überprüfen Sie, dass ein Nummernkreis für die Referenz "Zusammenfassende Meldung" angegeben ist.  

## <a name="create-a-customer-for-eu-sales-list-reporting-demo-purposes"></a>Einen Debitor für Demozwecke der zusammenfassenden Meldungen erstellen
1. Wechseln Sie zu "Debitoren" > "Debitoren" > "Alle Debitoren".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Debitorenkonto" den Wert 'PRT-001' ein.
4. Geben Sie im Feld "Name" "Debitor aus Portugal" ein.
5. Wählen Sie im Feld "Debitorengruppe" "10" aus.
6. Wählen Sie im Feld "Mehrwertsteuergruppe" "AR-DOM" aus.
7. Wählen Sie im Feld "USt-IdNr." die Zeichenfolge "PT12345".
8. Geben Sie im Feld "Land/Region" "PRT" ein.
9. Klicken Sie auf "Speichern".


