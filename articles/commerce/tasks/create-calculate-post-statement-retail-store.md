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
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 455dee5a14ca0c44ba823a467baa78352b367ec8
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5221304"
---
# <a name="create-calculate-and-post-statements-for-a-retail-store"></a><span data-ttu-id="bf6b6-103">Auszüge für ein Einzelhandelsgeschäft erstellen, berechnen und buchen</span><span class="sxs-lookup"><span data-stu-id="bf6b6-103">Create, calculate, and post statements for a retail store</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bf6b6-104">Dieses Thema führt Sie Schritt für Schritt durch manuelle Verfahren zum Erstellen, Berechnen und Buchen eines Auszugs für einen Shop.</span><span class="sxs-lookup"><span data-stu-id="bf6b6-104">This topic describes the manual steps for creating, calculating, and posting a statement for a store.</span></span> <span data-ttu-id="bf6b6-105">Es gibt auch Batchaufträge, die für die gleichen Aufgaben konfiguriert werden können.</span><span class="sxs-lookup"><span data-stu-id="bf6b6-105">There are also batch jobs that can be configured for the same tasks.</span></span> <span data-ttu-id="bf6b6-106">Die Schritte zum Konfigurieren und Ausführen der Batchaufträge werden in anderen Themen behandelt.</span><span class="sxs-lookup"><span data-stu-id="bf6b6-106">The steps for configuring and running the batch jobs can be found in other topics.</span></span> <span data-ttu-id="bf6b6-107">Um diese Prozedur abzuschließen, müssen Buchungen in POS abgeschlossen und dann in Dynamics 365 Commerce einbezogen worden sein.</span><span class="sxs-lookup"><span data-stu-id="bf6b6-107">To complete this procedure, you must have transactions that were completed in POS and then pulled into Dynamics 365 Commerce.</span></span> <span data-ttu-id="bf6b6-108">Für diese Aufzeichnung wird das Demo-Datenunternehmen USRT verwendet.</span><span class="sxs-lookup"><span data-stu-id="bf6b6-108">This recording uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="bf6b6-109">Wählen Sie **Shopfinanzdaten** auf der Startseite aus.</span><span class="sxs-lookup"><span data-stu-id="bf6b6-109">Select **Store financials** from the home page.</span></span>
2. <span data-ttu-id="bf6b6-110">Wählen Sie **Neuer Auszug** aus.</span><span class="sxs-lookup"><span data-stu-id="bf6b6-110">Select **New statement**.</span></span>
3. <span data-ttu-id="bf6b6-111">Wählen Sie im Feld **Shopnummer** eine Option in der Dropdownliste aus.</span><span class="sxs-lookup"><span data-stu-id="bf6b6-111">In the **Store number** field, select a option from the drop-down.</span></span>
4. <span data-ttu-id="bf6b6-112">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="bf6b6-112">Select **OK**.</span></span>
5. <span data-ttu-id="bf6b6-113">Die **Einstellungs** gruppe hat die Einstellungen, mit denen gesteuert wird, welche Buchungen im Auszug enthalten sind und wie sie in Auszugspositionen gruppiert werden.</span><span class="sxs-lookup"><span data-stu-id="bf6b6-113">The **Setup** group has the settings that control what transactions are included in the statement and how they are grouped into statement lines.</span></span> <span data-ttu-id="bf6b6-114">Sie können die **Einstellungs** gruppe öffnen und diese Einstellungen ändern, oder Sie können die Standardwerte verwenden.</span><span class="sxs-lookup"><span data-stu-id="bf6b6-114">You can open the **Setup** group and change these settings, or you can use the defaults.</span></span>  
    - <span data-ttu-id="bf6b6-115">Das Feld **Auszugsmethode** definiert, wie die Auszugspositionen gruppiert werden.</span><span class="sxs-lookup"><span data-stu-id="bf6b6-115">The **Statement method** field defines how the statement lines will be grouped.</span></span>  
    - <span data-ttu-id="bf6b6-116">Wählen Sie im Feld **Personal/Register** einen Mitarbeiter oder ein Register aus, wenn Sie einen Auszug nur für den bestimmten Mitarbeiter oder das bestimmte Register berechnen möchten.</span><span class="sxs-lookup"><span data-stu-id="bf6b6-116">Select a staff member or a register in the **staff/register** field if you want to calculate a statement only for the specific staff member or register.</span></span>  
6. <span data-ttu-id="bf6b6-117">Wählen Sie im Feld **Abschlussmethode** eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="bf6b6-117">In the **Closing method** field, select an option.</span></span>
7. <span data-ttu-id="bf6b6-118">Wählen Sie im Aktivitätsbereich **Auszug berechnen** aus.</span><span class="sxs-lookup"><span data-stu-id="bf6b6-118">Select **Calculate statement** from the Action Pane.</span></span>
8. <span data-ttu-id="bf6b6-119">Wählen Sie **Ja** aus.</span><span class="sxs-lookup"><span data-stu-id="bf6b6-119">Select **Yes**.</span></span>
    - <span data-ttu-id="bf6b6-120">Nachdem der Auszug berechnet wurde, sollte es Positionen geben, die mit Gesamtbeträgen für jede verwendete Zahlungsmethode und Auszugsmethode erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="bf6b6-120">After calculating the statement, there should be lines created with total amounts for each payment method and statement method that was used.</span></span>  
    - <span data-ttu-id="bf6b6-121">Geben Sie einen gezählten Betrag in jeder Position ein, wenn er eingegeben oder aktualisiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="bf6b6-121">Enter a counted amount in each line if it needs to be entered or updated.</span></span> <span data-ttu-id="bf6b6-122">Das gezählte Feld wird mit Beträgen von den Kassenstürzen aufgefüllt, die in POS geleistet werden.</span><span class="sxs-lookup"><span data-stu-id="bf6b6-122">The counted field is populated with amounts from tender declarations done in POS.</span></span>  
9. <span data-ttu-id="bf6b6-123">Wählen Sie im Aktivitätsbereich **Auszug buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="bf6b6-123">Select **Post statement** from the Action Pane.</span></span>
10. <span data-ttu-id="bf6b6-124">Wählen Sie **Schließen** aus.</span><span class="sxs-lookup"><span data-stu-id="bf6b6-124">Select **Close**.</span></span>
11. <span data-ttu-id="bf6b6-125">Schließen Sie den Bereich.</span><span class="sxs-lookup"><span data-stu-id="bf6b6-125">Close the pane.</span></span>
12. <span data-ttu-id="bf6b6-126">Wählen Sie auf der Startseite **Shopfinanzdaten**.</span><span class="sxs-lookup"><span data-stu-id="bf6b6-126">At the home page, select **Store financials**.</span></span>
13. <span data-ttu-id="bf6b6-127">Wählen Sie die Registerkarte **Gebuchte Auszüge** aus.</span><span class="sxs-lookup"><span data-stu-id="bf6b6-127">Select the **Posted statements** tab.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]