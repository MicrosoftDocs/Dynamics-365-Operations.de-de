---
title: Dynamics 365 Commerce-Evaluierungsumgebung – Überblick
description: Dieses Thema enthält eine Übersicht der Microsoft Dynamics 365 Commerce-Auswertungsumgebung.
author: v-chgri
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: cc6bffba6ee402c6b48d6a3c8f8356eb32b5423b
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478019"
---
# <a name="dynamics-365-commerce-evaluation-environment-overview"></a><span data-ttu-id="59538-103">Dynamics 365 Commerce-Evaluierungsumgebung – Überblick</span><span class="sxs-lookup"><span data-stu-id="59538-103">Dynamics 365 Commerce evaluation environment overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="59538-104">Dieses Thema enthält eine Übersicht der Microsoft Dynamics 365 Commerce-Auswertungsumgebung.</span><span class="sxs-lookup"><span data-stu-id="59538-104">This topic gives an overview of the Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

> [!NOTE]
> <span data-ttu-id="59538-105">Commerce-Auswertungsumgebungen sind nicht allgemein verfügbar und sie werden Partner und Kunden auf Anfrage gewährt.</span><span class="sxs-lookup"><span data-stu-id="59538-105">Commerce evaluation environments aren't generally available, and are granted to partners and customers on a per-request basis.</span></span> <span data-ttu-id="59538-106">Für weitere Informationen wenden Sie sich an den Ansprechpartner Ihres Microsoft-Partners.</span><span class="sxs-lookup"><span data-stu-id="59538-106">For more information, reach out to your Microsoft partner contact.</span></span>

<span data-ttu-id="59538-107">Die Commerce-Auswertungsumgebung ist eine optionale End-to-End-Umgebung von Dynamics 365 Commerce, mit der Partner und potenzielle Kunden das Commerce-Produkt testen können.</span><span class="sxs-lookup"><span data-stu-id="59538-107">The Commerce evaluation environment is an optional end-to-end environment of Dynamics 365 Commerce that lets partners and potential customers try out the Commerce product.</span></span>

<span data-ttu-id="59538-108">Auswertungsumgebungen sind teilweise vorkonfiguriert, um die erforderlichen Schritte nach der Bereitstellung zu reduzieren.</span><span class="sxs-lookup"><span data-stu-id="59538-108">Evaluation environments are partially preconfigured to reduce the required post-provisioning steps.</span></span>

<span data-ttu-id="59538-109">Abgesehen von einigen geringfügigen Einschränkungen, die sich nicht auf Funktionen oder Funktionalität auswirken, bietet die Commerce-Auswertungsumgebung die vollständige Commerce-Erfahrung und kann von Kunden und Implementierungspartnern verwendet werden, um das Produkt auszuwerten, Feedback zu geben und Anpassungs-/Lückenanalysen durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="59538-109">Aside from some minor limitations that don't affect features or functionality, the Commerce evaluation environment provides the complete Commerce experience, and can be used by customers and implementation partners to evaluate the product, provide feedback, and do fit/gap analysis.</span></span>

## <a name="limitations-of-the-commerce-evaluation-environment"></a><span data-ttu-id="59538-110">Einschränkungen der Commerce-Auswertungsumgebung</span><span class="sxs-lookup"><span data-stu-id="59538-110">Limitations of the Commerce evaluation environment</span></span>

<span data-ttu-id="59538-111">Obwohl die Commerce-Auswertungsumgebung alle Commerce-Funktionen und -Funktionalität bietet, gibt es einige geringfügige Einschränkungen:</span><span class="sxs-lookup"><span data-stu-id="59538-111">Although the Commerce evaluation environment provides the full set of Commerce features and functionality, there are some minor limitations:</span></span>

- <span data-ttu-id="59538-112">Obwohl die Commerce-Auswertungsumgebung selbst keine geografischen Einschränkungen aufweist, sollten Komponenten der Umgebung, wie z. B. Retail Cloud Scale Unit (RCSU) und E-Commerce-Anwendungen nur in den USA bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="59538-112">Although the Commerce evaluation environment itself has no geographical limitations, components of the environment, such as the Retail Cloud Scale Unit (RCSU) and e-Commerce applications, should be provisioned only in the United States.</span></span>
- <span data-ttu-id="59538-113">Die Verwendung der Commerce-Auswertungsumgebung ist auf 30 Tage ab dem Datum der Bereitstellung von E-Commerce beschränkt.</span><span class="sxs-lookup"><span data-stu-id="59538-113">Use of the Commerce evaluation environment is limited to 30 days from the date when e-Commerce is provisioned.</span></span>
- <span data-ttu-id="59538-114">Die Commerce-Auswertungsumgebung kann nur in einer Umgebung erfolgreich bereitgestellt und initialisiert werden, die die Demo-Topologie verwendet, in der alle Komponenten einer Umgebung in einer einzelnen virtuellen Maschine (VM), die in der Cloud gehostet wird, bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="59538-114">The Commerce evaluation environment can be successfully deployed and initialized only in an environment that uses the demo topology, where all components of an environment are deployed on a single cloud-hosted virtual machine (VM).</span></span> <span data-ttu-id="59538-115">Die Hauptbeschränkung dieser Topologie ist die Anzahl der gleichzeitigen Benutzer, die die Umgebung unterstützen kann.</span><span class="sxs-lookup"><span data-stu-id="59538-115">The main limitation of this topology is the number of concurrent users that the environment can support.</span></span>

## <a name="get-started"></a><span data-ttu-id="59538-116">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="59538-116">Get started</span></span>

<span data-ttu-id="59538-117">Informationen zum Bereitstellen der Commerce-Auswertungsumgebung finden Sie unter [Bereitstellen einer Commerce-Auswertungsumgebung](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="59538-117">To provision the Commerce evaluation environment, see [Provision a Commerce evaluation environment](provisioning-guide.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="59538-118">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="59538-118">Additional resources</span></span>

[<span data-ttu-id="59538-119">Bereitstellen einer Dynamics 365 Commerce-Auswertungsumgebung</span><span class="sxs-lookup"><span data-stu-id="59538-119">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="59538-120">Konfigurieren einer Dynamics 365 Commerce-Auswertungsumgebung</span><span class="sxs-lookup"><span data-stu-id="59538-120">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="59538-121">BOPIS in einer Dynamics 365 Commerce-Auswertungsumgebung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="59538-121">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="59538-122">Optionale Funktionen für eine Dynamics 365 Commerce-Auswertungsumgebung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="59538-122">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="59538-123">Dynamics 365 Commerce-Auswertungsumgebung – FAQ</span><span class="sxs-lookup"><span data-stu-id="59538-123">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
