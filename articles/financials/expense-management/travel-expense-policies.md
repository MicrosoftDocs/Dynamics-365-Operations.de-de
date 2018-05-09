---
title: Ausgabenrichtlinien definieren
description: "Sie können Ausgabenrichtlinien definieren, die ihre Arbeitskräfte einhalten müssen, wenn sie in Microsoft Dynamics 365 for Finance and Operations Spesenabrechnungen und Reiseanforderungen eingeben und übermitteln."
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 062d6f01bb07324ad5b8dc6b9fd7617756502c17
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---

# <a name="expense-policies"></a><span data-ttu-id="6c167-103">Ausgabenrichtlinien</span><span class="sxs-lookup"><span data-stu-id="6c167-103">Expense policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6c167-104">Sie können Richtlinien definieren, an die sich die Mitarbeiter beim Eingeben und Übermitteln von Spesenabrechnungen und Reiseanforderungen zu halten haben.</span><span class="sxs-lookup"><span data-stu-id="6c167-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="6c167-105">Die Implementierung von Ausgabenrichtlinien trägt zu einer Optimierung der Ausgabenverwaltung bei.</span><span class="sxs-lookup"><span data-stu-id="6c167-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="6c167-106">So können Sie beispielsweise eine Richtlinie für Hotelausgaben in New York City einrichten, die festlegt, dass die Hotelkosten pro Übernachtung höchstens EUR 250 betragen dürfen.</span><span class="sxs-lookup"><span data-stu-id="6c167-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="6c167-107">Wenn eine Arbeitskraft eine Spesenabrechnung oder eine Reiseanforderung übermittelt, in der der Übernachtungspreis diesen Betrag übersteigt, meldet das System dies der</span><span class="sxs-lookup"><span data-stu-id="6c167-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="6c167-108">Arbeitskraft, dass der Betrag entsprechend der Richtlinie überschritten wurde.</span><span class="sxs-lookup"><span data-stu-id="6c167-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="6c167-109">Sie können die Meldung konfigurieren, die die Arbeitskraft erhält, wenn Sie die Richtlinie definieren.</span><span class="sxs-lookup"><span data-stu-id="6c167-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="6c167-110">Richtlinienregeln festlegen.</span><span class="sxs-lookup"><span data-stu-id="6c167-110">define the policy.</span></span>      
        
<span data-ttu-id="6c167-111">Sie können drei Arten von Richtlinien definieren:</span><span class="sxs-lookup"><span data-stu-id="6c167-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="6c167-112">Warnung - Ermöglicht der Arbeitskraft, eine Spesenabrechnung oder eine Reiseanforderung zu übermitteln, die Ausgaben werden jedoch markiert für alle genehmigenden Personen</span><span class="sxs-lookup"><span data-stu-id="6c167-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="6c167-113">und für die spätere Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="6c167-113">for later reporting.</span></span>        

- <span data-ttu-id="6c167-114">Fehler – Verlangt, dass die Arbeitskraft vor dem Übermitteln der Spesenabrechnung oder der Reiseanforderung die Ausgaben überarbeiten, um die Einhaltung der Richtlinie zu garantieren.</span><span class="sxs-lookup"><span data-stu-id="6c167-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
  - <span data-ttu-id="6c167-115">Begründung – Erfordert, dass die Arbeitskraft oder ein Manager vor dem Übermitteln der Spesenabrechnung oder der Reiseanforderung eine Begründung für eine Überschreitung des Richtlinienbetrags eingibt.</span><span class="sxs-lookup"><span data-stu-id="6c167-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        
 
  <span data-ttu-id="6c167-116">Sie können auch einen Datumsbereich einrichten, für den Ausgabenrichtlinien wirksam sind.</span><span class="sxs-lookup"><span data-stu-id="6c167-116">You can also set up a date range for which expense policies are in effect.</span></span> <span data-ttu-id="6c167-117">Beispielsweise Flugtickets zwischen Dänemark</span><span class="sxs-lookup"><span data-stu-id="6c167-117">For example, airline fares for flights between Denmark</span></span>      
  <span data-ttu-id="6c167-118">und New York City können während der Hauptreisezeit besonders teuer sein.</span><span class="sxs-lookup"><span data-stu-id="6c167-118">and New York City can be expensive during the peak holiday travel season.</span></span> <span data-ttu-id="6c167-119">Sie können eine Flugkostenregel definieren, die die</span><span class="sxs-lookup"><span data-stu-id="6c167-119">You can define a flight expense rule that restricts the</span></span>      
  <span data-ttu-id="6c167-120">Flugkosten nach New York City auf einen Betrag von DKK 5000 festlegt und Sie können angeben, das diese Regeln zwischen 15. März und</span><span class="sxs-lookup"><span data-stu-id="6c167-120">cost of flights to New York City to a limit of DKK 5000, and you can specify that this rule be in effect between March 15 and</span></span>      
  <span data-ttu-id="6c167-121">15. September gilt.</span><span class="sxs-lookup"><span data-stu-id="6c167-121">September 15.</span></span>

