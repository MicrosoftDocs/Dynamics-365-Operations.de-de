---
title: Hauptbuch und Finanzberichterstellung-Startseite
description: "Verwenden Sie das Hauptbuch zum Verwalten der Finanzdatensätze der juristischen Person. Das Hauptbuch ist ein Register von Soll- und Habenbuchungen. Diese Einträge werden anhand der in einem Kontenplan aufgeführten Konten klassifiziert."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 65431
ms.assetid: d2c604df-daae-42cd-82d9-c80e3dee4a60
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 78f3d9c27767c089ac686f333cae3cb50c03ee18
ms.contentlocale: de-de
ms.lasthandoff: 07/18/2017

---

# <a name="general-ledger"></a><span data-ttu-id="b8dfc-105">Hauptbuch</span><span class="sxs-lookup"><span data-stu-id="b8dfc-105">General ledger</span></span> 

[!include[banner](../includes/banner.md)]


<span data-ttu-id="b8dfc-106">Verwenden Sie das Hauptbuch zum Verwalten der Finanzdatensätze der juristischen Person.</span><span class="sxs-lookup"><span data-stu-id="b8dfc-106">Use General ledger to define and manage the legal entity’s financial records.</span></span> <span data-ttu-id="b8dfc-107">Das Hauptbuch ist ein Register von Soll- und Habenbuchungen.</span><span class="sxs-lookup"><span data-stu-id="b8dfc-107">The general ledger is a register of debit and credit entries.</span></span> <span data-ttu-id="b8dfc-108">Diese Einträge werden anhand der in einem Kontenplan aufgeführten Konten klassifiziert.</span><span class="sxs-lookup"><span data-stu-id="b8dfc-108">These entries are classified using the accounts that are listed in a chart of accounts.</span></span> 

<span data-ttu-id="b8dfc-109">Sie können Geldbeträge auf Grundlage von Zuordnungsregeln einem oder mehreren Konten oder einer Kombination von Konten und Dimensionen zuteilen bzw. verteilen.</span><span class="sxs-lookup"><span data-stu-id="b8dfc-109">You can allocate, or distribute, monetary amounts to one or more accounts or account and dimension combinations based on allocation rules.</span></span> <span data-ttu-id="b8dfc-110">Zur Verfügung stehen zwei Arten von Zuteilungen: fest und variabel.</span><span class="sxs-lookup"><span data-stu-id="b8dfc-110">There are two types of allocations: fixed and variable.</span></span> <span data-ttu-id="b8dfc-111">Sie können auch Buchungen zwischen Sachkonten ausgleichen und Währungsbeträge neu bewerten.</span><span class="sxs-lookup"><span data-stu-id="b8dfc-111">You can also settle transactions between ledger accounts and revalue currency amounts.</span></span> <span data-ttu-id="b8dfc-112">Am Ende eines Geschäftsjahrs müssen Sie Abschlussbuchungen generieren und die Konten für das nächste Geschäftsjahr vorbereiten.</span><span class="sxs-lookup"><span data-stu-id="b8dfc-112">At the end of a fiscal year, you must generate closing transactions and prepare your accounts for the next fiscal year.</span></span> <span data-ttu-id="b8dfc-113">Sie können die Konsolidierungsfunktion verwenden, um die finanziellen Ergebnisse mehrerer juristischer Personen vom Typ Tochtergesellschaft in Ergebnissen für nur eine konsolidierte Organisation zusammenzufassen.</span><span class="sxs-lookup"><span data-stu-id="b8dfc-113">You can use the consolidation functionality to combine the financial results for several subsidiary legal entities into results for a single, consolidated organization.</span></span> <span data-ttu-id="b8dfc-114">Die Tochtergesellschaften können sich in der gleichen Microsoft Dynamics 365 for Finance and Operations-Datenbank oder in anderen Datenbanken befinden.</span><span class="sxs-lookup"><span data-stu-id="b8dfc-114">The subsidiaries can be in the same Microsoft Dynamics 365 for Finance and Operations database or in separate databases.</span></span>

# <a name="sales-tax"></a><span data-ttu-id="b8dfc-115">Mehrwertsteuer</span><span class="sxs-lookup"><span data-stu-id="b8dfc-115">Sales tax</span></span>
<span data-ttu-id="b8dfc-116">Jedes Unternehmen erfasst und zahlt Steuern an verschiedene Steuerbehörden.</span><span class="sxs-lookup"><span data-stu-id="b8dfc-116">Every company collects and pays taxes to various tax authorities.</span></span> <span data-ttu-id="b8dfc-117">Die Regeln und Sätze unterscheiden sich je nach Land/Region, Bundesland, Landkreis und Ort.</span><span class="sxs-lookup"><span data-stu-id="b8dfc-117">The rules and rates vary by country/region, state, county, and city.</span></span> <span data-ttu-id="b8dfc-118">Zudem müssen sie in regelmäßigen Abständen aktualisiert werden, wenn Steuerbehörden die Anforderungen ändern.</span><span class="sxs-lookup"><span data-stu-id="b8dfc-118">In addition, the rules must be updated periodically when tax authorities change their requirements.</span></span> <span data-ttu-id="b8dfc-119">Mehrwertsteuercodes enthalten die grundlegenden Informationen zum abzuführenden Steuerbetrag.</span><span class="sxs-lookup"><span data-stu-id="b8dfc-119">Sales tax codes contain the basic information about how much you collect and pay to the authorities.</span></span> <span data-ttu-id="b8dfc-120">Beim Einrichten von Mehrwertsteuercodes definieren Sie die zu erfassenden Beträge oder Prozentsätze.</span><span class="sxs-lookup"><span data-stu-id="b8dfc-120">When you set up sales tax codes, you define the amounts or percentages that must be collected.</span></span> <span data-ttu-id="b8dfc-121">Sie legen außerdem die unterschiedlichen Methoden zur Anwendung der Beträge oder Prozentsätze auf Buchungsbeträge fest.</span><span class="sxs-lookup"><span data-stu-id="b8dfc-121">You also define the various methods by which those amounts or percentages are applied to transaction amounts.</span></span> <span data-ttu-id="b8dfc-122">Die Themen dieses Abschnitts enthalten Informationen zum Einrichten von Mehrwertsteuercodes für die von den Steuerbehörden geforderten Methoden und Sätze.</span><span class="sxs-lookup"><span data-stu-id="b8dfc-122">The topics in this section provide information about how to set up sales tax codes for the methods and rates that your tax authorities require.</span></span>







