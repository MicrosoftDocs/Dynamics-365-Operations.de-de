---
title: EUR-00002 Generieren Sie eine EU-Intrastat-Meldung
description: Diese Prozedur führt Sie durch die Schritte, die erforderlich sind, um die Intrastat-Meldung im elektronischen Dateiformat zu exportieren und die Meldungsdaten in einem Excel-Format in der Vorschau anzuzeigen.
author: Anasyash
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionRepositoryTable, ERSolutionImport, IntrastatParameters, IntrastatCommodityLookup, IntrastatCompressParameters, Intrastat, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: anasyash
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e2aba5caaaf0fbee511e1a293b09fa8301bb6831
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145265"
---
# <a name="eur-00002-generate-an-eu-intrastat-declaration"></a>EUR-00002 Generieren Sie eine EU-Intrastat-Meldung

[!include [banner](../../includes/banner.md)]

Diese Prozedur führt Sie durch die Schritte, die erforderlich sind, um die Intrastat-Meldung im elektronischen Dateiformat zu exportieren und die Meldungsdaten in einem Excel-Format in der Vorschau anzuzeigen. 

Bevor Sie diese Prozedur abschließen können, müssen Sie Transaktionen zum Intrastat übertragen. 

Diese Prozedur wurde mit dem Demodatenunternehmen DEMF erstellt.


## <a name="import-configurations-with-settings"></a>Importkonfigurationen mit Einstellungen
1. Wechseln Sie zu "Arbeitsbereiche" > "Elektronische Berichterstellung"
2. Klicken Sie auf "Als aktiv festlegen"
3. Klicken Sie auf Repositorys.
4. Klicken Sie auf "Öffnen".
5. Öffnen Sie den Spaltenfilter "Konfigurationsname".
6. Wenden Sie einen Filter auf das Feld "Konfigurationsname" mit einem Wert von "Intrastat (DE)" unter Verwendung des Filteroperators "Beginnt mit" an.
    * Sie sollten den Konfigurationsnamen auswählen, der für das Land Ihrer juristischen Person gültig ist. Bei dieser Prozedur wird die deutsche juristische Person (DEMF) als Beispiel benutzt, daher sollte "Intrastat DE" ausgewählt werden.  
    * Klicken Sie auf "Importieren" und klicken Sie dann auf "Ja".  
7. Öffnen Sie den Spaltenfilter "Konfigurationsname".
8. Wenden Sie einen Filter auf das Feld "Konfigurationsname" mit einem Wert von "Intrastat-Bericht" unter Verwendung des Filteroperators "Beginnt mit" an.
    * Klicken Sie auf "Importieren" und klicken Sie dann auf "Ja".  

## <a name="set-up-foreign-trade-parameters"></a>Richten Sie Außenhandelsparameter ein
1. Wechseln Sie zu Steuer > Einstellungen > Außenhandel > Außenhandelsparameter.
2. Erweitern Sie den Bereich "Elektronische Berichterstellung".
3. Geben Sie im Feld "Dateiformatzuordnung" einen Wert "Intrastat (DE)" ein oder wählen Sie einen solchen Wert aus.
4. Geben Sie im Feld "Berichtformatzuordnung" einen Wert "Intrastat-Bericht" ein oder wählen Sie einen solchen Wert aus.
5. Erweitern Sie den Abschnitt "Rundungsregeln".
    * Sie sollten Rundungsregeln einrichten, die in Ihrem Land/Ihrer Region für Intrastat-Berichte gültig sind.  
6. Geben Sie im Feld "Rundungsregel" eine Zahl ein.
    * Geben Sie Rundungsgenauigkeit ein, beispielsweise "0.01".  
7. Geben Sie im Feld "Anzahl von Dezimalen für Betrag" eine Zahl ein.
    * Geben Sie beispielsweise "2" ein.  
8. Wählen Sie im Feld "Rundung unter 1 kg" eine Option aus.
    * Beispielsweise wählen Sie "Aufrunden auf 1 kg" aus.  
9. Geben Sie im Feld "Rundungsregel" eine Zahl ein.
    * Geben Sie beispielsweise "1 "für das Runden des Gewichts auf die ganze Zahl ein.  
10. Erweitern Sie den Abschnitt "Untergrenze".
11. Geben Sie im Feld "Gewicht" eine Zahl ein.
    * Geben Sie beispielsweise "10 "als das Mindestgewicht ein.  
12. Geben Sie im Feld "Betrag" eine Zahl ein.
    * Geben Sie beispielsweise "200 "als den Mindestbetrag ein.  
13. Geben Sie im Feld "Ware" einen Wert ein, oder wählen Sie einen Wert aus.

## <a name="set-up-compression-of-intrastat"></a>Richten Sie Komprimierung von Intrastat ein
1. Wechseln Sie zu "Steuer" > "Einstellungen" > "Außenhandel" > "Komprimierung von Intrastat".
2. Klicken Sie auf "Entfernen".
3. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Wählen Sie beispielsweise "Ware" im Abschnitt "Verfügbar" aus.  
4. Klicken Sie auf Hinzufügen.

## <a name="generate-intrastat-declaration"></a>Generieren Sie eine Intrastat-Meldung
1. Wechseln Sie zu "Steuer" > "Meldungen" > "Außenhandel" > "Intrastat"
2. Klicken Sie auf "Überprüfen".
    * Die Überprüfung erfolgt gemäß des Felds "Einstellungen prüfen" auf der Seite "Außenhandelsparameter".  
3. Klicken Sie auf "OK".
4. Klicken Sie auf Aktualisieren.
5. Klicken Sie auf "Untergrenze".
6. Geben Sie im Feld "Startdatum" ein Datum ein.
    * Geben Sie beispielsweise "1. Januar, 2015" ein.  
7. Wählen Sie "Ja" im Feld "Komprimieren" aus.
8. Geben Sie im Feld "Enddatum" ein Datum ein.
    * Geben Sie beispielsweise "31. Januar, 2015" ein.  
9. Klicken Sie auf "OK".
10. Klicken Sie auf Aktualisieren.
11. Klicken Sie auf "Komprimieren".
    * Diese Komprimierung geschieht gemäß dem, wie Sie die Komprimierung von Intrastat-Einstellungen einstellen.  
12. Geben Sie im Feld "Startdatum" ein Datum ein.
    * Geben Sie beispielsweise "1. Januar, 2015" ein.  
13. Geben Sie im Feld "Enddatum" ein Datum ein.
    * Geben Sie beispielsweise "31. Januar, 2015" ein.  
14. Klicken Sie auf "OK".
15. Klicken Sie auf Aktualisieren.
16. Klicken Sie auf "Sequenznummern von neuem generieren".
17. Klicken Sie auf "OK".
18. Klicken Sie auf "Ausgabe".
19. Klicken Sie auf "Bericht".
20. Geben Sie im Feld "Von Datum" das erste Datum des Berichtszeitraums ein.
    * Legen Sie beispielsweise das Datum auf den 1. Januar 2015 fest.  
21. Geben Sie in das Feld "Bis Datum" ein Datum ein.
    * Geben Sie beispielsweise "31. Januar, 2015" ein.  
22. Wählen Sie "Ja" im Feld "Datei generieren" aus.
23. Geben Sie im Feld "Dateiname" einen Wert ein.
24. Wählen Sie "Ja" im Feld "Bericht erzeugen" aus.
25. Geben Sie im Feld "Berichtsdateiname" einen Wert ein.
26. Wählen Sie im Feld "Richtung" eine Option aus.
    * Wählen Sie z. B. "Versand" aus.  
27. Klicken Sie auf "OK".

