---
title: Werbebanner-Modul
description: Dieses Thema behandelt Werbebanner-Module und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: be3cc9729b58fce9ebc9885d8cb20b63114362a0
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796245"
---
# <a name="promo-banner-module"></a><span data-ttu-id="387d0-103">Werbebannermodul</span><span class="sxs-lookup"><span data-stu-id="387d0-103">Promo banner module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="387d0-104">Dieses Thema behandelt Werbebanner-Module und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="387d0-104">This topic covers promo banner modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="387d0-105">Werbebanner-Module werden verwendet, um Informationsmeldungen auf einer Seite anzeigen.</span><span class="sxs-lookup"><span data-stu-id="387d0-105">Promo banner modules are used to show inline informational messages on a page.</span></span> <span data-ttu-id="387d0-106">Sie können verwendet werden, um Standort-weite Aktionen anzuzeigen, die auf allen Seiten einer E-Commerce-Webseite verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="387d0-106">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="387d0-107">Werbebanner-Modul unterstützen eine Textnachricht und einen Link.</span><span class="sxs-lookup"><span data-stu-id="387d0-107">Promo banner modules support a text message and a link.</span></span> <span data-ttu-id="387d0-108">Wenn einem Werbebanner-Modul mehrere Nachrichten hinzugefügt werden, wird es zu einem rotierenden Karussell-Banner, mit dem Kunden alle Nachrichten durchlaufen können.</span><span class="sxs-lookup"><span data-stu-id="387d0-108">If multiple messages are added to a promo banner module, it becomes a rotating carousel banner that lets customers cycle through all the messages.</span></span> 

<span data-ttu-id="387d0-109">Werbebanner-Module werden nach Daten des Content Management-System (CMS) gesteuert und können für jede beliebige Seite eingelagert werden.</span><span class="sxs-lookup"><span data-stu-id="387d0-109">Promo banner modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a><span data-ttu-id="387d0-110">Anwendungsbeispiele für Werbebanner im E-Commerce</span><span class="sxs-lookup"><span data-stu-id="387d0-110">Usage examples of promo banners in e-Commerce</span></span>

<span data-ttu-id="387d0-111">Werbebanner können im Site-Header verwendet werden, um Site-weite Werbeaktionen oder Nachrichten anzuzeigen, wie in den folgenden Beispielen dargestellt.</span><span class="sxs-lookup"><span data-stu-id="387d0-111">Promo banners can be used in the site header to show site-wide promotions or messages, as in the following examples.</span></span>

<span data-ttu-id="387d0-112">„Jahresendverkauf endet in 10 Tagen“</span><span class="sxs-lookup"><span data-stu-id="387d0-112">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="387d0-113">„Mit den Aktionen zum Schulbeginn viel sparen.</span><span class="sxs-lookup"><span data-stu-id="387d0-113">"Save big with back to school sale.</span></span> <span data-ttu-id="387d0-114">Jetzt shoppen.“</span><span class="sxs-lookup"><span data-stu-id="387d0-114">Shop Now."</span></span>

<span data-ttu-id="387d0-115">Für Thanksgiving SALE! shoppen</span><span class="sxs-lookup"><span data-stu-id="387d0-115">"Shop for Thanksgiving SALE!"</span></span> 

<span data-ttu-id="387d0-116">Das folgende Bild zeigt ein Beispiel für eine Werbeanzeige.</span><span class="sxs-lookup"><span data-stu-id="387d0-116">The following image shows an example of a promo banner.</span></span>

![Beispiel eines Werbe-Anzeige-Moduls](./media/ecommerce-Promobanner.PNG)

## <a name="promo-banner-module-properties"></a><span data-ttu-id="387d0-118">Eigenschaften von Werbebanner-Modulen</span><span class="sxs-lookup"><span data-stu-id="387d0-118">Promo banner module properties</span></span>

| <span data-ttu-id="387d0-119">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="387d0-119">Property name</span></span>             | <span data-ttu-id="387d0-120">Wert</span><span class="sxs-lookup"><span data-stu-id="387d0-120">Value</span></span>                              | <span data-ttu-id="387d0-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="387d0-121">Description</span></span> |
|---------------------------|------------------------------------|-------------|
| <span data-ttu-id="387d0-122">Bannernachrichten</span><span class="sxs-lookup"><span data-stu-id="387d0-122">Banner messages</span></span>           | <span data-ttu-id="387d0-123">Text und Links</span><span class="sxs-lookup"><span data-stu-id="387d0-123">Text and links</span></span>                     | <span data-ttu-id="387d0-124">Eine Reihe von Texten und Links.</span><span class="sxs-lookup"><span data-stu-id="387d0-124">An array of text and links.</span></span> |
| <span data-ttu-id="387d0-125">Automatische Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="387d0-125">Autoplay</span></span>                  | <span data-ttu-id="387d0-126">**True** oder **False**</span><span class="sxs-lookup"><span data-stu-id="387d0-126">**True** or **False**</span></span>              | <span data-ttu-id="387d0-127">Ein Wert, der angibt, ob Nachrichten automatisch durchlaufen werden, wenn mehrere Nachrichten konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="387d0-127">A value that indicates whether messages are automatically cycled through, if multiple messages are configured.</span></span> |
| <span data-ttu-id="387d0-128">Folienübergangsintervall</span><span class="sxs-lookup"><span data-stu-id="387d0-128">Slide transition interval</span></span> | <span data-ttu-id="387d0-129">Eine Anzahl von Millisekunden (ms)</span><span class="sxs-lookup"><span data-stu-id="387d0-129">A number of milliseconds (ms)</span></span>      | <span data-ttu-id="387d0-130">Das Intervall, in dem Nachrichten durchlaufen werden.</span><span class="sxs-lookup"><span data-stu-id="387d0-130">The interval that is used to cycle through messages.</span></span> |
| <span data-ttu-id="387d0-131">Ausblenden zulassen</span><span class="sxs-lookup"><span data-stu-id="387d0-131">Allow dismiss</span></span>             | <span data-ttu-id="387d0-132">**True** oder **False**</span><span class="sxs-lookup"><span data-stu-id="387d0-132">**True** or **False**</span></span>              | <span data-ttu-id="387d0-133">Wenn der Wert auf **True** gesetzt wird, können Debitoren die Warnung ablehnen.</span><span class="sxs-lookup"><span data-stu-id="387d0-133">If the value is set to **True**, customers can dismiss the alert.</span></span> |
| <span data-ttu-id="387d0-134">Karussellflipper anzeigen</span><span class="sxs-lookup"><span data-stu-id="387d0-134">Show carousel flipper</span></span>     | <span data-ttu-id="387d0-135">**True** oder **False**</span><span class="sxs-lookup"><span data-stu-id="387d0-135">**True** or **False**</span></span>              | <span data-ttu-id="387d0-136">Ein Wert, der angibt, ob die Karussellflipper angezeigt werden sollen, damit Debitoren mehrere Bannerelemente manuell durchlaufen können.</span><span class="sxs-lookup"><span data-stu-id="387d0-136">A value that indicates whether the carousel flippers should be shown, so that customers can manually cycle through multiple banner items.</span></span> |
| <span data-ttu-id="387d0-137">Textausrichtung</span><span class="sxs-lookup"><span data-stu-id="387d0-137">Text alignment</span></span>            | <span data-ttu-id="387d0-138">**Rechts** **Links** **Zentriert**</span><span class="sxs-lookup"><span data-stu-id="387d0-138">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="387d0-139">Die Textausrichtung im Werbebanner-Modul.</span><span class="sxs-lookup"><span data-stu-id="387d0-139">The text alignment in the promo banner module.</span></span> |
| <span data-ttu-id="387d0-140">Verknüpfung</span><span class="sxs-lookup"><span data-stu-id="387d0-140">Link</span></span>                      | <span data-ttu-id="387d0-141">Eine URL</span><span class="sxs-lookup"><span data-stu-id="387d0-141">A URL</span></span>                              | <span data-ttu-id="387d0-142">Die URL für einen optionalen Link.</span><span class="sxs-lookup"><span data-stu-id="387d0-142">The URL for an optional link.</span></span> |

## <a name="add-a-promo-banner-module-to-a-page"></a><span data-ttu-id="387d0-143">Ein Werbebanner-Modul einer neuen Seite hinzufügen</span><span class="sxs-lookup"><span data-stu-id="387d0-143">Add a promo banner module to a page</span></span> 

<span data-ttu-id="387d0-144">Um ein Werbebanner-Modul einer neuen Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="387d0-144">To add a promo banner module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="387d0-145">Wechseln Sie zu **Vorlagen** und wählen Sie **Neu** aus, um eine neue Vorlage zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="387d0-145">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="387d0-146">Im Dialogfeld **Neue Vorlage** unter **Vorlagenname** geben Sie **Werbebanner-Vorlage** ein und wählen **OK**.</span><span class="sxs-lookup"><span data-stu-id="387d0-146">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="387d0-147">Unter **Seitengliederung** fügen Sie ein Modul **Standardseite** zum Slot **Text** hinzu.</span><span class="sxs-lookup"><span data-stu-id="387d0-147">Under **Page Outline**, add a **Default page** module to the **Body** slot.</span></span> 
1. <span data-ttu-id="387d0-148">Wählen **Bearbeiten beenden**, um die Vorlage einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="387d0-148">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 
1. <span data-ttu-id="387d0-149">Verwenden Sie die Vorlage, die Sie soeben erstellt haben, um die Seite zu erstellen, die die Bezeichnung **Werbebanner-Seite** hat.</span><span class="sxs-lookup"><span data-stu-id="387d0-149">Use the template that you just created to create a page that is named **Promo banner page**.</span></span> 
1. <span data-ttu-id="387d0-150">Im **Haupt-** Slot der neuen Seite fügen Sie ein Containermodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="387d0-150">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="387d0-151">Stellen Sie im rechten Bereich den Wert **Breite** auf **Behälter füllen** ein.</span><span class="sxs-lookup"><span data-stu-id="387d0-151">In the pane on the right, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="387d0-152">Fügen Sie unter **Seitengliederung** dem Containermodul ein Werbebanner-Modul hinzu.</span><span class="sxs-lookup"><span data-stu-id="387d0-152">Under **Page Outline**, add a promo banner module to the container module.</span></span>
1. <span data-ttu-id="387d0-153">Fügen Sie in den Einstellungen für das Banner-Modul eine oder mehrere Banner-Nachrichten hinzu.</span><span class="sxs-lookup"><span data-stu-id="387d0-153">In the settings for the banner module, add one or more banner messages.</span></span> <span data-ttu-id="387d0-154">Jede Nachricht kann Text zusammen mit einem Link enthalten.</span><span class="sxs-lookup"><span data-stu-id="387d0-154">Each message can have text together with a link.</span></span> <span data-ttu-id="387d0-155">Sie können die anderen Eigenschaften bearbeiten, um das Modul weiter anzupassen.</span><span class="sxs-lookup"><span data-stu-id="387d0-155">You can edit the other properties to customize the module further.</span></span>
1. <span data-ttu-id="387d0-156">Wählen **Speichern** und dann **Vorschau** aus, um eine Vorschau der Seite anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="387d0-156">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="387d0-157">Am oberen Rand der Seite sollten Sie eine Warnung sehen, die den von Ihnen hinzugefügten Text anzeigt.</span><span class="sxs-lookup"><span data-stu-id="387d0-157">At the top of the page, you should see an alert that shows the text that you added.</span></span>
1. <span data-ttu-id="387d0-158">Wählen **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="387d0-158">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="387d0-159">Ein Werbebanner wird normalerweise im Seitenkopf- oder Untertitel-Slot verwendet.</span><span class="sxs-lookup"><span data-stu-id="387d0-159">A promo banner is typically used in the page header slot or a subheader slot.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="387d0-160">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="387d0-160">Additional resources</span></span>

[<span data-ttu-id="387d0-161">Übersicht über die Modulbibliothek</span><span class="sxs-lookup"><span data-stu-id="387d0-161">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="387d0-162">Karussellmodul</span><span class="sxs-lookup"><span data-stu-id="387d0-162">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="387d0-163">Textblockmodul</span><span class="sxs-lookup"><span data-stu-id="387d0-163">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="387d0-164">Inhaltsblockmodul</span><span class="sxs-lookup"><span data-stu-id="387d0-164">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="387d0-165">Video-Player-Modul</span><span class="sxs-lookup"><span data-stu-id="387d0-165">Video player module</span></span>](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]