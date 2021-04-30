---
title: Überblick Integration Dynamics 365 Commerce und Microsoft Teams
description: Dieses Thema bietet einen Überblick über die Integration von Microsoft Dynamics 365 Commerce und Microsoft Teams.
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: b9289aca4f53eb2ae8f1fa06d5f80b7ee0bbab8e
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908466"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-overview"></a><span data-ttu-id="fe762-103">Überblick Integration Dynamics 365 Commerce und Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="fe762-103">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fe762-104">Dieses Thema bietet einen Überblick über die Integration von Microsoft Dynamics 365 Commerce und Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="fe762-104">This topic presents an overview of Microsoft Dynamics 365 Commerce and Microsoft Teams integration.</span></span>

<span data-ttu-id="fe762-105">Dynamics 365 Commerce wird in Teams integriert, um Debitoren und ihren Mitarbeitern zu helfen, die Produktivität zu verbessern, indem die Aufgabenverwaltung zwischen den beiden Anwendungen synchronisiert wird.</span><span class="sxs-lookup"><span data-stu-id="fe762-105">Dynamics 365 Commerce is integrating with Teams to help customers and their employees improve productivity by synchronizing task management between the two applications.</span></span> <span data-ttu-id="fe762-106">Mit der nahtlosen Aufgabenverwaltung, die durch die Integration von Commerce und Teams bereitgestellt wird, können Filialleiter und Mitarbeiter Aufgabenlisten erstellen, Aufgaben mehreren Filialen zuweisen und den Status von Aufgaben in verschiedenen Shops von beiden Anwendungen aus verfolgen.</span><span class="sxs-lookup"><span data-stu-id="fe762-106">The seamless task management that Commerce and Teams integration provides lets store managers and employees create task lists, assign tasks to multiple stores, and track the status of tasks across stores, from either application.</span></span>

<span data-ttu-id="fe762-107">Die Integration von Commerce und Teams ist ab der Version 10.0.18 von Commerce verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fe762-107">Commerce and Teams integration is available as of the Commerce version 10.0.18 release.</span></span>

## <a name="key-features"></a><span data-ttu-id="fe762-108">Schlüsselfeatures</span><span class="sxs-lookup"><span data-stu-id="fe762-108">Key features</span></span>

<span data-ttu-id="fe762-109">Hier sind einige der wichtigsten Funktionen, welche die Integration von Commerce und Microsoft Teams bietet:</span><span class="sxs-lookup"><span data-stu-id="fe762-109">Here are some of the key features that the Commerce and Microsoft Teams integration provides:</span></span>

- <span data-ttu-id="fe762-110">Die Bereitstellung von Teams durch die Nutzung genau definierter Informationen aus Commerce nutzen, z. B. die Organisationsstruktur und Informationen zu Shops, Mitarbeitern, Berechtigungen und dem geschäftlichen Kontext.</span><span class="sxs-lookup"><span data-stu-id="fe762-110">Provision Teams by taking advantage of well-defined information from Commerce, such as the organizational structure and information about stores, workers, permissions, and business context.</span></span>
- <span data-ttu-id="fe762-111">Synchronisieren Sie problemlos laufende Änderungen (z. B. neu hinzugefügte Filialen oder neu eingestellte Mitarbeiter) zwischen Commerce und Teams, behalten Sie jedoch Commerce als Hauptquelle für Organisationsstrukturdaten bei.</span><span class="sxs-lookup"><span data-stu-id="fe762-111">Easily synchronize ongoing changes (for example, the addition of new stores or hiring of new employees) between Commerce and Teams, but keep Commerce as the master source of organizational structure data.</span></span>
- <span data-ttu-id="fe762-112">Integrieren Sie die Aufgabenverwaltung zwischen Commerce und Teams, um Filialmitarbeitern, Filialleitern, Regionalmanagern und Kommunikationsmanagern bei der Verwaltung von Aufgaben in beiden Anwendungen zu helfen.</span><span class="sxs-lookup"><span data-stu-id="fe762-112">Integrate task management between Commerce and Teams to help store workers, store managers, regional managers, and communications managers handle task management from either application.</span></span>

## <a name="prerequisites-for-using-integration-features"></a><span data-ttu-id="fe762-113">Voraussetzungen für die Verwendung von Integrationsfunktionen</span><span class="sxs-lookup"><span data-stu-id="fe762-113">Prerequisites for using integration features</span></span>

<span data-ttu-id="fe762-114">Die folgenden Voraussetzungen müssen erfüllt sein, bevor Sie mit der Verwendung von Microsoft Teams-Integrationsfunktionen beginnen können:</span><span class="sxs-lookup"><span data-stu-id="fe762-114">The following prerequisites must be in place before you can start to use Microsoft Teams integration features:</span></span>

- <span data-ttu-id="fe762-115">Microsoft 365 Business-Standardlizenz (diese Lizenz enthält Teams)</span><span class="sxs-lookup"><span data-stu-id="fe762-115">Microsoft 365 Business Standard License (This license includes Teams.)</span></span>
- <span data-ttu-id="fe762-116">Azure Active Directory (Azure AD)-Konten für alle Filialleiter und Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="fe762-116">Azure Active Directory (Azure AD) accounts for all store managers and workers</span></span>
- <span data-ttu-id="fe762-117">POS-Systeme (Point of Sale), die mit Azure AD-Authentifizierung konfiguriert sind</span><span class="sxs-lookup"><span data-stu-id="fe762-117">Point of sale (POS) systems that are configured with Azure AD authentication</span></span>

## <a name="conceptual-architecture"></a><span data-ttu-id="fe762-118">Konzeptionelle Architektur</span><span class="sxs-lookup"><span data-stu-id="fe762-118">Conceptual architecture</span></span>

<span data-ttu-id="fe762-119">Die folgende Abbildung zeigt die konzeptionelle Architektur der Integration von Dynamics 365 Commerce und Microsoft Teams am Beispiel eines Shops in San Francisco.</span><span class="sxs-lookup"><span data-stu-id="fe762-119">The following illustration shows the conceptual architecture of Dynamics 365 Commerce and Microsoft Teams integration, using a San Francisco store as an example.</span></span> <span data-ttu-id="fe762-120">Sowohl Teams als auch die Commerce-POS-Anwendung verwenden Microsoft Planner als Repository, sodass von Teams veröffentlichte Aufgaben in der POS-Anwendung angezeigt werden und von Filialleitern in der POS-Anwendung erstellte Ad-hoc-Aufgaben in Teams angezeigt werden, was zu einer nahtlosen Aufgabenverwaltung zwischen den Anwendungen führt.</span><span class="sxs-lookup"><span data-stu-id="fe762-120">Both Teams and the Commerce POS application use Microsoft Planner as a repository so that tasks published from Teams appear in the POS application and ad hoc tasks created by store managers in the POS application appear in Teams, resulting in a seamless task management experience between the applications.</span></span>    

![Architektur der Integration von Commerce und Teams](media/d365-commerce-teams-integration-conceptual-architecture.png)

## <a name="additional-resources"></a><span data-ttu-id="fe762-122">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="fe762-122">Additional resources</span></span>

[<span data-ttu-id="fe762-123">Integration von Dynamics 365 Commerce und Microsoft Teams aktivieren</span><span class="sxs-lookup"><span data-stu-id="fe762-123">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="fe762-124">Microsoft Teams aus Dynamics 365 Commerce bereitstellen</span><span class="sxs-lookup"><span data-stu-id="fe762-124">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="fe762-125">Aufgabenverwaltung zwischen Microsoft Teams und Dynamics 365 Commerce POS synchronisieren</span><span class="sxs-lookup"><span data-stu-id="fe762-125">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="fe762-126">Benutzerrollen in Microsoft Teams verwalten</span><span class="sxs-lookup"><span data-stu-id="fe762-126">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="fe762-127">Shops und Teams zuordnen, wenn in Microsoft Teams bereits Teams vorhanden sind</span><span class="sxs-lookup"><span data-stu-id="fe762-127">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="fe762-128">Integration von Dynamics 365 Commerce und Microsoft Teams – FAQ</span><span class="sxs-lookup"><span data-stu-id="fe762-128">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
