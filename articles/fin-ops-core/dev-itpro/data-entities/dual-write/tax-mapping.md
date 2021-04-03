---
title: Integrierte Steuer
description: In diesem Thema wird die Integration von Steuerdaten zwischen Finance and Operations and Dataverse beschrieben.
author: robinarh
manager: AnnBe
ms.date: 09/06/2019
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
ms.author: rhaertle
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 7501ef21492a96c81b971e1d9077beaba9be897b
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560336"
---
# <a name="integrated-tax"></a><span data-ttu-id="90016-103">Integrierte Steuer</span><span class="sxs-lookup"><span data-stu-id="90016-103">Integrated tax</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="90016-104">Steuereinstellungsdaten definieren die Einstellung sowohl für indirekte Steuern (MwSt., GST, Mehrwertsteuer) und Quellensteuer.</span><span class="sxs-lookup"><span data-stu-id="90016-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="90016-105">Es werden die Steuerberechnungsregel, der Steuersatz, die Steuerbuchhaltung, der Steuerausgleich und weitere Konzepte beschrieben.</span><span class="sxs-lookup"><span data-stu-id="90016-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="90016-106">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="90016-106">Templates</span></span>

<span data-ttu-id="90016-107">Steuerdaten enthalten eine Sammlung von Tabellenzuordnungen, die während der Dateninteraktion zusammenarbeiten, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="90016-107">Tax data includes a collection of table maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="90016-108">Finance and Operations Apps</span><span class="sxs-lookup"><span data-stu-id="90016-108">Finance and Operations apps</span></span> | <span data-ttu-id="90016-109">Modellgesteuerte Anwendungen in Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="90016-109">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="90016-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="90016-110">Description</span></span> |
-------------------------|---------------------------------|----|
<span data-ttu-id="90016-111">Artikel-Mehrwertsteuergruppe</span><span class="sxs-lookup"><span data-stu-id="90016-111">Item sales tax group</span></span> | <span data-ttu-id="90016-112">msdyn_taxitemgroups</span><span class="sxs-lookup"><span data-stu-id="90016-112">msdyn_taxitemgroups</span></span> |
<span data-ttu-id="90016-113">Mehrwertsteuer-Behörden</span><span class="sxs-lookup"><span data-stu-id="90016-113">Sales tax authorities</span></span> | <span data-ttu-id="90016-114">msdyn_taxauthorities</span><span class="sxs-lookup"><span data-stu-id="90016-114">msdyn_taxauthorities</span></span> |
<span data-ttu-id="90016-115">Entität „Mehrwertsteuer-Befreiungscode“ in CDS</span><span class="sxs-lookup"><span data-stu-id="90016-115">Sales tax exempt code entity CDS</span></span> | <span data-ttu-id="90016-116">msdyn_taxexemptcodes</span><span class="sxs-lookup"><span data-stu-id="90016-116">msdyn_taxexemptcodes</span></span> |
<span data-ttu-id="90016-117">Mehrwertsteuergruppen</span><span class="sxs-lookup"><span data-stu-id="90016-117">Sales tax groups</span></span> | <span data-ttu-id="90016-118">msdyn_taxgroups</span><span class="sxs-lookup"><span data-stu-id="90016-118">msdyn_taxgroups</span></span> |
<span data-ttu-id="90016-119">Mehrwertsteuer-Sachkontobuchungsgruppen V2</span><span class="sxs-lookup"><span data-stu-id="90016-119">Sales tax ledger posting groups V2</span></span> | <span data-ttu-id="90016-120">msdyn_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="90016-120">msdyn_taxpostinggroups</span></span> |
<span data-ttu-id="90016-121">Quellensteuercodes</span><span class="sxs-lookup"><span data-stu-id="90016-121">Withholding tax codes</span></span> | <span data-ttu-id="90016-122">msdyn_withholdingtaxcodes</span><span class="sxs-lookup"><span data-stu-id="90016-122">msdyn_withholdingtaxcodes</span></span> |
<span data-ttu-id="90016-123">Quellensteuergruppen</span><span class="sxs-lookup"><span data-stu-id="90016-123">Withholding tax groups</span></span> | <span data-ttu-id="90016-124">msdyn_withholdingtaxgroups</span><span class="sxs-lookup"><span data-stu-id="90016-124">msdyn_withholdingtaxgroups</span></span> | 


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]