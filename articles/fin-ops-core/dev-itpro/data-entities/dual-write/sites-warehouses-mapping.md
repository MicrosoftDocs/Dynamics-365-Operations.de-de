---
title: Integrierte Standorte und Lagerorte
description: In diesem Thema wird die Integration von Stand- und Lagerortdaten zwischen Finance and Operations and Dataverse beschrieben.
author: t-benebo
manager: AnnBe
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
ms.openlocfilehash: b93e5f15e281c20f8688d496fc78f8b46b8aa996
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560360"
---
# <a name="integrated-sites-and-warehouses"></a><span data-ttu-id="cc4b1-103">Integrierte Standorte und Lagerorte</span><span class="sxs-lookup"><span data-stu-id="cc4b1-103">Integrated sites and warehouses</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="cc4b1-104">In diesem Thema wird die Integration von Stand- und Lagerortdaten zwischen Finance and Operations and Dataverse beschrieben.</span><span class="sxs-lookup"><span data-stu-id="cc4b1-104">This topic describes the integration of site and warehouse data between Finance and Operations and Dataverse.</span></span> <span data-ttu-id="cc4b1-105">Betriebsstandorte und Lagerorte sind allgemeine Konzepte in einer Supply Chain Management-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="cc4b1-105">Operational sites and warehouses are common concepts in a Supply Chain Management application.</span></span> <span data-ttu-id="cc4b1-106">Sie werden verwendet, um die Lieferkette des Unternehmens zu modellieren.</span><span class="sxs-lookup"><span data-stu-id="cc4b1-106">They are used to model the supply chain of your company.</span></span>

## <a name="templates"></a><span data-ttu-id="cc4b1-107">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="cc4b1-107">Templates</span></span>

<span data-ttu-id="cc4b1-108">Bei der Integration in Dataverse sind diese Konzepte und alle ihre zugehörigen Informationen in Dataverse mithilfe der Standort- und Lagerortdatentabellen in der folgenden Tabelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cc4b1-108">With the integration with Dataverse, these concepts and all their related information are available in Dataverse using the sites and warehouses data tables in the following table.</span></span>

<span data-ttu-id="cc4b1-109">Finance and Operations Apps</span><span class="sxs-lookup"><span data-stu-id="cc4b1-109">Finance and Operations apps</span></span> | <span data-ttu-id="cc4b1-110">Sonstige Dynamics 365-Apps</span><span class="sxs-lookup"><span data-stu-id="cc4b1-110">Other Dynamics 365 apps</span></span> | <span data-ttu-id="cc4b1-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cc4b1-111">Description</span></span>
--------------------------|---------------------------|---
<span data-ttu-id="cc4b1-112">Websites</span><span class="sxs-lookup"><span data-stu-id="cc4b1-112">Sites</span></span> | <span data-ttu-id="cc4b1-113">msdyn_operationalsites</span><span class="sxs-lookup"><span data-stu-id="cc4b1-113">msdyn_operationalsites</span></span> | 
<span data-ttu-id="cc4b1-114">Lagerorte</span><span class="sxs-lookup"><span data-stu-id="cc4b1-114">Warehouses</span></span> | <span data-ttu-id="cc4b1-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="cc4b1-115">msdyn_warehouses</span></span> | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]