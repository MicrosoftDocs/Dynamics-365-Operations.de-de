---
title: Dauerauftragsverkaufspreise
description: Beim Erstellen eines Dauerauftrags leitet sich der Verkaufspreis von den im Formular Verkaufspreisdauerauftrag erstellten Verkaufspreiseinstellungen ab.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASalespriceSubscription
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f03efbbca4fc9da76c6ead7566457beb79c8c249
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428627"
---
# <a name="subscription-sales-prices"></a><span data-ttu-id="6c164-103">Dauerauftragsverkaufspreise</span><span class="sxs-lookup"><span data-stu-id="6c164-103">Subscription sales prices</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="6c164-104">Beim Erstellen eines Dauerauftrags leitet sich der Verkaufspreis von den im Formular **Verkaufspreisdauerauftrag** erstellten Verkaufspreiseinstellungen ab.</span><span class="sxs-lookup"><span data-stu-id="6c164-104">When you create a subscription, the sales price is derived from the sales price setup that was created in the **Sales price (subscription)** form.</span></span>

<span data-ttu-id="6c164-105">Im Formular **Verkaufspreisdauerauftrag** können sowohl Verkaufspreise für einen bestimmten Dauerauftrag als auch Verkaufspreise erstellt werden, die eine flexiblere Anwendung ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="6c164-105">In the **Sales price (subscription)** form, you can create sales prices for a specific subscription or you can create sales prices that apply more broadly.</span></span> <span data-ttu-id="6c164-106">Damit ein Verkaufspreis auf einen Dauerauftrag angewendet werden kann, müssen der Periodencode sowie die Währung des Dauerauftrags mit dem Periodencode und der Währung des Verkaufspreises identisch sein.</span><span class="sxs-lookup"><span data-stu-id="6c164-106">For a sales price to be applied to a subscription, the period code and the currency of the subscription must be identical to the period code and the currency of the sales price.</span></span>

<span data-ttu-id="6c164-107">Bei identischem Periodencode und identischer Währung für Dauerauftrag und Verkaufspreis werden die Verkaufspreise des Dauerauftrags auf Basis der in der folgenden Tabelle aufgeführten Prioritäten ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="6c164-107">If the period code and currency are identical for the subscription and the sales price, subscription sales prices are selected on the basis of the priorities listed in the following table.</span></span> <span data-ttu-id="6c164-108">Ein leeres Feld wird in der Tabelle durch eine leere Zelle dargestellt, und ein "X" steht für einen Wert, der dem Wert im Dauerauftragsformular entspricht, in dem die Buchung generiert wird.</span><span class="sxs-lookup"><span data-stu-id="6c164-108">A blank cell in the table indicates an empty field and an X indicates a value that is equal to the value in the subscription from which the transaction is generated.</span></span>

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
<th><p><span data-ttu-id="6c164-109">Priorität </span><span class="sxs-lookup"><span data-stu-id="6c164-109">Priority</span></span></p></th>
<th><p><span data-ttu-id="6c164-110"><strong>Kategorie</strong></span><span class="sxs-lookup"><span data-stu-id="6c164-110"><strong>Category</strong></span></span></p></th>
<th><p><span data-ttu-id="6c164-111"><strong>Projektkennung</strong></span><span class="sxs-lookup"><span data-stu-id="6c164-111"><strong>Project ID</strong></span></span></p></th>
<th><p><span data-ttu-id="6c164-112"><strong>Dauerauftrag</strong></span><span class="sxs-lookup"><span data-stu-id="6c164-112"><strong>Subscription</strong></span></span></p></th>
<th><p><span data-ttu-id="6c164-113"><strong>Verkaufswährung</strong></span><span class="sxs-lookup"><span data-stu-id="6c164-113"><strong>Sales currency</strong></span></span></p></th>
<th><p><span data-ttu-id="6c164-114"><strong>Periodencode</strong></span><span class="sxs-lookup"><span data-stu-id="6c164-114"><strong>Period code</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c164-115">1</span><span class="sxs-lookup"><span data-stu-id="6c164-115">1</span></span></p></td>
<td><p><span data-ttu-id="6c164-116">X</span><span class="sxs-lookup"><span data-stu-id="6c164-116">X</span></span></p></td>
<td><p><span data-ttu-id="6c164-117">X</span><span class="sxs-lookup"><span data-stu-id="6c164-117">X</span></span></p></td>
<td><p><span data-ttu-id="6c164-118">X</span><span class="sxs-lookup"><span data-stu-id="6c164-118">X</span></span></p></td>
<td><p><span data-ttu-id="6c164-119">X</span><span class="sxs-lookup"><span data-stu-id="6c164-119">X</span></span></p></td>
<td><p><span data-ttu-id="6c164-120">X</span><span class="sxs-lookup"><span data-stu-id="6c164-120">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c164-121">2</span><span class="sxs-lookup"><span data-stu-id="6c164-121">2</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="6c164-122">X</span><span class="sxs-lookup"><span data-stu-id="6c164-122">X</span></span></p></td>
<td><p><span data-ttu-id="6c164-123">X</span><span class="sxs-lookup"><span data-stu-id="6c164-123">X</span></span></p></td>
<td><p><span data-ttu-id="6c164-124">X</span><span class="sxs-lookup"><span data-stu-id="6c164-124">X</span></span></p></td>
<td><p><span data-ttu-id="6c164-125">X</span><span class="sxs-lookup"><span data-stu-id="6c164-125">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c164-126">3</span><span class="sxs-lookup"><span data-stu-id="6c164-126">3</span></span></p></td>
<td><p><span data-ttu-id="6c164-127">X</span><span class="sxs-lookup"><span data-stu-id="6c164-127">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="6c164-128">X</span><span class="sxs-lookup"><span data-stu-id="6c164-128">X</span></span></p></td>
<td><p><span data-ttu-id="6c164-129">X</span><span class="sxs-lookup"><span data-stu-id="6c164-129">X</span></span></p></td>
<td><p><span data-ttu-id="6c164-130">X</span><span class="sxs-lookup"><span data-stu-id="6c164-130">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c164-131">4</span><span class="sxs-lookup"><span data-stu-id="6c164-131">4</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="6c164-132">X</span><span class="sxs-lookup"><span data-stu-id="6c164-132">X</span></span></p></td>
<td><p><span data-ttu-id="6c164-133">X</span><span class="sxs-lookup"><span data-stu-id="6c164-133">X</span></span></p></td>
<td><p><span data-ttu-id="6c164-134">X</span><span class="sxs-lookup"><span data-stu-id="6c164-134">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c164-135">5</span><span class="sxs-lookup"><span data-stu-id="6c164-135">5</span></span></p></td>
<td><p><span data-ttu-id="6c164-136">X</span><span class="sxs-lookup"><span data-stu-id="6c164-136">X</span></span></p></td>
<td><p><span data-ttu-id="6c164-137">X</span><span class="sxs-lookup"><span data-stu-id="6c164-137">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="6c164-138">X</span><span class="sxs-lookup"><span data-stu-id="6c164-138">X</span></span></p></td>
<td><p><span data-ttu-id="6c164-139">X</span><span class="sxs-lookup"><span data-stu-id="6c164-139">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c164-140">6</span><span class="sxs-lookup"><span data-stu-id="6c164-140">6</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="6c164-141">X</span><span class="sxs-lookup"><span data-stu-id="6c164-141">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="6c164-142">X</span><span class="sxs-lookup"><span data-stu-id="6c164-142">X</span></span></p></td>
<td><p><span data-ttu-id="6c164-143">X</span><span class="sxs-lookup"><span data-stu-id="6c164-143">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c164-144">7</span><span class="sxs-lookup"><span data-stu-id="6c164-144">7</span></span></p></td>
<td><p><span data-ttu-id="6c164-145">X</span><span class="sxs-lookup"><span data-stu-id="6c164-145">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="6c164-146">X</span><span class="sxs-lookup"><span data-stu-id="6c164-146">X</span></span></p></td>
<td><p><span data-ttu-id="6c164-147">X</span><span class="sxs-lookup"><span data-stu-id="6c164-147">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c164-148">8</span><span class="sxs-lookup"><span data-stu-id="6c164-148">8</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="6c164-149">X</span><span class="sxs-lookup"><span data-stu-id="6c164-149">X</span></span></p></td>
<td><p><span data-ttu-id="6c164-150">X</span><span class="sxs-lookup"><span data-stu-id="6c164-150">X</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6c164-151">Beim Erstellen einer Dauerauftragsgebühr wird der Verkaufspreis mit der höchsten Genauigkeit (gemäß obiger Tabelle) als Verkaufspreis für den Dauerauftrag ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="6c164-151">When a subscription fee is created, the sales price with the greatest level of detail, as noted in the table above, is selected as the subscription sales price.</span></span>

## <a name="update-and-index-subscription-sales-prices"></a><span data-ttu-id="6c164-152">Aktualisieren und Indizieren von Dauerauftragsverkaufspreisen</span><span class="sxs-lookup"><span data-stu-id="6c164-152">Update and index subscription sales prices</span></span>

<span data-ttu-id="6c164-153">Aktualisieren Sie zum Aktualisieren des Verkaufspreises für den Dauerauftrag den Basispreis oder den Index.</span><span class="sxs-lookup"><span data-stu-id="6c164-153">You can update the subscription sales price by updating the base price or the index.</span></span> <span data-ttu-id="6c164-154">Die Aktualisierung kann prozentual oder durch Angabe eines neues Werts vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="6c164-154">You can update by a percentage or to a new value.</span></span>

## <a name="subscription-fee-sales-prices"></a><span data-ttu-id="6c164-155">Verkaufspreise für Dauerauftragsgebühren</span><span class="sxs-lookup"><span data-stu-id="6c164-155">Subscription fee sales prices</span></span>

<span data-ttu-id="6c164-156">Beim Erstellen einer Dauerauftragsgebühr basiert der Verkaufspreis auf den Verkaufspreiseinstellungen des Dauerauftrags.</span><span class="sxs-lookup"><span data-stu-id="6c164-156">When you create a subscription fee, the sales price is based on the sales price setup of the subscription.</span></span> <span data-ttu-id="6c164-157">Sie können entweder den Basispreis aus den Preiseinstellungen des Dauerauftrags verwenden oder indizierte Verkaufspreise erstellen.</span><span class="sxs-lookup"><span data-stu-id="6c164-157">You can either use the base price from the subscription price setup or create indexed sales prices.</span></span>

## <a name="example"></a><span data-ttu-id="6c164-158">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6c164-158">Example</span></span>

<span data-ttu-id="6c164-159">Sie möchten für das neue Projekt "9030" Dauerauftragsverkaufspreise in Höhe von EUR 500 einrichten.</span><span class="sxs-lookup"><span data-stu-id="6c164-159">You want to set up subscription sales prices of EUR 500 for a new project 9030.</span></span> <span data-ttu-id="6c164-160">Im Formular **Verkaufspreisdauerauftrag** erstellen Sie eine Verkaufspreisposition für den Dauerauftrag, wie dies in der folgenden Tabelle angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="6c164-160">In the **Sales price (subscription)** form, you create a subscription sales price line as indicated in the following table.</span></span>

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
<th><p><span data-ttu-id="6c164-161">Gültig ab</span><span class="sxs-lookup"><span data-stu-id="6c164-161">Valid from</span></span></p></th>
<th><p><span data-ttu-id="6c164-162">Kategorie</span><span class="sxs-lookup"><span data-stu-id="6c164-162">Category</span></span></p></th>
<th><p><span data-ttu-id="6c164-163">Projekt</span><span class="sxs-lookup"><span data-stu-id="6c164-163">Project</span></span></p></th>
<th><p><span data-ttu-id="6c164-164">Dauerauftrag</span><span class="sxs-lookup"><span data-stu-id="6c164-164">Subscription</span></span></p></th>
<th><p><span data-ttu-id="6c164-165">Periodencode</span><span class="sxs-lookup"><span data-stu-id="6c164-165">Period code</span></span></p></th>
<th><p><span data-ttu-id="6c164-166">Verkaufswährung</span><span class="sxs-lookup"><span data-stu-id="6c164-166">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="6c164-167">Verkaufspreis</span><span class="sxs-lookup"><span data-stu-id="6c164-167">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c164-168">28.08.2006</span><span class="sxs-lookup"><span data-stu-id="6c164-168">28-08-2006</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6c164-169">9030</span><span class="sxs-lookup"><span data-stu-id="6c164-169">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6c164-170">Monat</span><span class="sxs-lookup"><span data-stu-id="6c164-170">Month</span></span></p></td>
<td><p><span data-ttu-id="6c164-171">EUR</span><span class="sxs-lookup"><span data-stu-id="6c164-171">EUR</span></span></p></td>
<td><p><span data-ttu-id="6c164-172">500</span><span class="sxs-lookup"><span data-stu-id="6c164-172">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6c164-173">Beachten Sie, dass die Felder **Kategorie** und **Dauerauftrag** leer sind.</span><span class="sxs-lookup"><span data-stu-id="6c164-173">Note that the **Category** and **Subscription** fields are empty.</span></span>

<span data-ttu-id="6c164-174">Anschließend werden die folgenden Daueraufträge erstellt.</span><span class="sxs-lookup"><span data-stu-id="6c164-174">You then create the following subscriptions.</span></span>

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
<th><p><span data-ttu-id="6c164-175">Servicedauerauftrag</span><span class="sxs-lookup"><span data-stu-id="6c164-175">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="6c164-176">Projekt</span><span class="sxs-lookup"><span data-stu-id="6c164-176">Project</span></span></p></th>
<th><p><span data-ttu-id="6c164-177">Dauerauftragsgruppe</span><span class="sxs-lookup"><span data-stu-id="6c164-177">Subscription group</span></span></p></th>
<th><p><span data-ttu-id="6c164-178">Kategorie</span><span class="sxs-lookup"><span data-stu-id="6c164-178">Category</span></span></p></th>
<th><p><span data-ttu-id="6c164-179">Währung</span><span class="sxs-lookup"><span data-stu-id="6c164-179">Currency</span></span></p></th>
<th><p><span data-ttu-id="6c164-180">Periodencode</span><span class="sxs-lookup"><span data-stu-id="6c164-180">Period code</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c164-181">00020_135</span><span class="sxs-lookup"><span data-stu-id="6c164-181">00020_135</span></span></p></td>
<td><p><span data-ttu-id="6c164-182">9030</span><span class="sxs-lookup"><span data-stu-id="6c164-182">9030</span></span></p></td>
<td><p><span data-ttu-id="6c164-183">Unter1</span><span class="sxs-lookup"><span data-stu-id="6c164-183">Sub1</span></span></p></td>
<td><p><span data-ttu-id="6c164-184">UnterKat1</span><span class="sxs-lookup"><span data-stu-id="6c164-184">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="6c164-185">EUR</span><span class="sxs-lookup"><span data-stu-id="6c164-185">EUR</span></span></p></td>
<td><p><span data-ttu-id="6c164-186">Monatlich</span><span class="sxs-lookup"><span data-stu-id="6c164-186">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c164-187">00021_135</span><span class="sxs-lookup"><span data-stu-id="6c164-187">00021_135</span></span></p></td>
<td><p><span data-ttu-id="6c164-188">9030</span><span class="sxs-lookup"><span data-stu-id="6c164-188">9030</span></span></p></td>
<td><p><span data-ttu-id="6c164-189">Unter1</span><span class="sxs-lookup"><span data-stu-id="6c164-189">Sub1</span></span></p></td>
<td><p><span data-ttu-id="6c164-190">UnterKat2</span><span class="sxs-lookup"><span data-stu-id="6c164-190">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="6c164-191">EUR</span><span class="sxs-lookup"><span data-stu-id="6c164-191">EUR</span></span></p></td>
<td><p><span data-ttu-id="6c164-192">Monatlich</span><span class="sxs-lookup"><span data-stu-id="6c164-192">Monthly</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6c164-193">Im nächsten Schritt werden die Dauerauftragsgebühren für die beiden Daueraufträge der Gruppe "Unter1" erstellt:</span><span class="sxs-lookup"><span data-stu-id="6c164-193">Now you create subscription fees for both subscriptions in the subscription group Sub1:</span></span>

1.  <span data-ttu-id="6c164-194">Klicken Sie auf **Servicemanagement** \> **Einrichtung** \> **Daueraufträge** \> **Dauerauftragsgruppen**.</span><span class="sxs-lookup"><span data-stu-id="6c164-194">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

2.  <span data-ttu-id="6c164-195">In der **Dauerauftragsgruppen** im Formular und klicken im Formular **Funktion** \> **Dauerauftragsgebühr erstellen**.</span><span class="sxs-lookup"><span data-stu-id="6c164-195">In the **Subscription groups** form, click **Function** \> **Create subscription fee**.</span></span>

3.  <span data-ttu-id="6c164-196">In der **Dauerauftragsgebühr erstellen** Formular geben Sie die entsprechenden Informationen ein.</span><span class="sxs-lookup"><span data-stu-id="6c164-196">In the **Create subscription fee** form, enter the appropriate information.</span></span> <span data-ttu-id="6c164-197">Weitere Informationen finden Sie unter [Dauerauftragsgebühren-Buchungen erstellen](create-subscription-fee-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="6c164-197">For more information, see [Create subscription fee transactions](create-subscription-fee-transactions.md).</span></span>

<span data-ttu-id="6c164-198">Für beide Daueraufträge werden Dauerauftragsgebühren mit einem Verkaufspreis von EUR 500 erstellt. Dies ist in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="6c164-198">Subscription fees that have a sales price of EUR 500 are created for both subscriptions, as shown in the following table.</span></span>

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
<th><p><span data-ttu-id="6c164-199">Projektdatum</span><span class="sxs-lookup"><span data-stu-id="6c164-199">Project date</span></span></p></th>
<th><p><span data-ttu-id="6c164-200">Servicedauerauftrag</span><span class="sxs-lookup"><span data-stu-id="6c164-200">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="6c164-201">Projekt</span><span class="sxs-lookup"><span data-stu-id="6c164-201">Project</span></span></p></th>
<th><p><span data-ttu-id="6c164-202">Kategorie</span><span class="sxs-lookup"><span data-stu-id="6c164-202">Category</span></span></p></th>
<th><p><span data-ttu-id="6c164-203">Startdatum</span><span class="sxs-lookup"><span data-stu-id="6c164-203">Start date</span></span></p></th>
<th><p><span data-ttu-id="6c164-204">Enddatum</span><span class="sxs-lookup"><span data-stu-id="6c164-204">End date</span></span></p></th>
<th><p><span data-ttu-id="6c164-205">Verkaufswährung</span><span class="sxs-lookup"><span data-stu-id="6c164-205">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="6c164-206">Verkaufspreis</span><span class="sxs-lookup"><span data-stu-id="6c164-206">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c164-207">28.08.2006</span><span class="sxs-lookup"><span data-stu-id="6c164-207">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="6c164-208">00020_135</span><span class="sxs-lookup"><span data-stu-id="6c164-208">00020_135</span></span></p></td>
<td><p><span data-ttu-id="6c164-209">9030</span><span class="sxs-lookup"><span data-stu-id="6c164-209">9030</span></span></p></td>
<td><p><span data-ttu-id="6c164-210">UnterKat1</span><span class="sxs-lookup"><span data-stu-id="6c164-210">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="6c164-211">01.01.2007</span><span class="sxs-lookup"><span data-stu-id="6c164-211">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="6c164-212">31.03.2007</span><span class="sxs-lookup"><span data-stu-id="6c164-212">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="6c164-213">EUR</span><span class="sxs-lookup"><span data-stu-id="6c164-213">EUR</span></span></p></td>
<td><p><span data-ttu-id="6c164-214">500</span><span class="sxs-lookup"><span data-stu-id="6c164-214">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c164-215">28.08.2006</span><span class="sxs-lookup"><span data-stu-id="6c164-215">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="6c164-216">00021_135</span><span class="sxs-lookup"><span data-stu-id="6c164-216">00021_135</span></span></p></td>
<td><p><span data-ttu-id="6c164-217">9030</span><span class="sxs-lookup"><span data-stu-id="6c164-217">9030</span></span></p></td>
<td><p><span data-ttu-id="6c164-218">UnterKat2</span><span class="sxs-lookup"><span data-stu-id="6c164-218">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="6c164-219">01.01.2007</span><span class="sxs-lookup"><span data-stu-id="6c164-219">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="6c164-220">31.03.2007</span><span class="sxs-lookup"><span data-stu-id="6c164-220">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="6c164-221">EUR</span><span class="sxs-lookup"><span data-stu-id="6c164-221">EUR</span></span></p></td>
<td><p><span data-ttu-id="6c164-222">500</span><span class="sxs-lookup"><span data-stu-id="6c164-222">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6c164-223">Später entschließen Sie sich zum Angeben von Verkaufspreisen für die Kategorie "UnterKat1" des Projekts "9030".</span><span class="sxs-lookup"><span data-stu-id="6c164-223">Later, you decide that you want to specify sales prices for the category SubCat1 for project 9030.</span></span> <span data-ttu-id="6c164-224">Zu diesem Zweck erstellen Sie für die Kombination aus Projekt "9030" und Gebührenkategorie "UnterKat1" eine neue Verkaufspreisposition mit einem Verkaufspreis von EUR 550.</span><span class="sxs-lookup"><span data-stu-id="6c164-224">Therefore, you create a new sales price line that has a sales price of EUR 550 for the combination of project 9030 and fee category SubCat1.</span></span> <span data-ttu-id="6c164-225">Für das Projekt "9030" sind nun zwei Verkaufspreispositionen für Daueraufträge vorhanden. Dies ist in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="6c164-225">There are now two subscription sales price lines for project 9030, as shown in the following table.</span></span>

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
<th><p><span data-ttu-id="6c164-226">Gültig ab</span><span class="sxs-lookup"><span data-stu-id="6c164-226">Valid from</span></span></p></th>
<th><p><span data-ttu-id="6c164-227">Kategorie</span><span class="sxs-lookup"><span data-stu-id="6c164-227">Category</span></span></p></th>
<th><p><span data-ttu-id="6c164-228">Projekt</span><span class="sxs-lookup"><span data-stu-id="6c164-228">Project</span></span></p></th>
<th><p><span data-ttu-id="6c164-229">Dauerauftrag</span><span class="sxs-lookup"><span data-stu-id="6c164-229">Subscription</span></span></p></th>
<th><p><span data-ttu-id="6c164-230">Periodencode</span><span class="sxs-lookup"><span data-stu-id="6c164-230">Period code</span></span></p></th>
<th><p><span data-ttu-id="6c164-231">Währung</span><span class="sxs-lookup"><span data-stu-id="6c164-231">Currency</span></span></p></th>
<th><p><span data-ttu-id="6c164-232">Verkaufspreis</span><span class="sxs-lookup"><span data-stu-id="6c164-232">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c164-233">28.08.2007</span><span class="sxs-lookup"><span data-stu-id="6c164-233">28-08-2007</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6c164-234">9030</span><span class="sxs-lookup"><span data-stu-id="6c164-234">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6c164-235">Monat</span><span class="sxs-lookup"><span data-stu-id="6c164-235">Month</span></span></p></td>
<td><p><span data-ttu-id="6c164-236">EUR</span><span class="sxs-lookup"><span data-stu-id="6c164-236">EUR</span></span></p></td>
<td><p><span data-ttu-id="6c164-237">500</span><span class="sxs-lookup"><span data-stu-id="6c164-237">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c164-238">28.08.2007</span><span class="sxs-lookup"><span data-stu-id="6c164-238">28-08-2007</span></span></p></td>
<td><p><span data-ttu-id="6c164-239">UnterKat1</span><span class="sxs-lookup"><span data-stu-id="6c164-239">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="6c164-240">9030</span><span class="sxs-lookup"><span data-stu-id="6c164-240">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6c164-241">Monat</span><span class="sxs-lookup"><span data-stu-id="6c164-241">Month</span></span></p></td>
<td><p><span data-ttu-id="6c164-242">EUR</span><span class="sxs-lookup"><span data-stu-id="6c164-242">EUR</span></span></p></td>
<td><p><span data-ttu-id="6c164-243">550</span><span class="sxs-lookup"><span data-stu-id="6c164-243">550</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6c164-244">Sie wiederholen das oben beschriebene Verfahren und erstellen Dauerauftragsgebühren für beide Daueraufträge der Dauerauftragsgruppe "Unter1".</span><span class="sxs-lookup"><span data-stu-id="6c164-244">You repeat the procedure described above to create subscription fees for both subscriptions in the subscription group Sub1.</span></span> <span data-ttu-id="6c164-245">In der folgenden Tabelle sind die Buchungen aufgeführt, die für die einzelnen Daueraufträge erstellt werden, die der Dauerauftragsgruppe zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="6c164-245">The following table shows the transactions that are created for each subscription that is attached to the subscription group.</span></span>

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
<th><p><span data-ttu-id="6c164-246">Projektdatum</span><span class="sxs-lookup"><span data-stu-id="6c164-246">Project date</span></span></p></th>
<th><p><span data-ttu-id="6c164-247">Dauerauftrag</span><span class="sxs-lookup"><span data-stu-id="6c164-247">Subscription</span></span></p></th>
<th><p><span data-ttu-id="6c164-248">Projekt</span><span class="sxs-lookup"><span data-stu-id="6c164-248">Project</span></span></p></th>
<th><p><span data-ttu-id="6c164-249">Kategorie</span><span class="sxs-lookup"><span data-stu-id="6c164-249">Category</span></span></p></th>
<th><p><span data-ttu-id="6c164-250">Startdatum</span><span class="sxs-lookup"><span data-stu-id="6c164-250">Start date</span></span></p></th>
<th><p><span data-ttu-id="6c164-251">Enddatum</span><span class="sxs-lookup"><span data-stu-id="6c164-251">End date</span></span></p></th>
<th><p><span data-ttu-id="6c164-252">Verkaufswährung</span><span class="sxs-lookup"><span data-stu-id="6c164-252">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="6c164-253">Verkaufspreis</span><span class="sxs-lookup"><span data-stu-id="6c164-253">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c164-254">28.07.2007</span><span class="sxs-lookup"><span data-stu-id="6c164-254">28-07-2007</span></span></p></td>
<td><p><span data-ttu-id="6c164-255">00020_135</span><span class="sxs-lookup"><span data-stu-id="6c164-255">00020_135</span></span></p></td>
<td><p><span data-ttu-id="6c164-256">9030</span><span class="sxs-lookup"><span data-stu-id="6c164-256">9030</span></span></p></td>
<td><p><span data-ttu-id="6c164-257">UnterKat1</span><span class="sxs-lookup"><span data-stu-id="6c164-257">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="6c164-258">01.01.2008</span><span class="sxs-lookup"><span data-stu-id="6c164-258">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="6c164-259">31.03.2008</span><span class="sxs-lookup"><span data-stu-id="6c164-259">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="6c164-260">EUR</span><span class="sxs-lookup"><span data-stu-id="6c164-260">EUR</span></span></p></td>
<td><p><span data-ttu-id="6c164-261">550</span><span class="sxs-lookup"><span data-stu-id="6c164-261">550</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c164-262">28.07.2008</span><span class="sxs-lookup"><span data-stu-id="6c164-262">28-07-2008</span></span></p></td>
<td><p><span data-ttu-id="6c164-263">00021_135</span><span class="sxs-lookup"><span data-stu-id="6c164-263">00021_135</span></span></p></td>
<td><p><span data-ttu-id="6c164-264">9030</span><span class="sxs-lookup"><span data-stu-id="6c164-264">9030</span></span></p></td>
<td><p><span data-ttu-id="6c164-265">UnterKat2</span><span class="sxs-lookup"><span data-stu-id="6c164-265">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="6c164-266">01.01.2008</span><span class="sxs-lookup"><span data-stu-id="6c164-266">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="6c164-267">31.03.2008</span><span class="sxs-lookup"><span data-stu-id="6c164-267">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="6c164-268">EUR</span><span class="sxs-lookup"><span data-stu-id="6c164-268">EUR</span></span></p></td>
<td><p><span data-ttu-id="6c164-269">500</span><span class="sxs-lookup"><span data-stu-id="6c164-269">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6c164-270">In der ersten Buchung für den Dauerauftrag 00020\_135 wird der Verkaufspreis in Höhe von EUR 550 von dem Dauerauftragsverkaufspreis abgeleitet, der für die Kombination aus diesem speziellen Projekt und der Kategorie festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="6c164-270">In the first transaction for subscription 00020\_135, the sales price of EUR 550 derives from the subscription sales price that is set up for the combination of the specific project and category.</span></span> <span data-ttu-id="6c164-271">In der zweiten Buchung für den Dauerauftrag 00021\_135 wird als Verkaufspreis für den Projektdauerauftrag der Betrag EUR 500 verwendet, da für die Kombination aus dem Projekt "9030" und der Kategorie "UnterKat2" kein Preis eingerichtet wurde.</span><span class="sxs-lookup"><span data-stu-id="6c164-271">In the second transaction for subscription 00021\_135, the sales price of EUR 500 is used as the project subscription sales price because there is no price set up for the combination of project 9030 and category SubCat2.</span></span>

## <a name="see-also"></a><span data-ttu-id="6c164-272">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c164-272">See also</span></span>

[<span data-ttu-id="6c164-273">Aktualisieren und Indizieren von Dauerauftrag-Verkaufspreisen</span><span class="sxs-lookup"><span data-stu-id="6c164-273">Update and index subscription sales prices</span></span>](update-and-index-subscription-sales-prices.md)

  


