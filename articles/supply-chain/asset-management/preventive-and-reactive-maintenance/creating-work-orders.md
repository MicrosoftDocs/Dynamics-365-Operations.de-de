---
title: Erstellen von Arbeitsaufträgen
description: In diesem Thema wird erläutert, wie Sie Arbeitsaufträge in der Anlagenverwaltung erstellen.
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
ms.openlocfilehash: b23ed3251b2f6cf4f34b423ce2f85301d6ab31a1
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875667"
---
# <a name="creating-work-orders"></a><span data-ttu-id="c952f-103">Erstellen von Arbeitsaufträgen</span><span class="sxs-lookup"><span data-stu-id="c952f-103">Creating work orders</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="c952f-104">Wenn Sie vorbeugende Wartungsaufträge geplant haben, ist der nächste Schritt, Arbeitsaufträge für die Einzelvorgänge zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c952f-104">When you have scheduled preventive maintenance jobs, next step is to create work orders for the jobs.</span></span> <span data-ttu-id="c952f-105">Dies erfolgt in einem der Wartungszeitpläne.</span><span class="sxs-lookup"><span data-stu-id="c952f-105">This is done in one of the maintenance schedules.</span></span> <span data-ttu-id="c952f-106">Die geplanten Einzelvorgänge in einem Wartungszeitplan können verschiedene Referenztypen haben:</span><span class="sxs-lookup"><span data-stu-id="c952f-106">The scheduled jobs in a maintenance schedule can have different reference types:</span></span>

| <span data-ttu-id="c952f-107">Referenztyp</span><span class="sxs-lookup"><span data-stu-id="c952f-107">Reference type</span></span> | <span data-ttu-id="c952f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c952f-108">Description</span></span>                    |
|-----------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c952f-109">Wartungspläne</span><span class="sxs-lookup"><span data-stu-id="c952f-109">Maintenance plans</span></span>     | <span data-ttu-id="c952f-110">Vorbeugende Wartungsaufträge auf Grundlage der Wartungsplantypen „Zeit“ oder „Zähler“.</span><span class="sxs-lookup"><span data-stu-id="c952f-110">Preventive maintenance jobs based on maintenance plan types "Time" or "Counter".</span></span>                       |
| <span data-ttu-id="c952f-111">Wartungsdurchgänge</span><span class="sxs-lookup"><span data-stu-id="c952f-111">Maintenance rounds</span></span>    | <span data-ttu-id="c952f-112">Vorbeugende Wartungsaufträge, die mehrere Anlagen enthalten, die einen ähnlichen Wartungstyp erfordern.</span><span class="sxs-lookup"><span data-stu-id="c952f-112">Preventive maintenance jobs containing several assets that require a similar type of maintenance.</span></span>           |
| <span data-ttu-id="c952f-113">Wartungsanfrage</span><span class="sxs-lookup"><span data-stu-id="c952f-113">Maintenance request</span></span>   | <span data-ttu-id="c952f-114">Manuell erstellte Anforderung für die Wartung oder Reparatur einer Anlage, die in einen Arbeitsauftrag konvertiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="c952f-114">Manually created request for maintenance or repair of an asset, which can be converted into a work order.</span></span> |


1. <span data-ttu-id="c952f-115">Klicken Sie auf **Anlagenverwaltung** > **Allgemein** > **Alle Wartungspläne** oder **Wartungszeitplanpositionen öffnen** oder **Wartungszeitplanpools öffnen**.</span><span class="sxs-lookup"><span data-stu-id="c952f-115">Click **Asset management** > **Common** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools**.</span></span>

2. <span data-ttu-id="c952f-116">Wählen Sie die geplanten Wartungsaufträge aus, für die Sie einen Arbeitsauftrag erstellen möchten, und klicken Sie auf **Arbeitsauftrag**.</span><span class="sxs-lookup"><span data-stu-id="c952f-116">Select the scheduled maintenance jobs for which you want to create a work order and click **Work order**.</span></span> <span data-ttu-id="c952f-117">Die Gesamtanzahl von Planungsstunden für die ausgewählten Positionen wird im Feld **Wartungsprognosestunden** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c952f-117">The total number of forecast hours for the selected lines is shown in the **Maintenance forecast hours** field.</span></span>

3. <span data-ttu-id="c952f-118">Im Abschnitt **Parameter** wählen Sie aus, wie viele Arbeitsaufträge erstellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c952f-118">In the **Parameters** section, select how many work orders should be created.</span></span> <span data-ttu-id="c952f-119">Sie können einen Arbeitsauftrag pro Wartungszeitplanposition oder mehrere Arbeitsaufträge basierend auf Ihrer Auswahl im Abschnitt **Ein Arbeitsauftrag pro** erstellen.</span><span class="sxs-lookup"><span data-stu-id="c952f-119">You can create one work order per maintenance schedule line, or a number of work orders based on your selections in the **One work order per** section.</span></span>

4. <span data-ttu-id="c952f-120">Wählen Sie einen **Arbeitsauftragstyp** aus, der für alle Arbeitsaufträge verwendet wird, die Sie erstellen.</span><span class="sxs-lookup"><span data-stu-id="c952f-120">Select a **Work order type** that will be used on all the work orders you create.</span></span>

5. <span data-ttu-id="c952f-121">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="c952f-121">Click **OK**.</span></span> <span data-ttu-id="c952f-122">Einer oder mehrere Arbeitsaufträge werden erstellt.</span><span class="sxs-lookup"><span data-stu-id="c952f-122">One or more work orders are created.</span></span>

![Abbildung 1](media/18-preventive-maintenance.png)

