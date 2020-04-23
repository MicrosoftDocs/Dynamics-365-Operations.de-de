---
title: Automatische Erstellung von Serviceaufträgen
description: Sie können Serviceaufträge für einen oder mehrere Serviceverträge erstellen.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e4ba2cf115faacda14e25838a488fc54c53f48f3
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3202720"
---
# <a name="create-service-orders-automatically"></a><span data-ttu-id="2b492-103">Automatische Erstellung von Serviceaufträgen</span><span class="sxs-lookup"><span data-stu-id="2b492-103">Create service orders automatically</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="2b492-104">Sie können Serviceaufträge für einen oder mehrere Serviceverträge erstellen.</span><span class="sxs-lookup"><span data-stu-id="2b492-104">You can create service orders for one service agreement or for several service agreements.</span></span> <span data-ttu-id="2b492-105">Bei der Erstellung können die Serviceaufträge im Formular **Serviceaufträge** angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="2b492-105">When they are created, you can view your service orders in the **Service orders** form.</span></span>

<span data-ttu-id="2b492-106">Serviceaufträge werden nur für den Gültigkeitszeitraum des Servicevertrags erstellt.</span><span class="sxs-lookup"><span data-stu-id="2b492-106">Service orders are created only for the valid period of the service agreement.</span></span> <span data-ttu-id="2b492-107">Liegt das Intervall, das Sie im Formular **Serviceaufträge erstellen** angeben, vor dem Startdatum oder nach dem Enddatum des Servicevertrags, werden Serviceaufträge nur für den Bereich des Intervalls erstellt, der innerhalb des Zeitraums des Servicevertrags liegt.</span><span class="sxs-lookup"><span data-stu-id="2b492-107">If the interval that you specify in the **Create service orders** form is before the starting date or after the ending date of the service agreement, service orders are created only for the part of the interval that is within the service agreement dates.</span></span>

<span data-ttu-id="2b492-108">Werden Serviceaufträge manuell oder automatisch anhand der Servicevertragsposition erstellt, muss der Serviceauftrag in das Zeitintervall fallen, das durch das Start- und Enddatum für die Position definiert wird, sofern Sie kein Enddatum für die Position angeben.</span><span class="sxs-lookup"><span data-stu-id="2b492-108">When you create service orders manually or automatically from the service agreement line, the service order must be in the time interval that is defined by the starting and ending dates for the line, unless you do not specify an ending date on the line.</span></span>

## <a name="create-service-orders-automatically-for-a-service-agreement"></a><span data-ttu-id="2b492-109">Automatisches Erstellen von Serviceaufträgen für einen Servicevertrag</span><span class="sxs-lookup"><span data-stu-id="2b492-109">Create service orders automatically for a service agreement</span></span>

1.  <span data-ttu-id="2b492-110">Klicken Sie auf den Bereichsseitenknoten: **Serviceverwaltung** \> **Gemeinsam** \> **Servicevereinbarungen** \> **Servicevereinbarungen**.</span><span class="sxs-lookup"><span data-stu-id="2b492-110">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="2b492-111">Wählen Sie einen Servicevertrag aus.</span><span class="sxs-lookup"><span data-stu-id="2b492-111">Select a service agreement.</span></span>

3.  <span data-ttu-id="2b492-112">Klicken Sie auf der Registerkarte **Liefern** und dann auf **Geplante Serviceaufträge**.</span><span class="sxs-lookup"><span data-stu-id="2b492-112">Click the **Deliver** tab, and then click **Planned service orders**.</span></span>

4.  <span data-ttu-id="2b492-113">Geben Sie Datumsangaben in die Felder **Von Datum** und **Bis Datum** ein, um die Serviceperiode zu definieren.</span><span class="sxs-lookup"><span data-stu-id="2b492-113">Specify dates in the **From date** and **To date** fields to define the service period.</span></span>

5.  <span data-ttu-id="2b492-114">Aktivieren Sie das Kontrollkästchen **Infolog anzeigen**, um eine Liste der erstellten Serviceaufträge anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="2b492-114">Select the **Show Infolog** check box to display a list of the service orders that are created.</span></span>

6.  <span data-ttu-id="2b492-115">Wählen Sie Buchungsarten in der Feldgruppe **Buchungsarten einschließen** aus.</span><span class="sxs-lookup"><span data-stu-id="2b492-115">Select transaction types in the **Include transaction types** field group.</span></span> <span data-ttu-id="2b492-116">Die Buchungsarten stehen für die Positionen, die im Servicevertrag erstellt werden. Abhängig vom Serviceintervall, das für die Servicevertragsposition angegeben wurde, erzeugt jede ausgewählte Buchungsart mehrere Serviceaufträge.</span><span class="sxs-lookup"><span data-stu-id="2b492-116">The transaction types represent the lines that are created in the service agreement, and each transaction type that you select generates several service orders, depending on the service interval that is specified on the service agreement line.</span></span>

7.  <span data-ttu-id="2b492-117">Aktivieren Sie das Kontrollkästchen **Fortlaufend**, um die Serviceaufträge zu erstellen, die in einer fortlaufenden Reihe von Serviceaufträgen fehlen.</span><span class="sxs-lookup"><span data-stu-id="2b492-117">To create any service orders that are missing from continuous series of service orders, select the **Continuous** check box.</span></span>

8.  <span data-ttu-id="2b492-118">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="2b492-118">Click **OK**.</span></span>

## <a name="create-service-orders-automatically-for-several-service-agreements"></a><span data-ttu-id="2b492-119">Automatisches Erstellen von Serviceaufträgen für mehrere Serviceverträge</span><span class="sxs-lookup"><span data-stu-id="2b492-119">Create service orders automatically for several service agreements</span></span>

1.  <span data-ttu-id="2b492-120">Klicken Sie auf **Serviceverwaltung** \> **Periodisch** \> **Serviceaufträge** \> **Serviceaufträge erstellen**.</span><span class="sxs-lookup"><span data-stu-id="2b492-120">Click **Service management** \> **Periodic** \> **Service orders** \> **Create service orders**.</span></span>

2.  <span data-ttu-id="2b492-121">Klicken Sie auf **Auswählen**, um eine Auswahl zum Hinzufügen oder Entfernen von Kriterien für die Erstellung von Serviceaufträgen zu treffen.</span><span class="sxs-lookup"><span data-stu-id="2b492-121">Click **Select** to make selections to add or remove criteria to use to create service orders.</span></span>

3.  <span data-ttu-id="2b492-122">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="2b492-122">Click **OK**.</span></span>

## <a name="see-also"></a><span data-ttu-id="2b492-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b492-123">See also</span></span>

[<span data-ttu-id="2b492-124">Serviceaufträge</span><span class="sxs-lookup"><span data-stu-id="2b492-124">Service orders</span></span>](service-orders.md)

[<span data-ttu-id="2b492-125">Automatisches Erstellen von Serviceaufträgen</span><span class="sxs-lookup"><span data-stu-id="2b492-125">Automatically create service orders</span></span>](auto-create-service-orders.md)

  


