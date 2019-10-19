---
title: Vorteilsberechtigungsregeln und Richtlinien definieren
description: Diese Aufzeichnung zeigt Ihnen an, wie Sie Vorteilsberechtigungsregeln und -richtlinien erstellen und diese Regeln dann zu Vorteilen zuweisen.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d0d35266c95cfbf3473a14fec47a1c748229dd25
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190556"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a><span data-ttu-id="8b449-103">Vorteilsberechtigungsregeln und Richtlinien definieren</span><span class="sxs-lookup"><span data-stu-id="8b449-103">Define benefit eligibility rules and policies</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8b449-104">Diese Aufzeichnung zeigt Ihnen an, wie Sie Vorteilsberechtigungsregeln und -richtlinien erstellen und diese Regeln dann zu Vorteilen zuweisen.</span><span class="sxs-lookup"><span data-stu-id="8b449-104">This recording will show you how you can create benefit eligibility rules and policies and then assign rules to Benefits.</span></span>  

<span data-ttu-id="8b449-105">Das Demodatenunternehmen, das verwendet wird, um diese Aufzeichnung zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="8b449-105">The demo data company used to create this recording is USMF.</span></span>


## <a name="create-benefit-eligibility-policy-rule-type"></a><span data-ttu-id="8b449-106">Erstellen eines Regeltyps für Vergütungsberechtigungsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="8b449-106">Create benefit eligibility policy rule type</span></span>
1. <span data-ttu-id="8b449-107">Wechseln Sie zu "Personalverwaltung" > "Vorteile" > "Berechtigung" > "Regeltypen für Vergütungsberechtigungsrichtlinien".</span><span class="sxs-lookup"><span data-stu-id="8b449-107">Go to Human resources > Benefits > Eligibility > Benefit eligibility policy rule types.</span></span>
2. <span data-ttu-id="8b449-108">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="8b449-108">Click New.</span></span>
3. <span data-ttu-id="8b449-109">Geben Sie im Feld "Regelname" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="8b449-109">In the Rule name field, type a value.</span></span>
4. <span data-ttu-id="8b449-110">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="8b449-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="8b449-111">Klicken Sie im Feld "Abfragename" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8b449-111">In the Query name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="8b449-112">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="8b449-112">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="8b449-113">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="8b449-113">Click Save.</span></span>
8. <span data-ttu-id="8b449-114">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8b449-114">Close the page.</span></span>

## <a name="benefit-eligibility-policy"></a><span data-ttu-id="8b449-115">Vergütungsberechtigungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="8b449-115">Benefit eligibility policy</span></span>
1. <span data-ttu-id="8b449-116">Wechseln Sie zu "Personalverwaltung"  "Vorteile"  "Berechtigung"  "Vorteilsberechtigungsrichtlinien".</span><span class="sxs-lookup"><span data-stu-id="8b449-116">Go to Human resources > Benefits > Eligibility > Benefit eligibility policies.</span></span>
2. <span data-ttu-id="8b449-117">Wählen Sie eine vorhandene Vorteilsrichtlinie aus.</span><span class="sxs-lookup"><span data-stu-id="8b449-117">Select an existing benefit policy.</span></span>
3. <span data-ttu-id="8b449-118">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="8b449-118">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="8b449-119">Schalten Sie die Erweiterung des Abschnitts "Richtlinienorganisationen" ein/aus.</span><span class="sxs-lookup"><span data-stu-id="8b449-119">Toggle the expansion of the Policy organizations sections.</span></span>  <span data-ttu-id="8b449-120">Hier können Sie alle Organisationen hinzufügen oder entfernen, die Sie in der Richtlinie einbeziehen möchten.</span><span class="sxs-lookup"><span data-stu-id="8b449-120">Here you can add or remove any organizations you want to include in the policy.</span></span>
5. <span data-ttu-id="8b449-121">Erweitern oder reduzieren Sie den Abschnitt "Richtlinienregeln".</span><span class="sxs-lookup"><span data-stu-id="8b449-121">Expand or collapse the Policy rules section.</span></span>
6. <span data-ttu-id="8b449-122">Suchen Sie in der Liste die zuvor erstellte Richtlinienregel.</span><span class="sxs-lookup"><span data-stu-id="8b449-122">In the list find the policy rule previously created.</span></span>
7. <span data-ttu-id="8b449-123">Klicken Sie auf "Richtlinienregel erstellen".</span><span class="sxs-lookup"><span data-stu-id="8b449-123">Click Create policy rule.</span></span>
8. <span data-ttu-id="8b449-124">Geben Sie im Feld "Gültigkeitsdatum" das Datum ein, an dem die Richtlinie gültig werden soll.</span><span class="sxs-lookup"><span data-stu-id="8b449-124">In the Effective date field, enter the date in which you want the policy to become effective.</span></span>
    * <span data-ttu-id="8b449-125">Das Festlegen des effektiven Datums und des Enddatums ermöglicht es Ihnen, zukünftige Änderungen an den Richtlinienregeln vorzunehmen, ohne dass Sie zur Richtlinie zurückkehren müssen, wenn diese Änderungen wirksam werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8b449-125">Setting effective and end dates allows you to make future changes to policy rules and removing the need to come back to the policy when you want those changes to take effect.</span></span>  
9. 
    * <span data-ttu-id="8b449-126">Wenn Sie beispielsweise möchten, dass die Regel nur für Verkaufsleiter gilt, können Sie eine WHERE-Klausel erstellen, bei der die Positionsbeschreibung Verkaufsleiter entspricht.</span><span class="sxs-lookup"><span data-stu-id="8b449-126">For example if you wanted the rule to only apply to Sales Managers you could create the Where clause to say: Where position description equals Sales Manager.</span></span>  <span data-ttu-id="8b449-127">Sie können mehrere WHERE-Anweisungen mit AND und OR in der Regel verbinden.</span><span class="sxs-lookup"><span data-stu-id="8b449-127">You can And or Or multiple Where statements together in the rule.</span></span>  
10. <span data-ttu-id="8b449-128">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8b449-128">Click OK.</span></span>
11. <span data-ttu-id="8b449-129">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8b449-129">Close the page.</span></span>
12. <span data-ttu-id="8b449-130">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8b449-130">Close the page.</span></span>

## <a name="assign-rule-to-benefit"></a><span data-ttu-id="8b449-131">Zuweisen der Regel zum Vorteil</span><span class="sxs-lookup"><span data-stu-id="8b449-131">Assign rule to benefit</span></span>
1. <span data-ttu-id="8b449-132">Wechseln Sie zu "Personalverwaltung" > "Leistungen" > "Leistungen".</span><span class="sxs-lookup"><span data-stu-id="8b449-132">Go to Human resources > Benefits > Benefits.</span></span>
2. <span data-ttu-id="8b449-133">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="8b449-133">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="8b449-134">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="8b449-134">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="8b449-135">Erweitern oder reduzieren Sie den Abschnitt "Berechtigungsregeln".</span><span class="sxs-lookup"><span data-stu-id="8b449-135">Expand or collapse the Eligibility rules section.</span></span>
5. <span data-ttu-id="8b449-136">Klicken Sie auf Bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="8b449-136">Click Edit.</span></span>
6. <span data-ttu-id="8b449-137">Wählen Sie im Feld "Berechtigung" "Regelbasiert" aus der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="8b449-137">In the Eligibility field, select Rule based from the list.</span></span>
7. <span data-ttu-id="8b449-138">Klicken Sie im Feld "Regeltyp" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8b449-138">In the Rule type field, click the drop down button to open the lookup.</span></span>
8. <span data-ttu-id="8b449-139">Suchen Sie in der Liste die zuvor erstellte Richtlinienregel und wählen Sie diese aus.</span><span class="sxs-lookup"><span data-stu-id="8b449-139">In the list find and select the rule you previously created.</span></span>
9. <span data-ttu-id="8b449-140">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="8b449-140">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="8b449-141">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="8b449-141">Click Save.</span></span>
11. <span data-ttu-id="8b449-142">Schließt das Formular.</span><span class="sxs-lookup"><span data-stu-id="8b449-142">Close the form.</span></span>

