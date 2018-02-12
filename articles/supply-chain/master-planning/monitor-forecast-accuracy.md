---
title: "Überwachen der Planungsgenauigkeit"
description: "In diesem Artikel werden die Typen der Planungsgenauigkeit beschrieben, die Microsoft Dynamics 365 Finance and Operations berechnet, und es wird beschrieben, wie Sie die Genauigkeitswerte anzeigen können."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanForecastDetails
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: bd84dde353972d2d259706dd9f8f3621cef04472
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="monitor-forecast-accuracy"></a>Überwachen der Planungsgenauigkeit

[!include[banner](../includes/banner.md)]


In diesem Artikel werden die Typen der Planungsgenauigkeit beschrieben, die Microsoft Dynamics 365 Finance and Operations berechnet, und es wird beschrieben, wie Sie die Genauigkeitswerte anzeigen können.

Finance and Operations berechnet die folgenden Typen der Planungsgenauigkeit:

-   Genauigkeit der historischen Planung durch Vergleich der historischen Planung, die der Produktprogrammplan verwendet, mit dem historischen Bedarf. Um die Werte (absolute Werte und Prozentwerte) für die Genauigkeit der historischen Planung anzuzeigen, klicken Sie auf **Genauigkeit anzeigen** auf der Seite **Bedarfsplanungsdetails**.
-   Die geschätzte Genauigkeit des Planungsmodells, das verwendet wird, um die Vorhersagen zu generieren. Sie können die prozentuale Genauigkeit unter **Modelldetails - MAPE** auf der Seite **Bedarfsplanungsdetails** anzeigen. 

**Hinweis:** Wenn Sie den Microsoft Azure Machine Learning-Dienst der Finance and Operations-Bedarfsplanung verwenden, basiert die Berechnung der internen Modellgenauigkeit auf dem Testdataset. Um die Größe des Testdatasets anzugeben, legen Sie den Parameter **TEST\_SET\_SIZE\_PERCENT** Parameter auf der Seite **Bedarfsplanungsparameter** fest. Wenn Sie zum Beispiel den Wert auf **20** gesetzt haben, werden die letzten 20 Prozent der historischen Daten verwendet, um die interne Modellgenauigkeit zu berechnen.


<a name="see-also"></a>Siehe auch
--------

[Autorisieren der angepassten Planung](authorize-adjusted-forecast.md)

[Entfernen Sie Ausreißer aus den historischen Buchungsdaten, wenn Sie eine Bedarfsplanung berechnen.](remove-historical-outliers-calculating-demand-forecast.md)




