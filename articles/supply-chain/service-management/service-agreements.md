---
title: "Serviceverträge"
description: "In Serviceverträgen können Sie die Ressourcen definieren, die für einen typischen Servicebesuch benötigt werden, und festlegen, wie diese Ressourcen dem Debitor in Rechnung gestellt werden sollen."
author: YuyuScheller
manager: AnnBe
ms.date: 02/19/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAAgreementTable
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
ms.sourcegitcommit: bf9df2a31c758ba6b63ac7952e00065df04552dc
ms.openlocfilehash: aaff0c1d71fcf2656d5d6e76a2bf4b7b3a699281
ms.contentlocale: de-de
ms.lasthandoff: 02/19/2018

---

# <a name="service-agreements"></a><span data-ttu-id="9b538-103">Serviceverträge</span><span class="sxs-lookup"><span data-stu-id="9b538-103">Service agreements</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="9b538-104">In Serviceverträgen können Sie die Ressourcen definieren, die für einen typischen Servicebesuch benötigt werden, und festlegen, wie diese Ressourcen dem Debitor in Rechnung gestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9b538-104">Service agreements let you define the resources that are used in a typical service visit and how those resources are invoiced to the customer.</span></span>

<span data-ttu-id="9b538-105">Jeder Servicevertrag ist einem Projekt zugeordnet, durch das Buchungen ausgeführt und fakturiert werden.</span><span class="sxs-lookup"><span data-stu-id="9b538-105">Every service agreement is attached to a project through which transactions are posted and invoiced.</span></span> <span data-ttu-id="9b538-106">Sie haben jedoch auch die Möglichkeit, zum direkten Ausführen von Serviceauftragsbuchungen durch das Projekt, ohne zuvor eine Verbindung des Serviceauftrags mit einem Servicevertrag herstellen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="9b538-106">However, you can also invoice service order transactions directly through the project without first having to connect the service order to a service agreement.</span></span> <span data-ttu-id="9b538-107">Dies ist möglicherweise hilfreich, wenn es sich bei dem Serviceauftrag um einen einmaligen Servicebesuch handelt und die schnelle Bearbeitung der Servicebuchungen einen höheren Stellenwert einnimmt als die Erfassung ausführlicher Servicevereinbarungsdaten zum Debitor über einen längeren Zeitraum.</span><span class="sxs-lookup"><span data-stu-id="9b538-107">You might decide to do this if the service order is for a one-time-only service visit and the need for processing the service transactions quickly outweighs the need for maintaining detailed service-agreement information about the customer over a period of time.</span></span>

## <a name="service-agreement"></a><span data-ttu-id="9b538-108">Servicevereinbarung</span><span class="sxs-lookup"><span data-stu-id="9b538-108">Service agreement</span></span>

<span data-ttu-id="9b538-109">In jedem Servicevertrag müssen ein Projekt, eine Servicevertragskennung sowie eine Servicevertragsgruppe angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9b538-109">In each service agreement, you must specify a project, a service-agreement ID, and a service-agreement group.</span></span> <span data-ttu-id="9b538-110">Die Servicevertragsgruppe dient zum Sortieren und Organisieren von Serviceverträgen.</span><span class="sxs-lookup"><span data-stu-id="9b538-110">The service-agreement group can be used to sort and organize service agreements.</span></span>

<span data-ttu-id="9b538-111">Ein Servicevertragskopf enthält Einstellungen für alle zugeordneten Vertragspositionen:</span><span class="sxs-lookup"><span data-stu-id="9b538-111">A service agreement header contains settings that apply to all attached agreement lines:</span></span>

-  <span data-ttu-id="9b538-112">Aussetzungsstatus der Servicevereinbarung.</span><span class="sxs-lookup"><span data-stu-id="9b538-112">Whether the service agreement is suspended.</span></span> <span data-ttu-id="9b538-113">Ist die Servicevereinbarung ausgesetzt, können auf Basis dieser Servicevereinbarung keine Serviceaufträge generiert werden.</span><span class="sxs-lookup"><span data-stu-id="9b538-113">If the service agreement is suspended, you cannot generate service orders from the service agreement.</span></span>
-  <span data-ttu-id="9b538-114">Dauer der Servicevereinbarung</span><span class="sxs-lookup"><span data-stu-id="9b538-114">The duration of the service agreement.</span></span>
-  <span data-ttu-id="9b538-115">Angaben zur Kombinierung von Serviceauftragspositionen zu Serviceaufträgen</span><span class="sxs-lookup"><span data-stu-id="9b538-115">How service-order lines are to be combined into service orders.</span></span>
-  <span data-ttu-id="9b538-116">Vorlagenstatus des Servicevertrags.</span><span class="sxs-lookup"><span data-stu-id="9b538-116">Whether the service agreement is a template.</span></span>

<span data-ttu-id="9b538-117">Im Kopf der Servicevereinbarung werden auch alle Serviceobjekte und -aufgaben eingerichtet, die für die Servicevereinbarung zur Verfügung stehen sollen. Geben Sie dazu die jeweiligen Serviceaufgaben oder Serviceobjekte ein, die den verschiedenen Positionen des Vertrags zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9b538-117">In the service-agreement header, you also set up all the service objects and service tasks that can be used with the service agreement by entering the specific service tasks or service objects that are to be attached to the various lines of the agreement.</span></span>

<span data-ttu-id="9b538-118">Aus dem Kopf des Servicevertrags lassen sich auch Servicevertrags- oder Servicevorlagenpositionen in den aktuellen Servicevertrag kopieren.</span><span class="sxs-lookup"><span data-stu-id="9b538-118">From the service-agreement header, you can also copy service-agreement lines or service-template lines into the current service agreement.</span></span>

<span data-ttu-id="9b538-119">Sie können Serviceverträge aussetzen und einzelne Servicevertragspositionen beenden.</span><span class="sxs-lookup"><span data-stu-id="9b538-119">You can suspend service agreements and stop individual service agreement lines.</span></span>

<span data-ttu-id="9b538-120">Wenn Sie das Kontrollkästchen **Unterbrochen** für eine Servicevertragsposition aktivieren, können Sie Folgendes nicht durchführen:</span><span class="sxs-lookup"><span data-stu-id="9b538-120">If you select the **Suspended** check box on a service agreement, you cannot:</span></span>

-    <span data-ttu-id="9b538-121">Serviceaufträge aus der Servicevereinbarung automatisch oder manuell erstellen.</span><span class="sxs-lookup"><span data-stu-id="9b538-121">Create service orders automatically or manually from the service agreement.</span></span>

<span data-ttu-id="9b538-122">Wenn Sie das Kontrollkästchen **Anhalten** für eine Servicevertragsposition aktivieren, können Sie Folgendes nicht durchführen:</span><span class="sxs-lookup"><span data-stu-id="9b538-122">If you select the **Stopped** check box on a service agreement line, you cannot:</span></span>

-    <span data-ttu-id="9b538-123">Serviceaufträge aus der Servicevereinbarungsposition automatisch oder manuell erstellen.</span><span class="sxs-lookup"><span data-stu-id="9b538-123">Create service orders automatically or manually from the service agreement line.</span></span>
-    <span data-ttu-id="9b538-124">Servicevereinbarungsposition in eine andere Servicevereinbarung oder einen anderen Serviceauftrag kopieren.</span><span class="sxs-lookup"><span data-stu-id="9b538-124">Copy the service agreement line into another service agreement or service order.</span></span>


> [!NOTE]
> <span data-ttu-id="9b538-125">Wenn ein Servicevertrag ausgesetzt ist, werden alle zugeordneten Positionen unabhängig von ihrem jeweiligen Status beendet.</span><span class="sxs-lookup"><span data-stu-id="9b538-125">If a service agreement is suspended, all the attached lines are stopped, regardless of their individual status.</span></span>

## <a name="service-agreement-lines"></a><span data-ttu-id="9b538-126">Servicevertragspositionen</span><span class="sxs-lookup"><span data-stu-id="9b538-126">Service-agreement lines</span></span>

<span data-ttu-id="9b538-127">In jeder Servicevertragsposition wird der Inhalt der erforderlichen Servicearbeiten ausführlich beschrieben.</span><span class="sxs-lookup"><span data-stu-id="9b538-127">Each service-agreement line describes in detail the content of the proposed service work.</span></span> <span data-ttu-id="9b538-128">Die Positionen enthalten die folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="9b538-128">The lines contain the following settings:</span></span>

-  <span data-ttu-id="9b538-129">Die Buchungsart sowie eine Beschreibung der Buchungsart</span><span class="sxs-lookup"><span data-stu-id="9b538-129">The transaction type and the description of the transaction type.</span></span>
-  <span data-ttu-id="9b538-130">Den Mitarbeiter, von dem die Servicearbeiten ausgeführt werden</span><span class="sxs-lookup"><span data-stu-id="9b538-130">The employee who performs the service work.</span></span>
-  <span data-ttu-id="9b538-131">Die Objekte, für die der Service im Rahmen der Servicevereinbarung erbracht werden soll</span><span class="sxs-lookup"><span data-stu-id="9b538-131">The objects on which service must be performed for the service agreement.</span></span>
-  <span data-ttu-id="9b538-132">Die Häufigkeit, mit der die Arbeiten ausgeführt und die Artikel-, Spesen- und Gebührenbuchungen erfasst werden</span><span class="sxs-lookup"><span data-stu-id="9b538-132">The frequency with which work is performed and associated item, expense, and fee transactions are registered.</span></span>
-  <span data-ttu-id="9b538-133">Das Zeitfenster für die Gruppierung von Serviceauftragspositionen zu einem Serviceauftrag.</span><span class="sxs-lookup"><span data-stu-id="9b538-133">The time window within which service-order lines can be grouped into a service order.</span></span>
-  <span data-ttu-id="9b538-134">Die Serviceaufgaben zum Gruppieren von Vertragspositionssätzen zu Arbeitsaufgaben sowie für Zusammenfassungen der auszuführenden Serviceaufgaben für Servicetechniker und Debitoren.</span><span class="sxs-lookup"><span data-stu-id="9b538-134">The service tasks that are used to group sets of agreement lines together into work tasks and to summarize for service technicians and customers what service task is to be provided.</span></span>
-  <span data-ttu-id="9b538-135">Den Status einer Position.</span><span class="sxs-lookup"><span data-stu-id="9b538-135">Whether a line is stopped.</span></span> <span data-ttu-id="9b538-136">Wurde eine Position beendet, können für diese Position keine Serviceaufträge erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="9b538-136">If a line is stopped, you cannot create service orders for that individual line.</span></span>
-  <span data-ttu-id="9b538-137">Die Projekteinstellungen wie Kategorie oder Abrechnungscode.</span><span class="sxs-lookup"><span data-stu-id="9b538-137">Project settings, such as the category and the line property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9b538-138">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="9b538-138">Related topics</span></span>

[<span data-ttu-id="9b538-139">Erstellen von Servicevereinbarungen</span><span class="sxs-lookup"><span data-stu-id="9b538-139">Create service agreements</span></span>](create-service-agreements.md)
