---
title: Die Lohnintegration zwischen Talent und Dayforce konfigurieren
description: In diesem Thema wird erläutert, wie Sie die Integration zwischen Microsoft Dynamics 365 Talent und Ceridian Dayforce konfigurieren, damit Sie den Zahlungslauf verarbeiten können.
author: andreabichsel
manager: AnnBe
ms.date: 06/24/2019
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
ms.openlocfilehash: 075b2bdfa08bb190f66b6d60074e1263feedcf70
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898532"
---
# <a name="configure-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="48e7e-103">Konfigurieren der Lohnintegration zwischen Talent und Dayforce</span><span class="sxs-lookup"><span data-stu-id="48e7e-103">Configure payroll integration between Talent and Dayforce</span></span>

<span data-ttu-id="48e7e-104">Die Integration zwischen Microsoft Dynamics 365 Talent und Ceridian Dayforce beruht auf mehreren Konfigurationsschritten, die in diesem Thema beschrieben sind.</span><span class="sxs-lookup"><span data-stu-id="48e7e-104">The integration between Microsoft Dynamics 365 Talent and Ceridian Dayforce relies on several configuration steps that are described in this topic.</span></span> <span data-ttu-id="48e7e-105">Sie müssen die Integration sowohl in Talent als auch in Dayforce konfigurieren, bevor Sie einen Zahllauf verarbeiten können.</span><span class="sxs-lookup"><span data-stu-id="48e7e-105">You must configure the integration in both Talent and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="48e7e-106">Wenn Sie einen Dienst wie Dayforce verwenden, um Zahlläufe abzuschließen, müssen Sie die Integration in Talent ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="48e7e-106">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Talent.</span></span> <span data-ttu-id="48e7e-107">Die Integration erfordert bestimmte Daten aus Talent.</span><span class="sxs-lookup"><span data-stu-id="48e7e-107">The integration requires specific data from Talent.</span></span> <span data-ttu-id="48e7e-108">Daher müssen Sie überprüfen, dass die Daten, die Dayforce zugeordnet sind, in Talent in einer Weise konfiguriert werden, die die Integration unterstützt.</span><span class="sxs-lookup"><span data-stu-id="48e7e-108">Therefore, you must verify that data that is mapped to Dayforce is configured in Talent in a manner that supports the integration.</span></span> <span data-ttu-id="48e7e-109">Bei der Integration werden die folgenden allgemeinen Kategorien von Daten verwendet:</span><span class="sxs-lookup"><span data-stu-id="48e7e-109">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="48e7e-110">Personalverwaltungsdaten</span><span class="sxs-lookup"><span data-stu-id="48e7e-110">Human resources data</span></span>
- <span data-ttu-id="48e7e-111">Vergütungsdaten</span><span class="sxs-lookup"><span data-stu-id="48e7e-111">Compensation data</span></span>
- <span data-ttu-id="48e7e-112">Lohndaten, wie Lohnzyklen, Lohnperioden und Einkommenscodes</span><span class="sxs-lookup"><span data-stu-id="48e7e-112">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="48e7e-113">Arbeitskraftdaten</span><span class="sxs-lookup"><span data-stu-id="48e7e-113">Worker data</span></span>

<span data-ttu-id="48e7e-114">In diesem Thema werden die Schritte beschrieben, die Sie befolgen müssen, um die Integration zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="48e7e-114">This topic describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="48e7e-115">Es werden auch die Datentypen und die Konfigurationsdetails erklärt, die für die Integration erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="48e7e-115">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="48e7e-116">Die Integration aktivieren</span><span class="sxs-lookup"><span data-stu-id="48e7e-116">Enable the integration</span></span>

<span data-ttu-id="48e7e-117">In Talent müssen Sie die Integration aktivieren und die Konfigurationsinformationen eingeben, um eine Verbindung mit Dayforce herzustellen.</span><span class="sxs-lookup"><span data-stu-id="48e7e-117">In Talent, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="48e7e-118">Wenn Sie möchten, dass die erstellte Hauptbuchtransaktion in Microsoft Dynamics 365 Finance importiert wird, müssen Sie auch ein Microsoft Azure-Speicherkonto einrichten und die Azure Storage-Verbindungszeichenfolge in Finance eingeben.</span><span class="sxs-lookup"><span data-stu-id="48e7e-118">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 Finance, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance.</span></span>

<span data-ttu-id="48e7e-119">Um die Integration in Talent zu aktivieren, gehen Sie folgendermaßen vor.</span><span class="sxs-lookup"><span data-stu-id="48e7e-119">To turn on the integration in Talent, follow these steps.</span></span>

1. <span data-ttu-id="48e7e-120">Wählen Sie auf der Seite **Systemverwaltung** die Option **Integrationskonfiguration** aus.</span><span class="sxs-lookup"><span data-stu-id="48e7e-120">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="48e7e-121">Geben Sie den sicheren Datenübertragungsprotokoll-(FTP)-Endpunkt und den sicheren FTP-Ordnerpfad ein.</span><span class="sxs-lookup"><span data-stu-id="48e7e-121">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="48e7e-122">Geben Sie den Benutzernamen und das Kennwort des Benutzers ein, der auf den sicheren FTP-Endpunkt und Ordnerpfad zugreift.</span><span class="sxs-lookup"><span data-stu-id="48e7e-122">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="48e7e-123">Testen Sie die Verbindung nach Bedarf, und legen Sie die Option **Lohnintegration aktivieren** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="48e7e-123">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="48e7e-124">Wenn die Integration aktiviert ist, werden Datenexportpaket und Dateien erstellt und die Häufigkeit wird festgelegt.</span><span class="sxs-lookup"><span data-stu-id="48e7e-124">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="48e7e-125">Sie können diese Häufigkeit nach Bedarf ändern.</span><span class="sxs-lookup"><span data-stu-id="48e7e-125">You can change this frequency as you require.</span></span>

<span data-ttu-id="48e7e-126">Weitere Informationen zu Azure-Speicherkonten und Azure Storage-Verbindungszeichenfolgen finden Sie in den folgenden Azure-Themen:</span><span class="sxs-lookup"><span data-stu-id="48e7e-126">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure topics:</span></span>

- [<span data-ttu-id="48e7e-127">Über Azure-Speicherkonten</span><span class="sxs-lookup"><span data-stu-id="48e7e-127">About Azure storage accounts</span></span>](https://docs.microsoft.com/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="48e7e-128">Azure Storage-Verbindungszeichenfolgen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="48e7e-128">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="48e7e-129">Technische Details, wenn Lohnintegration aktiviert ist</span><span class="sxs-lookup"><span data-stu-id="48e7e-129">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="48e7e-130">Die Aktivierung von Lohnintegration hat zwei primäre Auswirkungen:</span><span class="sxs-lookup"><span data-stu-id="48e7e-130">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="48e7e-131">Ein Datenexportprojekt namens „Lohnintegrationsexport“ wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="48e7e-131">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="48e7e-132">Dieses Projekt enthält die Entitäten und Felder, die für die Lohnintegration erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="48e7e-132">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="48e7e-133">Um das Projekt zu überprüfen, wechseln Sie zu **Systemverwaltung**, wählen Sie die Kachel **Datenverwaltung** aus, und öffnen Sie anschließend das Datenprojekt aus der Projektliste.</span><span class="sxs-lookup"><span data-stu-id="48e7e-133">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="48e7e-134">Dieser Stapelverarbeitungsauftrag führt das Datenexportprojekt aus, verschlüsselt das Datenpaket und überträgt die Datenenpaketdatei auf den SFTP-Endpunkt, der auf dem Bildschirm **Integrationskonfiguration** konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="48e7e-134">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="48e7e-135">Das Datenpaket, das zum SFTP-Endpunkt übertragen wird, wird mit einem Schlüssel verschlüsselt, für das Paket eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="48e7e-135">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="48e7e-136">Der Schlüssel befindet sich in einer Azure Key Vault, auf den nur durch Ceridian zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="48e7e-136">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="48e7e-137">Es ist nicht möglich, die Datenpaketinhalte zu entschlüsseln und zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="48e7e-137">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="48e7e-138">Wenn Sie den Inhalt des Datenpakets überprüfen möchten, müssen Sie das Datenprojekt „Lohnintegrationsexport“ manuell exportieren, herunterladen und dann öffnen.</span><span class="sxs-lookup"><span data-stu-id="48e7e-138">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="48e7e-139">Beim manuellen Export wird keine Verschlüsselung angewendet oder das Paket übertragen.</span><span class="sxs-lookup"><span data-stu-id="48e7e-139">Manual export will not apply encryption or transfer the package.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="48e7e-140">Ihre Daten konfigurieren</span><span class="sxs-lookup"><span data-stu-id="48e7e-140">Configure your data</span></span> 

<span data-ttu-id="48e7e-141">Um die Lohnbuchung zu verarbeiten, müssen Sie Personalverwaltungsdaten in Talent konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="48e7e-141">To process payroll, you must configure human resource data in Talent.</span></span> <span data-ttu-id="48e7e-142">Sie müssen Organisationsdaten, wie Stellen und Positionen, zusammen mit Vorteilen Vergütungsinformationen einrichten.</span><span class="sxs-lookup"><span data-stu-id="48e7e-142">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="48e7e-143">Diese Informationen stellen Beschäftigung, Lohn und die Abzugsinformationen bereit, die zur Generierung der Mitarbeiterentlohnung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="48e7e-143">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="48e7e-144">Personalverwaltungsdaten</span><span class="sxs-lookup"><span data-stu-id="48e7e-144">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="48e7e-145">Vergütungen</span><span class="sxs-lookup"><span data-stu-id="48e7e-145">Benefits</span></span> 

<span data-ttu-id="48e7e-146">Die Personalverwaltung stellt eine Reihe von Tools für die Einrichtung und Verwaltung der Vorteile, Abzüge und Vergütungspläne der Arbeitskräfte bereit, die eine Organisation für seine Arbeitskräfte anbietet oder verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="48e7e-146">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="48e7e-147">Wenn Sie Vorteile erstellen, sollten Sie folgende Daten und Konfigurationen bedenken, die in Dayforce verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="48e7e-147">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="48e7e-148">Vorteilspläne</span><span class="sxs-lookup"><span data-stu-id="48e7e-148">Benefit plans</span></span>

- <span data-ttu-id="48e7e-149">Plan (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-149">Plan (required)</span></span>
- <span data-ttu-id="48e7e-150">Typ (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-150">Type (required)</span></span>
- <span data-ttu-id="48e7e-151">Lohnauswirkung (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-151">Payroll impact (required)</span></span>
- <span data-ttu-id="48e7e-152">Rückstände wiederherstellen</span><span class="sxs-lookup"><span data-stu-id="48e7e-152">Recover arrears</span></span>
- <span data-ttu-id="48e7e-153">Abzugsverfahren</span><span class="sxs-lookup"><span data-stu-id="48e7e-153">Deduction method</span></span>
- <span data-ttu-id="48e7e-154">Abzugspriorität</span><span class="sxs-lookup"><span data-stu-id="48e7e-154">Deduction priority</span></span>
- <span data-ttu-id="48e7e-155">Periode eingrenzen</span><span class="sxs-lookup"><span data-stu-id="48e7e-155">Limit period</span></span>
- <span data-ttu-id="48e7e-156">Limitbetrag</span><span class="sxs-lookup"><span data-stu-id="48e7e-156">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="48e7e-157">Vergütungen</span><span class="sxs-lookup"><span data-stu-id="48e7e-157">Benefits</span></span>

- <span data-ttu-id="48e7e-158">Plan (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-158">Plan (required)</span></span>
- <span data-ttu-id="48e7e-159">Typ (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-159">Type (required)</span></span>
- <span data-ttu-id="48e7e-160">Option (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-160">Option (required)</span></span>
- <span data-ttu-id="48e7e-161">Vorteilskennung (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-161">Benefit ID (required)</span></span>
- <span data-ttu-id="48e7e-162">Häufigkeit</span><span class="sxs-lookup"><span data-stu-id="48e7e-162">Frequency</span></span>
- <span data-ttu-id="48e7e-163">Basis</span><span class="sxs-lookup"><span data-stu-id="48e7e-163">Basis</span></span>
- <span data-ttu-id="48e7e-164">Betrag oder Satz</span><span class="sxs-lookup"><span data-stu-id="48e7e-164">Amount or rate</span></span>
- <span data-ttu-id="48e7e-165">Einkommenscode</span><span class="sxs-lookup"><span data-stu-id="48e7e-165">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="48e7e-166">Unterstützte Häufigkeiten</span><span class="sxs-lookup"><span data-stu-id="48e7e-166">Supported frequencies</span></span> 

- <span data-ttu-id="48e7e-167">Wöchentlich</span><span class="sxs-lookup"><span data-stu-id="48e7e-167">Weekly</span></span>
- <span data-ttu-id="48e7e-168">14-tägig</span><span class="sxs-lookup"><span data-stu-id="48e7e-168">Bi-weekly</span></span>
- <span data-ttu-id="48e7e-169">Halbmonatlich</span><span class="sxs-lookup"><span data-stu-id="48e7e-169">Semi-monthly</span></span>
- <span data-ttu-id="48e7e-170">Monatlich</span><span class="sxs-lookup"><span data-stu-id="48e7e-170">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="48e7e-171">Unterstützte Basen</span><span class="sxs-lookup"><span data-stu-id="48e7e-171">Supported bases</span></span> 

- <span data-ttu-id="48e7e-172">Fester Betrag</span><span class="sxs-lookup"><span data-stu-id="48e7e-172">Fixed amount</span></span>
- <span data-ttu-id="48e7e-173">Prozent des Einkommens</span><span class="sxs-lookup"><span data-stu-id="48e7e-173">Percent of earnings</span></span>
- <span data-ttu-id="48e7e-174">Produktive Stunden</span><span class="sxs-lookup"><span data-stu-id="48e7e-174">Productive hours</span></span>

<span data-ttu-id="48e7e-175">Dayforce erstellt die folgenden Abzüge, basierend auf den Lohnauswirkungen, die im Vorteilsplan definiert sind.</span><span class="sxs-lookup"><span data-stu-id="48e7e-175">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="48e7e-176">Auswahl in Talent</span><span class="sxs-lookup"><span data-stu-id="48e7e-176">Selection in Talent</span></span>        | <span data-ttu-id="48e7e-177">Ergebnis in Dayforce</span><span class="sxs-lookup"><span data-stu-id="48e7e-177">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="48e7e-178">None</span><span class="sxs-lookup"><span data-stu-id="48e7e-178">None</span></span>                       | <span data-ttu-id="48e7e-179">Es wird kein Abzug erstellt.</span><span class="sxs-lookup"><span data-stu-id="48e7e-179">No deduction is created.</span></span>                      |
| <span data-ttu-id="48e7e-180">Nur Abzug</span><span class="sxs-lookup"><span data-stu-id="48e7e-180">Deduction only</span></span>             | <span data-ttu-id="48e7e-181">Ein Mitarbeiterabzug wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="48e7e-181">An employee deduction is created.</span></span>             |
| <span data-ttu-id="48e7e-182">Nur Beitrag</span><span class="sxs-lookup"><span data-stu-id="48e7e-182">Contribution only</span></span>          | <span data-ttu-id="48e7e-183">Ein Arbeitgeberabzug wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="48e7e-183">An employer deduction is created.</span></span>             |
| <span data-ttu-id="48e7e-184">Abzug und Beitrag</span><span class="sxs-lookup"><span data-stu-id="48e7e-184">Deduction and contribution</span></span> | <span data-ttu-id="48e7e-185">Mitarbeiter- und Arbeitgeberabzüge werden erstellt.</span><span class="sxs-lookup"><span data-stu-id="48e7e-185">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="48e7e-186">Weitere Informationen darüber, wie Sie ein Vorteilsprogramm definieren und verwalten finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="48e7e-186">For more information about how to define and manage a benefits program, see the following topics:</span></span>

- [<span data-ttu-id="48e7e-187">Mitarbeitervergütungsprogramm bereitstellen</span><span class="sxs-lookup"><span data-stu-id="48e7e-187">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="48e7e-188">Neuen Vorteil erstellen</span><span class="sxs-lookup"><span data-stu-id="48e7e-188">Create a new benefit</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="48e7e-189">Vorteilsberechtigungsregeln und Richtlinien definieren</span><span class="sxs-lookup"><span data-stu-id="48e7e-189">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="48e7e-190">Vorteile von Arbeitskräften registrieren und entfernen</span><span class="sxs-lookup"><span data-stu-id="48e7e-190">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="48e7e-191">Vergütung</span><span class="sxs-lookup"><span data-stu-id="48e7e-191">Compensation</span></span> 

<span data-ttu-id="48e7e-192">Die Vergütungsverwaltung dient zum Steuern der Abwicklung des Grundlohns und der Prämien.</span><span class="sxs-lookup"><span data-stu-id="48e7e-192">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="48e7e-193">Sie steuern den festen Grundlohn eines Mitarbeiters und dessen Lohnsteigerungen nach Plänen für feste Vergütung.</span><span class="sxs-lookup"><span data-stu-id="48e7e-193">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="48e7e-194">Die Zahlung leistungsbezogener Prämien, wie Boni, Leistungsprämien, Aktienoptionen und -überlassungen sowie Einmalprämien werden durch Pläne für variable Vergütung gesteuert.</span><span class="sxs-lookup"><span data-stu-id="48e7e-194">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="48e7e-195">Dayforce verwendet Vergütungsinformationen, um einen Stunden- oder Jahressatz für einen Mitarbeiter zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="48e7e-195">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="48e7e-196">Feste Vergütungspläne und Lohnsatzumrechnungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="48e7e-196">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="48e7e-197">Mitarbeiter müssen einem festen Vergütungsplan zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="48e7e-197">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="48e7e-198">Weitere Informationen zu Vergütungsplänen finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="48e7e-198">For more information about compensation plans, see the following topics:</span></span>

- [<span data-ttu-id="48e7e-199">Feste Vergütungspläne erstellen</span><span class="sxs-lookup"><span data-stu-id="48e7e-199">Create fixed compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="48e7e-200">Variable Vergütungspläne erstellen</span><span class="sxs-lookup"><span data-stu-id="48e7e-200">Create variable compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="48e7e-201">Gehalts-/Vergütungsstruktur und -pläne entwickeln</span><span class="sxs-lookup"><span data-stu-id="48e7e-201">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="48e7e-202">Vergütung verarbeiten</span><span class="sxs-lookup"><span data-stu-id="48e7e-202">Process compensation</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="48e7e-203">Vergütungsprozess definieren und Ergebnisse berechnen</span><span class="sxs-lookup"><span data-stu-id="48e7e-203">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="48e7e-204">Einen Mitarbeiters in einem Plan für eine feste Vergütung registrieren</span><span class="sxs-lookup"><span data-stu-id="48e7e-204">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="48e7e-205">Einen Mitarbeiter in einem Plan für variable Vergütung registrieren</span><span class="sxs-lookup"><span data-stu-id="48e7e-205">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="48e7e-206">Stellentyp</span><span class="sxs-lookup"><span data-stu-id="48e7e-206">Jobs</span></span> 

<span data-ttu-id="48e7e-207">Eine Stelle ist eine Sammlung der Aufgaben und Zuständigkeiten, die für eine Person, die eine Tätigkeit ausführt, obligatorisch sind.</span><span class="sxs-lookup"><span data-stu-id="48e7e-207">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="48e7e-208">Weitere Informationen finden Sie in folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="48e7e-208">For more information, see the following topics:</span></span>

- [<span data-ttu-id="48e7e-209">Komponenten einer Stelle einrichten</span><span class="sxs-lookup"><span data-stu-id="48e7e-209">Setting up the components of a job</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="48e7e-210">Neue Einzelvorgänge definieren</span><span class="sxs-lookup"><span data-stu-id="48e7e-210">Define new jobs</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="48e7e-211">Positionen</span><span class="sxs-lookup"><span data-stu-id="48e7e-211">Positions</span></span>

<span data-ttu-id="48e7e-212">Eine Position ist eine einzelne Instanz eines Einzelvorgangs.</span><span class="sxs-lookup"><span data-stu-id="48e7e-212">A position is an individual instance of a job.</span></span> <span data-ttu-id="48e7e-213">Beispielsweise ist die Position „Verkaufsleiter (Ost)” eine der Positionen, die der Stelle „Verkaufsleiter” zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="48e7e-213">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="48e7e-214">Eine Position ist in einer Abteilung vorhanden.</span><span class="sxs-lookup"><span data-stu-id="48e7e-214">A position exists in a department.</span></span> <span data-ttu-id="48e7e-215">Nur jeweils eine Arbeitskraft kann jeder Position zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="48e7e-215">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="48e7e-216">Bedenken Sie die folgenden Daten und Konfigurationen, wenn Sie Positionen einrichten:</span><span class="sxs-lookup"><span data-stu-id="48e7e-216">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="48e7e-217">Position (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-217">Position (required)</span></span>
- <span data-ttu-id="48e7e-218">Beschreibung (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-218">Description (required)</span></span>
- <span data-ttu-id="48e7e-219">Stelle (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-219">Job (required)</span></span>
- <span data-ttu-id="48e7e-220">Abteilung (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-220">Department (required)</span></span>
- <span data-ttu-id="48e7e-221">Positionstyp (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-221">Position type (required)</span></span>
- <span data-ttu-id="48e7e-222">Vollzeitäquivalent</span><span class="sxs-lookup"><span data-stu-id="48e7e-222">Full-time equivalent</span></span>
- <span data-ttu-id="48e7e-223">Normale Stunden pro Jahr (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-223">Annual regular hours (required)</span></span>
- <span data-ttu-id="48e7e-224">Gezahlt von der juristischen Person (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-224">Paid by legal entity (required)</span></span>
- <span data-ttu-id="48e7e-225">Lohnzyklus (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-225">Pay cycle (required)</span></span>
- <span data-ttu-id="48e7e-226">Standardfinanzdimension – Kostenstelle (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-226">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="48e7e-227">Arbeitskraftzuweisung – Arbeitskraft, Zuweisungsanfang, Zuweisungsende, Ursachencode</span><span class="sxs-lookup"><span data-stu-id="48e7e-227">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="48e7e-228">Wenn mehrere Positionen in derselben Abteilung derselben Stelle zugeordnet sind, werden sie in einer einzelnen Position in Dayforce konsolidiert.</span><span class="sxs-lookup"><span data-stu-id="48e7e-228">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="48e7e-229">Weitere Informationen finden Sie in folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="48e7e-229">For more information, see the following topics:</span></span>

- [<span data-ttu-id="48e7e-230">Organisieren der Belegschaft anhand von Abteilungen, Stellen und Positionen</span><span class="sxs-lookup"><span data-stu-id="48e7e-230">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="48e7e-231">Positionen einrichten</span><span class="sxs-lookup"><span data-stu-id="48e7e-231">Set up positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="48e7e-232">Abteilungen</span><span class="sxs-lookup"><span data-stu-id="48e7e-232">Departments</span></span>

<span data-ttu-id="48e7e-233">Eine Abteilung ist eine Organisationseinheit, die eine Kategorie oder einen funktionalen Bereich einer Organisation darstellt.</span><span class="sxs-lookup"><span data-stu-id="48e7e-233">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="48e7e-234">Eine Abteilung ist für einen bestimmten Bereich der Organisation wie zum Beispiel Verkauf, Buchhaltung oder Personalverwaltung zuständig.</span><span class="sxs-lookup"><span data-stu-id="48e7e-234">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="48e7e-235">Sie können Abteilungen verwenden, um zu Funktionsbereiche zu melden.</span><span class="sxs-lookup"><span data-stu-id="48e7e-235">You can use departments to report on functional areas.</span></span> <span data-ttu-id="48e7e-236">Abteilungen können Gewinn- und Verlustzuständigkeit haben.</span><span class="sxs-lookup"><span data-stu-id="48e7e-236">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="48e7e-237">Weitere Informationen finden Sie in folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="48e7e-237">For more information, see the following topics:</span></span>

- [<span data-ttu-id="48e7e-238">Eine Abteilung erstellen und der Abteilungshierarchie zuordnen</span><span class="sxs-lookup"><span data-stu-id="48e7e-238">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="48e7e-239">Neue Abteilungen definieren</span><span class="sxs-lookup"><span data-stu-id="48e7e-239">Define new departments</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="48e7e-240">Lohnzyklen und Lohnperioden</span><span class="sxs-lookup"><span data-stu-id="48e7e-240">Pay cycles and pay periods</span></span>

<span data-ttu-id="48e7e-241">Ein Lohnzyklus bestimmt, wie oft Lohn ausgezahlt wird, sowie die spezifischen Tage, an denen Arbeitskräfte bezahlt werden.</span><span class="sxs-lookup"><span data-stu-id="48e7e-241">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="48e7e-242">Ein Lohnzyklus kann beispielsweise monatlich sein, und Mitarbeiter werden am letzten Tag des Monats bezahlt.</span><span class="sxs-lookup"><span data-stu-id="48e7e-242">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="48e7e-243">Alternativ könnte ein Lohnzyklus wöchentlich sein, und Mitarbeiter werden am Dienstag nach Ende der Lohnperiode bezahlt.</span><span class="sxs-lookup"><span data-stu-id="48e7e-243">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="48e7e-244">Lohnzyklen werden Positionen zugewiesen, um zu steuern, wann Mitarbeiter in diesen Positionen bezahlt werden.</span><span class="sxs-lookup"><span data-stu-id="48e7e-244">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="48e7e-245">Nachdem Sie Lohnzyklen erstellen, können Sie Lohnperioden für jeden Zyklus generieren.</span><span class="sxs-lookup"><span data-stu-id="48e7e-245">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="48e7e-246">Jede Lohnperiode enthält ein Standardzahlungsdatum, das auf den von Ihnen bereitgestellten Informationen basiert.</span><span class="sxs-lookup"><span data-stu-id="48e7e-246">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="48e7e-247">Allerdings können Sie das Standardzahlungsdatum in einer Lohnperiode ändern, um Ausnahmen zuzulassen, wie beispielsweise wenn das Zahlungsdatum auf einen Feiertag fällt.</span><span class="sxs-lookup"><span data-stu-id="48e7e-247">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="48e7e-248">Die folgenden Informationen werden in Dayforce verwendet:</span><span class="sxs-lookup"><span data-stu-id="48e7e-248">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="48e7e-249">Lohnzyklus (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-249">Pay cycle (required)</span></span>
- <span data-ttu-id="48e7e-250">Lohnzyklushäufigkeit (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-250">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="48e7e-251">Periodenstartdatum (erstes erforderliche Lohnperiode)</span><span class="sxs-lookup"><span data-stu-id="48e7e-251">Period start date (first pay period required)</span></span>
- <span data-ttu-id="48e7e-252">Standardzahlungsdatum (erste erforderliche Lohnperiode)</span><span class="sxs-lookup"><span data-stu-id="48e7e-252">Default payment date (first pay period required)</span></span>

<span data-ttu-id="48e7e-253">Diese Informationen werden mit Dayforce als Lohngruppen integriert und sind nach Land oder Region für jeden Lohnzyklus getrennt.</span><span class="sxs-lookup"><span data-stu-id="48e7e-253">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="48e7e-254">Es muss mindestens eine Lohnperiode vor der Integration generiert werden.</span><span class="sxs-lookup"><span data-stu-id="48e7e-254">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="48e7e-255">Dayforce generiert Lohngruppenkalender und Zahlungsdaten basierend auf dem Anfangsdatum der ersten Lohnperiode und dem Standardzahlungsdatums, das in Talent eingerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="48e7e-255">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Talent.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="48e7e-256">Einkommenscodes</span><span class="sxs-lookup"><span data-stu-id="48e7e-256">Earning codes</span></span>

<span data-ttu-id="48e7e-257">Einkommenscodes bestimmen jeden Typ von Einkünften eindeutig, die Arbeitskräfte erhalten</span><span class="sxs-lookup"><span data-stu-id="48e7e-257">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="48e7e-258">Die Codes haben verschiedene Parameter, die sich auf Einkünfte beziehen, wie beispielsweise Buchhaltungsvorschriften, Steuergesetze, Berichterstellungsanforderungen und Bruttoausgleichsfähigkeit.</span><span class="sxs-lookup"><span data-stu-id="48e7e-258">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="48e7e-259">Die folgenden Informationen werden in Dayforce verwendet:</span><span class="sxs-lookup"><span data-stu-id="48e7e-259">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="48e7e-260">Einkommenscode (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-260">Earning Code (required)</span></span>
- <span data-ttu-id="48e7e-261">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="48e7e-261">Description</span></span>
- <span data-ttu-id="48e7e-262">Maßeinheit</span><span class="sxs-lookup"><span data-stu-id="48e7e-262">Unit of measure</span></span>
- <span data-ttu-id="48e7e-263">Produktiv</span><span class="sxs-lookup"><span data-stu-id="48e7e-263">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="48e7e-264">Arbeitskraftdaten</span><span class="sxs-lookup"><span data-stu-id="48e7e-264">Worker data</span></span>

<span data-ttu-id="48e7e-265">Datensätze für die verschiedenen Arten von Arbeitskräften, die Sie haben, sind für Ihre Personalverwaltung- sowie für Ihre Lohnsysteme von Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="48e7e-265">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="48e7e-266">Anhand der eingegebenen Informationen lassen sich Arbeitskräfte sowie personenbezogene Informationen nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="48e7e-266">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="48e7e-267">Sie können die folgenden Informationen für Arbeitskräfte verwalten:</span><span class="sxs-lookup"><span data-stu-id="48e7e-267">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="48e7e-268">**Basis** – Verwalten grundlegender Informationen über eine Arbeitskraft, beispielsweise Kontaktinformationen, demografische Informationen, Kennungsinformationen, Familieninformationen, Militärdienststatus, Ausländerinformationen sowie personenbezogene und Notfallkontakte.</span><span class="sxs-lookup"><span data-stu-id="48e7e-268">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="48e7e-269">**Beschäftigung** – Verwalten von Informationen zum Beschäftigungsverhältnis einer Arbeitskraft, wie Unternehmens- oder Organisationszugehörigkeit, Positionszuweisung, Start- und Enddatum, Arbeitsberechtigung, Beschäftigungsbedingungen, Rente, Urlaub und Versetzungen.</span><span class="sxs-lookup"><span data-stu-id="48e7e-269">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="48e7e-270">**Urlaub und Abwesenheit** – Verwalten von Informationen zur Abwesenheit einer Arbeitskraft, beispielsweise Arbeitszeitkalender, Abwesenheitsbuchungen und Abwesenheitseinrichtung.</span><span class="sxs-lookup"><span data-stu-id="48e7e-270">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="48e7e-271">**Vergütung und Lohn** – Verwalten von Informationen zu den Vergütungsplänen und Lohndaten einer Arbeitskraft, wie der Planregistrierung, Boni, Leistung, Provision, Steuerdaten, Pensionierung und Gehaltsabzüge.</span><span class="sxs-lookup"><span data-stu-id="48e7e-271">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="48e7e-272">Wenn Sie Arbeitskraftinformationen eingeben, sollten Sie folgende Daten und Konfigurationen bedenken, die in Dayforce verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="48e7e-272">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="48e7e-273">Allgemeine Angaben</span><span class="sxs-lookup"><span data-stu-id="48e7e-273">General information</span></span>

- <span data-ttu-id="48e7e-274">Personalnummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-274">Personnel number (required)</span></span>
- <span data-ttu-id="48e7e-275">Vorname (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-275">First name (required)</span></span>
- <span data-ttu-id="48e7e-276">Nachname (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-276">Last name (required)</span></span>
- <span data-ttu-id="48e7e-277">Zweiter Vorname</span><span class="sxs-lookup"><span data-stu-id="48e7e-277">Middle name</span></span>
- <span data-ttu-id="48e7e-278">Dienstalterdatum</span><span class="sxs-lookup"><span data-stu-id="48e7e-278">Seniority date</span></span>
- <span data-ttu-id="48e7e-279">Bekannt als</span><span class="sxs-lookup"><span data-stu-id="48e7e-279">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="48e7e-280">Personenbezogene Informationen</span><span class="sxs-lookup"><span data-stu-id="48e7e-280">Personal information</span></span>

- <span data-ttu-id="48e7e-281">Familienstand (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-281">Marital status (required)</span></span>
- <span data-ttu-id="48e7e-282">Geburtsdatum (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-282">Birth date (required)</span></span>
- <span data-ttu-id="48e7e-283">Geschlecht (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-283">Gender (required)</span></span>
- <span data-ttu-id="48e7e-284">Person mit Behinderung</span><span class="sxs-lookup"><span data-stu-id="48e7e-284">Person with disabilities</span></span>
- <span data-ttu-id="48e7e-285">Nationalitätsland/-region (nur für Mexiko)</span><span class="sxs-lookup"><span data-stu-id="48e7e-285">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="48e7e-286">Adressdaten</span><span class="sxs-lookup"><span data-stu-id="48e7e-286">Address information</span></span>

- <span data-ttu-id="48e7e-287">Primär (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-287">Primary (required)</span></span>
- <span data-ttu-id="48e7e-288">Land/Region (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-288">Country/region (required)</span></span>
- <span data-ttu-id="48e7e-289">Postleitzahl (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-289">Postal code (required)</span></span>
- <span data-ttu-id="48e7e-290">Hausnummer (erforderlich) (nur für Mexiko)</span><span class="sxs-lookup"><span data-stu-id="48e7e-290">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="48e7e-291">Gebäudeergänzung (nur für Mexiko)</span><span class="sxs-lookup"><span data-stu-id="48e7e-291">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="48e7e-292">Ort (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-292">City (required)</span></span>
- <span data-ttu-id="48e7e-293">Bundesland/Kanton (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-293">State (required)</span></span>
- <span data-ttu-id="48e7e-294">Landkreis (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-294">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="48e7e-295">Kontaktdaten</span><span class="sxs-lookup"><span data-stu-id="48e7e-295">Contact information</span></span> 

- <span data-ttu-id="48e7e-296">Primär (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-296">Primary (required)</span></span>
- <span data-ttu-id="48e7e-297">Kontaktnummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-297">Contact number (required)</span></span>
- <span data-ttu-id="48e7e-298">Durchwahl</span><span class="sxs-lookup"><span data-stu-id="48e7e-298">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="48e7e-299">Lohndaten und Einkommenscodes</span><span class="sxs-lookup"><span data-stu-id="48e7e-299">Payroll information and earning codes</span></span>

<span data-ttu-id="48e7e-300">Mitarbeitern müssen bestimmte Einkommen mit einer bestimmten Zahlungshäufigkeit zugewiesen werden und sie müssen eine bevorzugte Zahlungsmethode haben.</span><span class="sxs-lookup"><span data-stu-id="48e7e-300">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="48e7e-301">Die folgenden Felder werden in Dayforce verwendet, um zu gewährleisten, dass diese Voreinstellungen und Einstellungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="48e7e-301">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="48e7e-302">Einkommenscodes</span><span class="sxs-lookup"><span data-stu-id="48e7e-302">Earning codes</span></span>

- <span data-ttu-id="48e7e-303">Position (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-303">Position (required)</span></span>
- <span data-ttu-id="48e7e-304">Einkommenscode (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-304">Earning Code (required)</span></span>
- <span data-ttu-id="48e7e-305">Häufigkeit (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-305">Frequency (required)</span></span>
- <span data-ttu-id="48e7e-306">Betrag (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-306">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="48e7e-307">Lohndaten</span><span class="sxs-lookup"><span data-stu-id="48e7e-307">Payroll information</span></span>

- <span data-ttu-id="48e7e-308">Zahlungsmethode</span><span class="sxs-lookup"><span data-stu-id="48e7e-308">Payment Method</span></span>
- <span data-ttu-id="48e7e-309">Wirtschaftliche Region (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-309">Economic Region (required)</span></span>
- <span data-ttu-id="48e7e-310">Mitarbeitervergütungs-ID</span><span class="sxs-lookup"><span data-stu-id="48e7e-310">Employee Benefits ID</span></span>
- <span data-ttu-id="48e7e-311">Personalausweisnummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-311">National ID Number (required)</span></span>
- <span data-ttu-id="48e7e-312">Militärdienstnummer</span><span class="sxs-lookup"><span data-stu-id="48e7e-312">Military Service Number</span></span>
- <span data-ttu-id="48e7e-313">Schichtkennung (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-313">Shift ID (required)</span></span>
- <span data-ttu-id="48e7e-314">Steuernummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-314">Tax Number (required)</span></span>
- <span data-ttu-id="48e7e-315">Gewerkschaftskennung (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-315">Union ID (required)</span></span>
- <span data-ttu-id="48e7e-316">Arbeitstagkennung (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-316">Work Day ID (required)</span></span>
- <span data-ttu-id="48e7e-317">Arbeitserlaubnisnummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-317">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="48e7e-318">Für die Zahlungsmethode unterstützt Mexiko **Bargeld**, **Scheck** (der physische Scheck des Unternehmens) und **Elektronische Zahlung**.</span><span class="sxs-lookup"><span data-stu-id="48e7e-318">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="48e7e-319">Wenn keine Zahlungsmethode angegeben wird, wird **Scheck** standardmäßig verwendet.</span><span class="sxs-lookup"><span data-stu-id="48e7e-319">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="48e7e-320">Anstellungsdetails</span><span class="sxs-lookup"><span data-stu-id="48e7e-320">Employment details</span></span>

<span data-ttu-id="48e7e-321">Beschäftigungsdetailhistorie wird als Schlüsselinformation verwendet, um die Status für Einstellung, Kündigung und erneute Einstellung in Dayforce abzuleiten.</span><span class="sxs-lookup"><span data-stu-id="48e7e-321">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="48e7e-322">Dayforce unterstützt nur einen aktiven Beschäftigungsdatensatz gleichzeitig.</span><span class="sxs-lookup"><span data-stu-id="48e7e-322">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="48e7e-323">Datum des Beschäftigungsbeginns (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-323">Employment start date (required)</span></span>
- <span data-ttu-id="48e7e-324">Datum des Beschäftigungsendes</span><span class="sxs-lookup"><span data-stu-id="48e7e-324">Employment end date</span></span>
- <span data-ttu-id="48e7e-325">Eintrittstermin</span><span class="sxs-lookup"><span data-stu-id="48e7e-325">Start date</span></span>
- <span data-ttu-id="48e7e-326">Angepasster Tätigkeitsbeginn</span><span class="sxs-lookup"><span data-stu-id="48e7e-326">Adjusted start date</span></span>
- <span data-ttu-id="48e7e-327">Kündigungsdatum (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-327">Termination date (required upon termination)</span></span>
- <span data-ttu-id="48e7e-328">Kündigungsgrund (erforderlich bei Kündigung)</span><span class="sxs-lookup"><span data-stu-id="48e7e-328">Termination reason (required upon termination)</span></span>

<span data-ttu-id="48e7e-329">Die Schlüsseldaten eines Mitarbeiters werden abgeleitet, indem die folgenden Informationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="48e7e-329">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="48e7e-330">Talent</span><span class="sxs-lookup"><span data-stu-id="48e7e-330">Talent</span></span>                | <span data-ttu-id="48e7e-331">Dayforce</span><span class="sxs-lookup"><span data-stu-id="48e7e-331">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48e7e-332">Aktuellstes Einstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="48e7e-332">Most recent hire date</span></span> | <span data-ttu-id="48e7e-333">Beschäftigungsbeginn des Verlaufsdatensatzes zur aktuellen, nicht gekündigten Beschäftigung</span><span class="sxs-lookup"><span data-stu-id="48e7e-333">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="48e7e-334">Kündigungsdatum</span><span class="sxs-lookup"><span data-stu-id="48e7e-334">Termination date</span></span>      | <span data-ttu-id="48e7e-335">Kündigungsdatum des Verlaufsdatensatzes zur aktuellen, nicht gekündigten Beschäftigung</span><span class="sxs-lookup"><span data-stu-id="48e7e-335">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="48e7e-336">Eintrittstermin</span><span class="sxs-lookup"><span data-stu-id="48e7e-336">Start date</span></span>            | <span data-ttu-id="48e7e-337">Angepasstes Startdatum, Startdatum oder Beschäftigungsbeginn des Verlaufsdatensatzes zur aktuellen, nicht aktiven Beschäftigung</span><span class="sxs-lookup"><span data-stu-id="48e7e-337">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="48e7e-338">Ursprüngliches Einstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="48e7e-338">Original hire date</span></span>    | <span data-ttu-id="48e7e-339">Beschäftigungsbeginn des frühesten Beschäftigungsverlaufsdatensatzes</span><span class="sxs-lookup"><span data-stu-id="48e7e-339">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="48e7e-340">Vergütung</span><span class="sxs-lookup"><span data-stu-id="48e7e-340">Compensation</span></span>

<span data-ttu-id="48e7e-341">Ein fester Vergütungsplan muss der primären Position jedes Mitarbeiters während einer Beschäftigungsperiode zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="48e7e-341">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="48e7e-342">Diese Periode beginnt mit dem Datum, an dem der Mitarbeiter eingestellt wurde (oder dem Datum des Beschäftigungsbeginns), und setzt sich bis zur Kündigung fort.</span><span class="sxs-lookup"><span data-stu-id="48e7e-342">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="48e7e-343">Gültigkeitsdatum (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-343">Effective Date (required)</span></span>
- <span data-ttu-id="48e7e-344">Ablaufdatum</span><span class="sxs-lookup"><span data-stu-id="48e7e-344">Expiration date</span></span>
- <span data-ttu-id="48e7e-345">Lohnsatz (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-345">Pay Rate (required)</span></span>
- <span data-ttu-id="48e7e-346">Lohnsatzkonvertierungen (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-346">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="48e7e-347">Jährliches Äquivalent (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-347">Annual equivalent (required)</span></span>
- <span data-ttu-id="48e7e-348">Stündliches Äquivalent (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-348">Hourly equivalent (required)</span></span>

<span data-ttu-id="48e7e-349">Wenn ein Mitarbeiter auf Stundenbasis mehrere Positionen hat, wird die feste Vergütung der primären Position in Dayforce als Basissatz/-gehalt auf Mitarbeiterebene importiert.</span><span class="sxs-lookup"><span data-stu-id="48e7e-349">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="48e7e-350">Für nicht-primäre Positionen wird der Stundensatz in der entsprechenden Position in Dayforce gespeichert.</span><span class="sxs-lookup"><span data-stu-id="48e7e-350">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="48e7e-351">Wenn ein Gehalt beziehender Mitarbeiter mehrere Positionen hat, wird der kumulative Stundensatz und das Jahresgehalt über alle aktiven Positionen hinweg abgeleitet und als Basissatz/-gehalt auf Arbeitnehmerebene verwendet.</span><span class="sxs-lookup"><span data-stu-id="48e7e-351">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="48e7e-352">Kennnummern</span><span class="sxs-lookup"><span data-stu-id="48e7e-352">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="48e7e-353">Sozialversicherungsbezeichner</span><span class="sxs-lookup"><span data-stu-id="48e7e-353">Social Security identifier</span></span> 

<span data-ttu-id="48e7e-354">Jeder Mitarbeiter muss einen primären Bezeichner haben.</span><span class="sxs-lookup"><span data-stu-id="48e7e-354">Every employee must have one primary identifier.</span></span> <span data-ttu-id="48e7e-355">Dieser Bezeichner muss vom Kennungstyp **P.Reg.Nr.** sein.</span><span class="sxs-lookup"><span data-stu-id="48e7e-355">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="48e7e-356">In Dayforce wird er automatisch als Sozialversicherungsbezeichner des Mitarbeiters abgeleitet, der für die Einstellung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="48e7e-356">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="48e7e-357">Primär (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-357">Primary (required)</span></span>
- <span data-ttu-id="48e7e-358">Kennungstyp = „P.Reg.Nr.”</span><span class="sxs-lookup"><span data-stu-id="48e7e-358">Identification Type = "SSN"</span></span>
- <span data-ttu-id="48e7e-359">Ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="48e7e-359">Issued Date</span></span>
- <span data-ttu-id="48e7e-360">Ablaufdatum</span><span class="sxs-lookup"><span data-stu-id="48e7e-360">Expiration Date</span></span>

<span data-ttu-id="48e7e-361">Mitarbeiter können mehrere Kennungsnummern des Kennungstyps **P.Reg.Nr.** melden.</span><span class="sxs-lookup"><span data-stu-id="48e7e-361">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="48e7e-362">Jedoch wird nur der Datensatz, der als **Primär** markiert ist, in Dayforce integriert, unabhängig davon, ob die Nummer aktiv oder abgelaufen ist.</span><span class="sxs-lookup"><span data-stu-id="48e7e-362">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="48e7e-363">Bankkonten und Auszahlungen</span><span class="sxs-lookup"><span data-stu-id="48e7e-363">Bank accounts and disbursements</span></span>

<span data-ttu-id="48e7e-364">Gültige Bankkontoinformationen müssen für jeden Mitarbeiter eingegeben werden, der per Bankkontoüberweisungen bezahlt werden möchte.</span><span class="sxs-lookup"><span data-stu-id="48e7e-364">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="48e7e-365">Talent</span><span class="sxs-lookup"><span data-stu-id="48e7e-365">Talent</span></span>                         | <span data-ttu-id="48e7e-366">Dayforce</span><span class="sxs-lookup"><span data-stu-id="48e7e-366">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48e7e-367">Bankkontonummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-367">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="48e7e-368">SWIFT-Code (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-368">SWIFT code (required)</span></span>          | <span data-ttu-id="48e7e-369">Feld **Bankkennung** wird verwendet, wenn Lohn in Mexiko verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="48e7e-369">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="48e7e-370">Filialnummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-370">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="48e7e-371">Bankkontotyp (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-371">Bank account type (required)</span></span>   | <span data-ttu-id="48e7e-372">Feld **Kontotyp** wird verwendet, wenn Lohn in Mexiko verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="48e7e-372">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="48e7e-373">Unterstützte Werte umfassen **Wird geprüft** und **Lohn**.</span><span class="sxs-lookup"><span data-stu-id="48e7e-373">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="48e7e-374">Mitarbeiter, die per Bankkontoüberweisungen bezahlt werden möchten, müssen eine Verknüpfung zu einem Restbetrags-Bankkonto angeben, das sich unter einer juristischen Person befindet, deren primäre Adresse in Mexiko ist und das einem gültigen Bankkonto von einer mexikanischen Bank zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="48e7e-374">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="48e7e-375">Alle anderen Nicht-Restbetrags-Bankkonten werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="48e7e-375">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="48e7e-376">Adressdaten</span><span class="sxs-lookup"><span data-stu-id="48e7e-376">Address information</span></span>

<span data-ttu-id="48e7e-377">Jeder Mitarbeiter muss einen primären Standort haben.</span><span class="sxs-lookup"><span data-stu-id="48e7e-377">Every employee must have one primary location.</span></span> <span data-ttu-id="48e7e-378">In Dayforce wird dieser Standort verwendet, um den primären Wohnsitz des Mitarbeiters für Steuerzwecke zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="48e7e-378">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="48e7e-379">Primär (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-379">Primary (required)</span></span>
- <span data-ttu-id="48e7e-380">Land/Region (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-380">Country/region (required)</span></span>
- <span data-ttu-id="48e7e-381">Postleitzahl (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-381">Zip/postal code (required)</span></span>
- <span data-ttu-id="48e7e-382">Straße (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-382">Street (required)</span></span>
- <span data-ttu-id="48e7e-383">Hausnummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-383">Street Number (required)</span></span>
- <span data-ttu-id="48e7e-384">Gebäudeergänzung</span><span class="sxs-lookup"><span data-stu-id="48e7e-384">Building Complement</span></span>
- <span data-ttu-id="48e7e-385">Ort (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-385">City (required)</span></span>
- <span data-ttu-id="48e7e-386">Bundesland/Kanton (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-386">State (required)</span></span>
- <span data-ttu-id="48e7e-387">Landkreis (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-387">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="48e7e-388">Konfigurieren Ihrer Daten, um Vergütung in den USA und Kanada zu generieren</span><span class="sxs-lookup"><span data-stu-id="48e7e-388">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="48e7e-389">Wenn Sie Vergütung für Mitarbeiter in den USA und Kanada generieren, müssen die folgenden Elemente konfiguriert werden:</span><span class="sxs-lookup"><span data-stu-id="48e7e-389">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="48e7e-390">Abteilungen sind für Positionen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="48e7e-390">Departments are required on positions.</span></span>
- <span data-ttu-id="48e7e-391">Kostenstellen müssen als Finanzdimensionen festgelegt werden und müssen das erste Element in der standardmäßigen Finanzdimensions-Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="48e7e-391">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="48e7e-392">Sie können Talent so konfigurieren, dass es anfordert, dass Positionen eine Abteilung angegeben.</span><span class="sxs-lookup"><span data-stu-id="48e7e-392">You can configure Talent to require that Positions specify a Department.</span></span> <span data-ttu-id="48e7e-393">Dazu wechseln Sie zu **Freigegebene Positionen der Personalverwaltung > Positionen > Abteilungen zu Positionen anfordern**.</span><span class="sxs-lookup"><span data-stu-id="48e7e-393">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="48e7e-394">Es wird empfohlen, dass diese Einstellungen für die Integration erzwungen wird.</span><span class="sxs-lookup"><span data-stu-id="48e7e-394">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="48e7e-395">Stellentypen</span><span class="sxs-lookup"><span data-stu-id="48e7e-395">Job types</span></span>

<span data-ttu-id="48e7e-396">Stellentypen werden verwendet, um ähnliche Stellen in Kategorien zu gruppieren.</span><span class="sxs-lookup"><span data-stu-id="48e7e-396">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="48e7e-397">Stellentypen sind erforderlich, damit Lohn in den USA und Kanada zu bearbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="48e7e-397">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="48e7e-398">Beispiele für Stellentypen umfassen Voll- und Teilzeit oder festes Gehalt und Stundenlohn.</span><span class="sxs-lookup"><span data-stu-id="48e7e-398">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="48e7e-399">Stellentypen werden Dayforce als Lohnarten zugeordnet, die angeben, ob ein Mitarbeiter auf Stundenbasis bezahlt wird oder ein festes Gehalt bezieht.</span><span class="sxs-lookup"><span data-stu-id="48e7e-399">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="48e7e-400">Folgende Stellentypen und Beschreibungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="48e7e-400">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="48e7e-401">Stellentyp</span><span class="sxs-lookup"><span data-stu-id="48e7e-401">Job type</span></span>   | <span data-ttu-id="48e7e-402">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="48e7e-402">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="48e7e-403">Stündlich</span><span class="sxs-lookup"><span data-stu-id="48e7e-403">Hourly</span></span>     | <span data-ttu-id="48e7e-404">Stündlich</span><span class="sxs-lookup"><span data-stu-id="48e7e-404">Hourly</span></span>      |
| <span data-ttu-id="48e7e-405">Fest angestellt</span><span class="sxs-lookup"><span data-stu-id="48e7e-405">Salaried</span></span>   | <span data-ttu-id="48e7e-406">Fest angestellt</span><span class="sxs-lookup"><span data-stu-id="48e7e-406">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="48e7e-407">Positionstypen</span><span class="sxs-lookup"><span data-stu-id="48e7e-407">Position types</span></span> 

<span data-ttu-id="48e7e-408">Sie verwenden Positionstypen, um zu beschreiben, ob die Position Vollzeit, Teilzeit oder etwas anderes ist.</span><span class="sxs-lookup"><span data-stu-id="48e7e-408">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="48e7e-409">Positionstypen werden Dayforce als Lohnklassen zugeordnet, die angeben, ob ein Mitarbeiter in Vollzeit oder Teilzeit arbeitet.</span><span class="sxs-lookup"><span data-stu-id="48e7e-409">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="48e7e-410">Folgende Positionstypen und Beschreibungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="48e7e-410">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="48e7e-411">Positionstyp</span><span class="sxs-lookup"><span data-stu-id="48e7e-411">Position type</span></span>   | <span data-ttu-id="48e7e-412">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="48e7e-412">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="48e7e-413">Vollzeit</span><span class="sxs-lookup"><span data-stu-id="48e7e-413">Full-time</span></span>       | <span data-ttu-id="48e7e-414">Vollzeitmitarbeiter</span><span class="sxs-lookup"><span data-stu-id="48e7e-414">Full time employee</span></span> |
| <span data-ttu-id="48e7e-415">Teilzeit</span><span class="sxs-lookup"><span data-stu-id="48e7e-415">Part-time</span></span>       | <span data-ttu-id="48e7e-416">Teilzeitmitarbeiter</span><span class="sxs-lookup"><span data-stu-id="48e7e-416">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="48e7e-417">Ursachencodes</span><span class="sxs-lookup"><span data-stu-id="48e7e-417">Reason codes</span></span>

<span data-ttu-id="48e7e-418">Ursachencodes enthalten Informationen zum Status eines Mitarbeiters.</span><span class="sxs-lookup"><span data-stu-id="48e7e-418">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="48e7e-419">Ursachencodes werden Dayforce als Statusgründe zugeordnet, die den Grund für Änderungen bei der Position eines Mitarbeiters oder dem Beschäftigungsstatus angeben.</span><span class="sxs-lookup"><span data-stu-id="48e7e-419">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="48e7e-420">Folgende Ursachencodes und Beschreibungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="48e7e-420">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="48e7e-421">Ursachencode</span><span class="sxs-lookup"><span data-stu-id="48e7e-421">Reason code</span></span>    | <span data-ttu-id="48e7e-422">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="48e7e-422">Description</span></span>      | <span data-ttu-id="48e7e-423">Zutreffende Szenarios</span><span class="sxs-lookup"><span data-stu-id="48e7e-423">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="48e7e-424">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="48e7e-424">RESIGNATION</span></span>    | <span data-ttu-id="48e7e-425">Kündigung durch Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="48e7e-425">Resignation</span></span>      | <span data-ttu-id="48e7e-426">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="48e7e-426">Terminate worker</span></span>     |
| <span data-ttu-id="48e7e-427">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="48e7e-427">TERMINATION</span></span>    | <span data-ttu-id="48e7e-428">Beendigung</span><span class="sxs-lookup"><span data-stu-id="48e7e-428">Termination</span></span>      | <span data-ttu-id="48e7e-429">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="48e7e-429">Terminate worker</span></span>     |
| <span data-ttu-id="48e7e-430">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="48e7e-430">RETIREMENT</span></span>     | <span data-ttu-id="48e7e-431">Ruhestand</span><span class="sxs-lookup"><span data-stu-id="48e7e-431">Retirement</span></span>       | <span data-ttu-id="48e7e-432">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="48e7e-432">Terminate worker</span></span>     |
| <span data-ttu-id="48e7e-433">OTHER</span><span class="sxs-lookup"><span data-stu-id="48e7e-433">OTHER</span></span>          | <span data-ttu-id="48e7e-434">Andere Gründe</span><span class="sxs-lookup"><span data-stu-id="48e7e-434">Other Reasons</span></span>    | <span data-ttu-id="48e7e-435">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="48e7e-435">Terminate worker</span></span>     |
| <span data-ttu-id="48e7e-436">DEATH</span><span class="sxs-lookup"><span data-stu-id="48e7e-436">DEATH</span></span>          | <span data-ttu-id="48e7e-437">Tod</span><span class="sxs-lookup"><span data-stu-id="48e7e-437">Death</span></span>            | <span data-ttu-id="48e7e-438">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="48e7e-438">Terminate worker</span></span>     |
| <span data-ttu-id="48e7e-439">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="48e7e-439">LEAVEOFABSENCE</span></span> | <span data-ttu-id="48e7e-440">Beurlaubung</span><span class="sxs-lookup"><span data-stu-id="48e7e-440">Leave of Absence</span></span> | <span data-ttu-id="48e7e-441">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="48e7e-441">Terminate worker</span></span>     |
| <span data-ttu-id="48e7e-442">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="48e7e-442">CONTRACTEND</span></span>    | <span data-ttu-id="48e7e-443">Vertragsende</span><span class="sxs-lookup"><span data-stu-id="48e7e-443">End of Contract</span></span>  | <span data-ttu-id="48e7e-444">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="48e7e-444">Terminate worker</span></span>     |
| <span data-ttu-id="48e7e-445">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="48e7e-445">SALARYCHANGE</span></span>   | <span data-ttu-id="48e7e-446">Gehaltsänderung</span><span class="sxs-lookup"><span data-stu-id="48e7e-446">Change of Salary</span></span> | <span data-ttu-id="48e7e-447">Vergütung</span><span class="sxs-lookup"><span data-stu-id="48e7e-447">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="48e7e-448">Familienstand</span><span class="sxs-lookup"><span data-stu-id="48e7e-448">Marital status</span></span>

<span data-ttu-id="48e7e-449">Familienstandwerte werden Dayforce zugeordnet und werden – je nach Bedarf – in die akzeptierten Werte bei der Integration übersetzt.</span><span class="sxs-lookup"><span data-stu-id="48e7e-449">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="48e7e-450">Die folgende Tabelle zeigt, wie Familienstandwerte Dayforce zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="48e7e-450">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="48e7e-451">Talent</span><span class="sxs-lookup"><span data-stu-id="48e7e-451">Talent</span></span>                 | <span data-ttu-id="48e7e-452">Dayforce</span><span class="sxs-lookup"><span data-stu-id="48e7e-452">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="48e7e-453">Verheiratet</span><span class="sxs-lookup"><span data-stu-id="48e7e-453">Married</span></span>                | <span data-ttu-id="48e7e-454">Verheiratet</span><span class="sxs-lookup"><span data-stu-id="48e7e-454">Married</span></span>              |
| <span data-ttu-id="48e7e-455">Ledig</span><span class="sxs-lookup"><span data-stu-id="48e7e-455">Single</span></span>                 | <span data-ttu-id="48e7e-456">Ledig</span><span class="sxs-lookup"><span data-stu-id="48e7e-456">Single</span></span>               |
| <span data-ttu-id="48e7e-457">Verwitwet</span><span class="sxs-lookup"><span data-stu-id="48e7e-457">Widowed</span></span>                | <span data-ttu-id="48e7e-458">Verwitwet</span><span class="sxs-lookup"><span data-stu-id="48e7e-458">Widowed</span></span>              |
| <span data-ttu-id="48e7e-459">Geschieden</span><span class="sxs-lookup"><span data-stu-id="48e7e-459">Divorced</span></span>               | <span data-ttu-id="48e7e-460">Geschieden</span><span class="sxs-lookup"><span data-stu-id="48e7e-460">Divorced</span></span>             |
| <span data-ttu-id="48e7e-461">Eingetragene Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="48e7e-461">Registered Partnership</span></span> | <span data-ttu-id="48e7e-462">Inländische Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="48e7e-462">Domestic Partnership</span></span> |
| <span data-ttu-id="48e7e-463">None</span><span class="sxs-lookup"><span data-stu-id="48e7e-463">None</span></span>                   | <span data-ttu-id="48e7e-464">None</span><span class="sxs-lookup"><span data-stu-id="48e7e-464">None</span></span>                 |
| <span data-ttu-id="48e7e-465">Freie Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="48e7e-465">Cohabiting</span></span>             | <span data-ttu-id="48e7e-466">Freie Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="48e7e-466">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="48e7e-467">Geschlecht</span><span class="sxs-lookup"><span data-stu-id="48e7e-467">Gender</span></span>

<span data-ttu-id="48e7e-468">Geschlechtsbezeichnungen werden Dayforce zugeordnet und werden – je nach Bedarf – in die akzeptierten Werte bei der Integration übersetzt.</span><span class="sxs-lookup"><span data-stu-id="48e7e-468">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="48e7e-469">Die folgende Tabelle zeigt, wie Geschlechtsbezeichnungen Dayforce zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="48e7e-469">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="48e7e-470">Talent</span><span class="sxs-lookup"><span data-stu-id="48e7e-470">Talent</span></span>       | <span data-ttu-id="48e7e-471">Dayforce</span><span class="sxs-lookup"><span data-stu-id="48e7e-471">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="48e7e-472">Männlich</span><span class="sxs-lookup"><span data-stu-id="48e7e-472">Male</span></span>         | <span data-ttu-id="48e7e-473">Männlich</span><span class="sxs-lookup"><span data-stu-id="48e7e-473">Male</span></span>            |
| <span data-ttu-id="48e7e-474">Weiblich</span><span class="sxs-lookup"><span data-stu-id="48e7e-474">Female</span></span>       | <span data-ttu-id="48e7e-475">Weiblich</span><span class="sxs-lookup"><span data-stu-id="48e7e-475">Female</span></span>          |
| <span data-ttu-id="48e7e-476">Nicht spezifisch</span><span class="sxs-lookup"><span data-stu-id="48e7e-476">Non-specific</span></span> | <span data-ttu-id="48e7e-477">*Nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="48e7e-477">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="48e7e-478">Einkommenscodes</span><span class="sxs-lookup"><span data-stu-id="48e7e-478">Earning codes</span></span>

<span data-ttu-id="48e7e-479">Einkommenscodes bestimmen jeden Typ von Einkünften eindeutig, die Arbeitskräfte erhalten</span><span class="sxs-lookup"><span data-stu-id="48e7e-479">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="48e7e-480">Die Codes decken verschiedene Parameter ab, die sich auf Einkünfte beziehen, wie beispielsweise Buchhaltungsvorschriften, Steuergesetze, Berichterstellungsanforderungen und Bruttoausgleichsfähigkeit.</span><span class="sxs-lookup"><span data-stu-id="48e7e-480">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="48e7e-481">Wenn eine nicht unterstützte Häufigkeit verwendet wird, wird die Häufigkeit **Jeder Lohn** standardmäßig für die Berechnung verwendet.</span><span class="sxs-lookup"><span data-stu-id="48e7e-481">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="48e7e-482">Unterstützte Häufigkeiten</span><span class="sxs-lookup"><span data-stu-id="48e7e-482">Supported frequencies</span></span>

- <span data-ttu-id="48e7e-483">Alle</span><span class="sxs-lookup"><span data-stu-id="48e7e-483">All</span></span>
- <span data-ttu-id="48e7e-484">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="48e7e-484">EVERYPAY</span></span>
- <span data-ttu-id="48e7e-485">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="48e7e-485">EACHPAYPERIOD</span></span>
- <span data-ttu-id="48e7e-486">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="48e7e-486">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="48e7e-487">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="48e7e-487">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="48e7e-488">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="48e7e-488">1OFMTH</span></span>
- <span data-ttu-id="48e7e-489">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="48e7e-489">LASTOFMTH</span></span>
- <span data-ttu-id="48e7e-490">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="48e7e-490">2OFMTH</span></span>
- <span data-ttu-id="48e7e-491">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="48e7e-491">3OFMTH</span></span>
- <span data-ttu-id="48e7e-492">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="48e7e-492">4OFMTH</span></span>
- <span data-ttu-id="48e7e-493">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="48e7e-493">5OFMTH</span></span>
- <span data-ttu-id="48e7e-494">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="48e7e-494">1N2OFMTH</span></span>
- <span data-ttu-id="48e7e-495">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="48e7e-495">3N4OFMTH</span></span>
- <span data-ttu-id="48e7e-496">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="48e7e-496">1N3OFMTH</span></span>
- <span data-ttu-id="48e7e-497">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="48e7e-497">1N4OFMTH</span></span>
- <span data-ttu-id="48e7e-498">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="48e7e-498">2N3OFMTH</span></span>
- <span data-ttu-id="48e7e-499">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="48e7e-499">2N4OFMTH</span></span>
- <span data-ttu-id="48e7e-500">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="48e7e-500">1N2N3OFMTH</span></span>
- <span data-ttu-id="48e7e-501">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="48e7e-501">1N2N4OFMTH</span></span>
- <span data-ttu-id="48e7e-502">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="48e7e-502">1N3N4OFMTH</span></span>
- <span data-ttu-id="48e7e-503">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="48e7e-503">2N3N4OFMTH</span></span>
- <span data-ttu-id="48e7e-504">1N2N3N4OFMTH – 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="48e7e-504">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="48e7e-505">2N3N4N5OFMth – 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="48e7e-505">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="48e7e-506">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="48e7e-506">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="48e7e-507">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="48e7e-507">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="48e7e-508">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="48e7e-508">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="48e7e-509">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="48e7e-509">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="48e7e-510">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="48e7e-510">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="48e7e-511">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="48e7e-511">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="48e7e-512">Adressen</span><span class="sxs-lookup"><span data-stu-id="48e7e-512">Addresses</span></span>

<span data-ttu-id="48e7e-513">Die Kennung bestimmter Codes für Land oder Region, Bundesland/Kanton oder Landkreis (Gemeinde) erfordert spezifische Formate, die Dayforce und Anbieter innerhalb des Landes/innerhalb der Region erkennen können.</span><span class="sxs-lookup"><span data-stu-id="48e7e-513">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="48e7e-514">Obwohl das Format für Orte flexibel ist, muss jeder Ort einem Bundesland zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="48e7e-514">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="48e7e-515">Talent</span><span class="sxs-lookup"><span data-stu-id="48e7e-515">Talent</span></span>          | <span data-ttu-id="48e7e-516">Dayforce</span><span class="sxs-lookup"><span data-stu-id="48e7e-516">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="48e7e-517">Land/Region</span><span class="sxs-lookup"><span data-stu-id="48e7e-517">Country/Region</span></span>  | <span data-ttu-id="48e7e-518">Ländercode</span><span class="sxs-lookup"><span data-stu-id="48e7e-518">Country Code</span></span>          |
| <span data-ttu-id="48e7e-519">Postleitzahl</span><span class="sxs-lookup"><span data-stu-id="48e7e-519">Zip/Postal Code</span></span> | <span data-ttu-id="48e7e-520">PLZ</span><span class="sxs-lookup"><span data-stu-id="48e7e-520">Postal Code</span></span>           |
| <span data-ttu-id="48e7e-521">Zustand</span><span class="sxs-lookup"><span data-stu-id="48e7e-521">State</span></span>           | <span data-ttu-id="48e7e-522">Bundeslandcode</span><span class="sxs-lookup"><span data-stu-id="48e7e-522">State Code</span></span>            |
| <span data-ttu-id="48e7e-523">Stadt</span><span class="sxs-lookup"><span data-stu-id="48e7e-523">City</span></span>            | <span data-ttu-id="48e7e-524">Stadt</span><span class="sxs-lookup"><span data-stu-id="48e7e-524">City</span></span>                  |
| <span data-ttu-id="48e7e-525">Verwaltungsbezirk</span><span class="sxs-lookup"><span data-stu-id="48e7e-525">County</span></span>          | <span data-ttu-id="48e7e-526">Landkreis (Gemeinde)</span><span class="sxs-lookup"><span data-stu-id="48e7e-526">County (Municipality)</span></span> |
| <span data-ttu-id="48e7e-527">Straße</span><span class="sxs-lookup"><span data-stu-id="48e7e-527">Street</span></span>          | <span data-ttu-id="48e7e-528">Adresszeile 1</span><span class="sxs-lookup"><span data-stu-id="48e7e-528">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="48e7e-529">Steuerregionen</span><span class="sxs-lookup"><span data-stu-id="48e7e-529">Tax regions</span></span>

<span data-ttu-id="48e7e-530">Steuerregionen werden verwendet, um die entsprechende Steuer festzulegen, die bei der Lohngenerierung angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="48e7e-530">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="48e7e-531">Steuerregionen werden Dayforce als Standortadressen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="48e7e-531">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="48e7e-532">Die Standardsteuerregion muss der aktiven Position der Arbeitskraft zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="48e7e-532">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="48e7e-533">Steuerregion (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-533">Tax region (required)</span></span>
- <span data-ttu-id="48e7e-534">Land/Region (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-534">Country/Region (required)</span></span>
- <span data-ttu-id="48e7e-535">Bundesland/Kanton (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-535">State (required)</span></span>
- <span data-ttu-id="48e7e-536">Verwaltungsbezirk</span><span class="sxs-lookup"><span data-stu-id="48e7e-536">County</span></span> 
- <span data-ttu-id="48e7e-537">Ort (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="48e7e-537">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="48e7e-538">Konfigurieren Ihrer Daten, um Lohn in Mexiko zu generieren</span><span class="sxs-lookup"><span data-stu-id="48e7e-538">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="48e7e-539">Wenn Sie Vergütung für Mitarbeiter in Mexiko generieren, müssen die folgenden Elemente konfiguriert werden:</span><span class="sxs-lookup"><span data-stu-id="48e7e-539">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="48e7e-540">Abteilungen sind für Positionen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="48e7e-540">Departments are required on positions.</span></span>
- <span data-ttu-id="48e7e-541">Kostenstellen müssen als Finanzdimensionen festgelegt werden und müssen das erste Element in der standardmäßigen Finanzdimensions-Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="48e7e-541">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="48e7e-542">Stellentypen</span><span class="sxs-lookup"><span data-stu-id="48e7e-542">Job types</span></span>

<span data-ttu-id="48e7e-543">Stellentypen werden verwendet, um ähnliche Stellen in Kategorien zu gruppieren.</span><span class="sxs-lookup"><span data-stu-id="48e7e-543">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="48e7e-544">Stellentypen sind erforderlich, um Lohn in Mexiko zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="48e7e-544">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="48e7e-545">Beispiele für Stellentypen umfassen Voll- und Teilzeit oder festes Gehalt und Stundenlohn.</span><span class="sxs-lookup"><span data-stu-id="48e7e-545">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="48e7e-546">Stellentypen werden Dayforce als Lohnarten zugeordnet, die angeben, ob ein Mitarbeiter auf Stundenbasis bezahlt wird oder ein festes Gehalt bezieht.</span><span class="sxs-lookup"><span data-stu-id="48e7e-546">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="48e7e-547">Folgende Stellentypen und Beschreibungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="48e7e-547">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="48e7e-548">Stellentyp</span><span class="sxs-lookup"><span data-stu-id="48e7e-548">Job type</span></span>   | <span data-ttu-id="48e7e-549">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="48e7e-549">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="48e7e-550">Stündlich</span><span class="sxs-lookup"><span data-stu-id="48e7e-550">Hourly</span></span>     | <span data-ttu-id="48e7e-551">MX – Stundenbasis</span><span class="sxs-lookup"><span data-stu-id="48e7e-551">MX Hourly</span></span>   |
| <span data-ttu-id="48e7e-552">Fest angestellt</span><span class="sxs-lookup"><span data-stu-id="48e7e-552">Salaried</span></span>   | <span data-ttu-id="48e7e-553">MX – Fest angestellt</span><span class="sxs-lookup"><span data-stu-id="48e7e-553">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="48e7e-554">Positionstypen</span><span class="sxs-lookup"><span data-stu-id="48e7e-554">Position types</span></span> 

<span data-ttu-id="48e7e-555">Sie verwenden Positionstypen, um zu beschreiben, ob die Position Vollzeit, Teilzeit oder etwas anderes ist.</span><span class="sxs-lookup"><span data-stu-id="48e7e-555">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="48e7e-556">Positionstypen werden Dayforce als Lohnklassen zugeordnet, die angeben, ob ein Mitarbeiter in Vollzeit oder Teilzeit arbeitet.</span><span class="sxs-lookup"><span data-stu-id="48e7e-556">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="48e7e-557">Folgende Positionstypen und Beschreibungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="48e7e-557">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="48e7e-558">Positionstyp</span><span class="sxs-lookup"><span data-stu-id="48e7e-558">Position type</span></span>   | <span data-ttu-id="48e7e-559">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="48e7e-559">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="48e7e-560">Vollzeit</span><span class="sxs-lookup"><span data-stu-id="48e7e-560">Full-time</span></span>       | <span data-ttu-id="48e7e-561">Vollzeitmitarbeiter</span><span class="sxs-lookup"><span data-stu-id="48e7e-561">Full time employee</span></span> |
| <span data-ttu-id="48e7e-562">Teilzeit</span><span class="sxs-lookup"><span data-stu-id="48e7e-562">Part-time</span></span>       | <span data-ttu-id="48e7e-563">Teilzeitmitarbeiter</span><span class="sxs-lookup"><span data-stu-id="48e7e-563">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="48e7e-564">Ursachencodes</span><span class="sxs-lookup"><span data-stu-id="48e7e-564">Reason codes</span></span>

<span data-ttu-id="48e7e-565">Ursachencodes enthalten Informationen zum Status eines Mitarbeiters.</span><span class="sxs-lookup"><span data-stu-id="48e7e-565">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="48e7e-566">Ursachencodes werden Dayforce als Statusgründe zugeordnet, die den Grund für Änderungen bei der Position eines Mitarbeiters oder dem Beschäftigungsstatus angeben.</span><span class="sxs-lookup"><span data-stu-id="48e7e-566">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="48e7e-567">Folgende Ursachencodes und Beschreibungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="48e7e-567">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="48e7e-568">Ursachencode</span><span class="sxs-lookup"><span data-stu-id="48e7e-568">Reason code</span></span>            | <span data-ttu-id="48e7e-569">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="48e7e-569">Description</span></span>                    | <span data-ttu-id="48e7e-570">Zutreffende Szenarios</span><span class="sxs-lookup"><span data-stu-id="48e7e-570">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="48e7e-571">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="48e7e-571">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="48e7e-572">Abgang vor erster Lohnzahlung</span><span class="sxs-lookup"><span data-stu-id="48e7e-572">Departure before first payroll</span></span> | <span data-ttu-id="48e7e-573">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="48e7e-573">Terminate worker</span></span>     |
| <span data-ttu-id="48e7e-574">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="48e7e-574">RESIGNATION</span></span>            | <span data-ttu-id="48e7e-575">Kündigung durch Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="48e7e-575">Resignation</span></span>                    | <span data-ttu-id="48e7e-576">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="48e7e-576">Terminate worker</span></span>     |
| <span data-ttu-id="48e7e-577">PENSION</span><span class="sxs-lookup"><span data-stu-id="48e7e-577">PENSION</span></span>                | <span data-ttu-id="48e7e-578">Rente</span><span class="sxs-lookup"><span data-stu-id="48e7e-578">Pension</span></span>                        | <span data-ttu-id="48e7e-579">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="48e7e-579">Terminate worker</span></span>     |
| <span data-ttu-id="48e7e-580">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="48e7e-580">TERMINATION</span></span>            | <span data-ttu-id="48e7e-581">Beendigung</span><span class="sxs-lookup"><span data-stu-id="48e7e-581">Termination</span></span>                    | <span data-ttu-id="48e7e-582">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="48e7e-582">Terminate worker</span></span>     |
| <span data-ttu-id="48e7e-583">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="48e7e-583">RETIREMENT</span></span>             | <span data-ttu-id="48e7e-584">Ruhestand</span><span class="sxs-lookup"><span data-stu-id="48e7e-584">Retirement</span></span>                     | <span data-ttu-id="48e7e-585">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="48e7e-585">Terminate worker</span></span>     |
| <span data-ttu-id="48e7e-586">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="48e7e-586">ABSENTEE</span></span>               | <span data-ttu-id="48e7e-587">Abwesende Person</span><span class="sxs-lookup"><span data-stu-id="48e7e-587">Absentee</span></span>                       | <span data-ttu-id="48e7e-588">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="48e7e-588">Terminate worker</span></span>     |
| <span data-ttu-id="48e7e-589">OTHER</span><span class="sxs-lookup"><span data-stu-id="48e7e-589">OTHER</span></span>                  | <span data-ttu-id="48e7e-590">Andere Gründe</span><span class="sxs-lookup"><span data-stu-id="48e7e-590">Other Reasons</span></span>                  | <span data-ttu-id="48e7e-591">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="48e7e-591">Terminate worker</span></span>     |
| <span data-ttu-id="48e7e-592">CLOSURE</span><span class="sxs-lookup"><span data-stu-id="48e7e-592">CLOSURE</span></span>                | <span data-ttu-id="48e7e-593">Betriebsferien</span><span class="sxs-lookup"><span data-stu-id="48e7e-593">Business Closure</span></span>               | <span data-ttu-id="48e7e-594">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="48e7e-594">Terminate worker</span></span>     |
| <span data-ttu-id="48e7e-595">DEATH</span><span class="sxs-lookup"><span data-stu-id="48e7e-595">DEATH</span></span>                  | <span data-ttu-id="48e7e-596">Tod</span><span class="sxs-lookup"><span data-stu-id="48e7e-596">Death</span></span>                          | <span data-ttu-id="48e7e-597">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="48e7e-597">Terminate worker</span></span>     |
| <span data-ttu-id="48e7e-598">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="48e7e-598">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="48e7e-599">Beurlaubung</span><span class="sxs-lookup"><span data-stu-id="48e7e-599">Leave of Absence</span></span>               | <span data-ttu-id="48e7e-600">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="48e7e-600">Terminate worker</span></span>     |
| <span data-ttu-id="48e7e-601">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="48e7e-601">CONTRACTEND</span></span>            | <span data-ttu-id="48e7e-602">Vertragsende</span><span class="sxs-lookup"><span data-stu-id="48e7e-602">End of Contract</span></span>                | <span data-ttu-id="48e7e-603">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="48e7e-603">Terminate worker</span></span>     |
| <span data-ttu-id="48e7e-604">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="48e7e-604">SALARYCHANGE</span></span>           | <span data-ttu-id="48e7e-605">Gehaltsänderung</span><span class="sxs-lookup"><span data-stu-id="48e7e-605">Change of Salary</span></span>               | <span data-ttu-id="48e7e-606">Vergütung</span><span class="sxs-lookup"><span data-stu-id="48e7e-606">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="48e7e-607">Einstellungsbedingungen</span><span class="sxs-lookup"><span data-stu-id="48e7e-607">Terms of employment</span></span>

<span data-ttu-id="48e7e-608">Beschäftigungsbedingungen werden verwendet, um Kategorien von Beschäftigungsbedingungen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="48e7e-608">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="48e7e-609">Die Bedingungen werden Dayforce als Beschäftigungsindikatorwerte zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="48e7e-609">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="48e7e-610">Die folgenden Bedingungen für Beschäftigung und Beschreibungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="48e7e-610">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="48e7e-611">Einstellungsbedingungen</span><span class="sxs-lookup"><span data-stu-id="48e7e-611">Terms of employment</span></span>   | <span data-ttu-id="48e7e-612">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="48e7e-612">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="48e7e-613">Regelmäßig</span><span class="sxs-lookup"><span data-stu-id="48e7e-613">Regular</span></span>               | <span data-ttu-id="48e7e-614">Regelmäßig</span><span class="sxs-lookup"><span data-stu-id="48e7e-614">Regular</span></span>     |
| <span data-ttu-id="48e7e-615">Direkt</span><span class="sxs-lookup"><span data-stu-id="48e7e-615">Direct</span></span>                | <span data-ttu-id="48e7e-616">Direkt</span><span class="sxs-lookup"><span data-stu-id="48e7e-616">Direct</span></span>      |
| <span data-ttu-id="48e7e-617">Praktikum</span><span class="sxs-lookup"><span data-stu-id="48e7e-617">Internship</span></span>            | <span data-ttu-id="48e7e-618">Praktikum</span><span class="sxs-lookup"><span data-stu-id="48e7e-618">Internship</span></span>  |
| <span data-ttu-id="48e7e-619">Unbefristet</span><span class="sxs-lookup"><span data-stu-id="48e7e-619">Permanent</span></span>             | <span data-ttu-id="48e7e-620">Unbefristet</span><span class="sxs-lookup"><span data-stu-id="48e7e-620">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="48e7e-621">Familienstand</span><span class="sxs-lookup"><span data-stu-id="48e7e-621">Marital status</span></span>

<span data-ttu-id="48e7e-622">Familienstandwerte werden Dayforce zugeordnet und werden – je nach Bedarf – in die akzeptierten Werte bei der Integration übersetzt.</span><span class="sxs-lookup"><span data-stu-id="48e7e-622">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="48e7e-623">Die folgende Tabelle zeigt, wie Familienstandwerte Dayforce zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="48e7e-623">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="48e7e-624">Talent</span><span class="sxs-lookup"><span data-stu-id="48e7e-624">Talent</span></span>                 | <span data-ttu-id="48e7e-625">Dayforce</span><span class="sxs-lookup"><span data-stu-id="48e7e-625">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="48e7e-626">Verheiratet</span><span class="sxs-lookup"><span data-stu-id="48e7e-626">Married</span></span>                | <span data-ttu-id="48e7e-627">Verheiratet</span><span class="sxs-lookup"><span data-stu-id="48e7e-627">Married</span></span>                   |
| <span data-ttu-id="48e7e-628">Ledig</span><span class="sxs-lookup"><span data-stu-id="48e7e-628">Single</span></span>                 | <span data-ttu-id="48e7e-629">Ledig</span><span class="sxs-lookup"><span data-stu-id="48e7e-629">Single</span></span>                    |
| <span data-ttu-id="48e7e-630">Verwitwet</span><span class="sxs-lookup"><span data-stu-id="48e7e-630">Widowed</span></span>                | <span data-ttu-id="48e7e-631">Verwitwet</span><span class="sxs-lookup"><span data-stu-id="48e7e-631">Widowed</span></span>                   |
| <span data-ttu-id="48e7e-632">Geschieden</span><span class="sxs-lookup"><span data-stu-id="48e7e-632">Divorced</span></span>               | <span data-ttu-id="48e7e-633">Geschieden</span><span class="sxs-lookup"><span data-stu-id="48e7e-633">Divorced</span></span>                  |
| <span data-ttu-id="48e7e-634">Eingetragene Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="48e7e-634">Registered Partnership</span></span> | <span data-ttu-id="48e7e-635">Inländische Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="48e7e-635">Domestic Partnership</span></span>      |
| <span data-ttu-id="48e7e-636">None</span><span class="sxs-lookup"><span data-stu-id="48e7e-636">None</span></span>                   | <span data-ttu-id="48e7e-637">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="48e7e-637">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="48e7e-638">Freie Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="48e7e-638">Cohabiting</span></span>             | <span data-ttu-id="48e7e-639">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="48e7e-639">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="48e7e-640">Geschlecht</span><span class="sxs-lookup"><span data-stu-id="48e7e-640">Gender</span></span>

<span data-ttu-id="48e7e-641">Geschlechtsbezeichnungen werden Dayforce zugeordnet und werden – je nach Bedarf – in die akzeptierten Werte bei der Integration übersetzt.</span><span class="sxs-lookup"><span data-stu-id="48e7e-641">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="48e7e-642">Die folgende Tabelle zeigt, wie Geschlechtsbezeichnungen Dayforce zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="48e7e-642">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="48e7e-643">Talent</span><span class="sxs-lookup"><span data-stu-id="48e7e-643">Talent</span></span>       | <span data-ttu-id="48e7e-644">Dayforce</span><span class="sxs-lookup"><span data-stu-id="48e7e-644">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="48e7e-645">Männlich</span><span class="sxs-lookup"><span data-stu-id="48e7e-645">Male</span></span>         | <span data-ttu-id="48e7e-646">Männlich</span><span class="sxs-lookup"><span data-stu-id="48e7e-646">Male</span></span>                      |
| <span data-ttu-id="48e7e-647">Weiblich</span><span class="sxs-lookup"><span data-stu-id="48e7e-647">Female</span></span>       | <span data-ttu-id="48e7e-648">Weiblich</span><span class="sxs-lookup"><span data-stu-id="48e7e-648">Female</span></span>                    |
| <span data-ttu-id="48e7e-649">Nicht spezifisch</span><span class="sxs-lookup"><span data-stu-id="48e7e-649">Non-specific</span></span> | <span data-ttu-id="48e7e-650">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="48e7e-650">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="48e7e-651">Zahlungsweise</span><span class="sxs-lookup"><span data-stu-id="48e7e-651">Payment method</span></span>

<span data-ttu-id="48e7e-652">Zahlungsmethoden geben dem Mitarbeiter und dem Unternehmen die Möglichkeit zu beschreiben, wie Mitarbeiter bezahlt werden.</span><span class="sxs-lookup"><span data-stu-id="48e7e-652">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="48e7e-653">Zahlungsmethoden werden Dayforce zugeordnet und werden – je nach Bedarf – in die akzeptierten Werte bei der Integration übersetzt.</span><span class="sxs-lookup"><span data-stu-id="48e7e-653">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="48e7e-654">Die folgende Tabelle zeigt, wie Zahlungsmethoden Dayforce zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="48e7e-654">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="48e7e-655">Talent</span><span class="sxs-lookup"><span data-stu-id="48e7e-655">Talent</span></span>             | <span data-ttu-id="48e7e-656">Dayforce</span><span class="sxs-lookup"><span data-stu-id="48e7e-656">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="48e7e-657">Bargeld</span><span class="sxs-lookup"><span data-stu-id="48e7e-657">Cash</span></span>               | <span data-ttu-id="48e7e-658">Bargeld</span><span class="sxs-lookup"><span data-stu-id="48e7e-658">Cash</span></span>                      |
| <span data-ttu-id="48e7e-659">Elektronische Zahlung</span><span class="sxs-lookup"><span data-stu-id="48e7e-659">Electronic Payment</span></span> | <span data-ttu-id="48e7e-660">Übertragen</span><span class="sxs-lookup"><span data-stu-id="48e7e-660">Transfer</span></span>                  |
| <span data-ttu-id="48e7e-661">Scheck</span><span class="sxs-lookup"><span data-stu-id="48e7e-661">Check</span></span>              | <span data-ttu-id="48e7e-662">Scheck</span><span class="sxs-lookup"><span data-stu-id="48e7e-662">Cheque</span></span>                    |
| <span data-ttu-id="48e7e-663">Bankwechsel</span><span class="sxs-lookup"><span data-stu-id="48e7e-663">Bank Draft</span></span>         | <span data-ttu-id="48e7e-664">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="48e7e-664">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="48e7e-665">Sonstige</span><span class="sxs-lookup"><span data-stu-id="48e7e-665">Other</span></span>              | <span data-ttu-id="48e7e-666">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="48e7e-666">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="48e7e-667">Bankkontotyp</span><span class="sxs-lookup"><span data-stu-id="48e7e-667">Bank account type</span></span>

<span data-ttu-id="48e7e-668">Bankkontotypen werden für elektronische Zahlungen an Mitarbeiter verwendet.</span><span class="sxs-lookup"><span data-stu-id="48e7e-668">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="48e7e-669">Bankkontotypen werden Dayforce als Übergweisungskontoinformationen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="48e7e-669">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="48e7e-670">Die Bankkontotypen werden bei Bedarf zu den akzeptierten Werte nach der Integration übersetzt.</span><span class="sxs-lookup"><span data-stu-id="48e7e-670">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="48e7e-671">Talent</span><span class="sxs-lookup"><span data-stu-id="48e7e-671">Talent</span></span>            | <span data-ttu-id="48e7e-672">Dayforce</span><span class="sxs-lookup"><span data-stu-id="48e7e-672">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="48e7e-673">Girokonto</span><span class="sxs-lookup"><span data-stu-id="48e7e-673">Checking Account</span></span>  | <span data-ttu-id="48e7e-674">Girokonto</span><span class="sxs-lookup"><span data-stu-id="48e7e-674">CheckingAccount</span></span>           |
| <span data-ttu-id="48e7e-675">Lohnkonto</span><span class="sxs-lookup"><span data-stu-id="48e7e-675">Payroll Account</span></span>   | <span data-ttu-id="48e7e-676">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="48e7e-676">PayrollAccount</span></span>            |
| <span data-ttu-id="48e7e-677">Sparkonto</span><span class="sxs-lookup"><span data-stu-id="48e7e-677">Savings Account</span></span>   | <span data-ttu-id="48e7e-678">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="48e7e-678">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="48e7e-679">BankGirot-Konto</span><span class="sxs-lookup"><span data-stu-id="48e7e-679">BankGirot account</span></span> | <span data-ttu-id="48e7e-680">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="48e7e-680">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="48e7e-681">PlusGirot-Konto</span><span class="sxs-lookup"><span data-stu-id="48e7e-681">PlusGirot account</span></span> | <span data-ttu-id="48e7e-682">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="48e7e-682">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="48e7e-683">Einkommenscodes</span><span class="sxs-lookup"><span data-stu-id="48e7e-683">Earning codes</span></span>

<span data-ttu-id="48e7e-684">Einkommenscodes bestimmen jeden Typ von Einkünften eindeutig, die Arbeitskräfte erhalten</span><span class="sxs-lookup"><span data-stu-id="48e7e-684">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="48e7e-685">Die Codes decken verschiedene Parameter ab, die sich auf Einkünfte beziehen, wie beispielsweise Buchhaltungsvorschriften, Steuergesetze, Berichterstellungsanforderungen und Bruttoausgleichsfähigkeit.</span><span class="sxs-lookup"><span data-stu-id="48e7e-685">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="48e7e-686">Wenn eine nicht unterstützte Häufigkeit verwendet wird, wird die Häufigkeit **Jeder Lohn** standardmäßig für die Berechnung verwendet.</span><span class="sxs-lookup"><span data-stu-id="48e7e-686">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="48e7e-687">Unterstützte Häufigkeiten</span><span class="sxs-lookup"><span data-stu-id="48e7e-687">Supported frequencies</span></span>

- <span data-ttu-id="48e7e-688">Alle</span><span class="sxs-lookup"><span data-stu-id="48e7e-688">All</span></span>
- <span data-ttu-id="48e7e-689">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="48e7e-689">EVERYPAY</span></span>
- <span data-ttu-id="48e7e-690">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="48e7e-690">EACHPAYPERIOD</span></span>
- <span data-ttu-id="48e7e-691">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="48e7e-691">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="48e7e-692">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="48e7e-692">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="48e7e-693">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="48e7e-693">1OFMTH</span></span>
- <span data-ttu-id="48e7e-694">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="48e7e-694">LASTOFMTH</span></span>
- <span data-ttu-id="48e7e-695">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="48e7e-695">2OFMTH</span></span>
- <span data-ttu-id="48e7e-696">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="48e7e-696">3OFMTH</span></span>
- <span data-ttu-id="48e7e-697">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="48e7e-697">4OFMTH</span></span>
- <span data-ttu-id="48e7e-698">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="48e7e-698">5OFMTH</span></span>
- <span data-ttu-id="48e7e-699">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="48e7e-699">1N2OFMTH</span></span>
- <span data-ttu-id="48e7e-700">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="48e7e-700">3N4OFMTH</span></span>
- <span data-ttu-id="48e7e-701">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="48e7e-701">1N3OFMTH</span></span>
- <span data-ttu-id="48e7e-702">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="48e7e-702">1N4OFMTH</span></span>
- <span data-ttu-id="48e7e-703">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="48e7e-703">2N3OFMTH</span></span>
- <span data-ttu-id="48e7e-704">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="48e7e-704">2N4OFMTH</span></span>
- <span data-ttu-id="48e7e-705">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="48e7e-705">1N2N3OFMTH</span></span>
- <span data-ttu-id="48e7e-706">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="48e7e-706">1N2N4OFMTH</span></span>
- <span data-ttu-id="48e7e-707">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="48e7e-707">1N3N4OFMTH</span></span>
- <span data-ttu-id="48e7e-708">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="48e7e-708">2N3N4OFMTH</span></span>
- <span data-ttu-id="48e7e-709">1N2N3N4OFMTH – 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="48e7e-709">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="48e7e-710">2N3N4N5OFMth – 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="48e7e-710">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="48e7e-711">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="48e7e-711">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="48e7e-712">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="48e7e-712">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="48e7e-713">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="48e7e-713">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="48e7e-714">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="48e7e-714">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="48e7e-715">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="48e7e-715">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="48e7e-716">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="48e7e-716">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="48e7e-717">Adressen</span><span class="sxs-lookup"><span data-stu-id="48e7e-717">Addresses</span></span>

<span data-ttu-id="48e7e-718">Die Kennung bestimmter Codes für Land oder Region, Bundesland/Kanton oder Landkreis (Gemeinde) erfordert spezifische Formate, die Dayforce und Anbieter innerhalb des Landes/innerhalb der Region erkennen können.</span><span class="sxs-lookup"><span data-stu-id="48e7e-718">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="48e7e-719">Obwohl das Format für Orte flexibel ist, muss jeder Ort einem Bundesland zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="48e7e-719">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="48e7e-720">Talent</span><span class="sxs-lookup"><span data-stu-id="48e7e-720">Talent</span></span>              | <span data-ttu-id="48e7e-721">Dayforce</span><span class="sxs-lookup"><span data-stu-id="48e7e-721">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="48e7e-722">Land/Region</span><span class="sxs-lookup"><span data-stu-id="48e7e-722">Country/Region</span></span>      | <span data-ttu-id="48e7e-723">Ländercode</span><span class="sxs-lookup"><span data-stu-id="48e7e-723">Country Code</span></span>          |
| <span data-ttu-id="48e7e-724">Postleitzahl</span><span class="sxs-lookup"><span data-stu-id="48e7e-724">Zip/Postal Code</span></span>     | <span data-ttu-id="48e7e-725">PLZ</span><span class="sxs-lookup"><span data-stu-id="48e7e-725">Postal Code</span></span>           |
| <span data-ttu-id="48e7e-726">Zustand</span><span class="sxs-lookup"><span data-stu-id="48e7e-726">State</span></span>               | <span data-ttu-id="48e7e-727">Bundeslandcode</span><span class="sxs-lookup"><span data-stu-id="48e7e-727">State Code</span></span>            |
| <span data-ttu-id="48e7e-728">Stadt</span><span class="sxs-lookup"><span data-stu-id="48e7e-728">City</span></span>                | <span data-ttu-id="48e7e-729">Stadt</span><span class="sxs-lookup"><span data-stu-id="48e7e-729">City</span></span>                  |
| <span data-ttu-id="48e7e-730">Verwaltungsbezirk</span><span class="sxs-lookup"><span data-stu-id="48e7e-730">County</span></span>              | <span data-ttu-id="48e7e-731">Landkreis (Gemeinde)</span><span class="sxs-lookup"><span data-stu-id="48e7e-731">County (Municipality)</span></span> |
| <span data-ttu-id="48e7e-732">Straße</span><span class="sxs-lookup"><span data-stu-id="48e7e-732">Street</span></span>              | <span data-ttu-id="48e7e-733">Adresszeile 1</span><span class="sxs-lookup"><span data-stu-id="48e7e-733">Address Line 1</span></span>        |
| <span data-ttu-id="48e7e-734">Hausnummer</span><span class="sxs-lookup"><span data-stu-id="48e7e-734">Street Number</span></span>       | <span data-ttu-id="48e7e-735">Adresszeile 2</span><span class="sxs-lookup"><span data-stu-id="48e7e-735">Address Line 2</span></span>        |
| <span data-ttu-id="48e7e-736">Gebäudeergänzung</span><span class="sxs-lookup"><span data-stu-id="48e7e-736">Building Complement</span></span> | <span data-ttu-id="48e7e-737">Adresszeile 5</span><span class="sxs-lookup"><span data-stu-id="48e7e-737">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="48e7e-738">Ausweisnummer</span><span class="sxs-lookup"><span data-stu-id="48e7e-738">Passport number</span></span>

<span data-ttu-id="48e7e-739">Mitarbeiter können Ausweisinformationen melden.</span><span class="sxs-lookup"><span data-stu-id="48e7e-739">Employees can declare passport information.</span></span> <span data-ttu-id="48e7e-740">Diese Informationen haben den Kennungstyp **Ausweis** und sind in Dayforce als Teil der für Mexiko spezifischen Informationen eines Mitarbeiters integriert.</span><span class="sxs-lookup"><span data-stu-id="48e7e-740">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="48e7e-741">Kennungstyp = „Ausweis”</span><span class="sxs-lookup"><span data-stu-id="48e7e-741">Identification Type = "Passport"</span></span>
- <span data-ttu-id="48e7e-742">Ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="48e7e-742">Issued Date</span></span>
- <span data-ttu-id="48e7e-743">Ablaufdatum</span><span class="sxs-lookup"><span data-stu-id="48e7e-743">Expiration Date</span></span>

<span data-ttu-id="48e7e-744">Mitarbeiter können mehrere Kennungsnummern des Kennungstyps **Ausweis** melden.</span><span class="sxs-lookup"><span data-stu-id="48e7e-744">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="48e7e-745">Jedoch wird nur der aktuell aktive Ausweiseintrag in Dayforce integriert.</span><span class="sxs-lookup"><span data-stu-id="48e7e-745">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="48e7e-746">Wenn alle Ausweiseinträge abgelaufen sind, ist der Ausweis, der zuletzt ausgestellt wurde, in Dayforce integriert.</span><span class="sxs-lookup"><span data-stu-id="48e7e-746">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>
