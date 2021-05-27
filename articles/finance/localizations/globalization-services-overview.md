---
title: Dynamics 365 Globalisierungsdienste
description: Dieses Thema enthält eine Übersicht über die Microsoft Dynamics 365 Globalisierungsdienste.
author: JaneA07
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Electronic invoicing, Tax calculation
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 2ef942f7f6dac2c321a51800ade0bf25f2162304
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018806"
---
# <a name="dynamics-365-globalization-services"></a><span data-ttu-id="b969a-103">Dynamics 365 Globalisierungsdienste</span><span class="sxs-lookup"><span data-stu-id="b969a-103">Dynamics 365 globalization services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b969a-104">Die folgenden Globalisierungsdienste können konfiguriert werden, um die in einigen Diensten von Microsoft Dynamics 365 Online vorhandenen Funktionen zu erweitern:</span><span class="sxs-lookup"><span data-stu-id="b969a-104">The following globalization services can be configured to extend the capabilities that exist in some Microsoft Dynamics 365 online services:</span></span>

- <span data-ttu-id="b969a-105">**Regulatory Configuration Service (RCS)** unterstützt die Konfiguration verschiedener Arten von elektronischen Dokumenten und Berichten.</span><span class="sxs-lookup"><span data-stu-id="b969a-105">**Regulatory Configuration Service (RCS)** supports the configuration of different types of electronic documents and reports.</span></span> <span data-ttu-id="b969a-106">RCS bietet eine erweiterte Version des Designers der elektronischen Berichtserstellung (EB) bei dem das Konfigurations-Repository ein eigenständiger Dienst ist.</span><span class="sxs-lookup"><span data-stu-id="b969a-106">RCS provides an enhanced version of the Electronic reporting (ER) designer where the configuration repository is a standalone service.</span></span> <span data-ttu-id="b969a-107">Weitere Informationen finden Sie unter [Regulatory Configuration Service](rcs-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b969a-107">For more information, see [Regulatory Configuration Service](rcs-overview.md).</span></span>
- <span data-ttu-id="b969a-108">**Elektronische Rechnungsstellung** vereint konfigurierbare Formate für Transformationen, digitale Signaturen und konfigurierbare Integrationen für die Konnektivität mit externen Webdiensten, einschließlich Zertifizierung und Antwortverarbeitung.</span><span class="sxs-lookup"><span data-stu-id="b969a-108">**Electronic Invoicing** brings together configurable formats for transformations, digital signatures, and configurable integrations for connectivity with external web services, including certification and response handling.</span></span> <span data-ttu-id="b969a-109">Weitere Informationen finden Sie unter [Elektronische Rechnungsstellung](e-invoicing-service-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b969a-109">For more information, see [Electronic Invoicing](e-invoicing-service-overview.md).</span></span>
- <span data-ttu-id="b969a-110">**Steuerberechnung** bietet mehr Flexibilität durch die Unterstützung mehrerer Steuer-IDs, die Bestimmung von Steuercodes, den Steuerberechnungsdesigner und eine Laufzeit-Engine zur Einhaltung komplexer Steuervorschriften weltweit.</span><span class="sxs-lookup"><span data-stu-id="b969a-110">**Tax Calculation** provides enhanced flexibility by supporting multiple tax IDs, tax code determination, the tax calculation designer, and a runtime engine to comply with complex tax regulations worldwide.</span></span> <span data-ttu-id="b969a-111">Weitere Informationen finden Sie unter [Steuerberechnung](global-tax-calcuation-service-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b969a-111">For more information, see [Tax Calculation](global-tax-calcuation-service-overview.md).</span></span>

<span data-ttu-id="b969a-112">Diese Globalisierungsdienste bieten eine sofort einsatzbereite Integration mit den folgenden Dynamics 365-Onlinediensten.</span><span class="sxs-lookup"><span data-stu-id="b969a-112">These globalization services provide out-of-box integration with the following Dynamics 365 online services.</span></span>

| <span data-ttu-id="b969a-113">Onlinedienst</span><span class="sxs-lookup"><span data-stu-id="b969a-113">Online service</span></span> | <span data-ttu-id="b969a-114">RCS</span><span class="sxs-lookup"><span data-stu-id="b969a-114">RCS</span></span> | <span data-ttu-id="b969a-115">Elektronische Rechnungsstellung</span><span class="sxs-lookup"><span data-stu-id="b969a-115">Electronic Invoicing</span></span> | <span data-ttu-id="b969a-116">Steuerberechnung (Vorschau)</span><span class="sxs-lookup"><span data-stu-id="b969a-116">Tax Calculation (Preview)</span></span> |
|----------------|-----|----------------------|---------------------------|
| <span data-ttu-id="b969a-117">Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="b969a-117">Dynamics 365 Finance</span></span> | <span data-ttu-id="b969a-118">Ja</span><span class="sxs-lookup"><span data-stu-id="b969a-118">Yes</span></span> | <span data-ttu-id="b969a-119">Ja</span><span class="sxs-lookup"><span data-stu-id="b969a-119">Yes</span></span> | <span data-ttu-id="b969a-120">Ja</span><span class="sxs-lookup"><span data-stu-id="b969a-120">Yes</span></span> | 
| <span data-ttu-id="b969a-121">Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="b969a-121">Dynamics 365 Supply Chain Management</span></span> | <span data-ttu-id="b969a-122">Ja</span><span class="sxs-lookup"><span data-stu-id="b969a-122">Yes</span></span> | <span data-ttu-id="b969a-123">Ja</span><span class="sxs-lookup"><span data-stu-id="b969a-123">Yes</span></span> | <span data-ttu-id="b969a-124">Ja</span><span class="sxs-lookup"><span data-stu-id="b969a-124">Yes</span></span> | 
| <span data-ttu-id="b969a-125">Dynamics 365 Project Operations</span><span class="sxs-lookup"><span data-stu-id="b969a-125">Dynamics 365 Project Operations</span></span> | <span data-ttu-id="b969a-126">Ja</span><span class="sxs-lookup"><span data-stu-id="b969a-126">Yes</span></span> | <span data-ttu-id="b969a-127">Ja</span><span class="sxs-lookup"><span data-stu-id="b969a-127">Yes</span></span> | <span data-ttu-id="b969a-128">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="b969a-128">Not applicable</span></span> | 
| <span data-ttu-id="b969a-129">Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="b969a-129">Dynamics 365 Commerce</span></span> | <span data-ttu-id="b969a-130">Ja</span><span class="sxs-lookup"><span data-stu-id="b969a-130">Yes</span></span> | <span data-ttu-id="b969a-131">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="b969a-131">Not applicable</span></span> | <span data-ttu-id="b969a-132">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="b969a-132">Not applicable</span></span> | 

> [!NOTE]
> <span data-ttu-id="b969a-133">Aufgrund der unterschiedlichen Verfügbarkeit von geografischen Azure-Standorten (Geos) für RCS kann die Konfiguration dieses Dienstes dazu führen, dass Debitorendaten außerhalb der für den entsprechenden Dynamics 365-Onlinedienst ausgewählten Geo übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="b969a-133">Because of differences in the availability of Azure geographic locations (geos) for RCS, configuration of this service might cause customer data to be transferred outside the geo that is selected for the applicable Dynamics 365 online service.</span></span> <span data-ttu-id="b969a-134">Weitere Informationen finden Sie unter [Dynamics 365 und Power Platform: Verfügbarkeit, Datenstandort, Sprache und Lokalisierung](https://aka.ms/rcs/D365Productavailabilityguide).</span><span class="sxs-lookup"><span data-stu-id="b969a-134">For more information, see [Dynamics 365 and Power Platform: Availability, data location, language, and localization](https://aka.ms/rcs/D365Productavailabilityguide).</span></span>