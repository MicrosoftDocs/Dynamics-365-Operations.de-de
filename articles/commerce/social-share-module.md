---
title: Social-Share-Modul
description: Dieses Thema enthält Social-Share-Module und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
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
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 0fd81aa1f4b1358528f0135c1334dc7b4ac4461f
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761392"
---
# <a name="social-share-module"></a><span data-ttu-id="2f7fb-103">Social-Share-Modul</span><span class="sxs-lookup"><span data-stu-id="2f7fb-103">Social share module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="2f7fb-104">Dieses Thema enthält Social-Share-Module und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="2f7fb-104">This topic covers social share modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2f7fb-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="2f7fb-105">Overview</span></span>

<span data-ttu-id="2f7fb-106">Mithilfe von Social-Share-Modulen können Benutzer URLs von E-Commerce-Websiteseiten in sozialen Medien wie z. B. Facebook, Twitter, Pinterest und LinkedIn verwenden.</span><span class="sxs-lookup"><span data-stu-id="2f7fb-106">Social share modules allow users to share e-Commerce site page URLs on social media such as Facebook, Twitter, Pinterest, and LinkedIn.</span></span> <span data-ttu-id="2f7fb-107">Webite-Seiten-URLs können auch per E-Mail freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2f7fb-107">Site page URLs can also be shared via email.</span></span> <span data-ttu-id="2f7fb-108">Social-Share-Module werden häufig auf Produktdetailseiten (PDPs) verwendet, um Benutzern den Austausch von Produktinformationen zu erleichtern.</span><span class="sxs-lookup"><span data-stu-id="2f7fb-108">Social share modules are commonly used on product details pages (PDPs) to help users share product information.</span></span>

<span data-ttu-id="2f7fb-109">Jedes Social-Share-Modul ist ein Container für Social-Share-Artieklmodule.</span><span class="sxs-lookup"><span data-stu-id="2f7fb-109">Each social share module is a container for social share item modules.</span></span> <span data-ttu-id="2f7fb-110">Jedes Social-Share-Artikelmodul kann so konfiguriert werden, dass es auf eine bestimmte Social-Media-Website verweist.</span><span class="sxs-lookup"><span data-stu-id="2f7fb-110">Each social share item module can be configured to point to a specific social media site.</span></span> <span data-ttu-id="2f7fb-111">Integration in Facebook, Twitter, Pinterest, LinkedIn und E-Mail wird sofort unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2f7fb-111">Integration with Facebook, Twitter, Pinterest, LinkedIn, and email is supported out of the box.</span></span> <span data-ttu-id="2f7fb-112">Wenn ein Website-Benutzer ein Social-Media-Symbol auswählt, wird ein HTML-IFrame für die jeweilige Social-Media-Website gestartet.</span><span class="sxs-lookup"><span data-stu-id="2f7fb-112">When a site user selects a social media symbol, an HTML iframe is launched for the respective social media site.</span></span> <span data-ttu-id="2f7fb-113">Innerhalb des IFrames kann sich der Benutzer anmelden und den angezeigten Seiteninhalt veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="2f7fb-113">Within the iframe, the user can sign in and post the page content that they were viewing.</span></span>

<span data-ttu-id="2f7fb-114">Jede Social-Media-Plattform kann Cookies verfolgen. Daher müssen Benutzer der Website für dieses Modul die Benachrichtigung über die Zustimmung zur Cookie-Zustimmung akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="2f7fb-114">Each social media platform may track cookies, so this module requires site users to accept the cookie consent notification message.</span></span> <span data-ttu-id="2f7fb-115">Wenn die Zustimmung zum Cookie nicht akzeptiert wird, wird das Modul auf der Seite ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="2f7fb-115">When cookie consent is not accepted, the module will be hidden on the page.</span></span> <span data-ttu-id="2f7fb-116">Weitere Informationen finden Sie unter [Cookie-Compliance](cookie-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="2f7fb-116">For more information, see [Cookie compliance](cookie-compliance.md).</span></span>

<span data-ttu-id="2f7fb-117">Die folgende Abbildung zeigt ein Beispiel für ein Social-Share-Modul, das auf einer Produktdetailseite verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2f7fb-117">The following illustration highlights an example of a social share module used on a product details page.</span></span>

![Beispiel eines Social-Share-Moduls](./media/ecommerce-socialshare.png)

## <a name="social-share-module-properties"></a><span data-ttu-id="2f7fb-119">Social-Share-Moduleigenschaften</span><span class="sxs-lookup"><span data-stu-id="2f7fb-119">Social share module properties</span></span>

| <span data-ttu-id="2f7fb-120">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="2f7fb-120">Property name</span></span>             | <span data-ttu-id="2f7fb-121">Wert</span><span class="sxs-lookup"><span data-stu-id="2f7fb-121">Value</span></span>                 | <span data-ttu-id="2f7fb-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2f7fb-122">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="2f7fb-123">Beschriftung</span><span class="sxs-lookup"><span data-stu-id="2f7fb-123">Caption</span></span>                  | <span data-ttu-id="2f7fb-124">Text</span><span class="sxs-lookup"><span data-stu-id="2f7fb-124">Text</span></span> | <span data-ttu-id="2f7fb-125">Diese Eigenschaft gibt eine Beschriftung für das Modul an.</span><span class="sxs-lookup"><span data-stu-id="2f7fb-125">This property specifies a caption for the module.</span></span> |
| <span data-ttu-id="2f7fb-126">Ausrichtung</span><span class="sxs-lookup"><span data-stu-id="2f7fb-126">Orientation</span></span> | <span data-ttu-id="2f7fb-127">**Horizontal** oder **vertikal**</span><span class="sxs-lookup"><span data-stu-id="2f7fb-127">**Horizontal** or **Vertical**</span></span>  | <span data-ttu-id="2f7fb-128">Diese Eigenschaft definiert die Layoutausrichtung für die Social-Media-Elemente.</span><span class="sxs-lookup"><span data-stu-id="2f7fb-128">This property defines the layout orientation for the social media items.</span></span> |

## <a name="social-share-item-module-properties"></a><span data-ttu-id="2f7fb-129">Social-Share-Artikelmoduleigenschaften</span><span class="sxs-lookup"><span data-stu-id="2f7fb-129">Social share item module properties</span></span>
| <span data-ttu-id="2f7fb-130">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="2f7fb-130">Property name</span></span>             | <span data-ttu-id="2f7fb-131">Wert</span><span class="sxs-lookup"><span data-stu-id="2f7fb-131">Value</span></span>                 | <span data-ttu-id="2f7fb-132">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2f7fb-132">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="2f7fb-133">Soziale Medien</span><span class="sxs-lookup"><span data-stu-id="2f7fb-133">Social media</span></span>              | <span data-ttu-id="2f7fb-134">**Facebook**, **Twitter**, **Pinterest**, **LinkedIn**, **E-Mail**</span><span class="sxs-lookup"><span data-stu-id="2f7fb-134">**Facebook**, **Twitter**, **Pinterest**, **LinkedIn**, **Mail**</span></span> | <span data-ttu-id="2f7fb-135">Ein Dropdown-Menü mit einer Liste von Social-Media-Plattformen.</span><span class="sxs-lookup"><span data-stu-id="2f7fb-135">A drop-down menu with a list of social media platforms.</span></span> |
| <span data-ttu-id="2f7fb-136">Symbol</span><span class="sxs-lookup"><span data-stu-id="2f7fb-136">Icon</span></span> |<span data-ttu-id="2f7fb-137">Bild</span><span class="sxs-lookup"><span data-stu-id="2f7fb-137">Image</span></span>    | <span data-ttu-id="2f7fb-138">Dies ist das Bild, das für die jeweiligen sozialen Medien angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="2f7fb-138">This will be the image that will be shown for the respective social media.</span></span> <span data-ttu-id="2f7fb-139">Als eine bewährte Methode, finden Sie das empfohlene Bild für jede Plattform im SDK der Social-Media-Plattform.</span><span class="sxs-lookup"><span data-stu-id="2f7fb-139">As a best practice, refer to the social media platform's SDK for the recommended image to use for each platform.</span></span> |

## <a name="add-a-social-share-module-to-a-buy-box-module"></a><span data-ttu-id="2f7fb-140">Hinzufügen eines Social-Share-Moduls zu einem Kauffeldmodul</span><span class="sxs-lookup"><span data-stu-id="2f7fb-140">Add a social share module to a buy box module</span></span>

<span data-ttu-id="2f7fb-141">Um ein Social-Share-Modul einem Kauffeldmodul hinzuzufügen, befolgen Sie diese Schritte.</span><span class="sxs-lookup"><span data-stu-id="2f7fb-141">To add a social share module to a buy box module, follow these steps.</span></span>

1. <span data-ttu-id="2f7fb-142">Wählen Sie auf der Fabrikam-Website **Seiten** und dann die Seite **DefaultPDP** aus, um die Produktdetailseite zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="2f7fb-142">In the Fabrikam site, select **Pages**, and then select the **DefaultPDP** page to open the product details page.</span></span> 
1. <span data-ttu-id="2f7fb-143">Wählen Sie im Slot **Kauffeld (erforderlich)** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="2f7fb-143">In the **Buybox (required)** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2f7fb-144">Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Social-Share** und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="2f7fb-144">In the **Add Module** dialog box, select the **Social Share** module, and then select **OK**.</span></span>
1. <span data-ttu-id="2f7fb-145">Wählen Sie im Slot **Social-Share** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="2f7fb-145">In the **Social Share** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2f7fb-146">Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **SocialShare** und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="2f7fb-146">In the **Add Module** dialog box, select the **SocialShare** module, and then select **OK**.</span></span>
1. <span data-ttu-id="2f7fb-147">Wählen Sie im Eigenschaftenbereich des Moduls **SocialShare** unter **Ausrichtung** **Horizontal**.</span><span class="sxs-lookup"><span data-stu-id="2f7fb-147">In the properties pane of the **SocialShare** module, under **Orientation**, select **Horizontal**.</span></span> <span data-ttu-id="2f7fb-148">Fügen Sie nach Bedarf eine Beschriftung hinzu.</span><span class="sxs-lookup"><span data-stu-id="2f7fb-148">Add a caption as needed.</span></span>
1. <span data-ttu-id="2f7fb-149">Wählen Sie im Slot **SocialShare** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="2f7fb-149">In the **SocialShare** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2f7fb-150">Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **SocialShareItem** und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="2f7fb-150">In the **Add Module** dialog box, select the **SocialShareItem** module, and then select **OK**.</span></span>
1. <span data-ttu-id="2f7fb-151">Wählen Sie im Eigenschaftenbereich des Moduls **SocialShareItem** unter **Soziale Medien** **Facebook**.</span><span class="sxs-lookup"><span data-stu-id="2f7fb-151">In the properties pane of the **SocialShareItem** module, under **Social Media**, select **Facebook**.</span></span>
1. <span data-ttu-id="2f7fb-152">Wählen Sie im Eigenschaftenbereich des Moduls **SocialShareItem** unter **Symbol** **+ Ein Bild hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="2f7fb-152">In the properties pane of the **SocialShareItem** module, under **Icon**, select **+ Add an image**.</span></span>
1. <span data-ttu-id="2f7fb-153">Wählen Sie im Dialogfeld **Medienauswahl** das Facebook-Logobild und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="2f7fb-153">In the **Media Picker** dialog box, select the Facebook logo image, and then select **OK**.</span></span> <span data-ttu-id="2f7fb-154">Wenn kein Facebook-Logobild vorhanden ist, wählen Sie **Neues Medienelement hochladen** aus, um eins hochladen.</span><span class="sxs-lookup"><span data-stu-id="2f7fb-154">If no Facebook logo image is present, select **Upload new media item** to upload one.</span></span>
1. <span data-ttu-id="2f7fb-155">Fügen Sie nach Bedarf zusätzliche **SocialShareItem**-Module hinzu und konfigurieren Sie diese.</span><span class="sxs-lookup"><span data-stu-id="2f7fb-155">Add and configure additional **SocialShareItem** modules as needed.</span></span>
1. <span data-ttu-id="2f7fb-156">Wählen **Speichern** und dann **Vorschau** aus, um eine Vorschau der Seite anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="2f7fb-156">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="2f7fb-157">Auf der Seite wird das Social-Share-Modul angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2f7fb-157">The page will show the social share module.</span></span>
1. <span data-ttu-id="2f7fb-158">Wählen **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="2f7fb-158">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2f7fb-159">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="2f7fb-159">Additional resources</span></span>

[<span data-ttu-id="2f7fb-160">Überblick über das Starterkit</span><span class="sxs-lookup"><span data-stu-id="2f7fb-160">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="2f7fb-161">Kauffeldmodul</span><span class="sxs-lookup"><span data-stu-id="2f7fb-161">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="2f7fb-162">Cookie-Compliance</span><span class="sxs-lookup"><span data-stu-id="2f7fb-162">Cookie compliance</span></span>](cookie-compliance.md)
