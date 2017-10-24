--- 
title: " Einen Einzelvorgang konfigurieren und aktivieren, um Auszüge zu berechnen"
description: "Diese Prozedur führt Sie Schritt für Schritt durch das Konfigurieren und Ausführen von wiederkehrenden Batchaufträgen zum Erstellen und Berechnen von Auszügen für einen ausgewählten Shop oder eine Gruppe von Shops."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2bae81073fa6561c02d2dac0cd83db6a10ad00c3
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="configure-and-run-a-job-to-calculate-statements"></a><span data-ttu-id="371ab-103"> Einen Einzelvorgang konfigurieren und aktivieren, um Auszüge zu berechnen</span><span class="sxs-lookup"><span data-stu-id="371ab-103">Configure and run a job to calculate statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="371ab-104">Diese Prozedur führt Sie Schritt für Schritt durch das Konfigurieren und Ausführen von wiederkehrenden Batchaufträgen zum Erstellen und Berechnen von Auszügen für einen ausgewählten Shop oder eine Gruppe von Shops.</span><span class="sxs-lookup"><span data-stu-id="371ab-104">This procedure walks through configuring and running recurrent batch jobs to create and calculate statements for a selected store or group of stores.</span></span> <span data-ttu-id="371ab-105">Für diese Prozedur wird das Demo-Datenunternehmen USRT verwendet.</span><span class="sxs-lookup"><span data-stu-id="371ab-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="371ab-106">Wechseln Sie zu Alle Arbeitsbereiche > Finanzdaten für den Einzelhandelsshop.</span><span class="sxs-lookup"><span data-stu-id="371ab-106">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="371ab-107">Klicken Sie auf "Auszüge berechnen".</span><span class="sxs-lookup"><span data-stu-id="371ab-107">Click Calculate statements.</span></span>
    * <span data-ttu-id="371ab-108">Wählen Sie entweder einen bestimmten Shop oder einen Knoten aus, wenn Sie den Batchauftrag für eine Gruppe von Shops erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="371ab-108">Select either a specific store, or a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="371ab-109">Klicken Sie auf den Pfeil, um die Auswahl hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="371ab-109">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="371ab-110">Klicken Sie auf die Registerkarte "Im Hintergrund ausführen".</span><span class="sxs-lookup"><span data-stu-id="371ab-110">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="371ab-111">Wählen Sie unter Stapelverarbeitung "Ja" aus.</span><span class="sxs-lookup"><span data-stu-id="371ab-111">Under Batch processing, select 'Yes'.</span></span>
5. <span data-ttu-id="371ab-112">Klicken Sie auf "Wiederholung".</span><span class="sxs-lookup"><span data-stu-id="371ab-112">Click Recurrence.</span></span>
6. <span data-ttu-id="371ab-113">Geben Sie im Feld "Startdatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="371ab-113">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="371ab-114">Geben Sie im Startzeit-Feld eine Zeit ein.</span><span class="sxs-lookup"><span data-stu-id="371ab-114">In the Start time field, enter a time.</span></span>
8. <span data-ttu-id="371ab-115">Wählen Sie die Option "Kein Enddatum" aus.</span><span class="sxs-lookup"><span data-stu-id="371ab-115">Select the No end date option.</span></span>
9. <span data-ttu-id="371ab-116">Geben Sie im PatternUnit-Feld "Days" ein.</span><span class="sxs-lookup"><span data-stu-id="371ab-116">In the PatternUnit field, enter 'Days'.</span></span>
10. <span data-ttu-id="371ab-117">Geben Sie im Feld "Pro" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="371ab-117">In the Per field, enter a number.</span></span>
11. <span data-ttu-id="371ab-118">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="371ab-118">Click OK.</span></span>
12. <span data-ttu-id="371ab-119">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="371ab-119">Click OK.</span></span>


