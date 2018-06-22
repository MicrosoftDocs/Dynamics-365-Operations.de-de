---
title: Integration mit Microsoft Dynamics 365 for Field Service
description: "Dieses Thema bietet einen Überblick über die Integration mit Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 04/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: a57e23691a6b4d48c6b8dd6d1f61fc9730365b39
ms.openlocfilehash: 0c1268d2fddcf7b28ecfc3197f21e9d30a5a5855
ms.contentlocale: de-de
ms.lasthandoff: 05/31/2018

---


# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a><span data-ttu-id="20934-103">Integration mit Microsoft Dynamics 365 for Field Service</span><span class="sxs-lookup"><span data-stu-id="20934-103">Integration with Microsoft Dynamics 365 for Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="20934-104">Microsoft Dynamics 365 for Finance and Operations ermöglicht die Synchronisierung von Geschäftsprozessen zwischen Finance and Operations und Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="20934-104">Microsoft Dynamics 365 for Finance and Operations enables synchronization of business processes between Finance and Operations and Microsoft Dynamics 365 for Field Service.</span></span> <span data-ttu-id="20934-105">Die Integrationsszenarien werden mithilfe erweiterbarer Datenintegratorvorlagen und des Common Data Service (CDS) konfiguriert, um die Synchronisierung von Geschäftsprozessen zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="20934-105">The integration scenarios are configured by using extensible Data integrator templates and the Common Data Service (CDS) to enable the synchronization of business processes.</span></span>

<span data-ttu-id="20934-106">[![Synchronisierung von Geschäftsprozessen zwischen Finance and Operations und Field Service](./media/field-service-integration.png)](./media/field-service-integration.png)</span><span class="sxs-lookup"><span data-stu-id="20934-106">[![Synchronization of business processes between Finance and Operations and Field Service](./media/field-service-integration.png)](./media/field-service-integration.png)</span></span>

<span data-ttu-id="20934-107">Die erste Phase der Integration zwischen Field Service und Finance and Operations konzentriert sich darauf zu ermöglichen, dass Arbeitsaufträge und Vereinbarungen aus Field Service in Finance and Operations fakturiert werden.</span><span class="sxs-lookup"><span data-stu-id="20934-107">The first phase  of the integration between Field Service and Finance and Operations is focused on enabling work orders and agreements in Field Service to be invoiced in Finance and Operations.</span></span> <span data-ttu-id="20934-108">Die unterstützten Flüsse beginnen in Field Service, wo Informationen aus Arbeitsaufträgen mit Finance and Operations als Aufträge synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="20934-108">The supported flow starts in Field Service, where information from work orders is synchronized to Finance and Operations as sales orders.</span></span> <span data-ttu-id="20934-109">In Finance and Operations werden die Aufträge fakturiert, um Rechnungsdokumente zu generieren.</span><span class="sxs-lookup"><span data-stu-id="20934-109">In Finance and Operations, the sales orders are invoiced to generate invoice documents.</span></span> <span data-ttu-id="20934-110">Darüber hinaus werden die Informationen aus Field Service-Vereinbarungsrechnungen mit Finance and Operations synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="20934-110">In addition, the information from Field Service agreement invoices is synchronized to Finance and Operations.</span></span> <span data-ttu-id="20934-111">Der Microsoft Dynamics 365-Datenenintegrator synchronisiert Daten mithilfe von anpassbaren Projekten.</span><span class="sxs-lookup"><span data-stu-id="20934-111">The Microsoft Dynamics 365 Data integrator synchronizes data by using customizable projects.</span></span> <span data-ttu-id="20934-112">Standardvorlagen können verwendet werden, um benutzerdefinierte Integrationsprojekte zu erstellen, in denen zusätzliche standardmäßige und benutzerdefinierte Felder sowie auch Entitäten zugeordnet werden können, um die Integration anzupassen und bestimmte Anforderungen zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="20934-112">Standard templates can be used to create custom integration projects where additional standard and custom fields, and also entities, can be mapped to adjust the integration and meet specific requirements.</span></span>

<span data-ttu-id="20934-113">Die erste Phase der Integration zwischen Field Service und Finance and Operations ermöglicht die Synchronisierung der folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="20934-113">The first phase of the integration between Field Service and Finance and Operations enables synchronization of the following items:</span></span>

- [<span data-ttu-id="20934-114">Produkte in Finance and Operations mit Produkten in Field Service, die Produkttypinformationen enthalten</span><span class="sxs-lookup"><span data-stu-id="20934-114">Products in Finance and Operations to products in Field Service that include Product Type information</span></span>](field-service-product.md)
- [<span data-ttu-id="20934-115">Arbeitsaufträge in Field Service mit Aufträgen in Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="20934-115">Work orders in Field Service to sales orders in Finance and Operations</span></span>](field-service-work-order.md)
- [<span data-ttu-id="20934-116">Rechnungen in Field Service mit Freitextrechnungen in Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="20934-116">Invoices in Field Service to free text invoices in Finance and Operations</span></span>](field-service-invoice.md)

<span data-ttu-id="20934-117">Um ein Beispiel zu sehen, wie Sie einen Arbeitsauftrag zwischen Field Service und Finance and Operations synchronisieren können, sehen Sie sich das kurze YouTube-Video [Arbeitsaufträge zwischen Dynamics 365 for Field Service und Finance and Operations synchronisieren](https://www.youtube.com/watch?v=hAB4TDVMjxU) an.</span><span class="sxs-lookup"><span data-stu-id="20934-117">To see an example of how you can synchronize a work order between Field Service and Finance and Operations, watch the short YouTube video [Synchronize a work order between Dynamics 365 for Field Service and Finance and Operations](https://www.youtube.com/watch?v=hAB4TDVMjxU).</span></span>

[![](https://img.youtube.com/vi/hAB4TDVMjxU/0.jpg)](https://www.youtube.com/watch?v=hAB4TDVMjxU)

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="20934-118">Systemanforderungen für Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="20934-118">System requirements for Finance and Operations</span></span>
<span data-ttu-id="20934-119">Field Service-Integration unterstützt die folgenden Versionen:</span><span class="sxs-lookup"><span data-stu-id="20934-119">Field Service integration supports the following versions:</span></span>

### <a name="dynamics-365-for-finance-and-operations-version-80-april-2018-or-later"></a><span data-ttu-id="20934-120">Dynamics 365 for Finance and Operations Version 8.0 (April 2018) oder höher</span><span class="sxs-lookup"><span data-stu-id="20934-120">Dynamics 365 for Finance and Operations version 8.0 (April 2018) or later</span></span>

- <span data-ttu-id="20934-121">Dynamics 365 for Finance and Operations Version 8.0 (April 2018) wurde im April 2018 veröffentlicht und hat die Anwendungserstellungsnummer 8.0.30.8020 mit Plattformupdate 15 (7.0.4841.35234).</span><span class="sxs-lookup"><span data-stu-id="20934-121">Dynamics 365 for Finance and Operations version 8.0 (April 2018) was released in April 2018 and has an application build number 8.0.30.8020 with Platform Update 15 (7.0.4841.35234).</span></span> 

## <a name="system-requirements-for-field-service"></a><span data-ttu-id="20934-122">Systemanforderungen für Field Service</span><span class="sxs-lookup"><span data-stu-id="20934-122">System requirements for Field Service</span></span>
<span data-ttu-id="20934-123">Um die Field Service-Integrationslösung zu nutzen, müssen Sie Folgendes installieren:</span><span class="sxs-lookup"><span data-stu-id="20934-123">To use the Field Service integration solution, you must install the following components:</span></span>

### <a name="microsoft-dynamics-365-for-field-service-90-or-later"></a><span data-ttu-id="20934-124">Microsoft Dynamics 365 for Field Service 9.0 oder höher</span><span class="sxs-lookup"><span data-stu-id="20934-124">Microsoft Dynamics 365 for Field Service 9.0 or later</span></span>

- <span data-ttu-id="20934-125">Dynamics 365 for Field Service Version 1612 (9.0.1.733) (DB 9.0.1.733) online oder eine spätere Version.</span><span class="sxs-lookup"><span data-stu-id="20934-125">Dynamics 365 for Field Service version 1612 (9.0.1.733) (DB 9.0.1.733) online or a later version.</span></span>
- <span data-ttu-id="20934-126">Interessent zu Bargeld (P2C)-Lösung für Dynamics 365, Version 1.15.0.1 oder eine spätere Version.</span><span class="sxs-lookup"><span data-stu-id="20934-126">Prospect to Cash (P2C) solution for Dynamics 365, version 1.15.0.1 or a later version.</span></span> <span data-ttu-id="20934-127">Die Lösung ist unter [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3) zum Download verfügbar.</span><span class="sxs-lookup"><span data-stu-id="20934-127">The solution is available for download from [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span></span>
- <span data-ttu-id="20934-128">Field Service-Integrationslösung für Dynamics 365, Version 1.0.0.0 oder eine spätere Version.</span><span class="sxs-lookup"><span data-stu-id="20934-128">Field Service integration solution for Dynamics 365, version 1.0.0.0 or a later version.</span></span> <span data-ttu-id="20934-129">Die Lösung ist unter [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.p2cfieldserviceintegration) zum Download verfügbar.</span><span class="sxs-lookup"><span data-stu-id="20934-129">The solution is available for download from [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.p2cfieldserviceintegration).</span></span>

