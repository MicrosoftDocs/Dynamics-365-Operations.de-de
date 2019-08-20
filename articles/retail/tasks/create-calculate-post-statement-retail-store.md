---
title: Auszüge für ein Einzelhandelsgeschäft erstellen, berechnen und buchen
description: Dieses Thema führt Sie Schritt für Schritt durch manuelle Verfahren zum Erstellen, Berechnen und Buchen eines Auszugs für einen Shop.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailStatementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 693d1821779d5f7af95b900daa3bb7a2c38a6354
ms.sourcegitcommit: cb63259ad8fa5649ff12bc4a7f195bd1e40bd968
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/16/2019
ms.locfileid: "1755522"
---
# <a name="create-calculate-and-post-statements-for-a-retail-store"></a><span data-ttu-id="a6f1d-103">Auszüge für ein Einzelhandelsgeschäft erstellen, berechnen und buchen</span><span class="sxs-lookup"><span data-stu-id="a6f1d-103">Create, calculate, and post statements for a retail store</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="a6f1d-104">Dieses Thema führt Sie Schritt für Schritt durch manuelle Verfahren zum Erstellen, Berechnen und Buchen eines Auszugs für einen Shop.</span><span class="sxs-lookup"><span data-stu-id="a6f1d-104">This topic describes the manual steps for creating, calculating, and posting a statement for a store.</span></span> <span data-ttu-id="a6f1d-105">Es gibt auch Batchaufträge, die für die gleichen Aufgaben konfiguriert werden können.</span><span class="sxs-lookup"><span data-stu-id="a6f1d-105">There are also batch jobs that can be configured for the same tasks.</span></span> <span data-ttu-id="a6f1d-106">Die Schritte zum Konfigurieren und Ausführen der Batchaufträge werden in anderen Themen behandelt.</span><span class="sxs-lookup"><span data-stu-id="a6f1d-106">The steps for configuring and running the batch jobs can be found in other topics.</span></span> <span data-ttu-id="a6f1d-107">Um diese Prozedur abzuschließen, müssen Buchungen in POS abgeschlossen und dann in Dynamics 365 for Finance and Operations einbezogen worden sein.</span><span class="sxs-lookup"><span data-stu-id="a6f1d-107">To complete this procedure, you must have transactions that were completed in POS and then pulled into Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="a6f1d-108">Für diese Aufzeichnung wird das Demo-Datenunternehmen USRT verwendet.</span><span class="sxs-lookup"><span data-stu-id="a6f1d-108">This recording uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="a6f1d-109">Wählen Sie **Finanzdaten für den Einzelhandelsshop** auf der Startseite aus.</span><span class="sxs-lookup"><span data-stu-id="a6f1d-109">Select **Retail store financials** from the home page.</span></span>
2. <span data-ttu-id="a6f1d-110">Wählen Sie **Neuer Auszug** aus.</span><span class="sxs-lookup"><span data-stu-id="a6f1d-110">Select **New statement**.</span></span>
3. <span data-ttu-id="a6f1d-111">Wählen Sie im Feld **Shopnummer** eine Option in der Dropdownliste aus.</span><span class="sxs-lookup"><span data-stu-id="a6f1d-111">In the **Store number** field, select a option from the drop-down.</span></span>
4. <span data-ttu-id="a6f1d-112">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="a6f1d-112">Select **OK**.</span></span>
5. <span data-ttu-id="a6f1d-113">Die **Einstellungs** gruppe hat die Einstellungen, mit denen gesteuert wird, welche Buchungen im Auszug enthalten sind und wie sie in Auszugspositionen gruppiert werden.</span><span class="sxs-lookup"><span data-stu-id="a6f1d-113">The **Setup** group has the settings that control what transactions are included in the statement and how they are grouped into statement lines.</span></span> <span data-ttu-id="a6f1d-114">Sie können die **Einstellungs** gruppe öffnen und diese Einstellungen ändern, oder Sie können die Standardwerte verwenden.</span><span class="sxs-lookup"><span data-stu-id="a6f1d-114">You can open the **Setup** group and change these settings, or you can use the defaults.</span></span>  
    - <span data-ttu-id="a6f1d-115">Das Feld **Auszugsmethode** definiert, wie die Auszugspositionen gruppiert werden.</span><span class="sxs-lookup"><span data-stu-id="a6f1d-115">The **Statement method** field defines how the statement lines will be grouped.</span></span>  
    - <span data-ttu-id="a6f1d-116">Wählen Sie im Feld **Personal/Register** einen Mitarbeiter oder ein Register aus, wenn Sie einen Auszug nur für den bestimmten Mitarbeiter oder das bestimmte Register berechnen möchten.</span><span class="sxs-lookup"><span data-stu-id="a6f1d-116">Select a staff member or a register in the **staff/register** field if you want to calculate a statement only for the specific staff member or register.</span></span>  
6. <span data-ttu-id="a6f1d-117">Wählen Sie im Feld **Abschlussmethode** eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="a6f1d-117">In the **Closing method** field, select an option.</span></span>
7. <span data-ttu-id="a6f1d-118">Wählen Sie im Aktivitätsbereich **Auszug berechnen** aus.</span><span class="sxs-lookup"><span data-stu-id="a6f1d-118">Select **Calculate statement** from the Action Pane.</span></span>
8. <span data-ttu-id="a6f1d-119">Wählen Sie **Ja** aus.</span><span class="sxs-lookup"><span data-stu-id="a6f1d-119">Select **Yes**.</span></span>
    - <span data-ttu-id="a6f1d-120">Nachdem der Auszug berechnet wurde, sollte es Positionen geben, die mit Gesamtbeträgen für jede verwendete Zahlungsmethode und Auszugsmethode erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="a6f1d-120">After calculating the statement, there should be lines created with total amounts for each payment method and statement method that was used.</span></span>  
    - <span data-ttu-id="a6f1d-121">Geben Sie einen gezählten Betrag in jeder Position ein, wenn er eingegeben oder aktualisiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="a6f1d-121">Enter a counted amount in each line if it needs to be entered or updated.</span></span> <span data-ttu-id="a6f1d-122">Das gezählte Feld wird mit Beträgen von den Kassenstürzen aufgefüllt, die in POS geleistet werden.</span><span class="sxs-lookup"><span data-stu-id="a6f1d-122">The counted field is populated with amounts from tender declarations done in POS.</span></span>  
9. <span data-ttu-id="a6f1d-123">Wählen Sie im Aktivitätsbereich **Auszug buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="a6f1d-123">Select **Post statement** from the Action Pane.</span></span>
10. <span data-ttu-id="a6f1d-124">Wählen Sie **Schließen** aus.</span><span class="sxs-lookup"><span data-stu-id="a6f1d-124">Select **Close**.</span></span>
11. <span data-ttu-id="a6f1d-125">Schließen Sie den Bereich.</span><span class="sxs-lookup"><span data-stu-id="a6f1d-125">Close the pane.</span></span>
12. <span data-ttu-id="a6f1d-126">Wählen Sie **Finanzdaten für den Einzelhandelsshop** auf der Startseite aus.</span><span class="sxs-lookup"><span data-stu-id="a6f1d-126">At the home page, select **Retail store financials**.</span></span>
13. <span data-ttu-id="a6f1d-127">Wählen Sie die Registerkarte **Gebuchte Auszüge** aus.</span><span class="sxs-lookup"><span data-stu-id="a6f1d-127">Select the **Posted statements** tab.</span></span>

