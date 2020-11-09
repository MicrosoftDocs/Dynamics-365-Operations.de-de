---
title: Mit dem Dynamics 365 Supply Chain Management-Preisgestaltungsmodul on demand synchronisieren
description: In diesem Thema wird die Verwendung des Preisgestaltungsmoduls in Microsoft Dynamics 365 Supply Chain Management über Dynamics 365 Sales beschrieben.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 740ae20704abd9c59f64c2c7622fa96d65dccb1d
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997145"
---
# <a name="sync-with-the-dynamics-365-supply-chain-management-pricing-engine-on-demand"></a><span data-ttu-id="39003-103">Mit dem Dynamics 365 Supply Chain Management-Preisgestaltungsmodul on demand synchronisieren</span><span class="sxs-lookup"><span data-stu-id="39003-103">Sync with the Dynamics 365 Supply Chain Management pricing engine on demand</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="39003-104">Microsoft Dynamics 365 Supply Chain Management enthält ein Preisgestaltungsmodul, das Handelsabkommen, Preislisten, Kundenbindungsprogramme, Werbeaktionen und Rabatte verwaltet.</span><span class="sxs-lookup"><span data-stu-id="39003-104">Microsoft Dynamics 365 Supply Chain Management includes a pricing engine that handles trade agreements, price lists, customer loyalty programs, promotions, and discounts.</span></span> <span data-ttu-id="39003-105">Das Preisgestaltungsmodul verwendet komplexe Regeln, um den besten Preis für ein bestimmtes Angebot oder eine bestimmte Bestellung zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="39003-105">The pricing engine uses complex rules to determine the best price for a given quotation or order.</span></span> <span data-ttu-id="39003-106">Wenn Sie duales Schreiben verwenden, verwenden Sie entweder die statische Preisgestaltung oder das Preisgestaltungsmodul von Dynamics 365 Supply Chain Management auf den Seiten „Angebot“ und „Bestellung“ in Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="39003-106">When you use dual-write, you use either static pricing or the pricing engine from Dynamics 365 Supply Chain Management on the Quote and Order pages in Dynamics 365 Sales.</span></span>

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a><span data-ttu-id="39003-107">Das Preisgestaltungsmodul von Supply Chain Management in Sales verwenden</span><span class="sxs-lookup"><span data-stu-id="39003-107">Use the pricing engine from Supply Chain Management in Sales</span></span>

1. <span data-ttu-id="39003-108">Gehen Sie in Sales zu **Verkäufe \> Aufträge**.</span><span class="sxs-lookup"><span data-stu-id="39003-108">In Sales, go to **Sales \> Orders**.</span></span>
2. <span data-ttu-id="39003-109">Wählen Sie **Neu** aus, um einen neuen Auftrag zu erstellen, oder wählen Sie einen vorhandenen Auftrag in der Liste **Eigene Aufträge** aus.</span><span class="sxs-lookup"><span data-stu-id="39003-109">Select **New** to create a new order, or select an existing order in the **My Orders** list.</span></span>
3. <span data-ttu-id="39003-110">Fügen Sie eine neue Auftragsposition hinzu.</span><span class="sxs-lookup"><span data-stu-id="39003-110">Add a new order line.</span></span>
4. <span data-ttu-id="39003-111">Wenn Sie eine neue Bestellung erstellen, wählen Sie Aktionsbereich **Preis für Auftrag** aus.</span><span class="sxs-lookup"><span data-stu-id="39003-111">If you're creating a new order, select **Price Order** on the Action Pane.</span></span> <span data-ttu-id="39003-112">Wenn Sie einen bestehenden Auftrag aktualisieren, wählen Sie Aktionsbereich **Neu berechnen** aus.</span><span class="sxs-lookup"><span data-stu-id="39003-112">If you're updating an existing order, select **Recalculate** on the Action Pane.</span></span>

    <span data-ttu-id="39003-113">Die folgenden Felder werden automatisch ausgefüllt:</span><span class="sxs-lookup"><span data-stu-id="39003-113">The following fields are automatically filled in:</span></span>

    + <span data-ttu-id="39003-114">Detailbetrag</span><span class="sxs-lookup"><span data-stu-id="39003-114">Detail Amount</span></span>
    + <span data-ttu-id="39003-115">Rabatt %</span><span class="sxs-lookup"><span data-stu-id="39003-115">Discount %</span></span>
    + <span data-ttu-id="39003-116">Skonto</span><span class="sxs-lookup"><span data-stu-id="39003-116">Discount</span></span>
    + <span data-ttu-id="39003-117">Vorfrachtbetrag</span><span class="sxs-lookup"><span data-stu-id="39003-117">Pre-Freight Amount</span></span>
    + <span data-ttu-id="39003-118">Frachtbetrag</span><span class="sxs-lookup"><span data-stu-id="39003-118">Freight Amount</span></span>
    + <span data-ttu-id="39003-119">Gesamte Steuern</span><span class="sxs-lookup"><span data-stu-id="39003-119">Total Tax</span></span>
    + <span data-ttu-id="39003-120">Gesamtbetrag</span><span class="sxs-lookup"><span data-stu-id="39003-120">Total Amount</span></span>
    
5. <span data-ttu-id="39003-121">Stellen Sie sicher, dass das System Handelsvereinbarungen und Kaufverträge zur Berechnung des Preises berücksichtigt:</span><span class="sxs-lookup"><span data-stu-id="39003-121">To ensure that the system considers trade and sales agreements to calculate the price:</span></span>
    1. <span data-ttu-id="39003-122">Navigieren Sie zu Ihrer Supply Chain Management-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="39003-122">Navigate to your Supply Chain Management environment.</span></span>
    2. <span data-ttu-id="39003-123">Navigieren Sie zu **Debitoren \> Einrichtung \> Debitorenparameter**.</span><span class="sxs-lookup"><span data-stu-id="39003-123">Navigate to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
    3. <span data-ttu-id="39003-124">Wählen Sie in der seitlichen Navigationsleiste die Registerkarte **Preise** aus.</span><span class="sxs-lookup"><span data-stu-id="39003-124">Select the **Prices** tab in the side navigation bar.</span></span>
    4. <span data-ttu-id="39003-125">Deaktivieren Sie im Inforegister **Handelsvereinbarungsauswertung** die Option **Manuelle Eingabe**.</span><span class="sxs-lookup"><span data-stu-id="39003-125">Under the **Trade agreement evaluation** fastab, uncheck the **Manual entry** option.</span></span>

## <a name="how-it-works"></a><span data-ttu-id="39003-126">Funktionsweise</span><span class="sxs-lookup"><span data-stu-id="39003-126">How it works</span></span>

<span data-ttu-id="39003-127">Wenn Sie in Sales **Preis für Auftrag** auswählen, wird die Funktion **Summen** in der Registerkarte **Auftrag \> Anzeigen** in Supply Chain Management für den zugehörigen Kundenauftrag aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="39003-127">When you select **Price Order** in Sales, the **Totals** function on the **Sales Order \> View** tab in Supply Chain Management is called for the associated sales order.</span></span> <span data-ttu-id="39003-128">Die Werte in der Auftragssumme in Sales werden verwendet, um die entsprechenden Felder im Supply Chain Management auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="39003-128">The values in the order total in Sales are used to fill in the corresponding fields in Supply Chain Management.</span></span>

<span data-ttu-id="39003-129">Wenn die Kundenauftragssumme im Supply Chain Management berechnet wird, wertet die Berechnung die vorhandenen Handelsvereinbarungen und Verkaufsvereinbarungen für den Kunden und die im Kundenauftrag aufgeführten Produkte aus.</span><span class="sxs-lookup"><span data-stu-id="39003-129">When the sales order total is calculated in Supply Chain Management, the calculation evaluates the existing trade agreements and sales agreements for the customer and the products that are listed in the sales order.</span></span> <span data-ttu-id="39003-130">Diese Daten werden zum Berechnen der Summen verwendet.</span><span class="sxs-lookup"><span data-stu-id="39003-130">This information is used to calculate the totals.</span></span> <span data-ttu-id="39003-131">Wenn die Option **Preis für Auftrag** ausgewählt ist, spiegelt Sales automatisch alle Einstellungen wider, die im Supply Chain Management vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="39003-131">When **Price Order** is selected, Sales automatically reflects all the setup that has been done in Supply Chain Management.</span></span>

## <a name="limitations"></a><span data-ttu-id="39003-132">Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="39003-132">Limitations</span></span>

<span data-ttu-id="39003-133">Wenn die Felder in Sales ausgefüllt sind, gelten folgende Einschränkungen:</span><span class="sxs-lookup"><span data-stu-id="39003-133">When the fields in Sales are filled in, the following limitations apply:</span></span>

+ <span data-ttu-id="39003-134">Das Einrichten von Gebühren und Gebührenzuordnungen im Supply Chain Management wird in Sales nicht repliziert.</span><span class="sxs-lookup"><span data-stu-id="39003-134">The setup of charges and charge allocations in Supply Chain Management isn't replicated in Sales.</span></span>
+ <span data-ttu-id="39003-135">Bei der Preisgestaltung werden keine speziellen Einzelhandelspreise berücksichtigt, die im Feld **Retail Channel** auf der Seite „Auftragsposition“ in Supply Chain Management angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="39003-135">Pricing doesn't consider special retail pricing that is specified in the **Retail Channel** field on the sales order line page in Supply Chain Management.</span></span>
+ <span data-ttu-id="39003-136">Rabatte, die im Abschnitt **Handelsvergütungsverwaltung** des Supply Chain Management definiert sind, werden nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="39003-136">Discounts that are defined in the **Trade Allowance Management** section of Supply Chain Management aren't considered.</span></span>
