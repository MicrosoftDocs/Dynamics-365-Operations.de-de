---
title: Arbeitsauftrag disponieren
description: In diesem Thema wird erläutert, wie ein Arbeitsauftrag in der Anlagenverwaltung disponiert wird.
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
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
ms.openlocfilehash: 3b1621cf0f1e47d7bd5fe2fa0b41fbcd61f14def
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887204"
---
# <a name="dispatch-work-order"></a><span data-ttu-id="9f099-103">Arbeitsauftrag disponieren</span><span class="sxs-lookup"><span data-stu-id="9f099-103">Dispatch work order</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="9f099-104">Sie können einen Arbeitsauftrag oder Arbeitsauftragseinzelvorgänge für eine Arbeitskraft einplanen, indem Sie die Funktion **Disponieren** verwenden.</span><span class="sxs-lookup"><span data-stu-id="9f099-104">You can schedule one work order or work order jobs to one worker using the **Dispatch** functionality.</span></span>

1. <span data-ttu-id="9f099-105">Klicken Sie auf **Anlagenverwaltung** > **Allgemein** > **Arbeitsaufträge** > **Alle Arbeitsaufträge** oder **Aktive Arbeitsaufträge**.</span><span class="sxs-lookup"><span data-stu-id="9f099-105">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="9f099-106">Wählen Sie den Arbeitsauftrag in der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="9f099-106">Select the work order in the list.</span></span>

3. <span data-ttu-id="9f099-107">Klicken Sie auf der Registerkarte **Allgemeines** auf **Disponieren**.</span><span class="sxs-lookup"><span data-stu-id="9f099-107">On the **General** tab, click **Dispatch**.</span></span>

4. <span data-ttu-id="9f099-108">Wählen Sie im Dialogfeld **Arbeitsauftrag planen** die Arbeitskraft im Feld **Arbeitskraft** aus.</span><span class="sxs-lookup"><span data-stu-id="9f099-108">n the **Schedule work order** dialog, select the worker in the **Worker** field.</span></span>

5. <span data-ttu-id="9f099-109">Im Feld **Stunden planen** können Sie erwartete Arbeitsstunden einfügen, falls sich die erwarteten Arbeitsstunden von den Planungsstunden unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="9f099-109">In the **Schedule hours** field, you can insert expected work hours in case expected work hours differ from forecast hours.</span></span>

6. <span data-ttu-id="9f099-110">Im Feld **Geplanter Start** können Sie Startdatum und -uhrzeit bearbeiten, nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="9f099-110">In the **Scheduled start** field, you can edit start date and time, if required.</span></span>

7. <span data-ttu-id="9f099-111">Soll der Planungsprozess die Kapazitätseinschränkungen zu Ressourcen, die bereits für andere Einzelvorgänge geplant sind, berücksichtigen, überprüfen Sie, ob die Umschaltschaltflächen **Anlage**, **Werkzeug** und **Arbeitskraft** auf „Ja“ festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="9f099-111">If the scheduling process should observe capacity limitations regarding resources already scheduled on other jobs, make sure that the **Asset**, **Tool**, and **Worker** toggle buttons are set to "Yes".</span></span> <span data-ttu-id="9f099-112">Wenn ausführliche Informationen zum Planungsprozess angezeigt werden sollen, wählen Sie „Ja“ bei der Umschaltschaltfläche **Ausführlich** aus.</span><span class="sxs-lookup"><span data-stu-id="9f099-112">If you want to see detailed information about the scheduling process, select "Yes" on the **Verbose** toggle button.</span></span> <span data-ttu-id="9f099-113">Das bedeutet, dass detaillierte Informationen zu den kalkulierten Bewertungen für den Arbeitsauftrag im Infolog angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="9f099-113">This means detailed information about the calculated scores on the work order is shown in the Infolog.</span></span>

8. <span data-ttu-id="9f099-114">Wählen Sie „Ja“ bei der Umschaltschaltfläche **Planung ignorieren** aus, um abgeschlossene Tage im Kalender zu ignorieren (gilt für Anlage, Arbeitskraft und Tools).</span><span class="sxs-lookup"><span data-stu-id="9f099-114">Select "Yes" on the **Ignore schedule** toggle button to ignore closed days in the calendar (applies to asset, worker, and tools).</span></span> <span data-ttu-id="9f099-115">Wählen Sie „Ja“ bei der Umschaltschaltfläche **Geplante Ausführung ignorieren** aus, um Einschränkungen zu ignorieren, die für den Arbeitsauftrag im Zusammenhang mit der Planung ggf. ausgewählt wurden.</span><span class="sxs-lookup"><span data-stu-id="9f099-115">Select "Yes" on the **Ignore scheduled execution** toggle button to ignore limitations that may have been selected on the work order regarding scheduling.</span></span> <span data-ttu-id="9f099-116">Der [Geplante Ausführung](../setup-for-work-orders/scheduled-execution.md)-Abschnitt enthält Informationen zu den Einstellungen der geplanten Ausführung.</span><span class="sxs-lookup"><span data-stu-id="9f099-116">Refer to the [Scheduled execution](../setup-for-work-orders/scheduled-execution.md) section for information on the setup of scheduled execution.</span></span>

9. <span data-ttu-id="9f099-117">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="9f099-117">Click **OK**.</span></span> <span data-ttu-id="9f099-118">Der Arbeitsauftragslebenszyklusstatus wird automatisch zum „Geplant“-Lebenszyklusstatus angegebenen **Anlagenverwaltung** > **Einstellungen** > **Arbeitsaufträge** > **Lebenszyklusmodelle** aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="9f099-118">The work order lifecycle state is automatically updated to the "Scheduled" lifecycle state specified **Asset management** > **Setup** > **Work orders** > **Lifecycle models**.</span></span>

<span data-ttu-id="9f099-119">Die folgende Abbildung zeigt ein Beispiel der Versandmöglichkeiten im Dialogfeld **Arbeitsauftrag planen** an.</span><span class="sxs-lookup"><span data-stu-id="9f099-119">The figure below shows an example of dispatch selections in the **Schedule work order** dialog.</span></span>

![Abbildung 1](media/04-work-order-scheduling.png)

>[!NOTE]
><span data-ttu-id="9f099-121">Wenn Sie die Planung für einen Arbeitsauftrag löschen möchten, wählen Sie den Arbeitsauftrag in **Alle Arbeitsaufträge** aus und klicken Sie auf **Zeitplan löschen** in der Registerkarte **Allgemein**. Denken Sie daran, den Arbeitsauftragslebenszyklusstatus manuell zu aktualisieren, wenn Sie den Zeitplan löschen.</span><span class="sxs-lookup"><span data-stu-id="9f099-121">If you want to delete the schedule on a work order, this is done by selecting the work order in **All work orders** and clicking **Delete schedule** on the **General** tab. Remember to manually update the work order lifecycle state if you delete the schedule.</span></span>
