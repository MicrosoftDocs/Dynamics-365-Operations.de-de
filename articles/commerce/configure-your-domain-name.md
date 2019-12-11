---
title: Konfigurieren Ihres Domänennamens
description: In diesem Thema wird erläutert, wie Sie einen Domänennamen für eine Microsoft Dynamics 365 E-Commerce-Webseite konfigurieren.
author: psimolin
manager: AnnBe
ms.date: 10/01/2019
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
ms.openlocfilehash: 7a988f533757cc3f8555fcf4fb724a22a5b014f8
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770457"
---
# <a name="configure-your-domain-name"></a><span data-ttu-id="341aa-103">Konfigurieren Ihres Domänennamens</span><span class="sxs-lookup"><span data-stu-id="341aa-103">Configure your domain name</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="341aa-104">In diesem Thema wird erläutert, wie Sie einen Domänennamen für eine Microsoft Dynamics 365 E-Commerce-Webseite konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="341aa-104">This topic explains how to configure a domain name for a Microsoft Dynamics 365 e-commerce site.</span></span> 

## <a name="add-domains-during-e-commerce-initialization"></a><span data-ttu-id="341aa-105">Domänen während der E-Commerce-Initialisierung hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="341aa-105">Add domains during e-Commerce initialization</span></span>

<span data-ttu-id="341aa-106">Wenn Sie Domänen Ihrer E-Commerce-Umgebung hinzufügen, initialisieren Sie E-Commerce wie beschrieben in [Eine neue E-Commerce-Webseite bereitstellen](deploy-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="341aa-106">To associate domains with your e-commerce environment, initialize e-Commerce as described in [Deploy a new e-Commerce site](deploy-ecommerce-site.md).</span></span> <span data-ttu-id="341aa-107">Während der Initialisierung werden Sie gebeten, Informationen bereitzustellen, die zur Bereitstellung der E-Commerce-Umgebung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="341aa-107">During initialization, you're asked to provide information that will be used to provision your e-Commerce environment.</span></span> <span data-ttu-id="341aa-108">Im Feld **Unterstützte Hostnamen** wählen Sie alle Domänen hinzufügen, die Sie mit dieser Umgebung verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="341aa-108">In the **Supported host names** field, add all the domains that you plan to use with this environment.</span></span> <span data-ttu-id="341aa-109">Mehrere Domänen sollten mit Trennzeichen getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="341aa-109">Multiple domains should be separated with semi-colon.</span></span> <span data-ttu-id="341aa-110">Auf diese Weise werden die Domänen in alle erforderlichen E-Commerce-Komponenten konfiguriert, und sie sind für die Verwendung bereit, wenn Sie vom Datenverkehr aus Ihrem Content-Vertriebsnetz (CDN) oder vom Webserver wechseln und ihn in den E-Commerce-Front-End anzeigen.</span><span class="sxs-lookup"><span data-stu-id="341aa-110">In this way, the domains are configured in all the required e-Commerce components, and they are ready to be used when you switch traffic from your content delivery network (CDN) or web server and point it to the e-Commerce front ends.</span></span>

## <a name="add-domains-after-e-commerce-initialization"></a><span data-ttu-id="341aa-111">Domänen hinzufügen,nach der E-Commerce-Initialisierung</span><span class="sxs-lookup"><span data-stu-id="341aa-111">Add domains after e-Commerce initialization</span></span>

<span data-ttu-id="341aa-112">Wenn Sie neue Domänen mit der E-Commerce-Umgebung nach der E-Commerce-Initialisierung zuordnen möchten, müssen Sie eine Serviceanforderung senden.</span><span class="sxs-lookup"><span data-stu-id="341aa-112">To associate new domains with your e-Commerce environment after e-Commerce initialization, you must submit a service request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="341aa-113">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="341aa-113">Additional resources</span></span>

[<span data-ttu-id="341aa-114">Onlineshop – Überblick</span><span class="sxs-lookup"><span data-stu-id="341aa-114">Online store overview</span></span>](online-store-overview.md)

[<span data-ttu-id="341aa-115">Erstellen einer E-Commerce-Webseite</span><span class="sxs-lookup"><span data-stu-id="341aa-115">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="341aa-116">Bereitstellen einer neuen E-Commerce-Webseite</span><span class="sxs-lookup"><span data-stu-id="341aa-116">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="341aa-117">Zuordnen einer Onlinewebseite zu einem Kanal</span><span class="sxs-lookup"><span data-stu-id="341aa-117">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="341aa-118">Unterstützung für ein Content Delivery Network (CDN) hinzufügen</span><span class="sxs-lookup"><span data-stu-id="341aa-118">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="341aa-119">Standortbasierte Shop-Erkennung aktivieren</span><span class="sxs-lookup"><span data-stu-id="341aa-119">Enable location-based store detection</span></span>](enable-store-detection.md)

[<span data-ttu-id="341aa-120">Einrichten angepasster Seiten für die Benutzeranmeldungen</span><span class="sxs-lookup"><span data-stu-id="341aa-120">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)
