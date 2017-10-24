---
title: Eine angepasste Planung autorisieren
description: "Nicht alle Planungsdaten müssen sofort autorisiert werden. In diesem Artikel wird beschrieben, wie Sie die Periode angeben können, für die eine Planung autorisiert ist. Er erläutert auch, wie Sie die Planung für bestimmte Unternehmen und Planzahlenmodelle autorisieren können."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanImportForecastDialog
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 72734
ms.assetid: cb8fd809-605a-4a8b-a390-636edfec21f9
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 399a7a21ec71fe50e280ccb24699cda76d571990
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="authorize-an-adjusted-forecast"></a><span data-ttu-id="f37a3-105">Eine angepasste Planung autorisieren</span><span class="sxs-lookup"><span data-stu-id="f37a3-105">Authorize an adjusted forecast</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="f37a3-106">Nicht alle Planungsdaten müssen sofort autorisiert werden.</span><span class="sxs-lookup"><span data-stu-id="f37a3-106">Not all forecast data must be authorized immediately.</span></span> <span data-ttu-id="f37a3-107">In diesem Artikel wird beschrieben, wie Sie die Periode angeben können, für die eine Planung autorisiert ist.</span><span class="sxs-lookup"><span data-stu-id="f37a3-107">This article explains how you can specify the period that a forecast is authorized for.</span></span> <span data-ttu-id="f37a3-108">Er erläutert auch, wie Sie die Planung für bestimmte Unternehmen und Planzahlenmodelle autorisieren können.</span><span class="sxs-lookup"><span data-stu-id="f37a3-108">It also explains how you can authorize the forecast for specific companies and forecast models.</span></span>

<span data-ttu-id="f37a3-109">Nicht alle Planungsdaten müssen sofort autorisiert werden.</span><span class="sxs-lookup"><span data-stu-id="f37a3-109">Not all forecast data must be authorized immediately.</span></span> <span data-ttu-id="f37a3-110">Sie können das Start- und Enddatum der Periode angeben, für die die Planung autorisiert ist.</span><span class="sxs-lookup"><span data-stu-id="f37a3-110">You can specify the start and end dates of the period that the forecast is authorized for.</span></span> <span data-ttu-id="f37a3-111">Diese Funktion lässt Sie bestimmte Zeitrahmen einfrieren.</span><span class="sxs-lookup"><span data-stu-id="f37a3-111">This functionality lets you freeze specific buckets.</span></span> 

<span data-ttu-id="f37a3-112">Das Start- und Enddatum, das Sie angeben, muss dem Start- und Enddatum der Liste entsprechen, in der die Planung generiert wird.</span><span class="sxs-lookup"><span data-stu-id="f37a3-112">The start and end dates that you specify must correspond to the start and end dates of the bucket that the forecast is generated in.</span></span> <span data-ttu-id="f37a3-113">Das System setzt diese Einschränkung durch und reguliert automatisch die Daten, wenn eine Regulierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="f37a3-113">The system enforces this restriction and automatically adjusts the dates, if adjustment is required.</span></span> 

<span data-ttu-id="f37a3-114">Auf der Registerkarte **Details** der Seite **Autorisierung** können Sie Details zur Planung anzeigen, die zuletzt generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="f37a3-114">On the **Details** tab of the **Authorization** page, you can view details about the forecast that was most recently generated.</span></span> 

<span data-ttu-id="f37a3-115">Sie können die Unternehmen und die Planzahlenmodelle auswählen, um die Planung für die Verwendung zu autorisieren.</span><span class="sxs-lookup"><span data-stu-id="f37a3-115">You can select the companies and the forecast models to authorize the forecast for use.</span></span> <span data-ttu-id="f37a3-116">Standardmäßig umfasst das Raster alle Unternehmen, für die der Planungsbedarf erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="f37a3-116">By default, the grid includes all the companies that forecast demand has been created for.</span></span> <span data-ttu-id="f37a3-117">Für jedes Unternehmen wird das Planzahlenmodell, das dem aktuellen Absatzplan entspricht, der in den Produktprogrammplanungsparametern eingerichtet ist, vorab ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="f37a3-117">For each company, the forecast model that corresponds to the current forecast plan that is set up in the master planning parameters is prefilled.</span></span> <span data-ttu-id="f37a3-118">Sie können dieses Planzahlenmodell jedoch in ein beliebiges anderes Planzahlenmodell ändern, das zu diesem Unternehmen gehört.</span><span class="sxs-lookup"><span data-stu-id="f37a3-118">However, you can change this forecast model to any forecast model that belongs to that company.</span></span> <span data-ttu-id="f37a3-119">Wenn keine Bedarfsplanungsdaten für ein ausgewähltes Unternehmen generiert wurden, wird beim Import eine Warnmeldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f37a3-119">If no forecast demand data has been generated for a selected company, you receive a warning message at import time.</span></span> 

<span data-ttu-id="f37a3-120">Es ist außerordentlich wichtig, dass Sie verstehen, wie das Kontrollkästchen **Manuelle Anpassungen der Grundbedarfsplanung speichern** funktioniert.</span><span class="sxs-lookup"><span data-stu-id="f37a3-120">It's very important that you understand how the **Save the manual adjustments made to the baseline demand forecast** check box works.</span></span> <span data-ttu-id="f37a3-121">Wenn Sie die manuelle Anpassungen an der statistischen Grundplanung vorgenommen haben, werden die angepassten Werte autorisiert, auch wenn dieses Kontrollkästchen deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="f37a3-121">If you've made manual adjustments to the statistical baseline forecast, the adjusted values are authorized for use, even if this check box is cleared.</span></span> <span data-ttu-id="f37a3-122">Allerdings werden die Änderungen nach der Autorisierung verworfen.</span><span class="sxs-lookup"><span data-stu-id="f37a3-122">However, the changes are discarded after the authorization.</span></span> <span data-ttu-id="f37a3-123">Daher ist beim nächsten Generieren einer Planung diese Planung nur eine statistische Planung und hat keine Korrekturmöglichkeiten, auch wenn **Manuelle Anpassungen auf Bedarfsplanung übertragen** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="f37a3-123">Therefore, the next time that a forecast is generated, that forecast is only a statistical forecast and doesn't have any manual overrides, even if **Transfer manual adjustments to the demand forecast** is selected.</span></span> <span data-ttu-id="f37a3-124">Daher können Sie das Kontrollkästchen **Manuelle Anpassungen der Grundbedarfsplanung speichern** als einen Mechanismus ansehen, mit dem Sie alle manuellen Änderungen beibehalten oder verwerfen können.</span><span class="sxs-lookup"><span data-stu-id="f37a3-124">Therefore, you can consider the **Save the manual adjustments made to the baseline demand forecast** check box a mechanism that lets you keep or discard all manual changes.</span></span>

<a name="see-also"></a><span data-ttu-id="f37a3-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f37a3-125">See also</span></span>
--------

[<span data-ttu-id="f37a3-126">Manuelle Anpassungen an die Grundplanung</span><span class="sxs-lookup"><span data-stu-id="f37a3-126">Making manual adjustments to the baseline forecast</span></span>](manual-adjustments-baseline-forecast.md)

[<span data-ttu-id="f37a3-127">Überwachen der Planungsgenauigkeit</span><span class="sxs-lookup"><span data-stu-id="f37a3-127">Monitoring forecast accuracy</span></span>](monitor-forecast-accuracy.md)




