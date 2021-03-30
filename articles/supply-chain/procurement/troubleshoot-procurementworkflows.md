---
title: Fehlerbehebung bei Beschaffungsworkflows
description: In diesem Thema wird beschrieben, wie Sie Probleme beheben, die bei der Arbeit mit Beschaffungsworkflows auftreten können.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: d5d688c5769a62580e48908117d0562b26eab10a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222824"
---
# <a name="troubleshoot-procurement-and-sourcing-workflows"></a><span data-ttu-id="e5061-103">Fehlerbehebung bei Beschaffungsworkflows</span><span class="sxs-lookup"><span data-stu-id="e5061-103">Troubleshoot procurement and sourcing workflows</span></span>

<span data-ttu-id="e5061-104">In diesem Thema wird beschrieben, wie Sie Probleme beheben, die bei der Arbeit mit Beschaffungsworkflows auftreten können.</span><span class="sxs-lookup"><span data-stu-id="e5061-104">This topic describes how to fix issues that you might encounter while you work with procurement and sourcing workflows.</span></span>

## <a name="error-when-re-submitting-a-purchase-order-to-the-workflow-after-a-change-changes-to-purchase-order-x-are-allowed-only-in-a-draft-state-when-change-management-is-activated"></a><span data-ttu-id="e5061-105">Fehler beim erneuten Übermitteln einer Bestellung an den Workflow nach einer Änderung: „Änderungen an Bestellung X sind nur in einem Entwurfsstatus zulässig, wenn das Änderungsmanagement aktiviert ist.“</span><span class="sxs-lookup"><span data-stu-id="e5061-105">Error when re-submitting a purchase order to the workflow after a change: "Changes to purchase order X are allowed only in a Draft state when change management is activated"</span></span>

<span data-ttu-id="e5061-106">Dieses Problem tritt nur auf, wenn sich die Bestellung in einem *Bestätigt*-Zustand befand, bevor Sie Änderungen angefordert haben.</span><span class="sxs-lookup"><span data-stu-id="e5061-106">This issue occurs only if the purchase order was in a *Confirmed* state before you requested changes.</span></span> <span data-ttu-id="e5061-107">Wenn Sie Änderungen anfordern, während sich die Bestellung in einem *Genehmigt*-Zustand befindet, kann der Workflow erfolgreich verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="e5061-107">If you request changes while the purchase order is in an *Approved* state, the workflow can be processed successfully.</span></span>

### <a name="error-description"></a><span data-ttu-id="e5061-108">Fehlerbeschreibung</span><span class="sxs-lookup"><span data-stu-id="e5061-108">Error description</span></span>

<span data-ttu-id="e5061-109">Der folgende Fehler tritt im Workflow auf, wenn eine Bestellung nach einer Änderung erneut übermittelt wird:</span><span class="sxs-lookup"><span data-stu-id="e5061-109">The following error occurs in the workflow when a purchase order is resubmitted after a change:</span></span>

> <span data-ttu-id="e5061-110">Gestoppt (Fehler): X++ Ausnahme: Änderungen an der Bestellung PO0000569 sind nur im Status Entwurf zulässig, wenn die Änderungsverwaltung aktiviert ist unter</span><span class="sxs-lookup"><span data-stu-id="e5061-110">Stopped (error): X++ Exception: Changes to purchase order PO0000569 are only allowed in state Draft when change management is activated at</span></span><br>
<span data-ttu-id="e5061-111">SysWorkflowParticipantProvider-Auflösung</span><span class="sxs-lookup"><span data-stu-id="e5061-111">SysWorkflowParticipantProvider-resolve</span></span><br>
<span data-ttu-id="e5061-112">SysWorkflowParticipantProvider-resolveParticipants</span><span class="sxs-lookup"><span data-stu-id="e5061-112">SysWorkflowParticipantProvider-resolveParticipants</span></span><br>
<span data-ttu-id="e5061-113">SysWorkflowServiceProvider-resolveParticipant</span><span class="sxs-lookup"><span data-stu-id="e5061-113">SysWorkflowServiceProvider-resolveParticipant</span></span><br>
<span data-ttu-id="e5061-114">SysWorkflowQueue-resume</span><span class="sxs-lookup"><span data-stu-id="e5061-114">SysWorkflowQueue-resume</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e5061-115">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="e5061-115">Issue resolution</span></span>

<span data-ttu-id="e5061-116">Dieses Problem kann aufgrund von Inkonsistenzen bei der Verteilung von Bestellungen auftreten.</span><span class="sxs-lookup"><span data-stu-id="e5061-116">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="e5061-117">So entsperren Sie dieses Problem und setzen die Bestellung auf den *Entwurf*-Zustand zurück. Gehen Sie zu **Beschaffung \> Periodische Aufgaben \> Bereinigen \> Zurücksetzen der Bestellverteilung**.</span><span class="sxs-lookup"><span data-stu-id="e5061-117">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="e5061-118">Weitere Informationen finden Sie im folgenden Blog-Beitrag: [Beheben von Bestellungsverteilungsfehlern in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="e5061-118">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

<span data-ttu-id="e5061-119">Das Problem wird behoben durch [diesen Artikel in der Microsodft Wissensdatenbank (KB)](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138).</span><span class="sxs-lookup"><span data-stu-id="e5061-119">The issue will be fixed through [this Microsoft Knowledge Base (KB) article](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138).</span></span>

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a><span data-ttu-id="e5061-120">Eine oder mehrere Buchhaltungsverteilungen sind entweder über- oder unterverteilt.</span><span class="sxs-lookup"><span data-stu-id="e5061-120">One or more accounting distributions are either over-distributed or under-distributed.</span></span>

<span data-ttu-id="e5061-121">Dieses Problem kann aufgrund von Inkonsistenzen bei der Verteilung von Bestellungen auftreten.</span><span class="sxs-lookup"><span data-stu-id="e5061-121">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="e5061-122">So entsperren Sie dieses Problem und setzen die Bestellung auf den *Entwurf*-Zustand zurück. Gehen Sie zu **Beschaffung \> Periodische Aufgaben \> Bereinigen \> Zurücksetzen der Bestellverteilung**.</span><span class="sxs-lookup"><span data-stu-id="e5061-122">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="e5061-123">Weitere Informationen finden Sie im folgenden Blog-Beitrag: [Beheben von Bestellungsverteilungsfehlern in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="e5061-123">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="if-a-delivery-remainder-is-canceled-on-a-purchase-order-where-change-management-is-turned-on-the-purchase-order-goes-to-a-confirmed-state"></a><span data-ttu-id="e5061-124">Wenn eine verbleibende Liefermenge für eine Bestellung storniert wird, für die das Änderungsmanagement aktiviert ist, wechselt die Bestellung in den Status Bestätigt.</span><span class="sxs-lookup"><span data-stu-id="e5061-124">If a delivery remainder is canceled on a purchase order where change management is turned on, the purchase order goes to a Confirmed state.</span></span>

### <a name="issue-description"></a><span data-ttu-id="e5061-125">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="e5061-125">Issue description</span></span>

<span data-ttu-id="e5061-126">Bei einer Bestellung, die dem Änderungsmanagement unterliegt, wird die Bestellung, wenn die einzige angeforderte Änderung die Stornierung einer verbleibenden Liefermenge bei einer oder mehreren Positionen ist, direkt an den Zustand *Bestätigt* weitergeleitet, wann sie genehmigt wurde, und es wird kein Journal erstellt.</span><span class="sxs-lookup"><span data-stu-id="e5061-126">For a purchase order that is subject to change management, if the only change that is requested is the cancellation of a delivery remainder on one or more of the lines, the purchase order will go directly to a *Confirmed* state when it's approved, and no journal will be created.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e5061-127">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="e5061-127">Issue resolution</span></span>

<span data-ttu-id="e5061-128">Die Stornierung einer verbleibenden Liefermenge hat keine Auswirkungen auf den Inhalt des Bestätigungsjournals.</span><span class="sxs-lookup"><span data-stu-id="e5061-128">Cancellation of a delivery remainder doesn't affect the contents of the confirmation journal.</span></span> <span data-ttu-id="e5061-129">Diese Funktionalität sollte verwendet werden, wenn die Position teilweise zugegangen ist, und die verbleibende Liefermenge sollte im Prozessschritt storniert werden, nachdem die Bestellung beim Lieferanten bestätigt wurde.</span><span class="sxs-lookup"><span data-stu-id="e5061-129">This functionality should be used when the line has been partially received, and the remainder quality should be canceled in the process step after the purchase order has been confirmed with the vendor.</span></span>

<span data-ttu-id="e5061-130">Sollte dies in der Bestellbestätigung berücksichtigt werden, sollte die Menge in der Bestellposition angepasst werden, sodass die Bestätigung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="e5061-130">If this should be reflected on the purchase order confirmation, the quantity should be adjusted on the purchase order line so that the confirmation will be required.</span></span> <span data-ttu-id="e5061-131">Wenn alternativ nichts in der Position empfangen wurde, kann die Menge entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="e5061-131">Alternatively, if nothing has been received on the line, the quantity can be removed.</span></span> <span data-ttu-id="e5061-132">In diesem Fall ist eine erneute Bestätigung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e5061-132">In this case, reconfirmation will be required.</span></span>

## <a name="canceled-purchase-orders-appear-in-the-draft-list-in-the-purchase-order-preparation-workspace"></a><span data-ttu-id="e5061-133">Stornierte Bestellungen werden in der Entwurfsliste im Arbeitsbereich für die Bestellvorbereitung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e5061-133">Canceled purchase orders appear in the draft list in the Purchase order preparation workspace.</span></span>

### <a name="issue-description"></a><span data-ttu-id="e5061-134">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="e5061-134">Issue description</span></span>

<span data-ttu-id="e5061-135">Nachdem Sie Bestellungen storniert haben, die im *Bestätigt*-Zustand waren, erscheinen die stornierten Bestellungen im **Bestellvorbereitung**-Arbeitsbereich weiterhin in der Liste der Bestellentwürfe.</span><span class="sxs-lookup"><span data-stu-id="e5061-135">After you cancel purchase orders that were in a *Confirmed* state, the canceled purchase orders still appear in the list of draft purchase orders in the **Purchase order preparation** workspace.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e5061-136">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="e5061-136">Issue resolution</span></span>

<span data-ttu-id="e5061-137">Dieses Problem tritt nur bei Bestellungen auf, die dem Änderungsmanagement unterliegen.</span><span class="sxs-lookup"><span data-stu-id="e5061-137">This issue occurs only for purchase orders that are subject to change management.</span></span> <span data-ttu-id="e5061-138">Dies liegt daran, dass die Stornierung als eine Änderung angesehen wird, die genehmigt werden muss.</span><span class="sxs-lookup"><span data-stu-id="e5061-138">It occurs because the cancellation is considered a change that must be approved.</span></span> <span data-ttu-id="e5061-139">Die Genehmigung kann automatisch vom System erfolgen.</span><span class="sxs-lookup"><span data-stu-id="e5061-139">The approval can be done automatically by the system.</span></span> <span data-ttu-id="e5061-140">Daher besteht der Prozess darin, die stornierte Bestellung an den Genehmigungsworkflow zu senden, damit sie in einen *Genehmigt*-Zustand wechseln kann.</span><span class="sxs-lookup"><span data-stu-id="e5061-140">Therefore, the process is to submit the canceled purchase order to the approval workflow so that it can go to an *Approved* state.</span></span> <span data-ttu-id="e5061-141">Ab diesem Zeitpunkt erscheint die Bestellung nicht mehr im **Bestellvorbereitung**-Arbeitsbereich in der Liste der Bestellentwürfe.</span><span class="sxs-lookup"><span data-stu-id="e5061-141">At that point, the purchase order will no longer appear in the list of draft purchase orders in the **Purchase order preparation** workspace.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]