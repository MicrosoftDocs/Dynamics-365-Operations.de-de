---
title: Vorteilsberechtigungsrichtlinien
description: Dieser Artikel enthält Informationen zu Vorteilseberechtigungspolicen fest, die Sie dabei unterstützen festzulegen, wer für bestimmte Vorteile berechtigt ist.
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: ae4be70058e61cdbc1d2b063b346b45b023eb9e9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "304478"
---
# <a name="benefit-eligibility-policies"></a><span data-ttu-id="af309-103">Vorteilsberechtigungsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="af309-103">Benefit eligibility policies</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="af309-104">Dieses Themal enthält Informationen zu Vorteilseberechtigungspolicen, die Sie dabei unterstützen festzulegen, wer für bestimmte Vorteile berechtigt ist.</span><span class="sxs-lookup"><span data-stu-id="af309-104">This topic provides information about benefit eligibility policies, which help you define who is eligible for specific benefits.</span></span>

<span data-ttu-id="af309-105">Wenn Sie Vorteile erstellen, müssen Sie entscheiden, welche Vorteile für welche Mitarbeiter zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="af309-105">When you create benefits, you decide which benefits will be available to which employees.</span></span> <span data-ttu-id="af309-106">Die folgende Tabelle zeigt Beispiele für Vorteile, die Sie vielleicht bestimmten Mitarbeitern zugänglich machen möchten.</span><span class="sxs-lookup"><span data-stu-id="af309-106">The following table shows examples of benefits that you might make available to specific employees.</span></span>

| <span data-ttu-id="af309-107">Vorteil</span><span class="sxs-lookup"><span data-stu-id="af309-107">Benefit</span></span>          | <span data-ttu-id="af309-108">Vorteil ist verfügbar für</span><span class="sxs-lookup"><span data-stu-id="af309-108">Who the benefit is available to</span></span> |
|------------------|---------------------------------|
| <span data-ttu-id="af309-109">Krankenversicherung</span><span class="sxs-lookup"><span data-stu-id="af309-109">Health insurance</span></span> | <span data-ttu-id="af309-110">Alle Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="af309-110">All employees</span></span>                   |
| <span data-ttu-id="af309-111">Mobiltelefon</span><span class="sxs-lookup"><span data-stu-id="af309-111">Mobile phone</span></span>     | <span data-ttu-id="af309-112">Verkaufspersonal, Führungskräfte</span><span class="sxs-lookup"><span data-stu-id="af309-112">Sales staff, executives</span></span>         |
| <span data-ttu-id="af309-113">Parkausweise</span><span class="sxs-lookup"><span data-stu-id="af309-113">Parking passes</span></span>   | <span data-ttu-id="af309-114">Führungskräfte</span><span class="sxs-lookup"><span data-stu-id="af309-114">Executives</span></span>                      |

<span data-ttu-id="af309-115">Die folgenden Komponenten werden verwendet, um Berechtigungsrichtlinien zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="af309-115">The following components in are used to create eligibility policies:</span></span>

-   <span data-ttu-id="af309-116">Richtlinienregeltypen</span><span class="sxs-lookup"><span data-stu-id="af309-116">Policy rule types</span></span>
-   <span data-ttu-id="af309-117">Vorteilsberechtigungsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="af309-117">Benefit eligibility policies</span></span>

<span data-ttu-id="af309-118">Durch Richtlinienregeltypen werden die Abfrageparameter definiert, die beim Entwickeln bestimmter Richtlinienregeln verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="af309-118">Policy rule types define the query parameters that are used when you develop specific policy rules.</span></span> <span data-ttu-id="af309-119">Wenn Sie Richtlinienregeltypen erstellt haben, können Sie Berechtigungsrichtlinien für Vorteile erstellen.</span><span class="sxs-lookup"><span data-stu-id="af309-119">After you create policy rule types, you can create benefit eligibility policies.</span></span> <span data-ttu-id="af309-120">Über die Richtlinien können Sie eine Regelsammlung erstellen, die für eine oder mehrere juristische Personen gilt.</span><span class="sxs-lookup"><span data-stu-id="af309-120">The policies let you create a collection of rules that apply to one or more legal entities.</span></span> <span data-ttu-id="af309-121">Innerhalb jeder Richtlinie können Sie jeden der eben erstellten Richtlinienregeltypen für die Vorteilsberechtigung anzeigen.</span><span class="sxs-lookup"><span data-stu-id="af309-121">Within each policy, you can view any of the benefit eligibility policy rule types that you created earlier.</span></span> 

<span data-ttu-id="af309-122">Sie definieren den Umfang der Regel innerhalb der Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="af309-122">You define the scope of the rule within the policy.</span></span> <span data-ttu-id="af309-123">Wenn Sie beispielsweise einen Richtlinienregeltyp für die Vorteilsberechtigung mit der Bezeichnung **Führungskraft** erstellen, können Sie die Regel innerhalb dieser Richtlinie definieren.</span><span class="sxs-lookup"><span data-stu-id="af309-123">For example, if you create a benefit eligibility policy rule type that is named **Executive**, you can specify what the rule is within that policy.</span></span> <span data-ttu-id="af309-124">Hier kann die Regel zum Beispiel angeben, dass jede Position, die das Wort "Führungskraft" enthält, in diese Regel einbezogen werden soll.</span><span class="sxs-lookup"><span data-stu-id="af309-124">In this example, the rule might state that any job title that contains the word “executive” should be included in the rule.</span></span> <span data-ttu-id="af309-125">Nachdem Sie die Parameter der in der Richtlinie enthaltenen Regel(n) definiert haben, können Sie dem Vorteil eine bestimmte Regel zuweisen.</span><span class="sxs-lookup"><span data-stu-id="af309-125">After you've defined the parameters of the rule or rules that are included in the policy, you can assign a specific rule to the benefit.</span></span>

<a name="additional-resources"></a><span data-ttu-id="af309-126">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="af309-126">Additional resources</span></span>
--------

[<span data-ttu-id="af309-127">Definieren und verwalten eines Vorteilprogramms</span><span class="sxs-lookup"><span data-stu-id="af309-127">Defining and managing a benefit program</span></span>](manage-benefit-program.md)



