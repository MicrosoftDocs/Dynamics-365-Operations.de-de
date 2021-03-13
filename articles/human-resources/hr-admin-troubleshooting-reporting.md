---
title: Sonstige Berichtsoptionen
description: In diesem Artikel wird erläutert, wie das Problem behoben wird, bei dem ein Kunde die Microsoft Dynamics 365 Human Resources-Berichte anpassen möchte oder neue Berichte erstellen möchte.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 830c8c32128a8dfc1b009557afb272e48ae3a1ff
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112640"
---
# <a name="reporting-options"></a><span data-ttu-id="0a4b8-103">Sonstige Berichtsoptionen</span><span class="sxs-lookup"><span data-stu-id="0a4b8-103">Reporting options</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="0a4b8-104">**Umgebungsdetails**</span><span class="sxs-lookup"><span data-stu-id="0a4b8-104">**Environment details**</span></span>

<span data-ttu-id="0a4b8-105">Dieses Problem gilt für alle Umgebungen.</span><span class="sxs-lookup"><span data-stu-id="0a4b8-105">This issue applies to all environments.</span></span>

<span data-ttu-id="0a4b8-106">**Symptom**</span><span class="sxs-lookup"><span data-stu-id="0a4b8-106">**Symptom**</span></span>

<span data-ttu-id="0a4b8-107">Der Kunde möchte Microsoft Dynamics 365 Human Resources-Berichte anpassen oder neue Berichte erstellen.</span><span class="sxs-lookup"><span data-stu-id="0a4b8-107">The customer wants to customize Microsoft Dynamics 365 Human Resources reports or create new reports.</span></span>

<span data-ttu-id="0a4b8-108">**Abgang**</span><span class="sxs-lookup"><span data-stu-id="0a4b8-108">**Issue**</span></span>

<span data-ttu-id="0a4b8-109">Der Benutzer kann die eingebetteten Microsoft Power BI-Berichte nicht anpassen.</span><span class="sxs-lookup"><span data-stu-id="0a4b8-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="0a4b8-110">**Lösung**</span><span class="sxs-lookup"><span data-stu-id="0a4b8-110">**Solution**</span></span>

- <span data-ttu-id="0a4b8-111">Über die Human Resources-Daten, die zu Dataverse fließen, kann über den Power Apps Dataverse-Connector zu Power BI Desktop berichtet werden.</span><span class="sxs-lookup"><span data-stu-id="0a4b8-111">The Human Resources data that flows to Dataverse can be reported on via the Power Apps Dataverse connector to Power BI Desktop.</span></span> <span data-ttu-id="0a4b8-112">Beachten Sie, dass Dataverse eine Untergruppe von Human Resources-Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="0a4b8-112">Note that Dataverse contains a subset of Human Resources data.</span></span> <span data-ttu-id="0a4b8-113">Weitere Informationen zu Power BI und Dashboards finden Sie unter [Erstellen von Power BI-Berichten mit Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span><span class="sxs-lookup"><span data-stu-id="0a4b8-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="0a4b8-114">Elektronische Berichterstellung (EB) ist für manche Berichte in Human Resources verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0a4b8-114">Electronic reporting (ER) is available for some reports in Human Resources.</span></span> <span data-ttu-id="0a4b8-115">Kundengesteuerte Anpassungen können über die EB-Konfigurationsoptionen erfolgen.</span><span class="sxs-lookup"><span data-stu-id="0a4b8-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="0a4b8-116">Daten können nach Microsoft Excel oder Microsoft Word exportiert werden, indem die verschiedenen Datenentitäten verwendet werden, die Human Resources durch die Microsoft Office-Integration bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="0a4b8-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Human Resources provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="0a4b8-117">**Langfristige Lösung**</span><span class="sxs-lookup"><span data-stu-id="0a4b8-117">**Long-term solution**</span></span>

<span data-ttu-id="0a4b8-118">Zusätzliche Power BI-Optionen werden verfügbar sein und mehr Daten und Entitäten werden Teil von Dataverse  sein.</span><span class="sxs-lookup"><span data-stu-id="0a4b8-118">Additional Power BI options will be available, and more data and entities will be part of Dataverse.</span></span>
