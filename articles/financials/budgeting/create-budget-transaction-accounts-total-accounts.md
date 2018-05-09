---
title: "Erstellen Sie ein Budget für Buchungs- und Summenkonten"
description: "Dieser Artikel gibt einen Überblick über den Prozess für das Erstellen von Budgets basierend auf Summenkonten. Er erläutert auch, wie die Budgetsteuerung für Summenkonten aktiviert wird, wenn die Budgetsteuerung erforderlich ist."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetControlConfiguration, BudgetPlanGenerate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13051
ms.assetid: fb1bb2d3-445c-402f-a9a3-aa6503eed78e
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 3b7c8031c40cf0ce3072577ac936aecc5de2a810
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---

# <a name="create-a-budget-from-transaction-accounts-and-total-accounts"></a><span data-ttu-id="70c1b-104">Erstellen Sie ein Budget für Buchungs- und Summenkonten</span><span class="sxs-lookup"><span data-stu-id="70c1b-104">Create a budget from transaction accounts and total accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="70c1b-105">Dieser Artikel gibt einen Überblick über den Prozess für das Erstellen von Budgets basierend auf Summenkonten.</span><span class="sxs-lookup"><span data-stu-id="70c1b-105">This article provides an overview of the process for creating budgets based on total accounts.</span></span> <span data-ttu-id="70c1b-106">Er erläutert auch, wie die Budgetsteuerung für Summenkonten aktiviert wird, wenn die Budgetsteuerung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="70c1b-106">It also explains how to turn on budget control for total accounts, if budget control is required.</span></span>

<span data-ttu-id="70c1b-107">Sowohl mit Haushaltsplan- als auch mit Budgetregistereintragsdokumenten können Hauptkonten budgetiert werden, deren Hauptkontotyp **Summe** lautet.</span><span class="sxs-lookup"><span data-stu-id="70c1b-107">Both budget plan and budget register entry documents allow for budgeting on main accounts that have a main account type of **Total**.</span></span> <span data-ttu-id="70c1b-108">Istwerte können nur den buchungsbezogenen Hauptkonten gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="70c1b-108">Actuals can be posted only to transactional main accounts.</span></span> 

<span data-ttu-id="70c1b-109">Für den periodischen Prozess zum **Generieren eines Budgetplans aus dem Hauptbuch** auf der Registerkarte **Quelle** können Sie den Hauptkontotyp **Summe** als Kriterium angeben.</span><span class="sxs-lookup"><span data-stu-id="70c1b-109">For the **Generate budget plan from General ledger** periodic process, on the **Source** tab, you can specify the **Total** main account type as a criterion.</span></span> <span data-ttu-id="70c1b-110">In diesem Fall ist jedes Gesamthauptkonto im Ziel-Haushaltsplan einbezogen, und der Betrag entspricht dem Gesamtbetrag des Bereichs der ausgewählten Hauptkonten.</span><span class="sxs-lookup"><span data-stu-id="70c1b-110">In this case, each total main account will be included in the target budget plan, and the amount will equal the total amount of the range of selected main accounts.</span></span> 

<span data-ttu-id="70c1b-111">Sie können die Budgetsteuerung für Hauptkonten vom **Summe**-Typ aktivieren.</span><span class="sxs-lookup"><span data-stu-id="70c1b-111">You can activate budget control for main accounts of the **Total** type.</span></span> <span data-ttu-id="70c1b-112">Diese Funktionalität wird durch die Verwendung von Budgetgruppen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="70c1b-112">This functionality is supported through the use of budget groups.</span></span> <span data-ttu-id="70c1b-113">Für jedes Hauptkonto muss das gesamte Budget, für das eine Budgetgruppe gesteuert werden soll, auf der Seite ** Budgetsteuerungskonfiguration ** erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="70c1b-113">For each total main account, the budget that should be controlled for a budget group must be created on the **Budget control configuration **page.</span></span> <span data-ttu-id="70c1b-114">Die Kriterien, die Sie angeben, müssen das gesamte Hauptkonto und den Bereich der Konten umfassen.</span><span class="sxs-lookup"><span data-stu-id="70c1b-114">The criteria that you specify must include the total main account and the range of accounts.</span></span> <span data-ttu-id="70c1b-115">Um den Prozess der Erstellung von Budgetgruppen zu beschleunigen, können Sie die Datenentität Budgetsteuerungsgruppen nutzen.</span><span class="sxs-lookup"><span data-stu-id="70c1b-115">To speed up the process of creating budget groups, you can take advantage of the Budget control groups data entity.</span></span> 

<span data-ttu-id="70c1b-116">Wenn ein Budget für die Berichterstellung, also beispielsweise in einer Finanzaufstellung, verwendet wird, setzt sich die Budgetsumme für das Summenkonto wie folgt zusammen:</span><span class="sxs-lookup"><span data-stu-id="70c1b-116">When a budget is used in reporting, such as on a financial statement, the budget sum for the total account consists of the following amounts:</span></span>

-   <span data-ttu-id="70c1b-117">Aus den Budgets, die auf jedem Buchungssachkonto innerhalb des Intervalls des Summenkontos erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="70c1b-117">The budgets that are created from each transaction ledger account in the interval of the total account.</span></span>
-   <span data-ttu-id="70c1b-118">Aus dem Budgetbetrag, der direkt auf dem Summenkonto gebucht wird</span><span class="sxs-lookup"><span data-stu-id="70c1b-118">The budget amount that is entered directly on the total account.</span></span>

<span data-ttu-id="70c1b-119">Auf diese Weise können also separate Budgets für die wichtigsten Buchungskonten im Intervall des Summenkontos erstellt und kann der verbleibende Budgetbetrag dem Summenkonto hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="70c1b-119">Therefore, you can create separate budgets for the most significant transaction accounts in the interval of the total account, and then add the available budget amount to the total account.</span></span>




