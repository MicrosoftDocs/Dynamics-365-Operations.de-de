---
title: Planungsgenauigkeit überwachen
description: In diesem Thema werden die Typen der Planungsgenauigkeit beschrieben, die Dynamics 365 Supply Chain Management berechnet, und es wird erklärt, wie Sie die Genauigkeitswerte anzeigen können.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanForecastDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6f238afadfa064e972ef11a95fdad073f63ff20c
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250667"
---
# <a name="monitor-forecast-accuracy"></a>Planungsgenauigkeit überwachen

[!include [banner](../includes/banner.md)]

In diesem Thema werden die Typen der Planungsgenauigkeit beschrieben, die Microsoft Dynamics 365 Supply Chain Management berechnet, und es wird erklärt, wie Sie die Genauigkeitswerte anzeigen können.

Supply Chain Management berechnet die folgenden Typen der Planungsgenauigkeit:

-   Genauigkeit der historischen Planung durch Vergleich der historischen Planung, die der Produktprogrammplan verwendet, mit dem historischen Bedarf. Um die Werte (absolute Werte und Prozentwerte) für die Genauigkeit der historischen Planung anzuzeigen, klicken Sie auf **Genauigkeit anzeigen** auf der Seite **Bedarfsplanungsdetails**.
-   Die geschätzte Genauigkeit des Planungsmodells, das verwendet wird, um die Vorhersagen zu generieren. Sie können die prozentuale Genauigkeit unter **Modelldetails - MAPE** auf der Seite **Bedarfsplanungsdetails** anzeigen. 

> [!NOTE]
> Wenn Sie den Machine Learning-Dienst der Microsoft Azure-Bedarfsplanung verwenden, basiert die Berechnung der internen Modellgenauigkeit auf dem Testdataset. Um die Größe des Testdatasets anzugeben, legen Sie den Parameter **TEST\_SET\_SIZE\_PERCENT** Parameter auf der Seite **Bedarfsplanungsparameter** fest. Wenn Sie zum Beispiel den Wert auf **20** gesetzt haben, werden die letzten 20 Prozent der historischen Daten verwendet, um die interne Modellgenauigkeit zu berechnen.


<a name="additional-resources"></a>Zusätzliche Ressourcen
--------

[Autorisieren der angepassten Planung](authorize-adjusted-forecast.md)

[Entfernen Sie Ausreißer aus den historischen Buchungsdaten, wenn Sie eine Bedarfsplanung berechnen.](remove-historical-outliers-calculating-demand-forecast.md)



