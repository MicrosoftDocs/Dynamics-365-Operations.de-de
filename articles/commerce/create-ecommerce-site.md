---
title: Erstellen einer E-Commerce-Webseite
description: In diesem Thema werden die Schritte und Informationen beschrieben, die zum Erstellen einer neuen E-Commerce-Site in Dynamics 365 Commerce Site Builder erforderlich sind.
author: bicyclingfool
manager: AnnBe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3d3d8a290f06d9734be21f2d59152acac6857506
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002012"
---
# <a name="create-an-e-commerce-site"></a><span data-ttu-id="cb8ee-103">Erstellen einer E-Commerce-Webseite</span><span class="sxs-lookup"><span data-stu-id="cb8ee-103">Create an e-Commerce site</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="cb8ee-104">In diesem Thema werden die Schritte und Informationen beschrieben, die zum Erstellen einer neuen E-Commerce-Site in Dynamics 365 Commerce Site Builder erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="cb8ee-104">This topic describes the steps and information required to create a new e-Commerce site in Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="cb8ee-105">Bevor Sie mit der Entwicklung Ihrer E-Commerce-Site beginnen, müssen Sie erst eine neue Site im Site Builder einrichten.</span><span class="sxs-lookup"><span data-stu-id="cb8ee-105">Before you can start developing your e-Commerce site, you must first establish a new site in site builder.</span></span> 


<span data-ttu-id="cb8ee-106">Um mit der Entwicklung der E-Commerce-Site zu beginnen, müssen Sie eine neue Site in der Siteerstellungsumgebung einrichten.</span><span class="sxs-lookup"><span data-stu-id="cb8ee-106">To start to develop your e-Commerce site, you must first establish a new site in the site authoring environment.</span></span> <span data-ttu-id="cb8ee-107">Bevor Sie eine neue Site erstellen können, muss mindestens ein Onlineshop in Commerce erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="cb8ee-107">Before you can create a new site, at least one online store must be created in Commerce.</span></span> 


## <a name="set-up-your-site"></a><span data-ttu-id="cb8ee-108">Site einrichten</span><span class="sxs-lookup"><span data-stu-id="cb8ee-108">Set up your site</span></span>

<span data-ttu-id="cb8ee-109">Um Ihre Site einzurichten, gehen Sie folgendermaßen vor.</span><span class="sxs-lookup"><span data-stu-id="cb8ee-109">To set up your site, do the following.</span></span>

1. <span data-ttu-id="cb8ee-110">Öffnen Sie die Site Builder-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="cb8ee-110">Open the site builder environment.</span></span> <span data-ttu-id="cb8ee-111">Sie finden einen Link zum Site Builder in Microsoft Lifecycle Services (LCS) auf der Seite mit den Umgebungsfunktionen für Commerce.</span><span class="sxs-lookup"><span data-stu-id="cb8ee-111">You can find a link to site builder in Microsoft Lifecycle Services (LCS) in the environment features page for Commerce.</span></span>
1. <span data-ttu-id="cb8ee-112">Auf der Startseite für die Siteerstellungsumgebung wählen Sie **Neue Site** aus.</span><span class="sxs-lookup"><span data-stu-id="cb8ee-112">On the home page for the site authoring environment, select **New site**.</span></span>
1. <span data-ttu-id="cb8ee-113">Geben Sie im Dialogfeld **Neue Site** die folgenden Informationen ein.</span><span class="sxs-lookup"><span data-stu-id="cb8ee-113">In the **New site** dialog box, provide the following information.</span></span>

| <span data-ttu-id="cb8ee-114">Feld</span><span class="sxs-lookup"><span data-stu-id="cb8ee-114">Field</span></span>                               | <span data-ttu-id="cb8ee-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cb8ee-115">Description</span></span> |
|-------------------------------------|-------------|
| <span data-ttu-id="cb8ee-116">Sitename</span><span class="sxs-lookup"><span data-stu-id="cb8ee-116">Site name</span></span>                           | <span data-ttu-id="cb8ee-117">Geben Sie den angezeigten Namen ein, der für Ihre Site in der Siteerstellungsumgebung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cb8ee-117">Enter the display name that should be used for your site in the site authoring environment.</span></span> <span data-ttu-id="cb8ee-118">Dieser Name ist nur in der Erstellungsumgebung sichtbar und wird nicht Debitoren angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="cb8ee-118">This name is visible only in the authoring environment and will not be shown to customers.</span></span> |
| <span data-ttu-id="cb8ee-119">Site-Administrator-Sicherheitsgruppe</span><span class="sxs-lookup"><span data-stu-id="cb8ee-119">Site administrator's security group</span></span> | <span data-ttu-id="cb8ee-120">Geben Sie die Microsoft Azure Active Directory (Azure AD) Sicherheitsgruppe ein, die Benutzer verwaltet, die die Siteadministratorrolle für diese Site haben.</span><span class="sxs-lookup"><span data-stu-id="cb8ee-120">Specify the Microsoft Azure Active Directory (Azure AD) security group that manages users who have the site administrator role in this site.</span></span> |
| <span data-ttu-id="cb8ee-121">Standardkanal (Nummer der Organisationseinheit)</span><span class="sxs-lookup"><span data-stu-id="cb8ee-121">Default channel (operating unit number)</span></span> | <span data-ttu-id="cb8ee-122">Wählen Sie den Onlineshop aus, aus, für den diese Site als Internet-Schaufenster dient.</span><span class="sxs-lookup"><span data-stu-id="cb8ee-122">Select the online store that this site will serve as the web storefront for.</span></span> <span data-ttu-id="cb8ee-123">Wenn Sie möchten, dass Ihre E-Commerce-Webseite mehrere Onlineshops unterstützen soll, müssen Sie die Shops Ihren Webseiten zuordnen unter **Site-Einstellungen**, nachdem die Site eingerichtet wurde.</span><span class="sxs-lookup"><span data-stu-id="cb8ee-123">If you want your e-Commerce site to support multiple online stores, you must associate the stores with your site in **Site settings** after the site is set up.</span></span> |
| <span data-ttu-id="cb8ee-124">Standardsprache</span><span class="sxs-lookup"><span data-stu-id="cb8ee-124">Default language</span></span>                            | <span data-ttu-id="cb8ee-125">Geben Sie die Standardsprache für diesen Onlineshop und Markt an.</span><span class="sxs-lookup"><span data-stu-id="cb8ee-125">Specify the default language for this online store and market.</span></span> <span data-ttu-id="cb8ee-126">Ein Onlineshop kann mehrere Sprachen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="cb8ee-126">An online store can support multiple languages.</span></span> <span data-ttu-id="cb8ee-127">Wenn Sie mehrere Sprachen für diesen Onlineshop oder einen anderen Onlineshop unterstützen möchten, können Sie diesen so konfigurieren unter **Siteeinstellungen**, nachdem die Site eingerichtet wurde.</span><span class="sxs-lookup"><span data-stu-id="cb8ee-127">If you want to support multiple languages for this online store or another online store, you can configure that support in **Site settings** after the site is set up.</span></span>  |
| <span data-ttu-id="cb8ee-128">Domäne</span><span class="sxs-lookup"><span data-stu-id="cb8ee-128">Domain</span></span>                              | <span data-ttu-id="cb8ee-129">Wählen Sie den Domänennamen, der als Domäne für diesen Onlineshop dienen soll.</span><span class="sxs-lookup"><span data-stu-id="cb8ee-129">Select a domain name that will serve as the domain for this online store.</span></span> <span data-ttu-id="cb8ee-130">Wenn Sie keine Domänen in LCS konfiguriert haben, können Sie dieses Feld leer lassen.</span><span class="sxs-lookup"><span data-stu-id="cb8ee-130">If you haven't configured any domains in LCS, you can leave this field blank.</span></span> <span data-ttu-id="cb8ee-131">Nachdem die Domäne in LCS konfiguriert ist, müssen Sie sie in Ihrem Onlineshop unter **Siteeinstellungen** hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="cb8ee-131">After your domain is configured in LCS, you must add it to your online store in **Site settings**.</span></span>  |
| <span data-ttu-id="cb8ee-132">Pfad</span><span class="sxs-lookup"><span data-stu-id="cb8ee-132">Path</span></span>                              | <span data-ttu-id="cb8ee-133">Wenn Ihr Site mehr als eine Sprache für einen angegebenen Domänennamen unterstützt, verwenden Sie das Pfadfeld, um eine eindeutige Standort URL für diese Domäne und Sprachenkombination zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="cb8ee-133">When your site supports more than one language for a given domain name, use the path field to create a unique site URL for that domain and language combination.</span></span> <span data-ttu-id="cb8ee-134">Sollte die gewünschte Sprache, die Sie im Feld **Standardsprache** angegeben haben, die einzige Sprache sein, die Sie für diese Domäne unterstützen oder die Standardsprache nach der Lokalisierung der Site in weitere Sprachen sein wird, wird empfohlen, dass Sie das Feld leer gelassen.</span><span class="sxs-lookup"><span data-stu-id="cb8ee-134">If the language you specified in the **Default language** field is the only language you will support for this domain, or will continue to be the default language after you have localized your site into additional languages, we recommend that you leave this field empty.</span></span> |


<span data-ttu-id="cb8ee-135">Nachdem Ihre Site erstellt wurde, können Sie prüfen, dass sie Ihrem Onlineshop zugeordnet ist, indem Sie die Registerkarte **Produkte** auswählen. Sie sollten das Sortiment von Produkten sehen, das dem Onlineshop zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="cb8ee-135">After your site is created, you can verify that it is associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="cb8ee-136">Sie können das Drop-Down-Menü im oberen linken Rand auch verwenden, um auf die zugewiesenen Produkte nach Kategorie zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="cb8ee-136">You can also use the drop-down menu in the upper left of the page to access the allocated products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cb8ee-137">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="cb8ee-137">Additional resources</span></span>

[<span data-ttu-id="cb8ee-138">Konfigurieren Ihres Domänennamens</span><span class="sxs-lookup"><span data-stu-id="cb8ee-138">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="cb8ee-139">Bereitstellen einer neuen E-Commerce-Webseite</span><span class="sxs-lookup"><span data-stu-id="cb8ee-139">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="cb8ee-140">Zuordnen einer Onlinewebseite zu einem Kanal</span><span class="sxs-lookup"><span data-stu-id="cb8ee-140">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="cb8ee-141">Verwalten von robots.txt-Dateien</span><span class="sxs-lookup"><span data-stu-id="cb8ee-141">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="cb8ee-142">Einrichten angepasster Seiten für die Benutzeranmeldungen</span><span class="sxs-lookup"><span data-stu-id="cb8ee-142">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="cb8ee-143">Unterstützung für ein Content Delivery Network (CDN) hinzufügen</span><span class="sxs-lookup"><span data-stu-id="cb8ee-143">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="cb8ee-144">Standortbasierte Shop-Erkennung aktivieren</span><span class="sxs-lookup"><span data-stu-id="cb8ee-144">Enable location-based store detection</span></span>](enable-store-detection.md)
