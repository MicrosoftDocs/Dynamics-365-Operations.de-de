---
title: E-Commerce-Website erstellen
description: In diesem Thema werden die Schritte und Informationen beschrieben, die zum Erstellen einer neuen E-Commerce-Website im Dynamics 365 Commerce-Website-Generator erforderlich sind.
author: bicyclingfool
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 61fe44df7165780be2dd00be3f210ab2da05ddfe
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795786"
---
# <a name="create-an-e-commerce-site"></a><span data-ttu-id="b0983-103">E-Commerce-Website erstellen</span><span class="sxs-lookup"><span data-stu-id="b0983-103">Create an e-commerce site</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b0983-104">In diesem Thema werden die Schritte und Informationen beschrieben, die zum Erstellen einer neuen E-Commerce-Website im Dynamics 365 Commerce-Website-Generator erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="b0983-104">This topic describes the steps and information required to create a new e-commerce site in Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="b0983-105">Wenn Sie die Dynamics 365 Commerce-Funktionen lizenzieren, wird der Website-Generator mit einer Starter Site bereitgestellt, die Sie als Grundlage für Ihre eigene Website verwenden können.</span><span class="sxs-lookup"><span data-stu-id="b0983-105">When you license the Dynamics 365 Commerce capabilities, site builder will be provisioned with a starter site that you can use as a basis for your own site.</span></span> <span data-ttu-id="b0983-106">Wenn Sie jedoch von Grund auf neu beginnen oder eine zweite Site einrichten möchten, müssen Sie eine neue Site in der Site-Erstellungsumgebung einrichten.</span><span class="sxs-lookup"><span data-stu-id="b0983-106">However, if you want to start from scratch or if you want to establish a second site, you will need to establish a new site in the site authoring environment.</span></span> 

## <a name="set-up-your-site"></a><span data-ttu-id="b0983-107">Site einrichten</span><span class="sxs-lookup"><span data-stu-id="b0983-107">Set up your site</span></span>

<span data-ttu-id="b0983-108">Um Ihre Site einzurichten, gehen Sie folgendermaßen vor.</span><span class="sxs-lookup"><span data-stu-id="b0983-108">To set up your site, do the following.</span></span>

1. <span data-ttu-id="b0983-109">Öffnen Sie die Site Builder-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="b0983-109">Open the site builder environment.</span></span> <span data-ttu-id="b0983-110">Sie finden einen Link zum Site Builder in Microsoft Lifecycle Services (LCS) auf der Seite mit den Umgebungsfunktionen für Commerce.</span><span class="sxs-lookup"><span data-stu-id="b0983-110">You can find a link to site builder in Microsoft Lifecycle Services (LCS) in the environment features page for Commerce.</span></span>
1. <span data-ttu-id="b0983-111">Auf der Startseite für die Siteerstellungsumgebung wählen Sie **Neue Site** aus.</span><span class="sxs-lookup"><span data-stu-id="b0983-111">On the home page for the site authoring environment, select **New site**.</span></span>
1. <span data-ttu-id="b0983-112">Geben Sie im Dialogfeld **Neue Site** die folgenden Informationen ein.</span><span class="sxs-lookup"><span data-stu-id="b0983-112">In the **New site** dialog box, provide the following information.</span></span>

| <span data-ttu-id="b0983-113">Feld</span><span class="sxs-lookup"><span data-stu-id="b0983-113">Field</span></span>                               | <span data-ttu-id="b0983-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b0983-114">Description</span></span> |
|-------------------------------------|-------------|
| <span data-ttu-id="b0983-115">Sitename</span><span class="sxs-lookup"><span data-stu-id="b0983-115">Site name</span></span>                           | <span data-ttu-id="b0983-116">Geben Sie den angezeigten Namen ein, der für Ihre Site in der Siteerstellungsumgebung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b0983-116">Enter the display name that should be used for your site in the site authoring environment.</span></span> <span data-ttu-id="b0983-117">Dieser Name ist nur in der Erstellungsumgebung sichtbar und wird nicht Debitoren angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="b0983-117">This name is visible only in the authoring environment and will not be shown to customers.</span></span> |
| <span data-ttu-id="b0983-118">Site-Administrator-Sicherheitsgruppe</span><span class="sxs-lookup"><span data-stu-id="b0983-118">Site administrator's security group</span></span> | <span data-ttu-id="b0983-119">Geben Sie die Microsoft Azure Active Directory (Azure AD) Sicherheitsgruppe ein, die Benutzer verwaltet, die die Siteadministratorrolle für diese Site haben.</span><span class="sxs-lookup"><span data-stu-id="b0983-119">Specify the Microsoft Azure Active Directory (Azure AD) security group that manages users who have the site administrator role in this site.</span></span> |
| <span data-ttu-id="b0983-120">Standardkanal (Nummer der Organisationseinheit)</span><span class="sxs-lookup"><span data-stu-id="b0983-120">Default channel (operating unit number)</span></span> | <span data-ttu-id="b0983-121">Wählen Sie den Onlineshop aus, aus, für den diese Site als Internet-Schaufenster dient.</span><span class="sxs-lookup"><span data-stu-id="b0983-121">Select the online store that this site will serve as the web storefront for.</span></span> <span data-ttu-id="b0983-122">Wenn Sie möchten, dass Ihre E-Commerce-Webseite mehrere Onlineshops unterstützen soll, müssen Sie die Shops Ihrer Website in **Website-Einstellungen** zuordnen, nachdem die Website eingerichtet wurde.</span><span class="sxs-lookup"><span data-stu-id="b0983-122">If you want your e-commerce site to support multiple online stores, you must associate the stores with your site in **Site settings** after the site is set up.</span></span> |
| <span data-ttu-id="b0983-123">Standardsprache</span><span class="sxs-lookup"><span data-stu-id="b0983-123">Default language</span></span>                            | <span data-ttu-id="b0983-124">Geben Sie die Standardsprache für diesen Onlineshop und Markt an.</span><span class="sxs-lookup"><span data-stu-id="b0983-124">Specify the default language for this online store and market.</span></span> <span data-ttu-id="b0983-125">Ein Onlineshop kann mehrere Sprachen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="b0983-125">An online store can support multiple languages.</span></span> <span data-ttu-id="b0983-126">Wenn Sie mehrere Sprachen für diesen Onlineshop oder einen anderen Onlineshop unterstützen möchten, können Sie diesen so konfigurieren unter **Siteeinstellungen**, nachdem die Site eingerichtet wurde.</span><span class="sxs-lookup"><span data-stu-id="b0983-126">If you want to support multiple languages for this online store or another online store, you can configure that support in **Site settings** after the site is set up.</span></span>  |
| <span data-ttu-id="b0983-127">Domäne</span><span class="sxs-lookup"><span data-stu-id="b0983-127">Domain</span></span>                              | <span data-ttu-id="b0983-128">Wählen Sie den Domänennamen, der als Domäne für diesen Onlineshop dienen soll.</span><span class="sxs-lookup"><span data-stu-id="b0983-128">Select a domain name that will serve as the domain for this online store.</span></span> <span data-ttu-id="b0983-129">Wenn Sie keine Domänen in LCS konfiguriert haben, können Sie dieses Feld leer lassen.</span><span class="sxs-lookup"><span data-stu-id="b0983-129">If you haven't configured any domains in LCS, you can leave this field blank.</span></span> <span data-ttu-id="b0983-130">Nachdem die Domäne in LCS konfiguriert ist, müssen Sie sie in Ihrem Onlineshop unter **Siteeinstellungen** hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b0983-130">After your domain is configured in LCS, you must add it to your online store in **Site settings**.</span></span>  |
| <span data-ttu-id="b0983-131">Pfad</span><span class="sxs-lookup"><span data-stu-id="b0983-131">Path</span></span>                              | <span data-ttu-id="b0983-132">Wenn Ihr Site mehr als eine Sprache für einen angegebenen Domänennamen unterstützt, verwenden Sie das Pfadfeld, um eine eindeutige Standort URL für diese Domäne und Sprachenkombination zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b0983-132">When your site supports more than one language for a given domain name, use the path field to create a unique site URL for that domain and language combination.</span></span> <span data-ttu-id="b0983-133">Sollte die gewünschte Sprache, die Sie im Feld **Standardsprache** angegeben haben, die einzige Sprache sein, die Sie für diese Domäne unterstützen oder die Standardsprache nach der Lokalisierung der Site in weitere Sprachen sein wird, wird empfohlen, dass Sie das Feld leer gelassen.</span><span class="sxs-lookup"><span data-stu-id="b0983-133">If the language you specified in the **Default language** field is the only language you will support for this domain, or will continue to be the default language after you have localized your site into additional languages, we recommend that you leave this field empty.</span></span> |


<span data-ttu-id="b0983-134">Nachdem Ihre Site erstellt wurde, können Sie prüfen, dass sie Ihrem Onlineshop zugeordnet ist, indem Sie die Registerkarte **Produkte** auswählen. Sie sollten das Sortiment von Produkten sehen, das dem Onlineshop zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="b0983-134">After your site is created, you can verify that it is associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="b0983-135">Sie können das Drop-Down-Menü im oberen linken Rand auch verwenden, um auf die zugewiesenen Produkte nach Kategorie zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="b0983-135">You can also use the drop-down menu in the upper left of the page to access the allocated products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b0983-136">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b0983-136">Additional resources</span></span>

[<span data-ttu-id="b0983-137">Domänennamen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="b0983-137">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="b0983-138">Neuen E-Commerce-Mandanten bereitstellen</span><span class="sxs-lookup"><span data-stu-id="b0983-138">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="b0983-139">Zuordnen einer Dynamics 365 Commerce-Website zu einem Onlinekanal</span><span class="sxs-lookup"><span data-stu-id="b0983-139">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="b0983-140">Robots.txt-Dateien verwalten</span><span class="sxs-lookup"><span data-stu-id="b0983-140">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="b0983-141">URL-Umleitungen in Massen hochladen</span><span class="sxs-lookup"><span data-stu-id="b0983-141">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="b0983-142">Einrichten eines B2C-Mandanten in Commerce</span><span class="sxs-lookup"><span data-stu-id="b0983-142">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="b0983-143">Einrichten angepasster Seiten für die Benutzeranmeldungen</span><span class="sxs-lookup"><span data-stu-id="b0983-143">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="b0983-144">Konfigurieren Sie mehrere B2C-Mandanten in einer Commerce-Umgebung</span><span class="sxs-lookup"><span data-stu-id="b0983-144">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="b0983-145">Hinzufügen von Unterstützung für ein Content Delivery Network (CDN)</span><span class="sxs-lookup"><span data-stu-id="b0983-145">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="b0983-146">Standortbasierte Shop-Erkennung aktivieren</span><span class="sxs-lookup"><span data-stu-id="b0983-146">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]