---
title: Ausgabenrichtlinien definieren
description: In Microsoft Dynamics 365 Finance können Richtlinien festgelegt werden, an die sich die Mitarbeiter beim Eingeben und Einreichen von Spesenabrechnungen und Reiseanforderungen zu halten haben.
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 22504e0e26c025d117f29dee3b59b41d508e7724
ms.sourcegitcommit: 4f90b9ddedf312e75a714e0ec7f7ee5fd43cac6a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/21/2020
ms.locfileid: "3389714"
---
# <a name="define-expense-policies"></a><span data-ttu-id="3d346-103">Ausgabenrichtlinien definieren</span><span class="sxs-lookup"><span data-stu-id="3d346-103">Define expense policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3d346-104">Sie können Richtlinien definieren, an die sich die Mitarbeiter beim Eingeben und Übermitteln von Spesenabrechnungen und Reiseanforderungen zu halten haben.</span><span class="sxs-lookup"><span data-stu-id="3d346-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="3d346-105">Die Implementierung von Ausgabenrichtlinien trägt zu einer Optimierung der Ausgabenverwaltung bei.</span><span class="sxs-lookup"><span data-stu-id="3d346-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="3d346-106">So können Sie beispielsweise eine Richtlinie für Hotelausgaben in New York City einrichten, die festlegt, dass die Hotelkosten pro Übernachtung höchstens EUR 250 betragen dürfen.</span><span class="sxs-lookup"><span data-stu-id="3d346-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="3d346-107">Wenn eine Arbeitskraft eine Spesenabrechnung oder eine Reiseanforderung übermittelt, in der der Übernachtungspreis diesen Betrag übersteigt, meldet das System dies der</span><span class="sxs-lookup"><span data-stu-id="3d346-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="3d346-108">Arbeitskraft, dass der Betrag entsprechend der Richtlinie überschritten wurde.</span><span class="sxs-lookup"><span data-stu-id="3d346-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="3d346-109">Sie können die Meldung konfigurieren, die die Arbeitskraft erhält, wenn Sie die Richtlinie definieren.</span><span class="sxs-lookup"><span data-stu-id="3d346-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="3d346-110">Richtlinienregeln festlegen.</span><span class="sxs-lookup"><span data-stu-id="3d346-110">define the policy.</span></span>      
        
<span data-ttu-id="3d346-111">Sie können drei Arten von Richtlinien definieren:</span><span class="sxs-lookup"><span data-stu-id="3d346-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="3d346-112">Warnung - Ermöglicht der Arbeitskraft, eine Spesenabrechnung oder eine Reiseanforderung zu übermitteln, die Ausgaben werden jedoch markiert für alle genehmigenden Personen</span><span class="sxs-lookup"><span data-stu-id="3d346-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="3d346-113">und für die spätere Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="3d346-113">for later reporting.</span></span>        

- <span data-ttu-id="3d346-114">Fehler – Verlangt, dass die Arbeitskraft vor dem Übermitteln der Spesenabrechnung oder der Reiseanforderung die Ausgaben überarbeiten, um die Einhaltung der Richtlinie zu garantieren.</span><span class="sxs-lookup"><span data-stu-id="3d346-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="3d346-115">Begründung – Erfordert, dass die Arbeitskraft oder ein Manager vor dem Übermitteln der Spesenabrechnung oder der Reiseanforderung eine Begründung für eine Überschreitung des Richtlinienbetrags eingibt.</span><span class="sxs-lookup"><span data-stu-id="3d346-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="3d346-116">Richtlinientipps</span><span class="sxs-lookup"><span data-stu-id="3d346-116">Policy tips</span></span>
<span data-ttu-id="3d346-117">Nachfolgend finden Sie einige Vorschläge, die Sie beim Erstellen neuer Richtlinien für Ausgabenverwaltung unterstützen.</span><span class="sxs-lookup"><span data-stu-id="3d346-117">Here are a few suggestions that can assist you when creating new policies for expense management.</span></span> 
* <span data-ttu-id="3d346-118">Die Wirksamtkein von Richtlinien ist vom Datum abhängig und sie treten nicht in Kraft, wenn die Richtlinie mit einem Datum erstellt wird, das hinter dem Datum der Aufwendung liegt.</span><span class="sxs-lookup"><span data-stu-id="3d346-118">Policies are date effective and won't take effect if the policy is created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="3d346-119">Wenn Sie z. B.heute eine neue Richtlinie erstellen, um maximale Verpflegungsausgaben von 50 US-Dollar zu erzwingen, dann gilt diese Richtlinie für keine vorhandenen Ausgaben, die bis Gestern eingereicht werden.</span><span class="sxs-lookup"><span data-stu-id="3d346-119">For example, if you are creating a new policy today to enforce a maximum meal expense of $50, then any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
* <span data-ttu-id="3d346-120">Bei Erstellung einer Richtlinie für eine Ausgabenkategorie, die aufgeschlüsselt werden kann, sollten Sie eine Bedingung für den Ausgabenpositionstyp hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="3d346-120">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="3d346-121">Einige Richtlinien wie das anfordern eines Belegt, sind möglicherweise für aufgeschlüsselte Positionen nicht sinnvoll und sollten nur auf die Kopfzeile oder eine nicht aufgeschlüsselte Position angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="3d346-121">Some policies such as requiring a receipt may not make sense for itemized lines and should only be applied to the header line or a non-itemized line.</span></span> 
* <span data-ttu-id="3d346-122">Ausgabenverwaltungsrichtlinien werden standardmäßig anhand der Quellenentität bewertet.</span><span class="sxs-lookup"><span data-stu-id="3d346-122">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="3d346-123">Für konzerninterne Szenarien können Sie stattdessen festlegen, dass die Richtlinie anhand der Zielentität (Kreditinstanz) bewertet wird.</span><span class="sxs-lookup"><span data-stu-id="3d346-123">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="3d346-124">Um die Richtlinien für die Zielentität auszuführen, aktivieren Sie die Funktion „Kostenrichtlinie gegen Ausleihen einer juristischen Person bewerten“ im Arbeitsbereich **Funktionsverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="3d346-124">To run the policies against the destination entity, turn on the "Evaluate Expense policy against borrowing legal entity" feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="3d346-125">Wann Richtlinien ausgewertet werden sollten</span><span class="sxs-lookup"><span data-stu-id="3d346-125">When to evaluate policies</span></span>

<span data-ttu-id="3d346-126">In den Parametern der Ausgabenverwaltung finden Sie eine Option, mit der Sie entweder die Ausgabenverwaltungsrichtlinien auswerten könne, wenn eine Position gespeichert wird, oder wenn ein Ausgabenbeleg eingereicht wird.</span><span class="sxs-lookup"><span data-stu-id="3d346-126">In expense management parameters, there is an option to either evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="3d346-127">Wenn Sie sich entscheiden, die Auswertung beim Speichern der Position vorzunehmen, wird sichergestellt, dass Benutzer frühere Sichtbarkeit in die erforderlichen Aufgaben erhalten, um Ihren Ausgabenbericht in einem Zug abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="3d346-127">If you choose to evaluate when a line is saved this ensures that users have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="3d346-128">Andernfalls können Sie die Richtlinienbewertung zurückstellen und Zeit sparen, wenn die Überprüfung am Ende durchgeführt wird, bei der Übermittlung an den Workflow.</span><span class="sxs-lookup"><span data-stu-id="3d346-128">Otherwise, you can delay policy evaluation and save time if you have validation occur at the end, during submission to workflow.</span></span>
