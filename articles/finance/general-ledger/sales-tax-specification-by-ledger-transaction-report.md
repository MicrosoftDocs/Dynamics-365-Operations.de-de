---
title: Bericht „Mehrwertsteuerspezifikation nach Sachkontobuchungen“
description: In diesem Thema wird erläutert, wie der Bericht „Mehrwertsteuerspezifikation nachSachkontobuchungsbericht“ verwendet wird, um Informationen zu Sachkontobuchungen anzuzeigen und zu drucken, für die Mehrwertsteuer berechnet wird.
author: ericwang
manager: Ann Beebe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2019-08-19
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 1c36d9f8fb81a0a7e7a6de3db48cebdcf9d13b2d
ms.sourcegitcommit: bdbca89bd9b328c282ebfb681f75b8f1ed96e7a8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/14/2019
ms.locfileid: "2591193"
---
# <a name="sales-tax-specification-by-ledger-transaction-report"></a><span data-ttu-id="352f6-103">Bericht „Mehrwertsteuerspezifikation nach Sachkontobuchungen“</span><span class="sxs-lookup"><span data-stu-id="352f6-103">Sales tax specification by ledger transaction report</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="352f6-104">In diesem Thema wird erläutert, wie die **Mehrwertsteuerspezifikation nachSachkontobuchungsbericht** verwendet wird, um Informationen zu Sachkontobuchungen anzuzeigen und zu drucken, für die Mehrwertsteuer berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="352f6-104">This topic explains how to use the **Sales tax specification by ledger transaction** report to view and print information about ledger transactions that sales tax is calculated for.</span></span>

## <a name="tax-accounts-vs-non-tax-accounts"></a><span data-ttu-id="352f6-105">Steuerkonto für Nicht-Steuerkonten</span><span class="sxs-lookup"><span data-stu-id="352f6-105">Tax accounts vs. non-tax accounts</span></span>

<span data-ttu-id="352f6-106">Der Bericht **Mehrwertsteuerspezifikation nach Sachkontobuchungen** enthält Steuerbuchungen für Steuerkonten und Nicht-Steuerkonten.</span><span class="sxs-lookup"><span data-stu-id="352f6-106">The **Sales tax specification by ledger transaction** report shows tax transactions for both tax accounts and non-tax accounts.</span></span> <span data-ttu-id="352f6-107">Diese Konten werden folgendermaßen kategorisiert:</span><span class="sxs-lookup"><span data-stu-id="352f6-107">These accounts are categorized in the following way:</span></span>

- <span data-ttu-id="352f6-108">**Steuerkonto** – Es wird ein Konto als ein Steuerkonto angesehen, wenn eine Steuerbuchung gebucht wird, und das Hauptkonto in der Erfassungsposition **Mehrwertsteuer** ein Steuerkonto ist, wie z. B. ein Konto für Mehrwertsteuer oder Vorsteuer.</span><span class="sxs-lookup"><span data-stu-id="352f6-108">**Tax account** – An account is considered a tax account when a tax transaction is posted, and the main account on the **Sales Tax** journal line is a tax account, such as a sales tax payable account or a sales tax receivable account.</span></span>
- <span data-ttu-id="352f6-109">**Nicht-Steuerkonto** – Es wird ein Konto als ein Nicht-Steuerkonto angesehen, wenn eine Steuerbuchung gebucht wird, und das Hauptkonto in der ursprünglichen Transaktion ein Nicht-Steuerkonto ist, wie z. B. ein Konto für Umsatzerlös oder Ausgaben.</span><span class="sxs-lookup"><span data-stu-id="352f6-109">**Non-tax account** – An account is considered a non-tax account when a tax transaction is posted, and the main account on the original transaction is a non-tax account, such as a revenue account or an expense account.</span></span>

<span data-ttu-id="352f6-110">Für Steuerkonten zeigen die Spalten **Buchungsgrundlage**, **Vorsteuer** und **Mehrwertsteuer** im Bericht **0** (null) an.</span><span class="sxs-lookup"><span data-stu-id="352f6-110">For tax accounts, the **Origin**, **Sales tax receivable**, and **Sales tax payable** columns on the report show **0** (zero).</span></span> <span data-ttu-id="352f6-111">Für Nicht-Steuerkonten zeigen die Spalten Beträge an.</span><span class="sxs-lookup"><span data-stu-id="352f6-111">For non-tax accounts, those columns show amounts.</span></span>

## <a name="filtering-the-data-on-the-report"></a><span data-ttu-id="352f6-112">Filtern der Daten im Bericht</span><span class="sxs-lookup"><span data-stu-id="352f6-112">Filtering the data on the report</span></span>

<span data-ttu-id="352f6-113">Wenn dieser Bericht generiert wird, werden die folgenden Felder verfügbar.</span><span class="sxs-lookup"><span data-stu-id="352f6-113">When you generate the report, the following default fields are available.</span></span> <span data-ttu-id="352f6-114">Sie können mithilfe dieser Felder die Daten filtern, die im Bericht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="352f6-114">You can use these fields to filter the data that is shown on the report.</span></span>

| <span data-ttu-id="352f6-115">Feld</span><span class="sxs-lookup"><span data-stu-id="352f6-115">Field</span></span>                      | <span data-ttu-id="352f6-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="352f6-116">Description</span></span> |
|----------------------------|-------------|
| <span data-ttu-id="352f6-117">Datum</span><span class="sxs-lookup"><span data-stu-id="352f6-117">Date</span></span>                       | <span data-ttu-id="352f6-118">Verwenden Sie die Felder in den Abschnitten **Von** und **Bis**, um für die Steuerbuchungen einen Datumsbereich zu definieren.</span><span class="sxs-lookup"><span data-stu-id="352f6-118">Use the fields in the **From** and **To** sections to define a date range for the tax transactions.</span></span> |
| <span data-ttu-id="352f6-119">Hauptkonto</span><span class="sxs-lookup"><span data-stu-id="352f6-119">Main account</span></span>               | <span data-ttu-id="352f6-120">Verwenden Sie die Felder in den Abschnitten **Von** und **Bis**, um für die Hauptkonten einen Bereich zu definieren.</span><span class="sxs-lookup"><span data-stu-id="352f6-120">Use the fields in the **From** and **To** sections to define a range of main accounts.</span></span> |
| <span data-ttu-id="352f6-121">Mehrwertsteuercode</span><span class="sxs-lookup"><span data-stu-id="352f6-121">Sales tax code</span></span>             | <span data-ttu-id="352f6-122">Verwenden Sie die Felder in den Abschnitten **Von** und **Bis**, um einen Bereich von Mehrwertsteuercodes zu definieren.</span><span class="sxs-lookup"><span data-stu-id="352f6-122">Use the fields in the **From** and **To** sections to define a range of sales tax codes.</span></span> |
| <span data-ttu-id="352f6-123">Gruppieren</span><span class="sxs-lookup"><span data-stu-id="352f6-123">Grouping</span></span>                   | <span data-ttu-id="352f6-124">Wählen Sie aus, ob der Bericht nach Sachkonto oder Mehrwertsteuercode gruppiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="352f6-124">Select whether the report should be grouped by ledger account or sales tax code.</span></span> |
| <span data-ttu-id="352f6-125">Zwischensumme nach Mehrwertsteuercode</span><span class="sxs-lookup"><span data-stu-id="352f6-125">Subtotal by sales tax code</span></span> | <span data-ttu-id="352f6-126">Legen Sie diese Option auf **Ja** fest, um Zwischensummen nach Mehrwertsteuercode anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="352f6-126">Set this option to **Yes** to show subtotals by sales tax code.</span></span> |
| <span data-ttu-id="352f6-127">Nur Summen</span><span class="sxs-lookup"><span data-stu-id="352f6-127">Totals only</span></span>                | <span data-ttu-id="352f6-128">Legen Sie diese Option auf **Ja** fest, um nur Summen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="352f6-128">Set this option to **Yes** to show only totals.</span></span> |
| <span data-ttu-id="352f6-129">Nur Hauptkonten</span><span class="sxs-lookup"><span data-stu-id="352f6-129">Main accounts only</span></span>         | <span data-ttu-id="352f6-130">Legen Sie diese Option auf **Ja** fest, um nur Hauptkonten im Bericht einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="352f6-130">Set this option to **Yes** to include only main accounts on the report.</span></span> |

## <a name="showing-only-non-tax-accounts-on-the-report"></a><span data-ttu-id="352f6-131">Ausschließliches Anzeigen von Nicht-Steuerkonten im Bericht</span><span class="sxs-lookup"><span data-stu-id="352f6-131">Showing only non-tax accounts on the report</span></span>

<span data-ttu-id="352f6-132">Um nur Nicht-Steuerkonten im Bericht anzuzeigen, richten Sie eine Filterbedingung ein, wie z. B. Sternchen (\*), wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="352f6-132">To show only non-tax accounts on the report, set up a filter condition, such as an asterisk (\*), as shown in the following illustration.</span></span>

![Bericht mit Nicht-Steuerkonten](media/taxspecperledgertrans.png)
