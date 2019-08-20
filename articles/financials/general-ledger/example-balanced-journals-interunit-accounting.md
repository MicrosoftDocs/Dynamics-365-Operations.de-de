---
title: Ausgeglichene Erfassungen für einheitenübergreifende Buchhaltung
description: Dieser Artikel zeigt, wie eine Erfassung automatisch ausgeglichen wird, wenn eine ausgleichende Finanzdimension auf der Sachkontoseite ausgewählt ist.
author: ShylaThompson
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e84d96b5467b38e07a9ed31f142c27b638289284
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839352"
---
# <a name="balanced-journals-for-interunit-accounting"></a><span data-ttu-id="a324e-103">Ausgeglichene Erfassungen für einheitenübergreifende Buchhaltung</span><span class="sxs-lookup"><span data-stu-id="a324e-103">Balanced journals for interunit accounting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a324e-104">Dieser Artikel zeigt, wie eine Erfassung automatisch ausgeglichen wird, wenn eine ausgleichende Finanzdimension auf der Sachkontoseite ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="a324e-104">This article shows how a journal is automatically balanced when a balancing financial dimension is selected on the Ledger page.</span></span> 

<span data-ttu-id="a324e-105">Wenn Buchhaltungseinträge nicht auf der Ebene der Finanzdimensionswerte ausgeglichen sind, werden zusätzliche Kontoeinträge automatisch erstellt, um die Erfassung auszugleichen.</span><span class="sxs-lookup"><span data-stu-id="a324e-105">If account entries don't balance at the level of the financial dimension values, additional account entries are created automatically to balance the journal.</span></span> <span data-ttu-id="a324e-106">Diese Kontoeinträge verwenden **Einheitenbezogen - Soll**- und **Einheitenbezogen - Haben**-Buchungstypen auf der Seite **Konten für automatische Buchungen**, um das Hauptkonto zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="a324e-106">These account entries use the **Interunit - debit** and **Interunit - credit** posting types on the **Accounts for automatic transactions** page to determine the main account.</span></span> <span data-ttu-id="a324e-107">Beispielsweise wird Geschäftseinheit, die das zweite Segment des Sachkontos darstellt, als Ausgleichsfinanzdimension ausgewählt, und die folgenden Buchhaltungseinträge werden anschließend erstellt.</span><span class="sxs-lookup"><span data-stu-id="a324e-107">For example, Business Unit, which is the second segment of the ledger account, is selected as the balancing financial dimension, and the following accounting entries are about to be created.</span></span>

|                      |           |
|----------------------|-----------|
| <span data-ttu-id="a324e-108">6100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="a324e-108">6100 – MSP – OU\_256</span></span> | <span data-ttu-id="a324e-109">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="a324e-109">100.00 DR</span></span> |
| <span data-ttu-id="a324e-110">6100 – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="a324e-110">6100 – NY – OU\_249</span></span>  | <span data-ttu-id="a324e-111">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="a324e-111">100.00 DR</span></span> |
| <span data-ttu-id="a324e-112">2100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="a324e-112">2100 – MSP – OU\_256</span></span> | <span data-ttu-id="a324e-113">200,00 CR</span><span class="sxs-lookup"><span data-stu-id="a324e-113">200.00 CR</span></span> |

<span data-ttu-id="a324e-114">In diesem Fall werden die folgenden Salden bestimmt:</span><span class="sxs-lookup"><span data-stu-id="a324e-114">In this case, the following balances are determined:</span></span>

-   <span data-ttu-id="a324e-115">Für Geschäftseinheit MSP = 100,00 CR</span><span class="sxs-lookup"><span data-stu-id="a324e-115">For Business Unit MSP = 100.00 CR</span></span>
-   <span data-ttu-id="a324e-116">Für Geschäftseinheit NY = 100,00 DR</span><span class="sxs-lookup"><span data-stu-id="a324e-116">For Business Unit NY = 100.00 DR</span></span>

<span data-ttu-id="a324e-117">Die folgenden Buchhaltungseinträge werden daher automatisch erstellt, damit die Erfassung auf der Ebene der Finanzdimensionswerte ausgeglichen ist.</span><span class="sxs-lookup"><span data-stu-id="a324e-117">Therefore, the following accounting entries are created automatically to balance the  journal at the level of the financial dimension values.</span></span>

|                                   |           |
|-----------------------------------|-----------|
| <span data-ttu-id="a324e-118">(Einheitenbezogen Soll) – MSP  – OU\_256</span><span class="sxs-lookup"><span data-stu-id="a324e-118">(Interunit Debit) – MSP – OU\_256</span></span> | <span data-ttu-id="a324e-119">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="a324e-119">100.00 DR</span></span> |
| <span data-ttu-id="a324e-120">(Einheitenbezogen Haben) – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="a324e-120">(Interunit Credit) – NY – OU\_249</span></span> | <span data-ttu-id="a324e-121">100,00 CR</span><span class="sxs-lookup"><span data-stu-id="a324e-121">100.00 CR</span></span> |





