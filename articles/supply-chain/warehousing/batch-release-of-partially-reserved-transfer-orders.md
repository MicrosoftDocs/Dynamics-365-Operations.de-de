---
title: Chargenfreigabe von teilweise reservierten Umlagerungsaufträgen
description: In diesem Thema wird beschrieben, wie Sie die Optionen für teilweise reservierte Umlagerungsaufträge auf einem mobilen Gerät einrichten und anwenden.
author: pjacobse
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, WHSFulfillmentPolicy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7807ae109a4a708f3530112feed1a4fb210a30ef
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016286"
---
# <a name="batch-release-of-partially-reserved-transfer-orders"></a><span data-ttu-id="6487c-103">Chargenfreigabe von teilweise reservierten Umlagerungsaufträgen</span><span class="sxs-lookup"><span data-stu-id="6487c-103">Batch release of partially reserved transfer orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6487c-104">Die Funktionen für Chargenfreigabe von teilweise reservierten Umlagerungsaufträgen können Sie Umlagerungsaufträge teilweise einem Lagerort freigeben, indem eines Stapelverarbeitungsauftrags können.</span><span class="sxs-lookup"><span data-stu-id="6487c-104">The functionality for batch release of partially reserved transfer orders lets you partially release transfer orders to a warehouse by using a batch job.</span></span>
<span data-ttu-id="6487c-105">Da Sie die Möglichkeit haben, eine Teilmenge freizugeben, müssen Sie nicht für die gesamte Auftragsmenge warten, die am Lagerort verfügbar ist, bevor ein Auftrag freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6487c-105">Because you have the option to release a partial quantity, you don’t have to wait for the whole order quantity to be available in the warehouse before you release an order.</span></span>

<span data-ttu-id="6487c-106">Die Version von Aufträgen an einen Lagerort ist ein erweiterter Lagerortverwaltungsprozess.</span><span class="sxs-lookup"><span data-stu-id="6487c-106">The release of orders to a warehouse is an advanced warehouse management process.</span></span> <span data-ttu-id="6487c-107">Dieser Prozess beinhaltet Aktivitäten wie Entnahme, Verpackung und Versand, die ein Lagerarbeiter ausführen kann, indem er ein mobiles Gerät verwendet.</span><span class="sxs-lookup"><span data-stu-id="6487c-107">This process involves activities, such as picking, packing, and shipping, that a warehouse worker can perform by using a mobile device.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="6487c-108">Wofür es angewendet wird</span><span class="sxs-lookup"><span data-stu-id="6487c-108">Where it applies</span></span>

<span data-ttu-id="6487c-109">Für diese Funktion werden Umlagerungsaufträge einem Lagerort freigegeben, indem Sie einen Stapelverarbeitungsauftrag verwenden.</span><span class="sxs-lookup"><span data-stu-id="6487c-109">For this functionality, transfer orders are released to a warehouse by using a batch job.</span></span> <span data-ttu-id="6487c-110">Diese Funktionalität ist hilfreich, wenn Sie nicht genügend Bestand am Lagerort haben, aber dennoch Artikel aus einem Lagerort an einen anderen übertragen möchten.</span><span class="sxs-lookup"><span data-stu-id="6487c-110">This functionality is useful when you don’t have enough inventory in the warehouse, but you still want to transfer items from one warehouse to another.</span></span>

## <a name="how-it-is-set-up"></a><span data-ttu-id="6487c-111">Wie er installiert wird</span><span class="sxs-lookup"><span data-stu-id="6487c-111">How it is set up</span></span>

### <a name="specify-fulfillment-criteria-for-transfer-orders-and-sales-orders"></a><span data-ttu-id="6487c-112">Geben Sie Erfüllungskriterien für Umlagerungsaufträge und Aufträge an</span><span class="sxs-lookup"><span data-stu-id="6487c-112">Specify fulfillment criteria for transfer orders and sales orders</span></span>

<span data-ttu-id="6487c-113">Bevor ein Auftrag einem Lagerort in einer Charge teilweise freigegeben werden kann, müssen die Erfüllungskriterien erfüllt werden.</span><span class="sxs-lookup"><span data-stu-id="6487c-113">Before an order can be partially released to a warehouse in a batch, the fulfillment criteria must be met.</span></span> <span data-ttu-id="6487c-114">Diese Erfüllungskriterien werden durch die Erfüllungsrichtlinie bestimmt.</span><span class="sxs-lookup"><span data-stu-id="6487c-114">These fulfillment criteria are determined by the fulfillment policy.</span></span>

<span data-ttu-id="6487c-115">Erfüllungspolitische Richtlinien für Umlagerungsaufträge und Aufträge werden auf Unternehmensebene angegeben.</span><span class="sxs-lookup"><span data-stu-id="6487c-115">Fulfillment policies for transfer orders and sales orders are specified at the company level.</span></span> <span data-ttu-id="6487c-116">Je nach den Einstellungen der Erfüllungsrichtlinie wird die Freisetzung von Aufträgen in einer Charge angenommen oder abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="6487c-116">Depending on the setup of the fulfillment policy, the release of orders in a batch will be accepted or rejected.</span></span> <span data-ttu-id="6487c-117">Die Aufträge werden dann entsprechend verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="6487c-117">The orders will then be processed accordingly.</span></span>

-   <span data-ttu-id="6487c-118">Weitere Erfüllungspolitische Richtlinien für Aufträge und Umlagerungsaufträge klicken Sie auf **Lagerortverwaltung** \> **Einstellungen** \> **Freigebung Lagerort** \> **Erfüllungsrichtlinie** , und erstellen Sie dann eine Erfüllungsrichtlinie, indem Sie einen Namen und eine Beschreibung eingeben.</span><span class="sxs-lookup"><span data-stu-id="6487c-118">To create fulfillment policies for transfer orders and sales orders, click **Warehouse management** \> **Setup** \> **Release to warehouse** \> **Fulfillment policy** , and then create a fulfillment policy by entering a name and a description.</span></span>

-   <span data-ttu-id="6487c-119">Um einen Erfüllungssatz anzugeben, legen Sie einen Werttyp und die Meldung fest, die angezeigt werden soll, wenn gegen die Erfüllungsrichtlinie verstoßen wird. Klicken Sie auf **Lagerortverwaltung** \> **Einstellungen** \> **Freigegebener Lagerort** \>  **Erfüllungsrichtlinie** und dann **Erfüllungssatz** , **Werttyp** und **Erfüllungsverstoßnachricht**.</span><span class="sxs-lookup"><span data-stu-id="6487c-119">To specify a fulfillment rate, a value type, and the message that is shown if the fulfillment policy is violated, click **Warehouse management** \> **Setup** \> **Release to warehouse** \> **Fulfillment policy** , and then set the **Fulfillment rate** , **Value type** , and **Fulfillment violation message** fields.</span></span>

### <a name="set-the-fulfillment-policies-for-transfer-orders-and-sales-orders"></a><span data-ttu-id="6487c-120">Geben Sie Erfüllungskriterien für Umlagerungsaufträge und Aufträge an</span><span class="sxs-lookup"><span data-stu-id="6487c-120">Set the fulfillment policies for transfer orders and sales orders</span></span>

-   <span data-ttu-id="6487c-121">Um die Erfüllungsrichtlinien für Umlagerungsaufträge festzulegen, klicken Sie auf **Lagerverwaltung** \> **Einstellungen** \> **Parameter für Lager- und Lagerortverwaltung** \> **Umlagerungsaufträge** \> **Lagerortverwaltung** , und wählen Sie dann eine Umlagerungsauftragserfüllungsrichtlinie aus.</span><span class="sxs-lookup"><span data-stu-id="6487c-121">To set the fulfillment policies for transfer orders, click **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters** \> **Transfer orders** \> **Warehouse management** , and then select a transfer order fulfillment policy.</span></span>

-   <span data-ttu-id="6487c-122">Um die Erfüllungsrichtlinie für Aufträge einzurichten, klicken Sie auf **Debitoren** \> **Einstellungen** \> **Debitorenparameter** \> **Lagerortverwaltung** , und wählen Sie dann eine Auftragserfüllungsrichtlinie aus.</span><span class="sxs-lookup"><span data-stu-id="6487c-122">To set the fulfillment policies for sales orders, click **Accounts receivable** \> **Setup** \> **Accounts receivable parameters** \> **Warehouse management** , and then select a sales order fulfillment policy.</span></span>

## <a name="allow-release-in-a-batch-and-specify-the-quantity-that-should-be-release-in-a-batch"></a><span data-ttu-id="6487c-123">Friegabe in Stapelverarbeitung zulassen und die Menge definieren, die Freigabe in einem Stapel freigegeben werden soll</span><span class="sxs-lookup"><span data-stu-id="6487c-123">Allow release in a batch and specify the quantity that should be release in a batch</span></span>

<span data-ttu-id="6487c-124">Ein Stapelverarbeitungsauftrag wird verwendet, um Aufträge in einer Stapelverarbeitung freizugeben.</span><span class="sxs-lookup"><span data-stu-id="6487c-124">A batch job is used to release orders to a warehouse in a batch.</span></span> <span data-ttu-id="6487c-125">Die Parameter, die sich vom Auftrag unterscheiden, sollten in einer Stapelverarbeitung ausgeführt werden und auf Stapelverarbeitungsauftrag auch festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="6487c-125">The parameters that distinguish the orders that should be run in a batch job are set on the batch job itself.</span></span>

<span data-ttu-id="6487c-126">Der Parameter **Menge** gibt an, ob die gesamte Menge oder die physisch reservierte Menge in der Charge verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6487c-126">The **Quantity** parameter specifies whether the whole quantity or the physically reserved quantity should be released in the batch.</span></span> <span data-ttu-id="6487c-127">Der Parameter **Teilweise Freisetzung von freigegebenen Aufträgen** bestimmt, ob Aufträge in der Charge übernommen oder abgelehnt werden sollen, wenn sie zuvor vollständig freigegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="6487c-127">The **Allow release of partially released orders** parameter determines whether orders in the batch should be accepted or rejected if they were partially released earlier.</span></span>

-   <span data-ttu-id="6487c-128">Wenn Sie die **Menge** und **Teilweise Freisetzung von Aufträgen ermöglichen** für Umlagerungsaufträge festlegen, klicken Sie auf **Lagerortverwaltung** \> **Freigebung Lagerort** \> **Automatische Freigabe der Umlagerungsaufträge**.</span><span class="sxs-lookup"><span data-stu-id="6487c-128">To set the **Quantity** and **Allow release of partially released orders** parameters for transfer orders, click **Warehouse management** \> **Release to warehouse** \> **Automatic release of transfer orders**.</span></span>

-   <span data-ttu-id="6487c-129">Wenn Sie die **Menge** und **Teilweise Freisetzung von Aufträgen ermöglichen** für Umlagerungsaufträge festlegen, klicken Sie auf **Lagerortverwaltung** \> **Freigebung Lagerort** \> **Automatische Freigabe der Umlagerungsaufträge**.</span><span class="sxs-lookup"><span data-stu-id="6487c-129">To set the **Quantity** and **Allow release of partially released orders** parameters for sales orders, click **Warehouse management** \> **Release to warehouse** \> **Automatic release of sales orders**.</span></span>
