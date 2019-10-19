---
title: Wartungsdurchgänge
description: In diesem Thema werden Wartungsdurchgänge im Asset Management erläutert.
author: josaw1
manager: AnnBe
ms.date: 08/27/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: eca732f245650c8e1f3dc976454536a0ab1ee117
ms.sourcegitcommit: 6476f27c8d3dced7c2e9a7344a4e378b51a1983e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2019
ms.locfileid: "1922021"
---
# <a name="maintenance-rounds"></a><span data-ttu-id="4933e-103">Wartungsdurchgänge</span><span class="sxs-lookup"><span data-stu-id="4933e-103">Maintenance rounds</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="4933e-104">In **Asset Management** können Sie für verschiedene Anlagen Wartungsdurchgänge anlegen, bei denen Sie eine ähnliche Aufgabe in regelmäßigen Abständen durchführen müssen.</span><span class="sxs-lookup"><span data-stu-id="4933e-104">In **Asset Management**, you can create maintenance rounds for various assets, on which you need to carry out a similar task at regular intervals.</span></span> <span data-ttu-id="4933e-105">Zum Beispiel Schmierarbeiten oder Sicherheitsprüfungen, die an mehreren Maschinen innerhalb derselben Zeiträume durchgeführt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="4933e-105">For example, lubrication jobs or safety inspection jobs that need to be carried out on a number of machines within the same intervals.</span></span> <span data-ttu-id="4933e-106">Der erste Schritt ist die Erstellung eines Wartungsdurchgangs, der Anlagen einbezieht, die die gleiche Form von Wartungsarbeiten erfordern.</span><span class="sxs-lookup"><span data-stu-id="4933e-106">First step is to create a maintenance round, including assets that require the same form of maintenance job.</span></span> <span data-ttu-id="4933e-107">Als nächstes planen Sie die Wartungsdurchgänge ein.</span><span class="sxs-lookup"><span data-stu-id="4933e-107">Next, you schedule the maintenance rounds.</span></span> <span data-ttu-id="4933e-108">Wenn Sie den Wartungsdurchgangsplan erstellt haben, sehen Sie alle Auftragsdatensätze, die sich auf die Runde beziehen, in **Alle Wartungszeitpläne**- und **Offene Wartungszeitpläne-Positionen**.</span><span class="sxs-lookup"><span data-stu-id="4933e-108">When you have completed the maintenance rounds schedule, you can see all the job records relating to the round in the **All maintenance schedule** and **Open maintenance schedule lines**.</span></span>

>[!NOTE]
><span data-ttu-id="4933e-109">Wartungsdurchgänge können auch auf funktionaler Standorten eingerichtet werden, die zum Zeitpunkt der Erstellung des durchgangsbasierten Arbeitsauftrags auf den funktionalem Standort installierten Anlagen abgeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4933e-109">Maintenance rounds can also be set up on functional locations to be completed on the assets installed on the functional location at the time of creation of the round-based work order.</span></span> <span data-ttu-id="4933e-110">Weitere Informationen zum Einrichten von Wartungsdurchgängen auf funktionalen Standorten finden Sie unter [Erstellen von funktionalen Standorten](../functional-locations/create-functional-locations.md).</span><span class="sxs-lookup"><span data-stu-id="4933e-110">Refer to [Create functional locations](../functional-locations/create-functional-locations.md) for more information on the setup of maintenance rounds on functional locations.</span></span>

## <a name="set-up-a-maintenance-round"></a><span data-ttu-id="4933e-111">Einrichten eines Wartungsdurchgangs</span><span class="sxs-lookup"><span data-stu-id="4933e-111">Set up a maintenance round</span></span>

1. <span data-ttu-id="4933e-112">Klicken Sie auf **Anlagenverwaltung** > **Einstellungen** > **Vorbeugende Wartung** > **Wartungsdurchgänge**.</span><span class="sxs-lookup"><span data-stu-id="4933e-112">Click **Asset management** > **Setup** > **Preventive maintenance** > **Maintenance rounds**.</span></span>

2. <span data-ttu-id="4933e-113">Klicken Sie auf **Neu**, um einen neuen Wartungsdurchgang zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4933e-113">Click **New** to create a new maintenance round.</span></span>

3. <span data-ttu-id="4933e-114">Fügen Sie im Feld **Wartungsdurchgang** eine Kennung ein und im Feld **Name** einen Namen für den Wartungsdurchgang.</span><span class="sxs-lookup"><span data-stu-id="4933e-114">Insert and ID in the **Maintenance round** field, and a name for the maintenance round in the **Name** field.</span></span>

4. <span data-ttu-id="4933e-115">Wählen Sie im Feld **Startdatum** ein Startdatum für den Durchgang aus.</span><span class="sxs-lookup"><span data-stu-id="4933e-115">Select a start date for the round in the **Start date** field.</span></span>

5. <span data-ttu-id="4933e-116">n den Feldern **Innerhalb von Tagen beenden** und **Innerhalb von Stunden beenden** können Sie das erwartete Enddatum in Tagen oder Stunden eingeben.</span><span class="sxs-lookup"><span data-stu-id="4933e-116">In the **Finish within days** and **Finish within hours** fields, you can insert expected end date in days or hours.</span></span> <span data-ttu-id="4933e-117">Das erwartete Enddatum wird relativ zum erwarteten Startdatum berechnet, das beim Anlegen von Wartungszeitplanpositionen berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="4933e-117">The expected end date is calculated relative to the start date, which is calculated when maintenance schedule lines are created.</span></span> <span data-ttu-id="4933e-118">Sie können beispielsweise „7“ in das Feld **Innerhalb von Tagen beenden** einfügen, um anzugeben, dass der betreffende Auftrag innerhalb einer Woche nach dem Startdatum abgeschlossen sein soll.</span><span class="sxs-lookup"><span data-stu-id="4933e-118">For example, you can insert "7" in the **Finish within days** field to indicate that the related job should be completed within a week from the start date.</span></span>

6. <span data-ttu-id="4933e-119">Wählen Sie „Ja“ auf der Umschaltfläche **Automatisch einrichten**, wenn Arbeitsaufträge automatisch aus Wartungszeitplanpositionen erstellt werden sollen, die aus diesem Wartungsdurchgang angelegt werden.</span><span class="sxs-lookup"><span data-stu-id="4933e-119">Select "Yes" on the **Auto create** toggle button if work orders should automatically be created from maintenance schedule lines that are created from this maintenance round.</span></span>

7. <span data-ttu-id="4933e-120">Wählen Sie im Feld **Arbeitsauftragstyp** den Arbeitsauftragstyp aus, der für Arbeitsaufträge verwendet werden soll, die aus diesem Wartungsdurchgang angelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="4933e-120">In the **Work order type** field, select the work order type to be used on work orders created from this maintenance round.</span></span>

8. <span data-ttu-id="4933e-121">Wählen Sie im Feld **Servicelevel** den Servicelevel des Arbeitsauftrags aus, der für Arbeitsaufträge verwendet werden soll, die aus diesem Wartungsdurchgang angelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="4933e-121">In the **Service level** field, select the work order service level to be used on work orders created from this maintenance round.</span></span>

9. <span data-ttu-id="4933e-122">Klicken Sie auf dem Inforegister **Anlagenpositionen** auf **Hinzufügen**, um eine Anlage zum Wartungsdurchgang hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="4933e-122">On the **Asset lines** FastTab, click **Add** to add an asset to the maintenance round.</span></span>

10. <span data-ttu-id="4933e-123">Im Feld **Positionsnummer** wird automatisch eine Positionsnummer eingefügt, um die Reihenfolge der Anlagen im Wartungsdurchgang anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="4933e-123">A line number is automatically inserted in the **Line number** field to indicate the sequence of the assets in maintenance round.</span></span>

11. <span data-ttu-id="4933e-124">Wählen Sie im Feld **Anlage** die Anlage aus.</span><span class="sxs-lookup"><span data-stu-id="4933e-124">Select the asset in the **Asset** field.</span></span>

12. <span data-ttu-id="4933e-125">Wählen Sie im Feld **Wartungsauftragstyp** den Wartungsauftragstyp für die Anlage aus.</span><span class="sxs-lookup"><span data-stu-id="4933e-125">Select the maintenance job type for the asset in the **Maintenance job type** field.</span></span>

13. <span data-ttu-id="4933e-126">Bei Bedarf wählen Sie **Wartungsauftragstypvariante** und **Branche** bezogen auf die Wartungsauftragsart.</span><span class="sxs-lookup"><span data-stu-id="4933e-126">If required, select **Maintenance job typ variant** and **Trade** related to the maintenance job type.</span></span>

14. <span data-ttu-id="4933e-127">Wählen Sie im Feld **Periodentyp** die Wiederholung (Tag, Woche, etc.) aus.</span><span class="sxs-lookup"><span data-stu-id="4933e-127">Select the recurrence (day, week, etc.) in the **Period type** field.</span></span>

15. <span data-ttu-id="4933e-128">Geben Sie im Feld **Periodenhäufigkeit** die Anzahl der Wiederholungen für den Wartungsdurchgang ein.</span><span class="sxs-lookup"><span data-stu-id="4933e-128">In the **Period frequency** field, insert the number of recurrences for the maintenance round.</span></span> <span data-ttu-id="4933e-129">Beispiel: Wenn Sie im Feld **Periodentyp** „Tag“ gewählt haben und in diesem Feld die Zahl „7“ eingeben, werden bei der Planung der vorbeugenden Wartung einmal pro Woche neue Wartungsdurchgangspositionen angelegt.</span><span class="sxs-lookup"><span data-stu-id="4933e-129">Example: If you have selected "Day" in the **Period type** field, and you insert the number "7" in this field, new maintenance round lines are created during preventive maintenance scheduling once a week.</span></span>

16. <span data-ttu-id="4933e-130">Wählen Sie im Feld **Startdatum** ein Startdatum für die Anlage, die in den Wartungsdurchgang aufgenommen werden soll.</span><span class="sxs-lookup"><span data-stu-id="4933e-130">Select a start date for the asset to be included in the maintenance round in the **Start date** field.</span></span> <span data-ttu-id="4933e-131">Dieses Datum kann von dem im Wartungsdurchgang festgelegten Startdatum abweichen.</span><span class="sxs-lookup"><span data-stu-id="4933e-131">This date may differ from the start date set on the maintenance round.</span></span>

17. <span data-ttu-id="4933e-132">Wiederholen Sie die Schritte 9-16, um dem Wartungsdurchgang weitere Anlagen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="4933e-132">Repeat steps 9-16 to add more assets to the maintenance round.</span></span>

18. <span data-ttu-id="4933e-133">Klicken Sie auf dem Inforegister **Funktionaler Standort-Positionen** auf **Hinzufügen**, um einen funktionalen Standort zum Wartungsdurchgang hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="4933e-133">On the **Functional location lines** FastTab, click **Add** to add a functional location to the maintenance round.</span></span> <span data-ttu-id="4933e-134">Siehe Beschreibung der zugehörigen Felder oben.</span><span class="sxs-lookup"><span data-stu-id="4933e-134">Refer to the description of the related fields above.</span></span> <span data-ttu-id="4933e-135">Es stehen Ihnen die gleichen Felder zur Verfügung wie beim Erstellen einer Anlagenposition, aber Sie können bei Bedarf auch **Hersteller** und **Modell** für einen funktionalen Standort auswählen.</span><span class="sxs-lookup"><span data-stu-id="4933e-135">The same fields are available as for creating an asset line, but you can also select **Manufacturer** and **Model** for a functional location, if required.</span></span> <span data-ttu-id="4933e-136">Wenn Sie nur einen funktionalen Standort in einer Zeile auswählen, aber keine Auswahl in **Anlagentyp**, **Hersteller**, **Modell**, **Wartungsauftragstyp**, **Wartungsauftragstypvariante** und **Branche** treffen, werden alle Anlagen, die zum Zeitpunkt der Wartungsplanung mit diesem funktionalen Standort zusammenhängen, in den Wartungsdurchgang aufgenommen.</span><span class="sxs-lookup"><span data-stu-id="4933e-136">If you only select a functional location on a line, but make no selections in **Asset type**, **Manufacturer**, **Model**, **Maintenance job type**, **Maintenance job type variant** and **Trade**, all assets related to that functional location at the time of maintenance scheduling will be included in the maintenance round.</span></span>

19. <span data-ttu-id="4933e-137">Klicken Sie im Inforegister **Pools** auf **Hinzufügen**, um einen Arbeitsauftragspool auszuwählen, der in den Wartungsdurchgang aufgenommen werden soll.</span><span class="sxs-lookup"><span data-stu-id="4933e-137">On the **Pools** FastTab, click **Add** to select a work order pool to be included in the maintenance round.</span></span> <span data-ttu-id="4933e-138">Einige Arbeitsauftragspools können mit einem Wartungsdurchgang verbunden werden.</span><span class="sxs-lookup"><span data-stu-id="4933e-138">Several work order pools can be connected to one maintenance round.</span></span>

20. <span data-ttu-id="4933e-139">Speichern Sie Ihre Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="4933e-139">Save your setup.</span></span>

>[!NOTE]
><span data-ttu-id="4933e-140">Die Felder **Anlagen** und **Positionen** in der Gruppe **Details** auf dem Inforegister **Kopfzeile** zeigen die Gesamtzahl der Anlagen und Positionen, die sich auf den ausgewählten Wartungsdurchgang beziehen.</span><span class="sxs-lookup"><span data-stu-id="4933e-140">The **Assets** and **Lines** fields located in the **Details** group on the **Header** FastTab show the total number of assets and lines related to the selected maintenance round.</span></span>

<span data-ttu-id="4933e-141">Die folgende Abbildung zeigt das Beispiel einer Wartungsdurchführung mit drei Anlagen.</span><span class="sxs-lookup"><span data-stu-id="4933e-141">The illustration below shows and example of a maintenance round containing three assets.</span></span>

![Abbildung 1](media/13-preventive-maintenance.png)


## <a name="schedule-maintenance-rounds"></a><span data-ttu-id="4933e-143">Wartungsdurchgänge terminieren</span><span class="sxs-lookup"><span data-stu-id="4933e-143">Schedule maintenance rounds</span></span>

<span data-ttu-id="4933e-144">Wenn Sie einen Wartungsdurchgang eingerichtet haben, führen Sie einen Zeitplanauftrag aus, um alle mit dem Wartungsdurchgang verbundenen Aufträge einzuplanen.</span><span class="sxs-lookup"><span data-stu-id="4933e-144">When you've set up a maintenance round, you run a schedule job to schedule all the jobs related to the maintenance round.</span></span>

1. <span data-ttu-id="4933e-145">Klicken Sie auf die Schlatfläche **Anlagenverwaltung** > **Periodisch** > **Vorbeugende Wartung** > **Wartungsdurchgänge planen**, oder **Anlagenverwaltung** > **Allgemein** > **Wartungszeitplan** > **Gesamter Wartungszeitplan** oder **Wartungszeitplanpositionen öffnen** oder **Wartungszeitplanpools öffnen** > Wartungszeitplanposition in der Liste auswählen > **Wartungsdurchgänge**.</span><span class="sxs-lookup"><span data-stu-id="4933e-145">Click **Asset management** > **Periodic** > **Preventive maintenance** > **Schedule maintenance rounds**, or **Asset management** > **Common** > **Maintenance schedule** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools** > select maintenance schedule line in the list > **Maintenance rounds** button.</span></span>

2. <span data-ttu-id="4933e-146">Wählen Sie im Feld **Periode** den Periodentyp, der für den Terminierungsauftrag verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4933e-146">In the **Period** field, select the period type to be used for the scheduling job.</span></span>

3. <span data-ttu-id="4933e-147">Geben Sie im Feld **Periodenhäufigkeit** die Anzahl der Perioden ein, die in den Terminierungsauftrag aufgenommen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4933e-147">In the **Period frequency** field, insert the number of periods to be included in the scheduling job.</span></span> <span data-ttu-id="4933e-148">Der Beginn der Terminierung ist das aktuelle Datum.</span><span class="sxs-lookup"><span data-stu-id="4933e-148">The start of the scheduling is the current date.</span></span>

4. <span data-ttu-id="4933e-149">Wählen Sie „Ja“ auf der Umschaltfläche **Automatisch einrichten**, wenn ein Arbeitsauftrag auf der Grundlage eines Wartungsdurchgangs automatisch erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4933e-149">Select "Yes" on the **Auto create** toggle button if a work order should automatically be created on the basis of a maintenance round.</span></span>

>[!NOTE]
><span data-ttu-id="4933e-150">Wenn diese Umschaltfläche auf „Ja“ gesetzt ist und die Umschaltfläche **Automatisch einrichten** auch im Wartungsdurchgang im Formular **Wartungsdurchgänge** auf „Ja“ gesetzt ist, werden Arbeitsaufträge auf der Grundlage der Wartungsdurchgangspositionen angelegt und Wartungszeitplanpositionen mit dem Status „Arbeitsauftrag angelegt“ ebenfalls erstellt.</span><span class="sxs-lookup"><span data-stu-id="4933e-150">If this toggle button is set to "Yes", and the **Auto create** toggle button is also set to "Yes" on the maintenance round in **Maintenance rounds** form, work orders are created based on the maintenance round lines, and maintenance schedule lines with status "Work order created" are also created.</span></span> <span data-ttu-id="4933e-151">Wenn nur eine der Umschaltflächen **Automatisch einrichten** auf „Ja“ gesetzt ist, in diesem Dropdownmenü oder in **Wartungsdurchgängen**, werden nur Wartungszeitplanpositionen mit dem Status „Erstellt“ angelegt.</span><span class="sxs-lookup"><span data-stu-id="4933e-151">If only one of the **Auto create** toggle buttons is set to "Yes", in this drop-down or in **Maintenance rounds**, only maintenance schedule lines are created with status "Created".</span></span> <span data-ttu-id="4933e-152">In diesem Fall werden keine Arbeitsaufträge erstellt.</span><span class="sxs-lookup"><span data-stu-id="4933e-152">In that case, no work orders are created.</span></span>

5. <span data-ttu-id="4933e-153">Bei Bedarf können Sie bestimmte Durchgänge oder ein anderes Startdatum für den Zeitplanauftrag auswählen.</span><span class="sxs-lookup"><span data-stu-id="4933e-153">If required, you can select specific rounds or another start date for the schedule job.</span></span> <span data-ttu-id="4933e-154">Klicken Sie **Filtern** und fügen Sie die einzubeziehenden Durchgänge hinzu.</span><span class="sxs-lookup"><span data-stu-id="4933e-154">Click **Filter**, and add the rounds to be included.</span></span>

6. <span data-ttu-id="4933e-155">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="4933e-155">Click **OK**.</span></span>

7. <span data-ttu-id="4933e-156">Sie können nun die Wartungsdurchgangsaufträge in **Anlagenverwaltung** > **Allgemein** > **Wartungszeitplan** > **Alle Wartungszeitpläne** oder **Wartungszeitplanpositionen öffnen** sehen.</span><span class="sxs-lookup"><span data-stu-id="4933e-156">You are now able to see the maintenance rounds jobs in **Asset management** > **Common** > **Maintenance schedule** > **All maintenance schedule** or **Open maintenance schedule lines**.</span></span> <span data-ttu-id="4933e-157">Wenn die terminierten Durchgänge an einen Arbeitsauftragspool angeschlossen sind, sehen Sie auch Wartungszeitplanpositionen in **Wartungszeitplanpools öffnen**.</span><span class="sxs-lookup"><span data-stu-id="4933e-157">If the scheduled rounds are connected to a work order pool, you also see maintenance schedule lines in **Open maintenance schedule pools**.</span></span> <span data-ttu-id="4933e-158">Wartungszeitplanpositionen, die aus einem Durchgang angelegt wurden, haben den Referenztyp „Wartungsdurchgänge“.</span><span class="sxs-lookup"><span data-stu-id="4933e-158">Maintenance schedule lines created from a round have the reference type "Maintenance rounds".</span></span>

<span data-ttu-id="4933e-159">Die zwei folgenden Abbildungen zeigen einen Zeitplaneinzelvorgang im Dialog **Wartungszeitplan anzeigen** und die Wartungsplanpositionen, die in **Alle Wartungszeitpläne** erstellt werden, die auf diesem Zeitplaneinzelvorgang basieren.</span><span class="sxs-lookup"><span data-stu-id="4933e-159">The two illustrations below show a schedule job in the **Schedule maintenance rounds** dialog, and the maintenance schedule lines created in **All maintenance schedule** based on that schedule job.</span></span>

![Abbildung 2](media/14-preventive-maintenance.png)

![Abbildung 3](media/15-preventive-maintenance.png)

- <span data-ttu-id="4933e-162">Wenn Arbeitsaufträge für Anlagen, die unter eine Lieferantengarantie fallen, manuell erstellt werden, erscheint ein Dialogfenster, um den Benutzer auf die Garantie aufmerksam zu machen</span><span class="sxs-lookup"><span data-stu-id="4933e-162">When work orders are manually created on assets that are covered by a vendor warranty, a dialog box is shown to make the user aware of the warranty.</span></span> <span data-ttu-id="4933e-163">Die Erstellung des Arbeitsauftrags kann dann abgebrochen werden.</span><span class="sxs-lookup"><span data-stu-id="4933e-163">The creation of the work order can then be canceled.</span></span> <span data-ttu-id="4933e-164">Bei Arbeitsaufträgen, die automatisch angelegt werden, entfällt die Prüfung auf eine Garantiebeziehung.</span><span class="sxs-lookup"><span data-stu-id="4933e-164">The check for a warranty relation is omitted for work orders that are automatically created.</span></span>  
- <span data-ttu-id="4933e-165">Sie können einen Batchauftrag auf dem Inforegister **Im Hintergrund ausführen** einrichten, um Durchgänge in regelmäßigen Abständen einzuplanen.</span><span class="sxs-lookup"><span data-stu-id="4933e-165">You can set up a batch job on the **Run in the background** FastTab to schedule rounds at regular intervals.</span></span>  
- <span data-ttu-id="4933e-166">Wenn ein Durchgang in mehreren Arbeitsauftragspools enthalten ist (siehe [Arbeitsauftragspools](../work-orders/work-order-pools.md)), wird für jeden Pool ein Datensatz in **Wartungszeitplanpools öffnen** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4933e-166">If a round is included in several work order pools (refer to [Work order pools](../work-orders/work-order-pools.md)), one record is shown for each pool in **Open maintenance schedule pools**.</span></span> <span data-ttu-id="4933e-167">Dies erfolgt, um die Filtermöglichkeiten für Arbeitsauftragspools zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="4933e-167">This is done to optimize the filtering options for work order pools.</span></span>

