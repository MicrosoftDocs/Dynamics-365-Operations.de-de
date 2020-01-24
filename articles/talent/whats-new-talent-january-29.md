---
title: Neuerungen oder Änderungen in Dynamics 365 Talent (31. Januar 2019)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 Talent entweder neu oder geändert sind.
author: Darinkramer
manager: AnnBe
ms.date: 01/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-01-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: fbbecd4e0f205c2f09ec30548756ff1a43872644
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/06/2019
ms.locfileid: "2899104"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-31-2019"></a><span data-ttu-id="cc781-103">Neuerungen oder Änderungen in Dynamics 365 Talent (31. Januar 2019)</span><span class="sxs-lookup"><span data-stu-id="cc781-103">What's new or changed in Dynamics 365 Talent (January 31, 2019)</span></span>

<span data-ttu-id="cc781-104">In diesem Thema werden die Funktionen beschrieben, die in Dynamics 365 Talent neu oder geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="cc781-104">This topic describes features that are either new or changed in Dynamics 365 Talent.</span></span>

<span data-ttu-id="cc781-105">**Build 8.1.2128**</span><span class="sxs-lookup"><span data-stu-id="cc781-105">**Build 8.1.2128**</span></span>

## <a name="core-hr-changes"></a><span data-ttu-id="cc781-106">Core HR Änderungen</span><span class="sxs-lookup"><span data-stu-id="cc781-106">Core HR Changes</span></span>

### <a name="time-off-taken-on-leave-people-card-doesnt-consider-leave-plan-dates"></a><span data-ttu-id="cc781-107">Freizeit auf Urlaub genommen Leute Karte berücksichtigt nicht Urlaubsplan Daten</span><span class="sxs-lookup"><span data-stu-id="cc781-107">Time off taken on leave people card doesn't consider leave plan dates</span></span>
<span data-ttu-id="cc781-108">Für diejenigen, die Urlaubspläne haben, die nicht auf einem Kalenderjahr laufen, zeigt die Karte **Genommen** jetzt Urlaub an, der im planmäßig definierten Urlaubsjahr genommen wurde.</span><span class="sxs-lookup"><span data-stu-id="cc781-108">For those that have leave plans that don’t run on a calendar year, the **Taken** card now displays time off that’s been taken in the plan-defined leave year.</span></span> <span data-ttu-id="cc781-109">Wenn beispielsweise das Urlaubsjahr eines Unternehmens vom 1. Juni bis zum 30. Mai dauert und ein Mitarbeiter im Dezember 3 Tage frei genommen hat, wird die **Genommen**-Karte am 15. Januar 3 Tage anzeigen.</span><span class="sxs-lookup"><span data-stu-id="cc781-109">For example, if an organization’s leave year is June 1 through May 30 and an employee has taken 3 days off in December, the **Taken** card on January 15, will display 3 days.</span></span> 

### <a name="accrual-amounts-not-matching-tier-date-basis"></a><span data-ttu-id="cc781-110">Abgrenzungsbeträge, die nicht der Tier-Datumsbasis entsprechen.</span><span class="sxs-lookup"><span data-stu-id="cc781-110">Accrual amounts not matching tier date basis</span></span>
<span data-ttu-id="cc781-111">Es wurden neue Urlaubs- und Abwesenheitsoptionen (**Personalparameter**) hinzugefügt, damit Kunden feststellen können, wann die Dienstzeit der Mitarbeiter wirksam ist.</span><span class="sxs-lookup"><span data-stu-id="cc781-111">New options have been added to leave and absence (**Human resources** parameters) to enable customers to determine when employees’ months of service date are effective.</span></span> <span data-ttu-id="cc781-112">Für einige Unternehmen ist das Datum das Ende des Monats, für andere kann es der Beginn des nächsten Monats sein.</span><span class="sxs-lookup"><span data-stu-id="cc781-112">For some organizations, the date is the end of the month, but for others it may be the start of the next month.</span></span> <span data-ttu-id="cc781-113">So kann beispielsweise ein Unternehmen am 31. Dezember Urlaub gewähren, während ein anderes am 1. Januar Urlaub gewähren kann.</span><span class="sxs-lookup"><span data-stu-id="cc781-113">For example, one organization may award time off on December 31, while another may award time off on January 1.</span></span> <span data-ttu-id="cc781-114">Mit dieser Option können Sie wählen, wann der Award stattfinden soll.</span><span class="sxs-lookup"><span data-stu-id="cc781-114">This option will allow you to choose when the award should occur.</span></span> 

### <a name="worker-hire-actions-are-stuck-in-workflow-complete-state"></a><span data-ttu-id="cc781-115">Aktionen zur Einstellung von Arbeitnehmern sind im Zustand "Workflow abgeschlossen" stecken geblieben.</span><span class="sxs-lookup"><span data-stu-id="cc781-115">Worker hire actions are stuck in "Workflow complete" state</span></span>
<span data-ttu-id="cc781-116">Es wurden Änderungen vorgenommen, um ein Problem zu beheben, bei dem eine kleine Anzahl von Workflows mit dem Status "Workflow abgeschlossen" beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="cc781-116">Changes have been made to correct an issue where a small number of workflows finished with a "Workflow complete" status.</span></span> <span data-ttu-id="cc781-117">Neue Workflows sollten nun nach Beendigung des Workflows in den Zustand "Abgeschlossen" übergehen.</span><span class="sxs-lookup"><span data-stu-id="cc781-117">New workflows should now move to a "Completed" state when the workflow finishes.</span></span> <span data-ttu-id="cc781-118">Alle Workflows in einem abgeschlossenen Workflow-Status werden in einen Fehlerstatus überführt, um bei Bedarf eine Aktualisierung oder Entfernung zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="cc781-118">Any workflows in a workflow completed status will be transitioned to an error status to allow for updating or removal if required.</span></span> 
