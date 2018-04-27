---
title: Integration mit Microsoft Dynamics 365 for Field Service
description: "Dieses Thema bietet einen Überblick über die Integration mit Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 04/10/2018
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
ms.sourcegitcommit: d32a4e376770fc73c79b94924d5ae062d201d84a
ms.openlocfilehash: a224962152e80293f6cf3425dea74d73a283e31a
ms.contentlocale: de-de
ms.lasthandoff: 04/12/2018

---


# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a><span data-ttu-id="0a3f1-103">Integration mit Microsoft Dynamics 365 for Field Service</span><span class="sxs-lookup"><span data-stu-id="0a3f1-103">Integration with Microsoft Dynamics 365 for Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="0a3f1-104">Microsoft Dynamics 365 for Finance and Operations ermöglicht die Synchronisierung von Geschäftsprozessen zwischen Finance and Operations und Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="0a3f1-104">Microsoft Dynamics 365 for Finance and Operations enables synchronization of business processes between Finance and Operations and Microsoft Dynamics 365 for Field Service.</span></span> <span data-ttu-id="0a3f1-105">Die Integrationsszenarien werden mithilfe erweiterbarer Datenintegratorvorlagen und des Common Data Service (CDS) konfiguriert, um die Synchronisierung von Geschäftsprozessen zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="0a3f1-105">The integration scenarios are configured by using extensible Data integrator templates and the Common Data Service (CDS) to enable the synchronization of business processes.</span></span>

<span data-ttu-id="0a3f1-106">[![Synchronisierung von Geschäftsprozessen zwischen Finance and Operations und Field Service](./media/field-service-integration.png)](./media/field-service-integration.png)</span><span class="sxs-lookup"><span data-stu-id="0a3f1-106">[![Synchronization of business processes between Finance and Operations and Field Service](./media/field-service-integration.png)](./media/field-service-integration.png)</span></span>

<span data-ttu-id="0a3f1-107">Die erste Phase der Integration zwischen Field Service und Finance and Operations konzentriert sich darauf zu ermöglichen, dass Arbeitsaufträge und Vereinbarungen aus Field Service in Finance and Operations fakturiert werden.</span><span class="sxs-lookup"><span data-stu-id="0a3f1-107">The first phase  of the integration between Field Service and Finance and Operations is focused on enabling work orders and agreements in Field Service to be invoiced in Finance and Operations.</span></span> <span data-ttu-id="0a3f1-108">Die unterstützten Flüsse beginnen in Field Service, wo Informationen aus Arbeitsaufträgen mit Finance and Operations als Aufträge synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="0a3f1-108">The supported flow starts in Field Service, where information from work orders is synchronized to Finance and Operations as sales orders.</span></span> <span data-ttu-id="0a3f1-109">In Finance and Operations werden die Aufträge fakturiert, um Rechnungsdokumente zu generieren.</span><span class="sxs-lookup"><span data-stu-id="0a3f1-109">In Finance and Operations, the sales orders are invoiced to generate invoice documents.</span></span> <span data-ttu-id="0a3f1-110">Darüber hinaus werden die Informationen aus Field Service-Vereinbarungsrechnungen mit Finance and Operations synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="0a3f1-110">In addition, the information from Field Service agreement invoices is synchronized to Finance and Operations.</span></span> <span data-ttu-id="0a3f1-111">Der Microsoft Dynamics 365-Datenenintegrator synchronisiert Daten mithilfe von anpassbaren Projekten.</span><span class="sxs-lookup"><span data-stu-id="0a3f1-111">The Microsoft Dynamics 365 Data integrator synchronizes data by using customizable projects.</span></span> <span data-ttu-id="0a3f1-112">Standardvorlagen können verwendet werden, um benutzerdefinierte Integrationsprojekte zu erstellen, in denen zusätzliche standardmäßige und benutzerdefinierte Felder sowie auch Entitäten zugeordnet werden können, um die Integration anzupassen und bestimmte Anforderungen zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="0a3f1-112">Standard templates can be used to create custom integration projects where additional standard and custom fields, and also entities, can be mapped to adjust the integration and meet specific requirements.</span></span>

<span data-ttu-id="0a3f1-113">Die erste Phase der Integration zwischen Field Service und Finance and Operations ermöglicht die Synchronisierung der folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="0a3f1-113">The first phase of the integration between Field Service and Finance and Operations enables synchronization of the following items:</span></span>

- [<span data-ttu-id="0a3f1-114">Produkte in Finance and Operations mit Produkten in Field Service, die Produkttypinformationen enthalten</span><span class="sxs-lookup"><span data-stu-id="0a3f1-114">Products in Finance and Operations to products in Field Service that include Product Type information</span></span>](field-service-product.md)
- [<span data-ttu-id="0a3f1-115">Arbeitsaufträge in Field Service mit Aufträgen in Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="0a3f1-115">Work orders in Field Service to sales orders in Finance and Operations</span></span>](field-service-work-order.md)
- [<span data-ttu-id="0a3f1-116">Rechnungen in Field Service mit Freitextrechnungen in Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="0a3f1-116">Invoices in Field Service to free text invoices in Finance and Operations</span></span>](field-service-invoice.md)

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="0a3f1-117">Systemanforderungen für Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="0a3f1-117">System requirements for Finance and Operations</span></span>
<span data-ttu-id="0a3f1-118">Field Service-Integration unterstützt die folgenden Versionen:</span><span class="sxs-lookup"><span data-stu-id="0a3f1-118">Field Service integration supports the following versions:</span></span>

### <a name="dynamics-365-for-finance-and-operations-version-80-april-2018-or-later"></a><span data-ttu-id="0a3f1-119">Dynamics 365 for Finance and Operations Version 8.0 (April 2018) oder höher</span><span class="sxs-lookup"><span data-stu-id="0a3f1-119">Dynamics 365 for Finance and Operations version 8.0 (April 2018) or later</span></span>

- <span data-ttu-id="0a3f1-120">Dynamics 365 for Finance and Operations Version 8.0 (April 2018) wurde im April 2018 veröffentlicht und hat die Anwendungserstellungsnummer 8.0.30.8020 mit Plattformupdate 15 (7.0.4841.35234).</span><span class="sxs-lookup"><span data-stu-id="0a3f1-120">Dynamics 365 for Finance and Operations version 8.0 (April 2018) was released in April 2018 and has an application build number 8.0.30.8020 with Platform Update 15 (7.0.4841.35234).</span></span> 

## <a name="system-requirements-for-field-service"></a><span data-ttu-id="0a3f1-121">Systemanforderungen für Field Service</span><span class="sxs-lookup"><span data-stu-id="0a3f1-121">System requirements for Field Service</span></span>
<span data-ttu-id="0a3f1-122">Um die Field Service-Integrationslösung zu nutzen, müssen Sie Folgendes installieren:</span><span class="sxs-lookup"><span data-stu-id="0a3f1-122">To use the Field Service integration solution, you must install the following components:</span></span>

### <a name="microsoft-dynamics-365-for-field-service-90-or-later"></a><span data-ttu-id="0a3f1-123">Microsoft Dynamics 365 for Field Service 9.0 oder höher</span><span class="sxs-lookup"><span data-stu-id="0a3f1-123">Microsoft Dynamics 365 for Field Service 9.0 or later</span></span>

- <span data-ttu-id="0a3f1-124">Dynamics 365 for Field Service Version 1612 (9.0.1.733) (DB 9.0.1.733) online oder eine spätere Version.</span><span class="sxs-lookup"><span data-stu-id="0a3f1-124">Dynamics 365 for Field Service version 1612 (9.0.1.733) (DB 9.0.1.733) online or a later version.</span></span>
- <span data-ttu-id="0a3f1-125">Interessent zu Bargeld (P2C)-Lösung für Dynamics 365, Version 1.15.0.1 oder eine spätere Version.</span><span class="sxs-lookup"><span data-stu-id="0a3f1-125">Prospect to Cash (P2C) solution for Dynamics 365, version 1.15.0.1 or a later version.</span></span> <span data-ttu-id="0a3f1-126">Die Lösung ist unter [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3) zum Download verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0a3f1-126">The solution is available for download from [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span></span>
- <span data-ttu-id="0a3f1-127">Field Service-Integrationslösung für Dynamics 365, Version 1.0.0.0 oder eine spätere Version.</span><span class="sxs-lookup"><span data-stu-id="0a3f1-127">Field Service integration solution for Dynamics 365, version 1.0.0.0 or a later version.</span></span> <span data-ttu-id="0a3f1-128">Die Lösung ist unter AppSource zum Download verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0a3f1-128">The solution is available for download from AppSource.</span></span> <span data-ttu-id="0a3f1-129">**(AUSSTEHENDE FREIGABE)**</span><span class="sxs-lookup"><span data-stu-id="0a3f1-129">**(PENDING RELEASE)**</span></span>

