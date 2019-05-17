---
title: Debitorenworkflow
description: Dieses Thema enthält Informationen zum Debitorenworkflow. Sie ändern bestimmte Felder für einen Debitor und senden diese Änderungen zur Genehmigung, indem Sie den Workflow durchlaufen, bevor die Änderungen dem Debitor hinzugefügt werden.
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 71b6380e587c9d8e8c5677bfea6f2e5642fbd0d9
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1508758"
---
# <a name="customer-workflow"></a><span data-ttu-id="4bcc7-104">Debitorenworkflow</span><span class="sxs-lookup"><span data-stu-id="4bcc7-104">Customer workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4bcc7-105">Der Debitorenworkflow wurde zu Version 8.0.4 von Microsoft Dynamics 365 for Finance and Operations hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-105">The customer workflow has been added to Microsoft Dynamics 365 for Finance and Operations version 8.0.4.</span></span> <span data-ttu-id="4bcc7-106">Sie können bestimmte Felder für einen Debitor ändern und diese Änderungen dann zur Genehmigung einreichen, indem Sie den Workflow durchlaufen, bevor die Änderungen dem Debitor hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-106">You can change specific fields for a customer and then send those changes for approval by using the workflow before they are added to the customer.</span></span>

## <a name="set-up-the-customer-workflow"></a><span data-ttu-id="4bcc7-107">Debitorenworkflow einrichten</span><span class="sxs-lookup"><span data-stu-id="4bcc7-107">Set up the customer workflow</span></span>

<span data-ttu-id="4bcc7-108">Bevor Sie die Debitorenworkflowfunktion verwenden können, müssen Sie sie aktivieren.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-108">Before you can use the customer workflow feature, you must enable it.</span></span>

1. <span data-ttu-id="4bcc7-109">Gehen Sie zu **Debitoren \> Einrichtung \> Debitorenparameter**.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-109">Go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="4bcc7-110">Um die Funktion einzuschalten, legen Sie auf der Registerkarte **Allgemein** im Inforegister **Debitorengenehmigung** die Option **Debitorengenehmigungen aktivieren** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-110">On the **General** tab, on the **Customer approval** FastTab, set the **Enable customer approvals** option to **Yes** to enable the feature.</span></span>
3. <span data-ttu-id="4bcc7-111">Wählen Sie dann im Feld **Datenentitätsverhalten** die gewünschte Funktionsweise von Datenentitäten beim Import von Daten aus:</span><span class="sxs-lookup"><span data-stu-id="4bcc7-111">In the **Data entity behavior** field, select the behavior that the data entities should use when data is imported:</span></span>

    - <span data-ttu-id="4bcc7-112">**Änderungen ohne Genehmigung zulassen**: Entitäten können den Debitorendatensatz ohne Bearbeitung im Workflow aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-112">**Allow changes without approval** – An entity can update the customer record without processing it through the workflow.</span></span>
    - <span data-ttu-id="4bcc7-113">**Änderungen ablehnen**: Der Debitorendatensatz kann nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-113">**Reject changes** – Changes can't be made to the customer record.</span></span> <span data-ttu-id="4bcc7-114">Bei sämtlichen Feldern, die im Rahmen des Workflows aktiviert sind, schlägt der Importvorgang fehl.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-114">The import will fail for the fields that are enabled for the workflow.</span></span>
    - <span data-ttu-id="4bcc7-115">**Änderungsvorschläge erstellen**: Alle Felder werden geändert. Ausgenommen sind Felder, die im Rahmen des Workflows aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-115">**Create change proposals** – All fields will be changed except the fields that are enabled for the workflow.</span></span> <span data-ttu-id="4bcc7-116">Die neuen Werte für dieser Felder werden dem Debitor als vorgeschlagene Änderungen hinzugefügt, und der Workflow wird automatisch gestartet.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-116">The new values for those fields will be added to the customer as proposed changes, and the workflow will be started automatically.</span></span>

4. <span data-ttu-id="4bcc7-117">Wählen Sie in der Liste mit den Debitorenfeldern anschließend für jedes Feld, das vor Vornahme der Änderungen genehmigt werden muss, die Option **Aktivieren** aus.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-117">In the list of customer fields, select then **Enable** check box for every field that must be approved before the changes can be made.</span></span>
5. <span data-ttu-id="4bcc7-118">Gehen Sie zu **Debitoren \> Einrichtung \> Debitorenworkflows**.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-118">Go to **Accounts receivable \> Setup \> Accounts receivable workflows**.</span></span>
6. <span data-ttu-id="4bcc7-119">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-119">Select **New**.</span></span>
7. <span data-ttu-id="4bcc7-120">Wählen Sie **Vorgeschlagener Debitorenänderungsworkflow** aus.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-120">Select **Proposed customer change workflow**.</span></span> 
8. <span data-ttu-id="4bcc7-121">Gestalten Sie den Workflow so, dass er Ihrem Genehmigungsverfahren entspricht.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-121">Set up the workflow so that it matches your approval process.</span></span> <span data-ttu-id="4bcc7-122">Mithilfe des Workflowgenehmigungselements **Workflowgenehmigung für Debitorenänderung** werden die Änderungen für den Debitoren übernommen.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-122">The **Workflow approval for proposed customer change** workflow approval element will apply the changes to the customer.</span></span>

## <a name="change-customer-information-and-submit-the-changes-to-the-workflow"></a><span data-ttu-id="4bcc7-123">Ändern Sie die Debitorenangaben, und übertragen Sie die Änderungen an den Workflow.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-123">Change customer information and submit the changes to the workflow</span></span>

<span data-ttu-id="4bcc7-124">Wenn Sie ein Feld ändern, das für den Workflow aktiviert ist, wird die Seite **Vorgeschlagene Änderungen** geöffnet.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-124">When you change a field that is enabled for the workflow, the **Proposed changes** page appears.</span></span> <span data-ttu-id="4bcc7-125">Diese zeigt den ursprünglichen Feldwert und den neu eingegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-125">This page shows the original value of the field and the new value that you entered.</span></span> <span data-ttu-id="4bcc7-126">Das von Ihnen geänderte Feld wird auf den Originalwert zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-126">The field that you changed is reverted to its original value.</span></span> <span data-ttu-id="4bcc7-127">Eine Statusmeldung auf der Seite informiert Sie darüber, dass die Änderungen nicht übermittelt wurden.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-127">A status message on the page informs you that your changes haven't been submitted.</span></span>

<span data-ttu-id="4bcc7-128">Immer wenn Sie ein Feld ändern, das für den Workflow aktiviert ist, wird dieses Feld der Liste mit den vorgeschlagenen Änderungen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-128">Every time that you change a field that is enabled for the workflow, that field is added to the list of proposed changes.</span></span> <span data-ttu-id="4bcc7-129">Um den für ein Feld vorgeschlagenen Wert zu verwerfen, klicken Sie in der Liste neben dem Feld auf **Verwerfen**.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-129">To discard the proposed value for a field, use the **Discard** button next to the field in the list.</span></span> <span data-ttu-id="4bcc7-130">Sollen sämtliche Änderungen verworfen werden, klicken Sie unten auf der Seite auf **Alle Änderungen verwerfen**.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-130">To discard all changes, use the **Discard all change** button at the bottom of the page.</span></span> <span data-ttu-id="4bcc7-131">Schließen Sie die Seite mit **OK**.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-131">Select **OK** to close the page.</span></span>

<span data-ttu-id="4bcc7-132">Liegt mindestens eine vorgeschlagene Änderung vor, werden im Aktivitätsbereich zwei weitere Menüs angezeigt: **Vorgeschlagene Änderungen** und **Workflow**.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-132">After you have at least one proposed change, two additional menus appear on the Action Pane: **Proposed changes** and **Workflow**.</span></span>

1. <span data-ttu-id="4bcc7-133">Mit **Vorgeschlagene Änderungen** können Sie die Seite **Vorgeschlagene Änderungen** öffnen und Ihre Änderungen überprüfen.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-133">Select **Proposed changes** to open the **Proposed changes** page and review your changes.</span></span>
2. <span data-ttu-id="4bcc7-134">Um die Änderungen an den Workflow zu übertragen, wählen Sie **Workflow \> Übermitteln** aus.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-134">Select **Workflow \> Submit** to submit the changes to the workflow.</span></span>

    <span data-ttu-id="4bcc7-135">Der Status auf der Seite ändert sich in **Änderungen mit ausstehender Genehmigung**.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-135">The status on the page is changed to **Changes pending approval**.</span></span>

<span data-ttu-id="4bcc7-136">Der Workflow folgt dem Standardworkflowablauf aus Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-136">The workflow follows the standard workflow process in Finance and Operations.</span></span> <span data-ttu-id="4bcc7-137">Die genehmigende Person wird an die Seite **Debitor** weitergeleitet. Dort kann sie die Änderungen auf der Seite **Vorgeschlagene Änderungen** einsehen und den Workflow dann mit **Workflow \> Genehmigen** genehmigen.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-137">The approver is directed to the **Customer** page, where he or she can review the changes on the **Proposed changes** page and then select **Workflow \> Approve** to approve the workflow.</span></span> <span data-ttu-id="4bcc7-138">Sind alle Genehmigungen bearbeitet, werden die Felder mit den vorgeschlagenen Werten aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-138">After all approvals are completed, the fields are updated with the values that you proposed.</span></span>
