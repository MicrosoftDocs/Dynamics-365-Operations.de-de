---
title: Integrierte Steuer
description: In diesem Thema wird die Integration von Steuerdaten zwischen Finance and Operations and Dataverse beschrieben.
author: robinarh
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: rhaertle
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 14c22dd6602b5fbf866c8dc6b057f6c8acb1f48f
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679295"
---
# <a name="integrated-tax"></a><span data-ttu-id="95d35-103">Integrierte Steuer</span><span class="sxs-lookup"><span data-stu-id="95d35-103">Integrated tax</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="95d35-104">Steuereinstellungsdaten definieren die Einstellung sowohl für indirekte Steuern (MwSt., GST, Mehrwertsteuer) und Quellensteuer.</span><span class="sxs-lookup"><span data-stu-id="95d35-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="95d35-105">Es werden die Steuerberechnungsregel, der Steuersatz, die Steuerbuchhaltung, der Steuerausgleich und weitere Konzepte beschrieben.</span><span class="sxs-lookup"><span data-stu-id="95d35-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="95d35-106">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="95d35-106">Templates</span></span>

<span data-ttu-id="95d35-107">Steuerdaten enthalten eine Sammlung von Tabellenzuordnungen, die während der Dateninteraktion zusammenarbeiten, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="95d35-107">Tax data includes a collection of table maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="95d35-108">Finance and Operations Apps</span><span class="sxs-lookup"><span data-stu-id="95d35-108">Finance and Operations apps</span></span> | <span data-ttu-id="95d35-109">Modellgesteuerte Anwendungen in Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="95d35-109">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="95d35-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="95d35-110">Description</span></span> |
-------------------------|---------------------------------|----|
<span data-ttu-id="95d35-111">Artikel-Mehrwertsteuergruppe</span><span class="sxs-lookup"><span data-stu-id="95d35-111">Item sales tax group</span></span> | <span data-ttu-id="95d35-112">msdyn_taxitemgroups</span><span class="sxs-lookup"><span data-stu-id="95d35-112">msdyn_taxitemgroups</span></span> |
<span data-ttu-id="95d35-113">Mehrwertsteuer-Behörden</span><span class="sxs-lookup"><span data-stu-id="95d35-113">Sales tax authorities</span></span> | <span data-ttu-id="95d35-114">msdyn_taxauthorities</span><span class="sxs-lookup"><span data-stu-id="95d35-114">msdyn_taxauthorities</span></span> |
<span data-ttu-id="95d35-115">Entität „Mehrwertsteuer-Befreiungscode“ in CDS</span><span class="sxs-lookup"><span data-stu-id="95d35-115">Sales tax exempt code entity CDS</span></span> | <span data-ttu-id="95d35-116">msdyn_taxexemptcodes</span><span class="sxs-lookup"><span data-stu-id="95d35-116">msdyn_taxexemptcodes</span></span> |
<span data-ttu-id="95d35-117">Mehrwertsteuergruppen</span><span class="sxs-lookup"><span data-stu-id="95d35-117">Sales tax groups</span></span> | <span data-ttu-id="95d35-118">msdyn_taxgroups</span><span class="sxs-lookup"><span data-stu-id="95d35-118">msdyn_taxgroups</span></span> |
<span data-ttu-id="95d35-119">Mehrwertsteuer-Sachkontobuchungsgruppen V2</span><span class="sxs-lookup"><span data-stu-id="95d35-119">Sales tax ledger posting groups V2</span></span> | <span data-ttu-id="95d35-120">msdyn_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="95d35-120">msdyn_taxpostinggroups</span></span> |
<span data-ttu-id="95d35-121">Quellensteuercodes</span><span class="sxs-lookup"><span data-stu-id="95d35-121">Withholding tax codes</span></span> | <span data-ttu-id="95d35-122">msdyn_withholdingtaxcodes</span><span class="sxs-lookup"><span data-stu-id="95d35-122">msdyn_withholdingtaxcodes</span></span> |
<span data-ttu-id="95d35-123">Quellensteuergruppen</span><span class="sxs-lookup"><span data-stu-id="95d35-123">Withholding tax groups</span></span> | <span data-ttu-id="95d35-124">msdyn_withholdingtaxgroups</span><span class="sxs-lookup"><span data-stu-id="95d35-124">msdyn_withholdingtaxgroups</span></span> | 


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

