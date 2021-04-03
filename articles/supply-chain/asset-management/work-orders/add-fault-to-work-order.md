---
title: Fehler zum Arbeitsauftrag hinzufügen
description: In diesem Thema wird beschrieben, wie Fehlererfassungen zu Arbeitsaufträgen in Asset Management hinzugefügt werden.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 489add5befe3660ad49e238b659bc8adbe1418a4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263757"
---
# <a name="add-fault-to-work-order"></a><span data-ttu-id="6f045-103">Fügen Sie Fehler zum Arbeitsauftrag hinzu</span><span class="sxs-lookup"><span data-stu-id="6f045-103">Add fault to work order</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="6f045-104">Sie können einem Arbeitsauftrag Fehler hinzufügen, die im Fehlerdesigner eingerichtet wurden.</span><span class="sxs-lookup"><span data-stu-id="6f045-104">You can add faults that were set up in the fault designer to a work order.</span></span> <span data-ttu-id="6f045-105">Mit den Anlagetypen, die für die Anlage verwendet werden, die im Arbeitsauftrag ausgewählt ist, müssen ein oder mehrere Fehlerdatensätze verbunden sein.</span><span class="sxs-lookup"><span data-stu-id="6f045-105">One or more fault records must be connected to the asset types that are used for the asset that is selected in the work order.</span></span> <span data-ttu-id="6f045-106">Weitere Informationen zum Einrichten finden Sie unter [Fehlermanagement](../setup-for-work-orders/fault-management.md).</span><span class="sxs-lookup"><span data-stu-id="6f045-106">For more information about the setup, see [Fault management](../setup-for-work-orders/fault-management.md).</span></span>

1. <span data-ttu-id="6f045-107">Wählen Sie **Anlagenverwaltung** > **Allgemein** > **Arbeitsaufträge** > **Alle Arbeitsaufträge** oder **Aktive Arbeitsaufträge** aus.</span><span class="sxs-lookup"><span data-stu-id="6f045-107">Select **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="6f045-108">Wählen Sie den Arbeitsauftrag aus, für den Sie eine Fehlererfassung durchführen möchten, und wählen Sie dann im Aktivitätsbereich auf der **Arbeitsauftrag**-Registerkarte in der **Anlage**-Gruppe **Anlagenfehler** aus.</span><span class="sxs-lookup"><span data-stu-id="6f045-108">Select the work order to make a fault registration on, and then, on the Action Pane, on the **Work order** tab, in the **Asset** group, select **Asset fault**.</span></span>

3. <span data-ttu-id="6f045-109">Wählen Sie auf dem Inforegister **Symptome** die Option **Position hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="6f045-109">On the **Symptoms** FastTab, select **Add line**.</span></span> <span data-ttu-id="6f045-110">Eine laufende Fehlernummer wird automatisch im **Fehler** eingegeben.</span><span class="sxs-lookup"><span data-stu-id="6f045-110">A sequential fault number is automatically entered in the **Fault** field.</span></span>

4. <span data-ttu-id="6f045-111">Wählen Sie das zutreffende Symptom im Feld **Fehlersymptom** aus.</span><span class="sxs-lookup"><span data-stu-id="6f045-111">In the **Fault symptom** field, select the relevant symptom.</span></span>

5. <span data-ttu-id="6f045-112">Wählen Sie in den Feldern **Fehlerbereich** und **Fehlertyp** die entsprechenden Werte aus.</span><span class="sxs-lookup"><span data-stu-id="6f045-112">In the **Fault area** and **Fault type** fields, select the appropriate values.</span></span>

6. <span data-ttu-id="6f045-113">Das Feld **Fehlerdatum** wird automatisch auf das aktuelle Datum festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6f045-113">In the **Fault date** field, the current date is automatically inserted.</span></span> <span data-ttu-id="6f045-114">Sie können bei Bedarf ein anderes Datum auswählen.</span><span class="sxs-lookup"><span data-stu-id="6f045-114">You can select a different date as you require.</span></span>

7. <span data-ttu-id="6f045-115">Im Inforegister **Ursachen für ausgewähltes Symptom** fügen Sie eine Position hinzu, die die Ursache des Problems beschreibt.</span><span class="sxs-lookup"><span data-stu-id="6f045-115">On the **Causes for selected symptom** FastTab, add a line to describe the cause of the issue.</span></span>

8. <span data-ttu-id="6f045-116">Im Inforegister **Lösungen für ausgewähltes Symptom** fügen Sie eine Position hinzu, die eine mögliche Lösung des Problems beschreibt.</span><span class="sxs-lookup"><span data-stu-id="6f045-116">On the **Remedies for selected symptom** FastTab, add a line to describe a possible solution to the issue.</span></span>

9. <span data-ttu-id="6f045-117">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="6f045-117">Select **Save**.</span></span>

<span data-ttu-id="6f045-118">Die folgende Abbildung zeigt das Beispiel einer Fehlererfassung.</span><span class="sxs-lookup"><span data-stu-id="6f045-118">The illustration below shows an example of a fault registration.</span></span>

![Abbildung 1](media/19-work-orders.png)


## <a name="view-asset-faults"></a><span data-ttu-id="6f045-120">Anzeigen von Anlagenfehlern</span><span class="sxs-lookup"><span data-stu-id="6f045-120">View asset faults</span></span>

<span data-ttu-id="6f045-121">In der Liste **Anlagenfehler** können Sie eine Übersicht aller Fehler erhalten, die für Anlagen erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="6f045-121">In the **Asset faults** list, you can get an overview of all faults registered on assets.</span></span>

<span data-ttu-id="6f045-122">Auf der Listenseite **Anlagenfehler** können Sie eine Übersicht aller Fehler erhalten, die für Anlagen erfasst wurden.</span><span class="sxs-lookup"><span data-stu-id="6f045-122">On the **Asset faults** list page, you can get an overview of all faults that have been registered on assets.</span></span> <span data-ttu-id="6f045-123">Wählen Sie **Anlagenverwaltung** > **Abfragen** > **Anlagenfehler** > **Anlagenfehler** aus, um die Seite zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="6f045-123">To open the page, select **Asset management** > **Inquiries** > **Asset fault** > **Asset faults**.</span></span>


## <a name="print-asset-fault-report"></a><span data-ttu-id="6f045-124">Anlagenfehlerberichte drucken</span><span class="sxs-lookup"><span data-stu-id="6f045-124">Print asset fault report</span></span>

<span data-ttu-id="6f045-125">Auf der Listenseite **Alle Anlagen** können Sie einen Anlagenfehlerbericht drucken, der alle Fehlererfassungen sowie eine grafische Übersicht über Fehlerstatistiken anzeigt.</span><span class="sxs-lookup"><span data-stu-id="6f045-125">From the **All assets** list page, you can print an asset fault report that shows all fault registrations and a graphical overview of fault statistics.</span></span>

1. <span data-ttu-id="6f045-126">Wählen Sie **Anlagenverwaltung** > **Allgemeines** > **Anlagen** > **Alle Anlagen**.</span><span class="sxs-lookup"><span data-stu-id="6f045-126">Select **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="6f045-127">Wählen Sie die Anlage aus, für die Sie den Fehlerbericht drucken möchten.</span><span class="sxs-lookup"><span data-stu-id="6f045-127">Select the asset to print a fault report for.</span></span>

3. <span data-ttu-id="6f045-128">Wählen Sie im Aktivitätsbereich auf der Registerkarte **Allgemein** in der Gruppe **Berichte** **Anlagenfehler** aus.</span><span class="sxs-lookup"><span data-stu-id="6f045-128">On the Action Pane, on the **General** tab, in the **Reports** group, select **Asset fault**.</span></span>

4. <span data-ttu-id="6f045-129">Geben Sie eine bestimmte Periode ein, oder wählen Sie einen Fehlertyp aus.</span><span class="sxs-lookup"><span data-stu-id="6f045-129">Enter a specific period, or select a fault type.</span></span>

5. <span data-ttu-id="6f045-130">Wählen Sie zum Drucken des Berichts **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="6f045-130">Select **OK** to print the report.</span></span>

>[!NOTE]
><span data-ttu-id="6f045-131">Sie können auch einen Fehlerbericht für mehrere Anlagen oder Anlagentypen drucken, indem Sie **Anlagenverwaltung** > **Berichte** > **Anlagen** > **Anlagenfehler** auswählen.</span><span class="sxs-lookup"><span data-stu-id="6f045-131">To print a fault report for several assets or asset types, select **Asset management** > **Reports** > **Assets** > **Asset fault**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]