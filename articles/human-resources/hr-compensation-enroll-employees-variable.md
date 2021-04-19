---
title: Registrieren eines Mitarbeiters in einem Plan für variable Vergütung
description: Der Leiter für Vergütungen/Bezüge kann Mitarbeiter in einem Plan für variable Vergütung registrieren, um Bargeld- und bargeldlose Prämien für Mitarbeiter zu berechnen.
author: andreabichsel
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HRMCompVarEnrollEmpl, HcmCompensationWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f31790dc9389eaed125f69e4039d06a8b28bcc8b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793728"
---
# <a name="enroll-an-employee-in-a-variable-compensation-plan"></a><span data-ttu-id="f7f7d-103">Registrieren eines Mitarbeiters in einem Plan für variable Vergütung</span><span class="sxs-lookup"><span data-stu-id="f7f7d-103">Enroll an employee in a variable compensation plan</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="f7f7d-104">Der Leiter für Vergütungen/Bezüge kann Mitarbeiter in einem Plan für variable Vergütung registrieren, um Bargeld- und bargeldlose Prämien für Mitarbeiter zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="f7f7d-104">The Compensation and Benefits manager can enroll employees in variable compensation plans to calculate cash and non-cash awards for employees.</span></span> <span data-ttu-id="f7f7d-105">Für dieses Verfahren wird vorausgesetzt, dass ein Plan für variable Vergütung mit dem Feld "Registrierung aktivieren" auf "Ja" festgelegt wurde und dass Berechtigungsregeln für diesen Plan für variable Vergütung erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="f7f7d-105">This procedure assumes that a variable compensation plan has been created with the Enable enrolment field set to Yes, and that eligibility rules have been created for that variable compensation plan.</span></span> <span data-ttu-id="f7f7d-106">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="f7f7d-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="f7f7d-107">Um das Verfahren zu starten, gehen Sie zu "Personalverwaltung" > "Arbeitskräfte" > "Mitarbeiter" > "Vergütung" > "Variabler Plan registrieren".</span><span class="sxs-lookup"><span data-stu-id="f7f7d-107">To begin this procedure, go to Human resources > Workers > Employees > Compensation > Variable plan enrolment</span></span>

1. <span data-ttu-id="f7f7d-108">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="f7f7d-108">Click New.</span></span>
2. <span data-ttu-id="f7f7d-109">Klicken Sie im Feld "Plan" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f7f7d-109">In the Plan field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f7f7d-110">Die Plansuche wird gefiltert, um nur die Pläne für variable Vergütung anzuzeigen, für die der Mitarbeiter auf Grundlage der Berechtigungsregeln freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="f7f7d-110">The plan lookup will be filtered to only show the variable compensation plans that the employee is eligible for based on the eligibility rules.</span></span>  
3. <span data-ttu-id="f7f7d-111">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="f7f7d-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="f7f7d-112">Schalten Sie die Erweiterung des Abschnitts "Allgemein" ein/aus.</span><span class="sxs-lookup"><span data-stu-id="f7f7d-112">Toggle the expansion of the General section.</span></span>
5. <span data-ttu-id="f7f7d-113">Geben Sie im Feld "Gültigkeitsdatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="f7f7d-113">In the Effective date field, enter a date.</span></span>
6. <span data-ttu-id="f7f7d-114">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="f7f7d-114">Click Save.</span></span>
7. <span data-ttu-id="f7f7d-115">Schalten Sie die Erweiterung des Abschnitts "Überschreibungen" ein/aus.</span><span class="sxs-lookup"><span data-stu-id="f7f7d-115">Toggle the expansion of the Overrides section.</span></span>
    * <span data-ttu-id="f7f7d-116">Optional kann ein Einstellungsregeldatum festgelegt werden, um das Einstellungsdatum für einen Mitarbeiter zu überschreiben, wenn die Einstellungsregel für den ausgewählten variablen Plan "Prozent" ist.</span><span class="sxs-lookup"><span data-stu-id="f7f7d-116">Optionally, a hire rule date can be set to override the hire date for an employee when the hire rule specified for the selected variable plan is Percent.</span></span>  
    * <span data-ttu-id="f7f7d-117">Wenn der variable Plan ein prozentualer Anteil des Basisplans ist, kann der Prämienprozentsatz für den Mitarbeiter überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="f7f7d-117">If the variable plan is a percent of basis plan, the award percentage can be overridden for the employee.</span></span> <span data-ttu-id="f7f7d-118">Wenn der variable Vergütungsplan ein Einheitenanzahlsplan ist, kann die Anzahl der Einheiten für den Mitarbeiter überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="f7f7d-118">If the variable compensation plan is a number of units plan, the number of units can be overridden for the employee.</span></span>  
    * <span data-ttu-id="f7f7d-119">Wenn dem Mitarbeiter als Pauschalbetrag für seine Zulage gezahlt wird, kann der Betrag hier festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f7f7d-119">If the employee should be given a flat amount for their award, the amount can be set here.</span></span>  
8. <span data-ttu-id="f7f7d-120">Schalten Sie die Erweiterung des Abschnitts "Überschreibungen in Organisation" ein/aus.</span><span class="sxs-lookup"><span data-stu-id="f7f7d-120">Toggle the expansion of the Organizational overrides section.</span></span>
    * <span data-ttu-id="f7f7d-121">Wenn die Leistung des Mitarbeiters, die Leistung unterschiedlicher Abteilungen oder einer anderen als die der Position des Mitarbeiters zugewiesene Abteilung berücksichtigt werden soll, kann die Abteilung überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="f7f7d-121">If the employee's performance should take into consideration, the performance of different departments, or a department other than the one assigned on the employee's position, the department can be overridden.</span></span> <span data-ttu-id="f7f7d-122">Die Spalte "Prozent" sollte sich auf 100 summieren.</span><span class="sxs-lookup"><span data-stu-id="f7f7d-122">The Percent column should total 100.</span></span>  



[!INCLUDE[footer-include](../includes/footer-banner.md)]