---
title: Einkaufswagenmodul
description: Dieses Thema enthält Einkaufsmodule und es wird beschrieben, wie diese den Sitesieten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
manager: annbe
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d91f6ff24f8f2c051ed23565983c2bc6a2c12b55
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261420"
---
# <a name="cart-module"></a><span data-ttu-id="c92b8-103">Einkaufswagenmodul</span><span class="sxs-lookup"><span data-stu-id="c92b8-103">Cart module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c92b8-104">Dieses Thema enthält Einkaufsmodule und es wird beschrieben, wie diese den Sitesieten in Microsoft Dynamics 365 Commerce hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="c92b8-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c92b8-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="c92b8-105">Overview</span></span>

<span data-ttu-id="c92b8-106">Über das Warenkorbmodul werden die Artikel angezeigt, die dem Warenkorb hinzugefügt wurden, bevor der Kunde zur Kasse geht.</span><span class="sxs-lookup"><span data-stu-id="c92b8-106">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="c92b8-107">Das Modul zeigt eine Bestellzusammenfassung an und der Kunde kann Werbecodes anwenden oder entfernen.</span><span class="sxs-lookup"><span data-stu-id="c92b8-107">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="c92b8-108">Das Einkaufskorbmodul unterstützt das Auschecken von angemeldeten Benutzern und von Gästen.</span><span class="sxs-lookup"><span data-stu-id="c92b8-108">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="c92b8-109">Es unterstützt auch eine Verknüpfung **Zurück zum Einkaufen**.</span><span class="sxs-lookup"><span data-stu-id="c92b8-109">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="c92b8-110">Sie können die Route für diesen Link unter **Seiteneinstellungen \>Erweiterungen \>Routen** konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="c92b8-110">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="c92b8-111">Das Warenkorbmodul rendert Daten basierend auf der Warenkorb-ID, einem auf der gesamten Site verfügbaren Browser-Cookie.</span><span class="sxs-lookup"><span data-stu-id="c92b8-111">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span>

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="c92b8-112">Einkaufswagenmodul-Eigenschaften und Slots</span><span class="sxs-lookup"><span data-stu-id="c92b8-112">Cart module properties and slots</span></span>

<span data-ttu-id="c92b8-113">Das Wagenmodul hat eine **Überschrift**-Eigenschaft, die auf Werte wie **Einkaufstasche** und **Artikel im Einkaufskorb** gesetzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="c92b8-113">The cart module has a **Heading** property that can be set to values such as **Shopping bag** and **Items in your cart**.</span></span> 

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="c92b8-114">Module, die im Einkaufswagenmodul verwendet werden können</span><span class="sxs-lookup"><span data-stu-id="c92b8-114">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="c92b8-115">**Textblock** – Dieses Modul unterstützt benutzerdefinierte Nachrichten im Einkaufswagenmodul.</span><span class="sxs-lookup"><span data-stu-id="c92b8-115">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="c92b8-116">Die Meldungen werden durch das Content Management-System (CMS) gesteuert.</span><span class="sxs-lookup"><span data-stu-id="c92b8-116">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="c92b8-117">Es können beliebige Nachrichten hinzugefügt werden wie „Für Probleme mit der Bestellung, kontaktieren Sie 1-800-Fabrikam.“</span><span class="sxs-lookup"><span data-stu-id="c92b8-117">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="c92b8-118">**Store-Selector** – Dieses Modul wird eine Liste von nahe gelegene Filialen anzeigen, die für eine Abholung zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="c92b8-118">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="c92b8-119">Hier können Benutzer einen Ort eingeben, um nach Geschäften in der Nähe zu suchen.</span><span class="sxs-lookup"><span data-stu-id="c92b8-119">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="c92b8-120">Weitere Informationen zu diesem Modul finden Sie unter [Auswahlmodul speichern](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="c92b8-120">For more information on this module, see [Store selector module](store-selector.md).</span></span>


## <a name="module-properties"></a><span data-ttu-id="c92b8-121">Moduleigenschaften</span><span class="sxs-lookup"><span data-stu-id="c92b8-121">Module properties</span></span>

<span data-ttu-id="c92b8-122">Einkaufswagenmodule haben die folgenden Einstellungen, die unter **Site-Einstellungen \> Erweiterungen** konfiguriert werden können:</span><span class="sxs-lookup"><span data-stu-id="c92b8-122">Cart modules have the following settings that can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="c92b8-123">**Höchstmenge** – Diese Eigenschaft dient zur Angabe der maximalen Anzahl jedes Artikels, die dem Einkaufskorb hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="c92b8-123">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="c92b8-124">Beispielsweise kann ein Einzelhändler festlegen, dass nur 10 eines Produkts als einzelne Transaktion verkauft werden können.</span><span class="sxs-lookup"><span data-stu-id="c92b8-124">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="c92b8-125">**Bestandsscheck** – Wenn der Wert auf **Wahr** gesetzt ist, wird nur ein Artikel in den Einkaufskorb gelegt, nachdem das Kauffeldmodul sicherstellt, dass es auf Lager ist.</span><span class="sxs-lookup"><span data-stu-id="c92b8-125">**Inventory check** – When the value is set to **True**, an item is added to the cart only after the buy box module makes sure that it's in stock.</span></span> <span data-ttu-id="c92b8-126">Diesee Lagerüberprüfung wird für Szenarien ausgeführt, bei denen der Artikel versendet wird und für Szenarien, wenn der Artikel in der Filiale abgeholt wird.</span><span class="sxs-lookup"><span data-stu-id="c92b8-126">This inventory check is done for scenarios where the item will be shipped and for scenarios where it will be picked up in the store.</span></span> <span data-ttu-id="c92b8-127">Wenn der Wert auf **Falsch** gesetzt wird, wird kein Bestandsscheck geleistet, bevor ein Artikel in den Einkaufskorb gelegt wird und der Auftrag erteilt wird.</span><span class="sxs-lookup"><span data-stu-id="c92b8-127">If the value is set to **False**, no inventory check is done before an item is added to the cart and the order is placed.</span></span> <span data-ttu-id="c92b8-128">Informationen zum Konfigurieren der Inventareinstellungen im Backoffice finden Sie unter [Berechnen Sie die Lagerverfügbarkeit für Einzelhandelskanäle](calculated-inventory-retail-channels.md).</span><span class="sxs-lookup"><span data-stu-id="c92b8-128">For information on how to configure inventory settings in back office, see [Calculate inventory availability for retail channels](calculated-inventory-retail-channels.md).</span></span>
- <span data-ttu-id="c92b8-129">**Inventarpuffer** – Diese Eigenschaft wird verwendet, um eine Puffernummer für das Inventar anzugeben.</span><span class="sxs-lookup"><span data-stu-id="c92b8-129">**Inventory buffer** – This property is used to specify a buffer number for inventory.</span></span> <span data-ttu-id="c92b8-130">Bestandspuffer – Lagerbestand wird in Echtzeit verwaltet und wenn viele Debitoren Bestellungen aufgeben, kann es schwierig sein, die Lagerzählung zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="c92b8-130">Inventory is maintained in real time, and when many customers place orders, it can be difficult to maintain an accurate inventory count.</span></span> <span data-ttu-id="c92b8-131">Wenn ein Bestandsscheck erfolgt, und wenn der Bestand kleiner ist als der Pufferbetrag, wird das Produkt nicht als vorrätig behandelt.</span><span class="sxs-lookup"><span data-stu-id="c92b8-131">When an inventory check is done, if the inventory is less than the buffer amount, the product is treated as out of stock.</span></span> <span data-ttu-id="c92b8-132">Wenn Verkäufe rasch in mehreren Kanälen erfolgen und die Bestandszählung nicht vollständig synchronisiert wird, ist das Risiko kleiner, dass ein Artikel verkauft wird, der nicht vorrätig ist.</span><span class="sxs-lookup"><span data-stu-id="c92b8-132">Therefore, when sales occur quickly through several channels, and the inventory count isn't fully synced, there is less risk that an item that is out of stock will be sold.</span></span>
- <span data-ttu-id="c92b8-133">**Zurück zum Einkaufen** – Mit dieser Eigenschaft wird die Route für die Verknüpfung **Zurück zum Einkaufen** angegeben.</span><span class="sxs-lookup"><span data-stu-id="c92b8-133">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="c92b8-134">Die Route kann auf Site-Ebene konfiguriert werden, sodass Einzelhändler den Kunden zur Homepage oder zu einer anderen Seite der Site zurückführen können.</span><span class="sxs-lookup"><span data-stu-id="c92b8-134">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="c92b8-135">Commerce Scale Unit-Interaktion</span><span class="sxs-lookup"><span data-stu-id="c92b8-135">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="c92b8-136">Das Einkaufskorbmoduls ruft Produktinformationen mithilfe der APIs der Commerce-Skalierungseinheit ab.</span><span class="sxs-lookup"><span data-stu-id="c92b8-136">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="c92b8-137">Die Kennung vom Einkaufskorb vom Browsercookie wird verwendet, um die gesamte Produktinformationen der Commerce-Skalierungseinheit abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c92b8-137">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="c92b8-138">Ein Einkaufswagenmodul einer Seite hinzufügen</span><span class="sxs-lookup"><span data-stu-id="c92b8-138">Add a cart module to a page</span></span>

<span data-ttu-id="c92b8-139">Um ein Einkaufswagenmodul einer neuen Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="c92b8-139">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="c92b8-140">Erstellen Sie ein Fragment, das mit dem Namen **Einkaufswagenfragment** bezeichnet ist und fügen Sie ein Einkaufswagenmodul dem neuen Fragment hinzu.</span><span class="sxs-lookup"><span data-stu-id="c92b8-140">Create a fragment named **Cart fragment**, and add a cart module to the new fragment.</span></span>
1. <span data-ttu-id="c92b8-141">Hinzufügen eines Titels zum Einkaufswagenmodul.</span><span class="sxs-lookup"><span data-stu-id="c92b8-141">Add a heading to the cart module.</span></span>
1. <span data-ttu-id="c92b8-142">Fügen Sie dem Einkaufswagenmodul ein Store-Selector-Modul hinzu.</span><span class="sxs-lookup"><span data-stu-id="c92b8-142">Add a store selector module to the cart module.</span></span>
1. <span data-ttu-id="c92b8-143">Speichern Sie das Fragment, beenden Sie die Bearbeitung und veröffentlichen Sie das Fragment.</span><span class="sxs-lookup"><span data-stu-id="c92b8-143">Save the fragment, finish editing, and then publish the fragment.</span></span>
1. <span data-ttu-id="c92b8-144">Erstellen Sie eine Vorlage mit der Bezeichnung **Einkaufswagenvorlage** und fügen Sie dann das Einkaufswagenfragment hinzu, das Sie soeben erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="c92b8-144">Create a template named **Cart template**, and add the cart fragment that you just created.</span></span>
1. <span data-ttu-id="c92b8-145">Speichern Sie die Vorlage, beenden Sie die Bearbeitung und veröffentlichen Sie die Vorlage.</span><span class="sxs-lookup"><span data-stu-id="c92b8-145">Save the template, finish editing, and then publish the template.</span></span>
1. <span data-ttu-id="c92b8-146">Hier können Sie eine Seite erstellen, für die die neue Vorlage verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c92b8-146">Create a page that uses the new template.</span></span>
1. <span data-ttu-id="c92b8-147">Seite speichern und Vorschau anzeigen.</span><span class="sxs-lookup"><span data-stu-id="c92b8-147">Save and preview the page.</span></span>
1. <span data-ttu-id="c92b8-148">Beenden Sie die Bearbeitung der Seite und veröffentlichen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="c92b8-148">Finish editing the page, and then publish the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c92b8-149">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c92b8-149">Additional resources</span></span>

[<span data-ttu-id="c92b8-150">Starterkit-Übersicht</span><span class="sxs-lookup"><span data-stu-id="c92b8-150">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="c92b8-151">Containermodul</span><span class="sxs-lookup"><span data-stu-id="c92b8-151">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="c92b8-152">Shopauswahlmodul</span><span class="sxs-lookup"><span data-stu-id="c92b8-152">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="c92b8-153">Kauffeldmodul</span><span class="sxs-lookup"><span data-stu-id="c92b8-153">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="c92b8-154">Symbol Einkaufswagenmodul</span><span class="sxs-lookup"><span data-stu-id="c92b8-154">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="c92b8-155">Auschecken-Modul</span><span class="sxs-lookup"><span data-stu-id="c92b8-155">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="c92b8-156">Auftragsbestätigungsmodul</span><span class="sxs-lookup"><span data-stu-id="c92b8-156">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="c92b8-157">Kopfzeilenmodul</span><span class="sxs-lookup"><span data-stu-id="c92b8-157">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="c92b8-158">Fußzeilenmodul</span><span class="sxs-lookup"><span data-stu-id="c92b8-158">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="c92b8-159">Lagerverfügbarkeit für Retail Channels berechnen</span><span class="sxs-lookup"><span data-stu-id="c92b8-159">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)
