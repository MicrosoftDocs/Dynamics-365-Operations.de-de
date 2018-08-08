---
title: Hauptbuch und Finanzberichterstellung-Startseite
description: "Verwenden Sie das Hauptbuch zum Verwalten der Finanzdatensätze der juristischen Person."
author: ShylaThompson
manager: AnnBe
ms.date: 08/31/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: GeneralJournalEntryWorkspace
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 65431
ms.assetid: d2c604df-daae-42cd-82d9-c80e3dee4a60
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 85afebcc88ad1c087d5f1dabaac56f694534cf98
ms.contentlocale: de-de
ms.lasthandoff: 08/07/2018

---

# <a name="general-ledger"></a><span data-ttu-id="462a5-103">Hauptbuch</span><span class="sxs-lookup"><span data-stu-id="462a5-103">General ledger</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="462a5-104">Verwenden Sie das Hauptbuch zum Verwalten der Finanzdatensätze der juristischen Person.</span><span class="sxs-lookup"><span data-stu-id="462a5-104">Use General ledger to define and manage the legal entity’s financial records.</span></span> <span data-ttu-id="462a5-105">Das Hauptbuch ist ein Register von Soll- und Habenbuchungen.</span><span class="sxs-lookup"><span data-stu-id="462a5-105">The general ledger is a register of debit and credit entries.</span></span> <span data-ttu-id="462a5-106">Diese Einträge werden anhand der in einem Kontenplan aufgeführten Konten klassifiziert.</span><span class="sxs-lookup"><span data-stu-id="462a5-106">These entries are classified using the accounts that are listed in a chart of accounts.</span></span> 

 - [<span data-ttu-id="462a5-107">Ihren Kontenplan planen</span><span class="sxs-lookup"><span data-stu-id="462a5-107">Plan your chart of accounts</span></span>](plan-chart-of-accounts.md)
 - [<span data-ttu-id="462a5-108">Hauptkontotypen</span><span class="sxs-lookup"><span data-stu-id="462a5-108">Main account types</span></span>](main-account-types.md)

<span data-ttu-id="462a5-109">Sie können Geldbeträge auf Grundlage von Zuordnungsregeln einem oder mehreren Konten oder einer Kombination von Konten und Dimensionen zuteilen bzw. verteilen.</span><span class="sxs-lookup"><span data-stu-id="462a5-109">You can allocate, or distribute, monetary amounts to one or more accounts or account and dimension combinations based on allocation rules.</span></span> <span data-ttu-id="462a5-110">Zur Verfügung stehen zwei Arten von Zuteilungen: fest und variabel.</span><span class="sxs-lookup"><span data-stu-id="462a5-110">There are two types of allocations: fixed and variable.</span></span> <span data-ttu-id="462a5-111">Sie können auch Buchungen zwischen Sachkonten ausgleichen und Währungsbeträge neu bewerten.</span><span class="sxs-lookup"><span data-stu-id="462a5-111">You can also settle transactions between ledger accounts and revalue currency amounts.</span></span> <span data-ttu-id="462a5-112">Am Ende eines Geschäftsjahrs müssen Sie Abschlussbuchungen generieren und die Konten für das nächste Geschäftsjahr vorbereiten.</span><span class="sxs-lookup"><span data-stu-id="462a5-112">At the end of a fiscal year, you must generate closing transactions and prepare your accounts for the next fiscal year.</span></span> <span data-ttu-id="462a5-113">Sie können die Konsolidierungsfunktion verwenden, um die finanziellen Ergebnisse mehrerer juristischer Personen vom Typ Tochtergesellschaft in Ergebnissen für nur eine konsolidierte Organisation zusammenzufassen.</span><span class="sxs-lookup"><span data-stu-id="462a5-113">You can use the consolidation functionality to combine the financial results for several subsidiary legal entities into results for a single, consolidated organization.</span></span> <span data-ttu-id="462a5-114">Die Tochtergesellschaften können sich in der gleichen Microsoft Dynamics 365 for Finance and Operations-Datenbank oder in anderen Datenbanken befinden.</span><span class="sxs-lookup"><span data-stu-id="462a5-114">The subsidiaries can be in the same Microsoft Dynamics 365 for Finance and Operations database or in separate databases.</span></span>

- [<span data-ttu-id="462a5-115">Konsolidierungs- und Löschungsüberblick</span><span class="sxs-lookup"><span data-stu-id="462a5-115">Consolidation and elimination overview</span></span>](../budgeting/consolidation-elimination-overview.md)
- [<span data-ttu-id="462a5-116">Kontosalden für das Hauptbuch</span><span class="sxs-lookup"><span data-stu-id="462a5-116">General ledger account balances</span></span>](general-ledger-account-balances.md)
- [<span data-ttu-id="462a5-117">Finanzdimensionen</span><span class="sxs-lookup"><span data-stu-id="462a5-117">Financial dimensions</span></span>](financial-dimensions.md)

<span data-ttu-id="462a5-118">[![Geschäftsprozess](./media/GL-process.PNG)](./media/GL-process.PNG)</span><span class="sxs-lookup"><span data-stu-id="462a5-118">[![Business process](./media/GL-process.PNG)](./media/GL-process.PNG)</span></span>

## <a name="sales-tax"></a><span data-ttu-id="462a5-119">Mehrwertsteuer</span><span class="sxs-lookup"><span data-stu-id="462a5-119">Sales tax</span></span>
<span data-ttu-id="462a5-120">Jedes Unternehmen erfasst und zahlt Steuern an verschiedene Steuerbehörden.</span><span class="sxs-lookup"><span data-stu-id="462a5-120">Every company collects and pays taxes to various tax authorities.</span></span> <span data-ttu-id="462a5-121">Die Regeln und Sätze unterscheiden sich je nach Land/Region, Bundesland, Landkreis und Ort.</span><span class="sxs-lookup"><span data-stu-id="462a5-121">The rules and rates vary by country/region, state, county, and city.</span></span>
<span data-ttu-id="462a5-122">Zudem müssen sie in regelmäßigen Abständen aktualisiert werden, wenn Steuerbehörden die Anforderungen ändern.</span><span class="sxs-lookup"><span data-stu-id="462a5-122">In addition, the rules must be updated periodically when tax authorities change their requirements.</span></span> <span data-ttu-id="462a5-123">Mehrwertsteuercodes enthalten die grundlegenden Informationen zum abzuführenden Steuerbetrag.</span><span class="sxs-lookup"><span data-stu-id="462a5-123">Sales tax codes contain the basic information about how much you collect and pay to the authorities.</span></span> <span data-ttu-id="462a5-124">Beim Einrichten von Mehrwertsteuercodes definieren Sie die zu erfassenden Beträge oder Prozentsätze.</span><span class="sxs-lookup"><span data-stu-id="462a5-124">When you set up sales tax codes, you define the amounts or percentages that must be collected.</span></span> <span data-ttu-id="462a5-125">Sie legen außerdem die unterschiedlichen Methoden zur Anwendung der Beträge oder Prozentsätze auf Buchungsbeträge fest.</span><span class="sxs-lookup"><span data-stu-id="462a5-125">You also define the various methods by which those amounts or percentages are applied to transaction amounts.</span></span> <span data-ttu-id="462a5-126">Die Themen dieses Abschnitts enthalten Informationen zum Einrichten von Mehrwertsteuercodes für die von den Steuerbehörden geforderten Methoden und Sätze.</span><span class="sxs-lookup"><span data-stu-id="462a5-126">The topics in this section provide information about how to set up sales tax codes for the methods and rates that your tax authorities require.</span></span>

 - [<span data-ttu-id="462a5-127">Mehrwertsteuerüberblick</span><span class="sxs-lookup"><span data-stu-id="462a5-127">Sales tax overview</span></span>](indirect-taxes-overview.md)
 - [<span data-ttu-id="462a5-128">Mehrwertsteuersteuersätze auf Grundlage der Felder Berechnungsgrundlage und Berechnungsmethode</span><span class="sxs-lookup"><span data-stu-id="462a5-128">Sales tax rates based on the Marginal base and Calculation methods</span></span>](marginal-base-field.md)
 - [<span data-ttu-id="462a5-129">Mehrwertsteuerzahlungen und Rundungsregeln</span><span class="sxs-lookup"><span data-stu-id="462a5-129">Sales tax payments and rounding rules</span></span>](round-sales-tax-payments.md)


## <a name="additional-resources"></a><span data-ttu-id="462a5-130">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="462a5-130">Additional resources</span></span>

### <a name="whats-new"></a><span data-ttu-id="462a5-131">Neuigkeiten</span><span class="sxs-lookup"><span data-stu-id="462a5-131">What's new</span></span>

<span data-ttu-id="462a5-132">Wechseln Sie zu [Versionshinweise](https://docs.microsoft.com/en-us/business-applications-release-notes/), um festzustellen, welche der neuen Funktionalität freigegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="462a5-132">Go to the [Release notes](https://docs.microsoft.com/en-us/business-applications-release-notes/) to see what new features have been released.</span></span> 

### <a name="videos"></a><span data-ttu-id="462a5-133">Videos</span><span class="sxs-lookup"><span data-stu-id="462a5-133">Videos</span></span>

<span data-ttu-id="462a5-134">Sehen Sie in den Videos zu Hilfe + Anleitungen nach, die jetzt im [YouTube-Kanal zu Microsoft Dynamics 365](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ) verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="462a5-134">Check out the how-to videos that are now available on the [Microsoft Dynamics 365 YouTube Channel](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ).</span></span>

### <a name="blogs"></a><span data-ttu-id="462a5-135">Blogs</span><span class="sxs-lookup"><span data-stu-id="462a5-135">Blogs</span></span>

<span data-ttu-id="462a5-136">Meinungen, Neuigkeiten und weitere Informationen zu Kreditorenkonten und anderen Lösungen finden Sie im [Microsoft Dynamics 365-Blog](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise).</span><span class="sxs-lookup"><span data-stu-id="462a5-136">You can find opinions, news, and other information about Accounts payable and other solutions on the [Microsoft Dynamics 365 blog](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise).</span></span>

<span data-ttu-id="462a5-137">Im [Microsoft Dynamics AX-Produktteamblog](https://blogs.msdn.microsoft.com/dax/) finden Sie viele Beiträge zum Hauptbuch.</span><span class="sxs-lookup"><span data-stu-id="462a5-137">There are many posts about General ledger on the [Microsoft Dynamics AX product team blog](https://blogs.msdn.microsoft.com/dax/).</span></span> <span data-ttu-id="462a5-138">Auch wenn einige dieser Beiträge für die ältere Version vom Hauptbuch verfasst wurden, gelten die gleichen Konzepte noch und die Prozeduren sind in der aktuellen Version ebenfalls vergleichbar.</span><span class="sxs-lookup"><span data-stu-id="462a5-138">Although some of these posts were written for the previous version of General ledger, the same concepts still apply, and the procedures are also similar in the current version.</span></span>

<span data-ttu-id="462a5-139">Der [Microsoft Dynamics Operations-Partner-Community-Blog](https://community.dynamics.com/partner/b/operationspartnercommunityblog) fasst alle Informationen zu Neuigkeiten und Trends bei MBS Operations für Microsoft Dynamics-Partner in einer einzigen Ressource zusammen.</span><span class="sxs-lookup"><span data-stu-id="462a5-139">The [Microsoft Dynamics Operations Partner Community Blog](https://community.dynamics.com/partner/b/operationspartnercommunityblog) gives Microsoft Dynamics Partners a single resource where they can learn what is new and trending in MBS Operations.</span></span>

#### <a name="community-blogs"></a><span data-ttu-id="462a5-140">Communityblogs</span><span class="sxs-lookup"><span data-stu-id="462a5-140">Community blogs</span></span>

- [<span data-ttu-id="462a5-141">Was Sie zum Sachkonto in Dynamics 365 für Finanzen und Arbeitsgänge wissen sollen</span><span class="sxs-lookup"><span data-stu-id="462a5-141">What you should know about ledger in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/04/29/what-you-should-know-about-ledger-in-dynamics-365-for-finance-and-operations)


