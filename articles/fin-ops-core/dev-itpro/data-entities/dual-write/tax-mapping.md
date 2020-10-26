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
ms.author: rhaertle
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 68461f375c6d5b04f224331dc192c921cf3c4d04
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3979328"
---
# <a name="integrated-tax"></a><span data-ttu-id="81612-103">Integrierte Steuer</span><span class="sxs-lookup"><span data-stu-id="81612-103">Integrated tax</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="81612-104">Steuereinstellungsdaten definieren die Einstellung sowohl für indirekte Steuern (MwSt., GST, Mehrwertsteuer) und Quellensteuer.</span><span class="sxs-lookup"><span data-stu-id="81612-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="81612-105">Es werden die Steuerberechnungsregel, der Steuersatz, die Steuerbuchhaltung, der Steuerausgleich und weitere Konzepte beschrieben.</span><span class="sxs-lookup"><span data-stu-id="81612-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="81612-106">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="81612-106">Templates</span></span>

<span data-ttu-id="81612-107">Steuerdaten enthalten eine Sammlung von Entitätszuordnungen, die während der Dateninteraktion zusammenarbeiten, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="81612-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="81612-108">Finance and Operations Apps</span><span class="sxs-lookup"><span data-stu-id="81612-108">Finance and Operations apps</span></span> | <span data-ttu-id="81612-109">Modellgesteuerte Anwendungen in Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="81612-109">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="81612-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="81612-110">Description</span></span> |
-------------------------|---------------------------------|----|
<span data-ttu-id="81612-111">Artikel-Mehrwertsteuergruppe</span><span class="sxs-lookup"><span data-stu-id="81612-111">Item sales tax group</span></span> | <span data-ttu-id="81612-112">msdyn_taxitemgroups</span><span class="sxs-lookup"><span data-stu-id="81612-112">msdyn_taxitemgroups</span></span> |
<span data-ttu-id="81612-113">Mehrwertsteuer-Behörden</span><span class="sxs-lookup"><span data-stu-id="81612-113">Sales tax authorities</span></span> | <span data-ttu-id="81612-114">msdyn_taxauthorities</span><span class="sxs-lookup"><span data-stu-id="81612-114">msdyn_taxauthorities</span></span> |
<span data-ttu-id="81612-115">Entität „Mehrwertsteuer-Befreiungscode“ in CDS</span><span class="sxs-lookup"><span data-stu-id="81612-115">Sales tax exempt code entity CDS</span></span> | <span data-ttu-id="81612-116">msdyn_taxexemptcodes</span><span class="sxs-lookup"><span data-stu-id="81612-116">msdyn_taxexemptcodes</span></span> |
<span data-ttu-id="81612-117">Mehrwertsteuergruppen</span><span class="sxs-lookup"><span data-stu-id="81612-117">Sales tax groups</span></span> | <span data-ttu-id="81612-118">msdyn_taxgroups</span><span class="sxs-lookup"><span data-stu-id="81612-118">msdyn_taxgroups</span></span> |
<span data-ttu-id="81612-119">Mehrwertsteuer-Sachkontobuchungsgruppen V2</span><span class="sxs-lookup"><span data-stu-id="81612-119">Sales tax ledger posting groups V2</span></span> | <span data-ttu-id="81612-120">msdyn_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="81612-120">msdyn_taxpostinggroups</span></span> |
<span data-ttu-id="81612-121">Quellensteuercodes</span><span class="sxs-lookup"><span data-stu-id="81612-121">Withholding tax codes</span></span> | <span data-ttu-id="81612-122">msdyn_withholdingtaxcodes</span><span class="sxs-lookup"><span data-stu-id="81612-122">msdyn_withholdingtaxcodes</span></span> |
<span data-ttu-id="81612-123">Quellensteuergruppen</span><span class="sxs-lookup"><span data-stu-id="81612-123">Withholding tax groups</span></span> | <span data-ttu-id="81612-124">msdyn_withholdingtaxgroups</span><span class="sxs-lookup"><span data-stu-id="81612-124">msdyn_withholdingtaxgroups</span></span> | 


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

