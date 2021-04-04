---
title: Vergütungsberechtigungsprozess
description: Diese Prozedur zeigt, wie der Leistungberechtigungsprozess arbeitet.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: 3720adf26d2cb942bc5d9f6988641bf5e504a852
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465125"
---
# <a name="benefit-eligibility-process"></a><span data-ttu-id="f8be2-103">Vergütungsberechtigungsprozess</span><span class="sxs-lookup"><span data-stu-id="f8be2-103">Benefit eligibility process</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="f8be2-104">Diese Prozedur zeigt, wie der Leistungberechtigungsprozess arbeitet.</span><span class="sxs-lookup"><span data-stu-id="f8be2-104">This procedure shows how the benefit eligibility process works.</span></span> <span data-ttu-id="f8be2-105">Wenn der Prozess abgeschlossen ist, können Sie die Ergebnisse anzeigen.</span><span class="sxs-lookup"><span data-stu-id="f8be2-105">When the process is complete you can view the results.</span></span> <span data-ttu-id="f8be2-106">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="f8be2-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="f8be2-107">Wechseln Sie zu "Personalverwaltung" > "Leistungen" > "Leistungen".</span><span class="sxs-lookup"><span data-stu-id="f8be2-107">Go to Human resources > Benefits > Benefits.</span></span>
2. <span data-ttu-id="f8be2-108">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="f8be2-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="f8be2-109">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="f8be2-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="f8be2-110">Klicken Sie auf Bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="f8be2-110">Click Edit.</span></span>
5. <span data-ttu-id="f8be2-111">Wählen Sie im Feld "Berechtigung" "Regelbasiert" aus.</span><span class="sxs-lookup"><span data-stu-id="f8be2-111">In the Eligibility field, select 'Rule based'.</span></span>
6. <span data-ttu-id="f8be2-112">Wählen Sie im Feld "Regeltyp" die Leistungrichtlinienregel aus, die Sie auf die Leistung anwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="f8be2-112">In the Rule type field, select the benefit policy rule you would like applied to the benefit.</span></span>
7. <span data-ttu-id="f8be2-113">Klicken Sie im Aktivitätsbereich auf "Vorteil".</span><span class="sxs-lookup"><span data-stu-id="f8be2-113">On the Action Pane, click Benefit.</span></span>
8. <span data-ttu-id="f8be2-114">Klicken Sie auf "Berechtigungsereignis erstellen", um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f8be2-114">Click Create eligibility event to open the drop dialog.</span></span>
9. <span data-ttu-id="f8be2-115">Geben Sie im Feld "Ereignis" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="f8be2-115">In the Event field, type a value.</span></span>
10. <span data-ttu-id="f8be2-116">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="f8be2-116">In the Description field, type a value.</span></span>
11. <span data-ttu-id="f8be2-117">Wählen Sie im Feld "Ereignistyp" die Option "Registrierung öffnen" aus.</span><span class="sxs-lookup"><span data-stu-id="f8be2-117">In the Event type field, select 'Open enrollment'.</span></span>
12. <span data-ttu-id="f8be2-118">Geben Sie im Feld "Startdatum der Disposition" ein Datum und eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="f8be2-118">In the Coverage start date field, enter a date and time.</span></span>
13. <span data-ttu-id="f8be2-119">Geben Sie im Feld "Registrierungsperiode" ein Datum und eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="f8be2-119">In the Enrollment period start date field, enter a date and time.</span></span>
14. <span data-ttu-id="f8be2-120">Geben Sie im Feld "Tage zur Registrierung" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="f8be2-120">In the Days to enroll field, enter a number.</span></span>
15. <span data-ttu-id="f8be2-121">Klicken Sie auf "Ereignis erstellen".</span><span class="sxs-lookup"><span data-stu-id="f8be2-121">Click Create event.</span></span>
16. <span data-ttu-id="f8be2-122">Klicken im Arbeitskraft-Inforegister auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="f8be2-122">Click Add in the Workers FastTab.</span></span>
17. <span data-ttu-id="f8be2-123">Wählen Sie im Feld "Nach Typ anzeigen" die Option "Mitarbeiter" aus.</span><span class="sxs-lookup"><span data-stu-id="f8be2-123">In the Show by type field, select 'Employees'.</span></span>
18. <span data-ttu-id="f8be2-124">Wählen Sie im Feld "Nach juristischer Person anzeigen" die Option "Aktuelle juristische Person" aus.</span><span class="sxs-lookup"><span data-stu-id="f8be2-124">In the Show by legal entity field, select 'Current legal entity'.</span></span>
19. <span data-ttu-id="f8be2-125">Markieren Sie alle Zeilen in der Liste, oder heben Sie die Markierung auf.</span><span class="sxs-lookup"><span data-stu-id="f8be2-125">In the list, mark or unmark all rows.</span></span>
20. <span data-ttu-id="f8be2-126">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f8be2-126">Click OK.</span></span>
21. <span data-ttu-id="f8be2-127">Prozess anklicken.</span><span class="sxs-lookup"><span data-stu-id="f8be2-127">Click Process.</span></span>
22. <span data-ttu-id="f8be2-128">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f8be2-128">Click OK.</span></span>
23. <span data-ttu-id="f8be2-129">Aktualisieren Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="f8be2-129">Refresh the page.</span></span>
24. <span data-ttu-id="f8be2-130">Klicken Sie auf "Ergebnisse anzeigen".</span><span class="sxs-lookup"><span data-stu-id="f8be2-130">Click Show results.</span></span>
25. <span data-ttu-id="f8be2-131">Öffnen Sie den Spaltenfilter "Status".</span><span class="sxs-lookup"><span data-stu-id="f8be2-131">Open Status column filter.</span></span>
26. <span data-ttu-id="f8be2-132">Von A nach Z sortieren</span><span class="sxs-lookup"><span data-stu-id="f8be2-132">Sort A to Z</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]