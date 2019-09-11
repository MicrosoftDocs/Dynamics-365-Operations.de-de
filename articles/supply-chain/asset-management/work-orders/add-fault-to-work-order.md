---
title: Fehler zum Arbeitsauftrag hinzufügen
description: In diesem Thema wird beschrieben, wie Fehlererfassungen zu Arbeitsaufträgen in Asset Management hinzugefügt werden.
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7c86973ca44d9113d14e180e27cc51343da5d2c0
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875677"
---
# <a name="add-fault-to-work-order"></a><span data-ttu-id="f7e89-103">Fehler zum Arbeitsauftrag hinzufügen</span><span class="sxs-lookup"><span data-stu-id="f7e89-103">Add fault to work order</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="f7e89-104">Sie können einem Arbeitsauftrag Fehlereinstellungen im Fehlerdesigner hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="f7e89-104">You can add faults set up in the fault designer to a work order.</span></span> <span data-ttu-id="f7e89-105">Die Anlage, die im Arbeitsauftrag ausgewählt wird, muss Anlagentypen enthalten, mit denen ein oder mehrere Fehlerdatensätze verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="f7e89-105">The asset selected in the work order must contain asset types that have one or more fault records connected to it.</span></span> <span data-ttu-id="f7e89-106">Lesen Sie mehr über die Einstellungen im Abschnitt [Fehlermanagement](../setup-for-work-orders/fault-management.md).</span><span class="sxs-lookup"><span data-stu-id="f7e89-106">Read more about setup in the [Fault management](../setup-for-work-orders/fault-management.md) section.</span></span>

1. <span data-ttu-id="f7e89-107">Klicken Sie auf **Anlagenverwaltung** > **Allgemein** > **Arbeitsaufträge** > **Alle Arbeitsaufträge** oder **Aktive Arbeitsaufträge**.</span><span class="sxs-lookup"><span data-stu-id="f7e89-107">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="f7e89-108">Wählen Sie in der Liste den Arbeitsauftrag aus, für den Sie eine Fehlererfassung vornehmen möchten, und klicken Sie auf **Anlagenfehler**.</span><span class="sxs-lookup"><span data-stu-id="f7e89-108">In the list, select the work order on which you want to make a fault registration and click **Asset fault**.</span></span>

3. <span data-ttu-id="f7e89-109">Klicken Sie auf dem Inforegister **Symptome** auf **Position hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="f7e89-109">On the **Symptoms** FastTab, click **Add line**.</span></span> <span data-ttu-id="f7e89-110">Eine laufende Fehlernummer wird automatisch im **Fehler** eingefügt.</span><span class="sxs-lookup"><span data-stu-id="f7e89-110">A sequential fault number is automatically inserted in the **Fault** field.</span></span>

4. <span data-ttu-id="f7e89-111">Wählen Sie das zutreffende Symptom im Feld **Fehlersymptom** aus.</span><span class="sxs-lookup"><span data-stu-id="f7e89-111">Select the relevant symptom in the **Fault symptom** field.</span></span>

5. <span data-ttu-id="f7e89-112">Wählen Sie **Fehlerbereich** und **Fehlertyp** aus.</span><span class="sxs-lookup"><span data-stu-id="f7e89-112">Select **Fault area** and **Fault type**.</span></span>

6. <span data-ttu-id="f7e89-113">Das Feld **Fehlerdatum** wird automatisch auf das aktuelle Datum festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f7e89-113">In the **Fault date** field, the current date is automatically inserted.</span></span> <span data-ttu-id="f7e89-114">Bei Bedarf können Sie ein anderes Datum auswählen.</span><span class="sxs-lookup"><span data-stu-id="f7e89-114">You can select another date, if necessary.</span></span>

7. <span data-ttu-id="f7e89-115">Im Inforegister **Ursachen für ausgewähltes Symptom** fügen Sie eine Position hinzu, die die Ursache des Problems beschreibt.</span><span class="sxs-lookup"><span data-stu-id="f7e89-115">On the **Causes for selected symptom** FastTab, add a line describing the cause of the problem.</span></span>

8. <span data-ttu-id="f7e89-116">Im Inforegister **Lösungen für ausgewähltes Symptom** fügen Sie eine Position hinzu, die eine mögliche Lösung des Problems beschreibt.</span><span class="sxs-lookup"><span data-stu-id="f7e89-116">On the **Remedies for selected symptom** FastTab, add a line describing a possible solution to the problem.</span></span>

9. <span data-ttu-id="f7e89-117">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="f7e89-117">Click **Save**.</span></span>

![Abbildung 1](media/19-work-orders.png)


## <a name="view-asset-faults"></a><span data-ttu-id="f7e89-119">Anzeigen von Anlagenfehlern</span><span class="sxs-lookup"><span data-stu-id="f7e89-119">View asset faults</span></span>

<span data-ttu-id="f7e89-120">In der Liste **Anlagenfehler** können Sie eine Übersicht aller Fehler erhalten, die für Anlagen erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="f7e89-120">In the **Asset faults** list, you can get an overview of all faults registered on assets.</span></span>

<span data-ttu-id="f7e89-121">Klicken Sie auf **Anlagenverwaltung** > **Abfragen** > **Anlagenfehler** > **Anlagenfehler**, um die Liste zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f7e89-121">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset faults** to open the list.</span></span>


## <a name="print-asset-fault-report"></a><span data-ttu-id="f7e89-122">Anlagenfehlerberichte drucken</span><span class="sxs-lookup"><span data-stu-id="f7e89-122">Print asset fault report</span></span>

<span data-ttu-id="f7e89-123">Auf der Listenseite **Alle Anlagen** können Sie einen Anlagenfehlerbericht drucken, der alle Fehlererfassungen sowie eine grafische Übersicht über Fehlerstatistiken anzeigt.</span><span class="sxs-lookup"><span data-stu-id="f7e89-123">From the **All assets** list page, you can print an asset fault report displaying all fault registrations as well as a graphic overview of fault statistics.</span></span>

1. <span data-ttu-id="f7e89-124">Klicken Sie auf **Anlagenmanagement** > **Allgemein** > **Anlagen** > **Alle Anlagen**.</span><span class="sxs-lookup"><span data-stu-id="f7e89-124">Click **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="f7e89-125">Wählen Sie in der Liste **Anlagen** eine Anlage aus, für die Sie einen Fehlerbericht drucken möchten.</span><span class="sxs-lookup"><span data-stu-id="f7e89-125">In the **Assets** list, select the asset for which you want to print a fault report.</span></span>

3. <span data-ttu-id="f7e89-126">Klicken Sie auf der Registerkarte **Allgemein** > Abschnitt **Berichte** auf **Anlagenfehler**.</span><span class="sxs-lookup"><span data-stu-id="f7e89-126">On the **General** tab > **Reports section**, click **Asset fault**.</span></span>

4. <span data-ttu-id="f7e89-127">Fügen Sie eine bestimmte Periode ein, oder wählen Sie einen Fehlertyp.</span><span class="sxs-lookup"><span data-stu-id="f7e89-127">Insert a specific period, or select a fault type.</span></span>

5. <span data-ttu-id="f7e89-128">Klicken Sie zum Drucken des Berichts auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="f7e89-128">Click **OK** to print the report.</span></span>

>[!NOTE]
><span data-ttu-id="f7e89-129">Sie können auch einen Fehlerbericht für mehrere Anlagen oder Anlagentypen drucken, indem Sie auf **Anlagenverwaltung** > **Berichte** > **Anlagen** > **Anlagenfehler** klicken.</span><span class="sxs-lookup"><span data-stu-id="f7e89-129">You can also print a fault report for several assets or asset types by clicking **Asset management** > **Reports** > **Assets** > **Asset fault**.</span></span>

