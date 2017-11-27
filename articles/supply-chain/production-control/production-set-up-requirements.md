---
title: "Anforderungen für Produktionseinstellungen"
description: "Dieser Artikel gibt Informationen zu Einrichtungsanforderungen, bevor Sie mit der Produktionssteuerung arbeiten können."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdParameters, RouteOpr, RouteOprTable, WorkCalendarTable, WorkTimeTable, WrkCtrTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 55561
ms.assetid: 1953059f-478d-4706-b461-25b89ace5fc3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 47fe11168ad2ddea2a7033eda8d8bd8220efea32
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="production-setup-requirements"></a><span data-ttu-id="b63aa-103">Anforderungen für Produktionseinstellungen</span><span class="sxs-lookup"><span data-stu-id="b63aa-103">Production setup requirements</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="b63aa-104">Dieser Artikel gibt Informationen zu Einrichtungsanforderungen, bevor Sie mit der Produktionssteuerung arbeiten können.</span><span class="sxs-lookup"><span data-stu-id="b63aa-104">This article provides information about setup requirements before you can work with Production control.</span></span> 

<span data-ttu-id="b63aa-105">Produktionssteuerung wird mit Funktionen in anderen Modulen integriert.</span><span class="sxs-lookup"><span data-stu-id="b63aa-105">Production control is integrated with features in other modules.</span></span> <span data-ttu-id="b63aa-106">Dadurch besteht die Möglichkeit zum Ändern von Produktionsaufträgen, und es wird sichergestellt, dass diese automatisch in allen anderen zugehörigen Prozessen und Berechnungen des Systems aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="b63aa-106">This interconnectivity lets you change production orders and make sure that they are automatically updated in all other related processes and calculations in the system.</span></span> <span data-ttu-id="b63aa-107">Die folgenden Einrichtungsverfahren sind in der Reihenfolge aufgeführt, in der sie abgeschlossen werden sollten.</span><span class="sxs-lookup"><span data-stu-id="b63aa-107">The following setup processes are listed in the order that you should complete them in.</span></span>

## <a name="required-baseline-setup-in-other-modules"></a><span data-ttu-id="b63aa-108">Erforderliche Grundeinstellungen in anderen Modulen</span><span class="sxs-lookup"><span data-stu-id="b63aa-108">Required baseline setup in other modules</span></span>
<span data-ttu-id="b63aa-109">Vor der Verwendung des Moduls Produktionssteuerung müssen zunächst Informationen in anderen Modulen eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="b63aa-109">Information in other modules must be set up before you can work with Production control.</span></span> <span data-ttu-id="b63aa-110">Diese Einrichtung umfasst die folgenden Aufgaben:</span><span class="sxs-lookup"><span data-stu-id="b63aa-110">This setup includes the following tasks:</span></span>

-   <span data-ttu-id="b63aa-111">Einrichten der allgemeinen Unternehmensdaten</span><span class="sxs-lookup"><span data-stu-id="b63aa-111">Set up general company information.</span></span>
-   <span data-ttu-id="b63aa-112">Einrichten des Hauptbuchs</span><span class="sxs-lookup"><span data-stu-id="b63aa-112">Set up the general ledger.</span></span>
-   <span data-ttu-id="b63aa-113">Definieren von Artikelgruppen</span><span class="sxs-lookup"><span data-stu-id="b63aa-113">Define item groups.</span></span>
-   <span data-ttu-id="b63aa-114">Einrichten von Sachkonten für Artikelgruppen</span><span class="sxs-lookup"><span data-stu-id="b63aa-114">Set up ledger accounts for item groups.</span></span>
-   <span data-ttu-id="b63aa-115">Einrichten der Lagerartikeltabelle im Modul Bestandsverwaltung.</span><span class="sxs-lookup"><span data-stu-id="b63aa-115">Set up the inventory item table in Inventory management.</span></span>
-   <span data-ttu-id="b63aa-116">Erstellen Sie Stücklisten (BOMs) und Stücklistenversionen im Modul Bestandsverwaltung.</span><span class="sxs-lookup"><span data-stu-id="b63aa-116">Create bills of materials (BOMs) and BOM versions in Inventory management.</span></span>

## <a name="required-calendar-and-resource-setup"></a><span data-ttu-id="b63aa-117">Erforderliche Kalender- und Ressourceneinstellungen</span><span class="sxs-lookup"><span data-stu-id="b63aa-117">Required calendar and resource setup</span></span>
<span data-ttu-id="b63aa-118">Öffnen Sie vor der Verwendung des Moduls Produktionssteuerung das Modul Organisationsverwaltung, und erstellen bzw. definieren Sie den Kalender und die betrieblichen Ressourcen in der folgenden Reihenfolge:</span><span class="sxs-lookup"><span data-stu-id="b63aa-118">Before you use Production control, open Organization administration, and create and define the calendar and operations resources in the following order:</span></span>

1.  <span data-ttu-id="b63aa-119">**Schichtmodelle** – Richten Sie Schichtmodelle ein, und definieren Sie die Zeiten, die für die Planung der Produktion zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="b63aa-119">**Working time templates** – Set up working time templates to define the times that are available for production scheduling.</span></span>
2.  <span data-ttu-id="b63aa-120">**Kalender** – Richten Sie Arbeitszeitkalender ein, und definieren Sie, welche Tage des Jahres für die Planung der Produktion zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="b63aa-120">**Calendars** – Set up working time calendars to define the days of the year that are available for production scheduling.</span></span>
3.  <span data-ttu-id="b63aa-121">**Ressourcengruppen** – Ressourcengruppen einrichten, um die betrieblichen Ressourcen zu gruppieren, um eine Übersicht zu allen freien Kapazitäten zu erhalten, wenn die Planung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b63aa-121">**Resource groups** – Set up resource groups to group the operations resources, so that you can get an overview of any free capacity when you run scheduling.</span></span> <span data-ttu-id="b63aa-122">Sie müssen Ressourcengruppen nicht einrichten, bevor Sie betriebliche Ressourcen einrichten.</span><span class="sxs-lookup"><span data-stu-id="b63aa-122">You don't have to set up resource groups before you set up operations resources.</span></span> <span data-ttu-id="b63aa-123">Es empfiehlt sich jedoch, dass Sie wissen, wie man Ressourcen gruppiert, wenn Sie das Modul Produktionssteuerung einrichten.</span><span class="sxs-lookup"><span data-stu-id="b63aa-123">However, we recommend that you understand how to group resources when you set up Production control.</span></span>
4.  <span data-ttu-id="b63aa-124">**Ressourcen** – Richten Sie betrieblichen Ressourcen ein, um die Ressourcen festzulegen, die zum Ausführen des Produktionsvorgangs sowie zum Planen von Kapazitäten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b63aa-124">**Resources** – Set up operations resources to define the resources that are used to complete the production process and plan for capacity.</span></span>

## <a name="required-production-parameters-setup"></a><span data-ttu-id="b63aa-125">Erforderliche Einstellungen für Produktionsparameter</span><span class="sxs-lookup"><span data-stu-id="b63aa-125">Required production parameters setup</span></span>
<span data-ttu-id="b63aa-126">**Produktionssteuerungsparameter** – Richten Sie die grundlegenden Produktionsparameter ein, um die Behandlung und Verarbeitung von Produktionsaufträgen im System festzulegen.</span><span class="sxs-lookup"><span data-stu-id="b63aa-126">**Production control parameters** – Set up basic production parameters to define how the system handles and processes production orders.</span></span> <span data-ttu-id="b63aa-127">Definieren Sie, wie Produktionsaufträge erstellt, geplant und ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b63aa-127">Define how production orders are created, estimated, scheduled, and consumed.</span></span> <span data-ttu-id="b63aa-128">Darüber hinaus können Sie die gewünschte Rückmeldungsart sowie die gewünschte Ausführung der Kostenrechnung auswählen.</span><span class="sxs-lookup"><span data-stu-id="b63aa-128">You can also select what kind of feedback you want and how cost accounting is done.</span></span>

## <a name="required-journal-name-identification"></a><span data-ttu-id="b63aa-129">Erforderliche Angabe von Journalen</span><span class="sxs-lookup"><span data-stu-id="b63aa-129">Required journal name identification</span></span>
<span data-ttu-id="b63aa-130">**Produktionserfassungsnamen** – Geben Sie die Produktionserfassungsnamen an, die verwendet werden, um Buchungen zu registrieren und zu buchen.</span><span class="sxs-lookup"><span data-stu-id="b63aa-130">**Production journal names** – Specify the production journal names that are used to record and post transactions.</span></span>

## <a name="setup-if-you-use-operations"></a><span data-ttu-id="b63aa-131">Einrichten der Verwendung von Arbeitsgängen</span><span class="sxs-lookup"><span data-stu-id="b63aa-131">Setup if you use operations</span></span>
<span data-ttu-id="b63aa-132">Bei Arbeitsgängen handelt es sich um bestimmte Aktivitäten, die für die Produktion des Endprodukts abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="b63aa-132">Operations represent the specific activities that are completed to produce the finished product.</span></span> <span data-ttu-id="b63aa-133">**Hinweis:** Sie müssen die Aktivitätstypen kennen, die erforderlich sind, um den Artikel zu produzieren, und die Reihenfolge und Prioritäten dieser Aktivitäten.</span><span class="sxs-lookup"><span data-stu-id="b63aa-133">**Note:** You must know the types of activities that are required in order to produce your item, and the order and priorities of those activities.</span></span> <span data-ttu-id="b63aa-134">Sie müssen auch wissen, welche Ressourcen beteiligt sind und wie viele.</span><span class="sxs-lookup"><span data-stu-id="b63aa-134">You must also know which resources are involved, and how many.</span></span>

1.  <span data-ttu-id="b63aa-135">**Vorgänge** – Richten Sie Arbeitsgänge für die Aufgaben ein, die für die Produktion des Endprodukts ausgeführt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="b63aa-135">**Operations** – Set up operations to represent the tasks that must be completed to produce the finished item.</span></span>
2.  <span data-ttu-id="b63aa-136">**Beziehungen** – Richten mithilfe von Arbeitsgangzuordnungen detaillierte Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="b63aa-136">**Relations** – Set up operation relations to establish detailed properties.</span></span> <span data-ttu-id="b63aa-137">Um Arbeitsgangzuordnungen zu definieren, klicken Sie **Beziehungen** auf der **Vorgänge** Seite.</span><span class="sxs-lookup"><span data-stu-id="b63aa-137">To define operation relations, click **Relations** on the **Operations** page.</span></span>

## <a name="setup-if-you-use-routes"></a><span data-ttu-id="b63aa-138">Einrichten der Verwendung von Arbeitsplänen</span><span class="sxs-lookup"><span data-stu-id="b63aa-138">Setup if you use routes</span></span>
<span data-ttu-id="b63aa-139">Bei Verwendung von Arbeitsplänen müssen Arbeitsgänge für jeden einzelnen einzurichtenden Produktionsarbeitsplan vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="b63aa-139">If you're working with routes, operations must be defined for every production route that you set up.</span></span> <span data-ttu-id="b63aa-140">Bei dem Arbeitsplan handelt es sich um die Route für den Artikel auf seinem Weg von Arbeitsgang zu Arbeitsgang – ab dem Beginn des Produktionsvorgangs bis zu dessen Ende.</span><span class="sxs-lookup"><span data-stu-id="b63aa-140">The route represents the path that the item takes from operation to operation, from the start of the production process to the end.</span></span>

1.  <span data-ttu-id="b63aa-141">**Kostenkategorien** – Richten Sie Kostenkategorien ein, und definieren Sie die Kosten pro Stunde für bestimmte Vorgänge und Rüstzeiten.</span><span class="sxs-lookup"><span data-stu-id="b63aa-141">**Cost categories** – Set up cost categories to define the cost per hour of specified processes and setup times.</span></span>
2.  <span data-ttu-id="b63aa-142">**Kostengruppen** – Richten Sie Kostengruppen ein, um unterschiedliche Kostenrechnungsarten zu erstellen und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="b63aa-142">**Cost groups** – Set up cost groups to create and maintain different types of costing.</span></span>
3.  <span data-ttu-id="b63aa-143">**Arbeitsplangruppen** – Richten Sie Arbeitsplangruppen ein, und definieren Sie Parameter, die für Gruppen von Arbeitsplänen gelten sollen.</span><span class="sxs-lookup"><span data-stu-id="b63aa-143">**Route groups** – Set up route groups to define parameters that are related to groups of routes.</span></span> <span data-ttu-id="b63aa-144">Zum Erstellen von Produktionsarbeitsplänen müssen zunächst Arbeitsplangruppen eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="b63aa-144">You must set up route groups before you can create production routes.</span></span>
4.  <span data-ttu-id="b63aa-145">**Arbeitspläne** – Richten Sie Produktionsarbeitspläne ein, und definieren Sie Standardeinstellungen zum Steuern von Planung, Kostenrechnung/Preisgestaltung für Arbeitsplan-Arbeitsgänge sowie von Statusberichten.</span><span class="sxs-lookup"><span data-stu-id="b63aa-145">**Routes** – Set up production routes, and define default settings to control scheduling, costing, and pricing of route operations, and to control progress reporting.</span></span>
5.  <span data-ttu-id="b63aa-146">**Arbeitspläne** – Richten Sie Arbeitsplanversionen ein, um in der Produktion die Verwendung von Artikelvarianten zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="b63aa-146">**Routes** – Set up route versions to enable item variations in production.</span></span>

## <a name="optional-advanced-settings"></a><span data-ttu-id="b63aa-147">Optionale erweiterte Einstellungen</span><span class="sxs-lookup"><span data-stu-id="b63aa-147">Optional advanced settings</span></span>
1.  <span data-ttu-id="b63aa-148">**Produktionsgruppen** – Richten Sie Produktionsgruppen ein, um Beziehungen zwischen dem Produktionsauftrag und den Sachkonten herzustellen.</span><span class="sxs-lookup"><span data-stu-id="b63aa-148">**Production groups** – Set up production groups to establish relationships between the production order and ledger accounts.</span></span> <span data-ttu-id="b63aa-149">Die Sachkonten dienen zum Buchen oder zum Gruppieren von Aufträgen für die Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="b63aa-149">The ledger accounts are used to post or group orders for reporting.</span></span>
2.  <span data-ttu-id="b63aa-150">**Produktionspools** – Erstellen Sie Produktionspools zum Gruppieren von Produktionsaufträgen ein, sodass Sie dringende Produktionsaufträge verarbeiten oder Auftragsgruppen löschen und buchen können.</span><span class="sxs-lookup"><span data-stu-id="b63aa-150">**Production pools** – Create production pools to group production orders so that you can process urgent production orders, or delete and post groups of orders.</span></span>
3.  <span data-ttu-id="b63aa-151">**Eigenschaften** – Sie können Eigenschaften festlegen, um spezielle Attribute zu erstellen, die Ressourcen zugewiesen werden können, um die Reihenfolge der Produktionen zu steuern.</span><span class="sxs-lookup"><span data-stu-id="b63aa-151">**Properties** – Define properties to create special attributes that you can assign to your resources to control the order of productions.</span></span> <span data-ttu-id="b63aa-152">Diese Attribute sind mit dem Schichtplan verbunden.</span><span class="sxs-lookup"><span data-stu-id="b63aa-152">These attributes are connected to the working time template.</span></span>





