---
title: Wartungsprognose
description: In diesem Thema wird die Wartungsprognose in Asset Management erläutert.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1a416bbb79be3f25998d3c0da8d231d0df808685
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875675"
---
# <a name="maintenance-forecasts"></a><span data-ttu-id="06111-103">Wartungsprognose</span><span class="sxs-lookup"><span data-stu-id="06111-103">Maintenance forecasts</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="06111-104">Wenn Sie einen Arbeitsauftrag erstellen möchten, erstellen Sie Arbeitsauftragseinzelvorgänge mit zugehörigen Anlagen und Wartungsauftragstypen.</span><span class="sxs-lookup"><span data-stu-id="06111-104">When you create a work order, you create work order jobs with related assets and maintenance job types.</span></span> <span data-ttu-id="06111-105">Wenn Sie einen Wartungsauftragstyp auswählen, der Wartungsprognosen enthält, werden die Prognosen automatisch in den Arbeitsauftrag übernommen.</span><span class="sxs-lookup"><span data-stu-id="06111-105">When you select a maintenance job type containing maintenance forecasts, the forecasts are automatically copied to the work order.</span></span>

<span data-ttu-id="06111-106">Sie könnenin einem Arbeitsauftrag Prognosezeile hinzufügen oder löschen.</span><span class="sxs-lookup"><span data-stu-id="06111-106">You may be able to add or delete forecast lines on a work order.</span></span> <span data-ttu-id="06111-107">Das Einrichten eines Lebenszyklusstatus von Arbeitsaufträgen, des zugehörigen Projekttyps und der mit dem Projekttyp verbundenen Stufenregeln bestimmt, ob Sie Prognosepositionen hinzufügen oder bearbeiten können.</span><span class="sxs-lookup"><span data-stu-id="06111-107">The setup of a work order lifecycle state, the related project type, and the stage rules related to the project type determines if you are able to add or edit forecast lines.</span></span> 

1. <span data-ttu-id="06111-108">Klicken Sie auf **Anlagenmanagement** > **Allgemein** > **Arbeitsaufträge** > **Alle Arbeitsaufträge** oder **Aktive Arbeitsaufträge**.</span><span class="sxs-lookup"><span data-stu-id="06111-108">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="06111-109">Wählen Sie den Arbeitsauftrag aus der liste aus und klicken Sie auf **Planung**.</span><span class="sxs-lookup"><span data-stu-id="06111-109">Select the work order in the list, and click **Forecast**.</span></span> <span data-ttu-id="06111-110">In **Arbeitsauftragswartungsprognose** werden Prognosepositionen des Wartungsauftragstyps, der im Arbeitsauftrageinzelvorgang ausgewählt wurde, angezeigt.</span><span class="sxs-lookup"><span data-stu-id="06111-110">In **Work order maintenance forecast**, forecast lines from the maintenance job type selected on the work order job are displayed.</span></span>


## <a name="add-hours-forecast-to-a-work-order"></a><span data-ttu-id="06111-111">Geplante Stunden einem Arbeitsauftrag hinzufügen</span><span class="sxs-lookup"><span data-stu-id="06111-111">Add hours forecast to a work order</span></span>

1. <span data-ttu-id="06111-112">Wählen Sie den Arbeitsauftragseinzelvorgang aus, den Sie einer Prognose hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="06111-112">Select the work order job to which you want to add a forecast.</span></span>

2. <span data-ttu-id="06111-113">Klicken Sie im Inforegister **Stunden** auf **Hinzufügen**, um eine neue Position zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="06111-113">On the **Hours** FastTab, click **Add** to create a new line.</span></span>

3. <span data-ttu-id="06111-114">Wählen Sie im Feld **Kategorie** eine Kategorie aus.</span><span class="sxs-lookup"><span data-stu-id="06111-114">Select a category in the **Category** field.</span></span>

4. <span data-ttu-id="06111-115">Fügen Sie die Anzahl der geplanten Stunden im Feld **Stunden** ein.</span><span class="sxs-lookup"><span data-stu-id="06111-115">Insert number of forecasted hours in the **Hours** field.</span></span>

5. <span data-ttu-id="06111-116">Wählen Sie im Feld **Abrechnungscode** den Belastungstyp aus, der verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="06111-116">In the **Line property** field, select the charge type to be used on the line.</span></span>


## <a name="add-items-forecast-to-a-work-order"></a><span data-ttu-id="06111-117">Artikelprognosen einem Arbeitsauftrag hinzufügen</span><span class="sxs-lookup"><span data-stu-id="06111-117">Add items forecast to a work order</span></span>

<span data-ttu-id="06111-118">Es gibt drei Möglichkeiten, Artikel zu einer Arbeitsauftrags-Wartungsprognose hinzuzufügen: Sie können Positionen für Artikel (Ersatzteile) anlegen, die nicht in der Ersatzteilliste oder Anlagenstückliste enthalten sind, Ersatzteile aus der Liste der genehmigten Ersatzteile auswählen und Artikel aus der Anlagenstückliste auswählen.</span><span class="sxs-lookup"><span data-stu-id="06111-118">There are three ways to add items to a work order maintenance forecast: You can create lines for items (spare parts) that are not included in the spare parts list or asset BOM, you can select spare parts from the approved spare parts list, and you can select items from the asset BOM.</span></span>

1. <span data-ttu-id="06111-119">Wählen Sie den Arbeitsauftragseinzelvorgang aus, den Sie einer Prognose hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="06111-119">Select the work order job to which you want to add a forecast.</span></span>

2. <span data-ttu-id="06111-120">Wählen Sie im Inforegister **Artikel** aus.</span><span class="sxs-lookup"><span data-stu-id="06111-120">Select the **Items** FastTab.</span></span>

3. <span data-ttu-id="06111-121">Klicken Sie auf **Hinzufügen**, um eine neue Position für das Ersatzteil zu erstellen, das nicht auf der Ersatzteilliste oder Anlagenstückliste ist.</span><span class="sxs-lookup"><span data-stu-id="06111-121">Click **Add** to create a new line for a spare part that is not on the spare parts list or the asset BOM list.</span></span>

4. <span data-ttu-id="06111-122">Wählen Sie im Feld **Artikelnummer** einen Artikel aus.</span><span class="sxs-lookup"><span data-stu-id="06111-122">Select the item in the **Item number** field.</span></span>

5. <span data-ttu-id="06111-123">Fügen Sie die Menge in das Feld **Verkaufsmenge** ein und wählen Sie eine Mengeneinheit im Feld **Einheit**.</span><span class="sxs-lookup"><span data-stu-id="06111-123">Insert quantity in the **Sales quantity** field, and select a quantity unit in the **Unit** field.</span></span>

6. <span data-ttu-id="06111-124">Geben Sie in die entsprechenden Felder den Einstandspreis und die Währung ein und wählen Sie einen **Abrechnungscode** aus.</span><span class="sxs-lookup"><span data-stu-id="06111-124">Insert cost price and currency in the relevant fields, and select a **Line property**.</span></span>

7. <span data-ttu-id="06111-125">Wenn Sie die in den Artikelpositionen angezeigte Liste mit den Dimensionen ändern möchten, klicken Sie auf **Inventar** > **Dimensionen anzeigen**, wählen Sie die Dimensionen aus und wählen Sie „Ja“ über die Umschalttaste **Einstellungen speichern**.</span><span class="sxs-lookup"><span data-stu-id="06111-125">If you want to change the list of dimensions displayed on the item lines, click **Inventory** > **Display dimensions**, select the dimensions, and select "Yes" on the **Save setup** toggle button.</span></span>

8. <span data-ttu-id="06111-126">Wenn Sie ein genehmigtes Ersatzteil zur Wartungsprognose hinzufügen möchten, klicken Sie auf **Ersatzteile hinzufügen**, wählen Sie das Ersatzteil aus, bearbeiten Sie ggf. die zugehörigen Informationen und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="06111-126">If you want to add an approved spare part to the maintenance forecast, click **Add spare parts**, select the spare part, edit related information if required, and click **OK**.</span></span>

9. <span data-ttu-id="06111-127">Wenn Sie Anlagenstücklistenartikel zur Prognose hinzufügen möchten, klicken Sie auf **Stücklistenartikel hinzufügen**, wählen Sie den Artikel aus, bearbeiten Sie ggf. zugehörige Informationen und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="06111-127">If you want to add asset BOM items to the forecast, click **Add BOM items**, select the item, edit related information if required, and click **OK**.</span></span>

10. <span data-ttu-id="06111-128">Klicken Sie auf **Artikelverwendungsort**, wenn Sie einen Überblick darüber erhalten möchten, wo der Artikel auf der ausgewählten Position im Asset Management in Bezug auf Anlagen, Standardwerte für Wartungsaufträge, Ersatzteile und Arbeitsaufträge verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="06111-128">Click **Item where used** if you want to get an overview of where the item on the selected line is used in Asset Management in relation to assets, maintenance job type defaults, spare parts, and work orders.</span></span> 



## <a name="add-expense-forecast-to-a-work-order"></a><span data-ttu-id="06111-129">Ausgabenprognosen einem Arbeitsauftrag hinzufügen</span><span class="sxs-lookup"><span data-stu-id="06111-129">Add expense forecast to a work order</span></span>

1. <span data-ttu-id="06111-130">In diesem Thema wird erläutert, wie eine Ausgabenprognose einem Arbeitsauftrag hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="06111-130">This topic explains how to add an expense forecast to a work order.</span></span> <span data-ttu-id="06111-131">Wählen Sie im linken Teil des Formulars den Arbeitsauftragseinzelvorgang aus, den Sie einer Prognose hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="06111-131">In the left-hand side of the form, select the work order job to which you want to add a forecast.</span></span>

2. <span data-ttu-id="06111-132">Wählen Sie im Inforegister **Ausgaben** aus.</span><span class="sxs-lookup"><span data-stu-id="06111-132">Select the **Expense** FastTab.</span></span>

3. <span data-ttu-id="06111-133">Klicken Sie zum Erstellen einer neuen Position auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="06111-133">Click **Add** to create a new line.</span></span>

4. <span data-ttu-id="06111-134">Wählen Sie im Feld **Kategorie** eine Kategorie aus.</span><span class="sxs-lookup"><span data-stu-id="06111-134">Select a category in the **Category** field.</span></span>

5. <span data-ttu-id="06111-135">Geben Sie im Feld **Menge** die Menge ein.</span><span class="sxs-lookup"><span data-stu-id="06111-135">Insert quantity in the **Quantity** field.</span></span>

6. <span data-ttu-id="06111-136">Fügen Sie Einstandspreis, Verkaufswährung und Verkaufspreis in die entsprechenden Felder ein.</span><span class="sxs-lookup"><span data-stu-id="06111-136">Insert cost price, sales currency, and sales price in the relevant fields.</span></span>

7. <span data-ttu-id="06111-137">Wählen Sie im Feld **Abrechnungscode** den Belastungstyp aus, der verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="06111-137">In the **Line property** field, select the charge type to be used on the line.</span></span>

>[!NOTE]
><span data-ttu-id="06111-138">Auf dem Inforegister **Wartungsprognose – Summen** sehen Sie eine Übersicht über die Anzahl der auf jeder Registerkarte angelegten Positionen, für den ausgewählten Arbeitsauftragseinzelvorgang und für den Arbeitsauftrag.</span><span class="sxs-lookup"><span data-stu-id="06111-138">On the **Maintenance forecast totals** FastTab, you can see an overview of the number of lines created on each tab, for the selected work order job and for the work order.</span></span> <span data-ttu-id="06111-139">Außerdem sehen Sie eine Summe der prognostizierten Arbeitsstunden für den Arbeitsauftragseinzelvorgang und für den Arbeitsauftrag.</span><span class="sxs-lookup"><span data-stu-id="06111-139">Also, you can see a sum of forecasted work hours for the work order job and for the work order.</span></span>

![Abbildung 1](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a><span data-ttu-id="06111-141">utomatische Aktualisierung von Arbeitsauftragsprognosen</span><span class="sxs-lookup"><span data-stu-id="06111-141">Automatic update of work order forecasts</span></span>

<span data-ttu-id="06111-142">Im Asset Management können Sie Änderungen an den Arbeitsauftragsprognosen für Stundenkosten, Artikelkosten und Ausgaben, die in anderen Modulen in Dynamics 365 for Finance and Operations aktualisiert wurden, automatisch aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="06111-142">In Asset Management, you can automatically update any changes in work order forecasts regarding hour costs, item costs, and expenses, which have been updated in other modules in Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="06111-143">Auf diese Weise wird sichergestellt, dass in Ihren Arbeitsauftragsprognosen immer die aktuellen Einstandspreise verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="06111-143">This is done to ensure that the latest cost prices are always used in your work order forecasts.</span></span> <span data-ttu-id="06111-144">Es ist auch möglich, ähnliche Aktualisierungen für [Wartungsauftragstypprognosen](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md) vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="06111-144">It is also possible to make similar updates for [maintenance job type forecasts](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span></span>

1. <span data-ttu-id="06111-145">Klicken Sie auf **Anlagenverwaltungsparameter** > **Periodisch** > **Planung** > **Arbeitsauftragsplanung aktualisieren**.</span><span class="sxs-lookup"><span data-stu-id="06111-145">Click **Asset management** > **Periodic** > **Forecast** > **Update work order forecast**.</span></span>

2. <span data-ttu-id="06111-146">Im Dropdown-Dialogfeld **Arbeitsauftragsplanung aktualisieren** können Sie bei Bedarf Auswahlmöglichkeiten für bestimmte Arbeitsaufträge oder Arbeitsauftragseinzelvorgänge hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="06111-146">In the **Update work order forecast** drop-down dialog, you can add selections regarding specific work orders or work order jobs, if required.</span></span> <span data-ttu-id="06111-147">Klicken Sie auf **Filtern**, um diese Auswahl treffen.</span><span class="sxs-lookup"><span data-stu-id="06111-147">Click **Filter** to make those selections.</span></span>

3. <span data-ttu-id="06111-148">Bei Bedarf können Sie die automatische Aktualisierung als Batchauftrag auf dem Inforegister **Im Hintergrund ausführen** einrichten.</span><span class="sxs-lookup"><span data-stu-id="06111-148">If required, you can set up the automatic update as a batch job on the **Run in the background** FastTab.</span></span>

4. <span data-ttu-id="06111-149">Klicken Sie auf **OK**, um die Aktualisierung der Prognose zu starten.</span><span class="sxs-lookup"><span data-stu-id="06111-149">Click **OK** to start the forecast update.</span></span>


![Abbildung 2](media/07-work-orders.png)

