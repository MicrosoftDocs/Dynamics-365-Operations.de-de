---
title: Erstellen von Affordable Care Act-(ACA)-Berichten
description: Die Berichterstattung nach dem Affordable Care Act (ACA) generiert die Formulare 1095-B und 1095-C zur Unterstützung des Teils **Arbeitgebermandat** des Affordable Care Act.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 055de1f0ff3f8fd4fadba0a685fd703b9d19d918
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805993"
---
# <a name="generate-aca-reports"></a><span data-ttu-id="f226a-103">ACA-Berichte generieren</span><span class="sxs-lookup"><span data-stu-id="f226a-103">Generate ACA reports</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="f226a-104">Die Berichterstattung nach dem Affordable Care Act (ACA) generiert die Formulare 1095-B und 1095-C zur Unterstützung des Teils **Arbeitgebermandat** des Affordable Care Act.</span><span class="sxs-lookup"><span data-stu-id="f226a-104">Affordable Care Act (ACA) reporting generates forms 1095-B and 1095-C in support of the **Employer Mandate** portion of the Affordable Care Act.</span></span>

> [!NOTE]
> <span data-ttu-id="f226a-105">Die ACA-Berichterstattung ist nur für juristische Personen in den USA aktiviert.</span><span class="sxs-lookup"><span data-stu-id="f226a-105">ACA reporting is only enabled for legal entities in the United States.</span></span>

## <a name="getting-started"></a><span data-ttu-id="f226a-106">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="f226a-106">Getting started</span></span>

<span data-ttu-id="f226a-107">Um Informationen für die Formulare 1095-B und 1095-C zu verfolgen, müssen Sie zunächst eine oder mehrere Dispositionssteuerungsgruppen für Affordable Care erstellen.</span><span class="sxs-lookup"><span data-stu-id="f226a-107">To track information for forms 1095-B and 1095-C, you must first create one or more Affordable care coverage groups.</span></span> <span data-ttu-id="f226a-108">Affordable Care-Dispositionssteuerungsgruppe geben Folgendes an:</span><span class="sxs-lookup"><span data-stu-id="f226a-108">Affordable Care coverage groups indicate:</span></span>

- <span data-ttu-id="f226a-109">Das Dispositionsangebot für einen Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="f226a-109">The offer of coverage for an employee</span></span>
- <span data-ttu-id="f226a-110">Der Arbeitnehmeranteil an der niedrigsten monatlichen Prämie, wenn die Kosten über der Bundesarmutsgrenze liegen</span><span class="sxs-lookup"><span data-stu-id="f226a-110">The employee’s share of the lowest cost monthly premium, if the cost is above the federal poverty line</span></span>
- <span data-ttu-id="f226a-111">Safe Harbor, der gegebenenfalls vom Arbeitgeber genutzt wird</span><span class="sxs-lookup"><span data-stu-id="f226a-111">Safe Harbor used by the employer, if applicable</span></span>

<span data-ttu-id="f226a-112">Mit Affordable Care Act-Gruppen können Sie die Informationen für diese Felder zu verwalten, ohne alle Mitarbeiterdatensätze mit gleichen Bedingungen ändern zu müssen.</span><span class="sxs-lookup"><span data-stu-id="f226a-112">Affordable Care coverage groups allow you to manage the information for these fields without changing every employee record where the conditions are the same.</span></span> <span data-ttu-id="f226a-113">Sie können leicht Affordable Care-Dispositionssteuerungsgruppen mit der Option **Massenzuweisung** auf der Seite einem oder mehreren Mitarbeitern zuweisen.</span><span class="sxs-lookup"><span data-stu-id="f226a-113">You can easily assign Affordable Care coverage groups to one or more employees by using the **Mass assign** option on the page.</span></span>

## <a name="maintaining-multiple-versions-of-a-coverage-group"></a><span data-ttu-id="f226a-114">Mehrere Versionen einer Dispositionssteuerungsgruppe aufrecht halten</span><span class="sxs-lookup"><span data-stu-id="f226a-114">Maintaining multiple versions of a coverage group</span></span>

<span data-ttu-id="f226a-115">Sie können mehrere Versionen einer beliebigen Dispositionssteuerungsgruppe beibehalten.</span><span class="sxs-lookup"><span data-stu-id="f226a-115">You can maintain multiple versions of any coverage group.</span></span> <span data-ttu-id="f226a-116">Mit dieser Funktion können Sie Änderungen vornehmen, ohne eine neue Gruppe erstellen und Mitarbeiter neu zuweisen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="f226a-116">This functionality allows you to make changes without having to create a new group and reassign employees to it.</span></span> 

<span data-ttu-id="f226a-117">Nachdem Sie ACA-Dispositionssteuergruppen erstellt haben, können Sie die Gruppen massenhaft Mitarbeitern mit der Option **Massenzuweisung** zuweisen.</span><span class="sxs-lookup"><span data-stu-id="f226a-117">After you’ve created ACA coverage groups, you can mass assign the groups to employees with the **Mass assignment** option.</span></span> <span data-ttu-id="f226a-118">Sie können auch individuell angeben, ob ACA-Informationen nachverfolgt und gemeldet werden sollen, und einen Mitarbeiter einer Affordable Care-Dispositionssteuergruppe zuordnen.</span><span class="sxs-lookup"><span data-stu-id="f226a-118">You can also individually indicate whether to track and report ACA information, and assign an employee to an Affordable Care coverage group.</span></span>

<span data-ttu-id="f226a-119">Sie müssen einige Informationen zur ACA-Disposition nicht nachverfolgen, z. B. für Teilzeitbeschäftigte.</span><span class="sxs-lookup"><span data-stu-id="f226a-119">You don't need to track some ACA coverage information, such as for part-time employees.</span></span> <span data-ttu-id="f226a-120">Stellen Sie in diesem Fall das Feld **Berichterstattung melden** auf **Nein**.</span><span class="sxs-lookup"><span data-stu-id="f226a-120">In this case, set the **Report coverage** field to **No**.</span></span> <span data-ttu-id="f226a-121">Obwohl Sie jeden Mitarbeiter mit nachverfolgbaren ACA-Informationen einer Affordable Care-Dispositionssteuerungsgruppe zuordnen müssen, können Sie die folgenden Optionen für Monate mit unterschiedlichen Werten ändern:</span><span class="sxs-lookup"><span data-stu-id="f226a-121">Although you must assign each employee with trackable ACA information to an Affordable Care coverage group, you can still change the following options for months with different values:</span></span>

- <span data-ttu-id="f226a-122">**Abdeckungsangebot**</span><span class="sxs-lookup"><span data-stu-id="f226a-122">**Offer of coverage**</span></span>
- <span data-ttu-id="f226a-123">**Mitarbeiteranteil an den Kosten**</span><span class="sxs-lookup"><span data-stu-id="f226a-123">**Employee share of cost**</span></span>
- <span data-ttu-id="f226a-124">**Safe Harbor**</span><span class="sxs-lookup"><span data-stu-id="f226a-124">**Safe Harbor**</span></span>

<span data-ttu-id="f226a-125">Um Ausnahmen für Affordable Care-Dispositionssteuerungsgruppenwerte einzugeben, wählen Sie den Link **Affordable Care-Disposition** auf der Seite **Details zur Arbeitskraft**, unter dem Abschnitt **Zusätzliche Informationen** auf der Registerkarte **Mitarbeiter**.</span><span class="sxs-lookup"><span data-stu-id="f226a-125">To enter exceptions for Affordable Care coverage group values, select the **Affordable Care Coverage** link on the **Worker detail** page under the **Additional information** section on the **Employment tab**.</span></span>

## <a name="reporting-health-care-coverage"></a><span data-ttu-id="f226a-126">Melden von Gesundheitsvorsorgeabdeckung</span><span class="sxs-lookup"><span data-stu-id="f226a-126">Reporting health care coverage</span></span>

<span data-ttu-id="f226a-127">Neben der Nachverfolgung, ob Vollzeitmitarbeitern Krankenversicherungsschutz angeboten wird, ob der Arbeitgeber eine vom Arbeitgeber geförderten selbstversicherten Krankenversicherungsschutz, für den der Mitarbeiter registriert ist, (unabhängig davon, ob sie Vollzeit- oder Teilzeitbeschäftigt sind) anbietet, müssen Zusatzinformationen im 1095-C gemeldet werden.</span><span class="sxs-lookup"><span data-stu-id="f226a-127">In addition to tracking health insurance coverage offered to full-time employees, if the employer offers employer-sponsored self-insured health coverage for which the employee is enrolled (regardless of whether their employment status is full-time or part-time), additional information needs to be reported on the 1095-C.</span></span> <span data-ttu-id="f226a-128">Jeder Mitarbeiter (einschließlich abhängiger), die von Arbeitgeber-geförderten Vorteilspläne abgedeckt sind, muss in dem Bericht für die Monate einbezogen werden, die sie abgedeckt waren.</span><span class="sxs-lookup"><span data-stu-id="f226a-128">Each employee (including dependents) covered by the employer-sponsored benefit plans needs to be included on the report for the months they were covered.</span></span> 

<span data-ttu-id="f226a-129">Sie können angeben, ob jeder Vorteilsplan angegeben werden muss, indem Sie das Kontrollkästchen **ACA meldepflichtig** aktivieren.</span><span class="sxs-lookup"><span data-stu-id="f226a-129">You can indicate whether or not each benefit plan must be reported by selecting the **ACA reportable** check box.</span></span>

<span data-ttu-id="f226a-130">Wenn Mitarbeiter darüber hinaus ausgewählt haben, irgendwelche ihrer abhängigen Personen unter einem Vorteil abdecken zu lassen, können Sie auf der Seite **Vorteile verwalten** das Datum angeben, zu dem die Unterhaltsberechtigten für jeden Mitarbeiter abgedeckt wurden.</span><span class="sxs-lookup"><span data-stu-id="f226a-130">In addition, if employees have chosen to have any of their dependents covered under a benefit, you can indicate the dates the dependent was covered for each employee on the **Maintain benefits** page.</span></span> <span data-ttu-id="f226a-131">Um anzugeben dass der Unterhaltsberechtigte unter dem Vorteil abgedeckt wird, wählen Sie im Aktivitätsbereich des Inforegisters **Unterhaltsberechtigte** die Schaltfläche **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="f226a-131">To indicate that the dependent is covered under the benefit, select the **Edit** button in the action pane of the **Dependents** fast tab.</span></span>

<span data-ttu-id="f226a-132">Auf der Seite **Manager des Dispositionsdatums für Unterhaltsberechtigte** können Sie den Zeitraum angeben, zu dem der Unterhaltsberechtigte durch die Vergütung abgedeckt wurde.</span><span class="sxs-lookup"><span data-stu-id="f226a-132">On the **Dependent coverage date manager** page, you can indicate the dates the dependent was covered by the benefit.</span></span> <span data-ttu-id="f226a-133">Das Eingeben von Daten auf dieser Seite aktiviert automatisch das Kontrollkästchen **Abgedeckt** auf der Seite **Vergütungen verwalten**.</span><span class="sxs-lookup"><span data-stu-id="f226a-133">Entering dates on this page will automatically select the **Covered** checkbox on the **Maintain benefits** page.</span></span>

## <a name="generate-1095-b-and-1095-c-forms"></a><span data-ttu-id="f226a-134">1095-B- und 1095-C-Formulare generieren</span><span class="sxs-lookup"><span data-stu-id="f226a-134">Generate 1095-B and 1095-C forms</span></span>

<span data-ttu-id="f226a-135">Sie können Formulare 1095-B und mit 1095-C im Produkt erstellen und sie an jeden der Mitarbeiter verteilen.</span><span class="sxs-lookup"><span data-stu-id="f226a-135">You can also generate 1095-B and 1095-C forms from within the product, and distribute them to each of your employees.</span></span> <span data-ttu-id="f226a-136">Das System kann auch elektronisch 1095-C-Formulare und die 1094-C-IRS-Übertragungsdateien generieren.</span><span class="sxs-lookup"><span data-stu-id="f226a-136">The system can also electronically generate 1095-C forms and the 1094-C IRS transmittal files.</span></span>  

<span data-ttu-id="f226a-137">Wenn Sie das Formular 1095-C generieren, geben Sie das jeweilige Geschäftsjahr ein und geben Sie an, ob Sozialversicherungsnummern maskiert werden.</span><span class="sxs-lookup"><span data-stu-id="f226a-137">When generating the 1095-C form, enter the appropriate tax year and indicate if social security numbers should be masked.</span></span> <span data-ttu-id="f226a-138">Wenn Sie 1095-C Formulare für mehr als 500 Mitarbeiter drucken, erhalten Sie mehr als eine PDF-Datei.</span><span class="sxs-lookup"><span data-stu-id="f226a-138">If you're printing 1095-C forms for more than 500 employees, you'll receive more than one PDF file.</span></span> <span data-ttu-id="f226a-139">Es wird empfohlen, dass Sie **Maximale Dateigröße** im Fenster **Parameter der Dokumentverwaltung** auf 150 MB erhöhen.</span><span class="sxs-lookup"><span data-stu-id="f226a-139">It’s recommended that you increase the **Maximum file size** in the **Document management parameters** window to 150 MB.</span></span>

## <a name="viewing-information"></a><span data-ttu-id="f226a-140">Informationen anzeigen</span><span class="sxs-lookup"><span data-stu-id="f226a-140">Viewing information</span></span>

<span data-ttu-id="f226a-141">Sie können die Seite **Deckung für Affordable Care Act für Arbeitskraft** verwenden, um festzustellen, welche Mitarbeiter jeder Dispositionssteuerungsgruppe zugewiesen wurden, welche Mitarbeiter im Bericht nicht eingeschlossen werden müssen und welche Mitarbeiter nicht zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="f226a-141">You can use the **Worker Affordable Care coverage** page to see which employees have been assigned to each coverage group, which employees don’t need to be included on a report, and which employees are unassigned.</span></span>

<span data-ttu-id="f226a-142">Wurden irgendwelche der Standardwerte der Affordable Care-Dispositionssteuerungsgruppe überschrieben, wird ein Sternchen neben dem geänderten Wert angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f226a-142">If any of the default values from the Affordable Care coverage group have been overridden, an asterisk will appear next to the value that was changed.</span></span> <span data-ttu-id="f226a-143">Wenn die Werte für alle 12 Monate identisch sind und nicht überschrieben wurden, wird der Wert in der Spalte **Alle 12 Monate** ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="f226a-143">If the values for all 12 months are the same and haven’t been overridden, the value will print in the **All 12 months** column.</span></span>

<span data-ttu-id="f226a-144">Sie können auch das Anfragefenster verwenden, um zu verstehen, welche Mitarbeiter als nicht ACA-meldepflichtig gekennzeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="f226a-144">You can also use the inquiry window to understand which employees have been flagged as not ACA reportable.</span></span> <span data-ttu-id="f226a-145">Sie müssen nicht nachverfolgen, ob ihnen Versicherungsschutz angeboten wurde, und müssen ihnen Ende des Jahres keinen 1095-C ausstellen.</span><span class="sxs-lookup"><span data-stu-id="f226a-145">You don’t need to track whether coverage was offered to them and won't need to issue a 1095-C to them at the end of the year.</span></span> <span data-ttu-id="f226a-146">Wählen Sie **Nicht ACA meldepflichtig** im Feld **Filtern nach** aus, um eine Liste aller Mitarbeiter zu erstellen, die keinen 1095-C erhalten.</span><span class="sxs-lookup"><span data-stu-id="f226a-146">Select **Not ACA reportable** in the **Filter by** field to generate a list of all employees who won't receive a 1095-C.</span></span>

<span data-ttu-id="f226a-147">Zusätzlich können Sie alle Mitarbeiter anzeigen, die nicht zugewiesen sind (das Feld **ACA-Berichtsdisposition** ist leer) oder die einer Affordable Care-Dispositionssteuerungsgruppe zugewiesen wurden, die für das im Feld **Jahr** ausgewählte Jahr abgelaufen ist.</span><span class="sxs-lookup"><span data-stu-id="f226a-147">In addition, you can view any employees who are unassigned (the **ACA Report coverage** field is empty) or who have been assigned to an Affordable Care coverage group that is expired for the year selected in the **Year** field.</span></span>

<span data-ttu-id="f226a-148">Sie können Mitarbeiterlisten exportieren, die mithilfe einer der Filteroptionen in Excel generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="f226a-148">You can export lists of employees that were generated using any of the filtering options to Excel.</span></span>

<span data-ttu-id="f226a-149">Wenn Sie versicherte Personen melden müssen, weil Sie selbstversicherten Versicherungsschutz bieten, können Sie Unterhaltsberechtigte anzeigen, die im Rahmen von Vorteilsplänen versichert sind, die als **ACA-meldepflichtig** gekennzeichnet sind.</span><span class="sxs-lookup"><span data-stu-id="f226a-149">If you need to report covered individuals because you provide self-insured coverage, you can view any dependents covered under benefit plans marked as **ACA reportable**.</span></span> <span data-ttu-id="f226a-150">Wählen Sie im Aktionsbereich **Disposition für Unterhaltsberechtigte anzeigen** aus.</span><span class="sxs-lookup"><span data-stu-id="f226a-150">Select **View Dependent coverage** on the action pane.</span></span>

> [!NOTE]
> <span data-ttu-id="f226a-151">Nur Vorteilspläne, die als **ACA-meldepflichtig** gekennzeichnet sind, werden im Anfragefenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f226a-151">Only benefit plans marked as **ACA reportable** display in the inquiry window.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]