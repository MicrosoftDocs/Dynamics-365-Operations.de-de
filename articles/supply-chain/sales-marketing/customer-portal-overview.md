---
title: Kundenportal für Dynamics 365 Supply Chain Management Überblick
description: In diesem Thema wird das Kundenportal vorgestellt und erläutert, wer es verwenden soll und wie es funktioniert.
author: dasani-madipalli
manager: tfehr
ms.date: 06/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 709ba18be9e2edd5d0a7f143aaed5ef94f365b91
ms.sourcegitcommit: 9a2e9f7dfec47c42178bb67a3e099e610515baf3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/16/2020
ms.locfileid: "3456925"
---
# <a name="customer-portal-for-dynamics-365-supply-chain-management-overview"></a><span data-ttu-id="09d07-103">Kundenportal für Dynamics 365 Supply Chain Management Überblick</span><span class="sxs-lookup"><span data-stu-id="09d07-103">Customer portal for Dynamics 365 Supply Chain Management overview</span></span>

## <a name="what-is-the-customer-portal"></a><span data-ttu-id="09d07-104">Was ist das Kundenportal?</span><span class="sxs-lookup"><span data-stu-id="09d07-104">What is the Customer portal?</span></span>

<span data-ttu-id="09d07-105">Moderne Supply-Chain-Systeme setzen auf Integration.</span><span class="sxs-lookup"><span data-stu-id="09d07-105">Modern supply chain systems rely on integration.</span></span> <span data-ttu-id="09d07-106">Sie erfordern, dass Inventar, Kundennachfrage und Verkaufsabteilungen integriert werden, anstatt sich in separaten Silos zu befinden.</span><span class="sxs-lookup"><span data-stu-id="09d07-106">They require that inventory, customer demand, and sales departments be integrated instead of residing in separate silos.</span></span> <span data-ttu-id="09d07-107">Das Kundenportal hilft Organisationen, die Microsoft Dynamics 365 Supply Chain Management ausführen, diese Integration zu verbessern und die Kunden effektiver auf dem Laufenden zu halten.</span><span class="sxs-lookup"><span data-stu-id="09d07-107">The Customer portal helps organizations that run Microsoft Dynamics 365 Supply Chain Management enhance this integration and more effectively keep their customers informed.</span></span>

<span data-ttu-id="09d07-108">Das Kundenportal ist eine [Power Apps Portale](https://docs.microsoft.com/powerapps/maker/portals/overview) Vorlage, mit der Unternehmen eine extern ausgerichtete B2B-Website (Business-to-Business) für Szenarien erstellen können, die sich auf die Auftragsabwicklung beziehen.</span><span class="sxs-lookup"><span data-stu-id="09d07-108">The Customer portal is a [Power Apps portals](https://docs.microsoft.com/powerapps/maker/portals/overview) template that lets companies create an externally facing business-to-business (B2B) website for scenarios that are related to sales order processing.</span></span> <span data-ttu-id="09d07-109">Die Vorlage verwendet [Duales Schreiben](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page), Supply Chain Management und Power Apps Portale, mit denen externe Unternehmenskunden Daten aus der Dynamics 365-Umgebung des Unternehmens anzeigen und erstellen können.</span><span class="sxs-lookup"><span data-stu-id="09d07-109">The template uses [dual-write](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page), Supply Chain Management, and Power Apps portals to enable external enterprise customers to view and create data from the company's Dynamics 365 environment.</span></span>

<span data-ttu-id="09d07-110">Die Kundenportalvorlage hat Anpassungsfunktionen, über die die Portale von Power Apps verfügen.</span><span class="sxs-lookup"><span data-stu-id="09d07-110">The Customer portal template has all the customization capabilities that the portals feature of Power Apps offers.</span></span> <span data-ttu-id="09d07-111">Die Vorlage kann einfach geändert werden, um die Marke des Unternehmens darzustellen, die Funktionalität zu erweitern und die Benutzererfahrung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="09d07-111">The template can easily be modified to represent the company's brand, add increased functionality, and change the user experience.</span></span> <span data-ttu-id="09d07-112">Alle Funktionen, die die Vorlage sofort bietet, können nach Bedarf geändert werden.</span><span class="sxs-lookup"><span data-stu-id="09d07-112">All the functionality that the template offers out of the box can be modified as desired.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="09d07-113">An sich wird nicht erwartet, dass die Vorlage vollständig funktionsfähig ist.</span><span class="sxs-lookup"><span data-stu-id="09d07-113">By itself, the template isn't expected to be completely functional.</span></span> <span data-ttu-id="09d07-114">Es dient lediglich als Enabler für Kunden, die eine nach außen gerichtete Website erstellen möchten, damit Unternehmenskunden mit Daten aus dem Supply Chain Management interagieren können.</span><span class="sxs-lookup"><span data-stu-id="09d07-114">It just serves as an enabler for customers who want to create an externally facing website so that enterprise customers can engage with data from Supply Chain Management.</span></span>

> [!NOTE]
> <span data-ttu-id="09d07-115">Die Dokumentation zum Kundenportal richtet sich an Administratoren, Anpasser und Systemintegratoren, die das Kundenportal für eine Supply Chain Management-Installation einrichten.</span><span class="sxs-lookup"><span data-stu-id="09d07-115">The Customer portal documentation is directed at admins, customizers, and system integrators who will set up the Customer portal for a Supply Chain Management installation.</span></span> <span data-ttu-id="09d07-116">Es verwendet die Begriffe _Kunde_ und _Benutzer_, um Personen zu beschreiben, die Kunden der Organisation sind, die Supply Chain Management ausführt, und die das endgültige Portal selbst verwenden.</span><span class="sxs-lookup"><span data-stu-id="09d07-116">It uses the terms _customer_ and _user_ to describe people who are customers of the organization that is running Supply Chain Management, and who will use the final portal itself.</span></span>

## <a name="video"></a><span data-ttu-id="09d07-117">-Video</span><span class="sxs-lookup"><span data-stu-id="09d07-117">Video</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4ylwW]

<span data-ttu-id="09d07-118">Das [Übersicht über die Debitorenportalvorlage in Dynamics 365 Supply Chain Management](https://youtu.be/nPrqoLuHfV8) Video (siehe oben) ist enthalten in der [Finance and Operations Wiedergabeliste](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) verfügbar auf YouTube.</span><span class="sxs-lookup"><span data-stu-id="09d07-118">The [Overview of the Customer portal template in Dynamics 365 Supply Chain Management](https://youtu.be/nPrqoLuHfV8) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

## <a name="who-should-use-it"></a><span data-ttu-id="09d07-119">Wer sollte es benutzen?</span><span class="sxs-lookup"><span data-stu-id="09d07-119">Who should use it?</span></span>

<span data-ttu-id="09d07-120">Das Kundenportal richtet sich an Unternehmen, die Supply Chain Management betreiben und folgende Merkmale aufweisen:</span><span class="sxs-lookup"><span data-stu-id="09d07-120">The Customer portal is designed for companies that run Supply Chain Management and have these characteristics:</span></span>

- <span data-ttu-id="09d07-121">Sie möchten eine nach außen gerichtete Website erstellen, die Informationen zur Auftragsabwicklung (z. B. Auftragsstatus oder Kontoinformationen) direkt von ihrem Supply Chain Management-System an ihre Unternehmenskunden übermittelt.</span><span class="sxs-lookup"><span data-stu-id="09d07-121">They want to build an externally facing website that communicates order processing information (such as order status or account information) directly from their Supply Chain Management system to their enterprise customers.</span></span>
- <span data-ttu-id="09d07-122">Sie wechseln von Dynamics AX 2012 zu Supply Chain Management und verwendet zuvor das [AX 2012 Kunden-Self-Service-Portal](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/about-the-customer-self-service-portal).</span><span class="sxs-lookup"><span data-stu-id="09d07-122">They are transitioning from Dynamics AX 2012 to Supply Chain Management and previously used the [AX 2012 Customer self-service portal](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/about-the-customer-self-service-portal).</span></span>

<span data-ttu-id="09d07-123">Die folgenden Arten von Organisationen sind **keine** guten Kandidaten für die Implementierung des Kundenportals:</span><span class="sxs-lookup"><span data-stu-id="09d07-123">The following types of organizations are **not** good candidates for implementing the Customer portal:</span></span>

- <span data-ttu-id="09d07-124">Unternehmen, die eine Website für Nicht-Unternehmenskunden erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="09d07-124">Companies that want to build a website for non-enterprise customers.</span></span> <span data-ttu-id="09d07-125">Diese Unternehmen sollten in Betracht ziehen, eine [Dynamics 365 Commerce E-Commerce-Website](https://docs.microsoft.com/dynamics365/commerce/create-ecommerce-site).</span><span class="sxs-lookup"><span data-stu-id="09d07-125">These companies should consider creating a [Dynamics 365 Commerce e-commerce website](https://docs.microsoft.com/dynamics365/commerce/create-ecommerce-site).</span></span>
- <span data-ttu-id="09d07-126">Unternehmen, die bereits eine bestehende nutzen Power Apps Portale Website für einen ähnlichen Zweck.</span><span class="sxs-lookup"><span data-stu-id="09d07-126">Companies that are already using an existing Power Apps portals website for a similar purpose.</span></span> <span data-ttu-id="09d07-127">Diese Unternehmen erhalten keine zusätzlichen Vorteile aus dem Kundenportal.</span><span class="sxs-lookup"><span data-stu-id="09d07-127">These companies won't receive any additional benefits from the Customer portal.</span></span> <span data-ttu-id="09d07-128">Das Kundenportal wird als Vorlage geliefert, die als Leitfaden und Ausgangspunkt für Kunden dient, die die Punkte zwischen Dualen Schreiben, Supply Chain Management und Power Apps Portal verbinden möchte.</span><span class="sxs-lookup"><span data-stu-id="09d07-128">The Customer portal is delivered as a template that acts as a guide and a starting point for customers who want to "connect the dots" between dual-write, Supply Chain Management, and Power Apps portals.</span></span> <span data-ttu-id="09d07-129">Wenn Sie bereits eine Website eingerichtet haben, die diesem Zweck dient, können Sie durch die Verwendung der Kundenportalvorlage zur erneuten Bereitstellung dieser Website möglicherweise nicht viel Wert gewinnen.</span><span class="sxs-lookup"><span data-stu-id="09d07-129">If you've already set up a website that serves this purpose, you might not gain much value from using the Customer portal template to re-provision that website.</span></span>

## <a name="how-does-it-work"></a><span data-ttu-id="09d07-130">Wie funktioniert das?</span><span class="sxs-lookup"><span data-stu-id="09d07-130">How does it work?</span></span>

<span data-ttu-id="09d07-131">Das Kundenportal wird als Power Apps Portal Vorlage bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="09d07-131">The Customer portal is provided as a Power Apps portals template.</span></span> <span data-ttu-id="09d07-132">Es hängt von dualem Schreiben und Power Apps Portalen ab.</span><span class="sxs-lookup"><span data-stu-id="09d07-132">It depends on Power Apps portals and dual-write.</span></span>

<span data-ttu-id="09d07-133">[Power Apps Portal](https://docs.microsoft.com/powerapps/maker/portals/overview) ist eine Funktion, mit der eine nach außen gerichtete Website erstellen können, bei der sich Personen außerhalb des Unternehmens anmelden können.</span><span class="sxs-lookup"><span data-stu-id="09d07-133">[Power Apps portals](https://docs.microsoft.com/powerapps/maker/portals/overview) is a feature that lets users create an externally facing website that people from outside the organization can sign in to.</span></span> <span data-ttu-id="09d07-134">Für die Erstellung von Portalen ist nur wenig bis gar keine Codierung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="09d07-134">Little to no coding is required to make portals.</span></span> <span data-ttu-id="09d07-135">Das Kundenportal ist eine von vielen [Dynamics 365-Portalvorlagen](https://docs.microsoft.com/powerapps/maker/portals/portal-templates#environment-with-model-driven-apps-in-dynamics-365), die von Microsoft erhältlich sind.</span><span class="sxs-lookup"><span data-stu-id="09d07-135">The Customer portal is one of many [Dynamics 365 portal templates](https://docs.microsoft.com/powerapps/maker/portals/portal-templates#environment-with-model-driven-apps-in-dynamics-365) that are available from Microsoft.</span></span>

<span data-ttu-id="09d07-136">[Duales Schreiben](https://docs.microsoft.com/powerapps/maker/portals/overview) ist eine Out-of-Box-Infrastruktur, die eine nahezu Echtzeit-Interaktion zwischen modellgesteuerten Anwendungen in Dynamics 365 und Finance and Operations Anwendungen ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="09d07-136">[Dual-write](https://docs.microsoft.com/powerapps/maker/portals/overview) is an out-of-box infrastructure product that provides near-real-time interaction between model-driven apps in Dynamics 365 and Finance and Operations apps.</span></span> <span data-ttu-id="09d07-137">Duales Schreiben bietet eine eng gekoppelte, bidirektionale Integration zwischen Finance and Operations Anwendungen und Common Data Service Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="09d07-137">Dual-write provides bidirectional integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="09d07-138">Deshalb bietet dieser automatisierte Datenfluss eine integrierte Benutzererfahrung über die Anwendungen hinweg.</span><span class="sxs-lookup"><span data-stu-id="09d07-138">Therefore, it provides an integrated user experience across the apps.</span></span> <span data-ttu-id="09d07-139">Das Kundenportal hängt von Entitäten ab, die mit dualem Schreiben synchronisiert sind.</span><span class="sxs-lookup"><span data-stu-id="09d07-139">The Customer portal depends on entities that are synced with dual-write.</span></span> <span data-ttu-id="09d07-140">Bevor Daten aus dem Supply Chain Management im Kundenportal angezeigt werden können, muss duales Schreiben für alle entsprechenden Entitäten aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="09d07-140">Before data from Supply Chain Management can be surfaced in the Customer portal, dual-write must be enabled for all the appropriate entities.</span></span>

<span data-ttu-id="09d07-141">![Kundenportalabhängigkeiten](media/customer-portal-elements.png "Kundenportalabhängigkeiten")</span><span class="sxs-lookup"><span data-stu-id="09d07-141">![Customer portal dependencies](media/customer-portal-elements.png "Customer portal dependencies")</span></span>

<span data-ttu-id="09d07-142">Das Kundenportal dient als Ausgangspunkt für Organisationen, die Power Apps Portal zum Erstellen einer nach außen gerichteten Website verwenden möchten, die Daten aus ihrer Supply Chain Management-Installation verwendet.</span><span class="sxs-lookup"><span data-stu-id="09d07-142">The Customer portal acts as a starting point for organizations that want to use Power Apps portals to build an externally facing website that uses data from their Supply Chain Management installation.</span></span> <span data-ttu-id="09d07-143">Es hilft Unternehmen dabei, duales Schreibe, Supply Chain Management und Power Apps Portal zu organisieren.</span><span class="sxs-lookup"><span data-stu-id="09d07-143">It helps organizations connect dual-write, Supply Chain Management, and Power Apps portals.</span></span>