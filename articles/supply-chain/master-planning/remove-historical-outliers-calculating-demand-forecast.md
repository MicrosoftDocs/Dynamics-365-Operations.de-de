---
title: "Entfernen Sie Ausreißer aus den historischen Buchungsdaten, wenn Sie eine Bedarfsplanung berechnen."
description: "In diesem Artikel wird beschrieben, wie Ausreißer aus den historischen Daten ausgeschlossen werden, die verwendet werden, um eine Bedarfsplanung zu berechnen. Wenn Sie Ausreißer ausschließen, können Sie die Prognosegenauigkeit verbessern."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanForecastParameters, ReqDemPlanOutlierQuerySetup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 72621
ms.assetid: 88a964af-14eb-4c5c-945b-388e5908362c
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 714a892ff4c168ee3ba1cefd25ae18345af5631b
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="remove-outliers-from-historical-transaction-data-when-calculating-a-demand-forecast"></a><span data-ttu-id="fabf8-104">Entfernen Sie Ausreißer aus den historischen Buchungsdaten, wenn Sie eine Bedarfsplanung berechnen.</span><span class="sxs-lookup"><span data-stu-id="fabf8-104">Remove outliers from historical transaction data when calculating a demand forecast</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="fabf8-105">In diesem Artikel wird beschrieben, wie Ausreißer aus den historischen Daten ausgeschlossen werden, die verwendet werden, um eine Bedarfsplanung zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="fabf8-105">This article describes how to exclude outliers from the historical data that is used to calculate a demand forecast.</span></span> <span data-ttu-id="fabf8-106">Wenn Sie Ausreißer ausschließen, können Sie die Prognosegenauigkeit verbessern.</span><span class="sxs-lookup"><span data-stu-id="fabf8-106">By excluding outliers, you can improve forecast accuracy.</span></span>

<span data-ttu-id="fabf8-107">Wenn Sie Ausreißer ausschließen, können Sie die Prognosegenauigkeit verbessern.</span><span class="sxs-lookup"><span data-stu-id="fabf8-107">You can exclude outliers to improve forecast accuracy.</span></span> <span data-ttu-id="fabf8-108">Diese Aufgabe ist optional.</span><span class="sxs-lookup"><span data-stu-id="fabf8-108">This is an optional task.</span></span> <span data-ttu-id="fabf8-109">Hier ein Überblick über den Prozess:</span><span class="sxs-lookup"><span data-stu-id="fabf8-109">Here is an overview of the process:</span></span>

1.  <span data-ttu-id="fabf8-110">Klicken Sie auf **Produktprogrammplanung** &gt; **Einstellungen** &gt; **Bedarfsplanung** &gt; **Ausreißer entfernen**, um die Seite **Ausreißer entfernen** zu öffnen, in der Sie eine Abfrage verwenden können, um die Buchungen auswählen, die Sie ausschließen wollen.</span><span class="sxs-lookup"><span data-stu-id="fabf8-110">Click **Master planning** &gt; **Setup** &gt; **Demand forecasting** &gt; **Outlier removal** to open the **Outlier removal** page, where you can use a query to select the transactions to exclude.</span></span>
2.  <span data-ttu-id="fabf8-111">Wählen Sie das Unternehmen, für das die Abfrage gilt, und geben Sie dann einen Namen und eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="fabf8-111">Select the company that the query applies to, and then enter a name and description.</span></span> <span data-ttu-id="fabf8-112">Das **Abfragendatum** Feld wird automatisch auf das aktuelle Datum festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fabf8-112">The **Query date** field is automatically set to the current date.</span></span>
3.  <span data-ttu-id="fabf8-113">Aktivieren Sie das Kontrollkästchen **Aktiv**, um die Transaktionen, die von der Abfrage gefunden wurden, von den historischen Daten auszuschließen.</span><span class="sxs-lookup"><span data-stu-id="fabf8-113">Select the **Active** check box to exclude the transactions that the query finds from the historical data.</span></span> <span data-ttu-id="fabf8-114">Diese Einstellung tritt in Kraft, wenn Sie eine Basisprognose erstellen.</span><span class="sxs-lookup"><span data-stu-id="fabf8-114">This setting will take effect when you create a baseline forecast.</span></span>
4.  <span data-ttu-id="fabf8-115">Auf der Seite **Abfrage für Ausreißerentfernung** können Sie die Kriterien hinzufügen, entfernen und auswählen, welche festlegen, welche Transaktionen ausgeschlossen werden, wenn die Basisprognose berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="fabf8-115">On the **Outlier removal query** page, you can add, remove, and select the criteria that define which transactions will be excluded when the baseline forecast is calculated.</span></span> <span data-ttu-id="fabf8-116">Beispielsweise wählen Sie einen bestimmten Artikel oder eine Auftragsbuchung aus, den bzw. die Sie ausschließen möchten.</span><span class="sxs-lookup"><span data-stu-id="fabf8-116">For example, select a specific item or order transaction to exclude.</span></span>
5.  <span data-ttu-id="fabf8-117">Klicken Sie auf **Transaktionen anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="fabf8-117">Click **Display transactions**.</span></span> <span data-ttu-id="fabf8-118">Die Seite **Ausreißerbuchungen** enthält die Transaktionen, die den Kriterien entsprechen, die Sie in der Abfrage definiert haben und die aus den historischen Daten ausgeschlossen werden, wenn die Bedarfsplanung berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="fabf8-118">The **Outlier transactions** page lists the transactions that meet the criteria that you defined in the query, and that will be excluded from the historical data when the demand forecast is calculated.</span></span>

<span data-ttu-id="fabf8-119">**Hinweis:** Sie können eine Abfrage auch erstellen, die auf einer vorhandenen Abfrage basiert.</span><span class="sxs-lookup"><span data-stu-id="fabf8-119">**Note:** You can also create a query that is based on an existing query.</span></span> <span data-ttu-id="fabf8-120">Wählen Sie die Abfrage aus, die kopiert werden soll, und klicken Sie dann auf **Duplizieren**.</span><span class="sxs-lookup"><span data-stu-id="fabf8-120">Select the query to copy, and then click **Duplicate**.</span></span> <span data-ttu-id="fabf8-121">Das Feld **Abfragedatum** kennzeichnet die Version.</span><span class="sxs-lookup"><span data-stu-id="fabf8-121">The **Query date** field identifies the version.</span></span> <span data-ttu-id="fabf8-122">Sie können die Abfrage verwenden, belassen, oder Sie können auf **Abfrage bearbeiten** klicken, um die Kriterien zu ändern.</span><span class="sxs-lookup"><span data-stu-id="fabf8-122">You can use the query as it is, or you can click **Edit query** to modify the criteria.</span></span> <span data-ttu-id="fabf8-123">Sie können den Namen und die Beschreibung der neuen Abfrage optional ändern.</span><span class="sxs-lookup"><span data-stu-id="fabf8-123">You can optionally modify the name and description of the new query.</span></span>

<a name="see-also"></a><span data-ttu-id="fabf8-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fabf8-124">See also</span></span>
--------

[<span data-ttu-id="fabf8-125">Einführung in die Bedarfsplanung</span><span class="sxs-lookup"><span data-stu-id="fabf8-125">Introduction to demand forecasting</span></span>](introduction-demand-forecasting.md)

[<span data-ttu-id="fabf8-126">Überwachen der Planungsgenauigkeit</span><span class="sxs-lookup"><span data-stu-id="fabf8-126">Monitoring forecast accuracy</span></span>](monitor-forecast-accuracy.md)




