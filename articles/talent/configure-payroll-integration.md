---
title: Die Lohnintegration zwischen Talent und Dayforce konfigurieren
description: In diesem Thema wird erläutert, wie Sie die Integration zwischen Microsoft Dynamics 365 for Talent und Ceridian Dayforce konfigurieren, damit Sie den Zahlungslauf verarbeiten können.
author: jcart1106
manager: AnnBe
ms.date: 07/10/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fcddf82cffb9f0ba94b83eb21809b810585ebc9e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "304499"
---
# <a name="configure-the-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="b3dc6-103">Lohnintegration zwischen Talent und Dayforce konfigurieren</span><span class="sxs-lookup"><span data-stu-id="b3dc6-103">Configure the payroll integration between Talent and Dayforce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b3dc6-104">Die Integration zwischen Microsoft Dynamics 365 for Talent und Ceridian Dayforce beruht auf mehreren Konfigurationsschritten, die in diesem Thema beschrieben sind.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-104">The integration between Microsoft Dynamics 365 for Talent and Ceridian Dayforce relies on several configuration steps that are described in this topic.</span></span> <span data-ttu-id="b3dc6-105">Sie müssen die Integration sowohl in Talent als auch in Dayforce konfigurieren, bevor Sie einen Zahllauf verarbeiten können.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-105">You must configure the integration in both Talent and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="b3dc6-106">Wenn Sie einen Dienst wie Dayforce verwenden, um Zahlläufe abzuschließen, müssen Sie die Integration in Talent ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-106">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Talent.</span></span> <span data-ttu-id="b3dc6-107">Die Integration erfordert bestimmte Daten aus Talent.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-107">The integration requires specific data from Talent.</span></span> <span data-ttu-id="b3dc6-108">Daher müssen Sie überprüfen, dass die Daten, die Dayforce zugeordnet sind, in Talent in einer Weise konfiguriert werden, die die Integration unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-108">Therefore, you must verify that data that is mapped to Dayforce is configured in Talent in a manner that supports the integration.</span></span> <span data-ttu-id="b3dc6-109">Bei der Integration werden die folgenden allgemeinen Kategorien von Daten verwendet:</span><span class="sxs-lookup"><span data-stu-id="b3dc6-109">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="b3dc6-110">Personalverwaltungsdaten</span><span class="sxs-lookup"><span data-stu-id="b3dc6-110">Human resources data</span></span>
- <span data-ttu-id="b3dc6-111">Vergütungsdaten</span><span class="sxs-lookup"><span data-stu-id="b3dc6-111">Compensation data</span></span>
- <span data-ttu-id="b3dc6-112">Lohndaten, wie Lohnzyklen, Lohnperioden und Einkommenscodes</span><span class="sxs-lookup"><span data-stu-id="b3dc6-112">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="b3dc6-113">Arbeitskraftdaten</span><span class="sxs-lookup"><span data-stu-id="b3dc6-113">Worker data</span></span>

<span data-ttu-id="b3dc6-114">In diesem Thema werden die Schritte beschrieben, die Sie befolgen müssen, um die Integration zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-114">This topic describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="b3dc6-115">Es werden auch die Datentypen und die Konfigurationsdetails erklärt, die für die Integration erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-115">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="b3dc6-116">Die Integration aktivieren</span><span class="sxs-lookup"><span data-stu-id="b3dc6-116">Enable the integration</span></span>

<span data-ttu-id="b3dc6-117">In Talent müssen Sie die Integration aktivieren und die Konfigurationsinformationen eingeben, um eine Verbindung mit Dayforce herzustellen.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-117">In Talent, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="b3dc6-118">Wenn Sie möchten, dass die erstellte Hauptbuchtransaktion in Microsoft Dynamics 365 for Finance and Operations importiert wird, müssen Sie auch ein Microsoft Azure-Speicherkonto einrichten und die Azure Storage-Verbindungszeichenfolge in Finance and Operations eingeben.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-118">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 for Finance and Operations, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance and Operations.</span></span>

<span data-ttu-id="b3dc6-119">Um die Integration in Talent zu aktivieren, gehen Sie folgendermaßen vor.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-119">To turn on the integration in Talent, follow these steps.</span></span>

1. <span data-ttu-id="b3dc6-120">Wählen Sie auf der Seite **Systemverwaltung** die Option **Integrationskonfiguration** aus.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-120">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="b3dc6-121">Geben Sie den sicheren Datenübertragungsprotokoll-(FTP)-Endpunkt und den sicheren FTP-Ordnerpfad ein.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-121">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="b3dc6-122">Geben Sie den Benutzernamen und das Kennwort des Benutzers ein, der auf den sicheren FTP-Endpunkt und Ordnerpfad zugreift.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-122">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="b3dc6-123">Testen Sie die Verbindung nach Bedarf, und legen Sie die Option **Lohnintegration aktivieren** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-123">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="b3dc6-124">Wenn die Integration aktiviert ist, werden Datenexportpaket und Dateien erstellt und die Häufigkeit wird festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-124">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="b3dc6-125">Sie können diese Häufigkeit nach Bedarf ändern.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-125">You can change this frequency as you require.</span></span>

<span data-ttu-id="b3dc6-126">Weitere Informationen zu Azure-Speicherkonten und Azure Storage-Verbindungszeichenfolgen finden Sie in den folgenden Azure-Themen:</span><span class="sxs-lookup"><span data-stu-id="b3dc6-126">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure topics:</span></span>

- [<span data-ttu-id="b3dc6-127">Über Azure-Speicherkonten</span><span class="sxs-lookup"><span data-stu-id="b3dc6-127">About Azure storage accounts</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="b3dc6-128">Azure Storage-Verbindungszeichenfolgen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="b3dc6-128">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-configure-connection-string)

## <a name="configure-your-data"></a><span data-ttu-id="b3dc6-129">Ihre Daten konfigurieren</span><span class="sxs-lookup"><span data-stu-id="b3dc6-129">Configure your data</span></span> 

<span data-ttu-id="b3dc6-130">Um die Lohnbuchung zu verarbeiten, müssen Sie Personalverwaltungsdaten in Talent konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-130">To process payroll, you must configure human resource data in Talent.</span></span> <span data-ttu-id="b3dc6-131">Sie müssen Organisationsdaten, wie Stellen und Positionen, zusammen mit Vorteilen Vergütungsinformationen einrichten.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-131">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="b3dc6-132">Diese Informationen stellen Beschäftigung, Lohn und die Abzugsinformationen bereit, die zur Generierung der Mitarbeiterentlohnung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-132">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="b3dc6-133">Personalverwaltungsdaten</span><span class="sxs-lookup"><span data-stu-id="b3dc6-133">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="b3dc6-134">Vergütungen</span><span class="sxs-lookup"><span data-stu-id="b3dc6-134">Benefits</span></span> 

<span data-ttu-id="b3dc6-135">Die Personalverwaltung stellt eine Reihe von Tools für die Einrichtung und Verwaltung der Vorteile, Abzüge und Vergütungspläne der Arbeitskräfte bereit, die eine Organisation für seine Arbeitskräfte anbietet oder verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-135">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="b3dc6-136">Wenn Sie Vorteile erstellen, sollten Sie folgende Daten und Konfigurationen bedenken, die in Dayforce verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-136">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="b3dc6-137">Vorteilspläne</span><span class="sxs-lookup"><span data-stu-id="b3dc6-137">Benefit plans</span></span>

- <span data-ttu-id="b3dc6-138">Plan (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-138">Plan (required)</span></span>
- <span data-ttu-id="b3dc6-139">Typ (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-139">Type (required)</span></span>
- <span data-ttu-id="b3dc6-140">Lohnauswirkung (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-140">Payroll impact (required)</span></span>
- <span data-ttu-id="b3dc6-141">Rückstände wiederherstellen</span><span class="sxs-lookup"><span data-stu-id="b3dc6-141">Recover arrears</span></span>
- <span data-ttu-id="b3dc6-142">Abzugsverfahren</span><span class="sxs-lookup"><span data-stu-id="b3dc6-142">Deduction method</span></span>
- <span data-ttu-id="b3dc6-143">Abzugspriorität</span><span class="sxs-lookup"><span data-stu-id="b3dc6-143">Deduction priority</span></span>
- <span data-ttu-id="b3dc6-144">Periode eingrenzen</span><span class="sxs-lookup"><span data-stu-id="b3dc6-144">Limit period</span></span>
- <span data-ttu-id="b3dc6-145">Limitbetrag</span><span class="sxs-lookup"><span data-stu-id="b3dc6-145">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="b3dc6-146">Vergütungen</span><span class="sxs-lookup"><span data-stu-id="b3dc6-146">Benefits</span></span>

- <span data-ttu-id="b3dc6-147">Plan (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-147">Plan (required)</span></span>
- <span data-ttu-id="b3dc6-148">Typ (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-148">Type (required)</span></span>
- <span data-ttu-id="b3dc6-149">Option (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-149">Option (required)</span></span>
- <span data-ttu-id="b3dc6-150">Vorteilskennung (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-150">Benefit ID (required)</span></span>
- <span data-ttu-id="b3dc6-151">Häufigkeit</span><span class="sxs-lookup"><span data-stu-id="b3dc6-151">Frequency</span></span>
- <span data-ttu-id="b3dc6-152">Basis</span><span class="sxs-lookup"><span data-stu-id="b3dc6-152">Basis</span></span>
- <span data-ttu-id="b3dc6-153">Betrag oder Satz</span><span class="sxs-lookup"><span data-stu-id="b3dc6-153">Amount or rate</span></span>
- <span data-ttu-id="b3dc6-154">Einkommenscode</span><span class="sxs-lookup"><span data-stu-id="b3dc6-154">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="b3dc6-155">Unterstützte Häufigkeiten</span><span class="sxs-lookup"><span data-stu-id="b3dc6-155">Supported frequencies</span></span> 

- <span data-ttu-id="b3dc6-156">Wöchentlich</span><span class="sxs-lookup"><span data-stu-id="b3dc6-156">Weekly</span></span>
- <span data-ttu-id="b3dc6-157">14-tägig</span><span class="sxs-lookup"><span data-stu-id="b3dc6-157">Bi-weekly</span></span>
- <span data-ttu-id="b3dc6-158">Halbmonatlich</span><span class="sxs-lookup"><span data-stu-id="b3dc6-158">Semi-monthly</span></span>
- <span data-ttu-id="b3dc6-159">Monatlich</span><span class="sxs-lookup"><span data-stu-id="b3dc6-159">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="b3dc6-160">Unterstützte Basen</span><span class="sxs-lookup"><span data-stu-id="b3dc6-160">Supported bases</span></span> 

- <span data-ttu-id="b3dc6-161">Fester Betrag</span><span class="sxs-lookup"><span data-stu-id="b3dc6-161">Fixed amount</span></span>
- <span data-ttu-id="b3dc6-162">Prozent des Einkommens</span><span class="sxs-lookup"><span data-stu-id="b3dc6-162">Percent of earnings</span></span>
- <span data-ttu-id="b3dc6-163">Produktive Stunden</span><span class="sxs-lookup"><span data-stu-id="b3dc6-163">Productive hours</span></span>

<span data-ttu-id="b3dc6-164">Dayforce erstellt die folgenden Abzüge, basierend auf den Lohnauswirkungen, die im Vorteilsplan definiert sind.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-164">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="b3dc6-165">Auswahl in Talent</span><span class="sxs-lookup"><span data-stu-id="b3dc6-165">Selection in Talent</span></span>        | <span data-ttu-id="b3dc6-166">Ergebnis in Dayforce</span><span class="sxs-lookup"><span data-stu-id="b3dc6-166">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="b3dc6-167">None</span><span class="sxs-lookup"><span data-stu-id="b3dc6-167">None</span></span>                       | <span data-ttu-id="b3dc6-168">Es wird kein Abzug erstellt.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-168">No deduction is created.</span></span>                      |
| <span data-ttu-id="b3dc6-169">Nur Abzug</span><span class="sxs-lookup"><span data-stu-id="b3dc6-169">Deduction only</span></span>             | <span data-ttu-id="b3dc6-170">Ein Mitarbeiterabzug wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-170">An employee deduction is created.</span></span>             |
| <span data-ttu-id="b3dc6-171">Nur Beitrag</span><span class="sxs-lookup"><span data-stu-id="b3dc6-171">Contribution only</span></span>          | <span data-ttu-id="b3dc6-172">Ein Arbeitgeberabzug wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-172">An employer deduction is created.</span></span>             |
| <span data-ttu-id="b3dc6-173">Abzug und Beitrag</span><span class="sxs-lookup"><span data-stu-id="b3dc6-173">Deduction and contribution</span></span> | <span data-ttu-id="b3dc6-174">Mitarbeiter- und Arbeitgeberabzüge werden erstellt.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-174">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="b3dc6-175">Weitere Informationen darüber, wie Sie ein Vorteilsprogramm definieren und verwalten finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="b3dc6-175">For more information about how to define and manage a benefits program, see the following topics:</span></span>

- [<span data-ttu-id="b3dc6-176">Mitarbeitervergütungsprogramm bereitstellen</span><span class="sxs-lookup"><span data-stu-id="b3dc6-176">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="b3dc6-177">Neuen Vorteil erstellen</span><span class="sxs-lookup"><span data-stu-id="b3dc6-177">Create a new benefit</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="b3dc6-178">Vorteilsberechtigungsregeln und Richtlinien definieren</span><span class="sxs-lookup"><span data-stu-id="b3dc6-178">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="b3dc6-179">Vorteile von Arbeitskräften registrieren und entfernen</span><span class="sxs-lookup"><span data-stu-id="b3dc6-179">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="b3dc6-180">Vergütung</span><span class="sxs-lookup"><span data-stu-id="b3dc6-180">Compensation</span></span> 

<span data-ttu-id="b3dc6-181">Die Vergütungsverwaltung dient zum Steuern der Abwicklung des Grundlohns und der Prämien.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-181">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="b3dc6-182">Sie steuern den festen Grundlohn eines Mitarbeiters und dessen Lohnsteigerungen nach Plänen für feste Vergütung.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-182">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="b3dc6-183">Die Zahlung leistungsbezogener Prämien, wie Boni, Leistungsprämien, Aktienoptionen und -überlassungen sowie Einmalprämien werden durch Pläne für variable Vergütung gesteuert.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-183">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="b3dc6-184">Dayforce verwendet Vergütungsinformationen, um einen Stunden- oder Jahressatz für einen Mitarbeiter zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-184">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="b3dc6-185">Feste Vergütungspläne und Lohnsatzumrechnungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-185">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="b3dc6-186">Mitarbeiter müssen einem festen Vergütungsplan zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-186">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="b3dc6-187">Weitere Informationen zu Vergütungsplänen finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="b3dc6-187">For more information about compensation plans, see the following topics:</span></span>

- [<span data-ttu-id="b3dc6-188">Feste Vergütungspläne erstellen</span><span class="sxs-lookup"><span data-stu-id="b3dc6-188">Create fixed compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="b3dc6-189">Variable Vergütungspläne erstellen</span><span class="sxs-lookup"><span data-stu-id="b3dc6-189">Create variable compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="b3dc6-190">Gehalts-/Vergütungsstruktur und -pläne entwickeln</span><span class="sxs-lookup"><span data-stu-id="b3dc6-190">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="b3dc6-191">Vergütung verarbeiten</span><span class="sxs-lookup"><span data-stu-id="b3dc6-191">Process compensation</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="b3dc6-192">Vergütungsprozess definieren und Ergebnisse berechnen</span><span class="sxs-lookup"><span data-stu-id="b3dc6-192">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="b3dc6-193">Einen Mitarbeiters in einem Plan für eine feste Vergütung registrieren</span><span class="sxs-lookup"><span data-stu-id="b3dc6-193">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="b3dc6-194">Einen Mitarbeiter in einem Plan für variable Vergütung registrieren</span><span class="sxs-lookup"><span data-stu-id="b3dc6-194">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="b3dc6-195">Stellentyp</span><span class="sxs-lookup"><span data-stu-id="b3dc6-195">Jobs</span></span> 

<span data-ttu-id="b3dc6-196">Eine Stelle ist eine Sammlung der Aufgaben und Zuständigkeiten, die für eine Person, die eine Tätigkeit ausführt, obligatorisch sind.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-196">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="b3dc6-197">Weitere Informationen finden Sie in folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="b3dc6-197">For more information, see the following topics:</span></span>

- [<span data-ttu-id="b3dc6-198">Komponenten einer Stelle einrichten</span><span class="sxs-lookup"><span data-stu-id="b3dc6-198">Setting up the components of a job</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="b3dc6-199">Neue Einzelvorgänge definieren</span><span class="sxs-lookup"><span data-stu-id="b3dc6-199">Define new jobs</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="b3dc6-200">Positionen</span><span class="sxs-lookup"><span data-stu-id="b3dc6-200">Positions</span></span>

<span data-ttu-id="b3dc6-201">Eine Position ist eine einzelne Instanz eines Einzelvorgangs.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-201">A position is an individual instance of a job.</span></span> <span data-ttu-id="b3dc6-202">Beispielsweise ist die Position „Verkaufsleiter (Ost)” eine der Positionen, die der Stelle „Verkaufsleiter” zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-202">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="b3dc6-203">Eine Position ist in einer Abteilung vorhanden.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-203">A position exists in a department.</span></span> <span data-ttu-id="b3dc6-204">Nur jeweils eine Arbeitskraft kann jeder Position zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-204">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="b3dc6-205">Bedenken Sie die folgenden Daten und Konfigurationen, wenn Sie Positionen einrichten:</span><span class="sxs-lookup"><span data-stu-id="b3dc6-205">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="b3dc6-206">Position (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-206">Position (required)</span></span>
- <span data-ttu-id="b3dc6-207">Beschreibung (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-207">Description (required)</span></span>
- <span data-ttu-id="b3dc6-208">Stelle (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-208">Job (required)</span></span>
- <span data-ttu-id="b3dc6-209">Abteilung (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-209">Department (required)</span></span>
- <span data-ttu-id="b3dc6-210">Positionstyp (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-210">Position type (required)</span></span>
- <span data-ttu-id="b3dc6-211">Vollzeitäquivalent</span><span class="sxs-lookup"><span data-stu-id="b3dc6-211">Full-time equivalent</span></span>
- <span data-ttu-id="b3dc6-212">Normale Stunden pro Jahr (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-212">Annual regular hours (required)</span></span>
- <span data-ttu-id="b3dc6-213">Gezahlt von der juristischen Person (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-213">Paid by legal entity (required)</span></span>
- <span data-ttu-id="b3dc6-214">Lohnzyklus (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-214">Pay cycle (required)</span></span>
- <span data-ttu-id="b3dc6-215">Standardfinanzdimension – Kostenstelle (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-215">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="b3dc6-216">Arbeitskraftzuweisung – Arbeitskraft, Zuweisungsanfang, Zuweisungsende, Ursachencode</span><span class="sxs-lookup"><span data-stu-id="b3dc6-216">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="b3dc6-217">Wenn mehrere Positionen in derselben Abteilung derselben Stelle zugeordnet sind, werden sie in einer einzelnen Position in Dayforce konsolidiert.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-217">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="b3dc6-218">Weitere Informationen finden Sie in folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="b3dc6-218">For more information, see the following topics:</span></span>

- [<span data-ttu-id="b3dc6-219">Organisieren der Belegschaft anhand von Abteilungen, Stellen und Positionen</span><span class="sxs-lookup"><span data-stu-id="b3dc6-219">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="b3dc6-220">Positionen einrichten</span><span class="sxs-lookup"><span data-stu-id="b3dc6-220">Set up positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="b3dc6-221">Abteilungen</span><span class="sxs-lookup"><span data-stu-id="b3dc6-221">Departments</span></span>

<span data-ttu-id="b3dc6-222">Eine Abteilung ist eine Organisationseinheit, die eine Kategorie oder einen funktionalen Bereich einer Organisation darstellt.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-222">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="b3dc6-223">Eine Abteilung ist für einen bestimmten Bereich der Organisation wie zum Beispiel Verkauf, Buchhaltung oder Personalverwaltung zuständig.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-223">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="b3dc6-224">Sie können Abteilungen verwenden, um zu Funktionsbereiche zu melden.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-224">You can use departments to report on functional areas.</span></span> <span data-ttu-id="b3dc6-225">Abteilungen können Gewinn- und Verlustzuständigkeit haben.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-225">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="b3dc6-226">Weitere Informationen finden Sie in folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="b3dc6-226">For more information, see the following topics:</span></span>

- [<span data-ttu-id="b3dc6-227">Eine Abteilung erstellen und der Abteilungshierarchie zuordnen</span><span class="sxs-lookup"><span data-stu-id="b3dc6-227">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="b3dc6-228">Neue Abteilungen definieren</span><span class="sxs-lookup"><span data-stu-id="b3dc6-228">Define new departments</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="b3dc6-229">Lohnzyklen und Lohnperioden</span><span class="sxs-lookup"><span data-stu-id="b3dc6-229">Pay cycles and pay periods</span></span>

<span data-ttu-id="b3dc6-230">Ein Lohnzyklus bestimmt, wie oft Lohn ausgezahlt wird, sowie die spezifischen Tage, an denen Arbeitskräfte bezahlt werden.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-230">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="b3dc6-231">Ein Lohnzyklus kann beispielsweise monatlich sein, und Mitarbeiter werden am letzten Tag des Monats bezahlt.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-231">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="b3dc6-232">Alternativ könnte ein Lohnzyklus wöchentlich sein, und Mitarbeiter werden am Dienstag nach Ende der Lohnperiode bezahlt.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-232">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="b3dc6-233">Lohnzyklen werden Positionen zugewiesen, um zu steuern, wann Mitarbeiter in diesen Positionen bezahlt werden.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-233">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="b3dc6-234">Nachdem Sie Lohnzyklen erstellen, können Sie Lohnperioden für jeden Zyklus generieren.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-234">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="b3dc6-235">Jede Lohnperiode enthält ein Standardzahlungsdatum, das auf den von Ihnen bereitgestellten Informationen basiert.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-235">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="b3dc6-236">Allerdings können Sie das Standardzahlungsdatum in einer Lohnperiode ändern, um Ausnahmen zuzulassen, wie beispielsweise wenn das Zahlungsdatum auf einen Feiertag fällt.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-236">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="b3dc6-237">Die folgenden Informationen werden in Dayforce verwendet:</span><span class="sxs-lookup"><span data-stu-id="b3dc6-237">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="b3dc6-238">Lohnzyklus (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-238">Pay cycle (required)</span></span>
- <span data-ttu-id="b3dc6-239">Lohnzyklushäufigkeit (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-239">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="b3dc6-240">Periodenstartdatum (erstes erforderliche Lohnperiode)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-240">Period start date (first pay period required)</span></span>
- <span data-ttu-id="b3dc6-241">Standardzahlungsdatum (erste erforderliche Lohnperiode)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-241">Default payment date (first pay period required)</span></span>

<span data-ttu-id="b3dc6-242">Diese Informationen werden mit Dayforce als Lohngruppen integriert und sind nach Land oder Region für jeden Lohnzyklus getrennt.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-242">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="b3dc6-243">Es muss mindestens eine Lohnperiode vor der Integration generiert werden.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-243">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="b3dc6-244">Dayforce generiert Lohngruppenkalender und Zahlungsdaten basierend auf dem Anfangsdatum der ersten Lohnperiode und dem Standardzahlungsdatums, das in Talent eingerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-244">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Talent.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="b3dc6-245">Einkommenscodes</span><span class="sxs-lookup"><span data-stu-id="b3dc6-245">Earning codes</span></span>

<span data-ttu-id="b3dc6-246">Einkommenscodes bestimmen jeden Typ von Einkünften eindeutig, die Arbeitskräfte erhalten</span><span class="sxs-lookup"><span data-stu-id="b3dc6-246">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="b3dc6-247">Die Codes haben verschiedene Parameter, die sich auf Einkünfte beziehen, wie beispielsweise Buchhaltungsvorschriften, Steuergesetze, Berichterstellungsanforderungen und Bruttoausgleichsfähigkeit.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-247">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="b3dc6-248">Die folgenden Informationen werden in Dayforce verwendet:</span><span class="sxs-lookup"><span data-stu-id="b3dc6-248">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="b3dc6-249">Einkommenscode (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-249">Earning Code (required)</span></span>
- <span data-ttu-id="b3dc6-250">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b3dc6-250">Description</span></span>
- <span data-ttu-id="b3dc6-251">Maßeinheit</span><span class="sxs-lookup"><span data-stu-id="b3dc6-251">Unit of measure</span></span>
- <span data-ttu-id="b3dc6-252">Produktiv</span><span class="sxs-lookup"><span data-stu-id="b3dc6-252">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="b3dc6-253">Arbeitskraftdaten</span><span class="sxs-lookup"><span data-stu-id="b3dc6-253">Worker data</span></span>

<span data-ttu-id="b3dc6-254">Datensätze für die verschiedenen Arten von Arbeitskräften, die Sie haben, sind für Ihre Personalverwaltung- sowie für Ihre Lohnsysteme von Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-254">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="b3dc6-255">Anhand der eingegebenen Informationen lassen sich Arbeitskräfte sowie personenbezogene Informationen nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-255">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="b3dc6-256">Sie können die folgenden Informationen für Arbeitskräfte verwalten:</span><span class="sxs-lookup"><span data-stu-id="b3dc6-256">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="b3dc6-257">**Basis** – Verwalten grundlegender Informationen über eine Arbeitskraft, beispielsweise Kontaktinformationen, demografische Informationen, Kennungsinformationen, Familieninformationen, Militärdienststatus, Ausländerinformationen sowie personenbezogene und Notfallkontakte.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-257">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="b3dc6-258">**Beschäftigung** – Verwalten von Informationen zum Beschäftigungsverhältnis einer Arbeitskraft, wie Unternehmens- oder Organisationszugehörigkeit, Positionszuweisung, Start- und Enddatum, Arbeitsberechtigung, Beschäftigungsbedingungen, Rente, Urlaub und Versetzungen.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-258">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="b3dc6-259">**Urlaub und Abwesenheit** – Verwalten von Informationen zur Abwesenheit einer Arbeitskraft, beispielsweise Arbeitszeitkalender, Abwesenheitsbuchungen und Abwesenheitseinrichtung.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-259">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="b3dc6-260">**Vergütung und Lohn** – Verwalten von Informationen zu den Vergütungsplänen und Lohndaten einer Arbeitskraft, wie der Planregistrierung, Boni, Leistung, Provision, Steuerdaten, Pensionierung und Gehaltsabzüge.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-260">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="b3dc6-261">Wenn Sie Arbeitskraftinformationen eingeben, sollten Sie folgende Daten und Konfigurationen bedenken, die in Dayforce verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-261">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="b3dc6-262">Allgemeine Angaben</span><span class="sxs-lookup"><span data-stu-id="b3dc6-262">General information</span></span>

- <span data-ttu-id="b3dc6-263">Personalnummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-263">Personnel number (required)</span></span>
- <span data-ttu-id="b3dc6-264">Vorname (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-264">First name (required)</span></span>
- <span data-ttu-id="b3dc6-265">Nachname (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-265">Last name (required)</span></span>
- <span data-ttu-id="b3dc6-266">Zweiter Vorname</span><span class="sxs-lookup"><span data-stu-id="b3dc6-266">Middle name</span></span>
- <span data-ttu-id="b3dc6-267">Dienstalterdatum</span><span class="sxs-lookup"><span data-stu-id="b3dc6-267">Seniority date</span></span>
- <span data-ttu-id="b3dc6-268">Bekannt als</span><span class="sxs-lookup"><span data-stu-id="b3dc6-268">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="b3dc6-269">Personenbezogene Informationen</span><span class="sxs-lookup"><span data-stu-id="b3dc6-269">Personal information</span></span>

- <span data-ttu-id="b3dc6-270">Familienstand (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-270">Marital status (required)</span></span>
- <span data-ttu-id="b3dc6-271">Geburtsdatum (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-271">Birth date (required)</span></span>
- <span data-ttu-id="b3dc6-272">Geschlecht (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-272">Gender (required)</span></span>
- <span data-ttu-id="b3dc6-273">Person mit Behinderung</span><span class="sxs-lookup"><span data-stu-id="b3dc6-273">Person with disabilities</span></span>
- <span data-ttu-id="b3dc6-274">Nationalitätsland/-region (nur für Mexiko)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-274">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="b3dc6-275">Adressdaten</span><span class="sxs-lookup"><span data-stu-id="b3dc6-275">Address information</span></span>

- <span data-ttu-id="b3dc6-276">Primär (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-276">Primary (required)</span></span>
- <span data-ttu-id="b3dc6-277">Land/Region (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-277">Country/region (required)</span></span>
- <span data-ttu-id="b3dc6-278">Postleitzahl (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-278">Postal code (required)</span></span>
- <span data-ttu-id="b3dc6-279">Hausnummer (erforderlich) (nur für Mexiko)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-279">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="b3dc6-280">Gebäudeergänzung (nur für Mexiko)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-280">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="b3dc6-281">Ort (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-281">City (required)</span></span>
- <span data-ttu-id="b3dc6-282">Bundesland/Kanton (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-282">State (required)</span></span>
- <span data-ttu-id="b3dc6-283">Landkreis (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-283">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="b3dc6-284">Kontaktdaten</span><span class="sxs-lookup"><span data-stu-id="b3dc6-284">Contact information</span></span> 

- <span data-ttu-id="b3dc6-285">Primär (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-285">Primary (required)</span></span>
- <span data-ttu-id="b3dc6-286">Kontaktnummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-286">Contact number (required)</span></span>
- <span data-ttu-id="b3dc6-287">Durchwahl</span><span class="sxs-lookup"><span data-stu-id="b3dc6-287">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="b3dc6-288">Lohndaten und Einkommenscodes</span><span class="sxs-lookup"><span data-stu-id="b3dc6-288">Payroll information and earning codes</span></span>

<span data-ttu-id="b3dc6-289">Mitarbeitern müssen bestimmte Einkommen mit einer bestimmten Zahlungshäufigkeit zugewiesen werden und sie müssen eine bevorzugte Zahlungsmethode haben.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-289">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="b3dc6-290">Die folgenden Felder werden in Dayforce verwendet, um zu gewährleisten, dass diese Voreinstellungen und Einstellungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-290">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="b3dc6-291">Einkommenscodes</span><span class="sxs-lookup"><span data-stu-id="b3dc6-291">Earning codes</span></span>

- <span data-ttu-id="b3dc6-292">Position (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-292">Position (required)</span></span>
- <span data-ttu-id="b3dc6-293">Einkommenscode (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-293">Earning Code (required)</span></span>
- <span data-ttu-id="b3dc6-294">Häufigkeit (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-294">Frequency (required)</span></span>
- <span data-ttu-id="b3dc6-295">Betrag (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-295">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="b3dc6-296">Lohndaten</span><span class="sxs-lookup"><span data-stu-id="b3dc6-296">Payroll information</span></span>

- <span data-ttu-id="b3dc6-297">Zahlungsmethode</span><span class="sxs-lookup"><span data-stu-id="b3dc6-297">Payment Method</span></span>
- <span data-ttu-id="b3dc6-298">Wirtschaftliche Region (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-298">Economic Region (required)</span></span>
- <span data-ttu-id="b3dc6-299">Mitarbeitervergütungs-ID</span><span class="sxs-lookup"><span data-stu-id="b3dc6-299">Employee Benefits ID</span></span>
- <span data-ttu-id="b3dc6-300">Personalausweisnummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-300">National ID Number (required)</span></span>
- <span data-ttu-id="b3dc6-301">Militärdienstnummer</span><span class="sxs-lookup"><span data-stu-id="b3dc6-301">Military Service Number</span></span>
- <span data-ttu-id="b3dc6-302">Schichtkennung (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-302">Shift ID (required)</span></span>
- <span data-ttu-id="b3dc6-303">Steuernummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-303">Tax Number (required)</span></span>
- <span data-ttu-id="b3dc6-304">Gewerkschaftskennung (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-304">Union ID (required)</span></span>
- <span data-ttu-id="b3dc6-305">Arbeitstagkennung (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-305">Work Day ID (required)</span></span>
- <span data-ttu-id="b3dc6-306">Arbeitserlaubnisnummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-306">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="b3dc6-307">Für die Zahlungsmethode unterstützt Mexiko **Bargeld**, **Scheck** (der physische Scheck des Unternehmens) und **Elektronische Zahlung**.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-307">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="b3dc6-308">Wenn keine Zahlungsmethode angegeben wird, wird **Scheck** standardmäßig verwendet.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-308">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="b3dc6-309">Anstellungsdetails</span><span class="sxs-lookup"><span data-stu-id="b3dc6-309">Employment details</span></span>

<span data-ttu-id="b3dc6-310">Beschäftigungsdetailhistorie wird als Schlüsselinformation verwendet, um die Status für Einstellung, Kündigung und erneute Einstellung in Dayforce abzuleiten.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-310">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="b3dc6-311">Dayforce unterstützt nur einen aktiven Beschäftigungsdatensatz gleichzeitig.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-311">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="b3dc6-312">Datum des Beschäftigungsbeginns (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-312">Employment start date (required)</span></span>
- <span data-ttu-id="b3dc6-313">Datum des Beschäftigungsendes</span><span class="sxs-lookup"><span data-stu-id="b3dc6-313">Employment end date</span></span>
- <span data-ttu-id="b3dc6-314">Eintrittstermin</span><span class="sxs-lookup"><span data-stu-id="b3dc6-314">Start date</span></span>
- <span data-ttu-id="b3dc6-315">Angepasster Tätigkeitsbeginn</span><span class="sxs-lookup"><span data-stu-id="b3dc6-315">Adjusted start date</span></span>
- <span data-ttu-id="b3dc6-316">Kündigungsdatum (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-316">Termination date (required upon termination)</span></span>
- <span data-ttu-id="b3dc6-317">Kündigungsgrund (erforderlich bei Kündigung)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-317">Termination reason (required upon termination)</span></span>

<span data-ttu-id="b3dc6-318">Die Schlüsseldaten eines Mitarbeiters werden abgeleitet, indem die folgenden Informationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-318">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="b3dc6-319">Talent</span><span class="sxs-lookup"><span data-stu-id="b3dc6-319">Talent</span></span>                | <span data-ttu-id="b3dc6-320">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b3dc6-320">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3dc6-321">Aktuellstes Einstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="b3dc6-321">Most recent hire date</span></span> | <span data-ttu-id="b3dc6-322">Beschäftigungsbeginn des Verlaufsdatensatzes zur aktuellen, nicht gekündigten Beschäftigung</span><span class="sxs-lookup"><span data-stu-id="b3dc6-322">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="b3dc6-323">Kündigungsdatum</span><span class="sxs-lookup"><span data-stu-id="b3dc6-323">Termination date</span></span>      | <span data-ttu-id="b3dc6-324">Kündigungsdatum des Verlaufsdatensatzes zur aktuellen, nicht gekündigten Beschäftigung</span><span class="sxs-lookup"><span data-stu-id="b3dc6-324">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="b3dc6-325">Eintrittstermin</span><span class="sxs-lookup"><span data-stu-id="b3dc6-325">Start date</span></span>            | <span data-ttu-id="b3dc6-326">Angepasstes Startdatum, Startdatum oder Beschäftigungsbeginn des Verlaufsdatensatzes zur aktuellen, nicht aktiven Beschäftigung</span><span class="sxs-lookup"><span data-stu-id="b3dc6-326">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="b3dc6-327">Ursprüngliches Einstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="b3dc6-327">Original hire date</span></span>    | <span data-ttu-id="b3dc6-328">Beschäftigungsbeginn des frühesten Beschäftigungsverlaufsdatensatzes</span><span class="sxs-lookup"><span data-stu-id="b3dc6-328">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="b3dc6-329">Vergütung</span><span class="sxs-lookup"><span data-stu-id="b3dc6-329">Compensation</span></span>

<span data-ttu-id="b3dc6-330">Ein fester Vergütungsplan muss der primären Position jedes Mitarbeiters während einer Beschäftigungsperiode zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-330">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="b3dc6-331">Diese Periode beginnt mit dem Datum, an dem der Mitarbeiter eingestellt wurde (oder dem Datum des Beschäftigungsbeginns), und setzt sich bis zur Kündigung fort.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-331">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="b3dc6-332">Gültigkeitsdatum (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-332">Effective Date (required)</span></span>
- <span data-ttu-id="b3dc6-333">Ablaufdatum</span><span class="sxs-lookup"><span data-stu-id="b3dc6-333">Expiration date</span></span>
- <span data-ttu-id="b3dc6-334">Lohnsatz (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-334">Pay Rate (required)</span></span>
- <span data-ttu-id="b3dc6-335">Lohnsatzkonvertierungen (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-335">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="b3dc6-336">Jährliches Äquivalent (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-336">Annual equivalent (required)</span></span>
- <span data-ttu-id="b3dc6-337">Stündliches Äquivalent (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-337">Hourly equivalent (required)</span></span>

<span data-ttu-id="b3dc6-338">Wenn ein Mitarbeiter auf Stundenbasis mehrere Positionen hat, wird die feste Vergütung der primären Position in Dayforce als Basissatz/-gehalt auf Mitarbeiterebene importiert.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-338">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="b3dc6-339">Für nicht-primäre Positionen wird der Stundensatz in der entsprechenden Position in Dayforce gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-339">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="b3dc6-340">Wenn ein Gehalt beziehender Mitarbeiter mehrere Positionen hat, wird der kumulative Stundensatz und das Jahresgehalt über alle aktiven Positionen hinweg abgeleitet und als Basissatz/-gehalt auf Arbeitnehmerebene verwendet.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-340">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="b3dc6-341">Kennnummern</span><span class="sxs-lookup"><span data-stu-id="b3dc6-341">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="b3dc6-342">Sozialversicherungsbezeichner</span><span class="sxs-lookup"><span data-stu-id="b3dc6-342">Social Security identifier</span></span> 

<span data-ttu-id="b3dc6-343">Jeder Mitarbeiter muss einen primären Bezeichner haben.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-343">Every employee must have one primary identifier.</span></span> <span data-ttu-id="b3dc6-344">Dieser Bezeichner muss vom Kennungstyp **P.Reg.Nr.** sein.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-344">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="b3dc6-345">In Dayforce wird er automatisch als Sozialversicherungsbezeichner des Mitarbeiters abgeleitet, der für die Einstellung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-345">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="b3dc6-346">Primär (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-346">Primary (required)</span></span>
- <span data-ttu-id="b3dc6-347">Kennungstyp = „P.Reg.Nr.”</span><span class="sxs-lookup"><span data-stu-id="b3dc6-347">Identification Type = "SSN"</span></span>
- <span data-ttu-id="b3dc6-348">Ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="b3dc6-348">Issued Date</span></span>
- <span data-ttu-id="b3dc6-349">Ablaufdatum</span><span class="sxs-lookup"><span data-stu-id="b3dc6-349">Expiration Date</span></span>

<span data-ttu-id="b3dc6-350">Mitarbeiter können mehrere Kennungsnummern des Kennungstyps **P.Reg.Nr.** melden.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-350">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="b3dc6-351">Jedoch wird nur der Datensatz, der als **Primär** markiert ist, in Dayforce integriert, unabhängig davon, ob die Nummer aktiv oder abgelaufen ist.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-351">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="b3dc6-352">Bankkonten und Auszahlungen</span><span class="sxs-lookup"><span data-stu-id="b3dc6-352">Bank accounts and disbursements</span></span>

<span data-ttu-id="b3dc6-353">Gültige Bankkontoinformationen müssen für jeden Mitarbeiter eingegeben werden, der per Bankkontoüberweisungen bezahlt werden möchte.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-353">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="b3dc6-354">Talent</span><span class="sxs-lookup"><span data-stu-id="b3dc6-354">Talent</span></span>                         | <span data-ttu-id="b3dc6-355">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b3dc6-355">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3dc6-356">Bankkontonummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-356">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="b3dc6-357">SWIFT-Code (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-357">SWIFT code (required)</span></span>          | <span data-ttu-id="b3dc6-358">Feld **Bankkennung** wird verwendet, wenn Lohn in Mexiko verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-358">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="b3dc6-359">Filialnummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-359">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="b3dc6-360">Bankkontotyp (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-360">Bank account type (required)</span></span>   | <span data-ttu-id="b3dc6-361">Feld **Kontotyp** wird verwendet, wenn Lohn in Mexiko verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-361">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="b3dc6-362">Unterstützte Werte umfassen **Wird geprüft** und **Lohn**.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-362">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="b3dc6-363">Mitarbeiter, die per Bankkontoüberweisungen bezahlt werden möchten, müssen eine Verknüpfung zu einem Restbetrags-Bankkonto angeben, das sich unter einer juristischen Person befindet, deren primäre Adresse in Mexiko ist und das einem gültigen Bankkonto von einer mexikanischen Bank zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-363">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="b3dc6-364">Alle anderen Nicht-Restbetrags-Bankkonten werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-364">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="b3dc6-365">Adressdaten</span><span class="sxs-lookup"><span data-stu-id="b3dc6-365">Address information</span></span>

<span data-ttu-id="b3dc6-366">Jeder Mitarbeiter muss einen primären Standort haben.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-366">Every employee must have one primary location.</span></span> <span data-ttu-id="b3dc6-367">In Dayforce wird dieser Standort verwendet, um den primären Wohnsitz des Mitarbeiters für Steuerzwecke zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-367">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="b3dc6-368">Primär (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-368">Primary (required)</span></span>
- <span data-ttu-id="b3dc6-369">Land/Region (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-369">Country/region (required)</span></span>
- <span data-ttu-id="b3dc6-370">Postleitzahl (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-370">Zip/postal code (required)</span></span>
- <span data-ttu-id="b3dc6-371">Straße (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-371">Street (required)</span></span>
- <span data-ttu-id="b3dc6-372">Hausnummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-372">Street Number (required)</span></span>
- <span data-ttu-id="b3dc6-373">Gebäudeergänzung</span><span class="sxs-lookup"><span data-stu-id="b3dc6-373">Building Complement</span></span>
- <span data-ttu-id="b3dc6-374">Ort (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-374">City (required)</span></span>
- <span data-ttu-id="b3dc6-375">Bundesland/Kanton (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-375">State (required)</span></span>
- <span data-ttu-id="b3dc6-376">Landkreis (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-376">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="b3dc6-377">Konfigurieren Ihrer Daten, um Vergütung in den USA und Kanada zu generieren</span><span class="sxs-lookup"><span data-stu-id="b3dc6-377">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="b3dc6-378">Wenn Sie Vergütung für Mitarbeiter in den USA und Kanada generieren, müssen die folgenden Elemente konfiguriert werden:</span><span class="sxs-lookup"><span data-stu-id="b3dc6-378">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="b3dc6-379">Abteilungen sind für Positionen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-379">Departments are required on positions.</span></span>
- <span data-ttu-id="b3dc6-380">Kostenstellen müssen als Finanzdimensionen festgelegt werden und müssen das erste Element in der standardmäßigen Finanzdimensions-Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-380">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="b3dc6-381">Stellentypen</span><span class="sxs-lookup"><span data-stu-id="b3dc6-381">Job types</span></span>

<span data-ttu-id="b3dc6-382">Stellentypen werden verwendet, um ähnliche Stellen in Kategorien zu gruppieren.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-382">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="b3dc6-383">Stellentypen sind erforderlich, damit Lohn in den USA und Kanada zu bearbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-383">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="b3dc6-384">Beispiele für Stellentypen umfassen Voll- und Teilzeit oder festes Gehalt und Stundenlohn.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-384">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="b3dc6-385">Stellentypen werden Dayforce als Lohnarten zugeordnet, die angeben, ob ein Mitarbeiter auf Stundenbasis bezahlt wird oder ein festes Gehalt bezieht.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-385">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="b3dc6-386">Folgende Stellentypen und Beschreibungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-386">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="b3dc6-387">Stellentyp</span><span class="sxs-lookup"><span data-stu-id="b3dc6-387">Job type</span></span>   | <span data-ttu-id="b3dc6-388">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b3dc6-388">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="b3dc6-389">Stündlich</span><span class="sxs-lookup"><span data-stu-id="b3dc6-389">Hourly</span></span>     | <span data-ttu-id="b3dc6-390">Stündlich</span><span class="sxs-lookup"><span data-stu-id="b3dc6-390">Hourly</span></span>      |
| <span data-ttu-id="b3dc6-391">Fest angestellt</span><span class="sxs-lookup"><span data-stu-id="b3dc6-391">Salaried</span></span>   | <span data-ttu-id="b3dc6-392">Fest angestellt</span><span class="sxs-lookup"><span data-stu-id="b3dc6-392">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="b3dc6-393">Positionstypen</span><span class="sxs-lookup"><span data-stu-id="b3dc6-393">Position types</span></span> 

<span data-ttu-id="b3dc6-394">Sie verwenden Positionstypen, um zu beschreiben, ob die Position Vollzeit, Teilzeit oder etwas anderes ist.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-394">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="b3dc6-395">Positionstypen werden Dayforce als Lohnklassen zugeordnet, die angeben, ob ein Mitarbeiter in Vollzeit oder Teilzeit arbeitet.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-395">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="b3dc6-396">Folgende Positionstypen und Beschreibungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-396">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="b3dc6-397">Positionstyp</span><span class="sxs-lookup"><span data-stu-id="b3dc6-397">Position type</span></span>   | <span data-ttu-id="b3dc6-398">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b3dc6-398">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="b3dc6-399">Vollzeit</span><span class="sxs-lookup"><span data-stu-id="b3dc6-399">Full-time</span></span>       | <span data-ttu-id="b3dc6-400">Vollzeitmitarbeiter</span><span class="sxs-lookup"><span data-stu-id="b3dc6-400">Full time employee</span></span> |
| <span data-ttu-id="b3dc6-401">Teilzeit</span><span class="sxs-lookup"><span data-stu-id="b3dc6-401">Part-time</span></span>       | <span data-ttu-id="b3dc6-402">Teilzeitmitarbeiter</span><span class="sxs-lookup"><span data-stu-id="b3dc6-402">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="b3dc6-403">Ursachencodes</span><span class="sxs-lookup"><span data-stu-id="b3dc6-403">Reason codes</span></span>

<span data-ttu-id="b3dc6-404">Ursachencodes enthalten Informationen zum Status eines Mitarbeiters.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-404">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="b3dc6-405">Ursachencodes werden Dayforce als Statusgründe zugeordnet, die den Grund für Änderungen bei der Position eines Mitarbeiters oder dem Beschäftigungsstatus angeben.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-405">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="b3dc6-406">Folgende Ursachencodes und Beschreibungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-406">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="b3dc6-407">Ursachencode</span><span class="sxs-lookup"><span data-stu-id="b3dc6-407">Reason code</span></span>    | <span data-ttu-id="b3dc6-408">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b3dc6-408">Description</span></span>      | <span data-ttu-id="b3dc6-409">Zutreffende Szenarios</span><span class="sxs-lookup"><span data-stu-id="b3dc6-409">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="b3dc6-410">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="b3dc6-410">RESIGNATION</span></span>    | <span data-ttu-id="b3dc6-411">Kündigung durch Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="b3dc6-411">Resignation</span></span>      | <span data-ttu-id="b3dc6-412">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="b3dc6-412">Terminate worker</span></span>     |
| <span data-ttu-id="b3dc6-413">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="b3dc6-413">TERMINATION</span></span>    | <span data-ttu-id="b3dc6-414">Beendigung</span><span class="sxs-lookup"><span data-stu-id="b3dc6-414">Termination</span></span>      | <span data-ttu-id="b3dc6-415">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="b3dc6-415">Terminate worker</span></span>     |
| <span data-ttu-id="b3dc6-416">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="b3dc6-416">RETIREMENT</span></span>     | <span data-ttu-id="b3dc6-417">Ruhestand</span><span class="sxs-lookup"><span data-stu-id="b3dc6-417">Retirement</span></span>       | <span data-ttu-id="b3dc6-418">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="b3dc6-418">Terminate worker</span></span>     |
| <span data-ttu-id="b3dc6-419">OTHER</span><span class="sxs-lookup"><span data-stu-id="b3dc6-419">OTHER</span></span>          | <span data-ttu-id="b3dc6-420">Andere Gründe</span><span class="sxs-lookup"><span data-stu-id="b3dc6-420">Other Reasons</span></span>    | <span data-ttu-id="b3dc6-421">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="b3dc6-421">Terminate worker</span></span>     |
| <span data-ttu-id="b3dc6-422">DEATH</span><span class="sxs-lookup"><span data-stu-id="b3dc6-422">DEATH</span></span>          | <span data-ttu-id="b3dc6-423">Tod</span><span class="sxs-lookup"><span data-stu-id="b3dc6-423">Death</span></span>            | <span data-ttu-id="b3dc6-424">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="b3dc6-424">Terminate worker</span></span>     |
| <span data-ttu-id="b3dc6-425">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="b3dc6-425">LEAVEOFABSENCE</span></span> | <span data-ttu-id="b3dc6-426">Beurlaubung</span><span class="sxs-lookup"><span data-stu-id="b3dc6-426">Leave of Absence</span></span> | <span data-ttu-id="b3dc6-427">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="b3dc6-427">Terminate worker</span></span>     |
| <span data-ttu-id="b3dc6-428">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="b3dc6-428">CONTRACTEND</span></span>    | <span data-ttu-id="b3dc6-429">Vertragsende</span><span class="sxs-lookup"><span data-stu-id="b3dc6-429">End of Contract</span></span>  | <span data-ttu-id="b3dc6-430">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="b3dc6-430">Terminate worker</span></span>     |
| <span data-ttu-id="b3dc6-431">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="b3dc6-431">SALARYCHANGE</span></span>   | <span data-ttu-id="b3dc6-432">Gehaltsänderung</span><span class="sxs-lookup"><span data-stu-id="b3dc6-432">Change of Salary</span></span> | <span data-ttu-id="b3dc6-433">Vergütung</span><span class="sxs-lookup"><span data-stu-id="b3dc6-433">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="b3dc6-434">Familienstand</span><span class="sxs-lookup"><span data-stu-id="b3dc6-434">Marital status</span></span>

<span data-ttu-id="b3dc6-435">Familienstandwerte werden Dayforce zugeordnet und werden – je nach Bedarf – in die akzeptierten Werte bei der Integration übersetzt.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-435">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="b3dc6-436">Die folgende Tabelle zeigt, wie Familienstandwerte Dayforce zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-436">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="b3dc6-437">Talent</span><span class="sxs-lookup"><span data-stu-id="b3dc6-437">Talent</span></span>                 | <span data-ttu-id="b3dc6-438">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b3dc6-438">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="b3dc6-439">Verheiratet</span><span class="sxs-lookup"><span data-stu-id="b3dc6-439">Married</span></span>                | <span data-ttu-id="b3dc6-440">Verheiratet</span><span class="sxs-lookup"><span data-stu-id="b3dc6-440">Married</span></span>              |
| <span data-ttu-id="b3dc6-441">Ledig</span><span class="sxs-lookup"><span data-stu-id="b3dc6-441">Single</span></span>                 | <span data-ttu-id="b3dc6-442">Ledig</span><span class="sxs-lookup"><span data-stu-id="b3dc6-442">Single</span></span>               |
| <span data-ttu-id="b3dc6-443">Verwitwet</span><span class="sxs-lookup"><span data-stu-id="b3dc6-443">Widowed</span></span>                | <span data-ttu-id="b3dc6-444">Verwitwet</span><span class="sxs-lookup"><span data-stu-id="b3dc6-444">Widowed</span></span>              |
| <span data-ttu-id="b3dc6-445">Geschieden</span><span class="sxs-lookup"><span data-stu-id="b3dc6-445">Divorced</span></span>               | <span data-ttu-id="b3dc6-446">Geschieden</span><span class="sxs-lookup"><span data-stu-id="b3dc6-446">Divorced</span></span>             |
| <span data-ttu-id="b3dc6-447">Eingetragene Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="b3dc6-447">Registered Partnership</span></span> | <span data-ttu-id="b3dc6-448">Inländische Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="b3dc6-448">Domestic Partnership</span></span> |
| <span data-ttu-id="b3dc6-449">None</span><span class="sxs-lookup"><span data-stu-id="b3dc6-449">None</span></span>                   | <span data-ttu-id="b3dc6-450">None</span><span class="sxs-lookup"><span data-stu-id="b3dc6-450">None</span></span>                 |
| <span data-ttu-id="b3dc6-451">Freie Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="b3dc6-451">Cohabiting</span></span>             | <span data-ttu-id="b3dc6-452">Freie Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="b3dc6-452">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="b3dc6-453">Geschlecht</span><span class="sxs-lookup"><span data-stu-id="b3dc6-453">Gender</span></span>

<span data-ttu-id="b3dc6-454">Geschlechtsbezeichnungen werden Dayforce zugeordnet und werden – je nach Bedarf – in die akzeptierten Werte bei der Integration übersetzt.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-454">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="b3dc6-455">Die folgende Tabelle zeigt, wie Geschlechtsbezeichnungen Dayforce zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-455">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="b3dc6-456">Talent</span><span class="sxs-lookup"><span data-stu-id="b3dc6-456">Talent</span></span>       | <span data-ttu-id="b3dc6-457">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b3dc6-457">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="b3dc6-458">Männlich</span><span class="sxs-lookup"><span data-stu-id="b3dc6-458">Male</span></span>         | <span data-ttu-id="b3dc6-459">Männlich</span><span class="sxs-lookup"><span data-stu-id="b3dc6-459">Male</span></span>            |
| <span data-ttu-id="b3dc6-460">Weiblich</span><span class="sxs-lookup"><span data-stu-id="b3dc6-460">Female</span></span>       | <span data-ttu-id="b3dc6-461">Weiblich</span><span class="sxs-lookup"><span data-stu-id="b3dc6-461">Female</span></span>          |
| <span data-ttu-id="b3dc6-462">Nicht spezifisch</span><span class="sxs-lookup"><span data-stu-id="b3dc6-462">Non-specific</span></span> | <span data-ttu-id="b3dc6-463">*Nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="b3dc6-463">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="b3dc6-464">Einkommenscodes</span><span class="sxs-lookup"><span data-stu-id="b3dc6-464">Earning codes</span></span>

<span data-ttu-id="b3dc6-465">Einkommenscodes bestimmen jeden Typ von Einkünften eindeutig, die Arbeitskräfte erhalten</span><span class="sxs-lookup"><span data-stu-id="b3dc6-465">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="b3dc6-466">Die Codes decken verschiedene Parameter ab, die sich auf Einkünfte beziehen, wie beispielsweise Buchhaltungsvorschriften, Steuergesetze, Berichterstellungsanforderungen und Bruttoausgleichsfähigkeit.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-466">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="b3dc6-467">Wenn eine nicht unterstützte Häufigkeit verwendet wird, wird die Häufigkeit **Jeder Lohn** standardmäßig für die Berechnung verwendet.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-467">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="b3dc6-468">Unterstützte Häufigkeiten</span><span class="sxs-lookup"><span data-stu-id="b3dc6-468">Supported frequencies</span></span>

- <span data-ttu-id="b3dc6-469">Alle</span><span class="sxs-lookup"><span data-stu-id="b3dc6-469">All</span></span>
- <span data-ttu-id="b3dc6-470">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="b3dc6-470">EVERYPAY</span></span>
- <span data-ttu-id="b3dc6-471">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="b3dc6-471">EACHPAYPERIOD</span></span>
- <span data-ttu-id="b3dc6-472">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="b3dc6-472">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="b3dc6-473">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="b3dc6-473">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="b3dc6-474">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3dc6-474">1OFMTH</span></span>
- <span data-ttu-id="b3dc6-475">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="b3dc6-475">LASTOFMTH</span></span>
- <span data-ttu-id="b3dc6-476">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3dc6-476">2OFMTH</span></span>
- <span data-ttu-id="b3dc6-477">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3dc6-477">3OFMTH</span></span>
- <span data-ttu-id="b3dc6-478">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3dc6-478">4OFMTH</span></span>
- <span data-ttu-id="b3dc6-479">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3dc6-479">5OFMTH</span></span>
- <span data-ttu-id="b3dc6-480">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3dc6-480">1N2OFMTH</span></span>
- <span data-ttu-id="b3dc6-481">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3dc6-481">3N4OFMTH</span></span>
- <span data-ttu-id="b3dc6-482">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3dc6-482">1N3OFMTH</span></span>
- <span data-ttu-id="b3dc6-483">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3dc6-483">1N4OFMTH</span></span>
- <span data-ttu-id="b3dc6-484">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3dc6-484">2N3OFMTH</span></span>
- <span data-ttu-id="b3dc6-485">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3dc6-485">2N4OFMTH</span></span>
- <span data-ttu-id="b3dc6-486">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3dc6-486">1N2N3OFMTH</span></span>
- <span data-ttu-id="b3dc6-487">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3dc6-487">1N2N4OFMTH</span></span>
- <span data-ttu-id="b3dc6-488">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3dc6-488">1N3N4OFMTH</span></span>
- <span data-ttu-id="b3dc6-489">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3dc6-489">2N3N4OFMTH</span></span>
- <span data-ttu-id="b3dc6-490">1N2N3N4OFMTH – 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3dc6-490">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="b3dc6-491">2N3N4N5OFMth – 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="b3dc6-491">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="b3dc6-492">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="b3dc6-492">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="b3dc6-493">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="b3dc6-493">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="b3dc6-494">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="b3dc6-494">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="b3dc6-495">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="b3dc6-495">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="b3dc6-496">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="b3dc6-496">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="b3dc6-497">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="b3dc6-497">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="b3dc6-498">Adressen</span><span class="sxs-lookup"><span data-stu-id="b3dc6-498">Addresses</span></span>

<span data-ttu-id="b3dc6-499">Die Kennung bestimmter Codes für Land oder Region, Bundesland/Kanton oder Landkreis (Gemeinde) erfordert spezifische Formate, die Dayforce und Anbieter innerhalb des Landes/innerhalb der Region erkennen können.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-499">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="b3dc6-500">Obwohl das Format für Orte flexibel ist, muss jeder Ort einem Bundesland zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-500">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="b3dc6-501">Talent</span><span class="sxs-lookup"><span data-stu-id="b3dc6-501">Talent</span></span>          | <span data-ttu-id="b3dc6-502">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b3dc6-502">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="b3dc6-503">Land/Region</span><span class="sxs-lookup"><span data-stu-id="b3dc6-503">Country/Region</span></span>  | <span data-ttu-id="b3dc6-504">Ländercode</span><span class="sxs-lookup"><span data-stu-id="b3dc6-504">Country Code</span></span>          |
| <span data-ttu-id="b3dc6-505">Postleitzahl</span><span class="sxs-lookup"><span data-stu-id="b3dc6-505">Zip/Postal Code</span></span> | <span data-ttu-id="b3dc6-506">PLZ</span><span class="sxs-lookup"><span data-stu-id="b3dc6-506">Postal Code</span></span>           |
| <span data-ttu-id="b3dc6-507">Zustand</span><span class="sxs-lookup"><span data-stu-id="b3dc6-507">State</span></span>           | <span data-ttu-id="b3dc6-508">Bundeslandcode</span><span class="sxs-lookup"><span data-stu-id="b3dc6-508">State Code</span></span>            |
| <span data-ttu-id="b3dc6-509">Stadt</span><span class="sxs-lookup"><span data-stu-id="b3dc6-509">City</span></span>            | <span data-ttu-id="b3dc6-510">Stadt</span><span class="sxs-lookup"><span data-stu-id="b3dc6-510">City</span></span>                  |
| <span data-ttu-id="b3dc6-511">Verwaltungsbezirk</span><span class="sxs-lookup"><span data-stu-id="b3dc6-511">County</span></span>          | <span data-ttu-id="b3dc6-512">Landkreis (Gemeinde)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-512">County (Municipality)</span></span> |
| <span data-ttu-id="b3dc6-513">Straße</span><span class="sxs-lookup"><span data-stu-id="b3dc6-513">Street</span></span>          | <span data-ttu-id="b3dc6-514">Adresszeile 1</span><span class="sxs-lookup"><span data-stu-id="b3dc6-514">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="b3dc6-515">Steuerregionen</span><span class="sxs-lookup"><span data-stu-id="b3dc6-515">Tax regions</span></span>

<span data-ttu-id="b3dc6-516">Steuerregionen werden verwendet, um die entsprechende Steuer festzulegen, die bei der Lohngenerierung angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-516">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="b3dc6-517">Steuerregionen werden Dayforce als Standortadressen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-517">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="b3dc6-518">Die Standardsteuerregion muss der aktiven Position der Arbeitskraft zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-518">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="b3dc6-519">Steuerregion (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-519">Tax region (required)</span></span>
- <span data-ttu-id="b3dc6-520">Land/Region (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-520">Country/Region (required)</span></span>
- <span data-ttu-id="b3dc6-521">Bundesland/Kanton (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-521">State (required)</span></span>
- <span data-ttu-id="b3dc6-522">Verwaltungsbezirk</span><span class="sxs-lookup"><span data-stu-id="b3dc6-522">County</span></span> 
- <span data-ttu-id="b3dc6-523">Ort (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-523">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="b3dc6-524">Konfigurieren Ihrer Daten, um Lohn in Mexiko zu generieren</span><span class="sxs-lookup"><span data-stu-id="b3dc6-524">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="b3dc6-525">Wenn Sie Vergütung für Mitarbeiter in Mexiko generieren, müssen die folgenden Elemente konfiguriert werden:</span><span class="sxs-lookup"><span data-stu-id="b3dc6-525">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="b3dc6-526">Abteilungen sind für Positionen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-526">Departments are required on positions.</span></span>
- <span data-ttu-id="b3dc6-527">Kostenstellen müssen als Finanzdimensionen festgelegt werden und müssen das erste Element in der standardmäßigen Finanzdimensions-Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-527">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="b3dc6-528">Stellentypen</span><span class="sxs-lookup"><span data-stu-id="b3dc6-528">Job types</span></span>

<span data-ttu-id="b3dc6-529">Stellentypen werden verwendet, um ähnliche Stellen in Kategorien zu gruppieren.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-529">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="b3dc6-530">Stellentypen sind erforderlich, um Lohn in Mexiko zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-530">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="b3dc6-531">Beispiele für Stellentypen umfassen Voll- und Teilzeit oder festes Gehalt und Stundenlohn.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-531">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="b3dc6-532">Stellentypen werden Dayforce als Lohnarten zugeordnet, die angeben, ob ein Mitarbeiter auf Stundenbasis bezahlt wird oder ein festes Gehalt bezieht.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-532">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="b3dc6-533">Folgende Stellentypen und Beschreibungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-533">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="b3dc6-534">Stellentyp</span><span class="sxs-lookup"><span data-stu-id="b3dc6-534">Job type</span></span>   | <span data-ttu-id="b3dc6-535">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b3dc6-535">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="b3dc6-536">Stündlich</span><span class="sxs-lookup"><span data-stu-id="b3dc6-536">Hourly</span></span>     | <span data-ttu-id="b3dc6-537">MX – Stundenbasis</span><span class="sxs-lookup"><span data-stu-id="b3dc6-537">MX Hourly</span></span>   |
| <span data-ttu-id="b3dc6-538">Fest angestellt</span><span class="sxs-lookup"><span data-stu-id="b3dc6-538">Salaried</span></span>   | <span data-ttu-id="b3dc6-539">MX – Fest angestellt</span><span class="sxs-lookup"><span data-stu-id="b3dc6-539">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="b3dc6-540">Positionstypen</span><span class="sxs-lookup"><span data-stu-id="b3dc6-540">Position types</span></span> 

<span data-ttu-id="b3dc6-541">Sie verwenden Positionstypen, um zu beschreiben, ob die Position Vollzeit, Teilzeit oder etwas anderes ist.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-541">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="b3dc6-542">Positionstypen werden Dayforce als Lohnklassen zugeordnet, die angeben, ob ein Mitarbeiter in Vollzeit oder Teilzeit arbeitet.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-542">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="b3dc6-543">Folgende Positionstypen und Beschreibungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-543">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="b3dc6-544">Positionstyp</span><span class="sxs-lookup"><span data-stu-id="b3dc6-544">Position type</span></span>   | <span data-ttu-id="b3dc6-545">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b3dc6-545">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="b3dc6-546">Vollzeit</span><span class="sxs-lookup"><span data-stu-id="b3dc6-546">Full-time</span></span>       | <span data-ttu-id="b3dc6-547">Vollzeitmitarbeiter</span><span class="sxs-lookup"><span data-stu-id="b3dc6-547">Full time employee</span></span> |
| <span data-ttu-id="b3dc6-548">Teilzeit</span><span class="sxs-lookup"><span data-stu-id="b3dc6-548">Part-time</span></span>       | <span data-ttu-id="b3dc6-549">Teilzeitmitarbeiter</span><span class="sxs-lookup"><span data-stu-id="b3dc6-549">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="b3dc6-550">Ursachencodes</span><span class="sxs-lookup"><span data-stu-id="b3dc6-550">Reason codes</span></span>

<span data-ttu-id="b3dc6-551">Ursachencodes enthalten Informationen zum Status eines Mitarbeiters.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-551">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="b3dc6-552">Ursachencodes werden Dayforce als Statusgründe zugeordnet, die den Grund für Änderungen bei der Position eines Mitarbeiters oder dem Beschäftigungsstatus angeben.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-552">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="b3dc6-553">Folgende Ursachencodes und Beschreibungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-553">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="b3dc6-554">Ursachencode</span><span class="sxs-lookup"><span data-stu-id="b3dc6-554">Reason code</span></span>            | <span data-ttu-id="b3dc6-555">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b3dc6-555">Description</span></span>                    | <span data-ttu-id="b3dc6-556">Zutreffende Szenarios</span><span class="sxs-lookup"><span data-stu-id="b3dc6-556">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="b3dc6-557">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="b3dc6-557">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="b3dc6-558">Abgang vor erster Lohnzahlung</span><span class="sxs-lookup"><span data-stu-id="b3dc6-558">Departure before first payroll</span></span> | <span data-ttu-id="b3dc6-559">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="b3dc6-559">Terminate worker</span></span>     |
| <span data-ttu-id="b3dc6-560">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="b3dc6-560">RESIGNATION</span></span>            | <span data-ttu-id="b3dc6-561">Kündigung durch Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="b3dc6-561">Resignation</span></span>                    | <span data-ttu-id="b3dc6-562">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="b3dc6-562">Terminate worker</span></span>     |
| <span data-ttu-id="b3dc6-563">PENSION</span><span class="sxs-lookup"><span data-stu-id="b3dc6-563">PENSION</span></span>                | <span data-ttu-id="b3dc6-564">Rente</span><span class="sxs-lookup"><span data-stu-id="b3dc6-564">Pension</span></span>                        | <span data-ttu-id="b3dc6-565">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="b3dc6-565">Terminate worker</span></span>     |
| <span data-ttu-id="b3dc6-566">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="b3dc6-566">TERMINATION</span></span>            | <span data-ttu-id="b3dc6-567">Beendigung</span><span class="sxs-lookup"><span data-stu-id="b3dc6-567">Termination</span></span>                    | <span data-ttu-id="b3dc6-568">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="b3dc6-568">Terminate worker</span></span>     |
| <span data-ttu-id="b3dc6-569">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="b3dc6-569">RETIREMENT</span></span>             | <span data-ttu-id="b3dc6-570">Ruhestand</span><span class="sxs-lookup"><span data-stu-id="b3dc6-570">Retirement</span></span>                     | <span data-ttu-id="b3dc6-571">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="b3dc6-571">Terminate worker</span></span>     |
| <span data-ttu-id="b3dc6-572">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="b3dc6-572">ABSENTEE</span></span>               | <span data-ttu-id="b3dc6-573">Abwesende Person</span><span class="sxs-lookup"><span data-stu-id="b3dc6-573">Absentee</span></span>                       | <span data-ttu-id="b3dc6-574">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="b3dc6-574">Terminate worker</span></span>     |
| <span data-ttu-id="b3dc6-575">OTHER</span><span class="sxs-lookup"><span data-stu-id="b3dc6-575">OTHER</span></span>                  | <span data-ttu-id="b3dc6-576">Andere Gründe</span><span class="sxs-lookup"><span data-stu-id="b3dc6-576">Other Reasons</span></span>                  | <span data-ttu-id="b3dc6-577">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="b3dc6-577">Terminate worker</span></span>     |
| <span data-ttu-id="b3dc6-578">CLOSURE</span><span class="sxs-lookup"><span data-stu-id="b3dc6-578">CLOSURE</span></span>                | <span data-ttu-id="b3dc6-579">Betriebsferien</span><span class="sxs-lookup"><span data-stu-id="b3dc6-579">Business Closure</span></span>               | <span data-ttu-id="b3dc6-580">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="b3dc6-580">Terminate worker</span></span>     |
| <span data-ttu-id="b3dc6-581">DEATH</span><span class="sxs-lookup"><span data-stu-id="b3dc6-581">DEATH</span></span>                  | <span data-ttu-id="b3dc6-582">Tod</span><span class="sxs-lookup"><span data-stu-id="b3dc6-582">Death</span></span>                          | <span data-ttu-id="b3dc6-583">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="b3dc6-583">Terminate worker</span></span>     |
| <span data-ttu-id="b3dc6-584">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="b3dc6-584">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="b3dc6-585">Beurlaubung</span><span class="sxs-lookup"><span data-stu-id="b3dc6-585">Leave of Absence</span></span>               | <span data-ttu-id="b3dc6-586">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="b3dc6-586">Terminate worker</span></span>     |
| <span data-ttu-id="b3dc6-587">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="b3dc6-587">CONTRACTEND</span></span>            | <span data-ttu-id="b3dc6-588">Vertragsende</span><span class="sxs-lookup"><span data-stu-id="b3dc6-588">End of Contract</span></span>                | <span data-ttu-id="b3dc6-589">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="b3dc6-589">Terminate worker</span></span>     |
| <span data-ttu-id="b3dc6-590">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="b3dc6-590">SALARYCHANGE</span></span>           | <span data-ttu-id="b3dc6-591">Gehaltsänderung</span><span class="sxs-lookup"><span data-stu-id="b3dc6-591">Change of Salary</span></span>               | <span data-ttu-id="b3dc6-592">Vergütung</span><span class="sxs-lookup"><span data-stu-id="b3dc6-592">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="b3dc6-593">Einstellungsbedingungen</span><span class="sxs-lookup"><span data-stu-id="b3dc6-593">Terms of employment</span></span>

<span data-ttu-id="b3dc6-594">Beschäftigungsbedingungen werden verwendet, um Kategorien von Beschäftigungsbedingungen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-594">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="b3dc6-595">Die Bedingungen werden Dayforce als Beschäftigungsindikatorwerte zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-595">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="b3dc6-596">Die folgenden Bedingungen für Beschäftigung und Beschreibungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-596">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="b3dc6-597">Einstellungsbedingungen</span><span class="sxs-lookup"><span data-stu-id="b3dc6-597">Terms of employment</span></span>   | <span data-ttu-id="b3dc6-598">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b3dc6-598">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="b3dc6-599">Regelmäßig</span><span class="sxs-lookup"><span data-stu-id="b3dc6-599">Regular</span></span>               | <span data-ttu-id="b3dc6-600">Regelmäßig</span><span class="sxs-lookup"><span data-stu-id="b3dc6-600">Regular</span></span>     |
| <span data-ttu-id="b3dc6-601">Direkt</span><span class="sxs-lookup"><span data-stu-id="b3dc6-601">Direct</span></span>                | <span data-ttu-id="b3dc6-602">Direkt</span><span class="sxs-lookup"><span data-stu-id="b3dc6-602">Direct</span></span>      |
| <span data-ttu-id="b3dc6-603">Praktikum</span><span class="sxs-lookup"><span data-stu-id="b3dc6-603">Internship</span></span>            | <span data-ttu-id="b3dc6-604">Praktikum</span><span class="sxs-lookup"><span data-stu-id="b3dc6-604">Internship</span></span>  |
| <span data-ttu-id="b3dc6-605">Unbefristet</span><span class="sxs-lookup"><span data-stu-id="b3dc6-605">Permanent</span></span>             | <span data-ttu-id="b3dc6-606">Unbefristet</span><span class="sxs-lookup"><span data-stu-id="b3dc6-606">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="b3dc6-607">Familienstand</span><span class="sxs-lookup"><span data-stu-id="b3dc6-607">Marital status</span></span>

<span data-ttu-id="b3dc6-608">Familienstandwerte werden Dayforce zugeordnet und werden – je nach Bedarf – in die akzeptierten Werte bei der Integration übersetzt.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-608">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="b3dc6-609">Die folgende Tabelle zeigt, wie Familienstandwerte Dayforce zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-609">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="b3dc6-610">Talent</span><span class="sxs-lookup"><span data-stu-id="b3dc6-610">Talent</span></span>                 | <span data-ttu-id="b3dc6-611">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b3dc6-611">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="b3dc6-612">Verheiratet</span><span class="sxs-lookup"><span data-stu-id="b3dc6-612">Married</span></span>                | <span data-ttu-id="b3dc6-613">Verheiratet</span><span class="sxs-lookup"><span data-stu-id="b3dc6-613">Married</span></span>                   |
| <span data-ttu-id="b3dc6-614">Ledig</span><span class="sxs-lookup"><span data-stu-id="b3dc6-614">Single</span></span>                 | <span data-ttu-id="b3dc6-615">Ledig</span><span class="sxs-lookup"><span data-stu-id="b3dc6-615">Single</span></span>                    |
| <span data-ttu-id="b3dc6-616">Verwitwet</span><span class="sxs-lookup"><span data-stu-id="b3dc6-616">Widowed</span></span>                | <span data-ttu-id="b3dc6-617">Verwitwet</span><span class="sxs-lookup"><span data-stu-id="b3dc6-617">Widowed</span></span>                   |
| <span data-ttu-id="b3dc6-618">Geschieden</span><span class="sxs-lookup"><span data-stu-id="b3dc6-618">Divorced</span></span>               | <span data-ttu-id="b3dc6-619">Geschieden</span><span class="sxs-lookup"><span data-stu-id="b3dc6-619">Divorced</span></span>                  |
| <span data-ttu-id="b3dc6-620">Eingetragene Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="b3dc6-620">Registered Partnership</span></span> | <span data-ttu-id="b3dc6-621">Inländische Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="b3dc6-621">Domestic Partnership</span></span>      |
| <span data-ttu-id="b3dc6-622">None</span><span class="sxs-lookup"><span data-stu-id="b3dc6-622">None</span></span>                   | <span data-ttu-id="b3dc6-623">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="b3dc6-623">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="b3dc6-624">Freie Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="b3dc6-624">Cohabiting</span></span>             | <span data-ttu-id="b3dc6-625">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="b3dc6-625">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="b3dc6-626">Geschlecht</span><span class="sxs-lookup"><span data-stu-id="b3dc6-626">Gender</span></span>

<span data-ttu-id="b3dc6-627">Geschlechtsbezeichnungen werden Dayforce zugeordnet und werden – je nach Bedarf – in die akzeptierten Werte bei der Integration übersetzt.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-627">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="b3dc6-628">Die folgende Tabelle zeigt, wie Geschlechtsbezeichnungen Dayforce zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-628">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="b3dc6-629">Talent</span><span class="sxs-lookup"><span data-stu-id="b3dc6-629">Talent</span></span>       | <span data-ttu-id="b3dc6-630">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b3dc6-630">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="b3dc6-631">Männlich</span><span class="sxs-lookup"><span data-stu-id="b3dc6-631">Male</span></span>         | <span data-ttu-id="b3dc6-632">Männlich</span><span class="sxs-lookup"><span data-stu-id="b3dc6-632">Male</span></span>                      |
| <span data-ttu-id="b3dc6-633">Weiblich</span><span class="sxs-lookup"><span data-stu-id="b3dc6-633">Female</span></span>       | <span data-ttu-id="b3dc6-634">Weiblich</span><span class="sxs-lookup"><span data-stu-id="b3dc6-634">Female</span></span>                    |
| <span data-ttu-id="b3dc6-635">Nicht spezifisch</span><span class="sxs-lookup"><span data-stu-id="b3dc6-635">Non-specific</span></span> | <span data-ttu-id="b3dc6-636">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="b3dc6-636">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="b3dc6-637">Zahlungsweise</span><span class="sxs-lookup"><span data-stu-id="b3dc6-637">Payment method</span></span>

<span data-ttu-id="b3dc6-638">Zahlungsmethoden geben dem Mitarbeiter und dem Unternehmen die Möglichkeit zu beschreiben, wie Mitarbeiter bezahlt werden.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-638">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="b3dc6-639">Zahlungsmethoden werden Dayforce zugeordnet und werden – je nach Bedarf – in die akzeptierten Werte bei der Integration übersetzt.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-639">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="b3dc6-640">Die folgende Tabelle zeigt, wie Zahlungsmethoden Dayforce zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-640">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="b3dc6-641">Talent</span><span class="sxs-lookup"><span data-stu-id="b3dc6-641">Talent</span></span>             | <span data-ttu-id="b3dc6-642">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b3dc6-642">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="b3dc6-643">Bargeld</span><span class="sxs-lookup"><span data-stu-id="b3dc6-643">Cash</span></span>               | <span data-ttu-id="b3dc6-644">Bargeld</span><span class="sxs-lookup"><span data-stu-id="b3dc6-644">Cash</span></span>                      |
| <span data-ttu-id="b3dc6-645">Elektronische Zahlung</span><span class="sxs-lookup"><span data-stu-id="b3dc6-645">Electronic Payment</span></span> | <span data-ttu-id="b3dc6-646">Übertragen</span><span class="sxs-lookup"><span data-stu-id="b3dc6-646">Transfer</span></span>                  |
| <span data-ttu-id="b3dc6-647">Scheck</span><span class="sxs-lookup"><span data-stu-id="b3dc6-647">Check</span></span>              | <span data-ttu-id="b3dc6-648">Scheck</span><span class="sxs-lookup"><span data-stu-id="b3dc6-648">Cheque</span></span>                    |
| <span data-ttu-id="b3dc6-649">Bankwechsel</span><span class="sxs-lookup"><span data-stu-id="b3dc6-649">Bank Draft</span></span>         | <span data-ttu-id="b3dc6-650">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="b3dc6-650">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="b3dc6-651">Sonstige</span><span class="sxs-lookup"><span data-stu-id="b3dc6-651">Other</span></span>              | <span data-ttu-id="b3dc6-652">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="b3dc6-652">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="b3dc6-653">Bankkontotyp</span><span class="sxs-lookup"><span data-stu-id="b3dc6-653">Bank account type</span></span>

<span data-ttu-id="b3dc6-654">Bankkontotypen werden für elektronische Zahlungen an Mitarbeiter verwendet.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-654">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="b3dc6-655">Bankkontotypen werden Dayforce als Übergweisungskontoinformationen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-655">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="b3dc6-656">Die Bankkontotypen werden bei Bedarf zu den akzeptierten Werte nach der Integration übersetzt.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-656">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="b3dc6-657">Talent</span><span class="sxs-lookup"><span data-stu-id="b3dc6-657">Talent</span></span>            | <span data-ttu-id="b3dc6-658">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b3dc6-658">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="b3dc6-659">Girokonto</span><span class="sxs-lookup"><span data-stu-id="b3dc6-659">Checking Account</span></span>  | <span data-ttu-id="b3dc6-660">Girokonto</span><span class="sxs-lookup"><span data-stu-id="b3dc6-660">CheckingAccount</span></span>           |
| <span data-ttu-id="b3dc6-661">Lohnkonto</span><span class="sxs-lookup"><span data-stu-id="b3dc6-661">Payroll Account</span></span>   | <span data-ttu-id="b3dc6-662">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="b3dc6-662">PayrollAccount</span></span>            |
| <span data-ttu-id="b3dc6-663">Sparkonto</span><span class="sxs-lookup"><span data-stu-id="b3dc6-663">Savings Account</span></span>   | <span data-ttu-id="b3dc6-664">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="b3dc6-664">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="b3dc6-665">BankGirot-Konto</span><span class="sxs-lookup"><span data-stu-id="b3dc6-665">BankGirot account</span></span> | <span data-ttu-id="b3dc6-666">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="b3dc6-666">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="b3dc6-667">PlusGirot-Konto</span><span class="sxs-lookup"><span data-stu-id="b3dc6-667">PlusGirot account</span></span> | <span data-ttu-id="b3dc6-668">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="b3dc6-668">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="b3dc6-669">Einkommenscodes</span><span class="sxs-lookup"><span data-stu-id="b3dc6-669">Earning codes</span></span>

<span data-ttu-id="b3dc6-670">Einkommenscodes bestimmen jeden Typ von Einkünften eindeutig, die Arbeitskräfte erhalten</span><span class="sxs-lookup"><span data-stu-id="b3dc6-670">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="b3dc6-671">Die Codes decken verschiedene Parameter ab, die sich auf Einkünfte beziehen, wie beispielsweise Buchhaltungsvorschriften, Steuergesetze, Berichterstellungsanforderungen und Bruttoausgleichsfähigkeit.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-671">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="b3dc6-672">Wenn eine nicht unterstützte Häufigkeit verwendet wird, wird die Häufigkeit **Jeder Lohn** standardmäßig für die Berechnung verwendet.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-672">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="b3dc6-673">Unterstützte Häufigkeiten</span><span class="sxs-lookup"><span data-stu-id="b3dc6-673">Supported frequencies</span></span>

- <span data-ttu-id="b3dc6-674">Alle</span><span class="sxs-lookup"><span data-stu-id="b3dc6-674">All</span></span>
- <span data-ttu-id="b3dc6-675">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="b3dc6-675">EVERYPAY</span></span>
- <span data-ttu-id="b3dc6-676">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="b3dc6-676">EACHPAYPERIOD</span></span>
- <span data-ttu-id="b3dc6-677">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="b3dc6-677">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="b3dc6-678">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="b3dc6-678">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="b3dc6-679">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3dc6-679">1OFMTH</span></span>
- <span data-ttu-id="b3dc6-680">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="b3dc6-680">LASTOFMTH</span></span>
- <span data-ttu-id="b3dc6-681">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3dc6-681">2OFMTH</span></span>
- <span data-ttu-id="b3dc6-682">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3dc6-682">3OFMTH</span></span>
- <span data-ttu-id="b3dc6-683">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3dc6-683">4OFMTH</span></span>
- <span data-ttu-id="b3dc6-684">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3dc6-684">5OFMTH</span></span>
- <span data-ttu-id="b3dc6-685">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3dc6-685">1N2OFMTH</span></span>
- <span data-ttu-id="b3dc6-686">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3dc6-686">3N4OFMTH</span></span>
- <span data-ttu-id="b3dc6-687">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3dc6-687">1N3OFMTH</span></span>
- <span data-ttu-id="b3dc6-688">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3dc6-688">1N4OFMTH</span></span>
- <span data-ttu-id="b3dc6-689">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3dc6-689">2N3OFMTH</span></span>
- <span data-ttu-id="b3dc6-690">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3dc6-690">2N4OFMTH</span></span>
- <span data-ttu-id="b3dc6-691">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3dc6-691">1N2N3OFMTH</span></span>
- <span data-ttu-id="b3dc6-692">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3dc6-692">1N2N4OFMTH</span></span>
- <span data-ttu-id="b3dc6-693">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3dc6-693">1N3N4OFMTH</span></span>
- <span data-ttu-id="b3dc6-694">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3dc6-694">2N3N4OFMTH</span></span>
- <span data-ttu-id="b3dc6-695">1N2N3N4OFMTH – 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b3dc6-695">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="b3dc6-696">2N3N4N5OFMth – 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="b3dc6-696">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="b3dc6-697">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="b3dc6-697">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="b3dc6-698">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="b3dc6-698">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="b3dc6-699">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="b3dc6-699">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="b3dc6-700">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="b3dc6-700">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="b3dc6-701">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="b3dc6-701">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="b3dc6-702">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="b3dc6-702">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="b3dc6-703">Adressen</span><span class="sxs-lookup"><span data-stu-id="b3dc6-703">Addresses</span></span>

<span data-ttu-id="b3dc6-704">Die Kennung bestimmter Codes für Land oder Region, Bundesland/Kanton oder Landkreis (Gemeinde) erfordert spezifische Formate, die Dayforce und Anbieter innerhalb des Landes/innerhalb der Region erkennen können.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-704">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="b3dc6-705">Obwohl das Format für Orte flexibel ist, muss jeder Ort einem Bundesland zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-705">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="b3dc6-706">Talent</span><span class="sxs-lookup"><span data-stu-id="b3dc6-706">Talent</span></span>              | <span data-ttu-id="b3dc6-707">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b3dc6-707">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="b3dc6-708">Land/Region</span><span class="sxs-lookup"><span data-stu-id="b3dc6-708">Country/Region</span></span>      | <span data-ttu-id="b3dc6-709">Ländercode</span><span class="sxs-lookup"><span data-stu-id="b3dc6-709">Country Code</span></span>          |
| <span data-ttu-id="b3dc6-710">Postleitzahl</span><span class="sxs-lookup"><span data-stu-id="b3dc6-710">Zip/Postal Code</span></span>     | <span data-ttu-id="b3dc6-711">PLZ</span><span class="sxs-lookup"><span data-stu-id="b3dc6-711">Postal Code</span></span>           |
| <span data-ttu-id="b3dc6-712">Zustand</span><span class="sxs-lookup"><span data-stu-id="b3dc6-712">State</span></span>               | <span data-ttu-id="b3dc6-713">Bundeslandcode</span><span class="sxs-lookup"><span data-stu-id="b3dc6-713">State Code</span></span>            |
| <span data-ttu-id="b3dc6-714">Stadt</span><span class="sxs-lookup"><span data-stu-id="b3dc6-714">City</span></span>                | <span data-ttu-id="b3dc6-715">Stadt</span><span class="sxs-lookup"><span data-stu-id="b3dc6-715">City</span></span>                  |
| <span data-ttu-id="b3dc6-716">Verwaltungsbezirk</span><span class="sxs-lookup"><span data-stu-id="b3dc6-716">County</span></span>              | <span data-ttu-id="b3dc6-717">Landkreis (Gemeinde)</span><span class="sxs-lookup"><span data-stu-id="b3dc6-717">County (Municipality)</span></span> |
| <span data-ttu-id="b3dc6-718">Straße</span><span class="sxs-lookup"><span data-stu-id="b3dc6-718">Street</span></span>              | <span data-ttu-id="b3dc6-719">Adresszeile 1</span><span class="sxs-lookup"><span data-stu-id="b3dc6-719">Address Line 1</span></span>        |
| <span data-ttu-id="b3dc6-720">Hausnummer</span><span class="sxs-lookup"><span data-stu-id="b3dc6-720">Street Number</span></span>       | <span data-ttu-id="b3dc6-721">Adresszeile 2</span><span class="sxs-lookup"><span data-stu-id="b3dc6-721">Address Line 2</span></span>        |
| <span data-ttu-id="b3dc6-722">Gebäudeergänzung</span><span class="sxs-lookup"><span data-stu-id="b3dc6-722">Building Complement</span></span> | <span data-ttu-id="b3dc6-723">Adresszeile 5</span><span class="sxs-lookup"><span data-stu-id="b3dc6-723">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="b3dc6-724">Ausweisnummer</span><span class="sxs-lookup"><span data-stu-id="b3dc6-724">Passport number</span></span>

<span data-ttu-id="b3dc6-725">Mitarbeiter können Ausweisinformationen melden.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-725">Employees can declare passport information.</span></span> <span data-ttu-id="b3dc6-726">Diese Informationen haben den Kennungstyp **Ausweis** und sind in Dayforce als Teil der für Mexiko spezifischen Informationen eines Mitarbeiters integriert.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-726">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="b3dc6-727">Kennungstyp = „Ausweis”</span><span class="sxs-lookup"><span data-stu-id="b3dc6-727">Identification Type = "Passport"</span></span>
- <span data-ttu-id="b3dc6-728">Ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="b3dc6-728">Issued Date</span></span>
- <span data-ttu-id="b3dc6-729">Ablaufdatum</span><span class="sxs-lookup"><span data-stu-id="b3dc6-729">Expiration Date</span></span>

<span data-ttu-id="b3dc6-730">Mitarbeiter können mehrere Kennungsnummern des Kennungstyps **Ausweis** melden.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-730">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="b3dc6-731">Jedoch wird nur der aktuell aktive Ausweiseintrag in Dayforce integriert.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-731">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="b3dc6-732">Wenn alle Ausweiseinträge abgelaufen sind, ist der Ausweis, der zuletzt ausgestellt wurde, in Dayforce integriert.</span><span class="sxs-lookup"><span data-stu-id="b3dc6-732">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>
