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
ms.sourcegitcommit: 83d9b76334c887a92c357eceeffd36e9a1e65b7f
ms.openlocfilehash: 86b8e5755f5b2591c04ad6f2335d2ed874102a75
ms.contentlocale: de-de
ms.lasthandoff: 01/22/2018

---

# <a name="monitor-forecast-accuracy"></a><span data-ttu-id="296ee-103">Überwachen der Planungsgenauigkeit</span><span class="sxs-lookup"><span data-stu-id="296ee-103">Monitor forecast accuracy</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="296ee-104">In diesem Artikel werden die Typen der Planungsgenauigkeit beschrieben, die Microsoft Dynamics 365 Finance and Operations berechnet, und es wird beschrieben, wie Sie die Genauigkeitswerte anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="296ee-104">This article describes the types of forecast accuracy that Microsoft Dynamics 365 for Finance and Operations calculates, and explains how you can view the accuracy values.</span></span>

<span data-ttu-id="296ee-105">Finance and Operations berechnet die folgenden Typen der Planungsgenauigkeit:</span><span class="sxs-lookup"><span data-stu-id="296ee-105">Finance and Operations calculates the following types of forecast accuracy:</span></span>

-   <span data-ttu-id="296ee-106">Genauigkeit der historischen Planung durch Vergleich der historischen Planung, die der Produktprogrammplan verwendet, mit dem historischen Bedarf.</span><span class="sxs-lookup"><span data-stu-id="296ee-106">Historical forecast accuracy, by comparing the historical forecast that Master Planning uses with the historical demand.</span></span> <span data-ttu-id="296ee-107">Um die Werte (absolute Werte und Prozentwerte) für die Genauigkeit der historischen Planung anzuzeigen, klicken Sie auf **Genauigkeit anzeigen** auf der Seite **Bedarfsplanungsdetails**.</span><span class="sxs-lookup"><span data-stu-id="296ee-107">To view the values (both absolute values and percentage values) for historical forecast accuracy, click **Show accuracy** on the **Demand forecast details** page.</span></span>
-   <span data-ttu-id="296ee-108">Die geschätzte Genauigkeit des Planungsmodells, das verwendet wird, um die Vorhersagen zu generieren.</span><span class="sxs-lookup"><span data-stu-id="296ee-108">The estimated accuracy of the forecasting model that is used to generate the predictions.</span></span> <span data-ttu-id="296ee-109">Sie können die prozentuale Genauigkeit unter **Modelldetails - MAPE** auf der Seite **Bedarfsplanungsdetails** anzeigen.</span><span class="sxs-lookup"><span data-stu-id="296ee-109">You can view the accuracy percentage under **Model details - MAPE** on the **Demand forecast details** page.</span></span> 

<span data-ttu-id="296ee-110">**Hinweis:** Wenn Sie den Microsoft Azure Machine Learning-Dienst der Finance and Operations-Bedarfsplanung verwenden, basiert die Berechnung der internen Modellgenauigkeit auf dem Testdataset.</span><span class="sxs-lookup"><span data-stu-id="296ee-110">**Note:** If you use the Finance and Operations Demand forecasting Microsoft Azure Machine Learning service, the calculation of internal model accuracy is based on the test data set.</span></span> <span data-ttu-id="296ee-111">Um die Größe des Testdatasets anzugeben, legen Sie den Parameter **TEST\_SET\_SIZE\_PERCENT** Parameter auf der Seite **Bedarfsplanungsparameter** fest.</span><span class="sxs-lookup"><span data-stu-id="296ee-111">To specify the size of the test data set, set the **TEST\_SET\_SIZE\_PERCENT** parameter on the **Demand forecasting parameters** page.</span></span> <span data-ttu-id="296ee-112">Wenn Sie zum Beispiel den Wert auf **20** gesetzt haben, werden die letzten 20 Prozent der historischen Daten verwendet, um die interne Modellgenauigkeit zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="296ee-112">For example, if you set the value to **20**, the last 20 percent of the historical data will be used to calculate the internal model accuracy.</span></span>


<a name="see-also"></a><span data-ttu-id="296ee-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="296ee-113">See also</span></span>
--------

[<span data-ttu-id="296ee-114">Autorisieren der angepassten Planung</span><span class="sxs-lookup"><span data-stu-id="296ee-114">Authorizing the adjusted forecast</span></span>](authorize-adjusted-forecast.md)

[<span data-ttu-id="296ee-115">Entfernen Sie Ausreißer aus den historischen Buchungsdaten, wenn Sie eine Bedarfsplanung berechnen.</span><span class="sxs-lookup"><span data-stu-id="296ee-115">Remove outliers from historical transaction data when calculating a demand forecast</span></span>](remove-historical-outliers-calculating-demand-forecast.md)




