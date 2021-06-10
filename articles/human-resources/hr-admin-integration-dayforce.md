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
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6d150daa92fe79cf6620ce5ddf1a01f369c64053
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051496"
---
# <a name="configure-integration-with-dayforce"></a><span data-ttu-id="b43c9-104">Integration mit Dayforce konfigurieren</span><span class="sxs-lookup"><span data-stu-id="b43c9-104">Configure integration with Dayforce</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="b43c9-105">Die Integration zwischen Microsoft Dynamics 365 Human Resources und Ceridian Dayforce erfordert mehrere Konfigurationsschritte, die in diesem Artikel beschrieben sind.</span><span class="sxs-lookup"><span data-stu-id="b43c9-105">The integration between Microsoft Dynamics 365 Human Resources and Ceridian Dayforce relies on several configuration steps that are described in this article.</span></span> <span data-ttu-id="b43c9-106">Sie müssen die Integration sowohl in Human Resources als auch in Dayforce konfigurieren, bevor Sie einen Zahlungslauf verarbeiten können.</span><span class="sxs-lookup"><span data-stu-id="b43c9-106">You must configure the integration in both Human Resources and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="b43c9-107">Wenn Sie einen Dienst wie Dayforce verwenden, um Zahlungsläufe abzuschließen, müssen Sie die Integration in Human Resources ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="b43c9-107">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Human Resources.</span></span> <span data-ttu-id="b43c9-108">Die Integration erfordert bestimmte Daten aus Human Resources.</span><span class="sxs-lookup"><span data-stu-id="b43c9-108">The integration requires specific data from Human Resources.</span></span> <span data-ttu-id="b43c9-109">Daher müssen Sie überprüfen, dass die Daten, die Dayforce zugeordnet sind, in Human Resources in einer Weise konfiguriert werden, die die Integration unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b43c9-109">Therefore, you must verify that data that is mapped to Dayforce is configured in Human Resources in a manner that supports the integration.</span></span> <span data-ttu-id="b43c9-110">Bei der Integration werden die folgenden allgemeinen Kategorien von Daten verwendet:</span><span class="sxs-lookup"><span data-stu-id="b43c9-110">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="b43c9-111">Personalverwaltungsdaten</span><span class="sxs-lookup"><span data-stu-id="b43c9-111">Human resources data</span></span>
- <span data-ttu-id="b43c9-112">Vergütungsdaten</span><span class="sxs-lookup"><span data-stu-id="b43c9-112">Compensation data</span></span>
- <span data-ttu-id="b43c9-113">Lohndaten, wie Lohnzyklen, Lohnperioden und Einkommenscodes</span><span class="sxs-lookup"><span data-stu-id="b43c9-113">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="b43c9-114">Arbeitskraftdaten</span><span class="sxs-lookup"><span data-stu-id="b43c9-114">Worker data</span></span>

<span data-ttu-id="b43c9-115">In diesem Artikel werden die Schritte beschrieben, die Sie befolgen müssen, um die Integration zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="b43c9-115">This article describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="b43c9-116">Es werden auch die Datentypen und die Konfigurationsdetails erklärt, die für die Integration erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="b43c9-116">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="b43c9-117">Die Integration aktivieren</span><span class="sxs-lookup"><span data-stu-id="b43c9-117">Enable the integration</span></span>

<span data-ttu-id="b43c9-118">In Human Resources müssen Sie die Integration aktivieren und die Konfigurationsinformationen eingeben, um eine Verbindung mit Dayforce herzustellen.</span><span class="sxs-lookup"><span data-stu-id="b43c9-118">In Human Resources, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="b43c9-119">Wenn Sie möchten, dass die erstellte Hauptbuchtransaktion in Microsoft Dynamics 365 Finance importiert wird, müssen Sie auch ein Microsoft Azure-Speicherkonto einrichten und die Azure Storage-Verbindungszeichenfolge in Finance eingeben.</span><span class="sxs-lookup"><span data-stu-id="b43c9-119">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 Finance, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance.</span></span>

<span data-ttu-id="b43c9-120">Um die Integration in Human Resources zu aktivieren, gehen Sie folgendermaßen vor.</span><span class="sxs-lookup"><span data-stu-id="b43c9-120">To turn on the integration in Human Resources, follow these steps.</span></span>

1. <span data-ttu-id="b43c9-121">Wählen Sie auf der Seite **Systemverwaltung** die Option **Integrationskonfiguration** aus.</span><span class="sxs-lookup"><span data-stu-id="b43c9-121">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="b43c9-122">Geben Sie den sicheren Datenübertragungsprotokoll-(FTP)-Endpunkt und den sicheren FTP-Ordnerpfad ein.</span><span class="sxs-lookup"><span data-stu-id="b43c9-122">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="b43c9-123">Geben Sie den Benutzernamen und das Kennwort des Benutzers ein, der auf den sicheren FTP-Endpunkt und Ordnerpfad zugreift.</span><span class="sxs-lookup"><span data-stu-id="b43c9-123">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="b43c9-124">Testen Sie die Verbindung nach Bedarf, und legen Sie die Option **Lohnintegration aktivieren** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="b43c9-124">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="b43c9-125">Wenn die Integration aktiviert ist, werden Datenexportpaket und Dateien erstellt und die Häufigkeit wird festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b43c9-125">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="b43c9-126">Sie können diese Häufigkeit nach Bedarf ändern.</span><span class="sxs-lookup"><span data-stu-id="b43c9-126">You can change this frequency as you require.</span></span>

<span data-ttu-id="b43c9-127">Weitere Informationen zu Azure-Speicherkonten und Azure Storage-Verbindungszeichenfolgen finden Sie in den folgenden Azure-Artikeln:</span><span class="sxs-lookup"><span data-stu-id="b43c9-127">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure articles:</span></span>

- [<span data-ttu-id="b43c9-128">Über Azure-Speicherkonten</span><span class="sxs-lookup"><span data-stu-id="b43c9-128">About Azure storage accounts</span></span>](/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="b43c9-129">Azure Storage-Verbindungszeichenfolgen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="b43c9-129">Configure Azure Storage connection strings</span></span>](/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="b43c9-130">Technische Details, wenn Lohnintegration aktiviert ist</span><span class="sxs-lookup"><span data-stu-id="b43c9-130">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="b43c9-131">Die Aktivierung von Lohnintegration hat zwei primäre Auswirkungen:</span><span class="sxs-lookup"><span data-stu-id="b43c9-131">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="b43c9-132">Ein Datenexportprojekt namens „Lohnintegrationsexport“ wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="b43c9-132">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="b43c9-133">Dieses Projekt enthält die Entitäten und Felder, die für die Lohnintegration erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="b43c9-133">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="b43c9-134">Um das Projekt zu überprüfen, wechseln Sie zu **Systemverwaltung**, wählen Sie die Kachel **Datenverwaltung** aus, und öffnen Sie anschließend das Datenprojekt aus der Projektliste.</span><span class="sxs-lookup"><span data-stu-id="b43c9-134">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="b43c9-135">Dieser Stapelverarbeitungsauftrag führt das Datenexportprojekt aus, verschlüsselt das Datenpaket und überträgt die Datenenpaketdatei auf den SFTP-Endpunkt, der auf dem Bildschirm **Integrationskonfiguration** konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="b43c9-135">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="b43c9-136">Das Datenpaket, das zum SFTP-Endpunkt übertragen wird, wird mit einem Schlüssel verschlüsselt, für das Paket eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="b43c9-136">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="b43c9-137">Der Schlüssel befindet sich in einer Azure Key Vault, auf den nur durch Ceridian zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="b43c9-137">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="b43c9-138">Es ist nicht möglich, die Datenpaketinhalte zu entschlüsseln und zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="b43c9-138">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="b43c9-139">Wenn Sie den Inhalt des Datenpakets überprüfen möchten, müssen Sie das Datenprojekt „Lohnintegrationsexport“ manuell exportieren, herunterladen und dann öffnen.</span><span class="sxs-lookup"><span data-stu-id="b43c9-139">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="b43c9-140">Beim manuellen Export wird keine Verschlüsselung angewendet oder das Paket übertragen.</span><span class="sxs-lookup"><span data-stu-id="b43c9-140">Manual export will not apply encryption or transfer the package.</span></span>
> <span data-ttu-id="b43c9-141">Für Fälle, in denen die Integrationsdateien von einer Dynamics 365 Human Resources-UAT- oder Sandbox-Umgebung für eine Ceridian Dayforce-Testumgebung gesendet werden, können Sie die folgende URL des Schlüsseltresors verwenden: https://payrollintegrationprod.vault.azure.net.</span><span class="sxs-lookup"><span data-stu-id="b43c9-141">For instances where the integration files are sent from a Dynamics 365 Human Resources UAT or Sandbox environment to a Ceridian Dayforce Test environment, you can use the following key vault URL: https://payrollintegrationprod.vault.azure.net.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="b43c9-142">Ihre Daten konfigurieren</span><span class="sxs-lookup"><span data-stu-id="b43c9-142">Configure your data</span></span> 

<span data-ttu-id="b43c9-143">Um die Lohnbuchung zu verarbeiten, müssen Sie Personalverwaltungsdaten in Human Resources konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="b43c9-143">To process payroll, you must configure human resource data in Human Resources.</span></span> <span data-ttu-id="b43c9-144">Sie müssen Organisationsdaten, wie Stellen und Positionen, zusammen mit Vorteilen Vergütungsinformationen einrichten.</span><span class="sxs-lookup"><span data-stu-id="b43c9-144">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="b43c9-145">Diese Informationen stellen Beschäftigung, Lohn und die Abzugsinformationen bereit, die zur Generierung der Mitarbeiterentlohnung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="b43c9-145">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="b43c9-146">Personalverwaltungsdaten</span><span class="sxs-lookup"><span data-stu-id="b43c9-146">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="b43c9-147">Vergütungen</span><span class="sxs-lookup"><span data-stu-id="b43c9-147">Benefits</span></span> 

<span data-ttu-id="b43c9-148">Die Personalverwaltung stellt eine Reihe von Tools für die Einrichtung und Verwaltung der Vorteile, Abzüge und Vergütungspläne der Arbeitskräfte bereit, die eine Organisation für seine Arbeitskräfte anbietet oder verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="b43c9-148">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="b43c9-149">Wenn Sie Vorteile erstellen, sollten Sie folgende Daten und Konfigurationen bedenken, die in Dayforce verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b43c9-149">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="b43c9-150">Vorteilspläne</span><span class="sxs-lookup"><span data-stu-id="b43c9-150">Benefit plans</span></span>

- <span data-ttu-id="b43c9-151">Plan (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-151">Plan (required)</span></span>
- <span data-ttu-id="b43c9-152">Typ (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-152">Type (required)</span></span>
- <span data-ttu-id="b43c9-153">Lohnauswirkung (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-153">Payroll impact (required)</span></span>
- <span data-ttu-id="b43c9-154">Rückstände wiederherstellen</span><span class="sxs-lookup"><span data-stu-id="b43c9-154">Recover arrears</span></span>
- <span data-ttu-id="b43c9-155">Abzugsverfahren</span><span class="sxs-lookup"><span data-stu-id="b43c9-155">Deduction method</span></span>
- <span data-ttu-id="b43c9-156">Abzugspriorität</span><span class="sxs-lookup"><span data-stu-id="b43c9-156">Deduction priority</span></span>
- <span data-ttu-id="b43c9-157">Periode eingrenzen</span><span class="sxs-lookup"><span data-stu-id="b43c9-157">Limit period</span></span>
- <span data-ttu-id="b43c9-158">Limitbetrag</span><span class="sxs-lookup"><span data-stu-id="b43c9-158">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="b43c9-159">Vergütungen</span><span class="sxs-lookup"><span data-stu-id="b43c9-159">Benefits</span></span>

- <span data-ttu-id="b43c9-160">Plan (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-160">Plan (required)</span></span>
- <span data-ttu-id="b43c9-161">Typ (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-161">Type (required)</span></span>
- <span data-ttu-id="b43c9-162">Option (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-162">Option (required)</span></span>
- <span data-ttu-id="b43c9-163">Vorteilskennung (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-163">Benefit ID (required)</span></span>
- <span data-ttu-id="b43c9-164">Häufigkeit</span><span class="sxs-lookup"><span data-stu-id="b43c9-164">Frequency</span></span>
- <span data-ttu-id="b43c9-165">Basis</span><span class="sxs-lookup"><span data-stu-id="b43c9-165">Basis</span></span>
- <span data-ttu-id="b43c9-166">Betrag oder Satz</span><span class="sxs-lookup"><span data-stu-id="b43c9-166">Amount or rate</span></span>
- <span data-ttu-id="b43c9-167">Einkommenscode</span><span class="sxs-lookup"><span data-stu-id="b43c9-167">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="b43c9-168">Unterstützte Häufigkeiten</span><span class="sxs-lookup"><span data-stu-id="b43c9-168">Supported frequencies</span></span> 

- <span data-ttu-id="b43c9-169">Wöchentlich</span><span class="sxs-lookup"><span data-stu-id="b43c9-169">Weekly</span></span>
- <span data-ttu-id="b43c9-170">14-tägig</span><span class="sxs-lookup"><span data-stu-id="b43c9-170">Bi-weekly</span></span>
- <span data-ttu-id="b43c9-171">Halbmonatlich</span><span class="sxs-lookup"><span data-stu-id="b43c9-171">Semi-monthly</span></span>
- <span data-ttu-id="b43c9-172">Monatlich</span><span class="sxs-lookup"><span data-stu-id="b43c9-172">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="b43c9-173">Unterstützte Basen</span><span class="sxs-lookup"><span data-stu-id="b43c9-173">Supported bases</span></span> 

- <span data-ttu-id="b43c9-174">Fester Betrag</span><span class="sxs-lookup"><span data-stu-id="b43c9-174">Fixed amount</span></span>
- <span data-ttu-id="b43c9-175">Prozent des Einkommens</span><span class="sxs-lookup"><span data-stu-id="b43c9-175">Percent of earnings</span></span>
- <span data-ttu-id="b43c9-176">Produktive Stunden</span><span class="sxs-lookup"><span data-stu-id="b43c9-176">Productive hours</span></span>

<span data-ttu-id="b43c9-177">Dayforce erstellt die folgenden Abzüge, basierend auf den Lohnauswirkungen, die im Vorteilsplan definiert sind.</span><span class="sxs-lookup"><span data-stu-id="b43c9-177">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="b43c9-178">Auswahl in Human Resources</span><span class="sxs-lookup"><span data-stu-id="b43c9-178">Selection in Human Resources</span></span>        | <span data-ttu-id="b43c9-179">Ergebnis in Dayforce</span><span class="sxs-lookup"><span data-stu-id="b43c9-179">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="b43c9-180">Nichts</span><span class="sxs-lookup"><span data-stu-id="b43c9-180">None</span></span>                       | <span data-ttu-id="b43c9-181">Es wird kein Abzug erstellt.</span><span class="sxs-lookup"><span data-stu-id="b43c9-181">No deduction is created.</span></span>                      |
| <span data-ttu-id="b43c9-182">Nur Abzug</span><span class="sxs-lookup"><span data-stu-id="b43c9-182">Deduction only</span></span>             | <span data-ttu-id="b43c9-183">Ein Mitarbeiterabzug wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="b43c9-183">An employee deduction is created.</span></span>             |
| <span data-ttu-id="b43c9-184">Nur Beitrag</span><span class="sxs-lookup"><span data-stu-id="b43c9-184">Contribution only</span></span>          | <span data-ttu-id="b43c9-185">Ein Arbeitgeberabzug wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="b43c9-185">An employer deduction is created.</span></span>             |
| <span data-ttu-id="b43c9-186">Abzug und Beitrag</span><span class="sxs-lookup"><span data-stu-id="b43c9-186">Deduction and contribution</span></span> | <span data-ttu-id="b43c9-187">Mitarbeiter- und Arbeitgeberabzüge werden erstellt.</span><span class="sxs-lookup"><span data-stu-id="b43c9-187">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="b43c9-188">Weitere Informationen darüber, wie Sie ein Vorteilsprogramm definieren und verwalten finden Sie in den folgenden Artikeln:</span><span class="sxs-lookup"><span data-stu-id="b43c9-188">For more information about how to define and manage a benefits program, see the following articles:</span></span>

- [<span data-ttu-id="b43c9-189">Mitarbeitervorteilsprogramm anbieten</span><span class="sxs-lookup"><span data-stu-id="b43c9-189">Deliver an employee benefits program</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="b43c9-190">Neue Vergütung erstellen</span><span class="sxs-lookup"><span data-stu-id="b43c9-190">Create a new benefit</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="b43c9-191">Vorteilsberechtigungsregeln und Richtlinien definieren</span><span class="sxs-lookup"><span data-stu-id="b43c9-191">Define benefit eligibility rules and policies</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="b43c9-192">Vorteile von Arbeitskräften registrieren und entfernen</span><span class="sxs-lookup"><span data-stu-id="b43c9-192">Enroll and remove benefits from workers</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="b43c9-193">Vergütung</span><span class="sxs-lookup"><span data-stu-id="b43c9-193">Compensation</span></span> 

<span data-ttu-id="b43c9-194">Die Vergütungsverwaltung dient zum Steuern der Abwicklung des Grundlohns und der Prämien.</span><span class="sxs-lookup"><span data-stu-id="b43c9-194">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="b43c9-195">Sie steuern den festen Grundlohn eines Mitarbeiters und dessen Lohnsteigerungen nach Plänen für feste Vergütung.</span><span class="sxs-lookup"><span data-stu-id="b43c9-195">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="b43c9-196">Die Zahlung leistungsbezogener Prämien, wie Boni, Leistungsprämien, Aktienoptionen und -überlassungen sowie Einmalprämien werden durch Pläne für variable Vergütung gesteuert.</span><span class="sxs-lookup"><span data-stu-id="b43c9-196">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="b43c9-197">Dayforce verwendet Vergütungsinformationen, um einen Stunden- oder Jahressatz für einen Mitarbeiter zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="b43c9-197">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="b43c9-198">Feste Vergütungspläne und Lohnsatzumrechnungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b43c9-198">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="b43c9-199">Mitarbeiter müssen einem festen Vergütungsplan zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="b43c9-199">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="b43c9-200">Weitere Informationen zu Kompensationsplänen finden Sie in den folgenden Artikeln:</span><span class="sxs-lookup"><span data-stu-id="b43c9-200">For more information about compensation plans, see the following articles:</span></span>

- [<span data-ttu-id="b43c9-201">Feste Vergütungspläne erstellen</span><span class="sxs-lookup"><span data-stu-id="b43c9-201">Create fixed compensation plans</span></span>](/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="b43c9-202">Variable Vergütungspläne erstellen</span><span class="sxs-lookup"><span data-stu-id="b43c9-202">Create variable compensation plans</span></span>](/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="b43c9-203">Gehalts-/Vergütungsstruktur und -pläne entwickeln</span><span class="sxs-lookup"><span data-stu-id="b43c9-203">Develop salary/compensation structure and plans</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="b43c9-204">Vergütung verarbeiten</span><span class="sxs-lookup"><span data-stu-id="b43c9-204">Process compensation</span></span>](/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="b43c9-205">Vergütungsprozess definieren und Ergebnisse berechnen</span><span class="sxs-lookup"><span data-stu-id="b43c9-205">Define compensation process and calculate results</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="b43c9-206">Einen Mitarbeiters in einem Plan für eine feste Vergütung registrieren</span><span class="sxs-lookup"><span data-stu-id="b43c9-206">Enroll an employee in a fixed compensation plan</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="b43c9-207">Einen Mitarbeiter in einem Plan für variable Vergütung registrieren</span><span class="sxs-lookup"><span data-stu-id="b43c9-207">Enroll an employee in a variable compensation plan</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="b43c9-208">Stellentyp</span><span class="sxs-lookup"><span data-stu-id="b43c9-208">Jobs</span></span> 

<span data-ttu-id="b43c9-209">Eine Stelle ist eine Sammlung der Aufgaben und Zuständigkeiten, die für eine Person, die eine Tätigkeit ausführt, obligatorisch sind.</span><span class="sxs-lookup"><span data-stu-id="b43c9-209">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="b43c9-210">Weitere Informationen finden Sie in folgenden Artikeln:</span><span class="sxs-lookup"><span data-stu-id="b43c9-210">For more information, see the following articles:</span></span>

- [<span data-ttu-id="b43c9-211">Komponenten einer Stelle einrichten</span><span class="sxs-lookup"><span data-stu-id="b43c9-211">Setting up the components of a job</span></span>](/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="b43c9-212">Neue Stellen definieren</span><span class="sxs-lookup"><span data-stu-id="b43c9-212">Define new jobs</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="b43c9-213">Positionen</span><span class="sxs-lookup"><span data-stu-id="b43c9-213">Positions</span></span>

<span data-ttu-id="b43c9-214">Eine Position ist eine einzelne Instanz eines Einzelvorgangs.</span><span class="sxs-lookup"><span data-stu-id="b43c9-214">A position is an individual instance of a job.</span></span> <span data-ttu-id="b43c9-215">Beispielsweise ist die Position „Verkaufsleiter (Ost)” eine der Positionen, die der Stelle „Verkaufsleiter” zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="b43c9-215">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="b43c9-216">Eine Position ist in einer Abteilung vorhanden.</span><span class="sxs-lookup"><span data-stu-id="b43c9-216">A position exists in a department.</span></span> <span data-ttu-id="b43c9-217">Nur jeweils eine Arbeitskraft kann jeder Position zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="b43c9-217">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="b43c9-218">Bedenken Sie die folgenden Daten und Konfigurationen, wenn Sie Positionen einrichten:</span><span class="sxs-lookup"><span data-stu-id="b43c9-218">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="b43c9-219">Position (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-219">Position (required)</span></span>
- <span data-ttu-id="b43c9-220">Beschreibung (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-220">Description (required)</span></span>
- <span data-ttu-id="b43c9-221">Stelle (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-221">Job (required)</span></span>
- <span data-ttu-id="b43c9-222">Abteilung (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-222">Department (required)</span></span>
- <span data-ttu-id="b43c9-223">Positionstyp (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-223">Position type (required)</span></span>
- <span data-ttu-id="b43c9-224">Vollzeitäquivalent</span><span class="sxs-lookup"><span data-stu-id="b43c9-224">Full-time equivalent</span></span>
- <span data-ttu-id="b43c9-225">Normale Stunden pro Jahr (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-225">Annual regular hours (required)</span></span>
- <span data-ttu-id="b43c9-226">Gezahlt von der juristischen Person (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-226">Paid by legal entity (required)</span></span>
- <span data-ttu-id="b43c9-227">Lohnzyklus (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-227">Pay cycle (required)</span></span>
- <span data-ttu-id="b43c9-228">Standardfinanzdimension – Kostenstelle (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-228">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="b43c9-229">Arbeitskraftzuweisung – Arbeitskraft, Zuweisungsanfang, Zuweisungsende, Ursachencode</span><span class="sxs-lookup"><span data-stu-id="b43c9-229">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="b43c9-230">Wenn mehrere Positionen in derselben Abteilung derselben Stelle zugeordnet sind, werden sie in einer einzelnen Position in Dayforce konsolidiert.</span><span class="sxs-lookup"><span data-stu-id="b43c9-230">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="b43c9-231">Weitere Informationen finden Sie in folgenden Artikeln:</span><span class="sxs-lookup"><span data-stu-id="b43c9-231">For more information, see the following articles:</span></span>

- [<span data-ttu-id="b43c9-232">Belegschaft mittels Abteilungen, Stellen und Positionen verwalten</span><span class="sxs-lookup"><span data-stu-id="b43c9-232">Organize your workforce using departments, jobs, and positions</span></span>](/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="b43c9-233">Positionen einrichten</span><span class="sxs-lookup"><span data-stu-id="b43c9-233">Set up positions</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="b43c9-234">Abteilungen</span><span class="sxs-lookup"><span data-stu-id="b43c9-234">Departments</span></span>

<span data-ttu-id="b43c9-235">Eine Abteilung ist eine Organisationseinheit, die eine Kategorie oder einen funktionalen Bereich einer Organisation darstellt.</span><span class="sxs-lookup"><span data-stu-id="b43c9-235">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="b43c9-236">Eine Abteilung ist für einen bestimmten Bereich der Organisation wie zum Beispiel Verkauf, Buchhaltung oder Personalverwaltung zuständig.</span><span class="sxs-lookup"><span data-stu-id="b43c9-236">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="b43c9-237">Sie können Abteilungen verwenden, um zu Funktionsbereiche zu melden.</span><span class="sxs-lookup"><span data-stu-id="b43c9-237">You can use departments to report on functional areas.</span></span> <span data-ttu-id="b43c9-238">Abteilungen können Gewinn- und Verlustzuständigkeit haben.</span><span class="sxs-lookup"><span data-stu-id="b43c9-238">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="b43c9-239">Weitere Informationen finden Sie in folgenden Artikeln:</span><span class="sxs-lookup"><span data-stu-id="b43c9-239">For more information, see the following articles:</span></span>

- [<span data-ttu-id="b43c9-240">Abteilung erstellen und der Abteilungshierarchie zuordnen</span><span class="sxs-lookup"><span data-stu-id="b43c9-240">Create a department and associate it with the department hierarchy</span></span>](/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="b43c9-241">Neue Abteilungen definieren</span><span class="sxs-lookup"><span data-stu-id="b43c9-241">Define new departments</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="b43c9-242">Lohnzyklen und Lohnperioden</span><span class="sxs-lookup"><span data-stu-id="b43c9-242">Pay cycles and pay periods</span></span>

<span data-ttu-id="b43c9-243">Ein Lohnzyklus bestimmt, wie oft Lohn ausgezahlt wird, sowie die spezifischen Tage, an denen Arbeitskräfte bezahlt werden.</span><span class="sxs-lookup"><span data-stu-id="b43c9-243">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="b43c9-244">Ein Lohnzyklus kann beispielsweise monatlich sein, und Mitarbeiter werden am letzten Tag des Monats bezahlt.</span><span class="sxs-lookup"><span data-stu-id="b43c9-244">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="b43c9-245">Alternativ könnte ein Lohnzyklus wöchentlich sein, und Mitarbeiter werden am Dienstag nach Ende der Lohnperiode bezahlt.</span><span class="sxs-lookup"><span data-stu-id="b43c9-245">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="b43c9-246">Lohnzyklen werden Positionen zugewiesen, um zu steuern, wann Mitarbeiter in diesen Positionen bezahlt werden.</span><span class="sxs-lookup"><span data-stu-id="b43c9-246">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="b43c9-247">Nachdem Sie Lohnzyklen erstellen, können Sie Lohnperioden für jeden Zyklus generieren.</span><span class="sxs-lookup"><span data-stu-id="b43c9-247">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="b43c9-248">Jede Lohnperiode enthält ein Standardzahlungsdatum, das auf den von Ihnen bereitgestellten Informationen basiert.</span><span class="sxs-lookup"><span data-stu-id="b43c9-248">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="b43c9-249">Allerdings können Sie das Standardzahlungsdatum in einer Lohnperiode ändern, um Ausnahmen zuzulassen, wie beispielsweise wenn das Zahlungsdatum auf einen Feiertag fällt.</span><span class="sxs-lookup"><span data-stu-id="b43c9-249">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="b43c9-250">Die folgenden Informationen werden in Dayforce verwendet:</span><span class="sxs-lookup"><span data-stu-id="b43c9-250">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="b43c9-251">Lohnzyklus (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-251">Pay cycle (required)</span></span>
- <span data-ttu-id="b43c9-252">Lohnzyklushäufigkeit (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-252">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="b43c9-253">Periodenstartdatum (erstes erforderliche Lohnperiode)</span><span class="sxs-lookup"><span data-stu-id="b43c9-253">Period start date (first pay period required)</span></span>
- <span data-ttu-id="b43c9-254">Standardzahlungsdatum (erste erforderliche Lohnperiode)</span><span class="sxs-lookup"><span data-stu-id="b43c9-254">Default payment date (first pay period required)</span></span>

<span data-ttu-id="b43c9-255">Diese Informationen werden mit Dayforce als Lohngruppen integriert und sind nach Land oder Region für jeden Lohnzyklus getrennt.</span><span class="sxs-lookup"><span data-stu-id="b43c9-255">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="b43c9-256">Es muss mindestens eine Lohnperiode vor der Integration generiert werden.</span><span class="sxs-lookup"><span data-stu-id="b43c9-256">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="b43c9-257">Dayforce generiert Lohngruppenkalender und Zahlungsdaten basierend auf dem Anfangsdatum der ersten Lohnperiode und dem Standardzahlungsdatums, das in Human Resources eingerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="b43c9-257">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Human Resources.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="b43c9-258">Einkommenscodes</span><span class="sxs-lookup"><span data-stu-id="b43c9-258">Earning codes</span></span>

<span data-ttu-id="b43c9-259">Einkommenscodes bestimmen jeden Typ von Einkünften eindeutig, die Arbeitskräfte erhalten</span><span class="sxs-lookup"><span data-stu-id="b43c9-259">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="b43c9-260">Die Codes haben verschiedene Parameter, die sich auf Einkünfte beziehen, wie beispielsweise Buchhaltungsvorschriften, Steuergesetze, Berichterstellungsanforderungen und Bruttoausgleichsfähigkeit.</span><span class="sxs-lookup"><span data-stu-id="b43c9-260">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="b43c9-261">Die folgenden Informationen werden in Dayforce verwendet:</span><span class="sxs-lookup"><span data-stu-id="b43c9-261">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="b43c9-262">Einkommenscode (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-262">Earning Code (required)</span></span>
- <span data-ttu-id="b43c9-263">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b43c9-263">Description</span></span>
- <span data-ttu-id="b43c9-264">Maßeinheit</span><span class="sxs-lookup"><span data-stu-id="b43c9-264">Unit of measure</span></span>
- <span data-ttu-id="b43c9-265">Produktiv</span><span class="sxs-lookup"><span data-stu-id="b43c9-265">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="b43c9-266">Arbeitskraftdaten</span><span class="sxs-lookup"><span data-stu-id="b43c9-266">Worker data</span></span>

<span data-ttu-id="b43c9-267">Datensätze für die verschiedenen Arten von Arbeitskräften, die Sie haben, sind für Ihre Personalverwaltung- sowie für Ihre Lohnsysteme von Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="b43c9-267">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="b43c9-268">Anhand der eingegebenen Informationen lassen sich Arbeitskräfte sowie personenbezogene Informationen nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="b43c9-268">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="b43c9-269">Sie können die folgenden Informationen für Arbeitskräfte verwalten:</span><span class="sxs-lookup"><span data-stu-id="b43c9-269">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="b43c9-270">**Basis** – Verwalten grundlegender Informationen über eine Arbeitskraft, beispielsweise Kontaktinformationen, demografische Informationen, Kennungsinformationen, Familieninformationen, Militärdienststatus, Ausländerinformationen sowie personenbezogene und Notfallkontakte.</span><span class="sxs-lookup"><span data-stu-id="b43c9-270">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="b43c9-271">**Beschäftigung** – Verwalten von Informationen zum Beschäftigungsverhältnis einer Arbeitskraft, wie Unternehmens- oder Organisationszugehörigkeit, Positionszuweisung, Start- und Enddatum, Arbeitsberechtigung, Beschäftigungsbedingungen, Rente, Urlaub und Versetzungen.</span><span class="sxs-lookup"><span data-stu-id="b43c9-271">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="b43c9-272">**Urlaub und Abwesenheit** – Verwalten von Informationen zur Abwesenheit einer Arbeitskraft, beispielsweise Arbeitszeitkalender, Abwesenheitsbuchungen und Abwesenheitseinrichtung.</span><span class="sxs-lookup"><span data-stu-id="b43c9-272">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="b43c9-273">**Vergütung und Lohn** – Verwalten von Informationen zu den Vergütungsplänen und Lohndaten einer Arbeitskraft, wie der Planregistrierung, Boni, Leistung, Provision, Steuerdaten, Pensionierung und Gehaltsabzüge.</span><span class="sxs-lookup"><span data-stu-id="b43c9-273">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="b43c9-274">Wenn Sie Arbeitskraftinformationen eingeben, sollten Sie folgende Daten und Konfigurationen bedenken, die in Dayforce verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b43c9-274">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="b43c9-275">Allgemeine Angaben</span><span class="sxs-lookup"><span data-stu-id="b43c9-275">General information</span></span>

- <span data-ttu-id="b43c9-276">Personalnummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-276">Personnel number (required)</span></span>
- <span data-ttu-id="b43c9-277">Vorname (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-277">First name (required)</span></span>
- <span data-ttu-id="b43c9-278">Nachname (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-278">Last name (required)</span></span>
- <span data-ttu-id="b43c9-279">Zweiter Vorname</span><span class="sxs-lookup"><span data-stu-id="b43c9-279">Middle name</span></span>
- <span data-ttu-id="b43c9-280">Dienstalterdatum</span><span class="sxs-lookup"><span data-stu-id="b43c9-280">Seniority date</span></span>
- <span data-ttu-id="b43c9-281">Bekannt als</span><span class="sxs-lookup"><span data-stu-id="b43c9-281">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="b43c9-282">Personenbezogene Informationen</span><span class="sxs-lookup"><span data-stu-id="b43c9-282">Personal information</span></span>

- <span data-ttu-id="b43c9-283">Familienstand (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-283">Marital status (required)</span></span>
- <span data-ttu-id="b43c9-284">Geburtsdatum (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-284">Birth date (required)</span></span>
- <span data-ttu-id="b43c9-285">Geschlecht (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-285">Gender (required)</span></span>
- <span data-ttu-id="b43c9-286">Person mit Behinderung</span><span class="sxs-lookup"><span data-stu-id="b43c9-286">Person with disabilities</span></span>
- <span data-ttu-id="b43c9-287">Nationalitätsland/-region (nur für Mexiko)</span><span class="sxs-lookup"><span data-stu-id="b43c9-287">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="b43c9-288">Adressdaten</span><span class="sxs-lookup"><span data-stu-id="b43c9-288">Address information</span></span>

- <span data-ttu-id="b43c9-289">Primär (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-289">Primary (required)</span></span>
- <span data-ttu-id="b43c9-290">Land/Region (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-290">Country/region (required)</span></span>
- <span data-ttu-id="b43c9-291">Postleitzahl (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-291">Postal code (required)</span></span>
- <span data-ttu-id="b43c9-292">Hausnummer (erforderlich) (nur für Mexiko)</span><span class="sxs-lookup"><span data-stu-id="b43c9-292">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="b43c9-293">Gebäudeergänzung (nur für Mexiko)</span><span class="sxs-lookup"><span data-stu-id="b43c9-293">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="b43c9-294">Ort (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-294">City (required)</span></span>
- <span data-ttu-id="b43c9-295">Bundesland/Kanton (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-295">State (required)</span></span>
- <span data-ttu-id="b43c9-296">Landkreis (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-296">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="b43c9-297">Kontaktdaten</span><span class="sxs-lookup"><span data-stu-id="b43c9-297">Contact information</span></span> 

- <span data-ttu-id="b43c9-298">Primär (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-298">Primary (required)</span></span>
- <span data-ttu-id="b43c9-299">Kontaktnummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-299">Contact number (required)</span></span>
- <span data-ttu-id="b43c9-300">Durchwahl</span><span class="sxs-lookup"><span data-stu-id="b43c9-300">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="b43c9-301">Lohndaten und Einkommenscodes</span><span class="sxs-lookup"><span data-stu-id="b43c9-301">Payroll information and earning codes</span></span>

<span data-ttu-id="b43c9-302">Mitarbeitern müssen bestimmte Einkommen mit einer bestimmten Zahlungshäufigkeit zugewiesen werden und sie müssen eine bevorzugte Zahlungsmethode haben.</span><span class="sxs-lookup"><span data-stu-id="b43c9-302">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="b43c9-303">Die folgenden Felder werden in Dayforce verwendet, um zu gewährleisten, dass diese Voreinstellungen und Einstellungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b43c9-303">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="b43c9-304">Einkommenscodes</span><span class="sxs-lookup"><span data-stu-id="b43c9-304">Earning codes</span></span>

- <span data-ttu-id="b43c9-305">Position (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-305">Position (required)</span></span>
- <span data-ttu-id="b43c9-306">Einkommenscode (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-306">Earning Code (required)</span></span>
- <span data-ttu-id="b43c9-307">Häufigkeit (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-307">Frequency (required)</span></span>
- <span data-ttu-id="b43c9-308">Betrag (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-308">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="b43c9-309">Lohndaten</span><span class="sxs-lookup"><span data-stu-id="b43c9-309">Payroll information</span></span>

- <span data-ttu-id="b43c9-310">Zahlungsmethode</span><span class="sxs-lookup"><span data-stu-id="b43c9-310">Payment Method</span></span>
- <span data-ttu-id="b43c9-311">Wirtschaftliche Region (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-311">Economic Region (required)</span></span>
- <span data-ttu-id="b43c9-312">Mitarbeitervergütungs-ID</span><span class="sxs-lookup"><span data-stu-id="b43c9-312">Employee Benefits ID</span></span>
- <span data-ttu-id="b43c9-313">Personalausweisnummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-313">National ID Number (required)</span></span>
- <span data-ttu-id="b43c9-314">Militärdienstnummer</span><span class="sxs-lookup"><span data-stu-id="b43c9-314">Military Service Number</span></span>
- <span data-ttu-id="b43c9-315">Schichtkennung (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-315">Shift ID (required)</span></span>
- <span data-ttu-id="b43c9-316">Steuernummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-316">Tax Number (required)</span></span>
- <span data-ttu-id="b43c9-317">Gewerkschaftskennung (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-317">Union ID (required)</span></span>
- <span data-ttu-id="b43c9-318">Arbeitstagkennung (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-318">Work Day ID (required)</span></span>
- <span data-ttu-id="b43c9-319">Arbeitserlaubnisnummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-319">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="b43c9-320">Für die Zahlungsmethode unterstützt Mexiko **Bargeld**, **Scheck** (der physische Scheck des Unternehmens) und **Elektronische Zahlung**.</span><span class="sxs-lookup"><span data-stu-id="b43c9-320">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="b43c9-321">Wenn keine Zahlungsmethode angegeben wird, wird **Scheck** standardmäßig verwendet.</span><span class="sxs-lookup"><span data-stu-id="b43c9-321">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="b43c9-322">Anstellungsdetails</span><span class="sxs-lookup"><span data-stu-id="b43c9-322">Employment details</span></span>

<span data-ttu-id="b43c9-323">Beschäftigungsdetailhistorie wird als Schlüsselinformation verwendet, um die Status für Einstellung, Kündigung und erneute Einstellung in Dayforce abzuleiten.</span><span class="sxs-lookup"><span data-stu-id="b43c9-323">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="b43c9-324">Dayforce unterstützt nur einen aktiven Beschäftigungsdatensatz gleichzeitig.</span><span class="sxs-lookup"><span data-stu-id="b43c9-324">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="b43c9-325">Datum des Beschäftigungsbeginns (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-325">Employment start date (required)</span></span>
- <span data-ttu-id="b43c9-326">Datum des Beschäftigungsendes</span><span class="sxs-lookup"><span data-stu-id="b43c9-326">Employment end date</span></span>
- <span data-ttu-id="b43c9-327">Eintrittstermin</span><span class="sxs-lookup"><span data-stu-id="b43c9-327">Start date</span></span>
- <span data-ttu-id="b43c9-328">Angepasster Tätigkeitsbeginn</span><span class="sxs-lookup"><span data-stu-id="b43c9-328">Adjusted start date</span></span>
- <span data-ttu-id="b43c9-329">Kündigungsdatum (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-329">Termination date (required upon termination)</span></span>
- <span data-ttu-id="b43c9-330">Kündigungsgrund (erforderlich bei Kündigung)</span><span class="sxs-lookup"><span data-stu-id="b43c9-330">Termination reason (required upon termination)</span></span>

<span data-ttu-id="b43c9-331">Die Schlüsseldaten eines Mitarbeiters werden abgeleitet, indem die folgenden Informationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b43c9-331">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="b43c9-332">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="b43c9-332">Human Resources</span></span>                | <span data-ttu-id="b43c9-333">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b43c9-333">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b43c9-334">Aktuellstes Einstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="b43c9-334">Most recent hire date</span></span> | <span data-ttu-id="b43c9-335">Beschäftigungsbeginn des Verlaufsdatensatzes zur aktuellen, nicht gekündigten Beschäftigung</span><span class="sxs-lookup"><span data-stu-id="b43c9-335">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="b43c9-336">Kündigungsdatum</span><span class="sxs-lookup"><span data-stu-id="b43c9-336">Termination date</span></span>      | <span data-ttu-id="b43c9-337">Kündigungsdatum des Verlaufsdatensatzes zur aktuellen, nicht gekündigten Beschäftigung</span><span class="sxs-lookup"><span data-stu-id="b43c9-337">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="b43c9-338">Eintrittstermin</span><span class="sxs-lookup"><span data-stu-id="b43c9-338">Start date</span></span>            | <span data-ttu-id="b43c9-339">Angepasstes Startdatum, Startdatum oder Beschäftigungsbeginn des Verlaufsdatensatzes zur aktuellen, nicht aktiven Beschäftigung</span><span class="sxs-lookup"><span data-stu-id="b43c9-339">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="b43c9-340">Ursprüngliches Einstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="b43c9-340">Original hire date</span></span>    | <span data-ttu-id="b43c9-341">Beschäftigungsbeginn des frühesten Beschäftigungsverlaufsdatensatzes</span><span class="sxs-lookup"><span data-stu-id="b43c9-341">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="b43c9-342">Vergütung</span><span class="sxs-lookup"><span data-stu-id="b43c9-342">Compensation</span></span>

<span data-ttu-id="b43c9-343">Ein fester Vergütungsplan muss der primären Position jedes Mitarbeiters während einer Beschäftigungsperiode zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="b43c9-343">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="b43c9-344">Diese Periode beginnt mit dem Datum, an dem der Mitarbeiter eingestellt wurde (oder dem Datum des Beschäftigungsbeginns), und setzt sich bis zur Kündigung fort.</span><span class="sxs-lookup"><span data-stu-id="b43c9-344">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="b43c9-345">Gültigkeitsdatum (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-345">Effective Date (required)</span></span>
- <span data-ttu-id="b43c9-346">Ablaufdatum</span><span class="sxs-lookup"><span data-stu-id="b43c9-346">Expiration date</span></span>
- <span data-ttu-id="b43c9-347">Lohnsatz (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-347">Pay Rate (required)</span></span>
- <span data-ttu-id="b43c9-348">Lohnsatzkonvertierungen (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-348">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="b43c9-349">Jährliches Äquivalent (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-349">Annual equivalent (required)</span></span>
- <span data-ttu-id="b43c9-350">Stündliches Äquivalent (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-350">Hourly equivalent (required)</span></span>

<span data-ttu-id="b43c9-351">Wenn ein Mitarbeiter auf Stundenbasis mehrere Positionen hat, wird die feste Vergütung der primären Position in Dayforce als Basissatz/-gehalt auf Mitarbeiterebene importiert.</span><span class="sxs-lookup"><span data-stu-id="b43c9-351">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="b43c9-352">Für nicht-primäre Positionen wird der Stundensatz in der entsprechenden Position in Dayforce gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b43c9-352">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="b43c9-353">Wenn ein Gehalt beziehender Mitarbeiter mehrere Positionen hat, wird der kumulative Stundensatz und das Jahresgehalt über alle aktiven Positionen hinweg abgeleitet und als Basissatz/-gehalt auf Arbeitnehmerebene verwendet.</span><span class="sxs-lookup"><span data-stu-id="b43c9-353">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="b43c9-354">Kennnummern</span><span class="sxs-lookup"><span data-stu-id="b43c9-354">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="b43c9-355">Sozialversicherungsbezeichner</span><span class="sxs-lookup"><span data-stu-id="b43c9-355">Social Security identifier</span></span> 

<span data-ttu-id="b43c9-356">Jeder Mitarbeiter muss einen primären Bezeichner haben.</span><span class="sxs-lookup"><span data-stu-id="b43c9-356">Every employee must have one primary identifier.</span></span> <span data-ttu-id="b43c9-357">Dieser Bezeichner muss vom Kennungstyp **P.Reg.Nr.** sein.</span><span class="sxs-lookup"><span data-stu-id="b43c9-357">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="b43c9-358">In Dayforce wird er automatisch als Sozialversicherungsbezeichner des Mitarbeiters abgeleitet, der für die Einstellung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="b43c9-358">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="b43c9-359">Primär (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-359">Primary (required)</span></span>
- <span data-ttu-id="b43c9-360">Kennungstyp = „P.Reg.Nr.”</span><span class="sxs-lookup"><span data-stu-id="b43c9-360">Identification Type = "SSN"</span></span>
- <span data-ttu-id="b43c9-361">Ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="b43c9-361">Issued Date</span></span>
- <span data-ttu-id="b43c9-362">Ablaufdatum</span><span class="sxs-lookup"><span data-stu-id="b43c9-362">Expiration Date</span></span>

<span data-ttu-id="b43c9-363">Mitarbeiter können mehrere Kennungsnummern des Kennungstyps **P.Reg.Nr.** melden.</span><span class="sxs-lookup"><span data-stu-id="b43c9-363">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="b43c9-364">Jedoch wird nur der Datensatz, der als **Primär** markiert ist, in Dayforce integriert, unabhängig davon, ob die Nummer aktiv oder abgelaufen ist.</span><span class="sxs-lookup"><span data-stu-id="b43c9-364">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="b43c9-365">Bankkonten und Auszahlungen</span><span class="sxs-lookup"><span data-stu-id="b43c9-365">Bank accounts and disbursements</span></span>

<span data-ttu-id="b43c9-366">Gültige Bankkontoinformationen müssen für jeden Mitarbeiter eingegeben werden, der per Bankkontoüberweisungen bezahlt werden möchte.</span><span class="sxs-lookup"><span data-stu-id="b43c9-366">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="b43c9-367">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="b43c9-367">Human Resources</span></span>                         | <span data-ttu-id="b43c9-368">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b43c9-368">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b43c9-369">Bankkontonummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-369">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="b43c9-370">SWIFT-Code (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-370">SWIFT code (required)</span></span>          | <span data-ttu-id="b43c9-371">Feld **Bankkennung** wird verwendet, wenn Lohn in Mexiko verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="b43c9-371">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="b43c9-372">Filialnummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-372">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="b43c9-373">Bankkontotyp (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-373">Bank account type (required)</span></span>   | <span data-ttu-id="b43c9-374">Feld **Kontotyp** wird verwendet, wenn Lohn in Mexiko verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="b43c9-374">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="b43c9-375">Unterstützte Werte umfassen **Wird geprüft** und **Lohn**.</span><span class="sxs-lookup"><span data-stu-id="b43c9-375">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="b43c9-376">Mitarbeiter, die per Bankkontoüberweisungen bezahlt werden möchten, müssen eine Verknüpfung zu einem Restbetrags-Bankkonto angeben, das sich unter einer juristischen Person befindet, deren primäre Adresse in Mexiko ist und das einem gültigen Bankkonto von einer mexikanischen Bank zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b43c9-376">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="b43c9-377">Alle anderen Nicht-Restbetrags-Bankkonten werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="b43c9-377">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="b43c9-378">Adressdaten</span><span class="sxs-lookup"><span data-stu-id="b43c9-378">Address information</span></span>

<span data-ttu-id="b43c9-379">Jeder Mitarbeiter muss einen primären Standort haben.</span><span class="sxs-lookup"><span data-stu-id="b43c9-379">Every employee must have one primary location.</span></span> <span data-ttu-id="b43c9-380">In Dayforce wird dieser Standort verwendet, um den primären Wohnsitz des Mitarbeiters für Steuerzwecke zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="b43c9-380">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="b43c9-381">Primär (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-381">Primary (required)</span></span>
- <span data-ttu-id="b43c9-382">Land/Region (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-382">Country/region (required)</span></span>
- <span data-ttu-id="b43c9-383">Postleitzahl (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-383">Zip/postal code (required)</span></span>
- <span data-ttu-id="b43c9-384">Straße (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-384">Street (required)</span></span>
- <span data-ttu-id="b43c9-385">Hausnummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-385">Street Number (required)</span></span>
- <span data-ttu-id="b43c9-386">Gebäudeergänzung</span><span class="sxs-lookup"><span data-stu-id="b43c9-386">Building Complement</span></span>
- <span data-ttu-id="b43c9-387">Ort (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-387">City (required)</span></span>
- <span data-ttu-id="b43c9-388">Bundesland/Kanton (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-388">State (required)</span></span>
- <span data-ttu-id="b43c9-389">Landkreis (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-389">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="b43c9-390">Konfigurieren Ihrer Daten, um Vergütung in den USA und Kanada zu generieren</span><span class="sxs-lookup"><span data-stu-id="b43c9-390">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="b43c9-391">Wenn Sie Vergütung für Mitarbeiter in den USA und Kanada generieren, müssen die folgenden Elemente konfiguriert werden:</span><span class="sxs-lookup"><span data-stu-id="b43c9-391">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="b43c9-392">Abteilungen sind für Positionen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b43c9-392">Departments are required on positions.</span></span>
- <span data-ttu-id="b43c9-393">Kostenstellen müssen als Finanzdimensionen festgelegt werden und müssen das erste Element in der standardmäßigen Finanzdimensions-Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="b43c9-393">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="b43c9-394">Sie können Human Resources so konfigurieren, dass Positionen eine Abteilung angeben müssen.</span><span class="sxs-lookup"><span data-stu-id="b43c9-394">You can configure Human Resources to require that Positions specify a Department.</span></span> <span data-ttu-id="b43c9-395">Dazu wechseln Sie zu **Freigegebene Positionen der Personalverwaltung > Positionen > Abteilungen zu Positionen anfordern**.</span><span class="sxs-lookup"><span data-stu-id="b43c9-395">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="b43c9-396">Es wird empfohlen, dass diese Einstellungen für die Integration erzwungen wird.</span><span class="sxs-lookup"><span data-stu-id="b43c9-396">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="b43c9-397">Stellentypen</span><span class="sxs-lookup"><span data-stu-id="b43c9-397">Job types</span></span>

<span data-ttu-id="b43c9-398">Stellentypen werden verwendet, um ähnliche Stellen in Kategorien zu gruppieren.</span><span class="sxs-lookup"><span data-stu-id="b43c9-398">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="b43c9-399">Stellentypen sind erforderlich, damit Lohn in den USA und Kanada zu bearbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="b43c9-399">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="b43c9-400">Beispiele für Stellentypen umfassen Voll- und Teilzeit oder festes Gehalt und Stundenlohn.</span><span class="sxs-lookup"><span data-stu-id="b43c9-400">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="b43c9-401">Stellentypen werden Dayforce als Lohnarten zugeordnet, die angeben, ob ein Mitarbeiter auf Stundenbasis bezahlt wird oder ein festes Gehalt bezieht.</span><span class="sxs-lookup"><span data-stu-id="b43c9-401">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="b43c9-402">Folgende Stellentypen und Beschreibungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b43c9-402">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="b43c9-403">Stellentyp</span><span class="sxs-lookup"><span data-stu-id="b43c9-403">Job type</span></span>   | <span data-ttu-id="b43c9-404">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b43c9-404">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="b43c9-405">Stündlich</span><span class="sxs-lookup"><span data-stu-id="b43c9-405">Hourly</span></span>     | <span data-ttu-id="b43c9-406">Stündlich</span><span class="sxs-lookup"><span data-stu-id="b43c9-406">Hourly</span></span>      |
| <span data-ttu-id="b43c9-407">Fest angestellt</span><span class="sxs-lookup"><span data-stu-id="b43c9-407">Salaried</span></span>   | <span data-ttu-id="b43c9-408">Fest angestellt</span><span class="sxs-lookup"><span data-stu-id="b43c9-408">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="b43c9-409">Positionstypen</span><span class="sxs-lookup"><span data-stu-id="b43c9-409">Position types</span></span> 

<span data-ttu-id="b43c9-410">Sie verwenden Positionstypen, um zu beschreiben, ob die Position Vollzeit, Teilzeit oder etwas anderes ist.</span><span class="sxs-lookup"><span data-stu-id="b43c9-410">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="b43c9-411">Positionstypen werden Dayforce als Lohnklassen zugeordnet, die angeben, ob ein Mitarbeiter in Vollzeit oder Teilzeit arbeitet.</span><span class="sxs-lookup"><span data-stu-id="b43c9-411">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="b43c9-412">Folgende Positionstypen und Beschreibungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b43c9-412">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="b43c9-413">Positionstyp</span><span class="sxs-lookup"><span data-stu-id="b43c9-413">Position type</span></span>   | <span data-ttu-id="b43c9-414">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b43c9-414">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="b43c9-415">Vollzeit</span><span class="sxs-lookup"><span data-stu-id="b43c9-415">Full-time</span></span>       | <span data-ttu-id="b43c9-416">Vollzeitmitarbeiter</span><span class="sxs-lookup"><span data-stu-id="b43c9-416">Full time employee</span></span> |
| <span data-ttu-id="b43c9-417">Teilzeit</span><span class="sxs-lookup"><span data-stu-id="b43c9-417">Part-time</span></span>       | <span data-ttu-id="b43c9-418">Teilzeitmitarbeiter</span><span class="sxs-lookup"><span data-stu-id="b43c9-418">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="b43c9-419">Ursachencodes</span><span class="sxs-lookup"><span data-stu-id="b43c9-419">Reason codes</span></span>

<span data-ttu-id="b43c9-420">Ursachencodes enthalten Informationen zum Status eines Mitarbeiters.</span><span class="sxs-lookup"><span data-stu-id="b43c9-420">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="b43c9-421">Ursachencodes werden Dayforce als Statusgründe zugeordnet, die den Grund für Änderungen bei der Position eines Mitarbeiters oder dem Beschäftigungsstatus angeben.</span><span class="sxs-lookup"><span data-stu-id="b43c9-421">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="b43c9-422">Folgende Ursachencodes und Beschreibungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b43c9-422">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="b43c9-423">Ursachencode</span><span class="sxs-lookup"><span data-stu-id="b43c9-423">Reason code</span></span>    | <span data-ttu-id="b43c9-424">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b43c9-424">Description</span></span>      | <span data-ttu-id="b43c9-425">Zutreffende Szenarios</span><span class="sxs-lookup"><span data-stu-id="b43c9-425">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="b43c9-426">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="b43c9-426">RESIGNATION</span></span>    | <span data-ttu-id="b43c9-427">Kündigung durch Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="b43c9-427">Resignation</span></span>      | <span data-ttu-id="b43c9-428">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="b43c9-428">Terminate worker</span></span>     |
| <span data-ttu-id="b43c9-429">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="b43c9-429">TERMINATION</span></span>    | <span data-ttu-id="b43c9-430">Beendigung</span><span class="sxs-lookup"><span data-stu-id="b43c9-430">Termination</span></span>      | <span data-ttu-id="b43c9-431">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="b43c9-431">Terminate worker</span></span>     |
| <span data-ttu-id="b43c9-432">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="b43c9-432">RETIREMENT</span></span>     | <span data-ttu-id="b43c9-433">Ruhestand</span><span class="sxs-lookup"><span data-stu-id="b43c9-433">Retirement</span></span>       | <span data-ttu-id="b43c9-434">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="b43c9-434">Terminate worker</span></span>     |
| <span data-ttu-id="b43c9-435">OTHER</span><span class="sxs-lookup"><span data-stu-id="b43c9-435">OTHER</span></span>          | <span data-ttu-id="b43c9-436">Andere Gründe</span><span class="sxs-lookup"><span data-stu-id="b43c9-436">Other Reasons</span></span>    | <span data-ttu-id="b43c9-437">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="b43c9-437">Terminate worker</span></span>     |
| <span data-ttu-id="b43c9-438">DEATH</span><span class="sxs-lookup"><span data-stu-id="b43c9-438">DEATH</span></span>          | <span data-ttu-id="b43c9-439">Tod</span><span class="sxs-lookup"><span data-stu-id="b43c9-439">Death</span></span>            | <span data-ttu-id="b43c9-440">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="b43c9-440">Terminate worker</span></span>     |
| <span data-ttu-id="b43c9-441">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="b43c9-441">LEAVEOFABSENCE</span></span> | <span data-ttu-id="b43c9-442">Beurlaubung</span><span class="sxs-lookup"><span data-stu-id="b43c9-442">Leave of Absence</span></span> | <span data-ttu-id="b43c9-443">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="b43c9-443">Terminate worker</span></span>     |
| <span data-ttu-id="b43c9-444">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="b43c9-444">CONTRACTEND</span></span>    | <span data-ttu-id="b43c9-445">Vertragsende</span><span class="sxs-lookup"><span data-stu-id="b43c9-445">End of Contract</span></span>  | <span data-ttu-id="b43c9-446">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="b43c9-446">Terminate worker</span></span>     |
| <span data-ttu-id="b43c9-447">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="b43c9-447">SALARYCHANGE</span></span>   | <span data-ttu-id="b43c9-448">Gehaltsänderung</span><span class="sxs-lookup"><span data-stu-id="b43c9-448">Change of Salary</span></span> | <span data-ttu-id="b43c9-449">Vergütung</span><span class="sxs-lookup"><span data-stu-id="b43c9-449">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="b43c9-450">Familienstand</span><span class="sxs-lookup"><span data-stu-id="b43c9-450">Marital status</span></span>

<span data-ttu-id="b43c9-451">Familienstandwerte werden Dayforce zugeordnet und werden – je nach Bedarf – in die akzeptierten Werte bei der Integration übersetzt.</span><span class="sxs-lookup"><span data-stu-id="b43c9-451">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="b43c9-452">Die folgende Tabelle zeigt, wie Familienstandwerte Dayforce zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="b43c9-452">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="b43c9-453">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="b43c9-453">Human Resources</span></span>                 | <span data-ttu-id="b43c9-454">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b43c9-454">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="b43c9-455">Verheiratet</span><span class="sxs-lookup"><span data-stu-id="b43c9-455">Married</span></span>                | <span data-ttu-id="b43c9-456">Verheiratet</span><span class="sxs-lookup"><span data-stu-id="b43c9-456">Married</span></span>              |
| <span data-ttu-id="b43c9-457">Ledig</span><span class="sxs-lookup"><span data-stu-id="b43c9-457">Single</span></span>                 | <span data-ttu-id="b43c9-458">Ledig</span><span class="sxs-lookup"><span data-stu-id="b43c9-458">Single</span></span>               |
| <span data-ttu-id="b43c9-459">Verwitwet</span><span class="sxs-lookup"><span data-stu-id="b43c9-459">Widowed</span></span>                | <span data-ttu-id="b43c9-460">Verwitwet</span><span class="sxs-lookup"><span data-stu-id="b43c9-460">Widowed</span></span>              |
| <span data-ttu-id="b43c9-461">Geschieden</span><span class="sxs-lookup"><span data-stu-id="b43c9-461">Divorced</span></span>               | <span data-ttu-id="b43c9-462">Geschieden</span><span class="sxs-lookup"><span data-stu-id="b43c9-462">Divorced</span></span>             |
| <span data-ttu-id="b43c9-463">Eingetragene Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="b43c9-463">Registered Partnership</span></span> | <span data-ttu-id="b43c9-464">Inländische Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="b43c9-464">Domestic Partnership</span></span> |
| <span data-ttu-id="b43c9-465">None</span><span class="sxs-lookup"><span data-stu-id="b43c9-465">None</span></span>                   | <span data-ttu-id="b43c9-466">None</span><span class="sxs-lookup"><span data-stu-id="b43c9-466">None</span></span>                 |
| <span data-ttu-id="b43c9-467">Freie Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="b43c9-467">Cohabiting</span></span>             | <span data-ttu-id="b43c9-468">Freie Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="b43c9-468">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="b43c9-469">Geschlecht</span><span class="sxs-lookup"><span data-stu-id="b43c9-469">Gender</span></span>

<span data-ttu-id="b43c9-470">Geschlechtsbezeichnungen werden Dayforce zugeordnet und werden – je nach Bedarf – in die akzeptierten Werte bei der Integration übersetzt.</span><span class="sxs-lookup"><span data-stu-id="b43c9-470">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="b43c9-471">Die folgende Tabelle zeigt, wie Geschlechtsbezeichnungen Dayforce zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="b43c9-471">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="b43c9-472">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="b43c9-472">Human Resources</span></span>       | <span data-ttu-id="b43c9-473">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b43c9-473">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="b43c9-474">Männl.</span><span class="sxs-lookup"><span data-stu-id="b43c9-474">Male</span></span>         | <span data-ttu-id="b43c9-475">Männl.</span><span class="sxs-lookup"><span data-stu-id="b43c9-475">Male</span></span>            |
| <span data-ttu-id="b43c9-476">Weibl.</span><span class="sxs-lookup"><span data-stu-id="b43c9-476">Female</span></span>       | <span data-ttu-id="b43c9-477">Weibl.</span><span class="sxs-lookup"><span data-stu-id="b43c9-477">Female</span></span>          |
| <span data-ttu-id="b43c9-478">Nicht spezifisch</span><span class="sxs-lookup"><span data-stu-id="b43c9-478">Non-specific</span></span> | <span data-ttu-id="b43c9-479">*Nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="b43c9-479">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="b43c9-480">Einkommenscodes</span><span class="sxs-lookup"><span data-stu-id="b43c9-480">Earning codes</span></span>

<span data-ttu-id="b43c9-481">Einkommenscodes bestimmen jeden Typ von Einkünften eindeutig, die Arbeitskräfte erhalten</span><span class="sxs-lookup"><span data-stu-id="b43c9-481">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="b43c9-482">Die Codes decken verschiedene Parameter ab, die sich auf Einkünfte beziehen, wie beispielsweise Buchhaltungsvorschriften, Steuergesetze, Berichterstellungsanforderungen und Bruttoausgleichsfähigkeit.</span><span class="sxs-lookup"><span data-stu-id="b43c9-482">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="b43c9-483">Wenn eine nicht unterstützte Häufigkeit verwendet wird, wird die Häufigkeit **Jeder Lohn** standardmäßig für die Berechnung verwendet.</span><span class="sxs-lookup"><span data-stu-id="b43c9-483">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="b43c9-484">Unterstützte Häufigkeiten</span><span class="sxs-lookup"><span data-stu-id="b43c9-484">Supported frequencies</span></span>

- <span data-ttu-id="b43c9-485">Alle</span><span class="sxs-lookup"><span data-stu-id="b43c9-485">All</span></span>
- <span data-ttu-id="b43c9-486">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="b43c9-486">EVERYPAY</span></span>
- <span data-ttu-id="b43c9-487">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="b43c9-487">EACHPAYPERIOD</span></span>
- <span data-ttu-id="b43c9-488">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="b43c9-488">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="b43c9-489">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="b43c9-489">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="b43c9-490">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="b43c9-490">1OFMTH</span></span>
- <span data-ttu-id="b43c9-491">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="b43c9-491">LASTOFMTH</span></span>
- <span data-ttu-id="b43c9-492">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="b43c9-492">2OFMTH</span></span>
- <span data-ttu-id="b43c9-493">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="b43c9-493">3OFMTH</span></span>
- <span data-ttu-id="b43c9-494">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b43c9-494">4OFMTH</span></span>
- <span data-ttu-id="b43c9-495">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="b43c9-495">5OFMTH</span></span>
- <span data-ttu-id="b43c9-496">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="b43c9-496">1N2OFMTH</span></span>
- <span data-ttu-id="b43c9-497">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b43c9-497">3N4OFMTH</span></span>
- <span data-ttu-id="b43c9-498">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="b43c9-498">1N3OFMTH</span></span>
- <span data-ttu-id="b43c9-499">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b43c9-499">1N4OFMTH</span></span>
- <span data-ttu-id="b43c9-500">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="b43c9-500">2N3OFMTH</span></span>
- <span data-ttu-id="b43c9-501">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b43c9-501">2N4OFMTH</span></span>
- <span data-ttu-id="b43c9-502">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="b43c9-502">1N2N3OFMTH</span></span>
- <span data-ttu-id="b43c9-503">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b43c9-503">1N2N4OFMTH</span></span>
- <span data-ttu-id="b43c9-504">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b43c9-504">1N3N4OFMTH</span></span>
- <span data-ttu-id="b43c9-505">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b43c9-505">2N3N4OFMTH</span></span>
- <span data-ttu-id="b43c9-506">1N2N3N4OFMTH – 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b43c9-506">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="b43c9-507">2N3N4N5OFMth – 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="b43c9-507">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="b43c9-508">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="b43c9-508">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="b43c9-509">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="b43c9-509">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="b43c9-510">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="b43c9-510">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="b43c9-511">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="b43c9-511">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="b43c9-512">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="b43c9-512">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="b43c9-513">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="b43c9-513">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="b43c9-514">Adressen</span><span class="sxs-lookup"><span data-stu-id="b43c9-514">Addresses</span></span>

<span data-ttu-id="b43c9-515">Die Kennung bestimmter Codes für Land oder Region, Bundesland/Kanton oder Landkreis (Gemeinde) erfordert spezifische Formate, die Dayforce und Anbieter innerhalb des Landes/innerhalb der Region erkennen können.</span><span class="sxs-lookup"><span data-stu-id="b43c9-515">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="b43c9-516">Obwohl das Format für Orte flexibel ist, muss jeder Ort einem Bundesland zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="b43c9-516">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="b43c9-517">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="b43c9-517">Human Resources</span></span>          | <span data-ttu-id="b43c9-518">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b43c9-518">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="b43c9-519">Land/Region</span><span class="sxs-lookup"><span data-stu-id="b43c9-519">Country/Region</span></span>  | <span data-ttu-id="b43c9-520">Ländercode</span><span class="sxs-lookup"><span data-stu-id="b43c9-520">Country Code</span></span>          |
| <span data-ttu-id="b43c9-521">Postleitzahl</span><span class="sxs-lookup"><span data-stu-id="b43c9-521">Zip/Postal Code</span></span> | <span data-ttu-id="b43c9-522">PLZ</span><span class="sxs-lookup"><span data-stu-id="b43c9-522">Postal Code</span></span>           |
| <span data-ttu-id="b43c9-523">Zustand</span><span class="sxs-lookup"><span data-stu-id="b43c9-523">State</span></span>           | <span data-ttu-id="b43c9-524">Bundeslandcode</span><span class="sxs-lookup"><span data-stu-id="b43c9-524">State Code</span></span>            |
| <span data-ttu-id="b43c9-525">Stadt</span><span class="sxs-lookup"><span data-stu-id="b43c9-525">City</span></span>            | <span data-ttu-id="b43c9-526">Stadt</span><span class="sxs-lookup"><span data-stu-id="b43c9-526">City</span></span>                  |
| <span data-ttu-id="b43c9-527">Verwaltungsbezirk</span><span class="sxs-lookup"><span data-stu-id="b43c9-527">County</span></span>          | <span data-ttu-id="b43c9-528">Landkreis (Gemeinde)</span><span class="sxs-lookup"><span data-stu-id="b43c9-528">County (Municipality)</span></span> |
| <span data-ttu-id="b43c9-529">Straße</span><span class="sxs-lookup"><span data-stu-id="b43c9-529">Street</span></span>          | <span data-ttu-id="b43c9-530">Adresszeile 1</span><span class="sxs-lookup"><span data-stu-id="b43c9-530">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="b43c9-531">Steuerregionen</span><span class="sxs-lookup"><span data-stu-id="b43c9-531">Tax regions</span></span>

<span data-ttu-id="b43c9-532">Steuerregionen werden verwendet, um die entsprechende Steuer festzulegen, die bei der Lohngenerierung angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="b43c9-532">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="b43c9-533">Steuerregionen werden Dayforce als Standortadressen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="b43c9-533">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="b43c9-534">Die Standardsteuerregion muss der aktiven Position der Arbeitskraft zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="b43c9-534">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="b43c9-535">Steuerregion (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-535">Tax region (required)</span></span>
- <span data-ttu-id="b43c9-536">Land/Region (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-536">Country/Region (required)</span></span>
- <span data-ttu-id="b43c9-537">Bundesland/Kanton (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-537">State (required)</span></span>
- <span data-ttu-id="b43c9-538">Verwaltungsbezirk</span><span class="sxs-lookup"><span data-stu-id="b43c9-538">County</span></span> 
- <span data-ttu-id="b43c9-539">Ort (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="b43c9-539">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="b43c9-540">Konfigurieren Ihrer Daten, um Lohn in Mexiko zu generieren</span><span class="sxs-lookup"><span data-stu-id="b43c9-540">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="b43c9-541">Wenn Sie Vergütung für Mitarbeiter in Mexiko generieren, müssen die folgenden Elemente konfiguriert werden:</span><span class="sxs-lookup"><span data-stu-id="b43c9-541">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="b43c9-542">Abteilungen sind für Positionen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b43c9-542">Departments are required on positions.</span></span>
- <span data-ttu-id="b43c9-543">Kostenstellen müssen als Finanzdimensionen festgelegt werden und müssen das erste Element in der standardmäßigen Finanzdimensions-Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="b43c9-543">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="b43c9-544">Stellentypen</span><span class="sxs-lookup"><span data-stu-id="b43c9-544">Job types</span></span>

<span data-ttu-id="b43c9-545">Stellentypen werden verwendet, um ähnliche Stellen in Kategorien zu gruppieren.</span><span class="sxs-lookup"><span data-stu-id="b43c9-545">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="b43c9-546">Stellentypen sind erforderlich, um Lohn in Mexiko zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="b43c9-546">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="b43c9-547">Beispiele für Stellentypen umfassen Voll- und Teilzeit oder festes Gehalt und Stundenlohn.</span><span class="sxs-lookup"><span data-stu-id="b43c9-547">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="b43c9-548">Stellentypen werden Dayforce als Lohnarten zugeordnet, die angeben, ob ein Mitarbeiter auf Stundenbasis bezahlt wird oder ein festes Gehalt bezieht.</span><span class="sxs-lookup"><span data-stu-id="b43c9-548">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="b43c9-549">Folgende Stellentypen und Beschreibungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b43c9-549">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="b43c9-550">Stellentyp</span><span class="sxs-lookup"><span data-stu-id="b43c9-550">Job type</span></span>   | <span data-ttu-id="b43c9-551">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b43c9-551">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="b43c9-552">Stündlich</span><span class="sxs-lookup"><span data-stu-id="b43c9-552">Hourly</span></span>     | <span data-ttu-id="b43c9-553">MX – Stundenbasis</span><span class="sxs-lookup"><span data-stu-id="b43c9-553">MX Hourly</span></span>   |
| <span data-ttu-id="b43c9-554">Fest angestellt</span><span class="sxs-lookup"><span data-stu-id="b43c9-554">Salaried</span></span>   | <span data-ttu-id="b43c9-555">MX – Fest angestellt</span><span class="sxs-lookup"><span data-stu-id="b43c9-555">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="b43c9-556">Positionstypen</span><span class="sxs-lookup"><span data-stu-id="b43c9-556">Position types</span></span> 

<span data-ttu-id="b43c9-557">Sie verwenden Positionstypen, um zu beschreiben, ob die Position Vollzeit, Teilzeit oder etwas anderes ist.</span><span class="sxs-lookup"><span data-stu-id="b43c9-557">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="b43c9-558">Positionstypen werden Dayforce als Lohnklassen zugeordnet, die angeben, ob ein Mitarbeiter in Vollzeit oder Teilzeit arbeitet.</span><span class="sxs-lookup"><span data-stu-id="b43c9-558">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="b43c9-559">Folgende Positionstypen und Beschreibungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b43c9-559">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="b43c9-560">Positionstyp</span><span class="sxs-lookup"><span data-stu-id="b43c9-560">Position type</span></span>   | <span data-ttu-id="b43c9-561">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b43c9-561">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="b43c9-562">Vollzeit</span><span class="sxs-lookup"><span data-stu-id="b43c9-562">Full-time</span></span>       | <span data-ttu-id="b43c9-563">Vollzeitmitarbeiter</span><span class="sxs-lookup"><span data-stu-id="b43c9-563">Full time employee</span></span> |
| <span data-ttu-id="b43c9-564">Teilzeit</span><span class="sxs-lookup"><span data-stu-id="b43c9-564">Part-time</span></span>       | <span data-ttu-id="b43c9-565">Teilzeitmitarbeiter</span><span class="sxs-lookup"><span data-stu-id="b43c9-565">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="b43c9-566">Ursachencodes</span><span class="sxs-lookup"><span data-stu-id="b43c9-566">Reason codes</span></span>

<span data-ttu-id="b43c9-567">Ursachencodes enthalten Informationen zum Status eines Mitarbeiters.</span><span class="sxs-lookup"><span data-stu-id="b43c9-567">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="b43c9-568">Ursachencodes werden Dayforce als Statusgründe zugeordnet, die den Grund für Änderungen bei der Position eines Mitarbeiters oder dem Beschäftigungsstatus angeben.</span><span class="sxs-lookup"><span data-stu-id="b43c9-568">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="b43c9-569">Folgende Ursachencodes und Beschreibungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b43c9-569">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="b43c9-570">Ursachencode</span><span class="sxs-lookup"><span data-stu-id="b43c9-570">Reason code</span></span>            | <span data-ttu-id="b43c9-571">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b43c9-571">Description</span></span>                    | <span data-ttu-id="b43c9-572">Zutreffende Szenarios</span><span class="sxs-lookup"><span data-stu-id="b43c9-572">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="b43c9-573">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="b43c9-573">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="b43c9-574">Abgang vor erster Lohnzahlung</span><span class="sxs-lookup"><span data-stu-id="b43c9-574">Departure before first payroll</span></span> | <span data-ttu-id="b43c9-575">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="b43c9-575">Terminate worker</span></span>     |
| <span data-ttu-id="b43c9-576">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="b43c9-576">RESIGNATION</span></span>            | <span data-ttu-id="b43c9-577">Kündigung durch Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="b43c9-577">Resignation</span></span>                    | <span data-ttu-id="b43c9-578">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="b43c9-578">Terminate worker</span></span>     |
| <span data-ttu-id="b43c9-579">PENSION</span><span class="sxs-lookup"><span data-stu-id="b43c9-579">PENSION</span></span>                | <span data-ttu-id="b43c9-580">Rente</span><span class="sxs-lookup"><span data-stu-id="b43c9-580">Pension</span></span>                        | <span data-ttu-id="b43c9-581">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="b43c9-581">Terminate worker</span></span>     |
| <span data-ttu-id="b43c9-582">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="b43c9-582">TERMINATION</span></span>            | <span data-ttu-id="b43c9-583">Beendigung</span><span class="sxs-lookup"><span data-stu-id="b43c9-583">Termination</span></span>                    | <span data-ttu-id="b43c9-584">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="b43c9-584">Terminate worker</span></span>     |
| <span data-ttu-id="b43c9-585">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="b43c9-585">RETIREMENT</span></span>             | <span data-ttu-id="b43c9-586">Ruhestand</span><span class="sxs-lookup"><span data-stu-id="b43c9-586">Retirement</span></span>                     | <span data-ttu-id="b43c9-587">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="b43c9-587">Terminate worker</span></span>     |
| <span data-ttu-id="b43c9-588">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="b43c9-588">ABSENTEE</span></span>               | <span data-ttu-id="b43c9-589">Abwesende Person</span><span class="sxs-lookup"><span data-stu-id="b43c9-589">Absentee</span></span>                       | <span data-ttu-id="b43c9-590">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="b43c9-590">Terminate worker</span></span>     |
| <span data-ttu-id="b43c9-591">OTHER</span><span class="sxs-lookup"><span data-stu-id="b43c9-591">OTHER</span></span>                  | <span data-ttu-id="b43c9-592">Andere Gründe</span><span class="sxs-lookup"><span data-stu-id="b43c9-592">Other Reasons</span></span>                  | <span data-ttu-id="b43c9-593">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="b43c9-593">Terminate worker</span></span>     |
| <span data-ttu-id="b43c9-594">CLOSURE</span><span class="sxs-lookup"><span data-stu-id="b43c9-594">CLOSURE</span></span>                | <span data-ttu-id="b43c9-595">Betriebsferien</span><span class="sxs-lookup"><span data-stu-id="b43c9-595">Business Closure</span></span>               | <span data-ttu-id="b43c9-596">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="b43c9-596">Terminate worker</span></span>     |
| <span data-ttu-id="b43c9-597">DEATH</span><span class="sxs-lookup"><span data-stu-id="b43c9-597">DEATH</span></span>                  | <span data-ttu-id="b43c9-598">Tod</span><span class="sxs-lookup"><span data-stu-id="b43c9-598">Death</span></span>                          | <span data-ttu-id="b43c9-599">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="b43c9-599">Terminate worker</span></span>     |
| <span data-ttu-id="b43c9-600">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="b43c9-600">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="b43c9-601">Beurlaubung</span><span class="sxs-lookup"><span data-stu-id="b43c9-601">Leave of Absence</span></span>               | <span data-ttu-id="b43c9-602">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="b43c9-602">Terminate worker</span></span>     |
| <span data-ttu-id="b43c9-603">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="b43c9-603">CONTRACTEND</span></span>            | <span data-ttu-id="b43c9-604">Vertragsende</span><span class="sxs-lookup"><span data-stu-id="b43c9-604">End of Contract</span></span>                | <span data-ttu-id="b43c9-605">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="b43c9-605">Terminate worker</span></span>     |
| <span data-ttu-id="b43c9-606">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="b43c9-606">SALARYCHANGE</span></span>           | <span data-ttu-id="b43c9-607">Gehaltsänderung</span><span class="sxs-lookup"><span data-stu-id="b43c9-607">Change of Salary</span></span>               | <span data-ttu-id="b43c9-608">Vergütung</span><span class="sxs-lookup"><span data-stu-id="b43c9-608">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="b43c9-609">Einstellungsbedingungen</span><span class="sxs-lookup"><span data-stu-id="b43c9-609">Terms of employment</span></span>

<span data-ttu-id="b43c9-610">Beschäftigungsbedingungen werden verwendet, um Kategorien von Beschäftigungsbedingungen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b43c9-610">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="b43c9-611">Die Bedingungen werden Dayforce als Beschäftigungsindikatorwerte zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="b43c9-611">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="b43c9-612">Die folgenden Bedingungen für Beschäftigung und Beschreibungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b43c9-612">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="b43c9-613">Einstellungsbedingungen</span><span class="sxs-lookup"><span data-stu-id="b43c9-613">Terms of employment</span></span>   | <span data-ttu-id="b43c9-614">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b43c9-614">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="b43c9-615">Regelmäßig</span><span class="sxs-lookup"><span data-stu-id="b43c9-615">Regular</span></span>               | <span data-ttu-id="b43c9-616">Regelmäßig</span><span class="sxs-lookup"><span data-stu-id="b43c9-616">Regular</span></span>     |
| <span data-ttu-id="b43c9-617">Direkt</span><span class="sxs-lookup"><span data-stu-id="b43c9-617">Direct</span></span>                | <span data-ttu-id="b43c9-618">Direkt</span><span class="sxs-lookup"><span data-stu-id="b43c9-618">Direct</span></span>      |
| <span data-ttu-id="b43c9-619">Praktikum</span><span class="sxs-lookup"><span data-stu-id="b43c9-619">Internship</span></span>            | <span data-ttu-id="b43c9-620">Praktikum</span><span class="sxs-lookup"><span data-stu-id="b43c9-620">Internship</span></span>  |
| <span data-ttu-id="b43c9-621">Unbefristet</span><span class="sxs-lookup"><span data-stu-id="b43c9-621">Permanent</span></span>             | <span data-ttu-id="b43c9-622">Unbefristet</span><span class="sxs-lookup"><span data-stu-id="b43c9-622">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="b43c9-623">Familienstand</span><span class="sxs-lookup"><span data-stu-id="b43c9-623">Marital status</span></span>

<span data-ttu-id="b43c9-624">Familienstandwerte werden Dayforce zugeordnet und werden – je nach Bedarf – in die akzeptierten Werte bei der Integration übersetzt.</span><span class="sxs-lookup"><span data-stu-id="b43c9-624">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="b43c9-625">Die folgende Tabelle zeigt, wie Familienstandwerte Dayforce zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="b43c9-625">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="b43c9-626">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="b43c9-626">Human Resources</span></span>                 | <span data-ttu-id="b43c9-627">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b43c9-627">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="b43c9-628">Verheiratet</span><span class="sxs-lookup"><span data-stu-id="b43c9-628">Married</span></span>                | <span data-ttu-id="b43c9-629">Verheiratet</span><span class="sxs-lookup"><span data-stu-id="b43c9-629">Married</span></span>                   |
| <span data-ttu-id="b43c9-630">Ledig</span><span class="sxs-lookup"><span data-stu-id="b43c9-630">Single</span></span>                 | <span data-ttu-id="b43c9-631">Ledig</span><span class="sxs-lookup"><span data-stu-id="b43c9-631">Single</span></span>                    |
| <span data-ttu-id="b43c9-632">Verwitwet</span><span class="sxs-lookup"><span data-stu-id="b43c9-632">Widowed</span></span>                | <span data-ttu-id="b43c9-633">Verwitwet</span><span class="sxs-lookup"><span data-stu-id="b43c9-633">Widowed</span></span>                   |
| <span data-ttu-id="b43c9-634">Geschieden</span><span class="sxs-lookup"><span data-stu-id="b43c9-634">Divorced</span></span>               | <span data-ttu-id="b43c9-635">Geschieden</span><span class="sxs-lookup"><span data-stu-id="b43c9-635">Divorced</span></span>                  |
| <span data-ttu-id="b43c9-636">Eingetragene Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="b43c9-636">Registered Partnership</span></span> | <span data-ttu-id="b43c9-637">Inländische Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="b43c9-637">Domestic Partnership</span></span>      |
| <span data-ttu-id="b43c9-638">None</span><span class="sxs-lookup"><span data-stu-id="b43c9-638">None</span></span>                   | <span data-ttu-id="b43c9-639">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="b43c9-639">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="b43c9-640">Freie Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="b43c9-640">Cohabiting</span></span>             | <span data-ttu-id="b43c9-641">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="b43c9-641">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="b43c9-642">Geschlecht</span><span class="sxs-lookup"><span data-stu-id="b43c9-642">Gender</span></span>

<span data-ttu-id="b43c9-643">Geschlechtsbezeichnungen werden Dayforce zugeordnet und werden – je nach Bedarf – in die akzeptierten Werte bei der Integration übersetzt.</span><span class="sxs-lookup"><span data-stu-id="b43c9-643">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="b43c9-644">Die folgende Tabelle zeigt, wie Geschlechtsbezeichnungen Dayforce zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="b43c9-644">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="b43c9-645">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="b43c9-645">Human Resources</span></span>       | <span data-ttu-id="b43c9-646">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b43c9-646">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="b43c9-647">Männl.</span><span class="sxs-lookup"><span data-stu-id="b43c9-647">Male</span></span>         | <span data-ttu-id="b43c9-648">Männl.</span><span class="sxs-lookup"><span data-stu-id="b43c9-648">Male</span></span>                      |
| <span data-ttu-id="b43c9-649">Weibl.</span><span class="sxs-lookup"><span data-stu-id="b43c9-649">Female</span></span>       | <span data-ttu-id="b43c9-650">Weibl.</span><span class="sxs-lookup"><span data-stu-id="b43c9-650">Female</span></span>                    |
| <span data-ttu-id="b43c9-651">Nicht spezifisch</span><span class="sxs-lookup"><span data-stu-id="b43c9-651">Non-specific</span></span> | <span data-ttu-id="b43c9-652">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="b43c9-652">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="b43c9-653">Zahlungsweise</span><span class="sxs-lookup"><span data-stu-id="b43c9-653">Payment method</span></span>

<span data-ttu-id="b43c9-654">Zahlungsmethoden geben dem Mitarbeiter und dem Unternehmen die Möglichkeit zu beschreiben, wie Mitarbeiter bezahlt werden.</span><span class="sxs-lookup"><span data-stu-id="b43c9-654">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="b43c9-655">Zahlungsmethoden werden Dayforce zugeordnet und werden – je nach Bedarf – in die akzeptierten Werte bei der Integration übersetzt.</span><span class="sxs-lookup"><span data-stu-id="b43c9-655">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="b43c9-656">Die folgende Tabelle zeigt, wie Zahlungsmethoden Dayforce zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="b43c9-656">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="b43c9-657">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="b43c9-657">Human Resources</span></span>             | <span data-ttu-id="b43c9-658">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b43c9-658">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="b43c9-659">Bargeld</span><span class="sxs-lookup"><span data-stu-id="b43c9-659">Cash</span></span>               | <span data-ttu-id="b43c9-660">Bargeld</span><span class="sxs-lookup"><span data-stu-id="b43c9-660">Cash</span></span>                      |
| <span data-ttu-id="b43c9-661">Elektronische Zahlung</span><span class="sxs-lookup"><span data-stu-id="b43c9-661">Electronic Payment</span></span> | <span data-ttu-id="b43c9-662">Übertragen</span><span class="sxs-lookup"><span data-stu-id="b43c9-662">Transfer</span></span>                  |
| <span data-ttu-id="b43c9-663">Prüfen</span><span class="sxs-lookup"><span data-stu-id="b43c9-663">Check</span></span>              | <span data-ttu-id="b43c9-664">Scheck</span><span class="sxs-lookup"><span data-stu-id="b43c9-664">Cheque</span></span>                    |
| <span data-ttu-id="b43c9-665">Bankwechsel</span><span class="sxs-lookup"><span data-stu-id="b43c9-665">Bank Draft</span></span>         | <span data-ttu-id="b43c9-666">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="b43c9-666">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="b43c9-667">Sonstige</span><span class="sxs-lookup"><span data-stu-id="b43c9-667">Other</span></span>              | <span data-ttu-id="b43c9-668">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="b43c9-668">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="b43c9-669">Bankkontotyp</span><span class="sxs-lookup"><span data-stu-id="b43c9-669">Bank account type</span></span>

<span data-ttu-id="b43c9-670">Bankkontotypen werden für elektronische Zahlungen an Mitarbeiter verwendet.</span><span class="sxs-lookup"><span data-stu-id="b43c9-670">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="b43c9-671">Bankkontotypen werden Dayforce als Übergweisungskontoinformationen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="b43c9-671">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="b43c9-672">Die Bankkontotypen werden bei Bedarf zu den akzeptierten Werte nach der Integration übersetzt.</span><span class="sxs-lookup"><span data-stu-id="b43c9-672">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="b43c9-673">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="b43c9-673">Human Resources</span></span>            | <span data-ttu-id="b43c9-674">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b43c9-674">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="b43c9-675">Girokonto</span><span class="sxs-lookup"><span data-stu-id="b43c9-675">Checking Account</span></span>  | <span data-ttu-id="b43c9-676">Girokonto</span><span class="sxs-lookup"><span data-stu-id="b43c9-676">CheckingAccount</span></span>           |
| <span data-ttu-id="b43c9-677">Lohnkonto</span><span class="sxs-lookup"><span data-stu-id="b43c9-677">Payroll Account</span></span>   | <span data-ttu-id="b43c9-678">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="b43c9-678">PayrollAccount</span></span>            |
| <span data-ttu-id="b43c9-679">Sparkonto</span><span class="sxs-lookup"><span data-stu-id="b43c9-679">Savings Account</span></span>   | <span data-ttu-id="b43c9-680">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="b43c9-680">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="b43c9-681">BankGirot-Konto</span><span class="sxs-lookup"><span data-stu-id="b43c9-681">BankGirot account</span></span> | <span data-ttu-id="b43c9-682">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="b43c9-682">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="b43c9-683">PlusGirot-Konto</span><span class="sxs-lookup"><span data-stu-id="b43c9-683">PlusGirot account</span></span> | <span data-ttu-id="b43c9-684">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="b43c9-684">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="b43c9-685">Einkommenscodes</span><span class="sxs-lookup"><span data-stu-id="b43c9-685">Earning codes</span></span>

<span data-ttu-id="b43c9-686">Einkommenscodes bestimmen jeden Typ von Einkünften eindeutig, die Arbeitskräfte erhalten</span><span class="sxs-lookup"><span data-stu-id="b43c9-686">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="b43c9-687">Die Codes decken verschiedene Parameter ab, die sich auf Einkünfte beziehen, wie beispielsweise Buchhaltungsvorschriften, Steuergesetze, Berichterstellungsanforderungen und Bruttoausgleichsfähigkeit.</span><span class="sxs-lookup"><span data-stu-id="b43c9-687">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="b43c9-688">Wenn eine nicht unterstützte Häufigkeit verwendet wird, wird die Häufigkeit **Jeder Lohn** standardmäßig für die Berechnung verwendet.</span><span class="sxs-lookup"><span data-stu-id="b43c9-688">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="b43c9-689">Unterstützte Häufigkeiten</span><span class="sxs-lookup"><span data-stu-id="b43c9-689">Supported frequencies</span></span>

- <span data-ttu-id="b43c9-690">Alle</span><span class="sxs-lookup"><span data-stu-id="b43c9-690">All</span></span>
- <span data-ttu-id="b43c9-691">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="b43c9-691">EVERYPAY</span></span>
- <span data-ttu-id="b43c9-692">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="b43c9-692">EACHPAYPERIOD</span></span>
- <span data-ttu-id="b43c9-693">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="b43c9-693">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="b43c9-694">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="b43c9-694">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="b43c9-695">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="b43c9-695">1OFMTH</span></span>
- <span data-ttu-id="b43c9-696">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="b43c9-696">LASTOFMTH</span></span>
- <span data-ttu-id="b43c9-697">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="b43c9-697">2OFMTH</span></span>
- <span data-ttu-id="b43c9-698">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="b43c9-698">3OFMTH</span></span>
- <span data-ttu-id="b43c9-699">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b43c9-699">4OFMTH</span></span>
- <span data-ttu-id="b43c9-700">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="b43c9-700">5OFMTH</span></span>
- <span data-ttu-id="b43c9-701">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="b43c9-701">1N2OFMTH</span></span>
- <span data-ttu-id="b43c9-702">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b43c9-702">3N4OFMTH</span></span>
- <span data-ttu-id="b43c9-703">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="b43c9-703">1N3OFMTH</span></span>
- <span data-ttu-id="b43c9-704">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b43c9-704">1N4OFMTH</span></span>
- <span data-ttu-id="b43c9-705">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="b43c9-705">2N3OFMTH</span></span>
- <span data-ttu-id="b43c9-706">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b43c9-706">2N4OFMTH</span></span>
- <span data-ttu-id="b43c9-707">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="b43c9-707">1N2N3OFMTH</span></span>
- <span data-ttu-id="b43c9-708">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b43c9-708">1N2N4OFMTH</span></span>
- <span data-ttu-id="b43c9-709">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b43c9-709">1N3N4OFMTH</span></span>
- <span data-ttu-id="b43c9-710">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b43c9-710">2N3N4OFMTH</span></span>
- <span data-ttu-id="b43c9-711">1N2N3N4OFMTH – 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b43c9-711">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="b43c9-712">2N3N4N5OFMth – 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="b43c9-712">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="b43c9-713">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="b43c9-713">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="b43c9-714">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="b43c9-714">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="b43c9-715">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="b43c9-715">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="b43c9-716">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="b43c9-716">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="b43c9-717">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="b43c9-717">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="b43c9-718">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="b43c9-718">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="b43c9-719">Adressen</span><span class="sxs-lookup"><span data-stu-id="b43c9-719">Addresses</span></span>

<span data-ttu-id="b43c9-720">Die Kennung bestimmter Codes für Land oder Region, Bundesland/Kanton oder Landkreis (Gemeinde) erfordert spezifische Formate, die Dayforce und Anbieter innerhalb des Landes/innerhalb der Region erkennen können.</span><span class="sxs-lookup"><span data-stu-id="b43c9-720">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="b43c9-721">Obwohl das Format für Orte flexibel ist, muss jeder Ort einem Bundesland zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="b43c9-721">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="b43c9-722">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="b43c9-722">Human Resources</span></span>              | <span data-ttu-id="b43c9-723">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b43c9-723">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="b43c9-724">Land/Region</span><span class="sxs-lookup"><span data-stu-id="b43c9-724">Country/Region</span></span>      | <span data-ttu-id="b43c9-725">Ländercode</span><span class="sxs-lookup"><span data-stu-id="b43c9-725">Country Code</span></span>          |
| <span data-ttu-id="b43c9-726">Postleitzahl</span><span class="sxs-lookup"><span data-stu-id="b43c9-726">Zip/Postal Code</span></span>     | <span data-ttu-id="b43c9-727">PLZ</span><span class="sxs-lookup"><span data-stu-id="b43c9-727">Postal Code</span></span>           |
| <span data-ttu-id="b43c9-728">Zustand</span><span class="sxs-lookup"><span data-stu-id="b43c9-728">State</span></span>               | <span data-ttu-id="b43c9-729">Bundeslandcode</span><span class="sxs-lookup"><span data-stu-id="b43c9-729">State Code</span></span>            |
| <span data-ttu-id="b43c9-730">Stadt</span><span class="sxs-lookup"><span data-stu-id="b43c9-730">City</span></span>                | <span data-ttu-id="b43c9-731">Stadt</span><span class="sxs-lookup"><span data-stu-id="b43c9-731">City</span></span>                  |
| <span data-ttu-id="b43c9-732">Verwaltungsbezirk</span><span class="sxs-lookup"><span data-stu-id="b43c9-732">County</span></span>              | <span data-ttu-id="b43c9-733">Landkreis (Gemeinde)</span><span class="sxs-lookup"><span data-stu-id="b43c9-733">County (Municipality)</span></span> |
| <span data-ttu-id="b43c9-734">Straße</span><span class="sxs-lookup"><span data-stu-id="b43c9-734">Street</span></span>              | <span data-ttu-id="b43c9-735">Adresszeile 1</span><span class="sxs-lookup"><span data-stu-id="b43c9-735">Address Line 1</span></span>        |
| <span data-ttu-id="b43c9-736">Hausnummer</span><span class="sxs-lookup"><span data-stu-id="b43c9-736">Street Number</span></span>       | <span data-ttu-id="b43c9-737">Adresszeile 2</span><span class="sxs-lookup"><span data-stu-id="b43c9-737">Address Line 2</span></span>        |
| <span data-ttu-id="b43c9-738">Gebäudeergänzung</span><span class="sxs-lookup"><span data-stu-id="b43c9-738">Building Complement</span></span> | <span data-ttu-id="b43c9-739">Adresszeile 5</span><span class="sxs-lookup"><span data-stu-id="b43c9-739">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="b43c9-740">Ausweisnummer</span><span class="sxs-lookup"><span data-stu-id="b43c9-740">Passport number</span></span>

<span data-ttu-id="b43c9-741">Mitarbeiter können Ausweisinformationen melden.</span><span class="sxs-lookup"><span data-stu-id="b43c9-741">Employees can declare passport information.</span></span> <span data-ttu-id="b43c9-742">Diese Informationen haben den Kennungstyp **Ausweis** und sind in Dayforce als Teil der für Mexiko spezifischen Informationen eines Mitarbeiters integriert.</span><span class="sxs-lookup"><span data-stu-id="b43c9-742">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="b43c9-743">Kennungstyp = „Ausweis”</span><span class="sxs-lookup"><span data-stu-id="b43c9-743">Identification Type = "Passport"</span></span>
- <span data-ttu-id="b43c9-744">Ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="b43c9-744">Issued Date</span></span>
- <span data-ttu-id="b43c9-745">Ablaufdatum</span><span class="sxs-lookup"><span data-stu-id="b43c9-745">Expiration Date</span></span>

<span data-ttu-id="b43c9-746">Mitarbeiter können mehrere Kennungsnummern des Kennungstyps **Ausweis** melden.</span><span class="sxs-lookup"><span data-stu-id="b43c9-746">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="b43c9-747">Jedoch wird nur der aktuell aktive Ausweiseintrag in Dayforce integriert.</span><span class="sxs-lookup"><span data-stu-id="b43c9-747">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="b43c9-748">Wenn alle Ausweiseinträge abgelaufen sind, ist der Ausweis, der zuletzt ausgestellt wurde, in Dayforce integriert.</span><span class="sxs-lookup"><span data-stu-id="b43c9-748">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]