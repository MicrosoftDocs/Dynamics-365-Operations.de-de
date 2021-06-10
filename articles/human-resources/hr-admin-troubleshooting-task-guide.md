---
title: Aufgabenleitfäden in LCS speichern und erneut wiedergeben
description: In diesem Artikel wird erläutert, wie Aufgabenleitfäden in Microsoft Dynamics Lifecycle Services (LCS) gespeichert und dann wiedergegeben werden.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8a18bb14ba8c3c926065c97b0ee26c38ee86ded2
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053274"
---
# <a name="save-task-guides-to-lcs-and-replay-them"></a><span data-ttu-id="96c88-103">Aufgabenleitfäden in LCS speichern und erneut wiedergeben</span><span class="sxs-lookup"><span data-stu-id="96c88-103">Save task guides to LCS and replay them</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="96c88-104">**Umgebungsdetails**</span><span class="sxs-lookup"><span data-stu-id="96c88-104">**Environment details**</span></span> 

<span data-ttu-id="96c88-105">Microsoft Dynamics 365 Human Resources, das über Microsoft Dynamics Lifecycle Services (LCS) bereitgestellt wurde</span><span class="sxs-lookup"><span data-stu-id="96c88-105">Microsoft Dynamics 365 Human Resources, which was deployed via Microsoft Dynamics Lifecycle Services (LCS)</span></span>

<span data-ttu-id="96c88-106">**Abgang**</span><span class="sxs-lookup"><span data-stu-id="96c88-106">**Issue**</span></span>

<span data-ttu-id="96c88-107">Kunden möchte neue Aufgabenaufzeichnungen im LCS-Projekt speichern und dann die gespeicherten Aufgabenleitfäden wiedergeben.</span><span class="sxs-lookup"><span data-stu-id="96c88-107">The customer wants to save new task recordings to the LCS project, and then replay the saved task guides.</span></span>

<span data-ttu-id="96c88-108">**Lösung**</span><span class="sxs-lookup"><span data-stu-id="96c88-108">**Resolution**</span></span>

<span data-ttu-id="96c88-109">Folgen Sie diesen Schritten, um eine Aufgabenaufzeichnung in LCS zu speichern.</span><span class="sxs-lookup"><span data-stu-id="96c88-109">Follow these steps to save a task recording to LCS.</span></span>

1. <span data-ttu-id="96c88-110">Melden Sie sich bei LCS an, und wählen Sie das Projekt aus.</span><span class="sxs-lookup"><span data-stu-id="96c88-110">Sign in to LCS, and select the project.</span></span>
2. <span data-ttu-id="96c88-111">Wählen Sie die Kachel **Geschäftsprozessmodellierer** aus.</span><span class="sxs-lookup"><span data-stu-id="96c88-111">Select the **Business process modeler** tile.</span></span>
3. <span data-ttu-id="96c88-112">Zeigen Sie die Seite in der „Aktualisierte BPM-Benutzeroberfläche” an.</span><span class="sxs-lookup"><span data-stu-id="96c88-112">View the page in the "Updated BPM experience."</span></span>
4. <span data-ttu-id="96c88-113">Wählen Sie eine Bibliothek aus, und wählen Sie dann **Kopieren** aus.</span><span class="sxs-lookup"><span data-stu-id="96c88-113">Select a library, and then select **Copy**.</span></span>
5. <span data-ttu-id="96c88-114">Geben Sie einen Namen für das Modell des Geschäftsprozessmodellierers (BPM) an.</span><span class="sxs-lookup"><span data-stu-id="96c88-114">Enter a name for the Business process modeler (BPM) model.</span></span>
6. <span data-ttu-id="96c88-115">Melden Sie sich bei Human Resources von LCS an.</span><span class="sxs-lookup"><span data-stu-id="96c88-115">Sign in to Human Resources from LCS.</span></span>
7. <span data-ttu-id="96c88-116">Geben Sie im Feld **Suche** den Text **Hilfe** ein.</span><span class="sxs-lookup"><span data-stu-id="96c88-116">In the **Search** field, enter **help**.</span></span> <span data-ttu-id="96c88-117">Lifecycle Services-Hilfe wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="96c88-117">Lifecycle Services Help is opened.</span></span>
8. <span data-ttu-id="96c88-118">Wählen Sie die Schaltfläche **Aktualisieren** für die Konfiguration der Lifecycle Services-Hilfe aus.</span><span class="sxs-lookup"><span data-stu-id="96c88-118">Select the **Refresh** button for Lifecycle Services Help configuration.</span></span>

    <span data-ttu-id="96c88-119">Ihre neue BPM-Bibliothek sollte angezeigt werden und aktiv sein.</span><span class="sxs-lookup"><span data-stu-id="96c88-119">Your new BPM library should appear, and it should be active.</span></span>

9. <span data-ttu-id="96c88-120">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="96c88-120">Close the page.</span></span>
10. <span data-ttu-id="96c88-121">Erstellen Sie eine Aufgabenaufzeichnung.</span><span class="sxs-lookup"><span data-stu-id="96c88-121">Create a task recording.</span></span>
11. <span data-ttu-id="96c88-122">Wenn Sie fertig sind, wählen Sie **In Lifecycle Services speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="96c88-122">When you've finished, select **Save to Lifecycle Services**.</span></span>

    ![In Lifecycle Services speichern](media/task-guides.png)

12. <span data-ttu-id="96c88-124">Wählen Sie die BPM-Bibliothek und -Knoten aus, um der Aufgabenaufzeichnung zu speichern.</span><span class="sxs-lookup"><span data-stu-id="96c88-124">Select the BPM library and node to save the task recording to.</span></span>

<span data-ttu-id="96c88-125">Gehen Sie folgendermaßen vor, um einen Aufgabenleitfaden von LCS wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="96c88-125">Follow these steps to replay a task guide from LCS.</span></span>

1. <span data-ttu-id="96c88-126">Starten Sie die Aufgabenaufzeichnung.</span><span class="sxs-lookup"><span data-stu-id="96c88-126">Start Task recorder.</span></span>
2. <span data-ttu-id="96c88-127">Wählen Sie **Von LCS aus öffnen** aus.</span><span class="sxs-lookup"><span data-stu-id="96c88-127">Select **Open from LCS**.</span></span>
3. <span data-ttu-id="96c88-128">Wählen Sie die Bibliothek und den BPM-Knoten aus, die den gespeicherten Aufgabenleitfaden haben.</span><span class="sxs-lookup"><span data-stu-id="96c88-128">Select the library and the BPM node that have the saved task guide.</span></span>
4. <span data-ttu-id="96c88-129">Öffnen Sie den Aufgabenleitfaden.</span><span class="sxs-lookup"><span data-stu-id="96c88-129">Open the task guide.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]