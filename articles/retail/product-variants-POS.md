---
title: Lagersuche in der Verkaufsstelle (POS)
description: In diesem Thema werden die Optionen beschrieben, die für die Anzeige von Lagerbestandsinformationen in der Verkaufsstelle (POS) verfügbar sind.
author: ashishmsft
manager: AnnBe
ms.date: 03/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: Application update 5, AX 8.0
ms.openlocfilehash: 609f5f13f3af4a7621fe7ee152800dac4d68a9fc
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2019
ms.locfileid: "2025148"
---
# <a name="inventory-lookup-in-the-point-of-sale-pos"></a><span data-ttu-id="ba442-103">Lagersuche in der Verkaufsstelle (POS)</span><span class="sxs-lookup"><span data-stu-id="ba442-103">Inventory lookup in the point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ba442-104">Mithilfe der Lagersuche in der Verkaufsstelle (POS) können Einzelhändler erstklassige Betriebsprozesse in Echtzeit erreichen und Einblicke erlangen, indem sie Filialen, die POS und das Backoffice verbinden.</span><span class="sxs-lookup"><span data-stu-id="ba442-104">Inventory lookup in the point of sale (POS) helps retailers achieve real-time operational excellence and gain insights by connecting stores, the POS, and the back office.</span></span> <span data-ttu-id="ba442-105">Diese Funktionalität bieten eine genaue Echtzeitansicht des Produktbestands über Filialen und Verteilungszentren hinweg.</span><span class="sxs-lookup"><span data-stu-id="ba442-105">This functionality provides an accurate real-time view of product inventory across stores and distribution centers.</span></span> <span data-ttu-id="ba442-106">Einzelhändler werden zudem darin unterstützt, zusätzliche Effektivität und Kosteneinsparungen zu erreichen, indem sie die Bestandsplanung in Echtzeit verbessern.</span><span class="sxs-lookup"><span data-stu-id="ba442-106">It also helps retailers drive additional efficiencies and cost savings by improving inventory planning in real time.</span></span>

<span data-ttu-id="ba442-107">Mithilfe einer genauen Echtzeitansicht des Bestands in einer gesamten Organisation können Filialmitarbeiter einen rechtzeitigen, hochkarätigen Kundenservice bieten.</span><span class="sxs-lookup"><span data-stu-id="ba442-107">An accurate real-time view of inventory across an organization helps store associates provide timely, superior customer service.</span></span> <span data-ttu-id="ba442-108">Am wichtigsten ist der Augenblick, an dem der Debitor bereit ist, eine Kaufentscheidung zu treffen.</span><span class="sxs-lookup"><span data-stu-id="ba442-108">The moment that matters most is the moment when the customer is ready to make a purchase decision.</span></span> <span data-ttu-id="ba442-109">Es ist wichtig, dass Kassierer in der Filiale Echtzeitbestandsinformationen zur Hand haben, sodass sie eine Produktlieferung und -abholung genau zusagen können.</span><span class="sxs-lookup"><span data-stu-id="ba442-109">It's important that cashiers in the store have real-time inventory information at their fingertips, so that they can accurately promise product delivery and pickup.</span></span>

<span data-ttu-id="ba442-110">Sie können die Seite **Lagersuche** aus dem Arbeitsbereich **Retail Modern POS** oder **Retail Cloud POS** öffnen.</span><span class="sxs-lookup"><span data-stu-id="ba442-110">You can open the **Inventory lookup** page from the **Retail Modern POS** workspace or the **Retail Cloud POS** workspace.</span></span>

![Bestandssuchenkachel auf der POS-Startseite](media/POSHomepage.png)

<span data-ttu-id="ba442-112">Auf der Seite **Lagersuche** können Sie die numerische Tastatur verwenden, um eine Produktnummer einzugeben.</span><span class="sxs-lookup"><span data-stu-id="ba442-112">On the **Inventory lookup** page, you can use the numeric keyboard to enter a product number.</span></span> <span data-ttu-id="ba442-113">Sie können dann die verfügbare Menge für mehrere Filialen und Lagerorte anzeigen.</span><span class="sxs-lookup"><span data-stu-id="ba442-113">You can then view the on-hand quantity for multiple stores and warehouses.</span></span>

![Standardmäßige Lagerbestandssuchseite](media/InventoryLookUp.png)

<span data-ttu-id="ba442-115">Die Mengen **Reserviert** und **Bestellt** werden auch für jeden Lagerplatz angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ba442-115">**Reserved** and **Ordered** quantities are also shown for each location.</span></span>

- <span data-ttu-id="ba442-116">**Reserviert** – Diese Menge bezieht sich auf den Wert **Physisch reserviert** aus dem Backoffice für die angegebene Produktnummer am Lagerplatz.</span><span class="sxs-lookup"><span data-stu-id="ba442-116">**Reserved** – This quantity refers to the **Physical reserved** value from the back office for the specified product number at the location.</span></span>
- <span data-ttu-id="ba442-117">**Bestellt** – Diese Menge bezieht sich auf den Wert **Insgesamt bestellt** aus dem Backoffice für die angegebene Produktnummer am Lagerplatz.</span><span class="sxs-lookup"><span data-stu-id="ba442-117">**Ordered** – This quantity refers to the **Ordered in total** value from the back office for the specified product number at the location.</span></span>

## <a name="locations-that-inventory-availability-information-is-shown-for"></a><span data-ttu-id="ba442-118">Lagerplätze, für die Bestandsverfügbarkeitsinformationen angezeigt werden</span><span class="sxs-lookup"><span data-stu-id="ba442-118">Locations that inventory availability information is shown for</span></span>

<span data-ttu-id="ba442-119">Die Liste der Lagerplätze umfasst zwei Typen von Entitäten:</span><span class="sxs-lookup"><span data-stu-id="ba442-119">The list of locations includes two types of entities:</span></span>

- <span data-ttu-id="ba442-120">**Einzelhandelsfilialen** – In der Liste werden Filialen angezeigt, die mithilfe der Filiallokatorgruppe für die aktuelle Filiale in der Retail Zentralverwaltung konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="ba442-120">**Retail stores** – The list shows stores that are configured by using the store locator group for the current store in the Retail headquarters.</span></span>
- <span data-ttu-id="ba442-121">**Verteilungszentren** – Verschiedene Typen von Verteilungszentren (beispielsweise Lagerorte) können in Retail konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="ba442-121">**Distribution centers** – Various types of distribution centers (such as warehouses) can be configured in Retail.</span></span> <span data-ttu-id="ba442-122">Allerdings zeigt die Liste nur Bestandsverfügbarkeitsinformationen für Verteilungszentren des Standardtyps **Standard** an.</span><span class="sxs-lookup"><span data-stu-id="ba442-122">However, the list shows inventory availability information only for distribution centers of the **Standard** default type.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ba442-123">Bestandsverfügbarkeitsinformationen wird nicht für Lagerorte der Typen **Zustellung**, **Quarantäne** und **Waren im Arbeitsplan** für die POS angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ba442-123">Inventory availability information isn't shown for warehouses of the **Transit**, **Quarantine**, and **Goods in Route** types for the POS.</span></span>

<span data-ttu-id="ba442-124">Auf der Seite **Lagersuche** können Sie die Mengen anzeigen, die verfügbar für Zusage (VfZ) für jede Filiale sind, zusätzlich zu den aktuellen verfügbaren Menge, reservierten Mengen und bestellten Mengen.</span><span class="sxs-lookup"><span data-stu-id="ba442-124">On the **Inventory lookup** page, you can view available to promise (ATP) quantities for each store, in addition to the current on-hand quantities, reserved quantities, and ordered quantities.</span></span> <span data-ttu-id="ba442-125">Wählen Sie die Filiale aus, für die die VfZ-Informationen angezeigt werden soll, und wählen Sie dann **Verfügbarkeit in Filiale anzeigen** aus.</span><span class="sxs-lookup"><span data-stu-id="ba442-125">Select the store to view the ATP information for, and then select **Show store availability**.</span></span>

![ATP-Mengen](media/ATP.png)

## <a name="opening-the-dimension-based-matrix-view-to-show-all-variants"></a><span data-ttu-id="ba442-127">Öffnen der dimensionsbasierten Matrix, um alle Varianten anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="ba442-127">Opening the Dimension based matrix view to show all variants</span></span>

<span data-ttu-id="ba442-128">Wählen Sie auf der Seite **Produktdetails** eines Produktmasters oder auf der Seite **Lagersuche** die Option **Alle Varianten anzeigen** aus der App-Leiste unten auf der Seite aus.</span><span class="sxs-lookup"><span data-stu-id="ba442-128">On the **Product details** page of a product master, or on the **Inventory lookup** page, select **View all variants** from the app-bar at bottom of the page.</span></span> <span data-ttu-id="ba442-129">Die Ansicht **Dimensionsbasierte Matrix** für den ersten Start aus diesen Seiten zeigt die Bestandsverfügbarkeitsinformationen für alle Varianten eines Produkts für die aktuelle Filiale an.</span><span class="sxs-lookup"><span data-stu-id="ba442-129">The **Dimension based matrix** view for the initial launch from these pages shows the inventory availability information for all variants of a product for the current store.</span></span>

> [!NOTE]
> <span data-ttu-id="ba442-130">Die Schaltfläche **Alle Varianten anzeigen** ist nur für Artikelproduktmaster verfügbar, die Produktvarianten haben.</span><span class="sxs-lookup"><span data-stu-id="ba442-130">The **View all variants** button is available only for item product masters that have product variants.</span></span> <span data-ttu-id="ba442-131">Sie ist nicht für eigenständige Produkte oder Bausätze verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ba442-131">It isn't available for standalone products or kits.</span></span>

![Schaltfläche „Alle Varianten anzeigen” auf der Seite „Lagersuche”](media/StandardToMatrix.png)

<span data-ttu-id="ba442-133">Wählen Sie **Alle Varianten anzeigen** auf der Seite **Produktdetails** eines Produktmasters oder auf der Seite **Lagersuche** aus, ohne einen Lagerplatz auszuwählen, um zur Ansicht **Dimensionsbasierte Matrix** zu wechseln, um die Bestandsverfügbarkeitsinformationen für alle Varianten eines Produkts für die aktuelle Filiale anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ba442-133">Select **View all variants** on the **Product details** page of a product master, or on the **Inventory lookup** page, without selecting a location, to go to the **Dimension based matrix** view to view the inventory availability information for all variants of a product for the current store.</span></span>

![Dimensionsbasierte Matrixansicht für die Seite „Lagersuche”](media/Matrix.png)

> [!NOTE]
> <span data-ttu-id="ba442-135">In der vorherigen Abbildung ist die Anzeigereihenfolge der Dimensionen alphabetisch, da die Anzeigereihenfolge der Dimensionen für das ausgewählte Produkt nicht konfiguriert wurde.</span><span class="sxs-lookup"><span data-stu-id="ba442-135">In the preceding illustration, the display order of the dimensions is alphabetic, because the display order of dimensions wasn't configured for the selected product.</span></span>

<span data-ttu-id="ba442-136">In der Ansicht **Dimensionsbasierte Matrix** umfassen die Zellen für die Produktvarianten einen verfügbaren Wert in der unteren rechten Ecke.</span><span class="sxs-lookup"><span data-stu-id="ba442-136">In the **Dimension based matrix** view, the cells for the product variants include an on-hand value in the lower-right corner.</span></span> <span data-ttu-id="ba442-137">In der folgenden Tabelle wird die Bedeutung der verschiedenen Werte erklärt.</span><span class="sxs-lookup"><span data-stu-id="ba442-137">The following table explains the meaning of the various values.</span></span>

| <span data-ttu-id="ba442-138">Verfügbarer Wert</span><span class="sxs-lookup"><span data-stu-id="ba442-138">On-hand value</span></span>                            | <span data-ttu-id="ba442-139">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ba442-139">Description</span></span> |
|------------------------------------------|-------------|
| <span data-ttu-id="ba442-140">Numerischer Wert der größer als 0 (null) ist</span><span class="sxs-lookup"><span data-stu-id="ba442-140">Numeric value that is more than 0 (zero)</span></span> | <span data-ttu-id="ba442-141">Eine Variante ist für den ausgewählten Lagerplatz freigegeben worden, und Sie können zusätzliche Aktivitäten in der Zelle ausführen.</span><span class="sxs-lookup"><span data-stu-id="ba442-141">A variant has been released to the selected location, and you can perform additional actions in the cell.</span></span> <span data-ttu-id="ba442-142">(Diese Aktivitäten werden detaillierter später in diesem Thema beschrieben.)</span><span class="sxs-lookup"><span data-stu-id="ba442-142">(These actions are described in more detail later in this topic.)</span></span> |
| <span data-ttu-id="ba442-143">**0** (null)</span><span class="sxs-lookup"><span data-stu-id="ba442-143">**0** (zero)</span></span>                             | <span data-ttu-id="ba442-144">Eine Variante ist für den ausgewählten Lagerplatz freigegeben worden, aber der Artikel ist nicht im ausgewählten Lagerplatz verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ba442-144">A variant has been released to the selected location, but the item isn't available in selected location.</span></span> <span data-ttu-id="ba442-145">Sie können jedoch zusätzliche Aktivitäten in der Zelle ausführen.</span><span class="sxs-lookup"><span data-stu-id="ba442-145">However, you can perform additional actions in the cell.</span></span> <span data-ttu-id="ba442-146">(Diese Aktivitäten werden detaillierter später in diesem Thema beschrieben.)</span><span class="sxs-lookup"><span data-stu-id="ba442-146">(These actions are described in more detail later in this topic.)</span></span> |
| <span data-ttu-id="ba442-147">**n/v** oder eine inaktive Zelle</span><span class="sxs-lookup"><span data-stu-id="ba442-147">**n/a** or an inactive cell</span></span>              | <span data-ttu-id="ba442-148">Eine Variante ist für den ausgewählten Lagerplatz nicht freigegeben worden, und Sie können keine zusätzlichen Aktivitäten in der Zelle ausführen.</span><span class="sxs-lookup"><span data-stu-id="ba442-148">A variant hasn't been released to the selected location, and you can't perform additional actions in the cell.</span></span> |

<span data-ttu-id="ba442-149">Sie können auch den Pivot für Dimensionen ändern, indem Sie die neue Dimension auswählen, die zu verwenden ist.</span><span class="sxs-lookup"><span data-stu-id="ba442-149">You can also change the pivot for dimensions by selecting the new dimension to use.</span></span>

![Ändern des Pivot](media/ChangePivot.png)

![Pivot geändert](media/PivotChanged.png)

> [!NOTE]
> <span data-ttu-id="ba442-152">In den vorhergehenden Abbildungen ist die Anzeigereihenfolge der Dimensionen für das ausgewählte Produkt benutzerdefiniert (nicht alphabetisch).</span><span class="sxs-lookup"><span data-stu-id="ba442-152">In the preceding illustrations, the display order of the dimensions for the selected product is custom (non-alphabetic).</span></span> <span data-ttu-id="ba442-153">Sie basiert auf der Dimensionsanzeigereihenfolge, die im Backoffice festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ba442-153">It's based on the dimension display order that is set in the back office.</span></span>

<span data-ttu-id="ba442-154">Darüber können in der Ansicht **Dimensionsbasierte Matrix** mehr Aktivitäten ausgeführt werden, mit deren Hilfe die Produktivität eines Filialmitarbeiters gesteigert werden kann.</span><span class="sxs-lookup"><span data-stu-id="ba442-154">Additionally, in the **Dimension based matrix** view, more actions can be performed to help boost a store associate's productivity.</span></span> <span data-ttu-id="ba442-155">Nachfolgend finden Sie einige Beispiele:</span><span class="sxs-lookup"><span data-stu-id="ba442-155">Here are some examples:</span></span>

- <span data-ttu-id="ba442-156">Ändern Sie den Filiallagerplatz, um die Bestandsverfügbarkeit aller Produktvarianten in anderen Lagerplätzen zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="ba442-156">Change the store location to look up the inventory availability of all product variants at other locations.</span></span> <span data-ttu-id="ba442-157">Diese Lagerplätze umfassen andere Filialen in der Filiallokatorgruppe und den Verteilungszentren des Standardtyps **Standard**.</span><span class="sxs-lookup"><span data-stu-id="ba442-157">These locations include other stores in the store locator group and distribution centers of the **Standard** default type.</span></span>
- <span data-ttu-id="ba442-158">Verkaufen Sie eine einzelne Produktvariante an einen Debitor unter Verwendung von Mitnahme, Filialabholung oder Lieferung an eine Adresse.</span><span class="sxs-lookup"><span data-stu-id="ba442-158">Sell an individual product variant to a customer by using cash and carry, in-store pickup, or shipment to an address.</span></span>
- <span data-ttu-id="ba442-159">Teilen Sie dem Debitor VfZ-Informationen für eine einzelne Produktvariante an einem bestimmten Lagerplatz mit.</span><span class="sxs-lookup"><span data-stu-id="ba442-159">Provide the customer with ATP information for an individual product variant at a specific location.</span></span>

![Zusätzliche Aktivitäten auf Variantenkacheln](media/VariantActions.png)

> [!NOTE]
> <span data-ttu-id="ba442-161">In der vorherigen Abbildung ist die Anzeigereihenfolge der Dimensionen alphabetisch, da die Anzeigereihenfolge der Dimensionen für das ausgewählte Produkt nicht konfiguriert wurde.</span><span class="sxs-lookup"><span data-stu-id="ba442-161">In the preceding illustration, the display order of the dimensions is alphabetic, because the display order of dimensions wasn't configured for the selected product.</span></span>

<span data-ttu-id="ba442-162">Die folgende Tabelle enthält weitere Informationen über die zusätzlichen Aktivitäten, die verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="ba442-162">The following table provides more information about the additional actions that are available.</span></span>

| <span data-ttu-id="ba442-163">Vorgang</span><span class="sxs-lookup"><span data-stu-id="ba442-163">Action</span></span>               | <span data-ttu-id="ba442-164">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ba442-164">Description</span></span> |
|----------------------|-------------|
| <span data-ttu-id="ba442-165">Jetzt verkaufen</span><span class="sxs-lookup"><span data-stu-id="ba442-165">Sell now</span></span>             | <span data-ttu-id="ba442-166">Fügen Sie die ausgewählten Artikelvarianten der Transaktion hinzu, und leiten Sie den Benutzer zum Transaktionsbildschirm um.</span><span class="sxs-lookup"><span data-stu-id="ba442-166">Add the selected item variant to the transaction, and redirect the user to the transaction screen.</span></span> <span data-ttu-id="ba442-167">(Diese Aktivität ist nicht verfügbar, wenn der ausgewählte Lagerplatz ein Verteilungszentrum ist.)</span><span class="sxs-lookup"><span data-stu-id="ba442-167">(This action isn't available when the selected location is a distribution center.)</span></span> |
| <span data-ttu-id="ba442-168">Abholung im Shop</span><span class="sxs-lookup"><span data-stu-id="ba442-168">Pick up in store</span></span>     | <span data-ttu-id="ba442-169">Erstellen Sie einen Debitorenauftrag für die Produktvariante, die vom ausgewählten Lagerplatz abgeholt wird, und leiten Sie den Benutzer zum Buchungsbildschirm um.</span><span class="sxs-lookup"><span data-stu-id="ba442-169">Create a customer order for the product variant that will be picked up from the selected location, and redirect the user to the transaction screen.</span></span> <span data-ttu-id="ba442-170">(Diese Aktivität ist nicht verfügbar, wenn der ausgewählte Lagerplatz ein Verteilungszentrum ist.)</span><span class="sxs-lookup"><span data-stu-id="ba442-170">(This action isn't available when the selected location is a distribution center.)</span></span> |
| <span data-ttu-id="ba442-171">Produkt versenden</span><span class="sxs-lookup"><span data-stu-id="ba442-171">Ship product</span></span>         | <span data-ttu-id="ba442-172">Erstellen Sie einen Debitorenauftrag für die Produktvariante, die vom ausgewählten Lagerplatz geliefert wird, und leiten Sie den Benutzer zum Buchungsbildschirm um.</span><span class="sxs-lookup"><span data-stu-id="ba442-172">Create a customer order for the product variant that will be shipped from the selected location, and redirect the user to the transaction screen.</span></span> |
| <span data-ttu-id="ba442-173">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="ba442-173">Availability</span></span>         | <span data-ttu-id="ba442-174">Zeigen Sie die VfZ-Informationen für die ausgewählte Variantenkombination für den ausgewählten Lagerplatz an.</span><span class="sxs-lookup"><span data-stu-id="ba442-174">Show the ATP information for the selected variant combination for the selected location.</span></span> |
| <span data-ttu-id="ba442-175">Alle Lagerplätze anzeigen</span><span class="sxs-lookup"><span data-stu-id="ba442-175">Show all locations</span></span>   | <span data-ttu-id="ba442-176">Wechseln Sie zur standardmäßigen Lagersuchansicht und heben Sie Bestandsverfügbarkeitsinformationen für die Artikelvariante für alle Filialen in der Filiallokatorgruppe und auch in Verteilungszentren des Typs **Standard/Standard** hervor.</span><span class="sxs-lookup"><span data-stu-id="ba442-176">Switch to the standard inventory lookup view, and highlight inventory availability information for the item variant across all stores in the store locator group, and also in distribution centers of the **Standard/Default** type.</span></span> |
| <span data-ttu-id="ba442-177">Produktdetails anzeigen</span><span class="sxs-lookup"><span data-stu-id="ba442-177">View product details</span></span> | <span data-ttu-id="ba442-178">Leiten Sie den Benutzer zur Seite **Produktdetails** des zugeordneten Produktmasters um.</span><span class="sxs-lookup"><span data-stu-id="ba442-178">Redirect the user to the **Product details** page of the associated product master.</span></span> |
