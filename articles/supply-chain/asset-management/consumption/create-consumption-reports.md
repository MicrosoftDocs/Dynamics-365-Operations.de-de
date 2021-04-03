---
title: Verbrauchsberichte erstellen
description: In diesem Thema wird erläutert, wie Verbrauchsberichte in der Anlagenverwaltung erstellt werden.
author: josaw1
manager: tfehr
ms.date: 08/21/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0cda21addfdc524537177740ebba6414ef8b4b96
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5260009"
---
# <a name="create-consumption-reports"></a><span data-ttu-id="ac18b-103">Verbrauchsberichte erstellen</span><span class="sxs-lookup"><span data-stu-id="ac18b-103">Create consumption reports</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="ac18b-104">Wenn Sie Verbrauchserfassungen für Arbeitsaufträge in der Anlagenverwaltung erstellt und gebucht haben, sind zwei Berichte für die Anzeige von Verbrauchsdetails verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ac18b-104">When you've created and posted consumption registrations on work orders in Asset Management, two reports are available to display consumption details.</span></span>


## <a name="asset-consumption-report"></a><span data-ttu-id="ac18b-105">Anlage – Verbrauchsbericht</span><span class="sxs-lookup"><span data-stu-id="ac18b-105">Asset consumption report</span></span>

<span data-ttu-id="ac18b-106">Wenn Sie den Verbrauch für Arbeitsaufträge gebucht haben, können Sie einen Anlagenverbrauchsbericht drucken.</span><span class="sxs-lookup"><span data-stu-id="ac18b-106">When you have posted consumption on work orders, you can print an asset consumption report.</span></span> <span data-ttu-id="ac18b-107">Im Bericht werden die Stunden, Stundenkosten, Artikelkosten und Aufwendungen, die für Anlagen gebucht wurden, angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ac18b-107">The report displays hours, hour costs, item costs, and expenses posted on assets.</span></span>

1. <span data-ttu-id="ac18b-108">Klicken Sie auf **Anlagenmanagement** > **Berichte** > **Anlagen** > **Anlagenverbrauch**.</span><span class="sxs-lookup"><span data-stu-id="ac18b-108">Click **Asset management** > **Reports** > **Assets** > **Asset consumption**.</span></span>

2. <span data-ttu-id="ac18b-109">Wählen Sie im Dialogfeld **Anlagenverbrauch** die Parameter und die Detailebene für die Anzeige aus, indem Sie **Ja** bei den relevanten Umschaltschaltflächen auswählen und eine funktionale Standortebene im Abschnitt **Anzeigen** einfügen.</span><span class="sxs-lookup"><span data-stu-id="ac18b-109">In the **Asset consumption** dialog, select the parameters and detail level you want to see by selecting **Yes** on the relevant toggle buttons, and inserting a functional location level in the **Show** section.</span></span>
    - <span data-ttu-id="ac18b-110">Sie können das Feld **Ebenen** verwenden, um anzugeben, wie detailliert die Anlagenpositionen bezüglich der funktionalen Standorte sein sollen.</span><span class="sxs-lookup"><span data-stu-id="ac18b-110">You can use the **Levels** field to indicate how detailed you want the asset lines to be regarding functional locations.</span></span> 
    
        <span data-ttu-id="ac18b-111">Wenn Sie beispielsweise die Zahl „1“ im Feld eingeben und eine funktionale Standortstruktur auf mehreren Ebenen haben, werden alle Anlagen für einen funktionalen Standort auf der höchsten Ebene angezeigt, und daher wird eine Position von den funktionalen Standorten auf einer niedrigeren Ebene hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ac18b-111">For example, if you enter the number "1" in the field, and you have a multi-level functional location structure, all assets for a functional location will be shown on the top level, and therefore a line may be added up from functional locations located at a lower level.</span></span> 
        
        <span data-ttu-id="ac18b-112">Wenn Sie die Zahl „0“ im Feld **Ebenen** eingeben, wird ein detailliertes Ergebnis mit allen Anlagen für alle funktionalen Standortebenen angezeigt, denen sie zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="ac18b-112">If you enter the number "0" in the **Levels** field, you will see a detailed result showing all assets on all the functional location levels to which they are related.</span></span> 
        
    - <span data-ttu-id="ac18b-113">Wählen Sie **Ja** bei der **Summe für alle Unteranlagen**-Umschaltschaltfläche aus, um Summen für jede Unteranlage im Bericht anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ac18b-113">Select **Yes** on the **Sum on all sub assets** toggle button to see sums for each sub asset in the report.</span></span>

3. <span data-ttu-id="ac18b-114">Wählen Sie ein Datumsintervall im Abschnitt **Datumsangaben** aus.</span><span class="sxs-lookup"><span data-stu-id="ac18b-114">Select a date interval in the **Dates** section.</span></span>

4. <span data-ttu-id="ac18b-115">Wählen Sie im Inforegister **Ziel** aus, ob Sie den Bericht auf dem Bildschirm anzeigen, ihn drucken oder als Datei oder E-Mail speichern möchten.</span><span class="sxs-lookup"><span data-stu-id="ac18b-115">On the **Destination** FastTab, select if you want to display the report on screen, print it, or save it as a file or email.</span></span>

5. <span data-ttu-id="ac18b-116">Bei Bedarf können Sie auswählen, dass bestimmte Anlagen im Bericht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ac18b-116">If required, you can select specific assets to be displayed in the report.</span></span> <span data-ttu-id="ac18b-117">Klicken Sie im Inforegister **Einzuschließende Datensätze** auf **Filtern**, und fügen die Anlagen hinzu, die im Bericht enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="ac18b-117">On the **Records to include** FastTab, click **Filter**, and add the assets you want to include in the report.</span></span>

6. <span data-ttu-id="ac18b-118">Klicken Sie auf **OK**, um den Bericht zu generieren.</span><span class="sxs-lookup"><span data-stu-id="ac18b-118">Click **OK** to generate the report.</span></span>


## <a name="work-order-consumption-report"></a><span data-ttu-id="ac18b-119">Arbeitsauftrags-Verbrauchsbericht</span><span class="sxs-lookup"><span data-stu-id="ac18b-119">Work order consumption report</span></span>

<span data-ttu-id="ac18b-120">Wenn Sie den Verbrauch für Arbeitsaufträge gebucht haben, können Sie einen Arbeitsauftrags-Verbrauchsbericht drucken.</span><span class="sxs-lookup"><span data-stu-id="ac18b-120">When you have posted consumption on work orders, you can print a work order consumption report.</span></span> <span data-ttu-id="ac18b-121">Im Bericht werden die Stunden, Stundenkosten, Artikelkosten und Aufwendungen, die für Arbeitsaufträge gebucht wurden, angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ac18b-121">The report displays hours, hour costs, item costs, and expenses posted on work orders.</span></span>

1. <span data-ttu-id="ac18b-122">Klicken Sie auf **Anlagenverwaltung** > **Berichte** > **Arbeitsaufträge** > **Arbeitsauftragsverbrauch**.</span><span class="sxs-lookup"><span data-stu-id="ac18b-122">Click **Asset management** > **Reports** > **Work orders** > **Work order consumption**.</span></span>

2. <span data-ttu-id="ac18b-123">Wählen Sie im Dialogfeld **Arbeitsauftragsverbrauch** die Parameter aus, die im Bericht enthalten sein sollen, indem Sie **Ja** bei den relevanten Umschaltschaltflächen im Abschnitt **Anzeigen** auswählen.</span><span class="sxs-lookup"><span data-stu-id="ac18b-123">In the **Work order consumption** dialog, select the parameters you want to include in the report by selecting **Yes** on the relevant toggle buttons in the **Show** section.</span></span>

3. <span data-ttu-id="ac18b-124">Wählen Sie ein Datumsintervall im Abschnitt **Datumsangaben** aus.</span><span class="sxs-lookup"><span data-stu-id="ac18b-124">Select a date interval in the **Dates** section.</span></span>

4. <span data-ttu-id="ac18b-125">Wählen Sie im Inforegister **Ziel** aus, ob Sie den Bericht auf dem Bildschirm anzeigen, ihn drucken oder als Datei oder E-Mail speichern möchten.</span><span class="sxs-lookup"><span data-stu-id="ac18b-125">On the **Destination** FastTab, select if you want to display the report on screen, print it, or save it as a file or email.</span></span>

5. <span data-ttu-id="ac18b-126">Bei Bedarf können Sie auswählen, dass bestimmte Arbeitsaufträge im Bericht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ac18b-126">If required, you can select specific work orders to be displayed in the report.</span></span> <span data-ttu-id="ac18b-127">Klicken Sie im Inforegister **Einzuschließende Datensätze** auf **Filtern**, und fügen die Arbeitsaufträge hinzu, die im Bericht enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="ac18b-127">On the **Records to include** FastTab, click **Filter**, and add the work orders you want to include in the report.</span></span>

6. <span data-ttu-id="ac18b-128">Klicken Sie auf **OK**, um den Bericht zu generieren.</span><span class="sxs-lookup"><span data-stu-id="ac18b-128">Click **OK** to generate the report.</span></span>


>[!NOTE]
><span data-ttu-id="ac18b-129">Sie können auch einen [Arbeitsauftragsbericht](../work-orders/work-order-report.md) generieren, der zusätzliche Arbeitsauftragseinzelheiten enthält.</span><span class="sxs-lookup"><span data-stu-id="ac18b-129">You can also generate a [work order report](../work-orders/work-order-report.md), which contains more work order details.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]