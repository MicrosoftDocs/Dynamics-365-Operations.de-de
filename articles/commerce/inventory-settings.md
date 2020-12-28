---
title: Wenden Sie Inventareinstellungen an
description: In diesem Thema werden Inventareinstellungen behandelt und beschrieben, wie sie in Microsoft Dynamics 365 Commerce angewendet werden.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: dfa8b2bdc03e3698feda26932db757421097140d
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517063"
---
# <a name="apply-inventory-settings"></a><span data-ttu-id="6c681-103">Wenden Sie Inventareinstellungen an</span><span class="sxs-lookup"><span data-stu-id="6c681-103">Apply inventory settings</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6c681-104">In diesem Thema werden Inventareinstellungen behandelt und beschrieben, wie sie in Microsoft Dynamics 365 Commerce angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="6c681-104">This topic covers inventory settings and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6c681-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="6c681-105">Overview</span></span>

<span data-ttu-id="6c681-106">Die Inventareinstellungen geben an, ob das Inventar überprüft werden soll, bevor Produkte in den Warenkorb gelegt werden.</span><span class="sxs-lookup"><span data-stu-id="6c681-106">Inventory settings specify whether inventory should be checked before products are added to the cart.</span></span> <span data-ttu-id="6c681-107">Sie definieren auch inventarbezogene Merchandising-Nachrichten wie Auf Lager und Nur noch wenige übrig.</span><span class="sxs-lookup"><span data-stu-id="6c681-107">They also define inventory-related merchandising messages, such as "In stock" and "Only a few left."</span></span> <span data-ttu-id="6c681-108">Diese Einstellungen stellen sicher, dass ein Produkt nicht gekauft werden kann, wenn es nicht vorrätig ist.</span><span class="sxs-lookup"><span data-stu-id="6c681-108">These settings ensure that a product can't be purchased if it's out of stock.</span></span>

<span data-ttu-id="6c681-109">Dynamics 365 Commerce bietet Schätzungen zur Verfügbarkeit von Produkten.</span><span class="sxs-lookup"><span data-stu-id="6c681-109">Dynamics 365 Commerce provides estimates of on-hand availability for products.</span></span> <span data-ttu-id="6c681-110">Informationen zur Berechnung der geschätzten Verfügbarkeit finden Sie unter [Berechnen Sie die Lagerverfügbarkeit für Einzelhandelskanäle](calculated-inventory-retail-channels.md).</span><span class="sxs-lookup"><span data-stu-id="6c681-110">For information about how estimated on-hand availability is calculated, see [Calculate inventory availability for retail channels](calculated-inventory-retail-channels.md).</span></span>

<span data-ttu-id="6c681-111">In Commerce Site Builder können Bestandsschwellenwerte und -bereiche für ein Produkt oder eine Kategorie definiert werden.</span><span class="sxs-lookup"><span data-stu-id="6c681-111">In Commerce site builder, inventory thresholds and ranges can be defined for a product or a category.</span></span> <span data-ttu-id="6c681-112">Sie bestimmen, ob der Lagerbestand als vorrätig, niedrig oder nicht vorrätig eingestuft werden kann.</span><span class="sxs-lookup"><span data-stu-id="6c681-112">They determine whether inventory can be classified as in stock, low stock, or out of stock.</span></span> <span data-ttu-id="6c681-113">Einzelheiten finden Sie unter [Konfigurieren Sie Bestandpuffer und Bestandebenen](inventory-buffers-levels.md).</span><span class="sxs-lookup"><span data-stu-id="6c681-113">For details, see [Configure inventory buffers and inventory levels](inventory-buffers-levels.md).</span></span>

> [!NOTE]
> <span data-ttu-id="6c681-114">Unterstützung für Bestandsschwellen und -bereiche finden Sie in der Dynamics 365 Commerce-Version 10.0.12.</span><span class="sxs-lookup"><span data-stu-id="6c681-114">Support for inventory thresholds and ranges is available in the Dynamics 365 Commerce 10.0.12 release.</span></span>

## <a name="inventory-settings"></a><span data-ttu-id="6c681-115">Bestandeinstellungen</span><span class="sxs-lookup"><span data-stu-id="6c681-115">Inventory settings</span></span>

<span data-ttu-id="6c681-116">In Commerce werden Bestandeinstellungen unter **Seiteneinstellungen \> Erweiterungen \> Bestandsverwaltung** im Site Builder definiert.</span><span class="sxs-lookup"><span data-stu-id="6c681-116">In Commerce, inventory settings are defined at **Site Settings \> Extensions \> Inventory Management** in site builder.</span></span> <span data-ttu-id="6c681-117">Es gibt vier Bestandeinstellungen, von denen eine veraltet (veraltet) ist:</span><span class="sxs-lookup"><span data-stu-id="6c681-117">There are four inventory settings, one of which is obsolete (deprecated):</span></span>

- <span data-ttu-id="6c681-118">**Bestandsüberprüfung in App aktivieren** – Diese Einstellung aktiviert eine Produktbestandsüberprüfung.</span><span class="sxs-lookup"><span data-stu-id="6c681-118">**Enable stock check in app** – This setting turns on a product inventory check.</span></span> <span data-ttu-id="6c681-119">Wenn Sie Box-, Warenkorb- und Abholmodule kaufen, wird der Produkbestand überprüft und das Hinzufügen eines Produkts zum Warenkorb nur dann ermöglicht, wenn Bestand verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="6c681-119">Buy box, cart, and pick up in store modules will then check product inventory, and will allow a product to be added to the cart only if inventory is available.</span></span>
- <span data-ttu-id="6c681-120">**Lagerbestand basierend auf** – Diese Einstellung definiert, wie die Lagerbestände berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="6c681-120">**Inventory level based on** – This setting defines how inventory levels are calculated.</span></span> <span data-ttu-id="6c681-121">Die verfügbaren Werte sind **Insgesamt verfügbar**, **Physisch verfügbar** und **Nicht verfügbar**.</span><span class="sxs-lookup"><span data-stu-id="6c681-121">The available values are **Total Available**, **Physical Available**, and **Out of stock threshold**.</span></span> <span data-ttu-id="6c681-122">In Commerce Site Builder können die Bestandsschwellenwerte und -bereiche für ein Produkt oder eine Kategorie definiert werden.</span><span class="sxs-lookup"><span data-stu-id="6c681-122">In Commerce, inventory threshold and ranges can be defined for each product and category.</span></span> <span data-ttu-id="6c681-123">Die Inventar-APIs geben Produktbestandinformationen für die Eigenschaft **Insgesamt verfügbar** und **Physisch verfügbar** zurück.</span><span class="sxs-lookup"><span data-stu-id="6c681-123">The inventory APIs return product inventory information for both the **Total Available** property and the **Physical Available** property.</span></span> <span data-ttu-id="6c681-124">Der Händler entscheidet, ob der Wert **Insgesamt verfügbar** oder **Physisch verfügbar** verwendet wird, um die Anzahl der Bestände und die entsprechenden Bereiche für den Status Lagerbestand verfügbar und Lagerbestand nicht verfügbar zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="6c681-124">The retailer decides whether the **Total Available** or **Physical Available** value should be used to determine the inventory count and the corresponding ranges for in-stock and out-of-stock statuses.</span></span>

    <span data-ttu-id="6c681-125">Der Wert **Nicht vorrätige Schwelle** des **Lagerbestand basierend auf** Einstellungen ist ein alter (veralteter) Wert.</span><span class="sxs-lookup"><span data-stu-id="6c681-125">The **Out of stock threshold** value of the **Inventory level based on** setting is an old (legacy), obsolete value.</span></span> <span data-ttu-id="6c681-126">Wenn er ausgewählt ist, wird die Bestandanzahl aus den Ergebnissen des Werts **Insgesamt verfügbar** ermittelt, aber der Schwellenwert wird durch die Einstellung **Nicht vorrätige Schwelle** numerische Einstellung definiert, die später beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="6c681-126">When it's selected, the inventory count is determined from the results of the **Total Available** value, but the threshold is defined by the **Out of stock threshold** numeric setting that is described later.</span></span> <span data-ttu-id="6c681-127">Diese Schwellenwerteinstellung gilt für alle Produkte auf einer E-Commerce-Website.</span><span class="sxs-lookup"><span data-stu-id="6c681-127">This threshold setting applies to all products across an e-commerce site.</span></span> <span data-ttu-id="6c681-128">Wenn der Lagerbestand unter dem Schwellenwert liegt, gilt ein Produkt als nicht vorrätig.</span><span class="sxs-lookup"><span data-stu-id="6c681-128">If inventory is below the threshold number, a product is considered out of stock.</span></span> <span data-ttu-id="6c681-129">Ansonsten gilt es als auf Lager.</span><span class="sxs-lookup"><span data-stu-id="6c681-129">Otherwise, it's considered in stock.</span></span> <span data-ttu-id="6c681-130">Die Möglichkeiten des Werts **Nicht vorrätige Schwelle** ist begrenzt und wir empfehlen nicht, ihn in Version 10.0.12 und höher zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="6c681-130">The capabilities of the **Out of stock threshold** value are limited, and we don't recommend that you use it in version 10.0.12 and later.</span></span>

- <span data-ttu-id="6c681-131">**Bestandsbereiche** – Diese Einstellung definiert die Bestandbereiche, für die die Meldung vor Ort angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="6c681-131">**Inventory ranges** – This setting defines the inventory ranges that message are shown for on site modules.</span></span> <span data-ttu-id="6c681-132">Er ist nur anwendbar, wenn entweder der **Insgesamt verfügbar** oder der Wert **Physisch verfügbar** ausgewählt für die Einstellung **Lagerbestand basierend auf**.</span><span class="sxs-lookup"><span data-stu-id="6c681-132">It's applicable only if either the **Total Available** value or the **Physical Available** value is selected for the **Inventory level based on** setting.</span></span> <span data-ttu-id="6c681-133">Die verfügbaren Werte sind **Alle**, **Niedrig und vergriffen** und **Ausverkauft**.</span><span class="sxs-lookup"><span data-stu-id="6c681-133">The available values are **All**, **Low and out of stock**, and **Out of stock**.</span></span>

    - <span data-ttu-id="6c681-134">Wenn **Alle** ausgewählt ist, werden Meldungen für alle Bestandsbereiche angezeigt, von Auf Lager (Meldung Verfügbar) bis Nicht vorrätig (Meldung Nicht vorrätig).</span><span class="sxs-lookup"><span data-stu-id="6c681-134">When **All** is selected, messages for all inventory ranges, from in stock ("Available" message) to out of stock ("Out of stock" message), will be shown.</span></span>
    - <span data-ttu-id="6c681-135">Wenn **tief und nicht an Lager** ausgewählt ist, werden Meldungen für alle Bestandsbereiche angezeigt, ausgenommen Auf Lager (Meldung Verfügbar).</span><span class="sxs-lookup"><span data-stu-id="6c681-135">When **Low and out of stock** is selected, messages for all inventory ranges except in stock ("Available" message) will be shown.</span></span>
    - <span data-ttu-id="6c681-136">Wenn **Ausverkauft** ausgewählt ist, werden nur die Nachrichten Nicht vorrätig angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6c681-136">When **Out of stock** is selected, only the "Out of stock" message will be shown.</span></span>

- <span data-ttu-id="6c681-137">**Nicht vorrätige Schwelle** – Diese alte numerische Einstellung wird nur wirksam, wenn der Wert **Nicht vorrätige Schwelle** für die Einstellung **Lagerbestand basierend auf** ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="6c681-137">**Out of stock threshold** – This old numeric setting will take effect only if the **Out of stock threshold** value is selected for the **Inventory level based on** setting.</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="6c681-138">Diese Einstellungen sind in Dynamics 365 Commerce 10.0.12 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6c681-138">These settings are available in the Dynamics 365 Commerce 10.0.12 release.</span></span> <span data-ttu-id="6c681-139">Wenn Sie eine Aktualisierung von einer älteren Version von Dynamics 365 Commerce durchführen, müssen Sie die Datei appsettings.json manuell aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="6c681-139">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="6c681-140">Anweisungen zum Aktualisieren der Datei appsettings.json finden Sie unter [SDK- und Modulbibliothekupdates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="6c681-140">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="modules-that-use-inventory-settings"></a><span data-ttu-id="6c681-141">Module, die Bestandeinstellungen verwenden</span><span class="sxs-lookup"><span data-stu-id="6c681-141">Modules that use inventory settings</span></span>

<span data-ttu-id="6c681-142">Kaufbox, Wunschliste, Filialauswahl, Warenkorb und Warenkorbsymbolmodule verwenden Bestandeinstellungen, um die Inventarbereiche und Meldungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="6c681-142">Buy box, wishlist, store selector, cart, and cart icon modules use inventory settings to show the inventory ranges and messages.</span></span>

<span data-ttu-id="6c681-143">Das folgende Bild zeigt ein Beispiel für eine Produktdetailseite (PDP), auf der eine Meldung Auf Lager (Verfügbar) angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="6c681-143">The following image shows an example of a product details page (PDP) that is showing an in-stock ("Available") message.</span></span>

![Beispiel eines PDP-Moduls mit einer Nachricht auf Lager](./media/pdp-InStock.png)

<span data-ttu-id="6c681-145">Das folgende Bild zeigt ein Beispiel für eine Produktdetailseite (PDP), auf der eine Meldung Nicht auf Lager (Nicht Verfügbar) angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="6c681-145">The following image shows an example of a PDP that is showing an "Out of stock" message.</span></span>

![Beispiel eines PDP-Moduls mit einer Nachricht Nicht auf Lager](./media/pdp-outofstock.png)

<span data-ttu-id="6c681-147">Das folgende Bild zeigt ein Beispiel für einen Einkaufswagen, mit der Meldung auf Lager (Verfügbar).</span><span class="sxs-lookup"><span data-stu-id="6c681-147">The following image shows an example of a cart that is showing an in-stock ("Available") message.</span></span>

![Beispiel eines Einkaufswagenmoduls mit einer Nachricht auf Lager](./media/cart-instock.png)

## <a name="additional-resources"></a><span data-ttu-id="6c681-149">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6c681-149">Additional resources</span></span>

[<span data-ttu-id="6c681-150">Übersicht über die Modulbibliothek</span><span class="sxs-lookup"><span data-stu-id="6c681-150">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="6c681-151">Bestandpuffer und Bestandsebenen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="6c681-151">Configure inventory buffers and inventory levels</span></span>](inventory-buffers-levels.md)

[<span data-ttu-id="6c681-152">Einkaufswagenmodul</span><span class="sxs-lookup"><span data-stu-id="6c681-152">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="6c681-153">Kauffeldmodul</span><span class="sxs-lookup"><span data-stu-id="6c681-153">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="6c681-154">Kontenverwaltungsseiten und -module</span><span class="sxs-lookup"><span data-stu-id="6c681-154">Account management pages and modules</span></span>](account-management.md)

[<span data-ttu-id="6c681-155">Shopauswahlmodul</span><span class="sxs-lookup"><span data-stu-id="6c681-155">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="6c681-156">SDK- und Modulbibliothekupdates</span><span class="sxs-lookup"><span data-stu-id="6c681-156">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)
