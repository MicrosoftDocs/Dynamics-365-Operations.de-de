---
title: Verwalten Sie Kauf- und Verkaufsurlaubsrichtlinien
description: Sie können Mitarbeitern ermöglichen, Urlaub zu kaufen und zu verkaufen in Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeaveBuySellPolicy, LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 55d29c42cc1b2d69517e2fcd458ee6a1bdf5277f
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "3712110"
---
# <a name="manage-buy-and-sell-leave-policies"></a><span data-ttu-id="7f713-103">Kauf- und Verkaufsurlaubsrichtlinien verwalten</span><span class="sxs-lookup"><span data-stu-id="7f713-103">Manage buy and sell leave policies</span></span>

<span data-ttu-id="7f713-104">Sie können Mitarbeitern den Kauf und Verkauf von Urlaub ermöglichen, indem Sie eine Richtlinie für den Kauf und Verkauf von Urlaub erstellen.</span><span class="sxs-lookup"><span data-stu-id="7f713-104">You can enable employees to buy and sell leave by creating a buy and sell leave policy.</span></span> <span data-ttu-id="7f713-105">Sie können diese Richtlinien so konfigurieren, dass sie den Workflow für Genehmigungen verwenden, maximale Beträge und Preise festlegen und Preise für Kauf und Verkauf festlegen.</span><span class="sxs-lookup"><span data-stu-id="7f713-105">You can configure these policies to use workflow for approvals, set maximum amounts and rates, and set rates for buying and selling.</span></span> 

## <a name="enable-employees-to-buy-and-sell-leave"></a><span data-ttu-id="7f713-106">Sie können Mitarbeitern ermöglichen, Urlaub zu kaufen und zu verkaufen in</span><span class="sxs-lookup"><span data-stu-id="7f713-106">Enable employees to buy and sell leave</span></span>

1. <span data-ttu-id="7f713-107">Auf der Seite **Urlaubs- und Abwesenheitsparameter** wählen Sie **Ja** für **Mitarbeitern erlauben, Urlaub zu kaufen** und **Mitarbeitern erlauben, Urlaub zu verkaufen**.</span><span class="sxs-lookup"><span data-stu-id="7f713-107">On the **Leave and absence parameters** page, select **Yes** for **Allow employees to buy leave** and **Allow employees to sell leave**.</span></span>

## <a name="create-a-buy-and-sell-leave-policy"></a><span data-ttu-id="7f713-108">Eine Richtlinie zum Kaufen und Verkaufen von Urlaub erstellen</span><span class="sxs-lookup"><span data-stu-id="7f713-108">Create a buy and sell leave policy</span></span>

1. <span data-ttu-id="7f713-109">Auf der Seite **Urlaub- und Abwesenheit** klicken Sie auf die Registerkarte **Links**.</span><span class="sxs-lookup"><span data-stu-id="7f713-109">On the **Leave and absence** page, select the **Links** tab.</span></span> 

2. <span data-ttu-id="7f713-110">Wählen Sie **Richtlinie für den Kauf- und Verkauf von Urlaub**.</span><span class="sxs-lookup"><span data-stu-id="7f713-110">Select **Buy and sell leave policy**.</span></span>

3. <span data-ttu-id="7f713-111">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="7f713-111">Select **New**.</span></span>

4. <span data-ttu-id="7f713-112">Geben Sie einen **Namen** und eine **Beschreibung** für die Richtlinie ein unter **Richtlinie für den Kauf- und Verkauf von Urlaub**.</span><span class="sxs-lookup"><span data-stu-id="7f713-112">Enter a **Name** and **Description** for the policy under **Buy and sell leave policy**.</span></span> 

5. <span data-ttu-id="7f713-113">Einen **Dokumenttyp** auswählen.</span><span class="sxs-lookup"><span data-stu-id="7f713-113">Select a **Policy type**.</span></span> 

   <span data-ttu-id="7f713-114">Die verfügbaren Richtlinientypen sind **Menge** und **Stunden pro Woche**.</span><span class="sxs-lookup"><span data-stu-id="7f713-114">The available policy types are **Amount** and **Hours per week**.</span></span> <span data-ttu-id="7f713-115">Wählen Sie **Menge** aus, um einen **Festen Betrag** für die maximalen Beträge, die Mitarbeiter kaufen und verkaufen können, einzugeben.</span><span class="sxs-lookup"><span data-stu-id="7f713-115">Select **Amount** to enter a **Fixed amount** for the maximum amounts employees can buy and sell.</span></span> <span data-ttu-id="7f713-116">Wenn Sie **Stunden pro Woche** auswählen, wrid die im zugewiesenen Arbeitszeitkalender des Mitarbeiters definierte Arbeitszeit verwendet, um den Höchstbetrag der Richtlinieolice zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="7f713-116">If you select **Hours per week**, the working time defined in the employee's assigned working time calendar is used to determine the maximum amount of the policy.</span></span> 

6. <span data-ttu-id="7f713-117">Wählen Sie ein **Startdatum** und ein **Enddatum** für die Richtlinie aus.</span><span class="sxs-lookup"><span data-stu-id="7f713-117">Select a **Start date** and **End date** for the policy.</span></span> <span data-ttu-id="7f713-118">Anträge auf Kauf oder Verkauf von Urlaub können nur in diesem Zeitraum eingereicht werden.</span><span class="sxs-lookup"><span data-stu-id="7f713-118">Requests to buy or sell leave will only be available for submission during this time frame.</span></span> 

7. <span data-ttu-id="7f713-119">Wählen Sie eine **Workflow-ID** für die Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="7f713-119">Select a **Workflow ID** for the policy.</span></span> <span data-ttu-id="7f713-120">Bei sämtlichen Kauf- und Verkaufsanforderungen wird dieser Workflow zur Überprüfung und Genehmigung verwendet.</span><span class="sxs-lookup"><span data-stu-id="7f713-120">Any buy and sell requests will use this workflow for review and approval.</span></span> 

8. <span data-ttu-id="7f713-121">Unter **Kaufrichtlinie**, wählen **Vollzeitäquivalenz** (FTE) aus, um den Höchstbetrag basierend auf dem auf der Position des Mitarbeiters definierten FTE aufzuteilen.</span><span class="sxs-lookup"><span data-stu-id="7f713-121">Under **Buy policy**, select **Full time equivalency** (FTE) to prorate the maximum amount based on the FTE defined on the employee's position.</span></span> <span data-ttu-id="7f713-122">Wenn der Richtlinientyp **Menge** ist, geben Sie einen **Maximalen festen Betrag** ein.</span><span class="sxs-lookup"><span data-stu-id="7f713-122">If the policy type is **Amount**, enter a **Maximum fixed amount**.</span></span> 

9. <span data-ttu-id="7f713-123">Wählen Sie **Hinzufügen**, um die Urlaubsarten für Mitarbeiter hinzuzufügen, um Urlaub zu kaufen.</span><span class="sxs-lookup"><span data-stu-id="7f713-123">Select **Add** to add the leave types for employees to buy leave.</span></span> <span data-ttu-id="7f713-124">Sie können der Richtlinie mehrere Urlaubstypen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="7f713-124">You can add multiple leave types to the policy.</span></span> 

10. <span data-ttu-id="7f713-125">Geben Sie die **Dienstmonate** für die Urlaubsart ein, damit verschiedene Dienstmonate den Höchstbetrag bestimmen können, den ein Mitarbeiter kaufen kann.</span><span class="sxs-lookup"><span data-stu-id="7f713-125">Enter the **Months of service** for the leave type to enable different months of service to determine the maximum amount an employee can buy.</span></span> 

11. <span data-ttu-id="7f713-126">Dient zum Eingeben des **Maximalen Betrags** für den Urlaubstyp.</span><span class="sxs-lookup"><span data-stu-id="7f713-126">Enter the **Maximum amount** for the leave type.</span></span> 

12. <span data-ttu-id="7f713-127">Geben Sie die **Rate** ein, zu der der Arbeitnehmer den Urlaub kauft.</span><span class="sxs-lookup"><span data-stu-id="7f713-127">Enter the **Rate** at which the employee will buy the leave.</span></span> 

13. <span data-ttu-id="7f713-128">Optional geben Sie den **Verdienstcode** ein, der für den Kauf von Urlaub verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7f713-128">Optionally enter the **Earning code** to be used for buying leave.</span></span> 

14. <span data-ttu-id="7f713-129">Legen Sie optional fest, ob FTE verwendet werden soll, um den Höchstbetrag für die Urlaubsart zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="7f713-129">Optionally set whether to use FTE to determine the maximum amount for the leave type.</span></span> 

15. <span data-ttu-id="7f713-130">Befolgen Sie die Schritte 8 bis 14 unter **Verkaufsrichtlinie**, um eine Verkaufsrichtlinie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7f713-130">To create a sell policy, follow steps 8 through 14 under **Sell policy**.</span></span> 

## <a name="add-the-buy-and-sell-leave-policy-to-a-leave-and-absence-plan"></a><span data-ttu-id="7f713-131">Fügen Sie die Kauf- und Verkaufsurlaubsrichtlinie einem Urlaubs- und Abwesenheitsplan hinzu</span><span class="sxs-lookup"><span data-stu-id="7f713-131">Add the buy and sell leave policy to a leave and absence plan</span></span>

1. <span data-ttu-id="7f713-132">Auf der **Urlaub und Abwesenheit** Seite, wählen Sie einen Urlaubs- und Abwesenheitsplan.</span><span class="sxs-lookup"><span data-stu-id="7f713-132">On the **Leave and absence** page, select a leave and absence plan.</span></span>

2. <span data-ttu-id="7f713-133">Wählen Sie **Regeln** für die **Richtlinie für den Kauf- und Verkauf**.</span><span class="sxs-lookup"><span data-stu-id="7f713-133">Under **Rules**, select **Buy and sell leave policy**.</span></span>

## <a name="see-also"></a><span data-ttu-id="7f713-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7f713-134">See also</span></span>

[<span data-ttu-id="7f713-135">Urlaubs- und Abwesenheitsübersicht</span><span class="sxs-lookup"><span data-stu-id="7f713-135">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="7f713-136">Urlaubs- und Abwesenheitstypen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="7f713-136">Configure leave and absence types</span></span>](hr-leave-and-absence-types.md)</br>
[<span data-ttu-id="7f713-137">Urlaubs- und Abwesenheitspläne antizipieren</span><span class="sxs-lookup"><span data-stu-id="7f713-137">Accrue leave and absence plans</span></span>](hr-leave-and-absence-accrue.md)</br>
[<span data-ttu-id="7f713-138">Urlaub kaufen und verkaufen</span><span class="sxs-lookup"><span data-stu-id="7f713-138">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

