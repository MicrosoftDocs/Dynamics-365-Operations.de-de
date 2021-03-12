---
title: Standortbasierte Shop-Erkennung aktivieren
description: In diesem Thema wird beschrieben, wie ortsbasierte Shoperkennung für Ihre Dynamics 365 Commerce Site erkannt wird.
author: brianshook
manager: annbe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3f7e9a3acde508f405ce85f125db552c3ae3656b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000721"
---
# <a name="enable-location-based-store-detection"></a><span data-ttu-id="7165e-103">Standortbasierte Shop-Erkennung aktivieren</span><span class="sxs-lookup"><span data-stu-id="7165e-103">Enable location-based store detection</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="7165e-104">In diesem Thema wird beschrieben, wie ortsbasierte Shoperkennung für Ihre Dynamics 365 Commerce Site erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="7165e-104">This topic describes how to turn on location-based store detection for your Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="7165e-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="7165e-105">Overview</span></span>

<span data-ttu-id="7165e-106">Mit ortsbasierter Shoperkennung im Handel können Sie Standortsinhalt für Debitoren auf Grundlage des Lagerplatzes angeben.</span><span class="sxs-lookup"><span data-stu-id="7165e-106">Location-based store detection in Commerce lets you provide relevant site content to customers, based on their location.</span></span> <span data-ttu-id="7165e-107">Wenn ortsbasierte Shoperkennung aktiviert ist, wird der Handelsrendering-Service die Länder/-Regionsinformationen von die IP-Adresse des Webbrowsers des Debitors verwenden, um den Debitor an die beste geografische Standortskonfiguration zu verweisen, die verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="7165e-107">When location-based store detection is turned on, the Commerce rendering service uses the country/region information from the IP address of the customer's web browser to direct the customer to the best geographical site configuration that is available.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="7165e-108">Datenschutzhinweis</span><span class="sxs-lookup"><span data-stu-id="7165e-108">Privacy notice</span></span>

<span data-ttu-id="7165e-109">Wenn Sie die ortsbasierte Shoperkennungsfunktion aktivieren, werden Informationen im Browser des Debitors für ein Microsoft-Lagerplatz-Service gesendet.</span><span class="sxs-lookup"><span data-stu-id="7165e-109">If you turn on the location-based store detection feature, information from the customer's browser is sent to a Microsoft location service.</span></span> <span data-ttu-id="7165e-110">Diese Angabe wird dann verwendet, um den Debitoreninhalt bereitzustellen, der für die elektronische Adresse relevant ist.</span><span class="sxs-lookup"><span data-stu-id="7165e-110">This information is then used to provide the customer content that is relevant to his or her location.</span></span> <span data-ttu-id="7165e-111">Beide Informationen, die vom im Browser des Debitors und von den standortbasierten Informationen übermittelt wird, die an den Debitor zurückgegeben wird, sind abhängig von Informationen zum Datenschutz und Cookiekompatibilitätspolitischen Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="7165e-111">Both the information that is sent from the customer's browser and the location-based information that is returned to the customer are subject to privacy and cookie compliance policies.</span></span>

## <a name="turn-on-location-based-store-detection"></a><span data-ttu-id="7165e-112">Standortbasierte Shop-Erkennung aktivieren</span><span class="sxs-lookup"><span data-stu-id="7165e-112">Turn on location-based store detection</span></span>

<span data-ttu-id="7165e-113">Um ortsbasierte Shoperkennung im Handel zu aktivieren, gehen Sie folgendermaßen vor.</span><span class="sxs-lookup"><span data-stu-id="7165e-113">To turn on location-based store detection in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="7165e-114">Im Erstellungstool gehen Sie zu Ihrer Site.</span><span class="sxs-lookup"><span data-stu-id="7165e-114">In the authoring tool, go to your site.</span></span>
1. <span data-ttu-id="7165e-115">Wählen Sie im linken Navigationsbereich **Site-Verwaltung** aus.</span><span class="sxs-lookup"><span data-stu-id="7165e-115">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="7165e-116">Wählen Sie **Site-Einstellungen**.</span><span class="sxs-lookup"><span data-stu-id="7165e-116">Select **Site Settings**.</span></span>
1. <span data-ttu-id="7165e-117">Hier können Sie die Option **Aktivieren basierend auf Shoperkennung** auf **Aktiviert** festlegen.</span><span class="sxs-lookup"><span data-stu-id="7165e-117">Set the **Enable location based store detection** option to **On**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7165e-118">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7165e-118">Additional resources</span></span>

[<span data-ttu-id="7165e-119">Domänennamen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="7165e-119">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="7165e-120">Neuen E-Commerce-Mandanten bereitstellen</span><span class="sxs-lookup"><span data-stu-id="7165e-120">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="7165e-121">E-Commerce-Website erstellen</span><span class="sxs-lookup"><span data-stu-id="7165e-121">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="7165e-122">Zuordnen einer Dynamics 365 Commerce-Website zu einem Onlinekanal</span><span class="sxs-lookup"><span data-stu-id="7165e-122">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="7165e-123">Robots.txt-Dateien verwalten</span><span class="sxs-lookup"><span data-stu-id="7165e-123">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="7165e-124">URL-Umleitungen in Massen hochladen</span><span class="sxs-lookup"><span data-stu-id="7165e-124">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="7165e-125">Einrichten eines B2C-Mandanten in Commerce</span><span class="sxs-lookup"><span data-stu-id="7165e-125">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="7165e-126">Einrichten angepasster Seiten für die Benutzeranmeldungen</span><span class="sxs-lookup"><span data-stu-id="7165e-126">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="7165e-127">Konfigurieren Sie mehrere B2C-Mandanten in einer Commerce-Umgebung</span><span class="sxs-lookup"><span data-stu-id="7165e-127">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="7165e-128">Hinzufügen von Unterstützung für ein Content Delivery Network (CDN)</span><span class="sxs-lookup"><span data-stu-id="7165e-128">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)
