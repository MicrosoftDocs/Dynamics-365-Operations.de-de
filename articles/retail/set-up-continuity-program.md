---
title: "Einrichten eines Anschlussprogramms für ein Callcenter"
description: "In diesem Atikel wird beschrieben, wie ein Anschlussprogramm für ein Callcenter eingerichtet wird."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16081
ms.assetid: 426a9be7-a931-4780-b372-e06f6083dd60
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 00504b62237ac4f121d603d5144ffa4e71956cc3
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-a-continuity-program-for-a-call-center"></a><span data-ttu-id="41b0f-103">Einrichten eines Anschlussprogramms für ein Callcenter</span><span class="sxs-lookup"><span data-stu-id="41b0f-103">Set up a continuity program for a call center</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="41b0f-104">In diesem Atikel wird beschrieben, wie ein Anschlussprogramm für ein Callcenter eingerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="41b0f-104">This article describes how to set up a continuity program for a call center.</span></span>

<span data-ttu-id="41b0f-105">In einem Anschlussprogramm, auch als wiederkehrendes Auftragsprogramm bekannt, erhalten Debitoren reguläre Produktlieferungen gemäß einem vordefinierten Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="41b0f-105">In a continuity program, which is also known as a recurring order program, customers receive regular product shipments according to a predefined schedule.</span></span> <span data-ttu-id="41b0f-106">Jede Lieferung kann ein anderes Produkt enthalten, wie im Falle eines Buch-des-Monats-Vereins, oder das gleiche Produkt kann wiederholt gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="41b0f-106">Each shipment can contain a different product, as in the case of a book-of-the-month club, or the same product can be sent repeatedly.</span></span> <span data-ttu-id="41b0f-107">Für die Konfiguration eines Anschlussprogramms müssen die folgenden Aufgaben ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="41b0f-107">To set up a continuity program, you must complete the following tasks.</span></span>

1.  <span data-ttu-id="41b0f-108">Legen Sie die Anschlussparameter auf der **Callcenter-Parameter**-Seite fest.</span><span class="sxs-lookup"><span data-stu-id="41b0f-108">Set the continuity parameters on the **Call center parameters** page.</span></span>
2.  <span data-ttu-id="41b0f-109">Erstellen Sie ein Anschlussprogramm, das Details angibt, wie Zahlungsplan, Zeitpunkt der Lieferungen und ob die Fakturierung vorab ist.</span><span class="sxs-lookup"><span data-stu-id="41b0f-109">Create a continuity program that specifies details such as the payment schedule, the timing of the shipments, and whether billing is up front.</span></span> <span data-ttu-id="41b0f-110">Sie müssen auch eine Liste von Produkten hinzufügen, die im Anschlussprogramm enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="41b0f-110">You must also add a list of products that are included in the continuity program.</span></span> <span data-ttu-id="41b0f-111">Jedem Produkt erhält eine sequenziell Ereignis-ID-Nummer, die zugewiesen und mit 1 beginnt.</span><span class="sxs-lookup"><span data-stu-id="41b0f-111">Each product receives an event ID number that is assigned sequentially, beginning with 1.</span></span> <span data-ttu-id="41b0f-112">Die Ereignis-IDs bestimmen die Reihenfolge, die Produkten eingereicht werden.</span><span class="sxs-lookup"><span data-stu-id="41b0f-112">The event IDs determine the order that products are sent in.</span></span>
    -   <span data-ttu-id="41b0f-113">Wenn Kunden ein unterschiedliches Produkt in jeder Lieferung erhalten, werden die Produkte sequenziell auf Grundlage ihrer Ereigniskennung und beginnend mit dem aktuellen Ereignis übermittelt.</span><span class="sxs-lookup"><span data-stu-id="41b0f-113">If customers receive a different product in each shipment, the products are sent in sequential order, based on their event IDs and beginning with the current event.</span></span>
    -   <span data-ttu-id="41b0f-114">Wenn Kunden das gleiche Produkt in jeder Lieferung erhalten, enthält die Liste nur ein Produkt, das eine Ereignis-ID hat.</span><span class="sxs-lookup"><span data-stu-id="41b0f-114">If customers receive the same product in each shipment, the list contains only one product that has one event ID.</span></span> <span data-ttu-id="41b0f-115">Dasselbe Ereignis tritt wiederholt auf.</span><span class="sxs-lookup"><span data-stu-id="41b0f-115">The same event occurs repeatedly.</span></span> <span data-ttu-id="41b0f-116">Sie können angeben, wie oft, jedes Ereignis wiederholt wird.</span><span class="sxs-lookup"><span data-stu-id="41b0f-116">You can specify how many times each event is repeated.</span></span>

3.  <span data-ttu-id="41b0f-117">Erstellen Sie ein übergeordnetes Produkt, das das Kontinuitätsprogramm ein, das Sie in Aufgabe. 2 erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="41b0f-117">Create a parent product that represents the continuity program that you created in task 2.</span></span> <span data-ttu-id="41b0f-118">Wenn Sie dieses Produkt einem Auftrag, hinzugefügt wird die **Kontinuität** Seite.</span><span class="sxs-lookup"><span data-stu-id="41b0f-118">If you add this product to a sales order, the **Continuity** page opens.</span></span> <span data-ttu-id="41b0f-119">Sie können dann diese Seite verwenden, um den tatsächlichen Anschlussauftrag zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="41b0f-119">You can then use that page to create the actual continuity order.</span></span> <span data-ttu-id="41b0f-120">Das übergeordnete Produkt gibt nicht die Einzelprodukte an, die der Debitor in jeder Lieferung erhält.</span><span class="sxs-lookup"><span data-stu-id="41b0f-120">The parent product doesn't specify the individual products that the customer receives in each shipment.</span></span>

<span data-ttu-id="41b0f-121">Nachdem Sie ein Anschlussprogramm eingerichtet haben, wie oben beschrieben, können Sie einen Anschlussauftrag für einen Debitor erstellen.</span><span class="sxs-lookup"><span data-stu-id="41b0f-121">After you've set up a continuity program as described above, you can create a continuity order for a customer.</span></span> <span data-ttu-id="41b0f-122">Unter Umständen müssen Sie auch die folgenden zusätzlichen Verwaltungsaufgaben ausführen.</span><span class="sxs-lookup"><span data-stu-id="41b0f-122">You might also have to perform the following additional maintenance tasks.</span></span>

-   <span data-ttu-id="41b0f-123">**Aktualisieren der aktuellen Einstellung für Anschlussereignisperioden** – Richten Sie einen Batchauftrag ein, der dem System mitteilt, welches die aktuelle Ereignissperiode ist.</span><span class="sxs-lookup"><span data-stu-id="41b0f-123">**Update the current continuity event period** – Set up a batch job that tells the system what the current event period is.</span></span>
-   <span data-ttu-id="41b0f-124">**Erstellen untergeordneter Aufträge** – Erstellen Sie untergeordnete Aufträge aus dem übergeordneten Anschlussauftrag.</span><span class="sxs-lookup"><span data-stu-id="41b0f-124">**Create continuity child orders** – Create child orders from the parent continuity order.</span></span>
-   <span data-ttu-id="41b0f-125">**Verarbeiten von Anschlusszahlungen** – Verarbeiten Sie die Fakturierung und Benachrichtigungen für Zahlungen, die Anschlussaufträgen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="41b0f-125">**Process continuity payments** – Process billing and notifications for payments that are associated with continuity sales orders.</span></span>
-   <span data-ttu-id="41b0f-126">**Erweitern von Anschlusspositionen** (Nach Bedarf) – Erweitern Sie die Anzahl der Male, die ein Anschlussereignis wiederholt werden kann.</span><span class="sxs-lookup"><span data-stu-id="41b0f-126">**Extend continuity lines** (if required) – Extend the number of times that a continuity event can be repeated.</span></span> <span data-ttu-id="41b0f-127">Die Wiederholung von Lieferungen kann sich dann über den Zeitpunkt hinaus verlängern, die im Feld **Anschlusswiederholungs-Schwellenwert** in den Callcenterparametern festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="41b0f-127">The repetition of shipments can then extend beyond the limit that was set in the **Continuity repeat threshold** field in the call center parameters.</span></span>
-   <span data-ttu-id="41b0f-128">**Ausführen einer Anschlusssaktualisierung** (Nach Bedarf) – Synchronisieren Sie Änderungen zwischen dem Anschlussprogramm und den übergeordneten Anschlussaufträgen.</span><span class="sxs-lookup"><span data-stu-id="41b0f-128">**Perform a continuity update** (if required) – Synchronize changes between the continuity program and the continuity parent sales orders.</span></span>
-   <span data-ttu-id="41b0f-129">**Übergeordnete Anschlusspositionen und -aufträge schließen** – Schließen Sie Anschlussaufträge.</span><span class="sxs-lookup"><span data-stu-id="41b0f-129">**Close continuity parent lines and orders** – Close continuity orders.</span></span>





