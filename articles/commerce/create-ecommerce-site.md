---
title: Erstellen einer E-Commerce-Webseite
description: In diesem Thema werden die Aufgaben beschrieben, die bei der Erstellung einer neuen E-Commerce-Site in Dynamics 365 Commerce zugeordnet werden.
author: bicyclingfool
manager: AnnBe
ms.date: 10/31/2019
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
ms.openlocfilehash: fd87a51b73deae64867b0420c00db9fce7c79336
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697128"
---
# <a name="create-an-e-commerce-site"></a><span data-ttu-id="39cb5-103">Erstellen einer E-Commerce-Webseite</span><span class="sxs-lookup"><span data-stu-id="39cb5-103">Create an e-Commerce site</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="39cb5-104">In diesem Thema werden die Aufgaben beschrieben, die bei der Erstellung einer neuen E-Commerce-Site in Dynamics 365 Commerce zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="39cb5-104">This topic describes the tasks that are associated with the creation of a new e-Commerce site in Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="39cb5-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="39cb5-105">Overview</span></span>

<span data-ttu-id="39cb5-106">Um mit der Entwicklung der E-Commerce-Site zu beginnen, müssen Sie eine neue Site in der Siteerstellungsumgebung einrichten.</span><span class="sxs-lookup"><span data-stu-id="39cb5-106">To start to develop your e-Commerce site, you must first establish a new site in the site authoring environment.</span></span> <span data-ttu-id="39cb5-107">Bevor Sie eine neue Site erstellen können, muss mindestens ein Onlineshop in Dynamics 365 Retail erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="39cb5-107">Before you can create a new site, at least one online store must be created in Dynamics 365 Retail.</span></span> 

## <a name="set-up-your-site"></a><span data-ttu-id="39cb5-108">Site einrichten</span><span class="sxs-lookup"><span data-stu-id="39cb5-108">Set up your site</span></span>

<span data-ttu-id="39cb5-109">Um Ihre Site einzurichten, gehen Sie folgendermaßen vor.</span><span class="sxs-lookup"><span data-stu-id="39cb5-109">To set up your site, do the following.</span></span>

1. <span data-ttu-id="39cb5-110">Im Microsoft Lifecycle Services (LCS) wählen Sie den Link für die Siteerstellungsumgebung aus.</span><span class="sxs-lookup"><span data-stu-id="39cb5-110">In Microsoft Lifecycle Services (LCS), select the link for the site authoring environment.</span></span> 
1. <span data-ttu-id="39cb5-111">Auf der Startseite für die Siteerstellungsumgebung wählen Sie **Neue Site** aus.</span><span class="sxs-lookup"><span data-stu-id="39cb5-111">On the home page for the site authoring environment, select **New site**.</span></span>
1. <span data-ttu-id="39cb5-112">Geben Sie im Dialogfeld **Neue Site** die folgenden Informationen ein.</span><span class="sxs-lookup"><span data-stu-id="39cb5-112">In the **New site** dialog box, provide the following information.</span></span>

| <span data-ttu-id="39cb5-113">Feld</span><span class="sxs-lookup"><span data-stu-id="39cb5-113">Field</span></span>                               | <span data-ttu-id="39cb5-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="39cb5-114">Description</span></span> |
|-------------------------------------|-------------|
| <span data-ttu-id="39cb5-115">Sitename</span><span class="sxs-lookup"><span data-stu-id="39cb5-115">Site name</span></span>                           | <span data-ttu-id="39cb5-116">Geben Sie den angezeigten Namen ein, der für Ihre Site in der Siteerstellungsumgebung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="39cb5-116">Enter the display name that should be used for your site in the site authoring environment.</span></span> <span data-ttu-id="39cb5-117">Dieser Name ist nur in der Erstellungsumgebung sichtbar und wird nicht Debitoren angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="39cb5-117">This name is visible only in the authoring environment and will not be shown to customers.</span></span> |
| <span data-ttu-id="39cb5-118">Site-Administrator-Sicherheitsgruppe</span><span class="sxs-lookup"><span data-stu-id="39cb5-118">Site administrator's security group</span></span> | <span data-ttu-id="39cb5-119">Geben Sie die Microsoft Azure Active Directory (Azure AD) Sicherheitsgruppe ein, die Benutzer verwaltet, die die Siteadministratorrolle für diese Site haben.</span><span class="sxs-lookup"><span data-stu-id="39cb5-119">Specify the Microsoft Azure Active Directory (Azure AD) security group that manages users who have the site administrator role in this site.</span></span> |
| <span data-ttu-id="39cb5-120">Standardkanal (Nummer der Organisationseinheit)</span><span class="sxs-lookup"><span data-stu-id="39cb5-120">Default channel (operating unit number)</span></span> | <span data-ttu-id="39cb5-121">Wählen Sie den Onlineshop aus, aus, für den diese Site als Internet-Schaufenster dient.</span><span class="sxs-lookup"><span data-stu-id="39cb5-121">Select the online store that this site will serve as the web storefront for.</span></span> <span data-ttu-id="39cb5-122">Wenn Sie möchten, dass Ihre E-Commerce-Webseite mehrere Onlineshops unterstützen soll, müssen Sie die Shops Ihren Webseiten zuordnen unter **Site-Einstellungen**, nachdem die Site eingerichtet wurde.</span><span class="sxs-lookup"><span data-stu-id="39cb5-122">If you want your e-Commerce site to support multiple online stores, you must associate the stores with your site in **Site settings** after the site is set up.</span></span> |
| <span data-ttu-id="39cb5-123">Standardsprache</span><span class="sxs-lookup"><span data-stu-id="39cb5-123">Default language</span></span>                            | <span data-ttu-id="39cb5-124">Geben Sie die Standardsprache für diesen Onlineshop und Markt an.</span><span class="sxs-lookup"><span data-stu-id="39cb5-124">Specify the default language for this online store and market.</span></span> <span data-ttu-id="39cb5-125">Ein Onlineshop kann mehrere Sprachen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="39cb5-125">An online store can support multiple languages.</span></span> <span data-ttu-id="39cb5-126">Wenn Sie mehrere Sprachen für diesen Onlineshop oder einen anderen Onlineshop unterstützen möchten, können Sie diesen so konfigurieren unter **Siteeinstellungen**, nachdem die Site eingerichtet wurde.</span><span class="sxs-lookup"><span data-stu-id="39cb5-126">If you want to support multiple languages for this online store or another online store, you can configure that support in **Site settings** after the site is set up.</span></span>  |
| <span data-ttu-id="39cb5-127">Domäne</span><span class="sxs-lookup"><span data-stu-id="39cb5-127">Domain</span></span>                              | <span data-ttu-id="39cb5-128">Wählen Sie den Domänennamen, der als Domäne für diesen Onlineshop dienen soll.</span><span class="sxs-lookup"><span data-stu-id="39cb5-128">Select a domain name that will serve as the domain for this online store.</span></span> <span data-ttu-id="39cb5-129">Wenn Sie keine Domänen in LCS konfiguriert haben, können Sie dieses Feld leer lassen.</span><span class="sxs-lookup"><span data-stu-id="39cb5-129">If you haven't configured any domains in LCS, you can leave this field blank.</span></span> <span data-ttu-id="39cb5-130">Nachdem die Domäne in LCS konfiguriert ist, müssen Sie sie in Ihrem Onlineshop unter **Siteeinstellungen** hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="39cb5-130">After your domain is configured in LCS, you must add it to your online store in **Site settings**.</span></span>  |
| <span data-ttu-id="39cb5-131">Pfad</span><span class="sxs-lookup"><span data-stu-id="39cb5-131">Path</span></span>                              | <span data-ttu-id="39cb5-132">Wenn Ihr Site mehr als eine Sprache für einen angegebenen Domänennamen unterstützt, verwenden Sie das Pfadfeld, um eine eindeutige Standort URL für diese Domäne und Sprachenkombination zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="39cb5-132">When your site supports more than one language for a given domain name, use the path field to create a unique site URL for that domain and language combination.</span></span> <span data-ttu-id="39cb5-133">Sollte die gewünschte Sprache, die Sie im Feld **Standardsprache** angegeben haben, die einzige Sprache sein, die Sie für diese Domäne unterstützen oder die Standardsprache nach der Lokalisierung der Site in weitere Sprachen sein wird, wird empfohlen, dass Sie das Feld leer gelassen.</span><span class="sxs-lookup"><span data-stu-id="39cb5-133">If the language you specified in the **Default language** field is the only language you will support for this domain, or will continue to be the default language after you have localized your site into additional languages, we recommend that you leave this field empty.</span></span> |


<span data-ttu-id="39cb5-134">Nachdem Ihre Site erstellt wurde, können Sie prüfen, dass sie Ihrem Onlineshop zugeordnet ist, indem Sie die Registerkarte **Produkte** auswählen. Sie sollten das Sortiment von Produkten sehen, das dem Onlineshop zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="39cb5-134">After your site is created, you can verify that it is associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="39cb5-135">Sie können das Drop-Down-Menü im oberen linken Rand auch verwenden, um auf die zugewiesenen Produkte nach Kategorie zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="39cb5-135">You can also use the drop-down menu in the upper left of the page to access the allocated products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="39cb5-136">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="39cb5-136">Additional resources</span></span>

[<span data-ttu-id="39cb5-137">Onlineshop – Überblick</span><span class="sxs-lookup"><span data-stu-id="39cb5-137">Online store overview</span></span>](online-store-overview.md)

[<span data-ttu-id="39cb5-138">Bereitstellen einer neuen E-Commerce-Webseite</span><span class="sxs-lookup"><span data-stu-id="39cb5-138">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="39cb5-139">Zuordnen einer Onlinewebseite zu einem Kanal</span><span class="sxs-lookup"><span data-stu-id="39cb5-139">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="39cb5-140">Konfigurieren Ihres Domänennamens</span><span class="sxs-lookup"><span data-stu-id="39cb5-140">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="39cb5-141">Unterstützung für ein Content Delivery Network (CDN) hinzufügen</span><span class="sxs-lookup"><span data-stu-id="39cb5-141">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="39cb5-142">Standortbasierte Shop-Erkennung aktivieren</span><span class="sxs-lookup"><span data-stu-id="39cb5-142">Enable location-based store detection</span></span>](enable-store-detection.md)

[<span data-ttu-id="39cb5-143">Einrichten angepasster Seiten für die Benutzeranmeldungen</span><span class="sxs-lookup"><span data-stu-id="39cb5-143">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="39cb5-144">Übersicht über die Erstellung von Startseiten</span><span class="sxs-lookup"><span data-stu-id="39cb5-144">Authoring home page overview</span></span>](authoring-home-overview.md)

[<span data-ttu-id="39cb5-145">Neue Seite hinzufügen</span><span class="sxs-lookup"><span data-stu-id="39cb5-145">Add a new site page</span></span>](add-new-page.md)
