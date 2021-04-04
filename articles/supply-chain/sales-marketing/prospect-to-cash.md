---
title: Interessent zu Bargeld
description: Dieses Thema enthält einen Überblick der Prospect to Cash-Lösung zwischen Dynamics 365 Supply Chain Management und Dynamics 365 Sales.
author: ChristianRytt
manager: tfehr
ms.date: 04/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, SalesTable, EcoResProductListPage
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 70ea2638408296df283a030dedce03b22cb57d81
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5248738"
---
# <a name="prospect-to-cash"></a><span data-ttu-id="6b6c2-103">Prospect-to-Cash</span><span class="sxs-lookup"><span data-stu-id="6b6c2-103">Prospect to cash</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6b6c2-104">Die Prospect to Cash-Lösung bietet direkte Synchronisierung zwischen Dynamics 365 Supply Chain Management und Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="6b6c2-104">The Prospect to cash solution provides direct synchronization across Dynamics 365 Supply Chain Management and Dynamics 365 Sales.</span></span> <span data-ttu-id="6b6c2-105">Die „Interessent zu Bargeld”-Vorlagen, die über die Datenintegrationsfunktion verfügbar sind, ermöglichen den Fluss von Konten, Kontakten, Produkten, Verkaufsangeboten, Aufträgen und Verkaufsrechnungen.</span><span class="sxs-lookup"><span data-stu-id="6b6c2-105">The Prospect to cash templates that are available with the Data Integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices.</span></span> <span data-ttu-id="6b6c2-106">Während die Daten fließen, können Sie Vertriebs- und Marketingaktivitäten zwischen Finance and Operations und Sales ausführen und die Auftagserfüllung mit Bestandsverwaltung in Supply Chain Management handhaben.</span><span class="sxs-lookup"><span data-stu-id="6b6c2-106">While data is flowing, you can perform sales and marketing activities in Sales, and you can handle order fulfillment by using inventory management in Supply Chain Management.</span></span> 

<span data-ttu-id="6b6c2-107">Für weitere Informationen über die Integration Prospect to Cash sehen Sie sich das kurze YouTube-Video an: [Integration von Prospect to Cash](https://www.youtube.com/watch?v=AVV9x5x-XCg).</span><span class="sxs-lookup"><span data-stu-id="6b6c2-107">For more information about the Prospect to cash integration, watch the short YouTube video [Prospect to cash integration](https://www.youtube.com/watch?v=AVV9x5x-XCg).</span></span>

<span data-ttu-id="6b6c2-108">In der aktuellen Version enthält die Interessent in Bargeldlösung die folgenden Typen der direkten Synchronisierung:</span><span class="sxs-lookup"><span data-stu-id="6b6c2-108">In the current version, the Prospect to cash solution provides the following types of direct synchronization:</span></span>

- [<span data-ttu-id="6b6c2-109">Konten direkt von Sales mit Konten in Supply Chain Management synchronisieren</span><span class="sxs-lookup"><span data-stu-id="6b6c2-109">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)
- [<span data-ttu-id="6b6c2-110">Produkte direkt von Supply Chain Management mit Produkten in Sales synchronisieren</span><span class="sxs-lookup"><span data-stu-id="6b6c2-110">Synchronize products directly from Supply Chain Management to products in Sales</span></span>](products-template-mapping-direct.md)
- [<span data-ttu-id="6b6c2-111">Kontakte direkt von Sales mit Kontakten oder Debitoren in Supply Chain Management synchronisieren</span><span class="sxs-lookup"><span data-stu-id="6b6c2-111">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>](contacts-template-mapping-direct.md)
- [<span data-ttu-id="6b6c2-112">Verkaufsangebotskopfzeilen und ‑positionen direkt von Sales zu Supply Chain Management synchronisieren</span><span class="sxs-lookup"><span data-stu-id="6b6c2-112">Synchronize sales quotation headers and lines directly from Sales to Supply Chain Management</span></span>](sales-quotation-template-mapping-sales-fin.md)
- [<span data-ttu-id="6b6c2-113">Synchronisieren von Aufträgen direkt zwischen Sales und Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="6b6c2-113">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)
- [<span data-ttu-id="6b6c2-114">Rechnungskopfzeilen und ‑positionen direkt von Supply Chain Management zu Sales synchronisieren</span><span class="sxs-lookup"><span data-stu-id="6b6c2-114">Synchronize sales invoice headers and lines directly from Supply Chain Management to Sales</span></span>](sales-invoice-template-mapping-direct.md)

## <a name="system-requirements-for-supply-chain-management"></a><span data-ttu-id="6b6c2-115">Systemanforderungen für Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="6b6c2-115">System requirements for Supply Chain Management</span></span>
<span data-ttu-id="6b6c2-116">„Interessent zu Bargeld”-Integration wird in den folgenden Versionen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="6b6c2-116">Prospect to cash integration is supported on the following versions:</span></span>

### <a name="microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-73-december-2017"></a><span data-ttu-id="6b6c2-117">Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3 (Dezember 2017)</span><span class="sxs-lookup"><span data-stu-id="6b6c2-117">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 (December 2017)</span></span>

- <span data-ttu-id="6b6c2-118">Dynamics 365 for Finance and Operations, Enterprise Edition (Dezember 2017) - Anwendungserstellung 7.3.11971.56116 mit Plattform-Update 12 (7.0.4709.41129)</span><span class="sxs-lookup"><span data-stu-id="6b6c2-118">Dynamics 365 for Finance and Operations, Enterprise edition (December 2017) - Application build 7.3.11971.56116 with Platform Update 12 (7.0.4709.41129)</span></span>

### <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a><span data-ttu-id="6b6c2-119">Dynamics 365 for Finance and Operations, Enterprise Edition (Juli 2017)</span><span class="sxs-lookup"><span data-stu-id="6b6c2-119">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017)</span></span>

- <span data-ttu-id="6b6c2-120">Dynamics 365 for Finance and Operations, Enterprise Edition (Juli 2017) - mit Plattformupdate 8 (Anwendungserstellung 7.2.11792.56024 mit Plattformbuild 7.0.4565.16212).</span><span class="sxs-lookup"><span data-stu-id="6b6c2-120">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) - with platform update 8 (application build 7.2.11792.56024 with platform build 7.0.4565.16212).</span></span>
- <span data-ttu-id="6b6c2-121">Die folgenden Hotfixes sind erforderlich:</span><span class="sxs-lookup"><span data-stu-id="6b6c2-121">The following hotfixes are required:</span></span>

  - <span data-ttu-id="6b6c2-122">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** Dieser Hotfix aktiviert die Auftragspositionssynchronisierung von Sales zu Supply Chain Management über die Datenintegrationsfunktion.</span><span class="sxs-lookup"><span data-stu-id="6b6c2-122">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – This hotfix enables sales order synchronization from Sales to Supply Chain Management via the Data Integration feature.</span></span> <span data-ttu-id="6b6c2-123">Er enthält auch einige anderen Erweiterungen.</span><span class="sxs-lookup"><span data-stu-id="6b6c2-123">It also provides several other enhancements.</span></span>
  - <span data-ttu-id="6b6c2-124">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** Dieser Hotfix aktiviert die Auftragspositionssynchronisierung von Supply Chain Management zu Sales über die Datenintegrationsfunktion.</span><span class="sxs-lookup"><span data-stu-id="6b6c2-124">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order line synchronization from Supply Chain Management to Sales via the Data Integration feature.</span></span>
  - <span data-ttu-id="6b6c2-125">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** Dieser Hotfix aktiviert die Auftragspositionssynchronisierung von Supply Chain Management zu Sales über die Datenintegrationsfunktion.</span><span class="sxs-lookup"><span data-stu-id="6b6c2-125">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order synchronization from Supply Chain Management to Sales via the Data Integration feature.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6b6c2-126">Sie müssen nur KB4045570 installieren, da diese Installation die Änderungen aus anderen Hotfixes enthält.</span><span class="sxs-lookup"><span data-stu-id="6b6c2-126">You only have to install KB4045570 because the installation includes the changes from other hotfixes.</span></span> 

### <a name="dynamics-365-for-finance-and-operations-version-1611-november-2016"></a><span data-ttu-id="6b6c2-127">Dynamics 365 for Finance and Operations Version 1611 (November 2016)</span><span class="sxs-lookup"><span data-stu-id="6b6c2-127">Dynamics 365 for Finance and Operations version 1611 (November 2016)</span></span>

- <span data-ttu-id="6b6c2-128">Dynamics 365 for Finance and Operations-Version 1611 (November 2016) mit Plattformaktualisierung 8 oder höher</span><span class="sxs-lookup"><span data-stu-id="6b6c2-128">Dynamics 365 for Finance and Operations version 1611 (November 2016)  with platform update 8 or higher</span></span>

- <span data-ttu-id="6b6c2-129">Die folgenden Hotfixes sind erforderlich:</span><span class="sxs-lookup"><span data-stu-id="6b6c2-129">The following hotfixes are required:</span></span>

  - <span data-ttu-id="6b6c2-130">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** – Aktiviert Auftragssynchronisierung mit Datenenintegrator von Supply Chain Management zu Sales.</span><span class="sxs-lookup"><span data-stu-id="6b6c2-130">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Enable sales order synchronization with Data integrator from Supply Chain Management to Sales.</span></span> 
  - <span data-ttu-id="6b6c2-131">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** – Aktiviert Synchronisierung von Auftragskopfzeilen und -positionen mit Datenenintegrator von Supply Chain Management zu Sales.</span><span class="sxs-lookup"><span data-stu-id="6b6c2-131">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Enable sales order header and line synchronization with Data integrator from Supply Chain Management to Sales.</span></span>
  - <span data-ttu-id="6b6c2-132">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** – Unterstützung für die Integration von „Interessent zu Bargeld” durch Datenentitäten ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6b6c2-132">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Support for prospect to cash integration through data entities is required.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="6b6c2-133">Nachdem Sie die Hotfixes installiert haben, müssen Sie die folgende Stapelverarbeitung vom Formular **SalesPopulateProspectToCash** auslösen.</span><span class="sxs-lookup"><span data-stu-id="6b6c2-133">After you install the hotfixes, you must trigger the following batch job from the **SalesPopulateProspectToCash** form.</span></span> <span data-ttu-id="6b6c2-134">Dieses Formular wird ausgeblendet, da Sie es nur einmal benötigen.</span><span class="sxs-lookup"><span data-stu-id="6b6c2-134">This form is hidden because you only need it once.</span></span> <span data-ttu-id="6b6c2-135">Um auf das Formular zuzugreifen, fügen Sie Folgendes der Browseradresse hinzu, wenn Sie sich bei der Umgebung angemeldet haben: *&mi=action:SalesPopulateProspectToCash*, beispielsweise `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`.</span><span class="sxs-lookup"><span data-stu-id="6b6c2-135">To access the form, log in to the environment and add the following to the URL in your browser address: *&mi=action:SalesPopulateProspectToCash*, for example, `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`.</span></span> <span data-ttu-id="6b6c2-136">Wenn das Formular geöffnet wird, klicken Sie auf OK.</span><span class="sxs-lookup"><span data-stu-id="6b6c2-136">When the form opens, click OK.</span></span> <span data-ttu-id="6b6c2-137">Dadurch wird ein neues Feld **LineCreationSequnceNumber** in den Tabellen **SalesLine**, **SalesQuotationLine** und **CustInvoiceTrans** mit eindeutigen Werte ergänzt, und die Produktliste wird aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="6b6c2-137">This will populate a new **LineCreationSequnceNumber** field in the **SalesLine**, **SalesQuotationLine**, and **CustInvoiceTrans** tables with unique values, and the product list will be refreshed.</span></span> <span data-ttu-id="6b6c2-138">Dies ist erforderlich, damit die „Interessent zu Bargeld”-Integration funktioniert.</span><span class="sxs-lookup"><span data-stu-id="6b6c2-138">This is required for the Prospect to cash integration to work.</span></span>


## <a name="system-requirements-for-sales"></a><span data-ttu-id="6b6c2-139">Systemanforderungen für Sales</span><span class="sxs-lookup"><span data-stu-id="6b6c2-139">System requirements for Sales</span></span>

<span data-ttu-id="6b6c2-140">Um die Interessent zu Bargeld-Lösung zu nutzen, müssen Sie Folgendes installieren:</span><span class="sxs-lookup"><span data-stu-id="6b6c2-140">To use the Prospect to cash solution, you must install the following components:</span></span>

- <span data-ttu-id="6b6c2-141">Dynamics 365 Sales-Version 1612 (8.2.1.207) (DB 8.2.1.207) online oder höher.</span><span class="sxs-lookup"><span data-stu-id="6b6c2-141">Dynamics 365 Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online or a later version</span></span>
- <span data-ttu-id="6b6c2-142">Interessent zu Bargeld-Lösung für Dynamics 365 Sales, Version 1.15.0.0 oder eine spätere Version.</span><span class="sxs-lookup"><span data-stu-id="6b6c2-142">Prospect to cash solution for Dynamics 365 Sales, version 1.15.0.0 or a later version.</span></span> <span data-ttu-id="6b6c2-143">Die Lösung ist aus AppSource zum Download verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6b6c2-143">The solution is available for download from AppSource.</span></span> <span data-ttu-id="6b6c2-144">[Laden Sie Dynamics 365, Prospect to Cash herunter](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span><span class="sxs-lookup"><span data-stu-id="6b6c2-144">[Download Dynamics 365, Prospect to Cash](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]