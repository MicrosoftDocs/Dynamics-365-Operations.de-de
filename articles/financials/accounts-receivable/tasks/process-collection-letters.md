--- 
title: Mahnschreiben verarbeiten
description: Dieses Verfahren zeigt , wie Mahnschreiben erstellt, gedruckt und gebucht werden.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: dc837ea6513992a5f94e48baa366e279df297866
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="process-collection-letters"></a>Mahnschreiben verarbeiten

[!include [task guide banner](../../includes/task-guide-banner.md)]

Dieses Verfahren zeigt , wie Mahnschreiben erstellt, gedruckt und gebucht werden. Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet.


## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a>Richten Sie eine Mahnschreibensequenz zum Buchungsprofil ein.
1. Wechseln Sie zu "Kredit und Inkasso" > "Einstellungen" > "Debitorenbuchungsprofile".
2. Klicken Sie auf "Bearbeiten".
    * Wählen Sie eine Mahnschreibensequenz aus der Dropdownliste aus. Wenn Sie kein Mahnschreiben für Buchungen dieses Buchungsprofils erstellen wollen, lassen Sie das Feld leer.  
    * Die Tabelleneinschränkungsregisterkarte ermöglicht Ihnen das Verfahren, mit dem Mahnschreiben verarbeitet werden, zu ändern. Wenn dieses Feld auf "Ja" festgelegt ist, werden Mahnschreiben für dieses Buchungsprofil erstellt.  
3. Schließen Sie die Seite.

## <a name="create-collection-letters"></a>Mahnschreiben erstellen
1. Wechseln Sie zu "Kredit und Inkasso" > "Mahnschreiben" > "Erstellen von Mahnschreiben".
    * Sie müssen die Buchungsarten auswählen, die Sie anmahnen wollen. Alle offenen Transaktionen für diese Typen werden in die Berechnung einbezogen.  
2. Wählen Sie im Feld "Mahnschreiben" eine Mahnschreibenoption aus.
3. Geben Sie das Datum des letzten Mahnschreibens an.
    * Es gibt zwei Buchungsprofiloptionen: Konto - Verwenden Sie das Buchungsprofil, das dem Debitorenkonto für die einzelnen Zinsrechnungen zugewiesen ist.   Auswählen – Dient zum Verwenden des im Feld "Buchungsprofil" ausgewählten Buchungsprofils.  
    * Wählen Sie ein Buchungsprofil aus, wenn Sie "Verwenden des Buchungsprofils aus" in" Auswählen " geändert haben.  
4. Erweitern Sie den Abschnitt "Einzuschließende Datensätze".
5. Klicken Sie auf "Filter".
6. Im Feld "Kriterien" geben Sie eine Debitorenkennung ein. Geben Sie beispielsweise "US-001" ein.
7. Klicken Sie auf "OK".
8. Klicken Sie auf "OK".

## <a name="print-collection-letters"></a>Mahnschreiben drucken
1. Wechseln Sie zu "Kredit und Inkasso" > "Mahnschreiben" > "Mahnschreiben prüfen und verarbeiten".
2. Wählen Sie im Feld "Status" die Option "Erstellt" aus.
3. Wählen Sie im Feld "Gedruckt" die Option "Nicht gedruckt" aus.
4. Klicken Sie auf Drucken.
5. Klicken Sie Mahnung
6. Erweitern Sie den Abschnitt "Einzuschließende Datensätze".
7. Geben Sie das Abschnittsdatum für Buchungen ein.
8. Klicken Sie "OK", um das Mahnschreiben zu drucken.

## <a name="post-the-collection-letter"></a>Mahnschreiben buchen
1. Klicken Sie auf "Buchen".
2. Geben Sie ein Buchungsdatum für die Mahnung ein.
3. Erweitern Sie den Abschnitt "Einzuschließende Datensätze".
4. Klicken Sie auf "OK".
5. Wählen Sie im Feld "Status" die Option "Gebucht" aus.
6. Wählen Sie im Feld "Gedruckt" eine Option aus.


