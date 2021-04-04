---
title: On-Demand-Synchronisierung mit dem Preisgestaltungsmodul von Supply Chain Management
description: In diesem Thema wird die Verwendung des Preisgestaltungsmoduls in Microsoft Dynamics 365 Supply Chain Management über Dynamics 365 Sales beschrieben.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: e2067e83d3f0c98e986873b8eaf1b817de912c0f
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570139"
---
# <a name="sync-on-demand-with-the-supply-chain-management-pricing-engine"></a><span data-ttu-id="22364-103">On-Demand-Synchronisierung mit dem Preisgestaltungsmodul von Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="22364-103">Sync on-demand with the Supply Chain Management pricing engine</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="22364-104">Microsoft Dynamics 365 Supply Chain Management enthält ein Preisgestaltungsmodul, das Handelsabkommen, Preislisten, Kundenbindungsprogramme, Werbeaktionen und Rabatte verwaltet.</span><span class="sxs-lookup"><span data-stu-id="22364-104">Microsoft Dynamics 365 Supply Chain Management includes a pricing engine that handles trade agreements, price lists, customer loyalty programs, promotions, and discounts.</span></span> <span data-ttu-id="22364-105">Das Preisgestaltungsmodul verwendet komplexe Regeln, um den besten Preis für ein bestimmtes Angebot oder eine bestimmte Bestellung zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="22364-105">The pricing engine uses complex rules to determine the best price for a given quotation or order.</span></span> <span data-ttu-id="22364-106">Wenn Sie duales Schreiben verwenden, verwenden Sie entweder die statische Preisgestaltung oder das Preisgestaltungsmodul von Dynamics 365 Supply Chain Management auf den Seiten „Angebot“ und „Bestellung“ in Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="22364-106">When you use dual-write, you use either static pricing or the pricing engine from Dynamics 365 Supply Chain Management on the Quote and Order pages in Dynamics 365 Sales.</span></span>

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a><span data-ttu-id="22364-107">Das Preisgestaltungsmodul von Supply Chain Management in Sales verwenden</span><span class="sxs-lookup"><span data-stu-id="22364-107">Use the pricing engine from Supply Chain Management in Sales</span></span>

1. <span data-ttu-id="22364-108">Gehen Sie in Sales zu **Verkäufe \> Aufträge**.</span><span class="sxs-lookup"><span data-stu-id="22364-108">In Sales, go to **Sales \> Orders**.</span></span>
2. <span data-ttu-id="22364-109">Wählen Sie **Neu** aus, um einen neuen Auftrag zu erstellen, oder wählen Sie einen vorhandenen Auftrag in der Liste **Eigene Aufträge** aus.</span><span class="sxs-lookup"><span data-stu-id="22364-109">Select **New** to create a new order, or select an existing order in the **My Orders** list.</span></span>
3. <span data-ttu-id="22364-110">Fügen Sie eine neue Auftragsposition hinzu.</span><span class="sxs-lookup"><span data-stu-id="22364-110">Add a new order line.</span></span>
4. <span data-ttu-id="22364-111">Wenn Sie eine neue Bestellung erstellen, wählen Sie Aktionsbereich **Preis für Auftrag** aus.</span><span class="sxs-lookup"><span data-stu-id="22364-111">If you're creating a new order, select **Price Order** on the Action Pane.</span></span> <span data-ttu-id="22364-112">Wenn Sie einen bestehenden Auftrag aktualisieren, wählen Sie Aktionsbereich **Neu berechnen** aus.</span><span class="sxs-lookup"><span data-stu-id="22364-112">If you're updating an existing order, select **Recalculate** on the Action Pane.</span></span>

    <span data-ttu-id="22364-113">Die folgenden Spalten werden automatisch ausgefüllt:</span><span class="sxs-lookup"><span data-stu-id="22364-113">The following columns are automatically filled in:</span></span>

    + <span data-ttu-id="22364-114">Detailbetrag</span><span class="sxs-lookup"><span data-stu-id="22364-114">Detail Amount</span></span>
    + <span data-ttu-id="22364-115">Rabatt %</span><span class="sxs-lookup"><span data-stu-id="22364-115">Discount %</span></span>
    + <span data-ttu-id="22364-116">Skonto</span><span class="sxs-lookup"><span data-stu-id="22364-116">Discount</span></span>
    + <span data-ttu-id="22364-117">Vorfrachtbetrag</span><span class="sxs-lookup"><span data-stu-id="22364-117">Pre-Freight Amount</span></span>
    + <span data-ttu-id="22364-118">Frachtbetrag</span><span class="sxs-lookup"><span data-stu-id="22364-118">Freight Amount</span></span>
    + <span data-ttu-id="22364-119">Gesamte Steuern</span><span class="sxs-lookup"><span data-stu-id="22364-119">Total Tax</span></span>
    + <span data-ttu-id="22364-120">Gesamtbetrag</span><span class="sxs-lookup"><span data-stu-id="22364-120">Total Amount</span></span>
    
5. <span data-ttu-id="22364-121">Stellen Sie sicher, dass das System Handelsvereinbarungen und Kaufverträge zur Berechnung des Preises berücksichtigt:</span><span class="sxs-lookup"><span data-stu-id="22364-121">To ensure that the system considers trade and sales agreements to calculate the price:</span></span>
    1. <span data-ttu-id="22364-122">Navigieren Sie zu Ihrer Supply Chain Management-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="22364-122">Navigate to your Supply Chain Management environment.</span></span>
    2. <span data-ttu-id="22364-123">Navigieren Sie zu **Debitoren \> Einrichtung \> Debitorenparameter**.</span><span class="sxs-lookup"><span data-stu-id="22364-123">Navigate to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
    3. <span data-ttu-id="22364-124">Wählen Sie in der seitlichen Navigationsleiste die Registerkarte **Preise** aus.</span><span class="sxs-lookup"><span data-stu-id="22364-124">Select the **Prices** tab in the side navigation bar.</span></span>
    4. <span data-ttu-id="22364-125">Deaktivieren Sie im Inforegister **Handelsvereinbarungsauswertung** die Option **Manuelle Eingabe**.</span><span class="sxs-lookup"><span data-stu-id="22364-125">Under the **Trade agreement evaluation** fastab, uncheck the **Manual entry** option.</span></span>

## <a name="how-it-works"></a><span data-ttu-id="22364-126">Funktionsweise</span><span class="sxs-lookup"><span data-stu-id="22364-126">How it works</span></span>

<span data-ttu-id="22364-127">Wenn Sie in Sales **Preis für Auftrag** auswählen, wird die Funktion **Summen** in der Registerkarte **Auftrag \> Anzeigen** in Supply Chain Management für den zugehörigen Kundenauftrag aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="22364-127">When you select **Price Order** in Sales, the **Totals** function on the **Sales Order \> View** tab in Supply Chain Management is called for the associated sales order.</span></span> <span data-ttu-id="22364-128">Die Werte in der Auftragssumme in Sales werden verwendet, um die entsprechenden Spalten in Supply Chain Management auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="22364-128">The values in the order total in Sales are used to fill in the corresponding columns in Supply Chain Management.</span></span>

<span data-ttu-id="22364-129">Wenn die Kundenauftragssumme im Supply Chain Management berechnet wird, wertet die Berechnung die vorhandenen Handelsvereinbarungen und Verkaufsvereinbarungen für den Kunden und die im Kundenauftrag aufgeführten Produkte aus.</span><span class="sxs-lookup"><span data-stu-id="22364-129">When the sales order total is calculated in Supply Chain Management, the calculation evaluates the existing trade agreements and sales agreements for the customer and the products that are listed in the sales order.</span></span> <span data-ttu-id="22364-130">Diese Daten werden zum Berechnen der Summen verwendet.</span><span class="sxs-lookup"><span data-stu-id="22364-130">This information is used to calculate the totals.</span></span> <span data-ttu-id="22364-131">Wenn die Option **Preis für Auftrag** ausgewählt ist, spiegelt Sales automatisch alle Einstellungen wider, die im Supply Chain Management vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="22364-131">When **Price Order** is selected, Sales automatically reflects all the setup that has been done in Supply Chain Management.</span></span>

## <a name="limitations"></a><span data-ttu-id="22364-132">Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="22364-132">Limitations</span></span>

<span data-ttu-id="22364-133">Wenn die Spalten in Sales ausgefüllt sind, gelten folgende Einschränkungen:</span><span class="sxs-lookup"><span data-stu-id="22364-133">When the columns in Sales are filled in, the following limitations apply:</span></span>

+ <span data-ttu-id="22364-134">Das Einrichten von Gebühren und Gebührenzuordnungen im Supply Chain Management wird in Sales nicht repliziert.</span><span class="sxs-lookup"><span data-stu-id="22364-134">The setup of charges and charge allocations in Supply Chain Management isn't replicated in Sales.</span></span>
+ <span data-ttu-id="22364-135">Bei der Preisgestaltung werden keine speziellen Einzelhandelspreise berücksichtigt, die in der Spalte **Retail Channel** auf der Seite „Auftragsposition“ in Supply Chain Management angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="22364-135">Pricing doesn't consider special retail pricing that is specified in the **Retail Channel** column on the sales order line page in Supply Chain Management.</span></span>
+ <span data-ttu-id="22364-136">Rabatte, die im Abschnitt **Handelsvergütungsverwaltung** des Supply Chain Management definiert sind, werden nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="22364-136">Discounts that are defined in the **Trade Allowance Management** section of Supply Chain Management aren't considered.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]