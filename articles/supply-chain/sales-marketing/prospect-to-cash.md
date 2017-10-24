---
title: Interessent zu Bargeld
description: "Das Thema bietet eine Übersicht der Lösung „Interessent zu Bargeld” zwischen Dynamics 365 for Finance and Operations, Enterprise Edition, und Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: a5f1ecd5f8b46287839439a963e571531ae161a7
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="prospect-to-cash"></a><span data-ttu-id="6ac1e-103">Interessent zu Bargeld</span><span class="sxs-lookup"><span data-stu-id="6ac1e-103">Prospect to cash</span></span>  

[!include[banner](../includes/banner.md)]

<span data-ttu-id="6ac1e-104">Die Lösung „Interessent zu Bargeld” verwendet [Datenintegration](/common-data-service/entity-reference/dynamics-365-integration), um Daten über Instanzen von Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, und Dynamics 365 for Sales hinweg mit dem Common Data Service (CDC) zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="6ac1e-104">The Prospect to cash solution uses [Data Integration](/common-data-service/entity-reference/dynamics-365-integration) to synchronize data across Microsoft Dynamics 365 for Finance and Operations, Enterprise edition and Dynamics 365 for Sales instances via the Common Data Service (CDS).</span></span> <span data-ttu-id="6ac1e-105">Die „Interessent zu Bargeld”-Vorlagen, die über die Datenintegrationsfunktion verfügbar sind, ermöglichen den Fluss von Konten, Kontakten, Produkten, Verkaufsangeboten, Aufträgen und Verkaufsrechnungen zwischen Finance and Operations und Sales.</span><span class="sxs-lookup"><span data-stu-id="6ac1e-105">The Prospect to cash templates available with the Data Integration feature enable the flow of accounts, contacts, products, sales quotes, sales orders, and sales invoices data between Finance and Operations and Sales.</span></span> <span data-ttu-id="6ac1e-106">Während die Daten zwischen Finance and Operations und Sales fließen, können Sie Vertriebs- und Marketingaktivitäten in Dynamics 365 for Sales ausführen und die Auftagserfüllung mit Bestandsverwaltung in Finance and Operations handhaben.</span><span class="sxs-lookup"><span data-stu-id="6ac1e-106">While the data is flowing between Finance and Operations and Sales, you can carry out sales and marketing activities in Sales and handle the order fulfillment with inventory management in Finance and Operations.</span></span> 

<span data-ttu-id="6ac1e-107">Diese Lösung bietet Integration in den folgenden Bereichen:</span><span class="sxs-lookup"><span data-stu-id="6ac1e-107">This solution provides integration in the following areas:</span></span> 

-   [<span data-ttu-id="6ac1e-108">Konten in Sales verwalten und mit Finance and Operations synchronisieren</span><span class="sxs-lookup"><span data-stu-id="6ac1e-108">Maintain accounts in Sales and sync them to Finance and Operations</span></span>](accounts-template-mapping.md)
-   [<span data-ttu-id="6ac1e-109">Kontakte in Sales verwalten und mit Finance and Operations synchronisieren</span><span class="sxs-lookup"><span data-stu-id="6ac1e-109">Maintain contacts in Sales and sync them to Finance and Operations</span></span>](contacts-template-mapping.md)
-   [<span data-ttu-id="6ac1e-110">Produkte in Finance and Operations verwalten und mit Sales synchronisieren</span><span class="sxs-lookup"><span data-stu-id="6ac1e-110">Maintain products in Finance and Operations and sync them to Sales</span></span>](products-template-mapping.md)
-   [<span data-ttu-id="6ac1e-111">Verkaufsangebote in Sales erstellen und mit Finance and Operations synchronisieren</span><span class="sxs-lookup"><span data-stu-id="6ac1e-111">Create sales quotes in Sales and sync them to Finance and Operations</span></span>](sales-quotation-template-mapping.md)
-   [<span data-ttu-id="6ac1e-112">Verkaufsaufträge in Finance and Operations erstellen und mit Sales synchronisieren</span><span class="sxs-lookup"><span data-stu-id="6ac1e-112">Create sales orders in Finance and Operations and sync them to Sales</span></span>](sales-order-template-mapping.md)
-   [<span data-ttu-id="6ac1e-113">Verkaufsrechnungen in Finance and Operations erstellen und mit Sales synchronisieren</span><span class="sxs-lookup"><span data-stu-id="6ac1e-113">Create sales invoices in Finance and Operations and sync them to Sales</span></span>](sales-invoice-template-mapping.md)

## <a name="system-requirements-for-dynamics-365-for-finance-and-operations-enterprise-edition"></a><span data-ttu-id="6ac1e-114">Systemanforderungen für Dynamics 365 for Finance and Operations, Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="6ac1e-114">System requirements for Dynamics 365 for Finance and Operations, Enterprise edition</span></span>

<span data-ttu-id="6ac1e-115">Um die Interessent zu Bargeld-Lösung zu nutzen, müssen Sie Folgendes installieren:</span><span class="sxs-lookup"><span data-stu-id="6ac1e-115">To use the Prospect to cash solution, you must install the following:</span></span>

- <span data-ttu-id="6ac1e-116">Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (Juli 2017) mit Plattform-Update 8 (App 7.2.11792.56024 w/ Plattform 7.0.4565.16212)</span><span class="sxs-lookup"><span data-stu-id="6ac1e-116">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) with Platform update 8 (App 7.2.11792.56024 w/ Platform 7.0.4565.16212)</span></span>

- <span data-ttu-id="6ac1e-117">Zwei Hotfixes für Dynamics 365 for Finance and Operations, Enterprise Edition (Juli 2017).</span><span class="sxs-lookup"><span data-stu-id="6ac1e-117">Two hotfixes for Dynamics 365 for Finance and Operations, Enterprise edition (July 2017).</span></span>

    -  <span data-ttu-id="6ac1e-118">[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) – Dieser Hotfix aktiviert die Auftragspositionssynchronisierung mit der Datenintegrationsfunktion zwischen Finance and Operations und Sales.</span><span class="sxs-lookup"><span data-stu-id="6ac1e-118">[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - This hotfix enables sales order line synchronization with the Data Integration feature from Finance and Operations to Sales.</span></span>
        
    -  <span data-ttu-id="6ac1e-119">[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) – Dieser Hotfix aktiviert die Auftragspositionssynchronisierung mit der Datenintegrationsfunktion zwischen Finance and Operations und Sales.</span><span class="sxs-lookup"><span data-stu-id="6ac1e-119">[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - This hotfix enables sales order synchronization with the Data Integration feature from Finance and Operations to Sales.</span></span>
    
<span data-ttu-id="6ac1e-120">**Hinweis**: Sie müssen nur KB4036524 installieren, da diese Installation Änderungen aus KB4036461 enthält.</span><span class="sxs-lookup"><span data-stu-id="6ac1e-120">**Note**: You only need to install KB4036524 because the installation includes the changes from KB4036461.</span></span>
 
## <a name="system-requirements-for-dynamics-365-for-sales"></a><span data-ttu-id="6ac1e-121">Systemanforderungen für Dynamics 365 for Sales</span><span class="sxs-lookup"><span data-stu-id="6ac1e-121">System requirements for Dynamics 365 for Sales</span></span>

<span data-ttu-id="6ac1e-122">Um die Interessent zu Bargeld-Lösung zu nutzen, müssen Sie Folgendes installieren:</span><span class="sxs-lookup"><span data-stu-id="6ac1e-122">To use the Prospect to cash solution, you must install the following:</span></span>

- <span data-ttu-id="6ac1e-123">Dynamics 365 for Sales, Version 1612 (8.2.1.207) (DB 8.2.1.207) online oder höher.</span><span class="sxs-lookup"><span data-stu-id="6ac1e-123">Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online or later.</span></span>
- <span data-ttu-id="6ac1e-124">Interessent zu Bargeld-Lösung für Dynamics 365 for Sales, Version 1.14.0.0 (v14) oder höher.</span><span class="sxs-lookup"><span data-stu-id="6ac1e-124">Prospect to cash solution for Dynamics 365 for Sales, version 1.14.0.0 (v14) or later.</span></span>

### <a name="install-the-prospect-to-cash-solution-for-sales"></a><span data-ttu-id="6ac1e-125">Installieren der Interessent zu Bargeld-Lösung für Sales</span><span class="sxs-lookup"><span data-stu-id="6ac1e-125">Install the Prospect to cash solution for Sales</span></span>

- <span data-ttu-id="6ac1e-126">Laden Sie die [Interessent zu Bargeld-Lösungspaket-ZIP-Datei für Dynamics 365 for Sales](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) von CustomerSource herunter.</span><span class="sxs-lookup"><span data-stu-id="6ac1e-126">Download the [Prospect to cash for Dynamics 365 for Sales solution package zip file](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) on CustomerSource.</span></span>

- <span data-ttu-id="6ac1e-127">Stellen Sie sicher, dass die ZIP-Datei nicht gesperrt ist, damit Sie beim Installieren des Lösungspakets keine Fehlermeldung erhalten, die besagt, dass keine Importpakete gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="6ac1e-127">Make sure that the zip file is unblocked so that you do not get the error message "No import packages were found" when you install the solution package.</span></span> <span data-ttu-id="6ac1e-128">Führen Sie die folgenden Schritte aus, um die Datei zu entsperren:</span><span class="sxs-lookup"><span data-stu-id="6ac1e-128">To unblock the file, do the following:</span></span>

    -  <span data-ttu-id="6ac1e-129">Klicken Sie mit der rechten Maustaste auf die ZIP-Datei.</span><span class="sxs-lookup"><span data-stu-id="6ac1e-129">Right-click the zip file.</span></span>
    -  <span data-ttu-id="6ac1e-130">Wählen Sie **Eigenschaften** und **Entsperren** aus.</span><span class="sxs-lookup"><span data-stu-id="6ac1e-130">Select **Properties** and then select **Unblock**.</span></span> 

- <span data-ttu-id="6ac1e-131">Entpacken Sie die Datei, und führen Sie PackageDeployer.exe aus.</span><span class="sxs-lookup"><span data-stu-id="6ac1e-131">Unzip and run PackageDeployer.exe.</span></span>

- <span data-ttu-id="6ac1e-132">Installieren Sie die Interessent zu Bargeld-Cash-Lösung auf Ihrer Sales-Instance.</span><span class="sxs-lookup"><span data-stu-id="6ac1e-132">Install the Prospect to Cash solution in your Sales instance.</span></span>

    - <span data-ttu-id="6ac1e-133">Wählen Sie den **Office 365**-Bereitstellungstyp aus.</span><span class="sxs-lookup"><span data-stu-id="6ac1e-133">Select the **Office 365** Deployment type.</span></span>
    - <span data-ttu-id="6ac1e-134">Wählen Sie die Option zum **Anzeigen von Erweiterungen** aus.</span><span class="sxs-lookup"><span data-stu-id="6ac1e-134">Select **Show advanced**.</span></span>
    - <span data-ttu-id="6ac1e-135">Wählen Sie für eine schnelle Installation **Region** aus.</span><span class="sxs-lookup"><span data-stu-id="6ac1e-135">For a quick installation, select a **Region**.</span></span> <span data-ttu-id="6ac1e-136">Wenn Sie **Ich weiß nicht** auswählen, sucht das System nach allen Regionen und die Installation dauert länger.</span><span class="sxs-lookup"><span data-stu-id="6ac1e-136">If you select **Don’t know**, the system searches for all regions and it will take longer to install.</span></span>
    - <span data-ttu-id="6ac1e-137">Geben Sie **Benutzername** und **Kennwort** für einen Administratorbenutzer ein, der über Benutzerrechte zum Installieren verfügt.</span><span class="sxs-lookup"><span data-stu-id="6ac1e-137">Enter **User name** and **Password** for an admin user who has the user rights to install.</span></span>

