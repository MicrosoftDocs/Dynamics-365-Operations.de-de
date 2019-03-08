---
title: Berichterstellungsoptionen in Talent
description: In diesem Thema wird erläutert, wie das Problem behoben wird, bei dem ein Kunde die Microsoft Dynamics 365 for Talent-Berichte anpassen möchte oder neue Berichte erstellen möchte.
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 2007e6adec7255b0b3abda7490c2103a8583393f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "304582"
---
# <a name="reporting-options-in-talent"></a><span data-ttu-id="bb025-103">Berichtsoptionen in Talent</span><span class="sxs-lookup"><span data-stu-id="bb025-103">Reporting options in Talent</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="bb025-104">**Umgebungsdetails**</span><span class="sxs-lookup"><span data-stu-id="bb025-104">**Environment details**</span></span>

<span data-ttu-id="bb025-105">Dieses Problem gilt für alle Umgebungen.</span><span class="sxs-lookup"><span data-stu-id="bb025-105">This issue applies to all environments.</span></span>

<span data-ttu-id="bb025-106">**Symptom**</span><span class="sxs-lookup"><span data-stu-id="bb025-106">**Symptom**</span></span>

<span data-ttu-id="bb025-107">Der Kunde möchte Microsoft Dynamics 365 for Talent-Berichte anpassen oder neue Berichte erstellen.</span><span class="sxs-lookup"><span data-stu-id="bb025-107">The customer wants to customize Microsoft Dynamics 365 for Talent reports or create new reports.</span></span>

<span data-ttu-id="bb025-108">**Abgang**</span><span class="sxs-lookup"><span data-stu-id="bb025-108">**Issue**</span></span>

<span data-ttu-id="bb025-109">Der Benutzer kann die eingebetteten Microsoft Power BI-Berichte nicht anpassen.</span><span class="sxs-lookup"><span data-stu-id="bb025-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="bb025-110">**Lösung**</span><span class="sxs-lookup"><span data-stu-id="bb025-110">**Solution**</span></span>

- <span data-ttu-id="bb025-111">Über die Core HR-Daten, die zum Common Data Service for Apps fließen, kann über den PowerApps CDS mit Power BI Desktop Desktop berichtet werden.</span><span class="sxs-lookup"><span data-stu-id="bb025-111">The Core HR data that flows to Common Data Service for Apps can be reported on via the PowerApps CDS connector to Power BI Desktop.</span></span> <span data-ttu-id="bb025-112">Beachten Sie, dass Common Data Service for Apps eine Untergruppe von Core HR-Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="bb025-112">Note that Common Data Service for Apps contains a subset of Core HR data.</span></span> <span data-ttu-id="bb025-113">Weitere Informationen zu Power BI und Dashboards, finden [Erstellen Power BI Berichte und PowerApps Dashboards mit Common Data Service](https://powerapps.microsoft.com/en-us/blog/cdsconnectortopowerbi) Sie unter.</span><span class="sxs-lookup"><span data-stu-id="bb025-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with PowerApps Common Data Service](https://powerapps.microsoft.com/en-us/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="bb025-114">Elektronische Berichterstellung (EB) ist für manche Berichte in Talent verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bb025-114">Electronic reporting (ER) is available for some reports in Talent.</span></span> <span data-ttu-id="bb025-115">Kundengesteuerte Anpassungen können über die EB-Konfigurationsoptionen erfolgen.</span><span class="sxs-lookup"><span data-stu-id="bb025-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="bb025-116">Daten können nach Microsoft Excel oder Microsoft Word exportiert werden, indem die verschiedenen Datenentitäten verwendet werden, die Talent durch die Microsoft Office-Integration bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="bb025-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Talent provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="bb025-117">**Langfristige Lösung**</span><span class="sxs-lookup"><span data-stu-id="bb025-117">**Long-term solution**</span></span>

<span data-ttu-id="bb025-118">Zusätzliche Power BI-Optionen werden verfügbar sein und mehr Daten und Entitäten werden Teil von Common Data Service for Apps sein.</span><span class="sxs-lookup"><span data-stu-id="bb025-118">Additional Power BI options will be available, and more data and entities will be part of Common Data Service for Apps.</span></span>
