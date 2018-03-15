--- 
title: " Online-Verkäufe und -Zahlungen buchen"
description: "Diese Prozedur führt Sie Schritt für Schritt durch das Konfigurieren und die Ausführung eines wiederkehrenden Batchauftrags zum Erstellen von Aufträgen und Zahlungen für Onlineshopbuchungen."
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 2feaf580c7ae1fc53f9257f117576c99764c6ea0
ms.contentlocale: de-de
ms.lasthandoff: 02/07/2018

---
# <a name="post-online-sales-and-payments"></a><span data-ttu-id="ddfe4-103"> Online-Verkäufe und -Zahlungen buchen</span><span class="sxs-lookup"><span data-stu-id="ddfe4-103">Post online sales and payments</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="ddfe4-104">Diese Prozedur führt Sie Schritt für Schritt durch das Konfigurieren und die Ausführung eines wiederkehrenden Batchauftrags zum Erstellen von Aufträgen und Zahlungen für Onlineshopbuchungen.</span><span class="sxs-lookup"><span data-stu-id="ddfe4-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="ddfe4-105">Für diese Prozedur wird das Demo-Datenunternehmen USRT verwendet.</span><span class="sxs-lookup"><span data-stu-id="ddfe4-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="ddfe4-106">Wechseln Sie zu Alle Arbeitsbereiche > Finanzdaten für den Einzelhandelsshop.</span><span class="sxs-lookup"><span data-stu-id="ddfe4-106">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="ddfe4-107">Klicken Sie auf "Aufträge synchronisieren".</span><span class="sxs-lookup"><span data-stu-id="ddfe4-107">Click Synchronize orders.</span></span>
3. <span data-ttu-id="ddfe4-108">Wählen Sie im Organisationshierarchie-Feld "Einzelhandelsgeschäfte nach Region" aus.</span><span class="sxs-lookup"><span data-stu-id="ddfe4-108">In the Organization hierarchy field, select 'Retail Stores by Region'.</span></span>
    * <span data-ttu-id="ddfe4-109">Wählen Sie entweder einen bestimmten Online-Shop oder einen Knoten aus, wenn Sie den Batchauftrag für eine Gruppe von Shops erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="ddfe4-109">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="ddfe4-110">Klicken Sie auf den Pfeil, um die Auswahl hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="ddfe4-110">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="ddfe4-111">Klicken Sie auf die Registerkarte "Im Hintergrund ausführen".</span><span class="sxs-lookup"><span data-stu-id="ddfe4-111">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="ddfe4-112">Aktivieren oder deaktivieren Sie das Kontrollkästchen ''Stapelverarbeitung".</span><span class="sxs-lookup"><span data-stu-id="ddfe4-112">Check or uncheck the Batch processing checkbox.</span></span>
6. <span data-ttu-id="ddfe4-113">Klicken Sie auf "Wiederholung".</span><span class="sxs-lookup"><span data-stu-id="ddfe4-113">Click Recurrence.</span></span>
7. <span data-ttu-id="ddfe4-114">Wählen Sie die Option "Kein Enddatum" aus.</span><span class="sxs-lookup"><span data-stu-id="ddfe4-114">Select the No end date option.</span></span>
8. <span data-ttu-id="ddfe4-115">Geben Sie im Feld ''Anzahl" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="ddfe4-115">In the Count field, enter a number.</span></span>
9. <span data-ttu-id="ddfe4-116">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="ddfe4-116">Click OK.</span></span>
10. <span data-ttu-id="ddfe4-117">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="ddfe4-117">Click OK.</span></span>


