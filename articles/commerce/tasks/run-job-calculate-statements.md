---
title: Konfigurieren und aktivieren Sie einen Einzelvorgang, um Auszüge zu berechnen
description: Diese Prozedur führt Sie Schritt für Schritt durch das Konfigurieren und Ausführen von wiederkehrenden Batchaufträgen zum Erstellen und Berechnen von Auszügen für einen ausgewählten Shop oder eine Gruppe von Shops.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 973236acca0cb8c0d57171e4bb9d4daaa7faaf38
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4412598"
---
# <a name="configure-and-run-job-to-calculate-statements"></a><span data-ttu-id="cb638-103">Konfigurieren und aktivieren Sie einen Einzelvorgang, um Auszüge zu berechnen</span><span class="sxs-lookup"><span data-stu-id="cb638-103">Configure and run job to calculate statements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cb638-104">Diese Prozedur führt Sie Schritt für Schritt durch das Konfigurieren und Ausführen von wiederkehrenden Batchaufträgen zum Erstellen und Berechnen von Auszügen für einen ausgewählten Shop oder eine Gruppe von Shops.</span><span class="sxs-lookup"><span data-stu-id="cb638-104">This procedure walks through configuring and running recurrent batch jobs to create and calculate statements for a selected store or group of stores.</span></span> <span data-ttu-id="cb638-105">Für diese Prozedur wird das Demo-Datenunternehmen USRT verwendet.</span><span class="sxs-lookup"><span data-stu-id="cb638-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="cb638-106">Gehen Sie zu Alle Arbeitsbereiche > Finanzdaten für Shop.</span><span class="sxs-lookup"><span data-stu-id="cb638-106">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="cb638-107">Klicken Sie auf "Auszüge berechnen".</span><span class="sxs-lookup"><span data-stu-id="cb638-107">Click Calculate statements.</span></span>
    * <span data-ttu-id="cb638-108">Wählen Sie entweder einen bestimmten Shop oder einen Knoten aus, wenn Sie den Batchauftrag für eine Gruppe von Shops erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="cb638-108">Select either a specific store, or a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="cb638-109">Klicken Sie auf den Pfeil, um die Auswahl hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="cb638-109">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="cb638-110">Klicken Sie auf die Registerkarte "Im Hintergrund ausführen".</span><span class="sxs-lookup"><span data-stu-id="cb638-110">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="cb638-111">Wählen Sie unter Stapelverarbeitung "Ja" aus.</span><span class="sxs-lookup"><span data-stu-id="cb638-111">Under Batch processing, select 'Yes'.</span></span>
5. <span data-ttu-id="cb638-112">Klicken Sie auf "Wiederholung".</span><span class="sxs-lookup"><span data-stu-id="cb638-112">Click Recurrence.</span></span>
6. <span data-ttu-id="cb638-113">Geben Sie im Feld "Startdatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="cb638-113">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="cb638-114">Geben Sie im Startzeit-Feld eine Zeit ein.</span><span class="sxs-lookup"><span data-stu-id="cb638-114">In the Start time field, enter a time.</span></span>
8. <span data-ttu-id="cb638-115">Wählen Sie die Option "Kein Enddatum" aus.</span><span class="sxs-lookup"><span data-stu-id="cb638-115">Select the No end date option.</span></span>
9. <span data-ttu-id="cb638-116">Geben Sie im PatternUnit-Feld "Days" ein.</span><span class="sxs-lookup"><span data-stu-id="cb638-116">In the PatternUnit field, enter 'Days'.</span></span>
10. <span data-ttu-id="cb638-117">Geben Sie im Feld "Pro" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="cb638-117">In the Per field, enter a number.</span></span>
11. <span data-ttu-id="cb638-118">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="cb638-118">Click OK.</span></span>
12. <span data-ttu-id="cb638-119">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="cb638-119">Click OK.</span></span>

