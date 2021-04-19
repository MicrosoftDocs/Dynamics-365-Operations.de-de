---
title: Integration mit Dayforce konfigurieren
description: Die Integration zwischen Microsoft Dynamics 365 Human Resources und Ceridian Dayforce erfordert mehrere Konfigurationsschritte, die in diesem Artikel beschrieben sind. Sie müssen die Integration sowohl in Human Resources als auch in Dayforce konfigurieren, bevor Sie einen Zahlungslauf verarbeiten können.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: bcb57082a49fc07a4139aa37f9507890ca7ed620
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805081"
---
# <a name="configure-integration-with-dayforce"></a><span data-ttu-id="054e3-104">Integration mit Dayforce konfigurieren</span><span class="sxs-lookup"><span data-stu-id="054e3-104">Configure integration with Dayforce</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="054e3-105">Die Integration zwischen Microsoft Dynamics 365 Human Resources und Ceridian Dayforce erfordert mehrere Konfigurationsschritte, die in diesem Artikel beschrieben sind.</span><span class="sxs-lookup"><span data-stu-id="054e3-105">The integration between Microsoft Dynamics 365 Human Resources and Ceridian Dayforce relies on several configuration steps that are described in this article.</span></span> <span data-ttu-id="054e3-106">Sie müssen die Integration sowohl in Human Resources als auch in Dayforce konfigurieren, bevor Sie einen Zahlungslauf verarbeiten können.</span><span class="sxs-lookup"><span data-stu-id="054e3-106">You must configure the integration in both Human Resources and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="054e3-107">Wenn Sie einen Dienst wie Dayforce verwenden, um Zahlungsläufe abzuschließen, müssen Sie die Integration in Human Resources ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="054e3-107">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Human Resources.</span></span> <span data-ttu-id="054e3-108">Die Integration erfordert bestimmte Daten aus Human Resources.</span><span class="sxs-lookup"><span data-stu-id="054e3-108">The integration requires specific data from Human Resources.</span></span> <span data-ttu-id="054e3-109">Daher müssen Sie überprüfen, dass die Daten, die Dayforce zugeordnet sind, in Human Resources in einer Weise konfiguriert werden, die die Integration unterstützt.</span><span class="sxs-lookup"><span data-stu-id="054e3-109">Therefore, you must verify that data that is mapped to Dayforce is configured in Human Resources in a manner that supports the integration.</span></span> <span data-ttu-id="054e3-110">Bei der Integration werden die folgenden allgemeinen Kategorien von Daten verwendet:</span><span class="sxs-lookup"><span data-stu-id="054e3-110">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="054e3-111">Personalverwaltungsdaten</span><span class="sxs-lookup"><span data-stu-id="054e3-111">Human resources data</span></span>
- <span data-ttu-id="054e3-112">Vergütungsdaten</span><span class="sxs-lookup"><span data-stu-id="054e3-112">Compensation data</span></span>
- <span data-ttu-id="054e3-113">Lohndaten, wie Lohnzyklen, Lohnperioden und Einkommenscodes</span><span class="sxs-lookup"><span data-stu-id="054e3-113">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="054e3-114">Arbeitskraftdaten</span><span class="sxs-lookup"><span data-stu-id="054e3-114">Worker data</span></span>

<span data-ttu-id="054e3-115">In diesem Artikel werden die Schritte beschrieben, die Sie befolgen müssen, um die Integration zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="054e3-115">This article describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="054e3-116">Es werden auch die Datentypen und die Konfigurationsdetails erklärt, die für die Integration erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="054e3-116">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="054e3-117">Die Integration aktivieren</span><span class="sxs-lookup"><span data-stu-id="054e3-117">Enable the integration</span></span>

<span data-ttu-id="054e3-118">In Human Resources müssen Sie die Integration aktivieren und die Konfigurationsinformationen eingeben, um eine Verbindung mit Dayforce herzustellen.</span><span class="sxs-lookup"><span data-stu-id="054e3-118">In Human Resources, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="054e3-119">Wenn Sie möchten, dass die erstellte Hauptbuchtransaktion in Microsoft Dynamics 365 Finance importiert wird, müssen Sie auch ein Microsoft Azure-Speicherkonto einrichten und die Azure Storage-Verbindungszeichenfolge in Finance eingeben.</span><span class="sxs-lookup"><span data-stu-id="054e3-119">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 Finance, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance.</span></span>

<span data-ttu-id="054e3-120">Um die Integration in Human Resources zu aktivieren, gehen Sie folgendermaßen vor.</span><span class="sxs-lookup"><span data-stu-id="054e3-120">To turn on the integration in Human Resources, follow these steps.</span></span>

1. <span data-ttu-id="054e3-121">Wählen Sie auf der Seite **Systemverwaltung** die Option **Integrationskonfiguration** aus.</span><span class="sxs-lookup"><span data-stu-id="054e3-121">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="054e3-122">Geben Sie den sicheren Datenübertragungsprotokoll-(FTP)-Endpunkt und den sicheren FTP-Ordnerpfad ein.</span><span class="sxs-lookup"><span data-stu-id="054e3-122">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="054e3-123">Geben Sie den Benutzernamen und das Kennwort des Benutzers ein, der auf den sicheren FTP-Endpunkt und Ordnerpfad zugreift.</span><span class="sxs-lookup"><span data-stu-id="054e3-123">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="054e3-124">Testen Sie die Verbindung nach Bedarf, und legen Sie die Option **Lohnintegration aktivieren** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="054e3-124">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="054e3-125">Wenn die Integration aktiviert ist, werden Datenexportpaket und Dateien erstellt und die Häufigkeit wird festgelegt.</span><span class="sxs-lookup"><span data-stu-id="054e3-125">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="054e3-126">Sie können diese Häufigkeit nach Bedarf ändern.</span><span class="sxs-lookup"><span data-stu-id="054e3-126">You can change this frequency as you require.</span></span>

<span data-ttu-id="054e3-127">Weitere Informationen zu Azure-Speicherkonten und Azure Storage-Verbindungszeichenfolgen finden Sie in den folgenden Azure-Artikeln:</span><span class="sxs-lookup"><span data-stu-id="054e3-127">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure articles:</span></span>

- [<span data-ttu-id="054e3-128">Über Azure-Speicherkonten</span><span class="sxs-lookup"><span data-stu-id="054e3-128">About Azure storage accounts</span></span>](https://docs.microsoft.com/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="054e3-129">Azure Storage-Verbindungszeichenfolgen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="054e3-129">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="054e3-130">Technische Details, wenn Lohnintegration aktiviert ist</span><span class="sxs-lookup"><span data-stu-id="054e3-130">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="054e3-131">Die Aktivierung von Lohnintegration hat zwei primäre Auswirkungen:</span><span class="sxs-lookup"><span data-stu-id="054e3-131">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="054e3-132">Ein Datenexportprojekt namens „Lohnintegrationsexport“ wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="054e3-132">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="054e3-133">Dieses Projekt enthält die Entitäten und Felder, die für die Lohnintegration erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="054e3-133">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="054e3-134">Um das Projekt zu überprüfen, wechseln Sie zu **Systemverwaltung**, wählen Sie die Kachel **Datenverwaltung** aus, und öffnen Sie anschließend das Datenprojekt aus der Projektliste.</span><span class="sxs-lookup"><span data-stu-id="054e3-134">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="054e3-135">Dieser Stapelverarbeitungsauftrag führt das Datenexportprojekt aus, verschlüsselt das Datenpaket und überträgt die Datenenpaketdatei auf den SFTP-Endpunkt, der auf dem Bildschirm **Integrationskonfiguration** konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="054e3-135">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="054e3-136">Das Datenpaket, das zum SFTP-Endpunkt übertragen wird, wird mit einem Schlüssel verschlüsselt, für das Paket eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="054e3-136">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="054e3-137">Der Schlüssel befindet sich in einer Azure Key Vault, auf den nur durch Ceridian zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="054e3-137">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="054e3-138">Es ist nicht möglich, die Datenpaketinhalte zu entschlüsseln und zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="054e3-138">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="054e3-139">Wenn Sie den Inhalt des Datenpakets überprüfen möchten, müssen Sie das Datenprojekt „Lohnintegrationsexport“ manuell exportieren, herunterladen und dann öffnen.</span><span class="sxs-lookup"><span data-stu-id="054e3-139">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="054e3-140">Beim manuellen Export wird keine Verschlüsselung angewendet oder das Paket übertragen.</span><span class="sxs-lookup"><span data-stu-id="054e3-140">Manual export will not apply encryption or transfer the package.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="054e3-141">Ihre Daten konfigurieren</span><span class="sxs-lookup"><span data-stu-id="054e3-141">Configure your data</span></span> 

<span data-ttu-id="054e3-142">Um die Lohnbuchung zu verarbeiten, müssen Sie Personalverwaltungsdaten in Human Resources konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="054e3-142">To process payroll, you must configure human resource data in Human Resources.</span></span> <span data-ttu-id="054e3-143">Sie müssen Organisationsdaten, wie Stellen und Positionen, zusammen mit Vorteilen Vergütungsinformationen einrichten.</span><span class="sxs-lookup"><span data-stu-id="054e3-143">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="054e3-144">Diese Informationen stellen Beschäftigung, Lohn und die Abzugsinformationen bereit, die zur Generierung der Mitarbeiterentlohnung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="054e3-144">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="054e3-145">Personalverwaltungsdaten</span><span class="sxs-lookup"><span data-stu-id="054e3-145">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="054e3-146">Vergütungen</span><span class="sxs-lookup"><span data-stu-id="054e3-146">Benefits</span></span> 

<span data-ttu-id="054e3-147">Die Personalverwaltung stellt eine Reihe von Tools für die Einrichtung und Verwaltung der Vorteile, Abzüge und Vergütungspläne der Arbeitskräfte bereit, die eine Organisation für seine Arbeitskräfte anbietet oder verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="054e3-147">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="054e3-148">Wenn Sie Vorteile erstellen, sollten Sie folgende Daten und Konfigurationen bedenken, die in Dayforce verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="054e3-148">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="054e3-149">Vorteilspläne</span><span class="sxs-lookup"><span data-stu-id="054e3-149">Benefit plans</span></span>

- <span data-ttu-id="054e3-150">Plan (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-150">Plan (required)</span></span>
- <span data-ttu-id="054e3-151">Typ (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-151">Type (required)</span></span>
- <span data-ttu-id="054e3-152">Lohnauswirkung (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-152">Payroll impact (required)</span></span>
- <span data-ttu-id="054e3-153">Rückstände wiederherstellen</span><span class="sxs-lookup"><span data-stu-id="054e3-153">Recover arrears</span></span>
- <span data-ttu-id="054e3-154">Abzugsverfahren</span><span class="sxs-lookup"><span data-stu-id="054e3-154">Deduction method</span></span>
- <span data-ttu-id="054e3-155">Abzugspriorität</span><span class="sxs-lookup"><span data-stu-id="054e3-155">Deduction priority</span></span>
- <span data-ttu-id="054e3-156">Periode eingrenzen</span><span class="sxs-lookup"><span data-stu-id="054e3-156">Limit period</span></span>
- <span data-ttu-id="054e3-157">Limitbetrag</span><span class="sxs-lookup"><span data-stu-id="054e3-157">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="054e3-158">Vergütungen</span><span class="sxs-lookup"><span data-stu-id="054e3-158">Benefits</span></span>

- <span data-ttu-id="054e3-159">Plan (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-159">Plan (required)</span></span>
- <span data-ttu-id="054e3-160">Typ (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-160">Type (required)</span></span>
- <span data-ttu-id="054e3-161">Option (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-161">Option (required)</span></span>
- <span data-ttu-id="054e3-162">Vorteilskennung (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-162">Benefit ID (required)</span></span>
- <span data-ttu-id="054e3-163">Häufigkeit</span><span class="sxs-lookup"><span data-stu-id="054e3-163">Frequency</span></span>
- <span data-ttu-id="054e3-164">Basis</span><span class="sxs-lookup"><span data-stu-id="054e3-164">Basis</span></span>
- <span data-ttu-id="054e3-165">Betrag oder Satz</span><span class="sxs-lookup"><span data-stu-id="054e3-165">Amount or rate</span></span>
- <span data-ttu-id="054e3-166">Einkommenscode</span><span class="sxs-lookup"><span data-stu-id="054e3-166">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="054e3-167">Unterstützte Häufigkeiten</span><span class="sxs-lookup"><span data-stu-id="054e3-167">Supported frequencies</span></span> 

- <span data-ttu-id="054e3-168">Wöchentlich</span><span class="sxs-lookup"><span data-stu-id="054e3-168">Weekly</span></span>
- <span data-ttu-id="054e3-169">14-tägig</span><span class="sxs-lookup"><span data-stu-id="054e3-169">Bi-weekly</span></span>
- <span data-ttu-id="054e3-170">Halbmonatlich</span><span class="sxs-lookup"><span data-stu-id="054e3-170">Semi-monthly</span></span>
- <span data-ttu-id="054e3-171">Monatlich</span><span class="sxs-lookup"><span data-stu-id="054e3-171">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="054e3-172">Unterstützte Basen</span><span class="sxs-lookup"><span data-stu-id="054e3-172">Supported bases</span></span> 

- <span data-ttu-id="054e3-173">Fester Betrag</span><span class="sxs-lookup"><span data-stu-id="054e3-173">Fixed amount</span></span>
- <span data-ttu-id="054e3-174">Prozent des Einkommens</span><span class="sxs-lookup"><span data-stu-id="054e3-174">Percent of earnings</span></span>
- <span data-ttu-id="054e3-175">Produktive Stunden</span><span class="sxs-lookup"><span data-stu-id="054e3-175">Productive hours</span></span>

<span data-ttu-id="054e3-176">Dayforce erstellt die folgenden Abzüge, basierend auf den Lohnauswirkungen, die im Vorteilsplan definiert sind.</span><span class="sxs-lookup"><span data-stu-id="054e3-176">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="054e3-177">Auswahl in Human Resources</span><span class="sxs-lookup"><span data-stu-id="054e3-177">Selection in Human Resources</span></span>        | <span data-ttu-id="054e3-178">Ergebnis in Dayforce</span><span class="sxs-lookup"><span data-stu-id="054e3-178">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="054e3-179">Nichts</span><span class="sxs-lookup"><span data-stu-id="054e3-179">None</span></span>                       | <span data-ttu-id="054e3-180">Es wird kein Abzug erstellt.</span><span class="sxs-lookup"><span data-stu-id="054e3-180">No deduction is created.</span></span>                      |
| <span data-ttu-id="054e3-181">Nur Abzug</span><span class="sxs-lookup"><span data-stu-id="054e3-181">Deduction only</span></span>             | <span data-ttu-id="054e3-182">Ein Mitarbeiterabzug wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="054e3-182">An employee deduction is created.</span></span>             |
| <span data-ttu-id="054e3-183">Nur Beitrag</span><span class="sxs-lookup"><span data-stu-id="054e3-183">Contribution only</span></span>          | <span data-ttu-id="054e3-184">Ein Arbeitgeberabzug wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="054e3-184">An employer deduction is created.</span></span>             |
| <span data-ttu-id="054e3-185">Abzug und Beitrag</span><span class="sxs-lookup"><span data-stu-id="054e3-185">Deduction and contribution</span></span> | <span data-ttu-id="054e3-186">Mitarbeiter- und Arbeitgeberabzüge werden erstellt.</span><span class="sxs-lookup"><span data-stu-id="054e3-186">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="054e3-187">Weitere Informationen darüber, wie Sie ein Vorteilsprogramm definieren und verwalten finden Sie in den folgenden Artikeln:</span><span class="sxs-lookup"><span data-stu-id="054e3-187">For more information about how to define and manage a benefits program, see the following articles:</span></span>

- [<span data-ttu-id="054e3-188">Mitarbeitervorteilsprogramm anbieten</span><span class="sxs-lookup"><span data-stu-id="054e3-188">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="054e3-189">Neue Vergütung erstellen</span><span class="sxs-lookup"><span data-stu-id="054e3-189">Create a new benefit</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="054e3-190">Vorteilsberechtigungsregeln und Richtlinien definieren</span><span class="sxs-lookup"><span data-stu-id="054e3-190">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="054e3-191">Vorteile von Arbeitskräften registrieren und entfernen</span><span class="sxs-lookup"><span data-stu-id="054e3-191">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="054e3-192">Vergütung</span><span class="sxs-lookup"><span data-stu-id="054e3-192">Compensation</span></span> 

<span data-ttu-id="054e3-193">Die Vergütungsverwaltung dient zum Steuern der Abwicklung des Grundlohns und der Prämien.</span><span class="sxs-lookup"><span data-stu-id="054e3-193">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="054e3-194">Sie steuern den festen Grundlohn eines Mitarbeiters und dessen Lohnsteigerungen nach Plänen für feste Vergütung.</span><span class="sxs-lookup"><span data-stu-id="054e3-194">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="054e3-195">Die Zahlung leistungsbezogener Prämien, wie Boni, Leistungsprämien, Aktienoptionen und -überlassungen sowie Einmalprämien werden durch Pläne für variable Vergütung gesteuert.</span><span class="sxs-lookup"><span data-stu-id="054e3-195">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="054e3-196">Dayforce verwendet Vergütungsinformationen, um einen Stunden- oder Jahressatz für einen Mitarbeiter zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="054e3-196">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="054e3-197">Feste Vergütungspläne und Lohnsatzumrechnungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="054e3-197">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="054e3-198">Mitarbeiter müssen einem festen Vergütungsplan zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="054e3-198">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="054e3-199">Weitere Informationen zu Kompensationsplänen finden Sie in den folgenden Artikeln:</span><span class="sxs-lookup"><span data-stu-id="054e3-199">For more information about compensation plans, see the following articles:</span></span>

- [<span data-ttu-id="054e3-200">Feste Vergütungspläne erstellen</span><span class="sxs-lookup"><span data-stu-id="054e3-200">Create fixed compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="054e3-201">Variable Vergütungspläne erstellen</span><span class="sxs-lookup"><span data-stu-id="054e3-201">Create variable compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="054e3-202">Gehalts-/Vergütungsstruktur und -pläne entwickeln</span><span class="sxs-lookup"><span data-stu-id="054e3-202">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="054e3-203">Vergütung verarbeiten</span><span class="sxs-lookup"><span data-stu-id="054e3-203">Process compensation</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="054e3-204">Vergütungsprozess definieren und Ergebnisse berechnen</span><span class="sxs-lookup"><span data-stu-id="054e3-204">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="054e3-205">Einen Mitarbeiters in einem Plan für eine feste Vergütung registrieren</span><span class="sxs-lookup"><span data-stu-id="054e3-205">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="054e3-206">Einen Mitarbeiter in einem Plan für variable Vergütung registrieren</span><span class="sxs-lookup"><span data-stu-id="054e3-206">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="054e3-207">Stellentyp</span><span class="sxs-lookup"><span data-stu-id="054e3-207">Jobs</span></span> 

<span data-ttu-id="054e3-208">Eine Stelle ist eine Sammlung der Aufgaben und Zuständigkeiten, die für eine Person, die eine Tätigkeit ausführt, obligatorisch sind.</span><span class="sxs-lookup"><span data-stu-id="054e3-208">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="054e3-209">Weitere Informationen finden Sie in folgenden Artikeln:</span><span class="sxs-lookup"><span data-stu-id="054e3-209">For more information, see the following articles:</span></span>

- [<span data-ttu-id="054e3-210">Komponenten einer Stelle einrichten</span><span class="sxs-lookup"><span data-stu-id="054e3-210">Setting up the components of a job</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="054e3-211">Neue Stellen definieren</span><span class="sxs-lookup"><span data-stu-id="054e3-211">Define new jobs</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="054e3-212">Positionen</span><span class="sxs-lookup"><span data-stu-id="054e3-212">Positions</span></span>

<span data-ttu-id="054e3-213">Eine Position ist eine einzelne Instanz eines Einzelvorgangs.</span><span class="sxs-lookup"><span data-stu-id="054e3-213">A position is an individual instance of a job.</span></span> <span data-ttu-id="054e3-214">Beispielsweise ist die Position „Verkaufsleiter (Ost)” eine der Positionen, die der Stelle „Verkaufsleiter” zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="054e3-214">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="054e3-215">Eine Position ist in einer Abteilung vorhanden.</span><span class="sxs-lookup"><span data-stu-id="054e3-215">A position exists in a department.</span></span> <span data-ttu-id="054e3-216">Nur jeweils eine Arbeitskraft kann jeder Position zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="054e3-216">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="054e3-217">Bedenken Sie die folgenden Daten und Konfigurationen, wenn Sie Positionen einrichten:</span><span class="sxs-lookup"><span data-stu-id="054e3-217">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="054e3-218">Position (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-218">Position (required)</span></span>
- <span data-ttu-id="054e3-219">Beschreibung (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-219">Description (required)</span></span>
- <span data-ttu-id="054e3-220">Stelle (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-220">Job (required)</span></span>
- <span data-ttu-id="054e3-221">Abteilung (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-221">Department (required)</span></span>
- <span data-ttu-id="054e3-222">Positionstyp (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-222">Position type (required)</span></span>
- <span data-ttu-id="054e3-223">Vollzeitäquivalent</span><span class="sxs-lookup"><span data-stu-id="054e3-223">Full-time equivalent</span></span>
- <span data-ttu-id="054e3-224">Normale Stunden pro Jahr (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-224">Annual regular hours (required)</span></span>
- <span data-ttu-id="054e3-225">Gezahlt von der juristischen Person (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-225">Paid by legal entity (required)</span></span>
- <span data-ttu-id="054e3-226">Lohnzyklus (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-226">Pay cycle (required)</span></span>
- <span data-ttu-id="054e3-227">Standardfinanzdimension – Kostenstelle (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-227">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="054e3-228">Arbeitskraftzuweisung – Arbeitskraft, Zuweisungsanfang, Zuweisungsende, Ursachencode</span><span class="sxs-lookup"><span data-stu-id="054e3-228">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="054e3-229">Wenn mehrere Positionen in derselben Abteilung derselben Stelle zugeordnet sind, werden sie in einer einzelnen Position in Dayforce konsolidiert.</span><span class="sxs-lookup"><span data-stu-id="054e3-229">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="054e3-230">Weitere Informationen finden Sie in folgenden Artikeln:</span><span class="sxs-lookup"><span data-stu-id="054e3-230">For more information, see the following articles:</span></span>

- [<span data-ttu-id="054e3-231">Belegschaft mittels Abteilungen, Stellen und Positionen verwalten</span><span class="sxs-lookup"><span data-stu-id="054e3-231">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="054e3-232">Positionen einrichten</span><span class="sxs-lookup"><span data-stu-id="054e3-232">Set up positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="054e3-233">Abteilungen</span><span class="sxs-lookup"><span data-stu-id="054e3-233">Departments</span></span>

<span data-ttu-id="054e3-234">Eine Abteilung ist eine Organisationseinheit, die eine Kategorie oder einen funktionalen Bereich einer Organisation darstellt.</span><span class="sxs-lookup"><span data-stu-id="054e3-234">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="054e3-235">Eine Abteilung ist für einen bestimmten Bereich der Organisation wie zum Beispiel Verkauf, Buchhaltung oder Personalverwaltung zuständig.</span><span class="sxs-lookup"><span data-stu-id="054e3-235">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="054e3-236">Sie können Abteilungen verwenden, um zu Funktionsbereiche zu melden.</span><span class="sxs-lookup"><span data-stu-id="054e3-236">You can use departments to report on functional areas.</span></span> <span data-ttu-id="054e3-237">Abteilungen können Gewinn- und Verlustzuständigkeit haben.</span><span class="sxs-lookup"><span data-stu-id="054e3-237">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="054e3-238">Weitere Informationen finden Sie in folgenden Artikeln:</span><span class="sxs-lookup"><span data-stu-id="054e3-238">For more information, see the following articles:</span></span>

- [<span data-ttu-id="054e3-239">Abteilung erstellen und der Abteilungshierarchie zuordnen</span><span class="sxs-lookup"><span data-stu-id="054e3-239">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="054e3-240">Neue Abteilungen definieren</span><span class="sxs-lookup"><span data-stu-id="054e3-240">Define new departments</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="054e3-241">Lohnzyklen und Lohnperioden</span><span class="sxs-lookup"><span data-stu-id="054e3-241">Pay cycles and pay periods</span></span>

<span data-ttu-id="054e3-242">Ein Lohnzyklus bestimmt, wie oft Lohn ausgezahlt wird, sowie die spezifischen Tage, an denen Arbeitskräfte bezahlt werden.</span><span class="sxs-lookup"><span data-stu-id="054e3-242">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="054e3-243">Ein Lohnzyklus kann beispielsweise monatlich sein, und Mitarbeiter werden am letzten Tag des Monats bezahlt.</span><span class="sxs-lookup"><span data-stu-id="054e3-243">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="054e3-244">Alternativ könnte ein Lohnzyklus wöchentlich sein, und Mitarbeiter werden am Dienstag nach Ende der Lohnperiode bezahlt.</span><span class="sxs-lookup"><span data-stu-id="054e3-244">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="054e3-245">Lohnzyklen werden Positionen zugewiesen, um zu steuern, wann Mitarbeiter in diesen Positionen bezahlt werden.</span><span class="sxs-lookup"><span data-stu-id="054e3-245">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="054e3-246">Nachdem Sie Lohnzyklen erstellen, können Sie Lohnperioden für jeden Zyklus generieren.</span><span class="sxs-lookup"><span data-stu-id="054e3-246">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="054e3-247">Jede Lohnperiode enthält ein Standardzahlungsdatum, das auf den von Ihnen bereitgestellten Informationen basiert.</span><span class="sxs-lookup"><span data-stu-id="054e3-247">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="054e3-248">Allerdings können Sie das Standardzahlungsdatum in einer Lohnperiode ändern, um Ausnahmen zuzulassen, wie beispielsweise wenn das Zahlungsdatum auf einen Feiertag fällt.</span><span class="sxs-lookup"><span data-stu-id="054e3-248">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="054e3-249">Die folgenden Informationen werden in Dayforce verwendet:</span><span class="sxs-lookup"><span data-stu-id="054e3-249">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="054e3-250">Lohnzyklus (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-250">Pay cycle (required)</span></span>
- <span data-ttu-id="054e3-251">Lohnzyklushäufigkeit (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-251">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="054e3-252">Periodenstartdatum (erstes erforderliche Lohnperiode)</span><span class="sxs-lookup"><span data-stu-id="054e3-252">Period start date (first pay period required)</span></span>
- <span data-ttu-id="054e3-253">Standardzahlungsdatum (erste erforderliche Lohnperiode)</span><span class="sxs-lookup"><span data-stu-id="054e3-253">Default payment date (first pay period required)</span></span>

<span data-ttu-id="054e3-254">Diese Informationen werden mit Dayforce als Lohngruppen integriert und sind nach Land oder Region für jeden Lohnzyklus getrennt.</span><span class="sxs-lookup"><span data-stu-id="054e3-254">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="054e3-255">Es muss mindestens eine Lohnperiode vor der Integration generiert werden.</span><span class="sxs-lookup"><span data-stu-id="054e3-255">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="054e3-256">Dayforce generiert Lohngruppenkalender und Zahlungsdaten basierend auf dem Anfangsdatum der ersten Lohnperiode und dem Standardzahlungsdatums, das in Human Resources eingerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="054e3-256">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Human Resources.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="054e3-257">Einkommenscodes</span><span class="sxs-lookup"><span data-stu-id="054e3-257">Earning codes</span></span>

<span data-ttu-id="054e3-258">Einkommenscodes bestimmen jeden Typ von Einkünften eindeutig, die Arbeitskräfte erhalten</span><span class="sxs-lookup"><span data-stu-id="054e3-258">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="054e3-259">Die Codes haben verschiedene Parameter, die sich auf Einkünfte beziehen, wie beispielsweise Buchhaltungsvorschriften, Steuergesetze, Berichterstellungsanforderungen und Bruttoausgleichsfähigkeit.</span><span class="sxs-lookup"><span data-stu-id="054e3-259">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="054e3-260">Die folgenden Informationen werden in Dayforce verwendet:</span><span class="sxs-lookup"><span data-stu-id="054e3-260">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="054e3-261">Einkommenscode (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-261">Earning Code (required)</span></span>
- <span data-ttu-id="054e3-262">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="054e3-262">Description</span></span>
- <span data-ttu-id="054e3-263">Maßeinheit</span><span class="sxs-lookup"><span data-stu-id="054e3-263">Unit of measure</span></span>
- <span data-ttu-id="054e3-264">Produktiv</span><span class="sxs-lookup"><span data-stu-id="054e3-264">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="054e3-265">Arbeitskraftdaten</span><span class="sxs-lookup"><span data-stu-id="054e3-265">Worker data</span></span>

<span data-ttu-id="054e3-266">Datensätze für die verschiedenen Arten von Arbeitskräften, die Sie haben, sind für Ihre Personalverwaltung- sowie für Ihre Lohnsysteme von Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="054e3-266">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="054e3-267">Anhand der eingegebenen Informationen lassen sich Arbeitskräfte sowie personenbezogene Informationen nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="054e3-267">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="054e3-268">Sie können die folgenden Informationen für Arbeitskräfte verwalten:</span><span class="sxs-lookup"><span data-stu-id="054e3-268">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="054e3-269">**Basis** – Verwalten grundlegender Informationen über eine Arbeitskraft, beispielsweise Kontaktinformationen, demografische Informationen, Kennungsinformationen, Familieninformationen, Militärdienststatus, Ausländerinformationen sowie personenbezogene und Notfallkontakte.</span><span class="sxs-lookup"><span data-stu-id="054e3-269">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="054e3-270">**Beschäftigung** – Verwalten von Informationen zum Beschäftigungsverhältnis einer Arbeitskraft, wie Unternehmens- oder Organisationszugehörigkeit, Positionszuweisung, Start- und Enddatum, Arbeitsberechtigung, Beschäftigungsbedingungen, Rente, Urlaub und Versetzungen.</span><span class="sxs-lookup"><span data-stu-id="054e3-270">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="054e3-271">**Urlaub und Abwesenheit** – Verwalten von Informationen zur Abwesenheit einer Arbeitskraft, beispielsweise Arbeitszeitkalender, Abwesenheitsbuchungen und Abwesenheitseinrichtung.</span><span class="sxs-lookup"><span data-stu-id="054e3-271">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="054e3-272">**Vergütung und Lohn** – Verwalten von Informationen zu den Vergütungsplänen und Lohndaten einer Arbeitskraft, wie der Planregistrierung, Boni, Leistung, Provision, Steuerdaten, Pensionierung und Gehaltsabzüge.</span><span class="sxs-lookup"><span data-stu-id="054e3-272">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="054e3-273">Wenn Sie Arbeitskraftinformationen eingeben, sollten Sie folgende Daten und Konfigurationen bedenken, die in Dayforce verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="054e3-273">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="054e3-274">Allgemeine Angaben</span><span class="sxs-lookup"><span data-stu-id="054e3-274">General information</span></span>

- <span data-ttu-id="054e3-275">Personalnummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-275">Personnel number (required)</span></span>
- <span data-ttu-id="054e3-276">Vorname (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-276">First name (required)</span></span>
- <span data-ttu-id="054e3-277">Nachname (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-277">Last name (required)</span></span>
- <span data-ttu-id="054e3-278">Zweiter Vorname</span><span class="sxs-lookup"><span data-stu-id="054e3-278">Middle name</span></span>
- <span data-ttu-id="054e3-279">Dienstalterdatum</span><span class="sxs-lookup"><span data-stu-id="054e3-279">Seniority date</span></span>
- <span data-ttu-id="054e3-280">Bekannt als</span><span class="sxs-lookup"><span data-stu-id="054e3-280">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="054e3-281">Personenbezogene Informationen</span><span class="sxs-lookup"><span data-stu-id="054e3-281">Personal information</span></span>

- <span data-ttu-id="054e3-282">Familienstand (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-282">Marital status (required)</span></span>
- <span data-ttu-id="054e3-283">Geburtsdatum (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-283">Birth date (required)</span></span>
- <span data-ttu-id="054e3-284">Geschlecht (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-284">Gender (required)</span></span>
- <span data-ttu-id="054e3-285">Person mit Behinderung</span><span class="sxs-lookup"><span data-stu-id="054e3-285">Person with disabilities</span></span>
- <span data-ttu-id="054e3-286">Nationalitätsland/-region (nur für Mexiko)</span><span class="sxs-lookup"><span data-stu-id="054e3-286">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="054e3-287">Adressdaten</span><span class="sxs-lookup"><span data-stu-id="054e3-287">Address information</span></span>

- <span data-ttu-id="054e3-288">Primär (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-288">Primary (required)</span></span>
- <span data-ttu-id="054e3-289">Land/Region (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-289">Country/region (required)</span></span>
- <span data-ttu-id="054e3-290">Postleitzahl (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-290">Postal code (required)</span></span>
- <span data-ttu-id="054e3-291">Hausnummer (erforderlich) (nur für Mexiko)</span><span class="sxs-lookup"><span data-stu-id="054e3-291">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="054e3-292">Gebäudeergänzung (nur für Mexiko)</span><span class="sxs-lookup"><span data-stu-id="054e3-292">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="054e3-293">Ort (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-293">City (required)</span></span>
- <span data-ttu-id="054e3-294">Bundesland/Kanton (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-294">State (required)</span></span>
- <span data-ttu-id="054e3-295">Landkreis (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-295">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="054e3-296">Kontaktdaten</span><span class="sxs-lookup"><span data-stu-id="054e3-296">Contact information</span></span> 

- <span data-ttu-id="054e3-297">Primär (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-297">Primary (required)</span></span>
- <span data-ttu-id="054e3-298">Kontaktnummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-298">Contact number (required)</span></span>
- <span data-ttu-id="054e3-299">Durchwahl</span><span class="sxs-lookup"><span data-stu-id="054e3-299">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="054e3-300">Lohndaten und Einkommenscodes</span><span class="sxs-lookup"><span data-stu-id="054e3-300">Payroll information and earning codes</span></span>

<span data-ttu-id="054e3-301">Mitarbeitern müssen bestimmte Einkommen mit einer bestimmten Zahlungshäufigkeit zugewiesen werden und sie müssen eine bevorzugte Zahlungsmethode haben.</span><span class="sxs-lookup"><span data-stu-id="054e3-301">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="054e3-302">Die folgenden Felder werden in Dayforce verwendet, um zu gewährleisten, dass diese Voreinstellungen und Einstellungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="054e3-302">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="054e3-303">Einkommenscodes</span><span class="sxs-lookup"><span data-stu-id="054e3-303">Earning codes</span></span>

- <span data-ttu-id="054e3-304">Position (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-304">Position (required)</span></span>
- <span data-ttu-id="054e3-305">Einkommenscode (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-305">Earning Code (required)</span></span>
- <span data-ttu-id="054e3-306">Häufigkeit (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-306">Frequency (required)</span></span>
- <span data-ttu-id="054e3-307">Betrag (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-307">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="054e3-308">Lohndaten</span><span class="sxs-lookup"><span data-stu-id="054e3-308">Payroll information</span></span>

- <span data-ttu-id="054e3-309">Zahlungsmethode</span><span class="sxs-lookup"><span data-stu-id="054e3-309">Payment Method</span></span>
- <span data-ttu-id="054e3-310">Wirtschaftliche Region (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-310">Economic Region (required)</span></span>
- <span data-ttu-id="054e3-311">Mitarbeitervergütungs-ID</span><span class="sxs-lookup"><span data-stu-id="054e3-311">Employee Benefits ID</span></span>
- <span data-ttu-id="054e3-312">Personalausweisnummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-312">National ID Number (required)</span></span>
- <span data-ttu-id="054e3-313">Militärdienstnummer</span><span class="sxs-lookup"><span data-stu-id="054e3-313">Military Service Number</span></span>
- <span data-ttu-id="054e3-314">Schichtkennung (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-314">Shift ID (required)</span></span>
- <span data-ttu-id="054e3-315">Steuernummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-315">Tax Number (required)</span></span>
- <span data-ttu-id="054e3-316">Gewerkschaftskennung (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-316">Union ID (required)</span></span>
- <span data-ttu-id="054e3-317">Arbeitstagkennung (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-317">Work Day ID (required)</span></span>
- <span data-ttu-id="054e3-318">Arbeitserlaubnisnummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-318">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="054e3-319">Für die Zahlungsmethode unterstützt Mexiko **Bargeld**, **Scheck** (der physische Scheck des Unternehmens) und **Elektronische Zahlung**.</span><span class="sxs-lookup"><span data-stu-id="054e3-319">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="054e3-320">Wenn keine Zahlungsmethode angegeben wird, wird **Scheck** standardmäßig verwendet.</span><span class="sxs-lookup"><span data-stu-id="054e3-320">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="054e3-321">Anstellungsdetails</span><span class="sxs-lookup"><span data-stu-id="054e3-321">Employment details</span></span>

<span data-ttu-id="054e3-322">Beschäftigungsdetailhistorie wird als Schlüsselinformation verwendet, um die Status für Einstellung, Kündigung und erneute Einstellung in Dayforce abzuleiten.</span><span class="sxs-lookup"><span data-stu-id="054e3-322">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="054e3-323">Dayforce unterstützt nur einen aktiven Beschäftigungsdatensatz gleichzeitig.</span><span class="sxs-lookup"><span data-stu-id="054e3-323">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="054e3-324">Datum des Beschäftigungsbeginns (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-324">Employment start date (required)</span></span>
- <span data-ttu-id="054e3-325">Datum des Beschäftigungsendes</span><span class="sxs-lookup"><span data-stu-id="054e3-325">Employment end date</span></span>
- <span data-ttu-id="054e3-326">Eintrittstermin</span><span class="sxs-lookup"><span data-stu-id="054e3-326">Start date</span></span>
- <span data-ttu-id="054e3-327">Angepasster Tätigkeitsbeginn</span><span class="sxs-lookup"><span data-stu-id="054e3-327">Adjusted start date</span></span>
- <span data-ttu-id="054e3-328">Kündigungsdatum (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-328">Termination date (required upon termination)</span></span>
- <span data-ttu-id="054e3-329">Kündigungsgrund (erforderlich bei Kündigung)</span><span class="sxs-lookup"><span data-stu-id="054e3-329">Termination reason (required upon termination)</span></span>

<span data-ttu-id="054e3-330">Die Schlüsseldaten eines Mitarbeiters werden abgeleitet, indem die folgenden Informationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="054e3-330">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="054e3-331">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="054e3-331">Human Resources</span></span>                | <span data-ttu-id="054e3-332">Dayforce</span><span class="sxs-lookup"><span data-stu-id="054e3-332">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="054e3-333">Aktuellstes Einstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="054e3-333">Most recent hire date</span></span> | <span data-ttu-id="054e3-334">Beschäftigungsbeginn des Verlaufsdatensatzes zur aktuellen, nicht gekündigten Beschäftigung</span><span class="sxs-lookup"><span data-stu-id="054e3-334">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="054e3-335">Kündigungsdatum</span><span class="sxs-lookup"><span data-stu-id="054e3-335">Termination date</span></span>      | <span data-ttu-id="054e3-336">Kündigungsdatum des Verlaufsdatensatzes zur aktuellen, nicht gekündigten Beschäftigung</span><span class="sxs-lookup"><span data-stu-id="054e3-336">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="054e3-337">Eintrittstermin</span><span class="sxs-lookup"><span data-stu-id="054e3-337">Start date</span></span>            | <span data-ttu-id="054e3-338">Angepasstes Startdatum, Startdatum oder Beschäftigungsbeginn des Verlaufsdatensatzes zur aktuellen, nicht aktiven Beschäftigung</span><span class="sxs-lookup"><span data-stu-id="054e3-338">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="054e3-339">Ursprüngliches Einstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="054e3-339">Original hire date</span></span>    | <span data-ttu-id="054e3-340">Beschäftigungsbeginn des frühesten Beschäftigungsverlaufsdatensatzes</span><span class="sxs-lookup"><span data-stu-id="054e3-340">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="054e3-341">Vergütung</span><span class="sxs-lookup"><span data-stu-id="054e3-341">Compensation</span></span>

<span data-ttu-id="054e3-342">Ein fester Vergütungsplan muss der primären Position jedes Mitarbeiters während einer Beschäftigungsperiode zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="054e3-342">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="054e3-343">Diese Periode beginnt mit dem Datum, an dem der Mitarbeiter eingestellt wurde (oder dem Datum des Beschäftigungsbeginns), und setzt sich bis zur Kündigung fort.</span><span class="sxs-lookup"><span data-stu-id="054e3-343">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="054e3-344">Gültigkeitsdatum (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-344">Effective Date (required)</span></span>
- <span data-ttu-id="054e3-345">Ablaufdatum</span><span class="sxs-lookup"><span data-stu-id="054e3-345">Expiration date</span></span>
- <span data-ttu-id="054e3-346">Lohnsatz (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-346">Pay Rate (required)</span></span>
- <span data-ttu-id="054e3-347">Lohnsatzkonvertierungen (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-347">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="054e3-348">Jährliches Äquivalent (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-348">Annual equivalent (required)</span></span>
- <span data-ttu-id="054e3-349">Stündliches Äquivalent (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-349">Hourly equivalent (required)</span></span>

<span data-ttu-id="054e3-350">Wenn ein Mitarbeiter auf Stundenbasis mehrere Positionen hat, wird die feste Vergütung der primären Position in Dayforce als Basissatz/-gehalt auf Mitarbeiterebene importiert.</span><span class="sxs-lookup"><span data-stu-id="054e3-350">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="054e3-351">Für nicht-primäre Positionen wird der Stundensatz in der entsprechenden Position in Dayforce gespeichert.</span><span class="sxs-lookup"><span data-stu-id="054e3-351">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="054e3-352">Wenn ein Gehalt beziehender Mitarbeiter mehrere Positionen hat, wird der kumulative Stundensatz und das Jahresgehalt über alle aktiven Positionen hinweg abgeleitet und als Basissatz/-gehalt auf Arbeitnehmerebene verwendet.</span><span class="sxs-lookup"><span data-stu-id="054e3-352">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="054e3-353">Kennnummern</span><span class="sxs-lookup"><span data-stu-id="054e3-353">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="054e3-354">Sozialversicherungsbezeichner</span><span class="sxs-lookup"><span data-stu-id="054e3-354">Social Security identifier</span></span> 

<span data-ttu-id="054e3-355">Jeder Mitarbeiter muss einen primären Bezeichner haben.</span><span class="sxs-lookup"><span data-stu-id="054e3-355">Every employee must have one primary identifier.</span></span> <span data-ttu-id="054e3-356">Dieser Bezeichner muss vom Kennungstyp **P.Reg.Nr.** sein.</span><span class="sxs-lookup"><span data-stu-id="054e3-356">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="054e3-357">In Dayforce wird er automatisch als Sozialversicherungsbezeichner des Mitarbeiters abgeleitet, der für die Einstellung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="054e3-357">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="054e3-358">Primär (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-358">Primary (required)</span></span>
- <span data-ttu-id="054e3-359">Kennungstyp = „P.Reg.Nr.”</span><span class="sxs-lookup"><span data-stu-id="054e3-359">Identification Type = "SSN"</span></span>
- <span data-ttu-id="054e3-360">Ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="054e3-360">Issued Date</span></span>
- <span data-ttu-id="054e3-361">Ablaufdatum</span><span class="sxs-lookup"><span data-stu-id="054e3-361">Expiration Date</span></span>

<span data-ttu-id="054e3-362">Mitarbeiter können mehrere Kennungsnummern des Kennungstyps **P.Reg.Nr.** melden.</span><span class="sxs-lookup"><span data-stu-id="054e3-362">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="054e3-363">Jedoch wird nur der Datensatz, der als **Primär** markiert ist, in Dayforce integriert, unabhängig davon, ob die Nummer aktiv oder abgelaufen ist.</span><span class="sxs-lookup"><span data-stu-id="054e3-363">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="054e3-364">Bankkonten und Auszahlungen</span><span class="sxs-lookup"><span data-stu-id="054e3-364">Bank accounts and disbursements</span></span>

<span data-ttu-id="054e3-365">Gültige Bankkontoinformationen müssen für jeden Mitarbeiter eingegeben werden, der per Bankkontoüberweisungen bezahlt werden möchte.</span><span class="sxs-lookup"><span data-stu-id="054e3-365">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="054e3-366">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="054e3-366">Human Resources</span></span>                         | <span data-ttu-id="054e3-367">Dayforce</span><span class="sxs-lookup"><span data-stu-id="054e3-367">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="054e3-368">Bankkontonummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-368">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="054e3-369">SWIFT-Code (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-369">SWIFT code (required)</span></span>          | <span data-ttu-id="054e3-370">Feld **Bankkennung** wird verwendet, wenn Lohn in Mexiko verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="054e3-370">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="054e3-371">Filialnummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-371">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="054e3-372">Bankkontotyp (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-372">Bank account type (required)</span></span>   | <span data-ttu-id="054e3-373">Feld **Kontotyp** wird verwendet, wenn Lohn in Mexiko verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="054e3-373">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="054e3-374">Unterstützte Werte umfassen **Wird geprüft** und **Lohn**.</span><span class="sxs-lookup"><span data-stu-id="054e3-374">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="054e3-375">Mitarbeiter, die per Bankkontoüberweisungen bezahlt werden möchten, müssen eine Verknüpfung zu einem Restbetrags-Bankkonto angeben, das sich unter einer juristischen Person befindet, deren primäre Adresse in Mexiko ist und das einem gültigen Bankkonto von einer mexikanischen Bank zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="054e3-375">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="054e3-376">Alle anderen Nicht-Restbetrags-Bankkonten werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="054e3-376">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="054e3-377">Adressdaten</span><span class="sxs-lookup"><span data-stu-id="054e3-377">Address information</span></span>

<span data-ttu-id="054e3-378">Jeder Mitarbeiter muss einen primären Standort haben.</span><span class="sxs-lookup"><span data-stu-id="054e3-378">Every employee must have one primary location.</span></span> <span data-ttu-id="054e3-379">In Dayforce wird dieser Standort verwendet, um den primären Wohnsitz des Mitarbeiters für Steuerzwecke zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="054e3-379">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="054e3-380">Primär (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-380">Primary (required)</span></span>
- <span data-ttu-id="054e3-381">Land/Region (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-381">Country/region (required)</span></span>
- <span data-ttu-id="054e3-382">Postleitzahl (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-382">Zip/postal code (required)</span></span>
- <span data-ttu-id="054e3-383">Straße (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-383">Street (required)</span></span>
- <span data-ttu-id="054e3-384">Hausnummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-384">Street Number (required)</span></span>
- <span data-ttu-id="054e3-385">Gebäudeergänzung</span><span class="sxs-lookup"><span data-stu-id="054e3-385">Building Complement</span></span>
- <span data-ttu-id="054e3-386">Ort (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-386">City (required)</span></span>
- <span data-ttu-id="054e3-387">Bundesland/Kanton (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-387">State (required)</span></span>
- <span data-ttu-id="054e3-388">Landkreis (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-388">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="054e3-389">Konfigurieren Ihrer Daten, um Vergütung in den USA und Kanada zu generieren</span><span class="sxs-lookup"><span data-stu-id="054e3-389">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="054e3-390">Wenn Sie Vergütung für Mitarbeiter in den USA und Kanada generieren, müssen die folgenden Elemente konfiguriert werden:</span><span class="sxs-lookup"><span data-stu-id="054e3-390">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="054e3-391">Abteilungen sind für Positionen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="054e3-391">Departments are required on positions.</span></span>
- <span data-ttu-id="054e3-392">Kostenstellen müssen als Finanzdimensionen festgelegt werden und müssen das erste Element in der standardmäßigen Finanzdimensions-Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="054e3-392">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="054e3-393">Sie können Human Resources so konfigurieren, dass Positionen eine Abteilung angeben müssen.</span><span class="sxs-lookup"><span data-stu-id="054e3-393">You can configure Human Resources to require that Positions specify a Department.</span></span> <span data-ttu-id="054e3-394">Dazu wechseln Sie zu **Freigegebene Positionen der Personalverwaltung > Positionen > Abteilungen zu Positionen anfordern**.</span><span class="sxs-lookup"><span data-stu-id="054e3-394">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="054e3-395">Es wird empfohlen, dass diese Einstellungen für die Integration erzwungen wird.</span><span class="sxs-lookup"><span data-stu-id="054e3-395">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="054e3-396">Stellentypen</span><span class="sxs-lookup"><span data-stu-id="054e3-396">Job types</span></span>

<span data-ttu-id="054e3-397">Stellentypen werden verwendet, um ähnliche Stellen in Kategorien zu gruppieren.</span><span class="sxs-lookup"><span data-stu-id="054e3-397">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="054e3-398">Stellentypen sind erforderlich, damit Lohn in den USA und Kanada zu bearbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="054e3-398">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="054e3-399">Beispiele für Stellentypen umfassen Voll- und Teilzeit oder festes Gehalt und Stundenlohn.</span><span class="sxs-lookup"><span data-stu-id="054e3-399">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="054e3-400">Stellentypen werden Dayforce als Lohnarten zugeordnet, die angeben, ob ein Mitarbeiter auf Stundenbasis bezahlt wird oder ein festes Gehalt bezieht.</span><span class="sxs-lookup"><span data-stu-id="054e3-400">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="054e3-401">Folgende Stellentypen und Beschreibungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="054e3-401">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="054e3-402">Stellentyp</span><span class="sxs-lookup"><span data-stu-id="054e3-402">Job type</span></span>   | <span data-ttu-id="054e3-403">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="054e3-403">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="054e3-404">Stündlich</span><span class="sxs-lookup"><span data-stu-id="054e3-404">Hourly</span></span>     | <span data-ttu-id="054e3-405">Stündlich</span><span class="sxs-lookup"><span data-stu-id="054e3-405">Hourly</span></span>      |
| <span data-ttu-id="054e3-406">Fest angestellt</span><span class="sxs-lookup"><span data-stu-id="054e3-406">Salaried</span></span>   | <span data-ttu-id="054e3-407">Fest angestellt</span><span class="sxs-lookup"><span data-stu-id="054e3-407">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="054e3-408">Positionstypen</span><span class="sxs-lookup"><span data-stu-id="054e3-408">Position types</span></span> 

<span data-ttu-id="054e3-409">Sie verwenden Positionstypen, um zu beschreiben, ob die Position Vollzeit, Teilzeit oder etwas anderes ist.</span><span class="sxs-lookup"><span data-stu-id="054e3-409">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="054e3-410">Positionstypen werden Dayforce als Lohnklassen zugeordnet, die angeben, ob ein Mitarbeiter in Vollzeit oder Teilzeit arbeitet.</span><span class="sxs-lookup"><span data-stu-id="054e3-410">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="054e3-411">Folgende Positionstypen und Beschreibungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="054e3-411">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="054e3-412">Positionstyp</span><span class="sxs-lookup"><span data-stu-id="054e3-412">Position type</span></span>   | <span data-ttu-id="054e3-413">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="054e3-413">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="054e3-414">Vollzeit</span><span class="sxs-lookup"><span data-stu-id="054e3-414">Full-time</span></span>       | <span data-ttu-id="054e3-415">Vollzeitmitarbeiter</span><span class="sxs-lookup"><span data-stu-id="054e3-415">Full time employee</span></span> |
| <span data-ttu-id="054e3-416">Teilzeit</span><span class="sxs-lookup"><span data-stu-id="054e3-416">Part-time</span></span>       | <span data-ttu-id="054e3-417">Teilzeitmitarbeiter</span><span class="sxs-lookup"><span data-stu-id="054e3-417">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="054e3-418">Ursachencodes</span><span class="sxs-lookup"><span data-stu-id="054e3-418">Reason codes</span></span>

<span data-ttu-id="054e3-419">Ursachencodes enthalten Informationen zum Status eines Mitarbeiters.</span><span class="sxs-lookup"><span data-stu-id="054e3-419">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="054e3-420">Ursachencodes werden Dayforce als Statusgründe zugeordnet, die den Grund für Änderungen bei der Position eines Mitarbeiters oder dem Beschäftigungsstatus angeben.</span><span class="sxs-lookup"><span data-stu-id="054e3-420">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="054e3-421">Folgende Ursachencodes und Beschreibungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="054e3-421">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="054e3-422">Ursachencode</span><span class="sxs-lookup"><span data-stu-id="054e3-422">Reason code</span></span>    | <span data-ttu-id="054e3-423">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="054e3-423">Description</span></span>      | <span data-ttu-id="054e3-424">Zutreffende Szenarios</span><span class="sxs-lookup"><span data-stu-id="054e3-424">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="054e3-425">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="054e3-425">RESIGNATION</span></span>    | <span data-ttu-id="054e3-426">Kündigung durch Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="054e3-426">Resignation</span></span>      | <span data-ttu-id="054e3-427">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="054e3-427">Terminate worker</span></span>     |
| <span data-ttu-id="054e3-428">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="054e3-428">TERMINATION</span></span>    | <span data-ttu-id="054e3-429">Beendigung</span><span class="sxs-lookup"><span data-stu-id="054e3-429">Termination</span></span>      | <span data-ttu-id="054e3-430">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="054e3-430">Terminate worker</span></span>     |
| <span data-ttu-id="054e3-431">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="054e3-431">RETIREMENT</span></span>     | <span data-ttu-id="054e3-432">Ruhestand</span><span class="sxs-lookup"><span data-stu-id="054e3-432">Retirement</span></span>       | <span data-ttu-id="054e3-433">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="054e3-433">Terminate worker</span></span>     |
| <span data-ttu-id="054e3-434">OTHER</span><span class="sxs-lookup"><span data-stu-id="054e3-434">OTHER</span></span>          | <span data-ttu-id="054e3-435">Andere Gründe</span><span class="sxs-lookup"><span data-stu-id="054e3-435">Other Reasons</span></span>    | <span data-ttu-id="054e3-436">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="054e3-436">Terminate worker</span></span>     |
| <span data-ttu-id="054e3-437">DEATH</span><span class="sxs-lookup"><span data-stu-id="054e3-437">DEATH</span></span>          | <span data-ttu-id="054e3-438">Tod</span><span class="sxs-lookup"><span data-stu-id="054e3-438">Death</span></span>            | <span data-ttu-id="054e3-439">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="054e3-439">Terminate worker</span></span>     |
| <span data-ttu-id="054e3-440">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="054e3-440">LEAVEOFABSENCE</span></span> | <span data-ttu-id="054e3-441">Beurlaubung</span><span class="sxs-lookup"><span data-stu-id="054e3-441">Leave of Absence</span></span> | <span data-ttu-id="054e3-442">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="054e3-442">Terminate worker</span></span>     |
| <span data-ttu-id="054e3-443">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="054e3-443">CONTRACTEND</span></span>    | <span data-ttu-id="054e3-444">Vertragsende</span><span class="sxs-lookup"><span data-stu-id="054e3-444">End of Contract</span></span>  | <span data-ttu-id="054e3-445">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="054e3-445">Terminate worker</span></span>     |
| <span data-ttu-id="054e3-446">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="054e3-446">SALARYCHANGE</span></span>   | <span data-ttu-id="054e3-447">Gehaltsänderung</span><span class="sxs-lookup"><span data-stu-id="054e3-447">Change of Salary</span></span> | <span data-ttu-id="054e3-448">Vergütung</span><span class="sxs-lookup"><span data-stu-id="054e3-448">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="054e3-449">Familienstand</span><span class="sxs-lookup"><span data-stu-id="054e3-449">Marital status</span></span>

<span data-ttu-id="054e3-450">Familienstandwerte werden Dayforce zugeordnet und werden – je nach Bedarf – in die akzeptierten Werte bei der Integration übersetzt.</span><span class="sxs-lookup"><span data-stu-id="054e3-450">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="054e3-451">Die folgende Tabelle zeigt, wie Familienstandwerte Dayforce zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="054e3-451">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="054e3-452">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="054e3-452">Human Resources</span></span>                 | <span data-ttu-id="054e3-453">Dayforce</span><span class="sxs-lookup"><span data-stu-id="054e3-453">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="054e3-454">Verheiratet</span><span class="sxs-lookup"><span data-stu-id="054e3-454">Married</span></span>                | <span data-ttu-id="054e3-455">Verheiratet</span><span class="sxs-lookup"><span data-stu-id="054e3-455">Married</span></span>              |
| <span data-ttu-id="054e3-456">Ledig</span><span class="sxs-lookup"><span data-stu-id="054e3-456">Single</span></span>                 | <span data-ttu-id="054e3-457">Ledig</span><span class="sxs-lookup"><span data-stu-id="054e3-457">Single</span></span>               |
| <span data-ttu-id="054e3-458">Verwitwet</span><span class="sxs-lookup"><span data-stu-id="054e3-458">Widowed</span></span>                | <span data-ttu-id="054e3-459">Verwitwet</span><span class="sxs-lookup"><span data-stu-id="054e3-459">Widowed</span></span>              |
| <span data-ttu-id="054e3-460">Geschieden</span><span class="sxs-lookup"><span data-stu-id="054e3-460">Divorced</span></span>               | <span data-ttu-id="054e3-461">Geschieden</span><span class="sxs-lookup"><span data-stu-id="054e3-461">Divorced</span></span>             |
| <span data-ttu-id="054e3-462">Eingetragene Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="054e3-462">Registered Partnership</span></span> | <span data-ttu-id="054e3-463">Inländische Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="054e3-463">Domestic Partnership</span></span> |
| <span data-ttu-id="054e3-464">None</span><span class="sxs-lookup"><span data-stu-id="054e3-464">None</span></span>                   | <span data-ttu-id="054e3-465">None</span><span class="sxs-lookup"><span data-stu-id="054e3-465">None</span></span>                 |
| <span data-ttu-id="054e3-466">Freie Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="054e3-466">Cohabiting</span></span>             | <span data-ttu-id="054e3-467">Freie Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="054e3-467">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="054e3-468">Geschlecht</span><span class="sxs-lookup"><span data-stu-id="054e3-468">Gender</span></span>

<span data-ttu-id="054e3-469">Geschlechtsbezeichnungen werden Dayforce zugeordnet und werden – je nach Bedarf – in die akzeptierten Werte bei der Integration übersetzt.</span><span class="sxs-lookup"><span data-stu-id="054e3-469">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="054e3-470">Die folgende Tabelle zeigt, wie Geschlechtsbezeichnungen Dayforce zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="054e3-470">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="054e3-471">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="054e3-471">Human Resources</span></span>       | <span data-ttu-id="054e3-472">Dayforce</span><span class="sxs-lookup"><span data-stu-id="054e3-472">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="054e3-473">Männl.</span><span class="sxs-lookup"><span data-stu-id="054e3-473">Male</span></span>         | <span data-ttu-id="054e3-474">Männl.</span><span class="sxs-lookup"><span data-stu-id="054e3-474">Male</span></span>            |
| <span data-ttu-id="054e3-475">Weibl.</span><span class="sxs-lookup"><span data-stu-id="054e3-475">Female</span></span>       | <span data-ttu-id="054e3-476">Weibl.</span><span class="sxs-lookup"><span data-stu-id="054e3-476">Female</span></span>          |
| <span data-ttu-id="054e3-477">Nicht spezifisch</span><span class="sxs-lookup"><span data-stu-id="054e3-477">Non-specific</span></span> | <span data-ttu-id="054e3-478">*Nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="054e3-478">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="054e3-479">Einkommenscodes</span><span class="sxs-lookup"><span data-stu-id="054e3-479">Earning codes</span></span>

<span data-ttu-id="054e3-480">Einkommenscodes bestimmen jeden Typ von Einkünften eindeutig, die Arbeitskräfte erhalten</span><span class="sxs-lookup"><span data-stu-id="054e3-480">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="054e3-481">Die Codes decken verschiedene Parameter ab, die sich auf Einkünfte beziehen, wie beispielsweise Buchhaltungsvorschriften, Steuergesetze, Berichterstellungsanforderungen und Bruttoausgleichsfähigkeit.</span><span class="sxs-lookup"><span data-stu-id="054e3-481">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="054e3-482">Wenn eine nicht unterstützte Häufigkeit verwendet wird, wird die Häufigkeit **Jeder Lohn** standardmäßig für die Berechnung verwendet.</span><span class="sxs-lookup"><span data-stu-id="054e3-482">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="054e3-483">Unterstützte Häufigkeiten</span><span class="sxs-lookup"><span data-stu-id="054e3-483">Supported frequencies</span></span>

- <span data-ttu-id="054e3-484">Alle</span><span class="sxs-lookup"><span data-stu-id="054e3-484">All</span></span>
- <span data-ttu-id="054e3-485">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="054e3-485">EVERYPAY</span></span>
- <span data-ttu-id="054e3-486">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="054e3-486">EACHPAYPERIOD</span></span>
- <span data-ttu-id="054e3-487">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="054e3-487">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="054e3-488">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="054e3-488">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="054e3-489">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="054e3-489">1OFMTH</span></span>
- <span data-ttu-id="054e3-490">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="054e3-490">LASTOFMTH</span></span>
- <span data-ttu-id="054e3-491">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="054e3-491">2OFMTH</span></span>
- <span data-ttu-id="054e3-492">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="054e3-492">3OFMTH</span></span>
- <span data-ttu-id="054e3-493">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="054e3-493">4OFMTH</span></span>
- <span data-ttu-id="054e3-494">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="054e3-494">5OFMTH</span></span>
- <span data-ttu-id="054e3-495">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="054e3-495">1N2OFMTH</span></span>
- <span data-ttu-id="054e3-496">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="054e3-496">3N4OFMTH</span></span>
- <span data-ttu-id="054e3-497">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="054e3-497">1N3OFMTH</span></span>
- <span data-ttu-id="054e3-498">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="054e3-498">1N4OFMTH</span></span>
- <span data-ttu-id="054e3-499">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="054e3-499">2N3OFMTH</span></span>
- <span data-ttu-id="054e3-500">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="054e3-500">2N4OFMTH</span></span>
- <span data-ttu-id="054e3-501">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="054e3-501">1N2N3OFMTH</span></span>
- <span data-ttu-id="054e3-502">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="054e3-502">1N2N4OFMTH</span></span>
- <span data-ttu-id="054e3-503">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="054e3-503">1N3N4OFMTH</span></span>
- <span data-ttu-id="054e3-504">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="054e3-504">2N3N4OFMTH</span></span>
- <span data-ttu-id="054e3-505">1N2N3N4OFMTH – 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="054e3-505">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="054e3-506">2N3N4N5OFMth – 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="054e3-506">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="054e3-507">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="054e3-507">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="054e3-508">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="054e3-508">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="054e3-509">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="054e3-509">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="054e3-510">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="054e3-510">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="054e3-511">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="054e3-511">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="054e3-512">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="054e3-512">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="054e3-513">Adressen</span><span class="sxs-lookup"><span data-stu-id="054e3-513">Addresses</span></span>

<span data-ttu-id="054e3-514">Die Kennung bestimmter Codes für Land oder Region, Bundesland/Kanton oder Landkreis (Gemeinde) erfordert spezifische Formate, die Dayforce und Anbieter innerhalb des Landes/innerhalb der Region erkennen können.</span><span class="sxs-lookup"><span data-stu-id="054e3-514">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="054e3-515">Obwohl das Format für Orte flexibel ist, muss jeder Ort einem Bundesland zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="054e3-515">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="054e3-516">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="054e3-516">Human Resources</span></span>          | <span data-ttu-id="054e3-517">Dayforce</span><span class="sxs-lookup"><span data-stu-id="054e3-517">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="054e3-518">Land/Region</span><span class="sxs-lookup"><span data-stu-id="054e3-518">Country/Region</span></span>  | <span data-ttu-id="054e3-519">Ländercode</span><span class="sxs-lookup"><span data-stu-id="054e3-519">Country Code</span></span>          |
| <span data-ttu-id="054e3-520">Postleitzahl</span><span class="sxs-lookup"><span data-stu-id="054e3-520">Zip/Postal Code</span></span> | <span data-ttu-id="054e3-521">PLZ</span><span class="sxs-lookup"><span data-stu-id="054e3-521">Postal Code</span></span>           |
| <span data-ttu-id="054e3-522">Zustand</span><span class="sxs-lookup"><span data-stu-id="054e3-522">State</span></span>           | <span data-ttu-id="054e3-523">Bundeslandcode</span><span class="sxs-lookup"><span data-stu-id="054e3-523">State Code</span></span>            |
| <span data-ttu-id="054e3-524">Stadt</span><span class="sxs-lookup"><span data-stu-id="054e3-524">City</span></span>            | <span data-ttu-id="054e3-525">Stadt</span><span class="sxs-lookup"><span data-stu-id="054e3-525">City</span></span>                  |
| <span data-ttu-id="054e3-526">Verwaltungsbezirk</span><span class="sxs-lookup"><span data-stu-id="054e3-526">County</span></span>          | <span data-ttu-id="054e3-527">Landkreis (Gemeinde)</span><span class="sxs-lookup"><span data-stu-id="054e3-527">County (Municipality)</span></span> |
| <span data-ttu-id="054e3-528">Straße</span><span class="sxs-lookup"><span data-stu-id="054e3-528">Street</span></span>          | <span data-ttu-id="054e3-529">Adresszeile 1</span><span class="sxs-lookup"><span data-stu-id="054e3-529">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="054e3-530">Steuerregionen</span><span class="sxs-lookup"><span data-stu-id="054e3-530">Tax regions</span></span>

<span data-ttu-id="054e3-531">Steuerregionen werden verwendet, um die entsprechende Steuer festzulegen, die bei der Lohngenerierung angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="054e3-531">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="054e3-532">Steuerregionen werden Dayforce als Standortadressen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="054e3-532">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="054e3-533">Die Standardsteuerregion muss der aktiven Position der Arbeitskraft zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="054e3-533">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="054e3-534">Steuerregion (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-534">Tax region (required)</span></span>
- <span data-ttu-id="054e3-535">Land/Region (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-535">Country/Region (required)</span></span>
- <span data-ttu-id="054e3-536">Bundesland/Kanton (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-536">State (required)</span></span>
- <span data-ttu-id="054e3-537">Verwaltungsbezirk</span><span class="sxs-lookup"><span data-stu-id="054e3-537">County</span></span> 
- <span data-ttu-id="054e3-538">Ort (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="054e3-538">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="054e3-539">Konfigurieren Ihrer Daten, um Lohn in Mexiko zu generieren</span><span class="sxs-lookup"><span data-stu-id="054e3-539">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="054e3-540">Wenn Sie Vergütung für Mitarbeiter in Mexiko generieren, müssen die folgenden Elemente konfiguriert werden:</span><span class="sxs-lookup"><span data-stu-id="054e3-540">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="054e3-541">Abteilungen sind für Positionen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="054e3-541">Departments are required on positions.</span></span>
- <span data-ttu-id="054e3-542">Kostenstellen müssen als Finanzdimensionen festgelegt werden und müssen das erste Element in der standardmäßigen Finanzdimensions-Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="054e3-542">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="054e3-543">Stellentypen</span><span class="sxs-lookup"><span data-stu-id="054e3-543">Job types</span></span>

<span data-ttu-id="054e3-544">Stellentypen werden verwendet, um ähnliche Stellen in Kategorien zu gruppieren.</span><span class="sxs-lookup"><span data-stu-id="054e3-544">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="054e3-545">Stellentypen sind erforderlich, um Lohn in Mexiko zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="054e3-545">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="054e3-546">Beispiele für Stellentypen umfassen Voll- und Teilzeit oder festes Gehalt und Stundenlohn.</span><span class="sxs-lookup"><span data-stu-id="054e3-546">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="054e3-547">Stellentypen werden Dayforce als Lohnarten zugeordnet, die angeben, ob ein Mitarbeiter auf Stundenbasis bezahlt wird oder ein festes Gehalt bezieht.</span><span class="sxs-lookup"><span data-stu-id="054e3-547">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="054e3-548">Folgende Stellentypen und Beschreibungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="054e3-548">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="054e3-549">Stellentyp</span><span class="sxs-lookup"><span data-stu-id="054e3-549">Job type</span></span>   | <span data-ttu-id="054e3-550">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="054e3-550">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="054e3-551">Stündlich</span><span class="sxs-lookup"><span data-stu-id="054e3-551">Hourly</span></span>     | <span data-ttu-id="054e3-552">MX – Stundenbasis</span><span class="sxs-lookup"><span data-stu-id="054e3-552">MX Hourly</span></span>   |
| <span data-ttu-id="054e3-553">Fest angestellt</span><span class="sxs-lookup"><span data-stu-id="054e3-553">Salaried</span></span>   | <span data-ttu-id="054e3-554">MX – Fest angestellt</span><span class="sxs-lookup"><span data-stu-id="054e3-554">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="054e3-555">Positionstypen</span><span class="sxs-lookup"><span data-stu-id="054e3-555">Position types</span></span> 

<span data-ttu-id="054e3-556">Sie verwenden Positionstypen, um zu beschreiben, ob die Position Vollzeit, Teilzeit oder etwas anderes ist.</span><span class="sxs-lookup"><span data-stu-id="054e3-556">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="054e3-557">Positionstypen werden Dayforce als Lohnklassen zugeordnet, die angeben, ob ein Mitarbeiter in Vollzeit oder Teilzeit arbeitet.</span><span class="sxs-lookup"><span data-stu-id="054e3-557">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="054e3-558">Folgende Positionstypen und Beschreibungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="054e3-558">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="054e3-559">Positionstyp</span><span class="sxs-lookup"><span data-stu-id="054e3-559">Position type</span></span>   | <span data-ttu-id="054e3-560">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="054e3-560">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="054e3-561">Vollzeit</span><span class="sxs-lookup"><span data-stu-id="054e3-561">Full-time</span></span>       | <span data-ttu-id="054e3-562">Vollzeitmitarbeiter</span><span class="sxs-lookup"><span data-stu-id="054e3-562">Full time employee</span></span> |
| <span data-ttu-id="054e3-563">Teilzeit</span><span class="sxs-lookup"><span data-stu-id="054e3-563">Part-time</span></span>       | <span data-ttu-id="054e3-564">Teilzeitmitarbeiter</span><span class="sxs-lookup"><span data-stu-id="054e3-564">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="054e3-565">Ursachencodes</span><span class="sxs-lookup"><span data-stu-id="054e3-565">Reason codes</span></span>

<span data-ttu-id="054e3-566">Ursachencodes enthalten Informationen zum Status eines Mitarbeiters.</span><span class="sxs-lookup"><span data-stu-id="054e3-566">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="054e3-567">Ursachencodes werden Dayforce als Statusgründe zugeordnet, die den Grund für Änderungen bei der Position eines Mitarbeiters oder dem Beschäftigungsstatus angeben.</span><span class="sxs-lookup"><span data-stu-id="054e3-567">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="054e3-568">Folgende Ursachencodes und Beschreibungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="054e3-568">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="054e3-569">Ursachencode</span><span class="sxs-lookup"><span data-stu-id="054e3-569">Reason code</span></span>            | <span data-ttu-id="054e3-570">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="054e3-570">Description</span></span>                    | <span data-ttu-id="054e3-571">Zutreffende Szenarios</span><span class="sxs-lookup"><span data-stu-id="054e3-571">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="054e3-572">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="054e3-572">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="054e3-573">Abgang vor erster Lohnzahlung</span><span class="sxs-lookup"><span data-stu-id="054e3-573">Departure before first payroll</span></span> | <span data-ttu-id="054e3-574">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="054e3-574">Terminate worker</span></span>     |
| <span data-ttu-id="054e3-575">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="054e3-575">RESIGNATION</span></span>            | <span data-ttu-id="054e3-576">Kündigung durch Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="054e3-576">Resignation</span></span>                    | <span data-ttu-id="054e3-577">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="054e3-577">Terminate worker</span></span>     |
| <span data-ttu-id="054e3-578">PENSION</span><span class="sxs-lookup"><span data-stu-id="054e3-578">PENSION</span></span>                | <span data-ttu-id="054e3-579">Rente</span><span class="sxs-lookup"><span data-stu-id="054e3-579">Pension</span></span>                        | <span data-ttu-id="054e3-580">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="054e3-580">Terminate worker</span></span>     |
| <span data-ttu-id="054e3-581">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="054e3-581">TERMINATION</span></span>            | <span data-ttu-id="054e3-582">Beendigung</span><span class="sxs-lookup"><span data-stu-id="054e3-582">Termination</span></span>                    | <span data-ttu-id="054e3-583">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="054e3-583">Terminate worker</span></span>     |
| <span data-ttu-id="054e3-584">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="054e3-584">RETIREMENT</span></span>             | <span data-ttu-id="054e3-585">Ruhestand</span><span class="sxs-lookup"><span data-stu-id="054e3-585">Retirement</span></span>                     | <span data-ttu-id="054e3-586">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="054e3-586">Terminate worker</span></span>     |
| <span data-ttu-id="054e3-587">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="054e3-587">ABSENTEE</span></span>               | <span data-ttu-id="054e3-588">Abwesende Person</span><span class="sxs-lookup"><span data-stu-id="054e3-588">Absentee</span></span>                       | <span data-ttu-id="054e3-589">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="054e3-589">Terminate worker</span></span>     |
| <span data-ttu-id="054e3-590">OTHER</span><span class="sxs-lookup"><span data-stu-id="054e3-590">OTHER</span></span>                  | <span data-ttu-id="054e3-591">Andere Gründe</span><span class="sxs-lookup"><span data-stu-id="054e3-591">Other Reasons</span></span>                  | <span data-ttu-id="054e3-592">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="054e3-592">Terminate worker</span></span>     |
| <span data-ttu-id="054e3-593">CLOSURE</span><span class="sxs-lookup"><span data-stu-id="054e3-593">CLOSURE</span></span>                | <span data-ttu-id="054e3-594">Betriebsferien</span><span class="sxs-lookup"><span data-stu-id="054e3-594">Business Closure</span></span>               | <span data-ttu-id="054e3-595">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="054e3-595">Terminate worker</span></span>     |
| <span data-ttu-id="054e3-596">DEATH</span><span class="sxs-lookup"><span data-stu-id="054e3-596">DEATH</span></span>                  | <span data-ttu-id="054e3-597">Tod</span><span class="sxs-lookup"><span data-stu-id="054e3-597">Death</span></span>                          | <span data-ttu-id="054e3-598">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="054e3-598">Terminate worker</span></span>     |
| <span data-ttu-id="054e3-599">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="054e3-599">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="054e3-600">Beurlaubung</span><span class="sxs-lookup"><span data-stu-id="054e3-600">Leave of Absence</span></span>               | <span data-ttu-id="054e3-601">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="054e3-601">Terminate worker</span></span>     |
| <span data-ttu-id="054e3-602">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="054e3-602">CONTRACTEND</span></span>            | <span data-ttu-id="054e3-603">Vertragsende</span><span class="sxs-lookup"><span data-stu-id="054e3-603">End of Contract</span></span>                | <span data-ttu-id="054e3-604">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="054e3-604">Terminate worker</span></span>     |
| <span data-ttu-id="054e3-605">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="054e3-605">SALARYCHANGE</span></span>           | <span data-ttu-id="054e3-606">Gehaltsänderung</span><span class="sxs-lookup"><span data-stu-id="054e3-606">Change of Salary</span></span>               | <span data-ttu-id="054e3-607">Vergütung</span><span class="sxs-lookup"><span data-stu-id="054e3-607">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="054e3-608">Einstellungsbedingungen</span><span class="sxs-lookup"><span data-stu-id="054e3-608">Terms of employment</span></span>

<span data-ttu-id="054e3-609">Beschäftigungsbedingungen werden verwendet, um Kategorien von Beschäftigungsbedingungen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="054e3-609">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="054e3-610">Die Bedingungen werden Dayforce als Beschäftigungsindikatorwerte zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="054e3-610">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="054e3-611">Die folgenden Bedingungen für Beschäftigung und Beschreibungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="054e3-611">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="054e3-612">Einstellungsbedingungen</span><span class="sxs-lookup"><span data-stu-id="054e3-612">Terms of employment</span></span>   | <span data-ttu-id="054e3-613">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="054e3-613">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="054e3-614">Regelmäßig</span><span class="sxs-lookup"><span data-stu-id="054e3-614">Regular</span></span>               | <span data-ttu-id="054e3-615">Regelmäßig</span><span class="sxs-lookup"><span data-stu-id="054e3-615">Regular</span></span>     |
| <span data-ttu-id="054e3-616">Direkt</span><span class="sxs-lookup"><span data-stu-id="054e3-616">Direct</span></span>                | <span data-ttu-id="054e3-617">Direkt</span><span class="sxs-lookup"><span data-stu-id="054e3-617">Direct</span></span>      |
| <span data-ttu-id="054e3-618">Praktikum</span><span class="sxs-lookup"><span data-stu-id="054e3-618">Internship</span></span>            | <span data-ttu-id="054e3-619">Praktikum</span><span class="sxs-lookup"><span data-stu-id="054e3-619">Internship</span></span>  |
| <span data-ttu-id="054e3-620">Unbefristet</span><span class="sxs-lookup"><span data-stu-id="054e3-620">Permanent</span></span>             | <span data-ttu-id="054e3-621">Unbefristet</span><span class="sxs-lookup"><span data-stu-id="054e3-621">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="054e3-622">Familienstand</span><span class="sxs-lookup"><span data-stu-id="054e3-622">Marital status</span></span>

<span data-ttu-id="054e3-623">Familienstandwerte werden Dayforce zugeordnet und werden – je nach Bedarf – in die akzeptierten Werte bei der Integration übersetzt.</span><span class="sxs-lookup"><span data-stu-id="054e3-623">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="054e3-624">Die folgende Tabelle zeigt, wie Familienstandwerte Dayforce zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="054e3-624">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="054e3-625">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="054e3-625">Human Resources</span></span>                 | <span data-ttu-id="054e3-626">Dayforce</span><span class="sxs-lookup"><span data-stu-id="054e3-626">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="054e3-627">Verheiratet</span><span class="sxs-lookup"><span data-stu-id="054e3-627">Married</span></span>                | <span data-ttu-id="054e3-628">Verheiratet</span><span class="sxs-lookup"><span data-stu-id="054e3-628">Married</span></span>                   |
| <span data-ttu-id="054e3-629">Ledig</span><span class="sxs-lookup"><span data-stu-id="054e3-629">Single</span></span>                 | <span data-ttu-id="054e3-630">Ledig</span><span class="sxs-lookup"><span data-stu-id="054e3-630">Single</span></span>                    |
| <span data-ttu-id="054e3-631">Verwitwet</span><span class="sxs-lookup"><span data-stu-id="054e3-631">Widowed</span></span>                | <span data-ttu-id="054e3-632">Verwitwet</span><span class="sxs-lookup"><span data-stu-id="054e3-632">Widowed</span></span>                   |
| <span data-ttu-id="054e3-633">Geschieden</span><span class="sxs-lookup"><span data-stu-id="054e3-633">Divorced</span></span>               | <span data-ttu-id="054e3-634">Geschieden</span><span class="sxs-lookup"><span data-stu-id="054e3-634">Divorced</span></span>                  |
| <span data-ttu-id="054e3-635">Eingetragene Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="054e3-635">Registered Partnership</span></span> | <span data-ttu-id="054e3-636">Inländische Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="054e3-636">Domestic Partnership</span></span>      |
| <span data-ttu-id="054e3-637">None</span><span class="sxs-lookup"><span data-stu-id="054e3-637">None</span></span>                   | <span data-ttu-id="054e3-638">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="054e3-638">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="054e3-639">Freie Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="054e3-639">Cohabiting</span></span>             | <span data-ttu-id="054e3-640">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="054e3-640">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="054e3-641">Geschlecht</span><span class="sxs-lookup"><span data-stu-id="054e3-641">Gender</span></span>

<span data-ttu-id="054e3-642">Geschlechtsbezeichnungen werden Dayforce zugeordnet und werden – je nach Bedarf – in die akzeptierten Werte bei der Integration übersetzt.</span><span class="sxs-lookup"><span data-stu-id="054e3-642">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="054e3-643">Die folgende Tabelle zeigt, wie Geschlechtsbezeichnungen Dayforce zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="054e3-643">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="054e3-644">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="054e3-644">Human Resources</span></span>       | <span data-ttu-id="054e3-645">Dayforce</span><span class="sxs-lookup"><span data-stu-id="054e3-645">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="054e3-646">Männl.</span><span class="sxs-lookup"><span data-stu-id="054e3-646">Male</span></span>         | <span data-ttu-id="054e3-647">Männl.</span><span class="sxs-lookup"><span data-stu-id="054e3-647">Male</span></span>                      |
| <span data-ttu-id="054e3-648">Weibl.</span><span class="sxs-lookup"><span data-stu-id="054e3-648">Female</span></span>       | <span data-ttu-id="054e3-649">Weibl.</span><span class="sxs-lookup"><span data-stu-id="054e3-649">Female</span></span>                    |
| <span data-ttu-id="054e3-650">Nicht spezifisch</span><span class="sxs-lookup"><span data-stu-id="054e3-650">Non-specific</span></span> | <span data-ttu-id="054e3-651">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="054e3-651">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="054e3-652">Zahlungsweise</span><span class="sxs-lookup"><span data-stu-id="054e3-652">Payment method</span></span>

<span data-ttu-id="054e3-653">Zahlungsmethoden geben dem Mitarbeiter und dem Unternehmen die Möglichkeit zu beschreiben, wie Mitarbeiter bezahlt werden.</span><span class="sxs-lookup"><span data-stu-id="054e3-653">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="054e3-654">Zahlungsmethoden werden Dayforce zugeordnet und werden – je nach Bedarf – in die akzeptierten Werte bei der Integration übersetzt.</span><span class="sxs-lookup"><span data-stu-id="054e3-654">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="054e3-655">Die folgende Tabelle zeigt, wie Zahlungsmethoden Dayforce zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="054e3-655">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="054e3-656">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="054e3-656">Human Resources</span></span>             | <span data-ttu-id="054e3-657">Dayforce</span><span class="sxs-lookup"><span data-stu-id="054e3-657">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="054e3-658">Bargeld</span><span class="sxs-lookup"><span data-stu-id="054e3-658">Cash</span></span>               | <span data-ttu-id="054e3-659">Bargeld</span><span class="sxs-lookup"><span data-stu-id="054e3-659">Cash</span></span>                      |
| <span data-ttu-id="054e3-660">Elektronische Zahlung</span><span class="sxs-lookup"><span data-stu-id="054e3-660">Electronic Payment</span></span> | <span data-ttu-id="054e3-661">Übertragen</span><span class="sxs-lookup"><span data-stu-id="054e3-661">Transfer</span></span>                  |
| <span data-ttu-id="054e3-662">Prüfen</span><span class="sxs-lookup"><span data-stu-id="054e3-662">Check</span></span>              | <span data-ttu-id="054e3-663">Scheck</span><span class="sxs-lookup"><span data-stu-id="054e3-663">Cheque</span></span>                    |
| <span data-ttu-id="054e3-664">Bankwechsel</span><span class="sxs-lookup"><span data-stu-id="054e3-664">Bank Draft</span></span>         | <span data-ttu-id="054e3-665">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="054e3-665">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="054e3-666">Sonstige</span><span class="sxs-lookup"><span data-stu-id="054e3-666">Other</span></span>              | <span data-ttu-id="054e3-667">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="054e3-667">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="054e3-668">Bankkontotyp</span><span class="sxs-lookup"><span data-stu-id="054e3-668">Bank account type</span></span>

<span data-ttu-id="054e3-669">Bankkontotypen werden für elektronische Zahlungen an Mitarbeiter verwendet.</span><span class="sxs-lookup"><span data-stu-id="054e3-669">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="054e3-670">Bankkontotypen werden Dayforce als Übergweisungskontoinformationen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="054e3-670">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="054e3-671">Die Bankkontotypen werden bei Bedarf zu den akzeptierten Werte nach der Integration übersetzt.</span><span class="sxs-lookup"><span data-stu-id="054e3-671">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="054e3-672">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="054e3-672">Human Resources</span></span>            | <span data-ttu-id="054e3-673">Dayforce</span><span class="sxs-lookup"><span data-stu-id="054e3-673">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="054e3-674">Girokonto</span><span class="sxs-lookup"><span data-stu-id="054e3-674">Checking Account</span></span>  | <span data-ttu-id="054e3-675">Girokonto</span><span class="sxs-lookup"><span data-stu-id="054e3-675">CheckingAccount</span></span>           |
| <span data-ttu-id="054e3-676">Lohnkonto</span><span class="sxs-lookup"><span data-stu-id="054e3-676">Payroll Account</span></span>   | <span data-ttu-id="054e3-677">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="054e3-677">PayrollAccount</span></span>            |
| <span data-ttu-id="054e3-678">Sparkonto</span><span class="sxs-lookup"><span data-stu-id="054e3-678">Savings Account</span></span>   | <span data-ttu-id="054e3-679">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="054e3-679">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="054e3-680">BankGirot-Konto</span><span class="sxs-lookup"><span data-stu-id="054e3-680">BankGirot account</span></span> | <span data-ttu-id="054e3-681">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="054e3-681">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="054e3-682">PlusGirot-Konto</span><span class="sxs-lookup"><span data-stu-id="054e3-682">PlusGirot account</span></span> | <span data-ttu-id="054e3-683">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="054e3-683">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="054e3-684">Einkommenscodes</span><span class="sxs-lookup"><span data-stu-id="054e3-684">Earning codes</span></span>

<span data-ttu-id="054e3-685">Einkommenscodes bestimmen jeden Typ von Einkünften eindeutig, die Arbeitskräfte erhalten</span><span class="sxs-lookup"><span data-stu-id="054e3-685">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="054e3-686">Die Codes decken verschiedene Parameter ab, die sich auf Einkünfte beziehen, wie beispielsweise Buchhaltungsvorschriften, Steuergesetze, Berichterstellungsanforderungen und Bruttoausgleichsfähigkeit.</span><span class="sxs-lookup"><span data-stu-id="054e3-686">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="054e3-687">Wenn eine nicht unterstützte Häufigkeit verwendet wird, wird die Häufigkeit **Jeder Lohn** standardmäßig für die Berechnung verwendet.</span><span class="sxs-lookup"><span data-stu-id="054e3-687">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="054e3-688">Unterstützte Häufigkeiten</span><span class="sxs-lookup"><span data-stu-id="054e3-688">Supported frequencies</span></span>

- <span data-ttu-id="054e3-689">Alle</span><span class="sxs-lookup"><span data-stu-id="054e3-689">All</span></span>
- <span data-ttu-id="054e3-690">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="054e3-690">EVERYPAY</span></span>
- <span data-ttu-id="054e3-691">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="054e3-691">EACHPAYPERIOD</span></span>
- <span data-ttu-id="054e3-692">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="054e3-692">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="054e3-693">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="054e3-693">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="054e3-694">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="054e3-694">1OFMTH</span></span>
- <span data-ttu-id="054e3-695">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="054e3-695">LASTOFMTH</span></span>
- <span data-ttu-id="054e3-696">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="054e3-696">2OFMTH</span></span>
- <span data-ttu-id="054e3-697">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="054e3-697">3OFMTH</span></span>
- <span data-ttu-id="054e3-698">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="054e3-698">4OFMTH</span></span>
- <span data-ttu-id="054e3-699">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="054e3-699">5OFMTH</span></span>
- <span data-ttu-id="054e3-700">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="054e3-700">1N2OFMTH</span></span>
- <span data-ttu-id="054e3-701">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="054e3-701">3N4OFMTH</span></span>
- <span data-ttu-id="054e3-702">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="054e3-702">1N3OFMTH</span></span>
- <span data-ttu-id="054e3-703">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="054e3-703">1N4OFMTH</span></span>
- <span data-ttu-id="054e3-704">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="054e3-704">2N3OFMTH</span></span>
- <span data-ttu-id="054e3-705">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="054e3-705">2N4OFMTH</span></span>
- <span data-ttu-id="054e3-706">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="054e3-706">1N2N3OFMTH</span></span>
- <span data-ttu-id="054e3-707">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="054e3-707">1N2N4OFMTH</span></span>
- <span data-ttu-id="054e3-708">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="054e3-708">1N3N4OFMTH</span></span>
- <span data-ttu-id="054e3-709">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="054e3-709">2N3N4OFMTH</span></span>
- <span data-ttu-id="054e3-710">1N2N3N4OFMTH – 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="054e3-710">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="054e3-711">2N3N4N5OFMth – 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="054e3-711">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="054e3-712">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="054e3-712">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="054e3-713">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="054e3-713">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="054e3-714">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="054e3-714">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="054e3-715">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="054e3-715">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="054e3-716">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="054e3-716">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="054e3-717">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="054e3-717">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="054e3-718">Adressen</span><span class="sxs-lookup"><span data-stu-id="054e3-718">Addresses</span></span>

<span data-ttu-id="054e3-719">Die Kennung bestimmter Codes für Land oder Region, Bundesland/Kanton oder Landkreis (Gemeinde) erfordert spezifische Formate, die Dayforce und Anbieter innerhalb des Landes/innerhalb der Region erkennen können.</span><span class="sxs-lookup"><span data-stu-id="054e3-719">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="054e3-720">Obwohl das Format für Orte flexibel ist, muss jeder Ort einem Bundesland zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="054e3-720">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="054e3-721">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="054e3-721">Human Resources</span></span>              | <span data-ttu-id="054e3-722">Dayforce</span><span class="sxs-lookup"><span data-stu-id="054e3-722">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="054e3-723">Land/Region</span><span class="sxs-lookup"><span data-stu-id="054e3-723">Country/Region</span></span>      | <span data-ttu-id="054e3-724">Ländercode</span><span class="sxs-lookup"><span data-stu-id="054e3-724">Country Code</span></span>          |
| <span data-ttu-id="054e3-725">Postleitzahl</span><span class="sxs-lookup"><span data-stu-id="054e3-725">Zip/Postal Code</span></span>     | <span data-ttu-id="054e3-726">PLZ</span><span class="sxs-lookup"><span data-stu-id="054e3-726">Postal Code</span></span>           |
| <span data-ttu-id="054e3-727">Zustand</span><span class="sxs-lookup"><span data-stu-id="054e3-727">State</span></span>               | <span data-ttu-id="054e3-728">Bundeslandcode</span><span class="sxs-lookup"><span data-stu-id="054e3-728">State Code</span></span>            |
| <span data-ttu-id="054e3-729">Stadt</span><span class="sxs-lookup"><span data-stu-id="054e3-729">City</span></span>                | <span data-ttu-id="054e3-730">Stadt</span><span class="sxs-lookup"><span data-stu-id="054e3-730">City</span></span>                  |
| <span data-ttu-id="054e3-731">Verwaltungsbezirk</span><span class="sxs-lookup"><span data-stu-id="054e3-731">County</span></span>              | <span data-ttu-id="054e3-732">Landkreis (Gemeinde)</span><span class="sxs-lookup"><span data-stu-id="054e3-732">County (Municipality)</span></span> |
| <span data-ttu-id="054e3-733">Straße</span><span class="sxs-lookup"><span data-stu-id="054e3-733">Street</span></span>              | <span data-ttu-id="054e3-734">Adresszeile 1</span><span class="sxs-lookup"><span data-stu-id="054e3-734">Address Line 1</span></span>        |
| <span data-ttu-id="054e3-735">Hausnummer</span><span class="sxs-lookup"><span data-stu-id="054e3-735">Street Number</span></span>       | <span data-ttu-id="054e3-736">Adresszeile 2</span><span class="sxs-lookup"><span data-stu-id="054e3-736">Address Line 2</span></span>        |
| <span data-ttu-id="054e3-737">Gebäudeergänzung</span><span class="sxs-lookup"><span data-stu-id="054e3-737">Building Complement</span></span> | <span data-ttu-id="054e3-738">Adresszeile 5</span><span class="sxs-lookup"><span data-stu-id="054e3-738">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="054e3-739">Ausweisnummer</span><span class="sxs-lookup"><span data-stu-id="054e3-739">Passport number</span></span>

<span data-ttu-id="054e3-740">Mitarbeiter können Ausweisinformationen melden.</span><span class="sxs-lookup"><span data-stu-id="054e3-740">Employees can declare passport information.</span></span> <span data-ttu-id="054e3-741">Diese Informationen haben den Kennungstyp **Ausweis** und sind in Dayforce als Teil der für Mexiko spezifischen Informationen eines Mitarbeiters integriert.</span><span class="sxs-lookup"><span data-stu-id="054e3-741">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="054e3-742">Kennungstyp = „Ausweis”</span><span class="sxs-lookup"><span data-stu-id="054e3-742">Identification Type = "Passport"</span></span>
- <span data-ttu-id="054e3-743">Ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="054e3-743">Issued Date</span></span>
- <span data-ttu-id="054e3-744">Ablaufdatum</span><span class="sxs-lookup"><span data-stu-id="054e3-744">Expiration Date</span></span>

<span data-ttu-id="054e3-745">Mitarbeiter können mehrere Kennungsnummern des Kennungstyps **Ausweis** melden.</span><span class="sxs-lookup"><span data-stu-id="054e3-745">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="054e3-746">Jedoch wird nur der aktuell aktive Ausweiseintrag in Dayforce integriert.</span><span class="sxs-lookup"><span data-stu-id="054e3-746">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="054e3-747">Wenn alle Ausweiseinträge abgelaufen sind, ist der Ausweis, der zuletzt ausgestellt wurde, in Dayforce integriert.</span><span class="sxs-lookup"><span data-stu-id="054e3-747">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]