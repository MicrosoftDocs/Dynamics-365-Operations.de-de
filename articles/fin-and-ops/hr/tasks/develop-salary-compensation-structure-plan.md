--- 
title: "Gehalts-/Vergütungsstruktur und -pläne entwickeln"
description: "Diese Aufgabe führt Schritt für Schritt durch den Prozess der Erstellung eines \"Festen Vergütungsplans\" und ermöglicht es Mitarbeitern, in dem Plan durch Berechtigungsregeln registriert zu werden."
author: kherr75
manager: AnnBe
ms.date: 11/01/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: d2a4a0b2bf2d33530dedc7ce3974ee558d063878
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---
# <a name="develop-salarycompensation-structure-and-plans"></a>Gehalts-/Vergütungsstruktur und -pläne entwickeln

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Diese Aufgabe führt Schritt für Schritt durch den Prozess der Erstellung eines "Festen Vergütungsplans" und ermöglicht es Mitarbeitern, in dem Plan durch Berechtigungsregeln registriert zu werden. Das Demodatunternehmen, das verwendet wird, um diese Aufgabe erstellen, ist USMF, und die Aufgabe ist für "Leiter Vergütungen/Bezüge" bestimmt.


## <a name="create-fixed-compensation-plan"></a>Erstellen eines festen Vergütungsplans.
1. Klicken Sie auf "Vergütungsverwaltung".
2. Klicken Sie auf feste Vergütungspläne.
3. Klicken Sie auf "Neu".
4. Geben Sie im Feld "Plan" einen Wert ein.
5. Geben Sie im Feld "Beschreibung" einen Wert ein.
6. Geben Sie im Feld "Gültigkeitsdatum" ein Datum ein.
7. Wählen Sie im Feld "Typ" aus, ob der "Feste Vergütungsplan" ein "Bereichs-", "Klassen-" oder "Stufenplan" ist.
8. Das Kontrollkästchen "Empfehlung erlaubt" fungiert als Standardwert für alle Aktivitäten, die zu diesem Plan in einem "Prozessereignis" hinzugefügt wurden.  Das Zulassen von Empfehlungen bietet Ihnen die Möglichkeit, den berechneten Richtbetrag zu überschreiben, wenn die Vergütung verarbeitet wird.
9. Die "Außerhalb des zulässigen Bereichs (Toleranz)" ermöglicht es Ihnen anzugeben, wie Vergütungsbeträge gehandhabt werden sollen, die außerhalb des angegebenen Vergütungsstrukturbereich für die bestimmte Ebene liegen.  Eine Auswahl von "Kein" bei "Außerhalb des zulässigen Bereichs (Toleranz)" ermöglicht, dass ein beliebiger Vergütungsbetrag verwendet wird.  Bei "Eingeschränkte Toleranz" erhält der Benutzer eine Warnung, wenn der Vergütungsbetrag geringer als der minimale Referenzpunktbetrag für diese Ebene ist oder größer als der Höchstbetrag für diese Ebene ist. Der Benutzer kann die Warnung ignorieren und fortfahren.  Eine "Uneingeschränkte Toleranz" generiert einen Fehler, wenn eine Mitarbeitervergütung außerhalb der Minimal- und Maximalreferenzpunkte für die Ebene festgelegt ist und wird die Mitarbeitervergütung automatisch anpassen, damit sie innerhalb des Bereichs fällt.
10. Das Feld "Einstellungsregel" wird verwendet, wenn ein "Prozessereignis" zur Vergütung ausgeführt wird, um die Vergütung eines Mitarbeiters zu berechnen.  Eine "Einstellungsregel" mit "Prozent" berechnet eine Erhöhung, die anteilig für die Länge der Zeit berechnet wird, während die Arbeitskraft in einem Zyklus beschäftigt war.
11. Geben Sie im Feld "Währung" einen Wert ein.
12. Geben Sie im Feld "Lohnsatzumwandlung" einen Wert ein, oder wählen Sie einen Wert aus.
13. Erweitern Sie den Abschnitt "Matrix für Bereichsauslastung".
    * Fügen Sie optional Bereichsauslastungsdatensätze hinzu, damit Mitarbeiter schneller zu ihrem Mittelwert gelangen und langsamer den Maximalwert ihres Bereichs erreichen.  
14. An diesem Punkt müssen Sie den "Festen Vergütungsplan" speichern, um die Schaltfläche Vergütung einrichten" zu aktivieren und das Definieren der Vergütungsstruktur für den Plan fortzusetzen.  Klicken Sie auf "Speichern".
15. Klicken Sie auf "Vergütung einrichten".
    * Es gibt drei Möglichkeiten, um eine Vergütungsstruktur zu erstellen. 1: Erstellen Sie eine vollständig neue Struktur, indem Sie eine Gruppe von Referenzpunkten auswählen und die Ebenen hinzufügen, um Ihre eigene Struktur zu erstellen. 2: Kopieren Sie eine Vergütungsstruktur aus einem vorhandenen Plan als Ausgangspunkt und ändern Sie sie für den neuen Plan. 3: Wählen Sie ein bestehendes Vergütungsraster aus. Wenn das Vergütungsraster bereits von einem anderen Plan verwendet wird, spiegeln sich alle Änderungen, die am Raster vorgenommen werden, auch im anderen Plan wieder.  
16. Wählen Sie die Option "Neue Vergütungsmatrix aufgrund der bestehenden Matrix erstellen" aus.
17. Geben Sie im Feld "Aus Raster kopieren" einen Wert ein, oder wählen Sie einen Wert aus.
    * Optional können Sie den Namen des neuen das Vergütungsrasters ändern, das als Kopie des ausgewählten Rasters erstellt wird.  
18. Klicken Sie auf "OK".
19. Klicken Sie auf "Massenänderung".
    * Massenänderung ermöglicht Ihnen, die Vergütungsmatrixbeträge zu verwalten, indem Sie einen Prozentsatz oder eine feste Betragserhöhung bei einem oder mehreren Ebenen und/oder Referenzpunkten anwenden.  
20. Geben Sie im Feld "Regulierungsbetrag" eine Zahl ein.
21. Markieren Sie alle Zeilen in der Liste, oder heben Sie die Markierung auf.
22. Klicken Sie auf "Auf Raster anwenden".
23. Schließen Sie die Seite.
    * Sobald eine Vergütungsstruktur erstellt oder ausgewählt wurde, können Sie auswählen, welche der Referenzpunkte als der Kontrollpunkt für den "Festen Vergütungsplan" verwendet werden sollte.  Der Kontrollpunkt wird verwendet, um die Compa-Ratio eines Mitarbeiters zu errechnen.  
24. Geben Sie im Feld "Kontrollpunkt" einen Wert ein, oder wählen Sie einen Wert aus.
25. Schließen Sie die Seite.

## <a name="create-an-eligibility-rule-for-the-new-fixed-compensation-plan"></a>Eine Berechtigungsregel für den neuen "Festen Vergütungsplan" erstellen
    * Der neue "Festen Vergütungsplan" kann nicht einem Mitarbeiter zugewiesen werden, bevor die "Berechtigungsregeln" für den Plan definiert wurden.  
1. Klicken Sie auf Berechtigungsregeln.
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Berechtigung" einen Wert ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
5. Geben Sie im Feld "Gültigkeitsdatum" ein Datum ein.
    * Berechtigungsregeln werden sowohl für "Feste Vergütungspläne" als auch für "Variable Vergütungspläne" verwendet.  Wählen Sie im Feld "Typ" aus, für welchen Typ von Plan dieser Satz von Berechtigungsregeln bestimmt ist.  
6. Geben Sie im Feld "Plan" einen Wert ein, oder wählen Sie einen Wert aus.
    * Wählen Sie die Kriterien aus, die ein Mitarbeiter erfüllen muss, um für den Vergütungsplan berechtigt zu sein. Kriterien können eine Abteilung, einen Gewerkschaft, einen Lagerplatz (Kompensationsregion), eine Stelle, eine Funktion, einen Stellentyp oder eine Vergütungsstufe enthalten. Der Mitarbeiter muss alle angegebenen Kriterien erfüllen, um für den Vergütungsplan berechtigt zu sein. Wenn keine Kriterien angegebenen wurden, sind alle Mitarbeiter für den Vergütungsplan berechtigt. Wenn ein Mitarbeiter nicht die Kriterien erfüllt, die in der Berechtigungsregel angegeben sind oder eine Berechtigungsregel nicht für einen Vergütungsplan festgelegt wurde, wird der Vergütungsplan nicht in der Suche angezeigt, wenn ein "Fester Vergütungsdatensatz" für einen Mitarbeiter erstellt wird.  
7. Schließen Sie die Seite.
8. Schließen Sie die Seite.


