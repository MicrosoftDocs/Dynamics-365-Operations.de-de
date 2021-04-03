---
title: EU-Gelangensbestätigung
description: Dieser Artikel enthält Informationen zu Gelangensbestätigungen der Europäischen Union (EU).
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustEntryCertificateJour_W, CustParameters, CustTable, SalesTable
audience: Application User
ms.reviewer: kfend
ms.custom: 11464
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1e1f763bb818bbbbb4ced1ce03f175df725cebc4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5243566"
---
# <a name="eu-entry-certificates"></a><span data-ttu-id="93e6d-103">EU-Gelangensbestätigungen</span><span class="sxs-lookup"><span data-stu-id="93e6d-103">EU entry certificates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="93e6d-104">Dieser Artikel enthält Informationen zu Gelangensbestätigungen der Europäischen Union (EU).</span><span class="sxs-lookup"><span data-stu-id="93e6d-104">This article provides information about European Union (EU) entry certificates.</span></span>

<span data-ttu-id="93e6d-105">Sie können die folgenden Aufgaben für eine EU-Gelangensbestätigung ausführen:</span><span class="sxs-lookup"><span data-stu-id="93e6d-105">You can complete the following tasks for a European Union (EU) entry certificate:</span></span>

-   <span data-ttu-id="93e6d-106">Erstellen und geben Sie eine EU-Gelangensbestätigung mit einem Lieferschein oder der Debitorenrechnung für die Lieferung von Artikeln oder Dienstleistungen an EU-Länder/-Regionen aus.</span><span class="sxs-lookup"><span data-stu-id="93e6d-106">Create and issue an EU entry certificate together with a packing slip or customer invoice for the delivery of items or services to EU countries/regions.</span></span>
-   <span data-ttu-id="93e6d-107">Empfangen Sie die EU-Gelangensbestätigung, die von einem EU-Debitor unterzeichnet wurde.</span><span class="sxs-lookup"><span data-stu-id="93e6d-107">Receive the EU entry certificate that is signed by an EU customer.</span></span>
-   <span data-ttu-id="93e6d-108">Laden Sie die unterzeichnete EU-Gelangensbestätigung hoch, die vom Debitor oder von einem Dritten, der für die Lieferung von Artikeln an den Debitor zuständig ist, entgegengenommen wurde.</span><span class="sxs-lookup"><span data-stu-id="93e6d-108">Upload the signed EU entry certificate that is received either from the customer or from a third party who is responsible for delivering items to the customer.</span></span>
-   <span data-ttu-id="93e6d-109">Ordnen Sie die hochgeladene EU-Gelangensbestätigung einer Debitorenrechnung zu.</span><span class="sxs-lookup"><span data-stu-id="93e6d-109">Associate the uploaded EU entry certificate with a customer invoice.</span></span>
-   <span data-ttu-id="93e6d-110">Aktualisieren Sie den Status der hochgeladenen EU-Gelangensbestätigung.</span><span class="sxs-lookup"><span data-stu-id="93e6d-110">Update the status of the uploaded EU entry certificate.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="93e6d-111">Erforderliche Komponenten</span><span class="sxs-lookup"><span data-stu-id="93e6d-111">Prerequisites</span></span>
<span data-ttu-id="93e6d-112">In der folgenden Tabelle werden die Voraussetzungen angezeigt, die vorhanden sein müssen, bevor Sie beginnen können.</span><span class="sxs-lookup"><span data-stu-id="93e6d-112">The following table shows the prerequisites that must be in place before you start.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93e6d-113">Kategorie</span><span class="sxs-lookup"><span data-stu-id="93e6d-113">Category</span></span></th>
<th><span data-ttu-id="93e6d-114">Voraussetzung</span><span class="sxs-lookup"><span data-stu-id="93e6d-114">Prerequisite</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="93e6d-115">Land/Region</span><span class="sxs-lookup"><span data-stu-id="93e6d-115">Country/region</span></span></td>
<td><span data-ttu-id="93e6d-116">Die primäre Adresse der juristischen Person muss in einem EU-Mitgliedsstaat sein.</span><span class="sxs-lookup"><span data-stu-id="93e6d-116">The primary address of the legal entity must be in a EU member state.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93e6d-117">Zugehörige Einrichtungsaufgaben</span><span class="sxs-lookup"><span data-stu-id="93e6d-117">Related set up tasks</span></span></td>
<td><ul>
<li><span data-ttu-id="93e6d-118">Wählen Sie <strong>Verwaltung der Gelangensbestätigung aktivieren</strong> und <strong>Ausstellung der Gelangensbestätigung aktivieren</strong> auf der <strong>Debitorenparameter</strong>-Seite aus.</span><span class="sxs-lookup"><span data-stu-id="93e6d-118">On the <strong>Accounts receivable parameters</strong> page, select the <strong>Enable entry certificate management</strong> and <strong>Enable entry certificate issuing</strong> options.</span></span></li>
<li><span data-ttu-id="93e6d-119">Auf der <strong>Debitoren</strong>-Seite auf dem <strong>Rechnung und Lieferung</strong>-Inforegister, wählen Sie die <strong>Gelangensbestätigung erforderlich</strong>-Option aus, um anzugeben, dass eine EU-Gelangensbestätigung für den Debitor obligatorisch ist.</span><span class="sxs-lookup"><span data-stu-id="93e6d-119">On the <strong>Customers</strong> page, on the <strong>Invoice and delivery</strong> FastTab, select the <strong>Entry certificate required</strong> option to indicate that an EU entry certificate is mandatory for the customer.</span></span> <span data-ttu-id="93e6d-120">Aktivieren Sie die Option <strong>Gelangensbestätigung ausstellen</strong>, um eine EU-Gelangensbestätigung der juristischen Person für den Debitor auszustellen.</span><span class="sxs-lookup"><span data-stu-id="93e6d-120">Select the <strong>Issue entry certificate</strong> option to issue an EU entry certificate of the legal entity to the customer.</span></span></li>
<li><span data-ttu-id="93e6d-121">Wählen Sie auf der <strong>Debitorenparameter</strong>-Seite einen Nummernkreiscode für die <strong>Gelangensbestätigung</strong>-Referenz aus.</span><span class="sxs-lookup"><span data-stu-id="93e6d-121">On the <strong>Accounts receivable parameters</strong> page, select a number sequence code for the <strong>Entry certificate</strong> reference.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93e6d-122">Zugehörige Transaktionen</span><span class="sxs-lookup"><span data-stu-id="93e6d-122">Related transactions</span></span></td>
<td><ul>
<li><span data-ttu-id="93e6d-123">Erstellen eines Debitorenkontos.</span><span class="sxs-lookup"><span data-stu-id="93e6d-123">Create a customer account.</span></span></li>
<li><span data-ttu-id="93e6d-124">Erstellen Sie einen Auftrag.</span><span class="sxs-lookup"><span data-stu-id="93e6d-124">Create a sales order.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="creating-registering-and-uploading-an-eu-entry-certificate"></a><span data-ttu-id="93e6d-125">Erstellen, Erfassen und Hochladen einer EU-Gelangensbestätigung</span><span class="sxs-lookup"><span data-stu-id="93e6d-125">Creating, registering, and uploading an EU entry certificate</span></span>
<span data-ttu-id="93e6d-126">Sie können eine EU-Gelangensbestätigung automatisch oder manuell erstellen.</span><span class="sxs-lookup"><span data-stu-id="93e6d-126">You can create an EU entry certificate automatically or manually.</span></span> <span data-ttu-id="93e6d-127">Eine EU-Eingangssbestätigung wird automatisch erstellt und gedruckt, wenn Sie einen Lieferschein oder eine Rechnung für einen Debitor über die Seite **Lieferschein buchen** oder **Rechnung buchen**.</span><span class="sxs-lookup"><span data-stu-id="93e6d-127">An EU entry certificate is created and printed automatically when you post a packing slip or invoice for a customer by using the **Packing slip posting** page or the **Posting invoice** page.</span></span> <span data-ttu-id="93e6d-128">Um eine EU-Eingangsbestätigung für eine Kundenrechnung manuell zu erstellen oder neu zu drucken, verwenden Sie die Seite **Rechnungserfassung**.</span><span class="sxs-lookup"><span data-stu-id="93e6d-128">To manually create or reprint an EU entry certificate for a customer invoice, use the **Invoice journal** page.</span></span> <span data-ttu-id="93e6d-129">Darüber hinaus können Sie mithilfe der Seite **Gelangensbestätigungsjournal** Details zu einer EU-Gelangensbestätigung eingeben, die von einem Dritten ausgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="93e6d-129">Additionally, you can use the **Entry certificate journal** page to enter details about an EU entry certificate that is issued by a third party.</span></span>

### <a name="creating-an-eu-entry-certificate-automatically-or-manually"></a><span data-ttu-id="93e6d-130">Eine EU-Gelangensbestätigung automatisch oder manuell erstellen</span><span class="sxs-lookup"><span data-stu-id="93e6d-130">Creating an EU entry certificate automatically or manually</span></span>

<span data-ttu-id="93e6d-131">Sie können eine EU-Gelangensbestätigung automatisch erstellen, indem Sie einen Lieferschein auf der Seite **Alle Aufträge** verwenden, oder indem Sie eine Rechnung auf der Seite **Auftrag** verwenden.</span><span class="sxs-lookup"><span data-stu-id="93e6d-131">You can create an EU entry certificate automatically by using a packing slip on the **All sales orders** page or by using an invoice on the **Sales order** page.</span></span> <span data-ttu-id="93e6d-132">Um eine EU-Gelangensbestätigung manuell zu erstellen, können Sie eine Rechnung auf der Seite **Rechnungserfassung** verwenden.</span><span class="sxs-lookup"><span data-stu-id="93e6d-132">To manually create an EU entry certificate, you can use an invoice on the **Invoice journal** page.</span></span> <span data-ttu-id="93e6d-133">Sie müssen den Status einer Gelangensbestätigung der Rechnung ändern, bevor Sie eine EU-Gelangensbestätigung manuell erstellen.</span><span class="sxs-lookup"><span data-stu-id="93e6d-133">However, you must change the certification status of the invoice before you manually create an EU entry certificate.</span></span>

### <a name="registering-an-eu-entry-certificate"></a><span data-ttu-id="93e6d-134">Erfassen einer EU-Gelangensbestätigung</span><span class="sxs-lookup"><span data-stu-id="93e6d-134">Registering an EU entry certificate</span></span>

<span data-ttu-id="93e6d-135">Wenn eine Erfassung erforderlich ist, können Sie mithilfe der Seite **Gelangensbestätigungsjournal** Details zu einer EU-Gelangensbestätigung erfassen, die von einem Dritten ausgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="93e6d-135">If registration is required, you can use the **Entry certificate journal** page to register an EU entry certificate that is issued by a third party.</span></span>

### <a name="uploading-a-received-eu-entry-certificate"></a><span data-ttu-id="93e6d-136">Hochladen einer empfangenen EU-Gelangensbestätigung</span><span class="sxs-lookup"><span data-stu-id="93e6d-136">Uploading a received EU entry certificate</span></span>

<span data-ttu-id="93e6d-137">Verwenden Sie die Seite **Anhänge**, um eine empfangene EU-Gelangensbestätigung hochzuladen, die von einem EU-Debitor unterzeichnet wurde.</span><span class="sxs-lookup"><span data-stu-id="93e6d-137">Use the **Attachments** page to upload a received EU entry certificate that is signed by an EU customer.</span></span> <span data-ttu-id="93e6d-138">Nachdem die Bescheinigung hochgeladen wurde, können Sie sie als Nachweis der Lieferung der Artikel einer Rechnung zuordnen.</span><span class="sxs-lookup"><span data-stu-id="93e6d-138">After the certificate is uploaded, you can associate it with an invoice as proof that the items were delivered.</span></span> <span data-ttu-id="93e6d-139">Dieser Nachweis ist erforderlich wenn Sie eine Rechnung ausstellen müssen, die keine Mehrwertsteuer (VAT) umfasst. Sie wird außerdem während der Überwachung verwendet.</span><span class="sxs-lookup"><span data-stu-id="93e6d-139">This proof is required if you must issue an invoice that doesn't include value-added tax (VAT), and it's also used during auditing.</span></span>

### <a name="optional-updating-the-certification-status-and-printing-status-of-an-invoice"></a><span data-ttu-id="93e6d-140">Optional: Aktualisieren des Status der Gelangensbestätigung und Drucken des Status einer Rechnung</span><span class="sxs-lookup"><span data-stu-id="93e6d-140">Optional: Updating the certification status and printing status of an invoice</span></span>

<span data-ttu-id="93e6d-141">Sie können den Status der Gelangensbestätigung und den Druckstatus einer Debitorenrechnung aktualisieren, indem Sie die Seite **Rechnungserfassung** verwenden.</span><span class="sxs-lookup"><span data-stu-id="93e6d-141">You can update the entry certification status and printing status of a customer invoice by using the **Invoice journal** page.</span></span>

## <a name="technical-information-for-system-administrators"></a><span data-ttu-id="93e6d-142">Technische Informationen für Systemadministratoren</span><span class="sxs-lookup"><span data-stu-id="93e6d-142">Technical information for system administrators</span></span>
<span data-ttu-id="93e6d-143">Wenn Sie keinen Zugriff auf die Seiten für die Durchführung dieser Aufgabe haben, wenden Sie sich mit den Informationen aus der folgenden Tabelle an Ihren Systemadministrator.</span><span class="sxs-lookup"><span data-stu-id="93e6d-143">If you don't have access to the pages that are used to complete this task, contact your system administrator, and provide the information that is shown in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93e6d-144">Kategorie</span><span class="sxs-lookup"><span data-stu-id="93e6d-144">Category</span></span></th>
<th><span data-ttu-id="93e6d-145">Voraussetzung</span><span class="sxs-lookup"><span data-stu-id="93e6d-145">Prerequisite</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="93e6d-146">Sicherheitsrollen und Aufgaben</span><span class="sxs-lookup"><span data-stu-id="93e6d-146">Security roles and duties</span></span></td>
<td><span data-ttu-id="93e6d-147">Um eine EU-Gelangensbestätigung für Artikel oder Dienstleistungen einzurichten und zu erstellen, müssen Sie Mitglied einer Sicherheitsrolle sein, die die folgenden Aufgaben umfasst:</span><span class="sxs-lookup"><span data-stu-id="93e6d-147">To set up and create EU entry certificates for items or services, you must be a member of a security role that includes the following duties:</span></span>
<ul>
<li><span data-ttu-id="93e6d-148"><strong>Sachbearbeiter Debitoren</strong> (CustInvoiceAccountsReceivableClerk)</span><span class="sxs-lookup"><span data-stu-id="93e6d-148"><strong>Accounts receivable clerk</strong> (CustInvoiceAccountsReceivableClerk)</span></span></li>
<li><span data-ttu-id="93e6d-149"><strong>Kundendienstmitarbeiter</strong> (TradeCustomerServiceRepresentative)</span><span class="sxs-lookup"><span data-stu-id="93e6d-149"><strong>Customer service representative</strong> (TradeCustomerServiceRepresentative)</span></span></li>
<li><span data-ttu-id="93e6d-150"><strong>Verkaufssachbearbeiter</strong> (TradeSalesClerk)</span><span class="sxs-lookup"><span data-stu-id="93e6d-150"><strong>Sales clerk</strong> (TradeSalesClerk)</span></span></li>
<li><span data-ttu-id="93e6d-151"><strong>Sachbearbeiter Versand</strong> (InventShippingClerk)</span><span class="sxs-lookup"><span data-stu-id="93e6d-151"><strong>Shipping clerk</strong> (InventShippingClerk)</span></span></li>
</ul></td>
</tr>
</tbody>
</table>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]