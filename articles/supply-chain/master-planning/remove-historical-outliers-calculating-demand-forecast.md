---
title: Entfernen Sie Ausreißer aus den historischen Buchungsdaten, wenn Sie eine Bedarfsplanung berechnen.
description: In diesem Artikel wird beschrieben, wie Ausreißer aus den historischen Daten ausgeschlossen werden, die verwendet werden, um eine Bedarfsplanung zu berechnen. Wenn Sie Ausreißer ausschließen, können Sie die Prognosegenauigkeit verbessern.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanForecastParameters, ReqDemPlanOutlierQuerySetup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 72621
ms.assetid: 88a964af-14eb-4c5c-945b-388e5908362c
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f8593b0f55e899a32f2407fcb668d8bcb0ff8431
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213445"
---
# <a name="remove-outliers-from-historical-transaction-data-when-calculating-a-demand-forecast"></a><span data-ttu-id="8c6c5-104">Entfernen Sie Ausreißer aus den historischen Buchungsdaten, wenn Sie eine Bedarfsplanung berechnen.</span><span class="sxs-lookup"><span data-stu-id="8c6c5-104">Remove outliers from historical transaction data when calculating a demand forecast</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8c6c5-105">In diesem Artikel wird beschrieben, wie Ausreißer aus den historischen Daten ausgeschlossen werden, die verwendet werden, um eine Bedarfsplanung zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="8c6c5-105">This article describes how to exclude outliers from the historical data that is used to calculate a demand forecast.</span></span> <span data-ttu-id="8c6c5-106">Wenn Sie Ausreißer ausschließen, können Sie die Prognosegenauigkeit verbessern.</span><span class="sxs-lookup"><span data-stu-id="8c6c5-106">By excluding outliers, you can improve forecast accuracy.</span></span>

<span data-ttu-id="8c6c5-107">Wenn Sie Ausreißer ausschließen, können Sie die Prognosegenauigkeit verbessern.</span><span class="sxs-lookup"><span data-stu-id="8c6c5-107">You can exclude outliers to improve forecast accuracy.</span></span> <span data-ttu-id="8c6c5-108">Diese Aufgabe ist optional.</span><span class="sxs-lookup"><span data-stu-id="8c6c5-108">This is an optional task.</span></span> <span data-ttu-id="8c6c5-109">Hier ein Überblick über den Prozess:</span><span class="sxs-lookup"><span data-stu-id="8c6c5-109">Here is an overview of the process:</span></span>

1.  <span data-ttu-id="8c6c5-110">Klicken Sie auf **Produktprogrammplanung** &gt; **Einstellungen** &gt; **Bedarfsplanung** &gt; **Ausreißer entfernen**, um die Seite **Ausreißer entfernen** zu öffnen, in der Sie eine Abfrage verwenden können, um die Buchungen auswählen, die Sie ausschließen wollen.</span><span class="sxs-lookup"><span data-stu-id="8c6c5-110">Click **Master planning** &gt; **Setup** &gt; **Demand forecasting** &gt; **Outlier removal** to open the **Outlier removal** page, where you can use a query to select the transactions to exclude.</span></span>
2.  <span data-ttu-id="8c6c5-111">Wählen Sie das Unternehmen, für das die Abfrage gilt, und geben Sie dann einen Namen und eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="8c6c5-111">Select the company that the query applies to, and then enter a name and description.</span></span> <span data-ttu-id="8c6c5-112">Das **Abfragendatum** Feld wird automatisch auf das aktuelle Datum festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8c6c5-112">The **Query date** field is automatically set to the current date.</span></span>
3.  <span data-ttu-id="8c6c5-113">Aktivieren Sie das Kontrollkästchen **Aktiv**, um die Transaktionen, die von der Abfrage gefunden wurden, von den historischen Daten auszuschließen.</span><span class="sxs-lookup"><span data-stu-id="8c6c5-113">Select the **Active** check box to exclude the transactions that the query finds from the historical data.</span></span> <span data-ttu-id="8c6c5-114">Diese Einstellung tritt in Kraft, wenn Sie eine Basisprognose erstellen.</span><span class="sxs-lookup"><span data-stu-id="8c6c5-114">This setting will take effect when you create a baseline forecast.</span></span>
4.  <span data-ttu-id="8c6c5-115">Auf der Seite **Abfrage für Ausreißerentfernung** können Sie die Kriterien hinzufügen, entfernen und auswählen, welche festlegen, welche Transaktionen ausgeschlossen werden, wenn die Basisprognose berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="8c6c5-115">On the **Outlier removal query** page, you can add, remove, and select the criteria that define which transactions will be excluded when the baseline forecast is calculated.</span></span> <span data-ttu-id="8c6c5-116">Beispielsweise wählen Sie einen bestimmten Artikel oder eine Auftragsbuchung aus, den bzw. die Sie ausschließen möchten.</span><span class="sxs-lookup"><span data-stu-id="8c6c5-116">For example, select a specific item or order transaction to exclude.</span></span>
5.  <span data-ttu-id="8c6c5-117">Klicken Sie auf **Transaktionen anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="8c6c5-117">Click **Display transactions**.</span></span> <span data-ttu-id="8c6c5-118">Die Seite **Ausreißerbuchungen** enthält die Transaktionen, die den Kriterien entsprechen, die Sie in der Abfrage definiert haben und die aus den historischen Daten ausgeschlossen werden, wenn die Bedarfsplanung berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="8c6c5-118">The **Outlier transactions** page lists the transactions that meet the criteria that you defined in the query, and that will be excluded from the historical data when the demand forecast is calculated.</span></span>

<span data-ttu-id="8c6c5-119">**Hinweis:** Sie können eine Abfrage auch erstellen, die auf einer vorhandenen Abfrage basiert.</span><span class="sxs-lookup"><span data-stu-id="8c6c5-119">**Note:** You can also create a query that is based on an existing query.</span></span> <span data-ttu-id="8c6c5-120">Wählen Sie die Abfrage aus, die kopiert werden soll, und klicken Sie dann auf **Duplizieren**.</span><span class="sxs-lookup"><span data-stu-id="8c6c5-120">Select the query to copy, and then click **Duplicate**.</span></span> <span data-ttu-id="8c6c5-121">Das Feld **Abfragedatum** kennzeichnet die Version.</span><span class="sxs-lookup"><span data-stu-id="8c6c5-121">The **Query date** field identifies the version.</span></span> <span data-ttu-id="8c6c5-122">Sie können die Abfrage verwenden, belassen, oder Sie können auf **Abfrage bearbeiten** klicken, um die Kriterien zu ändern.</span><span class="sxs-lookup"><span data-stu-id="8c6c5-122">You can use the query as it is, or you can click **Edit query** to modify the criteria.</span></span> <span data-ttu-id="8c6c5-123">Sie können den Namen und die Beschreibung der neuen Abfrage optional ändern.</span><span class="sxs-lookup"><span data-stu-id="8c6c5-123">You can optionally modify the name and description of the new query.</span></span>

<a name="additional-resources"></a><span data-ttu-id="8c6c5-124">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8c6c5-124">Additional resources</span></span>
--------

[<span data-ttu-id="8c6c5-125">Bedarfsplanung – Übersicht</span><span class="sxs-lookup"><span data-stu-id="8c6c5-125">Demand forecasting overview</span></span>](introduction-demand-forecasting.md)

[<span data-ttu-id="8c6c5-126">Planungsgenauigkeit überwachen</span><span class="sxs-lookup"><span data-stu-id="8c6c5-126">Monitor forecast accuracy</span></span>](monitor-forecast-accuracy.md)



