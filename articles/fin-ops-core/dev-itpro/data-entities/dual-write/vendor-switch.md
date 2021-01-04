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
ms.openlocfilehash: 731efd3ae841960f3a2c0b9be210c5c68ac835f5
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685508"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="37bb6-103">Wechsel zwischen Kreditorendesigns</span><span class="sxs-lookup"><span data-stu-id="37bb6-103">Switch between vendor designs</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



## <a name="vendor-data-flow"></a><span data-ttu-id="37bb6-104">Kreditorendatenfluss</span><span class="sxs-lookup"><span data-stu-id="37bb6-104">Vendor data flow</span></span> 

<span data-ttu-id="37bb6-105">Wenn Sie die Entität **Konto** zum Speichern von Kreditoren vom Typ **Organisation** und die Entität **Kontakt** zum Speichern von Kreditoren vom Typ **Person** verwenden, konfigurieren Sie die folgenden Workflows.</span><span class="sxs-lookup"><span data-stu-id="37bb6-105">If you choose to use the **Account** entity to store vendors of the **Organization** type and the **Contact** entity to store vendors of the **Person** type, configure the following workflows.</span></span> <span data-ttu-id="37bb6-106">Andernfalls ist diese Konfiguration nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="37bb6-106">Otherwise, this configuration isn't required.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a><span data-ttu-id="37bb6-107">Erweiterte Kreditorendesign für Kreditoren vom Typ „Organisation“ verwenden</span><span class="sxs-lookup"><span data-stu-id="37bb6-107">Use the extended vendor design for vendors of the Organization type</span></span>

<span data-ttu-id="37bb6-108">Das Lösungspaket **Dynamics365FinanceExtended** enthält die folgenden Workflow-Prozessvorlagen.</span><span class="sxs-lookup"><span data-stu-id="37bb6-108">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="37bb6-109">Sie erstellen für jede Vorlage einen Workflow.</span><span class="sxs-lookup"><span data-stu-id="37bb6-109">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="37bb6-110">Lieferanten in der Kontotabelle erstellen</span><span class="sxs-lookup"><span data-stu-id="37bb6-110">Create Vendors in Accounts Table</span></span>
+ <span data-ttu-id="37bb6-111">Lieferanten in der Lieferantentabelle erstellen</span><span class="sxs-lookup"><span data-stu-id="37bb6-111">Create Vendors in Vendors Table</span></span>
+ <span data-ttu-id="37bb6-112">Lieferanten in der Kontotabelle aktualisieren</span><span class="sxs-lookup"><span data-stu-id="37bb6-112">Update Vendors in Accounts Table</span></span>
+ <span data-ttu-id="37bb6-113">Lieferanten in der Lieferantentabelle aktualisieren</span><span class="sxs-lookup"><span data-stu-id="37bb6-113">Update Vendors in Vendors Table</span></span>

<span data-ttu-id="37bb6-114">Um neue Workflowprozesse mithilfe der Workflowprozessvorlagen zu erstellen, befolgen Sie diese Schritte:</span><span class="sxs-lookup"><span data-stu-id="37bb6-114">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="37bb6-115">Erstellen Sie einen Workflowprozess für die Entität **Lieferant** und wählen Sie die Workflowprozessvorlage **Lieferanten in der Kontotabelle erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="37bb6-115">Create a workflow process for the **Vendor** entity, and select the **Create Vendors in Accounts Table** workflow process template.</span></span> <span data-ttu-id="37bb6-116">Wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="37bb6-116">Then select **OK**.</span></span> <span data-ttu-id="37bb6-117">Dieser Workflow verarbeitet das Lieferantenerstellungsszenario für die Entität **Konto**.</span><span class="sxs-lookup"><span data-stu-id="37bb6-117">This workflow handles the vendor creation scenario for the **Account** entity.</span></span>

    ![Workflowprozess „Lieferanten in der Kontotabelle erstellen“](media/create_process.png)

2. <span data-ttu-id="37bb6-119">Erstellen Sie einen Workflowprozess für die Entität **Lieferant** und wählen Sie die Workflowprozessvorlage **Lieferanten in der Kontotabelle aktualisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="37bb6-119">Create a workflow process for the **Vendor** entity, and select the **Update Vendors in Accounts Table** workflow process template.</span></span> <span data-ttu-id="37bb6-120">Wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="37bb6-120">Then select **OK**.</span></span> <span data-ttu-id="37bb6-121">Dieser Workflow verarbeitet das Lieferantenaktualisierungsszenario für die Entität **Konto**.</span><span class="sxs-lookup"><span data-stu-id="37bb6-121">This workflow handles the vendor update scenario for the **Account** entity.</span></span>
3. <span data-ttu-id="37bb6-122">Erstellen Sie einen Workflowprozess für die Entität **Konto** und wählen Sie die Workflowprozessvorlage **Lieferanten in der Lieferantentabelle erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="37bb6-122">Create a workflow process for the **Account** entity, and select the **Create Vendors in Vendors Table** workflow process template.</span></span>
4. <span data-ttu-id="37bb6-123">Erstellen Sie einen Workflowprozess für die Entität **Konto** und wählen Sie die Workflowprozessvorlage **Lieferanten in der Lieferantentabelle aktualisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="37bb6-123">Create a workflow process for the **Account** entity, and select the **Update Vendors in Vendors Table** workflow process template.</span></span>
5. <span data-ttu-id="37bb6-124">Sie können die Workflow entweder als Echtzeit- oder Hintergrundworkflows je nach Ihren Anforderungen konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="37bb6-124">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="37bb6-125">Wählen Sie **In einen Hintergrundworkflow konvertieren** aus, um einen Workflow als Hintergrundworkflow zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="37bb6-125">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>

    ![Schaltfläche „In einen Hintergrundworkflow konvertieren“](media/background_workflow.png)

6. <span data-ttu-id="37bb6-127">Aktivieren Sie die Workflows, die Sie für die Tabellen **Konto** und **Lieferant** erstellt haben, um die Entität **Konto** für das Speichern von Informationen vom Typ **Organisation** zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="37bb6-127">Activate the workflows that you created for the **Account** and **Vendor** tables to start to use the **Account** entity to store information for vendors of the **Organization** type.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a><span data-ttu-id="37bb6-128">Erweiterte Kreditorendesign für Kreditoren vom Typ „Person“ verwenden</span><span class="sxs-lookup"><span data-stu-id="37bb6-128">Use the extended vendor design for vendors of the Person type</span></span>

<span data-ttu-id="37bb6-129">Das Lösungspaket **Dynamics365FinanceExtended** enthält die folgenden Workflow-Prozessvorlagen.</span><span class="sxs-lookup"><span data-stu-id="37bb6-129">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="37bb6-130">Sie erstellen für jede Vorlage einen Workflow.</span><span class="sxs-lookup"><span data-stu-id="37bb6-130">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="37bb6-131">Lieferanten vom Typ „Person“ in der Lieferantentabelle erstellen</span><span class="sxs-lookup"><span data-stu-id="37bb6-131">Create Vendors of type Person in Vendors Table</span></span>
+ <span data-ttu-id="37bb6-132">Lieferanten vom Typ „Person“ in der Kontakttabelle erstellen</span><span class="sxs-lookup"><span data-stu-id="37bb6-132">Create Vendors of type Person in Contacts Table</span></span>
+ <span data-ttu-id="37bb6-133">Lieferanten vom Typ „Person“ in der Kontakttabelle aktualisieren</span><span class="sxs-lookup"><span data-stu-id="37bb6-133">Update Vendors of type Person in Contacts Table</span></span>
+ <span data-ttu-id="37bb6-134">Lieferanten vom Typ „Person“ in der Lieferantentabelle aktualisieren</span><span class="sxs-lookup"><span data-stu-id="37bb6-134">Update Vendors of type Person in Vendors Table</span></span>

<span data-ttu-id="37bb6-135">Um neue Workflowprozesse mithilfe der Workflowprozessvorlagen zu erstellen, befolgen Sie diese Schritte:</span><span class="sxs-lookup"><span data-stu-id="37bb6-135">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="37bb6-136">Erstellen Sie einen Workflowprozess für die Entität **Lieferant** und wählen Sie die Workflowprozessvorlage **Lieferanten vom Typ „Person“ in der Lieferantentabelle erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="37bb6-136">Create a workflow process for the **Vendor** entity, and select the **Create Vendors of type Person in Contacts Table** workflow process template.</span></span> <span data-ttu-id="37bb6-137">Wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="37bb6-137">Then select **OK**.</span></span> <span data-ttu-id="37bb6-138">Dieser Workflow verarbeitet das Lieferantenerstellungsszenario für die Entität **Kontakt**.</span><span class="sxs-lookup"><span data-stu-id="37bb6-138">This workflow handles the vendor creation scenario for the **Contact** entity.</span></span>
2. <span data-ttu-id="37bb6-139">Erstellen Sie einen Workflowprozess für die Entität **Lieferant** und wählen Sie die Workflowprozessvorlage **Lieferanten vom Typ „Person“ in der Kontakttabelle aktualisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="37bb6-139">Create a workflow process for the **Vendor** entity, and select the **Update Vendors of type Person in Contacts Table** workflow process template.</span></span> <span data-ttu-id="37bb6-140">Wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="37bb6-140">Then select **OK**.</span></span> <span data-ttu-id="37bb6-141">Dieser Workflow verarbeitet das Lieferantenaktualisierungsszenario für die Entität **Kontakt**.</span><span class="sxs-lookup"><span data-stu-id="37bb6-141">This workflow handles the vendor update scenario for the **Contact** entity.</span></span>
3. <span data-ttu-id="37bb6-142">Erstellen Sie einen Workflowprozess für die Entität **Kontakt** und wählen Sie die Workflowprozessvorlage **Lieferanten vom Typ „Person“ in der Lieferantentabelle erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="37bb6-142">Create a workflow process for the **Contact** entity, and select the **Create Vendors of type Person in Vendors Table** template.</span></span>
4. <span data-ttu-id="37bb6-143">Erstellen Sie einen Workflowprozess für die Entität **Kontakt** und wählen Sie die Workflowprozessvorlage **Lieferanten vom Typ „Person“ in der Lieferantentabelle aktualisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="37bb6-143">Create a workflow process for the **Contact** entity, and select the **Update Vendors of type Person in Vendors Table** template.</span></span>
5. <span data-ttu-id="37bb6-144">Sie können die Workflow entweder als Echtzeit- oder Hintergrundworkflows je nach Ihren Anforderungen konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="37bb6-144">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="37bb6-145">Wählen Sie **In einen Hintergrundworkflow konvertieren** aus, um einen Workflow als Hintergrundworkflow zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="37bb6-145">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>
6. <span data-ttu-id="37bb6-146">Aktivieren Sie die Workflows, die Sie für die Tabellen **Kontakt** und **Lieferant** erstellt haben, um die Entität **Kontakt** für das Speichern von Informationen vom Typ **Person** zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="37bb6-146">Activate the workflows that you created on the **Contact** and **Vendor** tables to start to use the **Contact** entity to store information for vendors of the **Person** type.</span></span>
