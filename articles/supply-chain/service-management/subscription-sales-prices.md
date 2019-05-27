---
title: Dauerauftragsverkaufspreise
description: Beim Erstellen eines Dauerauftrags leitet sich der Verkaufspreis von den im Formular Verkaufspreisdauerauftrag erstellten Verkaufspreiseinstellungen ab.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASalespriceSubscription
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5e18690f7e9b790ecbd0ac0de1955fc95ab1f082
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560688"
---
# <a name="subscription-sales-prices"></a><span data-ttu-id="17752-103">Dauerauftragsverkaufspreise</span><span class="sxs-lookup"><span data-stu-id="17752-103">Subscription sales prices</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="17752-104">Beim Erstellen eines Dauerauftrags leitet sich der Verkaufspreis von den im Formular **Verkaufspreisdauerauftrag** erstellten Verkaufspreiseinstellungen ab.</span><span class="sxs-lookup"><span data-stu-id="17752-104">When you create a subscription, the sales price is derived from the sales price setup that was created in the **Sales price (subscription)** form.</span></span>

<span data-ttu-id="17752-105">Im Formular **Verkaufspreisdauerauftrag** können sowohl Verkaufspreise für einen bestimmten Dauerauftrag als auch Verkaufspreise erstellt werden, die eine flexiblere Anwendung ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="17752-105">In the **Sales price (subscription)** form, you can create sales prices for a specific subscription or you can create sales prices that apply more broadly.</span></span> <span data-ttu-id="17752-106">Damit ein Verkaufspreis auf einen Dauerauftrag angewendet werden kann, müssen der Periodencode sowie die Währung des Dauerauftrags mit dem Periodencode und der Währung des Verkaufspreises identisch sein.</span><span class="sxs-lookup"><span data-stu-id="17752-106">For a sales price to be applied to a subscription, the period code and the currency of the subscription must be identical to the period code and the currency of the sales price.</span></span>

<span data-ttu-id="17752-107">Bei identischem Periodencode und identischer Währung für Dauerauftrag und Verkaufspreis werden die Verkaufspreise des Dauerauftrags auf Basis der in der folgenden Tabelle aufgeführten Prioritäten ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="17752-107">If the period code and currency are identical for the subscription and the sales price, subscription sales prices are selected on the basis of the priorities listed in the following table.</span></span> <span data-ttu-id="17752-108">Ein leeres Feld wird in der Tabelle durch eine leere Zelle dargestellt, und ein "X" steht für einen Wert, der dem Wert im Dauerauftragsformular entspricht, in dem die Buchung generiert wird.</span><span class="sxs-lookup"><span data-stu-id="17752-108">A blank cell in the table indicates an empty field and an X indicates a value that is equal to the value in the subscription from which the transaction is generated.</span></span>

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
<th><p><span data-ttu-id="17752-109">Priorität </span><span class="sxs-lookup"><span data-stu-id="17752-109">Priority</span></span></p></th>
<th><p><span data-ttu-id="17752-110"><strong>Kategorie</strong></span><span class="sxs-lookup"><span data-stu-id="17752-110"><strong>Category</strong></span></span></p></th>
<th><p><span data-ttu-id="17752-111"><strong>Projektkennung</strong></span><span class="sxs-lookup"><span data-stu-id="17752-111"><strong>Project ID</strong></span></span></p></th>
<th><p><span data-ttu-id="17752-112"><strong>Dauerauftrag</strong></span><span class="sxs-lookup"><span data-stu-id="17752-112"><strong>Subscription</strong></span></span></p></th>
<th><p><span data-ttu-id="17752-113"><strong>Verkaufswährung</strong></span><span class="sxs-lookup"><span data-stu-id="17752-113"><strong>Sales currency</strong></span></span></p></th>
<th><p><span data-ttu-id="17752-114"><strong>Periodencode</strong></span><span class="sxs-lookup"><span data-stu-id="17752-114"><strong>Period code</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="17752-115">1</span><span class="sxs-lookup"><span data-stu-id="17752-115">1</span></span></p></td>
<td><p><span data-ttu-id="17752-116">X</span><span class="sxs-lookup"><span data-stu-id="17752-116">X</span></span></p></td>
<td><p><span data-ttu-id="17752-117">X</span><span class="sxs-lookup"><span data-stu-id="17752-117">X</span></span></p></td>
<td><p><span data-ttu-id="17752-118">X</span><span class="sxs-lookup"><span data-stu-id="17752-118">X</span></span></p></td>
<td><p><span data-ttu-id="17752-119">X</span><span class="sxs-lookup"><span data-stu-id="17752-119">X</span></span></p></td>
<td><p><span data-ttu-id="17752-120">X</span><span class="sxs-lookup"><span data-stu-id="17752-120">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17752-121">2</span><span class="sxs-lookup"><span data-stu-id="17752-121">2</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="17752-122">X</span><span class="sxs-lookup"><span data-stu-id="17752-122">X</span></span></p></td>
<td><p><span data-ttu-id="17752-123">X</span><span class="sxs-lookup"><span data-stu-id="17752-123">X</span></span></p></td>
<td><p><span data-ttu-id="17752-124">X</span><span class="sxs-lookup"><span data-stu-id="17752-124">X</span></span></p></td>
<td><p><span data-ttu-id="17752-125">X</span><span class="sxs-lookup"><span data-stu-id="17752-125">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17752-126">3</span><span class="sxs-lookup"><span data-stu-id="17752-126">3</span></span></p></td>
<td><p><span data-ttu-id="17752-127">X</span><span class="sxs-lookup"><span data-stu-id="17752-127">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="17752-128">X</span><span class="sxs-lookup"><span data-stu-id="17752-128">X</span></span></p></td>
<td><p><span data-ttu-id="17752-129">X</span><span class="sxs-lookup"><span data-stu-id="17752-129">X</span></span></p></td>
<td><p><span data-ttu-id="17752-130">X</span><span class="sxs-lookup"><span data-stu-id="17752-130">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17752-131">4</span><span class="sxs-lookup"><span data-stu-id="17752-131">4</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="17752-132">X</span><span class="sxs-lookup"><span data-stu-id="17752-132">X</span></span></p></td>
<td><p><span data-ttu-id="17752-133">X</span><span class="sxs-lookup"><span data-stu-id="17752-133">X</span></span></p></td>
<td><p><span data-ttu-id="17752-134">X</span><span class="sxs-lookup"><span data-stu-id="17752-134">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17752-135">5</span><span class="sxs-lookup"><span data-stu-id="17752-135">5</span></span></p></td>
<td><p><span data-ttu-id="17752-136">X</span><span class="sxs-lookup"><span data-stu-id="17752-136">X</span></span></p></td>
<td><p><span data-ttu-id="17752-137">X</span><span class="sxs-lookup"><span data-stu-id="17752-137">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="17752-138">X</span><span class="sxs-lookup"><span data-stu-id="17752-138">X</span></span></p></td>
<td><p><span data-ttu-id="17752-139">X</span><span class="sxs-lookup"><span data-stu-id="17752-139">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17752-140">6</span><span class="sxs-lookup"><span data-stu-id="17752-140">6</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="17752-141">X</span><span class="sxs-lookup"><span data-stu-id="17752-141">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="17752-142">X</span><span class="sxs-lookup"><span data-stu-id="17752-142">X</span></span></p></td>
<td><p><span data-ttu-id="17752-143">X</span><span class="sxs-lookup"><span data-stu-id="17752-143">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17752-144">7</span><span class="sxs-lookup"><span data-stu-id="17752-144">7</span></span></p></td>
<td><p><span data-ttu-id="17752-145">X</span><span class="sxs-lookup"><span data-stu-id="17752-145">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="17752-146">X</span><span class="sxs-lookup"><span data-stu-id="17752-146">X</span></span></p></td>
<td><p><span data-ttu-id="17752-147">X</span><span class="sxs-lookup"><span data-stu-id="17752-147">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17752-148">8</span><span class="sxs-lookup"><span data-stu-id="17752-148">8</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="17752-149">X</span><span class="sxs-lookup"><span data-stu-id="17752-149">X</span></span></p></td>
<td><p><span data-ttu-id="17752-150">X</span><span class="sxs-lookup"><span data-stu-id="17752-150">X</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="17752-151">Beim Erstellen einer Dauerauftragsgebühr wird der Verkaufspreis mit der höchsten Genauigkeit (gemäß obiger Tabelle) als Verkaufspreis für den Dauerauftrag ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="17752-151">When a subscription fee is created, the sales price with the greatest level of detail, as noted in the table above, is selected as the subscription sales price.</span></span>

## <a name="update-and-index-subscription-sales-prices"></a><span data-ttu-id="17752-152">Aktualisieren und Indizieren von Dauerauftragsverkaufspreisen</span><span class="sxs-lookup"><span data-stu-id="17752-152">Update and index subscription sales prices</span></span>

<span data-ttu-id="17752-153">Aktualisieren Sie zum Aktualisieren des Verkaufspreises für den Dauerauftrag den Basispreis oder den Index.</span><span class="sxs-lookup"><span data-stu-id="17752-153">You can update the subscription sales price by updating the base price or the index.</span></span> <span data-ttu-id="17752-154">Die Aktualisierung kann prozentual oder durch Angabe eines neues Werts vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="17752-154">You can update by a percentage or to a new value.</span></span>

## <a name="subscription-fee-sales-prices"></a><span data-ttu-id="17752-155">Verkaufspreise für Dauerauftragsgebühren</span><span class="sxs-lookup"><span data-stu-id="17752-155">Subscription fee sales prices</span></span>

<span data-ttu-id="17752-156">Beim Erstellen einer Dauerauftragsgebühr basiert der Verkaufspreis auf den Verkaufspreiseinstellungen des Dauerauftrags.</span><span class="sxs-lookup"><span data-stu-id="17752-156">When you create a subscription fee, the sales price is based on the sales price setup of the subscription.</span></span> <span data-ttu-id="17752-157">Sie können entweder den Basispreis aus den Preiseinstellungen des Dauerauftrags verwenden oder indizierte Verkaufspreise erstellen.</span><span class="sxs-lookup"><span data-stu-id="17752-157">You can either use the base price from the subscription price setup or create indexed sales prices.</span></span>

## <a name="example"></a><span data-ttu-id="17752-158">Beispiel</span><span class="sxs-lookup"><span data-stu-id="17752-158">Example</span></span>

<span data-ttu-id="17752-159">Sie möchten für das neue Projekt "9030" Dauerauftragsverkaufspreise in Höhe von EUR 500 einrichten.</span><span class="sxs-lookup"><span data-stu-id="17752-159">You want to set up subscription sales prices of EUR 500 for a new project 9030.</span></span> <span data-ttu-id="17752-160">Im Formular **Verkaufspreisdauerauftrag** erstellen Sie eine Verkaufspreisposition für den Dauerauftrag, wie dies in der folgenden Tabelle angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="17752-160">In the **Sales price (subscription)** form, you create a subscription sales price line as indicated in the following table.</span></span>

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
<th><p><span data-ttu-id="17752-161">Gültig ab</span><span class="sxs-lookup"><span data-stu-id="17752-161">Valid from</span></span></p></th>
<th><p><span data-ttu-id="17752-162">Kategorie</span><span class="sxs-lookup"><span data-stu-id="17752-162">Category</span></span></p></th>
<th><p><span data-ttu-id="17752-163">Projekt</span><span class="sxs-lookup"><span data-stu-id="17752-163">Project</span></span></p></th>
<th><p><span data-ttu-id="17752-164">Dauerauftrag</span><span class="sxs-lookup"><span data-stu-id="17752-164">Subscription</span></span></p></th>
<th><p><span data-ttu-id="17752-165">Periodencode</span><span class="sxs-lookup"><span data-stu-id="17752-165">Period code</span></span></p></th>
<th><p><span data-ttu-id="17752-166">Verkaufswährung</span><span class="sxs-lookup"><span data-stu-id="17752-166">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="17752-167">Verkaufspreis</span><span class="sxs-lookup"><span data-stu-id="17752-167">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="17752-168">28.08.2006</span><span class="sxs-lookup"><span data-stu-id="17752-168">28-08-2006</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="17752-169">9030</span><span class="sxs-lookup"><span data-stu-id="17752-169">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="17752-170">Monat</span><span class="sxs-lookup"><span data-stu-id="17752-170">Month</span></span></p></td>
<td><p><span data-ttu-id="17752-171">EUR</span><span class="sxs-lookup"><span data-stu-id="17752-171">EUR</span></span></p></td>
<td><p><span data-ttu-id="17752-172">500</span><span class="sxs-lookup"><span data-stu-id="17752-172">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="17752-173">Beachten Sie, dass die Felder **Kategorie** und **Dauerauftrag** leer sind.</span><span class="sxs-lookup"><span data-stu-id="17752-173">Note that the **Category** and **Subscription** fields are empty.</span></span>

<span data-ttu-id="17752-174">Anschließend werden die folgenden Daueraufträge erstellt.</span><span class="sxs-lookup"><span data-stu-id="17752-174">You then create the following subscriptions.</span></span>

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
<th><p><span data-ttu-id="17752-175">Servicedauerauftrag</span><span class="sxs-lookup"><span data-stu-id="17752-175">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="17752-176">Projekt</span><span class="sxs-lookup"><span data-stu-id="17752-176">Project</span></span></p></th>
<th><p><span data-ttu-id="17752-177">Dauerauftragsgruppe</span><span class="sxs-lookup"><span data-stu-id="17752-177">Subscription group</span></span></p></th>
<th><p><span data-ttu-id="17752-178">Kategorie</span><span class="sxs-lookup"><span data-stu-id="17752-178">Category</span></span></p></th>
<th><p><span data-ttu-id="17752-179">Währung</span><span class="sxs-lookup"><span data-stu-id="17752-179">Currency</span></span></p></th>
<th><p><span data-ttu-id="17752-180">Periodencode</span><span class="sxs-lookup"><span data-stu-id="17752-180">Period code</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="17752-181">00020_135</span><span class="sxs-lookup"><span data-stu-id="17752-181">00020_135</span></span></p></td>
<td><p><span data-ttu-id="17752-182">9030</span><span class="sxs-lookup"><span data-stu-id="17752-182">9030</span></span></p></td>
<td><p><span data-ttu-id="17752-183">Unter1</span><span class="sxs-lookup"><span data-stu-id="17752-183">Sub1</span></span></p></td>
<td><p><span data-ttu-id="17752-184">UnterKat1</span><span class="sxs-lookup"><span data-stu-id="17752-184">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="17752-185">EUR</span><span class="sxs-lookup"><span data-stu-id="17752-185">EUR</span></span></p></td>
<td><p><span data-ttu-id="17752-186">Monatlich</span><span class="sxs-lookup"><span data-stu-id="17752-186">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17752-187">00021_135</span><span class="sxs-lookup"><span data-stu-id="17752-187">00021_135</span></span></p></td>
<td><p><span data-ttu-id="17752-188">9030</span><span class="sxs-lookup"><span data-stu-id="17752-188">9030</span></span></p></td>
<td><p><span data-ttu-id="17752-189">Unter1</span><span class="sxs-lookup"><span data-stu-id="17752-189">Sub1</span></span></p></td>
<td><p><span data-ttu-id="17752-190">UnterKat2</span><span class="sxs-lookup"><span data-stu-id="17752-190">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="17752-191">EUR</span><span class="sxs-lookup"><span data-stu-id="17752-191">EUR</span></span></p></td>
<td><p><span data-ttu-id="17752-192">Monatlich</span><span class="sxs-lookup"><span data-stu-id="17752-192">Monthly</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="17752-193">Im nächsten Schritt werden die Dauerauftragsgebühren für die beiden Daueraufträge der Gruppe "Unter1" erstellt:</span><span class="sxs-lookup"><span data-stu-id="17752-193">Now you create subscription fees for both subscriptions in the subscription group Sub1:</span></span>

1.  <span data-ttu-id="17752-194">Klicken Sie auf **Servicemanagement** \> **Einrichtung** \> **Daueraufträge** \> **Dauerauftragsgruppen**.</span><span class="sxs-lookup"><span data-stu-id="17752-194">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

2.  <span data-ttu-id="17752-195">In der **Dauerauftragsgruppen** im Formular und klicken im Formular **Funktion** \> **Dauerauftragsgebühr erstellen**.</span><span class="sxs-lookup"><span data-stu-id="17752-195">In the **Subscription groups** form, click **Function** \> **Create subscription fee**.</span></span>

3.  <span data-ttu-id="17752-196">In der **Dauerauftragsgebühr erstellen** Formular geben Sie die entsprechenden Informationen ein.</span><span class="sxs-lookup"><span data-stu-id="17752-196">In the **Create subscription fee** form, enter the appropriate information.</span></span> <span data-ttu-id="17752-197">Weitere Informationen finden Sie unter [Dauerauftragsgebühren-Buchungen erstellen](create-subscription-fee-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="17752-197">For more information, see [Create subscription fee transactions](create-subscription-fee-transactions.md).</span></span>

<span data-ttu-id="17752-198">Für beide Daueraufträge werden Dauerauftragsgebühren mit einem Verkaufspreis von EUR 500 erstellt. Dies ist in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="17752-198">Subscription fees that have a sales price of EUR 500 are created for both subscriptions, as shown in the following table.</span></span>

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
<th><p><span data-ttu-id="17752-199">Projektdatum</span><span class="sxs-lookup"><span data-stu-id="17752-199">Project date</span></span></p></th>
<th><p><span data-ttu-id="17752-200">Servicedauerauftrag</span><span class="sxs-lookup"><span data-stu-id="17752-200">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="17752-201">Projekt</span><span class="sxs-lookup"><span data-stu-id="17752-201">Project</span></span></p></th>
<th><p><span data-ttu-id="17752-202">Kategorie</span><span class="sxs-lookup"><span data-stu-id="17752-202">Category</span></span></p></th>
<th><p><span data-ttu-id="17752-203">Startdatum</span><span class="sxs-lookup"><span data-stu-id="17752-203">Start date</span></span></p></th>
<th><p><span data-ttu-id="17752-204">Enddatum</span><span class="sxs-lookup"><span data-stu-id="17752-204">End date</span></span></p></th>
<th><p><span data-ttu-id="17752-205">Verkaufswährung</span><span class="sxs-lookup"><span data-stu-id="17752-205">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="17752-206">Verkaufspreis</span><span class="sxs-lookup"><span data-stu-id="17752-206">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="17752-207">28.08.2006</span><span class="sxs-lookup"><span data-stu-id="17752-207">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="17752-208">00020_135</span><span class="sxs-lookup"><span data-stu-id="17752-208">00020_135</span></span></p></td>
<td><p><span data-ttu-id="17752-209">9030</span><span class="sxs-lookup"><span data-stu-id="17752-209">9030</span></span></p></td>
<td><p><span data-ttu-id="17752-210">UnterKat1</span><span class="sxs-lookup"><span data-stu-id="17752-210">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="17752-211">01.01.2007</span><span class="sxs-lookup"><span data-stu-id="17752-211">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="17752-212">31.03.2007</span><span class="sxs-lookup"><span data-stu-id="17752-212">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="17752-213">EUR</span><span class="sxs-lookup"><span data-stu-id="17752-213">EUR</span></span></p></td>
<td><p><span data-ttu-id="17752-214">500</span><span class="sxs-lookup"><span data-stu-id="17752-214">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17752-215">28.08.2006</span><span class="sxs-lookup"><span data-stu-id="17752-215">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="17752-216">00021_135</span><span class="sxs-lookup"><span data-stu-id="17752-216">00021_135</span></span></p></td>
<td><p><span data-ttu-id="17752-217">9030</span><span class="sxs-lookup"><span data-stu-id="17752-217">9030</span></span></p></td>
<td><p><span data-ttu-id="17752-218">UnterKat2</span><span class="sxs-lookup"><span data-stu-id="17752-218">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="17752-219">01.01.2007</span><span class="sxs-lookup"><span data-stu-id="17752-219">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="17752-220">31.03.2007</span><span class="sxs-lookup"><span data-stu-id="17752-220">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="17752-221">EUR</span><span class="sxs-lookup"><span data-stu-id="17752-221">EUR</span></span></p></td>
<td><p><span data-ttu-id="17752-222">500</span><span class="sxs-lookup"><span data-stu-id="17752-222">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="17752-223">Später entschließen Sie sich zum Angeben von Verkaufspreisen für die Kategorie "UnterKat1" des Projekts "9030".</span><span class="sxs-lookup"><span data-stu-id="17752-223">Later, you decide that you want to specify sales prices for the category SubCat1 for project 9030.</span></span> <span data-ttu-id="17752-224">Zu diesem Zweck erstellen Sie für die Kombination aus Projekt "9030" und Gebührenkategorie "UnterKat1" eine neue Verkaufspreisposition mit einem Verkaufspreis von EUR 550.</span><span class="sxs-lookup"><span data-stu-id="17752-224">Therefore, you create a new sales price line that has a sales price of EUR 550 for the combination of project 9030 and fee category SubCat1.</span></span> <span data-ttu-id="17752-225">Für das Projekt "9030" sind nun zwei Verkaufspreispositionen für Daueraufträge vorhanden. Dies ist in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="17752-225">There are now two subscription sales price lines for project 9030, as shown in the following table.</span></span>

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
<th><p><span data-ttu-id="17752-226">Gültig ab</span><span class="sxs-lookup"><span data-stu-id="17752-226">Valid from</span></span></p></th>
<th><p><span data-ttu-id="17752-227">Kategorie</span><span class="sxs-lookup"><span data-stu-id="17752-227">Category</span></span></p></th>
<th><p><span data-ttu-id="17752-228">Projekt</span><span class="sxs-lookup"><span data-stu-id="17752-228">Project</span></span></p></th>
<th><p><span data-ttu-id="17752-229">Dauerauftrag</span><span class="sxs-lookup"><span data-stu-id="17752-229">Subscription</span></span></p></th>
<th><p><span data-ttu-id="17752-230">Periodencode</span><span class="sxs-lookup"><span data-stu-id="17752-230">Period code</span></span></p></th>
<th><p><span data-ttu-id="17752-231">Währung</span><span class="sxs-lookup"><span data-stu-id="17752-231">Currency</span></span></p></th>
<th><p><span data-ttu-id="17752-232">Verkaufspreis</span><span class="sxs-lookup"><span data-stu-id="17752-232">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="17752-233">28.08.2007</span><span class="sxs-lookup"><span data-stu-id="17752-233">28-08-2007</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="17752-234">9030</span><span class="sxs-lookup"><span data-stu-id="17752-234">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="17752-235">Monat</span><span class="sxs-lookup"><span data-stu-id="17752-235">Month</span></span></p></td>
<td><p><span data-ttu-id="17752-236">EUR</span><span class="sxs-lookup"><span data-stu-id="17752-236">EUR</span></span></p></td>
<td><p><span data-ttu-id="17752-237">500</span><span class="sxs-lookup"><span data-stu-id="17752-237">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17752-238">28.08.2007</span><span class="sxs-lookup"><span data-stu-id="17752-238">28-08-2007</span></span></p></td>
<td><p><span data-ttu-id="17752-239">UnterKat1</span><span class="sxs-lookup"><span data-stu-id="17752-239">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="17752-240">9030</span><span class="sxs-lookup"><span data-stu-id="17752-240">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="17752-241">Monat</span><span class="sxs-lookup"><span data-stu-id="17752-241">Month</span></span></p></td>
<td><p><span data-ttu-id="17752-242">EUR</span><span class="sxs-lookup"><span data-stu-id="17752-242">EUR</span></span></p></td>
<td><p><span data-ttu-id="17752-243">550</span><span class="sxs-lookup"><span data-stu-id="17752-243">550</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="17752-244">Sie wiederholen das oben beschriebene Verfahren und erstellen Dauerauftragsgebühren für beide Daueraufträge der Dauerauftragsgruppe "Unter1".</span><span class="sxs-lookup"><span data-stu-id="17752-244">You repeat the procedure described above to create subscription fees for both subscriptions in the subscription group Sub1.</span></span> <span data-ttu-id="17752-245">In der folgenden Tabelle sind die Buchungen aufgeführt, die für die einzelnen Daueraufträge erstellt werden, die der Dauerauftragsgruppe zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="17752-245">The following table shows the transactions that are created for each subscription that is attached to the subscription group.</span></span>

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
<th><p><span data-ttu-id="17752-246">Projektdatum</span><span class="sxs-lookup"><span data-stu-id="17752-246">Project date</span></span></p></th>
<th><p><span data-ttu-id="17752-247">Dauerauftrag</span><span class="sxs-lookup"><span data-stu-id="17752-247">Subscription</span></span></p></th>
<th><p><span data-ttu-id="17752-248">Projekt</span><span class="sxs-lookup"><span data-stu-id="17752-248">Project</span></span></p></th>
<th><p><span data-ttu-id="17752-249">Kategorie</span><span class="sxs-lookup"><span data-stu-id="17752-249">Category</span></span></p></th>
<th><p><span data-ttu-id="17752-250">Startdatum</span><span class="sxs-lookup"><span data-stu-id="17752-250">Start date</span></span></p></th>
<th><p><span data-ttu-id="17752-251">Enddatum</span><span class="sxs-lookup"><span data-stu-id="17752-251">End date</span></span></p></th>
<th><p><span data-ttu-id="17752-252">Verkaufswährung</span><span class="sxs-lookup"><span data-stu-id="17752-252">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="17752-253">Verkaufspreis</span><span class="sxs-lookup"><span data-stu-id="17752-253">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="17752-254">28.07.2007</span><span class="sxs-lookup"><span data-stu-id="17752-254">28-07-2007</span></span></p></td>
<td><p><span data-ttu-id="17752-255">00020_135</span><span class="sxs-lookup"><span data-stu-id="17752-255">00020_135</span></span></p></td>
<td><p><span data-ttu-id="17752-256">9030</span><span class="sxs-lookup"><span data-stu-id="17752-256">9030</span></span></p></td>
<td><p><span data-ttu-id="17752-257">UnterKat1</span><span class="sxs-lookup"><span data-stu-id="17752-257">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="17752-258">01.01.2008</span><span class="sxs-lookup"><span data-stu-id="17752-258">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="17752-259">31.03.2008</span><span class="sxs-lookup"><span data-stu-id="17752-259">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="17752-260">EUR</span><span class="sxs-lookup"><span data-stu-id="17752-260">EUR</span></span></p></td>
<td><p><span data-ttu-id="17752-261">550</span><span class="sxs-lookup"><span data-stu-id="17752-261">550</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17752-262">28.07.2008</span><span class="sxs-lookup"><span data-stu-id="17752-262">28-07-2008</span></span></p></td>
<td><p><span data-ttu-id="17752-263">00021_135</span><span class="sxs-lookup"><span data-stu-id="17752-263">00021_135</span></span></p></td>
<td><p><span data-ttu-id="17752-264">9030</span><span class="sxs-lookup"><span data-stu-id="17752-264">9030</span></span></p></td>
<td><p><span data-ttu-id="17752-265">UnterKat2</span><span class="sxs-lookup"><span data-stu-id="17752-265">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="17752-266">01.01.2008</span><span class="sxs-lookup"><span data-stu-id="17752-266">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="17752-267">31.03.2008</span><span class="sxs-lookup"><span data-stu-id="17752-267">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="17752-268">EUR</span><span class="sxs-lookup"><span data-stu-id="17752-268">EUR</span></span></p></td>
<td><p><span data-ttu-id="17752-269">500</span><span class="sxs-lookup"><span data-stu-id="17752-269">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="17752-270">In der ersten Buchung für den Dauerauftrag 00020\_135 wird der Verkaufspreis in Höhe von EUR 550 von dem Dauerauftragsverkaufspreis abgeleitet, der für die Kombination aus diesem speziellen Projekt und der Kategorie festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="17752-270">In the first transaction for subscription 00020\_135, the sales price of EUR 550 derives from the subscription sales price that is set up for the combination of the specific project and category.</span></span> <span data-ttu-id="17752-271">In der zweiten Buchung für den Dauerauftrag 00021\_135 wird als Verkaufspreis für den Projektdauerauftrag der Betrag EUR 500 verwendet, da für die Kombination aus dem Projekt "9030" und der Kategorie "UnterKat2" kein Preis eingerichtet wurde.</span><span class="sxs-lookup"><span data-stu-id="17752-271">In the second transaction for subscription 00021\_135, the sales price of EUR 500 is used as the project subscription sales price because there is no price set up for the combination of project 9030 and category SubCat2.</span></span>

## <a name="see-also"></a><span data-ttu-id="17752-272">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="17752-272">See also</span></span>

[<span data-ttu-id="17752-273">Aktualisieren und Indizieren von Dauerauftrag-Verkaufspreisen</span><span class="sxs-lookup"><span data-stu-id="17752-273">Update and index subscription sales prices</span></span>](update-and-index-subscription-sales-prices.md)

  


