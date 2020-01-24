---
title: Datenintegration nahezu in Echtzeit mit Common Data Service
description: In diesem Thema wird eine Übersicht über die Integration zwischen Finance and Operations und Common Data Service aufgeführt.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
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
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 072564446b74318ffc8e8e6ad4fd16f4421e7854
ms.sourcegitcommit: d0322d1ed6c798301058e44dae76227a0e1f49ac
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "2853905"
---
# <a name="near-real-time-data-integration-with-common-data-service"></a><span data-ttu-id="b88b4-103">Datenintegration nahezu in Echtzeit mit Common Data Service</span><span class="sxs-lookup"><span data-stu-id="b88b4-103">Near-real-time data integration with Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b88b4-104">In der derzeitigen digitalen Welt verwenden Geschäftsökosysteme die Microsoft Dynamics 365-Anwendungen als Ganzes.</span><span class="sxs-lookup"><span data-stu-id="b88b4-104">In the current digital world, business ecosystems use Microsoft Dynamics 365 applications as a whole.</span></span> <span data-ttu-id="b88b4-105">Da die Daten von Personen, Kunden, Arbeitsgängen und IoT-Geräten (Internet of Things) in eine Quelle fließen, gibt es eine Möglichkeit für digitale Rückmeldungsschleifen.</span><span class="sxs-lookup"><span data-stu-id="b88b4-105">Because data from people, customers, operations, and Internet of Things (IoT) devices flows into one source, there is an opportunity for digital feedback loops.</span></span> <span data-ttu-id="b88b4-106">Um dies zu erreichen, ist die Integration zwischen Finance and Operations-Apps und anderen Dynamics 365-Anwendungen unerlässlich.</span><span class="sxs-lookup"><span data-stu-id="b88b4-106">To achieve this experience, integration between Finance and Operations apps and other Dynamics 365 applications is essential.</span></span> <span data-ttu-id="b88b4-107">Einige Anwendungen basieren auf Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="b88b4-107">Some applications are built on top of Common Data Service.</span></span> <span data-ttu-id="b88b4-108">Durch die Integration zwischen Finance and Operations-App-Daten mit Common Data Service können andere Anwendungen kohärent und fließend mit Finance and Operations kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="b88b4-108">Integration between Finance and Operations apps data with Common Data Service lets other applications communicate coherently and fluently with Finance and Operations.</span></span>

<span data-ttu-id="b88b4-109">Finance and Operations-Apps und Common Data Service bieten eine Datensynchronisierung zwischen Finance and Operations-Apps and anderen Dynamics 365-Anwendungen über ein Framework für duales Schreiben nahezu in Echtzeit.</span><span class="sxs-lookup"><span data-stu-id="b88b4-109">Finance and Operations apps and Common Data Service provide near-real-time data synchronization between Finance and Operations apps and other Dynamics 365 applications via a dual-write framework.</span></span> <span data-ttu-id="b88b4-110">Die Deckung ist breit und umfasst 28 Oberflächenbereiche der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="b88b4-110">The coverage is broad and spans 28 surface areas of the application.</span></span> <span data-ttu-id="b88b4-111">Die Zielsetzung besteht darin, „eine Dynamics 365“-Benutzererfahrung über nahtlose Datenflüssen bereitzustellen, durch die Unternehmensprozesse über Anwendungen hinweg verbunden werden.</span><span class="sxs-lookup"><span data-stu-id="b88b4-111">The goal is to provide a "One Dynamics 365" user experience through seamless data flows that connect business processes across applications.</span></span>

![Übersicht über die Architektur](media/dual-write-overview.jpg)

<span data-ttu-id="b88b4-113">Die folgenden Wertvorschläge stehen zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="b88b4-113">The following value propositions are available:</span></span>

+ [<span data-ttu-id="b88b4-114">Organisationshierarchie in Common Data Service</span><span class="sxs-lookup"><span data-stu-id="b88b4-114">Organization hierarchy in Common Data Service</span></span>](dual-write-organization.md)
+ [<span data-ttu-id="b88b4-115">Unternehmenskonzept in Common Data Service</span><span class="sxs-lookup"><span data-stu-id="b88b4-115">Company concept in Common Data Service</span></span>](dual-write-company.md)
+ [<span data-ttu-id="b88b4-116">Integrierte Masterdaten von Debitoren</span><span class="sxs-lookup"><span data-stu-id="b88b4-116">Integrated customer master</span></span>](dual-write-customer.md)
+ [<span data-ttu-id="b88b4-117">Integriertes Sachkonto</span><span class="sxs-lookup"><span data-stu-id="b88b4-117">Integrated ledger</span></span>](dual-write-ledger.md)
+ [<span data-ttu-id="b88b4-118">Einheitliche Produktumgebung</span><span class="sxs-lookup"><span data-stu-id="b88b4-118">Unified product experience</span></span>](dual-write-product.md)
+ [<span data-ttu-id="b88b4-119">Integrierte Masterdaten von Kreditoren</span><span class="sxs-lookup"><span data-stu-id="b88b4-119">Integrated vendor master</span></span>](dual-write-vendor.md)
+ [<span data-ttu-id="b88b4-120">Integrierte Standorte und Lagerorte</span><span class="sxs-lookup"><span data-stu-id="b88b4-120">Integrated sites and warehouses</span></span>](dual-write-sites-and-warehouses.md)
+ [<span data-ttu-id="b88b4-121">Integrierter Steuermaster</span><span class="sxs-lookup"><span data-stu-id="b88b4-121">Integrated tax master</span></span>](dual-write-tax.md)

## <a name="system-requirements"></a><span data-ttu-id="b88b4-122">Systemanforderungen</span><span class="sxs-lookup"><span data-stu-id="b88b4-122">System requirements</span></span>

<span data-ttu-id="b88b4-123">Synchrone, bidirektionale Datenflüsse nahezu in Echtzeit erfordern die folgenden Versionen:</span><span class="sxs-lookup"><span data-stu-id="b88b4-123">Synchronous, bidirectional, near-real-time data flows require the following versions:</span></span>

+ <span data-ttu-id="b88b4-124">Microsoft Dynamics 365 for Finance and Operations-Version 10.0.4 (Juli 2019) mit Plattformaktualisierung 28 oder höher</span><span class="sxs-lookup"><span data-stu-id="b88b4-124">Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (July 2019) with Platform update 28, or later</span></span>
+ <span data-ttu-id="b88b4-125">Microsoft Dynamics 365 for Customer Engagement, Plattformversion 9.1 (4.2) oder höher</span><span class="sxs-lookup"><span data-stu-id="b88b4-125">Microsoft Dynamics 365 for Customer Engagement, Platform version 9.1 (4.2) or later</span></span>

## <a name="setup-instructions"></a><span data-ttu-id="b88b4-126">Setupanweisungen</span><span class="sxs-lookup"><span data-stu-id="b88b4-126">Setup instructions</span></span>

<span data-ttu-id="b88b4-127">Führen Sie die folgenden Schritte aus, um die Integration zwischen Finance and Operations-Apps und Common Data Service einzurichten.</span><span class="sxs-lookup"><span data-stu-id="b88b4-127">Follow these steps to set up integration between Finance and Operations apps and Common Data Service.</span></span>
    
1. <span data-ttu-id="b88b4-128">Informationen zur Einrichtung des Systems zum dualen Schreibens finden Sie im [Schritt-für-Schritt-Handbuch](https://aka.ms/dualwrite-docs) zur Ankündigung der Vorschau des dualen Schreibens.</span><span class="sxs-lookup"><span data-stu-id="b88b4-128">For the setup of the dual-write system, see the [step-by-step guide](https://aka.ms/dualwrite-docs) on Announcing Dual Write Preview.</span></span>
2. <span data-ttu-id="b88b4-129">Laden Sie die Lösung aus der Gruppe [Fin Ops und CDS/CE-Integration über Dual-Write](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer herunter.</span><span class="sxs-lookup"><span data-stu-id="b88b4-129">Download and install the solution from the [Fin Ops and CDS/CE Integration via Dual-Write](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer group.</span></span> <span data-ttu-id="b88b4-130">Das Paket beinhaltet fünf Lösungen:</span><span class="sxs-lookup"><span data-stu-id="b88b4-130">The package contains five solutions:</span></span>

    + <span data-ttu-id="b88b4-131">Dynamics365Company</span><span class="sxs-lookup"><span data-stu-id="b88b4-131">Dynamics365Company</span></span>
    + <span data-ttu-id="b88b4-132">CurrencyExchangeRates</span><span class="sxs-lookup"><span data-stu-id="b88b4-132">CurrencyExchangeRates</span></span>
    + <span data-ttu-id="b88b4-133">Dynamics365FinanceAndOperationsCommon</span><span class="sxs-lookup"><span data-stu-id="b88b4-133">Dynamics365FinanceAndOperationsCommon</span></span>
    + <span data-ttu-id="b88b4-134">Dynamics365FinanceCommon</span><span class="sxs-lookup"><span data-stu-id="b88b4-134">Dynamics365FinanceCommon</span></span>
    + <span data-ttu-id="b88b4-135">Dynamics365SupplyChainCommon</span><span class="sxs-lookup"><span data-stu-id="b88b4-135">Dynamics365SupplyChainCommon</span></span>

3. <span data-ttu-id="b88b4-136">Befolgen Sie die Ausführungsreihenfolge für die [Synchronisierung der ersten Referenzdaten](dual-write-initial.md).</span><span class="sxs-lookup"><span data-stu-id="b88b4-136">Follow the execution order for [synchronizing initial reference data](dual-write-initial.md).</span></span>
4. <span data-ttu-id="b88b4-137">Wenn Sie Probleme bei der Synchronisierung des dualen Schreibens feststellen, lesen Sie die Informationen im [Handbuch zur Problembehandlung für die Datenintegration](dual-write-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="b88b4-137">If you encounter dual-write synchronization issues, see the [Troubleshooting guide for data integration](dual-write-troubleshooting.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b88b4-138">Duales Schreiben und [Prospect to cash](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) können nicht parallel ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b88b4-138">You can’t run dual-write and [Prospect to cash](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) side-by-side.</span></span> <span data-ttu-id="b88b4-139">Wenn Sie die Prospect to cash-Lösung ausführen, müssen Sie sie deinstallieren.</span><span class="sxs-lookup"><span data-stu-id="b88b4-139">If you're running the Prospect to cash solution, you must uninstall it.</span></span> <span data-ttu-id="b88b4-140">Sie müssen auch die Vorlagen des dualen Schreibens für Debitor und Kreditor deaktivieren, die Teil der Prospect to cash-Lösung sind.</span><span class="sxs-lookup"><span data-stu-id="b88b4-140">You must also disable the customer and vendor dual-write templates that are part of the Prospect to cash solution.</span></span>
