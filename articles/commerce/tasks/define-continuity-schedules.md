---
title: " Anschlusszeitpläne definieren"
description: In diesem Artikel lernen Sie das Einrichten eines Anschlussprogramms kennen (auch als wiederkehrende Aufträge bezeichnet).
author: josaw1
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: MCRContinuitySchedule, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: faa55c844c8ee8742fbb0868b55a520cec6686aa
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885083"
---
# <a name="define-continuity-schedules"></a> Anschlusszeitpläne definieren

[!include [banner](../includes/banner.md)]

In diesem Artikel lernen Sie das Einrichten eines Anschlussprogramms kennen (auch als wiederkehrende Aufträge bezeichnet). Dieser Artikel verwendet das Unternehmen USRT in den Demodaten.


## <a name="create-continuity-program"></a>Erstellen eines Anschlussprogramms
1. Navigieren Sie zu Retail and Commerce > Anschluss > Anschlussprogramme.
2. Klicken Sie auf Neu.
3. Geben Sie im Feld "Planungskennung" die Anschlusszeitplankennung ein
4. Wählen Sie im "Auftragsanfang"-Feld "Erstes Ereignis" aus.
    * Wenn ein Kunde einen neuen Auftrag für das Kontinuitätsprogramm platziert, gibt es zwei Optionen für das Produkt versendet wird: . 1. Erstes Ereignis: das erste Produkt im Kontinuitätsprogramm wird versendet.  2. Aktuelles Ereignis: das aktuelle Produkt wird versendet. Beispiel: nach drei Monaten im Programm erhält der Debitor das dritte im Programm.  
5. Wählen Sie "Ja" aus, um das Auftragsstartdatum einzugeben.
6. Klicken Sie auf "Position hinzufügen".
7. Geben Sie im Feld Artikelnummer die Artikelnummer für das erste Produkt ein ('0013').
8. Geben Sie "AP" ein.
9. Geben Sie das Datum ein, an dem das erste Produkt bestellt werden kann.
10. Klicken Sie auf "Position hinzufügen".
11. Geben Sie im Feld "Artikelnummer" die Zeichenfolge "0014" ein.
12. Löschen Sie im Feld Datumsintervallcode den Wert, sodass das Feld leer ist.
    * Bei diesem Verfahren löschen Sie das Datumsintervall. Sie legen das Datum als inkrementell vom Startdatum des ersten Artikels fest.  
13. Hier geben Sie den Intervall ein, in dem die Produkte geliefert werden. Geben Sie 30 ein.
    * Für ein Monatsprogramm geben Sie 30 Tage für das Intervall ein.  
14. Klicken Sie auf "Position hinzufügen".
15. Geben Sie im Feld "Artikelnummer" die Zeichenfolge "0015" ein.
16. Geben Sie "Ende" ein.
17. Klicken Sie auf "Speichern".

## <a name="assign-to-continuity-item"></a>Zuweisen zu Anschlussartikel
1. Wechseln Sie zu "Produktinformationsverwaltung" > "Produkte" > "Freigegebene Produkte".
2. Wählen Sie Artikel 0016 aus.
    * Für diese Prozedur wählen Sie die Artikelnummer 0016 aus. Normalerweise haben Sie ein freigegebenes Produkt erstellt, für das zusätzliche Anschlussgeschäftslogik angewendet wird, wenn es im Callcenter für einen Auftrag platziert wird.  
3. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
4. Klicken Sie auf "Bearbeiten".
5. Erweitern oder reduzieren Sie den Abschnitt ''Verkaufen".
6. Hier geben Sie das Anschlussprogramm ein, das dieser Artikel darstellt. Geben Sie die Planungskennung ein, die Sie eben erstellt haben.
    * Wenn dieser Artikel in einem Callcenter verkauft wird, wird über das ausgewählte Anschlussprogramm eine zusätzliche Geschäftslogik angewendet.  
7. Klicken Sie auf "Speichern".



[!INCLUDE[footer-include](../../includes/footer-banner.md)]