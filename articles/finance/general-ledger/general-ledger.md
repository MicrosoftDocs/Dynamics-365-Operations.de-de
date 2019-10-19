---
title: Hauptbuch und Finanzberichterstellung-Übersicht
description: Verwenden Sie das Hauptbuch zum Verwalten der Finanzdatensätze der juristischen Person.
author: ShylaThompson
manager: AnnBe
ms.date: 08/31/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GeneralJournalEntryWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 65431
ms.assetid: d2c604df-daae-42cd-82d9-c80e3dee4a60
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c0e795e641314b4ef81f8972aadf597721995fcc
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186531"
---
# <a name="general-ledger-overview"></a><span data-ttu-id="7ad46-103">Hauptbuch – Übersicht</span><span class="sxs-lookup"><span data-stu-id="7ad46-103">General ledger overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7ad46-104">Verwenden Sie das Hauptbuch zum Verwalten der Finanzdatensätze der juristischen Person.</span><span class="sxs-lookup"><span data-stu-id="7ad46-104">Use General ledger to define and manage the legal entity’s financial records.</span></span> <span data-ttu-id="7ad46-105">Das Hauptbuch ist ein Register von Soll- und Habenbuchungen.</span><span class="sxs-lookup"><span data-stu-id="7ad46-105">The general ledger is a register of debit and credit entries.</span></span> <span data-ttu-id="7ad46-106">Diese Einträge werden anhand der in einem Kontenplan aufgeführten Konten klassifiziert.</span><span class="sxs-lookup"><span data-stu-id="7ad46-106">These entries are classified using the accounts that are listed in a chart of accounts.</span></span> 

 - [<span data-ttu-id="7ad46-107">Ihren Kontenplan planen</span><span class="sxs-lookup"><span data-stu-id="7ad46-107">Plan your chart of accounts</span></span>](plan-chart-of-accounts.md)
 - [<span data-ttu-id="7ad46-108">Hauptkontotypen</span><span class="sxs-lookup"><span data-stu-id="7ad46-108">Main account types</span></span>](main-account-types.md)

<span data-ttu-id="7ad46-109">Sie können Geldbeträge auf Grundlage von Zuordnungsregeln einem oder mehreren Konten oder einer Kombination von Konten und Dimensionen zuteilen bzw. verteilen.</span><span class="sxs-lookup"><span data-stu-id="7ad46-109">You can allocate, or distribute, monetary amounts to one or more accounts or account and dimension combinations based on allocation rules.</span></span> <span data-ttu-id="7ad46-110">Zur Verfügung stehen zwei Arten von Zuteilungen: fest und variabel.</span><span class="sxs-lookup"><span data-stu-id="7ad46-110">There are two types of allocations: fixed and variable.</span></span> <span data-ttu-id="7ad46-111">Sie können auch Buchungen zwischen Sachkonten ausgleichen und Währungsbeträge neu bewerten.</span><span class="sxs-lookup"><span data-stu-id="7ad46-111">You can also settle transactions between ledger accounts and revalue currency amounts.</span></span> <span data-ttu-id="7ad46-112">Am Ende eines Geschäftsjahrs müssen Sie Abschlussbuchungen generieren und die Konten für das nächste Geschäftsjahr vorbereiten.</span><span class="sxs-lookup"><span data-stu-id="7ad46-112">At the end of a fiscal year, you must generate closing transactions and prepare your accounts for the next fiscal year.</span></span> <span data-ttu-id="7ad46-113">Sie können die Konsolidierungsfunktion verwenden, um die finanziellen Ergebnisse mehrerer juristischer Personen vom Typ Tochtergesellschaft in Ergebnissen für nur eine konsolidierte Organisation zusammenzufassen.</span><span class="sxs-lookup"><span data-stu-id="7ad46-113">You can use the consolidation functionality to combine the financial results for several subsidiary legal entities into results for a single, consolidated organization.</span></span> <span data-ttu-id="7ad46-114">Die Tochtergesellschaften können sich in der gleichen Datenbank oder in anderen Datenbanken befinden.</span><span class="sxs-lookup"><span data-stu-id="7ad46-114">The subsidiaries can be in the same database or in separate databases.</span></span>

- [<span data-ttu-id="7ad46-115">Konsolidierungs- und Löschungsüberblick</span><span class="sxs-lookup"><span data-stu-id="7ad46-115">Consolidation and elimination overview</span></span>](../budgeting/consolidation-elimination-overview.md)
- [<span data-ttu-id="7ad46-116">Kontosalden für das Hauptbuch</span><span class="sxs-lookup"><span data-stu-id="7ad46-116">General ledger account balances</span></span>](general-ledger-account-balances.md)
- [<span data-ttu-id="7ad46-117">Finanzdimensionen</span><span class="sxs-lookup"><span data-stu-id="7ad46-117">Financial dimensions</span></span>](financial-dimensions.md)

<span data-ttu-id="7ad46-118">[![Geschäftsprozess](./media/GL-process.PNG)](./media/GL-process.PNG)</span><span class="sxs-lookup"><span data-stu-id="7ad46-118">[![Business process](./media/GL-process.PNG)](./media/GL-process.PNG)</span></span>

## <a name="sales-tax"></a><span data-ttu-id="7ad46-119">Mehrwertsteuer</span><span class="sxs-lookup"><span data-stu-id="7ad46-119">Sales tax</span></span>
<span data-ttu-id="7ad46-120">Jedes Unternehmen erfasst und zahlt Steuern an verschiedene Steuerbehörden.</span><span class="sxs-lookup"><span data-stu-id="7ad46-120">Every company collects and pays taxes to various tax authorities.</span></span> <span data-ttu-id="7ad46-121">Die Regeln und Sätze unterscheiden sich je nach Land/Region, Bundesland, Landkreis und Ort.</span><span class="sxs-lookup"><span data-stu-id="7ad46-121">The rules and rates vary by country/region, state, county, and city.</span></span>
<span data-ttu-id="7ad46-122">Zudem müssen sie in regelmäßigen Abständen aktualisiert werden, wenn Steuerbehörden die Anforderungen ändern.</span><span class="sxs-lookup"><span data-stu-id="7ad46-122">In addition, the rules must be updated periodically when tax authorities change their requirements.</span></span> <span data-ttu-id="7ad46-123">Mehrwertsteuercodes enthalten die grundlegenden Informationen zum abzuführenden Steuerbetrag.</span><span class="sxs-lookup"><span data-stu-id="7ad46-123">Sales tax codes contain the basic information about how much you collect and pay to the authorities.</span></span> <span data-ttu-id="7ad46-124">Beim Einrichten von Mehrwertsteuercodes definieren Sie die zu erfassenden Beträge oder Prozentsätze.</span><span class="sxs-lookup"><span data-stu-id="7ad46-124">When you set up sales tax codes, you define the amounts or percentages that must be collected.</span></span> <span data-ttu-id="7ad46-125">Sie legen außerdem die unterschiedlichen Methoden zur Anwendung der Beträge oder Prozentsätze auf Buchungsbeträge fest.</span><span class="sxs-lookup"><span data-stu-id="7ad46-125">You also define the various methods by which those amounts or percentages are applied to transaction amounts.</span></span> <span data-ttu-id="7ad46-126">Die Themen dieses Abschnitts enthalten Informationen zum Einrichten von Mehrwertsteuercodes für die von den Steuerbehörden geforderten Methoden und Sätze.</span><span class="sxs-lookup"><span data-stu-id="7ad46-126">The topics in this section provide information about how to set up sales tax codes for the methods and rates that your tax authorities require.</span></span>

 - [<span data-ttu-id="7ad46-127">Mehrwertsteuerüberblick</span><span class="sxs-lookup"><span data-stu-id="7ad46-127">Sales tax overview</span></span>](indirect-taxes-overview.md)
 - [<span data-ttu-id="7ad46-128">Mehrwertsteuersteuersätze auf Grundlage der Felder Berechnungsgrundlage und Berechnungsmethode</span><span class="sxs-lookup"><span data-stu-id="7ad46-128">Sales tax rates based on the Marginal base and Calculation methods</span></span>](marginal-base-field.md)
 - [<span data-ttu-id="7ad46-129">Mehrwertsteuerzahlungen und Rundungsregeln</span><span class="sxs-lookup"><span data-stu-id="7ad46-129">Sales tax payments and rounding rules</span></span>](round-sales-tax-payments.md)


## <a name="additional-resources"></a><span data-ttu-id="7ad46-130">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7ad46-130">Additional resources</span></span>

#### <a name="whats-new-and-in-development"></a><span data-ttu-id="7ad46-131">Neuigkeiten und Entwicklungen</span><span class="sxs-lookup"><span data-stu-id="7ad46-131">What's new and in development</span></span>

<span data-ttu-id="7ad46-132">Wechseln Sie zu [Microsoft Dynamics 365 Versionshinweise](https://go.microsoft.com/fwlink/?linkid=2010158), um festzustellen, welche der neuen Funktionalität geplant sind.</span><span class="sxs-lookup"><span data-stu-id="7ad46-132">Go to the [Microsoft Dynamics 365 Release Notes](https://go.microsoft.com/fwlink/?linkid=2010158) to see what new features have been planned.</span></span> 

#### <a name="blogs"></a><span data-ttu-id="7ad46-133">Blogs</span><span class="sxs-lookup"><span data-stu-id="7ad46-133">Blogs</span></span>

<span data-ttu-id="7ad46-134">Meinungen, Neuigkeiten und weitere Informationen finden Sie im [Microsoft Dynamics 365-Blog](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise) und im [Microsoft Dynamics 365 Finance and Operations - Finanzblog](https://community.dynamics.com/365/financeandoperations/b/financials).</span><span class="sxs-lookup"><span data-stu-id="7ad46-134">You can find opinions, news, and other information on the [Microsoft Dynamics 365 blog](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise) and the [Microsoft Dynamics 365 Finance and Operations - Financials blog](https://community.dynamics.com/365/financeandoperations/b/financials).</span></span>

<span data-ttu-id="7ad46-135">Der [Microsoft Dynamics Operations-Partner-Community-Blog](https://community.dynamics.com/partner/b/operationspartnercommunityblog) fasst alle Informationen zu Neuigkeiten und Trends bei MBS Operations für Microsoft Dynamics-Partner in einer einzigen Ressource zusammen.</span><span class="sxs-lookup"><span data-stu-id="7ad46-135">The [Microsoft Dynamics Operations Partner Community Blog](https://community.dynamics.com/partner/b/operationspartnercommunityblog) gives Microsoft Dynamics Partners a single resource where they can learn what is new and trending in MBS Operations.</span></span>

### <a name="videos"></a><span data-ttu-id="7ad46-136">Videos</span><span class="sxs-lookup"><span data-stu-id="7ad46-136">Videos</span></span>

<span data-ttu-id="7ad46-137">Sehen Sie in den Videos nach, die jetzt im [YouTube-Kanal zu Microsoft Dynamics 365](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ) verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="7ad46-137">Check out the how-to videos that are now available on the [Microsoft Dynamics 365 YouTube Channel](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ).</span></span>

#### <a name="community-blogs"></a><span data-ttu-id="7ad46-138">Communityblogs</span><span class="sxs-lookup"><span data-stu-id="7ad46-138">Community blogs</span></span>

- [<span data-ttu-id="7ad46-139">Was Sie zum Sachkonto in Dynamics 365 for Finance and Operations wissen sollten</span><span class="sxs-lookup"><span data-stu-id="7ad46-139">What you should know about ledger in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/04/29/what-you-should-know-about-ledger-in-dynamics-365-for-finance-and-operations)

