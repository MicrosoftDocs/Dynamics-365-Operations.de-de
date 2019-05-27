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
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5b596a2332a9ada01df7b4e718a79eb624ee52fc
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549103"
---
# <a name="balanced-journals-for-interunit-accounting"></a><span data-ttu-id="de534-103">Ausgeglichene Erfassungen für einheitenübergreifende Buchhaltung</span><span class="sxs-lookup"><span data-stu-id="de534-103">Balanced journals for interunit accounting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="de534-104">Dieser Artikel zeigt, wie eine Erfassung automatisch ausgeglichen wird, wenn eine ausgleichende Finanzdimension auf der Sachkontoseite ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="de534-104">This article shows how a journal is automatically balanced when a balancing financial dimension is selected on the Ledger page.</span></span> 

<span data-ttu-id="de534-105">Wenn Buchhaltungseinträge nicht auf der Ebene der Finanzdimensionswerte ausgeglichen sind, werden zusätzliche Kontoeinträge automatisch erstellt, um die Erfassung auszugleichen.</span><span class="sxs-lookup"><span data-stu-id="de534-105">If account entries don't balance at the level of the financial dimension values, additional account entries are created automatically to balance the journal.</span></span> <span data-ttu-id="de534-106">Diese Kontoeinträge verwenden **Einheitenbezogen - Soll**- und **Einheitenbezogen - Haben**-Buchungstypen auf der Seite **Konten für automatische Buchungen**, um das Hauptkonto zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="de534-106">These account entries use the **Interunit - debit** and **Interunit - credit** posting types on the **Accounts for automatic transactions** page to determine the main account.</span></span> <span data-ttu-id="de534-107">Beispielsweise wird Geschäftseinheit, die das zweite Segment des Sachkontos darstellt, als Ausgleichsfinanzdimension ausgewählt, und die folgenden Buchhaltungseinträge werden anschließend erstellt.</span><span class="sxs-lookup"><span data-stu-id="de534-107">For example, Business Unit, which is the second segment of the ledger account, is selected as the balancing financial dimension, and the following accounting entries are about to be created.</span></span>

|                      |           |
|----------------------|-----------|
| <span data-ttu-id="de534-108">6100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="de534-108">6100 – MSP – OU\_256</span></span> | <span data-ttu-id="de534-109">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="de534-109">100.00 DR</span></span> |
| <span data-ttu-id="de534-110">6100 – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="de534-110">6100 – NY – OU\_249</span></span>  | <span data-ttu-id="de534-111">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="de534-111">100.00 DR</span></span> |
| <span data-ttu-id="de534-112">2100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="de534-112">2100 – MSP – OU\_256</span></span> | <span data-ttu-id="de534-113">200,00 CR</span><span class="sxs-lookup"><span data-stu-id="de534-113">200.00 CR</span></span> |

<span data-ttu-id="de534-114">In diesem Fall werden die folgenden Salden bestimmt:</span><span class="sxs-lookup"><span data-stu-id="de534-114">In this case, the following balances are determined:</span></span>

-   <span data-ttu-id="de534-115">Für Geschäftseinheit MSP = 100,00 CR</span><span class="sxs-lookup"><span data-stu-id="de534-115">For Business Unit MSP = 100.00 CR</span></span>
-   <span data-ttu-id="de534-116">Für Geschäftseinheit NY = 100,00 DR</span><span class="sxs-lookup"><span data-stu-id="de534-116">For Business Unit NY = 100.00 DR</span></span>

<span data-ttu-id="de534-117">Die folgenden Buchhaltungseinträge werden daher automatisch erstellt, damit die Erfassung auf der Ebene der Finanzdimensionswerte ausgeglichen ist.</span><span class="sxs-lookup"><span data-stu-id="de534-117">Therefore, the following accounting entries are created automatically to balance the  journal at the level of the financial dimension values.</span></span>

|                                   |           |
|-----------------------------------|-----------|
| <span data-ttu-id="de534-118">(Einheitenbezogen Soll) – MSP  – OU\_256</span><span class="sxs-lookup"><span data-stu-id="de534-118">(Interunit Debit) – MSP – OU\_256</span></span> | <span data-ttu-id="de534-119">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="de534-119">100.00 DR</span></span> |
| <span data-ttu-id="de534-120">(Einheitenbezogen Haben) – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="de534-120">(Interunit Credit) – NY – OU\_249</span></span> | <span data-ttu-id="de534-121">100,00 CR</span><span class="sxs-lookup"><span data-stu-id="de534-121">100.00 CR</span></span> |





