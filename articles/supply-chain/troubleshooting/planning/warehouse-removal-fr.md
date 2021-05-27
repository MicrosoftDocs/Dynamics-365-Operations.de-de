---
title: Sie können die Lagerort-Bedarfsplanungsdimension nicht aus den Planungspositionen entfernen
description: Sie können die Lagerort-Bedarfsplanungsdimension nicht aus den Planungspositionen entfernen.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6b643c4fe51ae6ce73b34ab81d4e458dcd5032df
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026544"
---
# <a name="you-cant-remove-the-warehouse-demand-forecast-dimension-from-forecast-lines"></a><span data-ttu-id="49286-103">Sie können die Lagerort-Bedarfsplanungsdimension nicht aus den Planungspositionen entfernen</span><span class="sxs-lookup"><span data-stu-id="49286-103">You can't remove the Warehouse demand forecast dimension from forecast lines</span></span>

<span data-ttu-id="49286-104">KB-Nummer: 4614408</span><span class="sxs-lookup"><span data-stu-id="49286-104">KB number: 4614408</span></span>

## <a name="symptoms"></a><span data-ttu-id="49286-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="49286-105">Symptoms</span></span>

<span data-ttu-id="49286-106">Dieses Problem tritt auf, wenn die Dimension **Lagerort** nicht auf der Registerkarte **Planungsdimensionen** der Seite **Bedarfsplanungsparameter** zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="49286-106">This issue occurs when the **Warehouse** dimension isn't assigned on the **Forecast dimensions** tab of the **Demand forecasting parameter** page.</span></span> <span data-ttu-id="49286-107">Trotzdem ist die Spalte **Lagerplatz** auf der Seite **Bedarfsplanung** angezeigt (**Produktprogrammplanung \> Prognose \> Manuelle Planungseinheit \> Bedarfsplanungspositionen**).</span><span class="sxs-lookup"><span data-stu-id="49286-107">Nevertheless, the **Warehouse** column is shown on the **Demand forecast** page (**Master planning \> Forecasting \> Manual forecast entity \> Demand forecast lines**).</span></span>

## <a name="resolution"></a><span data-ttu-id="49286-108">Lösung</span><span class="sxs-lookup"><span data-stu-id="49286-108">Resolution</span></span>

<span data-ttu-id="49286-109">Die Einstellungen auf der Registerkarte **Planungsdimensionen** der Seite **Bedarfsplanungsparameter** beeinflussen die Seite **Bedarfsplanung** nicht.</span><span class="sxs-lookup"><span data-stu-id="49286-109">The settings on the **Forecast dimensions** tab of the **Demand forecasting parameter** page don't affect the **Demand forecast** page.</span></span> <span data-ttu-id="49286-110">Sie steuern die Grundplanung, die generiert und in der angepassten Bedarfsplanung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="49286-110">They control the baseline forecast that is generated and shown in the adjusted demand forecast.</span></span> <span data-ttu-id="49286-111">Sie steuern jedoch nicht die Dimensionen, die für die „echte“ Bedarfsplanung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="49286-111">However, they don't control the dimensions that are required for the "real" demand forecast.</span></span> <span data-ttu-id="49286-112">Durch die Autorisierung der Datensätze, die auf der Seite **Angepasste Bedarfsplanung** angezeigt werden, können Sie sie in „echte“ Planungseinträge für ein Planungsmodell konvertieren.</span><span class="sxs-lookup"><span data-stu-id="49286-112">By authorizing the records that are shown on the **Adjusted demand forecast** page, you can convert them to "real" forecast entries for a forecast model.</span></span> <span data-ttu-id="49286-113">Dieses Modell kann dann für die Produktprogrammplanung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="49286-113">That model can then be used for master planning.</span></span>

<span data-ttu-id="49286-114">Auf der Seite **Bedarfsplanung** sind die Dimensionen für die „echte“ Planung, die in den Bedarfsplanungspositionen angezeigt werden, Teil der Bedarfsdimensionen.</span><span class="sxs-lookup"><span data-stu-id="49286-114">On the **Demand forecast** page, the dimensions for the "real" forecast that are shown on the demand forecast lines are part of the inventory dimensions.</span></span> <span data-ttu-id="49286-115">(Dieses Verhalten ähnelt dem Verhalten für Auftragspositionen.) Wenn Ihr System nicht für die Verwendung des **Lagerorts** als obligatorische Bedarfsdimension eingerichtet ist, können Sie die Seite so anpassen, dass die Spalte ausgeblendet wird.</span><span class="sxs-lookup"><span data-stu-id="49286-115">(This behavior resembles the behavior for sales order lines.) If your system isn't set up to use **Warehouse** as a mandatory inventory dimension, you can customize the page to hide the column.</span></span>
