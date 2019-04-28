---
title: Die Lohnintegration zwischen Talent und Dayforce konfigurieren
description: In diesem Thema wird erläutert, wie Sie die Integration zwischen Microsoft Dynamics 365 for Talent und Ceridian Dayforce konfigurieren, damit Sie den Zahlungslauf verarbeiten können.
author: andreabichsel
manager: AnnBe
ms.date: 03/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9a88bf61dbb12520b555ceb7363b1c646d95386e
ms.sourcegitcommit: 204e4554e409c39fbbf7b273ad138ce2809931a8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/26/2019
ms.locfileid: "898443"
---
# <a name="configure-the-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="f2736-103">Lohnintegration zwischen Talent und Dayforce konfigurieren</span><span class="sxs-lookup"><span data-stu-id="f2736-103">Configure the payroll integration between Talent and Dayforce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f2736-104">Die Integration zwischen Microsoft Dynamics 365 for Talent und Ceridian Dayforce beruht auf mehreren Konfigurationsschritten, die in diesem Thema beschrieben sind.</span><span class="sxs-lookup"><span data-stu-id="f2736-104">The integration between Microsoft Dynamics 365 for Talent and Ceridian Dayforce relies on several configuration steps that are described in this topic.</span></span> <span data-ttu-id="f2736-105">Sie müssen die Integration sowohl in Talent als auch in Dayforce konfigurieren, bevor Sie einen Zahllauf verarbeiten können.</span><span class="sxs-lookup"><span data-stu-id="f2736-105">You must configure the integration in both Talent and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="f2736-106">Wenn Sie einen Dienst wie Dayforce verwenden, um Zahlläufe abzuschließen, müssen Sie die Integration in Talent ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="f2736-106">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Talent.</span></span> <span data-ttu-id="f2736-107">Die Integration erfordert bestimmte Daten aus Talent.</span><span class="sxs-lookup"><span data-stu-id="f2736-107">The integration requires specific data from Talent.</span></span> <span data-ttu-id="f2736-108">Daher müssen Sie überprüfen, dass die Daten, die Dayforce zugeordnet sind, in Talent in einer Weise konfiguriert werden, die die Integration unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f2736-108">Therefore, you must verify that data that is mapped to Dayforce is configured in Talent in a manner that supports the integration.</span></span> <span data-ttu-id="f2736-109">Bei der Integration werden die folgenden allgemeinen Kategorien von Daten verwendet:</span><span class="sxs-lookup"><span data-stu-id="f2736-109">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="f2736-110">Personalverwaltungsdaten</span><span class="sxs-lookup"><span data-stu-id="f2736-110">Human resources data</span></span>
- <span data-ttu-id="f2736-111">Vergütungsdaten</span><span class="sxs-lookup"><span data-stu-id="f2736-111">Compensation data</span></span>
- <span data-ttu-id="f2736-112">Lohndaten, wie Lohnzyklen, Lohnperioden und Einkommenscodes</span><span class="sxs-lookup"><span data-stu-id="f2736-112">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="f2736-113">Arbeitskraftdaten</span><span class="sxs-lookup"><span data-stu-id="f2736-113">Worker data</span></span>

<span data-ttu-id="f2736-114">In diesem Thema werden die Schritte beschrieben, die Sie befolgen müssen, um die Integration zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="f2736-114">This topic describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="f2736-115">Es werden auch die Datentypen und die Konfigurationsdetails erklärt, die für die Integration erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="f2736-115">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="f2736-116">Die Integration aktivieren</span><span class="sxs-lookup"><span data-stu-id="f2736-116">Enable the integration</span></span>

<span data-ttu-id="f2736-117">In Talent müssen Sie die Integration aktivieren und die Konfigurationsinformationen eingeben, um eine Verbindung mit Dayforce herzustellen.</span><span class="sxs-lookup"><span data-stu-id="f2736-117">In Talent, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="f2736-118">Wenn Sie möchten, dass die erstellte Hauptbuchtransaktion in Microsoft Dynamics 365 for Finance and Operations importiert wird, müssen Sie auch ein Microsoft Azure-Speicherkonto einrichten und die Azure Storage-Verbindungszeichenfolge in Finance and Operations eingeben.</span><span class="sxs-lookup"><span data-stu-id="f2736-118">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 for Finance and Operations, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance and Operations.</span></span>

<span data-ttu-id="f2736-119">Um die Integration in Talent zu aktivieren, gehen Sie folgendermaßen vor.</span><span class="sxs-lookup"><span data-stu-id="f2736-119">To turn on the integration in Talent, follow these steps.</span></span>

1. <span data-ttu-id="f2736-120">Wählen Sie auf der Seite **Systemverwaltung** die Option **Integrationskonfiguration** aus.</span><span class="sxs-lookup"><span data-stu-id="f2736-120">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="f2736-121">Geben Sie den sicheren Datenübertragungsprotokoll-(FTP)-Endpunkt und den sicheren FTP-Ordnerpfad ein.</span><span class="sxs-lookup"><span data-stu-id="f2736-121">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="f2736-122">Geben Sie den Benutzernamen und das Kennwort des Benutzers ein, der auf den sicheren FTP-Endpunkt und Ordnerpfad zugreift.</span><span class="sxs-lookup"><span data-stu-id="f2736-122">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="f2736-123">Testen Sie die Verbindung nach Bedarf, und legen Sie die Option **Lohnintegration aktivieren** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="f2736-123">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="f2736-124">Wenn die Integration aktiviert ist, werden Datenexportpaket und Dateien erstellt und die Häufigkeit wird festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f2736-124">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="f2736-125">Sie können diese Häufigkeit nach Bedarf ändern.</span><span class="sxs-lookup"><span data-stu-id="f2736-125">You can change this frequency as you require.</span></span>

<span data-ttu-id="f2736-126">Weitere Informationen zu Azure-Speicherkonten und Azure Storage-Verbindungszeichenfolgen finden Sie in den folgenden Azure-Themen:</span><span class="sxs-lookup"><span data-stu-id="f2736-126">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure topics:</span></span>

- [<span data-ttu-id="f2736-127">Über Azure-Speicherkonten</span><span class="sxs-lookup"><span data-stu-id="f2736-127">About Azure storage accounts</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="f2736-128">Azure Storage-Verbindungszeichenfolgen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="f2736-128">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-configure-connection-string)

## <a name="configure-your-data"></a><span data-ttu-id="f2736-129">Ihre Daten konfigurieren</span><span class="sxs-lookup"><span data-stu-id="f2736-129">Configure your data</span></span> 

<span data-ttu-id="f2736-130">Um die Lohnbuchung zu verarbeiten, müssen Sie Personalverwaltungsdaten in Talent konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="f2736-130">To process payroll, you must configure human resource data in Talent.</span></span> <span data-ttu-id="f2736-131">Sie müssen Organisationsdaten, wie Stellen und Positionen, zusammen mit Vorteilen Vergütungsinformationen einrichten.</span><span class="sxs-lookup"><span data-stu-id="f2736-131">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="f2736-132">Diese Informationen stellen Beschäftigung, Lohn und die Abzugsinformationen bereit, die zur Generierung der Mitarbeiterentlohnung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="f2736-132">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="f2736-133">Personalverwaltungsdaten</span><span class="sxs-lookup"><span data-stu-id="f2736-133">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="f2736-134">Vergütungen</span><span class="sxs-lookup"><span data-stu-id="f2736-134">Benefits</span></span> 

<span data-ttu-id="f2736-135">Die Personalverwaltung stellt eine Reihe von Tools für die Einrichtung und Verwaltung der Vorteile, Abzüge und Vergütungspläne der Arbeitskräfte bereit, die eine Organisation für seine Arbeitskräfte anbietet oder verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="f2736-135">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="f2736-136">Wenn Sie Vorteile erstellen, sollten Sie folgende Daten und Konfigurationen bedenken, die in Dayforce verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f2736-136">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="f2736-137">Vorteilspläne</span><span class="sxs-lookup"><span data-stu-id="f2736-137">Benefit plans</span></span>

- <span data-ttu-id="f2736-138">Plan (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-138">Plan (required)</span></span>
- <span data-ttu-id="f2736-139">Typ (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-139">Type (required)</span></span>
- <span data-ttu-id="f2736-140">Lohnauswirkung (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-140">Payroll impact (required)</span></span>
- <span data-ttu-id="f2736-141">Rückstände wiederherstellen</span><span class="sxs-lookup"><span data-stu-id="f2736-141">Recover arrears</span></span>
- <span data-ttu-id="f2736-142">Abzugsverfahren</span><span class="sxs-lookup"><span data-stu-id="f2736-142">Deduction method</span></span>
- <span data-ttu-id="f2736-143">Abzugspriorität</span><span class="sxs-lookup"><span data-stu-id="f2736-143">Deduction priority</span></span>
- <span data-ttu-id="f2736-144">Periode eingrenzen</span><span class="sxs-lookup"><span data-stu-id="f2736-144">Limit period</span></span>
- <span data-ttu-id="f2736-145">Limitbetrag</span><span class="sxs-lookup"><span data-stu-id="f2736-145">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="f2736-146">Vergütungen</span><span class="sxs-lookup"><span data-stu-id="f2736-146">Benefits</span></span>

- <span data-ttu-id="f2736-147">Plan (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-147">Plan (required)</span></span>
- <span data-ttu-id="f2736-148">Typ (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-148">Type (required)</span></span>
- <span data-ttu-id="f2736-149">Option (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-149">Option (required)</span></span>
- <span data-ttu-id="f2736-150">Vorteilskennung (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-150">Benefit ID (required)</span></span>
- <span data-ttu-id="f2736-151">Häufigkeit</span><span class="sxs-lookup"><span data-stu-id="f2736-151">Frequency</span></span>
- <span data-ttu-id="f2736-152">Basis</span><span class="sxs-lookup"><span data-stu-id="f2736-152">Basis</span></span>
- <span data-ttu-id="f2736-153">Betrag oder Satz</span><span class="sxs-lookup"><span data-stu-id="f2736-153">Amount or rate</span></span>
- <span data-ttu-id="f2736-154">Einkommenscode</span><span class="sxs-lookup"><span data-stu-id="f2736-154">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="f2736-155">Unterstützte Häufigkeiten</span><span class="sxs-lookup"><span data-stu-id="f2736-155">Supported frequencies</span></span> 

- <span data-ttu-id="f2736-156">Wöchentlich</span><span class="sxs-lookup"><span data-stu-id="f2736-156">Weekly</span></span>
- <span data-ttu-id="f2736-157">14-tägig</span><span class="sxs-lookup"><span data-stu-id="f2736-157">Bi-weekly</span></span>
- <span data-ttu-id="f2736-158">Halbmonatlich</span><span class="sxs-lookup"><span data-stu-id="f2736-158">Semi-monthly</span></span>
- <span data-ttu-id="f2736-159">Monatlich</span><span class="sxs-lookup"><span data-stu-id="f2736-159">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="f2736-160">Unterstützte Basen</span><span class="sxs-lookup"><span data-stu-id="f2736-160">Supported bases</span></span> 

- <span data-ttu-id="f2736-161">Fester Betrag</span><span class="sxs-lookup"><span data-stu-id="f2736-161">Fixed amount</span></span>
- <span data-ttu-id="f2736-162">Prozent des Einkommens</span><span class="sxs-lookup"><span data-stu-id="f2736-162">Percent of earnings</span></span>
- <span data-ttu-id="f2736-163">Produktive Stunden</span><span class="sxs-lookup"><span data-stu-id="f2736-163">Productive hours</span></span>

<span data-ttu-id="f2736-164">Dayforce erstellt die folgenden Abzüge, basierend auf den Lohnauswirkungen, die im Vorteilsplan definiert sind.</span><span class="sxs-lookup"><span data-stu-id="f2736-164">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="f2736-165">Auswahl in Talent</span><span class="sxs-lookup"><span data-stu-id="f2736-165">Selection in Talent</span></span>        | <span data-ttu-id="f2736-166">Ergebnis in Dayforce</span><span class="sxs-lookup"><span data-stu-id="f2736-166">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="f2736-167">None</span><span class="sxs-lookup"><span data-stu-id="f2736-167">None</span></span>                       | <span data-ttu-id="f2736-168">Es wird kein Abzug erstellt.</span><span class="sxs-lookup"><span data-stu-id="f2736-168">No deduction is created.</span></span>                      |
| <span data-ttu-id="f2736-169">Nur Abzug</span><span class="sxs-lookup"><span data-stu-id="f2736-169">Deduction only</span></span>             | <span data-ttu-id="f2736-170">Ein Mitarbeiterabzug wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="f2736-170">An employee deduction is created.</span></span>             |
| <span data-ttu-id="f2736-171">Nur Beitrag</span><span class="sxs-lookup"><span data-stu-id="f2736-171">Contribution only</span></span>          | <span data-ttu-id="f2736-172">Ein Arbeitgeberabzug wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="f2736-172">An employer deduction is created.</span></span>             |
| <span data-ttu-id="f2736-173">Abzug und Beitrag</span><span class="sxs-lookup"><span data-stu-id="f2736-173">Deduction and contribution</span></span> | <span data-ttu-id="f2736-174">Mitarbeiter- und Arbeitgeberabzüge werden erstellt.</span><span class="sxs-lookup"><span data-stu-id="f2736-174">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="f2736-175">Weitere Informationen darüber, wie Sie ein Vorteilsprogramm definieren und verwalten finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="f2736-175">For more information about how to define and manage a benefits program, see the following topics:</span></span>

- [<span data-ttu-id="f2736-176">Mitarbeitervergütungsprogramm bereitstellen</span><span class="sxs-lookup"><span data-stu-id="f2736-176">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="f2736-177">Neuen Vorteil erstellen</span><span class="sxs-lookup"><span data-stu-id="f2736-177">Create a new benefit</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="f2736-178">Vorteilsberechtigungsregeln und Richtlinien definieren</span><span class="sxs-lookup"><span data-stu-id="f2736-178">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="f2736-179">Vorteile von Arbeitskräften registrieren und entfernen</span><span class="sxs-lookup"><span data-stu-id="f2736-179">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="f2736-180">Vergütung</span><span class="sxs-lookup"><span data-stu-id="f2736-180">Compensation</span></span> 

<span data-ttu-id="f2736-181">Die Vergütungsverwaltung dient zum Steuern der Abwicklung des Grundlohns und der Prämien.</span><span class="sxs-lookup"><span data-stu-id="f2736-181">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="f2736-182">Sie steuern den festen Grundlohn eines Mitarbeiters und dessen Lohnsteigerungen nach Plänen für feste Vergütung.</span><span class="sxs-lookup"><span data-stu-id="f2736-182">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="f2736-183">Die Zahlung leistungsbezogener Prämien, wie Boni, Leistungsprämien, Aktienoptionen und -überlassungen sowie Einmalprämien werden durch Pläne für variable Vergütung gesteuert.</span><span class="sxs-lookup"><span data-stu-id="f2736-183">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="f2736-184">Dayforce verwendet Vergütungsinformationen, um einen Stunden- oder Jahressatz für einen Mitarbeiter zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="f2736-184">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="f2736-185">Feste Vergütungspläne und Lohnsatzumrechnungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f2736-185">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="f2736-186">Mitarbeiter müssen einem festen Vergütungsplan zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="f2736-186">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="f2736-187">Weitere Informationen zu Vergütungsplänen finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="f2736-187">For more information about compensation plans, see the following topics:</span></span>

- [<span data-ttu-id="f2736-188">Feste Vergütungspläne erstellen</span><span class="sxs-lookup"><span data-stu-id="f2736-188">Create fixed compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="f2736-189">Variable Vergütungspläne erstellen</span><span class="sxs-lookup"><span data-stu-id="f2736-189">Create variable compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="f2736-190">Gehalts-/Vergütungsstruktur und -pläne entwickeln</span><span class="sxs-lookup"><span data-stu-id="f2736-190">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="f2736-191">Vergütung verarbeiten</span><span class="sxs-lookup"><span data-stu-id="f2736-191">Process compensation</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="f2736-192">Vergütungsprozess definieren und Ergebnisse berechnen</span><span class="sxs-lookup"><span data-stu-id="f2736-192">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="f2736-193">Einen Mitarbeiters in einem Plan für eine feste Vergütung registrieren</span><span class="sxs-lookup"><span data-stu-id="f2736-193">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="f2736-194">Einen Mitarbeiter in einem Plan für variable Vergütung registrieren</span><span class="sxs-lookup"><span data-stu-id="f2736-194">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="f2736-195">Stellentyp</span><span class="sxs-lookup"><span data-stu-id="f2736-195">Jobs</span></span> 

<span data-ttu-id="f2736-196">Eine Stelle ist eine Sammlung der Aufgaben und Zuständigkeiten, die für eine Person, die eine Tätigkeit ausführt, obligatorisch sind.</span><span class="sxs-lookup"><span data-stu-id="f2736-196">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="f2736-197">Weitere Informationen finden Sie in folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="f2736-197">For more information, see the following topics:</span></span>

- [<span data-ttu-id="f2736-198">Komponenten einer Stelle einrichten</span><span class="sxs-lookup"><span data-stu-id="f2736-198">Setting up the components of a job</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="f2736-199">Neue Einzelvorgänge definieren</span><span class="sxs-lookup"><span data-stu-id="f2736-199">Define new jobs</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="f2736-200">Positionen</span><span class="sxs-lookup"><span data-stu-id="f2736-200">Positions</span></span>

<span data-ttu-id="f2736-201">Eine Position ist eine einzelne Instanz eines Einzelvorgangs.</span><span class="sxs-lookup"><span data-stu-id="f2736-201">A position is an individual instance of a job.</span></span> <span data-ttu-id="f2736-202">Beispielsweise ist die Position „Verkaufsleiter (Ost)” eine der Positionen, die der Stelle „Verkaufsleiter” zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="f2736-202">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="f2736-203">Eine Position ist in einer Abteilung vorhanden.</span><span class="sxs-lookup"><span data-stu-id="f2736-203">A position exists in a department.</span></span> <span data-ttu-id="f2736-204">Nur jeweils eine Arbeitskraft kann jeder Position zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="f2736-204">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="f2736-205">Bedenken Sie die folgenden Daten und Konfigurationen, wenn Sie Positionen einrichten:</span><span class="sxs-lookup"><span data-stu-id="f2736-205">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="f2736-206">Position (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-206">Position (required)</span></span>
- <span data-ttu-id="f2736-207">Beschreibung (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-207">Description (required)</span></span>
- <span data-ttu-id="f2736-208">Stelle (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-208">Job (required)</span></span>
- <span data-ttu-id="f2736-209">Abteilung (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-209">Department (required)</span></span>
- <span data-ttu-id="f2736-210">Positionstyp (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-210">Position type (required)</span></span>
- <span data-ttu-id="f2736-211">Vollzeitäquivalent</span><span class="sxs-lookup"><span data-stu-id="f2736-211">Full-time equivalent</span></span>
- <span data-ttu-id="f2736-212">Normale Stunden pro Jahr (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-212">Annual regular hours (required)</span></span>
- <span data-ttu-id="f2736-213">Gezahlt von der juristischen Person (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-213">Paid by legal entity (required)</span></span>
- <span data-ttu-id="f2736-214">Lohnzyklus (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-214">Pay cycle (required)</span></span>
- <span data-ttu-id="f2736-215">Standardfinanzdimension – Kostenstelle (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-215">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="f2736-216">Arbeitskraftzuweisung – Arbeitskraft, Zuweisungsanfang, Zuweisungsende, Ursachencode</span><span class="sxs-lookup"><span data-stu-id="f2736-216">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="f2736-217">Wenn mehrere Positionen in derselben Abteilung derselben Stelle zugeordnet sind, werden sie in einer einzelnen Position in Dayforce konsolidiert.</span><span class="sxs-lookup"><span data-stu-id="f2736-217">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="f2736-218">Weitere Informationen finden Sie in folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="f2736-218">For more information, see the following topics:</span></span>

- [<span data-ttu-id="f2736-219">Organisieren der Belegschaft anhand von Abteilungen, Stellen und Positionen</span><span class="sxs-lookup"><span data-stu-id="f2736-219">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="f2736-220">Positionen einrichten</span><span class="sxs-lookup"><span data-stu-id="f2736-220">Set up positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="f2736-221">Abteilungen</span><span class="sxs-lookup"><span data-stu-id="f2736-221">Departments</span></span>

<span data-ttu-id="f2736-222">Eine Abteilung ist eine Organisationseinheit, die eine Kategorie oder einen funktionalen Bereich einer Organisation darstellt.</span><span class="sxs-lookup"><span data-stu-id="f2736-222">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="f2736-223">Eine Abteilung ist für einen bestimmten Bereich der Organisation wie zum Beispiel Verkauf, Buchhaltung oder Personalverwaltung zuständig.</span><span class="sxs-lookup"><span data-stu-id="f2736-223">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="f2736-224">Sie können Abteilungen verwenden, um zu Funktionsbereiche zu melden.</span><span class="sxs-lookup"><span data-stu-id="f2736-224">You can use departments to report on functional areas.</span></span> <span data-ttu-id="f2736-225">Abteilungen können Gewinn- und Verlustzuständigkeit haben.</span><span class="sxs-lookup"><span data-stu-id="f2736-225">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="f2736-226">Weitere Informationen finden Sie in folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="f2736-226">For more information, see the following topics:</span></span>

- [<span data-ttu-id="f2736-227">Eine Abteilung erstellen und der Abteilungshierarchie zuordnen</span><span class="sxs-lookup"><span data-stu-id="f2736-227">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="f2736-228">Neue Abteilungen definieren</span><span class="sxs-lookup"><span data-stu-id="f2736-228">Define new departments</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="f2736-229">Lohnzyklen und Lohnperioden</span><span class="sxs-lookup"><span data-stu-id="f2736-229">Pay cycles and pay periods</span></span>

<span data-ttu-id="f2736-230">Ein Lohnzyklus bestimmt, wie oft Lohn ausgezahlt wird, sowie die spezifischen Tage, an denen Arbeitskräfte bezahlt werden.</span><span class="sxs-lookup"><span data-stu-id="f2736-230">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="f2736-231">Ein Lohnzyklus kann beispielsweise monatlich sein, und Mitarbeiter werden am letzten Tag des Monats bezahlt.</span><span class="sxs-lookup"><span data-stu-id="f2736-231">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="f2736-232">Alternativ könnte ein Lohnzyklus wöchentlich sein, und Mitarbeiter werden am Dienstag nach Ende der Lohnperiode bezahlt.</span><span class="sxs-lookup"><span data-stu-id="f2736-232">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="f2736-233">Lohnzyklen werden Positionen zugewiesen, um zu steuern, wann Mitarbeiter in diesen Positionen bezahlt werden.</span><span class="sxs-lookup"><span data-stu-id="f2736-233">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="f2736-234">Nachdem Sie Lohnzyklen erstellen, können Sie Lohnperioden für jeden Zyklus generieren.</span><span class="sxs-lookup"><span data-stu-id="f2736-234">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="f2736-235">Jede Lohnperiode enthält ein Standardzahlungsdatum, das auf den von Ihnen bereitgestellten Informationen basiert.</span><span class="sxs-lookup"><span data-stu-id="f2736-235">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="f2736-236">Allerdings können Sie das Standardzahlungsdatum in einer Lohnperiode ändern, um Ausnahmen zuzulassen, wie beispielsweise wenn das Zahlungsdatum auf einen Feiertag fällt.</span><span class="sxs-lookup"><span data-stu-id="f2736-236">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="f2736-237">Die folgenden Informationen werden in Dayforce verwendet:</span><span class="sxs-lookup"><span data-stu-id="f2736-237">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="f2736-238">Lohnzyklus (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-238">Pay cycle (required)</span></span>
- <span data-ttu-id="f2736-239">Lohnzyklushäufigkeit (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-239">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="f2736-240">Periodenstartdatum (erstes erforderliche Lohnperiode)</span><span class="sxs-lookup"><span data-stu-id="f2736-240">Period start date (first pay period required)</span></span>
- <span data-ttu-id="f2736-241">Standardzahlungsdatum (erste erforderliche Lohnperiode)</span><span class="sxs-lookup"><span data-stu-id="f2736-241">Default payment date (first pay period required)</span></span>

<span data-ttu-id="f2736-242">Diese Informationen werden mit Dayforce als Lohngruppen integriert und sind nach Land oder Region für jeden Lohnzyklus getrennt.</span><span class="sxs-lookup"><span data-stu-id="f2736-242">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="f2736-243">Es muss mindestens eine Lohnperiode vor der Integration generiert werden.</span><span class="sxs-lookup"><span data-stu-id="f2736-243">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="f2736-244">Dayforce generiert Lohngruppenkalender und Zahlungsdaten basierend auf dem Anfangsdatum der ersten Lohnperiode und dem Standardzahlungsdatums, das in Talent eingerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="f2736-244">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Talent.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="f2736-245">Einkommenscodes</span><span class="sxs-lookup"><span data-stu-id="f2736-245">Earning codes</span></span>

<span data-ttu-id="f2736-246">Einkommenscodes bestimmen jeden Typ von Einkünften eindeutig, die Arbeitskräfte erhalten</span><span class="sxs-lookup"><span data-stu-id="f2736-246">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="f2736-247">Die Codes haben verschiedene Parameter, die sich auf Einkünfte beziehen, wie beispielsweise Buchhaltungsvorschriften, Steuergesetze, Berichterstellungsanforderungen und Bruttoausgleichsfähigkeit.</span><span class="sxs-lookup"><span data-stu-id="f2736-247">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="f2736-248">Die folgenden Informationen werden in Dayforce verwendet:</span><span class="sxs-lookup"><span data-stu-id="f2736-248">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="f2736-249">Einkommenscode (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-249">Earning Code (required)</span></span>
- <span data-ttu-id="f2736-250">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f2736-250">Description</span></span>
- <span data-ttu-id="f2736-251">Maßeinheit</span><span class="sxs-lookup"><span data-stu-id="f2736-251">Unit of measure</span></span>
- <span data-ttu-id="f2736-252">Produktiv</span><span class="sxs-lookup"><span data-stu-id="f2736-252">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="f2736-253">Arbeitskraftdaten</span><span class="sxs-lookup"><span data-stu-id="f2736-253">Worker data</span></span>

<span data-ttu-id="f2736-254">Datensätze für die verschiedenen Arten von Arbeitskräften, die Sie haben, sind für Ihre Personalverwaltung- sowie für Ihre Lohnsysteme von Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="f2736-254">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="f2736-255">Anhand der eingegebenen Informationen lassen sich Arbeitskräfte sowie personenbezogene Informationen nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="f2736-255">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="f2736-256">Sie können die folgenden Informationen für Arbeitskräfte verwalten:</span><span class="sxs-lookup"><span data-stu-id="f2736-256">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="f2736-257">**Basis** – Verwalten grundlegender Informationen über eine Arbeitskraft, beispielsweise Kontaktinformationen, demografische Informationen, Kennungsinformationen, Familieninformationen, Militärdienststatus, Ausländerinformationen sowie personenbezogene und Notfallkontakte.</span><span class="sxs-lookup"><span data-stu-id="f2736-257">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="f2736-258">**Beschäftigung** – Verwalten von Informationen zum Beschäftigungsverhältnis einer Arbeitskraft, wie Unternehmens- oder Organisationszugehörigkeit, Positionszuweisung, Start- und Enddatum, Arbeitsberechtigung, Beschäftigungsbedingungen, Rente, Urlaub und Versetzungen.</span><span class="sxs-lookup"><span data-stu-id="f2736-258">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="f2736-259">**Urlaub und Abwesenheit** – Verwalten von Informationen zur Abwesenheit einer Arbeitskraft, beispielsweise Arbeitszeitkalender, Abwesenheitsbuchungen und Abwesenheitseinrichtung.</span><span class="sxs-lookup"><span data-stu-id="f2736-259">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="f2736-260">**Vergütung und Lohn** – Verwalten von Informationen zu den Vergütungsplänen und Lohndaten einer Arbeitskraft, wie der Planregistrierung, Boni, Leistung, Provision, Steuerdaten, Pensionierung und Gehaltsabzüge.</span><span class="sxs-lookup"><span data-stu-id="f2736-260">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="f2736-261">Wenn Sie Arbeitskraftinformationen eingeben, sollten Sie folgende Daten und Konfigurationen bedenken, die in Dayforce verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f2736-261">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="f2736-262">Allgemeine Angaben</span><span class="sxs-lookup"><span data-stu-id="f2736-262">General information</span></span>

- <span data-ttu-id="f2736-263">Personalnummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-263">Personnel number (required)</span></span>
- <span data-ttu-id="f2736-264">Vorname (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-264">First name (required)</span></span>
- <span data-ttu-id="f2736-265">Nachname (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-265">Last name (required)</span></span>
- <span data-ttu-id="f2736-266">Zweiter Vorname</span><span class="sxs-lookup"><span data-stu-id="f2736-266">Middle name</span></span>
- <span data-ttu-id="f2736-267">Dienstalterdatum</span><span class="sxs-lookup"><span data-stu-id="f2736-267">Seniority date</span></span>
- <span data-ttu-id="f2736-268">Bekannt als</span><span class="sxs-lookup"><span data-stu-id="f2736-268">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="f2736-269">Personenbezogene Informationen</span><span class="sxs-lookup"><span data-stu-id="f2736-269">Personal information</span></span>

- <span data-ttu-id="f2736-270">Familienstand (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-270">Marital status (required)</span></span>
- <span data-ttu-id="f2736-271">Geburtsdatum (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-271">Birth date (required)</span></span>
- <span data-ttu-id="f2736-272">Geschlecht (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-272">Gender (required)</span></span>
- <span data-ttu-id="f2736-273">Person mit Behinderung</span><span class="sxs-lookup"><span data-stu-id="f2736-273">Person with disabilities</span></span>
- <span data-ttu-id="f2736-274">Nationalitätsland/-region (nur für Mexiko)</span><span class="sxs-lookup"><span data-stu-id="f2736-274">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="f2736-275">Adressdaten</span><span class="sxs-lookup"><span data-stu-id="f2736-275">Address information</span></span>

- <span data-ttu-id="f2736-276">Primär (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-276">Primary (required)</span></span>
- <span data-ttu-id="f2736-277">Land/Region (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-277">Country/region (required)</span></span>
- <span data-ttu-id="f2736-278">Postleitzahl (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-278">Postal code (required)</span></span>
- <span data-ttu-id="f2736-279">Hausnummer (erforderlich) (nur für Mexiko)</span><span class="sxs-lookup"><span data-stu-id="f2736-279">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="f2736-280">Gebäudeergänzung (nur für Mexiko)</span><span class="sxs-lookup"><span data-stu-id="f2736-280">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="f2736-281">Ort (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-281">City (required)</span></span>
- <span data-ttu-id="f2736-282">Bundesland/Kanton (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-282">State (required)</span></span>
- <span data-ttu-id="f2736-283">Landkreis (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-283">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="f2736-284">Kontaktdaten</span><span class="sxs-lookup"><span data-stu-id="f2736-284">Contact information</span></span> 

- <span data-ttu-id="f2736-285">Primär (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-285">Primary (required)</span></span>
- <span data-ttu-id="f2736-286">Kontaktnummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-286">Contact number (required)</span></span>
- <span data-ttu-id="f2736-287">Durchwahl</span><span class="sxs-lookup"><span data-stu-id="f2736-287">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="f2736-288">Lohndaten und Einkommenscodes</span><span class="sxs-lookup"><span data-stu-id="f2736-288">Payroll information and earning codes</span></span>

<span data-ttu-id="f2736-289">Mitarbeitern müssen bestimmte Einkommen mit einer bestimmten Zahlungshäufigkeit zugewiesen werden und sie müssen eine bevorzugte Zahlungsmethode haben.</span><span class="sxs-lookup"><span data-stu-id="f2736-289">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="f2736-290">Die folgenden Felder werden in Dayforce verwendet, um zu gewährleisten, dass diese Voreinstellungen und Einstellungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f2736-290">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="f2736-291">Einkommenscodes</span><span class="sxs-lookup"><span data-stu-id="f2736-291">Earning codes</span></span>

- <span data-ttu-id="f2736-292">Position (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-292">Position (required)</span></span>
- <span data-ttu-id="f2736-293">Einkommenscode (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-293">Earning Code (required)</span></span>
- <span data-ttu-id="f2736-294">Häufigkeit (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-294">Frequency (required)</span></span>
- <span data-ttu-id="f2736-295">Betrag (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-295">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="f2736-296">Lohndaten</span><span class="sxs-lookup"><span data-stu-id="f2736-296">Payroll information</span></span>

- <span data-ttu-id="f2736-297">Zahlungsmethode</span><span class="sxs-lookup"><span data-stu-id="f2736-297">Payment Method</span></span>
- <span data-ttu-id="f2736-298">Wirtschaftliche Region (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-298">Economic Region (required)</span></span>
- <span data-ttu-id="f2736-299">Mitarbeitervergütungs-ID</span><span class="sxs-lookup"><span data-stu-id="f2736-299">Employee Benefits ID</span></span>
- <span data-ttu-id="f2736-300">Personalausweisnummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-300">National ID Number (required)</span></span>
- <span data-ttu-id="f2736-301">Militärdienstnummer</span><span class="sxs-lookup"><span data-stu-id="f2736-301">Military Service Number</span></span>
- <span data-ttu-id="f2736-302">Schichtkennung (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-302">Shift ID (required)</span></span>
- <span data-ttu-id="f2736-303">Steuernummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-303">Tax Number (required)</span></span>
- <span data-ttu-id="f2736-304">Gewerkschaftskennung (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-304">Union ID (required)</span></span>
- <span data-ttu-id="f2736-305">Arbeitstagkennung (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-305">Work Day ID (required)</span></span>
- <span data-ttu-id="f2736-306">Arbeitserlaubnisnummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-306">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="f2736-307">Für die Zahlungsmethode unterstützt Mexiko **Bargeld**, **Scheck** (der physische Scheck des Unternehmens) und **Elektronische Zahlung**.</span><span class="sxs-lookup"><span data-stu-id="f2736-307">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="f2736-308">Wenn keine Zahlungsmethode angegeben wird, wird **Scheck** standardmäßig verwendet.</span><span class="sxs-lookup"><span data-stu-id="f2736-308">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="f2736-309">Anstellungsdetails</span><span class="sxs-lookup"><span data-stu-id="f2736-309">Employment details</span></span>

<span data-ttu-id="f2736-310">Beschäftigungsdetailhistorie wird als Schlüsselinformation verwendet, um die Status für Einstellung, Kündigung und erneute Einstellung in Dayforce abzuleiten.</span><span class="sxs-lookup"><span data-stu-id="f2736-310">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="f2736-311">Dayforce unterstützt nur einen aktiven Beschäftigungsdatensatz gleichzeitig.</span><span class="sxs-lookup"><span data-stu-id="f2736-311">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="f2736-312">Datum des Beschäftigungsbeginns (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-312">Employment start date (required)</span></span>
- <span data-ttu-id="f2736-313">Datum des Beschäftigungsendes</span><span class="sxs-lookup"><span data-stu-id="f2736-313">Employment end date</span></span>
- <span data-ttu-id="f2736-314">Eintrittstermin</span><span class="sxs-lookup"><span data-stu-id="f2736-314">Start date</span></span>
- <span data-ttu-id="f2736-315">Angepasster Tätigkeitsbeginn</span><span class="sxs-lookup"><span data-stu-id="f2736-315">Adjusted start date</span></span>
- <span data-ttu-id="f2736-316">Kündigungsdatum (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-316">Termination date (required upon termination)</span></span>
- <span data-ttu-id="f2736-317">Kündigungsgrund (erforderlich bei Kündigung)</span><span class="sxs-lookup"><span data-stu-id="f2736-317">Termination reason (required upon termination)</span></span>

<span data-ttu-id="f2736-318">Die Schlüsseldaten eines Mitarbeiters werden abgeleitet, indem die folgenden Informationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f2736-318">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="f2736-319">Talent</span><span class="sxs-lookup"><span data-stu-id="f2736-319">Talent</span></span>                | <span data-ttu-id="f2736-320">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f2736-320">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2736-321">Aktuellstes Einstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="f2736-321">Most recent hire date</span></span> | <span data-ttu-id="f2736-322">Beschäftigungsbeginn des Verlaufsdatensatzes zur aktuellen, nicht gekündigten Beschäftigung</span><span class="sxs-lookup"><span data-stu-id="f2736-322">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="f2736-323">Kündigungsdatum</span><span class="sxs-lookup"><span data-stu-id="f2736-323">Termination date</span></span>      | <span data-ttu-id="f2736-324">Kündigungsdatum des Verlaufsdatensatzes zur aktuellen, nicht gekündigten Beschäftigung</span><span class="sxs-lookup"><span data-stu-id="f2736-324">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="f2736-325">Eintrittstermin</span><span class="sxs-lookup"><span data-stu-id="f2736-325">Start date</span></span>            | <span data-ttu-id="f2736-326">Angepasstes Startdatum, Startdatum oder Beschäftigungsbeginn des Verlaufsdatensatzes zur aktuellen, nicht aktiven Beschäftigung</span><span class="sxs-lookup"><span data-stu-id="f2736-326">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="f2736-327">Ursprüngliches Einstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="f2736-327">Original hire date</span></span>    | <span data-ttu-id="f2736-328">Beschäftigungsbeginn des frühesten Beschäftigungsverlaufsdatensatzes</span><span class="sxs-lookup"><span data-stu-id="f2736-328">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="f2736-329">Vergütung</span><span class="sxs-lookup"><span data-stu-id="f2736-329">Compensation</span></span>

<span data-ttu-id="f2736-330">Ein fester Vergütungsplan muss der primären Position jedes Mitarbeiters während einer Beschäftigungsperiode zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="f2736-330">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="f2736-331">Diese Periode beginnt mit dem Datum, an dem der Mitarbeiter eingestellt wurde (oder dem Datum des Beschäftigungsbeginns), und setzt sich bis zur Kündigung fort.</span><span class="sxs-lookup"><span data-stu-id="f2736-331">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="f2736-332">Gültigkeitsdatum (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-332">Effective Date (required)</span></span>
- <span data-ttu-id="f2736-333">Ablaufdatum</span><span class="sxs-lookup"><span data-stu-id="f2736-333">Expiration date</span></span>
- <span data-ttu-id="f2736-334">Lohnsatz (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-334">Pay Rate (required)</span></span>
- <span data-ttu-id="f2736-335">Lohnsatzkonvertierungen (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-335">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="f2736-336">Jährliches Äquivalent (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-336">Annual equivalent (required)</span></span>
- <span data-ttu-id="f2736-337">Stündliches Äquivalent (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-337">Hourly equivalent (required)</span></span>

<span data-ttu-id="f2736-338">Wenn ein Mitarbeiter auf Stundenbasis mehrere Positionen hat, wird die feste Vergütung der primären Position in Dayforce als Basissatz/-gehalt auf Mitarbeiterebene importiert.</span><span class="sxs-lookup"><span data-stu-id="f2736-338">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="f2736-339">Für nicht-primäre Positionen wird der Stundensatz in der entsprechenden Position in Dayforce gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f2736-339">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="f2736-340">Wenn ein Gehalt beziehender Mitarbeiter mehrere Positionen hat, wird der kumulative Stundensatz und das Jahresgehalt über alle aktiven Positionen hinweg abgeleitet und als Basissatz/-gehalt auf Arbeitnehmerebene verwendet.</span><span class="sxs-lookup"><span data-stu-id="f2736-340">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="f2736-341">Kennnummern</span><span class="sxs-lookup"><span data-stu-id="f2736-341">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="f2736-342">Sozialversicherungsbezeichner</span><span class="sxs-lookup"><span data-stu-id="f2736-342">Social Security identifier</span></span> 

<span data-ttu-id="f2736-343">Jeder Mitarbeiter muss einen primären Bezeichner haben.</span><span class="sxs-lookup"><span data-stu-id="f2736-343">Every employee must have one primary identifier.</span></span> <span data-ttu-id="f2736-344">Dieser Bezeichner muss vom Kennungstyp **P.Reg.Nr.** sein.</span><span class="sxs-lookup"><span data-stu-id="f2736-344">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="f2736-345">In Dayforce wird er automatisch als Sozialversicherungsbezeichner des Mitarbeiters abgeleitet, der für die Einstellung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="f2736-345">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="f2736-346">Primär (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-346">Primary (required)</span></span>
- <span data-ttu-id="f2736-347">Kennungstyp = „P.Reg.Nr.”</span><span class="sxs-lookup"><span data-stu-id="f2736-347">Identification Type = "SSN"</span></span>
- <span data-ttu-id="f2736-348">Ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="f2736-348">Issued Date</span></span>
- <span data-ttu-id="f2736-349">Ablaufdatum</span><span class="sxs-lookup"><span data-stu-id="f2736-349">Expiration Date</span></span>

<span data-ttu-id="f2736-350">Mitarbeiter können mehrere Kennungsnummern des Kennungstyps **P.Reg.Nr.** melden.</span><span class="sxs-lookup"><span data-stu-id="f2736-350">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="f2736-351">Jedoch wird nur der Datensatz, der als **Primär** markiert ist, in Dayforce integriert, unabhängig davon, ob die Nummer aktiv oder abgelaufen ist.</span><span class="sxs-lookup"><span data-stu-id="f2736-351">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="f2736-352">Bankkonten und Auszahlungen</span><span class="sxs-lookup"><span data-stu-id="f2736-352">Bank accounts and disbursements</span></span>

<span data-ttu-id="f2736-353">Gültige Bankkontoinformationen müssen für jeden Mitarbeiter eingegeben werden, der per Bankkontoüberweisungen bezahlt werden möchte.</span><span class="sxs-lookup"><span data-stu-id="f2736-353">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="f2736-354">Talent</span><span class="sxs-lookup"><span data-stu-id="f2736-354">Talent</span></span>                         | <span data-ttu-id="f2736-355">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f2736-355">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2736-356">Bankkontonummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-356">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="f2736-357">SWIFT-Code (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-357">SWIFT code (required)</span></span>          | <span data-ttu-id="f2736-358">Feld **Bankkennung** wird verwendet, wenn Lohn in Mexiko verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="f2736-358">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="f2736-359">Filialnummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-359">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="f2736-360">Bankkontotyp (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-360">Bank account type (required)</span></span>   | <span data-ttu-id="f2736-361">Feld **Kontotyp** wird verwendet, wenn Lohn in Mexiko verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="f2736-361">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="f2736-362">Unterstützte Werte umfassen **Wird geprüft** und **Lohn**.</span><span class="sxs-lookup"><span data-stu-id="f2736-362">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="f2736-363">Mitarbeiter, die per Bankkontoüberweisungen bezahlt werden möchten, müssen eine Verknüpfung zu einem Restbetrags-Bankkonto angeben, das sich unter einer juristischen Person befindet, deren primäre Adresse in Mexiko ist und das einem gültigen Bankkonto von einer mexikanischen Bank zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f2736-363">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="f2736-364">Alle anderen Nicht-Restbetrags-Bankkonten werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="f2736-364">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="f2736-365">Adressdaten</span><span class="sxs-lookup"><span data-stu-id="f2736-365">Address information</span></span>

<span data-ttu-id="f2736-366">Jeder Mitarbeiter muss einen primären Standort haben.</span><span class="sxs-lookup"><span data-stu-id="f2736-366">Every employee must have one primary location.</span></span> <span data-ttu-id="f2736-367">In Dayforce wird dieser Standort verwendet, um den primären Wohnsitz des Mitarbeiters für Steuerzwecke zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="f2736-367">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="f2736-368">Primär (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-368">Primary (required)</span></span>
- <span data-ttu-id="f2736-369">Land/Region (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-369">Country/region (required)</span></span>
- <span data-ttu-id="f2736-370">Postleitzahl (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-370">Zip/postal code (required)</span></span>
- <span data-ttu-id="f2736-371">Straße (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-371">Street (required)</span></span>
- <span data-ttu-id="f2736-372">Hausnummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-372">Street Number (required)</span></span>
- <span data-ttu-id="f2736-373">Gebäudeergänzung</span><span class="sxs-lookup"><span data-stu-id="f2736-373">Building Complement</span></span>
- <span data-ttu-id="f2736-374">Ort (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-374">City (required)</span></span>
- <span data-ttu-id="f2736-375">Bundesland/Kanton (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-375">State (required)</span></span>
- <span data-ttu-id="f2736-376">Landkreis (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-376">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="f2736-377">Konfigurieren Ihrer Daten, um Vergütung in den USA und Kanada zu generieren</span><span class="sxs-lookup"><span data-stu-id="f2736-377">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="f2736-378">Wenn Sie Vergütung für Mitarbeiter in den USA und Kanada generieren, müssen die folgenden Elemente konfiguriert werden:</span><span class="sxs-lookup"><span data-stu-id="f2736-378">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="f2736-379">Abteilungen sind für Positionen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f2736-379">Departments are required on positions.</span></span>
- <span data-ttu-id="f2736-380">Kostenstellen müssen als Finanzdimensionen festgelegt werden und müssen das erste Element in der standardmäßigen Finanzdimensions-Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="f2736-380">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="f2736-381">Sie können Talent so konfigurieren, dass es anfordert, dass Positionen eine Abteilung angegeben.</span><span class="sxs-lookup"><span data-stu-id="f2736-381">You can configure Talent to require that Positions specify a Department.</span></span> <span data-ttu-id="f2736-382">Dazu wechseln Sie zu **Freigegebene Positionen der Personalverwaltung > Positionen > Abteilungen zu Positionen anfordern**.</span><span class="sxs-lookup"><span data-stu-id="f2736-382">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="f2736-383">Es wird empfohlen, dass diese Einstellungen für die Integration erzwungen wird.</span><span class="sxs-lookup"><span data-stu-id="f2736-383">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="f2736-384">Stellentypen</span><span class="sxs-lookup"><span data-stu-id="f2736-384">Job types</span></span>

<span data-ttu-id="f2736-385">Stellentypen werden verwendet, um ähnliche Stellen in Kategorien zu gruppieren.</span><span class="sxs-lookup"><span data-stu-id="f2736-385">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="f2736-386">Stellentypen sind erforderlich, damit Lohn in den USA und Kanada zu bearbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="f2736-386">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="f2736-387">Beispiele für Stellentypen umfassen Voll- und Teilzeit oder festes Gehalt und Stundenlohn.</span><span class="sxs-lookup"><span data-stu-id="f2736-387">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="f2736-388">Stellentypen werden Dayforce als Lohnarten zugeordnet, die angeben, ob ein Mitarbeiter auf Stundenbasis bezahlt wird oder ein festes Gehalt bezieht.</span><span class="sxs-lookup"><span data-stu-id="f2736-388">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="f2736-389">Folgende Stellentypen und Beschreibungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f2736-389">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="f2736-390">Stellentyp</span><span class="sxs-lookup"><span data-stu-id="f2736-390">Job type</span></span>   | <span data-ttu-id="f2736-391">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f2736-391">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="f2736-392">Stündlich</span><span class="sxs-lookup"><span data-stu-id="f2736-392">Hourly</span></span>     | <span data-ttu-id="f2736-393">Stündlich</span><span class="sxs-lookup"><span data-stu-id="f2736-393">Hourly</span></span>      |
| <span data-ttu-id="f2736-394">Fest angestellt</span><span class="sxs-lookup"><span data-stu-id="f2736-394">Salaried</span></span>   | <span data-ttu-id="f2736-395">Fest angestellt</span><span class="sxs-lookup"><span data-stu-id="f2736-395">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="f2736-396">Positionstypen</span><span class="sxs-lookup"><span data-stu-id="f2736-396">Position types</span></span> 

<span data-ttu-id="f2736-397">Sie verwenden Positionstypen, um zu beschreiben, ob die Position Vollzeit, Teilzeit oder etwas anderes ist.</span><span class="sxs-lookup"><span data-stu-id="f2736-397">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="f2736-398">Positionstypen werden Dayforce als Lohnklassen zugeordnet, die angeben, ob ein Mitarbeiter in Vollzeit oder Teilzeit arbeitet.</span><span class="sxs-lookup"><span data-stu-id="f2736-398">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="f2736-399">Folgende Positionstypen und Beschreibungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f2736-399">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="f2736-400">Positionstyp</span><span class="sxs-lookup"><span data-stu-id="f2736-400">Position type</span></span>   | <span data-ttu-id="f2736-401">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f2736-401">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="f2736-402">Vollzeit</span><span class="sxs-lookup"><span data-stu-id="f2736-402">Full-time</span></span>       | <span data-ttu-id="f2736-403">Vollzeitmitarbeiter</span><span class="sxs-lookup"><span data-stu-id="f2736-403">Full time employee</span></span> |
| <span data-ttu-id="f2736-404">Teilzeit</span><span class="sxs-lookup"><span data-stu-id="f2736-404">Part-time</span></span>       | <span data-ttu-id="f2736-405">Teilzeitmitarbeiter</span><span class="sxs-lookup"><span data-stu-id="f2736-405">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="f2736-406">Ursachencodes</span><span class="sxs-lookup"><span data-stu-id="f2736-406">Reason codes</span></span>

<span data-ttu-id="f2736-407">Ursachencodes enthalten Informationen zum Status eines Mitarbeiters.</span><span class="sxs-lookup"><span data-stu-id="f2736-407">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="f2736-408">Ursachencodes werden Dayforce als Statusgründe zugeordnet, die den Grund für Änderungen bei der Position eines Mitarbeiters oder dem Beschäftigungsstatus angeben.</span><span class="sxs-lookup"><span data-stu-id="f2736-408">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="f2736-409">Folgende Ursachencodes und Beschreibungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f2736-409">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="f2736-410">Ursachencode</span><span class="sxs-lookup"><span data-stu-id="f2736-410">Reason code</span></span>    | <span data-ttu-id="f2736-411">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f2736-411">Description</span></span>      | <span data-ttu-id="f2736-412">Zutreffende Szenarios</span><span class="sxs-lookup"><span data-stu-id="f2736-412">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="f2736-413">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="f2736-413">RESIGNATION</span></span>    | <span data-ttu-id="f2736-414">Kündigung durch Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="f2736-414">Resignation</span></span>      | <span data-ttu-id="f2736-415">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="f2736-415">Terminate worker</span></span>     |
| <span data-ttu-id="f2736-416">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="f2736-416">TERMINATION</span></span>    | <span data-ttu-id="f2736-417">Beendigung</span><span class="sxs-lookup"><span data-stu-id="f2736-417">Termination</span></span>      | <span data-ttu-id="f2736-418">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="f2736-418">Terminate worker</span></span>     |
| <span data-ttu-id="f2736-419">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="f2736-419">RETIREMENT</span></span>     | <span data-ttu-id="f2736-420">Ruhestand</span><span class="sxs-lookup"><span data-stu-id="f2736-420">Retirement</span></span>       | <span data-ttu-id="f2736-421">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="f2736-421">Terminate worker</span></span>     |
| <span data-ttu-id="f2736-422">OTHER</span><span class="sxs-lookup"><span data-stu-id="f2736-422">OTHER</span></span>          | <span data-ttu-id="f2736-423">Andere Gründe</span><span class="sxs-lookup"><span data-stu-id="f2736-423">Other Reasons</span></span>    | <span data-ttu-id="f2736-424">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="f2736-424">Terminate worker</span></span>     |
| <span data-ttu-id="f2736-425">DEATH</span><span class="sxs-lookup"><span data-stu-id="f2736-425">DEATH</span></span>          | <span data-ttu-id="f2736-426">Tod</span><span class="sxs-lookup"><span data-stu-id="f2736-426">Death</span></span>            | <span data-ttu-id="f2736-427">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="f2736-427">Terminate worker</span></span>     |
| <span data-ttu-id="f2736-428">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="f2736-428">LEAVEOFABSENCE</span></span> | <span data-ttu-id="f2736-429">Beurlaubung</span><span class="sxs-lookup"><span data-stu-id="f2736-429">Leave of Absence</span></span> | <span data-ttu-id="f2736-430">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="f2736-430">Terminate worker</span></span>     |
| <span data-ttu-id="f2736-431">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="f2736-431">CONTRACTEND</span></span>    | <span data-ttu-id="f2736-432">Vertragsende</span><span class="sxs-lookup"><span data-stu-id="f2736-432">End of Contract</span></span>  | <span data-ttu-id="f2736-433">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="f2736-433">Terminate worker</span></span>     |
| <span data-ttu-id="f2736-434">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="f2736-434">SALARYCHANGE</span></span>   | <span data-ttu-id="f2736-435">Gehaltsänderung</span><span class="sxs-lookup"><span data-stu-id="f2736-435">Change of Salary</span></span> | <span data-ttu-id="f2736-436">Vergütung</span><span class="sxs-lookup"><span data-stu-id="f2736-436">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="f2736-437">Familienstand</span><span class="sxs-lookup"><span data-stu-id="f2736-437">Marital status</span></span>

<span data-ttu-id="f2736-438">Familienstandwerte werden Dayforce zugeordnet und werden – je nach Bedarf – in die akzeptierten Werte bei der Integration übersetzt.</span><span class="sxs-lookup"><span data-stu-id="f2736-438">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="f2736-439">Die folgende Tabelle zeigt, wie Familienstandwerte Dayforce zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="f2736-439">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="f2736-440">Talent</span><span class="sxs-lookup"><span data-stu-id="f2736-440">Talent</span></span>                 | <span data-ttu-id="f2736-441">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f2736-441">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="f2736-442">Verheiratet</span><span class="sxs-lookup"><span data-stu-id="f2736-442">Married</span></span>                | <span data-ttu-id="f2736-443">Verheiratet</span><span class="sxs-lookup"><span data-stu-id="f2736-443">Married</span></span>              |
| <span data-ttu-id="f2736-444">Ledig</span><span class="sxs-lookup"><span data-stu-id="f2736-444">Single</span></span>                 | <span data-ttu-id="f2736-445">Ledig</span><span class="sxs-lookup"><span data-stu-id="f2736-445">Single</span></span>               |
| <span data-ttu-id="f2736-446">Verwitwet</span><span class="sxs-lookup"><span data-stu-id="f2736-446">Widowed</span></span>                | <span data-ttu-id="f2736-447">Verwitwet</span><span class="sxs-lookup"><span data-stu-id="f2736-447">Widowed</span></span>              |
| <span data-ttu-id="f2736-448">Geschieden</span><span class="sxs-lookup"><span data-stu-id="f2736-448">Divorced</span></span>               | <span data-ttu-id="f2736-449">Geschieden</span><span class="sxs-lookup"><span data-stu-id="f2736-449">Divorced</span></span>             |
| <span data-ttu-id="f2736-450">Eingetragene Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="f2736-450">Registered Partnership</span></span> | <span data-ttu-id="f2736-451">Inländische Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="f2736-451">Domestic Partnership</span></span> |
| <span data-ttu-id="f2736-452">None</span><span class="sxs-lookup"><span data-stu-id="f2736-452">None</span></span>                   | <span data-ttu-id="f2736-453">None</span><span class="sxs-lookup"><span data-stu-id="f2736-453">None</span></span>                 |
| <span data-ttu-id="f2736-454">Freie Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="f2736-454">Cohabiting</span></span>             | <span data-ttu-id="f2736-455">Freie Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="f2736-455">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="f2736-456">Geschlecht</span><span class="sxs-lookup"><span data-stu-id="f2736-456">Gender</span></span>

<span data-ttu-id="f2736-457">Geschlechtsbezeichnungen werden Dayforce zugeordnet und werden – je nach Bedarf – in die akzeptierten Werte bei der Integration übersetzt.</span><span class="sxs-lookup"><span data-stu-id="f2736-457">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="f2736-458">Die folgende Tabelle zeigt, wie Geschlechtsbezeichnungen Dayforce zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="f2736-458">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="f2736-459">Talent</span><span class="sxs-lookup"><span data-stu-id="f2736-459">Talent</span></span>       | <span data-ttu-id="f2736-460">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f2736-460">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="f2736-461">Männlich</span><span class="sxs-lookup"><span data-stu-id="f2736-461">Male</span></span>         | <span data-ttu-id="f2736-462">Männlich</span><span class="sxs-lookup"><span data-stu-id="f2736-462">Male</span></span>            |
| <span data-ttu-id="f2736-463">Weiblich</span><span class="sxs-lookup"><span data-stu-id="f2736-463">Female</span></span>       | <span data-ttu-id="f2736-464">Weiblich</span><span class="sxs-lookup"><span data-stu-id="f2736-464">Female</span></span>          |
| <span data-ttu-id="f2736-465">Nicht spezifisch</span><span class="sxs-lookup"><span data-stu-id="f2736-465">Non-specific</span></span> | <span data-ttu-id="f2736-466">*Nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="f2736-466">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="f2736-467">Einkommenscodes</span><span class="sxs-lookup"><span data-stu-id="f2736-467">Earning codes</span></span>

<span data-ttu-id="f2736-468">Einkommenscodes bestimmen jeden Typ von Einkünften eindeutig, die Arbeitskräfte erhalten</span><span class="sxs-lookup"><span data-stu-id="f2736-468">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="f2736-469">Die Codes decken verschiedene Parameter ab, die sich auf Einkünfte beziehen, wie beispielsweise Buchhaltungsvorschriften, Steuergesetze, Berichterstellungsanforderungen und Bruttoausgleichsfähigkeit.</span><span class="sxs-lookup"><span data-stu-id="f2736-469">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="f2736-470">Wenn eine nicht unterstützte Häufigkeit verwendet wird, wird die Häufigkeit **Jeder Lohn** standardmäßig für die Berechnung verwendet.</span><span class="sxs-lookup"><span data-stu-id="f2736-470">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="f2736-471">Unterstützte Häufigkeiten</span><span class="sxs-lookup"><span data-stu-id="f2736-471">Supported frequencies</span></span>

- <span data-ttu-id="f2736-472">Alle</span><span class="sxs-lookup"><span data-stu-id="f2736-472">All</span></span>
- <span data-ttu-id="f2736-473">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="f2736-473">EVERYPAY</span></span>
- <span data-ttu-id="f2736-474">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="f2736-474">EACHPAYPERIOD</span></span>
- <span data-ttu-id="f2736-475">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="f2736-475">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="f2736-476">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="f2736-476">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="f2736-477">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2736-477">1OFMTH</span></span>
- <span data-ttu-id="f2736-478">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="f2736-478">LASTOFMTH</span></span>
- <span data-ttu-id="f2736-479">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2736-479">2OFMTH</span></span>
- <span data-ttu-id="f2736-480">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2736-480">3OFMTH</span></span>
- <span data-ttu-id="f2736-481">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2736-481">4OFMTH</span></span>
- <span data-ttu-id="f2736-482">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2736-482">5OFMTH</span></span>
- <span data-ttu-id="f2736-483">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2736-483">1N2OFMTH</span></span>
- <span data-ttu-id="f2736-484">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2736-484">3N4OFMTH</span></span>
- <span data-ttu-id="f2736-485">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2736-485">1N3OFMTH</span></span>
- <span data-ttu-id="f2736-486">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2736-486">1N4OFMTH</span></span>
- <span data-ttu-id="f2736-487">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2736-487">2N3OFMTH</span></span>
- <span data-ttu-id="f2736-488">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2736-488">2N4OFMTH</span></span>
- <span data-ttu-id="f2736-489">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2736-489">1N2N3OFMTH</span></span>
- <span data-ttu-id="f2736-490">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2736-490">1N2N4OFMTH</span></span>
- <span data-ttu-id="f2736-491">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2736-491">1N3N4OFMTH</span></span>
- <span data-ttu-id="f2736-492">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2736-492">2N3N4OFMTH</span></span>
- <span data-ttu-id="f2736-493">1N2N3N4OFMTH – 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2736-493">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="f2736-494">2N3N4N5OFMth – 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="f2736-494">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="f2736-495">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="f2736-495">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="f2736-496">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="f2736-496">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="f2736-497">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="f2736-497">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="f2736-498">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="f2736-498">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="f2736-499">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="f2736-499">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="f2736-500">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="f2736-500">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="f2736-501">Adressen</span><span class="sxs-lookup"><span data-stu-id="f2736-501">Addresses</span></span>

<span data-ttu-id="f2736-502">Die Kennung bestimmter Codes für Land oder Region, Bundesland/Kanton oder Landkreis (Gemeinde) erfordert spezifische Formate, die Dayforce und Anbieter innerhalb des Landes/innerhalb der Region erkennen können.</span><span class="sxs-lookup"><span data-stu-id="f2736-502">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="f2736-503">Obwohl das Format für Orte flexibel ist, muss jeder Ort einem Bundesland zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="f2736-503">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="f2736-504">Talent</span><span class="sxs-lookup"><span data-stu-id="f2736-504">Talent</span></span>          | <span data-ttu-id="f2736-505">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f2736-505">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="f2736-506">Land/Region</span><span class="sxs-lookup"><span data-stu-id="f2736-506">Country/Region</span></span>  | <span data-ttu-id="f2736-507">Ländercode</span><span class="sxs-lookup"><span data-stu-id="f2736-507">Country Code</span></span>          |
| <span data-ttu-id="f2736-508">Postleitzahl</span><span class="sxs-lookup"><span data-stu-id="f2736-508">Zip/Postal Code</span></span> | <span data-ttu-id="f2736-509">PLZ</span><span class="sxs-lookup"><span data-stu-id="f2736-509">Postal Code</span></span>           |
| <span data-ttu-id="f2736-510">Zustand</span><span class="sxs-lookup"><span data-stu-id="f2736-510">State</span></span>           | <span data-ttu-id="f2736-511">Bundeslandcode</span><span class="sxs-lookup"><span data-stu-id="f2736-511">State Code</span></span>            |
| <span data-ttu-id="f2736-512">Stadt</span><span class="sxs-lookup"><span data-stu-id="f2736-512">City</span></span>            | <span data-ttu-id="f2736-513">Stadt</span><span class="sxs-lookup"><span data-stu-id="f2736-513">City</span></span>                  |
| <span data-ttu-id="f2736-514">Verwaltungsbezirk</span><span class="sxs-lookup"><span data-stu-id="f2736-514">County</span></span>          | <span data-ttu-id="f2736-515">Landkreis (Gemeinde)</span><span class="sxs-lookup"><span data-stu-id="f2736-515">County (Municipality)</span></span> |
| <span data-ttu-id="f2736-516">Straße</span><span class="sxs-lookup"><span data-stu-id="f2736-516">Street</span></span>          | <span data-ttu-id="f2736-517">Adresszeile 1</span><span class="sxs-lookup"><span data-stu-id="f2736-517">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="f2736-518">Steuerregionen</span><span class="sxs-lookup"><span data-stu-id="f2736-518">Tax regions</span></span>

<span data-ttu-id="f2736-519">Steuerregionen werden verwendet, um die entsprechende Steuer festzulegen, die bei der Lohngenerierung angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="f2736-519">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="f2736-520">Steuerregionen werden Dayforce als Standortadressen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="f2736-520">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="f2736-521">Die Standardsteuerregion muss der aktiven Position der Arbeitskraft zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="f2736-521">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="f2736-522">Steuerregion (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-522">Tax region (required)</span></span>
- <span data-ttu-id="f2736-523">Land/Region (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-523">Country/Region (required)</span></span>
- <span data-ttu-id="f2736-524">Bundesland/Kanton (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-524">State (required)</span></span>
- <span data-ttu-id="f2736-525">Verwaltungsbezirk</span><span class="sxs-lookup"><span data-stu-id="f2736-525">County</span></span> 
- <span data-ttu-id="f2736-526">Ort (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f2736-526">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="f2736-527">Konfigurieren Ihrer Daten, um Lohn in Mexiko zu generieren</span><span class="sxs-lookup"><span data-stu-id="f2736-527">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="f2736-528">Wenn Sie Vergütung für Mitarbeiter in Mexiko generieren, müssen die folgenden Elemente konfiguriert werden:</span><span class="sxs-lookup"><span data-stu-id="f2736-528">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="f2736-529">Abteilungen sind für Positionen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f2736-529">Departments are required on positions.</span></span>
- <span data-ttu-id="f2736-530">Kostenstellen müssen als Finanzdimensionen festgelegt werden und müssen das erste Element in der standardmäßigen Finanzdimensions-Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="f2736-530">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="f2736-531">Stellentypen</span><span class="sxs-lookup"><span data-stu-id="f2736-531">Job types</span></span>

<span data-ttu-id="f2736-532">Stellentypen werden verwendet, um ähnliche Stellen in Kategorien zu gruppieren.</span><span class="sxs-lookup"><span data-stu-id="f2736-532">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="f2736-533">Stellentypen sind erforderlich, um Lohn in Mexiko zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="f2736-533">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="f2736-534">Beispiele für Stellentypen umfassen Voll- und Teilzeit oder festes Gehalt und Stundenlohn.</span><span class="sxs-lookup"><span data-stu-id="f2736-534">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="f2736-535">Stellentypen werden Dayforce als Lohnarten zugeordnet, die angeben, ob ein Mitarbeiter auf Stundenbasis bezahlt wird oder ein festes Gehalt bezieht.</span><span class="sxs-lookup"><span data-stu-id="f2736-535">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="f2736-536">Folgende Stellentypen und Beschreibungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f2736-536">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="f2736-537">Stellentyp</span><span class="sxs-lookup"><span data-stu-id="f2736-537">Job type</span></span>   | <span data-ttu-id="f2736-538">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f2736-538">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="f2736-539">Stündlich</span><span class="sxs-lookup"><span data-stu-id="f2736-539">Hourly</span></span>     | <span data-ttu-id="f2736-540">MX – Stundenbasis</span><span class="sxs-lookup"><span data-stu-id="f2736-540">MX Hourly</span></span>   |
| <span data-ttu-id="f2736-541">Fest angestellt</span><span class="sxs-lookup"><span data-stu-id="f2736-541">Salaried</span></span>   | <span data-ttu-id="f2736-542">MX – Fest angestellt</span><span class="sxs-lookup"><span data-stu-id="f2736-542">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="f2736-543">Positionstypen</span><span class="sxs-lookup"><span data-stu-id="f2736-543">Position types</span></span> 

<span data-ttu-id="f2736-544">Sie verwenden Positionstypen, um zu beschreiben, ob die Position Vollzeit, Teilzeit oder etwas anderes ist.</span><span class="sxs-lookup"><span data-stu-id="f2736-544">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="f2736-545">Positionstypen werden Dayforce als Lohnklassen zugeordnet, die angeben, ob ein Mitarbeiter in Vollzeit oder Teilzeit arbeitet.</span><span class="sxs-lookup"><span data-stu-id="f2736-545">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="f2736-546">Folgende Positionstypen und Beschreibungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f2736-546">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="f2736-547">Positionstyp</span><span class="sxs-lookup"><span data-stu-id="f2736-547">Position type</span></span>   | <span data-ttu-id="f2736-548">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f2736-548">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="f2736-549">Vollzeit</span><span class="sxs-lookup"><span data-stu-id="f2736-549">Full-time</span></span>       | <span data-ttu-id="f2736-550">Vollzeitmitarbeiter</span><span class="sxs-lookup"><span data-stu-id="f2736-550">Full time employee</span></span> |
| <span data-ttu-id="f2736-551">Teilzeit</span><span class="sxs-lookup"><span data-stu-id="f2736-551">Part-time</span></span>       | <span data-ttu-id="f2736-552">Teilzeitmitarbeiter</span><span class="sxs-lookup"><span data-stu-id="f2736-552">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="f2736-553">Ursachencodes</span><span class="sxs-lookup"><span data-stu-id="f2736-553">Reason codes</span></span>

<span data-ttu-id="f2736-554">Ursachencodes enthalten Informationen zum Status eines Mitarbeiters.</span><span class="sxs-lookup"><span data-stu-id="f2736-554">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="f2736-555">Ursachencodes werden Dayforce als Statusgründe zugeordnet, die den Grund für Änderungen bei der Position eines Mitarbeiters oder dem Beschäftigungsstatus angeben.</span><span class="sxs-lookup"><span data-stu-id="f2736-555">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="f2736-556">Folgende Ursachencodes und Beschreibungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f2736-556">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="f2736-557">Ursachencode</span><span class="sxs-lookup"><span data-stu-id="f2736-557">Reason code</span></span>            | <span data-ttu-id="f2736-558">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f2736-558">Description</span></span>                    | <span data-ttu-id="f2736-559">Zutreffende Szenarios</span><span class="sxs-lookup"><span data-stu-id="f2736-559">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="f2736-560">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="f2736-560">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="f2736-561">Abgang vor erster Lohnzahlung</span><span class="sxs-lookup"><span data-stu-id="f2736-561">Departure before first payroll</span></span> | <span data-ttu-id="f2736-562">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="f2736-562">Terminate worker</span></span>     |
| <span data-ttu-id="f2736-563">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="f2736-563">RESIGNATION</span></span>            | <span data-ttu-id="f2736-564">Kündigung durch Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="f2736-564">Resignation</span></span>                    | <span data-ttu-id="f2736-565">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="f2736-565">Terminate worker</span></span>     |
| <span data-ttu-id="f2736-566">PENSION</span><span class="sxs-lookup"><span data-stu-id="f2736-566">PENSION</span></span>                | <span data-ttu-id="f2736-567">Rente</span><span class="sxs-lookup"><span data-stu-id="f2736-567">Pension</span></span>                        | <span data-ttu-id="f2736-568">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="f2736-568">Terminate worker</span></span>     |
| <span data-ttu-id="f2736-569">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="f2736-569">TERMINATION</span></span>            | <span data-ttu-id="f2736-570">Beendigung</span><span class="sxs-lookup"><span data-stu-id="f2736-570">Termination</span></span>                    | <span data-ttu-id="f2736-571">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="f2736-571">Terminate worker</span></span>     |
| <span data-ttu-id="f2736-572">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="f2736-572">RETIREMENT</span></span>             | <span data-ttu-id="f2736-573">Ruhestand</span><span class="sxs-lookup"><span data-stu-id="f2736-573">Retirement</span></span>                     | <span data-ttu-id="f2736-574">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="f2736-574">Terminate worker</span></span>     |
| <span data-ttu-id="f2736-575">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="f2736-575">ABSENTEE</span></span>               | <span data-ttu-id="f2736-576">Abwesende Person</span><span class="sxs-lookup"><span data-stu-id="f2736-576">Absentee</span></span>                       | <span data-ttu-id="f2736-577">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="f2736-577">Terminate worker</span></span>     |
| <span data-ttu-id="f2736-578">OTHER</span><span class="sxs-lookup"><span data-stu-id="f2736-578">OTHER</span></span>                  | <span data-ttu-id="f2736-579">Andere Gründe</span><span class="sxs-lookup"><span data-stu-id="f2736-579">Other Reasons</span></span>                  | <span data-ttu-id="f2736-580">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="f2736-580">Terminate worker</span></span>     |
| <span data-ttu-id="f2736-581">CLOSURE</span><span class="sxs-lookup"><span data-stu-id="f2736-581">CLOSURE</span></span>                | <span data-ttu-id="f2736-582">Betriebsferien</span><span class="sxs-lookup"><span data-stu-id="f2736-582">Business Closure</span></span>               | <span data-ttu-id="f2736-583">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="f2736-583">Terminate worker</span></span>     |
| <span data-ttu-id="f2736-584">DEATH</span><span class="sxs-lookup"><span data-stu-id="f2736-584">DEATH</span></span>                  | <span data-ttu-id="f2736-585">Tod</span><span class="sxs-lookup"><span data-stu-id="f2736-585">Death</span></span>                          | <span data-ttu-id="f2736-586">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="f2736-586">Terminate worker</span></span>     |
| <span data-ttu-id="f2736-587">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="f2736-587">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="f2736-588">Beurlaubung</span><span class="sxs-lookup"><span data-stu-id="f2736-588">Leave of Absence</span></span>               | <span data-ttu-id="f2736-589">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="f2736-589">Terminate worker</span></span>     |
| <span data-ttu-id="f2736-590">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="f2736-590">CONTRACTEND</span></span>            | <span data-ttu-id="f2736-591">Vertragsende</span><span class="sxs-lookup"><span data-stu-id="f2736-591">End of Contract</span></span>                | <span data-ttu-id="f2736-592">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="f2736-592">Terminate worker</span></span>     |
| <span data-ttu-id="f2736-593">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="f2736-593">SALARYCHANGE</span></span>           | <span data-ttu-id="f2736-594">Gehaltsänderung</span><span class="sxs-lookup"><span data-stu-id="f2736-594">Change of Salary</span></span>               | <span data-ttu-id="f2736-595">Vergütung</span><span class="sxs-lookup"><span data-stu-id="f2736-595">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="f2736-596">Einstellungsbedingungen</span><span class="sxs-lookup"><span data-stu-id="f2736-596">Terms of employment</span></span>

<span data-ttu-id="f2736-597">Beschäftigungsbedingungen werden verwendet, um Kategorien von Beschäftigungsbedingungen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f2736-597">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="f2736-598">Die Bedingungen werden Dayforce als Beschäftigungsindikatorwerte zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="f2736-598">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="f2736-599">Die folgenden Bedingungen für Beschäftigung und Beschreibungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f2736-599">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="f2736-600">Einstellungsbedingungen</span><span class="sxs-lookup"><span data-stu-id="f2736-600">Terms of employment</span></span>   | <span data-ttu-id="f2736-601">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f2736-601">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="f2736-602">Regelmäßig</span><span class="sxs-lookup"><span data-stu-id="f2736-602">Regular</span></span>               | <span data-ttu-id="f2736-603">Regelmäßig</span><span class="sxs-lookup"><span data-stu-id="f2736-603">Regular</span></span>     |
| <span data-ttu-id="f2736-604">Direkt</span><span class="sxs-lookup"><span data-stu-id="f2736-604">Direct</span></span>                | <span data-ttu-id="f2736-605">Direkt</span><span class="sxs-lookup"><span data-stu-id="f2736-605">Direct</span></span>      |
| <span data-ttu-id="f2736-606">Praktikum</span><span class="sxs-lookup"><span data-stu-id="f2736-606">Internship</span></span>            | <span data-ttu-id="f2736-607">Praktikum</span><span class="sxs-lookup"><span data-stu-id="f2736-607">Internship</span></span>  |
| <span data-ttu-id="f2736-608">Unbefristet</span><span class="sxs-lookup"><span data-stu-id="f2736-608">Permanent</span></span>             | <span data-ttu-id="f2736-609">Unbefristet</span><span class="sxs-lookup"><span data-stu-id="f2736-609">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="f2736-610">Familienstand</span><span class="sxs-lookup"><span data-stu-id="f2736-610">Marital status</span></span>

<span data-ttu-id="f2736-611">Familienstandwerte werden Dayforce zugeordnet und werden – je nach Bedarf – in die akzeptierten Werte bei der Integration übersetzt.</span><span class="sxs-lookup"><span data-stu-id="f2736-611">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="f2736-612">Die folgende Tabelle zeigt, wie Familienstandwerte Dayforce zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="f2736-612">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="f2736-613">Talent</span><span class="sxs-lookup"><span data-stu-id="f2736-613">Talent</span></span>                 | <span data-ttu-id="f2736-614">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f2736-614">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="f2736-615">Verheiratet</span><span class="sxs-lookup"><span data-stu-id="f2736-615">Married</span></span>                | <span data-ttu-id="f2736-616">Verheiratet</span><span class="sxs-lookup"><span data-stu-id="f2736-616">Married</span></span>                   |
| <span data-ttu-id="f2736-617">Ledig</span><span class="sxs-lookup"><span data-stu-id="f2736-617">Single</span></span>                 | <span data-ttu-id="f2736-618">Ledig</span><span class="sxs-lookup"><span data-stu-id="f2736-618">Single</span></span>                    |
| <span data-ttu-id="f2736-619">Verwitwet</span><span class="sxs-lookup"><span data-stu-id="f2736-619">Widowed</span></span>                | <span data-ttu-id="f2736-620">Verwitwet</span><span class="sxs-lookup"><span data-stu-id="f2736-620">Widowed</span></span>                   |
| <span data-ttu-id="f2736-621">Geschieden</span><span class="sxs-lookup"><span data-stu-id="f2736-621">Divorced</span></span>               | <span data-ttu-id="f2736-622">Geschieden</span><span class="sxs-lookup"><span data-stu-id="f2736-622">Divorced</span></span>                  |
| <span data-ttu-id="f2736-623">Eingetragene Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="f2736-623">Registered Partnership</span></span> | <span data-ttu-id="f2736-624">Inländische Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="f2736-624">Domestic Partnership</span></span>      |
| <span data-ttu-id="f2736-625">None</span><span class="sxs-lookup"><span data-stu-id="f2736-625">None</span></span>                   | <span data-ttu-id="f2736-626">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="f2736-626">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="f2736-627">Freie Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="f2736-627">Cohabiting</span></span>             | <span data-ttu-id="f2736-628">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="f2736-628">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="f2736-629">Geschlecht</span><span class="sxs-lookup"><span data-stu-id="f2736-629">Gender</span></span>

<span data-ttu-id="f2736-630">Geschlechtsbezeichnungen werden Dayforce zugeordnet und werden – je nach Bedarf – in die akzeptierten Werte bei der Integration übersetzt.</span><span class="sxs-lookup"><span data-stu-id="f2736-630">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="f2736-631">Die folgende Tabelle zeigt, wie Geschlechtsbezeichnungen Dayforce zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="f2736-631">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="f2736-632">Talent</span><span class="sxs-lookup"><span data-stu-id="f2736-632">Talent</span></span>       | <span data-ttu-id="f2736-633">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f2736-633">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="f2736-634">Männlich</span><span class="sxs-lookup"><span data-stu-id="f2736-634">Male</span></span>         | <span data-ttu-id="f2736-635">Männlich</span><span class="sxs-lookup"><span data-stu-id="f2736-635">Male</span></span>                      |
| <span data-ttu-id="f2736-636">Weiblich</span><span class="sxs-lookup"><span data-stu-id="f2736-636">Female</span></span>       | <span data-ttu-id="f2736-637">Weiblich</span><span class="sxs-lookup"><span data-stu-id="f2736-637">Female</span></span>                    |
| <span data-ttu-id="f2736-638">Nicht spezifisch</span><span class="sxs-lookup"><span data-stu-id="f2736-638">Non-specific</span></span> | <span data-ttu-id="f2736-639">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="f2736-639">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="f2736-640">Zahlungsweise</span><span class="sxs-lookup"><span data-stu-id="f2736-640">Payment method</span></span>

<span data-ttu-id="f2736-641">Zahlungsmethoden geben dem Mitarbeiter und dem Unternehmen die Möglichkeit zu beschreiben, wie Mitarbeiter bezahlt werden.</span><span class="sxs-lookup"><span data-stu-id="f2736-641">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="f2736-642">Zahlungsmethoden werden Dayforce zugeordnet und werden – je nach Bedarf – in die akzeptierten Werte bei der Integration übersetzt.</span><span class="sxs-lookup"><span data-stu-id="f2736-642">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="f2736-643">Die folgende Tabelle zeigt, wie Zahlungsmethoden Dayforce zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="f2736-643">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="f2736-644">Talent</span><span class="sxs-lookup"><span data-stu-id="f2736-644">Talent</span></span>             | <span data-ttu-id="f2736-645">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f2736-645">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="f2736-646">Bargeld</span><span class="sxs-lookup"><span data-stu-id="f2736-646">Cash</span></span>               | <span data-ttu-id="f2736-647">Bargeld</span><span class="sxs-lookup"><span data-stu-id="f2736-647">Cash</span></span>                      |
| <span data-ttu-id="f2736-648">Elektronische Zahlung</span><span class="sxs-lookup"><span data-stu-id="f2736-648">Electronic Payment</span></span> | <span data-ttu-id="f2736-649">Übertragen</span><span class="sxs-lookup"><span data-stu-id="f2736-649">Transfer</span></span>                  |
| <span data-ttu-id="f2736-650">Scheck</span><span class="sxs-lookup"><span data-stu-id="f2736-650">Check</span></span>              | <span data-ttu-id="f2736-651">Scheck</span><span class="sxs-lookup"><span data-stu-id="f2736-651">Cheque</span></span>                    |
| <span data-ttu-id="f2736-652">Bankwechsel</span><span class="sxs-lookup"><span data-stu-id="f2736-652">Bank Draft</span></span>         | <span data-ttu-id="f2736-653">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="f2736-653">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="f2736-654">Sonstige</span><span class="sxs-lookup"><span data-stu-id="f2736-654">Other</span></span>              | <span data-ttu-id="f2736-655">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="f2736-655">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="f2736-656">Bankkontotyp</span><span class="sxs-lookup"><span data-stu-id="f2736-656">Bank account type</span></span>

<span data-ttu-id="f2736-657">Bankkontotypen werden für elektronische Zahlungen an Mitarbeiter verwendet.</span><span class="sxs-lookup"><span data-stu-id="f2736-657">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="f2736-658">Bankkontotypen werden Dayforce als Übergweisungskontoinformationen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="f2736-658">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="f2736-659">Die Bankkontotypen werden bei Bedarf zu den akzeptierten Werte nach der Integration übersetzt.</span><span class="sxs-lookup"><span data-stu-id="f2736-659">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="f2736-660">Talent</span><span class="sxs-lookup"><span data-stu-id="f2736-660">Talent</span></span>            | <span data-ttu-id="f2736-661">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f2736-661">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="f2736-662">Girokonto</span><span class="sxs-lookup"><span data-stu-id="f2736-662">Checking Account</span></span>  | <span data-ttu-id="f2736-663">Girokonto</span><span class="sxs-lookup"><span data-stu-id="f2736-663">CheckingAccount</span></span>           |
| <span data-ttu-id="f2736-664">Lohnkonto</span><span class="sxs-lookup"><span data-stu-id="f2736-664">Payroll Account</span></span>   | <span data-ttu-id="f2736-665">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="f2736-665">PayrollAccount</span></span>            |
| <span data-ttu-id="f2736-666">Sparkonto</span><span class="sxs-lookup"><span data-stu-id="f2736-666">Savings Account</span></span>   | <span data-ttu-id="f2736-667">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="f2736-667">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="f2736-668">BankGirot-Konto</span><span class="sxs-lookup"><span data-stu-id="f2736-668">BankGirot account</span></span> | <span data-ttu-id="f2736-669">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="f2736-669">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="f2736-670">PlusGirot-Konto</span><span class="sxs-lookup"><span data-stu-id="f2736-670">PlusGirot account</span></span> | <span data-ttu-id="f2736-671">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="f2736-671">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="f2736-672">Einkommenscodes</span><span class="sxs-lookup"><span data-stu-id="f2736-672">Earning codes</span></span>

<span data-ttu-id="f2736-673">Einkommenscodes bestimmen jeden Typ von Einkünften eindeutig, die Arbeitskräfte erhalten</span><span class="sxs-lookup"><span data-stu-id="f2736-673">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="f2736-674">Die Codes decken verschiedene Parameter ab, die sich auf Einkünfte beziehen, wie beispielsweise Buchhaltungsvorschriften, Steuergesetze, Berichterstellungsanforderungen und Bruttoausgleichsfähigkeit.</span><span class="sxs-lookup"><span data-stu-id="f2736-674">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="f2736-675">Wenn eine nicht unterstützte Häufigkeit verwendet wird, wird die Häufigkeit **Jeder Lohn** standardmäßig für die Berechnung verwendet.</span><span class="sxs-lookup"><span data-stu-id="f2736-675">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="f2736-676">Unterstützte Häufigkeiten</span><span class="sxs-lookup"><span data-stu-id="f2736-676">Supported frequencies</span></span>

- <span data-ttu-id="f2736-677">Alle</span><span class="sxs-lookup"><span data-stu-id="f2736-677">All</span></span>
- <span data-ttu-id="f2736-678">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="f2736-678">EVERYPAY</span></span>
- <span data-ttu-id="f2736-679">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="f2736-679">EACHPAYPERIOD</span></span>
- <span data-ttu-id="f2736-680">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="f2736-680">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="f2736-681">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="f2736-681">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="f2736-682">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2736-682">1OFMTH</span></span>
- <span data-ttu-id="f2736-683">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="f2736-683">LASTOFMTH</span></span>
- <span data-ttu-id="f2736-684">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2736-684">2OFMTH</span></span>
- <span data-ttu-id="f2736-685">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2736-685">3OFMTH</span></span>
- <span data-ttu-id="f2736-686">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2736-686">4OFMTH</span></span>
- <span data-ttu-id="f2736-687">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2736-687">5OFMTH</span></span>
- <span data-ttu-id="f2736-688">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2736-688">1N2OFMTH</span></span>
- <span data-ttu-id="f2736-689">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2736-689">3N4OFMTH</span></span>
- <span data-ttu-id="f2736-690">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2736-690">1N3OFMTH</span></span>
- <span data-ttu-id="f2736-691">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2736-691">1N4OFMTH</span></span>
- <span data-ttu-id="f2736-692">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2736-692">2N3OFMTH</span></span>
- <span data-ttu-id="f2736-693">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2736-693">2N4OFMTH</span></span>
- <span data-ttu-id="f2736-694">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2736-694">1N2N3OFMTH</span></span>
- <span data-ttu-id="f2736-695">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2736-695">1N2N4OFMTH</span></span>
- <span data-ttu-id="f2736-696">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2736-696">1N3N4OFMTH</span></span>
- <span data-ttu-id="f2736-697">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2736-697">2N3N4OFMTH</span></span>
- <span data-ttu-id="f2736-698">1N2N3N4OFMTH – 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="f2736-698">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="f2736-699">2N3N4N5OFMth – 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="f2736-699">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="f2736-700">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="f2736-700">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="f2736-701">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="f2736-701">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="f2736-702">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="f2736-702">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="f2736-703">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="f2736-703">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="f2736-704">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="f2736-704">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="f2736-705">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="f2736-705">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="f2736-706">Adressen</span><span class="sxs-lookup"><span data-stu-id="f2736-706">Addresses</span></span>

<span data-ttu-id="f2736-707">Die Kennung bestimmter Codes für Land oder Region, Bundesland/Kanton oder Landkreis (Gemeinde) erfordert spezifische Formate, die Dayforce und Anbieter innerhalb des Landes/innerhalb der Region erkennen können.</span><span class="sxs-lookup"><span data-stu-id="f2736-707">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="f2736-708">Obwohl das Format für Orte flexibel ist, muss jeder Ort einem Bundesland zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="f2736-708">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="f2736-709">Talent</span><span class="sxs-lookup"><span data-stu-id="f2736-709">Talent</span></span>              | <span data-ttu-id="f2736-710">Dayforce</span><span class="sxs-lookup"><span data-stu-id="f2736-710">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="f2736-711">Land/Region</span><span class="sxs-lookup"><span data-stu-id="f2736-711">Country/Region</span></span>      | <span data-ttu-id="f2736-712">Ländercode</span><span class="sxs-lookup"><span data-stu-id="f2736-712">Country Code</span></span>          |
| <span data-ttu-id="f2736-713">Postleitzahl</span><span class="sxs-lookup"><span data-stu-id="f2736-713">Zip/Postal Code</span></span>     | <span data-ttu-id="f2736-714">PLZ</span><span class="sxs-lookup"><span data-stu-id="f2736-714">Postal Code</span></span>           |
| <span data-ttu-id="f2736-715">Zustand</span><span class="sxs-lookup"><span data-stu-id="f2736-715">State</span></span>               | <span data-ttu-id="f2736-716">Bundeslandcode</span><span class="sxs-lookup"><span data-stu-id="f2736-716">State Code</span></span>            |
| <span data-ttu-id="f2736-717">Stadt</span><span class="sxs-lookup"><span data-stu-id="f2736-717">City</span></span>                | <span data-ttu-id="f2736-718">Stadt</span><span class="sxs-lookup"><span data-stu-id="f2736-718">City</span></span>                  |
| <span data-ttu-id="f2736-719">Verwaltungsbezirk</span><span class="sxs-lookup"><span data-stu-id="f2736-719">County</span></span>              | <span data-ttu-id="f2736-720">Landkreis (Gemeinde)</span><span class="sxs-lookup"><span data-stu-id="f2736-720">County (Municipality)</span></span> |
| <span data-ttu-id="f2736-721">Straße</span><span class="sxs-lookup"><span data-stu-id="f2736-721">Street</span></span>              | <span data-ttu-id="f2736-722">Adresszeile 1</span><span class="sxs-lookup"><span data-stu-id="f2736-722">Address Line 1</span></span>        |
| <span data-ttu-id="f2736-723">Hausnummer</span><span class="sxs-lookup"><span data-stu-id="f2736-723">Street Number</span></span>       | <span data-ttu-id="f2736-724">Adresszeile 2</span><span class="sxs-lookup"><span data-stu-id="f2736-724">Address Line 2</span></span>        |
| <span data-ttu-id="f2736-725">Gebäudeergänzung</span><span class="sxs-lookup"><span data-stu-id="f2736-725">Building Complement</span></span> | <span data-ttu-id="f2736-726">Adresszeile 5</span><span class="sxs-lookup"><span data-stu-id="f2736-726">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="f2736-727">Ausweisnummer</span><span class="sxs-lookup"><span data-stu-id="f2736-727">Passport number</span></span>

<span data-ttu-id="f2736-728">Mitarbeiter können Ausweisinformationen melden.</span><span class="sxs-lookup"><span data-stu-id="f2736-728">Employees can declare passport information.</span></span> <span data-ttu-id="f2736-729">Diese Informationen haben den Kennungstyp **Ausweis** und sind in Dayforce als Teil der für Mexiko spezifischen Informationen eines Mitarbeiters integriert.</span><span class="sxs-lookup"><span data-stu-id="f2736-729">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="f2736-730">Kennungstyp = „Ausweis”</span><span class="sxs-lookup"><span data-stu-id="f2736-730">Identification Type = "Passport"</span></span>
- <span data-ttu-id="f2736-731">Ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="f2736-731">Issued Date</span></span>
- <span data-ttu-id="f2736-732">Ablaufdatum</span><span class="sxs-lookup"><span data-stu-id="f2736-732">Expiration Date</span></span>

<span data-ttu-id="f2736-733">Mitarbeiter können mehrere Kennungsnummern des Kennungstyps **Ausweis** melden.</span><span class="sxs-lookup"><span data-stu-id="f2736-733">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="f2736-734">Jedoch wird nur der aktuell aktive Ausweiseintrag in Dayforce integriert.</span><span class="sxs-lookup"><span data-stu-id="f2736-734">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="f2736-735">Wenn alle Ausweiseinträge abgelaufen sind, ist der Ausweis, der zuletzt ausgestellt wurde, in Dayforce integriert.</span><span class="sxs-lookup"><span data-stu-id="f2736-735">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>
