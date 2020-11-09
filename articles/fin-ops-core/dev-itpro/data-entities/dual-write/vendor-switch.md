---
title: Wechsel zwischen Kreditorendesigns
description: In diesem Thema wird der Wechsel der Integration von Kreditorendaten zwischen Finance and Operations Apps und Common Data Service beschrieben.
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
ms.openlocfilehash: 0ecc401706911f8b92146b95bb6415185df8b451
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997551"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="ad860-103">Wechsel zwischen Kreditorendesigns</span><span class="sxs-lookup"><span data-stu-id="ad860-103">Switch between vendor designs</span></span>

[!include [banner](../../includes/banner.md)]



## <a name="vendor-data-flow"></a><span data-ttu-id="ad860-104">Kreditorendatenfluss</span><span class="sxs-lookup"><span data-stu-id="ad860-104">Vendor data flow</span></span> 

<span data-ttu-id="ad860-105">Wenn Sie die Entität **Konto** zum Speichern von Kreditoren vom Typ **Organisation** und die Entität **Kontakt** zum Speichern von Kreditoren vom Typ **Person** verwenden, konfigurieren Sie die folgenden Workflows.</span><span class="sxs-lookup"><span data-stu-id="ad860-105">If you choose to use the **Account** entity to store vendors of the **Organization** type and the **Contact** entity to store vendors of the **Person** type, configure the following workflows.</span></span> <span data-ttu-id="ad860-106">Andernfalls ist diese Konfiguration nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ad860-106">Otherwise, this configuration isn't required.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a><span data-ttu-id="ad860-107">Erweiterte Kreditorendesign für Kreditoren vom Typ „Organisation“ verwenden</span><span class="sxs-lookup"><span data-stu-id="ad860-107">Use the extended vendor design for vendors of the Organization type</span></span>

<span data-ttu-id="ad860-108">Das Lösungspaket **Dynamics365FinanceExtended** enthält die folgenden Workflow-Prozessvorlagen.</span><span class="sxs-lookup"><span data-stu-id="ad860-108">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="ad860-109">Sie erstellen für jede Vorlage einen Workflow.</span><span class="sxs-lookup"><span data-stu-id="ad860-109">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="ad860-110">Lieferanten in der Kontoentität erstellen</span><span class="sxs-lookup"><span data-stu-id="ad860-110">Create Vendors in Accounts Entity</span></span>
+ <span data-ttu-id="ad860-111">Lieferanten in der Lieferantenentität erstellen</span><span class="sxs-lookup"><span data-stu-id="ad860-111">Create Vendors in Vendors Entity</span></span>
+ <span data-ttu-id="ad860-112">Lieferanten in der Kontoentität aktualisieren</span><span class="sxs-lookup"><span data-stu-id="ad860-112">Update Vendors in Accounts Entity</span></span>
+ <span data-ttu-id="ad860-113">Lieferanten in der Lieferantenentität aktualisieren</span><span class="sxs-lookup"><span data-stu-id="ad860-113">Update Vendors in Vendors Entity</span></span>

<span data-ttu-id="ad860-114">Um neue Workflowprozesse mithilfe der Workflowprozessvorlagen zu erstellen, befolgen Sie diese Schritte:</span><span class="sxs-lookup"><span data-stu-id="ad860-114">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="ad860-115">Erstellen Sie einen Workflowprozess für die Entität **Lieferant** und wählen Sie die Workflowprozessvorlage **Lieferanten in der Kontoentität erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="ad860-115">Create a workflow process for the **Vendor** entity, and select the **Create Vendors in Accounts Entity** workflow process template.</span></span> <span data-ttu-id="ad860-116">Wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="ad860-116">Then select **OK**.</span></span> <span data-ttu-id="ad860-117">Dieser Workflow verarbeitet das Lieferantenerstellungsszenario für die Entität **Konto**.</span><span class="sxs-lookup"><span data-stu-id="ad860-117">This workflow handles the vendor creation scenario for the **Account** entity.</span></span>

    ![Workflowprozess „Lieferanten in der Kontoentität erstellen“](media/create_process.png)

2. <span data-ttu-id="ad860-119">Erstellen Sie einen Workflowprozess für die Entität **Lieferant** und wählen Sie die Workflowprozessvorlage **Lieferanten in der Kontoentität aktualisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="ad860-119">Create a workflow process for the **Vendor** entity, and select the **Update Vendors in Accounts Entity** workflow process template.</span></span> <span data-ttu-id="ad860-120">Wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="ad860-120">Then select **OK**.</span></span> <span data-ttu-id="ad860-121">Dieser Workflow verarbeitet das Lieferantenaktualisierungsszenario für die Entität **Konto**.</span><span class="sxs-lookup"><span data-stu-id="ad860-121">This workflow handles the vendor update scenario for the **Account** entity.</span></span>
3. <span data-ttu-id="ad860-122">Erstellen Sie einen Workflowprozess für die Entität **Konto** und wählen Sie die Workflowprozessvorlage **Lieferanten in der Lieferantenentität erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="ad860-122">Create a workflow process for the **Account** entity, and select the **Create Vendors in Vendors Entity** workflow process template.</span></span>
4. <span data-ttu-id="ad860-123">Erstellen Sie einen Workflowprozess für die Entität **Konto** und wählen Sie die Workflowprozessvorlage **Lieferanten in der Lieferantenentität aktualisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="ad860-123">Create a workflow process for the **Account** entity, and select the **Update Vendors in Vendors Entity** workflow process template.</span></span>
5. <span data-ttu-id="ad860-124">Sie können die Workflow entweder als Echtzeit- oder Hintergrundworkflows je nach Ihren Anforderungen konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="ad860-124">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="ad860-125">Wählen Sie **In einen Hintergrundworkflow konvertieren** aus, um einen Workflow als Hintergrundworkflow zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="ad860-125">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>

    ![Schaltfläche „In einen Hintergrundworkflow konvertieren“](media/background_workflow.png)

6. <span data-ttu-id="ad860-127">Aktivieren Sie die Workflows, die Sie für die Entitäten **Konto** und **Lieferant** erstellt haben, um die Entität **Konto** für das Speichern von Informationen vom Typ **Organisation** zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ad860-127">Activate the workflows that you created for the **Account** and **Vendor** entities to start to use the **Account** entity to store information for vendors of the **Organization** type.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a><span data-ttu-id="ad860-128">Erweiterte Kreditorendesign für Kreditoren vom Typ „Person“ verwenden</span><span class="sxs-lookup"><span data-stu-id="ad860-128">Use the extended vendor design for vendors of the Person type</span></span>

<span data-ttu-id="ad860-129">Das Lösungspaket **Dynamics365FinanceExtended** enthält die folgenden Workflow-Prozessvorlagen.</span><span class="sxs-lookup"><span data-stu-id="ad860-129">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="ad860-130">Sie erstellen für jede Vorlage einen Workflow.</span><span class="sxs-lookup"><span data-stu-id="ad860-130">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="ad860-131">Lieferanten vom Typ „Person“ in der Lieferantenentität erstellen</span><span class="sxs-lookup"><span data-stu-id="ad860-131">Create Vendors of type Person in Vendors Entity</span></span>
+ <span data-ttu-id="ad860-132">Lieferanten vom Typ „Person“ in der Kontaktentität zu erstellen</span><span class="sxs-lookup"><span data-stu-id="ad860-132">Create Vendors of type Person in Contacts Entity</span></span>
+ <span data-ttu-id="ad860-133">Lieferanten vom Typ „Person“ in der Kontaktentität aktualisieren</span><span class="sxs-lookup"><span data-stu-id="ad860-133">Update Vendors of type Person in Contacts Entity</span></span>
+ <span data-ttu-id="ad860-134">Lieferanten vom Typ „Person“ in der Lieferantenentität aktualisieren</span><span class="sxs-lookup"><span data-stu-id="ad860-134">Update Vendors of type Person in Vendors Entity</span></span>

<span data-ttu-id="ad860-135">Um neue Workflowprozesse mithilfe der Workflowprozessvorlagen zu erstellen, befolgen Sie diese Schritte:</span><span class="sxs-lookup"><span data-stu-id="ad860-135">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="ad860-136">Erstellen Sie einen Workflowprozess für die Entität **Lieferant** und wählen Sie die Workflowprozessvorlage **Lieferanten vom Typ „Person“ in der Lieferantenentität erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="ad860-136">Create a workflow process for the **Vendor** entity, and select the **Create Vendors of type Person in Contacts Entity** workflow process template.</span></span> <span data-ttu-id="ad860-137">Wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="ad860-137">Then select **OK**.</span></span> <span data-ttu-id="ad860-138">Dieser Workflow verarbeitet das Lieferantenerstellungsszenario für die Entität **Kontakt**.</span><span class="sxs-lookup"><span data-stu-id="ad860-138">This workflow handles the vendor creation scenario for the **Contact** entity.</span></span>
2. <span data-ttu-id="ad860-139">Erstellen Sie einen Workflowprozess für die Entität **Lieferant** und wählen Sie die Workflowprozessvorlage **Lieferanten vom Typ „Person“ in der Lieferantenentität aktualisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="ad860-139">Create a workflow process for the **Vendor** entity, and select the **Update Vendors of type Person in Contacts Entity** workflow process template.</span></span> <span data-ttu-id="ad860-140">Wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="ad860-140">Then select **OK**.</span></span> <span data-ttu-id="ad860-141">Dieser Workflow verarbeitet das Lieferantenaktualisierungsszenario für die Entität **Kontakt**.</span><span class="sxs-lookup"><span data-stu-id="ad860-141">This workflow handles the vendor update scenario for the **Contact** entity.</span></span>
3. <span data-ttu-id="ad860-142">Erstellen Sie einen Workflowprozess für die Entität **Kontakt** und wählen Sie die Workflowprozessvorlage **Lieferanten vom Typ „Person“ in der Lieferantenentität erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="ad860-142">Create a workflow process for the **Contact** entity, and select the **Create Vendors of type Person in Vendors Entity** template.</span></span>
4. <span data-ttu-id="ad860-143">Erstellen Sie einen Workflowprozess für die Entität **Kontakt** und wählen Sie die Workflowprozessvorlage **Lieferanten vom Typ „Person“ in der Lieferantenentität aktualisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="ad860-143">Create a workflow process for the **Contact** entity, and select the **Update Vendors of type Person in Vendors Entity** template.</span></span>
5. <span data-ttu-id="ad860-144">Sie können die Workflow entweder als Echtzeit- oder Hintergrundworkflows je nach Ihren Anforderungen konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="ad860-144">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="ad860-145">Wählen Sie **In einen Hintergrundworkflow konvertieren** aus, um einen Workflow als Hintergrundworkflow zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="ad860-145">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>
6. <span data-ttu-id="ad860-146">Aktivieren Sie die Workflows, die Sie für die Entitäten **Kontakt** und **Lieferant** erstellt haben, um die Entität **Kontakt** für das Speichern von Informationen vom Typ **Person** zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ad860-146">Activate the workflows that you created on the **Contact** and **Vendor** entities to start to use the **Contact** entity to store information for vendors of the **Person** type.</span></span>
