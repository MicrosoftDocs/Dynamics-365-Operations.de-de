---
title: Wechsel zwischen Kreditorendesigns
description: In diesem Thema wird der Wechsel von Kreditorendaten zwischen Finance and Operations-Apps und Common Data Service beschrieben.
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 204d788e72e79e7acf744d24cbeacb0f9b47da7d
ms.sourcegitcommit: 3306e451f04df01c51d8d332306b135d8ae1e254
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2019
ms.locfileid: "2902724"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="f019b-103">Wechsel zwischen Kreditorendesigns</span><span class="sxs-lookup"><span data-stu-id="f019b-103">Switch between vendor designs</span></span>

[!include [banner](../includes/banner.md)]

## <a name="vendor-data-flow"></a><span data-ttu-id="f019b-104">Kreditorendatenfluss</span><span class="sxs-lookup"><span data-stu-id="f019b-104">Vendor data flow</span></span> 

<span data-ttu-id="f019b-105">Wenn Sie andere Dynamics 365-Apps für das Lieferanten-Mastering verwenden und die Lieferanteninformationen von Kunden isolieren möchten, verwenden Sie dieses Basislieferantendesign.</span><span class="sxs-lookup"><span data-stu-id="f019b-105">If you use other Dynamics 365 apps for vendor mastering and you want to isolate vendor information from customers, use this basic vendor design.</span></span>  

![Grundlegender Lieferantenfluss](media/dual-write-vendor-data-flow.png)
 
<span data-ttu-id="f019b-107">Wenn Sie andere Dynamics 365-Apps für das Lieferanten-Mastering verwenden und weiterhin die **Kontoentität** zum Speichern der Lieferanteninformationen verwenden möchten, verwenden Sie dieses erweiterte Lieferantendesign.</span><span class="sxs-lookup"><span data-stu-id="f019b-107">If you use other Dynamics 365 apps for vendor mastering and you want to continue to use the **Account** entity for storing vendor information, use this extended vendor design.</span></span> <span data-ttu-id="f019b-108">In diesem Entwurf werden erweiterte Lieferanteninformationen wie der Gesperrt-Status des Lieferanten und das Lieferantenprofil in der Entität **Lieferanten** in Common Data Service gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f019b-108">In this design, extended vendor information like vendor on-hold status and vendor profile is stored in the **vendors** entity in Common Data Service.</span></span> 

![Erweiterter Lieferantenfluss](media/dual-write-vendor-detail.jpg)
 
<span data-ttu-id="f019b-110">Führen Sie die unten stehenden Schritte aus, um das erweiterte Lieferantendesign zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="f019b-110">Follow the below steps to use the extended vendor design:</span></span> 
 
1. <span data-ttu-id="f019b-111">Das **SupplyChainCommon**-Lösungspaket enthält die Workflowprozessvorlagen wie auf dem folgenden Bild gezeigt.</span><span class="sxs-lookup"><span data-stu-id="f019b-111">The **SupplyChainCommon** solution package contains the workflow process templates as shown in the following image.</span></span>
    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="f019b-112">![Workflowprozessvorlagen](media/dual-write-switch-3.png)</span><span class="sxs-lookup"><span data-stu-id="f019b-112">![Workflow process templates](media/dual-write-switch-3.png)</span></span>
2. <span data-ttu-id="f019b-113">Erstellen Sie neue Workflowprozesse mithilfe der Workflowprozessvorlagen:</span><span class="sxs-lookup"><span data-stu-id="f019b-113">Create new workflow processes using the workflow process templates:</span></span> 
    1. <span data-ttu-id="f019b-114">Erstellen Sie einen neuen Workflowprozess für die Entität **Lieferant** mithilfe der Workflowprozessvorlage **Lieferanten in der Kontoentität erstellen** und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="f019b-114">Create a new workflow process for the **Vendor** entity using the **Create Vendors in Account Entity** workflow process template and click **OK**.</span></span> <span data-ttu-id="f019b-115">Dieser Workflow verarbeitet das Lieferantenerstellungsszenario für die Entität **Konto**.</span><span class="sxs-lookup"><span data-stu-id="f019b-115">This workflow handles the vendor creation scenario for the **Account** entity.</span></span>
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="f019b-116">![Lieferanten in der Kontoentität erstellen](media/dual-write-switch-4.png)</span><span class="sxs-lookup"><span data-stu-id="f019b-116">![Create Vendors in Account Entity](media/dual-write-switch-4.png)</span></span>
    2. <span data-ttu-id="f019b-117">Erstellen Sie einen neuen Workflowprozess für die Entität **Lieferant** mithilfe der Workflowprozessvorlage **Kontoentität aktualisieren** und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="f019b-117">Create a new workflow process for the **Vendor** entity using the **Update Accounts Entity** workflow process template and click **OK**.</span></span> <span data-ttu-id="f019b-118">Dieser Workflow verarbeitet das Lieferantenaktualisierungsszenario für die Entität **Konto**.</span><span class="sxs-lookup"><span data-stu-id="f019b-118">This workflow handles the vendor update scenario for the **Account** entity.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="f019b-119">![Kontoentität aktualisieren](media/dual-write-switch-5.png)</span><span class="sxs-lookup"><span data-stu-id="f019b-119">![Update Accounts Entity](media/dual-write-switch-5.png)</span></span>
    3. <span data-ttu-id="f019b-120">Erstellen Sie neue Workflowprozesse aus den Vorlagen, die in der Entität **Konten** erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="f019b-120">Create new workflow processes from the templates created on the **Accounts** entity.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="f019b-121">![Lieferanten in der Kontoentität erstellen](media/dual-write-switch-6.png)
        > </span><span class="sxs-lookup"><span data-stu-id="f019b-121">![Create vendors in vendors entity](media/dual-write-switch-6.png)
        > </span></span>[!div class="mx-imgBorder"]
<span data-ttu-id="f019b-122">![Lieferantenentität aktualisieren](media/dual-write-switch-7.png)</span><span class="sxs-lookup"><span data-stu-id="f019b-122">![Update vendors entity](media/dual-write-switch-7.png)</span></span>
    4. <span data-ttu-id="f019b-123">Sie können die Workflow als Echtzeit- oder Hintergrundworkflows je nach Ihren Anforderungen konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="f019b-123">You can configure the workflows as real-time or background workflows based on your requirements.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="f019b-124">![In einen Hintergrundworkflow konvertieren](media/dual-write-switch-8.png)</span><span class="sxs-lookup"><span data-stu-id="f019b-124">![Convert to a background workflow](media/dual-write-switch-8.png)</span></span>
    5. <span data-ttu-id="f019b-125">Aktivieren Sie die Workflows, die Sie in den Entitäten **Konto** und **Kreditor** erstellt haben, um mit der Verwendung der Entität **Konto** für das Speichern von Kreditoreninformationen zu starten.</span><span class="sxs-lookup"><span data-stu-id="f019b-125">Activate the workflows that you created on the **Account** and **Vendor** entities to start using the **Account** entity for storing vendor information.</span></span> 
 
