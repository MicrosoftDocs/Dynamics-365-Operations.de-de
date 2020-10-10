---
title: Einkaufswagenmodul
description: Dieses Thema enthält Einkaufsmodule und es wird beschrieben, wie diese den Sitesieten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
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
ms.openlocfilehash: d9a15f85838849796d6ce4674712636251c75bf3
ms.sourcegitcommit: 97ceb24f191161ca601e0889a539df665834ac3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2020
ms.locfileid: "3818274"
---
# <a name="cart-module"></a><span data-ttu-id="93229-103">Einkaufswagenmodul</span><span class="sxs-lookup"><span data-stu-id="93229-103">Cart module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="93229-104">Dieses Thema enthält Einkaufsmodule und es wird beschrieben, wie diese den Sitesieten in Microsoft Dynamics 365 Commerce hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="93229-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="93229-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="93229-105">Overview</span></span>

<span data-ttu-id="93229-106">Über das Warenkorbmodul werden die Artikel angezeigt, die dem Warenkorb hinzugefügt wurden, bevor der Kunde zur Kasse geht.</span><span class="sxs-lookup"><span data-stu-id="93229-106">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="93229-107">Das Modul zeigt eine Bestellzusammenfassung an und der Kunde kann Werbecodes anwenden oder entfernen.</span><span class="sxs-lookup"><span data-stu-id="93229-107">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="93229-108">Das Einkaufskorbmodul unterstützt das Auschecken von angemeldeten Benutzern und von Gästen.</span><span class="sxs-lookup"><span data-stu-id="93229-108">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="93229-109">Es unterstützt auch eine Verknüpfung **Zurück zum Einkaufen**.</span><span class="sxs-lookup"><span data-stu-id="93229-109">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="93229-110">Sie können die Route für diesen Link unter **Seiteneinstellungen \> Erweiterungen \> Routen** konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="93229-110">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="93229-111">Das Warenkorbmodul rendert Daten basierend auf der Warenkorb-ID, einem auf der gesamten Site verfügbaren Browser-Cookie.</span><span class="sxs-lookup"><span data-stu-id="93229-111">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span> 

<span data-ttu-id="93229-112">Das folgende Bild zeigt ein Beispiel einer Warenkorbseite auf der Fabrikam-Site.</span><span class="sxs-lookup"><span data-stu-id="93229-112">The following image shows an example of a cart page on the Fabrikam site.</span></span>

![Beispiel eines Einkaufskorbmoduls auf der Fabrikam-Site](./media/cart2.PNG)

<span data-ttu-id="93229-114">Das folgende Bild zeigt ein Beispiel einer Warenkorbseite auf der Fabrikam-Site.</span><span class="sxs-lookup"><span data-stu-id="93229-114">The following image shows an example of a cart page on the Fabrikam site.</span></span> <span data-ttu-id="93229-115">In diesem Beispiel wird eine Bearbeitungsgebühr für eine Position fällig.</span><span class="sxs-lookup"><span data-stu-id="93229-115">In this example, there is a handling fee for a line item.</span></span>

![Beispiel eines Einkaufskorbmoduls mit einer Bearbeitungsgebühr für einen Positionsartikel](./media/ecommerce-handling-fee.png)

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="93229-117">Einkaufswagenmodul-Eigenschaften und Slots</span><span class="sxs-lookup"><span data-stu-id="93229-117">Cart module properties and slots</span></span>

| <span data-ttu-id="93229-118">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="93229-118">Property</span></span> | <span data-ttu-id="93229-119">Werte</span><span class="sxs-lookup"><span data-stu-id="93229-119">Values</span></span> | <span data-ttu-id="93229-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="93229-120">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="93229-121">Überschrift</span><span class="sxs-lookup"><span data-stu-id="93229-121">Heading</span></span> | <span data-ttu-id="93229-122">Überschriftentext und eine Überschriftsmarkierung (**H1**, **H2**, **H3**, **H4**, **H5** oder **H6**)</span><span class="sxs-lookup"><span data-stu-id="93229-122">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="93229-123">Eine Überschrift für den Einkaufskorb wie "Einkaufstasche" oder "Artikel in Ihrem Korb".</span><span class="sxs-lookup"><span data-stu-id="93229-123">A heading for the cart, such as "Shopping bag" or "Items in your cart."</span></span> |
| <span data-ttu-id="93229-124">Fehlermeldungen "Nicht vorrätig" anzeigen</span><span class="sxs-lookup"><span data-stu-id="93229-124">Show out of stock errors</span></span> | <span data-ttu-id="93229-125">**True** oder **False**</span><span class="sxs-lookup"><span data-stu-id="93229-125">**True** or **False**</span></span> | <span data-ttu-id="93229-126">Wenn diese Eigenschaft **True** ist, zeigt die Warenkorbseite Bestandsfehler an.</span><span class="sxs-lookup"><span data-stu-id="93229-126">If this property is set to **True**, the cart page will show stock-related errors.</span></span> <span data-ttu-id="93229-127">Wir empfehlen, dass Sie für diese Eigenschaft **True** festlegen, wenn Bestandsprüfungen auf die Website angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="93229-127">We recommend that you set this property to **True** if inventory checks are applied on the site.</span></span> |
| <span data-ttu-id="93229-128">Versandkosten für Positionsartikel anzeigen</span><span class="sxs-lookup"><span data-stu-id="93229-128">Show shipping charges for line items</span></span> | <span data-ttu-id="93229-129">**True** oder **False**</span><span class="sxs-lookup"><span data-stu-id="93229-129">**True** or **False**</span></span> | <span data-ttu-id="93229-130">Wenn diese Eigenschaft **True** ist, enthalten Warenkorbpositionen die Versandkosten, wenn diese Angabe verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="93229-130">If this property is set to **True**, cart line items will show the shipping charges, if this information is available.</span></span> <span data-ttu-id="93229-131">Diese Funktion wird im Fabrikam-Design nicht unterstützt, da Benutzer den Versand nur im Auschecken-Ablauf auswählen.</span><span class="sxs-lookup"><span data-stu-id="93229-131">This feature isn't supported in the Fabrikam theme, because users select shipping only in the checkout flow.</span></span> <span data-ttu-id="93229-132">Diese Funktion kann jedoch gegebenenfalls in anderen Workflows aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="93229-132">However, this feature can be turned on in other workflows if it's applicable.</span></span> |

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="93229-133">Module, die im Einkaufswagenmodul verwendet werden können</span><span class="sxs-lookup"><span data-stu-id="93229-133">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="93229-134">**Textblock** – Dieses Modul unterstützt benutzerdefinierte Nachrichten im Einkaufswagenmodul.</span><span class="sxs-lookup"><span data-stu-id="93229-134">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="93229-135">Die Meldungen werden durch das Content Management-System (CMS) gesteuert.</span><span class="sxs-lookup"><span data-stu-id="93229-135">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="93229-136">Es können beliebige Nachrichten hinzugefügt werden wie „Für Probleme mit der Bestellung, kontaktieren Sie 1-800-Fabrikam.“</span><span class="sxs-lookup"><span data-stu-id="93229-136">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="93229-137">**Store-Selector** – Dieses Modul wird eine Liste von nahe gelegene Filialen anzeigen, die für eine Abholung zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="93229-137">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="93229-138">Hier können Benutzer einen Ort eingeben, um nach Geschäften in der Nähe zu suchen.</span><span class="sxs-lookup"><span data-stu-id="93229-138">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="93229-139">Weitere Informationen zu diesem Modul finden Sie unter [Auswahlmodul speichern](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="93229-139">For more information on this module, see [Store selector module](store-selector.md).</span></span>

## <a name="module-properties"></a><span data-ttu-id="93229-140">Moduleigenschaften</span><span class="sxs-lookup"><span data-stu-id="93229-140">Module properties</span></span>

<span data-ttu-id="93229-141">Die folgenden Warenkorbmoduleigenschaften können unter **Site-Einstellungen \> Erweiterungen** konfiguriert werden:</span><span class="sxs-lookup"><span data-stu-id="93229-141">The following cart module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="93229-142">**Höchstmenge** – Diese Eigenschaft dient zur Angabe der maximalen Anzahl jedes Artikels, die dem Einkaufskorb hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="93229-142">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="93229-143">Beispielsweise kann ein Einzelhändler festlegen, dass nur 10 eines Produkts als einzelne Transaktion verkauft werden können.</span><span class="sxs-lookup"><span data-stu-id="93229-143">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="93229-144">**Bestand** – Informationen zum Anwenden von Bestandeinstellungen finden Sie unter [Wenden Sie Bestandeinstellungen an](inventory-settings.md).</span><span class="sxs-lookup"><span data-stu-id="93229-144">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="93229-145">**Zurück zum Einkaufen** – Mit dieser Eigenschaft wird die Route für die Verknüpfung **Zurück zum Einkaufen** angegeben.</span><span class="sxs-lookup"><span data-stu-id="93229-145">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="93229-146">Die Route kann auf Site-Ebene konfiguriert werden, sodass Einzelhändler den Kunden zur Homepage oder zu einer anderen Seite der Site zurückführen können.</span><span class="sxs-lookup"><span data-stu-id="93229-146">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="93229-147">Commerce Scale Unit-Interaktion</span><span class="sxs-lookup"><span data-stu-id="93229-147">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="93229-148">Das Einkaufskorbmoduls ruft Produktinformationen mithilfe der APIs der Commerce-Skalierungseinheit ab.</span><span class="sxs-lookup"><span data-stu-id="93229-148">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="93229-149">Die Kennung vom Einkaufskorb vom Browsercookie wird verwendet, um die gesamte Produktinformationen der Commerce-Skalierungseinheit abzurufen.</span><span class="sxs-lookup"><span data-stu-id="93229-149">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="93229-150">Ein Einkaufswagenmodul einer Seite hinzufügen</span><span class="sxs-lookup"><span data-stu-id="93229-150">Add a cart module to a page</span></span>

<span data-ttu-id="93229-151">Um ein Einkaufswagenmodul einer neuen Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="93229-151">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="93229-152">Wechseln Sie zu **Fragmente** und wählen Sie **Neu** aus, um ein neues Fragment zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="93229-152">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="93229-153">Wählen Sie im Dialogfeld **Neues Fragment** das Modul **Einkaufskorb** aus.</span><span class="sxs-lookup"><span data-stu-id="93229-153">In the **New fragment** dialog box, select the **Cart** module.</span></span>
1. <span data-ttu-id="93229-154">Geben Sie unter **Name des Fragments** den Namen **Einkaufswagenfragment** ein und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="93229-154">Under **Fragment name**, enter the name **Cart fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="93229-155">Wählen Sie den Slot **Warenkorb** aus.</span><span class="sxs-lookup"><span data-stu-id="93229-155">Select the **Cart** slot.</span></span>
1. <span data-ttu-id="93229-156">Wählen Sie im Eigenschaftenbereich rechts das Stiftsymbol aus, geben Sie den Überschriftentext in das Feld ein und wählen Sie dann das Häkchensymbol aus.</span><span class="sxs-lookup"><span data-stu-id="93229-156">In the properties pane on the right, select the pencil symbol, enter heading text in the field, and then select the check mark symbol.</span></span>
1. <span data-ttu-id="93229-157">Wählen Sie im Slot **Warenkorb** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="93229-157">In the **Cart** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="93229-158">Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Auswahl speichern** und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="93229-158">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="93229-159">Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um das Fragment einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="93229-159">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="93229-160">Wechseln Sie zu **Vorlagen** und wählen Sie **Neu** aus, um eine neue Vorlage zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="93229-160">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="93229-161">Im Dialogfeld **Neue Vorlage** unter Vorlagenname geben Sie einen Namen für die neue **Vorlage** ein und wählen OK.</span><span class="sxs-lookup"><span data-stu-id="93229-161">In the **New Template** dialog box, under **Template name**, enter a name for the template.</span></span>
1. <span data-ttu-id="93229-162">Wählen Sie in der Gliederungsstruktur den Slot **Text**, die Ellipsen-Schaltfläche (**...**) und dann **Fragment hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="93229-162">In the outline tree, select the **Body** slot, select the ellipsis (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="93229-163">Wählen Sie im Dialogfeld **Fragment auswählen** das Fragment **Warenkorbfragment** und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="93229-163">In the **Select fragment** dialog box, select the **Cart fragment** fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="93229-164">Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Vorlage einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="93229-164">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="93229-165">Wechseln Sie zu **Seiten**, und wählen Sie dann **Neu** aus, um eine neue Seite zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="93229-165">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="93229-166">Im Dialogfeld **Vorlage auswählen** wählen Sie die Vorlage, die Sie zuvor erstellt haben, und geben einen Namen ein und wählen dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="93229-166">In the **Choose a template** dialog box, select the template that you created, enter a page name, and then select **OK**.</span></span>
1. <span data-ttu-id="93229-167">Wählen **Speichern** und dann **Vorschau** aus, um eine Vorschau der Seite anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="93229-167">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="93229-168">Wählen **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="93229-168">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="93229-169">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="93229-169">Additional resources</span></span>

[<span data-ttu-id="93229-170">Modul für Einkaufswagensymbol</span><span class="sxs-lookup"><span data-stu-id="93229-170">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="93229-171">Auschecken-Modul</span><span class="sxs-lookup"><span data-stu-id="93229-171">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="93229-172">Zahlungsmodul</span><span class="sxs-lookup"><span data-stu-id="93229-172">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="93229-173">Versandadressmodul</span><span class="sxs-lookup"><span data-stu-id="93229-173">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="93229-174">Lieferoptionsmodul</span><span class="sxs-lookup"><span data-stu-id="93229-174">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="93229-175">Auftragsdetailmodul</span><span class="sxs-lookup"><span data-stu-id="93229-175">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="93229-176">Geschenkkartenmodul</span><span class="sxs-lookup"><span data-stu-id="93229-176">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="93229-177">Lagerverfügbarkeit für Retail Channels berechnen</span><span class="sxs-lookup"><span data-stu-id="93229-177">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)
