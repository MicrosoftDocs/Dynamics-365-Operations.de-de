---
title: Standortbasierte Shop-Erkennung aktivieren
description: In diesem Thema wird beschrieben, wie ortsbasierte Shoperkennung für Ihre Dynamics 365 Commerce Site erkannt wird.
author: brianshook
manager: annbe
ms.date: 03/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 66ffe56f9d969c9d62ed4ff49f0848fab7e58a56
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096868"
---
# <a name="enable-location-based-store-detection"></a><span data-ttu-id="6a4ae-103">Standortbasierte Shop-Erkennung aktivieren</span><span class="sxs-lookup"><span data-stu-id="6a4ae-103">Enable location-based store detection</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="6a4ae-104">In diesem Thema wird beschrieben, wie ortsbasierte Shoperkennung für Ihre Dynamics 365 Commerce Site erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="6a4ae-104">This topic describes how to turn on location-based store detection for your Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="6a4ae-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="6a4ae-105">Overview</span></span>

<span data-ttu-id="6a4ae-106">Mit ortsbasierter Shoperkennung im Handel können Sie Standortsinhalt für Debitoren auf Grundlage des Lagerplatzes angeben.</span><span class="sxs-lookup"><span data-stu-id="6a4ae-106">Location-based store detection in Commerce lets you provide relevant site content to customers, based on their location.</span></span> <span data-ttu-id="6a4ae-107">Wenn ortsbasierte Shoperkennung aktiviert ist, wird der Handelsrendering-Service die Länder/-Regionsinformationen von die IP-Adresse des Webbrowsers des Debitors verwenden, um den Debitor an die beste geografische Standortskonfiguration zu verweisen, die verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="6a4ae-107">When location-based store detection is turned on, the Commerce rendering service uses the country/region information from the IP address of the customer's web browser to direct the customer to the best geographical site configuration that is available.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="6a4ae-108">Datenschutzhinweis</span><span class="sxs-lookup"><span data-stu-id="6a4ae-108">Privacy notice</span></span>

<span data-ttu-id="6a4ae-109">Wenn Sie die ortsbasierte Shoperkennungsfunktion aktivieren, werden Informationen im Browser des Debitors für ein Microsoft-Lagerplatz-Service gesendet.</span><span class="sxs-lookup"><span data-stu-id="6a4ae-109">If you turn on the location-based store detection feature, information from the customer's browser is sent to a Microsoft location service.</span></span> <span data-ttu-id="6a4ae-110">Diese Angabe wird dann verwendet, um den Debitoreninhalt bereitzustellen, der für die elektronische Adresse relevant ist.</span><span class="sxs-lookup"><span data-stu-id="6a4ae-110">This information is then used to provide the customer content that is relevant to his or her location.</span></span> <span data-ttu-id="6a4ae-111">Beide Informationen, die vom im Browser des Debitors und von den standortbasierten Informationen übermittelt wird, die an den Debitor zurückgegeben wird, sind abhängig von Informationen zum Datenschutz und Cookiekompatibilitätspolitischen Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="6a4ae-111">Both the information that is sent from the customer's browser and the location-based information that is returned to the customer are subject to privacy and cookie compliance policies.</span></span>

## <a name="turn-on-location-based-store-detection"></a><span data-ttu-id="6a4ae-112">Standortbasierte Shop-Erkennung aktivieren</span><span class="sxs-lookup"><span data-stu-id="6a4ae-112">Turn on location-based store detection</span></span>

<span data-ttu-id="6a4ae-113">Um ortsbasierte Shoperkennung im Handel zu aktivieren, gehen Sie folgendermaßen vor.</span><span class="sxs-lookup"><span data-stu-id="6a4ae-113">To turn on location-based store detection in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="6a4ae-114">Im Erstellungstool gehen Sie zu Ihrer Site.</span><span class="sxs-lookup"><span data-stu-id="6a4ae-114">In the authoring tool, go to your site.</span></span>
1. <span data-ttu-id="6a4ae-115">Wählen Sie im linken Navigationsbereich **Site-Verwaltung** aus.</span><span class="sxs-lookup"><span data-stu-id="6a4ae-115">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="6a4ae-116">Wählen Sie **Site-Einstellungen**.</span><span class="sxs-lookup"><span data-stu-id="6a4ae-116">Select **Site Settings**.</span></span>
1. <span data-ttu-id="6a4ae-117">Hier können Sie die Option **Aktivieren basierend auf Shoperkennung** auf **Aktiviert** festlegen.</span><span class="sxs-lookup"><span data-stu-id="6a4ae-117">Set the **Enable location based store detection** option to **On**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6a4ae-118">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6a4ae-118">Additional resources</span></span>

[<span data-ttu-id="6a4ae-119">Ihren Domänennamen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="6a4ae-119">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="6a4ae-120">Bereitstellen einer neuen E-Commerce-Webseite</span><span class="sxs-lookup"><span data-stu-id="6a4ae-120">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="6a4ae-121">Onlineshopkanal einrichten</span><span class="sxs-lookup"><span data-stu-id="6a4ae-121">Set up an online store channel</span></span>](online-stores.md)

[<span data-ttu-id="6a4ae-122">E-Commerce-Site erstellen</span><span class="sxs-lookup"><span data-stu-id="6a4ae-122">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="6a4ae-123">Zuordnen einer Onlinewebseite zu einem Kanal</span><span class="sxs-lookup"><span data-stu-id="6a4ae-123">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="6a4ae-124">Verwalten von robots.txt-Dateien</span><span class="sxs-lookup"><span data-stu-id="6a4ae-124">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="6a4ae-125">URL-Weiterleitungen in großen Mengen hochladen</span><span class="sxs-lookup"><span data-stu-id="6a4ae-125">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="6a4ae-126">Einrichten eines B2C-Mandanten in Commerce</span><span class="sxs-lookup"><span data-stu-id="6a4ae-126">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="6a4ae-127">Einrichten angepasster Seiten für die Benutzeranmeldungen</span><span class="sxs-lookup"><span data-stu-id="6a4ae-127">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="6a4ae-128">Konfigurieren Sie mehrere B2C-Mandanten in einer Commerce-Umgebung</span><span class="sxs-lookup"><span data-stu-id="6a4ae-128">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="6a4ae-129">Hinzufügen von Unterstützung für ein Content Delivery Network (CDN)</span><span class="sxs-lookup"><span data-stu-id="6a4ae-129">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)
