---
title: Erstellen einer E-Commerce-Webseite
description: In diesem Thema werden die Schritte und Informationen beschrieben, die zum Erstellen einer neuen E-Commerce-Site in Dynamics 365 Commerce Site Builder erforderlich sind.
author: bicyclingfool
manager: AnnBe
ms.date: 03/02/2020
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
ms.openlocfilehash: 7177bae911dfa91a645b40581bf23b3ed76562a3
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096773"
---
# <a name="create-an-e-commerce-site"></a><span data-ttu-id="9f302-103">Erstellen einer E-Commerce-Webseite</span><span class="sxs-lookup"><span data-stu-id="9f302-103">Create an e-Commerce site</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="9f302-104">In diesem Thema werden die Schritte und Informationen beschrieben, die zum Erstellen einer neuen E-Commerce-Site in Dynamics 365 Commerce Site Builder erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="9f302-104">This topic describes the steps and information required to create a new e-Commerce site in Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="9f302-105">Bevor Sie mit der Entwicklung Ihrer E-Commerce-Site beginnen, müssen Sie erst eine neue Site im Site Builder einrichten.</span><span class="sxs-lookup"><span data-stu-id="9f302-105">Before you can start developing your e-Commerce site, you must first establish a new site in site builder.</span></span> 


<span data-ttu-id="9f302-106">Um mit der Entwicklung der E-Commerce-Site zu beginnen, müssen Sie eine neue Site in der Siteerstellungsumgebung einrichten.</span><span class="sxs-lookup"><span data-stu-id="9f302-106">To start to develop your e-Commerce site, you must first establish a new site in the site authoring environment.</span></span> <span data-ttu-id="9f302-107">Bevor Sie eine neue Site erstellen können, muss mindestens ein Onlineshop in Commerce erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="9f302-107">Before you can create a new site, at least one online store must be created in Commerce.</span></span> 


## <a name="set-up-your-site"></a><span data-ttu-id="9f302-108">Site einrichten</span><span class="sxs-lookup"><span data-stu-id="9f302-108">Set up your site</span></span>

<span data-ttu-id="9f302-109">Um Ihre Site einzurichten, gehen Sie folgendermaßen vor.</span><span class="sxs-lookup"><span data-stu-id="9f302-109">To set up your site, do the following.</span></span>

1. <span data-ttu-id="9f302-110">Öffnen Sie die Site Builder-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="9f302-110">Open the site builder environment.</span></span> <span data-ttu-id="9f302-111">Sie finden einen Link zum Site Builder in Microsoft Lifecycle Services (LCS) auf der Seite mit den Umgebungsfunktionen für Commerce.</span><span class="sxs-lookup"><span data-stu-id="9f302-111">You can find a link to site builder in Microsoft Lifecycle Services (LCS) in the environment features page for Commerce.</span></span>
1. <span data-ttu-id="9f302-112">Auf der Startseite für die Siteerstellungsumgebung wählen Sie **Neue Site** aus.</span><span class="sxs-lookup"><span data-stu-id="9f302-112">On the home page for the site authoring environment, select **New site**.</span></span>
1. <span data-ttu-id="9f302-113">Geben Sie im Dialogfeld **Neue Site** die folgenden Informationen ein.</span><span class="sxs-lookup"><span data-stu-id="9f302-113">In the **New site** dialog box, provide the following information.</span></span>

| <span data-ttu-id="9f302-114">Feld</span><span class="sxs-lookup"><span data-stu-id="9f302-114">Field</span></span>                               | <span data-ttu-id="9f302-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9f302-115">Description</span></span> |
|-------------------------------------|-------------|
| <span data-ttu-id="9f302-116">Sitename</span><span class="sxs-lookup"><span data-stu-id="9f302-116">Site name</span></span>                           | <span data-ttu-id="9f302-117">Geben Sie den angezeigten Namen ein, der für Ihre Site in der Siteerstellungsumgebung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9f302-117">Enter the display name that should be used for your site in the site authoring environment.</span></span> <span data-ttu-id="9f302-118">Dieser Name ist nur in der Erstellungsumgebung sichtbar und wird nicht Debitoren angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="9f302-118">This name is visible only in the authoring environment and will not be shown to customers.</span></span> |
| <span data-ttu-id="9f302-119">Site-Administrator-Sicherheitsgruppe</span><span class="sxs-lookup"><span data-stu-id="9f302-119">Site administrator's security group</span></span> | <span data-ttu-id="9f302-120">Geben Sie die Microsoft Azure Active Directory (Azure AD) Sicherheitsgruppe ein, die Benutzer verwaltet, die die Siteadministratorrolle für diese Site haben.</span><span class="sxs-lookup"><span data-stu-id="9f302-120">Specify the Microsoft Azure Active Directory (Azure AD) security group that manages users who have the site administrator role in this site.</span></span> |
| <span data-ttu-id="9f302-121">Standardkanal (Nummer der Organisationseinheit)</span><span class="sxs-lookup"><span data-stu-id="9f302-121">Default channel (operating unit number)</span></span> | <span data-ttu-id="9f302-122">Wählen Sie den Onlineshop aus, aus, für den diese Site als Internet-Schaufenster dient.</span><span class="sxs-lookup"><span data-stu-id="9f302-122">Select the online store that this site will serve as the web storefront for.</span></span> <span data-ttu-id="9f302-123">Wenn Sie möchten, dass Ihre E-Commerce-Webseite mehrere Onlineshops unterstützen soll, müssen Sie die Shops Ihren Webseiten zuordnen unter **Site-Einstellungen**, nachdem die Site eingerichtet wurde.</span><span class="sxs-lookup"><span data-stu-id="9f302-123">If you want your e-Commerce site to support multiple online stores, you must associate the stores with your site in **Site settings** after the site is set up.</span></span> |
| <span data-ttu-id="9f302-124">Standardsprache</span><span class="sxs-lookup"><span data-stu-id="9f302-124">Default language</span></span>                            | <span data-ttu-id="9f302-125">Geben Sie die Standardsprache für diesen Onlineshop und Markt an.</span><span class="sxs-lookup"><span data-stu-id="9f302-125">Specify the default language for this online store and market.</span></span> <span data-ttu-id="9f302-126">Ein Onlineshop kann mehrere Sprachen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="9f302-126">An online store can support multiple languages.</span></span> <span data-ttu-id="9f302-127">Wenn Sie mehrere Sprachen für diesen Onlineshop oder einen anderen Onlineshop unterstützen möchten, können Sie diesen so konfigurieren unter **Siteeinstellungen**, nachdem die Site eingerichtet wurde.</span><span class="sxs-lookup"><span data-stu-id="9f302-127">If you want to support multiple languages for this online store or another online store, you can configure that support in **Site settings** after the site is set up.</span></span>  |
| <span data-ttu-id="9f302-128">Domäne</span><span class="sxs-lookup"><span data-stu-id="9f302-128">Domain</span></span>                              | <span data-ttu-id="9f302-129">Wählen Sie den Domänennamen, der als Domäne für diesen Onlineshop dienen soll.</span><span class="sxs-lookup"><span data-stu-id="9f302-129">Select a domain name that will serve as the domain for this online store.</span></span> <span data-ttu-id="9f302-130">Wenn Sie keine Domänen in LCS konfiguriert haben, können Sie dieses Feld leer lassen.</span><span class="sxs-lookup"><span data-stu-id="9f302-130">If you haven't configured any domains in LCS, you can leave this field blank.</span></span> <span data-ttu-id="9f302-131">Nachdem die Domäne in LCS konfiguriert ist, müssen Sie sie in Ihrem Onlineshop unter **Siteeinstellungen** hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="9f302-131">After your domain is configured in LCS, you must add it to your online store in **Site settings**.</span></span>  |
| <span data-ttu-id="9f302-132">Pfad</span><span class="sxs-lookup"><span data-stu-id="9f302-132">Path</span></span>                              | <span data-ttu-id="9f302-133">Wenn Ihr Site mehr als eine Sprache für einen angegebenen Domänennamen unterstützt, verwenden Sie das Pfadfeld, um eine eindeutige Standort URL für diese Domäne und Sprachenkombination zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9f302-133">When your site supports more than one language for a given domain name, use the path field to create a unique site URL for that domain and language combination.</span></span> <span data-ttu-id="9f302-134">Sollte die gewünschte Sprache, die Sie im Feld **Standardsprache** angegeben haben, die einzige Sprache sein, die Sie für diese Domäne unterstützen oder die Standardsprache nach der Lokalisierung der Site in weitere Sprachen sein wird, wird empfohlen, dass Sie das Feld leer gelassen.</span><span class="sxs-lookup"><span data-stu-id="9f302-134">If the language you specified in the **Default language** field is the only language you will support for this domain, or will continue to be the default language after you have localized your site into additional languages, we recommend that you leave this field empty.</span></span> |


<span data-ttu-id="9f302-135">Nachdem Ihre Site erstellt wurde, können Sie prüfen, dass sie Ihrem Onlineshop zugeordnet ist, indem Sie die Registerkarte **Produkte** auswählen. Sie sollten das Sortiment von Produkten sehen, das dem Onlineshop zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="9f302-135">After your site is created, you can verify that it is associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="9f302-136">Sie können das Drop-Down-Menü im oberen linken Rand auch verwenden, um auf die zugewiesenen Produkte nach Kategorie zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="9f302-136">You can also use the drop-down menu in the upper left of the page to access the allocated products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9f302-137">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9f302-137">Additional resources</span></span>

[<span data-ttu-id="9f302-138">Ihren Domänennamen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="9f302-138">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="9f302-139">Bereitstellen einer neuen E-Commerce-Webseite</span><span class="sxs-lookup"><span data-stu-id="9f302-139">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="9f302-140">Onlineshopkanal einrichten</span><span class="sxs-lookup"><span data-stu-id="9f302-140">Set up an online store channel</span></span>](online-stores.md)

[<span data-ttu-id="9f302-141">Zuordnen einer Onlinewebseite zu einem Kanal</span><span class="sxs-lookup"><span data-stu-id="9f302-141">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="9f302-142">Verwalten von robots.txt-Dateien</span><span class="sxs-lookup"><span data-stu-id="9f302-142">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="9f302-143">URL-Weiterleitungen in großen Mengen hochladen</span><span class="sxs-lookup"><span data-stu-id="9f302-143">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="9f302-144">Einrichten eines B2C-Mandanten in Commerce</span><span class="sxs-lookup"><span data-stu-id="9f302-144">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="9f302-145">Einrichten angepasster Seiten für die Benutzeranmeldungen</span><span class="sxs-lookup"><span data-stu-id="9f302-145">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="9f302-146">Konfigurieren Sie mehrere B2C-Mandanten in einer Commerce-Umgebung</span><span class="sxs-lookup"><span data-stu-id="9f302-146">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="9f302-147">Hinzufügen von Unterstützung für ein Content Delivery Network (CDN)</span><span class="sxs-lookup"><span data-stu-id="9f302-147">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="9f302-148">Standortbasierte Shop-Erkennung aktivieren</span><span class="sxs-lookup"><span data-stu-id="9f302-148">Enable location-based store detection</span></span>](enable-store-detection.md)
