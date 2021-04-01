---
title: Leasinggenehmigungs-Workflows einrichten
description: In diesem Thema wird erläutert, wie Sie einen Genehmigungs-Workflow einrichten, der ausgeführt wird, wenn ein neuer Mietvertrag erstellt wird.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1eaa2f5cc191ec93c30f4f10a662a87e501a341d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249580"
---
# <a name="set-up-lease-approval-workflows"></a><span data-ttu-id="9de68-103">Leasinggenehmigungs-Workflows einrichten</span><span class="sxs-lookup"><span data-stu-id="9de68-103">Set up lease approval workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9de68-104">In diesem Thema wird erläutert, wie Sie einen Genehmigungs-Workflow einrichten, der ausgeführt wird, wenn ein neuer Mietvertrag erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="9de68-104">The topic explains how to set up an approval workflow that will run when a new lease is created.</span></span> <span data-ttu-id="9de68-105">Informationen zum Verwenden des Workflows finden Sie unter [Verwenden von Workflows für die Leasinggenehmigung](use-create-lease-wrkflw.md).</span><span class="sxs-lookup"><span data-stu-id="9de68-105">For information about how to use the workflow, see [Use lease approval workflows](use-create-lease-wrkflw.md).</span></span> 

1. <span data-ttu-id="9de68-106">Wechseln Sie zu **Anlagenleasing \> Einrichtung \> Leasing-Workflow**.</span><span class="sxs-lookup"><span data-stu-id="9de68-106">Go to **Asset leasing \> Setup \> Lease workflow**.</span></span>
2. <span data-ttu-id="9de68-107">Wählen Sie auf der Seite **Leasing-Workflow** die Option **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="9de68-107">On the **Lease workflow** page, select **New**.</span></span>
3. <span data-ttu-id="9de68-108">Im daraufhin angezeigten Dialogfeld unter **Workflow-Typ** wählen Sie die **Leaseing-Workflow**-Verknüpfung aus.</span><span class="sxs-lookup"><span data-stu-id="9de68-108">In the dialog box that appears, under **Workflow type**, select the **Lease workflow** link.</span></span>

    <span data-ttu-id="9de68-109">Die Anwendung wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="9de68-109">The application is opened.</span></span> <span data-ttu-id="9de68-110">Melden Sie sich nach der Ausführung bei Azure Active Directory (Azure AD) an, um zur Workflow-Anwendung weitergeleitet zu werden.</span><span class="sxs-lookup"><span data-stu-id="9de68-110">After it runs, sign in to Azure Active Directory (Azure AD) to be redirected to the workflow application.</span></span>

4. <span data-ttu-id="9de68-111">Ziehen Sie das **Leasing-Workflow-Genehmigung**-Element in den Workflow.</span><span class="sxs-lookup"><span data-stu-id="9de68-111">Drag the **Lease workflow approval** element onto the workflow.</span></span>
5. <span data-ttu-id="9de68-112">Verbinden Sie einen Knoten von **Start** mit **Leasing-Workflow-Genehmigung**.</span><span class="sxs-lookup"><span data-stu-id="9de68-112">Connect one node from **Start** to **Lease workflow approval**.</span></span> <span data-ttu-id="9de68-113">Verbinden Sie dann **Leasing-Workflow-Genehmigung** mit **Ende**.</span><span class="sxs-lookup"><span data-stu-id="9de68-113">Then connect **Lease workflow approval** to **End**.</span></span>
6. <span data-ttu-id="9de68-114">Klicken Sie zweimal auf **Leasing-Workflow-Genehmigung**.</span><span class="sxs-lookup"><span data-stu-id="9de68-114">Double-click **Lease workflow approval**.</span></span>
7. <span data-ttu-id="9de68-115">Wählen Sie **Eigenschaften** und geben Sie dann unter **Grundeinstellungen** einen Namen für den Workflow ein.</span><span class="sxs-lookup"><span data-stu-id="9de68-115">Select **Properties**, and then, under **Basic settings**, enter a name for the workflow.</span></span>

    <span data-ttu-id="9de68-116">Auf dieser Seite können Sie auch weitere Parameter für den Workflow festlegen.</span><span class="sxs-lookup"><span data-stu-id="9de68-116">On this page, you can also set more parameters for the workflow.</span></span> <span data-ttu-id="9de68-117">Wenn Sie **Automatische Aktionen** eingeschaltet haben, ergreift das System automatisch eine bestimmte Aktion.</span><span class="sxs-lookup"><span data-stu-id="9de68-117">If you've turned on **Automatic actions**, the system will automatically take a specific action.</span></span> <span data-ttu-id="9de68-118">Benachrichtigungen können gesendet werden, wenn sie auf der Registerkarte **Benachrichtigungen** angegeben sind. Auf der Registerkarte **Erweiterte Einstellungen** können Sie eine endgültige genehmigende Person angeben, ein Zeitlimit festlegen und bestimmte Aktionen festlegen, die ausgeführt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="9de68-118">Notifications can be sent if they are specified on the **Notifications** tab. On the **Advanced settings** tab, you can specify a final approver, set a time limit, and designate specific actions that must be completed.</span></span>

8. <span data-ttu-id="9de68-119">Wenn Sie die Workflow-Parameter eingestellt haben, wählen Sie **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="9de68-119">When you've finished setting the workflow parameters, select **Close**.</span></span>
9. <span data-ttu-id="9de68-120">Wählen Sie **Schritt 1** und dann **Eigenschaften** aus.</span><span class="sxs-lookup"><span data-stu-id="9de68-120">Select **Step 1**, and then select **Properties**.</span></span>
10. <span data-ttu-id="9de68-121">Geben Sie unter **Grundeinstellungen** einen Namen für den Schritt ein, erstellen Sie eine Betreffzeile für die Genehmigung und geben Sie Anweisungen für die Genehmigung an.</span><span class="sxs-lookup"><span data-stu-id="9de68-121">Under **Basic settings**, enter a name for the step, create a subject line for the approval, and specify instructions for the approval.</span></span>
11. <span data-ttu-id="9de68-122">Auf der **Zuweisung**-Seite wählen Sie den Zuweisungstyp aus.</span><span class="sxs-lookup"><span data-stu-id="9de68-122">On the **Assignment** page, select the assignment type.</span></span>
12. <span data-ttu-id="9de68-123">Um der Genehmigung bestimmte Benutzer zuzuweisen, wählen Sie **Benutzer** aus, wählen Sie die Benutzer aus, die Mietverträge genehmigen, und wählen Sie dann **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="9de68-123">To assign specific users to the approval, select **User**, select the users who approve leases, and then select **Close**.</span></span>
13. <span data-ttu-id="9de68-124">Wählen Sie **Speichern und schließen**, um den Workflow zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9de68-124">Select **Save and close** to create the workflow.</span></span> <span data-ttu-id="9de68-125">Wenn Sie dazu aufgefordert werden, wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="9de68-125">Then, when you're prompted, select **OK**.</span></span>
14. <span data-ttu-id="9de68-126">Wählen Sie auf der Seite **Workflow erstellen** die Option **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="9de68-126">On the **Create workflow** page, select **Close**.</span></span>
14. <span data-ttu-id="9de68-127">Wählen Sie den neuen Workflow aus und wählen Sie dann **Versionen**.</span><span class="sxs-lookup"><span data-stu-id="9de68-127">Select the new workflow, and then select **Versions**.</span></span> <span data-ttu-id="9de68-128">Wählen Sie dann **Aktivieren**, um sicherzustellen, dass der Workflow aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="9de68-128">Then select **Make active** to ensure that the workflow is active.</span></span>
15. <span data-ttu-id="9de68-129">Wählen Sie **Schließen** aus.</span><span class="sxs-lookup"><span data-stu-id="9de68-129">Select **Close**.</span></span> <span data-ttu-id="9de68-130">Die neue aktive Version wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9de68-130">The new active version appears.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]