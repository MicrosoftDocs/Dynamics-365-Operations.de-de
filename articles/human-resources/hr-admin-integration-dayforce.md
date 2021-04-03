---
title: Integration mit Dayforce konfigurieren
description: Die Integration zwischen Microsoft Dynamics 365 Human Resources und Ceridian Dayforce erfordert mehrere Konfigurationsschritte, die in diesem Artikel beschrieben sind. Sie müssen die Integration sowohl in Human Resources als auch in Dayforce konfigurieren, bevor Sie einen Zahlungslauf verarbeiten können.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: PersonnelIntegrationConfiguration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2d5f65672960716bee3f58c98ccce249fdbf8697
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467144"
---
# <a name="configure-integration-with-dayforce"></a><span data-ttu-id="edbca-104">Integration mit Dayforce konfigurieren</span><span class="sxs-lookup"><span data-stu-id="edbca-104">Configure integration with Dayforce</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="edbca-105">Die Integration zwischen Microsoft Dynamics 365 Human Resources und Ceridian Dayforce erfordert mehrere Konfigurationsschritte, die in diesem Artikel beschrieben sind.</span><span class="sxs-lookup"><span data-stu-id="edbca-105">The integration between Microsoft Dynamics 365 Human Resources and Ceridian Dayforce relies on several configuration steps that are described in this article.</span></span> <span data-ttu-id="edbca-106">Sie müssen die Integration sowohl in Human Resources als auch in Dayforce konfigurieren, bevor Sie einen Zahlungslauf verarbeiten können.</span><span class="sxs-lookup"><span data-stu-id="edbca-106">You must configure the integration in both Human Resources and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="edbca-107">Wenn Sie einen Dienst wie Dayforce verwenden, um Zahlungsläufe abzuschließen, müssen Sie die Integration in Human Resources ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="edbca-107">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Human Resources.</span></span> <span data-ttu-id="edbca-108">Die Integration erfordert bestimmte Daten aus Human Resources.</span><span class="sxs-lookup"><span data-stu-id="edbca-108">The integration requires specific data from Human Resources.</span></span> <span data-ttu-id="edbca-109">Daher müssen Sie überprüfen, dass die Daten, die Dayforce zugeordnet sind, in Human Resources in einer Weise konfiguriert werden, die die Integration unterstützt.</span><span class="sxs-lookup"><span data-stu-id="edbca-109">Therefore, you must verify that data that is mapped to Dayforce is configured in Human Resources in a manner that supports the integration.</span></span> <span data-ttu-id="edbca-110">Bei der Integration werden die folgenden allgemeinen Kategorien von Daten verwendet:</span><span class="sxs-lookup"><span data-stu-id="edbca-110">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="edbca-111">Personalverwaltungsdaten</span><span class="sxs-lookup"><span data-stu-id="edbca-111">Human resources data</span></span>
- <span data-ttu-id="edbca-112">Vergütungsdaten</span><span class="sxs-lookup"><span data-stu-id="edbca-112">Compensation data</span></span>
- <span data-ttu-id="edbca-113">Lohndaten, wie Lohnzyklen, Lohnperioden und Einkommenscodes</span><span class="sxs-lookup"><span data-stu-id="edbca-113">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="edbca-114">Arbeitskraftdaten</span><span class="sxs-lookup"><span data-stu-id="edbca-114">Worker data</span></span>

<span data-ttu-id="edbca-115">In diesem Artikel werden die Schritte beschrieben, die Sie befolgen müssen, um die Integration zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="edbca-115">This article describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="edbca-116">Es werden auch die Datentypen und die Konfigurationsdetails erklärt, die für die Integration erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="edbca-116">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="edbca-117">Die Integration aktivieren</span><span class="sxs-lookup"><span data-stu-id="edbca-117">Enable the integration</span></span>

<span data-ttu-id="edbca-118">In Human Resources müssen Sie die Integration aktivieren und die Konfigurationsinformationen eingeben, um eine Verbindung mit Dayforce herzustellen.</span><span class="sxs-lookup"><span data-stu-id="edbca-118">In Human Resources, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="edbca-119">Wenn Sie möchten, dass die erstellte Hauptbuchtransaktion in Microsoft Dynamics 365 Finance importiert wird, müssen Sie auch ein Microsoft Azure-Speicherkonto einrichten und die Azure Storage-Verbindungszeichenfolge in Finance eingeben.</span><span class="sxs-lookup"><span data-stu-id="edbca-119">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 Finance, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance.</span></span>

<span data-ttu-id="edbca-120">Um die Integration in Human Resources zu aktivieren, gehen Sie folgendermaßen vor.</span><span class="sxs-lookup"><span data-stu-id="edbca-120">To turn on the integration in Human Resources, follow these steps.</span></span>

1. <span data-ttu-id="edbca-121">Wählen Sie auf der Seite **Systemverwaltung** die Option **Integrationskonfiguration** aus.</span><span class="sxs-lookup"><span data-stu-id="edbca-121">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="edbca-122">Geben Sie den sicheren Datenübertragungsprotokoll-(FTP)-Endpunkt und den sicheren FTP-Ordnerpfad ein.</span><span class="sxs-lookup"><span data-stu-id="edbca-122">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="edbca-123">Geben Sie den Benutzernamen und das Kennwort des Benutzers ein, der auf den sicheren FTP-Endpunkt und Ordnerpfad zugreift.</span><span class="sxs-lookup"><span data-stu-id="edbca-123">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="edbca-124">Testen Sie die Verbindung nach Bedarf, und legen Sie die Option **Lohnintegration aktivieren** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="edbca-124">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="edbca-125">Wenn die Integration aktiviert ist, werden Datenexportpaket und Dateien erstellt und die Häufigkeit wird festgelegt.</span><span class="sxs-lookup"><span data-stu-id="edbca-125">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="edbca-126">Sie können diese Häufigkeit nach Bedarf ändern.</span><span class="sxs-lookup"><span data-stu-id="edbca-126">You can change this frequency as you require.</span></span>

<span data-ttu-id="edbca-127">Weitere Informationen zu Azure-Speicherkonten und Azure Storage-Verbindungszeichenfolgen finden Sie in den folgenden Azure-Artikeln:</span><span class="sxs-lookup"><span data-stu-id="edbca-127">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure articles:</span></span>

- [<span data-ttu-id="edbca-128">Über Azure-Speicherkonten</span><span class="sxs-lookup"><span data-stu-id="edbca-128">About Azure storage accounts</span></span>](https://docs.microsoft.com/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="edbca-129">Azure Storage-Verbindungszeichenfolgen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="edbca-129">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="edbca-130">Technische Details, wenn Lohnintegration aktiviert ist</span><span class="sxs-lookup"><span data-stu-id="edbca-130">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="edbca-131">Die Aktivierung von Lohnintegration hat zwei primäre Auswirkungen:</span><span class="sxs-lookup"><span data-stu-id="edbca-131">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="edbca-132">Ein Datenexportprojekt namens „Lohnintegrationsexport“ wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="edbca-132">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="edbca-133">Dieses Projekt enthält die Entitäten und Felder, die für die Lohnintegration erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="edbca-133">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="edbca-134">Um das Projekt zu überprüfen, wechseln Sie zu **Systemverwaltung**, wählen Sie die Kachel **Datenverwaltung** aus, und öffnen Sie anschließend das Datenprojekt aus der Projektliste.</span><span class="sxs-lookup"><span data-stu-id="edbca-134">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="edbca-135">Dieser Stapelverarbeitungsauftrag führt das Datenexportprojekt aus, verschlüsselt das Datenpaket und überträgt die Datenenpaketdatei auf den SFTP-Endpunkt, der auf dem Bildschirm **Integrationskonfiguration** konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="edbca-135">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="edbca-136">Das Datenpaket, das zum SFTP-Endpunkt übertragen wird, wird mit einem Schlüssel verschlüsselt, für das Paket eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="edbca-136">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="edbca-137">Der Schlüssel befindet sich in einer Azure Key Vault, auf den nur durch Ceridian zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="edbca-137">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="edbca-138">Es ist nicht möglich, die Datenpaketinhalte zu entschlüsseln und zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="edbca-138">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="edbca-139">Wenn Sie den Inhalt des Datenpakets überprüfen möchten, müssen Sie das Datenprojekt „Lohnintegrationsexport“ manuell exportieren, herunterladen und dann öffnen.</span><span class="sxs-lookup"><span data-stu-id="edbca-139">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="edbca-140">Beim manuellen Export wird keine Verschlüsselung angewendet oder das Paket übertragen.</span><span class="sxs-lookup"><span data-stu-id="edbca-140">Manual export will not apply encryption or transfer the package.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="edbca-141">Ihre Daten konfigurieren</span><span class="sxs-lookup"><span data-stu-id="edbca-141">Configure your data</span></span> 

<span data-ttu-id="edbca-142">Um die Lohnbuchung zu verarbeiten, müssen Sie Personalverwaltungsdaten in Human Resources konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="edbca-142">To process payroll, you must configure human resource data in Human Resources.</span></span> <span data-ttu-id="edbca-143">Sie müssen Organisationsdaten, wie Stellen und Positionen, zusammen mit Vorteilen Vergütungsinformationen einrichten.</span><span class="sxs-lookup"><span data-stu-id="edbca-143">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="edbca-144">Diese Informationen stellen Beschäftigung, Lohn und die Abzugsinformationen bereit, die zur Generierung der Mitarbeiterentlohnung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="edbca-144">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="edbca-145">Personalverwaltungsdaten</span><span class="sxs-lookup"><span data-stu-id="edbca-145">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="edbca-146">Vergütungen</span><span class="sxs-lookup"><span data-stu-id="edbca-146">Benefits</span></span> 

<span data-ttu-id="edbca-147">Die Personalverwaltung stellt eine Reihe von Tools für die Einrichtung und Verwaltung der Vorteile, Abzüge und Vergütungspläne der Arbeitskräfte bereit, die eine Organisation für seine Arbeitskräfte anbietet oder verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="edbca-147">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="edbca-148">Wenn Sie Vorteile erstellen, sollten Sie folgende Daten und Konfigurationen bedenken, die in Dayforce verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="edbca-148">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="edbca-149">Vorteilspläne</span><span class="sxs-lookup"><span data-stu-id="edbca-149">Benefit plans</span></span>

- <span data-ttu-id="edbca-150">Plan (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-150">Plan (required)</span></span>
- <span data-ttu-id="edbca-151">Typ (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-151">Type (required)</span></span>
- <span data-ttu-id="edbca-152">Lohnauswirkung (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-152">Payroll impact (required)</span></span>
- <span data-ttu-id="edbca-153">Rückstände wiederherstellen</span><span class="sxs-lookup"><span data-stu-id="edbca-153">Recover arrears</span></span>
- <span data-ttu-id="edbca-154">Abzugsverfahren</span><span class="sxs-lookup"><span data-stu-id="edbca-154">Deduction method</span></span>
- <span data-ttu-id="edbca-155">Abzugspriorität</span><span class="sxs-lookup"><span data-stu-id="edbca-155">Deduction priority</span></span>
- <span data-ttu-id="edbca-156">Periode eingrenzen</span><span class="sxs-lookup"><span data-stu-id="edbca-156">Limit period</span></span>
- <span data-ttu-id="edbca-157">Limitbetrag</span><span class="sxs-lookup"><span data-stu-id="edbca-157">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="edbca-158">Vergütungen</span><span class="sxs-lookup"><span data-stu-id="edbca-158">Benefits</span></span>

- <span data-ttu-id="edbca-159">Plan (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-159">Plan (required)</span></span>
- <span data-ttu-id="edbca-160">Typ (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-160">Type (required)</span></span>
- <span data-ttu-id="edbca-161">Option (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-161">Option (required)</span></span>
- <span data-ttu-id="edbca-162">Vorteilskennung (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-162">Benefit ID (required)</span></span>
- <span data-ttu-id="edbca-163">Häufigkeit</span><span class="sxs-lookup"><span data-stu-id="edbca-163">Frequency</span></span>
- <span data-ttu-id="edbca-164">Basis</span><span class="sxs-lookup"><span data-stu-id="edbca-164">Basis</span></span>
- <span data-ttu-id="edbca-165">Betrag oder Satz</span><span class="sxs-lookup"><span data-stu-id="edbca-165">Amount or rate</span></span>
- <span data-ttu-id="edbca-166">Einkommenscode</span><span class="sxs-lookup"><span data-stu-id="edbca-166">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="edbca-167">Unterstützte Häufigkeiten</span><span class="sxs-lookup"><span data-stu-id="edbca-167">Supported frequencies</span></span> 

- <span data-ttu-id="edbca-168">Wöchentlich</span><span class="sxs-lookup"><span data-stu-id="edbca-168">Weekly</span></span>
- <span data-ttu-id="edbca-169">14-tägig</span><span class="sxs-lookup"><span data-stu-id="edbca-169">Bi-weekly</span></span>
- <span data-ttu-id="edbca-170">Halbmonatlich</span><span class="sxs-lookup"><span data-stu-id="edbca-170">Semi-monthly</span></span>
- <span data-ttu-id="edbca-171">Monatlich</span><span class="sxs-lookup"><span data-stu-id="edbca-171">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="edbca-172">Unterstützte Basen</span><span class="sxs-lookup"><span data-stu-id="edbca-172">Supported bases</span></span> 

- <span data-ttu-id="edbca-173">Fester Betrag</span><span class="sxs-lookup"><span data-stu-id="edbca-173">Fixed amount</span></span>
- <span data-ttu-id="edbca-174">Prozent des Einkommens</span><span class="sxs-lookup"><span data-stu-id="edbca-174">Percent of earnings</span></span>
- <span data-ttu-id="edbca-175">Produktive Stunden</span><span class="sxs-lookup"><span data-stu-id="edbca-175">Productive hours</span></span>

<span data-ttu-id="edbca-176">Dayforce erstellt die folgenden Abzüge, basierend auf den Lohnauswirkungen, die im Vorteilsplan definiert sind.</span><span class="sxs-lookup"><span data-stu-id="edbca-176">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="edbca-177">Auswahl in Human Resources</span><span class="sxs-lookup"><span data-stu-id="edbca-177">Selection in Human Resources</span></span>        | <span data-ttu-id="edbca-178">Ergebnis in Dayforce</span><span class="sxs-lookup"><span data-stu-id="edbca-178">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="edbca-179">Nichts</span><span class="sxs-lookup"><span data-stu-id="edbca-179">None</span></span>                       | <span data-ttu-id="edbca-180">Es wird kein Abzug erstellt.</span><span class="sxs-lookup"><span data-stu-id="edbca-180">No deduction is created.</span></span>                      |
| <span data-ttu-id="edbca-181">Nur Abzug</span><span class="sxs-lookup"><span data-stu-id="edbca-181">Deduction only</span></span>             | <span data-ttu-id="edbca-182">Ein Mitarbeiterabzug wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="edbca-182">An employee deduction is created.</span></span>             |
| <span data-ttu-id="edbca-183">Nur Beitrag</span><span class="sxs-lookup"><span data-stu-id="edbca-183">Contribution only</span></span>          | <span data-ttu-id="edbca-184">Ein Arbeitgeberabzug wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="edbca-184">An employer deduction is created.</span></span>             |
| <span data-ttu-id="edbca-185">Abzug und Beitrag</span><span class="sxs-lookup"><span data-stu-id="edbca-185">Deduction and contribution</span></span> | <span data-ttu-id="edbca-186">Mitarbeiter- und Arbeitgeberabzüge werden erstellt.</span><span class="sxs-lookup"><span data-stu-id="edbca-186">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="edbca-187">Weitere Informationen darüber, wie Sie ein Vorteilsprogramm definieren und verwalten finden Sie in den folgenden Artikeln:</span><span class="sxs-lookup"><span data-stu-id="edbca-187">For more information about how to define and manage a benefits program, see the following articles:</span></span>

- [<span data-ttu-id="edbca-188">Mitarbeitervorteilsprogramm anbieten</span><span class="sxs-lookup"><span data-stu-id="edbca-188">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="edbca-189">Neue Vergütung erstellen</span><span class="sxs-lookup"><span data-stu-id="edbca-189">Create a new benefit</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="edbca-190">Vorteilsberechtigungsregeln und Richtlinien definieren</span><span class="sxs-lookup"><span data-stu-id="edbca-190">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="edbca-191">Vorteile von Arbeitskräften registrieren und entfernen</span><span class="sxs-lookup"><span data-stu-id="edbca-191">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="edbca-192">Vergütung</span><span class="sxs-lookup"><span data-stu-id="edbca-192">Compensation</span></span> 

<span data-ttu-id="edbca-193">Die Vergütungsverwaltung dient zum Steuern der Abwicklung des Grundlohns und der Prämien.</span><span class="sxs-lookup"><span data-stu-id="edbca-193">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="edbca-194">Sie steuern den festen Grundlohn eines Mitarbeiters und dessen Lohnsteigerungen nach Plänen für feste Vergütung.</span><span class="sxs-lookup"><span data-stu-id="edbca-194">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="edbca-195">Die Zahlung leistungsbezogener Prämien, wie Boni, Leistungsprämien, Aktienoptionen und -überlassungen sowie Einmalprämien werden durch Pläne für variable Vergütung gesteuert.</span><span class="sxs-lookup"><span data-stu-id="edbca-195">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="edbca-196">Dayforce verwendet Vergütungsinformationen, um einen Stunden- oder Jahressatz für einen Mitarbeiter zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="edbca-196">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="edbca-197">Feste Vergütungspläne und Lohnsatzumrechnungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="edbca-197">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="edbca-198">Mitarbeiter müssen einem festen Vergütungsplan zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="edbca-198">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="edbca-199">Weitere Informationen zu Kompensationsplänen finden Sie in den folgenden Artikeln:</span><span class="sxs-lookup"><span data-stu-id="edbca-199">For more information about compensation plans, see the following articles:</span></span>

- [<span data-ttu-id="edbca-200">Feste Vergütungspläne erstellen</span><span class="sxs-lookup"><span data-stu-id="edbca-200">Create fixed compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="edbca-201">Variable Vergütungspläne erstellen</span><span class="sxs-lookup"><span data-stu-id="edbca-201">Create variable compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="edbca-202">Gehalts-/Vergütungsstruktur und -pläne entwickeln</span><span class="sxs-lookup"><span data-stu-id="edbca-202">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="edbca-203">Vergütung verarbeiten</span><span class="sxs-lookup"><span data-stu-id="edbca-203">Process compensation</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="edbca-204">Vergütungsprozess definieren und Ergebnisse berechnen</span><span class="sxs-lookup"><span data-stu-id="edbca-204">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="edbca-205">Einen Mitarbeiters in einem Plan für eine feste Vergütung registrieren</span><span class="sxs-lookup"><span data-stu-id="edbca-205">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="edbca-206">Einen Mitarbeiter in einem Plan für variable Vergütung registrieren</span><span class="sxs-lookup"><span data-stu-id="edbca-206">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="edbca-207">Stellentyp</span><span class="sxs-lookup"><span data-stu-id="edbca-207">Jobs</span></span> 

<span data-ttu-id="edbca-208">Eine Stelle ist eine Sammlung der Aufgaben und Zuständigkeiten, die für eine Person, die eine Tätigkeit ausführt, obligatorisch sind.</span><span class="sxs-lookup"><span data-stu-id="edbca-208">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="edbca-209">Weitere Informationen finden Sie in folgenden Artikeln:</span><span class="sxs-lookup"><span data-stu-id="edbca-209">For more information, see the following articles:</span></span>

- [<span data-ttu-id="edbca-210">Komponenten einer Stelle einrichten</span><span class="sxs-lookup"><span data-stu-id="edbca-210">Setting up the components of a job</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="edbca-211">Neue Stellen definieren</span><span class="sxs-lookup"><span data-stu-id="edbca-211">Define new jobs</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="edbca-212">Positionen</span><span class="sxs-lookup"><span data-stu-id="edbca-212">Positions</span></span>

<span data-ttu-id="edbca-213">Eine Position ist eine einzelne Instanz eines Einzelvorgangs.</span><span class="sxs-lookup"><span data-stu-id="edbca-213">A position is an individual instance of a job.</span></span> <span data-ttu-id="edbca-214">Beispielsweise ist die Position „Verkaufsleiter (Ost)” eine der Positionen, die der Stelle „Verkaufsleiter” zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="edbca-214">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="edbca-215">Eine Position ist in einer Abteilung vorhanden.</span><span class="sxs-lookup"><span data-stu-id="edbca-215">A position exists in a department.</span></span> <span data-ttu-id="edbca-216">Nur jeweils eine Arbeitskraft kann jeder Position zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="edbca-216">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="edbca-217">Bedenken Sie die folgenden Daten und Konfigurationen, wenn Sie Positionen einrichten:</span><span class="sxs-lookup"><span data-stu-id="edbca-217">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="edbca-218">Position (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-218">Position (required)</span></span>
- <span data-ttu-id="edbca-219">Beschreibung (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-219">Description (required)</span></span>
- <span data-ttu-id="edbca-220">Stelle (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-220">Job (required)</span></span>
- <span data-ttu-id="edbca-221">Abteilung (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-221">Department (required)</span></span>
- <span data-ttu-id="edbca-222">Positionstyp (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-222">Position type (required)</span></span>
- <span data-ttu-id="edbca-223">Vollzeitäquivalent</span><span class="sxs-lookup"><span data-stu-id="edbca-223">Full-time equivalent</span></span>
- <span data-ttu-id="edbca-224">Normale Stunden pro Jahr (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-224">Annual regular hours (required)</span></span>
- <span data-ttu-id="edbca-225">Gezahlt von der juristischen Person (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-225">Paid by legal entity (required)</span></span>
- <span data-ttu-id="edbca-226">Lohnzyklus (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-226">Pay cycle (required)</span></span>
- <span data-ttu-id="edbca-227">Standardfinanzdimension – Kostenstelle (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-227">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="edbca-228">Arbeitskraftzuweisung – Arbeitskraft, Zuweisungsanfang, Zuweisungsende, Ursachencode</span><span class="sxs-lookup"><span data-stu-id="edbca-228">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="edbca-229">Wenn mehrere Positionen in derselben Abteilung derselben Stelle zugeordnet sind, werden sie in einer einzelnen Position in Dayforce konsolidiert.</span><span class="sxs-lookup"><span data-stu-id="edbca-229">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="edbca-230">Weitere Informationen finden Sie in folgenden Artikeln:</span><span class="sxs-lookup"><span data-stu-id="edbca-230">For more information, see the following articles:</span></span>

- [<span data-ttu-id="edbca-231">Belegschaft mittels Abteilungen, Stellen und Positionen verwalten</span><span class="sxs-lookup"><span data-stu-id="edbca-231">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="edbca-232">Positionen einrichten</span><span class="sxs-lookup"><span data-stu-id="edbca-232">Set up positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="edbca-233">Abteilungen</span><span class="sxs-lookup"><span data-stu-id="edbca-233">Departments</span></span>

<span data-ttu-id="edbca-234">Eine Abteilung ist eine Organisationseinheit, die eine Kategorie oder einen funktionalen Bereich einer Organisation darstellt.</span><span class="sxs-lookup"><span data-stu-id="edbca-234">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="edbca-235">Eine Abteilung ist für einen bestimmten Bereich der Organisation wie zum Beispiel Verkauf, Buchhaltung oder Personalverwaltung zuständig.</span><span class="sxs-lookup"><span data-stu-id="edbca-235">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="edbca-236">Sie können Abteilungen verwenden, um zu Funktionsbereiche zu melden.</span><span class="sxs-lookup"><span data-stu-id="edbca-236">You can use departments to report on functional areas.</span></span> <span data-ttu-id="edbca-237">Abteilungen können Gewinn- und Verlustzuständigkeit haben.</span><span class="sxs-lookup"><span data-stu-id="edbca-237">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="edbca-238">Weitere Informationen finden Sie in folgenden Artikeln:</span><span class="sxs-lookup"><span data-stu-id="edbca-238">For more information, see the following articles:</span></span>

- [<span data-ttu-id="edbca-239">Abteilung erstellen und der Abteilungshierarchie zuordnen</span><span class="sxs-lookup"><span data-stu-id="edbca-239">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="edbca-240">Neue Abteilungen definieren</span><span class="sxs-lookup"><span data-stu-id="edbca-240">Define new departments</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="edbca-241">Lohnzyklen und Lohnperioden</span><span class="sxs-lookup"><span data-stu-id="edbca-241">Pay cycles and pay periods</span></span>

<span data-ttu-id="edbca-242">Ein Lohnzyklus bestimmt, wie oft Lohn ausgezahlt wird, sowie die spezifischen Tage, an denen Arbeitskräfte bezahlt werden.</span><span class="sxs-lookup"><span data-stu-id="edbca-242">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="edbca-243">Ein Lohnzyklus kann beispielsweise monatlich sein, und Mitarbeiter werden am letzten Tag des Monats bezahlt.</span><span class="sxs-lookup"><span data-stu-id="edbca-243">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="edbca-244">Alternativ könnte ein Lohnzyklus wöchentlich sein, und Mitarbeiter werden am Dienstag nach Ende der Lohnperiode bezahlt.</span><span class="sxs-lookup"><span data-stu-id="edbca-244">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="edbca-245">Lohnzyklen werden Positionen zugewiesen, um zu steuern, wann Mitarbeiter in diesen Positionen bezahlt werden.</span><span class="sxs-lookup"><span data-stu-id="edbca-245">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="edbca-246">Nachdem Sie Lohnzyklen erstellen, können Sie Lohnperioden für jeden Zyklus generieren.</span><span class="sxs-lookup"><span data-stu-id="edbca-246">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="edbca-247">Jede Lohnperiode enthält ein Standardzahlungsdatum, das auf den von Ihnen bereitgestellten Informationen basiert.</span><span class="sxs-lookup"><span data-stu-id="edbca-247">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="edbca-248">Allerdings können Sie das Standardzahlungsdatum in einer Lohnperiode ändern, um Ausnahmen zuzulassen, wie beispielsweise wenn das Zahlungsdatum auf einen Feiertag fällt.</span><span class="sxs-lookup"><span data-stu-id="edbca-248">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="edbca-249">Die folgenden Informationen werden in Dayforce verwendet:</span><span class="sxs-lookup"><span data-stu-id="edbca-249">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="edbca-250">Lohnzyklus (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-250">Pay cycle (required)</span></span>
- <span data-ttu-id="edbca-251">Lohnzyklushäufigkeit (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-251">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="edbca-252">Periodenstartdatum (erstes erforderliche Lohnperiode)</span><span class="sxs-lookup"><span data-stu-id="edbca-252">Period start date (first pay period required)</span></span>
- <span data-ttu-id="edbca-253">Standardzahlungsdatum (erste erforderliche Lohnperiode)</span><span class="sxs-lookup"><span data-stu-id="edbca-253">Default payment date (first pay period required)</span></span>

<span data-ttu-id="edbca-254">Diese Informationen werden mit Dayforce als Lohngruppen integriert und sind nach Land oder Region für jeden Lohnzyklus getrennt.</span><span class="sxs-lookup"><span data-stu-id="edbca-254">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="edbca-255">Es muss mindestens eine Lohnperiode vor der Integration generiert werden.</span><span class="sxs-lookup"><span data-stu-id="edbca-255">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="edbca-256">Dayforce generiert Lohngruppenkalender und Zahlungsdaten basierend auf dem Anfangsdatum der ersten Lohnperiode und dem Standardzahlungsdatums, das in Human Resources eingerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="edbca-256">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Human Resources.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="edbca-257">Einkommenscodes</span><span class="sxs-lookup"><span data-stu-id="edbca-257">Earning codes</span></span>

<span data-ttu-id="edbca-258">Einkommenscodes bestimmen jeden Typ von Einkünften eindeutig, die Arbeitskräfte erhalten</span><span class="sxs-lookup"><span data-stu-id="edbca-258">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="edbca-259">Die Codes haben verschiedene Parameter, die sich auf Einkünfte beziehen, wie beispielsweise Buchhaltungsvorschriften, Steuergesetze, Berichterstellungsanforderungen und Bruttoausgleichsfähigkeit.</span><span class="sxs-lookup"><span data-stu-id="edbca-259">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="edbca-260">Die folgenden Informationen werden in Dayforce verwendet:</span><span class="sxs-lookup"><span data-stu-id="edbca-260">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="edbca-261">Einkommenscode (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-261">Earning Code (required)</span></span>
- <span data-ttu-id="edbca-262">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="edbca-262">Description</span></span>
- <span data-ttu-id="edbca-263">Maßeinheit</span><span class="sxs-lookup"><span data-stu-id="edbca-263">Unit of measure</span></span>
- <span data-ttu-id="edbca-264">Produktiv</span><span class="sxs-lookup"><span data-stu-id="edbca-264">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="edbca-265">Arbeitskraftdaten</span><span class="sxs-lookup"><span data-stu-id="edbca-265">Worker data</span></span>

<span data-ttu-id="edbca-266">Datensätze für die verschiedenen Arten von Arbeitskräften, die Sie haben, sind für Ihre Personalverwaltung- sowie für Ihre Lohnsysteme von Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="edbca-266">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="edbca-267">Anhand der eingegebenen Informationen lassen sich Arbeitskräfte sowie personenbezogene Informationen nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="edbca-267">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="edbca-268">Sie können die folgenden Informationen für Arbeitskräfte verwalten:</span><span class="sxs-lookup"><span data-stu-id="edbca-268">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="edbca-269">**Basis** – Verwalten grundlegender Informationen über eine Arbeitskraft, beispielsweise Kontaktinformationen, demografische Informationen, Kennungsinformationen, Familieninformationen, Militärdienststatus, Ausländerinformationen sowie personenbezogene und Notfallkontakte.</span><span class="sxs-lookup"><span data-stu-id="edbca-269">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="edbca-270">**Beschäftigung** – Verwalten von Informationen zum Beschäftigungsverhältnis einer Arbeitskraft, wie Unternehmens- oder Organisationszugehörigkeit, Positionszuweisung, Start- und Enddatum, Arbeitsberechtigung, Beschäftigungsbedingungen, Rente, Urlaub und Versetzungen.</span><span class="sxs-lookup"><span data-stu-id="edbca-270">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="edbca-271">**Urlaub und Abwesenheit** – Verwalten von Informationen zur Abwesenheit einer Arbeitskraft, beispielsweise Arbeitszeitkalender, Abwesenheitsbuchungen und Abwesenheitseinrichtung.</span><span class="sxs-lookup"><span data-stu-id="edbca-271">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="edbca-272">**Vergütung und Lohn** – Verwalten von Informationen zu den Vergütungsplänen und Lohndaten einer Arbeitskraft, wie der Planregistrierung, Boni, Leistung, Provision, Steuerdaten, Pensionierung und Gehaltsabzüge.</span><span class="sxs-lookup"><span data-stu-id="edbca-272">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="edbca-273">Wenn Sie Arbeitskraftinformationen eingeben, sollten Sie folgende Daten und Konfigurationen bedenken, die in Dayforce verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="edbca-273">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="edbca-274">Allgemeine Angaben</span><span class="sxs-lookup"><span data-stu-id="edbca-274">General information</span></span>

- <span data-ttu-id="edbca-275">Personalnummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-275">Personnel number (required)</span></span>
- <span data-ttu-id="edbca-276">Vorname (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-276">First name (required)</span></span>
- <span data-ttu-id="edbca-277">Nachname (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-277">Last name (required)</span></span>
- <span data-ttu-id="edbca-278">Zweiter Vorname</span><span class="sxs-lookup"><span data-stu-id="edbca-278">Middle name</span></span>
- <span data-ttu-id="edbca-279">Dienstalterdatum</span><span class="sxs-lookup"><span data-stu-id="edbca-279">Seniority date</span></span>
- <span data-ttu-id="edbca-280">Bekannt als</span><span class="sxs-lookup"><span data-stu-id="edbca-280">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="edbca-281">Personenbezogene Informationen</span><span class="sxs-lookup"><span data-stu-id="edbca-281">Personal information</span></span>

- <span data-ttu-id="edbca-282">Familienstand (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-282">Marital status (required)</span></span>
- <span data-ttu-id="edbca-283">Geburtsdatum (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-283">Birth date (required)</span></span>
- <span data-ttu-id="edbca-284">Geschlecht (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-284">Gender (required)</span></span>
- <span data-ttu-id="edbca-285">Person mit Behinderung</span><span class="sxs-lookup"><span data-stu-id="edbca-285">Person with disabilities</span></span>
- <span data-ttu-id="edbca-286">Nationalitätsland/-region (nur für Mexiko)</span><span class="sxs-lookup"><span data-stu-id="edbca-286">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="edbca-287">Adressdaten</span><span class="sxs-lookup"><span data-stu-id="edbca-287">Address information</span></span>

- <span data-ttu-id="edbca-288">Primär (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-288">Primary (required)</span></span>
- <span data-ttu-id="edbca-289">Land/Region (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-289">Country/region (required)</span></span>
- <span data-ttu-id="edbca-290">Postleitzahl (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-290">Postal code (required)</span></span>
- <span data-ttu-id="edbca-291">Hausnummer (erforderlich) (nur für Mexiko)</span><span class="sxs-lookup"><span data-stu-id="edbca-291">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="edbca-292">Gebäudeergänzung (nur für Mexiko)</span><span class="sxs-lookup"><span data-stu-id="edbca-292">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="edbca-293">Ort (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-293">City (required)</span></span>
- <span data-ttu-id="edbca-294">Bundesland/Kanton (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-294">State (required)</span></span>
- <span data-ttu-id="edbca-295">Landkreis (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-295">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="edbca-296">Kontaktdaten</span><span class="sxs-lookup"><span data-stu-id="edbca-296">Contact information</span></span> 

- <span data-ttu-id="edbca-297">Primär (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-297">Primary (required)</span></span>
- <span data-ttu-id="edbca-298">Kontaktnummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-298">Contact number (required)</span></span>
- <span data-ttu-id="edbca-299">Durchwahl</span><span class="sxs-lookup"><span data-stu-id="edbca-299">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="edbca-300">Lohndaten und Einkommenscodes</span><span class="sxs-lookup"><span data-stu-id="edbca-300">Payroll information and earning codes</span></span>

<span data-ttu-id="edbca-301">Mitarbeitern müssen bestimmte Einkommen mit einer bestimmten Zahlungshäufigkeit zugewiesen werden und sie müssen eine bevorzugte Zahlungsmethode haben.</span><span class="sxs-lookup"><span data-stu-id="edbca-301">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="edbca-302">Die folgenden Felder werden in Dayforce verwendet, um zu gewährleisten, dass diese Voreinstellungen und Einstellungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="edbca-302">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="edbca-303">Einkommenscodes</span><span class="sxs-lookup"><span data-stu-id="edbca-303">Earning codes</span></span>

- <span data-ttu-id="edbca-304">Position (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-304">Position (required)</span></span>
- <span data-ttu-id="edbca-305">Einkommenscode (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-305">Earning Code (required)</span></span>
- <span data-ttu-id="edbca-306">Häufigkeit (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-306">Frequency (required)</span></span>
- <span data-ttu-id="edbca-307">Betrag (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-307">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="edbca-308">Lohndaten</span><span class="sxs-lookup"><span data-stu-id="edbca-308">Payroll information</span></span>

- <span data-ttu-id="edbca-309">Zahlungsmethode</span><span class="sxs-lookup"><span data-stu-id="edbca-309">Payment Method</span></span>
- <span data-ttu-id="edbca-310">Wirtschaftliche Region (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-310">Economic Region (required)</span></span>
- <span data-ttu-id="edbca-311">Mitarbeitervergütungs-ID</span><span class="sxs-lookup"><span data-stu-id="edbca-311">Employee Benefits ID</span></span>
- <span data-ttu-id="edbca-312">Personalausweisnummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-312">National ID Number (required)</span></span>
- <span data-ttu-id="edbca-313">Militärdienstnummer</span><span class="sxs-lookup"><span data-stu-id="edbca-313">Military Service Number</span></span>
- <span data-ttu-id="edbca-314">Schichtkennung (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-314">Shift ID (required)</span></span>
- <span data-ttu-id="edbca-315">Steuernummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-315">Tax Number (required)</span></span>
- <span data-ttu-id="edbca-316">Gewerkschaftskennung (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-316">Union ID (required)</span></span>
- <span data-ttu-id="edbca-317">Arbeitstagkennung (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-317">Work Day ID (required)</span></span>
- <span data-ttu-id="edbca-318">Arbeitserlaubnisnummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-318">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="edbca-319">Für die Zahlungsmethode unterstützt Mexiko **Bargeld**, **Scheck** (der physische Scheck des Unternehmens) und **Elektronische Zahlung**.</span><span class="sxs-lookup"><span data-stu-id="edbca-319">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="edbca-320">Wenn keine Zahlungsmethode angegeben wird, wird **Scheck** standardmäßig verwendet.</span><span class="sxs-lookup"><span data-stu-id="edbca-320">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="edbca-321">Anstellungsdetails</span><span class="sxs-lookup"><span data-stu-id="edbca-321">Employment details</span></span>

<span data-ttu-id="edbca-322">Beschäftigungsdetailhistorie wird als Schlüsselinformation verwendet, um die Status für Einstellung, Kündigung und erneute Einstellung in Dayforce abzuleiten.</span><span class="sxs-lookup"><span data-stu-id="edbca-322">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="edbca-323">Dayforce unterstützt nur einen aktiven Beschäftigungsdatensatz gleichzeitig.</span><span class="sxs-lookup"><span data-stu-id="edbca-323">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="edbca-324">Datum des Beschäftigungsbeginns (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-324">Employment start date (required)</span></span>
- <span data-ttu-id="edbca-325">Datum des Beschäftigungsendes</span><span class="sxs-lookup"><span data-stu-id="edbca-325">Employment end date</span></span>
- <span data-ttu-id="edbca-326">Eintrittstermin</span><span class="sxs-lookup"><span data-stu-id="edbca-326">Start date</span></span>
- <span data-ttu-id="edbca-327">Angepasster Tätigkeitsbeginn</span><span class="sxs-lookup"><span data-stu-id="edbca-327">Adjusted start date</span></span>
- <span data-ttu-id="edbca-328">Kündigungsdatum (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-328">Termination date (required upon termination)</span></span>
- <span data-ttu-id="edbca-329">Kündigungsgrund (erforderlich bei Kündigung)</span><span class="sxs-lookup"><span data-stu-id="edbca-329">Termination reason (required upon termination)</span></span>

<span data-ttu-id="edbca-330">Die Schlüsseldaten eines Mitarbeiters werden abgeleitet, indem die folgenden Informationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="edbca-330">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="edbca-331">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="edbca-331">Human Resources</span></span>                | <span data-ttu-id="edbca-332">Dayforce</span><span class="sxs-lookup"><span data-stu-id="edbca-332">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edbca-333">Aktuellstes Einstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="edbca-333">Most recent hire date</span></span> | <span data-ttu-id="edbca-334">Beschäftigungsbeginn des Verlaufsdatensatzes zur aktuellen, nicht gekündigten Beschäftigung</span><span class="sxs-lookup"><span data-stu-id="edbca-334">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="edbca-335">Kündigungsdatum</span><span class="sxs-lookup"><span data-stu-id="edbca-335">Termination date</span></span>      | <span data-ttu-id="edbca-336">Kündigungsdatum des Verlaufsdatensatzes zur aktuellen, nicht gekündigten Beschäftigung</span><span class="sxs-lookup"><span data-stu-id="edbca-336">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="edbca-337">Eintrittstermin</span><span class="sxs-lookup"><span data-stu-id="edbca-337">Start date</span></span>            | <span data-ttu-id="edbca-338">Angepasstes Startdatum, Startdatum oder Beschäftigungsbeginn des Verlaufsdatensatzes zur aktuellen, nicht aktiven Beschäftigung</span><span class="sxs-lookup"><span data-stu-id="edbca-338">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="edbca-339">Ursprüngliches Einstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="edbca-339">Original hire date</span></span>    | <span data-ttu-id="edbca-340">Beschäftigungsbeginn des frühesten Beschäftigungsverlaufsdatensatzes</span><span class="sxs-lookup"><span data-stu-id="edbca-340">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="edbca-341">Vergütung</span><span class="sxs-lookup"><span data-stu-id="edbca-341">Compensation</span></span>

<span data-ttu-id="edbca-342">Ein fester Vergütungsplan muss der primären Position jedes Mitarbeiters während einer Beschäftigungsperiode zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="edbca-342">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="edbca-343">Diese Periode beginnt mit dem Datum, an dem der Mitarbeiter eingestellt wurde (oder dem Datum des Beschäftigungsbeginns), und setzt sich bis zur Kündigung fort.</span><span class="sxs-lookup"><span data-stu-id="edbca-343">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="edbca-344">Gültigkeitsdatum (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-344">Effective Date (required)</span></span>
- <span data-ttu-id="edbca-345">Ablaufdatum</span><span class="sxs-lookup"><span data-stu-id="edbca-345">Expiration date</span></span>
- <span data-ttu-id="edbca-346">Lohnsatz (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-346">Pay Rate (required)</span></span>
- <span data-ttu-id="edbca-347">Lohnsatzkonvertierungen (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-347">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="edbca-348">Jährliches Äquivalent (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-348">Annual equivalent (required)</span></span>
- <span data-ttu-id="edbca-349">Stündliches Äquivalent (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-349">Hourly equivalent (required)</span></span>

<span data-ttu-id="edbca-350">Wenn ein Mitarbeiter auf Stundenbasis mehrere Positionen hat, wird die feste Vergütung der primären Position in Dayforce als Basissatz/-gehalt auf Mitarbeiterebene importiert.</span><span class="sxs-lookup"><span data-stu-id="edbca-350">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="edbca-351">Für nicht-primäre Positionen wird der Stundensatz in der entsprechenden Position in Dayforce gespeichert.</span><span class="sxs-lookup"><span data-stu-id="edbca-351">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="edbca-352">Wenn ein Gehalt beziehender Mitarbeiter mehrere Positionen hat, wird der kumulative Stundensatz und das Jahresgehalt über alle aktiven Positionen hinweg abgeleitet und als Basissatz/-gehalt auf Arbeitnehmerebene verwendet.</span><span class="sxs-lookup"><span data-stu-id="edbca-352">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="edbca-353">Kennnummern</span><span class="sxs-lookup"><span data-stu-id="edbca-353">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="edbca-354">Sozialversicherungsbezeichner</span><span class="sxs-lookup"><span data-stu-id="edbca-354">Social Security identifier</span></span> 

<span data-ttu-id="edbca-355">Jeder Mitarbeiter muss einen primären Bezeichner haben.</span><span class="sxs-lookup"><span data-stu-id="edbca-355">Every employee must have one primary identifier.</span></span> <span data-ttu-id="edbca-356">Dieser Bezeichner muss vom Kennungstyp **P.Reg.Nr.** sein.</span><span class="sxs-lookup"><span data-stu-id="edbca-356">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="edbca-357">In Dayforce wird er automatisch als Sozialversicherungsbezeichner des Mitarbeiters abgeleitet, der für die Einstellung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="edbca-357">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="edbca-358">Primär (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-358">Primary (required)</span></span>
- <span data-ttu-id="edbca-359">Kennungstyp = „P.Reg.Nr.”</span><span class="sxs-lookup"><span data-stu-id="edbca-359">Identification Type = "SSN"</span></span>
- <span data-ttu-id="edbca-360">Ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="edbca-360">Issued Date</span></span>
- <span data-ttu-id="edbca-361">Ablaufdatum</span><span class="sxs-lookup"><span data-stu-id="edbca-361">Expiration Date</span></span>

<span data-ttu-id="edbca-362">Mitarbeiter können mehrere Kennungsnummern des Kennungstyps **P.Reg.Nr.** melden.</span><span class="sxs-lookup"><span data-stu-id="edbca-362">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="edbca-363">Jedoch wird nur der Datensatz, der als **Primär** markiert ist, in Dayforce integriert, unabhängig davon, ob die Nummer aktiv oder abgelaufen ist.</span><span class="sxs-lookup"><span data-stu-id="edbca-363">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="edbca-364">Bankkonten und Auszahlungen</span><span class="sxs-lookup"><span data-stu-id="edbca-364">Bank accounts and disbursements</span></span>

<span data-ttu-id="edbca-365">Gültige Bankkontoinformationen müssen für jeden Mitarbeiter eingegeben werden, der per Bankkontoüberweisungen bezahlt werden möchte.</span><span class="sxs-lookup"><span data-stu-id="edbca-365">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="edbca-366">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="edbca-366">Human Resources</span></span>                         | <span data-ttu-id="edbca-367">Dayforce</span><span class="sxs-lookup"><span data-stu-id="edbca-367">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edbca-368">Bankkontonummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-368">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="edbca-369">SWIFT-Code (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-369">SWIFT code (required)</span></span>          | <span data-ttu-id="edbca-370">Feld **Bankkennung** wird verwendet, wenn Lohn in Mexiko verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="edbca-370">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="edbca-371">Filialnummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-371">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="edbca-372">Bankkontotyp (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-372">Bank account type (required)</span></span>   | <span data-ttu-id="edbca-373">Feld **Kontotyp** wird verwendet, wenn Lohn in Mexiko verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="edbca-373">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="edbca-374">Unterstützte Werte umfassen **Wird geprüft** und **Lohn**.</span><span class="sxs-lookup"><span data-stu-id="edbca-374">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="edbca-375">Mitarbeiter, die per Bankkontoüberweisungen bezahlt werden möchten, müssen eine Verknüpfung zu einem Restbetrags-Bankkonto angeben, das sich unter einer juristischen Person befindet, deren primäre Adresse in Mexiko ist und das einem gültigen Bankkonto von einer mexikanischen Bank zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="edbca-375">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="edbca-376">Alle anderen Nicht-Restbetrags-Bankkonten werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="edbca-376">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="edbca-377">Adressdaten</span><span class="sxs-lookup"><span data-stu-id="edbca-377">Address information</span></span>

<span data-ttu-id="edbca-378">Jeder Mitarbeiter muss einen primären Standort haben.</span><span class="sxs-lookup"><span data-stu-id="edbca-378">Every employee must have one primary location.</span></span> <span data-ttu-id="edbca-379">In Dayforce wird dieser Standort verwendet, um den primären Wohnsitz des Mitarbeiters für Steuerzwecke zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="edbca-379">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="edbca-380">Primär (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-380">Primary (required)</span></span>
- <span data-ttu-id="edbca-381">Land/Region (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-381">Country/region (required)</span></span>
- <span data-ttu-id="edbca-382">Postleitzahl (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-382">Zip/postal code (required)</span></span>
- <span data-ttu-id="edbca-383">Straße (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-383">Street (required)</span></span>
- <span data-ttu-id="edbca-384">Hausnummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-384">Street Number (required)</span></span>
- <span data-ttu-id="edbca-385">Gebäudeergänzung</span><span class="sxs-lookup"><span data-stu-id="edbca-385">Building Complement</span></span>
- <span data-ttu-id="edbca-386">Ort (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-386">City (required)</span></span>
- <span data-ttu-id="edbca-387">Bundesland/Kanton (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-387">State (required)</span></span>
- <span data-ttu-id="edbca-388">Landkreis (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-388">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="edbca-389">Konfigurieren Ihrer Daten, um Vergütung in den USA und Kanada zu generieren</span><span class="sxs-lookup"><span data-stu-id="edbca-389">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="edbca-390">Wenn Sie Vergütung für Mitarbeiter in den USA und Kanada generieren, müssen die folgenden Elemente konfiguriert werden:</span><span class="sxs-lookup"><span data-stu-id="edbca-390">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="edbca-391">Abteilungen sind für Positionen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="edbca-391">Departments are required on positions.</span></span>
- <span data-ttu-id="edbca-392">Kostenstellen müssen als Finanzdimensionen festgelegt werden und müssen das erste Element in der standardmäßigen Finanzdimensions-Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="edbca-392">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="edbca-393">Sie können Human Resources so konfigurieren, dass Positionen eine Abteilung angeben müssen.</span><span class="sxs-lookup"><span data-stu-id="edbca-393">You can configure Human Resources to require that Positions specify a Department.</span></span> <span data-ttu-id="edbca-394">Dazu wechseln Sie zu **Freigegebene Positionen der Personalverwaltung > Positionen > Abteilungen zu Positionen anfordern**.</span><span class="sxs-lookup"><span data-stu-id="edbca-394">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="edbca-395">Es wird empfohlen, dass diese Einstellungen für die Integration erzwungen wird.</span><span class="sxs-lookup"><span data-stu-id="edbca-395">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="edbca-396">Stellentypen</span><span class="sxs-lookup"><span data-stu-id="edbca-396">Job types</span></span>

<span data-ttu-id="edbca-397">Stellentypen werden verwendet, um ähnliche Stellen in Kategorien zu gruppieren.</span><span class="sxs-lookup"><span data-stu-id="edbca-397">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="edbca-398">Stellentypen sind erforderlich, damit Lohn in den USA und Kanada zu bearbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="edbca-398">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="edbca-399">Beispiele für Stellentypen umfassen Voll- und Teilzeit oder festes Gehalt und Stundenlohn.</span><span class="sxs-lookup"><span data-stu-id="edbca-399">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="edbca-400">Stellentypen werden Dayforce als Lohnarten zugeordnet, die angeben, ob ein Mitarbeiter auf Stundenbasis bezahlt wird oder ein festes Gehalt bezieht.</span><span class="sxs-lookup"><span data-stu-id="edbca-400">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="edbca-401">Folgende Stellentypen und Beschreibungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="edbca-401">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="edbca-402">Stellentyp</span><span class="sxs-lookup"><span data-stu-id="edbca-402">Job type</span></span>   | <span data-ttu-id="edbca-403">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="edbca-403">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="edbca-404">Stündlich</span><span class="sxs-lookup"><span data-stu-id="edbca-404">Hourly</span></span>     | <span data-ttu-id="edbca-405">Stündlich</span><span class="sxs-lookup"><span data-stu-id="edbca-405">Hourly</span></span>      |
| <span data-ttu-id="edbca-406">Fest angestellt</span><span class="sxs-lookup"><span data-stu-id="edbca-406">Salaried</span></span>   | <span data-ttu-id="edbca-407">Fest angestellt</span><span class="sxs-lookup"><span data-stu-id="edbca-407">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="edbca-408">Positionstypen</span><span class="sxs-lookup"><span data-stu-id="edbca-408">Position types</span></span> 

<span data-ttu-id="edbca-409">Sie verwenden Positionstypen, um zu beschreiben, ob die Position Vollzeit, Teilzeit oder etwas anderes ist.</span><span class="sxs-lookup"><span data-stu-id="edbca-409">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="edbca-410">Positionstypen werden Dayforce als Lohnklassen zugeordnet, die angeben, ob ein Mitarbeiter in Vollzeit oder Teilzeit arbeitet.</span><span class="sxs-lookup"><span data-stu-id="edbca-410">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="edbca-411">Folgende Positionstypen und Beschreibungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="edbca-411">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="edbca-412">Positionstyp</span><span class="sxs-lookup"><span data-stu-id="edbca-412">Position type</span></span>   | <span data-ttu-id="edbca-413">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="edbca-413">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="edbca-414">Vollzeit</span><span class="sxs-lookup"><span data-stu-id="edbca-414">Full-time</span></span>       | <span data-ttu-id="edbca-415">Vollzeitmitarbeiter</span><span class="sxs-lookup"><span data-stu-id="edbca-415">Full time employee</span></span> |
| <span data-ttu-id="edbca-416">Teilzeit</span><span class="sxs-lookup"><span data-stu-id="edbca-416">Part-time</span></span>       | <span data-ttu-id="edbca-417">Teilzeitmitarbeiter</span><span class="sxs-lookup"><span data-stu-id="edbca-417">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="edbca-418">Ursachencodes</span><span class="sxs-lookup"><span data-stu-id="edbca-418">Reason codes</span></span>

<span data-ttu-id="edbca-419">Ursachencodes enthalten Informationen zum Status eines Mitarbeiters.</span><span class="sxs-lookup"><span data-stu-id="edbca-419">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="edbca-420">Ursachencodes werden Dayforce als Statusgründe zugeordnet, die den Grund für Änderungen bei der Position eines Mitarbeiters oder dem Beschäftigungsstatus angeben.</span><span class="sxs-lookup"><span data-stu-id="edbca-420">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="edbca-421">Folgende Ursachencodes und Beschreibungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="edbca-421">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="edbca-422">Ursachencode</span><span class="sxs-lookup"><span data-stu-id="edbca-422">Reason code</span></span>    | <span data-ttu-id="edbca-423">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="edbca-423">Description</span></span>      | <span data-ttu-id="edbca-424">Zutreffende Szenarios</span><span class="sxs-lookup"><span data-stu-id="edbca-424">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="edbca-425">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="edbca-425">RESIGNATION</span></span>    | <span data-ttu-id="edbca-426">Kündigung durch Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="edbca-426">Resignation</span></span>      | <span data-ttu-id="edbca-427">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="edbca-427">Terminate worker</span></span>     |
| <span data-ttu-id="edbca-428">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="edbca-428">TERMINATION</span></span>    | <span data-ttu-id="edbca-429">Beendigung</span><span class="sxs-lookup"><span data-stu-id="edbca-429">Termination</span></span>      | <span data-ttu-id="edbca-430">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="edbca-430">Terminate worker</span></span>     |
| <span data-ttu-id="edbca-431">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="edbca-431">RETIREMENT</span></span>     | <span data-ttu-id="edbca-432">Ruhestand</span><span class="sxs-lookup"><span data-stu-id="edbca-432">Retirement</span></span>       | <span data-ttu-id="edbca-433">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="edbca-433">Terminate worker</span></span>     |
| <span data-ttu-id="edbca-434">OTHER</span><span class="sxs-lookup"><span data-stu-id="edbca-434">OTHER</span></span>          | <span data-ttu-id="edbca-435">Andere Gründe</span><span class="sxs-lookup"><span data-stu-id="edbca-435">Other Reasons</span></span>    | <span data-ttu-id="edbca-436">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="edbca-436">Terminate worker</span></span>     |
| <span data-ttu-id="edbca-437">DEATH</span><span class="sxs-lookup"><span data-stu-id="edbca-437">DEATH</span></span>          | <span data-ttu-id="edbca-438">Tod</span><span class="sxs-lookup"><span data-stu-id="edbca-438">Death</span></span>            | <span data-ttu-id="edbca-439">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="edbca-439">Terminate worker</span></span>     |
| <span data-ttu-id="edbca-440">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="edbca-440">LEAVEOFABSENCE</span></span> | <span data-ttu-id="edbca-441">Beurlaubung</span><span class="sxs-lookup"><span data-stu-id="edbca-441">Leave of Absence</span></span> | <span data-ttu-id="edbca-442">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="edbca-442">Terminate worker</span></span>     |
| <span data-ttu-id="edbca-443">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="edbca-443">CONTRACTEND</span></span>    | <span data-ttu-id="edbca-444">Vertragsende</span><span class="sxs-lookup"><span data-stu-id="edbca-444">End of Contract</span></span>  | <span data-ttu-id="edbca-445">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="edbca-445">Terminate worker</span></span>     |
| <span data-ttu-id="edbca-446">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="edbca-446">SALARYCHANGE</span></span>   | <span data-ttu-id="edbca-447">Gehaltsänderung</span><span class="sxs-lookup"><span data-stu-id="edbca-447">Change of Salary</span></span> | <span data-ttu-id="edbca-448">Vergütung</span><span class="sxs-lookup"><span data-stu-id="edbca-448">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="edbca-449">Familienstand</span><span class="sxs-lookup"><span data-stu-id="edbca-449">Marital status</span></span>

<span data-ttu-id="edbca-450">Familienstandwerte werden Dayforce zugeordnet und werden – je nach Bedarf – in die akzeptierten Werte bei der Integration übersetzt.</span><span class="sxs-lookup"><span data-stu-id="edbca-450">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="edbca-451">Die folgende Tabelle zeigt, wie Familienstandwerte Dayforce zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="edbca-451">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="edbca-452">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="edbca-452">Human Resources</span></span>                 | <span data-ttu-id="edbca-453">Dayforce</span><span class="sxs-lookup"><span data-stu-id="edbca-453">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="edbca-454">Verheiratet</span><span class="sxs-lookup"><span data-stu-id="edbca-454">Married</span></span>                | <span data-ttu-id="edbca-455">Verheiratet</span><span class="sxs-lookup"><span data-stu-id="edbca-455">Married</span></span>              |
| <span data-ttu-id="edbca-456">Ledig</span><span class="sxs-lookup"><span data-stu-id="edbca-456">Single</span></span>                 | <span data-ttu-id="edbca-457">Ledig</span><span class="sxs-lookup"><span data-stu-id="edbca-457">Single</span></span>               |
| <span data-ttu-id="edbca-458">Verwitwet</span><span class="sxs-lookup"><span data-stu-id="edbca-458">Widowed</span></span>                | <span data-ttu-id="edbca-459">Verwitwet</span><span class="sxs-lookup"><span data-stu-id="edbca-459">Widowed</span></span>              |
| <span data-ttu-id="edbca-460">Geschieden</span><span class="sxs-lookup"><span data-stu-id="edbca-460">Divorced</span></span>               | <span data-ttu-id="edbca-461">Geschieden</span><span class="sxs-lookup"><span data-stu-id="edbca-461">Divorced</span></span>             |
| <span data-ttu-id="edbca-462">Eingetragene Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="edbca-462">Registered Partnership</span></span> | <span data-ttu-id="edbca-463">Inländische Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="edbca-463">Domestic Partnership</span></span> |
| <span data-ttu-id="edbca-464">None</span><span class="sxs-lookup"><span data-stu-id="edbca-464">None</span></span>                   | <span data-ttu-id="edbca-465">None</span><span class="sxs-lookup"><span data-stu-id="edbca-465">None</span></span>                 |
| <span data-ttu-id="edbca-466">Freie Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="edbca-466">Cohabiting</span></span>             | <span data-ttu-id="edbca-467">Freie Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="edbca-467">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="edbca-468">Geschlecht</span><span class="sxs-lookup"><span data-stu-id="edbca-468">Gender</span></span>

<span data-ttu-id="edbca-469">Geschlechtsbezeichnungen werden Dayforce zugeordnet und werden – je nach Bedarf – in die akzeptierten Werte bei der Integration übersetzt.</span><span class="sxs-lookup"><span data-stu-id="edbca-469">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="edbca-470">Die folgende Tabelle zeigt, wie Geschlechtsbezeichnungen Dayforce zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="edbca-470">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="edbca-471">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="edbca-471">Human Resources</span></span>       | <span data-ttu-id="edbca-472">Dayforce</span><span class="sxs-lookup"><span data-stu-id="edbca-472">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="edbca-473">Männl.</span><span class="sxs-lookup"><span data-stu-id="edbca-473">Male</span></span>         | <span data-ttu-id="edbca-474">Männl.</span><span class="sxs-lookup"><span data-stu-id="edbca-474">Male</span></span>            |
| <span data-ttu-id="edbca-475">Weibl.</span><span class="sxs-lookup"><span data-stu-id="edbca-475">Female</span></span>       | <span data-ttu-id="edbca-476">Weibl.</span><span class="sxs-lookup"><span data-stu-id="edbca-476">Female</span></span>          |
| <span data-ttu-id="edbca-477">Nicht spezifisch</span><span class="sxs-lookup"><span data-stu-id="edbca-477">Non-specific</span></span> | <span data-ttu-id="edbca-478">*Nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="edbca-478">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="edbca-479">Einkommenscodes</span><span class="sxs-lookup"><span data-stu-id="edbca-479">Earning codes</span></span>

<span data-ttu-id="edbca-480">Einkommenscodes bestimmen jeden Typ von Einkünften eindeutig, die Arbeitskräfte erhalten</span><span class="sxs-lookup"><span data-stu-id="edbca-480">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="edbca-481">Die Codes decken verschiedene Parameter ab, die sich auf Einkünfte beziehen, wie beispielsweise Buchhaltungsvorschriften, Steuergesetze, Berichterstellungsanforderungen und Bruttoausgleichsfähigkeit.</span><span class="sxs-lookup"><span data-stu-id="edbca-481">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="edbca-482">Wenn eine nicht unterstützte Häufigkeit verwendet wird, wird die Häufigkeit **Jeder Lohn** standardmäßig für die Berechnung verwendet.</span><span class="sxs-lookup"><span data-stu-id="edbca-482">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="edbca-483">Unterstützte Häufigkeiten</span><span class="sxs-lookup"><span data-stu-id="edbca-483">Supported frequencies</span></span>

- <span data-ttu-id="edbca-484">Alle</span><span class="sxs-lookup"><span data-stu-id="edbca-484">All</span></span>
- <span data-ttu-id="edbca-485">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="edbca-485">EVERYPAY</span></span>
- <span data-ttu-id="edbca-486">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="edbca-486">EACHPAYPERIOD</span></span>
- <span data-ttu-id="edbca-487">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="edbca-487">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="edbca-488">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="edbca-488">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="edbca-489">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="edbca-489">1OFMTH</span></span>
- <span data-ttu-id="edbca-490">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="edbca-490">LASTOFMTH</span></span>
- <span data-ttu-id="edbca-491">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="edbca-491">2OFMTH</span></span>
- <span data-ttu-id="edbca-492">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="edbca-492">3OFMTH</span></span>
- <span data-ttu-id="edbca-493">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="edbca-493">4OFMTH</span></span>
- <span data-ttu-id="edbca-494">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="edbca-494">5OFMTH</span></span>
- <span data-ttu-id="edbca-495">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="edbca-495">1N2OFMTH</span></span>
- <span data-ttu-id="edbca-496">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="edbca-496">3N4OFMTH</span></span>
- <span data-ttu-id="edbca-497">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="edbca-497">1N3OFMTH</span></span>
- <span data-ttu-id="edbca-498">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="edbca-498">1N4OFMTH</span></span>
- <span data-ttu-id="edbca-499">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="edbca-499">2N3OFMTH</span></span>
- <span data-ttu-id="edbca-500">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="edbca-500">2N4OFMTH</span></span>
- <span data-ttu-id="edbca-501">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="edbca-501">1N2N3OFMTH</span></span>
- <span data-ttu-id="edbca-502">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="edbca-502">1N2N4OFMTH</span></span>
- <span data-ttu-id="edbca-503">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="edbca-503">1N3N4OFMTH</span></span>
- <span data-ttu-id="edbca-504">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="edbca-504">2N3N4OFMTH</span></span>
- <span data-ttu-id="edbca-505">1N2N3N4OFMTH – 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="edbca-505">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="edbca-506">2N3N4N5OFMth – 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="edbca-506">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="edbca-507">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="edbca-507">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="edbca-508">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="edbca-508">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="edbca-509">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="edbca-509">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="edbca-510">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="edbca-510">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="edbca-511">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="edbca-511">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="edbca-512">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="edbca-512">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="edbca-513">Adressen</span><span class="sxs-lookup"><span data-stu-id="edbca-513">Addresses</span></span>

<span data-ttu-id="edbca-514">Die Kennung bestimmter Codes für Land oder Region, Bundesland/Kanton oder Landkreis (Gemeinde) erfordert spezifische Formate, die Dayforce und Anbieter innerhalb des Landes/innerhalb der Region erkennen können.</span><span class="sxs-lookup"><span data-stu-id="edbca-514">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="edbca-515">Obwohl das Format für Orte flexibel ist, muss jeder Ort einem Bundesland zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="edbca-515">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="edbca-516">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="edbca-516">Human Resources</span></span>          | <span data-ttu-id="edbca-517">Dayforce</span><span class="sxs-lookup"><span data-stu-id="edbca-517">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="edbca-518">Land/Region</span><span class="sxs-lookup"><span data-stu-id="edbca-518">Country/Region</span></span>  | <span data-ttu-id="edbca-519">Ländercode</span><span class="sxs-lookup"><span data-stu-id="edbca-519">Country Code</span></span>          |
| <span data-ttu-id="edbca-520">Postleitzahl</span><span class="sxs-lookup"><span data-stu-id="edbca-520">Zip/Postal Code</span></span> | <span data-ttu-id="edbca-521">PLZ</span><span class="sxs-lookup"><span data-stu-id="edbca-521">Postal Code</span></span>           |
| <span data-ttu-id="edbca-522">Zustand</span><span class="sxs-lookup"><span data-stu-id="edbca-522">State</span></span>           | <span data-ttu-id="edbca-523">Bundeslandcode</span><span class="sxs-lookup"><span data-stu-id="edbca-523">State Code</span></span>            |
| <span data-ttu-id="edbca-524">Stadt</span><span class="sxs-lookup"><span data-stu-id="edbca-524">City</span></span>            | <span data-ttu-id="edbca-525">Stadt</span><span class="sxs-lookup"><span data-stu-id="edbca-525">City</span></span>                  |
| <span data-ttu-id="edbca-526">Verwaltungsbezirk</span><span class="sxs-lookup"><span data-stu-id="edbca-526">County</span></span>          | <span data-ttu-id="edbca-527">Landkreis (Gemeinde)</span><span class="sxs-lookup"><span data-stu-id="edbca-527">County (Municipality)</span></span> |
| <span data-ttu-id="edbca-528">Straße</span><span class="sxs-lookup"><span data-stu-id="edbca-528">Street</span></span>          | <span data-ttu-id="edbca-529">Adresszeile 1</span><span class="sxs-lookup"><span data-stu-id="edbca-529">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="edbca-530">Steuerregionen</span><span class="sxs-lookup"><span data-stu-id="edbca-530">Tax regions</span></span>

<span data-ttu-id="edbca-531">Steuerregionen werden verwendet, um die entsprechende Steuer festzulegen, die bei der Lohngenerierung angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="edbca-531">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="edbca-532">Steuerregionen werden Dayforce als Standortadressen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="edbca-532">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="edbca-533">Die Standardsteuerregion muss der aktiven Position der Arbeitskraft zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="edbca-533">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="edbca-534">Steuerregion (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-534">Tax region (required)</span></span>
- <span data-ttu-id="edbca-535">Land/Region (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-535">Country/Region (required)</span></span>
- <span data-ttu-id="edbca-536">Bundesland/Kanton (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-536">State (required)</span></span>
- <span data-ttu-id="edbca-537">Verwaltungsbezirk</span><span class="sxs-lookup"><span data-stu-id="edbca-537">County</span></span> 
- <span data-ttu-id="edbca-538">Ort (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="edbca-538">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="edbca-539">Konfigurieren Ihrer Daten, um Lohn in Mexiko zu generieren</span><span class="sxs-lookup"><span data-stu-id="edbca-539">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="edbca-540">Wenn Sie Vergütung für Mitarbeiter in Mexiko generieren, müssen die folgenden Elemente konfiguriert werden:</span><span class="sxs-lookup"><span data-stu-id="edbca-540">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="edbca-541">Abteilungen sind für Positionen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="edbca-541">Departments are required on positions.</span></span>
- <span data-ttu-id="edbca-542">Kostenstellen müssen als Finanzdimensionen festgelegt werden und müssen das erste Element in der standardmäßigen Finanzdimensions-Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="edbca-542">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="edbca-543">Stellentypen</span><span class="sxs-lookup"><span data-stu-id="edbca-543">Job types</span></span>

<span data-ttu-id="edbca-544">Stellentypen werden verwendet, um ähnliche Stellen in Kategorien zu gruppieren.</span><span class="sxs-lookup"><span data-stu-id="edbca-544">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="edbca-545">Stellentypen sind erforderlich, um Lohn in Mexiko zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="edbca-545">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="edbca-546">Beispiele für Stellentypen umfassen Voll- und Teilzeit oder festes Gehalt und Stundenlohn.</span><span class="sxs-lookup"><span data-stu-id="edbca-546">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="edbca-547">Stellentypen werden Dayforce als Lohnarten zugeordnet, die angeben, ob ein Mitarbeiter auf Stundenbasis bezahlt wird oder ein festes Gehalt bezieht.</span><span class="sxs-lookup"><span data-stu-id="edbca-547">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="edbca-548">Folgende Stellentypen und Beschreibungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="edbca-548">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="edbca-549">Stellentyp</span><span class="sxs-lookup"><span data-stu-id="edbca-549">Job type</span></span>   | <span data-ttu-id="edbca-550">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="edbca-550">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="edbca-551">Stündlich</span><span class="sxs-lookup"><span data-stu-id="edbca-551">Hourly</span></span>     | <span data-ttu-id="edbca-552">MX – Stundenbasis</span><span class="sxs-lookup"><span data-stu-id="edbca-552">MX Hourly</span></span>   |
| <span data-ttu-id="edbca-553">Fest angestellt</span><span class="sxs-lookup"><span data-stu-id="edbca-553">Salaried</span></span>   | <span data-ttu-id="edbca-554">MX – Fest angestellt</span><span class="sxs-lookup"><span data-stu-id="edbca-554">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="edbca-555">Positionstypen</span><span class="sxs-lookup"><span data-stu-id="edbca-555">Position types</span></span> 

<span data-ttu-id="edbca-556">Sie verwenden Positionstypen, um zu beschreiben, ob die Position Vollzeit, Teilzeit oder etwas anderes ist.</span><span class="sxs-lookup"><span data-stu-id="edbca-556">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="edbca-557">Positionstypen werden Dayforce als Lohnklassen zugeordnet, die angeben, ob ein Mitarbeiter in Vollzeit oder Teilzeit arbeitet.</span><span class="sxs-lookup"><span data-stu-id="edbca-557">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="edbca-558">Folgende Positionstypen und Beschreibungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="edbca-558">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="edbca-559">Positionstyp</span><span class="sxs-lookup"><span data-stu-id="edbca-559">Position type</span></span>   | <span data-ttu-id="edbca-560">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="edbca-560">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="edbca-561">Vollzeit</span><span class="sxs-lookup"><span data-stu-id="edbca-561">Full-time</span></span>       | <span data-ttu-id="edbca-562">Vollzeitmitarbeiter</span><span class="sxs-lookup"><span data-stu-id="edbca-562">Full time employee</span></span> |
| <span data-ttu-id="edbca-563">Teilzeit</span><span class="sxs-lookup"><span data-stu-id="edbca-563">Part-time</span></span>       | <span data-ttu-id="edbca-564">Teilzeitmitarbeiter</span><span class="sxs-lookup"><span data-stu-id="edbca-564">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="edbca-565">Ursachencodes</span><span class="sxs-lookup"><span data-stu-id="edbca-565">Reason codes</span></span>

<span data-ttu-id="edbca-566">Ursachencodes enthalten Informationen zum Status eines Mitarbeiters.</span><span class="sxs-lookup"><span data-stu-id="edbca-566">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="edbca-567">Ursachencodes werden Dayforce als Statusgründe zugeordnet, die den Grund für Änderungen bei der Position eines Mitarbeiters oder dem Beschäftigungsstatus angeben.</span><span class="sxs-lookup"><span data-stu-id="edbca-567">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="edbca-568">Folgende Ursachencodes und Beschreibungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="edbca-568">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="edbca-569">Ursachencode</span><span class="sxs-lookup"><span data-stu-id="edbca-569">Reason code</span></span>            | <span data-ttu-id="edbca-570">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="edbca-570">Description</span></span>                    | <span data-ttu-id="edbca-571">Zutreffende Szenarios</span><span class="sxs-lookup"><span data-stu-id="edbca-571">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="edbca-572">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="edbca-572">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="edbca-573">Abgang vor erster Lohnzahlung</span><span class="sxs-lookup"><span data-stu-id="edbca-573">Departure before first payroll</span></span> | <span data-ttu-id="edbca-574">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="edbca-574">Terminate worker</span></span>     |
| <span data-ttu-id="edbca-575">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="edbca-575">RESIGNATION</span></span>            | <span data-ttu-id="edbca-576">Kündigung durch Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="edbca-576">Resignation</span></span>                    | <span data-ttu-id="edbca-577">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="edbca-577">Terminate worker</span></span>     |
| <span data-ttu-id="edbca-578">PENSION</span><span class="sxs-lookup"><span data-stu-id="edbca-578">PENSION</span></span>                | <span data-ttu-id="edbca-579">Rente</span><span class="sxs-lookup"><span data-stu-id="edbca-579">Pension</span></span>                        | <span data-ttu-id="edbca-580">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="edbca-580">Terminate worker</span></span>     |
| <span data-ttu-id="edbca-581">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="edbca-581">TERMINATION</span></span>            | <span data-ttu-id="edbca-582">Beendigung</span><span class="sxs-lookup"><span data-stu-id="edbca-582">Termination</span></span>                    | <span data-ttu-id="edbca-583">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="edbca-583">Terminate worker</span></span>     |
| <span data-ttu-id="edbca-584">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="edbca-584">RETIREMENT</span></span>             | <span data-ttu-id="edbca-585">Ruhestand</span><span class="sxs-lookup"><span data-stu-id="edbca-585">Retirement</span></span>                     | <span data-ttu-id="edbca-586">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="edbca-586">Terminate worker</span></span>     |
| <span data-ttu-id="edbca-587">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="edbca-587">ABSENTEE</span></span>               | <span data-ttu-id="edbca-588">Abwesende Person</span><span class="sxs-lookup"><span data-stu-id="edbca-588">Absentee</span></span>                       | <span data-ttu-id="edbca-589">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="edbca-589">Terminate worker</span></span>     |
| <span data-ttu-id="edbca-590">OTHER</span><span class="sxs-lookup"><span data-stu-id="edbca-590">OTHER</span></span>                  | <span data-ttu-id="edbca-591">Andere Gründe</span><span class="sxs-lookup"><span data-stu-id="edbca-591">Other Reasons</span></span>                  | <span data-ttu-id="edbca-592">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="edbca-592">Terminate worker</span></span>     |
| <span data-ttu-id="edbca-593">CLOSURE</span><span class="sxs-lookup"><span data-stu-id="edbca-593">CLOSURE</span></span>                | <span data-ttu-id="edbca-594">Betriebsferien</span><span class="sxs-lookup"><span data-stu-id="edbca-594">Business Closure</span></span>               | <span data-ttu-id="edbca-595">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="edbca-595">Terminate worker</span></span>     |
| <span data-ttu-id="edbca-596">DEATH</span><span class="sxs-lookup"><span data-stu-id="edbca-596">DEATH</span></span>                  | <span data-ttu-id="edbca-597">Tod</span><span class="sxs-lookup"><span data-stu-id="edbca-597">Death</span></span>                          | <span data-ttu-id="edbca-598">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="edbca-598">Terminate worker</span></span>     |
| <span data-ttu-id="edbca-599">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="edbca-599">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="edbca-600">Beurlaubung</span><span class="sxs-lookup"><span data-stu-id="edbca-600">Leave of Absence</span></span>               | <span data-ttu-id="edbca-601">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="edbca-601">Terminate worker</span></span>     |
| <span data-ttu-id="edbca-602">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="edbca-602">CONTRACTEND</span></span>            | <span data-ttu-id="edbca-603">Vertragsende</span><span class="sxs-lookup"><span data-stu-id="edbca-603">End of Contract</span></span>                | <span data-ttu-id="edbca-604">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="edbca-604">Terminate worker</span></span>     |
| <span data-ttu-id="edbca-605">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="edbca-605">SALARYCHANGE</span></span>           | <span data-ttu-id="edbca-606">Gehaltsänderung</span><span class="sxs-lookup"><span data-stu-id="edbca-606">Change of Salary</span></span>               | <span data-ttu-id="edbca-607">Vergütung</span><span class="sxs-lookup"><span data-stu-id="edbca-607">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="edbca-608">Einstellungsbedingungen</span><span class="sxs-lookup"><span data-stu-id="edbca-608">Terms of employment</span></span>

<span data-ttu-id="edbca-609">Beschäftigungsbedingungen werden verwendet, um Kategorien von Beschäftigungsbedingungen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="edbca-609">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="edbca-610">Die Bedingungen werden Dayforce als Beschäftigungsindikatorwerte zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="edbca-610">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="edbca-611">Die folgenden Bedingungen für Beschäftigung und Beschreibungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="edbca-611">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="edbca-612">Einstellungsbedingungen</span><span class="sxs-lookup"><span data-stu-id="edbca-612">Terms of employment</span></span>   | <span data-ttu-id="edbca-613">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="edbca-613">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="edbca-614">Regelmäßig</span><span class="sxs-lookup"><span data-stu-id="edbca-614">Regular</span></span>               | <span data-ttu-id="edbca-615">Regelmäßig</span><span class="sxs-lookup"><span data-stu-id="edbca-615">Regular</span></span>     |
| <span data-ttu-id="edbca-616">Direkt</span><span class="sxs-lookup"><span data-stu-id="edbca-616">Direct</span></span>                | <span data-ttu-id="edbca-617">Direkt</span><span class="sxs-lookup"><span data-stu-id="edbca-617">Direct</span></span>      |
| <span data-ttu-id="edbca-618">Praktikum</span><span class="sxs-lookup"><span data-stu-id="edbca-618">Internship</span></span>            | <span data-ttu-id="edbca-619">Praktikum</span><span class="sxs-lookup"><span data-stu-id="edbca-619">Internship</span></span>  |
| <span data-ttu-id="edbca-620">Unbefristet</span><span class="sxs-lookup"><span data-stu-id="edbca-620">Permanent</span></span>             | <span data-ttu-id="edbca-621">Unbefristet</span><span class="sxs-lookup"><span data-stu-id="edbca-621">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="edbca-622">Familienstand</span><span class="sxs-lookup"><span data-stu-id="edbca-622">Marital status</span></span>

<span data-ttu-id="edbca-623">Familienstandwerte werden Dayforce zugeordnet und werden – je nach Bedarf – in die akzeptierten Werte bei der Integration übersetzt.</span><span class="sxs-lookup"><span data-stu-id="edbca-623">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="edbca-624">Die folgende Tabelle zeigt, wie Familienstandwerte Dayforce zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="edbca-624">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="edbca-625">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="edbca-625">Human Resources</span></span>                 | <span data-ttu-id="edbca-626">Dayforce</span><span class="sxs-lookup"><span data-stu-id="edbca-626">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="edbca-627">Verheiratet</span><span class="sxs-lookup"><span data-stu-id="edbca-627">Married</span></span>                | <span data-ttu-id="edbca-628">Verheiratet</span><span class="sxs-lookup"><span data-stu-id="edbca-628">Married</span></span>                   |
| <span data-ttu-id="edbca-629">Ledig</span><span class="sxs-lookup"><span data-stu-id="edbca-629">Single</span></span>                 | <span data-ttu-id="edbca-630">Ledig</span><span class="sxs-lookup"><span data-stu-id="edbca-630">Single</span></span>                    |
| <span data-ttu-id="edbca-631">Verwitwet</span><span class="sxs-lookup"><span data-stu-id="edbca-631">Widowed</span></span>                | <span data-ttu-id="edbca-632">Verwitwet</span><span class="sxs-lookup"><span data-stu-id="edbca-632">Widowed</span></span>                   |
| <span data-ttu-id="edbca-633">Geschieden</span><span class="sxs-lookup"><span data-stu-id="edbca-633">Divorced</span></span>               | <span data-ttu-id="edbca-634">Geschieden</span><span class="sxs-lookup"><span data-stu-id="edbca-634">Divorced</span></span>                  |
| <span data-ttu-id="edbca-635">Eingetragene Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="edbca-635">Registered Partnership</span></span> | <span data-ttu-id="edbca-636">Inländische Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="edbca-636">Domestic Partnership</span></span>      |
| <span data-ttu-id="edbca-637">None</span><span class="sxs-lookup"><span data-stu-id="edbca-637">None</span></span>                   | <span data-ttu-id="edbca-638">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="edbca-638">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="edbca-639">Freie Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="edbca-639">Cohabiting</span></span>             | <span data-ttu-id="edbca-640">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="edbca-640">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="edbca-641">Geschlecht</span><span class="sxs-lookup"><span data-stu-id="edbca-641">Gender</span></span>

<span data-ttu-id="edbca-642">Geschlechtsbezeichnungen werden Dayforce zugeordnet und werden – je nach Bedarf – in die akzeptierten Werte bei der Integration übersetzt.</span><span class="sxs-lookup"><span data-stu-id="edbca-642">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="edbca-643">Die folgende Tabelle zeigt, wie Geschlechtsbezeichnungen Dayforce zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="edbca-643">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="edbca-644">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="edbca-644">Human Resources</span></span>       | <span data-ttu-id="edbca-645">Dayforce</span><span class="sxs-lookup"><span data-stu-id="edbca-645">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="edbca-646">Männl.</span><span class="sxs-lookup"><span data-stu-id="edbca-646">Male</span></span>         | <span data-ttu-id="edbca-647">Männl.</span><span class="sxs-lookup"><span data-stu-id="edbca-647">Male</span></span>                      |
| <span data-ttu-id="edbca-648">Weibl.</span><span class="sxs-lookup"><span data-stu-id="edbca-648">Female</span></span>       | <span data-ttu-id="edbca-649">Weibl.</span><span class="sxs-lookup"><span data-stu-id="edbca-649">Female</span></span>                    |
| <span data-ttu-id="edbca-650">Nicht spezifisch</span><span class="sxs-lookup"><span data-stu-id="edbca-650">Non-specific</span></span> | <span data-ttu-id="edbca-651">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="edbca-651">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="edbca-652">Zahlungsweise</span><span class="sxs-lookup"><span data-stu-id="edbca-652">Payment method</span></span>

<span data-ttu-id="edbca-653">Zahlungsmethoden geben dem Mitarbeiter und dem Unternehmen die Möglichkeit zu beschreiben, wie Mitarbeiter bezahlt werden.</span><span class="sxs-lookup"><span data-stu-id="edbca-653">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="edbca-654">Zahlungsmethoden werden Dayforce zugeordnet und werden – je nach Bedarf – in die akzeptierten Werte bei der Integration übersetzt.</span><span class="sxs-lookup"><span data-stu-id="edbca-654">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="edbca-655">Die folgende Tabelle zeigt, wie Zahlungsmethoden Dayforce zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="edbca-655">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="edbca-656">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="edbca-656">Human Resources</span></span>             | <span data-ttu-id="edbca-657">Dayforce</span><span class="sxs-lookup"><span data-stu-id="edbca-657">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="edbca-658">Bargeld</span><span class="sxs-lookup"><span data-stu-id="edbca-658">Cash</span></span>               | <span data-ttu-id="edbca-659">Bargeld</span><span class="sxs-lookup"><span data-stu-id="edbca-659">Cash</span></span>                      |
| <span data-ttu-id="edbca-660">Elektronische Zahlung</span><span class="sxs-lookup"><span data-stu-id="edbca-660">Electronic Payment</span></span> | <span data-ttu-id="edbca-661">Übertragen</span><span class="sxs-lookup"><span data-stu-id="edbca-661">Transfer</span></span>                  |
| <span data-ttu-id="edbca-662">Prüfen</span><span class="sxs-lookup"><span data-stu-id="edbca-662">Check</span></span>              | <span data-ttu-id="edbca-663">Scheck</span><span class="sxs-lookup"><span data-stu-id="edbca-663">Cheque</span></span>                    |
| <span data-ttu-id="edbca-664">Bankwechsel</span><span class="sxs-lookup"><span data-stu-id="edbca-664">Bank Draft</span></span>         | <span data-ttu-id="edbca-665">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="edbca-665">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="edbca-666">Sonstige</span><span class="sxs-lookup"><span data-stu-id="edbca-666">Other</span></span>              | <span data-ttu-id="edbca-667">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="edbca-667">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="edbca-668">Bankkontotyp</span><span class="sxs-lookup"><span data-stu-id="edbca-668">Bank account type</span></span>

<span data-ttu-id="edbca-669">Bankkontotypen werden für elektronische Zahlungen an Mitarbeiter verwendet.</span><span class="sxs-lookup"><span data-stu-id="edbca-669">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="edbca-670">Bankkontotypen werden Dayforce als Übergweisungskontoinformationen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="edbca-670">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="edbca-671">Die Bankkontotypen werden bei Bedarf zu den akzeptierten Werte nach der Integration übersetzt.</span><span class="sxs-lookup"><span data-stu-id="edbca-671">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="edbca-672">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="edbca-672">Human Resources</span></span>            | <span data-ttu-id="edbca-673">Dayforce</span><span class="sxs-lookup"><span data-stu-id="edbca-673">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="edbca-674">Girokonto</span><span class="sxs-lookup"><span data-stu-id="edbca-674">Checking Account</span></span>  | <span data-ttu-id="edbca-675">Girokonto</span><span class="sxs-lookup"><span data-stu-id="edbca-675">CheckingAccount</span></span>           |
| <span data-ttu-id="edbca-676">Lohnkonto</span><span class="sxs-lookup"><span data-stu-id="edbca-676">Payroll Account</span></span>   | <span data-ttu-id="edbca-677">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="edbca-677">PayrollAccount</span></span>            |
| <span data-ttu-id="edbca-678">Sparkonto</span><span class="sxs-lookup"><span data-stu-id="edbca-678">Savings Account</span></span>   | <span data-ttu-id="edbca-679">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="edbca-679">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="edbca-680">BankGirot-Konto</span><span class="sxs-lookup"><span data-stu-id="edbca-680">BankGirot account</span></span> | <span data-ttu-id="edbca-681">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="edbca-681">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="edbca-682">PlusGirot-Konto</span><span class="sxs-lookup"><span data-stu-id="edbca-682">PlusGirot account</span></span> | <span data-ttu-id="edbca-683">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="edbca-683">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="edbca-684">Einkommenscodes</span><span class="sxs-lookup"><span data-stu-id="edbca-684">Earning codes</span></span>

<span data-ttu-id="edbca-685">Einkommenscodes bestimmen jeden Typ von Einkünften eindeutig, die Arbeitskräfte erhalten</span><span class="sxs-lookup"><span data-stu-id="edbca-685">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="edbca-686">Die Codes decken verschiedene Parameter ab, die sich auf Einkünfte beziehen, wie beispielsweise Buchhaltungsvorschriften, Steuergesetze, Berichterstellungsanforderungen und Bruttoausgleichsfähigkeit.</span><span class="sxs-lookup"><span data-stu-id="edbca-686">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="edbca-687">Wenn eine nicht unterstützte Häufigkeit verwendet wird, wird die Häufigkeit **Jeder Lohn** standardmäßig für die Berechnung verwendet.</span><span class="sxs-lookup"><span data-stu-id="edbca-687">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="edbca-688">Unterstützte Häufigkeiten</span><span class="sxs-lookup"><span data-stu-id="edbca-688">Supported frequencies</span></span>

- <span data-ttu-id="edbca-689">Alle</span><span class="sxs-lookup"><span data-stu-id="edbca-689">All</span></span>
- <span data-ttu-id="edbca-690">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="edbca-690">EVERYPAY</span></span>
- <span data-ttu-id="edbca-691">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="edbca-691">EACHPAYPERIOD</span></span>
- <span data-ttu-id="edbca-692">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="edbca-692">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="edbca-693">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="edbca-693">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="edbca-694">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="edbca-694">1OFMTH</span></span>
- <span data-ttu-id="edbca-695">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="edbca-695">LASTOFMTH</span></span>
- <span data-ttu-id="edbca-696">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="edbca-696">2OFMTH</span></span>
- <span data-ttu-id="edbca-697">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="edbca-697">3OFMTH</span></span>
- <span data-ttu-id="edbca-698">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="edbca-698">4OFMTH</span></span>
- <span data-ttu-id="edbca-699">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="edbca-699">5OFMTH</span></span>
- <span data-ttu-id="edbca-700">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="edbca-700">1N2OFMTH</span></span>
- <span data-ttu-id="edbca-701">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="edbca-701">3N4OFMTH</span></span>
- <span data-ttu-id="edbca-702">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="edbca-702">1N3OFMTH</span></span>
- <span data-ttu-id="edbca-703">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="edbca-703">1N4OFMTH</span></span>
- <span data-ttu-id="edbca-704">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="edbca-704">2N3OFMTH</span></span>
- <span data-ttu-id="edbca-705">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="edbca-705">2N4OFMTH</span></span>
- <span data-ttu-id="edbca-706">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="edbca-706">1N2N3OFMTH</span></span>
- <span data-ttu-id="edbca-707">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="edbca-707">1N2N4OFMTH</span></span>
- <span data-ttu-id="edbca-708">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="edbca-708">1N3N4OFMTH</span></span>
- <span data-ttu-id="edbca-709">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="edbca-709">2N3N4OFMTH</span></span>
- <span data-ttu-id="edbca-710">1N2N3N4OFMTH – 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="edbca-710">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="edbca-711">2N3N4N5OFMth – 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="edbca-711">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="edbca-712">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="edbca-712">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="edbca-713">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="edbca-713">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="edbca-714">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="edbca-714">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="edbca-715">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="edbca-715">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="edbca-716">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="edbca-716">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="edbca-717">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="edbca-717">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="edbca-718">Adressen</span><span class="sxs-lookup"><span data-stu-id="edbca-718">Addresses</span></span>

<span data-ttu-id="edbca-719">Die Kennung bestimmter Codes für Land oder Region, Bundesland/Kanton oder Landkreis (Gemeinde) erfordert spezifische Formate, die Dayforce und Anbieter innerhalb des Landes/innerhalb der Region erkennen können.</span><span class="sxs-lookup"><span data-stu-id="edbca-719">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="edbca-720">Obwohl das Format für Orte flexibel ist, muss jeder Ort einem Bundesland zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="edbca-720">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="edbca-721">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="edbca-721">Human Resources</span></span>              | <span data-ttu-id="edbca-722">Dayforce</span><span class="sxs-lookup"><span data-stu-id="edbca-722">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="edbca-723">Land/Region</span><span class="sxs-lookup"><span data-stu-id="edbca-723">Country/Region</span></span>      | <span data-ttu-id="edbca-724">Ländercode</span><span class="sxs-lookup"><span data-stu-id="edbca-724">Country Code</span></span>          |
| <span data-ttu-id="edbca-725">Postleitzahl</span><span class="sxs-lookup"><span data-stu-id="edbca-725">Zip/Postal Code</span></span>     | <span data-ttu-id="edbca-726">PLZ</span><span class="sxs-lookup"><span data-stu-id="edbca-726">Postal Code</span></span>           |
| <span data-ttu-id="edbca-727">Zustand</span><span class="sxs-lookup"><span data-stu-id="edbca-727">State</span></span>               | <span data-ttu-id="edbca-728">Bundeslandcode</span><span class="sxs-lookup"><span data-stu-id="edbca-728">State Code</span></span>            |
| <span data-ttu-id="edbca-729">Stadt</span><span class="sxs-lookup"><span data-stu-id="edbca-729">City</span></span>                | <span data-ttu-id="edbca-730">Stadt</span><span class="sxs-lookup"><span data-stu-id="edbca-730">City</span></span>                  |
| <span data-ttu-id="edbca-731">Verwaltungsbezirk</span><span class="sxs-lookup"><span data-stu-id="edbca-731">County</span></span>              | <span data-ttu-id="edbca-732">Landkreis (Gemeinde)</span><span class="sxs-lookup"><span data-stu-id="edbca-732">County (Municipality)</span></span> |
| <span data-ttu-id="edbca-733">Straße</span><span class="sxs-lookup"><span data-stu-id="edbca-733">Street</span></span>              | <span data-ttu-id="edbca-734">Adresszeile 1</span><span class="sxs-lookup"><span data-stu-id="edbca-734">Address Line 1</span></span>        |
| <span data-ttu-id="edbca-735">Hausnummer</span><span class="sxs-lookup"><span data-stu-id="edbca-735">Street Number</span></span>       | <span data-ttu-id="edbca-736">Adresszeile 2</span><span class="sxs-lookup"><span data-stu-id="edbca-736">Address Line 2</span></span>        |
| <span data-ttu-id="edbca-737">Gebäudeergänzung</span><span class="sxs-lookup"><span data-stu-id="edbca-737">Building Complement</span></span> | <span data-ttu-id="edbca-738">Adresszeile 5</span><span class="sxs-lookup"><span data-stu-id="edbca-738">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="edbca-739">Ausweisnummer</span><span class="sxs-lookup"><span data-stu-id="edbca-739">Passport number</span></span>

<span data-ttu-id="edbca-740">Mitarbeiter können Ausweisinformationen melden.</span><span class="sxs-lookup"><span data-stu-id="edbca-740">Employees can declare passport information.</span></span> <span data-ttu-id="edbca-741">Diese Informationen haben den Kennungstyp **Ausweis** und sind in Dayforce als Teil der für Mexiko spezifischen Informationen eines Mitarbeiters integriert.</span><span class="sxs-lookup"><span data-stu-id="edbca-741">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="edbca-742">Kennungstyp = „Ausweis”</span><span class="sxs-lookup"><span data-stu-id="edbca-742">Identification Type = "Passport"</span></span>
- <span data-ttu-id="edbca-743">Ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="edbca-743">Issued Date</span></span>
- <span data-ttu-id="edbca-744">Ablaufdatum</span><span class="sxs-lookup"><span data-stu-id="edbca-744">Expiration Date</span></span>

<span data-ttu-id="edbca-745">Mitarbeiter können mehrere Kennungsnummern des Kennungstyps **Ausweis** melden.</span><span class="sxs-lookup"><span data-stu-id="edbca-745">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="edbca-746">Jedoch wird nur der aktuell aktive Ausweiseintrag in Dayforce integriert.</span><span class="sxs-lookup"><span data-stu-id="edbca-746">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="edbca-747">Wenn alle Ausweiseinträge abgelaufen sind, ist der Ausweis, der zuletzt ausgestellt wurde, in Dayforce integriert.</span><span class="sxs-lookup"><span data-stu-id="edbca-747">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]