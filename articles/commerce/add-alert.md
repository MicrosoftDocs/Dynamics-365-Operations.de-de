---
title: Werbebanner-Modul
description: Dieses Thema enthält Werbebanner-Module und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
manager: annbe
ms.date: 04/14/2020
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
ms.openlocfilehash: 12cabbf0b8d9f337f15a8cd6cb1f2a85100b75f7
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269773"
---
# <a name="promo-banner-module"></a><span data-ttu-id="76436-103">Werbebanner-Modul</span><span class="sxs-lookup"><span data-stu-id="76436-103">Promo banner module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="76436-104">Dieses Thema enthält Werbebanner-Module und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="76436-104">This topic covers promo banner modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="76436-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="76436-105">Overview</span></span>

<span data-ttu-id="76436-106">Werbebanner-Module werden verwendet, um Informationsmeldungen auf einer Seite anzeigen.</span><span class="sxs-lookup"><span data-stu-id="76436-106">Promo banner modules are used to show inline informational messages on a page.</span></span> <span data-ttu-id="76436-107">Sie können verwendet werden, um Standort-weite Aktionen anzuzeigen, die auf allen Seiten einer E-Commerce-Webseite verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="76436-107">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="76436-108">Werbebanner-Modul unterstützen eine Textnachricht und einen Link.</span><span class="sxs-lookup"><span data-stu-id="76436-108">Promo banner modules support a text message and a link.</span></span> <span data-ttu-id="76436-109">Wenn einem Werbebanner-Modul mehrere Nachrichten hinzugefügt werden, wird es zu einem rotierenden Karussell-Banner, mit dem Kunden alle Nachrichten durchlaufen können.</span><span class="sxs-lookup"><span data-stu-id="76436-109">If multiple messages are added to a promo banner module, it becomes a rotating carousel banner that lets customers cycle through all the messages.</span></span> 

<span data-ttu-id="76436-110">Werbebanner-Module werden nach Daten des Content Management-System (CMS) gesteuert und können für jede beliebige Seite eingelagert werden.</span><span class="sxs-lookup"><span data-stu-id="76436-110">Promo banner modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a><span data-ttu-id="76436-111">Anwendungsbeispiele für Werbebanner im E-Commerce</span><span class="sxs-lookup"><span data-stu-id="76436-111">Usage examples of promo banners in e-Commerce</span></span>

<span data-ttu-id="76436-112">Werbebanner können im Site-Header verwendet werden, um Site-weite Werbeaktionen oder Nachrichten anzuzeigen, wie in den folgenden Beispielen dargestellt.</span><span class="sxs-lookup"><span data-stu-id="76436-112">Promo banners can be used in the site header to show site-wide promotions or messages, as in the following examples.</span></span>

<span data-ttu-id="76436-113">„Jahresendverkauf endet in 10 Tagen“</span><span class="sxs-lookup"><span data-stu-id="76436-113">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="76436-114">„Mit den Aktionen zum Schulbeginn viel sparen.</span><span class="sxs-lookup"><span data-stu-id="76436-114">"Save big with back to school sale.</span></span> <span data-ttu-id="76436-115">Jetzt shoppen.“</span><span class="sxs-lookup"><span data-stu-id="76436-115">Shop Now."</span></span>

## <a name="promo-banner-module-properties"></a><span data-ttu-id="76436-116">Eigenschaften von Werbebanner-Modulen</span><span class="sxs-lookup"><span data-stu-id="76436-116">Promo banner module properties</span></span>

| <span data-ttu-id="76436-117">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="76436-117">Property name</span></span>             | <span data-ttu-id="76436-118">Value</span><span class="sxs-lookup"><span data-stu-id="76436-118">Value</span></span>                              | <span data-ttu-id="76436-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="76436-119">Description</span></span> |
|---------------------------|------------------------------------|-------------|
| <span data-ttu-id="76436-120">Bannernachrichten</span><span class="sxs-lookup"><span data-stu-id="76436-120">Banner messages</span></span>           | <span data-ttu-id="76436-121">Text und Links</span><span class="sxs-lookup"><span data-stu-id="76436-121">Text and links</span></span>                     | <span data-ttu-id="76436-122">Eine Reihe von Texten und Links.</span><span class="sxs-lookup"><span data-stu-id="76436-122">An array of text and links.</span></span> |
| <span data-ttu-id="76436-123">Automatische Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="76436-123">Autoplay</span></span>                  | <span data-ttu-id="76436-124">**True** oder **False**</span><span class="sxs-lookup"><span data-stu-id="76436-124">**True** or **False**</span></span>              | <span data-ttu-id="76436-125">Ein Wert, der angibt, ob Nachrichten automatisch durchlaufen werden, wenn mehrere Nachrichten konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="76436-125">A value that indicates whether messages are automatically cycled through, if multiple messages are configured.</span></span> |
| <span data-ttu-id="76436-126">Folienübergangsintervall</span><span class="sxs-lookup"><span data-stu-id="76436-126">Slide transition interval</span></span> | <span data-ttu-id="76436-127">Eine Anzahl von Millisekunden (ms)</span><span class="sxs-lookup"><span data-stu-id="76436-127">A number of milliseconds (ms)</span></span>      | <span data-ttu-id="76436-128">Das Intervall, in dem Nachrichten durchlaufen werden.</span><span class="sxs-lookup"><span data-stu-id="76436-128">The interval that is used to cycle through messages.</span></span> |
| <span data-ttu-id="76436-129">Ausblenden zulassen</span><span class="sxs-lookup"><span data-stu-id="76436-129">Allow dismiss</span></span>             | <span data-ttu-id="76436-130">**True** oder **False**</span><span class="sxs-lookup"><span data-stu-id="76436-130">**True** or **False**</span></span>              | <span data-ttu-id="76436-131">Wenn der Wert auf **True** gesetzt wird, können Debitoren die Warnung ablehnen.</span><span class="sxs-lookup"><span data-stu-id="76436-131">If the value is set to **True**, customers can dismiss the alert.</span></span> |
| <span data-ttu-id="76436-132">Karussellflipper anzeigen</span><span class="sxs-lookup"><span data-stu-id="76436-132">Show carousel flipper</span></span>     | <span data-ttu-id="76436-133">**True** oder **False**</span><span class="sxs-lookup"><span data-stu-id="76436-133">**True** or **False**</span></span>              | <span data-ttu-id="76436-134">Ein Wert, der angibt, ob die Karussellflipper angezeigt werden sollen, damit Debitoren mehrere Bannerelemente manuell durchlaufen können.</span><span class="sxs-lookup"><span data-stu-id="76436-134">A value that indicates whether the carousel flippers should be shown, so that customers can manually cycle through multiple banner items.</span></span> |
| <span data-ttu-id="76436-135">Textausrichtung</span><span class="sxs-lookup"><span data-stu-id="76436-135">Text alignment</span></span>            | <span data-ttu-id="76436-136">**Rechts** **Links** **Zentriert**</span><span class="sxs-lookup"><span data-stu-id="76436-136">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="76436-137">Die Textausrichtung im Werbebanner-Modul.</span><span class="sxs-lookup"><span data-stu-id="76436-137">The text alignment in the promo banner module.</span></span> |
| <span data-ttu-id="76436-138">Verknüpfung</span><span class="sxs-lookup"><span data-stu-id="76436-138">Link</span></span>                      | <span data-ttu-id="76436-139">Eine URL</span><span class="sxs-lookup"><span data-stu-id="76436-139">A URL</span></span>                              | <span data-ttu-id="76436-140">Die URL für einen optionalen Link.</span><span class="sxs-lookup"><span data-stu-id="76436-140">The URL for an optional link.</span></span> |

## <a name="add-a-promo-banner-module-to-a-page"></a><span data-ttu-id="76436-141">Ein Werbebanner-Modul einer neuen Seite hinzufügen</span><span class="sxs-lookup"><span data-stu-id="76436-141">Add a promo banner module to a page</span></span> 

<span data-ttu-id="76436-142">Um ein Werbebanner-Modul einer neuen Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="76436-142">To add a promo banner module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="76436-143">Wählen Sie **Neu** aus, um eine Seitenvorlage zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="76436-143">Select **New** to create a page template.</span></span>
1. <span data-ttu-id="76436-144">Im Dialogfeld **Neue Vorlage** unter **Vorlagenname** geben Sie **Werbebanner-Vorlage** ein und wählen **OK**.</span><span class="sxs-lookup"><span data-stu-id="76436-144">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="76436-145">Unter **Seitengliederung** fügen Sie ein Modul **Standardseite** zum Slot **Text** hinzu.</span><span class="sxs-lookup"><span data-stu-id="76436-145">Under **Page Outline**, add a **Default page** module to the **Body** slot.</span></span> 
1. <span data-ttu-id="76436-146">Wählen **Bearbeiten beenden**, um die Vorlage einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="76436-146">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 
1. <span data-ttu-id="76436-147">Verwenden Sie die Vorlage, die Sie soeben erstellt haben, um die Seite zu erstellen, die die Bezeichnung **Werbebanner-Seite** hat.</span><span class="sxs-lookup"><span data-stu-id="76436-147">Use the template that you just created to create a page that is named **Promo banner page**.</span></span> 
1. <span data-ttu-id="76436-148">Im **Haupt-** Slot der neuen Seite fügen Sie ein Containermodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="76436-148">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="76436-149">Stellen Sie im rechten Bereich den Wert **Breite** auf **Behälter füllen** ein.</span><span class="sxs-lookup"><span data-stu-id="76436-149">In the pane on the right, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="76436-150">Fügen Sie unter **Seitengliederung** dem Containermodul ein Werbebanner-Modul hinzu.</span><span class="sxs-lookup"><span data-stu-id="76436-150">Under **Page Outline**, add a promo banner module to the container module.</span></span>
1. <span data-ttu-id="76436-151">Fügen Sie in den Einstellungen für das Banner-Modul eine oder mehrere Banner-Nachrichten hinzu.</span><span class="sxs-lookup"><span data-stu-id="76436-151">In the settings for the banner module, add one or more banner messages.</span></span> <span data-ttu-id="76436-152">Jede Nachricht kann Text zusammen mit einem Link enthalten.</span><span class="sxs-lookup"><span data-stu-id="76436-152">Each message can have text together with a link.</span></span> <span data-ttu-id="76436-153">Sie können die anderen Eigenschaften bearbeiten, um das Modul weiter anzupassen.</span><span class="sxs-lookup"><span data-stu-id="76436-153">You can edit the other properties to customize the module further.</span></span>
1. <span data-ttu-id="76436-154">Wählen **Speichern** und dann **Vorschau** aus, um eine Vorschau der Seite anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="76436-154">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="76436-155">Am oberen Rand der Seite sollten Sie eine Warnung sehen, die den von Ihnen hinzugefügten Text anzeigt.</span><span class="sxs-lookup"><span data-stu-id="76436-155">At the top of the page, you should see an alert that shows the text that you added.</span></span>
1. <span data-ttu-id="76436-156">Wählen **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="76436-156">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> 

> [!NOTE]
> <span data-ttu-id="76436-157">Ein Werbebanner wird normalerweise im Seitenkopf- oder Untertitel-Slot verwendet.</span><span class="sxs-lookup"><span data-stu-id="76436-157">A promo banner is typically used in the page header slot or a subheader slot.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="76436-158">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="76436-158">Additional resources</span></span>

[<span data-ttu-id="76436-159">Starterkit-Übersicht</span><span class="sxs-lookup"><span data-stu-id="76436-159">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="76436-160">Karussellmodul</span><span class="sxs-lookup"><span data-stu-id="76436-160">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="76436-161">Textblock-Modul</span><span class="sxs-lookup"><span data-stu-id="76436-161">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="76436-162">Inhaltsblockmodul</span><span class="sxs-lookup"><span data-stu-id="76436-162">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="76436-163">Video-Player-Modul</span><span class="sxs-lookup"><span data-stu-id="76436-163">Video player module</span></span>](add-video-player.md)
