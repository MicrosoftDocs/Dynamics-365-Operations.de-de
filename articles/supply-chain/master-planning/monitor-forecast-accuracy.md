---
title: Überwachen der Planungsgenauigkeit
description: In diesem Artikel werden die Typen der Planungsgenauigkeit beschrieben, die Dynamics 365 Supply Chain Management berechnet, und es wird erklärt, wie Sie die Genauigkeitswerte anzeigen können.
author: t-benebo
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanForecastDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 76248d87533fd233b255060aa278c76e13719700
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740738"
---
# <a name="monitor-forecast-accuracy"></a>Überwachen der Planungsgenauigkeit

[!include [banner](../includes/banner.md)]

In diesem Artikel werden die Typen der Planungsgenauigkeit beschrieben, die Microsoft Dynamics 365 Supply Chain Management berechnet, und es wird erklärt, wie Sie die Genauigkeitswerte anzeigen können.

Supply Chain Management berechnet die folgenden Typen der Planungsgenauigkeit:

-   Genauigkeit der historischen Planung durch Vergleich der historischen Planung, die der Produktprogrammplan verwendet, mit dem historischen Bedarf. Um die Werte (absolute Werte und Prozentwerte) für die Genauigkeit der historischen Planung anzuzeigen, klicken Sie auf **Genauigkeit anzeigen** auf der Seite **Bedarfsplanungsdetails**.
-   Die geschätzte Genauigkeit des Planungsmodells, das verwendet wird, um die Vorhersagen zu generieren. Sie können die prozentuale Genauigkeit unter **Modelldetails - MAPE** auf der Seite **Bedarfsplanungsdetails** anzeigen. 

> [!NOTE]
> Wenn Sie den Machine Learning-Dienst der Microsoft Azure-Bedarfsplanung verwenden, basiert die Berechnung der internen Modellgenauigkeit auf dem Testdataset. Um die Größe des Testdatasets anzugeben, legen Sie den Parameter **TEST\_SET\_SIZE\_PERCENT** Parameter auf der Seite **Bedarfsplanungsparameter** fest. Wenn Sie zum Beispiel den Wert auf **20** gesetzt haben, werden die letzten 20 Prozent der historischen Daten verwendet, um die interne Modellgenauigkeit zu berechnen.


## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Eine angepasste Planung autorisieren](authorize-adjusted-forecast.md)
- [Entfernen Sie Ausreißer aus den historischen Buchungsdaten, wenn Sie eine Bedarfsplanung berechnen.](remove-historical-outliers-calculating-demand-forecast.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]