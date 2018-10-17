--- 
title: "Buchen von Online-Verkäufen und -Zahlungen"
description: "Diese Prozedur führt Sie Schritt für Schritt durch das Konfigurieren und die Ausführung eines wiederkehrenden Batchauftrags zum Erstellen von Aufträgen und Zahlungen für Onlineshopbuchungen."
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 13839bbe6ca03f3cfc7036fce87477bf7d5af2a7
ms.contentlocale: de-de
ms.lasthandoff: 09/14/2018

---
# <a name="posting-of-online-sales-and-payments"></a><span data-ttu-id="4da48-103">Buchen von Online-Verkäufen und -Zahlungen</span><span class="sxs-lookup"><span data-stu-id="4da48-103">Posting of online sales and payments</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="4da48-104">Diese Prozedur führt Sie Schritt für Schritt durch das Konfigurieren und die Ausführung eines wiederkehrenden Batchauftrags zum Erstellen von Aufträgen und Zahlungen für Onlineshopbuchungen.</span><span class="sxs-lookup"><span data-stu-id="4da48-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="4da48-105">Für diese Prozedur wird das Demo-Datenunternehmen USRT verwendet.</span><span class="sxs-lookup"><span data-stu-id="4da48-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="4da48-106">Wechseln Sie zu Alle Arbeitsbereiche > Finanzdaten für den Einzelhandelsshop.</span><span class="sxs-lookup"><span data-stu-id="4da48-106">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="4da48-107">Klicken Sie auf "Aufträge synchronisieren".</span><span class="sxs-lookup"><span data-stu-id="4da48-107">Click Synchronize orders.</span></span>
3. <span data-ttu-id="4da48-108">Wählen Sie im Organisationshierarchie-Feld "Einzelhandelsgeschäfte nach Region" aus.</span><span class="sxs-lookup"><span data-stu-id="4da48-108">In the Organization hierarchy field, select 'Retail Stores by Region'.</span></span>
    * <span data-ttu-id="4da48-109">Wählen Sie entweder einen bestimmten Online-Shop oder einen Knoten aus, wenn Sie den Batchauftrag für eine Gruppe von Shops erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="4da48-109">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="4da48-110">Klicken Sie auf den Pfeil, um die Auswahl hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="4da48-110">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="4da48-111">Klicken Sie auf die Registerkarte "Im Hintergrund ausführen".</span><span class="sxs-lookup"><span data-stu-id="4da48-111">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="4da48-112">Aktivieren oder deaktivieren Sie das Kontrollkästchen ''Stapelverarbeitung".</span><span class="sxs-lookup"><span data-stu-id="4da48-112">Check or uncheck the Batch processing checkbox.</span></span>
6. <span data-ttu-id="4da48-113">Klicken Sie auf "Wiederholung".</span><span class="sxs-lookup"><span data-stu-id="4da48-113">Click Recurrence.</span></span>
7. <span data-ttu-id="4da48-114">Wählen Sie die Option "Kein Enddatum" aus.</span><span class="sxs-lookup"><span data-stu-id="4da48-114">Select the No end date option.</span></span>
8. <span data-ttu-id="4da48-115">Geben Sie im Feld ''Anzahl" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="4da48-115">In the Count field, enter a number.</span></span>
9. <span data-ttu-id="4da48-116">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="4da48-116">Click OK.</span></span>
10. <span data-ttu-id="4da48-117">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="4da48-117">Click OK.</span></span>


