--- 
title: "Aufträge bestätigen"
description: "Diese Verfahren zeigt, wie Aufträge bestätigt werden."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 7cab69222c5004e6a62c632a9e85085403434ffd
ms.contentlocale: de-de
ms.lasthandoff: 08/29/2017

---
# <a name="confirm-sales-orders"></a><span data-ttu-id="0ba7d-103">Aufträge bestätigen</span><span class="sxs-lookup"><span data-stu-id="0ba7d-103">Confirm sales orders</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0ba7d-104">Diese Verfahren zeigt, wie Aufträge bestätigt werden.</span><span class="sxs-lookup"><span data-stu-id="0ba7d-104">This procedure demonstrates how to confirm sales orders.</span></span> <span data-ttu-id="0ba7d-105">Sie werden angezeigt, wie einen einzelnen Auftrag bestätigt und wie man bestätigt mehrerer Aufträge gleichzeitig.</span><span class="sxs-lookup"><span data-stu-id="0ba7d-105">You’ll be shown how to confirm a single order, and how to confirm multiple orders at once.</span></span> <span data-ttu-id="0ba7d-106">Diese Aufgaben werden normalerweise von einem Auftragsbearbeiter ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0ba7d-106">These tasks would typically be carried out by a sales order processor.</span></span> <span data-ttu-id="0ba7d-107">Sie können diese Prozedur im Demodatenunternehmen USMF oder für Ihre eigenen Daten verwenden.</span><span class="sxs-lookup"><span data-stu-id="0ba7d-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="0ba7d-108">Bevor Sie beginnen, stellen Sie sicher, dass es mehrere offene Aufträge für denselben Debitor vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="0ba7d-108">Before you start, make sure there are several open sales orders for the same customer.</span></span> <span data-ttu-id="0ba7d-109">Wenn Sie USMF verwenden, können Sie Debitor US-027 verwenden.</span><span class="sxs-lookup"><span data-stu-id="0ba7d-109">If you’re using USMF, you can use customer US-027.</span></span>


## <a name="confirm-a-single-sales-order"></a><span data-ttu-id="0ba7d-110">Einzelnen Auftrag bestätigen</span><span class="sxs-lookup"><span data-stu-id="0ba7d-110">Confirm a single sales order</span></span>
1. <span data-ttu-id="0ba7d-111">Wechseln Sie zu "Vertrieb und Marketing" > "Aufträge" > "Alle Aufträge".</span><span class="sxs-lookup"><span data-stu-id="0ba7d-111">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="0ba7d-112">Suchen Sie in der Liste den Auftrag und wählen Sie diese aus, den Sie bestätigen wollen.</span><span class="sxs-lookup"><span data-stu-id="0ba7d-112">In the list, find and select the order that you want to confirm.</span></span>
3. <span data-ttu-id="0ba7d-113">Klicken Sie auf den Link auf der Auftragsnummer, um den ausgewählten Auftrag zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="0ba7d-113">Click the link on the sales order number to open the selected order.</span></span>
4. <span data-ttu-id="0ba7d-114">Klicken Sie im Aktivitätsbereich auf "Verkaufen".</span><span class="sxs-lookup"><span data-stu-id="0ba7d-114">On the Action Pane, click Sell.</span></span>
5. <span data-ttu-id="0ba7d-115">Klicken Sie auf "Auftrag bestätigen".</span><span class="sxs-lookup"><span data-stu-id="0ba7d-115">Click Confirm sales order.</span></span>
6. <span data-ttu-id="0ba7d-116">Erweitern oder reduzieren Sie den Abschnitt "Parameter".</span><span class="sxs-lookup"><span data-stu-id="0ba7d-116">Expand or collapse the Parameters section.</span></span>
    * <span data-ttu-id="0ba7d-117">Stellen Sie sicher, dass das Feld Buchen Ja aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="0ba7d-117">Make sure that the Posting Yes field is active.</span></span>  
7. <span data-ttu-id="0ba7d-118">Legen Sie die Option "Bestätigung drucken" auf "Ja" fest.</span><span class="sxs-lookup"><span data-stu-id="0ba7d-118">Set the Print confirmation option to Yes.</span></span>
    * <span data-ttu-id="0ba7d-119">Das Scheckkreditlimitfeld gibt die Methode, die verwendet wird, um den verbleibenden Kredit eines Debitors zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="0ba7d-119">The Check credit limit field specifies the method that’s used to calculate a customer's remaining credit.</span></span> <span data-ttu-id="0ba7d-120">Standardmäßig wird der Code wird aus der Seite Debitorenparameter kopiert.</span><span class="sxs-lookup"><span data-stu-id="0ba7d-120">By default, it’s copied from the Accounts receivable parameters page.</span></span> <span data-ttu-id="0ba7d-121">Wenn Sie die Kreditlimitprüfung übersprungen werden sollen, wenn Sie einen bestimmten Auftrag bestätigen, festsetzten das Kreditlimit auf Kein.</span><span class="sxs-lookup"><span data-stu-id="0ba7d-121">If you want to skip the credit limit check when confirming a specific sales order, set the Check credit limit to None.</span></span> <span data-ttu-id="0ba7d-122">Sie sollten jedoch daran denken, dass auch mit, wenn dieses Feld auf Kein festgelegt ist, die Kreditlimitprüfung weiterhin ausgeführt wird, wenn die erforderliche Kreditlimitoption auf den Debitorenmasterdaten aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="0ba7d-122">However, you should be aware that even with if this field is set to None, the credit limit check will still be performed if the Mandatory credit limit option is selected on the customer master data.</span></span>  
8. <span data-ttu-id="0ba7d-123">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="0ba7d-123">Click OK.</span></span>
9. <span data-ttu-id="0ba7d-124">Klicken Sie auf "Ja".</span><span class="sxs-lookup"><span data-stu-id="0ba7d-124">Click Yes.</span></span>
10. <span data-ttu-id="0ba7d-125">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="0ba7d-125">Close the page.</span></span>
11. <span data-ttu-id="0ba7d-126">Klicken Sie im Aktivitätsbereich auf "Optionen".</span><span class="sxs-lookup"><span data-stu-id="0ba7d-126">On the Action Pane, click Options.</span></span>
12. <span data-ttu-id="0ba7d-127">Klicken Sie auf "Ansicht ändern".</span><span class="sxs-lookup"><span data-stu-id="0ba7d-127">Click Change view.</span></span>
13. <span data-ttu-id="0ba7d-128">Klicken Sie auf die Kopfzeilenansicht.</span><span class="sxs-lookup"><span data-stu-id="0ba7d-128">Click Header view.</span></span>
    * <span data-ttu-id="0ba7d-129">Wenn ein Auftrag bestätigt wird, wird der Dokumentstatus zur Bestätigung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0ba7d-129">When an order is confirmed, the Document status is set to Confirmation.</span></span>  
14. <span data-ttu-id="0ba7d-130">Klicken Sie im Aktivitätsbereich auf "Verkaufen".</span><span class="sxs-lookup"><span data-stu-id="0ba7d-130">On the Action Pane, click Sell.</span></span>
15. <span data-ttu-id="0ba7d-131">Klicken Sie auf Auftragsbestätigung anzeigen.</span><span class="sxs-lookup"><span data-stu-id="0ba7d-131">Click Sales order confirmation.</span></span>
16. <span data-ttu-id="0ba7d-132">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="0ba7d-132">Close the page.</span></span>

## <a name="confirm-multiple-sales-orders-at-once"></a><span data-ttu-id="0ba7d-133">Bestätigen Sie mehrere Aufträge gleichzeitig</span><span class="sxs-lookup"><span data-stu-id="0ba7d-133">Confirm multiple sales orders at once</span></span>
1. <span data-ttu-id="0ba7d-134">Wechseln Sie zu Vertrieb und Marketing > Aufträge > Buchungsbeschreibung > Bestätigen Sie Auftrag.</span><span class="sxs-lookup"><span data-stu-id="0ba7d-134">Go to Sales and marketing > Sales orders > Order confirmation > Confirm sales order.</span></span>
2. <span data-ttu-id="0ba7d-135">Klicken Sie auf Auswählen.</span><span class="sxs-lookup"><span data-stu-id="0ba7d-135">Click Select.</span></span>
3. <span data-ttu-id="0ba7d-136">In der Liste auf der Registerkarte "Bereich", finden und wählen Sie den Datensatz aus, der das Feld "Debitorenkonto" verweist.</span><span class="sxs-lookup"><span data-stu-id="0ba7d-136">In the list on the Range tab, find and select the record that references the Customer account field.</span></span>
4. <span data-ttu-id="0ba7d-137">Klicken Sie im Feld "Kriterien" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="0ba7d-137">In the Criteria field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="0ba7d-138">Suchen und wählen Sie das Debitorenkonto aus, für das mehrere Aufträge hat, die per Massenerstellung soll bestätigen.</span><span class="sxs-lookup"><span data-stu-id="0ba7d-138">In the list, find and select the customer account that has multiple orders which you want to mass confirm.</span></span>
    * <span data-ttu-id="0ba7d-139">Wenn Sie USMF verwenden, können Sie Konto US-027 auswählen.</span><span class="sxs-lookup"><span data-stu-id="0ba7d-139">If you’re using USMF, you can select account US-027.</span></span>  
6. <span data-ttu-id="0ba7d-140">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="0ba7d-140">Click OK.</span></span>
    * <span data-ttu-id="0ba7d-141">Die Registerkarte Überblick zeigt eine Liste der Aufträge an, die die Abfragekriterien übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0ba7d-141">The Overview tab displays a list of the orders that match the query criteria.</span></span> <span data-ttu-id="0ba7d-142">Dabei werden in der Bestätigung eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="0ba7d-142">These will be included in the confirmation.</span></span>  
    * <span data-ttu-id="0ba7d-143">Die Feld Sammelaktualisierung für gibt den Parameter an, um den mehrere Aufträge in einem Bestätigungsdokument zusammengefasst werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0ba7d-143">The Summary update for field specifies the parameter by which multiple orders are to be summarized into one confirmation document.</span></span> <span data-ttu-id="0ba7d-144">Standardmäßig wird der Option in den Standardwerten für Sammelaktualisierungseinstellung auf der Debitorenparameterseite kopiert.</span><span class="sxs-lookup"><span data-stu-id="0ba7d-144">By default, the option is copied from the Default values for summary update setting on the Accounts receivable parameters page.</span></span>  
7. <span data-ttu-id="0ba7d-145">Wählen Sie im Feld "Sammelaktualisierung für" die Option "Auftrag" aus.</span><span class="sxs-lookup"><span data-stu-id="0ba7d-145">In the Summary update for field, select 'Order'.</span></span>
    * <span data-ttu-id="0ba7d-146">Die mindestens erforderlichen Parameter zum Erstellen von Zusammenfassungsupdates sind Rechnungsbetrag und Währung.</span><span class="sxs-lookup"><span data-stu-id="0ba7d-146">The minimum parameters that are required to create summary updates are Invoice account and Currency.</span></span> <span data-ttu-id="0ba7d-147">Das bedeutet, dass Sammelaktualisierungen, die verschiedene Rechnungskontos und verschiedene Währungen aufweisen, nicht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="0ba7d-147">This means that summary updates that have different invoice accounts and different currencies are not allowed.</span></span> <span data-ttu-id="0ba7d-148">Zusätzliche Parameter können in der Sammelaktualisierungsparameterseite eingerichtet werden, die von der Debitorenparameterseite zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="0ba7d-148">Additional parameters can be set up in the Summary update parameters page which is accessible from the Accounts receivable parameters page.</span></span>  
8. <span data-ttu-id="0ba7d-149">Klicken Sie im Feld Auftrag auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="0ba7d-149">In the Sales order field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="0ba7d-150">Wählen Sie in der Liste den als Sammelauftrag zu verwendenden Auftragsnummer aus.</span><span class="sxs-lookup"><span data-stu-id="0ba7d-150">In the list, select the order number that you want to be the summary order.</span></span>
10. <span data-ttu-id="0ba7d-151">Klicken Sie auf Anordnen.</span><span class="sxs-lookup"><span data-stu-id="0ba7d-151">Click Arrange.</span></span>
11. <span data-ttu-id="0ba7d-152">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="0ba7d-152">Click OK.</span></span>
12. <span data-ttu-id="0ba7d-153">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="0ba7d-153">Click OK.</span></span>


