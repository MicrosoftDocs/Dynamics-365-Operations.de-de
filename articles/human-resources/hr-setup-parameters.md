---
title: Parameter in Human Resources konfigurieren
description: Dieses Thema erklärt, wie Sie firmenspezifische Parameter in Dynamics 365 Human Resources festlegen.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7c4c93e3d2644a380e3d5d2247961a8b6fb34568
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6052408"
---
# <a name="configure-human-resources-parameters"></a><span data-ttu-id="c875a-103">Parameter in Human Resources konfigurieren</span><span class="sxs-lookup"><span data-stu-id="c875a-103">Configure Human resources parameters</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="c875a-104">Die Einstellungen einiger Human Resources-Parameter sind firmenübergreifend, während die Einstellungen anderer Parameter firmenspezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="c875a-104">The settings of some Human resources parameters are shared across companies, while the settings of other parameters are company-specific.</span></span> <span data-ttu-id="c875a-105">In diesem Thema wird erklärt, wie Sie firmenspezifische Human Resources-Parameter festlegen.</span><span class="sxs-lookup"><span data-stu-id="c875a-105">This topic explains how to set up company-specific Human resources parameters.</span></span>

<span data-ttu-id="c875a-106">Zum Festlegen der Human Resources-Parameter werden zwei Seiten verwendet.</span><span class="sxs-lookup"><span data-stu-id="c875a-106">Two pages are used to set Human resources parameters.</span></span> <span data-ttu-id="c875a-107">Für Parameter, die innerhalb des Unternehmens freigegeben werden, verwenden Sie die Seite **Freigegeben Parameter für Personalverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="c875a-107">For parameters that are shared across companies, you use the **Human resources shared parameters** page.</span></span> <span data-ttu-id="c875a-108">Für Parameter, die unternehmensspezifisch sind (das heißt, die Einstellungen beziehen sich auf ein einzelnes Unternehmen), verwenden Sie die Seite **Personalverwaltungsparameter**.</span><span class="sxs-lookup"><span data-stu-id="c875a-108">For parameters that are company-specific (in other words, the settings apply to a single company), you use the **Human resource parameters** page.</span></span>

![Gehen Sie zu Human Resources-Parameter](./media/hr-employee-self-service-human-resources-parameters.png)

<span data-ttu-id="c875a-110">Auf der Seite **Personalverwaltungsparameter** sind die Einstellungen in sechs Registerkarten unterteilt:</span><span class="sxs-lookup"><span data-stu-id="c875a-110">On the **Human resources parameters** page, the settings are divided among six tabs:</span></span>

- <span data-ttu-id="c875a-111">**Allgemeines**</span><span class="sxs-lookup"><span data-stu-id="c875a-111">**General**</span></span>
- <span data-ttu-id="c875a-112">**Rekrutierung** (diese Registerkarte ist nicht in Dynamics 365 Human Resources enthalten)</span><span class="sxs-lookup"><span data-stu-id="c875a-112">**Recruitment** (this tab isn't included in Dynamics 365 Human Resources)</span></span>
- <span data-ttu-id="c875a-113">**Kompensation**</span><span class="sxs-lookup"><span data-stu-id="c875a-113">**Compensation**</span></span>
- <span data-ttu-id="c875a-114">**Nummernkreise**</span><span class="sxs-lookup"><span data-stu-id="c875a-114">**Number sequences**</span></span>
- <span data-ttu-id="c875a-115">**FMLA**</span><span class="sxs-lookup"><span data-stu-id="c875a-115">**FMLA**</span></span>
- <span data-ttu-id="c875a-116">**Mitarbeiter-Self-Service**</span><span class="sxs-lookup"><span data-stu-id="c875a-116">**Employee self service**</span></span>
- <span data-ttu-id="c875a-117">**Manager-Self-Service**</span><span class="sxs-lookup"><span data-stu-id="c875a-117">**Manager self service**</span></span>
- <span data-ttu-id="c875a-118">**Vergütungsverwaltung**</span><span class="sxs-lookup"><span data-stu-id="c875a-118">**Benefits management**</span></span>
- <span data-ttu-id="c875a-119">**Beurlaubung und Abwesenheit**</span><span class="sxs-lookup"><span data-stu-id="c875a-119">**Leave and absence**</span></span>
- <span data-ttu-id="c875a-120">**Zahlungsmethoden**</span><span class="sxs-lookup"><span data-stu-id="c875a-120">**Payment methods**</span></span>

<span data-ttu-id="c875a-121">Jede Registerkarte enthält Informationen, die sich auf ein einzelnes Unternehmen beziehen.</span><span class="sxs-lookup"><span data-stu-id="c875a-121">Each tab contains information that pertains to a single company.</span></span>

## <a name="general"></a><span data-ttu-id="c875a-122">Allgemeines</span><span class="sxs-lookup"><span data-stu-id="c875a-122">General</span></span>

<span data-ttu-id="c875a-123">Die Einstellungen auf der Registerkarte **Allgemein** definieren die Darstellung von Informationen zu Abwesenheitszeiten, Verletzung und Krankheit und Neueinstellungen.</span><span class="sxs-lookup"><span data-stu-id="c875a-123">The settings on the **General** tab define the appearance of information about absence, injury and illness, and new hires.</span></span> <span data-ttu-id="c875a-124">Die Einstellungen in dieser Registerkarte können auch mehrere Standardeingaben definieren, die angezeigt werden, während Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="c875a-124">The settings on this tab also define some default entries that appear as you work.</span></span> <span data-ttu-id="c875a-125">Auf dieser Registerkarte können Sie insbesondere:</span><span class="sxs-lookup"><span data-stu-id="c875a-125">Specifically, this tab lets you:</span></span>

- <span data-ttu-id="c875a-126">Eine Farbe auswählen, die auf offene Transaktionen zur Abwesenheit angewendet werden soll</span><span class="sxs-lookup"><span data-stu-id="c875a-126">Select a color to apply to open absence transactions</span></span>
- <span data-ttu-id="c875a-127">die Formatvorlage für die Berichte festlegen</span><span class="sxs-lookup"><span data-stu-id="c875a-127">Specify the style sheet to use for reports</span></span>
- <span data-ttu-id="c875a-128">die Integration zwischen Schulungskursen und Abwesenheitsregistrierung aktivieren</span><span class="sxs-lookup"><span data-stu-id="c875a-128">Enable the integration between training courses and absence registration</span></span>
- <span data-ttu-id="c875a-129">Den Abwesenheitscode auswählen, der zur Steuerung dieser Integration verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c875a-129">Select the absence code that is used to control this integration.</span></span>
- <span data-ttu-id="c875a-130">Geben Sie an, wie lange Fälle von Verletzungen und Krankheiten aufbewahrt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c875a-130">Indicate how long to keep injury and illness case incidents.</span></span>
- <span data-ttu-id="c875a-131">Legen Sie die Standard-Identifikationsnummer fest, die angezeigt wird, wenn eine neue Arbeitskraft eingestellt wird.</span><span class="sxs-lookup"><span data-stu-id="c875a-131">Specify the default identification number shown when a new worker is hired.</span></span>

![Registerkarte „Allgemeines“](./media/hr-setup-parameters-general.png)

## <a name="recruitment"></a><span data-ttu-id="c875a-133">Personalbeschaffung</span><span class="sxs-lookup"><span data-stu-id="c875a-133">Recruitment</span></span>

<span data-ttu-id="c875a-134">Die Einstellungen auf der Registerkarte **Rekrutierung** legen die Dokumenttypen fest, die für die Korrespondenz verwendet werden, die automatisch an Bewerber gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="c875a-134">The settings on the **Recruitment** tab define the document types used for correspondence automatically sent to applicants.</span></span> <span data-ttu-id="c875a-135">Sie können auch das Rekrutierungsprojekt angeben, das für Spontanbewerbungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c875a-135">You can also indicate the recruitment project used for unsolicited applications.</span></span>

<span data-ttu-id="c875a-136">Der für die Alterung der Rekrutierungsprojekte definierte Zeitraum bestimmt die Rekrutierungsprojekte, die auf der Kachel **Alterungsprojekte** im Arbeitsbereich **Rekrutierungsmanagement** enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="c875a-136">The period defined for recruitment project aging determines the recruitment projects included on the **Aging projects** tile in the **Recruitment management** workspace.</span></span> <span data-ttu-id="c875a-137">Der für die Bewerbungsfrist-Warnung definierte Zeitraum wird verwendet, um Rekrutierungsprojekte, die sich ihrer Bewerbungsfrist nähern, auf der Kachel **Bewerbungsfrist nähert sich** im Arbeitsbereich **Rekrutierung** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c875a-137">The period defined for the application deadline warning is used to display recruitment projects that are approaching their application deadline on the **Application deadline approaching** tile in the **Recruitment** workspace.</span></span>

<span data-ttu-id="c875a-138">Weitere Informationen zur Rekrutierung finden Sie unter [Bewerbung von Kandidaten](hr-personnel-recruit.md).</span><span class="sxs-lookup"><span data-stu-id="c875a-138">For more information about recruiting, see [Recruit job candidates](hr-personnel-recruit.md).</span></span>

## <a name="compensation"></a><span data-ttu-id="c875a-139">Kompensation</span><span class="sxs-lookup"><span data-stu-id="c875a-139">Compensation</span></span>

<span data-ttu-id="c875a-140">In Dynamics 365 Finance legen die Einstellungen auf der Registerkarte **Vergütung** fest, ob Benutzer bestätigen müssen, dass sie Informationen für einen festen oder variablen Vergütungsplan speichern wollen.</span><span class="sxs-lookup"><span data-stu-id="c875a-140">In Dynamics 365 Finance, the settings on the **Compensation** tab define whether users must confirm that they want to save information for a fixed or variable compensation plan.</span></span> <span data-ttu-id="c875a-141">Wenn Sie **Speichervalidierung aktivieren** wählen, erhalten Benutzer beim Schließen einer vergütungsbezogenen Seite eine Meldung, die sie fragt, ob sie den Datensatz speichern wollen.</span><span class="sxs-lookup"><span data-stu-id="c875a-141">If you select **Enable save validation**, when users close a compensation-related page, they receive a message that asks whether they want to save the record.</span></span> <span data-ttu-id="c875a-142">Einige Seiten im Vergütungsmanagement erlauben es Benutzern nicht, Informationen zu löschen.</span><span class="sxs-lookup"><span data-stu-id="c875a-142">Some pages in Compensation management don't let users delete information.</span></span> <span data-ttu-id="c875a-143">Indem Sie Benutzer auffordern, zu bestätigen, dass sie Informationen speichern möchten, können Sie möglicherweise die Menge der Informationen begrenzen, die gespeichert werden, aber später nicht gelöscht werden können.</span><span class="sxs-lookup"><span data-stu-id="c875a-143">By prompting users to verify that they want to save information, you might be able to limit the amount of information that is saved but can't be deleted later.</span></span> <span data-ttu-id="c875a-144">Wenn Sie **Speichervalidierung aktivieren** deaktivieren, werden Datensätze sofort gespeichert, möglicherweise bevor der Benutzer dazu bereit ist.</span><span class="sxs-lookup"><span data-stu-id="c875a-144">If you clear **Enable save validation**, records save immediately, possibly before the user is ready.</span></span> <span data-ttu-id="c875a-145">Wenn Sie das Leistungsmanagement verwenden, können Sie auf der Registerkarte **Vergütung** auch ein Bewertungsmodell auswählen, das anstelle des Modells, das den Vergütungsplänen zugeordnet ist, bei der Bewertung der Leistung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c875a-145">If you're using Performance management, the **Compensation** tab also lets you select a rating model to use instead of the model assigned to compensation plans when rating performance.</span></span>

<span data-ttu-id="c875a-146">In Human Resources können Sie auf der Registerkarte **Vergütung** wählen, ob Sie den Zugriff auf Vergütungspläne beschränken und eine Standardwährung festlegen wollen.</span><span class="sxs-lookup"><span data-stu-id="c875a-146">In Human Resources, you can use the **Compensation** tab to choose to restrict access to compensation plans and to set a default currency.</span></span>

<span data-ttu-id="c875a-147">Weitere Informationen über Vergütungen finden Sie unter [Übersicht über Vergütungspläne](hr-compensation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c875a-147">For more information about compensation, see [Compensation plans overview](hr-compensation-overview.md).</span></span>

![Registerkarte „Vergütung“](./media/hr-setup-parameters-compensation.png)

## <a name="number-sequences"></a><span data-ttu-id="c875a-149">Nummernkreise</span><span class="sxs-lookup"><span data-stu-id="c875a-149">Number sequences</span></span>

<span data-ttu-id="c875a-150">Die Einstellungen auf der Registerkarte **Nummernkreis** legen die Sequenzen fest, mit denen Artikeln in Human Resources automatisch IDs zugewiesen werden, z.B:</span><span class="sxs-lookup"><span data-stu-id="c875a-150">The settings on the **Number sequence** tab determine the sequences used to automatically assign IDs to items in Human Resources, such as:</span></span>

- <span data-ttu-id="c875a-151">Bewerbungen</span><span class="sxs-lookup"><span data-stu-id="c875a-151">Applications</span></span>
- <span data-ttu-id="c875a-152">Abwesenheitserfassungen</span><span class="sxs-lookup"><span data-stu-id="c875a-152">Absence registrations</span></span>
- <span data-ttu-id="c875a-153">Ergebnisse des Vergütungsprozesses</span><span class="sxs-lookup"><span data-stu-id="c875a-153">Compensation process results</span></span>
- <span data-ttu-id="c875a-154">Fallnummern</span><span class="sxs-lookup"><span data-stu-id="c875a-154">Case numbers</span></span>
- <span data-ttu-id="c875a-155">Kurse</span><span class="sxs-lookup"><span data-stu-id="c875a-155">Courses</span></span>
- <span data-ttu-id="c875a-156">Kurs-Agenden</span><span class="sxs-lookup"><span data-stu-id="c875a-156">Course agendas</span></span>

<span data-ttu-id="c875a-157">Um Nummernkreis-Referenzen und -Codes zu pflegen, verwenden Sie die Listenseite **Nummernkreise** (wählen Sie **Organisationsverwaltung > Nummernkreise > Nummernkreise**).</span><span class="sxs-lookup"><span data-stu-id="c875a-157">To maintain number sequence references and codes, use the **Number sequences** list page (select **Organization administration > Number sequences > Number sequences**).</span></span>

<span data-ttu-id="c875a-158">Weitere Informationen finden Sie unter [Übersicht über Nummernkreise](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="c875a-158">For more information, see [Number sequences overview](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span></span>

> [!NOTE]
> <span data-ttu-id="c875a-159">Die Anzahl der gearbeiteten Stunden kann 1,250 Stunden und eine Beschäftigungsdauer von 12 Monate nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="c875a-159">The number of hours that are worked can't exceed 1,250, and the length of employment can't exceed 12 months.</span></span> <span data-ttu-id="c875a-160">Diese maximalen Werte sind in Übereinstimmung mit dem Bundesgesetz in den USA festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c875a-160">These maximum values are in accordance with federal law in the United States.</span></span>

![Registerkarte Nummernkreise](./media/hr-setup-parameters-number-sequences.png)

## <a name="fmla"></a><span data-ttu-id="c875a-162">FMLA</span><span class="sxs-lookup"><span data-stu-id="c875a-162">FMLA</span></span>

<span data-ttu-id="c875a-163">Auf der Registerkarte FMLA legen Sie die FMLA-Berechtigungsvoraussetzungen und die FMLA-Anspruchsstunden fest.</span><span class="sxs-lookup"><span data-stu-id="c875a-163">On the FMLA tab, you set FMLA eligibility requirements and FMLA entitlement hours.</span></span> <span data-ttu-id="c875a-164">Weitere Informationen finden Sie unter [Urlaub- und Abwesenheitsparameter konfigurieren](hr-leave-and-absence-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c875a-164">For more information, see [Configure leave and absence parameters](hr-leave-and-absence-parameters.md).</span></span>

![Registerkarte FMLA](./media/hr-setup-parameters-fmla.png)

## <a name="employee-self-service"></a><span data-ttu-id="c875a-166">Mitarbeiter-Self-Service</span><span class="sxs-lookup"><span data-stu-id="c875a-166">Employee self service</span></span>

<span data-ttu-id="c875a-167">Die Einstellungen auf der Registerkarte **Mitarbeiter-Self-Service** beeinflussen, wie der Mitarbeiter-Self-Service den Mitarbeitern erscheint.</span><span class="sxs-lookup"><span data-stu-id="c875a-167">The settings on the **Employee self service** tab affect how Employee self service appears to employees.</span></span> <span data-ttu-id="c875a-168">Auf dieser Registerkarte können Sie:</span><span class="sxs-lookup"><span data-stu-id="c875a-168">On this tab, you can:</span></span>

- <span data-ttu-id="c875a-169">Einen Namen für den Arbeitsbereich des Mitarbeiter-Self-Service eingeben</span><span class="sxs-lookup"><span data-stu-id="c875a-169">Enter a name for the Employee self service workspace</span></span>
- <span data-ttu-id="c875a-170">auswählen, welche Informationen ein Manager für Mitarbeiter eingeben kann</span><span class="sxs-lookup"><span data-stu-id="c875a-170">Select which information a manager can enter for employees</span></span>
- <span data-ttu-id="c875a-171">Nützliche Links für Mitarbeiter hinzufügen</span><span class="sxs-lookup"><span data-stu-id="c875a-171">Add useful links for employees</span></span>
- <span data-ttu-id="c875a-172">Mitarbeitern das Hinzufügen oder Bearbeiten von geschäftlichen Kontaktdetails verbieten.</span><span class="sxs-lookup"><span data-stu-id="c875a-172">Restrict employees from adding or editing business contact details.</span></span> <span data-ttu-id="c875a-173">Weitere Informationen finden Sie unter [Bearbeiten von persönlichen Informationen einschränken](hr-employee-self-service-restrict-editing.md).</span><span class="sxs-lookup"><span data-stu-id="c875a-173">For more information, see [Restrict editing of personal information](hr-employee-self-service-restrict-editing.md).</span></span>

<span data-ttu-id="c875a-174">Weitere Informationen zum Festlegen des Mitarbeiter-Self-Service finden Sie unter [Übersicht über den Mitarbeiter- und Manager-Self-Service](hr-employee-manager-self-service-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c875a-174">For more information about setting up Employee self service, see [Employee and Manager self service overview](hr-employee-manager-self-service-overview.md).</span></span>

![Registerkarte Mitarbeiter-Self-Service](./media/hr-setup-parameters-employee-self-service.png)

## <a name="manager-self-service"></a><span data-ttu-id="c875a-176">Manager-Self-Service</span><span class="sxs-lookup"><span data-stu-id="c875a-176">Manager self service</span></span>

<span data-ttu-id="c875a-177">Die Einstellungen auf der Registerkarte **Manager-Self-Service** beeinflussen, was Manager im Manager-Self-Service sehen.</span><span class="sxs-lookup"><span data-stu-id="c875a-177">The settings on the **Manager self service** tab affect what managers see in Manager self service.</span></span> <span data-ttu-id="c875a-178">Auf dieser Registerkarte können Sie die folgenden Optionen konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="c875a-178">On this tab, you can configure the following options:</span></span>

- <span data-ttu-id="c875a-179">Der Bereich für auslaufende Datensätze</span><span class="sxs-lookup"><span data-stu-id="c875a-179">The range for expiring records</span></span>
- <span data-ttu-id="c875a-180">Informationen, die Manager in auslaufenden Datensätzen sehen können</span><span class="sxs-lookup"><span data-stu-id="c875a-180">Information managers can view in expiring records</span></span>
- <span data-ttu-id="c875a-181">Ob Manager offene Positionen für erweiterte Berichte anzeigen können</span><span class="sxs-lookup"><span data-stu-id="c875a-181">Whether managers can view open positions for extended reports</span></span>
- <span data-ttu-id="c875a-182">Ansichten von auslaufenden Arbeitskräften</span><span class="sxs-lookup"><span data-stu-id="c875a-182">Views of exiting workers</span></span>
- <span data-ttu-id="c875a-183">Nützliche Links für Manager</span><span class="sxs-lookup"><span data-stu-id="c875a-183">Useful links for managers</span></span>

<span data-ttu-id="c875a-184">Weitere Informationen zum Einrichten des Manager-Self-Service finden Sie unter [Übersicht über den Mitarbeiter- und Manager-Self-Service](hr-employee-manager-self-service-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c875a-184">For more information about setting up Manager self service, see [Employee and Manager self service overview](hr-employee-manager-self-service-overview.md).</span></span>

![Registerkarte Manager-Self-Service](./media/hr-setup-parameters-manager-self-service.png)

## <a name="benefits-management"></a><span data-ttu-id="c875a-186">Vergütungsverwaltung</span><span class="sxs-lookup"><span data-stu-id="c875a-186">Benefits management</span></span>

<span data-ttu-id="c875a-187">Auf der Registerkarte Manager-Selfservice können Sie E-Mail-Optionen für den Manager-Selfservice konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="c875a-187">On the Benefits management tab, you can configure email options for Benefits management.</span></span> <span data-ttu-id="c875a-188">Informationen zum Festlegen und Verwenden der Vorteilsverwaltung finden Sie unter [Übersicht zur Vorteilsverwaltung](hr-benefits-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c875a-188">For information about setting up and using Benefits management, see [Benefits management overview](hr-benefits-management-overview.md).</span></span>

![Registerkarte Vergütungsverwaltung](./media/hr-setup-parameters-benefits-management.png)

## <a name="leave-and-absence"></a><span data-ttu-id="c875a-190">Beurlaubung und Abwesenheit</span><span class="sxs-lookup"><span data-stu-id="c875a-190">Leave and absence</span></span>

<span data-ttu-id="c875a-191">Informationen zum Festlegen und Verwenden von Urlaub und Abwesenheit finden Sie unter [Übersicht über Urlaub und Abwesenheit](hr-leave-and-absence-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c875a-191">For information about setting up and using Leave and absence, see [Leave and absence overview](hr-leave-and-absence-overview.md).</span></span>

## <a name="payment-methods"></a><span data-ttu-id="c875a-192">Zahlungsmethoden</span><span class="sxs-lookup"><span data-stu-id="c875a-192">Payment methods</span></span>

<span data-ttu-id="c875a-193">Auf der Registerkarte **Zahlungsmethoden** können Sie die von Ihrer Organisation unterstützten Zahlungsmethoden auswählen.</span><span class="sxs-lookup"><span data-stu-id="c875a-193">On the **Payment methods** tab, you can select the payment methods supported by your organization.</span></span> <span data-ttu-id="c875a-194">Weitere Informationen zum Konfigurieren von Vergütungen finden Sie unter [Übersicht über Vergütungspläne](hr-compensation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c875a-194">For more information about configuring compensation, see [Compensation plans overview](hr-compensation-overview.md).</span></span>

![Registerkarte Zahlungsarten](./media/hr-setup-parameters-payment-methods.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]