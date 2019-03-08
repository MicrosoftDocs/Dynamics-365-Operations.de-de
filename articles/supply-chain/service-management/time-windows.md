---
title: Zeitfenster
description: Sie können Zeitfenster verwenden, um die Planung von Serviceauftragspositionen zu optimieren.
author: ShylaThompson
manager: AnnBe
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMATimeAgreement
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6f748268f6cb85ff835919485da2828689eee23c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "347214"
---
# <a name="time-windows"></a><span data-ttu-id="af0af-103">Zeitfenster</span><span class="sxs-lookup"><span data-stu-id="af0af-103">Time windows</span></span>  

[!include [banner](../includes/banner.md)]

<span data-ttu-id="af0af-104">Sie können Zeitfenster verwenden, um die Planung von Serviceauftragspositionen zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="af0af-104">You can use time windows to optimize the scheduling of service order lines.</span></span> <span data-ttu-id="af0af-105">Sie können das System so einrichten, dass es automatisch Serviceaufträge erstellt.</span><span class="sxs-lookup"><span data-stu-id="af0af-105">You can set up the system so that it automatically creates service orders.</span></span> <span data-ttu-id="af0af-106">Basierend auf den Kriterien, die durch ein Zeitfenster angegeben sind, können Sie möglichst viel Serviceauftragspositionen herstellen, die mit möglichst wenigen Serviceaufträgen verbinden werden können.</span><span class="sxs-lookup"><span data-stu-id="af0af-106">Based on the criteria specified by a time window, you can connect as many service order lines as possible to as few service orders as possible.</span></span>

<span data-ttu-id="af0af-107">Zeitfenster legen fest, wie weit eine Serviceauftragsposition in Bezug auf das berechnete Datum verschoben werden kann.</span><span class="sxs-lookup"><span data-stu-id="af0af-107">Time windows specify how far a service order line can move from its calculated date.</span></span> <span data-ttu-id="af0af-108">Das berechnete Datum ist das Datum, an dem die Serviceauftragsposition geplant war.</span><span class="sxs-lookup"><span data-stu-id="af0af-108">The calculated date is the date when the service order line was scheduled to occur.</span></span> <span data-ttu-id="af0af-109">Das Datum basiert auf der Intervalleinstellung und der Serviceperiode, die Sie im Formular **Serviceauftrag erstellen** definiert haben.</span><span class="sxs-lookup"><span data-stu-id="af0af-109">The date is based on its interval setting and the service period that you defined in the **Create service orders** page.</span></span> <span data-ttu-id="af0af-110">Ein Zeitfenster wird unter Verwendung der Werte in der folgenden Tabelle festgelegt.</span><span class="sxs-lookup"><span data-stu-id="af0af-110">You define a time window by using the values in the following table.</span></span>

| <span data-ttu-id="af0af-111">Methode</span><span class="sxs-lookup"><span data-stu-id="af0af-111">Method</span></span> | <span data-ttu-id="af0af-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="af0af-112">Description</span></span>                                                                                                                                                                                                                                                                                           |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af0af-113">Woche</span><span class="sxs-lookup"><span data-stu-id="af0af-113">Week</span></span>   | <span data-ttu-id="af0af-114">Das Datum, zu dem die Serviceauftragsposition verschoben werden kann, ist jeder offene Tag innerhalb der gleichen Woche wie das ursprüngliche berechnete Datum.</span><span class="sxs-lookup"><span data-stu-id="af0af-114">The date that the service order line can be moved to any open day in the same week as the initial calculated date.</span></span>                                                                                                                                                                                    |
| <span data-ttu-id="af0af-115">Monat</span><span class="sxs-lookup"><span data-stu-id="af0af-115">Month</span></span>  | <span data-ttu-id="af0af-116">Das Datum, zu dem die Serviceauftragsposition verschoben werden kann, ist jeder offene Tag innerhalb des gleichen Monats wie das ursprüngliche berechnete Datum.</span><span class="sxs-lookup"><span data-stu-id="af0af-116">The date that the service order line can be moved to any open day in the same month as the initial calculated date.</span></span> <span data-ttu-id="af0af-117">Beispielsweise ist das berechnete Datum für eine Serviceauftragsposition. der 15. Februar 2017.</span><span class="sxs-lookup"><span data-stu-id="af0af-117">For example, the calculated date for a service order line is February 15, 2017.</span></span> <span data-ttu-id="af0af-118">Die kann Serviceauftragsposition für einen beliebigen Wochentag und dem 28. Februar 2017 zwischen dem 1. Februar geplant werden.</span><span class="sxs-lookup"><span data-stu-id="af0af-118">The service order line can be scheduled for any weekday between February 1 and February 28, 2017.</span></span> |
| <span data-ttu-id="af0af-119">Manuell</span><span class="sxs-lookup"><span data-stu-id="af0af-119">Manual</span></span> | <span data-ttu-id="af0af-120">Sie können die maximale Zahl von Tagen vor oder nach dem ursprünglichen berechneten Datum für das Verschieben der Serviceauftragsposition festlegen.</span><span class="sxs-lookup"><span data-stu-id="af0af-120">You define the maximum number of days before or after the initial calculated date that the service order line can be moved.</span></span>                                                                                                                                                                           |

<span data-ttu-id="af0af-121">Wenn für eine Servicevereinbarungsposition kein Zeitfenster angegeben wird, muss die aus der Servicevereinbarung abgeleitete Serviceauftragsposition genau an dem ursprünglich geplanten Datum ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="af0af-121">If you do not specify a time window for a service agreement line, the service order line that is derived from the service agreement must be on the exact date for which it was originally scheduled.</span></span>

## <a name="related-topics"></a><span data-ttu-id="af0af-122">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="af0af-122">Related topics</span></span>

[<span data-ttu-id="af0af-123">Erstellen von Zeitfenstern</span><span class="sxs-lookup"><span data-stu-id="af0af-123">Create time windows</span></span>](create-time-windows.md)

