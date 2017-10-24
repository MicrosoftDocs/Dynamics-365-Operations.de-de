---
title: Abschreibungsmethoden und -konventionen
description: "Dieser Artikel gibt einen Überblick über die Abschreibungskonventionen und Abschreibungsmethoden, die von Microsoft Dynamics 365 for Finance and Operations, Enterprise edition unterstützt werden."
author: twheeloc
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile, AssetGroupBookSetup, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 3441
ms.assetid: 1d8267b1-86a8-44bf-8814-f56b5d45a0ae
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d802933f29b3e08704480035925b2fbf6743e996
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="depreciation-methods-and-conventions"></a>Abschreibungsmethoden und -konventionen

[!include[banner](../includes/banner.md)]


Dieser Artikel gibt einen Überblick über die Abschreibungskonventionen und Abschreibungsmethoden, die von Microsoft Dynamics 365 for Finance and Operations, Enterprise edition unterstützt werden.

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

[Anlagenabschreibung](fixed-asset-depreciation.md)

[Abschreibungsmethode "Lineare Nutzungsdauer"](Straight-line-service-life-depreciation.md)

[Degressive Abschreibung](reduce-balance-depreciation.md)

[Manuelle Abschreibung](manual-depreciation.md)

[Faktorabschreibung](factor-depreciation.md)

[Verbrauchsabschreibung](consumption-depreciation.md)

[Abschreibungsmethode "Verbleibende lineare Nutzungsdauer"](straight-line-life-remaining-depreciation.md)

[Degressiven Abschreibung von 125 Prozent](125-percent-reducing-balance-depreciation.md)

[Degressiven Abschreibung von 150 Prozent](150-percent-reducing-balance-depreciation.md)

[Degressiven Abschreibung von 175 Prozent](175-percent-reducing-balance-depreciation.md)

[Degressiven Abschreibung von 200 Prozent](200-percent-reducing-balance-depreciation.md)




