--- 
title: "Vergütungsraster einrichten"
description: "Vergütungsstrukturen werden zur Definition und Pflege der Vergütungsstrukturen für feste Vergütungspläne verwendet."
author: kherr75
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 33a95e4366dc352f28202155be7fc0b8f4c99e4a
ms.contentlocale: de-de
ms.lasthandoff: 07/28/2017

---
# <a name="set-up-compensation-grids"></a>Vergütungsraster einrichten

[!include[task guide banner](../../includes/task-guide-banner.md)]

Vergütungsstrukturen werden zur Definition und Pflege der Vergütungsstrukturen für feste Vergütungspläne verwendet. Vergütungsraster können zwischen mehreren Plänen geteilt oder kopiert werden, wenn Sie einen neuen Vergütungsplan erstellen.  Vor dem Erstellen eines Vergütungsrasters müssen Ebenen und Referenzpunkte eingerichtet werden. In diesem Beispiel erstellen Sie einen neuen Gradtyp für Vergütungsraster mit Demodaten für Ebenen und Referenzpunkte. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.


## <a name="set-up-information-about-the-compensation-grid"></a>Informationen zum Vergütungsraster einrichten
1. Wechseln Sie zu "Personalverwaltung" > "Vergütung" > "Feste Vergütung" > "Vergütungsraster".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Raster" einen Wert ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
5. Wählen Sie im Feld "Typ" eine Option aus.
6. Geben Sie im Feld 'Referenzeinstellungen' einen Wert ein, oder wählen Sie einen Wert aus.
7. Geben Sie im Feld "Währung" einen Wert ein, oder wählen Sie einen Wert aus.
8. Geben Sie im Feld "Währung" einen Wert ein.
9. Geben Sie im Feld "Gültigkeitsdatum" ein Datum ein.

## <a name="add-levels-to-the-compensation-structure"></a>Level zur Vergütungsstruktur hinzufügen
1. Klicken Sie auf "Vergütungsstruktur".
2. Markieren Sie in der Liste die ausgewählte Zeile.
3. Geben Sie im Feld "Level" einen Wert ein, oder wählen Sie einen Wert aus.
4. Klicken Sie auf Neu.
5. Markieren Sie in der Liste die ausgewählte Zeile.
6. Geben Sie im Feld "Level" einen Wert ein, oder wählen Sie einen Wert aus.
7. Klicken Sie auf Neu.
8. Markieren Sie in der Liste die ausgewählte Zeile.
9. Geben Sie im Feld "Level" einen Wert ein, oder wählen Sie einen Wert aus.
10. Klicken Sie auf Neu.
11. Markieren Sie in der Liste die ausgewählte Zeile.
12. Geben Sie im Feld "Level" einen Wert ein, oder wählen Sie einen Wert aus.
13. Klicken Sie auf Neu.
14. Markieren Sie in der Liste die ausgewählte Zeile.
15. Geben Sie im Feld "Level" einen Wert ein, oder wählen Sie einen Wert aus.

## <a name="fill-in-the-compensation-structure-with-values"></a>Füllen der Vergütungsstruktur mit Werten
1. Markieren Sie in der Liste die ausgewählte Zeile.
    * An diesem Punkt können Vergütungswerte manuell in jedes Feld in der Tabelle eingegeben werden, oder die Massenänderungsfunktionen kann zum Eintragen von mehreren Felder und für grundlegende Berechnungen verwendet werden.  
2. Klicken Sie auf "Massenänderung".
    * Bei diesem Raster wenden wir zuerst den Wert den Mittelwert der ersten Ebene auf alle Felder in der Tabelle an. Dies dient als Grundlage für die Vergütungsmatrix.  
3. Wählen Sie im Feld "Regulierungstyp" eine Option aus.
4. Geben Sie im Feld "Regulierungsbetrag" eine Zahl ein.
5. Markieren Sie alle Zeilen in der Liste, oder heben Sie die Markierung auf.
6. Klicken Sie auf "Auf Raster anwenden".
    * Jetzt verwenden wir die Massenänderungsfunktion, um die Beträge in jeder nächste Ebene über einen bestimmten Prozentsatz oder Betrag zu erhöhen. In diesem Beispiel hat jeder Grad einen Umfang von 12,5% zwischen den Mittelwerten.  
7. Wählen Sie im Feld "Regulierungstyp" eine Option aus.
8. Geben Sie im Feld "Regulierungsbetrag" eine Zahl ein.
9. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
10. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
11. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
12. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
13. Klicken Sie auf "Auf Raster anwenden".
14. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
15. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
16. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
17. Klicken Sie auf "Auf Raster anwenden".
18. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
19. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
20. Klicken Sie auf "Auf Raster anwenden".
21. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
22. Klicken Sie auf "Auf Raster anwenden".
    * Jetzt verwenden wir die Massenänderungsfunktion, um die Mindest- und Höchstwerte für Referenzpunkte auf jede Ebene einzustellen. In diesem Beispiel wird ein Umfang von 50 % verwendet, so das der minimale Referenzpunkt um -20% und der maximale um +20% reguliert wird.  
23. Geben Sie im Feld "Regulierungsbetrag" eine Zahl ein.
24. Geben Sie im Feld 'Referenzpunkt' einen Wert ein, oder wählen Sie einen Wert aus.
25. Markieren Sie alle Zeilen in der Liste, oder heben Sie die Markierung auf.
26. Klicken Sie auf "Auf Raster anwenden".
27. Geben Sie im Feld "Regulierungsbetrag" eine Zahl ein.
28. Geben Sie im Feld 'Referenzpunkt' einen Wert ein, oder wählen Sie einen Wert aus.
29. Markieren Sie alle Zeilen in der Liste, oder heben Sie die Markierung auf.
30. Klicken Sie auf "Auf Raster anwenden".


