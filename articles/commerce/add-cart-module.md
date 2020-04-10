---
title: Einkaufswagenmodul
description: Dieses Thema enthält Einkaufsmodule und es wird beschrieben, wie diese den Sitesieten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
manager: annbe
ms.date: 03/19/2020
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
ms.openlocfilehash: 598b35b1bd365e761d8d4c5ef214935e60b971f4
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154016"
---
# <a name="cart-module"></a><span data-ttu-id="746b3-103">Einkaufswagenmodul</span><span class="sxs-lookup"><span data-stu-id="746b3-103">Cart module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="746b3-104">Dieses Thema enthält Einkaufsmodule und es wird beschrieben, wie diese den Sitesieten in Microsoft Dynamics 365 Commerce hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="746b3-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="746b3-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="746b3-105">Overview</span></span>

<span data-ttu-id="746b3-106">Über das Warenkorbmodul werden die Artikel angezeigt, die dem Warenkorb hinzugefügt wurden, bevor der Kunde zur Kasse geht.</span><span class="sxs-lookup"><span data-stu-id="746b3-106">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="746b3-107">Das Modul zeigt eine Bestellzusammenfassung an und der Kunde kann Werbecodes anwenden oder entfernen.</span><span class="sxs-lookup"><span data-stu-id="746b3-107">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="746b3-108">Das Einkaufskorbmodul unterstützt das Auschecken von angemeldeten Benutzern und von Gästen.</span><span class="sxs-lookup"><span data-stu-id="746b3-108">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="746b3-109">Es unterstützt auch eine Verknüpfung **Zurück zum Einkaufen**.</span><span class="sxs-lookup"><span data-stu-id="746b3-109">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="746b3-110">Sie können die Route für diesen Link unter **Seiteneinstellungen \>Erweiterungen \>Routen** konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="746b3-110">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="746b3-111">Das Warenkorbmodul rendert Daten basierend auf der Warenkorb-ID, einem auf der gesamten Site verfügbaren Browser-Cookie.</span><span class="sxs-lookup"><span data-stu-id="746b3-111">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span>

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="746b3-112">Einkaufswagenmodul-Eigenschaften und Slots</span><span class="sxs-lookup"><span data-stu-id="746b3-112">Cart module properties and slots</span></span>

<span data-ttu-id="746b3-113">Das Wagenmodul hat eine **Überschrift**-Eigenschaft, die auf Werte wie **Einkaufstasche** und **Artikel im Einkaufskorb** gesetzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="746b3-113">The cart module has a **Heading** property that can be set to values such as **Shopping bag** and **Items in your cart**.</span></span> 

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="746b3-114">Module, die im Einkaufswagenmodul verwendet werden können</span><span class="sxs-lookup"><span data-stu-id="746b3-114">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="746b3-115">**Textblock** – Dieses Modul unterstützt benutzerdefinierte Nachrichten im Einkaufswagenmodul.</span><span class="sxs-lookup"><span data-stu-id="746b3-115">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="746b3-116">Die Meldungen werden durch das Content Management-System (CMS) gesteuert.</span><span class="sxs-lookup"><span data-stu-id="746b3-116">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="746b3-117">Es können beliebige Nachrichten hinzugefügt werden wie „Für Probleme mit der Bestellung, kontaktieren Sie 1-800-Fabrikam.“</span><span class="sxs-lookup"><span data-stu-id="746b3-117">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="746b3-118">**Store-Selector** – Dieses Modul wird eine Liste von nahe gelegene Filialen anzeigen, die für eine Abholung zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="746b3-118">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="746b3-119">Hier können Benutzer einen Ort eingeben, um nach Geschäften in der Nähe zu suchen.</span><span class="sxs-lookup"><span data-stu-id="746b3-119">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="746b3-120">Weitere Informationen zu diesem Modul finden Sie unter [Auswahlmodul speichern](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="746b3-120">For more information on this module, see [Store Selector module](store-selector.md).</span></span>

## <a name="cart-module-settings"></a><span data-ttu-id="746b3-121">Einkaufswagen-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="746b3-121">Cart module settings</span></span>

<span data-ttu-id="746b3-122">Einkaufswagenmodule haben die folgenden Einstellungen, die unter **Site-Einstellungen \> Erweiterungen** konfiguriert werden können:</span><span class="sxs-lookup"><span data-stu-id="746b3-122">Cart modules have the following settings that can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="746b3-123">**Höchstmenge** – Diese Eigenschaft dient zur Angabe der maximalen Anzahl jedes Artikels, die dem Einkaufskorb hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="746b3-123">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="746b3-124">Beispielsweise kann ein Einzelhändler festlegen, dass nur 10 eines Produkts als einzelne Transaktion verkauft werden können.</span><span class="sxs-lookup"><span data-stu-id="746b3-124">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="746b3-125">**Bestandsscheck** – Wenn der Wert auf **Wahr** gesetzt ist, wird nur ein Artikel in den Einkaufskorb gelegt, nachdem das Kauffeldmodul sicherstellt, dass es auf Lager ist.</span><span class="sxs-lookup"><span data-stu-id="746b3-125">**Inventory check** – When the value is set to **True**, an item is added to the cart only after the buy box module makes sure that it's in stock.</span></span> <span data-ttu-id="746b3-126">Diesee Lagerüberprüfung wird für Szenarien ausgeführt, bei denen der Artikel versendet wird und für Szenarien, wenn der Artikel in der Filiale abgeholt wird.</span><span class="sxs-lookup"><span data-stu-id="746b3-126">This inventory check is done for scenarios where the item will be shipped and for scenarios where it will be picked up in the store.</span></span> <span data-ttu-id="746b3-127">Wenn der Wert auf **Falsch** gesetzt wird, wird kein Bestandsscheck geleistet, bevor ein Artikel in den Einkaufskorb gelegt wird und der Auftrag erteilt wird.</span><span class="sxs-lookup"><span data-stu-id="746b3-127">If the value is set to **False**, no inventory check is done before an item is added to the cart and the order is placed.</span></span>
- <span data-ttu-id="746b3-128">**Inventarpuffer** – Diese Eigenschaft wird verwendet, um eine Puffernummer für das Inventar anzugeben.</span><span class="sxs-lookup"><span data-stu-id="746b3-128">**Inventory buffer** – This property is used to specify a buffer number for inventory.</span></span> <span data-ttu-id="746b3-129">Bestandspuffer – Lagerbestand wird in Echtzeit verwaltet und wenn viele Debitoren Bestellungen aufgeben, kann es schwierig sein, die Lagerzählung zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="746b3-129">Inventory is maintained in real time, and when many customers place orders, it can be difficult to maintain an accurate inventory count.</span></span> <span data-ttu-id="746b3-130">Wenn ein Bestandsscheck erfolgt, und wenn der Bestand kleiner ist als der Pufferbetrag, wird das Produkt nicht als vorrätig behandelt.</span><span class="sxs-lookup"><span data-stu-id="746b3-130">When an inventory check is done, if the inventory is less than the buffer amount, the product is treated as out of stock.</span></span> <span data-ttu-id="746b3-131">Wenn Verkäufe rasch in mehreren Kanälen erfolgen und die Bestandszählung nicht vollständig synchronisiert wird, ist das Risiko kleiner, dass ein Artikel verkauft wird, der nicht vorrätig ist.</span><span class="sxs-lookup"><span data-stu-id="746b3-131">Therefore, when sales occur quickly through several channels, and the inventory count isn't fully synced, there is less risk that an item that is out of stock will be sold.</span></span>
- <span data-ttu-id="746b3-132">**Zurück zum Einkaufen** – Mit dieser Eigenschaft wird die Route für die Verknüpfung **Zurück zum Einkaufen** angegeben.</span><span class="sxs-lookup"><span data-stu-id="746b3-132">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="746b3-133">Die Route kann auf Site-Ebene konfiguriert werden, sodass Einzelhändler den Kunden zur Homepage oder zu einer anderen Seite der Site zurückführen können.</span><span class="sxs-lookup"><span data-stu-id="746b3-133">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="746b3-134">Commerce Scale Unit-Interaktion</span><span class="sxs-lookup"><span data-stu-id="746b3-134">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="746b3-135">Das Einkaufskorbmoduls ruft Produktinformationen mithilfe der APIs der Commerce-Skalierungseinheit ab.</span><span class="sxs-lookup"><span data-stu-id="746b3-135">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="746b3-136">Die Kennung vom Einkaufskorb vom Browsercookie wird verwendet, um die gesamte Produktinformationen der Commerce-Skalierungseinheit abzurufen.</span><span class="sxs-lookup"><span data-stu-id="746b3-136">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="746b3-137">Ein Einkaufswagenmodul einer Seite hinzufügen</span><span class="sxs-lookup"><span data-stu-id="746b3-137">Add a cart module to a page</span></span>

<span data-ttu-id="746b3-138">Um ein Einkaufswagenmodul einer neuen Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="746b3-138">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="746b3-139">Erstellen Sie ein Fragment, das mit dem Namen **Einkaufswagenfragment** bezeichnet ist und fügen Sie ein Einkaufswagenmodul dem neuen Fragment hinzu.</span><span class="sxs-lookup"><span data-stu-id="746b3-139">Create a fragment named **Cart fragment**, and add a cart module to the new fragment.</span></span>
1. <span data-ttu-id="746b3-140">Hinzufügen eines Titels zum Einkaufswagenmodul.</span><span class="sxs-lookup"><span data-stu-id="746b3-140">Add a heading to the cart module.</span></span>
1. <span data-ttu-id="746b3-141">Fügen Sie dem Einkaufswagenmodul ein Store-Selector-Modul hinzu.</span><span class="sxs-lookup"><span data-stu-id="746b3-141">Add a store selector module to the cart module.</span></span>
1. <span data-ttu-id="746b3-142">Speichern Sie das Fragment, beenden Sie die Bearbeitung und veröffentlichen Sie das Fragment.</span><span class="sxs-lookup"><span data-stu-id="746b3-142">Save the fragment, finish editing, and then publish the fragment.</span></span>
1. <span data-ttu-id="746b3-143">Erstellen Sie eine Vorlage mit der Bezeichnung **Einkaufswagenvorlage** und fügen Sie dann das Einkaufswagenfragment hinzu, das Sie soeben erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="746b3-143">Create a template named **Cart template**, and add the cart fragment that you just created.</span></span>
1. <span data-ttu-id="746b3-144">Speichern Sie die Vorlage, beenden Sie die Bearbeitung und veröffentlichen Sie die Vorlage.</span><span class="sxs-lookup"><span data-stu-id="746b3-144">Save the template, finish editing, and then publish the template.</span></span>
1. <span data-ttu-id="746b3-145">Hier können Sie eine Seite erstellen, für die die neue Vorlage verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="746b3-145">Create a page that uses the new template.</span></span>
1. <span data-ttu-id="746b3-146">Seite speichern und Vorschau anzeigen.</span><span class="sxs-lookup"><span data-stu-id="746b3-146">Save and preview the page.</span></span>
1. <span data-ttu-id="746b3-147">Beenden Sie die Bearbeitung der Seite und veröffentlichen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="746b3-147">Finish editing the page, and then publish the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="746b3-148">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="746b3-148">Additional resources</span></span>

[<span data-ttu-id="746b3-149">Starterkit-Übersicht</span><span class="sxs-lookup"><span data-stu-id="746b3-149">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="746b3-150">Containermodul</span><span class="sxs-lookup"><span data-stu-id="746b3-150">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="746b3-151">Shopauswahlmodul</span><span class="sxs-lookup"><span data-stu-id="746b3-151">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="746b3-152">Kauffeldmodul</span><span class="sxs-lookup"><span data-stu-id="746b3-152">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="746b3-153">Auschecken-Modul</span><span class="sxs-lookup"><span data-stu-id="746b3-153">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="746b3-154">Auftragsbestätigungsmodul</span><span class="sxs-lookup"><span data-stu-id="746b3-154">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="746b3-155">Kopfzeilenmodul</span><span class="sxs-lookup"><span data-stu-id="746b3-155">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="746b3-156">Fußzeilenmodul</span><span class="sxs-lookup"><span data-stu-id="746b3-156">Footer module</span></span>](author-footer-module.md)
