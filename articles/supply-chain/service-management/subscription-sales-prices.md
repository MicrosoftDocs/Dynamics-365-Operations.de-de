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
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3985864"
---
# <a name="subscription-sales-prices"></a><span data-ttu-id="30f21-103">Dauerauftragsverkaufspreise</span><span class="sxs-lookup"><span data-stu-id="30f21-103">Subscription sales prices</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="30f21-104">Beim Erstellen eines Dauerauftrags leitet sich der Verkaufspreis von den im Formular **Verkaufspreisdauerauftrag** erstellten Verkaufspreiseinstellungen ab.</span><span class="sxs-lookup"><span data-stu-id="30f21-104">When you create a subscription, the sales price is derived from the sales price setup that was created in the **Sales price (subscription)** form.</span></span>

<span data-ttu-id="30f21-105">Im Formular **Verkaufspreisdauerauftrag** können sowohl Verkaufspreise für einen bestimmten Dauerauftrag als auch Verkaufspreise erstellt werden, die eine flexiblere Anwendung ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="30f21-105">In the **Sales price (subscription)** form, you can create sales prices for a specific subscription or you can create sales prices that apply more broadly.</span></span> <span data-ttu-id="30f21-106">Damit ein Verkaufspreis auf einen Dauerauftrag angewendet werden kann, müssen der Periodencode sowie die Währung des Dauerauftrags mit dem Periodencode und der Währung des Verkaufspreises identisch sein.</span><span class="sxs-lookup"><span data-stu-id="30f21-106">For a sales price to be applied to a subscription, the period code and the currency of the subscription must be identical to the period code and the currency of the sales price.</span></span>

<span data-ttu-id="30f21-107">Bei identischem Periodencode und identischer Währung für Dauerauftrag und Verkaufspreis werden die Verkaufspreise des Dauerauftrags auf Basis der in der folgenden Tabelle aufgeführten Prioritäten ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="30f21-107">If the period code and currency are identical for the subscription and the sales price, subscription sales prices are selected on the basis of the priorities listed in the following table.</span></span> <span data-ttu-id="30f21-108">Ein leeres Feld wird in der Tabelle durch eine leere Zelle dargestellt, und ein "X" steht für einen Wert, der dem Wert im Dauerauftragsformular entspricht, in dem die Buchung generiert wird.</span><span class="sxs-lookup"><span data-stu-id="30f21-108">A blank cell in the table indicates an empty field and an X indicates a value that is equal to the value in the subscription from which the transaction is generated.</span></span>

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
<th><p><span data-ttu-id="30f21-109">Priorität </span><span class="sxs-lookup"><span data-stu-id="30f21-109">Priority</span></span></p></th>
<th><p><span data-ttu-id="30f21-110"><strong>Kategorie</strong></span><span class="sxs-lookup"><span data-stu-id="30f21-110"><strong>Category</strong></span></span></p></th>
<th><p><span data-ttu-id="30f21-111"><strong>Projektkennung</strong></span><span class="sxs-lookup"><span data-stu-id="30f21-111"><strong>Project ID</strong></span></span></p></th>
<th><p><span data-ttu-id="30f21-112"><strong>Dauerauftrag</strong></span><span class="sxs-lookup"><span data-stu-id="30f21-112"><strong>Subscription</strong></span></span></p></th>
<th><p><span data-ttu-id="30f21-113"><strong>Verkaufswährung</strong></span><span class="sxs-lookup"><span data-stu-id="30f21-113"><strong>Sales currency</strong></span></span></p></th>
<th><p><span data-ttu-id="30f21-114"><strong>Periodencode</strong></span><span class="sxs-lookup"><span data-stu-id="30f21-114"><strong>Period code</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="30f21-115">1</span><span class="sxs-lookup"><span data-stu-id="30f21-115">1</span></span></p></td>
<td><p><span data-ttu-id="30f21-116">X</span><span class="sxs-lookup"><span data-stu-id="30f21-116">X</span></span></p></td>
<td><p><span data-ttu-id="30f21-117">X</span><span class="sxs-lookup"><span data-stu-id="30f21-117">X</span></span></p></td>
<td><p><span data-ttu-id="30f21-118">X</span><span class="sxs-lookup"><span data-stu-id="30f21-118">X</span></span></p></td>
<td><p><span data-ttu-id="30f21-119">X</span><span class="sxs-lookup"><span data-stu-id="30f21-119">X</span></span></p></td>
<td><p><span data-ttu-id="30f21-120">X</span><span class="sxs-lookup"><span data-stu-id="30f21-120">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30f21-121">2</span><span class="sxs-lookup"><span data-stu-id="30f21-121">2</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="30f21-122">X</span><span class="sxs-lookup"><span data-stu-id="30f21-122">X</span></span></p></td>
<td><p><span data-ttu-id="30f21-123">X</span><span class="sxs-lookup"><span data-stu-id="30f21-123">X</span></span></p></td>
<td><p><span data-ttu-id="30f21-124">X</span><span class="sxs-lookup"><span data-stu-id="30f21-124">X</span></span></p></td>
<td><p><span data-ttu-id="30f21-125">X</span><span class="sxs-lookup"><span data-stu-id="30f21-125">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="30f21-126">3</span><span class="sxs-lookup"><span data-stu-id="30f21-126">3</span></span></p></td>
<td><p><span data-ttu-id="30f21-127">X</span><span class="sxs-lookup"><span data-stu-id="30f21-127">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="30f21-128">X</span><span class="sxs-lookup"><span data-stu-id="30f21-128">X</span></span></p></td>
<td><p><span data-ttu-id="30f21-129">X</span><span class="sxs-lookup"><span data-stu-id="30f21-129">X</span></span></p></td>
<td><p><span data-ttu-id="30f21-130">X</span><span class="sxs-lookup"><span data-stu-id="30f21-130">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30f21-131">4</span><span class="sxs-lookup"><span data-stu-id="30f21-131">4</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="30f21-132">X</span><span class="sxs-lookup"><span data-stu-id="30f21-132">X</span></span></p></td>
<td><p><span data-ttu-id="30f21-133">X</span><span class="sxs-lookup"><span data-stu-id="30f21-133">X</span></span></p></td>
<td><p><span data-ttu-id="30f21-134">X</span><span class="sxs-lookup"><span data-stu-id="30f21-134">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="30f21-135">5</span><span class="sxs-lookup"><span data-stu-id="30f21-135">5</span></span></p></td>
<td><p><span data-ttu-id="30f21-136">X</span><span class="sxs-lookup"><span data-stu-id="30f21-136">X</span></span></p></td>
<td><p><span data-ttu-id="30f21-137">X</span><span class="sxs-lookup"><span data-stu-id="30f21-137">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="30f21-138">X</span><span class="sxs-lookup"><span data-stu-id="30f21-138">X</span></span></p></td>
<td><p><span data-ttu-id="30f21-139">X</span><span class="sxs-lookup"><span data-stu-id="30f21-139">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30f21-140">6</span><span class="sxs-lookup"><span data-stu-id="30f21-140">6</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="30f21-141">X</span><span class="sxs-lookup"><span data-stu-id="30f21-141">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="30f21-142">X</span><span class="sxs-lookup"><span data-stu-id="30f21-142">X</span></span></p></td>
<td><p><span data-ttu-id="30f21-143">X</span><span class="sxs-lookup"><span data-stu-id="30f21-143">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="30f21-144">7</span><span class="sxs-lookup"><span data-stu-id="30f21-144">7</span></span></p></td>
<td><p><span data-ttu-id="30f21-145">X</span><span class="sxs-lookup"><span data-stu-id="30f21-145">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="30f21-146">X</span><span class="sxs-lookup"><span data-stu-id="30f21-146">X</span></span></p></td>
<td><p><span data-ttu-id="30f21-147">X</span><span class="sxs-lookup"><span data-stu-id="30f21-147">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30f21-148">8</span><span class="sxs-lookup"><span data-stu-id="30f21-148">8</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="30f21-149">X</span><span class="sxs-lookup"><span data-stu-id="30f21-149">X</span></span></p></td>
<td><p><span data-ttu-id="30f21-150">X</span><span class="sxs-lookup"><span data-stu-id="30f21-150">X</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="30f21-151">Beim Erstellen einer Dauerauftragsgebühr wird der Verkaufspreis mit der höchsten Genauigkeit (gemäß obiger Tabelle) als Verkaufspreis für den Dauerauftrag ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="30f21-151">When a subscription fee is created, the sales price with the greatest level of detail, as noted in the table above, is selected as the subscription sales price.</span></span>

## <a name="update-and-index-subscription-sales-prices"></a><span data-ttu-id="30f21-152">Aktualisieren und Indizieren von Dauerauftragsverkaufspreisen</span><span class="sxs-lookup"><span data-stu-id="30f21-152">Update and index subscription sales prices</span></span>

<span data-ttu-id="30f21-153">Aktualisieren Sie zum Aktualisieren des Verkaufspreises für den Dauerauftrag den Basispreis oder den Index.</span><span class="sxs-lookup"><span data-stu-id="30f21-153">You can update the subscription sales price by updating the base price or the index.</span></span> <span data-ttu-id="30f21-154">Die Aktualisierung kann prozentual oder durch Angabe eines neues Werts vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="30f21-154">You can update by a percentage or to a new value.</span></span>

## <a name="subscription-fee-sales-prices"></a><span data-ttu-id="30f21-155">Verkaufspreise für Dauerauftragsgebühren</span><span class="sxs-lookup"><span data-stu-id="30f21-155">Subscription fee sales prices</span></span>

<span data-ttu-id="30f21-156">Beim Erstellen einer Dauerauftragsgebühr basiert der Verkaufspreis auf den Verkaufspreiseinstellungen des Dauerauftrags.</span><span class="sxs-lookup"><span data-stu-id="30f21-156">When you create a subscription fee, the sales price is based on the sales price setup of the subscription.</span></span> <span data-ttu-id="30f21-157">Sie können entweder den Basispreis aus den Preiseinstellungen des Dauerauftrags verwenden oder indizierte Verkaufspreise erstellen.</span><span class="sxs-lookup"><span data-stu-id="30f21-157">You can either use the base price from the subscription price setup or create indexed sales prices.</span></span>

## <a name="example"></a><span data-ttu-id="30f21-158">Beispiel</span><span class="sxs-lookup"><span data-stu-id="30f21-158">Example</span></span>

<span data-ttu-id="30f21-159">Sie möchten für das neue Projekt "9030" Dauerauftragsverkaufspreise in Höhe von EUR 500 einrichten.</span><span class="sxs-lookup"><span data-stu-id="30f21-159">You want to set up subscription sales prices of EUR 500 for a new project 9030.</span></span> <span data-ttu-id="30f21-160">Im Formular **Verkaufspreisdauerauftrag** erstellen Sie eine Verkaufspreisposition für den Dauerauftrag, wie dies in der folgenden Tabelle angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="30f21-160">In the **Sales price (subscription)** form, you create a subscription sales price line as indicated in the following table.</span></span>

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
<th><p><span data-ttu-id="30f21-161">Gültig ab</span><span class="sxs-lookup"><span data-stu-id="30f21-161">Valid from</span></span></p></th>
<th><p><span data-ttu-id="30f21-162">Kategorie</span><span class="sxs-lookup"><span data-stu-id="30f21-162">Category</span></span></p></th>
<th><p><span data-ttu-id="30f21-163">Projekt</span><span class="sxs-lookup"><span data-stu-id="30f21-163">Project</span></span></p></th>
<th><p><span data-ttu-id="30f21-164">Dauerauftrag</span><span class="sxs-lookup"><span data-stu-id="30f21-164">Subscription</span></span></p></th>
<th><p><span data-ttu-id="30f21-165">Periodencode</span><span class="sxs-lookup"><span data-stu-id="30f21-165">Period code</span></span></p></th>
<th><p><span data-ttu-id="30f21-166">Verkaufswährung</span><span class="sxs-lookup"><span data-stu-id="30f21-166">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="30f21-167">Verkaufspreis</span><span class="sxs-lookup"><span data-stu-id="30f21-167">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="30f21-168">28.08.2006</span><span class="sxs-lookup"><span data-stu-id="30f21-168">28-08-2006</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="30f21-169">9030</span><span class="sxs-lookup"><span data-stu-id="30f21-169">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="30f21-170">Monat</span><span class="sxs-lookup"><span data-stu-id="30f21-170">Month</span></span></p></td>
<td><p><span data-ttu-id="30f21-171">EUR</span><span class="sxs-lookup"><span data-stu-id="30f21-171">EUR</span></span></p></td>
<td><p><span data-ttu-id="30f21-172">500</span><span class="sxs-lookup"><span data-stu-id="30f21-172">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="30f21-173">Beachten Sie, dass die Felder **Kategorie** und **Dauerauftrag** leer sind.</span><span class="sxs-lookup"><span data-stu-id="30f21-173">Note that the **Category** and **Subscription** fields are empty.</span></span>

<span data-ttu-id="30f21-174">Anschließend werden die folgenden Daueraufträge erstellt.</span><span class="sxs-lookup"><span data-stu-id="30f21-174">You then create the following subscriptions.</span></span>

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
<th><p><span data-ttu-id="30f21-175">Servicedauerauftrag</span><span class="sxs-lookup"><span data-stu-id="30f21-175">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="30f21-176">Projekt</span><span class="sxs-lookup"><span data-stu-id="30f21-176">Project</span></span></p></th>
<th><p><span data-ttu-id="30f21-177">Dauerauftragsgruppe</span><span class="sxs-lookup"><span data-stu-id="30f21-177">Subscription group</span></span></p></th>
<th><p><span data-ttu-id="30f21-178">Kategorie</span><span class="sxs-lookup"><span data-stu-id="30f21-178">Category</span></span></p></th>
<th><p><span data-ttu-id="30f21-179">Währung</span><span class="sxs-lookup"><span data-stu-id="30f21-179">Currency</span></span></p></th>
<th><p><span data-ttu-id="30f21-180">Periodencode</span><span class="sxs-lookup"><span data-stu-id="30f21-180">Period code</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="30f21-181">00020_135</span><span class="sxs-lookup"><span data-stu-id="30f21-181">00020_135</span></span></p></td>
<td><p><span data-ttu-id="30f21-182">9030</span><span class="sxs-lookup"><span data-stu-id="30f21-182">9030</span></span></p></td>
<td><p><span data-ttu-id="30f21-183">Unter1</span><span class="sxs-lookup"><span data-stu-id="30f21-183">Sub1</span></span></p></td>
<td><p><span data-ttu-id="30f21-184">UnterKat1</span><span class="sxs-lookup"><span data-stu-id="30f21-184">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="30f21-185">EUR</span><span class="sxs-lookup"><span data-stu-id="30f21-185">EUR</span></span></p></td>
<td><p><span data-ttu-id="30f21-186">Monatlich</span><span class="sxs-lookup"><span data-stu-id="30f21-186">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30f21-187">00021_135</span><span class="sxs-lookup"><span data-stu-id="30f21-187">00021_135</span></span></p></td>
<td><p><span data-ttu-id="30f21-188">9030</span><span class="sxs-lookup"><span data-stu-id="30f21-188">9030</span></span></p></td>
<td><p><span data-ttu-id="30f21-189">Unter1</span><span class="sxs-lookup"><span data-stu-id="30f21-189">Sub1</span></span></p></td>
<td><p><span data-ttu-id="30f21-190">UnterKat2</span><span class="sxs-lookup"><span data-stu-id="30f21-190">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="30f21-191">EUR</span><span class="sxs-lookup"><span data-stu-id="30f21-191">EUR</span></span></p></td>
<td><p><span data-ttu-id="30f21-192">Monatlich</span><span class="sxs-lookup"><span data-stu-id="30f21-192">Monthly</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="30f21-193">Im nächsten Schritt werden die Dauerauftragsgebühren für die beiden Daueraufträge der Gruppe "Unter1" erstellt:</span><span class="sxs-lookup"><span data-stu-id="30f21-193">Now you create subscription fees for both subscriptions in the subscription group Sub1:</span></span>

1.  <span data-ttu-id="30f21-194">Klicken Sie auf **Servicemanagement** \> **Einrichtung** \> **Daueraufträge** \> **Dauerauftragsgruppen**.</span><span class="sxs-lookup"><span data-stu-id="30f21-194">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

2.  <span data-ttu-id="30f21-195">In der **Dauerauftragsgruppen** im Formular und klicken im Formular **Funktion** \> **Dauerauftragsgebühr erstellen**.</span><span class="sxs-lookup"><span data-stu-id="30f21-195">In the **Subscription groups** form, click **Function** \> **Create subscription fee**.</span></span>

3.  <span data-ttu-id="30f21-196">In der **Dauerauftragsgebühr erstellen** Formular geben Sie die entsprechenden Informationen ein.</span><span class="sxs-lookup"><span data-stu-id="30f21-196">In the **Create subscription fee** form, enter the appropriate information.</span></span> <span data-ttu-id="30f21-197">Weitere Informationen finden Sie unter [Dauerauftragsgebühren-Buchungen erstellen](create-subscription-fee-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="30f21-197">For more information, see [Create subscription fee transactions](create-subscription-fee-transactions.md).</span></span>

<span data-ttu-id="30f21-198">Für beide Daueraufträge werden Dauerauftragsgebühren mit einem Verkaufspreis von EUR 500 erstellt. Dies ist in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="30f21-198">Subscription fees that have a sales price of EUR 500 are created for both subscriptions, as shown in the following table.</span></span>

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
<th><p><span data-ttu-id="30f21-199">Projektdatum</span><span class="sxs-lookup"><span data-stu-id="30f21-199">Project date</span></span></p></th>
<th><p><span data-ttu-id="30f21-200">Servicedauerauftrag</span><span class="sxs-lookup"><span data-stu-id="30f21-200">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="30f21-201">Projekt</span><span class="sxs-lookup"><span data-stu-id="30f21-201">Project</span></span></p></th>
<th><p><span data-ttu-id="30f21-202">Kategorie</span><span class="sxs-lookup"><span data-stu-id="30f21-202">Category</span></span></p></th>
<th><p><span data-ttu-id="30f21-203">Startdatum</span><span class="sxs-lookup"><span data-stu-id="30f21-203">Start date</span></span></p></th>
<th><p><span data-ttu-id="30f21-204">Enddatum</span><span class="sxs-lookup"><span data-stu-id="30f21-204">End date</span></span></p></th>
<th><p><span data-ttu-id="30f21-205">Verkaufswährung</span><span class="sxs-lookup"><span data-stu-id="30f21-205">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="30f21-206">Verkaufspreis</span><span class="sxs-lookup"><span data-stu-id="30f21-206">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="30f21-207">28.08.2006</span><span class="sxs-lookup"><span data-stu-id="30f21-207">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="30f21-208">00020_135</span><span class="sxs-lookup"><span data-stu-id="30f21-208">00020_135</span></span></p></td>
<td><p><span data-ttu-id="30f21-209">9030</span><span class="sxs-lookup"><span data-stu-id="30f21-209">9030</span></span></p></td>
<td><p><span data-ttu-id="30f21-210">UnterKat1</span><span class="sxs-lookup"><span data-stu-id="30f21-210">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="30f21-211">01.01.2007</span><span class="sxs-lookup"><span data-stu-id="30f21-211">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="30f21-212">31.03.2007</span><span class="sxs-lookup"><span data-stu-id="30f21-212">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="30f21-213">EUR</span><span class="sxs-lookup"><span data-stu-id="30f21-213">EUR</span></span></p></td>
<td><p><span data-ttu-id="30f21-214">500</span><span class="sxs-lookup"><span data-stu-id="30f21-214">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30f21-215">28.08.2006</span><span class="sxs-lookup"><span data-stu-id="30f21-215">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="30f21-216">00021_135</span><span class="sxs-lookup"><span data-stu-id="30f21-216">00021_135</span></span></p></td>
<td><p><span data-ttu-id="30f21-217">9030</span><span class="sxs-lookup"><span data-stu-id="30f21-217">9030</span></span></p></td>
<td><p><span data-ttu-id="30f21-218">UnterKat2</span><span class="sxs-lookup"><span data-stu-id="30f21-218">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="30f21-219">01.01.2007</span><span class="sxs-lookup"><span data-stu-id="30f21-219">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="30f21-220">31.03.2007</span><span class="sxs-lookup"><span data-stu-id="30f21-220">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="30f21-221">EUR</span><span class="sxs-lookup"><span data-stu-id="30f21-221">EUR</span></span></p></td>
<td><p><span data-ttu-id="30f21-222">500</span><span class="sxs-lookup"><span data-stu-id="30f21-222">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="30f21-223">Später entschließen Sie sich zum Angeben von Verkaufspreisen für die Kategorie "UnterKat1" des Projekts "9030".</span><span class="sxs-lookup"><span data-stu-id="30f21-223">Later, you decide that you want to specify sales prices for the category SubCat1 for project 9030.</span></span> <span data-ttu-id="30f21-224">Zu diesem Zweck erstellen Sie für die Kombination aus Projekt "9030" und Gebührenkategorie "UnterKat1" eine neue Verkaufspreisposition mit einem Verkaufspreis von EUR 550.</span><span class="sxs-lookup"><span data-stu-id="30f21-224">Therefore, you create a new sales price line that has a sales price of EUR 550 for the combination of project 9030 and fee category SubCat1.</span></span> <span data-ttu-id="30f21-225">Für das Projekt "9030" sind nun zwei Verkaufspreispositionen für Daueraufträge vorhanden. Dies ist in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="30f21-225">There are now two subscription sales price lines for project 9030, as shown in the following table.</span></span>

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
<th><p><span data-ttu-id="30f21-226">Gültig ab</span><span class="sxs-lookup"><span data-stu-id="30f21-226">Valid from</span></span></p></th>
<th><p><span data-ttu-id="30f21-227">Kategorie</span><span class="sxs-lookup"><span data-stu-id="30f21-227">Category</span></span></p></th>
<th><p><span data-ttu-id="30f21-228">Projekt</span><span class="sxs-lookup"><span data-stu-id="30f21-228">Project</span></span></p></th>
<th><p><span data-ttu-id="30f21-229">Dauerauftrag</span><span class="sxs-lookup"><span data-stu-id="30f21-229">Subscription</span></span></p></th>
<th><p><span data-ttu-id="30f21-230">Periodencode</span><span class="sxs-lookup"><span data-stu-id="30f21-230">Period code</span></span></p></th>
<th><p><span data-ttu-id="30f21-231">Währung</span><span class="sxs-lookup"><span data-stu-id="30f21-231">Currency</span></span></p></th>
<th><p><span data-ttu-id="30f21-232">Verkaufspreis</span><span class="sxs-lookup"><span data-stu-id="30f21-232">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="30f21-233">28.08.2007</span><span class="sxs-lookup"><span data-stu-id="30f21-233">28-08-2007</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="30f21-234">9030</span><span class="sxs-lookup"><span data-stu-id="30f21-234">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="30f21-235">Monat</span><span class="sxs-lookup"><span data-stu-id="30f21-235">Month</span></span></p></td>
<td><p><span data-ttu-id="30f21-236">EUR</span><span class="sxs-lookup"><span data-stu-id="30f21-236">EUR</span></span></p></td>
<td><p><span data-ttu-id="30f21-237">500</span><span class="sxs-lookup"><span data-stu-id="30f21-237">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30f21-238">28.08.2007</span><span class="sxs-lookup"><span data-stu-id="30f21-238">28-08-2007</span></span></p></td>
<td><p><span data-ttu-id="30f21-239">UnterKat1</span><span class="sxs-lookup"><span data-stu-id="30f21-239">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="30f21-240">9030</span><span class="sxs-lookup"><span data-stu-id="30f21-240">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="30f21-241">Monat</span><span class="sxs-lookup"><span data-stu-id="30f21-241">Month</span></span></p></td>
<td><p><span data-ttu-id="30f21-242">EUR</span><span class="sxs-lookup"><span data-stu-id="30f21-242">EUR</span></span></p></td>
<td><p><span data-ttu-id="30f21-243">550</span><span class="sxs-lookup"><span data-stu-id="30f21-243">550</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="30f21-244">Sie wiederholen das oben beschriebene Verfahren und erstellen Dauerauftragsgebühren für beide Daueraufträge der Dauerauftragsgruppe "Unter1".</span><span class="sxs-lookup"><span data-stu-id="30f21-244">You repeat the procedure described above to create subscription fees for both subscriptions in the subscription group Sub1.</span></span> <span data-ttu-id="30f21-245">In der folgenden Tabelle sind die Buchungen aufgeführt, die für die einzelnen Daueraufträge erstellt werden, die der Dauerauftragsgruppe zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="30f21-245">The following table shows the transactions that are created for each subscription that is attached to the subscription group.</span></span>

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
<th><p><span data-ttu-id="30f21-246">Projektdatum</span><span class="sxs-lookup"><span data-stu-id="30f21-246">Project date</span></span></p></th>
<th><p><span data-ttu-id="30f21-247">Dauerauftrag</span><span class="sxs-lookup"><span data-stu-id="30f21-247">Subscription</span></span></p></th>
<th><p><span data-ttu-id="30f21-248">Projekt</span><span class="sxs-lookup"><span data-stu-id="30f21-248">Project</span></span></p></th>
<th><p><span data-ttu-id="30f21-249">Kategorie</span><span class="sxs-lookup"><span data-stu-id="30f21-249">Category</span></span></p></th>
<th><p><span data-ttu-id="30f21-250">Startdatum</span><span class="sxs-lookup"><span data-stu-id="30f21-250">Start date</span></span></p></th>
<th><p><span data-ttu-id="30f21-251">Enddatum</span><span class="sxs-lookup"><span data-stu-id="30f21-251">End date</span></span></p></th>
<th><p><span data-ttu-id="30f21-252">Verkaufswährung</span><span class="sxs-lookup"><span data-stu-id="30f21-252">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="30f21-253">Verkaufspreis</span><span class="sxs-lookup"><span data-stu-id="30f21-253">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="30f21-254">28.07.2007</span><span class="sxs-lookup"><span data-stu-id="30f21-254">28-07-2007</span></span></p></td>
<td><p><span data-ttu-id="30f21-255">00020_135</span><span class="sxs-lookup"><span data-stu-id="30f21-255">00020_135</span></span></p></td>
<td><p><span data-ttu-id="30f21-256">9030</span><span class="sxs-lookup"><span data-stu-id="30f21-256">9030</span></span></p></td>
<td><p><span data-ttu-id="30f21-257">UnterKat1</span><span class="sxs-lookup"><span data-stu-id="30f21-257">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="30f21-258">01.01.2008</span><span class="sxs-lookup"><span data-stu-id="30f21-258">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="30f21-259">31.03.2008</span><span class="sxs-lookup"><span data-stu-id="30f21-259">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="30f21-260">EUR</span><span class="sxs-lookup"><span data-stu-id="30f21-260">EUR</span></span></p></td>
<td><p><span data-ttu-id="30f21-261">550</span><span class="sxs-lookup"><span data-stu-id="30f21-261">550</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30f21-262">28.07.2008</span><span class="sxs-lookup"><span data-stu-id="30f21-262">28-07-2008</span></span></p></td>
<td><p><span data-ttu-id="30f21-263">00021_135</span><span class="sxs-lookup"><span data-stu-id="30f21-263">00021_135</span></span></p></td>
<td><p><span data-ttu-id="30f21-264">9030</span><span class="sxs-lookup"><span data-stu-id="30f21-264">9030</span></span></p></td>
<td><p><span data-ttu-id="30f21-265">UnterKat2</span><span class="sxs-lookup"><span data-stu-id="30f21-265">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="30f21-266">01.01.2008</span><span class="sxs-lookup"><span data-stu-id="30f21-266">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="30f21-267">31.03.2008</span><span class="sxs-lookup"><span data-stu-id="30f21-267">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="30f21-268">EUR</span><span class="sxs-lookup"><span data-stu-id="30f21-268">EUR</span></span></p></td>
<td><p><span data-ttu-id="30f21-269">500</span><span class="sxs-lookup"><span data-stu-id="30f21-269">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="30f21-270">In der ersten Buchung für den Dauerauftrag 00020\_135 wird der Verkaufspreis in Höhe von EUR 550 von dem Dauerauftragsverkaufspreis abgeleitet, der für die Kombination aus diesem speziellen Projekt und der Kategorie festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="30f21-270">In the first transaction for subscription 00020\_135, the sales price of EUR 550 derives from the subscription sales price that is set up for the combination of the specific project and category.</span></span> <span data-ttu-id="30f21-271">In der zweiten Buchung für den Dauerauftrag 00021\_135 wird als Verkaufspreis für den Projektdauerauftrag der Betrag EUR 500 verwendet, da für die Kombination aus dem Projekt "9030" und der Kategorie "UnterKat2" kein Preis eingerichtet wurde.</span><span class="sxs-lookup"><span data-stu-id="30f21-271">In the second transaction for subscription 00021\_135, the sales price of EUR 500 is used as the project subscription sales price because there is no price set up for the combination of project 9030 and category SubCat2.</span></span>

## <a name="see-also"></a><span data-ttu-id="30f21-272">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30f21-272">See also</span></span>

[<span data-ttu-id="30f21-273">Aktualisieren und Indizieren von Dauerauftrag-Verkaufspreisen</span><span class="sxs-lookup"><span data-stu-id="30f21-273">Update and index subscription sales prices</span></span>](update-and-index-subscription-sales-prices.md)

  


