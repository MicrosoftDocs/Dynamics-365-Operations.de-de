---
title: Standortbasierte Shop-Erkennung aktivieren
description: In diesem Thema wird beschrieben, wie ortsbasierte Shoperkennung für Ihre Dynamics 365 Commerce Site erkannt wird.
author: brianshook
manager: annbe
ms.date: 10/01/2019
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
ms.openlocfilehash: 304d8d2f05916295b9c6320561d6a25ff40df955
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003095"
---
# <a name="enable-location-based-store-detection"></a><span data-ttu-id="117dc-103">Standortbasierte Shop-Erkennung aktivieren</span><span class="sxs-lookup"><span data-stu-id="117dc-103">Enable location-based store detection</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="117dc-104">In diesem Thema wird beschrieben, wie ortsbasierte Shoperkennung für Ihre Dynamics 365 Commerce Site erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="117dc-104">This topic describes how to turn on location-based store detection for your Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="117dc-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="117dc-105">Overview</span></span>

<span data-ttu-id="117dc-106">Mit ortsbasierter Shoperkennung im Handel können Sie Standortsinhalt für Debitoren auf Grundlage des Lagerplatzes angeben.</span><span class="sxs-lookup"><span data-stu-id="117dc-106">Location-based store detection in Commerce lets you provide relevant site content to customers, based on their location.</span></span> <span data-ttu-id="117dc-107">Wenn ortsbasierte Shoperkennung aktiviert ist, wird der Handelsrendering-Service die Länder/-Regionsinformationen von die IP-Adresse des Webbrowsers des Debitors verwenden, um den Debitor an die beste geografische Standortskonfiguration zu verweisen, die verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="117dc-107">When location-based store detection is turned on, the Commerce rendering service uses the country/region information from the IP address of the customer's web browser to direct the customer to the best geographical site configuration that is available.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="117dc-108">Datenschutzhinweis</span><span class="sxs-lookup"><span data-stu-id="117dc-108">Privacy notice</span></span>

<span data-ttu-id="117dc-109">Wenn Sie die ortsbasierte Shoperkennungsfunktion aktivieren, werden Informationen im Browser des Debitors für ein Microsoft-Lagerplatz-Service gesendet.</span><span class="sxs-lookup"><span data-stu-id="117dc-109">If you turn on the location-based store detection feature, information from the customer's browser is sent to a Microsoft location service.</span></span> <span data-ttu-id="117dc-110">Diese Angabe wird dann verwendet, um den Debitoreninhalt bereitzustellen, der für die elektronische Adresse relevant ist.</span><span class="sxs-lookup"><span data-stu-id="117dc-110">This information is then used to provide the customer content that is relevant to his or her location.</span></span> <span data-ttu-id="117dc-111">Beide Informationen, die vom im Browser des Debitors und von den standortbasierten Informationen übermittelt wird, die an den Debitor zurückgegeben wird, sind abhängig von Informationen zum Datenschutz und Cookiekompatibilitätspolitischen Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="117dc-111">Both the information that is sent from the customer's browser and the location-based information that is returned to the customer are subject to privacy and cookie compliance policies.</span></span>

## <a name="turn-on-location-based-store-detection"></a><span data-ttu-id="117dc-112">Standortbasierte Shop-Erkennung aktivieren</span><span class="sxs-lookup"><span data-stu-id="117dc-112">Turn on location-based store detection</span></span>

<span data-ttu-id="117dc-113">Um ortsbasierte Shoperkennung im Handel zu aktivieren, gehen Sie folgendermaßen vor.</span><span class="sxs-lookup"><span data-stu-id="117dc-113">To turn on location-based store detection in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="117dc-114">Im Erstellungstool gehen Sie zu Ihrer Site.</span><span class="sxs-lookup"><span data-stu-id="117dc-114">In the authoring tool, go to your site.</span></span>
1. <span data-ttu-id="117dc-115">Wählen Sie im linken Navigationsbereich **Site-Verwaltung** aus.</span><span class="sxs-lookup"><span data-stu-id="117dc-115">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="117dc-116">Wählen Sie **Site-Einstellungen**.</span><span class="sxs-lookup"><span data-stu-id="117dc-116">Select **Site Settings**.</span></span>
1. <span data-ttu-id="117dc-117">Hier können Sie die Option **Aktivieren basierend auf Shoperkennung** auf **Aktiviert** festlegen.</span><span class="sxs-lookup"><span data-stu-id="117dc-117">Set the **Enable location based store detection** option to **On**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="117dc-118">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="117dc-118">Additional resources</span></span>

[<span data-ttu-id="117dc-119">Konfigurieren Ihres Domänennamens</span><span class="sxs-lookup"><span data-stu-id="117dc-119">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="117dc-120">Bereitstellen einer neuen E-Commerce-Webseite</span><span class="sxs-lookup"><span data-stu-id="117dc-120">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="117dc-121">Erstellen einer E-Commerce-Webseite</span><span class="sxs-lookup"><span data-stu-id="117dc-121">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="117dc-122">Zuordnen einer Onlinewebseite zu einem Kanal</span><span class="sxs-lookup"><span data-stu-id="117dc-122">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="117dc-123">Verwalten von robots.txt-Dateien</span><span class="sxs-lookup"><span data-stu-id="117dc-123">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="117dc-124">Einrichten angepasster Seiten für die Benutzeranmeldungen</span><span class="sxs-lookup"><span data-stu-id="117dc-124">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="117dc-125">Unterstützung für ein Content Delivery Network (CDN) hinzufügen</span><span class="sxs-lookup"><span data-stu-id="117dc-125">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)
