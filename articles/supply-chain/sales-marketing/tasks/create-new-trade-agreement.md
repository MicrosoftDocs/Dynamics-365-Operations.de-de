---
title: Eine neue Handelsvereinbarung erstellen
description: Dieses Verfahren zeigt Ihnen an, wie eine Handelsvereinbarung erstellt, in der Sie einen Verkaufspreis der neuen Produktdimensionsgruppen erfassen, den Sie mit einem bestimmten Debitor aktualisiert haben.
author: omulvad
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TradeNonStockedConversion, TradeNonStockedConversionChangeWizard, TradeNonStockedConversionCheckWorksheet, TradeNonStockedConversionWizard, TradeNonStockedRegister
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ad1221bb57aea4c93cb60fc29caec2d3b41798f9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836397"
---
# <a name="create-a-new-trade-agreement"></a><span data-ttu-id="a465d-103">Eine neue Handelsvereinbarung erstellen</span><span class="sxs-lookup"><span data-stu-id="a465d-103">Create a new trade agreement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a465d-104">Dieses Verfahren zeigt Ihnen an, wie eine Handelsvereinbarung erstellt, in der Sie einen Verkaufspreis der neuen Produktdimensionsgruppen erfassen, den Sie mit einem bestimmten Debitor aktualisiert haben.</span><span class="sxs-lookup"><span data-stu-id="a465d-104">This procedure shows you how to create a trade agreement where you register a new product sales price that you've agreed with a specific customer.</span></span> <span data-ttu-id="a465d-105">Sie können diese Prozedur im Demodatenunternehmen USMF oder für Ihre eigenen Daten ausführen.</span><span class="sxs-lookup"><span data-stu-id="a465d-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="a465d-106">Wenn Sie eigene Daten verwenden, bevor Sie dieses Handbuch starten, müssen Sie prüfen, ob ein Handelsvereinbarungserfassungsname vorhanden ist, in die standardmäßige Beziehung festgelegt ist „Preis- (Verkauf )“.</span><span class="sxs-lookup"><span data-stu-id="a465d-106">If you're using your own data, before you start this guide you need to make sure that a Trade agreement journal name exists where the Default relation is set to "Price (sales)".</span></span>


## <a name="create-and-post-a-new-trade-agreement-journal"></a><span data-ttu-id="a465d-107">Erstellen und buchen einer neuen Handelsvereinbarungs-Erfassung.</span><span class="sxs-lookup"><span data-stu-id="a465d-107">Create and post a new trade agreement journal</span></span>
1. <span data-ttu-id="a465d-108">Wechseln Sie zu **Navigationsbereich > Module > Verrieb und Marketing > Preise und Rabatte > Handelsvereinbarungserfassungen**.</span><span class="sxs-lookup"><span data-stu-id="a465d-108">Go to **Navigation pane > Modules > Sales and marketing > Prices and discounts > Trade agreement journals**.</span></span>
2. <span data-ttu-id="a465d-109">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="a465d-109">Click **New**.</span></span>
3. <span data-ttu-id="a465d-110">Klicken Sie im Feld **Name** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="a465d-110">In the **Name** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="a465d-111">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="a465d-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="a465d-112">Klicken Sie im **Aktivitätsbereich** auf **Zeilen**.</span><span class="sxs-lookup"><span data-stu-id="a465d-112">On **Action Pane**, click **Lines**.</span></span>
6. <span data-ttu-id="a465d-113">Wählen Sie im Feld **Kontocode** die Option „Tabelle“ aus.</span><span class="sxs-lookup"><span data-stu-id="a465d-113">In the **Account code** field, select 'Table'.</span></span>
    
    <span data-ttu-id="a465d-114">In diesem Beispiel aktualisieren Sie den Preis für einen bestimmten Debitor, dem Durchschnitt Sie Tabelle auswählen muss.</span><span class="sxs-lookup"><span data-stu-id="a465d-114">In this example, you're updating the price for a specific customer, which means you need to choose Table.</span></span> <span data-ttu-id="a465d-115">Wenn Sie den Listenpreis des Produkts aktualisierten, wählen Sie „Alle“ aus, damit der neue Preis für alle Debitoren gültig ist.</span><span class="sxs-lookup"><span data-stu-id="a465d-115">If you were updating the product's list price, you would select 'All', so that the new price is valid for all customers.</span></span> <span data-ttu-id="a465d-116">Wenn Sie Preise unter verschiedenen Debitorensegmenten unterschieden, dann geben Sie Gruppe auswählen.</span><span class="sxs-lookup"><span data-stu-id="a465d-116">If you were differentiating prices among different customer segments, then you would select Group.</span></span> <span data-ttu-id="a465d-117">Um Gruppe festzulegen, muss Debitorenpreisgruppen eingerichtet haben.</span><span class="sxs-lookup"><span data-stu-id="a465d-117">To select Group, you must have set up Customer price groups.</span></span>  

7. <span data-ttu-id="a465d-118">Klicken Sie im Feld **Konto-Auswahl** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="a465d-118">In the **Account selection** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="a465d-119">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="a465d-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="a465d-120">Wählen Sie im Feld **Artikelcode** „Tabelle“ aus.</span><span class="sxs-lookup"><span data-stu-id="a465d-120">In the **Item code** field, select 'Table'.</span></span>
    
    <span data-ttu-id="a465d-121">Wenn Sie eine Handelsvereinbarung vom Typ „Preis (Verkauf)“ eingeben, müssen Sie nur „Tabelle“ im Feld **Artikelcode** auswählen.</span><span class="sxs-lookup"><span data-stu-id="a465d-121">When you are entering a trade agreement of type 'Price (sales)', you must only select 'Table' in the **Item code** field.</span></span> <span data-ttu-id="a465d-122">Dies ist, da ein Preis ein absoluter Wert ist und nicht gleiche für alle oder eine Gruppe Produkte werden kann.</span><span class="sxs-lookup"><span data-stu-id="a465d-122">This is because a price is an absolute value and cannot be same for all products or a group of products.</span></span>
    
10. <span data-ttu-id="a465d-123">Klicken Sie im Feld **Artikelrelation** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="a465d-123">In the **Item relation** field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="a465d-124">In der Liste wählen Sie das Produkt aus, das Sie in die Vereinbarung aufnehmen wollen.</span><span class="sxs-lookup"><span data-stu-id="a465d-124">In the list, select the product you want to include in the agreement.</span></span> <span data-ttu-id="a465d-125">Notieren Sie, an dem Produkt Sie ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="a465d-125">Make a note of which product you've selected.</span></span>  
12. <span data-ttu-id="a465d-126">Geben Sie in das **Von**-Feld eine Minimalmenge ein.</span><span class="sxs-lookup"><span data-stu-id="a465d-126">In the **From** field, enter a minimum quantity.</span></span>
    - <span data-ttu-id="a465d-127">Wenn der Debitor eine Mindestmenge bestellen muss, bevor er sich für den neuen Preis qualifiziert, dann können Sie diese Menge hier angeben.</span><span class="sxs-lookup"><span data-stu-id="a465d-127">If the customer has to order a minimum quantity before they can qualify for the new price, then you need to specify that quantity here.</span></span>  
    - <span data-ttu-id="a465d-128">Geben Sie einen Wert im **Bis**-Feld ein, um die maximale Menge anzugeben, bis zu der der Preis der Vereinbarung nicht gültig ist.</span><span class="sxs-lookup"><span data-stu-id="a465d-128">Enter a value in the **To** field to specify the maximum quantity above which the agreement's price will not be valid.</span></span> <span data-ttu-id="a465d-129">Wenn Sie Preise und Rabatte auf Grundlage mehrerer Mengennachlässe anbieten, dann geben Sie jeden Mengennachlass als Paar der minimalen und maximalen Menge in den **Von**- und **Bis**-Feldern an.</span><span class="sxs-lookup"><span data-stu-id="a465d-129">If you offer prices and discounts based on multiple quantity breaks, then specify each quantity bracket as a pair of minimum and maximum quantity in the **From** and **To** fields respectively.</span></span>
13. <span data-ttu-id="a465d-130">Geben Sie einen Preis in das Feld **Betrag in Währung** ein.</span><span class="sxs-lookup"><span data-stu-id="a465d-130">In the **Amount in currency field**, enter a price.</span></span>
14. <span data-ttu-id="a465d-131">Geben Sie im Abschnitt **Details** im Feld **Von Datum** ein Datum ein, ab dem diese Vereinbarung gilt.</span><span class="sxs-lookup"><span data-stu-id="a465d-131">Under the **Details** section, in the **From date** field, enter a date from which this agreement will be valid.</span></span>
15. <span data-ttu-id="a465d-132">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="a465d-132">Click **Save**.</span></span>
16. <span data-ttu-id="a465d-133">Klicken Sie auf **Überprüfen**.</span><span class="sxs-lookup"><span data-stu-id="a465d-133">Click **Validate**.</span></span>
17. <span data-ttu-id="a465d-134">Klicken Sie auf **Ausgewählte Positionen überprüfen.**</span><span class="sxs-lookup"><span data-stu-id="a465d-134">Click **Validate selected lines**.</span></span>
18. <span data-ttu-id="a465d-135">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="a465d-135">Click **OK**.</span></span>
19. <span data-ttu-id="a465d-136">Klicken Sie auf **Buchen**.</span><span class="sxs-lookup"><span data-stu-id="a465d-136">Click **Post**.</span></span>
20. <span data-ttu-id="a465d-137">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="a465d-137">Click **OK**.</span></span>

## <a name="view-trade-agreements-for-a-product"></a><span data-ttu-id="a465d-138">Handelsvereinbarungen für ein Produkt anzeigen</span><span class="sxs-lookup"><span data-stu-id="a465d-138">View trade agreements for a product</span></span>
1. <span data-ttu-id="a465d-139">Wechseln Sie zu **Navigationsbereich > Module > Produktinformationsverwaltung > Produkte > Freigegebene Produkte**.</span><span class="sxs-lookup"><span data-stu-id="a465d-139">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="a465d-140">Wählen Sie in der Liste suchen Sie und wählen Sie das Produkt aus, dessen Preis Sie derzeit aktualisiert haben.</span><span class="sxs-lookup"><span data-stu-id="a465d-140">In the list, find and select the product whose price you have just updated.</span></span>
3. <span data-ttu-id="a465d-141">Klicken Sie im **Aktivitätsbereich** auf **Verkaufen**.</span><span class="sxs-lookup"><span data-stu-id="a465d-141">On the **Action Pane**, click **Sell**.</span></span>
4. <span data-ttu-id="a465d-142">Klicken Sie auf **Handelsvereinbarungen** anzeigen.</span><span class="sxs-lookup"><span data-stu-id="a465d-142">Click **View trade agreements**.</span></span>
    
    <span data-ttu-id="a465d-143">Prüfen Sie die Details der Preishandelsvereinbarung, soeben erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="a465d-143">Review the details of the price trade agreement you have just created.</span></span>    

5. <span data-ttu-id="a465d-144">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="a465d-144">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a465d-145">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a465d-145">Additional resources</span></span>

### <a name="whitepaper"></a><span data-ttu-id="a465d-146">Whitepaper</span><span class="sxs-lookup"><span data-stu-id="a465d-146">Whitepaper</span></span>
<span data-ttu-id="a465d-147">Laden Sie für weitere Informationen das folgende Whitepaper herunter (geschrieben zur Unterstützung von AX2012, gilt jedoch weiterhin für Dynamics 365 Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="a465d-147">For more information, download the following white paper (written to support AX2012, but still applies for Dynamics 365 Supply Chain Management)</span></span>
- [<span data-ttu-id="a465d-148">Handelsvereinbarungen</span><span class="sxs-lookup"><span data-stu-id="a465d-148">Trade agreements</span></span>](https://mbs.microsoft.com/files/public/CS/AX2012R3/TradeagreementsinAX.pdf)

### <a name="community-blogs"></a><span data-ttu-id="a465d-149">Communityblogs</span><span class="sxs-lookup"><span data-stu-id="a465d-149">Community blogs</span></span>
- [<span data-ttu-id="a465d-150">Verkaufspreise in Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a465d-150">Sales prices in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/11/14/sales-prices-in-dynamics-365-for-finance-and-operations/#sales_price_in_trade_agreements)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]