---
title: Abschreibungsmethoden und -konventionen
description: "Dieser Artikel gibt einen Überblick über die Abschreibungskonventionen und Abschreibungsmethoden, die von Microsoft Dynamics AX unterstützt werden."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetDepreciationProfile, AssetGroupBookSetup, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3441
ms.assetid: 1d8267b1-86a8-44bf-8814-f56b5d45a0ae
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 8e89a57dda8f2d392483ed13c686ea97b74926b0
ms.openlocfilehash: 51c053e6c130d20258e02284d097431a18bb38cb
ms.lasthandoff: 03/31/2017


---

# <a name="depreciation-methods-and-conventions"></a>Abschreibungsmethoden und -konventionen

Dieser Artikel gibt einen Überblick über die Abschreibungskonventionen und Abschreibungsmethoden, die von Microsoft Dynamics AX unterstützt werden.

Es können verschiedene Abschreibungsmethoden und -konventionen ausgewählt werden. Zweck der Methoden ist die Verteilung des abschreibungsfähigen Werts der Anlage auf Finanzzeiträume. Der abschreibungsfähige Wert der Anlage ist der Anschaffungspreis abzüglich eines Schrottwerts (sofern zutreffend). 

Wenn Sie bei der Verwendung von Abschreibungskonventionen das letzte Ausführungsdatum der Abschreibung für eine Anlage ändern, woraufhin einige Abschreibungen übersprungen werden, ist die Abschreibung für das letzte Jahr möglicherweise größer oder kleiner als erwartet. Die Abschreibung wird durch die Anzahl der Abschreibungszeiträume reguliert, die von der Änderung des letzten Anfangsdatums der Abschreibung betroffen sind.

Wenn Sie zum Beispiel die Abschreibungskonvention "Halbjahr" über einen Zeitraum von drei Jahren verwenden, erstreckt sich der Abschreibungszeitraum in der Regel auf 3,5 Jahre. Wenn Sie das letzte Anfangsdatum während dieser 3,5 Jahre ändern, wird das letzte Abschreibungsjahr um die Anzahl der betroffenen Zeiträume verlängert. Verschieben Sie z. B. das Datum um drei Monate, umfasst das letzte Jahr neun Abschreibungsmonate, während es normalerweise sechs Monate umfassen würde.

Die folgenden Abschreibungskonventionen stehen zur Auswahl.


-   Halbjahr
-   Ganzer Monat
-   Quartalsmitte
-   Monatsmitte (1. des Monats)
-   Monatsmitte (15. des Monats)
-   Halbes Jahr (Jahresanfang)
-   Halbes Jahr (nächstes Jahr)

Die folgenden Abschreibungsmethoden stehen zur Auswahl.
-   Lineare Nutzungsdauer
-   Degressiv
-   Manuell
-   Faktor
-   Verbrauch
-   Verbleibende lineare Nutzungsdauer
-   200% degressiv
-   175% degressiv
-   150% degressiv
-   125% degressiv

 



<a name="see-also"></a>Siehe auch
--------

[Fixed asset depreciation](fixed-asset-depreciation.md)

[Straight line service life depreciation](Straight-line-service-life-depreciation.md)

[Reducing balance depreciation](reduce-balance-depreciation.md)

[Manual depreciation](manual-depreciation.md)

[Factor depreciation](factor-depreciation.md)

[Consumption depreciation](consumption-depreciation.md)

[Straight line life remaining depreciation](straight-line-life-remaining-depreciation.md)

125-Prozent-degressiveAbschreibung []( 125 percent-reducing-balance-depreciation.md)

150-Prozent-degressiveAbschreibung []( 150 percent-reducing-balance-depreciation.md)

175-Prozent-degressiveAbschreibung []( 175 percent-reducing-balance-depreciation.md)

[200 percent reducing balance depreciation](200-percent-reducing-balance-depreciation.md)


