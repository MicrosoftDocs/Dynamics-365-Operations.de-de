---
title: Integrierte Steuer
description: In diesem Thema wird die Integration von Steuerdaten zwischen Finance and Operations and Common Data Service beschrieben.
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
ms.openlocfilehash: 0d32a5f7859f0200da823a73d94b9a6b2a9c8e7d
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019796"
---
# <a name="integrated-tax"></a><span data-ttu-id="f4425-103">Integrierte Steuer</span><span class="sxs-lookup"><span data-stu-id="f4425-103">Integrated tax</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="f4425-104">Steuereinstellungsdaten definieren die Einstellung sowohl für indirekte Steuern (MwSt., GST, Mehrwertsteuer) und Quellensteuer.</span><span class="sxs-lookup"><span data-stu-id="f4425-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="f4425-105">Es werden die Steuerberechnungsregel, der Steuersatz, die Steuerbuchhaltung, der Steuerausgleich und weitere Konzepte beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f4425-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="f4425-106">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="f4425-106">Templates</span></span>

<span data-ttu-id="f4425-107">Steuerdaten enthalten eine Sammlung von Entitätszuordnungen, die während der Dateninteraktion zusammenarbeiten, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="f4425-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="f4425-108">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f4425-108">Finance and Operations</span></span>   | <span data-ttu-id="f4425-109">Sonstige Dynamics 365-Apps</span><span class="sxs-lookup"><span data-stu-id="f4425-109">Other Dynamics 365 apps</span></span>
-------------------------|---------------------------------
<span data-ttu-id="f4425-110">Steuercodes</span><span class="sxs-lookup"><span data-stu-id="f4425-110">Tax codes</span></span>                  | <span data-ttu-id="f4425-111">msdyn\_taxcodes.md</span><span class="sxs-lookup"><span data-stu-id="f4425-111">msdyn\_taxcodes.md</span></span>
<span data-ttu-id="f4425-112">Steuergruppen</span><span class="sxs-lookup"><span data-stu-id="f4425-112">Tax groups</span></span>               | <span data-ttu-id="f4425-113">msdyn\_taxgroups.md</span><span class="sxs-lookup"><span data-stu-id="f4425-113">msdyn\_taxgroups.md</span></span>
<span data-ttu-id="f4425-114">Steuerpostengruppen</span><span class="sxs-lookup"><span data-stu-id="f4425-114">Tax item groups</span></span>          | <span data-ttu-id="f4425-115">msdyn\_taxitemgroups.md</span><span class="sxs-lookup"><span data-stu-id="f4425-115">msdyn\_taxitemgroups.md</span></span>
<span data-ttu-id="f4425-116">Steuerbefreiungen</span><span class="sxs-lookup"><span data-stu-id="f4425-116">Tax Exemptions</span></span>           | <span data-ttu-id="f4425-117">msdyn\_taxexemptcodes.md</span><span class="sxs-lookup"><span data-stu-id="f4425-117">msdyn\_taxexemptcodes.md</span></span>
<span data-ttu-id="f4425-118">Steuerbehörden</span><span class="sxs-lookup"><span data-stu-id="f4425-118">Tax Authorities</span></span>          | <span data-ttu-id="f4425-119">msdyn\_taxauthorities.md</span><span class="sxs-lookup"><span data-stu-id="f4425-119">msdyn\_taxauthorities.md</span></span>
<span data-ttu-id="f4425-120">Quellensteuercodes</span><span class="sxs-lookup"><span data-stu-id="f4425-120">Withholding tax codes</span></span>      | <span data-ttu-id="f4425-121">msdyn\_withholdingtaxcodes.md</span><span class="sxs-lookup"><span data-stu-id="f4425-121">msdyn\_withholdingtaxcodes.md</span></span>
<span data-ttu-id="f4425-122">Quellensteuergruppen</span><span class="sxs-lookup"><span data-stu-id="f4425-122">Withholding tax groups</span></span>   | <span data-ttu-id="f4425-123">msdyn\_withholdingtaxgroups.md</span><span class="sxs-lookup"><span data-stu-id="f4425-123">msdyn\_withholdingtaxgroups.md</span></span>
<span data-ttu-id="f4425-124">Steuersachkontengruppe</span><span class="sxs-lookup"><span data-stu-id="f4425-124">Tax Ledger Account Group</span></span> | <span data-ttu-id="f4425-125">msdyn\_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="f4425-125">msdyn\_taxpostinggroups</span></span>  

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

