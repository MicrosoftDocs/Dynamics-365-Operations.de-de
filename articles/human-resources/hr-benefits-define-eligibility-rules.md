---
title: Regeln und Richtlinien zur Vorteilsberechtigung festlegen
description: Dieser Artikel beschreibt, wie Sie Vorteilsberechtigungsregeln und -richtlinien erstellen und diese Regeln dann zu Vorteilen zuweisen.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: df517e1ab72634cb434411fab3bd92bf34c7e609
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805945"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a><span data-ttu-id="b030d-103">Regeln und Richtlinien zur Vorteilsberechtigung festlegen</span><span class="sxs-lookup"><span data-stu-id="b030d-103">Define benefit eligibility rules and policies</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="b030d-104">Dieses Thema beschreibt, wie Sie Vorteilsberechtigungsregeln und -richtlinien erstellen und diese Regeln dann zu Vorteilen zuweisen.</span><span class="sxs-lookup"><span data-stu-id="b030d-104">This topic shows you how you can create benefit eligibility rules and policies and then assign rules to benefits.</span></span>  

## <a name="create-benefit-eligibility-policy-rule-type"></a><span data-ttu-id="b030d-105">Erstellen eines Regeltyps für Vergütungsberechtigungsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="b030d-105">Create benefit eligibility policy rule type</span></span>

1. <span data-ttu-id="b030d-106">Wechseln Sie zu **Personalverwaltung > Vorteile > Berechtigung > Regeltypen für Vorteilsberechtigungsrichtlinien**.</span><span class="sxs-lookup"><span data-stu-id="b030d-106">Go to **Human resources > Benefits > Eligibility > Benefit eligibility policy rule types**.</span></span>
2. <span data-ttu-id="b030d-107">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="b030d-107">Select **New**.</span></span>
3. <span data-ttu-id="b030d-108">Geben Sie im Feld **Regelname** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="b030d-108">In the **Rule name** field, enter a value.</span></span>
4. <span data-ttu-id="b030d-109">Geben Sie im Feld **Beschreibung** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="b030d-109">In the **Description** field, enter a value.</span></span>
5. <span data-ttu-id="b030d-110">Wählen Sie im Feld **Abfragename** die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b030d-110">In the **Query name** field, select the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="b030d-111">Wählen Sie in der Liste den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="b030d-111">In the list, select the link in the selected row.</span></span>
7. <span data-ttu-id="b030d-112">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="b030d-112">Select **Save**.</span></span>
8. <span data-ttu-id="b030d-113">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="b030d-113">Close the page.</span></span>

## <a name="benefit-eligibility-policy"></a><span data-ttu-id="b030d-114">Vergütungsberechtigungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="b030d-114">Benefit eligibility policy</span></span>

1. <span data-ttu-id="b030d-115">Wechseln Sie zu **Personalverwaltung > Vorteile > Berechtigung > Vorteilsberechtigungsrichtlinien**.</span><span class="sxs-lookup"><span data-stu-id="b030d-115">Go to **Human resources > Benefits > Eligibility > Benefit eligibility policies**.</span></span>
2. <span data-ttu-id="b030d-116">Wählen Sie eine vorhandene Vorteilsrichtlinie aus.</span><span class="sxs-lookup"><span data-stu-id="b030d-116">Select an existing benefit policy.</span></span>
3. <span data-ttu-id="b030d-117">Wählen Sie in der Liste den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="b030d-117">In the list, select the link in the selected row.</span></span>
4. <span data-ttu-id="b030d-118">Schalten Sie die Erweiterung des Abschnitts **Richtlinienorganisationen** ein/aus.</span><span class="sxs-lookup"><span data-stu-id="b030d-118">Toggle the expansion of the **Policy organizations** sections.</span></span> <span data-ttu-id="b030d-119">Sie können alle Organisationen hinzufügen oder entfernen, die Sie in der Richtlinie einbeziehen möchten.</span><span class="sxs-lookup"><span data-stu-id="b030d-119">You can add or remove any organizations you want to include in the policy.</span></span>
5. <span data-ttu-id="b030d-120">Erweitern oder reduzieren Sie den Abschnitt **Richtlinienregeln**.</span><span class="sxs-lookup"><span data-stu-id="b030d-120">Expand or collapse the **Policy rules** section.</span></span>
6. <span data-ttu-id="b030d-121">Suchen Sie in der Liste die zuvor erstellte Richtlinienregel.</span><span class="sxs-lookup"><span data-stu-id="b030d-121">In the list, find the policy rule previously created.</span></span>
7. <span data-ttu-id="b030d-122">Wählen Sie **Richtlinienregel erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="b030d-122">Select **Create policy rule**.</span></span>
8. <span data-ttu-id="b030d-123">Geben Sie im Feld **Gültigkeitsdatum** das Datum ein, an dem die Richtlinie gültig werden soll.</span><span class="sxs-lookup"><span data-stu-id="b030d-123">In the **Effective date** field, enter the date in which you want the policy to become effective.</span></span>
    * <span data-ttu-id="b030d-124">Das Festlegen des effektiven Enddatums ermöglicht es Ihnen, zukünftige Änderungen an den Richtlinienregeln vorzunehmen, sodass Sie nicht zur Richtlinie zurückkehren müssen, wenn diese Änderungen wirksam werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b030d-124">Setting effective end dates allows you to make future changes to policy rules so you don't need to come back to the policy when you want those changes to take effect.</span></span>  
9. <span data-ttu-id="b030d-125">Fügen Sie bei Bedarf eine where-Klausel im **Bedingung hinzufügen**-Feld hinzu.</span><span class="sxs-lookup"><span data-stu-id="b030d-125">If needed, add a where clause to the **Add condition** field.</span></span>
    * <span data-ttu-id="b030d-126">Wenn Sie beispielsweise möchten, dass die Regel nur für Verkaufsleiter gilt, können Sie eine where-Klausel erstellen, bei der die Positionsbeschreibung Verkaufsleiter entspricht.</span><span class="sxs-lookup"><span data-stu-id="b030d-126">For example if you wanted the rule to only apply to Sales Managers you could create the where clause to say: Where position description equals Sales Manager.</span></span> <span data-ttu-id="b030d-127">Sie können mehrere where-Anweisungen zusammen in der Regel hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b030d-127">You can add multiple where statements together in the rule.</span></span>  
10. <span data-ttu-id="b030d-128">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="b030d-128">Select **OK**.</span></span>
11. <span data-ttu-id="b030d-129">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="b030d-129">Close the page.</span></span>

## <a name="assign-rule-to-benefit"></a><span data-ttu-id="b030d-130">Zuweisen der Regel zum Vorteil</span><span class="sxs-lookup"><span data-stu-id="b030d-130">Assign rule to benefit</span></span>

1. <span data-ttu-id="b030d-131">Wechseln Sie zu **Personalverwaltung > Vorteile > Vorteile**.</span><span class="sxs-lookup"><span data-stu-id="b030d-131">Go to **Human resources > Benefits > Benefits**.</span></span>
2. <span data-ttu-id="b030d-132">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="b030d-132">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="b030d-133">Wählen Sie in der Liste den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="b030d-133">In the list, select the link in the selected row.</span></span>
4. <span data-ttu-id="b030d-134">Erweitern oder reduzieren Sie den Abschnitt **Berechtigungsregeln**.</span><span class="sxs-lookup"><span data-stu-id="b030d-134">Expand or collapse the **Eligibility rules** section.</span></span>
5. <span data-ttu-id="b030d-135">Wählen Sie **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="b030d-135">Select **Edit**.</span></span>
6. <span data-ttu-id="b030d-136">Wählen Sie die Regel im Feld **Berechtigung** aus.</span><span class="sxs-lookup"><span data-stu-id="b030d-136">In the **Eligibility** field, select the rule.</span></span>
7. <span data-ttu-id="b030d-137">Wählen Sie im Feld **Regeltyp** die zuvor erstellte Regel aus.</span><span class="sxs-lookup"><span data-stu-id="b030d-137">In the **Rule type** field, select the rule you previously created.</span></span>
9. <span data-ttu-id="b030d-138">Wählen Sie in der Liste den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="b030d-138">In the list, select the link in the selected row.</span></span>
10. <span data-ttu-id="b030d-139">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="b030d-139">Select **Save**.</span></span>
11. <span data-ttu-id="b030d-140">Schließt das Formular.</span><span class="sxs-lookup"><span data-stu-id="b030d-140">Close the form.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]