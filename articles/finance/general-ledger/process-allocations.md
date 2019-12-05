---
title: Verarbeiten von Zuteilungen
description: Dieser Artikel enthält Informationen zu Zuweisungen, die Optionen zum Verarbeitung in Microsoft Dynamics 365 Finance und wie sie in der Budgetplanung verwendet werden können. Zuweisungen werden verwendet, um Beträge über mehrere Sachkontokombinationen zu verteilen. Sie unterstützen, um sicherzustellen, dass Ausgaben oder Umsatzerlöse zum richtigen Objekt Buchhaltungsmodul in der Buchhaltung berechnet wird.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 32271e967da2e7f3702b0c6c2dcdba460aa1b382
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770619"
---
# <a name="process-allocations"></a><span data-ttu-id="4936b-105">Zuteilungen verarbeiten</span><span class="sxs-lookup"><span data-stu-id="4936b-105">Process allocations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4936b-106">Dieser Artikel enthält Informationen zu Zuweisungen, die Optionen zum Verarbeitung und wie sie in der Budgetplanung verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="4936b-106">This article provides information about allocations, the options for processing them, and how they can be used in budget planning.</span></span> <span data-ttu-id="4936b-107">Zuweisungen werden verwendet, um Beträge über mehrere Sachkontokombinationen zu verteilen.</span><span class="sxs-lookup"><span data-stu-id="4936b-107">Allocations are used to distribute amounts across multiple ledger account combinations.</span></span> <span data-ttu-id="4936b-108">Sie unterstützen, um sicherzustellen, dass Ausgaben oder Umsatzerlöse zum richtigen Objekt Buchhaltungsmodul in der Buchhaltung berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="4936b-108">They help ensure that expenses or revenues are charged to the correct object in accounting.</span></span>

<span data-ttu-id="4936b-109">Folgende Funktionen unterstützen diesen Prozesses:</span><span class="sxs-lookup"><span data-stu-id="4936b-109">The following capabilities support this process:</span></span>

-   <span data-ttu-id="4936b-110">Manuelle Zuteilung von Transaktionsbeträgen: Verwenden Sie dazu die Aktivität "Teilen" in den Buchhaltungsverteilungen oder wenden Sie Standardvorlagen für Finanzdimensionen auf ein Dokument an.</span><span class="sxs-lookup"><span data-stu-id="4936b-110">Manually allocate transaction amounts by using the Split action in accounting distributions, or by applying financial dimension default templates to a document.</span></span> <span data-ttu-id="4936b-111">Weitere Informationen finden Sie unter [Abrechnungsverteilungen](../accounts-payable/accounting-distributions.md).</span><span class="sxs-lookup"><span data-stu-id="4936b-111">For more information, see [Accounting distributions](../accounts-payable/accounting-distributions.md).</span></span>
-   <span data-ttu-id="4936b-112">Automatische Zuteilung von Transaktionsbeträgen: Dies geschieht auf der Grundlage von Zuteilungsbedingungen, die für das jeweilige Hauptkonto definiert sind.</span><span class="sxs-lookup"><span data-stu-id="4936b-112">Automatically allocate transactions amounts based on allocation terms defined on individual main account.</span></span> <span data-ttu-id="4936b-113">Zuteilungskontoeinträge werden basierend auf dem Prozentsatz und dem Zielsachkonto für jede Erfassung generiert, wenn ein Buchhaltungseintrag die für das Quellsachkonto definierten Kriterien erfüllt.</span><span class="sxs-lookup"><span data-stu-id="4936b-113">Allocation account entries will be generated for each journal based on the percentage and destination ledger account whenever an accounting entry meets the criteria defined as the source ledger account.</span></span>
-   <span data-ttu-id="4936b-114">Automatische Zuteilung von Sachkontosalden oder festen Beträgen auf der Grundlage von Sachkonto-Zuordnungsregeln.</span><span class="sxs-lookup"><span data-stu-id="4936b-114">Automatically allocate ledger balances or fixed amounts based on ledger allocation rules.</span></span> <span data-ttu-id="4936b-115">Die Sachkonto-Zuordnungsregeln werden periodisch mithilfe der Zuordnungserfassungen verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="4936b-115">The ledger allocation rules are processed on a periodic basis using allocation journals.</span></span> 

###  <a name="allocations-in-budget-planning"></a><span data-ttu-id="4936b-116">Zuteilungen bei der Budgetplanung</span><span class="sxs-lookup"><span data-stu-id="4936b-116">Allocations in budget planning</span></span>

<span data-ttu-id="4936b-117">Sachkonto-Zuordnungsregeln können für Budgetpläne verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4936b-117">Ledger allocation rules can be used for budget plans.</span></span> <span data-ttu-id="4936b-118">Wenn Sie Sachkontozuordnungsregeln in der Budgetplanung verwenden, die arbeiten die Zuordnungsregeln nach der gleichen Methode wie im Sachkonto, aber die Quelldaten und die Zieldaten stammen aus dem Budgetplan.</span><span class="sxs-lookup"><span data-stu-id="4936b-118">When you use ledger allocation rules in budget planning, the allocation rules work the same way they would in the ledger, but the source data and destination data comes from the budget plan.</span></span> <span data-ttu-id="4936b-119">Sie können Sachkontozuordnungsregeln manuell auswählen, um sie für Budgetpläne zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="4936b-119">You can manually select ledger allocation rules to use for budget plans.</span></span> <span data-ttu-id="4936b-120">Alternativ können Sie einen Zuordnungszeitplan verwenden, der als Teil einer Workflowprozesses ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4936b-120">Alternatively, you can use an allocation schedule that runs as part of a workflow process.</span></span>

> [!NOTE]
> <span data-ttu-id="4936b-121">Sie können Intercompany-Sachkontozuordnungsregeln für Budgetplanung nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="4936b-121">You can’t use intercompany ledger allocation rules for budget planning.</span></span>





