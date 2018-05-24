---
title: Serviceverwaltung
description: "Mit der Serviceverwaltung können Sie Serviceverträge und Daueraufträge einrichten, Serviceaufträge und Debitorenanfragen handhaben und die Servicebereitstellung für Kunden verwalten und analysieren."
author: YuyuScheller
manager: AnnBe
ms.date: 05/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 02cdf4615e2071f2b7de2e86b6f9e6637c6e5d8d
ms.openlocfilehash: 236ab21b2d1c5a4e82270e5381d163e97437cb7f
ms.contentlocale: de-de
ms.lasthandoff: 05/09/2018

---


# <a name="service-management"></a><span data-ttu-id="8e31d-103">Serviceverwaltung</span><span class="sxs-lookup"><span data-stu-id="8e31d-103">Service management</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="8e31d-104">Mit der **Serviceverwaltung** können Sie Serviceverträge und Daueraufträge einrichten, Serviceaufträge und Debitorenanfragen handhaben und die Servicebereitstellung für Kunden verwalten und analysieren.</span><span class="sxs-lookup"><span data-stu-id="8e31d-104">Use **Service management** to establish service agreements and service subscriptions, handle service orders and customer inquiries, and to manage and analyze the delivery of services to customers.</span></span> <span data-ttu-id="8e31d-105">In Serviceverträgen können Sie die Ressourcen definieren, die für einen typischen Servicebesuch benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="8e31d-105">You can use service agreements to define the resources that are used in a typical service visit.</span></span> <span data-ttu-id="8e31d-106">Zudem können Sie in Serviceverträgen festlegen, wie diese Ressourcen dem Debitor in Rechnung gestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8e31d-106">You can also use service agreements to view how those resources are invoiced to the customer.</span></span> <span data-ttu-id="8e31d-107">Ein Servicevertrag kann auch eine Vereinbarung zum Servicelevel enthalten, die Standardantwortzeiten festlegt und Tools zum Erfassen der tatsächlichen Zeit anbietet.</span><span class="sxs-lookup"><span data-stu-id="8e31d-107">A service agreement can also include a service level agreement that specifies standard response times, and offers tools to record the actual time.</span></span>

<span data-ttu-id="8e31d-108">Sie können Serviceaufträge erstellen, um Informationen zu geplanten und nicht geplanten Besuchen von einem Servicetechniker am Kundenstandort zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="8e31d-108">You can create service orders to manage information about scheduled and unscheduled visits by a service technician to a customer site.</span></span> <span data-ttu-id="8e31d-109">Serviceaufträge enthalten beispielsweise folgende Informationen:</span><span class="sxs-lookup"><span data-stu-id="8e31d-109">Service orders include information such as:</span></span>

1.  <span data-ttu-id="8e31d-110">Die Arbeitsstunden, die der Servicetechniker ausführt</span><span class="sxs-lookup"><span data-stu-id="8e31d-110">The hours of work that the service technician will perform</span></span>

2.  <span data-ttu-id="8e31d-111">Der Typ des Service oder der Reparatur</span><span class="sxs-lookup"><span data-stu-id="8e31d-111">The type of service or repair</span></span>

3.  <span data-ttu-id="8e31d-112">Der zu reparierende Gegenstand, einschließlich Details zu Symptomen und Diagnose</span><span class="sxs-lookup"><span data-stu-id="8e31d-112">The item to repair, including details about the symptoms and diagnosis</span></span>

4.  <span data-ttu-id="8e31d-113">Ausgaben und Gebühren in Bezug auf den Service oder die Reparatur</span><span class="sxs-lookup"><span data-stu-id="8e31d-113">Any expenses and fees related to the service or repair</span></span>

<span data-ttu-id="8e31d-114">Debitoren können Serviceanforderungen mit Enterprise Portal über das Internet übermitteln.</span><span class="sxs-lookup"><span data-stu-id="8e31d-114">Customers can submit service requests through the Internet by using the Enterprise Portal.</span></span> <span data-ttu-id="8e31d-115">Sie können diese Anforderungen empfangen, verarbeiten und versenden.</span><span class="sxs-lookup"><span data-stu-id="8e31d-115">You can receive, process, and dispatch these requests.</span></span> <span data-ttu-id="8e31d-116">Nachdem Sie einen Serviceauftrag erstellt haben, können Sie mithilfe von Servicephasen den Fortschritt überwachen und anhand von Regeln steuern, welche Aktivitäten in jeder Phase aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="8e31d-116">After you have created a service order, you can use service stages to monitor progress and specify rules that control what actions are enabled in each stage.</span></span> <span data-ttu-id="8e31d-117">Wenn ein Serviceauftrag abgeschlossen ist, können Sie den Auftrag abzeichnen, um dessen Vollständigkeit zu bestätigen. Dann können Sie den Auftrag buchen, um den Rechnungsprozess zu starten.</span><span class="sxs-lookup"><span data-stu-id="8e31d-117">When a service order is complete, you can sign off on the order to confirm that it is complete, and then post the order to start the invoice process.</span></span>

<span data-ttu-id="8e31d-118">Mithilfe der Berichtstools können Sie Gewinnspannen für Serviceaufträge und Dauerauftragsbuchungen überwachen sowie Arbeitsbeschreibungen und Arbeitsquittungen drucken.</span><span class="sxs-lookup"><span data-stu-id="8e31d-118">Use the reporting tools to monitor service order margins and subscription transactions, and print work descriptions and work receipts.</span></span>

## <a name="business-processes"></a><span data-ttu-id="8e31d-119">Geschäftsprozesse</span><span class="sxs-lookup"><span data-stu-id="8e31d-119">Business processes</span></span>

<span data-ttu-id="8e31d-120">Im folgenden Diagramm werden die Geschäftsprozesse auf oberer Ebene für **Serviceverwaltung** dargestellt. Das Diagramm veranschaulicht, wo Serviceprozesse in andere Module in Microsoft Dynamics 365 for Finance and Operations integriert werden.</span><span class="sxs-lookup"><span data-stu-id="8e31d-120">The following diagram illustrates the high level business processes for **Service management**, and shows where service processes integrate with other modules in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="8e31d-121">[![Geschäftsprozessdiagramm für Serviceverwaltung](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span><span class="sxs-lookup"><span data-stu-id="8e31d-121">[![Service management business process diagram](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span></span>

## <a name="service-management-at-a-glance"></a><span data-ttu-id="8e31d-122">Serviceverwaltung auf einen Blick</span><span class="sxs-lookup"><span data-stu-id="8e31d-122">Service management at a glance</span></span>

<table>
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8e31d-123">Wichtige Aufgaben</span><span class="sxs-lookup"><span data-stu-id="8e31d-123">Important tasks</span></span></p></th>
<th><p><span data-ttu-id="8e31d-124">Primäre Formulare</span><span class="sxs-lookup"><span data-stu-id="8e31d-124">Primary forms</span></span></p></th>
<th><p><span data-ttu-id="8e31d-125">Häufig verwendete Berichte</span><span class="sxs-lookup"><span data-stu-id="8e31d-125">Popular reports</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8e31d-126">Serviceverträge erfüllen</span><span class="sxs-lookup"><span data-stu-id="8e31d-126">Fulfill service agreements</span></span></a></p></td>
<td><p><span data-ttu-id="8e31d-127"><a href="https://technet.microsoft.com/en-us/library/aa617823(v=ax.60)">Formular "Servicevereinbarungen"</a></span><span class="sxs-lookup"><span data-stu-id="8e31d-127"><a href="https://technet.microsoft.com/en-us/library/aa617823(v=ax.60)">Service agreements (form)</a></span></span></p></td>
<td><p><span data-ttu-id="8e31d-128"><strong>Gewinnspanne für Serviceauftrag</strong></span><span class="sxs-lookup"><span data-stu-id="8e31d-128"><strong>Service order margin</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e31d-129">Debitorenabfragen behandeln</span><span class="sxs-lookup"><span data-stu-id="8e31d-129">Handle customer inquiries</span></span></a></p></td>
<td><p><span data-ttu-id="8e31d-130"><a href="https://technet.microsoft.com/en-us/library/aa554361(v=ax.60)">Formular "Serviceaufträge"</a></span><span class="sxs-lookup"><span data-stu-id="8e31d-130"><a href="https://technet.microsoft.com/en-us/library/aa554361(v=ax.60)">Service orders (form)</a></span></span></p></td>
<td><p><span data-ttu-id="8e31d-131"><strong>Arbeitsbeschreibung</strong></span><span class="sxs-lookup"><span data-stu-id="8e31d-131"><strong>Work description</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="8e31d-132"><a href="https://technet.microsoft.com/en-us/library/hh242789(v=ax.60)">Einsatzplanung (Formular)</a></span><span class="sxs-lookup"><span data-stu-id="8e31d-132"><a href="https://technet.microsoft.com/en-us/library/hh242789(v=ax.60)">Dispatch board (form)</a></span></span></p></td>
<td><p><span data-ttu-id="8e31d-133"><strong>Buchung - Dauerauftrag</strong></span><span class="sxs-lookup"><span data-stu-id="8e31d-133"><strong>Transaction - subscription</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="8e31d-134"><strong>Buchungen von Dauerauftragsgebühren</strong></span><span class="sxs-lookup"><span data-stu-id="8e31d-134"><strong>Subscription fee transactions</strong></span></span></p></td>
</tr>
</tbody>
</table>


## <a name="integration-of-service-management"></a><span data-ttu-id="8e31d-135">Integration der Serviceverwaltung</span><span class="sxs-lookup"><span data-stu-id="8e31d-135">Integration of Service management</span></span>

<span data-ttu-id="8e31d-136">Die Serviceverwaltung kann in die folgenden Module in Microsoft Dynamics 365 for Finance and Operations integriert werden:</span><span class="sxs-lookup"><span data-stu-id="8e31d-136">Service management can be integrated with the following modules in Microsoft Dynamics 365 for Finance and Operations:</span></span>

  - [<span data-ttu-id="8e31d-137">Vertrieb und Marketing</span><span class="sxs-lookup"><span data-stu-id="8e31d-137">Sales and marketing</span></span>](../sales-marketing/overview-sales-marketing.md)

  - [<span data-ttu-id="8e31d-138">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="8e31d-138">Human resources</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/index)

  


