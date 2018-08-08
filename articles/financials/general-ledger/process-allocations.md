---
title: Verarbeiten von Zuteilungen
description: "Dieser Artikel enthält Informationen zu Zuteilungen, die Optionen zu ihrer Verarbeitung in Microsoft Dynamics 365 for Finance and Operations und wie sie in der Budgetplanung verwendet werden können. Zuweisungen werden verwendet, um Beträge über mehrere Sachkontokombinationen zu verteilen. Sie unterstützen, um sicherzustellen, dass eine Ausgabe oder Umsatzerlös zum richtigen Objekt Buchhaltungsmodul in der Buchhaltung berechnet wird."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: ac531726e04ebec4da9062f47726568723364cce
ms.contentlocale: de-de
ms.lasthandoff: 08/07/2018

---

# <a name="process-allocations"></a><span data-ttu-id="e5f60-105">Verarbeiten von Zuteilungen</span><span class="sxs-lookup"><span data-stu-id="e5f60-105">Process allocations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e5f60-106">Dieser Artikel enthält Informationen zu Zuteilungen, die Optionen zu ihrer Verarbeitung in Microsoft Dynamics 365 for Finance and Operations und wie sie in der Budgetplanung verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="e5f60-106">This article provides information about allocations, the options for processing them in Microsoft Dynamics 365 for Finance and Operations, and how they can be used in budget planning.</span></span> <span data-ttu-id="e5f60-107">Zuweisungen werden verwendet, um Beträge über mehrere Sachkontokombinationen zu verteilen.</span><span class="sxs-lookup"><span data-stu-id="e5f60-107">Allocations are used to distribute amounts across multiple ledger account combinations.</span></span> <span data-ttu-id="e5f60-108">Sie unterstützen, um sicherzustellen, dass eine Ausgabe oder Umsatzerlös zum richtigen Objekt Buchhaltungsmodul in der Buchhaltung berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="e5f60-108">They help guarantee that expenses or revenue is charged to the correct object in accounting.</span></span>

<span data-ttu-id="e5f60-109">Microsoft Dynamics 365 for Finance and Operations enthält die folgenden Funktionen zur Unterstützung dieses Vorgangs:</span><span class="sxs-lookup"><span data-stu-id="e5f60-109">Microsoft Dynamics 365 for Finance and Operations provides the following capabilities to support this process:</span></span>

-   <span data-ttu-id="e5f60-110">Manuelle Zuteilung von Transaktionsbeträgen: Verwenden Sie dazu die Aktivität "Teilen" in den Buchhaltungsverteilungen oder wenden Sie Standardvorlagen für Finanzdimensionen auf ein Dokument an.</span><span class="sxs-lookup"><span data-stu-id="e5f60-110">Manually allocate transaction amounts by using the Split action in accounting distributions, or by applying financial dimension default templates to a document.</span></span> <span data-ttu-id="e5f60-111">Weitere Informationen finden Sie unter [Buchhaltungsverteilungen](../accounts-payable/accounting-distributions.md).</span><span class="sxs-lookup"><span data-stu-id="e5f60-111">For more information, see [Accounting distributions.](../accounts-payable/accounting-distributions.md)</span></span>
-   <span data-ttu-id="e5f60-112">Automatische Zuteilung von Transaktionsbeträgen: Dies geschieht auf der Grundlage von Zuteilungsbedingungen, die für das jeweilige Hauptkonto definiert sind.</span><span class="sxs-lookup"><span data-stu-id="e5f60-112">Automatically allocate transactions amounts based on allocation terms defined on individual main account.</span></span> <span data-ttu-id="e5f60-113">Zuteilungskontoeinträge werden basierend auf dem Prozentsatz und dem Zielsachkonto für jede Erfassung generiert, wenn ein Buchhaltungseintrag die für das Quellsachkonto definierten Kriterien erfüllt.</span><span class="sxs-lookup"><span data-stu-id="e5f60-113">Allocation account entries will be generated for each journal based on the percentage and destination ledger account whenever an accounting entry meets the criteria defined as the source ledger account.</span></span>
-   <span data-ttu-id="e5f60-114">Automatische Zuteilung von Sachkontosalden oder festen Beträgen auf der Grundlage von Sachkonto-Zuordnungsregeln.</span><span class="sxs-lookup"><span data-stu-id="e5f60-114">Automatically allocate ledger balances or fixed amounts based on ledger allocation rules.</span></span> <span data-ttu-id="e5f60-115">Die Sachkonto-Zuordnungsregeln werden periodisch mithilfe der Zuordnungserfassungen verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="e5f60-115">The ledger allocation rules are processed on a periodic basis using allocation journals.</span></span> 

###  <a name="allocations-in-budget-planning"></a><span data-ttu-id="e5f60-116">Zuteilungen bei der Budgetplanung</span><span class="sxs-lookup"><span data-stu-id="e5f60-116">Allocations in budget planning</span></span>

<span data-ttu-id="e5f60-117">Sachkonto-Zuordnungsregeln können für Budgetpläne verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e5f60-117">Ledger allocation rules can be used for budget plans.</span></span> <span data-ttu-id="e5f60-118">Wenn Sie Sachkontozuordnungsregeln in der Budgetplanung verwenden, die arbeiten die Zuordnungsregeln nach der gleichen Methode wie im Sachkonto, aber die Quelldaten und die Zieldaten stammen aus dem Budgetplan.</span><span class="sxs-lookup"><span data-stu-id="e5f60-118">When you use ledger allocation rules in budget planning, the allocation rules work the same way they would in the ledger, but the source data and destination data comes from the budget plan.</span></span> <span data-ttu-id="e5f60-119">Sie können Sachkontozuordnungsregeln manuell auswählen, um sie für Budgetpläne zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="e5f60-119">You can manually select ledger allocation rules to use for budget plans.</span></span> <span data-ttu-id="e5f60-120">Alternativ können Sie einen Zuordnungszeitplan verwenden, der als Teil einer Workflowprozesses ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e5f60-120">Alternatively, you can use an allocation schedule that runs as part of a workflow process.</span></span>

> [!NOTE]
> <span data-ttu-id="e5f60-121">Sie können Intercompany-Sachkontozuordnungsregeln für Budgetplanung nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="e5f60-121">You can’t use intercompany ledger allocation rules for budget planning.</span></span>






