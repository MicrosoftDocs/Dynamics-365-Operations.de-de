---
title: Integrierte Steuer
description: In diesem Thema wird die Integration von Steuerdaten zwischen Finance and Operations und Common Data Service beschrieben.
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ''
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 86e74086a5a74c7af5f2572d1a653a1658d729c0
ms.sourcegitcommit: d0322d1ed6c798301058e44dae76227a0e1f49ac
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "2853858"
---
# <a name="integrated-tax"></a><span data-ttu-id="3f168-103">Integrierte Steuer</span><span class="sxs-lookup"><span data-stu-id="3f168-103">Integrated tax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3f168-104">Steuereinstellungsdaten definieren die Einstellung sowohl für indirekte Steuern (MwSt., GST, Mehrwertsteuer) und Quellensteuer.</span><span class="sxs-lookup"><span data-stu-id="3f168-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="3f168-105">Es werden die Steuerberechnungsregel, der Steuersatz, die Steuerbuchhaltung, der Steuerausgleich und weitere Konzepte beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3f168-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="3f168-106">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="3f168-106">Templates</span></span>

<span data-ttu-id="3f168-107">Steuerdaten enthalten eine Sammlung von Entitätszuordnungen, die während der Dateninteraktion zusammenarbeiten, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="3f168-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="3f168-108">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3f168-108">Finance and Operations</span></span>   | <span data-ttu-id="3f168-109">Sonstige Dynamics 365-Apps</span><span class="sxs-lookup"><span data-stu-id="3f168-109">Other Dynamics 365 apps</span></span>
-------------------------|---------------------------------
<span data-ttu-id="3f168-110">Steuercodes</span><span class="sxs-lookup"><span data-stu-id="3f168-110">Tax codes</span></span>                  | <span data-ttu-id="3f168-111">msdyn\_taxcodes.md</span><span class="sxs-lookup"><span data-stu-id="3f168-111">msdyn\_taxcodes.md</span></span>
<span data-ttu-id="3f168-112">Steuergruppen</span><span class="sxs-lookup"><span data-stu-id="3f168-112">Tax groups</span></span>               | <span data-ttu-id="3f168-113">msdyn\_taxgroups.md</span><span class="sxs-lookup"><span data-stu-id="3f168-113">msdyn\_taxgroups.md</span></span>
<span data-ttu-id="3f168-114">Steuerpostengruppen</span><span class="sxs-lookup"><span data-stu-id="3f168-114">Tax item groups</span></span>          | <span data-ttu-id="3f168-115">msdyn\_taxitemgroups.md</span><span class="sxs-lookup"><span data-stu-id="3f168-115">msdyn\_taxitemgroups.md</span></span>
<span data-ttu-id="3f168-116">Steuerbefreiungen</span><span class="sxs-lookup"><span data-stu-id="3f168-116">Tax Exemptions</span></span>           | <span data-ttu-id="3f168-117">msdyn\_taxexemptcodes.md</span><span class="sxs-lookup"><span data-stu-id="3f168-117">msdyn\_taxexemptcodes.md</span></span>
<span data-ttu-id="3f168-118">Steuerbehörden</span><span class="sxs-lookup"><span data-stu-id="3f168-118">Tax Authorities</span></span>          | <span data-ttu-id="3f168-119">msdyn\_taxauthorities.md</span><span class="sxs-lookup"><span data-stu-id="3f168-119">msdyn\_taxauthorities.md</span></span>
<span data-ttu-id="3f168-120">Quellensteuercodes</span><span class="sxs-lookup"><span data-stu-id="3f168-120">Withholding tax codes</span></span>      | <span data-ttu-id="3f168-121">msdyn\_withholdingtaxcodes.md</span><span class="sxs-lookup"><span data-stu-id="3f168-121">msdyn\_withholdingtaxcodes.md</span></span>
<span data-ttu-id="3f168-122">Quellensteuergruppen</span><span class="sxs-lookup"><span data-stu-id="3f168-122">Withholding tax groups</span></span>   | <span data-ttu-id="3f168-123">msdyn\_withholdingtaxgroups.md</span><span class="sxs-lookup"><span data-stu-id="3f168-123">msdyn\_withholdingtaxgroups.md</span></span>
<span data-ttu-id="3f168-124">Steuersachkontengruppe</span><span class="sxs-lookup"><span data-stu-id="3f168-124">Tax Ledger Account Group</span></span> | <span data-ttu-id="3f168-125">msdyn\_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="3f168-125">msdyn\_taxpostinggroups</span></span>  

[!include [banner](../includes/dual-write-symbols.md)]

[!include [Tax groups](dual-write/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](dual-write/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](dual-write/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](dual-write/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](dual-write/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](dual-write/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](dual-write/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

