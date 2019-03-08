---
title: Neuerungen oder Änderungen in Dynamics 365 for Talent Core HR (11. Januar 2019)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 for Talent Core HR entweder neu oder geändert sind.
author: Darinkramer
manager: AnnBe
ms.date: 01/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-01-11
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 6e7edf52db663c7ad28f316c324d68e57bf6699a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "304551"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-january-11-2019"></a><span data-ttu-id="8b45e-103">Neuerungen oder Änderungen in Dynamics 365 for Talent Core HR (11. Januar 2019)</span><span class="sxs-lookup"><span data-stu-id="8b45e-103">What's new or changed in Dynamics 365 for Talent Core HR (January 11, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8b45e-104">**Build 8.1.2100**</span><span class="sxs-lookup"><span data-stu-id="8b45e-104">**Build 8.1.2100**</span></span>

<span data-ttu-id="8b45e-105">In diesem Thema werden die Funktionen beschrieben, die in Core HR entweder neu oder geändert sind.</span><span class="sxs-lookup"><span data-stu-id="8b45e-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="changes"></a><span data-ttu-id="8b45e-106">Änderungen</span><span class="sxs-lookup"><span data-stu-id="8b45e-106">Changes</span></span>

### <a name="validate-leave-requests-by-forecasting-available-balance"></a><span data-ttu-id="8b45e-107">Validierung von Urlaubsanträgen durch Prognose des verfügbaren Saldos</span><span class="sxs-lookup"><span data-stu-id="8b45e-107">Validate leave requests by forecasting available balance</span></span>
<span data-ttu-id="8b45e-108">Die in diesem Release vorgenommenen Änderungen ermöglichen es den Mitarbeitern, zukünftige Urlaubszeiten zu beantragen, ohne von ihrem aktuellen Saldo abzuziehen.</span><span class="sxs-lookup"><span data-stu-id="8b45e-108">Changes made in this release allow employees to request future leave time without subtracting from their current balance.</span></span> <span data-ttu-id="8b45e-109">Für zukünftige Anfragen werden Standard-Workflows verwendet.</span><span class="sxs-lookup"><span data-stu-id="8b45e-109">Standard workflows will be used for any future requests made.</span></span> <span data-ttu-id="8b45e-110">Weitere Informationen finden Sie unter [Zeit basierend auf Freizeit auf Grundlage der gearbeiteten Stunden abgrenzen](leave-accrue-hours-worked.md).</span><span class="sxs-lookup"><span data-stu-id="8b45e-110">For more information, read [Accrue time off based on hours worked](leave-accrue-hours-worked.md).</span></span>

### <a name="view-forecasted-leave-balance-in-ess-and-people"></a><span data-ttu-id="8b45e-111">Ansicht der prognostizierten Urlaubsbilanz in ESS und People</span><span class="sxs-lookup"><span data-stu-id="8b45e-111">View forecasted leave balance in ESS and People</span></span>
<span data-ttu-id="8b45e-112">Diese Funktion ermöglicht die Anzeige von Salden für zukünftige Urlaubszeiträume durch HR, Manager und Mitarbeiter.</span><span class="sxs-lookup"><span data-stu-id="8b45e-112">This feature enables viewing of balances for future leave periods by HR, managers, and employees.</span></span> <span data-ttu-id="8b45e-113">Mitarbeiter können zukünftige Salden im **Mitarbeiter-Self-Service**-Arbeitsbereich einsehen und die Personalabteilung hat über den **Mitarbeiterarbeitsbereich** Zugriff auf die gleichen Informationen.</span><span class="sxs-lookup"><span data-stu-id="8b45e-113">Employees can view future balances in the **Employee Self-Service** workspace and HR has access to the same information using the **People** workspace.</span></span>

### <a name="notifications-for-changing-leave-balances"></a><span data-ttu-id="8b45e-114">Benachrichtigungen zur Änderung von Urlaubssalden</span><span class="sxs-lookup"><span data-stu-id="8b45e-114">Notifications for changing leave balances</span></span>
<span data-ttu-id="8b45e-115">Die Urlaubssalden zeigen den aktuellen Saldo des Mitarbeiters an.</span><span class="sxs-lookup"><span data-stu-id="8b45e-115">Leave balances will display the employees current balance.</span></span> <span data-ttu-id="8b45e-116">Zukünftige Salden sind auf den **Mitarbeiter-Self-Service**-**Arbeitsbereichen** verfügbar, indem Sie ein "Ab-Datum" eingeben, um den prognostizierten Saldo zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="8b45e-116">Future balances are available on the **Employee Self-Service** and **People** workspaces by entering an “as of date” to calculate the forecasted balance.</span></span>

<span data-ttu-id="8b45e-117">Die Navigation zur Anzeige der prognostizierten Salden in den folgenden Bereichen wurde hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="8b45e-117">Navigation has been added to view forecasted balances in the following areas:</span></span>
  - <span data-ttu-id="8b45e-118">**Urlaub**-Karte im **Mitarbeiter-Self-Service**-Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="8b45e-118">**Time off** card on the **Employee Self-Service** workspace.</span></span>
  - <span data-ttu-id="8b45e-119">**Urlaubs- und Abwesenheitskarte** im **Manager-Self-Service**-Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="8b45e-119">**Leave and absence** card on the **Manager Self-Service** workspace.</span></span>
  - <span data-ttu-id="8b45e-120">**Urlaubs- und Abwesenheitsseite** im **Mitarbeiter-Self-Service**-Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="8b45e-120">**Leave and absence** page on the **People** workspace.</span></span>

### <a name="allow-decimals-for-variable-compensation-plans-cash-plans"></a><span data-ttu-id="8b45e-121">Dezimalstellen für variable Vergütungspläne (Cash-Pläne) zulassen</span><span class="sxs-lookup"><span data-stu-id="8b45e-121">Allow decimals for Variable compensation plans (Cash plans)</span></span>
<span data-ttu-id="8b45e-122">Variable Barzuteilungen und -pläne haben nun die zusätzliche Flexibilität für Beträge und Überschreibungen für Werte mit Dezimalbeträgen.</span><span class="sxs-lookup"><span data-stu-id="8b45e-122">Variable cash awards and plans now have the additional flexibility for amounts and overrides for values with decimal amounts.</span></span>

### <a name="unable-to-change-the-dates-on-variable-comp-enrollments-after-the-plan-is-saved"></a><span data-ttu-id="8b45e-123">Es ist nicht möglich, die Daten der Anmeldungen für variable Komponenten nach dem Speichern des Plans zu ändern.</span><span class="sxs-lookup"><span data-stu-id="8b45e-123">Unable to change the dates on Variable comp enrollments after the plan is saved</span></span>
<span data-ttu-id="8b45e-124">Diese Änderung ermöglicht es, das Planenddatum nach dem Speichern des Plans zu aktualisieren (zu verlängern oder zu verfallen).</span><span class="sxs-lookup"><span data-stu-id="8b45e-124">This change allows for the plan end date to be updated (extended or expired) after the plan has been saved.</span></span> <span data-ttu-id="8b45e-125">Sie können Pläne unabhängig vom Start- und Enddatum weiterhin aktivieren oder deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="8b45e-125">You can still activate or de-activate plans independent of start and end dates.</span></span>

### <a name="payroll-information-available-when-assigned-the-payroll-admin-security-role"></a><span data-ttu-id="8b45e-126">Abrechnungsinformationen, die bei Zuweisung der Sicherheitsrolle Personalsachbearbeiter verfügbar sind</span><span class="sxs-lookup"><span data-stu-id="8b45e-126">Payroll information available when assigned the Payroll admin security role</span></span>
<span data-ttu-id="8b45e-127">Die Rolle Sachbearbeiter Abrechnung wurde aktualisiert, um während des Antragsprozesses Zugriff auf die Abrechnungsinformationen zu haben.</span><span class="sxs-lookup"><span data-stu-id="8b45e-127">The Payroll Administrator role has been updated to have access to the payroll information during the request process.</span></span>

### <a name="employee-self-service--position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a><span data-ttu-id="8b45e-128">Mitarbeiter-Self-Service | Details der Positionshierarchie aus der Kachel führt nicht zum übergeordneten Knoten</span><span class="sxs-lookup"><span data-stu-id="8b45e-128">Employee self-service | Position hierarchy drill-down from tile fails to get parent node</span></span>
<span data-ttu-id="8b45e-129">Es wurden Änderungen vorgenommen, um einen Fehler zu beheben, der beim Hinzufügen der Positionshierarchie zu neuen Arbeitsbereichen und beim Navigieren innerhalb der Organisationsstruktur aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="8b45e-129">Changes have been made to eliminate an error that occurred when adding the position hierarchy to new workspaces and navigating within the organizational structure.</span></span>

### <a name="new-validation-message-when-personnel-number-sequence-is-in-use"></a><span data-ttu-id="8b45e-130">Neue Validierungsmeldung bei Verwendung der Personalnummernreihenfolge</span><span class="sxs-lookup"><span data-stu-id="8b45e-130">New validation message when personnel number sequence is in use</span></span>
<span data-ttu-id="8b45e-131">Es wurde eine Änderung vorgenommen, um zu klären, worum es geht, wenn Sie einen Mitarbeiter einstellen und die nächste Personalnummer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8b45e-131">A change has been made to clarify what the issue is when you hire an employee and the next personnel number is in use.</span></span>

### <a name="employee-self-service-workspace-selected-as-the-initial-startup-page"></a><span data-ttu-id="8b45e-132">Mitarbeiter-Self-Service-Arbeitsbereich, der als Einstiegsseite ausgewählt wurde</span><span class="sxs-lookup"><span data-stu-id="8b45e-132">Employee self-service workspace selected as the initial startup page</span></span>
<span data-ttu-id="8b45e-133">Wenn der **Mitarbeiter-Self-Service**-Arbeitsbereich als Einstiegsseite für einen Benutzer ausgewählt ist und diesem Benutzer nicht die Mitarbeiterrolle zugewiesen ist, leitet das System zum Standard-Dashboard um.</span><span class="sxs-lookup"><span data-stu-id="8b45e-133">When the **Employee self-service** workspace is selected as the initial startup page for a user and that user is not assigned the employee role, the system will redirect to the default dashboard.</span></span>

### <a name="termination-reason-code-updates-position-assignment-record"></a><span data-ttu-id="8b45e-134">Abbruchgrund Code aktualisiert Positionszuordnungssatz</span><span class="sxs-lookup"><span data-stu-id="8b45e-134">Termination reason code updates position assignment record</span></span>
<span data-ttu-id="8b45e-135">Der Kündigungsgrund aktualisiert nun die Planstellenzuordnung, wenn ein Mitarbeiter gekündigt und die Planstelle beendet wird.</span><span class="sxs-lookup"><span data-stu-id="8b45e-135">The termination reason code will now update the position assignment when terminating an employee and ending the position.</span></span> 
