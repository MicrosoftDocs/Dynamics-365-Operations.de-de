---
title: Integriertes Sachkonto
description: In diesem Thema wird die Integration von Sachkontodaten zwischen Finance and Operations und anderen Dynamics 365-Anwendungen mithilfe von Dataverse beschrieben.
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
ms.openlocfilehash: f794d8306a3a752d811d7d84c0ed5f739f423cad
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681641"
---
# <a name="integrated-ledger"></a><span data-ttu-id="159ee-103">Integriertes Sachkonto</span><span class="sxs-lookup"><span data-stu-id="159ee-103">Integrated ledger</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="159ee-104">In einer Geschäftsanwendung definieren Sachkontodaten den Kern der Geschäftsabläufe eines Unternehmens.</span><span class="sxs-lookup"><span data-stu-id="159ee-104">In a business application, ledger data defines the core set up for how a company does business.</span></span> <span data-ttu-id="159ee-105">Sachkontodaten beschreiben beispielsweise das Geschäftsjahr, in dem das Unternehmen tätig ist, die Währungen, in denen es handelt, und die Konten, die es verwendet.</span><span class="sxs-lookup"><span data-stu-id="159ee-105">For example, ledger data describes the fiscal year the company follows, the currencies it transacts in, and the accounts it uses.</span></span> <span data-ttu-id="159ee-106">In diesem Thema wird die Integration dieser Finanzkennzahlen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="159ee-106">This topic describes the integration of this core financial data.</span></span>

## <a name="templates"></a><span data-ttu-id="159ee-107">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="159ee-107">Templates</span></span>

<span data-ttu-id="159ee-108">Sachkontodaten enthalten eine Sammlung von wichtigen Tabellenzuordnungen, die während der Dateninteraktion zusammenarbeiten, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="159ee-108">Ledger data includes a collection of core financial table maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="159ee-109">Finance and Operations Apps</span><span class="sxs-lookup"><span data-stu-id="159ee-109">Finance and Operations apps</span></span>      | <span data-ttu-id="159ee-110">Modellgesteuerte App in Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="159ee-110">Model-driven app in Dynamics 365</span></span> | <span data-ttu-id="159ee-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="159ee-111">Description</span></span>
---------------------------------|----------------------------------|------------
<span data-ttu-id="159ee-112">Währungen</span><span class="sxs-lookup"><span data-stu-id="159ee-112">Currencies</span></span>                       | <span data-ttu-id="159ee-113">transactioncurrencies</span><span class="sxs-lookup"><span data-stu-id="159ee-113">transactioncurrencies</span></span>            |
<span data-ttu-id="159ee-114">FiscalCalendar</span><span class="sxs-lookup"><span data-stu-id="159ee-114">FiscalCalendar</span></span>                   | <span data-ttu-id="159ee-115">msdyn\_fiscalcalendars</span><span class="sxs-lookup"><span data-stu-id="159ee-115">msdyn\_fiscalcalendars</span></span>        |
<span data-ttu-id="159ee-116">FiscalCalendarYear</span><span class="sxs-lookup"><span data-stu-id="159ee-116">FiscalCalendarYear</span></span>               | <span data-ttu-id="159ee-117">msdyn\_fiscalcalendaryears</span><span class="sxs-lookup"><span data-stu-id="159ee-117">msdyn\_fiscalcalendaryears</span></span>        |
<span data-ttu-id="159ee-118">ExchRateType</span><span class="sxs-lookup"><span data-stu-id="159ee-118">ExchRateType</span></span>                     | <span data-ttu-id="159ee-119">msdyn\_exchangeratetypes</span><span class="sxs-lookup"><span data-stu-id="159ee-119">msdyn\_exchangeratetypes</span></span>        |
<span data-ttu-id="159ee-120">ExchangeRateCurrencyPair</span><span class="sxs-lookup"><span data-stu-id="159ee-120">ExchangeRateCurrencyPair</span></span>         | <span data-ttu-id="159ee-121">msdyn\_currencyexchangeratepairs</span><span class="sxs-lookup"><span data-stu-id="159ee-121">msdyn\_currencyexchangeratepairs</span></span>        |
<span data-ttu-id="159ee-122">FiscalPeriodEntity</span><span class="sxs-lookup"><span data-stu-id="159ee-122">FiscalPeriodEntity</span></span>               | <span data-ttu-id="159ee-123">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="159ee-123">msdyn\_fiscalcalendarperiods</span></span>        |
<span data-ttu-id="159ee-124">MainAccountCategory</span><span class="sxs-lookup"><span data-stu-id="159ee-124">MainAccountCategory</span></span>              | <span data-ttu-id="159ee-125">msdyn\_mainaccountcategory</span><span class="sxs-lookup"><span data-stu-id="159ee-125">msdyn\_mainaccountcategory</span></span>        |
<span data-ttu-id="159ee-126">MainAccount</span><span class="sxs-lookup"><span data-stu-id="159ee-126">MainAccount</span></span>                      | <span data-ttu-id="159ee-127">msdyn\_mainaccounts</span><span class="sxs-lookup"><span data-stu-id="159ee-127">msdyn\_mainaccounts</span></span>        |
<span data-ttu-id="159ee-128">Unternehmen</span><span class="sxs-lookup"><span data-stu-id="159ee-128">Ledger</span></span>                           | <span data-ttu-id="159ee-129">msdyn\_ledgers</span><span class="sxs-lookup"><span data-stu-id="159ee-129">msdyn\_ledgers</span></span>        |
<span data-ttu-id="159ee-130">ExchangeRates</span><span class="sxs-lookup"><span data-stu-id="159ee-130">ExchangeRates</span></span>                    | <span data-ttu-id="159ee-131">msdyn\_currencyexchangerates</span><span class="sxs-lookup"><span data-stu-id="159ee-131">msdyn\_currencyexchangerates</span></span>        |
<span data-ttu-id="159ee-132">FinancialCalendarPeriod</span><span class="sxs-lookup"><span data-stu-id="159ee-132">FinancialCalendarPeriod</span></span>          | <span data-ttu-id="159ee-133">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="159ee-133">msdyn\_fiscalcalendarperiods</span></span>        |
<span data-ttu-id="159ee-134">DimensionAttributeEntity</span><span class="sxs-lookup"><span data-stu-id="159ee-134">DimensionAttributeEntity</span></span>         | <span data-ttu-id="159ee-135">msdyn\_dimensionattributes</span><span class="sxs-lookup"><span data-stu-id="159ee-135">msdyn\_dimensionattributes</span></span>        |
<span data-ttu-id="159ee-136">DimensionIntegrationFormatEntity</span><span class="sxs-lookup"><span data-stu-id="159ee-136">DimensionIntegrationFormatEntity</span></span> | <span data-ttu-id="159ee-137">msdyn\_financialdimensionformats</span><span class="sxs-lookup"><span data-stu-id="159ee-137">msdyn\_financialdimensionformats</span></span>        |
<span data-ttu-id="159ee-138">LedgerChartOfAccounts</span><span class="sxs-lookup"><span data-stu-id="159ee-138">LedgerChartOfAccounts</span></span>            | <span data-ttu-id="159ee-139">msdyn\_chartofaccounts</span><span class="sxs-lookup"><span data-stu-id="159ee-139">msdyn\_chartofaccounts</span></span>        |


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Currency](includes/Currencies-transactioncurrencies.md)]

[!include [Fiscal calendar](includes/FiscalCalendar-msdyn-fiscalcalendars.md)]

[!include [Fiscal calendar year](includes/FiscalCalendarYear-msdyn-fiscalcalendaryears.md)]

[!include [Exchange rate types](includes/ExchRateType-msdyn-exchangeratetypes.md)]

[!include [Exchange rate pair](includes/ExchangeRateCurrencyPair-msdyn-currencyexchangeratepairs.md)]

[!include [Main account category](includes/MainAccountCategory-msdyn-mainaccountcategory.md)]

[!include [Main account](includes/MainAccount-msdyn-mainaccounts.md)]

[!include [Ledger](includes/Ledger-msdyn-ledgers.md)]

[!include [Exchange rates](includes/ExchangeRates-msdyn-currencyexchangerates.md)]

[!include [Financial Calendar Period](includes/FiscalPeriodEntity-msdyn-fiscalcalendarperiods.md)]

[!include [Dimension attribute](includes/DimensionAttributeEntity-msdyn-dimensionattributes.md)]

[!include [Dimension integration format](includes/DimensionIntegrationFormatEntity-msdyn-financialdimensionformats.md)]

[!include [Chart Of Account](includes/LedgerChartOfAccounts-msdyn-chartofaccounts.md)]




