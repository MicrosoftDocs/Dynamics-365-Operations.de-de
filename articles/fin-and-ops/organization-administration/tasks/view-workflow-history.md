---
title: Anzeigen der Workflowhistorie
description: In diesem Thema werden die Schritte beschrieben, um den Status eines Dokuments anzuzeigen, das zur Verarbeitung und Genehmigung an das Workflowsystem übermittelt wurde.
author: jasongre
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowStatus
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 16c6594161f1fecd36183a6b8f2c798f52d70a9c
ms.sourcegitcommit: 81e6eaa2178fda7f7d086ad978f4c891bc4ec10a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/10/2019
ms.locfileid: "1738787"
---
# <a name="view-workflow-history"></a><span data-ttu-id="a8b0e-103">Anzeigen der Workflowhistorie</span><span class="sxs-lookup"><span data-stu-id="a8b0e-103">View workflow history</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a8b0e-104">In diesem Thema werden die Schritte beschrieben, um den Status eines Dokuments anzuzeigen, das zur Verarbeitung und Genehmigung an das Workflowsystem übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="a8b0e-104">This topic describes the steps to view the status of a document that was submitted to the workflow system for processing and approval.</span></span> <span data-ttu-id="a8b0e-105">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="a8b0e-105">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="a8b0e-106">Wechseln Sie zu **Navigationsbereich > Module > Allgemein > Abfragen > Workflow > Workflowhistorie**.</span><span class="sxs-lookup"><span data-stu-id="a8b0e-106">Go to **Navigation pane > Modules > Common > Inquiries > Workflow > Workflow history**.</span></span>
    - <span data-ttu-id="a8b0e-107">Mithilfe dieses Formulars können Sie den Status eines Dokuments anzeigen, das zur Verarbeitung und Genehmigung an das Workflowsystem übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="a8b0e-107">Use this form to view the status of a document that was submitted to the workflow system for processing and approval.</span></span>  
    - <span data-ttu-id="a8b0e-108">Die **Instanzkennung** ist der Kennungscode der Workflowinstanz, mit der das Dokument verarbeitet wird oder verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="a8b0e-108">The **Instance ID** is the identification code of the workflow instance that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="a8b0e-109">Der **Status** ist der Workflowstatus des Dokuments.</span><span class="sxs-lookup"><span data-stu-id="a8b0e-109">The **Status** is the workflow status of the document.</span></span>  
    - <span data-ttu-id="a8b0e-110">Die **Workflowkennung** ist der Kennungscode des Workflows, mit dem das Dokument verarbeitet wird oder verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="a8b0e-110">The **Workflow ID** is the identification code of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="a8b0e-111">Das **Dokument** ist der Kennungscode des Dokuments.</span><span class="sxs-lookup"><span data-stu-id="a8b0e-111">The **Document** is the identification code of the document.</span></span>  
    - <span data-ttu-id="a8b0e-112">Der **Dokumenttyp** ist der Typ des Dokuments, das zur Verarbeitung übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="a8b0e-112">The **Document type** is the type of document that was submitted for processing.</span></span>  
    - <span data-ttu-id="a8b0e-113">Der **Workflow** ist der Name des Workflows, mit dem das Dokument verarbeitet wird oder wurde.</span><span class="sxs-lookup"><span data-stu-id="a8b0e-113">The **Workflow** is the name of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="a8b0e-114">Die **Version** ist die Versionsnummer des Workflows, mit dem das Dokument verarbeitet wird oder verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="a8b0e-114">The **Version** is the version number of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="a8b0e-115">Das **Erstellungsdatum und -uhrzeit** ist das Datum und die Uhrzeit, an dem das Dokument übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="a8b0e-115">The **Created date and time** is the date and time that the document was submitted.</span></span>  
    - <span data-ttu-id="a8b0e-116">Die **Verstrichene Zeit** ist die seit der Übermittlung des Dokuments verstrichene Zeit.</span><span class="sxs-lookup"><span data-stu-id="a8b0e-116">The **Elapsed time** is the time that has passed since the document was submitted.</span></span>  
    - <span data-ttu-id="a8b0e-117">Mit der Schaltfläche **Fortsetzen** können Sie den Workflowprozess für das ausgewählte Dokument fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="a8b0e-117">The **Resume** button allows you to resume the workflow process for the selected document.</span></span>  
    - <span data-ttu-id="a8b0e-118">Mit der Schaltfläche **Rückruf** können Sie das ausgewählte Dokument zurückrufen, sodass es nicht verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="a8b0e-118">The **Recall** button allows you to recall the selected document so that it is not processed.</span></span>   
2. <span data-ttu-id="a8b0e-119">Wählen Sie in der Liste den Link in der gewünschten Zeile aus.</span><span class="sxs-lookup"><span data-stu-id="a8b0e-119">In the list, select the link in the desired row.</span></span>
    - <span data-ttu-id="a8b0e-120">Stellen Sie sicher, dass der Bereich **Arbeitsaufgaben** erweitert ist.</span><span class="sxs-lookup"><span data-stu-id="a8b0e-120">Make sure the **Work items** section is expanded.</span></span> <span data-ttu-id="a8b0e-121">In diesem Abschnitt können Sie die Arbeitsaufgaben anzeigen, die dem ausgewählten Dokument zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a8b0e-121">In this section you can view the work items that are associated with the selected document.</span></span> <span data-ttu-id="a8b0e-122">So muss eine Aufgabe möglicherweise abgeschlossen werden oder das Dokument muss möglicherweise genehmigt werden.</span><span class="sxs-lookup"><span data-stu-id="a8b0e-122">For example, a task may have to be completed, or the document may have to be approved.</span></span>  
    - <span data-ttu-id="a8b0e-123">Durch die Schaltfläche **Neu zuweisen** wird ein Dialogfeld geöffnet, in dem Sie eine Arbeitsaufgabe einem anderen Benutzer neu zuordnen können.</span><span class="sxs-lookup"><span data-stu-id="a8b0e-123">The **Reassign** button will open a dialog box where you can reassign a work item to another user.</span></span>  
    - <span data-ttu-id="a8b0e-124">Überprüfen Sie, ob der Bereich **Verfolgungsdetails** erweitert ist.</span><span class="sxs-lookup"><span data-stu-id="a8b0e-124">Make sure the **Tracking details** section is expanded.</span></span> <span data-ttu-id="a8b0e-125">In diesem Abschnitt können Sie die Workflowhistorie des ausgewählten Dokuments angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a8b0e-125">In this section you can view the workflow history of the selected document.</span></span>  

