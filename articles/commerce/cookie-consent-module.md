---
title: Cookie-Zustimmungsmodul
description: Dieses Thema behandelt Cookie-Zustimmungsmodule und erläutert, wie sie Webseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 504232285267fb3663093a84a371e0040233ce23
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993524"
---
# <a name="cookie-consent-module"></a><span data-ttu-id="6e590-103">Cookie-Zustimmungsmodul</span><span class="sxs-lookup"><span data-stu-id="6e590-103">Cookie consent module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6e590-104">Dieses Thema behandelt Cookie-Zustimmungsmodule und erläutert, wie sie Webseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="6e590-104">This topic covers cookie consent modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6e590-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="6e590-105">Overview</span></span>

<span data-ttu-id="6e590-106">Das Cookie-Zustimmungsmodul fordert die Benutzer der Website auf, ausdrücklich zuzustimmen, das Cookies für alle Funktionen oder Module, die Browser-Cookies verfolgen, zugelassen werden.</span><span class="sxs-lookup"><span data-stu-id="6e590-106">The cookie consent module prompts site users to explicitly provide consent to allow cookies for any feature or module that tracks browser cookies.</span></span> <span data-ttu-id="6e590-107">Die Zustimmung ist erforderlich, wenn ein Website-Benutzer eine Website zum ersten Mal in einer neuen Browsersitzung durchsucht.</span><span class="sxs-lookup"><span data-stu-id="6e590-107">The consent is required the first time a site user browses a site in a new browser session.</span></span> <span data-ttu-id="6e590-108">Wenn die Einwilligung eingegangen ist, wird sie nachverfolgt und der Benutzer der Website wird nicht erneut zur Einwilligung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="6e590-108">When consent is received, it is tracked and the site user will not be prompted for consent again.</span></span> <span data-ttu-id="6e590-109">Weitere Informationen finden Sie unter [Cookie-Compliance](cookie-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="6e590-109">For more information, see [Cookie compliance](cookie-compliance.md).</span></span>

<span data-ttu-id="6e590-110">Wenn keine Cookie-Zustimmung für Website-Benutzer eingeht, werden Funktionen oder Module, für die eine Cookie-Zustimmung erforderlich ist, nicht auf der Seite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6e590-110">If site user cookie consent is not received, any features or modules that require cookie consent will not be rendered on the page.</span></span> <span data-ttu-id="6e590-111">Das Checkout-Modul, das Social-Share-Modul und die Fujnktion für bevorzugte Stores erfordern beispielsweise die Zustimmung eines Cookies und werden nicht gerendert, wenn die Zustimmung des Website-Benutzers nicht erhalten wird.</span><span class="sxs-lookup"><span data-stu-id="6e590-111">For example, the checkout module, social share module, and preferred store feature all require cookie consent and will not be rendered if site user consent is not received.</span></span> 

<span data-ttu-id="6e590-112">Ein Cookie-Zustimmungsmodul kann für das Header-Fragment einer Seite konfiguriert werden, damit es beim Laden der Seite erzwungen werden kann.</span><span class="sxs-lookup"><span data-stu-id="6e590-112">A cookie consent module can be configured on a page's header fragment so that it can be enforced when the page loads.</span></span> <span data-ttu-id="6e590-113">Das Cookie-Zustimmungsmodul sollte eine eindeutige Meldung enthalten, die den Benutzer der Website über die Verwendung von Cookies auf der Website informiert, und einen Link zur Datenschutzseite der Website bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="6e590-113">The cookie consent module should have a clear message informing the site user about cookie usage on the site and should provide a link to the site's privacy page.</span></span>

<span data-ttu-id="6e590-114">Die folgende Abbildung zeigt ein Beispiel für eine Cookie-Zustimmungsnachricht mit einem Link zur Datenschutzrichtlinie der Website, die in der Kopfzeile einer Website-Seite angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="6e590-114">The following illustration highlights an example of a cookie consent message with a link to the site's privacy policy page displayed on the header of a site page.</span></span>
<span data-ttu-id="6e590-115">![Beispiel eines Cookie-Zustimmungsmoduls](./media/ecommerce-cookieconsent.png)</span><span class="sxs-lookup"><span data-stu-id="6e590-115">![Example of a cookie consent module](./media/ecommerce-cookieconsent.png)</span></span>

## <a name="cookie-consent-module-properties"></a><span data-ttu-id="6e590-116">Eigenschaften des Cookie-Zustimmungsmoduls</span><span class="sxs-lookup"><span data-stu-id="6e590-116">Cookie consent module properties</span></span>

| <span data-ttu-id="6e590-117">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="6e590-117">Property name</span></span>             | <span data-ttu-id="6e590-118">Wert</span><span class="sxs-lookup"><span data-stu-id="6e590-118">Value</span></span>                 | <span data-ttu-id="6e590-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6e590-119">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="6e590-120">Rich Text</span><span class="sxs-lookup"><span data-stu-id="6e590-120">Rich Text</span></span>                  | <span data-ttu-id="6e590-121">Rich Text</span><span class="sxs-lookup"><span data-stu-id="6e590-121">Rich Text</span></span> | <span data-ttu-id="6e590-122">Gibt in einer Rich-Text-Benachrichtigung an Benutzer der Website an, dass die Website Browser-Cookies verwendet und dass Benutzer die Verwendung von Cookies akzeptieren sollten, damit die Website voll funktionsfähig ist.</span><span class="sxs-lookup"><span data-stu-id="6e590-122">Specifies a Rich Text notification to site users that the site uses browser cookies and that users should accept the use of cookies for the site to be fully functional.</span></span> |
| <span data-ttu-id="6e590-123">Verknüpfungen</span><span class="sxs-lookup"><span data-stu-id="6e590-123">Links</span></span> | <span data-ttu-id="6e590-124">URL</span><span class="sxs-lookup"><span data-stu-id="6e590-124">URL</span></span> | <span data-ttu-id="6e590-125">Es kann mindestens ein Links zur Datenschutzseite einer Website hinzugefügt werden, auf der die Arten von Cookies beschrieben werden, die auf der Website verfolgt werden.</span><span class="sxs-lookup"><span data-stu-id="6e590-125">One or more links can be added to a site's privacy page that describes the types of cookies that are tracked on the site.</span></span> |

## <a name="add-a-cookie-consent-module-to-site-pages"></a><span data-ttu-id="6e590-126">Hinzufügen eines Cookie-Zustimmungsmoduls zu den Seiten der Website</span><span class="sxs-lookup"><span data-stu-id="6e590-126">Add a cookie consent module to site pages</span></span>

<span data-ttu-id="6e590-127">Um ein Cookie-Zustimmungsmodul effizient zu mehreren Websiteseiten hinzuzufügen, kann es einem freigegebenen Seitenkopffragment hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="6e590-127">To efficiently add a cookie consent module to multiple site pages, it can be added to a shared page header fragment.</span></span> <span data-ttu-id="6e590-128">Nachdem das Header-Fragment allen Websiteseiten hinzugefügt wurde, wird automatisch eine Cookie-Zustimmungsbenachrichtigung angezeigt, wenn ein Website-Benutzer zum ersten Mal zu einer Website-Seite navigiert.</span><span class="sxs-lookup"><span data-stu-id="6e590-128">After the header fragment is added to all site pages, a cookie consent notification will automatically be rendered the first time a site user navigates to any site page.</span></span>

<span data-ttu-id="6e590-129">Weitere Informationen zu Header-Fragmenten und Modulen finden Sie unter [Header-Modul](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="6e590-129">For more information about header fragments and modules, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6e590-130">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6e590-130">Additional resources</span></span>

[<span data-ttu-id="6e590-131">Übersicht über die Modulbibliothek</span><span class="sxs-lookup"><span data-stu-id="6e590-131">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="6e590-132">Kopfzeilenmodul</span><span class="sxs-lookup"><span data-stu-id="6e590-132">Header module</span></span>](author-header-module.md) 

[<span data-ttu-id="6e590-133">Cookie-Compliance</span><span class="sxs-lookup"><span data-stu-id="6e590-133">Cookie compliance</span></span>](cookie-compliance.md)
