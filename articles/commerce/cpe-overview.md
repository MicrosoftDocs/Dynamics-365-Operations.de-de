---
title: Dynamics 365 Commerce-Vorschauumgebung – Übersicht
description: Dieses Thema enthält eine Übersicht der Microsoft Dynamics 365 Commerce-Vorschauumgebung.
author: v-chgri
manager: annbe
ms.date: 12/10/2019
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
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1ff96aeb5963df9ddee56783a089dad129bbb71c
ms.sourcegitcommit: 4ed1d8ad8a0206a4172dbb41cc43f7d95073059c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024682"
---
# <a name="dynamics-365-commerce-preview-environment-overview"></a><span data-ttu-id="d888c-103">Dynamics 365 Commerce-Vorschauumgebung – Übersicht</span><span class="sxs-lookup"><span data-stu-id="d888c-103">Dynamics 365 Commerce preview environment overview</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="d888c-104">Dieses Thema enthält eine Übersicht der Microsoft Dynamics 365 Commerce-Vorschauumgebung.</span><span class="sxs-lookup"><span data-stu-id="d888c-104">This topic gives an overview of the Microsoft Dynamics 365 Commerce preview environment.</span></span>

## <a name="overview"></a><span data-ttu-id="d888c-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="d888c-105">Overview</span></span>

<span data-ttu-id="d888c-106">Die Commerce-Vorschauumgebung ist eine optionale End-to-End-Vorschauumgebung von Dynamics 365 Commerce, mit der potenzielle Debitoren das Commerce-Produkt testen können, bevor es der Öffentlichkeit zugänglich gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="d888c-106">The Commerce preview environment is an optional end-to-end preview environment of Dynamics 365 Commerce that lets potential customers try out the Commerce product before its general release to the public.</span></span>

<span data-ttu-id="d888c-107">Abgesehen von einigen geringfügigen Einschränkungen, die sich nicht auf Features oder Funktionen auswirken, bietet die Commerce-Vorschauumgebung die vollständige Commerce-Erfahrung und kann von Kunden und Implementierungspartnern verwendet werden, um das Produkt zu bewerten, Feedback zu geben und Anpassungs-/Lückenanalysen durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="d888c-107">Aside from some minor limitations that don't affect features or functionality, the Commerce preview environment provides the complete Commerce experience, and can be used by customers and implementation partners to evaluate the product, provide feedback, and do fit/gap analysis.</span></span>

## <a name="limitations-of-the-commerce-preview-environment"></a><span data-ttu-id="d888c-108">Einschränkungen der Commerce-Vorschauumgebung</span><span class="sxs-lookup"><span data-stu-id="d888c-108">Limitations of the Commerce preview environment</span></span>

<span data-ttu-id="d888c-109">Obwohl die Commerce-Vorschauumgebung alle Commerce-Funktionen und -Funktionen bietet, gibt es einige geringfügige Einschränkungen:</span><span class="sxs-lookup"><span data-stu-id="d888c-109">Although the Commerce preview environment provides the full set of Commerce features and functionality, there are some minor limitations:</span></span>

- <span data-ttu-id="d888c-110">Obwohl die Commerce-Vorschauumgebung selbst keine geografischen Einschränkungen aufweist, können Komponenten der Umgebung, wie z. B. Retail Cloud Scale Unit (RCSU) und E-Commerce-Anwendungen nur in den USA bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="d888c-110">Although the Commerce preview environment itself has no geographical limitations, components of the environment, such as the Retail Cloud Scale Unit (RCSU) and e-Commerce applications, can be provisioned only in the United States.</span></span>
- <span data-ttu-id="d888c-111">Die Verwendung der Commerce-Vorschauumgebung ist auf 30 Tage ab dem Datum der Bereitstellung von E-Commerce beschränkt.</span><span class="sxs-lookup"><span data-stu-id="d888c-111">Use of the Commerce preview environment is limited to 30 days from the date when e-Commerce is provisioned.</span></span>
- <span data-ttu-id="d888c-112">Die Commerce-Vorschauumgebung kann nur in einer Umgebung erfolgreich bereitgestellt und initialisiert werden, die die Demo-Topologie verwendet, in der alle Komponenten einer Umgebung in einer einzelnen virtuellen Maschine (VM) bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="d888c-112">The Commerce preview environment can be successfully deployed and initialized only in an environment that uses the demo topology, where all components of an environment are deployed in a single virtual machine (VM).</span></span> <span data-ttu-id="d888c-113">Die Hauptbeschränkung dieser OneBox-VM-Topologie ist die Anzahl der gleichzeitigen Benutzer, die die Vorschauumgebung unterstützen kann.</span><span class="sxs-lookup"><span data-stu-id="d888c-113">The main limitation of this OneBox VM topology is the number of concurrent users that the preview environment can support.</span></span>
- <span data-ttu-id="d888c-114">Die Commerce-Vorschauumgebung kann nur bis zur allgemeinen Verfügbarkeit (GA) des Commerce-Produkts evaluiert werden.</span><span class="sxs-lookup"><span data-stu-id="d888c-114">The Commerce preview environment can be evaluated only until the general availability (GA) of the Commerce product.</span></span> <span data-ttu-id="d888c-115">Neue Demo-Umgebungen werden nach GA verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="d888c-115">New demo environments will be available after GA.</span></span>

## <a name="get-started"></a><span data-ttu-id="d888c-116">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="d888c-116">Get started</span></span>

<span data-ttu-id="d888c-117">Informationen zum Bereitstellen der Commerce-Vorschauumgebung finden Sie unter [Stellen Sie eine Commerce-Vorschauumgebung bereit](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="d888c-117">To provision the Commerce preview environment, see [Provision a Commerce preview environment](provisioning-guide.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d888c-118">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d888c-118">Additional resources</span></span>

[<span data-ttu-id="d888c-119">Bereitstellen einer Dynamics 365 Commerce-Vorschauumgebung</span><span class="sxs-lookup"><span data-stu-id="d888c-119">Provision a Dynamics 365 Commerce preview environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="d888c-120">Konfigurieren einer Dynamics 365 Commerce-Vorschauumgebung</span><span class="sxs-lookup"><span data-stu-id="d888c-120">Configure a Dynamics 365 Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="d888c-121">Konfigurieren optionaler Funktionen für eine Dynamics 365 Commerce-Vorschauumgebung</span><span class="sxs-lookup"><span data-stu-id="d888c-121">Configure optional features for a Dynamics 365 Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="d888c-122">Dynamics 365 Commerce-Vorschauumgebung – FAQ</span><span class="sxs-lookup"><span data-stu-id="d888c-122">Dynamics 365 Commerce preview environment FAQ</span></span>](cpe-faq.md)
