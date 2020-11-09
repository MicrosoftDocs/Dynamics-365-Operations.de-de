---
title: Integriertes Sachkonto
description: In diesem Thema wird die Integration von Sachkontodaten zwischen Finance and Operations und anderen Dynamics 365-Anwendungen mithilfe von Common Data Service beschrieben.
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
ms.openlocfilehash: 7f5435a97776b817a4b99887cbab8283de25b692
ms.sourcegitcommit: 49f3011b8a6d8cdd038e153d8cb3cf773be25ae4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4014857"
---
# <a name="integrated-ledger"></a><span data-ttu-id="eccda-103">Integriertes Sachkonto</span><span class="sxs-lookup"><span data-stu-id="eccda-103">Integrated ledger</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="eccda-104">In einer Geschäftsanwendung definieren Sachkontodaten den Kern der Geschäftsabläufe eines Unternehmens.</span><span class="sxs-lookup"><span data-stu-id="eccda-104">In a business application, ledger data defines the core set up for how a company does business.</span></span> <span data-ttu-id="eccda-105">Sachkontodaten beschreiben beispielsweise das Geschäftsjahr, in dem das Unternehmen tätig ist, die Währungen, in denen es handelt, und die Konten, die es verwendet.</span><span class="sxs-lookup"><span data-stu-id="eccda-105">For example, ledger data describes the fiscal year the company follows, the currencies it transacts in, and the accounts it uses.</span></span> <span data-ttu-id="eccda-106">In diesem Thema wird die Integration dieser Finanzkennzahlen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="eccda-106">This topic describes the integration of this core financial data.</span></span>

## <a name="templates"></a><span data-ttu-id="eccda-107">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="eccda-107">Templates</span></span>

<span data-ttu-id="eccda-108">Sachkontodaten enthalten eine Sammlung von wichtigen Finanzentitätszuordnungen, die während der Dateninteraktion zusammenarbeiten, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="eccda-108">Ledger data includes a collection of core financial entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="eccda-109">Finance and Operations Apps</span><span class="sxs-lookup"><span data-stu-id="eccda-109">Finance and Operations apps</span></span>      | <span data-ttu-id="eccda-110">Modellgesteuerte App in Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="eccda-110">Model-driven app in Dynamics 365</span></span> | <span data-ttu-id="eccda-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eccda-111">Description</span></span>
---------------------------------|----------------------------------|------------
<span data-ttu-id="eccda-112">Währungen</span><span class="sxs-lookup"><span data-stu-id="eccda-112">Currencies</span></span>                       | <span data-ttu-id="eccda-113">transactioncurrencies</span><span class="sxs-lookup"><span data-stu-id="eccda-113">transactioncurrencies</span></span>            |
<span data-ttu-id="eccda-114">FiscalCalendar</span><span class="sxs-lookup"><span data-stu-id="eccda-114">FiscalCalendar</span></span>                   | <span data-ttu-id="eccda-115">msdyn\_fiscalcalendars</span><span class="sxs-lookup"><span data-stu-id="eccda-115">msdyn\_fiscalcalendars</span></span>        |
<span data-ttu-id="eccda-116">FiscalCalendarYear</span><span class="sxs-lookup"><span data-stu-id="eccda-116">FiscalCalendarYear</span></span>               | <span data-ttu-id="eccda-117">msdyn\_fiscalcalendaryears</span><span class="sxs-lookup"><span data-stu-id="eccda-117">msdyn\_fiscalcalendaryears</span></span>        |
<span data-ttu-id="eccda-118">ExchRateType</span><span class="sxs-lookup"><span data-stu-id="eccda-118">ExchRateType</span></span>                     | <span data-ttu-id="eccda-119">msdyn\_exchangeratetypes</span><span class="sxs-lookup"><span data-stu-id="eccda-119">msdyn\_exchangeratetypes</span></span>        |
<span data-ttu-id="eccda-120">ExchangeRateCurrencyPair</span><span class="sxs-lookup"><span data-stu-id="eccda-120">ExchangeRateCurrencyPair</span></span>         | <span data-ttu-id="eccda-121">msdyn\_currencyexchangeratepairs</span><span class="sxs-lookup"><span data-stu-id="eccda-121">msdyn\_currencyexchangeratepairs</span></span>        |
<span data-ttu-id="eccda-122">FiscalPeriodEntity</span><span class="sxs-lookup"><span data-stu-id="eccda-122">FiscalPeriodEntity</span></span>               | <span data-ttu-id="eccda-123">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="eccda-123">msdyn\_fiscalcalendarperiods</span></span>        |
<span data-ttu-id="eccda-124">MainAccountCategory</span><span class="sxs-lookup"><span data-stu-id="eccda-124">MainAccountCategory</span></span>              | <span data-ttu-id="eccda-125">msdyn\_mainaccountcategory</span><span class="sxs-lookup"><span data-stu-id="eccda-125">msdyn\_mainaccountcategory</span></span>        |
<span data-ttu-id="eccda-126">MainAccount</span><span class="sxs-lookup"><span data-stu-id="eccda-126">MainAccount</span></span>                      | <span data-ttu-id="eccda-127">msdyn\_mainaccounts</span><span class="sxs-lookup"><span data-stu-id="eccda-127">msdyn\_mainaccounts</span></span>        |
<span data-ttu-id="eccda-128">Unternehmen</span><span class="sxs-lookup"><span data-stu-id="eccda-128">Ledger</span></span>                           | <span data-ttu-id="eccda-129">msdyn\_ledgers</span><span class="sxs-lookup"><span data-stu-id="eccda-129">msdyn\_ledgers</span></span>        |
<span data-ttu-id="eccda-130">ExchangeRates</span><span class="sxs-lookup"><span data-stu-id="eccda-130">ExchangeRates</span></span>                    | <span data-ttu-id="eccda-131">msdyn\_currencyexchangerates</span><span class="sxs-lookup"><span data-stu-id="eccda-131">msdyn\_currencyexchangerates</span></span>        |
<span data-ttu-id="eccda-132">FinancialCalendarPeriod</span><span class="sxs-lookup"><span data-stu-id="eccda-132">FinancialCalendarPeriod</span></span>          | <span data-ttu-id="eccda-133">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="eccda-133">msdyn\_fiscalcalendarperiods</span></span>        |
<span data-ttu-id="eccda-134">DimensionAttributeEntity</span><span class="sxs-lookup"><span data-stu-id="eccda-134">DimensionAttributeEntity</span></span>         | <span data-ttu-id="eccda-135">msdyn\_dimensionattributes</span><span class="sxs-lookup"><span data-stu-id="eccda-135">msdyn\_dimensionattributes</span></span>        |
<span data-ttu-id="eccda-136">DimensionIntegrationFormatEntity</span><span class="sxs-lookup"><span data-stu-id="eccda-136">DimensionIntegrationFormatEntity</span></span> | <span data-ttu-id="eccda-137">msdyn\_financialdimensionformats</span><span class="sxs-lookup"><span data-stu-id="eccda-137">msdyn\_financialdimensionformats</span></span>        |
<span data-ttu-id="eccda-138">LedgerChartOfAccounts</span><span class="sxs-lookup"><span data-stu-id="eccda-138">LedgerChartOfAccounts</span></span>            | <span data-ttu-id="eccda-139">msdyn\_chartofaccounts</span><span class="sxs-lookup"><span data-stu-id="eccda-139">msdyn\_chartofaccounts</span></span>        |


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




