---
title: Serviceverwaltung
description: Mit der Serviceverwaltung können Sie Serviceverträge und Daueraufträge einrichten, Serviceaufträge und Debitorenanfragen handhaben und die Servicebereitstellung für Kunden verwalten und analysieren.
author: ShylaThompson
manager: AnnBe
ms.date: 05/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b2fc5361b1b30db29789ff67b56a15eb66a919f5
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843288"
---
# <a name="service-management"></a><span data-ttu-id="ec13e-103">Serviceverwaltung</span><span class="sxs-lookup"><span data-stu-id="ec13e-103">Service management</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="ec13e-104">Mit der **Serviceverwaltung** können Sie Serviceverträge und Daueraufträge einrichten, Serviceaufträge und Debitorenanfragen handhaben und die Servicebereitstellung für Kunden verwalten und analysieren.</span><span class="sxs-lookup"><span data-stu-id="ec13e-104">Use **Service management** to establish service agreements and service subscriptions, handle service orders and customer inquiries, and to manage and analyze the delivery of services to customers.</span></span> <span data-ttu-id="ec13e-105">In Serviceverträgen können Sie die Ressourcen definieren, die für einen typischen Servicebesuch benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="ec13e-105">You can use service agreements to define the resources that are used in a typical service visit.</span></span> <span data-ttu-id="ec13e-106">Zudem können Sie in Serviceverträgen festlegen, wie diese Ressourcen dem Debitor in Rechnung gestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ec13e-106">You can also use service agreements to view how those resources are invoiced to the customer.</span></span> <span data-ttu-id="ec13e-107">Ein Servicevertrag kann auch eine Vereinbarung zum Servicelevel enthalten, die Standardantwortzeiten festlegt und Tools zum Erfassen der tatsächlichen Zeit anbietet.</span><span class="sxs-lookup"><span data-stu-id="ec13e-107">A service agreement can also include a service level agreement that specifies standard response times, and offers tools to record the actual time.</span></span>

<span data-ttu-id="ec13e-108">Sie können Serviceaufträge erstellen, um Informationen zu geplanten und nicht geplanten Besuchen von einem Servicetechniker am Kundenstandort zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="ec13e-108">You can create service orders to manage information about scheduled and unscheduled visits by a service technician to a customer site.</span></span> <span data-ttu-id="ec13e-109">Serviceaufträge enthalten beispielsweise folgende Informationen:</span><span class="sxs-lookup"><span data-stu-id="ec13e-109">Service orders include information such as:</span></span>

1.  <span data-ttu-id="ec13e-110">Die Arbeitsstunden, die der Servicetechniker ausführt</span><span class="sxs-lookup"><span data-stu-id="ec13e-110">The hours of work that the service technician will perform</span></span>

2.  <span data-ttu-id="ec13e-111">Der Typ des Service oder der Reparatur</span><span class="sxs-lookup"><span data-stu-id="ec13e-111">The type of service or repair</span></span>

3.  <span data-ttu-id="ec13e-112">Der zu reparierende Gegenstand, einschließlich Details zu Symptomen und Diagnose</span><span class="sxs-lookup"><span data-stu-id="ec13e-112">The item to repair, including details about the symptoms and diagnosis</span></span>

4.  <span data-ttu-id="ec13e-113">Ausgaben und Gebühren in Bezug auf den Service oder die Reparatur</span><span class="sxs-lookup"><span data-stu-id="ec13e-113">Any expenses and fees related to the service or repair</span></span>

<span data-ttu-id="ec13e-114">Sie können diese Anforderungen empfangen, verarbeiten und versenden.</span><span class="sxs-lookup"><span data-stu-id="ec13e-114">You can receive, process, and dispatch service requests.</span></span> <span data-ttu-id="ec13e-115">Nachdem Sie einen Serviceauftrag erstellt haben, können Sie mithilfe von Servicephasen den Fortschritt überwachen und anhand von Regeln steuern, welche Aktivitäten in jeder Phase aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="ec13e-115">After you have created a service order, you can use service stages to monitor progress and specify rules that control what actions are enabled in each stage.</span></span> <span data-ttu-id="ec13e-116">Wenn ein Serviceauftrag abgeschlossen ist, können Sie den Auftrag abzeichnen, um dessen Vollständigkeit zu bestätigen. Dann können Sie den Auftrag buchen, um den Rechnungsprozess zu starten.</span><span class="sxs-lookup"><span data-stu-id="ec13e-116">When a service order is complete, you can sign off on the order to confirm that it is complete, and then post the order to start the invoice process.</span></span>

<span data-ttu-id="ec13e-117">Mithilfe der Berichtstools können Sie Gewinnspannen für Serviceaufträge und Dauerauftragsbuchungen überwachen sowie Arbeitsbeschreibungen und Arbeitsquittungen drucken.</span><span class="sxs-lookup"><span data-stu-id="ec13e-117">Use the reporting tools to monitor service order margins and subscription transactions, and print work descriptions and work receipts.</span></span>

## <a name="business-processes"></a><span data-ttu-id="ec13e-118">Geschäftsprozesse</span><span class="sxs-lookup"><span data-stu-id="ec13e-118">Business processes</span></span>

<span data-ttu-id="ec13e-119">Im folgenden Diagramm werden die Geschäftsprozesse auf oberer Ebene für **Serviceverwaltung** dargestellt. Das Diagramm veranschaulicht, wo Serviceprozesse in andere Module in Microsoft Dynamics 365 for Finance and Operations integriert werden.</span><span class="sxs-lookup"><span data-stu-id="ec13e-119">The following diagram illustrates the high level business processes for **Service management**, and shows where service processes integrate with other modules in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="ec13e-120">[![Geschäftsprozessdiagramm für Serviceverwaltung](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span><span class="sxs-lookup"><span data-stu-id="ec13e-120">[![Service management business process diagram](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span></span>

## <a name="service-management-at-a-glance"></a><span data-ttu-id="ec13e-121">Serviceverwaltung auf einen Blick</span><span class="sxs-lookup"><span data-stu-id="ec13e-121">Service management at a glance</span></span>

|<span data-ttu-id="ec13e-122">Wichtige Aufgaben</span><span class="sxs-lookup"><span data-stu-id="ec13e-122">Important tasks</span></span>           | <span data-ttu-id="ec13e-123">Primäre Seiten</span><span class="sxs-lookup"><span data-stu-id="ec13e-123">Primary pages</span></span>                         |<span data-ttu-id="ec13e-124">Häufig verwendete Berichte</span><span class="sxs-lookup"><span data-stu-id="ec13e-124">Popular reports</span></span>              |
|--------------------------|---------------------------------------|-----------------------------|
|<span data-ttu-id="ec13e-125">Serviceverträge erfüllen</span><span class="sxs-lookup"><span data-stu-id="ec13e-125">Fulfill service agreements</span></span>|<span data-ttu-id="ec13e-126">Serviceverträge</span><span class="sxs-lookup"><span data-stu-id="ec13e-126">Service agreements</span></span>                     |<span data-ttu-id="ec13e-127">Gewinnspanne für Serviceauftrag</span><span class="sxs-lookup"><span data-stu-id="ec13e-127">Service order margin</span></span>         |
|<span data-ttu-id="ec13e-128">Debitorenabfragen behandeln</span><span class="sxs-lookup"><span data-stu-id="ec13e-128">Handle customer inquiries</span></span> |<span data-ttu-id="ec13e-129">Serviceaufträge</span><span class="sxs-lookup"><span data-stu-id="ec13e-129">Service orders</span></span>                         |<span data-ttu-id="ec13e-130">Arbeitsbeschreibung</span><span class="sxs-lookup"><span data-stu-id="ec13e-130">Work description</span></span>             |
|                          |<span data-ttu-id="ec13e-131">Einsatzplanung</span><span class="sxs-lookup"><span data-stu-id="ec13e-131">Dispatch board</span></span>                         |<span data-ttu-id="ec13e-132">Buchung - Dauerauftrag</span><span class="sxs-lookup"><span data-stu-id="ec13e-132">Transaction - subscription</span></span>   |
|                          |                                       |<span data-ttu-id="ec13e-133">Buchungen von Dauerauftragsgebühren</span><span class="sxs-lookup"><span data-stu-id="ec13e-133">Subscription fee transactions</span></span>|


## <a name="integration-of-service-management"></a><span data-ttu-id="ec13e-134">Integration der Serviceverwaltung</span><span class="sxs-lookup"><span data-stu-id="ec13e-134">Integration of Service management</span></span>

<span data-ttu-id="ec13e-135">Die Serviceverwaltung kann in die folgenden Module in  integriert werden:</span><span class="sxs-lookup"><span data-stu-id="ec13e-135">Service management can be integrated with the following modules:</span></span>

  - [<span data-ttu-id="ec13e-136">Vertrieb und Marketing</span><span class="sxs-lookup"><span data-stu-id="ec13e-136">Sales and marketing</span></span>](../sales-marketing/overview-sales-marketing.md)
  - [<span data-ttu-id="ec13e-137">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="ec13e-137">Human resources</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/index)

  

