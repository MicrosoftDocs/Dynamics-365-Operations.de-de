---
title: Vorteilsberechtigungsrichtlinien
description: Dieser Artikel enthält Informationen zu Vorteilseberechtigungspolicen fest, die Sie dabei unterstützen festzulegen, wer für bestimmte Vorteile berechtigt ist.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: ad179e505d045dc40898105e1cfd090daafa09a8
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518128"
---
# <a name="benefit-eligibility-policies"></a><span data-ttu-id="5a74a-103">Vorteilsberechtigungsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="5a74a-103">Benefit eligibility policies</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5a74a-104">Dieses Themal enthält Informationen zu Vorteilseberechtigungspolicen, die Sie dabei unterstützen festzulegen, wer für bestimmte Vorteile berechtigt ist.</span><span class="sxs-lookup"><span data-stu-id="5a74a-104">This topic provides information about benefit eligibility policies, which help you define who is eligible for specific benefits.</span></span>

<span data-ttu-id="5a74a-105">Wenn Sie Vorteile erstellen, müssen Sie entscheiden, welche Vorteile für welche Mitarbeiter zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="5a74a-105">When you create benefits, you decide which benefits will be available to which employees.</span></span> <span data-ttu-id="5a74a-106">Die folgende Tabelle zeigt Beispiele für Vorteile, die Sie vielleicht bestimmten Mitarbeitern zugänglich machen möchten.</span><span class="sxs-lookup"><span data-stu-id="5a74a-106">The following table shows examples of benefits that you might make available to specific employees.</span></span>

| <span data-ttu-id="5a74a-107">Vorteil</span><span class="sxs-lookup"><span data-stu-id="5a74a-107">Benefit</span></span>          | <span data-ttu-id="5a74a-108">Vorteil ist verfügbar für</span><span class="sxs-lookup"><span data-stu-id="5a74a-108">Who the benefit is available to</span></span> |
|------------------|---------------------------------|
| <span data-ttu-id="5a74a-109">Krankenversicherung</span><span class="sxs-lookup"><span data-stu-id="5a74a-109">Health insurance</span></span> | <span data-ttu-id="5a74a-110">Alle Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="5a74a-110">All employees</span></span>                   |
| <span data-ttu-id="5a74a-111">Mobiltelefon</span><span class="sxs-lookup"><span data-stu-id="5a74a-111">Mobile phone</span></span>     | <span data-ttu-id="5a74a-112">Verkaufspersonal, Führungskräfte</span><span class="sxs-lookup"><span data-stu-id="5a74a-112">Sales staff, executives</span></span>         |
| <span data-ttu-id="5a74a-113">Parkausweise</span><span class="sxs-lookup"><span data-stu-id="5a74a-113">Parking passes</span></span>   | <span data-ttu-id="5a74a-114">Führungskräfte</span><span class="sxs-lookup"><span data-stu-id="5a74a-114">Executives</span></span>                      |

<span data-ttu-id="5a74a-115">Die folgenden Komponenten werden verwendet, um Berechtigungsrichtlinien zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="5a74a-115">The following components in are used to create eligibility policies:</span></span>

-   <span data-ttu-id="5a74a-116">Richtlinienregeltypen</span><span class="sxs-lookup"><span data-stu-id="5a74a-116">Policy rule types</span></span>
-   <span data-ttu-id="5a74a-117">Vorteilsberechtigungsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="5a74a-117">Benefit eligibility policies</span></span>

<span data-ttu-id="5a74a-118">Durch Richtlinienregeltypen werden die Abfrageparameter definiert, die beim Entwickeln bestimmter Richtlinienregeln verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5a74a-118">Policy rule types define the query parameters that are used when you develop specific policy rules.</span></span> <span data-ttu-id="5a74a-119">Wenn Sie Richtlinienregeltypen erstellt haben, können Sie Berechtigungsrichtlinien für Vorteile erstellen.</span><span class="sxs-lookup"><span data-stu-id="5a74a-119">After you create policy rule types, you can create benefit eligibility policies.</span></span> <span data-ttu-id="5a74a-120">Über die Richtlinien können Sie eine Regelsammlung erstellen, die für eine oder mehrere juristische Personen gilt.</span><span class="sxs-lookup"><span data-stu-id="5a74a-120">The policies let you create a collection of rules that apply to one or more legal entities.</span></span> <span data-ttu-id="5a74a-121">Innerhalb jeder Richtlinie können Sie jeden der eben erstellten Richtlinienregeltypen für die Vorteilsberechtigung anzeigen.</span><span class="sxs-lookup"><span data-stu-id="5a74a-121">Within each policy, you can view any of the benefit eligibility policy rule types that you created earlier.</span></span> 

<span data-ttu-id="5a74a-122">Sie definieren den Umfang der Regel innerhalb der Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="5a74a-122">You define the scope of the rule within the policy.</span></span> <span data-ttu-id="5a74a-123">Wenn Sie beispielsweise einen Richtlinienregeltyp für die Vorteilsberechtigung mit der Bezeichnung **Führungskraft** erstellen, können Sie die Regel innerhalb dieser Richtlinie definieren.</span><span class="sxs-lookup"><span data-stu-id="5a74a-123">For example, if you create a benefit eligibility policy rule type that is named **Executive**, you can specify what the rule is within that policy.</span></span> <span data-ttu-id="5a74a-124">Hier kann die Regel zum Beispiel angeben, dass jede Position, die das Wort "Führungskraft" enthält, in diese Regel einbezogen werden soll.</span><span class="sxs-lookup"><span data-stu-id="5a74a-124">In this example, the rule might state that any job title that contains the word “executive” should be included in the rule.</span></span> <span data-ttu-id="5a74a-125">Nachdem Sie die Parameter der in der Richtlinie enthaltenen Regel(n) definiert haben, können Sie dem Vorteil eine bestimmte Regel zuweisen.</span><span class="sxs-lookup"><span data-stu-id="5a74a-125">After you've defined the parameters of the rule or rules that are included in the policy, you can assign a specific rule to the benefit.</span></span>

<a name="additional-resources"></a><span data-ttu-id="5a74a-126">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5a74a-126">Additional resources</span></span>
--------

[<span data-ttu-id="5a74a-127">Definieren und verwalten eines Vorteilprogramms</span><span class="sxs-lookup"><span data-stu-id="5a74a-127">Defining and managing a benefit program</span></span>](manage-benefit-program.md)



