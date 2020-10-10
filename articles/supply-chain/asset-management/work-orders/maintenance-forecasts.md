---
title: Wartungsprognose
description: In diesem Thema wird die Wartungsprognose in Asset Management erläutert.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderForecastToJournals, EntAssetWorkOrderForecast
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6428981fcf560c541634d9466695be7bce4cb453
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/25/2020
ms.locfileid: "3888952"
---
# <a name="maintenance-forecasts"></a><span data-ttu-id="cf284-103">Wartungsprognose</span><span class="sxs-lookup"><span data-stu-id="cf284-103">Maintenance forecasts</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="cf284-104">Wenn Sie einen Arbeitsauftrag erstellen, erstellen Sie Arbeitsauftragseinzelvorgänge mit zugehörigen Anlagen und Wartungsauftragstypen.</span><span class="sxs-lookup"><span data-stu-id="cf284-104">When you create a work order, you create work order jobs that have related assets and maintenance job types.</span></span> <span data-ttu-id="cf284-105">Wenn Sie einen Wartungsauftragstyp auswählen, der Wartungsprognosen enthält, werden die Prognosen automatisch in den Arbeitsauftrag übernommen.</span><span class="sxs-lookup"><span data-stu-id="cf284-105">When you select a maintenance job type that contains maintenance forecasts, the forecasts are automatically copied to the work order.</span></span>

<span data-ttu-id="cf284-106">Sie könnten Planungspositionen zu einem Arbeitsauftrag hinzufügen oder aus diesem löschen.</span><span class="sxs-lookup"><span data-stu-id="cf284-106">You might be able to add forecast lines to a work order or delete them from a work order.</span></span> <span data-ttu-id="cf284-107">Die Einrichtung des Arbeitsauftrags-Lebenszykluszustands, der zugehörige Projekttyp und die mit dem Projekttyp verbundenen Stufenregeln bestimmen, ob Sie Planungspositionen hinzufügen oder bearbeiten können.</span><span class="sxs-lookup"><span data-stu-id="cf284-107">The setup of the work order lifecycle state, the related project type, and the stage rules that are related to the project type determine whether you can add or edit forecast lines.</span></span> <span data-ttu-id="cf284-108">Weitere Informationen über Lebenszyklusstatus von Arbeitsaufträgen und zugehörigen Projektphasen finden Sie unter [Planungen, Arbeitsaufträge und Projekte](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span><span class="sxs-lookup"><span data-stu-id="cf284-108">For more information about work order lifecycle states and related project stages, see [Forecasts, work orders, and projects](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span></span>

1. <span data-ttu-id="cf284-109">Wählen Sie **Anlagenverwaltung** > **Allgemein** > **Arbeitsaufträge** > **Alle Arbeitsaufträge** oder **Aktive Arbeitsaufträge** aus.</span><span class="sxs-lookup"><span data-stu-id="cf284-109">Select **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="cf284-110">Wählen Sie den Arbeitsauftrag in der Liste aus, und wählen Sie dann im Aktivitätsbereich > auf der Registerkarte **Arbeitsauftrag** > in der Gruppe **Projekt** **Planung** aus.</span><span class="sxs-lookup"><span data-stu-id="cf284-110">Select the work order in the list, and then, on the Action Pane > **Work order** tab > the **Project** group, select **Forecast**.</span></span> <span data-ttu-id="cf284-111">Auf der Seite **Arbeitsauftragswartungsprognose** werden Planungspositionen des Wartungsauftragstyps, der im Arbeitsauftragseinzelvorgang ausgewählt wurde, angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cf284-111">The **Work order maintenance forecast** page shows forecast lines from the maintenance job type that is selected on the work order job.</span></span>


## <a name="add-an-hours-forecast-to-a-work-order"></a><span data-ttu-id="cf284-112">Geplante Stunden einem Arbeitsauftrag hinzufügen</span><span class="sxs-lookup"><span data-stu-id="cf284-112">Add an hours forecast to a work order</span></span>

1. <span data-ttu-id="cf284-113">Wählen Sie auf der Seite **Arbeitsauftrag – Wartungsprognose** einen Arbeitsauftragseinzelvorgang zum Hinzufügen einer Planung aus.</span><span class="sxs-lookup"><span data-stu-id="cf284-113">On the **Work order maintenance forecast** page, select the work order job to add a forecast to.</span></span>

2. <span data-ttu-id="cf284-114">Wählen Sie im Inforegister **Stunden** **Hinzufügen** aus, um eine neue Position zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="cf284-114">On the **Hours** FastTab, select **Add** to create a new line.</span></span>

3. <span data-ttu-id="cf284-115">Wählen Sie im Feld **Kategorie** eine Kategorie aus.</span><span class="sxs-lookup"><span data-stu-id="cf284-115">In the **Category** field, select a category.</span></span>

4. <span data-ttu-id="cf284-116">Geben Sie die Anzahl der geplanten Stunden im Feld **Stunden** ein.</span><span class="sxs-lookup"><span data-stu-id="cf284-116">In the **Hours** field, enter the number of forecasted hours.</span></span>

5. <span data-ttu-id="cf284-117">Wählen Sie im Feld **Abrechnungscode** den Belastungstyp aus, der verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cf284-117">In the **Line property** field, select the type of charge that should be used on the line.</span></span>


## <a name="add-an-items-forecast-to-a-work-order"></a><span data-ttu-id="cf284-118">Artikelprognosen einem Arbeitsauftrag hinzufügen</span><span class="sxs-lookup"><span data-stu-id="cf284-118">Add an items forecast to a work order</span></span>

<span data-ttu-id="cf284-119">Es gibt drei Möglichkeiten, einer Arbeitsauftragswartungsprognose Artikel hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="cf284-119">There are three ways to add items to a work order maintenance forecast.</span></span> <span data-ttu-id="cf284-120">Sie können Positionen für Artikel (Ersatzteile) anlegen, die nicht in der Ersatzteilliste oder Anlagenstückliste enthalten sind, Ersatzteile aus der Liste der genehmigten Ersatzteile auswählen und Artikel aus der Anlagenstückliste auswählen.</span><span class="sxs-lookup"><span data-stu-id="cf284-120">You can create lines for items (spare parts) that aren't included on the spare parts list or the asset bill of materials (BOM), you can select spare parts from the approved spare parts list, or you can select items from the asset BOM.</span></span>

- <span data-ttu-id="cf284-121">Wählen Sie auf der Seite **Arbeitsauftrag – Wartungsprognose** einen Arbeitsauftragseinzelvorgang zum Hinzufügen einer Planung aus.</span><span class="sxs-lookup"><span data-stu-id="cf284-121">On the **Work order maintenance forecast** page, select the work order job to to add a forecast to.</span></span>

- <span data-ttu-id="cf284-122">Fügen Sie auf dem Inforegister **Artikel** Artikel zur Wartungsprognose hinzu, indem Sie die geeignete Methode anwenden.</span><span class="sxs-lookup"><span data-stu-id="cf284-122">On the **Items** FastTab, add items to the maintenance forecast by using the appropriate method.</span></span>

<span data-ttu-id="cf284-123">Befolgen Sie die folgenden Schritte, um eine Position für ein Ersatzteil zu erstellen, das nicht auf der Ersatzteilliste oder Anlagenstückliste ist.</span><span class="sxs-lookup"><span data-stu-id="cf284-123">To create a line for a spare part that isn't on the spare parts list or the asset BOM, follow these steps:</span></span>

1. <span data-ttu-id="cf284-124">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="cf284-124">Select **Add**.</span></span>
2. <span data-ttu-id="cf284-125">Wählen Sie im Feld **Artikelnummer** den Artikel aus.</span><span class="sxs-lookup"><span data-stu-id="cf284-125">In the **Item number** field, select the item.</span></span>
3. <span data-ttu-id="cf284-126">Geben Sie im Feld **Verkaufsmenge** die Menge ein.</span><span class="sxs-lookup"><span data-stu-id="cf284-126">In the **Sales quantity** field, enter the quantity.</span></span>
4. <span data-ttu-id="cf284-127">Wählen Sie im Feld **Einheit** die Maßeinheit für die Menge aus.</span><span class="sxs-lookup"><span data-stu-id="cf284-127">In the **Unit** field, select the unit of measure for the quantity.</span></span>
5. <span data-ttu-id="cf284-128">Geben Sie in den Feldern **Einstandspreis** und **Währung** entsprechende Werte ein.</span><span class="sxs-lookup"><span data-stu-id="cf284-128">In the **Cost price** and **Currency** fields, enter appropriate values.</span></span>
6. <span data-ttu-id="cf284-129">Wählen Sie im Feld **Abrechnungscode** einen Abrechnungscode aus.</span><span class="sxs-lookup"><span data-stu-id="cf284-129">In the **Line property** field, select a line property.</span></span>
7. <span data-ttu-id="cf284-130">Um die in den Artikelpositionen angezeigte Liste mit den Dimensionen zu ändern, wählen Sie **Inventar** > **Dimensionen anzeigen** aus, wählen Sie die Dimensionen aus und legen Sie dann die Option **Einstellungen speichern** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="cf284-130">To change the list of dimensions that is shown on the item lines, select **Inventory** > **Display dimensions**, select the dimensions, and then set the **Save setup** option to **Yes**.</span></span>

<span data-ttu-id="cf284-131">Um ein Ersatzteil aus einer genehmigten Ersatzteilliste hinzuzufügen, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="cf284-131">To add a spare part from an approved spare parts list, follow these steps:</span></span>

1. <span data-ttu-id="cf284-132">Wählen Sie **Ersatzteile hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="cf284-132">Select **Add spare parts**.</span></span>
2. <span data-ttu-id="cf284-133">Wählen Sie das Ersatzteil aus, und bearbeiten Sie die zugehörigen Informationen nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="cf284-133">Select the spare part, and edit the related information as you require.</span></span>
3. <span data-ttu-id="cf284-134">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="cf284-134">Select **OK**.</span></span>

<span data-ttu-id="cf284-135">Wenn Sie einen Artikel von der Anlagenstückliste hinzufügen möchten, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="cf284-135">To add an item from the asset BOM, follow these steps:</span></span>

1. <span data-ttu-id="cf284-136">Wählen Sie **Stücklistenartikel hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="cf284-136">Select **Add BOM items**.</span></span>
2. <span data-ttu-id="cf284-137">Wählen Sie den Artikel aus, und bearbeiten Sie die zugehörigen Informationen nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="cf284-137">Select the item, and edit the related information as you require.</span></span>
3. <span data-ttu-id="cf284-138">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="cf284-138">Select **OK**.</span></span>

<span data-ttu-id="cf284-139">Um einen Überblick darüber zu erhalten, wo der Artikel in der ausgewählten Position verwendet wird in Bezug auf Anlagen, Standardwerte für Wartungsauftragstypen, Ersatzteile und Arbeitsaufträge in Anlagenmanagement, wählen Sie die Option **Artikelverwendungsort** aus.</span><span class="sxs-lookup"><span data-stu-id="cf284-139">To get an overview that shows where the item on the selected line is used in relation to assets, maintenance job type defaults, spare parts, and work orders in Asset Management, select **Item where used**.</span></span> <span data-ttu-id="cf284-140">Weitere Informationen über diesen Überblick finden Sie unter [Artikelverwendungsort](../controlling-and-reporting/item-where-used.md).</span><span class="sxs-lookup"><span data-stu-id="cf284-140">For more information about this overview, see [Item where used](../controlling-and-reporting/item-where-used.md).</span></span>


## <a name="add-an-expense-forecast-to-a-work-order"></a><span data-ttu-id="cf284-141">Ausgabenprognosen einem Arbeitsauftrag hinzufügen</span><span class="sxs-lookup"><span data-stu-id="cf284-141">Add an expense forecast to a work order</span></span>

1. <span data-ttu-id="cf284-142">Wählen Sie auf der Seite **Arbeitsauftrag – Wartungsprognose** einen Arbeitsauftragseinzelvorgang zum Hinzufügen einer Planung aus.</span><span class="sxs-lookup"><span data-stu-id="cf284-142">On the **Work order maintenance forecast** page, select the work order job to add a forecast to.</span></span>

2. <span data-ttu-id="cf284-143">Wählen Sie im Inforegister **Ausgaben** **Hinzufügen** aus, um eine Position zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="cf284-143">On the **Expense** FastTab, select **Add** to create a line.</span></span>

3. <span data-ttu-id="cf284-144">Wählen Sie im Feld **Kategorie** eine Kategorie aus.</span><span class="sxs-lookup"><span data-stu-id="cf284-144">In the **Category** field, select a category.</span></span>

4. <span data-ttu-id="cf284-145">Geben Sie im Feld **Menge** die Menge ein.</span><span class="sxs-lookup"><span data-stu-id="cf284-145">In the **Quantity** field, enter the quantity.</span></span>

5. <span data-ttu-id="cf284-146">Geben Sie in den Feldern **Einstandspreis**, **Verkaufswährung** und **Verkaufspreis** entsprechende Werte ein.</span><span class="sxs-lookup"><span data-stu-id="cf284-146">In the **Cost price**, **Sales currency**, and **Sales price** fields, enter appropriate values.</span></span>

6. <span data-ttu-id="cf284-147">Wählen Sie im Feld **Abrechnungscode** den Belastungstyp aus, der verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cf284-147">In the **Line property** field, select the type of charge that should be used on the line.</span></span>

>[!NOTE]
><span data-ttu-id="cf284-148">Auf dem Inforegister **Wartungsprognose – Summen** sehen Sie eine Übersicht über die Anzahl der auf jedem Inforegister angelegten Positionen, für den ausgewählten Arbeitsauftragseinzelvorgang und für den Arbeitsauftrag.</span><span class="sxs-lookup"><span data-stu-id="cf284-148">The **Maintenance forecast totals** FastTab shows an overview of the number of lines that have been created, for the selected work order job and for the work order, on each FastTab.</span></span> <span data-ttu-id="cf284-149">Außerdem sehen Sie eine Summe der prognostizierten Arbeitsstunden für den Arbeitsauftragseinzelvorgang und für den Arbeitsauftrag.</span><span class="sxs-lookup"><span data-stu-id="cf284-149">It also shows the total forecasted work hours for the work order job and the work order.</span></span>

<span data-ttu-id="cf284-150">Die folgende Abbildung zeigt ein Beispiel für die Seite **Arbeitsauftrag – Wartungsprognose**.</span><span class="sxs-lookup"><span data-stu-id="cf284-150">The illustration below shows an example of the **Work order maintenance forecast** page.</span></span>

![Abbildung 1](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a><span data-ttu-id="cf284-152">utomatische Aktualisierung von Arbeitsauftragsprognosen</span><span class="sxs-lookup"><span data-stu-id="cf284-152">Automatic update of work order forecasts</span></span>

<span data-ttu-id="cf284-153">Im Anlagenmanagement können Sie Änderungen an den Arbeitsauftragsprognosen für Stundenkosten, Artikelkosten und Ausgaben, die in anderen Modulen in Microsoft Dynamics 365 for Finance and Operations aktualisiert wurden, automatisch aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="cf284-153">If hour costs, item costs, and expenses are updated in other modules in Microsoft Dynamics 365 for Finance and Operations, work order forecasts in Asset Management can automatically be updated to reflect those changes.</span></span> <span data-ttu-id="cf284-154">Auf diese Weise wird sichergestellt, dass in Ihren Arbeitsauftragsprognosen immer die aktuellen Einstandspreise verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cf284-154">This capability helps guarantee that the latest cost prices are always used in your work order forecasts.</span></span> <span data-ttu-id="cf284-155">Es ist auch möglich, ähnliche Aktualisierungen für [Wartungsauftragstypprognosen](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md) vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="cf284-155">You can also do similar updates for [maintenance job type forecasts](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span></span>

1. <span data-ttu-id="cf284-156">Wählen Sie **Anlagenverwaltung** > **Periodisch** > **Planung** > **Arbeitsauftragsplanung aktualisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="cf284-156">Select **Asset management** > **Periodic** > **Forecast** > **Update work order forecast**.</span></span>

2. <span data-ttu-id="cf284-157">Im Dialogfeld **Arbeitsauftragsplanung aktualisieren** auf dem Inforegister **Einzuschließende Datensätze** können Sie bei Bedarf Auswahlmöglichkeiten für bestimmte Arbeitsaufträge oder Arbeitsauftragseinzelvorgänge hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="cf284-157">In the **Update work order forecast** dialog, on the **Records to include** FastTab, you can add selections regarding specific work orders or work order jobs, as you require.</span></span> <span data-ttu-id="cf284-158">Klicken Sie auf **Filtern** und treffen Sie die zutreffende Auswahl.</span><span class="sxs-lookup"><span data-stu-id="cf284-158">Click **Filter** to make the relevant selections.</span></span>

3. <span data-ttu-id="cf284-159">Im Inforegister **Im Hintergrund ausführen** können Sie die automatische Aktualisierung bei Bedarf als Batchauftrag einrichten.</span><span class="sxs-lookup"><span data-stu-id="cf284-159">On the **Run in the background** FastTab, you can set up the automatic update as a batch job, as you require.</span></span>

4. <span data-ttu-id="cf284-160">Klicken Sie auf **OK**, um die Aktualisierung der Prognose zu starten.</span><span class="sxs-lookup"><span data-stu-id="cf284-160">Select **OK** to start the forecast update.</span></span>


<span data-ttu-id="cf284-161">Die folgende Abbildung zeigt ein Beispiel für das Dialogfeld **Arbeitsauftragsplanung aktualisieren**.</span><span class="sxs-lookup"><span data-stu-id="cf284-161">The illustration below shows an example of the **Update work order forecast** dialog.</span></span>

![Abbildung 2](media/07-work-orders.png)
