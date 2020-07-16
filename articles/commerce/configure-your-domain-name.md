---
title: Konfigurieren Ihres Domänennamens
description: In diesem Thema wird erläutert, wie Sie einen Domänennamen für eine Microsoft Dynamics 365 E-Commerce-Webseite konfigurieren.
author: psimolin
manager: AnnBe
ms.date: 07/02/2020
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
ms.search.industry: Retail
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: afc8c7fffbded82be32357bdeb30546afc8b0957
ms.sourcegitcommit: adf196c51e2b6f532d99c177b4c6778cea8a2efc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/02/2020
ms.locfileid: "3533297"
---
# <a name="configure-your-domain-name"></a><span data-ttu-id="e3b1a-103">Konfigurieren Ihres Domänennamens</span><span class="sxs-lookup"><span data-stu-id="e3b1a-103">Configure your domain name</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="e3b1a-104">In diesem Thema wird erläutert, wie Sie einen Domänennamen für eine Microsoft Dynamics 365 E-Commerce-Webseite konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="e3b1a-104">This topic explains how to configure a domain name for a Microsoft Dynamics 365 e-commerce site.</span></span> 

## <a name="add-domains-during-e-commerce-initialization"></a><span data-ttu-id="e3b1a-105">Domänen während der E-Commerce-Initialisierung hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e3b1a-105">Add domains during e-Commerce initialization</span></span>

<span data-ttu-id="e3b1a-106">Wenn Sie Domänen Ihrer E-Commerce-Umgebung hinzufügen, initialisieren Sie E-Commerce wie beschrieben in [Eine neue E-Commerce-Webseite bereitstellen](deploy-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="e3b1a-106">To associate domains with your e-commerce environment, initialize e-Commerce as described in [Deploy a new e-Commerce site](deploy-ecommerce-site.md).</span></span> <span data-ttu-id="e3b1a-107">Während der Initialisierung werden Sie gebeten, Informationen bereitzustellen, die zur Bereitstellung der E-Commerce-Umgebung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e3b1a-107">During initialization, you're asked to provide information that will be used to provision your e-Commerce environment.</span></span> <span data-ttu-id="e3b1a-108">Im Feld **Unterstützte Hostnamen** wählen Sie alle Domänen hinzufügen, die Sie mit dieser Umgebung verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="e3b1a-108">In the **Supported host names** field, add all the domains that you plan to use with this environment.</span></span> <span data-ttu-id="e3b1a-109">Mehrere Domänen sollten mit Trennzeichen getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="e3b1a-109">Multiple domains should be separated with semi-colon.</span></span> <span data-ttu-id="e3b1a-110">Auf diese Weise werden die Domänen in alle erforderlichen E-Commerce-Komponenten konfiguriert, und sie sind für die Verwendung bereit, wenn Sie vom Datenverkehr aus Ihrem Content-Vertriebsnetz (CDN) oder vom Webserver wechseln und ihn in den E-Commerce-Front-End anzeigen.</span><span class="sxs-lookup"><span data-stu-id="e3b1a-110">In this way, the domains are configured in all the required e-Commerce components, and they are ready to be used when you switch traffic from your content delivery network (CDN) or web server and point it to the e-Commerce front ends.</span></span>

## <a name="add-domains-after-e-commerce-initialization"></a><span data-ttu-id="e3b1a-111">Domänen hinzufügen,nach der E-Commerce-Initialisierung</span><span class="sxs-lookup"><span data-stu-id="e3b1a-111">Add domains after e-Commerce initialization</span></span>

<span data-ttu-id="e3b1a-112">Wenn Sie neue Domänen mit der E-Commerce-Umgebung nach der E-Commerce-Initialisierung zuordnen möchten, müssen Sie eine Serviceanforderung senden.</span><span class="sxs-lookup"><span data-stu-id="e3b1a-112">To associate new domains with your e-Commerce environment after e-Commerce initialization, you must submit a service request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e3b1a-113">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e3b1a-113">Additional resources</span></span>

[<span data-ttu-id="e3b1a-114">Bereitstellen einer neuen E-Commerce-Webseite</span><span class="sxs-lookup"><span data-stu-id="e3b1a-114">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="e3b1a-115">Erstellen einer E-Commerce-Webseite</span><span class="sxs-lookup"><span data-stu-id="e3b1a-115">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="e3b1a-116">Zuordnen einer Onlinewebseite zu einem Kanal</span><span class="sxs-lookup"><span data-stu-id="e3b1a-116">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="e3b1a-117">Verwalten von robots.txt-Dateien</span><span class="sxs-lookup"><span data-stu-id="e3b1a-117">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="e3b1a-118">URL-Weiterleitungen in großen Mengen hochladen</span><span class="sxs-lookup"><span data-stu-id="e3b1a-118">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="e3b1a-119">Einrichten eines B2C-Mandanten in Commerce</span><span class="sxs-lookup"><span data-stu-id="e3b1a-119">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="e3b1a-120">Einrichten angepasster Seiten für die Benutzeranmeldungen</span><span class="sxs-lookup"><span data-stu-id="e3b1a-120">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="e3b1a-121">Konfigurieren Sie mehrere B2C-Mandanten in einer Commerce-Umgebung</span><span class="sxs-lookup"><span data-stu-id="e3b1a-121">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="e3b1a-122">Hinzufügen von Unterstützung für ein Content Delivery Network (CDN)</span><span class="sxs-lookup"><span data-stu-id="e3b1a-122">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="e3b1a-123">Standortbasierte Shop-Erkennung aktivieren</span><span class="sxs-lookup"><span data-stu-id="e3b1a-123">Enable location-based store detection</span></span>](enable-store-detection.md)
