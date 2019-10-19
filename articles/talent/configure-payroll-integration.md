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
ms.openlocfilehash: ec1d14cb14ab709dfc1bead4be0785904efcce4e
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251038"
---
# <a name="configure-the-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="0fb3d-103">Lohnintegration zwischen Talent und Dayforce konfigurieren</span><span class="sxs-lookup"><span data-stu-id="0fb3d-103">Configure the payroll integration between Talent and Dayforce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0fb3d-104">Die Integration zwischen Microsoft Dynamics 365 Talent und Ceridian Dayforce beruht auf mehreren Konfigurationsschritten, die in diesem Thema beschrieben sind.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-104">The integration between Microsoft Dynamics 365 Talent and Ceridian Dayforce relies on several configuration steps that are described in this topic.</span></span> <span data-ttu-id="0fb3d-105">Sie müssen die Integration sowohl in Talent als auch in Dayforce konfigurieren, bevor Sie einen Zahllauf verarbeiten können.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-105">You must configure the integration in both Talent and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="0fb3d-106">Wenn Sie einen Dienst wie Dayforce verwenden, um Zahlläufe abzuschließen, müssen Sie die Integration in Talent ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-106">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Talent.</span></span> <span data-ttu-id="0fb3d-107">Die Integration erfordert bestimmte Daten aus Talent.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-107">The integration requires specific data from Talent.</span></span> <span data-ttu-id="0fb3d-108">Daher müssen Sie überprüfen, dass die Daten, die Dayforce zugeordnet sind, in Talent in einer Weise konfiguriert werden, die die Integration unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-108">Therefore, you must verify that data that is mapped to Dayforce is configured in Talent in a manner that supports the integration.</span></span> <span data-ttu-id="0fb3d-109">Bei der Integration werden die folgenden allgemeinen Kategorien von Daten verwendet:</span><span class="sxs-lookup"><span data-stu-id="0fb3d-109">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="0fb3d-110">Personalverwaltungsdaten</span><span class="sxs-lookup"><span data-stu-id="0fb3d-110">Human resources data</span></span>
- <span data-ttu-id="0fb3d-111">Vergütungsdaten</span><span class="sxs-lookup"><span data-stu-id="0fb3d-111">Compensation data</span></span>
- <span data-ttu-id="0fb3d-112">Lohndaten, wie Lohnzyklen, Lohnperioden und Einkommenscodes</span><span class="sxs-lookup"><span data-stu-id="0fb3d-112">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="0fb3d-113">Arbeitskraftdaten</span><span class="sxs-lookup"><span data-stu-id="0fb3d-113">Worker data</span></span>

<span data-ttu-id="0fb3d-114">In diesem Thema werden die Schritte beschrieben, die Sie befolgen müssen, um die Integration zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-114">This topic describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="0fb3d-115">Es werden auch die Datentypen und die Konfigurationsdetails erklärt, die für die Integration erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-115">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="0fb3d-116">Die Integration aktivieren</span><span class="sxs-lookup"><span data-stu-id="0fb3d-116">Enable the integration</span></span>

<span data-ttu-id="0fb3d-117">In Talent müssen Sie die Integration aktivieren und die Konfigurationsinformationen eingeben, um eine Verbindung mit Dayforce herzustellen.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-117">In Talent, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="0fb3d-118">Wenn Sie möchten, dass die erstellte Hauptbuchtransaktion in Microsoft Dynamics 365 Finance importiert wird, müssen Sie auch ein Microsoft Azure-Speicherkonto einrichten und die Azure Storage-Verbindungszeichenfolge in Finance eingeben.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-118">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 Finance, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance.</span></span>

<span data-ttu-id="0fb3d-119">Um die Integration in Talent zu aktivieren, gehen Sie folgendermaßen vor.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-119">To turn on the integration in Talent, follow these steps.</span></span>

1. <span data-ttu-id="0fb3d-120">Wählen Sie auf der Seite **Systemverwaltung** die Option **Integrationskonfiguration** aus.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-120">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="0fb3d-121">Geben Sie den sicheren Datenübertragungsprotokoll-(FTP)-Endpunkt und den sicheren FTP-Ordnerpfad ein.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-121">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="0fb3d-122">Geben Sie den Benutzernamen und das Kennwort des Benutzers ein, der auf den sicheren FTP-Endpunkt und Ordnerpfad zugreift.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-122">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="0fb3d-123">Testen Sie die Verbindung nach Bedarf, und legen Sie die Option **Lohnintegration aktivieren** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-123">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="0fb3d-124">Wenn die Integration aktiviert ist, werden Datenexportpaket und Dateien erstellt und die Häufigkeit wird festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-124">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="0fb3d-125">Sie können diese Häufigkeit nach Bedarf ändern.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-125">You can change this frequency as you require.</span></span>

<span data-ttu-id="0fb3d-126">Weitere Informationen zu Azure-Speicherkonten und Azure Storage-Verbindungszeichenfolgen finden Sie in den folgenden Azure-Themen:</span><span class="sxs-lookup"><span data-stu-id="0fb3d-126">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure topics:</span></span>

- [<span data-ttu-id="0fb3d-127">Über Azure-Speicherkonten</span><span class="sxs-lookup"><span data-stu-id="0fb3d-127">About Azure storage accounts</span></span>](https://docs.microsoft.com/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="0fb3d-128">Azure Storage-Verbindungszeichenfolgen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="0fb3d-128">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="0fb3d-129">Technische Details, wenn Lohnintegration aktiviert ist</span><span class="sxs-lookup"><span data-stu-id="0fb3d-129">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="0fb3d-130">Die Aktivierung von Lohnintegration hat zwei primäre Auswirkungen:</span><span class="sxs-lookup"><span data-stu-id="0fb3d-130">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="0fb3d-131">Ein Datenexportprojekt namens „Lohnintegrationsexport“ wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-131">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="0fb3d-132">Dieses Projekt enthält die Entitäten und Felder, die für die Lohnintegration erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-132">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="0fb3d-133">Um das Projekt zu überprüfen, wechseln Sie zu **Systemverwaltung**, wählen Sie die Kachel **Datenverwaltung** aus, und öffnen Sie anschließend das Datenprojekt aus der Projektliste.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-133">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="0fb3d-134">Dieser Stapelverarbeitungsauftrag führt das Datenexportprojekt aus, verschlüsselt das Datenpaket und überträgt die Datenenpaketdatei auf den SFTP-Endpunkt, der auf dem Bildschirm **Integrationskonfiguration** konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-134">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="0fb3d-135">Das Datenpaket, das zum SFTP-Endpunkt übertragen wird, wird mit einem Schlüssel verschlüsselt, für das Paket eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-135">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="0fb3d-136">Der Schlüssel befindet sich in einer Azure Key Vault, auf den nur durch Ceridian zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-136">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="0fb3d-137">Es ist nicht möglich, die Datenpaketinhalte zu entschlüsseln und zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-137">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="0fb3d-138">Wenn Sie den Inhalt des Datenpakets überprüfen möchten, müssen Sie das Datenprojekt „Lohnintegrationsexport“ manuell exportieren, herunterladen und dann öffnen.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-138">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="0fb3d-139">Beim manuellen Export wird keine Verschlüsselung angewendet oder das Paket übertragen.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-139">Manual export will not apply encryption or transfer the package.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="0fb3d-140">Ihre Daten konfigurieren</span><span class="sxs-lookup"><span data-stu-id="0fb3d-140">Configure your data</span></span> 

<span data-ttu-id="0fb3d-141">Um die Lohnbuchung zu verarbeiten, müssen Sie Personalverwaltungsdaten in Talent konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-141">To process payroll, you must configure human resource data in Talent.</span></span> <span data-ttu-id="0fb3d-142">Sie müssen Organisationsdaten, wie Stellen und Positionen, zusammen mit Vorteilen Vergütungsinformationen einrichten.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-142">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="0fb3d-143">Diese Informationen stellen Beschäftigung, Lohn und die Abzugsinformationen bereit, die zur Generierung der Mitarbeiterentlohnung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-143">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="0fb3d-144">Personalverwaltungsdaten</span><span class="sxs-lookup"><span data-stu-id="0fb3d-144">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="0fb3d-145">Vergütungen</span><span class="sxs-lookup"><span data-stu-id="0fb3d-145">Benefits</span></span> 

<span data-ttu-id="0fb3d-146">Die Personalverwaltung stellt eine Reihe von Tools für die Einrichtung und Verwaltung der Vorteile, Abzüge und Vergütungspläne der Arbeitskräfte bereit, die eine Organisation für seine Arbeitskräfte anbietet oder verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-146">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="0fb3d-147">Wenn Sie Vorteile erstellen, sollten Sie folgende Daten und Konfigurationen bedenken, die in Dayforce verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-147">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="0fb3d-148">Vorteilspläne</span><span class="sxs-lookup"><span data-stu-id="0fb3d-148">Benefit plans</span></span>

- <span data-ttu-id="0fb3d-149">Plan (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-149">Plan (required)</span></span>
- <span data-ttu-id="0fb3d-150">Typ (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-150">Type (required)</span></span>
- <span data-ttu-id="0fb3d-151">Lohnauswirkung (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-151">Payroll impact (required)</span></span>
- <span data-ttu-id="0fb3d-152">Rückstände wiederherstellen</span><span class="sxs-lookup"><span data-stu-id="0fb3d-152">Recover arrears</span></span>
- <span data-ttu-id="0fb3d-153">Abzugsverfahren</span><span class="sxs-lookup"><span data-stu-id="0fb3d-153">Deduction method</span></span>
- <span data-ttu-id="0fb3d-154">Abzugspriorität</span><span class="sxs-lookup"><span data-stu-id="0fb3d-154">Deduction priority</span></span>
- <span data-ttu-id="0fb3d-155">Periode eingrenzen</span><span class="sxs-lookup"><span data-stu-id="0fb3d-155">Limit period</span></span>
- <span data-ttu-id="0fb3d-156">Limitbetrag</span><span class="sxs-lookup"><span data-stu-id="0fb3d-156">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="0fb3d-157">Vergütungen</span><span class="sxs-lookup"><span data-stu-id="0fb3d-157">Benefits</span></span>

- <span data-ttu-id="0fb3d-158">Plan (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-158">Plan (required)</span></span>
- <span data-ttu-id="0fb3d-159">Typ (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-159">Type (required)</span></span>
- <span data-ttu-id="0fb3d-160">Option (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-160">Option (required)</span></span>
- <span data-ttu-id="0fb3d-161">Vorteilskennung (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-161">Benefit ID (required)</span></span>
- <span data-ttu-id="0fb3d-162">Häufigkeit</span><span class="sxs-lookup"><span data-stu-id="0fb3d-162">Frequency</span></span>
- <span data-ttu-id="0fb3d-163">Basis</span><span class="sxs-lookup"><span data-stu-id="0fb3d-163">Basis</span></span>
- <span data-ttu-id="0fb3d-164">Betrag oder Satz</span><span class="sxs-lookup"><span data-stu-id="0fb3d-164">Amount or rate</span></span>
- <span data-ttu-id="0fb3d-165">Einkommenscode</span><span class="sxs-lookup"><span data-stu-id="0fb3d-165">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="0fb3d-166">Unterstützte Häufigkeiten</span><span class="sxs-lookup"><span data-stu-id="0fb3d-166">Supported frequencies</span></span> 

- <span data-ttu-id="0fb3d-167">Wöchentlich</span><span class="sxs-lookup"><span data-stu-id="0fb3d-167">Weekly</span></span>
- <span data-ttu-id="0fb3d-168">14-tägig</span><span class="sxs-lookup"><span data-stu-id="0fb3d-168">Bi-weekly</span></span>
- <span data-ttu-id="0fb3d-169">Halbmonatlich</span><span class="sxs-lookup"><span data-stu-id="0fb3d-169">Semi-monthly</span></span>
- <span data-ttu-id="0fb3d-170">Monatlich</span><span class="sxs-lookup"><span data-stu-id="0fb3d-170">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="0fb3d-171">Unterstützte Basen</span><span class="sxs-lookup"><span data-stu-id="0fb3d-171">Supported bases</span></span> 

- <span data-ttu-id="0fb3d-172">Fester Betrag</span><span class="sxs-lookup"><span data-stu-id="0fb3d-172">Fixed amount</span></span>
- <span data-ttu-id="0fb3d-173">Prozent des Einkommens</span><span class="sxs-lookup"><span data-stu-id="0fb3d-173">Percent of earnings</span></span>
- <span data-ttu-id="0fb3d-174">Produktive Stunden</span><span class="sxs-lookup"><span data-stu-id="0fb3d-174">Productive hours</span></span>

<span data-ttu-id="0fb3d-175">Dayforce erstellt die folgenden Abzüge, basierend auf den Lohnauswirkungen, die im Vorteilsplan definiert sind.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-175">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="0fb3d-176">Auswahl in Talent</span><span class="sxs-lookup"><span data-stu-id="0fb3d-176">Selection in Talent</span></span>        | <span data-ttu-id="0fb3d-177">Ergebnis in Dayforce</span><span class="sxs-lookup"><span data-stu-id="0fb3d-177">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="0fb3d-178">None</span><span class="sxs-lookup"><span data-stu-id="0fb3d-178">None</span></span>                       | <span data-ttu-id="0fb3d-179">Es wird kein Abzug erstellt.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-179">No deduction is created.</span></span>                      |
| <span data-ttu-id="0fb3d-180">Nur Abzug</span><span class="sxs-lookup"><span data-stu-id="0fb3d-180">Deduction only</span></span>             | <span data-ttu-id="0fb3d-181">Ein Mitarbeiterabzug wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-181">An employee deduction is created.</span></span>             |
| <span data-ttu-id="0fb3d-182">Nur Beitrag</span><span class="sxs-lookup"><span data-stu-id="0fb3d-182">Contribution only</span></span>          | <span data-ttu-id="0fb3d-183">Ein Arbeitgeberabzug wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-183">An employer deduction is created.</span></span>             |
| <span data-ttu-id="0fb3d-184">Abzug und Beitrag</span><span class="sxs-lookup"><span data-stu-id="0fb3d-184">Deduction and contribution</span></span> | <span data-ttu-id="0fb3d-185">Mitarbeiter- und Arbeitgeberabzüge werden erstellt.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-185">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="0fb3d-186">Weitere Informationen darüber, wie Sie ein Vorteilsprogramm definieren und verwalten finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="0fb3d-186">For more information about how to define and manage a benefits program, see the following topics:</span></span>

- [<span data-ttu-id="0fb3d-187">Mitarbeitervergütungsprogramm bereitstellen</span><span class="sxs-lookup"><span data-stu-id="0fb3d-187">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="0fb3d-188">Neuen Vorteil erstellen</span><span class="sxs-lookup"><span data-stu-id="0fb3d-188">Create a new benefit</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="0fb3d-189">Vorteilsberechtigungsregeln und Richtlinien definieren</span><span class="sxs-lookup"><span data-stu-id="0fb3d-189">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="0fb3d-190">Vorteile von Arbeitskräften registrieren und entfernen</span><span class="sxs-lookup"><span data-stu-id="0fb3d-190">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="0fb3d-191">Vergütung</span><span class="sxs-lookup"><span data-stu-id="0fb3d-191">Compensation</span></span> 

<span data-ttu-id="0fb3d-192">Die Vergütungsverwaltung dient zum Steuern der Abwicklung des Grundlohns und der Prämien.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-192">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="0fb3d-193">Sie steuern den festen Grundlohn eines Mitarbeiters und dessen Lohnsteigerungen nach Plänen für feste Vergütung.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-193">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="0fb3d-194">Die Zahlung leistungsbezogener Prämien, wie Boni, Leistungsprämien, Aktienoptionen und -überlassungen sowie Einmalprämien werden durch Pläne für variable Vergütung gesteuert.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-194">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="0fb3d-195">Dayforce verwendet Vergütungsinformationen, um einen Stunden- oder Jahressatz für einen Mitarbeiter zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-195">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="0fb3d-196">Feste Vergütungspläne und Lohnsatzumrechnungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-196">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="0fb3d-197">Mitarbeiter müssen einem festen Vergütungsplan zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-197">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="0fb3d-198">Weitere Informationen zu Vergütungsplänen finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="0fb3d-198">For more information about compensation plans, see the following topics:</span></span>

- [<span data-ttu-id="0fb3d-199">Feste Vergütungspläne erstellen</span><span class="sxs-lookup"><span data-stu-id="0fb3d-199">Create fixed compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="0fb3d-200">Variable Vergütungspläne erstellen</span><span class="sxs-lookup"><span data-stu-id="0fb3d-200">Create variable compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="0fb3d-201">Gehalts-/Vergütungsstruktur und -pläne entwickeln</span><span class="sxs-lookup"><span data-stu-id="0fb3d-201">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="0fb3d-202">Vergütung verarbeiten</span><span class="sxs-lookup"><span data-stu-id="0fb3d-202">Process compensation</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="0fb3d-203">Vergütungsprozess definieren und Ergebnisse berechnen</span><span class="sxs-lookup"><span data-stu-id="0fb3d-203">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="0fb3d-204">Einen Mitarbeiters in einem Plan für eine feste Vergütung registrieren</span><span class="sxs-lookup"><span data-stu-id="0fb3d-204">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="0fb3d-205">Einen Mitarbeiter in einem Plan für variable Vergütung registrieren</span><span class="sxs-lookup"><span data-stu-id="0fb3d-205">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="0fb3d-206">Stellentyp</span><span class="sxs-lookup"><span data-stu-id="0fb3d-206">Jobs</span></span> 

<span data-ttu-id="0fb3d-207">Eine Stelle ist eine Sammlung der Aufgaben und Zuständigkeiten, die für eine Person, die eine Tätigkeit ausführt, obligatorisch sind.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-207">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="0fb3d-208">Weitere Informationen finden Sie in folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="0fb3d-208">For more information, see the following topics:</span></span>

- [<span data-ttu-id="0fb3d-209">Komponenten einer Stelle einrichten</span><span class="sxs-lookup"><span data-stu-id="0fb3d-209">Setting up the components of a job</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="0fb3d-210">Neue Einzelvorgänge definieren</span><span class="sxs-lookup"><span data-stu-id="0fb3d-210">Define new jobs</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="0fb3d-211">Positionen</span><span class="sxs-lookup"><span data-stu-id="0fb3d-211">Positions</span></span>

<span data-ttu-id="0fb3d-212">Eine Position ist eine einzelne Instanz eines Einzelvorgangs.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-212">A position is an individual instance of a job.</span></span> <span data-ttu-id="0fb3d-213">Beispielsweise ist die Position „Verkaufsleiter (Ost)” eine der Positionen, die der Stelle „Verkaufsleiter” zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-213">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="0fb3d-214">Eine Position ist in einer Abteilung vorhanden.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-214">A position exists in a department.</span></span> <span data-ttu-id="0fb3d-215">Nur jeweils eine Arbeitskraft kann jeder Position zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-215">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="0fb3d-216">Bedenken Sie die folgenden Daten und Konfigurationen, wenn Sie Positionen einrichten:</span><span class="sxs-lookup"><span data-stu-id="0fb3d-216">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="0fb3d-217">Position (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-217">Position (required)</span></span>
- <span data-ttu-id="0fb3d-218">Beschreibung (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-218">Description (required)</span></span>
- <span data-ttu-id="0fb3d-219">Stelle (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-219">Job (required)</span></span>
- <span data-ttu-id="0fb3d-220">Abteilung (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-220">Department (required)</span></span>
- <span data-ttu-id="0fb3d-221">Positionstyp (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-221">Position type (required)</span></span>
- <span data-ttu-id="0fb3d-222">Vollzeitäquivalent</span><span class="sxs-lookup"><span data-stu-id="0fb3d-222">Full-time equivalent</span></span>
- <span data-ttu-id="0fb3d-223">Normale Stunden pro Jahr (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-223">Annual regular hours (required)</span></span>
- <span data-ttu-id="0fb3d-224">Gezahlt von der juristischen Person (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-224">Paid by legal entity (required)</span></span>
- <span data-ttu-id="0fb3d-225">Lohnzyklus (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-225">Pay cycle (required)</span></span>
- <span data-ttu-id="0fb3d-226">Standardfinanzdimension – Kostenstelle (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-226">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="0fb3d-227">Arbeitskraftzuweisung – Arbeitskraft, Zuweisungsanfang, Zuweisungsende, Ursachencode</span><span class="sxs-lookup"><span data-stu-id="0fb3d-227">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="0fb3d-228">Wenn mehrere Positionen in derselben Abteilung derselben Stelle zugeordnet sind, werden sie in einer einzelnen Position in Dayforce konsolidiert.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-228">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="0fb3d-229">Weitere Informationen finden Sie in folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="0fb3d-229">For more information, see the following topics:</span></span>

- [<span data-ttu-id="0fb3d-230">Organisieren der Belegschaft anhand von Abteilungen, Stellen und Positionen</span><span class="sxs-lookup"><span data-stu-id="0fb3d-230">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="0fb3d-231">Positionen einrichten</span><span class="sxs-lookup"><span data-stu-id="0fb3d-231">Set up positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="0fb3d-232">Abteilungen</span><span class="sxs-lookup"><span data-stu-id="0fb3d-232">Departments</span></span>

<span data-ttu-id="0fb3d-233">Eine Abteilung ist eine Organisationseinheit, die eine Kategorie oder einen funktionalen Bereich einer Organisation darstellt.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-233">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="0fb3d-234">Eine Abteilung ist für einen bestimmten Bereich der Organisation wie zum Beispiel Verkauf, Buchhaltung oder Personalverwaltung zuständig.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-234">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="0fb3d-235">Sie können Abteilungen verwenden, um zu Funktionsbereiche zu melden.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-235">You can use departments to report on functional areas.</span></span> <span data-ttu-id="0fb3d-236">Abteilungen können Gewinn- und Verlustzuständigkeit haben.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-236">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="0fb3d-237">Weitere Informationen finden Sie in folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="0fb3d-237">For more information, see the following topics:</span></span>

- [<span data-ttu-id="0fb3d-238">Eine Abteilung erstellen und der Abteilungshierarchie zuordnen</span><span class="sxs-lookup"><span data-stu-id="0fb3d-238">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="0fb3d-239">Neue Abteilungen definieren</span><span class="sxs-lookup"><span data-stu-id="0fb3d-239">Define new departments</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="0fb3d-240">Lohnzyklen und Lohnperioden</span><span class="sxs-lookup"><span data-stu-id="0fb3d-240">Pay cycles and pay periods</span></span>

<span data-ttu-id="0fb3d-241">Ein Lohnzyklus bestimmt, wie oft Lohn ausgezahlt wird, sowie die spezifischen Tage, an denen Arbeitskräfte bezahlt werden.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-241">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="0fb3d-242">Ein Lohnzyklus kann beispielsweise monatlich sein, und Mitarbeiter werden am letzten Tag des Monats bezahlt.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-242">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="0fb3d-243">Alternativ könnte ein Lohnzyklus wöchentlich sein, und Mitarbeiter werden am Dienstag nach Ende der Lohnperiode bezahlt.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-243">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="0fb3d-244">Lohnzyklen werden Positionen zugewiesen, um zu steuern, wann Mitarbeiter in diesen Positionen bezahlt werden.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-244">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="0fb3d-245">Nachdem Sie Lohnzyklen erstellen, können Sie Lohnperioden für jeden Zyklus generieren.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-245">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="0fb3d-246">Jede Lohnperiode enthält ein Standardzahlungsdatum, das auf den von Ihnen bereitgestellten Informationen basiert.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-246">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="0fb3d-247">Allerdings können Sie das Standardzahlungsdatum in einer Lohnperiode ändern, um Ausnahmen zuzulassen, wie beispielsweise wenn das Zahlungsdatum auf einen Feiertag fällt.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-247">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="0fb3d-248">Die folgenden Informationen werden in Dayforce verwendet:</span><span class="sxs-lookup"><span data-stu-id="0fb3d-248">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="0fb3d-249">Lohnzyklus (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-249">Pay cycle (required)</span></span>
- <span data-ttu-id="0fb3d-250">Lohnzyklushäufigkeit (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-250">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="0fb3d-251">Periodenstartdatum (erstes erforderliche Lohnperiode)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-251">Period start date (first pay period required)</span></span>
- <span data-ttu-id="0fb3d-252">Standardzahlungsdatum (erste erforderliche Lohnperiode)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-252">Default payment date (first pay period required)</span></span>

<span data-ttu-id="0fb3d-253">Diese Informationen werden mit Dayforce als Lohngruppen integriert und sind nach Land oder Region für jeden Lohnzyklus getrennt.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-253">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="0fb3d-254">Es muss mindestens eine Lohnperiode vor der Integration generiert werden.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-254">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="0fb3d-255">Dayforce generiert Lohngruppenkalender und Zahlungsdaten basierend auf dem Anfangsdatum der ersten Lohnperiode und dem Standardzahlungsdatums, das in Talent eingerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-255">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Talent.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="0fb3d-256">Einkommenscodes</span><span class="sxs-lookup"><span data-stu-id="0fb3d-256">Earning codes</span></span>

<span data-ttu-id="0fb3d-257">Einkommenscodes bestimmen jeden Typ von Einkünften eindeutig, die Arbeitskräfte erhalten</span><span class="sxs-lookup"><span data-stu-id="0fb3d-257">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="0fb3d-258">Die Codes haben verschiedene Parameter, die sich auf Einkünfte beziehen, wie beispielsweise Buchhaltungsvorschriften, Steuergesetze, Berichterstellungsanforderungen und Bruttoausgleichsfähigkeit.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-258">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="0fb3d-259">Die folgenden Informationen werden in Dayforce verwendet:</span><span class="sxs-lookup"><span data-stu-id="0fb3d-259">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="0fb3d-260">Einkommenscode (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-260">Earning Code (required)</span></span>
- <span data-ttu-id="0fb3d-261">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0fb3d-261">Description</span></span>
- <span data-ttu-id="0fb3d-262">Maßeinheit</span><span class="sxs-lookup"><span data-stu-id="0fb3d-262">Unit of measure</span></span>
- <span data-ttu-id="0fb3d-263">Produktiv</span><span class="sxs-lookup"><span data-stu-id="0fb3d-263">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="0fb3d-264">Arbeitskraftdaten</span><span class="sxs-lookup"><span data-stu-id="0fb3d-264">Worker data</span></span>

<span data-ttu-id="0fb3d-265">Datensätze für die verschiedenen Arten von Arbeitskräften, die Sie haben, sind für Ihre Personalverwaltung- sowie für Ihre Lohnsysteme von Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-265">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="0fb3d-266">Anhand der eingegebenen Informationen lassen sich Arbeitskräfte sowie personenbezogene Informationen nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-266">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="0fb3d-267">Sie können die folgenden Informationen für Arbeitskräfte verwalten:</span><span class="sxs-lookup"><span data-stu-id="0fb3d-267">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="0fb3d-268">**Basis** – Verwalten grundlegender Informationen über eine Arbeitskraft, beispielsweise Kontaktinformationen, demografische Informationen, Kennungsinformationen, Familieninformationen, Militärdienststatus, Ausländerinformationen sowie personenbezogene und Notfallkontakte.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-268">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="0fb3d-269">**Beschäftigung** – Verwalten von Informationen zum Beschäftigungsverhältnis einer Arbeitskraft, wie Unternehmens- oder Organisationszugehörigkeit, Positionszuweisung, Start- und Enddatum, Arbeitsberechtigung, Beschäftigungsbedingungen, Rente, Urlaub und Versetzungen.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-269">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="0fb3d-270">**Urlaub und Abwesenheit** – Verwalten von Informationen zur Abwesenheit einer Arbeitskraft, beispielsweise Arbeitszeitkalender, Abwesenheitsbuchungen und Abwesenheitseinrichtung.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-270">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="0fb3d-271">**Vergütung und Lohn** – Verwalten von Informationen zu den Vergütungsplänen und Lohndaten einer Arbeitskraft, wie der Planregistrierung, Boni, Leistung, Provision, Steuerdaten, Pensionierung und Gehaltsabzüge.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-271">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="0fb3d-272">Wenn Sie Arbeitskraftinformationen eingeben, sollten Sie folgende Daten und Konfigurationen bedenken, die in Dayforce verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-272">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="0fb3d-273">Allgemeine Angaben</span><span class="sxs-lookup"><span data-stu-id="0fb3d-273">General information</span></span>

- <span data-ttu-id="0fb3d-274">Personalnummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-274">Personnel number (required)</span></span>
- <span data-ttu-id="0fb3d-275">Vorname (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-275">First name (required)</span></span>
- <span data-ttu-id="0fb3d-276">Nachname (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-276">Last name (required)</span></span>
- <span data-ttu-id="0fb3d-277">Zweiter Vorname</span><span class="sxs-lookup"><span data-stu-id="0fb3d-277">Middle name</span></span>
- <span data-ttu-id="0fb3d-278">Dienstalterdatum</span><span class="sxs-lookup"><span data-stu-id="0fb3d-278">Seniority date</span></span>
- <span data-ttu-id="0fb3d-279">Bekannt als</span><span class="sxs-lookup"><span data-stu-id="0fb3d-279">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="0fb3d-280">Personenbezogene Informationen</span><span class="sxs-lookup"><span data-stu-id="0fb3d-280">Personal information</span></span>

- <span data-ttu-id="0fb3d-281">Familienstand (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-281">Marital status (required)</span></span>
- <span data-ttu-id="0fb3d-282">Geburtsdatum (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-282">Birth date (required)</span></span>
- <span data-ttu-id="0fb3d-283">Geschlecht (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-283">Gender (required)</span></span>
- <span data-ttu-id="0fb3d-284">Person mit Behinderung</span><span class="sxs-lookup"><span data-stu-id="0fb3d-284">Person with disabilities</span></span>
- <span data-ttu-id="0fb3d-285">Nationalitätsland/-region (nur für Mexiko)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-285">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="0fb3d-286">Adressdaten</span><span class="sxs-lookup"><span data-stu-id="0fb3d-286">Address information</span></span>

- <span data-ttu-id="0fb3d-287">Primär (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-287">Primary (required)</span></span>
- <span data-ttu-id="0fb3d-288">Land/Region (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-288">Country/region (required)</span></span>
- <span data-ttu-id="0fb3d-289">Postleitzahl (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-289">Postal code (required)</span></span>
- <span data-ttu-id="0fb3d-290">Hausnummer (erforderlich) (nur für Mexiko)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-290">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="0fb3d-291">Gebäudeergänzung (nur für Mexiko)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-291">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="0fb3d-292">Ort (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-292">City (required)</span></span>
- <span data-ttu-id="0fb3d-293">Bundesland/Kanton (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-293">State (required)</span></span>
- <span data-ttu-id="0fb3d-294">Landkreis (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-294">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="0fb3d-295">Kontaktdaten</span><span class="sxs-lookup"><span data-stu-id="0fb3d-295">Contact information</span></span> 

- <span data-ttu-id="0fb3d-296">Primär (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-296">Primary (required)</span></span>
- <span data-ttu-id="0fb3d-297">Kontaktnummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-297">Contact number (required)</span></span>
- <span data-ttu-id="0fb3d-298">Durchwahl</span><span class="sxs-lookup"><span data-stu-id="0fb3d-298">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="0fb3d-299">Lohndaten und Einkommenscodes</span><span class="sxs-lookup"><span data-stu-id="0fb3d-299">Payroll information and earning codes</span></span>

<span data-ttu-id="0fb3d-300">Mitarbeitern müssen bestimmte Einkommen mit einer bestimmten Zahlungshäufigkeit zugewiesen werden und sie müssen eine bevorzugte Zahlungsmethode haben.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-300">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="0fb3d-301">Die folgenden Felder werden in Dayforce verwendet, um zu gewährleisten, dass diese Voreinstellungen und Einstellungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-301">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="0fb3d-302">Einkommenscodes</span><span class="sxs-lookup"><span data-stu-id="0fb3d-302">Earning codes</span></span>

- <span data-ttu-id="0fb3d-303">Position (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-303">Position (required)</span></span>
- <span data-ttu-id="0fb3d-304">Einkommenscode (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-304">Earning Code (required)</span></span>
- <span data-ttu-id="0fb3d-305">Häufigkeit (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-305">Frequency (required)</span></span>
- <span data-ttu-id="0fb3d-306">Betrag (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-306">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="0fb3d-307">Lohndaten</span><span class="sxs-lookup"><span data-stu-id="0fb3d-307">Payroll information</span></span>

- <span data-ttu-id="0fb3d-308">Zahlungsmethode</span><span class="sxs-lookup"><span data-stu-id="0fb3d-308">Payment Method</span></span>
- <span data-ttu-id="0fb3d-309">Wirtschaftliche Region (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-309">Economic Region (required)</span></span>
- <span data-ttu-id="0fb3d-310">Mitarbeitervergütungs-ID</span><span class="sxs-lookup"><span data-stu-id="0fb3d-310">Employee Benefits ID</span></span>
- <span data-ttu-id="0fb3d-311">Personalausweisnummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-311">National ID Number (required)</span></span>
- <span data-ttu-id="0fb3d-312">Militärdienstnummer</span><span class="sxs-lookup"><span data-stu-id="0fb3d-312">Military Service Number</span></span>
- <span data-ttu-id="0fb3d-313">Schichtkennung (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-313">Shift ID (required)</span></span>
- <span data-ttu-id="0fb3d-314">Steuernummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-314">Tax Number (required)</span></span>
- <span data-ttu-id="0fb3d-315">Gewerkschaftskennung (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-315">Union ID (required)</span></span>
- <span data-ttu-id="0fb3d-316">Arbeitstagkennung (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-316">Work Day ID (required)</span></span>
- <span data-ttu-id="0fb3d-317">Arbeitserlaubnisnummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-317">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="0fb3d-318">Für die Zahlungsmethode unterstützt Mexiko **Bargeld**, **Scheck** (der physische Scheck des Unternehmens) und **Elektronische Zahlung**.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-318">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="0fb3d-319">Wenn keine Zahlungsmethode angegeben wird, wird **Scheck** standardmäßig verwendet.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-319">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="0fb3d-320">Anstellungsdetails</span><span class="sxs-lookup"><span data-stu-id="0fb3d-320">Employment details</span></span>

<span data-ttu-id="0fb3d-321">Beschäftigungsdetailhistorie wird als Schlüsselinformation verwendet, um die Status für Einstellung, Kündigung und erneute Einstellung in Dayforce abzuleiten.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-321">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="0fb3d-322">Dayforce unterstützt nur einen aktiven Beschäftigungsdatensatz gleichzeitig.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-322">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="0fb3d-323">Datum des Beschäftigungsbeginns (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-323">Employment start date (required)</span></span>
- <span data-ttu-id="0fb3d-324">Datum des Beschäftigungsendes</span><span class="sxs-lookup"><span data-stu-id="0fb3d-324">Employment end date</span></span>
- <span data-ttu-id="0fb3d-325">Eintrittstermin</span><span class="sxs-lookup"><span data-stu-id="0fb3d-325">Start date</span></span>
- <span data-ttu-id="0fb3d-326">Angepasster Tätigkeitsbeginn</span><span class="sxs-lookup"><span data-stu-id="0fb3d-326">Adjusted start date</span></span>
- <span data-ttu-id="0fb3d-327">Kündigungsdatum (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-327">Termination date (required upon termination)</span></span>
- <span data-ttu-id="0fb3d-328">Kündigungsgrund (erforderlich bei Kündigung)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-328">Termination reason (required upon termination)</span></span>

<span data-ttu-id="0fb3d-329">Die Schlüsseldaten eines Mitarbeiters werden abgeleitet, indem die folgenden Informationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-329">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="0fb3d-330">Talent</span><span class="sxs-lookup"><span data-stu-id="0fb3d-330">Talent</span></span>                | <span data-ttu-id="0fb3d-331">Dayforce</span><span class="sxs-lookup"><span data-stu-id="0fb3d-331">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fb3d-332">Aktuellstes Einstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="0fb3d-332">Most recent hire date</span></span> | <span data-ttu-id="0fb3d-333">Beschäftigungsbeginn des Verlaufsdatensatzes zur aktuellen, nicht gekündigten Beschäftigung</span><span class="sxs-lookup"><span data-stu-id="0fb3d-333">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="0fb3d-334">Kündigungsdatum</span><span class="sxs-lookup"><span data-stu-id="0fb3d-334">Termination date</span></span>      | <span data-ttu-id="0fb3d-335">Kündigungsdatum des Verlaufsdatensatzes zur aktuellen, nicht gekündigten Beschäftigung</span><span class="sxs-lookup"><span data-stu-id="0fb3d-335">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="0fb3d-336">Eintrittstermin</span><span class="sxs-lookup"><span data-stu-id="0fb3d-336">Start date</span></span>            | <span data-ttu-id="0fb3d-337">Angepasstes Startdatum, Startdatum oder Beschäftigungsbeginn des Verlaufsdatensatzes zur aktuellen, nicht aktiven Beschäftigung</span><span class="sxs-lookup"><span data-stu-id="0fb3d-337">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="0fb3d-338">Ursprüngliches Einstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="0fb3d-338">Original hire date</span></span>    | <span data-ttu-id="0fb3d-339">Beschäftigungsbeginn des frühesten Beschäftigungsverlaufsdatensatzes</span><span class="sxs-lookup"><span data-stu-id="0fb3d-339">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="0fb3d-340">Vergütung</span><span class="sxs-lookup"><span data-stu-id="0fb3d-340">Compensation</span></span>

<span data-ttu-id="0fb3d-341">Ein fester Vergütungsplan muss der primären Position jedes Mitarbeiters während einer Beschäftigungsperiode zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-341">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="0fb3d-342">Diese Periode beginnt mit dem Datum, an dem der Mitarbeiter eingestellt wurde (oder dem Datum des Beschäftigungsbeginns), und setzt sich bis zur Kündigung fort.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-342">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="0fb3d-343">Gültigkeitsdatum (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-343">Effective Date (required)</span></span>
- <span data-ttu-id="0fb3d-344">Ablaufdatum</span><span class="sxs-lookup"><span data-stu-id="0fb3d-344">Expiration date</span></span>
- <span data-ttu-id="0fb3d-345">Lohnsatz (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-345">Pay Rate (required)</span></span>
- <span data-ttu-id="0fb3d-346">Lohnsatzkonvertierungen (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-346">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="0fb3d-347">Jährliches Äquivalent (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-347">Annual equivalent (required)</span></span>
- <span data-ttu-id="0fb3d-348">Stündliches Äquivalent (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-348">Hourly equivalent (required)</span></span>

<span data-ttu-id="0fb3d-349">Wenn ein Mitarbeiter auf Stundenbasis mehrere Positionen hat, wird die feste Vergütung der primären Position in Dayforce als Basissatz/-gehalt auf Mitarbeiterebene importiert.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-349">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="0fb3d-350">Für nicht-primäre Positionen wird der Stundensatz in der entsprechenden Position in Dayforce gespeichert.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-350">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="0fb3d-351">Wenn ein Gehalt beziehender Mitarbeiter mehrere Positionen hat, wird der kumulative Stundensatz und das Jahresgehalt über alle aktiven Positionen hinweg abgeleitet und als Basissatz/-gehalt auf Arbeitnehmerebene verwendet.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-351">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="0fb3d-352">Kennnummern</span><span class="sxs-lookup"><span data-stu-id="0fb3d-352">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="0fb3d-353">Sozialversicherungsbezeichner</span><span class="sxs-lookup"><span data-stu-id="0fb3d-353">Social Security identifier</span></span> 

<span data-ttu-id="0fb3d-354">Jeder Mitarbeiter muss einen primären Bezeichner haben.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-354">Every employee must have one primary identifier.</span></span> <span data-ttu-id="0fb3d-355">Dieser Bezeichner muss vom Kennungstyp **P.Reg.Nr.** sein.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-355">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="0fb3d-356">In Dayforce wird er automatisch als Sozialversicherungsbezeichner des Mitarbeiters abgeleitet, der für die Einstellung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-356">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="0fb3d-357">Primär (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-357">Primary (required)</span></span>
- <span data-ttu-id="0fb3d-358">Kennungstyp = „P.Reg.Nr.”</span><span class="sxs-lookup"><span data-stu-id="0fb3d-358">Identification Type = "SSN"</span></span>
- <span data-ttu-id="0fb3d-359">Ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="0fb3d-359">Issued Date</span></span>
- <span data-ttu-id="0fb3d-360">Ablaufdatum</span><span class="sxs-lookup"><span data-stu-id="0fb3d-360">Expiration Date</span></span>

<span data-ttu-id="0fb3d-361">Mitarbeiter können mehrere Kennungsnummern des Kennungstyps **P.Reg.Nr.** melden.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-361">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="0fb3d-362">Jedoch wird nur der Datensatz, der als **Primär** markiert ist, in Dayforce integriert, unabhängig davon, ob die Nummer aktiv oder abgelaufen ist.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-362">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="0fb3d-363">Bankkonten und Auszahlungen</span><span class="sxs-lookup"><span data-stu-id="0fb3d-363">Bank accounts and disbursements</span></span>

<span data-ttu-id="0fb3d-364">Gültige Bankkontoinformationen müssen für jeden Mitarbeiter eingegeben werden, der per Bankkontoüberweisungen bezahlt werden möchte.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-364">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="0fb3d-365">Talent</span><span class="sxs-lookup"><span data-stu-id="0fb3d-365">Talent</span></span>                         | <span data-ttu-id="0fb3d-366">Dayforce</span><span class="sxs-lookup"><span data-stu-id="0fb3d-366">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fb3d-367">Bankkontonummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-367">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="0fb3d-368">SWIFT-Code (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-368">SWIFT code (required)</span></span>          | <span data-ttu-id="0fb3d-369">Feld **Bankkennung** wird verwendet, wenn Lohn in Mexiko verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-369">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="0fb3d-370">Filialnummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-370">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="0fb3d-371">Bankkontotyp (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-371">Bank account type (required)</span></span>   | <span data-ttu-id="0fb3d-372">Feld **Kontotyp** wird verwendet, wenn Lohn in Mexiko verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-372">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="0fb3d-373">Unterstützte Werte umfassen **Wird geprüft** und **Lohn**.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-373">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="0fb3d-374">Mitarbeiter, die per Bankkontoüberweisungen bezahlt werden möchten, müssen eine Verknüpfung zu einem Restbetrags-Bankkonto angeben, das sich unter einer juristischen Person befindet, deren primäre Adresse in Mexiko ist und das einem gültigen Bankkonto von einer mexikanischen Bank zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-374">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="0fb3d-375">Alle anderen Nicht-Restbetrags-Bankkonten werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-375">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="0fb3d-376">Adressdaten</span><span class="sxs-lookup"><span data-stu-id="0fb3d-376">Address information</span></span>

<span data-ttu-id="0fb3d-377">Jeder Mitarbeiter muss einen primären Standort haben.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-377">Every employee must have one primary location.</span></span> <span data-ttu-id="0fb3d-378">In Dayforce wird dieser Standort verwendet, um den primären Wohnsitz des Mitarbeiters für Steuerzwecke zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-378">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="0fb3d-379">Primär (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-379">Primary (required)</span></span>
- <span data-ttu-id="0fb3d-380">Land/Region (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-380">Country/region (required)</span></span>
- <span data-ttu-id="0fb3d-381">Postleitzahl (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-381">Zip/postal code (required)</span></span>
- <span data-ttu-id="0fb3d-382">Straße (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-382">Street (required)</span></span>
- <span data-ttu-id="0fb3d-383">Hausnummer (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-383">Street Number (required)</span></span>
- <span data-ttu-id="0fb3d-384">Gebäudeergänzung</span><span class="sxs-lookup"><span data-stu-id="0fb3d-384">Building Complement</span></span>
- <span data-ttu-id="0fb3d-385">Ort (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-385">City (required)</span></span>
- <span data-ttu-id="0fb3d-386">Bundesland/Kanton (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-386">State (required)</span></span>
- <span data-ttu-id="0fb3d-387">Landkreis (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-387">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="0fb3d-388">Konfigurieren Ihrer Daten, um Vergütung in den USA und Kanada zu generieren</span><span class="sxs-lookup"><span data-stu-id="0fb3d-388">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="0fb3d-389">Wenn Sie Vergütung für Mitarbeiter in den USA und Kanada generieren, müssen die folgenden Elemente konfiguriert werden:</span><span class="sxs-lookup"><span data-stu-id="0fb3d-389">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="0fb3d-390">Abteilungen sind für Positionen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-390">Departments are required on positions.</span></span>
- <span data-ttu-id="0fb3d-391">Kostenstellen müssen als Finanzdimensionen festgelegt werden und müssen das erste Element in der standardmäßigen Finanzdimensions-Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-391">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="0fb3d-392">Sie können Talent so konfigurieren, dass es anfordert, dass Positionen eine Abteilung angegeben.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-392">You can configure Talent to require that Positions specify a Department.</span></span> <span data-ttu-id="0fb3d-393">Dazu wechseln Sie zu **Freigegebene Positionen der Personalverwaltung > Positionen > Abteilungen zu Positionen anfordern**.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-393">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="0fb3d-394">Es wird empfohlen, dass diese Einstellungen für die Integration erzwungen wird.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-394">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="0fb3d-395">Stellentypen</span><span class="sxs-lookup"><span data-stu-id="0fb3d-395">Job types</span></span>

<span data-ttu-id="0fb3d-396">Stellentypen werden verwendet, um ähnliche Stellen in Kategorien zu gruppieren.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-396">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="0fb3d-397">Stellentypen sind erforderlich, damit Lohn in den USA und Kanada zu bearbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-397">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="0fb3d-398">Beispiele für Stellentypen umfassen Voll- und Teilzeit oder festes Gehalt und Stundenlohn.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-398">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="0fb3d-399">Stellentypen werden Dayforce als Lohnarten zugeordnet, die angeben, ob ein Mitarbeiter auf Stundenbasis bezahlt wird oder ein festes Gehalt bezieht.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-399">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="0fb3d-400">Folgende Stellentypen und Beschreibungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-400">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="0fb3d-401">Stellentyp</span><span class="sxs-lookup"><span data-stu-id="0fb3d-401">Job type</span></span>   | <span data-ttu-id="0fb3d-402">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0fb3d-402">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="0fb3d-403">Stündlich</span><span class="sxs-lookup"><span data-stu-id="0fb3d-403">Hourly</span></span>     | <span data-ttu-id="0fb3d-404">Stündlich</span><span class="sxs-lookup"><span data-stu-id="0fb3d-404">Hourly</span></span>      |
| <span data-ttu-id="0fb3d-405">Fest angestellt</span><span class="sxs-lookup"><span data-stu-id="0fb3d-405">Salaried</span></span>   | <span data-ttu-id="0fb3d-406">Fest angestellt</span><span class="sxs-lookup"><span data-stu-id="0fb3d-406">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="0fb3d-407">Positionstypen</span><span class="sxs-lookup"><span data-stu-id="0fb3d-407">Position types</span></span> 

<span data-ttu-id="0fb3d-408">Sie verwenden Positionstypen, um zu beschreiben, ob die Position Vollzeit, Teilzeit oder etwas anderes ist.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-408">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="0fb3d-409">Positionstypen werden Dayforce als Lohnklassen zugeordnet, die angeben, ob ein Mitarbeiter in Vollzeit oder Teilzeit arbeitet.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-409">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="0fb3d-410">Folgende Positionstypen und Beschreibungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-410">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="0fb3d-411">Positionstyp</span><span class="sxs-lookup"><span data-stu-id="0fb3d-411">Position type</span></span>   | <span data-ttu-id="0fb3d-412">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0fb3d-412">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="0fb3d-413">Vollzeit</span><span class="sxs-lookup"><span data-stu-id="0fb3d-413">Full-time</span></span>       | <span data-ttu-id="0fb3d-414">Vollzeitmitarbeiter</span><span class="sxs-lookup"><span data-stu-id="0fb3d-414">Full time employee</span></span> |
| <span data-ttu-id="0fb3d-415">Teilzeit</span><span class="sxs-lookup"><span data-stu-id="0fb3d-415">Part-time</span></span>       | <span data-ttu-id="0fb3d-416">Teilzeitmitarbeiter</span><span class="sxs-lookup"><span data-stu-id="0fb3d-416">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="0fb3d-417">Ursachencodes</span><span class="sxs-lookup"><span data-stu-id="0fb3d-417">Reason codes</span></span>

<span data-ttu-id="0fb3d-418">Ursachencodes enthalten Informationen zum Status eines Mitarbeiters.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-418">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="0fb3d-419">Ursachencodes werden Dayforce als Statusgründe zugeordnet, die den Grund für Änderungen bei der Position eines Mitarbeiters oder dem Beschäftigungsstatus angeben.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-419">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="0fb3d-420">Folgende Ursachencodes und Beschreibungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-420">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="0fb3d-421">Ursachencode</span><span class="sxs-lookup"><span data-stu-id="0fb3d-421">Reason code</span></span>    | <span data-ttu-id="0fb3d-422">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0fb3d-422">Description</span></span>      | <span data-ttu-id="0fb3d-423">Zutreffende Szenarios</span><span class="sxs-lookup"><span data-stu-id="0fb3d-423">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="0fb3d-424">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="0fb3d-424">RESIGNATION</span></span>    | <span data-ttu-id="0fb3d-425">Kündigung durch Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="0fb3d-425">Resignation</span></span>      | <span data-ttu-id="0fb3d-426">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="0fb3d-426">Terminate worker</span></span>     |
| <span data-ttu-id="0fb3d-427">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="0fb3d-427">TERMINATION</span></span>    | <span data-ttu-id="0fb3d-428">Beendigung</span><span class="sxs-lookup"><span data-stu-id="0fb3d-428">Termination</span></span>      | <span data-ttu-id="0fb3d-429">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="0fb3d-429">Terminate worker</span></span>     |
| <span data-ttu-id="0fb3d-430">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="0fb3d-430">RETIREMENT</span></span>     | <span data-ttu-id="0fb3d-431">Ruhestand</span><span class="sxs-lookup"><span data-stu-id="0fb3d-431">Retirement</span></span>       | <span data-ttu-id="0fb3d-432">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="0fb3d-432">Terminate worker</span></span>     |
| <span data-ttu-id="0fb3d-433">OTHER</span><span class="sxs-lookup"><span data-stu-id="0fb3d-433">OTHER</span></span>          | <span data-ttu-id="0fb3d-434">Andere Gründe</span><span class="sxs-lookup"><span data-stu-id="0fb3d-434">Other Reasons</span></span>    | <span data-ttu-id="0fb3d-435">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="0fb3d-435">Terminate worker</span></span>     |
| <span data-ttu-id="0fb3d-436">DEATH</span><span class="sxs-lookup"><span data-stu-id="0fb3d-436">DEATH</span></span>          | <span data-ttu-id="0fb3d-437">Tod</span><span class="sxs-lookup"><span data-stu-id="0fb3d-437">Death</span></span>            | <span data-ttu-id="0fb3d-438">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="0fb3d-438">Terminate worker</span></span>     |
| <span data-ttu-id="0fb3d-439">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="0fb3d-439">LEAVEOFABSENCE</span></span> | <span data-ttu-id="0fb3d-440">Beurlaubung</span><span class="sxs-lookup"><span data-stu-id="0fb3d-440">Leave of Absence</span></span> | <span data-ttu-id="0fb3d-441">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="0fb3d-441">Terminate worker</span></span>     |
| <span data-ttu-id="0fb3d-442">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="0fb3d-442">CONTRACTEND</span></span>    | <span data-ttu-id="0fb3d-443">Vertragsende</span><span class="sxs-lookup"><span data-stu-id="0fb3d-443">End of Contract</span></span>  | <span data-ttu-id="0fb3d-444">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="0fb3d-444">Terminate worker</span></span>     |
| <span data-ttu-id="0fb3d-445">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="0fb3d-445">SALARYCHANGE</span></span>   | <span data-ttu-id="0fb3d-446">Gehaltsänderung</span><span class="sxs-lookup"><span data-stu-id="0fb3d-446">Change of Salary</span></span> | <span data-ttu-id="0fb3d-447">Vergütung</span><span class="sxs-lookup"><span data-stu-id="0fb3d-447">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="0fb3d-448">Familienstand</span><span class="sxs-lookup"><span data-stu-id="0fb3d-448">Marital status</span></span>

<span data-ttu-id="0fb3d-449">Familienstandwerte werden Dayforce zugeordnet und werden – je nach Bedarf – in die akzeptierten Werte bei der Integration übersetzt.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-449">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="0fb3d-450">Die folgende Tabelle zeigt, wie Familienstandwerte Dayforce zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-450">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="0fb3d-451">Talent</span><span class="sxs-lookup"><span data-stu-id="0fb3d-451">Talent</span></span>                 | <span data-ttu-id="0fb3d-452">Dayforce</span><span class="sxs-lookup"><span data-stu-id="0fb3d-452">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="0fb3d-453">Verheiratet</span><span class="sxs-lookup"><span data-stu-id="0fb3d-453">Married</span></span>                | <span data-ttu-id="0fb3d-454">Verheiratet</span><span class="sxs-lookup"><span data-stu-id="0fb3d-454">Married</span></span>              |
| <span data-ttu-id="0fb3d-455">Ledig</span><span class="sxs-lookup"><span data-stu-id="0fb3d-455">Single</span></span>                 | <span data-ttu-id="0fb3d-456">Ledig</span><span class="sxs-lookup"><span data-stu-id="0fb3d-456">Single</span></span>               |
| <span data-ttu-id="0fb3d-457">Verwitwet</span><span class="sxs-lookup"><span data-stu-id="0fb3d-457">Widowed</span></span>                | <span data-ttu-id="0fb3d-458">Verwitwet</span><span class="sxs-lookup"><span data-stu-id="0fb3d-458">Widowed</span></span>              |
| <span data-ttu-id="0fb3d-459">Geschieden</span><span class="sxs-lookup"><span data-stu-id="0fb3d-459">Divorced</span></span>               | <span data-ttu-id="0fb3d-460">Geschieden</span><span class="sxs-lookup"><span data-stu-id="0fb3d-460">Divorced</span></span>             |
| <span data-ttu-id="0fb3d-461">Eingetragene Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="0fb3d-461">Registered Partnership</span></span> | <span data-ttu-id="0fb3d-462">Inländische Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="0fb3d-462">Domestic Partnership</span></span> |
| <span data-ttu-id="0fb3d-463">None</span><span class="sxs-lookup"><span data-stu-id="0fb3d-463">None</span></span>                   | <span data-ttu-id="0fb3d-464">None</span><span class="sxs-lookup"><span data-stu-id="0fb3d-464">None</span></span>                 |
| <span data-ttu-id="0fb3d-465">Freie Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="0fb3d-465">Cohabiting</span></span>             | <span data-ttu-id="0fb3d-466">Freie Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="0fb3d-466">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="0fb3d-467">Geschlecht</span><span class="sxs-lookup"><span data-stu-id="0fb3d-467">Gender</span></span>

<span data-ttu-id="0fb3d-468">Geschlechtsbezeichnungen werden Dayforce zugeordnet und werden – je nach Bedarf – in die akzeptierten Werte bei der Integration übersetzt.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-468">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="0fb3d-469">Die folgende Tabelle zeigt, wie Geschlechtsbezeichnungen Dayforce zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-469">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="0fb3d-470">Talent</span><span class="sxs-lookup"><span data-stu-id="0fb3d-470">Talent</span></span>       | <span data-ttu-id="0fb3d-471">Dayforce</span><span class="sxs-lookup"><span data-stu-id="0fb3d-471">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="0fb3d-472">Männlich</span><span class="sxs-lookup"><span data-stu-id="0fb3d-472">Male</span></span>         | <span data-ttu-id="0fb3d-473">Männlich</span><span class="sxs-lookup"><span data-stu-id="0fb3d-473">Male</span></span>            |
| <span data-ttu-id="0fb3d-474">Weiblich</span><span class="sxs-lookup"><span data-stu-id="0fb3d-474">Female</span></span>       | <span data-ttu-id="0fb3d-475">Weiblich</span><span class="sxs-lookup"><span data-stu-id="0fb3d-475">Female</span></span>          |
| <span data-ttu-id="0fb3d-476">Nicht spezifisch</span><span class="sxs-lookup"><span data-stu-id="0fb3d-476">Non-specific</span></span> | <span data-ttu-id="0fb3d-477">*Nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="0fb3d-477">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="0fb3d-478">Einkommenscodes</span><span class="sxs-lookup"><span data-stu-id="0fb3d-478">Earning codes</span></span>

<span data-ttu-id="0fb3d-479">Einkommenscodes bestimmen jeden Typ von Einkünften eindeutig, die Arbeitskräfte erhalten</span><span class="sxs-lookup"><span data-stu-id="0fb3d-479">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="0fb3d-480">Die Codes decken verschiedene Parameter ab, die sich auf Einkünfte beziehen, wie beispielsweise Buchhaltungsvorschriften, Steuergesetze, Berichterstellungsanforderungen und Bruttoausgleichsfähigkeit.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-480">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="0fb3d-481">Wenn eine nicht unterstützte Häufigkeit verwendet wird, wird die Häufigkeit **Jeder Lohn** standardmäßig für die Berechnung verwendet.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-481">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="0fb3d-482">Unterstützte Häufigkeiten</span><span class="sxs-lookup"><span data-stu-id="0fb3d-482">Supported frequencies</span></span>

- <span data-ttu-id="0fb3d-483">Alle</span><span class="sxs-lookup"><span data-stu-id="0fb3d-483">All</span></span>
- <span data-ttu-id="0fb3d-484">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="0fb3d-484">EVERYPAY</span></span>
- <span data-ttu-id="0fb3d-485">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="0fb3d-485">EACHPAYPERIOD</span></span>
- <span data-ttu-id="0fb3d-486">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="0fb3d-486">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="0fb3d-487">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="0fb3d-487">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="0fb3d-488">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="0fb3d-488">1OFMTH</span></span>
- <span data-ttu-id="0fb3d-489">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="0fb3d-489">LASTOFMTH</span></span>
- <span data-ttu-id="0fb3d-490">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="0fb3d-490">2OFMTH</span></span>
- <span data-ttu-id="0fb3d-491">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="0fb3d-491">3OFMTH</span></span>
- <span data-ttu-id="0fb3d-492">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0fb3d-492">4OFMTH</span></span>
- <span data-ttu-id="0fb3d-493">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="0fb3d-493">5OFMTH</span></span>
- <span data-ttu-id="0fb3d-494">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="0fb3d-494">1N2OFMTH</span></span>
- <span data-ttu-id="0fb3d-495">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0fb3d-495">3N4OFMTH</span></span>
- <span data-ttu-id="0fb3d-496">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="0fb3d-496">1N3OFMTH</span></span>
- <span data-ttu-id="0fb3d-497">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0fb3d-497">1N4OFMTH</span></span>
- <span data-ttu-id="0fb3d-498">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="0fb3d-498">2N3OFMTH</span></span>
- <span data-ttu-id="0fb3d-499">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0fb3d-499">2N4OFMTH</span></span>
- <span data-ttu-id="0fb3d-500">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="0fb3d-500">1N2N3OFMTH</span></span>
- <span data-ttu-id="0fb3d-501">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0fb3d-501">1N2N4OFMTH</span></span>
- <span data-ttu-id="0fb3d-502">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0fb3d-502">1N3N4OFMTH</span></span>
- <span data-ttu-id="0fb3d-503">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0fb3d-503">2N3N4OFMTH</span></span>
- <span data-ttu-id="0fb3d-504">1N2N3N4OFMTH – 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0fb3d-504">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="0fb3d-505">2N3N4N5OFMth – 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="0fb3d-505">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="0fb3d-506">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="0fb3d-506">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="0fb3d-507">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="0fb3d-507">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="0fb3d-508">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="0fb3d-508">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="0fb3d-509">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="0fb3d-509">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="0fb3d-510">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="0fb3d-510">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="0fb3d-511">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="0fb3d-511">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="0fb3d-512">Adressen</span><span class="sxs-lookup"><span data-stu-id="0fb3d-512">Addresses</span></span>

<span data-ttu-id="0fb3d-513">Die Kennung bestimmter Codes für Land oder Region, Bundesland/Kanton oder Landkreis (Gemeinde) erfordert spezifische Formate, die Dayforce und Anbieter innerhalb des Landes/innerhalb der Region erkennen können.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-513">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="0fb3d-514">Obwohl das Format für Orte flexibel ist, muss jeder Ort einem Bundesland zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-514">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="0fb3d-515">Talent</span><span class="sxs-lookup"><span data-stu-id="0fb3d-515">Talent</span></span>          | <span data-ttu-id="0fb3d-516">Dayforce</span><span class="sxs-lookup"><span data-stu-id="0fb3d-516">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="0fb3d-517">Land/Region</span><span class="sxs-lookup"><span data-stu-id="0fb3d-517">Country/Region</span></span>  | <span data-ttu-id="0fb3d-518">Ländercode</span><span class="sxs-lookup"><span data-stu-id="0fb3d-518">Country Code</span></span>          |
| <span data-ttu-id="0fb3d-519">Postleitzahl</span><span class="sxs-lookup"><span data-stu-id="0fb3d-519">Zip/Postal Code</span></span> | <span data-ttu-id="0fb3d-520">PLZ</span><span class="sxs-lookup"><span data-stu-id="0fb3d-520">Postal Code</span></span>           |
| <span data-ttu-id="0fb3d-521">Zustand</span><span class="sxs-lookup"><span data-stu-id="0fb3d-521">State</span></span>           | <span data-ttu-id="0fb3d-522">Bundeslandcode</span><span class="sxs-lookup"><span data-stu-id="0fb3d-522">State Code</span></span>            |
| <span data-ttu-id="0fb3d-523">Stadt</span><span class="sxs-lookup"><span data-stu-id="0fb3d-523">City</span></span>            | <span data-ttu-id="0fb3d-524">Stadt</span><span class="sxs-lookup"><span data-stu-id="0fb3d-524">City</span></span>                  |
| <span data-ttu-id="0fb3d-525">Verwaltungsbezirk</span><span class="sxs-lookup"><span data-stu-id="0fb3d-525">County</span></span>          | <span data-ttu-id="0fb3d-526">Landkreis (Gemeinde)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-526">County (Municipality)</span></span> |
| <span data-ttu-id="0fb3d-527">Straße</span><span class="sxs-lookup"><span data-stu-id="0fb3d-527">Street</span></span>          | <span data-ttu-id="0fb3d-528">Adresszeile 1</span><span class="sxs-lookup"><span data-stu-id="0fb3d-528">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="0fb3d-529">Steuerregionen</span><span class="sxs-lookup"><span data-stu-id="0fb3d-529">Tax regions</span></span>

<span data-ttu-id="0fb3d-530">Steuerregionen werden verwendet, um die entsprechende Steuer festzulegen, die bei der Lohngenerierung angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-530">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="0fb3d-531">Steuerregionen werden Dayforce als Standortadressen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-531">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="0fb3d-532">Die Standardsteuerregion muss der aktiven Position der Arbeitskraft zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-532">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="0fb3d-533">Steuerregion (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-533">Tax region (required)</span></span>
- <span data-ttu-id="0fb3d-534">Land/Region (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-534">Country/Region (required)</span></span>
- <span data-ttu-id="0fb3d-535">Bundesland/Kanton (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-535">State (required)</span></span>
- <span data-ttu-id="0fb3d-536">Verwaltungsbezirk</span><span class="sxs-lookup"><span data-stu-id="0fb3d-536">County</span></span> 
- <span data-ttu-id="0fb3d-537">Ort (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-537">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="0fb3d-538">Konfigurieren Ihrer Daten, um Lohn in Mexiko zu generieren</span><span class="sxs-lookup"><span data-stu-id="0fb3d-538">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="0fb3d-539">Wenn Sie Vergütung für Mitarbeiter in Mexiko generieren, müssen die folgenden Elemente konfiguriert werden:</span><span class="sxs-lookup"><span data-stu-id="0fb3d-539">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="0fb3d-540">Abteilungen sind für Positionen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-540">Departments are required on positions.</span></span>
- <span data-ttu-id="0fb3d-541">Kostenstellen müssen als Finanzdimensionen festgelegt werden und müssen das erste Element in der standardmäßigen Finanzdimensions-Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-541">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="0fb3d-542">Stellentypen</span><span class="sxs-lookup"><span data-stu-id="0fb3d-542">Job types</span></span>

<span data-ttu-id="0fb3d-543">Stellentypen werden verwendet, um ähnliche Stellen in Kategorien zu gruppieren.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-543">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="0fb3d-544">Stellentypen sind erforderlich, um Lohn in Mexiko zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-544">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="0fb3d-545">Beispiele für Stellentypen umfassen Voll- und Teilzeit oder festes Gehalt und Stundenlohn.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-545">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="0fb3d-546">Stellentypen werden Dayforce als Lohnarten zugeordnet, die angeben, ob ein Mitarbeiter auf Stundenbasis bezahlt wird oder ein festes Gehalt bezieht.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-546">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="0fb3d-547">Folgende Stellentypen und Beschreibungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-547">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="0fb3d-548">Stellentyp</span><span class="sxs-lookup"><span data-stu-id="0fb3d-548">Job type</span></span>   | <span data-ttu-id="0fb3d-549">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0fb3d-549">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="0fb3d-550">Stündlich</span><span class="sxs-lookup"><span data-stu-id="0fb3d-550">Hourly</span></span>     | <span data-ttu-id="0fb3d-551">MX – Stundenbasis</span><span class="sxs-lookup"><span data-stu-id="0fb3d-551">MX Hourly</span></span>   |
| <span data-ttu-id="0fb3d-552">Fest angestellt</span><span class="sxs-lookup"><span data-stu-id="0fb3d-552">Salaried</span></span>   | <span data-ttu-id="0fb3d-553">MX – Fest angestellt</span><span class="sxs-lookup"><span data-stu-id="0fb3d-553">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="0fb3d-554">Positionstypen</span><span class="sxs-lookup"><span data-stu-id="0fb3d-554">Position types</span></span> 

<span data-ttu-id="0fb3d-555">Sie verwenden Positionstypen, um zu beschreiben, ob die Position Vollzeit, Teilzeit oder etwas anderes ist.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-555">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="0fb3d-556">Positionstypen werden Dayforce als Lohnklassen zugeordnet, die angeben, ob ein Mitarbeiter in Vollzeit oder Teilzeit arbeitet.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-556">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="0fb3d-557">Folgende Positionstypen und Beschreibungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-557">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="0fb3d-558">Positionstyp</span><span class="sxs-lookup"><span data-stu-id="0fb3d-558">Position type</span></span>   | <span data-ttu-id="0fb3d-559">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0fb3d-559">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="0fb3d-560">Vollzeit</span><span class="sxs-lookup"><span data-stu-id="0fb3d-560">Full-time</span></span>       | <span data-ttu-id="0fb3d-561">Vollzeitmitarbeiter</span><span class="sxs-lookup"><span data-stu-id="0fb3d-561">Full time employee</span></span> |
| <span data-ttu-id="0fb3d-562">Teilzeit</span><span class="sxs-lookup"><span data-stu-id="0fb3d-562">Part-time</span></span>       | <span data-ttu-id="0fb3d-563">Teilzeitmitarbeiter</span><span class="sxs-lookup"><span data-stu-id="0fb3d-563">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="0fb3d-564">Ursachencodes</span><span class="sxs-lookup"><span data-stu-id="0fb3d-564">Reason codes</span></span>

<span data-ttu-id="0fb3d-565">Ursachencodes enthalten Informationen zum Status eines Mitarbeiters.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-565">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="0fb3d-566">Ursachencodes werden Dayforce als Statusgründe zugeordnet, die den Grund für Änderungen bei der Position eines Mitarbeiters oder dem Beschäftigungsstatus angeben.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-566">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="0fb3d-567">Folgende Ursachencodes und Beschreibungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-567">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="0fb3d-568">Ursachencode</span><span class="sxs-lookup"><span data-stu-id="0fb3d-568">Reason code</span></span>            | <span data-ttu-id="0fb3d-569">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0fb3d-569">Description</span></span>                    | <span data-ttu-id="0fb3d-570">Zutreffende Szenarios</span><span class="sxs-lookup"><span data-stu-id="0fb3d-570">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="0fb3d-571">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="0fb3d-571">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="0fb3d-572">Abgang vor erster Lohnzahlung</span><span class="sxs-lookup"><span data-stu-id="0fb3d-572">Departure before first payroll</span></span> | <span data-ttu-id="0fb3d-573">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="0fb3d-573">Terminate worker</span></span>     |
| <span data-ttu-id="0fb3d-574">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="0fb3d-574">RESIGNATION</span></span>            | <span data-ttu-id="0fb3d-575">Kündigung durch Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="0fb3d-575">Resignation</span></span>                    | <span data-ttu-id="0fb3d-576">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="0fb3d-576">Terminate worker</span></span>     |
| <span data-ttu-id="0fb3d-577">PENSION</span><span class="sxs-lookup"><span data-stu-id="0fb3d-577">PENSION</span></span>                | <span data-ttu-id="0fb3d-578">Rente</span><span class="sxs-lookup"><span data-stu-id="0fb3d-578">Pension</span></span>                        | <span data-ttu-id="0fb3d-579">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="0fb3d-579">Terminate worker</span></span>     |
| <span data-ttu-id="0fb3d-580">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="0fb3d-580">TERMINATION</span></span>            | <span data-ttu-id="0fb3d-581">Beendigung</span><span class="sxs-lookup"><span data-stu-id="0fb3d-581">Termination</span></span>                    | <span data-ttu-id="0fb3d-582">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="0fb3d-582">Terminate worker</span></span>     |
| <span data-ttu-id="0fb3d-583">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="0fb3d-583">RETIREMENT</span></span>             | <span data-ttu-id="0fb3d-584">Ruhestand</span><span class="sxs-lookup"><span data-stu-id="0fb3d-584">Retirement</span></span>                     | <span data-ttu-id="0fb3d-585">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="0fb3d-585">Terminate worker</span></span>     |
| <span data-ttu-id="0fb3d-586">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="0fb3d-586">ABSENTEE</span></span>               | <span data-ttu-id="0fb3d-587">Abwesende Person</span><span class="sxs-lookup"><span data-stu-id="0fb3d-587">Absentee</span></span>                       | <span data-ttu-id="0fb3d-588">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="0fb3d-588">Terminate worker</span></span>     |
| <span data-ttu-id="0fb3d-589">OTHER</span><span class="sxs-lookup"><span data-stu-id="0fb3d-589">OTHER</span></span>                  | <span data-ttu-id="0fb3d-590">Andere Gründe</span><span class="sxs-lookup"><span data-stu-id="0fb3d-590">Other Reasons</span></span>                  | <span data-ttu-id="0fb3d-591">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="0fb3d-591">Terminate worker</span></span>     |
| <span data-ttu-id="0fb3d-592">CLOSURE</span><span class="sxs-lookup"><span data-stu-id="0fb3d-592">CLOSURE</span></span>                | <span data-ttu-id="0fb3d-593">Betriebsferien</span><span class="sxs-lookup"><span data-stu-id="0fb3d-593">Business Closure</span></span>               | <span data-ttu-id="0fb3d-594">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="0fb3d-594">Terminate worker</span></span>     |
| <span data-ttu-id="0fb3d-595">DEATH</span><span class="sxs-lookup"><span data-stu-id="0fb3d-595">DEATH</span></span>                  | <span data-ttu-id="0fb3d-596">Tod</span><span class="sxs-lookup"><span data-stu-id="0fb3d-596">Death</span></span>                          | <span data-ttu-id="0fb3d-597">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="0fb3d-597">Terminate worker</span></span>     |
| <span data-ttu-id="0fb3d-598">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="0fb3d-598">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="0fb3d-599">Beurlaubung</span><span class="sxs-lookup"><span data-stu-id="0fb3d-599">Leave of Absence</span></span>               | <span data-ttu-id="0fb3d-600">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="0fb3d-600">Terminate worker</span></span>     |
| <span data-ttu-id="0fb3d-601">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="0fb3d-601">CONTRACTEND</span></span>            | <span data-ttu-id="0fb3d-602">Vertragsende</span><span class="sxs-lookup"><span data-stu-id="0fb3d-602">End of Contract</span></span>                | <span data-ttu-id="0fb3d-603">Arbeitskraft kündigen</span><span class="sxs-lookup"><span data-stu-id="0fb3d-603">Terminate worker</span></span>     |
| <span data-ttu-id="0fb3d-604">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="0fb3d-604">SALARYCHANGE</span></span>           | <span data-ttu-id="0fb3d-605">Gehaltsänderung</span><span class="sxs-lookup"><span data-stu-id="0fb3d-605">Change of Salary</span></span>               | <span data-ttu-id="0fb3d-606">Vergütung</span><span class="sxs-lookup"><span data-stu-id="0fb3d-606">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="0fb3d-607">Einstellungsbedingungen</span><span class="sxs-lookup"><span data-stu-id="0fb3d-607">Terms of employment</span></span>

<span data-ttu-id="0fb3d-608">Beschäftigungsbedingungen werden verwendet, um Kategorien von Beschäftigungsbedingungen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-608">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="0fb3d-609">Die Bedingungen werden Dayforce als Beschäftigungsindikatorwerte zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-609">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="0fb3d-610">Die folgenden Bedingungen für Beschäftigung und Beschreibungen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-610">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="0fb3d-611">Einstellungsbedingungen</span><span class="sxs-lookup"><span data-stu-id="0fb3d-611">Terms of employment</span></span>   | <span data-ttu-id="0fb3d-612">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0fb3d-612">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="0fb3d-613">Regelmäßig</span><span class="sxs-lookup"><span data-stu-id="0fb3d-613">Regular</span></span>               | <span data-ttu-id="0fb3d-614">Regelmäßig</span><span class="sxs-lookup"><span data-stu-id="0fb3d-614">Regular</span></span>     |
| <span data-ttu-id="0fb3d-615">Direkt</span><span class="sxs-lookup"><span data-stu-id="0fb3d-615">Direct</span></span>                | <span data-ttu-id="0fb3d-616">Direkt</span><span class="sxs-lookup"><span data-stu-id="0fb3d-616">Direct</span></span>      |
| <span data-ttu-id="0fb3d-617">Praktikum</span><span class="sxs-lookup"><span data-stu-id="0fb3d-617">Internship</span></span>            | <span data-ttu-id="0fb3d-618">Praktikum</span><span class="sxs-lookup"><span data-stu-id="0fb3d-618">Internship</span></span>  |
| <span data-ttu-id="0fb3d-619">Unbefristet</span><span class="sxs-lookup"><span data-stu-id="0fb3d-619">Permanent</span></span>             | <span data-ttu-id="0fb3d-620">Unbefristet</span><span class="sxs-lookup"><span data-stu-id="0fb3d-620">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="0fb3d-621">Familienstand</span><span class="sxs-lookup"><span data-stu-id="0fb3d-621">Marital status</span></span>

<span data-ttu-id="0fb3d-622">Familienstandwerte werden Dayforce zugeordnet und werden – je nach Bedarf – in die akzeptierten Werte bei der Integration übersetzt.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-622">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="0fb3d-623">Die folgende Tabelle zeigt, wie Familienstandwerte Dayforce zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-623">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="0fb3d-624">Talent</span><span class="sxs-lookup"><span data-stu-id="0fb3d-624">Talent</span></span>                 | <span data-ttu-id="0fb3d-625">Dayforce</span><span class="sxs-lookup"><span data-stu-id="0fb3d-625">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="0fb3d-626">Verheiratet</span><span class="sxs-lookup"><span data-stu-id="0fb3d-626">Married</span></span>                | <span data-ttu-id="0fb3d-627">Verheiratet</span><span class="sxs-lookup"><span data-stu-id="0fb3d-627">Married</span></span>                   |
| <span data-ttu-id="0fb3d-628">Ledig</span><span class="sxs-lookup"><span data-stu-id="0fb3d-628">Single</span></span>                 | <span data-ttu-id="0fb3d-629">Ledig</span><span class="sxs-lookup"><span data-stu-id="0fb3d-629">Single</span></span>                    |
| <span data-ttu-id="0fb3d-630">Verwitwet</span><span class="sxs-lookup"><span data-stu-id="0fb3d-630">Widowed</span></span>                | <span data-ttu-id="0fb3d-631">Verwitwet</span><span class="sxs-lookup"><span data-stu-id="0fb3d-631">Widowed</span></span>                   |
| <span data-ttu-id="0fb3d-632">Geschieden</span><span class="sxs-lookup"><span data-stu-id="0fb3d-632">Divorced</span></span>               | <span data-ttu-id="0fb3d-633">Geschieden</span><span class="sxs-lookup"><span data-stu-id="0fb3d-633">Divorced</span></span>                  |
| <span data-ttu-id="0fb3d-634">Eingetragene Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="0fb3d-634">Registered Partnership</span></span> | <span data-ttu-id="0fb3d-635">Inländische Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="0fb3d-635">Domestic Partnership</span></span>      |
| <span data-ttu-id="0fb3d-636">None</span><span class="sxs-lookup"><span data-stu-id="0fb3d-636">None</span></span>                   | <span data-ttu-id="0fb3d-637">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="0fb3d-637">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="0fb3d-638">Freie Partnerschaft</span><span class="sxs-lookup"><span data-stu-id="0fb3d-638">Cohabiting</span></span>             | <span data-ttu-id="0fb3d-639">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="0fb3d-639">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="0fb3d-640">Geschlecht</span><span class="sxs-lookup"><span data-stu-id="0fb3d-640">Gender</span></span>

<span data-ttu-id="0fb3d-641">Geschlechtsbezeichnungen werden Dayforce zugeordnet und werden – je nach Bedarf – in die akzeptierten Werte bei der Integration übersetzt.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-641">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="0fb3d-642">Die folgende Tabelle zeigt, wie Geschlechtsbezeichnungen Dayforce zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-642">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="0fb3d-643">Talent</span><span class="sxs-lookup"><span data-stu-id="0fb3d-643">Talent</span></span>       | <span data-ttu-id="0fb3d-644">Dayforce</span><span class="sxs-lookup"><span data-stu-id="0fb3d-644">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="0fb3d-645">Männlich</span><span class="sxs-lookup"><span data-stu-id="0fb3d-645">Male</span></span>         | <span data-ttu-id="0fb3d-646">Männlich</span><span class="sxs-lookup"><span data-stu-id="0fb3d-646">Male</span></span>                      |
| <span data-ttu-id="0fb3d-647">Weiblich</span><span class="sxs-lookup"><span data-stu-id="0fb3d-647">Female</span></span>       | <span data-ttu-id="0fb3d-648">Weiblich</span><span class="sxs-lookup"><span data-stu-id="0fb3d-648">Female</span></span>                    |
| <span data-ttu-id="0fb3d-649">Nicht spezifisch</span><span class="sxs-lookup"><span data-stu-id="0fb3d-649">Non-specific</span></span> | <span data-ttu-id="0fb3d-650">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="0fb3d-650">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="0fb3d-651">Zahlungsweise</span><span class="sxs-lookup"><span data-stu-id="0fb3d-651">Payment method</span></span>

<span data-ttu-id="0fb3d-652">Zahlungsmethoden geben dem Mitarbeiter und dem Unternehmen die Möglichkeit zu beschreiben, wie Mitarbeiter bezahlt werden.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-652">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="0fb3d-653">Zahlungsmethoden werden Dayforce zugeordnet und werden – je nach Bedarf – in die akzeptierten Werte bei der Integration übersetzt.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-653">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="0fb3d-654">Die folgende Tabelle zeigt, wie Zahlungsmethoden Dayforce zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-654">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="0fb3d-655">Talent</span><span class="sxs-lookup"><span data-stu-id="0fb3d-655">Talent</span></span>             | <span data-ttu-id="0fb3d-656">Dayforce</span><span class="sxs-lookup"><span data-stu-id="0fb3d-656">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="0fb3d-657">Bargeld</span><span class="sxs-lookup"><span data-stu-id="0fb3d-657">Cash</span></span>               | <span data-ttu-id="0fb3d-658">Bargeld</span><span class="sxs-lookup"><span data-stu-id="0fb3d-658">Cash</span></span>                      |
| <span data-ttu-id="0fb3d-659">Elektronische Zahlung</span><span class="sxs-lookup"><span data-stu-id="0fb3d-659">Electronic Payment</span></span> | <span data-ttu-id="0fb3d-660">Übertragen</span><span class="sxs-lookup"><span data-stu-id="0fb3d-660">Transfer</span></span>                  |
| <span data-ttu-id="0fb3d-661">Scheck</span><span class="sxs-lookup"><span data-stu-id="0fb3d-661">Check</span></span>              | <span data-ttu-id="0fb3d-662">Scheck</span><span class="sxs-lookup"><span data-stu-id="0fb3d-662">Cheque</span></span>                    |
| <span data-ttu-id="0fb3d-663">Bankwechsel</span><span class="sxs-lookup"><span data-stu-id="0fb3d-663">Bank Draft</span></span>         | <span data-ttu-id="0fb3d-664">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="0fb3d-664">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="0fb3d-665">Sonstige</span><span class="sxs-lookup"><span data-stu-id="0fb3d-665">Other</span></span>              | <span data-ttu-id="0fb3d-666">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="0fb3d-666">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="0fb3d-667">Bankkontotyp</span><span class="sxs-lookup"><span data-stu-id="0fb3d-667">Bank account type</span></span>

<span data-ttu-id="0fb3d-668">Bankkontotypen werden für elektronische Zahlungen an Mitarbeiter verwendet.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-668">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="0fb3d-669">Bankkontotypen werden Dayforce als Übergweisungskontoinformationen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-669">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="0fb3d-670">Die Bankkontotypen werden bei Bedarf zu den akzeptierten Werte nach der Integration übersetzt.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-670">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="0fb3d-671">Talent</span><span class="sxs-lookup"><span data-stu-id="0fb3d-671">Talent</span></span>            | <span data-ttu-id="0fb3d-672">Dayforce</span><span class="sxs-lookup"><span data-stu-id="0fb3d-672">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="0fb3d-673">Girokonto</span><span class="sxs-lookup"><span data-stu-id="0fb3d-673">Checking Account</span></span>  | <span data-ttu-id="0fb3d-674">Girokonto</span><span class="sxs-lookup"><span data-stu-id="0fb3d-674">CheckingAccount</span></span>           |
| <span data-ttu-id="0fb3d-675">Lohnkonto</span><span class="sxs-lookup"><span data-stu-id="0fb3d-675">Payroll Account</span></span>   | <span data-ttu-id="0fb3d-676">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="0fb3d-676">PayrollAccount</span></span>            |
| <span data-ttu-id="0fb3d-677">Sparkonto</span><span class="sxs-lookup"><span data-stu-id="0fb3d-677">Savings Account</span></span>   | <span data-ttu-id="0fb3d-678">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="0fb3d-678">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="0fb3d-679">BankGirot-Konto</span><span class="sxs-lookup"><span data-stu-id="0fb3d-679">BankGirot account</span></span> | <span data-ttu-id="0fb3d-680">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="0fb3d-680">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="0fb3d-681">PlusGirot-Konto</span><span class="sxs-lookup"><span data-stu-id="0fb3d-681">PlusGirot account</span></span> | <span data-ttu-id="0fb3d-682">*Wird von Mexiko nicht unterstützt*</span><span class="sxs-lookup"><span data-stu-id="0fb3d-682">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="0fb3d-683">Einkommenscodes</span><span class="sxs-lookup"><span data-stu-id="0fb3d-683">Earning codes</span></span>

<span data-ttu-id="0fb3d-684">Einkommenscodes bestimmen jeden Typ von Einkünften eindeutig, die Arbeitskräfte erhalten</span><span class="sxs-lookup"><span data-stu-id="0fb3d-684">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="0fb3d-685">Die Codes decken verschiedene Parameter ab, die sich auf Einkünfte beziehen, wie beispielsweise Buchhaltungsvorschriften, Steuergesetze, Berichterstellungsanforderungen und Bruttoausgleichsfähigkeit.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-685">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="0fb3d-686">Wenn eine nicht unterstützte Häufigkeit verwendet wird, wird die Häufigkeit **Jeder Lohn** standardmäßig für die Berechnung verwendet.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-686">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="0fb3d-687">Unterstützte Häufigkeiten</span><span class="sxs-lookup"><span data-stu-id="0fb3d-687">Supported frequencies</span></span>

- <span data-ttu-id="0fb3d-688">Alle</span><span class="sxs-lookup"><span data-stu-id="0fb3d-688">All</span></span>
- <span data-ttu-id="0fb3d-689">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="0fb3d-689">EVERYPAY</span></span>
- <span data-ttu-id="0fb3d-690">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="0fb3d-690">EACHPAYPERIOD</span></span>
- <span data-ttu-id="0fb3d-691">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="0fb3d-691">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="0fb3d-692">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="0fb3d-692">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="0fb3d-693">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="0fb3d-693">1OFMTH</span></span>
- <span data-ttu-id="0fb3d-694">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="0fb3d-694">LASTOFMTH</span></span>
- <span data-ttu-id="0fb3d-695">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="0fb3d-695">2OFMTH</span></span>
- <span data-ttu-id="0fb3d-696">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="0fb3d-696">3OFMTH</span></span>
- <span data-ttu-id="0fb3d-697">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0fb3d-697">4OFMTH</span></span>
- <span data-ttu-id="0fb3d-698">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="0fb3d-698">5OFMTH</span></span>
- <span data-ttu-id="0fb3d-699">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="0fb3d-699">1N2OFMTH</span></span>
- <span data-ttu-id="0fb3d-700">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0fb3d-700">3N4OFMTH</span></span>
- <span data-ttu-id="0fb3d-701">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="0fb3d-701">1N3OFMTH</span></span>
- <span data-ttu-id="0fb3d-702">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0fb3d-702">1N4OFMTH</span></span>
- <span data-ttu-id="0fb3d-703">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="0fb3d-703">2N3OFMTH</span></span>
- <span data-ttu-id="0fb3d-704">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0fb3d-704">2N4OFMTH</span></span>
- <span data-ttu-id="0fb3d-705">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="0fb3d-705">1N2N3OFMTH</span></span>
- <span data-ttu-id="0fb3d-706">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0fb3d-706">1N2N4OFMTH</span></span>
- <span data-ttu-id="0fb3d-707">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0fb3d-707">1N3N4OFMTH</span></span>
- <span data-ttu-id="0fb3d-708">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0fb3d-708">2N3N4OFMTH</span></span>
- <span data-ttu-id="0fb3d-709">1N2N3N4OFMTH – 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="0fb3d-709">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="0fb3d-710">2N3N4N5OFMth – 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="0fb3d-710">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="0fb3d-711">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="0fb3d-711">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="0fb3d-712">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="0fb3d-712">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="0fb3d-713">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="0fb3d-713">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="0fb3d-714">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="0fb3d-714">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="0fb3d-715">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="0fb3d-715">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="0fb3d-716">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="0fb3d-716">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="0fb3d-717">Adressen</span><span class="sxs-lookup"><span data-stu-id="0fb3d-717">Addresses</span></span>

<span data-ttu-id="0fb3d-718">Die Kennung bestimmter Codes für Land oder Region, Bundesland/Kanton oder Landkreis (Gemeinde) erfordert spezifische Formate, die Dayforce und Anbieter innerhalb des Landes/innerhalb der Region erkennen können.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-718">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="0fb3d-719">Obwohl das Format für Orte flexibel ist, muss jeder Ort einem Bundesland zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-719">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="0fb3d-720">Talent</span><span class="sxs-lookup"><span data-stu-id="0fb3d-720">Talent</span></span>              | <span data-ttu-id="0fb3d-721">Dayforce</span><span class="sxs-lookup"><span data-stu-id="0fb3d-721">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="0fb3d-722">Land/Region</span><span class="sxs-lookup"><span data-stu-id="0fb3d-722">Country/Region</span></span>      | <span data-ttu-id="0fb3d-723">Ländercode</span><span class="sxs-lookup"><span data-stu-id="0fb3d-723">Country Code</span></span>          |
| <span data-ttu-id="0fb3d-724">Postleitzahl</span><span class="sxs-lookup"><span data-stu-id="0fb3d-724">Zip/Postal Code</span></span>     | <span data-ttu-id="0fb3d-725">PLZ</span><span class="sxs-lookup"><span data-stu-id="0fb3d-725">Postal Code</span></span>           |
| <span data-ttu-id="0fb3d-726">Zustand</span><span class="sxs-lookup"><span data-stu-id="0fb3d-726">State</span></span>               | <span data-ttu-id="0fb3d-727">Bundeslandcode</span><span class="sxs-lookup"><span data-stu-id="0fb3d-727">State Code</span></span>            |
| <span data-ttu-id="0fb3d-728">Stadt</span><span class="sxs-lookup"><span data-stu-id="0fb3d-728">City</span></span>                | <span data-ttu-id="0fb3d-729">Stadt</span><span class="sxs-lookup"><span data-stu-id="0fb3d-729">City</span></span>                  |
| <span data-ttu-id="0fb3d-730">Verwaltungsbezirk</span><span class="sxs-lookup"><span data-stu-id="0fb3d-730">County</span></span>              | <span data-ttu-id="0fb3d-731">Landkreis (Gemeinde)</span><span class="sxs-lookup"><span data-stu-id="0fb3d-731">County (Municipality)</span></span> |
| <span data-ttu-id="0fb3d-732">Straße</span><span class="sxs-lookup"><span data-stu-id="0fb3d-732">Street</span></span>              | <span data-ttu-id="0fb3d-733">Adresszeile 1</span><span class="sxs-lookup"><span data-stu-id="0fb3d-733">Address Line 1</span></span>        |
| <span data-ttu-id="0fb3d-734">Hausnummer</span><span class="sxs-lookup"><span data-stu-id="0fb3d-734">Street Number</span></span>       | <span data-ttu-id="0fb3d-735">Adresszeile 2</span><span class="sxs-lookup"><span data-stu-id="0fb3d-735">Address Line 2</span></span>        |
| <span data-ttu-id="0fb3d-736">Gebäudeergänzung</span><span class="sxs-lookup"><span data-stu-id="0fb3d-736">Building Complement</span></span> | <span data-ttu-id="0fb3d-737">Adresszeile 5</span><span class="sxs-lookup"><span data-stu-id="0fb3d-737">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="0fb3d-738">Ausweisnummer</span><span class="sxs-lookup"><span data-stu-id="0fb3d-738">Passport number</span></span>

<span data-ttu-id="0fb3d-739">Mitarbeiter können Ausweisinformationen melden.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-739">Employees can declare passport information.</span></span> <span data-ttu-id="0fb3d-740">Diese Informationen haben den Kennungstyp **Ausweis** und sind in Dayforce als Teil der für Mexiko spezifischen Informationen eines Mitarbeiters integriert.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-740">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="0fb3d-741">Kennungstyp = „Ausweis”</span><span class="sxs-lookup"><span data-stu-id="0fb3d-741">Identification Type = "Passport"</span></span>
- <span data-ttu-id="0fb3d-742">Ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="0fb3d-742">Issued Date</span></span>
- <span data-ttu-id="0fb3d-743">Ablaufdatum</span><span class="sxs-lookup"><span data-stu-id="0fb3d-743">Expiration Date</span></span>

<span data-ttu-id="0fb3d-744">Mitarbeiter können mehrere Kennungsnummern des Kennungstyps **Ausweis** melden.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-744">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="0fb3d-745">Jedoch wird nur der aktuell aktive Ausweiseintrag in Dayforce integriert.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-745">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="0fb3d-746">Wenn alle Ausweiseinträge abgelaufen sind, ist der Ausweis, der zuletzt ausgestellt wurde, in Dayforce integriert.</span><span class="sxs-lookup"><span data-stu-id="0fb3d-746">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>
