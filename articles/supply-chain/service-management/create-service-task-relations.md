---
title: Erstellen von Serviceaufgabenbeziehungen
description: Sie können Serviceaufgaben Servicevereinbarungen oder Serviceaufträgen zuordnen, um die Serviceaufgabe zu beschreiben, die für die Vereinbarung oder den Auftrag ausgeführt werden soll.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b167714dc81cf0e4ee70d7092f2ec030043abe71
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3202605"
---
# <a name="create-service-task-relations"></a><span data-ttu-id="50832-103">Erstellen von Serviceaufgabenbeziehungen</span><span class="sxs-lookup"><span data-stu-id="50832-103">Create service task relations</span></span>    

[!include [banner](../includes/banner.md)]

<span data-ttu-id="50832-104">Sie können Serviceaufgaben Servicevereinbarungen oder Serviceaufträgen zuordnen, um die Serviceaufgabe zu beschreiben, die für die Vereinbarung oder den Auftrag ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="50832-104">You can associate service tasks with service agreements or service orders in order to describe the service task to be completed for the agreement or order.</span></span> <span data-ttu-id="50832-105">Diese Informationen stehen Servicetechnikern und Debitoren zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="50832-105">This information is available to service technicians and customers.</span></span>

## <a name="create-a-relation-with-a-service-agreement"></a><span data-ttu-id="50832-106">Erstellen einer Beziehung mit einer Servicevereinbarung</span><span class="sxs-lookup"><span data-stu-id="50832-106">Create a relation with a service agreement</span></span>

1.  <span data-ttu-id="50832-107">Klicken Sie auf den Bereichsseitenknoten: **Serviceverwaltung** \> **Gemeinsam** \> **Servicevereinbarungen** \> **Servicevereinbarungen**.</span><span class="sxs-lookup"><span data-stu-id="50832-107">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="50832-108">Wählen Sie eine vorhandene Servicevereinbarung aus, oder erstellen Sie eine neue.</span><span class="sxs-lookup"><span data-stu-id="50832-108">Select an existing service agreement, or create a new service agreement.</span></span>

3.  <span data-ttu-id="50832-109">Klicken Sie im Aktivitätsbereich auf die Schaltfläche **Serviceaufgaben**.</span><span class="sxs-lookup"><span data-stu-id="50832-109">On the Action Pane, click the **Service tasks** button.</span></span>

4.  <span data-ttu-id="50832-110">Drücken Sie im Formular **Serviceaufgaben** die Tastenkombination STRG+N, um eine neue Position zu erstellen. Wählen Sie in der Liste **Serviceaufgaben** dann eine Serviceaufgabe aus, um die Serviceaufgabe der Servicevereinbarung zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="50832-110">On the **Service tasks** form, press CTRL+N to create a new line, and then select a service task from the **Service task** list to attach the service task to the service agreement.</span></span>

5.  <span data-ttu-id="50832-111">Geben Sie in die Freitextfelder der Registerkarte **Beschreibung** interne oder externe Hinweise ein.</span><span class="sxs-lookup"><span data-stu-id="50832-111">On the **Description** tab, enter any internal or external note descriptions in the free text fields.</span></span>

6.  <span data-ttu-id="50832-112">Schließen Sie das Formular, um den Datensatz zu speichern.</span><span class="sxs-lookup"><span data-stu-id="50832-112">Close the form to save the record.</span></span>

<span data-ttu-id="50832-113">Wiederholen Sie diese Schritte, bis alle erforderlichen Serviceaufgabenbeziehungen für die Servicevereinbarung erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="50832-113">Repeat this procedure until you have created all the necessary service task relations for the service agreement.</span></span> <span data-ttu-id="50832-114">Anschließend können die Serviceaufgaben für beliebige zugeordnete Vereinbarungspositionen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="50832-114">You can now specify these service tasks for any attached agreement lines.</span></span>

<span data-ttu-id="50832-115">Eine für eine Servicevereinbarung erstellte Serviceaufgabenbeziehung ist in allen Serviceaufträgen verfügbar, die der Servicevereinbarung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="50832-115">A service tasks relation that is created on a service agreement is available from all service orders that are attached to the service agreement.</span></span>

## <a name="create-a-relation-with-a-service-order"></a><span data-ttu-id="50832-116">Erstellen einer Beziehung mit einem Serviceauftrag</span><span class="sxs-lookup"><span data-stu-id="50832-116">Create a relation with a service order</span></span>

1.  <span data-ttu-id="50832-117">Klicken auf **Serviceverwaltung** \> **Gemeinsam** \> **Serviceaufträge** \> **Serviceaufträge**.</span><span class="sxs-lookup"><span data-stu-id="50832-117">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="50832-118">Wählen Sie einen vorhandenen Serviceauftrag aus, oder erstellen Sie einen neuen.</span><span class="sxs-lookup"><span data-stu-id="50832-118">Select an existing service order, or create a new service order.</span></span>

3.  <span data-ttu-id="50832-119">Klicken Sie im Aktivitätsbereich auf die Schaltfläche **Serviceaufgaben**.</span><span class="sxs-lookup"><span data-stu-id="50832-119">On the Action Pane, click the **Service tasks** button.</span></span>

4.  <span data-ttu-id="50832-120">Drücken Sie im Formular **Serviceaufgaben** die Tastenkombination STRG+N, um eine neue Position zu erstellen. Wählen Sie in der Liste **Serviceaufgaben** dann eine Serviceaufgabe aus, um die Serviceaufgabe der Servicevereinbarung zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="50832-120">From the **Service tasks** form, press CTRL+N to create a new line, and then select a service task from the **Service task** list to attach the service tasks to the service order.</span></span>

5.  <span data-ttu-id="50832-121">Geben Sie in die Freitextfelder der Registerkarte **Beschreibung** interne oder externe Hinweise ein.</span><span class="sxs-lookup"><span data-stu-id="50832-121">On the **Description** tab, enter any internal or external note descriptions in the free text fields.</span></span>

6.  <span data-ttu-id="50832-122">Schließen Sie das Formular, um den Datensatz zu speichern.</span><span class="sxs-lookup"><span data-stu-id="50832-122">Close the form to save the record.</span></span>

<span data-ttu-id="50832-123">Wiederholen Sie diese Schritte, bis alle erforderlichen Serviceaufgabenbeziehungen für die Servicevereinbarung erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="50832-123">Repeat this procedure until you have created all the necessary service task relations for the service order.</span></span> <span data-ttu-id="50832-124">Die Serviceaufgabe, für die die Beziehung erstellt wurde, kann nun beim Erstellen von Serviceauftragspositionen ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="50832-124">You can now select the service task for which you have created the relation when you create service order lines.</span></span>

<span data-ttu-id="50832-125">Für einen Serviceauftrag erstellte Serviceaufgabenbeziehungen sind für den speziellen Serviceauftrag verfügbar.</span><span class="sxs-lookup"><span data-stu-id="50832-125">Service task relations that are created on a service order are available on the specific service order.</span></span>

## <a name="see-also"></a><span data-ttu-id="50832-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="50832-126">See also</span></span>

[<span data-ttu-id="50832-127">Serviceaufgaben – Übersicht</span><span class="sxs-lookup"><span data-stu-id="50832-127">Service tasks overview</span></span>](service-tasks.md)


  


