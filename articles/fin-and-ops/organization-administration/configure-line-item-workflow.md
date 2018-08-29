---
title: Positionsworkflows konfigurieren
description: "In diesem Thema wird erläutert, wie das Positionsworkflowelement konfiguriert wird."
author: sericks007
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195833
ms.assetid: 3237347e-71d5-4569-bc9a-0d0fc9410b78
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: 0a57baa3ecae727721f62477cfc5fa41f60ad06d
ms.contentlocale: de-de
ms.lasthandoff: 08/08/2018

---

# <a name="configure-line-item-workflows"></a><span data-ttu-id="a3b04-103">Positionsworkflows konfigurieren</span><span class="sxs-lookup"><span data-stu-id="a3b04-103">Configure line-item workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a3b04-104">In diesem Thema wird erläutert, wie das Positionsworkflowelement konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="a3b04-104">This topic explains how to configure a line-item workflow element.</span></span>

<span data-ttu-id="a3b04-105">Klicken Sie zum Konfigurieren eines Positionsworkflowelements im Workflow-Editor mit der rechten Maustaste auf das Element, und klicken Sie dann auf **Eigenschaften**, um die Seite **Eigenschaften** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="a3b04-105">To configure a line-item workflow element, in the workflow editor, right-click the element, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="a3b04-106">Verwenden Sie die folgenden Verfahren, um die Eigenschaften des Positionsworkflowelements zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="a3b04-106">Then use the following procedures to configure the properties of the line-item workflow element.</span></span>

## <a name="name-the-line-item-workflow-element"></a><span data-ttu-id="a3b04-107">Benennen des Positionsworkflowelements</span><span class="sxs-lookup"><span data-stu-id="a3b04-107">Name the line-item workflow element</span></span>
<span data-ttu-id="a3b04-108">Gehen Sie folgendermaßen vor, um einen Namen für das Positionsworkflowelement einzugeben.</span><span class="sxs-lookup"><span data-stu-id="a3b04-108">Follow these steps to enter a name for the line-item workflow element.</span></span>

1.  <span data-ttu-id="a3b04-109">Klicken Sie im linken Bereich auf **Grundeinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="a3b04-109">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="a3b04-110">Geben Sie im Feld **Name** einen eindeutigen Namen für das Positionsworkflowelement ein.</span><span class="sxs-lookup"><span data-stu-id="a3b04-110">In the **Name** field, enter a unique name for the line-item workflow element.</span></span>

## <a name="specify-whether-the-same-workflow-is-used-to-process-all-line-items"></a><span data-ttu-id="a3b04-111">Angeben, ob derselbe Workflow zum Verarbeiten aller Positionen verwendet wird</span><span class="sxs-lookup"><span data-stu-id="a3b04-111">Specify whether the same workflow is used to process all line items</span></span>
<span data-ttu-id="a3b04-112">Gehen Sie folgendermaßen vor, um anzugeben, ob derselbe Workflow zum Verarbeiten aller Positionen in einem Dokument verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a3b04-112">Follow these steps to specify whether the same workflow is used to process all the line items on a document.</span></span>

1.  <span data-ttu-id="a3b04-113">Klicken Sie im linken Bereich auf **Grundeinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="a3b04-113">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="a3b04-114">Wird derselbe Workflow zum Verarbeiten aller Positionen in einem Dokument verwendet, klicken Sie **Einzelnen Workflow für alle Positionen aufrufen** auf.</span><span class="sxs-lookup"><span data-stu-id="a3b04-114">If the same workflow should process all the line items on a document, click **Invoke a single workflow for all line-items**.</span></span> <span data-ttu-id="a3b04-115">Wählen Sie anschließend den Workflow zum Verarbeiten der Positionen aus.</span><span class="sxs-lookup"><span data-stu-id="a3b04-115">Then select the workflow to use to process the line items.</span></span>
3.  <span data-ttu-id="a3b04-116">Wenn ein bestimmter Workflow Positionen verarbeiten sollte, die einen bestimmten Satz von Bedingungen erfüllen, klicken Sie auf **Einen Workflow für jede Position aufrufen**.</span><span class="sxs-lookup"><span data-stu-id="a3b04-116">If a specific workflow should process line items that meet a specific set of conditions, click **Invoke a workflow for each line-item**.</span></span> <span data-ttu-id="a3b04-117">Folgen Sie diesen Schritten, um die Bedingungen festzulegen:</span><span class="sxs-lookup"><span data-stu-id="a3b04-117">Then follow these steps to define the set of conditions:</span></span>
    1.  <span data-ttu-id="a3b04-118">Klicken Sie auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="a3b04-118">Click **Add**.</span></span>
    2.  <span data-ttu-id="a3b04-119">Wählen Sie die Bedingung in der Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="a3b04-119">Select the condition in the table.</span></span>
    3.  <span data-ttu-id="a3b04-120">Geben Sie auf der Registerkarte **Bedingungsname** einen Namen für die festzulegenden Bedingungen ein.</span><span class="sxs-lookup"><span data-stu-id="a3b04-120">On the **Condition name** tab, enter a name for the set of conditions that you're defining.</span></span>
    4.  <span data-ttu-id="a3b04-121">Klicken Sie auf **Bedingung hinzufügen**, um die Bedingung einzugeben.</span><span class="sxs-lookup"><span data-stu-id="a3b04-121">Click **Add condition** to enter a condition.</span></span>
    5.  <span data-ttu-id="a3b04-122">Geben Sie alle notwendigen zusätzlichen Bedingungen ein.</span><span class="sxs-lookup"><span data-stu-id="a3b04-122">Enter any additional conditions that are required.</span></span>
    6.  <span data-ttu-id="a3b04-123">Klicken Sie auf **Test**, um zu überprüfen, ob die eingegebenen Bedingungen korrekt konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="a3b04-123">To verify that the set of conditions that you entered is configured correctly, click **Test**.</span></span> <span data-ttu-id="a3b04-124">Auf der Seite **Workflowbedingung testen** im Bereich **Bedingung überprüfen** wählen Sie einen Datensatz aus und klicken auf **Test**.</span><span class="sxs-lookup"><span data-stu-id="a3b04-124">On the **Test workflow condition** page, in the **Validate condition** area, select a record, and then click **Test**.</span></span> <span data-ttu-id="a3b04-125">Der Datensatz wird ausgewertet, um zu bestimmen, ob er den festgelegten Bedingungen entspricht.</span><span class="sxs-lookup"><span data-stu-id="a3b04-125">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span> <span data-ttu-id="a3b04-126">Klicken Sie auf **OK** oder **Abbrechen**, um zur Seite **Eigenschaften** zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="a3b04-126">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

    <span data-ttu-id="a3b04-127">Wählen Sie auf der Registerkarte **Workflow** den Workflow aus, der verwendet werden soll zum Verarbeiten von Positionen, die die definierten Bedingungen erfüllen.</span><span class="sxs-lookup"><span data-stu-id="a3b04-127">On the **Workflow** tab, select the workflow select the workflow to use to process line items that meet the set of conditions that you defined.</span></span>





