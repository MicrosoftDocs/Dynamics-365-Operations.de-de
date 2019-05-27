---
title: Eine neue Handelsvereinbarung erstellen
description: Dieses Verfahren zeigt Ihnen an, wie eine Handelsvereinbarung erstellt, in der Sie einen Verkaufspreis der neuen Produktdimensionsgruppen erfassen, den Sie mit einem bestimmten Debitor aktualisiert haben.
author: omulvad
manager: AnnBe
ms.date: 11/16/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e132cd20437b7929e81fcaa123d70bb57fb320c8
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549266"
---
# <a name="create-a-new-trade-agreement"></a><span data-ttu-id="6a6c8-103">Eine neue Handelsvereinbarung erstellen</span><span class="sxs-lookup"><span data-stu-id="6a6c8-103">Create a new trade agreement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6a6c8-104">Dieses Verfahren zeigt Ihnen an, wie eine Handelsvereinbarung erstellt, in der Sie einen Verkaufspreis der neuen Produktdimensionsgruppen erfassen, den Sie mit einem bestimmten Debitor aktualisiert haben.</span><span class="sxs-lookup"><span data-stu-id="6a6c8-104">This procedure shows you how to create a trade agreement where you register a new product sales price that you've agreed with a specific customer.</span></span> <span data-ttu-id="6a6c8-105">Sie können diese Prozedur im Demodatenunternehmen USMF oder für Ihre eigenen Daten ausführen.</span><span class="sxs-lookup"><span data-stu-id="6a6c8-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="6a6c8-106">Wenn Sie eigene Daten verwenden, bevor Sie dieses Handbuch starten, müssen Sie prüfen, ob ein Handelsvereinbarungserfassungsname vorhanden ist, in die standardmäßige Beziehung festgelegt ist " Preis- (Verkauf )".</span><span class="sxs-lookup"><span data-stu-id="6a6c8-106">If you’re using your own data, before you start this guide you need to make sure that a Trade agreement journal name exists where the Default relation is set to “Price (sales)”.</span></span>


## <a name="create-and-post-a-new-trade-agreement-journal"></a><span data-ttu-id="6a6c8-107">Erstellen und buchen einer neuen Handelsvereinbarungs-Erfassung.</span><span class="sxs-lookup"><span data-stu-id="6a6c8-107">Create and post a new trade agreement journal</span></span>
1. <span data-ttu-id="6a6c8-108">Wechseln Sie zu Vertrieb und Marketing > Preise und Rabatte > Handelsvereinbarungserfassungen.</span><span class="sxs-lookup"><span data-stu-id="6a6c8-108">Go to Sales and marketing > Prices and discounts > Trade agreement journals.</span></span>
2. <span data-ttu-id="6a6c8-109">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="6a6c8-109">Click New.</span></span>
3. <span data-ttu-id="6a6c8-110">Klicken Sie im Feld "Name" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="6a6c8-110">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="6a6c8-111">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="6a6c8-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="6a6c8-112">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="6a6c8-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="6a6c8-113">Klicken Sie auf "Positionen".</span><span class="sxs-lookup"><span data-stu-id="6a6c8-113">Click Lines.</span></span>
7. <span data-ttu-id="6a6c8-114">Wählen Sie im Feld Kontocode die Option Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="6a6c8-114">In the Account code field, select 'Table'.</span></span>
    * <span data-ttu-id="6a6c8-115">In diesem Beispiel aktualisieren Sie den Preis für einen bestimmten Debitor, dem Durchschnitt Sie Tabelle auswählen muss.</span><span class="sxs-lookup"><span data-stu-id="6a6c8-115">In this example, you're updating the price for a specific customer, which means you need to choose Table.</span></span> <span data-ttu-id="6a6c8-116">Wenn Sie den Listenpreis des Produkts aktualisierten, geben Sie alle aktivieren, damit der neue Preis für alle Debitoren gültig ist.</span><span class="sxs-lookup"><span data-stu-id="6a6c8-116">If you were updating the product's list price, you would select All, so that the new price is valid for all customers.</span></span> <span data-ttu-id="6a6c8-117">Wenn Sie Preise unter verschiedenen Debitorensegmenten unterschieden, dann geben Sie Gruppe auswählen.</span><span class="sxs-lookup"><span data-stu-id="6a6c8-117">If you were differentiating prices among different customer segments, then you would select Group.</span></span> <span data-ttu-id="6a6c8-118">Um Gruppe festzulegen, muss Debitorenpreisgruppen eingerichtet haben.</span><span class="sxs-lookup"><span data-stu-id="6a6c8-118">To select Group, you must have set up Customer price groups.</span></span>  
8. <span data-ttu-id="6a6c8-119">Klicken Sie im Feld Konto-Auswahl auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="6a6c8-119">In the Account selection field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="6a6c8-120">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="6a6c8-120">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="6a6c8-121">Wählen Sie im Feld Artikelcode "Tabelle" aus.</span><span class="sxs-lookup"><span data-stu-id="6a6c8-121">In the Item code field, select 'Table'.</span></span>
    * <span data-ttu-id="6a6c8-122">Wenn Sie eine Handelsvereinbarung vom Typ "Preis (Verkauf)" eingegeben werden, müssen Sie "Tabelle" im Feld Artikelcode nur auswählen.</span><span class="sxs-lookup"><span data-stu-id="6a6c8-122">When you are entering a trade agreement of type 'Price (sales)', you must only select 'Table' in the Item code field.</span></span> <span data-ttu-id="6a6c8-123">Dies ist, da ein Preis ein absoluter Wert ist und nicht gleiche für alle oder eine Gruppe Produkte werden kann.</span><span class="sxs-lookup"><span data-stu-id="6a6c8-123">This is because a price is an absolute value and cannot be same for all products or a group of products.</span></span>  
11. <span data-ttu-id="6a6c8-124">Klicken Sie im Feld Artikelrelation auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="6a6c8-124">In the Item relation field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="6a6c8-125">In der Liste wählen Sie das Produkt aus, das Sie in die Vereinbarung aufnehmen wollen.</span><span class="sxs-lookup"><span data-stu-id="6a6c8-125">In the list, select the product you want to include in the agreement.</span></span>
    * <span data-ttu-id="6a6c8-126">Notieren Sie, an dem Produkt Sie ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="6a6c8-126">Make a note of which product you've selected.</span></span>  
13. <span data-ttu-id="6a6c8-127">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="6a6c8-127">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="6a6c8-128">Geben Sie in das Von-Feld eine Minimalmenge ein.</span><span class="sxs-lookup"><span data-stu-id="6a6c8-128">In the From field, enter a minimum quantity.</span></span>
    * <span data-ttu-id="6a6c8-129">Wenn der Debitor eine Menge bestellen muss, bevor sie für den neuen Preis qualifiziert sind, dann können Sie Anforderung, diese Menge hier anzugeben.</span><span class="sxs-lookup"><span data-stu-id="6a6c8-129">If the customer has to order a minimum quantity  before they can qualify for the new price, then you need to specify that quantity here.</span></span>  
    * <span data-ttu-id="6a6c8-130">Geben Sie einen Wert im Feld, um die maximale Menge anzugeben, zu der der Preis der Vereinbarung nicht gültig ist.</span><span class="sxs-lookup"><span data-stu-id="6a6c8-130">Enter a value in the To field to specify the maximum quantity above which the agreement's price will not be valid.</span></span> <span data-ttu-id="6a6c8-131">Wenn Sie Angebotspreise und Rabatte auf Grundlage mehrere Mengenpausen, dann jede Mengenklammer als Paar der minimalen und maximalen Menge in " " und"" zu aus den Feldern bzw. angeben.</span><span class="sxs-lookup"><span data-stu-id="6a6c8-131">If you offer prices and discounts based on multiple quantity breaks, then specify each quantity bracket as a pair of minimum and maximum quantity in the 'From' and 'To' fields respectively.</span></span>  
15. <span data-ttu-id="6a6c8-132">Geben Sie einen Preis in das Feld "Betrag in Währung" ein.</span><span class="sxs-lookup"><span data-stu-id="6a6c8-132">In the Amount in currency field, enter a price.</span></span>
16. <span data-ttu-id="6a6c8-133">In das Feld Von Datum, geben Sie ein Datum ein, ab dem diese Vereinbarung gilt.</span><span class="sxs-lookup"><span data-stu-id="6a6c8-133">In the From date field, enter a date from which this agreement will be valid.</span></span>
17. <span data-ttu-id="6a6c8-134">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="6a6c8-134">Click Save.</span></span>
18. <span data-ttu-id="6a6c8-135">Klicken Sie auf "Überprüfen".</span><span class="sxs-lookup"><span data-stu-id="6a6c8-135">Click Validate.</span></span>
19. <span data-ttu-id="6a6c8-136">Klicken Sie auf Ausgewählte Positionen überprüfen.</span><span class="sxs-lookup"><span data-stu-id="6a6c8-136">Click Validate selected lines.</span></span>
20. <span data-ttu-id="6a6c8-137">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="6a6c8-137">Click OK.</span></span>
21. <span data-ttu-id="6a6c8-138">Klicken Sie auf "Buchen".</span><span class="sxs-lookup"><span data-stu-id="6a6c8-138">Click Post.</span></span>
22. <span data-ttu-id="6a6c8-139">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="6a6c8-139">Click OK.</span></span>

## <a name="view-trade-agreements-for-a-product"></a><span data-ttu-id="6a6c8-140">Handelsvereinbarungen für ein Produkt anzeigen</span><span class="sxs-lookup"><span data-stu-id="6a6c8-140">View trade agreements for a product</span></span>
1. <span data-ttu-id="6a6c8-141">Wechseln Sie zu "Produktinformationsverwaltung" > "Produkte" > "Freigegebene Produkte".</span><span class="sxs-lookup"><span data-stu-id="6a6c8-141">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="6a6c8-142">Wählen Sie in der Liste suchen Sie und wählen Sie das Produkt aus, dessen Preis Sie derzeit aktualisiert haben.</span><span class="sxs-lookup"><span data-stu-id="6a6c8-142">In the list, find and select the product whose price you have just updated.</span></span>
3. <span data-ttu-id="6a6c8-143">Klicken Sie im Aktivitätsbereich auf "Verkaufen".</span><span class="sxs-lookup"><span data-stu-id="6a6c8-143">On the Action Pane, click Sell.</span></span>
4. <span data-ttu-id="6a6c8-144">Klicken Sie auf Handelsvereinbarungen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="6a6c8-144">Click View trade agreements.</span></span>
    * <span data-ttu-id="6a6c8-145">Prüfen Sie die Details der Preishandelsvereinbarung, soeben erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="6a6c8-145">Review the details of the price trade agreement you have just created.</span></span>    
5. <span data-ttu-id="6a6c8-146">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="6a6c8-146">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6a6c8-147">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6a6c8-147">Additional resources</span></span>
### <a name="community-blogs"></a><span data-ttu-id="6a6c8-148">Communityblogs</span><span class="sxs-lookup"><span data-stu-id="6a6c8-148">Community blogs</span></span>
- [<span data-ttu-id="6a6c8-149">Verkaufspreise in Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6a6c8-149">Sales prices in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/11/14/sales-prices-in-dynamics-365-for-finance-and-operations/#sales_price_in_trade_agreements)
