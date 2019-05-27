---
title: Ausgabenrichtlinien definieren
description: In Microsoft Dynamics 365 for Finance and Operations können Richtlinien festgelegt werden, an die sich die Mitarbeiter beim Eingeben und Einreichen von Spesenabrechnungen und Reiseanforderungen zu halten haben.
author: ryansandness
manager: AnnBe
ms.date: 04/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9f0ff56f0ff106bc168b6a27612e08743a539a07
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1514438"
---
# <a name="expense-policies"></a><span data-ttu-id="2abee-103">Ausgabenrichtlinien</span><span class="sxs-lookup"><span data-stu-id="2abee-103">Expense policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2abee-104">Sie können Richtlinien definieren, an die sich die Mitarbeiter beim Eingeben und Übermitteln von Spesenabrechnungen und Reiseanforderungen zu halten haben.</span><span class="sxs-lookup"><span data-stu-id="2abee-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="2abee-105">Die Implementierung von Ausgabenrichtlinien trägt zu einer Optimierung der Ausgabenverwaltung bei.</span><span class="sxs-lookup"><span data-stu-id="2abee-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="2abee-106">So können Sie beispielsweise eine Richtlinie für Hotelausgaben in New York City einrichten, die festlegt, dass die Hotelkosten pro Übernachtung höchstens EUR 250 betragen dürfen.</span><span class="sxs-lookup"><span data-stu-id="2abee-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="2abee-107">Wenn eine Arbeitskraft eine Spesenabrechnung oder eine Reiseanforderung übermittelt, in der der Übernachtungspreis diesen Betrag übersteigt, meldet das System dies der</span><span class="sxs-lookup"><span data-stu-id="2abee-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="2abee-108">Arbeitskraft, dass der Betrag entsprechend der Richtlinie überschritten wurde.</span><span class="sxs-lookup"><span data-stu-id="2abee-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="2abee-109">Sie können die Meldung konfigurieren, die die Arbeitskraft erhält, wenn Sie die Richtlinie definieren.</span><span class="sxs-lookup"><span data-stu-id="2abee-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="2abee-110">Richtlinienregeln festlegen.</span><span class="sxs-lookup"><span data-stu-id="2abee-110">define the policy.</span></span>      
        
<span data-ttu-id="2abee-111">Sie können drei Arten von Richtlinien definieren:</span><span class="sxs-lookup"><span data-stu-id="2abee-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="2abee-112">Warnung - Ermöglicht der Arbeitskraft, eine Spesenabrechnung oder eine Reiseanforderung zu übermitteln, die Ausgaben werden jedoch markiert für alle genehmigenden Personen</span><span class="sxs-lookup"><span data-stu-id="2abee-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="2abee-113">und für die spätere Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="2abee-113">for later reporting.</span></span>        

- <span data-ttu-id="2abee-114">Fehler – Verlangt, dass die Arbeitskraft vor dem Übermitteln der Spesenabrechnung oder der Reiseanforderung die Ausgaben überarbeiten, um die Einhaltung der Richtlinie zu garantieren.</span><span class="sxs-lookup"><span data-stu-id="2abee-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="2abee-115">Begründung – Erfordert, dass die Arbeitskraft oder ein Manager vor dem Übermitteln der Spesenabrechnung oder der Reiseanforderung eine Begründung für eine Überschreitung des Richtlinienbetrags eingibt.</span><span class="sxs-lookup"><span data-stu-id="2abee-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

# <a name="policy-tips"></a><span data-ttu-id="2abee-116">Richtlinientipps</span><span class="sxs-lookup"><span data-stu-id="2abee-116">Policy tips</span></span>
<span data-ttu-id="2abee-117">Nachfolgend finden Sie einige Vorschläge, die Sie beim Erstellen neuer Richtlinien für Ausgabenverwaltung unterstützen.</span><span class="sxs-lookup"><span data-stu-id="2abee-117">Here are a few suggestions that can assist you whe creating new policies for expense management.</span></span> 
* <span data-ttu-id="2abee-118">Die Wirksamtkein von Richtlinien ist vom Datum abhängig und sie treten nicht in Kraft, wenn die Richtlinie mit einem Datum erstellt wird, das hinter dem Datum der Aufwendung liegt.</span><span class="sxs-lookup"><span data-stu-id="2abee-118">Policies are date effective and won't take effect if the policy is created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="2abee-119">Wenn Sie z. B.heute eine neue Richtlinie erstellen, um maximale Verpflegungsausgaben von 50 US-Dollar zu erzwingen, dann gilt diese Richtlinie für keine vorhandenen Ausgaben, die bis Gestern eingereicht werden.</span><span class="sxs-lookup"><span data-stu-id="2abee-119">For example, if you are creating a new policy today to enforce a maximum meal expense of $50, then any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
* <span data-ttu-id="2abee-120">Bei Erstellung einer Richtlinie für eine Ausgabenkategorie, die aufgeschlüsselt werden kann, sollten Sie eine Bedingung für den Ausgabenpositionstyp hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="2abee-120">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="2abee-121">Einige Richtlinien wie das anfordern eines Belegt, sind möglicherweise für aufgeschlüsselte Positionen nicht sinnvoll und sollten nur auf die Kopfzeile oder eine nicht aufgeschlüsselte Position angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="2abee-121">Some policies such as requiring a receipt may not make sense for itemized lines and should only be applied to the header line or a non-itemized line.</span></span> 

# <a name="when-to-evaluate-policies"></a><span data-ttu-id="2abee-122">Wann Richtlinien ausgewertet werden sollten</span><span class="sxs-lookup"><span data-stu-id="2abee-122">When to evaluate policies</span></span>

<span data-ttu-id="2abee-123">In den Parametern der Ausgabenverwaltung finden Sie eine Option, mit der Sie entweder die Ausgabenverwaltungsrichtlinien auswerten könne, wenn eine Position gespeichert wird, oder wenn ein Ausgabenbeleg eingereicht wird.</span><span class="sxs-lookup"><span data-stu-id="2abee-123">In expense management parameters, there is an option to either evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="2abee-124">Wenn Sie sich entscheiden, die Auswertung beim Speichern der Position vorzunehmen, wird sichergestellt, dass Benutzer frühere Sichtbarkeit in die erforderlichen Aufgaben erhalten, um Ihren Ausgabenbericht in einem Zug abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="2abee-124">If you choose to evaluate when a line is saved this ensures that users have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="2abee-125">Andernfalls können Sie die Richtlinienbewertung zurückstellen und Zeit sparen, wenn die Überprüfung am Ende durchgeführt wird, bei der Übermittlung an den Workflow.</span><span class="sxs-lookup"><span data-stu-id="2abee-125">Otherwise, you can delay policy evaluation and save time if you have validation occur at the end, during submission to workflow.</span></span>
