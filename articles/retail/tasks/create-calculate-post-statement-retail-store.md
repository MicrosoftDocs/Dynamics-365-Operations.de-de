--- 
title: "Auszüge für ein Einzelhandelsgeschäft erstellen, berechnen und buchen"
description: "Diese Prozedur führt Sie Schritt für Schritt durch manuelle Verfahren zum Erstellen, Berechnen und Buchen eines Auszugs für einen Shop."
author: jashanno
manager: AnnBe
ms.date: 11/15/2016
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
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 1c31c849c4c72762f0fdeb3f1d256cd3529394b2
ms.contentlocale: de-de
ms.lasthandoff: 08/08/2018

---
# <a name="create-calculate-and-post-statements-for-a-retail-store"></a><span data-ttu-id="07f39-103">Auszüge für ein Einzelhandelsgeschäft erstellen, berechnen und buchen</span><span class="sxs-lookup"><span data-stu-id="07f39-103">Create, calculate, and post statements for a retail store</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="07f39-104">Diese Prozedur führt Sie Schritt für Schritt durch manuelle Verfahren zum Erstellen, Berechnen und Buchen eines Auszugs für einen Shop.</span><span class="sxs-lookup"><span data-stu-id="07f39-104">This procedure walks through the manual steps for creating, calculating, and posting a statement for a store.</span></span> <span data-ttu-id="07f39-105">Es gibt auch Batchaufträge, die für die gleichen Aufgaben konfiguriert werden können.</span><span class="sxs-lookup"><span data-stu-id="07f39-105">There are also batch jobs that can be configured for the same tasks.</span></span> <span data-ttu-id="07f39-106">Die Schritte zum Konfigurieren und Ausführen der Batchaufträge werden in anderen Themen behandelt.</span><span class="sxs-lookup"><span data-stu-id="07f39-106">The steps for configuring and running the batch jobs can be found in other topics.</span></span> <span data-ttu-id="07f39-107">Um dieses Verfahren abzuschließen, müssen Buchungen enthalten sein, die in POS abgeschlossen und dann in Dynamics AX gezogen wurden.</span><span class="sxs-lookup"><span data-stu-id="07f39-107">To complete this procedure, you must have transactions that were completed in POS and then pulled into Dynamics AX.</span></span> <span data-ttu-id="07f39-108">Für diese Aufzeichnung wird das Demo-Datenunternehmen USRT verwendet.</span><span class="sxs-lookup"><span data-stu-id="07f39-108">This recording uses the USRT company in demo data.</span></span> <span data-ttu-id="07f39-109">Diese Verfahren bezieht sich möglicherweise auf Microsoft Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="07f39-109">This procedure may refer to Microsoft Dynamics AX.</span></span> <span data-ttu-id="07f39-110">Beachten Sie, dass Microsoft Dynamics AX nun als Microsoft Dynamics 365 for Operations. bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="07f39-110">Please note that Dynamics AX is now called Microsoft Dynamics 365 for Operations.</span></span>

1. <span data-ttu-id="07f39-111">Gehen Sie zu Alle Arbeitsbereiche >..</span><span class="sxs-lookup"><span data-stu-id="07f39-111">Go to All workspaces > ..</span></span> <span data-ttu-id="07f39-112">> Finanzdaten für den Einzelhandelsshop.</span><span class="sxs-lookup"><span data-stu-id="07f39-112">> Retail store financials.</span></span>
2. <span data-ttu-id="07f39-113">Klicken Sie auf "Neuer Auszug".</span><span class="sxs-lookup"><span data-stu-id="07f39-113">Click New statement.</span></span>
3. <span data-ttu-id="07f39-114">Klicken Sie im Feld "Shopnummer" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="07f39-114">In the Store number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="07f39-115">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="07f39-115">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="07f39-116">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="07f39-116">Click OK.</span></span>
    * <span data-ttu-id="07f39-117">Die Einstellungsgruppe hat die Einstellungen, mit denen gesteuert wird, welche Buchungen im Auszug enthalten sind und wie sie in Auszugspositionen gruppiert werden.</span><span class="sxs-lookup"><span data-stu-id="07f39-117">The Setup group has the settings that control what transactions are included in the statement and how they are grouped into statement lines.</span></span> <span data-ttu-id="07f39-118">Sie können die Einstellungsgruppe öffnen und diese Einstellungen ändern, oder Sie können die Standards verwenden.</span><span class="sxs-lookup"><span data-stu-id="07f39-118">You can open the Setup group and change these settings, or you can use the defaults.</span></span>  
    * <span data-ttu-id="07f39-119">Das Auszugsmethodenfeld definiert, wie die Auszugspositionen gruppiert werden.</span><span class="sxs-lookup"><span data-stu-id="07f39-119">The Statement method field defines how the statement lines will be grouped.</span></span>  
    * <span data-ttu-id="07f39-120">Wählen Sie einen Mitarbeiter oder ein Register aus, wenn Sie einen Auszug nur für den bestimmten Mitarbeiter oder das bestimmte Register berechnen möchten.</span><span class="sxs-lookup"><span data-stu-id="07f39-120">Select a staff member or a register if you want to calculate a statement only for the specific staff member or register.</span></span>  
6. <span data-ttu-id="07f39-121">Wählen Sie im Feld "Abschlussmethode" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="07f39-121">In the Closing method field, select an option.</span></span>
7. <span data-ttu-id="07f39-122">Klicken Sie auf "Auszug berechnen".</span><span class="sxs-lookup"><span data-stu-id="07f39-122">Click Calculate statement.</span></span>
8. <span data-ttu-id="07f39-123">Klicken Sie auf "Ja".</span><span class="sxs-lookup"><span data-stu-id="07f39-123">Click Yes.</span></span>
    * <span data-ttu-id="07f39-124">Nachdem der Auszug berechnet wurde, sollte es Positionen geben, die mit Gesamtbeträgen für jede verwendete Zahlungsmethode und Auszugsmethode erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="07f39-124">After calculating the statement, there should be lines created with total amounts for each payment method and statement method that was used.</span></span>  
    * <span data-ttu-id="07f39-125">Geben Sie einen gezählten Betrag in jeder Position ein, wenn er eingegeben oder aktualisiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="07f39-125">Enter a counted amount in each line if it needs to be entered or updated.</span></span> <span data-ttu-id="07f39-126">Das gezählte Feld wird mit Beträgen von den Kassenstürzen aufgefüllt, die in POS geleistet werden.</span><span class="sxs-lookup"><span data-stu-id="07f39-126">The counted field is populated with amounts from tender declarations done in POS.</span></span>  
9. <span data-ttu-id="07f39-127">Klicken Sie auf "Auszug buchen".</span><span class="sxs-lookup"><span data-stu-id="07f39-127">Click Post statement.</span></span>
10. <span data-ttu-id="07f39-128">Klicken Sie auf "Schließen".</span><span class="sxs-lookup"><span data-stu-id="07f39-128">Click Close.</span></span>
11. <span data-ttu-id="07f39-129">Navigieren Sie zu Einzelhandel und Handel > Kanäle > Finanzdaten für den Einzelhandelsshop.</span><span class="sxs-lookup"><span data-stu-id="07f39-129">Go to Retail and commerce > Channels > Retail store financials.</span></span>
12. <span data-ttu-id="07f39-130">Klicken Sie auf die Registerkarte "Gebuchte Auszüge".</span><span class="sxs-lookup"><span data-stu-id="07f39-130">Click the Posted statements tab.</span></span>


