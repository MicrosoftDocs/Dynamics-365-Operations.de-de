---
title: Vorteilsberechtigungsrichtlinien
description: Dieser Artikel enthält Informationen zu Vorteilseberechtigungspolicen fest, die Sie dabei unterstützen festzulegen, wer für bestimmte Vorteile berechtigt ist.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 7b35d3f9a8afd3be44b648f6e138afd5f143ba55
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009221"
---
# <a name="benefit-eligibility-policies"></a><span data-ttu-id="e935d-103">Richtlinien zur Vorteilsberechtigung</span><span class="sxs-lookup"><span data-stu-id="e935d-103">Benefit eligibility policies</span></span>

<span data-ttu-id="e935d-104">Dieser Artikel enthält Informationen zu Vorteilseberechtigungspolicen fest, die Sie dabei unterstützen festzulegen, wer für bestimmte Vorteile berechtigt ist.</span><span class="sxs-lookup"><span data-stu-id="e935d-104">This article provides information about benefit eligibility policies, which help you define who is eligible for specific benefits.</span></span>

<span data-ttu-id="e935d-105">Wenn Sie Vorteile erstellen, müssen Sie entscheiden, welche Vorteile für welche Mitarbeiter zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="e935d-105">When you create benefits, you decide which benefits will be available to which employees.</span></span> <span data-ttu-id="e935d-106">Die folgende Tabelle zeigt Beispiele für Vorteile, die Sie vielleicht bestimmten Mitarbeitern zugänglich machen möchten.</span><span class="sxs-lookup"><span data-stu-id="e935d-106">The following table shows examples of benefits that you might make available to specific employees.</span></span>

| <span data-ttu-id="e935d-107">Vorteil</span><span class="sxs-lookup"><span data-stu-id="e935d-107">Benefit</span></span>          | <span data-ttu-id="e935d-108">Vorteil ist verfügbar für</span><span class="sxs-lookup"><span data-stu-id="e935d-108">Who the benefit is available to</span></span> |
|------------------|---------------------------------|
| <span data-ttu-id="e935d-109">Krankenversicherung</span><span class="sxs-lookup"><span data-stu-id="e935d-109">Health insurance</span></span> | <span data-ttu-id="e935d-110">Alle Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="e935d-110">All employees</span></span>                   |
| <span data-ttu-id="e935d-111">Mobiltelefon</span><span class="sxs-lookup"><span data-stu-id="e935d-111">Mobile phone</span></span>     | <span data-ttu-id="e935d-112">Verkaufspersonal, Führungskräfte</span><span class="sxs-lookup"><span data-stu-id="e935d-112">Sales staff, executives</span></span>         |
| <span data-ttu-id="e935d-113">Parkausweise</span><span class="sxs-lookup"><span data-stu-id="e935d-113">Parking passes</span></span>   | <span data-ttu-id="e935d-114">Führungskräfte</span><span class="sxs-lookup"><span data-stu-id="e935d-114">Executives</span></span>                      |

<span data-ttu-id="e935d-115">Die folgenden Komponenten werden verwendet, um Berechtigungsrichtlinien zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="e935d-115">The following components in are used to create eligibility policies:</span></span>

-   <span data-ttu-id="e935d-116">Richtlinienregeltypen</span><span class="sxs-lookup"><span data-stu-id="e935d-116">Policy rule types</span></span>
-   <span data-ttu-id="e935d-117">Vorteilsberechtigungsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="e935d-117">Benefit eligibility policies</span></span>

<span data-ttu-id="e935d-118">Durch Richtlinienregeltypen werden die Abfrageparameter definiert, die beim Entwickeln bestimmter Richtlinienregeln verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e935d-118">Policy rule types define the query parameters that are used when you develop specific policy rules.</span></span> <span data-ttu-id="e935d-119">Wenn Sie Richtlinienregeltypen erstellt haben, können Sie Berechtigungsrichtlinien für Vorteile erstellen.</span><span class="sxs-lookup"><span data-stu-id="e935d-119">After you create policy rule types, you can create benefit eligibility policies.</span></span> <span data-ttu-id="e935d-120">Über die Richtlinien können Sie eine Regelsammlung erstellen, die für eine oder mehrere juristische Personen gilt.</span><span class="sxs-lookup"><span data-stu-id="e935d-120">The policies let you create a collection of rules that apply to one or more legal entities.</span></span> <span data-ttu-id="e935d-121">Innerhalb jeder Richtlinie können Sie jeden der eben erstellten Richtlinienregeltypen für die Vorteilsberechtigung anzeigen.</span><span class="sxs-lookup"><span data-stu-id="e935d-121">Within each policy, you can view any of the benefit eligibility policy rule types that you created earlier.</span></span> 

<span data-ttu-id="e935d-122">Sie definieren den Umfang der Regel innerhalb der Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="e935d-122">You define the scope of the rule within the policy.</span></span> <span data-ttu-id="e935d-123">Wenn Sie beispielsweise einen Richtlinienregeltyp für die Vorteilsberechtigung mit der Bezeichnung **Führungskraft** erstellen, können Sie die Regel innerhalb dieser Richtlinie definieren.</span><span class="sxs-lookup"><span data-stu-id="e935d-123">For example, if you create a benefit eligibility policy rule type that is named **Executive**, you can specify what the rule is within that policy.</span></span> <span data-ttu-id="e935d-124">Hier kann die Regel zum Beispiel angeben, dass jede Position, die das Wort Führungskraft enthält, in diese Regel einbezogen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e935d-124">In this example, the rule might state that any job title that contains the word "executive" should be included in the rule.</span></span> <span data-ttu-id="e935d-125">Nachdem Sie die Parameter der in der Richtlinie enthaltenen Regel(n) definiert haben, können Sie dem Vorteil eine bestimmte Regel zuweisen.</span><span class="sxs-lookup"><span data-stu-id="e935d-125">After you've defined the parameters of the rule or rules that are included in the policy, you can assign a specific rule to the benefit.</span></span>




