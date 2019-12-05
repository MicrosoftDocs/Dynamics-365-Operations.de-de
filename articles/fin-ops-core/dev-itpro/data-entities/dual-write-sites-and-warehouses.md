---
title: Integrierte Standorte und Lagerorte
description: In diesem Thema wird die Integration von Stand- und Lagerortdaten zwischen Finance and Operations und Common Data Service beschrieben.
author: t-benebo
manager: AnnBe
ms.date: 10/09/2019
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
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: 4cf402e2811aaf92ddfa78eaf6d8887d88d93cbc
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770986"
---
# <a name="integrated-sites-and-warehouses"></a><span data-ttu-id="e815c-103">Integrierte Standorte und Lagerorte</span><span class="sxs-lookup"><span data-stu-id="e815c-103">Integrated sites and warehouses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e815c-104">In diesem Thema wird die Integration von Stand- und Lagerortdaten zwischen Finance and Operations und Common Data Service beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e815c-104">This topic describes the integration of site and warehouse data between Finance and Operations and Common Data Service.</span></span> <span data-ttu-id="e815c-105">Betriebsstandorte und Lagerorte sind allgemeine Konzepte in einer Supply Chain Management-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="e815c-105">Operational sites and warehouses are common concepts in a Supply Chain Management application.</span></span> <span data-ttu-id="e815c-106">Sie werden verwendet, um die Lieferkette des Unternehmens zu modellieren.</span><span class="sxs-lookup"><span data-stu-id="e815c-106">They are used to model the supply chain of your company.</span></span>

## <a name="templates"></a><span data-ttu-id="e815c-107">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="e815c-107">Templates</span></span>

<span data-ttu-id="e815c-108">Bei der Integration in Common Data Service sind diese Konzepte und all ihre zugehörigen Informationen in Common Data Service mithilfe der Standort- und Lagerortdatenentitäten in der folgenden Tabelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e815c-108">With the integration with Common Data Service, these concepts and all their related information are available in Common Data Service using the sites and warehouses data entities in the following table.</span></span>

<span data-ttu-id="e815c-109">Finance and Operations-Apps</span><span class="sxs-lookup"><span data-stu-id="e815c-109">Finance and Operations apps</span></span> | <span data-ttu-id="e815c-110">Sonstige Dynamics 365-Apps</span><span class="sxs-lookup"><span data-stu-id="e815c-110">Other Dynamics 365 apps</span></span> | <span data-ttu-id="e815c-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e815c-111">Description</span></span>
--------------------------|---------------------------|---
<span data-ttu-id="e815c-112">Websites</span><span class="sxs-lookup"><span data-stu-id="e815c-112">Sites</span></span> | <span data-ttu-id="e815c-113">msdyn_operationalsites</span><span class="sxs-lookup"><span data-stu-id="e815c-113">msdyn_operationalsites</span></span> | 
<span data-ttu-id="e815c-114">Lagerorte</span><span class="sxs-lookup"><span data-stu-id="e815c-114">Warehouses</span></span> | <span data-ttu-id="e815c-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="e815c-115">msdyn_warehouses</span></span> | 

[!include [symbols](../includes/dual-write-symbols.md)]

[!include [operational sites](dual-write/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](dual-write/InventWarehouseEntity-msdyn-warehouse.md)]

