---
title: Integriertes Sachkonto
description: In diesem Thema wird die Integration von Sachkontodaten zwischen Finance and Operations und anderen Dynamics 365-Anwendungen mithilfe von Dataverse beschrieben.
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
ms.openlocfilehash: f8095b0a755e40e5665d951d33ea4ce60e749165
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567695"
---
# <a name="integrated-ledger"></a><span data-ttu-id="b0b74-103">Integriertes Sachkonto</span><span class="sxs-lookup"><span data-stu-id="b0b74-103">Integrated ledger</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="b0b74-104">In einer Geschäftsanwendung definieren Sachkontodaten den Kern der Geschäftsabläufe eines Unternehmens.</span><span class="sxs-lookup"><span data-stu-id="b0b74-104">In a business application, ledger data defines the core set up for how a company does business.</span></span> <span data-ttu-id="b0b74-105">Sachkontodaten beschreiben beispielsweise das Geschäftsjahr, in dem das Unternehmen tätig ist, die Währungen, in denen es handelt, und die Konten, die es verwendet.</span><span class="sxs-lookup"><span data-stu-id="b0b74-105">For example, ledger data describes the fiscal year the company follows, the currencies it transacts in, and the accounts it uses.</span></span> <span data-ttu-id="b0b74-106">In diesem Thema wird die Integration dieser Finanzkennzahlen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b0b74-106">This topic describes the integration of this core financial data.</span></span>

## <a name="templates"></a><span data-ttu-id="b0b74-107">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="b0b74-107">Templates</span></span>

<span data-ttu-id="b0b74-108">Sachkontodaten enthalten eine Sammlung von wichtigen Tabellenzuordnungen, die während der Dateninteraktion zusammenarbeiten, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b0b74-108">Ledger data includes a collection of core financial table maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="b0b74-109">Finance and Operations Apps</span><span class="sxs-lookup"><span data-stu-id="b0b74-109">Finance and Operations apps</span></span>      | <span data-ttu-id="b0b74-110">Modellgesteuerte App in Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="b0b74-110">Model-driven app in Dynamics 365</span></span> | <span data-ttu-id="b0b74-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b0b74-111">Description</span></span>
---------------------------------|----------------------------------|------------
<span data-ttu-id="b0b74-112">Währungen</span><span class="sxs-lookup"><span data-stu-id="b0b74-112">Currencies</span></span>                       | <span data-ttu-id="b0b74-113">transactioncurrencies</span><span class="sxs-lookup"><span data-stu-id="b0b74-113">transactioncurrencies</span></span>            |
<span data-ttu-id="b0b74-114">FiscalCalendar</span><span class="sxs-lookup"><span data-stu-id="b0b74-114">FiscalCalendar</span></span>                   | <span data-ttu-id="b0b74-115">msdyn\_fiscalcalendars</span><span class="sxs-lookup"><span data-stu-id="b0b74-115">msdyn\_fiscalcalendars</span></span>        |
<span data-ttu-id="b0b74-116">FiscalCalendarYear</span><span class="sxs-lookup"><span data-stu-id="b0b74-116">FiscalCalendarYear</span></span>               | <span data-ttu-id="b0b74-117">msdyn\_fiscalcalendaryears</span><span class="sxs-lookup"><span data-stu-id="b0b74-117">msdyn\_fiscalcalendaryears</span></span>        |
<span data-ttu-id="b0b74-118">ExchRateType</span><span class="sxs-lookup"><span data-stu-id="b0b74-118">ExchRateType</span></span>                     | <span data-ttu-id="b0b74-119">msdyn\_exchangeratetypes</span><span class="sxs-lookup"><span data-stu-id="b0b74-119">msdyn\_exchangeratetypes</span></span>        |
<span data-ttu-id="b0b74-120">ExchangeRateCurrencyPair</span><span class="sxs-lookup"><span data-stu-id="b0b74-120">ExchangeRateCurrencyPair</span></span>         | <span data-ttu-id="b0b74-121">msdyn\_currencyexchangeratepairs</span><span class="sxs-lookup"><span data-stu-id="b0b74-121">msdyn\_currencyexchangeratepairs</span></span>        |
<span data-ttu-id="b0b74-122">FiscalPeriodEntity</span><span class="sxs-lookup"><span data-stu-id="b0b74-122">FiscalPeriodEntity</span></span>               | <span data-ttu-id="b0b74-123">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="b0b74-123">msdyn\_fiscalcalendarperiods</span></span>        |
<span data-ttu-id="b0b74-124">MainAccountCategory</span><span class="sxs-lookup"><span data-stu-id="b0b74-124">MainAccountCategory</span></span>              | <span data-ttu-id="b0b74-125">msdyn\_mainaccountcategory</span><span class="sxs-lookup"><span data-stu-id="b0b74-125">msdyn\_mainaccountcategory</span></span>        |
<span data-ttu-id="b0b74-126">MainAccount</span><span class="sxs-lookup"><span data-stu-id="b0b74-126">MainAccount</span></span>                      | <span data-ttu-id="b0b74-127">msdyn\_mainaccounts</span><span class="sxs-lookup"><span data-stu-id="b0b74-127">msdyn\_mainaccounts</span></span>        |
<span data-ttu-id="b0b74-128">Unternehmen</span><span class="sxs-lookup"><span data-stu-id="b0b74-128">Ledger</span></span>                           | <span data-ttu-id="b0b74-129">msdyn\_ledgers</span><span class="sxs-lookup"><span data-stu-id="b0b74-129">msdyn\_ledgers</span></span>        |
<span data-ttu-id="b0b74-130">ExchangeRates</span><span class="sxs-lookup"><span data-stu-id="b0b74-130">ExchangeRates</span></span>                    | <span data-ttu-id="b0b74-131">msdyn\_currencyexchangerates</span><span class="sxs-lookup"><span data-stu-id="b0b74-131">msdyn\_currencyexchangerates</span></span>        |
<span data-ttu-id="b0b74-132">FinancialCalendarPeriod</span><span class="sxs-lookup"><span data-stu-id="b0b74-132">FinancialCalendarPeriod</span></span>          | <span data-ttu-id="b0b74-133">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="b0b74-133">msdyn\_fiscalcalendarperiods</span></span>        |
<span data-ttu-id="b0b74-134">DimensionAttributeEntity</span><span class="sxs-lookup"><span data-stu-id="b0b74-134">DimensionAttributeEntity</span></span>         | <span data-ttu-id="b0b74-135">msdyn\_dimensionattributes</span><span class="sxs-lookup"><span data-stu-id="b0b74-135">msdyn\_dimensionattributes</span></span>        |
<span data-ttu-id="b0b74-136">DimensionIntegrationFormatEntity</span><span class="sxs-lookup"><span data-stu-id="b0b74-136">DimensionIntegrationFormatEntity</span></span> | <span data-ttu-id="b0b74-137">msdyn\_financialdimensionformats</span><span class="sxs-lookup"><span data-stu-id="b0b74-137">msdyn\_financialdimensionformats</span></span>        |
<span data-ttu-id="b0b74-138">LedgerChartOfAccounts</span><span class="sxs-lookup"><span data-stu-id="b0b74-138">LedgerChartOfAccounts</span></span>            | <span data-ttu-id="b0b74-139">msdyn\_chartofaccounts</span><span class="sxs-lookup"><span data-stu-id="b0b74-139">msdyn\_chartofaccounts</span></span>        |


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






[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]