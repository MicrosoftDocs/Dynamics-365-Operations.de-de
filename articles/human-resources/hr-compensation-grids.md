---
title: Vergütungsraster einrichten
description: Vergütungsstrukturen werden zur Definition und Pflege der Vergütungsstrukturen für feste Vergütungspläne verwendet.
author: twheeloc
ms.date: 01/03/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HRCCompGrid, HRCCompGridView, HcmCompensationWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9119c15cf80b9ebb9bed83ac438f24249aa4aa2f
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8691672"
---
# <a name="set-up-compensation-grids"></a>Vergütungsraster einrichten


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Vergütungsstrukturen werden zur Definition und Pflege der Vergütungsstrukturen für feste Vergütungspläne verwendet. Vergütungsraster können zwischen mehreren Plänen geteilt oder kopiert werden, wenn Sie einen neuen Vergütungsplan erstellen.  Vor dem Erstellen eines Vergütungsrasters müssen Ebenen und Referenzpunkte eingerichtet werden. In diesem Beispiel erstellen Sie einen neuen Gradtyp für Vergütungsraster mit Demodaten für Ebenen und Referenzpunkte. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.


## <a name="set-up-information-about-the-compensation-grid"></a>Informationen zum Vergütungsraster einrichten
1. Navigieren Sie zu **Personalverwaltung** > **Vergütung** > **Feste Vergütung** > **Vergütungsraster**.
2. Klicken Sie auf **Neu**.
3. Geben Sie im Feld **Raster** einen Wert ein.
4. Geben Sie im Feld **Beschreibung** einen Wert ein.
5. Wählen Sie im Feld **Typ** eine Option aus.
6. Geben Sie im Feld **Referenz**-Einstellungen einen Wert ein, oder wählen Sie einen Wert aus.
7. Geben Sie im Feld **Währung** einen Wert ein, oder wählen Sie einen Wert aus.
8. Geben Sie im Feld **Gültigkeitsdatum** ein Datum ein.

## <a name="add-levels-to-the-compensation-structure"></a>Level zur Vergütungsstruktur hinzufügen
1. Klicken Sie auf **Vergütungsstruktur**.
2. Markieren Sie in der Liste die ausgewählte Zeile.
3. Geben Sie im Feld **Level** einen Wert ein, oder wählen Sie einen Wert aus.
4. Klicken Sie auf **Neu**.
5. Markieren Sie in der Liste die ausgewählte Zeile.
6. Geben Sie im Feld **Level** einen Wert ein, oder wählen Sie einen Wert aus.
7. Klicken Sie auf **Neu**.
8. Markieren Sie in der Liste die ausgewählte Zeile.
9. Geben Sie im Feld **Level** einen Wert ein, oder wählen Sie einen Wert aus.
10. Klicken Sie auf **Neu**.
11. Markieren Sie in der Liste die ausgewählte Zeile.
12. Geben Sie im Feld **Level** einen Wert ein, oder wählen Sie einen Wert aus.
13. Klicken Sie auf **Neu**.
14. Markieren Sie in der Liste die ausgewählte Zeile.
15. Geben Sie im Feld **Level** einen Wert ein, oder wählen Sie einen Wert aus.

## <a name="fill-in-the-compensation-structure-with-values"></a>Füllen der Vergütungsstruktur mit Werten
1. Markieren Sie in der Liste die ausgewählte Zeile.
    * An diesem Punkt können Vergütungswerte manuell in jedes Feld in der Tabelle eingegeben werden, oder die Massenänderungsfunktionen kann zum Eintragen von mehreren Felder und für grundlegende Berechnungen verwendet werden.  
2. Klicken Sie auf **Massenänderung**.
    * Bei diesem Raster wenden wir zuerst den Wert den Mittelwert der ersten Ebene auf alle Felder in der Tabelle an. Dies dient als Grundlage für die Vergütungsmatrix.  
3. Wählen Sie im Feld **Regulierungstyp** eine Option aus.
4. Geben Sie in das Feld **Anpassungsbetrag** eine Zahl ein.
5. Markieren Sie alle Zeilen in der Liste, oder heben Sie die Markierung auf.
6. Klicken Sie auf **Anwendung auf Raster**.
    * Jetzt verwenden wir die Massenänderungsfunktion, um die Beträge in jeder nächste Ebene über einen bestimmten Prozentsatz oder Betrag zu erhöhen. In diesem Beispiel hat jeder Grad einen Umfang von 12,5% zwischen den Mittelwerten.  
7. Wählen Sie im Feld **Regulierungstyp** eine Option aus.
8. Geben Sie in das Feld **Anpassungsbetrag** eine Zahl ein.
9. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
10. Klicken Sie auf **Anwendung auf Raster**.
    * Jetzt verwenden wir die Massenänderungsfunktion, um die Mindest- und Höchstwerte für Referenzpunkte auf jede Ebene einzustellen. In diesem Beispiel wird ein Umfang von 50 % verwendet, so das der minimale Referenzpunkt um -20% und der maximale um +20% reguliert wird.  
11. Geben Sie in das Feld **Anpassungsbetrag** eine Zahl ein.
12. Geben Sie im Feld **Referenzpunkt** einen Wert ein, oder wählen Sie einen Wert aus.
13. Markieren Sie alle Zeilen in der Liste, oder heben Sie die Markierung auf.
14. Klicken Sie auf **Anwendung auf Raster**.
15. Geben Sie in das Feld **Anpassungsbetrag** eine Zahl ein.
16. Geben Sie im Feld **Referenzpunkt** einen Wert ein, oder wählen Sie einen Wert aus.
17. Markieren Sie alle Zeilen in der Liste, oder heben Sie die Markierung auf.
18. Klicken Sie auf **Anwendung auf Raster**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
