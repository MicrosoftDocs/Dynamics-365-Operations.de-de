---
title: Erstellen von Arbeitsaufträgen
description: In diesem Thema wird erläutert, wie Sie Arbeitsaufträge in der Anlagenverwaltung erstellen.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f94f8bc20753e38ce1cb6eccdfbc85c2e491ffad
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428743"
---
# <a name="creating-work-orders"></a><span data-ttu-id="335ab-103">Erstellen von Arbeitsaufträgen</span><span class="sxs-lookup"><span data-stu-id="335ab-103">Creating work orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="335ab-104">Wenn Sie vorbeugende Wartungsaufträge geplant haben, ist der nächste Schritt, Arbeitsaufträge für die Einzelvorgänge zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="335ab-104">When you have scheduled preventive maintenance jobs, next step is to create work orders for the jobs.</span></span> <span data-ttu-id="335ab-105">Dies erfolgt in einem der Wartungszeitpläne.</span><span class="sxs-lookup"><span data-stu-id="335ab-105">This is done in one of the maintenance schedules.</span></span> <span data-ttu-id="335ab-106">Die geplanten Einzelvorgänge in einem Wartungszeitplan können verschiedene Referenztypen haben:</span><span class="sxs-lookup"><span data-stu-id="335ab-106">The scheduled jobs in a maintenance schedule can have different reference types:</span></span>

| <span data-ttu-id="335ab-107">Referenztyp</span><span class="sxs-lookup"><span data-stu-id="335ab-107">Reference type</span></span> | <span data-ttu-id="335ab-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="335ab-108">Description</span></span>                    |
|-----------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="335ab-109">Wartungspläne</span><span class="sxs-lookup"><span data-stu-id="335ab-109">Maintenance plans</span></span>     | <span data-ttu-id="335ab-110">Vorbeugende Wartungsaufträge auf Grundlage der Wartungsplantypen „Zeit“ oder „Zähler“.</span><span class="sxs-lookup"><span data-stu-id="335ab-110">Preventive maintenance jobs based on maintenance plan types "Time" or "Counter".</span></span>                       |
| <span data-ttu-id="335ab-111">Wartungsdurchgänge</span><span class="sxs-lookup"><span data-stu-id="335ab-111">Maintenance rounds</span></span>    | <span data-ttu-id="335ab-112">Vorbeugende Wartungsaufträge, die mehrere Anlagen enthalten, die einen ähnlichen Wartungstyp erfordern.</span><span class="sxs-lookup"><span data-stu-id="335ab-112">Preventive maintenance jobs containing several assets that require a similar type of maintenance.</span></span>           |
| <span data-ttu-id="335ab-113">Wartungsanfrage</span><span class="sxs-lookup"><span data-stu-id="335ab-113">Maintenance request</span></span>   | <span data-ttu-id="335ab-114">Manuell erstellte Anforderung für die Wartung oder Reparatur einer Anlage, die in einen Arbeitsauftrag konvertiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="335ab-114">Manually created request for maintenance or repair of an asset, which can be converted into a work order.</span></span> |


1. <span data-ttu-id="335ab-115">Klicken Sie auf **Anlagenverwaltung** > **Allgemein** > **Alle Wartungspläne** oder **Wartungszeitplanpositionen öffnen** oder **Wartungszeitplanpools öffnen**.</span><span class="sxs-lookup"><span data-stu-id="335ab-115">Click **Asset management** > **Common** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools**.</span></span>

2. <span data-ttu-id="335ab-116">Wählen Sie die geplanten Wartungsaufträge aus, für die Sie einen Arbeitsauftrag erstellen möchten, und klicken Sie auf **Arbeitsauftrag**.</span><span class="sxs-lookup"><span data-stu-id="335ab-116">Select the scheduled maintenance jobs for which you want to create a work order and click **Work order**.</span></span> <span data-ttu-id="335ab-117">Im Dialog **Arbeitsaufträge erstellen** wird die Gesamtanzahl von Planungsstunden für die ausgewählten Positionen im Feld **Wartungsprognosestunden** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="335ab-117">In the **Create work orders** dialog, the total number of forecast hours for the selected lines is shown in the **Maintenance forecast hours** field.</span></span>

3. <span data-ttu-id="335ab-118">Im Abschnitt **Parameter** wählen Sie aus, wie viele Arbeitsaufträge erstellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="335ab-118">In the **Parameters** section, select how many work orders should be created.</span></span> <span data-ttu-id="335ab-119">Sie können einen Arbeitsauftrag pro Wartungszeitplanposition oder mehrere Arbeitsaufträge basierend auf Ihrer Auswahl im Abschnitt **Ein Arbeitsauftrag pro** erstellen.</span><span class="sxs-lookup"><span data-stu-id="335ab-119">You can create one work order per maintenance schedule line, or a number of work orders based on your selections in the **One work order per** section.</span></span>

4. <span data-ttu-id="335ab-120">Wählen Sie einen **Arbeitsauftragstyp** aus, der für alle Arbeitsaufträge verwendet wird, die Sie erstellen.</span><span class="sxs-lookup"><span data-stu-id="335ab-120">Select a **Work order type** that will be used on all the work orders you create.</span></span> <span data-ttu-id="335ab-121">In der folgenden Abbildung wird ein Beispiel des Dialogfelds **Arbeitsaufträge erstellen** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="335ab-121">The illustration below shows an example of the **Create work orders** dialog.</span></span>

![Abbildung 1](media/18-preventive-maintenance.png)

5. <span data-ttu-id="335ab-123">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="335ab-123">Click **OK**.</span></span> <span data-ttu-id="335ab-124">Einer oder mehrere Arbeitsaufträge werden erstellt.</span><span class="sxs-lookup"><span data-stu-id="335ab-124">One or more work orders are created.</span></span>

