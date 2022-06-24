---
title: 'ER – Konfigurieren des Formats für Inventuren und Summierungen (Teil 4: Format ausführen)'
description: In diesem Artikel wird beschrieben, wie Sie ein elektronisches Berichtsformat für das Zählen und Summieren basierend auf Daten der bereits generierten Textausgabe konfigurieren. (Teil 4)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, IntrastatParameters, Intrastat, InventItemIdLookupSimple, IntrastatCommodityLookup, ERFormatMappingRunLogTable, DocuView
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 665f51b3c0b7dd4fac1ca26f6918ee1e6c9fa85a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8848750"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-4---run-format"></a>ER – Konfigurieren des Formats für Inventuren und Summierungen (Teil 4: Format ausführen)

[!include [banner](../../includes/banner.md)]

In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Format zur Inventarisierung und Summierung basierend auf der bereits generierten Textausgabe. Diese Schritte können im DEMF-Unternehmen ausgeführt werden.

Um diese Schritte auszuführent, müssen Sie erst die Schritte im Aufgabenleitfaden ER - Konfigurieren des Formats für die Inventarisierung und Zusammenfassung (Teil 3: Nutzung von Berechnungen für Ausgaben) ausführen.

Diese Prozedur ist eine Funktion, für die in Dynamics 365 for Operations Version 1611 hinzugefügt wurde.


## <a name="test-this-configuration-for-generation-of-the-intrastat-reports"></a>Testen Sie diese zur Konfiguration zur Generierung von Intrastat-Berichten.
1. Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.
2. Klicken Sie auf "Berichterstellungskonfigurationen".
3. Erweitern Sie 'Intrastatmodell' in der Struktur.
4. Erweitern Sie in der Strukturdarstellung "Intrastatmodel\Intrastat (DE)".
5. Wählen Sie in der Struktur 'Intrastat model\Intrastat (DE)\Intrastat (DE) Bit Berechnung und Summieren.
6. Klicken Sie im Aktivitätsbereich auf Konfigurationen.
7. Klicken Sie auf Benutzerparameter.
8. Wählen Sie "Ja" im Feld "Testlaufeinstellungen".
9. Klicken Sie auf "OK".
10. Klicken Sie auf "Bearbeiten".
11. Wählen Sie "Ja" im Feld "Testentwurf".
12. Klicken Sie auf "Speichern".
13. Wechseln Sie zu "Steuer" > "Einstellungen" > "Außenhandel" > "Außenhandelsparameter".
14. Erweitern Sie den Bereich "Elektronische Berichterstellung".
15. Wählen Sie die Konfiguration Intrastat (DE) mit Berechnungs- und Summierungs-Konfiguration.
16. Wählen Sie die Konfiguration Intrastat (DE) mit Berechnungs- und Summierungs-Konfiguration.
17. Klicken Sie auf Speichern.
18. Schließen Sie die Seite.
19. Wechseln Sie zu "Steuer" > "Meldungen" > "Außenhandel" > "Intrastat".
20. Klicken Sie auf "Ausgabe".
21. Klicken Sie auf "Bericht".
    * Führen Sie den Intrastat-Bericht-Generierungsprozess aus.  
22. Legen Sie das Datum "2000-01-01" im Feld "Von Datum" fest.
    * Definieren Sie Start- und Enddaten für den Berichtszeitraum, die die vorhandenen Formularbuchungen einbeziehen.  
23. Legen Sie das Datum "2022-12-31" im Feld "Bis Datum" fest.
    * Definieren Sie Start- und Enddaten für den Berichtszeitraum, die die vorhandenen Formularbuchungen einbeziehen.  
24. Wählen Sie im Feld "Richtung" "Empfang" aus.
25. Wählen Sie "Ja" im Feld "Datei generieren" aus.
26. Klicken Sie auf "OK".
    * Prüfen Sie die erstellten Ausgaben über die zusammengefassten Positionen am Ende.  
27. Klicken Sie auf "Neu".
28. Markieren Sie in der Liste die ausgewählte Zeile.
29. Wählen Sie im Feld "Richtung" "Versand" aus.
30. Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.
31. Geben Sie im Feld "Ware" einen Wert ein, oder wählen Sie einen Wert aus.
32. Legen Sie "Gewicht" auf "10" fest.
33. Legen Sie "Rechnungsbetrag" auf "10000" fest.
34. Legen Sie "Statistikbetrag" auf "10000" fest.
35. Klicken Sie auf "Ausgabe".
36. Klicken Sie auf "Bericht".
37. Wählen Sie im Feld "Richtung" "Versand" aus.
38. Klicken Sie auf "OK".
    * Prüfen Sie die erstellten Ausgaben über die zusammengefassten Positionen am Ende. Beachten Sie, dass er sich im Vergleich zu dem ersten Durchlauf geändert hat.  

## <a name="run-this-configuration-in-debug-mode-to-review-the-collected-counting--summing-data"></a>Führen Sie diese Konfiguration im Debugmodus aus, um die gesammelten Zählungs- und Summierungsdaten zu prüfen.
1. Wechseln Sie zu Organisationsverwaltung > Elektronische Berichterstellung > Konfigurationen.
2. Erweitern Sie 'Intrastatmodell' in der Struktur.
3. Erweitern Sie in der Strukturdarstellung "Intrastatmodel\Intrastat (DE)".
4. Wählen Sie in der Struktur 'Intrastat model\Intrastat (DE)\Intrastat (DE) Bit Berechnung und Summieren.
5. Klicken Sie im Aktivitätsbereich auf Konfigurationen.
6. Klicken Sie auf Benutzerparameter.
7. Wählen Sie "Ja" im Feld "Im Debugmodus ausführen" aus.
8. Klicken Sie auf "OK".
9. Schließen Sie die Seite.
10. Wechseln Sie zu "Steuer" > "Meldungen" > "Außenhandel" > "Intrastat".
11. Klicken Sie auf "Ausgabe".
12. Klicken Sie auf "Bericht".
13. Klicken Sie auf "OK".
14. Schließen Sie die Seite.
15. Wechseln Sie zu Organisationsverwaltung > Elektronische Berichterstellung > Konfigurationen.
16. Erweitern Sie 'Intrastatmodell' in der Struktur.
17. Erweitern Sie in der Strukturdarstellung "Intrastatmodel\Intrastat (DE)".
18. Wählen Sie in der Struktur 'Intrastat model\Intrastat (DE)\Intrastat (DE) Bit Berechnung und Summieren.
19. Klicken Sie auf Debugprotokolle.
    * Beachten Sie, dass ein debuggensprotokolldatensatz für den Ausführungsprozess der ausgewählten Konfiguration erstellt wurde.  
20. Klicken Sie auf Anhänge.
21. Klicken Sie auf "Öffnen".
    * Prüfen Sie die erstellte XML-Datei, die die Inventur- und Zusammenfassungsdetails enthält, die bei der Ausführung der ausgewählten Konfiguration gesammelt wurden.  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]