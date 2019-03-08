---
title: Automatisches Erstellen von Serviceaufträgen
description: Serviceaufträge können auf der Grundlage einer Servicevereinbarung für die Gültigkeitsperiode der Servicevereinbarung generiert werden.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
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
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0189a9f99ffbb6ed2387211ba9e3b9f3bcdb3b52
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "331183"
---
# <a name="automatically-create-service-orders"></a><span data-ttu-id="46ff6-103">Automatisches Erstellen von Serviceaufträgen</span><span class="sxs-lookup"><span data-stu-id="46ff6-103">Automatically create service orders</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="46ff6-104">Serviceaufträge können auf der Grundlage einer Servicevereinbarung für die Gültigkeitsperiode der Servicevereinbarung generiert werden.</span><span class="sxs-lookup"><span data-stu-id="46ff6-104">You can generate service orders that are based on a service agreement for the valid period of the service agreement.</span></span>

<span data-ttu-id="46ff6-105">Die Serviceaufträge, die auf Basis einer Servicevereinbarung generiert werden, sind alle der entsprechenden Servicevereinbarung zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="46ff6-105">The service orders that you generate from a service agreement are all attached to the service agreement.</span></span>

<span data-ttu-id="46ff6-106">Serviceaufträge werden automatisch gemäß den folgenden Einstellungen generiert:</span><span class="sxs-lookup"><span data-stu-id="46ff6-106">Service orders are generated automatically from the following settings:</span></span>

  - <span data-ttu-id="46ff6-107">Das in den Servicevereinbarungspositionen eingerichtete Servicevereinbarungsintervall.</span><span class="sxs-lookup"><span data-stu-id="46ff6-107">The service agreement interval that is set up in the service agreement lines.</span></span> <span data-ttu-id="46ff6-108">Mit dem Servicevereinbarungsintervall wird die Erstellungshäufigkeit der Servicevereinbarungspositionen angegeben.</span><span class="sxs-lookup"><span data-stu-id="46ff6-108">The service agreement interval indicates the frequency that service-order lines are created.</span></span> <span data-ttu-id="46ff6-109">Weitere Informationen zu Serviceintervallen finden Sie unter [Serviceintervalle](service-intervals.md).</span><span class="sxs-lookup"><span data-stu-id="46ff6-109">For more information, see [Service intervals](service-intervals.md).</span></span>

  - <span data-ttu-id="46ff6-110">Die angegebene Periode zum Definieren der Serviceperiode (in den Feldern **Von Datum** und **Bis Datum** des Formulars **Erstellen von Serviceaufträgen**).</span><span class="sxs-lookup"><span data-stu-id="46ff6-110">The period that you specify to define the service period in the **From date** and **To date** fields in the **Create service orders** form.</span></span> <span data-ttu-id="46ff6-111">Weitere Informationen zum Erstellen von Serviceaufträgen finden Sie unter [Automatische Erstellung von Serviceaufträgen](create-service-orders-automatically.md).</span><span class="sxs-lookup"><span data-stu-id="46ff6-111">For more information, see [Create service orders automatically](create-service-orders-automatically.md).</span></span>

  - <span data-ttu-id="46ff6-112">Die Option **Serviceaufträge kombinieren** im Servicevertragskopf.</span><span class="sxs-lookup"><span data-stu-id="46ff6-112">The **Combine service orders** option on the service agreement header.</span></span> <span data-ttu-id="46ff6-113">Mit dieser Option wird definiert, ob Serviceaufträge anhand von Serviceauftragspositionen, die für eine Servicevereinbarung generiert werden, nach Mitarbeiter, Serviceaufgabe, Serviceobjekt oder nach Servicevereinbarung kombiniert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="46ff6-113">This option defines whether service order lines generated from a service agreement, combines service orders according to employee, service task, service object, or service agreement.</span></span> <span data-ttu-id="46ff6-114">Weitere Informationen zur Kombination von Serviceaufträgen finden Sie unter [Serviceaufträge kombinieren](combine-service-orders.md).</span><span class="sxs-lookup"><span data-stu-id="46ff6-114">For more information, see [Combine service orders](combine-service-orders.md).</span></span>

  - <span data-ttu-id="46ff6-115">Die Option **Zeitfenster** in der Servicevereinbarungsposition.</span><span class="sxs-lookup"><span data-stu-id="46ff6-115">The **Time window** option on the service agreement line.</span></span> <span data-ttu-id="46ff6-116">Durch das Zeitfenster wird definiert, wie weit eine Servicevereinbarungsposition relativ zu ihrem berechneten Datum verschoben werden kann.</span><span class="sxs-lookup"><span data-stu-id="46ff6-116">The time window defines how far a service order line can move with regard to its calculated date.</span></span> <span data-ttu-id="46ff6-117">Weitere Informationen zu Zeitfenstern finden Sie unter [Zeitfenster](time-windows.md).</span><span class="sxs-lookup"><span data-stu-id="46ff6-117">For more information, see [Time windows](time-windows.md).</span></span>


> [!NOTE]
> <P><span data-ttu-id="46ff6-118">Ist der für einen Serviceauftrag angegebene Tag in dem Kalender, der im Formular <STRONG>Serviceverwaltungsparameter</STRONG> ausgewählt ist, nicht offen, wird eine Meldung mit einem entsprechenden Hinweis angezeigt.</span><span class="sxs-lookup"><span data-stu-id="46ff6-118">If the day that is specified for a service order is not open in the calendar that you have selected in the <STRONG>Service management parameters</STRONG> form, a message will indicate that there is a calendar conflict.</span></span> <span data-ttu-id="46ff6-119">Diese Meldung kann ignoriert werden. Der Serviceauftrag wird auch dann erstellt, wenn der Tag im Kalender geschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="46ff6-119">You can safely ignore the message; the service order will be created, even though the day is closed on the calendar.</span></span></P>

## <a name="example-1"></a><span data-ttu-id="46ff6-120">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="46ff6-120">Example 1</span></span>

<span data-ttu-id="46ff6-121">Die Servicevereinbarung gilt vom 1. Januar 2012 bis zum 31. Dezember 2012.</span><span class="sxs-lookup"><span data-stu-id="46ff6-121">The service agreement lasts from January 1, 2012 until December 31, 2012.</span></span> <span data-ttu-id="46ff6-122">Liegt die im Formular **Erstellen von Serviceaufträgen** angegebene Serviceperiode zwischen dem 1. November 2012 und dem 1. Februar 2013, werden Serviceaufträge vom 1. November 2012 bis zum 31. Dezember 2012 erstellt.</span><span class="sxs-lookup"><span data-stu-id="46ff6-122">If the service period that you specify in the **Create service orders** form is from November 1, 2012 until February 1, 2013, service orders are created from November 1, 2012 until December 31, 2012.</span></span>

## <a name="example-2"></a><span data-ttu-id="46ff6-123">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="46ff6-123">Example 2</span></span>

<span data-ttu-id="46ff6-124">Die Servicevereinbarung gilt vom 1. Januar 2012 bis zum 31. Dezember 2012.</span><span class="sxs-lookup"><span data-stu-id="46ff6-124">The service agreement lasts from January 1, 2012 until December 31, 2012.</span></span> <span data-ttu-id="46ff6-125">Der Servicevereinbarung sind zwei Servicevereinbarungspositionen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="46ff6-125">Two service agreement lines are attached to the service agreement.</span></span> <span data-ttu-id="46ff6-126">Die eine Servicevereinbarungsposition besitzt als Startdatum den 2. Januar 2012 und als Enddatum den 1. März 2012.</span><span class="sxs-lookup"><span data-stu-id="46ff6-126">The first service agreement line has a starting date on January 2, 2012 and an ending date on March 1, 2012.</span></span> <span data-ttu-id="46ff6-127">Die andere Servicevereinbarungsposition besitzt als Startdatum den 1. April 2012 und als Enddatum den 31. Dezember 2012.</span><span class="sxs-lookup"><span data-stu-id="46ff6-127">The second service agreement line has a starting date on April 1, 2012 and an ending date on December 31, 2012.</span></span> <span data-ttu-id="46ff6-128">Im Formular **Erstellen von Serviceaufträgen** geben Sie eine Periode vom 1. Oktober 2012 bis zum 31. Dezember 2012 an.</span><span class="sxs-lookup"><span data-stu-id="46ff6-128">You specify a period in the **Create service orders** form that is from October 1, 2012 until December 31, 2012.</span></span> <span data-ttu-id="46ff6-129">Aus diesem Grund werden lediglich Serviceaufträge für die zweite Vereinbarungsposition generiert, da das Start- und das Enddatum der ersten Vereinbarungsposition vor der Periode liegen, die für den Serviceauftrag angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="46ff6-129">Therefore, service orders are generated only for the second agreement line, because the starting date and ending date of the first agreement line are before the period that you specified for the service order.</span></span>

  


