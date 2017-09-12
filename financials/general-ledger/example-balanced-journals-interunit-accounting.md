---
title: "Ausgeglichene Erfassungen für einheitenübergreifende Buchhaltung"
description: "Dieser Artikel zeigt, wie eine Erfassung automatisch ausgeglichen wird, wenn eine ausgleichende Finanzdimension auf der Sachkontoseite ausgewählt ist."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: f45d180dc8dcafb0579e76b890dd5d516df5b8c0
ms.contentlocale: de-de
ms.lasthandoff: 06/29/2017


---

# <a name="balanced-journals-for-interunit-accounting"></a><span data-ttu-id="38f19-103">Ausgeglichene Erfassungen für einheitenübergreifende Buchhaltung</span><span class="sxs-lookup"><span data-stu-id="38f19-103">Balanced journals for interunit accounting</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="38f19-104">Dieser Artikel zeigt, wie eine Erfassung automatisch ausgeglichen wird, wenn eine ausgleichende Finanzdimension auf der Sachkontoseite ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="38f19-104">This article shows how a journal is automatically balanced when a balancing financial dimension is selected on the Ledger page.</span></span> 

<span data-ttu-id="38f19-105">Wenn Buchhaltungseinträge nicht auf der Ebene der Finanzdimensionswerte ausgeglichen sind, werden zusätzliche Kontoeinträge automatisch erstellt, um die Erfassung auszugleichen.</span><span class="sxs-lookup"><span data-stu-id="38f19-105">If account entries don't balance at the level of the financial dimension values, additional account entries are created automatically to balance the journal.</span></span> <span data-ttu-id="38f19-106">Diese Kontoeinträge verwenden **Einheitenbezogen - Soll**- und **Einheitenbezogen - Haben**-Buchungstypen auf der Seite **Konten für automatische Buchungen**, um das Hauptkonto zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="38f19-106">These account entries use the **Interunit - debit** and **Interunit - credit** posting types on the **Accounts for automatic transactions** page to determine the main account.</span></span> <span data-ttu-id="38f19-107">Beispielsweise wird Verzweigung, die das zweite Segment des Sachkontos darstellt, als Ausgleichsfinanzdimension ausgewählt, und die folgenden Buchhaltungseinträge werden anschließend erstellt.</span><span class="sxs-lookup"><span data-stu-id="38f19-107">For example, Branch, which is the second segment of the ledger account, is selected as the balancing financial dimension, and the following accounting entries are about to be created.</span></span>

|                      |           |
|----------------------|-----------|
| <span data-ttu-id="38f19-108">6100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="38f19-108">6100 – MSP – OU\_256</span></span> | <span data-ttu-id="38f19-109">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="38f19-109">100.00 DR</span></span> |
| <span data-ttu-id="38f19-110">6100 – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="38f19-110">6100 – NY – OU\_249</span></span>  | <span data-ttu-id="38f19-111">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="38f19-111">100.00 DR</span></span> |
| <span data-ttu-id="38f19-112">2100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="38f19-112">2100 – MSP – OU\_256</span></span> | <span data-ttu-id="38f19-113">200,00 CR</span><span class="sxs-lookup"><span data-stu-id="38f19-113">200.00 CR</span></span> |

<span data-ttu-id="38f19-114">In diesem Fall werden die folgenden Salden bestimmt:</span><span class="sxs-lookup"><span data-stu-id="38f19-114">In this case, the following balances are determined:</span></span>

-   <span data-ttu-id="38f19-115">Für Verzweigung MSP = 100.00 HABEN</span><span class="sxs-lookup"><span data-stu-id="38f19-115">For Branch MSP = 100.00 CR</span></span>
-   <span data-ttu-id="38f19-116">Für Verzweigung NY = 100.00 SOLL</span><span class="sxs-lookup"><span data-stu-id="38f19-116">For Branch NY = 100.00 DR</span></span>

<span data-ttu-id="38f19-117">Die folgenden Buchhaltungseinträge werden daher automatisch erstellt, damit die Erfassung auf der Ebene der Finanzdimensionswerte ausgeglichen ist.</span><span class="sxs-lookup"><span data-stu-id="38f19-117">Therefore, the following accounting entries are created automatically to balance the  journal at the level of the financial dimension values.</span></span>

|                                   |           |
|-----------------------------------|-----------|
| <span data-ttu-id="38f19-118">(Einheitenbezogen Soll) – MSP  – OU\_256</span><span class="sxs-lookup"><span data-stu-id="38f19-118">(Interunit Debit) – MSP – OU\_256</span></span> | <span data-ttu-id="38f19-119">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="38f19-119">100.00 DR</span></span> |
| <span data-ttu-id="38f19-120">(Einheitenbezogen Haben) – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="38f19-120">(Interunit Credit) – NY – OU\_249</span></span> | <span data-ttu-id="38f19-121">100,00 CR</span><span class="sxs-lookup"><span data-stu-id="38f19-121">100.00 CR</span></span> |






