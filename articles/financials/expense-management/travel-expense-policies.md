---
title: Ausgabenrichtlinien definieren
description: "Sie können Ausgabenrichtlinien definieren, die ihre Arbeitskräfte einhalten müssen, wenn sie in Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, Spesenabrechnungen und Reiseanforderungen eingeben und übermitteln."
author: saraschi2
manager: AnnBe
ms.date: 09/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi2
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 9a5ce1a3b6519b510c9f5aa5618ab91f77a2d91a
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="expense-policies"></a><span data-ttu-id="3e356-103">Ausgabenrichtlinien</span><span class="sxs-lookup"><span data-stu-id="3e356-103">Expense policies</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="3e356-104">Sie können Richtlinien definieren, an die sich die Mitarbeiter beim Eingeben und Übermitteln von Spesenabrechnungen und Reiseanforderungen zu halten haben.</span><span class="sxs-lookup"><span data-stu-id="3e356-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span> <span data-ttu-id="3e356-105">Die Implementierung von Ausgabenrichtlinien trägt zu einer Optimierung der Ausgabenverwaltung bei.</span><span class="sxs-lookup"><span data-stu-id="3e356-105">Implementing expense policies can help you manage expenses effectively.</span></span> 

<span data-ttu-id="3e356-106">So können Sie beispielsweise eine Richtlinie für Hotelausgaben in New York City einrichten, die festlegt, dass die Hotelkosten pro Übernachtung höchstens EUR 250 betragen dürfen.</span><span class="sxs-lookup"><span data-stu-id="3e356-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span> <span data-ttu-id="3e356-107">Wenn eine Arbeitskraft eine Spesenabrechnung oder Reiseanforderung mit einem höheren Übernachtungspreis einreicht, wird die Arbeitskraft mittels einer entsprechenden Meldung darauf hingewiesen, dass der per Richtlinie festgelegte Betrag überschritten wurde.</span><span class="sxs-lookup"><span data-stu-id="3e356-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="3e356-108">Sie können die Meldung konfigurieren, die die Arbeitskraft erhält, wenn Sie die Richtlinie definieren.</span><span class="sxs-lookup"><span data-stu-id="3e356-108">You can configure the message that the worker will receive when you define the policy.</span></span> 

<span data-ttu-id="3e356-109">Sie können drei Arten von Richtlinien definieren:</span><span class="sxs-lookup"><span data-stu-id="3e356-109">You can define three types of policies:</span></span> 

 - <span data-ttu-id="3e356-110">Warnung - Ermöglicht der Arbeitskraft, eine Spesenabrechnung oder eine Reiseanforderung zu übermitteln, die Ausgaben werden jedoch markiert für alle genehmigenden Personen</span><span class="sxs-lookup"><span data-stu-id="3e356-110">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>  
 <span data-ttu-id="3e356-111">und für die spätere Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="3e356-111">for later reporting.</span></span> 
 - <span data-ttu-id="3e356-112">Fehler – Verlangt, dass die Arbeitskraft vor dem Übermitteln der Spesenabrechnung oder der Reiseanforderung die Ausgaben überarbeiten, um die Einhaltung der Richtlinie zu garantieren.</span><span class="sxs-lookup"><span data-stu-id="3e356-112">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span> 
 - <span data-ttu-id="3e356-113">Begründung – Erfordert, dass die Arbeitskraft oder ein Manager vor dem Übermitteln der Spesenabrechnung oder der Reiseanforderung eine Begründung für eine Überschreitung des Richtlinienbetrags eingibt.</span><span class="sxs-lookup"><span data-stu-id="3e356-113">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span> 

<span data-ttu-id="3e356-114">Sie können auch einen Datumsbereich einrichten, für den Ausgabenrichtlinien wirksam sind.</span><span class="sxs-lookup"><span data-stu-id="3e356-114">You can also set up a date range for which expense policies are in effect.</span></span> <span data-ttu-id="3e356-115">Zum Beispiel sind die Kosten für Flugtickets zwischen Dänemark und New York während der Hauptreisezeit besonders hoch.</span><span class="sxs-lookup"><span data-stu-id="3e356-115">For example, airline fares for flights between Denmark and New York City can be expensive during the peak holiday travel season.</span></span> <span data-ttu-id="3e356-116">Sie können eine Flugkostenregel definieren, die die Kosten von Flügen nach New York City auf das Limit von DKK 5000 beschränkt, und Sie können angeben, dass diese Regel zwischen dem 15. März und dem 15. September gilt.</span><span class="sxs-lookup"><span data-stu-id="3e356-116">You can define a flight expense rule that restricts the cost of flights to New York City to a limit of DKK 5000, and you can specify that this rule be in effect between March 15 and September 15.</span></span> 

