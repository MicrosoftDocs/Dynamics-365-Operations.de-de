---
title: Ausgeglichene Erfassungen für einheitenübergreifende Buchhaltung
description: Dieser Artikel zeigt, wie eine Erfassung automatisch ausgeglichen wird, wenn eine ausgleichende Finanzdimension auf der Sachkontoseite ausgewählt ist.
author: ShylaThompson
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: roschlom
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a5a926adcc631ec286f37796713466eb0144494c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818391"
---
# <a name="balanced-journals-for-interunit-accounting"></a><span data-ttu-id="c7c93-103">Ausgeglichene Erfassungen für einheitenübergreifende Buchhaltung</span><span class="sxs-lookup"><span data-stu-id="c7c93-103">Balanced journals for interunit accounting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c7c93-104">Dieser Artikel zeigt, wie eine Erfassung automatisch ausgeglichen wird, wenn eine ausgleichende Finanzdimension auf der Sachkontoseite ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="c7c93-104">This article shows how a journal is automatically balanced when a balancing financial dimension is selected on the Ledger page.</span></span> 

<span data-ttu-id="c7c93-105">Wenn Buchhaltungseinträge nicht auf der Ebene der Finanzdimensionswerte ausgeglichen sind, werden zusätzliche Kontoeinträge automatisch erstellt, um die Erfassung auszugleichen.</span><span class="sxs-lookup"><span data-stu-id="c7c93-105">If account entries don't balance at the level of the financial dimension values, additional account entries are created automatically to balance the journal.</span></span> <span data-ttu-id="c7c93-106">Diese Kontoeinträge verwenden **Einheitenbezogen - Soll**- und **Einheitenbezogen - Haben**-Buchungstypen auf der Seite **Konten für automatische Buchungen**, um das Hauptkonto zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="c7c93-106">These account entries use the **Interunit - debit** and **Interunit - credit** posting types on the **Accounts for automatic transactions** page to determine the main account.</span></span> <span data-ttu-id="c7c93-107">Beispielsweise wird Geschäftseinheit, die das zweite Segment des Sachkontos darstellt, als Ausgleichsfinanzdimension ausgewählt, und die folgenden Buchhaltungseinträge werden anschließend erstellt.</span><span class="sxs-lookup"><span data-stu-id="c7c93-107">For example, Business Unit, which is the second segment of the ledger account, is selected as the balancing financial dimension, and the following accounting entries are about to be created.</span></span>

| &nbsp;               | &nbsp;    |
|----------------------|-----------|
| <span data-ttu-id="c7c93-108">6100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="c7c93-108">6100 – MSP – OU\_256</span></span> | <span data-ttu-id="c7c93-109">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="c7c93-109">100.00 DR</span></span> |
| <span data-ttu-id="c7c93-110">6100 – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="c7c93-110">6100 – NY – OU\_249</span></span>  | <span data-ttu-id="c7c93-111">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="c7c93-111">100.00 DR</span></span> |
| <span data-ttu-id="c7c93-112">2100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="c7c93-112">2100 – MSP – OU\_256</span></span> | <span data-ttu-id="c7c93-113">200,00 CR</span><span class="sxs-lookup"><span data-stu-id="c7c93-113">200.00 CR</span></span> |

<span data-ttu-id="c7c93-114">In diesem Fall werden die folgenden Salden bestimmt:</span><span class="sxs-lookup"><span data-stu-id="c7c93-114">In this case, the following balances are determined:</span></span>

-   <span data-ttu-id="c7c93-115">Für Geschäftseinheit MSP = 100,00 CR</span><span class="sxs-lookup"><span data-stu-id="c7c93-115">For Business Unit MSP = 100.00 CR</span></span>
-   <span data-ttu-id="c7c93-116">Für Geschäftseinheit NY = 100,00 DR</span><span class="sxs-lookup"><span data-stu-id="c7c93-116">For Business Unit NY = 100.00 DR</span></span>

<span data-ttu-id="c7c93-117">Die folgenden Buchhaltungseinträge werden daher automatisch erstellt, damit die Erfassung auf der Ebene der Finanzdimensionswerte ausgeglichen ist.</span><span class="sxs-lookup"><span data-stu-id="c7c93-117">Therefore, the following accounting entries are created automatically to balance the  journal at the level of the financial dimension values.</span></span>

| &nbsp;                            | &nbsp;    |
|-----------------------------------|-----------|
| <span data-ttu-id="c7c93-118">(Einheitenbezogen Soll) – MSP  – OU\_256</span><span class="sxs-lookup"><span data-stu-id="c7c93-118">(Interunit Debit) – MSP – OU\_256</span></span> | <span data-ttu-id="c7c93-119">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="c7c93-119">100.00 DR</span></span> |
| <span data-ttu-id="c7c93-120">(Einheitenbezogen Haben) – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="c7c93-120">(Interunit Credit) – NY – OU\_249</span></span> | <span data-ttu-id="c7c93-121">100,00 CR</span><span class="sxs-lookup"><span data-stu-id="c7c93-121">100.00 CR</span></span> |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]