---
title: Integrierte Standorte und Lagerorte
description: In diesem Thema wird die Integration von Stand- und Lagerortdaten zwischen Finance and Operations and Dataverse beschrieben.
author: t-benebo
ms.date: 10/09/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: 533635ece005636dcee4e24d1d132111e1e2b370
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750665"
---
# <a name="integrated-sites-and-warehouses"></a><span data-ttu-id="0c890-103">Integrierte Standorte und Lagerorte</span><span class="sxs-lookup"><span data-stu-id="0c890-103">Integrated sites and warehouses</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="0c890-104">In diesem Thema wird die Integration von Stand- und Lagerortdaten zwischen Finance and Operations and Dataverse beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0c890-104">This topic describes the integration of site and warehouse data between Finance and Operations and Dataverse.</span></span> <span data-ttu-id="0c890-105">Betriebsstandorte und Lagerorte sind allgemeine Konzepte in einer Supply Chain Management-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="0c890-105">Operational sites and warehouses are common concepts in a Supply Chain Management application.</span></span> <span data-ttu-id="0c890-106">Sie werden verwendet, um die Lieferkette des Unternehmens zu modellieren.</span><span class="sxs-lookup"><span data-stu-id="0c890-106">They are used to model the supply chain of your company.</span></span>

## <a name="templates"></a><span data-ttu-id="0c890-107">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="0c890-107">Templates</span></span>

<span data-ttu-id="0c890-108">Bei der Integration in Dataverse sind diese Konzepte und alle ihre zugehörigen Informationen in Dataverse mithilfe der Standort- und Lagerortdatentabellen in der folgenden Tabelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0c890-108">With the integration with Dataverse, these concepts and all their related information are available in Dataverse using the sites and warehouses data tables in the following table.</span></span>

<span data-ttu-id="0c890-109">Finance and Operations Apps</span><span class="sxs-lookup"><span data-stu-id="0c890-109">Finance and Operations apps</span></span> | <span data-ttu-id="0c890-110">Sonstige Dynamics 365-Apps</span><span class="sxs-lookup"><span data-stu-id="0c890-110">Other Dynamics 365 apps</span></span> | <span data-ttu-id="0c890-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0c890-111">Description</span></span>
--------------------------|---------------------------|---
<span data-ttu-id="0c890-112">Websites</span><span class="sxs-lookup"><span data-stu-id="0c890-112">Sites</span></span> | <span data-ttu-id="0c890-113">msdyn_operationalsites</span><span class="sxs-lookup"><span data-stu-id="0c890-113">msdyn_operationalsites</span></span> | 
<span data-ttu-id="0c890-114">Lagerorte</span><span class="sxs-lookup"><span data-stu-id="0c890-114">Warehouses</span></span> | <span data-ttu-id="0c890-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="0c890-115">msdyn_warehouses</span></span> | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]