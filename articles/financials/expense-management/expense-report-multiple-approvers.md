---
title: Spesenabrechnungen und mehrere Genehmiger
description: "Dieses Thema enthält Informationen zu Spesenabrechnungen, für die die Genehmigung von mehr als einer Person erforderlich ist."
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: a76acb4912e6f4ace8bedfe45764f8a9594b9801
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---

# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="a90bb-103">Spesenabrechnungen und mehrere Genehmiger</span><span class="sxs-lookup"><span data-stu-id="a90bb-103">Expense reports and multiple approvers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a90bb-104">Je nach den Ausgabengenehmigungsrichtlinien der Organisation müssen u. U. mehrere Personen eine Spesenabrechnung genehmigen, die von einem Mitarbeiter eingereicht wird.</span><span class="sxs-lookup"><span data-stu-id="a90bb-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="a90bb-105">Wenn Sie den Workflowprozess für die Genehmigung von Spesenabrechnungen einrichten, können Sie Workflowelemente hinzufügen, die Aufgaben oder Schritte für eine oder mehrere für Spesenabrechnungen zuständige genehmigende Personen enthalten.</span><span class="sxs-lookup"><span data-stu-id="a90bb-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="a90bb-106">Sie können beispielsweise anfordern, dass alle Spesenabrechnungen zunächst vom Vorgesetzten des Mitarbeiters genehmigt werden, der die Abrechnung eingereicht hat, und dann vom Kreditorenkoordinator.</span><span class="sxs-lookup"><span data-stu-id="a90bb-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="a90bb-107">Wenn Sie festlegen, dass bei Spesenabrechnungen mehrere genehmigende Personen erforderlich sind, können Sie die Workflowelemente auf eine der folgenden Weisen hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="a90bb-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="a90bb-108">Ein Genehmigungselement hinzufügen, das einen Schritt enthält.</span><span class="sxs-lookup"><span data-stu-id="a90bb-108">Add one approval element that has one step.</span></span> <span data-ttu-id="a90bb-109">Der Schritt kann z. B. verlangen, dass eine Spesenabrechnung einer Benutzergruppe zugeordnet wird und dass sie von 50 % der Benutzergruppenmitglieder genehmigt werden muss.</span><span class="sxs-lookup"><span data-stu-id="a90bb-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="a90bb-110">Ein Genehmigungselement hinzufügen, das mehrere Schritte enthält.</span><span class="sxs-lookup"><span data-stu-id="a90bb-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="a90bb-111">Die Schritte im Genehmigungselement können z. B. folgende sein:</span><span class="sxs-lookup"><span data-stu-id="a90bb-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="a90bb-112">Der Vorgesetzte des Mitarbeiters, der die Spesenabrechnung eingereicht hat, genehmigt sie.</span><span class="sxs-lookup"><span data-stu-id="a90bb-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="a90bb-113">Der Kreditorensachbearbeiter überprüft die Zugänge und die Spesenabrechnungsartikel.</span><span class="sxs-lookup"><span data-stu-id="a90bb-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="a90bb-114">Der Budgetbesitzer genehmigt die Spesenabrechnung.</span><span class="sxs-lookup"><span data-stu-id="a90bb-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="a90bb-115">Fügen Sie mehrere Genehmigungselemente hinzu, von denen jedes einen Schritt hat.</span><span class="sxs-lookup"><span data-stu-id="a90bb-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="a90bb-116">Beispielsweise müssen Sie möglicherweise ein gesondertes Genehmigungselements für jeden der folgenden Schritte hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="a90bb-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="a90bb-117">Der Vorgesetzte des Mitarbeiters genehmigt die Spesenabrechnung.</span><span class="sxs-lookup"><span data-stu-id="a90bb-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="a90bb-118">Der Budgetbesitzer genehmigt die Spesenabrechnung.</span><span class="sxs-lookup"><span data-stu-id="a90bb-118">The budget owner approves the expense report.</span></span>

