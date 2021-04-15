---
title: Konfigurieren Ihres Domänennamens
description: In diesem Thema wird erläutert, wie Sie einen Domänennamen für eine Microsoft Dynamics 365 E-Commerce-Webseite konfigurieren.
author: psimolin
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
ms.search.industry: Retail
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3d41168da44100a09c58b8c05367ab45bbd62a30
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796050"
---
# <a name="configure-your-domain-name"></a><span data-ttu-id="9be65-103">Konfigurieren Ihres Domänennamens</span><span class="sxs-lookup"><span data-stu-id="9be65-103">Configure your domain name</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="9be65-104">In diesem Thema wird erläutert, wie Sie einen Domänennamen für eine Microsoft Dynamics 365 E-Commerce-Webseite konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="9be65-104">This topic explains how to configure a domain name for a Microsoft Dynamics 365 e-commerce site.</span></span> 

## <a name="add-domains-during-e-commerce-initialization"></a><span data-ttu-id="9be65-105">Domänen während der E-Commerce-Initialisierung hinzufügen</span><span class="sxs-lookup"><span data-stu-id="9be65-105">Add domains during e-commerce initialization</span></span>

<span data-ttu-id="9be65-106">Um Ihrer Dynamics 365 Commerce-E-Commerce-Umgebung Domänen zuzuordnen, initialisieren Sie E-Commerce wie beschrieben in [Einen neuen E-Commerce-Mandanten bereitstellen](deploy-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="9be65-106">To associate domains with your Dynamics 365 Commerce e-commerce environment, initialize e-commerce as described in [Deploy a new e-commerce tenant](deploy-ecommerce-site.md).</span></span> <span data-ttu-id="9be65-107">Während der Initialisierung werden Sie gebeten, Informationen bereitzustellen, die zur Bereitstellung Ihrer E-Commerce-Umgebung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9be65-107">During initialization, you're asked to provide information that will be used to provision your e-commerce environment.</span></span> <span data-ttu-id="9be65-108">Im Feld **Unterstützte Hostnamen** wählen Sie alle Domänen hinzufügen, die Sie mit dieser Umgebung verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="9be65-108">In the **Supported host names** field, add all the domains that you plan to use with this environment.</span></span> <span data-ttu-id="9be65-109">Mehrere Domänen sollten mit Trennzeichen getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="9be65-109">Multiple domains should be separated with semi-colon.</span></span> <span data-ttu-id="9be65-110">Auf diese Weise werden die Domänen in allen erforderlichen E-Commerce-Komponenten konfiguriert, und sie sind für die Verwendung bereit, wenn Sie von Ihrem Content Delivery Network (CDN) oder Webserver Datenverkehr umschalten und mit ihm auf die E-Commerce-Front-Ends zeigen.</span><span class="sxs-lookup"><span data-stu-id="9be65-110">In this way, the domains are configured in all the required Commerce components, and they are ready to be used when you switch traffic from your content delivery network (CDN) or web server and point it to the e-commerce front ends.</span></span>

## <a name="add-domains-after-e-commerce-initialization"></a><span data-ttu-id="9be65-111">Domänen nach der E-Commerce-Initialisierung hinzufügen</span><span class="sxs-lookup"><span data-stu-id="9be65-111">Add domains after e-commerce initialization</span></span>

<span data-ttu-id="9be65-112">Um nach der E-Commerce-Initialisierung neue Domänen zu Ihrer E-Commerce-Umgebung zuzuordnen, müssen Sie eine Dienstanforderung übermitteln.</span><span class="sxs-lookup"><span data-stu-id="9be65-112">To associate new domains with your e-commerce environment after e-commerce initialization, you must submit a service request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9be65-113">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9be65-113">Additional resources</span></span>

[<span data-ttu-id="9be65-114">Neuen E-Commerce-Mandanten bereitstellen</span><span class="sxs-lookup"><span data-stu-id="9be65-114">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="9be65-115">E-Commerce-Website erstellen</span><span class="sxs-lookup"><span data-stu-id="9be65-115">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="9be65-116">Zuordnen einer Dynamics 365 Commerce-Website zu einem Onlinekanal</span><span class="sxs-lookup"><span data-stu-id="9be65-116">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="9be65-117">Robots.txt-Dateien verwalten</span><span class="sxs-lookup"><span data-stu-id="9be65-117">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="9be65-118">URL-Umleitungen in Massen hochladen</span><span class="sxs-lookup"><span data-stu-id="9be65-118">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="9be65-119">Einrichten eines B2C-Mandanten in Commerce</span><span class="sxs-lookup"><span data-stu-id="9be65-119">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="9be65-120">Einrichten angepasster Seiten für die Benutzeranmeldungen</span><span class="sxs-lookup"><span data-stu-id="9be65-120">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="9be65-121">Konfigurieren Sie mehrere B2C-Mandanten in einer Commerce-Umgebung</span><span class="sxs-lookup"><span data-stu-id="9be65-121">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="9be65-122">Hinzufügen von Unterstützung für ein Content Delivery Network (CDN)</span><span class="sxs-lookup"><span data-stu-id="9be65-122">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="9be65-123">Standortbasierte Shop-Erkennung aktivieren</span><span class="sxs-lookup"><span data-stu-id="9be65-123">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]