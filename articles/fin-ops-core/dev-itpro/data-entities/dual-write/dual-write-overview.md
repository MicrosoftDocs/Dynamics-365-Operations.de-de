---
title: Datenintegration nahezu in Echtzeit mit Common Data Service
description: Dieser Artikel enthält eine Übersicht über die Integration zwischen Finance and Operations und Common Data Service.
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
ms.openlocfilehash: 1c09b0c0bb695e7695acb7a8821ffb99ae1f6f06
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019802"
---
# <a name="near-real-time-data-integration-with-common-data-service"></a><span data-ttu-id="0ba49-103">Datenintegration nahezu in Echtzeit mit Common Data Service</span><span class="sxs-lookup"><span data-stu-id="0ba49-103">Near-real-time data integration with Common Data Service</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="0ba49-104">In der derzeitigen digitalen Welt verwenden Geschäftsökosysteme die Microsoft Dynamics 365-Anwendungen als Ganzes.</span><span class="sxs-lookup"><span data-stu-id="0ba49-104">In the current digital world, business ecosystems use Microsoft Dynamics 365 applications as a whole.</span></span> <span data-ttu-id="0ba49-105">Da die Daten von Personen, Kunden, Arbeitsgängen und IoT-Geräten (Internet of Things) in eine Quelle fließen, gibt es eine Möglichkeit für digitale Rückmeldungsschleifen.</span><span class="sxs-lookup"><span data-stu-id="0ba49-105">Because data from people, customers, operations, and Internet of Things (IoT) devices flows into one source, there is an opportunity for digital feedback loops.</span></span> <span data-ttu-id="0ba49-106">Um dies zu erreichen, ist die Integration zwischen Finance and Operations-Apps und anderen Dynamics 365-Anwendungen unerlässlich.</span><span class="sxs-lookup"><span data-stu-id="0ba49-106">To achieve this experience, integration between Finance and Operations apps and other Dynamics 365 applications is essential.</span></span> <span data-ttu-id="0ba49-107">Einige Anwendungen basieren auf Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="0ba49-107">Some applications are built on top of Common Data Service.</span></span> <span data-ttu-id="0ba49-108">Integration zwischen Finance and Operations-Apps Daten mit Common Data Service lassen Anwendungen kohärent und flüssig mit Finance and Operations kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="0ba49-108">Integration between Finance and Operations apps data with Common Data Service lets other applications communicate coherently and fluently with Finance and Operations.</span></span>

<span data-ttu-id="0ba49-109">Finance and Operations-Apps und Common Data Service bieten eine Datensynchronisierung zwischen Finance and Operations-Apps and anderen Dynamics 365-Anwendungen über ein Framework für duales Schreiben nahezu in Echtzeit.</span><span class="sxs-lookup"><span data-stu-id="0ba49-109">Finance and Operations apps and Common Data Service provide near-real-time data synchronization between Finance and Operations apps and other Dynamics 365 applications via a dual-write framework.</span></span> <span data-ttu-id="0ba49-110">Die Deckung ist breit und umfasst 28 Oberflächenbereiche der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="0ba49-110">The coverage is broad and spans 28 surface areas of the application.</span></span> <span data-ttu-id="0ba49-111">Die Zielsetzung besteht darin, „eine Dynamics 365“-Benutzererfahrung über nahtlose Datenflüssen bereitzustellen, durch die Unternehmensprozesse über Anwendungen hinweg verbunden werden.</span><span class="sxs-lookup"><span data-stu-id="0ba49-111">The goal is to provide a "One Dynamics 365" user experience through seamless data flows that connect business processes across applications.</span></span>

![Übersicht über die Architektur](media/dual-write-overview.jpg)

<span data-ttu-id="0ba49-113">Die folgenden Wertvorschläge stehen zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="0ba49-113">The following value propositions are available:</span></span>

+ [<span data-ttu-id="0ba49-114">Organisationshierarchie in Common Data Service</span><span class="sxs-lookup"><span data-stu-id="0ba49-114">Organization hierarchy in Common Data Service</span></span>](organization-mapping.md)
+ [<span data-ttu-id="0ba49-115">Unternehmenskonzept in Common Data Service</span><span class="sxs-lookup"><span data-stu-id="0ba49-115">Company concept in Common Data Service</span></span>](company-data.md)
+ [<span data-ttu-id="0ba49-116">Integrierte Masterdaten von Debitoren</span><span class="sxs-lookup"><span data-stu-id="0ba49-116">Integrated customer master</span></span>](customer-mapping.md)
+ [<span data-ttu-id="0ba49-117">Integriertes Sachkonto</span><span class="sxs-lookup"><span data-stu-id="0ba49-117">Integrated ledger</span></span>](ledger-mapping.md)
+ [<span data-ttu-id="0ba49-118">Einheitliche Produktumgebung</span><span class="sxs-lookup"><span data-stu-id="0ba49-118">Unified product experience</span></span>](product-mapping.md)
+ [<span data-ttu-id="0ba49-119">Integrierte Masterdaten von Kreditoren</span><span class="sxs-lookup"><span data-stu-id="0ba49-119">Integrated vendor master</span></span>](vendor-mapping.md)
+ [<span data-ttu-id="0ba49-120">Integrierte Standorte und Lagerorte</span><span class="sxs-lookup"><span data-stu-id="0ba49-120">Integrated sites and warehouses</span></span>](sites-warehouses-mapping.md)
+ [<span data-ttu-id="0ba49-121">Integrierter Steuermaster</span><span class="sxs-lookup"><span data-stu-id="0ba49-121">Integrated tax master</span></span>](tax-mapping.md)

## <a name="system-requirements"></a><span data-ttu-id="0ba49-122">Systemanforderungen</span><span class="sxs-lookup"><span data-stu-id="0ba49-122">System requirements</span></span>

<span data-ttu-id="0ba49-123">Synchrone, bidirektionale Datenflüsse nahezu in Echtzeit erfordern die folgenden Versionen:</span><span class="sxs-lookup"><span data-stu-id="0ba49-123">Synchronous, bidirectional, near-real-time data flows require the following versions:</span></span>

+ <span data-ttu-id="0ba49-124">Microsoft Dynamics 365 for Finance and Operations-Version 10.0.4 (Juli 2019) mit Plattformaktualisierung 28 oder höher</span><span class="sxs-lookup"><span data-stu-id="0ba49-124">Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (July 2019) with Platform update 28, or later</span></span>
+ <span data-ttu-id="0ba49-125">Microsoft Dynamics 365 for Customer Engagement, Plattformversion 9.1 (4.2) oder höher</span><span class="sxs-lookup"><span data-stu-id="0ba49-125">Microsoft Dynamics 365 for Customer Engagement, Platform version 9.1 (4.2) or later</span></span>

## <a name="setup-instructions"></a><span data-ttu-id="0ba49-126">Setupanweisungen</span><span class="sxs-lookup"><span data-stu-id="0ba49-126">Setup instructions</span></span>

<span data-ttu-id="0ba49-127">Folgen Sie diesen Schritten, um die Integration zwischen Finance and Operations-Apps und Common Data Service einzurichten.</span><span class="sxs-lookup"><span data-stu-id="0ba49-127">Follow these steps to set up integration between Finance and Operations apps and Common Data Service.</span></span>
    
1. <span data-ttu-id="0ba49-128">Informationen zur Einrichtung des Systems zum dualen Schreibens finden Sie im [Schritt-für-Schritt-Handbuch](https://aka.ms/dualwrite-docs) zur Ankündigung der Vorschau des dualen Schreibens.</span><span class="sxs-lookup"><span data-stu-id="0ba49-128">For the setup of the dual-write system, see the [step-by-step guide](https://aka.ms/dualwrite-docs) on Announcing Dual Write Preview.</span></span>
2. <span data-ttu-id="0ba49-129">Laden Sie die Lösung aus der Gruppe [Fin Ops und CDS/CE-Integration über Dual-Write](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer herunter.</span><span class="sxs-lookup"><span data-stu-id="0ba49-129">Download and install the solution from the [Fin Ops and CDS/CE Integration via Dual-Write](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer group.</span></span> <span data-ttu-id="0ba49-130">Das Paket beinhaltet fünf Lösungen:</span><span class="sxs-lookup"><span data-stu-id="0ba49-130">The package contains five solutions:</span></span>

    + <span data-ttu-id="0ba49-131">Dynamics365Company</span><span class="sxs-lookup"><span data-stu-id="0ba49-131">Dynamics365Company</span></span>
    + <span data-ttu-id="0ba49-132">CurrencyExchangeRates</span><span class="sxs-lookup"><span data-stu-id="0ba49-132">CurrencyExchangeRates</span></span>
    + <span data-ttu-id="0ba49-133">Dynamics365FinanceAndOperationsCommon</span><span class="sxs-lookup"><span data-stu-id="0ba49-133">Dynamics365FinanceAndOperationsCommon</span></span>
    + <span data-ttu-id="0ba49-134">Dynamics365FinanceCommon</span><span class="sxs-lookup"><span data-stu-id="0ba49-134">Dynamics365FinanceCommon</span></span>
    + <span data-ttu-id="0ba49-135">Dynamics365SupplyChainCommon</span><span class="sxs-lookup"><span data-stu-id="0ba49-135">Dynamics365SupplyChainCommon</span></span>

3. <span data-ttu-id="0ba49-136">Befolgen Sie die Ausführungsreihenfolge für die [Synchronisierung der ersten Referenzdaten](initial-sync.md).</span><span class="sxs-lookup"><span data-stu-id="0ba49-136">Follow the execution order for [synchronizing initial reference data](initial-sync.md).</span></span>
4. <span data-ttu-id="0ba49-137">Wenn Sie Probleme bei der Synchronisierung des dualen Schreibens feststellen, lesen Sie die Informationen im [Handbuch zur Problembehandlung für die Datenintegration](dual-write-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="0ba49-137">If you encounter dual-write synchronization issues, see the [Troubleshooting guide for data integration](dual-write-troubleshooting.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0ba49-138">Duales Schreiben und [Prospect to cash](../../../../supply-chain/sales-marketing/prospect-to-cash.md) können nicht parallel ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="0ba49-138">You can’t run dual-write and [Prospect to cash](../../../../supply-chain/sales-marketing/prospect-to-cash.md) side-by-side.</span></span> <span data-ttu-id="0ba49-139">Wenn Sie die Prospect to cash-Lösung ausführen, müssen Sie sie deinstallieren.</span><span class="sxs-lookup"><span data-stu-id="0ba49-139">If you're running the Prospect to cash solution, you must uninstall it.</span></span> <span data-ttu-id="0ba49-140">Sie müssen auch die Vorlagen des dualen Schreibens für Debitor und Kreditor deaktivieren, die Teil der Prospect to cash-Lösung sind.</span><span class="sxs-lookup"><span data-stu-id="0ba49-140">You must also disable the customer and vendor dual-write templates that are part of the Prospect to cash solution.</span></span>
