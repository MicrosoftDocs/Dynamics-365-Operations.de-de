---
title: Dauerauftragsverkaufspreise
description: Beim Erstellen eines Dauerauftrags leitet sich der Verkaufspreis von den im Formular Verkaufspreisdauerauftrag erstellten Verkaufspreiseinstellungen ab.
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMASalespriceSubscription
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: d9d462121915ce3f800581a9540dc1ef8f6e785f
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---

# <a name="subscription-sales-prices"></a><span data-ttu-id="7d08f-103">Dauerauftragsverkaufspreise</span><span class="sxs-lookup"><span data-stu-id="7d08f-103">Subscription sales prices</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="7d08f-104">Beim Erstellen eines Dauerauftrags leitet sich der Verkaufspreis von den im Formular **Verkaufspreisdauerauftrag** erstellten Verkaufspreiseinstellungen ab.</span><span class="sxs-lookup"><span data-stu-id="7d08f-104">When you create a subscription, the sales price is derived from the sales price setup that was created in the **Sales price (subscription)** form.</span></span>

<span data-ttu-id="7d08f-105">Im Formular **Verkaufspreisdauerauftrag** können sowohl Verkaufspreise für einen bestimmten Dauerauftrag als auch Verkaufspreise erstellt werden, die eine flexiblere Anwendung ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="7d08f-105">In the **Sales price (subscription)** form, you can create sales prices for a specific subscription or you can create sales prices that apply more broadly.</span></span> <span data-ttu-id="7d08f-106">Damit ein Verkaufspreis auf einen Dauerauftrag angewendet werden kann, müssen der Periodencode sowie die Währung des Dauerauftrags mit dem Periodencode und der Währung des Verkaufspreises identisch sein.</span><span class="sxs-lookup"><span data-stu-id="7d08f-106">For a sales price to be applied to a subscription, the period code and the currency of the subscription must be identical to the period code and the currency of the sales price.</span></span>

<span data-ttu-id="7d08f-107">Bei identischem Periodencode und identischer Währung für Dauerauftrag und Verkaufspreis werden die Verkaufspreise des Dauerauftrags auf Basis der in der folgenden Tabelle aufgeführten Prioritäten ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="7d08f-107">If the period code and currency are identical for the subscription and the sales price, subscription sales prices are selected on the basis of the priorities listed in the following table.</span></span> <span data-ttu-id="7d08f-108">Ein leeres Feld wird in der Tabelle durch eine leere Zelle dargestellt, und ein "X" steht für einen Wert, der dem Wert im Dauerauftragsformular entspricht, in dem die Buchung generiert wird.</span><span class="sxs-lookup"><span data-stu-id="7d08f-108">A blank cell in the table indicates an empty field and an X indicates a value that is equal to the value in the subscription from which the transaction is generated.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7d08f-109">Priorität </span><span class="sxs-lookup"><span data-stu-id="7d08f-109">Priority</span></span></p></th>
<th><p><span data-ttu-id="7d08f-110"><strong>Kategorie</strong></span><span class="sxs-lookup"><span data-stu-id="7d08f-110"><strong>Category</strong></span></span></p></th>
<th><p><span data-ttu-id="7d08f-111"><strong>Projektkennung</strong></span><span class="sxs-lookup"><span data-stu-id="7d08f-111"><strong>Project ID</strong></span></span></p></th>
<th><p><span data-ttu-id="7d08f-112"><strong>Dauerauftrag</strong></span><span class="sxs-lookup"><span data-stu-id="7d08f-112"><strong>Subscription</strong></span></span></p></th>
<th><p><span data-ttu-id="7d08f-113"><strong>Verkaufswährung</strong></span><span class="sxs-lookup"><span data-stu-id="7d08f-113"><strong>Sales currency</strong></span></span></p></th>
<th><p><span data-ttu-id="7d08f-114"><strong>Periodencode</strong></span><span class="sxs-lookup"><span data-stu-id="7d08f-114"><strong>Period code</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7d08f-115">1</span><span class="sxs-lookup"><span data-stu-id="7d08f-115">1</span></span></p></td>
<td><p><span data-ttu-id="7d08f-116">X</span><span class="sxs-lookup"><span data-stu-id="7d08f-116">X</span></span></p></td>
<td><p><span data-ttu-id="7d08f-117">X</span><span class="sxs-lookup"><span data-stu-id="7d08f-117">X</span></span></p></td>
<td><p><span data-ttu-id="7d08f-118">X</span><span class="sxs-lookup"><span data-stu-id="7d08f-118">X</span></span></p></td>
<td><p><span data-ttu-id="7d08f-119">X</span><span class="sxs-lookup"><span data-stu-id="7d08f-119">X</span></span></p></td>
<td><p><span data-ttu-id="7d08f-120">X</span><span class="sxs-lookup"><span data-stu-id="7d08f-120">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d08f-121">2</span><span class="sxs-lookup"><span data-stu-id="7d08f-121">2</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="7d08f-122">X</span><span class="sxs-lookup"><span data-stu-id="7d08f-122">X</span></span></p></td>
<td><p><span data-ttu-id="7d08f-123">X</span><span class="sxs-lookup"><span data-stu-id="7d08f-123">X</span></span></p></td>
<td><p><span data-ttu-id="7d08f-124">X</span><span class="sxs-lookup"><span data-stu-id="7d08f-124">X</span></span></p></td>
<td><p><span data-ttu-id="7d08f-125">X</span><span class="sxs-lookup"><span data-stu-id="7d08f-125">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d08f-126">3</span><span class="sxs-lookup"><span data-stu-id="7d08f-126">3</span></span></p></td>
<td><p><span data-ttu-id="7d08f-127">X</span><span class="sxs-lookup"><span data-stu-id="7d08f-127">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="7d08f-128">X</span><span class="sxs-lookup"><span data-stu-id="7d08f-128">X</span></span></p></td>
<td><p><span data-ttu-id="7d08f-129">X</span><span class="sxs-lookup"><span data-stu-id="7d08f-129">X</span></span></p></td>
<td><p><span data-ttu-id="7d08f-130">X</span><span class="sxs-lookup"><span data-stu-id="7d08f-130">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d08f-131">4</span><span class="sxs-lookup"><span data-stu-id="7d08f-131">4</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="7d08f-132">X</span><span class="sxs-lookup"><span data-stu-id="7d08f-132">X</span></span></p></td>
<td><p><span data-ttu-id="7d08f-133">X</span><span class="sxs-lookup"><span data-stu-id="7d08f-133">X</span></span></p></td>
<td><p><span data-ttu-id="7d08f-134">X</span><span class="sxs-lookup"><span data-stu-id="7d08f-134">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d08f-135">5</span><span class="sxs-lookup"><span data-stu-id="7d08f-135">5</span></span></p></td>
<td><p><span data-ttu-id="7d08f-136">X</span><span class="sxs-lookup"><span data-stu-id="7d08f-136">X</span></span></p></td>
<td><p><span data-ttu-id="7d08f-137">X</span><span class="sxs-lookup"><span data-stu-id="7d08f-137">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="7d08f-138">X</span><span class="sxs-lookup"><span data-stu-id="7d08f-138">X</span></span></p></td>
<td><p><span data-ttu-id="7d08f-139">X</span><span class="sxs-lookup"><span data-stu-id="7d08f-139">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d08f-140">6</span><span class="sxs-lookup"><span data-stu-id="7d08f-140">6</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="7d08f-141">X</span><span class="sxs-lookup"><span data-stu-id="7d08f-141">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="7d08f-142">X</span><span class="sxs-lookup"><span data-stu-id="7d08f-142">X</span></span></p></td>
<td><p><span data-ttu-id="7d08f-143">X</span><span class="sxs-lookup"><span data-stu-id="7d08f-143">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d08f-144">7</span><span class="sxs-lookup"><span data-stu-id="7d08f-144">7</span></span></p></td>
<td><p><span data-ttu-id="7d08f-145">X</span><span class="sxs-lookup"><span data-stu-id="7d08f-145">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="7d08f-146">X</span><span class="sxs-lookup"><span data-stu-id="7d08f-146">X</span></span></p></td>
<td><p><span data-ttu-id="7d08f-147">X</span><span class="sxs-lookup"><span data-stu-id="7d08f-147">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d08f-148">8</span><span class="sxs-lookup"><span data-stu-id="7d08f-148">8</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="7d08f-149">X</span><span class="sxs-lookup"><span data-stu-id="7d08f-149">X</span></span></p></td>
<td><p><span data-ttu-id="7d08f-150">X</span><span class="sxs-lookup"><span data-stu-id="7d08f-150">X</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7d08f-151">Beim Erstellen einer Dauerauftragsgebühr wird der Verkaufspreis mit der höchsten Genauigkeit (gemäß obiger Tabelle) als Verkaufspreis für den Dauerauftrag ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="7d08f-151">When a subscription fee is created, the sales price with the greatest level of detail, as noted in the table above, is selected as the subscription sales price.</span></span>

## <a name="update-and-index-subscription-sales-prices"></a><span data-ttu-id="7d08f-152">Aktualisieren und Indizieren von Dauerauftragsverkaufspreisen</span><span class="sxs-lookup"><span data-stu-id="7d08f-152">Update and index subscription sales prices</span></span>

<span data-ttu-id="7d08f-153">Aktualisieren Sie zum Aktualisieren des Verkaufspreises für den Dauerauftrag den Basispreis oder den Index.</span><span class="sxs-lookup"><span data-stu-id="7d08f-153">You can update the subscription sales price by updating the base price or the index.</span></span> <span data-ttu-id="7d08f-154">Die Aktualisierung kann prozentual oder durch Angabe eines neues Werts vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="7d08f-154">You can update by a percentage or to a new value.</span></span>

## <a name="subscription-fee-sales-prices"></a><span data-ttu-id="7d08f-155">Verkaufspreise für Dauerauftragsgebühren</span><span class="sxs-lookup"><span data-stu-id="7d08f-155">Subscription fee sales prices</span></span>

<span data-ttu-id="7d08f-156">Beim Erstellen einer Dauerauftragsgebühr basiert der Verkaufspreis auf den Verkaufspreiseinstellungen des Dauerauftrags.</span><span class="sxs-lookup"><span data-stu-id="7d08f-156">When you create a subscription fee, the sales price is based on the sales price setup of the subscription.</span></span> <span data-ttu-id="7d08f-157">Sie können entweder den Basispreis aus den Preiseinstellungen des Dauerauftrags verwenden oder indizierte Verkaufspreise erstellen.</span><span class="sxs-lookup"><span data-stu-id="7d08f-157">You can either use the base price from the subscription price setup or create indexed sales prices.</span></span>

## <a name="example"></a><span data-ttu-id="7d08f-158">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7d08f-158">Example</span></span>

<span data-ttu-id="7d08f-159">Sie möchten für das neue Projekt "9030" Dauerauftragsverkaufspreise in Höhe von EUR 500 einrichten.</span><span class="sxs-lookup"><span data-stu-id="7d08f-159">You want to set up subscription sales prices of EUR 500 for a new project 9030.</span></span> <span data-ttu-id="7d08f-160">Im Formular **Verkaufspreisdauerauftrag** erstellen Sie eine Verkaufspreisposition für den Dauerauftrag, wie dies in der folgenden Tabelle angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="7d08f-160">In the **Sales price (subscription)** form, you create a subscription sales price line as indicated in the following table.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7d08f-161">Gültig ab</span><span class="sxs-lookup"><span data-stu-id="7d08f-161">Valid from</span></span></p></th>
<th><p><span data-ttu-id="7d08f-162">Kategorie</span><span class="sxs-lookup"><span data-stu-id="7d08f-162">Category</span></span></p></th>
<th><p><span data-ttu-id="7d08f-163">Projekt</span><span class="sxs-lookup"><span data-stu-id="7d08f-163">Project</span></span></p></th>
<th><p><span data-ttu-id="7d08f-164">Dauerauftrag</span><span class="sxs-lookup"><span data-stu-id="7d08f-164">Subscription</span></span></p></th>
<th><p><span data-ttu-id="7d08f-165">Periodencode</span><span class="sxs-lookup"><span data-stu-id="7d08f-165">Period code</span></span></p></th>
<th><p><span data-ttu-id="7d08f-166">Verkaufswährung</span><span class="sxs-lookup"><span data-stu-id="7d08f-166">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="7d08f-167">Verkaufspreis</span><span class="sxs-lookup"><span data-stu-id="7d08f-167">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7d08f-168">28.08.2006</span><span class="sxs-lookup"><span data-stu-id="7d08f-168">28-08-2006</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="7d08f-169">9030</span><span class="sxs-lookup"><span data-stu-id="7d08f-169">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="7d08f-170">Monat</span><span class="sxs-lookup"><span data-stu-id="7d08f-170">Month</span></span></p></td>
<td><p><span data-ttu-id="7d08f-171">EUR</span><span class="sxs-lookup"><span data-stu-id="7d08f-171">EUR</span></span></p></td>
<td><p><span data-ttu-id="7d08f-172">500</span><span class="sxs-lookup"><span data-stu-id="7d08f-172">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7d08f-173">Beachten Sie, dass die Felder **Kategorie** und **Dauerauftrag** leer sind.</span><span class="sxs-lookup"><span data-stu-id="7d08f-173">Note that the **Category** and **Subscription** fields are empty.</span></span>

<span data-ttu-id="7d08f-174">Anschließend werden die folgenden Daueraufträge erstellt.</span><span class="sxs-lookup"><span data-stu-id="7d08f-174">You then create the following subscriptions.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7d08f-175">Servicedauerauftrag</span><span class="sxs-lookup"><span data-stu-id="7d08f-175">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="7d08f-176">Projekt</span><span class="sxs-lookup"><span data-stu-id="7d08f-176">Project</span></span></p></th>
<th><p><span data-ttu-id="7d08f-177">Dauerauftragsgruppe</span><span class="sxs-lookup"><span data-stu-id="7d08f-177">Subscription group</span></span></p></th>
<th><p><span data-ttu-id="7d08f-178">Kategorie</span><span class="sxs-lookup"><span data-stu-id="7d08f-178">Category</span></span></p></th>
<th><p><span data-ttu-id="7d08f-179">Währung</span><span class="sxs-lookup"><span data-stu-id="7d08f-179">Currency</span></span></p></th>
<th><p><span data-ttu-id="7d08f-180">Periodencode</span><span class="sxs-lookup"><span data-stu-id="7d08f-180">Period code</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7d08f-181">00020_135</span><span class="sxs-lookup"><span data-stu-id="7d08f-181">00020_135</span></span></p></td>
<td><p><span data-ttu-id="7d08f-182">9030</span><span class="sxs-lookup"><span data-stu-id="7d08f-182">9030</span></span></p></td>
<td><p><span data-ttu-id="7d08f-183">Unter1</span><span class="sxs-lookup"><span data-stu-id="7d08f-183">Sub1</span></span></p></td>
<td><p><span data-ttu-id="7d08f-184">UnterKat1</span><span class="sxs-lookup"><span data-stu-id="7d08f-184">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="7d08f-185">EUR</span><span class="sxs-lookup"><span data-stu-id="7d08f-185">EUR</span></span></p></td>
<td><p><span data-ttu-id="7d08f-186">Monatlich</span><span class="sxs-lookup"><span data-stu-id="7d08f-186">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d08f-187">00021_135</span><span class="sxs-lookup"><span data-stu-id="7d08f-187">00021_135</span></span></p></td>
<td><p><span data-ttu-id="7d08f-188">9030</span><span class="sxs-lookup"><span data-stu-id="7d08f-188">9030</span></span></p></td>
<td><p><span data-ttu-id="7d08f-189">Unter1</span><span class="sxs-lookup"><span data-stu-id="7d08f-189">Sub1</span></span></p></td>
<td><p><span data-ttu-id="7d08f-190">UnterKat2</span><span class="sxs-lookup"><span data-stu-id="7d08f-190">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="7d08f-191">EUR</span><span class="sxs-lookup"><span data-stu-id="7d08f-191">EUR</span></span></p></td>
<td><p><span data-ttu-id="7d08f-192">Monatlich</span><span class="sxs-lookup"><span data-stu-id="7d08f-192">Monthly</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7d08f-193">Im nächsten Schritt werden die Dauerauftragsgebühren für die beiden Daueraufträge der Gruppe "Unter1" erstellt:</span><span class="sxs-lookup"><span data-stu-id="7d08f-193">Now you create subscription fees for both subscriptions in the subscription group Sub1:</span></span>

1.  <span data-ttu-id="7d08f-194">Klicken Sie auf **Servicemanagement** \> **Einrichtung** \> **Daueraufträge** \> **Dauerauftragsgruppen**.</span><span class="sxs-lookup"><span data-stu-id="7d08f-194">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

2.  <span data-ttu-id="7d08f-195">In der **Dauerauftragsgruppen** im Formular und klicken im Formular **Funktion** \> **Dauerauftragsgebühr erstellen**.</span><span class="sxs-lookup"><span data-stu-id="7d08f-195">In the **Subscription groups** form, click **Function** \> **Create subscription fee**.</span></span>

3.  <span data-ttu-id="7d08f-196">In der **Dauerauftragsgebühr erstellen** Formular geben Sie die entsprechenden Informationen ein.</span><span class="sxs-lookup"><span data-stu-id="7d08f-196">In the **Create subscription fee** form, enter the appropriate information.</span></span> <span data-ttu-id="7d08f-197">Weitere Informationen finden Sie unter [Dauerauftragsgebühren-Buchungen erstellen](create-subscription-fee-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="7d08f-197">For more information, see [Create subscription fee transactions](create-subscription-fee-transactions.md).</span></span>

<span data-ttu-id="7d08f-198">Für beide Daueraufträge werden Dauerauftragsgebühren mit einem Verkaufspreis von EUR 500 erstellt. Dies ist in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="7d08f-198">Subscription fees that have a sales price of EUR 500 are created for both subscriptions, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7d08f-199">Projektdatum</span><span class="sxs-lookup"><span data-stu-id="7d08f-199">Project date</span></span></p></th>
<th><p><span data-ttu-id="7d08f-200">Servicedauerauftrag</span><span class="sxs-lookup"><span data-stu-id="7d08f-200">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="7d08f-201">Projekt</span><span class="sxs-lookup"><span data-stu-id="7d08f-201">Project</span></span></p></th>
<th><p><span data-ttu-id="7d08f-202">Kategorie</span><span class="sxs-lookup"><span data-stu-id="7d08f-202">Category</span></span></p></th>
<th><p><span data-ttu-id="7d08f-203">Startdatum</span><span class="sxs-lookup"><span data-stu-id="7d08f-203">Start date</span></span></p></th>
<th><p><span data-ttu-id="7d08f-204">Enddatum</span><span class="sxs-lookup"><span data-stu-id="7d08f-204">End date</span></span></p></th>
<th><p><span data-ttu-id="7d08f-205">Verkaufswährung</span><span class="sxs-lookup"><span data-stu-id="7d08f-205">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="7d08f-206">Verkaufspreis</span><span class="sxs-lookup"><span data-stu-id="7d08f-206">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7d08f-207">28.08.2006</span><span class="sxs-lookup"><span data-stu-id="7d08f-207">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="7d08f-208">00020_135</span><span class="sxs-lookup"><span data-stu-id="7d08f-208">00020_135</span></span></p></td>
<td><p><span data-ttu-id="7d08f-209">9030</span><span class="sxs-lookup"><span data-stu-id="7d08f-209">9030</span></span></p></td>
<td><p><span data-ttu-id="7d08f-210">UnterKat1</span><span class="sxs-lookup"><span data-stu-id="7d08f-210">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="7d08f-211">01.01.2007</span><span class="sxs-lookup"><span data-stu-id="7d08f-211">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="7d08f-212">31.03.2007</span><span class="sxs-lookup"><span data-stu-id="7d08f-212">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="7d08f-213">EUR</span><span class="sxs-lookup"><span data-stu-id="7d08f-213">EUR</span></span></p></td>
<td><p><span data-ttu-id="7d08f-214">500</span><span class="sxs-lookup"><span data-stu-id="7d08f-214">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d08f-215">28.08.2006</span><span class="sxs-lookup"><span data-stu-id="7d08f-215">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="7d08f-216">00021_135</span><span class="sxs-lookup"><span data-stu-id="7d08f-216">00021_135</span></span></p></td>
<td><p><span data-ttu-id="7d08f-217">9030</span><span class="sxs-lookup"><span data-stu-id="7d08f-217">9030</span></span></p></td>
<td><p><span data-ttu-id="7d08f-218">UnterKat2</span><span class="sxs-lookup"><span data-stu-id="7d08f-218">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="7d08f-219">01.01.2007</span><span class="sxs-lookup"><span data-stu-id="7d08f-219">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="7d08f-220">31.03.2007</span><span class="sxs-lookup"><span data-stu-id="7d08f-220">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="7d08f-221">EUR</span><span class="sxs-lookup"><span data-stu-id="7d08f-221">EUR</span></span></p></td>
<td><p><span data-ttu-id="7d08f-222">500</span><span class="sxs-lookup"><span data-stu-id="7d08f-222">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7d08f-223">Später entschließen Sie sich zum Angeben von Verkaufspreisen für die Kategorie "UnterKat1" des Projekts "9030".</span><span class="sxs-lookup"><span data-stu-id="7d08f-223">Later, you decide that you want to specify sales prices for the category SubCat1 for project 9030.</span></span> <span data-ttu-id="7d08f-224">Zu diesem Zweck erstellen Sie für die Kombination aus Projekt "9030" und Gebührenkategorie "UnterKat1" eine neue Verkaufspreisposition mit einem Verkaufspreis von EUR 550.</span><span class="sxs-lookup"><span data-stu-id="7d08f-224">Therefore, you create a new sales price line that has a sales price of EUR 550 for the combination of project 9030 and fee category SubCat1.</span></span> <span data-ttu-id="7d08f-225">Für das Projekt "9030" sind nun zwei Verkaufspreispositionen für Daueraufträge vorhanden. Dies ist in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="7d08f-225">There are now two subscription sales price lines for project 9030, as shown in the following table.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7d08f-226">Gültig ab</span><span class="sxs-lookup"><span data-stu-id="7d08f-226">Valid from</span></span></p></th>
<th><p><span data-ttu-id="7d08f-227">Kategorie</span><span class="sxs-lookup"><span data-stu-id="7d08f-227">Category</span></span></p></th>
<th><p><span data-ttu-id="7d08f-228">Projekt</span><span class="sxs-lookup"><span data-stu-id="7d08f-228">Project</span></span></p></th>
<th><p><span data-ttu-id="7d08f-229">Dauerauftrag</span><span class="sxs-lookup"><span data-stu-id="7d08f-229">Subscription</span></span></p></th>
<th><p><span data-ttu-id="7d08f-230">Periodencode</span><span class="sxs-lookup"><span data-stu-id="7d08f-230">Period code</span></span></p></th>
<th><p><span data-ttu-id="7d08f-231">Währung</span><span class="sxs-lookup"><span data-stu-id="7d08f-231">Currency</span></span></p></th>
<th><p><span data-ttu-id="7d08f-232">Verkaufspreis</span><span class="sxs-lookup"><span data-stu-id="7d08f-232">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7d08f-233">28.08.2007</span><span class="sxs-lookup"><span data-stu-id="7d08f-233">28-08-2007</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="7d08f-234">9030</span><span class="sxs-lookup"><span data-stu-id="7d08f-234">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="7d08f-235">Monat</span><span class="sxs-lookup"><span data-stu-id="7d08f-235">Month</span></span></p></td>
<td><p><span data-ttu-id="7d08f-236">EUR</span><span class="sxs-lookup"><span data-stu-id="7d08f-236">EUR</span></span></p></td>
<td><p><span data-ttu-id="7d08f-237">500</span><span class="sxs-lookup"><span data-stu-id="7d08f-237">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d08f-238">28.08.2007</span><span class="sxs-lookup"><span data-stu-id="7d08f-238">28-08-2007</span></span></p></td>
<td><p><span data-ttu-id="7d08f-239">UnterKat1</span><span class="sxs-lookup"><span data-stu-id="7d08f-239">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="7d08f-240">9030</span><span class="sxs-lookup"><span data-stu-id="7d08f-240">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="7d08f-241">Monat</span><span class="sxs-lookup"><span data-stu-id="7d08f-241">Month</span></span></p></td>
<td><p><span data-ttu-id="7d08f-242">EUR</span><span class="sxs-lookup"><span data-stu-id="7d08f-242">EUR</span></span></p></td>
<td><p><span data-ttu-id="7d08f-243">550</span><span class="sxs-lookup"><span data-stu-id="7d08f-243">550</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7d08f-244">Sie wiederholen das oben beschriebene Verfahren und erstellen Dauerauftragsgebühren für beide Daueraufträge der Dauerauftragsgruppe "Unter1".</span><span class="sxs-lookup"><span data-stu-id="7d08f-244">You repeat the procedure described above to create subscription fees for both subscriptions in the subscription group Sub1.</span></span> <span data-ttu-id="7d08f-245">In der folgenden Tabelle sind die Buchungen aufgeführt, die für die einzelnen Daueraufträge erstellt werden, die der Dauerauftragsgruppe zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="7d08f-245">The following table shows the transactions that are created for each subscription that is attached to the subscription group.</span></span>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7d08f-246">Projektdatum</span><span class="sxs-lookup"><span data-stu-id="7d08f-246">Project date</span></span></p></th>
<th><p><span data-ttu-id="7d08f-247">Dauerauftrag</span><span class="sxs-lookup"><span data-stu-id="7d08f-247">Subscription</span></span></p></th>
<th><p><span data-ttu-id="7d08f-248">Projekt</span><span class="sxs-lookup"><span data-stu-id="7d08f-248">Project</span></span></p></th>
<th><p><span data-ttu-id="7d08f-249">Kategorie</span><span class="sxs-lookup"><span data-stu-id="7d08f-249">Category</span></span></p></th>
<th><p><span data-ttu-id="7d08f-250">Startdatum</span><span class="sxs-lookup"><span data-stu-id="7d08f-250">Start date</span></span></p></th>
<th><p><span data-ttu-id="7d08f-251">Enddatum</span><span class="sxs-lookup"><span data-stu-id="7d08f-251">End date</span></span></p></th>
<th><p><span data-ttu-id="7d08f-252">Verkaufswährung</span><span class="sxs-lookup"><span data-stu-id="7d08f-252">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="7d08f-253">Verkaufspreis</span><span class="sxs-lookup"><span data-stu-id="7d08f-253">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7d08f-254">28.07.2007</span><span class="sxs-lookup"><span data-stu-id="7d08f-254">28-07-2007</span></span></p></td>
<td><p><span data-ttu-id="7d08f-255">00020_135</span><span class="sxs-lookup"><span data-stu-id="7d08f-255">00020_135</span></span></p></td>
<td><p><span data-ttu-id="7d08f-256">9030</span><span class="sxs-lookup"><span data-stu-id="7d08f-256">9030</span></span></p></td>
<td><p><span data-ttu-id="7d08f-257">UnterKat1</span><span class="sxs-lookup"><span data-stu-id="7d08f-257">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="7d08f-258">01.01.2008</span><span class="sxs-lookup"><span data-stu-id="7d08f-258">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="7d08f-259">31.03.2008</span><span class="sxs-lookup"><span data-stu-id="7d08f-259">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="7d08f-260">EUR</span><span class="sxs-lookup"><span data-stu-id="7d08f-260">EUR</span></span></p></td>
<td><p><span data-ttu-id="7d08f-261">550</span><span class="sxs-lookup"><span data-stu-id="7d08f-261">550</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d08f-262">28.07.2008</span><span class="sxs-lookup"><span data-stu-id="7d08f-262">28-07-2008</span></span></p></td>
<td><p><span data-ttu-id="7d08f-263">00021_135</span><span class="sxs-lookup"><span data-stu-id="7d08f-263">00021_135</span></span></p></td>
<td><p><span data-ttu-id="7d08f-264">9030</span><span class="sxs-lookup"><span data-stu-id="7d08f-264">9030</span></span></p></td>
<td><p><span data-ttu-id="7d08f-265">UnterKat2</span><span class="sxs-lookup"><span data-stu-id="7d08f-265">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="7d08f-266">01.01.2008</span><span class="sxs-lookup"><span data-stu-id="7d08f-266">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="7d08f-267">31.03.2008</span><span class="sxs-lookup"><span data-stu-id="7d08f-267">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="7d08f-268">EUR</span><span class="sxs-lookup"><span data-stu-id="7d08f-268">EUR</span></span></p></td>
<td><p><span data-ttu-id="7d08f-269">500</span><span class="sxs-lookup"><span data-stu-id="7d08f-269">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7d08f-270">In der ersten Buchung für den Dauerauftrag 00020\_135 wird der Verkaufspreis in Höhe von EUR 550 von dem Dauerauftragsverkaufspreis abgeleitet, der für die Kombination aus diesem speziellen Projekt und der Kategorie festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7d08f-270">In the first transaction for subscription 00020\_135, the sales price of EUR 550 derives from the subscription sales price that is set up for the combination of the specific project and category.</span></span> <span data-ttu-id="7d08f-271">In der zweiten Buchung für den Dauerauftrag 00021\_135 wird als Verkaufspreis für den Projektdauerauftrag der Betrag EUR 500 verwendet, da für die Kombination aus dem Projekt "9030" und der Kategorie "UnterKat2" kein Preis eingerichtet wurde.</span><span class="sxs-lookup"><span data-stu-id="7d08f-271">In the second transaction for subscription 00021\_135, the sales price of EUR 500 is used as the project subscription sales price because there is no price set up for the combination of project 9030 and category SubCat2.</span></span>

## <a name="see-also"></a><span data-ttu-id="7d08f-272">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d08f-272">See also</span></span>

[<span data-ttu-id="7d08f-273">Aktualisieren und Indizieren von Dauerauftrag-Verkaufspreisen</span><span class="sxs-lookup"><span data-stu-id="7d08f-273">Update and index subscription sales prices</span></span>](update-and-index-subscription-sales-prices.md)

  



