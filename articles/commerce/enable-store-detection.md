---
title: Standortbasierte Shop-Erkennung aktivieren
description: In diesem Thema wird beschrieben, wie ortsbasierte Shoperkennung für Ihre Dynamics 365 Commerce Site erkannt wird.
author: brianshook
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3e26c3130914ebef5a63b79c477d7d5846fd5b71
ms.sourcegitcommit: cabd991fda2bfcabb55db84c225b24a7bb061631
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6027599"
---
# <a name="enable-location-based-store-detection"></a><span data-ttu-id="34e00-103">Standortbasierte Shop-Erkennung aktivieren</span><span class="sxs-lookup"><span data-stu-id="34e00-103">Enable location-based store detection</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="34e00-104">In diesem Thema wird beschrieben, wie ortsbasierte Shoperkennung für Ihre Dynamics 365 Commerce Site erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="34e00-104">This topic describes how to turn on location-based store detection for your Dynamics 365 Commerce site.</span></span>

<span data-ttu-id="34e00-105">Mit ortsbasierter Shoperkennung im Handel können Sie Standortsinhalt für Debitoren auf Grundlage des Lagerplatzes angeben.</span><span class="sxs-lookup"><span data-stu-id="34e00-105">Location-based store detection in Commerce lets you provide relevant site content to customers, based on their location.</span></span> <span data-ttu-id="34e00-106">Wenn ortsbasierte Shoperkennung aktiviert ist, wird der Handelsrendering-Service die Länder/-Regionsinformationen von die IP-Adresse des Webbrowsers des Debitors verwenden, um den Debitor an die beste geografische Standortskonfiguration zu verweisen, die verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="34e00-106">When location-based store detection is turned on, the Commerce rendering service uses the country/region information from the IP address of the customer's web browser to direct the customer to the best geographical site configuration that is available.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="34e00-107">Datenschutzhinweis</span><span class="sxs-lookup"><span data-stu-id="34e00-107">Privacy notice</span></span>

<span data-ttu-id="34e00-108">Wenn Sie die ortsbasierte Shoperkennungsfunktion aktivieren, werden Informationen im Browser des Debitors für ein Microsoft-Lagerplatz-Service gesendet.</span><span class="sxs-lookup"><span data-stu-id="34e00-108">If you turn on the location-based store detection feature, information from the customer's browser is sent to a Microsoft location service.</span></span> <span data-ttu-id="34e00-109">Diese Angabe wird dann verwendet, um den Debitoreninhalt bereitzustellen, der für die Adresse des Debitors relevant ist.</span><span class="sxs-lookup"><span data-stu-id="34e00-109">This information is then used to provide the customer content that is relevant to the customer's location.</span></span> <span data-ttu-id="34e00-110">Beide Informationen, die vom im Browser des Debitors und von den standortbasierten Informationen übermittelt wird, die an den Debitor zurückgegeben wird, sind abhängig von Informationen zum Datenschutz und Cookiekompatibilitätspolitischen Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="34e00-110">Both the information that is sent from the customer's browser and the location-based information that is returned to the customer are subject to privacy and cookie compliance policies.</span></span>

## <a name="turn-on-location-based-store-detection"></a><span data-ttu-id="34e00-111">Standortbasierte Shop-Erkennung aktivieren</span><span class="sxs-lookup"><span data-stu-id="34e00-111">Turn on location-based store detection</span></span>

<span data-ttu-id="34e00-112">Um ortsbasierte Shoperkennung im Handel zu aktivieren, gehen Sie folgendermaßen vor.</span><span class="sxs-lookup"><span data-stu-id="34e00-112">To turn on location-based store detection in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="34e00-113">Im Erstellungstool gehen Sie zu Ihrer Site.</span><span class="sxs-lookup"><span data-stu-id="34e00-113">In the authoring tool, go to your site.</span></span>
1. <span data-ttu-id="34e00-114">Wählen Sie im linken Navigationsbereich **Site-Verwaltung** aus.</span><span class="sxs-lookup"><span data-stu-id="34e00-114">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="34e00-115">Wählen Sie **Site-Einstellungen**.</span><span class="sxs-lookup"><span data-stu-id="34e00-115">Select **Site Settings**.</span></span>
1. <span data-ttu-id="34e00-116">Hier können Sie die Option **Aktivieren basierend auf Shoperkennung** auf **Aktiviert** festlegen.</span><span class="sxs-lookup"><span data-stu-id="34e00-116">Set the **Enable location based store detection** option to **On**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="34e00-117">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="34e00-117">Additional resources</span></span>

[<span data-ttu-id="34e00-118">Domänennamen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="34e00-118">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="34e00-119">Neuen E-Commerce-Mandanten bereitstellen</span><span class="sxs-lookup"><span data-stu-id="34e00-119">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="34e00-120">E-Commerce-Website erstellen</span><span class="sxs-lookup"><span data-stu-id="34e00-120">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="34e00-121">Zuordnen einer Dynamics 365 Commerce-Website zu einem Onlinekanal</span><span class="sxs-lookup"><span data-stu-id="34e00-121">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="34e00-122">Robots.txt-Dateien verwalten</span><span class="sxs-lookup"><span data-stu-id="34e00-122">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="34e00-123">URL-Umleitungen in Massen hochladen</span><span class="sxs-lookup"><span data-stu-id="34e00-123">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="34e00-124">Einrichten eines B2C-Mandanten in Commerce</span><span class="sxs-lookup"><span data-stu-id="34e00-124">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="34e00-125">Einrichten angepasster Seiten für die Benutzeranmeldungen</span><span class="sxs-lookup"><span data-stu-id="34e00-125">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="34e00-126">Konfigurieren Sie mehrere B2C-Mandanten in einer Commerce-Umgebung</span><span class="sxs-lookup"><span data-stu-id="34e00-126">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="34e00-127">Hinzufügen von Unterstützung für ein Content Delivery Network (CDN)</span><span class="sxs-lookup"><span data-stu-id="34e00-127">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
