---
title: Einen Mitarbeiters in einem Plan für eine feste Vergütung registrieren
description: Der Leiter für Vergütungen/Bezüge kann Mitarbeiter zu Plänen für feste Vergütung zuweisen, um ihren Grundlohn zu verwalten.
author: kherr75
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMCompFixedEmpl, HRMCompFixedEmplActionDialog, HcmPositionLookup, HRMCompRefPointLookup
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c9c11292feec06a53cd4426a25bfb2aaac7de3e8
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "353332"
---
# <a name="enroll-an-employee-in-a-fixed-compensation-plan"></a><span data-ttu-id="3d019-103">Einen Mitarbeiters in einem Plan für eine feste Vergütung registrieren</span><span class="sxs-lookup"><span data-stu-id="3d019-103">Enroll an employee in a fixed compensation plan</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3d019-104">Der Leiter für Vergütungen/Bezüge kann Mitarbeiter zu Plänen für feste Vergütung zuweisen, um ihren Grundlohn zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="3d019-104">The compensation and benefits manager can assign employees to fixed compensation plans to manage their base pay.</span></span> <span data-ttu-id="3d019-105">Für dieses Verfahren wird vorausgesetzt, dass ein fester Plan erstellt wurde und aktiv ist und dass Berechtigungsregeln für den Plan festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="3d019-105">This procedure assumes that a fixed plan has been created and is active, and that eligibility rules have been set for the plan.</span></span> <span data-ttu-id="3d019-106">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="3d019-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="3d019-107">Um das Verfahren zu starten, gehen Sie zu "Personalverwaltung" > "Arbeitskräfte" > "Mitarbeiter"  > "Vergütung" > "Fester Plan"</span><span class="sxs-lookup"><span data-stu-id="3d019-107">To begin the procedure, go to Human resources > Workers > Employees > Compensation > Fixed plan</span></span>

1. <span data-ttu-id="3d019-108">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="3d019-108">Click New.</span></span>
2. <span data-ttu-id="3d019-109">Wählen Sie im Feld "Aktion" eine Aktivität bezüglich fester Vergütung vom Typ "Einstellen/Neu einstellen" aus, um die Änderung in der Mitarbeitervergütung zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="3d019-109">In the Action field, select a Fixed compensation action of type Hire/Rehire to describe the change in the employee's compensation.</span></span>
3. <span data-ttu-id="3d019-110">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="3d019-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="3d019-111">Klicken Sie im Feld "Position" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="3d019-111">In the Position field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="3d019-112">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="3d019-112">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="3d019-113">Die Ebene, die angezeigt wird, stammt aus der Vergütungsstufe des Einzelvorgangs in der Position.</span><span class="sxs-lookup"><span data-stu-id="3d019-113">The level that's displayed is from the Compensation Level of the Job on the Position.</span></span> <span data-ttu-id="3d019-114">Die Ebene muss für den Einzelvorgang festgelegt werden, bevor dem Mitarbeiter eine Vergütung zugewiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="3d019-114">The level must be set on the Job before compensation can be assigned to the employee.</span></span>  
6. <span data-ttu-id="3d019-115">Wählen Sie im Feld "Plan" den Plan für feste Vergütung für den Mitarbeiter aus.</span><span class="sxs-lookup"><span data-stu-id="3d019-115">In the Plan field, select the fixed compensation plan for the employee.</span></span> <span data-ttu-id="3d019-116">Die Plansuche wird gefiltert, um nur die Pläne anzuzeigen, für die der Mitarbeiter auf Grundlage der Berechtigungsregeln freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="3d019-116">The Plan lookup is filtered to show only the plans that the employee is eligible for based on the Eligibility rules.</span></span>
7. <span data-ttu-id="3d019-117">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="3d019-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="3d019-118">Die Gültigkeits- und die Ablaufdaten für die Vergütung werden standardmäßig auf das Start- und Enddatum für die Positionszuweisung der Arbeitskraft festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3d019-118">The Effective and Expiration dates for the compensation default from the start and end dates for the worker's position assignment.</span></span> <span data-ttu-id="3d019-119">Sie können diese Daten bei Bedarf ändern.</span><span class="sxs-lookup"><span data-stu-id="3d019-119">You can adjust these dates as needed.</span></span>  
    * <span data-ttu-id="3d019-120">Wenn der Plan mit fester Vergütung ein Schrittplan ist, wählen Sie den Schritt aus, der den korrekten Lohnsatz für den Mitarbeiter enthält.</span><span class="sxs-lookup"><span data-stu-id="3d019-120">If the Fixed compensation plan is a step plan, select the step containing the correct pay rate for the employee.</span></span> <span data-ttu-id="3d019-121">Wenn der Plan mit fester Vergütung ein gradueller oder flexibler Plan ist, geben Sie den Lohnsatz für den Mitarbeiter ein.</span><span class="sxs-lookup"><span data-stu-id="3d019-121">If the fixed compensation plan is a grade or a band plan, enter the pay rate for the employee.</span></span> <span data-ttu-id="3d019-122">Der Lohnsatz wird gegen die Toleranzeinstellungen für den Plan und die minimalen und maximalen Referenzpunkte für die Vergütungsstufe des Einzelvorgangs geprüft.</span><span class="sxs-lookup"><span data-stu-id="3d019-122">The pay rate will be validated against the tolerance settings for the plan, and the minimum and maximum reference points for the job's compensation level.</span></span>  
8. <span data-ttu-id="3d019-123">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3d019-123">Click OK.</span></span>

