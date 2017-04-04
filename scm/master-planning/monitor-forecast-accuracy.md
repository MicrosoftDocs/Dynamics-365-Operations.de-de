---
title: Bildschirmplanungsrichtigkeit
description: "In diesem Artikel wird beschrieben die Typen der Planungs richtigkeit, die Microsoft Dynamics 365 für Arbeitsgänge berechnet, und es wird beschrieben, wie Sie die Richtigkeitswerte anzeigen können."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: d3f88a4fa54217cea909c54955de05e2175db0cd
ms.lasthandoff: 03/29/2017


---

# <a name="monitor-forecast-accuracy"></a>Bildschirmplanungsrichtigkeit

In diesem Artikel wird beschrieben die Typen der Planungs richtigkeit, die Microsoft Dynamics 365 für Arbeitsgänge berechnet, und es wird beschrieben, wie Sie die Richtigkeitswerte anzeigen können.

Dynamics 365 für Arbeitsgänge berechnet die folgenden Typen der Planungsrichtigkeit:

-   Genauigkeit der historischen Planung durch Vergleich der historischen Planung, die der Produktprogrammplan verwendet, mit dem historischen Bedarf. Um die Werte (absolute Werte und Prozentwerte) für die Genauigkeit der historischen Planung anzuzeigen, klicken Sie auf **Genauigkeit anzeigen** auf der Seite **Bedarfsplanungsdetails**.
-   Die geschätzte Genauigkeit des Planungsmodells, das verwendet wird, um die Vorhersagen zu generieren. Sie können die prozentuale Genauigkeit unter **Modelldetails - MAPE** auf der Seite **Bedarfsplanungsdetails** anzeigen. 

** Hinweis: ** Wenn Sie das Arbeitsgangs-Bedarfsplanungs-MicrosoftAzure-Lernfähigkeit-einer Dynamics 365 für Maschineservice verwenden, lautet die Berechnung des internen Projekt-Planzahlenmodells Genauigkeit auf dem Testdataset. Geben Sie die Größe des Testdatasets anzugeben, legen Sie den TESTEN Sie GRÖSSEN- ** Sie \_PROZENT\_\_FESTGELEGTES ** Parameter auf der Seite Bedarfsplanungsparameter ** ** fest. Wenn Sie zum Beispiel den Wert auf **20** gesetzt haben, werden die letzten 20 Prozent der historischen Daten verwendet, um die interne Modellgenauigkeit zu berechnen.


<a name="see-also"></a>Siehe auch
--------

[Authorizing the adjusted forecast](authorize-adjusted-forecast.md)

[Remove outliers from historical transaction data when calculating a demand forecast](remove-historical-outliers-calculating-demand-forecast.md)


