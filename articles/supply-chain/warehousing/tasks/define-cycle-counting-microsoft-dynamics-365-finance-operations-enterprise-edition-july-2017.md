--- 
title: "Zykluszählung definieren "
description: "Zykluszählung ist ein Lagerortprozess, den Sie verwenden können, um Artikel des verfügbaren Lagerbestands zu überwachen."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f9cdb0a7de0199363279c53e817c98085b31fe6b
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="define-cycle-counting"></a>Zykluszählung definieren  

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Zykluszählung ist ein Lagerortprozess, den Sie verwenden können, um Artikel des verfügbaren Lagerbestands zu überwachen. Diese Aufgabenerfassung zeigt, wie Sie: eine standardmäßige Inventurarbeitspriorität einrichten; ein Menüelement des mobilen Geräts aktivieren, um Entnahme und Zähleroperationen zu verarbeiten; einen Inventurschwellenwertauslöser aktivieren, wenn ein Lagerplatz leer wird; einen Zykluszählungsplan für einen bestimmten Artikel innerhalb eines bestimmten Lagerorts aktivieren. Normalerweise werden diese Aufgaben von einem Lagerortleiter ausgeführt. Sie können diese Prozedur Schritt für Schritt im Demodatenunternehmen USMF durchführen oder können Ihre eigenen Daten verwenden.


## <a name="set-the-priority-of-counting-work"></a>Priorität der Inventurarbeit festlegen.
1. Wechseln Sie zu "Lagerortverwaltung" > "Einstellungen" > "Lagerortverwaltungsparameter".
2. Klicken Sie auf die Registerkarte "Permanente Inventurprüfung".
3. Geben Sie im Feld "Standardmäßige Arbeitspriorität für Zykluszählung" eine Zahl ein.
    * Dieser Schritt ändert die Priorität der Zykluszählungsarbeit im Vergleich zu anderen Arten Arbeit am Lagerort. Wenn Sie eine niedrigere Nummer für die Zykluszählung als für andere Arbeitsarten setzen, steigt die Priorität der Zykluszählungsarbeit an.  
4. Klicken Sie auf "Speichern".
5. Schließen Sie die Seite.

## <a name="enable-the-mobile-device"></a>Aktivieren des mobilen Geräts.
1. Wechseln Sie zu "Lagerortverwaltung" > "Einstellungen" > "Mobiles Gerät" > "Menüoptionen für mobiles Gerät".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Menüoptionsname" einen Wert ein.
4. Geben Sie im Feld "Titel" einen Wert ein.
5. Wählen Sie im Feld "Modus" "Arbeit"aus.
6. Legen Sie die "Vorhandene Arbeit verwenden"-Option mit "Ja" fest.
    * Wenn Sie diese Option auswählen, sucht das System nach vorhandener Arbeit, wenn das Menüelement des mobilen Geräts verwendet wird.  
7. Wählen Sie "Systemgeleitet" im Feld "Geleitet von".
    * Wenn "das referenzierte System" aktiviert ist, ist der Lagerarbeiter aufgefordert, Arbeit zu öffnen, die im definierten Arbeitsklassen ist. (Wir erstellen diese Arbeitsklassen weiter)  
8. Erweitern oder reduzieren Sie den Abschnitt 'Arbeitsklassen'.
    * Nun erstellen wir zwei Arbeitsklassen, die mit dem Menüelement des mobilen Geräts verwendet werden. Wenn das Menüelement verwendet wird, werden diese Arbeitsklassen abgefragt, und dadurch wird dem Benutzer die Arbeit mit der höchsten Priorität angezeigt.  
9. Klicken Sie auf "Neu".
10. Wählen Sie im Feld "Arbeitsklassenkennung" einen Wert aus.
11. Klicken Sie auf "Neu".
12. Wählen Sie im Feld "Arbeitsklassenkennung" einen Wert aus.
13. Klicken Sie auf "Speichern".
14. Schließen Sie die Seite.
15. Wechseln Sie zu "Lagerortverwaltung" > "Einstellungen" > "Mobiles Gerät" > "Menü für mobiles Gerät".
16. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
17. Wählen Sie in der Struktur das Menüelement aus, das Sie soeben erstellt haben.
18. Klicken Sie auf "Bearbeiten".
19. Klicken Sie auf den Pfeil, um das Menüelement dem Menü hinzuzufügen.
20. Klicken Sie auf "Speichern".

## <a name="create-a-counting-threshold"></a>Schwellenwert für Zykluszählung erstellen
1. Wechseln Sie zu Lagerortverwaltung > Einrichten > Permanente Inventur > Permanente Inventur-Schwellenwerte.
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Schwellenwertkennung für Zykluszählung" einen Wert ein.
4. Legen Sie die Option "Zykluszählung sofort verarbeiten" auf "Ja" fest.
5. Geben Sie im Feld "Beschreibung" einen Wert ein.
6. Klicken Sie auf Speichern.
7. Klicken Sie auf "Lagerplätze auswählen".
8. Markieren Sie in der Liste die ausgewählte Zeile.
9. Wählen Sie im Feld "Kriterien" einen Wert aus.
10. Klicken Sie auf "OK".
11. Schließen Sie die Seite.

## <a name="create-a-cycle-count-plan"></a>Zykluszählungsplan erstellen
1. Wechseln Sie zu Lagerortverwaltung > Einrichten > Permanente Inventur > Permanenten Inventurplan erstellen.
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Zykluszählungs-Plankennung" einen Wert ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
5. Geben Sie im Feld "Maximale Anzahl von Zykluszählungen" eine Zahl ein.
6. Klicken Sie auf Speichern.
7. Klicken Sie auf "Lagerplätze auswählen".
8. Markieren Sie in der Liste die ausgewählte Zeile.
9. Wählen Sie im Feld "Kriterien" einen Wert aus.
10. Klicken Sie auf "OK".
11. Geben Sie im Feld "Tage zwischen Zykluszählung" eine Zahl ein.
    * Wenn beispielsweise der Wert, der im Feld "Tage zwischen permanenter Inventur" angegeben ist, 5 ist, wird die permanente Inventurarbeit alle fünf Tage erstellt. Wenn jedoch Zykluszählungsarbeit an Tag drei verarbeitet wird, wird die nächste Zykluszählungsarbeit fünf Tage nachdem die letzte Zyklusinventur verarbeitet wurde, erstellt, am Tag acht.  
12. Klicken Sie auf "Speichern".
13. Klicken Sie auf "Neu".
14. Geben Sie im Feld "Laufende Nummer" eine Zahl ein.
    * Die Sortierreihenfolge ist von der kleinsten Nummer zur größten Nummer. Der Wert muss größer als 0 (null) sein.  
15. Markieren Sie in der Liste die ausgewählte Zeile.
16. Geben Sie im Feld "Beschreibung" einen Wert ein.
17. Klicken Sie auf Speichern.
18. Produktabfrage definieren anklicken.
19. Markieren Sie in der Liste die ausgewählte Zeile.
20. Geben Sie im Feld "Kriterien" einen Wert ein oder wählen Sie einen Wert aus.
21. Klicken Sie auf "OK".
22. Schließen Sie die Seite.


