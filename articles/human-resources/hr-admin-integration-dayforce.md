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
ms.openlocfilehash: 1647b7fbf84a78051e745e918954df32a2e7e1dd
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890003"
---
# <a name="configure-integration-with-dayforce"></a><span data-ttu-id="9d043-104">Integration mit Dayforce konfigurieren</span><span class="sxs-lookup"><span data-stu-id="9d043-104">Configure integration with Dayforce</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="9d043-105">Die Integration zwischen Microsoft Dynamics 365 Human Resources und Ceridian Dayforce erfordert mehrere Konfigurationsschritte, die in diesem Artikel beschrieben sind.</span><span class="sxs-lookup"><span data-stu-id="9d043-105">The integration between Microsoft Dynamics 365 Human Resources and Ceridian Dayforce relies on several configuration steps that are described in this article.</span></span> <span data-ttu-id="9d043-106">Sie müssen die Integration sowohl in Human Resources als auch in Dayforce konfigurieren, bevor Sie einen Zahlungslauf verarbeiten können.</span><span class="sxs-lookup"><span data-stu-id="9d043-106">You must configure the integration in both Human Resources and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="9d043-107">Wenn Sie einen Dienst wie Dayforce verwenden, um Zahlungsläufe abzuschließen, müssen Sie die Integration in Human Resources ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="9d043-107">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Human Resources.</span></span> <span data-ttu-id="9d043-108">Die Integration erfordert bestimmte Daten aus Human Resources.</span><span class="sxs-lookup"><span data-stu-id="9d043-108">The integration requires specific data from Human Resources.</span></span> <span data-ttu-id="9d043-109">Daher müssen Sie überprüfen, dass die Daten, die Dayforce zugeordnet sind, in Human Resources in einer Weise konfiguriert werden, die die Integration unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9d043-109">Therefore, you must verify that data that is mapped to Dayforce is configured in Human Resources in a manner that supports the integration.</span></span> <span data-ttu-id="9d043-110">Bei der Integration werden die folgenden allgemeinen Kategorien von Daten verwendet:</span><span class="sxs-lookup"><span data-stu-id="9d043-110">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="9d043-111">Personalverwaltungsdaten</span><span class="sxs-lookup"><span data-stu-id="9d043-111">Human resources data</span></span>
- <span data-ttu-id="9d043-112">Vergütungsdaten</span><span class="sxs-lookup"><span data-stu-id="9d043-112">Compensation data</span></span>
- <span data-ttu-id="9d043-113">Lohndaten, wie Lohnzyklen, Lohnperioden und Einkommenscodes</span><span class="sxs-lookup"><span data-stu-id="9d043-113">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="9d043-114">Arbeitskraftdaten</span><span class="sxs-lookup"><span data-stu-id="9d043-114">Worker data</span></span>

<span data-ttu-id="9d043-115">In diesem Artikel werden die Schritte beschrieben, die Sie befolgen müssen, um die Integration zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="9d043-115">This article describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="9d043-116">Es werden auch die Datentypen und die Konfigurationsdetails erklärt, die für die Integration erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="9d043-116">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="9d043-117">Die Integration aktivieren</span><span class="sxs-lookup"><span data-stu-id="9d043-117">Enable the integration</span></span>

<span data-ttu-id="9d043-118">In Human Resources müssen Sie die Integration aktivieren und die Konfigurationsinformationen eingeben, um eine Verbindung mit Dayforce herzustellen.</span><span class="sxs-lookup"><span data-stu-id="9d043-118">In Human Resources, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="9d043-119">Wenn Sie möchten, dass die erstellte Hauptbuchtransaktion in Microsoft Dynamics 365 Finance importiert wird, müssen Sie auch ein Microsoft Azure-Speicherkonto einrichten und die Azure Storage-Verbindungszeichenfolge in Finance eingeben.</span><span class="sxs-lookup"><span data-stu-id="9d043-119">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 Finance, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance.</span></span>

<span data-ttu-id="9d043-120">Um die Integration in Human Resources zu aktivieren, gehen Sie folgendermaßen vor.</span><span class="sxs-lookup"><span data-stu-id="9d043-120">To turn on the integration in Human Resources, follow these steps.</span></span>

1. <span data-ttu-id="9d043-121">Wählen Sie auf der Seite **Systemverwaltung** die Option **Integrationskonfiguration** aus.</span><span class="sxs-lookup"><span data-stu-id="9d043-121">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="9d043-122">Geben Sie den sicheren Datenübertragungsprotokoll-(FTP)-Endpunkt und den sicheren FTP-Ordnerpfad ein.</span><span class="sxs-lookup"><span data-stu-id="9d043-122">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="9d043-123">Geben Sie den Benutzernamen und das Kennwort des Benutzers ein, der auf den sicheren FTP-Endpunkt und Ordnerpfad zugreift.</span><span class="sxs-lookup"><span data-stu-id="9d043-123">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="9d043-124">Testen Sie die Verbindung nach Bedarf, und legen Sie die Option **Lohnintegration aktivieren** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="9d043-124">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="9d043-125">Wenn die Integration aktiviert ist, werden Datenexportpaket und Dateien erstellt und die Häufigkeit wird festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9d043-125">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="9d043-126">Sie können diese Häufigkeit nach Bedarf ändern.</span><span class="sxs-lookup"><span data-stu-id="9d043-126">You can change this frequency as you require.</span></span>

<span data-ttu-id="9d043-127">Weitere Informationen zu Azure-Speicherkonten und Azure Storage-Verbindungszeichenfolgen finden Sie in den folgenden Azure-Artikeln:</span><span class="sxs-lookup"><span data-stu-id="9d043-127">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure articles:</span></span>

- [<span data-ttu-id="9d043-128">Über Azure-Speicherkonten</span><span class="sxs-lookup"><span data-stu-id="9d043-128">About Azure storage accounts</span></span>](/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="9d043-129">Azure Storage-Verbindungszeichenfolgen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="9d043-129">Configure Azure Storage connection strings</span></span>](/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="9d043-130">Technische Details, wenn Lohnintegration aktiviert ist</span><span class="sxs-lookup"><span data-stu-id="9d043-130">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="9d043-131">Die Aktivierung von Lohnintegration hat zwei primäre Auswirkungen:</span><span class="sxs-lookup"><span data-stu-id="9d043-131">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="9d043-132">Ein Datenexportprojekt namens „Lohnintegrationsexport“ wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="9d043-132">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="9d043-133">Dieses Projekt enthält die Entitäten und Felder, die für die Lohnintegration erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="9d043-133">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="9d043-134">Um das Projekt zu überprüfen, wechseln Sie zu **Systemverwaltung**, wählen Sie die Kachel **Datenverwaltung** aus, und öffnen Sie anschließend das Datenprojekt aus der Projektliste.</span><span class="sxs-lookup"><span data-stu-id="9d043-134">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="9d043-135">Dieser Stapelverarbeitungsauftrag führt das Datenexportprojekt aus, verschlüsselt das Datenpaket und überträgt die Datenenpaketdatei auf den SFTP-Endpunkt, der auf dem Bildschirm **Integrationskonfiguration** konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="9d043-135">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="9d043-136">Das Datenpaket, das zum SFTP-Endpunkt übertragen wird, wird mit einem Schlüssel verschlüsselt, für das Paket eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="9d043-136">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="9d043-137">Der Schlüssel befindet sich in einer Azure Key Vault, auf den nur durch Ceridian zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="9d043-137">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="9d043-138">Es ist nicht möglich, die Datenpaketinhalte zu entschlüsseln und zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="9d043-138">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="9d043-139">Wenn Sie den Inhalt des Datenpakets überprüfen möchten, müssen Sie das Datenprojekt „Lohnintegrationsexport“ manuell exportieren, herunterladen und dann öffnen.</span><span class="sxs-lookup"><span data-stu-id="9d043-139">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="9d043-140">Beim manuellen Export wird keine Verschlüsselung angewendet oder das Paket übertragen.</span><span class="sxs-lookup"><span data-stu-id="9d043-140">Manual export will not apply encryption or transfer the package.</span></span>
> <span data-ttu-id="9d043-141">Für Fälle, in denen die Integrationsdateien von einer Dynamics 365 Human Resources-UAT- oder Sandbox-Umgebung für eine Ceridian Dayforce-Testumgebung gesendet werden, können Sie die folgende URL des Schlüsseltresors verwenden: https://payrollintegrationprod.vault.azure.net.</span><span class="sxs-lookup"><span data-stu-id="9d043-141">For instances where the integration files are sent from a Dynamics 365 Human Resources UAT or Sandbox environment to a Ceridian Dayforce Test environment, you can use the following key vault URL: https://payrollintegrationprod.vault.azure.net.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="9d043-142">Ihre Daten konfigurieren</span><span class="sxs-lookup"><span data-stu-id="9d043-142">Configure your data</span></span> 

<span data-ttu-id="9d043-143">Um die Lohnbuchung zu verarbeiten, müssen Sie Personalverwaltungsdaten in Human Resources konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="9d043-143">To process payroll, you must configure human resource data in Human Resources.</span></span> <span data-ttu-id="9d043-144">Sie müssen Organisationsdaten, wie Stellen und Positionen, zusammen mit Vorteilen Vergütungsinformationen einrichten.</span><span class="sxs-lookup"><span data-stu-id="9d043-144">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="9d043-145">Diese Informationen stellen Beschäftigung, Lohn und die Abzugsinformationen bereit, die zur Generierung der Mitarbeiterentlohnung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="9d043-145">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="9d043-146">Personalverwaltungsdaten</span><span class="sxs-lookup"><span data-stu-id="9d043-146">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="9d043-147">Vergütungen</span><span class="sxs-lookup"><span data-stu-id="9d043-147">Benefits</span></span> 

<span data-ttu-id="9d043-148">Die Personalverwaltung stellt eine Reihe von Tools für die Einrichtung und Verwaltung der Vorteile, Abzüge und Vergütungspläne der Arbeitskräfte bereit, die eine Organisation für seine Arbeitskräfte anbietet oder verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="9d043-148">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="9d043-149">Wenn Sie Vorteile erstellen, sollten Sie folgende Daten und Konfigurationen bedenken, die in Dayforce verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9d043-149">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="9d043-150">Vorteilspläne</span><span class="sxs-lookup"><span data-stu-id="9d043-150">Benefit plans</span></span>

- <span data-ttu-id="9d043-151">Plan (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-151">Plan (required)</span></span>
- <span data-ttu-id="9d043-152">Typ (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-152">Type (required)</span></span>
- <span data-ttu-id="9d043-153">Lohnauswirkung (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-153">Payroll impact (required)</span></span>
- <span data-ttu-id="9d043-154">Rückstände wiederherstellen</span><span class="sxs-lookup"><span data-stu-id="9d043-154">Recover arrears</span></span>
- <span data-ttu-id="9d043-155">Abzugsverfahren</span><span class="sxs-lookup"><span data-stu-id="9d043-155">Deduction method</span></span>
- <span data-ttu-id="9d043-156">Abzugspriorität</span><span class="sxs-lookup"><span data-stu-id="9d043-156">Deduction priority</span></span>
- <span data-ttu-id="9d043-157">Periode eingrenzen</span><span class="sxs-lookup"><span data-stu-id="9d043-157">Limit period</span></span>
- <span data-ttu-id="9d043-158">Limitbetrag</span><span class="sxs-lookup"><span data-stu-id="9d043-158">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="9d043-159">Vergütungen</span><span class="sxs-lookup"><span data-stu-id="9d043-159">Benefits</span></span>

- <span data-ttu-id="9d043-160">Plan (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-160">Plan (required)</span></span>
- <span data-ttu-id="9d043-161">Typ (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-161">Type (required)</span></span>
- <span data-ttu-id="9d043-162">Option (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-162">Option (required)</span></span>
- <span data-ttu-id="9d043-163">Vorteilskennung (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-163">Benefit ID (required)</span></span>
- <span data-ttu-id="9d043-164">Häufigkeit</span><span class="sxs-lookup"><span data-stu-id="9d043-164">Frequency</span></span>
- <span data-ttu-id="9d043-165">Basis</span><span class="sxs-lookup"><span data-stu-id="9d043-165">Basis</span></span>
- <span data-ttu-id="9d043-166">Betrag oder Satz</span><span class="sxs-lookup"><span data-stu-id="9d043-166">Amount or rate</span></span>
- <span data-ttu-id="9d043-167">Einkommenscode</span><span class="sxs-lookup"><span data-stu-id="9d043-167">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="9d043-168">Unterstützte Häufigkeiten</span><span class="sxs-lookup"><span data-stu-id="9d043-168">Supported frequencies</span></span> 

- <span data-ttu-id="9d043-169">Wöchentlich</span><span class="sxs-lookup"><span data-stu-id="9d043-169">Weekly</span></span>
- <span data-ttu-id="9d043-170">14-tägig</span><span class="sxs-lookup"><span data-stu-id="9d043-170">Bi-weekly</span></span>
- <span data-ttu-id="9d043-171">Halbmonatlich</span><span class="sxs-lookup"><span data-stu-id="9d043-171">Semi-monthly</span></span>
- <span data-ttu-id="9d043-172">Monatlich</span><span class="sxs-lookup"><span data-stu-id="9d043-172">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="9d043-173">Unterstützte Basen</span><span class="sxs-lookup"><span data-stu-id="9d043-173">Supported bases</span></span> 

- <span data-ttu-id="9d043-174">Fester Betrag</span><span class="sxs-lookup"><span data-stu-id="9d043-174">Fixed amount</span></span>
- <span data-ttu-id="9d043-175">Prozent des Einkommens</span><span class="sxs-lookup"><span data-stu-id="9d043-175">Percent of earnings</span></span>
- <span data-ttu-id="9d043-176">Produktive Stunden</span><span class="sxs-lookup"><span data-stu-id="9d043-176">Productive hours</span></span>

<span data-ttu-id="9d043-177">Dayforce erstellt die folgenden Abzüge, basierend auf den Lohnauswirkungen, die im Vorteilsplan definiert sind.</span><span class="sxs-lookup"><span data-stu-id="9d043-177">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="9d043-178">Auswahl in Human Resources</span><span class="sxs-lookup"><span data-stu-id="9d043-178">Selection in Human Resources</span></span>        | <span data-ttu-id="9d043-179">Ergebnis in Dayforce</span><span class="sxs-lookup"><span data-stu-id="9d043-179">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="9d043-180">Nichts</span><span class="sxs-lookup"><span data-stu-id="9d043-180">None</span></span>                       | <span data-ttu-id="9d043-181">Es wird kein Abzug erstellt.</span><span class="sxs-lookup"><span data-stu-id="9d043-181">No deduction is created.</span></span>                      |
| <span data-ttu-id="9d043-182">Nur Abzug</span><span class="sxs-lookup"><span data-stu-id="9d043-182">Deduction only</span></span>             | <span data-ttu-id="9d043-183">Ein Mitarbeiterabzug wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="9d043-183">An employee deduction is created.</span></span>             |
| <span data-ttu-id="9d043-184">Nur Beitrag</span><span class="sxs-lookup"><span data-stu-id="9d043-184">Contribution only</span></span>          | <span data-ttu-id="9d043-185">Ein Arbeitgeberabzug wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="9d043-185">An employer deduction is created.</span></span>             |
| <span data-ttu-id="9d043-186">Abzug und Beitrag</span><span class="sxs-lookup"><span data-stu-id="9d043-186">Deduction and contribution</span></span> | <span data-ttu-id="9d043-187">Mitarbeiter- und Arbeitgeberabzüge werden erstellt.</span><span class="sxs-lookup"><span data-stu-id="9d043-187">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="9d043-188">Weitere Informationen darüber, wie Sie ein Vorteilsprogramm definieren und verwalten finden Sie in den folgenden Artikeln:</span><span class="sxs-lookup"><span data-stu-id="9d043-188">For more information about how to define and manage a benefits program, see the following articles:</span></span>

- [<span data-ttu-id="9d043-189">Mitarbeitervorteilsprogramm anbieten</span><span class="sxs-lookup"><span data-stu-id="9d043-189">Deliver an employee benefits program</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="9d043-190">Neue Vergütung erstellen</span><span class="sxs-lookup"><span data-stu-id="9d043-190">Create a new benefit</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="9d043-191">Vorteilsberechtigungsregeln und Richtlinien definieren</span><span class="sxs-lookup"><span data-stu-id="9d043-191">Define benefit eligibility rules and policies</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="9d043-192">Vorteile von Arbeitskräften registrieren und entfernen</span><span class="sxs-lookup"><span data-stu-id="9d043-192">Enroll and remove benefits from workers</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="9d043-193">Vergütung</span><span class="sxs-lookup"><span data-stu-id="9d043-193">Compensation</span></span> 

<span data-ttu-id="9d043-194">Die Vergütungsverwaltung dient zum Steuern der Abwicklung des Grundlohns und der Prämien.</span><span class="sxs-lookup"><span data-stu-id="9d043-194">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="9d043-195">Sie steuern den festen Grundlohn eines Mitarbeiters und dessen Lohnsteigerungen nach Plänen für feste Vergütung.</span><span class="sxs-lookup"><span data-stu-id="9d043-195">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="9d043-196">Die Zahlung leistungsbezogener Prämien, wie Boni, Leistungsprämien, Aktienoptionen und -überlassungen sowie Einmalprämien werden durch Pläne für variable Vergütung gesteuert.</span><span class="sxs-lookup"><span data-stu-id="9d043-196">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="9d043-197">Dayforce verwendet Vergütungsinformationen, um einen Stunden- oder Jahressatz für einen Mitarbeiter zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="9d043-197">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="9d043-198">Feste Vergütungspläne und Lohnsatzumrechnungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9d043-198">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="9d043-199">Mitarbeiter müssen einem festen Vergütungsplan zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="9d043-199">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="9d043-200">Weitere Informationen zu Kompensationsplänen finden Sie in den folgenden Artikeln:</span><span class="sxs-lookup"><span data-stu-id="9d043-200">For more information about compensation plans, see the following articles:</span></span>

- [<span data-ttu-id="9d043-201">Feste Vergütungspläne erstellen</span><span class="sxs-lookup"><span data-stu-id="9d043-201">Create fixed compensation plans</span></span>](/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="9d043-202">Variable Vergütungspläne erstellen</span><span class="sxs-lookup"><span data-stu-id="9d043-202">Create variable compensation plans</span></span>](/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="9d043-203">Gehalts-/Vergütungsstruktur und -pläne entwickeln</span><span class="sxs-lookup"><span data-stu-id="9d043-203">Develop salary/compensation structure and plans</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="9d043-204">Vergütung verarbeiten</span><span class="sxs-lookup"><span data-stu-id="9d043-204">Process compensation</span></span>](/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="9d043-205">Vergütungsprozess definieren und Ergebnisse berechnen</span><span class="sxs-lookup"><span data-stu-id="9d043-205">Define compensation process and calculate results</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="9d043-206">Einen Mitarbeiters in einem Plan für eine feste Vergütung registrieren</span><span class="sxs-lookup"><span data-stu-id="9d043-206">Enroll an employee in a fixed compensation plan</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="9d043-207">Einen Mitarbeiter in einem Plan für variable Vergütung registrieren</span><span class="sxs-lookup"><span data-stu-id="9d043-207">Enroll an employee in a variable compensation plan</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="9d043-208">Stellentyp</span><span class="sxs-lookup"><span data-stu-id="9d043-208">Jobs</span></span> 

<span data-ttu-id="9d043-209">Eine Stelle ist eine Sammlung der Aufgaben und Zuständigkeiten, die für eine Person, die eine Tätigkeit ausführt, obligatorisch sind.</span><span class="sxs-lookup"><span data-stu-id="9d043-209">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="9d043-210">Weitere Informationen finden Sie in folgenden Artikeln:</span><span class="sxs-lookup"><span data-stu-id="9d043-210">For more information, see the following articles:</span></span>

- [<span data-ttu-id="9d043-211">Komponenten einer Stelle einrichten</span><span class="sxs-lookup"><span data-stu-id="9d043-211">Setting up the components of a job</span></span>](/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="9d043-212">Neue Stellen definieren</span><span class="sxs-lookup"><span data-stu-id="9d043-212">Define new jobs</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="9d043-213">Positionen</span><span class="sxs-lookup"><span data-stu-id="9d043-213">Positions</span></span>

<span data-ttu-id="9d043-214">Eine Position ist eine einzelne Instanz eines Einzelvorgangs.</span><span class="sxs-lookup"><span data-stu-id="9d043-214">A position is an individual instance of a job.</span></span> <span data-ttu-id="9d043-215">Beispielsweise ist die Position „Verkaufsleiter (Ost)” eine der Positionen, die der Stelle „Verkaufsleiter” zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="9d043-215">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="9d043-216">Eine Position ist in einer Abteilung vorhanden.</span><span class="sxs-lookup"><span data-stu-id="9d043-216">A position exists in a department.</span></span> <span data-ttu-id="9d043-217">Nur jeweils eine Arbeitskraft kann jeder Position zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="9d043-217">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="9d043-218">Bedenken Sie die folgenden Daten und Konfigurationen, wenn Sie Positionen einrichten:</span><span class="sxs-lookup"><span data-stu-id="9d043-218">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="9d043-219">Position (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-219">Position (required)</span></span>
- <span data-ttu-id="9d043-220">Beschreibung (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-220">Description (required)</span></span>
- <span data-ttu-id="9d043-221">Stelle (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-221">Job (required)</span></span>
- <span data-ttu-id="9d043-222">Abteilung (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-222">Department (required)</span></span>
- <span data-ttu-id="9d043-223">Positionstyp (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-223">Position type (required)</span></span>
- <span data-ttu-id="9d043-224">Vollzeitäquivalent</span><span class="sxs-lookup"><span data-stu-id="9d043-224">Full-time equivalent</span></span>
- <span data-ttu-id="9d043-225">Normale Stunden pro Jahr (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-225">Annual regular hours (required)</span></span>
- <span data-ttu-id="9d043-226">Gezahlt von der juristischen Person (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-226">Paid by legal entity (required)</span></span>
- <span data-ttu-id="9d043-227">Lohnzyklus (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-227">Pay cycle (required)</span></span>
- <span data-ttu-id="9d043-228">Standardfinanzdimension – Kostenstelle (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-228">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="9d043-229">Arbeitskraftzuweisung – Arbeitskraft, Zuweisungsanfang, Zuweisungsende, Ursachencode</span><span class="sxs-lookup"><span data-stu-id="9d043-229">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="9d043-230">Wenn mehrere Positionen in derselben Abteilung derselben Stelle zugeordnet sind, werden sie in einer einzelnen Position in Dayforce konsolidiert.</span><span class="sxs-lookup"><span data-stu-id="9d043-230">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="9d043-231">Weitere Informationen finden Sie in folgenden Artikeln:</span><span class="sxs-lookup"><span data-stu-id="9d043-231">For more information, see the following articles:</span></span>

- [<span data-ttu-id="9d043-232">Belegschaft mittels Abteilungen, Stellen und Positionen verwalten</span><span class="sxs-lookup"><span data-stu-id="9d043-232">Organize your workforce using departments, jobs, and positions</span></span>](/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="9d043-233">Positionen einrichten</span><span class="sxs-lookup"><span data-stu-id="9d043-233">Set up positions</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="9d043-234">Abteilungen</span><span class="sxs-lookup"><span data-stu-id="9d043-234">Departments</span></span>

<span data-ttu-id="9d043-235">Eine Abteilung ist eine Organisationseinheit, die eine Kategorie oder einen funktionalen Bereich einer Organisation darstellt.</span><span class="sxs-lookup"><span data-stu-id="9d043-235">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="9d043-236">Eine Abteilung ist für einen bestimmten Bereich der Organisation wie zum Beispiel Verkauf, Buchhaltung oder Personalverwaltung zuständig.</span><span class="sxs-lookup"><span data-stu-id="9d043-236">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="9d043-237">Sie können Abteilungen verwenden, um zu Funktionsbereiche zu melden.</span><span class="sxs-lookup"><span data-stu-id="9d043-237">You can use departments to report on functional areas.</span></span> <span data-ttu-id="9d043-238">Abteilungen können Gewinn- und Verlustzuständigkeit haben.</span><span class="sxs-lookup"><span data-stu-id="9d043-238">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="9d043-239">Weitere Informationen finden Sie in folgenden Artikeln:</span><span class="sxs-lookup"><span data-stu-id="9d043-239">For more information, see the following articles:</span></span>

- [<span data-ttu-id="9d043-240">Abteilung erstellen und der Abteilungshierarchie zuordnen</span><span class="sxs-lookup"><span data-stu-id="9d043-240">Create a department and associate it with the department hierarchy</span></span>](/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="9d043-241">Neue Abteilungen definieren</span><span class="sxs-lookup"><span data-stu-id="9d043-241">Define new departments</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="9d043-242">Lohnzyklen und Lohnperioden</span><span class="sxs-lookup"><span data-stu-id="9d043-242">Pay cycles and pay periods</span></span>

<span data-ttu-id="9d043-243">Ein Lohnzyklus bestimmt, wie oft Lohn ausgezahlt wird, sowie die spezifischen Tage, an denen Arbeitskräfte bezahlt werden.</span><span class="sxs-lookup"><span data-stu-id="9d043-243">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="9d043-244">Ein Lohnzyklus kann beispielsweise monatlich sein, und Mitarbeiter werden am letzten Tag des Monats bezahlt.</span><span class="sxs-lookup"><span data-stu-id="9d043-244">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="9d043-245">Alternativ könnte ein Lohnzyklus wöchentlich sein, und Mitarbeiter werden am Dienstag nach Ende der Lohnperiode bezahlt.</span><span class="sxs-lookup"><span data-stu-id="9d043-245">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="9d043-246">Lohnzyklen werden Positionen zugewiesen, um zu steuern, wann Mitarbeiter in diesen Positionen bezahlt werden.</span><span class="sxs-lookup"><span data-stu-id="9d043-246">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="9d043-247">Nachdem Sie Lohnzyklen erstellen, können Sie Lohnperioden für jeden Zyklus generieren.</span><span class="sxs-lookup"><span data-stu-id="9d043-247">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="9d043-248">Jede Lohnperiode enthält ein Standardzahlungsdatum, das auf den von Ihnen bereitgestellten Informationen basiert.</span><span class="sxs-lookup"><span data-stu-id="9d043-248">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="9d043-249">Allerdings können Sie das Standardzahlungsdatum in einer Lohnperiode ändern, um Ausnahmen zuzulassen, wie beispielsweise wenn das Zahlungsdatum auf einen Feiertag fällt.</span><span class="sxs-lookup"><span data-stu-id="9d043-249">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="9d043-250">Die folgenden Informationen werden in Dayforce verwendet:</span><span class="sxs-lookup"><span data-stu-id="9d043-250">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="9d043-251">Lohnzyklus (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-251">Pay cycle (required)</span></span>
- <span data-ttu-id="9d043-252">Lohnzyklushäufigkeit (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-252">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="9d043-253">Periodenstartdatum (erstes erforderliche Lohnperiode)</span><span class="sxs-lookup"><span data-stu-id="9d043-253">Period start date (first pay period required)</span></span>
- <span data-ttu-id="9d043-254">Standardzahlungsdatum (erste erforderliche Lohnperiode)</span><span class="sxs-lookup"><span data-stu-id="9d043-254">Default payment date (first pay period required)</span></span>

<span data-ttu-id="9d043-255">Diese Informationen werden mit Dayforce als Lohngruppen integriert und sind nach Land oder Region für jeden Lohnzyklus getrennt.</span><span class="sxs-lookup"><span data-stu-id="9d043-255">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="9d043-256">Es muss mindestens eine Lohnperiode vor der Integration generiert werden.</span><span class="sxs-lookup"><span data-stu-id="9d043-256">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="9d043-257">Dayforce generiert Lohngruppenkalender und Zahlungsdaten basierend auf dem Anfangsdatum der ersten Lohnperiode und dem Standardzahlungsdatums, das in Human Resources eingerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="9d043-257">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Human Resources.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="9d043-258">Einkommenscodes</span><span class="sxs-lookup"><span data-stu-id="9d043-258">Earning codes</span></span>

<span data-ttu-id="9d043-259">Einkommenscodes bestimmen jeden Typ von Einkünften eindeutig, die Arbeitskräfte erhalten</span><span class="sxs-lookup"><span data-stu-id="9d043-259">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="9d043-260">Die Codes haben verschiedene Parameter, die sich auf Einkünfte beziehen, wie beispielsweise Buchhaltungsvorschriften, Steuergesetze, Berichterstellungsanforderungen und Bruttoausgleichsfähigkeit.</span><span class="sxs-lookup"><span data-stu-id="9d043-260">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="9d043-261">Die folgenden Informationen werden in Dayforce verwendet:</span><span class="sxs-lookup"><span data-stu-id="9d043-261">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="9d043-262">Einkommenscode (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-262">Earning Code (required)</span></span>
- <span data-ttu-id="9d043-263">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9d043-263">Description</span></span>
- <span data-ttu-id="9d043-264">Maßeinheit</span><span class="sxs-lookup"><span data-stu-id="9d043-264">Unit of measure</span></span>
- <span data-ttu-id="9d043-265">Produktiv</span><span class="sxs-lookup"><span data-stu-id="9d043-265">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="9d043-266">Arbeitskraftdaten</span><span class="sxs-lookup"><span data-stu-id="9d043-266">Worker data</span></span>

<span data-ttu-id="9d043-267">Datensätze für die verschiedenen Arten von Arbeitskräften, die Sie haben, sind für Ihre Personalverwaltung- sowie für Ihre Lohnsysteme von Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="9d043-267">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="9d043-268">Anhand der eingegebenen Informationen lassen sich Arbeitskräfte sowie personenbezogene Informationen nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="9d043-268">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="9d043-269">Sie können die folgenden Informationen für Arbeitskräfte verwalten:</span><span class="sxs-lookup"><span data-stu-id="9d043-269">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="9d043-270">**Basis** – Verwalten grundlegender Informationen über eine Arbeitskraft, beispielsweise Kontaktinformationen, demografische Informationen, Kennungsinformationen, Familieninformationen, Militärdienststatus, Ausländerinformationen sowie personenbezogene und Notfallkontakte.</span><span class="sxs-lookup"><span data-stu-id="9d043-270">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="9d043-271">**Beschäftigung** – Verwalten von Informationen zum Beschäftigungsverhältnis einer Arbeitskraft, wie Unternehmens- oder Organisationszugehörigkeit, Positionszuweisung, Start- und Enddatum, Arbeitsberechtigung, Beschäftigungsbedingungen, Rente, Urlaub und Versetzungen.</span><span class="sxs-lookup"><span data-stu-id="9d043-271">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="9d043-272">**Urlaub und Abwesenheit** – Verwalten von Informationen zur Abwesenheit einer Arbeitskraft, beispielsweise Arbeitszeitkalender, Abwesenheitsbuchungen und Abwesenheitseinrichtung.</span><span class="sxs-lookup"><span data-stu-id="9d043-272">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="9d043-273">**Vergütung und Lohn** – Verwalten von Informationen zu den Vergütungsplänen und Lohndaten einer Arbeitskraft, wie der Planregistrierung, Boni, Leistung, Provision, Steuerdaten, Pensionierung und Gehaltsabzüge.</span><span class="sxs-lookup"><span data-stu-id="9d043-273">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="9d043-274">Wenn Sie Arbeitskraftinformationen eingeben, sollten Sie folgende Daten und Konfigurationen bedenken, die in Dayforce verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9d043-274">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="9d043-275">Allgemeine Angaben</span><span class="sxs-lookup"><span data-stu-id="9d043-275">General information</span></span>

- <span data-ttu-id="9d043-276">Personalnummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-276">Personnel number (required)</span></span>
- <span data-ttu-id="9d043-277">Vorname (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-277">First name (required)</span></span>
- <span data-ttu-id="9d043-278">Nachname (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-278">Last name (required)</span></span>
- <span data-ttu-id="9d043-279">Zweiter Vorname</span><span class="sxs-lookup"><span data-stu-id="9d043-279">Middle name</span></span>
- <span data-ttu-id="9d043-280">Dienstalterdatum</span><span class="sxs-lookup"><span data-stu-id="9d043-280">Seniority date</span></span>
- <span data-ttu-id="9d043-281">Bekannt als</span><span class="sxs-lookup"><span data-stu-id="9d043-281">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="9d043-282">Personenbezogene Informationen</span><span class="sxs-lookup"><span data-stu-id="9d043-282">Personal information</span></span>

- <span data-ttu-id="9d043-283">Familienstand (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-283">Marital status (required)</span></span>
- <span data-ttu-id="9d043-284">Geburtsdatum (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-284">Birth date (required)</span></span>
- <span data-ttu-id="9d043-285">Geschlecht (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-285">Gender (required)</span></span>
- <span data-ttu-id="9d043-286">Person mit Behinderung</span><span class="sxs-lookup"><span data-stu-id="9d043-286">Person with disabilities</span></span>
- <span data-ttu-id="9d043-287">Nationalitätsland/-region (nur für Mexiko)</span><span class="sxs-lookup"><span data-stu-id="9d043-287">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="9d043-288">Adressdaten</span><span class="sxs-lookup"><span data-stu-id="9d043-288">Address information</span></span>

- <span data-ttu-id="9d043-289">Primär (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-289">Primary (required)</span></span>
- <span data-ttu-id="9d043-290">Land/Region (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-290">Country/region (required)</span></span>
- <span data-ttu-id="9d043-291">Postleitzahl (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-291">Postal code (required)</span></span>
- <span data-ttu-id="9d043-292">Hausnummer (erforderlich) (nur für Mexiko)</span><span class="sxs-lookup"><span data-stu-id="9d043-292">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="9d043-293">Gebäudeergänzung (nur für Mexiko)</span><span class="sxs-lookup"><span data-stu-id="9d043-293">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="9d043-294">Ort (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-294">City (required)</span></span>
- <span data-ttu-id="9d043-295">Bundesland/Kanton (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-295">State (required)</span></span>
- <span data-ttu-id="9d043-296">Landkreis (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-296">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="9d043-297">Kontaktdaten</span><span class="sxs-lookup"><span data-stu-id="9d043-297">Contact information</span></span> 

- <span data-ttu-id="9d043-298">Primär (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-298">Primary (required)</span></span>
- <span data-ttu-id="9d043-299">Kontaktnummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-299">Contact number (required)</span></span>
- <span data-ttu-id="9d043-300">Durchwahl</span><span class="sxs-lookup"><span data-stu-id="9d043-300">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="9d043-301">Lohndaten und Einkommenscodes</span><span class="sxs-lookup"><span data-stu-id="9d043-301">Payroll information and earning codes</span></span>

<span data-ttu-id="9d043-302">Mitarbeitern müssen bestimmte Einkommen mit einer bestimmten Zahlungshäufigkeit zugewiesen werden und sie müssen eine bevorzugte Zahlungsmethode haben.</span><span class="sxs-lookup"><span data-stu-id="9d043-302">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="9d043-303">Die folgenden Felder werden in Dayforce verwendet, um zu gewährleisten, dass diese Voreinstellungen und Einstellungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9d043-303">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="9d043-304">Einkommenscodes</span><span class="sxs-lookup"><span data-stu-id="9d043-304">Earning codes</span></span>

- <span data-ttu-id="9d043-305">Position (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-305">Position (required)</span></span>
- <span data-ttu-id="9d043-306">Einkommenscode (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-306">Earning Code (required)</span></span>
- <span data-ttu-id="9d043-307">Häufigkeit (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-307">Frequency (required)</span></span>
- <span data-ttu-id="9d043-308">Betrag (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-308">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="9d043-309">Lohndaten</span><span class="sxs-lookup"><span data-stu-id="9d043-309">Payroll information</span></span>

- <span data-ttu-id="9d043-310">Zahlungsmethode</span><span class="sxs-lookup"><span data-stu-id="9d043-310">Payment Method</span></span>
- <span data-ttu-id="9d043-311">Wirtschaftliche Region (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-311">Economic Region (required)</span></span>
- <span data-ttu-id="9d043-312">Mitarbeitervergütungs-ID</span><span class="sxs-lookup"><span data-stu-id="9d043-312">Employee Benefits ID</span></span>
- <span data-ttu-id="9d043-313">Personalausweisnummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-313">National ID Number (required)</span></span>
- <span data-ttu-id="9d043-314">Militärdienstnummer</span><span class="sxs-lookup"><span data-stu-id="9d043-314">Military Service Number</span></span>
- <span data-ttu-id="9d043-315">Schichtkennung (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-315">Shift ID (required)</span></span>
- <span data-ttu-id="9d043-316">Steuernummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-316">Tax Number (required)</span></span>
- <span data-ttu-id="9d043-317">Gewerkschaftskennung (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-317">Union ID (required)</span></span>
- <span data-ttu-id="9d043-318">Arbeitstagkennung (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-318">Work Day ID (required)</span></span>
- <span data-ttu-id="9d043-319">Arbeitserlaubnisnummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-319">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="9d043-320">Für die Zahlungsmethode unterstützt Mexiko **Bargeld**, **Scheck** (der physische Scheck des Unternehmens) und **Elektronische Zahlung**.</span><span class="sxs-lookup"><span data-stu-id="9d043-320">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="9d043-321">Wenn keine Zahlungsmethode angegeben wird, wird **Scheck** standardmäßig verwendet.</span><span class="sxs-lookup"><span data-stu-id="9d043-321">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="9d043-322">Anstellungsdetails</span><span class="sxs-lookup"><span data-stu-id="9d043-322">Employment details</span></span>

<span data-ttu-id="9d043-323">Beschäftigungsdetailhistorie wird als Schlüsselinformation verwendet, um die Status für Einstellung, Kündigung und erneute Einstellung in Dayforce abzuleiten.</span><span class="sxs-lookup"><span data-stu-id="9d043-323">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="9d043-324">Dayforce unterstützt nur einen aktiven Beschäftigungsdatensatz gleichzeitig.</span><span class="sxs-lookup"><span data-stu-id="9d043-324">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="9d043-325">Datum des Beschäftigungsbeginns (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-325">Employment start date (required)</span></span>
- <span data-ttu-id="9d043-326">Datum des Beschäftigungsendes</span><span class="sxs-lookup"><span data-stu-id="9d043-326">Employment end date</span></span>
- <span data-ttu-id="9d043-327">Eintrittstermin</span><span class="sxs-lookup"><span data-stu-id="9d043-327">Start date</span></span>
- <span data-ttu-id="9d043-328">Angepasster Tätigkeitsbeginn</span><span class="sxs-lookup"><span data-stu-id="9d043-328">Adjusted start date</span></span>
- <span data-ttu-id="9d043-329">Kündigungsdatum (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-329">Termination date (required upon termination)</span></span>
- <span data-ttu-id="9d043-330">Kündigungsgrund (erforderlich bei Kündigung)</span><span class="sxs-lookup"><span data-stu-id="9d043-330">Termination reason (required upon termination)</span></span>

<span data-ttu-id="9d043-331">Die Schlüsseldaten eines Mitarbeiters werden abgeleitet, indem die folgenden Informationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9d043-331">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="9d043-332">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="9d043-332">Human Resources</span></span>                | <span data-ttu-id="9d043-333">Dayforce</span><span class="sxs-lookup"><span data-stu-id="9d043-333">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d043-334">Aktuellstes Einstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="9d043-334">Most recent hire date</span></span> | <span data-ttu-id="9d043-335">Beschäftigungsbeginn des Verlaufsdatensatzes zur aktuellen, nicht gekündigten Beschäftigung</span><span class="sxs-lookup"><span data-stu-id="9d043-335">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="9d043-336">Kündigungsdatum</span><span class="sxs-lookup"><span data-stu-id="9d043-336">Termination date</span></span>      | <span data-ttu-id="9d043-337">Kündigungsdatum des Verlaufsdatensatzes zur aktuellen, nicht gekündigten Beschäftigung</span><span class="sxs-lookup"><span data-stu-id="9d043-337">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="9d043-338">Eintrittstermin</span><span class="sxs-lookup"><span data-stu-id="9d043-338">Start date</span></span>            | <span data-ttu-id="9d043-339">Angepasstes Startdatum, Startdatum oder Beschäftigungsbeginn des Verlaufsdatensatzes zur aktuellen, nicht aktiven Beschäftigung</span><span class="sxs-lookup"><span data-stu-id="9d043-339">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="9d043-340">Ursprüngliches Einstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="9d043-340">Original hire date</span></span>    | <span data-ttu-id="9d043-341">Beschäftigungsbeginn des frühesten Beschäftigungsverlaufsdatensatzes</span><span class="sxs-lookup"><span data-stu-id="9d043-341">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="9d043-342">Vergütung</span><span class="sxs-lookup"><span data-stu-id="9d043-342">Compensation</span></span>

<span data-ttu-id="9d043-343">Ein fester Vergütungsplan muss der primären Position jedes Mitarbeiters während einer Beschäftigungsperiode zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="9d043-343">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="9d043-344">Diese Periode beginnt mit dem Datum, an dem der Mitarbeiter eingestellt wurde (oder dem Datum des Beschäftigungsbeginns), und setzt sich bis zur Kündigung fort.</span><span class="sxs-lookup"><span data-stu-id="9d043-344">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="9d043-345">Gültigkeitsdatum (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-345">Effective Date (required)</span></span>
- <span data-ttu-id="9d043-346">Ablaufdatum</span><span class="sxs-lookup"><span data-stu-id="9d043-346">Expiration date</span></span>
- <span data-ttu-id="9d043-347">Lohnsatz (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-347">Pay Rate (required)</span></span>
- <span data-ttu-id="9d043-348">Lohnsatzkonvertierungen (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-348">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="9d043-349">Jährliches Äquivalent (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-349">Annual equivalent (required)</span></span>
- <span data-ttu-id="9d043-350">Stündliches Äquivalent (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-350">Hourly equivalent (required)</span></span>

<span data-ttu-id="9d043-351">Wenn ein Mitarbeiter auf Stundenbasis mehrere Positionen hat, wird die feste Vergütung der primären Position in Dayforce als Basissatz/-gehalt auf Mitarbeiterebene importiert.</span><span class="sxs-lookup"><span data-stu-id="9d043-351">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="9d043-352">Für nicht-primäre Positionen wird der Stundensatz in der entsprechenden Position in Dayforce gespeichert.</span><span class="sxs-lookup"><span data-stu-id="9d043-352">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="9d043-353">Wenn ein Gehalt beziehender Mitarbeiter mehrere Positionen hat, wird der kumulative Stundensatz und das Jahresgehalt über alle aktiven Positionen hinweg abgeleitet und als Basissatz/-gehalt auf Arbeitnehmerebene verwendet.</span><span class="sxs-lookup"><span data-stu-id="9d043-353">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="9d043-354">Kennnummern</span><span class="sxs-lookup"><span data-stu-id="9d043-354">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="9d043-355">Sozialversicherungsbezeichner</span><span class="sxs-lookup"><span data-stu-id="9d043-355">Social Security identifier</span></span> 

<span data-ttu-id="9d043-356">Jeder Mitarbeiter muss einen primären Bezeichner haben.</span><span class="sxs-lookup"><span data-stu-id="9d043-356">Every employee must have one primary identifier.</span></span> <span data-ttu-id="9d043-357">Dieser Bezeichner muss vom Kennungstyp **P.Reg.Nr.** sein.</span><span class="sxs-lookup"><span data-stu-id="9d043-357">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="9d043-358">In Dayforce wird er automatisch als Sozialversicherungsbezeichner des Mitarbeiters abgeleitet, der für die Einstellung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="9d043-358">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="9d043-359">Primär (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-359">Primary (required)</span></span>
- <span data-ttu-id="9d043-360">Kennungstyp = „P.Reg.Nr.”</span><span class="sxs-lookup"><span data-stu-id="9d043-360">Identification Type = "SSN"</span></span>
- <span data-ttu-id="9d043-361">Ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="9d043-361">Issued Date</span></span>
- <span data-ttu-id="9d043-362">Ablaufdatum</span><span class="sxs-lookup"><span data-stu-id="9d043-362">Expiration Date</span></span>

<span data-ttu-id="9d043-363">Mitarbeiter können mehrere Kennungsnummern des Kennungstyps **P.Reg.Nr.** melden.</span><span class="sxs-lookup"><span data-stu-id="9d043-363">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="9d043-364">Jedoch wird nur der Datensatz, der als **Primär** markiert ist, in Dayforce integriert, unabhängig davon, ob die Nummer aktiv oder abgelaufen ist.</span><span class="sxs-lookup"><span data-stu-id="9d043-364">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="9d043-365">Bankkonten und Auszahlungen</span><span class="sxs-lookup"><span data-stu-id="9d043-365">Bank accounts and disbursements</span></span>

<span data-ttu-id="9d043-366">Gültige Bankkontoinformationen müssen für jeden Mitarbeiter eingegeben werden, der per Bankkontoüberweisungen bezahlt werden möchte.</span><span class="sxs-lookup"><span data-stu-id="9d043-366">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="9d043-367">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="9d043-367">Human Resources</span></span>                         | <span data-ttu-id="9d043-368">Dayforce</span><span class="sxs-lookup"><span data-stu-id="9d043-368">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d043-369">Bankkontonummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-369">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="9d043-370">SWIFT-Code (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-370">SWIFT code (required)</span></span>          | <span data-ttu-id="9d043-371">Feld **Bankkennung** wird verwendet, wenn Lohn in Mexiko verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="9d043-371">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="9d043-372">Filialnummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-372">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="9d043-373">Bankkontotyp (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-373">Bank account type (required)</span></span>   | <span data-ttu-id="9d043-374">Feld **Kontotyp** wird verwendet, wenn Lohn in Mexiko verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="9d043-374">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="9d043-375">Unterstützte Werte umfassen **Wird geprüft** und **Lohn**.</span><span class="sxs-lookup"><span data-stu-id="9d043-375">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="9d043-376">Mitarbeiter, die per Bankkontoüberweisungen bezahlt werden möchten, müssen eine Verknüpfung zu einem Restbetrags-Bankkonto angeben, das sich unter einer juristischen Person befindet, deren primäre Adresse in Mexiko ist und das einem gültigen Bankkonto von einer mexikanischen Bank zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="9d043-376">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="9d043-377">Alle anderen Nicht-Restbetrags-Bankkonten werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="9d043-377">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="9d043-378">Adressdaten</span><span class="sxs-lookup"><span data-stu-id="9d043-378">Address information</span></span>

<span data-ttu-id="9d043-379">Jeder Mitarbeiter muss einen primären Standort haben.</span><span class="sxs-lookup"><span data-stu-id="9d043-379">Every employee must have one primary location.</span></span> <span data-ttu-id="9d043-380">In Dayforce wird dieser Standort verwendet, um den primären Wohnsitz des Mitarbeiters für Steuerzwecke zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="9d043-380">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="9d043-381">Primär (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-381">Primary (required)</span></span>
- <span data-ttu-id="9d043-382">Land/Region (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-382">Country/region (required)</span></span>
- <span data-ttu-id="9d043-383">Postleitzahl (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-383">Zip/postal code (required)</span></span>
- <span data-ttu-id="9d043-384">Straße (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-384">Street (required)</span></span>
- <span data-ttu-id="9d043-385">Hausnummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-385">Street Number (required)</span></span>
- <span data-ttu-id="9d043-386">Gebäudeergänzung</span><span class="sxs-lookup"><span data-stu-id="9d043-386">Building Complement</span></span>
- <span data-ttu-id="9d043-387">Ort (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-387">City (required)</span></span>
- <span data-ttu-id="9d043-388">Bundesland/Kanton (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-388">State (required)</span></span>
- <span data-ttu-id="9d043-389">Landkreis (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-389">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="9d043-390">Konfigurieren Ihrer Daten, um Vergütung in den USA und Kanada zu generieren</span><span class="sxs-lookup"><span data-stu-id="9d043-390">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="9d043-391">Wenn Sie Vergütung für Mitarbeiter in den USA und Kanada generieren, müssen die folgenden Elemente konfiguriert werden:</span><span class="sxs-lookup"><span data-stu-id="9d043-391">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="9d043-392">Abteilungen sind für Positionen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9d043-392">Departments are required on positions.</span></span>
- <span data-ttu-id="9d043-393">Kostenstellen müssen als Finanzdimensionen festgelegt werden und müssen das erste Element in der standardmäßigen Finanzdimensions-Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="9d043-393">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="9d043-394">Sie können Human Resources so konfigurieren, dass Positionen eine Abteilung angeben müssen.</span><span class="sxs-lookup"><span data-stu-id="9d043-394">You can configure Human Resources to require that Positions specify a Department.</span></span> <span data-ttu-id="9d043-395">Dazu wechseln Sie zu **Freigegebene Positionen der Personalverwaltung > Positionen > Abteilungen zu Positionen anfordern**.</span><span class="sxs-lookup"><span data-stu-id="9d043-395">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="9d043-396">Es wird empfohlen, dass diese Einstellungen für die Integration erzwungen wird.</span><span class="sxs-lookup"><span data-stu-id="9d043-396">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="9d043-397">Stellentypen</span><span class="sxs-lookup"><span data-stu-id="9d043-397">Job types</span></span>

<span data-ttu-id="9d043-398">Stellentypen werden verwendet, um ähnliche Stellen in Kategorien zu gruppieren.</span><span class="sxs-lookup"><span data-stu-id="9d043-398">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="9d043-399">Stellentypen sind erforderlich, damit Lohn in den USA und Kanada zu bearbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="9d043-399">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="9d043-400">Beispiele für Stellentypen umfassen Voll- und Teilzeit oder festes Gehalt und Stundenlohn.</span><span class="sxs-lookup"><span data-stu-id="9d043-400">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="9d043-401">Stellentypen werden Dayforce als Lohnarten zugeordnet, die angeben, ob ein Mitarbeiter auf Stundenbasis bezahlt wird oder ein festes Gehalt bezieht.</span><span class="sxs-lookup"><span data-stu-id="9d043-401">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="9d043-402">Folgende Stellentypen und Beschreibungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9d043-402">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="9d043-403">Stellentyp</span><span class="sxs-lookup"><span data-stu-id="9d043-403">Job type</span></span>   | <span data-ttu-id="9d043-404">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9d043-404">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="9d043-405">Stündlich</span><span class="sxs-lookup"><span data-stu-id="9d043-405">Hourly</span></span>     | <span data-ttu-id="9d043-406">Stündlich</span><span class="sxs-lookup"><span data-stu-id="9d043-406">Hourly</span></span>      |
| <span data-ttu-id="9d043-407">Fest angestellt</span><span class="sxs-lookup"><span data-stu-id="9d043-407">Salaried</span></span>   | <span data-ttu-id="9d043-408">Fest angestellt</span><span class="sxs-lookup"><span data-stu-id="9d043-408">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="9d043-409">Positionstypen</span><span class="sxs-lookup"><span data-stu-id="9d043-409">Position types</span></span> 

<span data-ttu-id="9d043-410">Sie verwenden Positionstypen, um zu beschreiben, ob die Position Vollzeit, Teilzeit oder etwas anderes ist.</span><span class="sxs-lookup"><span data-stu-id="9d043-410">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="9d043-411">Positionstypen werden Dayforce als Lohnklassen zugeordnet, die angeben, ob ein Mitarbeiter in Vollzeit oder Teilzeit arbeitet.</span><span class="sxs-lookup"><span data-stu-id="9d043-411">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="9d043-412">Folgende Positionstypen und Beschreibungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9d043-412">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="9d043-413">Positionstyp</span><span class="sxs-lookup"><span data-stu-id="9d043-413">Position type</span></span>   | <span data-ttu-id="9d043-414">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9d043-414">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="9d043-415">Vollzeit</span><span class="sxs-lookup"><span data-stu-id="9d043-415">Full-time</span></span>       | <span data-ttu-id="9d043-416">Vollzeitmitarbeiter</span><span class="sxs-lookup"><span data-stu-id="9d043-416">Full time employee</span></span> |
| <span data-ttu-id="9d043-417">Teilzeit</span><span class="sxs-lookup"><span data-stu-id="9d043-417">Part-time</span></span>       | <span data-ttu-id="9d043-418">Teilzeitmitarbeiter</span><span class="sxs-lookup"><span data-stu-id="9d043-418">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="9d043-419">Ursachencodes</span><span class="sxs-lookup"><span data-stu-id="9d043-419">Reason codes</span></span>

<span data-ttu-id="9d043-420">Ursachencodes enthalten Informationen zum Status eines Mitarbeiters.</span><span class="sxs-lookup"><span data-stu-id="9d043-420">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="9d043-421">Ursachencodes werden Dayforce als Statusgründe zugeordnet, die den Grund für Änderungen bei der Position eines Mitarbeiters oder dem Beschäftigungsstatus angeben.</span><span class="sxs-lookup"><span data-stu-id="9d043-421">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="9d043-422">Folgende Ursachencodes und Beschreibungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9d043-422">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="9d043-423">Ursachencode</span><span class="sxs-lookup"><span data-stu-id="9d043-423">Reason code</span></span>    | <span data-ttu-id="9d043-424">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9d043-424">Description</span></span>      | <span data-ttu-id="9d043-425">Zutreffende Szenarios</span><span class="sxs-lookup"><span data-stu-id="9d043-425">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="9d043-426">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="9d043-426">RESIGNATION</span></span>    | <span data-ttu-id="9d043-427">Kündigung durch Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="9d043-427">Resignation</span></span>      | <span data-ttu-id="9d043-428">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="9d043-428">Terminate worker</span></span>     |
| <span data-ttu-id="9d043-429">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="9d043-429">TERMINATION</span></span>    | <span data-ttu-id="9d043-430">Beendigung</span><span class="sxs-lookup"><span data-stu-id="9d043-430">Termination</span></span>      | <span data-ttu-id="9d043-431">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="9d043-431">Terminate worker</span></span>     |
| <span data-ttu-id="9d043-432">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="9d043-432">RETIREMENT</span></span>     | <span data-ttu-id="9d043-433">Ruhestand</span><span class="sxs-lookup"><span data-stu-id="9d043-433">Retirement</span></span>       | <span data-ttu-id="9d043-434">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="9d043-434">Terminate worker</span></span>     |
| <span data-ttu-id="9d043-435">OTHER</span><span class="sxs-lookup"><span data-stu-id="9d043-435">OTHER</span></span>          | <span data-ttu-id="9d043-436">Andere Gründe</span><span class="sxs-lookup"><span data-stu-id="9d043-436">Other Reasons</span></span>    | <span data-ttu-id="9d043-437">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="9d043-437">Terminate worker</span></span>     |
| <span data-ttu-id="9d043-438">DEATH</span><span class="sxs-lookup"><span data-stu-id="9d043-438">DEATH</span></span>          | <span data-ttu-id="9d043-439">Tod</span><span class="sxs-lookup"><span data-stu-id="9d043-439">Death</span></span>            | <span data-ttu-id="9d043-440">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="9d043-440">Terminate worker</span></span>     |
| <span data-ttu-id="9d043-441">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="9d043-441">LEAVEOFABSENCE</span></span> | <span data-ttu-id="9d043-442">Beurlaubung</span><span class="sxs-lookup"><span data-stu-id="9d043-442">Leave of Absence</span></span> | <span data-ttu-id="9d043-443">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="9d043-443">Terminate worker</span></span>     |
| <span data-ttu-id="9d043-444">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="9d043-444">CONTRACTEND</span></span>    | <span data-ttu-id="9d043-445">Vertragsende</span><span class="sxs-lookup"><span data-stu-id="9d043-445">End of Contract</span></span>  | <span data-ttu-id="9d043-446">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="9d043-446">Terminate worker</span></span>     |
| <span data-ttu-id="9d043-447">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="9d043-447">SALARYCHANGE</span></span>   | <span data-ttu-id="9d043-448">Gehaltsänderung</span><span class="sxs-lookup"><span data-stu-id="9d043-448">Change of Salary</span></span> | <span data-ttu-id="9d043-449">Vergütung</span><span class="sxs-lookup"><span data-stu-id="9d043-449">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="9d043-450">Familienstand</span><span class="sxs-lookup"><span data-stu-id="9d043-450">Marital status</span></span>

<span data-ttu-id="9d043-451">Familienstandwerte werden Dayforce zugeordnet und werden – je nach Bedarf – in die akzeptierten Werte bei der Integration übersetzt.</span><span class="sxs-lookup"><span data-stu-id="9d043-451">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="9d043-452">Die folgende Tabelle zeigt, wie Familienstandwerte Dayforce zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="9d043-452">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="9d043-453">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="9d043-453">Human Resources</span></span>                 | <span data-ttu-id="9d043-454">Dayforce</span><span class="sxs-lookup"><span data-stu-id="9d043-454">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="9d043-455">Verheiratet</span><span class="sxs-lookup"><span data-stu-id="9d043-455">Married</span></span>                | <span data-ttu-id="9d043-456">Verheiratet</span><span class="sxs-lookup"><span data-stu-id="9d043-456">Married</span></span>              |
| <span data-ttu-id="9d043-457">Ledig</span><span class="sxs-lookup"><span data-stu-id="9d043-457">Single</span></span>                 | <span data-ttu-id="9d043-458">Ledig</span><span class="sxs-lookup"><span data-stu-id="9d043-458">Single</span></span>               |
| <span data-ttu-id="9d043-459">Verwitwet</span><span class="sxs-lookup"><span data-stu-id="9d043-459">Widowed</span></span>                | <span data-ttu-id="9d043-460">Verwitwet</span><span class="sxs-lookup"><span data-stu-id="9d043-460">Widowed</span></span>              |
| <span data-ttu-id="9d043-461">Geschieden</span><span class="sxs-lookup"><span data-stu-id="9d043-461">Divorced</span></span>               | <span data-ttu-id="9d043-462">Geschieden</span><span class="sxs-lookup"><span data-stu-id="9d043-462">Divorced</span></span>             |
| <span data-ttu-id="9d043-463">Eingetragene Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="9d043-463">Registered Partnership</span></span> | <span data-ttu-id="9d043-464">Inländische Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="9d043-464">Domestic Partnership</span></span> |
| <span data-ttu-id="9d043-465">None</span><span class="sxs-lookup"><span data-stu-id="9d043-465">None</span></span>                   | <span data-ttu-id="9d043-466">None</span><span class="sxs-lookup"><span data-stu-id="9d043-466">None</span></span>                 |
| <span data-ttu-id="9d043-467">Freie Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="9d043-467">Cohabiting</span></span>             | <span data-ttu-id="9d043-468">Freie Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="9d043-468">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="9d043-469">Geschlecht</span><span class="sxs-lookup"><span data-stu-id="9d043-469">Gender</span></span>

<span data-ttu-id="9d043-470">Geschlechtsbezeichnungen werden Dayforce zugeordnet und werden – je nach Bedarf – in die akzeptierten Werte bei der Integration übersetzt.</span><span class="sxs-lookup"><span data-stu-id="9d043-470">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="9d043-471">Die folgende Tabelle zeigt, wie Geschlechtsbezeichnungen Dayforce zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="9d043-471">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="9d043-472">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="9d043-472">Human Resources</span></span>       | <span data-ttu-id="9d043-473">Dayforce</span><span class="sxs-lookup"><span data-stu-id="9d043-473">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="9d043-474">Männl.</span><span class="sxs-lookup"><span data-stu-id="9d043-474">Male</span></span>         | <span data-ttu-id="9d043-475">Männl.</span><span class="sxs-lookup"><span data-stu-id="9d043-475">Male</span></span>            |
| <span data-ttu-id="9d043-476">Weibl.</span><span class="sxs-lookup"><span data-stu-id="9d043-476">Female</span></span>       | <span data-ttu-id="9d043-477">Weibl.</span><span class="sxs-lookup"><span data-stu-id="9d043-477">Female</span></span>          |
| <span data-ttu-id="9d043-478">Nicht spezifisch</span><span class="sxs-lookup"><span data-stu-id="9d043-478">Non-specific</span></span> | <span data-ttu-id="9d043-479">*Nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="9d043-479">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="9d043-480">Einkommenscodes</span><span class="sxs-lookup"><span data-stu-id="9d043-480">Earning codes</span></span>

<span data-ttu-id="9d043-481">Einkommenscodes bestimmen jeden Typ von Einkünften eindeutig, die Arbeitskräfte erhalten</span><span class="sxs-lookup"><span data-stu-id="9d043-481">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="9d043-482">Die Codes decken verschiedene Parameter ab, die sich auf Einkünfte beziehen, wie beispielsweise Buchhaltungsvorschriften, Steuergesetze, Berichterstellungsanforderungen und Bruttoausgleichsfähigkeit.</span><span class="sxs-lookup"><span data-stu-id="9d043-482">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="9d043-483">Wenn eine nicht unterstützte Häufigkeit verwendet wird, wird die Häufigkeit **Jeder Lohn** standardmäßig für die Berechnung verwendet.</span><span class="sxs-lookup"><span data-stu-id="9d043-483">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="9d043-484">Unterstützte Häufigkeiten</span><span class="sxs-lookup"><span data-stu-id="9d043-484">Supported frequencies</span></span>

- <span data-ttu-id="9d043-485">Alle</span><span class="sxs-lookup"><span data-stu-id="9d043-485">All</span></span>
- <span data-ttu-id="9d043-486">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="9d043-486">EVERYPAY</span></span>
- <span data-ttu-id="9d043-487">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="9d043-487">EACHPAYPERIOD</span></span>
- <span data-ttu-id="9d043-488">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="9d043-488">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="9d043-489">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="9d043-489">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="9d043-490">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="9d043-490">1OFMTH</span></span>
- <span data-ttu-id="9d043-491">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="9d043-491">LASTOFMTH</span></span>
- <span data-ttu-id="9d043-492">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="9d043-492">2OFMTH</span></span>
- <span data-ttu-id="9d043-493">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="9d043-493">3OFMTH</span></span>
- <span data-ttu-id="9d043-494">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="9d043-494">4OFMTH</span></span>
- <span data-ttu-id="9d043-495">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="9d043-495">5OFMTH</span></span>
- <span data-ttu-id="9d043-496">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="9d043-496">1N2OFMTH</span></span>
- <span data-ttu-id="9d043-497">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="9d043-497">3N4OFMTH</span></span>
- <span data-ttu-id="9d043-498">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="9d043-498">1N3OFMTH</span></span>
- <span data-ttu-id="9d043-499">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="9d043-499">1N4OFMTH</span></span>
- <span data-ttu-id="9d043-500">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="9d043-500">2N3OFMTH</span></span>
- <span data-ttu-id="9d043-501">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="9d043-501">2N4OFMTH</span></span>
- <span data-ttu-id="9d043-502">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="9d043-502">1N2N3OFMTH</span></span>
- <span data-ttu-id="9d043-503">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="9d043-503">1N2N4OFMTH</span></span>
- <span data-ttu-id="9d043-504">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="9d043-504">1N3N4OFMTH</span></span>
- <span data-ttu-id="9d043-505">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="9d043-505">2N3N4OFMTH</span></span>
- <span data-ttu-id="9d043-506">1N2N3N4OFMTH – 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="9d043-506">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="9d043-507">2N3N4N5OFMth – 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="9d043-507">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="9d043-508">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="9d043-508">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="9d043-509">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="9d043-509">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="9d043-510">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="9d043-510">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="9d043-511">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="9d043-511">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="9d043-512">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="9d043-512">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="9d043-513">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="9d043-513">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="9d043-514">Adressen</span><span class="sxs-lookup"><span data-stu-id="9d043-514">Addresses</span></span>

<span data-ttu-id="9d043-515">Die Kennung bestimmter Codes für Land oder Region, Bundesland/Kanton oder Landkreis (Gemeinde) erfordert spezifische Formate, die Dayforce und Anbieter innerhalb des Landes/innerhalb der Region erkennen können.</span><span class="sxs-lookup"><span data-stu-id="9d043-515">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="9d043-516">Obwohl das Format für Orte flexibel ist, muss jeder Ort einem Bundesland zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="9d043-516">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="9d043-517">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="9d043-517">Human Resources</span></span>          | <span data-ttu-id="9d043-518">Dayforce</span><span class="sxs-lookup"><span data-stu-id="9d043-518">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="9d043-519">Land/Region</span><span class="sxs-lookup"><span data-stu-id="9d043-519">Country/Region</span></span>  | <span data-ttu-id="9d043-520">Ländercode</span><span class="sxs-lookup"><span data-stu-id="9d043-520">Country Code</span></span>          |
| <span data-ttu-id="9d043-521">Postleitzahl</span><span class="sxs-lookup"><span data-stu-id="9d043-521">Zip/Postal Code</span></span> | <span data-ttu-id="9d043-522">PLZ</span><span class="sxs-lookup"><span data-stu-id="9d043-522">Postal Code</span></span>           |
| <span data-ttu-id="9d043-523">Zustand</span><span class="sxs-lookup"><span data-stu-id="9d043-523">State</span></span>           | <span data-ttu-id="9d043-524">Bundeslandcode</span><span class="sxs-lookup"><span data-stu-id="9d043-524">State Code</span></span>            |
| <span data-ttu-id="9d043-525">Stadt</span><span class="sxs-lookup"><span data-stu-id="9d043-525">City</span></span>            | <span data-ttu-id="9d043-526">Stadt</span><span class="sxs-lookup"><span data-stu-id="9d043-526">City</span></span>                  |
| <span data-ttu-id="9d043-527">Verwaltungsbezirk</span><span class="sxs-lookup"><span data-stu-id="9d043-527">County</span></span>          | <span data-ttu-id="9d043-528">Landkreis (Gemeinde)</span><span class="sxs-lookup"><span data-stu-id="9d043-528">County (Municipality)</span></span> |
| <span data-ttu-id="9d043-529">Straße</span><span class="sxs-lookup"><span data-stu-id="9d043-529">Street</span></span>          | <span data-ttu-id="9d043-530">Adresszeile 1</span><span class="sxs-lookup"><span data-stu-id="9d043-530">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="9d043-531">Steuerregionen</span><span class="sxs-lookup"><span data-stu-id="9d043-531">Tax regions</span></span>

<span data-ttu-id="9d043-532">Steuerregionen werden verwendet, um die entsprechende Steuer festzulegen, die bei der Lohngenerierung angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="9d043-532">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="9d043-533">Steuerregionen werden Dayforce als Standortadressen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="9d043-533">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="9d043-534">Die Standardsteuerregion muss der aktiven Position der Arbeitskraft zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="9d043-534">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="9d043-535">Steuerregion (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-535">Tax region (required)</span></span>
- <span data-ttu-id="9d043-536">Land/Region (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-536">Country/Region (required)</span></span>
- <span data-ttu-id="9d043-537">Bundesland/Kanton (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-537">State (required)</span></span>
- <span data-ttu-id="9d043-538">Verwaltungsbezirk</span><span class="sxs-lookup"><span data-stu-id="9d043-538">County</span></span> 
- <span data-ttu-id="9d043-539">Ort (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9d043-539">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="9d043-540">Konfigurieren Ihrer Daten, um Lohn in Mexiko zu generieren</span><span class="sxs-lookup"><span data-stu-id="9d043-540">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="9d043-541">Wenn Sie Vergütung für Mitarbeiter in Mexiko generieren, müssen die folgenden Elemente konfiguriert werden:</span><span class="sxs-lookup"><span data-stu-id="9d043-541">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="9d043-542">Abteilungen sind für Positionen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9d043-542">Departments are required on positions.</span></span>
- <span data-ttu-id="9d043-543">Kostenstellen müssen als Finanzdimensionen festgelegt werden und müssen das erste Element in der standardmäßigen Finanzdimensions-Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="9d043-543">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="9d043-544">Stellentypen</span><span class="sxs-lookup"><span data-stu-id="9d043-544">Job types</span></span>

<span data-ttu-id="9d043-545">Stellentypen werden verwendet, um ähnliche Stellen in Kategorien zu gruppieren.</span><span class="sxs-lookup"><span data-stu-id="9d043-545">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="9d043-546">Stellentypen sind erforderlich, um Lohn in Mexiko zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="9d043-546">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="9d043-547">Beispiele für Stellentypen umfassen Voll- und Teilzeit oder festes Gehalt und Stundenlohn.</span><span class="sxs-lookup"><span data-stu-id="9d043-547">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="9d043-548">Stellentypen werden Dayforce als Lohnarten zugeordnet, die angeben, ob ein Mitarbeiter auf Stundenbasis bezahlt wird oder ein festes Gehalt bezieht.</span><span class="sxs-lookup"><span data-stu-id="9d043-548">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="9d043-549">Folgende Stellentypen und Beschreibungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9d043-549">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="9d043-550">Stellentyp</span><span class="sxs-lookup"><span data-stu-id="9d043-550">Job type</span></span>   | <span data-ttu-id="9d043-551">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9d043-551">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="9d043-552">Stündlich</span><span class="sxs-lookup"><span data-stu-id="9d043-552">Hourly</span></span>     | <span data-ttu-id="9d043-553">MX – Stundenbasis</span><span class="sxs-lookup"><span data-stu-id="9d043-553">MX Hourly</span></span>   |
| <span data-ttu-id="9d043-554">Fest angestellt</span><span class="sxs-lookup"><span data-stu-id="9d043-554">Salaried</span></span>   | <span data-ttu-id="9d043-555">MX – Fest angestellt</span><span class="sxs-lookup"><span data-stu-id="9d043-555">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="9d043-556">Positionstypen</span><span class="sxs-lookup"><span data-stu-id="9d043-556">Position types</span></span> 

<span data-ttu-id="9d043-557">Sie verwenden Positionstypen, um zu beschreiben, ob die Position Vollzeit, Teilzeit oder etwas anderes ist.</span><span class="sxs-lookup"><span data-stu-id="9d043-557">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="9d043-558">Positionstypen werden Dayforce als Lohnklassen zugeordnet, die angeben, ob ein Mitarbeiter in Vollzeit oder Teilzeit arbeitet.</span><span class="sxs-lookup"><span data-stu-id="9d043-558">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="9d043-559">Folgende Positionstypen und Beschreibungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9d043-559">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="9d043-560">Positionstyp</span><span class="sxs-lookup"><span data-stu-id="9d043-560">Position type</span></span>   | <span data-ttu-id="9d043-561">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9d043-561">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="9d043-562">Vollzeit</span><span class="sxs-lookup"><span data-stu-id="9d043-562">Full-time</span></span>       | <span data-ttu-id="9d043-563">Vollzeitmitarbeiter</span><span class="sxs-lookup"><span data-stu-id="9d043-563">Full time employee</span></span> |
| <span data-ttu-id="9d043-564">Teilzeit</span><span class="sxs-lookup"><span data-stu-id="9d043-564">Part-time</span></span>       | <span data-ttu-id="9d043-565">Teilzeitmitarbeiter</span><span class="sxs-lookup"><span data-stu-id="9d043-565">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="9d043-566">Ursachencodes</span><span class="sxs-lookup"><span data-stu-id="9d043-566">Reason codes</span></span>

<span data-ttu-id="9d043-567">Ursachencodes enthalten Informationen zum Status eines Mitarbeiters.</span><span class="sxs-lookup"><span data-stu-id="9d043-567">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="9d043-568">Ursachencodes werden Dayforce als Statusgründe zugeordnet, die den Grund für Änderungen bei der Position eines Mitarbeiters oder dem Beschäftigungsstatus angeben.</span><span class="sxs-lookup"><span data-stu-id="9d043-568">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="9d043-569">Folgende Ursachencodes und Beschreibungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9d043-569">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="9d043-570">Ursachencode</span><span class="sxs-lookup"><span data-stu-id="9d043-570">Reason code</span></span>            | <span data-ttu-id="9d043-571">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9d043-571">Description</span></span>                    | <span data-ttu-id="9d043-572">Zutreffende Szenarios</span><span class="sxs-lookup"><span data-stu-id="9d043-572">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="9d043-573">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="9d043-573">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="9d043-574">Abgang vor erster Lohnzahlung</span><span class="sxs-lookup"><span data-stu-id="9d043-574">Departure before first payroll</span></span> | <span data-ttu-id="9d043-575">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="9d043-575">Terminate worker</span></span>     |
| <span data-ttu-id="9d043-576">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="9d043-576">RESIGNATION</span></span>            | <span data-ttu-id="9d043-577">Kündigung durch Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="9d043-577">Resignation</span></span>                    | <span data-ttu-id="9d043-578">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="9d043-578">Terminate worker</span></span>     |
| <span data-ttu-id="9d043-579">PENSION</span><span class="sxs-lookup"><span data-stu-id="9d043-579">PENSION</span></span>                | <span data-ttu-id="9d043-580">Rente</span><span class="sxs-lookup"><span data-stu-id="9d043-580">Pension</span></span>                        | <span data-ttu-id="9d043-581">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="9d043-581">Terminate worker</span></span>     |
| <span data-ttu-id="9d043-582">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="9d043-582">TERMINATION</span></span>            | <span data-ttu-id="9d043-583">Beendigung</span><span class="sxs-lookup"><span data-stu-id="9d043-583">Termination</span></span>                    | <span data-ttu-id="9d043-584">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="9d043-584">Terminate worker</span></span>     |
| <span data-ttu-id="9d043-585">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="9d043-585">RETIREMENT</span></span>             | <span data-ttu-id="9d043-586">Ruhestand</span><span class="sxs-lookup"><span data-stu-id="9d043-586">Retirement</span></span>                     | <span data-ttu-id="9d043-587">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="9d043-587">Terminate worker</span></span>     |
| <span data-ttu-id="9d043-588">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="9d043-588">ABSENTEE</span></span>               | <span data-ttu-id="9d043-589">Abwesende Person</span><span class="sxs-lookup"><span data-stu-id="9d043-589">Absentee</span></span>                       | <span data-ttu-id="9d043-590">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="9d043-590">Terminate worker</span></span>     |
| <span data-ttu-id="9d043-591">OTHER</span><span class="sxs-lookup"><span data-stu-id="9d043-591">OTHER</span></span>                  | <span data-ttu-id="9d043-592">Andere Gründe</span><span class="sxs-lookup"><span data-stu-id="9d043-592">Other Reasons</span></span>                  | <span data-ttu-id="9d043-593">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="9d043-593">Terminate worker</span></span>     |
| <span data-ttu-id="9d043-594">CLOSURE</span><span class="sxs-lookup"><span data-stu-id="9d043-594">CLOSURE</span></span>                | <span data-ttu-id="9d043-595">Betriebsferien</span><span class="sxs-lookup"><span data-stu-id="9d043-595">Business Closure</span></span>               | <span data-ttu-id="9d043-596">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="9d043-596">Terminate worker</span></span>     |
| <span data-ttu-id="9d043-597">DEATH</span><span class="sxs-lookup"><span data-stu-id="9d043-597">DEATH</span></span>                  | <span data-ttu-id="9d043-598">Tod</span><span class="sxs-lookup"><span data-stu-id="9d043-598">Death</span></span>                          | <span data-ttu-id="9d043-599">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="9d043-599">Terminate worker</span></span>     |
| <span data-ttu-id="9d043-600">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="9d043-600">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="9d043-601">Beurlaubung</span><span class="sxs-lookup"><span data-stu-id="9d043-601">Leave of Absence</span></span>               | <span data-ttu-id="9d043-602">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="9d043-602">Terminate worker</span></span>     |
| <span data-ttu-id="9d043-603">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="9d043-603">CONTRACTEND</span></span>            | <span data-ttu-id="9d043-604">Vertragsende</span><span class="sxs-lookup"><span data-stu-id="9d043-604">End of Contract</span></span>                | <span data-ttu-id="9d043-605">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="9d043-605">Terminate worker</span></span>     |
| <span data-ttu-id="9d043-606">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="9d043-606">SALARYCHANGE</span></span>           | <span data-ttu-id="9d043-607">Gehaltsänderung</span><span class="sxs-lookup"><span data-stu-id="9d043-607">Change of Salary</span></span>               | <span data-ttu-id="9d043-608">Vergütung</span><span class="sxs-lookup"><span data-stu-id="9d043-608">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="9d043-609">Einstellungsbedingungen</span><span class="sxs-lookup"><span data-stu-id="9d043-609">Terms of employment</span></span>

<span data-ttu-id="9d043-610">Beschäftigungsbedingungen werden verwendet, um Kategorien von Beschäftigungsbedingungen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9d043-610">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="9d043-611">Die Bedingungen werden Dayforce als Beschäftigungsindikatorwerte zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="9d043-611">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="9d043-612">Die folgenden Bedingungen für Beschäftigung und Beschreibungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9d043-612">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="9d043-613">Einstellungsbedingungen</span><span class="sxs-lookup"><span data-stu-id="9d043-613">Terms of employment</span></span>   | <span data-ttu-id="9d043-614">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9d043-614">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="9d043-615">Regelmäßig</span><span class="sxs-lookup"><span data-stu-id="9d043-615">Regular</span></span>               | <span data-ttu-id="9d043-616">Regelmäßig</span><span class="sxs-lookup"><span data-stu-id="9d043-616">Regular</span></span>     |
| <span data-ttu-id="9d043-617">Direkt</span><span class="sxs-lookup"><span data-stu-id="9d043-617">Direct</span></span>                | <span data-ttu-id="9d043-618">Direkt</span><span class="sxs-lookup"><span data-stu-id="9d043-618">Direct</span></span>      |
| <span data-ttu-id="9d043-619">Praktikum</span><span class="sxs-lookup"><span data-stu-id="9d043-619">Internship</span></span>            | <span data-ttu-id="9d043-620">Praktikum</span><span class="sxs-lookup"><span data-stu-id="9d043-620">Internship</span></span>  |
| <span data-ttu-id="9d043-621">Unbefristet</span><span class="sxs-lookup"><span data-stu-id="9d043-621">Permanent</span></span>             | <span data-ttu-id="9d043-622">Unbefristet</span><span class="sxs-lookup"><span data-stu-id="9d043-622">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="9d043-623">Familienstand</span><span class="sxs-lookup"><span data-stu-id="9d043-623">Marital status</span></span>

<span data-ttu-id="9d043-624">Familienstandwerte werden Dayforce zugeordnet und werden – je nach Bedarf – in die akzeptierten Werte bei der Integration übersetzt.</span><span class="sxs-lookup"><span data-stu-id="9d043-624">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="9d043-625">Die folgende Tabelle zeigt, wie Familienstandwerte Dayforce zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="9d043-625">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="9d043-626">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="9d043-626">Human Resources</span></span>                 | <span data-ttu-id="9d043-627">Dayforce</span><span class="sxs-lookup"><span data-stu-id="9d043-627">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="9d043-628">Verheiratet</span><span class="sxs-lookup"><span data-stu-id="9d043-628">Married</span></span>                | <span data-ttu-id="9d043-629">Verheiratet</span><span class="sxs-lookup"><span data-stu-id="9d043-629">Married</span></span>                   |
| <span data-ttu-id="9d043-630">Ledig</span><span class="sxs-lookup"><span data-stu-id="9d043-630">Single</span></span>                 | <span data-ttu-id="9d043-631">Ledig</span><span class="sxs-lookup"><span data-stu-id="9d043-631">Single</span></span>                    |
| <span data-ttu-id="9d043-632">Verwitwet</span><span class="sxs-lookup"><span data-stu-id="9d043-632">Widowed</span></span>                | <span data-ttu-id="9d043-633">Verwitwet</span><span class="sxs-lookup"><span data-stu-id="9d043-633">Widowed</span></span>                   |
| <span data-ttu-id="9d043-634">Geschieden</span><span class="sxs-lookup"><span data-stu-id="9d043-634">Divorced</span></span>               | <span data-ttu-id="9d043-635">Geschieden</span><span class="sxs-lookup"><span data-stu-id="9d043-635">Divorced</span></span>                  |
| <span data-ttu-id="9d043-636">Eingetragene Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="9d043-636">Registered Partnership</span></span> | <span data-ttu-id="9d043-637">Inländische Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="9d043-637">Domestic Partnership</span></span>      |
| <span data-ttu-id="9d043-638">None</span><span class="sxs-lookup"><span data-stu-id="9d043-638">None</span></span>                   | <span data-ttu-id="9d043-639">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="9d043-639">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="9d043-640">Freie Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="9d043-640">Cohabiting</span></span>             | <span data-ttu-id="9d043-641">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="9d043-641">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="9d043-642">Geschlecht</span><span class="sxs-lookup"><span data-stu-id="9d043-642">Gender</span></span>

<span data-ttu-id="9d043-643">Geschlechtsbezeichnungen werden Dayforce zugeordnet und werden – je nach Bedarf – in die akzeptierten Werte bei der Integration übersetzt.</span><span class="sxs-lookup"><span data-stu-id="9d043-643">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="9d043-644">Die folgende Tabelle zeigt, wie Geschlechtsbezeichnungen Dayforce zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="9d043-644">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="9d043-645">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="9d043-645">Human Resources</span></span>       | <span data-ttu-id="9d043-646">Dayforce</span><span class="sxs-lookup"><span data-stu-id="9d043-646">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="9d043-647">Männl.</span><span class="sxs-lookup"><span data-stu-id="9d043-647">Male</span></span>         | <span data-ttu-id="9d043-648">Männl.</span><span class="sxs-lookup"><span data-stu-id="9d043-648">Male</span></span>                      |
| <span data-ttu-id="9d043-649">Weibl.</span><span class="sxs-lookup"><span data-stu-id="9d043-649">Female</span></span>       | <span data-ttu-id="9d043-650">Weibl.</span><span class="sxs-lookup"><span data-stu-id="9d043-650">Female</span></span>                    |
| <span data-ttu-id="9d043-651">Nicht spezifisch</span><span class="sxs-lookup"><span data-stu-id="9d043-651">Non-specific</span></span> | <span data-ttu-id="9d043-652">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="9d043-652">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="9d043-653">Zahlungsweise</span><span class="sxs-lookup"><span data-stu-id="9d043-653">Payment method</span></span>

<span data-ttu-id="9d043-654">Zahlungsmethoden geben dem Mitarbeiter und dem Unternehmen die Möglichkeit zu beschreiben, wie Mitarbeiter bezahlt werden.</span><span class="sxs-lookup"><span data-stu-id="9d043-654">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="9d043-655">Zahlungsmethoden werden Dayforce zugeordnet und werden – je nach Bedarf – in die akzeptierten Werte bei der Integration übersetzt.</span><span class="sxs-lookup"><span data-stu-id="9d043-655">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="9d043-656">Die folgende Tabelle zeigt, wie Zahlungsmethoden Dayforce zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="9d043-656">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="9d043-657">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="9d043-657">Human Resources</span></span>             | <span data-ttu-id="9d043-658">Dayforce</span><span class="sxs-lookup"><span data-stu-id="9d043-658">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="9d043-659">Bargeld</span><span class="sxs-lookup"><span data-stu-id="9d043-659">Cash</span></span>               | <span data-ttu-id="9d043-660">Bargeld</span><span class="sxs-lookup"><span data-stu-id="9d043-660">Cash</span></span>                      |
| <span data-ttu-id="9d043-661">Elektronische Zahlung</span><span class="sxs-lookup"><span data-stu-id="9d043-661">Electronic Payment</span></span> | <span data-ttu-id="9d043-662">Übertragen</span><span class="sxs-lookup"><span data-stu-id="9d043-662">Transfer</span></span>                  |
| <span data-ttu-id="9d043-663">Prüfen</span><span class="sxs-lookup"><span data-stu-id="9d043-663">Check</span></span>              | <span data-ttu-id="9d043-664">Scheck</span><span class="sxs-lookup"><span data-stu-id="9d043-664">Cheque</span></span>                    |
| <span data-ttu-id="9d043-665">Bankwechsel</span><span class="sxs-lookup"><span data-stu-id="9d043-665">Bank Draft</span></span>         | <span data-ttu-id="9d043-666">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="9d043-666">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="9d043-667">Sonstige</span><span class="sxs-lookup"><span data-stu-id="9d043-667">Other</span></span>              | <span data-ttu-id="9d043-668">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="9d043-668">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="9d043-669">Bankkontotyp</span><span class="sxs-lookup"><span data-stu-id="9d043-669">Bank account type</span></span>

<span data-ttu-id="9d043-670">Bankkontotypen werden für elektronische Zahlungen an Mitarbeiter verwendet.</span><span class="sxs-lookup"><span data-stu-id="9d043-670">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="9d043-671">Bankkontotypen werden Dayforce als Übergweisungskontoinformationen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="9d043-671">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="9d043-672">Die Bankkontotypen werden bei Bedarf zu den akzeptierten Werte nach der Integration übersetzt.</span><span class="sxs-lookup"><span data-stu-id="9d043-672">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="9d043-673">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="9d043-673">Human Resources</span></span>            | <span data-ttu-id="9d043-674">Dayforce</span><span class="sxs-lookup"><span data-stu-id="9d043-674">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="9d043-675">Girokonto</span><span class="sxs-lookup"><span data-stu-id="9d043-675">Checking Account</span></span>  | <span data-ttu-id="9d043-676">Girokonto</span><span class="sxs-lookup"><span data-stu-id="9d043-676">CheckingAccount</span></span>           |
| <span data-ttu-id="9d043-677">Lohnkonto</span><span class="sxs-lookup"><span data-stu-id="9d043-677">Payroll Account</span></span>   | <span data-ttu-id="9d043-678">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="9d043-678">PayrollAccount</span></span>            |
| <span data-ttu-id="9d043-679">Sparkonto</span><span class="sxs-lookup"><span data-stu-id="9d043-679">Savings Account</span></span>   | <span data-ttu-id="9d043-680">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="9d043-680">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="9d043-681">BankGirot-Konto</span><span class="sxs-lookup"><span data-stu-id="9d043-681">BankGirot account</span></span> | <span data-ttu-id="9d043-682">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="9d043-682">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="9d043-683">PlusGirot-Konto</span><span class="sxs-lookup"><span data-stu-id="9d043-683">PlusGirot account</span></span> | <span data-ttu-id="9d043-684">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="9d043-684">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="9d043-685">Einkommenscodes</span><span class="sxs-lookup"><span data-stu-id="9d043-685">Earning codes</span></span>

<span data-ttu-id="9d043-686">Einkommenscodes bestimmen jeden Typ von Einkünften eindeutig, die Arbeitskräfte erhalten</span><span class="sxs-lookup"><span data-stu-id="9d043-686">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="9d043-687">Die Codes decken verschiedene Parameter ab, die sich auf Einkünfte beziehen, wie beispielsweise Buchhaltungsvorschriften, Steuergesetze, Berichterstellungsanforderungen und Bruttoausgleichsfähigkeit.</span><span class="sxs-lookup"><span data-stu-id="9d043-687">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="9d043-688">Wenn eine nicht unterstützte Häufigkeit verwendet wird, wird die Häufigkeit **Jeder Lohn** standardmäßig für die Berechnung verwendet.</span><span class="sxs-lookup"><span data-stu-id="9d043-688">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="9d043-689">Unterstützte Häufigkeiten</span><span class="sxs-lookup"><span data-stu-id="9d043-689">Supported frequencies</span></span>

- <span data-ttu-id="9d043-690">Alle</span><span class="sxs-lookup"><span data-stu-id="9d043-690">All</span></span>
- <span data-ttu-id="9d043-691">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="9d043-691">EVERYPAY</span></span>
- <span data-ttu-id="9d043-692">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="9d043-692">EACHPAYPERIOD</span></span>
- <span data-ttu-id="9d043-693">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="9d043-693">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="9d043-694">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="9d043-694">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="9d043-695">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="9d043-695">1OFMTH</span></span>
- <span data-ttu-id="9d043-696">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="9d043-696">LASTOFMTH</span></span>
- <span data-ttu-id="9d043-697">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="9d043-697">2OFMTH</span></span>
- <span data-ttu-id="9d043-698">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="9d043-698">3OFMTH</span></span>
- <span data-ttu-id="9d043-699">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="9d043-699">4OFMTH</span></span>
- <span data-ttu-id="9d043-700">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="9d043-700">5OFMTH</span></span>
- <span data-ttu-id="9d043-701">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="9d043-701">1N2OFMTH</span></span>
- <span data-ttu-id="9d043-702">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="9d043-702">3N4OFMTH</span></span>
- <span data-ttu-id="9d043-703">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="9d043-703">1N3OFMTH</span></span>
- <span data-ttu-id="9d043-704">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="9d043-704">1N4OFMTH</span></span>
- <span data-ttu-id="9d043-705">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="9d043-705">2N3OFMTH</span></span>
- <span data-ttu-id="9d043-706">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="9d043-706">2N4OFMTH</span></span>
- <span data-ttu-id="9d043-707">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="9d043-707">1N2N3OFMTH</span></span>
- <span data-ttu-id="9d043-708">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="9d043-708">1N2N4OFMTH</span></span>
- <span data-ttu-id="9d043-709">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="9d043-709">1N3N4OFMTH</span></span>
- <span data-ttu-id="9d043-710">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="9d043-710">2N3N4OFMTH</span></span>
- <span data-ttu-id="9d043-711">1N2N3N4OFMTH – 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="9d043-711">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="9d043-712">2N3N4N5OFMth – 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="9d043-712">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="9d043-713">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="9d043-713">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="9d043-714">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="9d043-714">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="9d043-715">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="9d043-715">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="9d043-716">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="9d043-716">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="9d043-717">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="9d043-717">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="9d043-718">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="9d043-718">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="9d043-719">Adressen</span><span class="sxs-lookup"><span data-stu-id="9d043-719">Addresses</span></span>

<span data-ttu-id="9d043-720">Die Kennung bestimmter Codes für Land oder Region, Bundesland/Kanton oder Landkreis (Gemeinde) erfordert spezifische Formate, die Dayforce und Anbieter innerhalb des Landes/innerhalb der Region erkennen können.</span><span class="sxs-lookup"><span data-stu-id="9d043-720">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="9d043-721">Obwohl das Format für Orte flexibel ist, muss jeder Ort einem Bundesland zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="9d043-721">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="9d043-722">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="9d043-722">Human Resources</span></span>              | <span data-ttu-id="9d043-723">Dayforce</span><span class="sxs-lookup"><span data-stu-id="9d043-723">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="9d043-724">Land/Region</span><span class="sxs-lookup"><span data-stu-id="9d043-724">Country/Region</span></span>      | <span data-ttu-id="9d043-725">Ländercode</span><span class="sxs-lookup"><span data-stu-id="9d043-725">Country Code</span></span>          |
| <span data-ttu-id="9d043-726">Postleitzahl</span><span class="sxs-lookup"><span data-stu-id="9d043-726">Zip/Postal Code</span></span>     | <span data-ttu-id="9d043-727">PLZ</span><span class="sxs-lookup"><span data-stu-id="9d043-727">Postal Code</span></span>           |
| <span data-ttu-id="9d043-728">Zustand</span><span class="sxs-lookup"><span data-stu-id="9d043-728">State</span></span>               | <span data-ttu-id="9d043-729">Bundeslandcode</span><span class="sxs-lookup"><span data-stu-id="9d043-729">State Code</span></span>            |
| <span data-ttu-id="9d043-730">Stadt</span><span class="sxs-lookup"><span data-stu-id="9d043-730">City</span></span>                | <span data-ttu-id="9d043-731">Stadt</span><span class="sxs-lookup"><span data-stu-id="9d043-731">City</span></span>                  |
| <span data-ttu-id="9d043-732">Verwaltungsbezirk</span><span class="sxs-lookup"><span data-stu-id="9d043-732">County</span></span>              | <span data-ttu-id="9d043-733">Landkreis (Gemeinde)</span><span class="sxs-lookup"><span data-stu-id="9d043-733">County (Municipality)</span></span> |
| <span data-ttu-id="9d043-734">Straße</span><span class="sxs-lookup"><span data-stu-id="9d043-734">Street</span></span>              | <span data-ttu-id="9d043-735">Adresszeile 1</span><span class="sxs-lookup"><span data-stu-id="9d043-735">Address Line 1</span></span>        |
| <span data-ttu-id="9d043-736">Hausnummer</span><span class="sxs-lookup"><span data-stu-id="9d043-736">Street Number</span></span>       | <span data-ttu-id="9d043-737">Adresszeile 2</span><span class="sxs-lookup"><span data-stu-id="9d043-737">Address Line 2</span></span>        |
| <span data-ttu-id="9d043-738">Gebäudeergänzung</span><span class="sxs-lookup"><span data-stu-id="9d043-738">Building Complement</span></span> | <span data-ttu-id="9d043-739">Adresszeile 5</span><span class="sxs-lookup"><span data-stu-id="9d043-739">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="9d043-740">Ausweisnummer</span><span class="sxs-lookup"><span data-stu-id="9d043-740">Passport number</span></span>

<span data-ttu-id="9d043-741">Mitarbeiter können Ausweisinformationen melden.</span><span class="sxs-lookup"><span data-stu-id="9d043-741">Employees can declare passport information.</span></span> <span data-ttu-id="9d043-742">Diese Informationen haben den Kennungstyp **Ausweis** und sind in Dayforce als Teil der für Mexiko spezifischen Informationen eines Mitarbeiters integriert.</span><span class="sxs-lookup"><span data-stu-id="9d043-742">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="9d043-743">Kennungstyp = „Ausweis”</span><span class="sxs-lookup"><span data-stu-id="9d043-743">Identification Type = "Passport"</span></span>
- <span data-ttu-id="9d043-744">Ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="9d043-744">Issued Date</span></span>
- <span data-ttu-id="9d043-745">Ablaufdatum</span><span class="sxs-lookup"><span data-stu-id="9d043-745">Expiration Date</span></span>

<span data-ttu-id="9d043-746">Mitarbeiter können mehrere Kennungsnummern des Kennungstyps **Ausweis** melden.</span><span class="sxs-lookup"><span data-stu-id="9d043-746">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="9d043-747">Jedoch wird nur der aktuell aktive Ausweiseintrag in Dayforce integriert.</span><span class="sxs-lookup"><span data-stu-id="9d043-747">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="9d043-748">Wenn alle Ausweiseinträge abgelaufen sind, ist der Ausweis, der zuletzt ausgestellt wurde, in Dayforce integriert.</span><span class="sxs-lookup"><span data-stu-id="9d043-748">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]