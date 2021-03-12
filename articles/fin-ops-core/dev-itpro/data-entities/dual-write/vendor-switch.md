---
title: Wechsel zwischen Kreditorendesigns
description: In diesem Thema wird der Wechsel der Integration von Kreditorendaten zwischen Finance and Operations Apps und Dataverse beschrieben.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: d2c22123d5f05945b34eb107c5b912852aec387a
ms.sourcegitcommit: 7e1be696894731e1c58074d9b5e9c5b3acf7e52a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4744464"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="e26a1-103">Wechsel zwischen Kreditorendesigns</span><span class="sxs-lookup"><span data-stu-id="e26a1-103">Switch between vendor designs</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



## <a name="vendor-data-flow"></a><span data-ttu-id="e26a1-104">Kreditorendatenfluss</span><span class="sxs-lookup"><span data-stu-id="e26a1-104">Vendor data flow</span></span> 

<span data-ttu-id="e26a1-105">Wenn Sie die Tabelle **Konto** zum Speichern von Lieferanten vom Typ **Organisation** und die Tabelle **Kontakt** zum Speichern von Lieferanten vom Typ **Person** verwenden, konfigurieren Sie die folgenden Workflows.</span><span class="sxs-lookup"><span data-stu-id="e26a1-105">If you choose to use the **Account** table to store vendors of the **Organization** type and the **Contact** table to store vendors of the **Person** type, configure the following workflows.</span></span> <span data-ttu-id="e26a1-106">Andernfalls ist diese Konfiguration nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e26a1-106">Otherwise, this configuration isn't required.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a><span data-ttu-id="e26a1-107">Erweiterte Kreditorendesign für Kreditoren vom Typ „Organisation“ verwenden</span><span class="sxs-lookup"><span data-stu-id="e26a1-107">Use the extended vendor design for vendors of the Organization type</span></span>

<span data-ttu-id="e26a1-108">Das Lösungspaket **Dynamics365FinanceExtended** enthält die folgenden Workflow-Prozessvorlagen.</span><span class="sxs-lookup"><span data-stu-id="e26a1-108">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="e26a1-109">Sie erstellen für jede Vorlage einen Workflow.</span><span class="sxs-lookup"><span data-stu-id="e26a1-109">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="e26a1-110">Lieferanten in der Kontotabelle erstellen</span><span class="sxs-lookup"><span data-stu-id="e26a1-110">Create Vendors in Accounts Table</span></span>
+ <span data-ttu-id="e26a1-111">Lieferanten in der Lieferantentabelle erstellen</span><span class="sxs-lookup"><span data-stu-id="e26a1-111">Create Vendors in Vendors Table</span></span>
+ <span data-ttu-id="e26a1-112">Lieferanten in der Kontotabelle aktualisieren</span><span class="sxs-lookup"><span data-stu-id="e26a1-112">Update Vendors in Accounts Table</span></span>
+ <span data-ttu-id="e26a1-113">Lieferanten in der Lieferantentabelle aktualisieren</span><span class="sxs-lookup"><span data-stu-id="e26a1-113">Update Vendors in Vendors Table</span></span>

<span data-ttu-id="e26a1-114">Um neue Workflowprozesse mithilfe der Workflowprozessvorlagen zu erstellen, befolgen Sie diese Schritte:</span><span class="sxs-lookup"><span data-stu-id="e26a1-114">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="e26a1-115">Erstellen Sie einen Workflowprozess für die Tabelle **Lieferant** und wählen Sie die Workflowprozessvorlage **Lieferanten in der Kontotabelle erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="e26a1-115">Create a workflow process for the **Vendor** table, and select the **Create Vendors in Accounts Table** workflow process template.</span></span> <span data-ttu-id="e26a1-116">Wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="e26a1-116">Then select **OK**.</span></span> <span data-ttu-id="e26a1-117">Dieser Workflow verarbeitet das Lieferantenerstellungsszenario für die Tabelle **Konto**.</span><span class="sxs-lookup"><span data-stu-id="e26a1-117">This workflow handles the vendor creation scenario for the **Account** table.</span></span>

    ![Workflowprozess „Lieferanten in der Kontotabelle erstellen“](media/create_process.png)

2. <span data-ttu-id="e26a1-119">Erstellen Sie einen Workflowprozess für die Tabelle **Lieferant** und wählen Sie die Workflowprozessvorlage **Lieferanten in der Kontotabelle aktualisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="e26a1-119">Create a workflow process for the **Vendor** table, and select the **Update Vendors in Accounts Table** workflow process template.</span></span> <span data-ttu-id="e26a1-120">Wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="e26a1-120">Then select **OK**.</span></span> <span data-ttu-id="e26a1-121">Dieser Workflow verarbeitet das Lieferantenaktualisierungsszenario für die Tabelle **Konto**.</span><span class="sxs-lookup"><span data-stu-id="e26a1-121">This workflow handles the vendor update scenario for the **Account** table.</span></span>
3. <span data-ttu-id="e26a1-122">Erstellen Sie einen Workflowprozess für die Tabelle **Konto** und wählen Sie die Workflowprozessvorlage **Lieferanten in der Lieferantentabelle erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="e26a1-122">Create a workflow process for the **Account** table, and select the **Create Vendors in Vendors Table** workflow process template.</span></span>
4. <span data-ttu-id="e26a1-123">Erstellen Sie einen Workflowprozess für die Tabelle **Konto** und wählen Sie die Workflowprozessvorlage **Lieferanten in der Lieferantentabelle aktualisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="e26a1-123">Create a workflow process for the **Account** table, and select the **Update Vendors in Vendors Table** workflow process template.</span></span>
5. <span data-ttu-id="e26a1-124">Sie können die Workflow entweder als Echtzeit- oder Hintergrundworkflows je nach Ihren Anforderungen konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="e26a1-124">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="e26a1-125">Wählen Sie **In einen Hintergrundworkflow konvertieren** aus, um einen Workflow als Hintergrundworkflow zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="e26a1-125">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>

    ![Schaltfläche „In einen Hintergrundworkflow konvertieren“](media/background_workflow.png)

6. <span data-ttu-id="e26a1-127">Aktivieren Sie die Workflows, die Sie für die Tabellen **Konto** und **Lieferant** erstellt haben, um die Tabelle **Konto** für das Speichern von Informationen vom Typ **Organisation** zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="e26a1-127">Activate the workflows that you created for the **Account** and **Vendor** tables to start to use the **Account** table to store information for vendors of the **Organization** type.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a><span data-ttu-id="e26a1-128">Erweiterte Kreditorendesign für Kreditoren vom Typ „Person“ verwenden</span><span class="sxs-lookup"><span data-stu-id="e26a1-128">Use the extended vendor design for vendors of the Person type</span></span>

<span data-ttu-id="e26a1-129">Das Lösungspaket **Dynamics365FinanceExtended** enthält die folgenden Workflow-Prozessvorlagen.</span><span class="sxs-lookup"><span data-stu-id="e26a1-129">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="e26a1-130">Sie erstellen für jede Vorlage einen Workflow.</span><span class="sxs-lookup"><span data-stu-id="e26a1-130">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="e26a1-131">Lieferanten vom Typ „Person“ in der Lieferantentabelle erstellen</span><span class="sxs-lookup"><span data-stu-id="e26a1-131">Create Vendors of type Person in Vendors Table</span></span>
+ <span data-ttu-id="e26a1-132">Lieferanten vom Typ „Person“ in der Kontakttabelle erstellen</span><span class="sxs-lookup"><span data-stu-id="e26a1-132">Create Vendors of type Person in Contacts Table</span></span>
+ <span data-ttu-id="e26a1-133">Lieferanten vom Typ „Person“ in der Kontakttabelle aktualisieren</span><span class="sxs-lookup"><span data-stu-id="e26a1-133">Update Vendors of type Person in Contacts Table</span></span>
+ <span data-ttu-id="e26a1-134">Lieferanten vom Typ „Person“ in der Lieferantentabelle aktualisieren</span><span class="sxs-lookup"><span data-stu-id="e26a1-134">Update Vendors of type Person in Vendors Table</span></span>

<span data-ttu-id="e26a1-135">Um neue Workflowprozesse mithilfe der Workflowprozessvorlagen zu erstellen, befolgen Sie diese Schritte:</span><span class="sxs-lookup"><span data-stu-id="e26a1-135">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="e26a1-136">Erstellen Sie einen Workflowprozess für die Tabelle **Lieferant** und wählen Sie die Workflowprozessvorlage **Lieferanten vom Typ „Person“ in der Lieferantentabelle erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="e26a1-136">Create a workflow process for the **Vendor** table, and select the **Create Vendors of type Person in Contacts Table** workflow process template.</span></span> <span data-ttu-id="e26a1-137">Wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="e26a1-137">Then select **OK**.</span></span> <span data-ttu-id="e26a1-138">Dieser Workflow verarbeitet das Lieferantenerstellungsszenario für die Tabelle **Kontakt**.</span><span class="sxs-lookup"><span data-stu-id="e26a1-138">This workflow handles the vendor creation scenario for the **Contact** table.</span></span>
2. <span data-ttu-id="e26a1-139">Erstellen Sie einen Workflowprozess für die Tabelle **Lieferant** und wählen Sie die Workflowprozessvorlage **Lieferanten vom Typ „Person“ in der Lieferantentabelle aktualisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="e26a1-139">Create a workflow process for the **Vendor** table, and select the **Update Vendors of type Person in Contacts Table** workflow process template.</span></span> <span data-ttu-id="e26a1-140">Wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="e26a1-140">Then select **OK**.</span></span> <span data-ttu-id="e26a1-141">Dieser Workflow verarbeitet das Lieferantenaktualisierungsszenario für die Tabelle **Kontakt**.</span><span class="sxs-lookup"><span data-stu-id="e26a1-141">This workflow handles the vendor update scenario for the **Contact** table.</span></span>
3. <span data-ttu-id="e26a1-142">Erstellen Sie einen Workflowprozess für die Tabelle **Kontakt** und wählen Sie die Workflowprozessvorlage **Lieferanten vom Typ „Person“ in der Lieferantentabelle erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="e26a1-142">Create a workflow process for the **Contact** table, and select the **Create Vendors of type Person in Vendors Table** template.</span></span>
4. <span data-ttu-id="e26a1-143">Erstellen Sie einen Workflowprozess für die Tabelle **Kontakt** und wählen Sie die Workflowprozessvorlage **Lieferanten vom Typ „Person“ in der Lieferantentabelle aktualisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="e26a1-143">Create a workflow process for the **Contact** table, and select the **Update Vendors of type Person in Vendors Table** template.</span></span>
5. <span data-ttu-id="e26a1-144">Sie können die Workflow entweder als Echtzeit- oder Hintergrundworkflows je nach Ihren Anforderungen konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="e26a1-144">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="e26a1-145">Wählen Sie **In einen Hintergrundworkflow konvertieren** aus, um einen Workflow als Hintergrundworkflow zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="e26a1-145">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>
6. <span data-ttu-id="e26a1-146">Aktivieren Sie die Workflows, die Sie für die Tabellen **Kontakt** und **Lieferant** erstellt haben, um die Tabelle **Kontakt** für das Speichern von Informationen vom Typ **Person** zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="e26a1-146">Activate the workflows that you created on the **Contact** and **Vendor** tables to start to use the **Contact** table to store information for vendors of the **Person** type.</span></span>
