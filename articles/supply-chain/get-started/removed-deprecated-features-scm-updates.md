---
title: Entfernte oder veraltete Funktionen in Dynamics 365 Supply Chain Management
description: In diesem Thema werden die Funktionen beschrieben, die entfernt wurden oder entfernt werden sollen in Dynamics 365 Supply Chain Management.
author: kamaybac
manager: AnnBe
ms.date: 04/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 7502cd16129431d41d152508fb3b49ff85a5a9f8
ms.sourcegitcommit: f1db998ecfccca660eb15cc2739b12c8463fa54d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2020
ms.locfileid: "3331247"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a><span data-ttu-id="5ea0d-103">Entfernte oder veraltete Funktionen in Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="5ea0d-103">Removed or deprecated features in Dynamics 365 Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5ea0d-104">Dieses Thema wird aktualisiert, sobald neue entfernte oder veraltete Funktionen dokumentiert werden Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5ea0d-104">This topic will be updated as new removed or deprecated features are documented for Dynamics 365 Supply Chain Management.</span></span>

- <span data-ttu-id="5ea0d-105">Eine Funktion *entfernt* ist nicht mehr im Produkt verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5ea0d-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="5ea0d-106">Eine Funktion *veraltet* wird nicht aktiv entwickelt und könnte bei einem zukünftigen Update entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="5ea0d-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="5ea0d-107">Diese Liste soll ihnen dabei helfen, diese entfernten und veralteten Funktionen bei Ihrer eigenen Planung zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="5ea0d-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span>

> [!NOTE]
> <span data-ttu-id="5ea0d-108">Detaillierte Informationen über Objekte in Finance and Operations Apps finden Sie in den [Technischen Referenzberichten](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span><span class="sxs-lookup"><span data-stu-id="5ea0d-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="5ea0d-109">Sie können die verschiedenen Versionen dieser Berichte vergleichen, um sich über Objekte zu informieren, die sich in jeder Version von Finance and Operations-Anwendungen geändert haben oder entfernt wurden.</span><span class="sxs-lookup"><span data-stu-id="5ea0d-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10011-release"></a><span data-ttu-id="5ea0d-110">Entfernte oder veraltete Funktionen in Supply Chain Management 10.0.11</span><span class="sxs-lookup"><span data-stu-id="5ea0d-110">Features removed or deprecated in the Supply Chain Management 10.0.11 release</span></span>

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios"></a><span data-ttu-id="5ea0d-111">Verwenden des integrierten Supply Chain Management-Masterplanungsmoduls für Verteilungszenarien</span><span class="sxs-lookup"><span data-stu-id="5ea0d-111">Use of built-in Supply Chain Management master planning engine for distribution scenarios</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="5ea0d-112">**Grund für veralteten Zustand/Entfernung**</span><span class="sxs-lookup"><span data-stu-id="5ea0d-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="5ea0d-113">Um die Leistung zu verbessern und die SQL-Datenbanklast während der Ausführung der Masterplanung zu minimieren, wird das integrierte Supply Chain Management-Masterplanungsmodul durch die Planungsoptimierung ersetzt.</span><span class="sxs-lookup"><span data-stu-id="5ea0d-113">To enhance performance and minimize the SQL database load during master planning runs, the built-in Supply Chain Management master planning engine is being replaced by Planning Optimization.</span></span> <span data-ttu-id="5ea0d-114">Die Planungsoptimierung ermöglicht schnelle Planungsausführungen, die auch während der Geschäftszeiten durchgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="5ea0d-114">Planning Optimization allows for fast planning runs that can be performed even during office hours.</span></span> <span data-ttu-id="5ea0d-115">Dadurch können Planer sofort auf Änderungen in der Nachfrage oder bei den Planungsparametern reagieren.</span><span class="sxs-lookup"><span data-stu-id="5ea0d-115">This enables planners to react immediately to changes in demand or planning parameters.</span></span> |
| <span data-ttu-id="5ea0d-116">**Ersetzt durch eine andere Funktion?**</span><span class="sxs-lookup"><span data-stu-id="5ea0d-116">**Replaced by another feature?**</span></span>   | <span data-ttu-id="5ea0d-117">Ja, die Planungsoptimierung wird das bestehende integrierte Supply Chain Management-Masterplanungsmodul ersetzen.</span><span class="sxs-lookup"><span data-stu-id="5ea0d-117">Yes, Planning Optimization will replace the existing built-in Supply Chain Management master planning engine.</span></span> |
| <span data-ttu-id="5ea0d-118">**Betroffene Produktbereiche**</span><span class="sxs-lookup"><span data-stu-id="5ea0d-118">**Product areas affected**</span></span>         | <span data-ttu-id="5ea0d-119">Supply Chain Management – Masterplanung</span><span class="sxs-lookup"><span data-stu-id="5ea0d-119">Supply Chain Management - Master planning</span></span> |
| <span data-ttu-id="5ea0d-120">**Bereitstellungsoption**</span><span class="sxs-lookup"><span data-stu-id="5ea0d-120">**Deployment option**</span></span>              | <span data-ttu-id="5ea0d-121">Nur Cloud.</span><span class="sxs-lookup"><span data-stu-id="5ea0d-121">Cloud only.</span></span> <span data-ttu-id="5ea0d-122">Planungsoptimierung wird bei lokalen Bereitstellungen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5ea0d-122">Planning Optimization is not supported with on-premises deployments.</span></span> |
| <span data-ttu-id="5ea0d-123">**Status**</span><span class="sxs-lookup"><span data-stu-id="5ea0d-123">**Status**</span></span>                         | <span data-ttu-id="5ea0d-124">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="5ea0d-124">Deprecated.</span></span> <span data-ttu-id="5ea0d-125">Im April 2021 werden Verteilungsszenarien mit dem integrierten Dynamics 365 Supply Chain Management-Masterplanungsmodul nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5ea0d-125">On April 2021, distribution scenarios will no longer be supported with the built-in Dynamics 365 Supply Chain Management master planning engine.</span></span> <span data-ttu-id="5ea0d-126">Für Verteilungsszenarien müssen Kunden die Planungsoptimierung für Masterplanungsberechnungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="5ea0d-126">For distribution scenarios, customers must use Planning Optimization for master planning calculations.</span></span> <span data-ttu-id="5ea0d-127">Weitere Informationen finden Sie unter [Planungsoptimierungsdokumentation](https://go.microsoft.com/fwlink/?linkid=2105830).</span><span class="sxs-lookup"><span data-stu-id="5ea0d-127">For more information, see [Planning Optimization documentation](https://go.microsoft.com/fwlink/?linkid=2105830).</span></span> <span data-ttu-id="5ea0d-128">Kunden mit lokalen Bereitstellungen von Dynamics 365 Supply Chain Management verwenden möglicherweise weiterhin das Supply Chain Management-Masterplanungsmodul für Verteilungsszenarien nach April 2021.</span><span class="sxs-lookup"><span data-stu-id="5ea0d-128">Customers with on-premises deployments of Dynamics 365 Supply Chain Management may continue to use the Supply Chain Management master planning engine for distribution scenarios after April 2021.</span></span> <span data-ttu-id="5ea0d-129">Es werden jedoch keine weiteren Funktionserweiterungen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="5ea0d-129">However, no more feature enhancements will be provided.</span></span> |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="5ea0d-130">Frühere Ankündigungen über entfernte oder veraltete Funktionen</span><span class="sxs-lookup"><span data-stu-id="5ea0d-130">Previous announcements about removed or deprecated features</span></span>

<span data-ttu-id="5ea0d-131">Um mehr über Funktionen zu erfahren, die in früheren Versionen entfernt oder veraltet sind, siehe [Entfernte oder veraltete Funktionen in früheren Versionen](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span><span class="sxs-lookup"><span data-stu-id="5ea0d-131">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span></span>
