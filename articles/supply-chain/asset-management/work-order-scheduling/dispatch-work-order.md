---
title: Arbeitsauftrag disponieren
description: In diesem Thema wird erläutert, wie ein Arbeitsauftrag in der Anlagenverwaltung disponiert wird.
author: josaw1
manager: tfehr
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetScheduledExecution
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6b4b05dfe351bb61dc47c9c2bfe30831ab7b0a16
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/16/2021
ms.locfileid: "5016855"
---
# <a name="dispatch-work-order"></a><span data-ttu-id="99657-103">Arbeitsauftrag disponieren</span><span class="sxs-lookup"><span data-stu-id="99657-103">Dispatch work order</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="99657-104">Sie können einen Arbeitsauftrag oder Arbeitsauftragseinzelvorgänge für eine Arbeitskraft einplanen, indem Sie die Funktion **Disponieren** verwenden.</span><span class="sxs-lookup"><span data-stu-id="99657-104">You can schedule one work order or work order jobs to one worker using the **Dispatch** functionality.</span></span>

1. <span data-ttu-id="99657-105">Klicken Sie auf **Anlagenverwaltung** > **Allgemein** > **Arbeitsaufträge** > **Alle Arbeitsaufträge** oder **Aktive Arbeitsaufträge**.</span><span class="sxs-lookup"><span data-stu-id="99657-105">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="99657-106">Wählen Sie den Arbeitsauftrag in der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="99657-106">Select the work order in the list.</span></span>

3. <span data-ttu-id="99657-107">Klicken Sie auf der Registerkarte **Allgemeines** auf **Disponieren**.</span><span class="sxs-lookup"><span data-stu-id="99657-107">On the **General** tab, click **Dispatch**.</span></span>

4. <span data-ttu-id="99657-108">Wählen Sie im Dialogfeld **Arbeitsauftrag planen** die Arbeitskraft im Feld **Arbeitskraft** aus.</span><span class="sxs-lookup"><span data-stu-id="99657-108">In the **Schedule work order** dialog, select the worker in the **Worker** field.</span></span>

5. <span data-ttu-id="99657-109">Im Feld **Stunden planen** können Sie erwartete Arbeitsstunden einfügen, falls sich die erwarteten Arbeitsstunden von den Planungsstunden unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="99657-109">In the **Schedule hours** field, you can insert expected work hours in case expected work hours differ from forecast hours.</span></span>

6. <span data-ttu-id="99657-110">Im Feld **Geplanter Start** können Sie Startdatum und -uhrzeit bearbeiten, nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="99657-110">In the **Scheduled start** field, you can edit start date and time, if required.</span></span>

7. <span data-ttu-id="99657-111">Soll der Planungsprozess die Kapazitätseinschränkungen zu Ressourcen, die bereits für andere Einzelvorgänge geplant sind, berücksichtigen, überprüfen Sie, ob die Umschaltschaltflächen **Anlage**, **Werkzeug** und **Arbeitskraft** auf **Ja** festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="99657-111">If the scheduling process should observe capacity limitations regarding resources already scheduled on other jobs, make sure that the **Asset**, **Tool**, and **Worker** toggle buttons are set to **Yes**.</span></span> <span data-ttu-id="99657-112">Wenn ausführliche Informationen zum Planungsprozess angezeigt werden sollen, wählen Sie **Ja** bei der Umschaltschaltfläche **Ausführlich** aus.</span><span class="sxs-lookup"><span data-stu-id="99657-112">If you want to see detailed information about the scheduling process, select **Yes** on the **Verbose** toggle button.</span></span> <span data-ttu-id="99657-113">Das bedeutet, dass detaillierte Informationen zu den kalkulierten Bewertungen für den Arbeitsauftrag im Infolog angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="99657-113">This means detailed information about the calculated scores on the work order is shown in the Infolog.</span></span>

8. <span data-ttu-id="99657-114">Wählen Sie **Ja** bei der Umschaltschaltfläche **Planung ignorieren** aus, um abgeschlossene Tage im Kalender zu ignorieren (gilt für Anlage, Arbeitskraft und Tools).</span><span class="sxs-lookup"><span data-stu-id="99657-114">Select **Yes** on the **Ignore schedule** toggle button to ignore closed days in the calendar (applies to asset, worker, and tools).</span></span> <span data-ttu-id="99657-115">Wählen Sie **Ja** bei der Umschaltschaltfläche **Geplante Ausführung ignorieren** aus, um Einschränkungen zu ignorieren, die für den Arbeitsauftrag im Zusammenhang mit der Planung ggf. ausgewählt wurden.</span><span class="sxs-lookup"><span data-stu-id="99657-115">Select **Yes** on the **Ignore scheduled execution** toggle button to ignore limitations that may have been selected on the work order regarding scheduling.</span></span> 

    <span data-ttu-id="99657-116">Der [Geplante Ausführung](../setup-for-work-orders/scheduled-execution.md)-Abschnitt enthält Informationen zu den Einstellungen der geplanten Ausführung.</span><span class="sxs-lookup"><span data-stu-id="99657-116">For information on the setup of scheduled execution, see the [Scheduled execution](../setup-for-work-orders/scheduled-execution.md) section.</span></span>

9. <span data-ttu-id="99657-117">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="99657-117">Click **OK**.</span></span> <span data-ttu-id="99657-118">Der Arbeitsauftragslebenszyklusstatus wird automatisch zum **Geplant**-Lebenszyklusstatus angegebenen **Anlagenverwaltung** > **Einstellungen** > **Arbeitsaufträge** > **Lebenszyklusmodelle**. aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="99657-118">The work order lifecycle state is automatically updated to the **Scheduled** lifecycle state specified **Asset management** > **Setup** > **Work orders** > **Lifecycle models**.</span></span>

<span data-ttu-id="99657-119">Die folgende Abbildung zeigt ein Beispiel der Versandmöglichkeiten im Dialogfeld **Arbeitsauftrag planen** an.</span><span class="sxs-lookup"><span data-stu-id="99657-119">The figure below shows an example of dispatch selections in the **Schedule work order** dialog.</span></span>

![Abbildung 1](media/04-work-order-scheduling.png)

[!NOTE]
<span data-ttu-id="99657-121">Wenn Sie die Planung für einen Arbeitsauftrag löschen möchten, wählen Sie den Arbeitsauftrag in **Alle Arbeitsaufträge** aus und klicken Sie auf **Zeitplan löschen** in der Registerkarte **Allgemein**. Denken Sie daran, den Arbeitsauftragslebenszyklusstatus manuell zu aktualisieren, wenn Sie den Zeitplan löschen.</span><span class="sxs-lookup"><span data-stu-id="99657-121">If you want to delete the schedule on a work order, select the work order in **All work orders**, and then click **Delete schedule** on the **General** tab. Remember to manually update the work order lifecycle state if you delete the schedule.</span></span>

