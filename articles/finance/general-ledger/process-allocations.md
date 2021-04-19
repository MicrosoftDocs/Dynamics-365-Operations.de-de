---
title: Verarbeiten von Zuteilungen
description: Dieser Artikel enthält Informationen zu Zuweisungen, die Optionen zum Verarbeitung in Microsoft Dynamics 365 Finance und wie sie in der Budgetplanung verwendet werden können. Zuweisungen werden verwendet, um Beträge über mehrere Sachkontokombinationen zu verteilen. Sie unterstützen, um sicherzustellen, dass Ausgaben oder Umsatzerlöse zum richtigen Objekt Buchhaltungsmodul in der Buchhaltung berechnet wird.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: roschlom
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 30f445698eddba8bdbb2ac9a257142458fb5990f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815427"
---
# <a name="process-allocations"></a><span data-ttu-id="49bb4-105">Zuteilungen verarbeiten</span><span class="sxs-lookup"><span data-stu-id="49bb4-105">Process allocations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="49bb4-106">Dieser Artikel enthält Informationen zu Zuweisungen, die Optionen zum Verarbeitung und wie sie in der Budgetplanung verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="49bb4-106">This article provides information about allocations, the options for processing them, and how they can be used in budget planning.</span></span> <span data-ttu-id="49bb4-107">Zuweisungen werden verwendet, um Beträge über mehrere Sachkontokombinationen zu verteilen.</span><span class="sxs-lookup"><span data-stu-id="49bb4-107">Allocations are used to distribute amounts across multiple ledger account combinations.</span></span> <span data-ttu-id="49bb4-108">Sie unterstützen, um sicherzustellen, dass Ausgaben oder Umsatzerlöse zum richtigen Objekt Buchhaltungsmodul in der Buchhaltung berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="49bb4-108">They help ensure that expenses or revenues are charged to the correct object in accounting.</span></span>

<span data-ttu-id="49bb4-109">Folgende Funktionen unterstützen diesen Prozesses:</span><span class="sxs-lookup"><span data-stu-id="49bb4-109">The following capabilities support this process:</span></span>

-   <span data-ttu-id="49bb4-110">Manuelle Zuteilung von Transaktionsbeträgen: Verwenden Sie dazu die Aktivität "Teilen" in den Buchhaltungsverteilungen oder wenden Sie Standardvorlagen für Finanzdimensionen auf ein Dokument an.</span><span class="sxs-lookup"><span data-stu-id="49bb4-110">Manually allocate transaction amounts by using the Split action in accounting distributions, or by applying financial dimension default templates to a document.</span></span> <span data-ttu-id="49bb4-111">Weitere Informationen finden Sie unter [Abrechnungsverteilungen](../accounts-payable/accounting-distributions.md).</span><span class="sxs-lookup"><span data-stu-id="49bb4-111">For more information, see [Accounting distributions](../accounts-payable/accounting-distributions.md).</span></span>
-   <span data-ttu-id="49bb4-112">Automatische Zuteilung von Transaktionsbeträgen: Dies geschieht auf der Grundlage von Zuteilungsbedingungen, die für das jeweilige Hauptkonto definiert sind.</span><span class="sxs-lookup"><span data-stu-id="49bb4-112">Automatically allocate transactions amounts based on allocation terms defined on individual main account.</span></span> <span data-ttu-id="49bb4-113">Zuteilungskontoeinträge werden basierend auf dem Prozentsatz und dem Zielsachkonto für jede Erfassung generiert, wenn ein Buchhaltungseintrag die für das Quellsachkonto definierten Kriterien erfüllt.</span><span class="sxs-lookup"><span data-stu-id="49bb4-113">Allocation account entries will be generated for each journal based on the percentage and destination ledger account whenever an accounting entry meets the criteria defined as the source ledger account.</span></span> <span data-ttu-id="49bb4-114">Weitere Informationen finden Sie unter [Zuordnungserfassungen Hauptkonto](../general-ledger/main-account-allocation-terms.md)</span><span class="sxs-lookup"><span data-stu-id="49bb4-114">For more information, see [Main account allocation terms](../general-ledger/main-account-allocation-terms.md)</span></span>
-   <span data-ttu-id="49bb4-115">Automatische Zuteilung von Sachkontosalden oder festen Beträgen auf der Grundlage von Sachkonto-Zuordnungsregeln.</span><span class="sxs-lookup"><span data-stu-id="49bb4-115">Automatically allocate ledger balances or fixed amounts based on ledger allocation rules.</span></span> <span data-ttu-id="49bb4-116">Die Sachkonto-Zuordnungsregeln werden periodisch mithilfe der Zuordnungserfassungen verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="49bb4-116">The ledger allocation rules are processed on a periodic basis using allocation journals.</span></span> <span data-ttu-id="49bb4-117">Weitere Informationen finden Sie unter [Zuordnungsregeln](../general-ledger/ledger-allocation-rules.md).</span><span class="sxs-lookup"><span data-stu-id="49bb4-117">For more information, see [Allocation rules](../general-ledger/ledger-allocation-rules.md).</span></span>

###  <a name="allocations-in-budget-planning"></a><span data-ttu-id="49bb4-118">Zuteilungen bei der Budgetplanung</span><span class="sxs-lookup"><span data-stu-id="49bb4-118">Allocations in budget planning</span></span>

<span data-ttu-id="49bb4-119">Sachkonto-Zuordnungsregeln können für Budgetpläne verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="49bb4-119">Ledger allocation rules can be used for budget plans.</span></span> <span data-ttu-id="49bb4-120">Wenn Sie Sachkontozuordnungsregeln in der Budgetplanung verwenden, die arbeiten die Zuordnungsregeln nach der gleichen Methode wie im Sachkonto, aber die Quelldaten und die Zieldaten stammen aus dem Budgetplan.</span><span class="sxs-lookup"><span data-stu-id="49bb4-120">When you use ledger allocation rules in budget planning, the allocation rules work the same way they would in the ledger, but the source data and destination data comes from the budget plan.</span></span> <span data-ttu-id="49bb4-121">Sie können Sachkontozuordnungsregeln manuell auswählen, um sie für Budgetpläne zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="49bb4-121">You can manually select ledger allocation rules to use for budget plans.</span></span> <span data-ttu-id="49bb4-122">Alternativ können Sie einen Zuordnungszeitplan verwenden, der als Teil einer Workflowprozesses ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="49bb4-122">Alternatively, you can use an allocation schedule that runs as part of a workflow process.</span></span>

> [!NOTE]
> <span data-ttu-id="49bb4-123">Sie können Intercompany-Sachkontozuordnungsregeln für Budgetplanung nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="49bb4-123">You can’t use intercompany ledger allocation rules for budget planning.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]