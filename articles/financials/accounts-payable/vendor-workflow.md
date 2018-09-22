---
title: Lieferantenworkflow
description: "Ändern Sie Kreditordatendaten und Nutzen Sie zur Genehmigung Workflow."
author: mikefalkner
manager: annbe
ms.date: 08/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: Vendor
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: 98ed3378ab05c0c69c9e5b2a82310113a81c2264
ms.openlocfilehash: 950a1852acf9f3e4747ce2d55738c0eb3a646897
ms.contentlocale: de-de
ms.lasthandoff: 08/31/2018

---

# <a name="vendor-workflow"></a><span data-ttu-id="57122-103">Lieferantenworkflow</span><span class="sxs-lookup"><span data-stu-id="57122-103">Vendor workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="57122-104">Wenn der Kreditorenworkflow verwendet wird, werden Änderungen, die zu bestimmten Feldern vorgenommen werden, zur Genehmigung an den Workflow gesendet, bevor sie dem Kreditor hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="57122-104">When the vendor workflow is used, changes that are made to specific fields are sent to the workflow for approval before they are added to the vendor.</span></span>

## <a name="set-up-the-vendor-workflow"></a><span data-ttu-id="57122-105">Lieferantenworkflow einrichten</span><span class="sxs-lookup"><span data-stu-id="57122-105">Set up the vendor workflow</span></span>

<span data-ttu-id="57122-106">Die Funktion Workflow kann erst nach der Aktivierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="57122-106">Before you can use the workflow feature, you must enable it.</span></span>

1. <span data-ttu-id="57122-107">Wechseln Sie zu **Kreditoren \> Einstellung \> Kreditorenparameter**.</span><span class="sxs-lookup"><span data-stu-id="57122-107">Go to **Accounts payable \> Setup \> Accounts payable parameters**.</span></span>
2. <span data-ttu-id="57122-108">Legen Sie auf der Registerkarte **Genehmigter Kreditor** im Inforegister **Allgemein** die Option **Genehmigter Kretitor aktivieren** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="57122-108">On the **General** tab, on the **Vendor approval** FastTab, set the **Enable vendor approvals** option to **Yes**.</span></span>
3. <span data-ttu-id="57122-109">Im Feld **Datenentitätsverhalten** wählen Sie das Verhalten aus, das verwendet werden soll, wenn Daten importiert werden:</span><span class="sxs-lookup"><span data-stu-id="57122-109">In the **Data entity behavior** field, select the behavior that should be used when data is imported:</span></span>

    - <span data-ttu-id="57122-110">**Ermöglichen von Änderungen ohne Genehmigung** – Die Datenentität kann den Kreditorendatensatz aktualisieren, ohne ihn mit dem Standardworkflow verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="57122-110">**Allow changes without approval** – The data entity can update the vendor record without processing it through the workflow.</span></span>
    - <span data-ttu-id="57122-111">**Weisen Sie Änderungen zurück** – Änderungen können vorgenommen nicht auf dem Kreditorendatensatz vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="57122-111">**Reject changes** – Changes can't be made to the vendor record.</span></span> <span data-ttu-id="57122-112">Der Import schlägt für die Felder fehl, die für Importe Workflow aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="57122-112">The import will fail for the fields that are enabled for the workflow.</span></span>
    - <span data-ttu-id="57122-113">**Änderungsvorschläge erstellen** – Alle Felder werden mit Ausnahme der Felder geändert, die für den Workflow aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="57122-113">**Create change proposals** – All fields will be changed except the fields that are enabled for the workflow.</span></span> <span data-ttu-id="57122-114">Die neuen Werte für diese Felder werden an den Kreditor hinzugefügt, da vorgeschlagene Änderungen und der Workflow automatisch gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="57122-114">The new values for those fields will be added to the vendor as proposed changes, and the workflow will be started automatically.</span></span>

4. <span data-ttu-id="57122-115">In der Liste mit Kreditorenfeldern aktivieren Sie das Kästchen **Aktivieren** für jedes aus, das genehmigt werden muss, damit die Änderungen vorgenommen werden können.</span><span class="sxs-lookup"><span data-stu-id="57122-115">In the list of vendor fields, select the **Enable** check box for every field that must be approved before the changes can be made.</span></span>
5. <span data-ttu-id="57122-116">Wechseln Sie zu **Kreditoren \> Einstellung \> Kreditorenworkflows**.</span><span class="sxs-lookup"><span data-stu-id="57122-116">Go to **Accounts payable \> Setup \> Accounts payable workflows**.</span></span>
6. <span data-ttu-id="57122-117">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="57122-117">Select **New**.</span></span>
7. <span data-ttu-id="57122-118">Wählen Sie **Workflow zu vorgeschlagenen Lieferantenänderungen**.</span><span class="sxs-lookup"><span data-stu-id="57122-118">Select **Proposed vendor changes workflow**.</span></span> 
8. <span data-ttu-id="57122-119">Einrichten des Workflows, so dass er mit demn Genehmigungsprozess übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="57122-119">Set up the workflow so that it matches your approval process.</span></span> <span data-ttu-id="57122-120">Das Workflowgenehmigungselement **Workflowgenehmigungen für vorgeschlagene Kreditorenänderung** übernimmt die Änderung des Kreditors.</span><span class="sxs-lookup"><span data-stu-id="57122-120">The **Workflow approval for proposed vendor change** workflow approval element will apply the changes to the vendor.</span></span>

## <a name="change-vendor-information-and-submit-the-changes-to-the-workflow"></a><span data-ttu-id="57122-121">Ändern Sie Kreditoreninformationen und übermitteln Sie die Änderungen an den Workflow</span><span class="sxs-lookup"><span data-stu-id="57122-121">Change vendor information and submit the changes to the workflow</span></span>

<span data-ttu-id="57122-122">Wenn Sie ein Feld ändern, das für den Workflow aktiviert ist, wird die Seite **Vorgeschlagene Änderungen** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="57122-122">When you change a field that is enabled for the workflow, the **Proposed changes** page appears.</span></span> <span data-ttu-id="57122-123">Diese Seite enthält den ursprünglichen Wert des Felds und den neuen Wert, den Sie eingegeben haben.</span><span class="sxs-lookup"><span data-stu-id="57122-123">This page shows the original value of the field and the new value that you entered.</span></span> <span data-ttu-id="57122-124">Das Feld, das Sie ändern, wird auf den ursprünglichen Wert zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="57122-124">The field that you changed is reverted to its original value.</span></span> <span data-ttu-id="57122-125">Eine Statusmeldung informiert Sie auch, dass die Änderungen nicht übermittelt wurden.</span><span class="sxs-lookup"><span data-stu-id="57122-125">A status message also informs you that your changes haven't been submitted.</span></span> 

<span data-ttu-id="57122-126">Immer wenn Sie ein Feld ändern, das für den Workflow aktiviert ist, wird dieses Feld der Liste auf der Seite **Vorgeschlagene Änderungen** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="57122-126">Every time that you change a field that is enabled for the workflow, that field is added to the list on the **Proposed changes** page.</span></span> <span data-ttu-id="57122-127">Um den vorgeschlagenen Wert für ein Feld zu verwerfen, verwenden Sie die Schaltfläche **Verwerfen** neben dem Feld in der Liste.</span><span class="sxs-lookup"><span data-stu-id="57122-127">To discard the proposed value for a field, use the **Discard** button next to the field in the list.</span></span> <span data-ttu-id="57122-128">Um sämtliche Änderungen zu verwerfen, verwenden Sie die Schaltfläche **Alle Änderungen verwerfen** am unteren Seitenrand.</span><span class="sxs-lookup"><span data-stu-id="57122-128">To discard all changes, use the **Discard all changes** button at the bottom of the page.</span></span> <span data-ttu-id="57122-129">Klicken Sie auf **OK**, um die Seite zu schließen.</span><span class="sxs-lookup"><span data-stu-id="57122-129">Select **OK** to close the page.</span></span>

<span data-ttu-id="57122-130">Nachdem Sie mindestens eine vorgeschlagene Änderung haben, werden zwei zusätzliche Registerkarten im Aktivitätsbereich: **Vorgeschlagene Änderungen** und **Workflow** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="57122-130">After you have at least one proposed change, two additional tabs appear on the action pane: **Proposed changes** and **Workflow**.</span></span>

1. <span data-ttu-id="57122-131">Wählen Sie **Vorgeschlagene Änderungen**, um die Seite **Vorgeschlagene Änderungen** zu öffnen und die Änderungen zu prüfen.</span><span class="sxs-lookup"><span data-stu-id="57122-131">Select **Proposed changes** to open the **Proposed changes** page and review your changes.</span></span>
2. <span data-ttu-id="57122-132">Wählen Sie **Workflow\>Übermitteln, um die Änderungen für den Workflow zu ändern**.</span><span class="sxs-lookup"><span data-stu-id="57122-132">Select **Workflow \> Submit to submit the changes to workflow**.</span></span>

    <span data-ttu-id="57122-133">Der Status auf der Seite wird zu **Ändert ausstehenden Genehmigungen** geändert.</span><span class="sxs-lookup"><span data-stu-id="57122-133">The status on the page is changed to **Changes pending approval**.</span></span>

<span data-ttu-id="57122-134">Der Workflow Standardworkflowprozess erfolgt gemäß dem Prozess in Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="57122-134">The workflow follows the standard workflow process in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="57122-135">Die genehmigende Person wird auf die Seite **Kreditor** verwiesen, auf der sie die Änderungen auf der Seite Überprüfen **Vorgeschlagene Änderungen** und dann **Workflow \> Genehmigen** auswählen können, um den Workflow zu genehmigen.</span><span class="sxs-lookup"><span data-stu-id="57122-135">The approver is directed to the **Vendor** page, where he or she can review the changes on the **Proposed changes** page and then select **Workflow \> Approve** to approve the workflow.</span></span> <span data-ttu-id="57122-136">Wenn alle Genehmigungen abgeschlossen sind, werden die Felder mit den Werten gefüllt, die Sie vorschlugen.</span><span class="sxs-lookup"><span data-stu-id="57122-136">After all approvals are completed, the fields are updated with the values that you proposed.</span></span>

