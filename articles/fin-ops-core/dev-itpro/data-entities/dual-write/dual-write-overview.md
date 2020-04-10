---
title: Überblick über die Dual-Write-Funktion
description: Dieses Thema bietet einen Überblick über Dual-Write. Dual-Write ist eine Infrastruktur, die eine Interaktion zwischen Microsoft Dynamics 365 modellgesteuerten Anwendungen und Finance and Operations Anwendungen nahezu in Echtzeit ermöglicht.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 64626ebdd7fbad3d47a4b4c6bbc45bf3bc0c8277
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172783"
---
# <a name="dual-write-overview"></a><span data-ttu-id="5d26e-104">Dual-Write-Übersicht</span><span class="sxs-lookup"><span data-stu-id="5d26e-104">Dual-write overview</span></span>

[!include [banner](../../includes/banner.md)]



## <a name="what-is-dual-write"></a><span data-ttu-id="5d26e-105">Was ist Dual-Write?</span><span class="sxs-lookup"><span data-stu-id="5d26e-105">What is dual-write?</span></span>

<span data-ttu-id="5d26e-106">Dual-Write ist eine Out-of-Box-Infrastruktur, die eine nahezu Echtzeit-Interaktion zwischen modellgesteuerten Anwendungen in Microsoft Dynamics 365 und Finance and Operations Anwendungen ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="5d26e-106">Dual-write is an out-of-box infrastructure that provides near-real-time interaction between model-driven apps in Microsoft Dynamics 365 and Finance and Operations apps.</span></span> <span data-ttu-id="5d26e-107">Wenn Daten über Kunden, Produkte, Personen und Abläufe über Anwendungsgrenzen hinweg fließen, werden alle Abteilungen eines Unternehmens in die Lage versetzt, diese Daten zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="5d26e-107">When data about customers, products, people, and operations flows beyond application boundaries, all departments in an organization are empowered.</span></span>

<span data-ttu-id="5d26e-108">Dual-Write bietet eine eng gekoppelte, bidirektionale Integration zwischen Finance and Operations Anwendungen und Common Data Service Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="5d26e-108">Dual-write provides tightly coupled, bidirectional integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="5d26e-109">Jede Datenänderung in Finance and Operations Anwendungen führt zu Schreibvorgängen in Common Data Service, und jede Datenänderung in Common Data Service führt zu Schreibvorgängen in Finance and Operations Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="5d26e-109">Any data change in Finance and Operations apps causes writes to Common Data Service, and any data change in Common Data Service causes writes to Finance and Operations apps.</span></span> <span data-ttu-id="5d26e-110">Dieser automatisierte Datenfluss bietet eine integrierte Benutzererfahrung über die Anwendungen hinweg.</span><span class="sxs-lookup"><span data-stu-id="5d26e-110">This automated data flow provides an integrated user experience across the apps.</span></span>

![Datenbeziehung zwischen Anwendungen](media/dual-write-overview.jpg)

<span data-ttu-id="5d26e-112">Dual-Write hat zwei Aspekte: einen *Infrastruktur* Aspekt und einen *Anwendung* Aspekt.</span><span class="sxs-lookup"><span data-stu-id="5d26e-112">Dual-write has two aspects: an *infrastructure* aspect and an *application* aspect.</span></span>

### <a name="infrastructure"></a><span data-ttu-id="5d26e-113">Infrastruktur</span><span class="sxs-lookup"><span data-stu-id="5d26e-113">Infrastructure</span></span>

<span data-ttu-id="5d26e-114">Die Dual-Write-Infrastruktur ist erweiterbar und zuverlässig und umfasst die folgenden Hauptmerkmale:</span><span class="sxs-lookup"><span data-stu-id="5d26e-114">The dual-write infrastructure is extensible and reliable, and includes the following key features:</span></span>

+ <span data-ttu-id="5d26e-115">Synchroner und bidirektionaler Datenfluss zwischen Anwendungen</span><span class="sxs-lookup"><span data-stu-id="5d26e-115">Synchronous and bidirectional data flow between applications</span></span>
+ <span data-ttu-id="5d26e-116">Synchronisierung zusammen mit Spiel-, Pausen- und Aufholmodi zur Unterstützung des Systems im Online- und Offline-/Asynchronmodus.</span><span class="sxs-lookup"><span data-stu-id="5d26e-116">Synchronization, together with play, pause, and catchup modes to support the system during online and offline/asynchronous modes.</span></span>
+ <span data-ttu-id="5d26e-117">Fähigkeit zur Synchronisierung der Anfangsdaten zwischen den Anwendungen</span><span class="sxs-lookup"><span data-stu-id="5d26e-117">Ability to sync initial data between the applications</span></span>
+ <span data-ttu-id="5d26e-118">Konsolidierte Ansicht der Aktivitäts- und Fehlerprotokolle für Datenadministratoren</span><span class="sxs-lookup"><span data-stu-id="5d26e-118">Consolidated view of activity and error logs for data admins</span></span>
+ <span data-ttu-id="5d26e-119">Möglichkeit, benutzerdefinierte Benachrichtigungen und Schwellenwerte zu konfigurieren und Benachrichtigungen zu abonnieren</span><span class="sxs-lookup"><span data-stu-id="5d26e-119">Ability to configure custom alerts and thresholds, and to subscribe to notifications</span></span>
+ <span data-ttu-id="5d26e-120">Intuitive Benutzeroberfläche (UI) für Filterung und Transformationen</span><span class="sxs-lookup"><span data-stu-id="5d26e-120">Intuitive user interface (UI) for filtering and transformations</span></span>
+ <span data-ttu-id="5d26e-121">Fähigkeit, Abhängigkeiten und Beziehungen zwischen den Entitäten festzulegen und anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="5d26e-121">Ability to set and view entity dependencies and relationships</span></span>
+ <span data-ttu-id="5d26e-122">Erweiterbarkeit sowohl für Standard- als auch für benutzerdefinierte Entitäten und Karten</span><span class="sxs-lookup"><span data-stu-id="5d26e-122">Extensibility for both standard and custom entities and maps</span></span>
+ <span data-ttu-id="5d26e-123">Zuverlässige Verwaltung des Lebenszyklus von Anwendungen</span><span class="sxs-lookup"><span data-stu-id="5d26e-123">Reliable application lifecycle management</span></span>
+ <span data-ttu-id="5d26e-124">Out-of-Box-Einrichtungserfahrung für neue Kunden</span><span class="sxs-lookup"><span data-stu-id="5d26e-124">Out-of-box setup experience for new customers</span></span>

### <a name="application"></a><span data-ttu-id="5d26e-125">Bewerbung</span><span class="sxs-lookup"><span data-stu-id="5d26e-125">Application</span></span>

<span data-ttu-id="5d26e-126">Dual-Write erstellt eine Zuordnung zwischen Konzepten in Finance and Operations-Apps und Konzepten in modellgesteuerten Anwendungen in Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="5d26e-126">Dual-write creates a mapping between concepts in Finance and Operations apps and concepts in model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="5d26e-127">Diese Integration unterstützt die folgenden Szenarien:</span><span class="sxs-lookup"><span data-stu-id="5d26e-127">This integration supports the following scenarios:</span></span>

+ <span data-ttu-id="5d26e-128">Integrierte Masterdaten von Debitoren</span><span class="sxs-lookup"><span data-stu-id="5d26e-128">Integrated customer master</span></span>
+ <span data-ttu-id="5d26e-129">Zugang zu Kundenkarten und Belohnungspunkten</span><span class="sxs-lookup"><span data-stu-id="5d26e-129">Access to customer loyalty cards and reward points</span></span>
+ <span data-ttu-id="5d26e-130">Einheitliche Produktbeherrschung</span><span class="sxs-lookup"><span data-stu-id="5d26e-130">Unified product mastering experience</span></span>
+ <span data-ttu-id="5d26e-131">Bewusstsein für die Organisationshierarchie</span><span class="sxs-lookup"><span data-stu-id="5d26e-131">Awareness of organization hierarchy</span></span>
+ <span data-ttu-id="5d26e-132">Integrierte Masterdaten von Kreditoren</span><span class="sxs-lookup"><span data-stu-id="5d26e-132">Integrated vendor master</span></span>
+ <span data-ttu-id="5d26e-133">Zugang zu Finanz- und Steuerdaten</span><span class="sxs-lookup"><span data-stu-id="5d26e-133">Access to finance and tax reference data</span></span>
+ <span data-ttu-id="5d26e-134">Erfahrung mit Bedarfspreismodulen</span><span class="sxs-lookup"><span data-stu-id="5d26e-134">On-demand price engine experience</span></span>
+ <span data-ttu-id="5d26e-135">Integrierte Prospect-to-Cash-Erfahrung</span><span class="sxs-lookup"><span data-stu-id="5d26e-135">Integrated prospect-to-cash experience</span></span>
+ <span data-ttu-id="5d26e-136">Fähigkeit, sowohl interne Anlagen als auch Kundenanlagen durch Außendienstmitarbeiter zu bedienen</span><span class="sxs-lookup"><span data-stu-id="5d26e-136">Ability to serve both in-house assets and customer assets through field agents</span></span>
+ <span data-ttu-id="5d26e-137">Integrierte Procure-to-Pay-Erfahrung</span><span class="sxs-lookup"><span data-stu-id="5d26e-137">Integrated procure-to-pay experience</span></span>
+ <span data-ttu-id="5d26e-138">Integrierte Aktivitäten und Notizen für Kundendaten und Dokumente</span><span class="sxs-lookup"><span data-stu-id="5d26e-138">Integrated activities and notes for customer data and documents</span></span>
+ <span data-ttu-id="5d26e-139">Fähigkeit, die Verfügbarkeit und die Details der Bestände aus dem Lagerbestand nachzuschlagen</span><span class="sxs-lookup"><span data-stu-id="5d26e-139">Ability to look up on-hand inventory availability and details</span></span>
+ <span data-ttu-id="5d26e-140">Projekt-zu-Bargeld-Erfahrung</span><span class="sxs-lookup"><span data-stu-id="5d26e-140">Project-to-cash experience</span></span>
+ <span data-ttu-id="5d26e-141">Fähigkeit zur Handhabung mehrerer Adressen und Rollen durch das Parteikonzept</span><span class="sxs-lookup"><span data-stu-id="5d26e-141">Ability to handle multiple addresses and roles through the party concept</span></span>
+ <span data-ttu-id="5d26e-142">Verwaltung einer einzigen Quelle für Benutzer</span><span class="sxs-lookup"><span data-stu-id="5d26e-142">Single source management for users</span></span>
+ <span data-ttu-id="5d26e-143">Integrierte Kanäle für Retail und Marketing</span><span class="sxs-lookup"><span data-stu-id="5d26e-143">Integrated channels for retailing and marketing</span></span>
+ <span data-ttu-id="5d26e-144">Sichtbarkeit von Werbeaktionen und Rabatten</span><span class="sxs-lookup"><span data-stu-id="5d26e-144">Visibility into promotions and discounts</span></span>
+ <span data-ttu-id="5d26e-145">Anfrage für Service-Funktionen</span><span class="sxs-lookup"><span data-stu-id="5d26e-145">Request-for-service functions</span></span>
+ <span data-ttu-id="5d26e-146">Rationalisierte Serviceabläufe</span><span class="sxs-lookup"><span data-stu-id="5d26e-146">Streamlined service operations</span></span>

## <a name="top-reasons-to-use-dual-write"></a><span data-ttu-id="5d26e-147">Die wichtigsten Gründe für die Verwendung von Dual-Write</span><span class="sxs-lookup"><span data-stu-id="5d26e-147">Top reasons to use dual-write</span></span>

<span data-ttu-id="5d26e-148">Dual-Write bietet Datenintegration über Microsoft Dynamics 365 Apps hinweg.</span><span class="sxs-lookup"><span data-stu-id="5d26e-148">Dual-write provides data integration across Microsoft Dynamics 365 applications.</span></span> <span data-ttu-id="5d26e-149">Dieser robuste Rahmen verbindet Umgebungen und ermöglicht die Zusammenarbeit verschiedener Geschäftsanwendungen.</span><span class="sxs-lookup"><span data-stu-id="5d26e-149">This robust framework links environments and enables different business applications to work together.</span></span> <span data-ttu-id="5d26e-150">Hier sind die wichtigsten Gründe, warum Sie Dual-Write verwenden sollten:</span><span class="sxs-lookup"><span data-stu-id="5d26e-150">Here are the top reasons why you should use dual-write:</span></span>

+ <span data-ttu-id="5d26e-151">Dual-Write bietet eine eng gekoppelte, echtzeitnahe und bidirektionale Integration zwischen Finance and Operations-Anwendungen und modellgesteuerten Anwendungen in Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="5d26e-151">Dual-write provides tightly coupled, near-real-time, and bidirectional integration between Finance and Operations apps and model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="5d26e-152">Diese Integration macht Microsoft Dynamics 365 zum One-Stop-Shop für alle Ihre Geschäftslösungen.</span><span class="sxs-lookup"><span data-stu-id="5d26e-152">This integration makes Microsoft Dynamics 365 the one-stop shop for all your business solutions.</span></span> <span data-ttu-id="5d26e-153">Kunden, die Dynamics 365 Finance und Dynamics 365 Supply Chain Management verwenden, aber für das Kundenbeziehungsmanagement (CRM) Nicht-Microsoft-Lösungen einsetzen, entscheiden sich für Dynamics 365 wegen der Unterstützung von Dual-Write.</span><span class="sxs-lookup"><span data-stu-id="5d26e-153">Customers who use Dynamics 365 Finance and Dynamics 365 Supply Chain Management, but who use non-Microsoft solutions for customer relationship management (CRM), are moving toward Dynamics 365 for its dual-write support.</span></span>
+ <span data-ttu-id="5d26e-154">Daten von Kunden, Produkten, Operationen, Projekten und dem Internet der Dinge (Internet of Things, IoT) fließen automatisch durch Dual-Write zu Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="5d26e-154">Data from customers, products, operations, projects, and the Internet of Things (IoT) automatically flows to Common Data Service through dual-write.</span></span> <span data-ttu-id="5d26e-155">Diese Verbindung ist sehr nützlich für Unternehmen, die an Microsoft Power Platform-Erweiterungen interessiert sind.</span><span class="sxs-lookup"><span data-stu-id="5d26e-155">This connection is very useful for businesses that are interested in Microsoft Power Platform expansions.</span></span>
+ <span data-ttu-id="5d26e-156">Die Dual-Write-Infrastruktur folgt dem No-Code/Low-Code-Prinzip.</span><span class="sxs-lookup"><span data-stu-id="5d26e-156">The dual-write infrastructure follows the no-code/low-code principle.</span></span> <span data-ttu-id="5d26e-157">Es ist nur ein minimaler technischer Aufwand erforderlich, um die Standard-Tabelle-zu-Tabelle-Zuordnungen zu erweitern und um benutzerdefinierte Zuordnungen aufzunehmen.</span><span class="sxs-lookup"><span data-stu-id="5d26e-157">Minimal engineering effort is required to extend the standard table-to-table maps and to include custom maps.</span></span>
+ <span data-ttu-id="5d26e-158">Dual-Write unterstützt sowohl den Online- als auch den Offline-Modus.</span><span class="sxs-lookup"><span data-stu-id="5d26e-158">Dual-write supports both online mode and offline mode.</span></span> <span data-ttu-id="5d26e-159">Microsoft ist das einzige Unternehmen, das Unterstützung für den Online- und Offline-Modus bietet.</span><span class="sxs-lookup"><span data-stu-id="5d26e-159">Microsoft is the only company that offers support for online and offline modes.</span></span>

## <a name="what-does-dual-write-mean-for-users-and-architects-of-crm-products"></a><span data-ttu-id="5d26e-160">Was bedeutet Dual-Write für Benutzer und Architekten von CRM-Produkten?</span><span class="sxs-lookup"><span data-stu-id="5d26e-160">What does dual-write mean for users and architects of CRM products?</span></span>

<span data-ttu-id="5d26e-161">Dual-Write automatisiert den Datenfluss zwischen Finance and Operations Anwendungen und Common Data Service Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="5d26e-161">Dual-write automates the data flow between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="5d26e-162">In zukünftigen Versionen werden Konzepte in modellgesteuerten Anwendungen in Dynamics 365 (z.B. Kunde, Kontakt, Angebot und Bestellung) auf Kunden des mittleren und oberen Mittelstands skaliert.</span><span class="sxs-lookup"><span data-stu-id="5d26e-162">In future releases, concepts in model-driven apps in Dynamics 365 (for example, customer, contact, quotation, and order) will be scaled to mid-market and upper-mid-market customers.</span></span>

<span data-ttu-id="5d26e-163">In der ersten Version wird der größte Teil der Automatisierung durch Dual-Write-Lösungen abgewickelt.</span><span class="sxs-lookup"><span data-stu-id="5d26e-163">In the first release, most of the automation is handled by dual-write solutions.</span></span> <span data-ttu-id="5d26e-164">In zukünftigen Versionen werden diese Lösungen Teil von Common Data Service werden.</span><span class="sxs-lookup"><span data-stu-id="5d26e-164">In future releases, those solutions will become part of Common Data Service.</span></span> <span data-ttu-id="5d26e-165">Wenn Sie die bevorstehenden Änderungen an Common Data Service verstehen, können Sie sich langfristig Aufwand sparen.</span><span class="sxs-lookup"><span data-stu-id="5d26e-165">By understanding the upcoming changes to Common Data Service, you can save yourself effort in the long term.</span></span> <span data-ttu-id="5d26e-166">Hier sind einige der entscheidenden Änderungen:</span><span class="sxs-lookup"><span data-stu-id="5d26e-166">Here are some of the crucial changes:</span></span>

+ <span data-ttu-id="5d26e-167">Common Data Service wird neue Konzepte haben, wie z.B. Firma und Partei.</span><span class="sxs-lookup"><span data-stu-id="5d26e-167">Common Data Service will have new concepts, such as company and party.</span></span> <span data-ttu-id="5d26e-168">Diese Konzepte werden alle Anwendungen betreffen, die auf Common Data Service aufbauen, wie z.B. Dynamics 365 Marketing, Dynamics 365 Sales, Dynamics 365 Customer Service und Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="5d26e-168">These concepts will affect all apps that are built on Common Data Service, such as Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service, and Dynamics 365 Field Service.</span></span>
+ <span data-ttu-id="5d26e-169">Aktivitäten und Notizen werden vereinheitlicht und erweitert, um sowohl die C1 (Benutzer des Systems) als auch die C2 (Kunden des Systems) zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="5d26e-169">Activities and notes are unified and expanded to support both C1s (users of the system) and C2s (customers of the system).</span></span>
+ <span data-ttu-id="5d26e-170">Hier sind einige der bevorstehenden Änderungen in Common Data Service:</span><span class="sxs-lookup"><span data-stu-id="5d26e-170">Here are some of the upcoming changes in Common Data Service:</span></span>

    - <span data-ttu-id="5d26e-171">Der dezimale Datentyp wird den Gelddatentyp ersetzen.</span><span class="sxs-lookup"><span data-stu-id="5d26e-171">The decimal data type will replace the money data type.</span></span>
    - <span data-ttu-id="5d26e-172">Die Datumsgültigkeit wird vergangene, gegenwärtige und zukünftige Daten an der gleichen Stelle unterstützen.</span><span class="sxs-lookup"><span data-stu-id="5d26e-172">Date effectivity will support past, present, and future data in the same place.</span></span>
    - <span data-ttu-id="5d26e-173">Es wird mehr Unterstützung für Währung und Wechselkurse geben, und die **Wechselkurs** Programmierschnittstelle (API) wird überarbeitet.</span><span class="sxs-lookup"><span data-stu-id="5d26e-173">There will be more support for currency and exchange rates, and the **Exchange Rate** application programming interface (API) will be revised.</span></span>
    - <span data-ttu-id="5d26e-174">Einheitenumrechnungen werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5d26e-174">Unit conversions will be supported.</span></span>

<span data-ttu-id="5d26e-175">Weitere Informationen über bevorstehende Änderungen finden Sie unter [Daten in Common Data Service - Phase 1 unf 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/finance-operations-crossapp-capabilities/data-common-data-service-phase-1).</span><span class="sxs-lookup"><span data-stu-id="5d26e-175">For more information about upcoming changes, see [Data in Common Data Service – phase 1 & 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/finance-operations-crossapp-capabilities/data-common-data-service-phase-1).</span></span>
