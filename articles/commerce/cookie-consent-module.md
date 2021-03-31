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
ms.openlocfilehash: 57c8876f1faf08ce965ccd796551996a8651e2eb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5213937"
---
# <a name="cookie-consent-module"></a><span data-ttu-id="8b778-103">Cookie-Zustimmungsmodul</span><span class="sxs-lookup"><span data-stu-id="8b778-103">Cookie consent module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8b778-104">Dieses Thema behandelt Cookie-Zustimmungsmodule und erläutert, wie sie Webseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="8b778-104">This topic covers cookie consent modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="8b778-105">Das Cookie-Zustimmungsmodul fordert die Benutzer der Website auf, ausdrücklich zuzustimmen, das Cookies für alle Funktionen oder Module, die Browser-Cookies verfolgen, zugelassen werden.</span><span class="sxs-lookup"><span data-stu-id="8b778-105">The cookie consent module prompts site users to explicitly provide consent to allow cookies for any feature or module that tracks browser cookies.</span></span> <span data-ttu-id="8b778-106">Die Zustimmung ist erforderlich, wenn ein Website-Benutzer eine Website zum ersten Mal in einer neuen Browsersitzung durchsucht.</span><span class="sxs-lookup"><span data-stu-id="8b778-106">The consent is required the first time a site user browses a site in a new browser session.</span></span> <span data-ttu-id="8b778-107">Wenn die Einwilligung eingegangen ist, wird sie nachverfolgt und der Benutzer der Website wird nicht erneut zur Einwilligung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="8b778-107">When consent is received, it is tracked and the site user will not be prompted for consent again.</span></span> <span data-ttu-id="8b778-108">Weitere Informationen finden Sie unter [Cookie-Compliance](cookie-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="8b778-108">For more information, see [Cookie compliance](cookie-compliance.md).</span></span>

<span data-ttu-id="8b778-109">Wenn keine Cookie-Zustimmung für Website-Benutzer eingeht, werden Funktionen oder Module, für die eine Cookie-Zustimmung erforderlich ist, nicht auf der Seite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8b778-109">If site user cookie consent is not received, any features or modules that require cookie consent will not be rendered on the page.</span></span> <span data-ttu-id="8b778-110">Das Checkout-Modul, das Social-Share-Modul und die Fujnktion für bevorzugte Stores erfordern beispielsweise die Zustimmung eines Cookies und werden nicht gerendert, wenn die Zustimmung des Website-Benutzers nicht erhalten wird.</span><span class="sxs-lookup"><span data-stu-id="8b778-110">For example, the checkout module, social share module, and preferred store feature all require cookie consent and will not be rendered if site user consent is not received.</span></span> 

<span data-ttu-id="8b778-111">Ein Cookie-Zustimmungsmodul kann für das Header-Fragment einer Seite konfiguriert werden, damit es beim Laden der Seite erzwungen werden kann.</span><span class="sxs-lookup"><span data-stu-id="8b778-111">A cookie consent module can be configured on a page's header fragment so that it can be enforced when the page loads.</span></span> <span data-ttu-id="8b778-112">Das Cookie-Zustimmungsmodul sollte eine eindeutige Meldung enthalten, die den Benutzer der Website über die Verwendung von Cookies auf der Website informiert, und einen Link zur Datenschutzseite der Website bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="8b778-112">The cookie consent module should have a clear message informing the site user about cookie usage on the site and should provide a link to the site's privacy page.</span></span>

<span data-ttu-id="8b778-113">Die folgende Abbildung zeigt ein Beispiel für eine Cookie-Zustimmungsnachricht mit einem Link zur Datenschutzrichtlinie der Website, die in der Kopfzeile einer Website-Seite angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="8b778-113">The following illustration highlights an example of a cookie consent message with a link to the site's privacy policy page displayed on the header of a site page.</span></span>
<span data-ttu-id="8b778-114">![Beispiel eines Cookie-Zustimmungsmoduls](./media/ecommerce-cookieconsent.png)</span><span class="sxs-lookup"><span data-stu-id="8b778-114">![Example of a cookie consent module](./media/ecommerce-cookieconsent.png)</span></span>

## <a name="cookie-consent-module-properties"></a><span data-ttu-id="8b778-115">Eigenschaften des Cookie-Zustimmungsmoduls</span><span class="sxs-lookup"><span data-stu-id="8b778-115">Cookie consent module properties</span></span>

| <span data-ttu-id="8b778-116">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="8b778-116">Property name</span></span>             | <span data-ttu-id="8b778-117">Wert</span><span class="sxs-lookup"><span data-stu-id="8b778-117">Value</span></span>                 | <span data-ttu-id="8b778-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8b778-118">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="8b778-119">Rich Text</span><span class="sxs-lookup"><span data-stu-id="8b778-119">Rich Text</span></span>                  | <span data-ttu-id="8b778-120">Rich Text</span><span class="sxs-lookup"><span data-stu-id="8b778-120">Rich Text</span></span> | <span data-ttu-id="8b778-121">Gibt in einer Rich-Text-Benachrichtigung an Benutzer der Website an, dass die Website Browser-Cookies verwendet und dass Benutzer die Verwendung von Cookies akzeptieren sollten, damit die Website voll funktionsfähig ist.</span><span class="sxs-lookup"><span data-stu-id="8b778-121">Specifies a Rich Text notification to site users that the site uses browser cookies and that users should accept the use of cookies for the site to be fully functional.</span></span> |
| <span data-ttu-id="8b778-122">Verknüpfungen</span><span class="sxs-lookup"><span data-stu-id="8b778-122">Links</span></span> | <span data-ttu-id="8b778-123">URL</span><span class="sxs-lookup"><span data-stu-id="8b778-123">URL</span></span> | <span data-ttu-id="8b778-124">Es kann mindestens ein Links zur Datenschutzseite einer Website hinzugefügt werden, auf der die Arten von Cookies beschrieben werden, die auf der Website verfolgt werden.</span><span class="sxs-lookup"><span data-stu-id="8b778-124">One or more links can be added to a site's privacy page that describes the types of cookies that are tracked on the site.</span></span> |

## <a name="add-a-cookie-consent-module-to-site-pages"></a><span data-ttu-id="8b778-125">Hinzufügen eines Cookie-Zustimmungsmoduls zu den Seiten der Website</span><span class="sxs-lookup"><span data-stu-id="8b778-125">Add a cookie consent module to site pages</span></span>

<span data-ttu-id="8b778-126">Um ein Cookie-Zustimmungsmodul effizient zu mehreren Websiteseiten hinzuzufügen, kann es einem freigegebenen Seitenkopffragment hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="8b778-126">To efficiently add a cookie consent module to multiple site pages, it can be added to a shared page header fragment.</span></span> <span data-ttu-id="8b778-127">Nachdem das Header-Fragment allen Websiteseiten hinzugefügt wurde, wird automatisch eine Cookie-Zustimmungsbenachrichtigung angezeigt, wenn ein Website-Benutzer zum ersten Mal zu einer Website-Seite navigiert.</span><span class="sxs-lookup"><span data-stu-id="8b778-127">After the header fragment is added to all site pages, a cookie consent notification will automatically be rendered the first time a site user navigates to any site page.</span></span>

<span data-ttu-id="8b778-128">Weitere Informationen zu Header-Fragmenten und Modulen finden Sie unter [Header-Modul](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="8b778-128">For more information about header fragments and modules, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8b778-129">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8b778-129">Additional resources</span></span>

[<span data-ttu-id="8b778-130">Übersicht über die Modulbibliothek</span><span class="sxs-lookup"><span data-stu-id="8b778-130">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="8b778-131">Kopfzeilenmodul</span><span class="sxs-lookup"><span data-stu-id="8b778-131">Header module</span></span>](author-header-module.md) 

[<span data-ttu-id="8b778-132">Cookie-Compliance</span><span class="sxs-lookup"><span data-stu-id="8b778-132">Cookie compliance</span></span>](cookie-compliance.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]