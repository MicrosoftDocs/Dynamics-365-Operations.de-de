---
title: Aufgabenleitfäden in LCS speichern und erneut wiedergeben
description: In diesem Thema wird erläutert, wie Aufgabenleitfäden in Microsoft Dynamics Lifecycle Services (LCS) gespeichert und dann wiedergegeben werden.
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 40b4c3154a04a557b8a670e1f1ae3722c71122fe
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "304544"
---
# <a name="save-task-guides-to-lcs-and-replay-them"></a><span data-ttu-id="a20df-103">Aufgabenleitfäden in LCS speichern und erneut wiedergeben</span><span class="sxs-lookup"><span data-stu-id="a20df-103">Save task guides to LCS and replay them</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a20df-104">**Umgebungsdetails**</span><span class="sxs-lookup"><span data-stu-id="a20df-104">**Environment details**</span></span> 

<span data-ttu-id="a20df-105">Microsoft Dynamics 365 for Talent, das über Microsoft Dynamics Lifecycle Services (LCS) bereitgestellt wurde</span><span class="sxs-lookup"><span data-stu-id="a20df-105">Microsoft Dynamics 365 for Talent, which was deployed via Microsoft Dynamics Lifecycle Services (LCS)</span></span>

<span data-ttu-id="a20df-106">**Abgang**</span><span class="sxs-lookup"><span data-stu-id="a20df-106">**Issue**</span></span>

<span data-ttu-id="a20df-107">Der Kunde/die Kundin möchte neue Aufgabenaufzeichnungen in seinem oder ihrem LCS-Projekt speichern und dann die gespeicherten Aufgabenleitfäden wiedergeben.</span><span class="sxs-lookup"><span data-stu-id="a20df-107">The customer wants to save new task recordings to his or her LCS project, and then replay the saved task guides.</span></span>

<span data-ttu-id="a20df-108">**Auflösung**</span><span class="sxs-lookup"><span data-stu-id="a20df-108">**Resolution**</span></span>

<span data-ttu-id="a20df-109">Folgen Sie diesen Schritten, um eine Aufgabenaufzeichnung in LCS zu speichern.</span><span class="sxs-lookup"><span data-stu-id="a20df-109">Follow these steps to save a task recording to LCS.</span></span>

1. <span data-ttu-id="a20df-110">Melden Sie sich bei LCS an, und wählen Sie das Projekt aus.</span><span class="sxs-lookup"><span data-stu-id="a20df-110">Sign in to LCS, and select the project.</span></span>
2. <span data-ttu-id="a20df-111">Wählen Sie die Kachel **Geschäftsprozessmodellierer** aus.</span><span class="sxs-lookup"><span data-stu-id="a20df-111">Select the **Business process modeler** tile.</span></span>
3. <span data-ttu-id="a20df-112">Zeigen Sie die Seite in der „Aktualisierte BPM-Benutzeroberfläche” an.</span><span class="sxs-lookup"><span data-stu-id="a20df-112">View the page in the "Updated BPM experience."</span></span>
4. <span data-ttu-id="a20df-113">Wählen Sie eine Bibliothek aus, und wählen Sie dann **Kopieren** aus.</span><span class="sxs-lookup"><span data-stu-id="a20df-113">Select a library, and then select **Copy**.</span></span>
5. <span data-ttu-id="a20df-114">Geben Sie einen Namen für das Modell des Geschäftsprozessmodellierers (BPM) an.</span><span class="sxs-lookup"><span data-stu-id="a20df-114">Enter a name for the Business process modeler (BPM) model.</span></span>
6. <span data-ttu-id="a20df-115">Melden Sie sich bei Talent von LCS aus an.</span><span class="sxs-lookup"><span data-stu-id="a20df-115">Sign in to Talent from LCS.</span></span>
7. <span data-ttu-id="a20df-116">Geben Sie im Feld **Suche** den Text **Hilfe** ein.</span><span class="sxs-lookup"><span data-stu-id="a20df-116">In the **Search** field, enter **help**.</span></span> <span data-ttu-id="a20df-117">Lifecycle Services-Hilfe wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="a20df-117">Lifecycle Services Help is opened.</span></span>
8. <span data-ttu-id="a20df-118">Wählen Sie die Schaltfläche **Aktualisieren** für die Konfiguration der Lifecycle Services-Hilfe aus.</span><span class="sxs-lookup"><span data-stu-id="a20df-118">Select the **Refresh** button for Lifecycle Services Help configuration.</span></span>

    <span data-ttu-id="a20df-119">Ihre neue BPM-Bibliothek sollte angezeigt werden und aktiv sein.</span><span class="sxs-lookup"><span data-stu-id="a20df-119">Your new BPM library should appear, and it should be active.</span></span>

9. <span data-ttu-id="a20df-120">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="a20df-120">Close the page.</span></span>
10. <span data-ttu-id="a20df-121">Erstellen Sie eine Aufgabenaufzeichnung.</span><span class="sxs-lookup"><span data-stu-id="a20df-121">Create a task recording.</span></span>
11. <span data-ttu-id="a20df-122">Wenn Sie fertig sind, wählen Sie **In Lifecycle Services speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="a20df-122">When you've finished, select **Save to Lifecycle Services**.</span></span>

    ![In Lifecycle Services speichern](media/task-guides.png)

12. <span data-ttu-id="a20df-124">Wählen Sie die BPM-Bibliothek und -Knoten aus, um der Aufgabenaufzeichnung zu speichern.</span><span class="sxs-lookup"><span data-stu-id="a20df-124">Select the BPM library and node to save the task recording to.</span></span>

<span data-ttu-id="a20df-125">Gehen Sie folgendermaßen vor, um einen Aufgabenleitfaden von LCS wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="a20df-125">Follow these steps to replay a task guide from LCS.</span></span>

1. <span data-ttu-id="a20df-126">Starten Sie die Aufgabenaufzeichnung.</span><span class="sxs-lookup"><span data-stu-id="a20df-126">Start Task recorder.</span></span>
2. <span data-ttu-id="a20df-127">Wählen Sie **Von LCS aus öffnen** aus.</span><span class="sxs-lookup"><span data-stu-id="a20df-127">Select **Open from LCS**.</span></span>
3. <span data-ttu-id="a20df-128">Wählen Sie die Bibliothek und den BPM-Knoten aus, die den gespeicherten Aufgabenleitfaden haben.</span><span class="sxs-lookup"><span data-stu-id="a20df-128">Select the library and the BPM node that have the saved task guide.</span></span>
4. <span data-ttu-id="a20df-129">Öffnen Sie den Aufgabenleitfaden.</span><span class="sxs-lookup"><span data-stu-id="a20df-129">Open the task guide.</span></span>
