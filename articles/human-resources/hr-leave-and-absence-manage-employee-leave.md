---
title: Mitarbeiter-Sonderurlaub verwalten
description: Mitarbeiter-Sonderurlaub in Dynamics 365 Human Resources verwalten.
author: andreabichsel
ms.date: 11/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 33080fc5ca43f3d83ee9d17565f4c229ced7b94f
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055627"
---
# <a name="manage-employee-leave"></a><span data-ttu-id="873d2-103">Mitarbeiter-Sonderurlaub verwalten</span><span class="sxs-lookup"><span data-stu-id="873d2-103">Manage employee leave</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="873d2-104">Sie können die Abwesenheit eines Mitarbeiters nach Abwesenheitstyp verwalten.</span><span class="sxs-lookup"><span data-stu-id="873d2-104">You can manage an employee's leave by leave type.</span></span> <span data-ttu-id="873d2-105">Dies umfasst das Ablaufen der Abwesenheitsregistrierung und das Anpassen der Abwesenheitstypsguthaben.</span><span class="sxs-lookup"><span data-stu-id="873d2-105">This includes expiring leave enrollment and adjusting leave type balances.</span></span> 

## <a name="adjust-leave-balances"></a><span data-ttu-id="873d2-106">Abwesenheitsguthaben anpassen</span><span class="sxs-lookup"><span data-stu-id="873d2-106">Adjust leave balances</span></span>

1. <span data-ttu-id="873d2-107">Wählen Sie im Datensatz des Mitarbeiters **Abweseneheit** aus.</span><span class="sxs-lookup"><span data-stu-id="873d2-107">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="873d2-108">**Urlaubs- und Abwesenheitseinstellungen** auswählen.</span><span class="sxs-lookup"><span data-stu-id="873d2-108">Select **Leave and absence setup**.</span></span>

3. <span data-ttu-id="873d2-109">Wählen Sie **Saldo anpassen** aus.</span><span class="sxs-lookup"><span data-stu-id="873d2-109">Select **Adjust balance**.</span></span>

4. <span data-ttu-id="873d2-110">Wählen Sie **Abwesenheitstyp** aus.</span><span class="sxs-lookup"><span data-stu-id="873d2-110">Select the **Leave type**.</span></span>

5. <span data-ttu-id="873d2-111">Geben Sie einen **Regulierungsbetrag** ein.</span><span class="sxs-lookup"><span data-stu-id="873d2-111">Enter an **Adjustment amount**.</span></span> 

6. <span data-ttu-id="873d2-112">Sie können optional ein **Datum** eingeben.</span><span class="sxs-lookup"><span data-stu-id="873d2-112">Optionally, you can select a **Date**.</span></span> 

<span data-ttu-id="873d2-113">Sie können einen Ursachencode und einen Kommentar einfügen, wenn Sie das Abwesenheitsguthaben eines Mitarbeiters anpassen.</span><span class="sxs-lookup"><span data-stu-id="873d2-113">You can include a reason code and comment when adjusting an employee's leave balance.</span></span> 

>[!IMPORTANT]
><span data-ttu-id="873d2-114">Zusätzliche Informationen zu Abwesenheitsguthaben werden in der Vorschau angezeigt.</span><span class="sxs-lookup"><span data-stu-id="873d2-114">Viewing additional information about leave balances is in preview.</span></span> <span data-ttu-id="873d2-115">Sie müssen es in Ihrer **Sandbox**-Umgebung aktivieren.</span><span class="sxs-lookup"><span data-stu-id="873d2-115">You'll need to enable it in your **Sandbox** environment.</span></span> <span data-ttu-id="873d2-116">Weitere Informationen zum Aktivieren der Vorschaufunktionen finden Sie unter [Funktonen verwalten](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="873d2-116">For more information about enabling preview features, see [Manage features](hr-admin-manage-features.md).</span></span><br>
><span data-ttu-id="873d2-117">Wenn Sie die Maus über ein Abwesenheitsguthaben bewegen, wird Folgendes angezeigt:</span><span class="sxs-lookup"><span data-stu-id="873d2-117">When hovering over any leave balance, you will now see:</span></span><br>
>- <span data-ttu-id="873d2-118">**Verfügbar**: In diesem Jahr insgesamt – in diesem Jahr genommen</span><span class="sxs-lookup"><span data-stu-id="873d2-118">**Available**: Total this year - Take this year</span></span>
>- <span data-ttu-id="873d2-119">**In diesem Jahr insgesamt**: Alle aufgelaufenen, angepassten und übertragenen arbeitsfreien Zeiten des Jahres</span><span class="sxs-lookup"><span data-stu-id="873d2-119">**Total this year**: All accruals, adjustments, and carry forward for the year</span></span>
>- <span data-ttu-id="873d2-120">**In diesem Jahr genommen**: Alle genehmigten arbeitsfreien Zeiten</span><span class="sxs-lookup"><span data-stu-id="873d2-120">**Taken this year**: All approved time off</span></span>

## <a name="see-also"></a><span data-ttu-id="873d2-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="873d2-121">See also</span></span>

- [<span data-ttu-id="873d2-122">Urlaubs- und Abwesenheitsübersicht</span><span class="sxs-lookup"><span data-stu-id="873d2-122">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="873d2-123">Urlaubs- und Abwesenheitsanforderungen verwalten</span><span class="sxs-lookup"><span data-stu-id="873d2-123">Manage leave and absence requests</span></span>](hr-employee-self-service-manage-requests.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]