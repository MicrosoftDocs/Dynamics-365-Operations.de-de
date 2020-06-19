---
title: Verwalten Sie Kauf- und Verkaufsurlaubsrichtlinien
description: Sie können Mitarbeitern ermöglichen, Urlaub zu kaufen und zu verkaufen in Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 06/01/2020
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
ms.openlocfilehash: 859445f2b6e980b5960e512e69129f6a8fc6df2b
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429012"
---
# <a name="manage-buy-and-sell-leave-policies"></a><span data-ttu-id="87309-103">Verwalten Sie Kauf- und Verkaufsurlaubsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="87309-103">Manage buy and sell leave policies</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="87309-104">Sie können Mitarbeitern den Kauf von Urlaub ermöglichen, indem Sie eine Richtlinie für den Kauf von Urlaub erstellen.</span><span class="sxs-lookup"><span data-stu-id="87309-104">You can enable employees to buy leave by creating a buy leave policy.</span></span>  

## <a name="enable-employees-to-buy-and-sell-leave"></a><span data-ttu-id="87309-105">Sie können Mitarbeitern ermöglichen, Urlaub zu kaufen und zu verkaufen in</span><span class="sxs-lookup"><span data-stu-id="87309-105">Enable employees to buy and sell leave</span></span>

1. <span data-ttu-id="87309-106">Auf der **Urlaubs- und Abwesenheitsparameter** Seite wählen Sie **Ja**, um **Mitarbeitern zu erlauben, Urlaub zu kaufen**.</span><span class="sxs-lookup"><span data-stu-id="87309-106">On the **Leave and absence parameters** page, select **Yes** for **Allow employees to buy leave**.</span></span> 

## <a name="create-a-buy-leave-policy"></a><span data-ttu-id="87309-107">Erstellen einer Richtlinie für den Kuaf von Urlaub</span><span class="sxs-lookup"><span data-stu-id="87309-107">Create a buy leave policy</span></span>

1. <span data-ttu-id="87309-108">Auf der Seite **Urlaub- und Abwesenheit** klicken Sie auf die Registerkarte **Links**.</span><span class="sxs-lookup"><span data-stu-id="87309-108">On the **Leave and absence** page, select the **Links** tab.</span></span> 

2. <span data-ttu-id="87309-109">Wählen Sie **Richtlinie für den Kauf- und Verkauf von Urlaub**.</span><span class="sxs-lookup"><span data-stu-id="87309-109">Select **Buy and sell leave policy**.</span></span>

3. <span data-ttu-id="87309-110">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="87309-110">Select **New**.</span></span>

4. <span data-ttu-id="87309-111">Geben Sie einen **Namen** und eine **Beschreibung** für die Richtlinie ein unter **Richtlinie für den Kauf- und Verkauf von Urlaub**.</span><span class="sxs-lookup"><span data-stu-id="87309-111">Enter a **Name** and **Description** for the policy under **Buy and sell leave policy**.</span></span> 

5. <span data-ttu-id="87309-112">Einen **Dokumenttyp** auswählen.</span><span class="sxs-lookup"><span data-stu-id="87309-112">Select a **Policy type**.</span></span> 

   <span data-ttu-id="87309-113">Die verfügbaren Richtlinientypen sind **Menge** und **Stunden pro Woche**.</span><span class="sxs-lookup"><span data-stu-id="87309-113">The available policy types are **Amount** and **Hours per week**.</span></span> <span data-ttu-id="87309-114">Wählen Sie **Menge** aus, um einen **Festen Betrag** für die maximalen Beträge, die Mitarbeiter kaufen und verkaufen können, einzugeben.</span><span class="sxs-lookup"><span data-stu-id="87309-114">Select **Amount** to enter a **Fixed amount** for the maximum amounts employees can buy and sell.</span></span> <span data-ttu-id="87309-115">Wenn Sie **Stunden pro Woche** auswählen, wrid die im zugewiesenen Arbeitszeitkalender des Mitarbeiters definierte Arbeitszeit verwendet, um den Höchstbetrag der Richtlinieolice zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="87309-115">If you select **Hours per week**, the working time defined in the employee's assigned working time calendar is used to determine the maximum amount of the policy.</span></span> 

6. <span data-ttu-id="87309-116">Wählen Sie ein **Startdatum** und ein **Enddatum** für die Richtlinie aus.</span><span class="sxs-lookup"><span data-stu-id="87309-116">Select a **Start date** and **End date** for the policy.</span></span> <span data-ttu-id="87309-117">Anträge auf Kauf oder Verkauf von Urlaub können nur in diesem Zeitraum eingereicht werden.</span><span class="sxs-lookup"><span data-stu-id="87309-117">Requests to buy or sell leave will only be available for submission during this time frame.</span></span> 

7. <span data-ttu-id="87309-118">Unter **Kaufrichtlinie**, wählen **Vollzeitäquivalenz** (FTE) aus, um den Höchstbetrag basierend auf dem auf der Position des Mitarbeiters definierten FTE aufzuteilen.</span><span class="sxs-lookup"><span data-stu-id="87309-118">Under **Buy policy**, select **Full time equivalency** (FTE) to prorate the maximum amount based on the FTE defined on the employee's position.</span></span> <span data-ttu-id="87309-119">Wenn der Richtlinientyp **Menge** ist, geben Sie einen **Maximalen festen Betrag** ein.</span><span class="sxs-lookup"><span data-stu-id="87309-119">If the policy type is **Amount**, enter a **Maximum fixed amount**.</span></span> 

8. <span data-ttu-id="87309-120">Wählen Sie **Hinzufügen**, um die Urlaubsarten für Mitarbeiter hinzuzufügen, um Urlaub zu kaufen.</span><span class="sxs-lookup"><span data-stu-id="87309-120">Select **Add** to add the leave types for employees to buy leave.</span></span> <span data-ttu-id="87309-121">Sie können der Richtlinie mehrere Urlaubstypen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="87309-121">You can add multiple leave types to the policy.</span></span> 

9. <span data-ttu-id="87309-122">Geben Sie die **Dienstmonate** für die Urlaubsart ein, damit verschiedene Dienstmonate den Höchstbetrag bestimmen können, den ein Mitarbeiter kaufen kann.</span><span class="sxs-lookup"><span data-stu-id="87309-122">Enter the **Months of service** for the leave type to enable different months of service to determine the maximum amount an employee can buy.</span></span> 

10. <span data-ttu-id="87309-123">Dient zum Eingeben des **Maximalen Betrags** für den Urlaubstyp.</span><span class="sxs-lookup"><span data-stu-id="87309-123">Enter the **Maximum amount** for the leave type.</span></span> 

11. <span data-ttu-id="87309-124">Geben Sie die **Rate** ein, zu der der Arbeitnehmer den Urlaub kauft.</span><span class="sxs-lookup"><span data-stu-id="87309-124">Enter the **Rate** at which the employee will buy the leave.</span></span> 

12. <span data-ttu-id="87309-125">Optional geben Sie den **Verdienstcode** ein, der für den Kauf von Urlaub verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="87309-125">Optionally enter the **Earning code** to be used for buying leave.</span></span> 

13. <span data-ttu-id="87309-126">Legen Sie optional fest, ob FTE verwendet werden soll, um den Höchstbetrag für die Urlaubsart zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="87309-126">Optionally set whether to use FTE to determine the maximum amount for the leave type.</span></span> 

## <a name="add-the-buy-and-sell-leave-policy-to-a-leave-and-absence-plan"></a><span data-ttu-id="87309-127">Fügen Sie die Kauf- und Verkaufsurlaubsrichtlinie einem Urlaubs- und Abwesenheitsplan hinzu</span><span class="sxs-lookup"><span data-stu-id="87309-127">Add the buy and sell leave policy to a leave and absence plan</span></span>

1. <span data-ttu-id="87309-128">Auf der **Urlaub und Abwesenheit** Seite, wählen Sie einen Urlaubs- und Abwesenheitsplan.</span><span class="sxs-lookup"><span data-stu-id="87309-128">On the **Leave and absence** page, select a leave and absence plan.</span></span>

2. <span data-ttu-id="87309-129">Wählen Sie **Regeln** für die **Richtlinie für den Kauf- und Verkauf**.</span><span class="sxs-lookup"><span data-stu-id="87309-129">Under **Rules**, select **Buy and sell leave policy**.</span></span>

## <a name="see-also"></a><span data-ttu-id="87309-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="87309-130">See also</span></span>

[<span data-ttu-id="87309-131">Urlaubs- und Abwesenheitsübersicht</span><span class="sxs-lookup"><span data-stu-id="87309-131">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="87309-132">Urlaubs- und Abwesenheitstypen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="87309-132">Configure leave and absence types</span></span>](hr-leave-and-absence-types.md)</br>
[<span data-ttu-id="87309-133">Urlaubs- und Abwesenheitspläne antizipieren</span><span class="sxs-lookup"><span data-stu-id="87309-133">Accrue leave and absence plans</span></span>](hr-leave-and-absence-accrue.md)</br>
[<span data-ttu-id="87309-134">Urlaub kaufen und verkaufen</span><span class="sxs-lookup"><span data-stu-id="87309-134">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

